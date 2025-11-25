---
solution: Journey Optimizer
product: journey optimizer
title: 반응 이벤트
description: 반응 이벤트를 사용하여 여정 내 열기 및 클릭과 같은 메시지 추적 데이터에 응답하고, 응답자가 아닌 사용자를 위한 시간 제한 경로를 구성하는 방법에 대해 알아봅니다.
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: 여정, 이벤트, 반응, 추적, 플랫폼
exl-id: 235384f3-0dce-4797-8f42-1d4d01fa42d9
version: Journey Orchestration
source-git-commit: d8fa1c7055e4e31e393e36ba16863e0f8f95ca9b
workflow-type: tm+mt
source-wordcount: '504'
ht-degree: 16%

---

# 반응 이벤트 {#reaction-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_reaction"
>title="반응 이벤트"
>abstract="이 활동을 통해 동일한 여정 내에서 전송된 메시지와 관련된 추적 데이터에 반응할 수 있습니다. Adobe Experience Platform과 공유되는 순간 이 정보를 실시간으로 캡처합니다."

## 개요 {#overview}

팔레트에서 사용할 수 있는 다양한 이벤트 활동 중에서 기본으로 제공되는 **[!UICONTROL 반응]** 이벤트를 찾을 수 있습니다. 이 활동을 통해 동일한 여정 내에서 전송된 메시지와 관련된 추적 데이터에 반응할 수 있습니다. Adobe Experience Platform과 공유되는 순간 이 정보를 실시간으로 캡처합니다.

클릭하거나 연 메시지에 반응할 수 있습니다. 예를 들어, 개인이 이전 이메일을 열거나 그 내부를 클릭한 경우 다른 메시지를 보내거나, 커뮤니케이션에 참여하지 않은 경우 다른 후속 메시지를 보낼 수 있습니다.

[작업 활동](../building-journeys/about-journey-activities.md#action-activities)을 참조하세요.

메시지에 대한 반응이 없는 경우 **[!UICONTROL 반응]** 활동을 사용하여 작업을 수행할 수 있습니다. 이렇게 하려면 **[!UICONTROL 반응]** 활동과 평행한 두 번째 경로를 만들고 **[!UICONTROL 대기]** 활동을 추가합니다. **[!UICONTROL 대기]** 활동에 정의된 기간 동안 반응이 없으면 두 번째 경로가 선택됩니다. 예를 들어 후속 메시지를 보내도록 선택할 수 있습니다.

## 반응 이벤트를 구성하는 방법 {#configure}

![채널 선택 및 이벤트 유형 옵션을 사용한 반응 이벤트 구성](assets/journey45.png)

다음 단계에 따라 반응 이벤트를 구성합니다.

1. 여정 캔버스에서 **[!UICONTROL 채널 작업 활동]** 후에 **반응** 활동을 [즉시](journeys-message.md)합니다.
1. 반응에 **[!UICONTROL Label]**&#x200B;을(를) 추가합니다. 데이터 소스에 이벤트에 설명을 추가합니다.
1. 드롭다운 목록에서 반응할 작업 활동을 선택합니다. 경로의 이전 단계에 배치된 모든 작업 활동을 선택할 수 있습니다.
1. 선택한 작업에 따라 반응할 항목을 선택합니다.
1. 이벤트 시간 제한(40초~90일)과 시간 제한 경로를 정의할 수 있습니다. 이렇게 하면 정의된 기간 내에 반응하지 않은 개인에 대한 두 번째 경로가 만들어집니다. 반응 이벤트를 사용하는 여정을 테스트할 때 테스트 모드 **[!UICONTROL 대기 시간]**&#x200B;의 기본값과 최소값은 40초입니다. [이 섹션](../building-journeys/testing-the-journey.md)을 참조하십시오.

## 가드레일 및 제한 사항 {#guardrails-limitations}

* **[!UICONTROL 반응]** 활동은 여정 캔버스에서 **채널 작업 활동** 후에 [즉시](journeys-message.md)해야 합니다.
* **[!UICONTROL 반응]** 활동 전에 채널 작업 활동이 없으면 활동을 사용할 수 없습니다.
* 채널 액션과 **[!UICONTROL 반응]** 활동 사이에 **[!UICONTROL 대기]** 활동 또는 다른 활동을 배치하는 것은 지원되지 않으며 예상대로 반응이 작동하지 않을 수 있습니다.
* 반응 이벤트는 동일한 여정 내에서만 전송된 메시지를 추적할 수 있습니다. 다른 여정에서 발생하는 메시지를 추적할 수 없습니다.
* 반응 이벤트는 &quot;추적됨&quot; 유형의 링크에 대한 클릭을 추적합니다. 구독 취소 및 미러 페이지 링크는 고려되지 않습니다.
* 이메일에 포함된 0픽셀 이미지를 사용하여 이메일 열람을 추적합니다. 이메일 클라이언트(예: Gmail)가 이미지를 차단하는 경우 이메일 열기는 고려하지 않습니다.
