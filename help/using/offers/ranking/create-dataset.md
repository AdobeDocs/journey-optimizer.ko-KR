---
product: experience platform
solution: Experience Platform
title: 이벤트를 수집할 데이터 세트 만들기
description: 이벤트를 수집하기 위한 데이터 세트를 만드는 방법을 알아봅니다
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 99963ef4-0b19-475e-96f4-2eac3f680c6f
source-git-commit: 5abcef4ff057bb351abaafbf4dcb99e1ab61c6a9
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 12%

---

# 이벤트를 수집할 데이터 세트 만들기 {#create-dataset}

AI 모델을 만들기 전에 전환 이벤트를 수집할 데이터 세트를 만들어야 합니다. 먼저 데이터 세트에 사용할 스키마를 만듭니다.

1. 에서 **[!UICONTROL Data Management]** 메뉴, 선택 **[!UICONTROL Schema]**&#x200B;로 이동합니다. **[!UICONTROL Browse]** 탭을 클릭하고 **[!UICONTROL Create schema]**.

   ![](../assets/ai-ranking-create-schema.png)

1. 선택 **[!UICONTROL XDM ExperienceEvent]**.

   ![](../assets/ai-ranking-xdm-event.png)

   >[!NOTE]
   >
   >XDM 스키마 및 필드 그룹의 [XDM 시스템 개요 설명서](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko){target=&quot;_blank&quot;}.

1. 에서 **[!UICONTROL Field groups]** 왼쪽의 섹션에서 을 선택합니다. **[!UICONTROL Add]**.

   ![](../assets/ai-ranking-fields-groups.png)

1. 에서 **[!UICONTROL Search]** 필드를 입력하고 &quot;제안 상호 작용&quot;을 입력하고 을 선택합니다 **[!UICONTROL Experience Event - Proposition Interactions]** 필드 그룹.

   ![](../assets/ai-ranking-proposition-interactions.png)

   >[!CAUTION]
   >
   >데이터 집합에 사용할 스키마에는 **[!UICONTROL Experience Event - Proposition Interactions]** 연결된 필드 그룹입니다. 그렇지 않으면 순위 전략에서 사용할 수 없습니다.

1. **[!UICONTROL Add field groups]**&#x200B;을(를) 클릭합니다.

   ![](../assets/ai-ranking-add-field-group.png)

   >[!NOTE]
   >필드 그룹은 이전에 mixin이라고 불렀습니다.

1. 이름을 입력하고 스키마를 저장합니다.

>[!NOTE]
>
>스키마 빌드에 대한 자세한 내용 [스키마 작성 기본 사항](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=en#understanding-schemas){target=&quot;_blank&quot;}.

이제 이 스키마를 사용하여 데이터 세트를 만들 준비가 되었습니다. 이렇게 하려면 아래 단계를 수행합니다:

1. 에서 **[!UICONTROL Data Management]** 메뉴, 선택 **[!UICONTROL Datasets]**&#x200B;로 이동합니다. **[!UICONTROL Browse]** 탭을 클릭하고 **[!UICONTROL Create dataset]**.

   ![](../assets/ai-ranking-create-dataset.png)

1. **[!UICONTROL Create dataset from schema]**&#x200B;를 선택합니다.

   ![](../assets/ai-ranking-create-dataset-from-schema.png)

1. 목록에서 방금 만든 스키마를 선택합니다.

   ![](../assets/ai-ranking-dataset-select-schema.png)

1. **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.

1. 에서 데이터 세트에 대한 고유한 이름을 제공합니다 **[!UICONTROL Name]** 필드를 입력하고 **[!UICONTROL Finish]**.

   ![](../assets/ai-ranking-dataset-name.png)

이제 데이터 세트를 선택하여 이벤트 데이터를 수집할 준비가 되었습니다. [등급 전략 생성](#create-ranking-strategy).
