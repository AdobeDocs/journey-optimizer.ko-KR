---
title: 사용자 지정 작업 사용
description: 사용자 지정 작업 사용 방법 알아보기
feature: Actions
topic: Content Management
role: User
level: Intermediate
exl-id: 2b1b3613-3096-43ec-a860-600dda1d83b2
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 19%

---

# 사용자 지정 작업 사용 {#use-custom-actions}

사용자 지정 작업에서는 메시지나 API 호출을 전송할 서드파티 시스템의 연결을 구성할 수 있습니다. JSON 형식 페이로드를 사용하여 REST API를 통해 호출할 수 있는 모든 공급자의 어떤 서비스로든 작업을 구성할 수 있습니다.

## URL 구성

의 구성 창 **사용자 지정 작업** 활동은 사용자 지정 작업에 대해 구성된 URL 구성 매개 변수와 인증 매개 변수를 보여줍니다. 여정에서 URL의 정적 부분을 설정할 수 없지만 사용자 지정 작업의 전역 구성에서는 설정할 수 없습니다. [자세히 알아보기](../action/about-custom-action-configuration.md).

### 동적 경로

URL에 동적 경로가 포함된 경우에는 경로에 **[!UICONTROL Path]** 필드.

필드와 일반 텍스트 문자열을 연결하려면 고급 표현식 편집기에서 String 함수 또는 Plus 기호(+)를 사용하십시오. 일반 텍스트 문자열을 작은따옴표(&#39;)로 묶거나 큰따옴표(&quot;)로 묶습니다. [자세히 알아보기](expression/expressionadvanced.md).

이 표에서는 구성의 예를 보여 줍니다.

| 필드 | 값 |
| --- | --- |
| URL | `https://xxx.yyy.com:8080/somethingstatic/` |
| 경로 | `The id of marketingCampaign + '/messages'` |

연결된 URL에는 다음 양식이 있습니다.

`https://xxx.yyy.com:8080/somethingstatic/`\&lt;campaign id=&quot;&quot;>`/messages`

![](assets/journey-custom-action-url.png)

### 헤더

다음 **[!UICONTROL URL Configuration]** 섹션에는 동적 헤더 필드가 표시되지만, 상수 헤더 필드는 표시되지 않습니다. 동적 헤더 필드는 값이 변수로 구성되는 HTTP 헤더 필드입니다. [자세히 알아보기](../action/about-custom-action-configuration.md).

필요한 경우 다이내믹 헤더 필드의 값을 지정합니다.

1. 여정에서 사용자 지정 작업을 선택합니다.
1. 구성 창에서 페이지의 헤더 필드 옆에 있는 연필 아이콘을 클릭합니다 **[!UICONTROL URL Configuration]** 섹션을 참조하십시오.

   ![](assets/journey-dynamicheaderfield.png)

1. 필드를 선택하고 을(를) 클릭합니다 **[!UICONTROL OK]**.

## 작업 매개 변수

에서 **[!UICONTROL Action parameters]** 섹션에, _&quot;변수&quot;_. 이러한 매개 변수에 대해 이 정보를 가져올 위치를 정의할 수 있습니다(예: 이벤트, 데이터 소스)를 수동으로 전달하거나 고급 사용 사례를 위해 고급 표현식 편집기를 사용합니다. 고급 사용 사례는 데이터 조작 및 기타 기능 사용일 수 있습니다. 자세한 내용은 [Adobe Journey Orchestration 설명서](expression/expressionadvanced.md).

**관련 항목**

[작업 구성](../action/about-custom-action-configuration.md)
