---
solution: Journey Optimizer
product: journey optimizer
title: 캠페인 수정 또는 중지
description: Journey Optimizer에서 라이브 캠페인을 수정, 중지 또는 복제하는 방법을 알아봅니다
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: 캠페인, 상태, 일정, 액세스, 최적기 관리
exl-id: 1b88c84e-9d92-4cc1-b9bf-27a2f1d29569
source-git-commit: 9657862f1c6bdb2399fcf3e6384bb9dec5b8f32b
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 2%

---

# 캠페인 관리 {#modify-stop-campaign}

캠페인이 활성화되면 언제든지 수정하거나 중지할 수 있습니다. 이러한 작업은 반복 실행이 있는 캠페인에만 사용할 수 있습니다.

또한 라이브 캠페인을 복제(한 번 또는 반복 실행)하여 새 캠페인을 만들고, 완료되었거나 중지된 캠페인을 보관할 수 있습니다.

## 캠페인 액세스 {#access}

캠페인은 **[!UICONTROL 캠페인]** 메뉴 아래의 제품에서 사용할 수 있습니다.

기본적으로 이 목록에는 **[!UICONTROL 초안]**, **[!UICONTROL 예약됨]**, 및 **[!UICONTROL 라이브]** 상태.

중지, 완료 및 보관된 캠페인을 표시하려면 필터를 지워야 합니다.

![](assets/create-campaign-list.png)

## 캠페인 상태 {#statuses}

캠페인의 상태는 다음과 같습니다.

* **[!UICONTROL 초안]**: 캠페인이 편집 중이며 활성화되지 않았습니다.
* **[!UICONTROL 활성화]**: 캠페인이 활성화되고 있습니다.
* **[!UICONTROL 라이브]**: 캠페인이 활성화되었습니다.
* **[!UICONTROL 예약됨]**: 캠페인이 특정 시작 날짜에 활성화되도록 구성되었습니다.
* **[!UICONTROL 중지됨]**: 캠페인이 수동으로 중지되었습니다. 더 이상 활성화하거나 재사용할 수 없습니다. [캠페인을 중지하는 방법 알아보기](modify-stop-campaign.md#stop)
* **[!UICONTROL 완료됨]**: 캠페인이 완료되었습니다. 이 상태는 캠페인이 활성화되면 3일 후 자동으로 지정되거나, 반복 실행이 있는 경우 캠페인의 종료 날짜에 할당됩니다.
* **[!UICONTROL 보관됨]**: 캠페인이 보관되었습니다. [캠페인 아카이브 방법 알아보기](modify-stop-campaign.md#archive)

>[!NOTE]
>
>다음 옆에 있는 &quot;초안 버전 열기&quot; 아이콘 **[!UICONTROL 라이브]** 또는 **[!UICONTROL 예약됨]** 상태는 캠페인의 새 버전이 만들어지고 아직 활성화되지 않았음을 나타냅니다. [자세히 알아보기](modify-stop-campaign.md#modify).

## 반복 캠페인 수정 {#modify}

반복 캠페인의 새 버전을 수정하고 만들려면 다음 단계를 수행합니다.

1. 캠페인을 연 다음 **[!UICONTROL 캠페인 수정]** 버튼을 클릭합니다.

1. 캠페인의 새 버전이 만들어집니다. 를 클릭하여 라이브 버전을 확인할 수 있습니다 **[!UICONTROL 라이브 버전 열기]**.

   ![](assets/create-campaign-draft.png)

   캠페인 목록에서 초안 버전이 진행 중인 활성화된 캠페인이 의 특정 아이콘과 함께 표시됩니다 **[!UICONTROL 상태]** 열. 이 아이콘을 클릭하여 캠페인의 초안 버전을 엽니다.

   ![](assets/create-campaign-edit-list.png)

1. 변경 사항이 준비되면 새 버전의 캠페인을 활성화할 수 있습니다(참조). [캠페인 검토 및 활성화](create-campaign.md#review-activate)).

   >[!IMPORTANT]
   >
   >초안을 활성화하면 캠페인의 라이브 버전이 대체됩니다.

## 반복 캠페인 중지 {#stop}

반복 캠페인을 중지하려면 해당 캠페인을 연 다음 **[!UICONTROL 캠페인 중지]** 버튼을 클릭합니다.

![](assets/create-campaign-stop.png)

>[!IMPORTANT]
>
>캠페인을 중지하면 진행 중인 전송이 중지되지는 않지만 전송 작업이 진행 중인 경우 예약된 전송을 중지하거나 다음 작업이 중지됩니다.

<!-- inbound campaign (inapp): can stop and resume -->

## 캠페인 복제 {#duplicate}

라이브 캠페인을 복제하여 새 캠페인을 만들 수 있습니다. 이렇게 하려면 캠페인을 연 다음 **[!UICONTROL 복제]**.

![](assets/create-campaign-duplicate.png)

## 캠페인 보관 {#archive}

시간이 지나면서 캠페인 목록이 지속적으로 증가하고 결과적으로 완료 및 중지된 캠페인을 검색하는 것이 더 어렵습니다.

이를 방지하기 위해 더 이상 필요하지 않은 완료 및 중지된 캠페인을 보관할 수 있습니다. 이렇게 하려면 줄임표 단추를 클릭한 다음 을 선택합니다 **[!UICONTROL 아카이브]**.

![](assets/create-campaign-archive.png)

그런 다음 목록의 전용 필터를 사용하여 보관된 캠페인을 검색할 수 있습니다. [캠페인에 액세스하는 방법 알아보기](get-started-with-campaigns.md#access)
