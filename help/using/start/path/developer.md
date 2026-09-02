---
title: 개발자를 위한 시작
description: 데이터 엔지니어로서 Journey Optimizer로 작업하는 방법에 대해 자세히 알아봅니다.
feature: Get Started
role: Developer
level: Intermediate
exl-id: 5053dd4f-d050-415f-bc74-d6d061bdcbe1
TQID: https://experienceleague.adobe.com/7fRI-CPkIeBAPjtXmDgFdyNKgB4WwEc01yKrGUXnc3U
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: c2beecbb-b93e-4ae3-baa9-72adcdc06781
  - id: d08afb72-92f6-4856-88e3-11ec34313c2f
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b4dd41a7-ccf8-4e9d-918e-acaab534a307
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: e9001ce2-5245-4a8e-8601-dd958009072f
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: cf815079d67f4a41c3647c6a6e381ef5f1c44e51
workflow-type: ht
source-wordcount: 3490
ht-degree: 100%

---

# 개발자를 위한 시작 {#get-started-developers}

>[!BEGINSHADEBOX]

**이 페이지의 내용:** 애플리케이션을 Adobe Journey Optimizer에 연결하여 실시간 데이터에서 여정을 실행할 수 있도록 SDK, 이벤트 스트리밍, 사용자 정의 액션 엔드포인트 및 API를 구현합니다.

>[!ENDSHADEBOX]

**개발자**&#x200B;로서 [!DNL Adobe Journey Optimizer]를 구현하고 응용 프로그램 및 시스템에 통합해야 합니다. [시스템 관리자](administrator.md) 및 [데이터 엔지니어](data-engineer.md)에 액세스 권한을 부여하고 환경을 준비하면 [!DNL Adobe Journey Optimizer]로 작업을 시작할 수 있습니다.

>[!NOTE]
>
>**구현 순서:** [관리자](administrator.md) → [데이터 엔지니어](data-engineer.md) → 현재 위치: **개발자** → [마케터](marketer.md)
>
>모바일 및 웹 통합을 구현하기 전에 [데이터 스키마 및 이벤트{1}](data-engineer.md)가 구성되었는지 확인하세요.

## Journey Optimizer 생태계에서의 역할

다른 팀원이 사용자 인터페이스를 통해 Journey Optimizer를 구성하는 동안 다음 사항에 집중할 수 있습니다.

* 모바일 및 웹 애플리케이션에서 **SDK 구현**
* 여정을 트리거하기 위해 응용 프로그램에서 **이벤트 보내기**
* Journey Optimizer에서 사용자 지정 작업을 통해 호출할 수 있는 **API 엔드포인트 빌드**
* 기존 시스템 및 인프라와 Journey Optimizer **통합**
* 구현 **테스트 및 디버깅**

[데이터 엔지니어](data-engineer.md)가 데이터 스키마, 이벤트 구성 및 데이터 원본을 처리합니다. [관리자](administrator.md)가 권한 및 채널 구성을 설정합니다. [마케터](marketer.md)가 구현을 사용하는 여정 및 콘텐츠를 디자인합니다.

이 안내서에서는 Journey Optimizer를 시작하는 데 필요한 기술 구현 단계를 다룹니다. 모바일 앱, 웹 경험 또는 API 통합 중 어느 것을 구축하든 아래 섹션에 따라 구현을 설정하세요.

## 사전 요구 사항 {#prerequisites}

구현을 시작하기 전에 다음을 확인하세요.

