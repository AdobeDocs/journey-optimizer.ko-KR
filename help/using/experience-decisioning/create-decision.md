---
title: 의사 결정 정책 만들기
description: 의사 결정 정책을 만드는 방법 알아보기
feature: Decisioning
topic: Integrations
role: User
level: Experienced
exl-id: 63aa1763-2220-4726-a45d-3a3a8b8a55ec
source-git-commit: baf3a8dba9e83e3b82390bd2ab0725b9fc844138
workflow-type: tm+mt
source-wordcount: '1761'
ht-degree: 10%

---

# 결정 정책 만들기 {#create-decision}

>[!CONTEXTUALHELP]
>id="ajo_code_based_decision"
>title="의사 결정은 무엇입니까?"
>abstract="결정 정책에는 결정 엔진이 최상의 콘텐츠를 선택하기 위한 모든 선택 논리가 포함되어 있습니다. 결정 정책은 캠페인별로 다릅니다. 목표는 각 프로필에 가장 적합한 제안을 선택하는 것이며, 캠페인 작성을 통해서는 메시지에 포함될 항목 속성을 포함하여 선택한 결정 항목이 표시될 방법을 지정할 수 있습니다."
>additional-url="https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="결정 정보"

의사 결정 정책은 대상자에 따라 제공할 최상의 콘텐츠를 선택하기 위해 의사 결정 엔진을 활용하는 오퍼에 대한 컨테이너입니다.

<!--Decision policies contain all of the selection logic for the decisioning engine to pick the best content. Decision policies are campaign specific. -->이 프로필의 목표는 각 프로필에 가장 적합한 오퍼를 선택하는 것이며, 캠페인/여정 작성에서는 메시지에 포함할 항목 속성을 포함하여 선택한 결정 항목을 표시하는 방법을 나타낼 수 있습니다.

>[!NOTE]
>
>[!DNL Journey Optimizer] 사용자 인터페이스에서 결정 정책은 결정<!--but they are decision policies. TBC if this note is needed-->(으)로 레이블이 지정됩니다.

의사 결정 정책을 코드 기반 캠페인에 활용하는 주요 단계는 다음과 같습니다.

