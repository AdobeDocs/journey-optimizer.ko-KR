---
product: experience platform
solution: Experience Platform
title: AI 모델 시작
description: 오퍼의 등급을 매길 수 있는 AI 모델에 대해 알아봅니다
feature: Ranking, Decision Management
role: User
level: Intermediate
exl-id: 4f7f7d1d-a12a-4ff6-b0ff-1a1c3d305a9d
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 4%

---

# AI 모델 시작 {#ai-models}

[!DNL Journey Optimizer] 에서는 주어진 프로필에 대해 표시할 오퍼에 등급을 지정하는 훈련된 모델 시스템을 사용할 수 있습니다.

이 기능을 사용하면 다른 항목을 만들 수 있습니다 **AI 모델** 비즈니스 목표를 기반으로 합니다. 의사 결정에 이러한 다양한 목표 기반 전략을 사용하면 훈련된 모델 시스템을 통해 다양한 AI 모델이 목표에 미치는 영향을 이해할 수 있습니다.

예를 들어 이메일 채널에 대한 AI 모델과 푸시 채널에 대한 다른 AI 모델을 선택할 수 있습니다. 각 채널에 대해 훈련된 모델 시스템은 오퍼의 우선 순위 점수 또는 을 고려하기보다는 여러 데이터 포인트를 활용하여 주어진 배치에 대해 먼저 제시해야 하는 오퍼를 결정합니다 [순위 공식](create-ranking-formulas.md).

>[!IMPORTANT]
>
>현재 Journey Optimizer 작성 채널에서는 등급 모델이 지원되지 않습니다.

## AI 모델 유형 {#ai-model-types}

에서 두 가지 유형의 AI 모델을 사용할 수 있습니다. [!DNL Journey Optimizer]:

* **자동 최적화 모델** 비즈니스 고객이 설정한 KPI(반환)를 극대화하는 오퍼를 제공하는 것을 목표로 합니다. 이러한 KPI는 전환율, 수익 등의 형태일 수 있습니다. 이 시점에서 자동 최적화는 타겟으로 오퍼 전환을 사용하여 오퍼 클릭을 최적화하는 데 중점을 둡니다. 자동 최적화는 개인화되지 않으며 오퍼의 &quot;전역&quot; 성능을 기반으로 최적화됩니다. [자세히 알아보기](auto-optimization-model.md)

* **개인화된 최적화 모델** 비즈니스 목표를 정의하고 고객 데이터를 활용하여 비즈니스 지향 모델을 교육하여 개인화된 오퍼를 제공하고 KPI를 극대화할 수 있습니다. [자세히 알아보기](personalized-optimization-model.md)

## AI 모델 만들기 {#create-ai-model}

AI 모델을 만들고 사용하는 주요 단계는 다음과 같습니다.

1. 전환 및 노출 이벤트가 수집될 데이터 세트를 만듭니다. [자세히 알아보기](../data-collection/create-dataset.md)

1. 데이터 세트의 이벤트를 활용하여 오퍼의 등급을 매기는 AI 모델을 만듭니다. [자세히 알아보기](create-ranking-strategies.md)

1. 이벤트를 자동으로 캡처하도록 오퍼 스키마를 구성합니다. [자세히 알아보기](../data-collection/schema-requirement.md)

   >[!IMPORTANT]
   >
   >등급 모델을 수집하려면 피드백 이벤트를 경험 이벤트로 전송해야 합니다. [의사 결정 관리 데이터 수집에 대해 자세히 알아보기](../data-collection/data-collection.md)

1. 적격 오퍼의 등급을 지정하기 위한 의사 결정의 배치에 AI 모델을 지정합니다. [자세히 알아보기](../offer-activities/configure-offer-selection.md)
