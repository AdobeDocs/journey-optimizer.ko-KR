---
product: journey optimizer
title: 집계 함수
description: 집계 함수에 대해 알아보기
feature: Journeys
role: Developer
level: Experienced
keywords: 집계, 함수, 표현식, 여정, avg, count, max, min, sum
version: Journey Orchestration
exl-id: 871a5212-5b94-4a54-bf1d-276022be3c95
feature_v2: []
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1105
ht-degree: 5%

---

# 집계 함수 {#aggregation-functions}

집계 함수는 값 집합에 대해 계산을 수행하고 요약된 단일 결과를 반환합니다. 이러한 함수를 사용하면 평균을 계산하고, 최소값과 최대값을 찾고, 요소를 계산하고, 숫자 값을 합하여 여정 표현식 내에서 데이터를 분석할 수 있습니다.

다음을 수행해야 하는 경우 집계 함수를 사용합니다.

* 목록 또는 배열에서 통계값 계산([avg](#avg), [합계](#sum), [min](#min), [max](#max))
* null 값을 포함하거나 제외하는 옵션이 있는 컬렉션의 요소 계산([count](#count), [countOnlyNull](#countOnlyNull), [countWithNull](#countWithNull))
* 데이터 집합([distinctCount](#distinctCount), [distinctCountWithNull](#distinctCountWithNull)) 내에서 고유한 값 확인
* 계산된 지표를 기반으로 데이터 기반 의사 결정

집계 함수는 특정 동작에 따라 Null 값을 자동으로 처리하므로 누락되거나 정의되지 않은 값이 포함될 수 있는 실제 데이터를 보다 쉽게 사용할 수 있습니다.


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

+++예시

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

| 매개 변수 | 유형 | 설명 |
|-----------|------------------|------------------|
| listToprocess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly 또는 listObject | 처리할 목록. listObject의 경우 필드 참조여야 합니다. listObject는 null 개체를 포함할 수 없습니다. |

+++

+++서명 및 반환된 유형

`count(<listAny>)`

정수 반환.

+++

+++예시

`count([10,2,10,null])`

3을 반환합니다.

`count(@event{my_event.productListItems})`

지정된 개체 배열(listObject 형식)에 있는 개체 수를 반환합니다. 비고: listObject는 null 개체를 포함할 수 없습니다.

+++

## countOnlyNull {#countOnlyNull}

목록의 null 값 수를 계산합니다.

+++구문

`countOnlyNull(<listAny>)`

+++

+++매개변수

| 매개 변수 | 유형 |
|-----------|------------------|
| listToprocess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

+++

+++서명 및 반환된 유형

`countOnlyNull(<listAny>)`

정수 반환.

+++

+++예시

`countOnlyNull([10,2,10,null])`

1을 반환합니다.

+++

**참고:** 매개 변수 `<listObject>`은(는) 이 함수에서 지원되지 않습니다.

## countWithNull {#countWithNull}

null 값을 포함하여 목록의 모든 요소를 계산합니다.

+++구문

`countWithNull(<listAny>)`

+++

+++매개변수

| 매개 변수 | 유형 |
|-----------|------------------|
| listToprocess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

+++

+++서명 및 반환된 유형

`countWithNull(<listAny>)`

정수 반환.

+++

+++예시

`countWithNull([10,2,10,null])`

4를 반환합니다.

+++

**참고:** 매개 변수 `<listObject>`은(는) 이 함수에서 지원되지 않습니다.

## distinctCount {#distinctCount}

null 값을 무시하는 다른 값의 수를 계산합니다.

+++구문

`distinctCount(<listAny>)`

+++

+++매개변수

| 매개 변수 | 유형 | 설명 |
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

+++예시

`distinctCount([10,2,10,null])`

2를 반환합니다.

`distinctCount(@event{my_event.productListItems})`

지정된 개체 배열(listObject 형식)에서 엄격히 구별되는 개체 수를 반환합니다.

`distinctCount(@event{my_event.productListItems}, "SKU")`

고유한 &quot;SKU&quot; 속성 값{}이 있는 개체 수를 반환합니다.

+++

## distinctCountWithNull {#distinctCountWithNull}

null 값을 포함하여 다른 값의 수를 계산합니다.

+++구문

`distinctCountWithNull(<listAny>)`

+++

+++매개변수

| 매개 변수 | 유형 |
|-----------|------------------|
| listToprocess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

+++

+++서명 및 반환된 유형

`distinctCountWithNull(<listAny>)`

정수 반환.

+++

+++예시

`distinctCountWithNull([10,2,10,null])`

3을 반환합니다.

+++

**참고:** 매개 변수 `<listObject>`은(는) 이 함수에서 지원되지 않습니다.

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

+++예시

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

+++예시

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

+++예시

`sum(@event{BarBeacon.inventory},5)`

`sum([10,3,8])`

21을 반환합니다.

`sum([10.5,null,8.1])`

18.6을 반환합니다.

+++

+++ AI 기술 자료 참조

이 단원에는 이 주제와 관련된 해석, 검색 및 질문 답변을 지원하기 위한 구조화된 지식이 포함되어 있습니다.

이해를 돕기 위해 이 정보를 이 페이지의 설명서와 통합해야 합니다. 두 소스 모두 독립적으로 사용하기 위한 것은 아닙니다. 이 페이지에서는 기능에 대해 설명하지만, 용어, 의도, 적용 가능성 및 제약 조건을 명확히 하는 데 도움이 되는 추가 컨텍스트를 제공합니다.

* **TL;DR:** 이 페이지에서는 목록 및 배열에 대한 평균, 합계, 최소/최대 값, 개수 및 고유 개수를 계산하는 방법에 대해 AJO 여정 표현식에서 사용할 수 있는 모든 집계 함수를 설명합니다.

**의도:**
* `avg`을(를) 사용하여 숫자 값 목록의 평균 계산
* `sum`을(를) 사용하여 목록 또는 이벤트 필드의 숫자 값 합계
* `min` 또는 `max`을(를) 사용하여 목록에서 최소값 또는 최대값 찾기
* `count`, `countOnlyNull` 또는 `countWithNull`을(를) 사용하여 null이 아닌 요소, null 전용 요소 또는 목록의 모든 요소를 계산합니다.
* `distinctCount` 또는 `distinctCountWithNull`을(를) 사용하여 null이 있거나 없는 목록의 고유 값 계산
* 키 매개 변수와 함께 `distinctCount`을(를) 사용하여 listObject의 고유 개체를 특정 키 특성별로 필터링합니다.

**용어집:**
* **listObject**: 복합 개체(필드 참조) 목록입니다. null 개체 *(제품별)은 포함할 수 없습니다.*
* **listAny**: 지원되는 스칼라 유형(문자열, 부울, 정수, 소수점, duration, dateTime, dateTimeOnly, dateOnly) *(제품별)*&#x200B;의 목록입니다
* **Null 값**: 목록에 없거나 정의되지 않은 요소입니다. 함수가 명시적으로 Null을 처리하지 않는 한 대부분의 집계 함수는 Null을 무시합니다(예: `countOnlyNull`, `countWithNull`, `distinctCountWithNull`).

**보호 기능:**
* `countOnlyNull`, `countWithNull` 및 `distinctCountWithNull`은(는) `<listObject>` 매개 변수 형식을 지원하지 않습니다.
* `listObject`의 `distinctCount`에는 인라인 리터럴이 아닌 필드 참조용 목록이 필요합니다.
* `listObject`의 `count`에는 목록이 필드 참조여야 합니다. listObject에는 null 개체가 포함될 수 없습니다.

**용어:**
* 정식 이름: 집계 함수 — 약어: 없음 — 변형: 집계 함수, 컬렉션 함수
* 동의어: &quot;count&quot; = &quot;count non-null elements&quot;; &quot;countWithNull&quot; = &quot;count all elements including null&quot;
* 혼동하지 마십시오. &quot;distinctCount&quot;(null 무시) ≠ &quot;distinctCountWithNull&quot;(null을 고유한 값으로 포함)

**FAQ:**
* **Q: `avg`의 계산에 null 값이 포함됩니까?** — 아니요, `avg`은(는) null 값을 자동으로 무시합니다.
* **Q: `count`과(와) `countWithNull`의 차이점은 무엇입니까?** — `count`은(는) 합계에서 null 값을 제외하는 반면 `countWithNull`은(는) null을 포함한 모든 요소를 계산합니다.
* **Q: listObject에서 `countOnlyNull`을(를) 사용할 수 있습니까?** — 아니요, `<listObject>`은(는) `countOnlyNull`, `countWithNull` 또는 `distinctCountWithNull`에서 지원되지 않습니다.
* **Q: 특정 특성을 기반으로 배열에서 개별 개체를 계산하려면 어떻게 해야 합니까?** — 키 특성 이름을 두 번째 매개 변수로 제공하는 `distinctCount(@event{...}, "attributeName")`을(를) 사용합니다.
* **Q: 목록에 null이 포함되어 있으면 `max`에서 반환하는 것은 무엇입니까?** — `max`은(는) null 값을 무시하고 null이 아닌 요소 중 최대값을 반환합니다.

+++
