---
solution: Journey Optimizer
product: journey optimizer
title: 글로벌 보고서
description: 글로벌 보고서에서 데이터를 사용하는 방법을 알아봅니다
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: ec15e700-7659-4dbf-8446-6534ea48c5c8
source-git-commit: e7431d1b69e460471b01439c9bd2577fd69944ed
workflow-type: tm+mt
source-wordcount: '1441'
ht-degree: 4%

---

# 글로벌 보고서 시작 {#global-report}

>[!NOTE]
>
> Query Service를 사용할 때 API를 통해 사용자 지정 쿼리가 수행되는 경우 보고서가 약간 지연될 수 있습니다.

를 사용하십시오 **[!UICONTROL 글로벌 보고서]** 을 입력하여 선택한 기간 동안의 여정 및 게재의 영향을 측정합니다.

* 여정 컨텍스트에서 여정 또는 게재를 타깃팅하려면 **[!UICONTROL 여정]** 메뉴에서 여정에 액세스하여 **[!UICONTROL 보고서 보기]** 버튼을 클릭합니다. 그런 다음 여정, 이메일, SMS 및 푸시 글로벌 보고서를 찾을 수 있습니다.

   ![](assets/report_journey.png)

* 캠페인을 타깃팅하려면 **[!UICONTROL 캠페인]** 메뉴에서 캠페인에 액세스하고 **[!UICONTROL 보고서]** 버튼을 클릭합니다.

   ![](assets/report_campaign.png)

* 에서 전환하려면 **[!UICONTROL 라이브 보고서]** 변환 후 **[!UICONTROL 글로벌 보고서]** 게재의 경우 을(를) 클릭합니다. **[!UICONTROL 항상]** 탭 전환기에서 을 클릭합니다.

   ![](assets/report_5.png)

