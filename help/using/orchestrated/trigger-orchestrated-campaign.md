---
solution: Journey Optimizer
product: journey optimizer
title: 신호를 사용하여 오케스트레이션된 캠페인 트리거
description: ' [!DNL Adobe Journey Optimizer]의 신호를 사용하여 오케스트레이션된 캠페인을 트리거하는 방법을 알아봅니다.'
feature: Campaigns
topic: Content Management
role: Developer
level: Intermediate
version: Campaign Orchestration
source-git-commit: c9a5c29c685cf21fda2b5df1a3838713e054f696
workflow-type: tm+mt
source-wordcount: '814'
ht-degree: 0%

---


# 신호를 사용하여 오케스트레이션된 캠페인 트리거 {#trigger-signal}

오케스트레이션된 캠페인을 일정에 따라 실행하는 대신 신호를 전송하여 트리거할 수 있습니다. 신호는 외부 시스템 또는 애플리케이션에서 API 호출을 통해 전송됩니다. 신호를 사용할 때 매개 변수를 전달할 수 있습니다. 그런 다음 오케스트레이션된 캠페인에서 타겟팅, 조건 또는 표현식에 사용할 수 있도록 실행 컨텍스트의 이벤트 변수로 사용할 수 있습니다.

신호를 사용하여 오케스트레이션된 캠페인을 트리거하는 엔드투엔드 프로세스:

