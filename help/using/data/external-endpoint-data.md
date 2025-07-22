---
solution: Journey Optimizer
product: journey optimizer
title: 외부 엔드포인트의 데이터를 사용하여 콘텐츠 개인화
description: 외부 엔드포인트에서 데이터를 동적으로 가져와서 인바운드 콘텐츠를 개인화하는 방법을 알아봅니다.
badge: label="제한 공개" type="Informative"
feature: Personalization, Rules
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: 표현식, 편집기
source-git-commit: f5d1bc27afadbf875fe4dd3149ce090a8773e0f9
workflow-type: tm+mt
source-wordcount: '1174'
ht-degree: 0%

---


# 외부 엔드포인트의 데이터를 사용하여 콘텐츠 개인화 {#data-endpoint}

>[!AVAILABILITY]
>
>이 기능은 조직 집합(제한된 가용성)에만 사용할 수 있습니다.

Journey Optimizer을 사용하면 외부 끝점의 데이터를 활용하여 코드 기반 경험, 웹 및 인앱 메시지 채널과 같은 인바운드 채널에서 콘텐츠를 개인화할 수 있습니다.

이를 위해 개인화 편집기에서 전용 도우미 함수 `externalDataLookup`을(를) 사용할 수 있습니다. 도우미를 사용하려면 먼저 외부 끝점에 대한 세부 정보를 구성하는 [!DNL Journey Optimizer] **Action**&#x200B;을(를) 정의해야 합니다.

## 반드시 알아야 할 사항

### 런타임 실행

인바운드 작업에 externalDataLookup 도우미가 포함된 경우 [!DNL Adobe Experience Platform] Edge Network에서 개인화 요청을 받고 처리할 때 끝점이 동적으로 호출됩니다. 즉, 외부 끝점은 클라이언트가 지정된 표면에 대해 AEP Edge Network으로 전송하는 만큼의 동시 로드 및 처리량을 처리할 수 있어야 합니다.

### 인증

현재 externalDataLookup 도우미에서 작업 구성의 인증 옵션을 지원하지 않습니다.
그동안 API 키 기반 인증 또는 기타 일반 텍스트 인증 키의 경우 작업 구성에서 헤더 필드로 지정할 수 있습니다.
Adobe 내부 종단점의 경우: 종단점에 대한 서비스 토큰 기반 인증을 활성화하려면 AJO Engineering에 문의하십시오.

### 보호 및 제한 사항

AJO 인바운드 채널 캠페인 및 여정의 사용자 지정 작업 #GuardrailsandGuidelines 참조하십시오.

기본적으로 AJO은 외부 끝점을 호출할 때 300ms의 시간 제한을 사용합니다. 끝점에 대한 이 시간 제한을 늘리려면 AJO 엔지니어링 팀에 문의하십시오.
Personalization 편집기에서 AJO은 표현식을 삽입할 때 끝점 응답의 스키마를 찾을 수 없으며 표현식에 사용된 응답에서 JSON 속성에 대한 참조의 유효성을 검사하지 않습니다.
externalDataLookup 도우미를 통해 대체할 페이로드 변수 매개 변수에 대해 지원되는 데이터 유형은 String, Integer, Decimal, Boolean, listString, listInt, listInteger, listDecimal입니다.
작업 구성 변경 사항은 라이브 캠페인 및 여정의 해당 externalDataLookup 호출에 반영되지 않습니다. 변경 사항을 반영하려면 externalDataLookup 도우미에서 작업을 사용하는 모든 라이브 캠페인 또는 여정을 복사하거나 수정해야 합니다.
아직 외부 데이터 조회 도우미 매개 변수 내에서는 변수 사용이 지원되지 않습니다.
동적 URL 경로는 현재 지원되지 않습니다.  - 인바운드 사용자 지정 작업 개선 사항#DynamicPathSegments

## 작업 만들기

