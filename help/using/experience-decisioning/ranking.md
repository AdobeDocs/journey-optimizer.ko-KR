---
title: 순위 지정 방법
description: 등급 메서드를 사용하여 작업하는 방법을 알아봅니다.
feature: Experience Decisioning, Ranking
topic: Integrations
role: User
level: Intermediate
exl-id: c1d69bc9-4486-4037-b218-f4f704b2ba9c
source-git-commit: 22eae783ec2a7db2209b2a12b78b286e4f97ee1b
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 15%

---

# 순위 지정 방법 {#rankings}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_formulas"
>title="순위 공식 만들기"
>abstract="수식으로 먼저 제시할 항목을 결정하는 규칙을 정의할 수 있습니다. 이 경우 항목의 우선 순위 점수를 고려할 필요가 없습니다. 순위 지정 방법이 생성되면 이를 선택 전략에 할당하여 먼저 선택해야 하는 항목을 정의할 수 있습니다."

등급 지정 방법을 사용하면 특정 프로필에 표시할 항목의 등급을 지정할 수 있습니다. 순위 지정 방법이 생성되면 이를 선택 전략에 할당하여 먼저 선택해야 하는 항목을 정의할 수 있습니다.

두 가지 유형의 순위 방법을 사용할 수 있습니다.

* **수식**&#x200B;을 사용하면 항목의 우선 순위 점수를 고려하지 않고 먼저 표시할 항목을 결정하는 규칙을 정의할 수 있습니다.

* **AI 모델**&#x200B;을 사용하면 여러 데이터 포인트를 활용하는 훈련된 모델 시스템을 사용하여 먼저 표시할 항목을 결정할 수 있습니다.

## 등급 메서드 만들기 {#create}

등급 방법을 만들려면 다음 단계를 수행합니다.

1. **[!UICONTROL 전략 설정]** 메뉴로 이동한 다음 사용할 순위 유형에 따라 **[!UICONTROL 공식]** 또는 **[!UICONTROL AI 모델]** 메뉴를 선택하십시오.

1. 화면 오른쪽 상단의 **[!UICONTROL 수식 만들기]** 또는 **[!UICONTROL AI 모델 만들기]** 단추를 클릭합니다.

   ![](assets/ranking-create.png)

1. 필요에 맞게 공식 또는 AI 모델을 구성한 다음 저장합니다.

   등급 수식 및 AI 모델을 만드는 방법에 대한 자세한 내용은 의사 결정 관리 문서에서 확인할 수 있습니다.

   * [등급 공식](../offers/ranking/create-ranking-formulas.md)
   * [AI 모델](../offers/ranking/ai-models.md)

+++ 사용자 지정 [!DNL Customer Journey Analytics] 지표에 대한 모델 최적화 중

>[!NOTE]
>
>이 기능은 관리자 권한이 있는 [!DNL Customer Journey Analytics] 고객만 사용할 수 있습니다.
>
>시작하기 전에 Journey Optimizer 데이터 세트를 기본 데이터 보기로 내보내기 위해 Customer Journey Analytics과 Journey Optimizer을 통합했는지 확인하십시오. [데이터를 활용하는 방법 알아보기 [!DNL Journey Optmizer] 데이터 입력 [!DNL Customer Journey Analytics]](../reports/cja-ajo.md)

개인화된 최적화 모델은 비즈니스 목표를 정의하고 고객 데이터를 활용하여 비즈니스 지향 모델을 교육하여 개인화된 오퍼를 제공하고 KPI를 극대화할 수 있도록 하는 일종의 AI 모델입니다. 개인화된 AI 모델을 만드는 방법에 대한 자세한 내용은 [의사 결정 관리 설명서](../offers/ranking/personalized-optimization-model.md)를 참조하세요.

기본적으로 개인화된 최적화 모델은 **오퍼 클릭 수**&#x200B;를 최적화 지표로 사용합니다. [!DNL Customer Journey Analytics]을(를) 사용하여 작업하는 경우 [!DNL Decisioning]을(를) 사용하면 사용자 지정 지표를 활용하여 모델을 최적화할 수 있습니다.

이렇게 하려면 개인화된 AI 모델 만들기 화면에 액세스하고 **[!UICONTROL 전환 이벤트]** 드롭다운을 확장합니다. 기본 [!DNL Customer Journey Analytics] [데이터 보기](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/data-views){target="_blank"}의 모든 지표가 목록에 표시됩니다. 모델을 최적화할 지표를 선택한 다음 평소대로 AI 모델 생성을 완료합니다.

![](assets/ai-ranking-custom-metrics.png)

>[!NOTE]
>
>기본적으로 [!DNL Customer Journey Analytics]의 지표는 &quot;마지막 터치&quot; 속성 모델을 사용하며, 이 속성 모델은 전환 전에 가장 최근에 발생하는 접점에 크레딧의 100%를 할당합니다.
>
>속성 모델을 수정할 수 있지만 모든 속성 모델이 AI 모델 최적화에 이상적이지는 않습니다. 모델의 정확도와 성능을 보장하기 위해 최적화 목표에 맞는 속성 모델을 신중하게 선택하는 것이 좋습니다.
>
>사용 가능한 속성 모델 및 사용 지침에 대한 자세한 내용은 [[!DNL Customer Journey Analytics] 설명서](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/component-settings/attribution){target="_blank"}를 참조하세요.

+++

## 공식에서 의사 결정 항목 속성 활용 {#items}

등급 수식은 **PQL 구문**&#x200B;으로 표시되며 프로필 특성, [컨텍스트 데이터](context-data.md) 및 결정 항목과 관련된 특성과 같은 다양한 특성을 활용할 수 있습니다.

수식에서 결정 항목과 관련된 속성을 활용하려면 등급 수식 코드에서 아래 구문을 따라야 합니다. 자세한 내용을 보려면 각 섹션을 확장하십시오.

+++의사 결정 항목 표준 속성 활용

![](assets/formula-attribute.png)

+++

+++의사 결정 항목 사용자 지정 속성 활용

![](assets/formula-attribute-custom.png)

+++
