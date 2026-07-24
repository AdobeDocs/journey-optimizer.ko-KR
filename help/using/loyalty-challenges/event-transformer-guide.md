---
solution: Journey Optimizer
product: journey optimizer
title: 이벤트 변환기 안내서
description: Adobe Journey Optimizer에서 로열티 챌린지 이벤트 정의에 대한 스키마 및 변환기 설정을 구성하는 방법을 알아봅니다.
feature: Journeys
topic: Content Management
role: Admin
level: Intermediate
hide: true
badge: label="비공개 베타" type="Informative"
mini-toc-levels: 1
exl-id: d3ad85f0-7f7e-40ab-b8c4-fc0c1234be87
feature_v2: []
subfeature_v2: []
source-git-commit: c440ff464b2ea58519e6f1ba900728adfa718232
workflow-type: tm+mt
source-wordcount: 1731
ht-degree: 3%

---

# 이벤트 변환기 안내서 {#event-transformer-guide}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_event_transformer"
>title="이벤트 변환기 안내서"
>abstract="이 안내서를 사용하여 충성도 챌린지 이벤트 정의를 위한 스키마 유효성 검사 및 변환기 표현식을 구성할 수 있습니다."

>[!BEGINSHADEBOX]

**목차**

[충성도 문제 시작](get-started.md)

<table style="table-layout:fixed">
<tr style="border: 0;">
<td style="vertical-align:top;">

**문제 만들기 및 관리**

* [과제 및 작업 액세스 및 관리](access-loyalty-challenges.md)
* [과제 만들기](create-challenges.md)
* [작업 만들기](create-tasks.md)
* [충성도 과제 성능 모니터링](loyalty-reporting.md)

</td>
<td style="vertical-align:top;">

**구성 및 통합**

