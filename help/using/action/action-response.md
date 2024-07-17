---
solution: Journey Optimizer
product: journey optimizer
title: 사용자 지정 작업 개선 사항
description: 사용자 지정 작업에 대한 최신 개선 사항에 대해 자세히 알아보기
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: 작업, 서드파티, 사용자 지정, 여정, API
exl-id: d88daa58-20af-4dac-ae5d-4c10c1db6956
source-git-commit: 7e850261f1a82492c5df93c4437b4e3c6859a2d7
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 5%

---

# 사용자 정의 작업에서 API 호출 응답 사용 {#custom-action-enhancements}

사용자 지정 작업에서 API 호출 응답을 활용하고, 이러한 응답을 기반으로 여정을 오케스트레이션할 수 있습니다.

<!--
You can now leverage API call responses in custom actions and orchestrate your journeys based on these responses.

This capability was previously only available when using data sources. You can now use it with custom actions. 
-->

## 중요 정보{#custom-action-enhancements-notes}

<!--
* Custom actions should only be used with private or internal endpoints, and used with an appropriate capping or throttling limit. See [this page](../configuration/external-systems.md). 
-->

* 스칼라 배열은 응답 페이로드에서 지원됩니다.

  ```
  "dummyScalarArray": [
  "val1",
  "val2"
  ]
  ```

* 이기종 스토리지는 응답 페이로드에서 지원되지 않습니다.

  ```
  "dummyRandomArray": [
  20,
  "aafw",
  false
  ]
  ```

<!--
## Best practices{#custom-action-enhancements-best-practices}

A capping limit of 5000 calls/s is defined for all custom actions. This limit has been set based on customers usage, to protect external endpoints targeted by custom actions. You need to take this into account in your audience-based journeys by defining an appropriate reading rate (5000 profiles/s when custom actions are used). If needed, you can override this setting by defining a greater capping or throttling limit through our Capping/Throttling APIs. See [this page](../configuration/external-systems.md).

You should not target public endpoints with custom actions for various reasons:

* Without proper capping or throttling, there is a risk of sending too many calls to a public endpoint that may not support such volume.
* Profile data can be sent through custom actions, so targeting a public endpoint could lead to inadvertently sharing personal information externally.
* You have no control on the data being returned by public endpoints. If an endpoint changes its API or starts sending incorrect information, those will be made available in communications sent, with potential negative impacts.
-->

<!--
## Define the custom action {#define-custom-action}

When defining the custom action, two enhancements have been made available: the addition of the GET method and the new payload response field. The other options and parameters are unchanged. See [this page](../action/about-custom-action-configuration.md).

### Endpoint configuration {#endpoint-configuration}

The **URL configuration** section has been renamed **Endpoint configuration**.

In the **Method** drop-down, you can now select **GET**.

![](assets/action-response1.png){width="70%" align="left"}

### Payloads {#payloads-new}

The **Action parameters** section has been renamed **Payloads**. Two fields are available:

* The **Request** field: this field is only available for POST and PUT calling methods.
* The **Response** field: this is the new capability. This field as available for all calling methods.

>[!NOTE]
> 
>Both these fields are optional.

![](assets/action-response2.png){width="70%" align="left"}
-->

## 사용자 지정 작업 구성 {#config-response}

1. 사용자 지정 작업을 만듭니다. [이 페이지](../action/about-custom-action-configuration.md)를 참조하십시오.

1. **응답** 필드 내부를 클릭합니다.

   ![](assets/action-response2.png){width="80%" align="left"}

1. 호출에서 반환된 페이로드의 예제를 붙여넣습니다. 필드 유형(문자열, 정수 등)이 올바른지 확인합니다. 다음은 호출 동안 캡처된 응답 페이로드의 예입니다. 로컬 엔드포인트는 충성도 포인트 수 및 프로필 상태를 전송합니다.

   ```
   {
   "customerID" : "xY12hye",    
   "status":"gold",
   "points": 1290 }
   ```

   ![](assets/action-response4.png){width="80%" align="left"}

   API가 호출될 때마다 시스템은 페이로드 예제에 포함된 모든 필드를 검색합니다.

1. customerID를 쿼리 매개 변수로도 추가하겠습니다.

   ![](assets/action-response9.png){width="80%" align="left"}

1. **저장**&#x200B;을 클릭합니다.

## 여정에서 응답 활용 {#response-in-journey}

여정에 사용자 지정 작업을 추가하기만 하면 됩니다. 그런 다음 조건, 기타 작업 및 메시지 개인화의 응답 페이로드 필드를 활용할 수 있습니다.