작업을 만들어 조회에 대한 끝점을 구성합니다. 이 작업은 각 끝점에 대해 한 번만 수행하면 되며 기술 사용자가 수행해야 합니다. 이 페이지를 참조하십시오.

여정에서 콘텐츠를 가져오는 **[!UICONTROL 사용자 지정 작업]** 활동과 여정 또는 캠페인의 인바운드 작업에서 데이터를 가져오는 `externalDataLookup` 도우미 함수에서 모두 동일한 작업을 사용할 수 있습니다.

**[!UICONTROL 관리]** / **[!UICONTROL 구성]** 메뉴로 이동합니다.

작업 ID를 기록하고 6단계에서 사용할 ID를 복사합니다.


## 가져온 데이터를 사용하여 콘텐츠 개인화

### 콘텐츠에 도우미 함수 추가

1. 인바운드 캠페인 또는 여정 작업을 만들고 콘텐츠를 편집합니다.

1. 외부 끝점에서 가져온 데이터를 사용할 콘텐츠를 찾고 개인화 편집기에 액세스합니다.

1. 도우미 함수 메뉴를 선택하고 `externalDataLookup` 도우미 함수를 찾습니다.

1. 관련 구문을 코드에 삽입하고 `actionId` 및 `result` 매개 변수 값을 다음과 같이 바꾸려면 선택하십시오.

   * `actionId` : 작업을 만들 때 복사한 작업 nID를 붙여넣습니다.
   * `result`: 이 매개 변수를 선택한 이름으로 설정합니다. 이 결과 변수를 사용하여 가져온 콘텐츠에 액세스합니다.

1. 끝점 호출의 일부로 전달될 변수 매개 변수 값을 추가합니다. 예를 들어 언어 매개 변수와 최대 항목 매개 변수를 전달하는 방법은 다음과 같습니다.

### 가져온 데이터를 사용하여 개인화

외부 끝점 조회 호출에서 가져온 데이터에 액세스하려면 개인화 표현식 및 도우미 함수를 사용하여 작업 정의의 응답 페이로드에 정의된 필드를 참조할 수 있습니다.

가져온 데이터에 액세스하고 인바운드 작업을 위해 콘텐츠에 삽입하려면 `result` 변수를 사용하십시오. 예를 들어 엔드포인트에서 가져온 항목의 JSON 배열을 반환하는 방법은 다음과 같습니다.

작업의 응답 페이로드가 다음과 같이 구성된 아래 예를 살펴보겠습니다.

```
{
    "videos": [
        {
            "id": "integer",
            "title": "string",
            "description": "string",
            "thumbnail_url": "string",
            "video_page_url": "string",
            "url": "string",
            "video_type": "string",
            "start_timestamp": "dateOnly",
            "created_on": "dateOnly",
            ...
        }
    ]
}
```

Personalization 예제 1 - 코드 기반 Experience HTML 작업에 첫 번째 비디오의 설명을 표시합니다.

```
{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result"}}
 
First video description: <b>result.videos[0].description</b>
```

Personalization 예제 2 - 코드 기반 경험 JSON 작업에서 항목 배열 반환:

```
{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result"}}
 
[
{{#each result.videos as |item|}}
    {                                                  
        "title": "{{item.title}}",
        "url": "{{item.video_page_url}}",
        "thumbnail_url": "{{item.thumbnail_url}}",
        "start_timestamp": "{{item.start_timestamp}}"
    },
{{/each}}
]
```

## 시간 초과 및 오류 처리

AJO은 AEP Edge Network에 대해 짧은 지연 시간, 높은 처리량 성능 특성을 유지하기 위해 외부 끝점을 호출할 때 엄격한 시간 제한을 사용합니다.

끝점이 시간 초과되거나 끝점에 도달하는 다른 종류의 오류가 있는 경우 결과 변수는 비어 있습니다. 이 경우 결과 변수 내의 속성에 대한 모든 참조도 비어 있게 됩니다. 콘텐츠에 속성을 단순히 표시하는 경우 공백으로 표시됩니다. 결과에서 배열 특성을 반복하려고 하면 항목이 반환되지 않습니다.

