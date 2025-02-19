---
product: experience platform
solution: Experience Platform
title: 컨텍스트 데이터 및 의사 결정 요청
description: Decisioning 요청에서 컨텍스트 데이터를 전달하는 방법을 알아봅니다.
feature: Decision Management
role: Developer, Data Engineer
level: Experienced
source-git-commit: 9b66f4871d8b539bf0201b2974590672205a3243
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---


# 컨텍스트 데이터 및 의사 결정 요청 {#context-data-decisioning}

이 섹션에서는 의사 결정 요청에서 컨텍스트 데이터를 전달하고 자격 규칙에서 이를 사용하는 방법에 대해 안내합니다.

>[!BEGINSHADEBOX]

또한 컨텍스트를 **등급 수식**&#x200B;에 활용하여 오퍼를 높일 수 있습니다. 컨텍스트 데이터를 활용하는 등급 수식의 자세한 예는 [이 섹션](../offers/ranking/create-ranking-formulas.md#context-data)에서 확인할 수 있습니다.

>[!ENDSHADEBOX]

## 의사 결정 요청에 컨텍스트 데이터 전달

Decisioning 요청의 컨텍스트 데이터가 키 `xdm:ContextData`을(를) 사용하여 정의됩니다.

컨텍스트 데이터 속성은 XDM 스키마에 의해 제어되지 않습니다. JSON의 모든 컨텍스트 데이터를 Decisioning 요청 페이로드의 일부로 전달할 수 있습니다.

다음은 컨텍스트 데이터가 포함된 샘플 결정 요청입니다(`xdm:ContextData` 참조).

```
curl --location 'https://platform-stage.adobe.io/data/core/ods/decisions' \
--header 'Accept: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"' \
--header 'Content-Type: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0"' \
--header 'Authorization: Bearer eyJhbGciOi....' \
--header 'x-api-key: {{api_key}}' \
--header 'x-gw-ims-org-id: {{ims_org}}' \
--header 'x-sandbox-name: {{sandbox_name}}' \
--header 'x-request-id: {{$guid}}' \
--data-raw '{
    "xdm:propositionRequests": [
        {
            "xdm:activityId": "dps:offer-activity:19978bf95ebfc8fb",
            "xdm:placementId": "dps:offer-placement:199772e1c90d50ac"
        }
    ],
    "xdm:profiles": [
        {
            "xdm:identityMap": {
                "Email": [
                    {
                        "xdm:id": "test@test.com",
                        "primary": true
                    }
                ]
            },
            "xdm:contextData": [
                {
                    "@type": "_xdm.context.additionalParameters;version=1",
                    "xdm:data": {
                        "xdm:channel": "mobile",
                        "xdm:language": "en",
                        "xdm:isThirdParty": true,
                        "xdm:mobileVersion": "3.0.5106",
                        "xdm:mobileVersionMajor": "3",
                        "xdm:mobileVersionMinor": "0",
                        "xdm:mobileVersionPatch": "125",
                        "xdm:deviceType": "iOS",
                        "xdm:features": [
                            "p1000",
                            "p1001"
                        ]
                    }
                }
            ]
        }
    ],
    "xdm:allowDuplicatePropositions": {
        "xdm:acrossActivities": true,
        "xdm:acrossPlacements": true
    },
    "xdm:responseFormat": {
        "xdm:includeContent": true,
        "xdm:includeMetadata": {
            "xdm:activity": [
                "name"
            ],
            "xdm:option": [
                "name"
            ],
            "xdm:placement": [
                "name"
            ]
        }
    }
}'
```

## 자격 규칙에서 컨텍스트 데이터 사용

다음은 자격 규칙에서 의사 결정 요청에서 전달된 컨텍스트 데이터를 사용하는 방법을 보여 주는 예입니다.

* 컨텍스트 데이터 기능에 특정 값이 포함되어 있는지 여부:

  ```
  select contextData from @{_xdm.context.additionalParameters;version=1} where contextData.features AND (select personetic from contextData.features where personetic.contains("123"))
  ```

* 채널이 비어 있지 않고 모바일과 동일한 경우 적격:

  ```
  select contextData from @{_xdm.context.additionalParameters;version=1} where !contextData.channel.isNull() AND contextData.channel!="" AND contextData.channel="mobile"
  ```
