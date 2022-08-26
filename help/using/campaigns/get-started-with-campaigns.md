---
title: 캠페인 시작
description: 에서 캠페인에 대해 자세히 알아보십시오 [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: 8d8586a6c70b6fc01dbd1c2a8833079f422c93f7
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 4%

---

# 캠페인 시작 {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="캠페인"
>abstract="Campaign을 사용하면 여러 채널에서 특정 세그먼트에 일회성 콘텐츠를 제공할 수 있습니다. 새 캠페인을 만들기 전에 채널 표면(즉, 메시지 사전 설정)과 Adobe Experience Platform 세그먼트를 사용할 준비가 되었는지 확인하십시오."

## 캠페인 기본 정보 {#about}

캠페인을 사용하면 여러 채널을 사용하여 특정 세그먼트에 일회성 콘텐츠를 제공할 수 있습니다. 작업이 순서대로 실행되도록 디자인된 여정과 달리, 캠페인은 즉시 또는 지정된 일정에 따라 작업을 동시에 실행합니다.

이를 통해 홍보 오퍼, 참여 캠페인, 공지, 법적 고지 사항 또는 정책 업데이트와 같은 마케팅 사용 사례를 위한 간단한 임시 배치 커뮤니케이션을 전송할 수 있습니다.

➡️ [비디오에서 이 기능 살펴보기](#video)

<!--You can create two types of campaigns:

* **Scheduled campaigns** allow for simple ad-hoc batch communications for marketing use cases like promotional offers, engagement campaigns, announcements, legal notices, or policy updates.
* **API Triggered Campaigns** allow for simple transactional/operational messages with REST APIs (password reset, card abandonment, etc.), where the need may involve personalization using profile attributes and contextual data from payload.-->

## 전제 조건 {#campaign-prerequisites}

Campaign은 Campaign 관련 액세스 권한이 있는 사용자만 사용할 수 있습니다 **[!UICONTROL Product profile]** 캠페인 관리자, 캠페인 승인자, 캠페인 관리자 및/또는 캠페인 뷰어와 같은.

해당 **[!UICONTROL Product profile]** 사용자에게:

1. 에서 [!DNL Admin console]에서 을(를) 선택합니다. [!DNL Adobe Experience Platform] 제품.

1. 에서 **[!UICONTROL Product profile]** 탭에서 기본 제공 Campaign 관련 항목 중 하나를 선택합니다 **[!UICONTROL Product profile]**: 캠페인 관리자, 캠페인 승인자, 캠페인 관리자 또는 캠페인 뷰어.

   Campaign에 대한 자세한 정보 **[!UICONTROL Product profiles]** 및 **[!UICONTROL Permissions]**, 다음을 참조하십시오 [페이지](../administration/ootb-product-profiles.md).

   ![](assets/do-not-localize/admin_1.png)

1. 클릭 **[!UICONTROL Add user]** 사용자에게 할당하려면 **[!UICONTROL Product profile]**.

   ![](assets/do-not-localize/admin_2.png)

1. 사용자 이름, 그룹 또는 이메일 주소를 입력하고 **[!UICONTROL Save]**.

이제 사용자가 **[!UICONTROL Campaigns]**.

## 캠페인 액세스 {#access}

캠페인은 **[!UICONTROL Campaigns]** 메뉴 아래의 제품에서 사용할 수 있습니다.

기본적으로 이 목록에는 **[!UICONTROL Draft]**, **[!UICONTROL Scheduled]**, 및 **[!UICONTROL Live]** 상태. 중지, 완료 및 보관된 캠페인을 표시하려면 필터를 지워야 합니다.

![](assets/create-campaign-list.png)

## 캠페인 상태 {#statuses}

캠페인의 상태는 다음과 같습니다.

* **[!UICONTROL Draft]**: 캠페인이 편집 중이며 활성화되지 않았습니다.
* **[!UICONTROL Activating]**: 캠페인이 활성화되고 있습니다.
* **[!UICONTROL Live]**: 캠페인이 활성화되었습니다.
* **[!UICONTROL Scheduled]**: 캠페인이 특정 시작 날짜에 활성화되도록 구성되었습니다.
* **[!UICONTROL Stopped]**: 캠페인이 수동으로 중지되었습니다. 더 이상 활성화하거나 재사용할 수 없습니다( [캠페인 중지](modify-stop-campaign.md#stop))
* **[!UICONTROL Completed]**: 캠페인이 완료되었습니다. 이 상태는 캠페인이 활성화되면 3일 후 자동으로 지정되거나, 반복 실행이 있는 경우 캠페인의 종료 날짜에 할당됩니다.
* **[!UICONTROL Archived]**: 캠페인이 보관되었습니다.

>[!NOTE]
>
>다음 옆에 있는 &quot;초안 버전 열기&quot; 아이콘 **[!UICONTROL Live]** 또는 **[!UICONTROL Scheduled]** 상태는 캠페인의 새 버전이 만들어지고 아직 활성화되지 않았음을 나타냅니다( 참조) [캠페인 수정](modify-stop-campaign.md#modify)).

## 방법 비디오 {#video}

첫 번째 캠페인을 만드는 방법을 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/346680?quality=12)
