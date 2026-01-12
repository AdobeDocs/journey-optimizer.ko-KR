---
title: 규칙 작성
description: 규칙 작업 방법 알아보기
feature: Decisioning, Campaigns, Journeys, Activities
topic: Integrations, Content Management
role: User
level: Intermediate
exl-id: 033a11b8-c848-4e4a-b6f0-62fa0a2152bf
version: Journey Orchestration
source-git-commit: 27de3d2171e6f6575eb66ada20f951f6cb3abc98
workflow-type: tm+mt
source-wordcount: '958'
ht-degree: 9%

---

# 규칙 작성 {#rules}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_rules"
>title="규칙 만들기"
>abstract="의사 결정 항목 또는 선택 전략에 사용할 수 있는 **의사 결정 규칙**, 표시할 항목을 제어하는 규칙 **타깃팅 규칙**, 개인화된 콘텐츠를 수신할 수 있는 특정 대상 세그먼트를 결정하는 규칙 또는 특정 여정 경로를 입력하는 규칙 유형을 만들 수 있습니다.<br/><br/>의사 결정 규칙을 만들 때 **[!UICONTROL 데이터 집합 조회 사용]**&#x200B;을 선택하여 Adobe Experience Platform 데이터를 사용할 수 있습니다. 이를 통해 동적 외부 속성을 기반으로 적격성 기준을 정의하여 관련이 있는 경우에만 결정 항목이 표시되도록 할 수 있습니다."

## 규칙 기본 정보 {#about}

[!DNL Journey Optimizer]에서 두 가지 유형의 재사용 가능한 규칙을 만들 수 있습니다.

