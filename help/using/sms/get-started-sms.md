---
solution: Journey Optimizer
product: journey optimizer
title: 문자 메시지(SMS/MMS/RCS) 시작
description: Journey Optimizer에서 텍스트 메시지를 만들고 보내는 방법 알아보기
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: c1027268-0bbe-4e35-a5a6-2aef78083dd3
source-git-commit: 13552b3731a20fc9ca2d93a18c0a2c9fdf9378fa
workflow-type: tm+mt
source-wordcount: '812'
ht-degree: 27%

---

# 텍스트 메시지 시작 {#get-started-sms}

[!DNL Journey Optimizer]를 사용하여 고객의 모바일 디바이스로 문자 메시지(SMS/MMS/RCS)를 보냅니다. SMS/MMS/RCS 편집기에서 텍스트 형식으로 메시지를 만들고 개인화하고 미리 볼 수 있습니다.

텍스트 메시지는 여정 또는 캠페인에서 만들고 보낼 수 있습니다. SMS, MMS, RCS의 경우 SMS 액션을 사용합니다.

* **여정**&#x200B;에서. 여정을 만들고, SMS 활동을 추가하고, 기본 설정을 정의합니다. 그런 다음 오른쪽의 SMS 작업 창으로 이동하여 SMS, MMS 또는 RCS 메시지의 콘텐츠를 만듭니다. [여정 만드는 방법 알아보기](../building-journeys/journey-gs.md)

* **캠페인**&#x200B;에서. 캠페인을 만들고, 액션으로 SMS를 선택하고, 기본 설정을 정의합니다. 그런 다음 메시지 콘텐츠를 편집하여 전송할 SMS, MMS 또는 RCS 메시지를 정의합니다. [캠페인 만드는 방법 알아보기](../campaigns/create-campaign.md#configure)

>[!IMPORTANT]
>
>문자 메시지를 처음 만드는 경우 SMS 채널이 구성되었는지 확인하십시오. [자세히 알아보기](sms-configuration.md)

## 텍스트 메시지 기능 {#sms-capabilities}

Adobe Journey Optimizer은 다양한 채널에서 고객을 참여시킬 수 있는 포괄적인 텍스트 메시지 기능을 제공합니다.

**SMS(단문 메시지 서비스)**

최대 160자의 텍스트 전용 메시지를 보낼 수 있습니다. SMS는 모든 모바일 장치에서 가장 폭넓게 지원되는 텍스트 메시지 형식입니다.

**MMS(멀티미디어 메시지 서비스)**

