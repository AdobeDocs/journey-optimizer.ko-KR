---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Experience Platform 세그먼트
description: Adobe Experience Platform 세그먼트를 구성하는 방법 알아보기
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: 6c255d66fb89ba756add062d8a4315dd622fd8e7
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 1%

---

# Adobe Experience Platform 세그먼트 시작 {#about-segments}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_segment"
>title="세그먼트"
>abstract="Adobe Experience Platform은 실시간 고객 프로필 데이터를 활용하여 고객의 고유한 행동과 선호도를 캡처하는 타겟팅된 세그먼트를 쉽게 만들 수 있도록 해줍니다."

[!DNL Journey Optimizer]  에서는 **[!UICONTROL 세그먼트]** 메뉴를 보고 여정 또는 캠페인에 사용하십시오.

또한 세그먼테이션 서비스 자체에서 세그먼트를 만들 수도 있습니다. 자세한 내용은 [Adobe Experience Platform 세그멘테이션 서비스 설명서](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

## 에서 세그먼트 사용 [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

에서 세그먼트를 활용할 수 있습니다 **[!DNL Journey Optimizer]** 다양한 방법으로 다음을 수행합니다.

* 세그먼트를 **캠페인을 위한 대상**: 선택한 세그먼트에 속하는 모든 개인에게 메시지가 전송됩니다. [캠페인의 대상자를 정의하는 방법을 알아봅니다](../campaigns/create-campaign.md#define-the-audience-audience).

* 다음 작업 **세그먼트 읽기** 세그먼트의 모든 개인이 여정을 시작하고 여정에 포함된 메시지를 수신하도록 하는 여정의 오케스트레이션 활동.

   &quot;실버 고객&quot; 세그먼트가 있다고 가정해 보겠습니다. 이 활동을 사용하면 모든 실버 고객이 여정을 입력하고 일련의 개인화된 메시지를 전송하도록 할 수 있습니다. [세그먼트 읽기 활동을 구성하는 방법을 알아봅니다](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

* 를 사용하십시오 **세그먼트 자격** 여정의 이벤트 활동으로 Adobe Experience Platform 세그먼트 출입구 및 종료에 따라 개인이 여정에 들어오거나 앞으로 이동하도록 합니다.

   예를 들어 모든 신규 실버 고객이 여정을 입력하고 메시지를 보내게 할 수 있습니다. 이 활동을 사용하는 방법에 대한 자세한 내용은 [세그먼트 자격 활동을 구성하는 방법을 알아봅니다](../building-journeys/segment-qualification-events.md).

* 를 사용하십시오 **조건** 활동 을 사용하여 세그먼트 멤버십에 따라 조건을 만들 수 있습니다. [조건에서 세그먼트를 사용하는 방법 알아보기](../building-journeys/condition-activity.md#using-a-segment).

## 대상 평가 방법{#evaluation-method-in-journey-optimizer}

Adobe Journey Optimizer에서 대상은 다음 두 가지 평가 방법 중 하나를 사용하여 세그먼트 정의에서 생성됩니다.

* **스트리밍 세그멘테이션**: 세그먼트에 대한 대상 목록은 새 데이터가 시스템에 유입될 때 실시간으로 최신 상태로 유지됩니다.

   스트리밍 세그먼테이션은 사용자 활동에 대한 응답으로 세그먼트를 업데이트하는 지속적인 데이터 선택 프로세스입니다. 세그먼트가 만들어지고 저장되면, 세그먼트 정의가 Journey Optimizer에 들어오는 데이터에 대해 적용됩니다. 즉, 프로필 데이터가 변경됨에 따라 개인들이 세그먼트에서 추가 또는 제거되므로 타겟 대상이 항상 관련성이 있는지 확인합니다.

* **일괄 세분화**: 세그먼트의 대상 목록은 24시간 간격으로 평가됩니다.

   일괄 처리 세그먼테이션은 세그먼트 정의를 통해 모든 프로필 데이터를 한 번에 처리하는 스트리밍 세그먼테이션의 대안입니다. 이렇게 하면 저장되고 내보낼 수 있는 대상의 스냅숏이 만들어집니다. 그러나 스트리밍 세그먼테이션과 달리 배치 세그먼테이션은 대상 목록을 실시간으로 지속적으로 업데이트하지 않으며, 일괄 처리 프로세스 이후에 들어오는 새 데이터는 다음 일괄 처리 프로세스 때까지 세그먼트에 반영되지 않습니다.&quot;

배치 세그먼테이션과 스트리밍 세그먼테이션 간의 결정은 세그먼트 규칙 평가의 복잡성과 비용을 기반으로, 각 세그먼트 정의에 대해 시스템에서 수행됩니다. 에서 각 세그먼트에 대한 평가 방법을 볼 수 있습니다 **[!UICONTROL 평가 방법]** 세그먼트 목록의 열입니다.

![](assets/evaluation-method.png)

>[!NOTE]
>
>만약 **[!UICONTROL 평가 방법]** 열이 표시되지 않으면 목록 오른쪽 상단의 구성 버튼을 사용하여 열을 추가해야 합니다.

세그먼트를 처음 정의하면 자격이 되면 프로필이 대상에 추가됩니다.

이전 데이터에서 대상자를 다시 채우는 데는 최대 24시간이 걸릴 수 있습니다. 대상이 다시 채워지면 대상이 계속 최신 상태로 유지되며 항상 타깃팅할 준비가 됩니다.
