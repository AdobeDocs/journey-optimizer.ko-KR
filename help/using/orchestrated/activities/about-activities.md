---
solution: Journey Optimizer
product: journey optimizer
title: 오케스트레이션된 캠페인 활동 작업
description: 캠페인 활동을 오케스트레이션하는 방법 알아보기
exl-id: 02f986b2-8200-4e0e-8918-44e528a6a3ec
version: Campaign Orchestration
TQID: https://experienceleague.adobe.com/OUKBJeSTaPJKav-NNCCxKZ8esY-62JkdRMmcwoJpZJ0
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29c
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
subfeature_v2: id: b5e335a9-0e5f-4dda-8845-c4ac5dca2be4
source-git-commit: 4bae03291d44603ab1648416f34dd1a8b414a07a
workflow-type: tm+mt
source-wordcount: 530
ht-degree: 56%

---

# 오케스트레이션된 캠페인 활동 기본 정보 {#orchestrated-campaign-activities}

오케스트레이션된 캠페인 활동은 세 가지 카테고리로 그룹화됩니다. 컨텍스트에 따라 사용 가능한 활동이 다를 수 있습니다.

모든 활동은 아래 섹션에 자세히 설명되어 있습니다.

* [타기팅 활동](#targeting)
* [채널 활동](#channel)
* [흐름 제어 활동](#flow-control)

![캔버스에서 사용 가능한 활동 목록](../assets/orchestrated-activities.png){width="80%"}

>[!NOTE]
>
>라이선스 모델, 권한 및 구현에 따라 사용 가능한 활동이 다를 수 있습니다.

## 가드레일 및 제한 사항 {#activity-guardrails}

* **채널 활동 제한** - 오케스트레이션된 캠페인은 게시 시 최대 10개의 채널 활동(전자 메일, SMS, 푸시 또는 DM)을 지원합니다. 타겟팅 및 흐름 제어 활동은 이 제한에 포함되지 않습니다.

* **캔버스 활동 제한** - 캔버스의 활동 수는 500개로 제한됩니다. 유지 관리 및 성능을 위해 워크플로우를 100개 미만으로 유지하십시오.

오케스트레이션된 모든 캠페인 보호 및 제한 사항에 대해서는 [보호 및 제한 사항](../guardrails.md)을 참조하십시오.

## 타기팅 활동 {#targeting}

이 활동은 타기팅에만 해당됩니다. 이를 통해 대상자를 정의하고 교차, 합집합 또는 제외 작업을 사용하여 이러한 대상자를 분할 또는 결합하여 하나 이상의 대상을 빌드할 수 있습니다.

![타기팅 활동 목록](../assets/targeting-activities.png){width="40%"}

사용 가능한 타겟팅 활동은 다음과 같습니다.

* [대상자 작성](build-audience.md): 대상 집단을 정의합니다. 기존 대상자를 선택하거나 규칙 빌더를 사용하여 자체 쿼리를 정의할 수 있습니다.
* [차원 변경](change-dimension.md): 오케스트레이션된 캠페인을 빌드할 때 타깃팅 차원을 변경합니다.
* [결합](combine.md): 인바운드 집단에 세분화를 수행합니다. 합집합, 교차 또는 제외를 사용할 수 있습니다.
* [중복 제거](deduplication.md): 인바운드 활동의 결과에서 중복 항목을 삭제합니다.
* [데이터 보강](enrichment.md): 오케스트레이션된 캠페인에서 처리할 추가 데이터를 정의합니다. 이 활동을 사용하여 인바운드 전환을 활용하고 추가 데이터로 출력 전환을 완료하도록 활동을 구성할 수 있습니다.
* [조정](reconciliation.md): Journey Optimizer 데이터의 데이터와 작업 테이블의 데이터(예: 외부 파일에서 로드된 데이터) 간의 링크를 정의합니다.
* [분할](split.md): 들어오는 집단을 여러 하위 집합으로 세분화합니다.

## 채널 활동 {#channel}

Adobe Journey Optimizer에서는 여러 채널에 걸쳐 마케팅 캠페인을 자동화하고 실행할 수 있습니다. [채널 활동](channels.md)을 캔버스에 결합하여 고객 행동에 따라 작업을 트리거할 수 있는 크로스 채널 오케스트레이션된 캠페인을 만들 수 있습니다.

오케스트레이션된 캠페인에서 [채널 작업을 만드는 방법](channels.md)을 알아보세요.

## 흐름 제어 활동 {#flow-control}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_end"
>title="종료 활동"
>abstract="**종료** 활동은 캔버스에서 분기의 끝을 표시합니다. 필요한 경우 **외부 신호**&#x200B;를 사용하여 다운스트림 오케스트레이션된 캠페인을 시작하고 분기가 완료될 때 매개변수를 전달합니다. [자세히 알아보기](../trigger-orchestrated-campaign.md#signal-end)"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_signal"
>title="외부 신호"
>abstract="이 분기가 종료될 때 시작할 다운스트림 오케스트레이션된 캠페인을 선택하고, 신호를 전송할 매개변수 이름 및 값을 매핑합니다. 다운스트림 캠페인은 **신호에 의해 트리거됨**&#x200B;으로 설정되어야 이 캠페인이 종료 활동에 도달하기 전에 게시됩니다. [자세히 알아보기](../trigger-orchestrated-campaign.md#signal-end)"

다음 활동은 오케스트레이션된 캠페인을 구성하고 실행하는 데 특정적입니다. 이들의 주요 임무는 다른 활동을 조정하는 것입니다.

![흐름 제어 활동 목록](../assets/flow-control-activities.png){width="20%"}

사용 가능한 흐름 제어 활동은 다음과 같습니다.

* [And-join](and-join.md): 오케스트레이션된 캠페인의 여러 실행 분기를 동기화합니다.
* [포크](fork.md): 아웃바운드 전환을 만들어 여러 활동을 동시에 시작할 수 있습니다.
* [대기](wait.md): 오케스트레이션된 캠페인의 일부 실행을 잠시 일시 중지합니다.
  <!--* [Test](test.md): Enable transitions based on specified conditions.-->

* **[!UICONTROL 끝]**: 캔버스에서 분기의 끝을 표시합니다. 원할 경우 이를 사용하여 신호에서 시작하는 다른 오케스트레이션된 캠페인에 신호를 보낼 수 있습니다. [자세히 알아보기](../trigger-orchestrated-campaign.md#signal-end)
