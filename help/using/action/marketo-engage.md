---
solution: Journey Optimizer
product: journey optimizer
title: Marketo Engage와 통합
description: Marketo Engage 작업 사용 방법 알아보기
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Developer, Admin
level: Intermediate
keywords: marketo, marketo engage 통합
exl-id: 70d1ef5a-743b-4362-bb65-93a8c996209f
TQID: https://experienceleague.adobe.com/-aRINahKmp9bI1tyW-XA-LzZOFeoEPXpWoH8JydG6Rk
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: bb359667-ec7d-4d4b-8663-5850fc219d32id: d556b755-390a-43f0-be32-a08cf6236126id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: c2beecbb-b93e-4ae3-baa9-72adcdc06781
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: df401a2a-327d-468c-a5e4-b7b7ccd071a0id: e1e0219c-f879-479f-8427-888ed2a6e9c2id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 326
ht-degree: 3%

---

# Marketo Engage와 통합 {#integrating-with-marketo-engage}

Marketo Engage과의 원활한 데이터 통합 여정을 시작하십시오. Adobe Journey Optimizer과 Marketo Engage을 통합하는 여정에서 특정 사용자 지정 작업을 사용할 수 있습니다. 이 사용자 지정 작업은 두 가지 주요 데이터 유형의 수집을 지원합니다.

* **사용자**(프로필): Marketo은 프로필을 실행 가능한 인사이트로 변환합니다.
* **사용자 지정 개체**: 개인화된 마케팅 접근 방식을 위해 제품과 같은 사용자 지정 개체로 데이터를 사용자 지정합니다.

## 전제 조건 {#prerequisites}

이 통합에는 다음 사전 요구 사항이 적용됩니다.

* Marketo Engage의 고객 인스턴스는 IMS를 사용할 수 있어야 합니다
* Marketo Engage 인스턴스 및 Adobe Experience Platform/Journey Optimizer 인스턴스는 동일한 조직에 있어야 합니다
* 고객은 **MktoSync: 수집 서비스 액세스**(으)로 프로비저닝되어야 합니다.

## 작업 구성 {#configure-marketo-action}


Journey Optimizer에서 Marketo Engage에 대한 사용자 지정 작업을 구성해야 합니다. 다음 단계를 수행하십시오.

1. 관리 메뉴 섹션에서 **[!UICONTROL 구성]**&#x200B;을(를) 선택합니다.
1. **[!UICONTROL 작업]** 섹션에서 **[!UICONTROL 작업 만들기]**&#x200B;를 클릭합니다. 작업 구성 창이 화면 오른쪽에 열립니다.
1. 이름, 설명을 입력하고 **Adobe Marketo Engage**&#x200B;을(를) **작업 유형으로 선택하십시오.**
   ![](assets/engage-customaction-creation.png){width="40%" align="left"}
1. **요청** 및 **응답** 페이로드에 대한 **페이로드 편집** 아이콘을 클릭합니다.
1. 두 경우 모두 페이로드를 구성하고 전용 팝업에 붙여 넣습니다.
   ![](assets/engage-customaction-payload.png){width="70%" align="left"}
1. 페이로드 값 검사 및 구성

   참고: 값을 동적으로 전달하려면 각 필드에 대해 **상수**&#x200B;를 **변수**(으)로 변경하십시오.

   ![](assets/engage-customaction-payload-fields.png){width="70%" align="left"}

1. 필드 구성 화면에서 **저장**&#x200B;을 클릭한 다음 사용자 지정 작업을 **저장**&#x200B;합니다.

이제 여정 캔버스에서 사용자 지정 작업을 사용할 수 있습니다.

## 페이로드 구문 {#payload-syntax}

### 개인

![](assets/payload-person.png)

### CustomObject

![](assets/payload-customobject.png)


**개인용 페이로드 예**

```json
{
   "munchkinID": "388-KKG-245",  
   "person": {
    "priority": "normal",
    "partitionName": "XYZ",
    "dedupeFields": {
      "field1": "email",
      "field2": "firstName"
    },
    "objects": [
      {
        "email": "Email address",
        "firstName": "First name",
        "lastName": "Last name"
      }
    ]
  }
}
```

**사용자 지정 개체에 대한 페이로드 예**

```json
{
  "munchkinID": "388-KKG-245", 
  "customObject": {
    "priority": "normal",
    "objectName": "products",
    "objects": [
      {
        "email": "Email Address",
        "productName": "Product Name",
        "productQty": "Product Quantity",
        "priceTotal": "Price Total"
      }
    ]
  }
}
```


## 작업 사용 {#engage-using}

구성된 각 작업에 대해 여정 디자이너 팔레트에서 Marketo Engage 작업 활동을 사용할 수 있습니다.

사용하려면 다음 단계를 따르십시오.

1. 사용자 지정 작업을 여정 캔버스로 드래그합니다.

1. 이 작업의 레이블과 설명을 입력합니다.

1. **요청 매개 변수** 섹션에서 각 매개 변수에 대한 **편집** 아이콘을 클릭하고 페이로드에 구성한 동적 값을 선택합니다.

![](assets/engage-use-canvas.png){width="70%" align="left"}
