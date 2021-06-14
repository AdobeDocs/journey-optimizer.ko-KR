---
title: 푸시 알림 구성
description: Journey Optimizer에서 푸시 알림을 만드는 방법을 알아봅니다
feature: 개요
topic: 콘텐츠 관리
role: User
level: Beginner
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '1166'
ht-degree: 11%

---

# 푸시 알림 만들기 {#create-push-notification}

![](assets/do-not-localize/badge.png)

[메시지](create-message.md)를 만든 후 **[!UICONTROL Push Notification]** 탭을 클릭하여 푸시 알림의 설정과 콘텐츠를 정의합니다.

![](assets/create-content-push.png)

전용 탭을 사용하여 **iOS** 및 **Android** 운영 체제에 대한 푸시 알림 설정을 정의합니다.

>[!NOTE]
>
>**[!UICONTROL Compose Message]** 섹션은 **[!UICONTROL iOS]** 탭과 **[!UICONTROL Android]** 탭 모두에 공통입니다. 이 섹션의 변경 사항은 두 탭 모두에 적용됩니다.

## 제목 및 본문

메시지를 작성하려면 **[!UICONTROL Title]** 및 **[!UICONTROL Body]** 필드를 클릭합니다. 표현식 편집기를 사용하여 컨텐츠 및 개인화 데이터를 정의합니다. [이 섹션](personalization/personalize.md)의 표현식 편집기에서 개인화에 대해 자세히 알아보십시오

중앙 섹션을 사용하여 iOS 및 Android 장치에서 푸시 알림이 표시되는 방식을 시각화합니다.

## 클릭 동작 {#on-click-behavior}

수신자가 푸시 알림의 본문을 클릭할 때의 동작을 선택합니다.

![](assets/title-body-push.png)

* **[!UICONTROL Open app]** 옵션을 사용하여 **[!UICONTROL Preset]** 메시지와 연결된 응용 프로그램을 엽니다.
* 수신자를 애플리케이션 내에 있는 특정 콘텐츠로 리디렉션하려면 **[!UICONTROL Deeplink]** 옵션을 사용합니다. 관련 필드에 딥 링크를 입력합니다.
* 수신자를 외부 URL로 리디렉션하려면 **[!UICONTROL Web URL]** 옵션을 사용합니다. 관련 필드에 URL을 입력합니다.

## 미디어 추가

푸시 알림의 iOS 버전에서 알림 내에 표시될 이미지, 비디오 또는 GIF를 추가할 수 있습니다.

Android 버전에서는 이미지 아이콘과 확장된 알림용 이미지만 추가할 수 있습니다.

![](assets/push-config-add-media.png)

두 가지 옵션을 사용할 수 있습니다. 다음을 수행할 수 있습니다.

* **[!UICONTROL Add media]** 단추를 클릭하여 **[!DNL Adobe Experience Manager Assets Essentials]**&#x200B;에서 자산을 선택합니다.

   [이 페이지](assets-essentials.md)에서 **[!DNL Adobe Experience Manager Assets Essentials]**&#x200B;을 사용하는 방법을 알아봅니다.

* 또는 **[!UICONTROL Add media]** 필드를 클릭하여 미디어의 URL을 입력합니다. 이 경우 개인화를 추가할 수 있습니다.

추가된 미디어가 알림 본문의 오른쪽에 표시됩니다.


## 단추 추가

푸시 콘텐츠에 단추를 추가하여 실행 가능한 알림을 만들 수 있습니다.

장치 화면이 잠긴 경우 다음 단추가 표시되지 않습니다.알림의 **제목** 및 **메시지**&#x200B;만 표시됩니다. 장치의 잠금을 해제하면 수신자에게 단추가 표시됩니다.

iOS 버전에서는 최대 4개의 버튼을 추가할 수 있습니다. Android 버전에서는 최대 3개의 버튼을 추가할 수 있습니다.

