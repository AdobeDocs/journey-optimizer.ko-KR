---
title: 문자열 함수 라이브러리
description: 문자열 함수 라이브러리
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 8674ef9e-261b-49d9-800e-367f9f7ef979
source-git-commit: 8a1ec5acef067e3e1d971deaa4b10cffa6294d75
workflow-type: tm+mt
source-wordcount: '1846'
ht-degree: 9%

---

# 문자열 함수 {#string}

개인화 편집기에서 String 함수를 사용하는 방법을 알아봅니다.

## 카멜 대/소문자 {#camelCase}

`camelCase` 함수는 문자열의 각 단어의 첫 번째 문자를 대문자로 바꿉니다.

**구문**

```sql
{%= camelCase(string)%}
```

**예**

다음 함수는 프로필의 주소에서 첫 번째 문자 를 대문자로 표시합니다.

```sql
{%= camelCase(profile.homeAddress.street) %}
```

## 의 문자 코드 {#char-code-at}

`charCodeAt` 함수는 JavaScript의 charCodeAt 함수와 같은 문자의 ASCII 값을 반환합니다. 이 메서드는 문자열과 정수(문자 위치를 정의함)를 입력 인수로 사용하고 해당 ASCII 값을 반환합니다.

**구문**

```sql
{%= charCodeAt(string,int) %}: int
```

**예**

다음 함수는 o의 ASCII 값, 즉 111을 반환합니다.

```sql
{%= charCodeAt("some", 1)%}
```

## Concat {#concate}

`concat` 함수는 2개의 문자열을 하나로 결합합니다.

**구문**

```sql
{%= concat(string,string) %}
```

**예**

다음 함수는 프로필 도시와 국가를 단일 문자열로 결합합니다.

```sql
{%= concat(profile.homeAddress.city,profile.homeAddress.country) %}
```

## 다음 포함 {#contains}

`contains` 함수는 문자열에 지정된 하위 문자열이 포함되어 있는지 확인하는 데 사용합니다.

**구문**

