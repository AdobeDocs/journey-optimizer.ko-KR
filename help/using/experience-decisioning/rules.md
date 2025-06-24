---
title: 결정 규칙
description: 의사 결정 규칙 작업 방법 알아보기
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 033a11b8-c848-4e4a-b6f0-62fa0a2152bf
source-git-commit: ebefeb59a19e831ec7f86cee690a35fe71e14554
workflow-type: tm+mt
source-wordcount: '515'
ht-degree: 20%

---

# 결정 규칙 {#rules}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_rules"
>title="의사 결정 규칙 만들기"
>abstract="의사 결정 규칙을 사용하면 결정 항목 수준에서 직접 또는 특정 선택 전략 내에서 제한 사항을 적용하여 결정 항목의 대상자를 정의할 수 있습니다. 이를 통해 어떤 항목을 어떤 대상에게 제공할지 정확하게 제어할 수 있습니다."

## 의사 결정 규칙 기본 정보 {#about}

의사 결정 규칙을 사용하면 결정 항목 수준에서 직접 또는 특정 선택 전략 내에서 제한 사항을 적용하여 결정 항목의 대상자를 정의할 수 있습니다. 이를 통해 어떤 항목을 어떤 대상에게 제공할지 정확하게 제어할 수 있습니다.

예를 들어, 여성을 위해 디자인된 요가 관련 제품을 갖춘 의사 결정 항목이 있는 시나리오를 생각해 보자. 의사 결정 규칙을 사용하여 이러한 항목이 성별이 &#39;여성&#39;이고 &#39;요가&#39;에서 &#39;관심 영역&#39;을 표시한 프로필에만 표시되도록 지정할 수 있습니다.

>[!NOTE]
>
>항목 및 선택 전략 수준 결정 규칙 외에도 캠페인 수준에서 의도한 대상자를 정의할 수도 있습니다. [자세히 알아보기](../campaigns/create-campaign.md#audience)

결정 규칙 목록은 **[!UICONTROL 전략 설정]** 메뉴에서 액세스할 수 있습니다.

![](assets/decision-rules-list.png)

## 의사 결정 규칙 만들기 {#create}

의사 결정 규칙을 만들려면 다음 단계를 수행합니다.

1. **[!UICONTROL 전략 설정]** / **[!UICONTROL 의사 결정 규칙]**(으)로 이동한 다음 **[!UICONTROL 규칙 만들기]** 단추를 클릭합니다.

   >[!NOTE]
   >
   >Adobe Experience Platform의 데이터를 사용하여 외부 데이터로 의사 결정 논리를 보강할 수도 있습니다. 이 기능은 제품 가용성 또는 실시간 가격과 같이 자주 변경되는 속성에 특히 유용합니다. 이 기능은 현재 모든 고객이 공개 Beta로 사용할 수 있습니다. 액세스하려면 계정 담당자에게 문의하십시오. [의사 결정을 위해 Adobe Experience Platform 데이터를 사용하는 방법 알아보기](../experience-decisioning/aep-data-exd.md)

1. 의사 결정 규칙 만들기 화면이 열립니다. 규칙에 이름을 지정하고 설명을 제공합니다.

1. Adobe Experience Platform 세그먼트 빌더를 사용하여 필요에 따라 의사 결정 규칙을 만듭니다. 이렇게 하려면 다음과 같은 다양한 데이터 소스를 활용할 수 있습니다.
   * 프로필 및 결정 항목 속성,
   * 대상,
   * Adobe Experience Platform에서 제공되는 컨텍스트 데이터. [컨텍스트 데이터를 활용하는 방법 알아보기](context-data.md)

   ![](assets/decision-rules-build.png)

   >[!NOTE]
   >
   >의사 결정 규칙을 만들기 위해 제공된 세그먼트 빌더는 Adobe Experience Platform 세그먼테이션 서비스와 함께 사용되는 세그먼트 빌더와 비교하여 몇 가지 특성을 제공합니다. 그러나 설명서에 설명된 전역 프로세스는 의사 결정 규칙을 작성하는 데 여전히 유효합니다. [세그먼트 정의를 만드는 방법을 알아봅니다](../audience/creating-a-segment-definition.md)

1. 작업 영역에서 새 필드를 추가하고 구성할 때 **[!UICONTROL 대상 속성]** 창에 대상에 속하는 예상 프로필에 대한 정보가 표시됩니다. 데이터를 업데이트하려면 **[!UICONTROL 예상 새로 고침]**&#x200B;을 클릭하세요.

   >[!NOTE]
   >
   >규칙 매개 변수에 컨텍스트 데이터와 같이 프로필에 없는 데이터가 포함되어 있으면 프로필 추정치를 사용할 수 없습니다.

1. 결정 규칙이 준비되면 **[!UICONTROL 저장]**&#x200B;을 클릭합니다. 생성된 규칙은 목록에 표시되며 의사 결정 항목 및 선택 전략에서 사용하여 프로필에 대한 의사 결정 항목 표시를 제어할 수 있습니다.

   >[!NOTE]
   >
   >자격 규칙의 중첩 깊이는 30개 수준으로 제한됩니다. 이는 PQL 문자열에서 `)` 닫는 괄호를 계산하여 측정됩니다. 규칙 문자열의 크기는 UTF-8 인코딩 문자의 경우 최대 15KB까지 가능합니다. 이는 15,000개의 ASCII 문자(각각 1바이트) 또는 3,750-7,500개의 비 ASCII 문자(각각 2-4바이트)에 해당합니다. [보호 기능 및 제한 결정에 대해 자세히 알아보기](gs-experience-decisioning.md#guardrails)
