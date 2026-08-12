---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer에 대한 사전 릴리스 정보
description: Adobe Journey Optimizer 사전 릴리스 정보
feature: Release Notes
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2: id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
source-git-commit: f453579de2b5edac0e8ac8cbcf31d48bce8467ad
workflow-type: tm+mt
source-wordcount: 1282
ht-degree: 18%

---


# 사전 릴리스 정보 {#e-release-notes}

Adobe Journey Optimizer는 지속적으로 새로운 기능, 기존 기능 개선 및 버그 수정 사항을 제공합니다. 모든 변경 사항은 매월 말 [릴리스 정보](release-notes.md)에 통합됩니다.

## 2026년 8월 프리릴리스 정보 {#august-26-rn}

**아래 사전 릴리스 정보는 릴리스 공개 당일까지 사전 통지 없이 변경될 수 있습니다**. 링크, 스크린샷 및 업데이트된 설명서는 변경 사항이 프로덕션 환경에 적용된 후 게시됩니다. 대부분의 변경 사항은 릴리스 날짜에 전달되지만 일부는 나중에 롤아웃될 수 있습니다.

[Adobe Experience Platform 사전 릴리스 정보](https://experienceleague.adobe.com/ko/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}도 참조하십시오.

**릴리스 날짜**: 2026년 8월 18~19일

<!--
### Onboarding {#august-26-onboarding}

The following capability is coming to onboarding in this release.

<table>
<thead>
<tr>
<th><strong>Guided capabilities for onboarding emails and journeys (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Transitioning to Adobe Journey Optimizer from another marketing platform is easier with guided capabilities that help you move existing email content and journeys into Journey Optimizer. A dedicated workspace lets you reuse what you have instead of rebuilding from scratch.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<GIF placeholder: to be added>
<Documentation link: TBD>
</td>
</tr>
</tbody>
</table>

-->

### 여정 {#august-26-journeys}

이번 릴리스에서는 다음과 같은 기능 및 개선 사항이 여정에 추가됩니다.

<table>
<thead>
<tr>
<th><strong>여정 수준 보류(제한된 가용성)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 여정 속성에서 직접 여정에 대한 홀드아웃 그룹을 구성할 수 있습니다. 홀드아웃은 여정 입력에서 제외되고 커뮤니케이션을 수신하지 않는 타겟 대상의 구성 가능한 백분율입니다. 홀드아웃 프로필을 Customer Journey Analytics 보고의 활성 프로필과 비교하여 여정이 제공하는 증분 상승도 - 실제 영향을 측정할 수 있습니다.</p>
<p> 이 기능은 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **여정 표현식 편집기에 새 dateDiff 함수 추가** - 이제 여정 표현식 편집기에 두 날짜의 일 수 차이를 계산하는 `dateDiff` 함수가 포함됩니다. 이 기능은 기한 만들기, 고객 라이프사이클 기간 계산 또는 여정 조건에서 카운트다운 타이머 작성과 같은 시간 기반 논리에 유용합니다. <!-- Documentation link: TBD -->

* **여정 헤더의 시작 및 종료 날짜** - 여정에 시작 및/또는 종료 날짜가 구성되면 상태 배지 옆의 여정 헤더에 표시됩니다. 표시된 레이블은 각 날짜가 예정된 날짜인지 또는 이미 지난 날짜인지에 따라 조정됩니다. <!-- Documentation link: TBD -->

### 캠페인 {#august-26-camp}

이 릴리스의 Campaign에는 다음과 같은 기능 및 개선 사항이 적용됩니다.

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
<p>이 기능은 현재 개인 베타 버전으로 제한된 조직 세트에서 사용할 수 있습니다. 더 많은 내용은 Adobe 담당자에게 문의하십시오.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **작업 캠페인 작성 흐름 재디자인** - Adobe Journey Optimizer 작업 캠페인 작성 흐름이 훨씬 더 직관적이고 효율적이며 원활한 사용자 경험을 제공하도록 재디자인되었습니다.

* **작업 캠페인용 폴더** - 이제 작업 캠페인을 폴더로 구성하여 인터페이스에서 탐색 및 관리를 개선할 수 있습니다. <!-- Documentation link: TBD -->

<!--* **Brand alignment score in Action Campaign dashboard** - You can now assess your brand alignment score directly within your Action Campaign dashboard to ensure content stays on-brand. This allows you to verify guidelines at a glance without having to open the content designer.  Documentation link: TBD -->

* **작업 캠페인의 기본 실행 필드 재정의** - 이전에는 여정 수준에서 사용할 수 있었지만, 이제 작업 캠페인 매개 변수에서 이메일, SMS 및 WhatsApp 게재에 대해 전역적으로 구성된 기본 실행 필드를 재정의할 수 있습니다. <!-- Documentation link: TBD -->

### 오케스트레이션된 캠페인 {#august-26-oc}

이 릴리스의 오케스트레이션된 캠페인에는 다음과 같은 기능 및 개선 사항이 적용되었습니다.

<table>
<thead>
<tr>
<th><strong>업무 중지 시간 지원</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 자동 시간 을 적용할 수 있습니다. 방해 금지 - 특정 기간 동안 메시지가 전송되지 않도록 시간 기반 제외 항목을 정의할 수 있으므로, 캠페인 오케스트레이션 사용 사례 전반에서 고객 선호도 및 규정 준수 요구 사항을 준수할 수 있습니다.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>LINE 채널 지원(제한된 가용성)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 사용자 지정 아웃바운드 채널 기능 릴리스를 통해 캠페인에 직접 LINE 작업을 추가할 수 있습니다. 이 새로운 활동을 통해 텍스트, 스티커, 이미지, 비디오, 위치 데이터 및 풍부한 Flex 메시지를 비롯한 고도로 개인화된 콘텐츠를 구축 및 전달하여 LINE 플랫폼에서 고객을 원활하게 참여시킬 수 있습니다. 이 기능은 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **프로필 대상 차원을 관리하는 기능** - 이제 프로필 대상 Dimension을 삭제하거나 구성된 ID 네임스페이스를 편집 및 교환하여 데이터 설정을 보다 유연하게 제어할 수 있습니다. <!-- Documentation link: TBD -->

<!-- * **New public APIs** - New API specifications are now available. These APIs allow you to programmatically create, manage, and trigger orchestrated campaigns, enabling deeper integration with external systems and automation pipelines. Documentation link: TBD -->

* **받는 사람 및 캠페인별 전자 메일 보낸 사람 세부 정보 개인화(제한된 가용성)** - 이제 오케스트레이션된 캠페인에서 프로필 특성 또는 관계 데이터를 사용하여 보낸 사람 이름, 보낸 사람 전자 메일 접두사, 회신 주소 및 회신 전자 메일을 포함한 전자 메일 머리글 필드의 개인화를 지원합니다. 이 작업을 통해 모든 발송물을 단일 회사 주소를 통해 보내는 대신, 발신자 세부 정보에 각 수신자에게 적합한 담당자, 위치 또는 지점을 반영할 수 있습니다. 헤더 값은 채널 수준에서 설정할 수 있으며, 세밀한 제어를 위해 컨텍스트 데이터를 사용하여 캠페인별로 재정의할 수 있습니다.
이 기능은 일부 조직에서만 사용할 수 있습니다(제한된 가용성).
  <!-- Documentation link: TBD -->

* **대상 차원 단순화** - 이제 활성 타깃팅 차원이 워크플로우 캔버스에 표시되므로 채널 활동에서 사용하는 차원을 확인할 수 있습니다. 다중 엔티티 세분화 흐름은 더 이상 별도의 &quot;차원 변경&quot; 활동이 필요하지 않으므로 더 간단합니다. 또한 이제 메시지가 프로필 수준에서 전송되는지 또는 보조 차원 수준에서 전송되는지를 명시적으로 선택할 수 있습니다. <!-- Documentation link: TBD -->

* **웨이브를 사용하여 보내기** - 이제 아웃바운드 메시지를 시간에 따라 제어된 배치로 전달하도록 예약할 수 있습니다. 대량 또는 시간에 민감한 캠페인에 적합한 웨이브 전송은 더 나은 전달성을 지원하며, 스팸으로 플래그가 지정될 위험을 줄여 강력한 발신자 평판을 유지하는 데도 도움이 됩니다. <!-- Documentation link: TBD -->

### 채널 {#august-26-channels}

이 릴리스의 채널에는 다음과 같은 기능 및 개선 사항이 적용됩니다.

<table>
<thead>
<tr>
<th><strong>웹 채널에서 의사 결정 지원</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 웹 채널에 의사 결정을 사용할 수 있습니다. 웹 시각적 편집기에서 직접 의사 결정 정책을 사용하여 각 방문자에게 가장 관련성이 높은 오퍼를 전달할 수 있습니다.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>


* **처리량을 위한 성능 추가 기능 - 푸시** - API 트리거 캠페인에서 새로운 처리량 트랜잭션 메시지 모드를 사용할 수 있습니다. 이 모드는 대규모 실시간 트랜잭션 메시지 전송을 위해 설계되었으며 더 높은 가용성으로 초당 최대 5,000개의 트랜잭션을 지원합니다. 이전에는 이메일 채널에서만 사용할 수 있었지만, 이제 이 기능은 Adobe 고처리량 트랜잭션 메시지 추가 기능 서비스를 구입한 조직의 푸시 채널에서도 사용할 수 있습니다. 자세한 내용은 Adobe 담당자에게 문의하십시오. <!-- Documentation link: TBD -->

### 결정 {#august-26-decisioning}

이 릴리스의 Decisioning에는 다음과 같은 개선 사항이 적용됩니다.

* **의사 결정의 배치 수준 빈도 제한** - 이제 의사 결정의 빈도 제한 규칙을 개별 배치로 지정할 수 있으므로 오퍼가 지정된 표면에 표시되는 빈도를 보다 세밀하게 제어할 수 있습니다. 두 가지 모드를 사용할 수 있습니다. 배치별 캡핑은 오퍼가 선택한 배치에 표시될 때만 적용되는 캡을 정의하고, 배치별 캡핑은 오퍼가 나타나는 모든 배치에 독립적으로 캡을 적용하므로 각 배치는 자체 캡핑 카운터를 유지합니다. 배치 관련 한도 설정은 Adobe Experience Platform 데이터 기반의 규칙을 사용하여 설정된 오퍼에는 적용되지 않습니다. <!-- Documentation link: TBD -->

* **시각적 조각의 미러 페이지** - 이제 시각적 조각에 미러 페이지를 삽입할 수 있습니다. Decisioning을 활용하는 이메일 캠페인에서 조각을 사용하는 경우에도 Decisioning 속성이 미러 페이지 링크에서 올바르게 렌더링됩니다. 속성을 표시하려면 조각을 게시하기 전에 시각적 조각에 미러 페이지를 추가해야 합니다. <!-- Documentation link: TBD -->

### 이메일 디자이너 {#august-26-email}

이 릴리스의 이메일 Designer에는 다음과 같은 개선 사항이 적용됩니다.

* **전자 메일 Designer의 새 테이블 구성 요소** - 이제 전자 메일 Designer에 기본 제공 테이블 구성 요소가 포함되어 있으므로 전자 메일 내에서 직접 행 및 열의 콘텐츠를 구성할 수 있습니다. 구성 요소를 캔버스에 끌어다 놓고, 행과 열의 수를 사용자 지정하고, 각 셀의 스타일을 독립적으로 지정하여 사용자 지정 HTML에 의존하지 않고 명확하고, 정리된 레이아웃을 만듭니다. <!-- Documentation link: TBD -->

### 관리 {#august-26-administration}

이 릴리스에서는 다음과 같은 개선 사항이 적용되었습니다.

* **사용자 지정 하위 도메인에 대한 피드백 루프 OTP 프로세스** - 제품 UI 내에서 Yahoo sender 허브 OTP(일회성 암호)를 직접 표시하여 피드백 루프(FBL) 사용자 지정 하위 도메인 구성 프로세스가 개선되었습니다. 이제 사용자는 Yahoo 발신자 허브 도메인 소유권 확인 중에 생성된 OTP를 자동으로 검색하고 표시할 수 있습니다. <!-- Documentation link: TBD -->

<!--

## June '26 pre-release notes {#june-26-rn}

**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published once changes are live in production. While most changes are delivered on the release date, a few may roll out later — refer to the Availability Date listed for each entry for details.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Release date**: June 16-17, 2026

### Journeys {#june-26-journeys}

The following capabilities and improvements are coming to journeys in this release.

* **Increased live journey limit and new guardrails** - You can now have up to **200 active journeys**, increased from the previous limit of 100.



### Orchestrated campaigns {#june-26-oc}

The following capabilities and improvements are coming to orchestrated campaigns in this release.

-->


