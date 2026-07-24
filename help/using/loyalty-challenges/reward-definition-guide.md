---
solution: Journey Optimizer
product: journey optimizer
title: 보상 정의 안내서
description: Adobe Journey Optimizer에서 충성도 과제 보상 제공자에 대한 보상 정의를 구성하는 방법을 알아봅니다.
feature: Journeys
topic: Content Management
role: Admin
level: Intermediate
hide: true
badge: label="비공개 베타" type="Informative"
mini-toc-levels: 1
exl-id: 9b0fd9d8-18d1-4a51-8b6f-b2e2a4c6f1d7
feature_v2: []
subfeature_v2: []
source-git-commit: 00c24e9b97b4f6597048731858f3bfbcb39a0030
workflow-type: tm+mt
source-wordcount: 1206
ht-degree: 5%

---

# 보상 정의 안내서 {#reward-definition-guide}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_reward_definition"
>title="보상 정의 안내서"
>abstract="이 안내서를 사용하여 기본 정의 동작 및 이행 페이로드 필드를 포함한 보상 정의를 충성도 보상 제공자를 위해 구성할 수 있습니다."

>[!BEGINSHADEBOX]

**목차**

[충성도 문제 시작](get-started.md)

<table style="table-layout:fixed">
<tr style="border: 0;">
<td style="vertical-align:top;">

**문제 만들기 및 관리**

* [과제 및 작업 액세스 및 관리](access-loyalty-challenges.md)
* [과제 만들기](create-challenges.md)
* [작업 만들기](create-tasks.md)
* [충성도 과제 성능 모니터링](loyalty-reporting.md)

</td>
<td style="vertical-align:top;">

**구성 및 통합**