예를 들어 충성도 포인트의 수를 확인하는 조건을 추가할 수 있습니다. 사용자가 레스토랑에 들어오면 로컬 종단점이 프로필의 충성도 정보와 함께 호출을 보냅니다. 프로필이 Gold 고객인 경우 푸시를 보낼 수 있습니다. 또한 호출에서 오류가 감지되면 시스템 관리자에게 알리는 사용자 지정 작업을 보내십시오.

![](assets/action-response5.png)

1. 이전에 만든 이벤트와 충성도 사용자 지정 작업을 추가합니다.

1. 충성도 사용자 지정 작업에서 고객 ID 쿼리 매개 변수를 프로필 ID에 매핑합니다. **시간 초과 또는 오류 발생 시 대체 경로를 추가** 옵션을 선택합니다.

   ![](assets/action-response10.png)

1. 첫 번째 분기에서 조건을 추가하고 고급 편집기를 사용하여 **Context** 노드 아래의 작업 응답 필드를 활용합니다.

   ![](assets/action-response6.png)

1. 그런 다음 푸시를 추가하고 응답 필드를 사용하여 메시지를 개인화합니다. 이 예제에서는 충성도 포인트 수와 고객 상태를 사용하여 콘텐츠를 개인화합니다. 작업 응답 필드는 **컨텍스트 특성** > **Journey Orchestration** > **작업**&#x200B;에서 사용할 수 있습니다.

   ![](assets/action-response8.png)

   >[!NOTE]
   >
   >사용자 지정 작업을 입력하는 각 프로필은 호출을 트리거합니다. 응답이 항상 동일하더라도 여정은 프로필당 한 번의 호출을 수행합니다.

1. 시간 제한 및 오류 분기에 조건을 추가하고 기본 제공 **jo_status_code** 필드를 활용하십시오. 이 예제에서는
   **http_400** 오류 유형입니다. [이 섹션](#error-status)을 참조하십시오.

   ```
   @action{ActionLoyalty.jo_status_code} == "http_400"
   ```

   ![](assets/action-response7.png)

1. 조직에 전송할 사용자 지정 작업을 추가합니다.

   ![](assets/action-response11.png)

## 테스트 모드 로그 {#test-mode-logs}

테스트 모드를 통해 사용자 지정 작업 응답과 관련된 상태 로그에 액세스할 수 있습니다. 여정에서 응답이 있는 사용자 지정 작업을 정의한 경우 해당 로그에 외부 끝점에서 반환된 페이로드를 표시하는 **actionsHistory** 섹션이 표시됩니다(해당 사용자 지정 작업의 응답). 이 기능은 디버깅 측면에서 매우 유용할 수 있습니다.

![](assets/action-response12.png)

## 오류 상태 {#error-status}

응답 페이로드가 정의되지 않은 경우에도 **jo_status_code** 필드를 항상 사용할 수 있습니다.

다음은 이 필드에 사용할 수 있는 값입니다.

* http 상태 코드: http_`<HTTP API call returned code>`(예: http_200 또는 http_400)
* 시간 초과 오류: **시간 초과**
* 최대 가용량 오류: **제한됨**
* 내부 오류: **internalError**

반환된 http 코드가 2xx보다 크거나 오류가 발생하면 작업 호출이 오류로 간주됩니다. 이러한 경우 여정은 전용 시간 초과 또는 오류 분기로 이동합니다.

>[!WARNING]
>
>새로 만든 사용자 지정 작업에만 **jo_status_code** 필드가 기본적으로 포함됩니다. 기존 사용자 지정 작업에 사용하려면 작업을 업데이트해야 합니다. 예를 들어 설명을 업데이트하고 저장할 수 있습니다.

## 표현식 구문 {#exp-syntax}

구문은 다음과 같습니다.

```json
#@action{myAction.myField} 
```

다음은 몇 가지 예입니다.

```json
 // action response field
 @action{<action name>.<path to the field>}
 @action{ActionLoyalty.status}
```

```json
 // action response field
 @action{<action name>.<path to the field>, defaultValue: <default value expression>}
 @action{ActionLoyalty.points, defaultValue: 0}
 @action{ActionLoyalty.points, defaultValue: @event{myEvent.newPoints}}
```

사용자 지정 작업 응답에서 컬렉션을 조작하는 동안 `currentActionField`을(를) 사용하여 현재 항목에 액세스할 수 있습니다.

```json
count(
@action{MyAction.MyCollection.all(
currentActionField.description == "abc"
)}
)
```

## 추가 리소스

자세한 내용은 다음 페이지를 참조하십시오.

* [필드 참조](../building-journeys/expression/field-references.md).
* [컬렉션 관리 기능](../building-journeys/expression/collection-management-functions.md)
