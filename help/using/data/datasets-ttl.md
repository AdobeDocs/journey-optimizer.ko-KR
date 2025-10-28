---
solution: Journey Optimizer
product: journey optimizer
title: 데이터 세트 TTL(Time-to-Live) 보호 기능
description: ' [!DNL Adobe Journey Optimizer]의 데이터 세트 Time-to-Live 보호'
feature: Data Model, Datasets, Data Management
role: Developer, Admin
level: Experienced
keywords: Platform, Data Lake, 만들기, 레이크, 데이터 세트, 프로필
exl-id: 08633a79-5601-4e36-b8cf-080234956d99
source-git-commit: c4f6b7754255ce3bf0229702b10955abf9843548
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 12%

---

# 데이터 세트 TTL(Time-to-Live) 가드레일 {#ttl-guardrail}

2025년 2월부터 **새로운 샌드박스와 새로운 조직**&#x200B;에서 Journey Optimizer 시스템 생성 데이터 세트에 다음과 같은 TTL(Time-to-Live) 가드레일이 롤아웃됩니다.

* 프로필 스토어의 데이터에 대해 90일
* 데이터 레이크의 데이터에 대해 13개월

이 변경 사항은 후속 단계에서 **기존 고객 샌드박스**&#x200B;로 롤아웃됩니다.

## 영향을 받는 데이터 세트 {#datasets}

아래 표에는 영향을 받는 모든 데이터 세트와 데이터 레이크 및 프로필 스토어에서 해당 Time-To-Live가 나와 있습니다.

| 데이터 세트 | 데이터 레이크 TTL | 프로필 스토어 TTL |
|------|-----|-----|
| AJO 메시지 피드백 이벤트 데이터 세트 | 13개월 | 90일 |
| AJO 이메일 추적 경험 이벤트 데이터 세트 | 13개월 | 90일 |
| AJO 푸시 추적 경험 이벤트 데이터 세트 | 13개월 | 90일 |
| AJO 엔티티 데이터 세트 | 13개월 | 90일 |
| AJO 표면 데이터 세트 | 13개월 | 해당 사항 없음 |
| AJO 인바운드 활동 이벤트 데이터 세트 | 13개월 | 90일 |
| AJO 분류 데이터 세트 | 13개월 | 해당 사항 없음 |
| AJO 이메일 BCC 피드백 이벤트 데이터 세트 | 13개월 | 해당 사항 없음 |
| acpEntity 이벤트 데이터 세트 | 13개월 | 해당 사항 없음 |
| 여정 | 13개월 | 해당 사항 없음 |
| 여정 단계 이벤트 | 13개월 | 해당 사항 없음 |
| 의사 결정 개체 저장소 - 개인화된 오퍼 | 13개월 | 해당 사항 없음 |
| 의사 결정 개체 저장소 - 대체 오퍼 | 13개월 | 해당 사항 없음 |
| 의사 결정 객체 저장소 - 배치 | 13개월 | 해당 사항 없음 |
| 의사 결정 객체 저장소 - 활동 | 13개월 | 해당 사항 없음 |
| Experience Decisioning 개체 저장소 - 개인화된 오퍼 항목 | 13개월 | 해당 사항 없음 |
| ODE DecisionEvents - prod decisioning | 13개월 | 해당 사항 없음 |

## 자주 묻는 질문 {#faq}

데이터 세트 TTL(Time-to-Live)에 대한 FAQ는 다음과 같습니다.

세부 정보가 필요하십니까? 이 페이지 하단의 피드백 옵션을 사용하여 질문을 제기하거나 [Adobe Journey Optimizer 커뮤니티](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=en){target="_blank"}에 연결하세요.

+++이 변경 사항은 프로덕션 샌드박스에만 적용됩니까, 아니면 개발 샌드박스에도 적용됩니까?

이 변경 사항은 모든 샌드박스 유형에 적용됩니다.

+++

+++프로필 스토어의 90일 TTL에 대해 프로필 자체가 영향을 받습니까?

