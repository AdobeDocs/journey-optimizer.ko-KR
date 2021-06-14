---
title: 여정에서 세그먼트 사용
description: 여정에서 세그먼트를 사용하는 방법을 알아봅니다
feature: 여정
topic: 콘텐츠 관리
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '934'
ht-degree: 3%

---

# 여정 {#segment-trigger-activity}에서 세그먼트 사용

![](../assets/do-not-localize/badge.png)

## 세그먼트 읽기 활동 {#about-segment-trigger-actvitiy} 정보

세그먼트 읽기 활동을 사용하면 Adobe Experience Platform 세그먼트에 속하는 모든 개인이 여정을 입력하도록 할 수 있습니다. 여정의 시작은 한 번 또는 정기적으로 실행될 수 있습니다.

세그먼트 빌드](../segment/about-segments.md) 사용 사례에서 만든 &quot;Luma 앱 열기 및 체크아웃&quot; 세그먼트의 예를 예로 들어 보겠습니다. [ 세그먼트 읽기 활동을 사용하면 이 세그먼트에 속하는 모든 개인이 여정을 입력하고 모든 여정 기능을 활용하는 개인화된 여정으로 전환하도록 할 수 있습니다.조건, 타이머, 이벤트, 작업.

>[!NOTE]
>
>1시간이 짧은 시간대에 세그먼트 기반 여정을 트리거할 수 없습니다.

### 활동 구성 {#configuring-segment-trigger-activity}

세그먼트 읽기 활동을 구성하는 단계는 다음과 같습니다.

1. **[!UICONTROL Orchestration]** 카테고리를 펼치고 **[!UICONTROL Read Segment]** 활동을 캔버스에 놓습니다.

   활동을 여정의 첫 번째 단계로 배치해야 합니다.

1. 활동에 **[!UICONTROL Label]** 을 추가합니다(선택 사항).

1. **[!UICONTROL Segment]** 필드에서 여정을 입력할 Adobe Experience Platform 세그먼트를 선택한 다음 **[!UICONTROL Save]** 를 클릭합니다.

   목록에 표시된 열을 사용자 지정하고 정렬할 수 있습니다.

   >[!NOTE]
   >
   >**실현됨** 및 **기존** 세그먼트 기여도 상태가 있는 개인만 여정에 들어갑니다. 세그먼트를 평가하는 방법에 대한 자세한 내용은 [세분화 서비스 설명서](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=en#interpret-segment-results)를 참조하십시오.

   ![](../assets/read-segment-selection.png)

   세그먼트가 추가되면 **[!UICONTROL Copy]** 버튼을 사용하여 해당 이름과 ID를 복사할 수 있습니다.

   `{"name":"Luma app opening and checkout",”id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![](../assets/read-segment-copy.png)

1. **[!UICONTROL Namespace]** 필드에서 개인을 식별하는 데 사용할 네임스페이스를 선택합니다. [네임스페이스에 대해 자세히 알아보십시오](../event/about-creating.md#select-the-namespace).

   >[!NOTE]
   >
   >다른 ID 중 선택한 ID(네임스페이스)가 없는 세그먼트에 속하는 개인은 여정에 들어갈 수 없습니다.

1. **[!UICONTROL Read Segment]** 활동을 사용하면 세그먼트가 여정에 들어갈 시간을 지정할 수 있습니다. 이렇게 하려면 **[!UICONTROL Edit journey schedule]** 링크를 클릭하여 여정의 속성에 액세스한 다음 **[!UICONTROL Scheduler type]** 필드를 구성합니다.

   ![](../assets/read-segment-schedule.png)

   기본적으로 세그먼트는 여정 **[!UICONTROL As soon as possible]** 을 입력합니다. 이는 여정이 게시되고 1시간이 지난 후에 의미합니다. 세그먼트를 특정 날짜/시간 또는 반복으로 여정을 입력하도록 하려면 목록에서 원하는 값을 선택합니다.

   >[!NOTE]
   >
   >**[!UICONTROL Schedule]** 섹션은 **[!UICONTROL Read Segment]** 활동이 캔버스에 드롭된 경우에만 사용할 수 있습니다.

   ![](../assets/read-segment-schedule-list.png)

### 여정 테스트 및 게시 {#testing-publishing}

**[!UICONTROL Read Segment]** 활동을 사용하면 단일 여정에서 또는 세그먼트에 대해 자격이 있는 프로필 중에서 선택한 100개의 임의로 테스트 프로필을 테스트할 수 있습니다.

이렇게 하려면 테스트 모드를 활성화한 다음 왼쪽 창에서 원하는 옵션을 선택합니다.

![](../assets/read-segment-test-mode.png)

그런 다음 평소대로 테스트 모드를 구성하고 실행할 수 있습니다. [여정 ](testing-the-journey.md)를 테스트하는 방법을 알아봅니다.

테스트가 실행되면 **[!UICONTROL Show logs]** 버튼을 사용하여 선택한 테스트 옵션에 따라 테스트 결과를 볼 수 있습니다.

* **[!UICONTROL Single profile at a time]**:테스트 로그는 단일 테스트 모드를 사용할 때와 동일한 정보를 표시합니다. 이 작업에 대한 자세한 정보는 [이 섹션](testing-the-journey.md#viewing_logs)을 참조하십시오

* **[!UICONTROL Up to 100 profiles at once]**:테스트 로그를 사용하여 Adobe Experience Platform에서 세그먼트 내보내기의 진행 상황과 여정에 입력한 모든 사람의 개별 진행 상태를 추적할 수 있습니다.

   한 번에 최대 100개의 프로필을 사용하여 여정을 테스트해도 시각적 흐름을 사용하여 여정에서 개인의 진행 상황을 추적할 수 없습니다.

   ![](../assets/read-segment-log.png)

테스트가 성공하면 여정을 게시할 수 있습니다( [여정 게시](publishing-the-journey.md) 참조). 세그먼트에 속하는 개인은 여정의 속성 **[!UICONTROL Scheduler]** 섹션에 지정된 날짜/시간에 여정을 입력합니다.

>[!NOTE]
>
>되풀이가 아닌 세그먼트 기반 여정(&quot;가능한 한 빨리 시작&quot; 또는 &quot;한 번&quot;)가 실행되면 해당 상태가 자동으로 &quot;닫힌&quot;으로 변경됩니다.
>
>되풀이하는 세그먼트 기반 여정의 경우, 마지막 여정이 실행되면가 자동으로 닫힙니다. 종료 날짜/시간을 지정하지 않은 경우 수동으로 여정을 닫아야 새 출입구가 종료됩니다.


## 세그먼트 기반 여정의 대상 타깃팅

세그먼트 기반 여정은 항상 **세그먼트 읽기** 활동으로 시작하여 Adobe Experience Platform 세그먼트에 속하는 개인을 검색합니다.

세그먼트에 속하는 대상자는 한 번 또는 정기적으로 검색됩니다.

여정을 입력한 후 대상 오케스트레이션 사용 사례를 만들어 초기 세그먼트의 개인을 여정의 다른 분기로 유입시킬 수 있습니다.

**세그먼테이션**

조건을 사용하여 **조건** 활동을 사용하여 세그먼테이션을 수행할 수 있습니다. 예를 들어 VIP 사람이 특정 경로를 사용하고 VIP이 아닌 다른 경로를 취하도록 할 수 있습니다.

세그먼테이션은 다음을 기반으로 할 수 있습니다.

* 데이터 소스 데이터
* 여정 데이터의 이벤트 컨텍스트(예:한 시간 전에 받은 메시지를 누군가 클릭했습니까?
* 예: 날짜:6월에 여정이 있을 때?
* 시간(예:그 사람 시간대 아침 맞나요?
* 백분율을 기반으로 여정에 흐르는 대상을 분할하는 알고리즘. 예:컨트롤 그룹을 제외하려면 90% - 10%

![](../assets/read-segment-audience1.png)

**예외**

세그먼테이션에 사용되는 것과 동일한 **Condition** 활동을 사용하면 모집단의 일부를 제외할 수도 있습니다. 예를 들어, VIP 대상자를 바로 뒤에 종료 단계가 있는 분기로 유입시켜 제외할 수 있습니다.

이 제외는 세그먼트 검색 직후, 모집단 계산 목적 또는 여러 단계 여정을 위해 발생할 수 있습니다.

![](../assets/read-segment-audience2.png)

**합집합**

여정을 사용하면 N개의 분기를 만들고 세그멘테이션 후 함께 결합할 수 있습니다.

따라서 두 대상을 공통 경험으로 되돌아가게 할 수 있습니다.

예를 들어 여정에서 10일 동안 다른 경험을 수행한 후 VIP과 VIP 이외의 고객은 동일한 경로로 돌아갈 수 있습니다.

결합 후에는 세그먼테이션 또는 제외를 수행하여 대상을 다시 분할할 수 있습니다.

![](../assets/read-segment-audience3.png)
