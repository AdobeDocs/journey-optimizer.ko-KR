---
solution: Journey Optimizer
product: journey optimizer
title: 컬렉션 관리 기능
description: 컬렉션 관리 기능의 데이터 유형에 대해 알아봅니다
feature: Journeys
role: Developer
level: Experienced
keywords: 쿼리, 컬렉션, 함수, 페이로드, 여정
exl-id: 09b38179-9ace-4921-985b-ddd17eb64681
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/sNFI7l-UMGmRV2wRcvYa56tILLoWFxXeG3N5txgrUiw
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1000
ht-degree: 1%

---

# 컬렉션 관리 기능 {#collection-management-functions}


## 쿼리 컬렉션 함수 기본 정보

표현식 언어에서는 컬렉션을 쿼리하기 위한 함수 집합도 소개합니다. 이러한 기능은 아래에 설명되어 있습니다.

다음 예제에서는 푸시 알림 토큰 컬렉션을 포함하는 &quot;LobbyBeacon&quot;이라는 이벤트를 사용합니다. 이 페이지의 예제에서는 아래에 표시된 이벤트 페이로드 구조를 사용합니다.

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

>[!NOTE]
>
>아래 예에서 이 페이로드는 `@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens}`을(를) 사용하여 참조됩니다. 여기서 &quot;LobbyBeacon&quot;은 이벤트 이름이고 경로의 나머지 부분은 위에 표시된 구조에 해당합니다.

## all(`<condition>`) 함수

**[!UICONTROL all]** 함수를 사용하면 부울 식을 사용하여 주어진 컬렉션에서 필터를 정의할 수 있습니다.

```json
<listExpression>.all(<condition>)
```

**개념적 예:** 모든 앱 사용자 중에서 IOS 13(부울 표현식 &quot;app used == IOS 13&quot;)을 사용하여 앱 사용자를 가져올 수 있습니다. 이 함수의 결과는 부울 표현식(예: 앱 사용자 1, 앱 사용자 34, 앱 사용자 432)과 일치하는 항목을 포함하는 필터링된 목록입니다.

Data Source 조건 활동에서 **[!UICONTROL all]** 함수의 결과가 null인지 여부를 확인할 수 있습니다. 이 **[!UICONTROL all]** 함수를 **[!UICONTROL count]**&#x200B;와 같은 다른 함수와 결합할 수도 있습니다. 자세한 내용은 [데이터 Source 조건 활동](../conditions.md#data_source_condition)을 참조하세요.

**LobbyBeacon 페이로드를 사용하는 코드 예:**

아래 예제에서는 이 페이지 상단에 표시된 이벤트 페이로드를 사용합니다.


>[!CAUTION]
>
>여정 표현식/조건에서는 경험 이벤트를 사용할 수 없습니다. 사용 사례에서 경험 이벤트를 사용해야 하는 경우 대체 방법을 고려하십시오. [자세히 알아보기](../exp-event-lookup.md)

### 예제 1

사용자가 특정 버전의 애플리케이션을 설치했는지 확인하려고 합니다. 이를 위해 버전이 1.0인 모바일 애플리케이션과 연결된 모든 푸시 알림 토큰을 가져옵니다. 그런 다음 **[!UICONTROL count]** 함수로 조건을 수행하여 반환된 토큰 목록에 하나 이상의 요소가 포함되어 있는지 확인합니다.

```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all(currentEventField.application.version == "1.0").token}) > 0
```

결과는 true입니다.

### 예제 2

여기에서는 **[!UICONTROL count]** 함수를 사용하여 컬렉션에 푸시 알림 토큰이 있는지 확인합니다.

```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().token}) > 0
```


결과는 true입니다.


```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.token})
```

식의 결과는 **3**&#x200B;입니다.


>[!NOTE]
>
>* **all()** 함수의 필터링 조건이 비어 있으면 필터가 목록에 있는 모든 요소를 반환합니다. **그러나 컬렉션의 요소 수를 계산하려면 all 함수가 필요하지 않습니다.**
>
>* `currentEventField`은(는) 이벤트 컬렉션을 조작할 때만 사용할 수 있으며, `currentDataPackField`은(는) 데이터 소스 컬렉션을 조작할 때 사용할 수 있고 `currentActionField`은(는) 사용자 지정 작업 응답 컬렉션을 조작할 때만 사용할 수 있습니다.
>
>  `all`, `first` 및 `last`(으)로 컬렉션을 처리할 때 컬렉션의 각 요소를 하나씩 반복합니다. `currentEventField`, `currentDataPackField` 및 `currentActionField`은(는) 루프가 적용되는 요소에 해당합니다.


## 첫 번째(`<condition>`) 및 마지막(`<condition>`) 함수

**[!UICONTROL first]** 및 **[!UICONTROL last]** 함수는 필터를 충족하는 목록의 첫 번째/마지막 요소를 반환하면서 컬렉션에서 필터를 정의할 수도 있습니다.

_`<listExpression>.first(<condition>)`_

_`<listExpression>.last(<condition>)`_

### 예제 1

이 표현식은 버전이 1.0인 모바일 애플리케이션과 연결된 첫 번째 푸시 알림 토큰을 반환합니다.


```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.first(currentEventField.application.version == "1.0").token}
```

결과는 `token_1`입니다.

### 예제 2

이 표현식은 버전이 1.0인 모바일 애플리케이션과 연결된 마지막 푸시 알림 토큰을 반환합니다.


```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.last(currentEventField.application.version == "1.0").token}
```

결과는 `token_2`입니다.

## at(`<index>`) 함수

