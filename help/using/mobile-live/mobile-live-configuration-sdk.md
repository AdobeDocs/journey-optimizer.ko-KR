---
solution: Journey Optimizer
product: journey optimizer
title: 라이브 활동 채널 구성
description: Adobe Experience Platform Mobile SDK 통합을 구성하는 방법에 대해 알아봅니다
feature: Channel Configuration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: ce6bfca78d097588b5958c10c721b29b7013b3e2
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---


# Adobe Experience Platform Mobile SDK과 라이브 활동 통합 {#mobile-live-config-sdk}

>[!BEGINSHADEBOX]

* [라이브 활동 시작](get-started-mobile-live.md)
* [라이브 활동 구성](mobile-live-configuration.md)
* **[Adobe Experience Platform Mobile SDK과 라이브 활동 통합](mobile-live-configuration-sdk.md)**
* [라이브 활동 만들기](create-mobile-live.md)
* [자주 묻는 질문](mobile-live-faq.md)
* [라이브 활동 캠페인 보고서](../reports/campaign-global-report-cja-activity.md)


>[!ENDSHADEBOX]

Adobe Experience Platform Mobile SDK은 Apple의 라이브 활동에 대한 내장된 지원을 제공합니다. 이렇게 하면 앱을 열지 않고도 앱이 Lock Screen 및 Dynamic Island에서 직접 실시간 동적 업데이트를 표시할 수 있습니다.

