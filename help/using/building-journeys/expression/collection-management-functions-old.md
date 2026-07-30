---
solution: Journey Optimizer
product: journey optimizer
title: 컬렉션 관리 기능
description: 컬렉션 관리 기능의 데이터 유형에 대해 알아봅니다
feature: Journeys
hide: true
role: Developer
level: Experienced
keywords: 쿼리, 컬렉션, 함수, 페이로드, 여정
version: Journey Orchestration
feature_v2: []
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1222
ht-degree: 1%

---

# 컬렉션 관리 기능

표현식 언어에서는 컬렉션을 쿼리하기 위한 함수 집합도 소개합니다.

이러한 기능은 아래에 설명되어 있습니다. 다음 예제에서는 컬렉션을 포함하는 이벤트 페이로드를 사용하겠습니다.

```json
                { 
   "_experience":{ 
      "campaign":{ 
         "message":{ 
            "profile":{ 
               "pushNotificationTokens":[ 
                  { 
                     "token":"token_1",
                     "application":{ 
                        "_id":"APP1",
                        "name":"MarltonMobileApp",
                        "version":"1.0"
                     }
                  },
                  { 
                     "token":"token_2",
                     "application":{ 
                        "_id":"APP2",
                        "name":"MarketplaceApp",
                        "version":"1.0"
                     }
                  },
                  { 
                     "token":"token_3",
                     "application":{ 
                        "_id":"APP3",
                        "name":"VendorApp",
                        "version":"2.0"
                     }
                  }
               ]
            }
         }
      }
   },
   "timestamp":"1536160728"
}
```

**함수 &quot;all(`<condition>`)&quot;**

**[!UICONTROL all]** 함수를 사용하면 부울 식을 사용하여 주어진 컬렉션에서 필터를 정의할 수 있습니다.

```json
<listExpression>.all(<condition>)
```

예를 들어 모든 앱 사용자 중에서 IOS 13(부울 표현식 &quot;IOS 13== 사용된 앱&quot;)을 사용하여 앱 사용자를 가져올 수 있습니다. 이 함수의 결과는 부울 표현식(예: 앱 사용자 1, 앱 사용자 34, 앱 사용자 432)과 일치하는 항목을 포함하는 필터링된 목록입니다.

Data Source 조건 활동에서 **[!UICONTROL all]** 함수의 결과가 null인지 여부를 확인할 수 있습니다. 이 **[!UICONTROL all]** 함수를 **[!UICONTROL count]**&#x200B;와 같은 다른 함수와 결합할 수도 있습니다. 자세한 내용은 [데이터 Source 조건 활동](../conditions.md#data_source_condition)을 참조하세요.


## 예시

>[!CAUTION]
>
>여정 표현식/조건에서 경험 이벤트를 사용할 수 있지만 권장되지는 않습니다. 사용 사례에서 경험 이벤트를 사용해야 하는 경우 [계산된 특성](../../audience/computed-attributes.md)과 같은 대체 메서드를 사용하거나 이벤트를 사용하여 세그먼트를 만들고 해당 세그먼트를 [`inAudience` 식에 통합](../../building-journeys/functions/functioninaudience.md)해 보십시오.

**예제 1:**

사용자가 특정 버전의 애플리케이션을 설치했는지 확인하려고 합니다. 이를 위해 버전이 1.0인 모바일 애플리케이션과 연결된 모든 푸시 알림 토큰을 가져옵니다. 그런 다음 **[!UICONTROL count]** 함수로 조건을 수행하여 반환된 토큰 목록에 하나 이상의 요소가 포함되어 있는지 확인합니다.

```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all(currentEventField.application.version == "1.0").token}) > 0
```

결과는 true입니다.

**예제 2:**

여기에서는 **[!UICONTROL count]** 함수를 사용하여 컬렉션에 푸시 알림 토큰이 있는지 확인합니다.

```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().token}) > 0
```

그 결과는 참이 될 것이다.

<!--
Alternatively, you can check if there is no token in the collection:

   ```json
   count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().token}) == 0
   ```

The result will be false.

