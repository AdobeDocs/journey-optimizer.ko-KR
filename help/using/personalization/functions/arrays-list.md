---
title: 배열 함수 라이브러리
description: 배열 함수 라이브러리
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: dfe611fb-9c50-473c-9eb7-b983e1e6f01e
TQID: https://experienceleague.adobe.com/CUiT5GFH9o4q-oOSWuKC8ZyLbRbH9lj88M92LhMIX9E
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
feature_v2: id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2: []
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 742
ht-degree: 4%

---

# 배열 및 목록 함수 {#arrays}

이러한 함수를 사용하여 배열, 목록 및 문자열과 보다 쉽게 상호 작용할 수 있습니다.

## null만 계산 {#count-only-null}

`countOnlyNull` 함수는 목록의 null 값 수를 계산하는 데 사용됩니다.

**구문**

```sql
{%= countOnlyNull(array) %}
```

**예**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

3을 반환합니다.

## null이 포함된 개수 {#count-with-null}

`countWithNull` 함수는 null 값을 포함하여 목록의 모든 요소를 계산하는 데 사용됩니다.

**구문**

```sql
{%= countWithNull(array) %}
```

**예**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

6을 반환합니다.

## 고유{#distinct}

`distinct` 함수는 중복 값이 제거된 배열 또는 목록에서 값을 가져오는 데 사용됩니다.

**구문**

```sql
{%= distinct(array) %}
```

**예**

다음 작업은 두 개 이상의 스토어에서 주문한 사람을 지정합니다.

```sql
{%= distinct(person.orders.storeId).count() > 1 %}
```

## null이 포함된 고유 개수 {#distinct-count-with-null}

`distinctCountWithNull` 함수는 null 값을 포함하는 목록의 다른 값 수를 계산하는 데 사용됩니다.

**구문**

```sql
{%= distinctCountWithNull(array) %}
```

**예**

```sql
{%= distinctCountWithNull([10,2,10,null]) %}
```

3을 반환합니다.

## 첫 번째 항목{#head}

`head` 함수는 배열 또는 목록의 첫 번째 항목을 반환하는 데 사용됩니다.

**구문**

```sql
{%= head(array) %}
```

**예**

