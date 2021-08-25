---
title: 릴리스 정보
description: Journey Optimizer 릴리스 정보
source-git-commit: 77d392cc09bd0923faf3d27e951a17cd702d257c
workflow-type: tm+mt
source-wordcount: '964'
ht-degree: 11%

---


# 릴리스 정보 {#release-notes}

이 페이지에는 [!DNL Journey Optimizer]의 새로운 기능과 개선 사항이 모두 포함되어 있습니다. 최신 [설명서 업데이트](documentation-updates.md)도 확인할 수 있습니다.


## 2021년 8월 릴리스 {#august-2021-release}

### 새로운 기능

<table>
<thead>
<tr>

<th><strong>최적의 시간에 메시지 전송 - 전송 시간 최적화</strong><br/></th>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer을 사용하는 모든 고객을 위해 최적의 시간에 푸시 또는 이메일을 자동으로 전송합니다. Adobe의 AI 서비스를 기반으로 하는 전송 시간 최적화는 이메일 또는 푸시 메시지를 보내는 가장 적합한 시간을 예측하여 이메일 또는 푸시 메시지를 전송함으로써 기존의 공개 및 클릭률 기록을 기반으로 참여를 극대화할 수 있습니다.</p>
<p>이 기능은 현재 베타 버전이며 베타 고객에게만 제공됩니다. 베타 프로그램에 참여하려면 Adobe 고객 지원 센터에 문의하십시오.</p>
<p>자세한 내용은 <a href="building-journeys/journeys-message.md#send-time-optimization">자세한 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>

<th><strong>비즈니스 이벤트에서 스키마 관계 활용 - 조회 테이블 관리</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 비즈니스 이벤트를 구성할 때 스키마 간의 관계를 활용할 수 있습니다. 이는 단일 이벤트를 구성할 때, 여정에서 조건을 사용할 때, 메시지 개인화에서, 사용자 지정 작업 개인화에서 연결된 테이블의 필드를 활용하는 기능 외에 있습니다.</p>
<p>자세한 내용은 <a href="event/experience-event-schema.md#leverage_schema_relationships">자세한 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>
<!--
<table>
<thead>
<tr>
<th><strong>Personalized URLs</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Personalized URLs take recipients to specific pages of a website, or to a personalized microsite, depending on the profile attributes. In Adobe Journey Optimizer, you can now add personalization to URLs in your message content. URL personalization can be applied to text and images, and use profile data or contextual data.</p>
<p>For more information, refer to the <a href="documentation-updates.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>이메일이 사용자에게 전달되는지 확인합니다. - 이메일 다시 시도</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 사전 설정별로 다시 시도 기간을 정의하여 더 이상 필요하지 않은 경우 다시 시도 시도가 더 이상 수행되지 않도록 할 수 있습니다. 예를 들어, 하루 동안만 유효한 링크가 포함된 암호 재설정 트랜잭션 메시지에 대해 재시도 기간을 24시간으로 설정할 수 있습니다. 다시 시도 설정은 전자 메일 채널에만 적용됩니다.</p>
<p>자세한 내용은 <a href="configuration/retries.md">자세한 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>
<!--
<table>
<thead>
<tr>
<th><strong>Customer Alerts</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now subscribe to event-based alerts regarding Adobe Journey Optimizer activities. The user interface allows you to view a history of received alerts based on metrics revealed by Adobe Experience Platform Observability Insights. The UI also allows you to view, enable, and disable available alert rules.</p>
<p>This feature is currently in beta version and only available to beta customers. To join the beta program, contact Adobe Customer Care.
</p>
<p>For more information, refer to the <a href="https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html">Adobe Experience Platform documentation</a>.</p>
</td>
</tr>
</tbody>
</table>
-->

### 개선 사항

**여정**

