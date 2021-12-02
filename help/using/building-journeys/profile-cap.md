---
title: 프로필 상한
description: 프로필 상한
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 496c7666-a133-4aeb-be8e-c37b3b9bf5f9
hide: true
hidefromtoc: true
source-git-commit: b5ce2ea81d4091b4fa9c09e83573f9043c5e55a8
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 2%

---


# 발신자로서의 평판 확인

최근 다른 이메일 서비스 공급자, IP 주소 또는 이메일 도메인 또는 하위 도메인으로 이동한 경우, 발신자로서의 평판을 설정해야 합니다. 게재가 차단되거나 수신자 사서함의 스팸 폴더로 이동될 수 있습니다.

IP를 가열하기 위해 게재 수를 점진적으로 늘릴 수 있습니다. 다음 보기 [사용 사례](../building-journeys/ramp-up-deliveries-uc.md).

## 프로필 상한 조건 유형 {#profile_cap}

다른 조건 유형은 여기에 자세히 설명되어 있습니다 [섹션](../building-journeys/condition-activity.md).

이 조건 유형을 사용하여 여정 경로에 대한 최대 프로필 수를 설정합니다. 이 한도에 도달하면 입력한 프로필에서 대체 경로를 사용합니다.

이 조건 유형을 사용하여 게재 볼륨을 높일 수 있습니다. 다음 보기 [사용 사례](../building-journeys/ramp-up-deliveries-uc.md).

기본 캡은 1000입니다. 정수 값을 1에서 20,000으로 설정할 수 있습니다.

카운터는 선택한 여정 버전에만 적용됩니다. 카운터는 한 달 후에 0으로 재설정됩니다. 재설정 후 입력한 프로필은 카운터 제한에 도달할 때까지 명목상 경로를 다시 사용합니다.

대체 경로를 여정 캔버스에서 명목상 패스 위로 이동하더라도 명목상 경로는 항상 대체 경로보다 우선합니다.

![](../assets/profile-cap-condition.png)

## 사용 사례: 게재 강화

최근 다른 이메일 서비스 공급자, IP 주소 또는 이메일 도메인 또는 하위 도메인으로 이동한 경우, 발신자로서의 평판을 설정해야 합니다. 게재가 차단되거나 수신자 사서함의 스팸 폴더로 이동될 수 있습니다. IP 온난화를 통해 이메일 평판을 높이는 방법을 알아보십시오 [게재 가능성 모범 사례 안내서](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html){target=&quot;_blank&quot;}.

IP를 가열하기 위해 게재 수를 점진적으로 늘릴 수 있습니다. 자세한 내용 [Journey Optimizer에서 게재 기능 최적화](../deliverability.md).

이 사용 사례의 목적은 전자 메일 게재를 늘리기 위한 여정을 만드는 것입니다. 이 여정을 구성하려면 다음 단계를 수행합니다.

1. 여정 만들기. [자세히 보기](../building-journeys/journey-gs.md).

1. 추가 **[!UICONTROL Condition]** 활동을 여정에 추가합니다. [자세히 보기](../building-journeys/condition-activity.md).

1. 에서 **[!UICONTROL Condition]** 활동 설정에서 게재에 대한 최대 수신자 수를 설정합니다.

   1. 에서 **[!UICONTROL Condition]** 활동 설정, 설정 **[!UICONTROL Type]** 필드 대상 **[!UICONTROL Profile cap]**. [자세히 보기](profile-cap.md#profile_cap).

   1. 설정 **[!UICONTROL Limit]** 필드를 이 게재의 최대 수신자 수에 추가합니다.

   ![](../assets/profile-cap-condition.png)

   이 제한을 총 구독자 수까지 점진적으로 늘릴 수 있습니다.

1. 추가 **[!UICONTROL Message]** 활동 이후의 명목상 경로 **[!UICONTROL Condition]** 활동.

   ![](../assets/ramp-up-deliveries-message.png)

   여정이 실행되면 입력한 프로필(지정한 최대 프로필 수)까지 메시지가 전송됩니다. 이 한도에 도달하면 입력한 프로필에서 대체 경로를 사용합니다.

1. 선택한 활동으로 여정을 완료합니다.

IP가 따뜻해지면 이 조건을 제거할 수 있습니다.

