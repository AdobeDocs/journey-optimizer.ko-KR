---
title: 컬렉션 수식어 목록 만들기
description: 컬렉션 구분자를 사용하면 오퍼를 보다 잘 구성하고 정렬할 수 있습니다.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 8cee44ed-5569-416c-b463-e75fb20d4c9c
source-git-commit: 835e4bf227ce330b1426a9a4331fdf533fc757e3
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 4%

---

# 컬렉션 수식어 목록 만들기 {#list-tags}

컬렉션 구분자(이전에 &quot;태그&quot;라고 함)를 사용하면 오퍼를 보다 잘 구성하고 정렬할 수 있습니다. 예를 들어 블랙 프라이데이 컬렉션 한정자로 블랙 프라이데이 오퍼에 레이블을 지정할 수 있습니다. 그런 다음 오퍼 라이브러리에서 검색 기능을 사용하여 해당 컬렉션 한정자가 있는 모든 오퍼를 쉽게 찾을 수 있습니다.

컬렉션 구분자는 오퍼를 컬렉션으로 함께 그룹화하는 데 사용할 수도 있습니다. 자세한 내용은 [컬렉션 만들기](../../../offer-library/creating-collections.md).

단일 GET 요청을 수행하여 컨테이너 내의 모든 수집 구분자 목록을 볼 수 있습니다 [!DNL Offer Library] API.

**API 형식**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_TAG}&{QUERY_PARAMS}
```

| 매개 변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 저장소 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 수집 구분자가 있는 컨테이너입니다. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_TAG}` | 컬렉션 한정자와 연결된 스키마를 정의합니다. | `https://ns.adobe.com/experience/offer-management/tag;version=0.1` |
| `{QUERY_PARAMS}` | 결과를 기준으로 필터링할 선택적 쿼리 매개 변수입니다. | `limit=2` |

**요청**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/tag;version=0.1&limit=2' \
  -H 'Accept: *,application/vnd.adobe.platform.xcore.hal+json; schema="https://ns.adobe.com/experience/xcore/hal/results"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

## 쿼리 매개 변수 사용 {#using-query-parameters}

리소스를 나열할 때 쿼리 매개 변수를 사용하여 결과를 페이지 및 필터링할 수 있습니다.

### 페이징 {#paging}

페이징의 가장 일반적인 쿼리 매개 변수는 다음과 같습니다.

| 매개 변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `q` | 선택한 필드에서 검색할 선택적 쿼리 문자열입니다. 쿼리 문자열은 소문자여야 하며 큰따옴표로 묶어서 토큰화되지 않도록 하고 특수 문자를 이스케이프 처리할 수 있습니다. 문자 `+ - = && || > < ! ( ) { } [ ] ^ \" ~ * ? : \ /` 에는 특별한 의미가 있으며 쿼리 문자열에 나타나면 백슬래시로 이스케이프해야 합니다. | 웹 사이트 JSON |
| `qop` | q 쿼리 문자열 매개 변수의 값에 AND 또는 OR 연산자를 적용합니다. | `AND` / `OR` |
| `field` | 검색을 다음으로 제한할 필드 선택 사항입니다. 이 매개 변수는 다음과 같이 반복할 수 있습니다. field=field1[,field=field2,..] 및 (경로 표현식은 _instance.xdm:name과 같이 점으로 구분된 경로의 형식입니다.) | `_instance.xdm:name` |
| `orderBy` | 특정 속성별로 결과를 정렬합니다. 추가 `-` 이전 제목 (`orderby=-title`)은 제목별로 항목을 내림차순으로 정렬합니다(Z-A). | `-repo:createdDate` |
| `limit` | 반환된 컬렉션 구분자 수를 제한합니다. | `limit=5` |

**응답**

성공적인 응답은 액세스 권한이 있는 컨테이너 내에 있는 컬렉션 구분자 목록을 반환합니다.

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/tag;version=0.1",
    "requestTime": "2020-10-21T20:28:21.521267Z",
    "_embedded": {
        "results": [
            {
                "instanceId": "0adf2ef0-0f6e-11eb-b3be-9b775f952952",
                "schemas": [
                    "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 2,
                "repo:createdDate": "2020-10-16T05:11:26.815213Z",
                "repo:lastModifiedDate": "2020-10-16T22:20:20.190006Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "xdm:name": "Sneakers",
                    "@id": "xcore:tag:1246d138ec8cca1f"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/tag;version=0.1#0adf2ef0-0f6e-11eb-b3be-9b775f952952",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/0adf2ef0-0f6e-11eb-b3be-9b775f952952",
                        "@type": "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
                    }
                }
            },
            {
                "instanceId": "149e0de0-ff5f-11ea-b017-f98866426d43",
                "schemas": [
                    "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 1,
                "repo:createdDate": "2020-09-25T18:44:02.109748Z",
                "repo:lastModifiedDate": "2020-09-25T18:44:02.109748Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "xdm:name": "retirement",
                    "@id": "xcore:tag:122c81d2804e69e3"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/tag;version=0.1#149e0de0-ff5f-11ea-b017-f98866426d43",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/149e0de0-ff5f-11ea-b017-f98866426d43",
                        "@type": "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
                    }
                },
                "sandboxName": "ode-prod-va7-edge-testing"
            }
        ],
        "total": 11,
        "count": 2
    },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/tag;version=0.1&limit=2",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        },
        "next": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?start=149e0de0-ff5f-11ea-b017-f98866426d43&orderby=instanceId&schema=https://ns.adobe.com/experience/offer-management/tag;version=0.1&limit=2",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
    }
}
```