```sql
{%= contains(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| 인수 | 설명 |
| --------- | ----------- |
| `STRING_1` | 확인을 수행하는 문자열입니다. |
| `STRING_2` | 첫 번째 문자열에서 검색할 문자열입니다. |
| `CASE_SENSITIVE` | 검사가 대/소문자를 구분하는지 여부를 결정하는 선택적 매개 변수입니다. 가능한 값은 true (기본값) / false 입니다. |

**예**

* 다음 함수는 프로필 이름에 문자 A(대문자 또는 소문자)가 포함되어 있는지 확인합니다. 이 경우 &#39;true&#39;를 반환하고 그렇지 않으면 &#39;false&#39;를 반환합니다.

  ```sql
  {%= contains(profile.person.name.firstName, "A", false) %}
  ```

* 다음 쿼리는 대소문자 구분을 통해 개인의 이메일 주소에 문자열 &quot;2010@gm&quot;이 포함되어 있는지 확인합니다.

  ```sql
  {%= contains(profile.person.emailAddress,"2010@gm") %}
  ```

## 포함하지 않음{#doesNotContain}

`doesNotContain` 함수는 문자열에 지정된 하위 문자열이 포함되어 있지 않은지 확인하는 데 사용합니다.

**구문**

```sql
{%= doesNotContain(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| 인수 | 설명 |
| --------- | ----------- |
| `STRING_1` | 확인을 수행하는 문자열입니다. |
| `STRING_2` | 첫 번째 문자열에서 검색할 문자열입니다. |
| `CASE_SENSITIVE` | 검사가 대/소문자를 구분하는지 여부를 결정하는 선택적 매개 변수입니다. 가능한 값은 true (기본값) / false 입니다. |

**예**

다음 쿼리는 대소문자 구분을 통해 개인의 이메일 주소에 문자열 &quot;2010@gm&quot;이 포함되어 있지 않은 경우를 결정합니다.

```sql
{%= doesNotContain(profile.person.emailAddress,"2010@gm")%}
```


## 다음으로 끝나지 않음{#doesNotEndWith}

`doesNotEndWith` 함수는 문자열이 지정된 하위 문자열로 끝나지 않은지 확인하는 데 사용합니다.

**구문**

```sql
{%= doesNotEndWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| 인수 | 설명 |
| --------- | ----------- |
| `{STRING_1}` | 확인을 수행하는 문자열입니다. |
| `{STRING_2}` | 첫 번째 문자열에서 검색할 문자열입니다. |
| `{CASE_SENSITIVE}` | 검사가 대/소문자를 구분하는지 여부를 결정하는 선택적 매개 변수입니다. 가능한 값은 true (기본값) / false 입니다. |

**예**

다음 쿼리는 대소문자 구분을 통해 개인의 이메일 주소가 &quot;.com&quot;으로 끝나지 않는 경우를 결정합니다.

```sql
doesNotEndWith(person.emailAddress,".com")
```

## 다음으로 시작하지 않음{#doesNotStartWith}

`doesNotStartWith` 함수는 문자열이 지정된 하위 문자열로 시작되지 않는지 확인하는 데 사용합니다.

**구문**

```sql
{%= doesNotStartWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| 인수 | 설명 |
| --------- | ----------- |
| `{STRING_1}` | 확인을 수행하는 문자열입니다. |
| `{STRING_2}` | 첫 번째 문자열에서 검색할 문자열입니다. |
| `{CASE_SENSITIVE}` | 검사가 대/소문자를 구분하는지 여부를 결정하는 선택적 매개 변수입니다. 가능한 값은 true (기본값) / false 입니다. |

**예**

다음 쿼리는 대/소문자 구분을 통해 개인의 이름이 &quot;Joe&quot;로 시작되지 않는지 여부를 결정합니다.

```sql
{%= doesNotStartWith(person.name,"Joe")%}
```

## 인코딩 64{#encode64}

`encode64` 함수는 URL에 포함될 경우 PI(개인 정보)를 보존하기 위해 문자열을 인코딩하는 데 사용됩니다.

**구문**

```sql
{%= encode64(string) %}
```

## 다음으로 끝남{#endsWith}

`endsWith` 함수는 문자열이 지정된 하위 문자열로 끝나는지 확인하는 데 사용합니다.

**구문**

```sql
{%= endsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| 인수 | 설명 |
| --------- | ----------- |
| `{STRING_1}` | 확인을 수행하는 문자열입니다. |
| `{STRING_2}` | 첫 번째 문자열에서 검색할 문자열입니다. |
| `{CASE_SENSITIVE}` | 검사가 대/소문자를 구분하는지 여부를 결정하는 선택적 매개 변수입니다. 가능한 값은 true (기본값) / false 입니다. |

**예**

다음 쿼리는 대소문자 구분을 통해 개인의 이메일 주소가 &quot;.com&quot;으로 끝나는지 여부를 결정합니다.

```sql
{%= endsWith(person.emailAddress,".com") %}
```


## 같음{#equals}

`equals` 함수는 문자열이 지정된 문자열과 같은지 대/소문자를 구분합니다.

**구문**

```sql
{%= equals(STRING_1, STRING_2) %}
```

| 인수 | 설명 |
| --------- | ----------- |
| `{STRING_1}` | 확인을 수행하는 문자열입니다. |
| `{STRING_2}` | 첫 번째 문자열과 비교할 문자열입니다. |

**예**

다음 쿼리는 대소문자 구분을 통해 개인의 이름이 &quot;John&quot;인지 여부를 결정합니다.

```sql
{%=equals(profile.person.name,"John") %}
```

## 대/소문자 무시와 같음{#equalsIgnoreCase}

`equalsIgnoreCase` 함수는 대/소문자를 구분하지 않고 문자열이 지정된 문자열과 같은지 확인하는 데 사용합니다.

**구문**

```sql
{%= equalsIgnoreCase(STRING_1, STRING_2) %}
```

| 인수 | 설명 |
| --------- | ----------- |
| `{STRING_1}` | 확인을 수행하는 문자열입니다. |
| `{STRING_2}` | 첫 번째 문자열과 비교할 문자열입니다. |

**예**

다음 쿼리는 대소문자 구분 없이 개인의 이름이 &quot;John&quot;인지 여부를 결정합니다.

```sql
{%= equalsIgnoreCase(profile.person.name,"John") %}
```

## 이메일 도메인 추출 {#extractEmailDomain}

`extractEmailDomain` 함수는 전자 메일 주소의 도메인을 추출하는 데 사용됩니다.

**구문**

```sql
{%= extractEmailDomain(string) %}
```

**예**

다음 쿼리는 개인 이메일 주소의 이메일 도메인을 추출합니다.

```sql
{%= extractEmailDomain(profile.personalEmail.address) %}
```

## 통화 포맷 {#format-currency}

`formatCurrency` 함수는 두 번째 인수에서 문자열로 전달된 로케일에 따라 모든 숫자를 해당 언어 구분 통화 표시로 변환하는 데 사용합니다.

**구문**

```sql
{%= formatCurrency(number/double,string) %}: string
```

**예**

이 쿼리는 £56.00 반환

```sql
{%= formatCurrency(56L,"en_GB") %}
```

## URL 호스트 다운로드 {#get-url-host}

`getUrlHost` 함수는 URL의 호스트 이름을 검색하는 데 사용됩니다.

**구문**

```sql
{%= getUrlHost(string) %}: string
```

**예**

```sql
{%= getUrlHost("https://www.myurl.com/contact") %}
```

&quot;www.myurl.com&quot; 반환

## URL 경로 다운로드 {#get-url-path}

`getUrlPath` 함수는 URL의 도메인 이름 뒤에 있는 경로를 검색하는 데 사용됩니다.

**구문**

```sql
{%= getUrlPath(string) %}: string
```

**예**

```sql
{%= getUrlPath("https://www.myurl.com/contact.html") %}
```

&quot;/contact.html&quot; 반환

## URL 프로토콜 다운로드 {#get-url-protocol}

`getUrlProtocol` 함수는 URL의 프로토콜을 검색하는 데 사용됩니다.

**구문**

```sql
{%= getUrlProtocol(string) %}: string
```

**예**

```sql
{%= getUrlProtocol("https://www.myurl.com/contact.html") %}
```

&quot;http&quot; 반환

## 색인 {#index-of}

`indexOf` 함수는 첫 번째 인수에서 두 번째 매개 변수의 첫 번째 발생 횟수 위치를 반환하는 데 사용됩니다. 일치하는 항목이 없으면 -1을 반환합니다.

**구문**

```sql
{%= indexOf(STRING_1, STRING_2) %}: integer
```

| 인수 | 설명 |
| --------- | ----------- |
| `{STRING_1}` | 확인을 수행하는 문자열입니다. |
| `{STRING_2}` | 첫 번째 매개 변수에서 검색할 문자열 |

**예**

```sql
{%= indexOf("hello world","world" ) %}
```

6을 반환합니다.

## 비어 있음 {#isEmpty}

`isEmpty` 함수는 문자열이 비어 있는지 확인하는 데 사용합니다.

**구문**

```sql
{%= isEmpty(string) %}
```

**예**

다음 함수는 프로필의 휴대폰 번호가 비어 있는 경우 &#39;true&#39;를 반환합니다. 그렇지 않으면 &#39;false&#39;를 반환합니다.

```sql
{%= isEmpty(profile.mobilePhone.number) %}
```

## 비어 있지 않음 {#is-not-empty}

`isNotEmpty` 함수는 문자열이 비어 있지 않은지 확인하는 데 사용합니다.

**구문**

```sql
{= isNotEmpty(string) %}: boolean
```

**예**

다음 함수는 프로필의 휴대폰 번호가 비어 있지 않으면 &#39;true&#39;를 반환합니다. 그렇지 않으면 &#39;false&#39;를 반환합니다.

```sql
{%= isNotEmpty(profile.mobilePhone.number) %}
```

## 마지막 색인 {#last-index-of}

`lastIndexOf` 함수는 두 번째 매개 변수의 마지막 발생 횟수 위치(첫 번째 인수에서)를 반환하는 데 사용됩니다. 일치하는 항목이 없으면 -1을 반환합니다.

**구문**

```sql
{= lastIndexOf(STRING_1, STRING_2) %}: integer
```

| 인수 | 설명 |
| --------- | ----------- |
| `{STRING_1}` | 확인을 수행하는 문자열입니다. |
| `{STRING_2}` | 첫 번째 매개 변수에서 검색할 문자열 |

**예**

```sql
{%= lastIndexOf("hello world","o" ) %}
```

7을 반환합니다.

## Left trim {#leftTrim}

`leftTrim` 함수는 문자열의 시작에서 공백을 제거하는 데 사용합니다.

**구문**

```sql
{%= leftTrim(string) %}
```

## 길이 {#length}

`length` 함수는 문자열 또는 식의 문자 수를 가져오는 데 사용됩니다.

**구문**

```sql
{%= length(string) %}
```

**예**

다음 함수는 프로필의 도시 이름 길이를 반환합니다.

```sql
{%= length(profile.homeAddress.city) %}
```

## 좋아요{#like}

`like` 함수는 문자열이 지정된 패턴과 일치하는지 확인하는 데 사용합니다.

**구문**

```sql
{%= like(STRING_1, STRING_2) %}
```

| 인수 | 설명 |
| --------- | ----------- |
| `{STRING_1}` | 확인을 수행하는 문자열입니다. |
| `{STRING_2}` | 첫 번째 문자열과 일치하는 표현식. 식을 만드는 데 지원되는 특수 문자 `%`과(와) `_`이(가) 있습니다. <ul><li>`%`은(는) 0개 이상의 문자를 나타내는 데 사용됩니다.</li><li>`_`은(는) 정확히 하나의 문자를 나타내는 데 사용됩니다.</li></ul> |

**예**

다음 쿼리는 &quot;es&quot; 패턴을 포함하는 프로필이 살고 있는 모든 도시를 검색합니다.

```sql
{%= like(profile.homeAddress.city, "%es%")%}
```

## 소문자{#lower}

`lowerCase` 함수는 문자열을 소문자로 변환합니다.

**구문**

```sql
{%= lowerCase(string) %}
```

**예**

이 함수는 프로필 이름을 소문자로 변환합니다.

```sql
{%= lowerCase(profile.person.name.firstName) %}
```

## 일치{#matches}

`matches` 함수는 문자열이 특정 정규 표현식과 일치하는지 확인하는 데 사용합니다. 정규식의 일치 패턴에 대한 자세한 내용은 [이 문서](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html)를 참조하십시오.

**구문**

```sql
{%= matches(STRING_1, STRING_2) %}
```

**예**

다음 쿼리는 대소문자 구분 없이 개인의 이름이 &quot;John&quot;으로 시작하는지 여부를 결정합니다.

```sql
{%= matches(person.name.,"(?i)^John") %}
```

## 마스크 {#mask}

`Mask` 함수는 문자열의 일부를 &quot;X&quot; 문자로 바꾸는 데 사용합니다.

**구문**

```sql
{%= mask(string,integer,integer) %}
```

**예**

다음 쿼리는 &quot;123456789&quot; 문자열을 처음 2자와 마지막 2자를 제외한 &quot;X&quot; 문자로 바꿉니다.

```sql
{%= mask("123456789",1,2) %}
```

쿼리가 `1XXXXXX89`을(를) 반환합니다.

## MD5 {#md5}

`md5` 함수는 문자열의 md5 해시를 계산하고 반환하는 데 사용됩니다.

**구문**

```sql
{%= md5(string) %}: string
```

**예**

```sql
{%= md5("hello world") %}
```

&quot;5eb63bbbe01eeed093cb22bb8f5acdc3&quot; 반환

## 다음과 같지 않음{#notEqualTo}

`notEqualTo` 함수는 문자열이 지정된 문자열과 같지 않은지 확인하는 데 사용합니다.

**구문**

```sql
{%= notEqualTo(STRING_1, STRING_2) %}
```

| 인수 | 설명 |
| --------- | ----------- |
| `{STRING_1}` | 확인을 수행하는 문자열입니다. |
| `{STRING_2}` | 첫 번째 문자열과 비교할 문자열입니다. |

**예**

다음 쿼리는 대소문자 구분을 통해 개인의 이름이 &quot;John&quot;이 아님을 확인합니다.

```sql
{%= notEqualTo(profile.person.name,"John") %}
```

## 대/소문자 무시와 같지 않음 {#not-equal-with-ignore-case}

`notEqualWithIgnoreCase` 함수는 대/소문자를 무시하는 두 문자열을 비교하는 데 사용됩니다.

**구문**

```sql
{= notEqualWithIgnoreCase(STRING_1,STRING_2) %}: boolean
```

| 인수 | 설명 |
| --------- | ----------- |
| `{STRING_1}` | 확인을 수행하는 문자열입니다. |
| `{STRING_2}` | 첫 번째 문자열과 비교할 문자열입니다. |

**예**

다음 쿼리는 대소문자 구분 없이 개인의 이름이 &quot;john&quot;이 아닌지 확인합니다.

```sql
{%= notEqualTo(profile.person.name,"john") %}
```

## 정규 표현식 그룹{#regexGroup}

`Group` 함수는 제공된 정규 표현식을 기반으로 특정 정보를 추출하는 데 사용됩니다.

**구문**

```sql
{%= regexGroup(STRING, EXPRESSION, GROUP) %}
```

| 인수 | 설명 |
| --------- | ----------- |
| `{STRING}` | 확인을 수행하는 문자열입니다. |
| `{EXPRESSION}` | 첫 번째 문자열과 일치하는 정규 표현식. |
| `{GROUP}` | 일치시킬 표현식 그룹. |

**예**

다음 쿼리는 이메일 주소에서 도메인 이름을 추출하는 데 사용됩니다.

```sql
{%= regexGroup(emailAddress,"@(\\w+)", 1) %}
```

## 바꾸기 {#replace}

`replace` 함수는 문자열에서 지정된 하위 문자열을 다른 하위 문자열로 바꾸는 데 사용합니다.

**구문**

```sql
{%= replace(STRING_1,STRING_2,STRING_3) %}:string
```

| 인수 | 설명 |
| --------- | ----------- |
| `{STRING_1}` | 하위 문자열을 대체해야 하는 문자열입니다. |
| `{STRING_2}` | 대체할 하위 문자열. |
| `{STRING_3}` | 대체 하위 문자열. |

**예**

```sql
{%= replace("Hello John, here is your monthly newsletter!","John","Mark") %}
```

&quot;안녕하세요, 마크 님, 월간 뉴스레터입니다!&quot; 반환

## 모두 바꾸기{#replaceAll}

`replaceAll` 함수는 &quot;regex&quot; 식과 일치하는 텍스트의 모든 하위 문자열을 지정된 리터럴 &quot;replacement&quot; 문자열로 바꾸는 데 사용됩니다. Regex에는 &quot;\&quot; 및 &quot;+&quot;를 특별히 처리하는 기능이 있으며 모든 regex 표현식은 PQL 이스케이프 전략을 따릅니다. 교체는 문자열 시작부터 끝까지 진행됩니다. 예를 들어, 문자열 &quot;aaa&quot;에서 &quot;aa&quot;를 &quot;b&quot;로 바꾸면 &quot;ab&quot;가 아닌 &quot;ba&quot;가 생성됩니다.

**구문**

```sql
{%= replaceAll(string,string,string) %}
```

>[!NOTE]
>
> 두 번째 인수로 사용된 식이 특수 정규 표현식 문자인 경우 이중 백슬래시(`//`)를 사용합니다.  특수 정규 표현식 문자는 [., +, *, ?, ^, $, (, ), [,], {, }, |, \.]
> 
> 자세한 내용은 [Oracle 설명서](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html){_blank}를 참조하세요.
>

## 오른쪽 트림 {#rightTrim}

`rightTrim` 함수를 사용하면 문자열 끝에서 공백이 제거됩니다.

**구문**

```sql
{%= rightTrim(string) %}
```

## 분할 {#split}

`split` 함수는 특정 문자로 문자열을 분할하는 데 사용합니다.

**구문**

```sql
{%= split(string,string) %}
```

## 다음으로 시작{#startsWith}

`startsWith` 함수는 문자열이 지정된 하위 문자열로 시작하는지 확인하는 데 사용합니다.

**구문**

```sql
{%= startsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| 인수 | 설명 |
| --------- | ----------- |
| `{STRING_1}` | 확인을 수행하는 문자열입니다. |
| `{STRING_2}` | 첫 번째 문자열에서 검색할 문자열입니다. |
| `{CASE_SENSITIVE}` | 검사가 대/소문자를 구분하는지 여부를 결정하는 선택적 매개 변수입니다. 기본적으로 true로 설정됩니다. |

**예**

다음 쿼리는 대/소문자 구분을 통해 개인의 이름이 &quot;Joe&quot;로 시작하는지 여부를 결정합니다.

```sql
{%= startsWith(person.name,"Joe") %}
```

## 문자열을 날짜로 변환 {#string-to-date}

`stringToDate` 함수는 문자열 값을 날짜-시간 값으로 변환합니다. 이 메서드에는 날짜-시간의 문자열 표현과 포맷터의 문자열 표현이라는 두 가지 인수가 사용됩니다.

**구문**

```sql
{= stringToDate("date-time value","formatter" %}
```

**예**

```sql
{= stringToDate("2023-01-10 23:13:26", "yyyy-MM-dd HH:mm:ss") %}
```

## 문자열을 정수로 변환 {#string-to-integer}

`string_to_integer` 함수는 문자열 값을 정수 값으로 변환하는 데 사용합니다.

**구문**

```sql
{= string_to_integer(string) %}: int
```

## 문자열을 숫자로 변환 {#string-to-number}

`stringToNumber` 함수는 문자열을 숫자로 변환하는 데 사용합니다. 잘못된 입력에 대한 출력과 동일한 문자열을 반환합니다.

**구문**

```sql
{%= stringToNumber(string) %}: double
```

## 하위 문자열 {#sub-string}

`Count string` 함수는 시작 인덱스와 끝 인덱스 사이에 문자열 식의 하위 문자열을 반환하는 데 사용됩니다.
**구문**

```sql
{= substr(string, integer, integer) %}: string
```

## 제목 대/소문자{#titleCase}

**titleCase** 함수는 문자열의 각 단어의 첫 글자를 대문자로 사용하는 데 사용됩니다.

**구문**

```sql
{%= titleCase(string) %}
```

**예**

만약 그 사람이 워싱턴 하이 스트릿에 산다면, 이 기능은 워싱턴 하이 스트릿에 돌아올 것이다.

```sql
{%= titleCase(profile.person.location.Street) %}
```

## 부울로 변환 {#to-bool}

`toBool` 함수는 인수 유형에 따라 인수 값을 부울 값으로 변환하는 데 사용합니다.

**구문**

```sql
{= toBool(string) %}: boolean
```

## 날짜로 변환 {#to-date-time}

`toDateTime` 함수는 문자열을 날짜로 변환하는 데 사용합니다. 잘못된 입력에 대한 출력으로 에포크 날짜를 반환합니다.

**구문**

```sql
{%= toDateTime(string, string) %}: date-time
```

## 날짜/시간로만 변환 {#to-date-time-only}

`toDateTimeOnly` 함수는 인수 값을 날짜/시간 전용 값으로 변환하는 데 사용합니다. 잘못된 입력에 대한 출력으로 에포크 날짜를 반환합니다. 이 함수는 문자열, 날짜, long 및 int 필드 유형을 수락합니다.

**구문**

```sql
{%= toDateTimeOnly(string/date/long/int) %}: date-time
```

## 트리밍 {#trim}

**trim** 함수는 문자열의 시작과 끝에서 모든 공백을 제거합니다.

**구문**

```sql
{%= trim(string) %}
```

## 대문자{#upper}

**upperCase** 함수는 문자열을 대문자로 변환합니다.

**구문**

```sql
{%= upperCase(string) %}
```

**예**

이 함수는 프로필 성을 대문자로 변환합니다.

```sql
{%= upperCase(profile.person.name.lastName) %}
```

## URL 디코드 {#url-decode}

`urlDecode` 함수는 URL로 인코딩된 문자열을 디코딩하는 데 사용됩니다.

**구문**

```sql
{%= urlDecode(string) %}: string
```

## URL 인코드 {#url-encode}

`Count only null` 함수는 문자열을 URL 인코딩하는 데 사용됩니다.

**구문**

```sql
{%= urlEncode(string) %}: string
```
