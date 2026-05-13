---
solution: Journey Optimizer
product: journey optimizer
title: 여정에 이벤트를 보내는 추가 단계
description: 이벤트를 여정에 전송하는 추가 단계 알아보기
feature: Journeys, Events
topic: Administration
role: Developer, Admin
level: Intermediate, Experienced
keywords: 단계, 구성, 여정, 이벤트, 스트림, API
exl-id: e0144151-6c54-4656-9650-b544d8e7be16
TQID: https://experienceleague.adobe.com/SiUXmerz2D-TYmIEXvaYk4usjRq67Y0v7V7sGVN-4vo
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: dd51b532-b93f-4bcf-8dbf-0d007f593aca
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 318
ht-degree: 5%

---

# 추가적인 이벤트 전송 단계 {#additional-steps-to-send-events}

**[!UICONTROL 스트리밍 수집 API]**&#x200B;에 보내고 [!DNL Journey Optimizer]에서 사용할 이벤트를 구성하려면 다음 단계를 수행해야 합니다.

1. Adobe Experience Platform API에서 인렛 URL을 가져옵니다. [수집 API 스트리밍 개요](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=ko){target="_blank"}에서 자세히 알아보세요.
1. **[!UICONTROL 이벤트]** 메뉴의 페이로드 미리 보기에서 페이로드를 복사합니다. [이 페이지](../event/about-creating.md#define-the-payload-fields)에서 자세히 알아보십시오.

>[!IMPORTANT]
>
>이벤트 요구 사항 및 제한 사항(스트리밍, 쿼리 서비스, 일괄 처리 수집)에 대해서는 [여정 보호 - 이벤트](../start/guardrails.md#events-g)를 참조하십시오.

그런 다음 복사한 페이로드를 사용하여 이벤트를 스트리밍 수집 API로 푸시하는 데이터 시스템을 구성해야 합니다.

1. 스트리밍 수집 API URL(인렛이라고 함)에 대한 POST API 호출을 설정합니다.
1. 스트리밍 수집 API에 대한 API 호출의 본문(&quot;데이터 섹션&quot;)에 있는 [!DNL Journey Optimizer]에서 복사한 페이로드를 사용합니다. 예제는 아래를 참조하십시오
1. 페이로드에 있는 모든 변수를 가져올 위치를 결정합니다. 예: 이벤트가 주소를 전달해야 하는 경우 붙여넣은 페이로드에 &quot;address&quot;: &quot;string&quot;이 표시됩니다. &quot;string&quot;은 올바른 값(메시지를 보낼 사람의 이메일)을 자동으로 채우는 변수로 대체해야 합니다. 페이로드 미리 보기의 **[!UICONTROL 헤더]** 섹션에서 작업을 용이하게 하기 위해 필요한 많은 값을 자동으로 채웁니다.
1. 본문 유형으로 &quot;application/json&quot;을 선택합니다.
1. &quot;x-gw-ims-org-id&quot; 키를 사용하여 헤더에 조직 ID를 전달합니다. 값에 조직 ID(&quot;XXX@AdobeOrg&quot;)를 사용합니다.

다음은 스트리밍 수집 API 이벤트의 예입니다.

```
{
    "header": {
        "msgType": "xdmEntityCreate",
        "msgId": "c25585b9-252e-431d-b562-e73da70c04e7",
        "msgVersion": "1.0",
        "xactionId": "f5995abe-c49d-4848-9577-a7a4fc2996fb",
        "datasetId": "string - required if you want the data to land in a specific dataset - not mandatory",
        "imsOrgId": "XXX@AdobeOrg",
        "schemaRef": {
            "id": "XXX",
            "contentType": "application/vnd.adobe.xed-full+json;version=1"
        },
        "source": {
            "name": "Journeys"
        }
    },
    "body": {
        "xdmMeta": {
            "schemaRef": {
                "id": "XXX",
                "contentType": "application/vnd.adobe.xed-full+json;version=1"
            }
        },
        "xdmEntity": {
            "_instance_name": {
                "person": {
                    "firstName": "string",
                    "lastName": "string",
                    "gender": "string",
                    "birthYear": 10,
                    "emailAddress": "string"
                }
            },
            "identityMap": {
                "Email": [
                {
                    "id": "string"
                    }
                ]
            },
            "_id": "string",
            "timestamp": "2023-05-29T00:00:00.000Z",
            "_experience": {
                "campaign": {
                    "orchestration": {
                    "eventID": "XXX"
                    }
                }
            }
        }
    }
}
```

&quot;데이터&quot; 부분을 붙여넣을 위치를 쉽게 확인하려면 [JSON 포맷터](https://jsonformatter.curiousconcept.com){target="_blank"}와 같은 JSON 시각화 도구를 사용할 수 있습니다.

스트리밍 수집 API의 문제를 해결하려면 [Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html?lang=ko){target="_blank"}를 참조하세요.
