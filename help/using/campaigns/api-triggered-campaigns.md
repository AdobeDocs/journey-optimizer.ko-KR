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
source-git-commit: 81e54a3e3428d58818805b5dcb397ede4039436a
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 35%

---


# API 트리거 캠페인 작업 {#trigger-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_overview_api_triggered"
>title="API 트리거 캠페인"
>abstract="**트랜잭션 API 트리거 캠페인**<br/> API 통화를 통한 실시간 메시지 트리거&#x200B;<br/><br/>**마케팅 메시지**<br/>&#x200B;홍보 콘텐츠(옵트인 필요, 비즈니스 규칙 적용)<br/><br/>**트랜잭션 메시지**<br/>&#x200B;서비스 관련 콘텐츠(확인, 알림, 마케팅 동의 대상 아님)<br/><br/>**사용 가능한 채널**<br/>&#x200B;이메일, SMS, 푸시 알림"

## API 트리거 캠페인 기본 정보 {#about}

API 트리거 캠페인을 사용하면 마케팅 커뮤니케이션이 적시에 대상자에게 연락하거나, 암호 재설정과 같은 개인에 대한 트랜잭션/운영 메시지가 필요할 때 프로필 속성을 사용하는 것뿐만 아니라 REST API 페이로드인 트리거에서 실시간 컨텍스트 데이터를 사용하는 개인화가 포함될 수 있습니다.

이렇게 하려면 먼저 Journey Optimizer에서 API 트리거 캠페인을 만든 다음 [대화형 메시지 실행 REST API](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution)를 사용하여 API 호출을 통해 실행을 시작해야 합니다.

➡️ [비디오에서 이 기능 살펴보기](#video)

>[!NOTE]
>
>지원되는 채널에 대한 자세한 내용은 이 섹션의 표를 참조하십시오. [여정 및 캠페인의 채널](../channels/gs-channels.md#channels).
>
>사용 가능한 채널은 사용하는 라이선스 모델 및 추가 기능에 따라 다릅니다.

## API 트리거 캠페인 만들기에 대한 주요 단계 {#steps}

캠페인을 시작하기 전에 [이 섹션에 나열된 다음 필수 구성 요소를 확인](get-started-with-campaigns.md#prerequisites)하세요. 이러한 전제 조건이 충족되면 캠페인 생성을 시작할 수 있습니다.

1. [캠페인 속성 정의](api-triggered-campaign-properties.md)
1. [캠페인 액션 구성](api-triggered-campaign-action.md)
1. [캠페인 콘텐츠 편집](api-triggered-campaign-content.md)
1. [캠페인 대상자 정의](api-triggered-campaign-audience.md)
1. [캠페인 예약](api-triggered-campaign-schedule.md)
1. [캠페인 검토 및 활성화](review-activate-api-triggered-campaign.md)
1. [캠페인 실행 트리거](trigger-campaigns.md)

## 방법 비디오 {#video}

대화형 메시지 실행 REST API를 사용하여 사용자 상호 작용을 기반으로 외부 시스템에서 캠페인을 만들고 트리거하는 방법에 대해 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/3425358?quality=12)