다음 작업은 가격이 가장 높은 상위 5개 주문 중 첫 번째 주문을 반환합니다. `topN` 함수에 대한 자세한 내용은 배열의 [첫 번째 `n`](#first-n) 섹션에서 찾을 수 있습니다.

```sql
{%= head(topN(orders,price, 5)) %}
```

## 정렬하고 배열에서 첫 번째 N을 가져옵니다. {#first-n}

`topN` 함수는 지정된 수식을 기반으로 내림차순으로 배열을 정렬하고 첫 번째 `N`개 항목을 반환합니다. 배열 크기가 `N`보다 작으면 정렬된 전체 배열을 반환합니다.

이 함수
**구문**

```sql
{%= topN(array, value, amount) %}
```

| 인수 | 설명 |
| --------- | ----------- |
| `{ARRAY}` | 정렬할 배열 또는 목록입니다. |
| `{VALUE}` | 배열 또는 목록을 정렬할 속성입니다. |
| `{AMOUNT}` | 반환할 항목의 수입니다. |

**예**

다음 작업은 가격이 가장 낮은 처음 5개의 주문을 반환합니다.

```sql
{%= topN(orders,price, 5) %}
```

## 위치{#in}

`in` 함수는 항목이 배열의 멤버인지 또는 목록의 멤버인지 확인하는 데 사용합니다.

**구문**

```sql
{%= in(value, array) %}
```

**예**

다음 작업은 3월, 6월 또는 9월에 생일이 있는 사람을 정의합니다.

```sql
{%= in (person.birthMonth, [3, 6, 9]) %}
```

## 포함{#includes}

`includes` 함수는 배열 또는 목록에 지정된 항목이 포함되어 있는지 확인하는 데 사용됩니다.

**구문**

```sql
{%= includes(array,item) %}
```

**예**

다음 작업은 즐겨 찾는 색상에 빨간색이 포함된 사람을 정의합니다.

```sql
{%= includes(person.favoriteColors,"red") %}
```

## 교차{#intersects}

`intersects` 함수는 두 배열 또는 목록에 하나 이상의 공통 멤버가 있는지 확인하는 데 사용됩니다.

**구문**

```sql
{%= intersects(array1, array2) %}
```

**예**

다음 작업은 좋아하는 색상에 빨간색, 파란색 또는 녹색 중 하나 이상을 포함하는 사용자를 정의합니다.

```sql
{%= intersects(person.favoriteColors,["red", "blue", "green"]) %}
```


<!--
## Intersection{#intersection}

The `intersection` function is used to determine the common members of two arrays or lists.

**Syntax**

```sql
intersection({ARRAY},{ARRAY})
```

**Example**

The following operation defines if person 1 and person 2 both have favorite colors of red, blue, and green.

```sql
intersection(person1.favoriteColors,person2.favoriteColors) = ["red", "blue", "green"]
```
-->

## 배열에서 마지막 N 정렬 및 가져오기 {#last-n}

`bottomN` 함수는 지정된 수식을 기반으로 배열을 오름차순으로 정렬하고 첫 번째 `N`개 항목을 반환합니다. 배열 크기가 `N`보다 작으면 정렬된 전체 배열을 반환합니다.

**구문**

```sql
{%= bottomN(array, value, amount) %}
```

| 인수 | 설명 |
| --------- | ----------- |
| `{ARRAY}` | 정렬할 배열 또는 목록입니다. |
| `{VALUE}` | 배열 또는 목록을 정렬할 속성입니다. |
| `{AMOUNT}` | 반환할 항목의 수입니다. |

**예**

다음 작업은 가격이 가장 높은 마지막 5개의 주문을 반환합니다.

```sql
{%= bottomN(orders,price, 5) %}
```

## 다음에 없음{#notin}

`notIn` 함수는 항목이 배열 또는 목록의 멤버가 아닌지 확인하는 데 사용됩니다.

>[!NOTE]
>
>`notIn` 함수 *also*&#x200B;에서는 두 값 모두 null이 아닙니다. 따라서 결과는 `in` 함수에 대한 정확한 부정 결과가 아닙니다.

**구문**

```sql
{%= notIn(value, array) %}
```

**예**

다음 작업은 생일이 3월, 6월 또는 9월이 아닌 사람을 정의합니다.

```sql
{%= notIn(person.birthMonth ,[3, 6, 9]) %}
```


## 하위 집합{#subset}

`subsetOf` 함수는 특정 배열(배열 A)이 다른 배열(배열 B)의 하위 집합인지 확인하는 데 사용됩니다. 즉, 배열 A의 모든 요소는 배열 B의 요소이다.

**구문**

```sql
{%= subsetOf(array1, array2) %}
```

**예**

다음 작업은 자신이 좋아하는 모든 도시를 방문한 사람들을 정의합니다.

```sql
{%= subsetOf(person.favoriteCities,person.visitedCities) %}
```

## 상위 집합{#superset}

`supersetOf` 함수는 특정 배열(배열 A)이 다른 배열(배열 B)의 상위 집합인지 확인하는 데 사용합니다. 즉, 배열 A는 배열 B의 모든 요소를 포함합니다.

**구문**

```sql
{%= supersetOf(array1, array2) %}
```

**예**

다음 작업은 스시와 피자를 한 번이라도 먹은 사람들을 정의합니다.

```sql
{%= supersetOf(person.eatenFoods,["sushi", "pizza"]) %}
```

## 배열 반복 {#each-loop}

Handlebars `{{#each}}` 블록 도우미를 사용하여 배열을 반복하고 **개인화된 콘텐츠**&#x200B;의 각 항목에 대한 콘텐츠를 렌더링합니다(전자 메일, SMS, 푸시).

>[!NOTE]
>
>`{{#each}}`은(는) **개인화 편집기**&#x200B;에서만 사용할 수 있습니다(전자 메일 본문, SMS, 푸시 콘텐츠). 여정 조건 활동에서 **지원되지 않음**&#x200B;입니다. 여정 조건 내의 배열에서 항목을 필터링하거나 일치시키려면 대신 [컬렉션 관리 함수](../../building-journeys/expression/collection-management-functions.md)를 사용하십시오.

**구문**

```handlebars
{{#each arrayAttribute}}
  {{this}}
{{/each}}
```

+++예 — 배열의 모든 항목 나열

```handlebars
{{#each profile.purchases.items}}
  - {{this.name}}: {{this.price}}€
{{/each}}
```

출력(예):

```
- Running shoes: 89€
- Water bottle: 15€
- Gym bag: 45€
```

+++

+++예 — 루프 인덱스에 액세스합니다

`@index`을(를) 사용하여 현재 루프 위치(0 기반)에 액세스합니다.

```handlebars
{{#each profile.preferences.languages}}
  {{@index}}: {{this}}
{{/each}}
```

출력(예):

```
0: English
1: French
2: Spanish
```

+++

+++예 — 루프 내의 조건부 렌더링

조건이 충족될 때만 콘텐츠를 렌더링하려면 `{{#each}}` 내의 `{%#if%}` 블록을 사용합니다.

>[!NOTE]
>
>`{% if %}` / `{% endif %}`은(는) 지원되지 않습니다. 대신 `{%#if%}` / `{%/if%}`을(를) 사용합니다. 또한 `this.<field>`은(는) PQL 조건 표현식 내에서 작동하지 않습니다. 특성 이름(예: `order.status`)을 사용하여 직접 필드를 참조합니다.

```handlebars
{{#each profile.orders as |order|}}
  {%#if order.status = "pending"%}
  Your order {{order.id}} is still pending.
  {%/if%}
{{/each}}
```

이 패턴은 &quot;조건에 따른 브레이크&quot;를 시뮬레이션하는 데 권장되는 패턴입니다. 조건과 일치하는 항목만 출력을 생성합니다.

+++
