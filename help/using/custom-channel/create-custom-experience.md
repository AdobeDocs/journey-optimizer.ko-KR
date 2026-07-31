---
title: 사용자 지정 채널 경험 만들기
description: 여정 또는 Adobe Journey Optimizer의 캠페인에서 사용자 지정 채널을 사용하는 방법을 알아봅니다.
feature: Channel Configuration
topic: Content Management
role: User
level: Experienced
badge: label="제한 공개" type="Informative"
source-git-commit: 6aa595444e13ddd37a15734f47cc11ce17585117
workflow-type: tm+mt
source-wordcount: '997'
ht-degree: 14%

---


# 사용자 지정 채널 경험 만들기 {#create-custom-channel}

>[!BEGINSHADEBOX]

**이 페이지에서:** Adobe Journey Optimizer의 여정 또는 캠페인에 사용자 지정 채널을 추가하고 표현식 편집기를 사용하여 개인화된 메시지 페이로드를 작성하는 방법에 대해 알아봅니다.

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>이 기능은 제한적으로 이용할 수 있습니다. 액세스 권한을 얻으려면 Adobe 담당자에게 문의하십시오.

[!DNL Journey Optimizer]에서는 캠페인 및 여정에서 사용자 지정 채널을 사용하여 메시지를 전달할 수 있습니다. 사용자 지정 채널 경험을 설정하려면 아래 단계를 따르십시오.

>[!NOTE]
>
>사용자 지정 채널 경험을 만들기 전에 관리자가 사용자 지정 채널을 구성했는지 확인하십시오. [자세히 알아보기](configure-custom-channel.md)

## 여정 또는 캠페인을 통한 사용자 정의 액션 추가 {#create-custom-channel-experience}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_channel"
>title="사용자 정의 채널 액션"
>abstract="사용자 정의 채널 액션은 프로필이 여정의 이 단계에 도달하면 프로필에 메시지를 전달합니다. 레이블은 여정 캔버스에서 활동을 식별하고, 액션은 메시지 전달에 사용되는 엔드포인트, 페이로드 및 자격 증명을 정의하는 사용자 정의 채널 구성을 참조합니다. **최적화** 섹션은 콘텐츠 실험 또는 타기팅 규칙을 포함할 수 있고, **시간 초과 또는 오류** 섹션은 액션이 실패할 경우 대체 경로를 정의할 수 있습니다."
>additional-url="https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/orchestrate-journeys/about-journey-building/journey-action#add-action" text="사용자 정의 채널 시작하기"



>[!BEGINTABS]

>[!TAB 여정에 사용자 지정 채널 추가]

사용자 지정 채널은 여정 캔버스 팔레트의 **[!UICONTROL 작업]** 섹션에 표시되며, 채널 빌더에 정의된 대로 해당 표시 이름과 사용자 지정 아이콘으로 나열됩니다.

여정에 사용자 지정 채널 작업을 추가하려면:

1. [여정 만들기](../building-journeys/journey-gs.md).

1. [이벤트](../building-journeys/general-events.md) 또는 [대상자 읽기](../building-journeys/read-audience.md) 활동으로 여정을 시작하십시오.

1. 팔레트의 **[!UICONTROL 작업]** 섹션에서 **[!UICONTROL 작업]** 활동을 끌어서 놓습니다. [작업 활동](../building-journeys/journey-action.md)에 대해 자세히 알아보세요.

1. **[!UICONTROL 작업]** 드롭다운에서 사용할 사용자 지정 채널을 선택합니다. 사용자 지정 채널은 채널 빌더에 지정된 이름과 아이콘으로 나열됩니다.

   ![여정 캔버스에서 사용자 지정 채널 작업 선택](assets/custom_channel_journey_action.png){width="80%"}

1. 작업에 레이블을 추가하고 오른쪽 패널에서 **[!DNL Configure action]**&#x200B;을(를) 클릭한 다음 사용할 **[!UICONTROL 채널 구성]**&#x200B;을(를) 선택하십시오. [사용자 지정 채널 구성을 만드는 방법을 알아봅니다](custom-channel-configuration.md#create-channel-config)

1. **[!UICONTROL 메시지]** 섹션에서 **[!UICONTROL 콘텐츠 편집]**&#x200B;을 클릭하여 페이로드 편집기를 열고 메시지를 작성합니다. [콘텐츠를 작성하는 방법 알아보기](#author-content)

1. 필요에 따라 단계를 더 추가하여 여정 흐름을 완료한 다음 여정을 게시합니다. [자세히 알아보기](../building-journeys/journey-gs.md)

>[!TAB 사용자 지정 채널 캠페인 만들기]

캠페인에서 사용자 지정 채널을 사용하려면 다음 작업을 수행하십시오.

1. [캠페인을 만듭니다](../campaigns/create-campaign.md).

