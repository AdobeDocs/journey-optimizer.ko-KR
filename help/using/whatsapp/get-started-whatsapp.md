---
solution: Journey Optimizer
product: journey optimizer
title: WhatsApp 메시지 시작
description: Journey Optimizer에서 WhatsApp 메시지를 만들고 보내는 방법 알아보기
feature: Whatsapp
topic: Content Management
role: User
level: Beginner
exl-id: 22df2bfa-4d86-464e-ad83-3aa457e3a747
source-git-commit: 73a347c104fe28799c264f9a8b6c3e5e12c8d892
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 91%

---

# WhatsApp 메시지 시작 {#get-started-whatsapp}

이제 Meta의 [Cloud API](https://developers.facebook.com/docs/whatsapp/cloud-api/)를 통해 Journey Optimizer에서 직접 WhatsApp 메시지를 보낼 수 있습니다. 이 기능을 사용하면 WhatsApp을 여정 및 캠페인에 원활하게 통합하여 수신자와의 소통과 교류를 향상시킬 수 있습니다.

* **여정**&#x200B;에서 만들기. 여정을 만들고, **WhatsApp** 활동을 추가하고, 기본 설정을 정의한 다음 **[!UICONTROL 작업: WhatsApp]** 오른쪽 창으로 이동하여 WhatsApp 메시지의 콘텐츠를 만들 수 있습니다. [이 페이지](../building-journeys/journey-gs.md)에서 여정을 만드는 방법을 알아보십시오.

* **캠페인**&#x200B;에서 만들기. 캠페인을 만들고 **WhatsApp**&#x200B;을 작업으로 선택하고 기본 설정을 정의한 다음 메시지 콘텐츠를 편집하여 보낼 WhatsApp 메시지를 정의합니다. [작업 캠페인](../campaigns/campaign-action.md#action-campaign-action)을 만드는 방법을 알아봅니다. | [API 트리거 캠페인](../campaigns/api-triggered-campaigns.md) | [오케스트레이션된 캠페인](../orchestrated/create-orchestrated-campaign.md#create)

![](assets/do-not-localize/whatsapp-beta.png){zoomable="yes"}

## 사전 요구 사항 {#prereq}

WhatsApp을 Journey Optimizer와 통합하려면 다음 항목이 필요합니다.

* Meta Business Manager 계정
* [보낸 사람 이름과 전화 번호가 확인된 WhatsApp 비즈니스 계정](https://developers.facebook.com/docs/whatsapp/overview/business-accounts/)
* [적절한 권한이 있는 사용자 인증 토큰](https://developers.facebook.com/blog/post/2022/12/05/auth-tokens/)
* [승인된 Meta 템플릿](https://developers.facebook.com/docs/whatsapp/message-templates/guidelines/)

또한 통합을 진행하기 전에 다음 사항을 알고 있어야 합니다.

* [WhatsApp 콘텐츠 규칙](https://www.whatsapp.com/legal/messaging-guidelines)
* [Meta 정책 준수](https://www.whatsapp.com/legal)
* [24시간 대화 제한](https://developers.facebook.com/docs/whatsapp/messaging-limits/)

## 제한 사항 {#limitations}

WhatsApp 채널에는 다음 제한 사항이 적용됩니다.

* Adobe Journey Optimizer의 WhatsApp 채널은 HIPAA 준수를 대비한 채널이지만 제3자 공급업체는 Adobe의 BAA에 포함되지 않습니다. 자체 규정 준수 및 공급업체 유효성 검사에 대한 책임은 고객에게 있습니다.

* 자동 또는 사전 준비된 응답 메시지는 아직 지원되지 않습니다.

* 2025년 4월부터 미국 전화번호(+1 국가 코드와 미국 지역 번호로 구성된 번호)가 있는 WhatsApp 사용자에 대한 모든 마케팅 템플릿 메시지 게재가 일시적으로 중단되었습니다. [Meta 설명서에서 자세히 알아보기](https://developers.facebook.com/docs/whatsapp/cloud-api/guides/send-message-templates#per-user-marketing-template-message-limits)

* 네이티브 통합 기능은 제3자 비즈니스 서비스 제공자(BSP)와의 통합을 허용하지 않습니다.

## 사용 방법 비디오 {#video}

아래 비디오에서는 Adobe Journey Optimizer에서 WhatsApp을 기본 채널로 통합하여 규모에 맞게 안전하고, 실시간으로 개인화된 메시지를 제공하는 방법을 보여 줍니다.

+++ 비디오 보기

>[!VIDEO](https://video.tv.adobe.com/v/3470244?learn=on)

+++

## 추가 학습 리소스

WhatsApp 메시지 및 구성에 대한 추가 비디오 튜토리얼을 살펴보십시오.

➡️ [WhatsApp 채널 자습서](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/tutorials/channels/whatsapp/whatsapp-introduction){target="_blank"}

