---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Experience Platform 대상자 정보
description: Adobe Experience Platform 대상자 사용 방법 알아보기
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: d18b24f6afcd64745fe7bd3b3bc9832342b91c7b
workflow-type: tm+mt
source-wordcount: '909'
ht-degree: 47%

---

# Adobe Experience Platform 대상자 시작 {#about-segments}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_segment"
>title="Audience"
>abstract="Adobe Experience Platform에서는 실시간 고객 프로필 데이터를 활용하여 간단히 세그먼트 정의를 작성함으로써 고객의 고유 행동과 선호를 포착한 타겟팅 대상자를 만들 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_audience"
>title="캠페인 대상자 선택"
>abstract="이 목록에는 사용 가능한 모든 Adobe Experience Platform 대상자가 표시됩니다. 캠페인으로 타겟팅할 대상자를 선택합니다. 캠페인에 구성된 메시지는 선택한 대상자에 속한 모든 개인 사용자에게 전송됩니다. [대상자에 대해 자세히 알아보기](../audience/about-audiences.md)"

대상자는 유사한 행동 및/또는 특성을 공유하는 사람들의 집합입니다. 세그먼트 정의 또는 대상 구성을 사용하여 Adobe Experience Platform에서 생성하거나 CSV 파일에서 가져올 수 있습니다. 에서 대상자에 대해 자세히 알아보기 [Adobe Experience Platform 세그멘테이션 서비스 설명서](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=ko){target="_blank"}.

[!DNL Journey Optimizer] 을(를) 사용하면 다음에서 직접 Adobe Experience Platform 대상을 작성할 수 있습니다. **[!UICONTROL 대상]** 메뉴를 사용하여 여정 또는 캠페인에 활용할 수 있습니다.

## [!DNL Journey Optimizer]에서 대상자 사용 {#segments-in-journey-optimizer}

다음을 사용하여 생성된 Adobe Experience Platform 대상을 캠페인 및 여정에서 선택할 수 있습니다. [세그먼트 정의](../audience/creating-a-segment-definition.md).

