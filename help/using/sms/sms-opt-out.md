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
source-git-commit: d1c11881654580247e8d7c92237cad130f11f749
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---

# SMS 옵트아웃 관리 {#sms-opt-out}

업계 표준 및 규정에 따라 모든 SMS 마케팅 메시지에는 수신자가 간편하게 구독을 취소할 수 있는 방법이 포함되어야 합니다. [개인 정보 및 옵트아웃 관리에 대해 자세히 알아보십시오](../privacy/opt-out.md)

기본적으로 Adobe Journey Optimizer는 Sinch 및 Twilio와 같은 기본 통합을 위한 업계 표준에 따라 무료 및 긴 코드 메시지에 대해 STOP, UNSTOP 및 START와 같은 표준 영어 회신 메시지를 처리합니다. 이러한 키워드는 일반적으로 타사 공급자로부터 자동 표준 응답을 트리거합니다(예: Twilio, Sinch 등). 공급자나 설명서 사이트를 통해 직접 확인할 수 있습니다.

SMS 옵트아웃 기능이 Adobe Journey Optimizer에서 키워드 응답 STOP, UNSTOP 및 START가 자동으로 인식되도록 하는 단계는 필요하지 않습니다.

Adobe Journey Optimizer가 옵트아웃 상태(Twilio 또는 Sinch와의 직접 통합을 위해)를 기반으로 전송을 중지하는 것 외에도 대부분의 SMS 게이트웨이 공급업체는 차단 목록을 유지 관리하여 옵트아웃을 선택한 개인에게 SMS 메시지가 전달되지 않도록 합니다. Sinch 또는 Twilio 이외의 공급자를 사용하여 SMS를 전송하는 경우 [사용자 지정 채널](../building-journeys/using-custom-actions.md)를 채울 때는 공급자에게 확인해야 합니다.

>[!IMPORTANT]
>
>텍스트 메시지 캠페인에는 텍스트 메시지 캠페인의 특성, 텍스트 메시지를 보내는 위치 및 수신자의 위치에 따라 다양한 법적 준수 요구 사항이 적용될 수 있습니다. <br>Adobe Journey Optimizer는 위에서 설명한 것처럼 긴 코드 및 무료 전화번호에 대한 메시지를 처리하지만, 텍스트 메시지 캠페인이 적용 가능한 모든 법적 준수 요구 사항을 준수하는지 확인하려면 법률 자문을 구해야 합니다.

## 짧은 코드 {#short-codes}

기본적으로 Adobe Journey Optimizer는 짧은 코드 번호에 대한 옵트아웃, 옵트인 또는 도움말 키워드를 처리하지 않습니다.

짧은 코드가 옵트아웃 처리를 위한 모든 업계 규칙 및 규정을 준수하는지 확인해야 합니다.

## 영숫자 보낸 사람 ID {#alphanumeric}

영숫자 보낸 사람 ID는 단방향 메시징용이며 인바운드 메시지를 받을 수 없습니다. 따라서 Adobe Journey Optimizer의 SMS STOP, START, HELP 키워드는 알파 발신자 ID에 적용할 수 없습니다. 사용자가 영숫자 보낸 사람 ID를 통해 보낸 메시지에서 옵트아웃할 수 있도록 지원 팀에 쓰기, 지원 전화선 호출, 다른 전화 번호 또는 코드 문자 보내기 등의 다른 지침을 제공해야 합니다.

## 비디오 {#video-sms}

SMS에 대한 기본 인바운드 키워드 지원(START, STOP 및 UNSTOP)이 작동하는 방식에 대한 자세한 내용은 다음 비디오를 참조하십시오.

>[!VIDEO](https://video.tv.adobe.com/v/344026?quality=12)
