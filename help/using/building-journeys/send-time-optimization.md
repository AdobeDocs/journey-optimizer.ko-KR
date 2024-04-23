---
solution: Journey Optimizer
product: journey optimizer
title: 전송 시간 최적화
description: 메시지에서 매개 변수 전송 시간 최적화를 사용하는 방법 알아보기
feature: Journeys, Activities, Email, Push, Send Time Optimization
topic: Content Management
role: User
level: Intermediate
keywords: 전송 시간, 전송, 메시지, 최적화, 여정, AI, 지능형
exl-id: ec604e91-4c7f-459c-b6ff-d825919e7181
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 26%

---

# 전송 시간 최적화{#send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="전송된 시간 최적화 정보"
>abstract="Adobe의 AI 서비스에서 제공하는 Adobe Journey Optimizer의 전송 시간 최적화 기능은 기록 열기와 클릭률을 기반으로 이메일 또는 푸시 메시지를 전송하는 최적의 시간을 예측하여 참여도를 극대화할 수 있습니다."

Adobe의 AI 서비스를 기반으로 하는 Adobe Journey Optimizer의 전송 시간 최적화 기능을 사용하면 이메일 또는 푸시 메시지를 보내는 가장 적합한 시간을 예측하여 과거의 열기 및 클릭률을 기반으로 참여를 극대화할 수 있습니다. 머신 러닝 모델을 사용하여 각 사용자에 대해 개인화된 전송 시간을 예약하여 메시지 열람률과 클릭률을 높일 수 있습니다.

전송 시간 최적화 모델은 Adobe Journey Optimizer 데이터를 수집하고 사용자 수준의 열기(이메일 및 푸시의 경우) 및 클릭(이메일의 경우) 비율을 확인하여 고객이 메시징에 가장 많이 참여할 가능성이 있는 시기를 결정합니다. 전송 시간 최적화를 사용하려면 정보에 입각한 권장 사항을 제공하기 위해 최소 1개월 이상의 메시지 추적 데이터가 필요합니다. 각 사용자에 대해 시스템은 다음 점수를 사용하여 최적의 시간을 자동으로 선택합니다.

* 참여를 극대화하기 위한 각 요일의 최적 시간
* 참여를 극대화하기 위한 가장 좋은 요일
* 참여를 극대화하기 위한 가장 좋은 요일 시간

모델은 채점이나 교육 중 어떤 것을 말하는지에 따라 다릅니다. 교육은 매주, 그 후 분기별로 실시됩니다. 채점은 처음에는 주별로, 그 다음에는 월별로 수행됩니다.

* 교육 - 점수를 매기는 데 사용되는 알고리즘 개발
* 채점 - 훈련된 모델을 기반으로 개별 프로필에 점수 적용

이 정보는 사용자의 프로필과 함께 저장되며 여정 실행 시 참조되어 Adobe Journey Optimizer에 메시지를 보낼 시기를 알립니다.

## 전송 시간 최적화 활성화{#activate-send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_email"
>title="전송 시간 최적화 활성화"
>abstract="적절한 라디오 버튼을 선택하여 이메일 열람수 또는 이메일 클릭스루를 최적화할지 여부를 선택합니다. 다음 옵션에서 전송 값을 입력하여 시스템에서 사용하는 전송 시간을 괄호로 묶도록 선택할 수도 있습니다."

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_push"
>title="전송 시간 최적화 활성화"
>abstract="클릭수는 푸시 메시지에 적용할 수 없으므로 푸시 메시지의 기본값은 열람수 옵션으로 설정됩니다. 다음 옵션에서 전송 값을 입력하여 시스템에서 사용하는 전송 시간을 괄호로 묶도록 선택할 수도 있습니다."

다음을 선택하여 이메일 또는 푸시 메시지에서 전송 시간 최적화 활성화 **전송 시간 최적화** 활동 매개 변수에서 전환합니다.

![](../building-journeys/assets/jo-message5.png)

이메일 메시지의 경우 적절한 라디오 버튼을 선택하여 이메일 열기에서 최적화할지 이메일 클릭스루에서 최적화할지 여부를 선택합니다. 푸시 메시지에 클릭 수를 적용할 수 없으므로 푸시 메시지는 기본적으로 열기 옵션으로 설정됩니다.

에 대한 값을 입력하여 시스템에서 사용하는 전송 시간의 대괄호를 지정하도록 선택할 수도 있습니다. **다음 날짜 이내에 전송** 옵션을 선택합니다. &quot;6시간&quot;을 값으로 선택하면 [!DNL Journey Optimizer] 은(는) 각 사용자 프로필을 확인하고 여정 실행 시간으로부터 6시간 이내에 최적의 전송 시간을 선택합니다.
