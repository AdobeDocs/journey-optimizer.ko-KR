---
solution: Journey Optimizer
product: journey optimizer
title: 공급업체 통합
description: 유효한 API를 노출하는 외부 플랫폼과 Adobe Journey Optimizer 통합 및 설정을 디자인할 때 신뢰할 수 있도록 엔지니어링 테스트를 거친 공급업체 패턴을 사용합니다.
feature: Integrations
topic: Content Management
role: User
level: Intermediate
hide: true
keywords: 통합, 공급업체, 서드파티
source-git-commit: 16eb46843d0369ae14f004a5e0f9e743cad3170b
workflow-type: tm+mt
source-wordcount: '9348'
ht-degree: 5%

---

# 샘플 공급업체 구성 {#vendor-integration}

>[!BEGINSHADEBOX]

목차:

* [통합 작업](integrations.md)
* [공급업체 통합 시작](vendor-integration-gs.md)
* **[공급업체 구성 샘플](vendor-integration.md)**
* [FAQ](vendor-integration-faq.md)

>[!ENDSHADEBOX]

>[!BEGINSHADEBOX]

고객 및 서드파티 공급자는 보안 및 규정 준수 요구 사항에 필요한 API 종단점을 보호할 책임이 있습니다.

>[!ENDSHADEBOX]

## Content 및 CMS {#content-and-cms}

### 만족해 {#contentful}

>[!BEGINSHADEBOX]

Contents는 REST 또는 GraphQL보다 구조화된 항목 및 에셋을 위한 Headless CMS이므로 Journey Optimizer은 전송 또는 열기 시 콘텐츠를 가져올 수 있습니다.

일반적인 사용 사례에는 현지화된 히어로 블록, 대체 텍스트 및 이메일의 CTA와 동적 모듈의 제품 또는 프로모션 항목이 포함됩니다. 또 다른 일반적인 패턴은 개인화된 메시징을 위해 ID별로 특정 항목을 검색하는 것입니다.

>[!ENDSHADEBOX]

+++ Contentable을 위한 사전 요구 사항 및 제한 사항에 대해 자세히 알아보십시오.

다음 전제 조건이 적용됩니다.

* 게재 API 액세스 및 읽기 중심 API 키를 사용하는 콘텐츠 공간.
* 컨텐츠 유형 및 필드 ID를 지웁니다. 통합을 만들려면 Journey Optimizer에서 관리자 액세스 권한이 필요합니다.


다음 제한 사항 및 제외가 적용됩니다.

* 광범위한 목록 또는 페이지가 매겨진 콘텐츠풀 API는 이 패턴에 적합하지 않습니다. 특정 항목이나 자산을 대상으로 하는 검색 호출을 선호합니다.
* 쓰기 되돌리기 또는 양방향 동기화는 이 예제의 범위를 벗어납니다.

+++

아래 절차를 사용하여 Journey Optimizer에서 이 통합을 구성합니다. 요청 세부 정보는 **샘플 통합 필드**&#x200B;를 참조하고 해당 환경에 대한 공급업체 설명서를 통해 해당 값을 확인하십시오.

1. [통합 작업](integrations.md)을 따르십시오. 콘텐츠 배달 API 및 배달 토큰을 사용하여 **GET**&#x200B;을(를) 구성하고, 샘플 JSON을 붙여넣고, 필드를 매핑하고, 테스트하고, 활성화하십시오.

1. Journey Optimizer에서 **[!UICONTROL 구성]** > **[!UICONTROL 관리]**(으)로 이동한 다음 **[!UICONTROL 통합 만들기]**&#x200B;를 선택합니다.

1. 통합 이름을 공백 없이 입력하십시오.

1. CDA(콘텐츠 배달 API) URL을 사용하여 끝점을 구성합니다. `https://cdn.contentful.com/spaces/{space_id}/environments/{environment_id}/entries/{entry_id}`

1. HTTP 메서드 **GET**&#x200B;을(를) 선택하십시오.

1. 인증을 추가합니다. 아래 **샘플 통합 필드**&#x200B;와 같이 **`access_token`** **쿼리** 매개 변수를 콘텐츠 배달 API 토큰으로 설정합니다. 콘텐트도 `Authorization: Bearer` 헤더에서 동일한 토큰을 수락합니다. 통합 필드에서 지원하는 모든 항목을 사용하십시오.

1. 필요한 경우 경로 변수(예: 항목 ID, 로케일)를 추가합니다.

1. 필드를 감지하고 매핑할 수 있도록 샘플 JSON 응답을 붙여 넣습니다.

1. 개인화에 필요한 필드를 선택합니다.

1. 필요에 따라 시간 제한 및 캐싱을 구성합니다.

1. 연결 테스트 및 활성화.

아래 표에는 이 통합 요청에 대한 예제 값이 나와 있습니다.

+++ 샘플 통합 필드

