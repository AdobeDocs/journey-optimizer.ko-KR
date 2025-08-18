---
solution: Journey Optimizer
product: journey optimizer
title: 2024년 릴리스 정보
description: Journey Optimizer 2024년 릴리스 정보
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: bae533c5-1bfc-48bf-9f8d-1145383c040c
source-git-commit: 4d7ad2c3ed71801298f1afe31d0e29d7bb1d5c7f
workflow-type: ht
source-wordcount: '6783'
ht-degree: 100%

---

# 2024년 릴리스 정보 {#release-notes-2024}

이 페이지에서는 2024년에 릴리스된 [!DNL Journey Optimizer]의 기능과 개선 사항 목록을 확인할 수 있습니다.

## 2024년 10월 릴리스 {#24-10-rn}

**릴리스 일자**: 2024년 10월 29~30일

### 새로운 기능 {#24-10-features}

이번 릴리스에는 아래에 있는 새로운 기능이 제공됩니다.

<table>
<thead>
<tr>
<th><strong>이메일 콘텐츠 잠그기</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer에서 이메일 템플릿의 콘텐츠를 잠글 수 있습니다. 템플릿 전체를 잠그거나 특정 구조 및 구성 요소를 잠그는 것이 가능합니다. 이를 통해 의도하지 않은 편집 또는 삭제를 방지할 수 있으므로 템플릿의 사용자 정의 기능을 더욱 강력하게 제어하고 이메일 캠페인의 효율성과 안정성을 향상시킬 수 있습니다.</p>
<p>자세한 내용은 <a href="../content-management/content-locking.md">세부 설명서</a>를 참조하십시오.</p>
<img src="assets/do-not-localize/gif-content-locking.gif">
<p>2024년 10월 24일 이후 사용 가능</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>여정의 코드 기반 경험</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>코드 기반 경험 채널에서는 Adobe Journey Optimizer에서 원하는 인바운드 속성에 대해 고급 개인화 및 테스트를 수행할 수 있으므로 웹 앱, 모바일 앱, 데스크탑 앱, 비디오 콘솔, TV에 연결된 디바이스, 스마트 TV, 키오스크, ATM, IoT 디바이스 등과 같은 다양한 접점에서 맞춤형 경험을 원활하게 전달할 수 있습니다. 이제 여정 캔버스에서 코드 기반 경험 채널을 사용할 수 있습니다.</p>
<p>자세한 내용은 <a href="../code-based/create-code-based.md">세부 설명서</a>를 참조하십시오.</p>
<img src="../assets/do-not-localize/code-based-journey.gif"/>
<p>2024년 10월 1일 이후 사용 가능</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>여정의 웹 경험</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>웹 채널을 사용하면 Adobe Journey Optimizer에서 인바운드 웹 채널을 통해 고객에게 제공하는 웹 경험을 개인화할 수 있습니다. 이제 여정 캔버스에서 웹 채널을 사용할 수 있습니다.</p>
<p>자세한 내용은 <a href="../web/create-web.md">세부 설명서</a>를 참조하십시오.</p>
<img src="../assets/do-not-localize/web-journey.gif"/>
<p>2024년 10월 1일 이후 사용 가능</p>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>충돌 및 우선 순위 관리(제한된 가용성)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer에서 너무 많은 상호 작용으로 고객에게 부담을 주는 상황을 피하려면 캠페인과 여정의 양과 타이밍을 관리하는 것이 필수적입니다. 이제 Journey Optimizer에서 충돌 관리 및 우선 순위를 위한 몇 가지 도구를 제공합니다. <p>자세한 내용은 <a href="../conflict-prioritization/gs-conflict-prioritization.md">세부 설명서</a>를 참조하십시오.</p></p><p><ul><li><b>여정 빈도 캡핑</b>: 이제 여정에 적용할 규칙 집합을 만들어 일별, 주별 또는 월별로 한 프로필의 여정 수를 제한하고, 한꺼번에 실행되는 동시 여정 수도 제어할 수 있습니다.</li>
<li><b>우선 순위 점수</b>: 이제 캠페인이나 여정에 0에서 100 사이의 우선 순위 점수를 할당할 수 있습니다. 숫자가 높을수록 우선 순위가 높다는 뜻입니다. 두 캠페인 또는 여정이 동일한 채널 구성을 사용하는 경우 Journey Optimizer에서 우선 순위 점수가 가장 높은 캠페인 또는 여정을 선택합니다. 캠페인의 점수가 동일한 경우, 수정한지 가장 오래된 캠페인을 선택합니다.</li>
<li><b>잠재적 충돌 보기</b>: 이제 여정 및 캠페인의 새로운 "잠재적 충돌 보기" 버튼을 사용하여 시작 일자, 타깃팅된 대상자 또는 선택한 채널 구성 등이 다른 여정 또는 캠페인과 겹치는지 확인할 수 있습니다.</li>
<li><b>여정 중재</b>: 이 새로운 기능을 사용하면 고객에게 가장 중요한 여정을 우선시할 수 있습니다. 고객이 우선 순위가 더 높은 예정된 여정에 입장할 자격이 있는 경우 우선 순위가 낮은 여정에 들어가지 않도록 하는 규칙을 만들 수 있습니다.</li>
<li><b>커뮤니케이션 유형별 빈도 캡핑: </b>이제 규칙 세트 기능으로 커뮤니케이션 유형(예: 영업, 프로모션)마다 세분화된 규칙을 설정하여 고객에게 유사한 메시지를 과하게 보내는 상황을 예방할 수 있습니다. 여러 채널에 걸쳐 빈도를 제어할 수 있으며, 그간 과도하게 참여를 요청한 프로필을 자동으로 제외하여 고객 경험을 개선할 수 있습니다.</li></ul>

<img src="assets/do-not-localize/gif-conflict.gif">

<p>충돌 및 우선 순위 관리 기능은 제한된 가용성으로 일부 고객이 사용할 수 있습니다. 이 기능은 향후 더 많은 사용자에게 점진적으로 배포될 예정입니다. 이 기능에 대한 대기자 명단에 등록하려면 계정 팀에 문의하십시오.</p>

</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Movable Ink와 Adobe Journey Optimizer 통합</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Movable Ink Da Vinci와 Adobe Journey Optimizer를 통합할 수 있습니다. 이 새로운 통합을 통해 다음과 같은 작업을 수행할 수 있습니다. </p>
<p><ul><li>Movable Ink의 Da Vinci 제품에 포함된 강력한 기능을 활용하여 배치 캠페인에 사용할 이메일 변형을 조합하고 개인화</li>
<li>작성에는 Da Vinci를, 최적화 및 게재에는 Adobe Journey Optimizer를 사용하여 Journey Optimizer 고객의 실무 워크플로 가속화</li>
<li>Adobe 데이터로 Da Vinci 모델 최적화</li></ul></p>
<p>자세한 내용은 <a href="https://movableink.com/adobe-and-movable-ink">Movable Ink Da Vinci 설명서</a>를 참조하십시오.</p>
</tr>
</tbody>
</table>

이전에는 일부 조직에서만 사용할 수 있었던(LA) 아래 기능을 이제 모든 사용자가 사용할 수 있습니다(GA).

