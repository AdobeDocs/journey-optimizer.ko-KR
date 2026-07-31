---
title: 사용자 정의 채널 시작하기
description: ' [!DNL Journey Optimizer]''s Channel Builder to bring any outbound messaging channel into [!DNL Journey Optimizer] 을(를) 사용하여 캠페인 및 여정에서 사용하는 방법을 알아봅니다.'
feature: Channel Configuration
topic: Content Management
role: User
level: Beginner
badge: label="제한 공개" type="Informative"
source-git-commit: 99103a5028c9cebc63b2c1d69ce5848974b40c8e
workflow-type: tm+mt
source-wordcount: '669'
ht-degree: 5%

---


# 사용자 정의 채널 시작하기 {#get-started-custom-channel}

>[!BEGINSHADEBOX]

**이 페이지에서:** Adobe Journey Optimizer에 있는 사용자 지정 채널이 무엇인지, 사용자 지정 작업과 어떻게 비교되는지, 캠페인 및 여정에서 사용할 수 있도록 아웃바운드 HTTP 끝점을 AJO으로 가져오기 위한 전체 워크플로에 대해 알아봅니다.

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>이 기능은 제한적으로 이용할 수 있습니다. 액세스 권한을 얻으려면 Adobe 담당자에게 문의하십시오.

<!--Multilingual support, business rules enforcement, and [!DNL Adobe Experience Decisioning] integration are planned for a future release.-->

[!DNL Journey Optimizer]의 **사용자 지정 채널** 기능을 사용하면 모든 아웃바운드 채널을 [!DNL Journey Optimizer]&#x200B;(으)로 가져와 기본 채널처럼 캠페인 및 여정에서 사용할 수 있습니다. 관리자는 **채널 빌더**&#x200B;를 사용하여 엔지니어링 작업 없이 새 채널을 만들고 구성할 수 있으며 마케터는 즉시 이러한 채널을 사용하여 고객과 통신할 수 있습니다.

## 어떤 문제가 해결됩니까? {#why-custom-channels}

[!DNL Journey Optimizer]은(는) 기본적으로 이메일, SMS, 푸시 알림, WhatsApp, LINE 및 기타 채널을 지원합니다. 그러나 많은 조직이 WeChat, KakaoTalk, Messenger 또는 외부 공급자와 같이 기본적으로 통합되지 않은 메시징 플랫폼을 사용하며 자신의 공급업체와 전달하는 동안 오케스트레이션 및 캠페인 생성을 위해 [!DNL Journey Optimizer]에서 사용하기를 원합니다.

<!--TBC: Another use case is when organizations have a legacy messaging gateway that exposes an HTTP endpoint, and they want to use it in [!DNL Journey Optimizer] without having to build a custom integration.-->

사용자 지정 채널은 이 간격을 채웁니다. 이를 통해 아웃바운드 HTTP 끝점을 전체 [!DNL Journey Optimizer] 채널로 사용하여 다음을 잠금 해제할 수 있습니다.

* **전체 채널 기능** - 최적화(콘텐츠 실험 및 타깃팅), OOTB 보고 및 모니터링, 동의 및 거버넌스 적용, 표현식 조각. <!--Multilingual and business rules are planned for a future release.-->
* **통합 오케스트레이션** - 기본 게재 공급자에 관계없이 모든 메시징 채널을 한 곳에서 관리합니다.
* **코드 없는 설정** - 관리자가 채널 빌더 UI를 통해 채널을 구성합니다. 사용자 지정 코드나 엔지니어링 작업이 필요하지 않습니다.

## 사용자 지정 채널과 사용자 지정 작업 비교 {#custom-channel-vs-custom-action}

이전에 [!DNL Journey Optimizer] 여정에서 [사용자 지정 작업](../action/action.md)을 사용한 경우 사용자 지정 채널은 다른 사용 사례를 처리합니다.

**WeChat, KakaoTalk 또는 사용자 지정 메시징 게이트웨이와 같이 [!DNL Journey Optimizer]에서 기본적으로 지원되지 않는 플랫폼을 통해 최종 사용자에게 메시지를 보내야 하는 경우**&#x200B;사용자 지정 채널을 사용합니다. 사용자 지정 채널은 캠페인 및 여정에서 사용할 수 있으며, 다음과 같은 지원을 제공합니다.

* 기본 아웃바운드 채널과 유사한 개인화 편집기를 통한 전체 개인화
* 시각적/양식 페이로드 편집기, 미리보기 및 증명
* 콘텐츠 실험 및 타겟팅
* OOTB 보고 및 모니터링
* 여러 API 자격 증명 및 채널 구성
* RBAC/ABAC

사용자 지정 채널은 유일한 HTTP 메서드로 POST를 지원합니다.

