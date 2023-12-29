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
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 18%

---

# 실행 주소 변경 {#change-primary-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address"
>title="사용할 주소 정의"
>abstract="데이터베이스에서 여러 이메일 주소 또는 전화번호를 사용하는 경우(개인용, 업무용 등) 전송의 우선 순위를 지정할 수 있는 항목을 선택할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address_header"
>title="사용할 주소 정의"
>abstract="프로필의 이메일 주소 또는 전화번호 확인에 사용되는 필드를 편집하여 전송의 우선 순위를 지정합니다."

프로필을 타겟팅할 때 데이터베이스에서 여러 이메일 주소 또는 전화 번호(전문 이메일 주소, 개인 전화 번호 등)를 사용할 수 있습니다.

그럴 경우, [!DNL Journey Optimizer] 사용 **[!UICONTROL 실행 필드]** 우선 순위의 프로필 서비스에서 사용할 이메일 주소 또는 전화 번호를 결정합니다.

현재 기본적으로 사용되는 필드를 확인하려면 **[!UICONTROL 관리]** > **[!UICONTROL 채널]** > **[!UICONTROL 일반]** > **[!UICONTROL 실행 필드]** 메뉴 아래의 제품에서 사용할 수 있습니다.

![](assets/primary-address-execution-fields.png)

현재 값은 샌드박스 수준의 모든 게재에 사용됩니다. 필요한 경우 이러한 필드를 업데이트할 수 있습니다.

대부분의 경우 실행 필드를 전체적으로 변경하고 모든 이메일 또는 SMS 메시지에 사용해야 하는 값을 정의합니다. <!--[Learn how](#admin-settings)-->

<!--In some specific use cases only, you can override the value set globally and define a different value at the journey level. [Learn more](#journey-parameters)-->

## 관리 설정 업데이트 {#admin-settings}

샌드박스 수준에서 실행 필드를 전체적으로 변경하려면 아래 단계를 따르십시오.

1. 액세스  **[!UICONTROL 채널]** > **[!UICONTROL 일반]** > **[!UICONTROL 실행 필드]** 메뉴 아래의 제품에서 사용할 수 있습니다.

1. 클릭 **[!UICONTROL 편집]** 기본값을 변경합니다.

   ![](assets/primary-address.png)

1. 선택한 현재 필드 또는 편집 아이콘을 클릭하여 새 필드를 선택합니다.

   ![](assets/primary-address-edit.png)

1. 사용 가능한 이메일 유형 XDM 필드 목록이 표시됩니다. 사용할 필드를 선택합니다.

   ![](assets/primary-address-select-field.png)

1. 클릭 **[!UICONTROL 저장]** 선택을 확인합니다.

실행 필드가 업데이트되고, 이제 기본 주소로 사용됩니다.

<!--1. You can also select an additional field to use as secondary email address. This allows you to determine which field to use if the primary field is empty for a profile. -->

## 여정 매개 변수에서 값 재정의 {#journey-parameters}

특정 사용 사례의 경우에만 전역적으로 설정된 실행 필드를 재정의하고 여정 수준(특히 이메일 채널)에서 다른 값을 정의할 수 있습니다.

를 추가할 때 **[!UICONTROL 이메일]** 에 대한 작업 [여정](../email/create-email.md#create-email-journey-campaign)기본 이메일 주소가 여정 고급 매개 변수 아래에 표시됩니다.

일부 특정 컨텍스트에서는 **[!UICONTROL 매개 변수 재정의 활성화]** 아이콘 의 오른쪽 **[!UICONTROL 주소]** 필드.

![](assets/journey-enable-parameter-override.png)

>[!CAUTION]
>
>이메일 주소 재정의는 특정 사용 사례에만 사용해야 합니다. 대부분의 경우 값이 의 기본 주소로 정의되어 있으므로 이메일 주소를 변경할 필요가 없습니다. **[!UICONTROL 실행 필드]** 이것은 사용해야 하는 것입니다.

이 값을 재정의하는 것은 다음과 같은 경우에 유용합니다.

* 이메일을 테스트합니다. 자신의 이메일 주소를 추가할 수 있습니다. 여정을 게시하면 이메일이 전송됩니다.
* 목록의 구독자에게 이메일을 보냅니다. [사용 사례](../building-journeys/message-to-subscribers-uc.md)를 자세히 알아보십시오.
