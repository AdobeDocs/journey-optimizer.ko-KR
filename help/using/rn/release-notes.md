---
solution: Journey Optimizer
product: journey optimizer
title: 릴리스 정보
feature: Release Notes
topic: Content Management
description: Adobe Journey Optimizer 릴리스 정보
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: b08f996d9871f59665c2d329b493fd6e61030fac
workflow-type: tm+mt
source-wordcount: '1774'
ht-degree: 74%

---

# 릴리스 정보 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="새로운 기능"
>abstract="**Adobe Journey Optimizer**&#x200B;는 지속적으로 새로운 기능, 기존 기능 개선, 버그 수정을 제공합니다. 모든 변경 사항은 매달 마지막 주에 여기 있는 릴리스 정보에 통합됩니다."

[!DNL Adobe Journey Optimizer]은(는) 지속적인 게재 모델을 따르므로 Adobe은 새로운 기능, 개선 사항 및 수정 사항을 지속적으로 제공할 수 있습니다. 이 접근 방식을 사용하면 확장 가능한 단계별 기능 롤아웃을 통해 모든 환경에서 성능과 안정성을 보장할 수 있습니다.

이 모델로 인해 릴리스 노트는 월별 릴리스 사이에 업데이트됩니다.  전용 [최신 업데이트](#updates-rn) 섹션에서는 프로덕션에 배포할 때 새로운 기능과 향상된 기능을 강조하므로 항상 모든 변경 내용을 실시간으로 알려줍니다. <!--For full details about the release cycle and availability phases, see [Journey Optimizer release cycle](#releases.md).-->

[!DNL Adobe Journey Optimizer]은 기본적으로 [!DNL Adobe Experience Platform] 기반으로 빌드되었으며 최신 혁신 및 향상된 기능을 활용할 수 있습니다. 변경 사항에 대한 자세한 내용은 [Adobe Experience Platform 릴리스 정보](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=ko){target="_blank"}를 참조하십시오.

## 최신 업데이트 {#updates-rn}

지난 주에 릴리스된 새로운 기능 및 개선 사항은 아래에 나열되어 있으며 해당 사용 가능 날짜가 표시됩니다. 월말에 다음 릴리스 노트 콘텐츠로 그룹화됩니다. 아래의 최신 [릴리스 정보](#latest-rn)도 참조하세요.

### 새로운 기능 {#updates-features}

<table>
<thead>
<tr>
<th><strong>실행 메타데이터 도우미</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>개인화 편집기에서 새로운 'executionMetadata' 도우미 기능을 사용할 수 있습니다. 이를 통해 컨텍스트 정보를 모든 기본 작업에 추가하고 데이터 세트에 캡처하여 외부 시스템으로 내보낼 수 있습니다.</p>
<p>이 기능은 제한적으로 이용할 수 있습니다. 액세스 권한을 얻으려면 Adobe 담당자에게 문의하십시오.</p>
<p>자세한 내용은 <a href="https://developer.adobe.com/journey-optimizer-apis/references/journeys-retrieve/">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2025년 10월 13일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>이메일에 PDF 파일 첨부</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer로 보내는 이메일 메시지에 정적 PDF 파일을 첨부할 수 있습니다.</p>
<ul>
<li>매년 프로필별로 최대 6개의 PDF 첨부 파일을 사용하여 메시지를 보낼 수 있습니다.</li>
<li>각 첨부 파일의 최대 크기는 5MB입니다.</li>
<li>용량이나 수량이 더 필요하다면 PDF 첨부 파일 추가 기능을 구매할 수 있습니다. 자세한 내용은 Adobe 담당자에게 문의하십시오.</li>
</ul>
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).</p>
<p><img src="assets/do-not-localize/pdf-attachments.gif"/></p>
<p>자세한 내용은 <a href="../email/pdf-attachments.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2025년 9월 30일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>여정 검색을 위한 공개 API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 새로운 Journey Optimizer API를 사용하여 캠페인과 표면 등 여정 및 관련 개체를 검색할 수 있습니다.</p>
<p>자세한 내용은 <a href="https://developer.adobe.com/journey-optimizer-apis/references/journeys-retrieve/">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2025년 9월 25일</p>
</td>
</tr>
</tbody>
</table>

### 개선 사항 {#updates-improvements}

**Mailto(구독 취소) 주소에 대한 사용자 지정 특성 지원**

Journey Optimizer을 사용하여 Adobe 외부에서 동의를 관리하는 경우 이메일 구성에서 사용자 지정 구독 취소 이메일 주소와 원클릭 구독 취소 링크를 정의하여 외부 사용자 지정 엔드포인트를 설정할 수 있습니다. 수신자가 구독 취소 링크를 클릭하면 Journey Optimizer는 기본 프로필별 매개 변수 몇 가지를 동의 업데이트 이벤트에 추가합니다.

이제 사용자 지정 끝점을 추가로 개인화하기 위해 동의 이벤트에도 추가될 사용자 지정 특성을 정의할 수 있습니다. [자세히 보기](../email/list-unsubscribe.md#custom-attributes)

>[!AVAILABILITY]
>
>이 기능은 2025년 8월 이후 사용자 지정 **[!UICONTROL 한 번의 클릭으로 구독 취소 URL]**&#x200B;에 이미 사용할 수 있으며, 이제 [제한된 가용성]의 **[!UICONTROL Mailto(구독 취소)]** 옵션에 대해 릴리스되었습니다. 액세스 권한을 얻으려면 Adobe 담당자에게 문의하십시오.

사용 가능한 날짜: 2025년 10월 6일

## 25년 9월 릴리스 정보 {#latest-rn}

**릴리스 일자**: 2025년 9월 23~24일

### 새로운 기능 {#sept-25-9-features}

<table>
<thead>
<tr>
<th><strong>Journey Optimizer Experimentation Accelerator</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer Experimentation Accelerator는 실험을 한 단계 더 발전시키기 위해 설계된 AI 중심 제품입니다. Adobe Journey Optimizer 및 Adobe Target 사용자를 위해 구축된 이 솔루션은 실험 관리를 통합하고, AI 기반 인사이트와 기회를 제공하며, 새로운 실험 에이전트를 도입합니다.</p>
<p>다음과 같은 기능을 기대할 수 있습니다.</p>
<ul>
<li><strong>통합 실험 인벤토리:</strong> 하나의 중앙 작업 공간에서 Adobe Journey Optimizer 및 Adobe Target의 모든 실험을 빠르게 보고 필터링하고 관리합니다.</li>
<li><strong>AI 실험 인사이트 및 기회:</strong> 단순한 통계 읽기를 넘어 생성형 AI 기반 인사이트와 추천을 이용할 수 있습니다. 이제 실험별로 실행 가능한 기회를 근거와 함께 표시하므로 팀에서 다음에 테스트할 항목을 보다 자신 있게 결정할 수 있습니다.</li>
<li><strong>Journey Optimizer의 Multi-Armed Bandit(MAB) 지원:</strong> Multi-Armed Bandit 실험으로 트래픽 낭비를 줄이면서 효과를 극대화할 수 있습니다. MAB는 대상자를 균등하게 분할하지 않고 실시간으로 성과가 가장 좋은 베리에이션에 더 많은 방문자를 자동 할당하므로 더 많은 고객에게 더 나은 경험을 제공하면서 효과가 있는 변수를 파악할 수 있습니다.</li></ul>
<p><img src="assets/do-not-localize/experimentation-accelerator.gif"/></p>
<p>자세한 내용은 <a href="../content-management/experiment-accelerator.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2025년 10월 3일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey 에이전트가 등장했습니다!</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><a href="https://experienceleague.adobe.com/ko/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-orchestrator" target="_blank">Adobe Experience Platform Agent Orchestrator</a> 기반 Journey 에이전트를 Journey Optimizer에서 사용할 수 있습니다. 이 에이전트를 사용하면 자연어 인터페이스를 통해 여정을 분석할 수 있습니다. 에이전트는 여정에서 대상자 또는 일정 충돌 및 프로필 감소를 감지하여 이를 해결하기 위한 단계를 수행합니다. 곧 에이전틱 지원을 통해 여정을 만들 수 있게 될 것입니다.</p>
<p>자세한 내용은 <a href="https://experienceleague.adobe.com/ko/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent-analyze" target="_blank">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2025년 9월 24일</p>
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
<p><img src="assets/do-not-localize/dark-mode.gif"/></p>
<p>자세한 내용은 <a href="../email/dark-mode.md">세부 설명서</a>를 참조하십시오.</p>
 <p>사용 가능한 날짜: 2025년 9월 16일</p>
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
<p>새로운 최적화 노드를 사용하여 특정 대상자를 타기팅하거나 A/B 테스트를 실행하여 비즈니스 중심 KPI를 충족하는 최상의 경로를 결정합니다.</p>
<p>이 도구를 사용하여 테스트 및 변경을 수행하고 커뮤니케이션, 시퀀스, 타이밍을 사용자 정의하여 고객에게 가장 효과적으로 다가갈 수 있습니다.</p>
<p>이 기능은 제한적으로 이용할 수 있습니다. 액세스 권한을 얻으려면 Adobe 담당자에게 문의하십시오.</p>
<p><img src="assets/do-not-localize/optimize.gif"/></p>
<p>자세한 내용은 <a href="../building-journeys/optimize.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2025년 9월 4일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>하위 도메인에 대한 사용자 정의 위임 방법</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 전체 위임과 CNAME 방법 외에 새로운 하위 도메인 구성 방법인 사용자 정의 위임 방법을 사용할 수 있습니다. 이 방법을 사용하면 메시지 게재, 렌더링, 추적에 필요한 DNS의 모든 측면을 사용자가 완전히 제어하고 유지 관리할 수 있습니다.</p>
<p>이 기능은 제한적으로 이용할 수 있습니다. 액세스 권한을 얻으려면 Adobe 담당자에게 문의하십시오.</p>
<p><img src="assets/do-not-localize/custom-delegation.gif"/></p>
<p>자세한 내용은 <a href="../configuration/delegate-custom-subdomain.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2025년 9월 4일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>개인화 및 결정을 위해 Adobe Experience Platform 데이터 사용</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이전에 공개 Beta로 릴리스된 이 기능을 이제 모든 환경에서 사용할 수 있습니다. 이번 릴리스에서는 다음과 같은 개선 사항이 도입되었습니다.</p>
<ul><li>인바운드 채널에서 데이터 세트 조회 개인화를 지원합니다.</li>
<li>이제 “datasetLookup” 도우미 함수를 표현식 조각 내에서 사용할 수 있습니다. 현재 이 기능은 제한된 고객들만 사용할 수 있습니다. 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.</li>
<li>이제 API 호출을 수행하지 않고도 데이터 세트 관리 인터페이스의 옵션을 통해 조회 개인화를 위한 레코드 기반 데이터 세트를 활성화할 수 있습니다.</li>
<li>데이터 수집 상태를 추적하고 데이터 세트를 조회할 준비가 되었는지 알 수 있도록 모니터링을 개선했습니다.</li>
<li>최적의 성능과 안정성을 보장하기 위해 사용 지침 및 가드레일을 업데이트했습니다.</li>
<li>이제 결정 캡핑 규칙에 Adobe Experience Platform 데이터 세트를 활용할 수 있습니다.</li></ul></p>
<p>자세한 내용은 <a href="../data/lookup-aep-data.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2025년 9월 1일</p>
</td>
</tr>
</tbody>
</table>


### 개선 사항 {#sept-25-9-improvements}

* **API 트리거 캠페인에서 Webhook 지원**\
  이제 API 트리거 캠페인이 Webhook를 지원합니다. 모든 메시지에 대한 실시간 상태 업데이트를 받도록 웹후크 URL을 구성하여 가시성을 향상시키고 원활한 모니터링 및 자동화를 가능하게 합니다. [자세히 보기](../configuration/feedback-webhooks.md)

  사용 가능한 날짜: 2025년 9월 29일

* **SMS 채널에 대한 mTLS 지원**
이제 사용자 정의 SMS 공급자를 설정할 때 상호 TLS(mTLS) 인증을 활성화하는 옵션이 있습니다. 이 옵션을 선택하면 보안 연결이 설정되기 전에 클라이언트와 서버가 서로의 ID를 확인하도록 요구합니다. [자세히 보기](../sms/sms-configuration-custom.md) - 사용 가능한 날짜: 2025년 9월 23일

* **모델 기반 스키마**\
  이제 오케스트레이션된 캠페인에서 관계형 모델링 요구 사항을 지원하기 위해 모델 기반 스키마를 사용할 수 있습니다. [자세히 보기](../orchestrated/gs-schemas.md) - 사용 가능한 날짜: 2025년 9월 23일

* **여정에서 데이터 세트 조회 지원**\
  여정에 새로 추가된 **데이터 세트 조회** 활동을 사용하면 런타임 중에 Adobe Experience Platform 레코드 데이터 세트의 데이터를 동적으로 검색할 수 있습니다. 이 기능을 활용하면 프로필이나 이벤트 페이로드에 없을 수 있는 데이터에 액세스하여 고객 상호 작용이 적시에 적절하게 이루어질 수 있습니다. [자세히 보기](../building-journeys/dataset-lookup.md) - 사용 가능한 날짜: 2025년 9월 23일

  이 활동은 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.

* **여정 사용자 정의 액션에서 리디렉션 지원**\
  이제 여정 사용자 정의 액션에서 리디렉션(302)이 지원됩니다. - 사용 가능한 날짜: 2025년 9월 23일

* **채널 구성 모니터링 경고** - 이제 사용자 정의 하위 도메인 위임 유형을 사용하는 이메일 채널 구성 오류가 발생한 경우 이메일 또는 Journey Optimizer 알림 센터에서 구독 설정을 통해 시스템 경고를 받을 수 있습니다. [자세히 보기](../reports/alerts.md#alert-channel-config-failure) - 사용 가능한 날짜: 2025년 9월 23일

* **원클릭 구독 취소 요청** - Adobe 관리에서 구성한 원클릭 구독 취소 요청을 더욱 강력하게 처리하여 안정적이고 일관된 처리를 가능하게 하는 개선 업데이트를 진행했습니다. - 사용 가능한 날짜: 2025년 9월 23일

* **이제 사용자 정의 인증에서 중첩된 JSON 본문 매개 변수 지원**\
  사용자 정의 액션에 대한 사용자 정의 인증을 구성할 때 중첩 JSON 오브젝트(예: `bodyParams` 내 하위 오브젝트)가 지원됩니다. [자세히 보기](../datasource/external-data-sources.md#custom-authentication-mode) - 사용 가능한 날짜: 2025년 9월 18일

* **시간 단위 캡핑 빈도 재설정** - 이제 채널 규칙 세트에 대해 시간 단위로 캡핑을 적용할 수 있습니다. 이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있으며 1시간을 선택할 수 있습니다(이전에는 3시간). [자세히 보기](../conflict-prioritization/channel-capping.md) - 사용 가능한 날짜: 2025년 9월 17일

* **모든 인바운드 채널에 대한 콘텐츠 베리에이션 시뮬레이션**\
  이전에는 이메일, SMS, 푸시 알림 채널에서만 사용할 수 있던 콘텐츠 베리에이션 시뮬레이션이 이제 모든 인바운드 채널에도 적용됩니다. [자세히 보기](../test-approve/simulate-sample-input.md) - 사용 가능한 날짜: 2025년 9월 17일

* **결정 캡핑 규칙에 표현식 사용** - 이제 결정 항목에 대한 캡핑 규칙의 임계값을 정의하기 위해 자체 표현식을 작성할 수 있습니다. [자세히 보기](../experience-decisioning/items.md#capping) - 사용 가능한 날짜: 2025년 9월 16일

* **동적 도메인 지원** - 이제 Journey Optimizer가 Adobe에서 허용하는 사전 정의된 도메인에 대한 전체/기본 URL 개인화를 지원합니다. [자세히 보기](../personalization/personalization-build-expressions.md#where) - 사용 가능한 날짜: 2025년 9월 12일

  이 기능은 제한된 가용성으로 일부 고객에게만 제공됩니다.

* **Webhooks** - 이 릴리스에서는 사용자 지정 SMS 공급자를 구성할 때 Webhooks에 대해 다음과 같은 개선 사항이 도입되었습니다.

   * 이제 캡처하려는 데이터 유형에 따라 웹후크의 목적( 인바운드 또는 피드백)을 정의할 수 있습니다. [자세히 보기](../sms/sms-configuration-custom.md#webhook) - 사용 가능한 날짜: 2025년 9월 23일

   * 쉽게 설정할 수 있도록 키워드를 구성하는 인터페이스가 개선되었습니다. [자세히 보기](../sms/sms-configuration-custom.md#webhook) - 사용 가능한 날짜: 2025년 9월 23일

* **SMS**

   * 이제 사용자 지정 SMS 공급자를 설정할 때 들어오는 SMS에 인식할 수 없는 키워드가 포함되어 있을 때 사용되는 **Default** 키워드를 정의할 수 있습니다. 특정 작업에 대해 **사용자 지정** 키워드를 만들 수도 있습니다. [자세히 보기](../sms/sms-configuration-custom.md) - 사용 가능한 날짜: 2025년 9월 23일

   * 이제 구성에 명시적으로 정의되지 않은 오타, 단어 또는 문장 등 SMS 메시지를 통해 전송되는 정의되지 않은 인바운드 키워드 응답에 액세스할 수 있습니다. 이 데이터는 13개월 동안 **AJO 전자 메일 추적 경험 이벤트** 데이터 세트 **InboundMessage**&#x200B;에 저장됩니다. Sinch, Infobip 및 사용자 지정 SMS 공급자에서만 사용할 수 있습니다. - 사용 가능한 날짜: 2025년 9월 23일

<!--
* **Approval policy permissions**
  Added an option when creating or setting Approval Policy to prevent Journey/Campaign creators from approving their own objects. [Read more](../test-approve/approval-policies.md) - Availability date: Sept 23, 2025-->

<!--
### Coming soon {#sept-25-9-soon}

In the next few days, the following capabilities and enhancements are scheduled for release. **Information is subject to change**. Updated links, screens, and documentation will be shared once these updates are live in production.

<table>
<thead>
<tr>
<th><strong>New Web Push notifications channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer now supports Web Push notifications, expanding the push channel beyond mobile. You can seamlessly deliver notifications to both mobile and desktop browsers, enabling you to reach customers directly on their devices without requiring an app.</p>
<p>This enhancement allows you to engage users with timely, personalized messages in real time, leveraging the same authoring workflows and targeting capabilities already available for mobile push.</p>
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
<p>Availability date: Sept XX, 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Custom action monitoring and reporting</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Custom action monitoring and reporting is now available. This capability provides better visibility into journey health and execution, including lifecycle status and performance alerts. You can now quickly understand when, where, and why an anomalous situation is occurring in a custom action.</p>
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
<p>Availability date: Sept XX, 2025</p>
</td>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>New source connectors for loyalty apps</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>New source connectors are now available in Adobe Experience Platform for the Talon.One, Capillary, and Kobie loyalty apps. These connectors let you seamlessly stream loyalty data into Adobe Experience Platform and leverage these data in Journey Optimizer.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Landing page custom forms</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>With [!DNL Journey Optimizer], you can now capture profile attributes though your landing pages.</p>
<p>Create, design and manage custom forms tailored to your needs based on a specific dataset. You can then leverage these forms in landing pages to add the profile attributes of your choice into the dataset defined for each form.</p>
<p>This capability is available in Limited Availability. Contact your Adobe representative to gain access.</p>
<p><img src="assets/do-not-localize/forms.gif"/></p>
<p>For more information, refer to the <a href="../landing-pages/lp-forms.md">detailed documentation</a></p>
<p>Availability date: Sept XX, 2025</p>
</td>
</tr>
</tbody>
</table>


* **New Journey Alerts**  
  New pre-configured alerts are available for journeys:

  * Profile Discard Rate Exceeded: Ratio of profile discards to entered profiles over the last 5 mins exceeded threshold.  
  * Custom Action Error Rate Exceeded: Ratio of custom action errors to successful HTTP calls over the last 5 mins exceeded threshold.  
  * Profile Error Rate Exceeded: Ratio of profiles-in-error to entered profiles over the last 5 mins exceeded threshold.


  * [Profile Discard Rate Exceeded](../reports/alerts.md#profile-discard-rate-exceeded): Ratio of profile discards to entered profiles over the last 5 mins exceeded threshold.  
  * [Custom Action Error Rate Exceeded](../reports/alerts.md#custom-action-error-rate-exceeded): Ratio of custom action errors to successful HTTP calls over the last 5 mins exceeded threshold.  
  * [Profile Error Rate Exceeded](../reports/alerts.md#profile-error-rate-exceeded): Ratio of profiles-in-error to entered profiles over the last 5 mins exceeded threshold.

  You can modify threshold values and subscribe to individual journey-level alerts vs globally.

  Availability date: Sept XX, 2025

-->
