---
solution: Journey Optimizer
product: journey optimizer
title: 컨텍스트 기반 데이터 반복
description: Handlebars 구문을 사용하여 다양한 컨텍스트 소스에서 배열을 반복하는 방법에 대해 알아봅니다
feature: Personalization
topic: Personalization
role: Developer
level: Intermediate
hide: true
hidefromtoc: true
keywords: 표현식, 편집기, 핸들바, 반복, 배열, 컨텍스트, 개인화
source-git-commit: f51334a0d1fd5669a057c17a6991d556b08db94a
workflow-type: tm+mt
source-wordcount: '2666'
ht-degree: 0%

---

# 컨텍스트 기반 데이터 반복 {#personalization-contexts}

Handlebars 반복 구문을 사용하여 이벤트, 사용자 지정 작업 응답 및 기타 상황별 데이터를 포함하여 메시지에 있는 다양한 소스의 동적 데이터 목록을 표시하는 방법에 대해 알아봅니다.

## 개요 {#overview}

Journey Optimizer에서는 [메시지 개인화](personalize.md) 동안 여러 소스의 컨텍스트 데이터에 액세스할 수 있습니다. 기본 채널([email](../email/get-started-email-design.md), [push](../push/create-push.md), [SMS](../sms/create-sms.md))의 Handlebars 구문을 사용하여 이러한 원본에서 배열을 반복하여 제품 목록, 권장 사항 또는 기타 반복 요소와 같은 동적 콘텐츠를 표시할 수 있습니다.

**사용 가능한 컨텍스트 원본:**

