---
solution: Journey Optimizer
product: journey optimizer
title: 대상자 자격 여정에서 배치 대상자 마이그레이션
description: 시행일 전에 대상 자격 노드에서 배치 대상을 사용하는 여정을 마이그레이션하는 방법을 알아봅니다.
feature: Journeys, Activities, Audiences
topic: Content Management
role: User
level: Intermediate
keywords: 대상 자격, 일괄 처리 대상, 사용 중단, 마이그레이션, 대상 읽기, 스트리밍 대상
exl-id: f3c2a7d1-b58e-4a92-c3d5-0e871f2a9b4c
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
source-git-commit: 4a5cbd65b7046e8f1b82147cdc2cd61a3991c258
workflow-type: tm+mt
source-wordcount: 867
ht-degree: 0%

---


# 대상자 자격 여정에서 배치 대상자 마이그레이션 {#aq-batch-migration}

2026년 8월부터 Journey Optimizer은 대상 자격 노드에서 일괄 대상을 사용하는 여정에 대한 게시를 차단합니다. 아래에서 사용 사례를 식별하고 권장되는 마이그레이션 경로를 따릅니다.

>[!CAUTION]
>
>**시행일: 2026년 8월** 대상 자격 노드의 일괄 처리 대상을 사용하는 신규, 초안 및 중복 여정은 이 날짜 이후에 게시할 수 없습니다. 2026년 6월 릴리스 이후 여정 캔버스에 유효성 검사 경고가 이미 표시되어 있습니다.

## 변경 이유 {#why}

