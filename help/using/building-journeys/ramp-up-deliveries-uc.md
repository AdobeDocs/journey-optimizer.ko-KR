---
title: 게재 램프 업
description: 게재 속도를 높이는 방법을 알아봅니다
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 83d1b68d-011a-4109-b5f0-6ca1ade2944d
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 3%

---

# 사용 사례: 게재 강화{#use-case-ramp-up-your-deliveries}

최근 다른 이메일 서비스 공급자, IP 주소 또는 이메일 도메인 또는 하위 도메인으로 이동한 경우, 발신자로서의 평판을 설정해야 합니다. 게재가 차단되거나 수신자 사서함의 스팸 폴더로 이동될 수 있습니다. IP 온난화를 통해 이메일 평판을 높이는 방법을 알아보십시오 [게재 가능성 모범 사례 안내서](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html){target=&quot;_blank&quot;}.

IP를 가열하기 위해 게재 수를 점진적으로 늘릴 수 있습니다. 자세한 내용 [Journey Optimizer에서 게재 기능 최적화](../messages/deliverability.md).

이 사용 사례의 목적은 전자 메일 게재를 늘리기 위한 여정을 만드는 것입니다. 이 여정을 구성하려면 다음 단계를 수행합니다.

1. 여정 만들기. [자세히 보기](journey-gs.md).

1. 추가 **[!UICONTROL Condition]** 활동을 여정에 추가합니다. [자세히 보기](condition-activity.md).

1. 에서 **[!UICONTROL Condition]** 활동 설정에서 게재에 대한 최대 수신자 수를 설정합니다.

   1. 에서 **[!UICONTROL Condition]** 활동 설정, 설정 **[!UICONTROL Type]** 필드 대상 **[!UICONTROL Profile cap]**. [자세히 보기](condition-activity.md#profile_cap).

   1. 설정 **[!UICONTROL Limit]** 필드를 이 게재의 최대 수신자 수에 추가합니다.

   ![](assets/profile-cap-condition.png)

   이 제한을 총 구독자 수까지 점진적으로 늘릴 수 있습니다.

1. 추가 **[!UICONTROL Message]** 활동 이후의 명목상 경로 **[!UICONTROL Condition]** 활동.

   ![](assets/ramp-up-deliveries-message.png)

   여정이 실행되면 입력한 프로필(지정한 최대 프로필 수)까지 메시지가 전송됩니다. 이 한도에 도달하면 입력한 프로필에서 대체 경로를 사용합니다.

1. 선택한 활동으로 여정을 완료합니다.

IP가 따뜻해지면 이 조건을 제거할 수 있습니다.
