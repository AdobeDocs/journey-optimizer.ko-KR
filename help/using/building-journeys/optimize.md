---
solution: Journey Optimizer
product: journey optimizer
title: 조건 활동
description: 조건 활동에 대해 알아보기
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: 활동, 조건, 캔버스, 여정, 최적화
badge: label="제한된 가용성" type="Informative"
hidefromtoc: true
hide: true
exl-id: f6618de4-7861-488e-90c0-f299ef5897ca
source-git-commit: 19130e9eb5a2144afccab9fa8e5632de67bc7157
workflow-type: tm+mt
source-wordcount: '1024'
ht-degree: 6%

---

# 활동 최적화 {#journey-path-optimization}

>[!CONTEXTUALHELP]
>id="ajo_journey_optimize"
>title="활동 최적화"
>abstract="**최적화** 활동을 통해 실험, 타기팅, 특정 조건 등의 구체적인 기준에 따라 여러 경로를 만들어 개인이 여정을 어떻게 진행할지 정의할 수 있습니다."

>[!AVAILABILITY]
>
>이 기능은 제한적으로 이용할 수 있습니다. 액세스 권한을 얻으려면 Adobe 담당자에게 문의하십시오.

**최적화** 활동을 사용하면 실험, 타기팅 및 특정 조건을 포함한 특정 기준에 따라 여러 **여정**&#x200B;을 만들어 개개인이 여정을 진행하는 방법을 정의할 수 있습니다. 이를 통해 참여도와 성공을 극대화하여 고도로 사용자 지정되고 효과적인 경로를 만들 수 있습니다.

**여정 경로**&#x200B;은(는) 다음 중 하나로 구성될 수 있습니다.

* 커뮤니케이션의 순서
* 그들 사이의 시간;
* 커뮤니케이션 수;
* 또는 이 세 변수의 임의 조합입니다.

예를 들어 한 경로에는 하나의 전자 메일이 포함될 수 있고, 다른 경로에는 두 개의 SMS 메시지가 포함될 수 있으며, 세 경로에는 전자 메일, 2시간의 [대기](wait-activity.md) 노드, SMS 메시지가 포함될 수 있습니다.

<!--With this feature, [!DNL Journey Optimizer] empowers you with the tools to deliver personalized and optimized paths to your audience, ensuring maximum engagement and success to create highly customized and effective journeys.-->

**최적화** 활동을 통해 다음을 수행할 수 있습니다.

