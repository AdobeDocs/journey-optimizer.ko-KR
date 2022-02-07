---
title: 세그먼트 작성
description: 세그먼트 작성 방법 알아보기
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 289aac5d-6cdb-411f-985e-3acef58050a8
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 5%

---

# 세그먼트 작성 {#build-segments}

이 예에서는 1980년 이후에 태어난 Atlanta, San Francisco 또는 Seattle에 거주하는 모든 고객을 타겟팅하는 세그먼트를 만듭니다. 이 모든 고객은 지난 7일 이내에 Luma 애플리케이션을 연 다음 애플리케이션을 연 후 2시간 내에 구매했어야 합니다.

1. 액세스 권한 **[!UICONTROL Segments]** 메뉴를 클릭한 다음 **[!UICONTROL Create segment]** 버튼을 클릭합니다.

   ![](../assets/create-segment.png)

   세그먼트 정의 화면에서는 세그먼트를 정의하기 위해 모든 필수 필드를 구성할 수 있습니다. 에서 세그먼트를 구성하는 방법 알아보기 [Segmentation Service 설명서](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html){target=&quot;_blank&quot;}.

   ![](../assets/segment-builder.png)

1. 에서 **[!UICONTROL Segment properties]** 창에서 세그먼트의 이름과 설명(선택 사항)을 제공합니다.

   ![](../assets/segment-properties.png)

1. 왼쪽 창의 원하는 필드를 가운데 작업 영역으로 끌어다 놓은 뒤 필요에 따라 구성합니다.

   >[!NOTE]
   >
   >왼쪽 창에서 사용할 수 있는 필드는 **XDM 개별 프로필** 및 **XDM ExperienceEvent** 조직에 대해 스키마가 구성되었습니다.  자세한 내용은 [XDM(Experience Data Model) 설명서](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko){target=&quot;_blank&quot;}.

   ![](../assets/drag-fields.png)

   이 예제에서는 **속성** 및 **이벤트** 세그먼트를 작성할 필드:

   * **속성**: 애틀랜타, 샌프란시스코 또는 시애틀에서 1980년 이후에 태어난 프로필

      ![](../assets/add-attributes.png)

   * **이벤트**: 지난 7일 이내에 Luma 애플리케이션을 연 다음, 애플리케이션을 연 후 2시간 이내에 구입한 프로필입니다.

      ![](../assets/add-events.png)

1. 작업 공간에서 새 필드를 추가 및 구성하는 동안 **[!UICONTROL Segment Properties]** 창은 세그먼트에 속하는 예상 프로필에 대한 정보로 자동 업데이트됩니다.

   ![](../assets/segment-estimate.png)

1. 세그먼트를 준비했으면 을 클릭합니다 **[!UICONTROL Save]**. Adobe Experience Platform 세그먼트 목록에 표시됩니다. 검색 창에서는 목록에서 특정 세그먼트를 검색하는 데 도움이 됩니다.

이제 여정에서 세그먼트를 사용할 수 있습니다. 이 작업에 대한 자세한 정보는 [이 섹션](../segment/about-segments.md)을 참조하십시오.

## 튜토리얼 비디오{#create-segment-video}

>[!VIDEO](https://video.tv.adobe.com/v/334281?quality=12)
