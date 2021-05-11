---
title: 시작하기
description: 오퍼 라이브러리 API를 사용하여 의사 결정 관리 엔진을 사용하여 주요 작업을 수행하는 방법을 알아봅니다.
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 7%

---

# 의사 결정 관리 API 개발자 가이드

이 개발자 안내서에서는 [!DNL Offer Library] API 사용을 시작하는 데 도움이 되는 단계를 제공합니다. 그런 다음 이 안내서는 의사 결정 관리 엔진을 사용하여 주요 작업을 수행하기 위한 샘플 API 호출을 제공합니다.

![](../assets/do-not-localize/how-to-video.png) [비디오에서 이 기능 살펴보기](#video)

## 전제 조건

이 가이드를 사용하려면 다음과 같은 Adobe Experience Platform 구성 요소에 대해 작업해야 합니다.

* [[!DNL Experience Data Model (XDM) System]](https://docs.adobe.com/content/help/ko-KR/experience-platform/xdm/home.html):고객 경험 데이터를  [!DNL Experience Platform] 구성하는 표준화된 프레임워크
   * [스키마 컴포지션의 기본 사항](https://docs.adobe.com/content/help/ko-KR/experience-platform/xdm/schema/composition.html):XDM 스키마의 기본 구성 요소에 대해 알아봅니다.
* [의사 결정 관리](../../../using/offers/get-started/starting-offer-decisioning.md):특히 Offer decisioning의 일반적인 경험 의사 결정에 사용되는 개념과 구성 요소에 대해 설명합니다. 고객 경험 중에 가장 적합한 옵션을 선택하는 데 사용되는 전략을 보여줍니다.
* [[!DNL Profile Query Language (PQL)]](https://docs.adobe.com/content/help/en/experience-platform/segmentation/pql/overview.html):PQL은 XDM 인스턴스 위에 표현식을 작성할 수 있는 강력한 언어입니다. PQL은 의사 결정 규칙을 정의하는 데 사용됩니다.

## 샘플 API 호출 읽기

이 안내서에서는 요청의 서식을 지정하는 방법을 보여주는 API 호출 예를 제공합니다. 여기에는 경로, 필수 헤더 및 올바른 형식의 요청 페이로드가 포함됩니다. API 응답으로 반환된 샘플 JSON도 제공됩니다. 샘플 API 호출에 대한 설명서에 사용된 규칙에 대한 자세한 내용은 [!DNL Experience Platform] 문제 해결 안내서의 [API 호출 예](https://docs.adobe.com/content/help/en/experience-platform/landing/troubleshooting.html#how-do-i-format-an-api-request)를 읽는 방법에 대한 섹션을 참조하십시오.

## 필수 헤더에 대한 값 수집

[!DNL Platform] API를 호출하려면 먼저 [인증 자습서](https://docs.adobe.com/content/help/en/experience-platform/tutorials/authentication.html)를 완료해야 합니다. 인증 자습서를 완료하면 아래와 같이 모든 [!DNL Experience Platform] API 호출에서 각 필수 헤더에 대한 값을 제공합니다.

* `Authorization: Bearer {ACCESS_TOKEN}`
* `x-api-key: {API_KEY}`
* `x-gw-ims-org-id: {IMS_ORG}`

페이로드(POST, PUT, PATCH)을 포함하는 모든 요청에는 추가 헤더가 필요합니다.

* `Content-Type: application/json`

## 컨테이너에 대한 액세스 관리

컨테이너는 다른 우려를 분리시키는 격리 메커니즘입니다. 컨테이너 ID는 모든 저장소 API에 대한 첫 번째 경로 요소입니다. 모든 의사 결정 개체는 컨테이너 내에 있습니다.

관리자는 비슷한 주체, 리소스 및 액세스 권한을 프로필에 그룹화할 수 있습니다. 이렇게 하면 관리 부담이 줄어들고 [Adobe Admin Console](https://adminconsole.adobe.com/)에서 지원됩니다. 프로필을 만들고 해당 프로필에 사용자를 할당하려면 조직의 Adobe Experience Platform 제품 관리자여야 합니다. 한 번에 특정 권한에 일치하는 제품 프로필을 만든 다음 해당 프로필에 사용자를 추가하는 것만으로 충분합니다. 프로필은 권한을 부여받은 그룹 역할을 하며 해당 그룹의 모든 실제 사용자 또는 기술 사용자는 이러한 권한을 상속받습니다.

관리자 권한이 부여된 [Adobe Admin Console](https://adminconsole.adobe.com/)을 통해 사용자에게 권한을 부여하거나 해지할 수 있습니다. 자세한 내용은 [액세스 제어 개요](https://docs.adobe.com/content/help/ko-KR/experience-platform/access-control/home.html)를 참조하십시오.

### 사용자가 액세스할 수 있는 컨테이너 및 통합 목록

**API 형식**

```http
GET /{ENDPOINT_PATH}?product={PRODUCT_CONTEXT}&property={PROPERTY}==decisioning
```

| 매개 변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 저장소 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/xcore/` |
| `{PRODUCT_CONTEXT}` | 제품 컨텍스트에 대한 연관성을 기준으로 컨테이너 목록을 필터링합니다. | `acp` |
| `{PROPERTY}` | 반환되는 컨테이너 유형을 필터링합니다. | `_instance.containerType==decisioning` |

**요청**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/?product=acp&property=_instance.containerType==decisioning' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**응답**

성공적인 응답은 의사 결정 관리 컨테이너와 관련된 정보를 반환합니다. 여기에는 컨테이너 ID의 값이 되는 `instanceId` 속성이 포함됩니다.

```json
{
    "_embedded": {
        "https://ns.adobe.com/experience/xcore/container": [
            {
                "instanceId": "{INSTANCE_ID}",
                "schemas": [
                    "https://ns.adobe.com/experience/xcore/container;version=0.5"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 2,
                "repo:createdDate": "2020-09-16T07:54:28.319959Z",
                "repo:lastModifiedDate": "2020-09-16T07:54:32.098139Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "containerType": "decisioning",
                    "repo:name": "{REPO_NAME}",
                    "dataCenter": "{DATA_CENTER}",
                    "parentName": "{PARENT_NAME}",
                    "parentId": "{PARENT_ID}"
                },
                "_links": {
                    "self": {
                        "href": "/containers/{INSTANCE_ID}"
                    }
                }
            }
        ]
    },
    "_links": {
        "self": {
            "href": "/?product=acp&property=_instance.containerType==decisioning",
            "@type": "https://ns.adobe.com/experience/xcore/hal/home"
        }
    }
}
```

## 다음 단계

이 문서에서는 컨테이너 ID 획득을 포함하여 [!DNL Offer Library] API를 호출하는 데 필요한 사전 요구 사항을 다룹니다. 이제 이 개발자 안내서에 제공된 샘플 호출을 진행하여 지침을 따라 수행할 수 있습니다.

## 자습서 비디오 {#video}

다음 비디오는 의사 결정 관리의 구성 요소에 대한 이해를 지원하기 위한 것입니다.

>[!NOTE]
>
>이 비디오는 Adobe Experience Platform 기반으로 구축된 Offer decisioning 응용 프로그램 서비스에 적용됩니다. 그러나 Journey Optimizer 컨텍스트에서 오퍼를 사용하기 위한 일반적인 지침을 제공합니다.

>[!VIDEO](https://video.tv.adobe.com/v/329919?quality=12)
