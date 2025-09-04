---
solution: Journey Optimizer
product: journey optimizer
title: 중복 제거 활동 사용
description: 중복 제거 활동을 사용하는 방법 알아보기
exl-id: 4aa79448-f75a-48d5-8819-f4cb4baad5c7
version: Campaign Orchestration
source-git-commit: 07ec28f7d64296bdc2020a77f50c49fa92074a83
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 98%

---


# 중복 제거 {#deduplication}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication_fields"
>title="중복 요소 식별을 위한 필드"
>abstract="**중복 요소 식별을 위한 필드** 섹션에서 **속성 추가** 버튼을 클릭하여 이메일 주소, 이름, 성 등 동일한 값으로 중복 요소를 식별할 수 있는 필드를 지정합니다. 필드 순서에 따라 먼저 처리할 필드를 지정할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication"
>title="중복 제거 활동"
>abstract="**중복 제거** 활동을 통해 인바운드 활동의 결과에서 중복 요소를 삭제할 수 있습니다. 주로 타기팅 활동 이후와 대상 데이터를 사용할 수 있는 활동 이전에 사용됩니다."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication_complement"
>title="여집합 생성"
>abstract="중복으로 제외된 나머지 집단으로 추가 아웃바운드 전환을 생성할 수 있습니다. 이렇게 하려면 **여집합 생성** 옵션을 토글합니다."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication_settings"
>title="중복 제거 설정"
>abstract="수신 데이터에서 중복 요소를 삭제하려면 아래 필드에서 중복 제거 방법을 정의합니다. 기본적으로 하나의 레코드만 유지됩니다. 또한 표현식 또는 속성을 기반으로 중복 제거 모드를 선택해야 합니다. 기본적으로 중복에서 제외할 레코드는 무작위로 선택됩니다."

**[!UICONTROL 중복 제거]** 활동은 **[!UICONTROL 타기팅]** 활동입니다. 이 활동을 사용하면 인바운드 활동의 결과에서 중복 요소를 삭제할 수 있습니다(예: 수신자 목록의 중복 프로필). **[!UICONTROL 중복 제거]** 활동은 주로 타기팅 활동 이후 타기팅된 데이터를 사용하도록 허용하는 활동 이전에 사용됩니다.

## 중복 제거 활동 구성{#deduplication-configuration}

**[!UICONTROL 중복 제거]** 활동을 구성하려면 다음 단계를 따릅니다.


1. 오케스트레이션된 캠페인에 **[!UICONTROL 중복 제거]** 활동을 추가합니다.

1. **[!UICONTROL 중복 요소 식별을 위한 필드]** 섹션에서 **[!UICONTROL 속성 추가]** 버튼을 클릭하여 이메일 주소, 이름, 성 등 동일한 값으로 중복 요소를 식별할 수 있는 필드를 지정합니다. 필드 순서에 따라 먼저 처리할 필드를 지정할 수 있습니다.

   ![](../assets/deduplication-1.png)

1. **[!UICONTROL 중복 제거 설정]** 섹션에서 [유지할 중복] 필드를 사용하여 유지할 고유 레코드 수를 선택합니다. 기본값은 1이며, 이 경우 중복 그룹당 하나의 레코드가 유지됩니다. 모든 중복을 유지하려면 0으로 설정합니다.

   예를 들어 레코드 A와 B가 Y의 중복이고 레코드 C가 Z의 중복인 경우 다음과 같이 처리됩니다.

   * **필드 값이 1인 경우**: 레코드 Y와 Z만 유지됩니다.
   * **필드 값이 0인 경우**: 모든 레코드(A, B, C, Y, Z)가 유지됩니다.
   * **필드 값이 2인 경우**: C와 Z가 유지되고, A, B, Y 중 두 값이 임의로 또는 중복 제거 방법에 따라 유지됩니다.

1. **[!UICONTROL 중복 제거 방법]**&#x200B;을 선택합니다. 이 선택은 시스템이 각 중복 그룹에서 유지할 레코드를 결정하는 방법을 정의합니다.

   * **[!UICONTROL 임의 선택]**: 중복 레코드 중에서 유지할 레코드를 임의로 선택합니다.
   * **[!UICONTROL 표현식 사용]**: 사용자가 정의한 표현식에 따라 값이 가장 높거나 가장 낮은 레코드를 유지합니다.
   * **[!UICONTROL 비어 있지 않은 값]**: 선택한 필드가 비어 있지 않은 레코드를 유지합니다(예: 전화번호가 있는 프로필만 유지).
   * **[!UICONTROL 값 목록 따라가기]**: 하나 이상의 필드에 대해 특정 값을 우선시할 수 있습니다. 예를 들어 “국가”가 프랑스로 설정된 레코드를 우선시하도록 지정할 수 있습니다. **[!UICONTROL 속성]**&#x200B;을 클릭하여 필드를 선택하거나 사용자 정의 표현식을 만듭니다. **[!UICONTROL 추가 버튼]**&#x200B;을 사용하여 우선 고려할 값을 우선순위 순으로 입력합니다.

   ![](../assets/deduplication-2.png)

1. 남은 집단을 활용하려면 **[!UICONTROL 여집합 생성]** 옵션을 선택합니다. 여집합은 모든 중복으로 구성됩니다. 그런 다음 추가 전환이 활동에 추가됩니다.

## 예{#deduplication-example}

다음 예제에서는 게재를 보내기 전에 **[!UICONTROL 중복 제거]** 활동을 사용하여 타깃 대상자 중 중복 레코드를 제거합니다. 먼저 대상자를 필터링하여 비어 있지 않은 이메일 필드가 있는 프로필만 포함합니다. 그런 다음 **[!UICONTROL 중복 제거]** 활동이 이메일 주소를 사용하여 중복을 식별하고 제외합니다.

![](../assets/deduplication-3.png)
