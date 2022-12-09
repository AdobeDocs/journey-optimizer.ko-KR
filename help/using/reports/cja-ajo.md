---
solution: Journey Optimizer
product: journey optimizer
title: Customer Journey Analytics 작업
description: Customer Journey Analytics 시작하기
feature: Reporting
topic: Content Management
role: User
level: Beginner
exl-id: 5349b0cf-da4e-458c-89be-c75a38e4721a
source-git-commit: 928ad6822efbe95c0ddf5456531d92be8b4bed75
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 0%

---

# 작업 [!DNL Customer Journey Analytics] {#cja-ajo}


[!DNL Journey Optimizer] 통합 [!DNL Customer Journey Analytics] 는 자동화된 보고서 분배 및 데이터에 대한 사용자 지정 시각화를 사용하여 모든 여정의 전체적인 보기를 제공합니다.

![](assets/cja.png)

에서 여정을 만든 후 [!DNL Journey Optimizer], 고객 데이터를에 가져올 수 있습니다. [!DNL Customer Journey Analytics] 를 클릭하여 보고서를 시작하고 고객이 여정에 미치는 모든 상호 작용의 영향을 파악할 수 있습니다.

➡️ [Customer Journey Analytics 살펴보기](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-landing.html){target=&quot;_blank&quot;}

사용하기 전 [!DNL Customer Journey Analytics] 여정의 경우 먼저 이 통합을 구성해야 합니다.

1. [연결 만들기](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html) in [!DNL Customer Journey Analytics] 사용 **[!UICONTROL Dataset]** adobe Experience Platform으로 보내려는 경우

   다음 [!DNL Journey Optimizer] 구성할 수 있습니다.
   * [여정 단계 이벤트](../data/datasets-query-examples.md#journey-step-event): 여정에 들어가는 사람과 거리를 볼 수 있습니다.
   * [메시지 피드백/추적 데이터 세트](../data/datasets-query-examples.md#message-feedback-event-dataset): 을(를) 통해 전송된 메시지에 대한 게재 정보를 볼 수 있도록 해줍니다 [!DNL Journey Optimizer].
   * [엔티티 및 여정 데이터 세트](../data/datasets-query-examples.md#entity-dataset): 친숙한 이름을 검색하고 보고에 사용할 수 있습니다.

1. [데이터 보기 만들기](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html) 를 입력하여 보고서에 사용할 차원 및 지표를 구성할 수 있습니다.

   Journey Optimizer 관련 지표를 만들어 여정 데이터를 더 잘 반영하도록 할 수 있습니다. [추가 정보](https://experienceleague.adobe.com/docs/analytics-platform/using/integrations/ajo.html#configure-the-data-view-to-accommodate-journey-optimizer-dimensions-and-metrics)


사용 [!DNL Journey Optimizer] with [!DNL Customer Journey Analytics] 으로 인해 보고 데이터에 다음과 같은 불일치가 발생할 수 있습니다.

* **둘 다 [!DNL Journey Optimizer] 및 [!DNL Customer Journey Analytics] 보고를 위해 ADLS(Azure Data Lake Storage)의 데이터를 동기화합니다.**

   들어오는 데이터에 대한 처리 시간은 제품 간에 약간 다를 수 있습니다. 이로 인해 지정된 날짜에서 현재 날짜까지 보고서를 표시할 때 데이터가 일치하지 않을 수 있습니다. 불일치를 줄이려면 현재 날짜를 제외한 날짜 범위를 사용하십시오.

* **in [!DNL Journey Optimizer] 보고서, 보낸 지표에 다시 시도 지표도 포함됩니다.**

   **[!UICONTROL Retries]** 에는 포함되지 않습니다. **[!UICONTROL Sent]** 의 지표 [!DNL Customer Journey Analytics]. 이 경우 [!DNL Customer Journey Analytics] **[!UICONTROL Sent]** 지표보다 낮은 값을 표시하는 지표 [!DNL Journey Optimizer]. 그러나 다시 시도 데이터는 **[!UICONTROL Messages successfully sent]** 또는 **[!UICONTROL Bounces]** 지표.
불일치를 줄이려면 1주 전 또는 그 이상의 날짜 범위를 사용하십시오.

* **다른 데이터 소스에서 보고서가 제공됩니다.**

   이로 인해 제품 간 데이터 불일치가 1~2%로 발생할 수 있습니다.
