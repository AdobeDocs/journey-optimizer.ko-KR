---
title: 릴리스 정보
description: Journey Optimizer 릴리스 정보
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 711fdf1dce0688d2e21d405a4e3e8777612b2f3b
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 50%

---

# 릴리스 정보 {#release-notes}

이 페이지에는 [!DNL Journey Optimizer]의 새로운 기능과 개선 사항이 모두 포함되어 있습니다. 또한 자세한 변경 사항은 [최신 설명서 업데이트](documentation-updates.md) 페이지를 참조하십시오.

[!DNL Adobe Journey Optimizer]은(는) 기본적으로 [!DNL Adobe Experience Platform] 기반으로 구축되었으며 최신 혁신 및 향상된 기능을 활용할 수 있습니다. [Adobe Experience Platform 릴리스 노트](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=ko-KR){target=&quot;_blank&quot;}에서 이러한 변경 사항에 대해 자세히 알아보십시오.

![뉴스레터](../assets/do-not-localize/nl-icon.png) 오늘 [Adobe Journey Optimizer 분기 뉴스레터](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;}에 등록하시면 분기마다 최신 제품 업데이트, 흥미로운 사례, 사용 사례, 팁 등을 받은 편지함에 바로 받을 수 있습니다.

## 2022년 8월 릴리스 {#aug-2022-release}

### 새로운 기능

<table>
<thead>
<tr>
<th><strong>Journey Optimizer에서 캠페인 만들기 및 관리</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer 캠페인을 사용하여 다양한 채널을 사용하여 특정 세그먼트에 일회성 콘텐츠를 전달할 수 있습니다. 여정을 사용할 때 작업은 순서대로 실행되도록 디자인됩니다. 캠페인을 사용하면 작업이 동시에 즉시 또는 지정된 스케줄에 따라 수행됩니다. </p>
<img src="assets/do-not-localize/campaigns.gif"/>
<p>캠페인을 만드는 방법을 알아봅니다 <a href="../campaigns/get-started-with-campaigns.md">세부 설명서</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>사용자에게 SMS 보내기(일반 가용성)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 <b>Sinch</b> 또는 <b>Twilio</b>와의 통합을 통해 Journey Optimizer에서 SMS를 만들고, 개인화하고, 보낼 수 있습니다.</p>
<img src="assets/do-not-localize/SMS.gif"/>
<p>이 <a href="../messages/create-sms.md">세부 설명서</a>에서 SMS를 만들고 보내는 방법을 알아보십시오.</p>
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
<p>For more information, refer to the <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->



### 개선 사항

**보고**

* 이제 여정 글로벌 보고서에서 동의 정책 테이블 및 그래프를 사용할 수 있습니다. 이러한 위젯을 사용하면 사용자 지정 작업의 정책에서 제외된 프로필을 추적할 수 있습니다. [자세히 보기](../reports/journey-global-report.md#journey-global)

   최신 위젯에 액세스하려면 다른 보고 대시보드를 재설정해야 합니다. 대시보드 사용자 지정에 대한 자세한 내용은 [자세한 설명서](../reports/global-report.md).

**관리**

* 이제 SMS 채널에 사용할 기본 전화 번호를 업데이트할 수 있습니다. [자세히 보기](../configuration/primary-email-addresses.md)