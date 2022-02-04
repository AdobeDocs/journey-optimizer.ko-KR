---
title: 이메일 글로벌 보고서
description: 이메일 글로벌 보고서에서 데이터를 사용하는 방법을 알아봅니다
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 2bead395-082a-4fea-ad10-b2b2c5f484e9
source-git-commit: 7a07f2348f08b4582a1310fb65d431c55451d9b6
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 1%

---

# 이메일 글로벌 보고서 {#email-global-report}

이메일 **[!UICONTROL Global report]** 특정 이메일 게재만 타겟팅합니다.

에서 **[!UICONTROL Executions]** 의 탭 **[!UICONTROL Messages]** 메뉴, 선택 **[!UICONTROL Global view]** 그런 다음 선택한 게재의 고급 메뉴에서 을(를) 선택합니다 **[!UICONTROL Global report]**.

![](../assets/global_report_3.png)

이메일 **[!UICONTROL Global report]** 은 게재의 성공 및 오류를 설명하는 다른 위젯으로 구분됩니다. 필요한 경우 각 위젯의 크기를 조정하고 삭제할 수 있습니다. 자세한 정보는 다음을 참조하십시오 [섹션](global-report.md#modify-dashboard).

![](../assets/global_report_4.png)

**[!UICONTROL Email performance]** kpi를 사용하여 메시지에 대한 기본 정보를 자세히 설명합니다.

* **[!UICONTROL Sent]**: 게재에 대한 총 전송 수입니다.

* **[!UICONTROL Delivery Rate]**: 성공적으로 보낸 메시지 비율입니다.

* **[!UICONTROL Bounce Rate]**: 전송된 이메일과 비교하여 바운스된 이메일의 비율입니다.

* **[!UICONTROL Error Rate]**: 전송 중에 발생한 오류로 인해 전송된 이메일과 비교하여 전송되지 못했습니다.

* **[!UICONTROL Open Rate]**: 열린 메시지의 백분율입니다.

* **[!UICONTROL Click Rate]**: 게재 클릭 비율.

* **[!UICONTROL Spam Complaint Rate]**: 배달된 메시지와 비교하여 수신자가 스팸으로 표시한 이메일의 백분율입니다. 불만 사항에 대한 자세한 내용은 [게재 가능성 모범 사례 안내서](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/metrics-for-deliverability/complaints.html#metrics-for-deliverability){target=&quot;_blank&quot;}.

* **[!UICONTROL Unsubscribe Rate]**: 게재한 메시지 수와 비교하여 고유한 구독 취소 비율입니다. 이 지표는 구독 취소 링크 클릭 수에 의존하지 않지만 수신자가 시작한 구독 취소 수를 기반으로 합니다. 구독 취소에 대해 자세히 알아보십시오 [페이지](../messages/consent.md).

다음 **[!UICONTROL Email - Tracking statistics]** 게재에 대해 수신자 활동에 사용할 수 있는 데이터를 포함합니다.

* **[!UICONTROL Opens]**: 게재에서 게재를 연 횟수입니다.

* **[!UICONTROL Unique Opens]**: 연 게재의 백분율입니다.

* **[!UICONTROL Open Rate]**: 연 총 이메일 수와 배달된 이메일 수 비교

* **[!UICONTROL Clicks]**: 이메일에서 콘텐츠를 클릭한 횟수입니다.

* **[!UICONTROL Unique Clicks]**: 이메일의 콘텐츠를 클릭한 수신자 수입니다.

* **[!UICONTROL Click through rate]**: 여정과 상호 작용한 사용자의 비율입니다.

다음 **[!UICONTROL Sending Statistics]** 그래프는 게재 성공에 대해 자세히 설명합니다.

* **[!UICONTROL Delivered]**: 보낸 총 메시지 수와 관련하여 성공적으로 보낸 메시지 수입니다.

* **[!UICONTROL Bounces]**: 총 보낸 메시지 수와 관련하여 게재 및 자동 반환 처리 중에 누적된 총 오류 수입니다.

* **[!UICONTROL Errors]**: 게재 중에 발생한 총 오류로 인해 프로필이 전송되지 않았습니다.

![](../assets/global_report_5.png)

다음 **[!UICONTROL Bounce Reasons]** 및 **[!UICONTROL Bounce categories]** 위젯에는 다음과 같이 바운스된 메시지와 관련하여 사용할 수 있는 데이터가 포함되어 있습니다.

* **[!UICONTROL Hard bounce]**: 잘못된 이메일 주소와 같은 총 영구 오류 수입니다. 여기에는 알 수 없는 사용자와 같이 주소가 유효하지 않다는 오류 메시지가 명시적으로 표시됩니다.

* **[!UICONTROL Soft bounce]**: 전체 받은 편지함과 같은 총 임시 오류 수입니다.

* **[!UICONTROL Ignored]**: 부재 등의 총 임시 수 또는 기술 오류(예: 발신자 유형이 postmaster인 경우)입니다.

바운스에 대한 자세한 내용은 [제외 목록](../messages/suppression-list.md) 페이지.

다음 **[!UICONTROL Error Reasons]** 그래프 및 표를 사용하면 게재 중에 발생한 오류를 확인할 수 있습니다.

![](../assets/global_report_6.png)

다음 **[!UICONTROL Email - Top recipient domain]** 전자 메일을 여는 데 받는 사람이 가장 많이 사용하는 도메인을 그래프 및 표 세부 사항입니다.

다음 **[!UICONTROL Email - Top Url]** 가장 많이 방문한 게재 URL을 그래프 및 표 세부 사항으로 설명합니다.

다음 **[!UICONTROL Open vs Click]** 게재와 수신자의 상호 작용을 식별합니다.

* **[!UICONTROL Unique Clicks]**: 이메일의 콘텐츠를 클릭한 수신자 수입니다.

* **[!UICONTROL Unique Opens]**: 게재를 연 수신자 수입니다.

<!--
![](../assets/global_report_20.png)

>[!NOTE]
>
>The Offers widgets and metrics are only available if a decision was inserted in an email. For more information on Decision Management, refer to this [page](../offers/get-started/starting-offer-decisioning.md).

The **[!UICONTROL Offers statistic]** and **[!UICONTROL Offers statistics]** over time widgets measure your offer's success and impact on your targeted audience. It detail the main information relative to your message with KPIs:

* **[!UICONTROL Offer sent]**: Total number of sends for the offer.

* **[!UICONTROL Offer impression]**: Number of times the offer was opened in a delivery.

* **[!UICONTROL Offer clicks]**: Number of times an offer was clicked on in a delivery.

The **[!UICONTROL Offers detailed statistic]** table contains the available data for recipient activity with your offer:

* **[!UICONTROL Placement name]**: Name of your placement used to display your offer. For more information on placement, refer to this [page](../offers/offer-library/creating-placements.md).

* **[!UICONTROL Offer name]**: Name of the offer added in the delivery. For more information on placement, refer to this [page](../offers/offer-library/creating-personalized-offers.md).

* **[!UICONTROL Offer sent]**: Total number of sends for the offer.

* **[!UICONTROL Offer impression rate]**: Percentage of opened offers compared to the number of sent offers.

* **[!UICONTROL Offer click rate]**: Percentage of users who interacted with the offer.
-->
>[!NOTE]
>
>다음 포함 **[!UICONTROL Suppressed]** 또는 **[!UICONTROL Not allowed]** 상태는 메시지 전송 프로세스 중에 제외됩니다. 따라서 **여정 보고서** 은(는) 이러한 프로필을 여정을 통해 이동했음을 나타냅니다([세그먼트 읽기](../building-journeys/read-segment.md) 및 [메시지](../building-journeys/journeys-message.md) 활동), **이메일 보고서** 에는 이러한 매개 변수가 포함되지 않습니다. **[!UICONTROL Sent]** 지표는 이메일 전송 전에 필터링됩니다.
>
>추가 정보 [제외 목록](../messages/suppression-list.md) 및 [허용 목록](../messages/allow-list.md). 모든 제외 사례에 대한 이유를 알아보려면 [Adobe Experience Platform 쿼리 서비스](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;}.
