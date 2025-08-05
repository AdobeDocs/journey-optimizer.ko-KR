---
solution: Journey Optimizer
product: journey optimizer
title: 대상자 작성 활동 사용
description: 오케스트레이션된 캠페인에서 대상자 빌드 활동을 사용하는 방법을 알아봅니다
exl-id: 3959b5fa-0c47-42a5-828f-4d7ca9b7e72d
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 60%

---


# 대상자 작성 {#build-audience}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_build_audience"
>title="대상자 빌드 활동"
>abstract="**대상자 작성** 활동을 통해 오케스트레이션된 캠페인을 시작할 대상자를 정의할 수 있습니다. 오케스트레이션된 캠페인의 컨텍스트에서 메시지를 보낼 때 메시지 대상자는 채널 활동에 정의되지 않고 **대상자 빌드** 활동에 정의됩니다."

마케터는 직관적인 인터페이스를 통해 복잡한 대상자 세그먼트를 만들 수 있으므로 다양한 기준과 행동을 기반으로 사용자를 타겟팅하여 캠페인을 더욱 효과적으로 조정할 수 있습니다.

이렇게 하려면 **[!UICONTROL 대상자 작성]** 타겟팅 활동을 사용하십시오. 이 활동은 오케스트레이션된 캠페인에 돌입하는 대상자를 정의합니다. 오케스트레이션된 캠페인의 일부로 메시지를 보낼 때 대상자는 오케스트레이션된 캠페인 내부가 아닌 **[!UICONTROL 대상자 빌드]** 활동에서 정의됩니다.

## 대상자 빌드 활동 구성 {#build-audience-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_build_audience_audienceselector"
>title="대상자"
>abstract="새 게재를 디자인할 때 대상자를 사용하는 것과 같은 방식으로 대상자를 선택합니다."

**[!UICONTROL 대상자 빌드]** 활동을 구성하려면 다음 단계를 따르십시오.

1. **[!UICONTROL 대상자 빌드]** 활동을 추가합니다.

   ![](../assets/build-audience.png)

1. **[!UICONTROL 레이블]**&#x200B;을 정의합니다.

1. 아래 탭에 자세히 나와 있는 단계에 따라 대상자를 구성합니다.

1. **[!UICONTROL 차원 타겟팅]**&#x200B;을 선택합니다. 타기팅 차원을 사용하면 수신자, 약정 수혜자, 운영자, 구독자 등 작업에서 타기팅하는 집단을 정의할 수 있습니다. 기본적으로 대상은 수신자 중에서 선택됩니다.

1. **[!UICONTROL 계속]**&#x200B;을 클릭합니다.

1. 규칙 빌더를 사용하여 쿼리를 정의합니다. [이 섹션에서 규칙 빌더에 대해 자세히 알아보기](../orchestrated-rule-builder.md)

1. 대상자가 비어 있을 때 아웃바운드 전환을 생성할지 여부를 지정합니다.

## 예{#build-audience-examples}

다음은 두 개의 **[!UICONTROL 대상자 작성]** 활동을 통해 오케스트레이션된 캠페인의 예입니다. 첫 번째는 장바구니에 상품을 담은 프로필, 이메일 게재 순으로 타겟팅합니다. 두 번째는 위시리스트를 포함한 프로필, SMS 게재 순으로 타겟팅합니다.

![](../assets/build-audience-2.png)
