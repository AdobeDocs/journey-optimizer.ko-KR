---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer에서 콘텐츠 개인화
description: 개인화 시작.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Beginner
keywords: 표현식, 편집기, 시작, 개인화
exl-id: f448780b-91bc-455e-bf10-9a9aee0a0b24
source-git-commit: f0a7f785a84cb53be0319284a4886841f6974e3d
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 25%

---

# 개인화 시작{#add-personalization}

검색 [!DNL Adobe Journey Optimizer] 관련된 데이터 및 정보를 활용하여 메시지를 각 특정 수신자에게 적용하는 개인화 기능. 이름, 관심사, 사는 곳, 산 물건 등이 될 수 있다.

➡️ [다음 비디오에서는 메시지를 개인화하는 방법을 알아봅니다](#video-perso)
➡️ [개인화를 활용하는 사용 사례 살펴보기](personalization-use-case.md)

## 전용 구문을 사용하여 개인화 표현식 작성 {#syntax}

[!DNL Journey Optimizer] 다음 사용: **인라인** 중괄호로 묶은 내용이 포함된 표현식을 만들 수 있는 Handlebars를 기반으로 한 단순 개인화 구문 **{{}}**. 동일한 콘텐츠 또는 필드에 제한 없이 여러 식을 추가할 수 있습니다. 다음에서 자세히 알아보기 [개인화 구문](personalization-syntax.md).

**예:**

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`
* `Hello {{profile.person.name.fullName}}`

메시지(이메일 및 푸시)를 처리할 때 Journey Optimizer은 표현식을 Experience Platform 데이터베이스에 포함된 데이터로 대체합니다.  `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` 는 &quot;Hello John Doe&quot;가 됩니다.

## 프로필 데이터를 활용하여 메시지 개인화 {#data}

개인화는 Adobe Experience Platform에 정의된 **XDM 개인 프로필** 스키마에서 관리하는 프로필 데이터를 기반으로 합니다. 다음에서 자세히 알아보기 [Adobe Experience Platform 데이터 모델(XDM) 설명서](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko){target="_blank"}.

>[!CAUTION]
>다음 **XDM 개별 프로필** 스키마는 콘텐츠를 개인화하는 데 사용할 수 있는 유일한 스키마입니다. [!DNL Journey Optimizer].

또한 **계산된 속성** 을 클릭하여 콘텐츠를 개인화할 수 있습니다. 계산된 속성은 Adobe Experience Platform에 수집된 프로필 사용 경험 이벤트 데이터 세트를 기반으로 하며 개별 행동 이벤트를 요약하는 고객 프로필 내에 저장된 집계된 데이터 포인트 역할을 합니다 [계산된 속성으로 작업하는 방법 알아보기](../audience/computed-attributes.md)

## 다른 컨텍스트에서 개인화 추가 {#contexts}

[!DNL Journey Optimizer] 에서는 여러 가지 방법으로 메시지 콘텐츠와 표시를 개인화할 수 있습니다. 에서 개인화를 수행할 수 있는 컨텍스트에 대해 자세히 알아보십시오 [이 섹션](personalization-contexts.md).

## 표현식 편집기 작업 {#editor}

[!DNL Journey Optimizer] 는 모든 데이터를 선택, 정렬, 사용자 지정 및 확인하여 콘텐츠에 대한 사용자 지정된 개인화를 만들 수 있는 표현식 편집기를 제공합니다.

개인화 콘텐츠를 작성하는 데 도움이 되는 몇 가지 도구(도우미 함수, 사전 정의된 표현식 라이브러리, 속성 즐겨찾기...)를 사용할 수 있습니다.

자세히 알아보기 [!DNL Journey Optimizer] 표현식 편집기 [이 섹션](personalization-build-expressions.md)

## 방법 비디오{#video-perso}

여정에서 얻은 컨텍스트 기반 이벤트 정보를 사용하여 메시지를 개인화하는 방법을 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

메시지에 프로필 기반 개인 맞춤화를 추가하는 방법과 개인 맞춤화 블록의 전제 조건으로 대상자 멤버십을 사용하는 방법에 대해 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)
