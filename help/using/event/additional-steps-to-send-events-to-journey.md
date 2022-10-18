---
solution: Journey Optimizer
product: journey optimizer
title: 여정에 이벤트를 전송하는 추가 단계
description: 여정에 이벤트를 전송하는 추가 단계를 배웁니다.
feature: Events
topic: Administration
role: Admin
level: Intermediate
exl-id: e0144151-6c54-4656-9650-b544d8e7be16
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 5%

---

# 이벤트를 보내는 추가적인 단계 {#additional-steps-to-send-events}

보낼 이벤트를 구성하려면 **[!UICONTROL 스트리밍 수집 API]** 및에 사용 [!DNL Journey Optimizer]를 채울 때는 다음 단계를 수행해야 합니다.

1. Adobe Experience Platform API에서 인렛 URL을 가져옵니다. 추가 정보 [스트리밍 수집 API 개요](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=ko){target=&quot;_blank&quot;}.
1. 의 페이로드 미리 보기에서 페이로드를 복사합니다. **[!UICONTROL 이벤트]** 메뉴 아래의 제품에서 사용할 수 있습니다. [이 페이지](../event/about-creating.md#define-the-payload-fields)에서 자세히 알아보십시오.

그런 다음 복사한 페이로드를 사용하여 이벤트를 스트리밍 수집 API로 푸시하는 데이터 시스템을 구성해야 합니다.

1. 스트리밍 수집 API URL(인렛이라고 함)에 대한 POST API 호출을 설정합니다.
1. 복사한 페이로드를 사용합니다 [!DNL Journey Optimizer] 를 클릭합니다. 예를 보려면 아래를 참조하십시오
1. 페이로드에 있는 모든 변수를 가져올 위치를 결정합니다. 예: 이벤트가 주소를 전달해야 하는 경우 페이로드에 &quot;주소&quot;가 표시됩니다. &quot;string&quot;. &quot;string&quot;은 메시지를 보낼 사람의 이메일인 올바른 값을 자동으로 채우는 변수로 대체해야 합니다. 페이로드 미리 보기에서 **[!UICONTROL Header]** 섹션을 통해 업무를 원활하게 수행할 수 있도록 많은 가치를 자동 채웁니다.
1. 본문 유형으로 &quot;application/json&quot;을 선택합니다.
1. 키 &quot;x-gw-ims-org-id&quot;를 사용하여 헤더에 조직 ID를 전달합니다. 값은 조직 ID(&quot;XXX@AdobeOrg&quot;)를 사용합니다.

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

&quot;데이터&quot; 부분을 붙여넣을 위치를 쉽게 식별할 수 있도록 다음과 같은 JSON 시각화 도구를 사용할 수 있습니다. [JSON 포맷터](https://jsonformatter.curiousconcept.com){target=&quot;_blank&quot;}.

스트리밍 수집 API 문제를 해결하려면 [Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html){target=&quot;_blank&quot;}.
