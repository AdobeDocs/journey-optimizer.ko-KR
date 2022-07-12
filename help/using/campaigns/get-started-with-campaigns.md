---
title: 캠페인 시작
description: 에서 캠페인에 대해 자세히 알아보십시오 [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 6177a33edeb3b8381c3eb5609762b4d974dc93e3
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 8%

---


# 캠페인 시작 {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="캠페인"
>abstract="Campaign을 사용하면 여러 채널에서 특정 세그먼트에 일회성 콘텐츠를 제공할 수 있습니다. 새 캠페인을 만들기 전에 메시지 사전 설정과 Adobe Experience Platform 세그먼트를 사용할 수 있는지 확인하십시오."

## 캠페인 기본 정보 {#about}

캠페인을 사용하면 여러 채널을 사용하여 특정 세그먼트에 일회성 콘텐츠를 제공할 수 있습니다. 작업이 순서대로 실행되도록 디자인된 여정과 달리, 캠페인은 즉시 또는 지정된 일정에 따라 작업을 동시에 실행합니다.

두 가지 유형의 캠페인을 만들 수 있습니다.

* **예약된 캠페인** 홍보 오퍼, 참여 캠페인, 공지, 법적 고지 사항 또는 정책 업데이트와 같은 마케팅 사용 사례에 대해 간단한 임시 배치 커뮤니케이션을 허용합니다.
* **API 트리거 캠페인** 페이로드의 프로필 속성 및 컨텍스트 데이터를 사용하여 개인화를 수행해야 하는 경우 REST API(암호 재설정, 카드 중단 등)를 사용하여 간단한 트랜잭션/운영 메시지를 사용할 수 있습니다.

캠페인 사용 방법 알아보기:
* [캠페인 만들기](create-campaign.md)
* [API로 트리거된 캠페인 만들기](api-triggered-campaigns.md)
* [캠페인 수정 또는 중지](modify-stop-campaign.md)
* [캠페인 라이브 보고서](campaign-live-report.md)
* [캠페인 글로벌 보고서](campaign-global-report.md)

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
* **[!UICONTROL Completed]**: 캠페인이 완료되었습니다.
* **[!UICONTROL Archived]**: 캠페인이 보관되었습니다.

>[!NOTE]
>
>다음 옆에 있는 &quot;초안 버전 열기&quot; 아이콘 **[!UICONTROL Live]** 또는 **[!UICONTROL Scheduled]** 상태는 캠페인의 새 버전이 만들어지고 아직 활성화되지 않았음을 나타냅니다( 참조) [캠페인 수정](modify-stop-campaign.md#modify)).
