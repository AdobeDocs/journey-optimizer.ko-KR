---
solution: Journey Optimizer
product: journey optimizer
title: 조정된 캠페인 보호 및 제한 사항
description: 오케스트레이션된 캠페인 보호 및 제한 사항에 대해 알아봅니다
hide: true
hidefromtoc: true
exl-id: 82744db7-7358-4cc6-a9dd-03001759fef7
source-git-commit: 3be1b238962fa5d0e2f47b64f6fa5ab4337272a5
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 10%

---

# 가드레일 및 제한 사항 {#guardrails}

+++ 목차

| 오케스트레이션된 캠페인 시작 | 오케스트레이션된 첫 번째 캠페인 시작 | 데이터베이스 쿼리 | 오케스트레이션된 캠페인 활동 |
|---|---|---|---|
| [오케스트레이션된 캠페인 시작](gs-orchestrated-campaigns.md)<br/><br/>관계형 스키마 및 데이터 세트 만들기 및 관리:</br> <ul><li>[스키마 및 데이터 세트 시작](gs-schemas.md)</li><li>[수동 스키마](manual-schema.md)</li><li>[파일 업로드 스키마](file-upload-schema.md)</li><li>[데이터 수집](ingest-data.md)</li></ul>[오케스트레이션된 캠페인 액세스 및 관리](access-manage-orchestrated-campaigns.md)<br/><br/>[오케스트레이션된 캠페인을 만드는 주요 단계](gs-campaign-creation.md) | [캠페인 만들기 및 예약](create-orchestrated-campaign.md)<br/><br/>[활동 오케스트레이션](orchestrate-activities.md)<br/><br/>[캠페인 시작 및 모니터링](start-monitor-campaigns.md)<br/><br/>[보고](reporting-campaigns.md) | [규칙 빌더로 작업](orchestrated-rule-builder.md)<br/><br/>[첫 번째 쿼리 작성](build-query.md)<br/><br/>[표현식 편집](edit-expressions.md)<br/><br/>[리타기팅](retarget.md) | [활동 시작](activities/about-activities.md)<br/><br/>활동:<br/>[And 조인](activities/and-join.md) - [대상자 빌드](activities/build-audience.md) - [차원 변경](activities/change-dimension.md) - [채널 활동](activities/channels.md) - [결합](activities/combine.md) - [중복 제거](activities/deduplication.md) - [보강](activities/enrichment.md) - [포크](activities/fork.md) - [조정](activities/reconciliation.md) - [대상자 저장](activities/save-audience.md) - [분할](activities/split.md) - [대기](activities/wait.md) |

{style="table-layout:fixed"}

+++

## 데이터 흐름에서 데이터 세트로의 제한

Adobe Experience Platform의 각 데이터 세트는 한 번에 하나의 활성 데이터 흐름에만 연결할 수 있습니다. 이 1:1 카디널리티는 플랫폼에 의해 엄격하게 적용됩니다.

데이터 소스를 전환해야 하는 경우(예: Amazon S3에서 Salesforce으로):

데이터 세트에 연결된 기존 데이터 흐름을 삭제해야 합니다.

그런 다음 동일한 데이터 세트에 매핑된 새 소스로 새 데이터 흐름을 만듭니다.

이렇게 하면 신뢰할 수 있는 데이터 수집이 보장되며, 증분 업데이트를 위해 정의된 기본 키와 버전 관리 속성(예: 마지막으로 수정한 날짜)에 따라 달라지는 CDC(변경 데이터 캡처)를 사용할 때 필수적입니다.


## 관계형 스키마/데이터 수집 제한 사항

* 관계형 데이터 저장소에서 최대 200개의 관계형 스키마(테이블)가 지원됩니다.

* Campaign Orchestration에 사용되는 관계형 스키마의 총 크기는 100GB를 초과할 수 없습니다.

* Campaign Orchestration의 일괄 처리 수집은 15분에 한 번 이상 발생하지 않아야 합니다.

* 관계형 스키마에 대한 일일 변경 사항은 총 레코드 수의 20% 미만으로 유지되어야 합니다.

## 데이터 모델링

* 사실 테이블을 포함한 모든 스키마에는 버전 설명자가 필수입니다.

* 모든 테이블에 기본 키가 필요합니다.

* 데이터 세트 생성 중에 할당된 table_name은 세그먼테이션 UI 및 개인화 기능에서 사용됩니다.

  이 이름은 영구적이며 생성 후에는 변경할 수 없습니다.

* 필드 그룹은 현재 지원되지 않습니다.

## 데이터 수집

* 프로필 + 관계형 데이터 수집이 필요합니다.

* 파일 기반 수집에는 변경 유형 필드가 필요하지만 Cloud DB 수집에는 테이블 로깅이 활성화되어 있어야 합니다. CDC(변경 데이터 캡처)에 필요합니다.

* Snowflake에서 수집에서 데이터 가용성까지의 지연 시간은 데이터 볼륨, 동시 실행 및 작업 유형에 따라 15분에서 2시간 사이에 있습니다(삽입이 업데이트보다 빠름).

* Snowflake의 데이터 모니터링은 개발 중입니다. 현재 성공적인 수집에 대한 기본 확인이 없습니다.

* Snowflake 또는 데이터 세트에 대한 직접 업데이트는 지원되지 않습니다. 모든 변화는 CDC 공급원을 통해 흘러가야 한다.

  쿼리 서비스는 읽기 전용입니다.

* ETL은 지원되지 않습니다. 고객은 필요한 형식으로 데이터를 제공해야 합니다.

* 부분 업데이트는 허용되지 않습니다. 각 행을 전체 레코드로 제공해야 합니다.

* 수집은 쿼리 서비스 및 데이터 Distiller을 사용합니다.

## 세분화

* LOV(값 목록) 및 열거형을 현재 사용할 수 있습니다.

* 저장된 대상자는 정적 목록이며 컨텐츠는 캠페인 실행 시 사용할 수 있는 데이터를 반영합니다.

* 저장된 대상자에 대한 추가는 지원되지 않습니다. 업데이트에는 전체 덮어쓰기가 필요합니다.

* 대상은 스칼라 속성으로만 구성해야 합니다. 맵과 배열은 지원되지 않습니다.

* 세그먼테이션은 주로 관계형 데이터를 지원합니다. 프로필 데이터와 혼합하는 것은 허용되지만 큰 프로필 데이터 세트를 가져오면 성능에 영향을 줄 수 있습니다. 이 문제를 방지하려면

* 배치 또는 스트리밍 대상에서 선택한 프로필 속성 수를 제한하는 등 보호 기능이 적용됩니다.

* 읽기 대상은 캐시되지 않습니다. 각 캠페인 실행은 전체 읽기를 트리거합니다.

  대규모 또는 복잡한 대상자에 대한 최적화가 필요합니다.