---
title: 개인화 구문
description: 개인화 구문을 사용하는 방법 학습
translation-type: tm+mt
source-git-commit: 568b37f0bbcb663cf7062f26b90d57d89452e862
workflow-type: tm+mt
source-wordcount: '718'
ht-degree: 2%

---

# 개인화 구문 {#personalization-syntax}

![](../assets/do-not-localize/badge.png)

## 소개

Journey Optimizer의 개인화는 Handlebars라는 템플릿 구문을 기반으로 합니다.
Handlebars 구문에 대한 전체 설명은 [HandlebarsJS](https://handlebarsjs.com/)를 참조하십시오.

템플릿 및 입력 객체를 사용하여 HTML 또는 기타 텍스트 형식을 생성합니다. handlebars 템플릿은 포함된 핸들바 표현식이 있는 일반 텍스트와 같습니다.

간단한 표현식 샘플:

```
{{profile.person.name}}
```

where:

* **profileis** 는 네임스페이스입니다.
* **person.** name은 속성으로 구성된 토큰입니다. 특성 구조는 Adobe Experience Platform XDM 스키마에 정의되어 있습니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko).

## 구문 일반 규칙

식별자는 다음을 제외하고 유니코드 문자일 수 있습니다.

```
Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
```

구문은 대/소문자를 구분합니다.

**true**, **false**, **null** 및 **undefined**&#x200B;이라는 단어는 경로 식의 첫 부분에서만 사용할 수 있습니다.

Handlebars에서 {{expression}}에서 반환되는 값은 **HTML-escaped**&#x200B;입니다. 표현식에 &amp;가 포함되어 있으면 반환된 HTML 이스케이프 출력이 &amp;로 생성됩니다. 핸들바가 가치를 이탈하지 않도록 하려면 &quot;3중 은폐&quot;를 사용하십시오.

## 프로필

이 네임스페이스를 통해 [Adobe Experience Platform 데이터 모델(XDM) 설명서](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html)에 설명된 프로필 스키마에 정의된 모든 특성을 참조할 수 있습니다.

Journey Optimizer 개인화 블록에서 참조하기 전에 스키마에서 속성을 정의해야 합니다.

모든 참조는 유효성 검사 메커니즘이 [here](personalization-validation.md)에 설명된 프로필 스키마에 대해 유효성이 검사됩니다.

**샘플 참조:**

* ```{{profile.person.name.fullName}}```
* ```{{profile.person.name.firstName}}```
* ```{{profile.person.gender}}```
* ```{{profile.personalEmail.address}}```
* ```{{profile.mobilePhone.number}}```
* ```{{profile.homeAddress.city}}```
* ```{{profile.faxPhone.number}}```

**이메일 주소 확장** 결정:

```
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
{%else if contains(profile.personalEmail.address, ".org")%}
<a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
{%else%}
<a href="https://www.adobe.com/users">Checkout our page</a>
{%/if%}
```

## 세그먼트

세그멘테이션 및 세그멘테이션 서비스에 대한 자세한 내용은 이 [섹션](../segment/about-segments.md)을 참조하십시오.

**세그먼트 멤버십에 따라 다른 컨텐츠를 렌더링합니다**.

```
{%#if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8b").status = "existing"%}
  Hi! Esteemed gold member. <a href="https://www.somedomain.com/gold">Checkout your exclusive perks </a>
{%else%} if 'profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"'%}
  Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
{%/if%}
```

**프로파일이 이미 멤버인지** 확인:

```
{%#if profile.segmentMembership.get(segments.`123e4567-e89b-12d3-a456-426614174000`.id)%}
    You're a member!
{%else%}
    You should be a member! Sign up now!
{%/if%}
```

## 제공

이 네임스페이스를 사용하면 기존 오퍼 결정을 참조할 수 있습니다.
오퍼를 참조하려면 오퍼를 정의하는 다른 정보로 경로를 선언해야 합니다.

이 경로는 다음과 같은 구조를 가집니다.
0 - &#39;오퍼&#39; :offer 네임스페이스에 속하는 경로 표현식을 식별합니다.
1 - 유형:오퍼 표현 유형을 결정합니다. 유효한 값은 &#39;image&#39;, &#39;html&#39; 및 &#39;text&#39;입니다.
2 - 배치 ID
3 - 활동 ID
4 - 특정 속성을 제공합니다. 오퍼 유형에 따라 지원되는 속성을 사용할 수 있습니다. 예: `deliveryUrl` 이미지.

