---
solution: Journey Optimizer
product: journey optimizer
title: 텍스트 메시지에 대한 옵트아웃 관리
description: SMS/MMS 메시지로 옵트아웃을 관리하는 방법 알아보기
feature: SMS
topic: Content Management
role: User
level: Intermediate
exl-id: 59ea67d9-e90c-4ad0-afb9-d0e0fd868855
source-git-commit: 478706e893354d59be5d2010da84546aa4385d99
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 18%

---

# 텍스트 메시지에 대한 옵트아웃 관리 {#sms-opt-out}

업계 표준 및 규정에 따라 모든 SMS 마케팅 메시지에는 수신자가 간편하게 구독을 취소할 수 있는 방법이 포함되어야 합니다. [개인 정보 및 옵트아웃 관리에 대해 자세히 알아보기](../privacy/opt-out.md)

>[!IMPORTANT]
>
>문자 메시지 통신은 문자 메시지의 특성, 문자 메시지를 보내는 위치 및 받는 사람의 위치에 따라 다양한 법적 준수 요구 사항이 적용될 수 있습니다. Adobe Journey Optimizer은 아래 자세히 설명된 대로 짧은 코드, 긴 코드 및 수신자 부담 전화번호에 대한 메시지를 처리하지만, 귀하의 문자 메시지 통신이 적용 가능한 모든 법적 준수 요구 사항을 준수하는지 확인하려면 법률적인 자문을 구하십시오.
>

## 기본 인바운드 키워드 {#sms-native-keywords}

>[!NOTE]
>
> Journey Optimizer과 함께 사용할 경우 Sinch 및 Infobip만 기본 키워드를 지원합니다.

기본적으로 Adobe Journey Optimizer은 짧은 코드, 수신자 부담 및 긴 코드 메시지에 대해 다음과 같은 표준 영문 회신 메시지를 처리합니다.

* **옵트아웃**: 중지, 종료, 취소, 종료, 구독 취소, 아니요.
* **옵트인**: 구독, 예, 중지 취소, 시작, 계속, 다시 시작, 시작.
* **도움말**: 도움말.

이러한 키워드는 일반적으로 서드파티 공급자로부터 자동 표준 응답을 트리거합니다. 공급자나 설명서 사이트를 통해 직접 확인할 수 있습니다.

Infobip을 사용할 때 전달 작업이 끌어오기 구성으로 설정되어 있는지 확인합니다.

키워드 응답 STOP, UNSTOP, START, QUIT, CANCEL, END 및 UNSUBSCRIBE가 자동으로 인식되므로, Adobe Journey Optimizer에서 SMS 옵트아웃 기능이 작동하는지 확인하는 데는 단계가 필요하지 않습니다. 프로필 옵트아웃 상태는 Adobe Journey Optimizer에서 실시간으로 업데이트됩니다.

고객이 텍스트 메시지에 대해 STOP에 응답하면, 공급자는 트랜잭션 메시지를 포함하여 해당 특정 발신자 ID(짧은 코드 또는 긴 번호)에서 모든 후속 SMS를 차단합니다. 트랜잭션 SMS를 중단 없이 게재하려면 이전에 옵트아웃되지 않은 별도의 발신자 ID를 사용하십시오.

## 차단 목록 {#sms-blocklists}

Adobe Journey Optimizer에서 옵트아웃 상태(Twilio, Infoip 또는 Sinch와의 직접 통합을 위해)에 따라 전송을 중지하는 것 외에도 대부분의 SMS 게이트웨이 공급자는 SMS 메시지가 옵트아웃을 선택한 개인에게 전달되지 않도록 하는 차단 목록에 추가하다도 유지 관리합니다. Sinch 또는 Twilio 이외의 공급자를 사용하고 [사용자 지정 채널](../building-journeys/using-custom-actions.md)을 통해 SMS를 전송하는 경우 공급자에게 확인해야 합니다.


## 짧은 코드 {#short-codes}

기본적으로 짧은 코드 번호에 대한 옵트인 또는 도움말 키워드는 Adobe Journey Optimizer에서 처리되지 않습니다. 옵트아웃 처리에 대한 업계 규정 및 규칙을 준수하려면 짧은 코드가 모든 지침을 준수하는지 확인하는 것이 중요합니다.

하지만 Journey Optimizer에서는 다른 발신자 ID를 가진 수신 키워드를 기반으로 전역 옵트아웃을 지원합니다.

## 영문과 숫자로 구성된 발신자 ID {#alphanumeric}

영문과 숫자로 구성된 발신자 ID는 단방향 통신 전용이며 인바운드 메시지를 받을 수 없습니다. 따라서 Adobe Journey Optimizer의 SMS STOP, START, HELP 키워드는 Alpha 발신자 ID에 적용할 수 없습니다. 사용자가 영문과 숫자로 구성된 발신자 ID를 통해 발송된 메시지를 거부할 수 있도록 지원 팀에 문의하거나, 지원 팀에 전화하거나, 다른 전화 번호 또는 코드를 문자로 보내는 등의 다른 지침을 제공해야 합니다.

## 비디오 {#video-sms}

* 아래 비디오에서는 SMS에 대한 이중 옵트인을 구성하는 방법을 알아봅니다.

+++ 비디오 보기

  >[!VIDEO](https://video.tv.adobe.com/v/3427129/?learn=on)

+++
