---
solution: Journey Optimizer
product: journey optimizer
title: 고급 표현식 편집기 작업
description: 고급 표현식을 작성하는 방법에 대해 알아보기
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: 표현식 편집기, 데이터, 여정
exl-id: 9ea6cc3a-6a1b-4e8f-82ff-f8b1812617d7
source-git-commit: b69023669b6ca59ea5980b1a671a90c41eb665fb
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 55%

---

# 고급 표현식 편집기 작업 {#about-the-advanced-expression-editor}

>[!CONTEXTUALHELP]
>id="ajo_journey_expression_advanced"
>title="고급 표현식 편집기 정보"
>abstract="고급 표현식 편집기를 사용하여 다양한 인터페이스 화면에서 고급 표현식을 작성합니다. 예를 들어 여정을 구성 및 사용할 때와 데이터 원본 조건을 정의할 때 표현식을 작성할 수 있습니다."

여정 고급 표현식 편집기를 사용하여 인터페이스의 다양한 화면에서 고급 표현식을 작성합니다. 예를 들어 여정을 구성 및 사용할 때와 데이터 원본 조건을 정의할 때 표현식을 작성할 수 있습니다.

특정 데이터 조작이 필요한 작업 매개 변수를 정의해야 할 때마다 고급 표현식 편집기를 사용할 수도 있습니다. 이벤트로부터 얻은 데이터 또는 데이터 소스에서 검색된 추가 정보를 활용할 수 있습니다. 여정에서는 상황에 맞는 이벤트 필드 목록이 표시되며, 이 목록은 여정에 추가된 이벤트에 따라 달라집니다.

![](../assets/journey65.png)


고급 표현식 편집기는 값을 조작하고 필요에 맞는 표현식을 정의할 수 있는 함수 및 연산자를 기본 제공합니다. 고급 표현식 편집기를 사용하면 외부 데이터 소스 매개 변수의 값을 정의하고, 맵 필드와 컬렉션을 조작할 수도 있습니다.

>[!NOTE]
>
>여정 고급 표현식 편집기에서 사용할 수 있는 기능 및 기능은 [개인화 편집기](../../personalization/functions/functions.md)에서 사용할 수 있는 기능 및 기능과 다릅니다.

## 고급 표현식 편집기 액세스 {#accessing-the-advanced-expression-editor}

고급 표현식 편집기를 사용하여 다음을 수행할 수 있습니다.

* 데이터 소스 및 이벤트 정보에 대한 [고급 조건](../condition-activity.md#about_condition) 만들기
* 사용자 지정 [대기 활동](../wait-activity.md#custom) 정의
* 작업 매개 변수 매핑 정의

가능한 경우 **[!UICONTROL 고급 모드]** / **[!UICONTROL 단순 모드]** 단추를 사용하여 두 모드 간을 전환할 수 있습니다. 단순 모드는 [여기](../condition-activity.md#about_condition)에 설명되어 있습니다.

>[!NOTE]
>
>* 조건은 단순 또는 고급 표현식 편집기에서 정의할 수 있으며, 항상 부울 형식을 반환합니다.
>
>* 작업 매개 변수는 필드를 선택하여 정의하거나 고급 표현식 편집기를 통해 정의할 수 있으며, 표현식에 따라 특정 데이터 형식을 반환합니다.

다양한 방법으로 고급 표현식 편집기에 액세스할 수 있습니다.

* 데이터 원본 조건을 만들 때 **[!UICONTROL 고급 모드]**&#x200B;를 클릭하여 고급 편집기에 액세스할 수 있습니다.

  ![](../assets/journeyuc2_33.png)

* 사용자 지정 타이머를 만들 때 고급 편집기가 바로 나타납니다.
* 작업 매개 변수를 매핑할 때 **[!UICONTROL 고급 모드]**&#x200B;를 클릭합니다.

## 인터페이스 살펴보기 {#discovering-the-interface}

이 화면에서 표현식을 직접 작성할 수 있습니다.

![](../assets/journey70.png)

화면 왼쪽에 사용 가능한 필드와 함수가 표시됩니다.

* **[!UICONTROL 이벤트]**: 인바운드 이벤트에서 받은 필드 중 하나를 선택하십시오. 상황에 맞는 이벤트 필드 목록이 표시되며, 이 목록은 여정에 추가된 이벤트에 따라 달라집니다. [자세히 보기](../../event/about-events.md)

  >[!CAUTION]
  >
  >경험 이벤트를 사용하여 표현식을 만들 수 없습니다. 경험 이벤트를 사용하여 표현식/논리를 만드는 다른 방법 및 모범 사례가 [여기](../../building-journeys/exp-event-lookup.md)에서 참조됩니다.

* **[!UICONTROL 대상]**: **[!UICONTROL 대상 자격]** 이벤트를 삭제한 경우 표현식에 사용할 대상을 선택하십시오. [자세히 보기](../condition-activity.md#using-a-segment)
* **[!UICONTROL 데이터 원본]**: 데이터 원본의 필드 그룹에서 사용 가능한 필드 목록에서 선택하십시오. [자세히 보기](../../datasource/about-data-sources.md)
* **[!UICONTROL 여정 속성]**: 이 섹션에서는 지정된 프로필의 여정과 관련된 기술 필드를 다시 그룹화합니다. [자세히 보기](journey-properties.md)
* **[!UICONTROL 함수]**: 복잡한 필터링을 수행할 수 있는 기본 함수 목록 중에서 선택합니다. 함수는 카테고리별로 구성됩니다. [자세히 보기](functions.md)

![](../assets/journey65.png)

자동 완성 메커니즘이 상황에 맞는 제안을 표시합니다.

![](../assets/journey68.png)

구문 유효성 검사 메커니즘이 코드의 무결성을 확인합니다. 편집기 맨 위에 오류가 표시됩니다.

![](../assets/journey69.png)


>[!TIP]
>
>고급 표현식 편집기에서 조건을 만들 때는 표현식에 숨겨진 문자나 인쇄할 수 없는 문자가 포함되지 않아야 합니다. 또한 구문 분석 오류를 방지하려면 한 줄 식을 사용하십시오.


**고급 표현식 편집기를 사용하여 조건을 작성할 때의 매개 변수 필요성**

매개 변수를 호출해야 하는 외부 데이터 원본에서 필드를 선택하는 경우([이 페이지](../../datasource/external-data-sources.md) 참조), 이 매개 변수를 지정할 수 있도록 오른쪽에 새 탭이 나타납니다. 매개 변수 값은 여정 또는 Experience Platform 데이터 소스에 있는 이벤트에서 가져올 수 있으며 다른 외부 데이터 소스에서 가져올 수 없습니다. 예를 들어 날씨 관련 데이터 소스에서 자주 사용되는 매개 변수는 &quot;city&quot;입니다. 따라서 이 city 매개 변수를 가져올 위치를 선택해야 합니다. 매개 변수에 함수를 적용하여 형식 변경 또는 연결을 수행할 수도 있습니다.

![](../assets/journeyuc2_19.png)

보다 복잡한 사용 사례에서는 기본 표현식에 데이터 소스의 매개 변수를 포함하려는 경우 &quot;params&quot; 키워드를 사용하여 해당 값을 정의할 수 있습니다. [이 페이지](../expression/field-references.md)를 참조하십시오.
