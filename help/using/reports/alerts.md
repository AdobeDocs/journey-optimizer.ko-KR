---
solution: Journey Optimizer
product: journey optimizer
title: 경고
description: 경고 관리 방법 알아보기
feature: Alerts
topic: Administration
role: Admin
level: Intermediate
exl-id: 0855ca5b-c7af-41c4-ad51-bed820ae5ecf
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 6%

---

# 경고 시작 {#alerts}

Journey Optimizer은 Adobe Experience Platform 경고 기능을 활용합니다. 이렇게 하면 사용자 인터페이스를 통해 시스템 경고에 액세스할 수 있습니다. 사용 가능한 경고를 보고 구독할 수 있습니다.

작업의 특정 조건 세트에 도달하면(예: 시스템이 임계값을 위반한 경우 발생할 수 있는 문제) 경고 메시지가 이를 구독한 조직의 모든 사용자에게 전달됩니다. 이러한 메시지는 경고가 해결될 때까지 사전 정의된 시간 간격 동안 반복될 수 있습니다.

Adobe Experience Platform의 경고에 대해 자세히 알아보기 [설명서](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=ko).
경고를 구독하고 구성하는 방법은 다음을 참조하십시오. [페이지](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html).

>[!AVAILABILITY]
>
>&#39;대상 트리거 읽기 실패&#39; 경고에 대한 일부 디자인 변경이 진행 중이므로 이 경고는 현재 일시 중지되며 사용자 인터페이스에서 일시적으로 제거되었습니다. 이러한 변경 사항이 릴리스되면 경고가 다시 표시되며 알림을 구독할 수 있습니다.
>

왼쪽 메뉴에서 **관리**, 클릭 **경고**.

<!--A pre-configured alert for Journey Optimizer is available. This alert will warn you if a read segment node has not processed any profile during the defined time frame.

![](assets/alerts1.png)-->

예기치 않은 동작이 발생하면 경고 알림이 인터페이스 오른쪽 상단 모서리에 있는 이메일을 통해 경고 가입자에게 전송됩니다.

<!--![](assets/alerts2.png)-->


날짜 [Adobe Experience Platform UI에서 경고 규칙 보기](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html), 각 규칙에 개별적으로 가입할 수 있습니다. 을 통해 경고를 구독할 때 [I/O 이벤트 알림](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html)하지만 경고 규칙은 다른 구독 패키지로 구성됩니다.

<!--The I/O event subscription name corresponding to the Read segment alert is: "Journey read segment Delays, Failures and Errors".

>[!WARNING]
>
>These alerts apply only to live journeys. Alerts will not be triggered for journeys in test mode.-->
