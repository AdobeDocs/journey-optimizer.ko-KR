---
product: experience platform
solution: Experience Platform
title: 이벤트 캡처 구성
description: 이벤트를 캡처하도록 오퍼 스키마를 구성하는 방법에 대해 알아봅니다
feature: Ranking, Datasets, Decision Management
role: Developer, Data Engineer
level: Experienced
exl-id: f70ba749-f517-4e09-a381-243b21713b48
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 2%

---

# 데이터 수집 구성 {#schema-requirements}

의사 결정 이벤트 이외의 이벤트 유형에 대한 피드백을 받으려면 의 각 이벤트 유형에 대해 올바른 값을 설정해야 합니다. **경험 이벤트** Adobe Experience Platform으로 전송됩니다.

>[!CAUTION]
>
>각 이벤트 유형에 대해 데이터 세트에 사용되는 스키마에 **[!UICONTROL 경험 이벤트 - 제안 상호 작용]** 연결된 필드 그룹입니다. [자세히 알아보기](create-dataset.md)

다음은 JavaScript 코드에 구현해야 하는 스키마 요구 사항입니다.

>[!NOTE]
>
>의사 결정 관리에서 이러한 이벤트를 자동으로 생성하여 에 넣으므로 의사 결정 이벤트를 보낼 필요가 없습니다. **[!UICONTROL ODE DecisionEvents]** 데이터 세트<!--to check--> 자동으로 생성됩니다.

## 노출 횟수 추적 {#track-impressions}

이벤트 유형 및 소스가 다음과 같은지 확인합니다.

**경험 이벤트 유형:** `decisioning.propositionDisplay`
**소스:** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) 또는 일괄 처리 수집
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

## 클릭 수 추적 {#track-clicks}

이벤트 유형 및 소스가 다음과 같은지 확인합니다.

**경험 이벤트 유형:** `decisioning.propositionInteract`
**소스:** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) 또는 일괄 처리 수집
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

## 사용자 지정 이벤트 추적 {#track-custom-events}

사용자 지정 이벤트의 경우 데이터 세트에 사용되는 스키마에도 **[!UICONTROL 경험 이벤트 - 제안 상호 작용]** 연결된 필드 그룹이지만, 경험 이벤트 유형에는 이러한 이벤트에 태그를 지정하는 데 사용해야 하는 특정 요구 사항이 없습니다.

>[!NOTE]
>
>에서 사용자 지정 이벤트를 처리하려면 다음을 수행하십시오 [빈도 설정](../offer-library/add-constraints.md#capping), 경험 이벤트를 다음 두 Edge 데이터 수집 끝점 중 하나로 전송하여 Adobe Experience Platform 끝점에 연결해야 합니다.
>
>* POST /ee/v2/interact
>* POST /ee/v2/collect
>
>를 사용하는 경우 [Adobe Experience Platform 웹 SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=ko-KR){target="_blank"} or [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html){target="_blank"}, 연결이 자동으로 이루어집니다.
