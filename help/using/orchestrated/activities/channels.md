---
solution: Journey Optimizer
product: journey optimizer
title: 여러 단계로 구성된 캠페인에 채널 활동 추가
description: 여러 단계로 구성된 캠페인에 채널 활동을 추가하는 방법 알아보기
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: ffe1e77c-6c4f-4f23-9183-d715a4c7c402
source-git-commit: 3c3ef1555c587b3e50e3b70596fbac98e87d414e
workflow-type: tm+mt
source-wordcount: '1213'
ht-degree: 77%

---

# 채널 활동 {#channel}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_email"
>title="이메일 활동"
>abstract="이메일 활동을 사용하면 오케스트레이션된 캠페인 내에서 일회성 이메일과 반복 이메일을 모두 전송할 수 있습니다. 이는 동일한 오케스트레이션된 캠페인 내에서 계산된 대상으로 이메일을 전송하는 프로세스를 자동화하는 역할을 합니다. 채널 활동을 다단계 캠페인 캔버스에 결합하여 고객 행동 및 데이터에 따라 액션을 트리거할 수 있는 크로스 채널 캠페인을 만들 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_sms"
>title="SMS 활동"
>abstract="SMS 활동을 사용하면 오케스트레이션된 캠페인 내에서 일회성 SMS와 반복 SMS를 모두 전송할 수 있습니다. 이는 동일한 오케스트레이션된 캠페인 내에서 계산된 대상으로 SMS를 전송하는 프로세스를 자동화하는 역할을 합니다. 채널 활동을 다단계 캠페인 캔버스에 결합하여 고객 행동 및 데이터에 따라 액션을 트리거할 수 있는 크로스 채널 캠페인을 만들 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push"
>title="푸시 활동"
>abstract="푸시 활동을 사용하면 오케스트레이션된 캠페인의 일부로 푸시 알림을 전송할 수 있습니다. 일회성 메시지와 반복 오케스트레이션된 캠페인 모두를 게재할 수 있으며, 동일한 오케스트레이션된 캠페인 내에서 사전 정의된 대상으로 푸시 알림을 전송하는 프로세스를 자동화합니다. 채널 활동을 캠페인 캔버스에 결합하여 고객 행동 및 데이터에 따라 액션을 트리거할 수 있는 크로스 채널 캠페인을 만들 수 있습니다."

<!--
UNUSED IDs in BJ

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push_ios"
>title="Push iOS activity"
>abstract="The Push iOS activity let you send iOS Push notifications as part of your orchestrated campaign. It enables the delivery of both one-time and recurring orchestrated campaigns, automating the sending iOS Push notifications to a predefined target within the same workflow. You can combine channel activities into the campaign canvas to create cross-channel campaigns that can trigger actions based on customer behavior and data."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push_android"
>title="Push Android activity"
>abstract="The Push Android activity ket you send Android Push notifications as part of your orchestrated campaign. It enables the delivery of both one-time and recurring messages, automating the sending Android Push notifications to a predefined target within the same orchestrated campaign. You can combine channel activities into the orchestrated campaign canvas to create cross-channel campaigns that can trigger actions based on customer behavior and data."

-->

>[!CONTEXTUALHELP]
>id="ajo_orchestration_directmail"
>title="다이렉트 메일 활동"
>abstract="다이렉트 메일 활동은 오케스트레이션된 캠페인 내에서 다이렉트 메일 전송 과정을 원활하게 하며 일회성 메시지와 반복 메시지를 모두 전송할 수 있습니다. 이는 다이렉트 메일 제공업체에 필요한 추출 파일 생성 프로세스를 자동화하는 역할을 합니다. 채널 활동을 오케스트레이션된 캠페인 캔버스에 결합하여 고객 행동 및 데이터에 따라 액션을 트리거할 수 있는 크로스 채널 캠페인을 만들 수 있습니다."


+++ 목차

