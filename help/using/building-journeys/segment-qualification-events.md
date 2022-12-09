---
solution: Journey Optimizer
product: journey optimizer
title: 세그먼트 자격 이벤트
description: 세그먼트 자격 이벤트에 대해 알아보기
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 7e70b8a9-7fac-4450-ad9c-597fe0496df9
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '834'
ht-degree: 0%

---

# 세그먼트 자격 이벤트 {#segment-qualification}

## 세그먼트 자격 이벤트 정보{#about-segment-qualification}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_segment_qualification"
>title="세그먼트 자격 이벤트"
>abstract="이 활동을 사용하면 Adobe Experience Platform 세그먼트의 프로필의 처음과 끝에서 의견을 수렴하여 개인 사용자가 여정에 들어오거나 이동할 수 있습니다."

이 활동을 사용하면 Adobe Experience Platform 세그먼트의 프로필의 처음과 끝에서 의견을 수렴하여 개인 사용자가 여정에 들어오거나 이동할 수 있습니다. 세그먼트 만들기에 대한 자세한 내용은 다음을 참조하십시오 [섹션](../segment/about-segments.md).

&quot;실버 고객&quot; 세그먼트가 있다고 가정해 보겠습니다. 이 활동을 사용하면 모든 신규 실버 고객을 고객 여정에 참여시켜 일련의 개인화된 메시지를 보낼 수 있습니다.

이 유형의 이벤트는 여정의 첫 번째 단계 또는 그 나중에 배치할 수 있습니다.

