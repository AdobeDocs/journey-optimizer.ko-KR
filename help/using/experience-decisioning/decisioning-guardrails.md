---
title: 의사 결정 가드레일 및 제한 사항
description: Decisioning 보호 및 제한 사항에 대해 자세히 알아봅니다.
feature: Decisioning
role: User
level: Intermediate
exl-id: 73548973-ff8d-4d6c-b383-dd3679fa159a
source-git-commit: 58f4fdf8ec3cdb609efebf5b8713f6b770ef5414
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 18%

---

# 의사 결정 가드레일 및 제한 사항 {#decisioning-guardrails}

Decisioning을 최적으로 사용하려면 다음 보호 기능 및 제한 사항을 염두에 두십시오.

[!DNL Journey Optimizer] 보호 및 제한 사항의 전체 목록을 [이 섹션](../start/guardrails.md)에서 사용할 수 있습니다.

## 결정 요청 {#decision-requests}

| 가드레일 | 제한 |
| ------- | ------- |
| Edge 세그먼테이션을 사용한 의사 결정 정책이 있는 코드 기반 경험 API 요청 | 1500 |
| Edge 세그멘테이션을 사용하지 않는 의사 결정 정책이 있는 코드 기반 경험 API 요청 | 5000 |

## 항목 컬렉션 {#item-collections}

| 가드레일 | 제한 |
| ------- | ------- |
| 항목 컬렉션 | 10K |
| 항목 컬렉션당 총 오퍼 항목 | 500 |

## 결정 정책 {#decision-policy}

| 가드레일 | 제한 |
| ------- | ------- |
| 의사 결정 정책당 선택 전략 및 수동 항목 수 | 10 |
| 결정 정책당 반환되는 최대 오퍼 항목 수 | 30 |

## 자격 규칙 {#eligibility-rules}

| 가드레일 | 제한 |
| ------- | ------- |
| 총 의사 결정 규칙 및 등급 공식 | 10K 결합 |
| 규칙당 최대 프로필 속성 수 | 25 |
| 규칙당 최대 컨텍스트 데이터 속성 수 | 30 |
| 최대 pql 규칙 크기 | 15K(UTF-8) |
| 최대 중첩 수준 수 | 30 |

## 순위 공식 {#ranking-formulas}

| 가드레일 | 제한 |
| ------- | ------- |
| 순위 공식 PQL의 최대 크기 | 8K(UTF-8) |
| 최대 프로필 속성 수 | 25 |
| 최대 컨텍스트 데이터 속성 수 | 30 |
| 최대 중첩 수준 수 | 30 |

## 기타 {#others}

| 가드레일 | 제한 |
| ------- | ------- |
| 오퍼 카탈로그 스키마당 사용자 지정 속성 수 | 10 |
| 총 오퍼 항목 | 10K |
| 총 배치 | 1K |
| AI 등급 모델 | 5 |
| 빈도 규칙 - 오퍼당 최대 한도 규칙 수 | 10 |
