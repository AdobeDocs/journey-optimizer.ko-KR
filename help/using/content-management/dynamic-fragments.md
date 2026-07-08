---
solution: Journey Optimizer
product: journey optimizer
title: 동적 조각 사용
description: Adobe Journey Optimizer에서 동적 조각 해상도를 사용하여 프로필 속성, 데이터 세트 조회 또는 컨텍스트 데이터를 기반으로 런타임 시 조각을 선택하고 삽입하는 방법을 알아봅니다.
feature: Fragments
topic: Content Management
role: User, Developer
level: Intermediate, Experienced
keywords: 동적, 조각, 표현식, 개인화, 런타임
source-git-commit: b4affc5b905236419928a65cd173173b49058827
workflow-type: tm+mt
source-wordcount: '1317'
ht-degree: 2%

---

# 동적 조각 사용 {#dynamic-fragments}

>[!BEGINSHADEBOX]

**이 페이지에서:** Adobe Journey Optimizer에서 동적 조각 해상도를 사용하여 프로필 특성, 데이터 세트 조회 또는 전송 시 전달된 컨텍스트 데이터를 기반으로 런타임 시 메시지에 삽입할 게시된 조각을 선택하는 방법을 알아봅니다.

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer]은(는) 런타임에 **동적 조각 확인**&#x200B;을(를) 지원하므로 전송 시 전달된 프로필 특성, 데이터 세트 조회 또는 컨텍스트 데이터를 기반으로 메시지에 삽입된 조각을 선택할 수 있습니다. 이렇게 하면 캠페인 또는 여정 논리를 복제하지 않고도 고도로 개인화된 콘텐츠를 사용할 수 있습니다.

## 개요 {#overview}

**정적 조각**&#x200B;은(는) 디자인 타임에 메시지에 포함됩니다. 모든 받는 사람에 대해 동일한 조각이 사용됩니다. **동적 조각**&#x200B;은(는) 받는 사람마다 런타임에 조각 ID를 확인합니다. 즉, 다른 프로필이 동일한 캠페인이나 여정 내에서 완전히 다른 콘텐츠 블록을 받을 수 있습니다.

동적 조각 ID는 다음 세 가지 소스에서 가져올 수 있습니다.

* **데이터 세트 조회** - 예: 스타일 또는 제품별로 입력된 권장 사항 데이터 세트
* Adobe Experience Platform에 저장된 **프로필 특성**
* 전송 시 API 요청에서 직접 전달된 **컨텍스트 데이터**

>[!NOTE]
>
>현재 제한된 고객 집합에서 식 조각 내의 `datasetLookup` 도우미 함수를 사용할 수 있습니다. 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.

## 사전 요구 사항 {#prerequisites}

동적 조각을 사용하기 전에 다음 사항이 준비되었는지 확인하십시오.

