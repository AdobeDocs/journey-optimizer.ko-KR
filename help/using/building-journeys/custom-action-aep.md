---
solution: Journey Optimizer
product: journey optimizer
title: 사용자 지정 작업을 사용하여 AEP에서 여정 이벤트 작성
description: 사용자 지정 작업을 사용하여 AEP에서 여정 이벤트 작성
feature: Journeys, Use Cases, Custom Actions
topic: Content Management
role: Developer, Data Engineer
level: Experienced
exl-id: 890a194f-f54d-4230-863a-fb2b924d716a
source-git-commit: f00b157ec843eacdee480dcfe00a8724ab4a3495
workflow-type: tm+mt
source-wordcount: '369'
ht-degree: 0%

---

# 사용 사례: 사용자 지정 작업을 사용하여 Experience Platform에 여정 이벤트 작성 {#custom-action-aep}

이 사용 사례에서는 사용자 지정 작업 및 인증된 호출을 사용하여 여정에서 Adobe Experience Platform에 사용자 지정 이벤트를 작성하는 방법을 설명합니다.

## IO 프로젝트 구성 {#custom-action-aep-IO}

1. Adobe Developer Console에서 **프로젝트**&#x200B;를 클릭하고 IO 프로젝트를 엽니다.

1. **자격 증명** 섹션에서 **OAuth 서버 간**&#x200B;을(를) 클릭합니다.

   ![](assets/custom-action-aep-1.png)

1. **cURL 명령 보기**&#x200B;를 클릭합니다.

   ![](assets/custom-action-aep-2.png)

1. cURL 명령을 복사하고 client_id, client_secret, grant_type 및 범위를 저장합니다.

```
curl -X POST 'https://ims-na1.adobelogin.com/ims/token/v3' -H 'Content-Type: application/x-www-form-urlencoded' -d 'grant_type=client_credentials&client_id=1234&client_secret=5678&scope=openid,AdobeID,read_organizations,additional_info.projectedProductContext,session'
```

>[!CAUTION]
>
>Adobe Developer Console에서 프로젝트를 작성한 후 올바른 권한을 사용하여 개발자 및 API 액세스 제어를 부여해야 합니다. 자세한 내용은 [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/en/docs/experience-platform/landing/platform-apis/api-authentication#grant-developer-and-api-access-control){target="_blank"}를 참조하세요

## HTTP API Inlet을 사용하여 Source 구성

1. Adobe Experience Platform에서 엔드포인트를 만들어 여정에서 데이터를 기록합니다.

1. Adobe Experience Platform의 왼쪽 메뉴에서 **연결** 아래의 **원본**&#x200B;을 클릭합니다. **HTTP API**&#x200B;에서 **데이터 추가**&#x200B;를 클릭합니다.

   ![](assets/custom-action-aep-3.png)

1. **새 계정**&#x200B;을 선택하고 인증을 사용하도록 설정합니다. **Source에 연결**&#x200B;을 클릭합니다.

   ![](assets/custom-action-aep-4.png)

1. **다음**&#x200B;을 클릭하고 데이터를 쓸 데이터 집합을 선택하십시오. **다음** 및 **마침**&#x200B;을 클릭합니다.

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

## 사용자 지정 작업 구성 {#custom-action-config}

사용자 지정 작업 구성은 [이 페이지](../action/about-custom-action-configuration.md)에 자세히 설명되어 있습니다.

이 예제의 경우 다음 단계를 수행합니다.

1. Adobe Journey Optimizer을 열고 왼쪽 메뉴에서 **관리** 아래의 **구성**&#x200B;을 클릭합니다. **작업**&#x200B;에서 **관리**&#x200B;를 클릭하고 **작업 만들기**&#x200B;를 클릭합니다.

1. URL을 설정하고 Post 메서드를 선택합니다.

   `https://dcs.adobedc.net/collection/<collection_id>?syncValidation=false`

1. 헤더(Content-Type, Charset, sandbox-name)가 구성되어 있는지 확인합니다.

   ![](assets/custom-action-aep-7bis.png)

### 인증 설정 {#custom-action-aep-authentication}

1. 다음 페이로드를 사용하여 **Type**&#x200B;을(를) **Custom**(으)로 선택하십시오.

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

1. **인증을 테스트하려면 클릭** 단추를 사용하여 연결을 테스트하십시오.

   ![](assets/custom-action-aep-8.png)

### 페이로드 설정 {#custom-action-aep-payload}

1. **요청** 및 **응답** 필드에 이전에 사용한 원본 연결에서 페이로드를 붙여 넣으십시오.

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

1. 동적으로 채워질 필드에 대한 필드 구성을 **상수**&#x200B;에서 **변수**(으)로 변경합니다.

1. 사용자 지정 작업을 저장합니다.

## 여정

1. 마지막으로 여정에서 이 사용자 지정 작업을 사용하여 사용자 지정 여정 이벤트를 작성합니다.

1. 사용 사례에 따라 여정 버전 ID, 노드 ID, 노드 이름 및 기타 속성을 채웁니다.

   ![](assets/custom-action-aep-9.png)
