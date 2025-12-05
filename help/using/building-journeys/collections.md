---
solution: Journey Optimizer
product: journey optimizer
title: 사용자 정의 액션 매개 변수에 컬렉션 전달
description: 사용자 지정 작업을 사용하여 Journey Optimizer에서 컬렉션을 동적으로 전달하는 방법을 알아봅니다
feature: Journeys, Use Cases, Custom Actions, Collections
topic: Content Management
role: Developer
level: Experienced
exl-id: 8832d306-5842-4be5-9fb9-509050fcbb01
version: Journey Orchestration
source-git-commit: bf5b054eaaca73abf484ccbabf160e902fad3f5b
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 3%

---


# 사용자 정의 액션 매개 변수에 컬렉션 전달 {#passing-collection}

런타임 시 동적으로 채워진 사용자 지정 작업 매개 변수에서 컬렉션을 전달할 수 있습니다.

지원되는 컬렉션은 두 가지입니다.

* **단순 컬렉션**

  문자열, 숫자 또는 부울 같은 기본 값 목록에 간단한 컬렉션을 사용합니다. 이러한 기능은 추가 속성 없이 항목 목록을 전달하기만 하면 되는 경우에 유용합니다.

  예를 들어 디바이스 유형 목록은 다음과 같습니다.

  ```json
  {
   "deviceTypes": [
       "android",
       "ios"
   ]
  }
  ```

* **개체 컬렉션**

  각 항목에 여러 필드 또는 속성이 포함된 경우 개체 컬렉션을 사용합니다. 일반적으로 제품 세부 사항, 이벤트 레코드 또는 항목 속성과 같은 구조화된 데이터를 전달하는 데 사용됩니다.

  예:

  ```json
  {
  "products":[
     {
        "id":"productA",
        "name":"A",
        "price":20.1
     },
     {
        "id":"productB",
        "name":"B",
        "price":10.0
     },
     {
        "id":"productC",
        "name":"C",
        "price":5.99
     }
   ]
  }
  ```