* [!DNL Journey Optimizer]에서 조각을 만들고 게시하는 데 필요한 권한이 있습니다. [자세히 알아보기](../administration/ootb-product-profiles.md#content-library-manager)
* 참조할 조각은 **게시됨**(상태: **라이브**)입니다. 런타임 시 초안 조각을 해결할 수 없습니다.
* 데이터 집합에서 조각 ID를 확인하는 경우 데이터 집합 스키마에는 조각 ID를 저장하는 필드가 포함되며 데이터 집합은 [조회에 사용](../data/lookup-aep-data.md)됩니다.
* 동적 조각 자체가 참조하는 모든 프로필 속성은 메시지 내보내기 경로에 포함되어 있거나 전송 시 프로필에서 사용할 수 있습니다.

>[!CAUTION]
>
>동적 조각 플로우에서는 조각 관련 유효성 검사를 건너뜁니다. 잘못된 조각 ID가 사전 유효성 검사 오류가 아닌 런타임 게재 오류로 표시됩니다. 캠페인을 활성화하기 전에 항상 참조된 조각 ID가 유효하고 게시되었는지 확인하십시오.

## 1단계: 조각 만들기 및 게시 {#create-fragment}

조각을 동적으로 참조하기 전에 [!DNL Journey Optimizer]에 게시해야 합니다.

1. [!DNL Journey Optimizer]에서 **[!UICONTROL 콘텐츠 관리]** > **[!UICONTROL 조각]**&#x200B;으로 이동합니다.

1. **[!UICONTROL 조각 만들기]**&#x200B;를 선택하고 콘텐츠를 작성합니다. [조각을 만드는 방법을 알아봅니다](create-fragments.md)

1. 콘텐츠가 준비되면 **[!UICONTROL 게시]**&#x200B;를 클릭합니다. 게시는 비동기적으로 수행되며 몇 초 정도 걸릴 수 있습니다. 계속하기 전에 조각 상태가 **Live**(으)로 변경되었는지 확인하십시오.

1. 조각 세부 사항 보기 또는 조각 API 응답에서 **조각 ID**&#x200B;을(를) 확인합니다. 메시지에서 이 ID를 참조합니다.

>[!NOTE]
>
>`GET /fragments` API를 사용하여 프로그래밍 방식으로 게시된 모든 조각 ID를 검색할 수 있습니다. 자세한 내용은 [Journey Optimizer API 설명서](https://developer.adobe.com/journey-optimizer-apis/references/content){target="_blank"}를 참조하세요.

## 2단계: 동적 조각 참조를 사용하여 메시지 작성 {#author-message}

개인화 편집기에서 다음 구문을 사용하여 동적 조각 자리 표시자를 삽입합니다.

```handlebars
{{fragment id=dynamic_fragment_id}}
```

식별자 `dynamic_fragment_id`은(는) 변수 이름입니다. 조각 조회가 수행되기 전에 해당 값을 확인해야 합니다. 데이터 세트 조회 표현식, 프로필 속성 또는 컨텍스트 데이터를 사용하여 해결합니다.

### 데이터 세트 조회에서 해결 {#resolve-from-dataset}

조각 ID가 AEP 데이터 세트(예: 스타일-조각 매핑 테이블)에 저장된 경우 `datasetLookup` 도우미 함수를 사용하여 해결하십시오.

```handlebars
{{
  {datasetLookup datasetId="<your-dataset-id>" key=profile.style attribute="fragmentId"}
}}

{{fragment id=dynamic_fragment_id}}
```

이 예제에서 데이터 집합에는 스타일 값으로 처리된 행(예: `style1`)이 포함되어 있습니다. 지정된 프로필의 경우 조회가 해당 `fragmentId` 열 값을 검색하여 `dynamic_fragment_id`에 할당하면 해당 값을 사용하여 조각을 확인합니다.

>[!NOTE]
>
>현재 제한된 고객 집합에서 식 조각 내의 `datasetLookup` 도우미 함수를 사용할 수 있습니다. 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오. 개인화의 데이터 집합 조회에 대한 자세한 내용은 [Adobe Experience Platform 데이터 사용](../data/lookup-aep-data.md)을 참조하세요.

### 컨텍스트 데이터에서 해결 {#resolve-from-context}

전송 시 조각 ID가 API 요청 컨텍스트의 일부로 제공되는 경우 `context` 네임스페이스를 사용하여 이를 참조합니다.

```handlebars
{{fragment id=context.audiencePayload.fragmentId}}
```

경로 `context.audiencePayload`은(는) CSV 대상 파일에서 가져온 또는 API 요청 컨텍스트를 통해 전달된 모든 특성에 필요한 접두사입니다. CSV의 열 이름(예: `fragmentId`)이 접두사를 따릅니다.

### 프로필 속성에서 확인 {#resolve-from-profile}

조각 ID가 Adobe Experience Platform에 프로필 속성으로 저장된 경우 다음을 직접 참조하십시오.

```handlebars
{{fragment id=profile.mi.fragmentId}}
```

## 3단계: 조회 접근 방식을 위한 데이터 세트 구성 {#configure-dataset}

데이터 세트 조회 접근 방식을 사용하는 경우 데이터 세트 스키마 및 데이터를 업데이트하여 조각 ID를 전달합니다.

1. 권장 사항 또는 매핑 데이터 집합에서 각 행에 게시된 AJO 조각 ID를 저장하는 열(예: `fragmentId`)을 추가합니다.

1. 각 스타일 또는 변형(예: `style1`, `style2`)에 대해 `fragmentId` 열을 해당 조각 ID로 채웁니다.

1. 데이터 집합이 Adobe Experience Platform에 수집되고 [조회를 위해 활성화됨](../data/lookup-aep-data.md)인지 확인하십시오.

1. 내보내기 시 빈 렌더링을 방지하기 위해 동적 조각 내에서 참조된 모든 프로필 속성이 메시지 또는 정적 조각에 캡처되는지 확인합니다.

**데이터 집합 구조 예:**

| 열 | 예제 값 |
|---|---|
| 스타일 | style1 |
| fragmentId | &lt;fragment-id-1> |
| 스타일 | style2 |
| fragmentId | &lt;fragment-id-2> |

## 4단계: 전송 시 컨텍스트 데이터 전달 {#pass-context-data}

컨텍스트 데이터(예: CSV 대상 권장 사항 파일)에서 조각 ID를 해결하는 경우 필수 컨텍스트 접두사 아래의 API 요청에서 조각 ID를 전달하십시오.

캠페인 증명 API를 사용하는 경우 `context` 개체에 조각 ID를 포함하십시오.

```json
{
  "recipients": [
    {
      "userId": "<profile-email>",
      "namespace": "email"
    }
  ],
  "inChannelData": {
    "channel": "email",
    "emailAddresses": ["<delivery-address>"]
  },
  "context": {
    "audiencePayload": {
      "fragmentId": "<published-fragment-id>",
      "systemSource": "<optional-system-value>"
    }
  }
}
```

접두사 `context.audiencePayload`이(가) 필요합니다. 라이브 캠페인을 실행할 때 이 키 맵 아래에 중첩된 속성을 CSV 대상 파일의 열에 직접 추가합니다.

## 5단계: 증명 및 유효성 검사 {#proof-validate}

캠페인을 활성화하기 전에 캠페인 증명 API를 사용하여 동적 조각이 올바르게 확인되는지 그리고 렌더링된 이메일 출력이 예상대로 작동하는지 확인합니다.

1. `POST /campaigns/{id}/proofs` 끝점을 사용하여 증명 작업을 트리거합니다. 증명 요청에서 `context.audiencePayload.fragmentId`에서 테스트할 조각 ID를 전달합니다.

1. 상태가 `Submitted` 또는 `Failed`이(가) 될 때까지 `GET /campaigns/{id}/proofs/{proofId}` 끝점을 사용하여 증명 작업 상태를 폴링합니다.

1. 전달된 이메일을 확인하여 올바른 조각 콘텐츠가 렌더링되었는지 확인합니다.

1. 조각 컨텐츠가 누락되었거나 잘못된 경우 조각 ID가 유효하고 조각이 게시되며 필요한 모든 프로필 속성이 있는지 확인합니다.

Campaign API에 대한 자세한 내용은 [Journey Optimizer API 설명서](https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve){target="_blank"}를 참조하세요.

## 가드레일 및 제한 사항 {#guardrails}

>[!CAUTION]
>
>OLAC(개체 수준 액세스 제어)는 동적 조각 모델의 조각에 적용되지 않습니다. 액세스 제어 요구 사항이 캠페인 및 대상자 수준에서 설명되는지 확인합니다.

동적 조각을 사용하는 경우 다음 제한 사항이 적용됩니다.

* **내보내기 시 프로필 특성 적용 범위**: 프로필당 런타임 시 조각이 선택됩니다. 동적 조각에 필요한 프로필 속성을 미리 알 수 없습니다. 동적 조각이 원래 메시지 또는 메시지에서 참조된 정적 조각에 없는 프로필 속성에 의존하는 경우 내보내기 경로에서 해당 필드가 비어 있게 렌더링될 수 있습니다.

* **미리 조각 유효성 검사 없음**: 이 흐름에서 조각 관련 유효성 검사를 건너뜁니다. 잘못되거나 게시되지 않은 조각 ID는 UI에 표시되는 유효성 검사 오류가 아니라 런타임 게재 오류로 표시됩니다.

* **데이터 세트 접근 방식에 필요한 스키마 변경**: ID별 조회 경로를 사용하려면 조각 ID를 저장하고 전달하는 데이터 세트 스키마를 업데이트해야 하며, 메시지 파이프라인에 해당 ID를 제공하는 데 필요한 배관도 필요합니다.

* **내보내기를 위한 특성 캡처**: 동적 조각 내에 사용된 모든 특성을 메시지 또는 정적 조각에 캡처하여 내보내기 경로에서 빈 렌더링을 방지하십시오.

조각에 적용되는 추가 보호 기능은 [이 섹션](../start/guardrails.md#fragments-guardrails)에서 사용할 수 있습니다.

## 오류 처리 {#error-handling}

동적 조각이 런타임 시 해결되지 않으면 영향을 받는 프로필에 대한 제외 이벤트가 생성됩니다. 현재 모든 조각 렌더링 실패는 단일 총괄 오류 유형으로 분류됩니다.

조각 해결 오류를 디버깅하려면

1. 캠페인 게재 보고서에서 제외 이벤트를 확인합니다.
1. 런타임 시 전달된 조각 ID가 게시된 조각과 일치하는지 확인합니다.
1. 조각에 필요한 모든 프로필 속성이 전송 시 프로필에 있는지 확인합니다.
1. 캠페인을 활성화하기 전에 [증명 API](#proof-validate)를 사용하여 특정 조각 ID를 테스트하십시오.
