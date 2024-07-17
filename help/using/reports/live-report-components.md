---
solution: Journey Optimizer
product: journey optimizer
title: 구성 요소 목록
description: 라이브 보고서의 데이터를 사용하는 방법을 알아봅니다
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 12168cdf-f517-49b5-958b-ba689ade6982
source-git-commit: c4ab97999d000d969f6f09f4d84be017d1288f94
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 0%

---

# 구성 요소 목록 {#list-of-components-live}

아래 표는 보고서에 사용된 지표 목록과 게재 유형에 따라 해당 정의를 제공합니다.

## 여정 지표 {#journey-metrics}

<table> 
 <thead> 
  <tr> 
   <th> 지표<br/> </th> 
   <th> 정의<br/> </th> 
</tr>
 </thead> 
 <tbody> 
  <tr> 
   <td>작업이 실행되었습니다<br/> </td> 
   <td> 여정에 대해 실행된 총 작업 수입니다.<br/> </td> 
</tr> 
  <tr> 
   <td> 입력한 프로필<br/> </td> 
   <td> 여정의 시작 이벤트에 도달한 총 개인 수입니다.<br/> </td> 
</tr>
  <tr> 
   <td> <br/> 작업에 오류가 있습니다. </td> 
   <td>작업에 대해 발생한 총 오류 수입니다.<br/> </td> 
</tr> 
  <tr> 
   <td> 종료된 프로필<br/> </td> 
   <td> 여정을 종료한 총 개인 수입니다.<br/> </td> 
</tr> 
  <tr> 
   <td> 실패한 개별 여정<br/> </td> 
   <td> 실행되지 않은 총 개별 여정 수입니다.<br/> </td> 
</tr> 
 </tbody> 
</table>

## 이메일 및 SMS 차원 및 지표 {#email-and-sms-metrics}

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
   <td> 게재 및 자동 반환 처리 중 누적된 총 오류입니다.<br/> </td> 
</tr> 
  <tr> 
   <td> 바운스 비율<br/> </td> 
   <td> 보낸 전자 메일과 비교하여 반송된 전자 메일의 비율입니다.<br/> </td> 
</tr>
  <tr> 
   <td> 클릭 수<br/> </td> 
   <td> 전자 메일에서 콘텐츠를 클릭한 횟수입니다.<br/> </td> 
</tr> 
  <tr> 
   <td> 게재됨: <br/> </td> 
   <td> 정상적으로 전송된 메시지 수입니다.<br/></td> 
</tr> 
  <tr> 
   <td> 게재 속도<br/> </td> 
   <td> 성공적으로 보낸 메시지의 비율입니다.<br/> </td> 
</tr>
  <tr> 
   <td> 오류<br/> </td> 
   <td> 게재 중 발생한 총 오류 수로 인해 프로필로 전송되지 않았습니다.<br/> </td> 
</tr> 
  <tr> 
   <td> 오류율<br/> </td> 
   <td> 게재 중 발생한 오류 중 게재를 방해하는 오류의 백분율이 보낸 전자 메일과 비교됩니다.<br/> </td> 
</tr>
  <tr> 
   <td> 제외됨<br/> </td> 
   <td> Adobe Journey Optimizer에서 제외된 프로필 수입니다.<br/> </td> 
</tr>
  <tr> 
   <td> 하드 바운스<br/> </td> 
   <td> 잘못된 이메일 주소와 같은 총 영구 오류 수. 여기에는 알 수 없는 사용자와 같이 주소가 유효하지 않다는 오류 메시지가 명시적으로 표시됩니다.<br/> </td>
</tr>
  <tr> 
   <td> 무시됨<br/> </td> 
   <td> 부재 또는 기술 오류와 같은 총 임시 항목 수(예: 보낸 사람 유형이 postmaster인 경우).<br/> </td> 
</tr>
   <tr> 
   <td>오퍼 클릭률<br/> </td> 
   <td>오퍼와 상호 작용한 사용자의 비율입니다.<br/> </td> 
</tr>
   <tr> 
   <td>오퍼 노출률<br/> </td> 
   <td>전송된 오퍼 수와 비교하여 열린 오퍼의 비율입니다.<br/> </td> 
</tr>
   <tr> 
   <td>오퍼 이름<br/> </td> 
   <td> 게재에 추가된 오퍼의 이름입니다. 배치에 대한 자세한 정보는 이 <a href="../offers/offer-library/creating-personalized-offers.md">페이지</a>.<br/>를 참조하세요. </td> 
</tr>
   <tr> 
   <td>전송된 오퍼<br/> </td> 
   <td>오퍼에 대한 총 전송 수입니다.<br/> </td> 
</tr> 
  <tr>
   <td>열기<br/> </td> 
   <td> 메시지를 연 횟수입니다.<br/> </td> 
