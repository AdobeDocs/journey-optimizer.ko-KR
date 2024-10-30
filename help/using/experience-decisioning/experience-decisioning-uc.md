---
title: 의사 결정 사용 사례
description: 코드 기반 채널을 사용한 실험을 사용하여 의사 결정을 만드는 방법에 대해 알아봅니다
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate, Experienced
badge: label="제한 공개"
source-git-commit: ac8ccb52bd16a26c14dea148f989256e28170765
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 7%

---

# 의사 결정 사용 사례 {#experience-decisioning-uc}

이 사용 사례에서는 타겟 대상자에게 가장 성과가 좋은 결정 정책을 측정하기 위해 각각 다른 결정 정책을 포함하는 두 개의 게재 처리를 정의합니다.

## 항목 및 전략 만들기

먼저 항목을 만들고, 컬렉션에서 함께 그룹화하고, 규칙과 등급 지정 방법을 설정해야 합니다. 이러한 요소를 사용하여 선택 전략을 작성할 수 있습니다.

1. **[!UICONTROL Decisioning]** > **[!UICONTROL 카탈로그]**(으)로 이동하여 여러 오퍼 항목을 만듭니다. 대상자 또는 규칙을 사용하여 제한을 설정하여 각 항목을 특정 프로필로만 제한합니다. [자세히 알아보기](items.md)

   <!--
   1. From the items list, click the **[!UICONTROL Edit schema]** button  and edit the custom attributes if needed. [Learn how to work with catalogs](catalogs.md)-->

1. **컬렉션**&#x200B;을 만들어 환경 설정에 따라 결정 항목을 분류하고 그룹화합니다. [자세히 알아보기](collections.md)

1. 결정 항목을 표시할 대상을 결정하려면 **결정 규칙**&#x200B;을 만드십시오. [자세히 알아보기](rules.md)

1. **순위 메서드**&#x200B;를 만들고 결정 전략 내에서 적용하여 결정 항목을 선택하는 우선 순위를 결정합니다. [자세히 알아보기](ranking.md)

1. 컬렉션, 의사 결정 규칙 및 순위 방법을 활용하여 프로필에 표시하는 데 적합한 의사 결정 항목을 식별하는 **선택 전략**&#x200B;을 작성하십시오. [자세히 알아보기](selection-strategies.md)

## 결정 정책 만들기

웹 사이트 또는 모바일 앱에서 방문자에게 최고의 동적 오퍼 및 경험을 제공하려면 코드 기반 캠페인에 의사 결정 정책을 추가하십시오.

각각 다른 결정 정책이 포함된 두 가지 게재 처리를 정의합니다.

1. 캠페인을 만들고 **[!UICONTROL 코드 기반 경험]** 작업을 선택하십시오. [자세히 알아보기](../code-based/create-code-based.md)

1. 캠페인 요약 페이지에서 **[!UICONTROL 실험 만들기]**&#x200B;를 클릭하여 콘텐츠 실험 구성을 시작합니다. [자세히 알아보기](../content-management/content-experiment.md)

1. **[!UICONTROL 결정]** 아이콘을 선택하고 **[!UICONTROL 결정 만들기]**&#x200B;를 클릭한 다음 결정 세부 정보를 입력하십시오. [자세히 알아보기](create-decision.md)

   ![](assets/decision-code-based-create.png)

1. 의사 결정에 대한 선택 전략을 정의합니다. **[!UICONTROL 전략 추가]**&#x200B;를 클릭합니다.

1. Click **[!UICONTROL Create]**. 새 결정은 **[!UICONTROL 결정]**&#x200B;에 추가됩니다.

   ![](assets/decision-code-based-decision-added.png)

1. 추가 작업 아이콘(세 점)을 클릭하고 **[!UICONTROL 추가]**&#x200B;를 선택합니다. 이제 이 내에 원하는 모든 결정 특성을 추가할 수 있습니다.

   ![](assets/decision-code-based-add-decision.png)

1. 프로필 속성과 같이 개인화 편집기에서 사용할 수 있는 다른 속성을 추가할 수도 있습니다.

   ![](assets/decision-code-based-decision-profile-attribute.png)

1. 처리 B를 작성하고 위의 단계를 반복하여 다른 결정을 만듭니다.

1. 콘텐츠를 저장합니다.


