---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer에 대한 사전 릴리스 정보
description: Adobe Journey Optimizer 사전 릴리스 정보
feature: Release Notes
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
hide: true
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2: id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
source-git-commit: 6e665528805269903885ba9ba3f958de3f4374f4
workflow-type: tm+mt
source-wordcount: 331
ht-degree: 32%

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


### 캠페인 {#july-26-campaigns}

이 릴리스의 캠페인에 다음과 같은 기능 및 개선 사항이 추가되었습니다.

<!--
<table>
<thead>
<tr>
<th><strong>Inbound experience simulation in Action campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now simulate inbound channel actions in Action campaigns before going live. Use simulation mode to test your configuration with simulated users and preview the rendered experience, including a generated URL and QR code, so you can validate rules, decisioning, and content rendering end-to-end.</p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
</td>
</tr>
</tbody>
</table>
-->

### 오케스트레이션된 캠페인 {#july-26-oc}

이 릴리스의 오케스트레이션된 캠페인에 다음과 같은 개선 사항이 추가되었습니다.

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

* **Send messages in waves** - You can now schedule outbound messages from orchestrated campaigns to be delivered in controlled batches over time. Ideal for high-volume or time-sensitive campaigns, wave sending also supports better deliverability and helps maintain a strong sender reputation by reducing the risk of being flagged as spam.

-->

### 채널 {#july-26-channels}

이 릴리스의 채널에 다음과 같은 기능 및 개선 사항이 추가되었습니다.

### 결정 {#july-26-decisioning}

이 릴리스의 Decisioning에 다음과 같은 개선 사항이 추가되었습니다.

<!--
* **Placement-level frequency capping in Decisioning** - Frequency capping rules in Decisioning can now be scoped to individual placements, giving you finer control over how often an offer is shown in a given surface. Two modes are available: placement-specific capping (define a cap that applies only when the offer is displayed in a selected placement) and per-placement capping (apply a cap independently across every placement where the offer appears, so each placement maintains its own capping counter). Documentation link: TBD
-->

### 콘텐츠 관리 {#july-26-content}

이 릴리스의 콘텐츠 관리에 다음과 같은 개선 사항이 추가되었습니다.

<!--
### Integrations {#july-26-integrations}

The following improvements have been added to integrations in this release.

* **Real-time countdown timers for Adobe Experience Manager Dynamic Media integration** - Marketers can now build countdown timers as Dynamic Media templates in Adobe Experience Manager and pull them directly into Journey Optimizer. Timers render live at the moment of open, so every recipient sees an accurate countdown, not a static image. Configure dates, styling, and fallback values right within the Journey Optimizer editor to power flash sales and limited-time offers. [Documentation link: TBD]
-->

### 개인화 {#july-26-personalization}

이 릴리스의 개인화에 다음과 같은 개선 사항이 추가되었습니다.


### 이메일 디자이너 {#july-26-email}

이 릴리스의 이메일 채널에 다음 기능이 추가되었습니다.


### 관리 {#july-26-administration}

이 릴리스의 관리에 다음 기능이 추가되었습니다.


### 사용성 개선 사항 {#july-26-usability}

이번 릴리스에는 다음과 같은 사용 편의성 개선 사항이 적용되었습니다.

* **콘텐츠 템플릿의 SMS, 푸시, 인앱 및 Codebase 채널에 대한 빠른 실행 바로 가기** - 이제 콘텐츠 템플릿 목록의 **추가 작업** 단추에서 채널별 바로 가기를 추가로 사용할 수 있습니다. SMS 템플릿의 경우 메시지를 빠르게 편집하거나 문자 수/세그먼트를 확인합니다. 푸시 템플릿의 경우 제목, 본문 또는 미디어를 편집합니다. 인앱 템플릿의 경우 메시지 헤더, 메시지 본문 또는 미디어 URL을 편집합니다. 코드베이스 채널 템플릿의 경우 코드를 직접 편집합니다. 이러한 단축키는 이미 사용 가능한 이메일 채널 빠른 실행 단축키를 확장합니다. <!-- Documentation link: TBD -->
