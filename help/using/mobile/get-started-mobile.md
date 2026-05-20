---
solution: Journey Optimizer
product: journey optimizer
title: 모바일 메시지 시작
description: Journey Optimizer에서 모바일 메시지를 만들고 보내는 방법 알아보기
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: c1027268-0bbe-4e35-a5a6-2aef78083dd3
TQID: https://experienceleague.adobe.com/Ev0xJ86fpweQxgf-VjGUEl4ebk6BdzhVof2BgiMR9EM
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2:
  - id: cf64c7f6-7428-4ae5-b158-8df9771f38f4
  - id: e5329d1b-e590-4e24-a3fb-ef3fe0f2c721
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c13ff12d-60f1-49cd-833a-d43359628223
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 0201927f8d9260e8ba1d0db7014d6a7b30d09062
workflow-type: tm+mt
source-wordcount: 1006
ht-degree: 24%

---

# 모바일 메시지 시작 {#get-started-sms}

>[!IMPORTANT]
>
>모바일 메시지를 처음 만드는 경우 모바일 메시지 채널이 구성되었는지 확인하십시오. [자세히 알아보기](mobile-configuration.md)

[!DNL Journey Optimizer]을(를) 사용하여 콘텐츠를 만들고, 개인화하고, 미리 볼 수 있는 단일 SMS/MMS/RCS 편집기에서 **SMS**, **MMS**, **RCS**&#x200B;의 세 가지 채널을 통해 고객에게 모바일 메시지를 보냅니다.

