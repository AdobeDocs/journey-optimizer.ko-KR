---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: 표현식 편집기에서 지원되는 함수
description: 의사 결정 관리(Offer Decisioning)에서 지원되는 개인화 편집기 기능을 알아봅니다.
badge: label="레거시" type="Informative"
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
version: Journey Orchestration
exl-id: c4df41a2-d740-437c-acc3-957508c4a1c0
source-git-commit: b90e3af955496d4fcae54b109cb1e86a8a21be43
workflow-type: tm+mt
source-wordcount: '619'
ht-degree: 16%

---

# 표현식 편집기에서 지원되는 함수 {#personalization-editor-supported-functions}

의사 결정 관리에서 개인화 편집기를 사용하여 표현식을 작성합니다. 특히 다음과 같은 경우에 이 편집기를 사용합니다.

* **오퍼 콘텐츠 정의** - [표현을 추가](offer-library/add-representations.md)하고 오퍼 콘텐츠(이미지, 텍스트, 링크)를 개인화할 때
* **의사 결정 규칙 만들기** - 오퍼에 대해 [자격 정의](offer-library/creating-decision-rules.md)할 때
* **등급 수식 작성** - 오퍼를 정렬하기 위해 [등급 수식 만들기](ranking/create-ranking-formulas.md)

Offer Decisioning 백엔드는 개인화 편집기에서 사용할 수 있는 함수 중 **하위 집합**&#x200B;만 지원합니다. 이 페이지에는 안전하게 사용할 수 있는 모든 기능이 나열됩니다. 각 섹션을 확장하여 지원되는 연산자, 도우미 및 함수를 봅니다.

## 지원되는 함수 목록 {#supported-functions-list}

+++ 연산자

* 산술: `+` `-` `*` `/` `%`
* 논리: `and` `or` `!`
* 비교: `=` `!=` `>` `>=` `<` `<=`

+++

+++ 도우미

* 각
* 포함
* 조건
* Unless
* Let
* 기본 대체 값
* 조각
* datasetLookup
* externalDataLookup(Alpha)
* 인라인
* Url
* 실행 메타데이터
* valueAtPath

+++

+++ 문자열 함수

| 표시 이름 | 내부 이름 |
|--------------|---------------|
| 소문자 | 소문자 |
| 대문자 | upperCase |
| 카멜 대/소문자 | 카멜 대/소문자 |
| 제목 대/소문자 | titleCase |
| 트리밍 | trim |
| Left Trim | leftTrim |
| 오른쪽 트림 | rightTrim |
| 비어 있음 | isEmpty |
| 같음 대/소문자 무시 | equalsIgnoreCase |
| 대/소문자 무시와 같지 않음 | notEqualWithIgnoreCase |
| 바꾸기 | replace |
| 모두 바꾸기 | replaceAll |
| Concat | concat |
| 분할 | split |
| Encode64 | encode64 |
| Length | length |
| MD5 | md5 |
| SHA256 | sha256 |
| 다음과 유사 | 비슷함 |
| 다음으로 시작 | startsWith |
| 다음으로 시작하지 않음 | doesNotStartWith |
| 다음으로 끝남 | endsWith |
| 다음으로 끝나지 않음 | doesNotEndWith |
| 다음을 포함 | 다음 포함 |
| 다음을 포함하지 않음 | doesNotContain |
| 다음과 같음 | 다음과 같음 |
| 다음과 같지 않음 | notEqualTo |
| 일치 | matches |
| 정규 표현식 그룹 | regexGroup |
| 문자열을 숫자로 변환 | stringTonumber |
| 문자열을 현재까지 | stringToDate |
| 종료 날짜/시간 | toDateTime |
| 종료 날짜/시간만 | toDateTimeOnly |
| 이메일 도메인 추출 | extractEmailDomain |
| 이메일 사용자 이름 추출 | extractEmailUsername |
| 비어 있지 않음 | isNotEmpty |
| 색인 | indexOf |
| 마지막 색인 | lastIndexOf |
| 하위 문자열 | substr |
| 부울로 | toBool |
| 문자열을 정수로 변환 | string_to_integer |
| 마스크 | 마스크 |
| 형식 통화 가져오기 | formatCurrency |
| 문자의 유니코드 값 가져오기 | charCodeAt |
| 모든 텍스트에 대한 Qr 코드 가져오기 | qrCode |

