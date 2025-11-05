---
product: journey optimizer
title: 수학 함수
description: 수학 함수에 대해 알아보기
feature: Journeys
role: Developer
level: Experienced
keywords: 수학, 함수, 표현식, 여정, 계산, 숫자
version: Journey Orchestration
source-git-commit: bb47ca4957129a4d05aa3d7286409eef0cb62143
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 7%

---

# 수학 함수 {#math-functions}

수학 함수는 여정 표현식 내에서 수치 계산에 필수적인 수학 연산을 제공합니다. 이러한 함수를 사용하면 데이터에 대해 정확한 숫자 계산 및 변환을 수행할 수 있습니다.

다음과 같은 작업을 수행할 때 수학 함수를 사용합니다.

* 테스트, 샘플링 또는 임의화를 위한 임의 값 생성([random](#random))
* 깔끔한 데이터 표시를 위해 소수점 숫자를 가장 가까운 정수로 반올림합니다([round](#round)).
* 숫자 필드에 수학 계산 수행
* 비즈니스 논리 및 의사 결정에 대한 숫자 값 변환

수학 함수는 십진수 및 정수 유형을 모두 처리하며, 여정 표현식에서 정확한 결과를 보장하기 위해 유형 변환을 자동으로 관리합니다.

## random {#random}

0과 1 사이의 난수를 생성합니다.

+++구문

`random()`

+++

+++서명 및 반환된 유형

`random()`

십진수를 반환합니다.

+++

## round {#round}

인수에 가장 가까운 정수 값을 반환하며, 인수는 양의 무한대로 반올림됩니다.

+++구문

`round(<parameters>)`

+++

+++매개변수

* decimal
* 정수

+++

+++서명 및 반환된 유형

`round(<decimal>)`

`round(<integer>)`

정수를 반환합니다.

+++

+++예

`round(3.14)`

3을 반환합니다.

`round(3.54)`

4를 반환합니다.

`round(-3.14)`

-3을 반환합니다.

`round(3)`

3을 반환합니다.

+++

