---
solution: Journey Optimizer
product: journey optimizer
title: 컬렉션 관리 기능
description: 컬렉션 관리 기능의 데이터 유형에 대해 알아봅니다
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: 쿼리, 컬렉션, 함수, 페이로드, 여정
exl-id: 09b38179-9ace-4921-985b-ddd17eb64681
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 3%

---

# 컬렉션 관리 기능 {#collection-management-functions}


## 쿼리 컬렉션 함수 기본 정보

표현식 언어에서는 컬렉션을 쿼리하기 위한 함수 집합도 소개합니다. 이러한 기능은 아래에 설명되어 있습니다.

다음 예제에서는 컬렉션을 포함하는 이벤트 페이로드를 사용하겠습니다.

```json
                { 
   "_experience":{ 
      "campaign":{ 
         "message":{ 
            "profile":{ 
               "pushNotificationTokens":[ 
                  { 
                     "token":"token_1",
                     "application":{ 
                        "_id":"APP1",
                        "name":"MarltonMobileApp",
                        "version":"1.0"
                     }
                  },
                  { 
                     "token":"token_2",
                     "application":{ 
                        "_id":"APP2",
                        "name":"MarketplaceApp",
                        "version":"1.0"
                     }
                  },
                  { 
                     "token":"token_3",
                     "application":{ 
                        "_id":"APP3",
                        "name":"VendorApp",
                        "version":"2.0"
                     }
                  }
               ]
            }
         }
      }
   },
   "timestamp":"1536160728"
}
```

## all(`<condition>`) 함수

**[!UICONTROL all]** 함수를 사용하면 부울 식을 사용하여 주어진 컬렉션에서 필터를 정의할 수 있습니다.

```json
<listExpression>.all(<condition>)
```

예를 들어 모든 앱 사용자 중에서 IOS 13(부울 표현식 &quot;IOS 13== 사용된 앱&quot;)을 사용하여 앱 사용자를 가져올 수 있습니다. 이 함수의 결과는 부울 표현식(예: 앱 사용자 1, 앱 사용자 34, 앱 사용자 432)과 일치하는 항목을 포함하는 필터링된 목록입니다.

Data Source 조건 활동에서 **[!UICONTROL all]** 함수의 결과가 null인지 여부를 확인할 수 있습니다. 이 **[!UICONTROL all]** 함수를 **[!UICONTROL count]**&#x200B;와 같은 다른 함수와 결합할 수도 있습니다. 자세한 내용은 [데이터 Source 조건 활동](../condition-activity.md#data_source_condition)을 참조하세요.


>[!CAUTION]
>
>여정 표현식/조건에서는 경험 이벤트를 사용할 수 없습니다. 사용 사례에서 경험 이벤트를 사용해야 하는 경우 대체 방법을 고려하십시오. [자세히 알아보기](../exp-event-lookup.md)

### 예제 1

사용자가 특정 버전의 애플리케이션을 설치했는지 확인하려고 합니다. 이를 위해 버전이 1.0인 모바일 애플리케이션과 연결된 모든 푸시 알림 토큰을 가져옵니다. 그런 다음 **[!UICONTROL count]** 함수로 조건을 수행하여 반환된 토큰 목록에 하나 이상의 요소가 포함되어 있는지 확인합니다.

```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all(currentEventField.application.version == "1.0").token}) > 0
```

결과는 true입니다.

### 예제 2

여기에서는 **[!UICONTROL count]** 함수를 사용하여 컬렉션에 푸시 알림 토큰이 있는지 확인합니다.

```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().token}) > 0
```


결과는 true입니다.


```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.token})
```

식의 결과는 **3**&#x200B;입니다.


>[!NOTE]
>
>* **all()** 함수의 필터링 조건이 비어 있으면 필터가 목록에 있는 모든 요소를 반환합니다. **그러나 컬렉션의 요소 수를 계산하려면 all 함수가 필요하지 않습니다.
>
>* `currentEventField`은(는) 이벤트 컬렉션을 조작할 때만 사용할 수 있으며, `currentDataPackField`은(는) 데이터 소스 컬렉션을 조작할 때 사용할 수 있고 `currentActionField`은(는) 사용자 지정 작업 응답 컬렉션을 조작할 때만 사용할 수 있습니다.
>
>  `all`, `first` 및 `last`(으)로 컬렉션을 처리할 때 컬렉션의 각 요소를 하나씩 반복합니다. `currentEventField`, `currentDataPackField` 및 `currentActionField`은(는) 루프가 적용되는 요소에 해당합니다.


## 첫 번째(`<condition>`) 및 마지막(`<condition>`) 함수

**[!UICONTROL first]** 및 **[!UICONTROL last]** 함수는 필터를 충족하는 목록의 첫 번째/마지막 요소를 반환하면서 컬렉션에서 필터를 정의할 수도 있습니다.

_`<listExpression>.first(<condition>)`_

_`<listExpression>.last(<condition>)`_

### 예제 1

이 표현식은 버전이 1.0인 모바일 애플리케이션과 연결된 첫 번째 푸시 알림 토큰을 반환합니다.


```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.first(currentEventField.application.version == "1.0").token}
```

결과는 `token_1`입니다.

### 예제 2

이 표현식은 버전이 1.0인 모바일 애플리케이션과 연결된 마지막 푸시 알림 토큰을 반환합니다.


```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.last(currentEventField.application.version == "1.0").token}
```

결과는 `token_2`입니다.

## at(`<index>`) 함수

**[!UICONTROL at]** 함수를 사용하면 색인에 따라 컬렉션의 특정 요소를 참조할 수 있습니다.
색인 0은 컬렉션의 첫 번째 색인입니다.

_`<listExpression>`.at(`<index>`)_

### 예

이 표현식은 목록의 두 번째 푸시 알림 토큰을 반환합니다.


```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.at(1).token}`
```

결과는 `token_2`입니다.