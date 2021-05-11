---
solution: Journey Orchestration
title: 사용자 지정 작업 구성
description: 사용자 지정 작업을 구성하는 방법 알아보기
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 9%

---

# 작업 구성 {#configure-an-action}

![](../assets/do-not-localize/badge.png)

제3자 시스템을 사용하여 메시지를 보내거나 여정에서 API 호출을 제3자 시스템에 전송하도록 하려는 경우 여정에 대한 연결을 구성합니다. 그러면 기술 사용자가 정의한 사용자 지정 작업은 여정의 왼쪽 팔레트([이 페이지](../building-journeys/about-journey-activities.md#action-activities) 참조)에서 사용할 수 있습니다. **[!UICONTROL Action]** 다음은 사용자 정의 동작으로 연결할 수 있는 시스템의 몇 가지 예입니다.Epsilon, Facebook, Adobe.io, Firebase 등
제한 사항은 [이 페이지](../building-journeys/limitations.md)에 나열됩니다.

사용자 지정 작업을 구성하는 데 필요한 기본 단계는 다음과 같습니다.

1. **[!UICONTROL Actions]** 목록에서 **[!UICONTROL Add]**&#x200B;을 클릭하여 새 작업을 만듭니다. 화면 오른쪽에 작업 구성 창이 열립니다.

   ![](../assets/custom2.png)

1. 작업 이름을 입력합니다.

   >[!NOTE]
   >
   >공백이나 특수 문자는 사용하지 말고 이름은 30자까지만 입력하십시오.

1. 액션에 설명을 추가합니다. 데이터 소스에 이벤트에 설명을 추가합니다.
1. 이 작업을 사용하는 여정 수는 **[!UICONTROL Used in]** 필드에 표시됩니다. **[!UICONTROL View journeys]** 단추를 클릭하여 이 작업을 사용하는 여정 목록을 표시할 수 있습니다.
1. 다른 **[!UICONTROL URL Configuration]** 매개 변수를 정의합니다. [이 페이지](../action/about-custom-action-configuration.md#url-configuration)를 참조하십시오.
1. **[!UICONTROL Authentication]** 섹션을 구성합니다. 이 구성은 데이터 소스의 구성과 동일합니다.  [이 섹션](../datasource/external-data-sources.md#section_wjp_nl5_nhb)을 참조하십시오.
1. **[!UICONTROL Message parameters]**&#x200B;을(를) 정의합니다. [이 페이지](../action/about-custom-action-configuration.md#define-the-message-parameters)를 참조하십시오.
1. **[!UICONTROL Save]**&#x200B;을 클릭합니다.

   이제 사용자 지정 작업이 구성되어 여정에서 사용할 준비가 되었습니다. [이 페이지](../building-journeys/about-journey-activities.md#action-activities)를 참조하십시오.

   >[!NOTE]
   >
   >사용자 정의 액션을 여정에서 사용하면 대부분의 매개 변수가 읽기 전용입니다. **[!UICONTROL Name]**, **[!UICONTROL Description]**, **[!UICONTROL URL]** 필드 및 **[!UICONTROL Authentication]** 섹션만 수정할 수 있습니다.

## URL 구성 {#url-configuration}

사용자 지정 작업을 구성할 때 다음 **[!UICONTROL URL Configuration]** 매개 변수를 정의해야 합니다.

![](../assets/journeyurlconfiguration.png)

1. 외부 서비스의 **[!UICONTROL URL]**&#x200B;을(를) 추가합니다.

   >[!NOTE]
   >
   >보안상 HTTPS를 사용하는 것이 좋습니다. 공개되지 않은 Adobe 주소 및 IP 주소 사용을 허용하지 않습니다.

1. **[!UICONTROL Method]** 호출을 선택합니다.**[!UICONTROL POST]** 또는 **[!UICONTROL PUT]**&#x200B;일 수 있습니다.
1. **[!UICONTROL Headers]** 섹션에서 **[!UICONTROL Add a header field]**&#x200B;을 클릭하여 새 키/값 쌍을 정의합니다. 외부 서비스에 대한 요청의 HTTP 헤더에 해당합니다. 키/값 쌍을 삭제하려면 **[!UICONTROL Headers]** 필드에 커서를 놓고 **[!UICONTROL Delete]** 아이콘을 클릭합니다.

   **[!UICONTROL Content-Type]** 및 **[!UICONTROL Charset]** 는 기본적으로 설정되며 삭제 또는 재정의할 수 없습니다.

   >[!NOTE]
   >
   >헤더는 다음 [구문 분석 규칙](https://tools.ietf.org/html/rfc7230#section-3.2.4)에 따라 유효성이 확인됩니다.

## 메시지 매개 변수 {#define-the-message-parameters} 정의

![](../assets/messageparameterssection.png)

**[!UICONTROL Message parameters]** 섹션에서 외부 서비스로 전송할 JSON 페이로드의 예를 붙여 넣습니다.

![](../assets/customactionpayloadmessage.png)

매개 변수 유형(예:문자열, 정수 등).

매개 변수가 상수 또는 변수인지를 지정하는 방법 중에서 선택할 수도 있습니다.

* 상수는 매개 변수의 값이 작업 구성 창에서 기술적 모습을 통해 정의됨을 의미합니다. 값은 여정 간에 항상 동일합니다. 여정에서 사용자 지정 동작을 사용하는 경우 해당 동작이 달라질 수 있으므로 마케터는 이를 확인할 수 없습니다. 이것은 제3자 시스템이 기대하는 ID와 같은 것일 수 있습니다. 이 경우 전환 상수/변수 오른쪽에 있는 필드는 전달된 값입니다.
* 변수는 매개 변수의 값이 달라짐을 의미합니다. 여정에서 이 사용자 정의 액션을 사용하는 마케터는 원하는 값을 전달하거나 이 매개 변수의 값을 가져올 위치(예: 이벤트에서, Adobe Experience Platform 등에서)를 지정할 수 있습니다. 이 경우 전환 상수/변수 오른쪽에 있는 필드는 마케터가 이 매개 변수의 이름을 지정하기 위해 여정에 표시할 레이블입니다.

![](../assets/customactionpayloadmessage2.png)
