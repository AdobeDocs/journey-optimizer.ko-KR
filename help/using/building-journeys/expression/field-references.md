---
solution: Journey Optimizer
product: journey optimizer
title: 필드 참조
description: 고급 표현식의 필드 참조에 대해 알아보기
feature: Journeys
role: Developer
level: Experienced
keywords: 여정, 필드, 표현식, 이벤트
exl-id: 2348646a-b205-4b50-a08f-6625e92f44d7
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/G8ooc1R2PwL06V89EBs-jH8Lf43F6q5xj3I4Wl6hDHk
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
source-wordcount: 1044
ht-degree: 1%

---

# 필드 참조 {#field-references}

필드 참조는 이벤트 또는 필드 그룹에 첨부할 수 있습니다. 유일한 의미 있는 정보는 필드의 이름과 경로입니다.

필드에 특수 문자를 사용하는 경우 큰따옴표나 간단한 따옴표를 사용해야 합니다. 견적이 필요한 경우는 다음과 같습니다.

* 필드는 숫자로 시작합니다.
* 필드는 &quot;-&quot; 문자로 시작합니다.
* 필드에 _a_-_z_, _A_-_Z_, _0_-_9_, _,_-_ 이외의 항목이 포함되어 있습니다.

예를 들어 필드가 _3h_&#x200B;인 경우: _#{OpenWeather.weatherData.rain.&#39;3h&#39;} > 0_

```json
// event field
@event{<event name>.<XDM path to the field>}
@event{LobbyBeacon.endUserIDs._experience.emailid.id}

// field group
#{<data source name>.<field group name>.<path to the field>}
#{ExperiencePlatform.ProfileFieldGroup.profile.personalEmail.address}
```

식에서 이벤트 필드는 &quot;@&quot;에서 참조되고 데이터 소스 필드는 &quot;#&quot;에서 참조됩니다.

구문 색상은 이벤트 필드(녹색)와 필드 그룹(파란색)을 시각적으로 구별하는 데 사용됩니다.

## 필드 참조의 기본값 {#default-value}

기본값은 필드 이름과 연결할 수 있습니다. 구문은 다음과 같습니다.

```json
// event field
@event{<event name>.<XDM path to the field>, defaultValue: <default value expression>}
@event{LobbyBeacon.endUserIDs._experience.emailid.id, defaultValue: "example@adobe.com"}
// field group
#{<data source name>.<field group name>.<path to the field>, defaultValue: <default value expression>}
#{ExperiencePlatform.ProfileFieldGroup.profile.personalEmail.address, defaultValue: "example@adobe.com"}
```

>[!NOTE]
>
>필드 유형과 기본값은 동일해야 합니다. 예를 들어 `@event{LobbyBeacon.endUserIDs._experience.emailid.id, defaultValue : 2}`은(는) 기본값이 정수이지만 예상 값은 문자열이어야 하므로 잘못되었습니다.

예

```json
// for an event 'OrderEvent' having the following payload:
{
    "orderId": "12345"
}
 
expression example:
- @event{OrderEvent.orderId}                                    -> "12345"
- @event{OrderEvent.productId, defaultValue : "not specified" } -> "not specified" // default value, productId is not a field present in the payload
- @event{OrderEvent.productId}                                  -> null
 
 
// for an entity 'Profile' on datasource 'ACP' having fields person/lastName, with fetched data such as:
{
    "person": {
        "lastName":"Snow"
    },
    "emails": [
        { "email":"john.snow@winterfell.westeros" },
        { "email":"snow@thewall.westeros" }
    ]
}
 
expression examples:
- #{ACP.Profile.person.lastName}                 -> "Snow"
- #{ACP.Profile.emails.at(1).email}              -> "snow@thewall.westeros"
- #{ACP.Profile.person.age, defaultValue : -1}   -> -1 // default value, age is not a field present in the payload
- #{ACP.Profile.person.age}                      -> null
```

모든 종류의 표현식을 기본값으로 추가할 수 있습니다. 유일한 제약 조건은 식이 예상 데이터 형식을 반환해야 한다는 것입니다. 함수를 사용할 때 ()로 함수를 캡슐화해야 합니다.

```
#{ExperiencePlatform.Subscriptions.profile.consents.marketing.any.time, defaultValue : (now())} 
== date("2022-02-10T00:00:00Z")
```

