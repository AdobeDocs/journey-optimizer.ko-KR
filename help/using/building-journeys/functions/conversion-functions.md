---
product: journey optimizer
title: 전환 함수
description: 전환 함수에 대해 알아봅니다
feature: Journeys
role: Developer
level: Experienced
keywords: 전환, 함수, 표현식, 여정, 유형, 캐스트
version: Journey Orchestration
source-git-commit: 7d75abf6b428becc8b535a63421e85cca417daac
workflow-type: tm+mt
source-wordcount: '940'
ht-degree: 6%

---

# 전환 함수 {#conversion-functions}

변환 함수를 사용하면 여정 표현식 내에서 데이터를 한 유형에서 다른 유형으로 변환할 수 있습니다. 이러한 기능은 다양한 데이터 소스 및 작업으로 작업할 때 데이터 호환성과 적절한 유형 처리를 보장하기 위해 필수적입니다.

다음과 같은 작업을 수행할 때 변환 함수를 사용합니다.

* 문자열 값을 숫자, 부울 또는 날짜 유형으로 변환
* 다양한 형식과 표현 간에 날짜 및 시간 변환
* 정수 및 십진수 유형 간 숫자 값 캐스트
* 비교 및 작업을 위한 유형 호환성 보장
* 다른 형식 형식을 가질 수 있는 외부 소스의 데이터 처리

각 전환 기능은 유형별 규칙과 극단적 사례를 자동으로 처리하므로 여정 표현식에서 보다 안정적이고 예측 가능한 데이터 변환을 만들 수 있습니다.

## toBool {#toBool}

인수 유형에 따라 인수 값을 부울 값으로 변환합니다.

* From string: 문자열 값을 부울로 변환하고 문자열 값이 &quot;true&quot;이면 &quot;true&quot;를 반환하고 그렇지 않으면 false를 반환합니다
* 숫자에서: 숫자 값이 0이 아니면 true이고, 그렇지 않으면 false입니다

+++구문

`toBool(<parameter>)`

+++

+++매개변수

* decimal
* 부울
* 문자열
* 정수

+++

+++서명 및 반환된 유형

`toBool(<decimal>)`

`toBool(<boolean>)`

`toBool(<string>)`

`toBool(<integer>)`

부울 반환.

+++

+++예

`toBool("true")`

`toBool(1)`

true를 반환합니다.

`toBool("this is not a boolean")`

false를 반환합니다.

+++

## toDateOnly {#toDateOnly}

인수를 dateOnly 형식 값으로 변환합니다. 데이터 형식에 대한 자세한 내용은 이 [섹션](../expression/data-types.md)을 참조하세요.

+++구문

`toDateOnly(<parameters>)`

+++

+++매개변수