프로필에서 시스템이 생성한 데이터 세트 데이터는 프로필 자체가 아니라 90일 후에 삭제됩니다.

+++

+++시스템에서 생성한 데이터 세트 데이터가 [!DNL Customer Journey Analytics]&#x200B;(CJA)에 푸시되면 CJA의 데이터도 TTL의 영향을 받습니까?

[!DNL Customer Journey Analytics]의 데이터가 Experience Platform과 계속 동기화됩니다. 따라서 시스템 생성 데이터 집합 데이터에 대한 TTL로 인해 데이터가 제거되면 [!DNL Customer Journey Analytics]의 데이터에도 영향을 줍니다.

+++

+++ 고객이 프로필 스토어의 [!DNL Journey Optimizer] 시스템 데이터 세트 데이터에 대한 TTL을 늘릴 수 있습니까? 

TTL 확장은 현재 지원되지 않습니다. 그러나 2025년 후반부터 이러한 확장 요청을 허용하도록 TTL 프로세스를 최적화하기 위한 작업이 계획되어 있습니다.

>[!NOTE]
>
>프로필에 저장된 데이터는 총 데이터 볼륨 권한에 속합니다. 따라서 TTL 확장으로 인한 프로필의 데이터 저장소 증가는 총 데이터 볼륨 권한에 대해 계산됩니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/experience-platform/landing/license/total-data-volume.html){target=&quot;_blank}

+++

+++고객이 데이터 레이크에서 [!DNL Journey Optimizer] 시스템 데이터 세트 데이터의 TTL을 늘릴 수 있습니까? 

TTL 확장은 현재 지원되지 않습니다. 고객은 대상 을 통해 데이터를 내보내 데이터를 더 오래 유지할 수 있습니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html){target=&quot;_blank}. 또한 **[!DNL Data Distiller]** 권한이 있는 고객은 파생 데이터 세트를 만들어 TTL 없이 데이터 레이크에 데이터를 저장할 수 있습니다. [자세히 알아보기](https://experienceleague.adobe.com/en/docs/experience-platform/query/data-distiller/derived-datasets/overview){target=&quot;_blank}

+++

+++다음 기능이 TTL의 영향을 받습니까? 

* **조회 스토어**: 아니요
* **여정 한도**: 아니요
* **오퍼 한도**: 아니요
* **STO(전송 시간 최적화)**: 아니요
* **메시지 빈도 제한**(즉, 비즈니스 규칙): 아니요
* **보고**: 아니요

  >[!NOTE]
  >
  >TTL은 [!DNL Customer Journey Analytics]&#x200B;(CJA) 연결에 이미 구현되었으므로 영향을 받는 데이터 집합 데이터의 유효 최대 전환 확인 기간이 13개월로 줄어듭니다.

* **Experience Platform 데이터 원본**: 해당 사항 없음 - 데이터 원본을 통해 경험 이벤트 검색을 지원하지 않습니다.
* **계산된 특성**: 예 - 초기 채우기 계산은 마지막 90일 데이터로 제한됩니다. 계산된 특성은 후속 업데이트에 대한 증분 이벤트를 기반으로 업데이트됩니다. 후속 업데이트가 전환 확인 기간(최대 6개월)에 도달하면 TTL은 기본적으로 계산된 속성에 더 이상 영향을 주지 않습니다. 추가 정보.
* **세그먼테이션 및 재타겟팅**: 예 - 세그먼테이션은 프로필 저장소의 데이터에 따라 다르므로 영향을 받는 데이터 세트 데이터에서는 룩백을 90일로 제한합니다.
* **추적**: 예 - 영향을 받는 데이터 세트 데이터의 유효 최대 전환 확인 기간을 90일로 줄입니다. 영향을 받는 데이터 세트의 데이터는 데이터 레이크에 13개월 동안 있습니다.

+++

+++TTL 적용에 어떤 타임스탬프가 사용됩니까(예: 채우기 사용 사례의 경우)? 

이벤트 타임스탬프가 사용됩니다(즉, 수집 날짜가 아님).

+++
