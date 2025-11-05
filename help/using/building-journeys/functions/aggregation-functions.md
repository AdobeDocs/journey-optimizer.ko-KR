---
product: journey optimizer
title: 집계 함수
description: 집계 함수에 대해 알아보기
feature: Journeys
role: Developer
level: Experienced
keywords: 집계, 함수, 표현식, 여정, avg, count, max, min, sum
version: Journey Orchestration
source-git-commit: af1babe501a5b2c6a67730396a8f5e2c5d85e60a
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 8%

---

# 집계 함수 {#aggregation-functions}

집계 함수는 값 집합에 대해 계산을 수행하고 단일 값을 반환하는 데 사용됩니다. 이러한 함수는 여정 표현식에서 목록 및 배열로 작업할 때 특히 유용합니다.

## avg {#avg}

목록 또는 두 표현식으로 지정된 표현식 세트 중 평균 값을 반환합니다. Null 값은 무시됩니다.

+++구문

`avg(<parameter>)`

+++

+++매개변수

지원되는 유형:

* list정수
* listDecimal
* decimal
* 정수

+++

+++서명 및 반환된 유형

`avg(<listInteger>)`

`avg(<listDecimal>)`

`avg(<decimal>,<decimal>)`

`avg(<decimal>,<integer>)`

`avg(<integer>,<decimal>)`

`avg(<integer>,<integer>)`

십진수를 반환합니다.

+++

+++예

`avg(@event{BarBeacon.inventory},5)`

`avg([10,3,8])`

7.0을 반환합니다

`avg(10.2, 3)`

6.6 반환.

+++

## count {#count}

null 값을 고려하지 않는 목록의 요소를 계산합니다.

+++구문

`count(<listAny>)`

`count(<listObject>)`

+++

+++매개변수

| 매개변수 | 유형 | 설명 |
|-----------|------------------|------------------|
| listToprocess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly 또는 listObject | 처리할 목록. listObject의 경우 필드 참조여야 합니다. listObject는 null 개체를 포함할 수 없습니다. |

+++

+++서명 및 반환된 유형

`count(<listAny>)`

정수 반환.

+++

+++예

`count([10,2,10,null])`

3을 반환합니다.

`count(@event{my_event.productListItems})`

지정된 개체 배열(listObject 형식)에 있는 개체 수를 반환합니다. 비고: listObject는 null 개체를 포함할 수 없습니다.

+++

## countOnlyNull {#countOnlyNull}

목록의 null 값 수를 계산합니다.

**참고:** 매개 변수 `<listObject>`은(는) 이 함수에서 지원되지 않습니다.

+++구문

`countOnlyNull(<listAny>)`

+++

+++매개변수

| 매개변수 | 유형 |
|-----------|------------------|
| listToprocess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

+++

+++서명 및 반환된 유형

`countOnlyNull(<listAny>)`

정수 반환.

+++

+++예

`countOnlyNull([10,2,10,null])`

1을 반환합니다.

+++

## countWithNull {#countWithNull}

null 값을 포함하여 목록의 모든 요소를 계산합니다.

**참고:** 매개 변수 `<listObject>`은(는) 이 함수에서 지원되지 않습니다.

+++구문

`countWithNull(<listAny>)`

+++

+++매개변수

| 매개변수 | 유형 |
|-----------|------------------|
| listToprocess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

+++

+++서명 및 반환된 유형

`countWithNull(<listAny>)`

정수 반환.

+++

+++예

`countWithNull([10,2,10,null])`

4를 반환합니다.

+++

## distinctCount {#distinctCount}

null 값을 무시하는 다른 값의 수를 계산합니다.

+++구문

`distinctCount(<listAny>)`

+++

+++매개변수

| 매개변수 | 유형 | 설명 |
|-----------|------------------|------------------|
| listToprocess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly 또는 listObject | 처리할 목록. listObject의 경우 필드 참조여야 합니다. |
| keyAttributeName | 문자열 | 이 매개 변수는 선택 사항이며 listObject에만 사용됩니다. 매개변수를 제공하지 않으면 모든 속성의 값이 동일한 경우 객체가 복제된 것으로 간주됩니다. 그렇지 않으면, 지정된 속성에 동일한 값이 있으면 객체가 복제된 것으로 간주됩니다. |

+++

+++서명 및 반환된 유형

`distinctCount(<listAny>)`

정수 반환.

`distinctCount(<listObject>)`

`distinctCount(<listObject>,<string>)`

개체 목록을 반환합니다.

+++

+++예

`distinctCount([10,2,10,null])`

2를 반환합니다.

`distinctCount(@event{my_event.productListItems})`