## 컬렉션 내의 필드 참조

컬렉션 내에 정의된 요소는 특정 함수 `all`, `first` 및 `last`을(를) 사용하여 참조됩니다. 자세한 정보는 [이 페이지](../expression/collection-management-functions.md)를 참조하십시오.

예 :

```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all()
```

## 맵에 정의된 필드 참조

### `entry` 함수

맵에서 요소를 검색하기 위해 주어진 키와 함께 entry 함수를 사용한다. 예를 들어 선택한 네임스페이스에 따라 이벤트의 키를 정의할 때 사용됩니다. 자세한 내용은 [이 페이지](../../event/about-creating.md#select-the-namespace)를 참조하세요.

```json
@event{MyEvent.identityMap.entry('Email').first().id}
```

이 식에서 이벤트의 &#39;IdentityMap&#39; 필드의 &#39;이메일&#39; 키 항목을 가져옵니다. &#39;Email&#39; 항목은 컬렉션이며, 여기에서 &#39;first()&#39;를 사용하여 첫 번째 요소의 &#39;id&#39;를 가져옵니다. 자세한 내용은 [이 페이지](../expression/collection-management-functions.md)를 참조하세요.

### `firstEntryKey` 함수

맵의 첫 번째 시작 키를 검색하려면 `firstEntryKey` 함수를 사용하십시오.

다음 예에서는 특정 목록의 구독자에 대한 첫 번째 이메일 주소를 검색하는 방법을 보여 줍니다.

```json
#{ExperiencePlatform.Subscriptions.profile.consents.marketing.email.subscriptions.entry('daily-email').subscribers.firstEntryKey()}
```

이 예제에서 구독 목록의 이름은 `daily-email`입니다. 이메일 주소는 `subscribers` 맵에서 구독 목록 맵에 연결된 키로 정의됩니다.

### `keys` 함수

맵의 모든 키로 검색하려면 `keys` 함수를 사용하십시오.

다음 예에서는 특정 프로필에 대해 특정 목록의 구독자와 연결된 모든 이메일 주소를 검색하는 방법을 보여 줍니다.

```json
#{ExperiencePlatform.Subscriptions.profile.consents.marketing.email.subscriptions.entry('daily-mail').subscribers.keys()
```

## 데이터 소스의 매개 변수 값(데이터 소스 동적 값)

매개 변수를 호출해야 하는 외부 데이터 소스에서 필드를 선택하는 경우 이 매개 변수를 지정할 수 있도록 오른쪽에 새 탭이 나타납니다. [이 페이지](../expression/expressionadvanced.md)를 참조하십시오.

보다 복잡한 사용 사례에서는 기본 식에 데이터 원본의 매개 변수를 포함하려는 경우 키워드 _params_&#x200B;을 사용하여 해당 값을 정의할 수 있습니다. 매개 변수는 다른 매개 변수를 포함하는 다른 데이터 소스에서도 유효한 표현식이 될 수 있습니다.

>[!NOTE]
>
>표현식에서 매개 변수 값을 정의하면 오른쪽에 있는 탭이 사라집니다.

다음 구문을 사용합니다.

```json
#{<datasource>.<field group>.fieldName, params: {<params-1-name>: <params-1-value>, <params-2-name>: <params-2-value>}}
```

* **`<params-1-name>`**: 데이터 원본의 첫 번째 매개 변수의 정확한 이름.
* **`<params-1-value>`**: 첫 번째 매개 변수의 값입니다. 모든 유효한 표현식일 수 있습니다.

예:

```json
#{Weather.main.temperature, params: {localisation: @event{Profile.address.localisation}}}
#{Weather.main.temperature, params: {localisation: #{GPSLocalisation.main.coordinates, params: {city: @event{Profile.address.city}}}}}
```

+++ AI 기술 자료 참조

이 단원에는 이 주제와 관련된 해석, 검색 및 질문 답변을 지원하기 위한 구조화된 지식이 포함되어 있습니다.

이해를 돕기 위해 이 정보를 이 페이지의 설명서와 통합해야 합니다. 두 소스 모두 독립적으로 사용하기 위한 것은 아닙니다. 이 페이지에서는 기능에 대해 설명하지만, 용어, 의도, 적용 가능성 및 제약 조건을 명확히 하는 데 도움이 되는 추가 컨텍스트를 제공합니다.

* **TL;DR:** 이 페이지에서는 기본값 구문, 맵 액세스 함수(`entry`, `firstEntryKey`, `keys`) 및 `params` 키워드를 사용하는 인라인 데이터 소스 매개 변수를 포함하여 여정 식에서 이벤트 필드와 데이터 소스 필드 그룹을 참조하는 방법에 대해 설명합니다.

**의도:**

* `@event{eventName.fieldPath}` 구문을 사용하여 식에서 이벤트 필드를 참조합니다.
* `#{dataSourceName.fieldGroupName.fieldPath}` 구문을 사용하여 데이터 원본 필드 그룹을 참조합니다.
* 표현식이 null을 반환하지 않도록 필드 참조에 대체 기본값 할당
* `entry()` 함수를 사용하여 ID 맵 또는 구독 맵에서 특정 항목을 검색합니다.
* `keys()` 함수를 사용하여 맵 필드에서 모든 키 검색
* `params` 키워드를 사용하여 매개 변수 값을 외부 데이터 원본에 인라인으로 전달합니다.

**용어집:**

* **필드 참조**: 이벤트 페이로드 또는 데이터 원본 필드 그룹 *(제품별) 내의 명명된 필드를 가리키는 식 구문*
* **defaultValue**: 필드가 없거나 null *(제품별)*&#x200B;일 때 반환되는 필드 참조에 추가된 선택적 대체 식입니다.
* **entry(key)**: 지정된 키 *(제품별)와 연결된 컬렉션 항목을 검색하는 맵 함수입니다.*
* **firstEntryKey()**: 맵 필드 *(제품별)의 첫 번째 키를 반환하는 맵 함수입니다.*
* **keys()**: 맵 필드 *(제품별)의 모든 키를 반환하는 맵 함수*
* **params 키워드**: 기본 식 *(제품별)* 내의 외부 데이터 원본 필드에 대한 매개 변수 값을 지정하는 인라인 구문

**보호 기능:**

* 특수 문자(숫자로 시작, `-` 포함 또는 `a-z A-Z 0-9 _` 외부 문자)가 포함된 필드 이름은 작은따옴표나 큰따옴표로 묶어야 합니다
* 기본값 표현식은 필드와 동일한 데이터 유형을 반환해야 합니다. 일치하지 않는 유형은 유효하지 않습니다
* `params` 키워드를 사용하여 매개 변수 값을 인라인으로 정의하면 편집기 오른쪽에 있는 별도의 매개 변수 탭이 사라집니다
* 기본값으로 사용되는 함수는 괄호 안에 캡슐화해야 합니다

**용어:**

* 정식 이름: 필드 참조 — 약어: 없음 — 변형: 필드 경로, 필드 표현식
* 동의어: `@event{...}` = &quot;event field reference&quot;; `#{...}` = &quot;data source field reference&quot;
* 혼동하지 않음: 이벤트 필드(접두사 `@`) ≠ 데이터 원본 필드(접두사 `#`)

**FAQ:**

* **Q: 숫자로 시작하는 이름의 필드를 어떻게 참조합니까?** — 필드 이름을 작은 따옴표나 큰 따옴표로 묶습니다(예: `#{OpenWeather.weatherData.rain.'3h'}`).
* **Q: 참조된 필드가 이벤트 페이로드에서 누락되고 기본값이 설정되지 않으면 어떻게 됩니까?** — 식이 `null`을(를) 반환합니다.
* **Q: 함수를 사용하여 동적 기본값을 설정하려면 어떻게 해야 합니까?** — 함수 호출을 괄호로 묶습니다(예: `defaultValue: (now())`).
* **Q: 구독자 맵의 첫 번째 키로 저장된 전자 메일 주소를 검색하려면 어떻게 합니까?** — 구독자 맵 필드에서 `firstEntryKey()` 함수를 사용합니다.
* **Q: 오른쪽 탭을 사용하지 않고 외부 데이터 원본에 매개 변수를 전달하려면 어떻게 해야 합니까?** — `params` 키워드 인라인 사용: `#{DataSource.group.field, params: {paramName: value}}`.

+++
