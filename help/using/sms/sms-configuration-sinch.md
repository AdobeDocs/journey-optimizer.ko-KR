---
solution: Journey Optimizer
product: journey optimizer
title: Sinch 공급자 구성
description: Sinch를 사용하여 Journey Optimizer에서 텍스트 메시지를 보내도록 환경을 구성하는 방법에 대해 알아봅니다
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 85412a85-edf0-4069-8bc7-b80371375f1f
source-git-commit: 342b9210f79266cb11628dcdc411f90844a84e37
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 4%

---

# Sinch 공급자 구성 {#sms-configuration-sinch}

Journey Optimizer에서 Sinch 공급자를 사용하는 경우 두 가지 고유한 옵션을 찾을 수 있습니다.

* **SMS 구성**: SMS 메시지를 원활하게 보낼 수 있도록 Sinch API 자격 증명을 설정합니다.

* **MMS 구성**: MMS(멀티미디어 메시지)의 경우 Sinch MMS API 자격 증명을 구성합니다. 인바운드 메시지 추적 및 응답은 SMS 구성에서 처리합니다. MMS 설정은 MMS 메시지의 아웃바운드 게재에만 해당됩니다.

## Sinch API 자격 증명{#create-api}

Journey Optimizer에서 SMS 메시지 및 MMS를 전송하도록 Sinch 공급자를 구성하려면 다음 단계를 수행합니다.

1. 왼쪽 레일에서 다음을 찾습니다. **[!UICONTROL 관리]** > **[!UICONTROL 채널]** 및 선택 **[!UICONTROL API 자격 증명]** 메뉴 아래의 제품에서 사용할 수 있습니다. 다음을 클릭합니다. **[!UICONTROL 새 API 자격 증명 만들기]** 단추를 클릭합니다.

1. 아래에 자세히 설명된 대로 SMS API 자격 증명을 구성합니다.

   * **[!UICONTROL SMS 공급업체]**: Sinch

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

API 자격 증명을 만들고 구성한 후에는 SMS 메시지에 대한 채널 표면을 만들어야 합니다. [자세히 알아보기](sms-configuration-surface.md)

## Sinch MMS API 자격 증명 {#sinch-mms}

>[!IMPORTANT]
>
> MMS 설정과 함께 인바운드 메시지 추적 및 동의 요청 관리를 위한 Sinch API 자격 증명을 특별히 만들어야 합니다.

Journey Optimizer을 사용하여 MMS를 전송하도록 Sinch MMS를 구성하려면 다음 단계를 수행합니다.

1. 왼쪽 레일에서 다음을 찾습니다. **[!UICONTROL 관리]** > **[!UICONTROL 채널]** 및 선택 **[!UICONTROL API 자격 증명]** 메뉴 아래의 제품에서 사용할 수 있습니다. 다음을 클릭합니다. **[!UICONTROL 새 API 자격 증명 만들기]** 단추를 클릭합니다.

1. 아래에 자세히 설명된 대로 MMS API 자격 증명을 구성합니다.

   * **[!UICONTROL SMS 공급업체]**: Sinch MMS

   * **[!UICONTROL 이름]**: API 자격 증명의 이름을 선택합니다.

   * **[!UICONTROL 프로젝트 ID]**, **[!UICONTROL 앱 ID]** 및 **[!UICONTROL API 토큰]**: 아래 단계에 따라 MMS API 자격 증명을 수집합니다.

      * 대상 **[!UICONTROL 프로젝트 ID]** 및 **[!UICONTROL 앱 ID]**: 액세스 [대화 API 개요](https://dashboard.sinch.com/convapi/overview) Sinch 대시보드의 Sinch 프로젝트 페이지입니다.
      * 대상 **[!UICONTROL API 토큰]**: 가져오기 [액세스 키](https://community.sinch.com/t5/Customer-Dashboard/Sinch-Access-Keys/ta-p/12638) Sinch 프로젝트용 및 **Base64 API 토큰** 사용 중인 Sinch 프로젝트에서 **액세스 키**.

   * **[!UICONTROL 서비스 계획 ID]** 및 **[!UICONTROL SMS API 토큰]**: 사용자 **[!UICONTROL 서비스 계획 ID]** 및 **[!UICONTROL SMS API 토큰]** 는 API 페이지의 SMS 탭에 있습니다.

1. 클릭 **[!UICONTROL 제출]** api 자격 증명 구성을 완료한 경우입니다.

API 자격 증명을 만들고 구성한 후에는 MMS 메시지에 대한 채널 표면을 만들어야 합니다. [자세히 알아보기](sms-configuration-surface.md)
