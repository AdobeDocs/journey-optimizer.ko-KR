---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer에서 데이터 관리 시작
description: 데이터가 Adobe Journey Optimizer에 들어오고 나가는 방법을 알아보며 주요 개념, 설정 단계, 가드레일을 소개합니다.
feature: Data Management
role: Developer, Admin, User
level: Beginner, Intermediate
exl-id: 25519acb-a017-446a-992b-653d3a8a3d96
TQID: https://experienceleague.adobe.com/Dq8mzkfuxvcoAPI1vjq9lFHjz4Z5j9s42-kfMy59PeI
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: aeebb91a-f216-4d5f-8da1-3a7e6f696ed0
subfeature_v2: id: a1cdc218-59b7-4eef-b5cf-2a7ad74b3371id: d6e5c7fd-c1d6-4137-98cd-138ccde6752fid: cf3fbcd7-c075-4ae4-8de5-96e736ab2ea3id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: cc72dcf1-72e1-48cc-b434-e7c27d62d67cid: d095671a-1355-40aa-8b5f-06c33c68080bid: ebde5b41-29c9-4f5e-9ef6-1197e85409e3id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 2612
ht-degree: 100%

---

# 데이터 관리 시작 {#about-data}

데이터는 [!DNL Adobe Journey Optimizer]에서 게재하는 모든 여정, 의사 결정, 메시지의 토대입니다.

이 페이지에서는 다음 사항을 이해할 수 있는 실용적인 시작점을 제공합니다.

* Journey Optimizer에서 사용하는 핵심 데이터 구성 요소(스키마, 데이터 세트, ID, 프로필)
* Journey Optimizer에서 Adobe Experience Platform 데이터를 사용하는 방법
* 여정 및 캠페인을 작성하기 전에 팀에서 완료해야 하는 데이터 설정 단계
* 자세한 구성 및 모범 사례를 확인할 수 있는 위치

데이터 엔지니어, 관리자, 마케터와 함께 이 안내서를 활용하면 데이터가 Journey Optimizer으로 들어오고 나가는 방식에 대한 전체적인 그림을 모두가 공유할 수 있습니다.

>[!TIP]
>Journey Optimizer에서 데이터 관리를 처음 수행하시나요? [데이터 설정 개요 튜토리얼](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/tutorials/data-management/set-up-data-overview){target="_blank"}을 시청하면 스키마, 데이터 세트, 소스에 대해 실용적이고 초심자가 이해하기 쉬운 설명을 확인할 수 있습니다.

## Journey Optimizer에서 Adobe Experience Platform 데이터를 사용하는 방법 {#aep-data}

[!DNL Adobe Journey Optimizer]은(는) [!DNL Adobe Experience Platform] 기반으로 빌드됩니다. 별도의 격리된 데이터 저장소를 유지하지 않습니다. 대신 여타 Experience Cloud 애플리케이션과 동일한 데이터 기반을 사용합니다.

스키마 및 데이터 세트는 Adobe Experience Platform에 있습니다. ID 및 [실시간 고객 프로필](../audience/get-started-profiles.md)은 ID 서비스 및 프로필 서비스에서 관리합니다. Journey Optimizer는 Adobe Experience Platform에서 프로필 및 이벤트 데이터를 읽어 여정 조건을 평가하고 메시지를 개인화하고 오퍼를 선택합니다. 보내기, 열, 클릭, 바운스 이벤트 및 여정 단계 이벤트와 같은 상호 작용 데이터를 Experience Platform 데이터 세트에 다시 기록합니다. 또한 추가 데이터 세트를 조회하면서 런타임 시 프로필에 해당 데이터를 복사하지 않도록 할 수도 있습니다.

>[!TIP]
>Adobe Experience Platform은 중앙 데이터 레이어이고, Journey Optimizer는 그 공유형 데이터 기반을 사용하여 여정 및 메시지를 오케스트레이션하는 애플리케이션이라고 생각하면 됩니다.

