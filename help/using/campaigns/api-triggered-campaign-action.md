---
solution: Journey Optimizer
product: journey optimizer
title: API에서 트리거된 캠페인 작업 구성
description: API에서 트리거된 캠페인 작업을 구성하는 방법을 알아봅니다.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: 캠페인, API 트리거, REST, 최적화 도구, 메시지
exl-id: 322e035c-7370-40c9-b1cb-3428bc26e874
source-git-commit: ed00ef1f9aad7a9baf16b806e1cbffae677b2a91
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 55%

---

# API에서 트리거된 캠페인 작업 구성 {#api-action}

**[!UICONTROL 액션]** 탭을 사용하여 메시지의 채널 구성을 선택하고 추적, 콘텐츠 실험 또는 다국어 콘텐츠와 같은 추가 설정을 구성합니다.

1. **채널 선택**.

   **[!UICONTROL 작업]** 탭으로 이동하여 **[!UICONTROL 작업 추가]** 단추를 클릭하고 통신 채널을 선택합니다.

   ![](assets/api-triggered-channel.png)

   >[!NOTE]
   >
   >지원 채널: [이메일](../email/get-started-email.md), [SMS/MMS/RCS](../sms/get-started-sms.md), [푸시 알림](../push/get-started-push.md).
   >
   >사용 가능한 채널은 사용하는 라이선스 모델 및 추가 기능에 따라 다릅니다.

1. **채널 구성 선택**

   구성은 [시스템 관리자](../start/path/administrator.md)가 정의합니다. 여기에는 헤더 매개변수, 하위 도메인, 모바일 앱 등 메시지 전송을 위한 모든 기술적 매개변수가 포함되어 있습니다. [채널 구성을 설정하는 방법 알아보기](../configuration/channel-surfaces.md)

   ![](assets/create-campaign-action.png)

1. **최적화 활용**

   **[!UICONTROL 메시지 최적화]** 섹션을 사용하여 콘텐츠 실험을 실행하거나, 타깃팅 규칙을 활용하거나, 실험과 타깃팅을 모두 사용하는 고급 조합을 사용할 수 있습니다. 이러한 다양한 옵션과 따라야 할 단계는 이 섹션에 자세히 설명되어 있습니다. [캠페인의 최적화](campaigns-message-optimization.md).
<!--
1. **Create a content experiment**

    Use the **[!UICONTROL Content experiment]** section to define multiple delivery treatments in order to measure which one performs best for your target audience. Click the **[!UICONTROL Create experiment]** button then follow the steps detailed in this section: [Create a content experiment](../content-management/content-experiment.md).-->

1. **다국어 콘텐츠 추가**

   **[!UICONTROL 언어]** 섹션을 사용하여 캠페인 내에서 여러 언어로 콘텐츠를 만듭니다. 이렇게 하려면 **[!UICONTROL 언어 추가]** 버튼을 클릭하고 원하는 **[!UICONTROL 언어 설정]**&#x200B;을 선택합니다. 다국어 기능 설정 및 사용 방법에 대한 자세한 정보는 [다국어 콘텐츠 시작](../content-management/multilingual-gs.md) 섹션에서 확인할 수 있습니다.

선택한 통신 채널에 따라 추가 설정을 사용할 수 있습니다. 자세한 내용을 보려면 아래 섹션을 확장하십시오.

+++**최대 가용량 규칙 적용**(전자 메일, 푸시, SMS)

**[!UICONTROL 비즈니스 규칙]** 드롭다운 목록에서 최대 가용량 규칙을 캠페인에 적용할 규칙 집합을 선택하십시오. 채널 규칙 세트를 활용하면 통신 유형별로 빈도 상한을 설정하여 유사한 메시지가 있는 고객을 오버로드할 수 있습니다. [규칙 세트 작업 방법 알아보기](../conflict-prioritization/rule-sets.md)

+++

+++**참여 추적**(전자 메일, SMS).

**[!UICONTROL 액션 추적]** 섹션을 사용하여 수신자가 이메일 또는 SMS 게재에 어떻게 반응하는지 추적할 수 있습니다. 캠페인이 실행되면 캠페인 보고서에서 추적 결과에 액세스할 수 있습니다. [캠페인 보고서에 대해 자세히 알아보기](../reports/campaign-global-report-cja.md)

+++

+++**빠른 전송 모드를 사용**(푸시)합니다.

빠른 전송 모드는 캠페인을 통해 대량으로 매우 빠르게 푸시 메시지를 전송할 수 있는 [!DNL Journey Optimizer] 추가 기능입니다. 빠른 게재는 메시지 게재 지연이 비즈니스에 중요한 경우, 휴대폰에 긴급 푸시 알림을 전송하려는 경우(예: 뉴스 채널 앱을 설치한 사용자에게 속보 전달) 사용됩니다. 푸시 알림에 대해 빠른 전송 모드를 사용하는 방법을 알아봅니다. [&#x200B; 이 페이지](../push/create-push.md#rapid-delivery).

빠른 전송 모드를 사용할 때의 성능에 대한 자세한 내용은 [Adobe Journey Optimizer 제품 설명](https://helpx.adobe.com/kr/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}을 참조하십시오.

+++

## 다음 단계 {#next}

캠페인 구성 및 콘텐츠가 준비되면 콘텐츠를 디자인할 수 있습니다. [자세히 알아보기](api-triggered-campaign-content.md)