* [결정 규칙](#decision-rules)
* [타기팅 규칙](#targeting-rules)

### 결정 규칙 {#decision-rules}

의사 결정 규칙을 사용하면 의사 결정 항목 수준에서 직접 또는 특정 선택 전략 내에서 제한을 적용하여 의사 결정 항목의 대상자를 정의할 수 있습니다. 이를 통해 어떤 항목을 어떤 대상에게 제공할지 정확하게 제어할 수 있습니다.

예를 들어, 여성을 위해 디자인된 요가 관련 제품을 갖춘 의사 결정 항목이 있는 시나리오를 생각해 보자. 의사 결정 규칙을 사용하여 이러한 항목이 성별이 &#39;여성&#39;이고 &#39;요가&#39;에서 &#39;관심 영역&#39;을 표시한 프로필에만 표시되도록 지정할 수 있습니다.

>[!NOTE]
>
>항목 및 선택 전략 수준 결정 규칙 외에도 캠페인 수준에서 의도한 대상자를 정의할 수도 있습니다. [자세히 알아보기](../campaigns/create-campaign.md#audience)

### 타기팅 규칙 {#targeting-rules}

>[!AVAILABILITY]
>
>타기팅 규칙은 현재 제한된 가용성으로 제공됩니다. 액세스 권한을 얻으려면 Adobe 담당자에게 문의하십시오.
>
>이 기능은 **Decisioning** 추가 기능 서비스를 구입한 조직에서만 사용할 수 있습니다. 점진적으로 모든 고객을 대상으로 롤아웃될 예정입니다.

타겟팅 규칙을 사용하면 특정 대상 세그먼트를 기반으로 하여 고객이 개인화된 콘텐츠를 수신하거나 특정 여정 경로를 입력할 수 있도록 충족해야 하는 특정 자격을 결정할 수 있습니다. 이렇게 하면 여정 및 캠페인에서 하위 대상을 타겟팅할 수 있습니다.

고객 행동 이벤트 및 컨텍스트 데이터 외에 여러 속성의 조합인 경우가 많습니다. 시간과 노력을 절약하기 위해 타겟팅 규칙을 한 번 만들어 여정 및 캠페인에서 재사용할 수 있으며, 작성 시 인라인으로 빠르게 수정할 수 있습니다.

다음 규칙 중 하나를 사용할 수 있습니다.

* 여정 또는 캠페인에서 [콘텐츠 최적화 타깃팅](../content-management/optimization-targeting.md)을(를) 만드는 경우;
* [여정 경로 최적화](../building-journeys/optimize.md#targeting)을(를) 빌드하는 중입니다.

➡️ [비디오에서 이 기능 살펴보기](#video)

## 액세스 규칙 {#access}

규칙 목록은 **[!UICONTROL 의사 결정]** > **[!UICONTROL 전략 설정]** 메뉴에서 액세스할 수 있습니다.

다음 작업을 사용할 수 있습니다.

* 규칙 엔터티(**[!UICONTROL 결정 항목]** 또는 **[!UICONTROL 타깃팅]** - [자세히 알아보기](#about))를 필터링할 수 있습니다.

* 이름을 클릭하여 규칙을 선택하고 규칙 빌더를 사용하여 편집합니다. [방법 알아보기](#create)

* 각 항목 옆에 있는 **[!UICONTROL 추가 작업]** 단추에서 다음을 수행할 수 있습니다.

   * **[!UICONTROL 결정 항목]** 엔터티를 선택한 경우 규칙을 패키지에 추가하여 다른 샌드박스로 내보냅니다. [개체를 다른 샌드박스로 내보내기](../configuration/copy-objects-to-sandbox.md)하는 방법에 대해 알아봅니다.
   * 규칙 복제
   * 규칙을 삭제합니다.

![](assets/rules-list.png){width=100%}

* 규칙을 구성하는 수식을 표시하려면 **[!UICONTROL 추가 정보]** 아이콘을 클릭합니다.

![](assets/rule-formula.png){width=60%}

## 규칙 만들기 {#create}

규칙을 만들려면 다음 단계를 수행합니다.

1. **[!UICONTROL Decisioning]** > **[!UICONTROL 전략 설정]** > **[!UICONTROL 규칙]**(으)로 이동한 다음 **[!UICONTROL 규칙 만들기]** 단추를 클릭합니다.

1. 규칙 엔티티를 선택하여 규칙을 작성할 객체 유형을 지정합니다.

   ![](assets/rules-select-entity.png){width=90%}

   * **[!UICONTROL 결정 항목]** - 이 규칙은 의사 결정 컨텍스트의 [결정 항목](#decision-rules)에 적용할 수 있습니다.
   * **[!UICONTROL 타깃팅]** - [여정 활동 최적화](#targeting-rules)에서 캠페인 또는 여정의 [콘텐츠 최적화](../content-management/optimization-targeting.md)의 일부로 [타깃팅](../building-journeys/optimize.md#targeting) 규칙을 작성할 때 규칙을 사용할 수 있습니다.

1. **[!UICONTROL 의사 결정 항목]** 규칙을 만드는 경우 **[!UICONTROL 데이터 집합 조회 사용]**&#x200B;을 선택하여 Adobe Experience Platform의 데이터를 사용하여 외부 데이터로 의사 결정 논리를 보강할 수 있습니다. 이 기능은 제품 가용성 또는 실시간 가격과 같이 자주 변경되는 속성에 특히 유용합니다.

   >[!AVAILABILITY]
   >
   >이 기능은 현재 모든 고객이 공개 Beta로 사용할 수 있습니다. 액세스하려면 계정 담당자에게 문의하십시오. [의사 결정을 위해 Adobe Experience Platform 데이터를 사용하는 방법 알아보기](../experience-decisioning/aep-data-exd.md)

1. 규칙 만들기 화면이 열립니다. 규칙에 이름을 지정하고 설명을 제공합니다.

1. Adobe Experience Platform 세그먼트 빌더를 사용하여 필요에 따라 규칙을 만듭니다. 이렇게 하려면 다음과 같은 다양한 데이터 소스를 활용할 수 있습니다.
   * 프로필 속성;
   * 결정 항목 특성 - **[!UICONTROL 결정 항목]** 규칙을 만들 때만 사용할 수 있습니다.
   * 대상;
   * Adobe Experience Platform에서 제공되는 컨텍스트 데이터. [컨텍스트 데이터를 활용하는 방법 알아보기](context-data.md)

   ![](assets/decision-rules-build.png){width=85%}

   >[!NOTE]
   >
   >규칙을 만들기 위해 제공된 세그먼트 빌더는 Adobe Experience Platform 세그먼테이션 서비스와 함께 사용되는 세그먼트 빌더와 비교하여 몇 가지 특성을 제공합니다. 그러나 설명서에 설명된 전역 프로세스는 [!DNL Journey Optimizer]에서 규칙을 작성하는 데 유효합니다. [세그먼트 정의를 만드는 방법을 알아봅니다](../audience/creating-a-segment-definition.md)

1. 작업 영역에서 새 필드를 추가하고 구성할 때 **[!UICONTROL 대상 속성]** 창에 대상에 속하는 예상 프로필에 대한 정보가 표시됩니다. 데이터를 업데이트하려면 **[!UICONTROL 예상 새로 고침]**&#x200B;을 클릭하세요.

   ![](assets/decision-rule-audience-properties.png){width=85%}

   >[!NOTE]
   >
   >규칙 매개 변수에 컨텍스트 데이터와 같이 프로필에 저장되지 않은 데이터가 포함되어 있으면 프로필 추정을 사용할 수 없습니다.

1. 규칙이 준비되면 **[!UICONTROL 만들기]**&#x200B;를 클릭합니다. 생성된 규칙이 목록에 나타나고 사용자가 생성한 엔티티에 따라 사용할 수 있습니다.

   * 프로필에 대한 결정 항목 표시를 제어하는 **결정 항목** 및 **선택 전략**&#x200B;에서
   * 콘텐츠 최적화 또는 경로 최적화에서 **타깃팅**&#x200B;을(를) 빌드하는 경우입니다.

>[!NOTE]
>
>규칙의 중첩 깊이는 30개 수준으로 제한됩니다. 이는 PQL 문자열에서 닫는 괄호 `)`을(를) 계산하여 측정됩니다.
>
>규칙 문자열의 크기는 UTF-8 인코딩 문자의 경우 최대 15KB까지 가능합니다. 이는 15,000개의 ASCII 문자(각각 1바이트) 또는 3,750-7,500개의 비 ASCII 문자(각각 2-4바이트)에 해당합니다.
>
>[자격 규칙 보호 및 제한에 대해 자세히 알아보기](decisioning-guardrails.md#eligibility-rules)

## 사용 방법 비디오 {#video}

Adobe Journey Optimizer에서 재사용 가능한 **타깃팅 규칙**&#x200B;을(를) 만들고, 복제하고, 적용하여 지역, 언어 및 동작과 같은 고객 특성을 기반으로 캠페인을 효율적으로 개인화하여 시간을 절약하고 대상 정밀도를 향상시키는 방법을 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/3476127/?quality=12)
