---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer에서 콘텐츠 개인화
description: 개인화를 시작합니다.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Beginner
keywords: 표현식, 편집기, 시작, 개인화
exl-id: f448780b-91bc-455e-bf10-9a9aee0a0b24
source-git-commit: 8a1ec5acef067e3e1d971deaa4b10cffa6294d75
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 35%

---

# 개인화 시작{#add-personalization}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card5"
>title="개인화 경험"
>abstract="**Adobe Journey Optimizer**&#x200B;를 사용하면 수신자에 대한 데이터와 정보를 활용하여 각 수신자에 맞게 메시지를 적응할 수 있습니다. 이는 이름, 관심사, 거주지, 구입한 제품 등이 될 수 있습니다."

[!DNL Adobe Journey Optimizer] 개인 설정 기능을 통해 해당 데이터와 정보를 활용하여 각 받는 사람에게 메시지를 적용할 수 있습니다. 이는 이름, 관심사, 거주지, 구입한 제품 등이 될 수 있습니다.

➡️[이 비디오에서 메시지를 개인화하는 방법을 알아보세요](#video-perso)
➡️[개인화를 활용하는 사용 사례 살펴보기](personalization-use-case.md)

## 전용 구문을 사용하여 개인화 표현식 작성 {#syntax}

[!DNL Journey Optimizer]에서는 중괄호 **{{}}**&#x200B;로 묶은 내용을 포함하는 식을 만들 수 있는 Handlebars를 기반으로 한 **inline** 단순 개인화 구문을 사용합니다. 동일한 콘텐츠 또는 필드에 제한 없이 여러 식을 추가할 수 있습니다. [개인화 구문에 대해 자세히 알아보세요](personalization-syntax.md).

**예:**

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`
* `Hello {{profile.person.name.fullName}}`

메시지(전자 메일 및 푸시)를 처리할 때 Journey Optimizer은 표현식을 Experience Platform 데이터베이스에 포함된 데이터로 바꿉니다. `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`이(가) &quot;Hello John Doe&quot;가 됩니다.

## 프로필 데이터를 활용하여 메시지 개인화 {#data}

개인화는 Adobe Experience Platform에 정의된 **XDM 개인 프로필** 스키마에서 관리하는 프로필 데이터를 기반으로 합니다. 자세한 내용은 [XDM(Adobe Experience Platform 데이터 모델) 설명서](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko){target="_blank"}를 참조하세요.

>[!CAUTION]
>**XDM 개인 프로필** 스키마는 [!DNL Journey Optimizer]에서 콘텐츠를 개인화하는 데 사용할 수 있는 유일한 스키마입니다.

또한 **계산된 특성**&#x200B;을 활용하여 콘텐츠를 개인화할 수도 있습니다. 계산된 특성은 Adobe Experience Platform에 수집된 프로필 사용 경험 이벤트 데이터 세트를 기반으로 하며, 개별 행동 이벤트를 요약하는 고객 프로필 내에 저장된 집계된 데이터 포인트 역할을 합니다. [계산된 특성을 사용하여 작업하는 방법을 알아봅니다.](../audience/computed-attributes.md)

## 개인화 편집기 작업 {#editor}

[!DNL Journey Optimizer]은(는) 콘텐츠에 대한 사용자 지정된 개인 맞춤화를 만들기 위해 모든 데이터를 선택하고, 정렬하고, 사용자 지정하고, 유효성을 검사할 수 있는 개인 맞춤화 편집기를 제공합니다. felper 함수, 사전 정의된 표현식 라이브러리, 속성 즐겨찾기 등과 같은 몇 가지 도구를 사용하여 개인화 콘텐츠를 작성할 수 있습니다.

* [개인화 편집기 작업 방법 알아보기](personalization-build-expressions.md)
* [개인화를 수행할 수 있는 위치를 알아보세요](personalization-contexts.md).

## 방법 비디오{#video-perso}

여정에서 얻은 컨텍스트 기반 이벤트 정보를 사용하여 메시지를 개인화하는 방법을 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

메시지에 프로필 기반 개인 맞춤화를 추가하는 방법과 개인 맞춤화 블록의 전제 조건으로 대상자 멤버십을 사용하는 방법에 대해 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)

