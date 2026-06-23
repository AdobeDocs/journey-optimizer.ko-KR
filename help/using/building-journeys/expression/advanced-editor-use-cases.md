---
solution: Journey Optimizer
product: journey optimizer
title: 고급 표현식 편집기 사용
description: 고급 표현식을 작성하는 방법에 대해 알아보기
feature: Journeys
role: Developer
level: Experienced
hide: true
keywords: 표현식, 조건, 사용 사례, 이벤트
exl-id: 753ef9f4-b39d-4de3-98ca-e69a1766a78b
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/UUeCcATC7MFHsLuI8TPoVHqwVe9GOXUq3U3RoAG-a1o
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
subfeature_v2:
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1103
ht-degree: 2%

---

# 고급 표현식 예{#advanced-expression-examples}

고급 표현식 편집기를 사용하여 여정에서 사용자를 필터링할 수 있는 조건을 만들 수 있습니다. 이러한 조건을 사용하면 시간, 날짜, 위치, 기간에 사용자를 타깃팅할 수 있으므로 여정에서 해당 사용자를 다시 타깃팅할 수 있습니다.

>[!CAUTION]
>
>여정 표현식/조건에서는 경험 이벤트를 사용할 수 없습니다. 사용 사례에서 경험 이벤트를 사용해야 하는 경우 대체 방법을 고려하십시오. [자세히 알아보기](../exp-event-lookup.md)


## 경험 이벤트에 대한 조건 구축


>[!CAUTION]
>
>여정 표현식/조건에서는 경험 이벤트를 사용할 수 없습니다. 사용 사례에서 경험 이벤트를 사용해야 하는 경우 대체 방법을 고려하십시오. [자세히 알아보기](../exp-event-lookup.md)
>



고급 표현식 편집기는 구매 목록 또는 과거 메시지 클릭과 같은 시계열에 대한 쿼리를 수행해야 합니다. 이러한 쿼리는 단순 편집기를 사용하여 수행할 수 없습니다.

>[!NOTE]
>
>이벤트는 @으로 시작하며 데이터 소스는 #으로 시작합니다.

경험 이벤트는 Adobe Experience Platform에서 역시간 순서로 컬렉션으로 검색됩니다. 따라서 다음과 같습니다.

* 첫 번째 함수는 가장 최근 이벤트를 반환합니다.
* last 함수는 가장 오래된 함수를 반환합니다.

예를 들어 지난 7일 동안 장바구니 포기를 통해 고객이 스토어에 가까워지면 스토어에 있는 원하는 항목에 대한 오퍼와 함께 메시지를 보내기 위해 고객을 타겟팅한다고 가정해 보겠습니다.

**다음 조건을 만들어야 합니다.**

우선 온라인 매장을 찾아보았지만 지난 7일 동안 주문이 확정되지 않은 고객을 대상으로 했다.

**이 식은 문자열 값에서 지정된 값을 찾습니다.**

`In ("addToCart", #{field reference from experience event})`

**이 식은 지난 7일 동안 지정한 이 사용자의 모든 이벤트를 찾습니다.**

그런 다음 completePurchase로 변환되지 않은 장바구니에 추가 이벤트를 모두 선택합니다.

>[!NOTE]
>
>표현식에 필드를 빠르게 삽입하려면 편집기의 왼쪽 패널에서 필드를 두 번 클릭합니다.

지정된 타임스탬프가 날짜 시간 값으로 작동하고 있으며 두 번째는 일 수입니다.

```json
        in( "addToCart", #{ExperiencePlatformDataSource
                        .ExperienceEventFieldGroup
                        .experienceevent
                        .all(
                        inLastDays(currentDataPackField.timestamp, 7 ))
                        .productData
                        .productInteraction})
        and
        not(in( "completePurchase", #{ExperiencePlatformDataSource
                        .ExperienceEventFieldGroup
                        .experienceevent
                        .all(
                        inLastDays(currentDataPackField.timestamp, 7 ))
                        .productData
                        .productInteraction}))
```

이 표현식은 부울을 반환합니다.

**이제 제품의 재고 여부를 확인하는 식을 만들어 보겠습니다**

* Inventory에서 이 표현식은 제품의 수량 필드를 찾고 0보다 커야 한다고 지정합니다.

