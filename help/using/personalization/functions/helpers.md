---
title: 도우미
description: 도우미
feature: 개인화
topic: 개인화
role: Data Engineer
level: Experienced
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 4%

---


# 도우미 {#gs-helpers}

## 조건{#if-function}

`if` 도우미는 조건부 블록을 정의하는 데 사용됩니다.
표현식 평가가 true를 반환하는 경우 블록이 렌더링되지 않으면 무시됩니다.

**구문**

```sql
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Check out this link</a>
```

`if` 도우미 다음에 `else` 문을 입력하여 동일한 조건이 false인 경우 실행할 코드 블록을 지정할 수 있습니다.
`elseif` 문은 첫 번째 문이 false를 반환하는 경우 테스트할 새 조건을 지정합니다.


**형식**

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

1. **조건부 표현식을 기반으로 다른 저장소 링크 렌더링**

   ```sql
   {%#if profile.homeAddress.countryCode = "FR"%}
   <a href="https://www.somedomain.com/fr">Consultez notre catalogue</a>
   {%else%}
   <a href="https://www.somedomain.com/en">Checkout our catalogue</a>
   {%/if%}
   ```

1. **이메일 주소 확장 결정**

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

   다음 작업에서는 &#39;www.adobe.com/academia&#39; 웹 사이트(&#39;.edu&#39; 전자 메일 주소가 있는 프로필의 경우), &#39;www.adobe.com/org&#39; 웹 사이트(&#39;.org&#39; 전자 메일 주소가 있는 프로필의 경우) 및 기타 모든 프로필에 대한 기본 URL &#39;www.adobe.com/users&#39;&#39; 링크를 추가합니다.

   ```sql
   {%#if contains(profile.personalEmail.address, ".edu")%}
   <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
   {%else if contains(profile.personalEmail.address, ".org")%}
   <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
   {%else%}
   <a href="https://www.adobe.com/users">Checkout our page</a>
   {%/if%}
   ```

1. **세그먼트 멤버십 기반의 조건부 콘텐츠**

   ```sql
   {%#if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8b").status = "existing"%}
   Hi! Esteemed gold member. <a href="https://www.somedomain.com/gold">Checkout your exclusive perks </a>
   {%else%} if 'profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"'%}
   Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
   {%/if%}
   ```

1. **프로필이 이미 구성원인지 확인**

   ```sql
   {%#if profile.segmentMembership.get(segments.`123e4567-e89b-12d3-a456-426614174000`.id)%}
       You're a member!
   {%else%}
       You should be a member! Sign up now!
   {%/if%}
   ```

>[!NOTE]
>
>세그멘테이션 및 세그멘테이션 서비스에 대한 자세한 내용은 이 [섹션](../../segment/about-segments.md)을 참조하십시오.


## 그렇지 않은 경우{#unless}

`unless` 도우미는 조건부 블록을 정의하는 데 사용됩니다. `if` 도우미 대신 표현식 평가가 false를 반환하는 경우 블록이 렌더링됩니다.

**구문**

```sql
{%#unless unlessCondition%} element_1 {%else%} default_element {%/unless%}
```

**예**

전자 메일 주소 확장을 기반으로 일부 콘텐츠를 렌더링합니다.

```sql
{%#unless endsWith(profile.personalEmail.address, ".edu")%}
Some Normal Content
{%else%}
Some edu specific content Content
{%/unless%}
```

## 각{#each}

`each` 도우미는 배열을 반복하는 데 사용됩니다.
도우미 구문은 ```{{#each ArrayName}}``` YourContent {{/each}}입니다.
블록 내의 **this** 키워드를 사용하여 개별 배열 항목을 참조할 수 있습니다. {{@index}}을(를) 사용하여 배열 요소의 인덱스를 렌더링할 수 있습니다.

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

장바구니에 있는 제품 목록을 렌더링합니다.

```sql
{{#each profile.products as |product|}}
    <li>{{product.productName}} {{product.productRating}}</li>
   </br>
{{/each}}
```

## 사용{#with}

`with` 도우미는 템플릿 부품의 평가 토큰을 변경하는 데 사용됩니다.

**구문**

```sql
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

`with` 도우미는 바로 가기 변수를 정의하는 데에도 유용합니다.

**예**

긴 변수 이름을 짧은 이름으로 앨리어싱하는 데 을 사용합니다.

```sql
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```

## Let{#let}

`let` 함수를 사용하면 표현식을 변수로 저장하여 나중에 쿼리에서 사용할 수 있습니다.

**구문**

```sql
{% let variable = expression %} {{variable}}
```

**예**

다음 예에서는 합계가 $100보다 크고 $1000보다 작은 USD의 트랜잭션과 함께 모든 제품 합계를 사용할 수 있습니다.

```sql
{% let variable = expression %} {{variable}}
```
