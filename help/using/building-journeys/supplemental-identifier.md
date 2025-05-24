---
title: 이벤트가 트리거된 여정의 보조 식별자
description: 이벤트가 트리거된 여정에서 보조 식별자를 사용하는 방법을 알아봅니다.
badge: label="제한된 가용성" type="Informative"
source-git-commit: bfff5bfe0a87d65c453018c4f1af01e9b1456052
workflow-type: tm+mt
source-wordcount: '806'
ht-degree: 3%

---


# 이벤트가 트리거된 여정의 보조 식별자

>[!AVAILABILITY]
>
>이 기능은 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.

기본적으로 이벤트가 트리거된 여정은 **프로필 ID**&#x200B;의 컨텍스트에서 실행됩니다. 즉, 프로필이 주어진 여정에서 활성 상태인 한 다른 여정으로 다시 들어갈 수 없습니다. 이를 방지하기 위해 Journey Optimizer에서는 프로필 ID 외에 주문 ID, 구독 ID, 처방 ID와 같은 이벤트에서 **보조 식별자**&#x200B;를 캡처할 수 있습니다.
이 예에서는 예약 ID를 보조 식별자로 추가했습니다.

![](assets/event-supplemental-id.png){width=40% zoomable}

이렇게 하면 이벤트에 의해 트리거된 여정이 보조 식별자(여기서는 예약 ID)와 연결된 프로필 ID의 컨텍스트에서 실행됩니다. 여정의 하나의 인스턴스는 보조 식별자의 각 반복에 대해 실행된다. 이렇게 하면 서로 다른 예약을 한 경우 여정에 동일한 프로필 ID를 여러 번 넣을 수 있습니다.

또한 Journey Optimizer을 사용하면 메시지 맞춤화를 위해 보조 식별자의 속성(예: 예약 번호, 처방 갱신 날짜, 제품 유형)을 활용하여 관련성이 높은 커뮤니케이션을 보장할 수 있습니다. <!--Example: A healthcare provider can send renewal reminders for each prescription in a patient's profile.-->

## 가드레일 및 제한 사항

* **동시 인스턴스 제한**: 프로필에는 동시 여정 인스턴스가 10개를 초과할 수 없습니다.

<!--* **Array depth**: Supplemental identifier objects can have a maximum depth of 3 levels (2 levels of nesting).

    +++Example

    ```
    [
    (level 1) "Atorvastatin" : {
    "description" : "used to lower cholesterol",
    "renewal_date" : "11/20/25",
    "dosage" : "10mg"
    (level 2) "ingredients" : [
    (level 3) "Atorvastatin calcium",
    "lactose monohydrate",
    "microcrystalline cellulose",
    "other" ]
    }
    ]
    ```

    +++
-->
* **종료 기준**: 종료 기준이 트리거되면 해당 시점에 여정에 있는 프로필의 모든 인스턴스가 종료됩니다. 프로필 ID + 보조 식별자 조합과 컨텍스트가 맞지 않습니다.

* **빈도 규칙**: 보조 식별자 사용에서 만들어진 각 여정 인스턴스는 단일 이벤트로 인해 여러 여정 인스턴스가 발생하는 경우에도 빈도 상한에 포함됩니다.

* **데이터 형식 및 스키마 구조**: 보조 식별자는 `string` 형식이어야 합니다. 독립 문자열 속성이거나 객체 배열 내의 문자열 속성일 수 있습니다. 독립 문자열 속성은 단일 여정 인스턴스를 발생시키지만, 객체 배열 내의 문자열 속성은 객체 배열의 반복마다 고유한 여정 인스턴스를 발생시킵니다. 문자열 배열 및 맵은 지원되지 않습니다.

## 보조 식별자를 추가하고 여정에서 활용합니다

여정에서 보조 식별자를 사용하려면 다음 단계를 수행하십시오.

1. **특성을 이벤트 스키마의 식별자로 표시**

   1. 이벤트 스키마에 액세스하여 보조 식별자로 사용할 속성(예: 예약 ID, 구독 ID)을 찾아 ID로 표시합니다. [스키마 작업 방법 알아보기](../data/get-started-schemas.md)

   1. 식별자를 **[!UICONTROL ID]**(으)로 표시합니다.

      ![](assets/supplemental-ID-schema.png)

      >[!IMPORTANT]
      >
      >특성을 **기본 ID**(으)로 표시하지 않도록 하십시오.

   1. 보조 ID와 연결할 네임스페이스를 선택하십시오. 이는 비개인 식별자 네임스페이스여야 합니다.

