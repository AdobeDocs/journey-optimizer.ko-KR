---
solution: Journey Optimizer
product: journey optimizer
title: 세그먼트 정의 작성
description: 세그먼트 정의를 통해 대상자를 만드는 방법을 알아봅니다
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 289aac5d-6cdb-411f-985e-3acef58050a8
source-git-commit: f64388673b5a3b2a8702026ce09b39e928ac2ab4
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 13%

---

# 세그먼트 정의 작성 {#build-segments}

>[!CONTEXTUALHELP]
>id="ajo_ao_create_rule"
>title="규칙 만들기"
>abstract="규칙 빌드 만들기 메서드를 통해 Adobe Experience Platform 대상자 세분화 서비스를 사용하여 새 대상자 정의를 만들 수 있습니다."

이 예에서는 Atlanta, San Francisco 또는 Seattle에 거주하며 1980년 이후 출생한 모든 고객을 타깃팅하는 대상을 구성합니다. 이 모든 고객은 지난 7일 이내에 Luma 애플리케이션을 열었다가 애플리케이션을 연 후 2시간 이내에 구입했어야 합니다.

➡️ [이 비디오에서 대상자를 만드는 방법을 알아봅니다.](#video-segment)

1. 다음에서 **[!UICONTROL 대상]** 메뉴에서 **[!UICONTROL 대상자 만들기]** 단추 및 선택 **[!UICONTROL 규칙 작성]**.

   ![](assets/create-segment.png)

   세그먼트 정의 화면에서는 대상자를 정의하는 데 필요한 모든 필드를 구성할 수 있습니다. 에서 대상을 구성하는 방법을 알아봅니다. [세그먼테이션 서비스 설명서](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=ko){target="_blank"}.

   ![](assets/segment-builder.png)

1. 다음에서 **[!UICONTROL 대상 속성]** 창에서 대상자의 이름과 설명을 입력합니다(선택 사항).

   ![](assets/segment-properties.png)

1. 왼쪽 창에서 중앙 작업 영역으로 원하는 필드를 드래그하여 놓은 다음 필요에 따라 구성합니다.

   >[!NOTE]
   >
   >왼쪽 창에서 사용할 수 있는 필드는 을 사용하는 방법에 따라 다릅니다. **XDM 개별 프로필** 및 **XDM ExperienceEvent** 조직에 대해 스키마가 구성되었습니다.  다음에서 자세히 알아보기 [Experience Data Model(XDM) 설명서](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko-KR){target="_blank"}.

   ![](assets/drag-fields.png)

   이 예에서는 를 사용해야 합니다. **속성** 및 **이벤트** 대상을 작성할 필드:

   * **속성**: 애틀랜타, 샌프란시스코 또는 1980년 이후 태어난 시애틀에 거주하는 프로필

     ![](assets/add-attributes.png)

   * **이벤트**: 지난 7일 이내에 Luma 애플리케이션을 연 다음, 애플리케이션을 연 후 2시간 이내에 구입한 프로필.

     ![](assets/add-events.png)

1. 작업 영역에서 새 필드를 추가하고 구성할 때 **[!UICONTROL 대상 속성]** 창은 대상자에 속한 예상 프로필에 대한 정보로 자동으로 업데이트됩니다.

   ![](assets/segment-estimate.png)

1. 대상자가 준비되면 **[!UICONTROL 저장]**. Adobe Experience Platform 대상자 목록에 표시됩니다. 목록의 특정 대상자를 검색하는 데 도움이 되는 검색 창을 사용할 수 있습니다.

이제 여정에서 대상을 사용할 수 있습니다. 이 작업에 대한 자세한 정보는 [이 섹션](../audience/about-audiences.md)을 참조하십시오.

## 방법 비디오{#video-segment}

Journey Optimizer에서 규칙을 사용하여 대상자를 생성하는 방법을 이해하고 속성, 이벤트 및 기존 대상자를 사용하여 대상자를 만드는 방법을 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/3425020?quality=12)