**[대상 자격](audience-qualification-events.md)** 노드는 개별 프로필이 대상으로 들어오거나 나갈 때 실시간에 가깝게 반응하도록 설계되었습니다. 자격 이벤트는 하나씩 지속적으로 도착합니다. 이는 **[스트리밍 대상](../audience/creating-a-segment-definition.md#evaluation-method-in-journey-optimizer)**&#x200B;을 위한 것입니다.

배치 대상을 대상 자격 노드와 함께 대신 사용하면 모든 자격 이벤트가 수집 창 동안 동시에 도착합니다. 이렇게 하면 동시에 수만 개 또는 수백만 개의 여정 항목이 트리거되어 시스템 부하가 심하고 다운스트림 시스템에서 예측할 수 없는 동작이 발생할 수 있습니다. 이는 대상 자격 노드의 의도된 설계가 아닙니다.

**[대상자 읽기](read-audience.md)** 활동은 일괄 처리 기반 사용 사례에 적합한 도구입니다. 이 활동은 제어되고 예측 가능한 방식으로 예약된 일괄 처리를 처리하도록 빌드되었습니다.

## 여정 영향 방식 {#impact}

대상 자격 노드에서 일괄 대상을 사용하는 라이브 여정은 2026년 8월 이후에도 계속 실행됩니다. 그러나 여정을 중지, 복제 또는 다시 게시하는 경우 구성이 업데이트될 때까지 차단됩니다.


| 여정 상태 | 2026년 8월 이후의 영향 |
| --- | --- |
| **라이브 여정** | 영향을 받지 않습니다. 기존 라이브 여정은 계속 실행됩니다. 자동 중지 안 함. |
| **새 여정** | 일괄 처리 대상자가 대체될 때까지 게시에서 차단됩니다. |
| **초안 여정** | 일괄 처리 대상자가 대체될 때까지 게시에서 차단됩니다. |
| **중복된 여정** | 일괄 처리 대상자가 대체될 때까지 게시에서 차단됩니다. |


## 마이그레이션 안내서 {#migration-paths}

대상 자격 노드에서 일괄 처리 대상을 사용하는 경우 아래에서 사용 사례를 식별하고 권장되는 마이그레이션 경로를 따릅니다.

### 사용 사례 1 - AJO 메시지 추적 이벤트를 기반으로 구축된 대상 {#use-case-1}

**표시 형식:** 대상 자격 대상자는 Journey Optimizer의 내부 추적 데이터 세트에서 이메일 전송, 열기 또는 클릭에 따라 조건을 사용합니다. 예를 들어, *&quot;프로필이 이메일을 수신함&quot;* 또는 *&quot;프로필이 이메일을 열었습니다.&quot;*

>[!NOTE]
>
>2024년 11월부터 스트리밍 세분화는 더 이상 Journey Optimizer 추적 데이터 세트에서 이벤트 전송 및 열기를 지원하지 않습니다. 이제 이러한 이벤트를 기반으로 하는 대상이 배치 모드에서 평가됩니다. [대상 평가 방법에 대해 자세히 알아보기](../audience/creating-a-segment-definition.md#evaluation-method-in-journey-optimizer)

**권장 대체 요소:**

* **같은 여정 내에서 열림 또는 클릭에 반응하는 중** — **[반응 이벤트](reaction-events.md)** 노드를 사용하십시오. 별도의 대상 없이 동일한 여정 내에서 전송된 메시지의 열기 및 클릭에 응답할 수 있도록 특별히 빌드되었습니다. [반응 이벤트를 사용한 전체 예제 보기](journeys-uc.md#send-multi-channel-messages)

* **크로스 여정 클릭 타깃팅** — 클릭 이벤트에서 [스트리밍 대상](../audience/creating-a-segment-definition.md#evaluation-method-in-journey-optimizer)을 빌드하고 대신 해당 스트리밍 대상으로 대상 자격 노드를 사용합니다.

* **바운스 기반 제외** — 바운스 동작을 대상 조건으로 모델링하지 않고 Journey Optimizer의 기본 [제외 목록](../configuration/manage-suppression-list.md)을 사용합니다.

* **남은 전송/열기 논리** — 일괄 처리 대상을 안전하게 처리하기 위해 예약된 실행 시 **[대상 읽기](read-audience.md)** 여정으로 전환합니다.


### 사용 사례 2 - 새로운 일괄 처리 세분화 데이터를 기다리는 여정 {#use-case-2}

**표시 형식:** 일일 세분화 작업 후 여정 실행을 예약하고 대상 자격 노드를 사용하여 최신 대상 데이터를 사용할 수 있는 경우에만 여정이 실행되도록 합니다.

**권장 대체 요소:**

**[!UICONTROL 일괄 대상 평가 후 트리거]** 옵션이 활성화된 상태에서 **[대상 읽기](read-audience.md)** 여정을 사용합니다. 이 기본 기능은 세분화 작업이 완료될 때까지 여정 실행을 유지한 다음, 대상 자격 노드 없이도 새 데이터를 사용할 수 있을 때 즉시 시작합니다. [이 옵션을 구성하는 방법을 알아보세요](read-audience.md#schedule)


### 사용 사례 3 - 대규모 주기적 일괄 처리 대상 활성화 {#use-case-3}

**표시 형식:** 정기적으로 많은 대상(잠재적으로 수백만 프로필의 프로필)을 활성화하거나 새로 고치면 새로 자격이 있는 모든 프로필에 대해 대상 자격 여정이 한 번에 실행됩니다.

**권장 대체 요소:**

**[대상자 읽기](read-audience.md)** 여정을 사용합니다. 대규모 대상자를 대량으로 처리하고, 프로필을 제어된 배치로 처리하며, 규모에 맞게 보다 예측 가능하고 안정적인 여정 실행을 제공하기 위해 특별히 빌드되었습니다. [전체 예제 보기](message-to-subscribers-uc.md)

## 사용 사례에 적합한 대체 요소가 없으면 어떻게 합니까? {#exceptions}

위의 마이그레이션 경로를 사용하여 사용 사례를 해결할 수 없는 경우 Adobe 담당자에게 문의하십시오. 기존 대안으로는 해결할 수 없는 사례에 대해서는 개별적으로 검토할 것이다.

## 관련 리소스 {#related}

* [대상 자격 이벤트](audience-qualification-events.md) — 전체 구성 가이드 및 보호 기능
* [대상 활동 읽기](read-audience.md) — 예약된 일괄 처리 대상 항목을 구성하는 방법
* [반응 이벤트](reaction-events.md) — 동일한 여정 내에서 열린 이벤트와 클릭에 반응하는 방법
* [대상 평가 방법](../audience/creating-a-segment-definition.md#evaluation-method-in-journey-optimizer) — 일괄 처리, 스트리밍 및 에지 세분화 설명
* [대상 정보](../audience/about-audiences.md) - 대상 유형 및 Journey Optimizer에서 대상 유형을 작성하는 방법
* [제외 목록 관리](../configuration/manage-suppression-list.md) — 바운스 제외에 액세스하고 구성하는 방법
* [여정 보호 및 제한 사항](limitations.md)
* [여정 시작 및 종료 기준](entry-exit-criteria-guide.md) - 실제 사례를 통해 실시간 및 배치 시작 패턴을 파악합니다.
* [다중 채널 메시지 보내기](journeys-uc.md#send-multi-channel-messages) — 대상자 읽기, 반응 이벤트, 이메일 및 푸시를 결합한 엔드 투 엔드 사용 사례
* [구독자에게 메시지 보내기](message-to-subscribers-uc.md) — 대상자 읽기를 통한 일괄 대상자 활성화를 위한 엔드 투 엔드 사용 사례
