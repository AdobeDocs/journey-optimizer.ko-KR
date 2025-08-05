---
solution: Journey Optimizer
product: journey optimizer
title: 릴리스 정보
feature: Release Notes
topic: Content Management
description: Adobe Journey Optimizer 릴리스 정보
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '1361'
ht-degree: 35%

---

# 릴리스 정보 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="새로운 기능"
>abstract="**Adobe Journey Optimizer**&#x200B;는 지속적으로 새로운 기능, 기존 기능 개선, 버그 수정을 제공합니다. 모든 변경 사항은 매달 마지막 주에 여기 있는 릴리스 정보에 통합됩니다."

[!DNL Adobe Journey Optimizer]은(는) 지속적으로 새로운 기능, 기존 기능 개선, 버그 해결을 제공합니다. 모든 변경 사항은 매달 마지막 주 여기 있는 릴리스 정보에 통합됩니다. [!DNL Adobe Journey Optimizer]은 기본적으로 [!DNL Adobe Experience Platform] 기반으로 빌드되었으며 최신 혁신 및 향상된 기능을 활용할 수 있습니다. 변경 사항에 대한 자세한 내용은 [Adobe Experience Platform 릴리스 정보](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=ko){target="_blank"}를 참조하십시오.


## 캠페인 오케스트레이션

**사용 가능한 날짜**: 2025년 8월 4일

이제 Journey Optimizer에 브랜드 시작 일괄 캠페인을 위해 특별히 빌드된 새로운 기능인 **Campaign Orchestration**&#x200B;이(가) 포함되어 있습니다. 이 릴리스에서는 캠페인 오케스트레이션 캔버스 및 향상된 데이터 모델링을 도입하여 마케터가 개인화된 크로스 채널 캠페인을 계획, 타깃팅 및 제공할 수 있도록 함께 작업합니다.

![Campaign Orchestration GIF](assets/do-not-localize/release.gif)

