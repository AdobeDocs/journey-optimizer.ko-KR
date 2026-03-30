---
solution: Journey Optimizer
product: journey optimizer
title: 라이브 활동 문제 해결
description: 프로필 토큰 문제, 캠페인 구성 및 게재 실패를 포함하여 단일 및 브로드캐스트 사용 사례에 대한 Journey Optimizer의 라이브 활동 문제를 해결하는 방법에 대해 알아봅니다
role: User
level: Intermediate
exl-id: f0f83bd2-7c2b-4d9b-b455-e1df12dfa175
source-git-commit: 016d905840a3ccc05ca1d2a934130b53c1108e7c
workflow-type: tm+mt
source-wordcount: '4503'
ht-degree: 1%

---

# 라이브 활동 문제 해결 {#troubleshoot-mobile-live}

Adobe Journey Optimizer의 라이브 활동을 통해 iOS 잠금 화면 및 Dynamic Islands에서 실시간으로 동적 업데이트를 수행할 수 있습니다. API 트리거 캠페인을 통해서만 트리거하고 관리할 수 있습니다.

**사용 사례 유형:**

* **단일**: 개별 대상, 트랜잭션(API 트리거 트랜잭션 캠페인)
* **Broadcast**: 대상자 타겟팅, 대량 게재(API 트리거된 마케팅 캠페인)

라이브 활동을 트리거하거나 업데이트하기 위한 API 호출이 **성공 응답(200 OK)**&#x200B;을 반환하지만 라이브 활동이 사용자의 장치에 나타나거나 업데이트되지 않는 경우 라이브 활동에 대한 문제가 자주 발생합니다. API 확인과 실제 장치 동작 간의 이러한 연결 해제는 배달 파이프라인의 여러 지점에서 발생할 수 있습니다. 이 안내서에서는 API 요청 유효성 검사에서 장치 렌더링을 통해 각 단계를 검사하여 게재 실패 위치를 식별하는 체계적인 문제 해결 방법을 제공합니다.

## 전제 조건

문제 해결 전에 다음을 확인하십시오.

