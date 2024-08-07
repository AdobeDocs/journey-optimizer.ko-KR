---
solution: Journey Optimizer
product: journey optimizer
title: 여정 속성
description: 여정 속성에 대해 알아보기
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: 여정, 표현식, 편집기, 속성
exl-id: eb1ab0ed-90bd-4613-b63d-b28693947db2
source-git-commit: 619bcbc16b4117c29c482c85323603a4281298e0
workflow-type: tm+mt
source-wordcount: '589'
ht-degree: 2%

---

# 여정 속성 속성 {#journey-properties}

[단순 식 편집기](../condition-activity.md#about_condition)와 [고급 식 편집기](../expression/expressionadvanced.md)의 **이벤트** 및 **데이터 원본** 범주 아래에서 **여정 속성** 범주에 액세스할 수 있습니다. 이 카테고리에는 지정된 프로필의 여정과 관련된 기술 필드가 포함되어 있습니다. 이는 여정 ID 또는 발생한 특정 오류와 같은 라이브 여정에서 시스템이 검색한 정보입니다.

![](../assets/journey-properties.png)

여기에는 다음과 같은 정보가 포함됩니다.

* 여정 버전: 여정 uid, 여정 버전 uid, 인스턴스 uid 등
* 오류: 데이터 가져오기, 작업 실행 등
* 현재 단계, 마지막 현재 단계 등
* 삭제된 프로필

  필드 목록을 [이 섹션에서 사용 가능](#journey-properties-fields).

이러한 필드를 사용하여 표현식을 작성할 수 있습니다. 여정 실행 중에 여정에서 직접 값을 검색합니다.

다음은 사용 사례의 몇 가지 예입니다.

* **삭제된 프로필 기록**: 로깅 목적으로 최대 가용량 규칙에 의해 메시지에서 제외된 모든 프로필을 서드파티 시스템으로 보낼 수 있습니다. 이 경우 시간 초과 및 오류 발생 시 경로를 설정하고 특정 오류 유형(예: &quot;최대 가용량 규칙으로 사용자 삭제&quot;)을 필터링할 조건을 추가합니다. 그런 다음 사용자 지정 작업을 통해 삭제된 프로필을 타사 시스템으로 푸시할 수 있습니다.

* **오류 발생 시 알림 보내기**: 메시지에 오류가 발생할 때마다 서드파티 시스템으로 알림을 보낼 수 있습니다. 이를 위해 오류가 발생한 경우 경로를 설정하고, 조건 및 사용자 지정 작업을 추가합니다. 예를 들어 발생한 오류에 대한 설명과 함께 Slack 채널에서 알림을 보낼 수 있습니다.

* **보고에서 오류 세분화** : 오류 메시지에 대해 경로가 하나뿐인 대신 오류 유형별로 조건을 정의할 수 있습니다. 이렇게 하면 보고를 세분화하고 모든 오류 유형 데이터를 볼 수 있습니다.

## 필드 목록 {#journey-properties-fields}

| 카테고리 | 필드 이름 | 레이블 | 설명 |
|---|---|---|------------|
| 여정 버전 | journeyUID | 여정 식별자 | |
| | journeyVersionUID | 여정 버전 식별자 | |
| | 여정 버전 이름 | 여정 버전 이름 | |
| | 여정버전설명 | 여정 버전 설명 | |
| | journeyVersion | 여정 버전 | |
| 여정 인스턴스 | instanceUID | 여정 인스턴스 식별자 | 인스턴스 ID |
| | externalKey | 외부 키 | 여정을 트리거하는 개별 식별자 |
| | organizationId | 조직 식별자 | 브랜드 조직 |
| | sandboxName | 샌드박스 이름 | 샌드박스 이름 |
| 신원 | profileId | 프로필 ID 식별자 | 여정 내 프로필 식별자 |
| | 네임스페이스 | 프로필 ID 네임스페이스 | 여정 내 프로필의 네임스페이스(예: ECID) |
| 현재 노드 | currentNodeId | 현재 노드 식별자 | 현재 활동의 식별자(노드) |
| | currentNodeName | 현재 노드 이름 | 현재 활동의 이름(노드) |
| 이전 노드 | previousNodeId | 이전 노드 식별자 | 이전 활동의 식별자(노드) |
| | previousNodeName | 이전 노드 이름 | 이전 활동의 이름(노드) |
| 오류 | lastNodeUIDInError | 오류의 마지막 노드 식별자 | 오류의 최신 활동(노드) 식별자 |
| | lastNodeNameInError | 오류의 마지막 노드 이름 | 오류의 최신 활동(노드) 이름 |
| | lastNodeTypeInerror | 오류의 마지막 노드 유형 | 오류의 최신 활동(노드) 오류 유형. 가능한 유형:<ul><li>이벤트: 이벤트, 반응, SQ(예: 대상 자격)</li><li>흐름 제어: 종료, 조건, 대기</li><li>작업: ACS 작업, 이동, 사용자 지정 작업</li></ul> |
| | 마지막 오류 코드 | 마지막 오류 코드 | 오류의 최신 활동(노드) 오류 코드. 가능한 오류: <ul><li>HTTP 오류 코드</li><li>제한됨</li><li>timedOut</li><li>오류(예: 예기치 않은 오류의 경우 기본값) 일어나지 않아야/극히 드물게 발생해서는 안 됨)</li></ul> |
| | lastExecutedActionErrorCode | 마지막으로 실행된 작업 오류 코드 | 오류의 최신 액션에 대한 오류 코드 |
| | lastDataFetchErrorCode | 마지막 데이터 가져오기 오류 코드 | 데이터 소스에서 가져온 최신 데이터의 오류 코드 |
| 시간 | lastActionExecutionElapsedTime | 마지막 작업 실행 경과 시간 | 최신 작업을 실행하는 데 걸린 시간 |
| | lastDataFetchElapsedTime | 마지막 데이터 가져오기 경과 시간 | 데이터 소스에서 최신 데이터 가져오기를 실행하는 데 걸린 시간 |
