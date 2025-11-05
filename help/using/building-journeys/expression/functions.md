---
solution: Journey Optimizer
product: journey optimizer
title: 함수
description: 여정 표현식의 함수에 대해 알아보기
feature: Journeys
role: Developer
level: Experienced
keywords: 함수, 표현식, 편집기, 여정, 데이터, 조작
exl-id: 5b978eef-7d3e-41fe-bb08-0cf37c3b125d
version: Journey Orchestration
source-git-commit: 99053c6c1327818645adc4ab9a5d3dd30eb96b87
workflow-type: tm+mt
source-wordcount: '855'
ht-degree: 9%

---

# 함수 {#functions}

함수는 Adobe Journey Optimizer에서 동적 여정 표현식의 기본 구성단위입니다. 이를 통해 실시간으로 데이터를 변환, 계산, 유효성 검사 및 조작하여 개인화된 고객 경험을 만들 수 있습니다. 60개 이상의 함수를 직관적인 카테고리로 구성하여 고객 여정의 모든 단계에서 정교한 조건을 구축하고, 복잡한 계산을 수행하고, 데이터 중심의 의사 결정을 내릴 수 있습니다.

## 함수 이해

여정 표현식의 함수는 일관된 구문 패턴을 따릅니다.

`<function name>`(`<expression as param 1>`, `<expression as param 2>`, ... ,`<expression as param N>`)

**키 특성:**

* **여러 서명**: 함수에는 다양한 사용 사례를 수용할 수 있도록 다른 서명(순서가 지정된 매개 변수의 다른 집합)이 있을 수 있습니다
* **유형별 반환**: 각 함수에는 반환된 특정 유형(문자열, 정수, 부울, 날짜, 목록 등)이 있습니다.
* **0에서 N까지 매개 변수**: 함수에서 0-N 식을 순서가 지정된 매개 변수로 사용할 수 있으므로 사용 방법에 유연성을 제공합니다.

## 함수를 사용하는 이유

함수를 통해 다음과 같은 작업을 수행할 수 있습니다.

* **동적 조건 만들기** - 실시간 데이터 평가를 기반으로 여정 경로 분기
* **규모에 맞게 개인화** - 고객 데이터 및 행동 통찰력을 사용하여 콘텐츠 및 경험 맞춤화
* **의사 결정 자동화** - 수동 개입 없이 지능형 논리 구축
* **데이터 변환** - 호환성을 보장하기 위해 데이터 형식을 변환, 서식 지정 및 조작합니다.
* **계산 수행** - 수학 연산 및 통계 분석 실행
* **입력 유효성 검사** - 작업을 수행하기 전에 데이터 품질 및 완전성을 확인하십시오.

## 범주별 함수

기본 목적에 따라 구성된 기능을 탐색하여 요구 사항에 적합한 도구를 신속하게 찾을 수 있습니다.

### Adobe Experience Platform {#aep-functions}

**대상자 세분화 및 타깃팅**

대상 멤버십을 평가하여 Adobe Experience Platform에 정의된 고객 세그먼트를 기반으로 개인화된 여정 경로를 만듭니다.

| 함수 | 설명 |
|----------|-------------|
| [inAudience](../functions/functioninaudience.md) | 개인이 특정 대상자에 속하는지 확인 |

[Adobe Experience Platform 기능 세부 사항 보기 →](../functions/functioninaudience.md)

### 집계 함수 {#aggregation-functions}

**통계 계산 및 데이터 요약**

값 집합에 대해 계산을 수행하여 평균, 개수, 합계 및 최소/최대 값과 같은 통찰력을 얻습니다. 데이터 중심의 의사 결정에 필수적입니다.