1. **보조 ID를 이벤트에 추가**

   1. 원하는 이벤트를 만들거나 편집합니다. [단일 이벤트를 구성하는 방법을 알아봅니다](../event/about-creating.md)

   1. 이벤트 구성 화면에서 **[!UICONTROL 보조 식별자 사용]** 옵션을 선택합니다.

      ![](assets/supplemental-ID-event.png)

   1. 표현식 편집기를 사용하여 보조 ID로 표시한 속성을 선택합니다.

   1. 보조 ID를 선택하면 연관된 네임스페이스가 이벤트 구성 화면에 읽기 전용으로 표시됩니다.

1. **여정에 이벤트 추가**

   구성된 이벤트를 여정 캔버스로 드래그합니다. 프로필 ID와 보조 ID 모두를 기반으로 여정 항목을 트리거합니다.

   ![](assets/supplemental-ID-journey.png)

1. **보조 ID 특성 활용**

   표현식 편집기 및 개인화 편집기를 사용하여 개인화 또는 조건부 논리에 대한 보조 식별자의 속성을 참조합니다. 특성은 **[!UICONTROL 상황별 특성]** 메뉴에서 액세스할 수 있습니다.

   ![](assets/supplemental-ID-perso.png)

   >[!NOTE]
   >
   >배열(예: 여러 가지 처방 또는 정책)로 작업하는 경우 수식을 사용하여 특정 요소를 추출합니다.

+++ 예제 참조

   보조 ID가 &quot;bookingNum&quot;이고 &quot;bookingCountry&quot;라는 동일한 수준의 특성이 있는 개체 배열에서 여정은 bookingNum을 기반으로 배열 개체를 반복하고 각 개체에 대한 여정 인스턴스를 만듭니다.

   * 조건 활동의 다음 식은 개체 배열을 반복하고 `bookingCountry`의 값이 &quot;FR&quot;과 같은지 확인합니다.

     ```
     @event{<event_name>.<object_path>.<object_array_name>.all(currentEventField.<attribute_path>.bookingNum==${supplementalId}).at(0).<attribute_path>.bookingCountry}=="FR"
     ```

   * 이메일 개인화 편집기의 다음 표현식은 오브젝트 배열을 반복하고 현재 여정 인스턴스에 적용할 수 있는 &#39;bookingCountry&#39;를 가져와서 콘텐츠에 표시합니다.

     ```
     {{#each context.journey.events.<event_ID>.<object_path>.<object_array_name> as |l|}} 
     
     {%#if l.<attribute_path>.bookingNum = context.journey.technicalProperties.supplementalId%} {{l.<attribute_path>.bookingCountry}}  {%/if%}
     
     {{/each}}
     ```

   * 여정을 트리거하는 데 사용되는 이벤트의 예:

     ```
     "bookingList": [
           {
               "bookingInfo": {
                   "bookingNum": "x1",
                         "bookingCountry": "US"
               }
           },
           {
               "bookingInfo": {
                   "bookingNum": "x2",
                   "bookingCountry": "FR"
               }
           }
       ]
     ```

+++

1. **여정 게시**

   구성이 완료되면 보충 식별자를 기반으로 여러 동시 항목 사용을 시작하기 위해 여정을 게시합니다.

## 예시 사용 사례

### **정책 갱신 알림**

* **시나리오**: 보험 공급자가 고객이 보유한 각 활성 정책에 대한 갱신 알림 메시지를 보냅니다.
* **실행**:
   * 프로필: &quot;John&quot;.
   * 보조 ID: `"AutoPolicy123", "HomePolicy456"`.
   * 여정은 개인화된 갱신 일자, 적용 범위 세부 정보 및 프리미엄 정보와 함께 각 정책에 대해 개별적으로 실행됩니다.

### **구독 관리**

* **시나리오**: 구독 서비스가 고객 프로필에 연결된 각 구독에 대해 맞춤 메시지를 보냅니다.
* **실행**:
   * 프로필: &quot;Jane&quot;.
   * 보조 ID: `"Luma Yoga Program ", "Luma Fitness PlPrograman"`.
   * 여정은 개인화된 갱신 오퍼와 함께 각 구독에 대해 개별적으로 실행됩니다.

### **제품 추천**

* **시나리오**: 전자 상거래 플랫폼은 고객이 구매한 특정 제품을 기반으로 권장 사항을 보냅니다.
* **실행**:
   * 프로필: &quot;Alex&quot;
   * 보조 ID: `"productID1234", "productID5678"`.
   * 여정은 개인화된 상향 판매 기회를 통해 각 제품에 대해 개별적으로 실행됩니다.