* [충성도 문제 구성](loyalty-admin.md)
* [보상 정의 안내서](reward-definition-guide.md)
* **이벤트 변환기 안내서** ◀︎ **여기 있습니다**
* [충성도 데이터 및 데이터 세트](loyalty-data-and-datasets.md)
* [충성도 과제 API 참조](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

</td>
</tr>
</table>

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>이 기능은 현재 **개인 베타**&#x200B;에 있습니다. [!DNL Journey Optimizer]의 릴리스 주기 및 가용성 단계에 대한 자세한 내용은 [릴리스 주기](../rn/releases.md)를 참조하십시오.

고객 거래를 충성도 챌린지에 적용하려면 먼저 챌린지 서비스가 인식하는 **Adobe 충성도 이벤트** 형식이어야 합니다. POS 시스템, 모바일 앱, 전자 상거래 플랫폼 또는 기타 소스의 고객 이벤트는 일반적으로 고객의 데이터 스키마를 사용합니다. **이벤트 변환기** 업스트림 시스템을 변경하지 않고 이 간격을 메웁니다.

## 개요

**이벤트 정의**&#x200B;은(는) 플랫폼에 다음 두 가지를 알려줍니다.

* **청구할 이벤트** - 들어오는 이벤트가 이 정의에 속함을 인식하는 방법(일치)
* **모양을 변경하는 방법** — 고객의 필드를 고객 충성도 이벤트 형식(변환)에 매핑하는 [JSONata](https://docs.jsonata.org/overview) 식

조직당 여러 이벤트 정의를 구성할 수 있습니다. 플랫폼은 이를 순서대로 평가하고 일치하는 첫 번째 항목을 적용합니다. 정의와 일치하지 않는 이벤트는 기본 수집으로 전달됩니다([대체 — 기본 충성도 이벤트](#fallback--native-loyalty-events) 참조).

## Adobe 충성도 이벤트 형식

모든 이벤트 정의는 다음 형식의 JSON 개체를 생성해야 합니다. Challenge Service 프로세스에 대한 입력입니다.

```json
{
  "_id":              "string — optional; used for duplicate detection if enabled",
  "event_name":       "string — used for internal metrics and reporting only (e.g. 'purchase', 'visit')",
  "timestamp":        "ISO 8601 date-time string — when the event occurred",
  "utc_offset":       "string — UTC offset of the store or device (e.g. '-07:00'); required for daypart matching",
  "location_id":      "string — optional; store or location identifier",
  "transaction_id":   "string — optional; dedup key for the transaction",
  "loyalty_identity": {
    "id": "string — the member's loyalty ID"
  },
  "item_list": [
    {
      "item_set":   ["string", "..."],  // one or more identifiers — SKU, category, event code, etc.
      "item_name":  "string — optional human-readable label",
      "quantity":   1,                  // integer; how many units
      "unit_price": 4.99,               // float; price per unit
      "sub_total":  4.99                // float; line total (quantity × unit_price)
    }
  ]
}
```

### 필드 노트

| 필드 | 필수 여부 | 참고 |
|--------------------------------|--------------------|-------|
| `loyalty_identity` | **예** | `id`을(를) 포함해야 합니다. 멤버의 충성도 ID입니다. |
| `item_list` | **예** | ≥1 항목이 있어야 합니다. 빈 item_list가 거부되었습니다. |
| `item_set` | **예**(항목당) | 식별자 작업 포함/제외 목록은 와 일치합니다. |
| `timestamp` | **예** | 날짜 창 평가에 사용됩니다. ISO 8601이어야 합니다. |
| `utc_offset` | 권장 | 날짜 일치 및 연속 날짜 계산에 필요합니다. |
| `_id` | 아니오 | 조직에서 중복 검색을 사용하도록 설정한 경우 중복 제거에 사용됩니다. |
| `sub_total` | 아니오 | 지출-임계값 태스크는 이를 사용합니다. 생략은 0의 지출을 의미합니다. |

## 이벤트 정의 필드

| 필드 | 유형 | 필수 여부 | 설명 |
|--------------------------------|------------------|----------------------|-------------|
| `guid` | 문자열 | 아니요(시스템 지정) | 시스템에서 할당한 고유 ID, 읽기 전용. |
| `name` | 문자열 | **예** | 사람이 읽을 수 있는 레이블(예: `"Starbucks POS Purchase"`). |
| `xdmSchemaId` | 문자열 | **예** | XDM 스키마 ID별로 이벤트를 일치시킵니다(일치 작동 방식 참조). |
| `schema` | 문자열 | 아니오 | 들어오는 이벤트를 확인하기 위한 [JSON 스키마](https://json-schema.org/)&#x200B;(문자열). |
| `transformer` | 문자열 | **예** | 이벤트를 충성도 형식에 매핑하는 JSONata 표현식. |

## 일치 작동 방식

데이터 수집 핵심 서비스(DCCS)를 통해 도착하는 이벤트는 XDM 스키마 참조를 봉투에 포함합니다. 플랫폼은 `/body/xdmMeta/schemaRef/id`에서 스키마 ID를 읽고 각 정의의 `xdmSchemaId`과(와) 비교합니다.

플랫폼은 조직의 이벤트 정의를 **순서대로**&#x200B;하고 첫 번째 일치를 적용합니다. 일치 항목이 발견되면 `xdmEntity` 본문이 변환기에 전달됩니다.

## 변환기에 쓰기

`transformer` 필드는 [JSONata](https://docs.jsonata.org/overview) 식입니다. 수신 이벤트 JSON을 입력으로 받으며 유효한 Adobe 충성도 이벤트 개체를 반환해야 합니다.

+++기본 매핑 패턴

대상 형식의 각 최상위 필드를 소스 이벤트의 해당 경로에 매핑합니다.

```jsonata
{
  "_id":            sourceEvent._id,
  "event_name":     sourceEvent.eventType,
  "timestamp":      sourceEvent.timestamp,
  "utc_offset":     sourceEvent.storeInfo.utcOffset,
  "location_id":    sourceEvent.storeInfo.storeId,
  "transaction_id": sourceEvent.transaction.id,
  "loyalty_identity": {
    "id": sourceEvent.member.loyaltyId
  },
  "item_list": sourceEvent.transaction.items.{
    "item_set":   [itemSku, itemCategory],
    "item_name":  itemDescription,
    "quantity":   quantity,
    "unit_price": unitPrice,
    "sub_total":  lineTotal
  }
}
```

+++

+++이벤트 이름 하드코딩

이 정의와 일치하는 모든 이벤트가 동일한 논리 활동을 나타내는 경우 `event_name`을(를) 하드코딩하십시오.

```jsonata
{
  "event_name": "in-store-purchase",
  ...
}
```

`event_name`은(는) 내부 지표 및 보고에 사용됩니다. 작업 필터로 사용되지 않습니다. 작업 자격은 이벤트 이름이 아닌 `item_set` 내용으로 결정됩니다.

+++

+++DCCS/XDM 이벤트에 대한 ID 매핑

DCCS 경로를 통해 도착하는 이벤트의 경우 멤버의 ID는 일반적으로 사용자 지정 테넌트 속성이 아닌 표준 XDM `identityMap` 필드에 전달됩니다. `identityMap`은(는) 네임스페이스로 처리된 맵입니다. 키 자체는 네임스페이스 이름이고 값은 id 개체 배열입니다.

```jsonata
"loyalty_identity": {
  "id": identityMap.Email[0].id
}
```

* **네임스페이스 대체:** `Email`을(를) 조직이 충성도 멤버에 사용하는 네임스페이스(`Loyalty`, `ECID`, `CRMID` 등)로 바꿉니다. 기본 충성도 프로필 ID가 있는 네임스페이스에서 항상 읽습니다.

* **항상 `[0]` 사용:** `identityMap.Email`은(는) 배열입니다. 인덱스가 없으면 JSONata는 둘 이상의 ID가 있는 경우 단일 값이 아닌 시퀀스를 반환하며 `loyalty_identity.id`은(는) 목록이 됩니다. `[0]`을(를) 사용하여 첫 번째 요소에 고정합니다.

* **ID에 대한 사용자 지정 테넌트 필드를 사용하지 않음:** 사용자 지정 필드 그룹은 전자 메일 형식 필드(예: `_yourtenant.identification.core.email`)를 표시하는 경우가 있습니다. 샘플 데이터에서 값을 반환하고 올바른 것처럼 보이지만 프로덕션 이벤트에서는 비어 있는 경우가 많습니다. 신뢰할 수 있는 ID 원본은 항상 `identityMap`입니다.

+++

+++`item_set` 빌드 중

`item_set`은(는) 문자열 식별자의 배열입니다. 과제 작업이 필터링할 수 있는 모든 필드 포함:

```jsonata
"item_set": [itemSku, productCategory, departmentCode]
```

트랜잭션이 아닌 이벤트(체크 인, 설문 조사 완료, 사용자 지정 트리거)의 경우, 하나의 식별자로 충분합니다.

```jsonata
"item_set": [eventName]
```

+++

+++`unit_price` 매핑

`unit_price`은(는) 단위당 가격이어야 합니다. 일부 소스 스키마에는 라인 합계(가격 × 수량)가 대신 저장됩니다. 출처 필드가 라인 합계인 경우 수량을 기준으로 나누어 단가를 구합니다.

```jsonata
"unit_price": priceTotal / quantity
```

> 소스 필드가 라인 합계인 경우에만 나눕니다. 이미 단가를 저장하고 있다면 직접 매핑해서 단가를 수량으로 나누면 묵묵히 잘못된 값이 나온다.

+++

+++`transaction_id` 가져오기

소스 이벤트에 거래 식별자가 포함되지 않은 경우 타임스탬프에서 안정적인 식별자를 파생할 수 있습니다.

```jsonata
"transaction_id": "txn_" & $string($toMillis(timestamp))
```

이렇게 하면 ISO 타임스탬프가 에포크 밀리초로 변환되고 주어진 이벤트에 대한 결정적 값을 생성합니다. 사용 가능한 경우 플랫폼의 자체 ID 생성 기능을 사용하십시오.

+++

+++JSONata 함수 사용

전체 JSONata 함수 라이브러리를 사용할 수 있습니다. 유용한 예:

```jsonata
/* String concatenation */
"item_set": [skuId & ':' & categoryId]

/* Number formatting */
"item_set": ["spend:" & $formatNumber(totalAmount, '0.00')]

/* Conditional field */
"event_name": eventType ? eventType : "unknown"

/* Array transformation */
"item_list": items.{ "item_set": [sku], "quantity": qty, "sub_total": price * qty }
```

+++

## 예

+++예제 1 — 간단한 사용자 지정 이벤트(비트랜잭션)

**시나리오:** 모바일 앱에서 체크 인 이벤트를 보냅니다. 라인 항목이 없습니다. 이벤트 자체가 자격을 갖춘 활동입니다.

**들어오는 이벤트:**

```json
{
  "_id":       "evt-001",
  "eventName": "store-checkin",
  "timestamp": "2025-10-15T14:22:00Z",
  "storeId":   "STORE-042",
  "member": {
    "loyaltyId": "LM-8827361"
  }
}
```

**이벤트 정의:**

```json
{
  "name":        "Mobile Store Check-In",
  "xdmSchemaId": "https://ns.adobe.com/yourtenant/schemas/store-checkin-v1",
  "transformer": "{\"_id\": _id, \"event_name\": eventName, \"timestamp\": timestamp, \"location_id\": storeId, \"loyalty_identity\": {\"id\": member.loyaltyId}, \"item_list\": [{\"item_set\": [eventName], \"quantity\": 1}]}"
}
```

**서식 있는 변환기(가독성):**

```jsonata
{
  "_id":        _id,
  "event_name": eventName,
  "timestamp":  timestamp,
  "location_id": storeId,
  "loyalty_identity": {
    "id": member.loyaltyId
  },
  "item_list": [
    {
      "item_set": [eventName],
      "quantity": 1
    }
  ]
}
```

**출력 Adobe 충성도 이벤트:**

```json
{
  "_id":        "evt-001",
  "event_name": "store-checkin",
  "timestamp":  "2025-10-15T14:22:00Z",
  "location_id": "STORE-042",
  "loyalty_identity": { "id": "LM-8827361" },
  "item_list": [{ "item_set": ["store-checkin"], "quantity": 1 }]
}
```

포함/제외 제한이 없는 과제 작업은 이 이벤트를 자격 있는 방문으로 계산합니다. 단일 `item_set` 항목 `["store-checkin"]`이(가) 모든 항목을 허용하는 모든 작업과 일치합니다.

+++

+++예 2 - 라인 품목이 있는 POS 구매

**시나리오:** 판매 지점 시스템에서 트랜잭션 페이로드를 보냅니다. 각 라인 항목은 SKU를 포함하며 범주에 속합니다. 과제 작업은 SKU 및 범주를 사용하여 적합한 항목을 결정합니다.

**들어오는 이벤트:**

```json
{
  "_id":       "txn-20251015-4492",
  "timestamp": "2025-10-15T14:35:00Z",
  "storeInfo": {
    "storeId":   "STORE-042",
    "utcOffset": "-07:00"
  },
  "transaction": {
    "transactionId": "4492",
    "items": [
      { "sku": "COFFEE-001", "category": "BEVERAGE", "qty": 2, "unitPrice": 4.50, "lineTotal": 9.00 },
      { "sku": "MUFFIN-007", "category": "FOOD",     "qty": 1, "unitPrice": 3.25, "lineTotal": 3.25 }
    ]
  },
  "member": {
    "loyaltyId": "LM-8827361"
  }
}
```

**이벤트 정의:**

```json
{
  "name":        "Retail POS Purchase",
  "xdmSchemaId": "https://ns.adobe.com/yourtenant/schemas/retail-pos-purchase-v1",
  "transformer": "{\"_id\": _id, \"event_name\": \"purchase\", \"timestamp\": timestamp, \"utc_offset\": storeInfo.utcOffset, \"location_id\": storeInfo.storeId, \"transaction_id\": transaction.transactionId, \"loyalty_identity\": {\"id\": member.loyaltyId}, \"item_list\": transaction.items.{\"item_set\": [sku, category], \"quantity\": qty, \"unit_price\": unitPrice, \"sub_total\": lineTotal}}"
}
```

**서식 있는 변환기:**

```jsonata
{
  "_id":            _id,
  "event_name":     "purchase",
  "timestamp":      timestamp,
  "utc_offset":     storeInfo.utcOffset,
  "location_id":    storeInfo.storeId,
  "transaction_id": transaction.transactionId,
  "loyalty_identity": {
    "id": member.loyaltyId
  },
  "item_list": transaction.items.{
    "item_set":   [sku, category],
    "quantity":   qty,
    "unit_price": unitPrice,
    "sub_total":  lineTotal
  }
}
```

**출력 Adobe 충성도 이벤트:**

```json
{
  "_id":            "txn-20251015-4492",
  "event_name":     "purchase",
  "timestamp":      "2025-10-15T14:35:00Z",
  "utc_offset":     "-07:00",
  "location_id":    "STORE-042",
  "transaction_id": "4492",
  "loyalty_identity": { "id": "LM-8827361" },
  "item_list": [
    { "item_set": ["COFFEE-001", "BEVERAGE"], "quantity": 2, "unit_price": 4.50, "sub_total": 9.00 },
    { "item_set": ["MUFFIN-007", "FOOD"],     "quantity": 1, "unit_price": 3.25, "sub_total": 3.25 }
  ]
}
```

`include: ["BEVERAGE"]`이(가) 있는 과제 작업에서는 커피 라인 항목의 자격을 확인하고(`item_set`에 `"BEVERAGE"`이(가) 포함되어 있음) 해당 작업에 대한 9.00달러의 지출을 누적합니다. 머핀 라인 항목은 제외됩니다.

+++

+++예제 3 — AEP 경험 이벤트(XDM 스키마 일치)

**시나리오:** 이벤트가 Adobe Journey Optimizer을 통해 흐릅니다. 들어오는 이벤트는 알려진 스키마 ID가 있는 XDM 경험 이벤트입니다. 플랫폼은 경로/값 검사가 아닌 일치에 스키마 ID를 사용합니다.

**들어오는 XDM 엔터티 본문**(AJO 이벤트에서 추출된 `xdmEntity`):

```json
{
  "_brandname": {
    "identities": {
      "loyaltyId": "LM-8827361"
    },
    "transactions": {
      "transactionId": "TXN-9901",
      "storeNumber":   "042",
      "utcOffset":     "-07:00",
      "lineItems": [
        { "skuNumber": "11143053", "priceAmount": 345, "qty": 1, "category": "BEVERAGE" },
        { "skuNumber": "11161387", "priceAmount": 495, "qty": 1, "category": "FOOD" }
      ],
      "totalAmount": 840
    }
  },
  "_id":       "87c0cccf-5809-38e0-a703-3994e80173ab",
  "timestamp": "2025-07-04T16:03:32.000Z"
}
```

**이벤트 정의:**

```json
{
  "name":        "AJO Brand Purchase",
  "xdmSchemaId": "https://ns.adobe.com/brandname/schemas/purchase-event-v1",
  "transformer":  "{\"_id\": _id, \"event_name\": \"purchase\", \"timestamp\": timestamp, \"utc_offset\": _brandname.transactions.utcOffset, \"location_id\": _brandname.transactions.storeNumber, \"transaction_id\": _brandname.transactions.transactionId, \"loyalty_identity\": {\"id\": _brandname.identities.loyaltyId}, \"item_list\": _brandname.transactions.lineItems.{\"item_set\": [skuNumber, category], \"quantity\": qty, \"unit_price\": priceAmount, \"sub_total\": priceAmount * qty}}"
}
```

**서식 있는 변환기:**

```jsonata
{
  "_id":            _id,
  "event_name":     "purchase",
  "timestamp":      timestamp,
  "utc_offset":     _brandname.transactions.utcOffset,
  "location_id":    _brandname.transactions.storeNumber,
  "transaction_id": _brandname.transactions.transactionId,
  "loyalty_identity": {
    "id": _brandname.identities.loyaltyId
  },
  "item_list": _brandname.transactions.lineItems.{
    "item_set":   [skuNumber, category],
    "quantity":   qty,
    "unit_price": priceAmount,
    "sub_total":  priceAmount * qty
  }
}
```

> **참고:** 이벤트가 XDM 스키마 ID로 일치하는 경우 변환기는 이벤트의 `xdmEntity` 부분만 수신합니다(외부 AJO 봉투 아님). 변환기 표현식의 모든 경로는 XDM 엔티티 본문을 기준으로 합니다.

+++

## JSON 스키마 유효성 검사 추가(선택 사항)

플랫폼에서 변환을 시도하기 전에 들어오는 이벤트의 구조를 확인하도록 하려면 `schema` 필드를 JSON 문자열로 인코딩된 [JSON 스키마](https://json-schema.org/draft-04) 문서로 설정하십시오.

스키마 유효성 검사에 실패한 이벤트는 변환이 실행되기 전에 거부됩니다. 오류 응답에는 특정 유효성 검사 실패가 포함되므로 잘못된 업스트림 이벤트를 쉽게 진단할 수 있습니다.

+++예제 스키마(예: 위의 예 2)

```json
{
  "$schema": "http://json-schema.org/draft-04/schema#",
  "type": "object",
  "required": ["_id", "timestamp", "transaction", "member"],
  "properties": {
    "_id":       { "type": "string" },
    "timestamp": { "type": "string", "format": "date-time" },
    "member": {
      "type": "object",
      "required": ["loyaltyId"],
      "properties": {
        "loyaltyId": { "type": "string" }
      }
    },
    "transaction": {
      "type": "object",
      "required": ["items"],
      "properties": {
        "transactionId": { "type": "string" },
        "items": {
          "type": "array",
          "items": {
            "type": "object",
            "required": ["sku", "qty", "lineTotal"],
            "properties": {
              "sku":       { "type": "string" },
              "category":  { "type": "string" },
              "qty":       { "type": "number" },
              "unitPrice": { "type": "number" },
              "lineTotal": { "type": "number" }
            }
          }
        }
      }
    }
  }
}
```

+++

이벤트 정의의 `schema` 필드에 축소된 JSON 문자열로 이 스키마를 전달합니다.

## 대체 — 기본 충성도 이벤트

수신되는 이벤트와 일치하는 이벤트 정의가 없는 경우 플랫폼은 이를 기본 Adobe 충성도 이벤트로 직접 수집하려고 합니다. 페이로드가 이미 위에서 설명한 충성도 이벤트 형식을 준수하는 경우 변환기가 필요하지 않으며 이벤트가 그대로 적용됩니다. 이렇게 하면 이벤트의 형식을 미리 지정한 고객이 변형을 완전히 우회할 수 있습니다.

## API 참조

모든 이벤트 정의 작업에서 기본 경로 `/loyalty/metadata/config/events`을(를) 사용합니다.

+++이벤트 정의 만들기

```http
POST /loyalty/metadata/config/events
x-gw-ims-org-id: {ORG_ID}
x-sandbox-name: {SANDBOX}
Content-Type: application/json

{
  "name":        "Retail POS Purchase",
  "xdmSchemaId": "https://ns.adobe.com/yourtenant/schemas/retail-pos-purchase-v1",
  "transformer": "{ ... }"
}
```

+++

+++목록 이벤트 정의

```http
GET /loyalty/metadata/config/events
x-gw-ims-org-id: {ORG_ID}
x-sandbox-name: {SANDBOX}
```

+++

+++이벤트 정의 업데이트

```http
PUT /loyalty/metadata/config/events/{eventId}
x-gw-ims-org-id: {ORG_ID}
x-sandbox-name: {SANDBOX}
Content-Type: application/json

{
  "name":        "Retail POS Purchase (v2)",
  "transformer": "{ ... updated expression ... }"
}
```

+++

+++이벤트 정의 삭제

```http
DELETE /loyalty/metadata/config/events/{eventId}
x-gw-ims-org-id: {ORG_ID}
x-sandbox-name: {SANDBOX}
```

+++

## 변환기 유효성 검사

이벤트 정의가 저장될 때 JSONata 표현식의 구문 유효성이 검사됩니다. 표현식이 잘못된 경우 API가 구문 분석 실패에 대한 설명과 함께 `422` 오류를 반환합니다.

배포하기 전에 변환기를 테스트하려면 [JSONata Exerciser](https://try.jsonata.org/) — 소스 이벤트를 입력으로 붙여넣고 변환기 표현식을 적용하여 출력이 예상 충성도 이벤트 형식과 일치하는지 확인합니다.

## 일반적인 함정

이러한 실수는 모두 간단한 단일 항목 테스트 페이로드에서 오류 없이 실행되므로 감지되지 않은 상태로 슬쩍 넘어갑니다. 배포하기 전에 항상 두 개 이상의 제품을 사용하여 페이로드에 대해 변환기를 테스트하십시오.

+++스토리지에 매핑하는 대신 하나의 객체 구축

가장 빈번한 실수. `productListItems.SKU`에서 단일 개체 리터럴을 사용하면 제품당 하나의 라인 항목을 생성하는 대신 모든 SKU와 모든 수량을 묶은 시퀀스로 가져옵니다.

**✗이(가) 모든 항목을 하나로 축소:**

```jsonata
"item_list": [
  {
    "item_set": [ productListItems.SKU ],
    "quantity": productListItems.quantity
  }
]
```

두 제품을 사용하면 `item_set`은(는) SKU를 모두 보유하며 `quantity`은(는) `[1, 4]`과(와) 같은 배열이 됩니다.

**✓제품당 하나의 라인 항목:**

```jsonata
"item_list": [
  productListItems.{
    "item_set": [SKU],
    "quantity": quantity
  }
]
```

`.{ }` 맵은 제품당 한 번 실행되므로 각각 고유한 항목이 됩니다.

+++

+++ID에서 배열 인덱스를 삭제하는 중

`identityMap.Email`은(는) 배열입니다. `[0]`이(가) 없으면 프로필에 해당 네임스페이스에 둘 이상의 ID가 있는 경우 `id`은(는) 단일 문자열 대신 값 목록이 됩니다.

**✗** `identityMap.Email.id`

**✓** `identityMap.Email[0].id`

+++

+++사용자 지정 테넌트 필드의 소싱 ID

사용자 지정 필드 그룹은 경우에 따라 `_yourtenant.identification.core.email`과(와) 같은 전자 메일 모양 필드를 노출합니다. 샘플 데이터에서 값을 반환하고 올바른 것처럼 보이지만 프로덕션 이벤트에서는 빈 경우가 많기 때문에 `loyalty_identity.id`이(가) null로 표시됩니다. 항상 `identityMap`을(를) ID의 소스로 사용합니다.

+++

+++`item_set`(으)로 누출되는 중첩 배열

`item_set`에 범주 필드를 추가하는 것은 간단해 보이지만 `productCategories`이(가) 배열 자체일 경우 결과는 예상할 수 없이 확장됩니다.

**✗이(가) 예상보다 많은 항목을 생성할 수 있음:**

```jsonata
"item_set": [SKU, productCategories.categoryID]
```

범주가 세 개인 제품에서 네 개의 값이 있는 `item_set`을(를) 생성합니다.

**✓중첩된 배열을 인덱싱하여 정확히 하나의 값을 가져옵니다.**

```jsonata
"item_set": [SKU, productCategories[0].categoryID]
```

+++

+++`item_list`이(가) 비어 있거나 없습니다.

비어 있거나 없는 `item_list`이(가) 있는 이벤트가 잘못된 이벤트로 거부되었습니다. 트랜잭션이 아닌 이벤트(체크인, 사용자 지정 트리거)의 경우 자연어 라인 항목이 없으므로 합성 라인 항목을 생성합니다.

```jsonata
"item_list": [{ "item_set": [eventName], "quantity": 1 }]
```

+++

+++`timestamp`을(를) ISO 8601 대신 Unix Epoch 정수로 사용

플랫폼에는 ISO 8601 문자열이 필요합니다. epoch 이후 소스 이벤트가 밀리초로 전달되면 변환하십시오.

```jsonata
"timestamp": $fromMillis(timestamp)
```

+++

+++`utc_offset` 생략됨

`utc_offset`이(가) 없으면 날짜 범위 창 일치 및 연속 일 연속 계산을 모두 건너뜁니다. 소스 이벤트의 저장소 또는 장치 UTC 오프셋을 사용할 수 있는 위치에 매핑합니다.

+++

+++DCCS 이벤트에서 AJO 봉투 관련 변환기 경로

DCCS 이벤트의 경우 변환기는 외부 AJO 봉투가 아닌 `xdmEntity` 본문만 받습니다. 모든 경로는 XDM 엔티티 루트에 상대적이어야 합니다. 식이 외부 봉투(예: `/body/xdmMeta/...`)에 있는 필드를 참조하는 경우 해당 필드를 찾을 수 없으며 자동으로 null이 생성됩니다.

+++

