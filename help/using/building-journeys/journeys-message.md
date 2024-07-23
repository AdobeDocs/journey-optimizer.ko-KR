---
solution: Journey Optimizer
product: journey optimizer
title: 여정에 메시지 추가
description: 여정에 메시지를 추가하는 방법 알아보기
feature: Journeys, Activities, Channels Activity
topic: Content Management
role: User
level: Intermediate
keywords: 여정, 메시지, 푸시, sms, 이메일, 인앱
exl-id: 4db07a9e-c3dd-4873-8bd9-ac34c860694c
source-git-commit: 2c4c9064b11bce44331b6604c91221ba9829eff7
workflow-type: tm+mt
source-wordcount: '1177'
ht-degree: 17%

---

# 이메일, 인앱, 푸시 및 문자 메시지 보내기 {#add-a-message-in-a-journey}

>[!CONTEXTUALHELP]
>id="ajo_message_activity"
>title="메시지 활동"
>abstract="Journey Optimizer에는 메시지 기능이 내장되어 있습니다. 여정에 푸시, 문자 메시지(SMS/MMS), 인앱 또는 이메일 메시지 활동을 추가하고 설정과 콘텐츠를 정의하기만 하면 됩니다. 그런 다음 여정의 맥락에서 자동으로 실행되고 전송됩니다."

[!DNL Journey Optimizer]에는 기본 메시지 기능이 포함되어 있습니다. 푸시, SMS/MMS, 인앱 또는 이메일 메시지 활동을 여정에 추가하고 설정 및 콘텐츠를 정의할 수 있습니다. 그런 다음 여정의 맥락에서 자동으로 실행되고 전송됩니다.

메시지를 보내기 위한 특정 작업을 설정할 수도 있습니다.

* 서드파티 시스템을 사용하여 메시지를 전송하는 경우 사용자 지정 작업을 만들 수 있습니다. 이 [섹션](../action/action.md)에서 자세히 알아보세요.

* Campaign과 Journey Optimizer을 함께 사용하는 경우 다음 섹션을 참조하십시오.

   * [[!DNL Journey Optimizer] 및 Campaign v7/v8](../action/acc-action.md)
   * [[!DNL Journey Optimizer] 및 Campaign Standard](../action/acs-action.md)

여정에 메시지를 추가하려면 아래 단계를 수행합니다.

1. [이벤트](general-events.md) 또는 [대상자 읽기](read-audience.md) 활동으로 여정을 시작하십시오.

1. 팔레트의 **작업** 섹션에서 **이메일**, **인앱**, **SMS** 또는 **푸시** 활동을 캔버스로 드래그하여 놓습니다.

1. 활동을 구성합니다. 다음 페이지에서 메시지 콘텐츠를 만드는 자세한 단계를 배웁니다.

   <table style="table-layout:fixed">
   <tr style="border: 0;">
   <td>
   <a href="../email/create-email.md">
   <img alt="리드" src="../assets/do-not-localize/email.jpg">
   </a>
   <div><a href="../email/create-email.md"><strong>이메일 작성</strong>
   </div>
   <p>
   </td>
   <td>
   <a href="../in-app/create-in-app.md">
   <img alt="리드" src="../assets/do-not-localize/in-app.jpg">
   </a>
   <div><a href="../in-app/create-in-app.md"><strong>인앱 메시지 만들기</strong>
   </div>
   <p>
   </td>
   <td>
   <a href="../push/create-push.md">
   <img alt="드물게" src="../assets/do-not-localize/push.jpg">
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
   <a href="../sms/create-sms.md"><strong>문자 메시지(SMS/MMS) 만들기</strong></a>
   </div>
   <p>
   </td>
   </tr>
   </table>

## 라이브 콘텐츠 업데이트{#update-live-content}

라이브 여정에서 메시지 콘텐츠(이메일, 인앱, 푸시, SMS)를 업데이트할 수 있습니다.

