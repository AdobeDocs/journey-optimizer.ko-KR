---
solution: Journey Optimizer
product: journey optimizer
title: 푸시 알림 디자인
description: Journey Optimizer에서 푸시 알림을 디자인하는 방법을 알아봅니다
feature: Push
topic: Content Management
role: User
level: Beginner
exl-id: 6f6d693d-11f2-48b7-82a8-171829bf8045
source-git-commit: 3dd2db31a239ec5a81bfd677355aca862602e030
workflow-type: tm+mt
source-wordcount: '1365'
ht-degree: 17%

---

# 푸시 알림 디자인 {#design-push-notification}

## 제목 및 본문 {#push-title-body}

>[!CONTEXTUALHELP]
>id="ajo-message-push-compose"
>title="푸시 알림을 개인화합니다."
>abstract="메시지를 작성하려면 제목 및 본문 필드에 내용을 입력합니다. 개인화 토큰을 포함하려면 개인화 대화 상자를 엽니다."

메시지를 작성하려면 **[!UICONTROL 제목]** 및 **[!UICONTROL 본문]** 필드를 클릭합니다. 개인화 편집기를 사용하여 콘텐츠를 정의하고, 데이터를 개인화하고, 다이내믹 콘텐츠를 추가합니다. 개인화 편집기에서 [개인화](../personalization/personalize.md) 및 [다이내믹 콘텐츠](../personalization/get-started-dynamic-content.md)에 대해 자세히 알아보세요.

장치 미리 보기 섹션을 사용하여 iOS 및 Android 장치에 푸시 알림이 표시되는 방식을 시각화합니다.

## 클릭 시 비헤이비어 {#on-click-behavior}

>[!CONTEXTUALHELP]
>id="ajo-message-push-onclick"
>title="클릭 시 비헤이비어 정보"
>abstract="수신자가 푸시 알림 본문을 클릭할 때 비헤이비어를 선택합니다."

사용자가 푸시 알림의 본문을 클릭할 때의 동작을 선택할 수 있습니다.

![](assets/title-body-push.png)

* 앱을 열려면 **[!UICONTROL 앱 열기]** 옵션을 선택합니다. 알림과 연결된 앱이 [채널 구성](../configuration/channel-surfaces.md)(예: 메시지 사전 설정)에 정의되어 있습니다.
* 사용자를 앱 내의 특정 콘텐츠로 리디렉션하려면 **[!UICONTROL 딥링크]** 옵션을 선택하십시오.  특정 콘텐츠는 특정 보기, 페이지의 특정 섹션 또는 특정 탭일 수 있습니다. 옵션을 선택한 후 관련 필드에 딥 링크를 입력합니다.
* 사용자를 외부 URL로 리디렉션하려면 **[!UICONTROL 웹 URL]** 옵션을 사용하십시오. 옵션을 선택한 다음 관련 필드에 URL을 입력합니다.

## 미디어 추가 {#add-media-push}

>[!CONTEXTUALHELP]
>id="ajo-message-push-media"
>title="푸시 알림에 미디어 추가"
>abstract="알림 내에 표시되는 이미지, 비디오 또는 GIF를 추가할 수 있습니다."

푸시 알림의 iOS 버전에서 알림 내에 표시되는 이미지, 비디오 또는 GIF을 추가할 수 있습니다.

Android 버전에서는 이미지 아이콘과 확장된 알림에 대한 이미지만 추가할 수 있습니다.

![](assets/push-config-add-media.png)

두 가지 옵션을 사용할 수 있습니다. 다음과 같은 작업을 수행할 수 있습니다.

* **[!UICONTROL 미디어 추가]** 단추를 사용하여 **[!DNL Adobe Experience Manager Assets]**&#x200B;의 자산을 선택하십시오.

  [이 페이지](../content-management/assets.md)에서 **[!DNL Adobe Experience Manager Assets]**&#x200B;을(를) 사용하는 방법을 알아보세요.

* 또는 **[!UICONTROL 미디어 추가]** 필드에 미디어 URL을 입력하십시오. 이 경우 URL에 개인화를 추가할 수 있습니다.

미디어가 추가되면 알림 본문의 오른쪽에 표시됩니다.

## 버튼 추가 {#add-buttons-push}

>[!CONTEXTUALHELP]
>id="ajo-message-push-buttons"
>title="사용자가 푸시 알림과 상호 작용할 수 있는 버튼을 추가합니다."
>abstract="이 섹션에서는 메시지에 클릭 유도 버튼을 추가할 수 있습니다. iOS의 경우, 알림 카테고리 식별자를 지정합니다. Android의 경우, 각 버튼에 대해 사용자 정의 텍스트 및 대상을 포함할 수 있습니다."

