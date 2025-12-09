---
solution: Journey Optimizer
product: journey optimizer
title: 프로필 항목 관리
description: 프로필 항목 관리 방법 알아보기
feature: Journeys, Profiles
role: User
level: Intermediate
keywords: 재입력, 여정, 프로필, 반복
exl-id: 8874377c-6594-4a5a-9197-ba5b28258c02
version: Journey Orchestration
source-git-commit: b0b297ed33ab273a3201569760e1d2db5b3ccaad
workflow-type: tm+mt
source-wordcount: '1207'
ht-degree: 3%

---


# 프로필 시작 관리 {#entry-management}

여정 등록 관리는 프로필 유형에 따라 다릅니다.

>[!TIP]
>
>실제 사례를 사용한 실용적인 지침을 찾고 계십니까? 시작 캠페인, 포기한 장바구니 복구 및 전체 시작 및 종료 구성 예와 같은 충성도 프로그램과 같은 사용 사례가 포함된 [여정 시작 및 종료 기준에 대한 포괄적인 안내서](entry-exit-criteria-guide.md)를 참조하십시오.

## 여정 유형 {#types-of-journeys}

Adobe Journey Optimizer을 사용하여 다음 유형의 여정을 만들 수 있습니다.

* **단일 이벤트** 여정: 이러한 여정은 단일 이벤트로 시작합니다. 이벤트가 수신되면 관련 프로필이 여정에 들어갑니다. [자세히 보기](#entry-unitary)

* **비즈니스 이벤트** 여정: 이 여정은 비즈니스 이벤트로 바로 시작한 다음 **대상자 읽기** 활동으로 시작합니다. 이벤트가 수신되면 타겟팅된 대상에 속하는 프로필이 여정에 들어갑니다. 각 프로필에 대해 이 여정의 인스턴스가 하나씩 생성됩니다. [자세히 보기](#entry-business)

* **대상자 읽기** 여정: 이 여정은 **대상자 읽기** 활동으로 시작합니다. 여정이 실행되면 타겟팅된 대상에 속하는 프로필이 여정에 들어갑니다. 각 프로필에 대해 이 여정의 인스턴스가 하나씩 생성됩니다. 이러한 여정은 반복 또는 &quot;일회성&quot;일 수 있습니다. [자세히 보기](#entry-read-audience)

* **대상 자격** 여정: 이 여정은 대상 자격 이벤트로 시작합니다. 이러한 여정은 대상자의 프로필 출입구를 수신합니다. 이런 경우 관련 프로필이 여정에 들어갑니다. [자세히 보기](#entry-unitary)

모든 여정 유형에서 여정의 모든 활성 [버전](publish-journey.md#journey-versions)에 대해 프로필이 동일한 여정에 동시에 여러 번 있을 수 없습니다. 개인이 여정에 있는지 확인하기 위해 프로필 ID가 키로 사용됩니다. 시스템에서 동일한 키(예: 키 `CRMID=3224`)가 동일한 여정의 다른 위치에 있도록 허용하지 않습니다.

## 여정 처리율 {#journey-processing-rate}

여정 처리 속도는 프로필이 여정을 통해 이동하는 방식을 결정하는 여러 요인에 의해 영향을 받습니다.

### 프로필 진입률 {#profile-entrance-rate}

프로필이 여정 및 예상 비율을 입력하는 방법은 사용 중인 첫 번째 활동에 따라 다릅니다.

* **대상 읽기** 여정(프로필 대상을 타겟팅하고 해당 전체 대상에 대한 여정을 트리거하는 일괄 처리 시나리오): 최대값은 **샌드박스 수준**&#x200B;에서 사용할 수 있는 할당량인 20,000TPS(초당 트랜잭션)입니다. 해당 샌드박스에서 여러 여정이 동시에 실행되고 있는 경우 20,000개의 TPS를 달성할 수 없습니다. 이 최대값을 최상의 사례 시나리오로 간주합니다.

* **대상 자격** 여정(프로필이 스트리밍 대상의 자격을 얻거나 빼앗길 때 여정을 트리거하려는 단일 시나리오): 최대값은 5,000TPS입니다. 이 제한은 이벤트로 시작하는 여정에 대한 공유 제한이며 **조직 수준**&#x200B;에서 여정 간에 공유됩니다.

* **단일 이벤트** 여정(프로필에서 이벤트가 방출될 때 여정을 트리거하려는 단일 시나리오): 위와 동일하며 둘 다 동일한 5,000TPS 제한을 공유합니다. 여정 이벤트 처리량에 대한 자세한 정보는 [이 섹션](../event/about-events.md#event-thoughput)에서 확인할 수 있습니다.

* **비즈니스 이벤트** 여정(비즈니스 이벤트가 항상 대상자 읽기와 함께 수행되기 때문에 기본적으로 단일 대 일괄 시나리오임): 비즈니스 이벤트도 TPS 할당량 5,000에 포함되지만 바로 뒤에 대상자 읽기 활동은 대상자 읽기(20,000TPS)로 시작하는 여정과 동일한 제한을 갖습니다.

### 여정 내 이벤트 및 대상 자격 요건 {#events-inside-journeys}

입장한 후에는 여정 내에서 **단일 이벤트** 또는 **대상 자격** 활동을 사용할 수 있습니다. 프로필은 위에 설명된 4가지 유형의 여정 중 하나에 입력하여 이벤트가 방출될 때까지 기다리거나 이 프로필이 대상에 적합한지 기다릴 수 있습니다. 이러한 단일 이벤트 및 대상 자격은 위에서 설명한 할당량에 포함됩니다. 예를 들어 읽기 대상(최대 20,000TPS)으로 여정을 시작하고 바로 뒤에 이벤트가 있는 경우 이 이벤트는 최대 5,000TPS가 됩니다.

### 대기 활동 영향 {#wait-activities-impact}

여정의 **대기** 활동은 특정 시간에 여정을 통해 흐르는 프로필 수에 영향을 줄 수도 있습니다. 일반적으로 대기 활동은 상대적 시간을 기반으로 합니다(예: 대기를 입력한 후 2시간 후에 종료되므로 모든 프로필이 동시에 종료되지 않음). 그러나 해당 대기 활동에 고정 시간이 정의된 경우, 정확히 동시에 여러 프로필이 해당 여정을 종료할 수 있습니다. 권장되는 방법은 아닙니다. 대량 볼륨을 볼 수 있으며 이 시점에서의 TPS는 20,000 TPS를 초과할 수 있습니다.

### 작업 활동 {#action-activities-impact}

마지막으로 **작업** 활동(이메일, SMS, 푸시 등 기본 채널, 아웃바운드 또는 인바운드, 사용자 지정 작업, 다른 여정으로 프로필 전송 점프, 통합 프로필 서비스로 데이터 전송 프로필 업데이트 등)은 여정에서 발생하는 프로필 부하의 영향을 받을 수 있지만 처리 속도에도 영향을 줄 수 있습니다. 예를 들어 응답 시간이 긴 외부 끝점을 대상으로 하는 사용자 지정 작업은 여정 처리 속도를 느리게 합니다.

사용자 지정 작업의 경우 기본 제한은 분당 300,000회 호출이며, 사용자 지정 제한 정책으로 변경할 수 있습니다. [이 섹션](../configuration/external-systems.md#capping)에서 사용자 지정 작업 한도에 대해 자세히 알아보세요.

## 단일 이벤트 및 대상 자격 여정{#entry-unitary}

**단일 이벤트** 및 **대상 자격** 여정에서 재등록을 활성화하거나 비활성화할 수 있습니다.

* 재입력이 활성화된 경우 프로필은 여정을 여러 번 입력할 수 있지만 여정의 이전 인스턴스를 완전히 종료할 때까지는 다시 입력할 수 없습니다.

* 재입력이 비활성화된 경우 프로필은 글로벌 여정 시간 제한 기간 내에 동일한 여정을 여러 번 입력할 수 없습니다. 이 [섹션](../building-journeys/journey-properties.md#global_timeout)을 참조하세요.

기본적으로 여정은 재입력을 허용합니다. **재입력 허용** 옵션이 활성화되면 **재입력 대기 기간** 필드가 표시됩니다. 프로필에서 여정을 다시 입력할 수 있도록 허용하기 전에 대기할 시간을 정의할 수 있습니다. 이를 통해 동일한 이벤트에 대해 여정을 여러 번 트리거하는 오류를 방지할 수 있습니다. 이 필드는 기본적으로 5분으로 설정되어 있습니다. 최대 기간은 91일([전역 시간 초과](journey-properties.md#global_timeout))입니다.

<!--
When a journey ends, its status is **[!UICONTROL Closed]**. New individuals can no longer enter the journey. Persons already in the journey automatically exit the journey. 
-->

![여정 속성에서 다시 시작 설정 전환](assets/journey-re-entrance.png)

재입력 기간이 지나면 프로필이 여정에 다시 들어갈 수 있습니다. 이를 방지하고 이러한 프로필에 대한 재입력을 완전히 비활성화하려면 프로필 또는 대상 데이터를 사용하여 프로필이 이미 입력되었는지 여부를 테스트하는 조건을 추가할 수 있습니다.

<!--
Due to the 30-day journey timeout, when journey reentrance is not allowed, we cannot make sure the reentrance blocking will work more than 91 days. Indeed, as we remove all information about persons who entered the journey 91 days after they enter, we cannot know the person entered previously, more than 91 days ago. -->

## 비즈니스 여정 {#entry-business}

<!--
Business events follow reentrance rules in the same way as for unitary events. If a journey allows reentrance, the next business event will be processed.
-->

**비즈니스 여정**&#x200B;에서 여러 비즈니스 이벤트 실행을 허용하려면 여정 속성의 **[!UICONTROL 실행]** 섹션에서 해당 옵션을 활성화합니다.

![여정 구성의 비즈니스 이벤트 항목 관리 옵션](assets/business-entry.png)

비즈니스 이벤트의 경우, 주어진 여정의 경우 첫 번째 실행 시 검색된 대상 데이터가 1시간 기간 동안 재사용됩니다.

프로필은 동일한 여정에 동시에 여러 번 표시될 수 있지만, 서로 다른 비즈니스 이벤트의 컨텍스트에 있을 수 있습니다.

자세한 정보는 이 [섹션](../event/about-creating-business.md)을 참조하세요.

## 대상자 여정 읽기 {#entry-read-audience}

**대상자 읽기** 여정은 반복 또는 &quot;일회성&quot;일 수 있습니다.

* 반복되지 않는/&quot;단발성&quot; 여정의 경우: 프로필은 여정에 한 번만 입력합니다.

* 반복 여정의 경우: 기본적으로 대상에 속하는 모든 프로필은 각 반복에 여정을 입력합니다. 다른 경우에 다시 입력하기 전에 여정을 완료해야 합니다.

반복 대상자 읽기 여정에 몇 가지 옵션을 사용할 수 있습니다. 자세한 내용은 [여정에서 대상 사용](../building-journeys/read-audience.md) 섹션을 참조하세요.

<!--
After 91 days, a Read audience journey switches to the **Finished** status. This behavior is set for 91 days only (i.e. journey timeout default value) as all information about profiles who entered the journey is removed 91 days after they entered. Persons still in the journey automatically are impacted. They exit the journey after the 30 day timeout. 
-->

## 관련 항목

* [여정 시작 및 종료 기준 안내서](entry-exit-criteria-guide.md) - 실제 사례 및 모범 사례를 포함한 전체 안내서
* [종료 기준 구성](journey-properties.md#exit-criteria) - 프로필이 여정에서 나가는 시기를 정의합니다.
* [여정 종료](end-journey.md) - 여정이 닫히고 완료되는 방법 이해
* [여정 사용 사례](jo-use-cases.md) - 시작 및 종료 구성이 있는 전체 예제를 참조하십시오.
