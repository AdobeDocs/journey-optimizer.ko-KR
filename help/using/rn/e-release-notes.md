---
solution: Journey Optimizer
product: journey optimizer
title: 릴리스 정보
description: Journey Optimizer 초기 릴리스 정보
feature: Release Notes
hide: true
hidefromtoc: true
topic: Content Management
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 16812ed5a3f4a4626387d7f21be91c31530eb7cc
workflow-type: tm+mt
source-wordcount: '570'
ht-degree: 23%

---

# 초기 릴리스 정보 {#e-release-notes}

[!DNL Adobe Journey Optimizer]는 지속적으로 새로운 기능, 기존 기능 개선, 버그 해결을 제공합니다. 모든 변경 사항은 매월 말 [릴리스 정보](release-notes.md)에 통합됩니다.

**아래 초기 릴리스 정보는 릴리스 공개 당일까지 사전 통지 없이 변경될 수 있습니다**. 링크, 화면, 업데이트된 설명서는 릴리스 날짜의 [릴리스 정보](release-notes.md)에 게시됩니다.

## 2024년 6월 초기 릴리스 정보 {#e-2024}

**릴리스 날짜**: 2024년 6월 18~19일

### 새로운 기능 {#e-features}

이번 릴리스에는 아래에 있는 새로운 기능이 제공됩니다.

<table>
<thead>
<tr>
<th><strong>IP 준비 워크플로</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>완전히 새로운 IP 주소로 이메일을 보내는 경우 이제 사용자 인터페이스에서 직접 IP 준비 워크플로우를 쉽게 수행할 수 있습니다. Adobe Journey Optimizer은 최적의 전달성을 위한 모범 사례를 따르는 IP 주소를 데워 올리는 표준화되고 효율적인 방법을 제공합니다.</p>
<p>자세한 내용은 <a href="../configuration/ip-warmup-gs.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>콘텐츠 조각 사용자 지정 및 라이프사이클</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 캠페인 또는 여정에 조각을 추가할 때 편집할 수 있는 조각의 특정 필드를 정의할 수 있습니다. 이를 통해 사용 시 컨텐츠 부분을 조정할 수 있으므로 컨텍스트 특정 세부 사항으로 기본값을 대체할 수 있는 유연성을 제공합니다.</p>
<!--p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Adobe Journey Optimizer의 AI 지원</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>AI Assistant는 Adobe 개념을 탐색 및 이해하고 특정 환경에 대한 운영 통찰력을 얻는 데 사용할 수 있는 사용자 인터페이스 기능입니다. Adobe Journey Optimizer을 비롯한 Adobe Experience Cloud 전역의 여러 제품에서 사용할 수 있습니다.</p>
<p>자세한 내용은 <a href="../start/ai-assistant.md">자세한 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Reporting with Customer Journey Analytics (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer reporting is now fully integrated with Customer Journey Analytics capabilities, standardizing reporting across both platforms and improving data consistency and reliability. This seamless integration between Journey Optimizer and Customer Journey Analytics provides a clearer view of performance metrics, enabling users to make more informed decisions.</p>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Multilingual messages in journeys and campaigns  (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now effortlessly create content in multiple languages within a single campaign or journey. With this feature, you can switch between languages when editing your campaign or your journey, streamlining the entire editing process and improving your capability to efficiently manage multilingual content.</p>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Experimentation in journeys (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Already available in campaigns, Adobe Journey Optimizer now supports experiments in journeys. Experiments are randomized trials, which in the context of online testing, means that you expose some randomly selected users to a given variation of a message, and another randomly selected set of users to some other variation or treatment. After exposure, you can then measure the outcome metrics you are interested in, such as opens of emails, subscriptions, or purchases.</p>
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


**의사 결정 관리**

* **의사 결정 관리의 다중 규칙 지원** - 이제 의사 결정 관리에서 주어진 오퍼에 대해 최대 10개의 최대 가용량 규칙을 추가할 수 있습니다. 이를 통해 오퍼를 전송하는 방식에 대한 제어 수준을 향상시킬 수 있습니다. [자세히 알아보기](../offers/offer-library/add-constraints.md#capping)

<!--* **Audits** - The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu. -->

**콘텐츠 조각**

* 이제 조각을 편집할 수 있으며 변경 사항을 해당 조각이 사용되는 모든 라이브 여정 및 캠페인에 전파할 수 있습니다.
* 콘텐츠 조각에 대한 새로운 상태가 도입되었습니다. **초안**, **라이브**, **게시**, 및 **보관됨**.
* 여정 또는 캠페인에서 조각을 사용하려면 이제 다음 위치에 있어야 합니다 **라이브** 상태. 조각 생성 프로세스에 새 단계를 추가하여 조각을 게시하고 여정 및 캠페인에서 사용할 수 있도록 했습니다. 조각을 게시하려면 새 권한이 필요합니다.

  **주의** - 이후 **초안** 및 **라이브** Journey Optimizer 6월 릴리스와 함께 상태가 도입되었으며 이 릴리스 전에 생성된 모든 조각은 **초안** 상태(여정 또는 캠페인에서 사용되더라도). 이 섹션에서 기존 조각을 업데이트하는 방법을 알아봅니다.

**여정**

* 여정 전역 시간 제한이 30일에서 91일로 늘어났습니다.
* 이제 Adobe Journey Optimizer에서 개인 정보 삭제/액세스 요청을 지원합니다.
* 이제 여정 인벤토리에서 열의 크기를 조정할 수 있습니다.


**캠페인**

* 이제 Adobe Journey Optimizer에서 캠페인을 생성할 때 새 모달에서 캠페인 유형(예약됨 또는 트리거됨)을 선택할 수 있습니다.

**이메일 채널**

* **목록 구독 취소** - 대량 발신자에 대한 최근 Gmail 및 Yahoo 공지에 따라 Journey Optimizer은 &quot;게시/1클릭&quot; 목록 구독 취소 옵션을 지원합니다. <!--Refer to the following pages: [Email opt-out management](../email/email-opt-out.md#unsubscribe-header) and [Configure email settings](../email/email-settings.md#list-unsubscribe)-->


**SMS 채널**

* 이제 단일 API 구성을 통해 각 샌드박스에 고유한 짧은 코드를 추가할 수 있으므로 프로세스가 보다 효율적이고 간소화됩니다.
* 이제 기존 SMS 구성을 수정할 수 있습니다.

**인앱 채널**

* **표현식 조각** - 이제 표현식 조각을 사용할 수 있습니다. **인앱 채널**. [자세히 보기](../personalization/use-expression-fragments.md)


* 이제 Edge 게재 플러그인을 사용하여 인바운드 구현을 이해하고 문제를 해결하는 데 필요한 정보를 얻을 수 있습니다.


