---
title: 함수 라이브러리
description: 함수 라이브러리
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '696'
ht-degree: 7%

---

# 문자열 함수 {#string}

![](../../assets/do-not-localize/badge.png)


TBC CJM 문자열 함수

## 좋아요

`like` 함수는 문자열이 지정된 패턴과 일치하는지 확인하는 데 사용됩니다.

**형식**

```sql
like ({STRING_1},{STRING_2})
```

| 인수 | 설명 |
| --------- | ----------- |
| `{STRING_1}` | 검사를 수행할 문자열입니다. |
| `{STRING_2}` | 첫 번째 문자열과 일치시킬 표현식입니다. 표현식을 만드는 데 지원되는 두 가지 특수 문자가 있습니다.`%` 및 `_`. <ul><li>`%` 0개 이상의 문자를 나타내는 데 사용됩니다.</li><li>`_` 은 하나의 문자를 나타내는 데 사용됩니다.</li></ul> |

**예**

다음 쿼리는 &quot;es&quot; 패턴을 포함하는 모든 도시를 검색합니다.

```sql
like (city ,"%es%")
```

## 다음으로 시작

`startsWith` 함수는 문자열이 지정된 하위 문자열로 시작되는지 확인하는 데 사용됩니다.

**형식**

```sql
startsWith({STRING_1},{STRING_2}, {BOOLEAN})
```

| 인수 | 설명 |
| --------- | ----------- |
| `{STRING_1}` | 검사를 수행할 문자열입니다. |
| `{STRING_2}` | 첫 번째 문자열 내에서 검색할 문자열입니다. |
| `{BOOLEAN}` | 검사가 대/소문자를 구분하는지 확인하는 선택적 매개 변수입니다. 기본적으로 이 설정은 true로 설정됩니다. |

**예**

다음 쿼리는 사람의 이름이 &quot;Joe&quot;로 시작하는 경우 대/소문자 구분을 사용하여 결정합니다.

```sql
startsWith(person.name,"Joe")
```

## 다음으로 시작하지 않음

`doesNotStartWith` 함수는 문자열이 지정된 하위 문자열로 시작하지 않는지 여부를 확인하는 데 사용됩니다.

**형식**

```sql
doesNotStartWith({STRING_1},{STRING_2}, {BOOLEAN})
```

| 인수 | 설명 |
| --------- | ----------- |
| `{STRING_1}` | 검사를 수행할 문자열입니다. |
| `{STRING_2}` | 첫 번째 문자열 내에서 검색할 문자열입니다. |
| `{BOOLEAN}` | 검사가 대/소문자를 구분하는지 확인하는 선택적 매개 변수입니다. 기본적으로 이 설정은 true로 설정됩니다. |

**예**

다음 쿼리는 사람의 이름이 &quot;Joe&quot;로 시작하지 않을 경우 대/소문자 구분을 사용하여 결정합니다.

```sql
doesNotStartWith(person.name,"Joe")
```

## 다음으로 끝남

`endsWith` 함수는 문자열이 지정된 하위 문자열로 끝났는지 확인하는 데 사용됩니다.

**형식**

```sql
endsWith({STRING_1},{STRING_2}, {BOOLEAN})
```

| 인수 | 설명 |
| --------- | ----------- |
| `{STRING_1}` | 검사를 수행할 문자열입니다. |
| `{STRING_2}` | 첫 번째 문자열 내에서 검색할 문자열입니다. |
| `{BOOLEAN}` | 검사가 대/소문자를 구분하는지 확인하는 선택적 매개 변수입니다. 기본적으로 이 설정은 true로 설정됩니다. |

**예**

다음 쿼리는 고객의 이메일 주소가 &quot;.com&quot;으로 끝나는 경우 대/소문자 구분을 사용하여 결정합니다.

```sql
endsWith(person.emailAddress,".com")
```

## 다음으로 끝나지 않음

`doesNotEndWith` 함수는 문자열이 지정된 하위 문자열로 끝나지 않는지 확인하는 데 사용됩니다.

**형식**

```sql
doesNotEndWith({STRING_1},{STRING_2}, {BOOLEAN})
```

| 인수 | 설명 |
| --------- | ----------- |
| `{STRING_1}` | 검사를 수행할 문자열입니다. |
| `{STRING_2}` | 첫 번째 문자열 내에서 검색할 문자열입니다. |
| `{BOOLEAN}` | 검사가 대/소문자를 구분하는지 확인하는 선택적 매개 변수입니다. 기본적으로 이 설정은 true로 설정됩니다. |

