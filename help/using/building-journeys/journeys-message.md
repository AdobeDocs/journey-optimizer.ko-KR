---
solution: Journey Optimizer
product: journey optimizer
title: 여정에서 메시지 추가
description: 여정에서 메시지를 추가하는 방법 알아보기
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 4db07a9e-c3dd-4873-8bd9-ac34c860694c
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 0%

---

# 이메일, SMS, 푸시{#add-a-message-in-a-journey}

[!DNL Journey Optimizer] 에는 기본 제공 메시지 기능이 포함되어 있습니다. 여정에서 푸시, SMS 또는 이메일 메시지 활동을 추가하고 설정 및 콘텐츠를 정의할 수 있습니다. 그런 다음 실행되어 여정의 컨텍스트에서 전송됩니다.

특정 작업을 설정하여 메시지를 보낼 수도 있습니다.

* 서드파티 시스템을 사용하여 메시지를 전송하는 경우 사용자 지정 작업을 만들 수 있습니다. 자세한 내용 [섹션](../action/action.md).

* Campaign과 Journey Optimizer를 함께 사용하는 경우 다음 섹션을 참조하십시오.

   * [[!DNL Journey Optimizer] 및 Campaign Classic v7/Campaign v8](../action/acc-action.md)
   * [[!DNL Journey Optimizer] 및 Campaign Standard](../action/acs-action.md)

여정에서 메시지를 추가하려면 아래 단계를 수행하십시오.

1. 을(를) 통해 여정 시작 [이벤트](general-events.md) 또는 [세그먼트 읽기](read-segment.md) 활동.

1. 에서 **작업** 팔레트의 섹션에서 **이메일**, **SMS** 또는 **푸시** 활동을 캔버스로 이동합니다.

1. 활동을 구성합니다. 다음 페이지에서 메시지 콘텐츠를 만드는 자세한 단계를 배웁니다.

   <table style="table-layout:fixed">
   <tr style="border: 0;">
   <td>
   <a href="../email/create-email.md">
   <img alt="리드" src="../assets/do-not-localize/email.jpg">
   </a>
   <div><a href="../email/create-email.md"><strong>이메일 만들기</strong>
   </div>
   <p>
   </td>
   <td>
   <a href="../push/create-push.md">
   <img alt="자주" src="../assets/do-not-localize/push.jpg">
   </a>
   <div>
   <a href="../push/create-push.md"><strong>푸시 알림 만들기<strong></a>
   </div>
   <p>
   </td>
   <td>
   <a href="../sms/create-sms.md">
   <img alt="유효성 검사" src="../assets/do-not-localize/sms.jpg">
   </a>
   <div>
   <a href="../sms/create-sms.md"><strong>SMS 메시지 만들기</strong></a>
   </div>
   <p>
   </td>
   </tr>
   </table>

## 라이브 콘텐츠 업데이트{#update-live-content}

라이브 여정에서 메시지(이메일, sms, 푸시)의 콘텐츠를 업데이트할 수 있습니다.

이렇게 하려면 라이브 여정을 열고 메시지 활동을 선택한 다음 을(를) 클릭합니다 **컨텐츠 편집**.

![](assets/add-a-message2.png)

하지만 개인화에 사용되는 속성이 프로필 속성이든 컨텍스트 데이터(이벤트 또는 여정 속성)이든 변경할 수 없습니다.

## 전송 시간 최적화{#send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="전송 시간 최적화 기본 정보"
>abstract="Adobe의 AI 서비스를 기반으로 하는 Adobe Journey Optimizer의 전송 시간 최적화 기능은 이메일 또는 푸시 메시지를 보내는 최적의 시간을 예측하여 과거의 열기 및 클릭 비율에 따라 참여를 극대화할 수 있습니다."

### 전송 시간 최적화 기본 정보 {#about-send-time}

Adobe의 AI 서비스를 기반으로 하는 Adobe Journey Optimizer의 전송 시간 최적화 기능은 이메일 또는 푸시 메시지를 보내는 최적의 시간을 예측하여 과거의 열기 및 클릭 비율에 따라 참여를 극대화할 수 있습니다. Adobe의 기계 학습 모델을 사용하여 각 사용자가 메시지의 오픈과 클릭률을 높일 수 있도록 개인화된 전송 시간을 예약할 수 있습니다.

Send-Time Optimization 모델은 Adobe Journey Optimizer 데이터를 수집하여 사용자 수준 열기(이메일 및 푸시)를 확인하고 (이메일용) 비율을 클릭하여 고객이 메시지를 가장 많이 이용할 수 있는 시기를 결정합니다. 전송 시간 최적화를 사용하려면 올바른 권장 사항을 제공하기 위해 최소 1개월의 메시지 추적 데이터가 필요합니다. 각 사용자에 대해 다음 점수를 사용하여 최적의 시간을 자동으로 선택합니다.

* 참여를 최대화하기 위해 매일 가장 적합한 시간
* 참여를 최대화하는 데 가장 적합한 요일
* 참여를 최대화하기 위한 최상의 요일 중 가장 적합한 시간

채점이냐 훈련이냐에따라 모델은 달라진다. 훈련은 처음에는 매주, 그 다음에는 분기별로 실시된다. 점수는 처음에는 매주, 그 다음에는 매월 입니다.

* 교육 - 점수를 매기는 데 사용되는 알고리즘 개발
* 점수 - 훈련된 모델을 기반으로 개별 프로필에 점수 적용

이 정보는 사용자 프로필과 함께 저장되며 경로 실행 시 참조되어 Adobe Journey Optimizer에서 메시지를 보낼 시기를 알려줍니다.

>[!CAUTION]
>
>이 기능은 버스트 모드와 호환되지 않습니다.

### 전송 시간 최적화 활성화{#activate-send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_email"
>title="전송 시간 최적화 활성화"
>abstract="적절한 라디오 단추를 선택하여 이메일 열기 또는 이메일 클릭스루를 최적화할지 여부를 선택합니다. 다음 옵션 내에 전송 을 위한 값을 입력하여 시스템에서 사용하는 전송 시간을 대괄적으로 설정할 수도 있습니다."

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_push"
>title="전송 시간 최적화 활성화"
>abstract="푸시 메시지는 푸시 메시지에 클릭을 적용할 수 없으므로 기본적으로 열기 옵션으로 설정됩니다. 다음 옵션 내에 전송 을 위한 값을 입력하여 시스템에서 사용하는 전송 시간을 대괄적으로 설정할 수도 있습니다."

을(를) 선택하여 이메일 또는 푸시 메시지에 대한 전송 시간 최적화를 활성화합니다 **전송 시간 최적화** 활동 매개 변수에서 전환합니다.

![](../building-journeys/assets/jo-message5.png)

이메일 메시지의 경우 해당 라디오 단추를 선택하여 이메일 열기 또는 이메일 클릭스루를 최적화할지 여부를 선택합니다. 푸시 메시지는 푸시 메시지에 클릭을 적용할 수 없으므로 기본적으로 열기 옵션으로 설정됩니다.

또한, **다음 내 전송** 선택 사항입니다. &quot;6시간&quot;을 값으로 선택하면 [!DNL Journey Optimizer] 은(는) 각 사용자 프로필을 확인하고 경로 실행 시간으로부터 6시간 이내에 최적의 전송 시간을 선택합니다.
