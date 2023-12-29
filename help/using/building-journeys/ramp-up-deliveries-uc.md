---
solution: Journey Optimizer
product: journey optimizer
title: 게재 램프 업
description: 게재를 가속화하는 방법에 대해 알아봅니다
feature: Journeys, Use Cases, IP Warmup Plans
topic: Content Management
role: User, Data Engineer
level: Intermediate, Experienced
keywords: 전달성, 여정, 사용 사례, 이메일, 신뢰도
exl-id: 83d1b68d-011a-4109-b5f0-6ca1ade2944d
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 2%

---

# 사용 사례: 게재 램프 업{#use-case-ramp-up-your-deliveries}

최근 다른 이메일 서비스 공급자, IP 주소, 이메일 도메인 또는 하위 도메인으로 이동한 경우 발신자로서의 신뢰도를 설정해야 합니다. 그렇지 않으면 게재가 차단되거나 수신자 사서함의 스팸 폴더로 이동될 수 있습니다. 에서 IP warming을 사용하여 이메일 평판을 높이는 방법을 알아봅니다. [전달성 모범 사례 안내서](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=ko){target="_blank"}.

IP를 준비하려면 게재 수를 점차적으로 늘릴 수 있습니다. 자세한 내용 [Journey Optimizer의 전달성 최적화](../reports/deliverability.md).

이 사용 사례의 목적은 이메일 게재를 가속화하는 여정을 만드는 것입니다. 이 여정을 구성하려면 다음 단계를 수행합니다.

1. 여정 만들기 [자세히 보기](journey-gs.md).

1. 추가 **[!UICONTROL 조건]** 활동을 여정에 추가합니다. [자세히 보기](condition-activity.md).

1. 다음에서 **[!UICONTROL 조건]** 활동 설정에서 게재할 최대 수신자 수를 설정합니다.

   1. 다음에서 **[!UICONTROL 조건]** 활동 설정, 설정 **[!UICONTROL 유형]** 필드 대상 **[!UICONTROL 프로필 상한]**. [자세히 보기](condition-activity.md#profile_cap).

   1. 설정 **[!UICONTROL 제한]** 필드를 게재할 최대 수신자 수에 추가합니다.

   ![](assets/profile-cap-condition.png)

   이 제한을 총 구독자 수까지 점진적으로 늘릴 수 있습니다.

1. 추가 **[!UICONTROL 이메일]** 작업 활동을 명목 경로에 추가합니다. **[!UICONTROL 조건]** 활동.

   ![](assets/ramp-up-deliveries-message.png)

   여정이 실행되면 지정한 최대 프로필 수까지 입력한 프로필로 메시지가 전송됩니다. 이 한도에 도달하면 입력한 프로필에서 대체 경로를 사용합니다.

1. 선택한 활동으로 여정을 완료합니다.

IP가 예열되면 이 조건을 제거할 수 있습니다.
