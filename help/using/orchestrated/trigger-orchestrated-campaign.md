---
solution: Journey Optimizer
product: journey optimizer
title: 신호를 사용하여 오케스트레이션된 캠페인 트리거
description: REST API 또는 다른 캠페인의 종료 활동에서 신호로 오케스트레이션된 캠페인을 트리거하는 방법과 매개 변수를 캠페인에 전달하는 방법을 알아봅니다.
feature: Campaigns
topic: Content Management
role: Developer
level: Intermediate
version: Campaign Orchestration
exl-id: d1fd072d-b143-4752-822f-23f98684ba80
feature_v2: id: b423a773-0a58-4a77-b65d-3dd4ae6ef841
subfeature_v2: id: b5e335a9-0e5f-4dda-8845-c4ac5dca2be4
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 1429
ht-degree: 0%

---

# 신호를 사용하여 오케스트레이션된 캠페인 트리거 {#trigger-signal}

고정된 일정 대신 신호로 오케스트레이션된 캠페인을 시작할 수 있습니다. 캠페인이 신호를 받으면 실행되며 페이로드에 매개 변수를 전달할 수 있습니다. 타겟팅, 조건 또는 표현식에 변수로 사용할 수 있습니다.

신호는 다음 중 하나에서 올 수 있습니다.

