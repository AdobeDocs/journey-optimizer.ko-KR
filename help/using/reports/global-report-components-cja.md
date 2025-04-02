---
solution: Journey Optimizer
product: journey optimizer
title: 구성 요소 목록
description: 보고서에서 데이터를 사용하는 방법 알아보기
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: aa060d8e-23e2-4bab-b709-636077eb5d20
source-git-commit: ff722dd9f727a70fa3788f5e47a49e7a2fa7e952
workflow-type: tm+mt
source-wordcount: '1829'
ht-degree: 0%

---

# 지표 목록 {#list-of-components-global}

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
<td>여정 참여</td> 
<td>여정을 통해 전송된 메시지를 수신하여 여정의 지정된 작업 지점에 도달한 고유한 프로필을 나타내는 총 고유 개인 수입니다.</td> 
</tr> 
<tr> 
<td>여정 입력</td> 
<td>여정의 시작 이벤트에 도달한 총 개인 수입니다.</td> 
</tr>
<tr> 
<td>여정 종료</td> 
<td>여정을 종료한 총 개인 수.</td> 
</tr>
<tr> 
<td>여정 실패</td> 
<td>성공적으로 실행되지 않은 총 개별 여정 수입니다.</td> 
</tr>
<tr> 
<td>고유 여정 입력</td> 
<td>동일한 프로필의 여러 상호 작용을 고려하지 않고 여정의 시작 이벤트에 도달한 개인의 총 수입니다.</td> 
</tr>
<tr> 
<td>고유 여정 종료</td> 
<td>동일한 프로필의 여러 상호 작용을 고려하지 않고 여정을 종료한 총 개인 수입니다.</td> 
</tr>
<tr> 
<td>고유 여정 실패</td> 
<td>동일한 프로필의 여러 상호 작용을 고려하지 않고 성공적으로 실행되지 않은 총 개별 여정 수입니다.</td> 
</tr>
 </tbody> 
</table>

