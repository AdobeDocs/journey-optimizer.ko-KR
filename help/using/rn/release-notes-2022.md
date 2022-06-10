---
title: 2022년 릴리스 정보
description: Journey Optimizer 릴리스 정보
exl-id: 0997a640-3f89-4460-ba93-ea21a9d4efc5
source-git-commit: f5e3b7cee816be420a09abd8aa9404faaccfec87
workflow-type: ht
source-wordcount: '1069'
ht-degree: 100%

---

# 2022년 릴리스 정보 {#release-notes-2022}

이 페이지에서는 2022년에 릴리스된 [!DNL Journey Optimizer]의 기능 및 개선 사항 목록을 확인할 수 있습니다.

[이 페이지](release-notes.md)에서 최신 릴리스 노트를 사용할 수 있습니다.

## 2022년 4월 릴리스 {#april-2022-release}

### 개선 사항

**랜딩 페이지**

* **새로운 옵트인/옵트아웃 확인란 옵션** - 이제 옵트인/옵트아웃에 대한 단일 확인란을 구독 랜딩 페이지에 삽입할 수 있습니다. 사용자는 동의(옵트인)하려면 이 확인란을 선택하고 동의를 제거(옵트아웃)하려면 선택을 해제해야 합니다. [자세히 보기](../landing-pages/design-lp.md#define-lp-specific-content)

* **랜딩 페이지 필드 미리 채우기** - 이제 사용자에게 랜딩 페이지 필드를 프로필 정보로 미리 채우는 기능을 제공할 수 있습니다. [자세히 알아보기](../landing-pages/create-lp.md#configure-primary-page)

**의사 결정 관리**

* **Edge용 Decisioning API** - Edge Decisioning API는 Offer Decisioning에서 관리하는 개인화된 오퍼를 제공하고 렌더링할 수 있습니다. Offer Decisioning UI(사용자 인터페이스) 또는 API를 사용하여 오퍼 및 기타 관련 개체를 만들 수 있습니다. [자세히 알아보기](../offers/api-reference/offer-delivery-api/edge-decisioning-api.md)

**관리**

* **PTR 제출 기간** - PTR 편집 유효 기간이 몇 시간 수준으로 변경되었습니다. [자세히 보기](../configuration/ptr-records.md#processing)

**이메일 디자인**

* 이제 Journey Optimizer에서 **20개의 새로운 이메일 템플릿**&#x200B;으로 이메일 콘텐츠를 디자인할 수 있습니다.

**사용자 인터페이스**

* **Journey Optimizer UI의 상황별 도움말** - Journey Optimizer의 여러 페이지에 상황별 도움말 링크가 추가되었습니다. &quot;i&quot; 아이콘을 클릭할 수 있는 경우, 클릭하면 현재 기능에 대한 간단한 설명을 보고 관련 문서에 액세스합니다.

**Adobe Campaign Standard 통합**

이제 Adobe Campaign Standard 고객이 Journey Optimizer를 사용하여 이메일, 푸시 알림, SMS를 보낼 수 있습니다. 새로운 기본 제공 작업으로 Journey Optimizer에 Campaign Standard의 트랜잭션 메시지 기능을 활용하세요.  [자세히 보기](../action/acs-action.md)

<!--
### Fixes

* Fixed an issue which caused tracking reports not to be available as the `JourneyActionId` was not properly populated. PLATIR-19854, CJM-26006
* Fixed an error on business events which could block the journey publication. CJM-25931
* Fixed an issue which could prevent images in Email Designer templates from being displayed. PLATIR-18176, CJM-25008
-->

## 2022년 3월 릴리스 {#march-2022-release}

### 개선 사항

**여정**

* 통합 프로필 스키마에 불필요한 필드가 없도록 하기 위해, 여정 단계 이벤트 스키마는 이제 프로필에서 기본적으로 사용하도록 설정되지 않습니다. 필요한 경우 활성화할 수 있습니다. [자세히 알아보기](../reports/sharing-overview.md)
* 내보내기 작업 관련 새로운 단계 이벤트는 이제 Journey Optimizer에서 Adobe Experience Platform으로 보내집니다. 쿼리 예시를 설명서에 추가했습니다. [자세히 알아보기](../reports/query-examples.md)

**의사 결정 관리**

* 이제 오퍼 한도 설정이 모든 사용자 간에 적용되는지, 아니면 하나의 특정 프로필, 모든 배치 또는 배치마다 적용되는지를 지정할 수 있습니다. [자세히 알아보기](../offers/offer-library/add-constraints.md#capping)
* Batch Decisioning API를 사용하면 한 번의 호출로 주어진 세그먼트의 모든 프로필에 대해 Offer Decisioning 기능을 사용할 수 있습니다. 세그먼트에 있는 각 프로필에 대한 오퍼 콘텐츠는 사용자 정의 일괄 처리 워크플로우에 사용할 수 있도록 AEP 데이터 세트에 배치됩니다. [자세히 알아보기](../offers/api-reference/offer-delivery-api/batch-decisioning-api.md)

**관리**

* 이제 메시지 사전 설정 수준에서 이메일 헤더의 구독 취소 링크를 활성화/비활성화하고 메시지 수준에서 사용자 정의 구독 취소 URL을 설정할 수 있습니다. [자세히 알아보기](../configuration/message-presets.md#list-unsubscribe)
* 프로덕션 및 비프로덕션 샌드박스에서 [!DNL Journey Optimizer] 인터페이스를 통해 허용 목록을 활성화하고 비활성화할 수 있습니다. [자세히 알아보기](../reports/allow-list.md#enable-allow-list)

**개인화**

* 이제 라이브러리에 개인화 표현식을 40개 넘게 저장할 수 있습니다. [자세히 알아보기](../personalization/personalization-library.md)

## 2022년 2월 릴리스 {#feb-2022-release}

### 새로운 기능

<table>
<thead>
<tr>
<th><strong>구독 랜딩 페이지</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer에서 랜딩 페이지를 만들고 디자인하고, 커뮤니케이션 수신을 옵트인 또는 옵트아웃하거나 뉴스레터 등 특정 서비스를 구독하기 위한 온라인 양식으로 사용자를 보낼 수 있습니다.</p>
<p>자세한 내용은 <a href="../landing-pages/create-lp.md">세부 설명서</a> 및 관련 <a href="../landing-pages/lp-use-cases.md">샘플 사용 사례</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>새로운 개인화 표현식 라이브러리</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer에서는 사전 정의된 개인화 표현식에 액세스할 수 있는 라이브러리를 제공합니다. 이 표현식은 [관리자]인 사용자가 구성합니다.</p>
<p>자세한 내용은 <a href="../personalization/personalization-library.md">세부 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>API Developer Site and Suppression API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer provide RESTful APIs that allow you to programmatically perform key operations in your applications.
Developer SDK for Journey Optimizer is now available with the Suppression API (beta).</p>
<p>With this API, you can control your outgoing messages using suppression and allow lists.
The suppression list helps you with honoring the ISPs’ feedback to preserve sending IP reputation. The allow list helps you ensure that you send only to those email addresses which are in the allowed list, and typically to ensure that you don't send mails to customers from your development sandbox.</p>
<p>See <a href="https://developer.adobe.com/journey-optimizer-apis/">Adobe Journey Optimizer APIs</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>UTM 추적 매개 변수를 사용하여 메시지를 추적하는 정보 전달</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer 메시지 콘텐츠에서 링크에 UTM 매개 변수를 추가할 수 있습니다. 이 링크를 통해 해당 링크에 대한 추가 데이터를 제공할 수 있으며, 사용자가 링크를 클릭한 위치와 이유를 파악할 수 있습니다.</p>
<p>자세한 내용은 <a href="../configuration/message-presets.md#configure-email-settings">자세한 설명서</a>를 참조하세요.</p-->
</td>
</tr>
</tbody>
</table>

### 개선 사항

**여정**

* 성능을 최적화하기 위해 1주일 동안 트리거되지 않은 테스트 모드의 모든 여정이 이제 초안 상태로 다시 전환합니다. [자세히 보기](../building-journeys/testing-the-journey.md#important_notes)
* Journey Optimizer과 Adobe Campaign Classic 간 통합이 성능을 개선하기 위해 최적화되었습니다. 최대 가능한 기본 구성이 4,000회 호출/5분으로 변경되었습니다.	[자세히 보기](../action/acc-action.md#important-notes)

**보고**

* 이제 상태에 따라 게재를 필터링할 수 있습니다.
   * 이제 메시지 실행 목록에서 증명을 게재 목록에서 제외할 수 있습니다.
   * 라이브/전역 보고서에서 테스트 이벤트를 제외하도록 선택할 수 있습니다.

* 이제 메시지를 즉시 보낸 사람 수 및 1시간 최적화, 2시간 최적화 등을 통해 메시지를 보낸 사람 수 등 전송 시간 최적화 데이터에 대한 보고서에 액세스할 수 있습니다.

<!--* Offer Decisioning reports are now available in Journey Optimizer. You can access the following metrics: Offers sent - Offers' impression rate - Offers' click rate - Breakdown report on Offers' sent.-->

**의사 결정 관리**

* 이제 등급 및 AI 등급이 단일 탭으로 그룹화됩니다.

## 2022년 1월 릴리스 {#january-2022-release}

### 새로운 기능

<table>
<thead>
<tr>
<th><strong>여정 - 프로필 상한 조건으로 IP 램프 업 최적화</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>여정에서 <strong>조건</strong> 활동을 구성할 때 이제 프로필 상한을 정의할 수 있습니다. 이 새 조건 유형을 사용하면 여정 경로에 대해 최대 프로필 수를 설정할 수 있습니다. 이 한도에 도달하면 입력한 프로필에서 대체 경로를 사용합니다. 이를 통해 게재 볼륨을 증가시킬 수 있습니다(IP 램프 업). 예를 들어 실행을 분할하여 1일에는 1,000개의 메시지를, 2일에는 2,000개의 메시지를 발송하는 등 도메인에서 게재를 증가시킬 수 있습니다.</p>
<p>자세한 내용은 <a href="../building-journeys/condition-activity.md#profile_cap">세부 설명서</a> 및 관련 <a href="../building-journeys/ramp-up-deliveries-uc.md">샘플 사용 사례</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>여정 - 세그먼트 읽기 개선 사항</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>다음 <strong>증분 읽기</strong> 옵션이 반복 <strong>세그먼트 읽기</strong> 활동에 추가되었습니다. 이 옵션을 사용하면 여정의 마지막 실행 이후 세그먼트에 입력한 개인만 타겟팅할 수 있습니다. 첫 번째 실행은 항상 모든 세그먼트 구성원을 타깃팅합니다.</p>
<p>자세한 내용은 <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">자세한 설명서</a>를 참조하세요.
</td>
</tr>
</tbody>
</table>

### 개선 사항

**여정**

* 이제 Journey Optimizer 단계 이벤트를 [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=ko)의 다른 데이터 세트에 연결할 수 있습니다. 기본 제공 여정 단계 이벤트 스키마의 **profileID** 필드가 이제 ID 필드로 정의됩니다. [자세히 알아보기](../reports/sharing-overview.md#integration-cja)

**Offer Decisioning**

* 게시된 메시지에서 직접 또는 간접적으로 참조되는 오퍼, 대체 오퍼, 오퍼 컬렉션 또는 오퍼 결정을 업데이트하면 이제 다시 게시할 필요 없이 업데이트가 해당 메시지에 자동으로 반영됩니다. [자세히 알아보기](../offers/offers-e2e.md#insert-decision-in-email)

* 이제 주어진 테스트 프로필에 게재할 오퍼 시뮬레이션 시 기본 시뮬레이션 설정을 수정하고 시뮬레이션에 해당하는 코드를 볼 수 있습니다. 코드는 문제 해결용으로 사용할 수 있습니다. [자세히 알아보기](../offers/offer-activities/simulation.md#define-simulation-settings)

**관리**

* 이제 관리자는 CNAME 설정 하위 도메인으로 PTR 레코드를 편집할 수 있습니다. [자세히 알아보기](../configuration/ptr-records.md#edit-ptr-subdomains-cname)

**개인화**

* **즐겨찾기에 추가** - 개인화 작업 시 효율성을 개선하기 위해 즐겨찾기 저장 개념을 도입했습니다. 즐겨찾기 메뉴에 다양한 속성을 추가하면 가장 자주 사용하는 항목에 빠르게 액세스할 수 있습니다. [자세히 알아보기](../personalization/personalize.md#fav)
