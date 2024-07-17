---
solution: Journey Optimizer
product: journey optimizer
title: 고급 표현식 편집기 구문
description: 고급 표현식 편집기에 사용되는 구문에 대해 알아봅니다
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: 구문, 편집기, 여정
exl-id: c9434b28-2750-4a53-985e-c4a3f940472c
source-git-commit: 2de94e8ce3fe77399c8dc1d515ae73d58cb8f43d
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 5%

---

# 고급 표현식 편집기 구문 {#syntax}

[고급 표현식 편집기](expressionadvanced.md)를 사용할 때의 구문 기본 사항은 아래에 나와 있습니다. 고급 표현식 편집기의 사용 샘플은 [이 페이지](advanced-editor-use-cases.md)에서 확인할 수 있습니다.

## 괄호 및 표현식 우선 순위 {#parentheses-and-expression-priority}

괄호는 복잡한 표현식을 더 읽기 쉽게 하는 데 사용할 수 있습니다. _(&lt;표현식>)_&#x200B;은(는) _&lt;표현식>_&#x200B;과(와) 동일합니다. 괄호는 또한 평가 순서 및 연관성을 정의하는 데 사용될 수 있다.

표현식은 왼쪽에서 오른쪽으로 평가됩니다. 산술 연산자에 대한 연관성을 적용해야 합니다. 곱과 나눗셈은 덧셈과 뺄셈보다 우선합니다. 특정한 명령을 부과하기 위해서는 반드시 괄호를 추가하여 작업을 구분해야 한다. 예:

<!--```5 + 2 * 10 = 25, and (5 + 2) * 10 = 70```-->

| 표현식 | 평가 |
|--- |--- |
| `4 + 2 * 10` | <ul><li>&#39;*&#39;가 &#39;+&#39;보다 우선함: 2 * 10은 20→ 평가됨</li><li>4 + 20 → 24</li></ul> |
| `(4 + 2) * 10` | <ul><li>괄호는 우선 순위를 변경합니다. (4 + 2)는 6→ 평가됩니다.</li><li> 6 * 10 → 60</li></ul> |

## 대/소문자 구분 {#case-sensitivity}

다른 대소문자 구분 규칙은 다음과 같습니다.

* 모든 연산자(및, 또는 등) 소문자로 작성해야 합니다. 예를 들어 _`<expression1>`및`<expression2>`_&#x200B;은(는) 올바른 식이지만 _`<expression1>`및`<expression2>`_ 식은 올바른 식이 아닙니다.
* 모든 함수 이름은 대소문자를 구분합니다. 예를 들어 _inAudience()_&#x200B;은(는) 유효하지만 _INAUDIENCE()_ 함수는 유효하지 않습니다.
* 필드 참조 및 상수 값은 대소문자를 구분합니다. 연산자 및 함수와 달리 언어의 기본 제공 요소가 아니며, 최종 사용자가 작성합니다.

## 반환된 표현식 유형 {#returned-expression-type}

사용 컨텍스트에 따라 표현식 편집기에서 다른 값을 반환할 수 있습니다.

| 고급 표현식 편집기 사용 | 반환된 표현식 유형이 필요합니다. |
|--- |--- |
| 조건(데이터 소스 조건, 날짜 조건) | 부울 |
| 사용자 지정 타이머 | dateTimeOnly |
| 작업 매개 변수 매핑 | 모두 |
