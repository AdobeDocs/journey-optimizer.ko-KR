---
title: Journey Optimizer에서 콘텐츠 개인화
description: 개인화 시작.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Beginner
exl-id: f448780b-91bc-455e-bf10-9a9aee0a0b24
source-git-commit: 68407db81224e9c2b6930c800e57b65e081781fe
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 38%

---

# 개인화 시작{#add-personalization}

검색 [!DNL Adobe Journey Optimizer] 개인화 기능은 보유한 데이터 및 정보를 활용하여 특정 수신자에게 메시지를 조정할 수 있는 기능을 제공합니다. 그들의 이름, 관심, 그들이 사는 곳, 그들이 산 것 등이 될 수 있습니다.

➡️ [이 비디오에서 메시지를 개인화하는 방법을 알아봅니다](#video-perso)

[!DNL Journey Optimizer] 사용 **인라인** 중괄호로 둘러싸인 컨텐츠로 표현식을 만들 수 있는 Handlebars를 기반으로 한 단순 개인화 구문 **{{}}**. 동일한 콘텐츠 또는 필드에 제한 없이 여러 식을 추가할 수 있습니다. 추가 정보 [개인화 구문](personalization-syntax.md).

개인화는 Adobe Experience Platform에 정의된 **XDM 개인 프로필** 스키마에서 관리하는 프로필 데이터를 기반으로 합니다. 추가 정보 [Adobe Experience Platform 데이터 모델(XDM) 설명서](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko){target=&quot;_blank&quot;}.

>[!CAUTION]
>다음 **XDM 개별 프로필** 스키마는에서 컨텐츠를 개인화하는 데 사용할 수 있는 유일한 스키마입니다 [!DNL Journey Optimizer].

**예:**

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`

* `Hello {{profile.person.name.fullName}}`

메시지(전자 메일 및 푸시)를 처리할 때 Journey Optimizer은 표현식을 Experience Cloud 플랫폼 데이터베이스에 포함된 데이터로 대체합니다.  `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` 은 &quot;Hello John Doe&quot;가 됩니다.

## 방법 비디오{#video-perso}

여정에서 얻은 컨텍스트 기반 이벤트 정보를 사용하여 메시지를 개인화하는 방법을 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

여정에서 얻은 컨텍스트 기반 이벤트 정보를 사용하여 메시지를 개인화하는 방법을 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)
