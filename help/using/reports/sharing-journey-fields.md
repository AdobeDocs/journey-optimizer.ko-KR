---
solution: Journey Optimizer
product: journey optimizer
title: 여정 필드
description: 여정 필드
feature: Journeys, Reporting
topic: Content Management
role: Developer, Admin
level: Experienced
exl-id: 177b4a97-c757-40ca-a190-fbd88169e5e2
TQID: https://experienceleague.adobe.com/dpQ6PEm-afX4PZuWSPrpAWDH7yBhUKZHZRF134VehAg
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a9f73820-6899-47c2-a597-3fec28ab756a
  - id: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04
subfeature_v2:
  - id: d145add9-d5b9-481b-aa8a-e15e6bb7f813
  - id: a7289281-9ae4-47b1-b8cf-4028b98af776
  - id: b5afe8bf-bda6-41b5-ba06-922638872d63
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: 7f28f19b11ead867b0851943fdd997dcc3af170b
workflow-type: tm+mt
source-wordcount: 159
ht-degree: 5%

---

# 여정 필드 {#sharing-journey-fields}

>[!BEGINSHADEBOX]

**이 페이지에서:** 여정 스키마에 사용된 여정 필드를 참조하여 여정 단계 이벤트 보고에서 각 여정(예: 여정 ID, 버전, 이름, 설명)를 설명하십시오.

>[!ENDSHADEBOX]

이 필드 그룹은 **journeyStepEvent**&#x200B;과(와) 관련하여 **여정** 스키마에서 사용됩니다. 여기에는 아래 나열된 필드가 포함되어 있습니다.


>[!NOTE]
>
>이 섹션[&#128279;](../building-journeys/expression/journey-properties.md#journey-properties-fields)에서 여정 속성 특성 에 대해 자세히 알아보세요.


## journeyID {#journeyid-field}

기본 여정 ID.

유형: 문자열

## 여정 버전 ID {#journeyversionid-field}

여정 버전 ID. 이 ID는 여정 ID를 나타냅니다.

유형: 문자열

## 이름 {#name-field}

여정 이름.

유형: 문자열

>[!NOTE]
>
>여정 이름은 여정 실행 데이터를 보고 데이터 세트와 연결하는 데 사용됩니다. 여정 이름을 바꾸는 경우 정확한 보고를 유지하기 위해 새 이름이 보고 데이터 세트의 이름과 일치하는지 확인하십시오. 불일치로 인해 보고 데이터가 예상대로 표시되지 않을 수 있습니다. [누락된 보고 데이터 문제 해결](../building-journeys/report-journey.md#troubleshooting-missing-data)에 대해 자세히 알아보세요.

## 설명 {#description-field}

여정에 대한 설명.

유형: 문자열

## version {#version-field}

버전, `major`.`minor`(으)로 표시됨

유형: 문자열
