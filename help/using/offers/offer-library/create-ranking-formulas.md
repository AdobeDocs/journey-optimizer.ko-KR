---
title: 등급 수식 만들기
description: Adobe Experience Platform에서 등급 공식을 만드는 방법을 알아봅니다.
source-git-commit: ea8a3644ecef911a14ea087b03d367976f0c898d
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 등급 수식 만들기 {#create-ranking-formulas}

## 등급 공식 정보 {#about-ranking-formulas}

**등급** 공식 을 사용하면 오퍼의 우선순위 점수를 고려하지 않고, 주어진 배치에 대해 먼저 제시해야 하는 오퍼를 결정하는 규칙을 정의할 수 있습니다.

등급 공식은 **PQL 구문**&#x200B;에 표시되며 프로필 속성, 컨텍스트 데이터 및 오퍼 속성을 활용할 수 있습니다. PQL 구문 사용 방법에 대한 자세한 내용은 [전용 설명서](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html)를 참조하십시오.

등급 공식이 만들어지면 결정(이전에 오퍼 활동이라고 함)의 배치에 할당할 수 있습니다. 자세한 내용은 결정](../offer-activities/configure-offer-selection.md)에서 [오퍼 선택 구성 을 참조하십시오.

## 등급 공식 {#create-ranking-formula} 만들기

등급 공식을 만들려면 아래 단계를 수행하십시오.

1. **[!UICONTROL Components]** 메뉴에 액세스한 다음 **[!UICONTROL Rankings]** 탭을 선택합니다. 이전에 만든 등급 목록이 표시됩니다.

   ![](../../assets/rankings-list.png)

1. **[!UICONTROL Create ranking]** 을 클릭하여 새 등급 공식을 만듭니다.

   ![](../../assets/ranking-create-formula.png)

1. 순위 공식 이름, 설명 및 공식을 지정합니다.

   이 예에서는 실제 날씨가 더운 경우 &quot;핫&quot; 속성을 사용하여 모든 오퍼의 우선 순위를 늘리려고 합니다. 이를 위해 **contextData.weather=hot**&#x200B;이(가) 의사 결정 호출에서 전달되었습니다.

   ![](../../assets/ranking-syntax.png)

1. **[!UICONTROL Save]**&#x200B;을 클릭합니다. 등급 공식이 생성되면 목록에서 선택하여 세부 정보를 얻고 편집하거나 삭제할 수 있습니다.

   이제 배치에 적합한 오퍼의 등급을 매기는 결정에 사용할 준비가 되었습니다([결정](../offer-activities/configure-offer-selection.md)에서 오퍼 선택 구성 참조).

   ![](../../assets/ranking-formula-created.png)
