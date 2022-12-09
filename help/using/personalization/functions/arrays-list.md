---
title: 배열 함수 라이브러리
description: 배열 함수 라이브러리
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: dfe611fb-9c50-473c-9eb7-b983e1e6f01e
source-git-commit: 2160d52f24af50417cdcf8c6ec553b746a544c2f
workflow-type: tm+mt
source-wordcount: '564'
ht-degree: 0%

---

# 배열 및 목록 함수 {#arrays}

이러한 함수를 사용하여 배열, 목록 및 문자열과 보다 쉽게 상호 작용할 수 있습니다.

## null만 계산 {#count-only-null}

다음 `countOnlyNull` 함수는 목록의 null 값 수를 계산하는 데 사용됩니다.

**형식**

```sql
{%= countOnlyNull(array) %}
```

**예**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

3 반환.

## Null로 계산 {#count-with-null}

다음 `countWithNull` 함수는 null 값을 포함하는 목록의 모든 요소를 계산하는 데 사용됩니다.

**형식**

```sql
{%= countWithNull(array) %}
```

**예**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

6 반환.

## 고유{#distinct}

다음 `distinct` 함수는 중복 값이 제거된 배열 또는 목록의 값을 가져오는 데 사용됩니다.

**형식**

```sql
{%= distinct(array) %}
```

**예**

다음 작업은 둘 이상의 저장소에 주문을 한 사용자를 지정합니다.

```sql
{%= distinct(person.orders.storeId).count() > 1 %}
```

## Null이 있는 고유 개수 {#distinct-count-with-null}

다음 `distinctCountWithNull` 함수는 null 값을 포함하는 목록의 다른 값 수를 계산하는 데 사용됩니다.

**형식**

```sql
{%= distinctCountWithNull(array) %}
```

**예**

```sql
{%= distinctCountWithNull([10,2,10,null]) %}
```

3 반환.

## 첫 번째 항목{#head}

다음 `head` 함수는 배열 또는 목록의 첫 번째 항목을 반환하는 데 사용됩니다.

**형식**

```sql
{%= head(array) %}
```

**예**

다음 작업은 가격이 가장 높은 상위 5개 주문 중 첫 번째 주문을 반환합니다. 에 대한 추가 정보 `topN` 함수는 [첫 번째 `n` 어레이](#first-n) 섹션을 참조하십시오.

```sql
{%= head(topN(orders,price, 5)) %}
```

## 첫 번째 `n` 어레이 {#first-n}

다음 `topN` 함수는 `N` 지정된 숫자 식을 기반으로 오름차순으로 정렬하는 경우 배열의 항목이 표시됩니다.

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

다음 `in` 함수가 배열 또는 목록의 구성원인지 여부를 확인하는 데 사용됩니다.

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

다음 `includes` 함수는 배열 또는 목록에 지정된 항목이 포함되어 있는지 여부를 확인하는 데 사용됩니다.

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

다음 `intersects` 두 배열이나 목록에 하나 이상의 공통 멤버가 있는지 확인하는 데 사용되는 함수입니다.

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

## 마지막 `n` 어레이{#last-n}

다음 `bottomN` 함수는 `N` 지정된 숫자 식을 기반으로 오름차순으로 정렬하는 경우 배열의 항목이 표시됩니다.

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

다음 `notIn` 함수는 항목이 배열 또는 목록의 멤버가 아닌지 확인하는 데 사용됩니다.

>[!NOTE]
>
>다음 `notIn` 함수 *또한* 두 값이 모두 null인지 확인합니다. 따라서, 그 결과는 `in` 함수 위에 있어야 합니다.

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

다음 `subsetOf` 함수는 특정 배열(배열 A)이 다른 배열(배열 B)의 하위 집합인지 여부를 확인하는 데 사용됩니다. 즉, 배열 A의 모든 요소는 배열 B의 요소입니다.

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

다음 `supersetOf` 함수는 특정 배열(배열 A)이 다른 배열(배열 B)의 상위 집합인지 여부를 확인하는 데 사용됩니다. 즉, 해당 배열 A에 배열 B의 모든 요소가 포함됩니다.

**형식**

```sql
{%= supersetOf(array1, array2) %}
```

**예**

초밥과 피자를 적어도 한 번 먹은 사람은 다음 작업이다.

```sql
{%= supersetOf(person.eatenFoods,["sushi", "pizza"] %}
```