## 이메일 지표 {#email-metrics}

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
   <td> 보낸 총 메시지 수와 관련하여 전송 프로세스 및 자동 반환 처리 중에 누적된 총 오류입니다.<br/> </td> 
  </tr> 
  <tr> 
   <td> 클릭스루 열람율(CTOR)<br/> </td> 
   <td> 이메일을 연 횟수입니다.<br/> </td> 
  </tr>
  <tr> 
   <td> 클릭스루 비율(CTR)<br/> </td> 
   <td> 전자 메일과 상호 작용한 사용자의 비율입니다.<br/> </td> 
  </tr>
  <tr> 
   <td> 클릭 수<br/> </td> 
   <td> 전자 메일에서 콘텐츠를 클릭한 횟수입니다.<br/> </td> 
  </tr> 
  <tr> 
   <td> 게재됨: <br/> </td> 
   <td> 보낸 총 메시지 수와 관련하여 성공적으로 보낸 메시지 수.<br/></td> 
  </tr> 
  <tr> 
   <td> 게재 속도<br/> </td> 
   <td> 성공적으로 보낸 메시지의 비율입니다.<br/> </td> 
  </tr>
  <tr> 
   <td> 오류 이유<br/> </td> 
   <td> 오류의 특정 원래 원인 이름. <a href="exclusion-list.md">오류 원인에 대해 자세히 알아보기</a>.<br/> </td> 
  </tr>
  <tr> 
   <td> 오퍼 클릭률<br/> </td> 
   <td> 오퍼와 상호 작용한 사용자의 비율입니다.<br/> </td> 
  </tr>
  <tr> 
   <td> 오퍼 노출률<br/> </td> 
   <td> 전송된 오퍼 수와 비교하여 열린 오퍼의 비율입니다.<br/> </td> 
  </tr>
  <tr> 
   <td> 오퍼 이름<br/> </td> 
   <td> 게재에 추가된 오퍼의 이름입니다. 배치에 대한 자세한 정보는 이 <a href="../offers/offer-library/creating-personalized-offers.md">페이지</a>.<br/>를 참조하세요. </td> 
  </tr>
  <tr> 
   <td> 전송된 오퍼<br/> </td> 
   <td> 오퍼에 대한 총 전송 수입니다.<br/> </td> 
  </tr> 
  <tr> 
   <td> 열기<br/> </td> 
   <td> 메시지를 연 횟수입니다.<br/> </td> 
  </tr> 
  <tr> 
   <td> 아웃바운드 오류<br/> </td> 
   <td> 보내는 동안 프로필로 보낼 수 없는 총 오류 수입니다.<br/> </td> 
  </tr> 
  <tr> 
   <td> 아웃바운드 제외<br/> </td> 
   <td> Adobe Journey Optimizer에서 제외된 프로필 수입니다.<br/> </td> 
  </tr>
  <tr> 
   <td> 배치 이름<br/> </td> 
   <td> 오퍼를 표시하는 데 사용되는 배치 이름. 배치에 대한 자세한 내용은 이 <a href="../offers/offer-library/creating-placements.md">페이지</a>를 참조하세요. </td> 
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
   <td> 이메일에서 콘텐츠를 클릭한 프로필 수입니다.<br> 고유 클릭수를 계산할 때 지난 10일을 고려합니다. 프로필에서 10일 기간 내에 여러 번의 클릭을 등록하는 경우 고유 클릭으로 카운트됩니다. 그러나 프로필에서 10일 이상 떨어진 두 번의 클릭은 고유한 클릭으로 간주되지 않습니다.<br/> </td> 
  </tr>
  <tr> 
   <td> 고유 이메일 구독 취소<br/> </td> 
   <td> 이메일 구독을 취소한 프로필 수입니다.<br/> </td> 
  </tr>
  <tr> 
   <td> 고유 열기 수<br/> </td> 
   <td> 게재를 연 프로필 수입니다. <br> 고유 열람수를 계산할 때 지난 10일을 고려합니다. 프로필에서 10일 기간 내에 여러 개의 열기를 등록하는 경우 고유 열림으로 계산됩니다. 그러나 프로필의 열기가 10일 이상 차이가 나면 고유한 열기로 간주되지 않습니다.<br/> </td> 
  </tr> 
  <tr> 
   <td> 구독 취소<br/> </td> 
   <td> 구독 취소 링크를 클릭한 횟수입니다.<br/> </td> 
  </tr> 
 </tbody> 
</table>

## SMS 지표

<table> 
  <thead> 
    <tr> 
      <th> SMS 지표 </th> 
      <th> 정의 </th> 
    </tr>
  </thead> 
  <tbody> 
    <tr> 
      <td>게재됨</td> 
      <td>총 SMS 메시지 수와 관련하여 정상적으로 전송된 SMS 메시지 수입니다.</td> 
    </tr>
    <tr> 
      <td>클릭수</td> 
      <td>SMS 메시지 내의 링크를 클릭한 횟수입니다.</td> 
    </tr>
    <tr> 
      <td>아웃바운드 SMS 메시지에 대한 바운스</td> 
      <td>보낸 SMS 메시지의 총 수와 관련하여 전송 프로세스 및 자동 반환 처리 중에 누적된 오류의 총 수입니다.</td> 
    </tr>
    <tr> 
      <td>아웃바운드 SMS 오류</td> 
      <td>발생한 총 오류 수로, SMS 메시지가 수신자에게 전송되지 않습니다.</td> 
    </tr>
    <tr> 
      <td>아웃바운드 SMS 제외</td> 
      <td>Adobe Journey Optimizer에서 SMS 메시지를 받지 못한 프로필 수입니다.</td> 
    </tr>
    <tr> 
      <td>고유 클릭수</td> 
      <td>SMS 메시지에서 링크를 클릭한 고유 수신자 수.</td> 
    </tr>
    <tr> 
      <td>디스플레이</td> 
      <td>SMS 메시지가 표시되거나 열린 횟수입니다.</td> 
    </tr>
    <tr> 
      <td>고유 디스플레이</td> 
      <td>동일한 사용자의 여러 상호 작용을 제외하고 SMS 메시지를 연 고유 수신자의 수입니다.</td> 
    </tr>
    <tr> 
      <td>사람</td> 
      <td>SMS 메시지를 받았거나 SMS와 상호 작용한 고유 사용자 프로필 수입니다.</td> 
    </tr>
  </tbody> 
