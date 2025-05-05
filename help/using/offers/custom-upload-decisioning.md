---
title: 의사 결정을 위해 사용자 정의 업로드 대상 활용
description: 의사 결정을 위해 사용자 지정 업로드 대상자를 활용하는 방법을 알아봅니다.
feature: Decision Management
role: User
level: Intermediate
source-git-commit: 1e46321de543196277613889c438dc6756e45652
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---


# 의사 결정을 위해 사용자 정의 업로드 대상 활용 {#custom-upload-decisioning}

Journey Optimizer을 사용하면 Adobe Experience Platform으로의 사용자 지정 업로드(CSV 파일)를 사용하여 만든 대상의 데이터를 활용하여 의사 결정 관리 워크플로우를 지원할 수 있습니다. 이 기능은 프로필에 데이터가 필요하지 않지만 의사 결정 목적으로 여전히 필수인 경우에 특히 유용합니다.

사용자 지정 업로드 대상자의 데이터는 의사 결정 관리에서 다음에 사용할 수 있습니다.

1. 오퍼 및 의사 결정의 자격 기준.
2. 오퍼 표시에서 컨텐츠 개인화.

사용자 지정 업로드 대상자에 대한 자세한 내용은 다음 섹션을 참조하십시오.
* [대상자 및 Journey Optimizer 시작](../audience/about-audiences.md)
* [Adobe Experience Platform에서 대상 가져오기](https://experienceleague.adobe.com/ko/docs/experience-platform/segmentation/ui/audience-portal#import-audience){target="_blank"}

## 반드시 알아야 할 사항 {#must-read}

* 이 기능은 Decisioning(이전의 &quot;Experience Decisioning&quot;)이 아닌 **의사 결정 관리**&#x200B;에서만 지원됩니다.
* **Decisioning API(허브)** 요청을 통해서만 사용할 수 있으며 **Edge Decisioning API** 또는 **batch decisioning**&#x200B;에서 지원하지 않습니다.
 

## 사용자 정의 업로드 대상자를 자격 기준으로 사용 {#eligibilty}

사용자 지정 업로드 대상을 오퍼 또는 의사 결정 수준 모두에서 자격 기준으로 사용할 수 있습니다. 이 기준을 추가하면 해당 기준에서 오퍼 또는 오퍼 컬렉션을 적격성에서 제외할 수 있습니다. 다음은 사용자 지정 업로드 대상을 활용하여 오퍼 및 결정 자격을 세분화할 수 있는 다양한 위치입니다.

* 사용자 지정 업로드 대상자를 사용하여 의사 결정 규칙 만들기:

   1. 규칙을 작성할 때 **대상** 탭에 액세스하여 목록에서 CSV 대상을 검색합니다. 대상을 규칙 캔버스로 드래그하여 놓습니다.
   1. **특성** 탭을 사용하고 선택한 대상자에 연결된 데이터 보강 스키마로 이동하여 CSV 파일의 모든 데이터에 액세스하고 규칙에서 사용하십시오. 이렇게 하면 CSV 파일의 필드를 사용하여 규칙을 세분화할 수 있습니다. [의사 결정 규칙을 만드는 방법을 알아봅니다](../offers/offer-library/creating-decision-rules.md)
   1. 규칙을 저장합니다. 규칙이 만들어지면 오퍼 및 의사 결정 수준 모두에서 해당 규칙을 사용하여 자격 조건을 구체화할 수 있습니다.

  ![](assets/csv-rule.png)

* 사용자 지정 업로드 대상을 오퍼 제한 사항으로 사용합니다. [오퍼에 제약 조건을 추가하는 방법 알아보기](../offers/offer-library/add-constraints.md)

  오퍼를 작성할 때 **제약 조건 추가** 단계에서 다음 중 하나를 수행할 수 있습니다.

   * 사용자 정의 업로드 대상자를 사용하여 오퍼 자격 조건을 정의합니다.
   * 사용자 지정 업로드 대상을 활용하는 규칙을 적용합니다.

  ![](assets/csv-offer.png)

* 의사 결정 수준에서 사용자 지정 업로드 대상을 사용합니다.

  결정을 설정할 때 **결정 범위 추가** 단계에서 사용자 지정 업로드 대상을 오퍼 컬렉션에 대한 평가 기준으로 사용할 수 있습니다. [결정 범위를 정의하는 방법 알아보기](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)

  ![](assets/csv-decision.png)

## 사용자 정의 업로드 대상자를 사용하여 오퍼 표시 개인화

사용자 지정 업로드 대상을 사용하여 CSV 파일의 데이터를 참조하여 오퍼 표시 콘텐츠를 개인화할 수도 있습니다. [오퍼에 표시를 추가하는 방법을 알아봅니다](../offers/offer-library/add-representations.md)

개인화에 사용자 지정 업로드 대상자의 속성을 활용하려면 먼저 사용자 지정 대상자를 제한 사항으로 추가해야 합니다. 이렇게 하려면 오퍼를 작성하는 동안 **제약 조건 추가** 단계에서 대상을 제약 조건으로 추가하거나 사용자 지정 업로드 대상을 활용하는 규칙을 선택합니다.

![](assets/csv-offer.png)

대상자가 제약으로 추가되면 해당 속성을 사용하여 표현 콘텐츠를 개인화할 수 있습니다. 이렇게 하려면 **프로필 특성** 탭에 액세스하여 사용자 지정 업로드 대상자를 검색합니다. 대상자에서 관련 속성을 선택하여 오퍼 콘텐츠를 개인화합니다.

![](assets/csv-perso.png)
