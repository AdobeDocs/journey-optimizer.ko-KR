---
product: experience platform
solution: Experience Platform
title: AI 모델 시작
description: 오퍼의 등급을 매길 수 있는 AI 모델에 대해 알아봅니다
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 4f7f7d1d-a12a-4ff6-b0ff-1a1c3d305a9d
source-git-commit: 3188bc97b8103d2a01101a23d8c242a3e2924f76
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 4%

---

# AI 모델 시작 {#ai-models}

[!DNL Journey Optimizer] 지정된 프로필에 대해 표시할 오퍼에 등급을 지정하는 숙련된 모델 시스템을 사용할 수 있습니다.

이 기능을 사용하면 다른 기능을 만들 수 있습니다 **AI 모델** 비즈니스 목표를 기반으로 구축 이러한 다양한 목표 기반 전략을 의사 결정에 사용하면 숙련된 모델 시스템을 통해 다양한 AI 모델이 목표에 미치는 영향을 파악할 수 있습니다.

예를 들어 이메일 채널에 대한 AI 모델과 푸시 채널에 대한 다른 모델을 선택할 수 있습니다. 각 채널에 대해, 훈련된 모델 시스템은 여러 데이터 포인트를 활용하여 오퍼의 우선 순위 점수나 오퍼를 고려하지 않고 지정된 배치에 대해 먼저 제공해야 하는 오퍼를 결정합니다 [등급 공식](create-ranking-formulas.md).

## AI 모델 유형 {#ai-model-types}

에서는 두 가지 유형의 AI 모델을 사용할 수 있습니다 [!DNL Journey Optimizer]:

* **자동 최적화 모델** 비즈니스 클라이언트가 설정한 반환(KPI)을 극대화하는 오퍼를 제공하는 것을 목표로 합니다. 이러한 KPI는 전환율, 매출 등의 유형일 수 있습니다. 이때 자동 최적화는 오퍼를 Adobe Target으로 전환하여 오퍼 클릭 최적화에 중점을 둡니다. 자동 최적화는 오퍼의 &quot;전역&quot; 성능을 기반으로 개인화되지 않고 최적화합니다. [자세히 보기](auto-optimization-model.md)

* **개인화 모델** 을(를) 통해 비즈니스 목표를 정의하고 고객 데이터를 활용하여 비즈니스 중심 모델을 교육하여 개인화된 오퍼를 제공하고 KPI를 극대화할 수 있습니다. [자세히 보기](personalized-optimization-model.md)

>[!CAUTION]
>
>현재 개인화된 최적화 모델을 사용하면 사용자를 선택하기만 하면 조기 액세스에서 사용할 수 있습니다.

## AI 모델 만들기 {#create-ai-model}

AI 모델을 만들고 사용하는 주요 단계는 다음과 같습니다.

1. 전환 및 노출 이벤트를 수집할 데이터 세트를 만듭니다. [자세히 보기](create-dataset.md)
1. 데이터 세트의 이벤트를 활용하여 오퍼의 등급을 매기는 AI 모델을 만듭니다. [자세히 보기](create-ranking-strategies.md)
1. 이벤트를 자동으로 캡처하도록 오퍼 스키마를 구성합니다. [자세히 보기](schema-requirement.md)
1. 적합한 오퍼의 등급을 지정하도록 결정에서 배치에 AI 모델을 지정합니다. [자세히 보기](../offer-activities/configure-offer-selection.md)
