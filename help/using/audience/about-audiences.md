---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Experience Platform 대상자 정보
description: Adobe Experience Platform 대상자 사용 방법 알아보기
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 100%

---

# Adobe Experience Platform 대상자 시작 {#about-segments}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_segment"
>title="Audience"
>abstract="Adobe Experience Platform에서는 실시간 고객 프로필 데이터를 활용하여 간단히 세그먼트 정의를 작성함으로써 고객의 고유 행동과 선호를 포착한 타겟팅 대상자를 만들 수 있습니다."

[!DNL Journey Optimizer]의 **[!UICONTROL 대상자]** 메뉴에서 직접 실시간 고객 프로필 데이터를 사용하여 Adobe Experience Platform 대상자를 작성하고 활용하며 여정이나 캠페인에 사용할 수 있습니다.

[Adobe Experience Platform Segmentation Service 설명서](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=ko)에서 자세히 알아보세요.

## [!DNL Journey Optimizer]에서 대상자 사용 {#segments-in-journey-optimizer}

**[!DNL Journey Optimizer]**&#x200B;에서 다양한 방법으로 대상자를 활용할 수 있습니다.

* **캠페인** 대상자를 선택하면 선택한 대상자에 속하는 모든 개인에게 메시지를 보냅니다. [캠페인의 대상자를 정의하는 방법을 알아봅니다](../campaigns/create-campaign.md#define-the-audience-audience).

* 여정에서 **대상자 읽기** 오케스트레이션 활동을 사용하면 대상자에 속하는 모든 개인이 여정을 시작하면 여정에 포함된 메시지를 받도록 할 수 있습니다.

  “실버 고객”이라는 대상자가 있다고 가정해 보겠습니다. 이 활동으로 모든 실버 고객이 여정에 입장하도록 하여 이들에게 연속으로 이어지는 개인화된 메시지를 보낼 수 있습니다. [대상자 읽기 활동을 구성하는 방법을 알아봅니다](../building-journeys/read-audience.md#configuring-segment-trigger-activity).

* 여정에 **대상자 자격 조건** 이벤트 활동을 사용하면 Adobe Experience Platform 대상자 입장 및 퇴장을 기준으로 여정에 개인 사용자가 입장하거나 다음 단계로 진행하도록 할 수 있습니다.

  예를 들면 모든 신규 실버 고객이 여정에 입장하도록 하여 이들에게 메시지를 보낼 수 있습니다. 이 활동을 사용하는 자세한 방법은 [대상자 자격 조건 활동을 구성하는 방법 알아보기](../building-journeys/audience-qualification-events.md)를 참조하세요.

* 여정에 **조건** 활동을 사용하면 대상자 멤버십을 기반으로 조건을 작성할 수 있습니다. [조건에서 대상자를 사용하는 방법을 알아봅니다](../building-journeys/condition-activity.md#using-a-segment).

## 대상자 평가 방법{#evaluation-method-in-journey-optimizer}

Adobe Journey Optimizer에서 대상자는 세그먼트 정의를 기반으로 다음 두 가지 평가 방법 중 하나를 사용하여 생성됩니다.

* **스트리밍 세분화**: 새 데이터가 시스템으로 유입될 때마다 대상자의 프로필 목록이 실시간으로 최신 상태로 업데이트됩니다.

  스트리밍 세분화는 사용자 활동에 대응하여 대상자를 업데이트하는 진행형 데이터 선택 프로세스입니다. 세그먼트 정의를 작성하고 결과 대상자를 저장한 다음부터는 Journey Optimizer로 들어오는 데이터에 세그먼트 정의가 적용됩니다. 즉, 타겟팅 대상자의 관련성을 유지하기 위해 개인 사용자의 프로필 데이터가 변경될 때마다 해당 개인을 대상자에 추가하거나 대상자에서 제거합니다.

* **일괄 처리 세분화**: 대상자에 포함할 프로필 목록을 24시간마다 평가합니다.

  일괄 처리 세분화는 스트리밍 세분화 대신 사용할 수 있는 방법으로, 세그먼트 정의를 통해 모든 프로필 데이터를 한꺼번에 처리합니다. 이를 통해 대상자의 스냅샷을 만드는데, 이를 저장하거나 내보내서 사용할 수 있습니다. 그러나 스트리밍 세분화와 달리 일괄 처리 세분화는 계속 실시간으로 대상자 목록을 업데이트하지 않고, 일괄 처리 프로세스 이후에 수집한 데이터는 다음 일괄 처리 프로세스 때까지 대상자에 반영되지 않습니다.

일괄 처리 세분화와 스트리밍 세분화 중 어느 방법을 사용할지는 시스템에서 각 대상자의 복잡도와 세그먼트 정의 규칙 평가 비용을 기반으로 결정합니다. 각 대상자의 평가 방밥은 대상자 목록의 **[!UICONTROL 평가 방법]** 열에서 확인할 수 있습니다.

![](assets/evaluation-method.png)

>[!NOTE]
>
>**[!UICONTROL 평가 방법]** 열이 표시되지 않는 경우 목록 오른쪽 위의 구성 버튼을 사용하여 추가해야 합니다.

대상자를 처음 정의한 후 프로필이 자격 조건을 충족하면 대상자에 추가됩니다.

이전 데이터를 사용하여 대상자를 다시 채우는 데 최대 24시간이 걸릴 수 있습니다. 대상자를 다시 채운 후 대상자는 계속 최신 상태로 유지되며 언제든 타겟팅할 수 있습니다.
