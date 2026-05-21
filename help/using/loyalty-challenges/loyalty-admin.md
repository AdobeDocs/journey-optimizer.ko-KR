---
solution: Journey Optimizer
product: journey optimizer
title: 충성도 프로그램 구성
description: Adobe Journey Optimizer에서 충성도 프로그램에 대한 보상 제공자, 이벤트 정의 및 조직 수준 설정을 구성하는 방법에 대해 알아봅니다.
feature: Journeys
topic: Content Management
role: Admin
level: Intermediate
hide: true
badge: label="비공개 베타" type="Informative"
mini-toc-levels: 1
exl-id: f8a3b2c1-4d5e-6f7a-8b9c-0d1e2f3a4b5c
source-git-commit: a4ad533e54f3692eb0483138a8cfd1cee0e77ba1
workflow-type: tm+mt
source-wordcount: '1128'
ht-degree: 2%

---

# 충성도 프로그램 구성 {#loyalty-admin}

>[!BEGINSHADEBOX]

**충성도 과제 설명서:**

* [충성도 문제 시작](get-started.md)
* [과제 및 작업 액세스 및 관리](access-loyalty-challenges.md)
* [과제 만들기](create-challenges.md)
* [작업 만들기](create-tasks.md)
* [충성도 과제 성능 모니터링](loyalty-reporting.md)
* **충성도 프로그램 구성** ◀︎**현재 상태**
* [충성도 과제 API 참조](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>이 기능은 현재 **개인 베타**&#x200B;에 있습니다. 릴리스 주기 및 가용성 단계에 대한 자세한 내용은 [Journey Optimizer 릴리스 주기](../rn/releases.md)를 참조하십시오.

**[!UICONTROL 충성도 관리자]** 섹션에서 Journey Optimizer이 외부 충성도 시스템에 연결하는 방법을 구성할 수 있습니다. 마케터는 **[!UICONTROL 충성도 과제(Beta)]**&#x200B;를 사용하여 과제, 작업, 콘텐츠 및 메시지를 디자인합니다. **[!UICONTROL 충성도 관리자]**&#x200B;는 보상 이행, 이벤트 매핑 및 제품 인벤토리를 위한 별도의 관리자 전용 영역입니다.

고객이 도전을 완료하거나 보상 이정표에 도달하면 Journey Optimizer은 점수 또는 기타 보상을 제공하도록 구성한 보상 제공자를 호출합니다. **[!UICONTROL 충성도 관리자]**&#x200B;의 구성은 **[!UICONTROL 콘텐츠]**, **[!UICONTROL 메시징]** 또는 **[!UICONTROL 대상]** 설정에 영향을 주지 않습니다. 이러한 설정은 마케터가 제어합니다.

## 여기에서 구성하는 것과 충성도 문제 비교 {#scope}

| 영역 | 충성도 관리자에서 구성됨 | 충성도 문제 구성 |
|------|----------------------------|----------------------------------|
| 보상 이행 API | 예 — 보상 제공자 | 아니오 — 공급자 및 금액만 선택합니다. |
| 사용자 지정 활동에 대한 이벤트 매핑 | 예 — 이벤트 정의 | 아니요 — 사용자 지정 이벤트 작업에서 이벤트 이름을 선택합니다. |
| 제품 그룹 매핑 | 예 — 제품 재고 | 없음 — 구매/지출 태스크를 작성할 때 그룹을 사용합니다. |
| 과제 구조, 콘텐츠, 대상자 | 아니요 | 예 |

Adobe Journey Optimizer은 고객이 보상을 획득하면 보상 공급자에게 이행 호출을 보냅니다. 충성도 플랫폼은 멤버의 계정을 대변에 기입합니다.

## 사전 요구 사항 {#prerequisites}

**[!UICONTROL 충성도 관리자]**&#x200B;는 조직당 적은 수의 관리자를 위한 것입니다. [충성도 문제](get-started.md#prerequisites)에 필요한 권한 외에 Journey Optimizer 인스턴스에 대한 관리자 수준의 액세스 권한이 필요합니다. 액세스 권한을 요청하려면 Adobe 관리자에게 문의하십시오.

## 충성도 관리자 액세스 {#access-loyalty-admin}

**[!UICONTROL 충성도 관리자]**&#x200B;를 열려면 Journey Optimizer의 왼쪽 탐색에서 선택합니다.

<!-- SCREENSHOT: Loyalty Admin entry in the left navigation -->

**[!UICONTROL 충성도 관리자]**&#x200B;가 탭으로 구성되어 있습니다. **[!UICONTROL 전역 설정]**, **[!UICONTROL 보상 공급자]**, **[!UICONTROL 이벤트 정의]** 및 **[!UICONTROL 제품 인벤토리]**. 사용 가능한 탭은 조직의 권한 및 기능 구성에 따라 다릅니다.

## 전역 설정 {#global-settings}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_global_settings"
>title="전역 설정"
>abstract="충성도 프로그램을 위한 Adobe Experience Platform ID 네임스페이스를 선택하고 구성 ID를 복사합니다. 보상 제공자가 보상을 올바르게 이행하려면 이러한 조직 수준 설정이 필요합니다."

**[!UICONTROL 전역 설정]**&#x200B;을 사용하여 충성도 문제를 위한 조직 전체의 옵션을 구성하십시오.

1. **[!UICONTROL 전역 설정]** 탭을 엽니다.

1. **[!UICONTROL 네임스페이스]** 드롭다운에서 충성도 프로그램에서 사용하는 [ID 네임스페이스](https://experienceleague.adobe.com/ko/docs/experience-platform/identity/features/namespaces)을(를) 선택합니다.

1. 충성도 과제 구성에 네임스페이스를 적용하려면 **[!UICONTROL 저장]**&#x200B;을(를) 선택하십시오.

1. 구현 팀이나 외부 시스템과 공유해야 하는 경우(예: 인바운드 이벤트 게재를 구성할 때) **[!UICONTROL 구성 ID]**&#x200B;를 복사하십시오.

<!-- SCREENSHOT: Global settings tab showing namespace drop-down, Save, and Configuration ID -->

## 보상 제공자 {#reward-providers}

**보상 공급자**&#x200B;는 도전 진행률이 기록되거나 도전이 완료되면 이행 호출을 보낼 위치를 Journey Optimizer에 알려줍니다(예: 회원 계정에 충성도 점수 또는 스타트를 크레딧하는 API).

보상 제공자 구성은 다음과 같습니다.

* 기본 연결 세부 정보(이름, 설명, API URL, 헤더)
* **[!UICONTROL 보상 정의]** — 이 공급자가 발급할 수 있는 보상 유형(예: stars 또는 miles)
* **[!UICONTROL 보상 프록시]**(선택 사항) - 호출이 끝점 대신 직접 라우팅되는 중간 프록시
* **[!UICONTROL 인증 토큰 생성기]** - Journey Optimizer이 API를 호출하기 전에 액세스 토큰을 가져오는 데 사용하는 메커니즘

### 보상 제공자 만들기 {#create-reward-provider}

1. **[!UICONTROL 보상 공급자]** 탭을 열고 **[!UICONTROL 보상 공급자 만들기]**&#x200B;를 선택합니다.

1. 이행 요청을 받는 **[!UICONTROL 이름]**, **[!UICONTROL 설명]** 및 **[!UICONTROL API URL]**&#x200B;을(를) 입력하십시오.

1. 필요에 따라 API(예: API 키 또는 콘텐츠 유형)에 **[!UICONTROL 헤더]**&#x200B;를 추가합니다.

1. **[!UICONTROL 보상 정의]** 구성 - 공급자가 지원하는 보상 유형당 하나의 항목(예: 프로그램 포인트 또는 별)입니다. 각 정의에 대해 다음 작업을 수행합니다.

   * 이행 호출과 함께 전송된 **페이로드**&#x200B;를 지정하십시오.
   * 필요한 경우 하나의 정의를 이 공급자에 대한 **default**(으)로 표시합니다.

1. 선택적으로 **[!UICONTROL 보상 프록시]**&#x200B;를 구성하여 중간 서버를 통해 이행 호출을 라우팅합니다.

   * **[!UICONTROL 이름]**, **[!UICONTROL 설명]** 및 프록시가 **활성화됨**&#x200B;인지 여부
   * **[!UICONTROL 호스트]**, **[!UICONTROL 포트]** 및 자격 증명

1. API에 인증을 위한 전달자 토큰이 필요한 경우 **[!UICONTROL 인증 토큰 생성기]**&#x200B;를 구성하십시오.

   * 토큰 끝점 URL 및 HTTP 메서드(예: OAuth 스타일 흐름의 경우 **POST**)
   * 응답의 **[!UICONTROL 토큰 키]**(예: `access_token`)
   * 토큰 엔드포인트에 필요한 헤더

   Journey Optimizer은 보상 API를 호출하기 전에 이 구성을 사용하여 새 토큰을 얻습니다.

1. **[!UICONTROL 보상 공급자 만들기]**&#x200B;를 선택하십시오. 공급자와 구성된 모든 하위 리소스가 함께 저장됩니다.

<!-- SCREENSHOT: Reward provider creation form with definitions, proxy, and auth token sections -->

저장하면 보상 제공자 목록에 제공자가 나타납니다. 마케터는 [도전 보상을 구성](create-challenges.md#rewards)할 때 이 공급자를 선택합니다.

기존 보상 공급자를 편집하려면 **[!UICONTROL 보상 공급자]** 탭을 열고 공급자를 선택한 다음 필드를 업데이트하십시오. 하위 리소스(보상 정의, 프록시, 인증 토큰 생성기)를 업데이트하면 변경 사항이 저장됩니다.

<!-- SCREENSHOT: Reward provider detail view with child resource sections -->

>[!NOTE]
>
>**[!UICONTROL 자신의 데이터를 가져오세요]** 도전은 자신의 데이터 통합을 통해 보상을 충족합니다. 여기에 구성된 보상 제공자는 이러한 문제에 적용되지 않습니다. [데이터 문제 해결에 대해 자세히 알아보기](create-challenges.md#create-the-challenge).

## 이벤트 정의(선택 사항) {#event-definitions}

**[!UICONTROL 이벤트 정의]** 브랜드에서 사용하는 JSON 또는 XDM 형식에서 시스템의 경험 이벤트를 충성도 문제가 발생할 수 있는 활동(특히 **[!UICONTROL 사용자 지정 이벤트]** 작업)에 매핑합니다. 이벤트가 도착하면 Journey Optimizer은 이러한 정의를 사용하여 이벤트를 처리할지 여부를 결정합니다. 정의와 일치하지 않는 이벤트는 무시됩니다.

### 이벤트 정의 만들기 {#create-event-definition}

1. **[!UICONTROL 이벤트 정의]** 탭을 열고 새 정의를 만듭니다.

1. 이벤트의 **[!UICONTROL 이름]**(예: `Coffee purchase`)을 입력하십시오. 이는 마케터가 **[!UICONTROL 사용자 지정 이벤트]** 작업을 구성할 때 표시되는 이름입니다.

1. 수신 페이로드에서 이벤트를 식별하는 방법을 지정합니다.

   * **[!UICONTROL 식별자 경로]** — 이벤트 또는 멤버를 식별하는 필드의 JSON 경로(예: `data.memberId`)
   * **[!UICONTROL 식별자 값]** — 이 정의를 일치시키기 위해 존재해야 하는 값

1. 필요한 경우 이벤트 페이로드가 Experience Platform 스키마를 따르는 경우 **[!UICONTROL XDM 스키마 ID]**&#x200B;를 지정하십시오.

1. 필요한 경우 **[!UICONTROL 스키마]** 및 **[!UICONTROL 변환기]** 필드를 사용하여 들어오는 JSON의 구문 분석 및 유효성 검사를 위한 사용자 지정 스키마 및 변환 문자열을 제공합니다.

   이벤트 구성 방식에 따라 XDM 스키마 ID, 식별자 경로 또는 둘 다 제공할 수 있습니다.

1. 이벤트 정의를 저장합니다.

<!-- SCREENSHOT: Event definition form with identifier path, values, and schema fields -->

대부분의 조직에서는 추적하려는 활동당 하나(예: 구매, 체크인 또는 사이트 방문)의 여러 이벤트 정의를 만듭니다. [어려움에서 사용자 지정 이벤트 작업을 사용하는 방법에 대해 알아보세요](create-tasks.md#choose-activity).

## 제품 재고(선택 사항) {#product-inventory}

**[!UICONTROL 제품 인벤토리]** 탭을 사용하여 제품 또는 항목 식별자(예: MPG ID)를 제품 그룹에 매핑하는 CSV 파일을 업로드하십시오. 그런 다음 마케터는 개별 SKU를 입력하는 대신 작업 자격 규칙에서 이러한 그룹을 참조할 수 있습니다.

1. **[!UICONTROL 제품 인벤토리]** 탭을 엽니다.

1. 매핑 파일을 업로드합니다.

1. 인벤토리 목록에서 가져온 매핑을 검토합니다. 제품 그룹을 선택하여 해당 그룹의 모든 항목을 보거나 검색을 사용하여 이름 또는 ID로 항목을 찾습니다.

1. **[!UICONTROL 업로드 기록]**&#x200B;을 사용하여 이전 업로드를 확인합니다.

<!-- SCREENSHOT: Product inventory list after CSV upload -->

>[!NOTE]
>
>제품 인벤토리에 대한 **[!UICONTROL 전역 제외]**&#x200B;는 향후 릴리스로 예정되어 있으며 여기에 문서화되지 않습니다.