>[!NOTE]
>
>컬렉션 내의 중첩된 배열은 사용자 지정 작업 요청 페이로드에서 일부만 지원됩니다. 자세한 내용은 [제한 사항](#limitations)을 참조하세요.

## 일반 절차 {#general-procedure}

이 섹션에서는 다음의 JSON 페이로드 예제를 사용합니다. 단순 컬렉션인 필드가 있는 오브젝트 배열입니다.

```json
{
  "ctxt": {
    "products": [
      {
        "id": "productA",
        "name": "A",
        "price": 20.1,
        "color":"blue",
        "locations": [
          "Paris",
          "London"
        ]
      },
      {
        "id": "productB",
        "name": "B",
        "price": 10.99
      }
    ]
  }
}
```

`products`이(가) 두 개체의 배열임을 확인할 수 있습니다. 하나 이상의 개체가 있어야 합니다.

1. 사용자 지정 작업을 만듭니다. [이 페이지](../action/about-custom-action-configuration.md)에서 자세히 알아보십시오.

1. **[!UICONTROL 작업 매개 변수]** 섹션에 JSON 예제를 붙여 넣습니다. 표시된 구조는 정적입니다. 페이로드를 붙여 넣을 때 모든 필드가 상수로 정의됩니다.

   ![컬렉션 함수 및 작업을 표시하는 식 편집기](assets/uc-collection-1.png)

1. 필요한 경우 필드 유형을 조정합니다. 컬렉션에는 listString, listInteger, listDecimal, listBoolean, listDateTime, listDateTimeOnly, listDateOnly, listObject 필드 형식이 지원됩니다

   >[!NOTE]
   >
   >페이로드 예제에 따라 필드 유형이 자동으로 유추됩니다.

1. 개체를 동적으로 전달하려면 변수로 설정해야 합니다. 이 예제에서는 `products`을(를) 변수로 설정합니다. 객체에 포함된 모든 객체 필드는 자동으로 변수로 설정됩니다.

   >[!NOTE]
   >
   >페이로드 예제의 첫 번째 객체는 필드를 정의하는 데 사용됩니다.

1. 각 필드에 대해 여정 캔버스에 표시될 레이블을 정의합니다.

   ![조건 빌더 인터페이스를 사용한 컬렉션 함수 필터링](assets/uc-collection-2.png){width="70%" align="left"}

1. 여정을 만들고 만든 사용자 지정 작업을 추가합니다. [이 페이지](../building-journeys/using-custom-actions.md)에서 자세히 알아보십시오.

1. **[!UICONTROL 작업 매개 변수]** 섹션에서 고급 표현식 편집기를 사용하여 배열 매개 변수(`products`)를 정의합니다.

   필드 선택이 있는 ![컬렉션 필터링 식](assets/uc-collection-3.png)

1. 다음 각 오브젝트 필드에 대해 소스 XDM 스키마의 해당 필드 이름을 입력합니다. 이름이 동일한 경우 이 작업이 필요하지 않습니다. 이 예제에서는 `product id`과(와) &quot;color&quot;만 정의하면 됩니다.

   ![순서 지정 구성이 있는 컬렉션 정렬 함수](assets/uc-collection-4.png){width="50%" align="left"}

배열 필드의 경우 고급 표현식 편집기를 사용하여 데이터 조작을 수행할 수도 있습니다. 다음 예제에서는 [filter](functions/list-functions.md#filter) 및 [intersect](functions/list-functions.md#intersect) 함수를 사용합니다.

![필터, 정렬 및 제한 작업이 있는 컬렉션 식 완료](assets/uc-collection-5.png)

## 제한 사항 {#limitations}

사용자 지정 작업의 컬렉션은 동적 데이터를 유연하게 전달할 수 있지만 다음과 같은 특정 구조적 제약 조건이 있습니다.

* **사용자 지정 작업에서 중첩된 배열 지원**

  Adobe Journey Optimizer은 사용자 지정 작업 **응답 페이로드**&#x200B;에서 중첩된 오브젝트 배열을 지원하지만, 이 지원은 **요청 페이로드**&#x200B;에서 제한됩니다.

  요청 페이로드에서 중첩된 배열은 사용자 지정 작업 구성에 정의된 대로 고정 수의 항목이 포함된 경우에만 지원됩니다. 예를 들어 중첩된 배열에 항상 정확히 세 개의 항목이 포함되어 있으면 상수로 구성할 수 있습니다. 항목 수가 동적이어야 하는 경우, 중첩되지 않은 배열(맨 아래 수준의 배열)만 변수로 정의할 수 있습니다.

  예:

   1. 다음 예제에서는 **지원되지 않는 사용 사례**&#x200B;를 보여 줍니다.

      이 예제에서 제품 배열에는 동적 항목 수가 포함된 중첩된 배열(`locations`)이 포함되어 있습니다. 이 배열은 요청 페이로드에서 지원되지 않습니다.

      ```json
      {
      "products": [
         {
            "id": "productA",
            "name": "A",
            "price": 20,
            "locations": [
            { "name": "Paris" },
            { "name": "London" }
            ]
         }
      ]
      }
      ```

   2. 고정 항목이 상수로 정의된 지원되는 예입니다.

      이 경우 중첩된 위치가 고정 필드(`location1`, `location2`)로 대체되므로 페이로드가 지원되는 구성 내에서 유효한 상태로 유지될 수 있습니다.

      ```json
      {
      "products": [
         {
            "id": "productA",
            "name": "A",
            "price": 20,
            "location1": { "name": "Paris" },
            "location2": { "name": "London" }
         }
      ]
      }
      ```


* **컬렉션 테스트**: 테스트 모드를 사용하여 컬렉션을 테스트하려면 코드 보기 모드를 사용해야 합니다. 코드 보기 모드는 비즈니스 이벤트에 대해 지원되지 않으므로 이 경우 단일 요소가 포함된 컬렉션만 보낼 수 있습니다.


## 특별한 경우{#examples}

이기종 유형 및 배열 배열의 경우 배열은 listAny 형식으로 정의됩니다. 개별 항목만 매핑할 수 있지만 배열을 변수로 변경할 수는 없습니다.

![데이터 형식과 필드 선택이 혼합된 다른 형식 컬렉션](assets/uc-collection-heterogeneous.png){width="70%" align="left"}

형식이 다른 형식의 예:

```json
{
    "data_mixed-types": [
        "test",
        "test2",
        null,
        0
    ]
}
```

배열 배열의 예:

```json
{
    "data_multiple-arrays": [
        [
            "test",
            "test1",
            "test2"
        ]
    ]
}
```

## 추가 리소스

사용자 지정 작업의 구성, 사용 및 문제 해결에 대한 자세한 내용을 보려면 아래 섹션을 찾아보십시오.

* [사용자 지정 작업 시작](../action/action.md) - 사용자 지정 작업이 무엇이고 이러한 작업이 서드파티 시스템에 연결하는 데 어떻게 도움이 되는지 알아봅니다.
* [사용자 지정 작업 구성](../action/about-custom-action-configuration.md) - 사용자 지정 작업을 만들고 구성하는 방법에 대해 알아봅니다.
* [사용자 지정 작업 사용](../building-journeys/using-custom-actions.md) - 여정에서 사용자 지정 작업을 사용하는 방법에 대해 알아봅니다.
* [사용자 지정 작업 문제 해결](../action/troubleshoot-custom-action.md) - 사용자 지정 작업 문제를 해결하는 방법 알아보기
  <!--* [Iterate over contextual data](../personalization/personalization-contexts.md#arrays-in-journeys) - Learn how to work with arrays in Journey expressions and iterate over custom action responses, event data, and dataset lookups in message personalization-->