* **SMS(Short Message Service)**: 모든 모바일 장치에서 지원되는 최대 160자의 텍스트 전용 메시지를 보냅니다.
* **MMS(멀티미디어 메시지 서비스)**: 이미지, 비디오, 오디오 클립 및 GIF와 최대 1,600자의 텍스트를 추가하여 메시지를 보강합니다. [MMS 제한에 대해 자세히 알아보기](../start/guardrails.md#sms-guardrails)
* **리치 커뮤니케이션 서비스(RCS)**:Deliver 고객의 기본 메시징 앱에서 직접 브랜드 인터랙티브 콘텐츠를 제공하므로 별도의 앱 다운로드가 필요하지 않습니다.

모바일 메시지는 모바일 메시지 작업을 사용하여 여정 또는 캠페인에서 만들고 보낼 수 있습니다.

* **여정**&#x200B;에서: 여정에 모바일 메시지 작업을 추가하고 기본 설정을 정의한 다음 오른쪽의 모바일 메시지 작업 창에서 콘텐츠를 작성합니다. [여정 만드는 방법 알아보기](../building-journeys/journey-gs.md)

* **Campaign**:Create 캠페인에서 모바일 메시지를 작업으로 선택하고 기본 설정을 정의한 다음 메시지 콘텐츠를 편집합니다. [액션 캠페인](../campaigns/campaign-action.md#action-campaign-action) | [API 트리거 캠페인](../campaigns/api-triggered-campaigns.md) | [오케스트레이션된 캠페인](../orchestrated/create-orchestrated-campaign.md#create) 만드는 방법 알아보기


## 주요 기능 {#key-features}

| 기능 | 설명 |
|---|---|
| **개인화** | 개인화 편집기를 사용하여 프로필 속성, 조건부 콘텐츠 및 동적 데이터로 메시지를 사용자 지정합니다. [자세히 알아보기](../personalization/personalize.md) |
| **공급자 지원** | API 통합을 통해 [Sinch](mobile-configuration-sinch.md), [Twilio](mobile-configuration-twilio.md), [Infoip](mobile-configuration-infobip.md) 또는 [사용자 지정 공급자](mobile-configuration-custom.md)와 연결합니다. |
| **URL 단축** | 참여를 모니터링하려면 단축되고 추적 가능한 URL을 추가하십시오. 하위 도메인 구성이 필요합니다. [자세히 알아보기](mobile-subdomains.md) |
| **옵트아웃 관리** | 표준 옵트아웃 키워드(STOP, QUIT, CANCEL 등)의 기본 처리 Sinch 및 Infobip용. [자세히 알아보기](mobile-opt-out.md) |
| **미리 보기 및 테스트** | 보내기 전에 테스트 프로필 및 샘플 데이터를 사용하여 콘텐츠의 유효성을 검사합니다. [자세히 알아보기](send-mobile-message.md) |
| **보고** | 전용 [캠페인 보고서](../reports/campaign-global-report-cja-sms.md) 및 [여정 보고서](../reports/journey-global-report-cja-sms.md)를 사용하여 캠페인 및 여정 성과를 추적합니다. |

## 구성 요구 사항 {#configuration-requirements}

모바일 메시지를 보내기 전에 다음을 수행해야 합니다.

1. **SMS 공급자 선택**: Sinch, Twilio, Infobip 중에서 선택하거나 사용자 지정 공급자를 구성하십시오.
2. **API 자격 증명 설정**: 공급자의 API 토큰 및 서비스 ID를 Journey Optimizer과 통합합니다.
3. **채널 구성 만들기**: 마케팅 및 트랜잭션 메시지에 대한 SMS 구성을 설정합니다.
4. **하위 도메인 구성(선택 사항)**: 메시지에 URL 단축법을 사용하려는 경우에만 필요합니다.

이 구성 단계는 일반적으로 시스템 관리자가 수행합니다. [SMS 구성 시작](mobile-configuration.md)

### RCS 요구 사항 {#requirement-rcs}

Journey Optimizer에서 RCS를 사용하려면 다음 전제 조건이 필요합니다.

* **Sinch RCS API 자격 증명**: 관리자가 Sinch RCS 공급업체에 대한 API 자격 증명(프로젝트 ID, 앱 ID 및 API 토큰)을 구성해야 합니다. [자세히 알아보기](mobile-configuration-sinch.md)
* **모바일 메시지 채널 구성**: 메시지가 SMS가 아닌 RCS로 전달되도록 하려면 관리자가 RCS 사용 자격 증명을 선택하여 채널 구성을 만들어야 합니다. [자세히 알아보기](mobile-configuration.md)
* **대체 SMS**: 적극 권장합니다. RCS를 지원하지 않는 장치의 수신자는 SMS 대체를 사용할 수 없는 경우 메시지를 받지 못합니다. 기존 SMS 볼륨이 없는 고객은 SMS와 짧은 코드를 구입해야 합니다. [자세히 알아보기](design-mobile.md#rcs-content)
* **지원되는 공급업체**: 기본 RCS 작성에는 Sinch RCS가 필요합니다(Adobe 재판매 또는 직접). Twilio, Infobip 및 기타 공급자는 사용자 지정 공급자 통합을 사용해야 합니다.
* **장치 지원**: RCS 배달이 Android 및 iOS 장치에서 지원됩니다. 통신사 및 지역 가용성은 다양하며, RCS는 전 세계적으로 보편적으로 이용할 수 없습니다.

## 추가 리소스 {#additional-resources}

Journey Optimizer의 모바일 메시지에 대한 자세한 내용은 아래 항목을 참조하십시오.

+++구성 안내서

SMS 환경을 설정하고 구성하는 방법 알아보기:

* [SMS 채널 구성 개요](mobile-configuration.md)
* [SMS 채널 구성 만들기](mobile-configuration-surface.md)
* [URL 단축을 위한 SMS 하위 도메인 구성](mobile-subdomains.md)

+++

+++서비스 제공자 설정 안내서

각 SMS 서비스 제공자에 대한 단계별 구성:

* [Sinch 제공자 구성](mobile-configuration-sinch.md)
* [Twilio 제공자 구성](mobile-configuration-twilio.md)
* [Infobip 제공자 구성](mobile-configuration-infobip.md)
* [사용자 정의 SMS 제공자 구성](mobile-configuration-custom.md)

+++

+++콘텐츠 제작 및 관리

모바일 메시지 콘텐츠를 만들고, 개인화하고, 관리합니다.

* [SMS/RCS/MMS 메시지 만들기](create-mobile-message.md)
* [메시지 미리 보기, 테스트, 보내기](send-mobile-message.md)
* [모바일 메시지의 Personalization](../personalization/personalize.md)
* [다이내믹 콘텐츠](../personalization/get-started-dynamic-content.md)
* [AI 어시스턴트로 SMS 콘텐츠 생성](../content-management/generative-text.md)

+++

+++규정 준수 및 개인 정보

모바일 메시징이 규정 및 개인 정보 보호 표준을 준수하는지 확인합니다.

* [옵트아웃 관리](mobile-opt-out.md)
* [개인 정보 보호 및 동의](../privacy/opt-out.md#opt-out-decision-management)

+++

+++성과 추적

SMS 캠페인 및 여정 성과 모니터링 및 분석:

* [SMS 캠페인 보고서](../reports/campaign-global-report-cja-sms.md)
* [SMS 여정 보고서](../reports/journey-global-report-cja-sms.md)

+++

+++여정 및 캠페인 통합

SMS를 고객 여정 및 캠페인에 통합하는 방법 알아보기:

* [여정에 SMS 메시지 추가](../building-journeys/journey-action.md)
* [SMS 캠페인 만들기](../campaigns/create-campaign.md)

+++

+++RCS에 대해 자주 묻는 질문

**Twilio 또는 Infobip에서 기본 RCS 메시지를 사용할 수 있습니까?**

아니요. Twilio 또는 Infobip과 같은 서드파티 SMS 공급자를 사용하는 경우 Journey Optimizer의 기본 RCS 디자이너를 사용할 수 없습니다. 그러나 RCS 메시지는 [사용자 지정 공급자 통합](mobile-configuration-custom.md)을 통해 보낼 수 있습니다.

**RCS와 함께 SMS를 구입하는 이유는 무엇입니까?**

권장 경로인 SMS 폴백을 활성화하려면 SMS 볼륨과 짧은 코드를 구매해야 합니다. SMS가 구성되지 않은 경우, 장치 또는 통신사가 RCS를 지원하지 않는 프로필은 메시지를 전혀 받지 않습니다.

**Sinch 직접 고객에게 기본 RCS 메시지를 사용할 수 있습니까?**

예. Sinch의 대화형 API를 사용하는 고객은 Adobe 재판매 및 Sinch 직접 고객을 포함하여 기본 RCS 작성에 액세스할 수 있습니다.

**RCS를 어디에서나 사용할 수 있습니까?**

아니요. 통신사 채택은 전 세계적으로 계속 증가하고 있지만, RCS는 모든 통신사와 지역에서 보편적으로 지원되지 않습니다. RCS 캠페인을 계획할 때 지역 가용성 및 통신사 지원이 조사되어야 합니다.

**RCS 메시지가 장치에 표시되는 위치는 어디입니까?**

RCS 메시지는 디바이스의 기본 메시징 애플리케이션에서 표준 SMS 메시지와 동일한 위치에 나타납니다. 브랜드가 있고 검증된 발신자로부터 전송되어 수신자에게 메시지가 합법적이라는 신뢰 신호를 보냅니다.

**RCS 메시지의 문자 제한은 무엇입니까?**

리치 미디어(단일) 메시지 유형은 표준 SMS의 160자 제한보다 훨씬 많은 3,072자를 지원합니다. 기본 RCS 메시지 유형은 표준 SMS 제한과 일치하는 160자로 제한됩니다.

+++

## 방법 비디오 {#videos}

**SMS 메시지 구성 및 보내기**

고객 여정에 SMS 메시지를 구성하고, 작성하고, 포함하는 방법을 알아봅니다.

+++비디오 보기

>[!VIDEO](https://video.tv.adobe.com/v/3420509?learn=on)

+++

**모바일 메시지 기능 살펴보기**

Adobe Journey Optimizer가 마케터에게 제공하는 포괄적인 모바일 메시지 기능을 살펴봅니다.

+++비디오 보기

>[!VIDEO](https://video.tv.adobe.com/v/3426021?quality=12&learn=on)

+++

**브랜드 RCS 메시지 보내기**

사용자 정의 SMS 공급자를 사용하여 Adobe Journey Optimizer에서 인터랙티브한 브랜디드 RCS 메시지를 구성하고 전송하는 방법에 대해 알아봅니다.

+++비디오 보기

>[!VIDEO](https://video.tv.adobe.com/v/3464755)

+++
