---
solution: Journey Optimizer
product: journey optimizer
title: 업데이트된 보고 환경
description: 전체 기간 보고서 시작
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: bfd88d2a-e7b8-4e3b-85a1-4a14b0ba56dc
source-git-commit: a9349cedc4da2a8e76e53f9e2b5185270cda2558
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 32%

---

# 전체 기간 보고서 시작 {#channel-report-gs-cja}

>[!CONTEXTUALHELP]
>id="cja_connections_enable_cja"
>title="Customer Journey Analytics 활성화"
>abstract="Customer Journey Analytics에서 이 보고서를 분석하려면 관리자에게 문의하여 조직에서 Customer Journey Analytics를 구매했으며 통합이 올바르게 구성되어 있는지 확인하십시오."
>additional-url="https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/channels/email/design-email/add-content/content-components#add-content-components" text="Customer Journey Analytics"

Journey Optimizer의 보고 기능은 Customer Journey Analytics 기능의 개선된 상호 운용성과 함께 양 플랫폼의 보고를 표준화하고 데이터의 일관성과 안정성을 개선합니다. 이렇게 Journey Optimizer와 Customer Journey Analytics가 원활하게 통합됨으로써 사용자가 성과 지표를 보다 명확하게 확인하여 확실한 정보에 근거한 결정을 내릴 수 있습니다.

이러한 보고 기능에 대한 액세스는 컨텍스트 및 제품 영역에 따라 다릅니다.

* **여정** - 여정의 컨텍스트에서 여정 또는 게재를 타겟팅하려면 **[!UICONTROL 여정]** 메뉴에서 여정에 액세스하고 **[!UICONTROL 보고서 보기]** 단추를 클릭합니다.

  기존 여정 목록에서 선택한 여정의 고급 메뉴에서 **[!UICONTROL 보고서]**&#x200B;를 선택할 수도 있습니다. [여정 보고서에 대해 자세히 알아보기](journey-global-report-cja.md)

  ![](assets/gs-cja-report-3.png)

* **캠페인** - 캠페인을 타깃팅하려면 **[!UICONTROL 캠페인]** 메뉴에서 캠페인에 액세스하고 **[!UICONTROL 보고서]** 버튼을 클릭한 다음 **[!UICONTROL 모든 시간 보고서 보기]**&#x200B;를 클릭합니다.

  기존 캠페인 목록에서 선택한 캠페인의 고급 메뉴에서 **[!UICONTROL 보고서]**&#x200B;를 선택할 수도 있습니다. [Campaign 보고서에 대해 자세히 알아보기](campaign-global-report-cja.md)

  ![](assets/gs-cja-report-2.png)

* **전역** - 환경 내의 모든 캠페인과 여정에 대한 지표를 타깃팅하려면 **[!UICONTROL 여정 관리]** 섹션 내의 **[!UICONTROL 보고서]** 메뉴로 이동하여 **개요** 보고서에 액세스하십시오. [개요 보고서에 대해 자세히 알아보기](channel-report-cja.md)

  ![](assets/gs-cja-report-1.png)

>[!IMPORTANT]
>
>Adobe Journey Optimizer의 보고는 현재 UTC로 표준화되었습니다. 보고 시간대를 사용자 지정하는 기능은 향후 릴리스에 도입될 예정입니다.

## 전제 조건 {#prerequisites}

* Customer Journey Analytics을 **not** 소유하거나 소유하고 있지만 **not**&#x200B;에서 Customer Journey Analytics 제품 프로필에 액세스할 수 있는 경우 Journey Optimizer에서 권한이 관리됩니다. 이 경우 **[!UICONTROL 채널 보고서 보기]** 권한 또는 관련 역할이 필요합니다. [자세히 알아보기](../administration/permissions.md)

