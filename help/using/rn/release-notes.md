---
title: 릴리스 정보
description: Journey Optimizer 릴리스 정보
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 845a8324d96d8891bf1edf64a0962d23976bb29e
workflow-type: tm+mt
source-wordcount: '986'
ht-degree: 18%

---

# 릴리스 정보 {#release-notes}

이 페이지에는 [!DNL Journey Optimizer]의 새로운 기능과 개선 사항이 모두 포함되어 있습니다. 또한 자세한 변경 사항은 [최신 설명서 업데이트](documentation-updates.md) 페이지를 참조하십시오.

[!DNL Adobe Journey Optimizer]은(는) 기본적으로 [!DNL Adobe Experience Platform] 기반으로 구축되었으며 최신 혁신 및 향상된 기능을 활용할 수 있습니다. [Adobe Experience Platform 릴리스 노트](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=ko-KR){target=&quot;_blank&quot;}에서 이러한 변경 사항에 대해 자세히 알아보십시오.

![뉴스레터](../assets/do-not-localize/nl-icon.png) 오늘 [Adobe Journey Optimizer 분기 뉴스레터](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;}에 등록하시면 분기마다 최신 제품 업데이트, 흥미로운 사례, 사용 사례, 팁 등을 받은 편지함에 바로 받을 수 있습니다.

## 2022년 9월 릴리스{#sept-2022-release}

### 새로운 기능{#sept-2022-features}


<!--
<table>
<thead>
<tr>
<th><strong>Dynamic content & new conditional rule builder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create dynamic content to adapt the content of your messages based on conditional rules.</p> 
<p>Conditional rules are created using a visual rule builder within the Expression Editor, where you can store them for further reuse across your journeys and campaigns.</p>
<img src="assets/do-not-localize/dynamic-content.gif"/>
<p>For more information, refer to the <a href="../personalization/get-started-dynamic-content.md">detailed documentation</a>.
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>API가 트리거된 캠페인</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 기존의 예약된 캠페인 외에, Journey Optimizer에서 API 트리거된 캠페인을 만들어 API를 사용하여 외부 시스템에서 호출할 수 있습니다.</p>
<p>이를 통해 암호 재설정, OTP 토큰 등과 같은 다양한 운영 및 트랜잭션 메시지 요구 사항을 처리할 수 있습니다.</p>
<img src="assets/do-not-localize/api-triggered.gif"/>
<p>자세한 내용은 <a href="../campaigns/api-triggered-campaigns.md">세부 설명서</a>를 참조하세요.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>데이터 액세스 제어</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>속성 기반 액세스 제어를 통해 관리자는 특정 속성에 따라 특정 객체에 대한 액세스를 제어할 수 있습니다. 이러한 속성은 레이블과 같은 객체에 추가된 메타데이터일 수 있습니다. 이 릴리스부터 관리자는 특정 필드 및/또는 개체에만 액세스할 수 있는 사용자 역할과 해당 필드 및/또는 개체에 해당하는 데이터를 정의할 수도 있습니다.</p>
<p> 속성 기반 액세스 제어 사용은 현재 선택한 고객에게만 제한되며, 향후 릴리스의 모든 환경에 배포됩니다.</p>
<img src="assets/do-not-localize/olac.gif"/>
<p>자세한 내용은 <a href="../administration/object-based-access.md">세부 설명서</a>를 참조하세요.
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>데이터 거버넌스 및 개인 정보</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>DULE(Data Usage Labeling and Enforcement) 거버넌스 프레임워크를 사용하여 Journey Optimizer은 이제 Adobe Experience Platform 거버넌스 정책을 활용하여 사용자 지정 작업을 통해 중요한 필드를 타사 시스템으로 내보내지 못하도록 할 수 있습니다. 시스템이 사용자 지정 작업 매개 변수에서 제한된 필드를 식별하면 여정이 게시되지 않는 오류가 표시됩니다.</p>
<p>DULE(Data Usage Labeling and Enforcement) 사용은 현재 선택한 고객에게만 제한되며, 향후 릴리스의 모든 환경에 배포됩니다.</p>
<p>자세한 내용은 <a href="../action/action-privacy.md">세부 설명서</a>를 참조하세요.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>자동화된 동의 적용(동의 정책)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform을 사용하면 고객의 동의 환경 설정을 준수하도록 마케팅 정책을 쉽게 채택하고 적용할 수 있습니다. 동의 정책은 Adobe Experience Platform에 정의됩니다. Journey Optimizer에서는 이러한 동의 정책을 사용자 지정 작업에 적용할 수 있습니다. 예를 들어 이메일, 푸시 또는 SMS 커뮤니케이션에 동의하지 않은 고객을 제외하는 동의 정책을 정의할 수 있습니다.
<p>현재 Automated Consent Enforcement는 Healthcare Shield 추가 기능 서비스를 구입한 조직에서만 사용할 수 있습니다.</p>
<p>자세한 내용은 <a href="../action/consent.md">세부 설명서</a>를 참조하세요.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>권한 관리</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer에서는 기능 및 개체의 권한을 관리하기 위한 사용자 역할 및 액세스 정책 정의를 지원합니다. 사용 <strong>Adobe Experience Cloud 권한</strong>, 역할을 만들고 관리하며, 이러한 역할에 대해 원하는 리소스 권한을 지정할 수 있습니다. 또한 권한을 사용하여 특정 역할과 연관된 레이블, 샌드박스 및 사용자를 관리할 수도 있습니다.</p>
<p> 권한 사용은 현재 선택한 고객에게만 제한되며 향후 릴리스의 모든 환경에 배포됩니다.</p>
<p>자세한 내용은 <a href="../administration/attribute-based-access.md">세부 설명서</a>를 참조하세요.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>경고 및 모니터링</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer 사용자는 여정이 예상대로 작동하지 않을 때 사용자 인터페이스를 통해 시스템 경고에 액세스하여 알림을 받을 수 있습니다. 사용 가능한 경고를 보고 구독할 수 있습니다. 세그먼트 읽기 활동이 정의된 기간 동안 프로필을 처리하지 않은 경우 이 릴리스에서 사용할 수 있는 첫 번째 경고에 경고가 표시됩니다. 이 워크플로우의 잠금이 해제되면 더 많은 작업이 표시됩니다.</p>
<p>자세한 내용은 <a href="../reports/alerts.md">자세한 설명서</a>를 참조하세요.
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Data Hygiene</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform provides a suite of data hygiene capabilities that allow you manage your stored data through programmatic deletions of consumer records and datasets. This capability is now available for Adobe Journey Optimizer. </p>
<p>You can manage your data stores to ensure that information is used as expected, is updated when incorrect data needs fixing, and is deleted when organizational policies deem it necessary.</p>
<p><strong>Caution</strong> - Data Hygiene capabilities are currently only available for organizations that have purchased the Healthcare Shield add-on offering.</p>
<p>For more information, refer to the <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->

