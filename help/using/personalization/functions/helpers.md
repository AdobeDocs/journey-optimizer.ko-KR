---
title: 도우미
description: 도우미
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: b08dc0f8-c85f-4aca-85eb-92dc76b0e588
source-git-commit: b08f996d9871f59665c2d329b493fd6e61030fac
workflow-type: tm+mt
source-wordcount: '616'
ht-degree: 6%

---

# 도우미 {#gs-helpers}

## 기본 대체 값{#default-value}

`Default Fallback Value` 도우미는 특성이 비어 있거나 null인 경우 기본 대체 값을 반환하는 데 사용됩니다. 이 메커니즘은 프로필 속성 및 여정 이벤트에 대해 작동합니다.

**구문**

```sql
Hello {%=profile.personalEmail.name.firstName ?: "there" %}!
```

이 예제에서는 이 프로필의 `there` 특성이 비어 있거나 null인 경우 값 `firstName`이(가) 표시됩니다.

## 조건{#if-function}

`if` 도우미는 조건부 블록을 정의하는 데 사용됩니다.
표현식 계산이 true를 반환하면 블록이 렌더링되고 그렇지 않으면 건너뜁니다.

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

1. **조건부 표현식을 기반으로 다른 스토어 링크 렌더링**

   ```sql
   {%#if profile.homeAddress.countryCode = "FR"%}
   <a href="https://www.somedomain.com/fr">Consultez notre catalogue</a>
   {%else%}
   <a href="https://www.somedomain.com/en">Checkout our catalogue</a>
   {%/if%}
   ```

1. **전자 메일 주소 확장 확인**

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

1. **대상자 멤버십을 기반으로 하는 조건부 콘텐츠**

   ```sql
   {%#if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8b").status = "existing"%}
   Hi! Esteemed gold member. <a href="https://www.somedomain.com/gold">Checkout your exclusive perks </a>
   {%else%} if 'profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"'%}
   Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
   {%/if%}
   ```

>[!NOTE]
>
>대상자 및 세분화 서비스에 대한 자세한 내용은 [이 섹션](../../audience/about-audiences.md)을 참조하세요.


## Unless{#unless}

`unless` 도우미는 조건부 블록을 정의하는 데 사용됩니다. `if` 헬퍼와 반대로 식 계산이 false를 반환하는 경우 블록이 렌더링됩니다.

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

## Each{#each}

`each` 도우미는 배열을 반복하는 데 사용됩니다.
도우미의 구문은 ```{{#each ArrayName}}``` YourContent {{/each}}입니다.
블록 내에서 **this** 키워드를 사용하여 개별 배열 항목을 참조할 수 있습니다. {{@index}}을(를) 사용하여 배열 요소의 인덱스를 렌더링할 수 있습니다.

**구문**

```sql
{{#each profile.productsInCart}}
    <li>{{this.name}}</li>
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
{{/each}}
```

## With{#with}

`with` 도우미는 템플릿 부분의 평가 토큰을 변경하는 데 사용됩니다.

**구문**

```sql
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

`with` 도우미는 바로 가기 변수를 정의하는 데에도 유용합니다.

**예**

긴 변수 이름을 짧은 변수 이름으로 앨리어싱하려면 와 함께 사용합니다.

```sql
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```

## Let{#let}

`let` 함수를 사용하면 나중에 쿼리에서 사용할 변수로 식을 저장할 수 있습니다.

**구문**

```sql
{% let variable = expression %} {{variable}}
```

**예**

다음 예에서는 장바구니에 있는 제품의 가격 합계를 100에서 1000 사이로 계산할 수 있습니다.

```sql
{% let sum = 0%}
    {{#each profile.productsInCart as |p|}}
        {%#if p.price>100 and p.price<1000%}
            {%let sum = sum + p.price %}
        {%/if%}
    {{/each}}
{{sum}}
```

## 실행 메타데이터 {#execution-metadata}

>[!AVAILABILITY]
>
>이 기능은 제한적으로 이용할 수 있습니다. 액세스 권한을 얻으려면 Adobe 담당자에게 문의하십시오.

`executionMetadata` 도우미를 통해 사용자 지정 키-값 쌍을 동적으로 캡처하고 메시지 실행 컨텍스트에 저장할 수 있습니다.

**구문**

```
{{executionMetadata key="your_key" value="your_value"}}
```

이 구문에서 `key`은(는) 메타데이터 이름을 참조하며 `value`은(는) 유지할 메타데이터입니다.

**사용 사례**

이 함수를 사용하면 캠페인 또는 여정의 모든 기본 작업에 컨텍스트 정보를 추가할 수 있습니다. 이렇게 하면 추적, 분석, 개인화 및 다운스트림 처리와 같은 다양한 목적을 위해 실시간 게재 컨텍스트 데이터를 외부 시스템으로 내보낼 수 있습니다.

>[!NOTE]
>
>실행 메타데이터 함수는 [사용자 지정 작업](../../action/action.md)에서 지원되지 않습니다.

예를 들어 실행 메타데이터 도우미를 사용하여 각 프로필로 전송된 각 게재에 특정 ID를 추가할 수 있습니다. 이 정보는 런타임 중에 생성되며, 그런 다음 외부 보고 플랫폼과의 다운스트림 조정을 위해 보강된 실행 메타데이터를 내보낼 수 있습니다.

**작동 방식**

캠페인 또는 여정 내의 채널 콘텐츠에서 요소를 선택하고 개인화 편집기를 사용하여 이 요소에 `executionMetadata` 도우미를 추가하십시오.

>[!NOTE]
>
>컨텐츠 자체가 표시되면 실행 메타데이터 기능이 표시되지 않습니다.


런타임 시 메타데이터 값이 다음 스키마를 추가하여 기존 **[!UICONTROL 메시지 피드백 이벤트 데이터 세트]**&#x200B;에 추가됩니다.

```
"_experience": {
  "customerJourneyManagement": {
    "messageExecution": {
      "metadata": {
        "your_key": "your_value"
      }
    }
  }
}
```

>[!NOTE]
>
>[이 섹션](../../data/get-started-datasets.md)의 데이터 세트에 대해 자세히 알아보세요.

**제한**

작업당 키 값 쌍에는 2kb의 상한이 있습니다.

2Kb 제한을 초과하는 경우 메시지가 계속 전달되지만 키 값 쌍은 잘릴 수 있습니다.

**예**

```
{{executionMetadata key="firstName" value=profile.person.name.firstName}}
```

이 예에서 `profile.person.name.firstName` = &quot;Alex&quot;라고 가정하면 결과 엔터티는 다음과 같습니다.

```
{
  "key": "firstName",
  "value": "Alex"
}
```

