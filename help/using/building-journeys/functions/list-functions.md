---
product: journey optimizer
title: 목록 함수
description: 목록 함수에 대해 알아보기
feature: Journeys
role: Developer
level: Experienced
keywords: 목록, 함수, 표현식, 여정, 배열, 컬렉션
version: Journey Orchestration
source-git-commit: 0331f8fe2439d41c08ad88a6d0bd95dd150bab90
workflow-type: tm+mt
source-wordcount: '1144'
ht-degree: 9%

---

# 목록 함수 {#list-functions}

목록 함수를 사용하면 여정 표현식 내에서 값 컬렉션을 조작하고 작업할 수 있습니다. 이러한 기능은 고객 여정의 배열과 목록을 필터링, 정렬, 변환 및 분석하는 데 필수적입니다.

다음과 같은 작업을 수행할 때 목록 함수를 사용합니다.

* 기준에 따라 컬렉션에서 특정 항목 필터링 및 추출
* 목록 요소를 오름차순 또는 내림차순으로 정렬 및 구성
* 중복 항목을 제거하고 목록에서 고유 값을 가져옵니다.
* 컬렉션 내에 값이 있는지 확인
* 목록에서 반환되는 항목 수 제한
* 목록을 다른 형식 또는 데이터 형식으로 변환
* 목록 간 공통 요소 찾기와 같은 집합 작업 수행

목록 함수는 복잡한 데이터 구조 작업을 위한 강력한 도구를 제공하며 복잡한 데이터 조작과 수집 콘텐츠를 기반으로 하는 조건부 논리를 가능하게 합니다.

## distinct {#distinct}

주어진 목록의 고유 값 또는 개체를 반환합니다. Null 항목은 무시됩니다.

+++구문

`distinct(<parameters>)`

+++

+++매개변수

| 매개변수 | 유형 | 설명 |
|-----------|------------------|------------------|
| listToprocess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly 또는 listObject | 처리할 목록. listObject의 경우 필드 참조여야 합니다. |
| keyAttributeName | 문자열 | 이 매개 변수는 선택 사항이며 listObject에만 사용됩니다. 매개변수를 제공하지 않으면 모든 속성의 값이 동일한 경우 객체가 복제된 것으로 간주됩니다. 그렇지 않으면, 지정된 속성에 동일한 값이 있으면 객체가 복제된 것으로 간주됩니다. |

+++

+++서명 및 반환된 유형

`distinct(<listInteger>)`

정수 목록을 반환합니다.

`distinct(<listDecimal>)`

소수점 목록을 반환합니다.

`distinct(<listString>)`

문자열 목록을 반환합니다.

`distinct(<listDateTimeOnly>)`

시간대를 고려하지 않고 날짜/시간 목록을 반환합니다.

`distinct(<listDateTime>)`

날짜/시간 목록을 반환합니다.

`distinct(<listDateOnly>)`

날짜 목록을 반환합니다.

`distinct(<listBoolean>)`

부울 목록을 반환합니다.

`distinct(<listDuration>)`

기간 목록을 반환합니다.

`distinct(<listObject>)`

`distinct(<listObject>,<string>)`

개체 목록을 반환합니다.

+++

+++예

`distinct([10,2,10,null])`

`[10, 2]`을(를) 반환합니다

+++

## distinctWithNull {#distinctWithNull}

주어진 목록의 고유 값 또는 개체를 반환합니다. 목록에 null 항목이 하나 이상 있으면 반환된 목록에 null 항목이 표시됩니다.

+++구문

`distinctWithNull(<parameters>)`

+++

+++매개변수

| 매개변수 | 유형 | 설명 |
|-----------|------------------|------------------|
| listToprocess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly | 처리할 목록. |

+++

+++서명 및 반환된 유형

`distinctWithNull(<listInteger>)`

정수 목록을 반환합니다.

`distinctWithNull(<listDecimal>)`

소수점 목록을 반환합니다.

`distinctWithNull(<listString>)`

문자열 목록을 반환합니다.

`distinctWithNull(<listDateTimeOnly>)`

시간대를 고려하지 않고 날짜/시간 목록을 반환합니다.

`distinctWithNull(<listDateTime>)`

날짜/시간 목록을 반환합니다.

`distinctWithNull(<listDateOnly>)`

날짜 목록을 반환합니다.

`distinctWithNull(<listBoolean>)`

부울 목록을 반환합니다.

`distinctWithNull(<listDuration>)`