**[!UICONTROL Add button]** 을 클릭하여 설정을 정의합니다.레이블 및 관련 작업입니다. 가능한 작업은 [클릭 동작](#on-click-behavior)과 동일합니다.


>[!NOTE]
>
>iOS의 경우 **[!UICONTROL iOS category]** 필드를 사용하여 작업을 알림 카테고리와 연결합니다.


## 자동 알림 보내기

자동 푸시 알림(또는 백그라운드 알림)은 애플리케이션에 전달되는 숨겨진 명령입니다. 이 변수는 새로운 컨텐츠의 가용성을 애플리케이션에 알리거나 백그라운드에서 다운로드를 시작하는 데 사용됩니다.

**[!UICONTROL Silent Notification]** 옵션을 선택하여 애플리케이션에 조용히 알림을 보냅니다.이 경우 알림이 애플리케이션에 직접 전송됩니다. 장치 화면에 경고가 표시되지 않습니다.

**[!UICONTROL Custom data]** 섹션을 사용하여 키/값 쌍을 추가합니다.

## 사용자 지정 데이터

**[!UICONTROL Custom data]** 섹션에서는 모바일 애플리케이션 구성에 따라 페이로드에 사용자 지정 변수를 추가할 수 있습니다. Adobe Experience Platform 및 Adobe Launch에서 푸시 알림을 설정하는 방법에 대한 자세한 내용은 [이 섹션](push-gs.md)을 참조하십시오

## 고급 옵션

푸시 알림에 대해 **[!UICONTROL Advanced options]**&#x200B;을 구성할 수 있습니다. 사용 가능한 매개 변수는 아래에 나와 있습니다.

| 매개 변수 | 설명 |
|---------|---------|
| **[!UICONTROL Collapsible]** (iOS / Android) | 축소 가능한 메시지는 새 메시지로 대체될 수 있는 메시지입니다. 예를 들어 주제에 대한 최신 뉴스로 사용자를 업데이트하는 응용 프로그램이 있습니다. 이 경우 가장 최근 메시지만 관련이 있습니다. 반면, 축소 불가능한 메시지는 클라이언트 앱에 중요하며 모든 메시지를 전달해야 합니다. |
| **[!UICONTROL Custom sound]** (iOS / Android) | 알림을 받을 때 이동 단말기에서 재생할 사운드입니다. 앱에서 사운드를 번들로 제공해야 합니다. |
| **[!UICONTROL Badges]** (iOS / Android) | 배지는 애플리케이션 아이콘에 읽지 않은 새로운 정보의 수를 직접 표시하는 데 사용됩니다. <br/>사용자가 애플리케이션에서 새 콘텐츠를 열거나 읽으면 배지 값이 사라집니다. 디바이스에서 알림을 받으면 관련 앱에 대한 배지 값을 새로 고침하거나 추가할 수 있습니다.<br/>예를 들어 고객의 읽지 않은 문서 수를 저장하는 경우 개인화를 활용하여 각 고객에 대한 읽지 않은 고유한 문서 배지 값을 보낼 수 있습니다. 개인화에 대한 자세한 정보는 [이 섹션](personalization/personalize.md)을 참조하십시오. |
| **[!UICONTROL Notification group]**  (iOS만 해당) | 알림 그룹을 푸시 알림에 연결합니다.<br/>iOS 12부터 알림 그룹을 사용하면 메시지 스레드 및 알림 항목을 스레드 ID로 통합할 수 있습니다. 예를 들어, 브랜드는 하나 이상의 다른 ID 아래에 더 많은 운영 유형 알림을 유지하면서 한 그룹 ID에 마케팅 알림을 보낼 수 있습니다.<br/>이를 보여주기 위해 groupID가 있을 수 있습니다.123 &quot;스웨터의 새 봄 컬렉션 확인&quot; 및 groupID:456 &quot;패키지가 전달됨&quot; 알림 그룹. 이 예에서는 모든 게재 알림이 그룹 ID 아래에 번들로 제공됩니다.456. |
| **[!UICONTROL Notification channel]** (Android만 해당) | 푸시 알림에 알림 채널을 연결합니다.<br/>Android 8.0(API 레벨 26)부터 표시하려면 모든 알림을 채널에 할당해야 합니다. 자세한 내용은 [Android 개발자 설명서](https://developer.android.com/guide/topics/ui/notifiers/notifications#ManageChannels)를 참조하십시오. |
| **[!UICONTROL Add content-availability flag]** (iOS만 해당) | 푸시 알림을 받는 즉시 앱이 깨어날 수 있도록 푸시 페이로드에서 사용 가능한 콘텐츠 플래그를 보냅니다. 즉, 앱이 페이로드 데이터에 액세스할 수 있습니다.<br/> 이는 앱이 백그라운드에서 실행 중이고 사용자 상호 작용이 필요 없는 경우(예: 푸시 알림을 누르는 경우)에도 작동합니다. 그러나 앱이 실행되고 있지 않으면 적용되지 않습니다. 자세한 내용은 [Apple 개발자 설명서](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html)를 참조하십시오. |
| **[!UICONTROL Add mutable-content flag]** (iOS만 해당) | 푸시 페이로드에서 가변 콘텐츠 플래그를 전송하고 iOS SDK에서 제공하는 알림 서비스 애플리케이션 확장에 의해 푸시 알림 콘텐츠를 수정할 수 있도록 합니다. 자세한 내용은 [Apple 개발자 설명서](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/ModifyingNotifications.html)를 참조하십시오.<br/>그런 다음 모바일 앱 확장을 활용하여 에서 전송된 푸시 알림의 내용 또는 프레젠테이션을 추가로 수정할 수 있습니다.  [!DNL Journey Optimizer] 예를 들어 사용자는 이 옵션을 활용하여 데이터를 해독하고, 알림의 본문 또는 제목 텍스트를 변경하고, 알림에 스레드 식별자를 추가하는 등의 작업을 수행할 수 있습니다. |
| **[!UICONTROL Notification visibility]** (Android만 해당) | 푸시 알림의 가시성을 정의합니다. <br/><b></b> 개인 정보는 모든 잠금 화면에 알림을 표시하지만 보안 잠금 화면에 민감하거나 개인 정보를 숨깁니다. <br/><b></b> Publishers는 모든 잠금 화면에서 알림 전체를 표시합니다. <br/><b></b> Secretary는 보안 잠금 화면에 알림의 일부를 표시하지 않습니다. <br/>자세한 내용은  [Android 개발자 설명서](https://developer.android.com/reference/android/app/Notification)를 참조하십시오. |
| **[!UICONTROL Notification priority]** (Android만 해당) | 푸시 알림의 중요도를 낮음에서 최대값으로 정의합니다. 이를 통해 푸시 알림이 전달될 때 &quot;영향&quot;이 발생하는 방식을 결정합니다. 자세한 내용은 [Android 개발자 설명서](https://developer.android.com/guide/topics/ui/notifiers/notifications#importance) 를 참조하십시오 |
| **[!UICONTROL Delivery priority]** (Android만 해당) | 푸시 알림에 대해 높은 우선 순위 또는 일반적인 우선 순위를 설정합니다. 메시지 우선 순위에 대한 자세한 내용은 [Google 개발자 설명서](https://firebase.google.com/docs/cloud-messaging/concept-options#setting-the-priority-of-a-message)를 참조하십시오. |


**관련 항목**

<!--
* [Understand push notification flow](push-gs.md)
-->

* [푸시 채널 구성](push-gs.md)
* [새 메시지 만들기](create-message.md)
* [여정에 메시지 추가](building-journeys/journeys-message.md)

