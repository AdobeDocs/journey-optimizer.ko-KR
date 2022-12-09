---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Experience Platform 세그먼트 정보
description: Adobe Experience Platform 세그먼트를 구성하는 방법 알아보기
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: bfd262db2fd12afbb7df6c73c68b29d18a1abf98
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# Adobe Experience Platform 세그먼트 시작 {#about-segments}

[!DNL Journey Optimizer]  에서는 실시간 고객 프로필 데이터를 사용하여 Adobe Experience Platform 세그먼트를 **[!UICONTROL Segments]** 메뉴를 보고 여정에 활용할 수 있습니다.

세그먼테이션 서비스 자체에서도 만들 수 있습니다. 자세한 내용은 [Adobe Experience Platform 세그멘테이션 서비스 설명서](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

여정의 세그먼트를 다양한 방법으로 활용할 수 있습니다.

* 다음 작업 **세그먼트 읽기** 오케스트레이션 활동을 통해 지정된 세그먼트에 속하는 모든 개인이 여정을 시작합니다. 여정에 포함된 메시지는 세그먼트에 속하는 개인에게 전송됩니다. &quot;실버 고객&quot; 세그먼트가 있다고 가정해 보겠습니다. 이 활동을 사용하면 모든 실버 고객이 여정을 시작하고 일련의 개인화된 메시지를 보낼 수 있습니다.

   사용 방법에 대한 자세한 내용 **[!UICONTROL Read segment]** 활동, [이 섹션](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

* 를 사용하십시오 **세그먼트 자격** 이벤트 활동을 통해 Adobe Experience Platform 세그먼트 출입구 및 종료에 따라 개인이 여정에 들어오거나 앞으로 이동하도록 할 수 있습니다. 예를 들어 새로운 모든 실버 고객이 여정을 시작하고 메시지를 보낼 수 있습니다. 이 활동을 사용하는 방법에 대한 자세한 내용은 [이 섹션](../building-journeys/segment-qualification-events.md).

* 빌드 **복잡한 조건** 를 사용하십시오. 추가 정보 [이 섹션](../building-journeys/condition-activity.md#using-a-segment).

## 대상 평가 방법{#evaluation-method-in-journey-optimizer}

Adobe Journey Optimizer에서 다음 평가 방법 중 하나를 사용하여 세그먼트 정의에서 대상이 생성됩니다.

* 스트리밍 세그먼테이션 - 새로운 데이터가 시스템으로 이동하는 동안 세그먼트의 대상 목록이 실시간으로 최신 상태로 유지됩니다. 스트리밍 세그먼테이션은 사용자 활동에 대한 응답으로 세그먼트를 업데이트하는 지속적인 데이터 선택 프로세스입니다. 세그먼트가 만들어지고 저장되면 들어오는 데이터에 대해 세그먼트 정의가 Journey Optimizer에 적용됩니다. 세그먼트 추가 및 제거는 정기적으로 처리되므로 타겟 대상이 적절하도록 합니다.

* 배치 세그먼테이션 - 세그먼트의 대상 목록이 24시간 간격으로 평가됩니다. 일괄 처리 세그먼테이션은 진행 중인 데이터 선택 프로세스의 대안으로서, 세그먼트 정의를 통해 모든 프로필 데이터를 한 번에 이동하여 해당 대상을 생성합니다. 세그먼트가 만들어지면 저장되고 저장되므로 사용할 수 있도록 내보낼 수 있습니다.

배치 세그먼테이션과 스트리밍 세그먼테이션 간의 결정은 세그먼트 규칙 평가의 복잡성과 비용을 기반으로, 각 세그먼트 정의에 대해 시스템에서 수행됩니다.

에서 각 세그먼트에 대한 평가 방법을 볼 수 있습니다 **[!UICONTROL Evaluation method]** 세그먼트 목록의 열입니다.

세그먼트를 처음 정의하면 자격이 되면 프로필이 대상에 추가됩니다.

이전 데이터에서 대상자를 다시 채우는 데는 최대 24시간이 걸릴 수 있습니다. 대상이 다시 채워지면 대상이 계속 최신 상태로 유지되며 항상 타깃팅할 준비가 됩니다.