* [충성도 문제 구성](loyalty-admin.md)
* **보상 정의 가이드** ◀︎ **여기 있습니다**
* [이벤트 변환기 안내서](event-transformer-guide.md)
* [충성도 데이터 및 데이터 세트](loyalty-data-and-datasets.md)
* [충성도 과제 API 참조](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

</td>
</tr>
</table>

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>이 기능은 현재 **개인 베타**&#x200B;에 있습니다. [!DNL Journey Optimizer]의 릴리스 주기 및 가용성 단계에 대한 자세한 내용은 [릴리스 주기](../rn/releases.md)를 참조하십시오.

시도 작업, 마일스톤 또는 시도가 **을(를) 완료하고 보상 값이 구성되어**&#x200B;있으면 플랫폼에서 JSON 페이로드로 보상 공급자의 HTTP 끝점을 호출하여 보상을 발행합니다. **보상 정의**&#x200B;는 어떤 보상을 발행하는지 설명하고 공급자가 기대하는 정확한 페이로드를 형성하는 [JSONata](https://docs.jsonata.org/overview) 표현식(`rewardJsonata`)을 제공합니다.

이 안내서에서는 보상 제공자를 구성하고, 보상 정의를 만들고, `rewardJsonata` 표현식을 작성하고, 평가 시 사용할 수 있는 컨텍스트를 이해하는 방법에 대해 설명합니다.

## 2단계 모델

보상은 두 가지 수준으로 구성됩니다.

```
Reward Provider  (endpoint, auth, headers)
└── Reward Definition  (denomination, rewardJsonata)
└── Reward Definition
└── ...
```

**보상 공급자**&#x200B;는 게재 끝점 URL, 인증 및 사용자 지정 HTTP 헤더를 보유하는 단일 외부 보상 시스템을 나타냅니다. 한 공급자는 여러 **보상 정의**&#x200B;를 보유할 수 있으며, 각 공급자는 해당 공급자가 제공하는 고유한 보상 유형 또는 분모(예: &quot;50성&quot;, &quot;이중성&quot;, &quot;무료 항목&quot;)를 설명합니다.

과제는 공급자와 GUID에 의한 정의를 참조합니다. 보상이 발행되면 플랫폼은 정의의 `rewardJsonata` 식을 평가하고 결과를 공급자의 끝점에 게시합니다.

## 보상 제공자 및 정의 필드

+++보상 제공자 필드

<table>
<colgroup>
<col style="width:160px">
<col style="width:80px">
<col style="width:160px">
<col>
</colgroup>
<tr><th>필드</th><th>유형</th><th>필수 여부</th><th>설명</th></tr>
<tr><td><code>guid</code></td><td><code>String</code></td><td>아니요(시스템 지정)</td><td>고유 식별자. 읽기 전용.</td></tr>
<tr><td><code>name</code></td><td><code>String</code></td><td><strong>예</strong></td><td>조직 내에서 고유한 표시 이름입니다.</td></tr>
<tr><td><code>desc</code></td><td><code>String</code></td><td>아니오</td><td>사람이 인식할 수 있는 공급자에 대한 설명.</td></tr>
<tr><td><code>enabled</code></td><td><code>Boolean</code></td><td>아니오</td><td><code>false</code>일 때 이 공급자의 모든 정의에 대해 보상 배달이 <br>일시 중단됩니다.</td></tr>
<tr><td><code>url</code></td><td><code>String</code></td><td><strong>예</strong></td><td>보상 페이로드를 수신하는 HTTP 엔드포인트.<br>플랫폼이 평가된 <br><code>rewardJsonata</code> 출력을 이 URL에 게시합니다.</td></tr>
<tr><td><code>additionalHeaders</code></td><td><code>Object</code></td><td>아니오</td><td>모든<br>배달 요청에 포함할 사용자 지정 HTTP 헤더(예: API 키,<br>콘텐츠 유형 재정의).</td></tr>
<tr><td><code>maxRatePerSecond</code></td><td><code>Integer</code></td><td>아니오</td><td>공급자당 속도 제한(옵션)(1-5000).<br>Null은 무제한을 의미합니다.</td></tr>
<tr><td><code>enableMTLS</code></td><td><code>Boolean</code></td><td>아니오</td><td>끝점에 상호 TLS가 필요한지 여부입니다.</td></tr>
</table>

+++

+++보상 정의 필드

<table>
<colgroup>
<col style="width:160px">
<col style="width:80px">
<col style="width:160px">
<col>
</colgroup>
<tr><th>필드</th><th>유형</th><th>필수 여부</th><th>설명</th></tr>
<tr><td><code>guid</code></td><td><code>String</code></td><td>아니요(시스템 지정)</td><td>고유 식별자. 읽기 전용.</td></tr>
<tr><td><code>name</code></td><td><code>String</code></td><td><strong>예</strong></td><td>공급자 내에서 고유한 표시 이름입니다.</td></tr>
<tr><td><code>denomination</code></td><td><code>String</code></td><td>아니오</td><td><br> 표시에 사용되고 <br><code>reward.denomination</code><br>(예: <code>"Stars"</code>, <code>"Points"</code>, <code>"Miles"</code>) 식에 사용할 수 있는 보상 단위입니다.</td></tr>
<tr><td><code>desc</code></td><td><code>String</code></td><td>아니오</td><td><code>reward.desc</code>(으)로 표현식에서 사용 가능한<br>보상에 대한 설명입니다.</td></tr>
<tr><td><code>enabled</code></td><td><code>Boolean</code></td><td>아니오</td><td><code>false</code>일 때 이 정의는 비활성 상태이며<br>보상을 발행하지 않습니다.</td></tr>
<tr><td><code>isDefault</code></td><td><code>Boolean</code></td><td>아니오</td><td>샌드박스 전체 기본값<br>보상 정의로 표시합니다. 모든 공급자에서 한 번에 하나의 정의<br>만 기본값일 수 있습니다.<br>새 기본값을 설정하면 이전 정의가 지워집니다.<br>게시 시 <br>개인화된 문제에 대한 보상 세부 정보를 자동으로 채우는 데 사용됩니다.</td></tr>
<tr><td><code>rewardJsonata</code></td><td><code>String</code></td><td><strong>예</strong></td><td>JSONata 식이 <br>보상-문제 시간에 평가되었습니다. 전체<br>보상 컨텍스트를 받고 공급자에게 POST에 대한 JSON<br>페이로드를 반환해야 합니다.</td></tr>
</table>

+++

## 보상 컨텍스트

`rewardJsonata`이(가) 평가되면 보상 이벤트에 대해 알려진 모든 내용이 포함된 단일 루트 개체를 받습니다. 표현식의 모든 경로는 이 루트를 기준으로 합니다.

```json
{
  "rewardContext": {
    "rewardValue": "50",
    "source":      "challenge"
  },
  "reward": {
    "name":         "500 Stars",
    "desc":         "Issue 500 Stars to the member",
    "denomination": "Stars",
    "enabled":      true
  },
  "task": { ... },
  "milestone": { ... },
  "challenge": { ... },
  "timestamp": "2026-02-10T00:29:22.538+00:00"
}
```

+++ 컨텍스트 필드

| 필드 | 설명 |
|----------------------------------------|-------------|
| `rewardContext.rewardValue` | 이 발급을 트리거한 문제, 작업 또는 마일스톤에 구성된 보상 값 문자열입니다. |
| `rewardContext.source` | 보상을 트리거한 항목: `"task"`, `"challenge"` 또는 `"milestone"`. |
| `reward` | RewardDefinition 자체 — `name`, `desc`, `denomination`. |
| `task` | `accumulators`, `schedule` 및 `reward`을(를) 포함하여 작업을 완료하는 중입니다. |
| `task.accumulators.spend` | 작업에 의해 누적된 총 적격 지출. |
| `task.accumulators.qty` | 작업에 의해 누적된 총 적격 항목 수입니다. |
| `task.accumulators.item_list` | 작업에 적용되는 모든 적격 항목. 각 항목에는 `item`, `transactionId`, `timestamp`, `utcOffset`, `locationId`이(가) 있습니다. |
| `task.accumulators.item_list[-1]` | 가장 최근에 적용된 항목(JSONata 음성 인덱스)입니다. 마지막 거래 ID 또는 타임스탬프를 소싱하는 데 유용합니다. |
| `task.schedule.currentStreak` | 현재 연속 방문 횟수(연속 도전). |
| `task.schedule.currentVisits` | 총 방문 횟수(방문 챌린지의 경우). |
| `milestone` | 이 보상을 트리거한 마일스톤 또는 마일스톤 보상이 아닌 경우 `null`입니다. `count` 및 `reward.rewardValue`을(를) 포함합니다. |
| `challenge.profileId` | 멤버의 충성도 ID입니다. |
| `challenge.kvpCustom` | 챌린지에 구성된 사용자 지정 키-값 쌍입니다. 캠페인 ID, 제품 이름 또는 공급자별 메타데이터를 전달하는 일반적인 패턴입니다. |
| `challenge.name` | 과제 이름. |
| `challenge._id` | 과제 ID. |
| `timestamp` | 보상 발행의 ISO 8601 타임스탬프. |

+++

## rewardJsonata 표현식 작성

표현식은 보상 컨텍스트를 입력으로 받으며 JSON 개체(공급자의 끝점에 대한 POSTed)를 반환해야 합니다. 해당 객체의 모양은 전적으로 공급자의 API에 따라 결정됩니다. 사용자는 컨텍스트 필드를 공급자가 기대하는 구조에 매핑합니다.

+++단순 고정 페이로드

가장 간단한 경우: 공급자는 컨텍스트에서 알려진 포인트 카운트와 멤버 ID가 필요합니다.

```jsonata
{
  "memberId":   challenge.profileId,
  "points":     $number(rewardContext.rewardValue),
  "currency":   reward.denomination
}
```

**출력:**

```json
{
  "memberId": "ADB-0000030",
  "points":   50,
  "currency": "Stars"
}
```

> `rewardContext.rewardValue`은(는) 항상 문자열입니다. 공급자에 숫자 값이 필요한 경우 `$number()`을(를) 사용하여 변환하십시오.

+++

+++공급자별 메타데이터에 `kvpCustom` 사용

공급자는 각 과제 실행에 고유한 캠페인 ID 또는 소스 시스템 코드와 같은 필드를 필요로 하는 경우가 많습니다. 문제를 작성할 때 이러한 정보를 `challenge.kvpCustom`에 저장한 다음 표현식에서 참조하여 캠페인 간에 표현식을 재사용 가능하게 유지합니다.

```jsonata
{
  "memberId":         challenge.profileId,
  "points":           $number(rewardContext.rewardValue),
  "campaignId":       challenge.kvpCustom.campaignId,
  "transactionSource": "AJO"
}
```

시도별 대신 주어진 보상 형식에 대해 고정된 상수에 `reward.kvpCustom`을(를) 사용할 수도 있습니다.

+++

+++작업 누계 데이터 사용

작업 누계자는 모든 적격 이벤트에 대한 레코드를 보유합니다. `item_list[-1]`을(를) 사용하여 가장 최근에 적용된 항목에 액세스합니다. `transactionId` 및 `timestamp`은(는) 공급자 측의 감사 추적 및 중복 제거에 유용합니다.

```jsonata
{
  "memberId":       challenge.profileId,
  "points":         $number(rewardContext.rewardValue),
  "transactionId":  task.accumulators.item_list[-1].transactionId,
  "transactionDate": task.accumulators.item_list[-1].timestamp
}
```

+++

+++텍스트 메시지 구성

알림 기반 공급자(Slack, SMS, 이메일)의 경우 JSONata의 `&` 연결 연산자를 사용하여 메시지 문자열을 직접 작성할 수 있습니다.

```jsonata
{
  "text": "You just earned " & rewardContext.rewardValue & " " & reward.denomination & "!"
}
```

**출력:**

```json
{
  "text": "You just earned 50 Stars!"
}
```

+++

## 예

+++예제 1 - 단순 포인트 공급자

**시나리오:** 기본 충성도 포인트 API에는 멤버 ID와 포인트 금액이 필요합니다.

**보상 정의:**

```json
{
  "name":         "Standard Points",
  "denomination": "Points",
  "desc":         "Award loyalty points",
  "enabled":      true,
  "rewardJsonata": "{\"memberId\": challenge.profileId, \"pointQuantity\": $number(rewardContext.rewardValue), \"denomination\": reward.denomination}"
}
```

**서식이 지정된 식:**

```jsonata
{
  "memberId":      challenge.profileId,
  "pointQuantity": $number(rewardContext.rewardValue),
  "denomination":  reward.denomination
}
```

**공급자에 대한 페이로드 POST됨:**

```json
{
  "memberId":      "ADB-0000030",
  "pointQuantity": 50,
  "denomination":  "Points"
}
```

+++

+++예제 2 - 캠페인 메타데이터가 포함된 공급자 페이로드

**시나리오:** 공급자에는 감사 필드, 캠페인 참조 및 구성원 설명이 포함된 구조화된 포상 레코드가 필요합니다. 캠페인 특정 값이 `challenge.kvpCustom`에 저장되므로 식을 편집하지 않고 캠페인 간에 동일한 보상 정의가 작동합니다.

**챌린지`kvpCustom`**(챌린지를 작성할 때 설정됨):

```json
{
  "parentCampaignId": "CAMP-2026-Q1",
  "productName":      "Loyalty Program"
}
```

**보상 정의:**

```json
{
  "name":         "Stars — Campaign Award",
  "denomination": "Stars",
  "desc":         "Issue Stars for completing a qualifying purchase",
  "enabled":      true,
  "rewardJsonata": "{\"awardPoints\":[{\"idType\":\"externalId\",\"id\":challenge.profileId,\"transactionId\":task.accumulators.item_list[-1].transactionId,\"transactionDate\":task.accumulators.item_list[-1].timestamp,\"originalTransactionId\":task.accumulators.item_list[-1].transactionId,\"transactionSource\":\"AJO\",\"channelSource\":\"Web\",\"parentCampaignId\":challenge.kvpCustom.parentCampaignId,\"productName\":challenge.kvpCustom.productName,\"memberAwardDescription\":reward.desc,\"pointQuantity\":$number(rewardContext.rewardValue)}]}"
}
```

**서식이 지정된 식:**

```jsonata
{
  "awardPoints": [
    {
      "idType":                "externalId",
      "id":                    challenge.profileId,
      "transactionId":         task.accumulators.item_list[-1].transactionId,
      "transactionDate":       task.accumulators.item_list[-1].timestamp,
      "originalTransactionId": task.accumulators.item_list[-1].transactionId,
      "transactionSource":     "AJO",
      "channelSource":         "Web",
      "parentCampaignId":      challenge.kvpCustom.parentCampaignId,
      "productName":           challenge.kvpCustom.productName,
      "memberAwardDescription": reward.desc,
      "pointQuantity":         $number(rewardContext.rewardValue)
    }
  ]
}
```

**공급자에 대한 페이로드 POST됨:**

```json
{
  "awardPoints": [
    {
      "idType":                "externalId",
      "id":                    "ADB-0000030",
      "transactionId":         "b4fa0e89-f4bb-41ce-b370-fb97f9c52f1a",
      "transactionDate":       "2026-02-08T00:12:00.000+00:00",
      "originalTransactionId": "b4fa0e89-f4bb-41ce-b370-fb97f9c52f1a",
      "transactionSource":     "AJO",
      "channelSource":         "Web",
      "parentCampaignId":      "CAMP-2026-Q1",
      "productName":           "Loyalty Program",
      "memberAwardDescription": "Issue Stars for completing a qualifying purchase",
      "pointQuantity":         50
    }
  ]
}
```

+++

+++예제 3 — 마일스톤 보상

**시나리오:** 연속 도전은 N회 방문할 때마다 마일스톤 보상을 발행합니다. 표현식에 마일스톤 수와 공급자측 컨텍스트의 현재 행진이 포함됩니다.

**서식이 지정된 식:**

```jsonata
{
  "memberId":       challenge.profileId,
  "points":         $number(rewardContext.rewardValue),
  "milestoneCount": milestone.count,
  "currentStreak":  task.schedule.currentStreak,
  "denomination":   reward.denomination,
  "source":         rewardContext.source
}
```

**공급자에게 페이로드 POST됨**(두 번째 방문 마일스톤 시):

```json
{
  "memberId":       "ADB-0000030",
  "points":         20,
  "milestoneCount": 2,
  "currentStreak":  2,
  "denomination":   "Stars",
  "source":         "milestone"
}
```

> `rewardContext.source`이(가) `"milestone"`이면 `milestone` 개체가 `count` 및 `reward.rewardValue`(으)로 채워집니다. 소스가 `"task"` 또는 `"challenge"`인 경우 `milestone`은(는) `null`입니다.

+++

## API 참조

+++보상 제공자

```http
POST   /loyalty/metadata/config/rewards/providers
GET    /loyalty/metadata/config/rewards/providers
GET    /loyalty/metadata/config/rewards/providers/{providerId}
PUT    /loyalty/metadata/config/rewards/providers/{providerId}
DELETE /loyalty/metadata/config/rewards/providers/{providerId}
```

모든 요청에는 `x-gw-ims-org-id` 및 `x-sandbox-name` 헤더가 필요합니다.

**공급자 만들기:**

```http
POST /loyalty/metadata/config/rewards/providers
x-gw-ims-org-id: {ORG_ID}
x-sandbox-name: {SANDBOX}
Content-Type: application/json

{
  "name":    "My Points Provider",
  "desc":    "Issues loyalty points via REST",
  "enabled": true,
  "url":     "https://rewards.example.com/award",
  "additionalHeaders": {
    "x-api-key": "YOUR_API_KEY"
  }
}
```

+++

+++보상 정의

```http
POST   /loyalty/metadata/config/rewards/definitions/{providerId}
GET    /loyalty/metadata/config/rewards/definitions/{providerId}
GET    /loyalty/metadata/config/rewards/definitions/{providerId}/{rewardId}
PUT    /loyalty/metadata/config/rewards/definitions/{providerId}/{rewardId}
DELETE /loyalty/metadata/config/rewards/definitions/{providerId}/{rewardId}
```

**보상 정의 만들기:**

```http
POST /loyalty/metadata/config/rewards/definitions/{providerId}
x-gw-ims-org-id: {ORG_ID}
x-sandbox-name: {SANDBOX}
Content-Type: application/json

{
  "name":         "50 Stars",
  "denomination": "Stars",
  "desc":         "Award 50 Stars on task completion",
  "enabled":      true,
  "rewardJsonata": "{ \"memberId\": challenge.profileId, \"points\": $number(rewardContext.rewardValue) }"
}
```

+++

## 표현식 유효성 검사

게시 시 구문에 대한 `rewardJsonata` 식의 유효성을 검사했습니다. 표현식이 잘못된 경우 API가 구문 분석 실패에 대한 설명과 함께 `422` 오류를 반환합니다.

게시하기 전에 식을 개발하고 테스트하려면 [JSONata 연습기](https://try.jsonata.org/)를 사용하십시오. 보상 컨텍스트 JSON을 입력 문서 및 표현식으로 붙여넣어 출력이 공급자의 예상과 일치하는지 확인합니다. 각 트리거 유형(`task`, `milestone`, `challenge`)에 대한 대표적인 보상 컨텍스트가 위의 예제에 나와 있습니다.

## 일반적인 실수

| 실수 | 효과 | 고정 |
|---------|--------|-----|
| `rewardContext.rewardValue`이(가) 변환 없이 숫자로 사용됨 | 공급자가 필드를 숫자로 확인하는 경우 유형 불일치 | `$number(rewardContext.rewardValue)`(으)로 줄바꿈 |
| `challenge.kvpCustom.someKey`이(가) null을 반환합니다. | 작성 시 문제에 키가 설정되지 않음 | 이 정의를 사용하는 모든 문제에 대해 키가 `kvpCustom`에 있는지 확인하십시오. |
| `task.accumulators.item_list[-1]`이(가) null입니다. | 보상 발행 전 항목이 적용되지 않았습니다(비구매 이벤트). | 조건부로 보호하거나 컨텍스트의 `timestamp`을(를) 대신 사용하십시오. |
| 소스가 `"task"` 또는 `"challenge"`인 경우 `milestone`에 액세스함 | `milestone`이(가) null입니다. 식에서 null 필드가 생성되거나 발생합니다. | `milestone`에 액세스하기 전에 `rewardContext.source`을(를) 확인하거나 마일스톤 보상에 첨부된 정의에서만 `milestone`을(를) 사용하십시오. |
| 식이 개체 대신 배열을 반환합니다. | 공급자가 예기치 않은 페이로드 구조를 수신합니다. | 외부 개체에서 배열 반환 식을 래핑합니다. `{ "items": [...] }` |
