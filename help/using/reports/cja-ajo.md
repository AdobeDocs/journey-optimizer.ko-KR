---
solution: Journey Optimizer
product: journey optimizer
title: Customer Journey Analytics 작업
description: Customer Journey Analytics 시작
feature: Reporting
topic: Content Management
role: User
level: Beginner
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 8%

---

# [!DNL Customer Journey Analytics]로 작업  {#cja-ajo}

![](assets/cja.png)
[!DNL Journey Optimizer] 통합 [!DNL Customer Journey Analytics] 는 데이터의 자동화된 보고서 분배 및 사용자 지정 시각화를 통해 모든 여정을 전체적으로 볼 수 있도록 합니다.

여정을 만든 후 [!DNL Journey Optimizer], 고객 데이터를에 가져올 수 있습니다. [!DNL Customer Journey Analytics] 보고서를 시작하고 고객이 여정과 상호 작용이 미치는 영향을 이해하기 위해 노력합니다.

➡️ [검색 Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-landing.html){target=&quot;_blank&quot;}

사용하기 전 [!DNL Customer Journey Analytics] 여정의 경우 먼저 이 통합을 구성해야 합니다.

1. [연결 만들기](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html?lang=ko-KR) in [!DNL Customer Journey Analytics] 사용 **[!UICONTROL 데이터 집합]** Platform으로 보내려고 합니다.

   다음 [!DNL Journey Optimizer] 구성할 수 있습니다.
   * [여정 단계 이벤트](../start/datasets-query-examples.md#journey-step-event): 여정에 들어오는 사람과 받는 거리를 볼 수 있습니다.
   * [메시지 피드백/추적 데이터 세트](../start/datasets-query-examples.md#message-feedback-event-dataset): 을(를) 통해 전송된 메시지에 대한 게재 정보를 볼 수 있도록 해줍니다 [!DNL Journey Optimizer].
   * [엔티티 및 여정 데이터 세트](../start/datasets-query-examples.md#entity-dataset): 친숙한 이름을 검색하고 보고에 사용할 수 있습니다.

1. [데이터 보기 만들기](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html) 를 입력하여 보고서에 사용할 차원 및 지표를 구성할 수 있습니다.

   Journey Optimizer 관련 지표를 만들어 여정 데이터를 더 잘 반영하도록 할 수 있습니다. [자세히 보기](https://experienceleague.adobe.com/docs/analytics-platform/using/integrations/ajo.html#configure-the-data-view-to-accommodate-journey-optimizer-dimensions-and-metrics)


사용 [!DNL Journey Optimizer] with [!DNL Customer Journey Analytics] 으로 인해 보고 데이터에 다음과 같은 불일치가 발생할 수 있습니다.

* **둘 다 [!DNL Journey Optimizer] 및 [!DNL Customer Journey Analytics] 보고를 위해 ADLS(Azure Data Lake Storage)의 데이터를 동기화합니다.**

   들어오는 데이터에 대한 처리 시간은 제품 간에 약간 다를 수 있습니다. 이로 인해 지정된 날짜에서 현재 날짜까지 보고서를 표시할 때 데이터가 일치하지 않을 수 있습니다. 불일치를 줄이려면 현재 날짜를 제외한 날짜 범위를 사용하십시오.

* **in [!DNL Journey Optimizer] 보고서, 보낸 지표에 다시 시도 지표도 포함됩니다.**

   **[!UICONTROL 다시 시도]** 에는 포함되지 않습니다. **[!UICONTROL 전송]** 의 지표 [!DNL Customer Journey Analytics]. 이 경우 [!DNL Customer Journey Analytics] **[!UICONTROL 전송]** 지표보다 낮은 값을 표시하는 지표 [!DNL Journey Optimizer]. 그러나 다시 시도 데이터는 **[!UICONTROL 메시지를 보냈습니다.]** 또는 **[!UICONTROL 바운스 수]** 지표.
불일치를 줄이려면 1주 전 또는 그 이상의 날짜 범위를 사용하십시오.

* **다른 데이터 소스에서 보고서가 제공됩니다.**

   이로 인해 제품 간 데이터 불일치가 1~2%로 발생할 수 있습니다.