Adobe Journey Optimizer에서 사용할 수 있는 모든 지표에 대한 자세한 목록은 다음을 참조하십시오 [이 페이지](#list-of-components-global)

## 대시보드 사용자 지정 {#modify-dashboard}

기간 변경 및 위젯 크기 조정 또는 제거를 통해 각 보고 대시보드를 수정할 수 있습니다. 위젯을 변경하면 현재 사용자의 대시보드에만 영향을 줍니다. 다른 사용자는 자신의 대시보드 또는 기본적으로 설정된 대시보드를 보게 됩니다.

1. 글로벌 보고서에서 특정 데이터를 타깃팅할 시작 및 종료 시간을 선택합니다.

   ![](assets/report_modify_1.png)

1. 전환 표시줄을 사용하여 보고서에서 테스트 이벤트를 제외하려는 경우 선택합니다. 테스트 이벤트에 대한 자세한 내용은 [이 페이지](../building-journeys/testing-the-journey.md).

   다음 사항에 유의하십시오. **[!UICONTROL 테스트 이벤트 제외]** 옵션은 여정 보고서에만 사용할 수 있습니다.

   ![](assets/report_modify_2.png)

1. 클릭 **[!UICONTROL 수정]** 대시보드 사용자 지정을 시작하려면 다음을 수행하십시오.

   ![](assets/report_modify_3.png)

1. 오른쪽 아래 모서리를 드래그하여 위젯 크기를 조정합니다.

   ![](assets/report_modify_4.png)

1. 클릭 **[!UICONTROL 제거]** 위젯을 제거하려면 필요하지 않습니다.

   ![](assets/report_modify_5.png)

1. 위젯의 표시 순서와 크기에 만족하면 을(를) 클릭합니다 **[!UICONTROL 저장]**.

이제 대시보드가 저장됩니다. 나중에 라이브 보고서를 사용할 수 있도록 다른 변경 사항이 다시 적용됩니다. 필요한 경우 **[!UICONTROL 재설정]** 기본 위젯 및 위젯의 순서를 복원하는 옵션입니다.

## 구성 요소 목록 {#list-of-components-global}

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
   <td> 실패한 개별 여정<br/> </td> 
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
   <td> 바운스<br/> </td> 
   <td> 총 보낸 메시지 수와 관련하여 게재 및 자동 반환 처리 중에 누적된 총 오류 수입니다.<br/> </td> 
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
   <td> 게재됨 <br/> </td> 
   <td> 보낸 총 메시지 수와 관련하여 성공적으로 보낸 메시지 수입니다.<br/></td> 
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
   <td>열림<br/> </td> 
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
   <td> 보냄<br/> </td> 
   <td> 게재에 대한 총 전송 수입니다.<br/> </td> 
</tr>
  <tr> 
   <td> 소프트 바운스<br/> </td> 
   <td> 전체 받은 편지함과 같은 총 임시 오류 수입니다.<br/> </td> 
</tr>
  <tr> 
   <td> 스팸 불만 사항<br/> </td> 
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

<!--
### Experimentation metrics {#experimentation-metrics}
<table> 
 <thead> 
  <tr> 
   <th> Metric<br/> </th> 
   <th> Definition<br/> </th> 
</tr>
 </thead> 
 <tbody>
  <tr> 
   <td>App installs<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>App launches<br/> </td> 
   <td><br/> </td> 
</tr>
 <tr> 
   <td>Average lift<br/> </td> 
   <td> Percentage improvement in conversion rate of a given treatment over the baseline.<a href="../campaigns/experiment-calculations.md#understand-lift">Learn more</a>.<br/> </td> 
  </tr>
  <tr> 
   <td>Confidence<br/> </td> 
   <td>Evidence that a given treatment is the same as the baseline treatment. <a href="../campaigns/experiment-calculations.md#understand-confidence">Learn more</a>.<br/> </td> 
</tr>
  <tr> 
   <td>Confidence interval<br/> </td> 
   <td>Percentage difference in performance between the baseline and the best performing treatment. <a href="../campaigns/experiment-calculations.md#understand-intervals">Learn more</a>.<br/> </td> 
</tr> 
  <tr> 
   <td>Count per profile<br/> </td> 
   <td>Total value of the Experiment objective metric divided by the number of profiles.<br/> </td> 
</tr>
  <tr> 
   <td>Email Opens<br/> </td> 
   <td>.<br/> </td> 
</tr>
  <tr> 
   <td>Email Unsubscribes<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>First app launches<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>Outbound Clicks<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>Profiles<br/> </td> 
   <td>Number of profiles targeted for this treatment.<br/> </td> 
</tr>
  <tr> 
   <td>Unique email opens<br/> </td> 
   <td><br/> </td>
<tr>
  <tr> 
   <td>Unique email unsubscribes<br/> </td> 
   <td><br/> </td>
</tr>
  <tr> 
   <td>Unique installs<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>Unique launches<br/> </td> 
   <td><br/> </td> 
</tr> 
  <tr> 
   <td>Unique outbound clicks<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>Unique upgrades<br/> </td> 
   <td><br/> </td> 
</tr>
   <td>Upgrades<br/> </td> 
   <td><br/> </td> 
</tr> 
</tbody> 
</table>
-->

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
   <td>바운스<br/> </td> 
   <td> 총 보낸 메시지 수와 관련하여 게재 및 자동 반환 처리 중에 누적된 총 오류 수입니다.<br/> </td> 
</tr> 
  <tr> 
   <td> 바운스 비율<br/> </td> 
   <td> 전송된 푸시 알림과 비교하여 바운스된 푸시 알림의 비율입니다.<br/> </td>
</tr>
  <tr> 
   <td> 게재됨<br/> </td> 
   <td> 보낸 총 메시지 수와 관련하여 성공적으로 보낸 메시지 수입니다.<br/> </td> 
</tr> 
  <tr> 
   <td> 전송률<br/> </td> 
   <td> 성공적으로 전송된 푸시 알림의 비율입니다.<br/> </td> 
</tr>
  <tr> 
   <td>참여 횟수<br/> </td> 
   <td> 이 푸시 알림에 대한 총 열기 및 작업 수(즉, 프로필이 푸시를 열었는지 또는 단추를 클릭했는지 여부)입니다.<br/> </td> 
</tr> 
  <tr> 
   <td> 참여 비율<br/> </td> 
   <td> 이 푸시 알림에 대한 열기 및 작업의 비율(즉, 프로필이 푸시를 열었는지 또는 단추를 클릭했는지 여부)입니다.<br/> </td> 
</tr>
  <tr> 
   <td> 오류<br/> </td> 
   <td> 게재 중에 발생한 총 오류로 인해 프로필이 전송되지 않았습니다.<br/> </td> 
</tr>
  <tr> 
   <td> 오류율<br/> </td> 
   <td> 전송 중에 발생한 오류로 인해 전송된 푸시 알림과 비교하여 전송되지 못했습니다.<br/> </td> 
</tr> 
  <tr> 
   <td> 제외<br/> </td> 
   <td> Adobe Journey Optimizer에서 제외된 프로필 수입니다.<br/> </td> 
</tr>
  <tr> 
   <td> 열림<br/> </td> 
   <td> 장치에 배달되고 사용자가 클릭했던 총 푸시 알림 수로 인해 앱이 열립니다. 알림이 무시되면 푸시 열기가 트리거되지 않는다는 점을 제외하고 푸시 클릭과 유사합니다.<br/> </td> 
</tr> 
  <tr> 
   <td> 오픈율<br/> </td> 
   <td> 열린 푸시 알림의 비율입니다.<br/> </td> 
</tr> 
  <tr> 
   <td> 보냄<br/> </td> 
   <td> 게재에 대한 총 전송 수입니다.<br/> </td> 
</tr> 
  <tr> 
   <td> 타깃팅됨<br/> </td> 
   <td> 게재 분석 중에 처리된 총 푸시 메시지 수입니다.<br/> </td> 
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
  <td>바운스<br/> </td> 
   <td>랜딩 페이지와 상호 작용하지 않고 구독 작업을 완료하지 않은 사람 수입니다.<br/> </td> 
</tr>
 <tr> 
   <td>바운스 비율<br/> </td> 
   <td>총 방문 수와 관련하여 랜딩 페이지와 상호 작용하지 않고 구독 작업을 완료하지 않은 사람 수입니다.<br/> </td> 
</tr>
 <tr>
  <tr> 
   <td>클릭 수<br/> </td> 
   <td>랜딩 페이지에서 콘텐츠를 클릭한 횟수입니다.<br/> </td> 
</tr>
 <tr> 
   <td>클릭률<br/> </td> 
   <td>랜딩 페이지에서 클릭하는 비율입니다.<br/> </td>
</tr>
<tr>
<td>전환<br/> </td> 
   <td>랜딩 페이지와 상호 작용한 사용자(예: 양식 구독) 수입니다.<br/> </td> 
</tr>
<tr>
   <td>전환율<br/> </td> 
   <td>총 방문 수와 관련하여 양식을 구독하는 등 랜딩 페이지와 상호 작용한 사람의 수입니다.<br/> </td> 
</tr>
 <tr> 
   <td>여정<br/> </td> 
   <td>여정에서 랜딩 페이지에 대한 방문 수입니다.<br/> </td> 
</tr>
 <tr> 
   <td>기타 소스<br/> </td> 
   <td>랜딩 페이지에 대한 여정 대신 외부 소스에서 온 방문 수입니다.<br/> </td> 
</tr>
 <tr> 
   <td>총 방문 횟수<br/> </td> 
   <td> 한 수신자의 여러 방문을 포함하여 여정 및 외부 소스에서 랜딩 페이지에 대한 총 방문 수입니다.<br/> </td> 
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
   <td>바운스<br/> </td> 
   <td> 총 보낸 메시지 수와 관련하여 게재 및 자동 반환 처리 중에 누적된 총 오류 수입니다.<br/> </td> 
</tr> 
  <tr> 
   <td> 바운스 비율<br/> </td> 
   <td> 전송된 푸시 알림과 비교하여 바운스된 푸시 알림의 비율입니다.<br/> </td>
</tr>
  <tr> 
   <td> 게재됨<br/> </td> 
   <td> 보낸 총 메시지 수와 관련하여 성공적으로 보낸 메시지 수입니다.<br/> </td> 
</tr> 
  <tr> 
   <td> 전송률<br/> </td> 
   <td> 성공적으로 전송된 푸시 알림의 비율입니다.<br/> </td> 
</tr>
  <tr> 
   <td>참여 횟수<br/> </td> 
   <td> 이 푸시 알림에 대한 총 열기 및 작업 수(즉, 프로필이 푸시를 열었는지 또는 단추를 클릭했는지 여부)입니다.<br/> </td> 
</tr> 
  <tr> 
   <td> 참여 비율<br/> </td> 
   <td> 이 푸시 알림에 대한 열기 및 작업의 비율(즉, 프로필이 푸시를 열었는지 또는 단추를 클릭했는지 여부)입니다.<br/> </td> 
</tr>
  <tr> 
   <td> 오류<br/> </td> 
   <td> 게재 중에 발생한 총 오류로 인해 프로필이 전송되지 않았습니다.<br/> </td> 
</tr>
  <tr> 
   <td> 오류율<br/> </td> 
   <td> 전송 중에 발생한 오류로 인해 전송된 푸시 알림과 비교하여 전송되지 못했습니다.<br/> </td> 
</tr> 
  <tr> 
   <td> 제외<br/> </td> 
   <td> Adobe Journey Optimizer에서 제외된 프로필 수입니다.<br/> </td> 
</tr>
  <tr> 
   <td> 열림<br/> </td> 
   <td> 장치에 배달되고 사용자가 클릭했던 총 푸시 알림 수로 인해 앱이 열립니다. 알림이 무시되면 푸시 열기가 트리거되지 않는다는 점을 제외하고 푸시 클릭과 유사합니다.<br/> </td> 
</tr> 
  <tr> 
   <td> 오픈율<br/> </td> 
   <td> 열린 푸시 알림의 비율입니다.<br/> </td> 
</tr> 
  <tr> 
   <td> 보냄<br/> </td> 
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
   <td>Click rate<br/> </td> 
   <td>Percentage of users who interacted with the buttons included in the In-app message compared to users who saw the message.<br/> </td> 
</tr> 
  <tr> 
   <td>Dismiss rate<br/> </td> 
   <td> Percentage of In-app messages that recipients dismissed.<br/> </td> 
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
