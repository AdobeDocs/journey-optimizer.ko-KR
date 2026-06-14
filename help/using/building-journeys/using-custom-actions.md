---
solution: Journey Optimizer
product: journey optimizer
title: 사용자 정의 액션 사용
description: 사용자 지정 작업을 사용하는 방법 알아보기
feature: Journeys, Actions, Custom Actions
topic: Content Management
role: User, Developer
level: Intermediate
keywords: 작업, 사용자 지정, API, 여정, 구성, 서비스
exl-id: 2b1b3613-3096-43ec-a860-600dda1d83b2
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/Sw-hR0cfAG8Lk8YbhJKj53UqG-er2bC3-7Ijih0PF44
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: c2beecbb-b93e-4ae3-baa9-72adcdc06781id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: e0eb8757-182f-49f3-94a4-1587d16f5094id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: a5d9be4fcfcb52bb1ee65096262e18feaa2ce4b1
workflow-type: tm+mt
source-wordcount: 482
ht-degree: 18%

---

# 사용자 정의 액션 사용 {#use-custom-actions}

>[!BEGINSHADEBOX]

**이 페이지에서:** 데이터 거버넌스 및 동의 정책을 적용하는 동안 사용자 지정 작업을 사용하여 JSON 페이로드가 있는 REST API 호출을 통해 여정을 서드파티 시스템에 연결하는 방법을 알아봅니다.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom"
>title="사용자 정의 액션"
>abstract="사용자 정의 액션에서는 메시지나 API 호출을 전송할 서드파티 시스템의 연결을 구성할 수 있습니다. JSON 형식 페이로드를 사용하여 REST API를 통해 호출할 수 있는 모든 공급자의 어떤 서비스로든 작업을 구성할 수 있습니다."

사용자 지정 작업을 사용하여 메시지 또는 API 호출을 전송할 서드파티 시스템에 대한 연결을 활성화합니다. JSON 형식 페이로드를 사용하여 REST API를 통해 호출할 수 있는 모든 공급자의 어떤 서비스로든 작업을 구성할 수 있습니다.

[이 섹션](../action/action.md)에서 사용자 지정 작업에 대해 자세히 알아보세요.

[이 페이지](../action/about-custom-action-configuration.md)에서 사용자 지정 작업을 만들고 구성하는 방법에 대해 알아봅니다.

[이 페이지](../action/action-response.md)에서 개인화를 위해 사용자 지정 작업의 API 호출 응답을 사용하는 방법을 알아봅니다.

## 동의 및 데이터 거버넌스 {#privacy}

Journey Optimizer에서는 데이터 거버넌스 및 동의 정책을 사용자 지정 작업에 적용하여 특정 필드가 서드파티 시스템으로 내보내지지 않도록 하거나 이메일, 푸시 또는 SMS 통신 수신에 동의하지 않은 고객을 제외할 수 있습니다. 자세한 내용은 다음 페이지를 참조하십시오.

* [데이터 거버넌스](../action/action-privacy.md)
* [동의](../action/consent.md).

## URL 구성

**사용자 지정 작업** 활동의 구성 창에는 사용자 지정 작업에 대해 구성된 URL 구성 매개 변수와 인증 매개 변수가 표시됩니다. 여정에서 URL의 정적 부분을 설정할 수 없지만 사용자 지정 작업의 전역 구성에서는 설정할 수 있습니다. [자세히 알아보기](../action/about-custom-action-configuration.md)

### 동적 경로

URL에 동적 경로가 포함된 경우 **[!UICONTROL 경로]** 필드에 경로를 지정하십시오.

필드와 일반 텍스트 문자열을 연결하려면 고급 표현식 편집기에서 String 함수 또는 더하기 기호(+)를 사용하십시오. 일반 텍스트 문자열을 작은따옴표(&#39;) 또는 큰따옴표(&quot;)로 묶습니다. [자세히 알아보기](expression/expressionadvanced.md)

이 표에서는 구성의 예를 보여 줍니다.

| 필드 | 값 |
| --- | --- |
| URL | `https://xxx.yyy.com:8080/somethingstatic/` |
| 경로 | `The _id + '/messages'` |

연결된 URL의 형식은 다음과 같습니다.

`https://xxx.yyy.com:8080/somethingstatic/`\&lt;ID>`/messages`

![동적 매개 변수 매핑을 사용한 사용자 지정 작업 URL 구성](assets/journey-custom-action-url.png)

### 헤더 및 쿼리 매개 변수 {#headers}

**[!UICONTROL URL 구성]** 섹션에는 동적 헤더 및 쿼리 매개 변수 필드가 표시되지만 상수 필드는 표시되지 않습니다. 동적 헤더 및 쿼리 매개 변수 필드는 작업 구성 화면에서 변수로 정의됩니다. [자세히 알아보기](../action/about-custom-action-configuration.md#url-configuration)

동적 헤더 및 쿼리 매개 변수 필드의 값을 지정하려면 필드 내부 또는 연필 아이콘을 클릭하고 원하는 필드를 선택합니다.

사용자 지정 작업의 ![동적 헤더 필드 구성](assets/journey-dynamicheaderfield.png)

## 작업 매개 변수

**[!UICONTROL 작업 매개 변수]** 섹션에서 _&quot;변수&quot;_(으)로 정의된 메시지 매개 변수를 볼 수 있습니다. 이러한 매개 변수의 경우 이 정보를 가져올 위치(예: 이벤트, 데이터 소스)를 정의하거나, 값을 수동으로 전달하거나, 고급 사용 사례에 고급 표현식 편집기를 사용할 수 있습니다. 고급 사용 사례는 데이터 조작 및 기타 함수 사용일 수 있습니다. 이 [페이지](expression/expressionadvanced.md)를 참조하세요.