>[!NOTE]
>
>또한 을 사용하여 만든 Adobe Experience Platform 대상을 타깃팅할 수도 있습니다. [대상자 구성](../audience/get-started-audience-orchestration.md) 또는 [csv 파일에서 업로드됨](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html#import-audience){target="_blank"}. 이 기능은 현재 Private Beta로 사용할 수 있습니다.


**[!DNL Journey Optimizer]**&#x200B;에서 다양한 방법으로 대상자를 활용할 수 있습니다.

* **캠페인** 대상자를 선택하면 선택한 대상자에 속하는 모든 개인에게 메시지를 보냅니다. [캠페인의 대상자를 정의하는 방법을 알아봅니다](../campaigns/create-campaign.md#define-the-audience-audience).

* 여정에서 **대상자 읽기** 오케스트레이션 활동을 사용하면 대상자에 속하는 모든 개인이 여정을 시작하면 여정에 포함된 메시지를 받도록 할 수 있습니다.

  “실버 고객”이라는 대상자가 있다고 가정해 보겠습니다. 이 활동으로 모든 실버 고객이 여정에 입장하도록 하여 이들에게 연속으로 이어지는 개인화된 메시지를 보낼 수 있습니다. [대상자 읽기 활동을 구성하는 방법을 알아봅니다](../building-journeys/read-audience.md#configuring-segment-trigger-activity).

* 여정에 **대상자 자격 조건** 이벤트 활동을 사용하면 Adobe Experience Platform 대상자 입장 및 퇴장을 기준으로 여정에 개인 사용자가 입장하거나 다음 단계로 진행하도록 할 수 있습니다.

  예를 들면 모든 신규 실버 고객이 여정에 입장하도록 하여 이들에게 메시지를 보낼 수 있습니다. 이 활동을 사용하는 자세한 방법은 [대상자 자격 조건 활동을 구성하는 방법 알아보기](../building-journeys/audience-qualification-events.md)를 참조하세요.

* 여정에 **조건** 활동을 사용하면 대상자 멤버십을 기반으로 조건을 작성할 수 있습니다. [조건에서 대상자를 사용하는 방법을 알아봅니다](../building-journeys/condition-activity.md#using-a-segment).

## 대상자 평가 방법 {#evaluation-method-in-journey-optimizer}

Adobe Journey Optimizer에서 대상자는 아래 세 가지 평가 방법 중 하나를 사용하여 세그먼트 정의에서 생성됩니다.

+++ 스트리밍 세분화

대상에 대한 프로필 목록은 새 데이터가 시스템으로 유입될 때 실시간으로 최신 상태로 유지됩니다.

스트리밍 세분화는 사용자 활동에 대응하여 대상자를 업데이트하는 진행형 데이터 선택 프로세스입니다. 세그먼트 정의를 작성하고 결과 대상자를 저장한 다음부터는 Journey Optimizer로 들어오는 데이터에 세그먼트 정의가 적용됩니다. 즉, 프로필 데이터가 변경될 때 개인이 대상에서 추가되거나 제거되어 대상 대상이 항상 관련성이 있게 됩니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/streaming-segmentation.html){target="_blank"}

>[!NOTE]
>
>스트리밍 세분화 기준으로 올바른 이벤트를 사용해야 합니다. [자세히 알아보기](#streaming-segmentation-events-guardrails)

+++

+++ 배치 세분화

대상자에 대한 프로필 목록은 24시간마다 평가됩니다.

일괄 처리 세분화는 스트리밍 세분화 대신 사용할 수 있는 방법으로, 세그먼트 정의를 통해 모든 프로필 데이터를 한꺼번에 처리합니다. 이를 통해 대상자의 스냅샷을 만드는데, 이를 저장하거나 내보내서 사용할 수 있습니다. 하지만 스트리밍 세분화와 달리 배치 세분화는 실시간으로 대상 목록을 지속적으로 업데이트하지 않으며, 배치 프로세스 후에 들어오는 새 데이터는 다음 배치 프로세스가 진행될 때까지 대상에 반영되지 않습니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html#batch){target="_blank"}

+++

+++ 에지 세분화

에지 세그멘테이션은 Adobe Experience Platform의 세그먼트를 즉시 평가하는 기능입니다 [가장자리에](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=ko-KR){target="_blank"}, enabling same-page and next-page personalization use cases. Currently only select query types can be evaluated with edge segmentation. [Learn more](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/edge-segmentation.html#query-types){target="_blank"}

+++

사용할 평가 방법을 알고 있는 경우 드롭다운 목록을 사용하여 선택합니다. 돋보기로 찾아보기 아이콘 폴더 아이콘을 클릭하여 사용 가능한 세그먼트 정의 평가 방법 목록을 볼 수도 있습니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html#segment-properties){target="_blank"}

![](assets/evaluation-methods.png)

<!--The determination between batch segmentation and streaming segmentation is made by the system for each audience, based on the complexity and the cost of evaluating the segment definition rule. You can view the evaluation method for each audience in the **[!UICONTROL Evaluation method]** column of the audience list.
    
![](assets/evaluation-method.png)

>[!NOTE]
>
>If the **[!UICONTROL Evaluation method]** column does not display, you  need to add it using configuration button on the top right of the list.-->

대상자를 처음 정의한 후 프로필이 자격 조건을 충족하면 대상자에 추가됩니다.

이전 데이터를 사용하여 대상자를 다시 채우는 데 최대 24시간이 걸릴 수 있습니다. 대상자를 다시 채운 후 대상자는 계속 최신 상태로 유지되며 언제든 타겟팅할 수 있습니다.

### 스트리밍 세분화를 통한 이벤트 사용 {#streaming-segmentation-events-guardrails}

스트리밍 세분화는 가치가 높은 사용 사례를 사용하는 실시간 개인화에 유용합니다. 하지만, 옳은 것을 선택하는 것은 중요하다 [events](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html#events){target="_blank"} 을 세그먼테이션 기준으로 사용합니다.

따라서 스트리밍 세분화 최적 성능을 위해 다음 이벤트를 사용하지 마십시오.

* **메시지 열림** 인터랙션 유형 이벤트

  대상을 구축할 때 **메시지 열림** 상호 작용 이벤트는 사용자 활동의 실제 지표가 아니며 세그멘테이션 성능에 부정적인 영향을 줄 수 있으므로 신뢰할 수 없게 되었습니다. 여기에서 그 이유를 알아보십시오. [Adobe 블로그 게시물](https://blog.adobe.com/en/publish/2021/06/24/what-apples-mail-privacy-protection-means-for-email-marketers){target="_blank"}.

  따라서 Adobe은 를 사용하지 않는 것을 권장합니다 **메시지 열림** 스트리밍 세그먼테이션과 상호 작용 이벤트. 대신 클릭, 구매 또는 비콘 데이터와 같은 실제 사용자 활동 신호를 사용합니다.

* **메시지 전송됨** 피드백 상태 이벤트

  다음 **메시지 전송됨** 피드백 이벤트는 종종 이메일을 보내기 전에 빈도 또는 제외 확인에 사용됩니다. Adobe은 성능에 부담을 주고 시스템 저하를 유발할 수 있으므로 피하는 것이 좋습니다.

  따라서 빈도 또는 제외 논리의 경우 대신 비즈니스 규칙을 사용하십시오. **메시지 전송됨** 피드백 이벤트. 비즈니스 규칙에 대한 기존 월별 케이던스를 보완하여 개별 프로필에 대한 일일 빈도 상한을 곧 사용할 수 있습니다.

>[!NOTE]
>
>다음을 사용할 수 있습니다. **메시지 열림** 및 **메시지 전송됨** 성능 문제 없이 일괄 세분화된 이벤트.