| 함수 | 설명 |
|----------|-------------|
| [avg](../functions/aggregation-functions.md#avg) | 평균 값 계산 |
| [count](../functions/aggregation-functions.md#count) | null이 아닌 요소 계산 |
| [countOnlyNull](../functions/aggregation-functions.md#countOnlyNull) | null 값만 계산 |
| [countWithNull](../functions/aggregation-functions.md#countWithNull) | null을 포함한 모든 요소 계산 |
| [distinctCount](../functions/aggregation-functions.md#distinctCount) | null이 아닌 고유한 값 계산 |
| [distinctCountWithNull](../functions/aggregation-functions.md#distinctCountWithNull) | null을 포함한 고유 값 계산 |
| [max](../functions/aggregation-functions.md#max) | 최대 값 찾기 |
| [min](../functions/aggregation-functions.md#min) | 최소값 찾기 |
| [sum](../functions/aggregation-functions.md#sum) | 총 합계 계산 |

[모든 집계 함수 보기 →](../functions/aggregation-functions.md)

### 전환 함수 {#conversion-functions}

**데이터 형식 변환**

작업과 데이터 소스 간의 호환성을 보장하기 위해 다양한 유형(문자열, 정수, 십진수, 부울, 날짜, 기간) 간에 데이터를 변환합니다.

| 함수 | 설명 |
|----------|-------------|
| [toBool](../functions/conversion-functions.md#toBool) | 부울로 변환 |
| [toDateOnly](../functions/conversion-functions.md#toDateOnly) | 날짜로만 변환(시간 없음) |
| [toDateTime](../functions/conversion-functions.md#toDateTime) | 시간이 있는 날짜로 변환 |
| [toDateTimeOnly](../functions/conversion-functions.md#toDateTimeOnly) | 시간대 없이 날짜-시간으로 전환 |
| [toDecimal](../functions/conversion-functions.md#toDecimal) | 십진수로 변환 |
| [toDuration](../functions/conversion-functions.md#toDuration) | 기간으로 변환 |
| [toInteger](../functions/conversion-functions.md#toInteger) | 정수로 변환 |
| [toString](../functions/conversion-functions.md#toString) | 문자열로 변환 |

[모든 전환 함수 보기 →](../functions/conversion-functions.md)

### 날짜 함수 {#date-functions}

**날짜 및 시간 조작**

날짜, 시간 및 시간대를 사용하여 시간 기반 조건을 만들고, 작업을 예약하며, 임시 계산을 수행합니다.

| 함수 | 설명 |
|----------|-------------|
| [currentTimeInMillis](../functions/date-functions.md#currentTimeInMillis) | 현재 시간(밀리초) 가져오기 |
| [inLastDays](../functions/date-functions.md#inLastDays) | 날짜가 지난 N일 이내인지 확인 |
| [inLastHours](../functions/date-functions.md#inLastHours) | 날짜가 지난 N시간 이내인지 확인 |
| [inLastMonths](../functions/date-functions.md#inLastMonths) | 날짜가 지난 N개월 이내인지 확인 |
| [inLastYears](../functions/date-functions.md#inLastYears) | 날짜가 최근 N년 이내인지 확인 |
| [inNextDays](../functions/date-functions.md#inNextDays) | 날짜가 다음 N일 이내인지 확인 |
| [inNextHours](../functions/date-functions.md#inNextHours) | 날짜가 다음 N시간 이내인지 확인 |
| [inNextMonths](../functions/date-functions.md#inNextMonths) | 날짜가 다음 N개월 이내인지 확인 |
| [inNextYears](../functions/date-functions.md#inNextYears) | 날짜가 다음 N년 이내인지 확인 |
| [now](../functions/date-functions.md#now) | 현재 날짜-시간 가져오기 |
| [nowWithDelta](../functions/date-functions.md#nowWithDelta) | 오프셋으로 현재 시간 가져오기 |
| [setHours](../functions/date-functions.md#setHours) | 날짜-시간의 특정 시간 설정 |
| [setDays](../functions/date-functions.md#setDays) | 날짜-시간의 특정 일 설정 |
| [updateTimeZone](../functions/date-functions.md#updateTimeZone) | 날짜-시간의 시간대 업데이트 |

[모든 날짜 함수 보기 →](../functions/date-functions.md)

### 목록 함수 {#list-functions}

**컬렉션 조작 및 분석**

배열과 목록을 필터링, 정렬, 변환 및 분석하여 복잡한 데이터 구조를 사용하고 집합 작업을 수행합니다.

| 함수 | 설명 |
|----------|-------------|
| [distinct](../functions/list-functions.md#distinct) | 고유 값 가져오기(null 제외) |
| [distinctWithNull](../functions/list-functions.md#distinctWithNull) | 고유 값 가져오기(null 포함) |
| [필터](../functions/list-functions.md#filter) | 기준을 기반으로 목록 필터링 |
| [getListItem](../functions/list-functions.md#getListItem) | 특정 인덱스에서 항목 가져오기 |
| [in](../functions/list-functions.md#in) | 목록에 값이 있는지 확인 |
| [교차](../functions/list-functions.md#intersect) | 목록 간 공통 요소 찾기 |
| [제한](../functions/list-functions.md#limit) | 반환되는 항목 수 제한 |
| [listSize](../functions/list-functions.md#listSize) | 목록 크기 가져오기 |
| [serializeList](../functions/list-functions.md#serializeList) | 목록을 문자열로 변환 |
| [sort](../functions/list-functions.md#sort) | 목록 요소 정렬 |

[모든 목록 함수 보기 →](../functions/list-functions.md)

### 수학 함수 {#math-functions}

**수학 연산**

데이터 처리 및 비즈니스 논리를 위한 수치 계산 및 변환을 수행합니다.

| 함수 | 설명 |
|----------|-------------|
| [random](../functions/math-functions.md#random) | 난수 생성(0-1) |
| [round](../functions/math-functions.md#round) | 가장 가까운 정수로 반올림 |

[모든 수학 함수 보기 →](../functions/math-functions.md)

### 문자열 함수 {#string-functions}

**텍스트 조작 및 유효성 검사**

다이내믹 콘텐츠 생성 및 조건부 논리를 위해 텍스트 데이터를 처리, 변환, 검색 및 검증합니다.

| 함수 | 설명 |
|----------|-------------|
| [concat](../functions/string-functions.md#concat) | 문자열 연결 |
| [contain](../functions/string-functions.md#contain) | 문자열에 하위 문자열이 포함되어 있는지 확인 |
| [containIgnoreCase](../functions/string-functions.md#containIgnoreCase) | 포함 확인(대/소문자 구분 안 함) |
| [endWith](../functions/string-functions.md#endWith) | 문자열이 접미사로 끝나는지 확인 |
| [endWithIgnoreCase](../functions/string-functions.md#endWithIgnoreCase) | 확인 다음으로 끝남(대/소문자 구분 안 함) |
| [equalIgnoreCase](../functions/string-functions.md#equalIgnoreCase) | 문자열 비교(대/소문자 구분 안 함) |
| [indexOf](../functions/string-functions.md#indexOf) | 첫 번째 발생 위치 찾기 |
| [isEmpty](../functions/string-functions.md#isEmpty) | 문자열이 비어 있는지 확인 |
| [isNotEmpty](../functions/string-functions.md#isNotEmpty) | 문자열이 비어 있지 않은지 확인 |
| [lastIndexOf](../functions/string-functions.md#lastIndexOf) | 마지막 발생 위치 찾기 |
| [length](../functions/string-functions.md#length) | 문자열 길이 가져오기 |
| [lower](../functions/string-functions.md#lower) | 소문자로 변환 |
| [matchRegExp](../functions/string-functions.md#matchRegExp) | 정규 표현식 일치 |
| [notEqualIgnoreCase](../functions/string-functions.md#notEqualIgnoreCase) | 같지 않음 확인(대/소문자 구분 안 함) |
| [replace](../functions/string-functions.md#replace) | 첫 번째 발생 횟수 바꾸기 |
| [replaceAll](../functions/string-functions.md#replaceAll) | 모든 발생 항목 바꾸기 |
| [split](../functions/string-functions.md#split) | 문자열을 배열로 분할 |
| [startWith](../functions/string-functions.md#startWith) | 문자열이 접두사로 시작하는지 확인 |
| [startWithIgnoreCase](../functions/string-functions.md#startWithIgnoreCase) | 다음으로 시작 확인(대/소문자 구분 안 함) |
| [substr](../functions/string-functions.md#substr) | 하위 문자열 추출 |
| [trim](../functions/string-functions.md#trim) | 선행/후행 공백 제거 |
| [upper](../functions/string-functions.md#upper) | 대문자로 변환 |
| [uuid](../functions/string-functions.md#uuid) | UUID 생성 |

[모든 문자열 함수 보기 →](../functions/string-functions.md)

## 다음 단계

사용 가능한 기능을 이해했으므로 다음을 살펴보십시오.

* **[고급 표현식 편집기](expressionadvanced.md)** - 고급 편집기를 사용하여 복잡한 표현식을 만드는 방법에 대해 알아봅니다.
* **[식 구문](generalities.md)** - 여정 식을 작성하기 위한 구문 규칙을 기본으로 제공합니다.
* **[연산자](operators.md)** - 함수를 사용하여 논리를 빌드할 수 있는 연산자를 검색합니다.
* **[필드 참조](field-references.md)** - 식에서 데이터 필드를 참조하는 방법 이해
