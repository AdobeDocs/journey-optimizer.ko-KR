---
solution: Journey Optimizer
product: Journey Optimizer
title: 이벤트 캡처 구성
description: 이벤트를 캡처하도록 오퍼 스키마를 구성하는 방법에 대해 알아봅니다
feature: Ranking, Datasets, Decision Management
role: Developer
level: Experienced
exl-id: ce3a2c33-c15b-436f-90b1-7373d7b2b1ca
version: Journey Orchestration
source-git-commit: f43b1ea0dd2197331329e24cb3d76eef0b5a9e86
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 1%

---

# 데이터 수집 구성 {#schema-requirements}

결정 이벤트 이외의 이벤트 유형에 대한 피드백을 받으려면 Adobe Experience Platform으로 전송된 **경험 이벤트**&#x200B;에서 각 이벤트 유형에 올바른 값을 설정해야 합니다.

>[!CAUTION]
>
>각 이벤트 유형에 대해 데이터 세트에 사용되는 스키마에 **[!UICONTROL 경험 이벤트 - 제안 상호 작용]** 필드 그룹이 연결되어 있는지 확인하십시오. <!--[Learn more](create-dataset.md)-->

다음은 JavaScript 코드에 구현해야 하는 스키마 요구 사항입니다.

## 노출 횟수 추적 {#track-impressions}

다음 필드가 올바르게 구성되었는지 확인하십시오.

**경험 이벤트 유형:** `decisioning.propositionDisplay`

**propositionEventType:** `_experience.decisioning.propositionEventType.display`

**Source:** Web.sdk/Alloy.js(`sendEvent command -> xdm : {eventType, interactionMixin}`) 또는 일괄 처리 수집

+++**샘플 페이로드:**

```json
{
  "_experience": {
    "decisioning": {
      "propositionEventType": {
        "display": 1
      },
      "proposition": [
        {
          "items": [
            {
              "itemSelection": {
                "rankingDetail": {
                  "algorithmID": "RANDOM",
                  "strategyID": "1YYKhS4MImWqIBrpudMIf4",
                  "trafficType": "random",
                  "step": "aiModel"
                },
                "selectionDetail": {
                  "selectionType": "selectionStrategy",
                  "strategyName": "not a real selection strategy",
                  "strategyID": "dps:selection-strategy:1b630b32da42125a",
                  "version": "35a6b5b1-62ff-4a4b-94cd-96852a59d89a"
                }
              },
              "name": "not a real offer",
              "id": "dps:14c7468e7f6271ff8023748a1146d11f05f77b7fc1368081:1b630a7d8d9f2g4j",
              "score": 0.9765416360350985
            }
          ],
          "scopeDetails": {
            "decisionPolicy": {
              "id": "01c3ad3d-6d41-4013-a88f-5a4975579179"
            },
            "decisionProvider": "EXD",
            "placement": {
              "id": "a99d6b1e-5930-4ba6-hd64-17a14bb15032#farouk-img-test"
            },
            "correlationID": "28ca161e-552c-464e-dh37-bc38d4ce944b-0"
          },
          "scope": "a99d6b1e-5930-4ba6-hd64-17a14bb15032#farouk-img-test",
          "id": "86fb8f37-0498-4533-9dab-c206690c1f67"
        }
      ],
      "exdRequestID": "edb61199-ef92-46c8-adc5-f622df5b9078"
    }
  },
  "eventType": "decisioning.propositionDisplay",
  "_id": "04b5384e-c09c-4df8-b6f0-7c476a51b219",
  "timestamp": "2025-10-07T20:22:00Z"
}
```

+++

## 클릭 수 추적 {#track-clicks}

다음 필드가 올바르게 구성되었는지 확인하십시오.

**경험 이벤트 유형:** `decisioning.propositionInteract`

**propositionEventType:** `_experience.decisioning.propositionEventType.interact`

**Source:** Web.sdk/Alloy.js(`sendEvent command -> xdm : {eventType, interactionMixin}`) 또는 일괄 처리 수집

제안 내의 각 오퍼에는 Adobe에서 생성한 고유 식별자인 추적 토큰이 포함됩니다. 이 토큰은 해당 클릭 또는 노출 이벤트에서 받은 그대로(변경 없이) 전달되어야 합니다. 추적 토큰을 일치시키면 Adobe은 사용자 작업을 올바른 오퍼 의사 결정과 정확하게 연결하여 다운스트림 보고 및 AI 기반 최적화를 가능하게 합니다.

+++**샘플 페이로드:**

```json
{
  "_experience": {
    "decisioning": {
      "propositionEventType": {
        "interact": 1
      },
      "propositionAction": {
        "tokens": [
          "Vx9fwWXmp6/kyYRVOUZWEQ"
        ]
      },
      "proposition": [
        {
          "items": [
            {
              "itemSelection": {
                "rankingDetail": {
                  "algorithmID": "RANDOM",
                  "strategyID": "1YYKhS4MImWqIBrpudMIf4",
                  "trafficType": "random",
                  "step": "aiModel"
                },
                "selectionDetail": {
                  "selectionType": "selectionStrategy",
                  "strategyName": "not a real selection strategy",
                  "strategyID": "dps:selection-strategy:1b630b32da42125a",
                  "version": "35a6b5b1-62ff-4a4b-94cd-96852a59d89a"
                }
              },
              "name": "not a real offer",
              "id": "dps:14c7468e7f6271ff8023748a1146d11f05f77b7fc1368081:1b630a7d8d9f2g4j",
              "score": 0.9765416360350985
            }
          ],
          "scopeDetails": {
            "decisionPolicy": {
              "id": "01c3ad3d-6d41-4013-a88f-5a4975579179"
            },
            "decisionProvider": "EXD",
            "placement": {
              "id": "a99d6b1e-5930-4ba6-hd64-17a14bb15032#farouk-img-test"
            },
            "correlationID": "28ca161e-552c-464e-dh37-bc38d4ce944b-0"
          },
          "scope": "a99d6b1e-5930-4ba6-hd64-17a14bb15032#farouk-img-test",
          "id": "86fb8f37-0498-4533-9dab-c206690c1f67"
        }
      ],
      "exdRequestID": "edb61199-ef92-46c8-adc5-f622df5b9078"
    }
  },
  "eventType": "decisioning.propositionInteract",
  "_id": "04b5384e-c09c-4df8-b6f0-7c476a51b765",
  "timestamp": "2025-10-07T20:50:00Z"
}
```

+++

## 사용자 지정 이벤트 추적 {#track-custom-events}

사용자 지정 이벤트의 경우 데이터 세트에 사용되는 스키마에도 **[!UICONTROL 경험 이벤트 - 제안 상호 작용]** 필드 그룹이 연결되어 있어야 하지만 경험 이벤트 유형에는 이러한 이벤트에 태그를 지정하는 데 사용해야 하는 특정 요구 사항이 없습니다.

<!--

>[!NOTE]
>
>To have your custom events accounted for in [capping](../items.md#capping), you need to connect the experience event to Adobe Experience Platform endpoints by sending it to either one of these two Edge data collection endpoints:
>
>* POST /ee/v2/interact
>* POST /ee/v2/collect
>
>If you are using the [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=ko){target="_blank"} or [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html?lang=ko){target="_blank"}, the connection is made automatically.-->
