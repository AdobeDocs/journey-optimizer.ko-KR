---
solution: Journey Optimizer
product: journey optimizer
title: 릴리스 정보
description: Journey Optimizer 릴리스 정보
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 3a932747de33ced59d68835a96386b7ac560e4fe
workflow-type: ht
source-wordcount: '233'
ht-degree: 100%

---

# 릴리스 정보 {#release-notes}

이 페이지에는 [!DNL Journey Optimizer]의 새로운 기능과 개선 사항이 모두 포함되어 있습니다. 또한 자세한 변경 사항은 [최신 설명서 업데이트](documentation-updates.md) 페이지를 참조하십시오.

[!DNL Adobe Journey Optimizer]은(는) 기본적으로 [!DNL Adobe Experience Platform] 기반으로 구축되었으며 최신 혁신 및 향상된 기능을 활용할 수 있습니다. [Adobe Experience Platform 릴리스 노트](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=ko-KR){target=&quot;_blank&quot;}에서 이러한 변경 사항에 대해 자세히 알아보십시오.

![뉴스레터](../assets/do-not-localize/nl-icon.png) 오늘 [Adobe Journey Optimizer 분기 뉴스레터](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;}에 등록하시면 분기마다 최신 제품 업데이트, 흥미로운 사례, 사용 사례, 팁 등을 받은 편지함에 바로 받을 수 있습니다.


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

* **반복 시 강제 재입력** 옵션이 반복 읽기 세그먼트 일정 매개 변수에 추가되었습니다. 이 옵션을 사용하면 여정에 여전히 존재하는 모든 프로필이 다음 실행 시 자동으로 종료되도록 할 수 있습니다. 옵션이 비활성화되면 프로필은 다른 경우에 다시 입력하기 전에 여정을 완료해야 합니다. [자세히 알아보기](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

**관리**

* 하위 도메인, 방문 페이지 하위 도메인, PTR 레코드 및 IP 풀 구성은 모든 샌드박스에 공통적이므로 이러한 구성 중 하나를 수정하면 프로덕션 샌드박스에도 영향을 미친다는 경고 메시지가 사용자 인터페이스에 추가되었습니다.
* 사용자 인터페이스에서 제외 목록을 CSV 파일로 업로드하는 단계가 수정되었습니다. [자세히 알아보기](../configuration/manage-suppression-list.md#download-suppression-list)

**캠페인**

* 이제 완료되고 중지된 캠페인을 보관할 수 있습니다. [자세히 알아보기](../campaigns/modify-stop-campaign.md#archive)