* REST API — 응용 프로그램 또는 통합에서 트리거 끝점을 호출합니다([캠페인 게시 및 트리거](#publish) 및 [API 참조](https://developer.adobe.com/journey-optimizer-apis/references/oc-trigger){target="_blank"} 참조).
* 다른 오케스트레이션된 캠페인 — 업스트림 캠페인의 **[!UICONTROL End]** 활동은 분기가 완료될 때 동일한 종류의 신호를 보냅니다. [종료 활동을 구성하는 방법을 알아봅니다](#signal-end).

이 페이지에서는 신호(일정, 매개 변수, 테스트, 게시)를 수신하는 캠페인을 설정하는 방법과 API 또는 **[!UICONTROL 종료]** 활동에서 실행하는 방법에 대해 설명합니다. 변수를 사용할 수 있게 되면 규칙 및 **[!UICONTROL 테스트]** 조건에 변수를 사용하는 방법에 대한 자세한 내용은 [오케스트레이션된 캠페인에서 변수 사용](variables-orchestrated-campaigns.md)을 참조하세요.

트리거 끝점(경로, 헤더, 본문, 응답 및 오류)에 대한 전체 REST 사양은 Adobe Journey Optimizer API 설명서의 [오케스트레이션된 캠페인 API 트리거](https://developer.adobe.com/journey-optimizer-apis/references/oc-trigger){target="_blank"}를 참조하십시오.

신호를 사용하여 오케스트레이션된 캠페인을 트리거하는 엔드투엔드 프로세스:

1. [신호에 의해 트리거될 캠페인 예약](#configure-signal)
1. [신호 페이로드에 대한 매개 변수 추가](#parameters)(선택 사항)
1. [캠페인 빌드 및 테스트](#build-and-test)
1. [캠페인 게시 및 트리거](#publish)

>[!NOTE]
>
>신호를 사용하여 오케스트레이션된 캠페인을 트리거하려면 **[!DNL Publish orchestrated campaigns]** 권한(`orchestrated-campaign.publish`)이 필요합니다. [기본 제공 권한](../administration/ootb-permissions.md)을 참조하세요.

## 신호에 의해 트리거될 캠페인 예약 {#configure-signal}

일정 대신 신호에서 시작하도록 오케스트레이션된 캠페인을 설정하려면 다음 단계를 수행합니다.

1. 신호를 사용하여 트리거할 오케스트레이션된 캠페인을 엽니다.

1. 예약 구성을 엽니다. [오케스트레이션된 캠페인을 예약하는 방법을 알아보세요](create-orchestrated-campaign.md#schedule).

1. 캠페인이 일정에 따라 실행되지 않고 신호를 대기하도록 **[!UICONTROL 신호에 의해 트리거됨]**&#x200B;을(를) 선택하십시오.

   ![신호 옵션으로 트리거된 예약 메뉴](assets/triggered-oc-scheduler.png){zoomable="yes"}

## 신호 페이로드에 대한 매개 변수 추가(선택 사항) {#parameters}

트리거 신호에서 매개 변수를 전달하고 실행 컨텍스트(예: 타깃팅, 조건 또는 표현식)의 캠페인에서 사용할 수 있습니다. 먼저 일정 설정에서 각 매개 변수를 정의한 다음, 트리거 API를 호출하거나 업스트림 캠페인의 **[!UICONTROL 종료]** 활동에서 매개 변수를 매핑할 때 해당 값을 전달합니다([아래 참조](#signal-end)).

1. 캠페인 일정을 열고 **[!UICONTROL 매개 변수 추가]**&#x200B;를 선택합니다.

1. 신호 페이로드에서 전송할 각 매개 변수의 이름과 데이터 형식을 정의합니다. 테스트 모드에서 캠페인을 트리거할 때 사용할 **테스트 값**&#x200B;을 제공할 수도 있습니다. [트리거된 캠페인을 테스트하는 방법을 알아봅니다](#build-and-test).

   ![매개 변수를 추가하여 신호의 페이로드 매개 변수를 정의합니다](assets/triggered-oc-parameter.png){zoomable="yes"}

>[!NOTE]
>
>REST API에 의해 트리거된 오케스트레이션된 캠페인의 경우 스케줄러에 정의되지 않은 API 호출에서 매개 변수를 전달하면 API 호출이 계속 성공하고 매개 변수가 전파되므로 표현식에 사용할 수 있습니다. 하지만 오케스트레이션된 캠페인 인터페이스는 이 인터페이스를 사용하는 데 도움이 되지 않습니다. 예를 들어 테스트 활동에서는 스케줄러에 정의되지 않은 매개 변수를 나열하거나 표시하지 않습니다.

## 캠페인 테스트 {#build-and-test}

캔버스에서 캠페인을 빌드한 다음 REST API를 통해 신호를 전송하여 게시하기 전에 **[!UICONTROL 초안]**&#x200B;에서 테스트하십시오.

* **REST API에 의해 트리거된 오케스트레이션된 캠페인** - 아래 단계를 사용하여 초안에서 캠페인을 실행하고 게시 전에 타깃팅, 매개 변수 및 게재 논리의 유효성을 검사합니다.

* **종료 활동으로 트리거된 오케스트레이션된 캠페인** — 전체 체인을 초안에서 처음부터 끝까지 실행할 수 없습니다. 업스트림 캠페인이 게시되면 해당 **[!UICONTROL 종료]** 활동은 게시된 다운스트림 캠페인만 시작합니다. 두 캠페인이 게시되기 전에 다운스트림 측면을 테스트하려면 해당 캠페인을 **[!UICONTROL 초안]**&#x200B;에 보관하고, 스케줄러에서 신호 매개 변수에 대해 **[!UICONTROL 테스트 값]**&#x200B;을 설정([신호 페이로드에 대한 매개 변수 추가](#parameters))한 다음 아래 API 단계를 따르십시오. 트리거 API 호출은 런타임에 **[!UICONTROL End]** 활동과 동일한 페이로드를 사용하므로 다운스트림 캠페인을 게시하고 업스트림 **[!UICONTROL End]** 활동([다른 캠페인의 종료 활동에서 트리거](#signal-end))을 구성하기 전에 매개 변수 라우팅 및 캔버스 논리를 확인할 수 있습니다.

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

1. 스케줄러에서 복사한 샘플 요청을 사용하여 트리거 API 호출을 보냅니다. 요청 및 응답 세부 정보는 [오케스트레이션된 캠페인 API 트리거](https://developer.adobe.com/journey-optimizer-apis/references/oc-trigger){target="_blank"}를 참조하십시오.

테스트 결과가 만족스러우면 [캠페인을 게시](#publish)하십시오.

## 캠페인 게시 및 트리거 {#publish}

[캠페인을 테스트](#build-and-test)한 후 게시하면 응용 프로그램이나 다른 캠페인의 **[!UICONTROL 종료]** 활동에서 신호를 받을 수 있습니다. [캠페인 시작 및 모니터링에 대해 자세히 알아보세요](start-monitor-campaigns.md#publish).

그런 다음 REST API 또는 다른 캠페인의 **[!UICONTROL End]** 활동에서 트리거할 수 있습니다. 아래 섹션을 참조하십시오.

### REST API를 사용하여 신호 보내기 {#publish-api}

게시 후 자체 애플리케이션에서 캠페인을 트리거할 때마다 다음 단계를 따르십시오.

1. 캠페인 스케줄러를 열고 **[!UICONTROL API 요청 복사]**&#x200B;를 선택하고 형식(cURL 또는 HTTP 요청)을 선택합니다.

   복사된 정보에는 오케스트레이션된 캠페인 ID, 샌드박스 이름, 조직 ID 및 일부를 추가한 경우 매개 변수가 포함됩니다.

   ![예약 구성에서 API 요청 복사](assets/triggered-oc-copy.png)

1. 시스템에서 트리거 API를 호출합니다. 라이브 끝점 사양에 대해서는 [오케스트레이션된 캠페인 API 트리거](https://developer.adobe.com/journey-optimizer-apis/references/oc-trigger){target="_blank"}를 참조하십시오.

   >[!IMPORTANT]
   >
   >실시간 오케스트레이션된 캠페인의 경우 스로틀 가드레일은 두 API 트리거 실행 사이에 최소 1시간 간격을 적용합니다. 해당 간격이 경과하기 전에 API를 다시 호출하는 경우 API가 HTTP 429(요청이 너무 많음)를 반환합니다. 이 가드레일은 초안 버전을 테스트하도록 트리거할 때 적용되지 않습니다.

   신호 페이로드에 매개 변수를 추가한 경우 API 호출에 전달하는 값은 캠페인이 실행될 때 캠페인 이벤트 변수로 노출됩니다. 이를 검사하려면 캠페인 캔버스 도구 모음에서 캠페인 로그를 엽니다. **[!UICONTROL 작업]** 탭에서 신호에 해당하는 작업을 식별하고 연필 아이콘을 클릭하여 관련 이벤트 변수에 액세스합니다. [로그 및 작업에 액세스하는 방법을 알아봅니다](start-monitor-campaigns.md#logs-tasks).

   ![캠페인 이벤트 변수를 사용할 수 있는 로그 및 작업 화면](assets/trigger-events-variables.png){zoomable="yes"}

### 다른 캠페인의 종료 활동에서 신호 보내기 {#signal-end}

이 경로를 사용하여 오케스트레이션된 캠페인을 연결합니다. 업스트림 캠페인이 분기를 완료하면 **[!UICONTROL End]** 활동이 이미 **[!UICONTROL 신호에 의해 트리거됨]**(으)로 설정된 다운스트림 캠페인으로 신호를 보냅니다. 이를 통해 더 작은 캠페인을 재사용하고 각 호출자의 다른 페이로드를 전달할 수 있습니다.

>[!NOTE]
>
>* 동일한 캔버스에서 여러 **[!UICONTROL End]** 활동을 사용하고 각 활동을 구성하여 다른 다운스트림 캠페인을 트리거할 수 있습니다.
>* 여러 캠페인이 동일한 다운스트림 캠페인을 트리거할 수 있습니다. 각 호출은 다른 페이로드를 전송할 수 있습니다.

먼저 실행해야 하는 캠페인에 대해 다음 단계를 수행합니다.

1. 신호를 보내야 하는 오케스트레이션된 캠페인을 열고 다운스트림 캠페인이 시작되기 전에 완료해야 하는 분기의 끝에서 **[!UICONTROL End]** 활동을 선택합니다.
1. **[!UICONTROL 외부 신호]** 섹션에서 트리거할 다운스트림 캠페인을 선택하십시오.

1. 필요한 경우 매개 변수를 추가합니다. 다운스트림 캠페인의 일정과 동일한 이름을 사용하고 각 값을 설정합니다.

   ![](assets/end-signal.png)

1. 게시하기 전에 초안 모드에서 다운스트림 캠페인을 테스트하려면 [캠페인 테스트](#build-and-test) 섹션의 단계에 따라 REST API로 초안에서 트리거하십시오.

업스트림 캠페인이 트리거되는 **[!UICONTROL End]** 활동에 충분히 도달할 수 있을 만큼 실행되기 전에 다운스트림 캠페인을 게시해야 합니다. 대상 캠페인이 게시되지 않은 상태에서 신호를 보내면 실행이 실패합니다. 다운스트림 캠페인을 게시한 다음 필요에 따라 다시 시작하거나 재개합니다.
