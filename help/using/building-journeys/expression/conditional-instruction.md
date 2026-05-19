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
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 168
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
