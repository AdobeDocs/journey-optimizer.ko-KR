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
TQID: https://experienceleague.adobe.com/uHzRC9X6rB9EXH4gIFiRxFaeNcrTD0-40RrxZkN4XFg
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: b8df23d2-98a2-4406-86cc-2babe8728d36id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: 43066cc40499d87771b251766d5fa6b96afb1bb5
workflow-type: tm+mt
source-wordcount: 707
ht-degree: 62%

---

# WhatsApp 메시지 시작 {#get-started-whatsapp}

>[!BEGINSHADEBOX]

**이 페이지의 내용:** WhatsApp 채널이 Journey Optimizer에서 작동하는 방식과 필수 조건 및 제한 사항을 이해하여 여정과 캠페인에 WhatsApp을 추가하는 방법을 결정합니다.

>[!ENDSHADEBOX]

이제 Meta의 [Cloud API](https://developers.facebook.com/docs/whatsapp/cloud-api/)를 통해 Journey Optimizer에서 직접 WhatsApp 메시지를 보낼 수 있습니다. 이 기능을 사용하면 WhatsApp을 여정 및 캠페인에 원활하게 통합하여 수신자와의 소통과 교류를 향상시킬 수 있습니다.

* **여정**&#x200B;에서. 여정을 만들고, **WhatsApp** 활동을 추가하고, 기본 설정을 정의한 다음 **[!UICONTROL 작업: WhatsApp]** 오른쪽 창으로 이동하여 WhatsApp 메시지의 콘텐츠를 만들 수 있습니다. [이 페이지](../building-journeys/journey-gs.md)에서 여정을 만드는 방법을 알아보십시오.

* **캠페인**&#x200B;에서. 캠페인을 만들고 **WhatsApp**&#x200B;을 작업으로 선택하고 기본 설정을 정의한 다음 메시지 콘텐츠를 편집하여 보낼 WhatsApp 메시지를 정의합니다. [액션 캠페인](../campaigns/campaign-action.md#action-campaign-action) | [API 트리거 캠페인](../campaigns/api-triggered-campaigns.md) | [오케스트레이션된 캠페인](../orchestrated/create-orchestrated-campaign.md#create) 만드는 방법 알아보기

![](assets/do-not-localize/whatsapp-beta.png){zoomable="yes"}

## 사용 사례 {#use-cases}

WhatsApp은 대상자가 이미 플랫폼을 사용하고 있으며 풍부한 콘텐츠를 진정한 양방향 대화와 결합하고자 할 때 가장 잘 작동합니다.

| 이점 | 이유 | 예시 사용 사례 |
| --- | --- | --- |
| 높은 글로벌 참여 | 많은 지역에서 강력한 채택을 통해 널리 사용되는 메시징 플랫폼 | WhatsApp에서 이미 활성화된 해외 대상에게 연결 |
| 풍부한 대화형 메시지 | 이미지, 비디오, 단추 및 빠른 답글 지원 | 제품 카탈로그, 빠른 회신 옵션을 통한 약속 확인 |
| 양방향 대화 경험 | 수신자는 동일한 스레드 내에서 회신할 수 있습니다. | 고객 지원 대화, 주문 추적 질문 |
| 인터랙티브한 다중 화면 환경 | WhatsApp 흐름 템플릿을 사용하면 채팅 내에서 안내식 다단계 상호 작용을 구축할 수 있습니다 | 설문 조사, 잠재 고객 캡처 양식 |
| 공식 API를 통한 규정 준수 및 신뢰 | 보낸 사람 인증이 있는 Meta의 인증된 클라우드 API를 통해 제공됨 | 수신자 신뢰를 구축하는 브랜드 검증 커뮤니케이션 |
| 다른 채널과 통합 | 다른 채널과 함께 여정 및 캠페인과 계층화할 수 있음 | WhatsApp을 보완 접점으로 사용하는 다중 채널 여정 |

## 사용하지 않을 때 {#when-not-to-use}

WhatsApp은 대상 채택 및 명시적 동의에 따라 다르므로 모든 시나리오에 적합하지 않습니다. 다음 상황에서 다른 채널을 고려하십시오.

* 채택은 지역 및 인구통계에 따라 크게 다르므로 대상자는 WhatsApp을 사용하지 않습니다
* 수신자에게 Meta의 메시징 정책에 필요한 명시적 옵트인이 제공되지 않았습니다
* 메시지는 긴급하며 보장된 전달이 필요합니다. SMS 또는 푸시는 WhatsApp의 전달 및 템플릿 검토 제한을 고려하여 더 잘 처리합니다
* 컨텐츠가 길거나 복잡하고 이메일에 더 적합하여 더 많은 공간과 더 풍부한 포맷을 제공합니다
* 양방향 WhatsApp 스레드가 적시에 응답을 기대하기 때문에 실시간 대화 지원은 여러분의 입장에서 실현 가능하지 않습니다

## 사전 요구 사항 {#prereq}

WhatsApp을 Journey Optimizer와 통합하려면 다음 항목이 필요합니다.

* Meta Business Manager 계정
* [보낸 사람 이름과 전화번호가 확인된 WhatsApp 비즈니스 계정](https://developers.facebook.com/docs/whatsapp/overview/business-accounts/)
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

➡️ [WhatsApp 채널 튜토리얼](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/tutorials/channels/whatsapp/whatsapp-introduction){target="_blank"}