* [경로 실험 실행](#experimentation)
* 각 여정 경로에서 [타깃팅](#targeting) 규칙 활용
* 경로에 [조건](#conditions) 적용

![](assets/journey-optimize.png)

여정이 라이브되면 정의된 기준에 따라 프로필이 평가되고 일치하는 기준에 따라 여정에서 적절한 경로로 전송됩니다.

## 실험 사용 {#experimentation}

실험을 통해 무작위 분할을 기반으로 서로 다른 경로를 테스트하여 사전 정의된 성공 지표를 기반으로 가장 뛰어난 성과를 결정할 수 있습니다.

여정에서 실험을 설정하려면 아래 단계를 따르십시오.

세 가지 경로를 비교한다고 가정해 보겠습니다.

* 하나의 이메일로 하나의 경로;
* 2일의 대기 노드와 이메일이 포함된 두 번째 경로
* 이메일과 SMS 메시지가 포함된 세 번째 경로입니다.

1. **[!UICONTROL 최적화]** 활동을 여정 캔버스에 놓습니다.

1. 보고 및 테스트 모드 로그에서 활동을 식별하는 선택적 레이블을 추가합니다.

1. **[!UICONTROL 메서드]** 드롭다운 목록에서 **[!UICONTROL 실험]**&#x200B;을(를) 선택합니다.

   ![](assets/journey-optimize-experiment.png){width=85%}

1. **[!UICONTROL 실험 설정]**&#x200B;을 클릭합니다.

1. 원하는 대로 실험을 디자인하고 구성합니다. [방법 알아보기](../content-management/content-experiment.md)

   <!--
    ![](../campaigns/assets/msg-optimization-create-experiment.png){width=85%}
    Replace with appropriate screenshot
    The experiment applies to all the activities in the journey.TBC
   -->

여정이 활성 상태가 되면 사용자가 임의로 할당되어 다른 경로를 통해 이동합니다. [!DNL Journey Optimizer]은(는) 더 많은 구매를 유도하고 실행 가능한 통찰력을 제공하는 경로를 추적합니다.

<!--Follow the success of your journey with the [Experimentation journey report](../reports/campaign-global-report-cja-experimentation.md). Is there a report specific to experimentation in journey?-->

### 실험에 대한 사용 사례 {#uc-experiment}

다음 예제에서는 **[!UICONTROL Experiment]** 메서드와 함께 **[!UICONTROL Optimize]** 활동을 사용하여 전체적으로 가장 잘 작동하는 경로를 확인하는 방법을 보여 줍니다.

**채널 효율성**

첫 번째 메시지를 이메일로 전송할지 SMS로 전송할지 여부를 테스트하면 전환율이 높아집니다.

* 전환율을 최적화 지표로 사용합니다(예: 구매, 등록).

![](assets/journey-optimize-experiment-uc.png)

**메시지 빈도**

1주일에 한 개의 이메일을 보낼 때와 3개의 이메일을 보낼 때 더 많은 구매가 발생하는지 확인하는 실험을 실행하십시오.

* 구매 또는 구독 취소 비율을 최적화 지표로 사용합니다.

**통신 간 대기 시간**

24시간 대기 및 후속 조치 이전의 72시간 대기 를 비교하여 어느 타이밍이 참여를 극대화하는지 확인합니다.

* 클릭스루 비율 또는 매출을 최적화 지표로 사용합니다.

## 타깃팅 활용 {#targeting}

타깃팅을 사용하면 고객이 특정 대상 세그먼트<!-- depending on profile attributes or contextual attributes-->를 기반으로 여정 경로 중 하나를 입력할 수 있도록 충족해야 하는 특정 규칙이나 자격을 결정할 수 있습니다.

주어진 경로를 임의로 할당하는 실험과 달리, 타깃팅은 올바른 대상 또는 프로필이 지정된 경로로 들어가도록 하는 관점에서 결정적입니다.

타깃팅을 사용할 경우 다음을 기반으로 특정 규칙을 정의할 수 있습니다.

* 위치(예: **사용자 프로필 특성** 지역 타겟팅), 연령 또는 환경 설정. 예를 들어, 미국의 사용자는 &quot;골든 게이트&quot; 프로모션을 보고 프랑스의 사용자는 &quot;에펠탑&quot; 프로모션을 봅니다.

* 디바이스 유형(예: **컨텍스트 데이터** 디바이스 타기팅), 시간 또는 세션 세부 정보. 예를 들어 데스크탑 사용자는 데스크탑에 최적화된 콘텐츠를 수신하는 반면, 모바일 사용자는 모바일에 최적화된 콘텐츠를 수신합니다.

* 특정 대상 멤버십이 있는 프로필을 포함하거나 제외하는 데 사용할 수 있는 **대상**.

여정에서 타깃팅을 설정하려면 아래 단계를 따르십시오.

1. **[!UICONTROL 최적화]** 활동을 여정 캔버스에 놓습니다.

1. 보고 및 테스트 모드 로그에서 활동을 식별하는 선택적 레이블을 추가합니다.

1. **[!UICONTROL 메서드]** 드롭다운 목록에서 **[!UICONTROL 타깃팅]**&#x200B;을(를) 선택합니다.

   ![](assets/journey-optimize-targeting.png){width=85%}

1. **[!UICONTROL 타깃팅 규칙 만들기]**&#x200B;를 클릭합니다.

1. 규칙 빌더를 사용하여 기준을 정의합니다. 예를 들어 미국 거주자를 위한 규칙, 프랑스 거주자를 위한 규칙, 인도 거주자를 위한 규칙을 정의합니다.

   ![](assets/journey-targeting-rule.png)

1. 필요에 따라 **[!UICONTROL 대체 콘텐츠 사용]**&#x200B;을 선택합니다. 대체 콘텐츠 를 사용하면 타깃팅 규칙이 적격하지 않을 때 대상자가 기본 콘텐츠를 받을 수 있습니다. 이 옵션을 선택하지 않으면 위에서 정의한 타겟팅 규칙에 적합하지 않은 대상은 대체 경로를 입력하지 않습니다.

1. 타깃팅 규칙 설정을 저장합니다.

1. 다시 여정으로 돌아가서 특정 작업을 놓아 각 경로를 사용자 지정합니다. 예를 들어 미국 거주자를 위한 특정 이메일, 프랑스 거주자를 위한 다른 이메일 등을 만들 수 있습니다.

   ![](assets/journey-targeting-paths.png)

1. 타겟팅 규칙 설정으로 정의된 각 그룹에 적절한 콘텐츠를 디자인할 수 있습니다. 서로 다른 경로 사이를 원활하게 탐색할 수 있습니다.

   ![](assets/journey-targeting-design.png)

   이 예에서는 미국 거주자를 위한 특정 경로, 프랑스 거주자를 위한 다른 경로, 인도 거주자를 위한 다른 경로를 설계한다.

여정이 라이브되면 미국 거주자가 특정 경로로 들어가고 프랑스 거주자가 다른 경로로 들어가도록 세그먼트별로 지정된 경로가 처리됩니다.

### 타깃팅에 대한 사용 사례 {#uc-targeting}

다음 예제에서는 **[!UICONTROL Targeting]** 메서드와 함께 **[!UICONTROL Optimize]** 활동을 사용하여 다양한 하위 대상에 대한 경로를 개인화하는 방법을 보여 줍니다.

**세그먼트별 채널**

골드 상태 충성도 멤버는 이메일을 통해 개인화된 오퍼를 받을 수 있으며 다른 모든 멤버는 SMS 미리 알림으로 이동됩니다.

* 프로필당 매출 또는 전환율을 최적화 지표로 사용합니다.

![](assets/journey-optimize-targeting-uc.png)

**동작 기반 타깃팅**

이메일을 열었지만 클릭하지 않은 고객은 푸시 알림을 받을 수 있으며 열지 않은 고객은 SMS를 받습니다.

* 클릭스루 비율 또는 다운스트림 전환을 최적화 지표로 사용합니다.

**구매 기록 타깃팅**

최근 구매한 고객은 짧은 &#39;땡큐+크로스셀&#39; 길로 갈 수 있고, 구매 이력이 없는 고객은 더 긴 육성 여정으로 접어든다.

* 반복 구매 비율 또는 참여 비율을 최적화 지표로 사용합니다.

## 조건 추가 {#conditions}

특정 기준에 따라 여러 경로를 만들어 개인이 여정을 진행하는 방식을 정의하는 조건을 추가할 수 있습니다. 또한 시간 초과나 오류를 처리하기 위한 대체 경로를 구성하여 원활한 환경을 보장할 수 있습니다.

![](assets/journey-condition.png)

[이 섹션](conditions.md)에서 조건을 정의하는 방법을 알아보세요.

다음 유형의 조건을 사용할 수 있습니다.

* [데이터 Source 조건](condition-activity.md#data_source_condition)
* [시간 조건](condition-activity.md#time_condition)
* [분할 비율](condition-activity.md#percentage_split)
* [날짜 조건](condition-activity.md#date_condition)
* [프로필 상한](condition-activity.md#profile_cap)
