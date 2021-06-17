---
title: Adobe Experience Platform 세그먼트 기본 정보
description: Adobe Experience Platform 세그먼트를 구성하는 방법 알아보기
feature: 여정
topic: 콘텐츠 관리
role: User
level: Intermediate
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 1%

---

# Adobe Experience Platform 세그먼트 정보 {#about-segments}

[!DNL Journey Optimizer]  메뉴에서 직접 실시간 고객 프로필 데이터를 사용하여 Adobe Experience Platform 세그먼트를 만들고  **[!UICONTROL Segments]** 여정에 활용할 수 있습니다.

세그먼테이션 서비스 자체에서도 만들 수 있습니다. 자세한 내용은 [Adobe Experience Platform 세그멘테이션 서비스 설명서](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html)에서 알아보십시오.

여정의 세그먼트를 다양한 방법으로 활용할 수 있습니다.

* **세그먼트 읽기** 오케스트레이션 활동을 사용하여 지정된 세그먼트에 속하는 모든 개인이 여정을 입력하도록 하십시오. 여정에 포함된 메시지는 세그먼트에 속하는 개인에게 전송됩니다. &quot;실버 고객&quot; 세그먼트가 있다고 가정해 보겠습니다. 이 활동을 사용하면 모든 실버 고객이 여정을 입력하고 일련의 개인화된 메시지를 전송하도록 할 수 있습니다.

   **[!UICONTROL Read segment]** 활동을 사용하는 방법에 대한 자세한 내용은 [이 섹션](../building-journeys/read-segment.md#configuring-segment-trigger-activity)을 참조하십시오.

* **세그먼트 자격** 이벤트 활동을 사용하여 개인이 Adobe Experience Platform 세그먼트 출입구 및 종료에 따라 여정에 들어오거나 앞으로 이동하도록 하십시오. 예를 들어 모든 신규 실버 고객이 여정을 입력하고 메시지를 보내게 할 수 있습니다. 이 활동을 사용하는 방법에 대한 자세한 내용은 [이 섹션](../building-journeys/segment-qualification-events.md)을 참조하십시오.

* 단순 또는 고급 표현식 편집기를 사용하여 여정에서 **복잡한 조건**&#x200B;을 작성합니다. 자세한 내용은 [이 섹션](../building-journeys/condition-activity.md#using-a-segment)을 참조하십시오.
