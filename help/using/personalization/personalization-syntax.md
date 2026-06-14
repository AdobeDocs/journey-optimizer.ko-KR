---
solution: Journey Optimizer
product: journey optimizer
title: 개인화 구문
description: 개인화 구문을 사용하는 방법을 알아봅니다.
feature: Personalization
topic: Personalization
role: Developer
level: Intermediate
keywords: 표현식, 편집기, 구문, 개인화
exl-id: 5a562066-ece0-4a78-92a7-52bf3c3b2eea
TQID: https://experienceleague.adobe.com/kZEw2lITdt8SMWMe-UT2vPzdoiAjB2vbItmK9zt-WJo
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: fda7be7c-b81e-42c0-95a9-616e5b893c03
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
subfeature_v2: id: ac5d9310-7772-40fb-9d78-864562e1bfd6id: e51e8901-97d9-4f7d-a835-503025a90e32
source-git-commit: 378c98d4dc9552de3eed68eda59d9917c2b56347
workflow-type: tm+mt
source-wordcount: 1325
ht-degree: 3%

---

# 개인화 구문 {#personalization-syntax}

>[!BEGINSHADEBOX]

**이 페이지에서:** 일반 규칙, 예약된 키워드, 형식 강제 적용, 사용 가능한 네임스페이스 및 모범 사례를 포함하여 Adobe Journey Optimizer의 Handlebars 및 PQL 개인화 구문에 대해 알아봅니다.

>[!ENDSHADEBOX]

[!DNL Journey Optimizer]의 Personalization은 동일한 식에서 함께 작동하는 두 개의 보조 구문을 사용합니다.

* **Handlebars**(`{{...}}`) — 프로필 특성을 렌더링하고 배열을 반복하며 호출 차단 도우미를 호출하는 데 사용됩니다. 자세한 내용은 [HandlebarsJS 설명서](https://handlebarsjs.com/)를 참조하십시오.
* **Profile Query Language(PQL)**(`{%= ... %}`) — 기본 제공 함수(예: `upperCase()`, `formatDate()`, `dateDiff()`)를 호출하고 조건식을 평가하는 데 사용됩니다.

현재 있는 컨텍스트를 이해하는 것은 런타임 오류를 방지하는 데 중요합니다. 예를들어, Handlebars가 이 함수를 PQL 식으로 계산하지 않고 도우미로 확인하려고 하므로 `{{...}}` 내부에 배치된 PQL 함수 호출이 실패합니다.

**예**

| 사용 사례 | 구문 |
|----------|--------|
| 프로필 속성 렌더링 | `{{profile.person.name.firstName}}` |
| PQL 함수 호출 | `{%= upperCase(profile.person.name.firstName) %}` |
| 조건부 블록 | `{%#if profile.loyalty.tier = "gold"%}...{%/if%}` |
| 배열 위로 루프 | `{{#each profile.orders}}...{{/each}}` |

속성 구조는 Adobe Experience Platform XDM 스키마에서 정의됩니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko-KR){target="_blank"}

>[!TIP]
>
>이러한 구문을 실제 시나리오에 적용하는 즉시 사용 가능한 표현식(날짜 형식 지정, 계산, 조건부 폴백 등)에 대해서는 **[Personalization 레서피](personalization-recipes.md)** 페이지를 참조하십시오.

## 구문 일반 규칙 {#general-rules}

* 식별자는 Handlebars 구문에 예약된 다음 특수 문자를 제외한 모든 유니코드 문자일 수 있습니다.

  ```
  Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
  ```

* 구문은 대/소문자를 구분합니다.

* **true**, **false**, **null** 및 **정의되지 않음**&#x200B;은(는) 경로 식의 첫 부분에서만 사용할 수 있습니다.

* Handlebars에서 {{expression}}이(가) 반환한 값은 **HTML 이스케이프**&#x200B;입니다. 식에 `&`이(가) 포함된 경우 반환된 HTML 이스케이프 출력은 `&amp;`(으)로 생성됩니다. Handlebars가 값을 이스케이프 처리하지 않게 하려면 &quot;triple-stash&quot;를 사용합니다.

  필드 `profile.person.name`의 값이 &quot;Mark &amp; Mary&quot;라고 가정합니다. `{{profile.person.name}}` 구문은 `Mark &amp; Mary`을(를) 표시하지만 `{{{profile.person.name}}}`은(는) `Mark & Mary`을(를) 표시합니다.

