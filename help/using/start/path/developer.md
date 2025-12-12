---
title: 개발자를 위한 시작
description: 데이터 엔지니어로서 Journey Optimizer로 작업하는 방법에 대해 자세히 알아봅니다.
feature: Get Started
role: Developer
level: Experienced
exl-id: 5053dd4f-d050-415f-bc74-d6d061bdcbe1
source-git-commit: 2d699fe8a3320400dad2d5d962028d6e2a5425f8
workflow-type: tm+mt
source-wordcount: '1816'
ht-degree: 2%

---

# 개발자를 위한 시작 {#get-started-developers}

**개발자**&#x200B;로서 [!DNL Adobe Journey Optimizer]을(를) 구현하고 응용 프로그램 및 시스템에 통합해야 합니다. [!DNL Adobe Journey Optimizer]시스템 관리자[&#x200B; 및 &#x200B;](administrator.md)데이터 엔지니어[가 액세스 권한을 부여하고 환경을 준비하면 &#x200B;](data-engineer.md)(으)로 작업을 시작할 수 있습니다.

## Journey Optimizer 생태계에서의 귀하의 역할

다른 팀원이 사용자 인터페이스를 통해 Journey Optimizer을 구성하는 동안 다음 사항에 집중할 수 있습니다.

* 모바일 및 웹 응용 프로그램에서 **SDK 구현**
* 여정을 트리거하기 위해 응용 프로그램에서 **이벤트 보내기**
* Journey Optimizer에서 사용자 지정 작업을 통해 호출할 수 있는 **API 끝점 빌드**
* 기존 시스템 및 인프라와 **통합** Journey Optimizer
* 구현 **테스트 및 디버깅**

[데이터 엔지니어](data-engineer.md)가 데이터 스키마, 이벤트 구성 및 데이터 원본을 처리합니다. [관리자](administrator.md)가 권한 및 채널 구성을 설정합니다. [마케터](marketer.md)가 구현을 사용하는 여정 및 콘텐츠를 디자인합니다.

이 안내서에서는 Journey Optimizer을 시작하는 데 필요한 기술 구현 단계를 다룹니다. 모바일 앱, 웹 경험 또는 API 통합 중 어느 것을 구축하든 아래 섹션에 따라 구현을 설정하십시오.

## 전제 조건 {#prerequisites}

구현을 시작하기 전에 다음을 확인하십시오.