결정 API에 대한 자세한 내용은 이 [페이지](https://experienceleague.adobe.com/docs/offer-decisioning/using/api-reference/offer-delivery/deliver-offers.html?lang=en#deliver-offers-using-the-decisions-api)를 참조하십시오.

오퍼 표현에 대한 자세한 내용은 이 [페이지](https://experienceleague.adobe.com/docs/offer-decisioning/using/api-reference/offer-delivery/deliver-offers.html?lang=en#accept-and-content-type-headers)를 참조하십시오.

모든 참조는 [here](personalization-validation.md)에 설명된 유효성 검사 메커니즘을 사용하여 오퍼 스키마에 대해 검증됩니다.

**샘플 참조:**

* 이미지가 호스팅되는 위치:

```offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].deliveryUrl```

* 이미지를 클릭할 때 Target URL:

```offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].linkUrl```

* 의사 결정 엔진에서 제공되는 오퍼의 텍스트 컨텐츠:

```offers.text.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content```

* 의사 결정 엔진에서 오는 오퍼의 HTML 컨텐츠:

```offers.html.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content```


## 도움말 사용자

Handlebars 도우미는 매개 변수 뒤에 올 수 있는 간단한 식별자입니다.
각 매개 변수는 Handlebars 표현식입니다. 이러한 도움말은 템플릿의 모든 컨텍스트에서 액세스할 수 있습니다.

이러한 블록 도우미는 도우미 이름 앞에 #로 식별되며 같은 이름의 닫기 / 와 일치해야 합니다.
블록은 블록 열기({{# }})와 닫기({/}})가 있는 표현식입니다.

### If

조건 블록을 정의하는 데 **if** 도우미가 사용됩니다.
표현식 평가가 true를 반환하면 블록이 렌더링되지 않으면 무시됩니다.

```
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Check out this link</a>
```

**if** 도우미 다음에 **else** 문을 입력하여 동일한 조건이 false인 경우 실행할 코드 블록을 지정할 수 있습니다.
첫 번째 문이 false를 반환할 경우 테스트할 새 조건을 **else if** 문에서 지정합니다.

**조건부 표현식을 기반으로 다른 스토어 링크를 렌더링합니다**.

```
{%#if profile.homeAddress.countryCode = "FR"%}
  <a href="https://www.somedomain.com/fr">Consultez notre catalogue</a>
{%else%}
  <a href="https://www.somedomain.com/en">Checkout our catalogue</a>
{%/if%}
```

### 그렇지 않은 경우

**#** unlesshelper는 조건부 블록을 정의하는 데 사용됩니다. **#if** 도우미의 반대로 표현식 평가가 false를 반환하면 블록이 렌더링됩니다.

**이메일 주소 확장을 기반으로 일부 컨텐츠 렌더링**:

```
{%#unless endsWith(profile.personalEmail.address, ".edu")%}
Some Normal Content
{%else%}
Some edu specific content Content
{%/unless%}
```

### 각

**각** 도우미는 배열을 반복하는 데 사용됩니다.
도우미의 구문은 ```{{#each ArrayName}}``` YourContent {{/each}}입니다.
블록 내에 있는 키워드 **this**&#x200B;를 사용하여 개별 배열 항목을 참조할 수 있습니다. {{@index}}을(를) 사용하여 배열 요소의 인덱스를 렌더링할 수 있습니다.

예:

```
{{#each profile.productsInCart}}
    <li>{{this.name}}</li>
    </br>
{{/each}}
```

```
{{#each profile.homeAddress.city}}
  {{@index}} : {{this}}<br>
{{/each}}
```

**이 사용자가 장바구니에 가지고 있는 제품 목록을 렌더링합니다**.

```
{{#each profile.products as |product|}}
    <li>{{product.productName}} {{product.productRating}}</li>
   </br>
{{/each}}
```

### 사용

**#with** 도우미는 템플릿 부분의 평가 토큰을 변경하는 데 사용됩니다.

예:

```
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

**#with** 도우미는 단축키 변수를 정의하는 데에도 유용합니다.

**긴 변수 이름을 짧은 이름으로 앨리어싱하는 데 사용합니다**.

```
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```


## 제한 사항

* 개인화 식에는 **xEvent** 변수를 사용할 수 없습니다. xEvent에 대한 참조가 있으면 유효성 검사가 실패합니다.