| 카테고리 | 요구 사항 |
|----------|-------------|
| **보유 기술** | * JavaScript(Web SDK) 또는 Swift/Kotlin(모바일 SDK)에 대한 경험<br>* RESTful API 및 JSON에 대한 이해<br>* 비동기 프로그래밍 및 이벤트 기반 아키텍처 알아보기<br>* 조직의 애플리케이션 아키텍처에 대한 지식 |
| **액세스 및 도구** | * API 자격 증명에 대한 [Adobe Developer Console](https://developer.adobe.com){target="_blank"}에 액세스<br>* 응용 프로그램의 코드베이스에 액세스할 수 있는 개발 환경<br>* API 테스트를 위한 Postman과 같은 테스트 도구<br>* 브라우저 개발자 도구 또는 모바일 디버깅 도구 |
| **다른 팀원의** | * [관리자](administrator.md)<br>가 부여한 환경 액세스 권한* [데이터 엔지니어](data-engineer.md)<br>*의 XDM 스키마 및 이벤트 정의 *[마케터](marketer.md)의 요구 사항 및 사용 사례 |

## 기술적 기반 이해 {#technical-foundation}

구현으로 이동하기 전에 핵심 기술 개념을 숙지하세요.

1. **Adobe Experience Platform 통합**: Journey Optimizer는 기본적으로 Adobe Experience Platform에 빌드되어 있습니다. 기본 아키텍처를 이해하면 보다 효과적인 구현을 구축하는 데 도움이 됩니다. [Journey Optimizer 작동 방식](../understanding-ajo.md)에 대해 자세히 알아보세요.

1. **XDM 데이터 모델**: Journey Optimizer는 XDM(경험 데이터 모델)을 사용하여 이벤트 및 프로필 데이터를 구조화합니다. 개발자는 [데이터 엔지니어](data-engineer.md)가 구성한 스키마를 준수하는 데이터를 보내는 방법을 이해해야 합니다. [XDM 스키마](../../data/get-started-schemas.md)에 대해 알아보세요.

1. **인증 및 보안**: 모든 구현에는 적절한 인증이 필요합니다. SDK 및 API에 대한 인증을 설정하는 방법을 이해합니다. [API 인증](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"}에 대해 알아봅니다.

## 모바일 앱 통합 설정 {#mobile-integration}

### Adobe Experience Platform Mobile SDK 구성

모바일 SDK는 iOS 또는 Android 앱에 직접 임베드하는 라이브러리 컬렉션입니다. 앱과 Adobe Experience Platform 간의 커뮤니케이션 레이어 역할을 합니다. 사용자를 식별하고, 행동 이벤트를 수집하며, Journey Optimizer의 지침(푸시 알림, 인앱 메시지 및 개인화된 콘텐츠 포함)을 전달합니다. 모바일 SDK가 없으면 Journey Optimizer는 앱 사용자의 활동을 파악할 수 없고 사용자에게 도달할 방법도 없습니다.

1. **Mobile SDK 설치 및 구성**: SDK 통합을 시작하려면 [Adobe Experience Platform Mobile SDK 문서](https://developer.adobe.com/client-sdks/documentation/getting-started){target="_blank"}를 따르세요.

1. **모바일 속성 생성**: [!DNL Adobe Experience Platform Data Collection]에서 모바일 속성을 설정합니다. [모바일 속성을 생성하고 구성](https://developer.adobe.com/client-sdks/documentation/getting-started/create-a-mobile-property){target="_blank"}하는 방법을 알아보세요.

1. **푸시 알림 구성**:
   * **iOS 앱**&#x200B;의 경우: APNs(Apple Push Notification service)에 앱을 등록합니다. 자세한 내용은 [Apple 문서](https://developer.apple.com/documentation/usernotifications/registering_your_app_with_apns){target="_blank"}에서 확인하세요.
   * **Android 앱**&#x200B;의 경우: Android 앱에 Firebase 클라우드 메시징을 설정합니다. 자세한 내용은 [Google 문서](https://firebase.google.com/docs/cloud-messaging/android/client){target="_blank"}에서 확인하세요.

1. **모바일 통합 테스트**: [모바일 온보딩 빠른 시작 워크플로](../../push/mobile-onboarding-wf.md)를 사용하여 모바일 설정을 신속하게 구성하고 테스트합니다.

푸시 알림을 구성하는 자세한 단계는 [이 페이지](../../push/push-configuration.md)에서 확인할 수 있습니다.

### 코드 기반 경험 구현(Mobile SDK)

코드 기반 경험을 통해 새 앱을 출시하지 않고도 온보딩 화면, 제품 상세 페이지, 인앱 배너, 기능 플래그 등 기본 모바일 앱의 모든 영역에 개인화된 콘텐츠를 제공할 수 있습니다. 모바일 SDK를 사용하여 런타임에 개인화된 콘텐츠를 가져오고 렌더링하면 팀에서 배치 및 표시 방식을 충분히 제어할 수 있습니다.

* Mobile SDK 구현을 위해 [이 튜토리얼](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/code-based/tutorial){target="_blank"}을 따르세요.
* [iOS](https://github.com/adobe/aepsdk-messaging-ios/tree/main/TestApps/MessagingDemoAppSwiftUI){target="_blank"} 및 [Android](https://github.com/adobe/aepsdk-messaging-android/tree/main/code/testapp){target="_blank"}에 대한 샘플 구현을 검토합니다.

## 웹 경험 구현 {#web-implementation}

### Adobe Experience Platform Web SDK 설정

Web SDK(`alloy.js`)는 사이트에 필요한 여러 개의 개별 Adobe 태그를 대체하는 단일 JavaScript 라이브러리입니다. 이 라이브러리는 행동 데이터를 수집하고, 사용자가 구성한 데이터 스트림을 통해 Adobe Experience Platform으로 스트리밍하고, 개인화 지침을 다시 수신합니다. 이 모든 과정이 단 한 번의 네트워크 왕복으로 이루어집니다. Web SDK가 구축되면 Journey Optimizer는 방문자를 식별하고, 방문자의 행동에 따라 여정을 트리거하며, 맞춤형 콘텐츠를 페이지에 즉시 게재할 수 있습니다.

1. **Web SDK 설치**: [Web SDK 구현 안내서](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=ko-KR){target="_blank"}를 따라 웹 사이트에 SDK를 설정합니다.

1. **데이터 스트림 구성**: Journey Optimizer가 활성화된 [!DNL Adobe Experience Platform Data Collection]에서 데이터 스트림을 생성하고 구성합니다. 자세한 내용은 [데이터 스트림 문서](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=ko-KR){target="_blank"}에서 확인하세요.

1. **웹 푸시 알림 활성화**(선택 사항): 이제 웹 푸시 알림이 니다. Web SDK 구성에서 [pushNotifications 속성](https://experienceleague.adobe.com/ko/docs/experience-platform/collection/js/commands/configure/pushnotifications){target="_blank"}을 구성하고 [sendPushSubscription 명령](https://experienceleague.adobe.com/ko/docs/experience-platform/collection/js/commands/sendpushsubscription){target="_blank"}을 사용하여 푸시 구독을 등록합니다. [웹 푸시 구성에 대해 알아봅니다](../../push/push-configuration-web.md).

### 코드 기반 경험 구현(Web SDK)

마케터가 레이아웃을 완전히 제어하는 시각적 채널과 달리, 코드 기반 경험에서는 페이지에 개인화된 콘텐츠가 표시되는 방식을 완벽하게 제어할 수 있습니다. Journey Optimizer는 개인화 데이터가 포함된 JSON 페이로드를 반환하며, 사용자는 코드에서 해당 데이터를 어디에 어떻게 표시할지 결정합니다. 이 모델은 시각적 편집기나 페이지 게시 워크플로 없이도 히어로 배너, 추천 캐러셀, 검색 결과 순위, A/B 테스트 변형 등 모든 웹 영역에서 작동합니다.

1. **구현 방법 선택**: 클라이언트측, 서버측 또는 하이브리드입니다. 각 접근 방식에 대한 [구현 샘플](../../code-based/code-based-implementation-samples.md)을 검토하십시오.

1. **표면 정의**: 애플리케이션에서 개인화된 콘텐츠를 제공하려는 위치를 식별합니다. [표면 구성](../../code-based/code-based-surface.md)에 대해 알아보세요.

1. **콘텐츠 렌더링 구현**: Web SDK를 사용하여 개인화 콘텐츠를 가져오고 적용합니다. [코드 기반 구현 자습서](../../code-based/code-based-decisioning-implementations.md)를 참조하세요.

1. **표시 및 상호 작용 이벤트 전송**: 분석 및 최적화를 위해 콘텐츠가 표시되는 시점과 사용자가 콘텐츠와 상호 작용하는 시점을 추적합니다.

[GitHub에서 샘플 구현](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"}을 탐색하여 코드 기반 경험이 실제로 어떻게 작동하는지 확인하세요.

[코드 기반 경험을 시작](../../code-based/get-started-code-based.md)하는 방법에 대해 자세히 알아보세요.

## 이벤트 스트리밍 구현 {#event-streaming}

### 여정을 트리거할 이벤트 보내기

여정은 사용자 로그인, 장바구니 추가, 구매 완료, 양식 이탈 등의 이벤트에 따라 실행됩니다. 사용자는 애플리케이션에서 이러한 이벤트를 정확한 시점에 발생시키기만 하면 됩니다. 각 이벤트는 Experience Platform 스트리밍 수집 API로 전송되는 XDM 구조의 JSON 페이로드입니다. Journey Optimizer는 해당 이벤트를 밀리초 단위로 수신하여 프로필을 일치하는 여정으로 라우팅합니다. 이벤트 스키마 및 페이로드 구조는 [데이터 엔지니어](data-engineer.md)가 정의합니다. 코딩을 시작하기 전에 데이터 엔지니어와 협의합니다.

1. **이벤트 페이로드 이해**: 데이터 엔지니어와 협력하여 이벤트 스키마와 필요한 페이로드 구조를 확보합니다. 페이로드는 구성한 XDM 스키마를 준수해야 합니다. [이벤트 스키마 요구 사항](../../event/experience-event-schema.md)에 대해 알아봅니다.

1. **이벤트 스트리밍 구현**: [스트리밍 수집 API](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=ko){target="_blank"}를 사용하여 Adobe Experience Platform으로 이벤트를 전송합니다. [이벤트 전송 단계를 알아보세요](../../event/additional-steps-to-send-events-to-journey.md).

1. **이벤트 유형 처리**:
   * **단일 이벤트**: 사용자별 특정 작업(예: 버튼 클릭, 구매 완료)에 대한 이벤트 전송을 구현합니다.
   * **비즈니스 이벤트**: 재고 업데이트, 가격 변경 등 비즈니스 관련 이벤트를 전송합니다.

1. **테스트 이벤트 게재**: 이벤트가 제대로 수신되고 예상대로 여정이 트리거되는지 확인합니다. [이벤트 문제 해결](../../building-journeys/troubleshooting-inbound.md)에 대해 알아보세요.

API를 통해 이벤트를 전송하는 **구현 예시**:

```javascript
POST https://{DATACOLLECTION_ENDPOINT}/collection/{DATASTREAM_ID}
Content-Type: application/json

{
  "header": {
    "datasetId": "{DATASET_ID}",
    "imsOrgId": "{ORG_ID}",
    "source": {
      "name": "Web SDK"
    }
  },
  "body": {
    "xdmMeta": {
      "schemaRef": {
        "id": "{SCHEMA_ID}"
      }
    },
    "xdmEntity": {
      "_id": "unique-event-id",
      "eventType": "purchase",
      "timestamp": "2024-01-01T12:00:00Z",
      // ... your event data
    }
  }
}
```

[여정 이벤트 작업](../../event/about-events.md)에 대해 자세히 알아보세요.

## 사용자 정의 액션 엔드포인트 개발 {#custom-actions}

여정이 사용자 정의 액션 단계에 도달하면 Journey Optimizer는 사용자가 제공한 URL(백엔드, CRM, 충성도 플랫폼, REST 엔드포인트 등)로 HTTP 호출을 수행합니다. 사용자의 역할은 해당 엔드포인트를 구축하고 노출하는 것입니다. 요청 계약(페이로드 형태, 인증 방법, 응답 형식)을 정의하고, 관련 비즈니스 로직을 구현하며, Journey Optimizer가 생성할 호출량을 처리할 수 있도록 해야 합니다. [관리자](administrator.md)가 Journey Optimizer에 엔드포인트를 등록하면 마케터는 해당 엔드포인트를 여정의 단계로 사용할 수 있습니다.

1. **API 엔드포인트 작성**: Journey Optimizer가 여정 실행 중에 호출할 RESTful API 엔드포인트를 생성합니다. 엔드포인트는 다음과 같아야 합니다.
   * JSON 페이로드 수락
   * 요청 인증(OAuth, API 키 또는 JWT)
   * 적절한 시간 제한 내에 요청 처리
   * 예상된 형식의 응답 반환

1. **사용자 정의 액션 기능 이해**: 사용자 정의 액션은 Epsilon, Slack, Firebase와 같은 타사 시스템이나 자체 서비스에 연결할 수 있습니다. [사용자 지정 작업](../../action/action.md)에 대해 자세히 알아보세요.

1. **액션 구성 작업**: [관리자](administrator.md) 또는 [데이터 엔지니어](data-engineer.md)가 Journey Optimizer에서 사용자 정의 액션을 구성하여 API 엔드포인트 URL, 인증 방법 및 매개 변수를 정의합니다. API 사양을 제공해야 합니다. [사용자 정의 액션 구성](../../action/about-custom-action-configuration.md)에 대해 알아보세요. 선택에 따라 시간 초과/오류 분기에서 더 풍부한 대체 로직을 위해 **오류 응답 페이로드**&#x200B;를 정의할 수 있습니다.

1. **실행 가능한 데이터 반환**: 후속 여정 단계에서 사용할 수 있는 데이터를 반환하도록 API를 디자인합니다. [액션 응답](../../action/action-response.md)에 대해 알아보세요.

1. **사용자 정의 액션 상태 모니터링**: 사용자 정의 액션 모니터링 대시보드를 사용하여 성공한 호출, 오류, 처리량, 응답 시간, 대기열에서 대기한 시간을 추적합니다. [사용자 정의 액션 보고](../../action/reporting.md)에 대해 알아보세요.

1. **속도 제한 구현**: 엔드포인트가 예상되는 볼륨을 처리할 수 있는지 확인합니다. Journey Optimizer는 초당 5000회 호출 제한을 적용하지만, 시스템은 충분한 복원력을 갖추어야 합니다. [캡핑 및 스로틀링](../../configuration/external-systems.md)에 대해 알아보세요.

**사용 사례 예시**: 사용자 정의 액션을 사용하여 [Experience Platform에 여정 이벤트를 작성합니다](../../building-journeys/custom-action-aep.md).

## Journey Optimizer API 작업 {#apis}

모든 작업을 Journey Optimizer UI를 통해 수행할 필요는 없습니다. 때로는 자체 백엔드에서 캠페인을 트리거하거나, 개인 정보 요청 후 이메일 주소를 차단하거나, 외부 CMS에서 콘텐츠 템플릿을 동기화해야 할 수도 있습니다. Journey Optimizer의 REST API를 사용하면 플랫폼의 핵심 기능에 프로그래밍 방식으로 액세스할 수 있습니다. 모든 호출은 OAuth 서버 간 인증을 사용하며, 기존 JWT 방식은 더 이상 사용되지 않습니다.

1. **API 기능 이해**: Journey Optimizer API를 사용하면 다양한 리소스를 프로그래밍 방식으로 생성하고 읽고 업데이트 및 삭제할 수 있습니다. [Journey Optimizer API](../../configuration/ajo-apis.md)에 대해 알아보세요.

1. **인증**: Adobe Developer Console을 사용하여 API 인증을 설정하려면 [이 튜토리얼](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"}을 따르세요.

1. **API 참조 살펴보기**: 전체 API 문서를 찾아보고 [Adobe Journey Optimizer API 참조](https://developer.adobe.com/journey-optimizer-apis){target="_blank"}에서 API를 직접 사용해 보세요.

1. **API 트리거 캠페인**: API 트리거 캠페인을 사용하여 트랜잭션 메시지를 작성합니다. 대용량 시나리오(최대 5000TPS)의 경우 [높은 처리량 모드](../../campaigns/api-triggered-high-throughput.md)를 살펴보세요(추가 라이선스 필요).

1. **의사 결정 관리 API**: 오퍼 관리 및 의사 결정에 특수 API를 사용합니다. 자세한 내용은 [의사 결정 관리 API 안내서](../../offers/api-reference/getting-started.md)에서 확인하세요.

1. **의사 결정 마이그레이션 API**: 의사 결정 관리 엔터티를 프로그래밍 방식으로 유연한 범위, 자동 유효성 검사, 롤백 지원을 제공하는 의사 결정으로 마이그레이션합니다. 자세한 내용은 [의사 결정 마이그레이션 API 안내서](../../experience-decisioning/decisioning-migration-api.md)에서 확인하세요.

1. **SMS Webhook**: 들어오는 메시지를 캡처하는 인바운드 Webhook과 게재 확인 및 상태 업데이트를 수신하는 피드백 Webhook을 구성합니다. [자세히 알아보기](../../mobile/mobile-webhook.md).

## 테스트 및 디버깅 {#testing}

실제 구현을 시작하기 전에 이벤트가 적절한 시점에 발생하고, 여정이 예상대로 트리거되며, 사용자 정의 액션이 실제 부하에서 제대로 작동하고, 개인화된 콘텐츠가 올바르게 렌더링되는지 확인해야 합니다. 이 섹션에서는 SDK 로깅과 같은 저수준 도구부터 실제 프로필을 사용한 엔드투엔드 여정 테스트 실행에 이르기까지 문제를 조기에 발견하는 데 필요한 도구와 기술을 다룹니다.

1. **SDK 구현 디버그**: Adobe Experience Platform Assurance를 사용하여 SDK 이벤트를 검사하고, 데이터 수집의 유효성을 검사하며, 통합 문제를 발생 즉시 해결합니다. [Assurance에 대해 자세히 알아보세요](https://experienceleague.adobe.com/docs/experience-platform/assurance/home.html?lang=ko){target="_blank"}.

1. **테스트 이벤트 게재**: 애플리케이션의 이벤트가 Adobe Experience Platform에서 올바르게 수신되고 예상대로 여정이 트리거되는지 확인합니다. 이벤트 수집을 모니터링하고 페이로드 구조를 검증합니다.

1. **API 통합 유효성 검사**: 사용자 정의 액션 엔드포인트가 Journey Optimizer 요청을 올바르게 처리하고, 시간 제한 내에 응답하며, 예상되는 데이터 형식을 반환하는지 확인하기 위해 테스트합니다.

1. **테스트 프로필을 사용하여 테스트 모드 사용**: [데이터 엔지니어](data-engineer.md)와 협력하여 테스트 프로필에 액세스한 다음 여정 테스트 모드를 사용하여 구현을 검증합니다. [여정을 테스트](../../building-journeys/testing-the-journey.md)하는 방법을 알아보세요.

1. **SDK 로그 모니터링**: 개발 중 발생하는 문제를 해결하기 위해 SDK 구현에서 디버그 로깅을 활성화합니다.
   * **Mobile SDK**: SDK 이벤트와 API 호출을 확인하려면 로깅을 활성화합니다.
   * **Web SDK**: 브라우저 콘솔을 사용하여 SDK 활동을 모니터링합니다.

1. **데이터 스트림 구성 확인**: Journey Optimizer로 데이터를 전송하도록 데이터 스트림이 올바르게 구성되어 있는지 확인합니다. 이벤트가 데이터 스트림을 통해 올바른 대상으로 전달되는지 확인합니다.

1. **분석을 위한 여정 데이터 쿼리**: 데이터 레이크에서 SQL 쿼리를 사용하여 여정 단계 이벤트를 분석하고, 문제를 디버깅하고, 사용자 정의 액션 성능을 모니터링합니다. 다음과 같은 [여정 분석 쿼리 예시](../../reports/query-examples.md)를 살펴보세요.
   * 프로필 시작/종료 추적 및 삭제 이유
   * 사용자 정의 액션 성능 지표(지연, 처리량, 오류)
   * 이벤트 게재 및 오류 패턴
   * 여정 인스턴스 상태

## 고급 개발자 항목 {#advanced-topics}

핵심 SDK, 이벤트 및 API가 구축되면 다음 항목을 통해 프로필 크기를 늘리지 않고 런타임에 여정 데이터를 보강하고, 동의 신호를 처리하여 옵트아웃이 모든 통합에 반영되도록 하며, 프로덕션 규모에 필요한 처리량과 안정성을 위해 구현을 최적화하는 방법을 알아볼 수 있습니다.

### 상황별 데이터 및 보강 작업

여정에는 트리거 이벤트에 전달되는 데이터(제품 이름, 충성도 등급, 주문 품목 목록 등)보다 더 많은 데이터가 필요한 경우가 많습니다. 이 모든 정보를 모든 프로필에 미리 로딩하는 대신, 컨텍스트 보강 기능을 통해 여정은 런타임에 AEP 데이터 세트에서 해당 정보를 찾아보거나 사용자 정의 액션 응답에서 정보를 가져올 수 있습니다. 그러면 메시지와 분기 조건에서 해당 데이터를 참조할 수 있으며, 이 경우 데이터는 프로필에 영구적으로 저장되지 않습니다.

* **배열 반복**: Handlebars 구문을 사용하여 메시지에서 이벤트, 사용자 정의 액션 응답 및 데이터 세트 조회의 동적 목록을 표시합니다. [상황별 데이터 반복](../../personalization/iterate-contextual-data.md)에 대해 알아보세요.
* **데이터 집합 조회**: Adobe Experience Platform 데이터 세트에서 여정 데이터를 보강하기 위해 데이터 세트 조회 기능을 구현합니다. 데이터 엔지니어와 협력하여 구성을 진행합니다. [데이터 세트 조회](../../building-journeys/dataset-lookup.md)에 대해 알아보세요.

### 동의 및 거버넌스 작업

Journey Optimizer는 플랫폼 수준에서 데이터 거버넌스 및 동의 정책을 시행하지만, 통합 과정에서도 이러한 정책을 준수해야 합니다. 고객이 마케팅 커뮤니케이션 수신을 거부하거나 데이터 사용 레이블로 인해 필드 사용 방식이 제한되는 경우, 이러한 규칙은 UI에서 작업을 차단하는 것뿐만 아니라 사용자 정의 액션 및 데이터 세트 조회에도 반영되어야 합니다.

* **데이터 거버넌스**: 사용자 정의 액션에 데이터 사용 정책을 적용합니다. [데이터 거버넌스](../../action/action-privacy.md)에 대해 자세히 알아보세요.
* **동의 관리**: 구현에서 고객 동의 환경 설정을 처리합니다. [동의](../../action/consent.md)에 대해 알아보세요.

### 최적화 및 모범 사례

프로덕션 환경에서 Journey Optimizer를 구현하면 초당 수백만 건의 이벤트와 수천 건의 여정 실행이 정기적으로 처리됩니다. 이러한 리소스는 해당 규모에 맞춰 통합 기능을 최적화하는 데 도움이 됩니다. 예를 들어, 속도 제한에 도달하기 전에 이를 파악하고, 프로필이 자동으로 삭제되는 일반적인 여정 디자인 오류를 방지하며, 오류 발생 시 눈에 띄지 않게 처리되는 대신 정상적으로 작동하는 오류 처리를 구축하는 방법을 안내합니다.

* **캡핑 및 스로틀링**: 속도 제한을 이해하고 적절한 스로틀링을 구현합니다. [외부 시스템](../../configuration/external-systems.md)에 대해 알아보세요.
* **여정 최적화**: [여정 최적화](../../building-journeys/optimize.md)에 대한 모범 사례를 따릅니다.
* **오류 처리**: 강력한 오류 처리를 구현합니다. [오류 코드](../../building-journeys/error-codes-reference.md) 및 [문제 해결 안내서](../../building-journeys/troubleshooting.md)를 검토합니다.

## Journey Optimizer REST API 호출 {#rest-apis}

SDK 및 이벤트 스트리밍 구현 외에도 자체 시스템에서 Journey Optimizer를 프로그래밍 방식으로 실행할 수 있습니다. 전체 API 참조, OpenAPI 사양 및 코드 샘플은 [Journey Optimizer 개발자 포털](https://developer.adobe.com/journey-optimizer-apis){target="_blank"}에서 확인할 수 있습니다.

>[!NOTE]
>
>모든 은 OAuth 서버 간 인증을 사용해야 하며, JWT 방식은 더 이상 사용되지 않습니다. [인증 설정](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"}

### API 트리거 캠페인 실행 {#api-triggered}

대화형 메시지 실행 REST API를 사용하여 외부 시스템에서 트랜잭션 또는 마케팅 메시지를 트리거할 수 있습니다. 엔드포인트를 호출하기 전에 다음 사항을 확인하세요.

* 엔드포인트가 호출을 수락하기 전에 캠페인을 **활성화해야** 합니다.
* 호출에는 **60초의 시간 초과**&#x200B;가 있으며, 예기치 않은 시간 초과는 내부 재시도 기능을 통해 처리됩니다.
* 캠페인 시작/종료 날짜가 구성된 경우, 해당 날짜 이외의 API 호출은 실패합니다.
* 페이로드를 작성하려면 Journey Optimizer UI에서 실제 캠페인의 **cURL 요청** 섹션에서 생성된 샘플 cURL 요청을 가져오세요. 이 요청에는 해당 캠페인의 모든 개인화 변수가 포함되어 있습니다.
* 표준 캠페인과 [고처리량 캠페인](../../campaigns/api-triggered-high-throughput.md)은 서로 다른 엔드포인트를 사용합니다.

[API 참조](https://developer.adobe.com/journey-optimizer-apis/references/messaging){target="_blank"} · [코드 샘플](https://developer.adobe.com/journey-optimizer-apis/references/messaging-samples){target="_blank"} · [API 트리거 캠페인 작업](../../campaigns/api-triggered-campaigns.md)

### 외부 엔드포인트에 대한 상한 설정 및 스로틀링 {#capping-throttling}

여정이 사용자 정의 액션 또는 데이터 소스를 통해 외부 시스템을 호출할 때, 상한 설정 및 스로틀링 API는 해당 시스템의 과부하를 방지합니다. 상한 설정은 구성된 제한을 초과하는 호출을 거부하고, 스로틀링은 최대 6시간 동안 대기열에 저장합니다(프로덕션 샌드박스, 사용자 정의 액션에만 해당).

[상한 설정 API 참조](https://developer.adobe.com/journey-optimizer-apis/references/journeys-throttling){target="_blank"} · [상한 설정 API 사용](../../configuration/capping.md) · [스로틀링 API 사용](../../configuration/throttling.md)

### 추가 REST API {#more-rest-apis}

메시지 및 상한 설정 외에도 Journey Optimizer는 금지 목록 관리, 콘텐츠 템플릿, 캠페인 검색, 교정 및 오케스트레이션된 캠페인 실행을 위한 REST 엔드포인트를 제공합니다. 이러한 API는 UI에서 수동으로 처리해야 하는 작업을 자동화하는 데 유용합니다. 예를 들어 데이터 가져오기 후 주소를 일괄적으로 수신 거부하거나 외부 콘텐츠 파이프라인에서 템플릿을 동기화하는 경우에 사용할 수 있습니다.

| 필요한 작업 | API 참조 |
| ------------------- | ------------- |
| 이메일 주소 또는 도메인을 발송 대상에서 프로그래밍 방식으로 제외 | [금지 API](https://developer.adobe.com/journey-optimizer-apis/references/suppression){target="_blank"} · [금지 목록 관리](../../configuration/manage-suppression-list.md) |
| 감사 또는 외부 동기화를 위해 여정 메타데이터 검색 | [여정 API](https://developer.adobe.com/journey-optimizer-apis/references/journeys-retrieve){target="_blank"} |
| 외부 파이프라인에서 콘텐츠 템플릿 및 조각 생성 및 관리 | [콘텐츠 API](https://developer.adobe.com/journey-optimizer-apis/references/content){target="_blank"} · [템플릿](../../content-management/content-templates.md) · [조각](../../content-management/fragments.md) |
| 액션 캠페인 검색 및 필터링 | [캠페인 API](https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve){target="_blank"} |
| 캠페인 미리 보기 및 프로그래밍 방식으로 증명 전송 | [시뮬레이션 API](https://developer.adobe.com/journey-optimizer-apis/references/simulations){target="_blank"} |

>[!NOTE]
>
>시뮬레이션 API는 API 트리거 캠페인 및 액션(예약) 캠페인에 사용할 수 있습니다. **오케스트레이션된 캠페인에는 지원되지 않습니다**. 오케스트레이션된 캠페인의 경우 오케스트레이션된 캠페인 사용자 인터페이스의 미리보기 및 증명 워크플로를 사용하세요.

| 데이터 세트 유효성 검사 및 오케스트레이션된 캠페인 실행 트리거 | [데이터 세트 유효성 검사](https://developer.adobe.com/journey-optimizer-apis/references/orchestrated-campaign-dataset){target="_blank"} · [트리거](https://developer.adobe.com/journey-optimizer-apis/references/oc-trigger){target="_blank"} · [데이터 세트 활성화](../../orchestrated/manual-schema.md) |

## 추가 리소스 {#additional-resources}

* **Developer Console**: 통합을 생성하고 API 자격 증명을 관리하기 위해 [Adobe Developer Console](https://developer.adobe.com){target="_blank"}에 액세스합니다.
* **샘플 코드**: [GitHub에서 샘플 구현](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"}을 살펴봅니다.
* **튜토리얼 비디오**: [Experience League](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=ko){target="_blank"}에서 실습 튜토리얼을 통해 학습합니다.
* **개발자 커뮤니티**: Adobe 커뮤니티 포럼에서 다른 개발자들과 소통하고 지원을 받습니다.

## 다양한 역할 간의 협업 {#next-steps}

구현 작업은 다른 팀원들과 협업하여 진행됩니다.

>[!BEGINTABS]

>[!TAB 데이터 엔지니어와 협력]

[데이터 엔지니어](data-engineer.md)와 데이터 및 이벤트 구성에 대해 협업합니다. 사용자 행동에 반응하는 모든 여정은 전송하는 이벤트에 따라 달라집니다. 데이터 엔지니어는 스키마를 정의하고, 사용자는 해당 스키마를 생성하는 코드를 구현합니다.

* 구현에 필요한 [XDM 스키마](../../data/get-started-schemas.md) 및 이벤트 구조 가져오기
* 전송해야 하는 이벤트와 필요한 페이로드 형식 이해. [여정 이벤트 작업](../../event/about-events.md)을 참조하세요.
* 각 이벤트 페이로드에서 필수 필드와 선택 필드를 확인하고, 예상 필드가 누락되거나 형식이 잘못된 경우 여정에서 발생하는 상황을 확인하려면 [스키마 요구 사항](../../event/experience-event-schema.md#schema-requirements)을 참조하세요.
* [Adobe Experience Platform Assurance](https://experienceleague.adobe.com/docs/experience-platform/assurance/home.html?lang=ko){target="_blank"}를 사용하여 이벤트 게재 및 데이터 수집을 함께 테스트

>[!TAB 관리자와 협업]

[관리자](administrator.md)와 협력하여 액세스 및 채널 구성을 진행합니다. 여정은 관리자가 설정한 채널을 통해서만 사용자에게 도달할 수 있습니다. SDK 작업과 관리자 구성이 동기화되도록 미리 조율하세요.

* 관리자가 Journey Optimizer에서 구성할 [사용자 정의 액션](../../action/about-custom-action-configuration.md)에 대한 API 사양 제공
* [Adobe Developer Console](https://developer.adobe.com){target="_blank"}을 통해 필요한 권한 및 API 자격 증명 요청
* 채널 구성 요구 사항([iOS](../../push/push-configuration.md) 및 Android용 푸시 인증서, [웹 푸시](../../push/push-configuration-web.md) 설정, [SMS 웹훅](../../mobile/mobile-webhook.md) 엔드포인트)에 대해 협의
* [여정 테스트 모드](../../building-journeys/testing-the-journey.md)를 실행하기 전에 샌드박스 전략 및 테스트 환경에 대해 협의

>[!TAB 마케터와 협업]

[마케터](marketer.md)와 협력하여 여정을 디자인 및 테스트합니다. 마케터는 전송하는 이벤트와 노출하는 화면에 전적으로 의존하는 여정과 콘텐츠를 구축합니다. 협의가 긴밀할수록 여정을 더 빠르게 출시할 수 있습니다.

* [Journey Optimizer](../../building-journeys/journey.md)에서 여정 디자인을 함께 검토하여 어떤 사용자 상호 작용이 이벤트를 트리거해야 하고 어떤 화면에 개인화가 필요한지 파악합니다
* 마케터가 [콘텐츠 성과 및 사용자 참여도](../../reports/report-gs-cja.md)를 측정할 수 있도록 추적 기능을 구현합니다.
* 테스트 프로필로 [여정 테스트 모드](../../building-journeys/testing-the-journey.md)를 함께 실행하여 전체 흐름을 엔드투엔드 방식으로 검증합니다
* 메시지 게재, 개인화 렌더링 또는 [사용자 정의 액션](../../action/action.md) 응답 관련 문제를 해결합니다.

>[!ENDTABS]

## 구현 시작

빌드를 시작할 준비가 되셨나요? 위의 섹션에서 첫 번째 구현 영역을 선택합니다.

1. **모바일 앱?** [Mobile SDK 통합](#mobile-integration)으로 시작하세요
2. **웹 사이트인가요?** [Web SDK 설정](#web-implementation)부터 시작하세요
3. **API 통합인가요?** [API 작업](#apis)으로 넘어가세요
4. **사용자 정의 시스템인가요?** [사용자 정의 액션](#custom-actions)을 확인해 보세요

각 섹션에는 구현을 안내하는 자세한 기술 문서, 코드 샘플 및 튜토리얼 링크가 포함되어 있습니다.

## 기타 역할 안내서 {#other-role-guides}

| 역할 | 안내서 |
|------|-------|
| 관리자 | [관리자를 위한 시작](administrator.md) |
| 데이터 엔지니어 | [데이터 엔지니어를 위한 시작](data-engineer.md) |
| 개발자 | [개발자를 위한 시작](developer.md) |
| 마케터 | [마케터를 위한 시작](marketer.md) |

[역할 및 책임 개요](../quick-start.md)로 돌아가기 · [시작](../../../rp_landing_pages/get-started-landing-page.md)으로 돌아가기
