---
title: Journey Optimizer에서 콘텐츠 개인화
description: 개인화 시작.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Beginner
exl-id: f448780b-91bc-455e-bf10-9a9aee0a0b24
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 25%

---

# 개인화 시작{#add-personalization}

검색 [!DNL Adobe Journey Optimizer] 개인화 기능은 보유한 데이터 및 정보를 활용하여 특정 수신자에게 메시지를 조정할 수 있는 기능을 제공합니다. 그들의 이름, 관심, 그들이 사는 곳, 그들이 산 것 등이 될 수 있습니다.

➡️ [이 비디오에서 메시지를 개인화하는 방법을 알아봅니다](#video-perso)
➡️ [개인화를 활용하는 활용 사례 검색](personalization-use-case.md)

## 전용 구문을 사용하여 개인화 표현식 작성 {#syntax}

[!DNL Journey Optimizer] 사용 **인라인** 중괄호로 둘러싸인 컨텐츠로 표현식을 만들 수 있는 Handlebars를 기반으로 한 단순 개인화 구문 **{{}}**. 동일한 콘텐츠 또는 필드에 제한 없이 여러 식을 추가할 수 있습니다. 추가 정보 [개인화 구문](personalization-syntax.md).

**예:**

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`
* `Hello {{profile.person.name.fullName}}`

메시지(전자 메일 및 푸시)를 처리할 때 Journey Optimizer은 표현식을 Experience Platform 데이터베이스에 포함된 데이터로 대체합니다.  `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` 은 &quot;Hello John Doe&quot;가 됩니다.

## 프로필 데이터를 활용하여 메시지 개인화 {#data}

개인화는 Adobe Experience Platform에 정의된 **XDM 개인 프로필** 스키마에서 관리하는 프로필 데이터를 기반으로 합니다. 추가 정보 [Adobe Experience Platform 데이터 모델(XDM) 설명서](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko){target=&quot;_blank&quot;}.

>[!CAUTION]
>다음 **XDM 개별 프로필** 스키마는에서 컨텐츠를 개인화하는 데 사용할 수 있는 유일한 스키마입니다 [!DNL Journey Optimizer].

## 다른 컨텍스트에서 개인화 추가 {#contexts}

[!DNL Journey Optimizer] 에서는 콘텐츠를 개인화하고 여러 가지 방법으로 메시지 표시를 표시할 수 있습니다. 에서 개인화를 수행할 수 있는 컨텍스트에 대해 자세히 알아보십시오 [이 섹션](personalization-contexts.md).

## 표현식 편집기 작업 {#editor}

[!DNL Journey Optimizer] 은 컨텐츠에 대한 사용자 지정된 개인화를 만들기 위해 모든 데이터를 선택, 정렬, 사용자 지정 및 유효성 검사하여 사용할 표현식 편집기를 제공합니다.

개인화 컨텐츠(도우미 함수, 사전 정의된 표현식 라이브러리, 속성 즐겨찾기..)를 만드는 데 도움이 되는 몇 가지 도구를 사용할 수 있습니다.

추가 정보 [!DNL Journey Optimizer] 표현식 편집기 [이 섹션](personalization-build-expressions.md)

## 방법 비디오{#video-perso}

여정에서 얻은 컨텍스트 기반 이벤트 정보를 사용하여 메시지를 개인화하는 방법을 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

여정에서 얻은 컨텍스트 기반 이벤트 정보를 사용하여 메시지를 개인화하는 방법을 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)