</table>

<!--
## Experimentation metrics {#experimentation-metrics}
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
   <td>Number of times the email was opened.<br/> </td> 
</tr>
  <tr> 
   <td>Email Unsubscribes<br/> </td> 
   <td>Number of clicks on the unsubscription link.<br/> </td> 
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
   <td>Number of profiles who opened the email.<br/> </td>
<tr>
  <tr> 
   <td>Unique email unsubscribes<br/> </td> 
   <td>Number of profiles who clicked on the unsubscription link.<br/> </td>
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

## 인앱 지표 {#inapp-metrics}

<table> 
 <thead> 
  <tr> 
   <th> 지표<br/> </th> 
   <th> 정의<br/> </th> 
  </tr>
 </thead> 
 <tbody>
  <tr> 
   <td>클릭 수<br/> </td> 
   <td>인앱 메시지에 포함된 단추와 상호 작용한 총 프로필 수입니다.<br/> </td> 
  </tr>
  <tr> 
   <td>클릭률<br/> </td> 
   <td>인앱 메시지에 포함된 단추와 상호 작용한 사용자의 백분율과 메시지를 본 사용자의 백분율입니다.<br/> </td> 
  </tr>
  <tr> 
   <td>취소율<br/> </td> 
   <td>프로필이 무시한 인앱 메시지의 비율입니다.<br/> </td> 
  </tr>
  <tr> 
   <td>노출 횟수<br/> </td> 
   <td>모든 사용자에게 전달된 인앱 메시지의 총 수입니다.<br/> </td>
  </tr>
  <tr> 
   <td>고유 노출 횟수<br/> </td> 
   <td>인앱 메시지가 전달된 고유 사용자 수입니다.<br/> </td>
  </tr>
  <tr> 
   <td><br/> 표시 </td>
   <td>인앱 메시지를 연 횟수입니다.<br/> </td>
  </tr>
  <tr> 
   <td>고유 디스플레이<br/> </td>
   <td>동일한 프로필에서 여러 상호 작용을 제외하고 인앱 메시지를 연 횟수입니다.<br/> </td>
  </tr>
  <tr> 
   <td>고유 클릭수<br/> </td>
   <td>인앱 메시지의 콘텐츠를 클릭한 프로필 수입니다.<br/> </td>
  </tr>
  <tr> 
   <td>클릭 수<br/> </td>
   <td>인앱 메시지에서 콘텐츠를 클릭한 횟수입니다.<br/> </td>
  </tr>
  <tr> 
   <td>클릭스루 비율(CTR)<br/> </td>
   <td>인앱 메시지와 상호 작용한 사용자의 비율입니다.<br/> </td>
  </tr>
  <tr> 
   <td>클릭스루 열람율(CTOR)<br/> </td>
   <td>인앱 메시지를 연 횟수입니다.<br/> </td>
  </tr>
  <tr> 
   <td>전송<br/> </td>
   <td>보낸 인앱 메시지의 총 수입니다.<br/> </td>
  </tr>
  <tr> 
   <td>인바운드 트리거됨<br/> </td>
   <td>인앱 메시지가 사용자 상호 작용 또는 사전 정의된 이벤트에 의해 트리거된 횟수입니다.<br/> </td>
  </tr>
  <tr> 
   <td>인바운드 취소<br/> </td>
   <td>사용자가 인앱 메시지와 상호 작용하지 않고 인앱 메시지를 해제한 횟수입니다.<br/> </td>
  </tr>
 </tbody> 