**[!UICONTROL at]** 함수를 사용하면 색인에 따라 컬렉션의 특정 요소를 참조할 수 있습니다.
색인 0은 컬렉션의 첫 번째 색인입니다.

_`<listExpression>`.at(`<index>`)_

### 예

이 표현식은 목록의 두 번째 푸시 알림 토큰을 반환합니다.


```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.at(1).token}
```

결과는 `token_2`입니다.

+++ AI 기술 자료 참조

이 단원에는 이 주제와 관련된 해석, 검색 및 질문 답변을 지원하기 위한 구조화된 지식이 포함되어 있습니다.

이해를 돕기 위해 이 정보를 이 페이지의 설명서와 통합해야 합니다. 두 소스 모두 독립적으로 사용하기 위한 것은 아닙니다. 이 페이지에서는 기능에 대해 설명하지만, 용어, 의도, 적용 가능성 및 제약 조건을 명확히 하는 데 도움이 되는 추가 컨텍스트를 제공합니다.

* **TL;DR:** 이 페이지에서는 푸시 알림 토큰 페이로드 예와 함께 여정 고급 표현식 편집기에 사용된 `all()`, `first()`, `last()` 및 `at()` 컬렉션 관리 기능을 설명합니다.

**의도:**

* `all(<condition>)`과(와) 함께 부울 조건을 사용하여 이벤트 또는 데이터 원본 필드의 컬렉션을 필터링합니다.
* 컬렉션 함수와 결합된 `count()`을(를) 사용하여 필터링된 컬렉션 요소 또는 필터링되지 않은 컬렉션 요소 개수
* `first()` 또는 `last()`을(를) 사용하여 컬렉션의 첫 번째 또는 마지막 일치 요소를 검색합니다.
* `at(<index>)`을(를) 사용하여 특정 0부터 시작하는 인덱스의 컬렉션 요소에 액세스합니다.
* 각 컬렉션 컨텍스트에 적용되는 루프 변수(`currentEventField`, `currentDataPackField`, `currentActionField`)를 이해합니다.

**용어집:**

* **all(condition)**: 컬렉션을 필터링하고 지정된 부울 식 *(제품별)과(와) 일치하는 모든 항목을 반환합니다*
* **first(condition)**: 조건 *(제품별)과(와) 일치하는 컬렉션에서 첫 번째(경험 이벤트에 대해 가장 최근) 요소를 반환합니다*
* **last(condition)**: 조건 *(제품별)과(와) 일치하는 컬렉션의 마지막(경험 이벤트에 대해 가장 오래된) 요소를 반환합니다*
* **at(index)**: 컬렉션 *(제품별)*&#x200B;의 지정된 0부터 시작하는 인덱스에서 요소를 반환합니다.
* **currentEventField**: 이벤트 컬렉션 *(제품별)*&#x200B;을(를) 반복하는 경우에만 루프 변수를 사용할 수 있습니다.
* **currentDataPackField**: 데이터 원본 컬렉션 *(제품별)*&#x200B;을(를) 반복하는 경우에만 루프 변수를 사용할 수 있습니다.
* **currentActionField**: 사용자 지정 작업 응답 컬렉션 *(제품별)*&#x200B;을(를) 반복하는 경우에만 루프 변수를 사용할 수 있습니다.

**보호 기능:**

* 여정 표현식/조건에서는 경험 이벤트를 사용할 수 없습니다. 계산된 속성과 같은 대체 메서드를 고려하십시오.
* `currentEventField`, `currentDataPackField` 및 `currentActionField`은(는) 해당 컬렉션 컨텍스트 내에서만 사용할 수 있습니다.
* `all` 함수는 컬렉션 요소를 계산하는 데 필요하지 않습니다. `count()`은(는) 필드 경로에 직접 적용할 수 있습니다.
* 빈 조건으로 `all()`을(를) 호출하면 컬렉션의 모든 요소가 반환됩니다

**용어:**

* 정식 이름: 컬렉션 관리 함수 — 약어: 없음 — 변형: 컬렉션 함수, 쿼리 컬렉션 함수
* 동의어: &quot;all()&quot; = &quot;collection filter function&quot;; &quot;at()&quot; = &quot;index accessor&quot;
* 혼동하지 마십시오. `first()`(가장 최근 경험 이벤트)≠ 일반 목록에 처음 삽입된 요소입니다

**FAQ:**

* **Q: 빈 조건이 있는 `all()`과(와) 조건이 있는 `all()`의 차이점은 무엇입니까?** — 빈 `all()`은(는) 모든 요소를 반환하고 조건 기반 `all()`은(는) 해당 부울 표현식과 일치하는 요소만 반환합니다.
* **Q: `all()`을(를) 사용하지 않고 푸시 알림 토큰을 계산하려면 어떻게 해야 합니까?** — 토큰 필드 경로(예: `count(@event{LobbyBeacon...pushNotificationTokens.token})`)에서 직접 `count()`을(를) 호출합니다.
* **Q: 데이터 원본 컬렉션을 반복할 때 현재 요소를 참조하는 데 어떤 변수를 사용합니까?** — 데이터 원본 컬렉션의 `all()`, `first()` 또는 `last()` 내에서 `currentDataPackField`을(를) 사용합니다.
* **Q: 컬렉션에서 두 번째 항목을 가져오려면 어떻게 해야 합니까?** — 인덱스 0이 첫 번째 요소이므로 `at(1)`을(를) 사용합니다.
* **Q: `last()`에서 가장 오래된 경험 이벤트를 반환하는 이유는 무엇입니까?** — 경험 이벤트가 역시간 순서로 저장되므로 컬렉션의 마지막 위치가 가장 오래된 이벤트에 해당합니다.

+++