여기에는 [관계형 스키마 및 데이터 세트](#oc-relational) 및 [Campaign 캔버스](#oc-canvas)가 포함됩니다. 이러한 두 가지 혁신적인 기능을 통해 Journey Optimizer에서 일괄 캠페인을 오케스트레이션하기 위한 새로운 표준을 마련할 수 있습니다. 주요 기능은 아래에 나와 있습니다.

### 주요 기능 {#oc-capabilities}

* **여러 단계 워크플로**

  특별히 제작된 새로운 캠페인 오케스트레이션 캔버스를 통해 정교한 멀티채널 일괄 캠페인을 수행할 수 있습니다.

* **온디맨드 대상**

  즉각적인 활성화를 위해 온디맨드로 대상자를 세그먼트화합니다.

* **다중 엔터티 세분화**

  제품, 스토어, 갱신, 예약 등과 같은 비즈니스 컨텍스트(비사용자 차원)를 사용하여 대상을 작성합니다.

* **미리 전송 가시성**

  캠페인 실행 전과 실행 중에 대상자 및 캠페인을 검토, 세분화 및 최적화합니다.

### 캠페인 캔버스 {#oc-canvas}

일괄 캠페인을 위해 특별히 빌드된 새로운 시각적 오케스트레이션 인터페이스입니다. 이 캔버스를 통해 다음과 같은 작업을 수행할 수 있습니다.

* 여러 단계, 다중 채널 캠페인 흐름의 시각적 계획

* 관계형 쿼리를 기반으로 구축된 온디맨드 대상 지원

* 고급 대상 분할, 대기 및 조건부 논리

* 비즈니스 규칙 및 필터 적용 후 정확한 사전 전송 카운트

### 관계형 스키마 및 데이터 세트 {#oc-relational}

이제 Adobe Experience Platform은 사용자 기반 프로필에 연결된 관계형 엔티티(예: 제품, 스토어, 예약, 계약)를 지원합니다. 이를 통해 다차원 데이터 구조 간에 세분화 및 개인화를 수행할 수 있으므로 다음과 같은 사용 사례가 가능합니다.

* 예약, 구독 또는 계약당 하나의 메시지

* 관련 엔티티 속성(예: 제품 카테고리 또는 스토어 위치)을 기반으로 한 세분화

* 향상된 주소 지정(예: 엔티티에 연결된 알려진 모든 연락처로 전송)

### 중요한 이유

이 릴리스를 통해 마케터는 유연한 데이터 모델링과 특별히 빌드된 오케스트레이션 경험을 결합하여 브랜드 주도, 대상 기반 일괄 마케팅을 완벽하게 제어할 수 있습니다. 이는 고급 개인화 및 확장성을 제공하면서도 실시간 여정의 일괄 캠페인 오케스트레이션을 위해 특별히 설계되었습니다.

### 자세히 알아보기

자세한 내용은 [Campaign 오케스트레이션 설명서](../orchestrated/gs-orchestrated-campaigns.md)를 참조하세요.

<!--
## August '25 pre release notes {#25-7-rn}

**Pre release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published at the release date.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/ko/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Release date**: August 19, 2025


### New capabilities {#Aug-25-8-features}

New capabilities coming with this release are detailed below.

### Improvements {#Aug-25-8-improv}

Improvements coming with this release are listed below.
-->


## 2025년 7월 릴리스 정보 {#25-7-rn}

**릴리스 일자**: 2025년 7월 29일 수요일

### 새로운 기능 {#features-25-7}

이번 릴리스의 새로운 기능을 아래에서 자세히 설명합니다.

#### 기능

<table>
<thead>
<tr>
<th><strong>WhatsApp 채널</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer에서 직접 WhatsApp 메시지를 지원하여 여정 및 캠페인에 원활하게 통합하여 수신자 커뮤니케이션 및 참여를 개선할 수 있습니다. 이 기본 채널은 WhatsApp 템플릿 통합, 메시지 미리 보기, 개인화, 게재 보고, 웹후크, 옵트인 및 옵트아웃 동의 관리 등을 즉시 제공합니다.</p>
<p>이전에 Beta에서 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).</p>
<p><img src="../whatsapp/assets/do-not-localize/WA-Animation.gif"/><p>
<p>자세한 내용은 <a href="../whatsapp/get-started-whatsapp.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>브랜드</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 커뮤니케이션 전반에 걸쳐 시각적, 언어적 정체성을 명확하게 정의하기 위해 자체 브랜드를 만들고 사용자 정의할 수 있습니다. 브랜드 정렬 점수를 사용하면 콘텐츠가 브랜드의 톤, 스타일, 가이드라인을 얼마나 잘 반영하는지에 대한 실시간 피드백을 받을 수 있으므로 보내는 모든 메시지에서 일관되게 브랜드에 맞는 내용을 전달하는 데 도움이 됩니다.</p>
<p>이전에 Beta에서 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).</p>
<p><img src="assets/do-not-localize/brand-score.gif"/></p>
<p>자세한 내용은 <a href="../content-management/brands.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>이메일 채널에서 Decisioning 사용</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 이메일 여정 및 캠페인에 의사 결정 정책을 추가할 수 있습니다. 의사 결정 정책은 의사 결정 엔진을 활용하여 각 대상 구성원에 대해 제공할 최상의 콘텐츠를 동적으로 반환하는 오퍼에 대한 컨테이너입니다.</p>
<p>이 기능은 제한된 가용성으로 사용할 수 있습니다. 액세스 권한을 얻으려면 Adobe 담당자에게 문의하십시오.</p>
자세한 내용은 <a href="../experience-decisioning/create-decision.md">자세한 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>LINE 채널</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer는 LINE 채널에 대한 지원을 포함하도록 크로스 채널 기능을 확장했습니다. 이 향상된 기능을 통해 LINE 경험을 만들고 편집하고 미리 볼 수 있으므로 보다 개인화되고 매력적인 상호 작용을 제공할 수 있습니다. LINE을 사용하여 더 많은 고객과 소통하고 관련 콘텐츠를 전송하며 참여도를 개선할 수 있습니다.</p>
<p>이전에는 요청만 사용할 수 있었지만 이제 모든 사용자가 LINE 채널을 사용할 수 있게 되었습니다(일반 공급).</p>
<p>자세한 내용은 <a href="../line/get-started-line.md">세부 설명서</a>를 참조하십시오.</p></td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Optimization in campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer now empowers you with the tools to deliver personalized and optimized content to your campaigns' audience, allowing you to run content experiments, create rule-based targeting, and use advanced combinations of both, to maximize the effectiveness of your campaigns.</p>
<p>With Optimization, you can:</p>
<ul>
<li>Test multiple content variations to identify the most effective messaging.</li>
<li>Deliver personalized content based on user attributes and contextual data.</li>
<li>Combine targeting and experimentation for advanced campaign strategies.</li>
<li>Filter out users that do not match variant criteria.</li>
<li>Ensure fallback mechanisms to maintain user engagement.</li>
</ul>
<P>Once the campaign is live, profiles are evaluated against the defined criteria, and based on matching criteria, they are delivered with the appropriate experience or content from the campaign.</p>
<p><img src="assets/do-not-localize/campaign-optimization.gif"/></p>
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table>
-->



