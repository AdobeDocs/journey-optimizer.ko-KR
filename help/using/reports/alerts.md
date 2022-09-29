---
title: 경고
description: 경고 관리 방법 알아보기
feature: Alerts
topic: Administration
role: Admin
level: Intermediate
source-git-commit: 3d0d1b7d092ffae48ded337d5a1b14a5f5c4653b
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 2%

---

# 경고 시작 {#alerts}

Journey Optimizer은 Adobe Experience Platform 경고 기능을 활용합니다. 사용자 인터페이스를 통해 시스템 경고에 액세스할 수 있습니다. 사용 가능한 경고를 보고 구독할 수 있습니다. 작업의 특정 조건 세트에 도달하면(예: 시스템이 임계값을 위반한 경우 발생할 수 있는 문제) 해당 조건을 구독한 조직의 사용자에게 경고 메시지가 전달됩니다. 이러한 메시지는 경고가 해결될 때까지 미리 정의된 시간 간격에 따라 반복될 수 있습니다.

Adobe Experience Platform의 경고에 대해 자세히 알아보기 [설명서](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=ko).
경고를 구독하고 구성하는 방법에 대해 알아보려면 다음 문서를 참조하십시오 [페이지](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html).

왼쪽 메뉴에서 **관리**&#x200B;를 클릭합니다. **경고**. Journey Optimizer에 대해 사전 구성된 경고를 사용할 수 있습니다. 이 경고는 읽기 세그먼트 노드가 정의된 기간 동안 프로필을 처리하지 않은 경우 표시됩니다.

![](assets/alerts1.png)

이러한 예기치 않은 동작이 발생하면 인터페이스 오른쪽 상단 모서리에 있는 이메일 및 인앱 알림을 통해 경고 가입자에게 경고 알림이 전송됩니다.

![](assets/alerts2.png)

When [플랫폼 UI에서 경고 규칙 보기](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html)각 규칙에 개별적으로 가입할 수 있습니다. 경고 구독 시 [I/O 이벤트 알림](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html)그러나 경고 규칙은 다른 구독 패키지로 구성되어 있습니다. 세그먼트 읽기 경고에 해당하는 I/O 이벤트 구독 이름은 다음과 같습니다. &quot;여정 읽기 세그먼트 읽기 지연, 오류 및 오류&quot;

>[!WARNING]
>
>이러한 경고는 라이브 여정에만 적용됩니다. 테스트 모드의 여정에 대해 경고가 트리거되지 않습니다.