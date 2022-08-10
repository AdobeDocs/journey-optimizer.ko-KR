---
title: Adobe Experience Platform 세그먼트
description: Adobe Experience Platform 세그먼트를 구성하는 방법 알아보기
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 2%

---

# Adobe Experience Platform 세그먼트 시작 {#about-segments}

[!DNL Journey Optimizer]  에서는 **[!UICONTROL Segments]** 메뉴를 보고 여정에 활용할 수 있습니다.

세그먼테이션 서비스 자체에서도 만들 수 있습니다. 자세한 내용은 [Adobe Experience Platform 세그멘테이션 서비스 설명서](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

여정의 세그먼트를 다양한 방법으로 활용할 수 있습니다.

* 다음 작업 **세그먼트 읽기** 오케스트레이션 활동을 통해 지정된 세그먼트에 속하는 모든 개인이 여정에 들어갈 수 있습니다. 여정에 포함된 메시지는 세그먼트에 속하는 개인에게 전송됩니다. &quot;실버 고객&quot; 세그먼트가 있다고 가정해 보겠습니다. 이 활동을 사용하면 모든 실버 고객이 여정을 입력하고 일련의 개인화된 메시지를 전송하도록 할 수 있습니다.

   사용 방법에 대한 자세한 내용 **[!UICONTROL Read segment]** 활동, [이 섹션](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

* 를 사용하십시오 **세그먼트 자격** 이벤트 활동을 통해 개인이 Adobe Experience Platform 세그먼트 출입구 및 종료에 따라 여정에 들어오거나 앞으로 이동하도록 할 수 있습니다. 예를 들어 모든 신규 실버 고객이 여정을 입력하고 메시지를 보내게 할 수 있습니다. 이 활동을 사용하는 방법에 대한 자세한 내용은 [이 섹션](../building-journeys/segment-qualification-events.md).

* 빌드 **복잡한 조건** ( 단순 또는 고급 표현식 편집기를 사용하여 여정에서)을 참조하십시오. 자세한 내용은 [이 섹션](../building-journeys/condition-activity.md#using-a-segment)을 참조하십시오.

## Adobe Journey Optimizer의 평가 방법 {#evaluation-method-in-journey-optimizer}

Adobe Journey Optimizer에서 대상은 다음 평가 방법 중 하나를 사용하여 세그먼트 정의에서 생성됩니다.

* 스트리밍 세그먼테이션 - 새로운 데이터가 시스템으로 이동하는 동안 세그먼트의 대상 목록이 실시간으로 최신 상태로 유지됩니다.
* 배치 세그먼테이션 - 세그먼트의 대상 목록이 지난 시간에 도착한 데이터를 기반으로 시간별로 업데이트됩니다.

배치 세그먼테이션과 스트리밍 세그먼테이션 간의 결정은 세그먼트 규칙 평가의 복잡성과 비용을 기반으로, 각 세그먼트 정의에 대해 시스템에서 수행됩니다.

에서 각 세그먼트에 대한 평가 방법을 볼 수 있습니다 **[!UICONTROL Evaluation method]** 세그먼트 목록의 열입니다.

세그먼트를 처음 정의하면 자격이 되면 프로필이 대상에 추가됩니다.

이전 데이터에서 대상자를 다시 채우는 데는 최대 24시간이 걸릴 수 있습니다. 대상이 다시 채워지면 대상이 계속 최신 상태로 유지되며 항상 타깃팅할 준비가 됩니다.
