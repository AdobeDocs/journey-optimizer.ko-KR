---
title: 세그먼트 만들기
description: 세그먼트를 작성하는 방법 학습
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 5%

---

# 세그먼트 작성 {#build-segments}

![](../assets/do-not-localize/badge.png)

이 예에서는 애틀랜타, 샌프란시스코 또는 시애틀에 거주하는 모든 고객을 대상으로 1980년 이후에 태어난 세그먼트를 만듭니다. 이러한 모든 고객은 지난 7일 이내에 Luma 애플리케이션을 열고 애플리케이션을 연 후 2시간 이내에 구매해야 합니다.

1. **[!UICONTROL Segments]** 메뉴에 액세스한 다음 **[!UICONTROL Create segment]** 단추를 클릭합니다.

   ![](../assets/create-segment.png)

   세그먼트 정의 화면에서는 세그먼트를 정의하는 데 필요한 모든 필드를 구성할 수 있습니다. [세그멘테이션 서비스 설명서](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html)에서 세그먼트를 구성하는 방법을 알아봅니다.

   ![](../assets/segment-builder.png)

1. **[!UICONTROL Segment properties]** 창에서 세그먼트에 대한 이름 및 설명(선택 사항)을 입력합니다.

   ![](../assets/segment-properties.png)

1. 왼쪽 창에서 원하는 필드를 가운데 작업 영역으로 드래그하여 놓은 다음 필요에 따라 구성합니다.

   >[!NOTE]
   >
   >왼쪽 창에서 사용할 수 있는 필드는 **XDM 개인 프로필** 및 **XDM ExperienceEvent** 스키마가 조직에 맞게 구성된 방식에 따라 달라집니다.  [XDM(Experience Data Model) 설명서](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko)에서 자세한 내용을 알아보십시오.

   ![](../assets/drag-fields.png)

   이 예에서는 **특성** 및 **이벤트** 필드를 사용하여 세그먼트를 만들어야 합니다.

   * **속성**:애틀랜타, 샌프란시스코 또는 시애틀에서 1980년 이후에 태어난 프로필
   * **이벤트**:지난 7일 이내에 루마 애플리케이션을 열고 애플리케이션을 연 후 2시간 이내에 구매한 프로파일

      ![](../assets/add-attributes.png)

      ![](../assets/add-events.png)

1. 작업 공간에서 새 필드를 추가 및 구성하면 세그먼트에 속하는 예상 프로파일에 대한 정보가 자동으로 **[!UICONTROL Segment Properties]** 창에 업데이트됩니다.

   ![](../assets/segment-estimate.png)

1. 세그먼트가 준비되면 **[!UICONTROL Save]**&#x200B;을 클릭합니다. Adobe Experience Platform 세그먼트 목록에 표시됩니다. 검색 막대는 목록에서 특정 세그먼트를 검색하는 데 도움이 됩니다.

이제 세그먼트를 여정에서 사용할 수 있습니다. 이 작업에 대한 자세한 정보는 [이 섹션](../segment/about-segments.md)을 참조하십시오.