1. [필수 모듈 가져오기](#import)

   **[!DNL AEPMessaging]**, **[!DNL AEPMessagingLiveActivity]**, **[!DNL ActivityKit]** 모듈을 가져옵니다.

1. [특성 정의](#attributes)

   `LiveActivityAttributes`을(를) 준수하고 `LiveActivityData` 및 `ContentState` 특성을 포함합니다.

1. [라이브 활동 등록](#register)

   SDK 초기화 후 `Messaging.registerLiveActivity()`을(를) 사용합니다.

1. [위젯 구성 만들기](#widget)

   잠금 화면과 동적 섬 인터페이스 모두에 대해 `ActivityConfiguration`을(를) 구현합니다.

1. [로컬에서 라이브 활동 시작(선택 사항)](#local)

   라이브 활동은 Journey Optimizer을 통해 원격으로 또는 애플리케이션 코드 내에서 로컬로 시작할 수 있습니다.

1. [디버그 지원 추가(선택 사항)](#debug)

   Assurance용 `LiveActivityAssuranceDebuggable`을(를) 구현합니다.

올바른 구성 및 호환성을 위해 다음 최소 버전이 설치되어 있는지 확인하십시오.

>[!BEGINSHADEBOX]

**필수 구성 요소:**

* **iOS:**
   * **iOS16.1 이상**: 기본 라이브 활동 기능
   * **iOS 17.2+**: Push-to-start 지원
   * **iOS 18+**: 브로드캐스트 채널 지원
* **Xcode:** 14.0 이상
* **Swift:** 5.7 이상
* **종속성:** AEPCore, AEPMessaging, AEPMessagingLiveActivity, ActivityKit

>[!ENDSHADEBOX]

## 1단계: 필요한 모듈 가져오기 {#import}

시작하려면 먼저 **[!DNL AEPMessaging]**, **[!DNL AEPMessagingLiveActivity]**, **[!DNL ActivityKit]** 모듈을 가져와야 합니다.

```swift
import AEPMessaging
import AEPMessagingLiveActivity
import ActivityKit
```

## 2단계: 라이브 활동 속성 정의 {#attributes}

`LiveActivityAttributes` 프로토콜을 준수하는 구조체를 만듭니다. 라이브 활동에 대한 정적 데이터 및 동적 콘텐츠 상태를 모두 정의합니다.

주요 구성 요소는 다음과 같습니다.

* Adobe Experience Platform 관련 데이터가 포함된 **`liveActivityData`**(필수).
   * 개별 사용자의 경우: `LiveActivityData(liveActivityID: "unique-id")` 사용
   * 브로드캐스트의 경우: `LiveActivityData(channelID: "channel-id")` 사용

* 정적 특성, 사용 사례와 관련된 사용자 지정 속성(예: `restaurantName`).

* **`ContentState`**: 실시간 활동 라이프사이클 중에 업데이트할 수 있는 동적 데이터를 정의합니다. `Codable` 및 `Hashable`을(를) 준수해야 합니다.

* `LiveActivityOrigin` 열거형은 활동이 앱 내에서 로컬로 시작되었는지 또는 iOS 17.2 이상에서 지원되는 Push-to-Start 알림을 통해 원격으로 시작되었는지를 지정합니다. 이 값을 통해 SDK은 데이터 수집 중에 로컬에서 시작된 라이브 활동과 원격으로 트리거된 라이브 활동을 구분할 수 있습니다.

**예**

```swift
@available(iOS 16.1, *)
struct FoodDeliveryLiveActivityAttributes: LiveActivityAttributes {
    // Mandatory: AEP Integration Data
    var liveActivityData: LiveActivityData
    
    // Static Attributes: Custom properties that do not change
    var restaurantName: String
    
    // Dynamic Content State: Data that can be updated
    struct ContentState: Codable, Hashable {
        var orderStatus: String
    }
}
```

```swift
@available(iOS 16.1, *)
public struct LiveActivityData: Codable {
    /// Unique identifier for broadcast Live activity channels
    public let channelID: String?
     
    /// Unique identifier for individual Live activities
    public let liveActivityID: String?
     
    /// Indicates local vs remote creation
    public let origin: LiveActivityOrigin?
     
    // Initializers
    public init(channelID: String)        // For broadcast Live activities
    public init(liveActivityID: String)   // For individual Live activities
}
```

앱에 대해 여러 라이브 활동 유형을 등록할 수도 있습니다.

```swift
if #available(iOS 16.1, *) {
    Messaging.registerLiveActivity(AirplaneTrackingAttributes.self)
    Messaging.registerLiveActivity(FoodDeliveryLiveActivityAttributes.self)
    Messaging.registerLiveActivity(GameScoreLiveActivityAttributes.self)
}
```

## 3단계: 라이브 활동 등록 {#register}

SDK 초기화 후 `AppDelegate`에 라이브 활동 유형을 등록하면 다음과 같은 작업을 수행할 수 있습니다.

* 자동 Push-to-Start 토큰 컬렉션 사용(iOS 17.2+)
* 라이브 활동 업데이트 토큰 자동 수집
* 라이프사이클 관리 및 이벤트 추적 활성화

**음식 배달 라이브 활동의 예:**

```swift
if #available(iOS 16.1, *) {
    Messaging.registerLiveActivity(FoodDeliveryLiveActivityAttributes.self)
}
```

## 4단계: 라이브 활동 위젯 만들기 {#widgets}

라이브 활동은 위젯을 통해 표시되므로 위젯 번들과 구성을 만들어야 합니다.

**음식 배달 라이브 활동의 예:**

```swift
@main
struct FoodDeliveryWidgetBundle: WidgetBundle {
    var body: some Widget {
        FoodDeliveryLiveActivityWidget()
    }
}

@available(iOS 16.1, *)
struct FoodDeliveryLiveActivityWidget: Widget {
    var body: some WidgetConfiguration {
        ActivityConfiguration(for: FoodDeliveryLiveActivityAttributes.self) { context in
            // Lock Screen UI
            VStack {
                Text("Order from \(context.attributes.restaurantName)")
                Text("Status: \(context.state.orderStatus)") // possible status may include "Ordered", "Order accepted", "Preparing", "On the Way","Delivered"
            }
        } dynamicIsland: { context in
            // Dynamic Island UI
            DynamicIsland {
                // Expanded UI
            } compactLeading: {
                // Compact leading UI
            } compactTrailing: {
                // Compact trailing UI
            } minimal: {
                // Minimal UI
            }
        }
    }
}
```

## 5단계: 로컬에서 라이브 활동 시작(선택 사항) {#local}

Journey Optimizer은 라이브 활동을 원격으로 시작할 수 있지만 로컬로 시작할 수도 있습니다.

**음식 배달 라이브 활동의 예:**

```swift
let attributes = FoodDeliveryLiveActivityAttributes(
    liveActivityData: LiveActivityData(liveActivityID: "order123"),
    restaurantName: "Pizza Palace"
)

let contentState = FoodDeliveryLiveActivityAttributes.ContentState(
    orderStatus: "Ordered"
)

let activity = try Activity<FoodDeliveryLiveActivityAttributes>.request(
    attributes: attributes,
    contentState: contentState,
    pushType: .token
)
```

## 6단계: 디버그 지원 추가(선택 사항) {#debug}

필요한 경우 Adobe Assurance에서 라이브 활동 스키마를 디버깅할 수 있습니다.

**음식 배달 라이브 활동의 예:**

```swift
@available(iOS 16.1, *)
extension FoodDeliveryLiveActivityAttributes: LiveActivityAssuranceDebuggable {
    static func getDebugInfo() -> (attributes: FoodDeliveryLiveActivityAttributes, state: ContentState) {
        return (
            FoodDeliveryLiveActivityAttributes(
                liveActivityData: LiveActivityData(liveActivityID: "debug-order-123"),
                restaurantName: "Debug Restaurant"
            ),
            ContentState(orderStatus: "Ordered")
        )
    }
}
```


