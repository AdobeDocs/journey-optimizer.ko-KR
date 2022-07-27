---
title: 전송 시간 최적화
description: 메시지에서 전송 시간 최적화를 매개 변수로 지정하는 방법을 알아봅니다
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: ec604e91-4c7f-459c-b6ff-d825919e7181
source-git-commit: b31eb2bcf52bb57aec8e145ad8e94790a1fb44bf
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 0%

---

## 전송 시간 최적화{#send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="전송 시간 최적화 기본 정보"
>abstract="Adobe의 AI 서비스를 기반으로 하는 Adobe Journey Optimizer의 전송 시간 최적화 기능은 이메일 또는 푸시 메시지를 보내는 최적의 시간을 예측하여 과거의 공개 및 클릭 비율에 따라 참여를 극대화할 수 있습니다."

Adobe의 AI 서비스를 기반으로 하는 Adobe Journey Optimizer의 전송 시간 최적화 기능은 이메일 또는 푸시 메시지를 보내는 최적의 시간을 예측하여 과거의 공개 및 클릭 비율에 따라 참여를 극대화할 수 있습니다. Adobe의 기계 학습 모델을 사용하여 각 사용자가 메시지의 오픈과 클릭률을 높일 수 있도록 개인화된 전송 시간을 예약할 수 있습니다.

Send-Time Optimization 모델은 Adobe Journey Optimizer 데이터를 수집하여 사용자 수준의 열기(이메일 및 푸시)를 확인하고 (이메일용) 비율을 확인하여 고객이 언제 메시지를 가장 많이 이용할 수 있는지 결정합니다. 전송 시간 최적화를 사용하려면 올바른 권장 사항을 제공하기 위해 최소 1개월의 메시지 추적 데이터가 필요합니다. 각 사용자에 대해 다음 점수를 사용하여 최적의 시간을 자동으로 선택합니다.

* 참여를 최대화하기 위해 매일 가장 적합한 시간
* 참여를 최대화하는 데 가장 적합한 요일
* 참여를 최대화하기 위한 최상의 요일 중 가장 적합한 시간

채점이냐 훈련이냐에따라 모델은 달라진다. 훈련은 처음에는 매주, 그 다음에는 분기별로 실시된다. 점수는 처음에는 매주, 그 다음에는 매월 입니다.

* 교육 - 점수를 매기는 데 사용되는 알고리즘 개발
* 점수 - 훈련된 모델을 기반으로 개별 프로필에 점수 적용

이 정보는 사용자의 프로필과 함께 저장되며 여정 실행 시 참조되어 Adobe Journey Optimizer에서 메시지를 보낼 시점을 알려줍니다.

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

또한, **다음 내 전송** 선택 사항입니다. &quot;6시간&quot;을 값으로 선택하면 [!DNL Journey Optimizer] 은(는) 각 사용자 프로필을 확인하고 여정 실행 시간에서 6시간 내에 최적의 전송 시간을 선택합니다.
