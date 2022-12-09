---
solution: Journey Optimizer
product: journey optimizer
title: 첫 번째 여정 만들기
description: Adobe Journey Optimizer를 사용하여 첫 번째 여정을 구축하는 주요 단계
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: d940191e-8f37-4956-8482-d2df0c4274aa
source-git-commit: 978751263ba2ed21e35e41e767f1e31ddbe59d53
workflow-type: tm+mt
source-wordcount: '1004'
ht-degree: 0%

---

# 첫 번째 여정 만들기{#jo-quick-start}

## 전제 조건{#start-prerequisites}

여정으로 메시지를 전송하려면 다음 구성이 필요합니다.

1. **이벤트 구성**: 이벤트가 수신될 때까지 여정을 트리거하려면 이벤트를 구성해야 합니다. 필요한 정보와 정보를 처리하는 방법을 정의합니다. 이 단계는 **기술 사용자**. [자세한 내용](../event/about-events.md).

   ![](assets/jo-event7bis.png)

1. **세그먼트 만들기**: 여정은 Adobe Experience Platform 세그먼트를 수신하여 메시지를 지정된 프로필 세트에 일괄 전송할 수도 있습니다. 이를 위해 세그먼트를 만들어야 합니다. [자세한 내용](../segment/about-segments.md).

   ![](assets/segment2.png)

1. **데이터 소스 구성**: 여정에서 사용할 조건 등의 추가 정보를 검색하는 시스템에 대한 연결을 정의할 수 있습니다. 기본 제공 Adobe Experience Platform 데이터 소스도 프로비저닝 시에 구성됩니다. 여정 내 이벤트의 데이터만 활용하는 경우에는 이 단계를 수행할 필요가 없습니다. 이 단계는 **기술 사용자**. [자세한 내용](../datasource/about-data-sources.md)

   ![](assets/jo-datasource.png)

1. **작업 구성**: 서드파티 시스템을 사용하여 메시지를 전송하는 경우 사용자 지정 작업을 만들 수 있습니다. 자세한 내용 [섹션](../action/action.md). 이 단계는 **기술 사용자**. Journey Optimizer 기본 제공 메시지 기능을 사용하는 경우 경로에 채널 작업을 추가하고 컨텐츠를 디자인하기만 하면 됩니다.

   ![](assets/custom2.png)

## 여정 구축{#jo-build}

>[!CONTEXTUALHELP]
>id="ajo_journey_create"
>title="여정 구축"
>abstract="이 화면에는 기존 여정 목록이 표시됩니다. 여정을 열거나 &#39;여정 만들기&#39;를 클릭하고 다른 이벤트, 오케스트레이션 및 작업 활동을 결합하여 여러 단계로 구성된 크로스 채널 시나리오를 작성할 수 있습니다."

이 단계는 **비즈니스 사용자**. 여기에서 여정을 만들 수 있습니다. 다양한 이벤트, 오케스트레이션 및 작업 활동을 조합하여 여러 단계로 구성된 크로스 채널 시나리오를 작성할 수 있습니다.

여정을 통해 메시지를 보내는 주요 단계는 다음과 같습니다.

1. 여정 관리 메뉴 섹션에서 **[!UICONTROL Journeys]**. 여정 목록이 표시됩니다.

   ![](assets/interface-journeys.png)

1. 클릭 **[!UICONTROL Create Journey]** 새 여정을 만들 수 있습니다.