* Customer Journey Analytics을 **소유**&#x200B;하고 Customer Journey Analytics 제품 프로필에 액세스할 수 있는 경우 다음이 필요합니다.

   * Customer Journey Analytics에 대한 **[!UICONTROL 대상 만들기]** 및 **[!UICONTROL 대상 보기]** 권한. [자세히 알아보기](https://experienceleague.adobe.com/ko/docs/analytics-platform/using/technotes/access-control){target="_blank"}

   * Adobe Journey Optimizer에 대한 **[!UICONTROL 프로필 관리]** 권한. [자세히 알아보기](../administration/permissions.md)

* **Adobe Journey Optimizer에서 기본 데이터 보기로 설정**&#x200B;을 설정하여 Customer Journey Analytics 데이터 보기를 구성해야 합니다. [데이터 보기에 대해 자세히 알아보기](https://experienceleague.adobe.com/ko/docs/analytics-platform/using/cja-dataviews/create-dataview){target="_blank"}


## 채널당 모든 시간 보고서

모든 채널에서 항상 글로벌 보고서를 사용할 수 있습니다. 자세한 정보를 얻는 데 필요한 채널에 대한 보고서를 선택합니다.

### 아웃바운드 채널

연결된 **글로벌 실시간 보고서**&#x200B;를 검색할 아웃바운드 채널을 선택하십시오.

<table style="table-layout:fixed"><tr style="border: 0;">
<td><img alt="이메일" src="../channels/assets/do-not-localize/email.png">
<div align="center"><p><strong>이메일 채널</strong></p><p><a href="campaign-global-report-cja-email.md"><strong>캠페인 보고서</strong></a></p><p><a href="journey-global-report-cja-email.md"><strong>여정 보고서</strong></a></p></div></td>
<td><a href="campaign-global-report-cja-sms.md"><img alt="sms" src="../channels/assets/do-not-localize/sms.png"></a>
<div align="center"><p><strong>SMS 채널</strong></p><p><a href="campaign-global-report-cja-sms.md"><strong>캠페인 보고서</strong></a></p><p><a href="journey-global-report-cja-sms.md"><strong>여정 보고서</strong></a></p></div></td>
<td><a href="campaign-global-report-cja-push.md"><img alt="푸시" src="../channels/assets/do-not-localize/push.png"></a>
<div align="center"><p><strong>푸시 채널</strong></p><p><a href="campaign-global-report-cja-push.md"><strong>캠페인 보고서</strong></a></p><p><a href="journey-global-report-cja-push.md"><strong>여정 보고서</strong></a></p></div></td>
<td><a href="campaign-global-report-cja-direct.md"><img alt="다이렉트 메일" src="../channels/assets/do-not-localize/direct-mail.jpg"></a>
<div align="center"><p><strong>DM 채널</strong></p><p><a href="campaign-global-report-cja-direct.md"><strong>캠페인 보고서</strong></a></p><p><a href="journey-global-report-cja-direct.md"><strong>여정 보고서</strong></a></p></div></td>
</tr></table>

### 인바운드 경험

연결된 **글로벌 전체 기간 보고서**&#x200B;를 검색할 인바운드 경험을 선택하십시오.

<table style="table-layout:fixed"><tr style="border: 0;">
<td><img alt="인앱" src="../channels/assets/do-not-localize/inapp.jpg">
<div align="center"><p><strong>인앱 채널</strong></p><p><a href="campaign-global-report-cja-inapp.md"><strong>캠페인 보고서</strong></a></p><p><a href="journey-global-report-cja-inapp.md"><strong>여정 보고서</strong></a></p></div></td>
<td><p><img alt="웹" src="../channels/assets/do-not-localize/web.jpg"></p>
<div align="center"><p><strong>웹 채널</strong></p><p><a href="campaign-global-report-cja-web.md"><strong>캠페인 보고서</strong></a></p><p><a href="journey-global-report-cja-web.md"><strong>여정 보고서</strong></a></p></div></td>
<td><img alt="코드 기반 경험" src="../channels/assets/do-not-localize/code.png">
<div align="center"><p><strong>코드 기반 경험</strong></p><p><a href="campaign-global-report-cja-code.md"><strong>캠페인 보고서</strong></a></p><p><a href="campaign-global-report-cja-code.md"><strong>여정 보고서</strong></a></p></div></td>
<td><img alt="콘텐츠 카드" src="../channels/assets/do-not-localize/cards.png">
<div align="center"><p><strong>콘텐츠 카드</strong></p><p><a href="campaign-global-report-cja-content.md"><strong>캠페인 보고서</strong></a></p><p><a href="journey-global-report-cja-content.md"><strong>여정 보고서</strong></a></p></div></td>
</tr></table>

## 사용 방법 비디오{#video}

아래 비디오에서는 Customer Journey Analytics에서 향상된 Journey Optimizer 보고를 사용하는 방법을 보여 줍니다.

>[!VIDEO](https://video.tv.adobe.com/v/3443158?captions=kor)