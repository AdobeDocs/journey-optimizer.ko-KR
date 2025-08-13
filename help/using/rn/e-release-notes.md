---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer에 대한 사전 릴리스 정보
description: Adobe Journey Optimizer 사전 릴리스 정보
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 7f9828c1781468155702d9f8fd475736a7656188
workflow-type: tm+mt
source-wordcount: '1046'
ht-degree: 47%

---

# 사전 릴리스 정보 {#e-release-notes}

[!DNL Adobe Journey Optimizer]은 지속적으로 새로운 기능, 기존 기능 개선, 버그 해결을 제공합니다. 모든 변경 사항은 매월 말 [릴리스 정보](release-notes.md)에 통합됩니다.


## 2025년 8월 프리릴리스 정보 {#25-8-rn}

**아래의 사전 릴리스 노트는 릴리스 사용 가능 날짜까지 사전 공지 없이 변경될 수 있습니다**. 링크, 화면 및 업데이트된 설명서는 릴리스 날짜에 릴리스 정보에 게시됩니다.

[Adobe Experience Platform 사전 릴리스 정보](https://experienceleague.adobe.com/ko/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}도 참조하십시오.

**릴리스 일자**: 2025년 8월 19일


### 새로운 기능 {#Aug-25-8-features}

<table>
<thead>
<tr>
<th><strong>여정 일시 중단 및 다시 시작</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 여정을 일시 중단했다가 다시 시작할 수 있습니다. 이 기능을 사용하면 고객 경험을 중단하지 않고 라이브 여정을 일시적으로 중단할 수 있으므로 여정 실무자가 여정을 보다 자유롭게 제어하고 유연하게 조정할 수 있습니다. 일시 중단하면 커뮤니케이션이 전송되지 않으며 프로필은 여정이 다시 시작될 때까지 보류 상태로 유지됩니다.</p>
<p>하나의 여정만 일시 중단했다가 다시 시작하거나, 여정 그룹에 일괄 일시 중단 및 다시 시작 작업을 수행할 수 있습니다.</p>
<p>또한 일시 중단된 프로필에 전역 필터를 적용하여 속성에 따라 프로필을 제외할 수 있습니다.</p>
<p><!--img src="assets/do-not-localize/PauseResume.gif"/>--></p>
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).</p>
<p><!--For more information, refer to the <a href="../building-journeys/journey-pause.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>캘린더 보기</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 여정 및 캠페인 목록에서 캘린더 보기를 사용할 수 있습니다. 이를 통해 각 목록에 있는 모든 여정 및 캠페인의 활성화를 시각화할 수 있습니다.</p>
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다. 이번 GA 릴리스에서는 다음과 같은 기능이 제공됩니다.</p>
<ul>
<li>날짜의 탐색을 위한 디자인 개선 사항,</li>
<li>시작 및 종료 날짜를 설정한 경우 초안 캠페인을 볼 수 있는 기능,</li>
<li>오랫동안 실행 중인 일정 항목을 숨기고 표시하는 새로운 설정입니다.</li>
</ul>
<p><!--img src="assets/do-not-localize/calendar.gif"/>--></p>
<p><!--For more information, refer to the <a href="../building-journeys/journey-ui.md#journeys-calendar">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>이메일 디자이너의 다크 모드</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer 이메일 디자이너에서 다크모드 보기로 전환할 수 있는 기능을 제공합니다. 이 기능에서는 다크모드에서 이메일을 읽는 수신자에게만 표시되는 특정 사용자 지정 설정을 추가로 정의할 수 있습니다.</p>
<p>다음 사항에 유의하십시오.</p>
<ul>
<li>다크모드 최종 렌더링은 수신자의 이메일 클라이언트에 따라 다를 수 있습니다.</li>
<li>모든 이메일 클라이언트가 사용자 정의 다크모드를 지원하지는 않습니다. 또한 일부 이메일 클라이언트는 수신되는 모든 이메일에 대해 자신의 기본 다크모드만 적용합니다. 두 경우 모두 이메일 디자이너에서 정의한 사용자 지정 설정을 렌더링할 수 없습니다.</li>
</ul>
<P>이 기능은 현재 Beta 버전으로 Beta 고객에게만 제공됩니다. Beta 프로그램에 참여하려면 Adobe 담당자에게 문의하십시오.</p>
<p><!--img src="assets/do-not-localize/dark-mode.gif"/>--></p>
<p><!--For more information, refer to the <a href="../email/dark-mode.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>개인화에 Adobe Experience Platform 데이터 사용</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>개인화 편집기에서 Adobe Experience Platform의 데이터를 활용하여 콘텐츠를 개인화할 수 있습니다. 이렇게 하려면 조회 개인화에 필요한 데이터 세트를 먼저 API 호출을 통해 활성화해야 합니다. 완료되면 해당 데이터를 사용하여 콘텐츠를 [!DNL Journey Optimizer]​(으)로 개인화할 수 있습니다.</p>
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다. 이번 일반 가용성 릴리스에서는 다음과 같은 개선 사항이 도입되었습니다.</p>
<ul>
<li>인바운드 채널 지원,</li>
<li>이제 "datasetLookup" 도우미 함수를 표현식 및 시각적 조각 내에서 사용하여 Adobe Experience Platform 데이터 세트의 데이터를 사용하여 콘텐츠를 개인화할 수 있습니다.</li>
<li>이제 데이터 세트의 옵션을 사용하면 API 호출을 수행하지 않고도 조회 개인화에 대한 데이터 세트를 활성화할 수 있습니다.</li>
</ul>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>이메일 채널에서 의사 결정 사용</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 이메일 여정 및 캠페인에 의사 결정 정책을 추가할 수 있습니다. 의사 결정 정책은 의사 결정 엔진을 활용하여 각 대상 구성원에 대해 제공할 최상의 콘텐츠를 동적으로 반환하는 오퍼에 대한 컨테이너입니다.</p>
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).</p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>여정 경로 최적화</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer은 AI 및 실험 프레임워크를 활용하여 여정을 최적화할 수 있는 도구를 제공하는 동시에 조건 및 최적화 기능 간의 원활한 유용성과 차별화를 보장합니다.</p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>여정의 작업 활동</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer은 단일 작업과 다중 채널 아웃바운드 작업을 모두 구성할 수 있는 새로운 일반 작업 활동을 지원하므로 여정 캔버스 내에서 작업 구성을 간소화할 수 있습니다. 또한 이 새로운 활동을 통해 타기팅 최적화, 실험 및 다국어 언어 변형을 모든 기본 제공 채널 작업에 추가할 수 있습니다.</p>
<p>이 기능은 제한적으로 이용할 수 있습니다. 액세스 권한을 얻으려면 Adobe 담당자에게 문의하십시오.</p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>랜딩 페이지 사용자 정의 양식</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer을 사용하여 사용자 정의 양식을 만들고 랜딩 페이지에서 이를 활용하여 프로필 속성을 각 양식에 대해 정의된 데이터 세트에 캡처할 수 있습니다.</p>
<p>이 기능은 현재 Beta 버전으로 Beta 고객에게만 제공됩니다. Beta 프로그램에 참여하려면 Adobe 담당자에게 문의하십시오.</p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>