</table>

## 푸시 알림 지표

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
   <td> 보낸 총 메시지 수와 관련하여 게재 및 자동 반환 처리 중에 누적된 총 오류.<br/> </td> 
</tr> 
  <tr> 
   <td> 바운스 비율<br/> </td> 
   <td> 보낸 푸시 알림과 비교하여 반송된 푸시 알림의 비율입니다.<br/> </td>
</tr>
  <tr> 
   <td> 배달됨<br/> </td> 
   <td> 보낸 총 메시지 수와 관련하여 성공적으로 보낸 메시지 수입니다.<br/> </td> 
</tr> 
  <tr> 
   <td> 게재율<br/> </td> 
   <td> 푸시 알림이 성공적으로 전송된 비율입니다.<br/> </td> 
</tr>
  <tr> 
   <td>참여<br/> </td> 
   <td> 이 푸시 알림에 대한 열기 및 작업의 총 수입니다(프로필에서 푸시를 열었거나 단추를 클릭한 경우).<br/> </td> 
</tr> 
  <tr> 
   <td> 참여 비율<br/> </td> 
   <td> 이 푸시 알림에 대한 열기 및 작업의 비율(예: 프로필에서 푸시를 열었거나 단추를 클릭한 경우)입니다.<br/> </td> 
</tr>
  <tr> 
   <td> 오류<br/> </td> 
   <td> 게재 중 발생한 총 오류 수로 인해 프로필로 전송되지 않았습니다.<br/> </td> 
</tr>
  <tr> 
   <td> 오류율<br/> </td> 
   <td> 게재 중에 발생하여 게재를 방해하는 오류의 백분율과 전송된 푸시 알림의 백분율입니다.<br/> </td> 
</tr>
  <tr> 
   <td> 오류 이유<br/> </td> 
   <td> 오류의 특정 원래 원인 이름. <a href="exclusion-list.md">오류 원인에 대해 자세히 알아보기</a>.<br/> </td> 
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
   <td> 열람률<br/> </td> 
   <td> 열린 푸시 알림의 비율입니다.<br/> </td> 
</tr>
  <tr> 
   <td> 푸시 사용자 지정 작업<br/> </td> 
   <td>푸시 알림에 대한 응답으로 프로필에서 수행한 사용자 지정 작업 수입니다.<br/> </td> 
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
   <td>바운스 비율<br/> </td> 
   <td>랜딩 페이지를 열람했지만 상호 작용하거나 구독하지 않은 사용자의 백분율로, 총 방문 횟수에 상대적입니다.<br/> </td> 
</tr>
 <tr> 
   <td>클릭 수<br/> </td> 
   <td>랜딩 페이지에서 콘텐츠를 클릭한 횟수입니다.<br/> </td> 
</tr>

<tr> 
   <td>랜딩 페이지 전환<br/> </td> 
   <td>양식을 구독하는 등 랜딩 페이지와 상호 작용한 사람의 수입니다.<br/> </td> 
</tr>
<tr> 
   <td>랜딩 페이지 전환율<br/> </td> 
   <td>총 방문 횟수와 관련하여 랜딩 페이지와 상호 작용한 사람(예: 양식에 구독한 사람)의 비율입니다.<br/> </td> 
</tr>
 <tr> 
   <td>랜딩 페이지 보기<br/> </td> 
   <td>동일한 프로필의 여러 방문을 포함하여 여정 및 외부 소스에서 랜딩 페이지로 이동하는 총 방문 수입니다.<br/> </td> 
</tr>
<tr> 
   <td>고유한 랜딩 페이지 전환<br/> </td> 
   <td>동일한 프로필에서 여러 상호 작용을 제외하고 랜딩 페이지와 상호 작용한 고유 사용자의 수입니다.<br/> </td> 
