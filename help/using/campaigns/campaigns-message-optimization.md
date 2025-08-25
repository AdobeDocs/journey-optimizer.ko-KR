---
solution: Journey Optimizer
product: journey optimizer
title: 메시지 최적화
description: 메시지 최적화를 활용하여 개인화되고 최적화된 마케팅 캠페인을 만들 수 있습니다.
role: User
level: Intermediate
keywords: 캠페인 최적화, 실험, 타겟팅, A/B 테스트
exl-id: 0f563d61-7a9e-46bf-adfb-5a26e63505b9
source-git-commit: 17ca5d47fbf20ee25c3728d85877adaccf82aea8
workflow-type: tm+mt
source-wordcount: '1045'
ht-degree: 6%

---

# 캠페인 및 여정의 최적화 {#message-optimization}

최적화는 대상자에게 개인화되고 최적화된 콘텐츠를 제공하는 도구를 통해 <!--based on marketer-defined advanced decision configurations. This ensures that the right message reaches the right audience at the right time in order to maximize the effectiveness of your campaigns. (Removed for now as Decisioning is not yet supported)-->최대의 참여와 성공을 보장하여 <!--customized and -->효과적인 여정 및 캠페인을 만들 수 있습니다.

최적화를 사용하면 다음을 할 수 있습니다.

