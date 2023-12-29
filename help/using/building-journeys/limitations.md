---
solution: Journey Optimizer
product: journey optimizer
title: 여정 제한 사항
description: 여정 제한에 대해 자세히 알아보기
feature: Journeys, Best Practices, Guardrails
topic: Content Management
role: User
level: Intermediate
keywords: 여정, 제한
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 47%

---

# 제한 사항 {#journey-limitations}

다음은 여정 사용과 관련된 제한 사항입니다.

## 일반 작업 제한 사항 {#action-limitations}

* 전송 제한이 없습니다.  
* 오류가 발생하면 시스템에서 세 번 다시 시도합니다. 수신된 오류 메시지에 따라 재시도 횟수를 조정할 수 없습니다. 
* 기본 제공 **반응** 이벤트를 사용하면 즉시 사용 가능한 작업에 반응할 수 있습니다(다음 참조) [페이지](../building-journeys/reaction-events.md)). 사용자 지정 작업을 통해 전송된 메시지에 반응하려면 전용 이벤트를 구성해야 합니다. 
* 두 가지 작업을 병렬로 배치할 수 없으며 하나씩 추가해야 합니다.

## 여정 버전 제한 사항 {#journey-versions-limitations}

* v1에서 이벤트 활동으로 시작하는 여정은 이후 버전에서 이벤트 이외의 다른 것으로 시작할 수 없습니다. (으)로 여정을 시작할 수 없음 **대상 자격 조건** 이벤트.
* 다음으로 시작하는 여정 **대상 자격 조건** v1의 활동은 항상 다음으로 시작해야 함 **대상 자격 조건** 추가 버전에서.
* 에서 선택된 대상자 및 네임스페이스 **대상 자격 조건** (첫 번째 노드)는 새 버전에서 변경할 수 없습니다.
* 재입력 규칙은 모든 여정 버전에서 동일해야 합니다.
* **대상자 읽기**&#x200B;로 시작하는 여정은 다음 버전에서 다른 이벤트로 시작할 수 없습니다.

## 사용자 지정 작업 제한 사항 {#custom-actions-limitations}

* 사용자 정의 작업 URL은 동적 매개 변수를 지원하지 않습니다.  
* POST 및 PUT 호출 메서드만 지원됩니다. 
* 쿼리 매개 변수 또는 헤더의 이름은 “.” 또는 &quot;$&quot;입니다. 
* IP 주소는 허용되지 않습니다. 
* 내부 Adobe 주소(.adobe.)를 사용할 수 없습니다.

## 이벤트 제한 사항 {#events-limitations}

* 시스템 생성 이벤트의 경우 고유한 오케스트레이션 ID를 얻으려면 먼저 고객 여정을 시작하는 데 사용되는 스트리밍 데이터를 Journey Optimizer 내에서 구성해야 합니다. 이 오케스트레이션 ID는 Adobe Experience Platform으로 들어오는 스트리밍 페이로드에 추가되어야 합니다. 이 제한은 규칙 기반 이벤트에는 적용되지 않습니다. 

## 데이터 소스 제한 사항 {#data-sources-limitations}

* 고객 여정 내에서 외부 데이터 소스를 활용하여 실시간으로 외부 데이터를 조회할 수 있습니다. 이러한 소스는 REST API를 통해 사용할 수 있어야 하고 JSON을 지원하고 요청 볼륨을 처리할 수 있어야 합니다.

## 프로필 만들기와 동시에 시작하는 여정 {#journeys-limitation-profile-creation}

Adobe Experience Platform에서 API 기반 프로필 만들기/업데이트와 관련된 지연이 발생합니다. 지연 시간 측면에서 SLT(서비스 수준 목표)는 20,000RPS(초당 요청) 볼륨에서 95번째 백분위수 요청에 대해 수집에서 통합 프로필까지 1분 미만입니다.

프로필 만들기와 동시에 여정이 트리거되고 Profile Service에서 정보를 즉시 확인/검색하면 제대로 작동하지 않을 수 있습니다.

다음 두 가지 솔루션 중 하나를 선택할 수 있습니다.

* 첫 번째 이벤트 후에 대기 활동을 추가하여 Adobe Experience Platform에 Profile Service에 대한 수집을 수행하는 데 필요한 시간을 제공합니다.

* 프로필을 즉시 활용하지 않는 여정을 설정합니다. 예를 들어 여정이 계정 만들기를 확인하도록 디자인된 경우 경험 이벤트에는 첫 번째 확인 메시지(이름, 성, 이메일 주소 등)를 보내는 데 필요한 정보가 포함될 수 있습니다.

## 대상자 제한 사항 읽기 {#read-audiences-limitations}

* 스트리밍 대상자는 항상 최신 상태이지만 일괄 처리 대상자는 검색하는 순간에 계산되지 않습니다. 일일 배치 평가 시간에만 매일 평가됩니다.
