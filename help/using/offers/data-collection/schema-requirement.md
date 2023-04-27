---
product: experience platform
solution: Experience Platform
title: 이벤트 캡처 구성
description: 이벤트를 캡처하도록 오퍼 스키마를 구성하는 방법을 알아보십시오
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: f70ba749-f517-4e09-a381-243b21713b48
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 2%

---

# 데이터 수집 구성 {#schema-requirements}

결정 이벤트 이외의 이벤트 유형에 대한 피드백을 받으려면 페이지의 각 이벤트 유형에 대해 올바른 값을 설정해야 합니다 **경험 이벤트** Adobe Experience Platform으로 전송됩니다.

>[!CAUTION]
>
>각 이벤트 유형에 대해 데이터 집합에 사용되는 스키마에 가 있는지 확인합니다 **[!UICONTROL 경험 이벤트 - 제안 상호 작용]** 연결된 필드 그룹입니다. [자세히 알아보기](create-dataset.md)

다음은 JavaScript 코드에 구현해야 하는 스키마 요구 사항입니다.

>[!NOTE]
>
>의사 결정 관리에서 이러한 이벤트를 자동으로 생성하여 **[!UICONTROL 코드 결정 이벤트]** 데이터 세트<!--to check--> 자동 생성됩니다.

## 노출 횟수 추적

이벤트 유형과 소스가 다음과 같은지 확인합니다.

**경험 이벤트 유형:** `decisioning.propositionDisplay`
**소스:** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) 또는 배치 수집
+++**샘플 페이로드:**

```
{
    "@id": "a7864a96-1eac-4934-ab44-54ad037b4f2b",
    "xdm:timestamp": "2020-09-26T15:52:25+00:00",
    "xdm:eventType": "decisioning.propositionDisplay",
    "https://ns.adobe.com/experience/decisioning/propositions":
    [
        {
            "xdm:items":
            [
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee4",
                },
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee5",
                }
            ],
            "xdm:id": "3cc33a7e-13ca-4b19-b25d-c816eff9a70a", //decision event id - taken from experience event for "nextBestOffer"
            "xdm:scope": "scope:12cfc3fa94281acb", //decision scope id - taken from experience event for "nextBestOffer"
        }
    ]
}
```

+++

## 클릭 추적

이벤트 유형과 소스가 다음과 같은지 확인합니다.

**경험 이벤트 유형:** `decisioning.propositionInteract`
**소스:** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) 또는 배치 수집
+++**샘플 페이로드:**

```
{
    "@id": "a7864a96-1eac-4934-ab44-54ad037b4f2b",
    "xdm:timestamp": "2020-09-26T15:52:25+00:00",
    "xdm:eventType": "decisioning.propositionInteract",
    "https://ns.adobe.com/experience/decisioning/propositions":
    [
        {
            "xdm:items":
            [
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee4"
                },
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee5"
                },
            ],
            "xdm:id": "3cc33a7e-13ca-4b19-b25d-c816eff9a70a", //decision event id
            "xdm:scope": "scope:12cfc3fa94281acb", //decision scope id
        }
    ]
}
```

+++

## 사용자 지정 이벤트 추적

사용자 지정 이벤트의 경우, 데이터 집합에 사용되는 스키마에도 **[!UICONTROL 경험 이벤트 - 제안 상호 작용]** 필드 그룹과 연결되어 있지만, 이러한 이벤트에 태그를 지정하는 데 사용해야 하는 경험 이벤트 유형에 대한 특정 요구 사항은 없습니다.

<!--
## Using a ranking strategy {#using-ranking}

To use the ranking strategy you created above, follow the steps below:

Once a ranking strategy has been created, you can assign it to a placement in a decision. For more on this, see [Configure offers selection in decisions](../offer-activities/configure-offer-selection.md).

1. Create a decision.
1. Add a placement.
1. Add a collection.
1. Choose to rank offers by AI ranking (select it from the drop-down list).
1. Click Add ranking.
1. Select the ranking strategy that you created. All the details of the ranking strategy are displayed.
1. Click Next to confirm.
1. Save your decision.

It is now ready to be used in a decision to rank eligible offers for a placement (see [Configure offers selection in decisions](../offer-activities/configure-offer-selection.md)).
-->