<table>
<thead>
<tr>
<th><strong>여정 시험 실행</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>여정 시험 실행은 Adobe Journey Optimizer에서 제공되는 특별한 여정 게시 모드로, 여정 실무자가 실제 고객에게 연락하거나 프로필 정보를 업데이트하지 않고도 실제 프로덕션 데이터를 사용해 여정을 테스트할 수 있도록 합니다. 이 기능은 여정 실무자가 여정을 게시하기 전에 여정 설계와 대상자 타기팅에 대한 자신감을 얻는 데 도움이 됩니다.</p>
<img src="assets/do-not-localize/DryRun.gif">
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).</p>
<p>자세한 내용은 <a href="../building-journeys/journey-dry-run.md">자세한 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>여정에 대한 보조 ID</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 주문 ID, 구독 ID 또는 처방전 ID와 같은 다른 식별자와 함께 프로필 ID를 사용하여 여정을 트리거함으로써 동일한 프로필이 한 번에 여러 차례 동일한 여정에 있도록 할 수 있습니다. 이를 통해 각 인스턴스가 자체 여정 경로를 따르면서 여러 주문 또는 구독을 동시에 관리할 수도 있습니다.</p>
<p>이전에 [제한된 가용성]에서 릴리스된 이후에는 이제 여정에서 보조 ID를 사용할 수 있습니다. 이번 GA 릴리스에서는 이제 대상자 읽기 여정에 대한 지원이 기능에 포함됩니다.</p>
<p><img src="assets/do-not-localize/gif-supplemental.gif"/></p>
<p>자세한 내용은 <a href="../building-journeys/supplemental-identifier.md">자세한 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>

### 제품 내 경고

이제 Journey Optimizer 제품 릴리스에 대한 **이메일 및 제품 내 경고**&#x200B;를 구독할 수 있습니다.

구독하려면:

* **Adobe Experience Cloud 환경 설정**(으)로 이동
* **알림**&#x200B;에서 **Journey Optimizer 새 릴리스**&#x200B;를 찾습니다.
* 인앱 및 이메일 알림 활성화

![](assets/do-not-localize/pulse-notif.png){width="70%" align="left"}


### 여정 조건 변경 {#ee-change@}

7월 8일부로 신규 고객 조직의 경우 여정 조건에 사용하는 표현식 편집기에서 경험 이벤트를 사용하여 표현식을 만드는 작업이 지원되지 않습니다. 따라서 표현식을 만드는 데 [Experience Platform 데이터 소스](../datasource/adobe-experience-platform-data-source.md)의 경험 이벤트를 사용할 수 없습니다. 경험 이벤트를 사용하여 표현식/논리를 만드는 다른 방법 및 모범 사례는 [여기](../building-journeys/exp-event-lookup.md)에서 참조할 수 있습니다.

단일 여정에서 여정 컨텍스트 이벤트 데이터에 액세스하는 방법에는 변화가 없습니다. 사용자는 계속 표현식 편집기 및 개인화 편집기에서 초기 여정 이벤트로 전달된 데이터에 액세스할 수 있습니다.

