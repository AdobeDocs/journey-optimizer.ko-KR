---
solution: Journey Optimizer
product: journey optimizer
title: Capping API
description: 최대 가용량 API 사용 방법 알아보기
role: User
level: Beginner
keywords: 외부, API, 최적기, 최대 가용량
exl-id: 377b2659-d26a-47c2-8967-28870bddf5c5
source-git-commit: c823d1a02ca9d24fc13eaeaba2b688249e61f767
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 30%

---

# 최대 가용량 API 작업 {#work}

최대 가용량 API는 최대 가용량 구성을 생성, 구성 및 모니터링하는 데 도움이 됩니다.

이 섹션에서는 API를 사용하는 방법에 대한 글로벌 정보를 제공합니다. 자세한 API 설명은 [Adobe Journey Optimizer API 설명서](https://developer.adobe.com/journey-optimizer-apis/).

## API 설명 최대 가용량

| 메서드 | 경로 | 설명 |
|---|---|---|
| [!DNL POST] | list/endpointConfigs | 끝점 최대 가용량 구성 목록 가져오기 |
| [!DNL POST] | /endpointConfigs | 끝점 최대 가용량 구성 만들기 |
| [!DNL POST] | /endpointConfigs/`{uid}`/deploy | 끝점 최대 가용량 구성 배포 |
| [!DNL POST] | /endpointConfigs/`{uid}`/배포 취소 | 끝점 최대 가용량 구성 배포 취소 |
| [!DNL POST] | /endpointConfigs/`{uid}`/canDeploy | 끝점 최대 가용량 구성을 배포할 수 있는지 여부를 확인합니다 |
| [!DNL PUT] | /endpointConfigs/`{uid}` | 끝점 최대 가용량 구성 업데이트 |
| [!DNL GET] | /endpointConfigs/`{uid}` | 끝점 최대 가용량 구성 검색 |
| [!DNL DELETE] | /endpointConfigs/`{uid}` | 엔드포인트 캡핑 구성 삭제 |

구성을 만들거나 업데이트할 때 페이로드의 구문과 무결성을 보장하기 위해 검사가 자동으로 수행됩니다.
일부 문제가 발생하면 작업을 통해 경고 또는 오류를 반환하여 구성을 수정할 수 있습니다.

## 끝점 구성

다음은 끝점 구성의 기본 구조입니다.

```
{
    "url": "<endpoint URL>",  //wildcards are allowed in the endpoint URL
    "methods": [ "<HTTP method such as GET, POST, >, ...],
    "services": {
        "<service name>": { . //must be "action" or "dataSource" 
            "maxHttpConnections": <max connections count to the endpoint>
            "rating": {          
                "maxCallsCount": <max calls to be performed in the period defined by period/timeUnit>,
                "periodInMs": <integer value greater than 0>
            }
        },
        ...
    }
}
```

### 예:

```
`{
  "url": "https://api.example.org/data/2.5/*",
  "methods": [
    "GET"
  ],
  "services": {
    "dataSource": {
      "maxHttpConnections": 30000,
      "rating": {
        "maxCallsCount": 5000,
        "periodInMs": 1000
      }
    }
  },
  "orgId": "<IMS Org Id>"
}
```

## 경고 및 오류

다음의 경우 **canDeploy** 메서드가 호출되면 프로세스가 구성을 확인하고 고유 ID로 식별된 유효성 검사 상태를 반환합니다.

```
"ok" or "error"
```

잠재적 오류는 다음과 같습니다.

* **ERR_ENDPOINTCONFIG_100**: 최대 가용량 구성: URL이 없거나 잘못되었습니다.
* **ERR_ENDPOINTCONFIG_101**: 최대 가용량 구성: 잘못된 url
* **ERR_ENDPOINTCONFIG_102**: 최대 가용량 구성: 잘못된 url: url의 와일드카드 문자는 host:port에서 허용되지 않습니다.
* **ERR_ENDPOINTCONFIG_103**: 최대 가용량 구성: HTTP 메서드 누락
* **ERR_ENDPOINTCONFIG_104**: 최대 가용량 구성: 정의된 통화 등급 없음
* **ERR_ENDPOINTCONFIG_107**: 최대 가용량 구성: 잘못된 최대 호출 수(maxCallsCount)
* **ERR_ENDPOINTCONFIG_108**: 최대 가용량 구성: 잘못된 최대 호출 수(periodInMs)입니다.
* **ERR_ENDPOINTCONFIG_11**: 최대 가용량 구성: 끝점 구성을 만들 수 없습니다. 잘못된 페이로드
* **ERR_ENDPOINTCONFIG_112**: 최대 가용량 구성: 끝점 구성을 만들 수 없습니다. json 페이로드 필요
* **ERR_AUTHORING_ENDPOINTCONFIG_1**: 잘못된 서비스 이름 `<!--<given value>-->`: &#39;dataSource&#39; 또는 &#39;action&#39;이어야 합니다.

잠재적 경고는 다음과 같습니다.

**ERR_ENDPOINTCONFIG_106**: 최대 가용량 구성: 최대 HTTP 연결이 정의되지 않았습니다. 기본적으로 제한되지 않음

## 사용 사례

이 섹션에서는 에서의 최대 가용량 구성을 관리하기 위해 수행할 수 있는 5가지 기본 사용 사례를 확인할 수 있습니다 [!DNL Journey Optimizer].

[여기](https://raw.githubusercontent.com/AdobeDocs/JourneyAPI/master/postman-collections/Journey-Orchestration_Capping-API_postman-collection.json)에서 테스트 및 구성에 도움이 되는 Postman 컬렉션을 사용할 수 있습니다.

이 Postman 컬렉션은 __[Adobe I/O Console의 통합](https://console.adobe.io/integrations) > 사용해 보기 > Postman용으로 다운로드__&#x200B;를 통해 생성된 Postman 변수 컬렉션을 공유하는 용도로 설정되었습니다. 이 옵션은 선택한 통합 값을 가진 Postman 환경 파일을 생성합니다.

다운로드하여 Postman에 업로드한 다음에는 `{JO_HOST}`, `{BASE_PATH}`, `{SANDBOX_NAME}` 세 가지 변수를 추가해야 합니다.
* `{JO_HOST}`: [!DNL Journey Optimizer] 게이트웨이 URL입니다.
* `{BASE_PATH}`: API의 시작 지점입니다. 
* `{SANDBOX_NAME}`: API 작업이 발생할 샌드박스 이름에 해당하는 헤더 **x-sandbox-name**(예: ‘prod’)입니다.  자세한 내용은 [샌드박스 개요](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=ko)를 참조하십시오.

다음 섹션에서는 사용 사례를 수행하기 위한 Rest API 호출 목록을 순서대로 확인할 수 있습니다.

사용 사례°1: **새 최대 가용량 구성 만들기 및 배포**

1. list
1. create
1. candeploy
1. deploy

사용 사례°2: **아직 배포되지 않은 최대 가용량 구성 업데이트 및 배포**

1. list
1. get
1. update
1. candeploy
1. deploy

사용 사례°3: **배포된 최대 가용량 구성 배포 취소 및 삭제**

1. list
1. undeploy
1. delete

사용 사례°4: **배포된 최대 가용량 구성을 삭제합니다.**

forceDelete 매개 변수를 사용하면 API 호출 단 한 번에 구성의 배포를 취소하고 삭제할 수 있습니다.
1. list
1. delete, with forceDelete param

사용 사례°5: **이미 배포된 최대 가용량 구성 업데이트**

1. list
1. get
1. update
1. undeploy
1. candeploy
1. deploy
