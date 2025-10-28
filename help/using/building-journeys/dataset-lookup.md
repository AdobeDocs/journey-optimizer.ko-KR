---
solution: Journey Optimizer
product: journey optimizer
title: 여정에서 Adobe Experience Platform 데이터 사용
description: Adobe Journey Optimizer에서 데이터 세트 조회 활동 을 사용하여 Adobe Experience Platform의 외부 데이터로 고객 여정을 보강하는 방법을 알아봅니다.
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
version: Journey Orchestration
exl-id: b6f54a79-b9e7-4b3a-9a6f-72d5282c01d3
source-git-commit: ccd9f1aa3359875796104d9789d5dd8c0279c0c1
workflow-type: tm+mt
source-wordcount: '750'
ht-degree: 15%

---

# 여정에서 [!DNL Adobe Experience Platform] 데이터 사용 {#datalookup}

>[!CONTEXTUALHELP]
>id="ajo_journey_dataset_lookup"
>title="데이터 세트 조회 활동"
>abstract="**[!UICONTROL 데이터 세트 조회]** 활동을 사용하면 런타임 중에 Adobe Experience Platform 레코드 데이터 세트의 데이터를 동적으로 검색할 수 있습니다. 이 기능을 활용하면 프로필이나 이벤트 페이로드에 없을 수 있는 데이터에 액세스하여 고객 상호 작용이 적시에 적절하게 이루어질 수 있습니다."

**[!UICONTROL 데이터 세트 조회]** 활동을 사용하면 런타임 중에 Adobe Experience Platform 레코드 데이터 세트의 데이터를 동적으로 검색할 수 있습니다. 이 기능을 활용하면 프로필이나 이벤트 페이로드에 없을 수 있는 데이터에 액세스하여 고객 상호 작용이 적시에 적절하게 이루어질 수 있습니다.

주요 이점:

* **실시간 개인화**: 보강된 데이터를 사용하여 고객 경험을 사용자 지정합니다.
* **동적 의사 결정**: 외부 데이터를 사용하여 여정 논리와 작업을 실행합니다.
* **향상된 데이터 액세스**: 특정 키에 연결된 제품 메타데이터, 가격 테이블 또는 관계형 데이터를 검색합니다.

>[!AVAILABILITY]
>
>이 활동은 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.

## 반드시 알아야 할 사항 {#must-read}

### 데이터 세트 활성화

Adobe Experience Platform에서 조회를 위해 데이터 세트를 활성화해야 합니다. 자세한 정보는 이 섹션에서 확인할 수 있습니다. [Adobe Experience Platform 데이터 사용](../data/lookup-aep-data.md).

### 제한 및 제한 사항

* 데이터 세트당 최대 10개의 여정 조회 활동.
* 최대 20개의 선택된 필드.
* 조회 키 배열의 최대 50개 키.
* 보강된 데이터 크기는 10KB로 제한됩니다.

### 추가 성능 고려 사항

아래 권장 사항은 게재 기능의 지연을 방지하기 위한 지침입니다.

| 고려 사항 | 권장 제한 | 설명 |
| ------- | ------- | ------- |
| 조회당 속성 | 최대 20개 | 단일 조회 활동에서 레코드당 검색된 데이터 필드 수입니다. |
| 조회 활동 | 여정 당 최대 5개 | 각 여정은 최대 5개의 개별 조회 활동을 포함할 수 있습니다. 각 조회는 다른 데이터 세트를 타깃팅할 수 있습니다. |

## 데이터 세트 조회 활동 구성 {#configure}

**[!UICONTROL 데이터 집합 조회]** 활동을 구성하려면 다음 단계를 수행합니다.

1. **[!UICONTROL Orchestration]** 범주를 펼친 다음 **[!UICONTROL 데이터 집합 조회]** 활동을 캔버스에 놓습니다.

   ![](assets/aep-data-activity.png)

1. 레이블과 설명을 추가합니다.

