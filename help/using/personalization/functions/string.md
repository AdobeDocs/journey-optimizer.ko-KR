---
title: 문자열 함수 라이브러리
description: 문자열 함수 라이브러리
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 8674ef9e-261b-49d9-800e-367f9f7ef979
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '1199'
ht-degree: 7%

---

# 문자열 함수 {#string}

표현식 편집기에서 문자열 함수를 사용하는 방법을 알아봅니다.

## 카멜 사례 {#camelCase}

다음 `camelCase` 함수는 문자열의 각 단어의 첫 문자를 대문자로 바꿉니다.

**포맷**

```sql
{%= camelCase(string)%}
```

**예**

다음 함수는 프로필의 거리 주소에 첫 번째 단어 문자를 대문자로 사용합니다.

```sql
{%= camelCase(profile.homeAddress.street) %}
```

## Concat {#concate}

다음 `concat` 함수는 두 문자열을 하나로 결합합니다.

**포맷**

```sql
{%= concat(string,string) %}
```

**예**

다음 함수는 프로필 도시와 국가를 하나의 문자열로 결합합니다.

```sql
{%= concat(profile.homeAddress.city,profile.homeAddress.country) %}
```

## 다음 포함 {#contains}

다음 `contains` 함수에서 지정된 하위 문자열을 포함하는지 여부를 확인하는 데 사용됩니다.

**포맷**

