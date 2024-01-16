---
solution: Journey Optimizer
product: journey optimizer
title: 여정에서 대상자 사용
description: 여정에서 대상을 사용하는 방법 알아보기
feature: Journeys, Activities, Audiences
topic: Content Management
role: User
level: Intermediate
keywords: 활동, 여정, 읽기, 대상, 플랫폼
exl-id: 7b27d42e-3bfe-45ab-8a37-c55b231052ee
source-git-commit: d735f8c92466cb17a7364833950312e338c630cc
workflow-type: tm+mt
source-wordcount: '1398'
ht-degree: 10%

---

# 여정에서 대상자 사용 {#segment-trigger-activity}

## 대상자 읽기 활동 추가 {#about-segment-trigger-actvitiy}

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment"
>title="대상자 읽기 활동"
>abstract="대상자 읽기 활동을 사용하여 Adobe Experience Platform 대상자에 속하는 모든 개인이 여정을 시작할 수 있습니다. 여정의 시작은 한 번 또는 정기적으로 실행될 수 있습니다."

사용 **대상자 읽기** 활동을 통해 대상자의 모든 개인이 여정에 들어오도록 할 수 있습니다. 여정의 시작은 한 번 또는 정기적으로 실행될 수 있습니다.

다음에서 생성된 &quot;Luma 앱 열기 및 체크아웃&quot; 대상을 예로 들어 보겠습니다. [대상자 작성](../audience/about-audiences.md) 사용 사례. 대상자 읽기 활동을 사용하면 이 대상자에 속하는 모든 개인에게 여정을 입력하고 조건, 타이머, 이벤트, 작업과 같은 모든 여정 기능을 활용하는 개별화된 여정으로 흐르도록 할 수 있습니다.

## 반드시 알아야 할 사항 {#must-read}

* 대상자 읽기 활동을 사용하는 여정의 경우 정확히 동시에 시작할 수 있는 여정의 최대 개수가 정해져 있습니다. 시스템에서 재시도를 수행하기는 하지만, 정확히 같은 시간에 다섯 개가 넘는 여정(대상자 읽기 활동이 있으며 예약했거나 “최대한 빨리” 시작하는 여정)을 실행하는 것을 피하기 위해 5~10분 간격을 두는 등 시간을 분산하는 것이 좋습니다.

* 대상 읽기, 대상 자격 조건 또는 비즈니스 이벤트 활동으로 시작하는 여정에서 경험 이벤트 필드 그룹을 사용할 수 없습니다.

* 에서는 일괄 대상만 사용하는 것이 좋습니다. **대상자 읽기** 활동. 이렇게 하면 여정에 사용된 대상자에 대해 안정적이고 일관된 카운트를 제공합니다. 대상자 읽기는 일괄 사용 사례용으로 설계되었습니다. 사용 사례에 실시간 데이터가 필요한 경우 **[대상 자격 조건](audience-qualification-events.md)** 활동.

