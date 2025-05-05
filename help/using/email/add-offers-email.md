---
solution: Journey Optimizer
product: journey optimizer
title: 개인화된 오퍼 추가
description: 메시지에 개인화된 오퍼를 추가하는 방법 알아보기
feature: Email Design, Offers
topic: Content Management
role: User
level: Intermediate
keywords: 오퍼, 결정, 이메일, 개인화, 결정
exl-id: 1e648eca-b5ca-4767-b45d-c179243e347f
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 0%

---

# 개인화된 오퍼 추가 {#deliver-personalized-offers}

[!DNL Journey Optimizer] 이메일에서 고객에게 제공할 최상의 오퍼를 선택하기 위해 의사 결정 관리 엔진을 활용하는 의사 결정을 삽입할 수 있습니다.

예를 들어 수신자의 충성도 수준에 따라 달라지는 특별 할인 오퍼를 이메일에 표시하는 결정을 추가할 수 있습니다.

>[!IMPORTANT]
>
>여정의 메시지에 사용 중인 오퍼 의사 결정이 변경되는 경우 여정 게시를 취소하고 다시 게시해야 합니다.  이렇게 하면 변경 사항이 여정 메시지에 통합되고 메시지가 최신 업데이트와 일관되게 표시됩니다.

* 오퍼를 만들고 관리하는 방법에 대한 자세한 내용은 [이 섹션](../offers/get-started/starting-offer-decisioning.md)을 참조하세요.
* 오퍼를 구성하고 의사 결정에 사용하며 이 의사 결정을 전자 메일에 활용하는 방법을 보여 주는 **전체 전체 예제**&#x200B;의 경우 [이 섹션](../offers/offers-e2e.md#insert-decision-in-email)을(를) 확인하십시오.

➡️[이 비디오에서 오퍼를 개인화로 추가하는 방법을 알아봅니다](#video-offers)

## 이메일에 결정 삽입 {#insert-offers}

>[!CAUTION]
>
>시작하기 전에 [오퍼 결정을 정의](../offers/offer-activities/create-offer-activities.md)해야 합니다.

이메일 메시지에 결정을 삽입하려면 아래 단계를 수행합니다.

1. 이메일을 만든 다음 이메일 Designer 를 열어 콘텐츠를 구성합니다.

1. **[!UICONTROL 오퍼 결정]** 콘텐츠 구성 요소를 추가합니다.

   ![](assets/deliver-offer-component.png)

   [이 섹션](content-components.md)에서 콘텐츠 구성 요소를 사용하는 방법을 알아봅니다.

1. **[!UICONTROL 오퍼 결정]** 탭이 오른쪽 팔레트에 표시됩니다. **[!UICONTROL 오퍼 결정 선택]**&#x200B;을 클릭합니다.

   1. 표시되는 창에서 표시할 오퍼에 해당하는 배치를 선택합니다.

      [배치](../offers/offer-library/creating-placements.md)는 오퍼를 표시하는 데 사용되는 컨테이너입니다. 이 예제에서는 &quot;이메일 상단 이미지&quot; 배치를 사용합니다. 이 배치는 메시지 상단에 있는 이미지 유형 오퍼를 표시하기 위해 오퍼 라이브러리에 만들어졌습니다.

   1. 선택한 배치 표시와 일치하는 의사 결정 콘텐츠 구성 요소에서 사용할 결정을 선택한 다음 **[!UICONTROL 추가]**&#x200B;를 클릭합니다.

      >[!NOTE]
      >
      >선택한 배치와 호환되는 결정만 목록에 표시됩니다. 이 예에서는 하나의 오퍼 활동만 &quot;이메일 상단 이미지&quot; 배치와 일치합니다.

      ![](assets/deliver-offer-placement.png)

이제 결정이 구성 요소에 추가됩니다. 변경 사항을 저장하면 메시지를 여정의 일부로 보낼 때 관련 프로필에 오퍼를 표시할 수 있습니다.

>[!NOTE]
>
>메시지에 직접 또는 간접적으로 참조되는 오퍼, 대체 오퍼, 오퍼 컬렉션 또는 오퍼 결정을 업데이트하면 해당 메시지에 업데이트가 자동으로 반영됩니다.

## 이메일에서 오퍼 미리 보기 {#preview-offers-in-email}

**[!UICONTROL 오퍼]** 섹션 또는 콘텐츠 구성 요소 화살표를 사용하여 전자 메일에 추가된 결정의 일부인 다른 오퍼를 미리 볼 수 있습니다.

![](assets/deliver-offer-preview.png)

고객 프로필과 함께 결정의 일부인 다른 오퍼를 표시하려면 아래 단계를 따르십시오.

1. 오퍼를 미리 보는 데 사용할 테스트 프로필을 선택하십시오.

   1. **[!UICONTROL 콘텐츠 시뮬레이션 단추]** 단추를 클릭한 다음 **[!UICONTROL ID 네임스페이스]** 필드에서 테스트 프로필을 식별하는 데 사용할 네임스페이스를 선택하십시오.

      >[!NOTE]
      >
      >이 예제에서는 **Email** 네임스페이스를 사용합니다. 이 섹션[&#128279;](../audience/get-started-identity.md)에서 Adobe Experience Platform ID 네임스페이스 에 대해 자세히 알아보세요.

   1. **[!UICONTROL ID 값]** 필드에 테스트 프로필을 식별할 값을 입력하십시오. 이 예에서는 테스트 프로필의 이메일 주소를 입력합니다.

   <!--For example enter smith@adobe.com and click the **[!UICONTROL Add profile]** button.-->

   1. 프로필 데이터에 따라 메시지의 다양한 변형을 테스트할 수 있도록 다른 프로필을 추가합니다.

      ![](assets/deliver-offer-test-profiles.png)

1. **[!UICONTROL 미리 보기]** 탭을 클릭하여 메시지를 테스트한 다음 테스트 프로필을 선택합니다. 선택한 프로필(여성)에 해당하는 오퍼가 표시됩니다.

   ![](assets/deliver-offer-test-profile-female-preview.png)

   다른 테스트 프로필을 선택하여 메시지의 각 변형에 대한 이메일 콘텐츠를 미리 볼 수 있습니다. 이제 메시지 콘텐츠에 선택한 테스트 프로필에 해당하는 오퍼(이제 남자)가 표시됩니다.

[이 섹션](#preview-your-messages)에서 메시지 미리 보기를 확인하는 자세한 단계에 대해 자세히 알아보세요.

## 사용 방법 비디오{#video-offers}

[!DNL Journey Optimizer]의 메시지에 의사 결정 관리 구성 요소를 추가하는 방법을 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/3415690?quality=12&captions=kor)
