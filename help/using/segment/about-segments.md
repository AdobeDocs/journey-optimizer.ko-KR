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
ht-degree: 8%

---

# Adobe Experience Platform 세그먼트 시작 {#about-segments}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_segment"
>title="세그먼트"
>abstract="실시간 고객 프로필 데이터를 활용하여 Adobe Experience Platform에서 고객의 고유 비헤이비어와 환경 설정을 캡처하는 타겟팅된 세그먼트를 쉽게 만들 수 있습니다."

[!DNL Journey Optimizer]  에서 직접 실시간 고객 프로필 데이터를 사용하여 Adobe Experience Platform 세그먼트를 만들 수 있습니다. **[!UICONTROL 세그먼트]** 메뉴를 사용하여 여정 또는 캠페인에 사용할 수 있습니다.

또한 세그먼테이션 서비스 자체에서 세그먼트를 만들 수도 있습니다. 다음에서 자세히 알아보기 [Adobe Experience Platform 세그멘테이션 서비스 설명서](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

## [!DNL Journey Optimizer]에서  세그먼트 사용하기 {#segments-in-journey-optimizer}

에서 세그먼트를 활용할 수 있습니다. **[!DNL Journey Optimizer]** 다른 방법으로:

* 세그먼트를 다음으로 선택 **캠페인 대상**: 선택한 세그먼트에 속하는 모든 개인에게 메시지가 전송됩니다. [캠페인 대상자 정의 방법 알아보기](../campaigns/create-campaign.md#define-the-audience-audience).

* 사용 **세그먼트 읽기** 여정의 오케스트레이션 활동을 통해 세그먼트에 있는 모든 개인이 여정을 입력하고 여정에 포함된 메시지를 받도록 할 수 있습니다.

   &quot;실버 고객&quot; 세그먼트가 있다고 가정해 보겠습니다. 이 활동을 사용하면 모든 실버 고객이 여정을 입력하고 일련의 개인화된 메시지를 보내도록 할 수 있습니다. [세그먼트 읽기 활동을 구성하는 방법 알아보기](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

* 사용 **세그먼트 선별** 여정 이벤트 활동 을 통해 Adobe Experience Platform 세그먼트 출입구를 기준으로 여정에서 개인 사용자가 들어오거나 앞으로 이동하도록 할 수 있습니다.

   예를 들어 모든 신규 실버 고객이 여정을 입력하고 메시지를 보내도록 할 수 있습니다. 이 활동을 사용하는 방법에 대한 자세한 내용은 [세그먼트 자격 활동을 구성하는 방법 알아보기](../building-journeys/segment-qualification-events.md).

* 사용 **조건** 세그먼트 멤버십을 기반으로 조건을 빌드하기 위한 여정의 활동. [조건에서 세그먼트를 사용하는 방법 알아보기](../building-journeys/condition-activity.md#using-a-segment).

## 대상 평가 방법{#evaluation-method-in-journey-optimizer}

Adobe Journey Optimizer에서 대상은 다음 두 가지 평가 방법 중 하나를 사용하여 세그먼트 정의에서 생성됩니다.

* **스트리밍 세분화**: 새 데이터가 시스템으로 유입되므로 세그먼트의 대상 목록은 실시간으로 최신 상태로 유지됩니다.

   스트리밍 세분화는 사용자 활동에 대응하여 세그먼트를 업데이트하는 진행 중인 데이터 선택 프로세스입니다. 세그먼트를 작성하고 저장하면 Journey Optimizer으로 들어오는 데이터에 대해 세그먼트 정의가 적용됩니다. 즉, 프로필 데이터가 변경될 때 개인이 추가되거나 세그먼트에서 제거되어 타겟 대상자가 항상 관련성이 있게 됩니다.

* **일괄 처리 세분화**: 세그먼트의 대상 목록은 24시간마다 평가됩니다.

   일괄 처리 세그먼테이션은 세그먼트 정의를 통해 모든 프로필 데이터를 한 번에 처리하는 스트리밍 세그먼테이션의 대안입니다. 이렇게 하면 사용하기 위해 저장 및 내보낼 수 있는 대상자의 스냅샷이 생성됩니다. 그러나 스트리밍 세분화와 달리 배치 세분화는 실시간으로 대상 목록을 지속적으로 업데이트하지 않으며 배치 프로세스 후에 들어오는 새 데이터는 다음 배치 프로세스가 진행될 때까지 세그먼트에 반영되지 않습니다.&quot;

배치 세그먼테이션과 스트리밍 세그먼테이션 간의 결정은 복잡성과 세그먼트 규칙 평가 비용을 기준으로 각 세그먼트 정의에 대해 시스템에서 수행됩니다. 에서 각 세그먼트에 대한 평가 방법을 볼 수 있습니다. **[!UICONTROL 평가 방법]** 세그먼트 목록의 열입니다.

![](assets/evaluation-method.png)

>[!NOTE]
>
>다음과 같은 경우 **[!UICONTROL 평가 방법]** 열이 표시되지 않습니다. 목록 오른쪽 상단의 구성 단추를 사용하여 추가해야 합니다.

세그먼트를 처음 정의한 후 자격이 주어지면 프로필이 대상자에 추가됩니다.

이전 데이터에서 대상을 다시 채우는 데 최대 24시간이 걸릴 수 있습니다. 대상자가 다시 채워진 후 대상자는 계속 최신 상태로 유지되며 항상 타깃팅할 준비가 되어 있습니다.
