---
solution: Journey Optimizer
product: journey optimizer
title: 릴리스 정보
description: Journey Optimizer 초기 릴리스 정보
feature: Release Notes
topic: Content Management
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 61447b6400b65e29a9187790e74be47b09764c4a
workflow-type: ht
source-wordcount: '1967'
ht-degree: 100%

---

# 초기 릴리스 정보 {#e-release-notes}

[!DNL Adobe Journey Optimizer]는 지속적으로 새로운 기능, 기존 기능 개선, 버그 해결을 제공합니다. 모든 변경 사항은 매월 말 [릴리스 정보](release-notes.md)에 통합됩니다.

**아래 초기 릴리스 정보는 릴리스 공개 당일까지 사전 통지 없이 변경될 수 있습니다**. 링크, 화면, 업데이트된 설명서는 릴리스 날짜의 [릴리스 정보](release-notes.md)에 게시됩니다.

## 2024년 10월 초기 릴리스 정보 {#e-2024}

**릴리스 일자**: 2024년 10월 29~30일

### 새로운 기능 {#e-features}

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
<!--p>For more information, refer to the <a href="../content-management/gs-generative.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/ai-content.gif"/-->
</td>
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
<p>이전에는 일부 조직에서만 사용할 수 있던(LA) 승인 정책을 이제 모든 사용자가 사용할 수 있습니다(GA).</p>
<p>자세한 내용은 <a href="../test-approve/gs-approval.md">세부 설명서</a>를 참조하십시오.</p>
<img src="assets/do-not-localize/approval.gif"/>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>이메일 구성 개인화(일반 가용성)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 이메일 채널 구성을 만들 때 동적 하위 도메인과 개인화된 헤더 매개 변수를 정의하여 이메일 설정을 더욱 유연하게 제어할 수 있습니다.</p><p>캠페인 또는 여정에서 개인화된 구성을 사용하면 이메일 콘텐츠를 미리 보며 정의한 동적 설정 사용 시 오류 가능성이 있는지 확인할 수 있습니다.</p>
<p>이전에는 일부 조직에서만 사용할 수 있던(LA) 이메일 구성 개인화를 이제 모든 사용자가 사용할 수 있습니다(GA).</p>
<p>자세한 내용은 <a href="../email/surface-personalization.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>샘플 입력 데이터를 사용하여 콘텐츠 테스트(Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer에서 이메일 콘텐츠의 다양한 변형을 테스트하기 위해 CSV 파일에서 업로드하거나 수동으로 추가한 샘플 입력 데이터를 사용하여 변형을 미리 보고 증명을 전송할 수 있습니다. 콘텐츠에서 개인화를 위해 사용되는 모든 프로필 속성은 시스템에서 자동 감지되며, 이를 테스트에 사용하여 여러 변형을 만들 수 있습니다.</p>
<p>이 기능은 현재 Beta로 사용할 수 있습니다.</p>
<!--<p>For more information, refer to the <a href="../email/surface-personalization.md">detailed documentation</a>.</p>-->
</td>
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
<p>Journey Optimizer에서 너무 많은 상호 작용으로 고객에게 부담을 주는 상황을 피하려면 캠페인과 여정의 양과 타이밍을 관리하는 것이 필수적입니다. 이제 Journey Optimizer에서 충돌 관리 및 우선 순위를 위한 몇 가지 도구를 제공합니다.</p><p><ul><li><b>여정 빈도 캡핑</b>: 이제 여정에 적용할 규칙 집합을 만들어 일별, 주별 또는 월별로 한 프로필의 여정 수를 제한하고, 한꺼번에 실행되는 동시 여정 수도 제어할 수 있습니다.</li>
<li><b>우선 순위 점수</b>: 이제 캠페인이나 여정에 0에서 100 사이의 우선 순위 점수를 할당할 수 있습니다. 숫자가 높을수록 우선 순위가 높다는 뜻입니다. 두 캠페인 또는 여정이 동일한 채널 구성을 사용하는 경우 Journey Optimizer에서 우선 순위 점수가 가장 높은 캠페인 또는 여정을 선택합니다. 캠페인의 점수가 동일한 경우, 수정한지 가장 오래된 캠페인을 선택합니다.</li>
<li><b>잠재적 충돌 보기</b>: 이제 여정 및 캠페인의 새로운 "잠재적 충돌 보기" 버튼을 사용하여 시작 일자, 타깃팅된 대상자 또는 선택한 채널 구성 등이 다른 여정 또는 캠페인과 겹치는지 확인할 수 있습니다.</li>
<li><b>여정 중재</b>: 이 새로운 기능을 사용하면 고객에게 가장 중요한 여정을 우선시할 수 있습니다. 고객이 우선 순위가 더 높은 예정된 여정에 입장할 자격이 있는 경우 우선 순위가 낮은 여정에 들어가지 않도록 하는 규칙을 만들 수 있습니다.</li></ul></p>
<!--<p>For more information, refer to the <a href="../email/surface-personalization.md">detailed documentation</a>.</p>-->
<p>충돌 및 우선 순위 관리 기능은 제한된 가용성으로 일부 고객이 사용할 수 있습니다. 이 기능은 향후 더 많은 사용자에게 점진적으로 배포될 예정입니다. 이 기능에 대한 대기자 명단에 등록하려면 계정 팀에 문의하십시오.</p>

