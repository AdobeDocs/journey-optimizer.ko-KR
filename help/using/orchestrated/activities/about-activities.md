---
solution: Journey Optimizer
product: journey optimizer
title: 오케스트레이션된 캠페인 활동 작업
description: 캠페인 활동을 오케스트레이션하는 방법 알아보기
exl-id: 02f986b2-8200-4e0e-8918-44e528a6a3ec
version: Campaign Orchestration
source-git-commit: 4d5505cbb46bdff846218bfc3657c6a6e5447af3
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 61%

---


# 오케스트레이션된 캠페인 활동 기본 정보 {#orchestrated-campaign-activities}

오케스트레이션된 캠페인 활동은 세 가지 카테고리로 그룹화됩니다. 컨텍스트에 따라 사용 가능한 활동이 다를 수 있습니다.

모든 활동은 아래 섹션에 자세히 설명되어 있습니다.

* [타기팅 활동](#targeting)
* [채널 활동](#channel)
* [흐름 제어 활동](#flow-control)

![캔버스에서 사용 가능한 활동 목록](../assets/orchestrated-activities.png){width="80%" align="left"}


>[!NOTE]
>
>* 라이선스 모델, 권한 및 구현에 따라 사용 가능한 활동이 다를 수 있습니다.
>
>* 오케스트레이션된 캠페인의 활동 수는 500개로 제한됩니다.


## 타기팅 활동 {#targeting}

이 활동은 타기팅에만 해당됩니다. 이를 통해 대상자를 정의하고 교차, 합집합 또는 제외 작업을 사용하여 이러한 대상자를 분할 또는 결합하여 하나 이상의 대상을 빌드할 수 있습니다.

![타기팅 활동 목록](../assets/targeting-activities.png){width="40%" align="left"}

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
>abstract="**종료** 활동을 사용하여 오케스트레이션된 캠페인의 끝을 그래픽으로 표시할 수 있습니다. 이 활동은 기능에 영향을 미치지 않으므로 선택 사항입니다."

다음 활동은 오케스트레이션된 캠페인을 구성하고 실행하는 데 특정적입니다. 이들의 주요 임무는 다른 활동을 조정하는 것입니다.

![흐름 제어 활동 목록](../assets/flow-control-activities.png){width="20%" align="left"}

사용 가능한 흐름 제어 활동은 다음과 같습니다.

* [And-join](and-join.md): 오케스트레이션된 캠페인의 여러 실행 분기를 동기화합니다.
* [포크](fork.md): 아웃바운드 전환을 만들어 여러 활동을 동시에 시작할 수 있습니다.
* [대기](wait.md): 오케스트레이션된 캠페인의 일부 실행을 잠시 일시 중지합니다.
  <!--* [Test](test.md): Enable transitions based on specified conditions.-->

>[!NOTE]
>**End** 활동은 오케스트레이션된 캠페인의 끝을 그래픽으로 표시합니다. 이 활동은 기능에 영향을 미치지 않으므로 선택 사항입니다.
