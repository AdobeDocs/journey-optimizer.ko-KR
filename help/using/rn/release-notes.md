---
solution: Journey Optimizer
product: journey optimizer
title: 릴리스 정보
feature: Release Notes
topic: Content Management
description: Journey Optimizer 릴리스 정보
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 40e4aaa93400daf52c96aa5ac2de17151cdbb07f
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 42%

---

# 릴리스 정보 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="새로운 기능"
>abstract="**Adobe Journey Optimizer** 는 새로운 기능, 기존 기능의 개선 사항 및 버그 수정 사항을 지속적으로 제공합니다. 모든 변경 사항은 매달 마지막 주에 여기 있는 릴리스 정보에 통합됩니다."

[!DNL Adobe Journey Optimizer]는 지속적으로 새로운 기능, 기존 기능 개선, 버그 해결을 제공합니다. 모든 변경 사항은 매달 마지막 주에 여기 있는 릴리스 노트에 통합됩니다.

[!DNL Adobe Journey Optimizer]은(는) 기본적으로 [!DNL Adobe Experience Platform] 기반으로 구축되었으며 최신 혁신 및 향상된 기능을 활용할 수 있습니다. 변경 사항에 대한 자세한 내용은 [Adobe Experience Platform 릴리스 노트](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=ko-KR){target="_blank"}를 참조하세요.

![뉴스레터](../assets/do-not-localize/nl-icon.png) 오늘 [Adobe Journey Optimizer 분기별 뉴스레터](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"}에 등록하여 분기마다 최신 제품 업데이트, 재미있는 이야기, 사용 사례, 팁 등을 메일로 직접 받아 보세요.


## 2024년 5월 릴리스 정보 {#may-2024}

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
<p>이러한 의사 결정 항목은 이제 Journey Optimizer 캠페인에서 액세스할 수 있는 새로운 코드 기반 경험 채널을 통해 광범위한 인바운드 표면에 원활하게 통합됩니다. 경험 결정 의사 결정 정책은 코드 기반 경험 캠페인에서만 사용할 수 있습니다.</p>
<p>SMS 채널은 현재 조직 집합(제한된 가용성)에만 사용할 수 있습니다. 자세한 내용은 Adobe 담당자에게 문의하십시오.</p>
<img src="assets/do-not-localize/gif-exd.gif"/>
<p>자세한 내용은 <a href="../experience-decisioning/gs-experience-decisioning.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>이메일 표면 개인화 - 제한된 가용성</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 이메일 채널 표면을 만들 때 동적 하위 도메인 및 개인화된 헤더 매개 변수를 정의하여 이메일 설정을 보다 유연하게 제어하고 있습니다.</p>
<p>이메일 표면 개인화는 현재 조직 세트에만 사용할 수 있습니다(제한된 가용성). 자세한 내용은 Adobe 담당자에게 문의하십시오.</p>
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

**경험 의사 결정** (제한된 가용성)

Beta에서 이 릴리스까지 다음과 같은 개선 사항이 추가되었습니다.

* **Experience Decisioning + 코드 기반 경험** - 이제 Experience Decisioning 기능을 활용하여 코드 기반 캠페인에서 의사 결정 항목을 사용할 수 있습니다. 참고: Adobe Healthcare Shield 및 Privacy and Security Shield 추가 기능을 구매한 조직에서는 코드 기반 경험 채널 및 경험 결정을 사용할 수 없습니다. [자세히 보기](../code-based/get-started-code-based.md)
* **컨텍스트 데이터** - 이제 의사 결정 규칙 및 등급 지정에서 Adobe Experience Platform의 컨텍스트 데이터를 활용할 수 있습니다. [자세히 보기](../experience-decisioning/context-data.md)
* **새 권한** - 이제 의사 결정 관리 리소스에 대한 새로운 &#39;경험 의사 결정 관리&#39; 권한을 사용할 수 있습니다. 이를 통해 경험 결정과 관련된 권한을 관리할 수 있습니다. [자세히 보기](../experience-decisioning/gs-experience-decisioning.md)
* **최대 가용량 규칙** - 이제 Experience Decisioning에서 지정된 의사 결정 항목에 대해 여러 개의 최대 가용량 규칙을 추가할 수 있습니다. 이를 통해 오퍼를 전송하는 방식에 대한 제어 수준을 향상시킬 수 있습니다. [자세히 보기](../experience-decisioning/items.md#capping)
* **보고** - 이제 를 사용하여 Experience Decisioning 캠페인의 사용자 지정 보고 대시보드를 만들 수 있습니다. [!DNL Customer Journey Analytics]. [자세히 보기](../experience-decisioning/cja-reporting.md)


<!--**Decision Management**

* **Multi-rule support** - You can now add up to 10 capping rules for a given offer in Decision Management. This allows you to increase the level of control over the way offers are sent.
* **Audits** - The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu. -->


**이메일 채널**

<!--
* **List-unsubscribe** - Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. Refer to the following pages: [Email opt-out management](../email/email-opt-out.md#unsubscribe-header) and [Configure email settings](../email/email-settings.md#list-unsubscribe)
-->

* **스팸 점수** (베타) - 이제 전용 스팸 보고서에서 콘텐츠 스팸 점수를 확인할 수 있습니다. 이제 Adobe Journey Optimizer에서 SpamAssassin을 사용하여 이메일 콘텐츠를 테스트하고 ISP 또는 사서함 공급자가 이를 스팸으로 간주할지 여부를 나타내는 점수를 제공할 수 있습니다. [자세히 보기](../content-management/spam-report.md)

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
* **mTLS 지원** - 이제 사용자 지정 작업에서 mTLS 인증이 지원됩니다. mTLS를 활성화하기 위해 사용자 지정 작업 또는 여정에 필요한 추가 구성은 없습니다. mTLS 활성화 끝점이 감지되면 자동으로 발생합니다. [자세히 보기](../action/about-custom-action-configuration.md#mtls-protocol-support)
* **이벤트의 조회 테이블** - 이제 개체 배열 내의 특성을 사용하여 관계를 정의한 경우 조회 데이터 세트의 데이터를 활용할 수 있습니다. 조회 값은 여정(조건, 사용자 지정 작업 등)에서 사용할 수 있습니다. 및 메시지 개인화를 참조하십시오. [자세히 보기](../event/experience-event-schema.md#relationships_limitations)
* **이벤트 구성의 고급 표현식 편집기** (LA) - 이제 이벤트를 구성하는 동안 고급 표현식 편집기를 활용하여 이벤트 id 조건에서 보다 복잡한 표현식을 정의하거나 함수를 사용할 수 있습니다. 이 기능은 선택한 고객에 대해 제한된 가용성으로 릴리스됩니다. [자세히 보기](../event/about-creating.md)
* **병합 정책** (LA) - 여정에서 사용하는 병합 정책이 이제 여정 전체에서 볼 수 있으며 일관됩니다. 이 기능은 선택한 고객에 대해 제한된 가용성으로 릴리스됩니다. [자세히 보기](../building-journeys/journey-gs.md#merge-policies)

**세계화**

통합 사용자 경험을 제공하기 위한 지속적인 노력의 일환으로 Adobe Experience Cloud 제품 및 앱에서 사용되는 용어를 조화롭게 작성합니다. 이것은 객체의 이름과 관련된 경우 &quot;레이블&quot;로 변경되는 독일어 &quot;제목&quot;에 영향을 줍니다. 변경 사항은 UI 및 설명서에서 점진적으로 롤아웃됩니다.



