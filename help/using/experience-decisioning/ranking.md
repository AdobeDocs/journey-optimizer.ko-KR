---
title: 순위 방법
description: 등급 메서드를 사용하여 작업하는 방법을 알아봅니다.
feature: Experience Decisioning, Ranking
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: c1d69bc9-4486-4037-b218-f4f704b2ba9c
source-git-commit: f92e3882d3b5e515e672a4af8e787813d4d939ce
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 62%

---

# 순위 방법 {#rankings}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_formulas"
>title="등급 수식 만들기"
>abstract="수식으로 먼저 제시할 항목을 결정하는 규칙을 정의할 수 있습니다. 이 경우 항목의 우선 순위 점수를 고려할 필요가 없습니다. 순위 지정 방법이 생성되면 이를 결정 전략에 할당하여 먼저 선택해야 하는 항목을 정의할 수 있습니다."

>[!BEGINSHADEBOX]

이 설명서의 내용:

* [Experience Decisioning 시작](gs-experience-decisioning.md)
* 결정 항목 관리
   * [항목 카탈로그 구성](catalogs.md)
   * [결정 항목 만들기](items.md)
   * [항목 컬렉션 관리](collections.md)
* 항목 선택 구성
   * [의사 결정 규칙 만들기](rules.md)
   * **[등급 메서드 만들기](ranking.md)**
* [선택 전략 만들기](selection-strategies.md)
* [결정 정책 만들기](create-decision.md)

>[!ENDSHADEBOX]

등급 지정 방법을 사용하면 특정 프로필에 표시할 항목의 등급을 지정할 수 있습니다. 순위 지정 방법이 생성되면 이를 결정 전략에 할당하여 먼저 선택해야 하는 항목을 정의할 수 있습니다.

등급 메서드는 **[!UICONTROL 구성]** / **[!UICONTROL 순위 방법]** 메뉴 아래의 제품에서 사용할 수 있습니다. 두 가지 유형의 순위 방법을 사용할 수 있습니다.

* **수식으로 먼저 제시할 항목을 결정하는 규칙을 정의할 수 있습니다. 이 경우 항목의 우선 순위 점수를 고려할 필요가 없습니다.**

* **AI 모델** 에서는 여러 데이터 포인트를 활용하는 훈련된 모델 시스템을 사용하여 먼저 제시해야 하는 항목을 결정할 수 있습니다.

![](assets/ranking-create.png)

각 등급 방법 유형과 각 등급 방법을 생성하는 방법에 대한 자세한 내용은 의사 결정 관리 설명서에서 확인할 수 있습니다.

* [등급 공식](../offers/ranking/create-ranking-formulas.md)
* [AI 모델](../offers/ranking/ai-models.md)
