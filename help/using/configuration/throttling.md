---
solution: Journey Optimizer
product: journey optimizer
title: Throttling API
description: Throttling API로 작업하는 방법을 알아봅니다
feature: Journeys, API
role: User
level: Beginner
keywords: 외부, API, 최적화 프로그램, 한도
exl-id: b837145b-1727-43c0-a0e2-bf0e8a35347c
source-git-commit: 9f801b1fdcab38bffff851675eca5e2fb61dfbf9
workflow-type: tm+mt
source-wordcount: '1025'
ht-degree: 48%

---

# Throttling API로 작업하기

Throttling API는 초당 전송되는 이벤트 수를 제한하기 위해 제한 구성을 만들고 구성하고 모니터링하는 데 도움이 됩니다.

이 섹션에서는 API 작업 방법에 대한 전역 정보를 제공합니다. 자세한 API 설명은 [Adobe Journey Optimizer API 설명서](https://developer.adobe.com/journey-optimizer-apis/)에서 확인할 수 있습니다.

## 반드시 알아야 할 사항

* **조직당 하나의 구성:** 현재 조직당 하나의 구성만 허용됩니다. 구성은 프로덕션 샌드박스(헤더에서 `x-sandbox-name`을(를) 통해 제공됨)에 정의되어야 합니다.
* **조직 수준 응용 프로그램:** 구성이 조직 수준에서 적용됩니다.
* **API 제한 처리:** API에 설정된 제한에 도달하면 추가 이벤트가 최대 6시간 동안 큐에 대기됩니다. 이 값은 수정할 수 없습니다.
* **`maxHttpConnections`매개 변수:** &#39;maxHttpConnections&#39; 매개 변수는 최대 가용량 API에서만 사용할 수 있는 선택적 매개 변수이므로 Journey Optimizer에서 외부 시스템에 대해 여는 연결 수를 제한할 수 있습니다. [최대 가용량 API로 작업하는 방법을 알아봅니다](../configuration/capping.md)

  연결 수를 제한하고 이러한 외부 호출을 조절하려는 경우 동일한 끝점에 대해 두 개의 구성(한 개의 조절 및 한 개의 제한)을 구성할 수 있습니다. 하나의 엔드포인트에 대해 두 구성이 공존할 수 있습니다. 제한 종단점에 대해 &#39;maxHttpConnections&#39;를 설정하려면 제한 API를 사용하여 제한 임계값을 설정하고 제한 API를 사용하여 &#39;maxHttpConnections&#39;를 설정하십시오. 최대 가용량 API를 호출할 때 최대 가용량 임계값을 제한 임계값보다 높게 설정할 수 있으므로 최대 가용량 규칙이 효과적으로 실행되지 않습니다.

## 제한 API 설명 및 Postman 컬렉션 {#description}

아래 표에는 제한 API에 사용할 수 있는 명령이 나와 있습니다. 요청 샘플, 매개 변수 및 응답 형식을 포함한 자세한 정보는 [Adobe Journey Optimizer API 설명서](https://developer.adobe.com/journey-optimizer-apis/references/journeys/)에서 확인할 수 있습니다.

| 메서드 | 경로 | 설명 |
|---|---|---|
| [!DNL POST] | list/throttlingConfigs | 스로틀링 구성 목록 가져오기 |
| [!DNL POST] | /throttlingConfigs | 스로틀링 구성 만들기 |
| [!DNL POST] | /throttlingConfigs/`{uid}`/deploy | 스로틀링 구성 배포 |
| [!DNL POST] | /throttlingConfigs/`{uid}`/undeploy | 스로틀링 구성 배포 취소 |
| [!DNL POST] | /throttlingConfigs/`{uid}`/canDeploy | 스로틀링 구성을 배포할 수 있는지 확인 |
| [!DNL PUT] | /throttlingConfigs/`{uid}` | 스로틀링 구성 업데이트 |
| [!DNL GET] | /throttlingConfigs/`{uid}` | 스로틀링 구성 검색 |
| [!DNL DELETE] | /throttlingConfigs/`{uid}` | 스로틀링 구성 삭제 |

또한 테스트 구성에 도움이 되도록 [여기](https://github.com/AdobeDocs/JourneyAPI/blob/master/postman-collections/Journeys_Throttling-API_postman-collection.json)에서 Postman 컬렉션을 사용할 수 있습니다.

이 컬렉션은 __[Postman 콘솔의 통합](https://console.adobe.io/integrations) > 사용해 보기 > Postman 다운로드__&#x200B;를 통해 생성된 Adobe I/O 변수 컬렉션을 공유하도록 설정되었습니다. 이 컬렉션은 선택한 통합 값으로 Postman 환경 파일을 생성합니다.

다운로드하여 Postman에 업로드한 다음에는 `{JO_HOST}`, `{BASE_PATH}`, `{SANDBOX_NAME}` 세 가지 변수를 추가해야 합니다.
* `{JO_HOST}` : [!DNL Journey Optimizer] 게이트웨이 URL.
* `{BASE_PATH}` : API의 진입점입니다.
* `{SANDBOX_NAME}`: API 작업이 발생할 샌드박스 이름에 해당하는 헤더 **x-sandbox-name**(예: ‘prod’)입니다.  자세한 내용은 [샌드박스 개요](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=ko)를 참조하십시오.

## 스로틀링 구성 {#configuration}

다음은 스로틀링 구성의 구조입니다. **name** 및 **description** 속성은 선택 사항입니다.

```
{
    "name": "<given name - free text>",
    "description": "<given description - free text>"
    "urlPattern": "<endpoint URL - wildcards are allowed>",
    "methods": [ "<HTTP method such as GET, POST, PUT>" ],
    "maxThroughput": <max call throughput>
}
```

예:

```
{
  "name": "throttling-config-external",
  "description": "example of throttling config for an external endpoint",
  "urlPattern": "https://api.example.org/data/2.5/*",
  "methods": ["POST", "PUT"],
  "maxThroughput": 4000
}
```

>[!IMPORTANT]
>
>**deploy** 끝점을 호출한 후에만 구성이 활성화됩니다.

## 오류

구성을 만들거나 업데이트하면 프로세스는 해당 구성을 확인하고 고유 ID로 식별되는 검증 상태를 반환합니다.

```
"ok" or "error"
```

>[!IMPORTANT]
>
>속성 **maxThroughput**, **urlPattern**, **methods**&#x200B;는 필수 입력 사항입니다.
>
>**maxThroughput** 값은 200~5000 사이에 있어야 합니다.

스로틀링 구성을 만들거나 삭제 또는 배포할 때 다음 오류가 발생할 수 있습니다.

* **ERR_THROTTLING_CONFIG_100**: 스로틀링 구성: `<mandatory attribute>` 필수
* **ERR_THROTTLING_CONFIG_101**: 스로틀링 구성: maxThroughput은 필수 입력 사항이며 200~5000 사이여야 합니다.
* **ERR_THROTTLING_CONFIG_104**: 스로틀링 구성: 잘못된 URL 패턴
* **ERR_THROTTLING_CONFIG_105**: 스로틀링 구성: URL 패턴의 호스트 부분에는 와일드카드를 사용할 수 없습니다.
* **ERR_THROTTLING_CONFIG_106**: 스로틀링 구성: 잘못된 페이로드
* **THROTTLING_CONFIG_DELETE_FORBIDDEN_ERROR: 1456**, “배포한 스로틀링 구성을 삭제할 수 없습니다. 삭제하기 전에 배포를 취소하십시오.”
* **THROTTLING_CONFIG_DELETE_ERROR: 1457**, “스로틀링 구성을 삭제할 수 없습니다. 예기치 않은 오류가 발생했습니다.”
* **THROTTLING_CONFIG_DEPLOY_ERROR: 1458**, “스로틀링 구성을 배포할 수 없습니다. 예기치 않은 오류가 발생했습니다.”
* **THROTTLING_CONFIG_UNDEPLOY_ERROR: 1459**, “스로틀링 구성의 배포를 취소할 수 없습니다. 예기치 않은 오류가 발생했습니다.”
* **THROTTLING_CONFIG_GET_ERROR: 1460**, “스로틀링 구성을 가져올 수 없습니다. 예기치 않은 오류가 발생했습니다.”
* **THROTTLING_CONFIG_UPDATE_NOT_ACTIVE_ERROR: 1461**, “스로틀링 구성을 업데이트할 수 없습니다. 런타임 버전이 활성 상태가 아닙니다.”
* **THROTTLING_CONFIG_UPDATE_ERROR: 1462**, “스로틀링 구성을 업데이트할 수 없습니다. 예기치 않은 오류가 발생했습니다.”
* **THROTTLING_CONFIG_NON_PROD_SANDBOX_ERROR: 1463**, “스로틀링 구성 작업을 수행할 수 없습니다. 비프로덕션 샌드박스입니다.”
* **THROTTLING_CONFIG_CREATE_ERROR: 1464**, “스로틀링 구성을 만들 수 없습니다. 예기치 않은 오류가 발생했습니다.”
* **THROTTLING_CONFIG_CREATE_LIMIT_ERROR: 1465**, “스로틀링 구성을 만들 수 없습니다. 조직당 하나의 구성만 허용됩니다.”
* **THROTTLING_CONFIG_ALREADY_DEPLOYED_ERROR: 14466**, “스로틀링 구성을 배포할 수 없습니다. 이미 배포되었습니다.”
* **THROTTLING_CONFIG_NOT_FOUND_ERROR: 14467**, “스로틀링 구성을 찾을 수 없습니다.”
* **THROTTLING_CONFIG_NOT_DEPLOYED_ERROR: 14468**, “스로틀링 구성의 배포를 취소할 수 없습니다. 아직 배포되지 않은 상태입니다.”

**오류 예시**

비프로덕션 샌드박스에서 구성을 작성하려는 경우:

```
{
    "status": 400,
    "error": "{\"code\":1463,\"family\":\"INPUT_OUTPUT_ERROR\",\"message\":\"Operation not allowed on throttling config: non prod sandbox\",\"service\":\"vyg-authoring-api\",\"version\":\"ed87515\",\"context\":\"com.adobe.voyager.service.authoring.restapis.v1_0.ThrottlingConfigService:384\",\"schema\":\"throttlingConfigs$ui-tests\"}",
    "requestId": "5sgnAYXs8mpswwjAFEIaAU2faQYbtyHc"
}
```

지정한 샌드박스가 존재하지 않는 경우:

```
{
    "status": 500,
    "error": "{\"code\":4000,\"family\":\"INTERNAL_ERROR\",\"message\":\"INTERNAL ERROR\",\"service\":\"vyg-authoring-api\",\"version\":\"ed87515\",\"context\":\"com.adobe.voyager.common.exceptions.ApiErrorException:43\"}",
    "requestId": "04ZJ4e5ki4bYs3lfO17a7hovRGewjvdK"
}
```

다른 구성을 만들려는 경우:

```
{
    "status": 400,
    "error": "{\"code\":1465,\"family\":\"INPUT_OUTPUT_ERROR\",\"message\":\"Can't create throttling config: only one config allowed per org\",\"service\":\"vyg-authoring-api\",\"version\":\"ed87515\",\"context\":\"com.adobe.voyager.service.authoring.restapis.v1_0.ThrottlingConfigService:108\",\"schema\":\"throttlingConfigs$prod\"}",
    "requestId": "A7ezT8JhOQT4WIAf1Fv7K2wCDA8281qM"
}
```

## 런타임 수준에서 본 구성의 수명 주기 {#config}

배포를 취소한 구성은 런타임 수준에서 비활성 상태로 표시되고 대기 중인 이벤트는 24시간 동안 계속 처리됩니다. 그 다음에는 해당 구성이 런타임 서비스에서 삭제됩니다.

구성의 배포를 취소한 후에 업데이트하여 재배포할 수 있습니다. 그러면 향후 작업 실행 시 고려할 새 런타임 구성이 만들어집니다.

이미 배포한 구성을 업데이트하면 새로운 값을 즉시 고려합니다. 기본 시스템 리소스는 자동으로 조정됩니다. 구성의 배포를 취소한 다음 재배포하는 것보다 적합한 방법입니다.

## 응답 예제 {#responses}

**만들기 - POST**

```
{
    "canDeploy": {
        "validationStatus": "ok"
    },
    "createdElement": {
        "name": "throttling-config-external",
        "description": "example of throttling config for an external endpoint",
        "urlPattern": "https://api.example.org/data/2.5/*",
        "methods": [
            "PUT",
            "POST"
        ],
        "maxThroughput": 4000,
        "orgId": "AC202A3A5F615BD30A495FDE@AdobeOrg",
        "sandboxId": "8872a010-f91e-11ea-895c-11ef8f98ba52",
        "sandboxName": "prod",
        "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
        "metadata": {
            "createdBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "createdById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "lastModifiedBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "lastModifiedById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "createdAt": "2023-03-22T10:48:16.099647Z",
            "lastModifiedAt": "2023-03-22T10:48:16.099647Z"
        },
        "state": "created",
        "authoringFormatVersion": "1.0"
    },
    "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
    "uri": "/voyager/apis/throttlingConfigs/043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
    "resStatus": "created"
}
```

**업데이트 - PUT**

```
{
    "updatedElement": {
        "_id": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6_8872a010-f91e-11ea-895c-11ef8f98ba52",
        "name": "throttling-config-external -- optional",
        "description": "example of throttling config for an external endpoint -- optional",
        "urlPattern": "https://api.example.org/data/2.5/*",
        "methods": [
            "POST"
        ],
        "maxThroughput": 5000,
        "orgId": "AC202A3A5F615BD30A495FDE@AdobeOrg",
        "sandboxId": "8872a010-f91e-11ea-895c-11ef8f98ba52",
        "sandboxName": "prod",
        "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
        "metadata": {
            "createdBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "createdById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "lastModifiedBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "lastModifiedById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "createdAt": "2023-03-22T10:48:16.099647Z",
            "lastModifiedAt": "2023-03-22T11:39:14.212983Z"
        },
        "state": "updated",
        "authoringFormatVersion": "1.0",
        "hasBeenDeployed": false
    },
    "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
    "uri": "/voyager/apis/throttlingConfigs/043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
    "resStatus": "updated",
    "canDeploy": {
        "validationStatus": "ok"
    }
}
```

**읽기(업데이트 후) - GET**

```
{
    "result": {
        "_id": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6_8872a010-f91e-11ea-895c-11ef8f98ba52",
        "name": "throttling-config-external -- optional",
        "description": "example of throttling config for an external endpoint -- optional",
        "urlPattern": "https://api.example.org/data/2.5/*",
        "methods": [
            "POST"
        ],
        "maxThroughput": 5000,
        "orgId": "AC202A3A5F615BD30A495FDE@AdobeOrg",
        "sandboxId": "8872a010-f91e-11ea-895c-11ef8f98ba52",
        "sandboxName": "prod",
        "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
        "metadata": {
            "createdBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "createdById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "lastModifiedBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "lastModifiedById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "createdAt": "2023-03-22T10:48:16.099647Z",
            "lastModifiedAt": "2023-03-22T11:39:14.212983Z"
        },
        "state": "updated",
        "authoringFormatVersion": "1.0",
        "hasBeenDeployed": false
    }
}
```

**읽기(배포 후) - GET**

```
{
    "result": {
        "_id": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6_8872a010-f91e-11ea-895c-11ef8f98ba52",
        "orgId": "AC202A3A5F615BD30A495FDE@AdobeOrg",
        "sandboxId": "8872a010-f91e-11ea-895c-11ef8f98ba52",
        "sandboxName": "prod",
        "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
        "urlPattern": "https://api.example.org/data/2.5/*",
        "methods": [
            "POST"
        ],
        "maxThroughput": 5000,
        "authoringFormatVersion": "1.0",
        "name": "throttling-config-external -- optional",
        "description": "example of throttling config for an external endpoint -- optional",
        "version": "1.0",
        "state": "deployed",
        "metadata": {
            "createdBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "createdById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "createdAt": "2023-03-22T10:48:16.099647Z",
            "lastModifiedBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "lastModifiedById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "lastModifiedAt": "2023-03-22T11:39:14.212983Z",
            "lastDeployedBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "lastDeployedById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "lastDeployedAt": "2023-03-22T11:46:07.532648Z"
        },
        "hasBeenDeployed": true
    }
}
```

## 사용 사례 {#uc}

이 섹션에는 [!DNL Journey Optimizer]에서 제한 구성을 관리하기 위한 주요 사용 사례와 사용 사례를 구현하는 데 필요한 관련 API 명령이 나열되어 있습니다.

각 API 명령에 대한 자세한 내용은 [API 설명 및 Postman 컬렉션](#description)에서 확인할 수 있습니다.

+++새 조절 구성 만들기 및 배포

사용할 API 호출:

1. **`list`** - 기존 구성을 검색합니다.
1. **`create`** - 새 구성을 만듭니다.
1. **`candeploy`** - 구성을 배포할 수 있는지 확인합니다.
1. **`deploy`** - 구성을 배포합니다.

+++

+++조정 구성 업데이트 및 배포(아직 배포되지 않음)

사용할 API 호출:

1. **`list`** - 기존 구성을 검색합니다.
1. **`get`** - 특정 구성의 세부 정보를 가져옵니다.
1. **`update`** - 구성을 수정합니다.
1. **`candeploy`** - 배포 적격성을 확인합니다.
1. **`deploy`** - 구성을 배포합니다.

+++

+++배포된 제한 구성 배포 취소 및 삭제

사용할 API 호출:

1. **`list`** - 기존 구성을 검색합니다.
1. **`undeploy`** - 구성을 배포 취소합니다.
1. **`delete`** - 구성을 제거합니다.

+++

+++배포된 제한 구성 삭제

하나의 API 호출에서만 `forceDelete` 매개 변수를 사용하여 구성을 배포 취소하고 삭제할 수 있습니다.

사용할 API 호출:

1. **`list`** - 기존 구성을 검색합니다.
1. **`delete`(`forceDelete` 매개 변수 사용)** - 배포된 구성을 한 단계로 강제로 삭제합니다.

+++

+++이미 배포된 제한 구성 업데이트

>[!NOTE]
>
>업데이트하기 전에 구성의 배포를 취소할 필요는 없습니다.

사용할 API 호출:

1. **`list`** - 기존 구성을 검색합니다.
1. **`get`** - 특정 구성의 세부 정보를 가져옵니다.
1. **`update`** - 구성을 수정합니다.

+++