| 오케스트레이션된 캠페인 시작 | 첫 오케스트레이션된 캠페인 시작 | 데이터베이스 쿼리 | 오케스트레이션된 캠페인 활동 |
|---|---|---|---|
| [오케스트레이션된 캠페인 시작](../gs-orchestrated-campaigns.md)<br/><br/>관계형 스키마 및 데이터 세트 만들기 및 관리:</br> <ul><li>[스키마 및 데이터 세트 시작](../gs-schemas.md)</li><li>[수동 스키마](../manual-schema.md)</li><li>[파일 업로드 스키마](../file-upload-schema.md)</li><li>[데이터 수집](../ingest-data.md)</li></ul>[오케스트레이션된 캠페인 액세스 및 관리](../access-manage-orchestrated-campaigns.md) | [오케스트레이션된 캠페인을 만드는 주요 단계](../gs-campaign-creation.md)<br/><br/>[캠페인 만들기 및 예약](../create-orchestrated-campaign.md)<br/><br/>[활동 오케스트레이션](../orchestrate-activities.md)<br/><br/>[캠페인 시작 및 모니터링](../start-monitor-campaigns.md)<br/><br/>[보고](../reporting-campaigns.md) | [규칙 빌더로 작업](../orchestrated-rule-builder.md)<br/><br/>[첫 번째 쿼리 작성](../build-query.md)<br/><br/>[표현식 편집](../edit-expressions.md)<br/><br/>[리타기팅](../retarget.md) | [활동 시작](about-activities.md)<br/><br/>활동:<br/>[And 조인](and-join.md) - [대상자 빌드](build-audience.md) - [차원 변경](change-dimension.md) - <b>[채널 활동](channels.md)</b> - [결합](combine.md) - [중복 제거](deduplication.md) - [보강](enrichment.md) - [포크](fork.md) - [조정](reconciliation.md) - [대상자 저장](save-audience.md) - [분할](split.md) - [대기](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

이 페이지의 컨텐츠는 최종본이 아니며, 변경될 수 있습니다.

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer]을(를) 사용하면 여러 채널(이메일, SMS, 푸시 알림)에 걸쳐 마케팅 캠페인을 자동화하고 실행할 수 있습니다. 채널 활동을 캠페인 캔버스에 결합하여 고객 행동 및 데이터에 따라 액션을 트리거할 수 있는 크로스 채널 오케스트레이션된 캠페인을 만들 수 있습니다.

예:
* 이메일, SMS, 푸시를 통해 환영 인사 시리즈를 보냅니다.
* 구매 후에 후속 이메일을 전달합니다.
* SMS를 통해 개인화된 생일 인사를 보냅니다.

채널 활동을 사용하여 여러 터치포인트에서 고객을 참여시키고 전환을 유도하는 포괄적인 맞춤형 캠페인을 만들 수 있습니다.

>[!PREREQUISITES]
>
>채널 활동을 추가하기 전에 [대상자 작성 활동](build-audience.md)을 사용하여 타깃 대상자를 정의합니다.

## 채널 활동 추가 및 속성 정의 {#add}

1. 캔버스에 채널 활동을 추가합니다. 사용 가능한 채널 활동은 **[!UICONTROL 이메일]**, **[!UICONTROL SMS]**, **[!UICONTROL 푸시]**&#x200B;입니다.

   ![사용 가능한 활동이 있는 캔버스를 보여 주는 이미지](../assets/channel-add.png)

1. 선택한 채널에 따라 활동을 선택하고 **[!UICONTROL 이메일 편집]**, **[!UICONTROL SMS 편집]** 또는 **[!UICONTROL 푸시 편집]**&#x200B;을 클릭합니다.

   ![이메일 활동이 있는 캔버스를 보여 주는 이미지](../assets/channel-edit.png)

1. **[!UICONTROL 속성]** 탭에서 설명을 입력한 다음 **[!UICONTROL 액션]** 탭으로 전환하여 활동을 구성합니다.

## 채널 구성 및 설정 지정 {#configuration}

**[!UICONTROL 액션]** 탭을 사용하여 메시지의 채널 구성을 선택하고 추적, 콘텐츠 실험 또는 다국어 콘텐츠와 같은 추가 설정을 구성합니다.

1. **채널 구성 선택**

   구성은 [시스템 관리자](../../start/path/administrator.md)가 정의합니다. 여기에는 헤더 매개변수, 하위 도메인, 모바일 앱 등 메시지 전송을 위한 모든 기술적 매개변수가 포함되어 있습니다. [채널 구성을 설정하는 방법을 알아봅니다](../../configuration/channel-surfaces.md).

   ![액션 섹션을 보여 주는 이미지](../assets/channel-actions.png)

