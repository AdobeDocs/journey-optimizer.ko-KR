---
title: 사용자 지정 채널 구성 - 개요
description: 채널 만들기에서 채널 구성 설정에 이르기까지 Adobe Journey Optimizer에서 사용자 지정 채널을 구성하기 위해 관리자가 완료해야 하는 단계에 대해 알아봅니다.
feature: Channel Configuration
topic: Content Management
role: Admin
level: Experienced
badge: label="제한 공개" type="Informative"
source-git-commit: 4556e8b50fe71cf9d703d034a3c5772b8fea9d33
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 9%

---


# 사용자 지정 채널 구성 {#custom-channel-configuration}

>[!AVAILABILITY]
>
>이 기능은 제한적으로 이용할 수 있습니다. 액세스 권한을 얻으려면 Adobe 담당자에게 문의하십시오.

사용자 지정 채널 구성은 채널당 한 번 발생하는 관리자 작업입니다. 채널이 구성되면 마케터는 모든 기본 [!DNL Journey Optimizer] 채널과 마찬가지로 캠페인, 여정 및 오케스트레이션된 캠페인에서 즉시 선택할 수 있습니다.

구성 프로세스에는 채널 자체(엔드포인트, 인증, 페이로드)를 정의하고, 요청을 인증하는 데 사용되는 API 자격 증명을 관리하고, 선택적으로 링크 추적을 위해 하위 도메인을 위임하고, 마지막으로 마케터가 작성 시 선택할 채널 구성을 만드는 네 가지 단계가 포함됩니다.

>[!NOTE]
>
>시작하기 전에 필요한 권한 및 지원되는 인증 방법을 포함하여 사용자 지정 채널에 대한 사전 요구 사항 및 보호 기능을 검토하십시오.

## 구성 단계 {#steps}

사용자 지정 채널에 대한 구성 프로세스는 4단계로 구성됩니다. 각 단계는 아래 링크된 문서에 자세히 설명되어 있습니다.

| 단계 | 작업 | 이것이 중요한 이유 | 링크 |
| --- | --- | --- | --- |
| **1. 사용자 지정 채널 만들기** | 채널 빌더에서 끝점 URL, 헤더, 제한 정책, 인증 유형 및 메시지 페이로드 구조를 정의합니다. | 채널의 핵심 정의입니다. [!DNL Journey Optimizer]에게 메시지를 보내는 방법과 메시지 모양을 알려 줍니다. | [자세히 알아보기](create-custom-channel.md) |
| **2. API 자격 증명 관리** | 엔드포인트에 대한 요청을 인증하는 데 사용되는 자격 증명 세트를 만들고 관리합니다. | 여러 자격 증명 세트를 사용하면 채널을 복제하지 않고 다양한 브랜드 또는 환경에서 동일한 채널 정의를 재사용할 수 있습니다. | [자세히 알아보기](custom-channel-api-credentials.md) |
| **3. 하위 도메인 위임** *(선택 사항)* | 사용자 지정 채널에 맞는 하위 도메인을 위임합니다. | 메시지 페이로드에 추적 가능한 링크가 포함된 경우에만 필요합니다. 위임된 하위 도메인이 없으면 이 채널에 대한 링크 추적을 사용할 수 없습니다. | [자세히 알아보기](custom-channel-subdomains.md) |
| **4. 채널 구성 만들기** | 사용자 지정 채널을 특정 자격 증명 세트, 하위 도메인 및 선택적 페이로드 기본값에 연결하는 이름이 지정된 사전 설정을 만듭니다. | 캠페인 또는 여정을 작성할 때 마케터는 사용자 지정 채널 및 관련 채널 구성을 선택합니다. 동일한 채널에 대해 여러 구성을 만들 수 있습니다(예: 브랜드 또는 지역당 하나). | [자세히 알아보기](custom-channel-configuration.md) |

<!--
## Get started {#get-started}

1. [Create the custom channel](create-custom-channel.md) by defining its endpoint, authentication method, and message payload structure in the Channel Builder.
1. [Set up API credentials](custom-channel-api-credentials.md) to authenticate requests sent to your endpoint — required for all authentication types other than **None**.
1. [Delegate a subdomain](custom-channel-subdomains.md) if your message payload includes trackable links and you want them served from a branded domain.
1. [Create a channel configuration](custom-channel-configuration.md) to produce the named preset that marketers will select when building campaigns and journeys.


-->