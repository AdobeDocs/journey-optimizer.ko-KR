---
solution: Journey Orchestration
title: 사용자 지정 작업 구성 정보
description: 사용자 지정 작업을 구성하는 방법 알아보기
feature: Actions
topic: Administration
role: Admin
level: Intermediate
exl-id: 4df2fc7c-85cb-410a-a31f-1bc1ece237bb
source-git-commit: 967772bcf7413c4c916d045375a84807581ea6ae
workflow-type: tm+mt
source-wordcount: '777'
ht-degree: 6%

---

# 작업 구성 {#configure-an-action}

서드파티 시스템을 사용하여 메시지를 보내거나 여정이 서드파티 시스템에 API 호출을 전송하도록 하려는 경우 여기에서 여정에 대한 연결을 구성합니다. 기술 사용자가 정의한 사용자 정의 작업은 여정 왼쪽 팔레트의 **[!UICONTROL Action]** 범주에서 사용할 수 있습니다( [이 페이지](../building-journeys/about-journey-activities.md#action-activities) 참조). 다음은 사용자 지정 작업에 연결할 수 있는 시스템의 몇 가지 예입니다. Epsilon, Facebook, Adobe.io, Firebase 등
제한 사항은 [이 페이지](../limitations.md)에 나열되어 있습니다.

사용자 지정 작업을 구성하는 데 필요한 주요 단계는 다음과 같습니다.

1. 관리 메뉴 섹션에서 **[!UICONTROL Configurations]** 을 선택합니다. **[!UICONTROL Actions]** 섹션에서 **[!UICONTROL Manage]** 를 클릭합니다. **[!UICONTROL Create Action]** 을 클릭하여 새 작업을 만듭니다. 화면 오른쪽에 작업 구성 창이 열립니다.

   ![](../assets/custom2.png)

1. 작업의 이름을 입력합니다.

   >[!NOTE]
   >
   >공백이나 특수 문자는 사용하지 말고 이름은 30자까지만 입력하십시오.

1. 작업에 설명을 추가합니다. 데이터 소스에 이벤트에 설명을 추가합니다.
1. 이 작업을 사용하는 여정 수가 **[!UICONTROL Used in]** 필드에 표시됩니다. **[!UICONTROL View journeys]** 단추를 클릭하여 이 작업을 사용하는 여정 목록을 표시할 수 있습니다.
1. 다른 **[!UICONTROL URL Configuration]** 매개 변수를 정의합니다. [이 페이지](../action/about-custom-action-configuration.md#url-configuration)를 참조하십시오.
1. **[!UICONTROL Authentication]** 섹션을 구성합니다. 이 구성은 데이터 소스와 동일합니다.  [이 섹션](../datasource/external-data-sources.md#section_wjp_nl5_nhb)을 참조하십시오.
1. **[!UICONTROL Action parameters]**&#x200B;을(를) 정의합니다. [이 페이지](../action/about-custom-action-configuration.md#define-the-message-parameters)를 참조하십시오.
1. **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

   이제 사용자 지정 작업이 구성되었으며 여정에서 사용할 준비가 되었습니다. [이 페이지](../building-journeys/about-journey-activities.md#action-activities)를 참조하십시오.

   >[!NOTE]
   >
   >여정에서 사용자 지정 작업을 사용하면 대부분의 매개 변수가 읽기 전용입니다. **[!UICONTROL Name]**, **[!UICONTROL Description]**, **[!UICONTROL URL]** 필드 및 **[!UICONTROL Authentication]** 섹션만 수정할 수 있습니다.

## URL 구성 {#url-configuration}

사용자 지정 작업을 구성할 때 다음 **[!UICONTROL URL Configuration]** 매개 변수를 정의해야 합니다.

![](../assets/journeyurlconfiguration.png)

1. **[!UICONTROL URL]** 필드에서 외부 서비스의 URL을 지정합니다.

   * URL이 정적인 경우 이 필드에 URL을 입력합니다.

   * URL에 동적 경로가 포함된 경우 URL의 정적 부분, 즉 구성표, 호스트, 포트 및 선택적으로 경로의 정적 부분만 입력합니다.

      예: `https://xxx.yyy.com:8080/somethingstatic/`

      사용자 지정 작업을 여정에 추가할 때 URL의 동적 경로를 지정합니다. [자세히 알아보기](../building-journeys/using-custom-actions.md).
   >[!NOTE]
   >
   >보안상의 이유로 URL에 HTTPS 체계를 사용하는 것이 좋습니다. 공개되지 않은 Adobe 주소 및 IP 주소 사용을 허용하지 않습니다.

1. 호출 **[!UICONTROL Method]**&#x200B;을 선택합니다. **[!UICONTROL POST]** 또는 **[!UICONTROL PUT]**&#x200B;일 수 있습니다.
1. **[!UICONTROL Headers]** 섹션에서 외부 서비스로 전송할 요청 메시지의 HTTP 헤더를 정의합니다.
   1. 헤더 필드를 추가하려면 **[!UICONTROL Add a header field]** 을 클릭합니다.
   1. 헤더 필드의 키를 입력합니다.
   1. 키-값 쌍에 대한 동적 값을 설정하려면 **[!UICONTROL Variable]** 을 선택합니다. 그렇지 않으면 **[!UICONTROL Constant]** 을 선택합니다.

      예를 들어 타임스탬프의 경우 동적 값을 설정할 수 있습니다.

   1. **[!UICONTROL Constant]** 을 선택한 경우 상수 값을 입력합니다.

      **[!UICONTROL Variable]** 을 선택한 경우 여정에 사용자 지정 작업을 추가할 때 이 변수를 지정합니다. [자세히 알아보기](../building-journeys/using-custom-actions.md).

      ![](../assets/journeyurlconfiguration2.png)

   1. 헤더 필드를 삭제하려면 헤더 필드를 가리킨 다음 **[!UICONTROL Delete]** 아이콘을 클릭합니다.
   **[!UICONTROL Content-Type]** 및 **[!UICONTROL Charset]** 헤더 필드는 기본적으로 설정되어 있습니다. 이러한 필드는 수정하거나 삭제할 수 없습니다.

   여정에 사용자 지정 작업을 추가한 후에도 여정이 초안 상태인 경우 헤더 필드를 추가할 수 있습니다. 여정이 구성 변경 사항의 영향을 받지 않도록 하려면 사용자 지정 작업을 복제하고 헤더 필드를 새 사용자 지정 작업에 추가합니다.

   >[!NOTE]
   >
   >헤더는 필드 구문 분석 규칙에 따라 유효성이 검사됩니다. [자세히 알아보기](https://tools.ietf.org/html/rfc7230#section-3.2.4).

## 작업 매개 변수 정의 {#define-the-message-parameters}

![](../assets/messageparameterssection.png)

**[!UICONTROL Action parameters]** 섹션에서 외부 서비스로 전송할 JSON 페이로드의 예제를 붙여넣습니다.

![](../assets/customactionpayloadmessage.png)

>[!NOTE]
>
>페이로드의 필드 이름에는 &quot;.&quot;를 사용할 수 없습니다. 문자. &quot;$&quot; 문자로 시작할 수 없습니다.

매개 변수 유형(예: 문자열, 정수 등)

매개 변수가 상수 또는 변수인지를 지정할 수도 있습니다.

* 상수는 매개 변수의 값이 기술 성향에 의해 작업 구성 창에 정의되어 있음을 의미합니다. 값은 여정 간에 항상 동일합니다. 여정에서 사용자 지정 작업을 사용할 때에는 변경사항이 발생하지 않으며 마케터가 표시되지 않습니다. 예를 들어 서드파티 시스템에서 기대하는 ID일 수 있습니다. 이 경우 전환 상수/변수 오른쪽에 있는 필드가 전달된 값입니다.
* 변수는 매개 변수의 값이 변경됨을 의미합니다. 여정에서 이 사용자 지정 작업을 사용하는 마케터는 원하는 값을 전달하거나 이 매개 변수의 값을 검색할 위치(예: 이벤트에서 또는 Adobe Experience Platform에서)를 지정할 수 있습니다. 이 경우 전환 상수/변수 오른쪽의 필드는 여정에서 이 매개 변수의 이름을 지정하는 레이블입니다.

![](../assets/customactionpayloadmessage2.png)