</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>웹 디자이너용 비시각적 편집 모드</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer 웹 디자이너 대신 비시각적 편집기를 사용하여 웹 사이트에 수정 사항을 추가할 수 있습니다. 이 모드를 사용하면 페이지를 시각적 편집기에서 열지 않고 변경 사항을 수동으로 입력할 수 있습니다.
이 비시각적 편집 모드는 웹 디자이너에서 페이지를 로드하는 데 필요한 Adobe Experience Cloud Visual Helper와 같은 브라우저 확장 프로그램을 설치할 수 없는 경우에 유용합니다.</p>
<!--p>For more information, refer to the <a href="../email/surface-personalization.md">detailed documentation</a>.</p-->
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
<p>이전에는 일부 조직에서만 사용할 수 있던(LA) 여정 내 실험을 이제 모든 사용자가 사용할 수 있습니다(GA).</p>
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
<p>이전에는 일부 조직에서만 사용할 수 있고(LA) 경험 결정이라는 이름으로 제공되었던 의사 결정 기능을 이제 모든 사용자가 사용할 수 있습니다(GA). 이 기능은 '의사 결정 항목'이라는 중앙 집중식 마케팅 카탈로그와 정교한 결정 엔진을 제공하여 개인화를 간소화합니다. 이 엔진은 규칙과 순위 기준을 활용하여 각 개인에게 가장 관련성 높은 의사 결정 항목을 선택하고 제공합니다. 이 의사 결정 항목은 코드 기반 경험 채널을 통해 광범위한 인바운드 표면에 원활하게 통합됩니다.</p>

<p>현재 Adobe Healthcare Shield 및 Privacy and Security Shield Add-on 오퍼링을 구입한 고객은 의사 결정을 사용할 수 없습니다.</p>