1. [코드 기반 환경에 의사 결정 정책 추가](#add-decision)
1. [의사 결정 정책 사용](#use-decision-policy)
1. [사용자 지정 Customer Journey Analytics 보고 대시보드 만들기](cja-reporting.md)

## 코드 기반 환경에 의사 결정 정책 추가 {#add-decision}

>[!CONTEXTUALHELP]
>id="ajo_code_based_item_number"
>title="반환할 항목 수 정의"
>abstract="반환하려는 결정 항목의 수를 선택합니다. 예를 들어 항목 2개를 선택하면 현재 구성에 대한 적격 제안 2개가 표시됩니다."

>[!CONTEXTUALHELP]
>id="ajo_code_based_fallback"
>title="대체 항목 선택"
>abstract="해당 결정 정책에 정의된 선택 전략 중 어느 것도 적합하지 않은 경우 사용자에게 대체 항목이 표시됩니다."

>[!CONTEXTUALHELP]
>id="ajo_code_based_strategy"
>title="전략이란?"
>abstract="선택 전략의 순서에 따라 먼저 평가할 전략을 결정합니다. 적어도 한 개의 전략이 필요합니다. 결합된 전략의 결정 항목을 동시에 평가합니다."
>additional-url="https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="전략 만들기"
>additional-url="https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="평가 순서"

웹 사이트 또는 모바일 앱에서 방문자에게 최고의 동적 오퍼 및 경험을 제공하려면 코드 기반 캠페인 또는 여정에 의사 결정 정책을 추가하십시오. 그 방법은 다음과 같습니다.

### 의사 결정 정책 만들기 {#add}

1. 캠페인을 만들고 **[!UICONTROL 코드 기반 경험]** 작업을 선택하십시오. [자세히 알아보기](../code-based/create-code-based.md)

1. [코드 편집기](../code-based/create-code-based.md#edit-code)에서 **[!UICONTROL 결정 정책]**&#x200B;을 선택하고 **[!UICONTROL 결정 정책 추가]**&#x200B;를 클릭합니다.

   ![](assets/decision-code-based-create.png)

1. 기본적으로 새 정책을 만듭니다.

   >[!NOTE]
   >
   >기존 정책을 선택할 수도 있습니다.

1. 결정 정책에 대한 세부 정보를 입력합니다. 이름을 추가하고 카탈로그를 선택합니다.

   >[!NOTE]
   >
   >현재 기본 **[!UICONTROL 오퍼]** 카탈로그만 사용할 수 있습니다.

1. 반환할 항목 수를 선택합니다. 예를 들어 2를 선택하면 현재 구성에 가장 적합한 2개의 오퍼가 표시됩니다. **[!UICONTROL 다음]**&#x200B;을 클릭합니다.

   ![](assets/decision-code-based-details.png)

### 항목 및 선택 전략 선택 {#select}

**[!UICONTROL 전략 시퀀스]** 섹션에서 결정 정책과 함께 제공할 결정 항목 및 선택 전략을 선택할 수 있습니다.

1. **[!UICONTROL 추가]** 단추를 클릭합니다.

1. 정책에 포함할 개체 유형을 선택합니다.

   * **[!UICONTROL 선택 전략]**: 하나 이상의 선택 전략을 추가합니다. 의사 결정 전략은 자격 제한 및 등급 방법과 관련된 컬렉션을 활용하여 표시할 항목을 결정합니다. 기존 선택 전략을 선택하거나 **[!UICONTROL 선택 전략 만들기]** 단추를 사용하여 새 선택 전략을 만들 수 있습니다. [선택 전략을 만드는 방법을 알아봅니다](selection-strategies.md)

   * **[!UICONTROL 결정 항목]**: 선택 전략을 실행하지 않고도 표시할 단일 결정 항목을 추가하십시오. 한 번에 하나의 결정 항목만 선택할 수 있습니다. 품목에 대해 설정된 모든 자격 제한이 적용됩니다.

   ![](assets/decision-code-based-strategy-sequence.png)

   >[!NOTE]
   >
   >의사 결정 정책은 선택 전략과 의사 결정 항목을 합하여 최대 10개까지 지원한다. [의사 결정 보호 및 제한에 대해 자세히 알아보기](gs-experience-decisioning.md#guardrails)

1. 여러 개의 의사 결정 항목 및/또는 전략을 추가할 때 특정 순서로 평가된다. 시퀀스에 추가된 첫 번째 객체가 먼저 평가됩니다.

   기본 시퀀스를 변경하려면 개체 및/또는 그룹을 드래그하여 놓아 원하는 대로 순서를 변경할 수 있습니다. [자세히 알아보기](#evaluation-order)

### 의사 결정 정책에서 평가 순서 관리 {#evaluation-order}

정책에 결정 항목 및 선택 전략을 추가한 후에는 해당 순서를 정렬하여 평가 순서를 결정하고 선택 전략을 결합하여 함께 평가할 수 있습니다.

항목 및 전략을 평가할 **순차적 순서**&#x200B;은 각 개체 또는 개체 그룹의 왼쪽에 숫자로 표시됩니다. 시퀀스 내에서 선택 전략(또는 전략 그룹)의 위치를 이동하려면 해당 위치를 다른 위치로 끌어다 놓습니다.

>[!NOTE]
>
>선택 전략만 시퀀스 내에서 드래그하여 놓을 수 있습니다. 결정 항목의 위치를 변경하려면 먼저 평가하려는 다른 항목을 추가한 후 **[!UICONTROL 추가]** 단추를 사용하여 결정 항목을 제거하고 다시 추가해야 합니다.

![](assets/decision-code-based-strategy-groups.png)

여러 선택 전략을 그룹으로 **결합**&#x200B;하여 개별적으로 평가되지 않고 함께 평가할 수도 있습니다. 이렇게 하려면 선택 전략 아래의 **`+`** 단추를 클릭하여 다른 단추와 결합하십시오. 선택 전략을 다른 전략에 끌어다 놓아 두 전략을 그룹으로 그룹화할 수도 있습니다.

>[!NOTE]
>
>결정 항목을 다른 항목이나 선택 전략과 함께 그룹화할 수 없습니다.

여러 전략과 해당 그룹화에 따라 전략의 우선 순위와 적격 오퍼의 순위가 결정됩니다. 첫 번째 전략은 우선순위가 가장 높고 동일 그룹 내에서 결합된 전략은 우선순위가 같다.

예를 들어 전략 A와 전략 B에 각각 하나씩, 이렇게 두 개의 컬렉션이 있습니다. 요청은 두 개의 결정 항목이 다시 전송될 수 있도록 하는 것입니다. 전략 A의 2개의 적격 오퍼와 전략 B의 3개의 적격 오퍼가 있다고 가정해 보겠습니다.

* 두 전략이 **결합되지 않음** 또는 순차적 순서(1과 2)인 경우 첫 번째 전략의 상위 2개의 적격 오퍼가 첫 번째 행에 반환됩니다. 첫 번째 전략에 적합한 오퍼가 두 개 없는 경우, 의사 결정 엔진은 계속해서 필요한 만큼 많은 오퍼를 찾기 위해 다음 전략으로 이동하고, 필요한 경우 최종적으로 대체 오퍼를 반환합니다.

  ![](assets/decision-code-based-consecutive-strategies.png)

* 두 컬렉션이 **동시에 평가되는 경우**, 전략 A의 2개 적격 오퍼와 전략 B의 3개 적격 오퍼가 있으므로 5개 오퍼는 모두 각 순위 방법으로 결정된 값을 기준으로 스택됩니다. 2개의 오퍼가 요청되므로 이 5개의 오퍼 중 상위 2개의 적격 오퍼가 반환됩니다.

  ![](assets/decision-code-based-combined-strategies.png)

+++ **여러 전략을 사용하는 예제**

이제 여러 전략을 서로 다른 그룹으로 나눈 예를 살펴보겠습니다.

세 가지 전략을 정의했습니다. 전략 1과 전략 2는 그룹 1에서 함께 결합되고 전략 3은 독립적이다(그룹 2).

각 전략에 대한 적격 오퍼와 해당 우선순위(순위 함수 평가에 사용됨)는 다음과 같습니다.

* 그룹 1:
   * 전략 1 - (오퍼 1, 오퍼 2, 오퍼 3) - 우선순위 1
   * 전략 2 - (오퍼 3, 오퍼 4, 오퍼 5) - 우선순위 1

* 그룹 2:
   * 전략 3 - (오퍼 5, 오퍼 6) - 우선순위 0

우선 순위가 가장 높은 전략 오퍼를 먼저 평가하고 등급 오퍼 목록에 추가합니다.

**반복 1:**

전략 1 및 전략 2 오퍼는 함께 평가됩니다(오퍼 1, 오퍼 2, 오퍼 3, 오퍼 4, 오퍼 5). 그 결과는 다음과 같습니다.

오퍼 1 - 10
오퍼 2 - 20
전략 1에서 오퍼 3 - 30, 전략 2에서 오퍼 45. 둘 중 가장 높은 것을 고려할 것이므로 45를 고려한다.
오퍼 4 - 40
오퍼 5 - 50

이제 등급 오퍼는 다음과 같습니다. 오퍼 5, 오퍼 3, 오퍼 4, 오퍼 2, 오퍼 1.

**반복 2:**

전략 3 오퍼가 평가됩니다(오퍼 5, 오퍼 6). 그 결과는 다음과 같습니다.

* 오퍼 5 - 위의 결과에 이미 있으므로 평가되지 않습니다.
* 오퍼 6 - 60

이제 등급 오퍼는 다음과 같습니다. 오퍼 5 , 오퍼 3, 오퍼 4, 오퍼 2, 오퍼 1, 오퍼 6.

+++

### 대체 오퍼 추가 {#fallback}

결정 항목 및/또는 선택 전략을 선택하면 위의 항목 또는 선택 전략이 모두 충족되지 않는 경우 사용자에게 표시되는 대체 오퍼를 추가할 수 있습니다.

![](assets/decision-code-based-strategy-fallback.png)

현재 샌드박스에서 만든 모든 결정 항목을 표시하는 목록에서 항목을 선택할 수 있습니다. 적합한 선택 전략이 없으면 선택한 항목<!--nor frequency capping when available - TO CLARIFY-->에 적용된 날짜 및 자격 제한에 관계없이 대체 항목이 사용자에게 표시됩니다.

>[!NOTE]
>
>대체 항목은 선택 사항입니다. 대체 항목을 선택하지 않고 적합한 전략이 없으면 [!DNL Journey Optimizer]에서 아무 것도 표시되지 않습니다. 결정 정책에서 요청하는 항목 수를 추가할 수 있습니다. 이렇게 하면 사용 사례에 대해 원할 경우 일정 수의 항목이 반환될 수 있습니다.

결정 정책이 준비되면 저장한 다음 **[!UICONTROL 만들기]**&#x200B;를 클릭합니다. 의사 결정 정책이 만들어졌으므로 이제 코드 기반 경험 콘텐츠 내에서 의사 결정 특성을 사용할 수 있습니다. [자세히 알아보기](#use-decision-policy)

![](assets/decision-code-based-decision-added.png)

## 코드 편집기에서 의사 결정 정책 사용 {#use-decision-policy}

만든 후에는 [개인화 편집기](../code-based/create-code-based.md#edit-code)에서 결정 정책을 사용할 수 있습니다. 그 방법은 다음과 같습니다.

>[!NOTE]
>
>코드 기반 경험은 모든 개인화 및 작성 기능이 있는 [!DNL Journey Optimizer] 개인화 편집기를 활용합니다. [자세히 알아보기](../personalization/personalization-build-expressions.md)

1. **[!UICONTROL 정책 삽입]** 단추를 클릭합니다. 결정 정책에 해당하는 코드가 추가됩니다.

   ![](assets/decision-code-based-add-decision.png)

   >[!NOTE]
   >
   >이 순서는 결정 정책이 반환될 횟수를 반복합니다. 예를 들어 [결정을 만들](#add-decision) 때 다시 2개 항목을 반환하도록 선택한 경우 동일한 시퀀스가 두 번 반복됩니다.

1. 이제 해당 코드 내에 원하는 모든 결정 특성을 추가할 수 있습니다. 사용 가능한 특성은 **[!UICONTROL 오퍼]** 카탈로그의 스키마에 저장됩니다. 사용자 지정 특성은 **`_<imsOrg`>** 폴더에 저장되고 표준 특성은 **`_experience`** 폴더에 저장됩니다. [오퍼 카탈로그의 스키마에 대해 자세히 알아보기](catalogs.md)

   ![](assets/decision-code-based-decision-attributes.png)

   >[!NOTE]
   >
   >결정 정책 항목 추적의 경우 결정 정책 콘텐츠에 대해 `trackingToken` 특성을 다음과 같이 추가해야 합니다.
   >`trackingToken: {{item._experience.decisioning.decisionitem.trackingToken}}`

1. 각 폴더를 클릭하여 확장합니다. 원하는 위치에 마우스 커서를 놓고 추가하려는 속성 옆에 있는 + 아이콘을 클릭합니다. 코드에 원하는 수만큼 속성을 추가할 수 있습니다.

   ![](assets/decision-code-based-add-decision-attributes.png)

1. 프로필 속성과 같이 개인화 편집기에서 사용할 수 있는 다른 속성을 추가할 수도 있습니다.

   ![](assets/decision-code-based-decision-profile-attribute.png)

1. 변경 내용을 확인하려면 **[!UICONTROL 저장 후 닫기]**&#x200B;를 클릭하십시오.

## 코드 기반 경험 테스트 및 게시 {#test-and-publish}

아래 단계에 따라 코드 기반 경험을 완료하고 변경 사항을 라이브로 적용하십시오.

1. 게시하기 전에 코드 기반 경험 미리보기를 표시하여 테스트하십시오.

   >[!CAUTION]
   >
   >현재 [코드 기반 경험](../code-based/create-code-based.md) 캠페인이나 여정에서 의사 결정을 사용하여 사용자 인터페이스의 콘텐츠를 시뮬레이션할 수 없습니다.

   의사 결정을 테스트하기 위해 클라이언트 구현의 XDM 이벤트 `data` 블록에 `dryRun` 플래그를 추가할 수 있습니다.

   ```
   {
   "data": {
       "__adobe": {
       "ajo":
   {         "dryRun": true       }
       }
   }
   }
   ```

1. 코드 기반 경험 캠페인이나 여정을 검토하고 게시합니다. [방법 알아보기](../code-based/publish-code-based.md)

   이제 개발자가 채널 구성에 정의된 표면에 대한 콘텐츠를 가져오기 위해 API 또는 SDK을 호출하면 변경 사항이 웹 페이지 또는 앱에 적용됩니다.

1. 이제 사용자 지정 [Customer Journey Analytics 보고 대시보드](cja-reporting.md)를 만들어 의사 결정의 성과를 확인할 수 있습니다.