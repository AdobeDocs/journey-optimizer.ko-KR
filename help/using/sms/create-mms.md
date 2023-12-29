---
solution: Journey Optimizer
product: journey optimizer
title: MMS 만들기
description: Journey Optimizer에서 MMS를 만드는 방법 알아보기
feature: SMS
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 38defa47-9b33-43a3-9b3e-d3aa4cb2857f
source-git-commit: feae2cb9d0bed35f12eb117cf2969c9290ebc06f
workflow-type: tm+mt
source-wordcount: '1084'
ht-degree: 7%

---

# MMS 메시지 만들기  {#create-mms}

## 전제 조건{#sms-prerequisites}

SMS 메시지를 만들기 전에 먼저 Journey Optimizer을 사용하여 SMS 공급업체를 구성해야 합니다. 다음 단계를 따르십시오.

* SMS를 보내기 전에 공급자 설정을 Journey Optimizer과 통합해야 합니다.

+++ 새로운 Sinch MMS API 자격 증명을 만드는 방법을 알아봅니다.

   1. 왼쪽 레일에서 다음을 찾습니다. **[!UICONTROL 관리]** > **[!UICONTROL 채널]** 및 선택 **[!UICONTROL API 자격 증명]** 메뉴 아래의 제품에서 사용할 수 있습니다. 다음을 클릭합니다. **[!UICONTROL 새 API 자격 증명 만들기]** 단추를 클릭합니다.

      ![](assets/sms_6.png)

   1. SMS API 자격 증명을 구성합니다.

   * 대상 **[!DNL Sinch MMS]**:

      * **[!UICONTROL 이름]**: API 자격 증명의 이름을 선택합니다.

      * **[!UICONTROL 프로젝트 ID]**, **[!UICONTROL 앱 ID]** 및 **[!UICONTROL API 토큰]**: 대화 API 메뉴의 앱 메뉴에서 자격 증명을 찾을 수 있습니다.  [자세히 알아보기](https://docs.cc.sinch.com/cloud/service-configuration/en/oxy_ex-1/common/wln1620131604643.html)

     ![](assets/mms_provider.png)

   1. 클릭 **[!UICONTROL 제출]** api 자격 증명 구성을 완료한 경우입니다.

  API 자격 증명을 만들고 구성한 후에는 SMS 메시지에 대한 채널 표면(즉, 메시지 사전 설정)을 만들어야 합니다.

+++

* 완료되면 SMS 표면을 만들어야 합니다. 이 단계는 Adobe Journey Optimizer 시스템 관리자가 수행해야 합니다.

+++ 채널 표면을 만드는 방법을 알아봅니다.

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

      * 선택 **마케팅** 프로모션 SMS의 경우: 이러한 메시지에는 사용자의 동의가 필요합니다.
      * 선택 **트랜잭션** 예를 들어 주문 확인, 암호 재설정 알림 또는 게재 정보와 같은 비상업적인 메시지의 경우.

      SMS 메시지를 만들 때 메시지에 대해 선택한 카테고리와 일치하는 유효한 채널 표면을 선택해야 합니다.

      >[!CAUTION]
      >
      >**트랜잭션** 마케팅 커뮤니케이션의 구독을 취소한 프로필에 SMS 메시지를 보낼 수 있습니다. 이러한 메시지는 특정 컨텍스트에서만 보낼 수 있습니다.

   1. 다음 항목 선택 **[!UICONTROL SMS 구성]** 서피스와 연관시킬 수 있습니다.

      SMS 메시지를 보내도록 환경을 구성하는 방법에 대한 자세한 내용은 [이 섹션](#create-api).

   1. 다음을 입력합니다. **[!UICONTROL 발신자 번호]** 통신&#x200B;에 을 사용하려고 합니다.

   1. 다음 항목 선택 **[!UICONTROL SMS 실행 필드]** 을(를) 선택하려면 **[!UICONTROL 프로필 속성]** 프로필의 전화 번호와 연결됩니다.

   1. SMS 메시지에서 URL 단축 기능을 사용하려면 **[!UICONTROL 하위 도메인]** 목록을 표시합니다.

      >[!NOTE]
      >
      >하위 도메인을 선택하려면 최소 하나 이상의 SMS 하위 도메인을 이전에 구성했는지 확인하십시오. [방법 알아보기](sms-subdomains.md)

   1. 다음을 입력합니다. **[!UICONTROL 옵트아웃 번호]** 이 서피스에 를 사용합니다. 프로필이 이 번호에서 옵트아웃해도 를 사용하여 SMS 메시지를 보낼 수 있는 다른 번호에서 메시지를 보낼 수 있습니다. [!DNL Journey Optimizer].

      >[!NOTE]
      >
      >위치 [!DNL Journey Optimizer], SMS 옵트아웃은 더 이상 채널 수준에서 관리되지 않습니다. 이제 숫자에 따라 다릅니다.

   1. 모든 매개 변수가 구성되면 **[!UICONTROL 제출]** 확인할 수 있습니다. 채널 서피스를 구배로 저장하고 나중에 구성을 재개할 수도 있습니다.

      ![](assets/sms-submit-surface.png)

   1. 채널 표면이 만들어지면 목록에 다음과 같이 표시됩니다. **[!UICONTROL 처리 중]** 상태.

      >[!NOTE]
      >
      >검사가 실패한 경우 다음에서 가능한 실패 이유에 대해 자세히 알아보십시오. [이 섹션](#monitor-channel-surfaces).

   1. 검사가 성공하면 채널 표면이 **[!UICONTROL 활성]** 상태. 메시지를 전달하는 데 사용할 준비가 되었습니다.

      ![](assets/preset-active.png)


## SMS 메시지 만들기 {#create-sms-journey-campaign}

아래 탭을 탐색하여 캠페인 또는 여정에 SMS 메시지를 추가하는 방법을 알아보십시오.

>[!BEGINTABS]

>[!TAB 여정에 SMS 메시지 추가]

1. 여정을 연 다음 **작업** 팔레트의 섹션입니다.

   ![](assets/sms_create_1.png)

1. 메시지에 대한 기본 정보(레이블, 설명, 카테고리)를 입력한 다음 사용할 메시지 표면을 선택합니다.

   ![](assets/sms_create_2.png)

   여정 구성 방법에 대한 자세한 내용은 [이 페이지](../building-journeys/journey-gs.md)

   다음 **[!UICONTROL 표면]** 필드는 기본적으로 미리 채워져 있으며 사용자가 해당 채널에 대해 마지막으로 사용한 서페이스가 있습니다.

이제에서 SMS 메시지의 콘텐츠 디자인을 시작할 수 있습니다. **[!UICONTROL 콘텐츠 편집]** 단추를 클릭합니다. [SMS 콘텐츠 정의](#sms-content)

>[!TAB Campaign에 SMS 메시지 추가]

1. 새 예약된 캠페인 또는 API에서 트리거된 캠페인을 만들고, 다음을 선택합니다. **[!UICONTROL SMS]** 을(를) 작업으로 선택하고 **[!UICONTROL 앱 표면]** 사용할 수 있습니다. [SMS 구성에 대해 자세히 알아보기](sms-configuration.md).

   ![](assets/sms_create_3.png)

1. **[!UICONTROL 만들기]**&#x200B;를 클릭합니다.

1. 다음에서 **[!UICONTROL 속성]** 섹션, 캠페인의 편집 **[!UICONTROL 제목]** 및 **[!UICONTROL 설명]**.

   ![](assets/sms_create_4.png)

1. 다음을 클릭합니다. **[!UICONTROL 대상자 선택]** 사용 가능한 Adobe Experience Platform 대상 목록에서 타깃팅할 대상을 정의하는 단추입니다. [자세히 알아보기](../audience/about-audiences.md).

1. 다음에서 **[!UICONTROL ID 네임스페이스]** 필드에서 선택한 대상에서 개인을 식별하기 위해 사용할 네임스페이스를 선택합니다. [자세히 알아보기](../event/about-creating.md#select-the-namespace).

   ![](assets/sms_create_5.png)

1. 클릭 **[!UICONTROL 실험 만들기]** 콘텐츠 실험 구성을 시작하고 처리를 만들어 성능을 측정하고 타겟 대상자에 대한 최상의 옵션을 식별합니다. [자세히 알아보기](../campaigns/content-experiment.md)

1. 다음에서 **[!UICONTROL 작업 추적]** 섹션에서 SMS 메시지의 링크 클릭을 추적할지 여부를 지정합니다.

1. 캠페인은 특정 날짜 또는 되풀이되는 빈도로 실행되도록 디자인됩니다. 구성 방법 알아보기 **[!UICONTROL 예약]** 의 내 캠페인 [이 섹션](../campaigns/create-campaign.md#schedule).

1. 다음에서 **[!UICONTROL 작업 트리거]** 메뉴에서 다음을 선택합니다. **[!UICONTROL 빈도]** SMS 메시지:

   * 한 번
   * 일별
   * 주별
   * 월

이제에서 SMS 메시지의 콘텐츠 디자인을 시작할 수 있습니다. **[!UICONTROL 콘텐츠 편집]** 단추를 클릭합니다. [SMS 콘텐츠 디자인](#sms-content)

>[!ENDTABS]

## MMS 콘텐츠 정의{#mms-content}

1. 여정 또는 캠페인 구성 화면에서 **[!UICONTROL 콘텐츠 편집]** SMS 콘텐츠를 구성하는 단추입니다.

1. 다음을 클릭합니다. **[!UICONTROL 메시지]** 표현식 편집기를 여는 필드입니다.

   ![](assets/sms-content.png)

1. 표현식 편집기를 사용하여 콘텐츠를 정의하고 다이내믹 콘텐츠를 추가합니다. 프로필 이름 또는 구/군/시 등의 모든 속성을 사용할 수 있습니다. 자세히 알아보기 [개인화](../personalization/personalize.md) 및 [다이내믹 콘텐츠](../personalization/get-started-dynamic-content.md) 를 입력합니다.

1. SMS 콘텐츠에 미디어를 추가하려면 MMS 옵션을 활성화합니다.

   >[!NOTE]
   >
   > MMS 옵션은 Sinch에서만 사용할 수 있습니다. MMS를 만들려면 특정 API 자격 증명을 만들어야 합니다. [자세히 알아보기](sms-configuration.md#create-new-api)

   ![](assets/sms_create_6.png)

1. 추가 **[!UICONTROL 제목]** 미디어.

1. 에 미디어 URL을 입력합니다 **[!UICONTROL 미디어]** 필드.

   ![](assets/sms_create_7.png)

1. 클릭 **[!UICONTROL 저장]** 미리 보기에서 메시지를 확인합니다. 다음을 사용할 수 있습니다. **[!UICONTROL 콘텐츠 시뮬레이션]** 축약된 URL 또는 개인화된 콘텐츠를 미리 볼 수 있습니다.

이제 SMS 메시지를 테스트하고 대상자에게 보낼 수 있습니다. [자세히 알아보기](send-sms.md)
전송되면 캠페인 또는 여정 보고서 내에서 SMS의 영향을 측정할 수 있습니다. 보고와 관련한 자세한 정보는 [이 섹션](../reports/campaign-global-report.md#sms-tab)을 참조하십시오.

>[!NOTE]
>
>업계 표준 및 규정에 따라 모든 SMS 마케팅 메시지에는 수신자가 간편하게 구독을 취소할 수 있는 방법이 포함되어야 합니다. 이를 위해 SMS 수신자는 옵트인 및 옵트아웃 키워드로 회신할 수 있습니다. [옵트아웃 관리 방법 알아보기](../privacy/opt-out.md#sms-opt-out-management-sms-opt-out-management)

**관련 항목**

* [SMS 메시지 미리 보기, 테스트 및 보내기](send-sms.md)
* [SMS 채널 구성](sms-configuration.md)
* [SMS 보고서](../reports/journey-global-report.md#sms-global)
