---
solution: Journey Optimizer
product: journey optimizer
title: 라이브 보고서
description: 라이브 보고서에서 데이터를 사용하는 방법을 알아봅니다
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 8dd48bb2-a805-4c46-a16c-c68173a9ac08
source-git-commit: e7431d1b69e460471b01439c9bd2577fd69944ed
workflow-type: tm+mt
source-wordcount: '987'
ht-degree: 0%

---

# 라이브 보고서 시작 {#live-report}

를 사용하십시오 **[!UICONTROL Live report]** 내장된 대시보드에서 여정 및 메시지의 영향과 성능을 실시간으로 측정하고 시각화할 수 있습니다.
데이터는 **[!UICONTROL Live report]** 게재를 전송하거나 여정이 **[!UICONTROL Last 24hrs]** 탭.

* 여정의 컨텍스트에서 여정을 타깃팅하려면 **[!UICONTROL Journeys]** 메뉴에서 여정에 액세스하고 **[!UICONTROL View report]** 버튼을 클릭합니다.

   ![](assets/report_journey.png)

* 캠페인을 타깃팅하려면 **[!UICONTROL Campaigns]** 메뉴에서 캠페인에 액세스하고 **[!UICONTROL Reports]** 버튼을 클릭합니다.

   ![](assets/report_campaign.png)

* 에서 전환하려면 **[!UICONTROL Global report]** 변환 후 **[!UICONTROL Live report]** 게재의 경우 을(를) 클릭합니다. **[!UICONTROL Last 24hrs]** 탭 전환기에서 을 클릭합니다.

   ![](assets/report_3.png)