* 리터럴 함수 인수와 관련하여 템플릿 언어 파서는 이스케이프 처리되지 않은 단일 백슬래시(`\`) 기호를 지원하지 않습니다. 이 문자는 추가 백슬래시(`\`) 기호로 이스케이프해야 합니다. 예:

  `{%= regexGroup("abc@xyz.com","@(\\w+)", 1)%}`

* 문자열 값(예: JSON 출력 생성 시) 내에 **리터럴 큰따옴표**&#x200B;를 포함하려면 백슬래시(`\"`)로 이스케이프 처리하십시오.

  ```handlebars
  { "message": "Hello \"{{profile.person.name.firstName}}\"" }
  ```

  출력: `{ "message": "Hello \"John\"" }`

  또는 값 자체에 HTML으로 인코딩하지 않으려는 특수 문자가 포함되어 있는 경우 트리플 스태시 `{{{ }}}`을(를) 사용하여 이스케이프 처리되지 않은 HTML을 출력합니다.

## 예약된 키워드 {#reserved-keywords}

특정 키워드는 Profile Query Language(PQL)에서 예약되어 개인화 표현식에서 필드 또는 변수 이름으로 직접 사용할 수 없습니다. XDM 스키마에 예약된 키워드와 일치하는 이름을 가진 필드가 포함된 경우 백틱(`` ` ``)을 사용하여 이스케이프 처리하여 식에서 참조해야 합니다.

**예약된 키워드는 다음과 같습니다.**

* `next`
* `last`
* `this`

**예:**

프로필 스키마에 이름이 `next`인 필드가 있는 경우 백틱으로 래핑해야 합니다.

```
{{profile.person.`next`.name}}
```

백틱스가 없으면 오류가 발생하여 개인화 편집기의 유효성 검사가 실패합니다.

>[!NOTE]
>
>예약된 키워드에 대한 백틱 이스케이프는 `{{...}}` Handlebars 경로와 `{%= ... %}` PQL 표현식 모두에 적용됩니다. 이러한 키워드는 경로 확인 수준에서 예약되어 있기 때문입니다. 이는 백틱 이스케이프가 PQL 표현식 내에서만 지원되는 하이픈 넣기 필드 이름과 다릅니다. [하이픈이 연결된 특성 키](#hyphenated-keys)를 참조하세요.

## 특수 속성 키에 대한 PQL 구문 규칙 {#pql-special-keys}

예약된 키워드 외에 두 개의 추가 사례에서는 PQL 표현식에서 백틱 이스케이프가 필요합니다.

### 하이픈 넣기 속성 키 {#hyphenated-keys}

XDM 스키마에 하이픈이 있는 필드 이름(예: `my-field`, `event-type`)이나 숫자로 시작하거나 숫자가 들어 있는 이름이 포함된 경우 PQL 식 내의 백틱으로 키를 래핑하십시오.

```sql
{%= profile.events.`order-total` > 100 %}
```

>[!NOTE]
>
>백틱 이스케이프는 PQL 식(`{%= ... %}`) 내에서만 지원됩니다. Handlebars 보간(`{{...}}`)에서는 지원되지 않습니다. 그러나 하이픈이 있는 필드 이름은 `{{...}}`개 블록(예: `{{profile.my-custom-field}}`)에서 직접 참조할 수 있으며 백틱 구문만 실패합니다.

PQL 표현식에 백틱이 없으면 하이픈이 빼기 연산자로 해석되어 PQL 구문 오류가 발생합니다.

### 컨텍스트 속성의 숫자 이벤트 ID {#numeric-event-ids}

이벤트 ID가 숫자인 컨텍스트 이벤트 특성을 참조할 때(예: `1697323153`) 백틱으로 래핑하십시오. 이는 `formatDate()`과(와) 같은 함수 내에도 적용됩니다.

```handlebars
{% let ts = formatDate(toDateTime(context.journey.events.`1697323153`.timestamp), "dd/MM/yyyy") %}
{{ts}}
```

## 문자 강제 변환 {#type-coercion}

PQL은 강력한 형식입니다. 값을 비교하거나 전달할 때 양쪽이 같은 유형이어야 합니다. 일반적인 사례:

| 시나리오 | 솔루션 |
|----------|----------|
| 문자열로 저장된 숫자 값 | 산술 또는 비교 전에 `stringToNumber()` 사용: `{%= stringToNumber(profile.loyalty.pointsBalance) > 500 %}` |
| 문자열로 저장된 정수 | 산술 연산 전에 `string_to_integer()` 또는 `stringToNumber()` 사용 |
| 문자열로 저장된 부울 | `toBool()`을(를) 사용하여 변환: `{%= toBool(profile.consents.email.val) = true %}` |

## 사용 가능한 네임스페이스 {#namespaces}

* **프로필**

  이 네임스페이스를 사용하면 [XDM(Adobe Experience Platform 데이터 모델) 설명서](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko-KR){target="_blank"}에 설명된 프로필 스키마에 정의된 모든 특성을 참조할 수 있습니다.

  [!DNL Journey Optimizer] 개인화 블록에서 참조하기 전에 스키마에 특성을 정의해야 합니다.

  조건에서 프로필 특성을 활용하는 방법에 대한 자세한 내용은 [이 섹션](functions/helpers.md#if-function)을 참조하세요.

  +++샘플 참조

   * `{{profile.person.name.fullName}}`
   * `{{profile.person.name.firstName}}`
   * `{{profile.person.gender}}`
   * `{{profile.personalEmail.address}}`
   * `{{profile.mobilePhone.number}}`
   * `{{profile.homeAddress.city}}`
   * `{{profile.faxPhone.number}}`

  +++

* **대상자**

  세분화 서비스에 대한 자세한 내용은 [이 설명서](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=ko){target="_blank"}를 참조하세요.

* **오퍼**

  이 네임스페이스를 사용하면 기존 오퍼 결정을 참조할 수 있습니다.

  오퍼를 참조하려면 오퍼를 정의하는 다양한 정보가 있는 경로를 선언해야 합니다. 이 경로의 구조는 다음과 같습니다.

  `offers.Type.[Placement Id].[Activity Id].Attribute`

  여기서:

   * `offers`은(는) 오퍼 네임스페이스에 속하는 경로 식을 식별합니다
   * `Type`이(가) 오퍼 표시 형식을 결정합니다. 가능한 값은 `image`, `html` 및 `text`입니다.
   * `Placement Id` 및 `Activity Id`은(는) 배치 및 활동 식별자입니다.
   * `Attributes`은(는) 오퍼 유형에 따라 다른 오퍼 특정 특성입니다. 예제: `deliveryUrl`(이미지)

  Decisions API 및 오퍼 표시에 대한 자세한 내용은 [이 페이지](../offers/api-reference/offer-delivery-api/decisioning-api.md)를 참조하세요.

  [이 페이지](../personalization/personalization-build-expressions.md)에 설명된 유효성 검사 메커니즘을 사용하여 오퍼 스키마에 대해 모든 참조의 유효성을 검사합니다.

  +++샘플 참조

   * 이미지가 호스팅되는 위치:

     `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].deliveryUrl`

   * 이미지를 클릭할 때 대상 URL:

     `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].linkUrl`

   * 의사 결정 엔진에서 제공되는 오퍼의 텍스트 콘텐츠:

     `offers.text.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`

   * decisioning 엔진에서 제공하는 오퍼의 HTML 콘텐츠:

     `offers.html.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`

  +++

## 도우미 {#helpers-all}

Handlebars 도우미는 매개 변수 뒤에 올 수 있는 간단한 식별자입니다. 각 매개 변수는 Handlebars 표현식입니다. 이러한 도우미는 템플릿의 모든 컨텍스트에서 액세스할 수 있습니다.

이러한 블록 도우미는 도우미 이름 앞에 `#`이(가) 있어 같은 이름의 일치하는 닫는 `/`이(가) 필요합니다.

