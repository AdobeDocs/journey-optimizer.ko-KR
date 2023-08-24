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
source-git-commit: 6386a5ee5a0d1f221beab67f43636c599531736a
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 4%

---

# 경고 시작 {#alerts}

Journey Optimizer은 Adobe Experience Platform 경고 기능을 활용합니다. 이렇게 하면 사용자 인터페이스를 통해 시스템 경고에 액세스할 수 있습니다. 사용 가능한 경고를 보고 구독할 수 있습니다.

작업의 특정 조건 세트에 도달하면(예: 시스템이 임계값을 위반한 경우 발생할 수 있는 문제) 경고 메시지가 이를 구독한 조직의 모든 사용자에게 전달됩니다.

<!--These messages can repeat over a pre-defined time interval until the alert has been resolved.-->

Adobe Experience Platform의 경고에 대해 자세히 알아보기 [설명서](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=ko).

경고를 구독하고 구성하는 방법은 다음을 참조하십시오. [페이지](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html).

>[!AVAILABILITY]
>
>&#39;대상 트리거 읽기 실패&#39; 경고에 대한 일부 디자인 변경이 진행 중이므로 이 경고는 현재 일시 중지되며 사용자 인터페이스에서 일시적으로 제거되었습니다. 이러한 변경 사항이 릴리스되면 경고가 다시 표시되며 알림을 구독할 수 있습니다.

왼쪽 메뉴에서 **관리**, 클릭 **경고**. Journey Optimizer에 대해 사전 구성된 경고를 사용할 수 있습니다. 이 경고는 사용자 지정 작업이 실패할 경우 경고합니다. 지난 5분 동안 특정 사용자 지정 작업에 대해 1% 이상의 오류가 발생한 오류가 있는 것으로 간주됩니다. 이는 30초마다 평가됩니다.

![](assets/alerts-custom-action.png)


<!--A pre-configured alert for Journey Optimizer is available. This alert will warn you if a read segment node has not processed any profile during the defined time frame.

![](assets/alerts1.png)-->

예기치 않은 동작이 발생하면 사용자 환경 설정에 따라 경고 알림이 이메일을 통해 또는 인터페이스의 오른쪽 상단 모서리에 있는 Journey Optimizer에서 직접 경고 구독자에게 전송됩니다.

경고가 해결되면 &quot;해결됨&quot; 알림을 받습니다. 사용자 지정 작업 경고의 경우 다음 두 가지 이유로 인해 발생할 수 있습니다.
* 지난 5분 동안 해당 사용자 지정 작업에 대한 오류(또는 1% 임계값 아래의 오류)가 없었습니다.
* 해당 사용자 지정 작업에 도달한 프로필이 없습니다.

날짜 [Adobe Experience Platform UI에서 경고 규칙 보기](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html), 각 규칙에 개별적으로 가입할 수 있습니다. 을 통해 경고를 구독할 때 [I/O 이벤트 알림](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html)하지만 경고 규칙은 다른 구독 패키지로 구성됩니다. 사용자 지정 작업 경고에 해당하는 I/O 이벤트 구독 이름은 &quot;사용자 지정 작업 실패 여정&quot;입니다.

<!--The I/O event subscription name corresponding to the Read segment alert is: "Journey read segment Delays, Failures and Errors".-->

>[!WARNING]
>
>이러한 경고는 라이브 여정에 대해서만 적용됩니다. 테스트 모드의 여정에 대해서는 경고가 트리거되지 않습니다.