지정된 개체 배열(listObject 형식)에서 엄격히 구별되는 개체 수를 반환합니다.

`distinctCount(@event{my_event.productListItems}, "SKU")`

고유한 &quot;SKU&quot; 특성 값 {}이(가) 있는 개체 수를 반환합니다.

+++

## distinctCountWithNull {#distinctCountWithNull}

null 값을 포함하여 다른 값의 수를 계산합니다.

**참고:** 매개 변수 `<listObject>`은(는) 이 함수에서 지원되지 않습니다.

+++구문

`distinctCountWithNull(<listAny>)`

+++

+++매개변수

| 매개변수 | 유형 |
|-----------|------------------|
| listToprocess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

+++

+++서명 및 반환된 유형

`distinctCountWithNull(<listAny>)`

정수 반환.

+++

+++예

`distinctCountWithNull([10,2,10,null])`

3을 반환합니다.

+++

## max {#max}

목록 또는 두 표현식으로 지정된 표현식 세트 중 최대값을 반환합니다. Null 값은 무시됩니다.

+++구문

`max(<parameter>)`

+++

+++매개변수

* listDuration
* list정수
* listDecimal
* listDateTime
* listDateTimeOnly
* listDateOnly
* 지속 시간
* 정수
* decimal
* dateTime
* dateTimeOnly

+++

+++서명 및 반환된 유형

`max(<listDuration>)`

기간을 반환합니다.

`max(<listInteger>)`

기간을 반환합니다.

`max(<listDateTimeOnly>)`

시간대를 고려하지 않고 날짜/시간을 반환합니다.

`max(<listDateTime>)`

날짜/시간을 반환합니다.

`max(<listDateOnly>)`

날짜를 반환합니다.

`max(<listDecimal>)`

십진수를 반환합니다.

`max(<decimal>,<decimal>)`

십진수를 반환합니다.

`max(<duration>,<duration>)`

기간을 반환합니다.

`max(<dateTime>,<dateTime>)`

날짜/시간을 반환합니다.

`max(<dateTimeOnly>,<dateTimeOnly>)`

시간대를 고려하지 않고 날짜/시간을 반환합니다.

`max(<integer>,<integer>)`

정수 반환.

+++

+++예

`max(@event{BarBeacon.inventory},5)`

`max([10,3,8])`

10을 반환합니다.

`max([10,null,8])`

10을 반환합니다.

+++

## min {#min}

목록 또는 두 표현식으로 지정된 표현식 세트 중 최소값을 반환합니다. Null 값은 무시됩니다.

+++구문

`min(<parameters>)`

+++

+++매개변수

* listDuration
* list정수
* listDecimal
* listDateTime
* listDateTimeOnly
* listDateOnly
* 지속 시간
* 정수
* decimal
* dateTime
* dateTimeOnly

+++

+++서명 및 반환된 유형

`min(<listDuration>)`

기간을 반환합니다.

`min(<listInteger>)`

기간을 반환합니다.

`min(<listDateTimeOnly>)`

시간대를 고려하지 않고 날짜/시간을 반환합니다.

`min(<listDateTime>)`

날짜/시간을 반환합니다.

`min(<listDateOnly>)`

날짜를 반환합니다.

`min(<listDecimal>)`

십진수를 반환합니다.

`min(<decimal>,<decimal>)`

십진수를 반환합니다.

`min(<duration>,<duration>)`

기간을 반환합니다.

`min(<dateTime>,<dateTime>)`

날짜/시간을 반환합니다.

`min(<dateTimeOnly>,<dateTimeOnly>)`

시간대를 고려하지 않고 날짜/시간을 반환합니다.

`min(<integer>,<integer>)`

정수 반환.

+++

+++예

`min(@event{BarBeacon.inventory},5)`

`min([10,3,8])`

3을 반환합니다.

`min([10,null,8])`

8을 반환합니다.

+++

## sum {#sum}

표현식 집합의 값 합계를 반환합니다. Null 값은 무시됩니다.

+++구문

`sum(<parameters>)`

+++

+++매개변수

* list정수
* listDecimal
* 지속 시간
* 정수
* decimal

+++

+++서명 및 반환된 유형

`sum(<listDecimal>)`

십진수를 반환합니다.

`sum(<listInteger>)`

정수 반환.

`sum(<integer>,<integer>)`

정수 반환.

`sum(<decimal>,<decimal>)`

십진수를 반환합니다.

+++

+++예

`sum(@event{BarBeacon.inventory},5)`

`sum([10,3,8])`

21을 반환합니다.

`sum([10.5,null,8.1])`

18.6을 반환합니다.

+++