[이 FAQ](../building-journeys/exp-event-lookup.md#faq-ee)에서 자세히 알아보십시오.

### 개선 사항 {#25-7-improv}

다음은 이번 릴리스의 개선 사항 목록입니다.

* **캠페인**

   * **캠페인의 여러 인바운드 작업** - 이제 캠페인 오케스트레이션을 단순화하기 위해 단일 캠페인에서 여러 인바운드 작업을 정의할 수 있습니다. 이 기능을 사용하면 여러 코드 기반 경험, 인앱 메시지, 콘텐츠 카드 또는 웹 작업을 동시에 다른 위치에 전달할 수 있으며, 각 작업에는 특정 콘텐츠가 포함됩니다.
  <!-- [Read more](../FILE.md) -->

   * **캠페인 인벤토리 재구성** - 이제 예약된 캠페인 및 API 트리거 캠페인이 더 쉬운 탐색 및 관리를 위해 캠페인 인벤토리에서 별도의 탭으로 분할됩니다.

[자세히 표시](../campaigns/modify-stop-campaign.md)

* **데이터 관리**
   * **의사 결정 관리 시스템 데이터 세트 업데이트** - 이제 삭제된 개인화된 오퍼 및 대체 오퍼가 &quot;decision_object_repository_personalized_offers&quot; 및 &quot;decision_object_repository_fallback_offers&quot; 데이터 세트에 보관된 것으로 표시됩니다. 데이터 세트의 기존 레코드는 변경되지 않습니다.

[자세히 표시](../offers/export-catalog/access-dataset.md)

* **여정**
   * **여정 샌드박스 도구 개선 사항** - 패키지 내보내기 및 가져오기 기능을 사용하여 여러 샌드박스에서 여정을 복사할 때 이제 다음 기능도 사용할 수 있습니다.
      * 대상에서 기존 이벤트 선택
      * 여정과 독립적으로 이벤트 복사
      * 필드 그룹/데이터 소스 관계 감지, 대상(있는 경우)에서 연결, 없는 경우 생성.

[자세히 표시](../configuration/copy-objects-to-sandbox.md)

* **채널 - 인앱**
   * **인앱 키/값 쌍** - 인앱 메시지를 사용하여 메시지 페이로드에 사용자 지정 변수를 포함하도록 키 및 값 쌍을 정의할 수 있습니다. 이러한 키-값 쌍을 사용하면 특정 구성 및 사용 사례에 따라 추가 데이터를 전달할 수 있습니다. [자세히 보기](../in-app/design-in-app.md)

* **채널 - 콘텐츠 카드**

   * **규칙 기반 캠페인 결격** - 추가 게재 규칙을 편집할 때 이전 게재 규칙 옵션이 세 가지 개별 규칙 유형으로 대체되어 메시지 타이밍 및 가시성을 더 잘 제어할 수 있습니다.
      * 다음과 같은 경우 메시지 표시: 컨텐츠 카드가 표시되는 시기를 결정하는 조건입니다.
      * 다음과 같은 경우 메시지 닫기: 컨텐츠 카드를 일시적으로 숨기는 조건. 표시 조건이 다시 충족되는 경우 다시 나타날 수 있습니다.
      * 메시지 부적격: 컨텐츠 카드가 다시 표시되지 않도록 영구적으로 차단하는 조건.

[자세히 표시](../content-card/design-content-card.md)

* **의사 결정**
   * **마이그레이션 도구 API** - Journey Optimizer 팀은 현재 의사 결정 관리 엔터티를 Decisioning으로 마이그레이션하기 위한 마이그레이션 도구 API를 작업 중입니다. 이 도구를 사용하면 종속성 해결 및 롤백 기능을 통해 샌드박스 간에 원활하게 마이그레이션할 수 있습니다. 관심이 있는 경우 Adobe 담당자에게 문의하십시오.

* **개인화**
   * 새로운 도우미 함수인 &quot;SHA256&quot;이 개인화 편집기에 추가되었습니다. 이 함수는 문자열의 sha256 해시를 계산하고 반환하는 데 사용합니다.

[자세히 표시](../personalization/functions/string.md#sha256)