**예**

다음 쿼리는 고객의 이메일 주소가 &quot;.com&quot;으로 끝나지 않을 경우 대/소문자 구분을 사용하여 결정합니다.

```sql
doesNotEndWith(person.emailAddress,".com")
```

## 다음 포함

`contains` 함수는 문자열에 지정된 하위 문자열이 포함되어 있는지 확인하는 데 사용됩니다.

**형식**

```sql
contains({STRING_1},{STRING_2}, {BOOLEAN})
```

| 인수 | 설명 |
| --------- | ----------- |
| `{STRING_1}` | 검사를 수행할 문자열입니다. |
| `{STRING_2}` | 첫 번째 문자열 내에서 검색할 문자열입니다. |
| `{BOOLEAN}` | 검사가 대/소문자를 구분하는지 확인하는 선택적 매개 변수입니다. 기본적으로 이 설정은 true로 설정됩니다. |

**예**

다음 쿼리는 사람의 이메일 주소에 문자열 &quot;2010@gm&quot;이 포함된 경우 대/소문자 구분을 사용하여 결정합니다.

```sql
contains(person.emailAddress,"2010@gm")
```

## 다음을 포함하지 않음

`doesNotContain` 함수는 문자열에 지정된 하위 문자열이 포함되어 있지 않은지 확인하는 데 사용됩니다.

**형식**

```sql
doesNotContain({STRING_1},{STRING_2}, {BOOLEAN})
```

| 인수 | 설명 |
| --------- | ----------- |
| `{STRING_1}` | 검사를 수행할 문자열입니다. |
| `{STRING_2}` | 첫 번째 문자열 내에서 검색할 문자열입니다. |
| `{BOOLEAN}` | 검사가 대/소문자를 구분하는지 확인하는 선택적 매개 변수입니다. 기본적으로 이 설정은 true로 설정됩니다. |

**예**

다음 쿼리는 사람의 이메일 주소에 문자열 &quot;2010@gm&quot;이 포함되어 있지 않으면 대/소문자 구분 없이 결정합니다.

```sql
doesNotContain(person.emailAddress,"2010@gm")
```

## 다음과 같음

`equals` 함수는 문자열이 지정된 문자열과 동일한지 확인하는 데 사용됩니다.

**형식**

```sql
equals({STRING_1},{STRING_2})
```

| 인수 | 설명 |
| --------- | ----------- |
| `{STRING_1}` | 검사를 수행할 문자열입니다. |
| `{STRING_2}` | 첫 번째 문자열과 비교할 문자열입니다. |

**예**

다음 쿼리는 사람의 이름이 &quot;John&quot;인 경우 대/소문자 구분을 사용하여 결정합니다.

```sql
equals(person.name,"John")
```

## 같지 않음

`notEqualTo` 함수는 문자열이 지정된 문자열과 동일하지 않은지 확인하는 데 사용됩니다.

**형식**

```sql
notEqualTo({STRING_1},{STRING_2})
```

| 인수 | 설명 |
| --------- | ----------- |
| `{STRING_1}` | 검사를 수행할 문자열입니다. |
| `{STRING_2}` | 첫 번째 문자열과 비교할 문자열입니다. |

**예**

다음 쿼리는 사람의 이름이 &quot;John&quot;이 아닌 경우 대/소문자 구분을 사용하여 결정합니다.

```sql
notEqualTo(person.name,"John")
```

## 일치

`matches` 함수는 문자열이 특정 정규 표현식과 일치하는지 확인하는 데 사용됩니다. 정규 표현식의 일치 패턴에 대한 자세한 내용은 [이 문서](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html)를 참조하십시오.

**형식**

```sql
matches({STRING_1},STRING_2})
```

**예**

다음 쿼리는 대소문자를 구분하지 않고 사람의 이름이 &quot;John&quot;으로 시작하는 경우 결정합니다.

```sql
matches(person.name.,"(?i)^John")
```

## 정규 표현식 그룹

`regexGroup` 함수는 제공된 정규 표현식을 기반으로 특정 정보를 추출하는 데 사용됩니다.

**형식**

```sql
regexGroup({STRING},{EXPRESSION})
```

**예**

다음 쿼리는 이메일 주소에서 도메인 이름을 추출하는 데 사용됩니다.

```sql
regexGroup(emailAddress,"@(\w+)", 1)
```
