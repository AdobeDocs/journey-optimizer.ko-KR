---
solution: Journey Optimizer
product: journey optimizer
title: Sinch 공급자 구성
description: Sinch를 사용하여 Journey Optimizer에서 텍스트 메시지를 보내도록 환경을 구성하는 방법에 대해 알아봅니다
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 85412a85-edf0-4069-8bc7-b80371375f1f
source-git-commit: 3bc212ac7848e1671f5d6b41521152c11b5568b4
workflow-type: tm+mt
source-wordcount: '1146'
ht-degree: 2%

---

# Sinch 공급자 구성 {#sms-configuration-sinch}

Journey Optimizer에서 Sinch 공급자를 사용하는 경우 세 가지 고유한 옵션을 찾을 수 있습니다.

* **SMS 구성**: SMS 메시지를 원활하게 보낼 수 있도록 Sinch API 자격 증명을 설정합니다.

* **MMS 구성**: MMS(멀티미디어 메시지)의 경우 Sinch MMS API 자격 증명을 구성하십시오. 인바운드 메시지 추적 및 응답은 SMS 구성에서 처리합니다. MMS 설정은 MMS 메시지의 아웃바운드 게재에만 해당됩니다.

* **RCS 구성**: RCS 메시지를 원활하게 보내도록 Sinch API 자격 증명을 설정합니다.

## SMS에 대한 API 자격 증명 구성{#create-api}

>[!BEGINSHADEBOX]

옵트인 또는 옵트아웃 키워드가 제공되지 않으면 표준 동의 메시지가 사용자 개인 정보를 보장하는 데 사용됩니다. 사용자 지정 키워드를 추가하면 기본값이 자동으로 재정의됩니다.

**기본 키워드:**

* **옵트인**: 구독, 예, 중지 취소, 시작, 계속, 다시 시작, 시작
* **옵트아웃**: 중지, 종료, 취소, 종료, 구독 취소, 아니요
* **도움말**: 도움말

>[!ENDSHADEBOX]

Journey Optimizer에서 SMS 메시지 및 MMS를 전송하도록 Sinch 공급자를 구성하려면 다음 단계를 수행합니다.

1. 왼쪽 레일에서 **[!UICONTROL 관리]** > **[!UICONTROL 채널]** `>` **[!UICONTROL SMS 설정]**&#x200B;으로 이동한 다음 **[!UICONTROL API 자격 증명]** 메뉴를 선택합니다. **[!UICONTROL 새 API 자격 증명 만들기]** 단추를 클릭합니다.