Adobe Journey Optimizer에서 사용할 수 있는 모든 지표의 세부 목록을 보려면 다음을 참조하십시오 [이 페이지](#list-of-components-live).

## 대시보드 사용자 지정 {#modify-dashboard}

위젯의 크기 조정 또는 제거를 통해 각 보고 대시보드를 수정할 수 있습니다. 위젯을 변경하면 현재 사용자의 대시보드에만 영향을 줍니다. 다른 사용자는 자신의 대시보드 또는 기본적으로 설정된 대시보드를 보게 됩니다.

1. 전환 표시줄을 사용하여 보고서에서 테스트 이벤트를 제외하려는 경우 선택합니다. 테스트 이벤트에 대한 자세한 내용은 [이 페이지](../building-journeys/testing-the-journey.md).

   다음 사항에 유의하십시오. **[!UICONTROL Exclude test events]** 옵션은 여정 보고서에만 사용할 수 있습니다.

   ![](assets/report_modify_6.png)

1. 위젯의 크기를 조정하거나 제거하려면 **[!UICONTROL Modify]**.

   ![](assets/report_modify_7.png)

1. 오른쪽 아래 모서리를 드래그하여 위젯 크기를 조정합니다.

   ![](assets/report_modify_8.png)

1. 클릭 **[!UICONTROL Remove]** 위젯을 제거하려면 필요하지 않습니다.

   ![](assets/report_modify_9.png)

1. 위젯의 표시 순서와 크기에 만족하면 을(를) 클릭합니다 **[!UICONTROL Save]**.

이제 대시보드가 저장됩니다. 나중에 라이브 보고서를 사용할 수 있도록 다른 변경 사항이 다시 적용됩니다. 필요한 경우 **[!UICONTROL Reset]** 기본 위젯 및 위젯의 순서를 복원하는 옵션입니다.

## 구성 요소 목록 {#list-of-components-live}

아래 표는 보고서에 사용된 지표 목록과 배달 유형에 따라 해당 정의를 제공합니다.

### 여정 지표 {#journey-metrics}

<table> 
 <thead> 
  <tr> 
   <th> 지표<br/> </th> 
   <th> 정의<br/> </th> 
</tr>
 </thead> 
 <tbody> 
  <tr> 
   <td>작업이 실행됨<br/> </td> 
   <td> 여정에 대해 성공적으로 실행된 총 작업 수입니다.<br/> </td> 
</tr> 
  <tr> 
   <td> 입력한 프로필<br/> </td> 
   <td> 여정의 시작 이벤트에 도달한 총 개인 수입니다.<br/> </td> 
</tr>
  <tr> 
   <td> 작업 오류<br/> </td> 
   <td>작업에 대해 발생한 총 오류 수입니다.<br/> </td> 
</tr> 
  <tr> 
   <td> 종료한 프로필<br/> </td> 
   <td> 여정을 종료한 총 개인 수입니다.<br/> </td> 
</tr> 
  <tr> 
   <td> 개별 여정 실패<br/> </td> 
   <td> 성공적으로 실행되지 않은 개별 여정의 총 수입니다.<br/> </td> 
</tr> 
 </tbody> 
</table>

### 이메일 및 SMS 지표 {#email-and-sms-metrics}

<table> 
 <thead> 
  <tr> 
   <th> 지표<br/> </th> 
   <th> 정의<br/> </th> 
</tr>
 </thead> 
 <tbody>
  <tr> 
   <td> 바운스 수<br/> </td> 
   <td> 게재 및 자동 반환 처리 중에 누적되는 총 오류 수입니다.<br/> </td> 
</tr> 
  <tr> 
   <td> 바운스 비율<br/> </td> 
   <td> 전송된 이메일과 비교하여 바운스된 이메일의 비율입니다.<br/> </td> 
</tr>
  <tr> 
   <td> 클릭 수<br/> </td> 
   <td> 이메일에서 콘텐츠를 클릭한 횟수입니다.<br/> </td> 
</tr> 
  <tr> 
   <td> 배달됨 <br/> </td> 
   <td> 성공적으로 보낸 메시지 수입니다.<br/></td> 
</tr> 
  <tr> 
   <td> 전송률<br/> </td> 
   <td> 성공적으로 보낸 메시지 비율입니다.<br/> </td> 
</tr>
  <tr> 
   <td> 오류<br/> </td> 
   <td> 게재 중에 발생한 총 오류로 인해 프로필이 전송되지 않았습니다.<br/> </td> 
</tr> 
  <tr> 
   <td> 오류율<br/> </td> 
   <td> 전송 중에 발생한 오류로 인해 전송된 이메일과 비교하여 전송되지 못했습니다.<br/> </td> 
</tr>
  <tr> 
   <td> 제외<br/> </td> 
   <td> Adobe Journey Optimizer에서 제외된 프로필 수입니다.<br/> </td> 
</tr>
  <tr> 
   <td> 하드 바운스<br/> </td> 
   <td> 잘못된 이메일 주소와 같은 총 영구 오류 수입니다. 여기에는 알 수 없는 사용자와 같이 주소가 유효하지 않다는 오류 메시지가 명시적으로 표시됩니다.<br/> </td>
</tr>
  <tr> 
   <td> 무시됨<br/> </td> 
   <td> 부재 중 또는 기술 오류(예: 발신자 유형이 postmaster인 경우)와 같은 총 임시 수입니다.<br/> </td> 
</tr>
   <tr> 
   <td>오퍼 클릭률<br/> </td> 
   <td>오퍼와 상호 작용한 사용자의 비율입니다.<br/> </td> 
</tr>
   <tr> 
   <td>오퍼 노출 횟수<br/> </td> 
   <td>열린 오퍼의 백분율로, 보낸 오퍼 수와 비교됩니다.<br/> </td> 
</tr>
   <tr> 
   <td>오퍼 이름<br/> </td> 
   <td> 게재에 추가된 오퍼의 이름입니다. 배치에 대한 자세한 내용은 다음을 참조하십시오 <a href="../offers/offer-library/creating-personalized-offers.md">페이지</a>.<br/> </td> 
</tr>
   <tr> 
   <td>오퍼가 전송됨<br/> </td> 
   <td>오퍼에 대한 총 전송 수입니다.<br/> </td> 
</tr> 
  <tr>
   <td>열기<br/> </td> 
   <td> 메시지를 연 횟수입니다.<br/> </td> 
</tr> 
  <tr> 
   <td> 오픈율<br/> </td> 
   <td> 연 총 이메일 수와 배달된 이메일 수 비교<br/> </td> 
</tr>
  <tr> 
   <td>배치 이름<br/> </td> 
   <td> 오퍼를 표시하는 데 사용되는 배치의 이름입니다. 배치에 대한 자세한 내용은 다음을 참조하십시오 <a href="../offers/offer-library/creating-placements.md">페이지</a>. </td> 
</tr> 
  <tr> 
   <td> 다시 시도<br/> </td> 
   <td> 다시 시도 큐에 있는 전자 메일 수입니다.<br/> </td> 
</tr> 
  <tr> 
   <td> 전송<br/> </td> 
   <td> 게재에 대한 총 전송 수입니다.<br/> </td> 
</tr>
  <tr> 
   <td> 소프트 바운스<br/> </td> 
   <td> 전체 받은 편지함과 같은 총 임시 오류 수입니다.<br/> </td> 
</tr>
  <tr> 
   <td> 스팸 불만<br/> </td> 
   <td> 메시지가 스팸 또는 정크 메일로 선언된 횟수입니다.<br/> </td> 
</tr>
  <tr> 
   <td> 타깃팅됨<br/> </td> 
   <td> 게재 분석 중에 처리된 총 메시지 수입니다.<br/> </td> 
</tr> 
  <tr> 
   <td> 고유 클릭 수<br/> </td> 
   <td> 전자 메일의 콘텐츠를 클릭한 수신자 수입니다.<br/> </td> 
</tr> 
  <tr> 
   <td>고유 클릭률<br/> </td> 
   <td> 게재와 상호 작용한 사용자의 비율입니다.<br/> </td> 
</tr>
  <tr> 
   <td> 고유 열기 수<br/> </td> 
   <td>게재를 연 수신자 수입니다.<br/> </td> 
</tr> 
  <tr> 
   <td> 구독 취소<br/> </td> 
   <td> 구독 취소 링크에 대한 클릭 수입니다.<br/> </td> 
</tr> 
 </tbody> 
</table>

### 랜딩 페이지 지표 {#landing-page-metrics}

<table> 
 <thead> 
  <tr> 
   <th> 지표<br/> </th> 
   <th> 정의<br/> </th> 
</tr>
 </thead> 
 <tbody>
 <tr> 
  <td>바운스 수<br/> </td> 
   <td>랜딩 페이지와 상호 작용하지 않고 구독 작업을 완료하지 않은 사람 수입니다.<br/> </td> 
</tr>
 <tr>
  <tr> 
   <td>클릭 수<br/> </td> 
   <td>랜딩 페이지에서 콘텐츠를 클릭한 횟수입니다.<br/> </td> 
</tr>
<tr>
<td>전환<br/> </td> 
   <td>랜딩 페이지와 상호 작용한 사용자(예: 양식 구독) 수입니다.<br/> </td> 
</tr>
 <tr> 
   <td>여정<br/> </td> 
   <td>여정에서 돌아오는 랜딩 페이지에 대한 방문 횟수.<br/> </td> 
</tr>
 <tr> 
   <td>기타 소스<br/> </td> 
   <td>여정 대신 외부 소스에서 온 랜딩 페이지에 대한 방문 수입니다.<br/> </td> 
</tr>
 <tr> 
   <td>총 방문 횟수<br/> </td> 
   <td> 하나의 수신자의 여러 방문 횟수를 포함하여 여정 및 외부 소스에서 랜딩 페이지에 대한 총 방문 수입니다.<br/> </td> 
</tr>
 <tr> 
   <td>고유 방문자 수<br/> </td> 
   <td>랜딩 페이지를 방문한 사람 수, 수신자의 여러 방문이 고려되지 않습니다.<br/> </td> 
</tr>
 <tr> 
   <td>방문 횟수<br/> </td> 
   <td>한 수신자의 여러 방문 횟수를 포함하여 랜딩 페이지에 대한 방문 횟수.<br/> </td> 
</tr>
 </tbody> 
</table>

### 푸시 알림 지표 {#push-notification-metrics}

<table> 
 <thead> 
  <tr> 
   <th> 지표<br/> </th> 
   <th> 정의<br/> </th> 
</tr>
 </thead> 
 <tbody>
 <tr> 
   <td>작업<br/> </td> 
   <td> 전달된 푸시 알림에 대한 총 작업 수(예: 단추 클릭 또는 취소)<br/> </td> 
</tr>
  <tr> 
   <td>바운스 수<br/> </td> 
   <td> 게재 및 자동 반환 처리 중에 누적되는 총 오류 수입니다.<br/> </td> 
</tr> 
  <tr> 
   <td> 배달됨<br/> </td> 
   <td> 성공적으로 보낸 메시지 수입니다.<br/> </td> 
</tr> 
  <tr> 
   <td>참여 횟수<br/> </td> 
   <td> 이 푸시 알림에 대한 총 열기 및 작업 수(즉, 프로필이 푸시를 열었는지 또는 단추를 클릭했는지 여부)입니다.<br/> </td> 
</tr> 
  <tr> 
   <td> 오류<br/> </td> 
   <td> 게재 중에 발생한 총 오류로 인해 프로필이 전송되지 않았습니다.<br/> </td> 
</tr>
  <tr> 
   <td> 제외<br/> </td> 
   <td> Adobe Journey Optimizer에서 제외된 프로필 수입니다.<br/> </td> 
</tr>
  <tr> 
   <td> 열기<br/> </td> 
   <td> 장치에 배달되고 사용자가 클릭했던 총 푸시 알림 수로 인해 앱이 열립니다. 알림이 무시되면 푸시 열기가 트리거되지 않는다는 점을 제외하고 푸시 클릭과 유사합니다.<br/> </td> 
</tr> 
  <tr> 
   <td> 전송<br/> </td> 
   <td> 게재에 대한 총 전송 수입니다.<br/> </td> 
</tr> 
  <tr> 
   <td> 타깃팅됨<br/> </td> 
   <td> 게재 분석 중에 처리된 총 푸시 메시지 수입니다.<br/> </td> 
</tr>  
 </tbody> 
</table>

<!--
### In-app metrics {#inapp-metrics}
<table> 
 <thead> 
  <tr> 
   <th> Metric<br/> </th> 
   <th> Definition<br/> </th> 
</tr>
 </thead> 
 <tbody>
 <tr> 
   <td>Clicks<br/> </td> 
   <td>Total number of recipients who interacted with the buttons included in the In-app message.<br/> </td> 
</tr>
  <tr> 
   <td>Impressions<br/> </td> 
   <td> Total number of In-app messages delivered to all users.<br/> </td>
</tr>
  <tr> 
   <td>Unique impressions<br/> </td> 
   <td>Number of unique users to whom the In-app message was delivered.<br/> </td>
</tr>
 </tbody> 
</table>
-->