</tr>
 <tr> 
   <td>고유한 랜딩 페이지 보기 수<br/> </td> 
   <td>동일한 프로필에서 여러 번 방문한 경우를 제외하고 랜딩 페이지를 방문한 고유 사용자의 수입니다.<br/> </td> 
</tr>
 </tbody> 
</table>

## 다이렉트 메일 {#direct-mail}

<table> 
 <thead> 
  <tr> 
   <th> 지표<br/> </th> 
   <th> 정의<br/> </th> 
  </tr>
 </thead> 
 <tbody>
<tr> 
   <td>배달됨<br/> </td> 
   <td>받는 사람에게 배달된 DM 메시지 수입니다.<br/> </td> 
</tr>
<tr> 
   <td>아웃바운드 오류<br/> </td> 
   <td>처리하거나 보내는 동안 오류가 발생하여 배달이 되지 않은 DM 메시지 수입니다.<br/> </td> 
</tr>
<tr> 
   <td>아웃바운드 제외<br/> </td> 
   <td>사전 정의된 기준이나 Adobe Journey Optimizer의 필터링으로 인해 DM 수신에서 제외된 프로필 수입니다.<br/> </td> 
</tr>
<tr> 
   <td>프로필<br/> </td> 
   <td>DM 캠페인의 대상 대상자로 식별된 사용자 프로필 수입니다.<br/> </td> 
</tr>
<tr> 
   <td>보냄<br/> </td> 
   <td>캠페인의 일부로 보낸 DM 메시지의 총 수입니다.<br/> </td> 
</tr>
<tr> 
   <td><br/> 타깃팅됨 </td> 
   <td>전송을 위해 준비 및 처리된 총 DM 메시지 수입니다.<br/> </td> 
</tr>
 </tbody> 
</table>


## 콘텐츠 카드 지표 {#content-based}

<table> 
 <thead> 
  <tr> 
   <th> 지표<br/> </th> 
   <th> 정의<br/> </th> 
  </tr>
 </thead> 
 <tbody>
<tr> 
   <td>클릭스루 비율(CTR)<br/> </td> 
   <td>콘텐츠 카드와 상호 작용한 사용자의 비율입니다.<br/> </td> 
</tr>
<tr> 
   <td>클릭 수<br/> </td> 
   <td>콘텐츠 카드에서 콘텐츠를 클릭한 횟수입니다.<br/> </td> 
</tr>
<tr> 
   <td><br/> 표시 </td> 
   <td>메시지를 연 횟수입니다.<br/> </td> 
</tr>
<tr> 
   <td>직원<br/> </td> 
   <td>콘텐츠 카드의 대상 프로필로 사용할 수 있는 사용자 프로필 수입니다.<br/> </td> 
</tr>
<tr> 
   <td>고유 클릭수<br/> </td> 
   <td>콘텐츠 카드에서 콘텐츠를 클릭한 프로필 수입니다.<br/> </td> 
</tr>
<tr> 
   <td>고유 디스플레이<br/> </td> 
   <td>메시지를 연 횟수이며 한 프로필의 여러 상호 작용을 고려하지 않습니다.<br/> </td> 
</tr>
 </tbody> 
</table>

## 웹 페이지 지표 {#web}

<table> 
 <thead> 
  <tr> 
   <th> 지표<br/> </th> 
   <th> 정의<br/> </th> 
  </tr>
 </thead> 
 <tbody>
<tr> 
   <td>클릭 수<br/> </td> 
   <td>웹 페이지에서 콘텐츠를 클릭한 횟수입니다.<br/> </td> 
</tr>
<tr> 
   <td>클릭스루 비율(CTR)<br/> </td> 
   <td>웹 페이지와 상호 작용한 사용자의 비율입니다.<br/> </td> 
</tr>
<tr> 
   <td><br/> 표시 </td> 
   <td>웹 페이지를 연 횟수입니다.<br/> </td> 
</tr>
<tr> 
   <td>직원<br/> </td> 
   <td>웹 페이지에 대한 대상 프로필로 적합한 프로필의 수입니다.<br/> </td> 
