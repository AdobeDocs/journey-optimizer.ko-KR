---
title: 순위 지정 방법
description: 등급 메서드를 사용하여 작업하는 방법을 알아봅니다.
feature: Decisioning, Ranking
topic: Integrations
role: User
level: Intermediate
exl-id: c1d69bc9-4486-4037-b218-f4f704b2ba9c
source-git-commit: 58f4fdf8ec3cdb609efebf5b8713f6b770ef5414
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 16%

---

# 순위 지정 방법 {#rankings}

등급 지정 방법을 사용하면 특정 프로필에 표시할 항목의 등급을 지정할 수 있습니다. 순위 지정 방법이 생성되면 이를 선택 전략에 할당하여 먼저 선택해야 하는 항목을 정의할 수 있습니다.

두 가지 유형의 순위 방법을 사용할 수 있습니다.

* **수식**&#x200B;을 사용하면 항목의 우선 순위 점수를 고려하지 않고 먼저 표시할 항목을 결정하는 규칙을 정의할 수 있습니다.

* **AI 모델**&#x200B;을 사용하면 여러 데이터 포인트를 활용하는 훈련된 모델 시스템을 사용하여 먼저 표시할 항목을 결정할 수 있습니다.

## 순위 방법 만들기 {#create}

등급 방법을 만들려면 다음 단계를 수행합니다.

1. **[!UICONTROL 전략 설정]** 메뉴로 이동한 다음 사용할 순위 유형에 따라 **[!UICONTROL 공식]** 또는 **[!UICONTROL AI 모델]** 메뉴를 선택하십시오.

   ![](../assets/ranking-create.png)

1. 화면 오른쪽 상단의 **[!UICONTROL 수식 만들기]** 또는 **[!UICONTROL AI 모델 만들기]** 단추를 클릭합니다.

   등급 수식 및 AI 모델을 만드는 방법에 대한 자세한 내용은 다음 섹션에서 확인할 수 있습니다.

   * [순위 공식](ranking-formulas.md)
   * [AI 모델](ai-models.md)

1. 필요에 따라 수식 또는 AI 모델을 구성한 다음 저장합니다.

이제 [선택 전략](../selection-strategies.md)에서 순위 지정 방법을 사용하여 적격한 결정 항목의 등급을 지정할 준비가 되었습니다.


