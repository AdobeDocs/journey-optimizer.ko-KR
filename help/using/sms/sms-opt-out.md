---
solution: Journey Optimizer
product: journey optimizer
title: SMS 옵트아웃 관리
description: SMS 메시지로 옵트아웃을 관리하는 방법을 알아봅니다
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 59ea67d9-e90c-4ad0-afb9-d0e0fd868855
source-git-commit: 676e2d6788c8110b76a38e857a62ba9c1be5842c
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 45%

---

# SMS 옵트아웃 관리 {#sms-opt-out}

업계 표준 및 규정에 따라 모든 SMS 마케팅 메시지에는 수신자가 간편하게 구독을 취소할 수 있는 방법이 포함되어야 합니다. [개인 정보 및 옵트아웃 관리에 대해 자세히 알아보십시오](../privacy/opt-out.md)

>[!IMPORTANT]
>
>텍스트 메시지 통신에는 성격, 텍스트 메시지를 보내는 위치 및 수신자의 위치에 따라 다양한 법적 준수 요구 사항이 적용될 수 있습니다. Adobe Journey Optimizer이 긴 코드 및 무료 전화번호에 대한 메시지를 아래 자세히 설명하는 동안, 법률 자문을 통해 텍스트 메시지 통신이 적용 가능한 모든 법적 준수 요구 사항을 준수하는지 확인하십시오.

## 기본 인바운드 키워드{#sms-native-keywords}

기본적으로 Adobe Journey Optimizer은 Sinch 및 Twilio와 같은 기본적인 통합을 위한 업계 표준에 따라 수신자 부담 및 긴 코드 메시지에 대해 STOP, UNSTOP 및 START와 같은 표준 영문 회신 메시지를 처리합니다.

이러한 키워드는 일반적으로 타사 공급자로부터 자동 표준 응답을 트리거합니다(예: Twilio 또는 Sinch). 공급자나 설명서 사이트를 통해 직접 확인할 수 있습니다.

SMS 옵트아웃 기능이 키워드 응답 STOP, UNSTOP 및 START가 자동으로 인식되도록 Adobe Journey Optimizer에서 작동하도록 하는 단계는 필요하지 않습니다. 프로필 옵트아웃 상태는 Adobe Journey Optimizer에서 실시간으로 업데이트됩니다.


## 차단 목록{#sms-blocklists}

Adobe Journey Optimizer에서 옵트아웃 상태(Tilio 또는 Sinch와의 직접 통합을 위해)에 따라 전송을 중지하는 것 외에도 대부분의 SMS 게이트웨이 공급업체는 SMS 메시지가 옵트아웃하도록 선택한 개인에게 전달되지 않도록 하는차단 목록에 추가하다를 유지합니다. Sinch 또는 Twilio 이외의 공급자를 사용하고 SMS를 통해 보내는 경우 [사용자 지정 채널](../building-journeys/using-custom-actions.md)를 채울 때는 공급자에게 확인해야 합니다.


## 짧은 코드 {#short-codes}

기본적으로 Adobe Journey Optimizer은 짧은 코드 번호에 대한 옵트아웃, 옵트인 또는 도움말 키워드를 처리하지 않습니다. 짧은 코드가 옵트아웃 처리를 위한 모든 업계 규칙 및 규정을 준수하는지 확인해야 합니다.

## 영문과 숫자로 구성된 발신자 ID {#alphanumeric}

영문과 숫자로 구성된 발신자 ID는 단방향 통신 전용이며 인바운드 메시지를 받을 수 없습니다. 따라서 Adobe Journey Optimizer의 SMS STOP, START, HELP 키워드는 Alpha Sender ID에 적용할 수 없습니다. 사용자가 영문과 숫자로 구성된 발신자 ID를 통해 발송된 메시지를 거부할 수 있도록 지원 팀에 문의하거나, 지원 팀에 전화하거나, 다른 전화 번호 또는 코드를 문자로 보내는 등의 다른 지침을 제공해야 합니다.

## 비디오 {#video-sms}

기본 인바운드 키워드 지원(START, STOP 및 UNSTOP)이 SMS에서 작동하는 방법에 대한 자세한 내용은 다음 영상을 참조하십시오:

>[!VIDEO](https://video.tv.adobe.com/v/344026?quality=12)