<table>
<thead>
<tr>
<th><strong>이메일 구성 개인화(일반 가용성) </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이메일 설정을 보다 유연하고 정밀하게 제어하기 위해 이메일 채널 구성을 만들 때 동적 하위 도메인 및 개인화된 헤더 매개 변수를 정의할 수 있습니다.
</p>
<p>자세한 내용은 <a href="../email/surface-personalization.md">세부 설명서</a>를 참조하십시오.</p>
<img src="assets/do-not-localize/surface-perso.gif"/>
<p>2024년 10월 23일 이후 사용 가능</p>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>여정 및 캠페인의 승인(일반 가용성)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 승인 정책을 사용하여 Journey Optimizer 내 승인 프로세스를 설정할 수 있습니다. 이를 통해 마케팅 팀에서 캠페인 및 여정을 라이브로 전환하기 전에 적절한 이해 관계자의 검토 및 승인을 놓치지 않을 수 있습니다.</p>
<p>자세한 내용은 <a href="../test-approve/gs-approval.md">세부 설명서</a>를 참조하십시오.</p>
<img src="assets/do-not-localize/approval.gif"/>
<p>2024년 10월 22일 이후 사용 가능</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>여정 내 콘텐츠 실험(일반 가용성)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer가 이제 여정에서도 실험을 지원합니다. 캠페인에서는 이미 실험을 사용할 수 있습니다. 실험은 무작위화한 시험 회기 여러 개를 모아 놓은 것입니다. 온라인 테스팅 맥락에서는 무작위로 선택한 사용자 일부를 특정한 버전의 메시지에 노출하고, 무작위로 선택한 다른 사용자들을 다른 처리 버전에 노출하는 것을 말합니다. 노출 후에는 이메일 열람, 구독 또는 구매 등 궁금한 결과 지표를 측정할 수 있습니다.</p>
<p>자세한 내용은 <a href="../content-management/content-experiment.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>의사 결정(일반 가용성)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이전에는 일부 조직에서만 사용할 수 있고(LA) 경험 결정이라는 이름으로 제공되었던 의사 결정 기능을 이제 Adobe Healthcare Shield 또는 Privacy and Security Shield Add-on 오퍼를 구입한 조직을 포함하여 모든 Adobe 사용자가 사용할 수 있습니다(GA).</p><p>의사 결정 기능은 '의사 결정 항목'이라는 중앙 집중식 마케팅 카탈로그와 정교한 의사 결정 엔진을 제공하여 개인화를 간소화합니다. 이 엔진은 규칙과 순위 기준을 활용하여 각 개인에게 가장 관련성 높은 의사 결정 항목을 선택하고 제공합니다. 이 의사 결정 항목은 코드 기반 경험 채널을 통해 광범위한 인바운드 표면에 원활하게 통합됩니다.</p>
<p>자세한 내용은 <a href="../experience-decisioning/gs-experience-decisioning.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>여정 및 캠페인의 다국어 메시지(일반 가용성)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 단일 캠페인 또는 여정 내에서 간편하게 여러 언어로 콘텐츠를 만들 수 있습니다. 이 기능을 사용하면 캠페인이나 여정을 편집할 때 언어를 전환할 수 있으므로 전체 편집 프로세스를 간소화하고 다국어 콘텐츠를 더욱 효율적으로 관리할 수 있습니다.</p>
<p>자세한 내용은 <a href="../content-management/multilingual-gs.md">세부 설명서</a>를 참조하십시오.</p>
<img src="assets/do-not-localize/multilingual.gif">
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>업데이트된 보고 환경(일반 가용성)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer의 보고 기능이 이제 일반 가용성(GA)으로 공개되었습니다. 이 기능은 Customer Journey Analytics 기능의 개선된 상호 운용성과 함께 제공되어 양 플랫폼의 보고를 표준화하고 데이터의 일관성과 안정성을 개선합니다. 이렇게 Journey Optimizer와 Customer Journey Analytics가 원활하게 통합됨으로써 사용자가 성과 지표를 보다 명확하게 확인하여 확실한 정보에 근거한 결정을 내릴 수 있습니다.</p>
<p>일반 가용성 전환과 더불어 네 가지 새로운 기능이 도입되었습니다. 이제 간단한 지표 만들기, 대상자 만들기 및 게시, Insight Builder를 사용한 임시 질문 사용, 주요 수신자에게 이메일로 자동 전송할 보고서 예약이 가능합니다.</p>
<p>자세한 내용은 <a href="../reports/report-cja-manage.md">세부 설명서</a>를 참조하십시오.</p>
<img src="assets/do-not-localize/ajo-cja.gif">
<p>중요: 현재 보고 경험은 2025년 1월부로 사용이 종료됩니다. 이 날짜 이후에는 새로운 보고 경험이 표준이 됩니다. 원활한 전환을 위해 새로운 기능을 숙지하는 것이 좋습니다. <a href="../reports/report-gs-cja.md">Journey Optimizer의 새로운 보고 인터페이스를 시작하는 방법 알아보기</a></p>
<p>2024년 10월 16일 이후 사용 가능</p>
</tr>
</tbody>
</table>

<!--The following capabilities are available to all customers in public beta:-->

