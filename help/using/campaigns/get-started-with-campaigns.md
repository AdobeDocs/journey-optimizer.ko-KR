---
solution: Journey Optimizer
product: journey optimizer
title: 캠페인 시작
description: 에서 캠페인에 대해 자세히 알아보십시오 [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# 캠페인 시작 {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="캠페인"
>abstract="다양한 채널에서 특정 세그먼트에 일회성 콘텐츠를 전달하는 캠페인을 만듭니다. 캠페인을 만들기 전에 채널 표면(즉, 메시지 사전 설정)과 Adobe Experience Platform 세그먼트를 사용할 수 있는지 확인하십시오."

Journey Optimizer 캠페인을 사용하여 다양한 채널을 사용하여 특정 세그먼트에 일회성 콘텐츠를 전달할 수 있습니다. 여정을 사용할 때 작업이 순서대로 실행됩니다. 캠페인을 사용하면 작업이 동시에 즉시 또는 지정된 스케줄에 따라 수행됩니다.

두 가지 유형의 캠페인을 만들 수 있습니다.

* **예약된 캠페인** 홍보 오퍼, 참여 캠페인, 공지, 법적 고지 사항 또는 정책 업데이트와 같은 마케팅 사용 사례에 대해 간단한 임시 배치 커뮤니케이션을 허용합니다.
* **API 트리거 캠페인** 페이로드의 프로필 속성 및 컨텍스트 데이터를 사용하여 개인화를 수행해야 하는 경우 REST API(암호 재설정, 카드 중단 등)를 사용하여 간단한 트랜잭션/운영 메시지를 사용할 수 있습니다.

캠페인을 만드는 주요 단계는 다음과 같습니다.

![](assets/create-campaign-process.png)

➡️ [비디오에서 이 기능 살펴보기](#video)

## 시작하기 전 {#campaign-prerequisites}

Journey Optimizer에서 첫 번째 캠페인을 만들기 전에 다음 사전 요구 사항을 확인하십시오.

1. **적절한 권한이 필요합니다**. 캠페인은 캠페인 관련 액세스 권한이 있는 사용자만 사용할 수 있습니다 **[!UICONTROL Product profile]** 캠페인 관리자, 캠페인 승인자, 캠페인 관리자 및/또는 캠페인 뷰어와 같은.

   캠페인에 액세스할 수 없는 경우 권한을 확장해야 합니다. 액세스 권한이 있는 경우 [Adobe Admin Console](https://adminconsole.adobe.com/)조직에 대해 {target=&quot;_blank&quot;}에서 아래 단계를 수행하십시오. 없는 경우 Journey Optimizer 관리자에게 문의하십시오.

   +++캠페인 권한을 할당하는 방법 알아보기

   해당 **[!UICONTROL Product profile]** 사용자에게:

   1. From [Adobe Admin Console](https://adminconsole.adobe.com/){target=&quot;_blank&quot;}, [!DNL Adobe Experience Platform] 제품.

   1. 다음 위치로 이동합니다. **[!UICONTROL Product profile]** 탭에서 기본 제공 캠페인 관련 항목 중 하나를 선택합니다 **[!UICONTROL Product profile]**: 캠페인 관리자, 캠페인 승인자, 캠페인 관리자 또는 캠페인 뷰어.

      Journey Optimizer 캠페인에 대한 자세한 내용은 **[!UICONTROL Product profiles]** 및 **[!UICONTROL Permissions]**, [이 페이지 참조](../administration/ootb-product-profiles.md).

      ![](assets/do-not-localize/admin_1.png)

   1. 클릭 **[!UICONTROL Add user]** 사용자에게 할당하려면 **[!UICONTROL Product profile]**.

      ![](assets/do-not-localize/admin_2.png)

   1. 사용자 이름, 그룹 또는 이메일 주소를 입력하고 **[!UICONTROL Save]**.
   이제 사용자가 **[!UICONTROL Campaigns]**.

+++

1. **대상이 필요합니다.**. 캠페인을 만들기 전에 대상 세그먼트를 사용할 수 있어야 합니다. 대상 만들기에 대해 자세히 알아보기 [이 페이지에서](../segment/about-segments.md).
1. **채널 서피스가 필요합니다**. 채널을 선택하려면 해당 채널 서피스(즉, 사전 설정)를 만들고 사용할 수 있어야 합니다. 채널 표면에 대해 자세히 알아보기 [이 페이지에서](../configuration/channel-surfaces.md).

## 방법 비디오 {#video}

첫 번째 캠페인을 만드는 방법을 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/346680?quality=12)
