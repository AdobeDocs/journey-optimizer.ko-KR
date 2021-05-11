---
title: Journey Optimizer에서 컨텐츠 개인화
description: 개인화 시작하기
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 5%

---

# 시작하기 {#add-personalization}

![](../assets/do-not-localize/badge.png)

개인화는 Journey Optimizer의 컨텍스트에서 사용자에 대한 데이터와 정보를 활용하여 특정 가입자에게 메시지를 타깃팅하는 작업입니다. 그것은 그의 이름, 그의 관심, 그가 사는 곳 등이 될 수 있다.

Journey Optimizer에서는 중괄호 **{}**&#x200B;로 묶은 내용을 포함하는 표현식을 만들 수 있도록 하는 핸들바를 기반으로 한 **인라인** 단순 개인화 구문을 사용합니다. 동일한 컨텐츠 또는 필드에 제한 없이 여러 표현식을 추가할 수 있습니다. [개인화 구문](personalization-syntax.md)을 참조하십시오.

개인화는 Adobe Experience Platform에 정의된 **XDM 개인 프로필** 스키마에서 관리되는 프로필 데이터를 기반으로 합니다. 자세한 내용은 [Adobe Experience Platform 데이터 모델(XDM) 설명서](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko)을 참조하십시오.

>[!CAUTION]
>**XDM 개별 프로필** 스키마는 Journey Optimizer에서 컨텐츠를 개인화하는 데 사용할 수 있는 유일한 스키마입니다.

**예**

```
Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}

Hello {{profile.person.gender}} {{profile.person.name.fullName}}
```

**메시지 처리**(전자 메일 및 푸시) 동안 표현식은 Experience Cloud 플랫폼 데이터베이스에 포함된 데이터로 바뀝니다.

```
Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}} becomes “Hello John Doe”.
```
