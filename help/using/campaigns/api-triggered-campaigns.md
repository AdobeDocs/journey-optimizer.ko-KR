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
source-git-commit: 15f5fdfde0e9f7c93739a624918838dbd6787833
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 4%

---


# API 트리거 캠페인 작업 {#trigger-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_overview_api_triggered"
>title="API 트리거 캠페인"
>abstract="**트랜잭션 API 트리거 캠페인**<br/> API 호출을 통해 실시간 메시지 트리거&#x200B;<br/><br/>**마케팅 메시지**<br/>&#x200B;프로모션 콘텐츠(비즈니스 규칙에 따라 옵트인 필요)<br/><br/>**트랜잭션 메시지**<br/>&#x200B;서비스 관련 콘텐츠(확인, 알림, 마케팅 동의에 따라 적용되지 않음)<br/><br/>**사용 가능한 채널**<br/>&#x200B;이메일, SMS, 푸시 알림"

## API 트리거 캠페인 기본 정보 {#about}

API 트리거 캠페인을 사용하면 마케팅 커뮤니케이션이 적시에 대상자에게 연락하거나, 암호 재설정과 같은 개인에 대한 트랜잭션/운영 메시지를 보낼 수 있습니다. 여기에서는 프로필 속성뿐만 아니라 REST API 페이로드인 트리거에서 실시간 컨텍스트 데이터를 사용하여 개인화가 필요할 수 있습니다.

이렇게 하려면 먼저 Journey Optimizer에서 API 트리거 캠페인을 만든 다음 [대화형 메시지 실행 REST API](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution)를 사용하여 API 호출을 통해 실행을 시작해야 합니다.

API 트리거 캠페인에 사용할 수 있는 채널은 이메일, SMS 및 푸시 메시지입니다.

➡️ [비디오에서 이 기능 살펴보기](#video)

## API 트리거 캠페인 만들기에 대한 주요 단계 {#steps}

1. [캠페인 속성 정의](api-triggered-campaign-properties.md)
1. [캠페인 작업 구성](api-triggered-campaign-action.md)
1. [캠페인 콘텐츠 편집](api-triggered-campaign-content.md)
1. [캠페인 대상자 정의](api-triggered-campaign-audience.md)
1. [캠페인 예약](api-triggered-campaign-schedule.md)
1. [캠페인 검토 및 활성화](review-activate-api-triggered-campaign.md)
1. [캠페인 실행 트리거](trigger-campaigns.md)

## 방법 비디오 {#video}

대화형 메시지 실행 REST API를 사용하여 사용자 상호 작용을 기반으로 외부 시스템에서 캠페인을 만들고 트리거하는 방법에 대해 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/3452732?quality=12&captions=kor)
