---
title: 코드 기반 구현에서 의사 결정 항목 중복 제거
description: 이 페이지에서는 Journey Optimizer 코드 기반 구현에서 의사 결정 요청에 중복 제거를 적용하는 방법을 보여 줍니다.
feature: Code-based Experiences
topic: Content Management
role: Developer
level: Experienced
exl-id: f9477611-b792-4b28-8ec2-6bbea2fa3328
source-git-commit: 57686b9684f9233c81bd46b67d12ec5f1e3544c5
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 1%

---

# 코드 기반 경험 구현에서의 결정

코드 기반 경험에서 Decisioning을 사용할 때 아래에 설명된 경우 클라이언트 구현에 다음 플래그를 추가하는 것이 좋습니다.

## 의사 결정을 사용하여 코드 기반 경험 테스트 {#code-based-test-decisions}

<!--Currently you cannot simulate content from the user interface in a [code-based experience](create-code-based.md) campaign or journey using decisions.-->

Decisioning을 사용하여 [코드 기반 경험](create-code-based.md)을(를) 테스트할 때 `dryRun` 플래그를 사용하여 보고 및 최대 가용량 카운터 모두에 대한 피드백 이벤트를 억제할 수 있습니다.

캠페인을 게시한 후 클라이언트 구현의 XDM 이벤트 `dryRun` 블록에 `data` 플래그를 추가하십시오.

    &quot;
    {
    &quot;data&quot;: {
    &quot;__adobe&quot;: {
    &quot;ajo&quot;: {
    &quot;dryRun&quot;: true
    }
    
    
    
    &quot;

<!--
>[!CAUTION]
>
>Adding the `dryRun` flag to your request will prevent feedback to be captured for reporting and frequency counters from being added to.-->

## 코드 기반 구현에서 의사 결정 항목 중복 제거 {#code-based-decisioning-deduplication}

코드 기반 환경에서 [의사 결정 정책](../experience-decisioning/create-decision.md)을 사용할 때 클라이언트 구현에서 의사 결정 요청에 중복 제거를 적용할 수 있습니다.

의사 결정 요청(콘덕터를 통해)은 중복 제거 플래그를 허용하며, 이 플래그는 여러 의사 결정 정책 또는 배치로 구성된 단일 요청에서 의사 결정 항목의 고유성을 처리합니다.

### 중복 제거 논리 {#deduplication-logic}

의사 결정 요청의 경우 설정에 따라 하나 이상의 의사 결정 정책/배치를 가질 수 있습니다.

* 요청의 **single** 결정 정책 및 배치의 경우, 응답의 모든 항목은 기본적으로 고유합니다. 두 개의 결정 항목은 단일 요청에서 동일할 수 없습니다.

* 요청의 **다중** 결정 정책/배치에 대해:

   * `allowDuplicateDecisionItems`이(가) `false`(으)로 설정된 경우: 항목의 메시지/결정 정책/배치에 관계없이 응답의 모든 항목이 고유합니다.

   * `allowDuplicateDecisionItems`이(가) `true`(기본값)로 설정된 경우: 응답의 항목이 중복될 수 있습니다(여러 메시지/결정 정책/배치가 해당 요청에 대한 동일한 결정 항목에 적합한 경우).

### 요청에 중복 제거 적용 {#deduplication-in-request}

기본적으로 중복 제거 플래그는 `true`(으)로 설정됩니다.

Konductor 요청에서 응답에 고유한 요소를 원하는 경우 중복 제거 플래그를 전달할 수 있습니다. 이 경우 `false`(으)로 설정합니다.

```
{
    "data": {
        "__adobe": {
            "ajo": {
                "allowDuplicateDecisionItems": false
            }
        }
    }
}
```

+++의사 결정 샘플 요청

```
curl --location 'https://edge-int.adobedc.net/ee/v1/interact?configId=2f21d344-b69f-4a4f-98e8-000282fc9552' \
--header 'Content-Type: application/json' \
--data-raw '{
    "events": [
        {
            "query": {
                "personalization": {
                    "schemas": [
                        "https://ns.adobe.com/personalization/html-content-item"
                    ],
                    "surfaces": [
                        "https://www.adobe.com/san/placement/header",
                        "https://www.adobe.com/san/placement/footer"
                    ]
                }
            },
            "xdm": {
                "identityMap": {
                    "Email": [
                        {
                            "id": "cmk-exd-user01-deleted@adobe.com",
                            "primary": true
                        }
                    ]
                }
            },
            "data": {
                "__adobe":{
                    "ajo":{
                        "allowDuplicateDecisionItems": false
                    }
                }       
            }
        }
    ]
}'
```

+++

### 중복 제거 응답 {#deduplication-response}

단일 요청에서 머리글 및 바닥글 배치와 동일한 결정 정책이 있다고 가정해 보겠습니다.

* Decisioning은 두 개의 제안을 반환합니다.

* `itemId-X`이(가) 결정 정책 및 배치 조합에 모두 적합한 단일 결정 항목인 경우:

   * `allowDuplicateDecisionItems`이(가) `true`인 경우(기본값): 단일 응답에서 두 제안에 대해 `itemId-X`이(가) 다시 반환됩니다.

   * `allowDuplicateDecisionItems`이(가) `false`인 경우:

      * 첫 번째 제안에 대해 `itemId-X`이(가) 다시 반환됩니다.

      * 두 번째 제안에 대해 대체 결정 항목(고유함) 또는 빈 결정 항목이 전달됩니다.

+++샘플 응답(`allowDuplicateDecisionItems` = `true`) 결정 중

```
{
    "requestId": "b40170e9-7d31-4242-adcc-18063d6b1d9e",
    "handle": [
        {
            "payload": [
                {
                    "id": "d97f102c-bdae-4ed7-aff6-622d73e3db3d",
                    "scope": "https://www.adobe.com/san/placement/header",
                    "scopeDetails": {
                        "decisionProvider": "AJO",
                        "correlationID": "3cc4ee00-bb76-4eaa-94b6-9b9be2c53e3a-0",
                        "characteristics": {
                            "eventToken": "eyJtZXNzYWdlRXhlY3V0aW9uIjp7Im1lc3NhZ2VFeGVjdXRpb25JRCI6IlVFOkluYm91bmQiLCJtZXNzYWdlSUQiOiJmYWM4YzVmZi1mYWNlLTRkOWItYmEzYi0yYzJjZTEyYzBjODYiLCJtZXNzYWdlUHVibGljYXRpb25JRCI6IjNjYzRlZTAwLWJiNzYtNGVhYS05NGI2LTliOWJlMmM1M2UzYSIsIm1lc3NhZ2VUeXBlIjoibWFya2V0aW5nIiwiY2FtcGFpZ25JRCI6ImUzYmJlZmZkLTZjYjItNGEwMy1iMjRhLTk1YzQ5ZjBkZjRlNCIsImNhbXBhaWduVmVyc2lvbklEIjoiZDlmMTMwNjAtZGVhNC00MTE1LTk5YzMtOGZjMTRjMWFiNTFiIiwiY2FtcGFpZ25BY3Rpb25JRCI6ImE1NmE0OTIxLWJjMjQtNGRjMC04Nzk3LTA2NmU4YzE0NTM5YiJ9LCJtZXNzYWdlUHJvZmlsZSI6eyJtZXNzYWdlUHJvZmlsZUlEIjoiYmQxMDEzNGMtNjBkMS00NjZiLWEwYWMtOWQ0MzdmNmY5YTczIiwiY2hhbm5lbCI6eyJfaWQiOiJodHRwczovL25zLmFkb2JlLmNvbS94ZG0vY2hhbm5lbHMvY29kZSIsIl90eXBlIjoiaHR0cHM6Ly9ucy5hZG9iZS5jb20veGRtL2NoYW5uZWwtdHlwZXMvY29kZSJ9fX0=",
                            "subPropositions": "W3siaWQiOiI4ZmMzMDBjYy1iMTg5LTQ2MTUtYmY0OC03NjIwMjZkMjlmMWYiLCJzY29wZSI6Imh0dHBzOi8vd3d3LmFkb2JlLmNvbS9zYW4vcGxhY2VtZW50L2hlYWRlciIsInNjb3BlRGV0YWlscyI6eyJkZWNpc2lvblByb3ZpZGVyIjoiRVhEIiwiY29ycmVsYXRpb25JRCI6IjNjYzRlZTAwLWJiNzYtNGVhYS05NGI2LTliOWJlMmM1M2UzYS0wIiwic3RyYXRlZ2llcyI6W3sic3RyYXRlZ3lJRCI6IjlhOTRjZjhjLTNkZjItNDE2NS1hMzRiLTIxNzBlMjg2YmUzMiIsInN0ZXAiOiJkZWNpc2lvblBvbGljeSJ9LHsic3RyYXRlZ3lJRCI6Imh0dHBzOi8vd3d3LmFkb2JlLmNvbS9zYW4vcGxhY2VtZW50L2hlYWRlciIsInN0ZXAiOiJwbGFjZW1lbnQifV0sInJhbmsiOjEsImFjdGl2aXR5Ijp7ImlkIjoiZTNiYmVmZmQtNmNiMi00YTAzLWIyNGEtOTVjNDlmMGRmNGU0I2E1NmE0OTIxLWJjMjQtNGRjMC04Nzk3LTA2NmU4YzE0NTM5YiIsInByaW9yaXR5IjowLCJtYXRjaGVkU3VyZmFjZXMiOlsiaHR0cHM6Ly93d3cuYWRvYmUuY29tL3Nhbi9wbGFjZW1lbnQvaGVhZGVyIl19fSwiaXRlbXMiOlt7ImlkIjoiZHBzOmM3MjI1YzNmYWMxNGUzMDBjYTNkZTlmY2I2ZDk4NTI0YjM5NTQ4YzFmYzFlYmQ2OToxOThkM2I5NDczZDRjYzQ3IiwiZXRhZyI6IjciLCJuYW1lIjoidGVzdFNhbi1tYW51YWxGYWxsYmFjay1vZmZlcjAxIiwic2NvcmUiOjExLjAsIml0ZW1TZWxlY3Rpb24iOnsic2VsZWN0aW9uRGV0YWlsIjp7InN0cmF0ZWd5SUQiOiJkcHM6c2VsZWN0aW9uLXN0cmF0ZWd5OjFhMGUzOTY4NzJlOWZiMWUiLCJzdHJhdGVneU5hbWUiOiJ0ZXN0U2FuLW1hbnVhbEZhbGxiYWNrLXN0cmF0ZWd5MTAwIiwic2VsZWN0aW9uVHlwZSI6InNlbGVjdGlvblN0cmF0ZWd5IiwidmVyc2lvbiI6Ijc0NUYzN0MzNUU0Qjc3NkUwQTQ5NDIxQkBBZG9iZU9yZzo2MzM5NzRmNC1lNTRlLTQyZjMtYjk3NC1mNGU1NGVjMmYzYmU6NThlNjE0MTItZTExOS00Mjg4LWJiZGEtYmQ1NGQ1MDgxNjVmIn0sInJhbmtpbmdEZXRhaWwiOnsic3RlcCI6InByaW9yaXR5In19LCJ0b2tlbiI6IitsckV1NWtHdnkrRXVYRFZ1K0VMWHcifV19XQ=="
                        },
                        "rank": 1,
                        "activity": {
                            "id": "e3bbeffd-6cb2-4a03-b24a-95c49f0df4e4#a56a4921-bc24-4dc0-8797-066e8c14539b",
                            "priority": 0,
                            "matchedSurfaces": [
                                "https://www.adobe.com/san/placement/header"
                            ]
                        }
                    },
                    "items": [
                        {
                            "id": "f37463f7-d23b-4ef1-b412-de1ac127efb9",
                            "schema": "https://ns.adobe.com/personalization/html-content-item",
                            "data": {
                                "content": "\nitemId: dps:c7225c3fac14e300ca3de9fcb6d98524b39548c1fc1ebd69:198d3b9473d4cc47\nitemName: testSan-manualFallback-offer01\ntrackingToken: +lrEu5kGvy+EuXDVu+ELXw\n"
                            }
                        }
                    ]
                },
                {
                    "id": "e1de0998-44d6-435d-8974-1d5175a845ea",
                    "scope": "https://www.adobe.com/san/placement/footer",
                    "scopeDetails": {
                        "decisionProvider": "AJO",
                        "correlationID": "3cc4ee00-bb76-4eaa-94b6-9b9be2c53e3a-0",
                        "characteristics": {
                            "eventToken": "eyJtZXNzYWdlRXhlY3V0aW9uIjp7Im1lc3NhZ2VFeGVjdXRpb25JRCI6IlVFOkluYm91bmQiLCJtZXNzYWdlSUQiOiJmYWM4YzVmZi1mYWNlLTRkOWItYmEzYi0yYzJjZTEyYzBjODYiLCJtZXNzYWdlUHVibGljYXRpb25JRCI6IjNjYzRlZTAwLWJiNzYtNGVhYS05NGI2LTliOWJlMmM1M2UzYSIsIm1lc3NhZ2VUeXBlIjoibWFya2V0aW5nIiwiY2FtcGFpZ25JRCI6ImUzYmJlZmZkLTZjYjItNGEwMy1iMjRhLTk1YzQ5ZjBkZjRlNCIsImNhbXBhaWduVmVyc2lvbklEIjoiZDlmMTMwNjAtZGVhNC00MTE1LTk5YzMtOGZjMTRjMWFiNTFiIiwiY2FtcGFpZ25BY3Rpb25JRCI6ImE1NmE0OTIxLWJjMjQtNGRjMC04Nzk3LTA2NmU4YzE0NTM5YiJ9LCJtZXNzYWdlUHJvZmlsZSI6eyJtZXNzYWdlUHJvZmlsZUlEIjoiMGI4NTYxMzAtNDZiNy00OTQ1LTgwYTAtZjM2MGUzMjhlMjllIiwiY2hhbm5lbCI6eyJfaWQiOiJodHRwczovL25zLmFkb2JlLmNvbS94ZG0vY2hhbm5lbHMvY29kZSIsIl90eXBlIjoiaHR0cHM6Ly9ucy5hZG9iZS5jb20veGRtL2NoYW5uZWwtdHlwZXMvY29kZSJ9fX0=",
                            "subPropositions": "W3siaWQiOiI1NzViZDY3My0yMTQ1LTQ2MzAtYjQ1Yy1iNDAwMGUxMzI1NmMiLCJzY29wZSI6Imh0dHBzOi8vd3d3LmFkb2JlLmNvbS9zYW4vcGxhY2VtZW50L2Zvb3RlciIsInNjb3BlRGV0YWlscyI6eyJkZWNpc2lvblByb3ZpZGVyIjoiRVhEIiwiY29ycmVsYXRpb25JRCI6IjNjYzRlZTAwLWJiNzYtNGVhYS05NGI2LTliOWJlMmM1M2UzYS0wIiwic3RyYXRlZ2llcyI6W3sic3RyYXRlZ3lJRCI6IjlhOTRjZjhjLTNkZjItNDE2NS1hMzRiLTIxNzBlMjg2YmUzMiIsInN0ZXAiOiJkZWNpc2lvblBvbGljeSJ9LHsic3RyYXRlZ3lJRCI6Imh0dHBzOi8vd3d3LmFkb2JlLmNvbS9zYW4vcGxhY2VtZW50L2Zvb3RlciIsInN0ZXAiOiJwbGFjZW1lbnQifV0sInJhbmsiOjEsImFjdGl2aXR5Ijp7ImlkIjoiZTNiYmVmZmQtNmNiMi00YTAzLWIyNGEtOTVjNDlmMGRmNGU0I2E1NmE0OTIxLWJjMjQtNGRjMC04Nzk3LTA2NmU4YzE0NTM5YiIsInByaW9yaXR5IjowLCJtYXRjaGVkU3VyZmFjZXMiOlsiaHR0cHM6Ly93d3cuYWRvYmUuY29tL3Nhbi9wbGFjZW1lbnQvZm9vdGVyIl19fSwiaXRlbXMiOltdfV0="
                        },
                        "rank": 1,
                        "activity": {
                            "id": "e3bbeffd-6cb2-4a03-b24a-95c49f0df4e4#a56a4921-bc24-4dc0-8797-066e8c14539b",
                            "priority": 0,
                            "matchedSurfaces": [
                                "https://www.adobe.com/san/placement/footer"
                            ]
                        }
                    },
                    "items": [
                        {
                            "id": "f37463f7-d23b-4ef1-b412-de1ac127efb9",
                            "schema": "https://ns.adobe.com/personalization/html-content-item",
                            "data": {
                                "content": "\nitemId: dps:c7225c3fac14e300ca3de9fcb6d98524b39548c1fc1ebd69:198d3b9473d4cc47\nitemName: testSan-manualFallback-offer01\ntrackingToken: +lrEu5kGvy+EuXDVu+ELXw\n"
                            }
                        }
                    ]
                }
            ],
            "type": "personalization:decisions",
            "eventIndex": 0
        }
    ]
}
```

+++

+++샘플 응답(`allowDuplicateDecisionItems` = `false`) 결정 중

```
{
    "requestId": "b40170e9-7d31-4242-adcc-18063d6b1d9e",
    "handle": [
        {
            "payload": [
                {
                    "id": "d97f102c-bdae-4ed7-aff6-622d73e3db3d",
                    "scope": "https://www.adobe.com/san/placement/header",
                    "scopeDetails": {
                        "decisionProvider": "AJO",
                        "correlationID": "3cc4ee00-bb76-4eaa-94b6-9b9be2c53e3a-0",
                        "characteristics": {
                            "eventToken": "eyJtZXNzYWdlRXhlY3V0aW9uIjp7Im1lc3NhZ2VFeGVjdXRpb25JRCI6IlVFOkluYm91bmQiLCJtZXNzYWdlSUQiOiJmYWM4YzVmZi1mYWNlLTRkOWItYmEzYi0yYzJjZTEyYzBjODYiLCJtZXNzYWdlUHVibGljYXRpb25JRCI6IjNjYzRlZTAwLWJiNzYtNGVhYS05NGI2LTliOWJlMmM1M2UzYSIsIm1lc3NhZ2VUeXBlIjoibWFya2V0aW5nIiwiY2FtcGFpZ25JRCI6ImUzYmJlZmZkLTZjYjItNGEwMy1iMjRhLTk1YzQ5ZjBkZjRlNCIsImNhbXBhaWduVmVyc2lvbklEIjoiZDlmMTMwNjAtZGVhNC00MTE1LTk5YzMtOGZjMTRjMWFiNTFiIiwiY2FtcGFpZ25BY3Rpb25JRCI6ImE1NmE0OTIxLWJjMjQtNGRjMC04Nzk3LTA2NmU4YzE0NTM5YiJ9LCJtZXNzYWdlUHJvZmlsZSI6eyJtZXNzYWdlUHJvZmlsZUlEIjoiYmQxMDEzNGMtNjBkMS00NjZiLWEwYWMtOWQ0MzdmNmY5YTczIiwiY2hhbm5lbCI6eyJfaWQiOiJodHRwczovL25zLmFkb2JlLmNvbS94ZG0vY2hhbm5lbHMvY29kZSIsIl90eXBlIjoiaHR0cHM6Ly9ucy5hZG9iZS5jb20veGRtL2NoYW5uZWwtdHlwZXMvY29kZSJ9fX0=",
                            "subPropositions": "W3siaWQiOiI4ZmMzMDBjYy1iMTg5LTQ2MTUtYmY0OC03NjIwMjZkMjlmMWYiLCJzY29wZSI6Imh0dHBzOi8vd3d3LmFkb2JlLmNvbS9zYW4vcGxhY2VtZW50L2hlYWRlciIsInNjb3BlRGV0YWlscyI6eyJkZWNpc2lvblByb3ZpZGVyIjoiRVhEIiwiY29ycmVsYXRpb25JRCI6IjNjYzRlZTAwLWJiNzYtNGVhYS05NGI2LTliOWJlMmM1M2UzYS0wIiwic3RyYXRlZ2llcyI6W3sic3RyYXRlZ3lJRCI6IjlhOTRjZjhjLTNkZjItNDE2NS1hMzRiLTIxNzBlMjg2YmUzMiIsInN0ZXAiOiJkZWNpc2lvblBvbGljeSJ9LHsic3RyYXRlZ3lJRCI6Imh0dHBzOi8vd3d3LmFkb2JlLmNvbS9zYW4vcGxhY2VtZW50L2hlYWRlciIsInN0ZXAiOiJwbGFjZW1lbnQifV0sInJhbmsiOjEsImFjdGl2aXR5Ijp7ImlkIjoiZTNiYmVmZmQtNmNiMi00YTAzLWIyNGEtOTVjNDlmMGRmNGU0I2E1NmE0OTIxLWJjMjQtNGRjMC04Nzk3LTA2NmU4YzE0NTM5YiIsInByaW9yaXR5IjowLCJtYXRjaGVkU3VyZmFjZXMiOlsiaHR0cHM6Ly93d3cuYWRvYmUuY29tL3Nhbi9wbGFjZW1lbnQvaGVhZGVyIl19fSwiaXRlbXMiOlt7ImlkIjoiZHBzOmM3MjI1YzNmYWMxNGUzMDBjYTNkZTlmY2I2ZDk4NTI0YjM5NTQ4YzFmYzFlYmQ2OToxOThkM2I5NDczZDRjYzQ3IiwiZXRhZyI6IjciLCJuYW1lIjoidGVzdFNhbi1tYW51YWxGYWxsYmFjay1vZmZlcjAxIiwic2NvcmUiOjExLjAsIml0ZW1TZWxlY3Rpb24iOnsic2VsZWN0aW9uRGV0YWlsIjp7InN0cmF0ZWd5SUQiOiJkcHM6c2VsZWN0aW9uLXN0cmF0ZWd5OjFhMGUzOTY4NzJlOWZiMWUiLCJzdHJhdGVneU5hbWUiOiJ0ZXN0U2FuLW1hbnVhbEZhbGxiYWNrLXN0cmF0ZWd5MTAwIiwic2VsZWN0aW9uVHlwZSI6InNlbGVjdGlvblN0cmF0ZWd5IiwidmVyc2lvbiI6Ijc0NUYzN0MzNUU0Qjc3NkUwQTQ5NDIxQkBBZG9iZU9yZzo2MzM5NzRmNC1lNTRlLTQyZjMtYjk3NC1mNGU1NGVjMmYzYmU6NThlNjE0MTItZTExOS00Mjg4LWJiZGEtYmQ1NGQ1MDgxNjVmIn0sInJhbmtpbmdEZXRhaWwiOnsic3RlcCI6InByaW9yaXR5In19LCJ0b2tlbiI6IitsckV1NWtHdnkrRXVYRFZ1K0VMWHcifV19XQ=="
                        },
                        "rank": 1,
                        "activity": {
                            "id": "e3bbeffd-6cb2-4a03-b24a-95c49f0df4e4#a56a4921-bc24-4dc0-8797-066e8c14539b",
                            "priority": 0,
                            "matchedSurfaces": [
                                "https://www.adobe.com/san/placement/header"
                            ]
                        }
                    },
                    "items": [
                        {
                            "id": "f37463f7-d23b-4ef1-b412-de1ac127efb9",
                            "schema": "https://ns.adobe.com/personalization/html-content-item",
                            "data": {
                                "content": "\nitemId: dps:c7225c3fac14e300ca3de9fcb6d98524b39548c1fc1ebd69:198d3b9473d4cc47\nitemName: testSan-manualFallback-offer01\ntrackingToken: +lrEu5kGvy+EuXDVu+ELXw\n"
                            }
                        }
                    ]
                },
                {
                    "id": "e1de0998-44d6-435d-8974-1d5175a845ea",
                    "scope": "https://www.adobe.com/san/placement/footer",
                    "scopeDetails": {
                        "decisionProvider": "AJO",
                        "correlationID": "3cc4ee00-bb76-4eaa-94b6-9b9be2c53e3a-0",
                        "characteristics": {
                            "eventToken": "eyJtZXNzYWdlRXhlY3V0aW9uIjp7Im1lc3NhZ2VFeGVjdXRpb25JRCI6IlVFOkluYm91bmQiLCJtZXNzYWdlSUQiOiJmYWM4YzVmZi1mYWNlLTRkOWItYmEzYi0yYzJjZTEyYzBjODYiLCJtZXNzYWdlUHVibGljYXRpb25JRCI6IjNjYzRlZTAwLWJiNzYtNGVhYS05NGI2LTliOWJlMmM1M2UzYSIsIm1lc3NhZ2VUeXBlIjoibWFya2V0aW5nIiwiY2FtcGFpZ25JRCI6ImUzYmJlZmZkLTZjYjItNGEwMy1iMjRhLTk1YzQ5ZjBkZjRlNCIsImNhbXBhaWduVmVyc2lvbklEIjoiZDlmMTMwNjAtZGVhNC00MTE1LTk5YzMtOGZjMTRjMWFiNTFiIiwiY2FtcGFpZ25BY3Rpb25JRCI6ImE1NmE0OTIxLWJjMjQtNGRjMC04Nzk3LTA2NmU4YzE0NTM5YiJ9LCJtZXNzYWdlUHJvZmlsZSI6eyJtZXNzYWdlUHJvZmlsZUlEIjoiMGI4NTYxMzAtNDZiNy00OTQ1LTgwYTAtZjM2MGUzMjhlMjllIiwiY2hhbm5lbCI6eyJfaWQiOiJodHRwczovL25zLmFkb2JlLmNvbS94ZG0vY2hhbm5lbHMvY29kZSIsIl90eXBlIjoiaHR0cHM6Ly9ucy5hZG9iZS5jb20veGRtL2NoYW5uZWwtdHlwZXMvY29kZSJ9fX0=",
                            "subPropositions": "W3siaWQiOiI1NzViZDY3My0yMTQ1LTQ2MzAtYjQ1Yy1iNDAwMGUxMzI1NmMiLCJzY29wZSI6Imh0dHBzOi8vd3d3LmFkb2JlLmNvbS9zYW4vcGxhY2VtZW50L2Zvb3RlciIsInNjb3BlRGV0YWlscyI6eyJkZWNpc2lvblByb3ZpZGVyIjoiRVhEIiwiY29ycmVsYXRpb25JRCI6IjNjYzRlZTAwLWJiNzYtNGVhYS05NGI2LTliOWJlMmM1M2UzYS0wIiwic3RyYXRlZ2llcyI6W3sic3RyYXRlZ3lJRCI6IjlhOTRjZjhjLTNkZjItNDE2NS1hMzRiLTIxNzBlMjg2YmUzMiIsInN0ZXAiOiJkZWNpc2lvblBvbGljeSJ9LHsic3RyYXRlZ3lJRCI6Imh0dHBzOi8vd3d3LmFkb2JlLmNvbS9zYW4vcGxhY2VtZW50L2Zvb3RlciIsInN0ZXAiOiJwbGFjZW1lbnQifV0sInJhbmsiOjEsImFjdGl2aXR5Ijp7ImlkIjoiZTNiYmVmZmQtNmNiMi00YTAzLWIyNGEtOTVjNDlmMGRmNGU0I2E1NmE0OTIxLWJjMjQtNGRjMC04Nzk3LTA2NmU4YzE0NTM5YiIsInByaW9yaXR5IjowLCJtYXRjaGVkU3VyZmFjZXMiOlsiaHR0cHM6Ly93d3cuYWRvYmUuY29tL3Nhbi9wbGFjZW1lbnQvZm9vdGVyIl19fSwiaXRlbXMiOltdfV0="
                        },
                        "rank": 1,
                        "activity": {
                            "id": "e3bbeffd-6cb2-4a03-b24a-95c49f0df4e4#a56a4921-bc24-4dc0-8797-066e8c14539b",
                            "priority": 0,
                            "matchedSurfaces": [
                                "https://www.adobe.com/san/placement/footer"
                            ]
                        }
                    },
                    "items": [
                        {
                            "id": "3913a28e-d33b-475b-9737-9f6de3940799",
                            "schema": "https://ns.adobe.com/personalization/html-content-item",
                            "data": {
                                "content": ""
                            }
                        }
                    ]
                }
            ],
            "type": "personalization:decisions",
            "eventIndex": 0
        }       
    ]
}
```

+++