Here we use the count function in a condition to count the number of push notification tokens in the event.

`count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().token})`

The result is true.

Note that when the condition in the **all()** function is empty, the filter will return all the elements in the list. Hence, the expression above is equivalent to:

`count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.application.name})`

In both cases, the result of the expression is **3**.

A query of experience events recorded on the Adobe Experience Platform may or may not include the current event that triggered the current Journey. This will depend on the relative processing time with which [!DNL Journey Orchestration] sees an event and started evaluating conditions, versus the time it takes for that event to be ingested into the Adobe Experience Platform. For example, when using the .all() syntax to query experience events from the Adobe Experience Platform, we recommend enforcing the exclusion of the current event (by requiring an
earlier timestamp) in order to only consider prior events.
-->

>[!NOTE]
>
>**all()** 함수의 필터링 조건이 비어 있으면 필터가 목록에 있는 모든 요소를 반환합니다. **그러나 컬렉션의 요소 수를 계산하려면 all 함수가 필요하지 않습니다.**


```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.token})
```

식의 결과는 **3**&#x200B;입니다.

**예제 3:**

여기에서는 개인이 지난 24시간 내에 어떤 연락도 받지 않았는지 확인합니다. 컬렉션의 두 요소를 기반으로 하는 두 개의 표현식을 사용하여 ExperiencePlatform 데이터 소스에서 검색된 경험 이벤트 컬렉션을 필터링합니다. 특히 이벤트의 타임스탬프는 **[!UICONTROL nowWithDelta]** 함수에서 반환된 dateTime과 비교됩니다.

```json
count(#{ExperiencePlatform.MarltonExperience.experienceevent.all(
   currentDataPackField.directMarketing.sends.value > 0 and
   currentDataPackField.timestamp > nowWithDelta(-1, "days")).timestamp}) == 0
```

두 조건과 일치하는 경험 이벤트가 없으면 결과는 true가 됩니다.

**예제 4:**

여기에서는 개인이 자습서를 시작할 수 있도록 푸시 알림을 트리거하기 위해 지난 7일 동안 애플리케이션을 최소 한 번 시작했는지 확인하려고 합니다.

```json
count(
 #{ExperiencePlatform.AnalyticsData.experienceevent.all(
 nowWithDelta(-7,"days") <= currentDataPackField.timestamp
 and currentDataPackField.application.firstLaunches.value > 0
)._id}) > 0
```

<!--
**"All + Count" example 4:** here we use the count function in a boolean expression to see if there is push notification tokens in the collection.

`count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().application.name}) > 0`

The result will be:

`true`

Alternatively, you can check if there is NO token in the collection:

`count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().application.name}) =0`

The result will be:

`false`
-->

>[!NOTE]
>
>**[!UICONTROL currentEventField]**&#x200B;은 이벤트 컬렉션을 조작할 때만 사용할 수 있고, 데이터 소스 컬렉션을 조작할 때는 **[!UICONTROL currentDataPackField]**, 사용자 지정 작업 응답 컬렉션을 조작할 때는 **[!UICONTROL currentActionField]**&#x200B;할 수 있습니다.
>
>**[!UICONTROL all]**, **[!UICONTROL first]** 및 **[!UICONTROL last]**&#x200B;의 컬렉션을 처리할 때 컬렉션의 각 요소를 하나씩 반복합니다. **[!UICONTROL currentEventField]**, **currentDataPackField** 및 **[!UICONTROL currentActionField]**&#x200B;은(는) 루핑되는 요소에 해당합니다.

**함수 &quot;first(`<condition>`)&quot; 및 &quot;last(`<condition>`)&quot;**

**[!UICONTROL first]** 및 **[!UICONTROL last]** 함수는 필터를 충족하는 목록의 첫 번째/마지막 요소를 반환하면서 컬렉션에서 필터를 정의할 수도 있습니다.

_`<listExpression>.first(<condition>)`_

_`<listExpression>.last(<condition>)`_

**예제 1:**

이 표현식은 버전이 1.0인 모바일 애플리케이션과 연결된 첫 번째 푸시 알림 토큰을 반환합니다.