기간 목록을 반환합니다.

+++

+++예

`distinctWithNull([10,2,10,null])`

[10, 2, null] 반환

+++

**참고:** 매개 변수 `<listObject>`은(는) 이 함수에서 지원되지 않습니다.

## filter {#filter}

지정된 키 값 중 하나와 일치하는 키 특성을 가진 개체와 함께 listObject를 반환합니다.

+++구문

`filter(<parameters>)`

+++

+++매개변수

| 매개변수 | 유형 | 설명 |
|-----------|------------------|------------------|
| listTofilter | listObject | 필터링할 객체 목록입니다. 필드 참조여야 합니다. |
| keyAttributeName | 문자열 | 해당 목록의 개체에서 필터링용 키로 사용되는 속성 이름 |
| 키 값 목록 | list | 필터링에 사용할 키 값 배열 |

+++

+++서명 및 반환된 유형

`filter(listObject, string, listString)`

`filter(listObject, string, listInteger)`

`filter(listObject, string, listDecimal)`

`filter(listObject, string, listDateTime)`

`filter(listObject, string, listDateTimeOnly)`

`filter(listObject, string, listDateOnly)`

`filter(listObject, string, listDuration)`

`filter(listObject, string, listBoolean)`

listObject를 반환합니다.

+++

+++예