</tr> 
  <tr> 
   <td> 열람률<br/> </td> 
   <td> 배달된 전자 메일 수와 비교하여 열린 전자 메일의 총 수입니다.<br/> </td> 
</tr>
  <tr> 
   <td>배치 이름<br/> </td> 
   <td> 오퍼를 표시하는 데 사용되는 배치 이름. 배치에 대한 자세한 내용은 이 <a href="../offers/offer-library/creating-placements.md">페이지</a>를 참조하세요. </td> 
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
   <td> 스팸 고객 불만<br/> </td> 
   <td> 메시지가 스팸 또는 정크로 선언된 횟수입니다.<br/> </td> 
</tr>
  <tr> 
   <td> <br/> 타깃팅됨 </td> 
   <td> 게재 분석 중에 처리된 총 메시지 수입니다.<br/> </td> 
</tr> 
  <tr> 
   <td> 고유 클릭수<br/> </td> 
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
   <td> 구독 취소 링크를 클릭한 횟수입니다.<br/> </td> 
</tr> 
 </tbody> 
</table>

## 랜딩 페이지 지표 {#landing-page-metrics}

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
   <td>랜딩 페이지와 상호 작용하지 않고 구독 작업을 완료하지 않은 사용자 수입니다.<br/> </td> 
</tr>
 <tr>
  <tr> 
   <td>클릭 수<br/> </td> 
   <td>랜딩 페이지에서 콘텐츠를 클릭한 횟수입니다.<br/> </td> 
</tr>
<tr>
<td>전환<br/> </td> 
   <td>양식을 구독하는 등 랜딩 페이지와 상호 작용한 사람의 수입니다.<br/> </td> 
</tr>
 <tr> 
   <td>여정<br/> </td> 
   <td>여정 방문 횟수입니다.<br/> </td> 
</tr>
 <tr> 
   <td>기타 원본<br/> </td> 
   <td>여정 대신 외부 소스에서 들어오는 랜딩 페이지 방문 횟수입니다.<br/> </td> 
</tr>
 <tr> 
   <td>총 방문 수<br/> </td> 
   <td> 여정 및 외부 소스에서 온 랜딩 페이지에 대한 총 방문 횟수로, 받는 사람 한 명이 여러 번 방문한 횟수입니다.<br/> </td> 
</tr>
 <tr> 
   <td>고유 방문자 수<br/> </td> 
   <td>랜딩 페이지를 방문한 사람 수, 받는 사람 한 명의 여러 방문 횟수를 고려하지 않습니다.<br/> </td> 
</tr>
 <tr> 
   <td>방문 횟수<br/> </td> 
   <td>받는 사람 한 명의 여러 방문을 포함하여 랜딩 페이지에 대한 방문 횟수입니다.<br/> </td> 
</tr>
 </tbody> 
</table>

## 푸시 알림 지표 {#push-notification-metrics}

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
   <td> 전달된 푸시 알림에 대한 총 작업 수(예: 단추 클릭 또는 해제).<br/> </td> 
</tr>
  <tr> 
   <td>바운스 수<br/> </td> 
   <td> 게재 및 자동 반환 처리 중 누적된 총 오류입니다.<br/> </td> 
</tr> 
  <tr> 
   <td> 배달됨<br/> </td> 
   <td> 성공적으로 보낸 메시지 수입니다.<br/> </td> 
</tr> 
  <tr> 
   <td>참여<br/> </td> 
   <td> 이 푸시 알림에 대한 열기 및 작업의 총 수입니다(프로필에서 푸시를 열었거나 단추를 클릭한 경우).<br/> </td> 
</tr> 
  <tr> 
   <td> 오류<br/> </td> 
   <td> 게재 중 발생한 총 오류 수로 인해 프로필로 전송되지 않았습니다.<br/> </td> 
</tr>
  <tr> 
   <td> 제외됨<br/> </td> 
   <td> Adobe Journey Optimizer에서 제외된 프로필 수입니다.<br/> </td> 
</tr>
  <tr> 
   <td> 열기<br/> </td> 
   <td> 장치로 전달되고 사용자가 클릭하여 앱을 여는 총 푸시 알림 수입니다. 알림이 무시되면 푸시 열기가 트리거되지 않는다는 점을 제외하면 푸시 클릭과 유사합니다.<br/> </td> 
</tr> 
  <tr> 
   <td> 보냄<br/> </td> 
   <td> 게재에 대한 총 전송 수입니다.<br/> </td> 
</tr> 
  <tr> 
   <td> <br/> 타깃팅됨 </td> 
   <td> 게재 분석 중에 처리된 총 푸시 메시지 수입니다.<br/> </td> 
</tr>  
 </tbody> 
</table>

<!--
## In-app metrics {#inapp-metrics}
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