* 
  +++ Assurance 세션 설정

  **Assurance 세션**&#x200B;을 설정하여 SDK 이벤트를 캡처하고 게재 파이프라인을 검사합니다. Assurance은 다음에 대한 가시성을 제공합니다.

   * Edge Network 요청 및 응답
   * 프로필 자격 이벤트
   * 푸시 토큰 등록
   * 라이브 활동 라이프사이클 이벤트

  [Assurance 설명서](https://experienceleague.adobe.com/ko/docs/platform-learn/implement-mobile-sdk/app-implementation/assurance)에서 Adobe Experience Platform Assurance을 설정하는 방법을 알아보세요.

  **참고**: iOS Live 활동의 경우 앱이 실제 iOS 장치(iOS 16.1 이상) 또는 Xcode 시뮬레이터(iOS 16.1 이상)에서 실행되고 있는지 확인하십시오.

  +++

* 
  +++ API 트리거된 캠페인 세부 정보 수집

  Journey Optimizer에서 API 트리거 캠페인으로 이동하여 다음을 검색하십시오.

   * 캠페인 이름
   * URL 또는 캠페인 속성에 있는 캠페인 ID
   * 해당되는 경우 Campaign 버전
   * 라이브 활동에 사용되는 표면 구성, iOS 앱 표면

  +++

* 
  +++ API 요청 정보 수집

  라이브 활동을 트리거하기 위해 API를 호출할 때 다음을 저장합니다.

   * 프로필 식별자 및 라이브 활동 데이터를 포함하는 API 요청 페이로드
   * 상태 코드, 메시지 ID, 요청 ID를 포함한 API 응답
   * API가 호출된 시간의 타임스탬프
   * 사용된 끝점(예: `/campaign/{CAMPAIGN_ID}/execute`)

  +++

* 
  +++ 테스트 프로필 식별

  API 요청에서 다음을 검색합니다.

   * 프로필 네임스페이스(예: ECID, 이메일, 고객 ID)
   * API 호출에 사용된 프로필 ID

  Adobe Experience Platform에서 이 프로필을 조회할 수 있는지 확인합니다. [Experience Platform 설명서에서 프로필을 찾는 방법](https://experienceleague.adobe.com/en/docs/experience-platform/profile/ui/user-guide.html)을 알아보세요.

  +++

* 
  +++ 장치 및 앱 정보

  테스트 장치에서 다음 정보를 수집합니다.

   * 장치 모델(예: iPhone 14 Pro)
   * iOS 버전
   * 앱 번들 식별자
   * APNs 푸시 토큰
   * 테스트 시 네트워크 연결 상태

  +++

## 일반적인 시나리오

### 프로필 또는 푸시 토큰 문제 {#profile-issue}

[!BADGE 단일 및 브로드캐스트 사용 사례에 모두 적용]{type=Positive}

API는 HTTP 200을 반환하지만 라이브 활동이 표시되지 않습니다. 일반적인 원인:

* Adobe Experience Platform에 프로필이 없습니다.
* 라이브 활동 푸시 토큰이 프로필에 동기화되지 않았습니다.
* 라이브 활동 푸시 세부 정보가 동기화되었지만 잘못된 구성(예: `appId` 또는 `attributeType`)이 포함되어 있습니다.

**브로드캐스트 사용 사례에 대한 참고 사항**: 대상의 일부 프로필에 토큰이 없는 경우 해당 프로필만 라이브 활동을 수신할 수 없습니다. 대상의 여러 프로필을 샘플링하여 토큰 문제를 진단합니다. 이 설정은 업데이트 또는 종료 이벤트가 아닌 원격 시작 이벤트에만 적용됩니다.

#### 사전 확인

* iOS 앱 요구 사항:
   * iOS 16.1+
   * `NSSupportsLiveActivities`에서 `YES`을(를) `Info.plist`(으)로 설정
   * `ActivityAttributes`이(가) 올바르게 구현되었습니다.
* 모바일 SDK 통합:
   * Adobe Experience Platform Mobile SDK (메시징 SDK 5.11.0+)
   * `Messaging.registerLiveActivities`이(가) 라이브 활동 푸시 토큰을 사용하여 구현되고 호출되었습니다.

#### 디버깅 단계

1. 
   +++ Adobe Experience Platform에 프로필이 있는지 확인

   1. Journey Optimizer에서 **고객** `>` **프로필**(으)로 이동합니다.
   1. API 요청에서 네임스페이스 및 ID 값을 사용하여 검색합니다.
   1. 프로필을 찾을 수 없으면 프로필이 존재하지 않거나 수집이 완료되지 않습니다. 라이브 활동을 트리거하기 전에 프로필을 만들거나 수집을 기다립니다.
   1. 프로필이 발견되면 아래 2단계로 진행하여 푸시 토큰이 동기화되었는지 확인합니다.

      +++

1. 
   +++ 라이브 활동 푸시 토큰이 동기화되었는지 확인

   Assurance을 사용하여 토큰 등록을 확인할 수 있습니다.

   1. Assurance의 **이벤트** 목록에서 이벤트 `eventType = "liveActivity.pushToStart"`을(를) 필터링하거나 검색합니다.
   1. **이벤트**&#x200B;를 선택하고 페이로드를 검사하십시오.
   1. 토큰, appId 및 attributeType 값이 있는지 확인합니다.
   1. 이벤트가 성공적으로 전송되었는지 확인합니다.

   Adobe Experience Platform 프로필에서도 확인할 수 있습니다.

   1. Adobe Experience Platform의 **프로필**&#x200B;에서 **이벤트** 탭에 액세스합니다.
   1. `liveActivity.pushToStart`개 이벤트를 검색합니다.
   1. 짝수 타임스탬프 및 페이로드를 확인합니다.

   이벤트를 찾을 수 없으면 모바일 앱에서 `Messaging.registerLiveActivity`을(를) 올바르게 호출하지 않습니다. SDK 통합을 수정해야 합니다.

   +++

1. 
   +++ 프로필의 토큰 세부 정보 확인

   1. **프로필**&#x200B;에서 **특성** 탭에 액세스합니다.
   1. `liveActivityPushNotificationDetails` 찾기.
   1. 토큰 구성 확인:

      ```json
      {
        "liveActivityPushNotificationDetails": [
          {
            "appId": "com.example.myapp",
            "token": "abc123def456...",
            "platform": "apns",
            "denylisted": false,
            "attributeType": "OrderTrackingAttributes",
            "identity": {}
          }
        ]
      }
      ```

   **각 필드 유효성 검사:**

   | 필드 | 요구 사항 | 일반적인 문제 |
   |-|-|-|
   | `appId` | iOS 번들 식별자와 정확히 일치해야 함 | 개발/프로덕션 번들 ID 간 불일치 |
   | `attributeType` | Swift `ActivityAttributes` 구조체 이름과 정확히 일치해야 합니다(대/소문자 구분). | 구조체 이름이 잘못되었거나 입력 |
   | `platform` | `"apns"` 또는 `"apnsSandbox"`이어야 합니다. | 잘못된 플랫폼 값 |
   | `denylisted` | `false`이어야 합니다. | 토큰이 유효하지 않거나 사용자가 옵트아웃한 것으로 표시됨 |
   | `token` | 유효한 APNs 푸시 토큰 | 토큰이 만료되거나 앱이 다시 설치됨 |

   잘못된 필드가 있는 경우: 모바일 앱을 업데이트하고 `Messaging.registerLiveActivities`을(를) 사용하여 다시 등록하고 5~10분 정도 기다린 다음 다시 확인하십시오.

   `liveActivityPushNotificationDetails`이(가) 누락된 경우: 토큰이 아직 동기화되지 않았습니다. Assurance에서 `liveActivity.pushToStart` 이벤트를 보고 5~10분 정도 기다립니다.

   +++

### 캠페인 구성 및 페이로드 문제 {#payload-issues}

[!BADGE 단일 및 브로드캐스트 사용 사례에 모두 적용]{type=Positive}

유효한 토큰이 있는 프로필이 있지만 라이브 활동이 나타나지 않습니다. 이 문제는 다음 원인으로 인해 발생할 수 있습니다.

* 표면 또는 채널 구성이 잘못되었습니다.
* 잘못된 API 페이로드 구조입니다.
* `content-state` 및 `attributes`이(가) iOS `ActivityAttributes` 구현과 일치하지 않습니다.
* 오래된 `timestamp`(업데이트/종료에 중요).

**브로드캐스트 사용 사례에 대한 참고 사항**: 캠페인은 **API로 트리거된 마케팅**(트랜잭션 아님)이어야 합니다. 페이로드에서 개별 `audience` 대신 `profile`을(를) 사용합니다. 브로드캐스트별 페이로드 구조는 [이 섹션](#broadcast-config)을 참조하고, 전체 API 사양은 [Adobe Developer 설명서](https://developer.adobe.com/journey-optimizer-apis/references/messaging#operation/postIMAudienceMessageExecution)를 참조하십시오.

#### 사전 확인

* Campaign은 **API 트리거 트랜잭션**(단일) 또는 **API 트리거 마케팅**(브로드캐스트)이며 **높은 처리량** 옵션은 **활성화되지 않음**&#x200B;이어야 합니다. 실시간 활동과 호환되지 않기 때문입니다.
* [위의 시나리오](#profile-issue)을(를) 사용하여 프로필이 있고 토큰이 올바르게 동기화되었는지 확인하십시오.

#### 디버깅 단계

1. 
   +++ 캠페인 표면 구성 확인

   1. Journey Optimizer에서 **Campaign**&#x200B;을(를) 열고 **작업** 메뉴로 이동합니다.
   1. **라이브 활동 구성**&#x200B;을 확인하세요. 프로필 `appId`의 `liveActivityPushNotificationDetails`과(와) 일치하는 번들 식별자로 iOS 앱에 대한 표면을 구성해야 합니다. 예를 들어 프로필에 `"appId": "com.example.myapp"`이(가) 있는 경우 표면이 동일한 앱을 대상으로 해야 합니다.
   1. 캠페인 구성의 **활동 유형**&#x200B;이(가) 프로필 `attributeType`의 `liveActivityPushNotificationDetails`과(와) 정확히 일치하는지 확인하십시오. 예를 들어 프로필에 `"attributeType": "FoodDeliveryLiveActivityAttributes"`이(가) 있는 경우 캠페인에서 이와 동일한 활동 유형을 지정해야 합니다.

      +++

1. 
   +++API 페이로드 구조 확인

   API를 통해 캠페인을 실행할 때 페이로드가 올바른 구조를 따르는지 확인하십시오.

   **단일 페이로드:**

   ```json
   {
     "campaignId": "your-campaign-id",
     "recipients": [{
       "type": "aep",
       "userId": "user@example.com",
       "namespace": "email",
       "context": {
         "requestPayload": {
           "aps": {
             "content-available": 1,
             "timestamp": 1756984054,
             "event": "start",
             "attributes-type": "FoodDeliveryLiveActivityAttributes",
             "content-state": { ... },
             "attributes": { ... }
           }
         }
       }
     }]
   }
   ```

   **일반적인 페이로드 문제:**

   | 필드 | 요구 사항 | 일반적인 문제 |
   |-|-|-|
   | `attributes-type` | 캠페인 활동 유형 및 프로필 `attributeType`과(와) 일치해야 합니다. | 불일치 또는 오타 |
   | `campaignId` | 활성화된 캠페인 ID와 일치해야 함 | 캠페인 ID가 잘못되었거나 누락 |
   | `content-available` | `1`이어야 합니다. | 누락되거나 잘못된 값 |
   | `event` | `"start"`, `"update"` 또는 `"end"`이어야 합니다. | 잘못된 이벤트 유형 |
   | `timestamp` | 항상 현재/최신 Unix Epoch 시간(초)이어야 함 | 이전/캐시된 타임스탬프 사용 |
   | `userId` / `namespace` | AEP의 기존 프로필과 일치해야 합니다. | 프로필 식별자 불일치 |

   **중요: 항상 최신 타임스탬프를 사용합니다**

   * 각 API 호출이 수행될 때 `timestamp` 필드는 **always**&#x200B;이(가) **현재 Unix Epoch 시간**(초)이어야 합니다.
   * 이는 **모든 이벤트 유형**: `start`, `update` 및 **특히`end`**&#x200B;에 적용됩니다.
   * **업데이트/종료 요청에 미치는 영향**: 오래된 타임스탬프를 사용하면 업데이트 및 종료 요청이 실패하거나 장치에서 무시됩니다.
   * **NOT**&#x200B;은(는) 이전 요청의 타임스탬프를 다시 사용하거나 캐시된 값을 사용하지 마십시오.
   * 모든 API 호출에 대해 새 타임스탬프를 생성합니다.

   **선택적 필드(모든 이벤트 유형):**

   * `requestId`: 추적에 대한 고유 식별자(권장).
   * `alert`: 알림에 대해 `title` 및 `body`이(가) 있는 개체(업데이트에 주의를 기울이는 데 유용함).

   **정보 `dismissal-date`:**

   * Unix epoch 시간(초)을 포함하는 선택적 필드입니다.
   * **관련성이`event: "end"`**&#x200B;에만 있습니다.
   * 라이브 활동을 장치에서 자동으로 제거해야 하는 시기를 지정합니다.
   * 종료 이벤트에 제공되지 않는 경우 사용자가 취소할 때까지 라이브 활동이 계속 표시됩니다.
   * 미래 타임스탬프여야 합니다(`timestamp` 이후).

     +++

1. 
   +++ 페이로드를 iOS 구현에 정렬

   API 페이로드가 iOS 앱의 `ActivityAttributes` 구현과 일치하는지 확인하십시오. Adobe SDK의 `LiveActivityAttributes` 프로토콜은 iOS `ActivityAttributes`을(를) 확장하며 `liveActivityData` 속성이 필요합니다.

   **매핑 유효성 검사:**

   1. `ActivityAttributes`에서 Adobe의 `LiveActivityAttributes` 프로토콜을 구현해야 합니다. 예:

      ```swift
      struct FoodDeliveryLiveActivityAttributes: LiveActivityAttributes {
       public struct ContentState: Codable, Hashable {
           var orderStatus: String
           var estimatedDeliveryTime: String
       }
      
       // Adobe SDK requirement
       var liveActivityData: LiveActivityData
      
       // Your custom attributes
       var restaurantName: String
      }
      ```

      **참고** `liveActivityData` 필드는 Adobe SDK에 필요하며 모든 구현에 포함되어야 합니다.

   1. API 페이로드는 iOS 구조를 미러링해야 합니다.

      ```json
      {
        "aps": {
           "event": "start",
           "timestamp": 1756984054,
           "attributes-type": "FoodDeliveryLiveActivityAttributes",
           "content-state": {
           "orderStatus": "Preparing",
           "estimatedDeliveryTime": "20 mins"
        },
        "attributes": {
          "liveActivityData": {
            "liveActivityID": "order-12345"
          },
          "restaurantName": "Pizza Palace"
        }
        }
      }
      ```

   **유효성 검사 목록:**

   * `ContentState`에 모든 `content-state` 필드를 포함합니다(모든 이벤트 유형에 필요).
   * 다음을 포함하여 `LiveActivityAttributes`의 모든 `attributes` 필드(시작 이벤트만 해당) 포함:
      * `liveActivityData`(필수, 일반적으로 `liveActivityID` 또는 유사한 식별자를 포함)
      * 구조의 모든 사용자 정의 필드
   * 필드 이름을 정확히 일치시키십시오(대/소문자 구분).
   * 데이터 유형(문자열, 정수, 부울, 중첩된 오브젝트)을 일치시킵니다.
   * 중첩된 오브젝트 구조를 유지합니다.

   **일반적인 실수:**

   | 문제 | 영향 | 변수 이름이 아니라, 필터링된 보고서의 머리글로 잘못 표시하는 |
   |-------|--------|-----|
   | 특성에 `liveActivityData`이(가) 없습니다. | 라이브 활동이 시작되지 않음 | 시작 이벤트에 항상 `liveActivityData` 개체 포함 |
   | 시작 이벤트에 필수 필드 누락 | 라이브 활동이 시작되지 않음 | iOS 구조의 모든 필드 추가 |
   | 잘못된 필드 이름(오타/사례) | 무시된 필드 또는 구문 분석 오류 | iOS 필드 이름과 정확히 일치 |
   | 잘못된 데이터 유형 | 구문 분석 오류 | iOS 데이터 유형 일치 |
   | 중첩된 오브젝트 누락 | 불완전한 데이터 | 중첩된 구조 모두 포함 |
   | 업데이트/종료에 `attributes` 포함 | 불필요하지만 일반적으로 무시됨 | 시작 이벤트에 `attributes`만 포함 |
   | 업데이트/종료 시 오래된 타임스탬프 | 장치에서 무시한 업데이트/종료 | 항상 새 타임스탬프 생성 |

   자세한 예제는 [라이브 활동 페이지 만들기](create-mobile-live.md)를 참조하세요.

   +++

1. 
   +++ Assurance으로 테스트

   Assurance을 사용하여 API 실행 및 페이로드 게재 확인:

   1. Assurance 세션을 엽니다.
   1. 라이브 활동을 트리거하기 위해 API 호출을 실행합니다.
   1. **이벤트 목록**&#x200B;에서 다음을 확인하십시오.
      * 캠페인 실행 이벤트.
      * 라이브 활동 전달 이벤트.
      * 페이로드 유효성 검사 오류 이벤트
   1. 이벤트 페이로드를 검토하여 다음을 확인합니다.
      * 페이로드가 올바르게 처리되었습니다.
      * 유효성 검사 오류가 발생하지 않았습니다.
      * 라이브 활동이 APNs로 전송되었습니다.

      +++

### 게재 실패 및 오류 분석

[!BADGE 단일 및 브로드캐스트 사용 사례에 모두 적용]{type=Positive}

이 시나리오에서는 모든 이전 검사를 통과했습니다.

* 프로필이 [유효한 라이브 활동 푸시 토큰](#profile-issue)에 있음
* 캠페인이 올바르게 [적절한 페이로드로 구성됨](#payload-issues)
* [업데이트 토큰이 동기화됨](#token-not-synced)(업데이트/종료 이벤트의 경우 단일 사용 사례만 해당)

하지만 라이브 활동은 여전히 예상대로 표시, 업데이트 또는 종료되지 않습니다. Adobe 전달 시스템 수준이나 푸시 알림 서비스 공급자(APNs)에서 문제가 발생할 수 있습니다.

**브로드캐스트 사용 사례에 대한 참고 사항**: 보고서에는 모든 대상 구성원에 대한 지표가 표시됩니다. 일부 프로필은 성공하지만 다른 프로필은 실패할 수 있습니다.

**사전 확인**

* **이전 시나리오 유효성 검사:**
   * 올바른 `liveActivityPushNotificationDetails`을(를) 가진 프로필이 있습니다.
   * 캠페인 표면 및 활동 유형이 올바름
   * API 페이로드가 현재 타임스탬프와 함께 유효합니다.
   * 업데이트 토큰이 동기화됨(업데이트/종료 이벤트의 경우)

* **API 호출 확인됨:**

   * API 호출이 HTTP 200(성공)을 반환했습니다.
   * 캠페인 ID 및 수신자 세부 정보가 올바릅니다

#### 디버깅 단계

1. 
   +++ 캠페인 보고서 확인

   1. **라이브 활동 캠페인**(으)로 이동합니다.
   1. **보고서** 단추를 클릭합니다.
   1. **모든 시간 보고서 보기**&#x200B;를 선택합니다.
   1. 다음 섹션을 검토하십시오.

      1. 게재 성공을 이해하려면 **전송 통계** 지표를 확인하십시오.

         | 지표 | 의미 | 찾을 내용 |
         |-|-|-|
         | 타기팅됨 | 대상자에 적합한 프로필 수 | 테스트 프로필을 포함해야 함 |
         | 전송 횟수 | 시도된 총 푸시 알림 수 | API 호출과 일치해야 함 |
         | 게재됨 | 장치에 정상적으로 전달됨 | 성공률을 보려면 전송과 비교 |
         | 오류 보내기 | 보내지 못한 푸시 알림 | 높은 숫자 |
         | 제외 보내기 | Adobe Journey Optimizer에 의해 제외된 프로필 | 프로필이 제외되었는지 확인 |

      1. Send errors > 0인 경우 **Error Reasons** 테이블에서 특정 오류 코드 및 메시지를 확인합니다.

         | 일반 오류 | 의미 | 해결 방법 |
         |-|-|-|
         | 잘못된 토큰 | 푸시 토큰이 잘못되었거나 만료됨 | 장치에서 라이브 활동 토큰 재등록 |
         | 토큰을 찾을 수 없음 | 프로필과 연결된 유효한 토큰 없음 | `liveActivityPushNotificationDetails`이(가) 있는지 확인 |
         | 거부된 APNs | Apple 푸시 알림 서비스가 푸시를 거부했습니다 | APNs 인증서, 번들 ID, 환경 확인 |
         | 네트워크 시간 제한 | APNs에 연결할 수 없음 | 일시적인 문제; API 호출 다시 시도 |

      1. **제외 보내기** > 0인 경우 **제외된 이유** 표를 확인하십시오.

         | 공통 제외 | 의미 | 해결 방법 |
         |-|-|-|
         | 프로필이 옵트아웃됨 | 사용자가 알림을 옵트아웃했습니다. | 프로필 동의 상태 확인 |
         | 토큰 차단 목록에 추가된 | 토큰이 잘못된 것으로 표시됨 | 토큰 재등록 또는 차단 목록 상태 확인 |
         | 프로필이 적격하지 않음 | 프로필이 캠페인 기준을 충족하지 않음 | 캠페인 대상자 규칙 검토 |

   [라이브 활동 보고서 페이지](../reports/campaign-global-report-cja-activity.md)에서 자세히 알아보세요.

   +++

1. 
   +++ 프로필에서 메시지 피드백 이벤트 확인

   1. Journey Optimizer의 **고객** > **프로필**(으)로 이동합니다.
   1. 프로필을 검색하여 엽니다.
   1. **이벤트** 탭을 선택합니다.
   1. `eventType = "message.feedback"`을(를) 사용하여 이벤트를 필터링하거나 검색합니다.
   1. 라이브 활동의 `liveActivityID` 및 `event` 유형과 일치하는 피드백 이벤트를 찾습니다.
   1. 다음 주요 필드를 검토하십시오.

      | 필드 | 가능한 값 | 의미 |
      |-|-|-|
      | `feedbackStatus` | `sent`, `error`, `denylist` | 서비스 공급자의 게재 결과 |
      | `serviceProvider` | `apns/apnsSandbox` | iOS Live 활동용 APNs여야 함 |
      | `errorCode` | 숫자 코드 또는 `null` | 실패한 경우 APNs 관련 오류 코드 |
      | `errorMessage` | 오류 설명 또는 `null` | 사람이 읽을 수 있는 오류 메시지 |

   1. **경우 `feedbackStatus: "error"`:**
      * `errorCode` 및 `errorMessage`에서 특정 APNs 오류를 확인합니다.
      * 일반적인 APNs 오류에는 만료된 토큰, 잘못된 인증서, 잘못된 번들 ID가 포함됩니다.

   1. **피드백 이벤트가 없는 경우:**
      * 푸시 알림이 시도되지 않았을 수 있습니다.
      * 위의 1단계에서 자세히 설명한 대로 프로필이 캠페인 보고서에 제외되었는지 확인합니다.

      +++

1. 
   +++ Assurance에서 APNs에 라이브 활동 전달 확인

   1. Assurance 세션을 엽니다. API 호출 중에 활성화되어 있어야 합니다.
   1. API 호출 실행(시작, 업데이트 또는 종료).
   1. **이벤트 목록**&#x200B;에서 라이브 활동 전달 이벤트를 찾습니다.
   1. APNs 푸시 게재와 관련된 이벤트를 검색합니다.
   1. 다음 지표를 확인하십시오.
      * **APNs에 대한 푸시 요청**: Adobe이 Apple 서버로 푸시를 보냈는지 확인합니다.
      * **APNs 응답**: APNs가 푸시를 수락했는지 또는 거부했는지 여부를 표시합니다.
      * **게재 상태**: 성공 또는 실패 표시
   1. 문제가 발견되면 다음의 일반적인 APNs 전달 문제를 참조하십시오.

      | 문제 | Assurance의 증상 | 해결 방법 |
      |-|-|-|
      | APNs 인증서 만료됨 | 인증 오류 | 새 APNs 인증서 갱신 및 업로드 |
      | 잘못된 환경(개발 및 프로덕션) | 토큰 불일치 오류 | 인증서가 앱 빌드 유형과 일치하는지 확인 |
      | 번들 ID 불일치 | 잘못된 번들 식별자 | 인증서 번들 ID가 앱과 일치하는지 확인 |
      | 토큰 만료됨 | APNs에서 잘못된 토큰 오류 | 라이브 활동 토큰 재등록 |
      | 속도 제한 | 요청이 너무 많음 | API 호출 빈도 감소 |

      +++

1. 
   +++ 추가 진단 검사 진행

   1. Campaign 보고서에서 라이브 활동 라이프사이클 지표를 확인합니다.

      캠페인 보고서에서 **라이브 활동 라이프사이클** 섹션을 검토하십시오.

      | 지표 | 확인할 사항 |
      |-|-|
      | 원격 시작 | API 트리거 시작 수를 표시해야 함 |
      | 업데이트 | 업데이트 이벤트 수를 표시해야 함 |
      | 종료 | 종료 이벤트 수를 표시해야 함 |
      | 총계 수 | 전체 라이브 활동 이벤트 볼륨 |

      이러한 지표가 0이거나 API 호출과 일치하지 않으면 Adobe과 APNs 간에 게재 문제가 있습니다.

   1. Adobe에 성공적인 게재가 표시되지만 디바이스에 라이브 활동이 표시되지 않는 경우:

      * iOS 장치 로그에서 라이브 활동 오류를 확인합니다.
      * 앱이 전경이나 배경에 있는지 확인합니다(종료되지 않음).
      * 장치에 네트워크 연결이 있는지 확인하십시오.
      * 여러 장치를 테스트하여 장치별 문제를 배제합니다.
      * iOS 버전이 16.1 이상인지 확인합니다.

      +++

1. 
   +++ Adobe 지원으로 에스컬레이션

   모든 단계를 완료했지만 문제가 해결되지 않은 경우 Adobe 고객 지원 센터에 문의하십시오.

   **필수 정보:**

   * 캠페인 ID 및 이름
   * 프로필 네임스페이스 및 ID
      * API 페이로드의 `liveActivityID`
   * API 호출의 타임스탬프
   * 스크린샷:
      * 캠페인 보고서(전송 통계, 오류 이유, 제외된 이유)
      * 프로필 이벤트(`liveActivity.updateToken`, `message.feedback`)
      * 게재 이벤트를 보여주는 Assurance 세션
   * 전체 API 요청 페이로드
   * APNs 인증서 세부 정보(만료, 환경, 번들 ID)

     +++

## 단일 고유 시나리오

### 라이브 활동 업데이트 토큰이 동기화되지 않음{#token-not-synced}

장치에서 라이브 활동이 성공적으로 시작되지만 후속 `update` 또는 `end` API 호출(HTTP 200 반환)에서 라이브 활동을 업데이트하거나 취소하지 못했습니다. 이 문제는 **Live 활동 업데이트 토큰**&#x200B;이(가) Adobe 시스템에 제대로 동기화되지 않을 때 발생합니다.

**업데이트 토큰 이해**

장치에서 라이브 활동이 시작되면 iOS은 해당 특정 라이브 활동 인스턴스에 대한 고유한 업데이트 토큰을 생성합니다. 이 토큰은 다음에 필요합니다.

* 라이브 활동에 업데이트 보내기
* 라이브 활동 원격 종료

각 라이브 활동 인스턴스에는 고유한 업데이트 토큰이 있습니다. Adobe은 업데이트 및 최종 이벤트를 전달하기 위해 이 토큰이 필요합니다.

**필요한 동작**

업데이트 및 종료 이벤트가 작동하려면 다음 상황이 발생해야 합니다.

1. 장치에서 라이브 활동이 성공적으로 시작됩니다.
1. 장치는 해당 라이브 활동 인스턴스에 대한 업데이트 토큰을 생성합니다.
1. Mobile SDK은 업데이트 토큰을 캡처하여 Adobe으로 보냅니다.
1. 업데이트 토큰이 동기화되어 Adobe 시스템에 저장됩니다.
1. 업데이트/종료에 대한 후속 API 호출은 이 토큰을 게재에 사용합니다.

**사전 확인:**

* **사용자 권한**: 장치에서 라이브 활동이 처음 시작될 때 iOS에 &quot;[앱 이름]에서 라이브 활동 업데이트를 제공할 수 있도록 허용하시겠습니까?&quot;라는 시스템 메시지가 표시됩니다. **사용자는 업데이트 토큰을 생성하고 동기화하려면 &quot;허용&quot;**&#x200B;을 탭해야 합니다. 사용자가 &quot;허용 안 함&quot;을 탭하면 업데이트 토큰이 생성되지 않고 업데이트/종료 요청이 실패합니다. 앱당 1회 권한입니다.
* **프로필 및 캠페인 유효성 검사**: 프로필, 토큰 및 캠페인 구성이 올바른지 확인하기 위한 [시나리오 1](#profile-issue) 및 [시나리오 2](#payload-issues) 검사를 완료합니다.

#### 디버깅 단계

1. 
   +++ Assurance에서 업데이트 토큰 동기화 확인

   1. Assurance 세션을 엽니다.
   1. 장치에서 라이브 활동이 시작될 때 세션이 활성화되었는지 확인합니다.
   1. `eventType = "liveActivity.updateToken"`을(를) 사용하여 이벤트를 필터링하거나 검색합니다.
   1. 이벤트를 선택하고 페이로드를 검사합니다.

      * `token` 필드에 올바른 업데이트 토큰 문자열이 포함되어 있는지 확인하십시오.
      * `liveActivityID`이(가) 라이브 활동 인스턴스와 일치하는지 확인하십시오.
      * `activityType`이(가) `attributes-type`과(와) 일치하는지 확인하십시오.

   1. 이벤트를 찾을 수 없는 경우:

      * 업데이트 토큰이 SDK에서 생성되거나 캡처되지 않았습니다.
      * 사용자가 라이브 활동 권한을 부여했는지 확인합니다.
      * 장치에서 라이브 활동이 실제로 성공적으로 시작되었는지 확인합니다.
      * 모바일 SDK이 업데이트 토큰을 캡처하도록 올바르게 통합되었는지 확인합니다.

   1. 이벤트가 발견되면 2단계로 진행합니다.

      +++

2. 
   +++ 프로필 이벤트에서 업데이트 토큰 확인

   1. Journey Optimizer의 **고객** > **프로필**(으)로 이동합니다.
   1. 프로필을 검색하여 엽니다.
   1. **이벤트** 탭을 선택합니다.
   1. `liveActivity.updateToken`개의 이벤트를 찾습니다.
   1. 이벤트 세부 사항을 확인합니다.

      * 타임스탬프가 최근인지 확인합니다(라이브 활동이 시작된 시기와 일치).
      * `token` 및 `liveActivityID`이(가) 있는지 확인하십시오.
      * `activityType`이(가) 올바른지 확인하십시오.

   1. 프로필에서 이벤트를 찾을 수 없는 경우

      * 업데이트 토큰 이벤트가 아직 프로필에 수집되지 않았을 수 있습니다.
      * 5-10분 정도 기다린 후 다시 확인하십시오.
      * 15분 후에도 계속 누락된 경우 이벤트 수집 문제가 있을 수 있습니다.

   1. 이벤트가 발견되면 업데이트 토큰이 동기화됩니다. 3단계로 진행할 수 있습니다.

      +++

3. 
   +++ Assurance에서 라이브 활동 전달 이벤트 확인

   1. Assurance 세션에서 업데이트 또는 종료 API 호출을 실행합니다.
   1. **이벤트 목록**&#x200B;에서 라이브 활동 전달 이벤트(APNs 푸시 이벤트)를 찾습니다.
   1. 다음을 나타내는 이벤트를 확인합니다.
      * APNs에 푸시 알림을 보냈습니다.
      * APNs 응답(성공 또는 오류).
      * 게재 확인.
   1. APNs 게재 이벤트가 있는 경우 푸시 알림이 전송되었습니다. 디바이스가 여전히 업데이트되지 않으면 디바이스 측에서 문제가 발생할 수 있습니다(푸시, 네트워크 문제 등을 처리하지 않는 앱).
   1. APNs 게재 이벤트가 누락된 경우: 업데이트 토큰이 Adobe 시스템의 프로필에 제대로 저장되거나 연결되지 않을 수 있습니다.
   1. 오류 이벤트가 있는 경우: 특정 실패 이유(잘못된 토큰, APNs 거부됨 등)에 대해 오류 세부 사항을 검사합니다.

      +++

## 브로드캐스트 특정 시나리오

### 브로드캐스트 캠페인 구성 및 페이로드 문제{#broadcast-config}

이 섹션에서는 단일 캠페인과 다른 디버깅 접근 방식이 필요한 라이브 브로드캐스트 활동과 관련된 문제 해결 시나리오를 다룹니다.

프로필에 유효한 토큰이 있지만 라이브 활동이 대상 구성원에 대해 나타나거나, 업데이트되거나, 예상대로 작동하지 않는 경우 문제는 일반적으로 다음 중 하나에서 발생합니다.

* 캠페인이 API 트리거 마케팅으로 구성되지 않았습니다.
* API 페이로드가 잘못된 브로드캐스트 구조를 사용합니다(`audience` 또는 `input-push-channel` 누락).
* `content-state` 및 `attributes` 필드가 iOS `ActivityAttributes` 구현과 일치하지 않습니다.
* Apple 개발자 포털에 `input-push-channel`이(가) 올바르게 만들어지지 않았습니다.

이 문제 해결 시나리오는 브로드캐스트 캠페인의 모든 라이브 활동 이벤트(`start`, `update` 및 `end`)에 적용됩니다.

**사전 확인:**

* **캠페인 유형**:
   * 캠페인이 API 트리거 마케팅으로 생성되었는지 확인합니다(브로드캐스트/대상 기반 캠페인에 필요).
   * 대상이 캠페인 구성에 정의되어 있는지 확인합니다.
* **프로필 및 토큰 유효성 검사**: 대상에서 여러 프로필을 샘플링하여 `liveActivityPushNotificationDetails`이(가) 유효한지 확인합니다. 자세한 유효성 검사 단계는 [시나리오 1](#profile-issue)을(를) 참조하십시오.

#### 디버깅 단계

1. 
   +++ 캠페인 대상자 구성 확인

   1. Journey Optimizer에서 **API로 트리거된 마케팅 캠페인**&#x200B;을 엽니다.
   1. **대상자** 섹션으로 이동하여 다음을 확인하십시오.
      * 캠페인에 대한 대상자가 선택됩니다.
      * 대상 ID는 API 페이로드에 사용된 ID와 일치합니다.
      * 대상에는 예상 프로필이 포함됩니다.
   1. **작업** 섹션으로 이동합니다.
   1. **라이브 활동 구성**&#x200B;을 확인하세요.
      * iOS 앱에 대한 구성을 올바른 번들 식별자로 설정해야 합니다.
      * 활동 유형은 API 페이로드의 `attributes-type`과(와) 일치해야 합니다. 예를 들어 페이로드에 `"attributes-type": "AirplaneTrackingAttributes"`이(가) 포함된 경우 캠페인은 동일한 활동 유형을 지정해야 합니다.

      +++

1. 
   +++ 브로드캐스트 API 페이로드 구조 확인

   브로드캐스트 페이로드 구조는 단일 캠페인과 다릅니다. 페이로드가 올바른 브로드캐스트 형식을 따르는지 확인합니다.

   **브로드캐스트의 필수 필드:**

   ```json
   {
     "campaignId": "878a11d4-b519-47bd-8313-fecfee19857b",
     "audience": {
       "id": "8c3dbdea-2957-401f-acf0-3966fba1601e"
     },
     "context": {
       "requestPayload": {
         "aps": {
           "input-push-channel": "FEt0NgvLEfEAAOqA6AXdIQ==",
           "content-available": 1,
           "timestamp": 1771829292,
           "event": "update",
           "attributes-type": "AirplaneTrackingAttributes",
           "content-state": { ... },
           "attributes": { ... }
         }
       }
     }
   }
   ```

   **일반적인 페이로드 문제:**

   | 필드 | 요구 사항 | 일반적인 문제 |
   |-|-|-|
   | `campaignId` | 활성화된 마케팅 캠페인 ID와 일치해야 함 | 잘못된 캠페인 ID 또는 트랜잭션 캠페인 사용 |
   | `audience.id` | AEP의 기존 대상과 일치해야 합니다. | 잘못된 대상 ID 또는 대상이 존재하지 않습니다. |
   | `input-push-channel` | 브로드캐스트에 필요 - 이 브로드캐스트 인스턴스의 고유 식별자 | 누락되었거나 `channelID`의 `liveActivityData`과(와) 일치하지 않습니다. |
   | `timestamp` | 항상 현재/최신 Unix Epoch 시간(초)이어야 함 | 이전/캐시된 타임스탬프 사용 |
   | `event` | `"start"`, `"update"` 또는 `"end"`이어야 합니다. | 잘못된 이벤트 유형 |
   | `attributes-type` | 캠페인 활동 유형과 일치해야 함 | 불일치 또는 오타 |
   | `content-available` | `1`이어야 합니다. | 누락되거나 잘못된 값 |

   **중요한 브로드캐스트 관련 필드:**

   * **`input-push-channel`**:
      * 모든 브로드캐스트 라이브 활동에 필요합니다.
      * 이 특정 브로드캐스트 인스턴스의 고유 식별자 역할을 합니다.
      * 대상자의 모든 프로필은 이 채널에 연결된 라이브 활동을 수신합니다.
      * `channelID`의 `liveActivityData.channelID`과(와) 일치해야 합니다(3단계 참조).
      * 클라이언트가 Apple 개발자 포털에서 `appID`에 대해 만들어야 합니다.
      * 특정 `appID`에 대해 만들어진 채널만 해당 앱에서 라이브 활동을 브로드캐스트하는 데 사용할 수 있습니다.

   * **`audience.id`**:
      * Adobe Experience Platform에서 생성된 유효한 대상 세그먼트를 참조해야 합니다.
      * 이 대상자의 모든 프로필은 라이브 활동을 대상으로 합니다.
      * 대상자를 활성화해야 하며 올바른 `liveActivityPushNotificationDetails`의 프로필을 포함해야 합니다.

   **항상 최신 타임스탬프 사용:**

   * `timestamp` 필드는 모든 API 호출에 대해 항상 현재 Unix Epoch 시간(초)이어야 합니다.
   * 이 요구 사항은 모든 이벤트 유형(`start`, `update` 및 `end`)에 적용됩니다.
   * **업데이트/종료에 중요**: 오래된 타임스탬프를 사용하면 업데이트 및 종료 요청이 실패합니다.
   * 모든 브로드캐스트 API 호출에 대해 새 타임스탬프를 생성합니다.

   **선택적 필드:**

   * `dismissal-date`: 자동 해지를 위한 Unix epoch 시간(`end`개 이벤트에만 관련됨)
   * `alert`: 알림에 대해 `title` 및 `body`이(가) 있는 개체

   전체 API 사양은 [Adobe Journey Optimizer 메시징 API 설명서](https://developer.adobe.com/journey-optimizer-apis/references/messaging)를 참조하십시오.

   +++

1. 
   +++ 컨텐츠 상태, 속성 및 입력-푸시 채널을 iOS 구현에 맞게 조정

   페이로드 필드가 iOS 앱의 `ActivityAttributes` 구현과 일치하고 `input-push-channel`이(가) `channelID`의 `liveActivityData`과(와) 일치하는지 확인하십시오.

   1. iOS ActivityAttributes 정의를 검토합니다.

   사용자 지정 `ActivityAttributes` 구조체가 Adobe의 `LiveActivityAttributes` 프로토콜을 구현해야 합니다.

   ```swift
   struct AirplaneTrackingAttributes: LiveActivityAttributes {
    public struct ContentState: Codable, Hashable {
        var journeyProgress: Int
    }
   
    // Adobe SDK requirement
    var liveActivityData: LiveActivityData
   
    // Your custom attributes
    var arrivalAirport: String
    var departureAirport: String
    var arrivalTerminal: String
   }
   ```

   1. iOS 필드를 브로드캐스트 API 페이로드에 매핑합니다.

   모든 이벤트에 `attributes`과(와) `content-state`을(를) 모두 포함합니다.

   ```json
         {
         "aps": {
          "input-push-channel": "FEt0NgvLEfEAAOqA6AXdIQ==",
          "event": "start",
          "timestamp": 1771829292,
          "attributes-type": "AirplaneTrackingAttributes",
          "content-state": {
            "journeyProgress": 0
          },
          "attributes": {
            "arrivalAirport": "DEL",
            "departureAirport": "MUM",
            "arrivalTerminal": "T1",
            "liveActivityData": {
              "channelID": "FEt0NgvLEfEAAOqA6AXdIQ=="
            }
          }
         }
         }
   ```

   **중요: `input-push-channel`은(는)`channelID`**&#x200B;과(와) 일치해야 합니다.

   * `input-push-channel`의 루트에 있는 `aps` 값은 `channelID`의 `liveActivityData`과(와) 정확히 일치해야 합니다.
   * 위의 예에서 두 값은 모두 `"FEt0NgvLEfEAAOqA6AXdIQ=="`입니다.
   * 이렇게 일치하면 브로드캐스트 인스턴스가 라이브 활동 데이터에 연결됩니다.
   * 불일치로 인해 게재 오류가 발생합니다.

   **주요 유효성 검사 지점:**

   * 모든 이벤트 유형에 대해 `ContentState`에 모든 `content-state` 필드를 포함하십시오.
   * 시작 이벤트에 대해서만 `LiveActivityAttributes`의 모든 사용자 지정 `attributes` 필드를 포함합니다.
   * 시작 이벤트의 경우 `liveActivityData.channelID`은(는) `input-push-channel`과(와) 일치해야 합니다.
   * 필드 이름은 대소문자를 구분하며 정확히 일치해야 합니다.
   * 데이터 유형은 일치해야 합니다(문자열, 정수, 부울, 중첩된 오브젝트 등).
   * 업데이트/종료 이벤트의 경우 원래 시작 이벤트와 동일한 `input-push-channel`을(를) 사용합니다.

   **일반적인 실수:**

   | 문제 | 영향 | 변수 이름이 아니라, 필터링된 보고서의 머리글로 잘못 표시하는 |
   |-|-|-|
   | `input-push-channel` 누락 | 브로드캐스트가 작동하지 않습니다. | 각 브로드캐스트에 대한 고유 채널 ID 추가 |
   | `input-push-channel`이(가) `channelID`과(와) 일치하지 않습니다. | 라이브 활동이 시작되지 않음 | 두 값이 동일한지 확인합니다. |
   | 업데이트/종료에 대해 다른 `input-push-channel` | 업데이트/종료가 라이브 활동에 도달하지 않음 | 라이프사이클 전체에서 동일한 채널 ID 사용 |
   | `liveActivityData.channelID` 누락 | 라이브 활동이 브로드캐스트에 연결되지 않습니다. | 시작 이벤트의 특성에 `channelID` 포함 |
   | 시작 이벤트에 필수 필드 누락 | 라이브 활동이 시작되지 않음 | iOS 구조의 모든 필드 추가 |
   | 잘못된 필드 이름(오타/사례) | 무시된 필드 또는 구문 분석 오류 | iOS 필드 이름과 정확히 일치 |
   | 업데이트/종료 시 오래된 타임스탬프 | 장치에서 무시한 업데이트/종료 | 항상 새 타임스탬프 생성 |

   +++

1. 
   +++ Assurance으로 테스트

   Assurance을 사용하여 API 실행 및 페이로드 게재 확인:

   1. 대상의 일부인 테스트 장치에서 Assurance 세션을 엽니다.
   1. 브로드캐스트 API 호출을 실행합니다.
   1. **이벤트 목록**&#x200B;에서 다음을 찾습니다.
      * 캠페인 실행 이벤트.
      * 라이브 활동 전달 이벤트.
      * 페이로드 유효성 검사 실패를 나타내는 오류 이벤트
   1. 이벤트 페이로드를 검사하여 확인:
      * 페이로드가 올바르게 처리되었습니다.
      * `input-push-channel`이(가) 있습니다.
      * 유효성 검사 오류가 발생하지 않았습니다.
      * 라이브 활동이 대상 구성원을 위해 APNs로 전송되었습니다.

      +++

### 프로필이 대상 또는 부실 대상 스냅샷에 없음

이 시나리오에서는 캠페인과 페이로드가 올바르게 구성되었지만 특정 프로필이 라이브 활동을 수신하고 있지 않습니다. 이 문제는 일반적으로 다음과 같은 경우에 발생합니다.

* 프로필이 캠페인에 연결된 대상자의 멤버가 아닙니다.
* 대상자는 일괄 처리 대상자이며 프로필 데이터의 오래된 스냅샷을 포함합니다.
* 프로필의 라이브 활동 토큰이 최근에 추가되었지만 아직 대상 스냅숏에 반영되지 않았습니다.

이 문제 해결 시나리오는 특히 대상 기반 타깃팅을 사용하는 브로드캐스트 캠페인에 적용됩니다.

**대상 평가 이해**

Adobe Experience Platform에서는 프로필 업데이트가 대상에 반영되는 시기를 결정하는 다양한 대상 평가 방법을 사용합니다.

| 메서드 | 평가 빈도 | 데이터 새로 고침 | 다음에 대한 우수 사례 |
|-|-|-|--|
| 배치 | 매일 한 번(예약됨) | 최장 24시간 오래됨 | 대규모 대상, 시간에 민감하지 않음 |
| 스트리밍 | 실시간(프로필 변경 시) | 업데이트된 프로필에 대해 거의 실시간으로 | 시간에 민감함, 프로필 업데이트 필요 |

**사전 확인:**

* **캠페인 및 페이로드 유효성 검사**:
   * [이 시나리오](#broadcast-config)에서 검사를 완료하여 캠페인과 페이로드가 올바른지 확인하세요.
   * API 페이로드의 `audience.id`이(가) 캠페인 구성과 일치하는지 확인하십시오.
* **프로필 있음**: 프로필이 유효한 `liveActivityPushNotificationDetails`을(를) 사용하여 AEP에 있는지 확인하십시오.

#### 디버깅 단계

1. 
   +++ 프로필이 대상자에 있는지 확인

   먼저 라이브 활동을 수신해야 하는 프로필이 실제로 대상자의 일부인지 확인합니다.

   1. Adobe Experience Platform의 **대상**(으)로 이동합니다.
   1. 캠페인의 `audience.id`을(를) 사용하여 대상자를 검색하고 엽니다.
   1. 대상 구성원을 보려면 **찾아보기** 또는 **샘플 프로필**&#x200B;을 클릭하세요.
   1. 네임스페이스 및 ID 값을 사용하여 테스트 프로필을 검색합니다.
   1. **프로필이 대상자에 없는 경우:**
      * 프로필이 대상자 기준이나 세그먼트 규칙을 충족하지 않습니다.
      * 대상자 정의를 검토하여 멤버십 요구 사항을 이해합니다.
      * 프로필을 포함하도록 프로필 데이터 또는 대상자 정의를 업데이트합니다.
      * 대상 평가가 완료될 때까지 기다립니다( 2단계 참조).
   1. **대상자에 프로필이 있는 경우:** 2단계로 진행하여 데이터의 최신 상태를 확인합니다.

      +++

2. 
   +++ 대상 평가 유형 및 일정 확인

   대상자가 일괄 처리 또는 스트리밍 평가를 사용하는지 여부를 식별하십시오. 이렇게 하면 데이터 신선도가 결정됩니다.

   1. **대상자 세부 정보** 페이지에서 **평가 메서드**&#x200B;를 확인하세요.
      * **일괄 처리**: 일정에 따라 매일 한 번 평가됩니다.
      * **스트리밍**: 프로필 업데이트가 발생할 때 실시간으로 평가됩니다.
      * **Edge**: 가장자리 위치에서 실시간으로 평가되었습니다.

   평가 방법에 따라 적절한 문제 해결 단계를 수행합니다.

   **대상자가 일괄 처리 평가를 사용하는 경우:**

   1. **일괄 처리 대상 제한 이해:**
      * 배치 대상은 하루에 한 번(일반적으로 밤에) 평가됩니다.
      * 대상 스냅샷은 최대 24시간 경과할 수 있습니다.
      * 프로필이 최근에 등록된 라이브 활동 토큰인 경우 해당 토큰이 현재 스냅샷에 없을 수 있습니다.
      * 프로필에 대한 업데이트는 다음 일괄 처리 평가 때까지 반영되지 않습니다.

   1. **마지막 평가 발생 시기 확인:**
      * 대상 세부 정보에서 **마지막 평가** 타임스탬프를 찾습니다.
      * 이 타임스탬프 후에 프로필의 `liveActivityPushNotificationDetails`이(가) 업데이트된 경우 대상자에게 오래된 데이터가 있습니다.

   1. **부실 데이터 해결:**
      1. **옵션 1: 예약된 일괄 처리 평가 대기**
         * 다음 배치 평가에는 업데이트된 프로필 데이터가 포함됩니다.
         * 이 작업은 하루에 한 번 자동으로 수행됩니다.
         * 긴급하지 않은 시나리오에 적합합니다.

      1. **옵션 2: 온디맨드 대상 평가 트리거**
         1. AEP의 **대상**(으)로 이동합니다.
         1. 대상자를 선택합니다.
         1. **지금 평가** 또는 **요청 시 활성화**&#x200B;를 클릭합니다.
         1. 평가가 완료될 때까지 기다립니다(대상 크기에 따라 몇 분에서 몇 시간이 소요될 수 있음).
         1. 이제 프로필에서 대상 스냅샷의 데이터를 업데이트했는지 확인합니다.
         1. 브로드캐스트 API 호출을 다시 시도하십시오.

   **대상자가 스트리밍 평가를 사용하는 경우:**

   1. **스트리밍 대상 동작 이해:**
      * 스트리밍 대상은 프로필 업데이트가 발생할 때 실시간으로 평가됩니다.
      * **새 프로필**: 세그먼트 기준을 충족하면 만든 후 곧 사용할 수 있습니다.
      * **업데이트된 프로필**: 업데이트한 후 곧 자격 조건을 지정하거나 자격을 박탈합니다.
      * **변경되지 않은 기존 프로필**: 업데이트가 없으면 다시 평가되지 않습니다.

   1. **문제 식별:**
      * 프로필이 이미 존재하고 세그먼트 기준을 충족하지만 해당 프로필에서 업데이트가 발생하지 않는 경우 새로 만든 스트리밍 대상에 추가되지 않을 수 있습니다.
      * 재평가를 트리거하려면 프로필이 업데이트(속성 변경 사항)를 받아야 합니다.

   1. **문제 해결:**
      * **새 프로필의 경우**: 조건이 충족되면 자동으로 자격을 부여합니다. 조치가 필요하지 않습니다.
      * **최근 업데이트가 없는 기존 프로필의 경우:**
         * 프로필의 작은 업데이트(예: 타임스탬프 필드 업데이트)를 수행합니다.
         * 이렇게 하면 스트리밍 평가가 트리거되고 프로필이 대상자에 추가됩니다.
         * 대체 요소: 기존 프로필에 대해 배치 대상 또는 에지 대상을 사용합니다.

      +++
