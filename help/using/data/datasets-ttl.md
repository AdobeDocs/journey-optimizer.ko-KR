---
solution: Journey Optimizer
product: journey optimizer
title: 새로운 TTL(Time-to-Live) 보호 기능 정보
description: Adobe Journey Optimizer의 새로운 TTL(Time-to-Live) 보호 기능
feature: Data Model, Datasets, Data Management
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: Platform, Data Lake, 만들기, 레이크, 데이터 세트, 프로필
source-git-commit: f16ce53f61d64d23f530d007e0124a84e2cc3405
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 5%

---


# TTL(Time-to-Live) 및 스트리밍 세그먼테이션 업데이트 {#ttl-guardrail}

## TTL(Time-to-Live) 보호 기능 {#ttl}

2024년 11월 1일부터 TTL(Time-to-Live) 가드레일이 다음과 같이 **새 샌드박스 및 새 조직**&#x200B;에서 Journey Optimizer 시스템 생성 데이터 세트로 배포됩니다.

* 프로필 스토어의 데이터에 대해 90일
* 데이터 레이크의 데이터에 대해 13개월

이 변경 사항은 이후 단계에서 **기존 고객 샌드박스**&#x200B;로 롤아웃됩니다.

**자주 묻는 질문**

+++ 이 변경 사항은 프로덕션 샌드박스에만 적용됩니까, 아니면 개발 샌드박스에도 적용됩니까?

이 변경 사항은 모든 샌드박스 유형에 적용됩니다.

+++


+++ 프로필 스토어의 90일 TTL에 대해 프로필 자체가 영향을 받습니까?

프로필에서 시스템이 생성한 데이터 세트 데이터는 프로필 자체가 아니라 90일 후에 삭제됩니다.

+++

+++ 시스템 생성 데이터 세트 데이터가 CJA(Customer Journey Analytics)로 푸시되는 경우 CJA의 데이터도 TTL의 영향을 받습니까?

CJA의 데이터는 Experience Platform과 계속 동기화됩니다. 따라서 시스템 생성 데이터 세트 데이터의 TTL로 인한 데이터 제거는 CJA의 데이터에도 영향을 줍니다.

+++

## 스트리밍 세분화 업데이트 {#segmentation-update}

또한 11월 1일부터 스트리밍 세분화는 추적 및 피드백 데이터 세트의 전송 및 피드백 이벤트 사용을 더 이상 지원하지 않습니다. 이 연습이 이전에 권장되지 않은 이유에 대한 정보는 [여기](../audience/about-audiences.md#streaming-segmentation-events-guardrails)에서 확인할 수 있습니다.


**자주 묻는 질문**

+++ 이러한 변경 사항이 클릭 수 또는 기타 추적 이벤트 사용에 영향을 줍니까?

이 변경 사항은 전송 및 열기 이벤트의 사용에만 영향을 줍니다. 클릭 수 및 기타 추적 이벤트는 여전히 스트리밍 세그먼트에서 사용할 수 있습니다.

+++

+++ 배치 세분화는 이 변경의 영향을 받습니까?

이 변경 사항은 스트리밍 세분화에만 영향을 줍니다. 전송 및 열기 이벤트는 여전히 배치 세그먼트에서 사용할 수 있습니다. 스트리밍 세그먼트에서 사용하는 경우 묶음 방식으로 평가됩니다.

+++

+++ 이 변경 사항이 추적 데이터 수집에 영향을 줍니까?

이 변경 사항은 추적 데이터 수집에 영향을 주지 않습니다. 보내기 및 열기 이벤트는 계속 수집됩니다.

+++


+++ 반응 이벤트가 이 변경의 영향을 받습니까?

여정의 반응 이벤트는 이 변경의 영향을 받지 않습니다.

+++


+++ 이 변경 사항은 프로덕션 샌드박스에만 적용됩니까, 아니면 개발 샌드박스에도 적용됩니까?

이 변경 사항은 모든 샌드박스 유형에 적용됩니다.

+++