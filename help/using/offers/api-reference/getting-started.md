---
title: 시작하기
description: 오퍼 라이브러리 API를 사용하여 의사 결정 관리 엔진을 사용하여 주요 작업을 수행하는 방법을 알아봅니다.
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 773bee50-849f-4b07-9423-67de5279ad28
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '611'
ht-degree: 6%

---

# 의사 결정 관리 API 개발자 안내서 {#decision-management-api-developer-guide}

이 개발자 가이드는 를 사용하는 데 도움이 되는 단계를 제공합니다. [!DNL Offer Library] API. 그러면 안내서에서는 결정 관리 엔진을 사용하여 주요 작업을 수행하기 위한 샘플 API 호출을 제공합니다.

➡️ [비디오에서 이 기능 살펴보기](#video)

## 전제 조건 {#prerequisites}

이 안내서에서는 Adobe Experience Platform의 다음 구성 요소를 이해하고 있어야 합니다.

* [[!DNL Experience Data Model (XDM) System]](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko){target=&quot;_blank&quot;}: 표준화된 프레임워크 [!DNL Experience Platform] 고객 경험 데이터를 구성합니다.
   * [스키마 작성 기본 사항](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=ko-KR){target=&quot;_blank&quot;}: XDM 스키마의 기본 구성 요소에 대해 알아봅니다.
* [의사 결정 관리](../../../using/offers/get-started/starting-offer-decisioning.md): 일반적으로 Experience Decisioning에 사용되는 개념과 구성 요소, 특히 Offer decisioning에 대해 설명합니다. 고객 경험 중에 가장 적합한 옵션을 선택하는 데 사용되는 전략을 보여줍니다.
* [[!DNL Profile Query Language (PQL)]](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html){target=&quot;_blank&quot;}: PQL은 XDM 인스턴스에서 표현식을 작성할 수 있는 강력한 언어입니다. PQL은 의사 결정 규칙을 정의하는 데 사용됩니다.

## 샘플 API 호출 읽기 {#reading-sample-api-calls}

이 안내서에서는 요청의 형식을 지정하는 방법을 보여주는 예제 API 호출을 제공합니다. 여기에는 경로, 필수 헤더 및 올바른 형식의 요청 페이로드가 포함됩니다. API 응답으로 반환되는 샘플 JSON도 제공됩니다. 샘플 API 호출에 대한 설명서에 사용된 규칙에 대한 자세한 내용은 [예제 API 호출을 읽는 방법](https://experienceleague.adobe.com/docs/experience-platform/landing/troubleshooting.html#how-do-i-format-an-api-request)의 {target=&quot;_blank&quot;} [!DNL Experience Platform] 문제 해결 가이드.

## 필수 헤더에 대한 값을 수집합니다 {#gather-values-for-required-headers}

을 호출하려면 [!DNL Platform] API를 먼저 완료해야 합니다. [인증 자습서](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html){target=&quot;_blank&quot;}. 인증 자습서를 완료하면 모든 히트에 필요한 각 헤더에 대한 값이 제공됩니다 [!DNL Experience Platform] 아래에 표시된 대로 API 호출:

* `Authorization: Bearer {ACCESS_TOKEN}`
* `x-api-key: {API_KEY}`
* `x-gw-ims-org-id: {IMS_ORG}`

페이로드(POST, PUT, PATCH)이 포함된 모든 요청에는 추가 헤더가 필요합니다.

* `Content-Type: application/json`

## 컨테이너에 대한 액세스 관리 {#manage-access-to-container}

용기는 서로 다른 관심사를 구분하기 위한 격리장치이다. 컨테이너 ID는 모든 저장소 API의 첫 번째 경로 요소입니다. 모든 의사 결정 개체는 컨테이너 내에 있습니다.

관리자는 유사한 주체, 리소스 및 액세스 권한을 프로필로 그룹화할 수 있습니다. 따라서 관리 부담이 줄어들고 [Adobe Admin Console](https://adminconsole.adobe.com/). 프로필을 만들고 사용자를 조직의 Adobe Experience Platform에 할당하려면 조직의 제품 관리자여야 합니다. 한 번에 하나의 권한과 일치하는 제품 프로필을 만든 다음 해당 프로필에 사용자를 추가하면 됩니다. 프로필은 권한이 부여된 그룹 역할을 하며 해당 그룹의 모든 실제 사용자 또는 기술 사용자는 해당 권한을 상속합니다.

지정된 관리자 권한이 있는 경우 [Adobe Admin Console](https://adminconsole.adobe.com/){target=&quot;_blank&quot;}. 자세한 내용은 [액세스 제어 개요](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html?lang=ko){target=&quot;_blank&quot;}.

### 사용자 및 통합에 액세스할 수 있는 컨테이너 나열 {#list-containers-accessible-to-users-and-integrations}

**API 형식**

```http
GET /{ENDPOINT_PATH}?product={PRODUCT_CONTEXT}&property={PROPERTY}==decisioning
```

| 매개 변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 저장소 API의 끝점 경로입니다. | `https://platform.adobe.io/data/core/xcore/` |
| `{PRODUCT_CONTEXT}` | 제품 컨텍스트에 대한 컨테이너 목록을 필터링합니다. | `acp` |
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

성공적인 응답은 결정 관리 컨테이너에 대한 정보를 반환합니다. 여기에는 다음이 포함됩니다 `instanceId` 속성. 값은 컨테이너 ID입니다.

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

## 다음 단계 {#next-steps}

이 문서는 [!DNL Offer Library] 컨테이너 ID 획득을 포함한 API. 이제 이 개발자 가이드에 제공된 샘플 호출을 진행하여 지침을 따라 수행할 수 있습니다.

## 튜토리얼 비디오 {#video}

다음 비디오는 의사 결정 관리의 구성 요소를 이해할 수 있도록 하기 위한 것입니다.

>[!NOTE]
>
>이 비디오는 Adobe Experience Platform을 기반으로 하는 Offer decisioning 애플리케이션 서비스에 적용됩니다. 그러나 Journey Optimizer 컨텍스트에서 오퍼를 사용하는 일반적인 지침을 제공합니다.

>[!VIDEO](https://video.tv.adobe.com/v/329919?quality=12)
