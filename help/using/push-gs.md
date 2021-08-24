---
title: 푸시 구성 시작
description: 푸시 알림 데이터 흐름 및 구성 요소 이해
feature: 애플리케이션 설정, 푸시
role: Admin
level: Intermediate
source-git-commit: 1b11ff3848434a4cac1ca17318950481f20537c8
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 푸시 구성 시작 {#get-started-push}

푸시 알림은 모바일 앱 사용자에게 언제든지 연락할 수 있도록 해줍니다. 특히 앱을 사용하고 있지 않을 때 유용합니다. 푸시 알림은 서비스에 대한 업데이트 제공, 사용자에게 조치 요청, 사용자에게 새로운 거래를 알리는 등의 다양한 사용 사례를 달성하는 데 도움이 될 수 있습니다. 최종 사용자가 알림을 받거나 볼 수 있으려면 장치 플랫폼에는 옵트인이 필요합니다. 사용자 옵트인은 앱을 처음 설치한 후 또는 후속 세션 또는 워크플로우에서 적절하게 시작한 후 즉시 받을 수 있습니다. [!DNL Journey Optimizer] 은 푸시 알림을 지원하며 업계 선도적인 처리량 비율로 관련 알림을 전송하는 데 도움이 됩니다. 푸시 알림에는 Adobe Experience Cloud에서 보유한 데이터 통찰력을 활용하기 위해 개인화 및 여정 기반 컨텍스트가 포함될 수 있습니다.

이 페이지는 [!DNL Journey Optimizer]에서 푸시 알림과 관련된 주요 서비스 및 워크플로우를 설정하고 이해하는 데 도움이 됩니다.

[!DNL Adobe Journey Optimizer]에서 푸시 채널을 구성하는 단계는 [이 페이지](push-configuration.md)에 자세히 설명되어 있습니다.

## 푸시 알림 및 [!DNL Adobe Journey Optimizer]

다음 그림은 관련 데이터 흐름과 관련된 시스템 및 서비스를 보여줍니다. 이때 푸시 알림이 종단 간 서비스 관점에서 전달되는 방식을 강조 표시합니다.

![](assets/push-flow.png)

1. Apple의 APNs 및 Google FCM 푸시 메시지 서비스를 사용하여 브랜드 모바일 앱(Android 또는 iOS)의 등록
1. 메시징 서비스는 푸시 알림을 통해 특정 장치를 타깃팅하는 데 [!DNL Adobe Journey Optimizer]이 사용할 식별자인 푸시 토큰을 생성합니다.
1. 이전에 생성한 푸시 토큰은 Adobe Experience Platform에 전달되고 실시간 고객 프로필과 동기화됩니다. 이 작업은 클라이언트 SDK를 쉽게 통합할 수 있도록 OOTB로 수행됩니다
1. 푸시 메시지는 [!DNL Adobe Journey Optimizer]에서 작성되며, 푸시 메시지는 메시지 사전 설정에 대해 만들어집니다
1. 푸시 메시지는 여정의 오케스트레이션 캔버스에 포함될 수 있습니다
1. 여정 게시 시, 여정 조건을 기반으로 하는 고객 프로필은 푸시 알림을 받을 수 있는 자격이 있으며 푸시 메시지 페이로드는 이 단계에서 개인화됩니다
1. 개인화된 푸시 페이로드는 내부 푸시 메시지 게재 서비스로 전달됩니다
1. 그런 다음 이 내부 서비스는 메시지와 연결된 앱의 자격 증명을 확인하고
1. 최종 전달을 위해 Apple 및 Google 메시징 서비스로 메시지를 보냅니다
1. 메시지 서비스의 피드백이 기록되며, 여정 Live 및 글로벌 보고서에서 보고를 위해 오류 및 성공이 기록됩니다
1. 푸시 알림은 최종 사용자 장치에 전달됩니다
1. 최종 사용자 푸시 알림 상호 작용은 SDK 통합을 통해 최종 사용자 클라이언트에서 경험 이벤트로 전송됩니다

## 푸시 알림의 주요 서비스 역할

* **푸시 알림 서비스** 제공자는 원격 서버에서 모바일 앱으로 알림을 전달하는 핵심 구성 요소 웹 서비스입니다.

   [!DNL Adobe Journey Optimizer]  는 Android 및 iOS 플랫폼을 모두 지원하며 따라서 다음과 통합됩니다.
   * [Firebase Cloud Messaging(FCM)](https://firebase.google.com/docs/cloud-messaging)  - Android 모바일 앱으로 알림을 전송할 수 있습니다
   * [Apple APNs(푸시 알림 서비스)](https://developer.apple.com/library/archive/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/APNSOverview.html)  - iOS 모바일 앱으로 알림을 전송할 수 있습니다

* **Adobe Experience Platform Mobile** SDK는 Android 및 iOS 호환 SDK를 통해 모바일에 대한 클라이언트측 통합 API를 제공합니다. SDK는 푸시 메시지에 대한 다양한 API를 노출하는 [!DNL Adobe Journey Optimizer] 확장 프로그램을 제공하고 푸시 토큰 등록 또는 푸시 추적 이벤트 또는 기타 사용자 지정 경험 이벤트를 Adobe Experience Platform에 전송하는 것과 같은 데이터 흐름을 활성화합니다. 또한 SDK는 다른 Adobe Experience Cloud과 타사 파트너 기능을 사용할 수 있는 다양한 기타 확장도 제공합니다.

   SDK 통합에는 다음과 같은 Adobe Experience Platform [데이터 수집](https://experienceleague.adobe.com/docs/launch/using/home.html?lang=ko-KR){target=&quot;_blank&quot;} 서비스를 설정해야 합니다.

   * 데이터 스트림을 만들어 데이터가 Adobe Experience Platform으로 이동하는 프로필 및 경험 이벤트 데이터 세트를 구성합니다
   * 클라이언트측 모바일 속성 만들기 및 확장 추가 SDK는 이러한 확장과 긴밀하게 통합되어 완벽한 데이터 수집 환경을 제공합니다.
   * 모바일 앱 번들 식별자 및 앱 자격 증명을 등록

* **Adobe Experience Platform 실시간 고객 프로필**  은 웹, 모바일, CRM 및 서드파티 등 여러 채널의 데이터를 결합함으로써 각 개별 고객에 대한 전체적인 보기를 포함합니다. 프로필 을 사용하면 고객 데이터를 모든 고객 상호 작용을 실행 가능하고 타임스탬프가 지정된 계정을 제공하는 통합 보기에 통합할 수 있습니다. 주어진 앱 사용자에 대한 푸시 토큰은 사용자의 프로필에 대해 레코드 데이터로 저장되는 반면, 사용자가 푸시 알림과 함께 수행하는 상호 작용은 시계열 이벤트 데이터로 추적됩니다. [Adobe Experience Platform 실시간 고객 프로필](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html?lang=ko){target=&quot;_blank&quot;}에 대해 자세히 알아보십시오.

* **[!DNL Adobe Journey Optimizer]** : 위에 언급된 구성 요소와의 모바일 앱 통합이 준비되고 Adobe Experience Platform에 고객 프로필이 배치되면, 푸시 알림을 작성하여 사용자 [!DNL Adobe Journey Optimizer] 와 참여하도록 구성할 수 있습니다.

## 푸시 기술 설정 및 의사 워크플로우

다음 그림은 푸시 데이터 흐름의 골격을 형성하는 구성 요소 구성과 관련된 다양한 단계인 종단 간 방법을 보여줍니다. 작업 항목은 구성을 수행하는 역할 및 구성 중인 구성 요소에 따라 분류되었습니다.

![](assets/user-flow.png)