>[!IMPORTANT]
>
>Adobe Experience Platform 세그먼트는 하루에 한 번 계산됩니다(**배치** 세그먼트) 또는 실시간(**스트리밍** 세그먼트(Adobe Experience Platform의 빈도가 높은 대상 옵션 사용)
>
>선택한 세그먼트가 스트리밍되는 경우 이 세그먼트에 속하는 개인이 잠재적으로 실시간으로 여정에 들어갈 수 있습니다. 세그먼트가 배치인 경우, 이 세그먼트에 대해 새로 자격이 되는 사람은 Adobe Experience Platform에서 세그먼트 계산을 실행할 때 여정을 시작할 수 있습니다.
>
>경험 이벤트 필드 그룹은 읽기 세그먼트, 세그먼트 자격 또는 비즈니스 이벤트 활동으로 시작하는 여정에서 사용할 수 없습니다.


1. 을(를) 펼칩니다. **[!UICONTROL Events]** 카테고리 및 삭제 **[!UICONTROL Segment Qualification]** 활동을 캔버스로 이동합니다.

   ![](assets/segment5.png)

1. 추가 **[!UICONTROL Label]** 추적했습니다. 이 단계는 선택 사항입니다.

1. 을(를) 클릭합니다. **[!UICONTROL Segment]** 필드를 선택하고 활용할 세그먼트를 선택합니다.

   >[!NOTE]
   >
   >목록에 표시된 열을 사용자 지정하고 정렬할 수 있습니다.

   ![](assets/segment6.png)

   세그먼트를 추가하면 **[!UICONTROL Copy]** 버튼을 사용하면 이름과 ID를 복사할 수 있습니다.

   `{"name":"Loyalty membership“,”id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![](assets/segment-copy.png)

1. 에서 **[!UICONTROL Behaviour]** 필드, 세그먼트 출입구, 종료 또는 둘 다 수신 여부를 선택합니다.

   >[!NOTE]
   >
   >참고 사항 **[!UICONTROL Enter]** 및 **[!UICONTROL Exit]** 에 해당합니다 **실현** 및 **종료됨** adobe Experience Platform의 세그먼트 기여도 상태. 세그먼트 평가 방법에 대한 자세한 내용은 [Segmentation Service 설명서](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results){target=&quot;_blank&quot;}.

1. 네임스페이스를 선택합니다. 이벤트가 여정의 첫 번째 단계로 배치된 경우에만 필요합니다.

   ![](assets/segment7.png)

페이로드에는 조건 및 작업에서 사용할 수 있는 다음 컨텍스트 정보가 포함되어 있습니다.

* 동작(시작, 종료)
* 자격 타임스탬프
* 세그먼트 id

다음 조건 또는 작업에서 표현식 편집기를 사용할 때 **[!UICONTROL Segment Qualification]** 활동, 액세스 권한 **[!UICONTROL SegmentQualification]** 노드 아래에 있어야 합니다. 다음 중 하나를 선택할 수 있습니다 **[!UICONTROL Last qualification time]** 그리고 **[!UICONTROL status]** (시작 또는 종료).

자세한 내용은 [조건 활동](../building-journeys/condition-activity.md#about_condition).

![](assets/segment8.png)

세그먼트 자격 이벤트를 포함하는 새 여정은 게시한 후 10분 후에 작동합니다. 이 시간 간격은 전용 서비스의 캐시 새로 고침 간격에 해당합니다. 따라서 이 여정을 사용하기 전에 10분을 기다려야 합니다.

## 우수 사례 {#best-practices-segments}

다음 **[!UICONTROL Segment Qualification]** 활동을 통해 Adobe Experience Platform 세그먼트에서 자격을 얻거나 자격을 갖추지 못한 개인 여정 즉시 입장할 수 있습니다.

이 정보의 수신 속도가 빠르다. 측정된 횟수는 초당 수신된 10,000개의 이벤트 속도를 보여줍니다. 그 결과, 여러분은 얼마나 많은 정점이 발생할 수 있는지, 어떻게 그것을 피할 수 있는지 그리고 어떻게 그들을 위해 여러분의 여정을 준비시킬 수 있는지 이해하도록 해야 합니다.

### 배치 세그먼트{#batch-speed-segment-qualification}

배치 세그먼트에 세그먼트 자격을 사용할 때는 일별 계산 시 최대 시작 시간이 발생합니다. 피크 크기는 매일 세그먼트를 시작(또는 종료)하는 개인 수에 따라 달라집니다.

또한 배치 세그먼트가 새로 만들어지고 여정에서 바로 사용되는 경우 첫 번째 계산 일괄 처리가 여정에 매우 많은 개인이 들어갈 수 있습니다.

### 스트리밍된 세그먼트{#streamed-speed-segment-qualification}

스트리밍되는 세그먼트에 세그먼트 자격을 사용할 때는 세그먼트에 대한 지속적인 평가로 인해 출입구의 최대 수를 확보할 위험이 줄어듭니다. 여전히, 세그먼트 정의로 인해 많은 수의 고객이 동시에 자격을 얻는 경우 피크도 있을 수 있습니다.

스트리밍 세그멘테이션에 대한 자세한 내용은 [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/segmentation/api/streaming-segmentation.html#api)

### 오버로드를 방지하는 방법{#overloads-speed-segment-qualification}

다음은 여정에서 활용하는 시스템(데이터 소스, 사용자 지정 작업, 채널 작업 활동)을 오버로드하는 것을 방지하는 데 도움이 되는 몇 가지 모범 사례입니다.

에서 를 사용하지 않음 **[!UICONTROL Segment Qualification]** 활동, 배치 세그먼트가 생성된 직후 첫 번째 계산 최고점을 피합니다. 계산되지 않은 세그먼트를 사용하려는 경우 여정 캔버스에 노란색 경고가 표시됩니다.

![](assets/segment-error.png)

여정에 사용되는 데이터 소스 및 작업에 대해 최대 가용량 규칙을 설정하여 오버로드를 방지합니다. 추가 정보 [Journey Orchestration 설명서](https://experienceleague.adobe.com/docs/journeys/using/working-with-apis/capping.html){target=&quot;_blank&quot;}. 최대 가용량 규칙은 다시 시도되지 않습니다. 다시 시도해야 하는 경우 상자를 선택하여 여정에서 대체 경로를 사용해야 합니다 **[!UICONTROL Add an alternative path in case of a timeout or an error]** 를 클릭하거나 탭합니다.

프로덕션 여정에서 세그먼트를 사용하기 전에 항상 먼저 매일 이 세그먼트에 대해 자격을 부여받은 개인의 볼륨을 평가하십시오. 이를 위해 다음을 확인할 수 있습니다 **[!UICONTROL Segments]** 메뉴를 열고 세그먼트를 열고 **[!UICONTROL Profiles over time]** 그래프.

![](assets/segment-overload.png)