1. [신호에 의해 트리거될 캠페인 예약](#set-an-orchestrated-campaign-to-wait-for-a-signal-configure-signal)
1. [신호 페이로드에 대한 매개 변수 추가](#add-parameters-for-the-signal-payload-optional-parameters)(선택 사항)
1. [캠페인 빌드 및 테스트](#build-and-test-the-campaign-build-and-test)
1. [캠페인 게시 및 트리거](#publish-and-trigger-the-campaign-publish)

## 신호에 의해 트리거될 캠페인 예약 {#configure-signal}

일정 대신 신호에서 시작하도록 오케스트레이션된 캠페인을 설정하려면 다음 단계를 수행합니다.

1. 신호를 사용하여 트리거할 오케스트레이션된 캠페인을 엽니다.

1. 예약 구성을 엽니다. [오케스트레이션된 캠페인을 예약하는 방법을 알아보세요](create-orchestrated-campaign.md#schedule).

1. 캠페인이 일정에 따라 실행되지 않고 신호를 대기하도록 **[!UICONTROL 신호에 의해 트리거됨]**&#x200B;을(를) 선택하십시오.

   ![신호 옵션으로 트리거된 예약 메뉴](assets/triggered-oc-scheduler.png){zoomable="yes"}

## 신호 페이로드에 대한 매개 변수 추가(선택 사항) {#parameters}

트리거 신호에서 매개 변수를 전달하고 실행 컨텍스트(예: 타깃팅, 조건 또는 표현식)의 캠페인에서 사용할 수 있습니다. 먼저 예약 설정에서 각 매개 변수를 정의한 다음, 트리거 API를 호출할 때 해당 값을 전달합니다.

1. 캠페인 일정을 열고 **[!UICONTROL 매개 변수 추가]**&#x200B;를 선택합니다.

1. 신호 페이로드에서 전송할 각 매개 변수의 이름과 데이터 형식을 정의합니다. 테스트 모드에서 캠페인을 트리거할 때 사용할 **테스트 값**&#x200B;을 제공할 수도 있습니다. [트리거된 캠페인을 테스트하는 방법을 알아봅니다](#build-and-test).

   ![매개 변수를 추가하여 신호의 페이로드 매개 변수를 정의합니다](assets/triggered-oc-parameter.png){zoomable="yes"}

>[!NOTE]
>
>스케줄러에 정의되지 않은 API 호출에서 매개 변수를 전달하면 API 호출이 계속 성공하고 매개 변수가 전파되므로 표현식에 사용할 수 있습니다. 하지만 오케스트레이션된 캠페인 인터페이스는 이 인터페이스를 사용하는 데 도움이 되지 않습니다. 예를 들어 테스트 활동에서는 스케줄러에 정의되지 않은 매개 변수를 나열하거나 표시하지 않습니다.

## 캠페인 빌드 및 테스트 {#build-and-test}

캔버스에서 캠페인을 빌드한 다음 선택적으로 게시하기 전에 API를 통해 신호를 트리거하여 초안에서 테스트합니다.

1. 캔버스에서 활동(대상, 타기팅, 게재)을 추가하고 연결합니다. [캠페인 활동을 조율하는 방법 알아보기](orchestrate-activities.md)

1. 신호에서 매개 변수를 정의한 경우 이를 캔버스 논리(예: 조건 또는 타깃팅)에 연결할 수 있습니다. 이 예제에서는 &quot;channel&quot; 매개 변수가 **[!UICONTROL Test]** 활동의 조건으로 사용됩니다.

   ![테스트 활동에서 조건으로 사용되는 채널 매개 변수](assets/triggered-oc-use-parameters.png)

   표현식 편집기에서 신호 매개 변수를 사용하려면(예: **[!UICONTROL 대상 작성]** 활동에서 쿼리를 작성하려면) 표현식 필드에 `$(vars/@<parameterName>)`을(를) 입력하십시오. `<parameterName>`을(를) 스케줄러에 정의된 매개 변수 이름(예: `$(vars/@channel)`)으로 바꾸십시오. [식 편집기로 작업하는 방법을 알아봅니다](edit-expressions.md).

1. 캠페인 스케줄러를 열고 **[!UICONTROL API 요청 복사]**&#x200B;를 선택하고 형식(cURL 또는 HTTP 요청)을 선택합니다.

   복사된 정보에는 오케스트레이션된 캠페인 ID, 샌드박스 이름, 조직 ID 및 일부를 추가한 경우 매개변수에 대한 테스트 값이 포함됩니다.

   ![예약 구성의 API 요청 옵션 복사](assets/triggered-oc-copy.png)

   +++매개 변수 및 테스트 값이 있는 샘플 cURL 요청

   ```bash
   POST https://platform.adobe.io/ajo/campaign-orchestration/orchestratedCampaigns/1c7529c7-7a8c-491a-a2c6-3d8131d2e17d/trigger
   
   Headers:
   Authorization: Bearer ## Access token ##
   Content-Type: application/json
   x-api-key: ## Provide API Key here ##
   x-api-version: 1
   x-gw-ims-org-id: 123456ABCDEFG@LumaOrg
   x-sandbox-name: prod
   
   Body:
   {
   "variables": {
      "channel": "sms"
   }
   }
   ```

   +++

1. 캠페인을 시작하려면 **[!UICONTROL 시작]**&#x200B;을 클릭하세요.

1. 스케줄러에서 복사한 샘플 요청을 사용하여 트리거 API 호출을 보냅니다. <!--For the complete API reference, refer to the [Journey Optimizer API documentation](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"}.-->

테스트 결과가 만족스러우면 [캠페인을 게시](#publish)하십시오.

## 캠페인 게시 및 트리거 {#publish}

[캠페인을 빌드하고 테스트한 후](#build-and-test) 응용 프로그램에서 트리거할 수 있도록 캠페인을 게시합니다.

1. 캠페인 캔버스에서 **[!UICONTROL 게시]**&#x200B;를 클릭합니다. 외부 시스템에서 캠페인을 트리거하려면 먼저 캠페인을 게시해야 합니다. [캠페인 시작 및 모니터링에 대해 자세히 알아보세요](start-monitor-campaigns.md#publish).

1. 캠페인 스케줄러를 열고 **[!UICONTROL API 요청 복사]**&#x200B;를 선택하고 형식(cURL 또는 HTTP 요청)을 선택합니다.

   복사된 정보에는 오케스트레이션된 캠페인 ID, 샌드박스 이름, 조직 ID 및 일부를 추가한 경우 매개 변수가 포함됩니다.

   ![예약 구성에서 API 요청 복사](assets/triggered-oc-copy.png)

1. 시스템에서 트리거 API를 호출합니다.

   >[!IMPORTANT]
   >
   >실시간 오케스트레이션된 캠페인의 경우 스로틀 가드레일은 두 API 트리거 실행 사이에 **최소 1시간 간격**&#x200B;을 적용합니다. 해당 간격이 경과하기 전에 API를 다시 호출하는 경우 API가 **HTTP 429** 오류를 반환합니다(요청이 너무 많음). 이 가드레일은 초안 버전을 테스트하도록 트리거할 때 적용되지 않습니다.

   신호 페이로드에 매개 변수를 추가한 경우 API 호출에 전달하는 값은 캠페인이 실행될 때 캠페인 이벤트 변수로 노출됩니다. 이를 검사하려면 캠페인 캔버스 도구 모음에서 캠페인 로그를 엽니다. **[!UICONTROL 작업]** 탭에서 신호에 해당하는 작업을 식별하고 연필 아이콘을 클릭하여 관련 이벤트 변수에 액세스합니다. [로그 및 작업에 액세스하는 방법을 알아봅니다](start-monitor-campaigns.md#logs-tasks).

   ![캠페인 이벤트 변수를 사용할 수 있는 로그 및 작업 화면](assets/trigger-events-variables.png){zoomable="yes"}
