---
product: experience platform
solution: Experience Platform
title: 이벤트를 수집할 데이터 세트 만들기
description: 이벤트를 수집하기 위한 데이터 세트를 만드는 방법을 알아봅니다
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 99963ef4-0b19-475e-96f4-2eac3f680c6f
source-git-commit: b06b545d377fcd1ffe6ed218badeb94c1bb85ef2
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 12%

---

# 이벤트를 수집할 데이터 세트 만들기 {#create-dataset}

경험 이벤트를 수집하려면 먼저 이러한 이벤트를 보낼 데이터 세트를 만들어야 합니다.

먼저 데이터 세트에 사용할 스키마를 만듭니다.

1. 에서 **[!UICONTROL 데이터 관리]** 메뉴, 선택 **[!UICONTROL 스키마]**&#x200B;로 이동합니다. **[!UICONTROL 찾아보기]** 탭을 클릭하고 **[!UICONTROL 스키마 만들기]**.

   ![](../assets/ai-ranking-create-schema.png)

1. 선택 **[!UICONTROL XDM ExperienceEvent]**.

   ![](../assets/ai-ranking-xdm-event.png)

   >[!NOTE]
   >
   >XDM 스키마 및 필드 그룹의 [XDM 시스템 개요 설명서](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko){target="_blank"}.

1. 에서 **[!UICONTROL 필드 그룹]** 왼쪽의 섹션에서 을 선택합니다. **[!UICONTROL 추가]**.

   ![](../assets/ai-ranking-fields-groups.png)

1. 에서 **[!UICONTROL 검색]** 필드를 입력하고 &quot;제안 상호 작용&quot;을 입력하고 을 선택합니다 **[!UICONTROL 경험 이벤트 - 제안 상호 작용]** 필드 그룹.

   ![](../assets/ai-ranking-proposition-interactions.png)

   >[!CAUTION]
   >
   >데이터 집합에 사용할 스키마에는 **[!UICONTROL 경험 이벤트 - 제안 상호 작용]** 연결된 필드 그룹입니다. 그렇지 않으면 순위 전략에서 사용할 수 없습니다.

1. 클릭 **[!UICONTROL 필드 그룹 추가]**.

   ![](../assets/ai-ranking-add-field-group.png)

   >[!NOTE]
   >필드 그룹은 이전에 mixin이라고 불렀습니다.

1. 이름을 입력하고 스키마를 저장합니다.

>[!NOTE]
>
>스키마 빌드에 대한 자세한 내용 [스키마 작성 기본 사항](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=en#understanding-schemas){target="_blank"}.

이제 이 스키마를 사용하여 데이터 세트를 만들 준비가 되었습니다. 이렇게 하려면 아래 단계를 수행합니다:

1. 에서 **[!UICONTROL 데이터 관리]** 메뉴, 선택 **[!UICONTROL 데이터 세트]**&#x200B;로 이동합니다. **[!UICONTROL 찾아보기]** 탭을 클릭하고 **[!UICONTROL 데이터 집합 만들기]**.

   ![](../assets/ai-ranking-create-dataset.png)

1. **[!UICONTROL 스키마에서 데이터 세트 만들기]**&#x200B;를 선택합니다.

   ![](../assets/ai-ranking-create-dataset-from-schema.png)

1. 목록에서 방금 만든 스키마를 선택합니다.

   ![](../assets/ai-ranking-dataset-select-schema.png)

1. **[!UICONTROL 다음]**&#x200B;을 클릭합니다.

1. 에서 데이터 세트에 대한 고유한 이름을 제공합니다 **[!UICONTROL 이름]** 필드를 입력하고 **[!UICONTROL 완료]**.

   ![](../assets/ai-ranking-dataset-name.png)

>[!NOTE]
>
>이제 다음 경우에 이벤트 데이터를 수집하도록 이 데이터 세트를 선택할 수 있습니다 [등급 전략 생성](#create-ranking-strategy).
