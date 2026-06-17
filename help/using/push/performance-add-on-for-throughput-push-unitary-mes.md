---
solution: Journey Optimizer
product: journey optimizer
title: 처리량 - (푸시) 단일 - 메시지 게재를 위한 성능 추가 기능
description: Adobe Journey Optimizer에서 처리량 - (푸시) 단일 메시지 전달을 위한 성능 추가 기능을 구성하고 사용하는 방법을 알아봅니다.
feature: Push
topic: Content Management
role: User
level: Intermediate
exl-id: 2d0677ad-41c8-4299-a7c8-0e4f8a1716f7
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: c96d2aa5-76a2-443d-8d23-5de95577c909
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b6b77c26-2a48-4a62-9ceb-5ae67f4dfde5
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 4aebdb06094628cfe7393c7f7b41e5fe0ee9df13
workflow-type: tm+mt
source-wordcount: 252
ht-degree: 3%

---


# 처리량 - (푸시) 단일 - 메시지 게재를 위한 성능 추가 기능 {#performance-add-on-for-throughput-push-unitary-mes}

>[!AVAILABILITY]
>
>이 기능은 **AJO26.7**(2026-07-27)에서 사용할 수 있습니다.

## 개요 {#overview}

Adobe Journey Optimizer에서는 **처리량을 위한 성능 추가 기능 - (푸시) 단일 - 메시지 게재**&#x200B;를 도입하여 조직에서 푸시 채널 전체에 보다 관련성이 높고 개인화된 고객 경험을 제공할 수 있습니다.

이 페이지에서는 캠페인 및 여정에서 이 기능을 구성하고 사용하는 방법을 설명합니다.

## 사전 요구 사항 {#prerequisites}

시작하기 전에:

* 필요한 **푸시** 권한으로 Adobe Journey Optimizer에 액세스할 수 있습니다.
* 푸시 채널 표면이 구성되어 있습니다. [푸시 채널 구성](../configuration/channel-surfaces.md)을 참조하세요.

## 작동 방식 {#how-it-works}

처리량을 위한 성능 추가 기능 - (푸시) 단일 - 메시지 게재는 AJO 실행 엔진과 직접 통합됩니다. 프로필이 여정 또는 캠페인의 푸시 동작에 도달하면 구성된 매개 변수를 전송 시간에 적용하는 기능입니다.

주요 기능:

* **프로필 수준 개인화** - 프로필 및 컨텍스트 특성을 사용하여 수신자별로 설정이 조정됩니다.
* **여정 및 캠페인 지원** - 오케스트레이션된 여정과 일회성 캠페인 모두에서 작동합니다.
* **실시간 지표** — 결과는 [푸시 보고서](../reports/push-report.md)에 표시됩니다.

## 처리량을 위한 성능 추가 기능 구성 {#configure}

1. AJO 왼쪽 메뉴에서 **채널** > **푸시 구성**&#x200B;으로 이동합니다.
1. 채널 구성을 선택하거나 만듭니다.
1. **에 대한**&#x200B;성능 추가 기능 섹션에서 기능을 사용하도록 설정합니다.
1. 필요한 매개 변수를 설정합니다.
1. **저장**&#x200B;을 클릭합니다.

>[!NOTE]
>
>구성 변경 사항은 새 여정 실행에 적용됩니다. 진행 중인 여정은 영향을 받지 않습니다.

## 관련 항목 {#related-topics}

* [푸시 시작](get-started-push.md)
* [푸시 알림 만들기](create-push.md)
* [AJO26.7 릴리스 노트](../rn/release-notes.md)
