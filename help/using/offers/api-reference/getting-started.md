---
title: 시작하기
description: Learn how to start using the Offer Library API to perform key operations using the Decision Management Engine.
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 773bee50-849f-4b07-9423-67de5279ad28
source-git-commit: 79d3bd42c208d38aaebce742e70b247106c21587
workflow-type: tm+mt
source-wordcount: '640'
ht-degree: 5%

---

# Decision Management API developer guide {#decision-management-api-developer-guide}

[!DNL Offer Library] The guide then provides sample API calls for performing key operations using the Decision Management Engine.

[](#video)

## 전제 조건 {#prerequisites}

This guide requires a working understanding of the following components of Adobe Experience Platform:

* [[!DNL Experience Data Model (XDM) System]](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko)[!DNL Experience Platform]
   * [](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=ko-KR)
* [](../../../using/offers/get-started/starting-offer-decisioning.md) Illustrates the strategies used for choosing the best option to present during a customer&#39;s experience.
* [[!DNL Profile Query Language (PQL)]](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html) PQL is used to define decision rules.

## Reading sample API calls {#reading-sample-api-calls}

This guide provides example API calls to demonstrate how to format your requests. These include paths, required headers, and properly formatted request payloads. Sample JSON returned in API responses is also provided. [](https://experienceleague.adobe.com/docs/experience-platform/landing/troubleshooting.html#how-do-i-format-an-api-request)[!DNL Experience Platform]

## Gather values for required headers {#gather-values-for-required-headers}

[!DNL Adobe Experience Platform][](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html) [!DNL Experience Platform]

* `Authorization: Bearer {ACCESS_TOKEN}`
* `x-api-key: {API_KEY}`
* `x-gw-ims-org-id: {IMS_ORG}`

All requests that contain a payload (POST, PUT, PATCH) require an additional header:

* `Content-Type: application/json`

## Manage access to a container {#manage-access-to-container}

A container is an isolation mechanism to keep different concerns apart. The container ID is the first path element for all repository APIs. All decisioning objects reside within a container.

An administrator can group similar principals, resources, and access permissions into profiles. [](https://adminconsole.adobe.com/) You must be a product administrator for Adobe Experience Platform in your organization to create profiles and assign users to them. It is sufficient to create product profiles that match certain permissions in a one-time step and then simply add users to those profiles. Profiles act as groups that have been granted permissions and every real user or technical user in that group inherits those permissions.

[](https://adminconsole.adobe.com/) [](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html?lang=ko)

### List containers accessible to users and integrations {#list-containers-accessible-to-users-and-integrations}

****

```http
GET /{ENDPOINT_PATH}?product={PRODUCT_CONTEXT}&property={PROPERTY}==decisioning
```

| 매개 변수 | 설명 | 예 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | The endpoint path for repository APIs. | `https://platform.adobe.io/data/core/xcore/` |
| `{PRODUCT_CONTEXT}` | Filters the list of containers by their association to product contexts. | `acp` |
| `{PROPERTY}` | Filters the type of container that is returned. | `_instance.containerType==decisioning` |

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

A successful response returns information regarding decision management containers. `instanceId`

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

[!DNL Offer Library] You can now proceed to the sample calls provided in this developer guide and follow along with their instructions.

>[!NOTE]
>
> The In-app messaging channel in Adobe Journey Optimizer uses offer decisioning objects. If your organization uses the in-app messaging channel, then API list requests for objects will include objects created by the in-app messaging service and can be ignored for offer decisioning use cases. `createdBy = “Mobile_Sheliak”`

## How-to video {#video}

The following video is intended to support your understanding of the components of Decision Management.

>[!VIDEO](https://video.tv.adobe.com/v/329919?quality=12)

