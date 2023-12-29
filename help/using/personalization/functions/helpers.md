---
title: 도우미
description: 도우미
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: b08dc0f8-c85f-4aca-85eb-92dc76b0e588
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 4%

---

# 도우미 {#gs-helpers}

## 기본 대체 값{#default-value}

다음 `Default Fallback Value` 속성이 비어 있거나 null인 경우 도우미가 기본 대체 값을 반환하는 데 사용됩니다. 이 메커니즘은 프로필 속성 및 여정 이벤트에 대해 작동합니다.

**구문**

```sql
Hello {%=profile.personalEmail.name.firstName ?: "there" %}!
```

이 예에서 값은 `there` 다음 경우에 표시됩니다. `firstName` 이 프로필의 속성이 비어 있거나 null입니다.

## 조건{#if-function}

다음 `if` 헬퍼를 사용하여 조건부 블록을 정의합니다.
표현식 계산이 true를 반환하면 블록이 렌더링되고 그렇지 않으면 건너뜁니다.

**구문**

```sql
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Check out this link</a>
```

팔로우 중 `if` 도우미에서 다음을 입력할 수 있습니다. `else` 동일한 조건이 false인 경우 실행할 코드 블록을 지정하는 문입니다.
다음 `elseif` 문은 첫 번째 문이 false를 반환하는 경우 테스트할 새 조건을 지정합니다.


**포맷**

```sql
{
    {
        {%#if condition1%} element_1 
        {%else if condition2%} element_2 
        {%else%} default_element 
        {%/if%}
    }
}
```

**예**

1. **조건부 표현식을 기반으로 다양한 스토어 링크 렌더링**

   ```sql
   {%#if profile.homeAddress.countryCode = "FR"%}
   <a href="https://www.somedomain.com/fr">Consultez notre catalogue</a>
   {%else%}
   <a href="https://www.somedomain.com/en">Checkout our catalogue</a>
   {%/if%}
   ```

1. **이메일 주소 확장 확인**

   ```sql
   {%#if contains(profile.personalEmail.address, ".edu")%}
   <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
   {%else if contains(profile.personalEmail.address, ".org")%}
   <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
   {%else%}
   <a href="https://www.adobe.com/users">Checkout our page</a>
   {%/if%}
   ```

1. **조건부 링크 추가**

   다음 작업을 수행하면 이메일 주소가 &#39;.edu&#39;인 프로필에 대한 &#39;www.adobe.com/academia&#39; 웹 사이트&#39;, 이메일 주소가 &#39;.org&#39;인 프로필에 대한 &#39;www.adobe.com/org&#39; 웹 사이트&#39; 및 기타 모든 프로필에 대한 기본 URL &#39;www.adobe.com/users&#39;에 링크가 추가됩니다.

   ```sql
   {%#if contains(profile.personalEmail.address, ".edu")%}
   <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
   {%else if contains(profile.personalEmail.address, ".org")%}
   <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
   {%else%}
   <a href="https://www.adobe.com/users">Checkout our page</a>
   {%/if%}
   ```

1. **대상자 멤버십을 기반으로 한 조건부 콘텐츠**

   ```sql
   {%#if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8b").status = "existing"%}
   Hi! Esteemed gold member. <a href="https://www.somedomain.com/gold">Checkout your exclusive perks </a>
   {%else%} if 'profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"'%}
   Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
   {%/if%}
   ```

>[!NOTE]
>
>대상자 및 세분화 서비스에 대한 자세한 내용은 다음을 참조하십시오. [섹션](../../audience/about-audiences.md).


## Unless{#unless}

다음 `unless` 헬퍼를 사용하여 조건부 블록을 정의합니다. 에 대한 반대로 `if`  도우미, 표현식 계산에서 false를 반환하면 블록이 렌더링됩니다.

**구문**

```sql
{%#unless unlessCondition%} element_1 {%else%} default_element {%/unless%}
```

**예**

이메일 주소 확장을 기반으로 일부 콘텐츠 렌더링:

```sql
{%#unless endsWith(profile.personalEmail.address, ".edu")%}
Some Normal Content
{%else%}
Some edu specific content Content
{%/unless%}
```

## 각{#each}

다음 `each` helper는 배열을 반복하는 데 사용됩니다.
헬퍼의 구문은 다음과 같습니다. ```{{#each ArrayName}}``` 귀하의 콘텐츠 {{/each}}
키워드를 사용하여 개별 배열 항목을 참조할 수 있습니다 **이** 블록 안에요 를 사용하여 배열 요소의 인덱스를 렌더링할 수 있습니다. {{@index}}.

**구문**

```sql
{{#each profile.productsInCart}}
    <li>{{this.name}}</li>
    </br>
{{/each}}
```

**예**

```sql
{{#each profile.homeAddress.city}}
  {{@index}} : {{this}}<br>
{{/each}}
```

**예**

이 사용자가 장바구니에 보유한 제품 목록을 렌더링합니다.

```sql
{{#each profile.products as |product|}}
    <li>{{product.productName}} {{product.productRating}}</li>
   </br>
{{/each}}
```

## 포함{#with}

다음 `with` helper를 사용하여 템플릿 부분의 평가 토큰을 변경합니다.

**구문**

```sql
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

다음 `with` 도우미는 바로 가기 변수를 정의하는 데에도 유용합니다.

**예**

긴 변수 이름을 짧은 변수 이름으로 앨리어싱하려면 와 함께 사용합니다.

```sql
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```

## Let{#let}

다음 `let` 함수를 사용하면 표현식을 나중에 쿼리에서 사용할 변수로 저장할 수 있습니다.

**구문**

```sql
{% let variable = expression %} {{variable}}
```

**예**

다음 예에서는 거래와 함께 제품 합계의 모든 합계를 USD로 사용할 수 있습니다. 여기서 합계는 $100보다 크고 $1000보다 작습니다.

```sql
{% let variable = expression %} {{variable}}
```