* [타깃팅](#targeting) 규칙 활용
* [콘텐츠 실험 실행](#experimentation)
* 단일 캠페인 내에서 실험과 타깃팅을 모두 [고급 조합](#combination)을 사용합니다.

여정 또는 캠페인이 라이브되면 정의된 기준에 따라 프로필이 평가되고, 일치하는 기준을 기반으로 여정/캠페인의 적절한 경험 또는 콘텐츠와 함께 전달됩니다.

실험과 타겟팅 간의 차이점은 다음과 같이 요약할 수 있습니다.

* 실험은 트래픽 할당을 기반으로 콘텐츠를 전달할 때 무작위 분할로 구성됩니다&#x200B;.
* 타깃팅은 결정론적 기술을 사용하여 사용자 프로필, 대상 멤버십 또는 컨텍스트 기반 규칙을 기반으로 콘텐츠를 전달합니다.

![](assets/msg-optimization-experiment-vs-targeting.png){width="110%" zoomable="yes"}

➡️ [이 비디오에서 캠페인의 최적화에 대해 자세히 알아보세요](#video)

## 타깃팅 활용 {#targeting}

타깃팅은 사용자 프로필 속성 또는 컨텍스트 속성에 따라 개인화된 콘텐츠를 특정 대상 세그먼트에 전달합니다.

메시지 콘텐츠를 무작위로 할당하는 실험과 달리 타기팅은 콘텐츠를 올바른 대상자에게 전달한다는 측면에서 결정적입니다.

타깃팅을 사용할 경우 다음을 기반으로 특정 규칙을 정의할 수 있습니다.

* 위치(예: **사용자 프로필 특성** 지역 타겟팅), 연령 또는 환경 설정. 예를 들어, 미국의 사용자는 &quot;골든 게이트&quot; 프로모션을 보고 프랑스의 사용자는 &quot;에펠탑&quot; 프로모션을 봅니다.

* 디바이스 유형(예: **컨텍스트 데이터** 디바이스 타기팅), 시간 또는 세션 세부 정보. 예를 들어 데스크탑 사용자는 데스크탑에 최적화된 콘텐츠를 수신하는 반면, 모바일 사용자는 모바일에 최적화된 콘텐츠를 수신합니다.

* 특정 대상 멤버십이 있는 프로필을 포함하거나 제외하는 데 사용할 수 있는 **대상**.

타깃팅을 설정하려면 아래 단계를 따르십시오.

1. [여정](../building-journeys/journey-gs.md#jo-build) 또는 [캠페인](../campaigns/create-campaign.md)을 만듭니다.

   >[!NOTE]
   >
   >여정에 있는 경우 **[!UICONTROL 작업]** 활동을 추가하고 채널 활동을 선택한 다음 **[!UICONTROL 작업 구성]**&#x200B;을 선택하십시오. [자세히 알아보기](../building-journeys/journey-action.md#add-action)

1. **[!UICONTROL 작업]** 탭에서 하나 이상의 작업을 선택합니다.

1. **[!UICONTROL 최적화]** 섹션에서 **[!UICONTROL 타깃팅 규칙 만들기]**&#x200B;를 선택합니다.

   ![](assets/msg-optimization-select-targeting.png){width=85%}

1. 규칙 빌더를 사용하여 기준을 정의합니다. 예를 들어 미국 거주자를 위한 규칙, 프랑스 거주자를 위한 규칙, 인도 거주자를 위한 규칙을 정의합니다.

   ![](assets/msg-optimization-create-targeting.png){width=85%}

1. 필요에 따라 **[!UICONTROL 대체 콘텐츠 사용]**&#x200B;을 선택합니다. 대체 콘텐츠 를 사용하면 타깃팅 규칙이 적격하지 않을 때 대상자가 기본 콘텐츠를 받을 수 있습니다.

   >[!NOTE]
   >
   >이 옵션을 선택하지 않으면 위에서 정의한 타겟팅 규칙에 적합하지 않은 모든 대상자는 컨텐츠를 받지 않습니다.

1. 타깃팅 규칙 설정을 저장합니다.

1. **[!UICONTROL 작업]** 탭으로 돌아가 **[!UICONTROL 콘텐츠 편집]**&#x200B;을 선택합니다.

1. 타겟팅 규칙 설정으로 정의된 각 그룹에 적절한 콘텐츠를 디자인할 수 있습니다.

   ![](assets/msg-optimization-targeting-design.png){width=85%}

   이 예제에서는 미국 거주자를 위한 특정 콘텐츠, 프랑스 거주자를 위한 다른 콘텐츠 및 인도 거주자를 위한 다른 콘텐츠를 디자인합니다.

1. 여정 또는 캠페인을 [활성화](review-activate-campaign.md)합니다.

여정/캠페인이 라이브되면 미국 거주자는 특정 메시지를, 프랑스 거주자는 다른 메시지를 얻을 수 있도록 타겟팅한 각 콘텐츠에 맞는 콘텐츠가 전송됩니다.

<!--Default content:

* If no targeting rules match, default content can be delivered.

* If default content is not enabled, passthrough behavior ensures lower-priority campaigns are evaluated.-->

## 실험 사용 {#experimentation}

실험을 통해 여러 버전의 콘텐츠를 테스트하여 사전 정의된 성공 지표를 기반으로 가장 뛰어난 성과를 확인할 수 있습니다.

실험을 설정하려면 아래 단계를 따르십시오.

캠페인에서 다음 프로모션 메시지를 테스트한다고 가정해 보겠습니다.

* **처리 A**: &quot;다음 구매 시 20% 할인&quot;
* **처리 B**: &quot;50달러 이상 주문에 대해 무료 배송&quot;
* **처리 C**: &quot;10달러 기프트 카드 받기&quot;

실험을 설정하고 가장 많은 구매를 유도하는 메시지를 확인하려면 아래 단계를 따르십시오.

1. [여정](../building-journeys/journey-gs.md#jo-build) 또는 [캠페인](../campaigns/create-campaign.md)을 만듭니다.

   >[!NOTE]
   >
   >여정에 있는 경우 **[!UICONTROL 작업]** 활동을 추가하고 채널 활동을 선택한 다음 **[!UICONTROL 작업 구성]**&#x200B;을 선택하십시오. [자세히 알아보기](../building-journeys/journey-action.md#add-action)

1. **[!UICONTROL 작업]** 탭에서 [코드 기반 경험](../code-based/get-started-code-based.md) 및 [인앱](../../rp_landing_pages/in-app-landing-page.md)과 같은 두 개 이상의 인바운드 작업을 선택하십시오.

1. **[!UICONTROL 최적화]** 섹션에서 **[!UICONTROL 실험 만들기]**&#x200B;를 선택합니다.

   ![](assets/msg-optimization-select-experiment.png){width=85%}

1. 콘텐츠 실험을 원하는 대로 디자인하고 구성합니다. [방법 알아보기](../content-management/content-experiment.md)

   ![](assets/msg-optimization-create-experiment.png){width=85%}

   실험이 정의되면 해당 캠페인이나 여정 **[!UICONTROL Action]** 활동을 통해 삽입된 모든 작업에 적용됩니다. 즉, 동일한 고객이 모든 표면에 걸쳐 동일한 오퍼를 표시함을 의미합니다.

   >[!NOTE]
   >
   >다른 작업을 선택할 수 있습니다. 실험은 캠페인 또는 여정 작업에 추가된 모든 작업에 적용됩니다.

1. 여정 또는 캠페인을 [활성화](review-activate-campaign.md)합니다.

여정/캠페인이 라이브되면 사용자에게 다양한 콘텐츠 변형이 무작위로 할당됩니다. [!DNL Journey Optimizer]은(는) 더 많은 구매를 유도하는 변형을 추적하고 실행 가능한 통찰력을 제공합니다.

[여정](../reports/journey-global-report-cja.md) 및 [캠페인](../reports/campaign-global-report-cja-experimentation.md) 보고서를 통해 캠페인의 성공을 추적하세요. <!--Link to Experimentation journey reportis missing-->

## 타깃팅과 실험 결합 {#combination}

또한 Journey Optimizer을 사용하면 단일 여정 또는 캠페인 내에 타기팅과 실험을 결합하여 보다 정교한 전략을 만들 수 있습니다.

실제로 타깃팅을 사용하여 여러 변형을 만들 수 있으며, 각 변형에 대해 실험을 사용하여 각 콘텐츠를 추가로 최적화할 수 있습니다. 이렇게 하면 실험이 각 타깃팅 규칙에 특정되고 변형에 걸쳐 있지 않게 됩니다.

예를 들어 미국의 고객을 위해 &#39;50% 할인 프로모션&#39;과 &#39;50$ 기프트 카드&#39;를 테스트하고, 유럽의 고객을 위해 &#39;€50 이상 주문에 대한 무료 배송&#39; 및 &#39;다음 구매 시 20% 할인&#39;과 같은 다른 테스트를 실행할 수 있습니다.

여정 또는 캠페인에서 타겟팅과 실험을 모두 결합하려면 아래 단계를 따르십시오.

1. 여러 타겟팅 규칙을 정의하는 여정 또는 캠페인을 만듭니다. [방법 알아보기](#targeting)

   ![](assets/msg-optimization-create-targeting.png){width=85%}

1. 첫 번째 타겟팅 규칙에 대한 실험을 만듭니다.

1. 콘텐츠 실험을 원하는 대로 디자인하고 구성합니다. [방법 알아보기](../content-management/content-experiment.md)

   ![](assets/msg-optimization-targeting-with-experiment.png){width=85%}

   실험이 정의되면 첫 번째 타겟팅 규칙에만 적용됩니다.

1. **[!UICONTROL 작업]** 탭으로 돌아가 **[!UICONTROL 콘텐츠 편집]**&#x200B;을 선택합니다.

1. 첫 번째 타겟팅 규칙으로 정의된 그룹의 경우 실험의 각 변형에 대해 특정 콘텐츠를 정의할 수 있습니다.

   여정 또는 캠페인에 두 개 이상의 인바운드 작업을 추가한 경우 각 작업에 동일한 타기팅 및 실험 조합이 적용됩니다. 하지만 각 작업의 각 변형에 대해 특정 콘텐츠를 정의해야 합니다.

   ![](assets/msg-optimization-targeting-experiment-design.png){width=85%}

1. 다른 타겟팅 규칙에 대해서도 유사하게 진행하고 각 변형에 대해 해당 콘텐츠를 디자인합니다.

1. 변경 내용을 저장하고 여정 또는 캠페인을 [활성화](review-activate-campaign.md)합니다.

여정/캠페인이 라이브되면 타겟팅된 각 그룹의 사용자는 자신이 속한 그룹에 대해 정의된 다른 콘텐츠 변형이 임의로 할당됩니다.

<!--
## Reporting on Message optimization

E.g. explaining how a marketer can look at the report to determine which treatment (e.g. which message content) is performing the best for the targeting audience
-->

## 사용 방법 비디오{#video}

작업 또는 API 트리거 캠페인에서 메시지 최적화를 활용하는 방법을 알아봅니다. 하위 대상자를 타기팅하고, 위치별 메시지 베리에이션을 만들고, 대체 콘텐츠를 활성화하고, 단일 캠페인 내에서 여러 실험을 실행하는 방법을 알 수 있습니다. 이 튜토리얼에서는 메시지 일관성을 유지하면서 멀티채널 캠페인을 관리하는 방법도 다룹니다.

>[!VIDEO](https://video.tv.adobe.com/v/3470375?quality=12&captions=kor)