<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>규칙 세트(제한된 가용성)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 세분화된 빈도 캡핑 규칙을 만들고 규칙 세트를 통해 메시지 또는 여정에 적용할 수 있습니다. 이 새로운 기능을 사용하면 메시지 및 액션에서 과도하게 요청된 프로필을 자동으로 제외하는 크로스 채널 규칙을 설정하여 대상자가 메시지를 받는 빈도를 제어할 수 있습니다.</p><p>또한 일별, 주별 또는 월별로 한 프로필의 여정 수를 제한하고, 한꺼번에 실행되는 동시 여정 수도 제어할 수 있습니다.</p>
<p>규칙 세트 기능은 제한된 가용성으로 일부 고객이 사용할 수 있습니다. 이 기능은 향후 더 많은 사용자에게 점진적으로 배포될 예정입니다. 이 기능에 대한 대기자 명단에 등록하려면 계정 팀에 문의하십시오.</p>
<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
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
<p>이제 일반 가용성으로 모든 채널에서 다국어 콘텐츠에 액세스할 수 있습니다. </p>
<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
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
<li>Journey Optimizer 고객의 실무 워크플로 가속화를 위해 작성에는 Da Vinci를 사용하고 최적화 및 게재에는 AJO 사용</li>
<li>Adobe 데이터로 Da Vinci 모델 최적화</li></ul></p>
<!--p>For more information, refer to the <a href="../code-based/get-started-code-based.md">detailed documentation</a>.</p-->
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
<p>2024년 10월 16일 이후 사용 가능</p>
<p>Journey Optimizer의 보고 기능이 이제 일반 가용성(GA)으로 공개되었습니다. 이 기능은 Customer Journey Analytics 기능의 개선된 상호 운용성과 함께 제공되어 양 플랫폼의 보고를 표준화하고 데이터의 일관성과 안정성을 개선합니다. 이렇게 Journey Optimizer와 Customer Journey Analytics가 원활하게 통합됨으로써 사용자가 성과 지표를 보다 명확하게 확인하여 확실한 정보에 근거한 결정을 내릴 수 있습니다.</p>
<p>일반 가용성 전환과 더불어 네 가지 새로운 기능이 도입되었습니다. 이제 간단한 지표 만들기, 대상자 만들기 및 게시, Insight Builder를 사용한 임시 질문 사용, 주요 수신자에게 자동으로 이메일로 전송할 보고서 예약이 가능합니다.</p>
<p>자세한 내용은 <a href="../reports/report-cja-manage.md">세부 설명서</a>를 참조하십시오.</p>
<img src="assets/do-not-localize/ajo-cja.gif">
<p>중요: 현재 보고 경험은 2025년 1월부로 사용이 종료됩니다. 이 날짜 이후에는 새로운 보고 경험이 표준이 됩니다. 원활한 전환을 위해 새로운 기능을 숙지하는 것이 좋습니다. <a href="../reports/report-gs-cja.md">Journey Optimizer의 새로운 보고 인터페이스를 시작하는 방법 알아보기</a></p>
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
<p>2024년 10월 1일 이후 사용 가능</p>
<p>코드 기반 경험 채널에서는 Adobe Journey Optimizer에서 원하는 인바운드 속성에 대해 고급 개인화 및 테스트를 수행할 수 있으므로 웹 앱, 모바일 앱, 데스크탑 앱, 비디오 콘솔, TV에 연결된 디바이스, 스마트 TV, 키오스크, ATM, IoT 디바이스 등과 같은 다양한 접점에서 맞춤형 경험을 원활하게 전달할 수 있습니다. 이제 여정 캔버스에서 코드 기반 경험 채널을 사용할 수 있습니다.</p>
<p>자세한 내용은 <a href="../code-based/create-code-based.md">세부 설명서</a>를 참조하십시오.</p>
<img src="../assets/do-not-localize/code-based-journey.gif"/>
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
<p>2024년 10월 1일 이후 사용 가능</p>
<p>웹 채널을 사용하면 Adobe Journey Optimizer에서 인바운드 웹 채널을 통해 고객에게 제공하는 웹 경험을 개인화할 수 있습니다. 이제 여정 캔버스에서 웹 채널을 사용할 수 있습니다.</p>
<p>자세한 내용은 <a href="../web/create-web.md">세부 설명서</a>를 참조하십시오.</p>
<img src="../assets/do-not-localize/web-journey.gif"/>
</tr>
</tbody>
</table>

### 개선 사항 {#e-improvements}

이 릴리스는 아래 목록에 있는 개선 사항과 함께 제공됩니다.

**SMS 채널**

>[!AVAILABILITY]
>
>다음 개선 사항은 Sinch 및 Infobip 공급자만 사용할 수 있습니다.

메시징 기능을 개선하기 위해 다음과 같은 SMS 개선 사항이 도입되었습니다.

* SMS 캠페인 및 여정에 대한 고유 키워드를 정의하고 관리하여 보다 개인화되고 효율적인 커뮤니케이션을 가능하게 할 수 있습니다.

* 키워드가 인식되지 않을 때 사용할 기본 SMS 메시지를 만들고 전송할 수 있습니다.

* 이제 SMS API 채널 구성을 편집하거나 삭제할 수 있습니다.

<!--**Journeys**-->

<!--* **Path experiment in journeys** - With the journey path experiment, you can now define and track key metrics for your journey paths, allowing you to measure the impact of your activities and to provide clearer insights into your performance. -->

<!--* **Max number of Live journeys** - Journey Optimizer now has a guardrail of 500 live journeys on production sandboxes, instead of 100. The number of live journeys is visible in the journey canvas. (DOCAC-10977) -->