+++

+++ 배열, 목록 및 집합 함수

| 표시 이름 | 내부 이름 |
|--------------|---------------|
| 고유 | distinct |
| 위치 | in |
| 다음에 없음 | notIn |
| 교차 | 교차 |
| 하위 집합 | 부분 집합 |
| 상위 집합 | 위 집합 |
| 포함 | 포함 |
| 정렬하고 배열에서 첫 번째 N을 가져옵니다. | topN |
| 배열에서 마지막 N 정렬 및 가져오기 | bottomN |
| 첫 번째 항목 | head |
| Count | count |
| Sum | sum |
| 평균 | 평균 |
| 최소 | min |
| 최대 | max |

+++

+++ 맵 함수

| 표시 이름 | 내부 이름 |
|--------------|---------------|
| Get | get |
| 키 | 키 |
| 값 | 값 |

+++

+++ 개체 함수

| 표시 이름 | 내부 이름 |
|--------------|---------------|
| null임 | isNull |
| null이 아님 | isNotNull |

+++

+++ 수학 함수

| 표시 이름 | 내부 이름 |
|--------------|---------------|
| 백분율로 변환 | toPercent |
| 올림 | roundUp |
| 내림 | 내림 |
| 전체 자릿수로 | toPrecision |
| 절대 | 절대 |
| 무작위 | random |
| 16진수로 변환 | toHexString |
| 로케일로 번호 가져오기 | formatNumber |
| 대상 문자열 | toString |
| 끝 정수 | toInt |
| 길게 | toLong |

+++

+++ 날짜 시간 함수

| 표시 이름 | 내부 이름 |
|--------------|---------------|
| 지금 | now |
| CurrentZonedDateTime 가져오기 | getCurrentZonedDateTime |
| 종료 날짜 | toDate |
| 종료 시간 | toTime |
| 종료 날짜/시간 | toDateTime |
| 종료 날짜/시간만 | toDateTimeOnly |
| 종료 날짜만 | toDateOnly |
| 종료 시간만 | toTimeOnly |
| 종료 시간대 | 시간대 지정 |
| 날짜 형식 지정 | formatDate |
| 날짜 시간 형식 지정 | formatDateTime |
| 시간 포맷 | formatTime |
| 구문 분석 날짜 | parseDate |
| 날짜 시간 구문 분석 | parseDateTime |
| 구문 분석 시간 | parseTime |
| 일 추가 | addDays |
| 월 추가 | addMonth |
| 연도 추가 | addYears |
| 시간 추가 | addHours |
| 분 추가 | addMinutes |
| 초 추가 | addSeconds |
| 일 빼기 | subtractDays |
| 월 빼기 | 빼기 |
| 연도 빼기 | subtractYars |
| 시간 빼기 | 빼기 |
| 분 빼기 | 빼기 시간(분) |
| 초 빼기 | subtractSeconds |
| 일 차이 | diffDays |
| 월 차이 | diffMonths |
| 연도 차이 | diffYears |
| 시간 차이 | diffHours |
| 시간 차이(분) | diffMinutes |
| 차이(초) | diffSeconds |
| 하루의 시작 | startOfDay |
| 하루의 끝 | endOfDay |
| 다음 이전임 | isAfter |
| 다음 이후임 | isAfter |

+++

+++ URL 함수

| 표시 이름 | 내부 이름 |
|--------------|---------------|
| URL 인코딩 | encodeUrl |
| URL 디코딩 | decodeUrl |
| URL 쿼리 매개 변수 가져오기 | getUrlQueryParam |
| URL 프로토콜 가져오기 | getUrlProtocol |
| URL 호스트 가져오기 | getUrlHost |

+++

>[!NOTE]
>
>위의 목록에 없는 함수를 사용하는 경우 런타임에 식이 실패하거나 예기치 않은 결과가 발생할 수 있습니다. [!DNL Journey Optimizer] 개인화에서 사용할 수 있는 전체 함수 집합을 보려면 [도우미 함수 목록](../personalization/functions/functions.md)을 참조하세요. Offer Decisioning에서는 이 페이지에 설명된 하위 집합만 지원됩니다.
