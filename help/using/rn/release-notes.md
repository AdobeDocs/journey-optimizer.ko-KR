---
solution: Journey Optimizer
product: journey optimizer
title: 릴리스 정보
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
description: Journey Optimizer 릴리스 정보
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 299b34dec2e864fff5eb874b3fd491da80bc0c16
workflow-type: ht
source-wordcount: '418'
ht-degree: 100%

---

# 릴리스 정보 {#release-notes}


>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="새로운 기능"
>abstract="**Adobe Journey Optimizer**&#x200B;는 지속적으로 새로운 기능, 기존 기능 개선, 버그 해결을 제공합니다. 모든 변경 사항은 매달 마지막 주에 여기 있는 릴리스 정보에 통합됩니다."

[!DNL Adobe Journey Optimizer]는 지속적으로 새로운 기능, 기존 기능 개선, 버그 해결을 제공합니다. 모든 변경 사항은 매달 마지막 주에 여기 있는 릴리스 노트에 통합됩니다.

이전 릴리스 노트는 [이 페이지](release-notes-2023.md)에서 확인하실 수 있습니다. 또한 자세한 변경 사항은 [최신 설명서 업데이트](documentation-updates.md) 페이지를 참조하십시오.

[!DNL Adobe Journey Optimizer]은(는) 기본적으로 [!DNL Adobe Experience Platform] 기반으로 구축되었으며 최신 혁신 및 향상된 기능을 활용할 수 있습니다. 변경 사항에 대한 자세한 내용은 [Adobe Experience Platform 릴리스 노트](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=ko-KR){target="_blank"}를 참조하세요.

![뉴스레터](../assets/do-not-localize/nl-icon.png) 오늘 [Adobe Journey Optimizer 분기별 뉴스레터](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"}에 등록하여 분기마다 최신 제품 업데이트, 재미있는 이야기, 사용 사례, 팁 등을 메일로 직접 받아 보세요.

## 2023년 10월 릴리스 정보 {#oct-rn-2023}

### 새로운 기능{#oct-2023-features}

이번 릴리스에는 아래 목록에 있는 새로운 기능이 제공됩니다.

<table>
<thead>
<tr>
<th><strong>샌드박스 도구</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>샌드박스 도구를 사용하면 패키지 내보내기 및 가져오기를 활용하여 여러 샌드박스 간에 개체를 복사할 수 있습니다. 패키지는 단일 개체 또는 여러 개체로 구성될 수 있습니다. 패키지에 포함되는 모든 개체는 동일한 샌드박스에서 가져온 개체여야 합니다.</p>
<!--img src="../data/assets/dataset-export-setup.png"-->
<p>자세한 내용은 <a href="../building-journeys/copy-to-sandbox.md">세부 설명서</a>를 참고하십시오.</p>
</td>
</tr>
</tbody>
</table>

<!-- table>
<thead>
<tr>
<th><strong>Composed audiences in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use audiences created in composition workflows in your journeys to target customers. Once an audience composition is published, and the audience saved, use a Read Audience activity to select this new audience in your journey canvas.</p>
<img src="assets/channel-reports.png"/>
<p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p>
</tr>
</tbody>
</table -->

<table>
<thead>
<tr>
<th><strong>SMS를 통한 MMS(멀티미디어 메시지 서비스)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 [SMS 채널]을 통해 MMS(멀티미디어 메시지 서비스) 메시지를 보내 고객과 이미지, GIF 또는 비디오를 공유하는 기능이 추가되어 커뮤니케이션을 더욱 원활하게 진행할 수 있습니다. 단, 이 기능은 현재 Sinch에서만 사용할 수 있습니다.</p>
<img src="assets/do-not-localize/mms.gif"/>
<p>자세한 내용은 <a href="../sms/create-sms.md#mms-content">자세한 설명서</a>를 참조하세요.</p>
</tr>
</tbody>
</table>

### 개선 사항 {#oct-2023-improvements}

이 릴리스는 아래 목록에 있는 개선 사항과 함께 제공됩니다.

**대상자**

* 이제 CSV 파일에서 여정 및 캠페인으로 업로드한 대상자를 타겟팅할 수 있습니다. [자세히 알아보기](../audience/about-audiences.md#segments-in-journey-optimizer)
* 이제 대상자 구성을 통해 만든 대상자를 타겟팅하고 [여정]에서 데이터 보강 속성을 활용할 수 있습니다. [자세히 알아보기](../building-journeys/read-audience.md)

>[!AVAILABILITY]
>
>이 기능은 현재 Private Beta로 사용할 수 있습니다.

<!--
**Spam scoring for emails**

* When simulating an email content, a new option enables you to check how your content performs against inboxes spam filtering. This feature is currently proposed to a set of customers only (Limited Availability), and available for the Email channel.-->

**캠페인**

<!--* You can now stop a live one-time campaign, make modifications and resume it again. This improvement is available in Beta.-->
* 이제 캠페인 중 하나에서 오류가 발생하면 캠페인 목록의 캠페인 상태 옆에 경고 아이콘이 표시됩니다. [자세히 보기](../campaigns/modify-stop-campaign.md#statuses)

**여정**

* 모든 대기 시간에 정의할 수 있는 최대 기간이 기존 30일에서 29일로 변경되었습니다. 대기 시간이 여정 수명 30일을 초과하지 않도록 하기 위해 도입한 개선 사항입니다. 이것은 다음에 적용됩니다.

   * [대기 활동](../building-journeys/wait-activity.md)의 **시간** 필드
   * [여정 속성](../building-journeys/journey-gs.md#entrance)의 **재진입 대기 기간** 
   * [이벤트 활동](../building-journeys/general-events.md#events-specific-time)의 시간 초과 정의 내 **대기 기간** 필드.

<!--
**Consent in channel configuration**

* You can now select a marketing action at the channel surface level. When used in a surface, all consent policies associated with that marketing action are leveraged in order to respect the preferences of your customers.-->

**의사 결정 관리**

* 의사 결정 관리 인터페이스의 오퍼 캡핑 설정과 관련된 몇 가지 레이블을 업데이트했습니다. [자세히 알아보기](../offers/offer-library/add-constraints.md#capping)