<table>
<thead>
<tr>
<th><strong>샘플 입력 데이터를 사용하여 콘텐츠 테스트(Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer에서 콘텐츠의 다양한 변형을 테스트하기 위해 파일에서 업로드하거나 수동으로 추가한 샘플 입력 데이터를 사용하여 변형을 미리 보고 이메일 증명을 전송할 수 있습니다. 콘텐츠에서 개인화를 위해 사용되는 모든 프로필 속성은 시스템에서 자동 감지되며, 이를 테스트에 사용하여 여러 변형을 만들 수 있습니다.</p>
<p>이 기능은 현재 모든 고객이 이메일, SMS 및 푸시 알림 채널에 공개 Beta 버전으로 사용할 수 있습니다.</p>
<p>자세한 내용은 <a href="../test-approve/simulate-sample-input.md">세부 설명서</a>를 참조하십시오.</p>
<img src="assets/do-not-localize/gif-simulate.gif">
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>개인화(Beta)에 Adobe Experience Platform 데이터 사용</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>개인화 편집기에서 Adobe Experience Platform의 데이터를 활용하여 콘텐츠를 개인화할 수 있습니다. 이렇게 하려면 조회 개인화에 필요한 데이터 세트를 먼저 API 호출을 통해 활성화해야 합니다. 완료되면 해당 데이터를 사용하여 콘텐츠를 [!DNL Journey Optimizer]​(으)로 개인화할 수 있습니다.</p>
<p>이 기능은 모든 고객이 공개 Beta로 사용할 수 있습니다.</p>
<p>자세한 내용은 <a href="../personalization/aep-data-perso.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>

### 개선 사항 {#24-10-improvements}

이 릴리스는 아래 목록에 있는 개선 사항과 함께 제공됩니다.

**SMS 채널**

* 이제 SMS API 채널 구성을 편집하거나 삭제할 수 있습니다. [자세히 알아보기](../sms/sms-configuration.md)

* Infobip 및 Sinch를 통한 SMS 메시지 기능 강화를 위해 다음 같은 개선 사항이 도입되었습니다.

   * SMS 캠페인 및 여정에 대한 고유 키워드를 정의하고 관리하여 보다 개인화되고 효율적인 커뮤니케이션을 가능하게 할 수 있습니다.

   * 키워드가 인식되지 않을 때 사용할 기본 SMS 메시지를 만들고 전송할 수 있습니다.

  [Infoip](../sms/sms-configuration-infobip.md) 및 [Sinch](../sms/sms-configuration-sinch.md)에 대한 SMS 구성 설명서에서 이러한 개선 사항에 대해 자세히 알아보십시오.


<!--**Journeys**-->

<!--* **Path experiment in journeys** - With the journey path experiment, you can now define and track key metrics for your journey paths, allowing you to measure the impact of your activities and to provide clearer insights into your performance. -->

<!--* **Max number of Live journeys** - Journey Optimizer now has a guardrail of 500 live journeys on production sandboxes, instead of 100. The number of live journeys is visible in the journey canvas. (DOCAC-10977) -->

**웹 채널**

* **웹 디자이너용 비시각적 편집 모드** - 이제 Journey Optimizer 웹 디자이너 대신 비시각적 편집기를 사용하여 웹 사이트에 수정 사항을 추가할 수 있습니다. 이 모드를 사용하면 페이지를 시각적 편집기에서 열지 않고도 변경 사항을 수동으로 입력할 수 있습니다. 이 비시각적 편집 모드는 웹 디자이너에서 페이지를 로드하는 데 필요한 Adobe Experience Cloud Visual Helper와 같은 브라우저 확장 프로그램을 설치할 수 없는 경우에 유용합니다. [자세히 알아보기](../web/web-non-visual-editor.md)


**데이터 세트**

* **이벤트 전송 및 열기** - 2024년 11월 1일부터 스트리밍 세분화에서는 더 이상 Journey Optimizer 추적 및 피드백 데이터 세트의 이벤트 전송 및 열기를 지원하지 않습니다. 이 변경 사항은 모든 고객 샌드박스 및 조직에 적용됩니다. [자세히 알아보기](../data/datasets-ttl.md#segmentation-update)

* **데이터 세트 TTL(Time-to-Live)** - 2025년 2월부터 새 샌드박스 및 새 조직의 Journey Optimizer 시스템 생성 데이터 세트에 대해 다음과 같은 TTL(Time-to-Live) 가드레일이 롤아웃됩니다.

   * 프로필 스토어의 데이터에 대해 90일
   * 데이터 레이크의 데이터에 대해 13개월

  이 변경 사항은 차후 기존 고객 샌드박스에 대해서도 롤아웃됩니다. [자세히 알아보기](../data/datasets-ttl.md#ttl)

* **사용자 정의 액션의 매개 변수**(사용 가능한 날짜: 2024년 10월 3일) - 이제 사용자 정의 액션에서 NULL 및 선택적 매개 변수가 지원됩니다. [자세히 알아보기](../action/about-custom-action-configuration.md#define-the-message-parameters)

**보고**

* 이제 **결정 보고**&#x200B;를 사용할 수 있습니다. 이 기능은 방문자가 경험과 상호 작용하는 방식에 대해 기본적인 인사이트를 제공합니다. [자세히 알아보기](../reports/campaign-global-report-cja-code.md#decisioning-kpis)

**데이터 거버넌스 및 동의 정책** - 사용 가능한 날짜: 2024년 10월 7일

* **데이터 거버넌스 정책** 시행이 이제 Journey Optimizer의 모든 채널에 적용됩니다. Adobe Experience Platform에서 정책을 만든 고객의 경우 이 정책은 채널 구성 설정의 일부로 마케팅 액션에 적용됩니다. 구성을 사용하여 콘텐츠를 만들 때 시스템은 모든 개인화 필드를 확인하여 데이터 거버넌스 위반 여부를 찾습니다. 위반이 발견되면 여정 또는 캠페인을 게시할 수 없습니다. [자세히 알아보기](../action/action-privacy.md)

* 이제 **사용자 정의 동의 정책**&#x200B;이 모든 Journey Optimizer 채널에 적용됩니다. 메시지가 전송되거나 인바운드 경험이 게재되기 전에 적용 시 시스템은 사용자가 수신할 콘텐츠의 개인화 필드 사용에 동의했는지 확인합니다. 동의를 하지 않은 경우 해당 경험이 표시되지 않습니다. [자세히 알아보기](../action/consent.md)

  >[!NOTE]
  >
  >동의 정책 기능은 현재 Adobe **Healthcare Shield** 또는 **Privacy and Security Shield** 추가 기능 서비스를 구매한 조직에만 제공됩니다.

**대상자** - 사용 가능한 날짜: 2024년 10월 8일

* 이제 CSV 파일 대상자를 타기팅할 때 개인화 편집기와 여정 및 캠페인 규칙 빌더에서 파일의 속성을 사용할 수 있습니다. [자세히 알아보기](../audience/about-audiences.md)

* 이제 사용자 정의 업로드(CSV 파일)의 대상자 및 속성을 Healthcare Shield 또는 Privacy and Security Shield에서도 사용할 수 있습니다.

**구성** - 사용 가능한 날짜: 2024년 10월 23일

* 이제 캠페인 또는 여정에서 개인화된 구성을 사용할 때 이메일 콘텐츠를 미리 보며 정의한 동적 설정 사용 시 오류 가능성이 있는지 확인할 수 있습니다. [자세히 알아보기](../email/surface-personalization.md#check-configuration)

**코드 기반 채널**

* 이제 콘텐츠 템플릿을 사용할 수 있습니다. 개발자가 작성한 콘텐츠 템플릿에서 시작하여 코드 기반 경험을 빠르게 작성할 수 있습니다. 콘텐츠 템플릿을 사용하면 마케터가 전체 HTML 또는 JSON 콘텐츠 페이로드를 작성할 필요 없이 일부 값 또는 필드만 수정할 수 있습니다. [자세히 알아보기](../content-management/content-templates.md)

**의사 결정**

* [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=ko) 사용자는 이제 의사 결정(이전 이름: 경험 결정)에서 AI 모델을 설정할 때 최적화할 사용자 정의 모델을 선택할 수 있습니다. 예를 들어 클릭스루 비율과 같은 정의된 제한 대신 사용자 정의 &quot;구매&quot; 테이블을 기반으로 최적화할 수 있습니다. [자세히 알아보기](../experience-decisioning/ranking/ranking.md)

* 이제 의사 결정을 사용하여 코드 기반 캠페인에 결정 정책을 추가할 때 선택 전략에 더해 단일 결정 항목을 수동으로 선택할 수 있습니다. 또한 이제 두 개 이상의 대체 오퍼를 선택하는 것도 가능합니다. 이 방법으로 일정 수의 결정 항목이 반환되도록 보장할 수 있습니다. [자세히 알아보기](../experience-decisioning/create-decision.md)



## 24년 9월 릴리스 {#24-9-rn}

<!--
>[!CAUTION]
>
>**Early release notes below are subject to change without prior notice until the release date**. Links, screens and updated documentation are published at the release date.
>
-->

**릴리스 일자**: 2024년 9월 24~25일

### 새로운 기능 {#24-9-features}

이번 릴리스에는 아래에 있는 새로운 기능이 제공됩니다.

<table>
<thead>
<tr>
<th><strong>모바일 앱 및 웹 사이트용 콘텐츠 카드</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>콘텐츠 카드는 모바일 앱 및 웹 사이트에서 직접 개인화되고 흥미로운 콘텐츠를 제공하는 Adobe Journey Optimizer의 새로운 디지털 메시징 기능입니다. 기존 푸시 알림과 달리 콘텐츠 카드는 사용자 인터페이스에 원활하게 통합되어 사용자 상호 작용과 경험을 향상시키고 방해하지 않는 지속적인 업데이트를 제공합니다.</p>
<p>이 기능을 통해 마케터는 사용자에게 관련성이 높은 리치 미디어 콘텐츠를 제공할 수 있으므로 참여도가 높아지고 사용자 여정을 중단하지 않고도 중요한 메시지를 볼 수 있습니다.</p>
<p>자세한 내용은 <a href="../../rp_landing_pages/content-card-landing-page.md">세부 설명서</a>를 참조하십시오.</p>
<img src="assets/do-not-localize/content-card.gif"/>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>여정 및 캠페인의 승인(LA)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 승인 정책을 사용하여 Journey Optimizer 내 승인 프로세스를 설정할 수 있습니다. 이를 통해 마케팅 팀에서 캠페인 및 여정을 라이브로 전환하기 전에 적절한 이해 관계자의 검토 및 승인을 놓치지 않을 수 있습니다.</p>
<p>승인 정책은 현재 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.</p>
<p>자세한 내용은 <a href="../test-approve/gs-approval.md">세부 설명서</a>를 참조하십시오.</p>
<img src="assets/do-not-localize/approval.gif"/>
</td>
</tr>
</tbody>
</table>

<!--<table>
<thead>
<tr>
<th><strong>Email Content Locking</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer now allows you to lock content in email templates, either by locking the entire template or specific structures and component. This allows you to prevent unintentional edits or deletions, giving you greater control over template customization, and improving the efficiency and reliability of your email campaigns.</p>
<p>For more information, refer to the <a href="../content-management/gs-generative.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/gif-content-locking.gif">
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>여정의 전역 종료 기준</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 여정 수준에서 종료 기준을 정의합니다. 종료 기준을 추가하면 이벤트가 발생(예: 구매)하거나 프로필이 대상자 자격에 해당하는 즉시 해당 프로필의 여정을 종료합니다. 그러면 해당 사용자가 더 이상 해당 여정의 커뮤니케이션을 받지 않게 됩니다.</p>
<p>자세한 내용은 <a href="../building-journeys/journey-properties.md#exit-criteria">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>AI 어시스턴트</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>메시지를 만들고 개인화한 후에는 Journey Optimizer의 AI 어시스턴트로 콘텐츠를 한 단계 더 발전시킬 수 있습니다. 이제 Al 어시스턴트를 사용하여 다양한 주요 제목과 이미지를 실험해 보며 메시지의 영향을 최적화할 수 있습니다. 각 변형 버전이 고유한 처리 항목으로 관리되어 어떤 제목이 더 많은 클릭으로 이어지는지 측정하고 비교할 수 있습니다.</p>
<p>기능을 직접 탐색하고 기능을 완전히 이해할 수 있도록 설계된 <a href="https://experienceleague.adobe.com/ko/apps/journey-optimizer/ai-assistant-content-accelerator">라이브 기능 미리 보기</a>를 통해 실습 경험에 몰입하세요.</a>.</p>
<p>자세한 내용은 <a href="../content-management/gs-generative.md">세부 설명서</a>를 참조하십시오.</p>
<img src="assets/do-not-localize/ai-content.gif"/>
<p>사용 가능한 날짜: 2024년 9월 12일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>안내식 채널 설정</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>[안내식 채널 설정]을 사용하면 통합 환경에서 채널 설정을 자동화하고 유효성을 검사하여 Journey Optimizer를 보다 빠르게 시작할 수 있습니다. 이 새로운 안내식 설정으로 빠른 채널 구성을 간소화하여 필요한 리소스를 모두 손쉽게 설치하고 Experience Platform, Journey Optimizer, 데이터 수집 내에서 사용할 수 있습니다. 이를 통해 마케팅, 제품, 데이터 엔지니어링 팀이 캠페인 및 여정 만들기를 신속하게 시작할 수 있습니다.</p>
<p>자세한 내용은 <a href="../configuration/set-mobile-config.md">세부 설명서</a>를 참조하십시오.</p>
<img src="assets/do-not-localize/guided-setup.gif"/>
<p>사용 가능한 날짜: 2024년 9월 3일</p>
</br>
</td>
</tr>
</tbody>
</table>


### 개선 사항 {#24-9-improvements}

이 릴리스는 아래 목록에 있는 개선 사항과 함께 제공됩니다.

**대상저** - 사용 가능한 날짜: 2024년 9월 17일

**라이선스 사용** - 이제 라이선스 사용 대시보드에 참여 가능한 대상자 대신 참여 가능한 프로필이 표시됩니다. [자세히 알아보기](../audience/license-usage.md)

**콘텐츠 관리**

이제 샌드박스 간에 콘텐츠 템플릿과 조각을 내보낼 수 있습니다. [자세히 보기](../configuration/copy-objects-to-sandbox.md)

**여정**

* **실시간 보고 개선** - 실시간 보고에서는 지난 24시간 동안의 여정 성과에 대한 인사이트를 제공합니다. 새로운 지표(입장함, 퇴장함, 삭제 프로필, 오류 프로필)를 추가하여 여정 캔버스에서 직접 사용자 동작 및 성과를 더 깊이 있게 이해할 수 있도록 개선했습니다. [자세히 알아보기](../building-journeys/report-journey.md)


* (사용 가능한 날짜: 9월 10일) **대상자 읽기 자동 재시도** -이제 내보내기 작업을 검색하는 동안 대상자에 의해 트리거되는 여정(**대상자 읽기** 또는 **비즈니스 이벤트**&#x200B;로 시작)에 대해 기본적으로 재시도를 적용합니다. 내보내기 작업 생성 중 오류가 발생하면 최대 1시간 동안 10분마다 다시 시도됩니다. 그 후에는 실패로 간주합니다. 따라서 이러한 유형의 여정은 예정된 시간보다 최대 1시간 후에 실행될 수 있습니다. [자세히 알아보기](../building-journeys/read-audience.md#retries)

**이메일 채널**

* **보낸 이메일 및 BCC 사본의 메시지 헤더** - 모든 이메일 메시지에 새 헤더가 추가되었습니다. 이 헤더는 보낸 각 이메일과 해당 BCC 이메일 사본에 대해 고유한 값을 가집니다. 이 헤더는 메시지 및 BCC 피드백 데이터 세트에도 저장되며, 이를 통해 BCC 사본과 이에 해당하는 전송된 이메일 정보를 조정할 수 있습니다. [자세히 보기](../configuration/archiving-support.md#bcc-header)

* **스팸 점수**(GA) - 이제 전용 **스팸 보고서**&#x200B;를 통해 콘텐츠 스팸 점수를 확인할 수 있습니다. 이제 Adobe Journey Optimizer에서 SpamAssassin을 사용하여 이메일 콘텐츠를 테스트하고 ISP 또는 사서함 공급자가 이를 스팸으로 간주할지 여부를 나타내는 점수를 매길 수 있습니다. [자세히 보기](../content-management/spam-report.md)

**SMS 채널**

* **API 자격 증명 편집** - 이제 SMS API 자격 증명의 옵트인/옵트아웃 키워드 업데이트 및 답장 등 설정을 편집할 수 있습니다.

**API**

* **캠페인 시뮬레이션 API** - 이 API를 사용하여 캠페인의 교정 작업을 트리거합니다. 캠페인 증명 보내기가 비동기 프로세스인 경우 이 API는 증명 상태를 확인하는 데 사용할 수 있는 proofJobId를 반환합니다. [자세히 알아보기](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target="_blank"}

* (가용성 일자: 9월 10일) [Adobe Journey Optimizer API 설명서](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target="_blank"}가 대화형으로 변경되었습니다. 설명서 페이지에서 직접 API 엔드포인트를 탐색하여 즉각적인 피드백을 얻고 기술 구현 속도를 높일 수 있습니다. 


  이제 모든 API 참조 페이지에는 설명서 웹 사이트 페이지에서 직접 API 호출을 테스트하는 데 사용할 수 있는 **사용해 보기** 기능이 있습니다. [필요한 인증 자격 증명을 얻고](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"} 이 기능을 사용하여 API 엔드포인트를 탐색하십시오.

  이 새로운 기능을 사용하여 API 엔드포인트에 대한 요청과 응답을 살펴보고 즉각적인 피드백을 받고 기술 구현 속도를 높일 수 있습니다.

  >[!CAUTION]
  >
  >설명서 페이지의 대화형 API 기능을 사용하면 엔드포인트에 실제 API 호출을 할 수 있다는 점에 유의하십시오. 프로덕션 샌드박스를 실험할 때는 이 점을 명심하십시오.

**구성**

* **IP 워밍업 플랜** - 이제 Adobe **Healthcare Shield** 또는 **Privacy and Security Shield** 추가 기능 서비스를 구입한 조직을 포함하여 모든 고객이 이 기능을 사용할 수 있습니다. [자세히 알아보기](../configuration/ip-warmup-gs.md)

<!--
![Newsletter](../assets/do-not-localize/nl-icon.png) Sign up for the [Adobe Journey Optimizer quarterly newsletter](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} today, and receive the latest product updates, exciting stories, use cases, tips and more delivered directly to your inbox every quarter.-->



## 24년 8월 릴리스 {#8-2024}

**릴리스 날짜**: 2024년 8월 20~21일

### 새로운 기능 {#8-features}

이번 릴리스에는 아래에 있는 새로운 기능이 제공됩니다.

<!--
<table>
<thead>
<tr>
<th><strong>Content Cards (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Content cards are a new digital messaging feature in Adobe Journey Optimizer that delivers personalized and engaging content directly within mobile apps and websites. Unlike traditional push notifications, Content Cards integrate seamlessly into the user interface, offering persistent, non-intrusive updates that enhance user interaction and experience.</p>
<p>This feature enables marketers to present relevant, rich media content to users, driving higher engagement and ensuring important messages are seen without disrupting the user journey.</p>
</br>
<p>Content card are currently only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>향상된 채널 구성</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>현재 채널 표면 기능은 모든 채널에서 일관된 접근 방식을 위해 향상되었습니다. 이제 [웹], [인앱 메시지] 또는 [코드 기반 경험]을 포함하여 모든 채널에 대해 구성을 정의, 관리, 재사용할 수 있습니다.</p>
<p><ul>
<li>이제 채널 표면 이름이 <strong>채널 구성</strong>으로 변경되었습니다.</li>
<li>동의 및 데이터 거버넌스 정책을 시행하기 위해 하나 이상의 마케팅 액션을 첨부할 수 있습니다.</li>
<li>이제 각 채널 구성에 OLAC(개체 수준 액세스 제어)를 사용할 수 있으므로 특정 구성을 만들거나 사용할 수 있는 사용자를 결정할 수 있습니다.</li>
<li>일부 채널의 경우 여러 플랫폼을 대상으로 하는 채널 구성을 만들 수 있습니다. 웹 페이지, iOS 앱 및 Android 앱을 타깃팅할 수 있는 인앱 메시지 채널 구성이 여기에 해당합니다.</li>
</ul></p>
<p>자세한 내용은 <a href="../configuration/channel-surfaces.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Marketo Engage 사용자 정의 작업</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Adobe Journey Optimizer를 Adobe Marketo Engage와 통합하여 B2B 사용 사례를 작성할 수 있습니다. 여정에서 새로운 사용자 정의 작업을 통해 데이터를 Marketo로 수집할 수 있습니다.</p>
<p>자세한 내용은 <a href="../action/marketo-engage.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>콘텐츠 조각의 변수</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>조각 전역 변수로 기존 조각 기능을 향상시켜 콘텐츠 재사용과 스크립팅 사용 사례의 효율성을 개선합니다. 이제 조각에서 입력 변수를 사용하고 캠페인 및 여정 콘텐츠에 사용할 수 있는 출력 변수를 만들 수 있습니다. 조각이 입력 변수를 <a href="../personalization/use-expression-fragments.md">표현식 조각</a> 및 <a href="../email/use-visual-fragments.md">시각적 조각</a> 모두에서 사용할 수 있습니다. 이러한 변수를 사용하여 캠페인 및 여정에서 메시지 콘텐츠 및 매개 변수를 개인화할 수 있습니다.</p>
<p>자세한 내용은 <a href="../personalization/use-expression-fragments.md">세부 설명서</a>를 참조하십시오.</p>
</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>IP 준비 워크플로</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>사용 가능한 날짜: 2013년 8월</p>
<p>완전히 새로운 IP 주소로 이메일을 보내는 경우 이제 사용자 인터페이스에서 직접 IP 준비 워크플로를 쉽게 수행할 수 있습니다. Adobe Journey Optimizer는 최적의 전달성을 위한 모범 사례에 따라 IP 주소를 준비하는 표준화되고 효율적인 방법을 제공합니다.</p>
<p>자세한 내용은 <a href="../configuration/ip-warmup-gs.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>

### 개선 사항 {#8-improvements}

이번 릴리스에는 아래 목록에 있는 개선 사항이 제공됩니다.

**여정**

* 이제 **조건** 활동에서 **[!UICONTROL 시간 조건]**&#x200B;은 기본적으로 00:00부터 12:00까지 시간 단위로 설정됩니다. [자세히 보기](../building-journeys/condition-activity.md#time_condition)
* 이제 여정을 작성할 때에도 경고가 다른 경고와 마찬가지로 **경고** 버튼에서 표시되어 일관된 사용자 경험을 제공합니다. [자세히 보기](../building-journeys/troubleshooting.md#checking-for-errors-before-testing)
* 여정 도구 모음의 확대/축소 옵션이 개선되었습니다. 이제 확대/축소 비율이 표시되며 확대/축소 값을 보다 쉽게 재설정할 수 있습니다.

**푸시 채널**

* 이제 Adobe Journey Optimizer 채널 구성 설정 내에 모바일 애플리케이션 푸시 자격 증명을 추가할 수 있습니다. 더 이상 Adobe Experience Platform 데이터 수집에서 앱 표면을 만들 필요가 없습니다.

### 기타 변경 사항 {#changes}

**보고**

* 새로운 보고 경험에 다음과 같이 새로운 사용 사례가 추가되었습니다.

   * 보고서 내에서 직접 사용자 정의한 계산된 지표를 만듭니다.
   * 보고 데이터를 사용하여 대상자를 만듭니다.
   * [탐색적 분석] 도구를 사용하여 선택한 **[!UICONTROL 차원]** 및 **[!UICONTROL 지표]**&#x200B;로 손쉽게 테이블과 시각화 자료를 만듭니다.

  자세한 내용은 [세부 설명서](../reports/report-cja-manage.md)를 참조하십시오.



## 24년 7월 릴리스 {#24-7-2024}

**릴리스 일자**: 2024년 7월 30~31일

### 새로운 기능 {#27-4-features}

이번 릴리스에는 아래 목록에 있는 새로운 기능이 제공됩니다.

<table>
<thead>
<tr>
<th><strong>모든 공급자의 SMS 채널(Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer 내에서 기본 공급자인 Sinch, Infobip, Twilio 외 추가 SMS 공급자를 구성할 수 있습니다.</p>
<img src="assets/do-not-localize/byo_sms.gif"/>
<p>자세한 내용은 <a href="../sms/sms-configuration-custom.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>페더레이션된 대상자 컴포지션(제한된 가용성)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Adobe Journey Optimizer에서 [페더레이션된 대상자 컴포지션]을 사용할 수 있습니다. 이 기능으로 기업이 다양한 사용 사례에서 데이터를 더 잘 활용할 수 있습니다. 이 새로운 접근 방식을 사용하면 Adobe Real-Time Customer Data Platform 및/또는 Adobe Journey Optimizer 사용자로서 기존 데이터 웨어하우스에서 직접 데이터 세트를 페더레이션하여 Adobe Experience Platform 대상자와 속성을 모두 하나의 시스템에 작성하고 강화할 수 있습니다.</p>
<p>자세한 내용은 <a href="https://experienceleague.adobe.com/ko/docs/federated-audience-composition/using/home"  target="_blank">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>

### 개선 사항 {#27-4-improvements}

이 릴리스는 아래 목록에 있는 개선 사항과 함께 제공됩니다.

**여정**

* (공개일: 7월 8일)**여정 이벤트 구성의 고급 표현식 편집기** - 이제 이벤트를 구성할 때 고급 표현식 편집기를 활용하여 이벤트 ID 조건에 보다 복잡한 표현식을 정의하거나 함수를 사용할 수 있습니다. [자세히 알아보기](../event/about-creating.md#adv-exp-editor)



## 24년 6월 릴리스 {#24-6-2024}

**릴리스 날짜**: 2024년 6월 18~19일

### 새로운 기능 {#june-24-features}

이번 릴리스에는 아래에 있는 새로운 기능이 제공됩니다.

<table>
<thead>
<tr>
<th><strong>콘텐츠 조각 사용자 정의</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 캠페인 또는 여정에 조각을 추가할 때 해당 조각에서 편집할 수 있는 특정 필드를 정의할 수 있습니다. 이를 통해 콘텐츠의 일부분을 사용 시 조정할 수 있으므로 유연하게 맥락에 따라 달라지는 세부 사항을 기본값 대신 사용할 수 있습니다.</p>
<img src="../content-management/assets/do-not-localize/gif-fragments.gif"/>
<p>자세한 내용은 <a href="../content-management/customizable-fragments.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Customer Journey Analytics를 사용한 보고(제한된 가용성)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer의 보고 기능은 Customer Journey Analytics 기능의 개선된 상호 운용성과 함께 양 플랫폼의 보고를 표준화하고 데이터의 일관성과 안정성을 개선합니다. 이렇게 Journey Optimizer와 Customer Journey Analytics가 원활하게 통합됨으로써 사용자가 성과 지표를 보다 명확하게 확인하여 확실한 정보에 근거한 결정을 내릴 수 있습니다.</p>
<img src="assets/do-not-localize/ajo-cja.gif"/>
<p>자세한 내용은 <a href="../reports/report-gs-cja.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Adobe Journey Optimizer의 AI 어시스턴트</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>AI 어시스턴트는 Adobe의 개념을 탐색 및 이해하고 사용자의 환경에 적절한 작업 인사이트를 얻는 데 사용할 수 있는 사용자 인터페이스 기능입니다. Adobe Journey Optimizer를 비롯한 Adobe Experience Cloud 전체의 여러 제품에서 사용할 수 있습니다.</p>
<p>자세한 내용은 <a href="../start/ai-assistant.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>여정 및 캠페인의 다국어 메시지(제한된 가용성)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 단일 캠페인 또는 여정 내에서 간편하게 여러 언어로 콘텐츠를 만들 수 있습니다. 이 기능을 사용하면 캠페인이나 여정을 편집할 때 언어를 전환할 수 있으므로 전체 편집 프로세스를 간소화하고 다국어 콘텐츠를 더욱 효율적으로 관리할 수 있습니다.</p>
<p>다국어 콘텐츠는 현재 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>여정 내 실험(제한된 가용성)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer가 이제 여정에서도 실험을 지원합니다. 캠페인에서는 이미 실험을 사용할 수 있습니다. 실험은 무작위화한 시험 회기 여러 개를 모아 놓은 것입니다. 온라인 테스팅 맥락에서는 무작위로 선택한 사용자 일부를 특정한 버전의 메시지에 노출하고, 무작위로 선택한 다른 사용자들을 다른 처리 버전에 노출하는 것을 말합니다. 노출 후에는 이메일 열람, 구독 또는 구매 등 궁금한 결과 지표를 측정할 수 있습니다.</p>
<p>여정 내 실험은 현재 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Extended personalization data - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now lookup and fetch data values within Adobe Experience Platform datasets, and use these values to build conditions in Adobe Journey Optimizer. You can leverage data from a lookup dataset when a relationship has been defined using an attribute inside of an array of objects. You can specify non-profile enabled datasets for lookup. Once enabled, you can use a profile attribute as a join key to the specified dataset to retrive further data for personalization.</p>
<p>This capability is currently available as a public beta.</p>
</td>
</tr>
</tbody>
</table-->

### 개선 사항 {#june24-improvements}

이 릴리스는 아래 목록에 있는 개선 사항과 함께 제공됩니다.

#### 의사 결정 관리

* **의사 결정 관리의 다중 규칙 지원** - 이제 의사 결정 관리에서 주어진 오퍼에 대해 최대 10개의 캡핑 규칙을 추가할 수 있습니다. 이를 통해 오퍼를 전송하는 방식에 대한 제어 수준을 향상시킬 수 있습니다. [자세히 알아보기](../offers/offer-library/add-constraints.md#capping)

<!--* **Audits** - The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu. -->

#### 콘텐츠 조각

>[!AVAILABILITY]
>
>단, 이러한 개선 사항은 초기 릴리스 후 며칠에 걸쳐 점진적으로 적용됩니다. 일부 사용자는 즉시 액세스할 수 있지만, 일부 사용자는 자신의 환경에서 사용할 수 있게 될 때까지 지연될 수 있습니다.

* 이제 조각을 편집할 수 있으며 변경 사항을 해당 조각이 사용되는 모든 라이브 여정 및 캠페인에 전파할 수 있습니다.
* 콘텐츠 조각에 대해 상태 설정이 새로 도입되었습니다. **초안**, **라이브**, **게시 중**, **보관됨** 상태를 설정할 수 있습니다.
* 이제 여정 또는 캠페인에서 조각을 사용하려면 해당 조각이 **라이브** 상태여야 합니다. 조각을 만드는 프로세스에 새로운 단계를 추가하여 조각을 게시하고 여정 및 캠페인에서 사용할 수 있도록 했습니다. 단, 조각을 게시하려면 새로운 권한이 필요합니다.

  **주의** - **초안** 및 **라이브** 상태는 Journey Optimizer 6월 릴리스에서 도입되었으므로 이 릴리스 이전에 만든 모든 조각은 여정 또는 캠페인에서 사용되더라도 **초안** 상태입니다. 이 조각을 변경할 경우 [해당 조각을 게시](../content-management/create-fragments.md#publish)하여 “라이브”로 만들고 관련 캠페인 및 여정에 변경 사항을 전파해야 합니다. 또한 여정/캠페인 버전을 새로 만들어 게시해야 합니다. 

자세한 내용은 [콘텐츠 조각](../content-management/fragments.md) 설명서를 참조하십시오.

#### 여정

* 여정의 전역 시간 제한이 91일로 연장되었습니다. [자세히 보기](../building-journeys/journey-properties.md#global_timeout)

  새로 만드는 모든 여정에 이 새로운 시간 제한이 반영됩니다. 자세한 내용은 이 [FAQ 섹션](../building-journeys/journey-properties.md#timeout-faq)을 참조하십시오. 단, 이 변경 사항은 6월 한 달 동안 점진적으로 적용될 예정입니다.


* Adobe Journey Optimizer가 이제 데이터 수명 주기 관리 요청뿐만 아니라 개인 정보 삭제/액세스 요청도 지원합니다. [자세히 보기](../privacy/requests.md)
* 이제 여정 인벤토리에서 열의 크기를 조정할 수 있습니다.
  <!--* **Advanced expression editor in Event configuration** is now GA - You can now leverage the advanced expression editor while configuring an event, allowing you to define more complex expressions or use functions in the event id condition. This capability is released in Limited Availability for selected customers. [Read more](../event/about-creating.md)-->
* **병합 정책** GA 변경 - 여정에서 사용하는 병합 정책이 이제 여정 전체에서 일관적이며 직접 볼 수 있습니다. [자세히 보기](../building-journeys/journey-properties.md#merge-policies)


#### 캠페인

* 이제 Adobe Journey Optimizer에서 캠페인을 만들 때 새로운 모달에서 캠페인 유형(예약됨 또는 트리거됨)을 선택할 수 있습니다. [자세히 보기](../campaigns/create-campaign.md)

#### 이메일 채널

* **목록 구독 취소** - 대량 발신자에 대한 최근 Gmail 및 Yahoo의 공지에 따라 Journey Optimizer는 “게시/원클릭” 목록 구독 취소 옵션을 지원합니다. [이메일 옵트아웃 관리](../email/email-opt-out.md#unsubscribe-header) 및 [이메일 설정 구성](../email/email-settings.md#list-unsubscribe) 페이지를 참조하십시오.

  **참고** - 새로 만든 채널 표면의 경우 기본적으로 목록 구독 취소 헤더 옵션이 활성화되어 있습니다. 기존 표면의 경우 기본적으로 채널 표면 설정의 [원클릭 구독 취소 URL] 옵션이 선택되어 있지 않습니다. 이전에 이메일 본문에서 원클릭 옵트아웃 URL을 사용하고 있었던 경우 해당 설정은 여전히 유효합니다. 채널 표면 설정에서 [원클릭 구독 취소 URL]을 선택한 경우 Adobe Journey Optimizer는 채널 표면 설정에서 생성된 기본 [원클릭 구독 취소 URL]을 사용합니다.

#### SMS 채널

* 이제 한 번의 API 구성으로 각 샌드박스마다 고유한 짧은 코드를 추가할 수 있어 프로세스가 효율화, 간소화됩니다. [자세히 알아보기](../sms/sms-configuration.md)

* 이제 **API 자격 증명 세부 정보** 페이지의 **API 토큰** 필드가 토큰을 만든 후 마스킹됩니다.

<!--* You can now modify existing SMS configurations.-->

#### 인앱 채널

<!--* **Expression fragment** - Expression fragments are now available for the **In-app channel**. [Read more](../personalization/use-expression-fragments.md)-->

* 이제 Edge Delivery 플러그인을 사용하여 인바운드 구현을 이해하고 문제를 해결하는 데 필요한 정보를 얻을 수 있습니다. [Edge Delivery 보기에 대해 자세히 알아봅니다](https://experienceleague.adobe.com/ko/docs/experience-platform/assurance/view/edge-delivery){target="_blank"}.


#### DM 채널

* 이제 모든 고객이 다이렉트 메일 채널을 사용할 수 있습니다. [자세히 보기](../direct-mail/get-started-direct-mail.md)



## 24년 5월 릴리스 {#may-2024}

**릴리스 날짜**: 2024년 5월 21~22일

### 새로운 기능 {#e-features}

이번 릴리스에는 아래에 있는 새로운 기능이 제공됩니다.

<table>
<thead>
<tr>
<th><strong>Experience Decisioning - 제한된 가용성</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Experience Decisioning은 '의사 결정 항목'으로 알려진 마케팅 의 중앙 집중식 카탈로그와 정교한 의사 결정 엔진을 제공하여 개인화를 간소화합니다. 이 엔진은 규칙과 순위 기준을 활용하여 각 개인에게 가장 관련성 높은 의사 결정 항목을 선택하고 제공합니다.</p>
<p>이 의사 결정 항목은 이제 Journey Optimizer 캠페인에서 액세스할 수 있는 새로운 코드 기반 경험 채널을 통해 광범위한 인바운드 구성에 원활하게 통합됩니다. 경험 결정 의사 결정 정책은 코드 기반 경험 캠페인에서만 사용할 수 있습니다.</p>
<p>SMS 채널은 현재 조직 집합(제한된 가용성)에만 사용할 수 있습니다. 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.</p>
<img src="assets/do-not-localize/gif-exd.gif"/>
<p>자세한 내용은 <a href="../experience-decisioning/gs-experience-decisioning.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>이메일 구성 개인화 - 제한된 가용성</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 이메일 채널 구성을 만들 때 동적 하위 도메인과 개인화된 헤더 매개 변수를 정의하여 이메일 설정을 더욱 유연하게 제어할 수 있습니다.</p>
<p>이메일 구성 개인화는 현재 일부 조직 집합에만 사용할 수 있습니다(제한된 가용성). 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.</p>
<p>자세한 내용은 <a href="../email/surface-personalization.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>IP Warmup Workflow</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>If you are sending email on a brand new IP address, you can now easily perform IP warmup workflows directly from the user interface. Adobe Journey Optimizer offers a standardized and efficient way to warm up your IP adresses that follows the best practices for optimal deliverability.</p>
<p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Business rules - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create granular frequency capping rules, and apply them to different types of marketing communications through rule sets. This new capability lets you control how often your audiences receive a message by setting cross-channel rules, that automatically exclude over-solicited profiles from messages and actions.</p>
<p>Business rules capability is currently available as a beta. To join the beta program, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Extended personalization data - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now lookup and fetch data values within Adobe Experience Platform datasets, and use these values to build conditions in Adobe Journey Optimizer. You can leverage data from a lookup dataset when a relationship has been defined using an attribute inside of an array of objects. You can specify non-profile enabled datasets for lookup. Once enabled, you can use a profile attribute as a join key to the specified dataset to retrive further data for personalization.</p>
<p>This capability is currently available as a public beta.</p>
</td>
</tr>
</tbody>
</table-->

### 개선 사항 {#e-improvements}

이 릴리스는 아래 목록에 있는 개선 사항과 함께 제공됩니다.

**경험 결정**(제한된 가용성)

Beta부터 이 릴리스까지 다음과 같은 개선 사항이 추가되었습니다.

* **경험 결정+코드 기반 경험(LA)**: 이제 경험 결정 기능을 활용하여 코드 기반 캠페인에서 의사 결정 항목을 사용할 수 있습니다. 참고: Adobe Healthcare Shield 및 Privacy and Security Shield 추가 기능을 구매한 조직에서는 코드 기반 경험 채널 및 경험 결정을 사용할 수 없습니다. [자세히 보기](../code-based/get-started-code-based.md)
* **컨텍스트 데이터** - 이제 의사 결정 규칙 및 등급 수식에서 Adobe Experience Platform의 컨텍스트 데이터를 활용할 수 있습니다. [자세히 보기](../experience-decisioning/context-data.md)
* **새로운 권한** - 이제 의사 결정 관리 리소스에 대해 새로운 ‘경험 결정 관리’ 권한을 사용할 수 있습니다. 이를 통해 경험 결정과 관련된 권한을 관리할 수 있습니다. [자세히 보기](../experience-decisioning/gs-experience-decisioning.md)
* **캡핑 규칙** - 이제 경험 결정에서 지정된 의사 결정 항목에 대해 여러 개의 캡핑 규칙을 추가할 수 있습니다. 이를 통해 오퍼를 전송하는 방식에 대한 제어 수준을 향상시킬 수 있습니다. [자세히 보기](../experience-decisioning/items.md#capping)
* **보고** - 이제 [!DNL Customer Journey Analytics]를 사용하여 경험 결정 캠페인의 사용자 정의 보고 대시보드를 만들 수 있습니다. [자세히 보기](../experience-decisioning/cja-reporting.md)


<!--**Decision Management**

* **Multi-rule support** - You can now add up to 10 capping rules for a given offer in Decision Management. This allows you to increase the level of control over the way offers are sent.
* **Audits** - The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu. -->


**이메일 채널**

<!--
* **List-unsubscribe** - Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. Refer to the following pages: [Email opt-out management](../email/email-opt-out.md#unsubscribe-header) and [Configure email settings](../email/email-settings.md#list-unsubscribe)
-->

* **스팸 점수**(Beta) - 이제 전용 스팸 보고서에서 콘텐츠 스팸 점수를 확인할 수 있습니다. 이제 Adobe Journey Optimizer에서 SpamAssassin을 사용하여 이메일 콘텐츠를 테스트하고 ISP 또는 사서함 공급자가 이를 스팸으로 간주할지 여부를 나타내는 점수를 매길 수 있습니다. [자세히 보기](../content-management/spam-report.md)

  >[!AVAILABILITY]
  >
  >이 기능은 현재 Beta 버전으로 Beta 고객에게만 제공됩니다. Beta 프로그램에 참여하려면 Adobe 담당자에게 문의하십시오.

<!--
**Audiences**

* The use of audiences and attributes from audience composition and custom upload (CSV file) is now available for use with Healthcare Shield or Privacy and Security Shield.-->

<!--**Personalization**

* **Expression fragment** - Expression fragments are now available for the **In-app channel**. [Read more](../personalization/use-expression-fragments.md)-->

**여정**

<!--* **Merge policies** (Limited Availability)- Merge policies used by a journey are now visible and consistent throughout the journey.-->
* **mTLS 지원** - 이제 사용자 정의 작업에 mTLS 인증이 지원됩니다. mTLS를 활성화하기 위해 사용자 정의 작업 또는 여정에 구성을 추가할 필요는 없습니다. mTLS 활성화 엔드포인트가 감지되면 자동으로 활성화됩니다. [자세히 보기](../action/about-custom-action-configuration.md#mtls-protocol-support)
* **이벤트의 조회 테이블** - 이제 개체 배열 내의 속성을 사용하여 관계를 정의한 경우 조회 데이터 세트의 데이터를 활용할 수 있습니다. 조회 값을 여정(조건, 사용자 정의 작업 등) 및 메시지 개인화에서 사용할 수 있습니다. [자세히 보기](../event/experience-event-schema.md#relationships_limitations)
* **이벤트 구성의 고급 표현식 편집기**(LA) - 이제 이벤트를 구성할 때 고급 표현식 편집기를 활용하여 이벤트 ID 조건에 보다 복잡한 표현식을 정의하거나 함수를 사용할 수 있습니다. 이 기능은 일부 고객 대상 제한된 가용성으로 릴리스됩니다. [자세히 보기](../event/about-creating.md#adv-exp-editor)
* **병합 정책**(LA) - 여정에서 사용하는 병합 정책이 이제 여정 전체에서 일관적이며 직접 볼 수 있습니다. 이 기능은 일부 고객 대상 제한된 가용성으로 릴리스됩니다. [자세히 보기](../building-journeys/journey-properties.md#merge-policies)

**세계화**

통일성 있는 사용자 경험을 제공하기 위한 지속적인 노력의 일환으로 Adobe Experience Cloud 제품 및 앱에서 사용되는 용어를 서로 맞추는 작업을 합니다. 이에 따라 독일어 서비스에서 “Titel”이라는 용어가 개체와 관련된 상황의 경우 “Label”로 변경됩니다. 이 변경 사항은 UI 및 설명서에 점진적으로 적용됩니다.


## 24년 4월 릴리스 {#apr-2024}

**릴리스 일자**: 2024년 5월 2일

### 새로운 기능 {#apr-features}

이번 릴리스에는 아래에 있는 새로운 기능이 제공됩니다.

<table>
<thead>
<tr>
<th><strong>MMS(멀티미디어 메시지 서비스) - 모든 공급자</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 [SMS 채널]을 통해 MMS(멀티미디어 메시지 서비스) 메시지를 보내 고객과 이미지, GIF 또는 비디오를 공유하는 기능이 추가되어 커뮤니케이션을 더욱 원활하게 진행할 수 있습니다. 이전에는 Sinch에서만 사용할 수 있었지만, 이제 MMS는 Infobip 및 Twilio에서도 사용할 수 있습니다.</p>
<img src="assets/do-not-localize/mms.gif"/>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>향상된 여정 디자이너 및 라이브 보고</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이번 릴리스는 여정을 위한 캔버스 사용자 인터페이스가 개선되어 보다 직관적이고 효율적인 사용자 경험을 제공합니다. 활동은 더 적은 클릭 수로 여정 캔버스에 더 명확하고 많은 정보를 제공합니다.</p>
<img src="assets/new-canvas3.gif"/>
<p>향상된 여정 캔버스 디자인과 함께 지난 24시간 보고 지표를 여정 캔버스에서 직접 볼 수 있는 기능을 도입했습니다. </p>
<img src="assets/new-canvas6bis.png"/>
<p><strong>참고</strong>: 이러한 변경 사항은 4월 릴리스부터 모든 환경으로 점진적으로 롤아웃됩니다.</p>
<p>자세한 내용은 <a href="new-canvas.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>

<!-- table>
<thead>
<tr>
<th><strong>AI Assistant - Experience Variant Generation - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Once you have created and personalized your message, take your content to the next level with AI Assistant. You can now use AI Assistant to optimize your message's impact by experimenting with different main titles, and images. Each variant is managed as a unique Treatment, to measure and compare which title effectively generates more clicks.</p>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Email Surface Personalization - Private beta </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now define dynamic subdomains and personalized header parameters when creating email channel configurations, for increased flexibility and control over your email settings.</p>
</td>
</tr>
</tbody>
</table-->

### 개선 사항 {#apr-improvements}

이 릴리스는 아래 목록에 있는 개선 사항과 함께 제공됩니다.

<!--
* **Expression Fragments supported for Web and In-App**: Expression fragments are now available for the Web and In-app channels. 
-->


<!--
* **DULE for AJO channel configuration**: It is now possible to apply a label on certain profile attributes to restrict their usage inside a channel configuration through marketing actions.
-->


<!--
* **List-Unsubscribe updates**: Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. 
-->

**구성**

* 이제 채널 구성 수준에서 마케팅 액션을 선택할 수 있습니다. 구성에서 사용할 경우 고객의 환경 설정을 존중하기 위해 해당 마케팅 액션과 관련된 모든 동의 정책을 활용합니다. [자세히 보기](../action/consent.md#surface-marketing-actions)
* 이제 채널 구성에 대해 오브젝트 수준 액세스 컨트롤을 사용할 수 있습니다. [자세히 보기](../configuration/channel-surfaces.md#create-channel-surface)
* 이제 채널 구성에서 목록 구독 취소를 활성화하면서 다른 모든 소스의 동의를 관리하는 방식에 맞게 동의 수준을 정의할 수 있습니다. [자세히 보기](../email/email-settings.md#list-unsubscribe)

**콘텐츠 관리**

* 이제 모든 채널에 대한 콘텐츠 템플릿을 시뮬레이션할 수 있습니다. [자세히 보기](../content-management/content-templates.md#test-templates)

**개인화**

* 새로운 **toInt** 헬퍼 함수는 표현식 편집기에서 사용할 수 있습니다. 이 옵션을 사용하면 이러한 유형(number, double, int, long, float, short, byte, boolean, string) 중 하나를 정수로 전환할 수 있습니다. [자세히 보기](../personalization/functions/math.md#to-int)



## 24년 3월 릴리스 {#mar-2024}

**릴리스 날짜**: 2024년 3월 19~20일

### 새로운 기능 {#mar-features}

이번 릴리스에서 제공하는 새로운 기능을 아래에서 자세히 설명합니다.

<table>
<thead>
<tr>
<th><strong>코드 기반 경험</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>새로운 [코드 기반 경험] 채널로 Adobe Journey Optimizer에서 원하는 인바운드 속성에 대해 고급 개인화 및 테스트를 수행할 수 있으므로 웹 앱, 모바일 앱, 데스크탑 앱, 비디오 콘솔, TV에 연결된 디바이스, 스마트 TV, 키오스크, ATM, IoT 디바이스 등과 같은 다양한 접점에서 맞춤형 경험을 원활하게 전달할 수 있습니다.</p>
<P>주요 기능은 다음을 포함합니다.</p>
<ul><li> 범용 개인화: 개인화된 경험을 모든 접점으로 확장하여 통합적이고 맞춤화된 사용자 여정을 보장합니다.</li>
<li>세분화된 편집 정밀도: 앱 또는 웹 페이지 내의 개별 위치에서 있는 특정 콘텐츠를 편집할 수 있습니다.</li>
<li>다목적 구현: 개발 환경과 원활하게 통합할 수 있도록 서버측, API 기반 또는 SDK 기반 구현 방법을 지원합니다.</li></ul></p>
<p>자세한 내용은 <a href="../code-based/get-started-code-based.md">세부 설명서</a>를 참조하십시오.</p>
<img src="assets/do-not-localize/code-based.gif"> 
</tr>
</tbody>
</table>

### 개선 사항 {#mar-improvements}

이 릴리스는 아래 목록에 있는 개선 사항과 함께 제공됩니다.

**콘텐츠 템플릿**

* **썸네일** - 이제 콘텐츠 템플릿을 시각적 접근성을 개선하기 위해 썸네일을 표시하는 **그리드 보기** 모드로 볼 수 있습니다. 현재는 이메일 HTML 템플릿만 지원됩니다. [자세히 알아보기](../content-management/content-templates.md#template-thumbnails)

  >[!AVAILABILITY]
  >
  >이 기능은 소규모 고객을 위해 LA(Limited Availability)에서 출시됩니다.

**여정**

여정 작성 라이프사이클에 새로운 중간 상태가 추가되었습니다.

* **초안** 상태와 **라이브** 상태 사이의 **게시 중** 상태
* **라이브** 상태와 **정지됨** 상태 사이의 **멈추는 중** 상태
* **초안** 상태와 **초안(테스트)** 상태 사이의 **테스트 모드 활성화 중** 또는 **테스트 모드 비활성화 중** 

여정이 중간 상태일 때는 읽기 전용입니다. [자세히 알아보기](../building-journeys/journey-gs.md#filter)

## 24년 2월 릴리스 {#feb-2024}

**릴리스 날짜**: 2024년 2월 21~22일

### 새로운 기능{#feb-features}

이번 릴리스에는 아래 목록에 있는 새로운 기능이 제공됩니다.


<table>
<thead>
<tr>
<th><strong>웹 인앱 메시지</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 새로운 웹 인앱 메시지 기능을 사용하면 모달 오버레이 메시지를 통해 웹 사이트에 직접 개인화된 콘텐츠를 표시할 수 있습니다. 이 기능을 사용하면 웹 방문자와 효과적으로 상호 작용하여 사용자 상호 작용, 보존 및 전환율을 향상할 수 있습니다.<br/><br/></p>
<p>자세한 내용은 <a href="../in-app/create-in-app-web.md">세부 설명서</a>를 참조하십시오.<br></br></p>
<img src="assets/do-not-localize/web_inapp.gif">
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>다중 채널 콘텐츠 템플릿</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 이메일 외에도 푸시, 인앱, SMS 및 DM 채널에 콘텐츠 템플릿을 사용할 수 있습니다. 각 채널에는 전용 템플릿 유형이 있습니다. 이메일의 경우 이제 제목 줄을 이메일 템플릿의 일부로 저장할 수 있는 콘텐츠 유형을 선택할 수 있습니다. <br/><br/></p>
<p>자세한 내용은 <a href="../content-management/content-templates.md">세부 설명서</a>를 참조하십시오.<br></br></p>
<img src="assets/do-not-localize/multi-chan-templates.gif"> 
</tr>
</tbody>
</table>


### 개선 사항 {#feb-improvements}

이 릴리스는 아래 목록에 있는 개선 사항과 함께 제공됩니다.

**대상자**

* **시드 목록** - 이제 **시드 목록**&#x200B;을 사용할 때 변형이 지원됩니다. 시드 주소는 동일한 메시지의 모든 변형(예: 콘텐츠 실험의 다양한 처리) 사본을 받습니다. [자세히 보기](../configuration/seed-lists.md)

이전에 Beta로 제공되었던 향상된 기능은 이제 모든 사용자가 사용할 수 있습니다.

* 이제 **대상자 컴포지션을 통해 생성된** 대상자를 타기팅하고 여정에서 데이터 보강 속성을 활용할 수 있습니다. [자세히 알아보기](../building-journeys/read-audience.md)

* 이제 여정과 캠페인에 **CSV 파일에서 업로드된 대상자**&#x200B;를 타겟팅할 수 있습니다. [자세히 알아보기](../audience/about-audiences.md#segments-in-journey-optimizer)

  >[!AVAILABILITY]
  >
  >* 대상자 컴포지션 및 사용자 정의 업로드(CSV 파일)의 대상자 및 속성은 현재 Healthcare Shield 또는 Privacy and Security Shield에서 사용할 수 없습니다.
  >* **CSV 파일의 대상자 업로드** 개선 사항은 초기 릴리스 이후 며칠 동안 점진적으로 롤아웃됩니다. 일부 사용자는 즉시 액세스할 수 있지만 다른 사용자는 자신의 환경에서 사용할 수 있게 되기까지 지연이 발생할 수 있습니다.

**여정**

* **여정 필터링** - 이제 기존의 사전 정의된 날짜 필터 외에도 **사용자 정의 날짜를 사용하여 여정** 인벤토리를 필터링할 수 있습니다. 이렇게 하면 특정 날짜, 특정 달 내, 전체 연도 또는 지정된 시간 범위에 작성되었거나 게시된 여정을 표시하여 목록을 세분화할 수 있습니다. [자세히 보기](../building-journeys/journey-gs.md#filter)
* **사용자 정의 작업** - 이제 **content-type** 헤더를 업데이트할 수 있습니다. 이 새로운 **content-type**&#x200B;은 JSON 콘텐츠를 참조해야 합니다. [자세히 보기](../action/about-custom-action-configuration.md#url-configuration)
* **구성** - stepEvents의 identityMap 속성이 이제 미리 채워져 있습니다. 기본 ID는 “primary = true”로 정의됩니다. [자세히 보기](../reports/sharing-field-list.md)
* **사용자 인터페이스** - 여정 화면의 상단 표시줄이 향상된 경험을 위해 재구성되었습니다. 여러 업데이트 중 여정 속성에 액세스할 수 있는 &#39;연필&#39; 아이콘이 이제 여정 이름 옆의 상단 표시줄 왼쪽에 표시됩니다. [자세히 보기](../building-journeys/journey-properties.md)

**SMS 채널**

* **옵트인/옵트아웃 키워드** - 이제 SMS 채널을 구성할 때 원하는 대로 **옵트인 및 옵트아웃 키워드**&#x200B;를 사용자 정의할 수 있습니다. Journey Optimizer는 지정된 이러한 키워드를 기반으로 응답을 트리거합니다. [자세히 알아보기](../sms/sms-configuration.md)

**캠페인**

* **API 트리거 캠페인** - API 트리거 캠페인을 활성화한 후 생성된 cURL 코드가 향상되었습니다. 이제 메시지에 사용된 모든 개인화(프로필 및 컨텍스트) 변수가 포함됩니다. [자세히 보기](../campaigns/api-triggered-campaigns.md#execute)

**빈도 규칙**

* 이제 이메일 및 푸시 외에도 SMS 및 DM 채널에 대한 빈도 규칙을 만들 수 있습니다. 빈도 규칙은 빈도 상한에 도달하면 메시지 및 작업에서 과도하게 요청된 프로필을 자동으로 제외합니다. [자세히 보기](../conflict-prioritization/rule-sets.md)

<!--**Decision management**

* **Capping rules** - You can now add **multiple capping rules** for one offer. This allows you to increase the level of control over the way offers are sent.-->


## 24년 1월 릴리스 {#jan-2024}

**릴리스 날짜**: 2024년 1월 30~31일

### 새로운 기능{#jan24-features}

이번 릴리스에는 아래 목록에 있는 새로운 기능이 제공됩니다.

<table>
<thead>
<tr>
<th><strong>전달성 업데이트</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer에서 DMARC 인증 기술을 지원합니다.</p>
<p>2024년 2월 1일부터 Google 및 Yahoo!에서 이메일을 보내는 데 사용하는 모든 도메인에 DMARC 레코드를 요구합니다. Journey Optimizer에서 Adobe에 위임한 모든 하위 도메인에 DMARC 레코드가 설정되어 있는지 확인해 주세요.</p>
<p>자세한 내용은 <a href="../configuration/dmarc-record-update.md">세부 설명서</a>를 참고하십시오.</p>
<br/><img src="assets/do-not-localize/dmarc.gif"/>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>사용 사례 플레이북</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Real-Time CDP 및 Journey Optimizer의 산업별 사용 사례 플레이북 카탈로그를 활용하여 Adobe Experience Platform 및 Adobe Journey Optimizer를 사용하여 수행할 수 있는 일반적인 사용 사례를 해결합니다.</p><p>요구 사항에 가장 적합한 플레이북을 선택하면 여정, 메시지, 스키마 또는 세그먼트와 같은 사용 사례를 지원하는 데 필요한 자산을 생성하고, 가치 창출 시간을 단축하기 위해 스키마에 맞게 사용자 지정할 수 있습니다.</p>
<p>자세한 내용은 <a href="../start/playbooks.md">세부 설명서</a>를 참조하십시오.</p>
<br/><img src="assets/do-not-localize/playbooks.gif"/>
</tr>
</tbody>
</table>

### 개선 사항 {#jan24-improvements}

이 릴리스는 아래 목록에 있는 개선 사항과 함께 제공됩니다.

**보고**

* **새 도메인 기반 분류 위젯** - 캠페인 및 여정 보고서를 개선하기 위해 새 위젯이 추가되었습니다. **도메인별 바운스 이유**, **도메인에서 전송 및 전달**, **도메인별 열기 및 클릭 수** 및 **도메인별 바운스 및 오류** 위젯은 도메인 수준에서 주요 이메일 게재 및 추적 지표에 대한 세부 분류를 제공합니다. [자세히 알아보기](../reports/channel-report-cja.md)

**SMS 채널**

* **이중 옵트인** - SMS에 대한 이중 옵트인 워크플로를 사용하면 장치에서 요청을 시작할 때 사용자가 메시지를 수신하도록 명시적으로 옵트인할 수 있습니다. 사용자는 인바운드 SMS 메시지를 전송하여 동의 프로세스를 시작합니다. 동의를 확인하면 최종 확인을 요청하는 후속 메시지가 발송됩니다. 사용자 프로필이 존재하지 않으면 확인 후 생성됩니다. [자세히 알아보기](../sms/sms-configuration.md)

  이 기능은 Sinch 및 Infobip SMS 공급자만 사용할 수 있습니다.

**여정**

* **반응 이벤트 기간** - **반응 이벤트**&#x200B;에서 정의할 수 있는 최대 기간은 이제 30일이 아니라 29일입니다. [자세히 알아보기](../building-journeys/reaction-events.md)

<!--* **Date filters** - You can now use custom dates to filter the journeys inventory, in addition to the existing predefined date filters. This allows you to refine the list by displaying journeys published on a specific date, within a particular month, throughout an entire year, or within specified time ranges. [Learn more](../building-journeys/journey-gs.md#filter)-->

* **대상자 읽기**  - **대상자 읽기** 활동은 이제 예약된 일별 배치 작업이 실행된 후 하루에 한 번만 생성되는 배치 세그먼트에 대한 프로필 스냅샷 데이터 세트를 사용하므로 데이터는 마지막 일별 배치 작업까지 새로 고쳐집니다. [자세히 알아보기](../building-journeys/read-audience.md)

* **필드 그룹** - 이 릴리스에서는 특정 경우에 필드 그룹이 저장되지 않는 문제를 해결했습니다.

* 여러 함수에서 `<listObject>` 지원이 수정되었습니다.

**빈도 규칙**

* **주별 빈도 상한** - 이제 월별 외에 일주일 단위로 고객 프로필에 전송되는 최대 메시지 수를 지정할 수 있습니다. 빈도 캡은 선택된 캘린더 기간에 기반하고 대응하는 시간대가 시작될 때 재설정됩니다. [자세히 알아보기](../conflict-prioritization/rule-sets.md)

  >[!NOTE]
  >
  >필요에 따라 일일 빈도 상한도 이용하실 수 있습니다. Adobe 담당자에게 문의하십시오.

**의사 결정 관리**

* **Edge 빈도 상한 설정** - 이제 빈도 상한 설정 카운터가 업데이트되어 Edge Decisioning API 결정에서 3초 이내에 사용할 수 있습니다. [자세히 알아보기](../offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)