```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.first(currentEventField.application.version == "1.0").token
```

결과는 &quot;token_1&quot;입니다.

**예제 2:**

이 표현식은 버전이 1.0인 모바일 애플리케이션과 연결된 마지막 푸시 알림 토큰을 반환합니다.

```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.last(currentEventField.application.version == "1.0").token}
```

결과는 &quot;token_2&quot;입니다.

>[!NOTE]
>
>경험 이벤트는 Adobe Experience Platform에서 역시간 순서로 컬렉션으로 검색되므로
>
>* **[!UICONTROL first]** 함수는 가장 최근 이벤트를 반환합니다.
>* **[!UICONTROL last]** 함수는 가장 오래된 함수를 반환합니다.

**예제 3:**

DMA ID에 대해 0이 아닌 값이 있는 첫 번째(가장 최근) Adobe Analytics 이벤트의 값이 602와 같은지 확인합니다.

```json
#{ExperiencePlatform.AnalyticsProd_EvarsProps.experienceevent.first(
currentDataPackField.placeContext.geo.dmaID > 0).placeContext.geo.dmaID} == 602
```

**함수 &quot;at(`<index>`)&quot;**

**[!UICONTROL at]** 함수를 사용하면 색인에 따라 컬렉션의 특정 요소를 참조할 수 있습니다.
색인 0은 컬렉션의 첫 번째 색인입니다.

_`<listExpression>`.at(`<index>`)_

**예:**

이 표현식은 목록의 두 번째 푸시 알림 토큰을 반환합니다.

```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.at(1).token}
```

결과는 &quot;token_2&quot;입니다.

**다른 예**

이 표현식은 SKU 값을 기반으로 제품 이름을 반환합니다. 이러한 제품 목록은 이벤트 목록에 포함되며 조건은 이벤트 ID입니다.

```json
#{ExperiencePlatform.ExperienceEventFieldGroup.experienceevent.all(currentDataPackField._aepgdcdevenablement2.purchase_event.receipt_nbr == "10-337-4016"). 
_aepgdcdevenablement2.purchase_event.productListItems.all(currentDataPackField.SKU == "AB17 1234 1775 19DT B4DR 8HDK 762").name}
```

이 식은 이벤트 유형이 &#39;productListAdds&#39;이고 총 가격이 150보다 크거나 같은 상거래 이벤트의 제품 목록에서 마지막 제품의 이름을 검색합니다.

```json
 #{ExperiencePlatform.ExperienceEventFieldGroup.experienceevent.last(
currentDataPackField.eventType == "commerce.productListAdds").productListItems.last(currentDataPackField.priceTotal >= 150).name}
```

+++ AI 기술 자료 참조

이 단원에는 이 주제와 관련된 해석, 검색 및 질문 답변을 지원하기 위한 구조화된 지식이 포함되어 있습니다.

이해를 돕기 위해 이 정보를 이 페이지의 설명서와 통합해야 합니다. 두 소스 모두 독립적으로 사용하기 위한 것은 아닙니다. 이 페이지에서는 기능에 대해 설명하지만, 용어, 의도, 적용 가능성 및 제약 조건을 명확히 하는 데 도움이 되는 추가 컨텍스트를 제공합니다.

* **TL;DR:** 이 페이지에서는 푸시 알림 토큰 페이로드 및 경험 이벤트 데이터를 사용하는 예제와 함께 여정 표현식 언어로 사용할 수 있는 컬렉션 관리 함수 `all()`, `first()`, `last()` 및 `at()`에 대해 설명합니다.

**의도:**

* `all(<condition>)`과(와) 함께 부울 조건을 사용하여 컬렉션을 필터링하여 일치하는 요소를 검색합니다.
* `all()`과(와) 결합된 `count()` 함수를 사용하여 컬렉션의 요소 계산
* `first()` 또는 `last()`을(를) 사용하여 필터링된 컬렉션의 첫 번째 또는 마지막 요소를 검색합니다.
* `at(<index>)`을(를) 사용하여 인덱스로 컬렉션의 특정 요소에 액세스
* 중첩된 컬렉션 쿼리를 결합하여 SKU 또는 이벤트 유형 및 가격 임계값별로 제품 이름을 조회합니다.

