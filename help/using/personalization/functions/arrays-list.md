---
title: 함수 라이브러리
description: 함수 라이브러리
source-git-commit: 8c58dd667ea59a17833bbe3482b1a233ac2e28fe
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 4%

---

# 배열 및 목록 함수 {#arrays}

![](../../assets/do-not-localize/badge.png)

이러한 함수를 사용하여 배열, 목록 및 문자열과 보다 쉽게 상호 작용할 수 있습니다.

## 고유{#distinct}

`distinct` 함수는 중복된 값이 제거된 배열 또는 목록의 값을 가져오는 데 사용됩니다.

**형식**

```sql
{%= distinct(array) %}
```

**예**

다음 작업은 둘 이상의 저장소에 주문을 한 사용자를 지정합니다.

```sql
{%= distinct(person.orders.storeId).count() > 1 %}
```

## 첫 번째 항목{#head}

`head` 함수는 배열 또는 목록의 첫 번째 항목을 반환하는 데 사용됩니다.

**형식**

```sql
{%= head({array}) %}
```

**예**

다음 작업은 가격이 가장 높은 상위 5개 주문 중 첫 번째 주문을 반환합니다. `topN` 함수에 대한 자세한 내용은 array](#first-n) 섹션의 [첫 번째 `n`에서 찾을 수 있습니다.

```sql
{%= head(topN(orders,price, 5)) %}
```

## {#first-n} 배열의 첫 번째 `n`

`topN` 함수는 지정된 숫자 식을 기반으로 오름차순으로 정렬한 경우 배열의 첫 번째 `N` 항목을 반환하는 데 사용됩니다.

**형식**

```sql
{%= topN(array, value, amount) %}
```

| 인수 | 설명 |
| --------- | ----------- |
| `{ARRAY}` | 정렬할 배열 또는 목록입니다. |
| `{VALUE}` | 배열이나 목록을 정렬할 속성입니다. |
| `{AMOUNT}` | 반환할 항목 수입니다. |

**예**

다음 작업은 가격이 가장 높은 상위 5개 주문을 반환합니다.

```sql
{%= topN(orders,price, 5) %}
```

## in{#in}

`in` 함수는 항목이 배열 또는 목록의 구성원인지 확인하는 데 사용됩니다.

**형식**

```sql
{%= in(value, array) %}
```

**예**

다음 작업은 3월, 6월, 9월에 생일이 있는 사람들을 규정합니다.

```sql
{%= in (person.birthMonth, [3, 6, 9]) %}
```

## 포함{#includes}

`includes` 함수는 배열 또는 목록에 지정된 항목이 포함되어 있는지 여부를 확인하는 데 사용됩니다.

**형식**

```sql
{%= includes(array,item) %}
```

**예**

다음 작업은 즐겨찾는 색상이 빨간색인 사람을 정의합니다.

```sql
{%= includes(person.favoriteColors,"red") %}
```

## 교차{#intersects}

`intersects` 함수는 두 배열 또는 목록에 하나 이상의 공통 멤버가 있는지 확인하는 데 사용됩니다.

**형식**

```sql
{%= intersects(array1, array2) %}
```

**예**

다음 작업은 빨간색, 파란색 또는 녹색 중 하나 이상의 색상을 포함하는 사람을 정의합니다.

```sql
{%= intersects(person.favoriteColors,["red", "blue", "green"]) %}
```


<!-- ## Intersection{#intersection}

The `intersection` function is used to determine the common members of two arrays or lists.

**Format**

```sql
intersection({ARRAY},{ARRAY})
```

**Example**

The following operation defines if person 1 and person 2 both have favorite colors of red, blue, and green.

```sql
intersection(person1.favoriteColors,person2.favoriteColors) = ["red", "blue", "green"]
```
-->

## 배열{#last-n}의 마지막 `n`

`bottomN` 함수는 지정된 숫자 식을 기반으로 오름차순으로 정렬하는 경우 배열의 마지막 `N` 항목을 반환하는 데 사용됩니다.

**형식**

```sql
{%= bottomN(array, value, amount) %}
```

| 인수 | 설명 |
| --------- | ----------- | 
| `{ARRAY}` | 정렬할 배열 또는 목록입니다. |
| `{VALUE}` | 배열이나 목록을 정렬할 속성입니다. |
| `{AMOUNT}` | 반환할 항목 수입니다. |

**예**

다음 작업은 가장 낮은 가격을 가진 상위 5개 주문을 반환합니다.

```sql
{%= bottomN(orders,price, 5) %}
```


## 아님{#notin}

`notIn` 함수는 항목이 배열 또는 목록의 멤버가 아닌지 확인하는 데 사용됩니다.

>[!NOTE]
>
>`notIn` 함수 *또한*&#x200B;는 두 값이 모두 null과 동일하지 않도록 합니다. 따라서 결과는 `in` 함수의 정확한 부정은 아닙니다.

**형식**

```sql
{%= notIn(value, array) %}
```

**예**

다음 작업은 3월, 6월, 9월에 없는 생일이 있는 사람들을 규정합니다.

```sql
{%= notIn(person.birthMonth ,[3, 6, 9]) %}
```


## 하위 집합{#subset}

`subsetOf` 함수는 특정 배열(배열 A)이 다른 배열(배열 B)의 하위 집합인지 확인하는 데 사용됩니다. 즉, 배열 A의 모든 요소는 배열 B의 요소입니다.

**형식**

```sql
{%= subsetOf(array1, array2) %}
```

**예**

다음 작업은 자신이 좋아하는 모든 도시를 방문한 사람들을 정의합니다.

```sql
{%= subsetOf(person.favoriteCities,person.visitedCities) %}
```

## 의 상위 집합{#superset}

`supersetOf` 함수는 특정 배열(배열 A)이 다른 배열(배열 B)의 상위 집합인지 확인하는 데 사용됩니다. 즉, 해당 배열 A에 배열 B의 모든 요소가 포함됩니다.

**형식**

```sql
{%= supersetOf(array1, array2) %}
```

**예**

초밥과 피자를 적어도 한 번 먹은 사람은 다음 작업이다.

```sql
{%= supersetOf(person.eatenFoods,["sushi", "pizza"] %}
```







