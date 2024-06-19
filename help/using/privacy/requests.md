---
solution: Journey Optimizer
product: journey optimizer
title: 개인 정보 보호 요청
description: 개인 정보 보호 요청 및 Privacy Service에 대해 자세히 알아보십시오.
feature: Privacy
role: User
level: Intermediate
exl-id: 19ec3410-761e-4a9c-a277-f105fc446d7a
source-git-commit: 41717213cb75185476f054bd076e67f942be0f1c
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 23%

---

# 개인 정보 보호 요청 {#track-changes}

Adobe Experience Platform **Privacy Service**&#x200B;는 고객 데이터 요청을 관리하는 데 도움이 되는 RESTful API 및 사용자 인터페이스를 제공합니다. Privacy Service를 사용하면 Adobe Experience Cloud 애플리케이션에서 개인 고객 데이터에 액세스하고 삭제하도록 요청할 수 있으므로, 법적 및 조직의 개인 정보 보호 규정을 자동으로 준수할 수 있습니다.

개인 정보 보호 요청은 **[!UICONTROL 요청]** 메뉴에서 생성하고 관리할 수 있습니다.

![](assets/requests.png)

Privacy Service 및 개인 정보 보호 요청을 만들고 관리하는 방법에 대한 자세한 내용은 Adobe Experience Platform 설명서를 참조하십시오.

* [Privacy Service 개요](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=ko)
* [Privacy Service UI에서 개인 정보 작업 관리](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=ko)



## Adobe Journey Optimizer에 보낼 수 있는 개별 데이터 개인 정보 보호 요청 관리 {#data-privacy-requests}

다음 두 가지 방법으로 Adobe Journey Optimizer에서 소비자 데이터에 액세스하고 삭제하기 위한 개별 요청을 제출할 수 있습니다.

