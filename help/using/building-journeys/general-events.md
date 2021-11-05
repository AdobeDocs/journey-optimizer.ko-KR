---
solution: Journey Orchestration
title: 일반 이벤트
description: 일반 이벤트 사용 방법 알아보기
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: b1813122-7031-452e-9ac5-a4ea7c6dc57c
source-git-commit: 3c21d797c85c2dabbec77f109b160fbd77170da5
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 1%

---

# 일반 이벤트 {#section_ofg_jss_dgb}

이러한 유형의 이벤트에 대해서는 레이블과 설명만 추가할 수 있습니다. 나머지 구성은 편집할 수 없습니다. 기술 사용자가 수행했습니다. [이 페이지](../event/about-events.md)를 참조하십시오.

![](../assets/general-events.png)

비즈니스 이벤트를 삭제하면 자동으로 **세그먼트 읽기** 활동. 비즈니스 이벤트에 대한 자세한 내용은 [이 섹션](../event/about-events.md)

## 특정 시간 동안 이벤트 수신 {#events-specific-time}

여정에 배치된 이벤트 활동은 무한정 이벤트를 수신합니다. 특정 시간 동안에만 이벤트를 수신하려면 이벤트에 대한 시간 제한을 구성해야 합니다.

그러면 여정이 시간 초과에 지정된 시간 동안 이벤트를 수신합니다. 해당 기간 동안 이벤트가 수신되면 이벤트 경로에서 개인이 이동합니다. 그렇지 않은 경우 고객은 시간 초과 경로로 이동하거나 여정을 종료합니다.

이벤트에 대한 시간 제한을 구성하려면 다음 단계를 수행합니다.

1. 를 활성화합니다 **[!UICONTROL Define the event timeout]** 이벤트 속성의 옵션.

1. 여정이 이벤트를 기다리는 시간을 지정합니다.

1. 지정된 시간 제한 내에 이벤트를 받지 못할 때 개인을 시간 제한 경로로 보내려면 **[!UICONTROL Set a timeout path]** 선택 사항입니다. 이 옵션이 활성화되지 않으면 시간 초과에 도달하면 여정이 개별 항목에 대해 종료됩니다.

   ![](../assets/event-timeout.png)

이 예에서 여정은 고객에게 첫 번째 환영 푸시를 보냅니다. 그런 다음 고객이 다음 날 내에 레스토랑에 입장하는 경우에만 식사 할인 푸시를 보냅니다. 따라서 1일 시간 초과로 레스토랑 이벤트를 구성했습니다.

* 시작 푸시 후 1일 이내에 레스토랑 이벤트가 수신되면 식사 할인 푸시 활동이 전송됩니다.
* 다음 날 내에 받은 레스토랑 이벤트가 없으면 이 사람은 시간 초과 경로를 통해 이동합니다.

다음 시간 후에 위치한 여러 이벤트에 대한 시간 제한을 구성하려면 **[!UICONTROL Wait]** 활동, 이러한 이벤트 중 하나에 대해서만 시간 제한을 구성해야 합니다.

시간 제한은 다음에 위치한 모든 이벤트에 적용됩니다 **[!UICONTROL Wait]** 활동. 지정된 시간 초과 전에 이벤트가 수신되지 않으면 개인은 하나의 시간 제한 경로로 이동되거나 여정을 종료합니다.

![](../assets/event-timeout-group.png)