```sql
{%= contains(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| 인수 | 설명 |
| --------- | ----------- |
| `STRING_1` | 확인을 수행할 문자열입니다. |
| `STRING_2` | 첫 번째 문자열 내에서 검색할 문자열입니다. |
| `CASE_SENSITIVE` | 검사가 대/소문자를 구분하는지 여부를 판별하는 선택적 매개 변수입니다. 가능한 값: true(기본값) / false. |

**예**

* 다음 함수는 프로필 이름에 문자 A(위 또는 아래)가 포함되어 있는지 확인합니다. 이 경우 &#39;true&#39;를 반환하고, 그렇지 않으면 &#39;false&#39;를 반환합니다.

   ```sql
   {%= contains(profile.person.name.firstName, "A", false) %}
   ```

* 다음 쿼리는 대/소문자 구분을 사용하여 개인의 이메일 주소에 문자열 &quot;2010@gm&quot;이 포함된 경우 결정합니다.

   ```sql
   {%= contains(profile.person.emailAddress,"2010@gm") %}
   ```

## 다음을 포함하지 않음{#doesNotContain}

다음 `doesNotContain` 함수에서 지정된 하위 문자열을 포함하지 않는지 확인하는 데 사용됩니다.

**포맷**

```sql
{%= doesNotContain(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| 인수 | 설명 |
| --------- | ----------- |
| `STRING_1` | 확인을 수행할 문자열입니다. |
| `STRING_2` | 첫 번째 문자열 내에서 검색할 문자열입니다. |
| `CASE_SENSITIVE` | 검사가 대/소문자를 구분하는지 여부를 판별하는 선택적 매개 변수입니다. 가능한 값: true(기본값) / false. |

**예**

다음 쿼리는 대/소문자 구분을 사용하여 개인의 이메일 주소에 문자열 &quot;2010@gm&quot;이 포함되지 않은 경우 결정합니다.

```sql
{%= doesNotContain(profile.person.emailAddress,"2010@gm")%}
```


## 다음으로 끝나지 않음{#doesNotEndWith}

다음 `doesNotEndWith` 함수는 문자열이 지정된 하위 문자열로 끝나지 않는지 여부를 확인하는 데 사용됩니다.

**포맷**

```sql
{%= doesNotEndWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| 인수 | 설명 |
| --------- | ----------- |
| `{STRING_1}` | 확인을 수행할 문자열입니다. |
| `{STRING_2}` | 첫 번째 문자열 내에서 검색할 문자열입니다. |
| `{CASE_SENSITIVE}` | 검사가 대/소문자를 구분하는지 여부를 판별하는 선택적 매개 변수입니다. 가능한 값: true(기본값) / false. |

**예**

다음 쿼리는 대/소문자 구분을 사용하여 개인의 이메일 주소가 &quot;.com&quot;으로 끝나지 않으면 결정합니다.

```sql
doesNotEndWith(person.emailAddress,".com")
```

## 다음으로 시작하지 않음{#doesNotStartWith}

다음 `doesNotStartWith` 함수는 문자열이 지정된 하위 문자열로 시작하지 않는지 여부를 확인하는 데 사용됩니다.

**포맷**

```sql
{%= doesNotStartWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| 인수 | 설명 |
| --------- | ----------- |
| `{STRING_1}` | 확인을 수행할 문자열입니다. |
| `{STRING_2}` | 첫 번째 문자열 내에서 검색할 문자열입니다. |
| `{CASE_SENSITIVE}` | 검사가 대/소문자를 구분하는지 여부를 판별하는 선택적 매개 변수입니다. 가능한 값: true(기본값) / false. |

**예**

다음 쿼리는 대/소문자 구분을 사용하여 개인 이름이 &quot;Joe&quot;로 시작하지 않으면 결정합니다.

```sql
{%= doesNotStartWith(person.name,"Joe")%}
```

## 64 인코딩{#encode64}

다음 `encode64` URL에 예를 들어 포함해야 하는 경우 PI(개인 정보)를 유지하기 위한 문자열을 인코딩하는 데 사용됩니다.

**포맷**

```sql
{%= encode64(string) %}
```

## 다음으로 끝남{#endsWith}

다음 `endsWith` 함수는 문자열이 지정된 하위 문자열로 끝났는지 여부를 확인하는 데 사용됩니다.

**포맷**

```sql
{%= endsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| 인수 | 설명 |
| --------- | ----------- |
| `{STRING_1}` | 확인을 수행할 문자열입니다. |
| `{STRING_2}` | 첫 번째 문자열 내에서 검색할 문자열입니다. |
| `{CASE_SENSITIVE}` | 검사가 대/소문자를 구분하는지 여부를 판별하는 선택적 매개 변수입니다. 가능한 값: true(기본값) / false. |

**예**

다음 쿼리는 대/소문자 구분을 사용하여 개인의 이메일 주소가 &quot;.com&quot;으로 끝나는 경우 결정합니다.

```sql
{%= endsWith(person.emailAddress,".com") %}
```


## 다음과 같음{#equals}

다음 `equals` 함수는 문자열을 대소문자 구분을 사용하여 지정된 문자열과 일치하는지 확인하는 데 사용됩니다.

**포맷**

```sql
{%= equals(STRING_1, STRING_2) %}
```

| 인수 | 설명 |
| --------- | ----------- |
| `{STRING_1}` | 확인을 수행할 문자열입니다. |
| `{STRING_2}` | 첫 번째 문자열과 비교할 문자열입니다. |

**예**

다음 쿼리는 대/소문자 구분을 사용하여 개인의 이름이 &quot;John&quot;인 경우 결정합니다.

```sql
{%=equals(profile.person.name,"John") %}
```

## 대/소문자 무시 같음{#equalsIgnoreCase}

다음 `equalsIgnoreCase` 변수는 대/소문자를 구분하지 않고 지정된 문자열과 동일한지 확인하는 데 사용됩니다.

**포맷**

```sql
{%= equalsIgnoreCase(STRING_1, STRING_2) %}
```

| 인수 | 설명 |
| --------- | ----------- |
| `{STRING_1}` | 확인을 수행할 문자열입니다. |
| `{STRING_2}` | 첫 번째 문자열과 비교할 문자열입니다. |

**예**

다음 쿼리는 대/소문자를 구분하지 않고 개인의 이름이 &quot;John&quot;인 경우 결정합니다.

```sql
{%= equalsIgnoreCase(profile.person.name,"John") %}
```

## 이메일 도메인 추출 {#extractEmailDomain}

다음 `extractEmailDomain` 함수는 이메일 주소의 도메인을 추출하는 데 사용됩니다.

**포맷**

```sql
{%= extractEmailDomain(string) %}
```

**예**

다음 쿼리는 개인 이메일 주소의 이메일 도메인을 추출합니다.

```sql
{%= extractEmailDomain(profile.personalEmail.address) %}
```

## 비어 있음 {#isEmpty}

다음 `isEmpty` 함수는 문자열이 비어 있는지 확인하는 데 사용됩니다.

**포맷**

```sql
{%= isEmpty(string) %}
```

**예**

프로필의 휴대폰 번호가 비어 있는 경우 다음 함수는 &#39;true&#39;를 반환합니다. 그렇지 않으면 &#39;false&#39;를 반환합니다.

```sql
{%= isEmpty(profile.mobilePhone.number) %}
```

## 왼쪽 트림 {#leftTrim}

다음 `leftTrim` 함수는 문자열 시작 부분에서 공백을 제거하는 데 사용됩니다.

**포맷**

```sql
{%= leftTrim(string) %}
```

## Length {#length}

다음 `length` 함수는 문자열 또는 표현식의 문자 수를 가져오는 데 사용됩니다.

**포맷**

```sql
{%= length(string) %}
```

**예**

다음 함수는 프로필의 도시 이름의 길이를 반환합니다.

```sql
{%= length(profile.homeAddress.city) %}
```

## 좋아요{#like}

다음 `like` 함수는 문자열이 지정된 패턴과 일치하는지 확인하는 데 사용됩니다.

**포맷**

```sql
{%= like(STRING_1, STRING_2) %}
```

| 인수 | 설명 |
| --------- | ----------- |
| `{STRING_1}` | 확인을 수행할 문자열입니다. |
| `{STRING_2}` | 첫 번째 문자열에 대해 일치하는 표현식입니다. 표현식을 만드는 데 지원되는 두 가지 특수 문자가 있습니다. `%` 및 `_`. <ul><li>`%` 0개 이상의 문자를 나타내는 데 사용됩니다.</li><li>`_` 는 정확히 하나의 문자를 나타내는 데 사용됩니다.</li></ul> |

**예**

다음 쿼리는 프로필이 거주하는 모든 도시를 검색하여 &quot;es&quot; 패턴을 검색합니다.

```sql
{%= like(profile.homeAddress.city, "%es%")%}
```

## 소문자{#lower}

다음 `lowerCase` 함수는 문자열을 소문자로 변환합니다.

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

다음 `matches` 함수가 특정 정규 표현식과 일치하는지 여부를 확인하는 데 사용됩니다. 자세한 내용은 [이 문서](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html) 를 참조하십시오.

**포맷**

```sql
{%= matches(STRING_1, STRING_2) %}
```

**예**

다음 쿼리는 대/소문자를 구분하지 않고 개인 이름이 &quot;John&quot;으로 시작하는 경우를 결정합니다.

```sql
{%= matches(person.name.,"(?i)^John") %}
```

## 같지 않음{#notEqualTo}

다음 `notEqualTo` 함수는 문자열이 지정된 문자열과 같지 않은지 확인하는 데 사용됩니다.

**포맷**

```sql
{%= notEqualTo(STRING_1, STRING_2) %}
```

| 인수 | 설명 |
| --------- | ----------- |
| `{STRING_1}` | 확인을 수행할 문자열입니다. |
| `{STRING_2}` | 첫 번째 문자열과 비교할 문자열입니다. |

**예**

다음 쿼리는 대/소문자 구분을 사용하여 개인의 이름이 &quot;John&quot;이 아닌 경우 결정합니다.

```sql
{%= notEqualTo(profile.person.name,"John") %}
```

## 정규 표현식 그룹{#regexGroup}

다음 `Group` 함수는 제공된 정규 표현식을 기반으로 특정 정보를 추출하는 데 사용됩니다.

**포맷**

```sql
{%= regexGroup(STRING, EXPRESSION, GROUP) %}
```

| 인수 | 설명 |
| --------- | ----------- |
| `{STRING}` | 확인을 수행할 문자열입니다. |
| `{EXPRESSION}` | 첫 번째 문자열에 일치하는 정규 표현식입니다. |
| `{GROUP}` | 일치하는 표현식 그룹입니다. |

**예**

다음 쿼리는 이메일 주소에서 도메인 이름을 추출하는 데 사용됩니다.

```sql
{%= regexGroup(emailAddress,"@(\w+)", 1) %}
```

## 바꾸기 {#replace}

다음 `replace` 함수는 문자열에서 주어진 하위 문자열을 다른 하위 문자열로 바꾸는 데 사용됩니다.

**포맷**

```sql
{%= replace(string,string,string) %}
```

**예**

다음 함수 .

```sql

```


## 모두 바꾸기{#replaceAll}

다음 `replaceAll` 함수는 &quot;target&quot;과 일치하는 텍스트의 모든 하위 문자열을 지정된 리터럴 &quot;replacement&quot; 문자열로 바꾸는 데 사용됩니다. 대체는 문자열 시작 부분부터 끝 부분까지 진행됩니다. 예를 들어 문자열 &quot;aaa&quot;에서 &quot;aa&quot;를 &quot;b&quot;로 바꾸면 &quot;ab&quot;가 아니라 &quot;ba&quot;가 됩니다.

**포맷**

```sql
{%= replaceAll(string,string,string) %}
```


## 오른쪽 트림 {#rightTrim}

다음 `rightTrim` 함수는 문자열 끝에서 공백을 제거합니다.


**포맷**

```sql
{%= rightTrim(string) %}
```

## 분할 {#split}

다음 `split` 함수는 문자열을 지정된 문자로 분할하는 데 사용됩니다.

**포맷**

```sql
{%= split(string,string) %}
```

<!--
**Example**

The following function .

```sql

```

-->

## 다음으로 시작{#startsWith}

다음 `startsWith` 함수는 문자열이 지정된 하위 문자열로 시작하는지 여부를 확인하는 데 사용됩니다.

**포맷**

```sql
{%= startsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| 인수 | 설명 |
| --------- | ----------- |
| `{STRING_1}` | 확인을 수행할 문자열입니다. |
| `{STRING_2}` | 첫 번째 문자열 내에서 검색할 문자열입니다. |
| `{CASE_SENSITIVE}` | 검사가 대/소문자를 구분하는지 여부를 판별하는 선택적 매개 변수입니다. 기본적으로 true로 설정됩니다. |

**예**

다음 쿼리는 대/소문자 구분을 사용하여 개인 이름이 &quot;Joe&quot;로 시작하는 경우 결정합니다.

```sql
{%= startsWith(person.name,"Joe") %}
```

## 제목 사례{#titleCase}

다음 **titleCase** 함수는 문자열의 각 단어의 첫 문자를 대문자로 바꾸는 데 사용됩니다.

**구문**

```sql
{%= titleCase(string) %}
```

**예**

만약 그 사람이 워싱턴 하이 스트리트에 살면, 이 기능은 워싱턴 하이스트리트로 돌아갈 것이다.

```sql
{%= titleCase(profile.person.location.Street) %}
```

## Trim{#trim}

다음 **trim** 함수는 문자열 시작 및 끝에서 모든 공백을 제거합니다.

**구문**

```sql
{%= trim(string) %}
```

## 대문자{#upper}

다음 **upperCase** 함수는 문자열을 대문자로 변환합니다.

**구문**

```sql
{%= upperCase(string) %}
```

**예**

이 함수는 프로필 성을 대/소문자를 구분합니다.

```sql
{%= upperCase(profile.person.name.lastName) %}
```