* 현재, 대상 사용 [csv 파일에서 가져옴](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html#import-audience) 또는 다음의 결과물 [컴포지션 워크플로](../audience/get-started-audience-orchestration.md) 인앱 여정은 비공개 베타로 사용할 수 있습니다. 자세한 내용은 Adobe 직원에게 문의하십시오.

## 활동 구성 {#configuring-segment-trigger-activity}

대상 읽기 활동을 구성하는 단계는 다음과 같습니다.

1. 펼치기 **[!UICONTROL 오케스트레이션]** 범주 및 놓기 **[!UICONTROL 대상자 읽기]** 활동을 캔버스에 추가합니다.

   활동은 여정의 첫 번째 단계로 배치해야 합니다.

1. 추가 **[!UICONTROL 레이블]** (선택 사항).

1. 다음에서 **[!UICONTROL 대상자]** 필드에서 여정을 입력할 Adobe Experience Platform 대상을 선택한 다음 을(를) 클릭합니다 **[!UICONTROL 저장]**. 을 사용하여 생성된 모든 Adobe Experience Platform 대상을 선택할 수 있습니다. [세그먼트 정의](../audience/creating-a-segment-definition.md).

   >[!NOTE]
   >
   >또한 을 사용하여 만든 Adobe Experience Platform 대상을 타깃팅할 수도 있습니다. [대상자 구성](../audience/get-started-audience-orchestration.md) 또는 [csv 파일에서 업로드됨](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html#import-audience){target="_blank"}. 이 기능은 현재 Private Beta로 사용할 수 있습니다.

   목록에 표시되는 열을 사용자 정의하고 정렬할 수 있습니다.

   ![](assets/read-segment-selection.png)

   대상자가 추가되면 **[!UICONTROL 복사]** 버튼을 사용하면 해당 이름과 ID를 복사할 수 있습니다.

   `{"name":"Luma app opening and checkout","id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![](assets/read-segment-copy.png)

   >[!NOTE]
   >
   >다음을 보유한 개인만 **실현됨** 및 **기존 항목** 대상자 기여도 상태가 여정으로 들어갑니다. 대상을 평가하는 방법에 대한 자세한 내용은 [세그먼테이션 서비스 설명서](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results){target="_blank"}.

1. 다음에서 **[!UICONTROL 네임스페이스]** 필드에서 개인을 식별하기 위해 사용할 네임스페이스를 선택합니다. 기본적으로 필드는 마지막으로 사용된 네임스페이스로 미리 채워집니다. [네임스페이스에 대해 자세히 알아보기](../event/about-creating.md#select-the-namespace).

   >[!NOTE]
   >
   >서로 다른 ID 중에서 선택한 ID(네임스페이스)가 없는 대상에 속하는 개인은 여정에 들어갈 수 없습니다. 사용자 기반 ID 네임스페이스만 선택할 수 있습니다. 조회 테이블에 대한 네임스페이스를 정의한 경우(예: 제품 조회에 대한 ProductID 네임스페이스) **네임스페이스** 드롭다운 목록입니다.

1. 설정 **[!UICONTROL 독서율]**. 초당 여정을 입력할 수 있는 최대 프로필 수입니다. 이 비율은 이 활동에만 적용되며 여정의 다른 활동에는 적용되지 않습니다. 예를 들어 사용자 지정 작업에 대한 전송률 조절 속도를 정의하려면 전송률 조절 API를 사용해야 합니다. 다음을 참조하십시오. [페이지](../configuration/throttling.md).

   이 값은 여정 버전 페이로드에 저장됩니다. 기본값은 초당 5,000개의 프로필입니다. 이 값은 초당 500개에서 20,000개의 프로필로 수정할 수 있습니다.

   >[!NOTE]
   >
   >샌드박스당 전체 읽기 속도는 초당 20,000개의 프로필로 설정됩니다. 따라서 동일한 샌드박스에서 동시에 실행되는 모든 읽기 대상의 읽기 속도는 초당 최대 20,000개의 프로필을 추가합니다. 이 캡은 수정할 수 없습니다.

1. 다음 **[!UICONTROL 대상자 읽기]** 활동을 통해 대상자가 여정을 입력하는 시간을 지정할 수 있습니다. 이렇게 하려면 **[!UICONTROL 여정 일정 편집]** 여정 속성에 액세스한 다음 **[!UICONTROL 스케줄러 유형]** 필드.

   ![](assets/read-segment-schedule.png)

   기본적으로 대상은 여정을 입력합니다 **[!UICONTROL 빠른 시일 내에]**. 대상자가 특정 날짜/시간 또는 반복적으로 여정을 입력하도록 하려면 목록에서 원하는 값을 선택합니다.

   >[!NOTE]
   >
   >다음 사항에 주의하십시오. **[!UICONTROL 예약]** 섹션은 다음 경우에만 사용할 수 있습니다. **[!UICONTROL 대상자 읽기]** 활동이 캔버스에 삭제되었습니다.

   ![](assets/read-segment-schedule-list.png)

   **증분 읽기** 옵션: 여정에 반복이 있는 경우 **대상자 읽기** 은 처음으로 실행되며 대상자의 모든 프로필이 여정에 들어갑니다. 이 옵션을 사용하면 여정의 마지막 실행 이후 대상에 들어온 개인만 첫 번째 발생 후 타깃팅할 수 있습니다.

   **재발 시 강제 재진입**: 이 옵션을 사용하면 여정에 여전히 있는 모든 프로필이 다음 실행 시 자동으로 종료되도록 할 수 있습니다. 예를 들어 일별 반복 여정에서 2일 대기하는 경우 이 옵션을 활성화하면 프로필이 다음 실행 대상에 있는지 여부에 관계없이 항상 다음 여정 실행 시(즉, 다음 날) 이동됩니다. 이 여정에서 프로필의 수명이 반복 빈도보다 길 수 있는 경우 프로필이 여정을 완료할 수 있도록 이 옵션을 활성화하지 마십시오.

<!--

### Segment filters {#segment-filters}

[!CONTEXTUALHELP]
>id="jo_segment_filters"
>title="About segment filters"
>abstract="You can choose to target only the individuals who entered or exited a specific segment during a specific time window. For example, you can decide to only retrieve all the customers who entered the VIP segment since last week."

You can choose to target only the individuals who entered or exited a specific segment during a specific time window. For example, you can decide to only retrieve all the customers who entered the VIP segment since last week. Only the new VIP customers will be targeted. All the customers who were already part of the VIP segment before will be excluded.

To activate this mode, click the **Segment Filters** toggle. Two fields are displayed:

**Segment membership**: choose whether you want to listen to segment entrances or exits. 

**Lookback window**: define when you want to start to listen to entrances or exits. This lookback window is expressed in hours, starting from the moment the journey is triggered.  If you set this duration to 0, the journey will target all members of the segment. For recurring journeys, it will take into account all entrances/exits since the last time the journey was triggered.

-->

>[!NOTE]
>
>일회성 읽기 대상 여정은 여정 실행 후 30일 후에 완료됨 상태로 이동합니다. 예약된 읽기 대상의 경우 마지막 항목이 실행된 후 30일이 경과해야 합니다.

## 여정 테스트 및 게시 {#testing-publishing}

다음 **[!UICONTROL 대상자 읽기]** 활동을 사용하면 단일 프로필에서 여정을 테스트할 수 있습니다.

이렇게 하려면 테스트 모드를 활성화합니다.

![](assets/read-segment-test-mode.png)

평소대로 테스트 모드를 구성하고 실행합니다. [여정 테스트 방법 알아보기](testing-the-journey.md).

테스트가 실행되면 **[!UICONTROL 로그 표시]** 버튼을 사용하면 테스트 결과를 볼 수 있습니다. 자세한 내용은 다음을 참조하십시오. [이 섹션](testing-the-journey.md#viewing_logs)

![](assets/read-segment-log.png)

테스트가 성공하면 여정을 게시할 수 있습니다( 참조) [여정 게시](publishing-the-journey.md)). 대상자에 속한 개인은 여정 속성에 지정된 날짜/시간에 여정을 입력합니다 **[!UICONTROL 스케줄러]** 섹션.

>[!NOTE]
>
>반복 대상 기반 여정의 경우 마지막 발생이 실행되면 여정이 자동으로 닫힙니다. 종료 날짜/시간이 지정되지 않은 경우 신규 진입에 대한 여정을 수동으로 마감하여 종료해야 합니다.

## 대상 기반 여정의 대상 타기팅

대상 기반 여정은 항상 다음으로 시작 **대상자 읽기** 활동은 Adobe Experience Platform 대상자에 속하는 개인을 검색합니다.

대상자에 속한 대상자는 한 번 또는 정기적으로 검색됩니다.

여정에 입장한 후 대상 오케스트레이션 사용 사례를 만들어 초기 대상의 개인이 여정의 다른 분기로 유입될 수 있도록 할 수 있습니다.

**세그먼테이션**

조건을 사용하여 다음을 사용하여 세분화를 수행할 수 있습니다 **조건** 활동. 예를 들어 VIP 사용자가 특정 경로를 사용하고 비 VIP 사용자가 다른 경로에서 이동하도록 할 수 있습니다.

세분화는 다음을 기반으로 할 수 있습니다.

* 데이터 소스 데이터
* 여정 이벤트 컨텍스트(예: 한 시간 전에 받은 메시지를 클릭했습니까?)
* 예를 들어, 날짜가 어떤 사람이 여정을 거치는 6월에 있습니까?
* 시간, 예를 들어 아침이 개인 시간대의 시간대입니까?
* 여정에서 흐르는 대상을 백분율에 따라 분할하는 알고리즘(예: 90% - 10%)으로, 컨트롤 그룹을 제외합니다.

![](assets/read-segment-audience1.png)

**예외**

동일 **조건** 세분화에 사용되는 활동(위 참조)을 사용하면 모집단의 일부를 제외할 수도 있습니다. 예를 들어 VIP 사용자가 바로 뒤에 종료 단계가 있는 분기로 연결되도록 하여 제외할 수 있습니다.

이 제외는 대상 검색 직후, 모집단 계산을 위해 또는 여러 단계의 여정을 따라 발생할 수 있습니다.

![](assets/read-segment-audience2.png)

**합집합**

여정을 사용하면 N개의 분기를 만들고 세그멘테이션 후 서로 연결할 수 있습니다.

따라서 두 대상이 공통 경험으로 돌아오도록 할 수 있습니다.

예를 들어 여정에서 10일 동안 다른 경험을 팔로우한 후 VIP 및 비 VIP 고객은 동일한 경로로 돌아갈 수 있습니다.

결합 후 세분화 또는 제외를 수행하여 대상을 다시 분할할 수 있습니다.

![](assets/read-segment-audience3.png)
