---
solution: Journey Optimizer
product: journey optimizer
title: Capping API
description: 최대 가용량 API로 작업하는 방법을 알아봅니다
feature: Journeys, API
role: Developer
level: Beginner
keywords: 외부, API, 최적화 프로그램, 한도
exl-id: 377b2659-d26a-47c2-8967-28870bddf5c5
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 6%

---

# 최대 가용량 API 작업 {#work}

최대 가용량 API를 사용하면 최대 가용량 구성을 만들고, 구성하고, 모니터링할 수 있습니다.

이 섹션에서는 API 작업 방법에 대한 전역 정보를 제공합니다. 자세한 API 설명은 [Adobe Journey Optimizer API 설명서](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"}에서 확인할 수 있습니다.

## 최대 가용량 API 설명 및 Postman 컬렉션 {#description}

아래 표에는 최대 가용량 API에 사용할 수 있는 명령이 나열되어 있습니다. 요청 샘플, 매개 변수 및 응답 형식을 포함한 자세한 정보는 [Adobe Journey Optimizer API 설명서](https://developer.adobe.com/journey-optimizer-apis/references/journeys/){target="_blank"}에서 확인할 수 있습니다.

| 메서드 | 경로 | 설명 |
|---|---|---|
| [!DNL POST] | list/endpointConfigs | 끝점 제한 구성 목록 가져오기 |
| [!DNL POST] | /endpointConfigs | 엔드포인트 제한 구성 만들기 |
| [!DNL POST] | /endpointConfigs/`{uid}`/deploy | 끝점 제한 구성 배포 |
| [!DNL POST] | /endpointConfigs/`{uid}`/undeploy | 끝점 제한 구성 배포 해제 |
| [!DNL POST] | /endpointConfigs/`{uid}`/canDeploy | 끝점 제한 구성을 배포할 수 있는지 확인 |
| [!DNL PUT] | /endpointConfigs/`{uid}` | 끝점 제한 구성 업데이트 |
| [!DNL GET] | /endpointConfigs/`{uid}` | 끝점 제한 구성 검색 |
| [!DNL DELETE] | /endpointConfigs/`{uid}` | 끝점 제한 구성 삭제 |

구성을 만들거나 업데이트할 때 페이로드의 구문 및 무결성을 보장하기 위해 자동으로 검사가 수행됩니다.
일부 문제가 발생하면 작업을 수행할 때 경고 또는 오류가 반환되어 구성을 수정하는 데 도움이 됩니다.

또한 테스트 구성에 도움이 되도록 [여기](https://github.com/AdobeDocs/JourneyAPI/blob/master/postman-collections/Journeys_Capping-API_postman-collection.json)에서 Postman 컬렉션을 사용할 수 있습니다.

이 컬렉션은 __[Postman 콘솔의 통합](https://console.adobe.io/integrations) > 사용해 보기 > Postman 다운로드__&#x200B;를 통해 생성된 Adobe I/O 변수 컬렉션을 공유하도록 설정되었습니다. 이 컬렉션은 선택한 통합 값으로 Postman 환경 파일을 생성합니다.

다운로드하여 Postman에 업로드한 다음에는 `{JO_HOST}`, `{BASE_PATH}`, `{SANDBOX_NAME}` 세 가지 변수를 추가해야 합니다.

* `{JO_HOST}` : [!DNL Journey Optimizer] 게이트웨이 URL.
* `{BASE_PATH}` : API의 진입점입니다.
* `{SANDBOX_NAME}`: API 작업이 발생할 샌드박스 이름에 해당하는 헤더 **x-sandbox-name**(예: ‘prod’)입니다.  자세한 내용은 [샌드박스 개요](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=ko){target="_blank"}를 참조하십시오.

## 끝점 구성

다음은 끝점 구성의 기본 구조입니다.

```json
{
    "url": "<endpoint URL>",  //wildcards are allowed in the endpoint URL
    "methods": [ "<HTTP method such as GET, POST, >, ...],
    "services": {
        "<service name>": { . //must be "action" or "dataSource" 
            "maxHttpConnections": <max connections count to the endpoint (optional)>
            "rating": {          
                "maxCallsCount": <max calls to be performed in the period defined by period/timeUnit>,
                "periodInMs": <integer value greater than 0>
            }
        },
        ...
    }
}
```

>[!IMPORTANT]
>
>**maxHttpConnections** 매개 변수는 선택 사항입니다. 이를 통해 Journey Optimizer이 외부 시스템에 대해 여는 연결 수를 제한할 수 있습니다.
>
>설정할 수 있는 최대값은 400입니다. 아무 것도 지정되지 않은 경우, 시스템은 시스템의 동적 확장에 따라 최대 수천 개의 연결을 열 수 있습니다.
>
>최대 가용량 구성이 배포될 때 `maxHttpConnections` 값이 설정되지 않은 경우 배포된 구성에 기본 `maxHttpConnections = -1`이(가) 추가되고 Journey Optimizer에서 기본 시스템 값을 사용합니다.

예:

```json
{
  "url": "https://api.example.org/data/2.5/*",
  "methods": [
    "GET"
  ],
  "services": {
    "dataSource": {
      "rating": {
        "maxCallsCount": 500,
        "periodInMs": 1000
      }
    }
  }
}
```

>[!IMPORTANT]
>
>**deploy** 끝점을 호출한 후에만 구성이 활성화됩니다.

## 경고 및 오류

**canDeploy** 메서드가 호출되면 이 프로세스는 구성을 확인하고 다음 중 하나의 고유 ID로 확인된 유효성 검사 상태를 반환합니다.

```json
"ok" or "error"
```

잠재적 오류는 다음과 같습니다.

* **ERR_ENDPOINTCONFIG_100**: 최대 구성: 누락되었거나 잘못된 url
* **ERR_ENDPOINTCONFIG_101**: 구성 제한: url 형식이 잘못되었습니다.
* **ERR_ENDPOINTCONFIG_102**: 최대 구성: url 형식이 잘못되었습니다. url의 wildchar가 호스트에 허용되지 않습니다.:port
* **ERR_ENDPOINTCONFIG_103**: 최대 구성: HTTP 메서드가 없습니다.
* **ERR_ENDPOINTCONFIG_104**: 최대 구성: 호출 등급이 정의되지 않았습니다.
* **ERR_ENDPOINTCONFIG_107**: 최대 호출 수 제한 구성: 잘못된 최대 호출 수(maxCallsCount)
* **ERR_ENDPOINTCONFIG_108**: 최대 호출 수 제한 구성: 잘못된 최대 호출 수(periodInMs)
* **ERR_ENDPOINTCONFIG_111**: 최대 구성: 끝점 구성을 만들 수 없음: 잘못된 페이로드
* **ERR_ENDPOINTCONFIG_112**: 최대 구성: 끝점 구성을 만들 수 없습니다. JSON 페이로드가 필요합니다.
* **ERR_AUTHORING_ENDPOINTCONFIG_1**: 잘못된 서비스 이름 `<!--<given value>-->`: &#39;dataSource&#39; 또는 &#39;action&#39;이어야 합니다.

잠재적인 경고는 다음과 같습니다.

**ERR_ENDPOINTCONFIG_106**: 최대 구성: 최대 HTTP 연결이 정의되지 않음: 기본적으로 제한 없음

## 사용 사례

이 섹션에는 [!DNL Journey Optimizer]에서 최대 가용량 구성을 관리하기 위한 주요 사용 사례와 사용 사례를 구현하는 데 필요한 관련 API 명령이 나열되어 있습니다.

각 API 명령에 대한 자세한 내용은 [API 설명 및 Postman 컬렉션](#description)에서 확인할 수 있습니다.

+++새 최대 가용량 구성 만들기 및 배포

사용할 API 호출:

1. **`list`** - 기존 구성을 검색합니다.
1. **`create`** - 새 구성을 만듭니다.
1. **`candeploy`** - 구성을 배포할 수 있는지 확인합니다.
1. **`deploy`** - 구성을 배포합니다.

+++

+++최대 가용량 구성 업데이트 및 배포(아직 배포되지 않음)

사용할 API 호출:

1. **`list`** - 기존 구성을 검색합니다.
1. **`get`** - 특정 구성의 세부 정보를 가져옵니다.
1. **`update`** - 구성을 수정합니다.
1. **`candeploy`** - 배포 적격성을 확인합니다.
1. **`deploy`** - 구성을 배포합니다.

+++

+++배포된 최대 가용량 구성 배포 취소 및 삭제

사용할 API 호출:

1. **`list`** - 기존 구성을 검색합니다.
1. **`undeploy`** - 구성을 배포 취소합니다.
1. **`delete`** - 구성을 제거합니다.

+++

+++한 단계에서 배포된 최대 가용량 구성을 삭제합니다.

하나의 API 호출에서만 `forceDelete` 매개 변수를 사용하여 구성을 배포 취소하고 삭제할 수 있습니다.

사용할 API 호출:

1. **`list`** - 기존 구성을 검색합니다.
1. **`delete`(`forceDelete` 매개 변수 사용)** - 배포된 구성을 한 단계로 강제로 삭제합니다.

+++

+++이미 배포된 최대 가용량 구성 업데이트

>[!NOTE]
>
>이미 배포된 구성을 업데이트한 후 재배포가 필요합니다.

사용할 API 호출:

1. **`list`** - 기존 구성을 검색합니다.
1. **`get`** - 특정 구성의 세부 정보를 가져옵니다.
1. **`update`** - 구성을 수정합니다.
1. **`undeploy`** - 변경 내용을 적용하기 전에 구성을 배포 취소합니다.
1. **`candeploy`** - 배포 적격성을 확인합니다.
1. **`deploy`** - 업데이트된 구성을 배포합니다.

+++
