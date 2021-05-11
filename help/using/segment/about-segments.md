---
title: Adobe Experience Platform 세그먼트 정보
description: Adobe Experience Platform 세그먼트를 구성하는 방법 알아보기
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---

# Adobe Experience Platform 세그먼트 정보 {#about-segments}

![](../assets/do-not-localize/badge.png)

Journey Optimizer을 사용하면 **[!UICONTROL Segments]** 메뉴에서 바로 실시간 고객 프로필 데이터를 사용하여 Adobe Experience Platform 세그먼트를 만들고 여정에 활용할 수 있습니다.

세그먼트는 세그멘테이션 서비스 자체에서 만들 수도 있습니다. [Adobe Experience Platform 세그멘테이션 서비스 설명서](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html)에서 자세한 내용을 살펴보십시오.

여정의 세그먼트를 다양한 방법으로 활용할 수 있습니다.

* **세그먼트 읽기** 오케스트레이션 활동을 사용하여 지정된 세그먼트에 속하는 모든 사용자가 여정을 입력하도록 하십시오. 여정에 포함된 메시지는 세그먼트에 속하는 개인에게 전송됩니다. &quot;실버(silver) 고객&quot; 세그먼트가 있는 경우 이 활동을 통해 모든 실버(Silver) 고객이 여정을 입력하고 일련의 개인화된 메시지를 보낼 수 있습니다.

   **[!UICONTROL Read segment]** 활동 사용 방법에 대한 자세한 내용은 [이 섹션](../building-journeys/read-segment.md#configuring-segment-trigger-activity)을 참조하십시오.

* **세그먼트 자격 조건** 이벤트 활동을 사용하여 개인이 Adobe Experience Platform 세그먼트 입장 및 종료를 기준으로 여정에 들어가거나 앞으로 이동할 수 있도록 합니다. 예를 들어 모든 새 실버 고객이 여정을 입력하고 메시지를 보내도록 할 수 있습니다. 이 활동을 사용하는 방법에 대한 자세한 내용은 [이 섹션](../building-journeys/segment-qualification-events.md)을 참조하십시오.

* 단순 또는 고급 표현식 편집기를 사용하여 여정에 **복잡한 조건**&#x200B;을 만듭니다. [이 섹션](../building-journeys/condition-activity.md#using-a-segment)에서 자세히 알아보십시오.
