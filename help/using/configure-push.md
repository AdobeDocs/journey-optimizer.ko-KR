---
title: 푸시 알림 구성
description: Journey Optimizer에서 푸시 알림을 만드는 방법 학습
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '934'
ht-degree: 13%

---

# 푸시 알림 {#create-push-notification} 구성

![](assets/do-not-localize/badge.png)

푸시 알림은 메시지를 만들 때 **[!UICONTROL Push Notification]** 탭에서 구성됩니다( [메시지 만들기](create-message.md) 참조).

전용 탭을 사용하여 iOS 또는 Android 운영 체제에 대한 푸시 알림 콘텐츠를 구성할 수 있습니다.

![](assets/create-content-push.png)

## 제목 및 본문

메시지를 작성하려면 **[!UICONTROL Title]** 및 **[!UICONTROL Body]** 필드를 클릭합니다. 표현식 편집기를 사용하여 컨텐츠 및 개인화 데이터를 정의합니다.

[이 섹션](personalization/personalize.md)에서 개인화에 대한 자세한 내용

중앙 섹션을 사용하여 iOS 및 Android 터미널에서 푸시 알림이 표시되는 방식을 시각화할 수 있습니다.

>[!NOTE]
>
>**[!UICONTROL Compose Message]** 섹션은 **[!UICONTROL iOS]** 및 **[!UICONTROL Android]** 탭 모두에 공통입니다. 이 섹션의 변경 사항은 두 운영 체제 모두에 적용됩니다.

## 클릭 동작 {#on-click-behavior}

수신자가 푸시 알림의 본문을 클릭할 때의 동작을 선택합니다.

* **[!UICONTROL Open app]** 옵션을 사용하여 **[!UICONTROL Preset]** 메시지와 연결된 응용 프로그램을 엽니다.
* 수신자를 응용 프로그램 내에 있는 특정 콘텐트로 리디렉션하려면 **[!UICONTROL Deeplink]** 옵션을 사용합니다. 관련 필드에 기본값을 입력합니다.
* 수신자를 외부 URL로 리디렉션하려면 **[!UICONTROL Web URL]** 옵션을 사용합니다. 관련 필드에 URL을 입력합니다.

## 자동 알림 보내기

자동 푸시 알림(또는 백그라운드 알림)은 응용 프로그램에 전달되는 숨겨진 명령입니다. 이 변수는 예를 들어 애플리케이션에 새로운 컨텐츠의 사용 가능성을 알리거나 백그라운드에서 다운로드를 시작하는 데 사용됩니다.

**[!UICONTROL Silent Notification]** 옵션을 선택하여 응용 프로그램에 자동으로 알립니다.이 경우 알림이 응용 프로그램으로 직접 전송됩니다. 장치 화면에 경고가 표시되지 않습니다.

**[!UICONTROL Custom data]** 섹션을 사용하여 키/값 쌍을 추가합니다.

## 고급 옵션

**[!UICONTROL Advanced options]**&#x200B;을 구성합니다. 사용 가능한 매개 변수는 다음과 같습니다.

