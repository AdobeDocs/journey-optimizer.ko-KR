---
solution: Journey Optimizer
product: journey optimizer
title: 오케스트레이션된 캠페인에 개인화 추가
description: 프로필 속성, 작업 테이블의 타겟 속성 및 데이터 보강 컬렉션 배열을 사용하여 오케스트레이션된 캠페인 메시지를 개인화하는 방법을 알아봅니다.
exl-id: c4a91e2b-6f08-4d1a-9e3b-2f8f5a0d1c62
version: Campaign Orchestration
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d556b755-390a-43f0-be32-a08cf6236126id: fe338112-e2ce-4876-8989-fc4d497613f1
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: e0a12bd7971c778378f9905cf93653792f38509d
workflow-type: tm+mt
source-wordcount: 477
ht-degree: 0%

---

# 오케스트레이션된 캠페인에 개인화 추가 {#add-personalization}

캔버스에서 [활동을 오케스트레이션](orchestrate-activities.md)하고 채널 활동을 추가하면 전자 메일, SMS 또는 기타 채널 편집기에서 메시지 콘텐츠를 개인화할 수 있습니다.

오케스트레이션된 캠페인의 Personalization은 다른 [!DNL Journey Optimizer] 캠페인 또는 여정과 유사하게 작동하며, **worktable**: 프로필 스토어의 데이터뿐만 아니라 캔버스에서 타겟팅 및 데이터 보강 활동을 통해 계산된 특성에도 차이가 있습니다.

## 개인화 편집기 액세스 {#access}

1. 오케스트레이션된 캠페인을 열고 채널 활동을 추가합니다. [채널 활동을 추가하는 방법 알아보기](activities/channels.md#add)

1. 채널 활동을 구성한 다음 **[!UICONTROL 콘텐츠]** 탭을 열고 메시지를 편집합니다.

1. 메시지 편집기에서 개인화 편집기를 사용하여 콘텐츠에 속성을 삽입합니다.

채널 활동에서 개인화된 콘텐츠를 미리 보고 테스트하려면 [콘텐츠 확인 및 테스트](activities/channels.md#simulate-content-test-profiles)를 참조하세요.

## 프로필 및 대상 속성 {#attributes}

개인화 편집기를 열면 두 개의 기본 폴더에 개인화에 사용할 수 있는 속성이 포함되어 있습니다.

* **[!UICONTROL 프로필 속성]**

  [!DNL Adobe Experience Platform]의 프로필 관련 데이터(이름, 이메일 주소, 위치 및 사용자 프로필에 캡처된 기타 트레이트).

* **[!UICONTROL Target 특성]**(오케스트레이션된 캠페인만 해당)

  작업 테이블의 캠페인 캔버스에서 계산된 속성입니다. 이 폴더에는 두 개의 하위 폴더가 있습니다.

   * **`<Targeting dimension>`**(예: 수신자 또는 구매) — 캠페인에서 타겟팅하는 차원과 관련된 속성입니다.

   * **`Enrichment`** — **[!UICONTROL 데이터 보강]** 활동(관계형 링크, 수집된 라인, 집계)을 통해 추가된 데이터입니다. 1:N **[!UICONTROL 데이터 수집]** 데이터 보강 후 번호 매기기 라인과 컬렉션 배열을 모두 가져옵니다. [데이터 보강 수집 데이터를 사용하여 작업하는 방법을 알아봅니다](#enrichment-collections)

[!DNL Journey Optimizer]의 개인화 편집기에 대한 자세한 개요는 [개인화 시작](../personalization/personalize.md)을 참조하세요.

## 데이터 보강 작업 {#enrichment-collections}

1:N 링크 및 **[!UICONTROL 데이터 수집]**&#x200B;을(를) 사용하여 **[!UICONTROL 데이터 보강]** 활동을 구성할 때 데이터 보강 특성은 두 가지 양식으로 **[!UICONTROL 대상 특성] > [!UICONTROL 데이터 보강]**&#x200B;에서 사용할 수 있습니다.

* **병합된 라인** — 검색된 라인당 하나의 필드(예: **구매 1**, **구매 2**, **구매 3**), 각 필드는 링크에서 선택한 특성(예: 가격 또는 제품)을 갖습니다. 별도의 고정 슬롯(예: `target.enrichment.purchase1.price`)이 필요한 경우 사용하십시오.

* **컬렉션 배열** — 링크 레이블에서 이름이 지정된 수집된 모든 행에 대한 하나의 배열입니다(예: **구매**). [배열 함수](#array-functions)를 사용하여 전체 레코드 집합에서 작업해야 할 때 사용합니다.

![](assets/enrichment-target-attributes-picker.png)

컬렉션 배열에서 플랫 라인을 식별하려면 표현식 편집기에 속성을 삽입하고 생성된 경로를 읽습니다. 컬렉션 배열은 경로가 **plural**(예: `purchases`)이고 줄 번호가 **없음**(`purchase1`, `purchase2` 등)인 항목입니다.

| 필요한 사항 | 표현식 편집기의 경로 |
| --- | --- |
| **수집된 한 줄** | **번호** — 예: `target.enrichment.purchase1.price` |
| **전체 컬렉션** | **Plural 및 unnumbered** — 예: `target.enrichment.purchases.price` |

[!DNL Journey Optimizer]의 다른 곳에서 사용된 것과 동일한 [배열 및 목록 함수](../personalization/functions/arrays-list.md)을(를) 데이터 보강 컬렉션에 적용하여 `target.enrichment.<label>`을(를) 참조할 수 있습니다.

예를 들어 제목란에서 수집된 구매의 수와 첫 번째 항목의 가격을 표시할 수 있습니다.

```sql
Hello number of Items: {%= count(target.enrichment.purchases.price) %} , Name of first item: {%= head(target.enrichment.purchases.product) %}
```

➡️ [캔버스에서 컬렉션 강화를 구성하는 방법을 알아봅니다](activities/enrichment.md#collection-personalization)