| 카테고리 | 요구 사항 |
|----------|-------------|
| **기술 기술** | * JavaScript(웹 SDK) 또는 Swift/Kotlin(모바일 SDK)에 대한 경험<br>* RESTful API 및 JSON에 대한 이해<br>* 비동기 프로그래밍 및 이벤트 기반 아키텍처에 익숙함<br>* 조직의 애플리케이션 아키텍처에 대한 지식 |
| **액세스 및 도구** | * API 자격 증명에 대한 [Adobe Developer Console](https://developer.adobe.com){target="_blank"}에 액세스<br>* 응용 프로그램의 코드베이스에 액세스할 수 있는 개발 환경<br>* API 테스트를 위한 Postman과 같은 테스트 도구<br>* 브라우저 개발자 도구 또는 모바일 디버깅 도구 |
| **다른 팀원의** | * [관리자](administrator.md)<br>*가 부여한 환경 액세스 권한 [데이터 엔지니어](data-engineer.md)<br>*의 XDM 스키마 및 이벤트 정의 [마케터](marketer.md)의 요구 사항 및 사용 사례 |

## 기술적 토대 이해 {#technical-foundation}

구현으로 이동하기 전에 핵심 기술 개념을 숙지하십시오.

1. **Adobe Experience Platform 통합**: Journey Optimizer은 기본적으로 Adobe Experience Platform에 빌드되어 있습니다. 기본 아키텍처를 이해하면 보다 효과적인 구현을 구축하는 데 도움이 됩니다. [Journey Optimizer 작동 방식](../understanding-ajo.md)에 대해 자세히 알아보세요.

1. **XDM 데이터 모델**: Journey Optimizer은 XDM(경험 데이터 모델)을 사용하여 이벤트 및 프로필 데이터를 구조화합니다. 개발자는 [데이터 엔지니어](data-engineer.md)가 구성한 스키마를 준수하는 데이터를 보내는 방법을 이해해야 합니다. [XDM 스키마](../../data/get-started-schemas.md)에 대해 알아봅니다.

1. **인증 및 보안**: 모든 구현에는 적절한 인증이 필요합니다. SDK 및 API에 대한 인증을 설정하는 방법을 이해합니다. [API 인증](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}에 대해 알아봅니다.

## 모바일 앱 통합 설정 {#mobile-integration}

### Adobe Experience Platform Mobile SDK 구성

푸시 알림, 인앱 메시지 및 기타 모바일 기능을 활성화하려면 Adobe Experience Platform Mobile SDK을 모바일 애플리케이션에 통합합니다.

1. **Mobile SDK 설치 및 구성**: [Adobe Experience Platform Mobile SDK 설명서](https://developer.adobe.com/client-sdks/documentation/getting-started/){target="_blank"}에 따라 SDK 통합을 시작하십시오.

1. **모바일 속성을 만듭니다**: [!DNL Adobe Experience Platform Data Collection]에서 모바일 속성을 설정합니다. [모바일 속성을 만들고 구성](https://developer.adobe.com/client-sdks/documentation/getting-started/create-a-mobile-property/){target="_blank"}하는 방법을 알아보세요.

1. **푸시 알림 구성**:
   * **iOS 앱**&#x200B;의 경우: APNs(Apple 푸시 알림 서비스)에 앱을 등록합니다. 자세한 내용은 [Apple 설명서](https://developer.apple.com/documentation/usernotifications/registering_your_app_with_apns){target="_blank"}를 참조하세요.
   * **Android 앱**&#x200B;의 경우: Android 앱에 대한 Firebase Cloud Messaging을 설정합니다. 자세한 내용은 [Google 설명서](https://firebase.google.com/docs/cloud-messaging/android/client){target="_blank"}를 참조하세요.

1. **모바일 통합 테스트**: [모바일 온보딩 빠른 시작 워크플로우](../../push/mobile-onboarding-wf.md)를 사용하여 모바일 설정을 빠르게 구성하고 테스트하십시오.

푸시 알림을 구성하는 자세한 단계는 [이 페이지](../../push/push-configuration.md)에서 확인할 수 있습니다.

### 코드 기반 경험 구현(모바일 SDK)

코드 기반 경험을 사용하는 기본 모바일 앱 개인화의 경우:

* 모바일 SDK 구현의 경우 [이 자습서](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/code-based/tutorial/){target="_blank"}를 따르십시오.
* [iOS](https://github.com/adobe/aepsdk-messaging-ios/tree/main/TestApps/MessagingDemoAppSwiftUI){target="_blank"} 및 [Android](https://github.com/adobe/aepsdk-messaging-android/tree/main/code/testapp){target="_blank"}에 대한 샘플 구현 검토

## 웹 경험 구현 {#web-implementation}

### Adobe Experience Platform 웹 SDK 설정

웹 기반 구현의 경우 웹 SDK은 기본 통합 지점입니다.

1. **웹 SDK 설치**: [웹 SDK 구현 안내서](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=ko-KR){target="_blank"}에 따라 웹 사이트에서 SDK을 설정합니다.

1. **데이터스트림 구성**: Journey Optimizer이 활성화된 [!DNL Adobe Experience Platform Data Collection]에서 데이터스트림을 만들고 구성합니다. 자세한 내용은 [데이터스트림 설명서](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=ko-KR){target="_blank"}를 참조하세요.

1. **웹 푸시 알림 사용**(선택 사항): 웹 SDK 구성에서 [pushNotifications 속성](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/pushnotifications){target="_blank"}을 구성하고 [sendPushSubscription 명령](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/sendpushsubscription){target="_blank"}을(를) 사용하여 푸시 구독을 등록합니다.

### 코드 기반 경험 구현(웹 SDK)

코드 기반 경험을 통해 모든 디지털 터치포인트를 개인화할 수 있습니다.

1. **구현 방법을 선택하십시오**: 클라이언트측, 서버측 또는 하이브리드입니다. 각 접근 방식에 대한 [구현 샘플](../../code-based/code-based-implementation-samples.md)을 검토하십시오.

1. **표면 정의**: 응용 프로그램에서 개인화된 콘텐츠를 전달할 위치를 식별합니다. [표면 구성](../../code-based/code-based-surface.md)에 대해 알아봅니다.

1. **컨텐츠 렌더링 구현**: 웹 SDK을 사용하여 개인화 컨텐츠를 가져오고 적용하십시오. [코드 기반 구현 자습서](../../code-based/code-based-decisioning-implementations.md)를 참조하십시오.

1. **디스플레이 및 상호 작용 이벤트 보내기**: 콘텐츠가 표시되는 시기와 사용자가 분석 및 최적화를 위해 상호 작용하는 시기를 추적합니다.

코드 기반 경험이 작동하는지 확인하려면 [GitHub의 샘플 구현](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"}을 살펴보십시오.

[코드 기반 경험 시작하기](../../code-based/get-started-code-based.md)에 대해 자세히 알아보세요.

## 이벤트 스트리밍 구현 {#event-streaming}

### 여정을 트리거할 이벤트 보내기

개발자는 여정을 트리거하는 이벤트를 전송하는 코드를 구현합니다. [데이터 엔지니어](data-engineer.md)가 Journey Optimizer에서 이벤트 스키마와 정의를 구성합니다.

1. **이벤트 페이로드 이해**: 데이터 엔지니어와 협력하여 이벤트 스키마와 필요한 페이로드 구조를 가져옵니다. 페이로드는 구성한 XDM 스키마를 준수해야 합니다. [이벤트 스키마 요구 사항](../../event/experience-event-schema.md)에 대해 알아봅니다.

1. **이벤트 스트리밍 구현**: [수집 API 스트리밍](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=ko){target="_blank"}을 사용하여 Adobe Experience Platform에 이벤트를 보냅니다. 이벤트를 보내는 [단계](../../event/additional-steps-to-send-events-to-journey.md)를 알아보세요.

1. **이벤트 유형 처리**:
   * **단일 이벤트**: 사용자별 작업(예: 단추 클릭, 구매 완료)에 대한 이벤트 전송을 구현합니다.
   * **비즈니스 이벤트**: 비즈니스 관련 이벤트(예: 재고 업데이트, 가격 변경) 보내기

1. **여정 배달 테스트**: 이벤트가 제대로 수신되었는지 확인하고 예상대로 이벤트를 트리거하십시오. [이벤트 문제 해결](../../building-journeys/troubleshooting-inbound.md)에 대해 알아봅니다.

API를 통해 이벤트를 전송하기 위한 **예제 구현**:

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

## 사용자 지정 작업 엔드포인트 개발 {#custom-actions}

여정 지정 작업을 사용하면 사용자가 API를 호출할 수 있습니다. 개발자는 사용자 지정 작업에서 호출하는 API 끝점을 빌드합니다.

1. **API 끝점 빌드**: 여정 실행 중에 Journey Optimizer에서 호출할 RESTful API 끝점을 만듭니다. 엔드포인트는 다음과 같아야 합니다.
   * JSON 페이로드 수락
   * 요청 인증(OAuth, API 키 또는 JWT)
   * 적절한 시간 제한 내에 요청 처리
   * 예상 형식의 응답 반환

1. **사용자 지정 작업 기능 이해**: 사용자 지정 작업은 Epsilon, Slack, Firebase 또는 자체 서비스와 같은 서드파티 시스템에 연결할 수 있습니다. [사용자 지정 작업](../../action/action.md)에 대해 자세히 알아보세요.

1. **작업 구성을 사용하여 작업**: [관리자](administrator.md) 또는 [데이터 엔지니어](data-engineer.md)가 Journey Optimizer에서 API 끝점 URL, 인증 방법 및 매개 변수를 정의하는 사용자 지정 작업을 구성합니다. API 사양을 제공합니다. [사용자 지정 작업 구성](../../action/about-custom-action-configuration.md)에 대해 알아봅니다.

1. **실행 가능한 데이터 반환**: 후속 여정 단계에서 사용할 수 있는 데이터를 반환하도록 API를 디자인합니다. [작업 응답](../../action/action-response.md)에 대해 알아봅니다.

1. **속도 제한 구현**: 끝점이 예상 볼륨을 처리할 수 있는지 확인하십시오. Journey Optimizer은 5000 호출/초 제한을 적용하지만 시스템이 복원력이 있어야 합니다. [제한 및 조절](../../configuration/external-systems.md)에 대해 알아봅니다.

**사용 사례**&#x200B;의 예: [사용자 지정 작업을 사용하여 Experience Platform에 여정 이벤트 작성](../../building-journeys/custom-action-aep.md).

## Journey Optimizer API 작업 {#apis}

Journey Optimizer은 프로그래밍 방식 액세스를 위한 포괄적인 REST API를 제공합니다.

1. **API 기능 이해**: Journey Optimizer API를 사용하면 다양한 리소스를 프로그래밍 방식으로 만들고, 읽고, 업데이트하고, 삭제할 수 있습니다. [Journey Optimizer API](../../configuration/ajo-apis.md)에 대해 알아봅니다.

1. **인증**: [이 자습서](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}에 따라 Adobe Developer Console을 사용하여 API 인증을 설정하십시오.

1. **API 참조 살펴보기**: 전체 API 설명서를 찾아보고 [Adobe Journey Optimizer API 참조](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"}에서 직접 API를 사용해 보십시오.

1. **API 트리거 캠페인**: API 트리거 캠페인을 사용하여 트랜잭션 메시지를 작성합니다. 대량 시나리오(최대 5000TPS)의 경우 [높은 처리량 모드](../../campaigns/api-triggered-high-throughput.md)를 탐색하십시오(추가 라이선스 필요).

1. **의사 결정 관리 API**: 오퍼 관리 및 의사 결정에 특수 API를 사용합니다. 자세한 내용은 [의사 결정 관리 API 안내서](../../offers/api-reference/getting-started.md)를 참조하세요.

## 테스트 및 디버깅 {#testing}

1. **SDK 구현 디버깅**: Adobe Experience Platform Assurance을 사용하여 SDK 이벤트를 검사하고, 데이터 수집을 확인하고, 통합 문제를 실시간으로 해결할 수 있습니다. [Assurance에 대해 자세히 알아보기](https://experienceleague.adobe.com/docs/experience-platform/assurance/home.html){target="_blank"}.

1. **여정 배달 테스트**: 응용 프로그램의 이벤트가 Adobe Experience Platform에서 올바르게 수신되는지 확인하고 예상대로 이벤트를 트리거합니다. 이벤트 수집을 모니터링하고 페이로드 구조를 확인합니다.

1. **API 통합 유효성 검사**: 사용자 지정 작업 끝점을 테스트하여 Journey Optimizer 요청을 올바르게 처리하고, 시간 제한 내에 응답하고, 예상 데이터 형식을 반환하는지 확인하십시오.

1. **테스트 프로필과 함께 테스트 모드 사용**: [데이터 엔지니어](data-engineer.md)와(과) 협력하여 테스트 프로필에 액세스한 다음 여정 테스트 모드를 사용하여 구현의 유효성을 검사하십시오. [여정 테스트](../../building-journeys/testing-the-journey.md)하는 방법을 알아보세요.

1. **SDK 로그 모니터링**: SDK 구현에서 디버그 로깅을 사용하여 개발 중 문제를 해결합니다.
   * **Mobile SDK**: 로깅을 사용하여 SDK 이벤트 및 API 호출을 볼 수 있습니다.
   * **웹 SDK**: 브라우저 콘솔을 사용하여 SDK 활동을 모니터링합니다.

1. **데이터 스트림 구성 확인**: 데이터 스트림이 Journey Optimizer에 데이터를 보내도록 올바르게 구성되어 있는지 확인하십시오. 이벤트가 데이터 스트림을 통해 올바른 대상으로 이동하는지 확인하십시오.

1. **분석을 위한 여정 데이터 쿼리**: 데이터 레이크에서 SQL 쿼리를 사용하여 여정 단계 이벤트를 분석하고, 문제를 디버깅하고, 사용자 지정 작업 성능을 모니터링합니다. 다음을 포함하여 [여정 분석을 위한 쿼리 예제](../../reports/query-examples.md)를 살펴보십시오.
   * 프로필 시작/종료 추적 및 무시 이유
   * 사용자 지정 작업 성능 지표(지연, 처리량, 오류)
   * 이벤트 전달 및 오류 패턴
   * 여정 인스턴스 상태

## 고급 개발자 항목 {#advanced-topics}

### 상황별 데이터 및 데이터 보강 작업

* **배열 반복**: Handlebars 구문을 사용하여 메시지의 이벤트, 사용자 지정 작업 응답 및 데이터 집합 조회의 동적 목록을 표시합니다. [컨텍스트 데이터 반복](../../personalization/iterate-contextual-data.md)에 대해 알아봅니다.
* **데이터 집합 조회**: 데이터 집합 조회를 구현하여 Adobe Experience Platform 데이터 집합에서 여정 데이터를 보강합니다. 구성에 대해 데이터 엔지니어와 협력합니다. [데이터 집합 조회](../../building-journeys/dataset-lookup.md)에 대해 알아봅니다.

### 동의 및 거버넌스 작업

통합에서 데이터 거버넌스 및 동의 정책 구현:

* **데이터 거버넌스**: 사용자 지정 작업에 데이터 사용 정책을 적용합니다. [데이터 거버넌스](../../action/action-privacy.md)에 대해 자세히 알아보세요.
* **동의 관리**: 구현에서 고객 동의 환경 설정을 처리합니다. [동의](../../action/consent.md)에 대해 알아봅니다.

### 최적화 및 모범 사례

* **제한 및 조절**: 속도 제한을 이해하고 적절한 조절을 구현합니다. [외부 시스템](../../configuration/external-systems.md)에 대해 알아봅니다.
* **여정 최적화**: [여정 최적화](../../building-journeys/optimize.md)에 대한 모범 사례를 따르십시오.
* **오류 처리**: 강력한 오류 처리를 구현합니다. [오류 코드](../../building-journeys/error-codes-reference.md) 및 [문제 해결 가이드](../../building-journeys/troubleshooting.md)를 검토하십시오.

## 추가 리소스 {#additional-resources}

* **Developer Console**: [Adobe Developer Console](https://developer.adobe.com){target="_blank"}에 액세스하여 통합을 만들고 API 자격 증명을 관리합니다.
* **샘플 코드**: [GitHub에서 샘플 구현 살펴보기](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"}.
* **튜토리얼 비디오**: [Experience League](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=ko){target="_blank"}에서 실습형 튜토리얼을 통해 알아봅니다.
* **개발자 커뮤니티**: 다른 개발자와 연결하고 Adobe 커뮤니티 포럼에서 지원을 받으십시오.

## 여러 역할에 걸쳐 공동 작업 {#next-steps}

구현 작업이 다른 팀 구성원과 교차합니다.

>[!BEGINTABS]

>[!TAB 데이터 엔지니어와 작업]

데이터 및 이벤트 구성에 대해 [데이터 엔지니어](data-engineer.md)와(과) 공동 작업:

* 구현해야 하는 XDM 스키마 및 이벤트 구조 가져오기
* 전송해야 하는 이벤트와 해당 페이로드 형식을 이해합니다.
* 데이터 수집 요구 사항 및 데이터 품질 표준 조정
* 이벤트 전달 및 데이터 수집 함께 테스트

>[!TAB 관리자 작업]

액세스 및 구성에 대해 [관리자](administrator.md)와(과) 공동 작업:

* 사용자가 구성할 사용자 지정 작업에 대한 API 사양 제공
* 필요한 권한 및 API 자격 증명 요청
* 채널 구성 요구 사항(예: 푸시 인증서) 조정
* 테스트 환경 및 샌드박스 전략에 맞게 조정

>[!TAB 마케터와 함께 작업]

여정 요구 사항 및 테스트에 대해 [마케터](marketer.md)와 공동 작업:

* 이벤트를 트리거해야 하는 사용자 상호 작용 이해
* 컨텐츠 성능 및 사용자 참여를 위한 추적 구현
* 구현된 기능이 포함된 여정 테스트 지원
* 메시지 게재 또는 개인화 문제 해결

>[!ENDTABS]

## 구현 시작

빌드를 시작할 준비가 되셨습니까? 위의 섹션에서 첫 번째 구현 영역을 선택합니다.

1. **모바일 앱?** [Mobile SDK 통합 시작](#mobile-integration)
2. **웹 사이트** [웹 SDK 설치](#web-implementation) 시작
3. **API 통합** [API 작업](#apis)(으)로 이동
4. **사용자 지정 시스템입니까?** [사용자 지정 작업](#custom-actions) 체크 아웃

각 섹션에는 구현을 안내하는 자세한 기술 설명서, 코드 샘플 및 튜토리얼에 대한 링크가 포함되어 있습니다.