* 다음을 통해 **PRIVACY SERVICE UI**. 설명서 참조 [여기](https://experienceleague.adobe.com/en/docs/experience-platform/privacy/ui/user-guide#_blank).
* 다음을 통해 **PRIVACY SERVICE API**. 설명서 참조 [여기](https://developer.adobe.com/experience-platform-apis/references/privacy-service/#_blank) 및 API 정보 [여기](https://developer.adobe.com/experience-platform-apis/#_blank).

이 Privacy Service은 두 가지 유형의 요청을 지원합니다. **데이터 액세스** 및 **데이터 삭제**.

>[!NOTE]
>
>이 안내서에서는 Adobe Journey Optimizer에 대한 개인 정보 보호 요청을 하는 방법만 다룹니다. Platform 데이터 레이크에 대한 개인 정보 보호 요청도 수행할 계획이라면 다음을 참조하십시오. [안내서](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/privacy) 이 튜토리얼 외에. 실시간 고객 프로필의 경우 다음을 참조하십시오. [안내서](https://experienceleague.adobe.com/en/docs/experience-platform/profile/privacy) 및 ID 서비스의 경우 다음을 참조하십시오. [안내서](https://experienceleague.adobe.com/en/docs/experience-platform/identity/privacy). 삭제 및 액세스 요청의 경우 이러한 개별 시스템을 호출하여 요청이 각 시스템에 의해 처리되는지 확인해야 합니다. Adobe Journey Optimizer에 개인 정보 보호 요청을 해도 이러한 모든 시스템에서 데이터가 제거되지는 않습니다.

대상 **액세스 요청**&#x200B;에서 UI의 &quot;Adobe Journey Optimizer&quot;(또는 CJM&quot;을 API의 제품 코드로 지정)를 지정합니다.

대상 **요청 삭제**, &quot;Adobe Journey Optimizer&quot; 요청 외에도 Journey Optimizer에서 삭제된 데이터를 다시 거부하지 않도록 3개의 업스트림 서비스에 삭제 요청을 제출해야 합니다. 이러한 업스트림 서비스를 지정하지 않으면 업스트림 서비스에 대한 삭제 요청이 생성될 때까지 &quot;Adobe Journey Optimizer&quot; 요청은 &quot;처리&quot; 상태로 유지됩니다.

세 개의 업스트림 서비스는 다음과 같습니다.

* 프로필(제품 코드: &quot;profileService&quot;)
* AEP 데이터 레이크(제품 코드: &quot;AdobeCloudPlatform&quot;)
* ID(제품 코드: &quot;id&quot;)

## 액세스 및 삭제 요청을 만드는 방법

### 전제 조건

Adobe Journey Optimizer에 대한 데이터 액세스 및 삭제를 요청하려면 다음 권한이 있어야 합니다.

* ims 조직 ID
* 작업을 수행할 사람의 ID 식별자와 해당 네임스페이스입니다. Adobe Journey Optimizer 및 Experience Platform의 ID 네임스페이스에 대한 자세한 내용은 [id 네임스페이스 개요](https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/namespaces).

### API 요청에 대한 Adobe Journey Optimizer의 필수 필드 값

```json
"companyContexts":
    "namespace": imsOrgID
    "value": <Your IMS Org ID Value>

"users":
    "action": either access or delete

    "userIDs":
        "namespace": e.g. email, aaid, ecid, etc.
        "type": standard
        "value": <Data Subject's Identity Identifier>

"include":
    CJM (which is the Adobe product code for Adobe Journey Optimizer)
    profileService (product code for Profile)
    AdobeCloudPlatform (product code for AEP Data Lake)
    identity (product code for Identity)

"regulation":
    gdpr, ccpa, pdpa, lgpd_bra, or nzpa_nzl (which is the privacy regulation that applies to the request)
```


### GDPR 액세스 요청 예:

UI에서:

![](assets/accessrequest.png)

API를 통해:

```json
// JSON Request
{
   "companyContexts":[
      {
         "namespace":"imsOrgID",
         "value":"745F37C35E4B776E0A49421B@AdobeOrg"
      }
   ],
   "users":[
      {
         "action":[
            "access"
         ],
         "userIDs":[
            {
               "namespace":"ecid",
               "value":"38400000-8cf0-11bd-b23e-10b96e40000d",
               "type":"standard"
            },
            {
               "namespace":"email",
               "value":"johndoe4@gmail.com",
               "type":"standard"
            }
         ]
      }
   ],
   "include":[
      "CJM"
   ],
   "regulation":"gdpr"
}
```

```json
// JSON Response
{
    "requestId": "17163122360480365RX-705",
    "totalRecords": 1,
    "jobs": [
        {
            "jobId": "e709b1f4-1796-11ef-b422-eddd0aebc40d",
            "customer": {
                "user": {
                    "key": "John Doe",
                    "action": [
                        "access"
                    ],
                    "userIDs": [
                        {
                            "namespace": "ecid",
                            "value": "38400000-8cf0-11bd-b23e-10b96e40000d",
                            "type": "standard",
                            "namespaceId": 4,
                            "isDeletedClientSide": false
                        },
                        {
                            "namespace": "email",
                            "value": "johndoe4@gmail.com",
                            "type": "standard",
                            "namespaceId": 6,
                            "isDeletedClientSide": false
                        }
                    ]
                }
            }
        }
    ]
}
```

### GDPR 삭제 요청 예:

UI에서:

![](assets/deleterequest.png)

API를 통해:

```json
// JSON Request
{
  "companyContexts": [
    {
      "namespace": "imsOrgID",
      "value": "745F37C35E4B776E0A49421B@AdobeOrg"
    }
  ],
  "users": [
    {
      "action": [
          "delete"
      ],
      "userIDs": [
        {
          "namespace": "ecid",
          "value": "38400000-8cf0-11bd-b23e-10b96e40000d",
          "type": "standard"
        },
                {
          "namespace": "email",
          "value": "johndoe4@gmail.com",
          "type": "standard"
        }
      ]
    }
  ],
  "include": [
    "CJM", "profileService", "AdobeCloudPlatform", "identity"
  ],
  "regulation": "gdpr"
}
```

```json
// JSON Response
{
    "requestId": "17163122360480365RX-705",
    "totalRecords": 1,
    "jobs": [
        {
            "jobId": "e709b1f4-1796-11ef-b422-eddd0aebc40d",
            "customer": {
                "user": {
                    "key": "John Doe",
                    "action": [
                        "delete"
                    ],
                    "userIDs": [
                        {
                            "namespace": "ecid",
                            "value": "38400000-8cf0-11bd-b23e-10b96e40000d",
                            "type": "standard",
                            "namespaceId": 4,
                            "isDeletedClientSide": false
                        },
                        {
                            "namespace": "email",
                            "value": "johndoe4@gmail.com",
                            "type": "standard",
                            "namespaceId": 6,
                            "isDeletedClientSide": false
                        }
                    ]
                }
            }
        }
    ]
}
```
