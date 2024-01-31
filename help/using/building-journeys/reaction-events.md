---
solution: Journey Optimizer
product: journey optimizer
title: 반응 이벤트
description: 반응 이벤트에 대해 알아보기
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: 여정, 이벤트, 반응, 추적, 플랫폼
exl-id: 235384f3-0dce-4797-8f42-1d4d01fa42d9
source-git-commit: 110fd5f1055455ec040ab8de0b599a343e8de298
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 20%

---

# 반응 이벤트 {#reaction-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_reaction"
>title="반응 이벤트"
>abstract="이 활동을 통해 동일한 여정 내에서 전송된 메시지와 관련된 추적 데이터에 반응할 수 있습니다. Adobe Experience Platform과 공유되는 순간 이 정보를 실시간으로 캡처합니다."

팔레트에서 사용할 수 있는 여러 이벤트 활동 중에서 기본 제공 활동은 다음과 같습니다 **[!UICONTROL 반응]** 이벤트. 이 활동을 통해 동일한 여정 내에서 전송된 메시지와 관련된 추적 데이터에 반응할 수 있습니다. Adobe Experience Platform과 공유되는 순간 이 정보를 실시간으로 캡처합니다.

클릭하거나 연 메시지에 반응할 수 있습니다.

메시지에 대한 반응이 없을 때 이 메커니즘을 사용하여 작업을 수행할 수도 있습니다. 이렇게 하려면 반응 활동과 평행한 두 번째 경로를 만들고 대기 활동을 추가합니다. 대기 활동에 정의된 기간 동안 반응이 없으면 두 번째 경로가 선택됩니다. 예를 들어 후속 메시지를 보내도록 선택할 수 있습니다.

이전에 채널 작업 활동(이메일 및 푸시)이 있는 경우에만 캔버스에서 반응 활동을 사용할 수 있습니다.

다음을 참조하십시오 [작업 활동 기본 정보](../building-journeys/about-journey-activities.md#action-activities).

![](assets/journey45.png)

반응 이벤트를 구성하는 여러 단계는 다음과 같습니다.

1. 추가 **[!UICONTROL 레이블]** 반응으로. 데이터 소스에 이벤트에 설명을 추가합니다.
1. 드롭다운 목록에서 반응할 작업 활동을 선택합니다. 경로의 이전 단계에 배치된 모든 작업 활동을 선택할 수 있습니다.
1. 선택한 작업에 따라 반응할 항목을 선택합니다.
1. 이벤트 시간 제한(40초~29일)과 시간 제한 경로를 정의할 수 있습니다. 이렇게 하면 정의된 기간 내에 반응하지 않은 개인에 대한 두 번째 경로가 만들어집니다. 반응 이벤트를 사용하는 여정을 테스트할 때에는 테스트 모드 **[!UICONTROL 대기 시간]** 기본값과 최소값은 40초입니다. [이 섹션](../building-journeys/testing-the-journey.md)을 참조하십시오.

>[!NOTE]
>
>
>반응 이벤트는 다른 여정에서 발생하는 메시지를 추적할 수 없습니다.
>
>반응 이벤트는 &quot;추적됨&quot; 유형의 링크에 대한 클릭을 추적합니다. 구독 취소 및 미러 페이지 링크는 고려되지 않습니다.

>[!IMPORTANT]
>
>Gmail과 같은 이메일 클라이언트는 이미지 차단을 허용합니다. 이메일에 포함된 0픽셀 이미지를 사용하여 이메일 열람을 추적합니다. 이미지가 차단되면 이메일 열림은 고려되지 않습니다.
