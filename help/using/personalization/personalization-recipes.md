---
title: Personalization 레서피
description: Adobe Journey Optimizer의 일반적인 개인화 패턴 및 실제 사례
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
source-git-commit: 04fca756923d53595639e221fb59d3f6a458ac4a
workflow-type: tm+mt
source-wordcount: '815'
ht-degree: 0%

---

# Personalization 레서피 {#personalization-recipes}

이 페이지에서는 Adobe Journey Optimizer의 가장 일반적인 사용 사례에 대해 즉시 사용 가능한 개인화 패턴을 제공합니다. 모든 예는 개인화 편집기 구문을 사용하며, 이메일, SMS 또는 푸시 콘텐츠에 직접 복사할 수 있습니다.

사용 가능한 함수에 대한 전체 참조는 [도우미 함수](functions/helpers.md), [날짜/시간 함수](functions/dates.md), [문자열 함수](functions/string.md) 및 [배열 함수](functions/arrays-list.md)를 참조하십시오.

>[!TIP]
>
>예제를 복사하기 전에 [Personalization 모범 사례](personalization-syntax.md#best-practices)를 검토하여 가장 일반적인 구문 오류를 방지하십시오.

## 날짜 및 시간 레서피 {#date-time-recipes}

### 레서피 1 — 현재 날짜를 읽을 수 있는 형식으로 표시합니다. {#recipe-current-date}

`getCurrentZonedDateTime()`과(와) 함께 `formatDate`을(를) 사용하여 오늘의 날짜를 모든 형식으로 렌더링합니다.

```sql
{%= formatDate(getCurrentZonedDateTime(), "MMMM dd, yyyy") %}
```

출력(예): `April 11, 2026`

**일반적인 형식 패턴:**

| 패턴 | 출력 예 |
|---------|---------------|
| `"dd/MM/yyyy"` | `11/04/2026` |
| `"MM/dd/yyyy"` | `04/11/2026` |
| `"EEEE, MMMM dd"` | `Saturday, April 11` |
| `"yyyy-MM-dd"` | `2026-04-11` |

>[!NOTE]
>
>연도 경계에서 예기치 않은 결과가 발생하지 않도록 하려면 `Y`(주 기준 연도)이 아닌 소문자 `y`(달력 연도)을 사용하십시오. 전체 참조는 [패턴 문자](functions/dates.md#pattern-characters)를 참조하십시오.

### 레서피 2 — 만료 또는 이벤트 날짜의 카운트다운 {#recipe-countdown}

`dateDiff`을(를) 사용하여 프로필 날짜 특성까지 남은 일수를 계산한 다음 동적으로 렌더링합니다.

```handlebars
{% let daysLeft = dateDiff(getCurrentZonedDateTime(), stringToDate(profile.loyalty.expiryDate)) %}
{%#if daysLeft > 0%}
Your reward points expire in {{daysLeft}} day{%#if daysLeft > 1%}s{%/if%}. Use them before they're gone!
{%else%}
Your reward points have expired.
{%/if%}
```

출력(예): `Your reward points expire in 7 days. Use them before they're gone!`

### 레서피 3 — 동적 종료 일자보다 X일 전 {#recipe-days-before}

프로필 속성(예: 콘텐츠 또는 제목 줄에서 참조)의 X일 전 날짜를 계산하려면 음수 오프셋과 함께 `addDays`을(를) 사용합니다.

```sql
{%= formatDate(addDays(stringToDate(profile.subscription.endDate), -7), "MMMM dd, yyyy") %}
```

출력(예): `April 04, 2026` *(4월 11일 7일 전)*

고정 시간(예: 오전 9시)도 설정하려면 `setHours`과(와) 결합하십시오.

```sql
{%= formatDate(setHours(addDays(stringToDate(profile.subscription.endDate), -7), 9), "dd/MM/yyyy HH:mm") %}
```

### 레서피 4 — 현재 시간을 HH:MM(으)로만 표시 {#recipe-time-only}

`extractHours` 및 `extractMinutes`을(를) 사용하여 시간 부분만 표시합니다. 분 동안 앞에 영(0)의 가드를 사용합니다.

```handlebars
{% let h = extractHours(getCurrentZonedDateTime()) %}
{% let m = extractMinutes(getCurrentZonedDateTime()) %}
Your appointment is at {{h}}:{%#if m < 10%}0{%/if%}{{m}}.
```

출력(예): `Your appointment is at 14:05.`

### 레시피 5 - 주말과 평일 비교 감지 {#recipe-weekend}

날짜에 따라 콘텐츠를 조정하려면 `dayOfWeek`을(를) 사용합니다. 이 함수는 1(월요일)부터 7(일요일)까지 반환합니다. 단일 `=` 연산자 사용(`==`이 아닌 PQL 구문):

```handlebars
{%#if dayOfWeek(getCurrentZonedDateTime()) = 6 or dayOfWeek(getCurrentZonedDateTime()) = 7%}
We're closed on weekends — our team will follow up on the next business day.
{%else%}
Our team will get back to you within 24 hours.
{%/if%}
```

>[!NOTE]
>
>`dayOfWeek()`은(는) 날짜에 따라 **콘텐츠**&#x200B;을(를) 조정하기 위한 것입니다. 여정에서 요일을 기준으로 프로필을 다르게 라우팅하려면 여정 조건 활동에서 기본 제공된 **시간 조건 → 요일** 옵션을 사용하십시오. [자세히 알아보기](../building-journeys/condition-activity.md#date_condition)

## 배열 및 루프 레서피 {#array-recipes}

### 레서피 6 — 프로파일 배열의 모든 항목 나열 {#recipe-list-items}

`{{#each}}`을(를) 사용하여 프로필 배열을 반복하고 각 항목을 렌더링합니다. 이는 개인화 편집기(이메일, SMS, 푸시)에서만 사용할 수 있습니다.

```handlebars
{{#each profile.purchases.recentItems}}
  - {{this.name}}: {{this.price}}&euro;
{{/each}}
```

출력(예):

```
- Running shoes: 89&euro;
- Water bottle: 15&euro;
- Gym bag: 45&euro;
```

>[!NOTE]
>
>`{{#each}}`은(는) 여정 조건 활동에서 지원되지 않습니다. 조건에서 배열 필터링을 수행하려면 [컬렉션 관리 함수](../building-journeys/expression/collection-management-functions.md)를 사용하십시오.

### 레서피 7 — 가격별로 배열의 상위 N개 항목 표시 {#recipe-first-n}

숫자 필드를 기준으로 상위 N개 항목을 정렬하고 검색하려면 `topN`을(를) 사용하십시오. `topN`이(가) PQL 함수이므로 먼저 `{% let %}`을(를) 사용하여 변수에 할당한 다음 `{{#each}}`을(를) 사용하여 반복하십시오.

```handlebars
{% let topOrders = topN(profile.orders, price, 3) %}
{{#each topOrders}}
  {{this.name}} — {{this.price}}&euro;
{{/each}}
```

>[!NOTE]
>
>`topN(profile.orders, price, 3)`은(는) `price`별로 순서를 내림차순으로 정렬하고 상위 3을 반환합니다. 즉, 원래 배열 순서의 처음 3개 항목을 반환하지 않습니다.

또는 `head`을(를) 사용하여 단일 상위 항목만 가져옵니다.

```sql
{%= head(profile.purchases.recentItems).name %}
```

### 레서피 8 — 배열 항목당 조건부로 컨텐츠 렌더링 {#recipe-conditional-loop}

`{{#each}}` 내의 `{%#if%}`을(를) 사용하여 일치하는 항목에 대해서만 출력을 렌더링합니다. PQL 평가기가 다음 조건에서 특성 참조를 확인할 수 있도록 `as |order|`을(를) 사용하여 루프 별칭을 정의하십시오.

```handlebars
{{#each profile.orders as |order|}}
  {%#if order.status = "pending"%}
  Order {{order.id}} is pending — we'll notify you when it ships.
  {%/if%}
{{/each}}
```

>[!NOTE]
>
>`this.status`은(는) Handlebars 식에서 작동하지만 `{%#if%}` 내의 PQL 평가기에서 확인되지 않습니다. 명명된 루프 별칭(예: `order`)을 사용하면 Handlebars 및 PQL 컨텍스트 모두에서 특성을 사용할 수 있습니다.

## 문자열 및 형식 지정 레서피 {#string-recipes}

### 레서피 9 — replaceAll로 문자열을 지우고 재사용합니다. {#recipe-replaceall-reuse}

`replaceAll`이(가) 새 값을 반환합니다. 원본을 수정하지 않습니다. 함수 호출을 반복하지 않고 결과를 저장하고 여러 번 참조하려면 `{% let %}`을(를) 사용하십시오.

```handlebars
{% let cleanName = replaceAll(profile.person.name.firstName, "[^a-zA-Z]", "") %}
Hi {{cleanName}},
Your exclusive code is: WELCOME-{%= upperCase(cleanName) %}
```

출력(예):

```
Hi John,
Your exclusive code is: WELCOME-JOHN
```

### 레서피 10 — JSON 출력의 값 큰따옴표 {#recipe-json-quotes}

문자열 내에 리터럴 큰따옴표를 포함하려면(예: 사용자 지정 페이로드에 대해 JSON 생성) 백슬래시(`\"`)로 이스케이프 처리하십시오.

```handlebars
{ "greeting": "Hello \"{{profile.person.name.firstName}}\"" }
```

출력: `{ "greeting": "Hello \"John\"" }`

### 레시피 11 — 날짜 구성 요소의 서식을 대문자로 지정합니다 {#recipe-uppercase-date}

`formatDate`을(를) `upperCase`과(와) 결합하여 월 또는 일 이름을 대문자로 렌더링합니다.

```sql
{%= upperCase(formatDate(getCurrentZonedDateTime(), "MMMM")) %}
```

출력(예): `APRIL`

전체 대문자 날짜 문자열:

```sql
{%= upperCase(formatDate(profile.person.birthDateTime, "EEEE MMMM dd yyyy")) %}
```

출력(예): `WEDNESDAY JANUARY 01 2020`

## 조건부 논리 레시피 {#conditional-recipes}

### 레시피 12 — 개인화된 콘텐츠의 경우/경우/경우/경우 {#recipe-if-elseif}

다중 분기 조건부 논리에 `{%#if%}`, `{%else if%}` 및 `{%else%}`을(를) 사용합니다. 이 패턴은 이메일 콘텐츠 및 조각에서 작동합니다.

```handlebars
{%#if profile.loyalty.tier = "gold"%}
As a Gold member, enjoy free shipping on all orders.
{%else if profile.loyalty.tier = "silver"%}
As a Silver member, enjoy free shipping on orders over &euro;50.
{%else%}
Join our loyalty program to unlock exclusive benefits.
{%/if%}
```

### 레서피 13 — Null 안전 속성 표시 {#recipe-null-safe}

프로필 속성이 null이거나 누락된 경우 빈 값을 렌더링하지 않도록 하려면 조건부 폴백을 사용합니다.

```handlebars
{%#if profile.person.name.firstName%}
Hi {{profile.person.name.firstName}},
{%else%}
Hi there,
{%/if%}
```

또는 `isEmpty`을(를) 사용하여 삼항 스타일 패턴으로 인라인합니다.

```handlebars
Hi {%#if isEmpty(profile.person.name.firstName)%}valued customer{%else%}{{profile.person.name.firstName}}{%/if%},
```

## PQL edge case 레서피 {#pql-edge-cases}

### 레서피 14 — 하이픈이 연결된 속성 키 참조 {#recipe-hyphenated-key}

XDM 스키마 필드 이름에 하이픈(예: `order-total`, `event-type`)이 포함된 경우 하이픈을 빼기 연산자로 해석하지 않도록 PQL 식 내에서 백틱으로 줄바꿈합니다.

```sql
{%= profile.events.`order-total` > 100 %}
```

>[!NOTE]
>
>백틱은 PQL 식(`{%= ... %}`) 내에서만 지원됩니다. 일반 Handlebars 보간(`{{...}}`)에서 허용되지 않습니다. 하이픈이 있는 필드 값을 직접 렌더링해야 하는 경우 먼저 PQL 식을 통해 계산하거나 `{% let %}`을(를) 사용하여 변수에 저장하십시오.

### 레서피 15 — 컨텍스트 속성에서 숫자 이벤트 ID를 참조합니다. {#recipe-numeric-event-id}

ID가 숫자 문자열인 여정 컨텍스트 이벤트를 사용하는 경우(예: `1697323153`) 백틱으로 ID를 래핑하고 `toDateTime()` 및 `formatDate()`과(와) 함께 `{% let %}`을(를) 사용합니다.

```handlebars
{% let appointmentDate = formatDate(toDateTime(context.journey.events.`1697323153`.timestamp), "dd/MM/yyyy HH:mm") %}
Your appointment: {{appointmentDate}}
```

출력(예): `Your appointment: 18/03/2026 14:30`

### 레서피 16 — 입력 강제 변환: 문자열 필드를 숫자와 비교 {#recipe-type-coercion}

PQL은 강력한 형식입니다. 프로필 필드가 문자열로 저장되었지만 숫자로 비교해야 하는 경우 먼저 `stringToNumber()`을(를) 사용하여 변환하십시오.

```sql
{%= stringToNumber(profile.loyalty.pointsBalance) > 500 %}
```

문자열로 저장된 부울 필드의 경우:

```sql
{%= toBool(profile.consents.email.val) = true %}
```

