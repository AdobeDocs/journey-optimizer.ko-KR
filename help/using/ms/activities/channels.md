---
solution: Journey Optimizer
product: journey optimizer
title: 다중 단계 캠페인에 채널 활동 추가
description: 여러 단계로 구성된 캠페인에서 채널 활동을 추가하는 방법 알아보기
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: ffe1e77c-6c4f-4f23-9183-d715a4c7c402
source-git-commit: 960c7ab18cdca6e34c06f2dc6672aefdb5340ef0
workflow-type: tm+mt
source-wordcount: '892'
ht-degree: 48%

---

# 채널 활동 {#channel}

Adobe Journey Optimizer을 사용하면 인바운드 및 아웃바운드 채널에서 마케팅 캠페인을 자동화하고 실행할 수 있습니다. 채널 활동을 오케스트레이션된 캠페인 캔버스에 결합하여 고객 행동 및 데이터를 기반으로 작업을 트리거할 수 있는 크로스 채널 오케스트레이션된 캠페인을 만들 수 있습니다. 지원되는 채널은 [이 페이지](../../channels/gs-channels.md)에 나열됩니다.

예를 들어 이메일, SMS, 푸시 및 DM과 같은 다양한 채널에 걸친 일련의 메시지를 포함하는 환영 이메일 캠페인을 만들 수 있습니다. 고객이 구매를 완료하면 후속 이메일을 보내거나, SMS를 통해 고객에게 맞춤형 생일 메시지를 보낼 수도 있습니다.

채널 활동을 사용하여 여러 터치포인트에서 고객을 참여시키고 전환을 유도하는 포괄적인 맞춤형 캠페인을 만들 수 있습니다.

## 전제 조건 {#channel-activity-prereq}

관련 활동을 통해 오케스트레이션된 캠페인 구축을 시작합니다.

* 채널 활동을 삽입하기 전에 대상자를 정의해야 합니다. 대상자는 게재의 주요 타겟인 메시지를 받는 프로필입니다.

* 반복 게재를 보내려면 **스케줄러** 활동으로 오케스트레이션된 캠페인을 시작하십시오. 일회성 단일 게재에 대해 **스케줄러** 활동을 사용하여 해당 게재에 대한 연락 날짜를 설정할 수도 있습니다. 연락 날짜는 게재 설정에서 설정할 수도 있습니다.

## 채널 활동 구성 {#create-a-delivery-in-a-workflow}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_email"
>title="이메일 활동"
>abstract="이메일 활동을 사용하면 다단계 캠페인 내에서 일회성 이메일과 반복 이메일을 모두 전송할 수 있습니다. 이는 동일한 다단계 캠페인 내에서 계산된 대상으로 이메일을 전송하는 프로세스를 자동화하는 역할을 합니다. 채널 활동을 다단계 캠페인 캔버스에 결합하여 고객 행동 및 데이터에 따라 액션을 트리거할 수 있는 크로스 채널 캠페인을 만들 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_sms"
>title="SMS 활동"
>abstract="SMS 활동을 사용하면 다단계 캠페인 내에서 일회성 SMS와 반복 SMS를 모두 전송할 수 있습니다. 이는 동일한 다단계 캠페인 내에서 계산된 대상으로 SMS를 전송하는 프로세스를 자동화하는 역할을 합니다. 채널 활동을 다단계 캠페인 캔버스에 결합하여 고객 행동 및 데이터에 따라 액션을 트리거할 수 있는 크로스 채널 캠페인을 만들 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push_ios"
>title="푸시 iOS 활동"
>abstract="푸시 iOS 활동을 사용하면 다단계 캠페인의 일부로 iOS 푸시 알림을 전송할 수 있습니다. 일회성 메시지와 반복 다단계 캠페인 모두를 게재할 수 있으며 동일한 워크플로 내에서 사전 정의된 대상으로 iOS 푸시 알림을 전송하는 프로세스를 자동화합니다. 채널 활동을 워크플로 캔버스에 결합하여 고객 행동 및 데이터에 따라 작업을 트리거할 수 있는 크로스 채널 워크플로를 만들 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push_android"
>title="푸시 Android 활동"
>abstract="Android 푸시 활동을 사용하면 다단계 캠페인의 일부로 Android 푸시 알림을 전송할 수 있습니다. 일회성 메시지와 반복 메시지 모두를 게재할 수 있으며 동일한 다단계 캠페인 내에서 사전 정의된 대상으로 Android 푸시 알림을 전송하는 프로세스를 자동화합니다. 채널 활동을 다단계 캠페인 캔버스에 결합하여 고객 행동 및 데이터에 따라 액션을 트리거할 수 있는 크로스 채널 캠페인을 만들 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_directmail"
>title="다이렉트 메일 활동"
>abstract="다이렉트 메일 활동은 다단계 캠페인 내에서 다이렉트 메일 전송 과정을 원활하게 하며 일회성 메시지와 반복 메시지를 모두 전송할 수 있습니다. 이는 다이렉트 메일 제공업체에 필요한 추출 파일 생성 프로세스를 자동화하는 역할을 합니다. 채널 활동을 다단계 캠페인 캔버스에 결합하여 고객 행동 및 데이터에 따라 액션을 트리거할 수 있는 크로스 채널 캠페인을 만들 수 있습니다."