1. 오른쪽에 표시되는 구성 창에서 여정의 속성을 편집합니다. 자세한 내용 [섹션](journey-gs.md#change-properties).

   ![](assets/jo-properties.png)

1. 먼저 이벤트 또는 **세그먼트 읽기** 활동을 팔레트에서 캔버스로 가져옵니다. 여정 디자인에 대한 자세한 내용은 [이 섹션](using-the-journey-designer.md).

   ![](assets/read-segment.png)

1. 개인이 수행할 다음 단계를 끌어서 놓습니다. 예를 들어 조건 뒤에 채널 작업을 추가할 수 있습니다. 활동에 대한 자세한 내용은 [이 섹션](using-the-journey-designer.md).

1. 테스트 프로필을 사용하여 여정을 테스트합니다. 자세한 내용 [섹션](testing-the-journey.md)

1. 여정을 게시하여 활성화하십시오. 자세한 내용 [섹션](publishing-the-journey.md).

   ![](assets/jo-journeyuc2_32bis.png)

1. 전용 보고 도구를 사용하여 여정의 효율성을 모니터링합니다. 자세한 내용 [섹션](../reports/live-report.md).

   ![](assets/jo-dynamic_report_journey_12.png)

## 여정 속성 정의 {#change-properties}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties"
>title="여정 속성"
>abstract="이 섹션에서는 여정 속성을 보여줍니다. 기본적으로 읽기 전용 매개 변수는 숨겨집니다. 사용 가능한 설정은 여정의 상태, 권한 및 제품 구성에 따라 다릅니다."

오른쪽 상단에 있는 연필 아이콘을 클릭하여 여정의 속성에 액세스합니다.

여정의 이름을 변경하고, 설명을 추가하고, 다시 시작하고, 시작 날짜와 종료 날짜를 선택하고, 관리자로서 을(를) 정의할 수 있습니다 **[!UICONTROL Timeout and error]** 지속 시간.

라이브 여정의 경우 이 화면에는 게시 날짜와 여정을 게시한 사용자의 이름이 표시됩니다.

다음 **기술 세부 정보 복사** 지원 팀이 문제를 해결하는 데 사용할 수 있는 여정에 대한 기술 정보를 복사할 수 있습니다. 다음 정보가 복사됩니다. JourneyVersion UID, OrgID, orgName, sandboxName, lastDeployedBy, lastDeployedAt.

![](assets/journey32.png)

### 입구{#entrance}

기본적으로 새 여정은 재진입을 허용합니다. 예를 들어, 한 사람이 상점에 들어올 때 일회성 선물을 제공하려는 경우, &quot;일회성&quot; 여정에 대한 옵션을 선택 취소할 수 있습니다.

프로필 시작 관리에 대한 자세한 내용은 [이 섹션](entry-management.md).

### 여정 활동의 시간 초과 및 오류 {#timeout_and_error}

작업 또는 조건 활동을 편집할 때 오류 또는 시간 제한 시 대체 경로를 정의할 수 있습니다. 서드파티 시스템을 심문하는 활동이 여정의 속성에 정의된 시간 초과 기간을 초과하는 경우(**[!UICONTROL Timeout and  error]** 필드), 잠재적인 대체 작업을 수행하도록 두 번째 경로가 선택됩니다.

허용된 값은 1초에서 30초 사이입니다.

매우 짧은 을 정의하는 것이 좋습니다 **[!UICONTROL Timeout and error]** 여정이 시간에 민감한 경우 값(예: 몇 초 이상 작업을 지연할 수 없으므로 여기에 응답합니다. 여정에 시간이 덜 걸리는 경우 더 긴 값을 사용하여 유효한 응답을 보내기 위해 라는 시스템에 더 많은 시간을 줄 수 있습니다.

여정은 글로벌 시간 초과도 사용합니다. 자세한 내용은 [다음 섹션](#global_timeout).

### 글로벌 여정 시간 초과 {#global_timeout}

추가 [timeout](#timeout_and_error) 여정 활동에는 인터페이스에 표시되지 않고 변경할 수 없는 글로벌 여정 시간 초과도 있습니다. 이 시간 제한은 개인 사용자가 참여한 후 30일 후에 여정에 있는 개인의 진행 상태를 중지합니다. 즉, 개인의 여정은 30일 이상 지속될 수 없습니다. 30일 시간 제한 기간 후 개인의 데이터가 삭제됩니다. 시간 제한 기간이 끝날 때 여전히 여정에 흐르는 개인은 중지되며 보고에서 오류로 간주됩니다.

>[!NOTE]
>
>여정은 개인 정보 보호 옵트아웃, 액세스 또는 삭제 요청에 직접 응답하지 않습니다. 그러나 글로벌 시간 제한은 개인이 30일 이상 여정에 머무르지 않도록 합니다.

30일 여정 시간 초과로 인해 여정 재입력이 허용되지 않는 경우 30일 이상 재수신 차단 기능을 사용할 수 없습니다. 실제로 입국한 지 30일이 지난 뒤 입국자의 모든 정보를 가리기 때문에 30일이 넘는 전에 입국한 사람을 알 수 없다.

### 표준 시간대 및 프로필 시간대 {#timezone}

시간대는 여정 수준에서 정의됩니다.

고정 시간대를 입력하거나 Adobe Experience Platform 프로필을 사용하여 여정 시간대를 정의할 수 있습니다.

시간대가 Adobe Experience Platform 프로필에 정의된 경우 여정에서 검색할 수 있습니다.

시간대 관리에 대한 자세한 내용은 [이 페이지](../building-journeys/timezone-management.md).

### 액세스 관리 {#access}

사용자 지정 또는 핵심 데이터 사용 레이블을 여정에 할당하려면 **[!UICONTROL Manage access]** 버튼을 클릭합니다. [개체 수준 액세스 제어(OLA)에 대한 자세한 정보](../administration/object-based-access.md)

![](assets/journeys-manage-access.png)