블록은 블록 열기(`{{# }}`)와 닫기(`{{/}}`)가 있는 식입니다.

도우미 함수에 대한 자세한 내용은 [이 섹션](functions/helpers.md)을 참조하세요.

## 리터럴 유형 {#literal-types}

[!DNL Adobe Journey Optimizer]은(는) 다음 리터럴 형식을 지원합니다.

| 리터럴 | 정의 |
| ------- | ---------- |
| 문자열 | 큰따옴표로 묶인 문자로 구성된 데이터 유형입니다. <br>예: `"prospect"`, `"jobs"`, `"articles"` |
| 부울 | true 또는 false인 데이터 유형입니다. |
| 정수 | 정수를 나타내는 데이터 형식입니다. 양수, 음수 또는 0일 수 있습니다. <br>예: `-201`, `0`, `412` |
| 배열 | 다른 리터럴 값의 그룹으로 구성된 데이터 유형입니다. 대괄호를 사용하여 그룹화하고 쉼표를 사용하여 서로 다른 값 사이를 구분합니다. <br> **참고:** 배열 내의 항목 속성에 직접 액세스할 수 없습니다. <br> 예: `[1, 4, 7]`, `["US", "FR"]` |

>[!CAUTION]
>
>개인화 식에는 **xEvent** 변수를 사용할 수 없습니다. xEvent에 대한 모든 참조는 유효성 검사 실패를 초래합니다.