비디오, 이미지, 오디오 클립 및 GIF를 포함한 멀티미디어 콘텐츠와의 커뮤니케이션을 향상시킵니다. MMS 메시지는 미디어 파일 외에 최대 1600자의 텍스트를 입력할 수 있습니다. [MMS 제한에 대해 자세히 알아보기](../start/guardrails.md#sms-guardrails)

**RCS(리치 통신 서비스)**

캐러셀, 리치 카드, 제안된 작업 및 향상된 미디어 지원과 같은 고급 기능이 포함된 브랜드 대화형 메시지를 보냅니다. RCS는 지원되는 장치에서 더 풍부한 메시징 환경을 제공합니다.

## 주요 기능 {#key-features}

**Personalization 및 다이내믹 콘텐츠**

개인화 편집기를 사용하여 개인화된 텍스트 메시지를 만듭니다. 프로필 속성, 조건부 콘텐츠 및 동적 데이터를 추가하여 메시지를 개별 수신자에게 사용자 지정할 수 있습니다. [개인화에 대해 알아보기](../personalization/personalize.md)

**여러 공급자 지원**

Adobe Journey Optimizer은 주요 SMS 서비스 공급자와 통합됩니다.

* **Sinch** - [구성 안내서](sms-configuration-sinch.md)
* **Twilio** - [구성 안내서](sms-configuration-twilio.md)
* **Infobip** - [구성 안내서](sms-configuration-infobip.md)
* **사용자 지정 공급자** - 사용자 지정 API 통합을 사용하여 다른 SMS 공급자를 구성합니다. [자세히 알아보기](sms-configuration-custom.md)

**URL 단축 및 추적**

메시지에 단축되고 추적 가능한 URL을 추가하여 참여를 모니터링합니다. URL 단축 기능을 사용하려면 하위 도메인을 구성해야 합니다. [SMS 하위 도메인을 구성하는 방법 알아보기](sms-subdomains.md)

**옵트아웃 관리**

내장된 옵트아웃 관리를 통해 업계 표준 및 규정을 준수할 수 있습니다. Journey Optimizer은 Sinch 및 Infobip 공급자에 대한 표준 옵트아웃 키워드(STOP, QUIT, CANCEL 등)를 자동으로 처리합니다. [옵트아웃 관리에 대해 알아보기](sms-opt-out.md)

**미리 보기 및 테스트**

테스트 프로필 및 샘플 데이터를 사용하여 보내기 전에 텍스트 메시지를 테스트합니다. 메시지가 올바르게 표시되도록 개인화, 콘텐츠 및 서식을 미리 봅니다. [메시지를 보내는 방법 알아보기](send-sms.md)

**보고 및 분석**

포괄적인 보고 기능을 사용하여 SMS 캠페인 및 여정의 성과를 추적합니다.

* [SMS 캠페인 보고서](../reports/campaign-global-report-cja-sms.md)
* [SMS 여정 보고서](../reports/journey-global-report-cja-sms.md)

## 구성 요구 사항 {#configuration-requirements}

문자 메시지를 보내기 전에 다음을 수행해야 합니다.

1. **SMS 공급자 선택** - Sinch, Twilio, Infobip 중에서 선택하거나 사용자 지정 공급자를 구성합니다.
2. **API 자격 증명 설정** - 공급자의 API 토큰 및 서비스 ID를 Journey Optimizer과 통합
3. **채널 구성 만들기** - 마케팅 및 트랜잭션 메시지에 대한 SMS 구성 설정
4. **하위 도메인 구성(선택 사항)** - 메시지에 URL 단축법을 사용하려는 경우에만 필요합니다.

이러한 구성 단계는 일반적으로 시스템 관리자가 수행합니다. [SMS 구성 시작](sms-configuration.md)

## 빠른 시작 안내서 {#quick-start}

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="sms-configuration.md">
<img alt="유효성 검사" src="../assets/do-not-localize/sms-config.jpg">
</a>
<div>
<a href="sms-configuration.md"><strong>SMS 채널 구성</strong></a>
</div>
<p>SMS 공급자 및 채널 구성 설정</p>
</td>
<td>
<a href="create-sms.md">
<img alt="리드" src="../assets/do-not-localize/sms-create.jpeg">
</a>
<div><a href="create-sms.md"><strong>문자 메시지 만들기</strong>
</div>
<p>SMS, MMS 또는 RCS 콘텐츠 디자인 및 개인화</p>
</td>
<td>
<a href="send-sms.md">
<img alt="드물게" src="../assets/do-not-localize/sms-sending.jpg">
</a>
<div>
<a href="send-sms.md"><strong>미리 보기 및 보내기</strong></a>
</div>
<p>문자 메시지를 테스트하여 대상자에게 보내기</p>
</td>
<td>
<a href="sms-opt-out.md">
<img alt="유효성 검사" src="../assets/do-not-localize/sms-opt-out.jpg">
</a>
<div>
<a href="sms-opt-out.md"><strong>옵트아웃 관리</strong></a>
</div>
<p>구독 취소 요청을 처리하고 규정 준수 보장</p>
</td>
</tr></table>

## 추가 리소스 {#additional-resources}

Journey Optimizer의 텍스트 메시지에 대한 자세한 내용은 아래 항목을 참조하십시오.

+++구성 안내서

SMS 환경을 설정하고 구성하는 방법을 알아봅니다.

* [SMS 채널 구성 개요](sms-configuration.md)
* [SMS 채널 구성 만들기](sms-configuration-surface.md)
* [URL 단축에 대한 SMS 하위 도메인 구성](sms-subdomains.md)

+++

+++공급자 설정 안내서

각 SMS 서비스 공급자에 대한 단계별 구성:

* [Sinch 공급자 구성](sms-configuration-sinch.md)
* [Twilio 공급자 구성](sms-configuration-twilio.md)
* [Infobip 공급자 구성](sms-configuration-infobip.md)
* [사용자 지정 SMS 공급자 구성](sms-configuration-custom.md)

+++

+++콘텐츠 제작 및 관리

문자 메시지 콘텐츠를 만들고, 개인화하고, 관리합니다.

* [SMS/MMS 메시지 만들기](create-sms.md)
* [메시지 미리 보기, 테스트 및 보내기](send-sms.md)
* [텍스트 메시지의 Personalization](../personalization/personalize.md)
* [다이내믹 콘텐츠](../personalization/get-started-dynamic-content.md)

+++

+++규정 준수 및 개인정보 보호

문자 메시지가 규정 및 개인 정보 보호 표준을 준수하는지 확인합니다.

* [옵트아웃 관리](sms-opt-out.md)
* [개인 정보 보호 및 동의](../privacy/opt-out.md#sms-opt-out-management-sms-opt-out-management)

+++

+++성능 추적

SMS 캠페인 및 여정 성과 모니터링 및 분석:

* [SMS 캠페인 보고서](../reports/campaign-global-report-cja-sms.md)
* [SMS 여정 보고서](../reports/journey-global-report-cja-sms.md)

+++

+++여정 및 캠페인 통합

SMS를 고객 여정 및 캠페인에 통합하는 방법을 알아봅니다.

* [여정에 SMS 메시지 추가](../building-journeys/journeys-message.md)
* [SMS 캠페인 만들기](../campaigns/create-campaign.md)

+++

## 방법 비디오 {#videos}

**SMS 메시지 구성 및 보내기**

고객 여정에 SMS 메시지를 구성하고, 작성하고, 포함하는 방법을 알아봅니다.

+++비디오 보기

>[!VIDEO](https://video.tv.adobe.com/v/3420509?learn=on)

+++

**모바일 메시징 기능 살펴보기**

Adobe Journey Optimizer이 마케터에게 제공하는 포괄적인 모바일 메시징 기능을 살펴보십시오.

+++비디오 보기

>[!VIDEO](https://video.tv.adobe.com/v/3426021?quality=12&learn=on)

+++

**브랜드 RCS 메시지 보내기**

사용자 정의 SMS 공급자를 사용하여 Adobe Journey Optimizer에서 인터랙티브한 브랜디드 RCS 메시지를 구성하고 전송하는 방법에 대해 알아봅니다.

+++비디오 보기

>[!VIDEO](https://video.tv.adobe.com/v/3464755)

+++

**관련 항목**

* [여정에 메시지 추가하기](../building-journeys/journeys-message.md)
* [마케팅 캠페인 만들기](../campaigns/create-campaign.md)
* [가드레일 및 제한 사항](../start/guardrails.md#sms-guardrails)
