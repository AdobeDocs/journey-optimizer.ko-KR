---
title: 세그먼트 작성
description: 세그먼트 작성 방법 알아보기
feature: 여정
topic: 콘텐츠 관리
role: User
level: Intermediate
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 6%

---

# 세그먼트 빌드 {#build-segments}

이 예에서는 1980년 이후에 태어난 Atlanta, San Francisco 또는 Seattle에 거주하는 모든 고객을 타겟팅하는 세그먼트를 만듭니다. 이 모든 고객은 지난 7일 이내에 Luma 애플리케이션을 연 다음 애플리케이션을 연 후 2시간 내에 구매했어야 합니다.

1. **[!UICONTROL Segments]** 메뉴에 액세스한 다음 **[!UICONTROL Create segment]** 단추를 클릭합니다.

   ![](../assets/create-segment.png)

   세그먼트 정의 화면에서는 세그먼트를 정의하기 위해 모든 필수 필드를 구성할 수 있습니다. [세분화 서비스 설명서](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html)에서 세그먼트를 구성하는 방법을 알아봅니다.

   ![](../assets/segment-builder.png)

1. **[!UICONTROL Segment properties]** 창에서 세그먼트의 이름과 설명(선택 사항)을 제공합니다.

   ![](../assets/segment-properties.png)

1. 왼쪽 창의 원하는 필드를 가운데 작업 영역으로 끌어다 놓은 뒤 필요에 따라 구성합니다.

   >[!NOTE]
   >
   >왼쪽 창에서 사용할 수 있는 필드는 **XDM 개별 프로필** 및 **XDM ExperienceEvent** 스키마가 조직에 구성되어 있는 방식에 따라 달라집니다.  자세한 내용은 [XDM(Experience Data Model) 설명서](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko)에서 알아보십시오.

   ![](../assets/drag-fields.png)

   이 예제에서는 **Attributes** 및 **Events** 필드를 사용하여 세그먼트를 만들어야 합니다.

   * **속성**:애틀랜타, 샌프란시스코 또는 시애틀에서 1980년 이후에 태어난 프로필
   * **이벤트**:지난 7일 이내에 Luma 애플리케이션을 연 다음, 애플리케이션을 연 후 2시간 이내에 구입한 프로필입니다.

      ![](../assets/add-attributes.png)

      ![](../assets/add-events.png)

1. 작업 공간에서 새 필드를 추가 및 구성할 때 세그먼트에 속하는 예상 프로필에 대한 정보로 **[!UICONTROL Segment Properties]** 창이 자동으로 업데이트됩니다.

   ![](../assets/segment-estimate.png)

1. 세그먼트가 준비되면 **[!UICONTROL Save]** 을 클릭합니다. Adobe Experience Platform 세그먼트 목록에 표시됩니다. 검색 창에서는 목록에서 특정 세그먼트를 검색하는 데 도움이 됩니다.

이제 여정에서 세그먼트를 사용할 수 있습니다. 이 작업에 대한 자세한 정보는 [이 섹션](../segment/about-segments.md)을 참조하십시오.
