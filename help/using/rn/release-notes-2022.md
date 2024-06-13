---
solution: Journey Optimizer
product: journey optimizer
title: 2022년 릴리스 정보
description: Journey Optimizer 릴리스 정보
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
hidefromtoc: true
exl-id: 0997a640-3f89-4460-ba93-ea21a9d4efc5
source-git-commit: e34c39c02f71361277f28b1a116a54390875f93d
workflow-type: ht
source-wordcount: '3598'
ht-degree: 100%

---

# 2022년 릴리스 정보 {#release-notes-2022}

이 페이지에서는 2022년에 릴리스된 [!DNL Journey Optimizer]의 기능 및 개선 사항 목록을 확인할 수 있습니다.



## 2022년 10월 릴리스 {#oct-2022-release}

<!--

### New capability{#oct-2022-features}

<table>
<thead>
<tr>
<th><strong>Direct Mail Channel (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add direct mail messages in your campaigns and journeys. Direct mail is an offline channel that allows you to personalize and generate the files required by direct mail providers to send mail to your customers.</p>
<p>When you prepare a direct mail delivery, Journey Optimizer generates a file including all the targeted profiles and the chosen contact information (postal address for example). You will then be able to send this file to your direct mail provider who will take care of the actual sending.</p>
</td>
</tr>
</tbody>
</table>

-->

### 개선 사항 {#oct-2022-improvements}

**여정**

* 반복 대상자 읽기 일정 매개 변수에 **반복 시 강제 재입력** 이 추가되었습니다. 이 옵션을 사용하면 여정에 여전히 존재하는 모든 프로필이 다음 실행 시 자동으로 종료되도록 할 수 있습니다. 옵션이 비활성화되면 프로필은 다른 경우에 다시 입력하기 전에 여정을 완료해야 합니다. [자세히 알아보기](../building-journeys/read-audience.md#configuring-segment-trigger-activity)

**관리**

* 하위 도메인, 방문 페이지 하위 도메인, PTR 레코드 및 IP 풀 구성은 모든 샌드박스에 공통적이므로 이러한 구성 중 하나를 수정하면 프로덕션 샌드박스에도 영향을 미친다는 경고 메시지가 사용자 인터페이스에 추가되었습니다.
* 사용자 인터페이스에서 금지 목록을 CSV 파일로 업로드하는 단계가 수정되었습니다. [자세히 알아보기](../configuration/manage-suppression-list.md#download-suppression-list)

**캠페인**

* 이제 완료되고 중지된 캠페인을 보관할 수 있습니다. [자세히 알아보기](../campaigns/modify-stop-campaign.md#archive)


## 2022년 9월 릴리스{#sept-2022-release}

### 새로운 기능{#sept-2022-features}

<table>
<thead>
<tr>
<th><strong>다이내믹 콘텐츠 및 새로운 조건부 규칙 빌더</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 조건부 규칙에 따라 메시지 콘텐츠를 조정할 수 있는 다이내믹 콘텐츠를 만들 수 있습니다.</p> 
<p>조건부 규칙은 표현식 편집기 내에서 시각적 규칙 빌더를 사용하여 작성되며, 이 빌더를 저장하여 여정 및 캠페인 간에 다시 사용할 수 있습니다.</p>
<img src="assets/do-not-localize/dynamic-content.gif"/>
<p>자세한 내용은 <a href="../personalization/get-started-dynamic-content.md">세부 설명서</a>를 참조하세요.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>API-트리거된 캠페인</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 기존의 예약된 캠페인 외에도, Journey Optimizer에서 API 트리거된 캠페인을 만들고 API를 사용하여 외부 시스템에서 호출할 수 있습니다.</p>
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
<p>속성 기반 액세스 제어를 통해 관리자는 특정 속성에 따라 특정 객체에 대한 액세스를 제어할 수 있습니다. 이러한 속성은 레이블과 같은 객체에 추가된 메타데이터일 수 있습니다. 이번 릴리스부터 관리자는 특정 필드 및/또는 개체에만 액세스할 수 있는 사용자 역할과 해당 필드 및/또는 개체에 해당하는 데이터를 정의할 수 있습니다.</p>
<p> 속성 기반 액세스 제어 사용은 현재 선택한 고객으로 제한되며 향후 릴리스의 모든 환경에 배포될 예정입니다.</p>
<img src="assets/do-not-localize/olac.gif"/>
<p>자세한 내용은 <a href="../administration/object-based-access.md">세부 설명서</a>를 참조하세요.
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>데이터 거버넌스 및 개인 정보 보호</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>DULE(데이터 사용 레이블 및 적용) 거버넌스 프레임워크를 사용하여 Journey Optimizer는 이제 Adobe Experience Platform 거버넌스 정책을 활용하여 사용자 지정 작업을 통해 중요한 필드를 타사 시스템으로 내보내지는 것을 방지할 수 있습니다. 시스템이 사용자 지정 작업 매개 변수에서 제한된 필드를 식별하면 여정을 게시하지 못하게 하는 오류가 표시됩니다.</p>
<p>DULE(데이터 사용 레이블 및 적용) 사용은 현재 선택한 고객으로 제한되며, 향후 릴리스의 모든 환경에 배포될 예정입니다.</p>
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
<p>Adobe Experience Platform을 사용하면 고객의 동의 환경 설정을 준수하도록 마케팅 정책을 쉽게 채택하고 적용할 수 있습니다. 동의 정책은 Adobe Experience Platform에 정의되어 있습니다. Journey Optimizer에서는 이러한 동의 정책을 사용자 지정 작업에 적용할 수 있습니다. 예를 들어 이메일, 푸시 또는 SMS 커뮤니케이션에 동의하지 않은 고객을 제외하는 동의 정책을 정의할 수 있습니다.
<p>현재 자동화된 동의 적용은 Healthcare Shield 추가 기능 서비스를 구입한 조직에서만 사용할 수 있습니다.</p>
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
<p>Journey Optimizer에서는 기능 및 개체의 권한을 관리하기 위한 사용자 역할 및 액세스 정책 정의를 지원합니다. <strong>Adobe Experience Cloud 권한</strong>을 통해 역할을 만들고 관리하며, 이러한 역할에 대해 원하는 리소스 권한을 지정할 수 있습니다. 또한 권한을 사용하여 레이블, 샌드박스 및 특정 역할과 연관된 사용자를 관리할 수 있습니다.</p>
<p> 권한의 사용은 현재 선택한 고객으로 제한되며 향후 릴리스의 모든 환경에 배포될 예정입니다.</p>
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
<p>Journey Optimizer 사용자는 이제 여정이 예상대로 작동하지 않을 때 사용자 인터페이스를 통해 시스템 경고에 액세스하여 알림을 받을 수 있습니다. 사용 가능한 경고를 보고 구독할 수 있습니다. 이 릴리스 후에 대상자 읽기 활동이 정의된 시간대 내에 프로필을 처리하지 않은 경우 첫 번째 경고가 표시됩니다. 이 워크플로우의 잠금이 해제되어 더 많은 작업이 제공됩니다.</p>
<!--p>For more information, refer to the <a href="../reports/alerts.md">detailed documentation</a>.</p-->
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
<p>For more information, refer to the <a href="../building-journeys/read-audience.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->

### 개선 사항{#sept-2022-improvements}

**여정**

* **엔티티 데이터 세트**&#x200B;를 Adobe Journey Optimizer에서 바로 사용할 수 있는 데이터 세트로 이제 사용할 수 있습니다. 이 조회 데이터 세트에는 추적 및 피드백 데이터 세트 정보를 보강하는 메타 데이터가 포함되어 있습니다. 이렇게 하면 보다 이해하기 쉬운 데이터로 보고서 및 쿼리를 향상시킬 수 있습니다. [자세히 보기](../data/datasets-query-examples.md#entity-dataset)
* 동일한 이벤트에 대해 여정이 여러 번 잘못 트리거되는 것을 방지하기 위해 단일 여정(이벤트 또는 대상자 자격 조건 시작)에 새로운 가드레일을 추가했습니다. 프로필 재입장은 이제 기본 5분 동안 일시적으로 차단됩니다. [자세히 알아보기](../start/guardrails.md#events-g)

**관리**

* 허용 목록을 활성화하거나 비활성화할 때 이제 각 작업의 영향을 자세히 설명하는 새로운 경고가 표시됩니다. [자세히 보기](../configuration/allow-list.md#enable-allow-list)
* 채널 표면 생성, IP 풀 생성, 금지 목록 및 허용 목록 관리 및 SMS 채널 구성을 위한 사용자 인터페이스가 업데이트되었습니다.
* 이제 주어진 하위 도메인에 대한 첫 번째 채널 표면을 생성할 때 처리 시간은 10분에서 10일정도 소요되며, 해당 하위 도메인을 사용하는 후속 표면에 대해 최대 3시간만 소요됩니다. [자세히 보기](../configuration/channel-surfaces.md#create-channel-surface)
* 랜딩 페이지 사전 설정 및 랜딩 페이지 하위 도메인을 만들기 위한 사용자 인터페이스가 업데이트되었습니다. [자세히 보기](../landing-pages/lp-subdomains.md)

**감사 제어**

* Journey Optimizer를 사용하면 캠페인, 여정, 메시지, 랜딩 페이지 등과 같은 다양한 서비스 및 기능에 대해 시스템에서 사용자가 수행한 작업을 식별할 수 있습니다. 감사 로그 리소스에는 이제 다양한 다른 작업에 대한 변경 사항이 포함되어 있으며, 활동이 발생하면 자동으로 기록됩니다. [이 페이지](../privacy/audit-logs.md)에서 자세히 알아보십시오.

**아카이브 지원**

* 새로운 **엔티티 데이터 세트**&#x200B;에는 보관을 위해 모든 채널에서 보낸 메시지의 형식 및 구조를 내보낼 수 있는 템플릿 필드가 포함되어 있습니다. [자세히 보기](../configuration/archiving-support.md)

**랜딩 페이지**

* 이제 동일한 랜딩 페이지 내에서 다른 페이지에서 가져온 상황별 데이터를 사용할 수 있습니다. 예를 들어, 기본 랜딩 페이지의 구독 목록에 확인란을 연결하는 경우, 하위 페이지 “감사합니다”에서 해당 구독 목록을 사용할 수 있습니다. [자세히 보기](../landing-pages/lp-content.md#use-primary-page-context)

<!--* When configuring the primary page, you can now create additional data to enable storing information when the landing page is being submitted. [Learn more](../landing-pages/lp-content.md#use-additional-data)-->

<!--* You can now use information that was submitted on a landing page to send communications to your customers. For example, if a user subscribes to a given subscription list, you can leverage that information to send an email recommending other subscription lists to that user.-->

### 기타 변경 사항{#sept-2022-other}

* 여정 버스트 모드가 캠페인 신속 전달 모드로 대체되었습니다. [자세히 보기](../push/create-push.md#rapid-delivery)
* 성능을 개선하기 위해 대상자 읽기, 대상자 자격 조건 또는 비즈니스 이벤트 활동으로 시작하는 여정에서 더 이상 경험 이벤트 필드 그룹을 사용할 수 없습니다. 이 변경 사항은 새로운 여정에만 적용됩니다. 기존 동작은 현재 동작을 유지합니다. [자세히 보기](../start/guardrails.md#expression-editor)
* 예약된 대상자 읽기 여정의 1시간 제한이 제거되었습니다. 이제 이러한 여정을 지연 없이 실행할 수 있습니다.




## 2022년 8월 릴리스 {#aug-2022-release}

### 새로운 기능

<table>
<thead>
<tr>
<th><strong>Journey Optimizer에서 캠페인 만들고 관리하기</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer 캠페인으로 다양한 채널을 사용하는 특정 대상자에 일회성 콘텐츠를 게재할 수 있습니다. 여정을 사용할 때 작업은 순서대로 실행되도록 디자인됩니다. 캠페인을 사용하면 작업을 동시에 즉시 또는 지정한 일정에 따라 수행합니다. </p>
<img src="assets/do-not-localize/campaigns.gif"/>
<p><a href="../campaigns/get-started-with-campaigns.md">세부 설명서</a> 및 <a href="https://video.tv.adobe.com/v/346680">기능 비디오</a>에서 캠페인을 만드는 방법을 알아보세요.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>사용자에게 SMS 보내기(일반적인 가용성)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 <b>Sinch</b> 또는 <b>Twilio</b>와의 통합을 통해 Journey Optimizer에서 SMS를 만들고, 개인화하고, 보낼 수 있습니다.</p>
<img src="assets/do-not-localize/SMS.gif"/>
<p>이 <a href="../sms/create-sms.md">세부 설명서</a>에서 SMS를 만들고 보내는 방법을 알아보십시오.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>New Dynamic Expression Builder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create conditional content blocks across different authoring services to personalize your content.</p>
<p>In addition to the Personalization Expression Library, the Expression Editor provides a new Conditional Rule Builder to help you design and save your content blocks.</p>
<p>For more information, refer to the <a href="../building-journeys/read-audience.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->


### 개선 사항

**보고**

* 이제 [여정] 글로벌 보고서에서 동의 정책 테이블 및 그래프를 사용할 수 있습니다. 이 위젯을 사용하여 사용자 정의 작업의 정책에서 제외된 프로필을 추적할 수 있습니다. [자세히 보기](../reports/journey-global-report.md#journey-global)

  최신 위젯에 액세스하려면 다른 보고 대시보드를 재설정해야 합니다. 대시보드 사용자 정의에 대한 자세한 내용은 [자세한 설명서](../reports/global-report.md)를 참조하세요.

**관리**

* 이제 SMS 채널에 사용할 기본 전화 번호를 업데이트할 수 있습니다. [자세히 보기](../configuration/primary-email-addresses.md)


## 2022년 7월 릴리스 {#july-2022-release}

### 새로운 기능

<table>
<thead>
<tr>
<th><strong>새로운 인라인 메시징 흐름</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer는 여정에서 메시지를 작성할 수 있는 새로운 흐름을 제공합니다. 인라인 메시징을 사용하면 사용자가 상당한 시간을 절약하고 Journey Optimizer에서 이메일, 푸시 알림 또는 SMS를 만들고 전달하는 워크플로우 프로세스를 간소화할 수 있습니다. 메시지를 별도의 단계로 제거하고 대신 여정 캔버스에서 작업의 일부로 편집할 수 있는 인라인으로 만들어 사용자는 버튼을 더 적게 클릭하고 화면을 더 적게 탐색하여 콘텐츠를 디자인하고 편집해야 합니다.</p>
<img src="assets/do-not-localize/inline.gif"/>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>속성 기반 액세스 제어(제한된 가용성)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 조직 또는 데이터 사용 범위를 정의하는 레이블을 사용하여 스키마 필드를 식별할 수 있습니다. 관리자는 권한 인터페이스를 사용하여 XDM 스키마 필드에 적용되는 액세스 정책을 정의하고 사용자 또는 사용자 그룹(내부, 외부 또는 타사 사용자)에 부여된 액세스를 더 잘 관리하며 특정 데이터 유형(즉, 중요한 개인 데이터/SPD)에 대한 액세스를 관리할 수 있습니다.</p>
<p>속성 기반 액세스 제어 사용은 현재 선택한 사용자로만 제한되며 향후 릴리스의 모든 환경에 배포됩니다.</p>
<p>자세한 내용은 <a href="../administration/attribute-based-access.md">세부 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>일괄 의사 결정 작업</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 사용자 인터페이스에서 일괄 의사 결정 작업을 실행할 수 있으므로 일괄 API 작업을 실행하는 개발자가 필요하지 않으며 마케팅 관련 시간을 줄일 수 있습니다. 이 새 인터페이스를 사용하면 작업을 만들고 현재/과거 작업을 관리할 수 있습니다.</p>
<img src="assets/do-not-localize/batch.gif"/>
<p>자세한 내용은 <a href="../offers/batch-delivery.md">세부 설명서를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>의사 결정 시 가장 성과가 좋은 오퍼를 자동으로 사용(제한된 가용성)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 의사 결정 관리에 개인화된 최적화 모델 시스템을 사용할 수 있습니다. 이 새로운 유형의 모델을 사용하면 대상자와 오퍼의 성과를 기반으로 오퍼를 최적화하고 개인화할 수 있습니다.</p>
<p>개인화된 최적화 AI 모델의 사용은 현재 선택한 사용자로만 제한되며 향후 릴리스의 모든 환경에 배포됩니다.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>자세한 내용은 <a href="../offers/ranking/personalized-optimization-model.md">자세한 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>

### 개선 사항

**여정**

* **여정 종료** - 여정 캔버스에서 **종료** 활동이 팔레트에서 제거되었습니다. 이제 종료 태그가 각 경로 끝에 기본적으로 추가되므로 제거할 수 없습니다. 이 개선 사항을 통해 고객이 여정에서 드롭된 위치를 여정 전문가의 작업 없이 더 잘 보고할 수 있습니다. 자세한 내용은 [설명서](../building-journeys/end-journey.md) 및 [기능 비디오](https://video.tv.adobe.com/v/345376){target="_blank"}를 참조하세요.


* 이제 여정 속성에서 **프로필 시간대** 옵션이 기본적으로 선택되지 않습니다. [자세히 보기](../building-journeys/timezone-management.md#timezone-from-profiles)

**메시지**

* 이제 메시지 사전 설정은 **채널 표면**&#x200B;입니다. [자세히 알아보기](../configuration/channel-surfaces.md)

**관리**

* **PTR 기록 편집** - 이제 PTR 기록을 업데이트할 때 처리 시간은 최대 3시간만 소요됩니다. [자세히 보기](../configuration/ptr-records.md#processing)

* **허용 목록 UI** - 이제 Journey Optimizer 사용자 인터페이스를 사용하여 허용 목록에 새 이메일 주소 또는 도메인을 추가할 수 있습니다. [자세히 보기](../configuration/allow-list.md)

* **허용 목록 로직 업데이트** - 이제 목록이 비어 있더라도 기능이 활성화되는 즉시 허용 목록 로직이 적용됩니다. [자세히 보기](../configuration/allow-list.md#logic)

* **URL 추적 매개 변수** - 이제 표현식 편집기를 사용하여 이메일 표면(즉, 사전 설정)에서 URL 추적 매개 변수를 구성할 수 있습니다. [자세히 보기](../email/email-settings.md#url-tracking)

**의사 결정 관리**

* **대상자 크기** - 이제 의사 결정 규칙을 만들거나, 대상자 또는 규칙을 선택하여 오퍼 적격성을 설정하거나, 대상자 또는 규칙을 의사 결정 범위에 추가할 때 사용자 인터페이스에 대상자 크기 추정치를 보여 주는 새로운 구성 요소가 표시됩니다.


## 2022년 6월 릴리스 {#june-2022-release}

### 새로운 기능

<table>
<thead>
<tr>
<th><strong>사용자에게 SMS 보내기(제한된 가용성)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 <b>Sinch</b> 또는 <b>Twilio</b>와의 통합을 통해 Journey Optimizer에서 SMS를 만들고, 개인화하고, 보낼 수 있습니다.</p>
<!--img src="assets/do-not-localize/SMS.gif"/-->
<p>SMS 채널은 현재 조직 집합(제한된 가용성)에만 사용할 수 있습니다. 자세한 내용은 Adobe 직원에게 문의하십시오.</p>
<p>이 <a href="../sms/create-sms.md">세부 설명서</a>에서 SMS를 만들고 보내는 방법을 알아보십시오.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Adobe Stock 통합을 통해 더 효과적인 이미지 찾기</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Stock 및 Adobe Journey Optimizer 이메일 디자이너 통합 플러그인을 사용하면 메시지를 작성하는 데 사용할 이미지를 쉽게 탐색, 라이선싱 및 저장할 수 있습니다. </br> 새로운 <b>유사한 스톡 사진 찾기</b> 옵션으로도 이미지의 내용, 색상 및 컴포지션과 일치하는 스톡 사진을 찾을 수 있습니다. </p>
<!--img src="assets/do-not-localize/stock-rn.gif"/-->
<p>자세한 내용은 <a href="../content-management/stock.md">세부 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>모든 이메일에서 이메일 BCC 사용</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 이메일 BCC(숨은 참조) 기능을 사용하여 Adobe Journey Optimizer에서 보낸 이메일을 저장할 수 있습니다. 이메일 사전 설정에서 이 옵션을 활성화하여 전송된 모든 이메일이 BCC 주소로 블라인드(bcc)로 복사됩니다.</p>
<!--img src="assets/do-not-localize/bcc-rn.gif"/-->
<p>자세한 내용은 <a href="../configuration/archiving-support.md#bcc-email">세부 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>

<!--<table>
<thead>
<tr>
<th><strong>Automatically use the best performing offer in your decisions</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use personalized optimization model systems in Decision Management. This new type of model allows you to optimize and personalize offers based on audiences and offer performance.</p>
<p>The use of personalized optimization AI models is currently restricted to selected users, and will be deployed to all environments in a future release.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>For more information, refer to the <a href="../offers/ranking/personalized-optimization-model.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>샌드박스 간 개체 복사</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer 샌드박스에서 다른 샌드박스(예: 비프로덕션 샌드박스에서 프로덕션 샌드박스로)로 경험을 다시 만들 수 있습니다. 이 새 기능은 여정이 올바르게 실행하기 위해 사용하는 개체 등 전체 여정을 특정 환경에서 다른 환경으로 복사합니다. 여정 외에도 오퍼, 메시지, 스키마, 데이터 세트, 데이터 소스, 이벤트, 작업과 같은 다른 구성 요소를 복사할 수 있습니다.</p>
<p>자세한 내용은 <a href="../building-journeys/copy-to-sandbox.md">자세한 설명서</a>를 참조하세요.
</td>
</tr>
</tbody>
</table>




### 개선 사항

**의사 결정 관리**

* **HTML 및 JSON 파일 지원** - 이제 Adobe Experience Cloud 자산 라이브러리의 외부 HTML 및 JSON 파일을 오퍼 표시 컨텐츠로 끌어다 놓을 수 있습니다. [자세히 보기](../offers/offer-library/add-representations.md#html-json)


**이메일**

* **템플릿으로 저장** - 이제 이메일 콘텐츠를 템플릿으로 저장하고 다른 메시지를 만들 때 다시 사용할 수 있습니다. [자세히 알아보기](../content-management/content-templates.md#save-as-template)


**관리**

* **미리 보기 추적 URL 매개 변수** - 메시지 사전 설정을 구성할 때 URL 추적 매개 변수를 정의하는 경우 결과 추적 URL의 동적 미리 보기가 표시됩니다. [자세히 보기](../email/email-settings.md#url-tracking)

* **메시지 사전 설정 에디션** - 메시지 사전 설정을 업데이트할 때 드는 최대 처리 시간이 3시간으로 단축되었습니다. [자세히 보기](../configuration/channel-surfaces.md#edit-channel-surface)

* **IP 풀 에디션** - IP 풀을 업데이트할 때 드는 최대 처리 시간이 최대 3시간으로 단축되었습니다. [자세히 보기](../configuration/ip-pools.md#edit-ip-pool)




## 2022년 5월 릴리스 {#may-2022-release}

### 새로운 기능

<table>
<thead>
<tr>
<th><strong>메시지 빈도 규칙</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 메시지 및 작업에서 과도하게 요청된 프로필을 자동으로 제외하는 채널  비즈니스 규칙을 설정할 수 있습니다.</p>
<!--img src="assets/do-not-localize/frequency-rn.gif"/-->
<p>자세한 내용은 <a href="../configuration/frequency-rules.md">세부 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>의사 결정 관리 - AI 등급 자동 최적화 모델</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 의사 결정 관리에서 련된 모델 시스템을 사용할 수 있습니다. 이 새 기능은 주어진 프로필에 대해 표시할 오퍼에 등급을 지정합니다.</p>
<!--img src="assets/do-not-localize/optimization.gif"/-->
<p>자세한 내용은 <a href="../offers/offer-activities/configure-offer-selection.md#use-ranking-strategy">세부 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Attribute-based Access Control (ABAC)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Permission management in Journey Optimizer has been extended to data access. You can now manage data access for specific teams or groups of users (i.e. internal, external, 3rd parties) ​and manage access to specific types of data (i.e. Sensitive Personal Data/SPD).</p>
<p>This capability is available for a limited set of customers.</p>
<p>For more information, refer to the <a href="../landing-pages/create-lp.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Journey Optimizer 감사 로그</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Adobe Journey Optimizer 리소스에서 사용자가 수행한 작업을 모니터링할 수 있습니다.</p>
<!--img src="assets/do-not-localize/audit-rn.gif"/-->
<p>자세한 내용은 <a href="../privacy/audit-logs.md">자세한 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>

### 개선 사항

**개인화**

* **문자 숨김을 위한 새 도우미 함수** - `mask` 도우미 함수를 사용하면 문자열의 일부를 &quot;X&quot; 문자로 바꿀 수 있습니다. [자세히 보기](../personalization/functions/string.md#mask)

**랜딩 페이지**

* **양식이 없는 랜딩 페이지** - 이제 양식을 포함하지 않고 방문자의 작업이 필요 없는 랜딩 페이지를 만들어 게시할 수 있습니다.
* **랜딩 페이지 템플릿** - 이제 랜딩 페이지를 템플릿으로 저장하고 다른 랜딩 페이지를 만들 때 다시 사용할 수 있습니다. [자세히 보기](../landing-pages/lp-templates.md)
* **기본 페이지로 돌아가기** - 이제 동일한 랜딩 페이지 내의 하위 페이지에서 기본 페이지에 링크를 추가할 수 있습니다.
* **사용자 지정 JavaScript 지원** - 이제 사용자 지정 JavaScript를 랜딩 페이지 콘텐츠에 추가하여 고급 스타일을 수행하거나 사용자 지정 동작을 랜딩 페이지에 추가할 수 있습니다.    [자세히 보기](../landing-pages/lp-custom-js.md)

**여정**

* **대상자 읽기** - 이제 일회성 대상자 읽기 여정을 실행한 후 30일이 지나면 여정이 완료 상태로 이동합니다. 예약된 대상자 읽기의 경우 마지막 읽기를 실행한 후 30일이 경과한 시점에 이동합니다. [자세히 보기](../building-journeys/read-audience.md)
* **표현식 편집기** - 목록의 항목 수를 제한할 수 있도록 [limit](../building-journeys/functions/functionlimit.md) 함수가 추가되었습니다. 이제 [sort](../building-journeys/functions/functionsort.md) 함수를 사용하여 목록 개체를 정렬할 수 있습니다. 또한 [disctinct](../building-journeys/functions/functiondistinct.md) 및 [distinctWithNull](../building-journeys/functions/functiondistinctwithnull.md) 함수에 listObject에 대한 지원도 추가되었습니다.

**관리**

* **라이선스 사용 대시보드 업데이트** - 이제 사용자 인터페이스에서 [!DNL Adobe Journey Optimizer]사용할 수 있는 라이선스 사용 대시보드가 **라이선스** 평균 프로필 풍부도의 정확한 값을 반영합니다. 이 지표 표시에 감소가 표시되는데, 이것은 이제 라이선스 제한이 올바로 보고됨을 의미합니다. [자세히 보기](../audience/license-usage.md)


## 2022년 4월 릴리스 {#april-2022-release}

### 개선 사항

**랜딩 페이지**

* **새로운 옵트인/옵트아웃 확인란 옵션** - 이제 옵트인/옵트아웃에 대한 단일 확인란을 구독 랜딩 페이지에 삽입할 수 있습니다. 사용자는 동의(옵트인)하려면 이 확인란을 선택하고 동의를 제거(옵트아웃)하려면 선택을 해제해야 합니다. [자세히 보기](../landing-pages/design-lp.md#define-lp-specific-content)

* **랜딩 페이지 필드 미리 채우기** - 이제 사용자에게 랜딩 페이지 필드를 프로필 정보로 미리 채우는 기능을 제공할 수 있습니다. [자세히 알아보기](../landing-pages/create-lp.md#configure-primary-page)

**의사 결정 관리**

* **Edge의 Decisioning API** - Edge Decisioning API는 Offer Decisioning에서 관리하는 개인화된 오퍼를 제공하고 렌더링할 수 있습니다. 의사 결정 관리 UI(사용자 인터페이스) 또는 API를 사용하여 오퍼 및 기타 관련 개체를 만들 수 있습니다. [자세히 알아보기](../offers/api-reference/offer-delivery-api/edge-decisioning-api.md)

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
* Batch Decisioning API를 사용하면 한 번의 호출로 주어진 대상자 내 모든 프로필에 의사 결정 관리 기능을 사용할 수 있습니다. 대상자 내 각 프로필의 오퍼 콘텐츠가 AEP 데이터 세트에 배치되어 사용자 정의 일괄 처리 워크플로우에 사용할 수 있습니다. [자세히 알아보기](../offers/api-reference/offer-delivery-api/batch-decisioning-api.md)

**관리**

* 이제 메시지 사전 설정 수준에서 이메일 헤더의 구독 취소 링크를 활성화/비활성화하고 메시지 수준에서 사용자 정의 구독 취소 URL을 설정할 수 있습니다. [자세히 알아보기](../configuration/channel-surfaces.md#list-unsubscribe)
* 프로덕션 및 비프로덕션 샌드박스에서 [!DNL Journey Optimizer] 인터페이스를 통해 허용 목록을 활성화하고 비활성화할 수 있습니다. [자세히 알아보기](../configuration/allow-list.md#enable-allow-list)

**개인화**

* 이제 라이브러리에 개인화 표현식을 40개 넘게 저장할 수 있습니다. [자세히 알아보기](../personalization/use-expression-fragments.md)

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
<p>자세한 내용은 <a href="../personalization/use-expression-fragments.md">세부 설명서</a>를 참조하세요.</p>
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
The suppression list helps you with honoring the ISPs' feedback to preserve sending IP reputation. The allow list helps you ensure that you send only to those email addresses which are in the allowed list, and typically to ensure that you don't send mails to customers from your development sandbox.</p>
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
<p>자세한 내용은 <a href="../configuration/channel-surfaces.md#configure-email-settings">자세한 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>

### 개선 사항

**여정**

* 성능을 최적화하기 위해 1주일 동안 트리거되지 않은 테스트 모드의 모든 여정이 이제 초안 상태로 다시 전환합니다. [자세히 보기](../building-journeys/testing-the-journey.md#important_notes)
* 성능을 개선하기 위해 Journey Optimizer와 Adobe Campaign v7/v8 간 통합을 최적화했습니다. 빈도 설정 기본 구성이 호출 4,000회/5분으로 변경되었습니다. [자세히 보기](../action/acc-action.md#important-notes)

**보고**

* 이제 상태에 따라 게재를 필터링할 수 있습니다.
   * 이제 메시지 실행 목록에서 증명을 게재 목록에서 제외할 수 있습니다.
   * 라이브/전역 보고서에서 테스트 이벤트를 제외하도록 선택할 수 있습니다.

* 이제 메시지를 즉시 보낸 사람 수 및 1시간 최적화, 2시간 최적화 등을 통해 메시지를 보낸 사람 수 등 전송 시간 최적화 데이터에 대한 보고서에 액세스할 수 있습니다.

<!--* decision management reports are now available in Journey Optimizer. You can access the following metrics: Offers sent - Offers' impression rate - Offers' click rate - Breakdown report on Offers' sent.-->

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
<p>자세한 내용은 <a href="../building-journeys/condition-activity.md#profile_cap">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>여정 - 대상자 읽기 개선 사항</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>반복 <strong>대상자 읽기</strong> 활동에 <strong>증분 읽기</strong> 옵션을 추가했습니다. 이 옵션을 사용하면 여정의 마지막 실행 이후 대상자에 포함된 개인만 타겟팅할 수 있습니다. 첫 번째 실행 시에는 항상 모든 대상자 구성원을 타겟팅합니다.</p>
<p>자세한 내용은 <a href="../building-journeys/read-audience.md#configuring-segment-trigger-activity">자세한 설명서</a>를 참조하세요.
</td>
</tr>
</tbody>
</table>

### 개선 사항

**여정**

* 이제 Journey Optimizer 단계 이벤트를 [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=ko)의 다른 데이터 세트에 연결할 수 있습니다. 기본 제공 여정 단계 이벤트 스키마의 **profileID** 필드가 이제 ID 필드로 정의됩니다. [자세히 알아보기](../reports/sharing-overview.md#integration-cja)

**의사 결정 관리**

* 게시된 메시지에서 직접 또는 간접적으로 참조되는 오퍼, 대체 오퍼, 오퍼 컬렉션 또는 오퍼 결정을 업데이트하면 이제 다시 게시할 필요 없이 업데이트가 해당 메시지에 자동으로 반영됩니다. [자세히 알아보기](../offers/offers-e2e.md#insert-decision-in-email)

* 이제 주어진 테스트 프로필에 게재할 오퍼 시뮬레이션 시 기본 시뮬레이션 설정을 수정하고 시뮬레이션에 해당하는 코드를 볼 수 있습니다. 코드는 문제 해결용으로 사용할 수 있습니다. [자세히 알아보기](../offers/offer-activities/simulation.md#define-simulation-settings)

**관리**

* 이제 관리자는 CNAME 설정 하위 도메인으로 PTR 레코드를 편집할 수 있습니다. [자세히 알아보기](../configuration/ptr-records.md#edit-ptr-subdomains-cname)

**개인화**

* **즐겨찾기에 추가** - 개인화 작업 시 효율성을 개선하기 위해 즐겨찾기 저장 개념을 도입했습니다. 즐겨찾기 메뉴에 다양한 속성을 추가하면 가장 자주 사용하는 항목에 빠르게 액세스할 수 있습니다. [자세히 알아보기](../personalization/personalize.md#fav)