대체 콘텐츠를 표시하여 시간 초과나 오류를 보다 적절하게 처리하려는 경우 조회 결과가 비어 있는지 확인하고 대체 콘텐츠를 표시할 수 있습니다.

예를 들어 다음과 같이 단일 속성에 대한 대체 값을 표시할 수 있습니다.

첫 번째 비디오 설명: {%=result.videos[0].description ?: &quot;없음&quot; %}


또는 다음과 같이 컨텐츠 전체 블록을 조건부로 렌더링할 수 있습니다.

{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result"}}

{%#if result%}
... 결과를 토대로 작업 수행 ...
{%else%}
... 대체 콘텐츠 반환 ...
{%/if%}
디버깅
디버깅에 도움이 되도록 외부 데이터 조회에 대한 시간 제한 및 오류 세부 정보가 AEP Assurance의 Edge Delivery 보기에 포함되어 있습니다. 인바운드 작업에서 externalDataLookup 도우미에 대한 예상 결과가 표시되지 않는 경우 Assurance 세션을 시작하고, 웹 또는 모바일 구현에서 AJO 호출을 시작하고, Edge Delivery 보기를 사용하여 시간 초과 또는 오류 세부 정보를 확인할 수 있습니다.

예:

실행 세부 정보의 일부로서 보증 추적의 Edge Delivery 섹션 아래에 새 customActions 블록이 추가되었습니다.

아래 요청과 유사한 요청 및 응답 세부 정보. 오류 섹션은 사용자 지정 작업을 실행하는 동안 문제가 있는 경우 디버깅에 도움이 됩니다

## 자주 묻는 질문

+++요청의 컨텍스트 특성을 매개 변수로 외부 데이터 조회에 전달하는 방법

컨텍스트 속성 > 데이터스트림 > 이벤트 메뉴를 사용하여 사용 중인 경험 이벤트 스키마를 검색하고 관련 속성을 다음과 같은 매개 변수 값으로 삽입합니다.

`{{externalDataLookup actionId="..." result="result" query.myQueryParameter=context.datastream.event.<schemaId>.my.xdm.attribute}}`

+++

+++AJO에서 외부 엔드포인트 응답을 캐싱합니까?

현재는 지원되지 않습니다. 이 기능은 향후에 지원됩니다.

+++









구문
{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result" optional-parameters...}}



매개 변수 전달
외부 끝점이 호출되면 작업에 정의된 모든 상수 헤더 값, 쿼리 매개 변수 및 요청 페이로드 값이 작업 구성에 지정된 값과 함께 전송됩니다.

변수 헤더 값, 쿼리/경로 매개 변수 또는 요청 페이로드 값의 경우 매개 변수를 사용하여 값을 externalDataLookup 도우미에 동적으로 전달할 수 있습니다.

매개 변수 이름:

헤더 매개 변수: header.&lt;parameter-name>
쿼리 매개 변수: query.&lt;parameter-name>
페이로드 매개변수: 페이로드.&lt;parameter-name>
경로 매개 변수: dynamic_path.&lt;parameter-name>
예:

{{externalDataLookup actionId="..." result="result" header.myHeaderParameter="value1" query.myQueryParameter="value2" payload.myPayloadParameter="value3"}}
매개 변수 값은 고정 값일 수 있으며, 프로필 필드 또는 기타 컨텍스트 속성을 참조하여 개인화할 수 있습니다. 예:

{{externalDataLookup actionId="..." result="result" query.myQueryParameter=profile.myProfileValue}}
페이로드 매개 변수는 다음과 같이 중첩된 JSON 속성을 참조하는 점 표기법을 사용하여 제공할 수 있습니다.

{{externalDataLookup actionId="..." result="result" payload.context.channel="web"}}