---
solution: Journey Optimizer
product: journey optimizer
title: 차원 변경 활동 사용
description: 차원 변경 활동을 사용하는 방법 알아보기
exl-id: 83e66f10-93dd-4759-840c-2c83abc42a28
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 74%

---


# 차원 변경 {#change-dimension}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_dimension_complement"
>title="여집합 생성"
>abstract="중복으로 제외된 나머지 집단으로 추가 아웃바운드 전환을 생성할 수 있습니다. 이렇게 하려면 **여집합 생성** 옵션을 토글합니다."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_change_dimension"
>title="차원 활동 변경"
>abstract="이 활동을 통해 대상자를 빌드하면서 타기팅 차원을 변경할 수 있습니다. 데이터 템플릿과 입력 차원에 따라 축이 이동됩니다. 예를 들어 “계약” 차원에서 “클라이언트” 차원으로 전환할 수 있습니다."

마케터는 오케스트레이션된 캠페인 내에서 한 데이터 엔티티에서 관련 엔티티로 전환하여 대상 타깃팅을 향상시킬 수 있습니다. 이를 통해 단순히 사용자 프로필을 활용하는 것을 넘어 구매, 예약 또는 기타 상호 작용과 같은 특정 행동에 집중할 수 있습니다.

이렇게 하려면 **[!UICONTROL 차원 변경]** 활동을 사용합니다. 오케스트레이션된 캠페인 동안 타겟팅 차원을 조정할 수 있습니다.

<!--
>[!IMPORTANT]
>
>Please note that the **[!UICONTROL Change Dimension]** and **[!UICONTROL Change Data source]** activities should not be added in one row. If you need to use both activities consecutively, make sure you include an **[!UICONTROL Enrichement]** activity in between them. This ensures proper execution and prevents potential conflicts or errors.-->

## 차원 변경 활동 구성 {#configure}

**[!UICONTROL 차원 변경]** 활동을 구성하려면 다음 단계를 따릅니다.

1. 오케스트레이션된 캠페인에 **[!UICONTROL 차원 변경]** 활동을 추가합니다.

   ![](../assets/orchestrated-change-dimension.png)

1. **[!UICONTROL 새 타깃 차원]**&#x200B;을 정의합니다. 차원 변경 중에는 모든 레코드가 유지됩니다.


## 예 {#example}

이 사용 사례는 지난 한 달 내에 위시리스트를 만든 프로필에 SMS를 보내는 데 중점을 둡니다.

먼저 **[!UICONTROL 대상자 작성]** 활동을 만들며 **[!UICONTROL 위시리스트]** 타기팅 차원으로 모든 관련 위시리스트를 식별합니다.

그런 다음 **[!UICONTROL 차원 변경]** 활동을 추가하여 타기팅 차원을 **[!UICONTROL 위시리스트]**&#x200B;에서 **[!UICONTROL 수신자]로 전환합니다.** 이 단계에서는 오케스트레이션된 캠페인 타겟이 해당 위시리스트에 연결된 올바른 프로필을 사용하도록 하여 의도한 프로필로 SMS를 보낼 수 있도록 합니다.

![](../assets/orchestrated-change-dimension-example.png)