`#{Inventory.fieldgroup3.quantity} > 0`

* 오른쪽에서 필요한 값이 지정됩니다. 여기에서는 이벤트 &quot;ArriveLumaStudio&quot;의 위치에서 매핑된 스토어의 위치를 검색해야 합니다.

`#{ArriveLumaStudio._acpevangelists1.location.location}`

* `first` 함수를 사용하여 가장 최근의 &quot;addToCart&quot; 상호 작용을 검색하는 SKU를 지정하십시오.

  ```json
      #{ExperiencePlatformDataSource
                      .ExperienceEventFieldGroup
                      .experienceevent
                      .first(
                      currentDataPackField
                      .productData
                      .productInteraction == "addToCart"
                      )
                      .SKU}
  ```

여기에서 제품이 스토어에 없는 경우 여정에 다른 경로를 추가하고 참여 오퍼와 함께 알림을 전송할 수 있습니다. 이에 따라 메시지를 구성하고 개인화 데이터를 사용하여 메시지 타겟을 향상시킵니다.

## 표현식의 타임스탬프 필터링

여러 장바구니 활동 이벤트를 참조할 때 내역 데이터를 선택하지 않도록 시작 및 종료 타임스탬프 창을 모두 지정합니다. 예:

```json
toDateTimeOnly(currentDataPackField.timestamp) >= toDateTimeOnly(@event{poc_UDXCartAddSavedCheckOutEv.timestamp})
AND
toDateTimeOnly(currentDataPackField.timestamp) < toDateTimeOnly(nowWithDelta(4, "hours"))
```

## 고급 표현식 편집기를 사용한 문자열 조작의 예

**조건**

이 조건은 &quot;Arlington&quot;에서 트리거된 geofence 이벤트만 검색합니다.

```json
        @event{GeofenceEntry
                    .placeContext
                    .POIinteraction
                    .POIDetail
                    .name} == "Arlington"
```

설명: 이는 엄격한 문자열 비교(대/소문자 구분)입니다. `Is sensitive`이(가) 선택된 상태에서 `equal to`을(를) 사용하는 단순 모드의 쿼리와 같습니다.

`Is sensitive`을(를) 선택 취소한 동일한 쿼리는 고급 모드에서 다음 식을 생성합니다.

```json
        equalIgnoreCase(@event{GeofenceEntry
                        .placeContext
                        .POIinteraction
                        .POIDetail
                        .name}, "Arlington")
```

**작업에서**

다음 표현식을 사용하면 작업 개인화 필드에서 CRM ID를 정의할 수 있습니다.

```json
substr(
   @event{MobileAppLaunch
   ._myorganization
   .identification
   .crmid},
   1, 
   lastIndexOf(
     @event{MobileAppLaunch
     ._myorganization
     .identification
     .crmid},
     '}'
   )
)
```

설명: 이 예제에서는 `substr` 및 `lastIndexOf` 함수를 사용하여 모바일 앱 실행 이벤트와 함께 전달된 CRM ID를 둘러싸는 중괄호를 제거합니다.


고급 표현식 편집기를 사용하는 방법에 대한 자세한 내용은 [이 비디오](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/introduction-to-building-a-journey.html?lang=ko-KR)를 시청하십시오.

+++ AI 기술 자료 참조

이 단원에는 이 주제와 관련된 해석, 검색 및 질문 답변을 지원하기 위한 구조화된 지식이 포함되어 있습니다.

이해를 돕기 위해 이 정보를 이 페이지의 설명서와 통합해야 합니다. 두 소스 모두 독립적으로 사용하기 위한 것은 아닙니다. 이 페이지에서는 기능에 대해 설명하지만, 용어, 의도, 적용 가능성 및 제약 조건을 명확히 하는 데 도움이 되는 추가 컨텍스트를 제공합니다.

* **TL;DR:** 이 페이지에서는 고급 표현식 편집기를 사용하여 장바구니 활동, 인벤토리 상태, geofence 이벤트, 문자열 조작 및 타임스탬프 창별로 사용자를 필터링하는 여정 조건을 만드는 실제 사례를 제공합니다.

**의도:**

