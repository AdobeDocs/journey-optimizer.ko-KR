---
solution: Journey Optimizer
product: journey optimizer
title: 여정에 기본 제공 채널 작업 추가
description: 여정에 기본 제공 채널 작업을 추가하는 방법 알아보기
feature: Journeys, Activities, Channels Activity
topic: Content Management
role: User
level: Intermediate
keywords: 여정, 메시지, 푸시, sms, 이메일, 인앱, 웹, 콘텐츠 카드, 코드 기반 경험
exl-id: 4db07a9e-c3dd-4873-8bd9-ac34c860694c
source-git-commit: 4c1908ad8022ff811537aa25be95db66a55882b4
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 18%

---

# 기본 제공 채널 작업 사용 {#add-a-message-in-a-journey}

>[!CONTEXTUALHELP]
>id="ajo_message_activity"
>title="기본 제공 채널 작업"
>abstract="Journey Optimizer에는 채널 작업 기능이 빌트인되어 있습니다. 여정에 아웃바운드(이메일, 문자 메시지(SMS/MMS), 푸시) 또는 인바운드(인앱, 웹, 코드 기반 경험, 콘텐츠 카드) 활동을 간단히 추가하고 설정과 콘텐츠를 정의할 수 있습니다. 그런 다음 여정의 맥락에서 자동으로 실행되고 전송됩니다."

[!DNL Journey Optimizer]에는 메시지를 보내는 데 사용되는 기본 제공 채널 작업 기능이 포함되어 있습니다. 프로필이 이 활동에 들어가면 메시지를 보냅니다.

기본 제공 채널 작업을 여정에 추가하려면 채널 활동을 끌어다 놓고 해당 설정 및 콘텐츠를 정의합니다. 그런 다음 여정의 맥락에서 자동으로 실행되고 전송됩니다.

>[!NOTE]
>
>사용자 지정 작업을 설정하여 메시지를 보낼 수도 있습니다. [자세히 알아보기](#recommendation)

## 여정에 메시지 추가  {#add-msg-in-journey}

기본 제공 채널 작업으로 아웃바운드 또는 인바운드 메시지를 구성할 수 있습니다. 지원되는 인바운드 채널은 이메일, 문자 메시지(SMS/MMS), 푸시 알림입니다. 지원되는 아웃바운드 채널은 인앱, 웹, 코드 기반 경험, 콘텐츠 카드입니다.

여정에 기본 제공 채널 작업을 추가하려면 아래 단계를 수행합니다.

1. [이벤트](general-events.md) 또는 [대상자 읽기](read-audience.md) 활동으로 여정을 시작하십시오.

1. 팔레트의 **작업** 섹션에서 채널 활동을 캔버스로 끌어서 놓습니다.

   ![](assets/journey-web-activity.png)


1. 활동을 구성합니다. 자세한 구성 지침은 아래 링크에서 확인할 수 있습니다.

   * 아웃바운드 작업을 만드는 자세한 단계를 다음과 같이 배웁니다.

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

     >[!NOTE]
     >
     >이메일 및 푸시 알림의 경우 전송 시간 최적화를 활성화할 수 있습니다. [자세히 알아보기](send-time-optimization.md)

   * 인바운드 작업을 생성하는 자세한 단계를 다음과 같이 알아보십시오.

     <table style="table-layout:fixed">
      <tr style="border: 0;">
      <td>
      <a href="../in-app/create-in-app.md">
      <img alt="리드" src="../assets/do-not-localize/in-app.jpg">
      </a>
      <div><a href="../in-app/create-in-app.md"><strong>인앱 메시지 만들기</strong>
      </div>
      <p>
      </td>
      <td>
      <a href="../web/create-web.md">
      <img alt="리드" src="../assets/do-not-localize/web-create.jpg">
      </a>
      <div><a href="../web/create-web.md"><strong>웹 경험 만들기</strong>
      </div>
      <p>
      </td>
      <td>
      <a href="../content-card/create-content-card.md">
      <img alt="리드" src="../assets/do-not-localize/sms-config.jpg">
      </a>
      <div><a href="../content-card/create-content-card.md"><strong>콘텐츠 카드 만들기</strong>
      </div>
      <p>
      </td>
      <td>
      <a href="../code-based/create-code-based.md">
      <img alt="드물게" src="../assets/do-not-localize/web-design.jpg">
      </a>
      <div>
      <a href="../code-based/create-code-based.md"><strong>코드 기반 경험 만들기<strong></a>
      </div>
      <p>
      </td>
      </tr>
      </table>

     >[!NOTE]
     >
     >각 인바운드 메시지 활동은 3일 **대기** 활동과 함께 제공됩니다. [자세히 알아보기](wait-activity.md#auto-wait-node)


## 라이브 콘텐츠 업데이트 {#update-live-content}

라이브 여정에서 기본 제공 채널 작업의 콘텐츠를 업데이트할 수 있습니다.

이렇게 하려면 라이브 여정을 열고 채널 활동을 선택한 다음 **콘텐츠 편집**&#x200B;을 클릭하세요.

![](assets/add-a-message2.png)

그러나 프로필 속성이든 컨텍스트 데이터(이벤트 또는 여정 속성)이든 간에 개인화에 사용되는 속성은 변경할 수 없습니다.

컨텍스트 데이터를 수정하면 다음 오류 메시지가 표시됩니다. `ERR_AUTHORING_JOURNEYVERSION_201`

프로필 속성을 수정하면 다음 오류 메시지가 표시됩니다. `ERR_AUTHORING_JOURNEYVERSION_202`

인앱 활동의 경우 여정이 라이브되는 동안 컨텐츠를 변경할 수 있지만 인앱 트리거는 수정할 수 없습니다.

## 사용자 지정 작업으로 보내기 {#recommendation}

기본 제공 메시지 기능을 사용하는 대신 사용자 지정 작업을 사용하여 메시지나 API 호출을 전송할 서드파티 시스템의 연결을 구성할 수 있습니다.

* 서드파티 시스템을 사용하여 메시지를 전송하는 경우 사용자 지정 작업을 만들 수 있습니다. [자세히 알아보기](../action/action.md)

* Adobe Campaign을 사용하여 작업하는 경우 다음 섹션을 참조하십시오.

   * [[!DNL Journey Optimizer] 및 Campaign v7/v8](../action/acc-action.md)
   * [[!DNL Journey Optimizer] 및 Campaign Standard](../action/acs-action.md)