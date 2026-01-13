---
solution: Journey Optimizer
product: journey optimizer
title: 메시지 최적화에 실험 사용
description: 콘텐츠 실험을 사용하여 여러 버전의 콘텐츠를 테스트하고 성과가 가장 좋은 콘텐츠를 결정하는 방법에 대해 알아봅니다.
role: User
level: Intermediate
keywords: 실험, 최적화, A/B 테스트, 콘텐츠 실험, 처리
source-git-commit: f4eb982ba0840acfe336e759fcbf9cfd47b3b98c
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 2%

---

# 실험 사용 {#experimentation}

>[!NOTE]
>
>이 페이지에서는 콘텐츠 최적화 내에서 실험을 사용하는 방법에 대한 개요를 제공합니다. 구성 옵션, 지표 및 분석을 포함한 콘텐츠 실험에 대한 자세한 내용은 [콘텐츠 실험 설명서](../content-management/get-started-experiment.md)를 참조하십시오.

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

1. **[!UICONTROL 작업]** 탭에서 두 개의 인바운드 작업을 선택합니다. 예를 들어 [코드 기반 경험](../code-based/get-started-code-based.md) 및 [인앱](../../rp_landing_pages/in-app-landing-page.md)을 선택합니다.

1. **[!UICONTROL 최적화]** 섹션에서 **[!UICONTROL 실험 만들기]**&#x200B;를 선택합니다.

   ![](../campaigns/assets/msg-optimization-select-experiment.png){width=85%}

1. 콘텐츠 실험을 원하는 대로 디자인하고 구성합니다. [방법 알아보기](../content-management/content-experiment.md)

   ![](../campaigns/assets/msg-optimization-create-experiment.png){width=85%}

   실험이 정의되면 해당 캠페인이나 여정 **[!UICONTROL Action]** 활동을 통해 삽입된 모든 작업에 적용됩니다. 즉, 동일한 고객이 모든 표면에 걸쳐 동일한 오퍼를 표시함을 의미합니다.

   >[!NOTE]
   >
   >다른 동작을 선택할 수 있습니다. 실험은 캠페인이나 여정 [동작 활동](../building-journeys/journey-action.md)에 추가된 모든 동작에 적용됩니다.

1. 여정 또는 캠페인을 [활성화](../campaigns/review-activate-campaign.md)합니다.

여정/캠페인이 라이브되면 사용자에게 다양한 콘텐츠 변형이 무작위로 할당됩니다. [!DNL Journey Optimizer]은(는) 더 많은 구매를 유도하는 변형을 추적하고 실행 가능한 통찰력을 제공합니다.

[여정](../reports/journey-global-report-cja.md) 및 [캠페인](../reports/campaign-global-report-cja-experimentation.md) 보고서를 통해 캠페인의 성공을 추적하세요. <!--Link to Experimentation journey reportis missing-->