푸시 콘텐츠에 버튼을 추가하여 실행 가능한 알림을 만듭니다.

장치 화면이 잠겨 있으면 알림의 **제목** 및 **메시지** 단추만 표시됩니다. 장치가 잠금 해제되면 수신자에게 버튼이 표시됩니다.

Android 버전에서는 최대 3개의 버튼을 추가할 수 있습니다.

iOS 버전에서는 알림 범주 식별자가 지정됩니다. 표시할 버튼과 수행한 작업을 정의하는 iOS 앱에 알림 범주를 미리 구성해야 합니다. 자세한 내용은 [Apple 설명서](https://developer.apple.com/documentation/usernotifications/declaring_your_actionable_notification_types)를 참조하세요.

1. **[!UICONTROL 추가 단추]**&#x200B;를 사용하여 설정(레이블 및 관련 작업)을 정의합니다. 가능한 작업은 [클릭 시 동작](#on-click-behavior)과 동일합니다.

1. 중앙 미리 보기 이미지 아래의 **[!UICONTROL 보기 확장]** 아이콘을 사용하여 개인화된 단추를 미리 보십시오.

   ![](assets/push_buttons.png)

## 사일런트 알림 보내기 {#silent-notification}

>[!CONTEXTUALHELP]
>id="ajo_message_push_silent_notification"
>title="사일런트 알림 정보"
>abstract="사용자를 방해하지 않고 알림을 전송합니다. 알림 센터나 알림 표시줄에 알림이 표시되지 않습니다."

자동 푸시 알림(또는 백그라운드 알림)은 애플리케이션에 전달되는 숨겨진 명령입니다. 예를 들어 애플리케이션에 새 콘텐츠의 가용성에 대해 알리거나 백그라운드에서 다운로드를 시작하는 데 사용됩니다.

응용 프로그램에 자동으로 알리려면 **[!UICONTROL 자동 알림]** 옵션을 선택하십시오. 이 경우 알림이 응용 프로그램으로 직접 전송됩니다. 장치 화면에 경고가 표시되지 않습니다.

**[!UICONTROL 사용자 지정 데이터]** 섹션을 사용하여 키-값 쌍을 추가합니다.

## 사용자 정의 데이터 {#custom-data}

>[!CONTEXTUALHELP]
>id="ajo-message-push-custom"
>title="푸시 알림에 대한 사용자 정의 데이터를 구성합니다."
>abstract="모바일 애플리케이션 구성에 따라 페이로드에 사용자 정의 변수를 추가합니다."

모바일 애플리케이션 구성에 따라 **[!UICONTROL 사용자 지정 데이터]** 섹션에서 페이로드에 사용자 지정 변수를 추가할 수 있습니다. Adobe Experience Platform Adobe 및 Launch에서 푸시 알림을 설정하는 방법에 대한 자세한 내용은 [이 섹션](push-gs.md)을 참조하세요.

## 고급 옵션 {#advanced-options-push}

>[!CONTEXTUALHELP]
>id="ajo-message-push-advanced"
>title="푸시 알림에 대한 고급 옵션을 구성합니다."
>abstract="이 섹션에서는 푸시 알림의 개인화를 향상할 수 있습니다."

푸시 알림에 대해 **[!UICONTROL 고급 옵션]**&#x200B;을 구성할 수 있습니다. 사용 가능한 매개 변수는 다음과 같습니다.

| 매개변수 | 설명 |
|---------|---------|
| **[!UICONTROL 축소 가능]**(iOS/Android) | 축소 가능한 메시지는 오래된 경우 새 메시지로 대체될 수 있는 메시지입니다. 축소 가능한 메시지의 일반적인 사용 사례는 모바일 앱에 서버의 데이터를 동기화하도록 알리는 데 사용되는 메시지입니다. 예를 들어 사용자를 최신 점수로 업데이트하는 스포츠 앱이 있습니다. 가장 최근 메시지만 관련성이 있습니다. 반면 축소 불가능한 메시지는 클라이언트 앱에 중요하며 전달되어야 합니다. |
| **[!UICONTROL 사용자 지정 사운드]**(iOS/Android) | 알림을 수신할 때 이동 단말기에서 재생될 사운드. 앱에서 사운드를 번들로 제공해야 합니다. |
| **[!UICONTROL 배지]**(iOS/Android) | 배지는 애플리케이션 아이콘에 읽지 않은 새로운 정보의 수를 직접 표시하는 데 사용됩니다. <br/>사용자가 응용 프로그램에서 새 콘텐츠를 열거나 읽으면 배지 값이 사라집니다. 디바이스에서 알림을 받으면 관련 앱에 대한 배지 값을 새로 고치거나 추가할 수 있습니다.<br/>예를 들어, 고객의 읽지 않은 문서 수를 저장하는 경우 개인화를 활용하여 각 고객에 대해 읽지 않은 고유 문서 배지 값을 보낼 수 있습니다. 개인화를 더 보려면 [이 섹션](../personalization/personalize.md)을 참조하세요. |
| **[!UICONTROL 알림 그룹]**(iOS 전용) | 푸시 알림에 알림 그룹을 연결합니다.<br/>iOS 12부터 알림 그룹을 사용하면 메시지 스레드와 알림 주제를 스레드 ID로 통합할 수 있습니다. 예를 들어 브랜드는 하나 이상의 다른 ID에 더 많은 운영 유형 알림을 유지하면서 하나의 그룹 ID로 마케팅 알림을 전송할 수 있습니다.<br/>이를 설명하기 위해 groupID: 123 &quot;새 봄 스웨터 컬렉션 확인&quot; 및 groupID: 456 &quot;패키지가 배달되었습니다&quot; 알림 그룹을 사용할 수 있습니다. 이 예에서 모든 게재 알림은 그룹 ID: 456 아래에 번들로 제공됩니다. |
| **[!UICONTROL 알림 채널]**(Android 전용) | 푸시 알림에 알림 채널을 연결합니다.<br/>Android 8.0(API 레벨 26)부터 모든 알림을 채널에 할당해야 표시됩니다. 자세한 내용은 [Android 개발자 설명서](https://developer.android.com/guide/topics/ui/notifiers/notifications#ManageChannels)를 참조하세요. |
| **[!UICONTROL 콘텐츠 가용성 플래그 추가]**(iOS 전용) | 푸시 알림을 받는 즉시 앱이 깨어날 수 있도록 푸시 페이로드에 사용 가능한 콘텐츠 플래그를 보내 앱이 페이로드 데이터에 액세스할 수 있도록 합니다.<br/> 앱이 백그라운드에서 실행 중이고 사용자 상호 작용(예: 푸시 알림을 누르는 경우)이 필요 없는 경우에도 작동합니다. 하지만 앱이 실행되고 있지 않으면 적용되지 않습니다. 자세한 내용은 [Apple 개발자 설명서](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html)를 참조하십시오. |
| **[!UICONTROL 변경 가능한 콘텐츠 플래그 추가]**(iOS 전용) | 푸시 페이로드에서 변경 가능한 콘텐츠 플래그를 보내고 iOS SDK에 제공된 알림 서비스 애플리케이션 확장에 의해 푸시 알림 콘텐츠가 수정되도록 합니다. 자세한 내용은 [Apple 개발자 설명서](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/ModifyingNotifications.html)를 참조하십시오.<br/>그런 다음 모바일 앱 확장을 활용하여 [!DNL Journey Optimizer]에서 보낸 푸시 알림의 내용 또는 프레젠테이션을 추가로 수정할 수 있습니다. 예를 들어 사용자는 이 옵션을 사용하여 데이터의 암호를 해독하고, 알림의 본문이나 제목 텍스트를 변경하고, 알림에 스레드 식별자를 추가할 수 있습니다. |
| **[!UICONTROL 알림 가시성]**(Android 전용) | 푸시 알림의 가시성을 정의합니다. <br/><b>개인</b>은(는) 모든 잠금 화면에 알림을 표시하지만 보안 잠금 화면에 중요한 정보나 개인 정보를 숨깁니다. <br/><b>공개</b>는 모든 잠금 화면에서 알림을 모두 표시합니다. <br/><b>암호</b>은(는) 보안 잠금 화면에서 알림의 일부를 표시하지 않습니다. <br/>자세한 내용은 [Android 개발자 설명서](https://developer.android.com/reference/android/app/Notification)를 참조하세요. |
| **[!UICONTROL 알림 우선 순위]**(Android 전용) | 푸시 알림의 중요도를 낮음에서 최대로 정의합니다. 푸시 알림이 전달될 때 푸시 알림이 얼마나 &quot;간섭&quot;되는지를 결정합니다. 자세한 내용은 [Android 개발자 설명서](https://developer.android.com/guide/topics/ui/notifiers/notifications#importance)를 참조하세요. |
| **[!UICONTROL 배달 우선 순위]**(Android만 해당) | 푸시 알림에 대해 높은 우선 순위 또는 일반적인 우선 순위를 설정합니다. 메시지 우선 순위에 대한 자세한 내용은 [Google 개발자 설명서](https://firebase.google.com/docs/cloud-messaging/concept-options#setting-the-priority-of-a-message)를 참조하십시오. |
