---
solution: Journey Orchestration
title: 사용자 지정 작업 구성
description: 사용자 지정 작업을 구성하는 방법 알아보기
feature: Actions
topic: Administration
role: Admin
level: Intermediate
exl-id: 4df2fc7c-85cb-410a-a31f-1bc1ece237bb
source-git-commit: a101ee8cd7b57ee951d0ef2d5fd366757cb0a014
workflow-type: tm+mt
source-wordcount: '863'
ht-degree: 6%

---

# 사용자 지정 작업 구성 {#configure-an-action}

서드파티 시스템을 사용하여 메시지를 보내거나 여정이 서드파티 시스템에 API 호출을 전송하도록 하려면 사용자 지정 작업을 사용하여 여정에 대한 연결을 구성하십시오. 예를 들어 사용자 지정 작업으로 다음 시스템에 연결할 수 있습니다. Epsilon, Slack, Adobe.io, Firebase 등

사용자 지정 작업은 기술 사용자가 정의하며 마케터가 사용할 수 있는 추가 작업입니다. 구성되면 여정 왼쪽 팔레트의 **[!UICONTROL Action]** 카테고리. [이 페이지](../building-journeys/about-journey-activities.md#action-activities)에서 자세히 알아보십시오.

## 제한 사항{#custom-actions-limitations}

사용자 지정 작업은 다음과 같은 몇 가지 제한 사항이 있습니다. [이 페이지](../start/limitations.md).

사용자 지정 작업 매개 변수에서는 간단한 컬렉션과 객체 컬렉션을 전달할 수 있습니다. 의 컬렉션 제한 사항에 대해 자세히 알아보십시오 [이 페이지](../building-journeys/collections.md#limitations).

사용자 지정 작업 매개 변수에는 예상 형식(예: 문자열, 십진수 등.) 이러한 예상 형식을 준수하도록 주의해야 합니다. 자세한 내용 [사용 사례](../building-journeys/collections.md).


## 구성 단계 {#configuration-steps}

사용자 지정 작업을 구성하는 데 필요한 주요 단계는 다음과 같습니다.

1. 관리 메뉴 섹션에서 **[!UICONTROL Configurations]**. 에서  **[!UICONTROL Actions]** 섹션을 클릭합니다. **[!UICONTROL Manage]**. 클릭 **[!UICONTROL Create Action]** 새 작업을 만들려면 화면 오른쪽에 작업 구성 창이 열립니다.

   ![](../assets/custom2.png)

1. 작업의 이름을 입력합니다.

   >[!NOTE]
   >
   >공백이나 특수 문자는 사용하지 말고 이름은 30자까지만 입력하십시오.

1. 작업에 설명을 추가합니다. 데이터 소스에 이벤트에 설명을 추가합니다.
1. 이 작업을 사용하는 여정 수는 **[!UICONTROL Used in]** 필드. 을(를) 클릭합니다. **[!UICONTROL View journeys]** 버튼을 클릭하여 이 작업을 사용하는 여정 목록을 표시합니다.
1. 다양한 정의 **[!UICONTROL URL Configuration]** 매개 변수. [이 페이지](../action/about-custom-action-configuration.md#url-configuration)를 참조하십시오.
1. 구성 **[!UICONTROL Authentication]** 섹션을 참조하십시오. 이 구성은 데이터 소스와 동일합니다.  [이 섹션](../datasource/external-data-sources.md#custom-authentication-mode)을 참조하십시오.
1. 을(를) 정의합니다 **[!UICONTROL Action parameters]**. [이 페이지](../action/about-custom-action-configuration.md#define-the-message-parameters)를 참조하십시오.
1. **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

   이제 사용자 지정 작업이 구성되었으며 여정에서 사용할 준비가 되었습니다. [이 페이지](../building-journeys/about-journey-activities.md#action-activities)를 참조하십시오.

   >[!NOTE]
   >
   >여정에서 사용자 지정 작업을 사용하면 대부분의 매개 변수가 읽기 전용입니다. 는 **[!UICONTROL Name]**, **[!UICONTROL Description]**, **[!UICONTROL URL]** 필드 및 **[!UICONTROL Authentication]** 섹션을 참조하십시오.

## URL 구성 {#url-configuration}

사용자 지정 작업을 구성할 때 다음을 정의해야 합니다 **[!UICONTROL URL Configuration]** 매개 변수:

![](../assets/journeyurlconfiguration.png)

1. 에서 **[!UICONTROL URL]** 필드에서 외부 서비스의 URL을 지정합니다.

   * URL이 정적인 경우 이 필드에 URL을 입력합니다.

   * URL에 동적 경로가 포함된 경우 URL의 정적 부분, 즉 구성표, 호스트, 포트 및 선택적으로 경로의 정적 부분만 입력합니다.

      예: `https://xxx.yyy.com/somethingstatic/`

      사용자 지정 작업을 여정에 추가할 때 URL의 동적 경로를 지정합니다. [자세히 알아보기](../building-journeys/using-custom-actions.md).
   >[!NOTE]
   >
   >보안상의 이유로 URL에 HTTPS 체계를 사용하는 것이 좋습니다. 공개되지 않은 Adobe 주소 및 IP 주소 사용을 허용하지 않습니다.
   >
   >사용자 지정 작업을 정의할 때는 기본 포트만 허용됩니다. http의 경우 80, https의 경우 443.

1. 호출을 선택합니다 **[!UICONTROL Method]**: 다음 중 하나일 수 있습니다 **[!UICONTROL POST]** 또는 **[!UICONTROL PUT]**.
1. 에서 **[!UICONTROL Headers]** 섹션에서 외부 서비스로 전송할 요청 메시지의 HTTP 헤더를 정의합니다.
   1. 헤더 필드를 추가하려면 **[!UICONTROL Add a header field]**.
   1. 헤더 필드의 키를 입력합니다.
   1. 키-값 쌍에 대한 동적 값을 설정하려면 다음을 선택합니다 **[!UICONTROL Variable]**. 그렇지 않으면 을 선택합니다. **[!UICONTROL Constant]**.

      예를 들어 타임스탬프의 경우 동적 값을 설정할 수 있습니다.

   1. 선택한 경우 **[!UICONTROL Constant]**&#x200B;를 입력한 다음 상수 값을 입력합니다.

      선택한 경우 **[!UICONTROL Variable]**&#x200B;를 채울 경우 사용자 지정 작업을 여정에 추가할 때 이 변수를 지정합니다. [자세히 알아보기](../building-journeys/using-custom-actions.md).

      ![](../assets/journeyurlconfiguration2.png)

   1. 헤더 필드를 삭제하려면 헤더 필드를 가리킨 다음 **[!UICONTROL Delete]** 아이콘.
   다음 **[!UICONTROL Content-Type]** 및 **[!UICONTROL Charset]** 헤더 필드는 기본적으로 설정되어 있습니다. 이러한 필드는 수정하거나 삭제할 수 없습니다.

   여정에 사용자 지정 작업을 추가한 후에도 여정이 초안 상태인 경우 헤더 필드를 추가할 수 있습니다. 여정이 구성 변경 사항의 영향을 받지 않도록 하려면 사용자 지정 작업을 복제하고 헤더 필드를 새 사용자 지정 작업에 추가합니다.

   >[!NOTE]
   >
   >헤더는 필드 구문 분석 규칙에 따라 유효성이 검사됩니다. [자세히 알아보기](https://tools.ietf.org/html/rfc7230#section-3.2.4).

## 작업 매개 변수 정의 {#define-the-message-parameters}

![](../assets/messageparameterssection.png)

에서 **[!UICONTROL Action parameters]** 섹션을 통해 외부 서비스로 전송할 JSON 페이로드의 예를 붙여넣습니다.

![](../assets/customactionpayloadmessage.png)

>[!NOTE]
>
>페이로드의 필드 이름에는 &quot;.&quot;를 사용할 수 없습니다. 문자. &quot;$&quot; 문자로 시작할 수 없습니다.

매개 변수 유형(예: 문자열, 정수 등)

매개 변수가 상수 또는 변수인지를 지정할 수도 있습니다.

* 상수는 매개 변수의 값이 기술 성향에 의해 작업 구성 창에 정의되어 있음을 의미합니다. 값은 여정 간에 항상 동일합니다. 여정에서 사용자 지정 작업을 사용할 때에는 변경사항이 발생하지 않으며 마케터가 표시되지 않습니다. 예를 들어 서드파티 시스템에서 기대하는 ID일 수 있습니다. 이 경우 전환 상수/변수 오른쪽에 있는 필드가 전달된 값입니다.
* 변수는 매개 변수의 값이 변경됨을 의미합니다. 여정에서 이 사용자 지정 작업을 사용하는 마케터는 원하는 값을 전달하거나 이 매개 변수의 값을 검색할 위치(예: 이벤트에서 또는 Adobe Experience Platform에서)를 지정할 수 있습니다. 이 경우 전환 상수/변수 오른쪽에 있는 필드는 이 매개 변수의 이름을 지정하기 위해 여정에 표시되는 레이블 마케터입니다.

![](../assets/customactionpayloadmessage2.png)

