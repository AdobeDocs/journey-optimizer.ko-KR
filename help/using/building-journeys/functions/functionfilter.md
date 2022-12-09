---
product: journey optimizer
title: 필터
description: 함수 필터에 대해 알아보기
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 05e3d2ba-1a27-4f27-88cc-3d83eb3b14af
source-git-commit: 0b19af568b33d29f4b35deeab6def17919cfe824
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---

# 필터{#filter}

지정된 키 값 중 하나와 일치하는 키 특성이 있는 개체를 사용하여 listObject를 반환합니다.

>[!NOTE]
>
>대상 목록이 listObject인 경우 이 함수는 사용자 지정 작업 표현식에서만 사용할 수 있습니다.

## 카테고리

목록

## 함수 구문

`filter(<parameters>)`

## 매개 변수

| 매개 변수 | 유형 | 설명 |
|-----------|------------------|------------------|
| listToFilter | listObject | 필터링할 개체 목록 필드 참조여야 합니다. |
| keyAttributeName | string | 필터링에 키로 사용되는 지정된 목록의 객체 속성 이름 |
| keyValueList | list | 필터링을 위한 키 값 배열 |

## 서명 및 반환된 형식

`filter(listObject, string, listString)`

`filter(listObject, string, listInteger)`

`filter(listObject, string, listDecimal)`

`filter(listObject, string, listDateTime)`

`filter(listObject, string, listDateTimeOnly)`

`filter(listObject, string, listDateOnly)`

`filter(listObject, string, listDuration)`

`filter(listObject, string, listBoolean)`

listObject를 반환합니다.

## 예

다음은 들어오는 이벤트 &quot;myevent&quot;에서 전달된 페이로드의 예입니다.

```json
"productListItems": [{
   "id": "product1",
   "name": "the product 1",
   "price": 20
},{
   "id": "product2",
   "name": "the product 2",
   "price": 30
},{
   "id": "product3",
   "name": "the product 3",
   "price": 50
}]
```

다음 표현식을 사용할 수 있습니다.

```json
filter(
 @{myevent.productListItems},
 "id", 
 ["product2", "product3", "product4"]
)
```

id로 &quot;product2&quot; 및 &quot;product3&quot;이 있는 두 개체가 포함된 listObject를 반환합니다.
