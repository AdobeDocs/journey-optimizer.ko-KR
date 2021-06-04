---
title: 푸시 알림 구성
description: Journey Optimizer을 사용하여 푸시 알림을 전송하도록 환경을 구성하는 방법을 알아봅니다
hide: true
hidefromtoc: true
source-git-commit: 03d003682d796906fcf89af02aa98d549b5214a3
workflow-type: tm+mt
source-wordcount: '624'
ht-degree: 0%

---

# 푸시 알림 채널 구성 {#push-notification-configuration}

![](assets/do-not-localize/badge.png)

[!DNL Journey Optimizer]으로 푸시 알림 전송을 시작하기 전에 [!DNL Adobe Experience Platform] 및 [!DNL Adobe Experience Platform Launch]에서 설정을 정의해야 합니다.

## Adobe Experience Platform 설정 {#platform-settings}

[!DNL Adobe Experience Platform Launch]에서 모바일 앱을 설정하려면 다음 단계를 따르십시오.

1. [속성 및 회사 권한 할당](#push-rights)
1. [platform launch ](#push-credentials-launch)에 모바일 애플리케이션의 푸시 자격 증명을 추가합니다.
1. [확장](#edge-configuration) 에서 모바일  **[!UICONTROL Edge]** 장치에서 로 사용자 지정 데이터를 전송하는 데 사용할 Edge 구성을  [!DNL Adobe Experience Platform]만듭니다.
1. [platform launch 속성을 설정합니다](#launch-property).
1. [속성을 게시합니다](#publish-property).
1. [ProfileDataSource를 구성합니다](#configure-profiledatasource).

### 1단계:속성 및 회사 권한 할당 {#push-rights}

모바일 애플리케이션을 만들기 전에 먼저 올바른 사용자 권한이 있는지 또는 지정되었는지 확인해야 합니다.

[!DNL Adobe Experience Platform Launch]을 사용하는 사용자 관리에 대한 자세한 내용은 [Platform launch 설명서](https://experienceleague.adobe.com/docs/launch/using/admin/user-permissions.html#experience-cloud-permissions)를 참조하십시오.

속성 및 회사 권한을 할당하려면

1. [!DNL Admin Console]에 액세스합니다.

1. **[!UICONTROL Products]** 탭에서 **[!UICONTROL Adobe Experience Platform Launch]** 카드를 선택합니다.

   ![](assets/push_product_1.png)

1. 기존 **[!UICONTROL Product Profile]** 을 선택하거나 **[!UICONTROL New profile]** 버튼을 사용하여 새 하나를 만듭니다. 새 **[!UICONTROL New profile]**&#x200B;을(를) 만드는 방법에 대한 자세한 내용은 [Admin Console 설명서](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/create-profile.html#ui)를 참조하십시오.

1. **[!UICONTROL Permissions]** 탭에서 **[!UICONTROL Property rights]** 을 선택합니다.

   ![](assets/push_product_2.png)

1. **[!UICONTROL Add all]**&#x200B;을 클릭합니다. 이렇게 하면 제품 프로필에 다음 권한이 추가됩니다.
   * **[!UICONTROL Approve]**
   * **[!UICONTROL Develop]**
   * **[!UICONTROL Manage Environments]**
   * **[!UICONTROL Manage Extensions]**
   * **[!UICONTROL Publish]**

   ![](assets/push_product_3.png)

1. 그런 다음 왼쪽 메뉴에서 **[!UICONTROL Company rights]** 을 선택합니다.

   ![](assets/push_product_4.png)

1. 다음 권한을 추가합니다.

   * **[!UICONTROL Manage App Configurations]**
   * **[!UICONTROL Manage Properties]**

   ![](assets/push_product_5.png)

1. **[!UICONTROL Save]**&#x200B;을 클릭합니다.

이 **[!UICONTROL Product profile]**&#x200B;을 사용자에게 할당하려면

1. [!DNL Admin Console]의 **[!UICONTROL Products]** 탭에서 **[!UICONTROL Adobe Experience Platform Launch]** 카드를 선택합니다.

1. 이전에 구성한 **[!UICONTROL Product profile]** 을 선택합니다.

1. **[!UICONTROL Users]** 탭에서 **[!UICONTROL Add user]**&#x200B;을 클릭합니다.

   ![](assets/push_product_6.png)

1. 사용자 이름이나 이메일 주소를 입력하고 사용자를 선택합니다. 그런 다음 **[!UICONTROL Save]** 을 클릭합니다.

   >[!NOTE]
   >
   >이전에 Admin Console에서 사용자를 만들지 않은 경우 [사용자 추가 설명서](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html#add-users)를 참조하십시오.

   ![](assets/push_product_7.png)


이제 [!DNL Adobe Experience Platform Launch]에서 모바일 애플리케이션을 만들고 구성할 수 있는 올바른 사용자 권한이 있습니다.

### 2단계:platform launch {#push-credentials-launch}에 모바일 애플리케이션 푸시 자격 증명을 추가합니다.

올바른 사용자 권한을 부여한 후 이제 [!DNL Adobe Experience Platform Launch]에 모바일 애플리케이션 푸시 자격 증명을 추가해야 합니다.

모바일 애플리케이션 푸시 자격 증명을 추가하는 방법에 대한 자세한 내용 및 절차는 [Adobe Experience Platform Mobile SDK 설명서](https://aep-sdks.gitbook.io/docs/beta/adobe-journey-optimizer#configure-the-journey-optimizer-extension-in-launch)에 설명된 단계를 참조하십시오.

<!--
Note that to add push credentials in [!DNL Adobe Experience Platform Launch], the owner of the mobile app should fetch them from APNs/FCM.
1. From [!DNL Adobe Experience Platform Launch], ensure that **[!UICONTROL Client Side]** is selected in the drop-down menu.

1. Select the **[!UICONTROL App Configurations]** tab in the left-hand panel and click **[!UICONTROL App Configuration]** to create a new configuration.

1. Enter a **[!UICONTROL Name]** for the configuration.

1. From the **[!UICONTROL Messaging Service Type]** drop-down menu, select the **[!UICONTROL Messaging service type]** to be used for these credentials. Here, we selected **[!UICONTROL Apple Push Notification Service]** since we are working with iOS.

1. Enter the mobile app **[!UICONTROL Bundle Id]** in the **[!UICONTROL App ID (iOS Bundle ID)]** field if you are using Apple push notification service or in the **[!UICONTROL App ID (Android package name)]** field if you are using Firebase Cloud Messaging.

    ![](assets/push_launch_app_configuration.png)

1. Drag and drop the .p8 key file or the .json private key file to the **[!UICONTROL Push Credentials]** field.

1. Enter the **[!UICONTROL Key Id]** and **[!UICONTROL Team Id]** if you are using Apple push notification service.

1. Click **[!UICONTROL Save]** to create your app configuration.
-->

### 3단계:에지 구성 만들기 {#edge-configuration}

**[!UICONTROL Edge configuration]** 는 확장 **[!UICONTROL Edge]** 에서 모바일 장치에서 사용자 지정 데이터로 사용자 지정 데이터를 전송하는 데 사용됩니다 [!DNL Adobe Experience Platform].
[!DNL Adobe Experience Platform]을 구성하려면 **[!UICONTROL Sandbox]** 이름과 **[!UICONTROL Event Dataset]**&#x200B;를 제공해야 합니다.

**[!UICONTROL Edge configuration]** 을 만드는 방법에 대한 자세한 내용과 절차는 [Adobe Experience Platform Mobile SDK 설명서](https://aep-sdks.gitbook.io/docs/getting-started/configure-datastreams)에 자세히 나와 있는 단계를 참조하십시오.


<!--
1. From [!DNL Adobe Experience Platform Launch], select the **[!UICONTROL Edge Configurations]** tab and click **[!UICONTROL Edge Configurations]**.
    
1. Select **[!UICONTROL New Edge Configuration]** to add a new **[!UICONTROL Edge Configuration]**.
1. Enter a **[!UICONTROL Name]** and click **[!UICONTROL Save]**

1. Click the **[!UICONTROL Adobe Experience Platform]** toggle to enable it.

1. Fill in the **[!UICONTROL Sandbox]**, **[!UICONTROL Event dataset]** and **[!UICONTROL Profile Dataset]** fields. Then, click **[!UICONTROL Save]**.
    
    ![](assets/push-config-4.png)
-->

### 4단계:platform launch 속성 {#launch-property} 설정

[!DNL Adobe Experience Platform Launch] 속성을 설정하면 모바일 앱 개발자 또는 마케터가 세션 시간 초과, 타깃팅할 [!DNL Adobe Experience Platform] 샌드박스 및 데이터를 보낼 모바일 SDK에 사용할 **[!UICONTROL Adobe Experience Platform Datasets]** 등의 모바일 SDK 속성을 구성할 수 있습니다.

**[!UICONTROL Platform Launch property]** 설정 방법에 대한 자세한 내용 및 절차는 [Adobe Experience Platform Mobile SDK 설명서](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property#create-a-mobile-property)에 자세히 설명된 단계를 참조하십시오.

푸시 알림이 작동하는 데 필요한 SDK를 가져오려면 Android 및 iOS용 다음 SDK 확장이 필요합니다.

* **[!UICONTROL Mobile Core]** (자동으로 설치됨)
* **[!UICONTROL Profile]** (자동으로 설치됨)
* **[!UICONTROL Adobe Experience Platform Edge]**
* **[!UICONTROL Adobe Experience Platform Assurance]**, 선택 사항이지만 모바일 구현을 디버깅하는 것이 좋습니다.

[!DNL Adobe Experience Platform Launch] 확장에 대한 자세한 내용은 [Platform launch 설명서](https://experienceleague.adobe.com/docs/launch-learn/implementing-in-mobile-android-apps-with-launch/configure-launch/launch-add-extensions.html)를 참조하십시오.

<!--

1. From [!DNL Adobe Experience Platform Launch], ensure that **[!UICONTROL Client Side]** is selected in the drop-down menu.

1. select the **[!UICONTROL Properties]** tab and click **[!UICONTROL New Property]**.

    ![](assets/push-config-6.png)

1. Enter a **[!UICONTROL Name]** for your new property.

1. Select **[!UICONTROL Mobile]** as **[!UICONTROL Platform]**.

    ![](assets/push-config-7.png)

1. Click **[!UICONTROL Save]** to create your new property.

To configure **[!UICONTROL Adobe Experience Platform Edge Extension]** to send custom data from mobile devices to [!DNL Adobe Experience Platform].

1. Select your previously created property and select the **[!UICONTROL Extensions]** tab to view the extensions for this property.

    ![](assets/push-config-8.png)

1. Click **[!UICONTROL Configure]** under the **[!UICONTROL Adobe Experience Platform Edge]** Network' extension.

1. From the **[!UICONTROL Edge Configuration]** drop-down list, select the **[!UICONTROL Edge Configuration]** created in the previous steps. For more information on **[!UICONTROL Edge Configuration]**, refer to this [section](#edge-configuration).

1. Click **[!UICONTROL Save]**.

To configure **[!UICONTROL Adobe Experience Platform Messaging]** extension to send push profile and push interactions to the correct datasets, follow the same steps as above. Use **[!UICONTROL Sandbox]**, **[!UICONTROL Event dataset]** and **[!UICONTROL Profile Dataset]** created in the [Adobe Experience Platform setup](#edge-configuration).
-->

### 5단계:속성 {#publish-property} 게시

이제 구성을 통합하고 모바일 앱에서 사용하려면 속성을 게시해야 합니다.

속성을 게시하려면 [Adobe Experience Platform Mobile SDK 설명서](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property#publish-the-configuration)에 자세히 나와 있는 단계를 참조하십시오

### 6단계:ProfileDataSource {#configure-profiledatasource} 구성

`ProfileDataSource`을(를) 구성하려면 [!DNL Adobe Experience Platform] 설정의 `ProfileDCInletURL`을(를) 사용하고 모바일 앱에 다음을 추가하십시오.

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

### 7단계:메시지 사전 설정 {#message-preset} 만들기

모바일 앱이 [!DNL Adobe Experience Platform Launch]에 설정되면 **[!DNL Journey Optimizer]**&#x200B;에서 푸시 알림을 전송할 수 있도록 메시지 사전 설정을 만들어야 합니다.

[이 섹션](configuration/message-presets.md)에서 메시지 사전 설정을 만들고 구성하는 방법을 알아봅니다.