</tr>
<tr> 
   <td>고유 클릭수<br/> </td> 
   <td>웹 페이지에서 콘텐츠를 클릭한 프로필 수입니다.<br/> </td> 
</tr>
<tr> 
   <td>고유 디스플레이<br/> </td> 
   <td>웹 페이지를 연 횟수입니다. 한 프로필의 여러 상호 작용을 고려하지 않습니다.<br/> </td> 
</tr>
 </tbody> 
</table>

## 코드 기반 경험 지표 {#code-based}

<table> 
 <thead> 
  <tr> 
   <th> 지표<br/> </th> 
   <th> 정의<br/> </th> 
  </tr>
 </thead> 
 <tbody>
<tr> 
   <td>클릭 수<br/> </td> 
   <td>사용자에게 표시된 개인화된 경험을 사용자가 클릭한 총 횟수입니다.<br/> </td> 
</tr>
<tr> 
   <td>클릭스루 비율(CTR)<br/> </td> 
   <td>링크, 광고 또는 권장 사항을 클릭한 사용자 수와 표시된 횟수가 비교한 비율입니다.<br/> </td> 
</tr>
<tr> 
   <td>전환율<br/> </td> 
   <td>모델이 사용자 참여를 성공적으로 이끌었음을 나타내는 사용자 작업(예: 클릭)을 초래한 디스플레이의 비율입니다.<br/> </td> 
</tr>
<tr> 
   <td>결정 항목 성능<br/> </td> 
   <td>각 항목이 사용자의 참여를 유도하고 구매, 클릭 수 또는 기타 응답과 같은 원하는 작업을 유도하는 데 얼마나 적합한지 평가합니다.<br/> </td> 
</tr>
<tr> 
   <td>의사 결정 KPI<br/> </td> 
   <td>총 항목 수, 총 클릭 수, 총 디스플레이 수 및 대체 비율을 포함하여 방문자의 경험 참여에 대한 주요 통찰력입니다.<br/> </td> 
</tr>
<tr> 
   <td><br/> 표시 </td> 
   <td>다양한 접점에서 개인화된 경험이 사용자에게 표시되거나 제공된 총 횟수입니다.<br/> </td> 
</tr>
<tr> 
   <td>참여 단계<br/> </td> 
   <td>단계 단계별로 사용자 상호 작용을 얼마나 효과적으로 유도하는지 평가하여 개인화된 경험의 성능을 모니터링합니다.<br/> </td> 
</tr>
<tr> 
   <td>선택 전략별 참여 단계<br/> </td> 
   <td>다양한 선택 전략이 개인화된 경험으로 사용자를 얼마나 효과적으로 끌어들이는지 모니터링하고 분석합니다.<br/> </td> 
</tr>
<tr> 
   <td>직원<br/> </td> 
   <td>코드 기반 경험에 대한 대상 프로필로 적합한 사용자 프로필의 수입니다.<br/> </td> 
</tr>
<tr> 
   <td>순위 전략<br/> </td> 
   <td>모델 기반 및 홀드아웃의 두 트래픽 유형을 비교하는 AI 기반 등급 모델의 성능에 대한 인사이트.<br/> </td> 
</tr>
<tr> 
   <td>CTR<br/>의 최상위 결정 항목 </td> 
   <td>클릭스루 비율(CTR)에 따라 개별 항목의 성능을 강조 표시하여 사용자를 참여시키는 데 가장 효과적인 항목을 평가하는 데 도움이 됩니다.<br/> </td> 
</tr>
<tr> 
   <td>고유 클릭수<br/> </td> 
   <td>코드 기반 경험에서 콘텐츠를 클릭한 프로필 수입니다.<br/> </td> 
</tr>
<tr> 
   <td>고유 디스플레이<br/> </td> 
   <td>경험이 열린 횟수에서는 한 프로필의 여러 상호 작용을 고려하지 않습니다.<br/> </td> 
</tr>
 </tbody> 
</table>