샘플 통합 필드(스페이스 및 환경에 대한 [콘텐츠 배달 API](https://www.contentful.com/developers/docs/references/content-delivery-api/){target="_blank"}에 맞게 조정):

| 필드 | 값 |
| -- | -- |
| **URL** | `https://cdn.contentful.com/spaces/{{spaceID}}/environments/{{environment_id}}/entries/{{entry_id}}` |
| 응답 페이로드 | API 응답을 기반으로 작성 중에 사용할 응답 필드를 선택하고 구성합니다. |
| 정책 | 필요에 따라 정책 수준 세부 정보를 구성합니다. |
| **HTTP 메서드** | `GET` |

**경로 매개 변수**

| 경로 매개 변수 | 이름 | 기본 값 |
| --- | --- | --- |
| `spaceID` | `spaceID` | `<YOUR_SPACE_ID>` |
| `environment_id` | `environment_id` | `<YOUR_ENV_ID>` |
| `entry_id` | `entry_id` | `<YOUR_ENTRY_ID>` |

**머리글**

| 매개 변수 | 이름 | 유형 | 값 | 필수 |
| --- | --- | --- | --- | --- |
| Content-Type(기본값) | Content-Type | 상수 | application/json | 예(켜기) |

**인증**

| 유형 | API 키 이름 | API 키 값 | 위치 |
| --- | --- | --- | --- |
| API 키 | `access_token` | `<YOUR_API_KEY>` | 쿼리 매개 변수 |

+++

### Sitecore {#sitecore}

>[!BEGINSHADEBOX]

Sitecore Content Hub 및 관련 클라우드 API는 DAM 스타일의 다운로드 및 메타데이터 흐름을 지원합니다. 아래 예제 패턴은 ID별 다운로드 순서에 중점을 둡니다.

일반적인 사용 사례에는 이메일 콘텐츠의 에셋 또는 다운로드 메타데이터와 Sitecore에서 관리되는 DAM 워크플로우와의 정렬이 포함됩니다.

>[!ENDSHADEBOX]

+++ Sitecore에 대한 사전 요구 사항 및 제한 사항에 대해 자세히 알아보십시오.

다음 전제 조건이 적용됩니다.

* 테넌트 URL 및 자격 증명(API 표면당 전달자 또는 토큰).
* 통합을 만들기 위한 Journey Optimizer의 관리자 액세스 권한.

다음 제한 사항 및 제외가 적용됩니다.

* 호스트 이름과 경로는 Sitecore 제품에 따라 다릅니다. 테넌트가 노출하는 엔드포인트만 사용합니다.
* OAuth 액세스 토큰, 새로 고침 및 수명은 Sitecore 보안 정책을 따라야 합니다.

+++

아래 절차를 사용하여 Journey Optimizer에서 이 통합을 구성합니다. 요청 세부 정보는 **샘플 통합 필드**&#x200B;를 참조하고 해당 환경에 대한 공급업체 설명서를 통해 해당 값을 확인하십시오.

1. [통합 작업](integrations.md)을 따르십시오. 다운로드 순서 경로에서 **GET**&#x200B;을(를) 구성하고, 사이트코어별 권한 부여 헤더를 설정하고, 컨텍스트에서 `id`을(를) 매핑하고, 샘플 JSON을 붙여넣고, 필드를 매핑하고, 자산 지연 시간을 조정하십시오.

1. Journey Optimizer에서 **[!UICONTROL 구성]** > **[!UICONTROL 관리]**(으)로 이동한 다음 **[!UICONTROL 통합 만들기]**&#x200B;를 선택합니다.

1. 통합 이름을 공백 없이 입력하십시오.

1. Content Hub API를 사용하여 끝점을 구성합니다(예: ID별 다운로드 순서). 예제 URL 패턴:

   `https://xmapps-api.sitecorecloud.io/api/v1/downloadorders/{id}`

1. 별도로 명시되지 않는 한 구성 테이블에 표시된 HTTP 메서드(일반적으로 GET)를 선택합니다.

1. 표 및 공급업체 설명서에 지정된 대로 인증(헤더, 쿼리 매개 변수 또는 OAuth)을 구성합니다.

1. 경로, 쿼리 및 헤더 매개 변수를 정의하고 필요한 경우 프로필 또는 컨텍스트 데이터에 변수를 매핑합니다.

1. 필드를 감지하고 매핑할 수 있도록 샘플 JSON 응답을 붙여 넣습니다.

1. 응답 페이로드 매핑에서 개인화에 필요한 필드를 선택합니다.

1. 예상 볼륨을 기반으로 시간 제한, 재시도 및 캐싱 정책을 구성합니다.

1. 연결을 테스트한 다음 통합을 활성화합니다.

아래 표에는 이 통합 요청에 대한 예제 값이 나와 있습니다.

+++ 샘플 통합 필드

Journey Optimizer에서 이 샘플 호출을 구성할 때 다음 필드를 사용하십시오. [Sitecore 설명서](https://doc.sitecore.com/){target="_blank"}에서 제품(Content Hub, XM Cloud 등)의 호스트 이름과 API 버전을 확인합니다.

| 필드 | 값 |
| --- | --- |
| **URL** | `https://xmapps-api.sitecorecloud.io/api/v1/downloadorders/{{id}}` |
| **HTTP 메서드** | `GET` |
| 응답 페이로드 | API 응답을 기반으로 작성 중에 사용할 응답 필드를 선택하고 구성합니다. |
| 정책 | 필요에 따라 정책 수준 세부 정보를 구성합니다. |

**경로 매개 변수**

| 경로 매개 변수 | 이름 | 기본 값 |
| --- | --- | --- |
| `id` | `id` | `<id_of_download_order>` |

**머리글**

| 매개 변수 | 이름 | 유형 | 값 | 필수 |
| --- | --- | --- | --- | --- |
| Content-Type(기본값) | Content-Type | 상수 | application/json | 예(켜기) |
| Authorization | Authorization | 상수 | 전달자 `<token>` | 예(켜기) |
| If-Modified-Since | If-Modified-Since | 변수 | 2019-08-24T14:15:22Z | 아니요(해제) |

**인증**

| 유형 | API 키 이름 | API 키 값 | 위치 |
| --- | --- | --- | --- |
| API 키 | X-Auth-Token | `<token>` | Header |

+++

### 살시피 {#salsify}

>[!BEGINSHADEBOX]

Salsify는 제품, 채널 및 디지털 에셋에 대한 API가 있는 PIM입니다.

일반적인 사용 사례에는 신디케이트된 카탈로그 데이터와 연계된 이메일 및 메시지의 제품 속성 또는 미디어 URL이 포함됩니다.

>[!ENDSHADEBOX]

+++ Salsify의 사전 요구 사항 및 제한 사항에 대해 자세히 알아보십시오.

다음 전제 조건이 적용됩니다.

* API 토큰 및 조직 컨텍스트. 프로필 또는 컨텍스트에서 확인할 수 있는 제품 ID.
* Journey Optimizer의 관리자 액세스 권한.

다음 제한 사항 및 제외가 적용됩니다.

* 매우 큰 카탈로그: 통합에서 엔티티별 검색이 필요한 경우 벌크 목록 끝점을 사용하지 마십시오.
* 역할 할당 권한에 의해 속성 가시성을 제한할 수 있습니다.

+++

아래 절차를 사용하여 Journey Optimizer에서 이 통합을 구성합니다. 요청 세부 정보는 **샘플 통합 필드**&#x200B;를 참조하고 해당 환경에 대한 공급업체 설명서를 통해 해당 값을 확인하십시오.

1. [통합 작업](integrations.md)을 따르십시오. 벌크 카탈로그 호출보다 단일 제품 검색을 선호하고, 전달자 인증을 설정하고, 샘플 JSON, 맵 필드, 테스트, 활성화를 붙여넣습니다.

1. Journey Optimizer에서 **[!UICONTROL 구성]** > **[!UICONTROL 관리]**(으)로 이동한 다음 **[!UICONTROL 통합 만들기]**&#x200B;를 선택합니다.

1. 통합 이름을 공백 없이 입력하십시오.

1. Salsify 제품 API를 사용하여 끝점을 구성합니다. 예제 URL 패턴:

   `https://api.salsify.com/v1/...`

1. 별도로 명시되지 않는 한 구성 테이블에 표시된 HTTP 메서드(일반적으로 GET)를 선택합니다.

1. 표 및 공급업체 설명서에 지정된 대로 인증(헤더, 쿼리 매개 변수 또는 OAuth)을 구성합니다.

1. 경로, 쿼리 및 헤더 매개 변수를 정의하고 필요한 경우 프로필 또는 컨텍스트 데이터에 변수를 매핑합니다.

1. 필드를 감지하고 매핑할 수 있도록 샘플 JSON 응답을 붙여 넣습니다.

1. 응답 페이로드 매핑에서 개인화에 필요한 필드를 선택합니다.

1. 예상 볼륨을 기반으로 시간 제한, 재시도 및 캐싱 정책을 구성합니다.

1. 연결을 테스트한 다음 통합을 활성화합니다.

아래 표에는 이 통합 요청에 대한 예제 값이 나와 있습니다.

+++ 샘플 통합 필드

일부 이전 참조가 Salsify에 다운로드 순서 스타일 경로를 다시 사용했습니다. 테넌트가 대신 `https://app.salsify.com/api/v1/orgs/{org_id}/products/{salsify_id}` 또는 유사한 항목을 사용할 수 있습니다. [개발자 정렬](https://developers.salsify.com/){target="_blank"}에서 확인하십시오.

| 필드 | 값 |
| --- | --- |
| **URL** | `https://app.salsify.com/api/v1/orgs/{{org_id}}/products/{{salsify_id}}` |
| **HTTP 메서드** | `GET` |
| **정책** | 필요에 따라 정책 수준 세부 정보를 구성합니다. |
| **응답 페이로드** | API 응답을 기반으로 작성 중에 사용할 응답 필드를 선택하고 구성합니다. |

**경로 매개 변수**

| 경로 매개 변수 | 이름 | 기본 값 |
| --- | --- | --- |
| `org_id` | `org_id` | `<org_id>` |
| `salsify_id` | `salsify_id` | `<salsify_id>` |

**머리글**

| 매개 변수 | 이름 | 유형 | 값 | 필수 |
| --- | --- | --- | --- | --- |
| Content-Type(기본 매개 변수) | Content-Type | 상수 | application/json | 예(켜기) |
| Authorization | Authorization | 상수 | `Bearer <YOUR_TOKEN_HERE>` | 예(켜기) |
| If-Modified-Since | If-Modified-Since | 변수 | 2019-08-24T14:15:22Z | 아니요(해제) |

**인증**

| 유형 | API 키 이름 | API 키 값 | 위치 |
| --- | --- | --- | --- |
| API 키 | `apiKey` | `<your_api_key>` | Header |

+++

### Contentstack {#contentstack}

>[!BEGINSHADEBOX]

Contentstack은 Headless CMS입니다. REST 게재는 Journey Optimizer에서 JSON 필드 매핑에 일반적으로 사용됩니다.

일반적인 사용 사례는 로케일이 포함된 매개 변수와 함께 배너 또는 프로모션에 항목을 사용하는 것입니다.

>[!ENDSHADEBOX]

+++ Contentstack의 사전 요구 사항 및 제한 사항에 대해 자세히 알아보십시오.

다음 전제 조건이 적용됩니다.

* 스택 API 키, 게재 토큰, 환경 이름 및 콘텐츠 유형 UID.
* Journey Optimizer의 관리자 액세스 권한.

다음 제한 사항 및 제외가 적용됩니다.

* 이 패턴은 필드 매핑에 REST JSON을 사용합니다. GraphQL 전달은 다른 통합 경로를 따릅니다.
* 프로덕션에 적합한 게재 토큰을 사용하십시오. 미리 보기와 게시된 흐름은 서로 바꿀 수 없습니다.

+++

아래 절차를 사용하여 Journey Optimizer에서 이 통합을 구성합니다. 요청 세부 정보는 **샘플 통합 필드**&#x200B;를 참조하고 해당 환경에 대한 공급업체 설명서를 통해 해당 값을 확인하십시오.

1. [통합 작업](integrations.md)을 따르십시오. Contentstack에 필요한 대로 `api_key` 및 `access_token` 헤더를 모두 추가, `environment` 쿼리 매개 변수 포함, 샘플 JSON 붙여넣기, 필드 매핑, 테스트, 활성화.

1. Journey Optimizer에서 **[!UICONTROL 구성]** > **[!UICONTROL 관리]**(으)로 이동한 다음 **[!UICONTROL 통합 만들기]**&#x200B;를 선택합니다.

1. 통합 이름을 공백 없이 입력하십시오.

1. 콘텐츠 배달 API를 사용하여 끝점을 구성합니다. 예제 URL 패턴:

   `https://cdn.contentstack.io/v3/content_types/{content_type_uid}/entries/{entry_uid}`

1. 별도로 명시되지 않는 한 구성 테이블에 표시된 HTTP 메서드(일반적으로 GET)를 선택합니다.

1. 표 및 공급업체 설명서에 지정된 대로 인증(헤더, 쿼리 매개 변수 또는 OAuth)을 구성합니다.

1. 경로, 쿼리 및 헤더 매개 변수를 정의하고 필요한 경우 프로필 또는 컨텍스트 데이터에 변수를 매핑합니다.

1. 필드를 감지하고 매핑할 수 있도록 샘플 JSON 응답을 붙여 넣습니다.

1. 응답 페이로드 매핑에서 개인화에 필요한 필드를 선택합니다.

1. 예상 볼륨을 기반으로 시간 제한, 재시도 및 캐싱 정책을 구성합니다.

1. 연결을 테스트한 다음 통합을 활성화합니다.

아래 표에는 이 통합 요청에 대한 예제 값이 나와 있습니다.

+++ 샘플 통합 필드

샘플 통합 필드. [Contentstack 콘텐츠 배달 API](https://www.contentstack.com/docs/developers/apis/content-delivery-api/){target="_blank"}를 참조하십시오.

| 필드 | 값 |
| --- | --- |
| **URL** | `https://cdn.contentstack.io/v3/content_types/{{content_type_uid}}/entries/{{entry_uid}}` |
| **HTTP 메서드** | `GET` |
| 응답 페이로드 | API 응답을 기반으로 작성 중에 사용할 응답 필드를 선택하고 구성합니다. |
| 정책 | 필요에 따라 정책 수준 세부 정보를 구성합니다. |
| 헤더 | 추가 헤더가 필요하지 않습니다. |

**경로 매개 변수**

| 경로 매개 변수 | 이름 | 기본 값 |
| --- | --- | --- |
| `content_type_uid` | 컨텐츠 유형 UID | `<your_content_type_uid>` |
| `entry_uid` | 시작 UID | `<your_entry_uid>` |

**인증**

| 키 이름 | 키 값 | 추가 |
| --- | --- | --- |
| `api_key` | `<YOUR_STACK_API_KEY>` | Header |
| `access_token` | `<YOUR_DELIVERY_TOKEN>` | Header |

Contentstack에는 게재 요청에 대한 헤더로 **둘 다** 키가 필요합니다.

**쿼리 매개 변수**

| 매개 변수 | 이름 | 유형 | 값 | 필수 |
| --- | --- | --- | --- | --- |
| `environment` | 환경 이름 | 변수 | `<your_environment_name>` | 예(켜기) |

+++

### 아케네오 {#akeneo}

>[!BEGINSHADEBOX]

Akeneo PIM은 제품, 특성 및 미디어에 REST API를 노출합니다.

일반적인 사용 사례에는 이메일 모듈의 제품 데이터 및 여정의 해당 채널에 대한 속성이 포함됩니다.

>[!ENDSHADEBOX]

+++ Akeneo에 대한 사전 요구 사항 및 제한 사항에 대해 자세히 알아보십시오.

다음 전제 조건이 적용됩니다.

* PIM 기본 URL 및 OAuth 클라이언트, 제품 UUID 또는 식별자 전략.
* Journey Optimizer의 관리자 액세스 권한.

다음 제한 사항 및 제외가 적용됩니다.

* PIM 응답이 클 수 있습니다. 개인화에 필요한 속성만 매핑합니다.
* 쓰기 작업은 일반적인 읽기 전용 개인화 예제에서 다루지 않습니다.

+++

아래 절차를 사용하여 Journey Optimizer에서 이 통합을 구성합니다. 요청 세부 정보는 **샘플 통합 필드**&#x200B;를 참조하고 해당 환경에 대한 공급업체 설명서를 통해 해당 값을 확인하십시오.

1. [통합 작업](integrations.md)을 따르십시오. 전달자 토큰과 함께 **GET**&#x200B;을(를) 사용하고, 쿼리 플래그에 필요한 속성 옵션만 요청하고, 샘플 JSON을 붙여 넣고, 최소 속성 집합을 매핑하고, 테스트하고, 활성화하십시오.

1. Journey Optimizer에서 **[!UICONTROL 구성]** > **[!UICONTROL 관리]**(으)로 이동한 다음 **[!UICONTROL 통합 만들기]**&#x200B;를 선택합니다.

1. 통합 이름을 공백 없이 입력하십시오.

1. Akeneo REST API를 사용하여 끝점을 구성합니다. 예제 URL 패턴:

   `https://{pim-host}/api/rest/v1/...`

1. 별도로 명시되지 않는 한 구성 테이블에 표시된 HTTP 메서드(일반적으로 GET)를 선택합니다.

1. 표 및 공급업체 설명서에 지정된 대로 인증(헤더, 쿼리 매개 변수 또는 OAuth)을 구성합니다.

1. 경로, 쿼리 및 헤더 매개 변수를 정의하고 필요한 경우 프로필 또는 컨텍스트 데이터에 변수를 매핑합니다.

1. 필드를 감지하고 매핑할 수 있도록 샘플 JSON 응답을 붙여 넣습니다.

1. 응답 페이로드 매핑에서 개인화에 필요한 필드를 선택합니다.

1. 예상 볼륨을 기반으로 시간 제한, 재시도 및 캐싱 정책을 구성합니다.

1. 연결을 테스트한 다음 통합을 활성화합니다.

아래 표에는 이 통합 요청에 대한 예제 값이 나와 있습니다.

+++ 샘플 통합 필드

예제 패턴: `https://{pim-host}/api/rest/v1/products-uuid/{uuid}`(`Accept: application/json` 포함). [Akeneo API](https://api.akeneo.com/){target="_blank"}를 참조하세요.

| 필드 | 값 |
| --- | --- |
| **URL** | `https://{{your-akeneo-domain}}.com/api/rest/v1/products-uuid/{{uuidProduct}}` |
| **HTTP 메서드** | `GET` |
| **정책** | 필요에 따라 정책 수준 세부 정보를 구성합니다. |
| **응답 페이로드** | API 응답을 기반으로 작성 중에 사용할 응답 필드를 선택하고 구성합니다. |

**경로 매개 변수**

| 경로 매개 변수 | 이름 | 기본 값 |
| --- | --- | --- |
| `uuidProduct` | UUID | `<product_uuid>` |

**머리글**

| 매개 변수 | 이름 | 유형 | 값 | 필수 |
| --- | --- | --- | --- | --- |
| Authorization | Authorization | 상수 | `Bearer <YOUR_TOKEN>` | 예(켜기) |
| 수락 | 수락 | 상수 | application/json | 예(켜기) |

**쿼리 매개 변수**

| 매개 변수 | 이름 | 유형 | 값 | 필수 |
| --- | --- | --- | --- | --- |
| `with_attribute_options` | 속성 옵션 포함 | 변수 | 거짓 | 아니요(해제) |
| `with_quality_scores` | 품질 점수 포함 | 변수 | 거짓 | 아니요(해제) |
| `with_completenesses` | 완성도 포함 | 변수 | 거짓 | 아니요(해제) |

**인증**

| 유형 | API 키 이름 | API 키 값 | 위치 |
| --- | --- | --- | --- |
| API 키 | Authorization | `Bearer <YOUR_ACCESS_TOKEN>` | Header |

+++

### 목련 {#magnolia}

>[!BEGINSHADEBOX]

Magnolia는 배포에 따라 헤드리스 및 REST 게재 엔드포인트를 제공합니다.

일반적인 사용 사례는 마케팅 모듈용 콘텐츠 노드 또는 조각을 전달하는 것입니다.

>[!ENDSHADEBOX]

+++ Magnolia의 사전 요구 사항 및 제한 사항에 대해 자세히 알아보십시오.

다음 전제 조건이 적용됩니다.

* 인스턴스 URL 및 토큰 또는 기본 인증, 게재할 작업 공간 및 경로.
* Journey Optimizer의 관리자 액세스 권한.

다음 제한 사항 및 제외가 적용됩니다.

* REST 게재 URL은 설치된 Magnolia 모듈 및 구성에 따라 다릅니다.

+++

아래 절차를 사용하여 Journey Optimizer에서 이 통합을 구성합니다. 요청 세부 정보는 **샘플 통합 필드**&#x200B;를 참조하고 해당 환경에 대한 공급업체 설명서를 통해 해당 값을 확인하십시오.

1. [통합 작업](integrations.md)을 따르십시오. 모듈이 노출하는 공개 게재 URL 패턴 사용, 목련당 인증 지침(보호되는 콘텐츠의 익명 게재와 토큰), 샘플 JSON 붙여넣기, 필드 매핑, 테스트, 활성화.

1. Journey Optimizer에서 **[!UICONTROL 구성]** > **[!UICONTROL 관리]**(으)로 이동한 다음 **[!UICONTROL 통합 만들기]**&#x200B;를 선택합니다.

1. 통합 이름을 공백 없이 입력하십시오.

1. Magnolia REST(게재)를 사용하여 끝점을 구성합니다. 예제 URL 패턴:

   `https://{author-or-public}/.rest/delivery/...`

1. 별도로 명시되지 않는 한 구성 테이블에 표시된 HTTP 메서드(일반적으로 GET)를 선택합니다.

1. 표 및 공급업체 설명서에 지정된 대로 인증(헤더, 쿼리 매개 변수 또는 OAuth)을 구성합니다.

1. 경로, 쿼리 및 헤더 매개 변수를 정의하고 필요한 경우 프로필 또는 컨텍스트 데이터에 변수를 매핑합니다.

1. 필드를 감지하고 매핑할 수 있도록 샘플 JSON 응답을 붙여 넣습니다.

1. 응답 페이로드 매핑에서 개인화에 필요한 필드를 선택합니다.

1. 예상 볼륨을 기반으로 시간 제한, 재시도 및 캐싱 정책을 구성합니다.

1. 연결을 테스트한 다음 통합을 활성화합니다.

아래 표에는 이 통합 요청에 대한 예제 값이 나와 있습니다.

+++ 샘플 통합 필드

예제 패턴: `https://{domain}/magnoliaAuthor/.rest/delivery/...` 또는 공용 게재 둘러보기 스타일 URL. 경로는 설치된 모듈에 따라 다릅니다. [목련 설명서](https://docs.magnolia-cms.com/){target="_blank"}를 참조하세요.

| 필드 | 값 |
| --- | --- |
| **URL** | `http://{{your-domain}}/magnoliaAuthor/.rest/delivery/<myEndpoint>/travel/@nodes` |
| **HTTP 메서드** | `GET` |
| **정책** | 필요에 따라 정책 수준 세부 정보를 구성합니다. |
| **응답 페이로드** | API 응답을 기반으로 작성 중에 사용할 응답 필드를 선택하고 구성합니다. |

**머리글**

| 매개 변수 | 이름 | 유형 | 값 | 필수 |
| --- | --- | --- | --- | --- |
| Content-Type | Content-Type | 상수 | application/json | 예(켜기) |
| 수락 | 수락 | 상수 | application/json | 예(켜기) |

**인증**

| 유형 | API 키 이름 | API 키 값 | 위치 |
| --- | --- | --- | --- |
| API 키 | Authorization | `<bearer_token>` | Header |

참고: 배달 API는 로그인이 필요하지 않은 콘텐츠에 대해 rest-anonymous 역할을 사용하는 것입니다. 보호된 데이터에 대한 보안 액세스를 위해서는 API 토큰 또는 OAuth 2.0과 같은 보다 강력한 방법이 선호됩니다.

+++


## 충성도 및 보상 {#loyalty-and-rewards}

### 부셰리피 {#voucherify}

>[!BEGINSHADEBOX]

Voucherify는 프로모션 및 충성도 REST API(캠페인, 바우처, 충성도 프로그램)를 제공합니다.

일반적인 사용 사례에는 콘텐츠의 오퍼에 대한 충성도 또는 프로모션 상태를 읽고 적절한 경우 계층 또는 균형을 표시하는 작업이 포함됩니다.

>[!ENDSHADEBOX]

+++ Voucherify에 대한 사전 요구 사항 및 제한 사항에 대해 자세히 알아보십시오.

다음 전제 조건이 적용됩니다.

* 애플리케이션 ID 및 암호(지역/클러스터당), 충성도 또는 캠페인 엔드포인트를 호출하는 명확성.
* Journey Optimizer의 관리자 액세스 권한.

다음 제한 사항 및 제외가 적용됩니다.

* 고객용 오류 또는 메시지 콘텐츠에서 내부 프로모션 또는 캠페인 식별자를 노출하지 마십시오.
* 애플리케이션 수준 요율 제한이 적용됩니다. Voucherify 지침에 따라 다시 시도 및 캐싱을 구성합니다.

+++

아래 절차를 사용하여 Journey Optimizer에서 이 통합을 구성합니다. 요청 세부 정보는 **샘플 통합 필드**&#x200B;를 참조하고 해당 환경에 대한 공급업체 설명서를 통해 해당 값을 확인하십시오.

1. [통합 작업](integrations.md)을 따르십시오. 클러스터의 기본 URL을 설정하고, 필수 헤더(`X-APP-ID`, `X-APP-TOKEN`)를 추가하고, 필터 또는 ID로 목록 끝점을 제한하고, 샘플 JSON을 붙여 넣고, 필드를 매핑하고, 테스트하고, 활성화합니다.

1. Journey Optimizer에서 **[!UICONTROL 구성]** > **[!UICONTROL 관리]**(으)로 이동한 다음 **[!UICONTROL 통합 만들기]**&#x200B;를 선택합니다.

1. 통합 이름을 공백 없이 입력하십시오.

1. 충성도/REST API를 사용하여 끝점을 구성합니다. [Voucherify](https://docs.voucherify.io/){target="_blank"}에 따라 해당 지역의 **클러스터** 호스트 및 경로를 설정하십시오. 예제 URL 패턴:

   `https://{cluster}.voucherify.io/`

1. 별도로 명시되지 않는 한 구성 테이블에 표시된 HTTP 메서드(일반적으로 GET)를 선택합니다.

1. 표 및 공급업체 설명서에 지정된 대로 인증(헤더, 쿼리 매개 변수 또는 OAuth)을 구성합니다.

1. 경로, 쿼리 및 헤더 매개 변수를 정의하고 필요한 경우 프로필 또는 컨텍스트 데이터에 변수를 매핑합니다.

1. 필드를 감지하고 매핑할 수 있도록 샘플 JSON 응답을 붙여 넣습니다.

1. 응답 페이로드 매핑에서 개인화에 필요한 필드를 선택합니다.

1. 예상 볼륨을 기반으로 시간 제한, 재시도 및 캐싱 정책을 구성합니다.

1. 연결을 테스트한 다음 통합을 활성화합니다.

아래 표에는 이 통합 요청에 대한 예제 값이 나와 있습니다.

+++ 샘플 통합 필드

샘플 통합 필드. 전체 참조: [Voucherify API](https://docs.voucherify.io/reference/introduction){target="_blank"}.

| 필드 | 값 |
| --- | --- |
| **URL** | `https://{{cluster}}.voucherify.io/v1/loyalties/{{campaignId}}/members` |
| **HTTP 메서드** | `GET` |
| 응답 페이로드 | API 응답을 기반으로 작성 중에 사용할 응답 필드를 선택하고 구성합니다. |
| 정책 | 필요에 따라 정책 수준 세부 정보를 구성합니다. |

**경로 매개 변수**

| 경로 매개 변수 | 이름 | 기본 값 |
| --- | --- | --- |
| `cluster` | `cluster` | `<your_cluster>` |
| `campaignId` | `campaignId` | `<loyalty_campaign_Id>` |

**머리글**

| 매개 변수 | 이름 | 유형 | 값 | 필수 |
| --- | --- | --- | --- | --- |
| Content-Type(기본값) | Content-Type | 상수 | application/json | 예(켜기) |
| X-APP-ID | X-APP-ID | 상수 | `<YOUR-APP-ID>` | 예(켜기) |
| X-Voucherify-채널 | X-Voucherify-채널 | 상수 | Voucherify 설명서 | 아니요(해제) |

**쿼리 매개 변수**

| 매개 변수 | 이름 | 유형 | 값 | 필수 |
| --- | --- | --- | --- | --- |
| `limit` | `limit` | 변수 | 10 | 아니요(해제) |
| `page` | `page` | 변수 | 1 | 아니요(해제) |
| `customer` | `customer` | 변수 | `<customer_identifier>` | 아니요(해제) |
| `created_at` | `created_at` | 변수 | `<iso8601_date>` | 아니요(해제) |
| `updated_at` | `updated_at` | 변수 | `<iso8601_date>` | 아니요(해제) |
| `order` | `order` | 변수 | `<sort_field>` | 아니요(해제) |
| `code` | `code` | 변수 | `<loyalty_card_code>` | 아니요(해제) |
| `ids` | `ids` | 변수 | `<array_of_ids>` | 아니요(해제) |

**인증**

| 유형 | API 키 이름 | API 키 값 | 위치 |
| --- | --- | --- | --- |
| API 키 | X-APP-TOKEN | `<YOUR-APP-TOKEN>` | Header |

+++

### 탈론 {#talon-one}

>[!BEGINSHADEBOX]

Talon.One은 세션, 효과 및 프로필에 대한 REST API가 있는 프로모션 및 충성도 규칙 엔진입니다.

일반적인 사용 사례에는 개인화된 콘텐츠의 장바구니 또는 프로필 수준에서의 프로모션과 충성도 진행 상황 또는 보상 표시가 포함됩니다.

>[!ENDSHADEBOX]

+++ Talon.One에 대한 사전 요구 사항 및 제한 사항에 대해 자세히 알아보십시오.

다음 전제 조건이 적용됩니다.

* API 키 및 배포별 기본 URL, 애플리케이션 또는 캠페인 범위에 대한 식별자.
* Journey Optimizer의 관리자 액세스 권한.

다음 제한 사항 및 제외가 적용됩니다.

* 세션 사용량이 많은 흐름은 통합 요청 모델에 신중하게 매핑해야 할 수 있습니다.
* Talon.One의 속도 제한 및 역가 지침을 준수하십시오.

+++

아래 절차를 사용하여 Journey Optimizer에서 이 통합을 구성합니다. 요청 세부 정보는 **샘플 통합 필드**&#x200B;를 참조하고 해당 환경에 대한 공급업체 설명서를 통해 해당 값을 확인하십시오.

1. [통합 작업](integrations.md)을 따르십시오. 필요한 프로필 또는 도전 과제 경로에 **GET**&#x200B;을(를) 사용하고, `Authorization: ApiKey-v1 <key>`을(를) 문서화된 대로 설정하고, 샘플 JSON을 붙여 넣고, 필드를 매핑하고, 테스트하고, 활성화하십시오.

1. Journey Optimizer에서 **[!UICONTROL 구성]** > **[!UICONTROL 관리]**(으)로 이동한 다음 **[!UICONTROL 통합 만들기]**&#x200B;를 선택합니다.

1. 통합 이름을 공백 없이 입력하십시오.

1. Talon.One 통합 API를 사용하여 끝점을 구성합니다. 예제 URL 패턴:

   `https://{your-domain}.talon.one/v1/...`

1. 별도로 명시되지 않는 한 구성 테이블에 표시된 HTTP 메서드(일반적으로 GET)를 선택합니다.

1. 표 및 공급업체 설명서에 지정된 대로 인증(헤더, 쿼리 매개 변수 또는 OAuth)을 구성합니다.

1. 경로, 쿼리 및 헤더 매개 변수를 정의하고 필요한 경우 프로필 또는 컨텍스트 데이터에 변수를 매핑합니다.

1. 필드를 감지하고 매핑할 수 있도록 샘플 JSON 응답을 붙여 넣습니다.

1. 응답 페이로드 매핑에서 개인화에 필요한 필드를 선택합니다.

1. 예상 볼륨을 기반으로 시간 제한, 재시도 및 캐싱 정책을 구성합니다.

1. 연결을 테스트한 다음 통합을 활성화합니다.

아래 표에는 이 통합 요청에 대한 예제 값이 나와 있습니다.

+++ 샘플 통합 필드

| 필드 | 값 |
| --- | --- |
| **URL** | `https://{{your-deployment}}.talon.one/v1/customer_profiles/{{integrationId}}/achievements/{{achievementId}}` |
| **HTTP 메서드** | `GET` |

**경로 매개 변수**

| 경로 매개 변수 | 이름 | 기본 값 |
| --- | --- | --- |
| `your-deployment` | `your-deployment` | `<your_deployment>` |
| `integrationId` | `integrationId` | `<integrationId>` |
| `achievementId` | `achievementId` | `<achievementId>` |

**머리글**

| 매개 변수 | 이름 | 유형 | 값 | 필수 |
| --- | --- | --- | --- | --- |
| Content-Type(기본값) | Content-Type | 상수 | application/json | 예(켜기) |

**쿼리 매개 변수**

| 매개 변수 | 이름 | 유형 | 값 | 필수 |
| --- | --- | --- | --- | --- |
| `progressStatus` | `progressStatus` | 변수 | 진행 중 / 완료됨 / 만료됨 | 아니요(해제) |
| `startDate` | `startDate` | 변수 | 2024-05-29T15:04:05+07:00 | 아니요(해제) |
| `endDate` | `endDate` | 변수 | 2024-05-29T15:04:05+07:00 | 아니요(해제) |
| `pageSize` | `pageSize` | 변수 | `<default_page_size>` | 아니요(해제) |
| `skip` | `skip` | 변수 | `<items_to_skip>` | 아니요(해제) |

**인증**

| 유형 | API 키 이름 | API 키 값 | 위치 |
| --- | --- | --- | --- |
| API 키 | Authorization | ApiKey-v1 `<YOUR_API_KEY>` | Header |

+++

### 안타보 {#antavo}

>[!BEGINSHADEBOX]

Antavo는 회원, 보상 및 이벤트를 위한 REST API가 포함된 엔터프라이즈 충성도 플랫폼입니다.

일반적인 사용 사례에는 이메일 또는 푸시의 포인트, 계층 또는 보상과 충성도 상태에 따른 오퍼가 포함됩니다.

>[!ENDSHADEBOX]

+++ Antavo에 대한 사전 요구 사항 및 제한 사항에 대해 자세히 알아보십시오.

다음 전제 조건이 적용됩니다.

* 스택 URL 및 API 자격 증명; 필요한 경우 프로그램 또는 샵 식별자.
* Journey Optimizer의 관리자 액세스 권한.

다음 제한 사항 및 제외가 적용됩니다.

* 고객 PII는 Antavo 계약 및 개인정보 처리방침에 따라 처리되어야 합니다.
* Antavo를 사용하여 API 버전 및 안정적인 끝점을 확인합니다.

+++

아래 절차를 사용하여 Journey Optimizer에서 이 통합을 구성합니다. 요청 세부 정보는 **샘플 통합 필드**&#x200B;를 참조하고 해당 환경에 대한 공급업체 설명서를 통해 해당 값을 확인하십시오.

1. [통합 작업](integrations.md)을 따르십시오. 공급업체의 인증(예: 쿼리의 API 키)으로 **GET**&#x200B;을(를) 구성하고, 정책에 대한 PII를 노출하지 않도록 하고, 샘플 JSON을 붙여 넣고, 필드를 매핑하고, 테스트하고, 활성화합니다.

1. Journey Optimizer에서 **[!UICONTROL 구성]** > **[!UICONTROL 관리]**(으)로 이동한 다음 **[!UICONTROL 통합 만들기]**&#x200B;를 선택합니다.

1. 통합 이름을 공백 없이 입력하십시오.

1. Antavo Enterprise API를 사용하여 끝점을 구성합니다.

1. 별도로 명시되지 않는 한 구성 테이블에 표시된 HTTP 메서드(일반적으로 GET)를 선택합니다.

1. 표 및 공급업체 설명서에 지정된 대로 인증(헤더, 쿼리 매개 변수 또는 OAuth)을 구성합니다.

1. 경로, 쿼리 및 헤더 매개 변수를 정의하고 필요한 경우 프로필 또는 컨텍스트 데이터에 변수를 매핑합니다.

1. 필드를 감지하고 매핑할 수 있도록 샘플 JSON 응답을 붙여 넣습니다.

1. 응답 페이로드 매핑에서 개인화에 필요한 필드를 선택합니다.

1. 예상 볼륨을 기반으로 시간 제한, 재시도 및 캐싱 정책을 구성합니다.

1. 연결을 테스트한 다음 통합을 활성화합니다.

아래 표에는 이 통합 요청에 대한 예제 값이 나와 있습니다.

+++ 샘플 통합 필드

샘플 통합 필드는 **스테이징** 호스트를 사용하고, 프로덕션은 Antavo 스택 호스트 이름을 사용합니다. [Antavo 설명서](https://antavo.com/docs/){target="_blank"}를 참조하세요.

| 필드 | 값 |
| --- | --- |
| **URL** | `https://api.staging.antavo.com/customers/{{customer_id}}/activities/offers` |
| **HTTP 메서드** | `GET` |
| **정책** | 필요에 따라 정책 수준 세부 정보를 구성합니다. |
| **응답 페이로드** | API 응답을 기반으로 작성 중에 사용할 응답 필드를 선택하고 구성합니다. |

**경로 매개 변수**

| 경로 매개 변수 | 이름 | 기본 값 |
| --- | --- | --- |
| `customer_id` | `customer_id` | `<customer_id>` |

**머리글**

| 매개 변수 | 이름 | 유형 | 값 | 필수 |
| --- | --- | --- | --- | --- |
| Content-Type(기본값) | Content-Type | 상수 | application/json | 예(켜기) |
| 수락 | 수락 | 상수 | application/json | 아니요(해제) |

**인증**

| 유형 | API 키 이름 | API 키 값 | 위치 |
| --- | --- | --- | --- |
| API 키 | `api_key` | `<YOUR_API_KEY>` | 쿼리 매개변수 |

+++

### Salesforce 충성도 {#salesforce-loyalty}

>[!BEGINSHADEBOX]

Salesforce 충성도 관리는 멤버, 프로그램 및 트랜잭션을 위해 Salesforce 플랫폼의 REST API를 노출합니다.

일반적인 사용 사례에는 여정의 계층, 포인트 또는 이점 표시 및 CRM 및 로열티 데이터에 메시징 정렬 등이 포함됩니다.

>[!ENDSHADEBOX]

+++ Salesforce 충성도에 대한 사전 요구 사항 및 제한 사항에 대해 자세히 알아보십시오.

다음 전제 조건이 적용됩니다.

* Salesforce 인스턴스, 연결된 앱 또는 통합 사용자 및 조직에 적합한 OAuth.
* Journey Optimizer의 관리자 액세스 권한.

다음 제한 사항 및 제외가 적용됩니다.

* Salesforce API 제한 및 OAuth 토큰 새로 고침은 통합에 디자인되어야 합니다.
* 필드 수준 보안 및 공유 규칙은 API 응답에 표시되는 필드를 제어합니다.

+++

아래 절차를 사용하여 Journey Optimizer에서 이 통합을 구성합니다. 요청 세부 정보는 **샘플 통합 필드**&#x200B;를 참조하고 해당 환경에 대한 공급업체 설명서를 통해 해당 값을 확인하십시오.

1. [통합 작업](integrations.md)을 따르십시오. 팀이 승인하는 충성도 통합 엔드포인트를 사용하고, Salesforce OAuth를 완료하고, 샘플 JSON을 붙여넣고, 필드를 매핑하고, 복합 API 제한을 준수하고, 테스트하고, 활성화합니다.

1. Journey Optimizer에서 **[!UICONTROL 구성]** > **[!UICONTROL 관리]**(으)로 이동한 다음 **[!UICONTROL 통합 만들기]**&#x200B;를 선택합니다.

1. 통합 이름을 공백 없이 입력하십시오.

1. Salesforce 충성도 관리 REST를 사용하여 끝점을 구성합니다. 예제 URL 패턴:

   `https://{instance}.salesforce.com/services/data/vXX.X/...`

1. 별도로 명시되지 않는 한 구성 테이블에 표시된 HTTP 메서드(일반적으로 GET)를 선택합니다.

1. 표 및 공급업체 설명서에 지정된 대로 인증(헤더, 쿼리 매개 변수 또는 OAuth)을 구성합니다.

1. 경로, 쿼리 및 헤더 매개 변수를 정의하고 필요한 경우 프로필 또는 컨텍스트 데이터에 변수를 매핑합니다.

1. 필드를 감지하고 매핑할 수 있도록 샘플 JSON 응답을 붙여 넣습니다.

1. 응답 페이로드 매핑에서 개인화에 필요한 필드를 선택합니다.

1. 예상 볼륨을 기반으로 시간 제한, 재시도 및 캐싱 정책을 구성합니다.

1. 연결을 테스트한 다음 통합을 활성화합니다.

아래 표에는 이 통합 요청에 대한 예제 값이 나와 있습니다.

+++ 샘플 통합 필드

조직의 API 버전에 대해 문서화된 충성도 관리 **구성원 프로필** GET 작업을 사용하십시오. 경로에는 프로그램 및 구성원 식별자가 포함됩니다. [Salesforce 개발자](https://developer.salesforce.com/){target="_blank"}를 참조하십시오.

| 필드 | 값 |
| --- | --- |
| **URL** | `https://{{your-instance}}.my.salesforce.com/services/data/{{version}}/connect/loyalty/management/members` |
| **HTTP 메서드** | `GET` |
| **정책** | 필요에 따라 정책 수준 세부 정보를 구성합니다. |
| **응답 페이로드** | API 응답을 기반으로 작성 중에 사용할 응답 필드를 선택하고 구성합니다. |

**경로 매개 변수**

| 경로 매개 변수 | 이름 | 기본 값 |
| --- | --- | --- |
| `your-instance` | `your-instance` | `<your_instance>` |
| `version` | `version` | `version` |

**머리글**

| 매개 변수 | 이름 | 유형 | 값 | 필수 |
| --- | --- | --- | --- | --- |
| Content-Type(기본값) | Content-Type | 상수 | application/json | 예(켜기) |
| 수락 | 수락 | 상수 | application/json | 아니요(해제) |

**쿼리 매개 변수**

| 매개 변수 | 이름 | 유형 | 값 | 필수 |
| --- | --- | --- | --- | --- |
| `membershipNumber` | `membershipNumber` | 변수 | `<membership_number>` | 아니요(해제) * |
| `membershipId` | `membershipId` | 변수 | `<membership_id>` | 아니요(해제) * |
| `posMemId` | `posMemId` | 변수 | `<pos_mem_id>` | 아니요(해제) * |

\* 세 가지 중 하나 이상이 필요합니다.

**인증**

| 유형 | API 키 이름 | API 키 값 | 위치 |
| --- | --- | --- | --- |
| API 키 | Authorization | `<access_token>` | Header |

+++

### 모세관 {#capillary}

>[!BEGINSHADEBOX]

Capillary는 소매 스택에서 일반적인 충성도 및 참여 API를 제공합니다.

일반적인 사용 사례에는 개인화된 여정 내의 포인트, 계층 또는 오퍼가 포함됩니다.

>[!ENDSHADEBOX]

+++ Capillary에 대한 사전 요구 사항 및 제한 사항에 대해 자세히 알아보십시오.

다음 전제 조건이 적용됩니다.

* API 호스트 및 인증(종종 서명된 요청, Capillary 문서 준수).
* 엔드포인트에 대한 프로그램 식별자.

다음 제한 사항 및 제외가 적용됩니다.

* 인증 체계 및 지역 호스트는 배포에 따라 다릅니다. Capillary에 당신의 스택에 대해 확인합니다.

+++

아래 절차를 사용하여 Journey Optimizer에서 이 통합을 구성합니다. 요청 세부 정보는 **샘플 통합 필드**&#x200B;를 참조하고 해당 환경에 대한 공급업체 설명서를 통해 해당 값을 확인하십시오.

1. [통합 작업](integrations.md)을 따르십시오. 필요에 따라 `CAP-API-ACCESS-TOKEN`과(와) 같은 헤더를 구성하고, 샘플 JSON을 붙여넣고, 필드를 매핑하고, 테스트하고, 활성화합니다.

1. Journey Optimizer에서 **[!UICONTROL 구성]** > **[!UICONTROL 관리]**(으)로 이동한 다음 **[!UICONTROL 통합 만들기]**&#x200B;를 선택합니다.

1. 통합 이름을 공백 없이 입력하십시오.

1. Capillary API를 사용하여 끝점을 구성합니다.

1. 별도로 명시되지 않는 한 구성 테이블에 표시된 HTTP 메서드(일반적으로 GET)를 선택합니다.

1. 표 및 공급업체 설명서에 지정된 대로 인증(헤더, 쿼리 매개 변수 또는 OAuth)을 구성합니다.

1. 경로, 쿼리 및 헤더 매개 변수를 정의하고 필요한 경우 프로필 또는 컨텍스트 데이터에 변수를 매핑합니다.

1. 필드를 감지하고 매핑할 수 있도록 샘플 JSON 응답을 붙여 넣습니다.

1. 응답 페이로드 매핑에서 개인화에 필요한 필드를 선택합니다.

1. 예상 볼륨을 기반으로 시간 제한, 재시도 및 캐싱 정책을 구성합니다.

1. 연결을 테스트한 다음 통합을 활성화합니다.

아래 표에는 이 통합 요청에 대한 예제 값이 나와 있습니다.

+++ 샘플 통합 필드

예: `https://ushc.intouch.capillarytech.com/api/v3/rewards/{reward_id}`(호스트는 지역에 따라 다름). [Capillary](https://capillarytech.com/){target="_blank"}을(를) 사용하여 호스트 및 인증 체계의 유효성을 검사합니다.


| 필드 | 값 |
| --- | --- |
| **URL** | `https://ushc.intouch.capillarytech.com/api/v3/rewards/{{reward_id}}` |
| **HTTP 메서드** | `GET` |
| **정책** | 필요에 따라 정책 수준 세부 정보를 구성합니다. |
| **응답 페이로드** | API 응답을 기반으로 작성 중에 사용할 응답 필드를 선택하고 구성합니다. |

**경로 매개 변수**

| 경로 매개 변수 | 이름 | 기본 값 |
| --- | --- | --- |
| `reward_id` | 보상 ID | `<your_reward_id>` |

**머리글**

| 매개 변수 | 이름 | 유형 | 값 | 필수 |
| --- | --- | --- | --- | --- |
| Content-Type | Content-Type | 상수 | application/json | 예(켜기) |
| CAP-API-ACCESS-TOKEN | 액세스 토큰 | 상수 | `<YOUR_ACCESS_TOKEN>` | 예(켜기) |

**인증**

| 유형 | API 키 이름 | API 키 값 | 위치 |
| --- | --- | --- | --- |
| API 키 | CAP-API-ACCESS-TOKEN | `<YOUR_ACCESS_TOKEN>` | Header |

+++


## 템플릿 및 메시징 {#templates-and-messaging}

### 스텐술 {#stensul}

>[!BEGINSHADEBOX]

Stensul은 승인된 템플릿을 위한 이메일 생성 플랫폼입니다. Journey Optimizer은 API를 통해 템플릿 메타데이터 및 구조화된 영역을 사용할 수 있습니다.

일반적인 사용 사례에는 승인된 템플릿 및 프로필 속성에 대한 매핑 영역 가져오기, 확장 가능한 캠페인 빌드에 대해 관리 블록 재사용 등이 있습니다.

>[!ENDSHADEBOX]

+++ Stensul의 사전 요구 사항 및 제한 사항에 대해 자세히 알아보십시오.

다음 전제 조건이 적용됩니다.

* API 액세스가 포함된 Stensul 계정 및 정의된 토큰으로 게시된 템플릿.
* 통합을 만들기 위한 Journey Optimizer의 관리자 액세스 권한.

다음 제한 사항 및 제외가 적용됩니다.

* Journey Optimizer 내의 Stensul 템플릿에 대한 즉석 WYSIWYG 편집은 여기에서 다루지 않습니다.
* 템플릿 페이로드가 크거나 복잡한 HTML은 보안 검토 및 삭제해야 할 수 있습니다.

+++

아래 절차를 사용하여 Journey Optimizer에서 이 통합을 구성합니다. 요청 세부 정보는 **샘플 통합 필드**&#x200B;를 참조하고 해당 환경에 대한 공급업체 설명서를 통해 해당 값을 확인하십시오.

1. Journey Optimizer에서 **[!UICONTROL 구성]** > **[!UICONTROL 관리]**(으)로 이동한 다음 **[!UICONTROL 통합 만들기]**&#x200B;를 선택합니다.

1. 통합 이름을 입력합니다.

1. Stensul 템플릿 API URL을 사용하여 끝점을 구성합니다. 예제 URL 패턴:

   `https://api.stensul.com/v1/templates/{template_id}`

1. 인증을 구성합니다(Stensul API 설명서별 API 키 또는 OAuth).

1. 경로 변수 를 정의합니다(예: 템플릿 ID).

1. 필드 감지를 위한 샘플 JSON 응답을 붙여 넣습니다.

1. 필수 템플릿 필드를 Journey Optimizer 개인화 필드에 매핑합니다.

1. 연결 테스트 및 활성화.

### 마리골드 {#marigold}

>[!BEGINSHADEBOX]

Marigold는 충성도 및 참여 API를 노출하며, 호스트는 지역에 따라 다릅니다(EU와 US 모듈 호스트 이름).

대표적인 활용 사례로는 Marigold 프로그램의 충성도 또는 선호도 데이터로 메시지를 풍부하게 하는 것이 있다.

>[!ENDSHADEBOX]

+++ Marigold의 사전 요구 사항 및 제한 사항에 대해 자세히 알아보십시오.

다음 전제 조건이 적용됩니다.

* 계약의 기본 URL 및 자격 증명, 가능한 경우 최소 권한 API 사용자.
* Journey Optimizer의 관리자 액세스 권한.

다음 제한 사항 및 제외가 적용됩니다.

* 엔드포인트는 Marigold 제품에 따라 다릅니다. 배포에 대한 Marigold 지원을 통해 확인합니다.
* 응답의 개인 데이터는 DPA 및 보존 정책을 준수해야 합니다.

+++

아래 절차를 사용하여 Journey Optimizer에서 이 통합을 구성합니다. 요청 세부 정보는 **샘플 통합 필드**&#x200B;를 참조하고 해당 환경에 대한 공급업체 설명서를 통해 해당 값을 확인하십시오.

1. [통합 작업](integrations.md)을 따르십시오. 영역에 대한 Marigold 호스트를 가리키고, 인증을 설정하고(아래 샘플은 키 및 암호와 함께 `X-Api-Key`을 사용), 샘플 JSON을 붙여넣고, 필드를 매핑하고, 테스트하고, 활성화합니다.

1. Journey Optimizer에서 **[!UICONTROL 구성]** > **[!UICONTROL 관리]**(으)로 이동한 다음 **[!UICONTROL 통합 만들기]**&#x200B;를 선택합니다.

1. 통합 이름을 공백 없이 입력하십시오.

1. Marigold REST API를 사용하여 끝점을 구성합니다.

1. 별도로 명시되지 않는 한 구성 테이블에 표시된 HTTP 메서드(일반적으로 GET)를 선택합니다.

1. 표 및 공급업체 설명서에 지정된 대로 인증(헤더, 쿼리 매개 변수 또는 OAuth)을 구성합니다.

1. 경로, 쿼리 및 헤더 매개 변수를 정의하고 필요한 경우 프로필 또는 컨텍스트 데이터에 변수를 매핑합니다.

1. 필드를 감지하고 매핑할 수 있도록 샘플 JSON 응답을 붙여 넣습니다.

1. 응답 페이로드 매핑에서 개인화에 필요한 필드를 선택합니다.

1. 예상 볼륨을 기반으로 시간 제한, 재시도 및 캐싱 정책을 구성합니다.

1. 연결을 테스트한 다음 통합을 활성화합니다.

1. Marigold는 고객 인스턴스가 활성화된 지리적 영역을 기반으로 두 개의 끝점을 사용합니다.

   * 유럽: `https://{{customername}}.module.slgnt.eu`
   * 미국: `https://{{customername}}.module.slgnt.us`

아래 표에는 이 통합 요청에 대한 예제 값이 나와 있습니다.

+++ 샘플 통합 필드

기본 호스트는 지역에 따라 다릅니다(예: `https://{{customername}}.module.slgnt.eu` 또는 `https://{{customername}}.module.slgnt.us`). Marigold를 사용하여 배포용 경로를 확인합니다.

| 필드 | 값 |
| --- | --- |
| **URL** | `https://{{customername}}.module.slgnt.{{locale}}/Portal/Api/organizations/{{organization}}/content/{{api_name}}` |
| **HTTP 메서드** | `GET` |
| 응답 페이로드 | API 응답을 기반으로 작성 중에 사용할 응답 필드를 선택하고 구성합니다. |
| 정책 | 필요에 따라 정책 수준 세부 정보를 구성합니다. |

**경로 매개 변수**

| 경로 매개 변수 | 이름 | 기본 값 |
| --- | --- | --- |
| `customername` | `customername` | `<your_name>` |
| `locale` | `locale` | `eu` / `us` |
| `organization` | `organization` | `<your_organization>` |
| `api_name` | `api_name` | `<api_name>` |

**머리글**

| 매개 변수 | 이름 | 유형 | 값 | 필수 |
| --- | --- | --- | --- | --- |
| Content-Type(기본값) | Content-Type | 상수 | application/json | 예(켜기) |

**인증**

| 유형 | API 키 이름 | API 키 값 | 위치 |
| --- | --- | --- | --- |
| API 키 | X-Api-Key | `<apiKey>:<apiSecret>` | Header |

+++

### Adobe Target 권장 사항 {#adobe-target-recommendations}

>[!BEGINSHADEBOX]

Adobe Target에는 권한에 따라 서버측 또는 통합 경험을 위한 권장 사항 및 게재 API가 포함되어 있습니다.

일반적인 사용 사례에는 Journey Optimizer에서 작성한 경험에 권장 사항을 삽입하고 프로필 또는 Experience Platform 컨텍스트에 키를 맞추는 작업이 포함됩니다.

>[!ENDSHADEBOX]

+++ Adobe Target Recommendations에 대한 사전 요구 사항 및 제한 사항에 대해 자세히 알아보십시오.

다음 전제 조건이 적용됩니다.

* 권장 사항이 있는 타겟, IMS 조직 및 지원되는 인증.
* Journey Optimizer의 관리자 액세스 권한.

다음 제한 사항 및 제외가 적용됩니다.

* 권장 사항 및 게재 API에는 특정 매개 변수(예: mbox 또는 제품 식별자)가 필요합니다. Adobe Target 설명서를 따르십시오.
* 전송 볼륨 및 사용 사례에 대한 지연 시간 및 캐싱을 조정합니다.

+++

아래 절차를 사용하여 Journey Optimizer에서 이 통합을 구성합니다. 요청 세부 정보는 **샘플 통합 필드**&#x200B;를 참조하고 해당 환경에 대한 공급업체 설명서를 통해 해당 값을 확인하십시오.

1. [통합 작업](integrations.md)을 따르십시오. 게재 호출은 종종 JSON 본문이 있는 **POST**&#x200B;입니다. [Target 인증](https://experienceleague.adobe.com/en/docs/target-dev/developer/api/configure-authentication){target="_blank"}당 OAuth를 구성하고 샘플 응답을 붙여 넣고 필드를 매핑한 다음 예상 볼륨에서 테스트하십시오.

1. Journey Optimizer에서 **[!UICONTROL 구성]** > **[!UICONTROL 관리]**(으)로 이동한 다음 **[!UICONTROL 통합 만들기]**&#x200B;를 선택합니다.

1. 통합 이름을 공백 없이 입력하십시오.

1. Target Recommendations/게재 API를 사용하여 끝점을 구성합니다.

1. 별도로 명시되지 않는 한 구성 테이블에 표시된 HTTP 메서드(일반적으로 GET)를 선택합니다.

1. 표 및 공급업체 설명서에 지정된 대로 인증(헤더, 쿼리 매개 변수 또는 OAuth)을 구성합니다.

1. 경로, 쿼리 및 헤더 매개 변수를 정의하고 필요한 경우 프로필 또는 컨텍스트 데이터에 변수를 매핑합니다.

1. 필드를 감지하고 매핑할 수 있도록 샘플 JSON 응답을 붙여 넣습니다.

1. 응답 페이로드 매핑에서 개인화에 필요한 필드를 선택합니다.

1. 예상 볼륨을 기반으로 시간 제한, 재시도 및 캐싱 정책을 구성합니다.

1. 연결을 테스트한 다음 통합을 활성화합니다.

아래 표에는 이 통합 요청에 대한 예제 값이 나와 있습니다.

+++ 샘플 통합 필드

| 필드 | 값 |
| --- | --- |
| **URL** | `https://{{client}}.tt.omtrdc.net/rest/v1/delivery` |
| 정책 | 필요에 따라 정책 수준 세부 정보를 구성합니다. |
| **HTTP 메서드** | `POST` |

**경로 매개 변수**

| 경로 매개 변수 | 이름 | 기본 값 |
| --- | --- | --- |
| `client` | `client` | `<client_name>` |

**머리글**

| 매개 변수 | 이름 | 유형 | 값 | 필수 |
| --- | --- | --- | --- | --- |
| Content-Type(기본값) | Content-Type | 상수 | application/json | 예(켜기) |

**쿼리 매개 변수**

| 매개 변수 | 이름 | 유형 | 값 | 필수 |
| --- | --- | --- | --- | --- |
| 클라이언트 | 클라이언트 | 변수 | `<customer_client_code>` | 예(켜기) |
| sessionId | sessionId | 변수 | ` <session_identifier>` | 예(켜기) |

**인증**

[Target 인증 구성](https://experienceleague.adobe.com/en/docs/target-dev/developer/api/configure-authentication)을 참조하고 페이로드에 JSON을 추가하십시오.

**요청 페이로드**

```Sample Request Payload JSON
{
  "id": {
    "tntId": "<YOUR_TENANT_ID>"
  },
  "context": {
    "channel": "web",
    "address": {
      "url": "https://example.com/store.html"
    },
    "screen": {
      "width": 1200,
      "height": 1400
    }
  },
  "experienceCloud": {
    "analytics": {
      "logging": "server_side",
      "supplementalDataId": "<supDataId>",
      "trackingServer": "sstats.adobe.com"
    }
  },
  "execute": {
    "pageLoad": {
      "parameters": {
        "pageType": "checkout",
        "preferredCurrency": "$"
      }
    },
    "mboxes": [
      {
        "index": 1,
        "name": "orderConfirmPage"
      }
    ]
  },
  "prefetch": {
    "views": [
      {
        "parameters": {
          "ad": "view"
        }
      }
    ],
    "mboxes": {
      "index": 1,
      "name": "SummerOffer"
    }
  }
}
```

+++


## 데이터, 날씨 및 작업 {#data-weather-and-operations}

### 아큐웨더 {#accuweather}

>[!BEGINSHADEBOX]

AccuWeather는 메시지에 날씨 인식 스니펫이 포함될 수 있도록 예측 및 위치 REST API를 노출합니다.

일반적인 사용 사례에는 이메일이나 푸시 콘텐츠의 짧은 예측 및 프로필 또는 컨텍스트에 연결된 예측 값을 사용하는 맞춤화가 포함됩니다.

>[!ENDSHADEBOX]

+++ AccuWeather의 사전 요구 사항 및 제한 사항에 대해 자세히 알아보십시오.

다음 전제 조건이 적용됩니다.

* API 구독 및 키(위치 키 또는 도시 검색 흐름).
* 통합을 만들기 위한 Journey Optimizer의 관리자 액세스 권한.

다음 제한 사항 및 제외가 적용됩니다.

* AccuWeather 구독 계층에 대한 JSON 응답 형태를 확인합니다. 통합은 JSON 응답의 필드를 매핑합니다.
* AccuWeather 비율 제한 및 권장 캐싱을 확인하십시오.
* `locationKey`을(를) 해결하려면 종종 예측 호출 전에 별도의 지리적 위치 또는 도시 검색 요청이 필요합니다.

+++

아래 절차를 사용하여 Journey Optimizer에서 이 통합을 구성합니다. 요청 세부 정보는 **샘플 통합 필드**&#x200B;를 참조하고 해당 환경에 대한 공급업체 설명서를 통해 해당 값을 확인하십시오.

1. [통합 작업](integrations.md)을 따르십시오. 구독에 다른 요구 사항이 없으면 **GET**&#x200B;을(를) 사용하십시오. `apiKey` 쿼리 매개 변수, 맵 `locationKey` 및 프로필/컨텍스트의 기타 변수를 첨부하고 샘플 JSON을 붙여 넣은 다음 필드를 매핑한 다음 테스트하십시오.

1. Journey Optimizer에서 **[!UICONTROL 구성]** > **[!UICONTROL 관리]**(으)로 이동한 다음 **[!UICONTROL 통합 만들기]**&#x200B;를 선택합니다.

1. 통합 이름을 공백 없이 입력하십시오.

1. 일별 예측 API를 사용하여 끝점을 구성합니다. 예제 URL 패턴:

   `https://dataservice.accuweather.com/forecasts/v1/daily/{days}day/{locationKey}`

1. 별도로 명시되지 않는 한 구성 테이블에 표시된 HTTP 메서드(일반적으로 GET)를 선택합니다.

1. 표 및 공급업체 설명서에 지정된 대로 인증(헤더, 쿼리 매개 변수 또는 OAuth)을 구성합니다.

1. 경로, 쿼리 및 헤더 매개 변수를 정의하고 필요한 경우 프로필 또는 컨텍스트 데이터에 변수를 매핑합니다.

1. 필드를 감지하고 매핑할 수 있도록 샘플 JSON 응답을 붙여 넣습니다.

1. 응답 페이로드 매핑에서 개인화에 필요한 필드를 선택합니다.

1. 예상 볼륨을 기반으로 시간 제한, 재시도 및 캐싱 정책을 구성합니다.

1. 연결을 테스트한 다음 통합을 활성화합니다.

아래 표에는 이 통합 요청에 대한 예제 값이 나와 있습니다.

+++샘플 통합 필드

샘플 통합 필드. 세부 정보 및 계층은 [AccuWeather API](https://developer.accuweather.com/apis){target="_blank"}에 설명되어 있습니다. `locationKey`을(를) 별도의 위치 검색 호출로 해결하는 경우가 많습니다(예: `.../locations/v1/cities/search?q={{cityName}}`).

| 필드 | 값 |
| --- | --- |
| **URL** | `https://dataservice.accuweather.com/forecasts/v1/daily/{{days}}day/{{locationKey}}` |
| **HTTP 메서드** | `GET` |
| 응답 페이로드 | API 응답을 기반으로 작성 중에 사용할 응답 필드를 선택하고 구성합니다. |
| 정책 | 필요에 따라 정책 수준 세부 정보를 구성합니다. |

**경로 매개 변수**

| 경로 매개 변수 | 이름 | 기본 값 |
| --- | --- | --- |
| `days` | `days` | `15` |
| `locationKey` | `locationKey` | `<desired_location_key>` |

**머리글**

| 매개 변수 | 이름 | 유형 | 값 | 필수 |
| --- | --- | --- | --- | --- |
| Content-Type(기본값) | Content-Type | 상수 | application/json | 예(켜기) |

**쿼리 매개 변수**

| 매개 변수 | 이름 | 유형 | 값 | 필수 |
| --- | --- | --- | --- | --- |
| `format` | `format` | 변수 | json | 아니요(해제) |
| `language` | `language` | 변수 | en-US | 아니요(해제) |
| `details` | `details` | 변수 | False | 아니요(해제) |
| `metric` | `metric` | 변수 | False | 아니요(해제) |

**인증**

| 유형 | API 키 이름 | API 키 값 | 위치 |
| --- | --- | --- | --- |
| API 키 | `apiKey` | `<YOUR_API_KEY>` | 쿼리 매개변수 |

+++

### ShipStation {#shipstation}

>[!BEGINSHADEBOX]

ShipStation에서는 운송업체, 라벨 및 추적을 위한 배송 및 주문 API를 제공합니다.

일반적인 사용 사례에는 트랜잭션 메시지의 주문 상태, 추적 링크 또는 게재 ETA가 포함됩니다.

>[!ENDSHADEBOX]

+++ ShipStation의 사전 요구 사항 및 제한 사항에 대해 자세히 알아보십시오.

다음 전제 조건이 적용됩니다.

* API 키 및 암호(ShipStation 문서당 기본 인증).
* Journey Optimizer의 관리자 액세스 권한.

다음 제한 사항 및 제외가 적용됩니다.

* 메시지 콘텐츠에 ShipStation API 키를 노출하지 말고 통합 구성에서만 자격 증명을 유지합니다.
* 페이지 매김된 목록 종단점은 통합에 적합하지 않을 수 있으므로, 가능한 경우 단일 리소스 GET을 선호합니다.

+++

아래 절차를 사용하여 Journey Optimizer에서 이 통합을 구성합니다. 요청 세부 정보는 **샘플 통합 필드**&#x200B;를 참조하고 해당 환경에 대한 공급업체 설명서를 통해 해당 값을 확인하십시오.

1. [통합 작업](integrations.md)을 따르십시오. 필요한 리소스를 타겟팅(주문과 배송), [ShipStation API당 인증](https://www.shipstation.com/docs/api/){target="_blank"}, 샘플 JSON 붙여넣기, 필드 매핑, 테스트, 활성화.

1. Journey Optimizer에서 **[!UICONTROL 구성]** > **[!UICONTROL 관리]**(으)로 이동한 다음 **[!UICONTROL 통합 만들기]**&#x200B;를 선택합니다.

1. 통합 이름을 공백 없이 입력하십시오.

1. ShipStation REST API를 사용하여 끝점을 구성합니다. 예제 URL 패턴:

   `https://ssapi.shipstation.com/...`

1. 별도로 명시되지 않는 한 구성 테이블에 표시된 HTTP 메서드(일반적으로 GET)를 선택합니다.

1. 표 및 공급업체 설명서에 지정된 대로 인증(헤더, 쿼리 매개 변수 또는 OAuth)을 구성합니다.

1. 경로, 쿼리 및 헤더 매개 변수를 정의하고 필요한 경우 프로필 또는 컨텍스트 데이터에 변수를 매핑합니다.

1. 필드를 감지하고 매핑할 수 있도록 샘플 JSON 응답을 붙여 넣습니다.

1. 응답 페이로드 매핑에서 개인화에 필요한 필드를 선택합니다.

1. 예상 볼륨을 기반으로 시간 제한, 재시도 및 캐싱 정책을 구성합니다.

1. 연결을 테스트한 다음 통합을 활성화합니다.

아래 표에는 이 통합 요청에 대한 예제 값이 나와 있습니다.

+++ 샘플 통합 필드

다음 **Get Timer** 예제는 ShipStation 자동화 타이밍 호출 하나를 보여 줍니다. Journey Optimizer에서 재현할 때 ShipStation 통합 가이드의 정확한 경로와 인증을 사용하십시오.

| 필드 | 값 |
| --- | --- |
| **URL** | `https://dashboard.sendtric.com/api/v1/timers/{{id}}` |
| **HTTP 메서드** | `POST` |
| **정책** | 필요에 따라 정책 수준 세부 정보를 구성합니다. |

**머리글**

| 매개 변수 | 이름 | 유형 | 값 | 필수 |
| --- | --- | --- | --- | --- |
| Content-Type(기본값) | Content-Type | 상수 | application/json | 예(켜기) |

**인증**

| 유형 | API 키 이름 | API 키 값 | 위치 |
| --- | --- | --- | --- |
| API 키 | apiKey | `<your_api_key>` | Header |

**요청 페이로드**

```Sample Request Payload
{
    "external_batch_id": "se-28529731",
    "batch_notes": "This is my batch",
    "shipment_ids": [
      "se-28529731"
    ],
    "rate_ids": [
      "se-28529731"
    ]
}
```

+++

### 매출액Cat {#revenuecat}

>[!BEGINSHADEBOX]

RevenueCat은 앱에 대한 구독 상태 및 자격 API를 제공합니다.

일반적인 사용 사례는 정책이 허용하는 라이프사이클 캠페인에 구독 상태를 반영하는 것입니다.

>[!ENDSHADEBOX]

+++ RevenueCat에 대한 사전 요구 사항 및 제한 사항에 대해 자세히 알아보십시오.

다음 전제 조건이 적용됩니다.

* 비밀 API 키 및 앱 식별자. 프로필과 RevenueCat 고객 ID 간의 안정적인 매핑.
* Journey Optimizer의 관리자 액세스 권한.

다음 제한 사항 및 제외가 적용됩니다.

* 비밀 API 키를 보호하고 순환 정책을 따릅니다.
* 구독 및 자격 데이터는 민감합니다. 개인 정보 및 동의 요구 사항을 충족합니다.

+++

아래 절차를 사용하여 Journey Optimizer에서 이 통합을 구성합니다. 요청 세부 정보는 **샘플 통합 필드**&#x200B;를 참조하고 해당 환경에 대한 공급업체 설명서를 통해 해당 값을 확인하십시오.

1. [통합 작업](integrations.md)을 따르십시오. 아래 모델링된 REST **GET**&#x200B;을(를) 호출하고, 비밀 키 헤더로 인증하고, 샘플 JSON을 붙여 넣고, 필드를 매핑하고, 테스트하고, 활성화합니다.

1. Journey Optimizer에서 **[!UICONTROL 구성]** > **[!UICONTROL 관리]**(으)로 이동한 다음 **[!UICONTROL 통합 만들기]**&#x200B;를 선택합니다.

1. 통합 이름을 공백 없이 입력하십시오.

1. RevenueCat REST API를 사용하여 끝점을 구성합니다. 예제 URL 패턴:

   `https://api.revenuecat.com/v1/...`

1. 별도로 명시되지 않는 한 구성 테이블에 표시된 HTTP 메서드(일반적으로 GET)를 선택합니다.

1. 표 및 공급업체 설명서에 지정된 대로 인증(헤더, 쿼리 매개 변수 또는 OAuth)을 구성합니다.

1. 경로, 쿼리 및 헤더 매개 변수를 정의하고 필요한 경우 프로필 또는 컨텍스트 데이터에 변수를 매핑합니다.

1. 필드를 감지하고 매핑할 수 있도록 샘플 JSON 응답을 붙여 넣습니다.

1. 응답 페이로드 매핑에서 개인화에 필요한 필드를 선택합니다.

1. 예상 볼륨을 기반으로 시간 제한, 재시도 및 캐싱 정책을 구성합니다.

1. 연결을 테스트한 다음 통합을 활성화합니다.

아래 표에는 이 통합 요청에 대한 예제 값이 나와 있습니다.

+++ 샘플 통합 필드

예제 패턴: 프로젝트의 기본 URL 및 버전을 사용하여 [RevenueCat 문서](https://docs.revenuecat.com/){target="_blank"}에서 RevenueCat의 **제품 가져오기**(또는 이에 상응하는 제품/권한 부여 GET)를 사용합니다.

| 필드 | 값 |
| --- | --- |
| **URL** | `https://api.revenuecat.com/projects/{{project_id}}/products/{{product_id}}` |
| **HTTP 메서드** | `GET` |
| **정책** | 필요에 따라 정책 수준 세부 정보를 구성합니다. |
| **응답 페이로드** | API 응답을 기반으로 작성 중에 사용할 응답 필드를 선택하고 구성합니다. |

**경로 매개 변수**

| 경로 매개 변수 | 이름 | 기본 값 |
| --- | --- | --- |
| `project_id` | `project_id` | `<project_id>` |
| `product_id` | `product_id` | `<product_id>` |

**머리글**

| 매개 변수 | 이름 | 유형 | 값 | 필수 |
| --- | --- | --- | --- | --- |
| Content-Type(기본값) | Content-Type | 상수 | application/json | 예(켜기) |

**쿼리 매개 변수**

| 매개 변수 | 이름 | 유형 | 값 | 필수 |
| --- | --- | --- | --- | --- |
| `country` | `country` | 변수 | `<iso_country_code>` | 아니요(해제) |
| `locale` | `locale` | 변수 | `<locale_code>` | 아니요(해제) |
| `parentId` | `parentId` | 변수 | `<parent_category_id>` | 아니요(해제) |

**인증**

| 유형 | API 키 이름 | API 키 값 | 위치 |
| --- | --- | --- | --- |
| API 키 | Authorization | `Bearer <token>` | Header |

+++

### Databricks {#databricks}

>[!BEGINSHADEBOX]

데이터 블록은 레이크하우스 데이터를 통해 SQL 및 REST API를 제공합니다. 이전 초안은 **jobs/get** 샘플과 문 실행 지침을 결합했습니다.

일반적인 사용 사례는 엄격한 최소 권한으로 개인화를 위해 관리 테이블의 비정규화된 작은 속성을 사용하는 것입니다.

>[!ENDSHADEBOX]

+++ Databricks에 대한 사전 요구 사항 및 제한 사항에 대해 자세히 알아봅니다.

다음 전제 조건이 적용됩니다.

* Workspace 호스트, 토큰 또는 조직당 OAuth 정책, 최소 범위의 서비스 주체.
* Journey Optimizer의 관리자 액세스 권한.

+++

아래 절차를 사용하여 Journey Optimizer에서 이 통합을 구성합니다. 요청 세부 정보는 **샘플 통합 필드**&#x200B;를 참조하고 해당 환경에 대한 공급업체 설명서를 통해 해당 값을 확인하십시오.

1. [통합 작업](integrations.md)을 따르십시오. 좁은 읽기 경로를 선호합니다. **POST** 문 실행을 사용하는 경우 API에 필요한 JSON 본문을 포함하고, 매핑에 대한 샘플 성공 응답을 붙여넣고, 지연을 주의 깊게 테스트하고, 활성화합니다.

1. Journey Optimizer에서 **[!UICONTROL 구성]** > **[!UICONTROL 관리]**(으)로 이동한 다음 **[!UICONTROL 통합 만들기]**&#x200B;를 선택합니다.

1. 통합 이름을 공백 없이 입력하십시오.

1. Databricks SQL 문 실행 API를 사용하여 끝점을 구성합니다. 예제 URL 패턴:

   `https://{workspace-host}/api/2.0/sql/statements/...`

1. 별도로 명시되지 않는 한 구성 테이블에 표시된 HTTP 메서드(일반적으로 GET)를 선택합니다.

1. 표 및 공급업체 설명서에 지정된 대로 인증(헤더, 쿼리 매개 변수 또는 OAuth)을 구성합니다.

1. 경로, 쿼리 및 헤더 매개 변수를 정의하고 필요한 경우 프로필 또는 컨텍스트 데이터에 변수를 매핑합니다.

1. 필드를 감지하고 매핑할 수 있도록 샘플 JSON 응답을 붙여 넣습니다.

1. 응답 페이로드 매핑에서 개인화에 필요한 필드를 선택합니다.

1. 예상 볼륨을 기반으로 시간 제한, 재시도 및 캐싱 정책을 구성합니다.

1. 연결을 테스트한 다음 통합을 활성화합니다.

아래 표에는 이 통합 요청에 대한 예제 값이 나와 있습니다.

+++샘플 통합 필드

아래의 **GET** 작업 예는 예입니다. SQL 기반 개인화의 경우 작업 영역에서 지원하는 [문 실행 API](https://docs.databricks.com/api/workspace/statementexecution){target="_blank"} 패턴을 선호합니다.

| 필드 | 값 |
| --- | --- |
| **URL** | `https://<databricks-instance>/api/2.0/jobs/get` |
| **HTTP 메서드** | `GET` |
| 응답 페이로드 | API 응답을 기반으로 작성 중에 사용할 응답 필드를 선택하고 구성합니다. |
| 정책 | 필요에 따라 정책 수준 세부 정보를 구성합니다. |
| 인증 | OAuth |

**머리글**

| 매개 변수 | 이름 | 유형 | 값 | 필수 |
| --- | --- | --- | --- | --- |
| 수락 | 수락 | 상수 | application/json | 예(켜기) |

**쿼리 매개 변수**

| 매개 변수 | 이름 | 유형 | 값 | 필수 |
| --- | --- | --- | --- | --- |
| `job_id` | `job_id` | 변수 | `12` | 예 |

+++

## 리뷰, 동의 및 소셜 {#reviews-consent-and-social}

### bynder {#bynder}

>[!BEGINSHADEBOX]

Byender는 REST API가 있는 DAM입니다. 통합에서는 일반적으로 읽기 전용 메타데이터 또는 에셋 URL에 OAuth 2.0을 사용합니다.

일반적인 사용 사례에는 에셋 메타데이터나 게재 URL을 메시지로 가져와서 Bynder에서 승인된 크리에이티브를 여정과 정렬하여 유지하는 작업이 포함됩니다.

>[!ENDSHADEBOX]

+++ Bynder의 사전 요구 사항 및 제한 사항에 대해 자세히 알아보십시오.

다음 전제 조건이 적용됩니다.

* 포털 도메인 및 OAuth 클라이언트(또는 승인된 토큰 접근 방식).
* 읽기 전용 액세스 범위(Journey Optimizer의 관리자 액세스).

다음 제한 사항 및 제외가 적용됩니다.

* 페이지 매김 및 OAuth 토큰 새로 고침은 Byender의 API 규칙을 따라야 합니다.
* 페이지가 매겨진 대형 응답: 개인화에 필요한 필드만 매핑합니다.

+++

아래 절차를 사용하여 Journey Optimizer에서 이 통합을 구성합니다. 요청 세부 정보는 **샘플 통합 필드**&#x200B;를 참조하고 해당 환경에 대한 공급업체 설명서를 통해 해당 값을 확인하십시오.

1. [통합 작업](integrations.md)을 따르십시오. 선택한 엔드포인트에서 **GET**&#x200B;을(를) 구성하고(하나의 공통 패턴은 사용자 목록) [바이트당 OAuth를 완료합니다. ](https://developer.bynder.com/){target="_blank"} 불필요한 데이터 페이지를 가져오지 않고 필드 매핑하고 테스트한 다음 활성화합니다.

1. Journey Optimizer에서 **[!UICONTROL 구성]** > **[!UICONTROL 관리]**(으)로 이동한 다음 **[!UICONTROL 통합 만들기]**&#x200B;를 선택합니다.

1. 통합 이름을 공백 없이 입력하십시오.

1. Byender API v4를 사용하여 끝점을 구성합니다. 예제 URL 패턴:

   `https://{your-bynder-domain}/api/v4/users/`

1. 별도로 명시되지 않는 한 구성 테이블에 표시된 HTTP 메서드(일반적으로 GET)를 선택합니다.

1. 표 및 공급업체 설명서에 지정된 대로 인증(헤더, 쿼리 매개 변수 또는 OAuth)을 구성합니다.

1. 경로, 쿼리 및 헤더 매개 변수를 정의하고 필요한 경우 프로필 또는 컨텍스트 데이터에 변수를 매핑합니다.

1. 필드를 감지하고 매핑할 수 있도록 샘플 JSON 응답을 붙여 넣습니다.

1. 응답 페이로드 매핑에서 개인화에 필요한 필드를 선택합니다.

1. 예상 볼륨을 기반으로 시간 제한, 재시도 및 캐싱 정책을 구성합니다.

1. 연결을 테스트한 다음 통합을 활성화합니다.

아래 표에는 이 통합 요청에 대한 예제 값이 나와 있습니다.

+++ 샘플 통합 필드

샘플 통합 필드. OAuth 2.0 페이로드 세부 정보는 [Byender API 설명서](https://developer.bynder.com/){target="_blank"}를 참조하십시오.

| 필드 | 값 |
| --- | --- |
| **URL** | `https://{{your-bynder-domain}}/api/v4/users/` |
| **HTTP 메서드** | `GET` |
| 응답 페이로드 | API 응답을 기반으로 작성 중에 사용할 응답 필드를 선택하고 구성합니다. |
| 정책 | 필요에 따라 정책 수준 세부 정보를 구성합니다. |

**경로 매개 변수**

| 경로 매개 변수 | 이름 | 기본 값 |
| --- | --- | --- |
| `your-bynder-domain` | `your-bynder-domain` | `<your-bynder-domain>` |

**머리글**

| 매개 변수 | 이름 | 유형 | 값 | 필수 |
| --- | --- | --- | --- | --- |
| Content-Type(기본값) | Content-Type | 상수 | application/json | 예(켜기) |
| Authorization | Authorization | 상수 | 전달자 `<token>` | 예(켜기) |

**쿼리 매개 변수**

| 매개 변수 | 이름 | 유형 | 값 | 필수 |
| --- | --- | --- | --- | --- |
| `includeInActive` | `includeInActive` | 변수 | False | 아니요(해제) |
| `limit` | `limit` | 변수 | 100 | 아니요(해제) |
| `page` | `page` | 변수 | 1 | 아니요(해제) |

**인증**

| 유형 | 페이로드 |
| --- | --- |
| OAuth 2.0 | OAuth 2.0 페이로드(Byender 설명서 참조) |

```
{
    "type": "oauth2",
    "endpoint": {
        "uri": ""
    },
    "method": "get",
    "response": {
        "type": "json"
    },
    "request": {
        "header": [
            {
                "key": "client_id",
                "value": ""
            },
            {
                "key": "client_secret",
                "value": ""
            }
        ],
        "queryParams": [
            {
                "key": "grant_type",
                "value": ""
            },
            {
                "key": "scope",
                "value": ""
            }
        ],
        "payload": {
            "type": "json",
            "content": {}
        }
    },
    "credentialPaths": [
        "header.client_id",
        "header.client_secret",
        "queryParam.scope"
    ],
    "tokenPath": "message.token",
    "policy": {
        "timeoutInMilliseconds": 30000,
        "cache": {
            "enabled": true,
            "ttlInSeconds": 300
        },
        "retry": {
            "enabled": false
        }
    },
    "locationConfig": {
        "key": "x-token",
        "location": "query"
    }
}
```

+++

### Trustpilot {#trustpilot}

>[!BEGINSHADEBOX]

Trustpilot은 사용 사례와 계약이 허용하는 비즈니스 및 검토 요약 데이터를 위한 API를 제공합니다.

일반적인 사용 사례는 Trustpilot 약관을 준수하는 마케팅 콘텐츠에서 검토 카운트 또는 등급을 표시하는 것입니다.

>[!ENDSHADEBOX]

+++ Trustpilot의 사전 요구 사항 및 제한 사항에 대해 자세히 알아보십시오.

다음 전제 조건이 적용됩니다.

* API 키 및 승인된 사용 사례, 쿼리에 대한 비즈니스 식별자.
* Journey Optimizer의 관리자 액세스 권한.

다음 제한 사항 및 제외가 적용됩니다.

* Trustpilot 데이터 사용은 Trustpilot 브랜딩 및 데이터 사용 정책을 준수해야 합니다.
* 비율 제한은 요약 및 관련 끝점을 검토하는 데 적용됩니다.

+++

아래 절차를 사용하여 Journey Optimizer에서 이 통합을 구성합니다. 요청 세부 정보는 **샘플 통합 필드**&#x200B;를 참조하고 해당 환경에 대한 공급업체 설명서를 통해 해당 값을 확인하십시오.

1. [통합 작업](integrations.md)을 따르십시오. 필수 쿼리 인증을 사용하여 **GET**&#x200B;을(를) 구성하고, 프로필 또는 컨텍스트에서 식별자를 매핑하고, 샘플 JSON을 붙여 넣고, 필드를 매핑하고, 테스트하고, 활성화합니다.

1. Journey Optimizer에서 **[!UICONTROL 구성]** > **[!UICONTROL 관리]**(으)로 이동한 다음 **[!UICONTROL 통합 만들기]**&#x200B;를 선택합니다.

1. 통합 이름을 공백 없이 입력하십시오.

1. Trustpilot API를 사용하여 끝점을 구성합니다. 예제 URL 패턴:

   `https://api.trustpilot.com/v1/...`

1. 별도로 명시되지 않는 한 구성 테이블에 표시된 HTTP 메서드(일반적으로 GET)를 선택합니다.

1. 표 및 공급업체 설명서에 지정된 대로 인증(헤더, 쿼리 매개 변수 또는 OAuth)을 구성합니다.

1. 경로, 쿼리 및 헤더 매개 변수를 정의하고 필요한 경우 프로필 또는 컨텍스트 데이터에 변수를 매핑합니다.

1. 필드를 감지하고 매핑할 수 있도록 샘플 JSON 응답을 붙여 넣습니다.

1. 응답 페이로드 매핑에서 개인화에 필요한 필드를 선택합니다.

1. 예상 볼륨을 기반으로 시간 제한, 재시도 및 캐싱 정책을 구성합니다.

1. 연결을 테스트한 다음 통합을 활성화합니다.

아래 표에는 이 통합 요청에 대한 예제 값이 나와 있습니다.

+++ 샘플 통합 필드

통합 패턴에 [Trustpilot 개발자](https://developers.trustpilot.com/){target="_blank"}의 범주 목록 작업을 사용하십시오. 매개 변수는 리소스마다 다릅니다.

| 필드 | 값 |
| --- | --- |
| **URL** | `https://api.trustpilot.com/v1/categories` |
| **HTTP 메서드** | `GET` |
| **정책** | 필요에 따라 정책 수준 세부 정보를 구성합니다. |
| **응답 페이로드** | API 응답을 기반으로 작성 중에 사용할 응답 필드를 선택하고 구성합니다. |

**머리글**

| 매개 변수 | 이름 | 유형 | 값 | 필수 |
| --- | --- | --- | --- | --- |
| Content-Type(기본값) | Content-Type | 상수 | application/json | 예(켜기) |

**쿼리 매개 변수**

| 매개 변수 | 이름 | 유형 | 값 | 필수 |
| --- | --- | --- | --- | --- |
| `country` | `country` | 변수 | `<iso_country_code>` | 아니요(해제) |
| `locale` | `locale` | 변수 | `<locale_code>` | 아니요(해제) |
| `parentId` | `parentId` | 변수 | `<parent_category_id>` | 아니요(해제) |

**인증**

| 유형 | API 키 이름 | API 키 값 | 위치 |
| --- | --- | --- | --- |
| API 키 | apiKey | `<your_api_key>` | Header |

+++

### 바자르보이스 {#bazaarvoice}

>[!BEGINSHADEBOX]

Bazaarvoice는 등급, 리뷰 및 UGC API를 제공합니다.

일반적인 사용 사례는 정책이 허용될 때 이메일에 검토 요약 또는 등급을 표시하는 것입니다.

>[!ENDSHADEBOX]

+++ Bazaarvoice의 사전 요구 사항 및 제한 사항에 대해 자세히 알아보십시오.

다음 전제 조건이 적용됩니다.

* 계약의 API 암호 키 및 클라이언트 식별자.
* Journey Optimizer의 관리자 액세스 권한.

다음 제한 사항 및 제외가 적용됩니다.

* 등급 및 리뷰 표시는 Bazaarvoice 콘텐츠 정책을 따라야 합니다.
* API 키당 비율 제한 및 캐싱 규칙이 적용됩니다.

+++

아래 절차를 사용하여 Journey Optimizer에서 이 통합을 구성합니다. 요청 세부 정보는 **샘플 통합 필드**&#x200B;를 참조하고 해당 환경에 대한 공급업체 설명서를 통해 해당 값을 확인하십시오.

1. [통합 작업](integrations.md)을 따르십시오. `passkey`과(와) 함께 **GET**&#x200B;을(를) 대화 API의 쿼리 매개 변수로 사용하고, `Accept: application/json`을(를) 설정하고, 샘플 JSON을 붙여 넣고, 필드를 매핑하고, 테스트하고, 활성화하십시오.

1. Journey Optimizer에서 **[!UICONTROL 구성]** > **[!UICONTROL 관리]**(으)로 이동한 다음 **[!UICONTROL 통합 만들기]**&#x200B;를 선택합니다.

1. 통합 이름을 공백 없이 입력하십시오.

1. Bazaarvoice 대화 API를 사용하여 끝점을 구성합니다. 예제 URL 패턴:

   `https://api.bazaarvoice.com/...`

1. 별도로 명시되지 않는 한 구성 테이블에 표시된 HTTP 메서드(일반적으로 GET)를 선택합니다.

1. 표 및 공급업체 설명서에 지정된 대로 인증(헤더, 쿼리 매개 변수 또는 OAuth)을 구성합니다.

1. 경로, 쿼리 및 헤더 매개 변수를 정의하고 필요한 경우 프로필 또는 컨텍스트 데이터에 변수를 매핑합니다.

1. 필드를 감지하고 매핑할 수 있도록 샘플 JSON 응답을 붙여 넣습니다.

1. 응답 페이로드 매핑에서 개인화에 필요한 필드를 선택합니다.

1. 예상 볼륨을 기반으로 시간 제한, 재시도 및 캐싱 정책을 구성합니다.

1. 연결을 테스트한 다음 통합을 활성화합니다.

아래 표에는 이 통합 요청에 대한 예제 값이 나와 있습니다.

+++ 샘플 통합 필드

버전 및 필터 쿼리 매개 변수가 있는 `https://api.bazaarvoice.com/data/products.json` 진입점의 예입니다. [Bazaarvoice 개발자](https://developer.bazaarvoice.com/){target="_blank"}를 참조하세요.

| 필드 | 값 |
| --- | --- |
| **URL** | `https://api.bazaarvoice.com/data/products.json` |
| **HTTP 메서드** | `GET` |
| **정책** | 필요에 따라 정책 수준 세부 정보를 구성합니다. |
| **응답 페이로드** | API 응답을 기반으로 작성 중에 사용할 응답 필드를 선택하고 구성합니다. |

**머리글**

| 매개 변수 | 이름 | 유형 | 값 | 필수 |
| --- | --- | --- | --- | --- |
| 수락 | 수락 | 상수 | application/json | 예(켜기) |

**인증**

| 유형 | 키 값 | 위치 |
| --- | --- | --- |
| 암호 키 | `<YOUR_ACCESS_TOKEN>` | 쿼리 매개변수 |

**쿼리 매개 변수**

| 매개 변수 | 이름 | 유형 | 값 | 필수 |
| --- | --- | --- | --- | --- |
| `apiversion` | apiversionNumber | 상수 | 5.4 | 예(켜기) |
| `filter` | `filter` | 변수 | Id:47950830 | 아니요(해제) |
| `stats` | `stats` | 변수 | 모두 | 아니요(해제) |

+++

### OneTrust {#onetrust}

>[!BEGINSHADEBOX]

OneTrust는 개인 정보 및 동의 API(제품별 URL 및 스키마)를 노출합니다.

대표적인 사용 사례는 아키텍처 및 법률 검토를 허용하는 조건부 콘텐츠에 대한 동의 또는 환경 설정 신호를 읽는 것입니다.

>[!ENDSHADEBOX]

+++ OneTrust의 사전 요구 사항 및 제한 사항에 대해 자세히 알아보십시오.

다음 전제 조건이 적용됩니다.

* API 자격 증명 및 지역 기본 URL, 메시지에 사용되는 필드에 대한 법적 승인.
* Journey Optimizer의 관리자 액세스 권한.

다음 제한 사항 및 제외가 적용됩니다.

* 동의 및 환경 설정 데이터는 엄격하게 규제됩니다. 개인 정보 보호 및 법률 팀과 협력.
* API 경로 및 페이로드는 OneTrust 제품별로 다릅니다. 구독에 대한 설명서를 사용하십시오.

+++

아래 절차를 사용하여 Journey Optimizer에서 이 통합을 구성합니다. 요청 세부 정보는 **샘플 통합 필드**&#x200B;를 참조하고 해당 환경에 대한 공급업체 설명서를 통해 해당 값을 확인하십시오.

1. [통합 작업](integrations.md)을 따르십시오. 게시된 스키마 또는 환경 설정 센터 경로를 사용하여 구독 문서를 만들고, 필요한 경우 OAuth를 완료하고, 샘플 JSON을 붙여넣고, 필드를 매핑하고, 테스트하고, 활성화합니다.

1. Journey Optimizer에서 **[!UICONTROL 구성]** > **[!UICONTROL 관리]**(으)로 이동한 다음 **[!UICONTROL 통합 만들기]**&#x200B;를 선택합니다.

1. 통합 이름을 공백 없이 입력하십시오.

1. OneTrust API를 사용하여 끝점을 구성합니다. 테넌트, 제품 및 경로는 구독의 [OneTrust](https://developer.onetrust.com/){target="_blank"} 설명서에서 가져온 것입니다. 예제 URL 패턴:

   `https://{tenant}.my.onetrust.com/api/...`

1. 별도로 명시되지 않는 한 구성 테이블에 표시된 HTTP 메서드(일반적으로 GET)를 선택합니다.

1. 표 및 공급업체 설명서에 지정된 대로 인증(헤더, 쿼리 매개 변수 또는 OAuth)을 구성합니다.

1. 경로, 쿼리 및 헤더 매개 변수를 정의하고 필요한 경우 프로필 또는 컨텍스트 데이터에 변수를 매핑합니다.

1. 필드를 감지하고 매핑할 수 있도록 샘플 JSON 응답을 붙여 넣습니다.

1. 응답 페이로드 매핑에서 개인화에 필요한 필드를 선택합니다.

1. 예상 볼륨을 기반으로 시간 제한, 재시도 및 캐싱 정책을 구성합니다.

1. 연결을 테스트한 다음 통합을 활성화합니다.

아래 표에는 이 통합 요청에 대한 예제 값이 나와 있습니다.

+++ 샘플 통합 필드

| 필드 | 값 |
| --- | --- |
| **URL** | `https://customer.my.onetrust.com/api/consentmanager/v2/preferencecenters/{{preferencecenterid}}/schema` |
| **HTTP 메서드** | `GET` |
| **정책** | 필요에 따라 정책 수준 세부 정보를 구성합니다. |
| **응답 페이로드** | API 응답을 기반으로 작성 중에 사용할 응답 필드를 선택하고 구성합니다. |
| **인증** | OAuth |

**경로 매개 변수**

| 매개 변수 | 이름 | 값 |
| --- | --- | --- |
| `preferencecenterid` | `preferencecenterid` | `<pref-id>` |

**머리글**

| 매개 변수 | 이름 | 유형 | 값 | 필수 |
| --- | --- | --- | --- | --- |
| 수락 | 수락 | 상수 | application/json | 예(켜기) |

**쿼리 매개 변수**

| 매개 변수 | 이름 | 유형 | 값 | 필수 |
| --- | --- | --- | --- | --- |
| `state` | `state` | 상수 | 게시됨 | 예 |

+++

#### 환경 설정 센터 스키마(게시됨)

예제 패턴(조각): `https://{tenant}.my.onetrust.com/api/consentmanager/v2/preferencecenters/{preferencecenterid}/schema?state=PUBLISHED`. [OneTrust Developer](https://developer.onetrust.com/){target="_blank"}에서 정확한 경로를 확인하십시오.

### Meta {#meta}

>[!BEGINSHADEBOX]

Meta Graph 및 Marketing API는 인증된 비즈니스 통합을 위해 카탈로그 및 캠페인 오브젝트를 노출합니다.

일반적인 사용 사례는 토큰과 정책이 허용하는 Meta의 속성으로 콘텐츠를 보강하는 것입니다.

>[!ENDSHADEBOX]

+++ Meta에 대한 사전 요구 사항 및 제한 사항에 대해 자세히 알아보십시오.

다음 전제 조건이 적용됩니다.

* 올바른 권한이 있는 시스템 사용자 또는 앱 토큰, Business Manager 정렬.
* Journey Optimizer의 관리자 액세스 권한.

다음 제한 사항 및 제외가 적용됩니다.

* 단기 액세스 토큰은 서버측 통합에 적합한 갱신 또는 장기 전략이 필요합니다.
* Meta 플랫폼 약관을 준수합니다. 메시지 페이로드에 토큰이나 기타 비밀을 기록하지 마십시오.

+++

아래 절차를 사용하여 Journey Optimizer에서 이 통합을 구성합니다. 요청 세부 정보는 **샘플 통합 필드**&#x200B;를 참조하고 해당 환경에 대한 공급업체 설명서를 통해 해당 값을 확인하십시오.

1. [통합 작업](integrations.md)을 따르십시오. 그래프 호출은 종종 버전이 지정된 경로를 사용하는 **GET**&#x200B;입니다. 토큰 만료 처리, 샘플 JSON 붙여넣기, 맵 필드, 테스트, 활성화 등을 수행합니다.

1. Journey Optimizer에서 **[!UICONTROL 구성]** > **[!UICONTROL 관리]**(으)로 이동한 다음 **[!UICONTROL 통합 만들기]**&#x200B;를 선택합니다.

1. 통합 이름을 공백 없이 입력하십시오.

1. Meta Graph API를 사용하여 끝점을 구성합니다. 예제 URL 패턴:

   `https://graph.facebook.com/vXX.X/...`

1. 별도로 명시되지 않는 한 구성 테이블에 표시된 HTTP 메서드(일반적으로 GET)를 선택합니다.

1. 표 및 공급업체 설명서에 지정된 대로 인증(헤더, 쿼리 매개 변수 또는 OAuth)을 구성합니다.

1. 경로, 쿼리 및 헤더 매개 변수를 정의하고 필요한 경우 프로필 또는 컨텍스트 데이터에 변수를 매핑합니다.

1. 필드를 감지하고 매핑할 수 있도록 샘플 JSON 응답을 붙여 넣습니다.

1. 응답 페이로드 매핑에서 개인화에 필요한 필드를 선택합니다.

1. 예상 볼륨을 기반으로 시간 제한, 재시도 및 캐싱 정책을 구성합니다.

1. 연결을 테스트한 다음 통합을 활성화합니다.

아래 표에는 이 통합 요청에 대한 예제 값이 나와 있습니다.

+++ 샘플 통합 필드

샘플 통합 필드. 버전 관리 및 액세스 토큰은 [Graph API](https://developers.facebook.com/docs/graph-api){target="_blank"}를 참조하십시오.

| 필드 | 값 |
| --- | --- |
| **URL** | `https://graph.facebook.com/{{API_VERSION}}/{{PRODUCT_CATALOG_ID}}/products` |
| **HTTP 메서드** | `GET` |
| 응답 페이로드 | API 응답을 기반으로 작성 중에 사용할 응답 필드를 선택하고 구성합니다. |
| 정책 | 필요에 따라 정책 수준 세부 정보를 구성합니다. |
| 인증 | OAuth |

**경로 매개 변수**

| 경로 매개 변수 | 이름 | 기본 값 |
| --- | --- | --- |
| `API_VERSION` | `API_VERSION` | `v19.0` |
| `PRODUCT_CATALOG_ID` | `PRODUCT_CATALOG_ID` | `12345` |

**머리글**

| 매개 변수 | 이름 | 유형 | 값 | 필수 |
| --- | --- | --- | --- | --- |
| 수락 | 수락 | 상수 | application/json | 예(켜기) |

**쿼리 매개 변수**

| 매개 변수 | 이름 | 유형 | 값 | 필수 |
| --- | --- | --- | --- | --- |
| `fields` | `fields` | 변수 | ID | 아니요 |
| `filter` | `filter` | 변수 | — | 아니요 |

+++

### 아프리모 {#aprimo}

>[!BEGINSHADEBOX]

Aprimo는 레코드, 에셋 및 메타데이터에 대한 마케팅 작업과 DAM API를 결합합니다.

일반적인 사용 사례에는 다이내믹 콘텐츠의 승인된 레코드 또는 에셋 필드와 규제 대상 산업의 관리 DAM 워크플로우가 포함됩니다.

>[!ENDSHADEBOX]

+++ Aprimo의 사전 요구 사항 및 제한 사항에 대해 자세히 알아보십시오.

다음 전제 조건이 적용됩니다.

* 테넌트 URL 및 자격 증명(설정에 따른 OAuth 또는 API 키).
* Journey Optimizer의 관리자 액세스 권한.

다음 제한 사항 및 제외가 적용됩니다.

* Aprimo 필드 수준 보안은 Journey Optimizer에서 매핑하는 속성과 일치해야 합니다.
* 큰 HAL 또는 JSON 페이로드: 매핑된 필드를 필요한 최소 세트로 제한합니다.

+++

아래 절차를 사용하여 Journey Optimizer에서 이 통합을 구성합니다. 요청 세부 정보는 **샘플 통합 필드**&#x200B;를 참조하고 해당 환경에 대한 공급업체 설명서를 통해 해당 값을 확인하십시오.

1. [통합 작업](integrations.md)을 따르십시오. 필요한 레코드 경로에서 **GET**&#x200B;을(를) 사용하고, `API-VERSION`과(와) 같은 필수 헤더를 보내고, 샘플 JSON(반환된 대로 HAL 또는 JSON)을 붙여 넣고, 최소 필드 집합을 매핑하고, 테스트하고, 활성화합니다.

1. Journey Optimizer에서 **[!UICONTROL 구성]** > **[!UICONTROL 관리]**(으)로 이동한 다음 **[!UICONTROL 통합 만들기]**&#x200B;를 선택합니다.

1. 통합 이름을 공백 없이 입력하십시오.

1. Aprimo DAM / Records API를 사용하여 끝점을 구성합니다. **테넌트**&#x200B;에 대한 API 기본 URL 및 레코드 경로(Aprimo당)를 사용합니다. 예제 URL 패턴:

   `https://{tenant}.dam.aprimo.com/`

1. 별도로 명시되지 않는 한 구성 테이블에 표시된 HTTP 메서드(일반적으로 GET)를 선택합니다.

1. 표 및 공급업체 설명서에 지정된 대로 인증(헤더, 쿼리 매개 변수 또는 OAuth)을 구성합니다.

1. 경로, 쿼리 및 헤더 매개 변수를 정의하고 필요한 경우 프로필 또는 컨텍스트 데이터에 변수를 매핑합니다.

1. 필드를 감지하고 매핑할 수 있도록 샘플 JSON 응답을 붙여 넣습니다.

1. 응답 페이로드 매핑에서 개인화에 필요한 필드를 선택합니다.

1. 예상 볼륨을 기반으로 시간 제한, 재시도 및 캐싱 정책을 구성합니다.

1. 연결을 테스트한 다음 통합을 활성화합니다.

아래 표에는 이 통합 요청에 대한 예제 값이 나와 있습니다.

+++ 샘플 통합 필드

| 필드 | 값 |
| --- | --- |
| **URL** | `https://productstrategy1.dam.aprimo.com/api/core/record/{{recordID}}` |
| **HTTP 메서드** | `GET` |

**경로 매개 변수**

| 경로 매개 변수 | 이름 | 기본 값 |
| --- | --- | --- |
| `recordId` | `recordId` | `<record_identifier>` |

**머리글**

| 매개 변수 | 이름 | 유형 | 값 | 필수 |
| --- | --- | --- | --- | --- |
| Content-Type(기본값) | Content-Type | 상수 | application/json | 예(켜기) |
| API-버전 | API-버전 | 상수 | 1 | 예(켜기) |
| 수락 | 수락 | 상수 | application/hal+json 또는 application/json | 아니요(해제) |
| select-record | select-record | 변수 | `<selection_type>` | 아니요(해제) |
| 레코드 필드 선택 | 레코드 필드 선택 | 변수 | `<field_list>` | 아니요(해제) |
| 필드 선택 | 필드 선택 | 변수 | `<field_selection>` | 아니요(해제) |

**인증**

| 유형 | API 키 이름 | API 키 값 | 위치 |
| --- | --- | --- | --- |
| API 키 | Authorization | 전달자 `<token>` | Header |

+++

### 엡실론(엡실론3) {#epsilon}

>[!BEGINSHADEBOX]

Epsilon은 엔터프라이즈 계약당 API를 노출합니다. 기본 URL 및 인증은 계정 팀에서 가져옵니다(아래 이벤트 API 예는 설명).

일반적인 사용 사례는 지원되는 JSON API를 통해 충성도 또는 오퍼 속성을 노출하는 것입니다.

>[!ENDSHADEBOX]

+++ Epsilon(Epsilon3)의 사전 요구 사항 및 제한 사항에 대해 자세히 알아보십시오.

다음 전제 조건이 적용됩니다.

* Epsilon의 자격 증명 및 끝점, Journey Optimizer의 관리자 액세스

다음 제한 사항 및 제외가 적용됩니다.

* 엔드포인트와 호스트는 고객별로 다릅니다. Epsilon 계정 팀의 문서 없이 배포하지 마십시오.

+++

아래 절차를 사용하여 Journey Optimizer에서 이 통합을 구성합니다. 요청 세부 정보는 **샘플 통합 필드**&#x200B;를 참조하고 해당 환경에 대한 공급업체 설명서를 통해 해당 값을 확인하십시오.

1. [통합 작업](integrations.md)을 따르십시오. 공개 URL은 추측하지 마십시오. Epsilon의 사양을 사용하고, 샘플 JSON을 붙여넣고, 필드를 매핑하고, 테스트 및 활성화합니다.

1. Journey Optimizer에서 **[!UICONTROL 구성]** > **[!UICONTROL 관리]**(으)로 이동한 다음 **[!UICONTROL 통합 만들기]**&#x200B;를 선택합니다.

1. 통합 이름을 공백 없이 입력하십시오.

1. 통합 사양에 따라 Epsilon API를 사용하여 끝점을 구성합니다. 기본 URL 및 리소스 경로는 Epsilon 계정 팀에서 제공합니다. 예제 URL 패턴:

   `https://{your-instance}.epsilon3.io/api/...`

1. 별도로 명시되지 않는 한 구성 테이블에 표시된 HTTP 메서드(일반적으로 GET)를 선택합니다.

1. 표 및 공급업체 설명서에 지정된 대로 인증(헤더, 쿼리 매개 변수 또는 OAuth)을 구성합니다.

1. 경로, 쿼리 및 헤더 매개 변수를 정의하고 필요한 경우 프로필 또는 컨텍스트 데이터에 변수를 매핑합니다.

1. 필드를 감지하고 매핑할 수 있도록 샘플 JSON 응답을 붙여 넣습니다.

1. 응답 페이로드 매핑에서 개인화에 필요한 필드를 선택합니다.

1. 예상 볼륨을 기반으로 시간 제한, 재시도 및 캐싱 정책을 구성합니다.

1. 연결을 테스트한 다음 통합을 활성화합니다.

아래 표에는 이 통합 요청에 대한 예제 값이 나와 있습니다.

+++ 샘플 통합 필드

예제 패턴: `start` 및 `end` 쿼리 매개 변수와 헤더 기반 API 키가 있는 `https://{your-instance}.epsilon3.io/api/v1/planning/events`. 제작 전에 Epsilon과 확인합니다.

| 필드 | 값 |
| --- | --- |
| **URL** | `https://{{your-instance}}.epsilon3.io/api/v1/planning/events` |
| **HTTP 메서드** | `GET` |
| **정책** | 필요에 따라 정책 수준 세부 정보를 구성합니다. |
| **응답 페이로드** | API 응답을 기반으로 작성 중에 사용할 응답 필드를 선택하고 구성합니다. |

**경로 매개 변수**

| 경로 매개 변수 | 이름 | 기본 값 |
| --- | --- | --- |
| `your-instance` | `your-instance` | `<your_instance>` |

**머리글**

| 매개 변수 | 이름 | 유형 | 값 | 필수 |
| --- | --- | --- | --- | --- |
| Content-Type(기본값) | Content-Type | 상수 | application/json | 예(켜기) |

**쿼리 매개 변수**

| 매개 변수 | 이름 | 유형 | 값 | 필수 |
| --- | --- | --- | --- | --- |
| `start` | `start` | 변수 | 2019-08-24T14:15:22Z | 예(켜짐) * |
| `end` | `end` | 변수 | 2019-08-24T14:15:22Z | 예(켜짐) * |
| `eventType` | `eventType` | 변수 | 예약됨 / 예약되지 않음 | 아니요(해제) |
| `exclude_recurrences` | `exclude_recurrences` | 변수 | true / false | 아니요(해제) |

\* `eventType` = `unscheduled`의 경우 선택 사항이고 `exclude_recurrences` = `true`의 경우 선택 사항입니다.

**인증**

| 유형 | API 키 이름 | API 키 값 | 위치 |
| --- | --- | --- | --- |
| API 키 | `<your_username>` | `<EPSILON3_API_KEY>` | Header |

+++

