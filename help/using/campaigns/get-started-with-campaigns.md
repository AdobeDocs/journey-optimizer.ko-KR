---
solution: Journey Optimizer
product: journey optimizer
title: 캠페인 시작
description: Journey Optimizer의 캠페인에 대해 자세히 알아보기
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: 캠페인, 방법 , 시작, Optimizer
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: 523f38743a827db4f8a94430ef02eda78d4151d9
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 100%

---

# 캠페인 시작 {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card3"
>title="캠페인 만들기"
>abstract="**Adobe Journey Optimizer**&#x200B;로 다양한 채널을 사용하는 특정 대상자에 일회성 콘텐츠를 게재할 수 있습니다. 여정을 사용할 때 작업은 순서대로 실행됩니다. 캠페인을 사용하면 작업을 동시에 즉시 또는 지정한 일정에 따라 수행합니다."


>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="캠페인"
>abstract="캠페인을 만들어 다양한 채널에서 일회성 콘텐츠를 특정 대상자에게 게재할 수 있습니다. 캠페인을 만들기 전 사용할 수 있는 채널 표면(즉, 메시지 사전 설정)과 Adobe Experience Platform 대상자가 있는지 확인합니다."

Journey Optimizer 캠페인으로 다양한 채널을 사용하는 특정 대상자에 일회성 콘텐츠를 게재할 수 있습니다. 여정을 사용할 때 작업은 순서대로 실행됩니다. 캠페인을 사용하면 작업을 동시에 즉시 또는 지정한 일정에 따라 수행합니다.

캠페인은 다음 두 가지 유형으로 만들 수 있습니다.

* **예약 캠페인**&#x200B;에서는 홍보 오퍼나 참여 캠페인, 공지, 법적 고지 사항 또는 정책 업데이트 등 마케팅 사용 사례에서 간단한 즉석 일괄 커뮤니케이션을 보낼 수 있습니다.
* **API 트리거 캠페인**&#x200B;을 통해 적시에 마케팅 커뮤니케이션을 대상자에게 보내거나 암호 재설정 등 개인에 대한 트랜잭션/운영 메시지를 보낼 수 있습니다. 이 경우 프로필 속성뿐만 아니라 실시간 상황 데이터, 즉 REST API 페이로드를 사용한 개인화가 필요할 수 있습니다.

캠페인을 만드는 주요 단계는 다음과 같습니다.

![](assets/create-campaign-process.png)

➡️ [비디오에서 이 기능 살펴보기](#video)

## 시작하기 전 {#campaign-prerequisites}

Journey Optimizer에서 캠페인을 처음으로 만들 때는 먼저 다음 전제 조건을 확인해야 합니다.

1. **적절한 권한이 필요합니다**. 캠페인은 캠페인 전체 관리자, 캠페인 승인자, 캠페인 관리자 및/또는 캠페인 확인자 등 캠페인 관련 **[!UICONTROL 제품 프로필]**&#x200B;에 액세스 권한이 있는 사용자만 사용할 수 있습니다.

   캠페인에 액세스할 수 없는 경우 권한을 확장해야 합니다. 조직의 [Adobe Admin Console](https://adminconsole.adobe.com/){target="_blank"}에 액세스할 권한이 있는 경우 아래 단계를 따르십시오. 없는 경우 조직의 Journey Optimizer 관리자에게 문의하십시오.

   +++캠페인 권한을 할당하는 방법 알아보기

   **[!UICONTROL 제품 프로필]**&#x200B;을 사용자에게 할당하는 방법:

   1. [Adobe Admin Console](https://adminconsole.adobe.com/){target="_blank"}에서 [!DNL Adobe Experience Platform] 제품을 선택합니다.

   1. **[!UICONTROL 제품 프로필]** 탭으로 이동하여 기본적으로 제공되는 캠페인 관련 **[!UICONTROL 제품 프로필]**(캠페인 전체 관리자나 캠페인 승인자, 캠페인 관리자 또는 캠페인 확인자) 중 하나를 선택합니다.

      Journey Optimizer 캠페인의 **[!UICONTROL 제품 프로필]**&#x200B;과 **[!UICONTROL 권한]**&#x200B;에 대한 자세한 내용은 [이 페이지를 참조하십시오](../administration/ootb-product-profiles.md).

      ![](assets/do-not-localize/admin_1.png)

   1. **[!UICONTROL 사용자 추가]**&#x200B;를 클릭하여 사용자에게 선택한 **[!UICONTROL 제품 프로필]**&#x200B;을 할당합니다.

      ![](assets/do-not-localize/admin_2.png)

   1. 사용자 이름이나 그룹 또는 이메일 주소를 입력하고 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

   이제 사용자가 **[!UICONTROL 캠페인]**&#x200B;에 액세스할 수 있습니다.

+++

1. **대상자가 필요합니다**. 캠페인을 만들기 전에 대상자를 사용할 수 있어야 합니다. [이 페이지에서](../audience/about-audiences.md) 대상자에 대해 자세히 알아보세요.
1. **채널 표면이 필요합니다**. 채널을 선택하려면 해당 채널 표면(즉, 사전 설정)을 만들고 사용할 수 있는 상태로 설정해야 합니다. 채널 표면에 대한 자세한 내용은 [이 페이지](../configuration/channel-surfaces.md)를 참조하십시오.

## 방법 비디오 {#video}

캠페인을 처음으로 만드는 방법을 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/346680?quality=12)
