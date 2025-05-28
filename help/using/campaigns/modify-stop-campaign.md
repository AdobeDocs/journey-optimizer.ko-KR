---
solution: Journey Optimizer
product: journey optimizer
title: 캠페인 수정 또는 중지
description: Journey Optimizer에서 라이브 캠페인을 수정, 중지 또는 복제하는 방법에 대해 알아봅니다
feature: Campaigns
topic: Content Management
role: User
level: Beginner
keywords: 캠페인, 상태, 일정, 액세스, 최적화 도구 관리
exl-id: 1b88c84e-9d92-4cc1-b9bf-27a2f1d29569
source-git-commit: 29d12b6190f49e7f3f6fd2760e522a5a62c0de87
workflow-type: tm+mt
source-wordcount: '868'
ht-degree: 1%

---

# 캠페인 관리 {#modify-stop-campaign}

캠페인이 활성화되면 언제든지 수정하거나 중지할 수 있습니다. 이러한 작업은 반복 실행이 있는 캠페인에만 사용할 수 있습니다.

또한 라이브 캠페인(한 번 또는 반복 실행으로 실행)을 복제하여 새 캠페인을 만들고, 완료되거나 중지된 캠페인을 보관할 수 있습니다.

## 캠페인 액세스 {#access}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_view"
>title="캠페인 목록 및 달력 보기"
>abstract="[!DNL Journey Optimizer]은(는) 캠페인 목록 외에 캠페인의 일정 보기를 제공하여 일정에 대한 명확한 시각적 표현을 제공합니다. 이 단추를 사용하여 언제든지 목록 보기와 달력 보기 간에 전환할 수 있습니다."

캠페인은 **[!UICONTROL 캠페인]** 메뉴에서 액세스할 수 있습니다.

기본적으로 목록에는 **[!UICONTROL 초안]**, **[!UICONTROL 예약됨]** 및 **[!UICONTROL 라이브]** 상태의 모든 캠페인이 표시됩니다. 중지, 완료 및 보관된 캠페인을 표시하려면 필터를 지워야 합니다.

![](assets/create-campaign-list.png)

