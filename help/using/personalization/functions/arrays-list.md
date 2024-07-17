---
title: 배열 함수 라이브러리
description: 배열 함수 라이브러리
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: dfe611fb-9c50-473c-9eb7-b983e1e6f01e
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '564'
ht-degree: 9%

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

## 배열의 첫 `n` {#first-n}

`topN` 함수는 특정 수식에 따라 오름차순으로 정렬되면 배열에서 첫 번째 `N` 항목을 반환하는 데 사용됩니다.

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

## 안에 있음{#in}

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

## 다음을 포함{#includes}

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


<!-- ## Intersection{#intersection}

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

## 배열의 마지막 `n`{#last-n}

`bottomN` 함수는 특정 수식에 따라 내림차순으로 정렬되면 배열에서 마지막 `N` 항목을 반환하는 데 사용됩니다.

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

## 안에 없음{#notin}

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
{%= supersetOf(person.eatenFoods,["sushi", "pizza"] %}
```
