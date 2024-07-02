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
source-git-commit: 6c4e0418776622467e7f5b7bb3d9332d965becf1
workflow-type: ht
source-wordcount: '434'
ht-degree: 100%

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
<p>완전히 새로운 IP 주소로 이메일을 보내는 경우 이제 사용자 인터페이스에서 직접 IP 준비 워크플로를 쉽게 수행할 수 있습니다. Adobe Journey Optimizer는 최적의 전달성을 위한 모범 사례에 따라 IP 주소를 준비하는 표준화되고 효율적인 방법을 제공합니다.</p>
<!--p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<!--<table>
<thead>
<tr>
<th><strong>Content Fragments customization</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now define specific fields in a fragment that can be edited when the fragment is added to a campaign or journey. This allows for the adjustment of content portions at the time of use, providing flexibility to override default values with context-specific details.</p>
<p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>-->


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
<p>자세한 내용은 <a href="../start/ai-assistant.md">자세한 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>





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

* **의사 결정 관리의 다중 규칙 지원** - 이제 의사 결정 관리에서 주어진 오퍼에 대해 최대 10개의 캡핑 규칙을 추가할 수 있습니다. 이를 통해 오퍼를 전송하는 방식에 대한 제어 수준을 향상시킬 수 있습니다. [자세히 알아보기](../offers/offer-library/add-constraints.md#capping)

<!--* **Audits** - The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu. -->

<!--**Content fragments**

* Fragments can now be edited, and changes can be propagated across all live journeys and campaigns where they are used.
* New statuses for content fragments have been introduced: **Draft**, **Live**, **Publishing**, and **Archived**. 
* To use a fragment in a journey or campaign, it must now be in the **Live** status. A new step has been added to the fragment creation process, allowing the fragment to be published and made available for use in journeys and campaigns. Note that fragment publishing requires a new permission.
   
   **CAUTION** - Since **Draft** and **Live** statuses have been introduced with Journey Optimizer June release, all fragments created before this release have the **Draft** status, even if they are used in a journey or campaign. Learn how to update your existing fragments in this section.-->

**여정**

* 여정의 전역 시간 제한이 30일에서 91일로 늘어났습니다.
* Adobe Journey Optimizer가 이제 데이터 수명 주기 관리 요청뿐만 아니라 개인 정보 삭제/액세스 요청도 지원합니다.
* 이제 여정 인벤토리에서 열의 크기를 조정할 수 있습니다.
* **이벤트 구성의 고급 표현식 편집기** GA 변경 - 이제 이벤트를 구성할 때 고급 표현식 편집기를 활용하여 이벤트 ID 조건에 보다 복잡한 표현식을 정의하거나 함수를 사용할 수 있습니다. 이 기능은 일부 고객을 대상으로 한 제한된 가용성으로 릴리스됩니다. <!--[Read more](../event/about-creating.md)-->
* **병합 정책** GA 변경 - 여정에서 사용하는 병합 정책이 이제 여정 전체에서 일관적이며 직접 볼 수 있습니다. 이 기능은 일부 고객을 대상으로 한 제한된 가용성으로 릴리스됩니다. <!--[Read more](../building-journeys/journey-gs.md#merge-policies)-->



**캠페인**

* 이제 Adobe Journey Optimizer에서 캠페인을 만들 때 새로운 모달에서 캠페인 유형(예약됨 또는 트리거됨)을 선택할 수 있습니다.

<!--**Email channel**

* **List-unsubscribe** - Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. Refer to the following pages: [Email opt-out management](../email/email-opt-out.md#unsubscribe-header) and [Configure email settings](../email/email-settings.md#list-unsubscribe)-->


**SMS 채널**

* 이제 한 번의 API 구성으로 각 샌드박스마다 고유한 짧은 코드를 추가할 수 있어 프로세스가 보다 효율적이고 간소화됩니다.
  <!--* You can now modify existing SMS configurations.-->

**인앱 채널**

* **표현식 조각** - 이제 표현식 조각을 **인앱 채널**&#x200B;에서 사용할 수 있습니다. <!--[Read more](../personalization/use-expression-fragments.md)-->


* 이제 Edge Delivery 플러그인을 사용하여 인바운드 구현을 이해하고 문제를 해결하는 데 필요한 정보를 얻을 수 있습니다.