* **동적 헤더**  - 이제 HTTP 헤더 매개 변수로 동적 데이터를 전달할 수 있습니다. 이러한 매개 변수는 타임스탬프 또는 추적 ID와 같이 여정 작업 HTTP 호출을 받는 통합 시스템에서 사용할 수 있습니다. [자세히 알아보기](action/about-custom-action-configuration.md#url-configuration)
* **동적 URL 경로**  - 이제 사용자 지정 작업에 대한 동적 URL 경로를 설정할 수 있습니다. [자세히 알아보기](action/about-custom-action-configuration.md#url-configuration)
* 읽기 세그먼트의 전체 전송률이 초당 17,000개에서 20,000개로 변경되었습니다. [자세히 보기](building-journeys/read-segment.md#configuring-segment-trigger-activity)

**사용자 인터페이스**

* **검색**  - 이제 모든 페이지에서 통합 Experience Cloud 검색 필드에서 직접 비즈니스 개체를 검색하고 도움말 문서를 검색할 수 있습니다. [자세히 알아보기](user-interface.md#unified-search)
* **최근 항목**  - 이제 Adobe Journey Optimizer 홈 페이지의 최근 요소 표시가 추가 비즈니스 개체로 확장되었습니다. 이 업데이트를 사용하면 최근에 액세스한 항목에 메시지, 여정, 세그먼트, 스키마, 데이터 세트, 데이터 소스, 이벤트, 작업, 소스 및 대상이 포함됩니다. [자세히 알아보기](action/about-custom-action-configuration.md#passing-collection)

**컨텐츠 디자인**

* **배경**  - 이제 배경 이미지가 라이브 미리 보기에서 지원됩니다. [자세히 알아보기](preview.md)
* **한 번의 클릭으로 옵트아웃 링크**  - 이메일 콘텐츠에 새로운 유형의 링크를 삽입할 수 있습니다. 옵트아웃  **링크를** 사용하면 옵트아웃을 확인하기 위해 랜딩 페이지로 리디렉션되지 않고 한 번의 클릭으로 커뮤니케이션으로부터 구독을 취소할 수 있습니다. [자세히 알아보기](message-tracking.md#one-click-opt-out-link)

**개인화**

<!--* **Expression Editor** - You can now easily add a fall-back value when defining personalization: when personalization field is empty for a profile, the fall-back value will display. [Learn more](documentation-updates.md)-->

**이메일 구성**

* **허용 목록**  - 이제 API 호출을 통해 비프로덕션 샌드박스에서 허용 목록을 활성화하고 비활성화할 수 있습니다. [자세히 알아보기](allow-list.md#enable-allow-list)

<!--* **Suppression list** - Adding email addresses and domains into the suppression list is now available from the user interface, either one by one, either in bulk mode through a CSV file upload. [Learn more](configuration/manage-suppression-list.md#add-addresses-and-domains)-->
<!--* **Navigation** - The suppression list, which was accessible under the **Channels > Email configuration > General** menu, has been moved to the **Channels > Email configuration > Suppression list** menu for easier access. [Learn more](configuration/manage-suppression-list.md#access-suppression-list)-->


### 수정 사항

* 메시지 탭 탐색에서 액세스 가능성 문제가 해결되었습니다.
* 이메일 디자이너 레이블의 현지화 문제를 수정했습니다.
* 여정에서 두 개 이상의 노드를 선택하고 속성 패널에서 &#39;삭제&#39;를 클릭할 때 발생하는 문제를 수정했습니다.
* 여정에 사용된 작업에 새 헤더를 추가할 수 없는 문제를 수정했습니다.
* 이제 사용자 인터페이스에서 보다 명시적 경고를 통해 메시지 사전 설정을 만들지 못한 이유를 확인할 수 있습니다.


## 2021년 7월 릴리스 {#july-2021-release}

### 새로운 기능

<table>
<thead>
<tr>
<th><strong>메시지에서 메타데이터 사용 - 조회 테이블 관리</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer에 로드한 참조 데이터를 사용하여 경험을 보강합니다. 예로는 경험 이벤트에서 예약 ID에서 메타데이터를 조회하거나, 캔버스에서 사용할 경험 이벤트에서 sku의 제품 정보를 찾는 작업이 있습니다. </p>
<p>이제 스키마 간의 관계를 활용하여 하나의 데이터 세트를 다른 데이터 세트에 대한 조회 테이블로 사용할 수 있습니다. 그런 다음 단일 이벤트를 구성할 때, 여정에서 조건을 사용할 때, 메시지 개인화에서, 사용자 지정 작업 개인화에서 연결된 테이블의 모든 필드를 활용할 수 있습니다.</p>
<p>자세한 내용은 <a href="event/experience-event-schema.md#leverage_schema_relationships">자세한 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>허용 목록</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 테스트 목적으로 안전한 환경을 갖도록 샌드박스 수준에서 특정 전송 안전 목록을 정의할 수 있습니다. 허용 목록이 실수가 발생할 수 있는 비프로덕션 인스턴스에서 고객에게 원치 않는 메시지를 보낼 위험이 없습니다. 이 기능은 억제 API를 활용하여 활성화됩니다.</p>
<p>자세한 내용은 <a href="allow-list.md">자세한 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>

### 개선 사항

**여정**

* 동일한 샌드박스에서 동시에 실행되는 모든 읽기 세그먼트의 전체 전송률은 초당 17,000개의 메시지로 제한됩니다. [자세히 보기](building-journeys/read-segment.md#configuring-segment-trigger-activity)
* **캐시 기간** 필드가 데이터 소스 구성 창에서 제거되었습니다. [자세히 보기](datasource/about-data-sources.md)
* 이제 외부 데이터 소스의 경우 초당 15개의 호출의 최대 가용량 규칙이 자동으로 정의됩니다. [자세히 보기](configuration/external-systems.md#capping)
* 이제 라이브 여정의 경우 여정 속성 화면에 게시 날짜와 여정을 게시한 사용자의 이름이 표시됩니다. [자세히 보기](building-journeys/journey-gs.md#change-properties)
* 여정 목록 화면에서 여정 유형 필터가 추가되었습니다. [자세히 보기](user-interface.md#section_lgm_hpz_pgb)
* **[!UICONTROL Throttling rate]** 매개 변수가 세그먼트 읽기 활동에 추가되었습니다. [자세히 보기](building-journeys/read-segment.md#configuring-segment-trigger-activity)

**메시지 미리 보기 및 테스트**

* 이제 ID 및 네임스페이스가 **[!UICONTROL Preview]** 화면에 표시됩니다. [자세히 보기](preview.md#preview-your-messages)
* 이제 증명을 위한 테스트 전자 메일 수가 10개로 제한됩니다.
* 이제 증명에서 **제목 줄 접두사**&#x200B;에 사용할 수 있는 문자가 제한됩니다. [자세히 보기](preview.md#send-proofs)

**개인화 표현식 편집기**

* 도우미 드롭다운 목록의 이름이 변경되고 순서가 변경되었습니다.

### 수정 사항

* 배치 이메일 게재에 대해 중복 메시지가 전달되는 문제를 해결했습니다.
* 이제 다시 시도 기간이 끝나면 이메일 전송이 수행되지 않을 때 그에 따라 이벤트가 생성됩니다.
* PTR Records 화면에서 IP 정보가 누락되는 문제를 해결했습니다.
* 이제 표현식 편집기 내의 오퍼 레일의 현지화가 구현되었습니다.
* 정보 팝업에서 잘못된 간격이 수정되었습니다.
* `background-image` 속성이 있는 내부 스타일 시트가 지원되지 않는 HTML 파일을 업로드할 때 이메일 디자이너의 문제가 해결되었습니다.

