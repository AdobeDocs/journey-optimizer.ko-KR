---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Journey Optimizer을 사용하여 오케스트레이션된 캠페인 시작 및 모니터링
description: Adobe Journey Optimizer을 사용하여 오케스트레이션된 캠페인을 시작 및 모니터링하는 방법을 알아봅니다.
hide: true
hidefromtoc: true
exl-id: 3c1cad30-3ed7-4df1-a46a-60394a834e79
source-git-commit: 0ae8372c179707a87a6b512a5420753a4aaef754
workflow-type: tm+mt
source-wordcount: '591'
ht-degree: 2%

---

# 리타겟팅 쿼리 빌드 {#retarget}

+++ 목차

| 오케스트레이션된 캠페인 시작 | 첫 오케스트레이션된 캠페인 시작 | 데이터베이스 쿼리 | 오케스트레이션된 캠페인 활동 |
|---|---|---|---|
| [오케스트레이션된 캠페인 시작](gs-orchestrated-campaigns.md)<br/><br/>[구성 단계](configuration-steps.md)<br/><br/>[오케스트레이션된 캠페인 액세스 및 관리](access-manage-orchestrated-campaigns.md)<br/><br/>[오케스트레이션된 캠페인을 만드는 주요 단계](gs-campaign-creation.md) | [캠페인 만들기 및 예약](create-orchestrated-campaign.md)<br/><br/>[활동 오케스트레이션](orchestrate-activities.md)<br/><br/>[캠페인 시작 및 모니터링](start-monitor-campaigns.md)<br/><br/>[보고](reporting-campaigns.md) | [규칙 빌더로 작업](orchestrated-rule-builder.md)<br/><br/>[첫 번째 쿼리 빌드](build-query.md)<br/><br/>[표현식 편집](edit-expressions.md)<br/><br/><b>[재타겟팅](retarget.md)</b> | [활동 시작](activities/about-activities.md)<br/><br/>활동:<br/>[및 가입](activities/and-join.md) - [대상 작성](activities/build-audience.md) - [차원 변경](activities/change-dimension.md) - [채널 활동](activities/channels.md) - [결합](activities/combine.md) - [중복 제거](activities/deduplication.md) - [데이터 보강](activities/enrichment.md) - [포크](activities/fork.md) - [조정](activities/reconciliation.md) - [대상 저장](activities/save-audience.md) - [분할](activities/split.md) - [대기](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

설명서 진행 중

>[!ENDSHADEBOX]

리타겟팅을 사용하면 이전에 오케스트레이션된 캠페인에 응답한 방식을 기반으로 수신자를 후속 처리할 수 있습니다. 예를 들어 첫 번째 이메일을 수신했지만 클릭하지 않은 프로필에 두 번째 이메일을 보낼 수 있습니다.

오케스트레이션된 캠페인에서는 이를 위한 두 가지 기본 데이터 소스를 제공합니다.

- **메시지 피드백**: 게재 관련 이벤트(예: 보낸 메시지, 연 메시지, 반송된 메시지 등)를 캡처합니다.

- **전자 메일 추적**: 사용자 작업(예: 클릭 및 열기)을 캡처합니다.

## 피드백 기반 리타겟팅 규칙 만들기

피드백 기반 리타겟팅 규칙을 사용하면 **메시지 피드백** 데이터 집합에서 캡처된 메시지 게재 이벤트에 따라 수신자를 리타겟팅할 수 있습니다. 이러한 이벤트에는 전송, 열기, 반송 또는 스팸으로 표시된 메시지와 같은 결과가 포함됩니다.

이 데이터를 사용하여 이전 메시지를 수신했지만 해당 메시지에 관여하지 않은 수신자를 식별하는 규칙을 정의할 수 있으므로 특정 게재 상태에 따라 후속 커뮤니케이션이 가능합니다.

1. 새 **오케스트레이션된 캠페인 만들기**.

2. **대상자 빌드** 활동을 추가하고 타겟팅 차원을 **수신자(caas)**(으)로 설정합니다.

3. **규칙 빌더**&#x200B;에서 **조건 추가**&#x200B;를 클릭하고 특성 선택기에서 **메시지 피드백**&#x200B;을 선택합니다. **확인**&#x200B;을 클릭합니다.

4. **피드백 상태**&#x200B;에 대한 조건을 추가하고 값을 **보낸 메시지**(으)로 설정합니다.

5. 오케스트레이션된 특정 캠페인을 타깃팅하려면:

   - 다른 조건을 추가하고 `entity`을(를) 검색한 후 다음으로 이동:\
     `_experience > CustomerJourneyManagement > Entities > AJO Orchestrated Campaign`.

   - **오케스트레이션된 캠페인 이름**&#x200B;을 선택하고 캠페인 이름을 지정합니다.

6. 오케스트레이션된 캠페인 내에서 특정 메시지 또는 활동을 타겟팅하려면 다음을 수행합니다.

   - 다른 조건을 추가하고 `entity`을(를) 검색한 후 다음으로 이동:\
     `_experience > CustomerJourneyManagement > Entities > AJO Orchestrated Campaign`.

   - **오케스트레이션된 캠페인 작업 이름**&#x200B;을 선택하고 캠페인 작업 이름을 지정합니다.

     캔버스에서 활동 옆에 있는 ![정보 아이콘](assets/do-not-localize/info-icon.svg)을 클릭하여 작업 이름을 찾을 수 있습니다.

   >[!TIP]
   >
   >이름을 사용하는 대신 Campaign 속성에서 찾을 수 있는 **Campaign ID**(UUID)별로 필터링할 수도 있습니다.

## 추적 기반 리타겟팅 규칙 만들기

추적 기반 리타겟팅 규칙은 **전자 메일 추적** 데이터 세트의 데이터를 사용하여 메시지와의 상호 작용에 따라 수신자를 타깃팅합니다. 이메일 열기 및 링크 클릭과 같은 사용자 작업을 캡처합니다.

메시지 상호 작용(예: 열기 또는 클릭)에 따라 수신자를 다시 타겟팅하려면 다음과 같이 **전자 메일 추적** 엔터티를 사용합니다.

1. 새 **오케스트레이션된 캠페인**&#x200B;을(를) 만든 다음 **수신자(caas)**&#x200B;를 타깃팅 차원으로 사용하는 **대상자 빌드** 활동을 추가하여 오케스트레이션된 이전 캠페인 수신자에게 집중합니다.

1. **전자 메일 추적**&#x200B;에 대한 새 조건을 추가합니다. **확인**&#x200B;을 클릭하여 &quot;전자 메일 추적이 다음과 같이 존재합니다&quot; 조건을 만듭니다.

1. 해당 조건 내에 조건을 추가하고 **상호 작용 유형** 특성을 검색합니다.

1. 사용자 지정 조건 옵션에서 연산자로 **포함**&#x200B;을(를) 사용하고 사용 사례에 따라 하나 이상의 값을 선택합니다. 예:
   - **열린 메시지**
   - **클릭한 메시지 링크**

1. 추적 데이터를 특정 캠페인과 연결하려면 다음 작업을 수행하십시오.

   - 이메일 추적 블록 내에 조건을 추가합니다.

   - `_experience > CustomerJourneyManagement > Entities > AJO Orchestrated Campaign`(으)로 이동합니다.

   - **오케스트레이션된 캠페인 이름** 및 필요한 경우 **오케스트레이션된 캠페인 작업 이름**&#x200B;에 대한 조건을 추가합니다.

     캔버스에서 활동 옆에 있는 ![정보 아이콘](assets/do-not-localize/info-icon.svg)을 클릭하여 작업 이름을 찾을 수 있습니다.

   >[!TIP]
   >
   >이름을 사용하는 대신 Campaign 속성에서 찾을 수 있는 **Campaign ID**(UUID)별로 필터링할 수도 있습니다.
