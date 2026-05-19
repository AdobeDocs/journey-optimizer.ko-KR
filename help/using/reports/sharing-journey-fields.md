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
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4ebid: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2: id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 130
ht-degree: 6%

---

# 여정 필드 {#sharing-journey-fields}

이 필드 그룹은 **journeyStepEvent**&#x200B;과(와) 관련하여 **여정** 스키마에서 사용됩니다. 여기에는 아래 나열된 필드가 포함되어 있습니다.


>[!NOTE]
>
>이 섹션](../building-journeys/expression/journey-properties.md#journey-properties-fields)에서 여정 속성 특성 [에 대해 자세히 알아보세요.


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
