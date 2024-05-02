---
solution: Journey Optimizer
product: journey optimizer
title: 사용자 지정 작업을 사용하여 AEP에서 여정 이벤트 작성
description: 사용자 지정 작업을 사용하여 AEP에서 여정 이벤트 작성
feature: Journeys, Use Cases, Custom Actions
topic: Content Management
role: Developer, Data Engineer
level: Experienced
source-git-commit: 0571a11eabffeb5e318bebe341a8df18da7db598
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 0%

---


# 사용 사례: 사용자 지정 작업을 사용하여 Experience Platform에 여정 이벤트 작성{#custom-action-aep}

이 사용 사례에서는 사용자 지정 작업 및 인증된 호출을 사용하여 여정에서 Adobe Experience Platform에 사용자 지정 이벤트를 작성하는 방법을 설명합니다.

## IO 프로젝트 구성

1. Adobe Developer 콘솔에서 **프로젝트** IO 프로젝트를 여십시오.

1. 다음에서 **자격 증명** 섹션, 클릭 **OAuth 서버 간**.

   ![](assets/custom-action-aep-1.png)

1. 클릭 **cURL 보기 명령**.

   ![](assets/custom-action-aep-2.png)

1. cURL 명령을 복사하고 client_id, client_secret, grant_type 및 범위를 저장합니다.

```
curl -X POST 'https://ims-na1.adobelogin.com/ims/token/v3' -H 'Content-Type: application/x-www-form-urlencoded' -d 'grant_type=client_credentials&client_id=1234&client_secret=5678&scope=openid,AdobeID,read_organizations,additional_info.projectedProductContext,session'
```

## HTTP API Inlet을 사용하여 소스 구성

1. Adobe Experience Platform에서 엔드포인트를 만들어 여정에서 데이터를 기록합니다.

1. Adobe Experience Platform에서 **소스**, 아래 **연결** 왼쪽 메뉴에서 을 클릭합니다. 아래 **HTTP API**, 클릭 **데이터 추가**.

   ![](assets/custom-action-aep-3.png)

1. 선택 **새 계정** 인증을 활성화하십시오. 클릭 **소스에 연결**.

   ![](assets/custom-action-aep-4.png)

1. 클릭 **다음** 데이터를 쓸 데이터 세트를 선택합니다. 클릭 **다음** 및 **완료**.

   ![](assets/custom-action-aep-5.png)

1. 새로 생성된 데이터 흐름을 엽니다. 스키마 페이로드를 복사하여 메모장에 저장합니다.

```
{
"header": {
"schemaRef": {
"id": "https://ns.adobe.com/<your_org>/schemas/<schema_id>",
"contentType": "application/vnd.adobe.xed-full+json;version=1.0"
},
"imsOrgId": "<org_id>",
"datasetId": "<dataset_id>",
"source": {
"name": "Custom Journey Events"
}
},
"body": {
"xdmMeta": {
"schemaRef": {
"id": "https://ns.adobe.com/<your_org>/schemas/<schema_id>",
"contentType": "application/vnd.adobe.xed-full+json;version=1.0"
}
},
"xdmEntity": {
"_id": "test1",
"<your_org>": {
"journeyVersionId": "",
"nodeId": "", "customer_Id":""
},
"eventMergeId": "",
"eventType": "",
"producedBy": "self",
"timestamp": "2018-11-12T20:20:39+00:00"
}
}
}
```

## 사용자 지정 작업 구성

1. Adobe Journey Optimizer을 열고 **구성**, 아래 **관리** 왼쪽 메뉴에서 을 클릭합니다. 아래 **작업**, 클릭 **관리** 및 클릭 **작업 만들기**.

1. URL을 설정하고 Post 메서드를 선택합니다.

   `https://dcs.adobedc.net/collection/<collection_id>?syncValidation=false`

1. 헤더(Content-Type, Charset, sandbox-name)가 구성되어 있는지 확인합니다.

   ![](assets/custom-action-aep-7bis.png)

### 인증 설정

1. 다음 항목 선택 **유형** 다음으로: **사용자 정의** 다음 페이로드와 함께 사용됩니다.

1. (이전에 사용한 IO 프로젝트 페이로드에서) client_secret, client_id, scope 및 grant_type을 붙여넣습니다.

   ```
   {
   "type": "customAuthorization",
   "authorizationType": "Bearer",
   "endpoint": "https://ims-na1.adobelogin.com/ims/token/v3",
   "method": "POST",
   "headers": {},
   "body": {
   "bodyType": "form",
   "bodyParams": {
   "grant_type": "client_credentials",
   "client_secret": "********",
   "client_id": "<client_id>",
   "scope": "openid,AdobeID,read_organizations,additional_info.projectedProductContext,session"
   }
   },
   "tokenInResponse": "json://access_token",
   "cacheDuration": {
   "duration": 28000,
   "timeUnit": "seconds"
   }
   }
   ```

1. 사용 **클릭하여 인증 테스트** 단추를 클릭하여 연결을 테스트합니다.

   ![](assets/custom-action-aep-8.png)

### 페이로드 설정

1. 다음에서 **요청** 및 **응답** 필드에 이전에 사용한 소스 연결의 페이로드를 붙여 넣습니다.

   ```
   {
   "xdmMeta": {
   "schemaRef": {
   "id": "https://ns.adobe.com/<your_org>/schemas/<schema_id>",
   "contentType": "application/vnd.adobe.xed-full+json;version=1.0"
   }
   },
   "xdmEntity": {
   "_id": "/uri-reference",
   "<your_org>": {
   "journeyVersionId": "Sample value",
   "nodeId": "Sample value",
   "customer_Id":""
   },
   "eventMergeId": "Sample value",
   "eventType": "advertising.completes,
   "producedBy": "self",
   "timestamp": "2018-11-12T20:20:39+00:00"
   }
   }
   ```

1. 다음에서 필드 구성 변경 **상수** 끝 **변수** 동적으로 채워지는 필드용입니다. 사용자 지정 작업을 저장합니다.

## 여정

1. 마지막으로 여정에서 이 사용자 지정 작업을 사용하여 사용자 지정 여정 이벤트를 작성합니다.

1. 사용 사례에 따라 여정 버전 ID, 노드 ID, 노드 이름 및 기타 속성을 채웁니다.

   ![](assets/custom-action-aep-9.png)


