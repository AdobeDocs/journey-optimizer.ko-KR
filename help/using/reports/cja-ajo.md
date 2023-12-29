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
source-git-commit: c2f2dde40385f56ea86be15a5857fa9e5e2e2fed
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 7%

---

# 로 작업 [!DNL Customer Journey Analytics] {#cja-ajo}


[!DNL Journey Optimizer] 과 통합 [!DNL Customer Journey Analytics] 에서는 자동화된 보고서 배포 및 데이터에 대한 사용자 지정 시각화를 통해 모든 여정을 전체적으로 볼 수 있습니다.

![](assets/cja.png)

에서 여정 생성 후 [!DNL Journey Optimizer], 고객 데이터를 가져올 수 있습니다. [!DNL Customer Journey Analytics] 보고서를 시작하고 고객과 여정 간의 모든 상호 작용이 미치는 영향을 파악합니다.

➡️ [Customer Journey Analytics 검색](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-landing.html){target="_blank"}

>[!NOTE]
>
>이 통합 외에도 Adobe Journey Optimizer 데이터 세트의 콘텐츠를 클라우드 스토리지 위치로 내보내고 이 정보를 보고 또는 분석 목적으로 사용할 수도 있습니다. [데이터 세트를 클라우드 스토리지 위치로 내보내는 방법 알아보기](../data/export-datasets.md)
>
>데이터 세트 내보내기 기능은 현재 베타 버전이며 모든 Adobe Journey Optimizer 사용자가 사용할 수 있습니다. 아직 액세스 권한이 없는 경우 Adobe 담당자에게 대상 액세스 권한 부여를 요청하십시오.

사용 전 [!DNL Customer Journey Analytics] 여정의 경우 먼저 이 통합을 구성해야 합니다.

1. [연결 만들기](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html) 위치: [!DNL Customer Journey Analytics] (으)로 **[!UICONTROL 데이터 세트]** Adobe Experience Platform으로 보내려고 합니다.

   다음 [!DNL Journey Optimizer] 다음을 구성할 수 있습니다.
   * [여정 단계 이벤트](../data/datasets-query-examples.md#journey-step-event): 여정에 누가 들어가며 얼마나 멀리 도달하는지 볼 수 있습니다.
   * [메시지 피드백/추적 데이터 세트](../data/datasets-query-examples.md#message-feedback-event-dataset): 를 통해 전송된 메시지에 대한 게재 정보를 볼 수 있습니다 [!DNL Journey Optimizer].
   * [엔티티 및 여정 데이터 세트](../data/datasets-query-examples.md#entity-dataset): 알기 쉬운 이름을 검색하고 보고에 사용할 수 있습니다.

1. [데이터 보기 만들기](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html) 보고서에 사용할 차원 및 지표를 구성하려면 다음 작업을 수행하십시오.

   Journey Optimizer 관련 지표를 만들어 여정 데이터를 더 잘 반영할 수 있습니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/analytics-platform/using/integrations/ajo.html#configure-the-data-view-to-accommodate-journey-optimizer-dimensions-and-metrics)

사용 [!DNL Journey Optimizer] 포함 [!DNL Customer Journey Analytics] 이로 인해 다음과 같은 원인으로 데이터 보고에 불일치가 발생할 수 있습니다.

* **모두 [!DNL Journey Optimizer] 및 [!DNL Customer Journey Analytics] 보고를 위해 ADLS(Azure Data Lake Storage)의 데이터를 동기화합니다.**

  수신 데이터 처리 시간은 제품마다 약간 다를 수 있습니다. 이로 인해 주어진 날짜부터 현재 날짜까지의 보고서를 표시할 때 데이터가 일치하지 않을 수 있습니다. 불일치를 줄이려면 현재 날짜를 제외한 날짜 범위를 사용하십시오.

* **위치 [!DNL Journey Optimizer] 보고서, 전송된 지표에는 다시 시도 지표도 포함됩니다.**

  **[!UICONTROL 다시 시도]** 이(가)에 포함되지 않음 **[!UICONTROL 전송됨]** 지표 [!DNL Customer Journey Analytics]. 이로 인해 다음이 발생합니다. [!DNL Customer Journey Analytics] **[!UICONTROL 전송됨]** 낮은 값을 표시하는 지표 [!DNL Journey Optimizer]. 하지만 재시도 데이터는 **[!UICONTROL 정상적으로 전송된 메시지]** 또는 **[!UICONTROL 바운스]** 지표.
불일치를 줄이려면 일주일 전 또는 그 이후의 날짜 범위를 사용하십시오.

* **보고서가 다른 데이터 소스에서 제공되고 있습니다.**

  이로 인해 제품 간에 1~2%의 데이터 불일치가 발생할 수 있습니다.