**여정 내의 한 단계로 콜센터, 로깅 플랫폼 또는 오프라인 데이터베이스와 같은 외부 시스템에서 데이터를 검색하거나 정보를 푸시해야 하는 경우**&#x200B;사용자 지정 작업을 사용합니다. 사용자 지정 작업은 여정 전용이며 GET, PUT 및 POST 메서드를 지원합니다.

<!--
| | Custom Action | Custom Channel |
| --- | --- | --- |
| **Primary use case** | Retrieve data from or send information to external systems (call centers, offline systems, logging) | Send messages to end users through channels not natively supported in [!DNL Journey Optimizer] |
| **Available in** | Journeys only | Campaigns, journeys, and orchestrated campaigns |
| **Supported HTTP methods** | GET, PUT, POST | POST only |
| **Full personalization (PE)** | No | Yes, through the personalization editor, similar to native outbound channels |
| **Visual/form editor** | No | Yes |
| **Preview and proof** | No | Yes |
| **Content experimentation** | No | Yes |
| **Targeting** | No | Yes |
| **OOTB Reporting** | Yes | Yes |
| **Multiple API credentials and channel configurations** | No | Yes |
| **RBAC/ABAC** | No | Yes |
-->

>[!TIP]
>
>일반적으로 최종 사용자에게 메시지를 보내는 채널 사용 사례에는 사용자 지정 채널을 사용하는 것이 좋습니다. 데이터 검색 또는 외부 시스템 트리거와 같이 여정에 필요한 다른 커넥터와 같은 사용 사례의 경우 사용자 지정 작업을 계속 사용할 수 있습니다.

## 사용 사례 {#use-cases}

사용자 지정 채널은 다음 작업에 이상적입니다.

* **지원되지 않는 메시징 플랫폼** - 기본 [!DNL Journey Optimizer] 채널이 없는 WeChat, Kakao Talk, Messenger, Telegram 또는 지역 메시징 서비스와 같은 채널입니다.
* **사용자 지정 게재 공급자** - 메시지 게재를 위해 계속 사용할 외부 공급자에 투자했지만 오케스트레이션, 개인화 및 캠페인 관리를 위해 [!DNL Journey Optimizer]을(를) 활용하는 것을 선호하는 조직
* **레거시 채널** - HTTP 끝점을 노출하는 독점 또는 레거시 메시징 게이트웨이입니다.
* **업종별 채널** - 의료, 금융 경고 시스템 또는 정부 알림 서비스를 위한 보안 메시지.

## 작동 방식 {#how-it-works}

사용자 지정 채널 설정 및 사용은 아래의 주요 단계를 따릅니다.

1. **구성**(관리자) - 관리자가 **채널 빌더**&#x200B;에서 사용자 지정 채널을 만들어 끝점, 인증, 제한 정책 및 메시지 페이로드 구조를 정의합니다. 그런 다음 채널 구성이 만들어지고 사용자 지정 채널에 연결됩니다.
1. **만들기**(마케터) - 마케터가 여정 또는 캠페인에 사용자 지정 채널을 추가하고, 채널 구성을 선택하고, [!DNL Journey Optimizer]의 개인화 편집기를 사용하여 메시지 페이로드를 작성합니다.
1. **보내기** - 프로필이 유효하면 [!DNL Journey Optimizer]에서 구성된 끝점으로 개인화된 페이로드를 보냅니다. 외부 시스템은 호출을 처리하고 메시지를 전달합니다.
1. **모니터링**(관리자/마케터) - 관리자와 마케터는 [!DNL Journey Optimizer]의 보고 및 모니터링 대시보드를 통해 사용자 지정 채널의 성능과 안정성을 모니터링할 수 있습니다.

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="configure-custom-channel.md">
<img alt="구성" src="../assets/do-not-localize/inapp-config.jpg">
</a>
<div>
<a href="configure-custom-channel.md"><strong>사용자 지정 채널 구성</strong></a>
</div>
<p>
</td>
<td>
<a href="create-custom-experience.md">
<img alt="만들기" src="../assets/do-not-localize/inapp-create.jpeg">
</a>
<div>
<a href="create-custom-experience.md"><strong>사용자 지정 채널 경험 만들기</strong></a>
</div>
<p>
</td>
<td>
<a href="monitor-custom-channel.md">
<img alt="모니터" src="../assets/do-not-localize/inapp-report.jpg">
</a>
<div>
<a href="monitor-custom-channel.md"><strong>사용자 지정 채널 모니터링</strong></a>
</div>
<p>
</td>
</tr></table>

<!--
## Next steps {#next-steps}

* Review the prerequisites and permissions before setting up your first custom channel. [Learn more](custom-channel-prerequisites.md)
* Configure your first custom channel using the Channel Builder. [Learn more](custom-channel-configuration.md)
* Create a custom channel experience in a journey or campaign. [Learn more](create-custom-experience.md)
-->