**데이터 세트**

* **Time-to-Live 가드레일** - 2024년 11월 1일부터 새 샌드박스 및 새 조직의 Journey Optimizer 시스템 생성 데이터 세트에 대해 다음과 같은 TTL(Time-to-Live) 가드레일이 롤아웃됩니다.

   * 프로필 스토어의 데이터에 대해 90일
   * 데이터 레이크의 데이터에 대해 13개월

  이 변경 사항은 이어질 두 번째 단계에서 기존 고객 샌드박스에 대해서도 롤아웃됩니다. 

  또한 11월 1일부터 스트리밍 세분화는 더 이상 추적 및 피드백 데이터 세트에서 이벤트 보내기 및 열기 사용을 지원하지 않습니다. 이 변경 사항은 해당 시점에 모든 고객 샌드박스 및 조직에 적용됩니다. [자세히 알아보기](../data/datasets-ttl.md)

* **사용자 정의 액션의 매개 변수**(사용 가능한 날짜: 2024년 10월 3일) - 이제 사용자 정의 액션에서 NULL 및 선택적 매개 변수가 지원됩니다. [자세히 알아보기](../action/about-custom-action-configuration.md#define-the-message-parameters)

**보고**

* 이제 **결정 보고**&#x200B;를 사용할 수 있습니다. 이 기능은 방문자가 경험과 상호 작용하는 방식에 대해 기본적인 인사이트를 제공합니다.

**데이터 거버넌스 및 동의 정책** - 사용 가능한 날짜: 2024년 10월 7일

* **데이터 거버넌스 정책** 시행이 이제 Journey Optimizer의 모든 채널에 적용됩니다. Adobe Experience Platform에서 정책을 만든 고객의 경우 이 정책은 채널 구성 설정의 일부로 마케팅 액션에 적용됩니다. 구성을 사용하여 콘텐츠를 만들 때 시스템은 모든 개인화 필드를 확인하여 데이터 거버넌스 위반 여부를 찾습니다. 위반이 발견되면 여정 또는 캠페인을 게시할 수 없습니다. [자세히 알아보기](../action/action-privacy.md)

* 이제 **사용자 정의 동의 정책**&#x200B;이 모든 Journey Optimizer 채널에 적용됩니다. 메시지가 전송되거나 인바운드 경험이 게재되기 전에 적용 시 시스템은 사용자가 수신할 콘텐츠의 개인화 필드 사용에 동의했는지 확인합니다. 동의를 하지 않은 경우 해당 경험이 표시되지 않습니다. [자세히 알아보기](../action/consent.md)

  >[!NOTE]
  >
  >동의 정책 기능은 현재 Adobe **Healthcare Shield** 또는 **Privacy and Security Shield** 추가 기능 서비스를 구매한 조직에만 제공됩니다.

**대상자** - 사용 가능한 날짜: 2024년 10월 8일

* 이제 CSV 파일 대상자를 타기팅할 때 개인화 편집기와 여정 및 캠페인 규칙 빌더에서 파일의 속성을 사용할 수 있습니다. [자세히 알아보기](../audience/about-audiences.md)

* 이제 사용자 정의 업로드(CSV 파일)의 대상자 및 속성을 Healthcare Shield 또는 Privacy and Security Shield에서도 사용할 수 있습니다.

**코드 기반 채널**

* 이제 콘텐츠 템플릿을 사용할 수 있습니다. 개발자가 작성한 콘텐츠 템플릿에서 시작하여 코드 기반 경험을 빠르게 작성할 수 있습니다. 콘텐츠 템플릿을 사용하면 마케터가 전체 HTML 또는 JSON 콘텐츠 페이로드를 작성할 필요 없이 일부 값 또는 필드만 수정할 수 있습니다.

**의사 결정**

[Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=ko) 사용자는 이제 의사 결정(이전 이름: 경험 결정)에서 AI 모델을 설정할 때 최적화할 사용자 정의 모델을 선택할 수 있습니다. 예를 들어 클릭스루 비율과 같은 정의된 제한 대신 사용자 정의 &quot;구매&quot; 테이블을 기반으로 최적화할 수 있습니다.