이렇게 하려면 라이브 여정을 열고 메시지 활동을 선택한 다음 **콘텐츠 편집**&#x200B;을 클릭하세요.

![](assets/add-a-message2.png)

그러나 프로필 속성이든 컨텍스트 데이터(이벤트 또는 여정 속성)이든 간에 개인화에 사용되는 속성은 변경할 수 없습니다.

컨텍스트 데이터를 수정하면 다음 오류 메시지가 표시됩니다. ERR_AUTHORING_JOURNEYVERSION_201

프로필 속성을 수정하면 다음 오류 메시지가 표시됩니다. ERR_AUTHORING_JOURNEYVERSION_202

인앱 활동의 경우 여정이 라이브되는 동안 컨텐츠를 변경할 수 있지만 인앱 트리거는 수정할 수 없습니다.

## 전송 시간 최적화{#send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="전송된 시간 최적화 정보"
>abstract="Adobe의 AI 서비스에서 제공하는 Adobe Journey Optimizer의 전송 시간 최적화 기능은 기록 열기와 클릭률을 기반으로 이메일 또는 푸시 메시지를 전송하는 최적의 시간을 예측하여 참여도를 극대화할 수 있습니다."

>[!NOTE]
>
>이 기능은 기본적으로 활성화되어 있지 않습니다. Adobe 담당자에게 연락하여 활성화할 수 있습니다.

### 전송 시간 최적화 정보 {#about-send-time}

Adobe의 AI 서비스를 기반으로 하는 Adobe Journey Optimizer의 전송 시간 최적화 기능을 사용하면 이메일 또는 푸시 메시지를 보내는 가장 적합한 시간을 예측하여 과거의 열기 및 클릭률을 기반으로 참여를 극대화할 수 있습니다. 머신 러닝 모델을 사용하여 각 사용자에 대해 개인화된 전송 시간을 예약하여 메시지 열람률과 클릭률을 높일 수 있습니다.

전송 시간 최적화 모델은 Adobe Journey Optimizer 데이터를 수집하고 사용자 수준의 열기(이메일 및 푸시의 경우) 및 클릭(이메일의 경우) 비율을 확인하여 고객이 메시징에 가장 많이 참여할 가능성이 있는 시기를 결정합니다. 전송 시간 최적화를 사용하려면 정보에 입각한 권장 사항을 제공하기 위해 최소 1개월 이상의 메시지 추적 데이터가 필요합니다. 각 사용자에 대해 시스템은 다음 점수를 사용하여 최적의 시간을 자동으로 선택합니다.

* 참여를 극대화하기 위한 각 요일의 최적 시간
* 참여를 극대화하기 위한 가장 좋은 요일
* 참여를 극대화하기 위한 가장 좋은 요일 시간

모델은 채점이나 교육 중 어떤 것을 말하는지에 따라 다릅니다. 교육은 매주, 그 후 분기별로 실시됩니다. 채점은 처음에는 주별로, 그 다음에는 월별로 수행됩니다.

* 교육 - 점수를 매기는 데 사용되는 알고리즘 개발
* 채점 - 훈련된 모델을 기반으로 개별 프로필에 점수 적용

이 정보는 사용자의 프로필과 함께 저장되며 여정 실행 시 참조되어 Adobe Journey Optimizer에 메시지를 보낼 시기를 알립니다.

### 자주 묻는 질문 {#faq-send-time}

+++ 전송 시간 최적화는 어떤 작업을 수행할 수 있습니까? 새 프로필을 어떻게 처리합니까? 전송이 6/12/24시간 동안 분할됩니까?

전송 시간 최적화 는 고객과 소통하기 위한 최적의 시간을 예측하고 이메일 열기/클릭률을 최적화하려고 합니다. 점수는 각 프로필에 대해 `3*7*24` 특성 형식입니다. `7*24` 특성은 받는 사람에게 전자 메일을 보내는 가장 적합한 예상 시간의 순위를 설명하며, 3은 전자 메일 열기 비율, 전자 메일 클릭 비율 및 푸시 열기 비율을 최적화하기 위한 것입니다.

