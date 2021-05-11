---
title: 등급 수식 만들기
description: Adobe Experience Platform에서 등급 공식을 만드는 방법을 알아봅니다.
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 3%

---

# 등급 수식 만들기 {#create-ranking-formulas}

## 등급 공식 정보 {#about-ranking-formulas}

**등급** 공식을 사용하면 오퍼의 우선순위 점수를 고려하지 않고 주어진 배치에 대해 먼저 제시해야 할 오퍼를 결정하는 규칙을 정의할 수 있습니다.

등급 수식은 **PQL 구문**&#x200B;으로 표현되며 프로필 속성, 컨텍스트 데이터 및 오퍼 특성을 활용할 수 있습니다. PQL 구문 사용 방법에 대한 자세한 내용은 [전용 설명서](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html)를 참조하십시오.

등급 공식이 생성되면 결정(이전의 오퍼 활동이라고 함)의 배치에 할당할 수 있습니다. 자세한 내용은 [결정](../offer-activities/configure-offer-selection.md)에서 오퍼 선택 구성을 참조하십시오.

## 등급 공식 {#create-ranking-formula} 만들기

등급 공식을 만들려면 아래 단계를 수행합니다.

* **[!UICONTROL Components]** 메뉴에 액세스한 다음 **[!UICONTROL Rankings]** 탭을 선택합니다.

* **[!UICONTROL Create formula]**&#x200B;을 클릭하여 새 등급 공식을 만듭니다.

   ![](../assets/ranking-create-formula.png)

* 등급 공식 이름, 설명 및 공식을 지정합니다.

   이 예에서는 실제 날씨가 덥다면 &quot;핫&quot; 속성을 사용하여 모든 오퍼의 우선 순위를 높입니다. 이를 위해 의사 결정 호출에서 **contextData.weather=hot**&#x200B;이(가) 전달되었습니다.

   ![](../assets/ranking-syntax.png)

* **[!UICONTROL Save]**&#x200B;을 클릭합니다. 등급 공식이 생성되면 목록에서 선택하여 세부 사항을 가져오고 편집하거나 삭제할 수 있습니다.

   이제 배치에 적합한 오퍼의 등급을 매기는 결정에 사용할 수 있습니다([결정](../offer-activities/configure-offer-selection.md)에서 오퍼 선택 구성 참조).

   ![](../assets/ranking-formula-created.png)
