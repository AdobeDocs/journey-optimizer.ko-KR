---
title: 받은 편지함 만들기
description: Adobe Journey Optimizer의 받은 편지함 기능을 사용하여 사용자에게 지속적이고 방해받지 않는 메시지를 전달합니다.
feature: Content Cards
topic: Content Management
role: User
level: Beginner
exl-id: 60190d0b-d8e7-4a78-9924-d948f2769f6c
source-git-commit: c2bb6cf702a14b4eef8f2209082e39cd73338378
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 92%

---

# 받은 편지함 시작 {#inbox-gs}

>[!BEGINSHADEBOX]

**이 페이지에서:** 받은 편지함 채널이 앱 또는 웹 사이트 내에서 마케팅 메시지를 영구적인 한 위치에 보관하여 사용자가 편한 시간에 다시 읽고 작업할 수 있도록 하는 방법을 이해합니다.

>[!ENDSHADEBOX]

받은 편지함은 모바일 앱 또는 웹 사이트 내 한 곳에서 지속적이고 간편한 메시지를 제공합니다. 인앱 메시지와 푸시 알림은 스와이프 또는 탭 후 사라질 수 있지만, 받은 편지함은 사용자가 원하는 시간에 메시지를 열고 조치를 취할 수 있도록 메시지를 항상 표시합니다.

받은 편지함은 콘텐츠 카드 채널을 기반으로 다음과 같은 기능을 추가합니다.

* **지속적인 메시징**: 콘텐츠는 사용자가 제거하거나 만료될 때까지 받은 편지함에 남아 있으므로, 알림을 닫거나 앱을 종료한 후에도 다시 확인할 수 있습니다.
* **중앙 집중식 위치**: 앱 또는 웹 사이트 내 단일 사서함에서 관련 마케팅 메시지를 관리할 수 있습니다.
* **유연한 구현**: 기본 제공되는 받은 편지함 컨테이너를 사용하거나 자체 UI로 환경을 맞춤 설정할 수 있습니다.
* **읽음 상태**: 메시지를 열어본 장치에서 읽음 또는 읽지 않음으로 표시할 수 있습니다.

## 빠른 시작 안내서

다음 단계에 따라 받은 편지함을 구성하고 사용하십시오.

1. [Adobe Journey Optimizer 구성](inbox-configuration.md)

   **채널 구성** 아래에 **받은 편지함** 채널 구성을 추가하여 Journey Optimizer가 받은 편지함이 실행되는 위치와 방식(웹 페이지 또는 규칙, 모바일 앱 화면)을 알 수 있도록 합니다.

1. [Journey Optimizer에서 받은 편지함 만들기](inbox-create.md)

   **콘텐츠 카드** 액션을 사용하는 캠페인을 만들고 게재 위치로 **받은 편지함**&#x200B;을 선택합니다. UI에서 예약하거나 API를 통해 트리거할 수 있습니다.

1. [받은 편지함 디자인](inbox-design.md)

   받은 편지함 템플릿과 목록 또는 확장 레이아웃을 선택하여 메시지가 브랜드 및 UX에 맞도록 합니다.

1. [콘텐츠 카드를 만들고 받은 편지함에 연결](../content-card/create-content-card.md)

   디자이너에서 카드 내용을 작성하고, 받은 편지함 관련 옵션을 완료한 후 캠페인을 활성화하여 메시지가 받은 편지함에 도달하도록 합니다.

## 추가 리소스

* [받은 편지함 UI(iOS)](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/iOS): Adobe Experience Platform Mobile SDK를 사용하여 iOS 앱에 Journey Optimizer 받은 편지함을 구현하기 위한 요구 사항, 공개 API 인터페이스, 받은 편지함 설정 및 튜토리얼 링크(iOS 15 이상, Xcode 15 이상, Swift 5.1 이상)입니다.

* [받은 편지함 가져오기 및 표시](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/Android/tutorial/displaying-inbox): Journey Optimizer 받은 편지함 메시지를 로드하고 Android에서 받은 편지함 UI를 렌더링합니다(Adobe 개발자 설명서).

* [받은 편지함 사용자 정의](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/Android/tutorial/customizing-inbox): Android 앱의 받은 편지함 레이아웃, 스타일 및 상호 작용 동작을 조정합니다(Adobe 개발자 설명서).

* [받은 편지함 이벤트 수신](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/Android/tutorial/listening-inbox-events): Android에서 사용자 액션 및 수명 주기 업데이트에 대한 받은 편지함 콜백을 구독합니다(Adobe 개발자 설명서).