오케스트레이션된 캠페인의 컨텍스트에서 게재를 설정하려면 아래 단계를 따르십시오.

1. 채널 활동 추가: **[!UICONTROL 이메일]**, **[!UICONTROL SMS]**, **[!UICONTROL 푸시 알림(Android)]**, **[!UICONTROL 푸시 알림(iOS)]** 또는 **[!UICONTROL 다이렉트 메일]**.

1. **게재 유형**(단일 또는 반복)을 선택하십시오.

   * **단일 게재**&#x200B;는 일회성 게재로, 블랙 프라이데이 이메일과 같이 한 번만 전송됩니다.
   * **반복 게재**&#x200B;는 실행 빈도에 따라 여러 번 전송됩니다. 오케스트레이션된 캠페인이 실행될 때마다 대상자가 다시 계산되고, 업데이트된 콘텐츠와 함께 업데이트된 대상자에게 게재가 전송됩니다. 예를 들어 주간 뉴스레터 또는 반복 생일 이메일일 수 있습니다.

1. 게재 **템플릿** 구성을 선택합니다. 템플릿은 채널별로 미리 구성된 게재 설정입니다. 기본 제공 템플릿은 각 채널에 대해 사용할 수 있으며 기본적으로 미리 채워져 있습니다.

   ![](../assets/delivery-activity-in-wf.png)

   채널 활동 구성 왼쪽 창에서 템플릿을 선택할 수 있습니다. 이전에 선택한 대상자가 채널과 호환되지 않는 경우 템플릿을 선택할 수 없습니다. 이 문제를 해결하려면 **대상자 작성** 활동을 업데이트하여 올바른 대상 매핑이 있는 대상자를 선택하십시오.

1. **게재 만들기**&#x200B;를 클릭합니다. 그런 다음 독립형 게재를 만드는 것과 동일한 방법으로 메시지 설정 및 콘텐츠를 정의할 수 있습니다. 콘텐츠를 테스트하고 시뮬레이션할 수도 있습니다.

1. 워크플로우로 다시 이동합니다. 워크플로우를 계속하려면 **아웃바운드 전환 생성** 옵션을 전환하여 채널 활동 후에 전환을 추가합니다.

1. 오케스트레이션된 캠페인을 시작하려면 **시작**&#x200B;을 클릭하세요.

   기본적으로 오케스트레이션된 캠페인을 시작하면 메시지를 즉시 보내지 않고 메시지 준비 단계가 트리거됩니다.

1. 채널 활동을 열어 **검토 및 보내기** 단추에서 전송을 확인합니다.

1. 게재 대시보드에서 **전송**&#x200B;을 클릭합니다.

## 예시 {#cross-channel-workflow-sample}

다음은 세그먼테이션과 두 개의 게재가 있는 크로스 채널 오케스트레이션 캠페인 예입니다. 이번 캠페인은 파리에 살면서 커피 자판기에 관심이 있는 모든 고객을 대상으로 한다. 이 모집단 중 일반 고객에게는 이메일이 전송되고 VIP 클라이언트에게는 SMS가 전송됩니다.

![](../assets/workflow-channel-example.png)

<!--
description, which use case you can perform (common other activities that you can link before of after the activity)

how to add and configure the activity

example of a configured activity within a workflow
The Email delivery activity allows you to configure the sending an email in a workflow. 

-->

매월 1일 오후 8시에 파리에 거주하는 모든 고객에게 개인화된 SMS를 전송하는 오케스트레이션된 반복 캠페인을 만들 수도 있습니다.

![](../assets/workflow-channel-example2.png)

<!-- Scheduled emails available?

This can be a single send email and sent just once, or it can be a recurring email.
* Single send emails are standard emails, sent once.
* Recurring emails allow you to send the same email multiple times to different targets over a defined period. You can aggregate the deliveries per period in order to get reports that correspond to your needs.

When linked to a scheduler, you can define recurring emails.
Email recipients are defined upstream of the activity in the same workflow, via an Audience targeting activity.

-->


<!--The message preparation is triggered according to the workflow execution parameters. From the message dashboard, you can select whether to request or not a manual confirmation to send the message (required by default). You can start the workflow manually or place a scheduler activity in the workflow to automate execution.-->