+++

+++각 프로필의 예상 전송 시간은 어디에서 볼 수 있습니까?

**프로필** 인터페이스에서 전체 점수를 볼 수 있습니다. 세 세트의 168개의 점수 각각에 대해, 그 등급은 -83에서 84로 올라간다. 순위가 높을수록 수신자와 상호 작용하기 위해 더 좋은 시간을 선택하였다. 여정의 시작 및 기간을 정의할 수 있으므로 최상의 순위(84)는 해당 시간 범위에 포함되지 않을 수 있습니다. 이 경우 등급 값이 가장 높은 시간을 선택하는 것이 좋습니다.

+++


+++어떤 보고를 사용할 수 있습니까?

여정에 액세스하여 오른쪽 상단의 **보고서 보기** 버튼을 클릭하고 왼쪽의 **여정** 탭을 선택합니다. [자세히 보기](../reports/journey-global-report.md)

+++

+++전송 시간 최적화 데이터가 프로필 풍부성에 어떤 영향을 줍니까?

전송 시간 최적화는 각 프로필에 점수/속성을 추가하지만 새 프로필은 만들어지지 않습니다.

+++

### 전송 시간 최적화 활성화{#activate-send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_email"
>title="전송 시간 최적화 활성화"
>abstract="적절한 라디오 버튼을 선택하여 이메일 열람수 또는 이메일 클릭스루를 최적화할지 여부를 선택합니다. 다음 옵션에서 전송 값을 입력하여 시스템에서 사용하는 전송 시간을 괄호로 묶도록 선택할 수도 있습니다."

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_push"
>title="전송 시간 최적화 활성화"
>abstract="클릭수는 푸시 메시지에 적용할 수 없으므로 푸시 메시지의 기본값은 열람수 옵션으로 설정됩니다. 다음 옵션에서 전송 값을 입력하여 시스템에서 사용하는 전송 시간을 괄호로 묶도록 선택할 수도 있습니다."

활동 매개 변수에서 **전송 시간 최적화** 스위치를 선택하여 이메일 또는 푸시 메시지에서 전송 시간 최적화를 사용하도록 설정합니다.

![](../building-journeys/assets/jo-message5.png)

이메일 메시지의 경우 적절한 라디오 버튼을 선택하여 이메일 열기에서 최적화할지 이메일 클릭스루에서 최적화할지 여부를 선택합니다. 푸시 메시지에 클릭 수를 적용할 수 없으므로 푸시 메시지는 기본적으로 열기 옵션으로 설정됩니다.

**다음** 옵션 내에 보내기 값을 입력하여 시스템에서 사용하는 전송 시간의 대괄호로 묶도록 선택할 수도 있습니다. &quot;6시간&quot;을 값으로 선택하면 [!DNL Journey Optimizer]이(가) 각 사용자 프로필을 확인하고 여정 실행 시간으로부터 6시간 내에 최적의 전송 시간을 선택합니다.

**최적의 시간이 창 밖에 있으면 어떻게 됩니까?**

다음 설정에 대한 예를 살펴보겠습니다.

* 클릭 시 최적화
* 작업은 오전 10시에 시작해야 합니다.
* 기간은 3시간입니다.

프로파일은 창 밖의 최적의 열기 시간을 가질 수 있습니다. 예를 들어 John이 클릭할 때 열리는 최적의 시간은 오후 5시입니다.

프로필 수준에서 한 주의 매시간 점수가 있습니다. 이 예에서는 이메일이 항상 창 내에서 전송됩니다. 런타임에 시스템은 해당 창(오전 10시부터 시작되는 3시간 창) 내의 점수 목록을 확인합니다. 그 후 시스템은 10, 11, 정오에 대한 점수를 비교하고 가장 높은 점수를 선택한다. 해당 시점에 이메일이 발송됩니다.
