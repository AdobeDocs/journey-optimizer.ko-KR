---
title: 받은 편지함 만들기
description: Adobe Journey Optimizer의 받은 편지함을 시작하여 지속적이고 방해받지 않는 메시지를 사용자에게 전달합니다.
feature: Content Cards
topic: Content Management
role: User
level: Beginner
exl-id: 60190d0b-d8e7-4a78-9924-d948f2769f6c
source-git-commit: f7f303685e954614b44a9b62368460e9b07b26b3
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 1%

---

# 받은 편지함 시작 {#inbox-gs}

받은 편지함은 모바일 앱 또는 웹 사이트 내에서 한 곳에서 지속적이고 마찰이 적은 메시지를 제공합니다. 스와이프 또는 탭 후 인앱 및 푸시가 사라질 수 있습니다. 받은 편지함은 메시지를 사용할 수 있도록 유지하여 사람들이 자신에게 맞는 메시지를 열고, 읽고, 작업할 수 있습니다.

받은 편지함은 콘텐츠 카드 채널을 기반으로 빌드되고 다음을 추가합니다.

* **영구 메시징**: 콘텐츠가 제거되거나 만료될 때까지 받은 편지함에 남아 있으므로 사용자는 알림을 닫거나 앱을 나간 후 받은 편지함으로 돌아갈 수 있습니다.
* **중앙 위치**: 관련 마케팅 메시지를 위한 앱 또는 사이트의 단일 사서함.
* **유연한 구현**: 준비된 받은 편지함 컨테이너를 사용하거나 사용자 UI에서 환경을 사용자 지정합니다.
* **읽기 상태**: 메시지를 연 장치에서 읽음 또는 읽지 않음으로 표시할 수 있습니다.

## 빠른 시작 안내서

받은 편지함을 구성하고 사용하려면 다음 단계를 따르십시오.

1. [Adobe Journey Optimizer 구성](inbox-configuration.md)

   **채널 구성**&#x200B;에 **받은 편지함** 채널 구성을 추가하여 Journey Optimizer에서 받은 편지함이 실행되는 위치와 방법(웹 페이지 또는 규칙, 또는 모바일 앱 표면)을 알 수 있도록 합니다.

1. [Journey Optimizer에서 받은 편지함 만들기](inbox-create.md)

   **콘텐츠 카드** 작업을 사용하는 캠페인을 만들고 **받은 편지함**&#x200B;을(를) 배달 위치로 선택합니다(UI에서 예약되거나 API에 의해 트리거됨).

1. [받은 편지함 디자인](inbox-design.md)

   받은 편지함 템플릿을 선택하고 메시지가 브랜드와 UX에 맞게 목록 또는 확장된 레이아웃을 선택하십시오.

1. [콘텐츠 카드를 만들고 받은 편지함에 연결](../content-card/create-content-card.md)

   디자이너에서 카드 콘텐츠를 작성하고 받은 편지함별 옵션을 완료한 다음 메시지가 받은 편지함에 도달하도록 캠페인을 활성화합니다.

## 추가 리소스

* [받은 편지함 UI(iOS)](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/iOS/): 요구 사항, 공개 API 표면, 받은 편지함 설정 및 Adobe Experience Platform Mobile SDK을 사용하여 iOS 앱에서 Journey Optimizer 받은 편지함을 구현하기 위한 자습서에 대한 링크(iOS 15 이상, Xcode 15 이상, Swift 5.1 이상).

* [받은 편지함 가져오기 및 표시](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/Android/tutorial/displaying-inbox/): Journey Optimizer 받은 편지함 메시지를 로드하고 Android에서 받은 편지함 UI를 렌더링합니다(Adobe Developer 설명서).

* [받은 편지함 사용자 지정](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/Android/tutorial/customizing-inbox/): Android 앱에 대한 받은 편지함 레이아웃, 스타일 및 상호 작용 동작을 조정합니다(Adobe Developer 설명서).

* [받은 편지함 이벤트 수신](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/Android/tutorial/listening-inbox-events/): Android에서 사용자 작업 및 라이프사이클 업데이트에 대한 받은 편지함 콜백을 구독합니다(Adobe Developer 설명서).