1. 캠페인 유형 선택:

   * **[!UICONTROL 예약됨 - 마케팅]** - 즉시 실행되거나 지정된 날짜에 실행됨. UI에서 구성된 마케팅 메시지용으로 설계되었습니다.
   * **[!UICONTROL API 트리거됨 - 마케팅/트랜잭션]** - API 호출을 통해 실행됩니다. 이벤트 트리거 메시징을 위해 설계되었습니다(예: 주문 확인 또는 암호 재설정). [자세히 알아보기](../campaigns/api-triggered-campaigns.md)

1. 캠페인 설정 완료: 캠페인 속성, [대상자](../audience/about-audiences.md) 및 [일정](../campaigns/create-campaign.md#schedule).

1. **[!UICONTROL 작업]** 섹션의 채널 선택기에서 사용자 지정 채널을 선택합니다. 샌드박스에 구성된 모든 사용자 지정 채널이 기본 채널과 함께 표시됩니다.

   ![Campaign 사용자 지정 작업 선택](assets/custom_channel_campaign_action.png){width="80%"}

1. 사용할 **[!UICONTROL 채널 구성]**&#x200B;을 선택하거나 만드십시오. [채널 구성을 만드는 방법을 알아봅니다](custom-channel-configuration.md#create-channel-config)

   ![사용자 지정 채널 구성 선택](assets/custom_channel_campaign_action_config.png){width="80%"}

1. 필요한 경우 **[!UICONTROL 작업 추적]**&#x200B;을(를) 활성화하여 메시지 페이로드에 포함된 링크를 자동으로 추적합니다(사용자 지정 채널에 대해 구성된 하위 도메인 필요). [사용자 지정 채널의 하위 도메인을 위임하는 방법을 알아봅니다](custom-channel-subdomains.md#subdomain-delegation)

1. **[!UICONTROL 최적화]** 섹션에서 다음을 수행할 수 있습니다.

   * **[!UICONTROL 타깃팅 규칙을 만들고]** 대상자의 서로 다른 세그먼트에 다른 메시지를 보냅니다. [자세히 알아보기](../campaigns/create-campaign.md#targeting)
   * 사용자 지정 채널 메시지에 대해 A/B 테스트를 실행하려면 **[!UICONTROL 실험 만들기]**&#x200B;를 클릭하십시오. [자세히 알아보기](../campaigns/create-campaign.md#content-experiment)

1. **[!UICONTROL 콘텐츠 편집]**&#x200B;을 클릭하여 페이로드 편집기를 열고 메시지를 작성합니다. [콘텐츠를 작성하는 방법 알아보기](#author-content)

1. 캠페인을 검토하고 활성화합니다. [자세히 알아보기](../campaigns/create-campaign.md)

<!--
>[!TAB Add a custom channel to an orchestrated campaign]

Custom channels appear in the channel selection list in the orchestrated Campaigns canvas, below the native channels, with their custom icon and display name.

To add a custom channel in an orchestrated campaign:

1. Open or create an orchestrated campaign.

1. In the canvas, add a channel action node and select your custom channel from the list.

1. Select the **[!UICONTROL Channel configuration]** to use. Ensure the configuration includes the **[!UICONTROL Execution details]** section required for orchestrated campaigns.

1. Click **[!UICONTROL Edit content]** to open the payload editor and author your message. [Learn how to author content](#author-content)
-->

>[!ENDTABS]

## 사용자 지정 채널 콘텐츠 작성 {#author-content}

콘텐츠 편집기는 사용자 지정 채널을 구성할 때 정의한 페이로드 구조를 반영합니다. **[!UICONTROL 코드 편집]**&#x200B;을 클릭하여 페이로드 편집기를 열고 메시지 내용을 입력합니다.

![사용자 지정 채널 페이로드 편집기](assets/custom_channel_payload_editor.png){width="80%"}

작성하고 개인화할 수 있는 필드가 표시됩니다. [!DNL Journey Optimizer] 개인화 편집기를 모든 개인화 및 작성 기능과 함께 활용할 수 있습니다. [자세히 알아보기](../personalization/personalization-build-expressions.md)

>[!NOTE]
>
>JSON 페이로드만 지원됩니다. 사용자 지정 채널 페이로드가 JSON이 아닌 경우 JSON 래퍼를 사용하여 콘텐츠를 캡슐화할 수 있습니다. 예를 들어 페이로드가 XML인 경우 다음과 같이 JSON 개체에 래핑할 수 있습니다.
>
>```json
>{
>   "payload": "<xml>...</xml>"
>}
>```

### 페이로드 개인화 {#personalize}

[!DNL Journey Optimizer]의 전체 개인화 기능을 페이로드 편집기에서 사용할 수 있습니다.

* **프로필 특성** - `{{profile.person.name.firstName}}`과(와) 같은 XDM 프로필 특성이나 사용자 지정 네임스페이스에 저장된 메시징 플랫폼 사용자 ID와 같은 사용자 지정 ID를 삽입합니다.
* **컨텍스트 특성** - 전송 시 확인된 여정 이벤트 특성 또는 캠페인 컨텍스트 데이터를 사용합니다.
* **도우미 함수** - 기본 제공 문자열, 날짜 또는 산술 함수를 사용하여 값의 형식을 지정합니다. [자세히 알아보기](../personalization/functions/helpers.md)
* **식 조각** - 여러 채널 및 캠페인에서 공유 개인화 논리를 다시 사용합니다. [자세히 알아보기](../content-management/customizable-fragments.md)

>[!CAUTION]
>
>현재 작성 시 페이로드의 유효성 검사가 없습니다. **[!UICONTROL 콘텐츠 시뮬레이션]** 기능을 사용하여 페이로드가 올바른 형식의 JSON이고 모든 개인화 표현식이 테스트 프로필에 대해 올바르게 확인되는지 확인할 수 있습니다. [자세히 알아보기](test-custom-channel.md#simulate-content)

다음 예는 프로필 개인화를 통한 JSON 페이로드를 보여 줍니다.

```json
{
  "message": {
    "template": "Limited offer just for you, {{profile.person.name.firstName}}!",
    "header": "You have a FREE drink when you buy a King menu!"
  },
  "campaign_ref": {
    "id": "2grjya",
    "type": "loyalty",
    "url": "/companies/wNmRsLbu/campaigns/wallet/2grjya"
  }
}
```

```json
{
  "messaging_product": "mess",
  "recipient_type": "individual",
  "to": "{{profile.mobilePhone.number}}",
  "zipCode": 4001,
  "type": "image",
  "image": {
    "id": "1479537139650973",
    "caption": "The best succulent ever?"
  }
}
```

### 페이로드에서 링크 추적 {#track-links}

사용자 지정 채널 페이로드에 추적된 링크를 포함시켜 클릭 수가 자동으로 추적되어 채널의 보고 대시보드에 표시되도록 하려면 다음 핸들바 구문을 사용하여 URL을 래핑합니다.

```
{{url trackedUrl='' originalUrl='https://example.com/' type='TRACKED'}}
```

* `originalUrl` - 수신자를 리디렉션할 대상 URL입니다.
* `trackedUrl` - 비워 둡니다. [!DNL Journey Optimizer]은(는) 전송 시 자동으로 추적 사용 리디렉션 URL로 채웁니다.
* `type` - `TRACKED`(으)로 설정해야 합니다.

>[!NOTE]
>
>링크 추적에는 사용자 지정 채널에 대해 구성된 하위 도메인이 필요합니다. [사용자 지정 채널의 하위 도메인을 위임하는 방법을 알아봅니다](custom-channel-subdomains.md#subdomain-delegation)

**예 - Viber 페이로드에서 추적된 링크:**

```json
{
  "receiver": "{{profile.mobilePhone.number}}",
  "min_api_version": 1,
  "sender": {
    "name": "Luma Rewards",
    "avatar": "https://avatar.example.com"
  },
  "tracking_data": "{{profile.person.name.firstName}}",
  "type": "text",
  "text": "Hello {{profile.person.name.firstName}}! Discover our new collection: {{url trackedUrl='' originalUrl='https://luma.com/collection' type='TRACKED'}}"
}
```

<!--
### Strict JSON mode {#strict-json}

The editor supports a **[!UICONTROL Strict JSON]** toggle:

* **Strict JSON: Off (default)** – The editor accepts any payload content, including personalization helpers and functions that may temporarily produce non-JSON syntax. A warning is displayed at the **Review to Activate** step if the payload is not well-formed JSON, prompting you to simulate and proof before publishing.
* **Strict JSON: On** – The editor validates that the payload is well-formed JSON as you type. At the **Review to Activate** step, [!DNL Journey Optimizer] validates the payload against the channel schema and flags missing required fields or type mismatches as errors that must be resolved before activation.
-->

## 사용자 지정 채널 경험 활성화 {#activate}

>[!IMPORTANT]
>
>활성화하기 전에 사용자 지정 채널 페이로드를 미리 보고 테스트하십시오. [방법 알아보기](test-custom-channel.md)
>
>캠페인이나 여정이 승인 정책의 대상인 경우 활성화하기 전에 승인을 요청해야 합니다. [자세히 알아보기](../test-approve/gs-approval.md)

* **여정에서** - 오른쪽 상단의 **[!UICONTROL 게시]**&#x200B;를 클릭합니다. 여정이 라이브로 전환되고 자격 조건을 갖춘 프로필에 대한 외부 엔드포인트 호출을 시작합니다.
* **캠페인에서** - **[!UICONTROL 활성화하려면 검토]**&#x200B;를 클릭하고 설정을 검토한 다음 **[!UICONTROL 활성화]**&#x200B;를 클릭합니다. 캠페인은 **[!UICONTROL Live]** 상태(또는 향후 시작 날짜가 정의된 경우 **[!UICONTROL 예약됨]**)를 사용합니다.