**용어집:**

* **all(condition)**: 목록을 필터링하고 지정된 부울 식 *(제품별)과(와) 일치하는 항목을 반환하는 컬렉션 함수*
* **first(condition)**: 조건 *(제품별)과(와) 일치하는 첫 번째(경험 이벤트의 경우 가장 최근) 요소를 반환하는 컬렉션 함수*
* **last(condition)**: 조건 *(제품별)과(와) 일치하는 마지막(경험 이벤트의 경우 가장 오래된) 요소를 반환하는 컬렉션 함수*
* **at(index)**: 특정 0부터 시작하는 인덱스 *(제품별)*&#x200B;에서 요소를 반환하는 컬렉션 함수
* **currentEventField**: `all()`, `first()` 또는 `last()` *(제품별)* 내의 이벤트 컬렉션을 반복할 때 루프 변수를 사용할 수 있습니다.
* **currentDataPackField**: 데이터 원본 컬렉션 *(제품별)*&#x200B;에서 반복할 때 루프 변수를 사용할 수 있습니다.
* **currentActionField**: 사용자 지정 작업 응답 컬렉션 *(제품별)*&#x200B;을(를) 반복할 때 루프 변수를 사용할 수 있습니다.

**보호 기능:**

* 여정 표현식/조건에서 경험 이벤트를 사용할 수 있지만 권장되지는 않습니다. 대신 계산된 속성 또는 대상 세그먼트를 고려하십시오
* `currentEventField`은(는) 이벤트 컬렉션에만 사용할 수 있고, `currentDataPackField`은(는) 데이터 소스 컬렉션에만 사용할 수 있고, `currentActionField`은(는) 사용자 지정 작업 응답 컬렉션에만 사용할 수 있습니다.
* `all` 함수는 컬렉션의 요소를 계산하는 데 필요하지 않습니다. `count()`은(는) 컬렉션 필드에 직접 적용할 수 있습니다.
* 경험 이벤트는 역시간 순서로 검색됩니다. `first()`은(는) 가장 최근 이벤트를 반환하고 `last()`은(는) 가장 오래된 이벤트를 반환합니다.

**용어:**

* 정식 이름: 컬렉션 관리 함수 — 약어: 없음 — 변형: 컬렉션 함수, 쿼리 컬렉션 함수
* 동의어: &quot;all()&quot; = &quot;filter function&quot;; &quot;first()&quot; = &quot;most recent element function&quot; (경험 이벤트의 경우)
* 다음 항목을 혼동하지 마십시오. `first()`(가장 최근 경험 이벤트)≠ 삽입 순서에 따라 첫 번째 요소를 사용합니다.

**FAQ:**

* **Q: 조건이 비어 있을 때 `all()`은(는) 무엇을 반환합니까?** — 필터링하지 않는 것과 같은 목록의 모든 요소를 반환합니다.
* **Q: 컬렉션에 있는 푸시 알림 토큰 수를 계산하려면 어떻게 해야 합니까?** — `all()`(예: `count(@event{...pushNotificationTokens.token})`) 없이 토큰 필드 경로에서 직접 `count()`을(를) 사용합니다.
* **Q: 컬렉션의 두 번째 요소를 가져오려면 어떻게 해야 합니까?** — 인덱스 0이 첫 번째 요소이므로 `at(1)`을(를) 사용합니다.
* **Q: `first()`에서 가장 최근의 경험 이벤트를 반환하는 이유는 무엇입니까?** — 경험 이벤트가 Adobe Experience Platform에서 시간 역순으로 검색되므로 `first()`에서 최상위(최신) 항목을 선택합니다.
* **Q: 사용자가 지난 24시간 동안 어떠한 연락도 받지 않았는지 어떻게 확인합니까?** — `nowWithDelta(-1, "days")`을(를) 타임스탬프 하한으로 사용하여 경험 이벤트 컬렉션을 필터링하고 `count(...) == 0`을(를) 사용합니다.

+++
