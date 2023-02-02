---
solution: Journey Optimizer
product: journey optimizer
title: 릴리스 정보
description: Journey Optimizer 릴리스 정보
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: ad0ca954d2ba15293bdde2715a7aaed62b040cce
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 92%

---

# 릴리스 정보 {#release-notes}

[!DNL Adobe Journey Optimizer]는 지속적으로 새로운 기능, 기존 기능 개선, 버그 해결을 제공합니다. 모든 변경 사항은 매달 마지막 주에 여기 있는 릴리스 노트에 통합됩니다.

이전 릴리스 노트는 [이 페이지](release-notes-2022.md)에서 확인하실 수 있습니다. 또한 자세한 변경 사항은 [최신 설명서 업데이트](documentation-updates.md) 페이지를 참조하십시오.

[!DNL Adobe Journey Optimizer]은(는) 기본적으로 [!DNL Adobe Experience Platform] 기반으로 구축되었으며 최신 혁신 및 향상된 기능을 활용할 수 있습니다. 변경 사항에 대한 자세한 내용은 [Adobe Experience Platform 릴리스 노트](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=ko-KR){target="_blank"}를 참조하세요.

![뉴스레터](../assets/do-not-localize/nl-icon.png) 오늘 [Adobe Journey Optimizer 분기별 뉴스레터](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"}에 등록하여 분기마다 최신 제품 업데이트, 재미있는 이야기, 사용 사례, 팁 등을 메일로 직접 받아 보세요.


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
<p><strong>주의</strong> - 데이터 위생 기능은 현재 <strong>Healthcare Shield</strong>와 <strong>Privacy and Security Shield</strong> 추가 기능 서비스를 구매한 조직에만 제공됩니다.</p><p>자세한 내용은 <a href="../privacy/data-hygiene.md">세부 설명서</a>를 참조하세요.

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
<p>이제 여정 및 캠페인 전반에서 활용하여 신속하게 재사용할 수 있는 독립형 콘텐츠 템플릿을 만들 수 있습니다.</p> 
</p>
<img src="assets/do-not-localize/content-template.gif"/>
<p>에서 콘텐츠 템플릿을 작성, 편집 및 사용하는 방법을 알아봅니다. <a href="https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/email-channel/content-templates.html">이 비디오</a>. 자세한 내용은 <a href="../email/content-templates.md">자세한 설명서</a>를 참조하세요.
</p>
</td>
</tr>
</tbody>
</table>

### 개선 사항 {#jan-2023-improvements}

**여정**

<!--
* The **Re-entrance wait period** field has been added to the journey properties. This field allows you to define the time to wait before allowing a profile to enter the journey again in unitary journeys (starting with an event or a segment qualification). This prevents journeys from being erroneously triggered multiple times for the same event. By default the field is set to 5 minutes. [Learn more](../building-journeys/journey-gs.md#entrance)

* Improvements have been made for **journey start and end dates**. If you have not specified a start date, it is now automatically added at publication time. For **Read segment** journeys, you can now add an end date. This allows profiles to exit automatically when the date is reached. [Learn more](../building-journeys/journey-gs.md#dates)
-->

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

<!--
**Decision management**

* Additional parameters have been added in placements creation screen. They allow you to control whether an offer can be duplicated across multiple placements, and to specify if the offer's content and metadata should be included in the API response. [Learn more](../offers/offer-library/creating-placements.md)-->

<!--* It is now possible to reset the offer capping counter on a daily, weekly or monthly basis. [Learn more](../offers/offer-library/add-constraints.md#capping)-->

**개인화**

* 새로운 도우미 함수 formatCurrency, charCodeAt, stringToDate, toString, formatNumber, toHexString을 사용할 수 있습니다. 또한 이제 toDateTimeOnly 함수에 문자열, 날짜, 긴 필드, int 필드 유형을 사용할 수 있습니다. [자세히 알아보기](../personalization/functions/functions.md)