1. **[!UICONTROL 데이터 집합]** 필드에서 필요한 특성이 있는 데이터 집합을 선택합니다.

   >[!NOTE]
   >
   >찾고 있는 데이터 세트가 목록에 표시되지 않는 경우 조회를 위해 활성화했는지 확인하십시오. 자세한 내용은 [읽어야 함](#must-read) 섹션을 참조하십시오.

1. 데이터 세트에서 가져올 특정 필드를 선택합니다.

   * 리프 노드(스키마의 최하위 레벨에 있는 필드)만 선택할 수 있습니다. 필드는 기본 값(문자열, 숫자, 부울, 날짜 등)이어야 합니다.

   * 목록(배열) 및 맵(키-값 개체)을 선택할 수 없습니다.

   +++예

   ![](assets/aep-data-leaf-primitive.png)

   +++

1. **[!UICONTROL 조회 키]** 필드에서 결정 항목 특성과 데이터 세트 모두에 있는 조인 키를 선택합니다. 이 키는 시스템에서 선택한 데이터 세트에서 검색하는 데 사용됩니다.

   * 키는 SKU, 이메일 ID 또는 기타 식별자와 같은 여정 컨텍스트에서 파생된 표현식일 수 있습니다. 예: `@profile.email` 또는 `list(@event{purchase_event.products.sku})`

   * **문자열** 또는 **문자열 목록**&#x200B;만 지원됩니다.

   +++예

   ![](assets/aep-data-strings.png)

   +++

## 여정에서 보강된 데이터 사용

**[!UICONTROL 데이터 집합 조회]** 활동으로 검색된 데이터는 개체 배열로 여정 컨텍스트에 저장됩니다. 여정 표현식 편집기 및 개인화 편집기에서 사용할 수 있으며, 보강된 데이터를 기반으로 조건부 논리 및 개인화된 메시징을 가능하게 합니다.

* **여정 식 편집기**:

  **[!UICONTROL 고급 모드]** 편집기에 액세스하여 `@datasetLookup{MyDatasetLookUpActivity1.entities}` 구문을 사용합니다. [고급 표현식 편집기로 작업하는 방법을 알아봅니다](../building-journeys/expression/expressionadvanced.md)

* **Personalization 편집기**:

  `{{context.journey.datasetLookup.1482319411.entities}}` 구문을 사용합니다.

>[!NOTE]
>
>보강된 데이터는 일시적이며 여정 런타임 시 및 아웃바운드 활동(이메일, 푸시, SMS 등)의 개인화 동안에만 사용할 수 있습니다.

## 사용 사례의 예

+++제품 범주 기반 필터링

**시나리오**:Send 가정용품에 40달러 이상을 사용하는 사용자에게 쿠폰을 제공합니다.

**여정 흐름**:

1. **구매 이벤트**: 사용자의 장바구니에서 SKU를 캡처합니다.

1. **데이터 집합 조회 활동**:

   * 데이터 집합: `products-dataset`(기본 키로 SKU).
   * 조회 키: `list(@event{purchase_event.products.sku})`.
   * 반환할 필드: `["SKU", "category", "price"]`.

1. **조건 활동**:

   * 범주가 &quot;세대&quot;인 SKU를 필터링합니다.

     ```
     @event{purchase_event.products.all( in(currentEventField.sku, @datasetlookup{MyDatasetLookupActivity1.entities.all(currentDatasetLookupField.category == 'household').sku} ) )} 
     ```

   또는

   * 가정용품에 대한 총 지출을 집계하여 $40 임계값과 비교합니다.

     ```
     sum(@event{purchase_event.products.all( in(currentEventField.sku, @datasetlookup{MyDatasetLookUpActivity1.entities.all(currentDatasetLookupField.category == 'household').sku} ) )}.price}, ',', true ) > 40
     ```

1. **Personalization 편집기**:

   보강된 데이터를 사용하여 이메일 콘텐츠를 개인화합니다.

   ```
   {% let householdTotal = 0 %}
   {{#each journey.datasetlookup.3709000.entities as |product|}}
   {%#if get(product, "category") = "household"%}
   {% let householdTotal = householdTotal + product.price %}{%/if%}
   {{/each}}
   "Hi, thanks for spending " + {%= householdTotal %} + " on household products. Here is your reward!"
   ```

+++

+++외부 충성도 데이터를 사용하는 Personalization

**시나리오**: 프로필의 충성도 상태가 플래티넘인 전자 메일 계정을 식별합니다. 이 시나리오에서는 충성도 계정이 이메일 ID와 연결되고, 충성도 데이터를 표준 프로필 조회 스토어에서 사용할 수 없습니다.

**여정 흐름**:

1. **프로필 이벤트 트리거**: 프로필 또는 이벤트 컨텍스트에서 전자 메일 ID를 캡처합니다.

1. **데이터 집합 조회 활동**:
   * 데이터 집합: `loyalty-member-dataset`(기본 키로 전자 메일).
   * 조회 키: `@profile.email`.
   * 반환할 필드: `["email", "loyaltyTier"]`.

1. **조건 활동**:

   충성도 계층을 기반으로 여정을 분기합니다.

   ```
   @datasetLookup{MyDatasetLookUpActivity1.entity.loyaltyMember.loyaltyTier} == 'Platinum'
   ```

1. **Personalization 편집기**:

   보강된 충성도 계층 데이터를 사용하여 아웃바운드 통신을 개인화합니다.

   ```
   {{context.journey.datasetLookup.1482319411.entity.loyaltyMember.loyaltyTier}}
   ```