### 개선 사항 {#Aug-25-8-improv}

다음은 이번 릴리스의 개선 사항 목록입니다.

- **관리**
   - **채널 구성 모니터링 경고** - 이제 채널 구성 오류가 발생하거나 DNS 레코드가 누락된 경우 시스템 경고를 수신하도록 이메일 또는 Journey Optimizer 알림 센터에서 구독할 수 있습니다.

- **캠페인**
   - **아웃바운드 캠페인의 비율 제어** - 이제 아웃바운드 캠페인(이메일, SMS, 푸시 알림)에 대한 전송률 제어를 활성화하여 랜딩 페이지나 고객 지원 플랫폼과 같은 다운스트림 시스템에서 오버로드를 방지할 수 있습니다.
   - **작업 캠페인 예약** - 세부 기간을 개선하기 위해 일일, 주별 및 월별 캠페인 스케줄러가 업데이트되었습니다. 예를 들어 이제 일정 간의 주/개월 수를 설정하고, 실행할 날짜를 정의하고, 특정 발생 횟수 이후 또는 특정 날짜에 중단하기로 결정할 수 있습니다.

- **채널 - 푸시**
   - **푸시 알림 만료일** - 이제 각 푸시 알림에 대해 만료일을 지정할 수 있습니다. 그러면 특정 날짜 이후에 시간에 민감한 메시지(예: 블랙 프라이데이 세일)가 전송되지 않으므로 고객에게 좋지 않은 경험이 전달되지 않습니다.

- **채널 - 전자 메일**
   - **전자 메일에 PDF 첨부 파일** - 이제 Journey Optimizer으로 보낸 전자 메일 메시지에 정적 PDF 파일을 첨부할 수 있습니다.

- **구성**
   - **동적 도메인 지원** - 이제 Journey Optimizer에서 채널 구성 수준에 나열된 사전 정의된 도메인의 URL 추적에 대한 개인화를 지원합니다.
   - **한 번 클릭 구독 취소 URL로 사용자 지정 특성 지원** - Journey Optimizer에서 Adobe 외부에서 동의를 관리하는 경우 이메일 구성에서 한 번 클릭 구독 취소 링크를 정의하여 외부 사용자 지정 끝점을 설정할 수 있습니다. 수신자가 구독 취소 링크를 클릭하면 Journey Optimizer이 일부 기본 프로필별 매개 변수를 동의 업데이트 이벤트에 추가합니다.

     이제 원클릭 구독 취소 링크를 개인화하기 위해 동의 이벤트에 추가할 사용자 지정 속성을 정의할 수 있습니다.

- **여정**
   - **대량 작업 여정** - 이제 여정 목록에서 여러 항목을 선택할 수 있습니다. 선택하면 한 번에 최대 10개의 여정을 일시 중지하거나 다시 시작할 수 있습니다.

