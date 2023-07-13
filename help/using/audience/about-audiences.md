---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Experience Platform 대상자 기본 정보
description: Adobe Experience Platform 대상자를 사용하여 작업하는 방법에 대해 알아봅니다
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 0%

---

# Adobe Experience Platform 대상자 시작 {#about-segments}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_segment"
>title="Audience"
>abstract="Adobe Experience Platform은 실시간 고객 프로필 데이터를 활용함으로써 세그먼트 정의를 쉽게 작성하여 고객의 고유한 행동과 선호도를 포착하는 타겟팅된 대상자를 만들 수 있습니다."

[!DNL Journey Optimizer] 을(를) 사용하면 다음에서 직접 실시간 고객 프로필 데이터를 사용하여 Adobe Experience Platform 대상을 구축하고 활용할 수 있습니다. **[!UICONTROL 대상]** 메뉴를 사용하여 여정 또는 캠페인에 사용할 수 있습니다.

다음에서 자세히 알아보기 [Adobe Experience Platform 세그멘테이션 서비스 설명서](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

## 에서 대상 사용 [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

에서 대상을 활용할 수 있습니다. **[!DNL Journey Optimizer]** 다른 방법으로:

* 다음에 대한 대상자 선택 **campaign**: 선택한 대상자에 속하는 모든 개인에게 메시지가 전송됩니다. [캠페인 대상자 정의 방법 알아보기](../campaigns/create-campaign.md#define-the-audience-audience).

* 사용 **대상자 읽기** 여정의 오케스트레이션 활동을 통해 대상에 있는 모든 개인이 여정에 들어가 여정에 포함된 메시지를 수신하도록 할 수 있습니다.

  &quot;실버 고객&quot; 대상이 있다고 가정해 보겠습니다. 이 활동을 사용하면 모든 실버 고객이 여정을 입력하고 일련의 개인화된 메시지를 보내도록 할 수 있습니다. [대상자 읽기 활동을 구성하는 방법 알아보기](../building-journeys/read-audience.md#configuring-segment-trigger-activity).

* 사용 **대상 자격 조건** 여정 이벤트 활동 을 통해 Adobe Experience Platform 대상자 출입구를 기준으로 여정에서 개인 사용자가 들어오거나 앞으로 이동하도록 할 수 있습니다.

  예를 들어 모든 신규 실버 고객이 여정을 입력하고 메시지를 보내도록 할 수 있습니다. 이 활동을 사용하는 방법에 대한 자세한 내용은 [대상 자격 활동을 구성하는 방법 알아보기](../building-journeys/audience-qualification-events.md).

* 사용 **조건** 여정의 활동을 통해 대상자 멤버십을 기반으로 조건을 작성할 수 있습니다. [조건에서 대상을 사용하는 방법 알아보기](../building-journeys/condition-activity.md#using-a-segment).

## 대상 평가 방법{#evaluation-method-in-journey-optimizer}

Adobe Journey Optimizer에서 대상은 다음 두 가지 평가 방법 중 하나를 사용하여 세그먼트 정의에서 생성됩니다.

* **스트리밍 세분화**: 새 데이터가 시스템으로 유입될 때 대상의 프로필 목록이 실시간으로 최신 상태로 유지됩니다.

  스트리밍 세분화는 사용자 활동에 대한 응답으로 대상자를 업데이트하는 지속적인 데이터 선택 프로세스입니다. 세그먼트 정의가 구축되고 결과 대상이 저장되면 Journey Optimizer으로 들어오는 데이터에 대해 세그먼트 정의가 적용됩니다. 즉, 프로필 데이터가 변경될 때 개인이 대상에서 추가되거나 제거되어 대상 대상이 항상 관련성이 있게 됩니다.

* **일괄 처리 세분화**: 대상자에 대한 프로필 목록은 24시간마다 평가됩니다.

  일괄 처리 세그먼테이션은 세그먼트 정의를 통해 모든 프로필 데이터를 한 번에 처리하는 스트리밍 세그먼테이션의 대안입니다. 이렇게 하면 사용하기 위해 저장 및 내보낼 수 있는 대상자의 스냅샷이 생성됩니다. 그러나 스트리밍 세분화와 달리 배치 세분화는 실시간으로 대상 목록을 지속적으로 업데이트하지 않으며 배치 프로세스 후에 들어오는 새 데이터는 다음 배치 프로세스가 진행될 때까지 대상에 반영되지 않습니다.&quot;

배치 세그먼테이션과 스트리밍 세그먼테이션 간의 의사 결정은 복잡성과 세그먼트 정의 규칙 평가 비용을 기준으로 각 대상자에 대해 시스템에서 수행됩니다. 에서 각 대상에 대한 평가 방법을 볼 수 있습니다. **[!UICONTROL 평가 방법]** 대상 목록의 열입니다.

![](assets/evaluation-method.png)

>[!NOTE]
>
>다음과 같은 경우 **[!UICONTROL 평가 방법]** 열이 표시되지 않습니다. 목록 오른쪽 상단의 구성 단추를 사용하여 추가해야 합니다.

대상을 처음 정의한 후 자격이 주어지면 프로필이 대상에 추가됩니다.

이전 데이터에서 대상을 다시 채우는 데 최대 24시간이 걸릴 수 있습니다. 대상자가 다시 채워진 후 대상자는 계속 최신 상태로 유지되며 항상 타깃팅할 준비가 되어 있습니다.
