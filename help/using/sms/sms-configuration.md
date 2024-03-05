---
solution: Journey Optimizer
product: journey optimizer
title: SMS 채널 구성
description: Journey Optimizer에서 텍스트 메시지를 전송하도록 환경을 구성하는 방법 알아보기
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: 75638e9b463278efab16b2b85ed2707640f088f2
workflow-type: tm+mt
source-wordcount: '1676'
ht-degree: 11%

---

# SMS 채널 구성 {#sms-configuration}

SMS 또는 MMS를 보내기 전에 Adobe Journey Optimizer 환경을 구성해야 합니다. 다음을 수행합니다.

* [공급자 설정 통합](#create-api) Journey Optimizer 사용
* [SMS 표면 만들기](#message-preset-sms) (즉, SMS 사전 설정), MMS에도 사용

이 단계는 Adobe Journey Optimizer에서 수행해야 합니다 [시스템 관리자](../start/path/administrator.md).

## 전제 조건{#sms-prerequisites}

Adobe Journey Optimizer은 현재 Adobe Journey Optimizer과 독립적으로 텍스트 메시지 서비스를 제공하는 서드파티 공급자와 통합됩니다. 텍스트 메시징에 지원되는 공급자는 다음과 같습니다. **Sinch**, **트빌리오** 및 **정보 피드**. MMS는 **Sinch**.

SMS 채널 구성 전에 이러한 공급자 중 하나로 계정을 만들어야 **API 토큰** 및 **서비스 ID**: Adobe Journey Optimizer과 해당 공급자 간의 연결을 구성해야 합니다.

문자 메시지 서비스 사용은 해당 공급자의 추가 약관이 적용됩니다. 타사 솔루션인 Sinch, Twilio 및 Infobip은 통합을 통해 Adobe Journey Optimizer 사용자에게 제공됩니다. Adobe은 서드파티 제품을 제어하지 않으며 책임지지 않습니다. 문자 메시지 서비스(SMS/MMS)와 관련된 문제 또는 지원 요청은 공급자에게 문의하십시오.

>[!CAUTION]
>
>SMS 하위 도메인에 액세스하고 편집하려면 **[!UICONTROL SMS 하위 도메인 관리]** 프로덕션 샌드박스에 대한 권한. 의 권한에 대해 자세히 알아보기 [이 페이지](../administration/high-low-permissions.md#administration-permissions).
>

## 새 API 자격 증명 만들기 {#create-api}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_header"
>title="Journey Optimizer로 SMS 공급자 구성"
>abstract="Adobe Journey Optimizer는 SMS 서비스 공급자를 통해 문자 메시지를 보냅니다. 공급자를 선택하고 API 자격 증명을 입력하십시오."

>[!CONTEXTUALHELP]
>id="ajo_admin_mms_api_header"
>title="Journey Optimizer로 MMS 공급자 구성"
>abstract="Adobe Journey Optimizer는 MMS 서비스 공급자를 통해 미디어 콘텐츠를 보냅니다. 공급자를 선택하고 API 자격 증명을 입력하십시오."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api"
>title="Journey Optimizer로 SMS/MMS 공급자 구성"
>abstract="문자 메시지(SMS/MMS)를 보내기 전에 공급자 설정을 Journey Optimizer와 통합해야 합니다. 완료되면 SMS/MMS 표면을 만들어야 합니다. 이 단계는 Adobe Journey Optimizer 시스템 관리자가 수행해야 합니다."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/sms/sms-configuration.html#message-preset-sms" text="SMS 채널 표면 만들기"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_configuration"
>title="SMS 공급업체 구성 선택"
>abstract="SMS 공급업체에 맞게 구성된 API 자격 증명을 선택합니다."

### Sinch {#sinch-api}

Journey Optimizer을 사용하여 SMS/MMS 공급자를 구성하려면 다음 단계를 수행합니다.

1. 왼쪽 레일에서 다음을 찾습니다. **[!UICONTROL 관리]** > **[!UICONTROL 채널]** 및 선택 **[!UICONTROL API 자격 증명]** 메뉴 아래의 제품에서 사용할 수 있습니다. 다음을 클릭합니다. **[!UICONTROL 새 API 자격 증명 만들기]** 단추를 클릭합니다.

   ![](assets/sms_6.png)

1. 아래에 자세히 설명된 대로 SMS API 자격 증명을 구성합니다.

   * **[!UICONTROL 이름]**: API 자격 증명의 이름을 선택합니다.

   * **[!UICONTROL 서비스 ID]** 및 **[!UICONTROL API 토큰]**: API 페이지에 액세스하면 SMS 탭 아래에서 자격 증명을 찾을 수 있습니다. 다음에서 자세히 알아보기 [Sinch 설명서](https://developers.sinch.com/docs/sms/getting-started/){target="_blank"}.

   * **[!UICONTROL 옵트인 키워드]**: 를 자동으로 트리거할 기본 또는 사용자 지정 키워드를 입력합니다. **[!UICONTROL 옵트인 메시지]**. 여러 키워드의 경우 쉼표로 구분된 값을 사용하십시오.

   * **[!UICONTROL 옵트인 메시지]**: (으)로 자동으로 전송되는 사용자 지정 응답을 입력합니다. **[!UICONTROL 옵트인 메시지]**.

   * **[!UICONTROL 옵트아웃 키워드]**: 를 자동으로 트리거할 기본 또는 사용자 지정 키워드를 입력합니다. **[!UICONTROL 옵트아웃 메시지]**. 여러 키워드의 경우 쉼표로 구분된 값을 사용하십시오.

   * **[!UICONTROL 옵트아웃 메시지]**: (으)로 자동으로 전송되는 사용자 지정 응답을 입력합니다. **[!UICONTROL 옵트아웃 메시지]**.

   * **[!UICONTROL 도움말 키워드]**: 를 자동으로 트리거할 기본 또는 사용자 지정 키워드를 입력합니다. **도움말 메시지**. 여러 키워드의 경우 쉼표로 구분된 값을 사용하십시오.

   * **[!UICONTROL 도움말 메시지]**: (으)로 자동으로 전송되는 사용자 지정 응답을 입력합니다. **도움말 메시지**.

   * **[!UICONTROL 이중 옵트인 키워드]**: 이중 옵트인 프로세스를 트리거하는 키워드를 입력합니다. 사용자 프로필이 존재하지 않으면 확인 후 생성됩니다. 여러 키워드의 경우 쉼표로 구분된 값을 사용하십시오. [SMS 이중 옵트인에 대해 자세히 알아보기](https://video.tv.adobe.com/v/3427129/?learn=on).

   * **[!UICONTROL 이중 옵트인 메시지]**: 이중 옵트인 확인에 응답하여 자동으로 전송되는 사용자 지정 응답을 입력합니다.

1. 클릭 **[!UICONTROL 제출]** api 자격 증명 구성을 완료한 경우입니다.

API 자격 증명을 만들고 구성한 후에는 SMS 메시지에 대한 채널 표면(즉, 메시지 사전 설정)을 만들어야 합니다.

### Sinch MMS {#sinch-mms}

Journey Optimizer으로 Sinch MMS를 구성하려면 다음 단계를 수행합니다.

1. 왼쪽 레일에서 다음을 찾습니다. **[!UICONTROL 관리]** > **[!UICONTROL 채널]** 및 선택 **[!UICONTROL API 자격 증명]** 메뉴 아래의 제품에서 사용할 수 있습니다. 다음을 클릭합니다. **[!UICONTROL 새 API 자격 증명 만들기]** 단추를 클릭합니다.

   ![](assets/sms_6.png)

1. 아래에 자세히 설명된 대로 SMS API 자격 증명을 구성합니다.

   * **[!UICONTROL 이름]**: API 자격 증명의 이름을 선택합니다.

   * **[!UICONTROL 프로젝트 ID]**, **[!UICONTROL 앱 ID]** 및 **[!UICONTROL API 토큰]**: 대화 API 메뉴의 앱 메뉴에서 자격 증명을 찾을 수 있습니다. 다음에서 자세히 알아보기 [Sinch 설명서](https://docs.cc.sinch.com/cloud/service-configuration/en/oxy_ex-1/common/wln1620131604643.html){target="_blank"}.

   * **[!UICONTROL 서비스 계획 ID]** 및 **[!UICONTROL SMS API 토큰]**: 사용자 **[!UICONTROL 서비스 계획 ID]** 및 **[!UICONTROL SMS API 토큰]** 는 API 페이지의 SMS 탭에 있습니다.

1. 클릭 **[!UICONTROL 제출]** api 자격 증명 구성을 완료한 경우입니다.

API 자격 증명을 만들고 구성한 후에는 MMS 메시지에 대한 채널 표면(즉, 메시지 사전 설정)을 만들어야 합니다.

### 트빌리오 {#twilio-api}

Journey Optimizer으로 Twilio를 구성하려면 다음 단계를 수행합니다.

1. 왼쪽 레일에서 다음을 찾습니다. **[!UICONTROL 관리]** > **[!UICONTROL 채널]** 및 선택 **[!UICONTROL API 자격 증명]** 메뉴 아래의 제품에서 사용할 수 있습니다. 다음을 클릭합니다. **[!UICONTROL 새 API 자격 증명 만들기]** 단추를 클릭합니다.

   ![](assets/sms_6.png)

1. 아래에 자세히 설명된 대로 SMS API 자격 증명을 구성합니다.

   * **[!UICONTROL 이름]**: API 자격 증명의 이름을 선택합니다.

   * **[!UICONTROL 계정 SID]** 및 **[!UICONTROL 인증 토큰]**: 액세스 **계정 정보** 자격 증명을 찾을 수 있는 Twilio 콘솔 대시보드 페이지의 창입니다.

   * **[!UICONTROL 메시지 SID]**: Twilio의 API에서 만든 모든 메시지에 할당된 고유 식별자를 입력합니다. 다음에서 자세히 알아보기 [Twilio 설명서](https://support.twilio.com/hc/en-us/articles/223134387-What-is-a-Message-SID-){target="_blank"}.

1. 클릭 **[!UICONTROL 제출]** api 자격 증명 구성을 완료한 경우입니다.

API 자격 증명을 만들고 구성한 후에는 SMS 메시지에 대한 채널 표면(즉, 메시지 사전 설정)을 만들어야 합니다.

### 정보 피드 {#infobip-api}

Journey Optimizer을 사용하여 Infobip을 구성하려면 다음 단계를 수행합니다.

1. 왼쪽 레일에서 다음을 찾습니다. **[!UICONTROL 관리]** > **[!UICONTROL 채널]** 및 선택 **[!UICONTROL API 자격 증명]** 메뉴 아래의 제품에서 사용할 수 있습니다. 다음을 클릭합니다. **[!UICONTROL 새 API 자격 증명 만들기]** 단추를 클릭합니다.

   ![](assets/sms_6.png)

1. 아래에 자세히 설명된 대로 SMS API 자격 증명을 구성합니다.

   * **[!UICONTROL 이름]**: API 자격 증명의 이름을 선택합니다.

   * **[!UICONTROL API 기본 URL]** 및 **[!UICONTROL API 키]**: 웹 인터페이스 홈 페이지 또는 API 키 관리 페이지에 액세스하여 자격 증명을 찾을 수 있습니다. 다음에서 자세히 알아보기 [Infobip 설명서](https://www.infobip.com/docs/api){target="_blank"}.

   * **[!UICONTROL 옵트인 키워드]**: 를 자동으로 트리거할 기본 또는 사용자 지정 키워드를 입력합니다. **[!UICONTROL 옵트인 메시지]**. 여러 키워드의 경우 쉼표로 구분된 값을 사용하십시오.

   * **[!UICONTROL 옵트인 메시지]**: (으)로 자동으로 전송되는 사용자 지정 응답을 입력합니다. **[!UICONTROL 옵트인 메시지]**.

   * **[!UICONTROL 옵트아웃 키워드]**: 를 자동으로 트리거할 기본 또는 키워드를 입력합니다. **[!UICONTROL 옵트아웃 메시지]**. 여러 키워드의 경우 쉼표로 구분된 값을 사용하십시오.

   * **[!UICONTROL 옵트아웃 메시지]**: (으)로 자동으로 전송되는 사용자 지정 응답을 입력합니다. **[!UICONTROL 옵트아웃 메시지]**.

   * **[!UICONTROL 도움말 키워드]**: 를 자동으로 트리거할 기본 또는 사용자 지정 키워드를 입력합니다. **도움말 메시지**. 여러 키워드의 경우 쉼표로 구분된 값을 사용하십시오.

   * **[!UICONTROL 도움말 메시지]**: (으)로 자동으로 전송되는 사용자 지정 응답을 입력합니다. **도움말 메시지**.

   * **[!UICONTROL 이중 옵트인 키워드]**: 이중 옵트인 프로세스를 트리거하는 키워드를 입력합니다. 사용자 프로필이 존재하지 않으면 확인 후 생성됩니다. 여러 키워드의 경우 쉼표로 구분된 값을 사용하십시오.

   * **[!UICONTROL 이중 옵트인 메시지]**: 이중 옵트인 확인에 응답하여 자동으로 전송되는 사용자 지정 응답을 입력합니다.

   * **[!UICONTROL 주체 엔티티 ID]**: 할당된 DLT 주체 엔티티 ID를 입력합니다.

   * **[!UICONTROL 컨텐츠 템플릿 ID]**: 등록된 DLT 콘텐츠 템플릿 ID를 입력합니다.

   * **[!UICONTROL 유효 기간]**: 메시지 유효 기간을 시간 단위로 입력합니다. 이 기간 내에 메시지를 게재할 수 없는 경우 시스템에서 다시 전송을 시도합니다. 기본 유효 기간은 48시간으로 설정됩니다.

   * **[!UICONTROL 콜백 데이터]**: 알림 URL에 전송할 추가 클라이언트 데이터를 입력합니다.

1. 클릭 **[!UICONTROL 제출]** api 자격 증명 구성을 완료한 경우입니다.

API 자격 증명을 만들고 구성한 후에는 SMS 메시지에 대한 채널 표면(즉, 메시지 사전 설정)을 만들어야 합니다.

## SMS 표면 만들기 {#message-preset-sms}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_sms_type"
>title="메시지 범주 정의"
>abstract="이 표면을 사용하여 문자 메시지 유형 선택: 사용자 동의가 필요한 프로모션 메시지를 위한 마케팅 또는 암호 재설정과 같은 비상업적 메시지를 위한 트랜잭션."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html#sms-opt-out-management" text="마케팅 문자 메시지 옵트아웃"

SMS/MMS 채널이 구성되면 SMS 메시지를 보낼 수 있는 채널 표면을 만들어야 합니다. **[!DNL Journey Optimizer]**.

채널 표면을 만들려면 다음 단계를 수행합니다.

1. 왼쪽 레일에서 다음을 찾습니다. **[!UICONTROL 관리]** > **[!UICONTROL 채널]** 및 선택 **[!UICONTROL 브랜딩]** > **[!UICONTROL 채널 표면]**. 다음을 클릭합니다. **[!UICONTROL 채널 표면 만들기]** 단추를 클릭합니다.

   ![](assets/preset-create.png)

1. 표면에 대한 이름과 설명(선택 사항)을 입력한 다음 SMS 채널을 선택합니다.

   ![](assets/sms-create-surface.png)

   >[!NOTE]
   >
   > 이름은 문자(A-Z)로 시작해야 합니다. 영숫자만 포함할 수 있습니다. 밑줄을 사용할 수도 있습니다 `_`, 점`.` 및 하이픈 `-` 자.

1. 다음을 정의합니다. **SMS 설정**.

   ![](assets/sms-surface-settings.png)

   다음을 선택하여 시작 **[!UICONTROL SMS 유형]** 이 데이터는 표면과 함께 전송됩니다. **[!UICONTROL 트랜잭션]** 또는 **[!UICONTROL 마케팅]**.

   * 선택 **마케팅** 프로모션 텍스트 메시지: 이러한 메시지에는 사용자의 동의가 필요합니다.
   * 선택 **트랜잭션** 예를 들어 주문 확인, 암호 재설정 알림 또는 게재 정보와 같은 비상업적인 메시지의 경우.

   SMS/MMS를 만들 때 메시지에 대해 선택한 범주와 일치하는 유효한 채널 표면을 선택해야 합니다.

   >[!CAUTION]
   >
   >**트랜잭션** 마케팅 커뮤니케이션의 구독을 취소한 프로필에 메시지를 보낼 수 있습니다. 이러한 메시지는 특정 컨텍스트에서만 보낼 수 있습니다.

1. 다음 항목 선택 **[!UICONTROL SMS 구성]** 서피스와 연관시킬 수 있습니다.

   SMS 메시지를 보내도록 환경을 구성하는 방법에 대한 자세한 내용은 [이 섹션](#create-api).

1. 다음을 입력합니다. **[!UICONTROL 발신자 번호]** 통신&#x200B;에 을 사용하려고 합니다.

1. 다음 항목 선택 **[!UICONTROL SMS 실행 필드]** 을(를) 선택하려면 **[!UICONTROL 프로필 속성]** 프로필의 전화 번호와 연결됩니다.

1. SMS 메시지에서 URL 단축 기능을 사용하려면 **[!UICONTROL 하위 도메인]** 목록을 표시합니다.

   >[!NOTE]
   >
   >하위 도메인을 선택하려면 최소 하나 이상의 SMS/MMS 하위 도메인을 이전에 구성했는지 확인하십시오. [방법 알아보기](sms-subdomains.md)

1. 다음을 입력합니다. **[!UICONTROL 옵트아웃 번호]** 이 서피스에 를 사용합니다. 프로필이 이 번호에서 옵트아웃해도 문자 메시지를 보낼 때 사용할 수 있는 다른 번호에서 메시지를 보낼 수 있습니다. [!DNL Journey Optimizer].

   >[!NOTE]
   >
   >위치 [!DNL Journey Optimizer], 텍스트 메시지에 대한 옵트아웃은 더 이상 채널 수준에서 관리되지 않습니다. 이제 숫자에 따라 다릅니다.

1. 모든 매개 변수가 구성되면 **[!UICONTROL 제출]** 확인할 수 있습니다. 채널 서피스를 구배로 저장하고 나중에 구성을 재개할 수도 있습니다.

   ![](assets/sms-submit-surface.png)

1. 채널 표면이 만들어지면 목록에 다음과 같이 표시됩니다. **[!UICONTROL 처리 중]** 상태.

   >[!NOTE]
   >
   >검사가 실패한 경우 다음에서 가능한 실패 이유에 대해 자세히 알아보십시오. [이 섹션](#monitor-channel-surfaces).

1. 검사가 성공하면 채널 표면이 **[!UICONTROL 활성]** 상태. 메시지를 전달하는 데 사용할 준비가 되었습니다.

   ![](assets/preset-active.png)

이제 Journey Optimizer에서 문자 메시지를 보낼 준비가 되었습니다.

**관련 항목**

* [문자 메시지(SMS/MMS) 만들기](create-sms.md)
* [여정에 메시지 추가](../building-journeys/journeys-message.md)
* [캠페인에 메시지 추가](../campaigns/create-campaign.md)

