---
solution: Journey Optimizer
product: journey optimizer
title: Marketo Engage와 통합
description: Marketo Engage 작업 사용 방법 알아보기
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate
keywords: marketo, marketo engage 통합
exl-id: 70d1ef5a-743b-4362-bb65-93a8c996209f
source-git-commit: 844c0f8dc9b14d69cbd87893042f048443d7a5e6
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 4%

---

# Marketo Engage와 통합 {#integrating-with-marketo-engage}

Marketo Engage과의 원활한 데이터 통합 여정을 시작하십시오. Journey Optimizer의 이 특정 사용자 지정 작업은 두 가지 주요 데이터 유형 수집을 지원합니다.

* 사람(프로필): Marketo은 프로필을 실행 가능한 인사이트로 변환합니다.
* 사용자 지정 개체: 개인화된 마케팅 접근 방식을 위해 제품과 같은 사용자 지정 개체로 데이터를 사용자 지정합니다.

## 전제 조건 {#prerequisites}

* Marketo Engage의 고객 인스턴스는 IMS를 사용할 수 있어야 합니다.
* Marketo Engage 인스턴스와 Adobe Experience Platform/Journey Optimizer 인스턴스가 동일한 조직에 있어야 합니다.
* 고객은 **MktoSync: 수집 서비스 액세스**(으)로 프로비저닝되어야 합니다.

## 작업 구성 {#configure-marketo-action}

* 관리 > 구성 > 작업 으로 이동한 다음 관리 를 클릭합니다
* 작업 목록에서 작업 생성을 누릅니다. [사용자 지정 작업](../building-journeys/using-custom-actions.md){target="_blank"}에 대해 자세히 알아보세요.
* 이름, 설명을 입력하고 작업 유형으로 Adobe Marketo Engage 를 선택합니다.

![](assets/engage-customaction-creation.png){width="40%" align="left"}

* **요청** 및 **응답** 페이로드에 대한 페이로드 편집을 클릭합니다.
* 두 경우 모두 페이로드를 구성하고 전용 팝업에 붙여 넣습니다.

![](assets/engage-customaction-payload.png){width="70%" align="left"}

* Inspect 및 페이로드 값 구성
참고: 값을 동적으로 전달하려면 각 필드에 대해 **상수**&#x200B;를 **변수**(으)로 변경하십시오.

![](assets/engage-customaction-payload-fields.png){width="70%" align="left"}

* 필드 구성 창에서 **저장**&#x200B;을 클릭한 다음 사용자 지정 작업에 대해 **저장**&#x200B;을 클릭합니다.

이제 전용 캔버스에서 사용자 지정 작업을 사용할 수 있습니다.


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

* 사용자 지정 작업을 여정 캔버스로 드래그합니다.
* **요청 매개 변수** 섹션에서 페이로드에 구성한 동적 값이 있는 각 매개 변수에 대해 [편집]을 클릭합니다.

![](assets/engage-use-canvas.png){width="70%" align="left"}
