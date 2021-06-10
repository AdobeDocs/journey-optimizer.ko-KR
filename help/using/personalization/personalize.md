---
title: Journey Optimizer에서 콘텐츠 개인화
description: 개인화 시작
source-git-commit: 8c58dd667ea59a17833bbe3482b1a233ac2e28fe
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 49%

---

# 개인화 시작{#add-personalization}

![](../assets/do-not-localize/badge.png)

여정 최적화 개인화 기능을 살펴보고 그에 대한 데이터 및 정보를 활용하여 특정 수신자에게 메시지를 반영합니다. 그것은 그의 이름, 그의 관심, 그가 사는 곳, 그가 산 것 등이 될 수 있습니다.

Journey Optimizer에서는 중괄호 **{}**&#x200B;로 묶은 내용을 포함하는 식을 만들 수 있도록 하는 Handlebars를 기반으로 한 **인라인** 단순 개인화 구문을 사용합니다. 동일한 콘텐츠 또는 필드에 제한 없이 여러 식을 추가할 수 있습니다. 자세한 내용은 [개인화 구문](personalization-syntax.md)을 참조하십시오.

개인화는 Adobe Experience Platform에 정의된 **XDM 개인 프로필** 스키마에서 관리하는 프로필 데이터를 기반으로 합니다. 자세한 내용은 [Adobe XDM(Experience Platform Data Model) 설명서](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko)를 참조하십시오.

>[!CAUTION]
>**XDM 개별 프로필** 스키마는 Journey Optimizer에서 컨텐츠를 개인화하는 데 사용할 수 있는 유일한 스키마입니다.

**예:**

```
Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}

Hello {{profile.person.gender}} {{profile.person.name.fullName}}
```

메시지(전자 메일 및 푸시)를 처리할 때 Journey Optimizer은 표현식을 Experience Cloud 플랫폼 데이터베이스에 포함된 데이터로 대체합니다.

```
Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}} becomes “Hello John Doe”.
```
