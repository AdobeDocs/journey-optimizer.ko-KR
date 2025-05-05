---
solution: Journey Optimizer
product: journey optimizer
title: Customer Journey Analytics 작업
description: Customer Journey Analytics 시작
feature: Reporting, Integrations
topic: Content Management
role: User
level: Beginner
exl-id: 5349b0cf-da4e-458c-89be-c75a38e4721a
source-git-commit: 47482adb84e05fe41eb1c50479a8b50e00469ec4
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 6%

---

# 수동으로 [!DNL Customer Journey Analytics] 구성 {#cja-ajo}

[!DNL Journey Optimizer]과(와) [!DNL Customer Journey Analytics]의 통합은 자동화된 보고서 배포와 데이터의 사용자 지정 시각화를 통해 모든 여정을 전체적으로 볼 수 있도록 합니다.

다음 섹션에서는 Customer Journey Analytics 내에서 심층적인 분석을 위해 Journey Optimizer에서 생성한 데이터를 수동으로 활용하는 방법에 대해 설명합니다. 이 통합은 자동으로 설정할 수 있습니다. [자세히 알아보기](report-gs-cja.md)

![](assets/cja.png)

[!DNL Journey Optimizer]에서 여정을 만든 후 고객 데이터를 [!DNL Customer Journey Analytics] (으)로 가져와서 보고를 시작하고 고객이 여정과 갖는 모든 상호 작용의 영향을 이해할 수 있습니다.

➡️0&rbrace;검색 Customer Journey Analytics[&#128279;](https://experienceleague.adobe.com/ko/docs/analytics-platform/using/integrations/ajo#manually-configure-a-data-view-to-be-used-with-journey-optimizer){target="_blank"}

>[!NOTE]
>
>이 통합 외에도 Adobe Journey Optimizer 데이터 세트의 콘텐츠를 클라우드 스토리지 위치로 내보내고 이 정보를 보고 또는 분석 목적으로 사용할 수도 있습니다. [클라우드 저장소 위치로 데이터 세트를 내보내는 방법에 대해 알아봅니다](../data/export-datasets.md)
>
>데이터 세트 내보내기 기능은 현재 베타 버전이며 모든 Adobe Journey Optimizer 사용자가 사용할 수 있습니다. 아직 액세스 권한이 없는 경우 Adobe 담당자에게 대상 액세스 권한 부여를 요청하십시오.

여정에 [!DNL Customer Journey Analytics]을(를) 사용하기 전에 먼저 이 통합을 구성해야 합니다.

1. Adobe Experience Platform으로 보낼 **[!UICONTROL 데이터 세트]**&#x200B;를 사용하여 [연결을 만듭니다](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html?lang=ko).[!DNL Customer Journey Analytics]

   다음 [!DNL Journey Optimizer]을(를) 구성할 수 있습니다.
   * [여정 단계 이벤트](../data/datasets-query-examples.md#journey-step-event): 여정에 입장한 사람과 입장한 거리를 볼 수 있습니다.
   * [메시지 피드백/추적 데이터 세트](../data/datasets-query-examples.md#message-feedback-event-dataset): [!DNL Journey Optimizer]을(를) 통해 보낸 메시지에 대한 게재 정보를 볼 수 있습니다.
   * [엔터티 및 여정 데이터 세트](../data/datasets-query-examples.md#entity-dataset): 알기 쉬운 이름을 검색하고 보고에 사용할 수 있습니다.

1. 보고서에 사용할 차원 및 지표를 구성하려면 [데이터 보기를 만듭니다](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html?lang=ko).

   Journey Optimizer 관련 지표를 만들어 여정 데이터를 더 잘 반영할 수 있습니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/analytics-platform/using/integrations/ajo.html?lang=ko#configure-the-data-view-to-accommodate-journey-optimizer-dimensions-and-metrics)

[!DNL Journey Optimizer]을(를) [!DNL Customer Journey Analytics]과(와) 함께 사용하면 다음 원인으로 인해 데이터 보고에 불일치가 발생할 수 있습니다.

* **보고를 위해 Azure ADLS(데이터 레이크 저장소)에서 [!DNL Journey Optimizer] 및 [!DNL Customer Journey Analytics] 동기화 데이터를 모두 사용합니다.**

  수신 데이터 처리 시간은 제품마다 약간 다를 수 있습니다. 이로 인해 주어진 날짜부터 현재 날짜까지의 보고서를 표시할 때 데이터가 일치하지 않을 수 있습니다. 불일치를 줄이려면 현재 날짜를 제외한 날짜 범위를 사용하십시오.

* **[!DNL Journey Optimizer] 보고서에서 보낸 메트릭에 다시 시도 메트릭도 포함됩니다.**

  **[!UICONTROL 다시 시도]**&#x200B;은(는) [!DNL Customer Journey Analytics]의 **[!UICONTROL 전송됨]** 지표에 포함되지 않습니다. 이로 인해 [!DNL Customer Journey Analytics] **[!UICONTROL 전송됨]** 지표가 [!DNL Journey Optimizer]보다 낮은 값을 표시합니다. 그러나 다시 시도 데이터는 **[!UICONTROL 정상적으로 전송된 메시지]** 또는 **[!UICONTROL 바운스]** 지표에 포함됩니다.
불일치를 줄이려면 일주일 전 또는 그 이후의 날짜 범위를 사용하십시오.

* **다른 데이터 원본에서 보고서가 제공됩니다.**

  이로 인해 제품 간에 1~2%의 데이터 불일치가 발생할 수 있습니다.
