---
product: journey optimizer
title: 문자열 함수
description: 문자열 함수에 대해 알아보기
feature: Journeys
role: Developer
level: Experienced
keywords: 문자열, 함수, 표현식, 여정, 텍스트, 조작
version: Journey Orchestration
source-git-commit: bb47ca4957129a4d05aa3d7286409eef0cb62143
workflow-type: tm+mt
source-wordcount: '1127'
ht-degree: 15%

---

# 문자열 함수 {#string-functions}

문자열 함수를 사용하면 여정 표현식 내에서 텍스트 값을 조작하고 작업할 수 있습니다. 이러한 기능은 고객 여정의 텍스트 처리, 유효성 검사, 변형 및 분석에 필수적입니다.

다음을 수행해야 하는 경우 문자열 함수 사용:

* 여러 텍스트 값 연결 및 결합([concat](#concat))
* 특정 텍스트 패턴 또는 하위 문자열 검색([contain](#contain), [containIgnoreCase](#containIgnoreCase), [indexOf](#indexOf), [lastIndexOf](#lastIndexOf), [matchRegExp](#matchRegExp))
* 대/소문자를 구분하지 않거나 대/소문자를 구분하지 않는 일치와 문자열 비교([equalIgnoreCase](#equalIgnoreCase), [notEqualIgnoreCase](#notEqualIgnoreCase))
* 확인 문자열 시작 및 종료([startWith](#startWith), [startWithIgnoreCase](#startWithIgnoreCase), [endWith](#endWith), [endWithIgnoreCase](#endWithIgnoreCase))
* 하위 문자열 작업([substr](#substr))을 사용하여 텍스트 일부 추출
* 텍스트를 대문자 또는 소문자로 변환([upper](#upper), [lower](#lower), [trim](#trim))
* 문자열이 비어 있거나 특정 값([isEmpty](#isEmpty), [isNotEmpty](#isNotEmpty))을 포함하는지 확인하십시오.
* 텍스트 패턴을 새 값으로 바꾸기([replace](#replace), [replaceAll](#replaceAll))
* 추가 처리를 위해 문자열을 배열로 분할([split](#split))
* 문자열 길이([length](#length))를 가져오거나 고유 식별자([uuid](#uuid))를 생성합니다.

문자열 함수는 포괄적인 텍스트 조작 기능을 제공하여 여정 표현식의 텍스트 콘텐츠를 기반으로 하는 정교한 데이터 처리 및 조건부 논리를 가능하게 합니다.

## concat {#concat}

두 개의 문자열 매개 변수 또는 문자열 목록을 연결합니다.

+++구문

`concat(<parameters>)`

+++

+++매개변수

| 매개변수 | 유형 |
|-----------|------------------|
| 목록 | listString |
| 문자열 | 문자열 |

+++

+++서명 및 반환된 유형

`concat(<string>,<string>)`

`concat(<listString>)`

문자열을 반환합니다.

+++

+++예

`concat("Hello","World")`

&quot;HelloWorld&quot;를 반환합니다.

`concat(["Hello"," ","World"])`

&quot;Hello World&quot;를 반환합니다.

+++

## contain {#contain}

두 번째 인수 문자열이 첫 번째 인수 문자열에 포함되어 있는지 확인합니다.

+++구문

`contain(<parameters>)`

+++

+++매개변수

* 문자열

+++

+++서명 및 반환된 유형

`contain(<string>,<string>)`

부울 반환.

+++

+++예

`contain("rowing is great", "great")`

true를 반환합니다.

+++

## containIgnoreCase {#containIgnoreCase}

두 번째 인수 문자열이 대소문자를 고려하지 않고 첫 번째 인수 문자열에 포함되어 있는지 확인합니다.

+++구문

`containIgnoreCase(<parameters>)`

+++

+++매개변수

| 매개변수 | 유형 |
|-----------|------------------|
| 문자열 | 문자열 |
| 문자열 검색됨 | 문자열 |

+++

+++서명 및 반환된 유형

`containIgnoreCase(<string>,<string>)`

부울 반환.

+++

+++예

`containIgnoreCase("rowing is great", "GREAT")`

true를 반환합니다.

+++

## endWith {#endWith}

두 번째 매개 변수가 첫 번째 매개 변수의 접미사인 경우 true를 반환합니다.

+++구문

`endWith(<parameters>)`

+++

+++매개변수

| 매개변수 | 유형 |
|-----------|------------------|
| 문자열 | 문자열 |
| 접미사 | 문자열 |

+++

+++서명 및 반환된 유형

`endWith(<string>,<string>)`

부울 반환.

+++

+++예

`endWith("Hello World", "World")`

true를 반환합니다.

`endWith("Hello World", "Hello")`

false를 반환합니다.

+++

## endWithIgnoreCase {#endWithIgnoreCase}

첫 번째 인수 문자열이 대소문자를 고려하지 않고 특정 문자열(두 번째 인수 문자열)로 끝나는지 확인합니다.

+++구문

`endWithIgnoreCase(<parameters>)`

+++

+++매개변수

| 매개변수 | 유형 |
|-----------|------------------|
| 문자열 | 문자열 |
| 접미사 | 문자열 |

+++

+++서명 및 반환된 유형

`endWithIgnoreCase(<string>,<string>)`

부울 반환.

+++

+++예

`endWithIgnoreCase("rowing is great", "AT")`

true를 반환합니다.

+++

## equalIgnoreCase {#equalIgnoreCase}

대/소문자 고려 사항을 무시하면서 첫 번째 인수 문자열과 두 번째 인수 문자열을 비교합니다.

+++구문

`equalIgnoreCase(<parameters>)`

+++

+++매개변수

* 문자열

+++

+++서명 및 반환된 유형

`equalIgnoreCase(<string>,<string>)`

부울 반환.

+++

+++예

`equalIgnoreCase("rowing is great", "rowing is GREAT")`

true를 반환합니다.

+++

## indexOf {#indexOf}

두 번째 매개 변수의 첫 번째 발생 횟수 위치(첫 번째 인수에서)를 반환합니다. 일치하는 항목이 없으면 -1을 반환합니다.

+++구문

`indexOf(<parameters>)`

+++

+++매개변수

| 매개변수 | 유형 |
|-----------|------------------|
| 문자열 | 문자열 |
| 지정된 값 | 문자열 |

+++

+++서명 및 반환된 유형

`indexOf(<string>,<string>)`

정수 반환.

+++

+++예

`indexOf("Hello", "l")`

2를 반환합니다.

설명:

&quot;Hello&quot;에서 &quot;l&quot;의 첫 번째 발생은 위치 2에 있다.

+++

## isEmpty {#isEmpty}

매개 변수의 문자열에 문자가 없으면 true를 반환합니다.

+++구문

`isEmpty(<parameters>)`

+++

+++매개변수

* 문자열

+++

+++서명 및 반환된 유형

`isEmpty(<string>)`

부울 반환.

+++

+++예

`isEmpty("")`

true를 반환합니다.

`isEmpty("Hello World")`

false를 반환합니다.

+++

## isNotEmpty {#isNotEmpty}

매개 변수의 문자열이 비어 있지 않으면 true를 반환합니다.

+++구문

`isNotEmpty(<parameters>)`

+++

+++매개변수

* 문자열

+++

+++서명 및 반환된 유형

`isNotEmpty(<string>)`

부울 반환.

+++

+++예

`isNotEmpty("")`

false를 반환합니다.

`isNotEmpty("hello")`

true를 반환합니다.

+++

## lastIndexOf {#lastIndexOf}

두 번째 매개 변수의 마지막 발생 횟수 위치(첫 번째 인수에서)를 반환합니다. 일치하는 항목이 없으면 -1을 반환합니다.

+++구문

`lastIndexOf(<parameters>)`

+++

+++매개변수

| 매개변수 | 유형 |
|-----------|------------------|
| 문자열 | 문자열 |
| 지정된 값 | 문자열 |

+++

+++서명 및 반환된 유형

`lastIndexOf(<string>,<string>)`

정수 반환.

+++

+++예

`lastIndexOf("Hello", "l")`

3을 반환합니다.

설명:

&quot;Hello&quot;에서 &quot;l&quot;의 마지막 발생은 위치 3에 있다.

+++

## length {#length}

매개 변수에서 문자열 식의 문자 수를 반환합니다.

+++구문

`length(<parameters>)`

+++

+++매개변수

* 문자열

+++

+++서명 및 반환된 유형

`length(<string>)`

정수 반환.

+++

+++예

`length("Hello World")`

11을 반환합니다.

+++

## lower {#lower}

매개 변수의 소문자 버전을 반환합니다.

+++구문

`lower(<parameter>)`

+++

+++매개변수

* 문자열

+++

+++서명 및 반환된 유형

`lower(<string>)`

문자열을 반환합니다.

+++

+++예

`lower("A")`

&quot;a&quot;를 반환합니다.

+++

## matchRegExp {#matchRegExp}

첫 번째 매개 변수의 문자열이 두 번째 매개 변수의 정규 표현식과 일치하면 true를 반환합니다. 자세한 내용은 [이 페이지](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html)를 참조하세요.

+++구문

`matchRegExp(<parameters>)`

+++

+++매개변수

| 매개변수 | 유형 |
|--- |--- |
| 문자열 | 문자열 |
| regexp | 문자열 |

+++

+++서명 및 반환된 유형

`matchRegExp(<string>,<string>)`

부울 반환.

+++

+++예

`matchRegExp("12345", "\\d+")`

true를 반환합니다.

+++

## notEqualIgnoreCase {#notEqualIgnoreCase}

대/소문자 고려 사항을 무시한 채 첫 번째 인수 문자열과 두 번째 인수 문자열이 다른지 확인합니다.

+++구문

`notEqualIgnoreCase(<parameters>)`

+++

+++매개변수

* 문자열

+++

+++서명 및 반환된 유형

`notEqualIgnoreCase(<string>,<string>)`

부울 반환.

+++

+++예

`notEqualIgnoreCase(@event{iOSPushPermissionAllowed.device.model}, "iPad")`

+++

## replace {#replace}

대상 문자열과 일치하는 첫 번째 발생 횟수를 기본 문자열의 대체 문자열로 바꿉니다.

교체는 문자열 시작부터 끝까지 진행됩니다. 예를 들어, 문자열 &quot;aaa&quot;에서 &quot;aa&quot;를 &quot;b&quot;로 바꾸면 &quot;ab&quot;가 아닌 &quot;ba&quot;가 생성됩니다.

+++구문

`replace(<parameters>)`

+++

+++매개변수

| 매개변수 | 유형 |
|-----------|--------------|
| 기본 | 문자열 |
| 대상 | 문자열(RegExp) |
| 교체 | 문자열 |

+++

+++서명 및 반환된 유형

`replace(<base>,<target>,<replacement>)`

문자열을 반환합니다.

+++

+++예

`replace("Hello World", "l", "x")`

&quot;Hexlo World&quot;를 반환합니다.

**RegExp가 있는 예제:**

대상 매개 변수는 RegExp이므로 바꿀 문자열에 따라 일부 문자를 이스케이프해야 할 수 있습니다. 다음은 한 예입니다.

* 평가할 문자열: `|OFFER_A|OFFER_B`
* 프로필 특성 `#{ExperiencePlatform.myFieldGroup.profile.myOffers}`에서 제공함
* 바꿀 문자열: `|OFFER_A`
* 문자열을 `''`(으)로 대체함
* `\\`자 앞에 `|`을(를) 추가해야 합니다.

표현식:

`replace(#{ExperiencePlatform.myFieldGroup.profile.myOffers}, '\\|OFFER_A', '')`

반환된 문자열: `|OFFER_B`

지정된 속성에서 대체할 문자열을 빌드할 수도 있습니다.

`replace(#{ExperiencePlatform.myFieldGroup.profile.myOffers}, '\\|' + #{ExperiencePlatform.myFieldGroup.profile.myOfferCode}, '')`

+++

## replaceAll {#replaceAll}

대상 문자열과 일치하는 모든 발생 항목을 기본 문자열의 대체 문자열로 바꿉니다.

교체는 문자열 시작부터 끝까지 진행됩니다. 예를 들어, 문자열 &quot;aaa&quot;에서 &quot;aa&quot;를 &quot;b&quot;로 바꾸면 &quot;ab&quot;가 아닌 &quot;ba&quot;가 생성됩니다.

+++구문

`replaceAll(<parameters>)`

+++

+++매개변수

| 매개변수 | 유형 |
|-----------|--------------|
| 기본 | 문자열 |
| 대상 | 문자열(RegExp) |
| 교체 | 문자열 |

+++

+++서명 및 반환된 유형

`replaceAll(<baseString>,<sourceString>,<replacementString>)`

문자열을 반환합니다.

+++

+++예

`replaceAll("Hello World", "l", "x")`

&quot;Hexxo Worxd&quot;를 반환합니다.

대상 매개 변수는 RegExp이므로 바꿀 문자열에 따라 일부 문자를 이스케이프해야 할 수 있습니다. [replace](#replace) 함수의 예제를 참조하십시오.

+++

## split {#split}

첫 번째 인수 문자열을 구분 문자 문자열(정규 표현식일 수 있는 두 번째 인수 문자열)로 분할하여 문자열(토큰) 목록을 생성합니다.

+++구문

`split(<parameters>)`

+++

+++매개변수

| 매개변수 | 유형 |
|-----------|------------------|
| 입력 문자열 | 문자열 |
| 구분 문자 문자열 | 문자열 |

+++

+++서명 및 반환된 유형

`split(<input string>, <separator string>)`

listString을 반환합니다.

+++

+++예

`split("A_B_C", "_")`

`["A","B","C"]` 반환

값이 &quot;20.45.2.3434&quot;인 이벤트 필드 &#39;event.appVersion&#39;이 있는 예

`split(@event{event.appVersion}, "\\.")`

`["20", "45", "2", "3434"]` 반환

+++

## startWith {#startWith}

두 번째 매개 변수가 첫 번째 매개 변수의 접두사인 경우 true를 반환합니다.

+++구문

`startWith(<parameters>)`

+++

+++매개변수

| 매개변수 | 유형 |
|-------------|--------|
| 문자열 | 문자열 |
| 접두사 | 문자열 |

+++

+++서명 및 반환된 유형

`startWith(<string>,<string>)`

부울 반환.

+++

+++예

`startWith("Hello World", "Hello")`

true를 반환합니다.

`startWith("Hello World", "World")`

false를 반환합니다.

+++

## startWithIgnoreCase {#startWithIgnoreCase}

두 번째 매개 변수가 첫 번째 매개 변수의 접두사이면 대소문자를 고려하지 않고 true를 반환합니다.

+++구문

`startWithIgnoreCase(<parameters>)`

+++

+++매개변수

| 매개변수 | 유형 |
|-------------|--------|
| 문자열 | 문자열 |
| 접두사 | 문자열 |

+++

+++서명 및 반환된 유형

`startWithIgnoreCase(<string>,<string>)`

부울 반환.

+++

+++예

`startWithIgnoreCase("rowing is great", "RO")`

true를 반환합니다.

+++

## substr {#substr}

시작 색인과 끝 색인 사이에 있는 문자열 식의 하위 문자열을 반환합니다. 끝 색인이 정의되지 않으면 시작 색인과 끝 사이에 있습니다.

+++구문

`substr(<parameters>)`

+++

+++매개변수

| 매개변수 | 유형 |
|-------------|----------|
| 문자열 | 문자열 |
| beginIndex | 정수 |
| endIndex | 정수 |

+++

+++서명 및 반환된 유형

`substr(<string>,<beginIndex>)`

`substr(<string>,<beginIndex>,<endIndex>)`

문자열을 반환합니다.

+++

+++예

`substr("Hello World",6)`

&quot;World&quot;를 반환합니다.

`substr("Hello World", 0, 5)`

&quot;Hello&quot;를 반환합니다.

+++

## trim {#trim}

시작 및 끝 공백을 제거합니다.

+++구문

`trim(<parameters>)`

+++

+++매개변수

| 매개변수 | 유형 |
|-----------|------------------|
| 문자열 | 문자열 |

+++

+++서명 및 반환된 유형

`trim(<string>)`

문자열을 반환합니다.

+++

+++예

`trim(" Hello ")`

&quot;Hello&quot;를 반환합니다.

+++

## upper {#upper}

매개 변수의 대문자 버전을 반환합니다.

+++구문

`upper(<parameters>)`

+++

+++서명 및 반환된 유형

`upper(<string>)`

문자열을 반환합니다.

+++

+++예

`upper("b")`

&quot;B&quot;를 반환합니다.

+++

## uuid {#uuid}

임의의 UUID(Universal Unique IDentifier)를 생성합니다.

+++구문

`uuid()`

+++

+++매개변수 

이 함수에는 매개 변수가 필요하지 않습니다.

+++

+++서명 및 반환된 유형

`uuid()`

문자열을 반환합니다.

+++

+++예

`uuid()`

&quot;79e70b7f-8a85-400b-97a1-9f9826121553&quot;를 반환합니다.

+++

