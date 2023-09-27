---
title: 오퍼 게재 API 시작
description: 개인화된 오퍼를 제공하는 데 사용할 수 있는 API에 대해 자세히 알아보십시오.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 7bc1a4ec-113c-4af7-b549-ee17b843b818
source-git-commit: 805f7bdc921c53f63367041afbb6198d0ec05ad8
workflow-type: tm+mt
source-wordcount: '641'
ht-degree: 5%

---

# 오퍼 게재 API 시작 {#about-decisioning-apis}

다음 중 하나를 사용하여 오퍼를 게재할 수 있습니다. **의사 결정** 또는 **Edge Decisioning** API. 또한 **일괄 의사 결정** API를 사용하면 한 번의 호출로 주어진 대상의 모든 프로필에 오퍼를 게재할 수 있습니다. 대상의 각 프로필에 대한 오퍼 콘텐츠는 사용자 지정 일괄 처리 워크플로우에 사용할 수 있는 Adobe Experience Platform 데이터 세트에 배치됩니다.

이 페이지에서는 사용 가능한 특정 기능에 대한 정보를 확인할 수 있습니다. **의사 결정** 및 **Edge Decisioning** API. 둘 다 고객에게 오퍼를 게재할 수 있지만 **Edge Decisioning** 인바운드 사용 사례와 플랫폼에서 더 나은 지연 시간 및 처리량을 보장하기 위해 가능한 한 항상 API입니다.


API 작업 방법에 대한 자세한 내용은 다음 섹션을 참조하십시오.
* [Decisioning API](decisioning-api.md)
* [Edge Decisioning API](edge-decisioning-api.md)
* [Batch Decisioning API](batch-decisioning-api.md)

## 컨테이너에 대한 액세스 관리 {#manage-access-to-container}

용기는 서로 다른 문제를 분리하기 위한 격리 메커니즘입니다. 컨테이너 ID는 모든 저장소 API의 첫 번째 경로 요소입니다. 모든 의사 결정 개체는 컨테이너 내에 있습니다.

관리자는 유사한 주도자, 리소스 및 액세스 권한을 프로필로 그룹화할 수 있습니다. 이렇게 하면 관리 부담이 줄어들고 [Adobe Admin Console](https://adminconsole.adobe.com/). 프로필을 만들고 사용자를 조직에 할당하려면 Adobe Experience Platform의 제품 관리자여야 합니다. 1회 단계에서 특정 권한과 일치하는 제품 프로필을 만든 다음 해당 프로필에 사용자를 추가하면 됩니다. 프로필은 권한이 부여된 그룹 역할을 하며 해당 그룹의 모든 실제 사용자 또는 기술 사용자는 이러한 권한을 상속합니다.

관리자 권한이 주어지면 다음을 통해 사용자에게 권한을 부여하거나 철회할 수 있습니다. [Adobe Admin Console](https://adminconsole.adobe.com/){target="_blank"}. For more information, see the [Access control overview](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html?lang=ko){target="_blank"}.

### 사용자 및 통합에 액세스할 수 있는 목록 컨테이너 {#list-containers-accessible-to-users-and-integrations}

**API 형식**

```http
GET /{ENDPOINT_PATH}?product={PRODUCT_CONTEXT}&property={PROPERTY}==decisioning
```

| 매개변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 저장소 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/xcore/` |
| `{PRODUCT_CONTEXT}` | 제품 컨텍스트와의 연관성을 기준으로 컨테이너 목록을 필터링합니다. | `acp` |
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

성공적인 응답은 의사 결정 관리 컨테이너에 대한 정보를 반환합니다. 여기에는 다음이 포함됩니다. `instanceId` 속성. 값이 컨테이너 ID입니다.

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

## Edge Decisioning API 기능 {#edge}

**경험 이벤트 및 의사 결정 요청에 대한 고유 요청**

Edge Decisioning API를 사용하면 두 개의 서로 다른 요청이 없는 대신, 하나의 단일 요청에서 Decisioning 요청과 함께 경험 이벤트 자체를 보낼 수 있습니다.

예를 들어 고객이 웹 사이트를 방문하는 경우 요청에는 경험 이벤트(고객의 페이지 방문)가 포함되고, 오퍼를 다시 가져와서 방문한 페이지를 채웁니다.

**Adobe Experience Platform에 컨텍스트 데이터 스토리지**

컨텍스트 데이터는 오퍼를 반환하려는 시점에만 알고 있는 데이터를 나타냅니다. 예를 들어 구입한 문서의 색상, 구입 시 날씨 등이 여기에 해당합니다.

Edge Decisioning API 요청을 사용하여 컨텍스트 데이터를 전달할 때 데이터가 Adobe Experience Platform 프로필에 저장되므로 나중에 다시 사용할 수 있습니다.

>[!NOTE]
>
>컨텍스트 데이터를 저장하려면 전용 XDM 스키마가 구성되어 있어야 합니다.

## API 기능 결정 {#decisioning}

아래 나열된 기능은 Decisioning API를 통해서만 사용할 수 있습니다. 이들 중 하나를 활용하여 요구 사항을 충족해야 하는 경우 Decisioning API를 사용하십시오. 그렇지 않으면 Edge Decisioning API를 사용하는 것이 좋습니다.

* **경험 이벤트**: 경험 이벤트를 활용하여 의사 결정 규칙을 만듭니다.
* **오퍼 콘텐츠 및 특성**: 전용 옵션을 사용하여 오퍼의 콘텐츠 및 특성을 반환하지 않도록 선택할 수 있습니다.
* **오퍼 메타데이터**: 오퍼의 메타데이터를 반환하는 옵션을 활성화합니다.
* **병합 정책**: 샌드박스에 연결된 정책과 다른 병합 정책을 요청에 사용합니다.
* **이벤트 및 빈도 결정**: 발생하는 빈도 캡핑에 의해 이벤트 계산이 차단됩니다.
* **중복 제안**: 제안에 대한 중복 제거를 수행하지 않는 옵션을 활성화합니다.
