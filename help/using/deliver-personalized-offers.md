---
title: 개인화된 오퍼 추가
description: 메시지에 개인화된 오퍼를 추가하는 방법을 알아봅니다
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 1e648eca-b5ca-4767-b45d-c179243e347f
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 1%

---

# 개인화된 오퍼 추가 {#deliver-personalized-offers}

in [!DNL Journey Optimizer] 이메일 메시지를 통해 고객에게 전달할 최상의 오퍼를 선택하기 위해 오퍼 결정 엔진을 활용할 의사 결정(이전에 &#39;오퍼 활동&#39;이라고 함)을 삽입할 수 있습니다.

예를 들어 이메일에 수신자의 충성도 수준에 따라 달라지는 특별 할인 오퍼가 표시되는 결정을 추가할 수 있습니다.

오퍼를 만들고 관리하는 방법에 대한 자세한 내용은 [이 섹션](offers/get-started/starting-offer-decisioning.md).

대상 **전체 종단 간 예제** 오퍼를 구성하고, 결정에서 오퍼를 사용하고, 이메일에서 이 결정을 활용하는 방법을 표시하고, 체크아웃합니다. [이 섹션](offers/offers-e2e.md#insert-decision-in-email).

➡️ [이 비디오에서 오퍼를 개인화로 추가하는 방법을 배웁니다](#video-offers)

## 이메일에 결정 삽입 {#insert-offers}

>[!CAUTION]
>
>시작하기 전에 다음을 수행해야 합니다 [오퍼 결정 정의](offers/offer-activities/create-offer-activities.md).

전자 메일 메시지에 의사 결정을 삽입하려면 아래 단계를 따르십시오.

1. 이메일을 만든 다음 이메일 디자이너를 열어 해당 콘텐츠를 구성합니다.

1. 추가 **[!UICONTROL Offer decision]** 컨텐츠 구성 요소입니다.

   ![](assets/deliver-offer-component.png)

   에서 콘텐츠 구성 요소를 사용하는 방법을 알아봅니다. [이 섹션](content-components.md).

1. 다음 **[!UICONTROL Offer decision]** 오른쪽 팔레트에 탭이 표시됩니다. **[!UICONTROL Select Offer decision]**&#x200B;을(를) 클릭합니다.

   ![](assets/deliver-offer-tab.png)

1. 표시되는 창에서 표시할 오퍼에 해당하는 배치를 선택합니다.

   [배치](offers/offer-library/creating-placements.md) 오퍼를 표시하는 데 사용되는 컨테이너입니다. 이 예에서는 &quot;이메일 상단 이미지&quot; 배치를 사용합니다. 이 배치는 메시지 상단에 있는 이미지 유형 오퍼를 표시하기 위해 오퍼 라이브러리에 생성되었습니다.

1. 컨텐츠 구성 요소에서 사용할 오퍼 활동을 선택한 다음, **[!UICONTROL Add]**.

   >[!NOTE]
   >
   >선택한 배치와 호환되는 결정만 목록에 표시됩니다. 이 예제에서 한 개의 오퍼 활동만 &quot;이메일 상단 이미지&quot; 배치와 일치합니다.

   ![](assets/deliver-offer-placement.png)

이제 오퍼 활동이 구성 요소에 추가됩니다.


## 이메일에서 오퍼 미리 보기 {#preview-offers-in-email}

을 사용하여 이메일에 추가된 의사 결정의 일부인 다른 오퍼를 미리 볼 수 있습니다 **[!UICONTROL Offers]** 섹션 또는 컨텐츠 구성 요소 화살표

![](assets/deliver-offer-preview.png)

고객 프로필과 함께 의사 결정의 일부인 다른 오퍼를 표시하려면 아래 단계를 따르십시오.

1. **[!UICONTROL Preview]**&#x200B;을(를) 클릭합니다.

   ![](assets/deliver-offer-preview-button.png)

   >[!NOTE]
   >
   >메시지를 미리 보려면 테스트 프로필을 사용할 수 있어야 합니다. 방법 알아보기 [테스트 프로필 만들기](building-journeys/creating-test-profiles.md).

1. 테스트 프로필을 식별하는 데 사용할 네임스페이스를 선택하려면 을(를) 선택합니다 **[!UICONTROL Email]** 에서 **[!UICONTROL Identity namespace]** 필드.

   >[!NOTE]
   >
   >이 예제에서는 **이메일** 네임스페이스. Adobe Experience Platform ID 네임스페이스에 대해 자세히 알아보십시오 [이 섹션](get-started-identity.md).

1. ID 네임스페이스 목록에서 을(를) 선택합니다 **[!UICONTROL Email]** 을(를) 클릭합니다. **[!UICONTROL Select]**.

1. 에서 **[!UICONTROL Identity value]** 필드에 테스트 프로필을 식별할 값을 입력합니다. 이 예에서는 테스트 프로필의 이메일 주소를 입력합니다.

   <!--For example enter smith@adobe.com and click the **[!UICONTROL Add profile]** button.-->

1. 프로필 데이터에 따라 메시지의 다른 변형을 테스트할 수 있도록 다른 프로필을 추가합니다.

   ![](assets/deliver-offer-test-profiles.png)

1. 을(를) 클릭합니다. **[!UICONTROL Preview]** 탭을 클릭하여 메시지를 테스트합니다.

1. 테스트 프로필을 선택합니다. 선택한 프로필(여성)에 해당하는 오퍼가 표시됩니다.

   ![](assets/deliver-offer-test-profile-female-preview.png)

1. 다른 테스트 프로필을 선택하여 메시지의 각 변형에 대한 이메일 콘텐츠를 미리 봅니다. 이제 메시지 콘텐츠에 선택한 테스트 프로필(이제 남성)에 해당하는 오퍼가 표시됩니다.

   ![](assets/deliver-offer-test-profile-male-preview.png)

에서 메시지 미리 보기를 확인하는 세부 단계에 대해 자세히 알아보십시오 [이 섹션](#preview-your-messages).

## 방법 비디오{#video-offers}

의 메시지에 offer decisioning 구성 요소를 추가하는 방법을 알아봅니다. [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/334088?quality=12)
