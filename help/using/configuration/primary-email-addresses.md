---
solution: Journey Optimizer
product: journey optimizer
title: 실행 주소 변경
description: 프로필 서비스에서 사용할 이메일 주소를 결정하는 방법을 알아봅니다.
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: 기본, 실행, 이메일, 타겟, 프로필, 최적화 도구
exl-id: fe2f6516-7790-4501-a3a1-3d7cb94d7874
source-git-commit: f69e482daf457f1c331d158d1bf04b4cfb392197
workflow-type: tm+mt
source-wordcount: '641'
ht-degree: 20%

---

# 실행 주소 변경 {#change-primary-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address"
>title="사용할 주소 정의"
>abstract="데이터베이스에서 여러 이메일 주소 또는 전화번호를 사용하는 경우(개인용, 업무용 등) 전송의 우선순위를 지정할 수 있는 항목을 선택할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address_header"
>title="사용할 주소 정의"
>abstract="프로필의 이메일 주소 또는 전화번호 확인에 사용되는 필드를 편집하여 전송의 우선순위를 지정합니다."

프로필을 타겟팅할 때 데이터베이스에서 여러 이메일 주소 또는 전화 번호(전문 이메일 주소, 개인 전화 번호 등)를 사용할 수 있습니다.

이 경우 [!DNL Journey Optimizer]은(는) **[!UICONTROL 실행 필드]**&#x200B;를 사용하여 우선 순위의 프로필 서비스에서 사용할 전자 메일 주소 또는 전화 번호를 결정합니다.

현재 기본적으로 사용되는 필드를 확인하려면 **[!UICONTROL 관리]** > **[!UICONTROL 채널]** > **[!UICONTROL 일반 설정]** > **[!UICONTROL 실행 필드]** 메뉴에 액세스합니다.

![](assets/primary-address-execution-fields.png){width=90%}

>[!NOTE]
>
>실행 필드는 이메일, SMS 및 WhatsApp 채널에 사용할 수 있습니다.

현재 값은 샌드박스 수준의 모든 게재에 사용됩니다. 필요한 경우 이러한 필드를 업데이트할 수 있습니다.

대부분의 경우 실행 필드를 전체적으로 변경하고 모든 이메일, SMS 또는 WhatsApp 메시지에 사용해야 하는 값을 정의합니다.

## 관리 설정 업데이트 {#admin-settings}

샌드박스 수준에서 실행 필드를 전체적으로 변경하려면 아래 단계를 따르십시오.

1. **[!UICONTROL 채널]** > **[!UICONTROL 일반 설정]** > **[!UICONTROL 실행 필드]** 메뉴에 액세스합니다.

1. 기본값을 변경하려면 **[!UICONTROL 편집]**&#x200B;을 클릭하세요.

   ![](assets/primary-address-edit.png){width=70%}

1. 선택한 현재 필드 또는 편집 아이콘을 클릭하여 새 필드를 선택합니다.

   ![](assets/primary-address-edit-field.png){width=70%}

1. 사용 가능한 이메일 유형 XDM 필드 목록이 표시됩니다. 사용할 필드를 선택합니다.

   ![](assets/primary-address-select-field.png){width=90%}

1. **[!UICONTROL 저장]**&#x200B;을 클릭하여 선택을 확인합니다.

실행 필드가 업데이트되고, 이제 기본 주소로 사용됩니다.

<!--1. You can also select an additional field to use as secondary email address. This allows you to determine which field to use if the primary field is empty for a profile. -->

## 여정 매개 변수의 기본 실행 필드 재정의 {#override-execution-address-journey}

>[!CONTEXTUALHELP]
>id="ajo_journey_execution_address"
>title="사용자 정의 값 정의"
>abstract="특정 경우에는 기본 실행 주소를 재정의할 수 있습니다. 필드 오른쪽에 있는 **매개변수 재정의 활성화** 아이콘을 사용하여 사용자 정의 기본 주소를 정의합니다."
>additional-url="https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/configuration/primary-email-addresses#journey-parameters" text="실행 주소 정보"

특정 사용 사례의 경우 전역적으로 설정된 실행 필드를 재정의하고 여정 수준에서 다른 값을 정의할 수 있습니다.

이 값을 재정의하는 것은 다음과 같은 경우에 유용합니다.

* 게재를 테스트합니다. 자신의 이메일 주소 또는 전화번호를 추가할 수 있습니다. 여정을 게시하면 이메일, SMS 또는 WhatsApp 메시지가 전송됩니다.
* 목록의 구독자에게 메시지를 보냅니다. [사용 사례](../building-journeys/message-to-subscribers-uc.md)를 자세히 알아보십시오.

**[!UICONTROL 여정]**&#x200B;에 **[!UICONTROL Email]**, **[!UICONTROL SMS]** 또는 [WhatsApp](../email/create-email.md#create-email-journey-campaign) 액션을 추가하면 기본 전자 메일 주소 또는 전화 번호가 여정 고급 매개 변수 아래에 표시됩니다.

필드 오른쪽에 있는 **[!UICONTROL 매개 변수 재정의 사용]** 아이콘을 사용하여 이 값을 재정의합니다.

![](assets/journey-enable-parameter-override.png){width=85%}

>[!CAUTION]
>
>이메일 주소 또는 전화 번호 재정의는 특정 사용 사례에만 사용해야 합니다. 대부분의 경우 샌드박스 수준의 **[!UICONTROL 실행 필드]**&#x200B;에서 기본 주소로 정의된 값을 사용해야 하므로 변경할 필요가 없습니다.

## 채널 구성의 기본 실행 필드 재정의 {#override-execution-address-channel-config}

>[!CONTEXTUALHELP]
>id="ajo_email_config_execution_address"
>title="사용할 기본 실행 주소 재정의"
>abstract="데이터베이스에서 여러 이메일 주소 또는 전화 번호를 사용할 수 있는 경우(개인, 전문가 등), 우선 순위를 지정할 전송 주소를 선택할 수 있습니다. 기본 주소는 샌드박스 수준에서 정의되지만, 여기에서 이 특정 채널 구성에 대한 기본 설정을 재정의할 수 있습니다."

특정 이메일, SMS 또는 WhatsApp [채널 구성](channel-surfaces.md)에 대한 기본 실행 주소를 변경할 수 있습니다.

이렇게 하려면 **[!UICONTROL 실행 차원]** 섹션으로 이동하여 **[!UICONTROL 실행 주소]** 아래의 전용 필드를 편집하십시오.

>[!NOTE]
>
>[WhatsApp 채널](../whatsapp/whatsapp-configuration.md#whatsapp-configuration)의 경우 **[!UICONTROL WhatsApp 실행 필드]**&#x200B;이(가) **[!UICONTROL WhatsApp 설정]** 섹션에 있습니다.

![](assets/sms-config-execution-address.png){width=85%}

그런 다음 사용 가능한 이메일 유형 XDM 필드 목록에서 항목을 선택합니다.

![](assets/sms-config-execution-field.png)

실행 필드가 업데이트되고, 이 채널 구성을 사용하여 캠페인 또는 여정의 기본 주소로 사용됩니다. 샌드박스 수준에서 정의된 [일반 설정](#admin-settings)을 재정의합니다.

<!--[Learn more on the execution address in the email configuration ](../email/email-settings.md#execution-address)-->