캠페인 유형 및 채널 또는 캠페인 생성 시 캠페인에 할당된 태그를 기반으로 목록을 필터링할 수도 있습니다. [캠페인에 태그를 할당하는 방법을 알아보세요](create-campaign.md#create)

## 캠페인 캘린더 {#calendar}

[!DNL Journey Optimizer]은(는) 캠페인 목록 외에 캠페인의 일정 보기를 제공하여 일정에 대한 명확한 시각적 표현을 제공합니다.

>[!AVAILABILITY]
>
>달력 보기는 현재 조직 집합(제한된 가용성)에만 사용할 수 있습니다. 액세스 권한을 요청하려면 [이 양식](https://forms.cloud.microsoft/r/FC49afuJVi){target=”_blank”}을 사용하세요.
>
>이 기능은 현재 개발 중입니다. 상단 메뉴의 **[!UICONTROL Beta 피드백]** 버튼을 사용하여 입력 및 요청을 환영합니다.

캘린더에 현재 주에 예약된 모든 캠페인이 표시됩니다. 달력 위에 있는 화살표 단추를 사용하여 주 사이를 이동합니다.

![실시간 캠페인을 표시하는 달력 보기](assets/campaigns-timeline.png)

캠페인 표시 방법:

* 기본적으로 달력 표에는 선택한 주에 대한 모든 라이브 및 예약된 캠페인이 표시됩니다. 추가 필터 옵션은 특정 유형 또는 채널의 완료된 활성화, 중지된 활성화 및 완료된 활성화를 표시할 수 있습니다.
* 초안 캠페인은 표시되지 않습니다.
* 여러 날에 걸친 캠페인이 달력 격자의 맨 위에 나타납니다.
* 시작 시간을 지정하지 않으면 가장 가까운 수동 활성화 시간이 달력에 배치됩니다.
* 캠페인은 1시간 시간대로 표시되지만, 실제 전송 또는 완료 시간은 반영되지 않습니다.

캠페인에 대한 자세한 내용을 보려면 해당 시각적 블록을 클릭하여 캠페인에 대한 세부 정보를 엽니다.

특정 캠페인에 대한 세부 정보를 보려면 목록에서 해당 캠페인을 선택합니다. 유형, 보고서에 대한 액세스 권한 또는 할당된 태그 등 캠페인에 대한 다양한 정보가 있는 정보 창이 열립니다.

정보 창이 열린 ![캠페인 목록](assets/campaign-rail.png)

## 캠페인 상태 및 경고 {#statuses}

캠페인은 여러 상태를 가질 수 있습니다.

* **[!UICONTROL 초안]**: 캠페인이 편집 중이며 활성화되지 않았습니다.
* **[!UICONTROL 활성화]**: 캠페인이 활성화 중입니다.
* **[!UICONTROL 처리]** *(전자 메일 캠페인만 해당)*: 대상자 내보내기가 완료되었으며 캠페인이 게시되고 있습니다.
* **[!UICONTROL Live]**: 캠페인이 활성화되었습니다.
* **[!UICONTROL 예약됨]**: 캠페인이 특정 시작 날짜에 활성화되도록 구성되었습니다.
* **[!UICONTROL 중지됨]**: 캠페인이 수동으로 중지되었습니다. 더 이상 활성화하거나 재사용할 수 없습니다. [캠페인을 중지하는 방법 알아보기](modify-stop-campaign.md#stop)
* **[!UICONTROL 완료]**: 캠페인이 완료되었습니다. 이 상태는 캠페인이 활성화된 후 3일 또는 캠페인 종료 날짜(반복 실행이 있는 경우)에 자동으로 할당됩니다.
* **[!UICONTROL 보관됨]**: 캠페인이 보관되었습니다. [캠페인을 보관하는 방법 알아보기](modify-stop-campaign.md#archive)

>[!NOTE]
>
>**[!UICONTROL Live]** 또는 **[!UICONTROL 예약됨]** 상태 옆에 있는 &quot;초안 버전 열기&quot; 아이콘은 캠페인의 새 버전이 만들어졌고 아직 활성화되지 않았음을 나타냅니다. [자세히 알아보기](modify-stop-campaign.md#modify).

캠페인 중 하나에서 오류가 발생하면 캠페인 상태와 함께 경고 아이콘이 표시됩니다. 경고와 관련된 정보를 표시하려면 이 패널을 클릭합니다. 이러한 경고는 캠페인 메시지가 게시되지 않았거나 선택한 구성이 잘못된 경우와 같은 다양한 상황에서 발생할 수 있습니다.

![](assets/campaign-alerts.png)

## 반복 캠페인 수정 {#modify}

반복 캠페인의 새 버전을 수정하고 만들려면 다음 단계를 수행합니다.

1. 캠페인을 열고 **[!UICONTROL 캠페인 수정]** 단추를 클릭합니다.

1. 캠페인의 새 버전이 만들어집니다. **[!UICONTROL 라이브 버전 열기]**&#x200B;를 클릭하여 라이브 버전을 확인할 수 있습니다.

   ![](assets/create-campaign-draft.png)

   캠페인 목록에서 진행 중인 초안 버전의 활성화된 캠페인이 **[!UICONTROL 상태]** 열에 특정 아이콘과 함께 표시됩니다. 이 아이콘을 클릭하여 캠페인의 초안 버전을 엽니다.

   ![](assets/create-campaign-edit-list.png)

1. 변경 사항이 준비되면 새 버전의 캠페인을 활성화할 수 있습니다([캠페인 검토 및 활성화](create-campaign.md#review-activate) 참조).

   >[!IMPORTANT]
   >
   >초안을 활성화하면 캠페인의 라이브 버전이 대체됩니다.

## 반복 캠페인 중지 {#stop}

반복 캠페인을 중지하려면 해당 캠페인을 연 다음 **[!UICONTROL 캠페인 중지]** 단추를 클릭하십시오.

![](assets/create-campaign-stop.png)

>[!IMPORTANT]
>
>캠페인을 중지해도 진행 중인 전송은 중지되지 않지만, 전송이 이미 진행 중인 경우 예약된 전송 또는 다음 작업이 중지됩니다.

<!-- inbound campaign (inapp): can stop and resume -->

## 캠페인 복제 {#duplicate}

라이브 캠페인을 복제하여 새 캠페인을 만들 수 있습니다. 이렇게 하려면 캠페인을 연 다음 **[!UICONTROL 복제]**&#x200B;를 클릭합니다.

![](assets/create-campaign-duplicate.png)

## 캠페인 보관 {#archive}

시간이 지남에 따라 캠페인 목록이 계속 증가하고 결국 완료 및 중지된 캠페인을 탐색하는 것이 더 어려워집니다.

이를 방지하기 위해 더 이상 필요하지 않은 완료 및 중지된 캠페인을 보관할 수 있습니다. 이렇게 하려면 줄임표 버튼을 클릭한 다음 **[!UICONTROL 보관]**&#x200B;을(를) 선택합니다.

![](assets/create-campaign-archive.png)

보관된 캠페인은 목록의 전용 필터를 사용하여 검색할 수 있습니다. [캠페인에 액세스하는 방법 알아보기](get-started-with-campaigns.md#access)
