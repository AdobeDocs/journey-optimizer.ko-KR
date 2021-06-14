---
title: 개인화된 오퍼 추가
description: 메시지에 개인화된 오퍼를 추가하는 방법을 알아봅니다
feature: 여정
topic: 콘텐츠 관리
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 4%

---

# 개인화된 오퍼 추가 {#deliver-personalized-offers}

![](assets/do-not-localize/badge.png)

## 의사 결정 관리 정보 {#about-offer-decisioning}

[!DNL Journey Optimizer] 을 사용하면 고객에게 제공할 최상의 오퍼를 선택하기 위해 오퍼 결정 엔진을 활용할 이메일 메시지 결정(이전에 오퍼 활동이라고 함)에 을 삽입할 수 있습니다.

예를 들어 이메일에 수신자의 충성도 수준에 따라 달라지는 특별 할인 오퍼가 표시되는 결정을 추가할 수 있습니다.

오퍼를 만들고 관리하는 방법에 대한 자세한 내용은 [이 섹션](offers/get-started/starting-offer-decisioning.md)을 참조하십시오.

## 전자 메일 {#insert-offers}에 결정 삽입

전자 메일 메시지에 의사 결정을 삽입하려면 아래 단계를 따르십시오.

1. 이메일을 만든 다음 이메일 디자이너를 열어 콘텐츠를 구성합니다.

1. **[!UICONTROL Offer decision]** 컨텐츠 구성 요소를 추가합니다( [컨텐츠 구성 요소 사용](content-components.md) 참조).

   ![](assets/deliver-offer-component.png)

1. **[!UICONTROL Offer decision]** 탭이 구성 요소에 추가됩니다. **[!UICONTROL Add personalization - Offer decision]** 을 클릭하여 오퍼 활동을 추가합니다.

   ![](assets/deliver-offer-tab.png)

1. 표시할 오퍼에 해당하는 배치를 선택합니다.

   배치는 오퍼를 표시하는 데 사용되는 컨테이너입니다. 이 예에서는 &quot;이메일 상단 이미지&quot; 배치를 사용합니다. 이 배치는 메시지 상단에 있는 이미지 유형 오퍼를 표시하기 위해 오퍼 라이브러리에 생성되었습니다.

1. 컨텐츠 구성 요소에서 사용할 오퍼 활동을 선택한 다음, **[!UICONTROL Add]** 을 클릭합니다.

   >[!NOTE]
   >
   >선택한 배치와 호환되는 결정만 목록에 표시됩니다. 이 예제에서 한 개의 오퍼 활동만 &quot;이메일 상단 이미지&quot; 배치와 일치합니다.

   ![](assets/deliver-offer-placement.png)

1. 이제 오퍼 활동이 구성 요소에 추가됩니다. **[!UICONTROL Offers]** 섹션이나 컨텐츠 구성 요소 화살표를 사용하여 의사 결정의 일부인 다른 오퍼를 미리 볼 수 있습니다.

   ![](assets/deliver-offer-preview.png)
