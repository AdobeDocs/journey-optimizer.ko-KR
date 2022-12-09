---
solution: Journey Optimizer
product: journey optimizer
title: 릴리스 노트
description: Journey Optimizer 릴리스 노트
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 3a932747de33ced59d68835a96386b7ac560e4fe
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---

# 릴리스 노트 {#release-notes}

이 페이지에는 의 새로운 기능과 개선 사항이 모두 포함되어 있습니다 [!DNL Journey Optimizer]. 또한 [최신 설명서 업데이트](documentation-updates.md) 페이지를 참조하십시오.

[!DNL Adobe Journey Optimizer] 기본적으로 [!DNL Adobe Experience Platform] 최신 혁신 및 향상된 기능을 활용할 수 있습니다. 에서 이러한 변경 사항에 대해 자세히 알아보십시오 [Adobe Experience Platform 릴리스 노트](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html){target=&quot;_blank&quot;}.

![뉴스레터](../assets/do-not-localize/nl-icon.png) 에 등록 [Adobe Journey Optimizer 분기별 뉴스레터](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html)오늘 {target=&quot;_blank&quot;}에서 최신 제품 업데이트, 흥미로운 스토리, 사용 사례, 팁 등을 분기마다 받은 편지함으로 직접 배달됩니다.


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

* 다음 **되풀이 시 강제 재진입** 반복 세그먼트 예약 매개 변수에 옵션이 추가되었습니다. 이 옵션을 사용하면 여정에 있는 모든 프로필을 다음 실행 시 자동으로 종료하도록 할 수 있습니다. 옵션이 비활성화되면 프로필이 다른 항목에 다시 입장하려면 먼저 여정을 완료해야 합니다. [추가 정보](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

**관리**

* 하위 도메인, 랜딩 페이지 하위 도메인, PTR 레코드 및 IP 풀 구성은 모든 샌드박스에 공통으로 사용된다는 메시지를 사용자 인터페이스에 추가하여 이러한 구성 중 하나를 수정하면 프로덕션 샌드박스에도 영향을 줍니다.
* 사용자 인터페이스에서 제외 목록을 CSV 파일로 업로드하는 단계가 수정되었습니다. [추가 정보](../configuration/manage-suppression-list.md#download-suppression-list)

**캠페인**

* 이제 완료되고 중지된 캠페인을 보관할 수 있습니다. [추가 정보](../campaigns/modify-stop-campaign.md#archive)
