---
solution: Journey Optimizer
product: journey optimizer
title: 릴리스 정보
description: Journey Optimizer 릴리스 정보
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: e35aeba17f45145cc7712740cbcf1f0e169760fc
workflow-type: tm+mt
source-wordcount: '1435'
ht-degree: 77%

---

# 릴리스 정보 {#release-notes}

[!DNL Adobe Journey Optimizer]는 지속적으로 새로운 기능, 기존 기능 개선, 버그 해결을 제공합니다. 모든 변경 사항은 매달 마지막 주에 여기 있는 릴리스 노트에 통합됩니다.

이전 릴리스 노트는 [이 페이지](release-notes-2022.md)에서 확인하실 수 있습니다. 또한 자세한 변경 사항은 [최신 설명서 업데이트](documentation-updates.md) 페이지를 참조하십시오.

[!DNL Adobe Journey Optimizer]은(는) 기본적으로 [!DNL Adobe Experience Platform] 기반으로 구축되었으며 최신 혁신 및 향상된 기능을 활용할 수 있습니다. 변경 사항에 대한 자세한 내용은 [Adobe Experience Platform 릴리스 노트](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=ko-KR){target="_blank"}를 참조하세요.

![뉴스레터](../assets/do-not-localize/nl-icon.png) 오늘 [Adobe Journey Optimizer 분기별 뉴스레터](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"}에 등록하여 분기마다 최신 제품 업데이트, 재미있는 이야기, 사용 사례, 팁 등을 메일로 직접 받아 보세요.


## 2023년 3월 릴리스 노트 {#mar-2023}

아래 정보는 릴리스 가용 날짜까지 사전 통지 없이 변경될 수 있습니다. 업데이트된 설명서는 릴리스 날짜에 게시되고 직접 링크가 이 페이지에 추가됩니다.


### 새로운 기능{#mar-2023-features}

<table>
<thead>
<tr>
<th><strong>인앱 채널(일반 가용성)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 캠페인 내에서 앱 사용자에게 개인화된 인앱 메시지를 보낼 수 있습니다. Journey Optimizer를 사용하여 알림을 디자인하고 메시지 레이아웃, 디스플레이, 텍스트, 버튼을 사용자 정의하여 원활한 경험을 만들 수 있습니다.</p>
<img src="assets/do-not-localize/in-app.gif"/>
<p>자세한 내용은 <a href="../in-app/get-started-in-app.md">세부 설명서</a>를 참조하십시오.</p>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>SMS click tracking</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>With SMS click tracking, you can monitor the performance of your shortened URLs, identify who clicked on them, and use this data to retarget those customers with subsequent campaigns.</p>
<img src="assets/do-not-localize/sms-tracking.gif"/>
<p>For more information, refer to the <a href="../sms/create-sms.md#sms-content">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>여정에서 태그 사용(베타)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer 사용자는 이제 태그를 사용하여 비즈니스 개체를 정리할 수 있습니다. 태그를 사용하면 개체를 빠르고 간단하게 분류하여 검색을 개선할 수 있습니다. 이 기능은 현재 beta 버전이며 여정에 대해서만 사용할 수 있습니다.</p>
<p>자세한 내용은 <a href="../building-journeys/tags.md">자세한 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>


### 개선 사항 {#mar-2023-improvements}

**여정**

* 새로운 **조절 API** 에서는 외부 시스템 또는 API에서 급격한 트래픽 스파이크를 방지하기 위해 초당 전송된 이벤트 수에 제한을 설정할 수 있습니다. 설정 제한에 도달하면 모든 후속 API 호출이 수신되는 순서로 가능한 한 빨리 큐에 올라가 처리됩니다. 이 기능은 모든 샌드박스에서 하나의 조절 구성만 지원합니다. [자세히 알아보기](../configuration/external-systems.md)
* 여정 캔버스가 개선되어 보다 간단하고 향상된 사용자 경험을 제공합니다. 캔버스에서 각 경로의 끝에 빈 자리 표시자가 제거되었습니다. 이제 경로 끝에 활동을 드래그하여 추가하면 됩니다.
* 여정 캔버스에서 **종료** 태그는 더 이상 이전 활동의 이름으로 자동으로 설정되지 않습니다. 필요한 경우 사용자가 수동으로 사용자 지정 레이블을 추가할 수 있습니다.
* 여정 속성의 기본 시간 제한 및 오류 지속 시간이 5초에서 30초로 변경되었습니다. [자세히 알아보기](../configuration/external-systems.md#timeout)
* 읽기 세그먼트 활동의 기본 전송률이 초당 20,000개에서 5,000개로 변경되었습니다. [자세히 알아보기](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

<!-- 
* When adding an Email, SMS or Push action in a journey, the surface is now pre-filled, by default, with the last used surface for that channel.
* A new type of system alert has been introduced. You can now get notified when a custom action fails. [Learn more](../reports/alerts.md)
* Timeout and error management has been improved in journeys. Timeout and error paths are now always added on the canvas. A new toolbar button is available to show/hide these paths. [Learn more](../building-journeys/journey-gs.md#timeout_and_error)
* The Journey dashboard is now split in two tabs:
    * Use the **Overview** tab to access a new dashboard which displays key metrics related to your journeys.
    * Use the **Browse** tab to access list of all journeys.
-->

**의사 결정 관리**

* 최근 Adobe Experience Platform 전체에 걸친 태그 기능 릴리스와 관련하여 발생할 수 있는 혼란을 방지하기 위해 의사 결정 관리 태그의 이름을 “컬렉션 수식어”로 변경했습니다.

   의사 결정 관리 사용자 인터페이스에서는 “태그”라는 단어를 더 이상 사용하지 않지만 API와 데이터 세트 등 백엔드 서비스에서는 계속 사용한다는 점에 유의해 주시기 바랍니다.

* 이제 일별, 주별 또는 월별 기준으로 오퍼 한도 카운터를 재설정할 수 있습니다. [자세히 알아보기](../offers/offer-library/add-constraints.md#capping)

* Offer Decisioning 한도 적용 시 확인할 Adobe Experience Platform 이벤트를 선택할 수도 있습니다. [자세히 알아보기](../offers/offer-library/add-constraints.md#capping)

* 배치 만들기 화면에 추가 매개 변수가 추가되었습니다. 이 매개 변수를 사용하면 여러 배치에서 오퍼를 복제할 수 있는지 여부를 제어할 수 있고 오퍼의 컨텐츠 및 메타데이터를 API 응답에 포함해야 하는지 여부를 지정할 수 있습니다. [자세히 알아보기](../offers/offer-library/creating-placements.md)

**개인화**

* 이제 표현식 편집기에서 문자열 기반 프로필 속성에 대한 기본 대체 텍스트를 포함할 수 있습니다. 이러한 값은 선택한 속성이 결과를 반환하지 않을 경우 표시됩니다. [자세히 알아보기](../personalization/personalization-build-expressions.md#add)

<!--
**Reporting**

* The reporting widget functionality has been improved with the ability to customize how users view their data. With this improvement, users can now choose between multiple visualization options, including graph, table, and donut charts.

    To have access to the latest widgets, please note that you will have to reset the different reporting dashboards. For more information on dashboard customization, refer to the [detailed documentation](../reports/global-report.md#modify-dashboard).
-->

## 2023년 2월 릴리스 정보 {#feb-2023}

### 새로운 기능{#feb-2023-features}

<table>
<thead>
<tr>
<th><strong>인앱 채널(beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 캠페인 내에서 앱 사용자에게 개인화된 인앱 메시지를 보낼 수 있습니다. Journey Optimizer를 사용하여 알림을 디자인하고 메시지 레이아웃, 디스플레이, 텍스트, 버튼을 사용자 정의하여 원활한 경험을 만들 수 있습니다.</p>
<p><strong>주의</strong> - 이 기능은 현재 beta 버전으로 beta 고객에게만 제공됩니다. beta 프로그램에 참여하려면 Adobe 고객 지원 센터에 문의해 주세요.</p>
<img src="assets/do-not-localize/in-app.gif"/>
<p>자세한 내용은 <a href="../in-app/get-started-in-app.md">자세한 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Optimizer 데이터 세트를 클라우드 스토리지 대상으로 내보내기(beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 클라우드 스토리지 위치와 실시간 연결을 설정하여 데이터 세트의 콘텐츠를 내보낼 수 있습니다. 사용 가능한 대상은 Amazon S3 Cloud Storage, Azure Blob, Azure Data Lake Gen 2, Data Landing Zone, Google Cloud Storage, SFTP가 있습니다.</p>
<p><strong>주의</strong> - 이 기능은 현재 beta 버전으로 모든 Adobe Journey Optimizer 사용자가 사용할 수 있습니다. 아직 액세스 권한이 없는 경우 Adobe 담당자에게 대상 액세스 권한 부여를 요청하십시오.</p>
<img src="assets/do-not-localize/gif-destinations.gif"/>
<p>자세한 내용은 <a href="../data/export-datasets.md">자세한 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>

<!--

<table>
<thead>
<tr>
<th><strong>Performance Measurement in campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now measure the performance of your campaigns across inbound and outbound through dedicated reports. Adobe Journey Optimizer reports can retrieve additional metrics to use in the <strong>Objective</strong> tab of your campaign reports. </p>
<img src="assets/do-not-localize/performance_report.gif"/>
<p>For more information, refer to the <a href="../privacy/data-hygiene.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>

+++ Learn more about Performance Measurement

The **[!UICONTROL Objective]** tab of your Campaign report allows you to better fine-tune your deliveries' reports by targeting one specific metric. With this feature, you can effectively track and analyze your campaign's performance and make informed decisions to improve your results.

The **[!UICONTROL Objectives]** listed are linked to **[!UICONTROL Datasets]** that define a connection to a system in order to retrieve additional information. A list of pre-configured **[!UICONTROL Objectives]** is available, but you can also customize your report by adding new **[!UICONTROL Datasets]** and defining your own objectives. 

By selecting the desired Objectives, the **[!UICONTROL Performance overview]** and **[!UICONTROL Campaign objective]** widgets provide a comprehensive and insightful summary of your delivery performance, allowing you to closely monitor and evaluate the success of your campaign.

With the **[!UICONTROL Campaign objective]** widget, you can also choose to compare your primary objective against another performance metric.

Note that each widget can be resized and deleted as needed.
+++




<table>
<thead>
<tr>
<th><strong>Use Tags in your Journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>As a Journey Optimizer practitioner, you can now organize your business objects using tags. Tags are a quick and easy way of classifying objects to improve search. Tags are currently only available for Journeys.</p>
</td>
</tr>
</tbody>
</table>

-->

### 개선 사항 {#feb-2023-improvements}

**여정**

* 여정 속성에 **재입장 대기 시간** 필드가 추가되었습니다. 이 필드에서는 단일 여정(이벤트 또는 세그먼트 검증으로 시작)에서 프로필이 다시 여정에 들어오려면 기다려야 하는 시간을 정의할 수 있습니다. 이를 통해 동일한 이벤트에 대해 여정을 여러 번 트리거하는 오류를 방지할 수 있습니다. 이 필드는 기본적으로 5분으로 설정되어 있습니다. [자세히 알아보기](../building-journeys/journey-gs.md#entrance)

* **여정 시작 및 종료 일자**&#x200B;를 개선했습니다. 이제 시작 일자를 지정하지 않은 경우 게시할 때 자동으로 추가됩니다. 이제 **세그먼트 읽기** 여정에 종료 일자를 추가할 수 있습니다. 이렇게 하면 해당 일자가 되었을 때 프로필이 자동으로 종료됩니다. [자세히 알아보기](../building-journeys/journey-gs.md#dates)

<!--

* The Journey canvas has been enhanced for a simpler and improved user experience. At the end of each path in the canvas, the empty placeholders have been removed. You can now simply add your activities by dragging them anywhere between nodes. [Learn more](../building-journeys/using-the-journey-designer.md)

* Timeout and error management has been improved in journeys. Timeout and error paths are now always added on the canvas. A new toolbar button is available to show/hide these paths. [Learn more](../building-journeys/journey-gs.md#timeout_and_error)

* A new type of system alert has been introduced. You can now get notified when a custom action fails. [Learn more](../reports/alerts.md)

* The Journey dashboard is now split in two tabs:
    * Use the **Overview** tab to access a new dashboard which displays key metrics related to your journeys.
    * Use the **Browse** tab to access list of all journeys.
-->


**관리**

* **허용 목록** - 이제 허용 목록을 .csv 파일로 다운로드할 수 있습니다. [자세히 알아보기](../configuration/allow-list.md#download-allowed-list)

* **이메일 표면** - 이메일 표면 설정에 확인을 하나 더 추가했습니다. 이제 **답장 대상(이메일) 주소** 또는 **숨은 참조 이메일 주소**&#x200B;에서 사용하는 하위 도메인에 대한 MX 레코드가 제대로 구성되지 않은 경우 이메일 표면을 만들 수 없습니다. 해당 MX 레코드를 구성하거나 다른 MX 레코드를 사용해야 합니다. [자세히 알아보기](../email/email-settings.md#reply-to-email)

* **이메일 표면** - Adobe Analytics 추적과의 호환을 위해 이메일 표면 설정의 **URL 추적 매개 변수** 섹션에서 각 **값** 필드의 제한을 255자에서 5KB로 업데이트했습니다. [자세히 알아보기](../email/email-settings.md#url-tracking)

**의사 결정 관리**

* **배치** - 배치 만들기 화면에 추가 매개 변수가 추가되었습니다. 이 매개 변수를 사용하면 여러 배치에서 오퍼를 복제할 수 있는지 여부를 제어할 수 있고 오퍼의 컨텐츠 및 메타데이터를 API 응답에 포함해야 하는지 여부를 지정할 수 있습니다. [자세히 알아보기](../offers/offer-library/creating-placements.md)

* **URL 개인화** - 이제 URL을 오퍼 표시의 콘텐츠로 추가할 때 표현식 편집기를 사용하여 해당 URL을 개인화할 수 있습니다. [자세히 알아보기](../offers/offer-library/add-representations.md)

## 2023년 1월 릴리스 {#jan-2023-release}

### 새로운 기능{#jan-2023-features}

<table>
<thead>
<tr>
<th><strong>데이터 위생</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform은 프로그램 수준에서 소비자 기록 및 데이터 세트를 삭제함으로써 저장 데이터를 관리할 수 있도록 해 주는 데이터 위생 기능 세트를 제공합니다. 이제 Adobe Journey Optimizer에서 이 기능을 사용할 수 있습니다. </p>
<p>데이터 저장소를 관리하여 정보를 의도대로 사용하고 정확하지 않은 데이터를 수정해야 할 때 업데이트하며 조직 정책에 따라 필요한 경우 삭제할 수 있습니다.</p>
<p><strong>주의</strong> - 데이터 위생 기능은 현재 <strong>Healthcare Shield</strong>와 <strong>Privacy and Security Shield</strong> 추가 기능 서비스를 구매한 조직에만 제공됩니다.</p><p>자세한 내용은 <a href="../privacy/data-hygiene.md">세부 설명서</a>를 참조하십시오.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>이메일 콘텐츠 템플릿</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 빠른 재사용을 위해 여정과 캠페인에서 활용할 수 있는 독립 실행형 콘텐츠 템플릿을 만들 수 있습니다.</p> 
</p>
<img src="assets/do-not-localize/content-template.gif"/>
<p><a href="https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/email-channel/content-templates.html?lang=ko">이 비디오</a>에서 콘텐츠 템플릿을 작성, 편집, 사용하는 방법을 알아보십시오. 자세한 내용은 <a href="../email/content-templates.md">자세한 설명서</a>를 참조하세요.
</p>
</td>
</tr>
</tbody>
</table>

### 개선 사항 {#jan-2023-improvements}

**여정**

* 여정에 **세그먼트 검증**&#x200B;이나 **세그먼트 읽기**&#x200B;를 추가할 때 이제 기본적으로 네임스페이스를 마지막으로 사용한 네임스페이스를 사용하여 미리 채웁니다. [세그먼트 검증](../building-journeys/segment-qualification-events.md#about-segment-qualification) 및 [세그먼트 읽기](../building-journeys/read-segment.md#configuring-segment-trigger-activity) 섹션을 참조하세요.

* 여정 캔버스에서 도구 모음의 새 버튼을 통해 여정의 스크린샷을 다운로드할 수 있습니다.

**이메일 디자이너**

* 이제 **HTML 내보내기** 메뉴에서 이메일 콘텐츠를 내보낼 수 있습니다. 내보낸 파일은 압축(.ZIP) 파일 형태로 사용할 수 있습니다.

**관리**

* 새로운 하위 섹션에서 **답장 대상(이메일)** 주소를 작성하고 적절한 답장 관리를 보장하기 위한 추천 사항을 설명합니다. [자세히 알아보기](../email/email-settings.md#reply-to-email)

* **IP 풀**&#x200B;을 만들거나 편집할 때 이제 연결된 PTR 레코드가 IP 목록에 표시되며 선택한 IP 주소 위에 커서를 올렸을 때도 표시됩니다. [자세히 알아보기](../configuration/ip-pools.md#create-ip-pool)

* 이제 채널 표면에서 IP 풀을 선택한 후 IP 주소 위에 커서를 올리면 PTR 레코드 정보가 표시됩니다. [자세히 알아보기](../email/email-settings.md#subdomains-and-ip-pools)

* [PTR 레코드](../configuration/ptr-records.md#edit-ptr-record) 및 [실행 필드](../configuration/primary-email-addresses.md) 편집 사용자 인터페이스를 업데이트했습니다.

* 하위 도메인을 만들고 편집하는 사용자 인터페이스를 개선했습니다. [자세히 알아보기](../configuration/delegate-subdomain.md)

* 금지 목록 **최근 업로드** 화면을 업데이트했습니다. [자세히 알아보기](../configuration/manage-suppression-list.md#recent-uploads)

**캠페인**

* 이제 API에서 트리거하는 캠페인을 실행할 수 있도록 하는 샘플 cURL 요청이 자동으로 생성되어 캠페인 화면에서 사용할 수 있습니다. [자세히 알아보기](../campaigns/api-triggered-campaigns.md)


**개인화**

* 새로운 도우미 함수 formatCurrency, charCodeAt, stringToDate, toString, formatNumber, toHexString을 사용할 수 있습니다. 또한 이제 toDateTimeOnly 함수에 문자열, 날짜, 긴 필드, int 필드 유형을 사용할 수 있습니다. [자세히 알아보기](../personalization/functions/functions.md)
