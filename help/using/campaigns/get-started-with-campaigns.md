---
title: 캠페인 시작
description: 에서 캠페인에 대해 자세히 알아보십시오 [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: 711fdf1dce0688d2e21d405a4e3e8777612b2f3b
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 3%

---

# 캠페인 시작 {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="캠페인"
>abstract="Campaign을 사용하면 여러 채널에서 특정 세그먼트에 일회성 콘텐츠를 제공할 수 있습니다. 새 캠페인을 만들기 전에 채널 표면(즉, 메시지 사전 설정)과 Adobe Experience Platform 세그먼트를 사용할 준비가 되었는지 확인하십시오."

## 캠페인 기본 정보 {#about}

>[!IMPORTANT]
>
>이 기능은 캠페인 관리자, 캠페인 승인자, 캠페인 관리자 및/또는 캠페인 뷰어와 같은 Campaign 관련 제품 프로필에 액세스할 수 있는 사용자만 사용할 수 있습니다. 제품 프로필을 할당하는 방법에 대한 자세한 내용은 [이 페이지](../administration/permissions.md).

캠페인을 사용하면 여러 채널을 사용하여 특정 세그먼트에 일회성 콘텐츠를 제공할 수 있습니다. 작업이 순서대로 실행되도록 디자인된 여정과 달리, 캠페인은 즉시 또는 지정된 일정에 따라 작업을 동시에 실행합니다.

이를 통해 홍보 오퍼, 참여 캠페인, 공지, 법적 고지 사항 또는 정책 업데이트와 같은 마케팅 사용 사례를 위한 간단한 임시 배치 커뮤니케이션을 전송할 수 있습니다.

<!--You can create two types of campaigns:

* **Scheduled campaigns** allow for simple ad-hoc batch communications for marketing use cases like promotional offers, engagement campaigns, announcements, legal notices, or policy updates.
* **API Triggered Campaigns** allow for simple transactional/operational messages with REST APIs (password reset, card abandonment, etc.), where the need may involve personalization using profile attributes and contextual data from payload.-->

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