다음은 수신 이벤트 &quot;myevent&quot;에서 전달된 페이로드의 예입니다.

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
 @event{myevent.productListItems},
 "id", 
 ["product2", "product3", "product4"]
)
```

id로 &quot;product2&quot; 및 &quot;product3&quot;을 사용하는 두 개체가 포함된 listObject를 반환합니다.

+++

## getListItem {#getListItem}

지정된 인덱스에서 목록의 항목을 반환합니다.

+++구문

`getListItem(<parameters>)`

+++

+++매개변수

| 매개변수 | 유형 |
|-----------|------------------|
| list | listString |
| list | list부울 |
| list | list정수 |
| list | listDecimal |
| list | listDuration |
| list | listDateTime |
| list | listDateTimeOnly |
| list | listDateOnly |
| 색인 | 정수 |

+++

+++서명 및 반환된 유형

`getListItem(<listInteger>,<index>)`

정수 반환.

`getListItem(<listDecimal>,<index>)`

십진수를 반환합니다.

`getListItem(<listString>,<index>)`

문자열을 반환합니다.

`getListItem(<listDateTimeOnly>,<index>)`

시간대를 고려하지 않고 날짜/시간을 반환합니다.

`getListItem(<listDateTime>,<index>)`

날짜/시간을 반환합니다.

`getListItem(<listDateOnly>,<index>)`

날짜 목록을 반환합니다.

`getListItem(<listBoolean>,<index>)`

부울 반환.

`getListItem(<listDuration>,<index>)`

기간을 반환합니다.

+++

+++예

`getListItem([10, 2, 3], 1)`

&quot;2&quot; 반환

`getListItem(["A", "B", "C"], 2)`

&quot;C&quot; 반환

값이 &quot;20.45.2.3434&quot;인 이벤트 필드 &#39;event.appVersion&#39;이 있는 예

`split(@event{event.appVersion}, "\\.")`

`["20", "45", "2", "3434"]` 반환

`getListItem(split(@event{event.appVersion}, "\\."), 0)`

&quot;20&quot; 반환

+++

## in {#in}

첫 번째 인수 값이 목록에 있는지 확인합니다. 각 인수 값에 대해 같음 을 통해 확인이 수행됩니다. 인수 값이 발견되면 true를 반환하고, 그렇지 않으면 false를 반환합니다.

`<expression>`의 형식은 목록의 항목과 일치해야 합니다. 미리 알림으로 목록의 항목 유형은 서로 일치해야 합니다.

+++구문

`in(<parameters>)`

+++

+++매개변수

| 매개변수 | 유형 |
|-----------|------------------|
| 문자열 | 문자열 |
| 부울 | 부울 |
| 정수 | 정수 |
| 소수 | 소수 |
| 기간 | 기간 |
| 날짜/시간 | 날짜/시간 |
| 날짜/시간만 | 날짜/시간만 |
| 목록 | listString |
| 목록 | list부울 |
| 목록 | list정수 |
| 목록 | listDecimal |
| 목록 | listDuration |
| 목록 | listDateTime |
| 목록 | listDateTimeOnly |
| 목록 | listDateOnly |

+++

+++서명 및 반환된 유형

`in(<integer>,<listInteger>)`

`in(<decimal>,<listDecimal>)`

`in(<string>,<listString>)`

`in(<boolean>,<listBoolean>)`

`in(<dateTimeOnly>,<listDateTimeOnly>)`

`in(<dateTime>,<listDateTime>)`

`in(<dateOnly>,<listDateOnly>)`

`in(<duration>,<listDuration>)`

부울 반환.

+++

+++예

`in(4,[4,5,3,4])`

true를 반환합니다.

`in(8,[4,5,3,4])`

false를 반환합니다.

`in(#{ExperiencePlatform.ProfileFieldGroup.profile.person.gender}, ["male"])`

+++

## intersect {#intersect}

두 입력 목록의 공통 값을 반환합니다. 두 목록 중 하나가 null이면 빈 목록을 반환합니다.

+++구문

`intersect(<parameters>)`

+++

+++매개변수

| 매개변수 | 유형 |
|-----------|------------------|
| 목록 1 | list |
| 목록 2 | list |

+++

+++서명 및 반환된 유형

`intersect(listString,listString)`: listString

`intersect(listDecimal,listDecimal)`: listDecimal

`intersect(listInteger,listInteger)`: list정수

`intersect(listDateTime,listDateTime)`: listDateTime

`intersect(listDateTimeOnly,listDateTimeOnly)`: listDateTimeOnly

`intersect(listDateOnly,listDateOnly)`: listDateOnly

`intersect(listDuration,listDuration)`: listDuration

`intersect(listBoolean,listBoolean)`: list부울

목록을 반환합니다.

+++

+++예

```json
intersect(
    ["sports", "news", "documentary"],
    ["sports", "movies", "documentary"]
)
```

[&quot;sports&quot;, &quot;news&quot;] 반환

```json
intersect(
    #{ExperienceDataPlatform.profile.interests},
    ["sports", "documentary"]
)
```

프로필 속성과 지정된 범주 목록 간의 공통 항목을 반환합니다.

```json
intersect(
    #{ExperienceDataPlatform.profile.interests},
        @event{myEvent.sport_interests}
)
```

프로필 속성과 지정된 이벤트 필드 간의 공통 항목을 반환합니다.

+++

## limit {#limit}

목록의 첫 번째 또는 마지막 N 요소를 반환합니다.

+++구문

`limit(<parameters>)`

+++

+++매개변수

| 매개변수 | 유형 | 설명 |
|-----------|------------------|------------------|
| listToprocess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly 또는 listObject | 고려할 목록입니다. listObject의 경우 필드 참조여야 합니다. |
| numberOfItems | 정수 | 해당 목록에서 반환할 항목 수. |
| 첫 번째 또는 마지막 항목 | 부울 | 이 매개 변수는 선택 사항입니다(기본값: true). true는 첫 번째 항목을 반환합니다. false는 마지막 항목을 반환합니다. |

+++

+++서명 및 반환된 유형

`limit(<listString>,<integer>)`

`limit(<listString>,<integer>,<boolean>)`

문자열 목록을 반환합니다.

`limit(<listInteger>,<integer>)`

`limit(<listInteger>,<integer>,<boolean>)`

정수 목록을 반환합니다.

`limit(<listDecimal>,<integer>)`

`limit(<listDecimal>,<integer>,<boolean>)`

소수점 목록을 반환합니다.

`limit(<listBoolean>,<integer>)`

`limit(<listBoolean>,<integer>,<boolean>)`

부울 목록을 반환합니다.

`limit(<listDateOnly>,<integer>)`

`limit(<listDateOnly>,<integer>,<boolean>)`

날짜 목록을 반환합니다.

`limit(<listDateTimeOnly>,<integer>)`

`limit(<listDateTimeOnly>,<integer>,<boolean>)`

시간대를 고려하지 않고 날짜/시간 목록을 반환합니다.

`limit(<listDateTime>,integer>)`

`limit(<listDateTime>,<integer>,<boolean>)`

날짜/시간 목록을 반환합니다.

`limit(<listDuration>,<integer>)`

`limit(<listDuration>,<integer>,<boolean>)`

기간 목록을 반환합니다.

`limit(<listObject>,<integer>)`

`limit(<listObject>,<integer>,<boolean>)`

개체 목록을 반환합니다.

+++

+++예

`limit(["A", "B", "C", "D", "E"], 3)`

`["A","B","C"]`을(를) 반환합니다

`limit(["A", "B", "C", "D", "E"], 3, false)`

`["C","D","E"]`을(를) 반환합니다

+++

## listSize {#listSize}

목록의 요소 수를 계산합니다.

+++구문

`listSize(<parameters>)`

+++

+++매개변수

| 매개변수 | 유형 | 설명 |
|-----------|------------------|------------------|
| listToprocess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly 또는 listObject | 처리할 목록. listObject의 경우 필드 참조여야 합니다. listObject는 null 개체를 포함할 수 없습니다. |

+++

+++서명 및 반환된 유형

`listSize(<listInteger>)`

`listSize(<listDecimal>)`

`listSize(<listString>)`

`listSize(<listBoolean>)`

`listSize(<listDateTimeOnly>)`

`listSize(<listDateTime>)`

`listSize(<listDateOnly>)`

`listSize(<listDuration>)`

정수를 반환합니다.

`listSize(<listObject>)`

+++

+++예

`listSize([10,2,3])`

3을 반환합니다.

`listSize(@event{my_event.productListItems})`

지정된 개체 배열(listObject 형식)에 있는 개체 수를 반환합니다.

+++

## serializeList {#serializeList}

지정된 목록(listObject를 제외한 모든 유형)을 문자열로 변환합니다.

+++구문

`serializeList(<parameters>)`

+++

+++매개변수

| 매개변수 | 유형 | 설명 |
|-----------|------------------|------------------|
| listToprocess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly | 문자열로 변환할 목록입니다. |
| 분리자 | 문자열 | 출력 문자열에서 각 목록 요소 사이의 구분 기호입니다. |
| addQuotes | 부울 | 이 매개 변수는 출력 문자열의 각 요소에 따옴표(true)를 포함해야 하는지 여부를 나타냅니다(false). |

+++

+++서명 및 반환된 유형

`serializeList(<listInteger>,<string>,<boolean>)`

`serializeList(<listDecimal>,<string>,<boolean>)`

`serializeList(<listString>,<string>,<boolean>)`

`serializeList(<listBoolean>,<string>,<boolean>)`

`serializeList(<listDateTimeOnly>,<string>,<boolean>)`

`serializeList(<listDateTime>,<string>,<boolean>)`

`serializeList(<listDateOnly>,<string>,<boolean>)`

`serializeList(<listDuration>,<string>,<boolean>)`

문자열을 반환합니다.

+++

+++예

`serializeList(["Hello","World"], " ", false)`

&quot;Hello World&quot;를 반환합니다.

`serializeList(["Hello", "World"], ",", true)`

&quot;&quot;Hello&quot;,&quot;World&quot;&quot;를 반환합니다.

+++

## sort {#sort}

값 또는 개체 목록을 원래 순서로 정렬합니다.

+++구문

`sort(<parameters>)`

+++

+++매개변수

| 매개변수 | 유형 | 설명 |
|-----------|------------------|------------------|
| listToSort | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly 또는 listObject | 정렬할 목록입니다. listObject의 경우 필드 참조여야 합니다. |
| keyAttributeName | 문자열 | 이 매개 변수는 listObject에만 사용할 수 있습니다. 해당 목록의 개체에 있는 특성 이름은 정렬의 키로 사용됩니다. |
| 정렬 순서 | 부울 | 오름차순(true) 또는 내림차순(false) |

+++

+++서명 및 반환된 유형

`sort(<listInteger>,<boolean>)`

정수 목록을 반환합니다.

`sort(<listDecimal>,<boolean>)`

소수점 목록을 반환합니다.

`sort(<listString>,<boolean>)`

문자열 목록을 반환합니다.

`sort(<listDateTimeOnly>,<boolean>)`

시간대를 고려하지 않고 날짜/시간 목록을 반환합니다.

`sort(<listDateTime>,<boolean>)`

날짜/시간 목록을 반환합니다.

`sort(<listDateOnly>,<boolean>)`

날짜 목록을 반환합니다.

`sort(<listBoolean>,<boolean>)`

부울 목록을 반환합니다.

`sort(<listObject>,<string>,<boolean>)`

개체 목록을 반환합니다.

+++

+++예

`sort(["A", "C", "B"], true)`

`["A","B","C"]`을(를) 반환합니다

`sort([1, 3, 2], false)`

`[3, 2, 1]`을(를) 반환합니다

`sort(@event{my_event.productListItems}, "SKU", true)`

SKU 속성으로 정렬된 listObject 반환(오름차순)

+++

