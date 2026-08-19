---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer에 대한 사전 릴리스 정보
description: Adobe Journey Optimizer 사전 릴리스 정보
feature: Release Notes
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2:
  - id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794
  - id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0
  - id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
source-git-commit: 556acc780e4077e129394a6e8c8fdf93e814e426
workflow-type: tm+mt
source-wordcount: 790
ht-degree: 17%

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

### 채널 {#august-26-channels}

이 릴리스의 캠페인에는 다음과 같은 개선 사항이 적용됩니다.

* **라이브 활동 실행 메타데이터(executionMetadata)** - 이제 API로 트리거된 라이브 활동 캠페인(트랜잭션 및 마케팅)에서 각 수신자의 선택적 executionMetadata 필드를 지원합니다. 이렇게 하면 주문 ID, 충성도 계층 또는 지역 코드와 같은 사용자 지정 키/값 데이터를 실행에 첨부할 수 있습니다.

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

### 결정 {#august-26-decisioning}

이 릴리스의 Decisioning에는 다음과 같은 기능과 개선 사항이 적용되었습니다.

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

* **의사 결정의 배치 수준 빈도 제한** - 이제 의사 결정의 빈도 제한 규칙을 개별 배치로 지정할 수 있으므로 오퍼가 지정된 표면에 표시되는 빈도를 보다 세밀하게 제어할 수 있습니다. 두 가지 모드를 사용할 수 있습니다. **배치별 한도**(오퍼가 선택한 배치에 표시될 때만 적용되는 한도 정의) 및 **배치당 한도**(오퍼가 나타나는 모든 배치에 독립적으로 적용되는 한도 정의). 따라서 각 배치는 자체 한도 카운터를 유지합니다. 배치 관련 한도 설정은 Adobe Experience Platform 데이터 기반의 규칙을 사용하여 설정된 오퍼에는 적용되지 않습니다. <!-- Documentation link: TBD -->

### 콘텐츠 관리 {#august-26-content}

이 릴리스에서는 콘텐츠 관리에 대해 다음과 같은 개선 사항이 적용되었습니다.

* **콘텐츠 변형 크기 경고** - 이제 Journey Optimizer은 콘텐츠 변형이 권장 크기 임계값(템플릿 및 메시지: 1200KB, 조각: 700KB, 랜딩 페이지: 1000KB)을 초과할 때 소프트 제한 경고를 표시합니다. 저장 및 게시가 차단되지 않습니다.

* **콘텐츠의 조각 수 제한** - 이제 Journey Optimizer이 변형당 최대 60개, 단일 메시지의 모든 변형에서 최대 120개의 콘텐츠 조각 내에서 사용된 고유 조각 수를 확인합니다. 경고는 각 제한의 75%에 표시됩니다. 엄격한 제한에 도달하면 게시가 차단됩니다.

<!--

## June '26 pre-release notes {#june-26-rn}

**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published once changes are live in production. While most changes are delivered on the release date, a few may roll out later — refer to the Availability Date listed for each entry for details.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/ko/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Release date**: June 16-17, 2026

### Journeys {#june-26-journeys}

The following capabilities and improvements are coming to journeys in this release.

* **Increased live journey limit and new guardrails** - You can now have up to **200 active journeys**, increased from the previous limit of 100.



### Orchestrated campaigns {#june-26-oc}

The following capabilities and improvements are coming to orchestrated campaigns in this release.

-->


