---
title: '기본 이메일 주소 변경 '
description: 프로필 서비스에서 사용할 이메일 주소를 결정하는 방법을 알아봅니다.
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: fe2f6516-7790-4501-a3a1-3d7cb94d7874
source-git-commit: f1ac47a0cb405eaadc5428e7e5479eaf776d7abe
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 6%

---

# 기본 이메일 주소 변경 {#change-primary-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address"
>title="사용할 주소 정의"
>abstract="데이터베이스에서 여러 주소(개인, 전문가 등)를 사용할 수 있는 경우 발송에 우선 순위를 둘 이메일 주소를 선택할 수 있습니다."

프로필을 타겟팅할 때 데이터베이스에서 여러 이메일 주소(개인, 전문 이메일 주소 등)를 사용할 수 있습니다.

사용 [!DNL Journey Optimizer], 프로필 서비스에서 사용할 이메일 주소를 확인하고 몇 개의 주소를 사용할 수 있는 경우 우선 순위를 지정할 수 있습니다. 이렇게 하려면 아래 단계를 수행합니다.

1. **[!UICONTROL Channels]** > **[!UICONTROL General]** > **[!UICONTROL Executions fields]** 메뉴에 액세스합니다.

   ![](assets/primary-address-execution-fields.png)

1. 현재 이 화면에 표시되는 프로필의 이메일 주소를 결정하는 데 기본적으로 사용되는 필드입니다. 클릭 **[!UICONTROL Edit]** 변경

   ![](assets/primary-address.png)

1. 현재 필드 또는 편집 아이콘을 클릭하여 새 필드를 선택합니다.

   ![](assets/primary-address-edit.png)

1. 사용 가능한 이메일 유형 XDM 필드 목록이 표시됩니다. 사용할 필드를 선택합니다.

   ![](assets/primary-address-field.png)

1. 클릭 **[!UICONTROL Save]** 을 클릭하여 선택 사항을 확인합니다.

   ![](assets/primary-address-save.png)

   실행 필드가 업데이트되어 이제 기본 주소로 사용됩니다.

<!--1. You can also select an additional field to use as secondary email address. This allows you to determine which field to use if the primary field is empty for a profile. -->
