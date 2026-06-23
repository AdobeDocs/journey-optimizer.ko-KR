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
feature_v2: []
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1339
ht-degree: 6%

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

+++ AI 기술 자료 참조

이 단원에는 이 주제와 관련된 해석, 검색 및 질문 답변을 지원하기 위한 구조화된 지식이 포함되어 있습니다.

이해를 돕기 위해 이 정보를 이 페이지의 설명서와 통합해야 합니다. 두 소스 모두 독립적으로 사용하기 위한 것은 아닙니다. 이 페이지에서는 기능에 대해 설명하지만, 용어, 의도, 적용 가능성 및 제약 조건을 명확히 하는 데 도움이 되는 추가 컨텍스트를 제공합니다.

* **TL;DR:** 이 페이지는 집계, 전환, 날짜/시간, 목록, 수학, 문자열 및 Adobe Experience Platform 대상 함수를 다루는 여정 고급 표현식 편집기에서 사용할 수 있는 60개 이상의 기본 제공 함수에 대한 범주화된 참조입니다.

**의도:**

* 분류된 함수 테이블을 탐색하여 작업에 적합한 함수 식별
* 변환 함수를 사용하여 문자열, 정수, 십진수, 부울, 날짜 및 기간 간에 데이터 유형 변환
* `inLastDays`, `inNextHours`, `nowWithDelta` 등의 함수를 사용하여 날짜 기반 필터링 수행
* `contain`, `replace`, `split` 및 `trim`과(와) 같은 함수를 사용하여 문자열 값 조작 및 유효성 검사
* `count`, `avg`, `sum` 및 `distinctCount`과(와) 같은 집계 함수를 사용하여 컬렉션에 대한 통계 계산 수행
* `inAudience` 함수를 사용하여 여정 조건에서 대상 멤버십 확인

**용어집:**

* **집계 함수**: 값 컬렉션 *(제품별)*&#x200B;에서 단일 값(개수, 합계, 평균, 최소, 최대)을 계산하는 함수
* **전환 함수**: 값을 한 데이터 형식에서 다른 데이터 형식으로 캐스팅하는 함수(예: `toString`, `toDateTime`, `toDuration`) *(제품별)*
* **날짜 함수**: 여정 식 *(제품별)*&#x200B;에서 날짜, 시간 및 시간대 값을 사용하여 작업하는 함수입니다.
* **목록 함수**: 배열/컬렉션 데이터 *(제품별)*&#x200B;을(를) 필터링, 정렬 및 분석하는 함수입니다.
* **inAudience**: 프로필이 지정된 Adobe Experience Platform 대상 세그먼트 *(제품별)에 속하는지 여부를 확인하는 함수입니다.*

**보호 기능:**

* 함수는 일관된 구문을 따릅니다. `functionName(param1, param2, ...)`
* 함수는 서로 다른 사용 사례를 처리하기 위해 여러 개의 서명(서로 다른 매개 변수 세트)을 가질 수 있습니다
* 각 함수에는 고정 반환 유형이 있습니다. 반환 유형이 표현식 컨텍스트에서 예상하는 것과 일치하는지 확인합니다.
* 여정 표현식 편집기에서 사용할 수 있는 기능은 개인화 편집기의 기능과 다릅니다

**용어:**

* 정식 이름: 함수 — 약어: 없음 — 변형: 내장 함수, 표현식 함수
* 동의어: &quot;집계 함수&quot; = &quot;통계 함수&quot;; &quot;전환 함수&quot; = &quot;유형 캐스팅 함수&quot;
* 혼동하지 않음: 여정 표현식 함수 ≠ 개인화 편집기 함수 (서로 다른 세트)

**FAQ:**

* **Q: 여정 표현식 편집기에 사용할 수 있는 함수 수는 몇 개입니까?** — 집계, 전환, 날짜, 목록, 수학, 문자열 및 Adobe Experience Platform을 포함하여 범주로 구성된 60개 이상의 함수.
* **Q: 프로필이 여정 조건의 대상에 속하는지 어떻게 확인합니까?** — 대상 식별자와 함께 `inAudience` 함수를 사용합니다.
* **Q: 현재 날짜 및 시간 오프셋을 일 수로 가져오는 데 어떤 함수를 사용해야 합니까?** — `nowWithDelta(N, "days")`을(를) 사용하여 현재 시간으로부터 dateTime 오프셋을 가져옵니다.
* **Q: 함수를 호출하는 방법에 따라 다른 형식을 반환할 수 있습니까?** — 함수에는 시그니처마다 특정 반환 유형이 있지만 단일 함수 이름에는 여러 매개 변수 집합과 반환 유형이 있는 여러 시그니처가 있을 수 있습니다.
* **Q: `count`과(와) `countWithNull`의 차이점은 무엇입니까?** — `count`은(는) null이 아닌 요소만 계산하며, `countWithNull`은(는) null을 포함한 모든 요소를 계산합니다.

+++
