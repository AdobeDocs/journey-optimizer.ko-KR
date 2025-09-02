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
source-git-commit: c39a71da901b888ff440a1488658b577ff72cc32
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 19%

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

![](assets/primary-address-execution-fields.png)

현재 값은 샌드박스 수준의 모든 게재에 사용됩니다. 필요한 경우 이러한 필드를 업데이트할 수 있습니다.

대부분의 경우 실행 필드를 전체적으로 변경하고 모든 이메일 또는 SMS 메시지에 사용해야 하는 값을 정의합니다. <!--[Learn how](#admin-settings)-->

<!--In some specific use cases only, you can override the value set globally and define a different value at the journey level. [Learn more](#journey-parameters)-->

## 관리 설정 업데이트 {#admin-settings}

샌드박스 수준에서 실행 필드를 전체적으로 변경하려면 아래 단계를 따르십시오.

1. **[!UICONTROL 채널]** > **[!UICONTROL 일반 설정]** > **[!UICONTROL 실행 필드]** 메뉴에 액세스합니다.

1. 기본값을 변경하려면 **[!UICONTROL 편집]**&#x200B;을 클릭하세요.

   ![](assets/primary-address.png)

1. 선택한 현재 필드 또는 편집 아이콘을 클릭하여 새 필드를 선택합니다.

   ![](assets/primary-address-edit.png)

1. 사용 가능한 이메일 유형 XDM 필드 목록이 표시됩니다. 사용할 필드를 선택합니다.

   ![](assets/primary-address-select-field.png)

1. **[!UICONTROL 저장]**&#x200B;을 클릭하여 선택을 확인합니다.

실행 필드가 업데이트되고, 이제 기본 주소로 사용됩니다.

<!--1. You can also select an additional field to use as secondary email address. This allows you to determine which field to use if the primary field is empty for a profile. -->

## 기본 실행 필드 재정의 {#override-default-execution-address}

>[!CONTEXTUALHELP]
>id="ajo_journey_execution_address"
>title="사용자 지정 값 정의"
>abstract="경우에 따라 기본 실행 주소를 재정의할 수 있습니다. 필드 오른쪽에 있는 **매개 변수 재정의 사용** 아이콘을 사용하여 사용자 지정 기본 주소를 정의합니다."
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/configuration/primary-email-addresses#journey-parameters" text="실행 주소 정보"

특정 사용 사례의 경우 전역적으로 설정된 실행 필드를 재정의하고 이메일 구성 수준 또는 여정 수준에서 다른 값을 정의할 수 있습니다.

이 값을 재정의하는 것은 다음과 같은 경우에 유용합니다.

* 이메일을 테스트합니다. 자신의 이메일 주소를 추가할 수 있습니다. 여정을 게시하면 이메일이 전송됩니다.
* 목록의 구독자에게 이메일을 보냅니다. [사용 사례](../building-journeys/message-to-subscribers-uc.md)를 자세히 알아보십시오.

### 이메일 구성에서

전자 메일 채널 구성을 정의할 때 [일반 설정](#admin-settings)에서 설정된 기본 실행 필드를 변경할 수 있습니다. [자세히 알아보기](../email/email-settings.md#execution-address)

전자 메일 구성에 실행 주소가 정의된 경우 이 주소는 기본 주소로 사용되며 샌드박스 수준의 일반 설정을 무시합니다.

### 여정 매개 변수에서 {#journey-parameters}

**[!UICONTROL 여정]**&#x200B;에 **[!UICONTROL Email]** 또는 [SMS](../email/create-email.md#create-email-journey-campaign) 액션을 추가하면 기본 전자 메일 주소가 여정 고급 매개 변수 아래에 표시됩니다.

일부 특정 컨텍스트에서는 필드 오른쪽에 있는 **[!UICONTROL 매개 변수 재정의 활성화]** 아이콘을 사용하여 이 값을 재정의할 수 있습니다.

![](assets/journey-enable-parameter-override.png)

>[!CAUTION]
>
>이메일 주소 재정의는 특정 사용 사례에만 사용해야 합니다. 대부분의 경우 **[!UICONTROL 실행 필드]**&#x200B;에서 기본 주소로 정의된 값을 사용해야 하므로 전자 메일 주소를 변경할 필요가 없습니다.