| 매개변수 | 유형 |
|-----------|------------------|
| 날짜를 &quot;YYYY-MM-DD&quot;로 나타내는 문자열 표현(XDM 형식). 또한 ISO-8601 형식을 지원합니다. **전체 날짜** 부분만 고려됩니다([RFC 3339, 섹션 5.6](https://www.rfc-editor.org/rfc/rfc3339#section-5.6) 참조). | 문자열 |
| 날짜 시간 | dateTime |
| 시간대 없는 날짜 시간 | dateTimeOnly |
| 에포크의 정수 값(밀리초) | 정수 |

+++

+++서명 및 반환된 유형

`toDateOnly(<dateTime>)`

`toDateOnly(<dateTimeOnly>)`

`toDateOnly(<string>)`

`toDateOnly(<integer>, <integer>, <integer>)`

dateOnly 형식 값을 반환합니다.

+++

+++예

`toDateOnly("2023-08-18")`

`toDateOnly("2023-08-18T00:00:00.000Z")`

`toDateOnly("2023-08-18T00:00:00")`

all은 2023-08-18을 나타내는 dateOnly 개체를 반환합니다.

`toDateOnly(#{ExperiencePlatform.ProfileFieldGroup.person.birthDate})`

dateOnly를 반환합니다.

+++

## toDateTime {#toDateTime}

유형에 따라 매개 변수를 날짜/시간 값으로 변환합니다.

+++구문

`toDateTime(<parameters>)`

+++

+++매개변수

| 매개변수 | 유형 |
|-----------|------------------|
| ISO-8601 형식의 날짜 시간 | 문자열 |
| 시간대 id | 문자열 |
| 시간대 없는 날짜 시간 | dateTimeOnly |
| 에포크의 정수 값(밀리초) | 정수 |

+++

+++서명 및 반환된 유형

`toDateTime(<string>)`

`toDateTime(<stringified time zone id>, <dateTimeOnly>)`

`toDateTime(<integer>)`

**dateTime** 반환

+++

+++예

`toDateTime ("2023-08-18T23:17:59.123Z")`

2023-08-18T23 반환:17:59.123Z

`toDateTime(toDateTimeOnly("UTC", "2023-08-18T23:17:59.123"))`

2023-08-18T23 반환:17:59.123Z

`toDateTime(1560762190189)`

2023-06-17T09:03:10.189Z 반환

+++

>[!NOTE]
>
>시간대 ID는 문자열 상수여야 합니다. 필드 참조나 식이 될 수 없습니다. 데이터 형식에 대한 자세한 내용은 [이 페이지](../expression/data-types.md)를 참조하세요.

## toDateTimeOnly {#toDateTimeOnly}

인수 값을 날짜/시간 전용 값으로 변환합니다.

+++구문

`toDateTimeOnly(<parameters>)`

+++

+++매개변수

| 매개변수 | 유형 |
|-----------|------------------|
| ISO-8601 또는 &quot;YYYY-MM-DD&quot; 형식의 날짜 시간(XDM 날짜 형식) | 문자열 |
| 날짜 시간 | dateTime |

+++

+++서명 및 반환된 유형

`toDateTimeOnly(<dateTime>)`

`toDateTimeOnly(<string>)`

시간대를 고려하지 않고 날짜/시간을 반환합니다.

+++

+++예

`toDateTimeOnly ("2023-08-18")`

2023-08-18T00:00:00.000을 나타내는 dateTime을 반환합니다

`toDateTimeOnly(now())`

+++

## toDecimal {#toDecimal}

인수 유형에 따라 인수 값을 십진수 값으로 변환합니다.

+++구문

`toDecimal(<parameter>)`

+++

+++매개변수

| 매개변수 | 설명 |
|--- |--- |
| 문자열 | 문자열 값을 소수로 변환합니다. |
| dateTime | 날짜를 밀리초 단위로 변환(에포크 밀리초) |
| 부울 | true이면 부울 값을 1, false이면 부울 값으로 변환합니다. |
| 정수 | 소수로 변환합니다(예: ).: 1이 1.0이 됨) |

+++

+++서명 및 반환된 유형

`toDecimal(<integer>)`

`toDecimal(<decimal>)`

`toDecimal(<string>)`

`toDecimal(<boolean>)`

십진수를 반환합니다.

+++

+++예

`toDecimal("4.0")`

4.0을 반환합니다

+++

## toDuration {#toDuration}

인수 값을 duration으로 변환합니다. 데이터 형식에 대한 자세한 내용은 [이 페이지](../expression/data-types.md)를 참조하세요.

+++구문

`toDuration(<parameter>)`

+++

+++매개변수

| 매개변수 | 설명 |
|--- |--- |
| 문자열 | ISO-8601 기간 형식 PnDTnHnMn.nS를 기반으로 하는 형식이며, 일 수는 정확히 24시간으로 간주됩니다. |
| 정수 | 시간(밀리초) |

문자열 표현식: 허용되는 형식은 ISO-8601 기간 형식 PnDTnHnMn.nS를 기반으로 하며, 일은 정확히 24시간으로 간주됩니다.

문자열은 ASCII 음수 또는 양수 기호로 표시되는 선택적 기호로 시작합니다. 음수이면 전체 기간이 무효화됩니다. ASCII 문자 &quot;P&quot;는 다음으로 대문자 또는 소문자로 구성됩니다. 그 다음에는 4개의 섹션이 있는데, 각각의 섹션은 숫자와 접미사로 구성되어 있다. 섹션에는 일, 시간, 분 및 초 동안 &quot;D&quot;, &quot;H&quot;, &quot;M&quot; 및 &quot;S&quot;의 ASCII 접미사가 있으며, 대문자나 소문자로 허용됩니다. 접미사는 순서대로 수행되어야 합니다. ASCII 문자 &quot;T&quot;는 시간, 분 또는 초 구간의 첫 번째 항목(있는 경우) 전에 발생해야 합니다. 4개의 섹션 중 적어도 하나가 있어야 하며, &quot;T&quot;가 있으면 &quot;T&quot; 다음에 적어도 하나의 섹션이 있어야 합니다. 각 섹션의 숫자 부분은 하나 이상의 ASCII 숫자로 구성되어야 합니다. 숫자는 ASCII 음수 또는 양수 기호로 접두사로 사용될 수 있습니다. 일, 시간 및 분 수는 함께 구문 분석해야 합니다. 초 수는 선택적 분수와 함께 로 구문 분석해야 합니다. 소수점은 점 또는 쉼표일 수 있습니다. 분수 부분은 0부터 9자리까지 가질 수 있다.

+++

+++서명 및 반환된 유형

`toDuration(<string>)`

`toDuration(<integer>)`

기간을 반환합니다.

+++

+++예

`toDuration("PT10H")`

10시간의 기간을 반환합니다.

`toDuration("PT4S")`

기간을 4초로 반환합니다.

`toDuration(4000)`

기간을 4초로 반환합니다.

+++

## toInteger {#toInteger}

인수 값을 정수로 변환합니다.

+++구문

`toInteger(<parameter>)`

+++

+++매개변수

| 매개변수 | 설명 |
|--- |--- |
| 문자열 | 문자열 값을 정수로 변환합니다. |
| dateTime | 날짜를 밀리초 단위로 변환(에포크 밀리초) |
| decimal | 소수 부분을 제거하여 정수로 변환합니다(예: 1.5가 1이 됨). |
| 부울 | true이면 부울 값을 1, false이면 부울 값으로 변환합니다. |

+++

+++서명 및 반환된 유형

`toInteger(<dateTime>)`

`toInteger(<decimal>)`

`toInteger(<integer>)`

`toInteger(<string>)`

`toInteger(<boolean>)`

정수를 반환합니다.

+++

+++예

`toInteger("4")`

4를 반환합니다.

+++

## toString {#toString}

인수 유형에 따라 인수 값을 문자열 값으로 변환합니다. 데이터 형식에 대한 자세한 내용은 [이 페이지](../expression/data-types.md)를 참조하세요.

+++구문

`toString(<parameter>)`

+++

+++매개변수

| 매개변수 | 설명 |
|--- |--- |
| dateTime | 날짜를 UTC 날짜 형식으로 변환 |
| dateTimeOnly | 날짜를 UTC 날짜 형식으로 변환 |
| 지속 시간 | 문자열로 해당 시간(밀리초)으로 변환 |
| 정수 | 값의 문자열 표현으로 변환(1이 &quot;1&quot;이 됨) |
| decimal | 값의 문자열 표현으로 변환(1.5가 &quot;1.5&quot;가 됨) |
| 부울 | true이면 &#39;true&#39;로, false이면 &#39;false&#39;로 부울 값 변환 |

+++

+++서명 및 반환된 유형

`toString(<dateTimeOnly>)`

`toString(<dateTime>)`

`toString(<duration>)`

`toString(<boolean>)`

`toString(<integer>)`

`toString(<decimal>)`

문자열을 반환합니다.

+++

+++예

`toString(4)`

&quot;4&quot;를 반환합니다.

`toString(#{ExperiencePlatform.test_date.person.birthDate}))`

지정된 dateOnly 필드(XDM 날짜 필드)의 문자열 표현을 반환합니다(예: &quot;2023-08-18&quot;).

`toString(toDuration(1520))`

&quot;PT1.52S&quot;를 반환합니다.

+++

