---
title: 함수 라이브러리
description: 함수 라이브러리
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '535'
ht-degree: 5%

---

# 배열 및 목록 함수 {#arrays}

![](../../assets/do-not-localize/badge.png)

[!DNL Profile Query Language] (PQL)은 배열, 목록 및 문자열과 쉽게 상호 작용할 수 있는 기능을 제공합니다.

## 시작

`in` 함수는 항목이 배열 또는 목록의 구성원인지 확인하는 데 사용됩니다.

**형식**

```sql
in ({VALUE},{ARRAY})
```

**예**

다음 PQL 질의는 3월, 6월 또는 9월에 생일을 사용하는 사람을 정의합니다.

```sql
in (person.birthMonth, [3, 6, 9])
```

## 안 함

`notIn` 함수는 항목이 배열 또는 목록의 구성원이 아닌지 확인하는 데 사용됩니다.

>[!NOTE]
>
>`notIn` 함수 *도*&#x200B;에서 두 값 중 어느 것도 null과 동일하지 않도록 합니다. 따라서 결과는 `in` 함수의 정확한 부정이 아닙니다.

**형식**

```sql
notIn ({VALUE},{ARRAY})
```

**예**

다음 PQL 쿼리는 3월, 6월 또는 9월에 없는 생일을 가진 사람을 정의합니다.

```sql
notIn (person.birthMonth ,[3, 6, 9])
```

## 교차점

`intersects` 함수는 두 배열 또는 목록에 하나 이상의 공통 구성원이 있는지 확인하는 데 사용됩니다.

**형식**

```sql
intersects({ARRAY},{ARRAY})
```

**예**

다음 PQL 쿼리는 즐겨찾기 색상이 하나 이상의 빨강, 파랑 또는 녹색을 포함하는 사람을 정의합니다.

```sql
intersects(person.favoriteColors,["red", "blue", "green"])
```

## 교차

`intersection` 함수는 두 배열 또는 목록의 공통 멤버를 결정하는 데 사용됩니다.

**형식**

```sql
intersection({ARRAY},{ARRAY})
```

**예**

다음 PQL 쿼리는 사람 1과 사람 2가 모두 빨간색, 파란색 및 녹색의 즐겨찾기 색상을 가지고 있는지 여부를 정의합니다.

```sql
intersection(person1.favoriteColors,person2.favoriteColors) = ["red", "blue", "green"]
```

## 하위 집합

`subsetOf` 함수는 특정 배열(배열 A)이 다른 배열(배열 B)의 하위 집합인지 확인하는 데 사용됩니다. 즉, 배열 A의 모든 요소는 배열 B의 요소입니다.

**형식**

```sql
subsetOf({ARRAY},{ARRAY})
```

**예**

다음 PQL 쿼리는 즐겨찾기 도시를 모두 방문한 사람을 정의합니다.

```sql
subsetOf(person.favoriteCities,person.visitedCities)
```

## 상위 세트

`supersetOf` 함수는 특정 배열(배열 A)이 다른 배열(배열 B)의 상위 집합인지 확인하는 데 사용됩니다. 즉, 배열 A에는 배열 B의 모든 요소가 포함됩니다.

**형식**

```sql
supersetOf({ARRAY},{ARRAY})
```

**예**

다음 PQL 쿼리는 초밥과 피자를 최소한 한 번 먹은 사람을 정의합니다.

```sql
supersetOf(person.eatenFoods,["sushi", "pizza"])
```

## 포함 사항

`includes` 함수는 배열 또는 목록에 지정된 항목이 포함되어 있는지 확인하는 데 사용됩니다.

**형식**

```sql
includes({ARRAY},{ITEM})
```

**예**

다음 PQL 쿼리는 즐겨찾기 색상이 빨간색을 포함하는 사람을 정의합니다.

```sql
includes(person.favoriteColors,"red")
```

## Distinct

`distinct` 함수는 배열 또는 목록에서 중복 값을 제거하는 데 사용됩니다.

**형식**

```sql
distinct({ARRAY})
```

**예**

다음 PQL 쿼리는 둘 이상의 스토어에서 주문을 제출한 사람을 지정합니다.

```sql
distinct(person.orders.storeId).count() > 1
```

## 배열 {#first-n}의 첫 번째 `n`

`topN` 함수는 지정된 숫자 표현식에 따라 오름차순으로 정렬할 때 배열의 첫 번째 `N` 항목을 반환하는 데 사용됩니다.

**형식**

```sql
topN({ARRAY},{VALUE}, {AMOUNT})
```

| 인수 | 설명 |
| --------- | ----------- |
| `{ARRAY}` | 정렬할 배열 또는 목록입니다. |
| `{VALUE}` | 배열 또는 목록을 정렬할 속성입니다. |
| `{AMOUNT}` | 반환할 항목 수입니다. |

**예**

다음 PQL 쿼리는 가격이 가장 높은 상위 5개 주문을 반환합니다.

```sql
topN(orders,price, 5)
```

## 배열의 마지막 `n`

`bottomN` 함수는 지정된 숫자 표현식에 따라 오름차순으로 정렬할 때 배열의 마지막 `N` 항목을 반환하는 데 사용됩니다.

**형식**

```sql
bottomN({ARRAY},{VALUE}, {AMOUNT})
```

| 인수 | 설명 |
| --------- | ----------- | 
| `{ARRAY}` | 정렬할 배열 또는 목록입니다. |
| `{VALUE}` | 배열 또는 목록을 정렬할 속성입니다. |
| `{AMOUNT}` | 반환할 항목 수입니다. |

**예**

다음 PQL 쿼리는 가장 낮은 가격으로 상위 5개의 주문을 반환합니다.

```sql
bottomN(orders,price, 5)
```

## 첫 번째 항목

`head` 함수는 배열 또는 목록의 첫 번째 항목을 반환하는 데 사용됩니다.

**형식**

```sql
head({ARRAY})
```

**예**

다음 PQL 쿼리는 상위 5개 주문 중 첫 번째 주문을 가장 높은 가격으로 반환합니다. `topN` 함수에 대한 자세한 내용은 array](#first-n) 섹션의 [first `n`에서 확인할 수 있습니다.

```sql
head(topN(orders,price, 5))
```
