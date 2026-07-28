---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer에 대한 사전 릴리스 정보
description: Adobe Journey Optimizer 사전 릴리스 정보
feature: Release Notes
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
hide: true
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2:
  - id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794
  - id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0
  - id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
source-git-commit: c5460f65413375aac7b76a0651c7ed94b0de6a9d
workflow-type: tm+mt
source-wordcount: 1960
ht-degree: 14%

---


# 사전 릴리스 정보 {#e-release-notes}

Adobe Journey Optimizer는 지속적으로 새로운 기능, 기존 기능 개선 및 버그 수정 사항을 제공합니다. 모든 변경 사항은 매월 말 [릴리스 정보](release-notes.md)에 통합됩니다.

<!--
## June '26 pre-release notes {#june-26-rn}

**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published once changes are live in production. While most changes are delivered on the release date, a few may roll out later — refer to the Availability Date listed for each entry for details.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Release date**: June 16-17, 2026

### Journeys {#june-26-journeys}

The following capabilities and improvements are coming to journeys in this release.

<table>
<thead>
<tr>
<th><strong>Channel optimization (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add multiple outbound channels (Email, Push, SMS) to a single journey action and let Journey Optimizer automatically deliver through the best channel for each customer. Three optimization modes are available: manual ranking, customer profile preference (XDM attribute), and AI model-based ranking using propensity scores. When the top-ranked channel is unavailable, the system falls back to the next available channel.</p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../building-journeys/channel-optimization.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>

* **Increased live journey limit and new guardrails** - You can now have up to **200 active journeys**, increased from the previous limit of 100.



### Orchestrated campaigns {#june-26-oc}

The following capabilities and improvements are coming to orchestrated campaigns in this release.

-->

## 2026년 7월 프리릴리스 정보 {#july-26-rn}

**아래 사전 릴리스 정보는 릴리스 공개 당일까지 사전 통지 없이 변경될 수 있습니다**. 링크, 스크린샷 및 업데이트된 설명서는 변경 사항이 프로덕션 환경에 적용된 후 게시됩니다. 대부분의 변경 사항은 릴리스 날짜에 전달되지만 일부는 나중에 롤아웃될 수 있습니다.

[Adobe Experience Platform 사전 릴리스 정보](https://experienceleague.adobe.com/ko/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}도 참조하십시오.

**릴리스 날짜**: 2026년 7월 28~29일

<!--

### Onboarding {#july-26-onboarding}

Journey Optimizer introduces the Onboarding Assistant, a new capability in this release.

<table>
<thead>
<tr>
<th><strong>Onboarding Assistant</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Transitioning to Adobe Journey Optimizer from another marketing platform is easier with guided capabilities that help you move existing email content and journeys into Journey Optimizer. A dedicated workspace lets you reuse what you have instead of rebuilding from scratch.</p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<GIF placeholder: to be added>
<Documentation link: TBD>
</td>
</tr>
</tbody>
</table>

-->

### 여정 {#july-26-journeys}

이 릴리스의 여정에 다음과 같은 개선 사항이 추가되었습니다.

* **여정 시뮬레이션의 외부 대상** - 이제 여정 시뮬레이션이 외부 대상을 지원합니다. CSV 또는 Federated Audience Composition 대상을 타겟팅하는 여정을 시뮬레이션할 때 UI 양식 또는 JSON 가져오기를 통해 해당 대상의 데이터 보강 속성을 직접 모의할 수 있습니다. UI는 여정 논리에 사용된 특정 데이터 보강 속성만 동적으로 표시하므로 실행 전에 의사 결정 분기 및 개인화 규칙을 정확하게 확인할 수 있습니다. <!-- Documentation link: TBD -->

### 캠페인 {#july-26-campaigns}

이 릴리스의 캠페인에 다음과 같은 기능 및 개선 사항이 추가되었습니다.

<table>
<thead>
<tr>
<th><strong>API가 트리거된 이메일의 개인화된 PDF 첨부 파일</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer에서는 API 트리거 캠페인에서 이메일당 최대 5개의 수신자 특정 PDF를 첨부할 수 있습니다. PDF 파일은 Azure 또는 AWS 저장소에서 안전하게 가져오고 전송 시 첨부하며, 각 파일의 위치는 API 페이로드에 직접 전달됩니다. 이렇게 하면 Journey Optimizer에서 게재를 처리하면서 기존 업스트림 문서 생성 시스템이 제자리에 유지될 수 있습니다.</p>
<p>지원되는 사용 사례에는 송장, 명세서, 티켓, 계약서, 배송 라벨 및 수신자마다 다른 유사한 문서가 포함됩니다. 개인화된 PDF 첨부 파일은 API 트리거 캠페인에서만 사용할 수 있으며, 여정 또는 다른 캠페인 유형(작업, 오케스트레이션)에서는 지원되지 않습니다.</p>
<p>PDF 첨부 파일 추가 기능을 통해 더 큰 첨부 파일 볼륨 및 크기가 지원됩니다. 자세한 내용은 Adobe 담당자에게 문의하십시오.</p>
<p></p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>액션 캠페인의 인바운드 경험 시뮬레이션</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 시작하기 전에 작업 캠페인에서 인바운드 채널 작업을 시뮬레이션할 수 있습니다. 시뮬레이션 모드를 사용하여 시뮬레이트된 사용자로 구성을 테스트하고 생성된 URL 및 QR 코드를 포함한 렌더링된 경험을 미리 보면 규칙, 의사 결정 및 컨텐츠 렌더링의 엔드 투 엔드를 확인할 수 있습니다.</p>
<p>이 기능은 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **캠페인용 폴더** - 이제 캠페인을 폴더로 구성하여 인터페이스에서 탐색 및 관리를 개선할 수 있습니다. 이 기능은 작업 및 API 트리거 캠페인에만 사용할 수 있습니다. <!-- Documentation link: TBD -->

* **캠페인의 기본 실행 필드 재정의** - 이전에는 여정 수준에서 사용할 수 있었지만, 이제 캠페인 매개 변수에서 이메일, SMS 및 WhatsApp 게재에 대해 전역으로 설정된 기본 실행 필드를 재정의할 수 있습니다. <!-- Documentation link: TBD -->

* **캠페인 대시보드의 브랜드 일관성 점수** - 이제 캠페인 대시보드에서 직접 브랜드 일관성 점수를 평가하여 콘텐츠가 브랜드에 부합하는지 확인할 수 있습니다. 이렇게 하면 콘텐츠 디자이너를 열지 않고도 지침을 한 눈에 확인할 수 있습니다. <!-- Documentation link: TBD -->

### 오케스트레이션된 캠페인 {#july-26-oc}

이 릴리스의 오케스트레이션된 캠페인에 다음과 같은 개선 사항이 추가되었습니다.

* **오케스트레이션된 캠페인 전환 보기** - 기존 **오케스트레이션된 캠페인에서 파일 보기** 옵션을 대체할 새 **오케스트레이션된 캠페인 전환 보기** 권한을 추가했습니다. 이 변경 사항을 사용하면 개인 식별 정보 규정 준수를 지원하기 위해 캠페인 전환 내에서 미리 보기 결과를 숨길 수 있습니다.

<!--
* **Send messages in waves** - You can now schedule outbound messages from orchestrated campaigns to be delivered in controlled batches over time. Ideal for high-volume or time-sensitive campaigns, wave sending also supports better deliverability and helps maintain a strong sender reputation by reducing the risk of being flagged as spam.
-->

<!--
### Optimization {#july-26-optimization}

<table>
<thead>
<tr>
<th><strong>Channel optimization</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now configure a journey or campaign action to include multiple outbound channels (Email, Push, SMS) and let Journey Optimizer automatically deliver through the best channel for each customer. Three optimization modes are available:</p>
<ul>
<li>Manual ranking: specify your preferred channel order.</li>
<li>Customer preference: use the customer's preferred channel from their profile (Experience Data Model Consents & Preferences attribute).</li>
<li>AI model-based ranking: use machine learning propensity scores to infer the most effective channel per customer.</li>
</ul>
<p>When the top-ranked channel is unavailable (not opted-in, frequency-capped, or not configured), the system falls back to the next available channel.</p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
</td>
</tr>
</tbody>
</table>
-->

<!--
<table>
<thead>
<tr>
<th><strong>Quiet Hours support for orchestrated campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now apply quiet hours to Orchestrated campaigns. Quiet hours let you define time-based exclusions to prevent messages from being sent during specific periods, helping you respect customer preferences and compliance requirements across campaign orchestration use cases.</p>
<Documentation link: TBD>
</td>
</tr>
</tbody>
</table>

* **Ability to Manage Profile Target Dimensions** - You can now delete a Profile Target Dimension or edit and swap its configured identity namespace, providing greater control and flexibility over your data setups.

* **Support for Line** - You can now add LINE actions directly into your Orchestrated campaigns. This new activity allows you to build and deliver highly personalized content, including text, stickers, images, videos, location data, and rich Flex Messages, to engage your customers seamlessly on the LINE platform. This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.

* **New Orchestrated campaigns public APIs** - New API specifications are now available for Orchestrated campaigns. These APIs allow you to programmatically create, manage, and trigger orchestrated campaigns, enabling deeper integration with external systems and automation pipelines.

* **Personalize email sender details per recipient and campaign** - Orchestrated campaigns now support personalization of email header fields, including From name, From address, and Reply-To, using profile attributes or relational data. This allows sender details to reflect the relevant advisor, location, or branch for each recipient, rather than routing all sends through a single corporate address. Header values can be set at the channel level and overridden per campaign using contextual data for more precise control. Documentation link: TBD

* **Target dimension simplification in Orchestrated campaigns** - The active targeting dimension is now shown on the workflow canvas, so you can see which dimension is used by a channel activity. The multi-entity segmentation flow is simpler as you no longer need a separate "Change dimension" activity. Moreover, you can now choose explicitly whether messages are sent at the profile level or at a secondary dimension level.

-->

### 채널 {#july-26-channels}

이 릴리스의 채널에 다음과 같은 기능 및 개선 사항이 추가되었습니다.

<table>
<thead>
<tr>
<th><strong>사용자 지정 아웃바운드 채널</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer은 이제 관리자가 WeChat, KakaoTalk, Messenger 또는 독점 공급자와 같은 아웃바운드 HTTP 기반 메시징 채널을 코드 없는 채널 빌더를 통해 Journey Optimizer으로 직접 가져올 수 있는 새로운 기능인 사용자 지정 채널을 도입했습니다.</p >
<p>구성하고 나면 캠페인, 여정 및 오케스트레이션된 캠페인 전반에서 기본 채널과 동일한 전체 기능 세트를 사용하여 사용자 정의 채널을 사용할 수 있습니다. 표현식 편집기를 사용한 개인화, 콘텐츠 실험, 미리보기 및 증명, 기본 보고, 동의 및 거버넌스 시행.</p>
<p>이렇게 하면 이전에 여정 지정 작업으로 해결했던 공백이 해소되며, 이는 채널로만 제한되고 전용 채널 기능이 부족합니다.</p>
<p>사용자 지정 아웃바운드 채널은 현재 제한된 가용성으로 사용할 수 있습니다. 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **WhatsApp 채널: WhatsApp 흐름 템플릿 지원** - 이제 Adobe Journey Optimizer에서 WhatsApp 흐름 템플릿을 전송하여 설문 조사 및 잠재 고객 캡처와 같은 대화형 다중 화면 경험을 제공할 수 있습니다. 응답은 제출 시 캡처되어 새 Journey Optimizer 채널 추적 이벤트 데이터 세트에 원시 JSON 페이로드로 저장됩니다. <!-- Documentation link: TBD -->

* **처리량을 위한 성능 추가 기능 - 푸시** - API 트리거 캠페인에서 새로운 처리량 트랜잭션 메시지 모드를 사용할 수 있습니다. 이 모드는 대규모 실시간 트랜잭션 메시지 전송을 위해 설계되었으며 더 높은 가용성으로 초당 최대 5,000개의 트랜잭션을 지원합니다. 이전에는 이메일 채널에서만 사용할 수 있었지만, 이제 이 기능은 Adobe 고처리량 트랜잭션 메시지 추가 기능 서비스를 구입한 조직의 푸시 채널에서도 사용할 수 있습니다. 자세한 내용은 Adobe 담당자에게 문의하십시오. <!-- Documentation link: TBD -->

* **향상된 사용자 지정 공급자 통합 - Mobile** - 이제 사용자 지정 공급자 통합을 통해 주요 메시지 및 헤더 업데이트를 통해 확장된 유연성을 제공합니다.

  * 헤더 사용자 정의: 이제 기본 Content-Type 헤더 값을 편집하고 최대 10개의 사용자 정의 헤더 매개 변수를 추가할 수 있습니다.

  * SMS 페이로드 지원: encode64를 포함하여 SMS 페이로드 내에 Adobe Journey Optimizer 도우미 기능에 대한 지원이 추가되었습니다.

### 결정 {#july-26-decisioning}

이 릴리스의 Decisioning에 다음과 같은 개선 사항이 추가되었습니다.

* **자연어 식에서 의사 결정 규칙 만들기** - 이제 일반 언어로 만들려는 의사 결정 규칙을 설명하고 AI가 자동으로 생성하도록 할 수 있습니다. 이 기능은 Adobe AI 기능에 액세스하는 고객이 사용할 수 있습니다.

  이 기능은 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 액세스 권한을 얻으려면 Adobe 담당자에게 문의하십시오. <!-- Documentation link: TBD -->

* **의사 결정 규칙 및 등급 수식 시뮬레이션** - 이제 규칙 또는 수식 편집기에서 직접 의사 결정 규칙 및 등급 수식을 시뮬레이션할 수 있습니다. 수동 테스트 변형을 추가하거나 AI를 사용하여 생성한 다음 테스트 데이터에 대해 표현식을 실행하여 자격 조건을 확인하고 등급 결과를 검토한 후 프로덕션에 배포합니다. Adobe AI 기능에 액세스하는 고객은 변형 생성을 사용할 수 있습니다.

  이 기능은 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 액세스 권한을 얻으려면 Adobe 담당자에게 문의하십시오. <!-- Documentation link: TBD -->

* **오퍼 수준의 Personalization** - 이제 프로필, 컨텍스트 및 대상 데이터를 사용하여 게재 시 의사 결정 항목 사용자 지정 특성을 개인화할 수 있습니다. 이를 통해 사소한 콘텐츠 변형에 대해 중복 오퍼를 유지할 필요가 없으므로 마케터는 보다 적고 유연한 결정 항목을 관리할 수 있습니다. <!-- Documentation link: TBD -->

<!--
* **Placement-level frequency capping in Decisioning** - Frequency capping rules in Decisioning can now be scoped to individual placements, giving you finer control over how often an offer is shown in a given surface. Two modes are available: placement-specific capping (define a cap that applies only when the offer is displayed in a selected placement) and per-placement capping (apply a cap independently across every placement where the offer appears, so each placement maintains its own capping counter). Documentation link: TBD
-->

### 콘텐츠 관리 {#july-26-content}

이 릴리스의 콘텐츠 관리에 다음과 같은 개선 사항이 추가되었습니다.

* **전자 메일 서식 파일의 `<head>`에서 식 조각 지원** - 이제 전자 메일 서식 파일의 `<head>`에서 식 조각을 사용할 수 있습니다. 이를 통해 스타일링 또는 사용자 지정 코드를 단일 조각에 중앙 집중화하고 여러 템플릿에서 재사용할 수 있습니다. 조각을 업데이트하고 다시 게시하면 이를 참조하는 템플릿에서 빌드된 모든 이메일이 자동으로 최신 코드를 상속하므로 각 이메일을 개별적으로 수동으로 업데이트할 필요가 없습니다. <!-- Documentation link: TBD -->

* **&quot;AI Assistant&quot;가 &quot;콘텐츠 생성&quot;으로 이름이 변경되었습니다** - AI Assistant의 이름이 Adobe Journey Optimizer 전체에서 콘텐츠 생성으로 변경되었습니다. 이 업데이트는 이름 지정 및 용어로 제한되며 기능 변경 사항이 도입되지 않았습니다. 콘텐츠 생성, 이미지 생성, 개인화 표현식 및 콘텐츠 실험에 대한 탐색 레이블, 단추, 메뉴 및 대화 상자의 이름이 &quot;AI Assistant&quot;에서 &quot;콘텐츠 생성&quot;으로 변경되었습니다. <!-- Documentation link: TBD -->

* **AI 콘텐츠 생성을 위한 유연한 이미지 소싱** - 이제 Journey Optimizer에서 콘텐츠를 생성하면 Adobe Experience Manager Assets Essentials 등에서 브랜드로 승인된 이미지를 직접 소싱합니다. 균형을 제어하는 모드는 Assets(Digital Asset Management-sourced, default), Balanced(Digital Asset Management-first, AI 채우기) 및 Creative(AI-first)입니다. 이렇게 하면 여정 및 캠페인에 대해 정확하고 브랜드 규정을 준수하며 프로덕션에 바로 사용할 수 있습니다. <!-- Documentation link: TBD -->

* **다국어 개선** - 이제 언어 설정을 기존 활성 설정에서 복제할 수 있으므로 더 이상 구성을 완전히 다시 빌드하여 변경할 필요가 없습니다. 언어 설정을 작성하는 동안 한 로케일에서 다른 로케일로 조건을 복사할 수도 있으므로 여러 언어를 사용하는 사이트에 대한 설정을 간소화할 수 있습니다.

<!--
### Integrations {#july-26-integrations}

The following improvements have been added to integrations in this release.

* **Real-time countdown timers for Adobe Experience Manager Dynamic Media integration** - Marketers can now build countdown timers as Dynamic Media templates in Adobe Experience Manager and pull them directly into Journey Optimizer. Timers render live at the moment of open, so every recipient sees an accurate countdown, not a static image. Configure dates, styling, and fallback values right within the Journey Optimizer editor to power flash sales and limited-time offers. [Documentation link: TBD]
-->

### 개인화 {#july-26-personalization}

이 릴리스의 개인화에 다음과 같은 개선 사항이 추가되었습니다.

* **전체/기본 URL 개인화를 위한 도메인 관리** - 이제 Adobe 지원에 문의하지 않고도 Adobe Journey Optimizer의 관리 설정에서 직접 전체 및 기본 URL 개인화를 위한 승인된 도메인을 만들고 관리할 수 있습니다. <!-- Documentation link: TBD -->

* **개인화 식에 새 도우미 함수** - 이제 개인화 식에 새 도우미 함수를 사용할 수 있습니다.

  * `appendQueryParams`: 쿼리 매개 변수를 URL에 추가하거나 키가 이미 있는 경우 바꿉니다.
  * `dateBetween`: 날짜가 시작 및 종료 날짜 범위(포함)에 속하는지 확인합니다.
  * `equalsAnyIgnoreCase`: 문자열이 제공된 값과 일치하면 true를 반환하고 대/소문자를 무시합니다.
  * `getUrlFragment`: URL의 조각 부분(# 다음 부분)을 추출합니다.
  * `join`: 구분 기호를 사용하여 배열 요소를 단일 문자열로 연결합니다.
  * `decode64`: Base64로 인코딩된 문자열을 디코딩합니다. 입력이 유효한 Base64가 아닌 경우 원래 입력 문자열은 변경되지 않고 반환됩니다.
  * `parseJson`: JSON 문자열을 템플릿에서 사용할 수 있는 구조화된 변수로 구문 분석합니다.
  * `valueAtPath`: 배열 또는 컬렉션에서 특정 요소를 추출하기 위한 선택적 인덱싱을 사용하여 데이터 경로의 값을 템플릿 변수에 할당합니다.

  `concat` 함수도 향상되었으며 이제 두 개 이상의 인수를 지원합니다.

  또한 다음 템플릿 마이그레이션 기능 을 사용하여 기존 템플릿을 Journey Optimizer으로 마이그레이션할 수 있습니다.

  * `ampCompare`: 지정된 비교 연산자를 사용하여 두 값을 비교합니다.
  * `ampSubstr`: 지정된 시작 및 끝 인덱스 사이의 문자열 부분을 반환합니다.
  * `compareTo`: 두 문자열을 사전적으로 비교합니다.

<!-- Documentation link: TBD -->

### 이메일 디자이너 {#july-26-email}

이 릴리스의 이메일 채널에 다음 기능이 추가되었습니다.

<table>
<thead>
<tr>
<th><strong>이메일 디자이너의 모듈</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 이메일 디자이너에 헤더, 제품 카드, 정보 블록, 바닥글과 같은 바로 사용할 수 있는 레이아웃 모듈 라이브러리가 포함되어 있어 이메일 캔버스에 직접 끌어다 놓을 수 있습니다.</p>
<p>각 모듈은 편집 가능한 속성(이미지, 제목, 텍스트, 버튼, 링크)으로 사전 구성되어 있으며 WYSIWYG 인터페이스를 통해 완벽하게 사용자 정의할 수 있으므로 처음부터 구조를 만들 필요 없이 이메일 작성 속도를 높일 수 있습니다.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>


### 관리 {#july-26-administration}

이 릴리스의 관리에 다음 기능이 추가되었습니다.

<table>
<thead>
<tr>
<th><strong>웹 응용 프로그램 방화벽 IP 허용 목록</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer은 이제 랜딩 페이지에 대한 웹 애플리케이션 방화벽 IP 허용 목록을 지원하므로 조직에서 모든 수신 요청이 구성된 웹 애플리케이션 방화벽 인프라를 통해서만 라우팅되도록 할 수 있습니다. 이 향상된 기능을 통해 고객은 웹 애플리케이션 방화벽 계층을 무시하는 직접 요청을 거부하도록 Journey Optimizer을 구성할 수 있으므로 Imperva와 같은 도구에 정의된 보안 정책이 일관되게 적용됩니다.</p>
<p>이 기능은 엄격한 네트워크 액세스 요구 사항을 가진 기업의 보안 태세를 강화하여 Journey Optimizer이 호스팅하는 랜딩 페이지로의 트래픽 흐름을 완벽하게 제어합니다.</p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

### 사용성 개선 사항 {#july-26-usability}

이번 릴리스에는 다음과 같은 사용 편의성 개선 사항이 적용되었습니다.

* **콘텐츠 템플릿의 SMS, 푸시, 인앱 및 Codebase 채널에 대한 빠른 실행 바로 가기** - 이제 콘텐츠 템플릿 목록의 **추가 작업** 단추에서 채널별 바로 가기를 추가로 사용할 수 있습니다. SMS 템플릿의 경우 메시지를 빠르게 편집하거나 문자 수/세그먼트를 확인합니다. 푸시 템플릿의 경우 제목, 본문 또는 미디어를 편집합니다. 인앱 템플릿의 경우 메시지 헤더, 메시지 본문 또는 미디어 URL을 편집합니다. 코드베이스 채널 템플릿의 경우 코드를 직접 편집합니다. 이러한 단축키는 이미 사용 가능한 이메일 채널 빠른 실행 단축키를 확장합니다. <!-- Documentation link: TBD -->

* **콘텐츠 테스트를 위한 새로운 콘텐츠 시뮬레이션 경험** - **콘텐츠 시뮬레이션** 워크플로에서는 새롭게 디자인된 경험을 도입했습니다. 이제 모든 변형을 한 번에 한 가지 변형인 보기를 대체하여 스크롤 가능한 단일 그리드(나란히, 스택 또는 래핑된 레이아웃)에서 함께 렌더링합니다. 단일 하단 작업 표시줄은 테스트 변형 간 탐색, 확대/축소, 뷰포트 전환(데스크탑/모바일), 로케일 전환, 샘플 입력 추가, AI를 통한 변형 생성, 시뮬레이션된 사용자 선택 및 저장, 변형 가져오기 또는 내보내기를 통합합니다. 왼쪽 레일을 제거하고 추가 헤더 레이어를 축소하면 미리보기에 훨씬 더 많은 공간이 제공됩니다. 하단 작업 표시줄의 **클래식 경험으로 전환** 옵션을 사용하면 언제든지 이전 경험으로 되돌릴 수 있습니다. <!-- Documentation link: TBD -->