1. 아래에 자세히 설명된 대로 SMS API 자격 증명을 구성합니다.

   +++ 구성을 위한 SMS 자격 증명 목록

   | 구성 필드 | 설명 |
   |---|---|    
   | SMS 공급업체 | Sinch |
   | 이름 | API 자격 증명의 이름을 선택합니다. |
   | 서비스 ID 및 API 토큰 | API 페이지에 액세스하면 SMS 탭에서 자격 증명을 찾을 수 있습니다. 자세한 내용은 [Sinch 설명서](https://developers.sinch.com/docs/sms/getting-started/){target="_blank"}를 참조하세요. |
   | 옵트인 키워드 | 옵트인 메시지를 자동으로 트리거할 기본 또는 사용자 지정 키워드를 입력합니다. 여러 키워드의 경우 쉼표로 구분된 값을 사용하십시오. |
   | 옵트인 메시지 | 옵트인 메시지로 자동 전송되는 사용자 지정 응답을 입력합니다. |
   | 옵트아웃 키워드 | 옵트아웃 메시지를 자동으로 트리거할 기본 또는 사용자 지정 키워드를 입력합니다. 여러 키워드의 경우 쉼표로 구분된 값을 사용하십시오. |
   | 옵트아웃 메시지 | 옵트아웃 메시지로 자동 전송되는 사용자 지정 응답을 입력합니다. |
   | 도움말 키워드 | **도움말 메시지**&#x200B;를 자동으로 트리거할 기본 또는 사용자 지정 키워드를 입력하십시오. 여러 키워드의 경우 쉼표로 구분된 값을 사용하십시오. |
   | 도움말 메시지 | **도움말 메시지**(으)로 자동으로 전송되는 사용자 지정 응답을 입력하십시오. |
   | 이중 옵트인 키워드 | 이중 옵트인 프로세스를 트리거하는 키워드를 입력합니다. 사용자 프로필이 존재하지 않으면 확인 후 생성됩니다. 여러 키워드의 경우 쉼표로 구분된 값을 사용하십시오. [SMS 이중 옵트인에 대해 자세히 알아보기](https://video.tv.adobe.com/v/3427129/?learn=on). |
   | 이중 옵트인 메시지 | 이중 옵트인 확인에 대한 응답으로 자동으로 전송되는 사용자 지정 응답을 입력합니다. |
   | 인바운드 번호 | 고유한 인바운드 번호 또는 짧은 코드를 추가합니다. 이를 통해 서로 다른 샌드박스에서 동일한 API 자격 증명을 사용할 수 있습니다. 각 샌드박스는 고유한 인바운드 번호 또는 짧은 코드를 갖습니다. |
   | 사용자 지정 인바운드 키워드 | 특정 작업(예: 할인, 오퍼, 등록)에 대한 고유 키워드를 정의합니다. 이러한 키워드는 프로필의 속성으로 캡처 및 저장되므로 여정 내에서 스트리밍 세그먼트 자격을 트리거하고 사용자 지정된 응답 또는 작업을 제공할 수 있습니다. |
   | 기본 인바운드 회신 메시지 | 최종 사용자가 정의된 키워드와 일치하지 않는 인바운드 SMS를 전송할 때 전송되는 기본 응답을 입력합니다. |
   | URL 재정의 | SMS 게재 보고서, 피드백 데이터, 인바운드 메시지 또는 이벤트 알림의 기본 끝점을 대체할 사용자 지정 URL을 입력합니다. Sinch는 사전 정의된 업데이트 대신 이 URL에 관련된 모든 업데이트를 보냅니다. |

   +++

1. **[!UICONTROL 유사 옵트아웃]** 옵션을 활성화하여 옵트아웃 키워드와 유사한 메시지(예: &#39;CANCIL&#39;)를 감지하고 **[!UICONTROL 유사 자동 회신]** 필드에서 확인 회신을 사용자 지정합니다.

   **[!UICONTROL 퍼지 옵트아웃]**&#x200B;은(는) 메시지가 정의된 옵트아웃 키워드와 정확히 일치하지 않더라도 사용자가 구독을 취소하려고 함을 나타내는 SMS 메시지를 식별합니다. 일반적인 옵트아웃 구문과 특정 공격 용어를 탐지할 수 있으므로 캠페인이 사용자 환경 설정을 준수하고 규정을 준수하도록 하는 데 도움이 됩니다.

1. API 자격 증명 구성을 마치면 **[!UICONTROL 제출]**&#x200B;을 클릭합니다.

1. **[!UICONTROL API 자격 증명]** 메뉴에서 bin 아이콘을 클릭하여 API 자격 증명을 삭제합니다.

1. 기존 자격 증명을 수정하려면 원하는 API 자격 증명을 찾은 다음 **[!UICONTROL 편집]** 옵션을 클릭하여 필요한 변경을 수행합니다.

1. 기존 API 자격 증명에서 **[!UICONTROL SMS 연결 확인]**&#x200B;을 클릭하여 샘플 메시지를 지정된 장치로 보내 SMS API 자격 증명을 테스트하고 확인합니다.

1. **숫자** 및 **메시지** 필드를 입력하고 **[!UICONTROL 연결 확인]**&#x200B;을 클릭합니다.

   >[!IMPORTANT]
   >
   >공급자의 페이로드 형식에 맞게 메시지를 구조화해야 합니다.

   ![](assets/verify-connection.png)

API 자격 증명을 만들고 구성한 후에는 SMS 메시지에 대한 채널 구성을 만들어야 합니다. [자세히 알아보기](sms-configuration-surface.md)

## MMS에 대한 API 자격 증명 구성{#sinch-mms}

>[!IMPORTANT]
>
> MMS 설정과 함께 인바운드 메시지 추적 및 동의 요청 관리를 위한 Sinch API 자격 증명을 특별히 만들어야 합니다.

Journey Optimizer을 사용하여 MMS를 전송하도록 Sinch MMS를 구성하려면 다음 단계를 수행합니다.

1. 왼쪽 레일에서 **[!UICONTROL 관리]** > **[!UICONTROL 채널]** `>` **[!UICONTROL SMS 설정]**&#x200B;으로 이동한 다음 **[!UICONTROL API 자격 증명]** 메뉴를 선택합니다. **[!UICONTROL 새 API 자격 증명 만들기]** 단추를 클릭합니다.

1. 아래에 자세히 설명된 대로 MMS API 자격 증명을 구성합니다.

   * **[!UICONTROL SMS 공급업체]**: Sinch MMS.

   * **[!UICONTROL 이름]**: API 자격 증명의 이름을 선택하십시오.

   * **[!UICONTROL 프로젝트 ID]**, **[!UICONTROL 앱 ID]** 및 **[!UICONTROL API 토큰]**: 아래 단계에 따라 MMS API 자격 증명을 수집합니다.

      * **[!UICONTROL 프로젝트 ID]** 및 **[!UICONTROL 앱 ID]**&#x200B;의 경우: Sinch 대시보드에서 Sinch 프로젝트의 [대화 API 개요](https://dashboard.sinch.com/convapi/overview) 페이지에 액세스합니다.
      * **[!UICONTROL API 토큰]**&#x200B;의 경우: Sinch 프로젝트에 대한 [액세스 키](https://community.sinch.com/t5/Customer-Dashboard/Sinch-Access-Keys/ta-p/12638)를 가져와 Sinch 프로젝트 **액세스 키**&#x200B;에서 **Base64 API 토큰**&#x200B;을(를) 생성합니다.

1. API 자격 증명 구성을 마치면 **[!UICONTROL 제출]**&#x200B;을 클릭합니다.

1. **[!UICONTROL API 자격 증명]** 메뉴에서 bin 아이콘을 클릭하여 API 자격 증명을 삭제합니다.

1. 기존 자격 증명을 수정하려면 원하는 API 자격 증명을 찾은 다음 **[!UICONTROL 편집]** 옵션을 클릭하여 필요한 변경을 수행합니다.

API 자격 증명을 만들고 구성한 후에는 MMS 메시지에 대한 채널 구성을 만들어야 합니다. [자세히 알아보기](sms-configuration-surface.md)


## RCS에 대한 API 자격 증명 구성

<!--![](assets/do-not-localize/rcs-sms.png)-->

RCS(Rich Communication Services) 메시징은 Sinch를 통해 Journey Optimizer에서 지원되므로 로고 및 발신자 이름과 같은 브랜딩 요소가 있는 검증된 비즈니스 프로필을 사용하여 기본 메시지를 보낼 수 있습니다.

프로필의 장치가 RCS를 지원하지 않거나 일시적으로 RCS를 통해 연결할 수 없는 경우 메시지는 자동으로 SMS로 대체됩니다.

<!--
### Basic RCS Messages

>[!AVAILABILITY]
>
> Basic RCS messages is only available upon Adobe RCS add-on offering.

1. **Set up your branded RCS agent**

    Create a branded RCS agent in the Sinch Dashboard. [Learn more on branded RCS agent](https://community.sinch.com/t5/RCS/Getting-Started-with-RCS-using-Conversation-API/ta-p/17844)

1. **Set up your [Custom API credentials](sms-configuration-custom.md)**
    
    Once your RCS agent is approved, you need to set up your Sinch API credentials, which include your access key, secret, and service plan ID. These credentials will be used by Journey Optimizer to authenticate and send messages through Sinch's platform.

1. **Create a [channel configuration](sms-configuration-surface.md) for your RCS messages**

    Configure a channel surface in Journey Optimizer by linking your Sinch credentials and defining the messaging parameters. This setup enables you to compose and send RCS messages from Journey Optimizer.

1. **Create and personalize your [SMS message](../sms/create-sms.md)**

    Your messages automatically falls back to SMS when the profile's device does not support RCS or is temporarily unreachable via RCS.
-->

### RCS 멀티미디어 메시지

>[!AVAILABILITY]
>
> 고급 RCS 메시지는 Sinch가 관리하는 직접 계정에서만 사용할 수 있습니다.

1. **브랜드 RCS 에이전트 설정**

   Sinch 대시보드에서 브랜드 RCS 에이전트를 만듭니다. [브랜드 RCS 에이전트에 대해 자세히 알아보기](https://community.sinch.com/t5/RCS/Getting-Started-with-RCS-using-Conversation-API/ta-p/17844)

1. **사용자 지정 API 자격 증명 설정[&#128279;](sms-configuration-custom.md)**

   RCS 에이전트가 승인되면 AppId, 이름, URL 및 인증 유형을 포함하는 사용자 정의 API 자격 증명을 설정해야 합니다.

1. **공급자 페이로드로 RCS를 구성합니다.**

   [사용자 지정 API 자격 증명](sms-configuration-custom.md)에서 공급자 페이로드를 추가하여 RCS 메시지의 유효성을 검사하고 사용자 지정합니다.

1. **RCS 메시지에 대한 [채널 구성](sms-configuration-surface.md)을 만듭니다**

   Sinch 자격 증명을 연결하고 메시징 매개 변수를 정의하여 Journey Optimizer에서 채널 표면을 구성합니다. 이 설정을 통해 Journey Optimizer에서 RCS 메시지를 구성하고 전송할 수 있습니다.

1. **SMS 메시지 만들기 및 개인화[2&rbrace;](../sms/create-sms.md)**

   페이로드를 SMS 콘텐츠에 직접 붙여넣어 RCS(Rich Communication Services) 메시지를 임베드하고 전달합니다.

   ➡️ [Sinch 설명서에서 Sinch가 RCS를 지원하는 방법을 살펴봅니다](https://sinch.com/blog/rcs-api-guide/)


