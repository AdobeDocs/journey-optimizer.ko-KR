---
solution: Journey Optimizer
product: journey optimizer
title: API 트리거 캠페인 작업
description: Journey Optimizer API를 사용하여 캠페인을 트리거하는 방법에 대해 알아봅니다.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: 캠페인, API 트리거, REST, 최적화 도구, 메시지
exl-id: 0ef03d33-da11-43fa-8e10-8e4b80c90acb
source-git-commit: d4765f9084efac1fd241404dff365a66027ce5af
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 53%

---


# API 트리거 캠페인 작업 {#trigger-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_overview_api_triggered"
>title="API 트리거 캠페인"
>abstract="**트랜잭션 API 트리거 캠페인**<br/> API 통화를 통한 실시간 메시지 트리거&#x200B;<br/><br/>**마케팅 메시지**<br/>&#x200B;홍보 콘텐츠(옵트인 필요, 비즈니스 규칙 적용)<br/><br/>**트랜잭션 메시지**<br/>&#x200B;서비스 관련 콘텐츠(확인, 알림, 마케팅 동의 대상 아님)<br/><br/>**사용 가능한 채널**<br/>&#x200B;이메일, SMS, 푸시 알림"

## API 트리거 캠페인 기본 정보 {#about}

API 트리거 캠페인을 사용하면 적시에 마케팅 커뮤니케이션을 대상자에게 보내거나 암호 재설정 등 개인에 대한 트랜잭션/운영 메시지를 보낼 수 있습니다. 이 경우 프로필 속성뿐만 아니라 실시간 상황 데이터, 즉 REST API 페이로드를 사용한 개인화가 필요할 수 있습니다.

이렇게 하려면 먼저 Journey Optimizer에서 API 트리거 캠페인을 만든 다음 [대화형 메시지 실행 REST API](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution)를 사용하여 API 호출을 통해 실행을 시작해야 합니다.

API 트리거 캠페인에 사용할 수 있는 채널은 이메일, SMS 및 푸시 메시지입니다.

➡️ [비디오에서 이 기능 살펴보기](#video)


>[!NOTE]
>
>지원되는 채널: [이메일](../email/get-started-email.md), [SMS/MMS/RCS](../sms/get-started-sms.md), [푸시 알림](../push/get-started-push.md).
>
>사용 가능한 채널은 라이선스 모델 및 추가 기능에 따라 다릅니다.

## API 트리거 캠페인 만들기에 대한 주요 단계 {#steps}

1. [캠페인 속성 정의](api-triggered-campaign-properties.md)
1. [캠페인 액션 구성](api-triggered-campaign-action.md)
1. [캠페인 콘텐츠 편집](api-triggered-campaign-content.md)
1. [캠페인 대상자 정의](api-triggered-campaign-audience.md)
1. [캠페인 예약](api-triggered-campaign-schedule.md)
1. [캠페인 검토 및 활성화](review-activate-api-triggered-campaign.md)
1. [캠페인 실행 트리거](trigger-campaigns.md)

>[!IMPORTANT]
>
>캠페인을 만들기 전에 일반적인 [캠페인 필수 구성 요소](../campaigns/get-started-with-campaigns.md#prerequisites)를 검토했는지 확인하세요.

## 방법 비디오 {#video}

대화형 메시지 실행 REST API를 사용하여 사용자 상호 작용을 기반으로 외부 시스템에서 캠페인을 만들고 트리거하는 방법에 대해 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/3425358?quality=12)
