---
title: 이메일 글로벌 보고서
description: 이메일 글로벌 보고서에서 데이터를 사용하는 방법 학습
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 0%

---

# 전자 메일 글로벌 보고서 {#email-global-report}

![](../assets/do-not-localize/badge.png)

이메일 **[!UICONTROL Global report]**&#x200B;은 특정 이메일 배달만 타깃팅합니다.

**[!UICONTROL Messages]** 메뉴의 **[!UICONTROL Executions]** 탭에서 **[!UICONTROL Global view]**&#x200B;를 선택한 다음 선택한 배달의 고급 메뉴에서 **[!UICONTROL Global report]**&#x200B;을 선택합니다.

![](../assets/global_report_3.png)

이메일 **[!UICONTROL Global report]**&#x200B;은(는) 배달의 성공 및 오류를 설명하는 다른 위젯으로 나누어집니다. 필요한 경우 각 위젯의 크기를 조정하고 삭제할 수 있습니다. 이에 대한 자세한 내용은 이 [섹션](global-report.md#modify-dashboard)을 참조하십시오.

![](../assets/global_report_4.png)

**[!UICONTROL Email performance]** KPI를 사용하여 메시지와 관련된 주요 정보를 자세히 설명합니다.

* **[!UICONTROL Sent]**:배달에 대한 총 전송 수입니다.

* **[!UICONTROL Delivery Rate]**:성공적으로 전송한 메시지의 비율입니다.

* **[!UICONTROL Bounce Rate]**:보낸 이메일과 비교하여 바운스된 이메일의 비율입니다.

* **[!UICONTROL Error Rate]**:전송 중에 발생한 오류로 인해 보낸 이메일과 비교하여 전송되지 못했습니다.

* **[!UICONTROL Open Rate]**:연 메시지의 백분율입니다.

* **[!UICONTROL Click Rate]**:배달된 클릭 수의 비율입니다.

* **[!UICONTROL Spam Complaint Rate]**:배달된 메시지와 비교하여 수신자가 스팸으로 표시한 이메일의 비율입니다. 불만 사항에 대한 자세한 내용은 이 [페이지](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/metrics-for-deliverability/complaints.html#metrics-for-deliverability)를 참조하십시오.

* **[!UICONTROL Unsubscribe Rate]**:배달된 메시지와 비교하여 고유 구독 취소 횟수입니다.

**[!UICONTROL Sending Statistics]** 그래프는 배달에 대한 성공을 자세히 설명합니다.

* **[!UICONTROL Delivered]**:보낸 총 메시지 수와 관련하여 성공적으로 보낸 메시지 수입니다.

* **[!UICONTROL Bounces]**:총 보낸 메시지 수와 관련하여 배달 중 및 자동 반환 처리 중에 누적된 총 오류 수입니다.

* **[!UICONTROL Errors]**:배달 중에 발생한 총 오류 수 때문에 프로필로 전송되지 않습니다.

**[!UICONTROL Bounce Reasons]** 및 **[!UICONTROL Bounce categories]** 위젯에는 바운스된 메시지와 관련하여 사용할 수 있는 다음과 같은 데이터가 포함됩니다.

* **[!UICONTROL Hard bounce]**:잘못된 이메일 주소와 같은 총 영구 오류 수입니다. 이 작업에는 주소를 알 수 없는 사용자 등의 유효하지 않다고 명시적으로 표시하는 오류 메시지가 포함됩니다.

* **[!UICONTROL Soft bounce]**:전체 받은 편지함과 같은 총 임시 오류 수입니다.

* **[!UICONTROL Ignored]**:부재 중 또는 기술적 오류 등 총 임시 수입니다(예: 보낸 사람 유형이 postmaster인 경우).

바운스에 대한 자세한 내용은 [제외 목록 관리](../suppression-lists.md) 페이지를 참조하십시오.

![](../assets/global_report_5.png)

**[!UICONTROL Error Reasons]** 그래프 및 표를 사용하면 배달 중 발생한 오류를 확인할 수 있습니다.

수신자가 이메일을 여는 데 가장 많이 사용하는 도메인이 포함된 **[!UICONTROL Email - Best recipient domain]** 그래프 및 테이블 세부 사항.

![](../assets/global_report_6.png)

**[!UICONTROL Email - Tracking statistics]** 표에는 배달에 대한 수신자 활동에 사용할 수 있는 데이터가 포함되어 있습니다.

* **[!UICONTROL Opens]**:배달에서 배달을 연 횟수입니다.

* **[!UICONTROL Unique Opens]**:배달을 연 받는 사람 수입니다.

* **[!UICONTROL Open Rate]**:연 메시지의 백분율입니다.

* **[!UICONTROL Clicks]**:이메일에서 컨텐츠를 클릭한 횟수입니다.

* **[!UICONTROL Unique Clicks]**&#x200B;이메일 콘텐츠를 클릭한 수신자의 수.

* **[!UICONTROL Click through rate]**:배달된 클릭 수의 비율입니다.

**[!UICONTROL Open vs Click]**&#x200B;은 배달과 받는 사람의 상호 작용을 식별합니다.

* **[!UICONTROL Unique Clicks]**&#x200B;이메일 콘텐츠를 클릭한 수신자의 수.

* **[!UICONTROL Unique Opens]**:배달을 연 받는 사람 수입니다.

**[!UICONTROL Email - Top Url]** 그래프와 배달에서 가장 많이 방문한 URL에 대한 테이블 세부 사항입니다.
