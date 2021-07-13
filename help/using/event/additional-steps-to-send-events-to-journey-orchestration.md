---
title: 여정에 이벤트를 전송하는 추가 단계
description: 여정에 이벤트를 전송하는 추가 단계를 배웁니다.
feature: 이벤트
topic: 관리
role: Admin
level: Intermediate
source-git-commit: 63de381ea3a87b9a77bc6f1643272597b50ed575
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 4%

---

# 추가적인 이벤트 전송 단계 {#concept_xrz_n1q_y2b}

**[!UICONTROL Streaming Ingestion APIs]**&#x200B;에 전송하고 [!DNL Journey Optimizer]에 사용할 이벤트를 구성하려면 다음 단계를 수행해야 합니다.

1. Adobe Experience Platform API에서 인렛 URL을 가져옵니다. 자세한 내용은 [스트리밍 수집 API 개요](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html){target=&quot;_blank&quot;}를 참조하십시오.
1. **[!UICONTROL Event]** 메뉴의 페이로드 미리 보기에서 페이로드를 복사합니다. [이 페이지](../event/about-creating.md#define-the-payload-fields)에서 자세히 알아보십시오.

그런 다음 복사한 페이로드를 사용하여 이벤트를 스트리밍 수집 API로 푸시하는 데이터 시스템을 구성해야 합니다.

1. 스트리밍 수집 API URL(인렛이라고 함)에 대한 POST API 호출을 설정합니다.
1. 스트리밍 수집 API에 대한 API 호출의 본문(&quot;데이터 섹션&quot;)에 [!DNL Journey Optimizer]에서 복사한 페이로드를 사용합니다. 예를 보려면 아래를 참조하십시오
1. 페이로드에 있는 모든 변수를 가져올 위치를 결정합니다. 예: 이벤트가 주소를 전달해야 하는 경우 페이로드에 &quot;주소&quot;가 표시됩니다. &quot;string&quot;. &quot;string&quot;은 메시지를 보낼 사람의 이메일인 올바른 값을 자동으로 채우는 변수로 대체해야 합니다. 페이로드 미리 보기에서는 **[!UICONTROL Header]** 섹션에서 작업을 용이하게 할 것으로 예상되는 많은 값을 자동으로 채웁니다.
1. 본문 유형으로 &quot;application/json&quot;을 선택합니다.
1. 키 &quot;x-gw-ims-org-id&quot;를 사용하여 헤더에 IMS 조직 ID를 전달합니다. 값은 IMS 조직 ID(&quot;XXX@AdobeOrg&quot;)를 사용합니다.

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
            "timestamp": "2018-05-29T00:00:00.000Z",
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

&quot;데이터&quot; 부분을 붙여넣을 위치를 쉽게 식별할 수 있도록, [JSON 포맷터](https://jsonformatter.curiousconcept.com){target=&quot;_blank&quot;}와 같은 JSON 시각화 도구를 사용할 수 있습니다.

스트리밍 수집 API 문제를 해결하려면 [Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html){target=&quot;_blank&quot;}를 참조하십시오.
