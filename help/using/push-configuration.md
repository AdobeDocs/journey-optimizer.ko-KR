---
title: 푸시 알림 구성
description: Journey Optimizer을 사용하여 푸시 알림을 전송하도록 환경을 구성하는 방법에 대해 알아봅니다.
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '744'
ht-degree: 0%

---

# 푸시 알림 구성 {#push-notification-configuration}

![](assets/do-not-localize/badge.png)

## 푸시 구성 {#gs-push} 시작하기

[!DNL Journey Optimizer]으로 푸시 알림을 전송하기 전에 [!DNL Adobe Experience Platform] 및 [!DNL Adobe Experience Platform Launch] 모두에 설정을 정의해야 합니다.

## Adobe Experience Platform 설정 {#platform-settings}

[!DNL Adobe Experience Platform Launch]에서 모바일 앱을 설정하려면 다음 단계를 따르십시오.

1. [속성 및 회사 권한 할당](#push-rights)
1. [platform launch에 모바일 응용 프로그램의 푸시 자격 증명을 추가합니다](#push-credentials-launch).
1. [Edge ](#edge-configuration) 구성을 만들어  **[!UICONTROL Edge]** 확장 기능이 사용하여 모바일 디바이스에서 모바일 디바이스로 맞춤형 데이터를 보낼 수  [!DNL Adobe Experience Platform]있습니다.
1. [platform launch 속성을 설정합니다](#launch-property).
1. [속성을 게시합니다](#publish-property).
1. [ProfileDataSource를 구성합니다](#configure-profiledatasource).

### 1단계:속성 및 회사 권한 할당 {#push-rights}

모바일 응용 프로그램을 만들기 전에 먼저 올바른 사용자 권한을 가지고 있는지 또는 할당해야 합니다.

[!DNL Adobe Experience Platform Launch]의 사용자 관리에 대한 자세한 내용은 [Platform launch 설명서](https://experienceleague.adobe.com/docs/launch/using/admin/user-permissions.html#experience-cloud-permissions)를 참조하십시오.

속성 및 회사 권한을 지정하려면

1. [!DNL Admin Console]에 액세스합니다.

1. **[!UICONTROL Products]** 탭에서 **[!UICONTROL Adobe Experience Platform Launch]** 카드를 선택합니다.

   ![](assets/push_product_1.png)

1. 기존 **[!UICONTROL Product Profile]**&#x200B;을 선택하거나 **[!UICONTROL New profile]** 단추를 사용하여 새  단추를 만듭니다. 새 **[!UICONTROL New profile]**&#x200B;을(를) 만드는 방법에 대한 자세한 내용은 [관리 콘솔 문서](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/create-profile.html#ui)를 참조하십시오.

1. **[!UICONTROL Permissions]** 탭에서 **[!UICONTROL Property rights]**&#x200B;을 선택합니다.

   ![](assets/push_product_2.png)

1. **[!UICONTROL Add all]**&#x200B;을 클릭합니다. 제품 프로필에 다음과 같은 권한이 추가됩니다.
   * **[!UICONTROL Approve]**
   * **[!UICONTROL Develop]**
   * **[!UICONTROL Manage Environments]**
   * **[!UICONTROL Manage Extensions]**
   * **[!UICONTROL Publish]**

   ![](assets/push_product_3.png)

1. 그런 다음 왼쪽 메뉴에서 **[!UICONTROL Company rights]**&#x200B;을 선택합니다.

   ![](assets/push_product_4.png)

1. 다음 권한을 추가합니다.

   * **[!UICONTROL Manage App Configurations]**
   * **[!UICONTROL Manage Properties]**

   ![](assets/push_product_5.png)

1. **[!UICONTROL Save]**&#x200B;을 클릭합니다.

이 **[!UICONTROL Product profile]**&#x200B;을(를) 사용자에게 할당하려면:

1. [!DNL Admin Console]의 **[!UICONTROL Products]** 탭에서 **[!UICONTROL Adobe Experience Platform Launch]** 카드를 선택합니다.

1. 이전에 구성한 **[!UICONTROL Product profile]**&#x200B;을 선택합니다.

1. **[!UICONTROL Users]** 탭에서 **[!UICONTROL Add user]**&#x200B;을 클릭합니다.

   ![](assets/push_product_6.png)

1. 사용자 이름 또는 이메일 주소를 입력하고 사용자를 선택합니다. 그런 다음 **[!UICONTROL Save]**&#x200B;을 클릭합니다.

   >[!NOTE]
   >
   >사용자가 관리 콘솔에서 이전에 만들어지지 않은 경우 [사용자 추가 설명서](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html#add-users)를 참조하십시오.

   ![](assets/push_product_7.png)


이제 [!DNL Adobe Experience Platform Launch]에서 모바일 응용 프로그램을 만들고 구성할 수 있는 올바른 사용자 권한이 있습니다.

### 2단계:platform launch {#push-credentials-launch}에 모바일 응용 프로그램 푸시 자격 증명 추가

>[!NOTE]
>
> [!DNL Adobe Experience Platform Launch]에 푸시 자격 증명을 추가하려면 모바일 앱 소유자가 APNs/FCM에서 푸시 자격 증명을 가져와야 합니다.

1. [!DNL Adobe Experience Platform Launch]에서 드롭다운 메뉴에서 **[!UICONTROL Client Side]**&#x200B;이 선택되어 있는지 확인합니다.

1. 왼쪽 패널에서 **[!UICONTROL App Configurations]** 탭을 선택하고 **[!UICONTROL App Configuration]**&#x200B;을 클릭하여 새 구성을 만듭니다.

1. 구성에 대해 **[!UICONTROL Name]**&#x200B;을 입력합니다.

1. **[!UICONTROL Messaging Service Type]** 드롭다운 메뉴에서 이러한 자격 증명에 사용할 **[!UICONTROL Messaging service type]**&#x200B;을 선택합니다. 여기서 **[!UICONTROL Apple Push Notification Service]**&#x200B;은(는) iOS를 사용하여 작업하고 있으므로 선택했습니다.

1. Apple 푸시 알림 서비스를 사용하는 경우 **[!UICONTROL App ID (iOS Bundle ID)]** 필드에 모바일 앱 **[!UICONTROL Bundle Id]**&#x200B;을, Firebase 클라우드 메시지 기능을 사용하는 경우에는 **[!UICONTROL App ID (Android package name)]** 필드에 입력합니다.

   ![](assets/push_launch_app_configuration.png)

1. .p8 키 파일 또는 .json 개인 키 파일을 **[!UICONTROL Push Credentials]** 필드에 드래그하여 놓습니다.

1. Apple 푸시 알림 서비스를 사용하는 경우 **[!UICONTROL Key Id]** 및 **[!UICONTROL Team Id]**&#x200B;을 입력합니다.

1. **[!UICONTROL Save]**&#x200B;을 클릭하여 앱 구성을 만듭니다.

### 3단계:가장자리 구성 {#edge-configuration} 만들기

**[!UICONTROL Edge configuration]** 는  **[!UICONTROL Edge]** 확장 기능으로 모바일 장치에서 사용자 지정 데이터를 전송하는 데 사용됩니다  [!DNL Adobe Experience Platform].
[!DNL Adobe Experience Platform]을 구성하려면 **[!UICONTROL Sandbox]** 이름과 **[!UICONTROL Event Dataset]**&#x200B;를 제공해야 합니다.

1. [!DNL Adobe Experience Platform Launch]에서 **[!UICONTROL Edge Configurations]** 탭을 선택하고 **[!UICONTROL Edge Configurations]**&#x200B;를 클릭합니다.

1. **[!UICONTROL New Edge Configuration]**&#x200B;을 선택하여 새 **[!UICONTROL Edge Configuration]**&#x200B;을 추가합니다.
1. **[!UICONTROL Name]**&#x200B;을 입력하고 **[!UICONTROL Save]**&#x200B;을 클릭합니다.

1. **[!UICONTROL Adobe Experience Platform]** 토글을 클릭하여 활성화합니다.

1. **[!UICONTROL Sandbox]**, **[!UICONTROL Event dataset]** 및 **[!UICONTROL Profile Dataset]** 필드를 채웁니다. 그런 다음 **[!UICONTROL Save]**&#x200B;을 클릭합니다.

   ![](assets/push-config-4.png)

### 4단계:platform launch 속성 {#launch-property} 설정

[!DNL Adobe Experience Platform Launch] 속성을 설정하면 모바일 앱 개발자 또는 마케터가 세션 시간 초과, 타깃팅할 [!DNL Adobe Experience Platform] 샌드박스 및 데이터를 전송하는 모바일 SDK에 사용할 **[!UICONTROL Adobe Experience Platform Datasets]**&#x200B;와 같은 모바일 SDK 속성을 구성할 수 있습니다.

1. [!DNL Adobe Experience Platform Launch]에서 드롭다운 메뉴에서 **[!UICONTROL Client Side]**&#x200B;이 선택되어 있는지 확인합니다.

1. **[!UICONTROL Properties]** 탭을 선택하고 **[!UICONTROL New Property]**&#x200B;을 클릭합니다.

   ![](assets/push-config-6.png)

1. 새 속성에 대해 **[!UICONTROL Name]**&#x200B;을 입력합니다.

1. **[!UICONTROL Mobile]**&#x200B;을 **[!UICONTROL Platform]**(으)로 선택합니다.

   ![](assets/push-config-7.png)

1. **[!UICONTROL Save]**&#x200B;을 클릭하여 새 속성을 만듭니다.

푸시 알림이 작동되는 데 필요한 SDK를 얻으려면 Android 및 iOS용 다음 SDK 확장이 필요합니다.

* **[!UICONTROL Mobile Core]** (자동으로 설치됨)
* **[!UICONTROL Profile]** (자동으로 설치됨)
* **[!UICONTROL Adobe Experience Platform Edge]**
* **[!UICONTROL Adobe Experience Platform Assurance]**, 선택 사항이지만 모바일 구현을 디버깅하는 것이 좋습니다.

[!DNL Adobe Experience Platform Launch] 확장에 대한 자세한 내용은 [Platform launch 설명서](https://experienceleague.adobe.com/docs/launch-learn/implementing-in-mobile-android-apps-with-launch/configure-launch/launch-add-extensions.html)를 참조하십시오.

모바일 장치에서 [!DNL Adobe Experience Platform](으)로 사용자 지정 데이터를 전송하도록 **[!UICONTROL Adobe Experience Platform Edge Extension]**&#x200B;을(를) 구성하려면

1. 이전에 만든 속성을 선택하고 **[!UICONTROL Extensions]** 탭을 선택하여 이 속성의 확장을 봅니다.

   ![](assets/push-config-8.png)

1. **[!UICONTROL Adobe Experience Platform Edge]** 네트워크&#39; 확장 아래에 있는 **[!UICONTROL Configure]**&#x200B;을 클릭합니다.

1. **[!UICONTROL Edge Configuration]** 드롭다운 목록에서 이전 단계에서 만든 **[!UICONTROL Edge Configuration]**&#x200B;을 선택합니다. **[!UICONTROL Edge Configuration]**&#x200B;에 대한 자세한 내용은 이 [섹션](#edge-configuration)을 참조하십시오.

1. **[!UICONTROL Save]**&#x200B;을 클릭합니다.

푸시 프로필 및 푸시 상호 작용을 올바른 데이터 세트로 보내도록 **[!UICONTROL Adobe Experience Platform Messaging]** 확장을 구성하려면 위와 동일한 단계를 수행하십시오. [Adobe Experience Platform 설정](#edge-configuration)에서 만든 **[!UICONTROL Sandbox]**, **[!UICONTROL Event dataset]** 및 **[!UICONTROL  Profile Dataset]**&#x200B;를 사용합니다.

### 5단계:속성 {#publish-property} 게시

이제 구성을 통합하고 모바일 앱에서 사용하려면 속성을 게시해야 합니다.
속성을 게시하려면 [Adobe Experience Platform Mobile SDK 설명서](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property#publish-the-configuration)에 설명된 단계를 참조하십시오.

### 6단계:ProfileDataSource {#configure-profiledatasource} 구성

`ProfileDataSource`을(를) 구성하려면 [!DNL Adobe Experience Platform] 설정의 `ProfileDCInletURL`을(를) 사용하고 모바일 앱에 다음 내용을 추가하십시오.

```
    MobileCore.updateConfiguration(
    mutableMapOf("messaging.dccs" to <ProfileDCSInletURL>)
```

<!--
## Test your mobile app with custom action {#mobile-app-test}

After configuring your mobile app in both Adobe Experience Platform and Adobe Launch, you can now test it before sending push notifications to your profiles. In this use case, we will create a journey to target our mobile app and set a custom action which will trigger the push notification.

You can use a test mobile app for this use case. For more on this, refer to this [page](https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=CJM&title=Details+of+setting+the+mobile+test+app) (internal use only).

For this journey to work, you need to create an XDM schema. For more information, refer to [XDM documentation](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=en#schemas-and-data-ingestion).

1. In the left menu, click **[!UICONTROL Data]** then **[!UICONTROL Schemas]** under **[!UICONTROL Data management]** to create your XDM schema.

    ![](assets/test_push_1.png)

1. Click **[!UICONTROL Create schema]** then select **[!UICONTROL XDM Experience event]**.

    ![](assets/test_push_2.png)

1. In the right pane, enter the name of your schema and description. Enable this schema for **[!UICONTROL Profile]**.

1. In the left pane, click **[!UICONTROL Add]** under **[!UICONTROL Mixins]** and select  **[!UICONTROL Create a new Mixin]**. For more information on how to create mixin, refer to [XDM System documentation](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/create-mixin.html?lang=en#api).

    ![](assets/test_push_3.png)

1. Enter a **[!UICONTROL Display Name]** and a **[!UICONTROL Description]**. Click **[!UICONTROL Add mixin]** when done.

    ![](assets/test_push_4.png)

1. In the **[!UICONTROL Field properties]** window, add a **[!UICONTROL Field name]**, **[!UICONTROL Display name]** and select **[!UICONTROL String]** as **[!UICONTROL Type]**.

    ![](assets/test_push_5.png)

1. Check **[!UICONTROL Required]** and click **[!UICONTROL Apply]**.

1. Click **[!UICONTROL Save]**. Your schema is now created and can be used in an **[!UICONTROL Event schema]**.

You then need to set up an **[!UICONTROL Event schema]** where you will set the custom action which you will need to enter in your mobile app to trigger your push notification.

1. From the left menu of the home page, click the **[!UICONTROL Admin]** icon, then click **[!UICONTROL Manage]** from the **[!UICONTROL Events]** card to create your new **[!UICONTROL Event schema]**.

1. Click **[!UICONTROL Add]**, the event configuration pane opens on the right side of the screen.

    ![](assets/test_push_6.png)

1. Enter the name of your event. You can also add a description.

1. In the **[!UICONTROL Event ID type]** field, select **[!UICONTROL Rule Based]**.

1. In the **[!UICONTROL Parameters]**, select your previously created XDM event.

    ![](assets/test_push_7.png)

1. Click **[!UICONTROL Edit]** in the **[!UICONTROL Event ID condition]** field.

1. Drag and your previously added mixin to define the condition that will be used by the system to identify the events that will trigger your journey.

    ![](assets/test_push_8.png)

1. Type in the syntax that you will need to use to trigger your push notification in your test app, in this example **order confirmation**.

    ![](assets/test_push_9.png)

1. Select **[!UICONTROL ECID]** as your **[!UICONTROL Namespace]**.

1. Click **[!UICONTROL Ok]** then **[!UICONTROL Save]**.

Your **[!UICONTROL Event schema]** is now created and can now be used in a journey.

1. In the left menu from [!DNL Journey Optimizer] homepage, click **[!UICONTROL Journeys]**.

1. Click **[!UICONTROL Create]** to create a new journey.

    ![](assets/test_push_10.png)

1. Edit the journey's properties in the configuration pane displayed on the right side. Learn more in this [section](building-journeys/journey-gs.md#change-properties).

1. Start by drag and dropping the **[!UICONTROL Event schema]** created in the previous steps from the **[!UICONTROL Events]** drop-down.

    ![](assets/test_push_11.png)

1. From the **[!UICONTROL Actions]** drop-down, drag and drop a **[!UICONTROL Message]** activity to your journey.

1. Select a previously created message. For more information on how to create push notifications, refer to this [page](create-message.md).

1. Drag and drop an **[!UICONTROL End]** activity to your journey.

1. Activate **[!UICONTROL Test]** to your journey to start testing your push notifications and click **[!UICONTROL Trigger an event]**.

    ![](assets/test_push_12.png)

1. Enter your ECID in the **[!UICONTROL Key]** field then your event that will trigger the push notification in our case **order confirmation**.

    ![](assets/test_push_13.png)

1. Click **[!UICONTROL Send]**.

Your event will be triggered and you will receive your push notification to your mobile app.

![](assets/test_push_14.png)
-->