* 항목을 추가했지만 7일 이내에 구매를 완료하지 않은 사용자를 대상으로 `in()` 및 `inLastDays()`을(를) 사용하여 장바구니 포기 조건을 작성하십시오.
* 내역 데이터를 캡처하지 않도록 타임스탬프 창으로 경험 이벤트 컬렉션 필터링
* geofence 이벤트 필드에 대한 대/소문자 구분 및 대/소문자를 구분하지 않는 문자열 비교 적용
* `substr` 및 `lastIndexOf`을(를) 사용하여 모바일 앱 실행 이벤트에서 CRM ID 추출 및 조작
* 수량 필드를 임계값과 비교하여 제품 재고 가용성을 확인합니다.
* 여정 조건에서 `and` / `not` 논리를 사용하여 여러 부울 표현식을 결합합니다.

**용어집:**

* **고급 표현식 편집기**: 함수, 연산자 및 필드 참조를 사용하여 복잡한 코드 수준 표현식을 작성하기 위한 Journey Optimizer 인터페이스 *(제품별)*
* **currentDataPackField**: `all()`, `first()` 또는 `last()` 함수 *(제품별)* 내에서 데이터 원본 컬렉션을 반복할 때 사용되는 루프 변수
* **inLastDays(timestamp, N)**: 지정된 타임스탬프가 마지막 N일 *(제품별)* 내에 있으면 true를 반환하는 날짜 함수입니다.
* **경험 이벤트**: Adobe Experience Platform에 저장된 시계열 동작 데이터 레코드가 역시간 순서로 검색됨 *(제품별)*

**보호 기능:**

* 여정 표현식/조건에서는 경험 이벤트를 직접 사용할 수 없습니다. 대신 계산된 속성이나 대상 세그먼트와 같은 대체 메서드를 사용해야 합니다
* 구매 컬렉션이나 클릭 수와 같은 시계열 데이터에 대한 쿼리에는 고급 표현식 편집기를 사용해야 합니다(단순 편집기가 아님)
* 왼쪽 패널에서 필드를 두 번 클릭하면 표현식에 빠르게 삽입됩니다. 오류를 줄이려면 필드 경로를 수동으로 입력하지 마십시오
* 경험 이벤트를 쿼리하는 표현식은 부울을 반환합니다. 다운스트림 논리에 부울 유형이 필요한지 확인합니다.

**용어:**

* 정식 이름: 고급 표현식 편집기 — 약어: 없음 — 변형: 표현식 편집기, 고급 편집기
* 동의어: &quot;addToCart&quot; = &quot;장바구니에 추가 상호 작용&quot;; &quot;completePurchase&quot; = &quot;구매 완료 이벤트&quot;
* 혼동하지 않음: 이벤트(접두사가 `@`인 경우) ≠ 데이터 소스(접두사가 `#`인 경우)

**FAQ:**

* **Q: 장바구니 포기 쿼리에 단순 편집기 대신 고급 편집기를 사용해야 하는 이유는 무엇입니까?** — 단순 편집기에서 시계열 컬렉션에 대한 쿼리를 수행할 수 없습니다. `all()`, `first()` 및 `last()` 컬렉션 함수에는 고급 편집기가 필요합니다.
* **Q: 식에서 가장 최근 &quot;addToCart&quot; 이벤트를 어떻게 참조합니까?** — 이벤트가 역연대순으로 반환되므로 `productInteraction == "addToCart"`(으)로 필터링된 경험 이벤트 컬렉션에 `first()` 함수를 사용합니다.
* **Q: 고급 편집기에서 문자열 비교 대/소문자를 구분하지 않게 하려면 어떻게 해야 합니까?** — `==` 연산자 대신 `equalIgnoreCase()` 함수를 사용합니다.
* **Q: 장바구니 이벤트를 쿼리할 때 타임스탬프 창을 추가하는 목적은 무엇입니까?** — 시작 타임스탬프와 종료 타임스탬프를 모두 지정하면 의도한 활동 기간을 벗어난 내역 데이터를 선택할 수 없습니다.
* **Q: 이벤트에 전달된 CRM ID 문자열에서 중괄호를 제거하려면 어떻게 합니까?** — `substr()`을(를) `lastIndexOf()`과(와) 함께 사용하여 중괄호 사이의 내용을 추출합니다.

+++
