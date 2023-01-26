---
solution: Journey Optimizer
product: journey optimizer
title: 릴리스 정보
description: Journey Optimizer 릴리스 정보
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: dc313d7cbee9e412b9294b644fddbc7840f90339
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 17%

---

# 릴리스 정보 {#release-notes}

[!DNL Adobe Journey Optimizer] 는 새로운 기능, 기존 기능의 개선 사항 및 버그 수정을 지속적으로 제공합니다. 모든 변경 사항은 이러한 릴리스 노트에서 각 달의 마지막 주에 통합됩니다.

이전 릴리스 노트는 [이 페이지](release-notes-2022.md). 또한 자세한 변경 사항은 [최신 설명서 업데이트](documentation-updates.md) 페이지를 참조하십시오.

[!DNL Adobe Journey Optimizer]은(는) 기본적으로 [!DNL Adobe Experience Platform] 기반으로 구축되었으며 최신 혁신 및 향상된 기능을 활용할 수 있습니다. 에서 이러한 변경 사항에 대해 자세히 알아보십시오 [Adobe Experience Platform 릴리스 노트](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=ko-KR){target="_blank"}.

![뉴스레터](../assets/do-not-localize/nl-icon.png) 에 등록 [Adobe Journey Optimizer 분기별 뉴스레터](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} 현재 최신 제품 업데이트, 흥미로운 사례, 활용 사례, 팁 등을 분기마다 받은 편지함으로 바로 배달됩니다.


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
<p>Adobe Experience Platform은 소비자 레코드 및 데이터 세트의 프로그래밍 방식 삭제를 통해 저장된 데이터를 관리할 수 있도록 해주는 데이터 위생 기능 세트를 제공합니다. 이제 Adobe Journey Optimizer에서 이 기능을 사용할 수 있습니다. </p>
<p>데이터 저장소를 관리하여 정보가 예상대로 사용되고 잘못된 데이터를 수정해야 할 때 가 업데이트되며, 조직 정책이 필요하다고 인정하는 경우 가 삭제됩니다.</p>
<p><strong>주의</strong> - 데이터 위생 기능은 현재 Healthcare Shield 추가 기능을 구입한 조직에서만 사용할 수 있습니다.</p>
<p>자세한 내용은 <a href="../privacy/data-hygiene.md">자세한 설명서</a>를 참조하세요.
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Email content templates</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create standalone content templates that can be leveraged across journeys and campaigns for quick reuse.</p> 
<p>For more information, refer to the <a href="../personalization/get-started-dynamic-content.md">detailed documentation</a>.
</td>
</tr>
</tbody>
</table>
-->

### 개선 사항 {#jan-2023-improvements}

**여정**

<!--
* The **Re-entrance wait period** field has been added to the journey properties. This field allows you to define the time to wait before allowing a profile to enter the journey again in unitary journeys (starting with an event or a segment qualification). This prevents journeys from being erroneously triggered multiple times for the same event. By default the field is set to 5 minutes. [Learn more](../building-journeys/journey-gs.md#entrance)

* Improvements have been made for **journey start and end dates**. If you have not specified a start date, it is now automatically added at publication time. For **Read segment** journeys, you can now add an end date. This allows profiles to exit automatically when the date is reached. [Learn more](../building-journeys/journey-gs.md#dates)
-->

* 추가 시 **세그먼트 자격** 또는 **세그먼트 읽기** 여정에서 네임스페이스는 기본적으로 마지막으로 사용된 네임스페이스와 함께 미리 채워집니다. 자세한 내용은 [세그먼트 자격](../building-journeys/segment-qualification-events.md#about-segment-qualification) 및 [세그먼트 읽기](../building-journeys/read-segment.md#configuring-segment-trigger-activity) 섹션에 자세히 설명되어 있습니다.

* 여정 캔버스에서 여정의 스크린샷을 다운로드할 수 있는 도구 모음에서 새 단추를 사용할 수 있습니다.

**이메일 디자이너**

* 이제 **내보내기 HTML** 메뉴 아래의 제품에서 사용할 수 있습니다. 내보낸 파일은 아카이브(.ZIP) 파일에서 사용할 수 있습니다.

**관리**

* 새로운 하위 섹션에서는 **회신 대상(이메일)** 주소 및 적절한 회신 관리 보장 [자세히 알아보기](../email/email-settings.md#reply-to-email)

* 만들거나 편집할 때 **IP 풀**&#x200B;를 눌러 연결된 PTR 레코드가 IP 목록에 표시되고 마우스로 선택한 IP 주소를 가리키면 표시됩니다. [자세히 알아보기](../configuration/ip-pools.md#create-ip-pool)

* 이제 채널 표면에서 IP 풀을 선택한 후 IP 주소를 마우스로 가리키면 PTR 레코드 정보가 표시됩니다. [자세히 알아보기](../email/email-settings.md#subdomains-and-ip-pools)

* 편집할 사용자 인터페이스 [PTR 레코드](../configuration/ptr-records.md#edit-ptr-record) 및 [실행 필드](../configuration/primary-email-addresses.md) 이 업데이트되었습니다.

* 하위 도메인을 만들고 편집하기 위한 사용자 인터페이스가 개선되었습니다. [자세히 알아보기](../configuration/delegate-subdomain.md)

* 제외 목록 **최근 업로드** 화면이 업데이트되었습니다. [자세히 알아보기](../configuration/manage-suppression-list.md#recent-uploads)

**캠페인**

* 이제 API 트리거된 캠페인 실행을 허용하는 샘플 cURL 요청이 자동으로 생성되어 캠페인 화면에서 사용할 수 있습니다. [자세히 알아보기](../campaigns/api-triggered-campaigns.md)

<!--
**Decision management**

* Additional parameters have been added in placements creation screen. They allow you to control whether an offer can be duplicated across multiple placements, and to specify if the offer's content and metadata should be included in the API response. [Learn more](../offers/offer-library/creating-placements.md)-->

<!--* It is now possible to reset the offer capping counter on a daily, weekly or monthly basis. [Learn more](../offers/offer-library/add-constraints.md#capping)-->

**개인화**

* 새 도우미 기능을 사용할 수 있습니다. formatCurrency, charCodeAt, stringToDate, toString, formatNumber 및 toHexString. 또한 toDateTimeOnly 함수는 이제 문자열, 날짜, 긴 필드 및 int 필드 유형을 허용합니다. [자세히 알아보기](../personalization/functions/functions.md)