### 개선 사항{#sept-2022-improvements}

**여정**

* 다음 **엔티티 데이터 세트** 이제 Adobe Journey Optimizer에서 바로 사용할 수 있는 데이터 세트로 사용할 수 있습니다. 이 조회 데이터 세트에는 추적 및 피드백 데이터 세트 정보를 보강하는 메타 데이터가 포함되어 있습니다. 이렇게 하면 보다 쉽게 이해할 수 있는 데이터로 보고서 및 쿼리를 향상시킬 수 있습니다. [자세히 보기](../start/datasets-query-examples.md#entity-dataset)
* 여정이 동일한 이벤트에 대해 여러 번 잘못 트리거되지 않도록 단일 여정(이벤트 또는 세그먼트 자격 시작)에 새 보호 기능이 추가되었습니다. 이제 프로필 다시 시작은 기본적으로 5분 동안 일시적으로 차단됩니다. [자세히 알아보기](../start/guardrails.md#events-g)

**관리**

* 이제 허용 목록을 활성화하거나 비활성화할 때 각 작업의 영향을 자세히 설명하는 새 경고가 표시됩니다. [자세히 보기](../configuration/allow-list.md#enable-allow-list)
* 채널 서피스 생성, IP 풀 생성, 제외 목록 및 허용 목록 관리 및 SMS 채널 구성을 위한 사용자 인터페이스가 업데이트되었습니다.
* 이제 주어진 하위 도메인에 대한 첫 번째 채널 서피스를 생성할 때 처리 시간은 10분에서 10일, 해당 하위 도메인을 사용하는 후속 서피스에 대해 최대 3시간까지 소요됩니다. [자세히 보기](../configuration/channel-surfaces.md#create-channel-surface)

<!--* Now when downloading the suppression list as a CSV file, you can choose the file that was previously generated, or generate a new file.-->
* 랜딩 페이지 사전 설정 및 랜딩 페이지 하위 도메인을 만들기 위한 사용자 인터페이스를 업데이트했습니다. [자세히 보기](../configuration/lp-subdomains.md)

**감사 제어**

* Journey Optimizer을 사용하여 캠페인, 여정, 메시지, 랜딩 페이지 등과 같은 다양한 서비스 및 기능에서 시스템의 사용자가 수행한 작업을 식별할 수 있습니다. 이제 감사 로그 리소스에는 다양한 다른 작업에 대한 변경 사항이 포함되며, 활동이 발생하면 자동으로 기록됩니다. [이 페이지](../privacy/audit-logs.md)에서 자세히 알아보십시오.

**아카이빙 지원**

* 새로운 **엔티티 데이터 세트** 에는 보관을 위해 모든 채널에서 보낸 메시지의 형식 및 구조를 내보낼 수 있는 템플릿 필드가 포함되어 있습니다. [자세히 보기](../configuration/archiving-support.md)

**랜딩 페이지**

* 이제 동일한 랜딩 페이지 내에서 다른 페이지에서 가져온 컨텍스트 데이터를 사용할 수 있습니다. 예를 들어, 기본 랜딩 페이지의 구독 목록에 확인란을 연결하는 경우, &quot;감사합니다&quot; 하위 페이지에서 해당 구독 목록을 사용할 수 있습니다. [자세히 보기](../landing-pages/lp-content.md#use-primary-page-context)

<!--* When configuring the primary page, you can now create additional data to enable storing information when the landing page is being submitted. [Learn more](../landing-pages/lp-content.md#use-additional-data)-->

<!--* You can now use information that was submitted on a landing page to send communications to your customers. For example, if a user subscribes to a given subscription list, you can leverage that information to send an email recommending other subscription lists to that user.-->

### 기타 변경 사항{#sept-2022-other}

* 여정 버스트 모드가 Campaign Rapid 게재 모드로 대체되었습니다. [자세히 보기](../campaigns/create-campaign.md#rapid-delivery)
* 성능을 향상시키기 위해 읽기 세그먼트, 세그먼트 자격 또는 비즈니스 이벤트 활동으로 시작하는 여정에서 더 이상 경험 이벤트 필드 그룹을 사용할 수 없습니다. 이 변경 사항은 새 여정에만 적용됩니다. 기존 동작은 현재 동작을 유지합니다. [자세히 보기](../start/guardrails.md#expression-editor)
* 예약된 읽기 세그먼트 여정에 대한 1시간 제한이 제거되었습니다. 이제 이러한 여정을 지연 없이 실행할 수 있습니다.