➡️ [Journey Optimizer 아키텍처에 대해 자세히 알아보기](https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/get-started/essentials/understanding-ajo#architecture-details){target="_blank"}

## Journey Optimizer의 주요 데이터 개념 {#key-concepts}

Journey Optimizer에서 데이터를 사용하여 작업할 때는 몇 가지 관련 개념을 접하게 됩니다. 아래 표에서는 간단한 개요를 확인할 수 있고, 이어질 섹션에서는 각 개념을 자세히 설명합니다.

| 개념 | 정의 | Journey Optimizer 내 주된 용도 |
|---|---|---|
| XDM 스키마 | 데이터를 나타내고 유효성을 검사하고 형식을 지정하는 규칙(클래스+필드 그룹으로 작성) | 프로필 속성 및 행동 이벤트 모델링 |
| 데이터 세트 | 스키마를 따르는 데이터 스토리지 테이블 | 프로필, 이벤트, 시스템 생성 데이터 저장 |
| 소스 커넥터 | 외부 시스템의 데이터를 AEP로 스트리밍 또는 배치 수집 | CRM, 분석, 웹 데이터 수집 |
| 데이터 소스 | 여정 내부에 AEP 또는 외부 필드 표시 | 여정 조건 및 메시지 개인화 지원 |
| ID | 개별 고객을 고유하게 나타내는 식별자 | 채널 간 프로필 결합 |
| 조회 데이터 세트 | 프로필 스토리지 없이 런타임 중 AEP 데이터 참조 | 라이브 참조 데이터로 메시지 보강 |

### 스키마(XDM 스키마) {#schema}

스키마는 데이터를 나타내고 유효성을 검사하며 서식을 지정하는 규칙 세트입니다. **클래스**(레코드 또는 시계열 중 기준 동작 정의)와 선택적 **필드 그룹**(특정 필드 추가)으로 구성됩니다. 스키마는 경험 데이터 모델(XDM) 표준을 사용하여 정의되며 Adobe Experience Platform에 저장됩니다.

XDM은 동일한 개념(고객, 구매, 제품)에 소스 시스템마다 다른 이름과 구조화가 적용된다는 실질적인 문제를 해결하기 위해 존재합니다. XDM은 데이터의 출처에 관계없이 단일 정의 하에 이러한 개념을 통합하는 공유 언어를 제공합니다. 이렇게 하면 Journey Optimizer이 CRM, 웹 사이트, 모바일 앱, 데이터 웨어하우스의 데이터를 동시에 사용하여 일관되게 작업할 수 있습니다.

Journey Optimizer에서는 일반적으로 고객 속성(이름, 환경 설정, 동의)에 대한 **XDM 개별 프로필** 스키마와 행동 이벤트(구매, 페이지 조회, 등록)에 대한 **XDM ExperienceEvent** 스키마로 작업합니다.

➡️ [스키마에 대해 자세히 알아보기](get-started-schemas.md)

### 데이터 세트 {#dataset}

데이터 세트는 스키마를 준수하는 데이터의 저장 및 관리 구조입니다. 정의된 열과 행 집합으로 구성된 테이블로 생각하면 됩니다. Journey Optimizer에서 사용하는 모든 데이터는 Adobe Experience Platform 데이터 세트에 저장됩니다. 이 데이터 세트는 프로필 데이터 세트(실시간 고객 프로필에 기여)나 이벤트 데이터 세트(여정 및 분석을 위해 행동 데이터 저장) 또는 Journey Optimizer에서 추적, 피드백, 여정 단계 이벤트를 위해 자동으로 만든 시스템 데이터 세트일 수 있습니다.

➡️ [데이터 세트에 대해 자세히 알아보기](get-started-datasets.md)

### 소스 커넥터 {#source-connector}

소스 커넥터(**소스**&#x200B;라고도 지칭)는 Adobe Analytics, Adobe Experience Platform Web SDK, 클라우드 스토리지(S3, Azure Blob) 또는 CRM 데이터베이스와 같은 여러 시스템의 데이터를 Adobe Experience Platform으로 수집하는 데 도움이 됩니다. 원시 데이터 수집 외에도 커넥터를 통해 Experience Platform 서비스를 사용하여 XDM 스키마에 필드를 매핑하거나 데이터 거버넌스에 레이블을 지정하는 등 데이터의 구조화, 레이블 지정, 개선을 수행할 수 있습니다.

➡️ [소스 커넥터에 대해 자세히 알아보기](../start/get-started-sources.md)

### 데이터 소스(Journey Optimizer) {#data-source}

Journey Optimizer의 데이터 소스에서는 Adobe Experience Platform(이나 외부 API)의 필드 중 여정 및 메시지 내에 노출할 필드를 정의합니다. Journey Optimizer UI에서 구성되는 데이터 소스에는 일반적으로 기본 제공 Adobe Experience Platform 데이터 소스(실시간 고객 프로필 속성 노출)와, 추가적인 데이터 강화를 위해 여정 런타임 시 호출되는 선택적 외부 소스 또는 사용자 정의 데이터 소스가 포함됩니다. 여정 조건, 사용자 정의 액션, 메시지 개인화에 사용됩니다.

➡️ [데이터 소스에 대해 자세히 알아보기](../datasource/about-data-sources.md)

>[!NOTE]
>[Adobe Experience Platform 용어집](https://experienceleague.adobe.com/ko/docs/experience-platform/landing/glossary){target="_blank"}에서는 &#39;데이터 소스&#39;를 일반적으로 데이터의 원본 출처(CRM, 모바일 앱 등)로 정의합니다. Journey Optimizer에서 **데이터 소스**&#x200B;는 여정 및 메시지 내에 노출되는 필드를 제어하는 UI 구성이라는 특정한 의미를 갖습니다.

### ID 및 실시간 고객 프로필 {#identity}

ID는 쿠키 ID, 디바이스 ID, 이메일 주소 또는 CRM ID 등 개별 고객을 고유하게 나타내는 식별자입니다. ID는 네임스페이스(이메일, ECID, CRMID)로 구성되며, 동일한 사용자에 대한 여러 ID가 통합 ID 그래프로 결합됩니다. 실시간 고객 프로필은 이 그래프로 온라인과 오프라인, CRM, 서드파티를 비롯한 여러 채널의 데이터를 결합하여 각각의 고객을 거시적으로 확인할 수 있도록 자원합니다.

초심자에게 중요한 개념은 **프로필 조각** 모델입니다. 고객이 특정 디바이스 또는 채널(웹 사이트, 모바일 앱, 스토어)에서 브랜드와 상호 작용할 때마다 해당 상호 작용은 프로필 조각, 즉 해당 특정 터치포인트를 기반으로 하는 해당 고객의 부분적 보기로 기록됩니다. 실시간 고객 프로필은 공유 ID 값을 기반으로 이러한 조각을 지속적으로 결합함으로써 온전한 최신 상태의 프로필을 빌드합니다. Journey Optimizer은 이렇게 결합된 프로필에서 데이터를 읽어 실시간으로 조건을 평가하고 오퍼를 선택하며 메시지를 개인화합니다.

➡️ [Journey Optimizer의 ID에 대해 자세히 알아보기](../audience/get-started-identity.md)

### 조회 데이터 세트 {#lookup-dataset}

조회 데이터 세트를 사용하면 Journey Optimizer가 실시간 고객 프로필에 데이터를 저장할 필요 없이 런타임 중에 Adobe Experience Platform 데이터 세트의 참조 또는 트랜잭션 데이터를 검색할 수 있습니다. 이 기능은 메시지를 보낼 때는 필요하지만 프로필에 속하지는 않으며 자주 변하는 참조 데이터(가격, 인벤토리, 매장 운영 시간) 또는 트랜잭션 데이터에 유용합니다. Journey Optimizer는 여정 또는 메시지 실행 중에 제품 ID와 같은 키를 기반으로 조회를 수행합니다.

➡️ [조회 데이터 세트에 대해 자세히 알아보기](lookup-aep-data.md)

## 데이터 준비 상태 체크리스트 {#checklist}

마케터가 여정 및 캠페인 작성을 시작하기 전에 먼저 조직에서 일련의 데이터 준비 단계를 완료해야 합니다. 그래야 Journey Optimizer가 적절한 시점에 규정을 준수하는 방식으로 올바른 데이터를 사용할 수 있습니다.

>[!NOTE]
>아래 단계에는 데이터 엔지니어, 관리자, 마케터 등 여러 역할이 포함됩니다. 이 체크리스트를 공동 계획으로 활용하여 환경을 준비하십시오. 1~4단계는 Adobe Experience Platform에서 완료되고 5~6단계는 Journey Optimizer에서 구성됩니다.

아래 6개의 단계에서는 ID 구성에서부터 데이터가 Journey Optimizer으로 올바르게 유입되는지 확인하는 것까지 전체 데이터 설정 프로세스를 안내합니다.

1. ID 전략 정의
1. 프로필 및 이벤트 데이터를 위한 스키마 디자인
1. 프로필이 활성화된 데이터 세트 만들기
1. 소스에서 데이터 수집
1. Journey Optimizer에서 데이터 소스 구성
1. 추적, 피드백, 여정 데이터 세트 확인

+++ ID 전략 정의

고객을 위한 기본 ID(예: ECID, 이메일 또는 CRMID)를 선택하고 Adobe Experience Platform ID 서비스에서 그에 해당하는 네임스페이스를 구성합니다. 프로필이 활성화된 스키마에 반드시 ID 필드를 포함하고 프로필이 ID 그래프에 올바르게 결합되었는지 확인합니다.

➡️ [Journey Optimizer의 ID에 대해 자세히 알아보기](../audience/get-started-identity.md)

+++

+++ 프로필 및 이벤트 데이터를 위한 스키마 디자인

**XDM 개인 프로필** 스키마를 만들어 이름 및 연락처 정보, 환경 설정 및 관심 분야, 라이프사이클 단계 또는 동의 상태와 같은 고객 속성을 캡처합니다. **XDM ExperienceEvent** 스키마를 만들어 웹 및 앱 이벤트, 구매, 오프라인 상호 작용과 같은 동작 및 트랜잭션 데이터를 캡처합니다. 적절한 경우 올바른 필드를 ID 및 프로필 속성으로 표시합니다.

➡️ [스키마에 대해 자세히 알아보기](get-started-schemas.md)

+++

+++ 프로필이 활성화된 데이터 세트 만들기

Adobe Experience Platform에서 XDM 스키마를 기반으로 데이터 세트를 만들고 실시간 고객 프로필에 기여해야 하는 모든 데이터 세트에서 프로필을 활성화합니다. Journey Optimizer에서 만든 시스템 생성 데이터 세트가 데이터 세트 작업 영역에 표시되는지 확인합니다.

➡️ [데이터 세트에 대해 자세히 알아보기](get-started-datasets.md)

+++

+++ 소스에서 데이터 수집

Adobe Analytics, Adobe Experience Platform Web SDK, CRM / POS 플랫폼 같은 엔터프라이즈 시스템에 대한 소스 커넥터를 구성하고, 들어오는 필드를 XDM 스키마에 매핑합니다. 데이터가 올바른 데이터 세트에 도달하고 실시간 고객 프로필에 예상대로 표시되는지 확인합니다.

➡️ [소스 커넥터에 대해 자세히 알아보기](../start/get-started-sources.md)

➡️ [튜토리얼: 데이터 세트 만들기 ](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/tutorials/data-management/create-datasets-and-ingest-data){target="_blank"}

+++

+++ Journey Optimizer에서 데이터 소스 구성

데이터 소스는 Journey Optimizer에서 특별히 사용하는 개념입니다. 여기에서 소스는 데이터가 있는 위치가 아니고, 여정 및 메시지 실행 중에 Journey Optimizer에서 읽을 수 있는 필드를 선언하는 위치입니다. 여정에서 &quot;고객이 충성 멤버인가?&quot;와 같은 조건을 평가하거나 메시지에 이름을 적용하여 개인화하려면 데이터 소스 구성을 통해 관련 프로필 필드를 노출해야 합니다.

Journey Optimizer에는 실시간 고객 프로필 속성에 직접 액세스할 수 있는 기본 제공 [Adobe Experience Platform 데이터 소스](../datasource/adobe-experience-platform-data-source.md)가 포함되어 있습니다. 개인화를 위한 프로필 속성 읽기 또는 동의 및 환경 설정 필드 확인과 같은 대부분의 사용 사례에 적용됩니다. [외부 데이터 소스](../datasource/external-data-sources.md)를 구성해 여정 런타임 시 서드파티 API를 호출할 수도 있습니다. 예를 들어, 실시간 충성도 점수, 제품 추천 또는 Adobe Experience Platform에 저장되지 않은 스토어 재고 수량을 검색할 수 있습니다.

>[!NOTE]
>기본 제공 Adobe Experience Platform 데이터 소스를 통해 경험 이벤트 데이터에 직접 액세스하는 방법은 사용 중지 예정이며 점진적으로 비활성화되고 있습니다. [자세히 알아보기](https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/orchestrate-journeys/journey-use-cases/exp-event-lookup){target="_blank"}.

데이터 소스 구성은 여정 작성자 및 마케터가 전체 데이터 레이어를 활용할 수 있도록 하는 관리 작업입니다. 필드가 데이터 소스를 통해 노출되면 바로 여정 조건 빌더, 메시지 개인화 편집기, 오퍼 결정 규칙에 필드를 사용할 수 있으며, 데이터 소스 작성 시 추가 엔지니어링 작업이 필요하지 않습니다.

➡️ [데이터 소스 구성에 대해 자세히 알아보기](../datasource/about-data-sources.md)

+++

+++ 추적, 피드백, 여정 데이터 세트 확인

Journey Optimizer 시스템에서 생성한 데이터 세트를 데이터 세트 작업 영역에서 사용할 수 있는지 확인합니다. 테스트 여정 및 캠페인을 실행한 다음 쿼리 편집기를 사용하여 보내기, 열, 클릭, 바운스 이벤트가 기록되고 여정 단계 이벤트와 상태가 올바르게 캡처되는지 확인합니다. 지속적인 모니터링, 문제 해결, 여정 최적화를 위해 이러한 데이터 세트를 사용합니다.

➡️ [Journey Optimizer의 쿼리에 대해 자세히 알아보기](get-started-queries.md)

+++

## 가드레일 및 데이터 디자인 시 고려 사항 {#guardrails}

일부 제품 가드레일과 제한 사항은 데이터 모델 및 여정을 디자인하는 방식에 영향을 줄 수 있습니다. 나중에 다시 작업할 필요가 없도록 이 내용을 초기부터 검토하십시오.

>[!IMPORTANT]
>항상 [Journey Optimizer 가드레일 및 제한 사항](../start/guardrails.md) 페이지를 참조하여 최신 . 아래 요약에서 주요 항목을 소개하지만, 시간이 지나면서 변할 수 있습니다.

### Journey Optimizer 시스템 데이터 세트 및 TTL {#datasets-ttl}

Journey Optimizer는 추적, 피드백, 여정 단계 이벤트를 위해 몇 가지 시스템 생성 데이터 세트를 만듭니다. 2025년 2월부터 이러한 데이터 세트 중 일부에 TTL(Time-to-Live) 가드레일이 배포되고 있으며, 이는 분석 및 문제 해결을 위해 데이터를 유지하는 기간에 영향을 줄 수 있습니다.

➡️ [데이터 세트 TTL 가드레일에 대해 자세히 알아보기](datasets-ttl.md)

### 스트리밍 세분화 및 Journey Optimizer 이벤트 {#streaming-segmentation}

2024년 11월 1일부로 스트리밍 세분화는 더 이상 Journey Optimize 추적 및 피드백 데이터 세트의 보내기 및 열기 이벤트를 지원하지 않습니다. 빈도 캡핑 및 피로도 관리와 같은 사용 사례에서는 보내기/열기 이벤트를 기반으로 세그먼트를 스트리밍하는 대신 [비즈니스 규칙](../conflict-prioritization/rule-sets.md)을 사용하십시오.

➡️ [데이터 세트에 대해 자세히 알아보기](get-started-datasets.md)

### 데이터 세트 조회 및 의사 결정 {#lookup-guardrails}

데이터 세트 조회는 자주 변경되는 속성(재고, 가격, 날씨) 또는 실시간 고객 프로필에 저장할 필요가 없는 데이터에 니다. 조회 전략을 설계하기 전에 관련 설명서에서 데이터 세트 크기 제한 및 쿼리 제한 등 제품별 가드레일을 검토하십시오.

➡️ [조회 데이터 세트에 대해 자세히 알아보기](lookup-aep-data.md)

## 예: 시작 여정을 위한 데이터 준비 {#example}

다음 예시에서는 이 페이지에서 소개한 개념이 간단한 시나리오에서 함께 작동하는 방식을 보여 줍니다.

1. 데이터 엔지니어는 고객 속성(이름, 이메일, 충성도 등급, 동의)에 대한 [XDM 개인 프로필 스키마](get-started-schemas.md)와 웹 등록 이벤트에 대한 XDM ExperienceEvent 스키마를 만듭니다.
1. [프로필이 활성화된 데이터 세트](get-started-datasets.md)가 각 스키마에 대해 만들어집니다. 하나는 CRM 속성, 하나는 등록 이벤트를 위한 것입니다.
1. 웹 및 모바일 팀에서 Adobe Experience Platform Web SDK를 통해 등록 이벤트를 스트리밍하고, [소스 커넥터](../start/get-started-sources.md)를 통해 CRM 데이터가 수집됩니다.
1. 관리자는 Journey Optimizer에서 [Adobe Experience Platform 데이터 소스](../datasource/adobe-experience-platform-data-source.md)를 구성하고 `profile.person.name.firstName`, `profile.personalEmail.address`, `profile.loyaltyTier` 등 필드를 노출합니다.
1. 마케터는 등록 이벤트를 수신하고 해당 프로필 속성을 사용하여 [시작 이메일을 개인화](../personalization/personalize.md)하는 [시작 여정을 만듭니다](../building-journeys/journey-gs.md). Journey Optimizer는 추적 데이터 세트에 보내기 및 열기 이벤트를 쓰고 여정 단계 이벤트 데이터 세트에 여정 진행 을 기록합니다.
1. 개발자는 [쿼리 편집기](get-started-queries.md)를 사용하여 이벤트가 올바르게 흐르는지 확인하고 성과(열기, 클릭 수, 보내기 시간)를 분석합니다. 팀 이 인사이트를 기반으로 여정 및 콘텐츠를 조정합니다.

이 플로우에서는 초심자가 적용하기 쉬운 온전한 사용 사례에서 스키마, 데이터 세트, 소스, 데이터 소스, 쿼리가 함께 작동하는 방식을 보여 줍니다.

## 관련 리소스 {#related-resources}

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg)

**Get started with schemas**

Adobe Experience Platform에서 XDM 스키마를 만들고 올바른 클래스 및 필드 그룹을 선택하고 프로필 속성 및 행동 이벤트를 모델링하는 방법에 대해 알아봅니다.

[자세히 알아보기](get-started-schemas.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg)

**데이터 세트 작업**

프로필 활성화 및 이벤트 데이터 세트를 만들고, 데이터 수집을 모니터링하고, Journey Optimizer가 추적, 피드백, 여정 단계 이벤트를 위해 자동으로 만드는 시스템 생성 데이터 세트를 탐색하는 방법을 이해합니다.

[자세히 알아보기](get-started-datasets.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg)

**데이터 소스 구성**

기본 제공 Adobe Experience Platform 데이터 소스와, 여정 내에 프로필 필드 및 외부 API 응답을 노출하기 위한 선택적 외부 데이터 소스를 설정하는 단계별 지침입니다.

[자세히 알아보기](../datasource/about-data-sources.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg)

**Adobe Experience Platform 데이터 사용()**

AEP 데이터 세트의 참조 또는 트랜잭션 데이터를 실시간 고객 프로필에 저장하지 않고 사용하여 런타임 중에 메시지를 보강하는 방법에 대해 알아봅니다.

[자세히 알아보기](lookup-aep-data.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg)

**쿼리 시작**

쿼리 서비스를 사용하여 Journey Optimizer 데이터 세트를 분석하고 이벤트가 올바르게 흐르는지 확인하며 데이터 보내기, 열기, 클릭, 바운스에 대한 보고 쿼리를 작성합니다.

[자세히 알아보기](get-started-queries.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg)

**프로필 시작**

Journey Optimizer에서 실시간 고객 프로필이 작동하는 방식과 Platform UI에서 개별 고객 프로필을 탐색, 조사, 확인하는 방법을 살펴봅니다.

[자세히 알아보기](../audience/get-started-profiles.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

**데이터 설정 개요 튜토리얼**

Journey Optimizer에서 데이터 설정을 시작하는 초보자를 위한 비디오 가이드로, 스키마, 데이터 세트, 소스를 포괄적으로 다룹니다.

[튜토리얼 보기](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/tutorials/data-management/set-up-data-overview){target="_blank"}
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

**데이터 세트 생성 및 데이터 수집 튜토리얼**

이 실습 튜토리얼은 Adobe Experience Platform에서 데이터 세트를 생성하고 소스 커넥터를 사용하여 데이터를 수집하는 방법을 단계별로 보여주어, 사용자 샌드박스 환경에서 따라할 수 있습니다.

[튜토리얼 보기](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/tutorials/data-management/create-datasets-and-ingest-data){target="_blank"}
:::

::::
