---
solution: Journey Optimizer
product: journey optimizer
title: 타깃팅과 실험 결합
description: 단일 여정 또는 캠페인 내에서 타기팅과 실험을 결합하여 정교한 최적화 전략을 만드는 방법을 알아봅니다.
role: User
level: Intermediate
keywords: 최적화, 타기팅, 실험, 조합, 고급
source-git-commit: 27de3d2171e6f6575eb66ada20f951f6cb3abc98
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 1%

---

# 타깃팅과 실험 결합 {#combination}

또한 Journey Optimizer을 사용하면 단일 여정 또는 캠페인 내에 타기팅과 실험을 결합하여 보다 정교한 전략을 만들 수 있습니다.

실제로 타깃팅을 사용하여 여러 변형을 만들 수 있으며, 각 변형에 대해 실험을 사용하여 각 콘텐츠를 추가로 최적화할 수 있습니다. 이렇게 하면 실험이 각 타깃팅 규칙에 특정되고 변형에 걸쳐 있지 않게 됩니다.

예를 들어 미국의 고객을 위해 &#39;50% 할인 프로모션&#39;과 &#39;50$ 기프트 카드&#39;를 테스트하고, 유럽의 고객을 위해 &#39;€50 이상 주문에 대한 무료 배송&#39; 및 &#39;다음 구매 시 20% 할인&#39;과 같은 다른 테스트를 실행할 수 있습니다.

여정 또는 캠페인에서 타겟팅과 실험을 모두 결합하려면 아래 단계를 따르십시오.

1. 여러 타겟팅 규칙을 정의하는 여정 또는 캠페인을 만듭니다. [방법 알아보기](optimization-targeting.md)

   ![](../campaigns/assets/msg-optimization-create-targeting.png){width=85%}

1. 첫 번째 타겟팅 규칙에 대한 실험을 만듭니다.

1. 콘텐츠 실험을 원하는 대로 디자인하고 구성합니다. [방법 알아보기](../content-management/content-experiment.md)

   ![](../campaigns/assets/msg-optimization-targeting-with-experiment.png){width=85%}

   실험이 정의되면 첫 번째 타겟팅 규칙에만 적용됩니다.

1. **[!UICONTROL 작업]** 탭으로 돌아가 **[!UICONTROL 콘텐츠 편집]**&#x200B;을 선택합니다.

1. 첫 번째 타겟팅 규칙으로 정의된 그룹의 경우 실험의 각 변형에 대해 특정 콘텐츠를 정의할 수 있습니다.

   여정 또는 캠페인에 두 개 이상의 인바운드 작업을 추가한 경우 각 작업에 동일한 타기팅 및 실험 조합이 적용됩니다. 하지만 각 작업의 각 변형에 대해 특정 콘텐츠를 정의해야 합니다.

   ![](../campaigns/assets/msg-optimization-targeting-experiment-design.png){width=85%}

1. 다른 타겟팅 규칙에 대해서도 유사하게 진행하고 각 변형에 대해 해당 콘텐츠를 디자인합니다.

1. 변경 내용을 저장하고 여정 또는 캠페인을 [활성화](review-activate-campaign.md)합니다.

여정/캠페인이 라이브되면 타겟팅된 각 그룹의 사용자는 자신이 속한 그룹에 대해 정의된 다른 콘텐츠 변형이 임의로 할당됩니다.

<!--
## Reporting on Message optimization

E.g. explaining how a marketer can look at the report to determine which treatment (e.g. which message content) is performing the best for the targeting audience
-->

