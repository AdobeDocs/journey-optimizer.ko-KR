---
solution: Journey Optimizer
product: journey optimizer
title: 조건부 지침(if, then, else)
description: 조건부 지침에 대해 알아보기
feature: Journeys
role: Developer
level: Experienced
keywords: 고급, 조건, 작업, 여정
exl-id: 5a5b35a7-e3b5-4dc0-8a87-e985956b04a4
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/SObpEvgu0D-pcoLVaKM7iRffLTSP1stp1zcg4Ygs-vQ
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: cce82f05-fc3c-4af7-85ff-8bba603861a7id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 576
ht-degree: 0%

---

# 조건부 지침(if, then, else) {#conditional-instruction}

조건부 지침(if, then, else)은 고급 편집기에서 지원됩니다. 이를 통해 보다 복잡한 표현식을 정의할 수 있습니다. 이 구성 요소는 다음 요소로 구성됩니다.

* **[!UICONTROL if]**: 먼저 평가할 조건입니다.
* **[!UICONTROL then]**: 조건 평가 결과가 true인 경우 평가할 식입니다.
* **[!UICONTROL else]**: 조건 평가 결과가 false인 경우 평가할 식입니다.

>[!NOTE]
>
>모든 표현식에 괄호가 필요합니다.

```json
if  (<expression1>)
then
   (<expression2>)
else
   (<expression3>)
```

`<expression1>`은(는) **부울**&#x200B;을 반환해야 합니다.

`<expression2>`과(와) `<expression3>`은(는) 같은 형식이거나 호환되는 형식이어야 합니다. 지원되는 서명 및 반환된 유형은 다음과 같습니다.

```json
boolean,boolean : boolean
dateTime,dateTime : dateTime
dateTimeOnly,dateTimeOnly : dateTimeOnly
decimal,integer : decimal
integer,decimal : integer
integer,decimal : decimal
duration,duration : duration
string,string : string
listBoolean,listBoolean : listBoolean
listDateTime,listDateTime : listDateTime
listDateTimeOnly,listDateTimeOnly : listDateTimeOnly
listDateOnly,listDateOnly : listDateOnly
listDecimal,listDecimal : listDecimal
listInteger,listInteger : listInteger
listString,listString : listString
```

**사용**

조건부 명령을 사용하면 조건 활동의 수를 줄여 여정 워크플로우를 최적화할 수 있습니다. 예를 들어 동일한 작업 활동 내에서 하나의 조건 표현식만 사용하여 필드 정의에 대한 두 가지 대체 요소를 지정할 수 있습니다.

작업 활동의 예(조건부 명령의 결과로 문자열이 필요한 필드의 경우):

```json
if (startWithIgnoreCase(@event{eventiOSPushPermissionAllowed.device.model}, 'iPad') or startWithIgnoreCase(@event{eventiOSPushPermissionAllowed.device.model}, 'iOS'))
then
   ('apns')
else
   ('fcm')
```

+++ AI 기술 자료 참조

이 단원에는 이 주제와 관련된 해석, 검색 및 질문 답변을 지원하기 위한 구조화된 지식이 포함되어 있습니다.

이해를 돕기 위해 이 정보를 이 페이지의 설명서와 통합해야 합니다. 두 소스 모두 독립적으로 사용하기 위한 것은 아닙니다. 이 페이지에서는 기능에 대해 설명하지만, 용어, 의도, 적용 가능성 및 제약 조건을 명확히 하는 데 도움이 되는 추가 컨텍스트를 제공합니다.

* **TL;DR:** 이 페이지에서는 구문 규칙, 지원되는 유형 조합 및 실제 사용 예제를 포함하여 여정 고급 표현식 편집기에서 사용할 수 있는 `if / then / else` 조건부 지침에 대해 설명합니다.

**의도:**

* 부울 조건을 기반으로 다른 값을 반환하려면 `if`, `then` 및 `else`을(를) 사용하여 조건부 식을 작성하십시오
* 단일 작업 활동 내에 인라인 조건부 논리를 임베드하여 여정의 조건 활동 수를 줄이십시오
* `then` 및 `else` 분기에 대해 유효한 데이터 형식 조합을 확인하십시오.
* 조건부 명령을 적용하여 장치 모델을 기반으로 푸시 알림 토큰을 APNS 또는 FCM으로 라우팅합니다

**용어집:**

* **조건부 명령**: 부울을 평가하고 두 식 *(제품별) 중 하나를 반환하는 고급 편집기의 `if / then / else` 식 구문*
* **고급 표현식 편집기**: 조건, 대기 활동 및 작업 매개 변수 매핑에 사용되는 복잡한 표현식을 작성하기 위한 Journey Optimizer 인터페이스 *(제품별)*

**보호 기능:**

* `if`, `then` 및 `else` 절의 모든 식에 괄호가 필요합니다.
* `if` 절(`<expression1>`)은 부울 형식을 반환해야 합니다.
* `then` 및 `else` 식(`<expression2>` 및 `<expression3>`)의 형식이 같거나 호환 가능한 형식이어야 합니다(예: `decimal` 및 `integer`은(는) 호환되며, `string` 및 `integer`은(는) 호환되지 않음).
* 모든 유형 조합이 지원되는 것은 아닙니다. 지원되는 서명 테이블에 나열된 쌍만 유효합니다

**용어:**

* 정식 이름: 조건부 지침 — 약어: 없음 — 변형: if/then/else, 삼항 스타일 조건
* 동의어: &quot;조건부 명령&quot; = &quot;인라인 조건&quot; = &quot;if-then-else 표현식&quot;
* 혼동하지 않음: 조건부 명령(인라인 표현식) ≠ 조건 활동(여정 캔버스 노드)

**FAQ:**

* **Q: `if` 절을 괄호로 묶어야 합니까?** — 예. `if` 절의 조건을 포함한 모든 표현식에 괄호가 필요합니다.
* **Q: `if / then / else`을(를) 사용하여 한 분기의 숫자와 다른 분기의 문자열을 반환할 수 있습니까?** — 아니요. `<expression2>`과(와) `<expression3>`은(는) 같거나 호환 가능한 유형을 사용해야 합니다.
* **Q: 조건부 명령을 사용하면 여정 복잡성을 어떻게 줄일 수 있습니까?** — 캔버스에서 별도의 조건 활동 노드를 사용하지 않고 하나의 표현식을 사용하여 단일 작업 활동 내에 두 개의 필드 값 대안을 지정할 수 있습니다.
* **Q: 두 분기가 모두 문자열이면 조건부 명령이 반환하는 형식은 무엇입니까?** — `string`을(를) 반환합니다.
* **Q: `if / then / else`을(를) 사용하여 푸시 알림 채널을 선택할 수 있습니까?** — 예. 예를 들어 Apple 장치의 경우 `'apns'`을(를) 반환하고 다른 장치의 경우 `'fcm'`을(를) 반환하도록 장치 모델을 평가하는 중입니다.

+++