| 매개 변수 | 사용 가능 | 설명 |
|---------|----------|---------|
| **[!UICONTROL Collapsible]** | iOS / Android | 축소 가능한 메시지는 새 메시지로 바꿀 수 있는 메시지입니다. 예를 들어 주제에 대한 최신 뉴스로 사용자를 업데이트하는 애플리케이션입니다. 이 경우 가장 최근의 메시지만 관련이 있습니다. 반면, 축소 가능한 메시지가 없는 경우 클라이언트 앱에 중요한 메시지를 모두 전달해야 합니다. |
| **[!UICONTROL Custom sound]** | iOS / Android | 알림을 받을 때 모바일 터미널에서 재생할 사운드입니다. 사운드를 앱에 번들로 묶어야 합니다. |
| **[!UICONTROL Badges]** | iOS / Android | 배지는 애플리케이션 아이콘에 읽지 않은 새로운 정보의 수를 직접 표시하는 데 사용됩니다. <br/>사용자가 애플리케이션에서 새 콘텐츠를 열거나 읽으면 배지 값이 사라집니다. 디바이스에서 알림을 받으면 관련 앱에 대한 배지 값을 새로 고침하거나 추가할 수 있습니다.<br/>예를 들어 고객의 읽지 않은 아티클 수를 저장하는 경우 개인화를 활용하여 각 고객에 대해 고유한 읽지 않은 아티클 배지 값을 보낼 수 있습니다. 자세한 개인화는 [이 섹션](personalization/personalize.md)을 참조하십시오. |
| **[!UICONTROL Notification group]** / | iOS | 알림 그룹을 푸시 알림에 연결합니다.<br/>iOS 12부터 알림 그룹을 사용하면 메시지 스레드와 알림 항목을 스레드 ID에 통합할 수 있습니다. 예를 들어, 한 브랜드는 하나 이상의 다른 ID 아래에 더 많은 운영 유형 알림을 유지하면서 하나의 그룹 ID 아래에 마케팅 알림을 보낼 수 있습니다.<br/>이를 설명하기 위해 groupID를 사용할 수 있습니다.123 &quot;스웨터의 새로운 봄 컬렉션 확인&quot; 및 groupID:456 &quot;패키지가 배달되었습니다&quot; 알림 그룹. 이 예에서 모든 배달 알림은 그룹 ID 아래에 번들로 제공됩니다.456. |
| **[!UICONTROL Notification channel]** | Android | 알림 채널을 푸시 알림에 연결합니다.<br/>Android 8.0(API 레벨 26)에서 표시하기 위해 모든 알림을 채널에 할당해야 합니다. 자세한 내용은 [Android 개발자 설명서](https://developer.android.com/guide/topics/ui/notifiers/notifications#ManageChannels)를 참조하십시오. |
| **[!UICONTROL Add content-availability flag]** | iOS | 푸시 알림을 수신하자마자 앱이 깨워지도록 푸시 페이로드의 사용 가능한 플래그를 보내 앱이 페이로드 데이터에 액세스할 수 있도록 합니다.<br/> 이는 앱이 백그라운드에서 실행되며 사용자 상호 작용(예: 푸시 알림 탭)이 없어도 작동합니다. 그러나 앱이 실행되고 있지 않은 경우에는 적용되지 않습니다. 자세한 내용은 [Apple 개발자 설명서](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html)를 참조하십시오. |
| **[!UICONTROL Add mutable-content flag]** | iOS | 푸시 페이로드에서 mutable-content 플래그를 전송하고 iOS SDK에서 제공하는 알림 서비스 애플리케이션 확장 기능을 통해 푸시 알림 콘텐츠를 수정할 수 있습니다. 자세한 내용은 [Apple 개발자 설명서](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/ModifyingNotifications.html)를 참조하십시오.<br/>그런 다음 모바일 앱 확장 기능을 사용하여 전송한 푸시 알림의 내용 또는 프레젠테이션을 추가로 수정할 수 있습니다.  [!DNL Journey Optimizer] 예를 들어 사용자는 이 옵션을 사용하여 데이터를 해독하고 알림의 본문 또는 제목 텍스트를 변경하고 알림 메시지에 스레드 식별자를 추가할 수 있습니다. |
| **[!UICONTROL Notification visibility]** | Android | 푸시 알림의 가시성을 정의합니다. <b>개인 정보</b> 는 모든 잠금 화면에서 알림을 표시하지만 보안 잠금 화면 상의 중요 또는 개인 정보를 숨깁니다. <b>발행자</b> 는 모든 폐쇄형 화면에 알림 전체를 표시합니다. <b>보안</b> 은 알림 일부를 보안 잠금 화면에 표시하지 않습니다. 자세한 내용은 [Android 개발자 설명서](https://developer.android.com/reference/android/app/Notification)를 참조하십시오. |
| **[!UICONTROL Notification priority]** | Android | 푸시 알림의 중요도를 낮음에서 최대순으로 정의합니다. 푸시 알림이 배달될 때 &quot;중단&quot; 방식을 결정합니다. 자세한 내용은 [Android 개발자 설명서](https://developer.android.com/guide/topics/ui/notifiers/notifications#importance)를 참조하십시오. |
| **[!UICONTROL Delivery priority]** | Android | 푸시 알림에 대한 높은 우선 순위 또는 일반적인 우선 순위를 설정합니다. 메시지 우선 순위에 대한 자세한 내용은 [Google 개발자 설명서](https://firebase.google.com/docs/cloud-messaging/concept-options#setting-the-priority-of-a-message)를 참조하십시오. |

## 사용자 지정 데이터

**[!UICONTROL Custom data]** 섹션에서 모바일 애플리케이션 구성에 따라 사용자 지정 변수를 페이로드에 추가할 수 있습니다. Adobe Experience Platform 및 Adobe 론치에서 푸시 알림을 설정하는 방법에 대한 자세한 내용은 [이 섹션](push-configuration.md)을 참조하십시오.