* **[이벤트](#event-data)**: 여정 이벤트(비즈니스 이벤트, 단일 이벤트)의 데이터
* **[사용자 지정 작업 응답](#custom-action-responses)**: 사용자 지정 작업을 통해 외부 API 호출에서 반환된 데이터입니다
* **[데이터 세트 조회](#dataset-lookup)**: Adobe Experience Platform 데이터 세트에서 검색된 보강된 데이터
* **[기술 속성](#technical-properties)**: 여정 ID 및 보조 식별자와 같은 여정 메타데이터
* **[여정 컨텍스트](#other-contexts)**: 실행 중에 액세스할 수 있는 기타 여정 관련 데이터

이 안내서에서는 메시지의 각 소스에서 배열을 반복하는 방법과 여정 활동을 구성할 때 배열을 사용하는 방법을 보여 줍니다. 메시지 개인화 기본 사항을 이해하려면 [Handlebars 반복 구문](#syntax)으로 시작하거나, 사용자 지정 작업 및 데이터 세트 조회에 배열 데이터를 전달하는 방법을 알아보려면 [여정 식에서 배열 작업](#arrays-in-journeys)으로 이동하십시오.

## Handlebars 반복 구문 {#syntax}

Handlebars는 배열을 반복하도록 `{{#each}}` [helper](functions/helpers.md)을(를) 제공합니다. 기본 구문은 입니다.

```handlebars
{{#each arrayPath as |item|}}
  <!-- Access item properties here -->
  {{item.property}}
{{/each}}
```

**주요 사항:**

* `arrayPath`을(를) 배열 데이터의 경로로 바꿉니다.
* `item`을(를) 원하는 변수 이름으로 바꾸십시오(예: `product`, `response`, `element`).
* `{{item.propertyName}}`을(를) 사용하여 각 항목의 속성에 액세스
* 다중 수준 배열에 대해 여러 `{{#each}}` 블록을 중첩할 수 있습니다.

## 이벤트 데이터 반복 {#event-data}

이벤트 데이터는 여정이 [event](../event/about-events.md)에 의해 트리거될 때 사용할 수 있습니다. 장바구니 콘텐츠, 주문 항목 또는 양식 제출과 같이, 여정이 시작된 시점에 캡처된 데이터를 표시하는 데 유용합니다.

>[!TIP]
>
>이벤트 데이터를 다른 소스와 결합할 수 있습니다. 예제는 [여러 컨텍스트 소스 결합](#combine-sources)을 참조하십시오.

### 이벤트에 대한 컨텍스트 경로

```handlebars
context.journey.events.<event_ID>.<fieldPath>
```

* `<event_ID>`: 여정에 구성된 이벤트의 고유 ID
* `<fieldPath>`: 이벤트 스키마 내의 필드 또는 배열에 대한 경로

### 예: 이벤트의 장바구니 항목

[이벤트 스키마](../event/experience-event-schema.md)에 `productListItems` 배열(표준 [XDM 형식](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/product-list-item.html){target="_blank"})이 포함된 경우 아래 샘플에 자세히 설명된 대로 장바구니 콘텐츠를 표시할 수 있습니다.

+++ 예제 코드 보기

```handlebars
{{#each context.journey.events.event_ID.productListItems as |product|}}
  <div class="product">
    <h3>{{product.name}}</h3>
    <p>Quantity: {{product.quantity}}</p>
    <p>Price: ${{product.priceTotal}}</p>
  </div>
{{/each}}
```

+++

### 예: 이벤트의 중첩된 배열

중첩된 구조의 경우 중첩된 `{{#each}}` 블록을 사용합니다.

+++ 예제 코드 보기

```handlebars
{{#each context.journey.events.event_ID.categories as |category|}}
  <h2>{{category.name}}</h2>
  <ul>
    {{#each category.items as |item|}}
      <li>{{item.title}}</li>
    {{/each}}
  </ul>
{{/each}}
```

+++

[모범 사례](#best-practices)의 중첩에 대해 자세히 알아보세요.

## 사용자 지정 작업 응답 반복 {#custom-action-responses}

[사용자 지정 작업](../action/about-custom-action-configuration.md) 응답에는 외부 API 호출에서 반환된 데이터가 포함되어 있습니다. 충성도 포인트, 제품 권장 사항, 재고 상태 또는 개인화된 오퍼와 같은 시스템의 실시간 정보를 표시하는 데 유용합니다.

>[!NOTE]
>
>이 기능을 사용하려면 사용자 지정 작업을 응답 페이로드로 구성해야 합니다. 자세한 내용은 [이 섹션](../action/action-response.md#config-response)을 참조하세요. 사용자 지정 작업 응답을 이벤트 데이터 또는 데이터 세트 조회와 결합할 수도 있습니다. 예를 보려면 [여러 컨텍스트 소스 결합](#combine-sources)을 참조하십시오.

### 사용자 지정 작업에 대한 컨텍스트 경로

```handlebars
context.journey.actions.<actionName>.<fieldPath>
```

* `<actionName>`: 여정에 구성된 [사용자 지정 작업](../action/about-custom-action-configuration.md)의 이름
* `<fieldPath>`: 응답 페이로드 내의 필드 또는 배열에 대한 경로

### 예: API의 제품 권장 사항

사용자 지정 작업 API 호출에서 반환된 제품 권장 사항을 표시하려면 아래 예를 참조하십시오.

+++ 예제 코드 보기

**API 응답:**

```json
{
  "recommendations": [
    {
      "productId": "12345",
      "productName": "Summer Jacket",
      "price": 89.99,
      "imageUrl": "https://example.com/jacket.jpg"
    },
    {
      "productId": "67890",
      "productName": "Running Shoes",
      "price": 129.99,
      "imageUrl": "https://example.com/shoes.jpg"
    }
  ]
}
```

**메시지 개인화:**

```handlebars
<h2>Recommended for You</h2>
<div class="recommendations">
  {{#each context.journey.actions.GetRecommendations.recommendations as |item|}}
    <div class="product-card">
      <img src="{{item.imageUrl}}" alt="{{item.productName}}" />
      <h3>{{item.productName}}</h3>
      <p class="price">${{item.price}}</p>
    </div>
  {{/each}}
</div>
```

+++

### 예: 사용자 지정 작업의 중첩된 배열

사용자 지정 작업에서 반환된 중첩된 배열(예: 제품이 있는 범주)을 반복하려면 아래 예를 참조하십시오.

+++ 예제 코드 보기

**API 응답:**

```json
{    
  "id": "84632848268632",    
  "responses": [
    { "productIDs": [1111, 2222, 3333] },
    { "productIDs": [4444, 5555, 6666] },
    { "productIDs": [7777, 8888, 9999] }
  ]
}
```

**메시지 개인화:**

```handlebars
<h2>Product Groups</h2>
{{#each context.journey.actions.GetProducts.responses as |response|}}
  <div class="product-group">
    <ul>
      {{#each response.productIDs as |productID|}}
        <li>Product ID: {{productID}}</li>
      {{/each}}
    </ul>
  </div>
{{/each}}
```

+++

더 복잡한 중첩 패턴은 [모범 사례](#best-practices)를 참조하세요.

### 예: 충성도 계층의 이점

충성도 상태에 따라 동적 이점을 표시하려면 아래 예를 참조하십시오.

+++ 예제 코드 보기

**API 응답:**

```json
{
  "loyaltyTier": "gold",
  "benefits": [
    { "name": "Free shipping", "icon": "truck" },
    { "name": "20% discount", "icon": "percent" },
    { "name": "Priority support", "icon": "headset" }
  ]
}
```

**메시지 개인화:**

```handlebars
<h2>Your {{context.journey.actions.GetLoyaltyInfo.loyaltyTier}} Member Benefits</h2>
<ul class="benefits">
  {{#each context.journey.actions.GetLoyaltyInfo.benefits as |benefit|}}
    <li>
      <span class="icon-{{benefit.icon}}"></span>
      {{benefit.name}}
    </li>
  {{/each}}
</ul>
```

+++

## 데이터 세트 조회 결과 반복 {#dataset-lookup}

[데이터 세트 조회 활동](../building-journeys/dataset-lookup.md)을 사용하면 여정 런타임 동안 [Adobe Experience Platform 데이터 세트](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=ko){target="_blank"}에서 데이터를 검색할 수 있습니다. 보강된 데이터는 배열로 저장되며 메시지에서 반복될 수 있습니다.

>[!AVAILABILITY]
>
>데이터 세트 조회 활동은 제한된 조직 세트에만 사용할 수 있습니다. 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.

[이 섹션](../building-journeys/dataset-lookup.md)에서 데이터 집합 조회 활동을 구성하는 방법에 대해 자세히 알아보세요. 데이터 집합 조회는 이벤트 데이터와 결합할 때 특히 유용합니다. 실제 사용 사례는 [예: 데이터 집합 조회로 보강된 이벤트 데이터](#combine-sources)를 참조하십시오.

### 데이터 세트 조회를 위한 컨텍스트 경로

```handlebars
context.journey.datasetLookup.<activityID>.entities
```

* `<activityID>`: 데이터 세트 조회 활동의 고유 ID
* `entities`: 데이터 집합에서 검색된 보강된 데이터의 배열

### 예: 데이터 세트의 제품 세부 정보

데이터 세트 조회 활동을 사용하여 SKU를 기반으로 제품 정보를 검색하는 경우 아래 샘플을 참조하십시오.

+++ 예제 코드 보기

**데이터 집합 조회 구성:**

* 조회 키: `list(@event{purchase_event.products.sku})`
* 반환할 필드: `["SKU", "category", "price", "name"]`

**메시지 개인화:**

```handlebars
<h2>Product Details</h2>
<table>
  <thead>
    <tr>
      <th>Product Name</th>
      <th>Category</th>
      <th>Price</th>
    </tr>
  </thead>
  <tbody>
    {{#each context.journey.datasetLookup.3709000.entities as |product|}}
      <tr>
        <td>{{product.name}}</td>
        <td>{{product.category}}</td>
        <td>${{product.price}}</td>
      </tr>
    {{/each}}
  </tbody>
</table>
```

+++

### 예: 데이터 세트 데이터를 사용하여 필터링된 반복

데이터 세트 조회 결과를 반복할 때 특정 범주의 제품만 필터링하고 표시하려면 아래 예를 참조하십시오.

+++ 예제 코드 보기

```handlebars
<h2>Household Products</h2>
{{#each context.journey.datasetLookup.3709000.entities as |product|}}
  {{#if product.category = "household"}}
    <div class="product">
      <h3>{{product.name}}</h3>
      <p>Price: ${{product.price}}</p>
    </div>
  {{/if}}
{{/each}}
```

+++

[모범 사례](#best-practices)에서 조건부 필터링에 대해 자세히 알아보세요.

### 예: 데이터 세트 조회에서 합계 계산

데이터 세트 조회 결과를 반복하면서 합계를 계산하고 표시하려면 아래 예를 참조하십시오.

+++ 예제 코드 보기

```handlebars
{% let householdTotal = 0 %}
{{#each context.journey.datasetLookup.3709000.entities as |product|}}
  {%#if product.category = "household"%}
    {% let householdTotal = householdTotal + product.price %}
  {%/if%}
{{/each}}

<p>Your household products total: ${{householdTotal}}</p>
```

+++

## 여정 기술 속성 사용 {#technical-properties}

여정 기술 속성은 여정 ID 및 보조 식별자와 같은 여정 실행에 대한 메타데이터에 대한 액세스를 제공합니다. 이러한 기능은 특히 특정 여정 인스턴스를 기반으로 하는 배열 필터링에 대해 반복 패턴과 결합할 때 유용할 수 있습니다.

### 사용 가능한 기술 속성

```handlebars
context.journey.technicalProperties.journeyUID
context.journey.technicalProperties.supplementalId
```

### 예: 보조 식별자를 사용하여 배열 항목 필터링

배열이 있는 이벤트 트리거 여정에서 보조 식별자를 사용할 때 현재 여정 인스턴스에 대한 관련 항목만 표시하도록 필터링할 수 있습니다. [이 안내서](../building-journeys/supplemental-identifier.md)에서 보조 식별자에 대해 자세히 알아보세요.

**시나리오**: 여정이 여러 예약으로 트리거되었지만 이 여정 인스턴스를 트리거한 특정 예약(보조 ID로 식별됨)에 대한 정보만 표시하려고 합니다.

+++ 예제 코드 보기

```handlebars
{{#each context.journey.events.event_ID.bookingList as |booking|}}
  {%#if booking.bookingInfo.bookingNum = context.journey.technicalProperties.supplementalId%}
    <div class="booking-details">
      <h3>Your Booking: {{booking.bookingInfo.bookingNum}}</h3>
      <p>Destination: {{booking.bookingInfo.bookingCountry}}</p>
      <p>Date: {{booking.bookingInfo.bookingDate}}</p>
    </div>
  {%/if%}
{{/each}}
```

+++

### 예: 추적할 여정 ID 포함

추적을 위해 메시지에 여정 ID를 포함하려면 아래 예를 참조하십시오.

+++ 예제 코드 보기

```handlebars
<footer>
  <p>Journey Reference: {{context.journey.technicalProperties.journeyUID}}</p>
</footer>
```

+++

## 여러 컨텍스트 소스 결합 {#combine-sources}

동일한 메시지에 다른 소스의 데이터를 결합하여 풍부하고 개인화된 경험을 만들 수 있습니다. 이 섹션에서는 여러 컨텍스트 소스를 함께 사용하는 실제 예를 보여줍니다.

결합할 수 있는 **컨텍스트 원본:**

* [이벤트 데이터](#event-data) + [사용자 지정 작업 응답](#custom-action-responses)
* [이벤트 데이터](#event-data) + [데이터 집합 조회](#dataset-lookup)
* [여러 원본](#combine-sources) + [기술 속성](#technical-properties)

### 예: 실시간 재고가 있는 장바구니 항목

이벤트 데이터(장바구니 컨텐츠)를 사용자 지정 작업 데이터(인벤토리 상태)와 결합하려면 아래 샘플을 보십시오.

+++ 예제 코드 보기

```handlebars
<h2>Your Cart</h2>
{{#each context.journey.events.cartEvent.productListItems as |product|}}
  <div class="cart-item">
    <h3>{{product.name}}</h3>
    <p>Quantity: {{product.quantity}}</p>
    <p>Price: ${{product.priceTotal}}</p>
  </div>
{{/each}}

<h2>We Also Recommend</h2>
{{#each context.journey.actions.GetRecommendations.items as |recommendation|}}
  <div class="recommendation">
    <h4>{{recommendation.name}}</h4>
    <p>${{recommendation.price}}</p>
    {{#if recommendation.inStock}}
      <span class="badge">In Stock</span>
    {{else}}
      <span class="badge out-of-stock">Out of Stock</span>
    {{/if}}
  </div>
{{/each}}
```

+++

### 예: 데이터 세트 조회로 보강된 이벤트 데이터

[이벤트 SKU](#event-data)를 [데이터 집합 조회](#dataset-lookup)의 자세한 제품 정보와 결합하려면 아래 샘플을 참조하세요.

+++ 예제 코드 보기

```handlebars
<h2>Your Order Details</h2>
{{#each context.journey.events.orderEvent.productListItems as |item|}}
  <div class="order-item">
    <p><strong>SKU:</strong> {{item.SKU}}</p>
    <p><strong>Quantity:</strong> {{item.quantity}}</p>
    
    <!-- Enrich with dataset lookup data -->
    {{#each context.journey.datasetLookup.1234567.entities as |enrichedProduct|}}
      {{#if enrichedProduct.SKU = item.SKU}}
        <p><strong>Product Name:</strong> {{enrichedProduct.name}}</p>
        <p><strong>Category:</strong> {{enrichedProduct.category}}</p>
        <img src="{{enrichedProduct.imageUrl}}" alt="{{enrichedProduct.name}}" />
      {{/if}}
    {{/each}}
  </div>
{{/each}}
```

+++

### 예: 여러 소스를 기술 속성과 결합

여러 컨텍스트 소스(프로필 데이터, 이벤트 데이터, 사용자 지정 작업 및 기술 속성)를 단일 메시지로 결합하려면 아래 샘플을 참조하십시오.

+++ 예제 코드 보기

```handlebars
<div class="personalized-content">
  <!-- Profile data -->
  <h1>Hello {{profile.person.name.firstName}},</h1>
  
  <!-- Event data iteration -->
  <h2>Your Recent Purchases</h2>
  {{#each context.journey.events.purchaseEvent.items as |purchase|}}
    <div class="purchase">
      <p>{{purchase.productName}} - ${{purchase.price}}</p>
    </div>
  {{/each}}
  
  <!-- Custom action response iteration -->
  <h2>Recommended for You</h2>
  {{#each context.journey.actions.GetPersonalizedRecs.recommendations as |rec|}}
    <div class="recommendation">
      <h3>{{rec.title}}</h3>
      <p>{{rec.description}}</p>
    </div>
  {{/each}}
  
  <!-- Technical properties -->
  <footer>
    <p class="fine-print">Journey ID: {{context.journey.technicalProperties.journeyUID}}</p>
  </footer>
</div>
```

+++

## 기타 컨텍스트 유형 {#other-contexts}

이 안내서는 배열 상에서의 반복에 중점을 두고 있지만, 일반적으로 반복이 필요하지 않은 개인화에는 다른 컨텍스트 유형을 사용할 수 있습니다. 루프가 아닌 직접 액세스합니다.

* **[프로필 특성](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=ko){target="_blank"}**(`profile.*`): Adobe Experience Platform의 개별 프로필 필드
* **[대상](../audience/about-audiences.md)**(`inAudience()`): 대상 멤버십 확인
* **[오퍼 결정](../offers/get-started/starting-offer-decisioning.md)**: 의사 결정 관리 오퍼
* **[타겟 특성](../orchestrated/activities/channels.md#add-personalization)**(오케스트레이션된 캠페인만 해당): 캠페인 캔버스에서 계산된 특성
* **토큰**(`context.token`): 세션 또는 인증 토큰

완벽한 개인화 구문 및 이러한 소스를 사용한 예는 다음을 참조하십시오.

* [개인화 추가](personalization-build-expressions.md)
* [개인화 구문](personalization-syntax.md)

## 여정 표현식에서 배열 작업 {#arrays-in-journeys}

이전 섹션은 Handlebars를 사용한 메시지 개인화에서 배열을 반복하는 데 중점을 두고 있지만 여정 활동을 구성할 때도 배열에서 작업합니다. 이 섹션에서는 특히 사용자 지정 작업에 데이터를 전달하거나 데이터 세트 조회가 있는 배열을 사용할 때 여정 표현식의 이벤트에서 배열 데이터를 사용하는 방법을 설명합니다.

>[!IMPORTANT]
>
>여정 표현식은 Handlebars 개인화와 다른 구문을 사용합니다. 여정 구성(사용자 지정 작업 매개 변수 또는 조건 등)에서는 [, &#x200B;](../building-journeys/expression/expressionadvanced.md), `first` 등의 함수와 함께 `all`여정 표현식 편집기`serializeList`를 사용합니다. 메시지 콘텐츠에서 `{{#each}}` 루프가 있는 Handlebars 구문을 사용합니다.

### 사용자 지정 작업 매개 변수에 배열 값 전달 {#arrays-to-custom-actions}

[사용자 지정 작업](../action/about-custom-action-configuration.md)을 구성할 때 종종 이벤트 배열에서 값을 추출하여 매개 변수로 전달해야 합니다. 이 섹션에서는 일반적인 패턴을 다룹니다.

[사용자 지정 작업 매개 변수에 컬렉션 전달](../building-journeys/collections.md#passing-collection)에 대해 자세히 알아보세요.

#### 배열에서 단일 값 추출

**사용 사례**: 이벤트 배열에서 특정 필드를 가져와 GET 요청에서 쿼리 매개 변수로 전달하십시오.

+++ 예제 코드 보기

**예제 시나리오**: 제품 목록에서 가격이 0보다 큰 첫 번째 SKU를 추출합니다.

**이벤트 스키마 예**:

```json
{
  "commerce": {
    "productListItems": [
      { "SKU": "SKU-1", "priceTotal": 10.0 },
      { "SKU": "SKU-2", "priceTotal": 0.0 },
      { "SKU": "SKU-3", "priceTotal": 20.0 }
    ]
  }
}
```

**사용자 지정 작업 구성**:

1. 사용자 지정 작업에서 `sku` 형식의 쿼리 매개 변수(예: `string`)를 구성합니다.
2. 동적 값을 허용하도록 `Variable`(으)로 표시

**작업 매개 변수의 여정 식**:

```javascript
@event{YourEventName.commerce.productListItems.first(currentEventField.priceTotal > 0).SKU}
```

**설명**:

* `@event{YourEventName}`: 여정 이벤트를 참조합니다.
* `.first(currentEventField.condition)`: 조건과 일치하는 첫 번째 배열 항목을 반환합니다.
* `currentEventField`: 반복하는 이벤트 배열의 각 항목을 나타냅니다.
* `.SKU`: 일치하는 항목에서 SKU 필드 추출
* 결과: `"SKU-1"`(작업 매개 변수에 적합한 문자열)

`first`컬렉션 관리 함수[에서 &#x200B;](../building-journeys/expression/collection-management-functions.md) 함수에 대해 자세히 알아보세요.

+++

#### 배열에서 값 목록 작성

**사용 사례**: 쿼리 매개 변수로 전달할 쉼표로 구분된 ID 목록을 만듭니다(예: `/products?ids=sku1,sku2,sku3`).

+++ 예제 코드 보기

**사용자 지정 작업 구성**:

1. 형식이 `ids`인 쿼리 매개 변수(예: `string`) 구성
2. `Variable`(으)로 표시

**여정 식**:

```javascript
serializeList(
  @event{YourEventName.commerce.productListItems.all(currentEventField.priceTotal > 0).SKU},
  ",",
  true
)
```

**설명**:

* `.all(currentEventField.condition)`: 조건과 일치하는 모든 배열 항목을 반환합니다(목록 반환).
* `currentEventField`: 반복하는 이벤트 배열의 각 항목을 나타냅니다.
* `.SKU`: SKU 값만 포함하도록 목록을 빌드합니다.
* `serializeList(list, delimiter, addQuotes)`: 목록을 문자열에 조인
   * `","`: 구분 기호로 쉼표 사용
   * `true`: 각 문자열 요소 주위에 따옴표 추가
* 결과: `"SKU-1,SKU-3"`(쿼리 매개 변수에 적합)

자세히 알아보기:

* [&#39;모든&#39;](../building-journeys/expression/collection-management-functions.md)
* [&#39;serializeList&#39;](../building-journeys/functions/list-functions.md#serializeList)

사용자 지정 작업에 대한 컬렉션 처리는 [사용자 지정 작업 매개 변수에 컬렉션 전달](../building-journeys/collections.md#passing-collection)에서 다룹니다.

+++

#### 사용자 지정 작업에 오브젝트 배열 전달

**사용 사례**: 요청 본문에 전체 개체 배열을 보냅니다(본문이 있는 POST 또는 GET).

+++ 예제 코드 보기

**요청 본문 예**:

```json
{
  "ctxt": {
    "products": [
      {
        "id": "productA",
        "name": "Product A",
        "price": 20.1,
        "color": "blue"
      }
    ]
  }
}
```

**사용자 지정 작업 구성**:

1. 요청 본문에서 `products`을(를) `listObject` 유형으로 정의합니다.
2. `Variable`(으)로 표시
3. 개체 필드 `id`, `name`, `price`, `color`을(를) 정의합니다(각각 매핑 가능함).

**여정 캔버스 구성**:

1. 고급 모드에서 컬렉션 표현식을 설정합니다.

   ```javascript
   @event{YourEventName.commerce.productListItems.all(currentEventField.priceTotal > 0)}
   ```

1. 컬렉션 매핑 UI에서:
   * `id` → `productListItems.SKU` 매핑
   * `name` → `productListItems.name` 매핑
   * `price` → `productListItems.priceTotal` 매핑
   * `color` → `productListItems.color` 매핑

Journey Optimizer은 작업 페이로드 구조와 일치하는 오브젝트의 배열을 구성합니다.

>[!NOTE]
>
>이벤트 배열을 사용하여 작업할 때 `currentEventField`을(를) 사용하여 각 항목을 참조합니다. 데이터 원본 컬렉션(Adobe Experience Platform)의 경우 `currentDataPackField`을(를) 사용합니다. 사용자 지정 작업 응답 컬렉션의 경우 `currentActionField`을(를) 사용하십시오.

[사용자 지정 작업 매개 변수에 컬렉션 전달](../building-journeys/collections.md#passing-collection)에서 자세히 알아보세요.

+++

### 데이터 세트 조회를 사용하여 배열 사용 {#arrays-with-dataset-lookup}

[데이터 집합 조회 활동](../building-journeys/dataset-lookup.md)을 사용할 때 값 배열을 조회 키로 전달하여 보강된 데이터를 검색할 수 있습니다.

**예**: 이벤트 배열의 모든 SKU에 대한 제품 세부 정보를 조회합니다.

+++ 예제 코드 보기

**데이터 집합 조회 구성**:

조회 키 필드에서 `list()`을(를) 사용하여 배열 경로를 목록으로 변환합니다.

```javascript
list(@event{purchaseEvent.productListItems.SKU})
```

이렇게 하면 데이터 세트에서 조회할 모든 SKU 값 목록이 만들어집니다. 결과는 메시지에서 반복할 수 있는 배열로 `context.journey.datasetLookup.<activityID>.entities`에 사용할 수 있습니다([데이터 집합 조회 결과 반복](#dataset-lookup) 참조).

+++

### 제한 사항 및 패턴 {#array-limitations}

여정에서 배열을 사용하여 작업할 때 다음 제한 사항에 유의하십시오.

#### 여정 플로우에서 스토리지에 대한 동적 루핑 없음

여정은 배열의 각 항목에 대해 하나의 작업 노드가 여러 번 실행되는 동적 루프를 만들 수 없습니다. 이는 폭주하는 성능 문제를 방지하기 위한 의도입니다.

**수행할 수 없는 작업**:

* 배열 항목당 사용자 지정 작업을 동적으로 한 번 실행
* 배열 길이에 따라 여러 여정 분기 만들기

**대신 권장 패턴**:

1. **한 번에 모든 항목 보내기**: 전체 배열 또는 serialize된 목록을 모든 항목을 처리하는 단일 사용자 지정 작업에 전달합니다. [배열에서 값 목록 만들기](#arrays-to-custom-actions)를 참조하십시오.

2. **외부 집계 사용**: 외부 API에서 여러 ID를 수락하고 결합된 결과를 한 번의 호출로 반환하도록 합니다.

3. **AEP에서 미리 계산**: [계산된 특성](../audience/computed-attributes.md)을 사용하여 프로필 수준에서 배열의 값을 미리 계산합니다.

4. **단일 값 추출**: 하나의 값만 필요한 경우 `first` 또는 `head`을(를) 사용하여 추출하십시오. [배열에서 단일 값 추출](#arrays-to-custom-actions)을 참조하십시오.

자세한 내용은 [보호 기능 및 제한 사항](../start/guardrails.md)을 참조하세요.

#### 어레이 크기 고려 사항

대용량 스토리지는 여정 성능에 영향을 미칠 수 있습니다.

* **이벤트 배열**: 총 50KB 미만의 이벤트 페이로드를 유지합니다.
* **사용자 지정 작업 응답**: 응답 페이로드는 100KB 미만이어야 합니다.
* **데이터 집합 조회 결과**: 조회 키 및 반환된 엔터티의 수를 제한합니다.

### 전체 예: 사용자 지정 작업에 대한 이벤트 배열 {#complete-example}

다음은 사용자 지정 작업으로 이벤트 배열을 사용하는 방법을 보여 주는 전체 워크플로우입니다.

**시나리오**: 사용자가 장바구니를 중단하면 장바구니 데이터를 외부 추천 API로 전송하여 개인화된 제안을 받은 다음 전자 메일에 표시하십시오.

+++ 예제 코드 보기

**1단계: 사용자 지정 작업 구성**

사용자 지정 작업 &quot;GetCartRecommendations&quot;를 만듭니다.

* **메서드**: POST
* **URL**: `https://api.example.com/recommendations`
* **요청 본문**:

```json
{
  "cartItems": [
    {
      "sku": "string",
      "price": 0,
      "quantity": 0
    }
  ]
}
```

* `cartItems`을(를) `listObject` 및 `Variable` 유형으로 표시
* 필드 정의: `sku`(문자열), `price`(숫자), `quantity`(정수)

[사용자 지정 작업 구성](../action/about-custom-action-configuration.md)에서 자세히 알아보세요.

**2단계: 응답 페이로드 구성**

사용자 지정 작업에서 응답을 구성합니다.

```json
{
  "recommendations": [
    {
      "productId": "string",
      "productName": "string",
      "price": 0,
      "imageUrl": "string"
    }
  ]
}
```

[API 호출 응답 사용](../action/action-response.md)에서 자세히 알아보세요.

**3단계: 여정에서 작업을 전송함**

1. 장바구니 포기 이벤트 후에 사용자 지정 작업을 추가합니다.
1. `cartItems` 컬렉션의 고급 모드에서 다음을 수행합니다.

   ```javascript
   @event{cartAbandonment.commerce.productListItems.all(currentEventField.quantity > 0)}
   ```

1. 컬렉션 필드를 매핑합니다.
   * `sku` → `productListItems.SKU`
   * `price` → `productListItems.priceTotal`
   * `quantity` → `productListItems.quantity`

**4단계: 전자 메일에 있는 응답 사용**

이메일 콘텐츠에서 권장 사항을 반복합니다.

```handlebars
<h2>We noticed you left these items in your cart</h2>
{{#each context.journey.events.cartAbandonment.productListItems as |item|}}
  <div class="cart-item">
    <p>{{item.name}} - Quantity: {{item.quantity}}</p>
  </div>
{{/each}}

<h2>You might also like</h2>
{{#each context.journey.actions.GetCartRecommendations.recommendations as |rec|}}
  <div class="recommendation">
    <img src="{{rec.imageUrl}}" alt="{{rec.productName}}" />
    <h3>{{rec.productName}}</h3>
    <p>${{rec.price}}</p>
  </div>
{{/each}}
```

**5단계: 구성을 테스트합니다**

라이브 여정을 실행하기 전에 작업 구성에서 &quot;테스트 요청 보내기&quot; 기능을 사용하여 사용자 지정 작업을 테스트하여 빌드된 요청 및 값을 확인합니다.

1. [여정 테스트 모드 사용](../building-journeys/testing-the-journey.md)
2. `productListItems` 배열을 포함하는 샘플 이벤트 데이터로 트리거
3. 사용자 지정 작업에서 올바른 배열 구조를 수신하는지 확인합니다.
4. [작업 테스트 로그](../action/action-response.md#test-mode-logs) 확인
5. 이메일을 미리 확인하여 두 스토리지가 올바르게 표시되는지 확인

[사용자 지정 작업 문제 해결](../action/troubleshoot-custom-action.md)에서 자세히 알아보세요.

+++

## 모범 사례 {#best-practices}

컨텍스트 기반 데이터를 반복하여 유지 관리가 가능하고 성능이 좋은 개인화를 만들 때 다음 모범 사례를 따르십시오.

### 설명 변수 이름 사용

반복하고 있는 내용을 명확하게 나타내는 변수 이름을 선택하십시오. 이렇게 하면 코드를 보다 읽기 쉽고 유지 관리하기 쉽습니다. [개인화 구문](personalization-syntax.md)에 대해 자세히 알아보기:

+++ 예제 코드 보기

```handlebars
<!-- Good -->
{{#each products as |product|}}
{{#each users as |user|}}
{{#each recommendations as |recommendation|}}

<!-- Less clear -->
{{#each items as |item|}}
{{#each array as |element|}}
```

+++

### 빈 배열 처리

배열이 비어 있을 때 대체 콘텐츠를 제공하려면 `{{else}}` 절을 사용하십시오. [도우미 함수](functions/helpers.md)에 대해 자세히 알아보세요.

+++ 예제 코드 보기

```handlebars
{{#each context.journey.actions.GetRecommendations.items as |item|}}
  <div>{{item.name}}</div>
{{else}}
  <p>No recommendations available at this time.</p>
{{/each}}
```

+++

### 조건부 도우미와 결합

조건부 콘텐츠에 대해 루프 내에서 `{{#if}}`을(를) 사용합니다. [조건부 규칙](create-conditions.md)에 대해 자세히 알아보고 [사용자 지정 작업 응답](#custom-action-responses) 및 [데이터 집합 조회](#dataset-lookup) 섹션에서 예제를 참조하십시오.

+++ 예제 코드 보기

```handlebars
{{#each context.journey.actions.GetProducts.items as |product|}}
  <div class="product">
    <h3>{{product.name}}</h3>
    {{#if product.onSale}}
      <span class="badge">On Sale!</span>
    {{/if}}
    {{#if product.newArrival}}
      <span class="badge">New</span>
    {{/if}}
  </div>
{{/each}}
```

+++

### 성능에 대한 반복 제한

대용량 배열의 경우 반복 횟수를 제한하는 것이 좋습니다.

+++ 예제 코드 보기

```handlebars
<!-- Display only first 5 items -->
{{#each context.journey.actions.GetProducts.items as |product|}}
  {{#if @index < 5}}
    <div>{{product.name}}</div>
  {{/if}}
{{/each}}
```

+++

### 배열 메타데이터 액세스

Handlebars는 고급 반복 패턴에 도움이 되는 루프 내의 특수 변수를 제공합니다.

* `@index`: 현재 반복 인덱스(0 기반)
* `@first`: 첫 번째 반복에 대해 True
* `@last`: 마지막 반복에 대해 True

+++ 예제 코드 보기

```handlebars
{{#each products as |product|}}
  <div class="product {{#if @first}}featured{{/if}}">
    {{@index}}. {{product.name}}
  </div>
{{/each}}
```

+++

>[!NOTE]
>
>이러한 Handlebars 변수(`@index`, `@first`, `@last`)는 메시지 개인화의 `{{#each}}` 루프 내에서만 사용할 수 있습니다. 여정 식에서 배열을 사용하여 작업하려면(예: 사용자 지정 작업으로 전달하기 전에 배열에서 첫 번째 항목을 가져오는 경우) [`head`](../personalization/functions/arrays-list.md#head), [`first`](../building-journeys/expression/collection-management-functions.md) 또는 [`all`](../building-journeys/expression/collection-management-functions.md)과(와) 같은 배열 함수를 사용합니다. 자세한 내용은 [여정 식에서 배열 작업](#arrays-in-journeys)을 참조하십시오.

## 문제 해결 {#troubleshooting}

반복에 문제가 있습니까? 이 섹션에서는 일반적인 문제와 해결 방법을 다룹니다.

### 배열이 표시되지 않음

**문제**: 배열 반복에 콘텐츠가 표시되지 않습니다.

+++ 가능한 원인 및 해결 방법 보기

**가능한 원인 및 해결 방법**:

1. **잘못된 경로**: 컨텍스트 원본을 기준으로 배열에 대한 정확한 경로를 확인하십시오.
   * [이벤트](#event-data)의 경우: `context.journey.events.<event_ID>.<fieldPath>`
   * [사용자 지정 작업](#custom-action-responses)의 경우: `context.journey.actions.<actionName>.<fieldPath>`
   * [데이터 집합 조회](#dataset-lookup)의 경우: `context.journey.datasetLookup.<activityID>.entities`

2. **배열이 비어 있음**: 배열에 데이터가 없는지 확인하려면 `{{else}}` 절을 추가하십시오. 예제는 [모범 사례](#best-practices)를 참조하세요.

3. **아직 데이터를 사용할 수 없음**: 여정 흐름에서 메시지 활동 전에 사용자 지정 작업, 이벤트 또는 데이터 집합 조회 활동이 실행되었는지 확인하십시오.

+++

### 구문 오류

**문제**: 식 유효성 검사가 실패하거나 메시지가 렌더링되지 않습니다.

+++ 일반적인 실수 보기

**일반적인 실수**:

* 닫는 태그가 없습니다. `{{#each}}`마다 `{{/each}}`이(가) 있어야 합니다. 올바른 구조를 보려면 [Handlebars 반복 구문](#syntax)을 검토하십시오.
* 잘못된 변수 이름: 블록 전체에서 변수 이름이 일관되게 사용되도록 합니다. 명명 규칙에 대해서는 [모범 사례](#best-practices)를 참조하십시오.
* 잘못된 경로 구분 기호: 슬래시나 다른 문자를 사용하지 않는 점(`.`)을 사용합니다.

+++

### 반복 테스트

[여정 테스트 모드](../building-journeys/testing-the-journey.md)를 사용하여 반복을 확인하세요. 이는 [사용자 지정 작업](#custom-action-responses) 또는 [데이터 집합 조회](#dataset-lookup)를 사용할 때 특히 중요합니다.

+++ 테스트 단계 보기

1. [테스트 모드](../building-journeys/testing-the-journey.md)에서 여정 시작
2. 샘플 데이터로 이벤트 또는 사용자 지정 작업 트리거
3. [메시지 미리 보기](../content-management/preview.md)를 확인하여 반복이 올바르게 표시되는지 확인하십시오.
4. 테스트 모드 로그에서 오류를 검토합니다([사용자 지정 작업 테스트 모드 로그](../action/action-response.md#test-mode-logs) 참조).

+++

## 관련 항목 {#related-topics}

**Personalization 기본 사항:** [개인화 시작](personalize.md) | [개인화 추가](personalization-build-expressions.md) | [Personalization 구문](personalization-syntax.md) | [도우미 함수](functions/helpers.md) | [조건부 규칙 만들기](create-conditions.md)

**여정 구성:** [이벤트 정보](../event/about-events.md) | [사용자 지정 작업 구성](../action/about-custom-action-configuration.md) | [사용자 지정 작업 매개 변수에 컬렉션 전달](../building-journeys/collections.md#passing-collection) | [사용자 지정 작업에서 API 호출 응답 사용](../action/action-response.md) | [사용자 지정 작업 문제 해결](../action/troubleshoot-custom-action.md) | [여정에서 Adobe Experience Platform 데이터 사용](../building-journeys/dataset-lookup.md) | [여정에서 보조 식별자 사용](../building-journeys/supplemental-identifier.md) | [보호 기능 및 제한 사항](../start/guardrails.md) | [여정 테스트](../building-journeys/testing-the-journey.md)

**여정 식 함수:** [고급 식 편집기](../building-journeys/expression/expressionadvanced.md) | [컬렉션 관리 기능](../building-journeys/expression/collection-management-functions.md)(처음, 모두, 마지막) | [목록 함수](../building-journeys/functions/list-functions.md)(serializeList, filter, sort) | [배열 함수](../personalization/functions/arrays-list.md)(head, tail)

**Personalization 사용 사례:** [장바구니 포기 전자 메일](personalization-use-case-helper-functions.md) | [주문 상태 알림](personalization-use-case.md)

**메시지 디자인:** [이메일 디자인 시작](../email/get-started-email-design.md) | [푸시 알림 만들기](../push/create-push.md) | [SMS 메시지 만들기](../sms/create-sms.md) | [콘텐츠 미리 보기 및 테스트](../content-management/preview-test.md)

