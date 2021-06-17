---
title: 이메일 글로벌 보고서
description: 이메일 글로벌 보고서에서 데이터를 사용하는 방법을 알아봅니다
feature: 보고
topic: 콘텐츠 관리
role: User
level: Intermediate
source-git-commit: 42e5cdec54339f65cddd79df4deabbf28292d16b
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 1%

---

# 전자 메일 글로벌 보고서 {#email-global-report}

이메일 **[!UICONTROL Global report]**&#x200B;은(는) 특정 이메일 게재만 타겟팅합니다.

**[!UICONTROL Messages]** 메뉴의 **[!UICONTROL Executions]** 탭에서 **[!UICONTROL Global view]**&#x200B;를 선택한 다음 선택한 게재의 고급 메뉴에서 **[!UICONTROL Global report]**&#x200B;을 선택합니다.

![](../assets/global_report_3.png)

이메일 **[!UICONTROL Global report]**&#x200B;은(는) 게재의 성공 및 오류를 설명하는 다른 위젯으로 나누어집니다. 필요한 경우 각 위젯의 크기를 조정하고 삭제할 수 있습니다. 이에 대한 자세한 정보는 이 [섹션](global-report.md#modify-dashboard)을 참조하십시오.

![](../assets/global_report_4.png)

**[!UICONTROL Email performance]** kpi를 사용하여 메시지에 대한 기본 정보를 자세히 설명합니다.

* **[!UICONTROL Sent]**:게재에 대한 총 전송 수입니다.

* **[!UICONTROL Delivery Rate]**:성공적으로 보낸 메시지 비율입니다.

* **[!UICONTROL Bounce Rate]**:전송된 이메일과 비교하여 바운스된 이메일의 비율입니다.

* **[!UICONTROL Error Rate]**:전송 중에 발생한 오류로 인해 전송된 이메일과 비교하여 전송되지 못했습니다.

* **[!UICONTROL Open Rate]**:열린 메시지의 백분율입니다.

* **[!UICONTROL Click Rate]**:게재 클릭 비율.

* **[!UICONTROL Spam Complaint Rate]**:배달된 메시지와 비교하여 수신자가 스팸으로 표시한 이메일의 백분율입니다. 불만 사항에 대한 자세한 내용은 이 [페이지](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/metrics-for-deliverability/complaints.html#metrics-for-deliverability)를 참조하십시오.

* **[!UICONTROL Unsubscribe Rate]**:게재한 메시지 수와 비교하여 고유한 구독 취소 비율입니다. 이 지표는 구독 취소 링크 클릭 수에 의존하지 않지만 수신자가 시작한 구독 취소 수를 기반으로 합니다. 이 [페이지](../consent.md)에서 구독 취소에 대해 자세히 알아보십시오.

**[!UICONTROL Email - Tracking statistics]**&#x200B;에는 게재에 사용할 수 있는 수신자 활동이 포함되어 있습니다.

* **[!UICONTROL Opens]**:게재에서 게재를 연 횟수입니다.

* **[!UICONTROL Unique Opens]**:연 게재의 백분율입니다.

* **[!UICONTROL Open Rate]**:연 총 이메일 수와 배달된 이메일 수 비교

* **[!UICONTROL Clicks]**:이메일에서 콘텐츠를 클릭한 횟수입니다.

* **[!UICONTROL Unique Clicks]**: 이메일의 콘텐츠를 클릭한 수신자 수입니다.

* **[!UICONTROL Click through rate]**:여정과 상호 작용한 사용자의 비율입니다.

**[!UICONTROL Sending Statistics]** 그래프는 게재의 성공에 대해 자세히 설명합니다.

* **[!UICONTROL Delivered]**:보낸 총 메시지 수와 관련하여 성공적으로 보낸 메시지 수입니다.

* **[!UICONTROL Bounces]**:총 보낸 메시지 수와 관련하여 게재 및 자동 반환 처리 중에 누적된 총 오류 수입니다.

* **[!UICONTROL Errors]**:게재 중에 발생한 총 오류로 인해 프로필이 전송되지 않았습니다.

![](../assets/global_report_5.png)

**[!UICONTROL Bounce Reasons]** 및 **[!UICONTROL Bounce categories]** 위젯에는 다음과 같이 바운스된 메시지와 관련하여 사용할 수 있는 데이터가 포함됩니다.

* **[!UICONTROL Hard bounce]**:잘못된 이메일 주소와 같은 총 영구 오류 수입니다. 여기에는 알 수 없는 사용자와 같이 주소가 유효하지 않다는 오류 메시지가 명시적으로 표시됩니다.

* **[!UICONTROL Soft bounce]**:전체 받은 편지함과 같은 총 임시 오류 수입니다.

* **[!UICONTROL Ignored]**:부재 등의 총 임시 수 또는 기술 오류(예: 발신자 유형이 postmaster인 경우)입니다.

바운스에 대한 자세한 내용은 [억제 목록](../suppression-list.md) 페이지를 참조하십시오.

**[!UICONTROL Error Reasons]** 그래프 및 표를 사용하면 게재 중에 발생한 오류를 확인할 수 있습니다.

![](../assets/global_report_6.png)

**[!UICONTROL Email - Top recipient domain]** 그래프 및 표는 수신자가 이메일을 여는 데 가장 많이 사용하는 도메인을 자세히 설명합니다.

**[!UICONTROL Email - Top Url]** 그래프 및 표는 게재에서 가장 많이 방문한 URL을 자세히 설명합니다.

**[!UICONTROL Open vs Click]**&#x200B;은(는) 수신자와 게재의 상호 작용을 식별합니다.

* **[!UICONTROL Unique Clicks]**: 이메일의 콘텐츠를 클릭한 수신자 수입니다.

* **[!UICONTROL Unique Opens]**:게재를 연 수신자 수입니다.


