---
solution: Journey Optimizer
product: journey optimizer
title: 여정에 메시지 추가
description: 여정에 메시지를 추가하는 방법 알아보기
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 4db07a9e-c3dd-4873-8bd9-ac34c860694c
source-git-commit: 0b19af568b33d29f4b35deeab6def17919cfe824
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 18%

---

# 이메일, SMS, 푸시{#add-a-message-in-a-journey}

[!DNL Journey Optimizer] 에는 기본 제공 메시지 기능이 포함되어 있습니다. 여정에 푸시, SMS 또는 이메일 메시지 활동 및 [설정 및 콘텐츠 정의](../messages/messages-in-journeys.md). 그런 다음 여정 컨텍스트에서 실행됩니다.

특정 작업을 설정하여 메시지를 보낼 수도 있습니다.

* 서드파티 시스템을 사용하여 메시지를 전송하는 경우 사용자 지정 작업을 만들 수 있습니다. 자세한 내용 [섹션](../action/action.md).

* Campaign과 Journey Optimizer을 함께 사용하는 경우 다음 섹션을 참조하십시오.

   * [[!DNL Journey Optimizer] 및 Campaign Classic v7/Campaign v8](../action/acc-action.md)
   * [[!DNL Journey Optimizer] 및 Campaign Standard](../action/acs-action.md)

여정에 메시지를 추가하려면 아래 단계를 따르십시오.

1. [이벤트](general-events.md) 또는 [세그먼트 읽기](read-segment.md) 활동으로 여정을 시작하십시오.

1. 팔레트의 **작업** 섹션에서 **이메일**, **SMS** 또는 **푸시** 활동을 캔버스로 드래그하여 놓습니다.

   ![](../messages/assets/add-a-message.png)


   메시지를 구성하고 해당 컨텐츠를 정의하는 모든 단계는 [이 섹션](../messages/get-started-content.md).

## 라이브 콘텐츠 업데이트{#update-live-content}

라이브 여정에서 메시지(이메일, sms, 푸시)의 콘텐츠를 업데이트할 수 있습니다.

이렇게 하려면 라이브 여정을 열고 메시지 활동을 선택한 다음 을(를) 클릭합니다 **컨텐츠 편집**.

![](assets/add-a-message2.png)

하지만 개인화에 사용되는 속성이 프로필 속성이든 컨텍스트 데이터(이벤트 또는 여정 속성에서)이든 간에 변경할 수 없습니다.
