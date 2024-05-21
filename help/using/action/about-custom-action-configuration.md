---
solution: Journey Optimizer
product: journey optimizer
title: 사용자 정의 액션 구성
description: 사용자 지정 작업을 구성하는 방법 알아보기
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: 작업, 서드파티, 사용자 지정, 여정, API
exl-id: 4df2fc7c-85cb-410a-a31f-1bc1ece237bb
source-git-commit: 12423d9fe07e5c757154ae4f732ff20ec6dc2427
workflow-type: tm+mt
source-wordcount: '1799'
ht-degree: 17%

---

# 사용자 정의 액션 구성 {#configure-an-action}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_configuration"
>title="사용자 정의 작업"
>abstract="서드파티 시스템을 사용하여 메시지를 보내거나 서드파티 시스템으로 API 호출을 보내려는 경우, 사용자 정의 액션을 사용하여 여정에 대한 연결을 구성합니다. 예를 들어 사용자 정의 액션으로 Epsilon, Slack, [Adobe Developer](https://developer.adobe.com), Firebase 등의 시스템에 연결할 수 있습니다."

서드파티 시스템을 사용하여 메시지를 보내거나 서드파티 시스템으로 API 호출을 보내려는 경우, 사용자 정의 액션을 사용하여 여정에 대한 연결을 구성합니다. 예를 들어 사용자 지정 작업으로 Epsilon, Slack, [Adobe Developer](https://developer.adobe.com){target="_blank"}, Firebase 등

사용자 지정 작업은 기술 사용자가 정의하고 마케터가 사용할 수 있는 추가 작업입니다. 구성하고 나면 여정 왼쪽 팔레트의 **[!UICONTROL 작업]** 범주. [이 페이지](../building-journeys/about-journey-activities.md#action-activities)에서 자세히 알아보십시오.

## 제한 사항{#custom-actions-limitations}

사용자 지정 작업은에 나열된 몇 가지 제한 사항이 있습니다. [이 페이지](../start/guardrails.md).

사용자 지정 작업 매개 변수에서 간단한 컬렉션과 개체 컬렉션을 전달할 수 있습니다. 의 컬렉션 제한에 대해 자세히 알아보기 [이 페이지](../building-journeys/collections.md#limitations).

또한 사용자 지정 작업 매개 변수에는 예상 형식(예: 문자열, 십진수 등)이 있습니다. 이러한 예상 형식을 준수하도록 주의해야 합니다. 자세히 알아보기 [사용 사례](../building-journeys/collections.md).

사용자 지정 작업은 을 사용하는 경우에만 JSON 형식을 지원합니다. [요청](../action/about-custom-action-configuration.md#define-the-message-parameters) 또는 [응답 페이로드](../action/action-response.md).

## 모범 사례{#custom-action-enhancements-best-practices}

사용자 정의 작업을 사용하여 타깃팅할 엔드포인트를 선택할 때 다음을 확인하십시오.

* 이 엔트포인트는 제한하는 [Throttling API](../configuration/throttling.md) 또는 [Capping API](../configuration/capping.md)의 구성을 사용하여 여정의 처리량을 지원할 수 있습니다. 스로틀링 구성은 200TPS 미만일 수 없습니다. 타겟팅된 모든 엔드포인트는 최소 200개의 TPS를 지원해야 합니다.
* 이 엔드포인트는 가능한 한 낮은 응답 시간을 가져야 합니다. 예상 처리량에 따라 응답 시간이 길면 실제 처리량에 영향을 줄 수 있습니다.

모든 사용자 지정 작업에 대해 1분 동안 30만 번의 최대 호출 제한이 정의됩니다. 또한 기본 캡핑은 호스트 및 샌드박스 별로 수행됩니다. 예를 들어 한 샌드박스에서 동일한 호스트를 사용하는 두 개의 엔드포인트가 있는 경우(예: `https://www.adobe.com/endpoint1` 및 `https://www.adobe.com/endpoint2`) 빈도 설정은 adobe.com 호스트 아래의 모든 엔드포인트에 대해 적용됩니다. &quot;endpoint1&quot;과 &quot;endpoint2&quot;는 동일한 최대 가용량 구성을 공유하며 한 끝점이 한도에 도달하면 다른 끝점에 영향을 줍니다.

이 제한은 사용자 정의 작업으로 타깃팅된 외부 끝점을 보호하기 위해 고객 사용량을 기준으로 설정되었습니다. 대상자 기반 여정에서 이를 고려하여 적절한 읽기 속도(사용자 정의 작업 사용 시 프로필 5,000개/초)를 정의해야 합니다. 필요한 경우 Capping/Throttling API를 통해 빈도 설정 또는 스로틀링 제한을 보다 크게 정의하는 방법으로 이 설정을 재정의할 수 있습니다. [이 페이지](../configuration/external-systems.md)를 참조하십시오.

다음과 같은 다양한 이유로 사용자 지정 작업으로 공개 끝점을 타깃팅해서는 안 됩니다.

* 적절한 제한 또는 제한이 없으면 이러한 볼륨을 지원하지 않을 수 있는 공개 끝점에 너무 많은 호출을 보낼 위험이 있습니다.
* 프로필 데이터는 사용자 지정 작업을 통해 전송될 수 있으므로 공개 엔드포인트를 타겟팅하면 의도치 않게 외부적으로 개인 정보를 공유할 수 있습니다.
* 공개 끝점에서 반환되는 데이터에 대해 제어할 수 없습니다. 엔드포인트가 API를 변경하거나 잘못된 정보를 보내기 시작하는 경우 전송된 통신에서 사용할 수 있게 되고 부정적인 영향이 발생할 수 있습니다.

## 동의 및 데이터 거버넌스 {#privacy}

Journey Optimizer에서는 데이터 거버넌스 및 동의 정책을 사용자 지정 작업에 적용하여 특정 필드가 서드파티 시스템으로 내보내지지 않도록 하거나 이메일, 푸시 또는 SMS 통신 수신에 동의하지 않은 고객을 제외할 수 있습니다. 자세한 내용은 다음 페이지를 참조하십시오.

* [데이터 거버넌스](../action/action-privacy.md).
* [동의](../action/action-privacy.md).


## 구성 단계 {#configuration-steps}

사용자 지정 작업을 구성하는 데 필요한 주요 단계는 다음과 같습니다.

1. 관리 메뉴 섹션에서 다음을 선택합니다. **[!UICONTROL 구성]**. 다음에서  **[!UICONTROL 작업]** 섹션, 클릭 **[!UICONTROL 관리]**. 클릭 **[!UICONTROL 작업 만들기]** 새 작업을 만듭니다. 작업 구성 창이 화면 오른쪽에 열립니다.

   ![](assets/custom2.png)

1. 작업 이름을 입력합니다.

   >[!NOTE]
   >
   >영숫자와 밑줄만 허용됩니다. 최대 길이는 30자입니다.

1. 작업에 설명을 추가합니다. 데이터 소스에 이벤트에 설명을 추가합니다.
1. 이 작업을 사용하는 여정 수는 **[!UICONTROL 다음에서 사용됨]** 필드. 다음을 클릭할 수 있습니다 **[!UICONTROL 여정 보기]** 단추를 클릭하여 이 작업을 사용하는 여정 목록을 표시합니다.
1. 다른 항목 정의 **[!UICONTROL URL 구성]** 매개 변수. [이 페이지](../action/about-custom-action-configuration.md#url-configuration)를 참조하십시오.
1. 구성 **[!UICONTROL 인증]** 섹션. 이 구성은 데이터 소스의 경우와 동일합니다.  [이 섹션](../datasource/external-data-sources.md#custom-authentication-mode)을 참조하십시오.
1. 다음을 정의합니다. **[!UICONTROL 작업 매개 변수]**. [이 페이지](../action/about-custom-action-configuration.md#define-the-message-parameters)를 참조하십시오.
1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

   이제 사용자 지정 작업이 구성되었으며 여정에서 사용할 준비가 되었습니다. [이 페이지](../building-journeys/about-journey-activities.md#action-activities)를 참조하십시오.

   >[!NOTE]
   >
   >여정에서 사용자 지정 작업을 사용하는 경우 대부분의 매개 변수는 읽기 전용입니다. 다음 작업만 수정할 수 있습니다. **[!UICONTROL 이름]**, **[!UICONTROL 설명]**, **[!UICONTROL URL]** 필드 및 **[!UICONTROL 인증]** 섹션.

## 끝점 구성 {#url-configuration}

사용자 지정 작업을 구성할 때 다음을 정의해야 합니다 **[!UICONTROL 끝점 구성]** 매개 변수:

![](assets/action-response1bis.png){width="70%" align="left"}

1. 다음에서 **[!UICONTROL URL]** 필드에 외부 서비스의 URL을 지정합니다.

   * URL이 정적인 경우 이 필드에 URL을 입력합니다.

   * URL에 동적 경로가 포함된 경우 URL의 정적 부분, 즉 체계, 호스트, 포트 및 경로의 정적 부분(선택 사항)만 입력합니다.

     예: `https://xxx.yyy.com/somethingstatic/`

     사용자 지정 작업을 여정에 추가할 때 URL의 동적 경로를 지정합니다. [자세히 알아보기](../building-journeys/using-custom-actions.md).

   >[!NOTE]
   >
   >보안상의 이유로 URL에 HTTPS 스키마를 사용하는 것이 좋습니다. 공개되지 않은 Adobe 주소 및 IP 주소의 사용은 허용되지 않습니다.
   >
   >사용자 지정 작업을 정의할 때 기본 포트만 허용됩니다. http의 경우 80, https의 경우 443.

1. 호출 선택 **[!UICONTROL 방법]**: 다음 중 하나일 수 있습니다. **[!UICONTROL POST]**, **[!UICONTROL GET]** 또는 **[!UICONTROL PUT]**.

   >[!NOTE]
   >
   > 다음 **DELETE** 메서드가 지원되지 않습니다. 기존 리소스를 업데이트해야 하는 경우 **PUT** 메서드를 사용합니다.

1. 헤더 및 쿼리 매개 변수를 정의합니다.

   * 다음에서 **[!UICONTROL 헤더]** 섹션, 클릭 **[!UICONTROL 헤더 필드 추가]** 외부 서비스로 보낼 요청 메시지의 HTTP 헤더를 정의합니다. 다음 **[!UICONTROL Content-Type]** 및 **[!UICONTROL Charset]** 헤더 필드는 기본적으로 설정됩니다. 이러한 필드는 삭제할 수 없습니다. 만 **[!UICONTROL Content-Type]** 머리글은 수정할 수 있습니다. 해당 값은 JSON 형식을 준수해야 합니다. 기본값은 다음과 같습니다.

   ![](assets/content-type-header.png)

   * 다음에서 **[!UICONTROL 쿼리 매개 변수]** 섹션, 클릭 **[!UICONTROL 쿼리 매개 변수 필드 추가]** 를 사용하여 URL에 추가할 매개 변수를 정의할 수 있습니다.

   ![](assets/journeyurlconfiguration2bis.png)

1. 필드의 레이블 또는 이름을 입력합니다.

1. 유형을 선택합니다. **[!UICONTROL 상수]** 또는 **[!UICONTROL 변수]**. 을(를) 선택한 경우 **[!UICONTROL 상수]**&#x200B;을(를) 만든 다음 **[!UICONTROL 값]** 필드. 을(를) 선택한 경우 **[!UICONTROL 변수]**&#x200B;를 설치한 다음 여정에 사용자 지정 작업을 추가할 때 이 변수를 지정합니다. [자세히 알아보기](../building-journeys/using-custom-actions.md).

   ![](assets/journeyurlconfiguration2.png)

   >[!NOTE]
   >
   >여정에 사용자 지정 작업을 추가한 후에도 여정이 초안 상태인 경우 헤더 또는 쿼리 매개 변수 필드를 추가할 수 있습니다. 여정이 구성 변경의 영향을 받지 않도록 하려면 사용자 지정 작업을 복제하고 필드를 새 사용자 지정 작업에 추가합니다.
   >
   >헤더는 필드 구문 분석 규칙에 따라 유효성이 검사됩니다. 다음에서 자세히 알아보기 [이 설명서](https://tools.ietf.org/html/rfc7230#section-3.2.4){_blank}.

## 페이로드 매개 변수 정의 {#define-the-message-parameters}

1. 다음에서 **[!UICONTROL 요청]** 섹션에 외부 서비스로 전송할 JSON 페이로드의 예제를 붙여 넣습니다. 이 필드는 선택 사항이며 POST 및 PUT 호출 메서드에만 사용할 수 있습니다.

1. 다음에서 **[!UICONTROL 응답]** 섹션에 호출에서 반환된 페이로드의 예제를 붙여 넣습니다. 이 필드는 선택 사항이며 모든 호출 방법에서 사용할 수 있습니다. 사용자 지정 작업에서 API 호출 응답을 활용하는 방법에 대한 자세한 내용은 다음을 참조하십시오. [이 페이지](../action/action-response.md).

>[!NOTE]
>
>응답 기능은 현재 Beta 버전으로 제공됩니다.

![](assets/action-response2bis.png){width="70%" align="left"}

>[!NOTE]
>
>페이로드 예는 null 값을 포함할 수 없습니다. 페이로드의 필드 이름에는 &quot;.&quot;를 사용할 수 없습니다. 표시합니다. &quot;$&quot; 문자로 시작할 수 없습니다.

매개 변수 유형(예: 문자열, 정수 등)을 정의할 수 있습니다.

매개 변수가 상수인지 변수인지 지정할 것인지 선택할 수도 있습니다.

* **상수** 는 매개 변수 값이 기술 담당자에 의해 작업 구성 창에서 정의됨을 의미합니다. 값은 여정 간에 항상 동일합니다. 여정에서 사용자 지정 작업을 사용할 때 변경되지 않으며 마케터가 표시되지 않습니다. 예를 들어 서드파티 시스템에서 예상하는 ID일 수 있습니다. 이 경우 상수/변수 전환 오른쪽에 있는 필드가 전달된 값입니다.
* **변수** 는 매개 변수의 값이 달라짐을 의미합니다. 여정에서 이 사용자 지정 작업을 사용하는 마케터는 원하는 값을 전달하거나 이 매개 변수에 대한 값을 검색할 위치를 지정할 수 있습니다(예: 이벤트, Adobe Experience Platform 등). 이 경우 전환 상수/변수 오른쪽의 필드는 마케터가 여정에서 이 매개 변수의 이름을 지정하는 레이블입니다.

![](assets/customactionpayloadmessage2.png)

## mTLS 프로토콜 지원 {#mtls-protocol-support}

이제 mTLS(상호 전송 계층 보안)를 사용하여 HTTP API 대상 및 Adobe Journey Optimizer 사용자 지정 작업에 대한 아웃바운드 연결에서 보안을 강화할 수 있습니다. mTLS는 상호 인증을 위한 종단간 보안 방법으로, 정보를 공유하는 양 당사자가 데이터를 공유하기 전에 자신이 주장하는 사람임을 보장합니다. mTLS에는 TLS와 비교하여 추가 단계가 포함되어 있으며, 이 단계에서 서버는 클라이언트의 인증서를 요청하고 마지막에 검증한다.

Adobe Journey Optimizer에서 mTLS는 사용자 지정 작업과 함께 사용됩니다. mTLS를 활성화하기 위해 Adobe Journey Optimizer 사용자 지정 작업에 대한 추가 구성이 필요하지 않습니다. 사용자 지정 작업의 끝점이 mTLS를 사용하는 경우 시스템은 Adobe Experience Platform 키 저장소에서 인증서를 가져와 자동으로 끝점에 제공합니다(mTLS 연결에 필요한 경우).

이러한 Adobe Journey Optimizer 및 Experience Platform HTTP API 대상 워크플로우에서 mTLS를 사용하려면 Adobe Journey Optimizer 고객 작업 UI 또는 대상 UI에 입력하는 서버 주소에 TLS 프로토콜이 비활성화되어 있고 mTLS만 활성화되어야 합니다. 해당 끝점에서 TLS 1.2 프로토콜이 여전히 활성화되어 있으면 클라이언트 인증을 위한 인증서가 전송되지 않습니다. 즉, 이러한 워크플로우에서 mTLS를 사용하려면 &quot;수신&quot; 서버 엔드포인트가 mTLS여야 합니다 **전용** 연결 끝점을 사용하도록 설정했습니다.

>[!IMPORTANT]
>
>mTLS를 활성화하기 위해 Adobe Journey Optimizer 사용자 지정 작업 또는 여정에 추가 구성이 필요하지 않습니다. 이 프로세스는 mTLS 지원 끝점이 검색될 때 자동으로 발생합니다. 각 인증서에 대한 일반 이름(CN) 및 주체 대체 이름(SAN)은 인증서의 일부로 설명서에서 사용할 수 있으며, 원할 경우 소유권 유효성 검사의 추가 계층으로 사용할 수 있습니다.
>
>2000년 5월에 게시된 RFC 2818은 주체 이름 확인을 위해 HTTPS 인증서의 CN(일반 이름) 필드를 사용하는 것을 중단합니다. 대신 &quot;dns name&quot; 유형의 &quot;SAN(주체 대체 이름)&quot;을 사용하는 것이 좋습니다.

CN 또는 SAN을 확인하여 추가 타사 유효성 검사를 수행하려면 여기에서 관련 인증서를 다운로드할 수 있습니다.

```
Prod:
{
    "serviceName": "AJO Journeys",
    "publicCertificate": "-----BEGIN CERTIFICATE-----
MIIG9TCCBd2gAwIBAgIQBX+pDP5hB0gqDzFKyq5wLjANBgkqhkiG9w0BAQsFADBZ
MQswCQYDVQQGEwJVUzEVMBMGA1UEChMMRGlnaUNlcnQgSW5jMTMwMQYDVQQDEypE
aWdpQ2VydCBHbG9iYWwgRzIgVExTIFJTQSBTSEEyNTYgMjAyMCBDQTEwHhcNMjQw
NTA5MDAwMDAwWhcNMjUwNjA5MjM1OTU5WjB0MQswCQYDVQQGEwJVUzETMBEGA1UE
CBMKQ2FsaWZvcm5pYTERMA8GA1UEBxMIU2FuIEpvc2UxEzARBgNVBAoTCkFkb2Jl
IEluYy4xKDAmBgNVBAMTH2Fqby1qb3VybmV5cy5hZXAtbXRscy5hZG9iZS5jb20w
ggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQDaI8HZHzbmPEgTy9O7cYmq
ZVX5283Gw7j7v4/O810jZXItBDmsSiWotvTgAT0s2oZMZZ6tGPbQB7hL+xJJ+yu2
HxFl1WzB4UGHJ+UbrL94hI930xQs0FVgSOGgIarj5HucF2ZxwHIkVHY5whrOq9t4
UxFBG0siUPQrTzV9GfA0wREElugpTbwaM8CTWwOQ9ekroOD2C5zAcLTycXFtSMiU
B4L4u38S9hGoBByzzKv9GnUMQudvt/s5zsGykZgEEYeN6IitfVO6BOD9jT94Aytx
/O3XH5w8v4KNTn+An99bXFmyg3JRUFSYZFxha8s1f6uu0XbdToQ+ao0WkE06nMmV
AgMBAAGjggOcMIIDmDAfBgNVHSMEGDAWgBR0hYDAZsffN97PvSk3qgMdvu3NFzAd
BgNVHQ4EFgQUn8OqtzccNdrsb+fbRnTHmtTZxLMwKgYDVR0RBCMwIYIfYWpvLWpv
dXJuZXlzLmFlcC1tdGxzLmFkb2JlLmNvbTA+BgNVHSAENzA1MDMGBmeBDAECAjAp
MCcGCCsGAQUFBwIBFhtodHRwOi8vd3d3LmRpZ2ljZXJ0LmNvbS9DUFMwDgYDVR0P
AQH/BAQDAgWgMB0GA1UdJQQWMBQGCCsGAQUFBwMBBggrBgEFBQcDAjCBnwYDVR0f
BIGXMIGUMEigRqBEhkJodHRwOi8vY3JsMy5kaWdpY2VydC5jb20vRGlnaUNlcnRH
bG9iYWxHMlRMU1JTQVNIQTI1NjIwMjBDQTEtMS5jcmwwSKBGoESGQmh0dHA6Ly9j
cmw0LmRpZ2ljZXJ0LmNvbS9EaWdpQ2VydEdsb2JhbEcyVExTUlNBU0hBMjU2MjAy
MENBMS0xLmNybDCBhwYIKwYBBQUHAQEEezB5MCQGCCsGAQUFBzABhhhodHRwOi8v
b2NzcC5kaWdpY2VydC5jb20wUQYIKwYBBQUHMAKGRWh0dHA6Ly9jYWNlcnRzLmRp
Z2ljZXJ0LmNvbS9EaWdpQ2VydEdsb2JhbEcyVExTUlNBU0hBMjU2MjAyMENBMS0x
LmNydDAMBgNVHRMBAf8EAjAAMIIBfwYKKwYBBAHWeQIEAgSCAW8EggFrAWkAdwBO
daMnXJoQwzhbbNTfP1LrHfDgjhuNacCx+mSxYpo53wAAAY9ecsWsAAAEAwBIMEYC
IQDQclgq89ZVlwdYBJFEIs8q4WIcZ9Siw+jb9OgCrz+wjwIhALQLnC1WyT+dHjvY
FvZjc99WkjnEwhIevj/Rz7r0EzhmAHUAfVkeEuF4KnscYWd8Xv340IdcFKBOlZ65
Ay/ZDowuebgAAAGPXnLF5AAABAMARjBEAiBy9cNT3CnmSMOdJe+JbG8f7ha1UGgN
TdDlaR9x9fKmKQIgNmGjz5AzP1evB2G1TTvVLkHfWQw0864c4F23WSV+6TsAdwDP
EVbu1S58r/OHW9lpLpvpGnFnSrAX7KwB0lt3zsw7CAAAAY9ecsYnAAAEAwBIMEYC
IQCTcB7s1xDP8Olif3jj4X8jHgVxv5C3bTvG6wDYBByfcQIhAOt8PhR6tWSLtF1V
HB8r7dns7Oth1+QT7WMonQZsP/3WMA0GCSqGSIb3DQEBCwUAA4IBAQAjTy45fbQV
aVTZ71wcIyHnkJfq/8SSc/UNT5//6AMiV6kb3YsFW1+EaQ1wPHZS0Qfjs7aIsXi5
f2TCGps8onELNpOfFfptrOCMfcYGMvV1wPCBy+kuoGY/YRZlsdNUTTzQAGztfRev
79w+XIDzioCrY+sfyUkkw+N/F7/RIjzMKjP6onSfuD+5WjqVKq9kFE0fCyJixedV
BPoPM4Cktgvc9SsK17JmLWkg+V2yH1eDzmjF3sR0/dcmoAM0qgV/CDuhIIqX2o7m
3/aQSNsPUpgBVbkz+SjEtchmw8DXW/Kro8QVulsXdbkiLTOj4JopxdOzrbKgWMwr
pIw7KKJoktDk
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
MIIEyDCCA7CgAwIBAgIQDPW9BitWAvR6uFAsI8zwZjANBgkqhkiG9w0BAQsFADBh
MQswCQYDVQQGEwJVUzEVMBMGA1UEChMMRGlnaUNlcnQgSW5jMRkwFwYDVQQLExB3
d3cuZGlnaWNlcnQuY29tMSAwHgYDVQQDExdEaWdpQ2VydCBHbG9iYWwgUm9vdCBH
MjAeFw0yMTAzMzAwMDAwMDBaFw0zMTAzMjkyMzU5NTlaMFkxCzAJBgNVBAYTAlVT
MRUwEwYDVQQKEwxEaWdpQ2VydCBJbmMxMzAxBgNVBAMTKkRpZ2lDZXJ0IEdsb2Jh
bCBHMiBUTFMgUlNBIFNIQTI1NiAyMDIwIENBMTCCASIwDQYJKoZIhvcNAQEBBQAD
ggEPADCCAQoCggEBAMz3EGJPprtjb+2QUlbFbSd7ehJWivH0+dbn4Y+9lavyYEEV
cNsSAPonCrVXOFt9slGTcZUOakGUWzUb+nv6u8W+JDD+Vu/E832X4xT1FE3LpxDy
FuqrIvAxIhFhaZAmunjZlx/jfWardUSVc8is/+9dCopZQ+GssjoP80j812s3wWPc
3kbW20X+fSP9kOhRBx5Ro1/tSUZUfyyIxfQTnJcVPAPooTncaQwywa8WV0yUR0J8
osicfebUTVSvQpmowQTCd5zWSOTOEeAqgJnwQ3DPP3Zr0UxJqyRewg2C/Uaoq2yT
zGJSQnWS+Jr6Xl6ysGHlHx+5fwmY6D36g39HaaECAwEAAaOCAYIwggF+MBIGA1Ud
EwEB/wQIMAYBAf8CAQAwHQYDVR0OBBYEFHSFgMBmx9833s+9KTeqAx2+7c0XMB8G
A1UdIwQYMBaAFE4iVCAYlebjbuYP+vq5Eu0GF485MA4GA1UdDwEB/wQEAwIBhjAd
BgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwdgYIKwYBBQUHAQEEajBoMCQG
CCsGAQUFBzABhhhodHRwOi8vb2NzcC5kaWdpY2VydC5jb20wQAYIKwYBBQUHMAKG
NGh0dHA6Ly9jYWNlcnRzLmRpZ2ljZXJ0LmNvbS9EaWdpQ2VydEdsb2JhbFJvb3RH
Mi5jcnQwQgYDVR0fBDswOTA3oDWgM4YxaHR0cDovL2NybDMuZGlnaWNlcnQuY29t
L0RpZ2lDZXJ0R2xvYmFsUm9vdEcyLmNybDA9BgNVHSAENjA0MAsGCWCGSAGG/WwC
ATAHBgVngQwBATAIBgZngQwBAgEwCAYGZ4EMAQICMAgGBmeBDAECAzANBgkqhkiG
9w0BAQsFAAOCAQEAkPFwyyiXaZd8dP3A+iZ7U6utzWX9upwGnIrXWkOH7U1MVl+t
wcW1BSAuWdH/SvWgKtiwla3JLko716f2b4gp/DA/JIS7w7d7kwcsr4drdjPtAFVS
slme5LnQ89/nD/7d+MS5EHKBCQRfz5eeLjJ1js+aWNJXMX43AYGyZm0pGrFmCW3R
bpD0ufovARTFXFZkAdl9h6g4U5+LXUZtXMYnhIHUfoyMo5tS58aI7Dd8KvvwVVo4
chDYABPPTHPbqjc1qCmBaZx2vN4Ye5DUys/vZwP9BFohFrH/6j/f3IL16/RZkiMN
JCqVJUzKoZHm1Lesh3Sz8W2jmdv51b2EQJ8HmA==
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
MIIDjjCCAnagAwIBAgIQAzrx5qcRqaC7KGSxHQn65TANBgkqhkiG9w0BAQsFADBh
MQswCQYDVQQGEwJVUzEVMBMGA1UEChMMRGlnaUNlcnQgSW5jMRkwFwYDVQQLExB3
d3cuZGlnaWNlcnQuY29tMSAwHgYDVQQDExdEaWdpQ2VydCBHbG9iYWwgUm9vdCBH
MjAeFw0xMzA4MDExMjAwMDBaFw0zODAxMTUxMjAwMDBaMGExCzAJBgNVBAYTAlVT
MRUwEwYDVQQKEwxEaWdpQ2VydCBJbmMxGTAXBgNVBAsTEHd3dy5kaWdpY2VydC5j
b20xIDAeBgNVBAMTF0RpZ2lDZXJ0IEdsb2JhbCBSb290IEcyMIIBIjANBgkqhkiG
9w0BAQEFAAOCAQ8AMIIBCgKCAQEAuzfNNNx7a8myaJCtSnX/RrohCgiN9RlUyfuI
2/Ou8jqJkTx65qsGGmvPrC3oXgkkRLpimn7Wo6h+4FR1IAWsULecYxpsMNzaHxmx
1x7e/dfgy5SDN67sH0NO3Xss0r0upS/kqbitOtSZpLYl6ZtrAGCSYP9PIUkY92eQ
q2EGnI/yuum06ZIya7XzV+hdG82MHauVBJVJ8zUtluNJbd134/tJS7SsVQepj5Wz
tCO7TG1F8PapspUwtP1MVYwnSlcUfIKdzXOS0xZKBgyMUNGPHgm+F6HmIcr9g+UQ
vIOlCsRnKPZzFBQ9RnbDhxSJITRNrw9FDKZJobq7nMWxM4MphQIDAQABo0IwQDAP
BgNVHRMBAf8EBTADAQH/MA4GA1UdDwEB/wQEAwIBhjAdBgNVHQ4EFgQUTiJUIBiV
5uNu5g/6+rkS7QYXjzkwDQYJKoZIhvcNAQELBQADggEBAGBnKJRvDkhj6zHd6mcY
1Yl9PMWLSn/pvtsrF9+wX3N3KjITOYFnQoQj8kVnNeyIv/iPsGEMNKSuIEyExtv4
NeF22d+mQrvHRAiGfzZ0JFrabA0UWTW98kndth/Jsw1HKj2ZL7tcu7XUIOGZX1NG
Fdtom/DzMNU+MeKNhJ7jitralj41E6Vf8PlwUHBHQRFXGU7Aj64GxJUTFy8bJZ91
8rGOmaFvE7FBcf6IKshPECBV1/MUReXgRPTqh5Uykw7+U0b6LJ3/iyK5S9kJRaTe
pLiaWN0bfVKfjllDiIGknibVb63dDcY3fe0Dkhvld1927jyNxF1WW6LZZm6zNTfl
MrY=
-----END CERTIFICATE-----",
    "expiryDate": "2025-06-09T23:59:59Z"
}
```