1. **최대 가용량 규칙 적용**

   **[!UICONTROL 규칙 집합]** 드롭다운 목록에서 최대 가용량 규칙을 캠페인에 적용할 채널 규칙 집합을 선택하십시오. 채널 규칙 세트를 활용하면 통신 유형별로 빈도 상한을 설정하여 유사한 메시지가 있는 고객을 오버로드할 수 있습니다. [규칙 세트 작업 방법 알아보기](../conflict-prioritization/rule-sets.md)

1. **참여 추적**(전자 메일 및 SMS)

   **[!UICONTROL 액션 추적]** 섹션을 사용하여 수신자가 이메일 또는 SMS 게재에 어떻게 반응하는지 추적할 수 있습니다. 캠페인이 실행되면 캠페인 보고서에서 추적 결과에 액세스할 수 있습니다. [캠페인 보고서에 대해 자세히 알아보기](../../reports/campaign-global-report-cja.md)

1. **빠른 전송 모드 사용**(푸시)

   빠른 전송 모드는 캠페인을 통해 대량으로 매우 빠르게 푸시 메시지를 전송할 수 있는 [!DNL Journey Optimizer] 추가 기능입니다. 빠른 게재는 메시지 게재 지연이 비즈니스에 중요한 경우, 휴대폰에 긴급 푸시 알림을 전송하려는 경우(예: 뉴스 채널 앱을 설치한 사용자에게 속보 전달) 사용됩니다. 빠른 전송 모드를 사용할 때의 성능에 대한 자세한 내용은 [Adobe Journey Optimizer 제품 설명](https://helpx.adobe.com/kr/legal/product-descriptions/adobe-journey-optimizer.html)을 참조하십시오.

1. **콘텐츠 실험 만들기**

   **[!UICONTROL 콘텐츠 실험]** 섹션을 사용하여 여러 가지 게재 방식을 정의하고, 어떤 방식이 타깃 대상자에게 가장 효과적인지 측정합니다. **[!UICONTROL 실험 만들기]** 버튼을 클릭한 다음 [콘텐츠 실험 만들기](../../content-management/content-experiment.md) 섹션에 자세히 설명된 단계를 따릅니다.

1. **다국어 콘텐츠 추가**

   **[!UICONTROL 언어]** 섹션을 사용하여 캠페인 내에서 여러 언어로 콘텐츠를 만듭니다. 이렇게 하려면 **[!UICONTROL 언어 추가]** 버튼을 클릭하고 원하는 **[!UICONTROL 언어 설정]**&#x200B;을 선택합니다. 다국어 기능 설정 및 사용 방법에 대한 자세한 정보는 [다국어 콘텐츠 시작](../../content-management/multilingual-gs.md) 섹션에서 확인할 수 있습니다.

   ![콘텐츠 실험 섹션을 표시하는 이미지](../assets/channel-experiment.png)

채널 활동이 구성되면 **[!UICONTROL 콘텐츠]** 탭을 선택하여 콘텐츠를 정의합니다.

## 콘텐츠 정의 {#content}

메시지를 만들려면 **[!UICONTROL 콘텐츠]** 탭으로 전환합니다. 단계별 프로세스는 선택한 채널에 따라 다릅니다. 다음 페이지에서 메시지 콘텐츠를 만드는 자세한 단계를 살펴봅니다.

<table style="table-layout:fixed"><tr style="border: 0; text-align: center;" >
<td><a href="../../email/create-email.md"><img alt="이메일" src="../../channels/assets/do-not-localize/email.png"></a><br/><a href="../../email/create-email.md"><strong>이메일 만들기</strong></a></td>
<td><a href="../../sms/create-sms.md"><img alt="sms" src="../../channels/assets/do-not-localize/sms.png"></a><br/><a href="../../sms/create-sms.md"><strong>SMS 만들기</strong></a></td>
<td><a href="../../push/create-push.md"><img alt="푸시" src="../../channels/assets/do-not-localize/push.png"></a><a href="../../push/create-push.md"><strong>푸시 알림 만들기</strong></a></td>
</tr></table>

## 개인화 추가

오케스트레이션된 캠페인의 Personalization은 다른 **[!UICONTROL Journey Optimizer]** 캠페인 또는 여정과 비슷하게 작동하지만 오케스트레이션된 캔버스와 관련된 몇 가지 주요 차이점이 있습니다.

오케스트레이션된 캠페인에서 개인화 편집기에 액세스하면 두 개의 기본 폴더에 아래에 설명된 개인화에 사용할 수 있는 속성이 포함됩니다.

* **[!UICONTROL 프로필 속성]**

  이 폴더에는 [!DNL Adobe Experience Platform]의 모든 프로필 관련 데이터가 포함되어 있습니다. 이름, 이메일 주소, 위치 또는 사용자 프로필에 캡처된 기타 트레이트와 같은 표준 속성입니다.

* **[!UICONTROL Target 특성]**(오케스트레이션된 캠페인에만 해당)

  이 폴더는 오케스트레이션된 캠페인에만 사용할 수 있습니다. 여기에는 캠페인 캔버스 내에서 직접 계산된 속성이 포함됩니다. 여기에는 두 개의 하위 폴더가 있습니다.

   * **`<Targeting dimension>`**(예: &quot;수신자&quot;, &quot;구매&quot;): 캠페인에서 타겟팅한 차원과 관련된 모든 특성을 포함합니다.

   * **`Enrichment`**: 캔버스에 **[!UICONTROL 데이터 보강]** 활동을 통해 추가된 데이터를 포함합니다. 이렇게 하면 오케스트레이션 중에 통합된 외부 데이터 세트 또는 추가 논리를 기반으로 메시지를 개인화할 수 있습니다. [데이터 보강 활동을 사용하는 방법을 알아보세요](../activities/enrichment.md)

개인화 편집기 사용 방법에 대한 자세한 개요는 [개인화 시작](../../personalization/personalize.md)을 참조하세요.

## 콘텐츠 확인 및 테스트

콘텐츠가 생성되면 **[!UICONTROL 콘텐츠 시뮬레이션]** 버튼을 사용하여 CSV/JSON 파일에서 업로드하거나 수동으로 추가한 테스트 프로필이나 샘플 입력 데이터로 콘텐츠를 미리 보고 테스트합니다. [자세히 알아보기](../../content-management/preview-test.md)

![콘텐츠 시뮬레이션 버튼을 표시하는 이미지](../assets/channel-simulate.png)

## 다음 단계 {#next}

메시지 콘텐츠가 준비되면 **[!UICONTROL 뒤로]** 화살표를 사용하여 오케스트레이션된 캠페인으로 다시 이동합니다. 그런 다음 캔버스에서 활동 오케스트레이션을 완료하고 캠페인을 게시하여 메시지 전송을 시작할 수 있습니다. [오케스트레이션된 캠페인을 시작하고 모니터링하는 방법 알아보기](../start-monitor-campaigns.md)

![뒤로 버튼을 표시하는 이미지](../assets/channel-back.png)

<!--
## Examples {#cross-channel-workflow-sample}

Here is a cross-channel orchestrated campaign example with a segmentation and two deliveries. The orchestrated campaign targets all customers who live in Paris and who are interested in coffee machines. Among this population, an email is sent to the regular customers and an SMS is sent to the VIP clients.

![](../assets/workflow-channel-example.png)

<!--
description, which use case you can perform (common other activities that you can link before of after the activity)

how to add and configure the activity

example of a configured activity within a workflow
The Email delivery activity allows you to configure the sending an email in a workflow. 

-->

<!--You can also create a recurring orchestrated campaign to send a personalized SMS every first day of the month at 8 PM to all customers living in Paris.

![](../assets/workflow-channel-example2.png)-->

<!-- Scheduled emails available?

This can be a single send email and sent just once, or it can be a recurring email.
* Single send emails are standard emails, sent once.
* Recurring emails allow you to send the same email multiple times to different targets over a defined period. You can aggregate the deliveries per period in order to get reports that correspond to your needs.

When linked to a scheduler, you can define recurring emails.
Email recipients are defined upstream of the activity in the same workflow, via an Audience targeting activity.

-->


<!--The message preparation is triggered according to the workflow execution parameters. From the message dashboard, you can select whether to request or not a manual confirmation to send the message (required by default). You can start the workflow manually or place a scheduler activity in the workflow to automate execution.-->