## 모범 사례 {#best-practices}

개인화 표현식을 작성하기 전에 이러한 구문 규칙을 검토하십시오. 대부분의 런타임 오류는 Handlebars와 PQL 컨텍스트를 혼합하여 발생합니다.

**올바른 조건부 블록 구문을 사용하십시오**

항상 `{%#if%}` / `{%else if%}` / `{%else%}` / `{%/if%}`을(를) 사용하십시오. `{% if %}` / `{% elseif %}` / `{% endif %}` 구문은 지원되지 않습니다.

```handlebars
{%#if profile.loyalty.tier = "gold"%}
Gold member content
{%else if profile.loyalty.tier = "silver"%}
Silver member content
{%else%}
Default content
{%/if%}
```

**Handlebars 블록 `{{...}}`에서 PQL 함수를 호출하지 마십시오**

`{{...}}`은(는) Handlebars 변수 및 도우미만 확인하며 PQL은 평가하지 않습니다. `{{...}}` 내에 `upperCase()`과(와) 같은 PQL 함수를 래핑하면 &quot;도우미를 찾을 수 없습니다&quot; 오류가 발생합니다. 대신 `{%= ... %}`을(를) 사용합니다.

| 전체적으로 잘못됨 | 맞음 |
|-----------|---------|
| `{{upperCase(cleanName)}}` | `{%= upperCase(cleanName) %}` |

**`{{#each}}`을(를)`{%#if%}`**&#x200B;과(와) 결합할 때 명명된 루프 별칭을 사용합니다.

`this.field`은(는) Handlebars 렌더러에서 확인되지만 `{%#if%}` 조건 내에서 PQL 평가기에서 확인하지 않습니다. 두 컨텍스트에서 필드를 확인할 수 있도록 `as |item|`(으)로 명명된 별칭을 정의합니다.

```handlebars
{{#each profile.orders as |order|}}
  {%#if order.status = "pending"%}
  Order {{order.id}} is pending.
  {%/if%}
{{/each}}
```

**반복하기 전에 변수에 PQL 함수 결과 할당**

`topN`과(와) 같은 PQL UDF는 `{{#each}}` 내에서 직접 호출할 수 없습니다. 먼저 `{% let %}`(으)로 평가한 다음 결과를 반복합니다.

```handlebars
{% let topOrders = topN(profile.orders, price, 3) %}
{{#each topOrders}}
  {{this.name}} — {{this.price}}&euro;
{{/each}}
```

**반복적인 함수 호출을 방지하려면 `{% let %}`을(를) 사용합니다**

계산된 값이 두 번 이상 필요한 경우 변수에 저장합니다. 이렇게 하면 가독성이 향상되고 평가가 중복되지 않습니다.

```handlebars
{% let cleanName = replaceAll(profile.person.name.firstName, "[^a-zA-Z]", "") %}
Hi {{cleanName}}, your code is: WELCOME-{%= upperCase(cleanName) %}
```

**올바른 인수 순서를 사용하여`dateDiff`**

`dateDiff(start, end)`이(가) 먼저 이전 날짜를 사용합니다. 미래 날짜까지 남은 일 수를 계산하려면 현재 날짜를 첫 번째 인수로 전달합니다.

```handlebars
{% let daysLeft = dateDiff(getCurrentZonedDateTime(), stringToDate(profile.loyalty.expiryDate)) %}
```

**PQL의 같음 비교에`==`**&#x200B;이(가) 아닌 `=`을(를) 사용합니다.

PQL에서는 같음을 위해 단일 `=` 연산자를 사용합니다. `==`을(를) 사용하면 구문 오류가 발생합니다.

**하이픈이 있는 필드 이름에 백틱 사용 - PQL 식에서만 사용**

XDM 스키마 필드 이름에 하이픈(예: `order-total`)이 포함된 경우 백틱으로 래핑하여 하이픈이 빼기 연산자로 구문 분석되지 않도록 하십시오. `{%= ... %}` PQL 식에서만 지원되며 `{{...}}` Handlebars 블록에서는 지원되지 않습니다.

```sql
{%= profile.events.`order-total` > 100 %}
```

바로 사용할 수 있는 표현식을 콘텐츠로 직접 복사하려면 [Personalization 레시피](personalization-recipes.md)를 참조하십시오.
