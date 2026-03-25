---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer에서 데이터 관리 시작
description: 주요 개념, 설정 단계 및 보호 기능을 포함하여 데이터가 Adobe Journey Optimizer으로 들어오고 나가는 방법을 알아봅니다.
feature: Data Management
role: Developer, Admin, User
level: Beginner, Intermediate
exl-id: 25519acb-a017-446a-992b-653d3a8a3d96
source-git-commit: 89d575834871a5c55bfce75511083b4b651301b8
workflow-type: tm+mt
source-wordcount: '2444'
ht-degree: 1%

---


# 데이터 관리 시작 {#about-data}

데이터는 [!DNL Adobe Journey Optimizer]과(와) 함께 제공하는 모든 여정, 의사 결정 및 메시지의 기초입니다.

이 페이지에서는 다음 사항을 이해할 수 있는 실용적인 시작점을 제공합니다.

* Journey Optimizer에서 사용하는 핵심 데이터 빌딩 블록(스키마, 데이터 세트, ID, 프로필)
* Journey Optimizer에서 Adobe Experience Platform 데이터를 사용하는 방법
* 여정 및 캠페인을 빌드하기 전에 팀이 완료해야 하는 데이터 설정 단계
* 자세한 구성 및 모범 사례를 보려면 다음 단계로 이동하십시오.

이 안내서를 데이터 엔지니어, 관리자 및 마케터와 함께 사용하면 모든 사람이 데이터가 Journey Optimizer으로 들어오고 나가는 방식에 대한 일반적인 그림을 공유할 수 있습니다.

>[!TIP]
>Journey Optimizer에서 데이터 관리를 처음 사용하십니까? 스키마, 데이터 세트 및 소스에 대한 실용적이고 초보자 친화적인 설명을 보려면 [데이터 설정 개요 튜토리얼](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/data-management/set-up-data-overview){target="_blank"}을 시청하십시오.

## Journey Optimizer에서 Adobe Experience Platform 데이터를 사용하는 방법 {#aep-data}

[!DNL Adobe Journey Optimizer]이(가) [!DNL Adobe Experience Platform]에 작성되었습니다. 별도의 격리된 데이터 저장소는 유지 관리하지 않습니다. 대신 다른 Experience Cloud 애플리케이션과 동일한 데이터 기반을 사용합니다.

스키마 및 데이터 세트는 Adobe Experience Platform에 있습니다. ID 및 [실시간 고객 프로필](../audience/get-started-profiles.md)은(는) Identity Service 및 Profile Service에서 관리합니다. Journey Optimizer은 Adobe Experience Platform에서 프로필 및 이벤트 데이터를 읽어 여정 조건을 평가하고 메시지를 개인화하고 오퍼를 선택합니다. 전송, 열기, 클릭 및 바운스 이벤트와 여정 단계 이벤트와 같은 상호 작용 데이터를 Experience Platform 데이터 세트에 다시 기록합니다. 또한 런타임 시 프로필에 해당 데이터를 복사하지 않고 추가 데이터 세트를 조회할 수도 있습니다.

>[!TIP]
>Adobe Experience Platform을 중앙 데이터 레이어로 생각하고 Journey Optimizer을 해당 공유 데이터 기반을 사용하여 여정 및 메시지를 오케스트레이션하는 애플리케이션으로 생각해 보십시오.

➡️ [Journey Optimizer 아키텍처에 대해 자세히 알아보기](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/essentials/understanding-ajo#architecture-details){target="_blank"}

## Journey Optimizer의 주요 데이터 개념 {#key-concepts}

Journey Optimizer에서 데이터를 사용하여 작업할 때 몇 가지 관련 개념이 접하게 됩니다. 아래 표는 빠른 개요를 제공합니다. 다음 섹션에서는 각 개념을 자세히 설명합니다.

| 개념 | 정의 | Journey Optimizer의 주요 사용 |
|---|---|---|
| XDM 스키마 | 데이터(클래스 + 필드 그룹으로 구축됨)를 나타내고, 유효성을 검사하고, 형식을 지정하는 규칙 | 모델 프로필 속성 및 행동 이벤트 |
| 데이터 세트 | 스키마를 따르는 데이터의 저장소 테이블 | 프로필, 이벤트 및 시스템 생성 데이터 일시 중단 |
| Source 커넥터 | 외부 시스템의 데이터를 AEP으로 스트리밍 또는 일괄 처리 | CRM, 분석 및 웹 데이터 수집 |
| 데이터 소스 | 여정 내부에 AEP 또는 외부 필드 표시 | 고급 여정 조건 및 메시지 개인화 |
| ID | 개별 고객을 고유하게 나타내는 식별자 | 채널 간 프로필 결합 |
| 조회 데이터 세트 | 프로필 저장소 없이 AEP 데이터에 대한 런타임 참조 | 라이브 참조 데이터를 사용하여 메시지 강화 |

### 스키마(XDM 스키마) {#schema}

스키마는 데이터를 나타내고, 유효성을 검사하고, 형식을 지정하는 규칙 세트입니다. 기본 동작을 정의하는 **class**(레코드 또는 시계열)과 선택적 **필드 그룹**(특정 필드를 추가)으로 구성됩니다. 스키마는 XDM(Experience Data Model) 표준을 사용하여 정의되며 Adobe Experience Platform에서 활성화됩니다.

XDM은 실제 문제를 해결하기 위해 존재합니다. 동일한 개념(고객, 구매, 제품)을 소스 시스템에서 다르게 이름 지정하고 구조화합니다. XDM은 데이터의 출처에 관계없이 단일 정의에서 이러한 개념을 통합하는 공유 언어를 제공합니다. 이렇게 하면 Journey Optimizer이 CRM, 웹 사이트, 모바일 앱 및 데이터 웨어하우스의 데이터로 동시에 일관되게 작업할 수 있습니다.

Journey Optimizer에서는 일반적으로 고객 특성(이름, 환경 설정, 동의)에 대한 **XDM 개별 프로필** 스키마와 동작 이벤트(구매, 페이지 보기, 등록)에 대한 **XDM ExperienceEvent** 스키마로 작업합니다.

➡️ [스키마에 대해 자세히 알아보기](get-started-schemas.md)

### 데이터 세트 {#dataset}

데이터 집합은 스키마를 준수하는 데이터의 저장 및 관리 구성입니다. 열 및 행 집합이 정의된 테이블로 간주합니다. Journey Optimizer에서 사용하는 모든 데이터는 Adobe Experience Platform 데이터 세트에 저장됩니다. 이는 프로필 데이터 세트(실시간 고객 프로필에 기여), 이벤트 데이터 세트(여정 및 분석을 위해 행동 데이터 저장) 또는 Journey Optimizer에서 추적, 피드백 및 여정 단계 이벤트를 위해 자동으로 만든 시스템 데이터 세트일 수 있습니다.

➡️ [데이터 세트에 대해 자세히 알아보기](get-started-datasets.md)

### Source 커넥터 {#source-connector}

소스 커넥터(**source**)는 Adobe Analytics, Adobe Experience Platform Web SDK, 클라우드 저장소(S3, Azure Blob) 또는 CRM 데이터베이스와 같은 여러 시스템의 데이터를 Adobe Experience Platform으로 수집하는 데 도움이 됩니다. 원시 수집 외에도 커넥터는 XDM 스키마에 대한 필드 매핑 및 데이터 거버넌스 레이블 지정을 포함하여 Experience Platform 서비스를 사용하여 데이터의 구조, 레이블 지정 및 개선을 활성화합니다.

➡️ [소스 커넥터에 대해 자세히 알아보기](../start/get-started-sources.md)

### 데이터 소스(Journey Optimizer) {#data-source}

Journey Optimizer의 데이터 소스는 Adobe Experience Platform(또는 외부 API)의 필드 중 여정 및 메시지 내에 노출되는 필드를 정의합니다. Journey Optimizer UI에서 구성되는 데이터 소스에는 일반적으로 내장된 Adobe Experience Platform 데이터 소스(실시간 고객 프로필 속성 및 이벤트 노출) 및 추가적인 데이터 강화를 위해 여정 런타임 시 호출되는 선택적 외부 또는 사용자 지정 데이터 소스가 포함됩니다. 여정 조건, 사용자 지정 작업 및 메시지 개인화에 사용됩니다.

➡️ [데이터 원본에 대해 자세히 알아보기](../datasource/about-data-sources.md)

>[!NOTE]
>[Adobe Experience Platform 용어집](https://experienceleague.adobe.com/en/docs/experience-platform/landing/glossary){target="_blank"}은(는) &quot;데이터 소스&quot;를 일반적으로 데이터 원본(CRM, 모바일 앱 등)으로 정의합니다. Journey Optimizer에서 **데이터 원본**&#x200B;은(는) 여정 및 메시지 내에 노출되는 필드를 제어하는 UI 구성이라는 특정한 의미를 갖습니다.

### ID 및 실시간 고객 프로필 {#identity}

ID는 쿠키 ID, 장치 ID, 이메일 주소 또는 CRM ID와 같이 개별 고객을 고유하게 나타내는 식별자입니다. ID는 네임스페이스(이메일, ECID, CRMID)로 구성되며, 동일한 사용자에 대한 여러 ID가 통합 ID 그래프에 결합됩니다. 실시간 고객 프로필은 이 그래프를 사용하여 온라인, 오프라인, CRM 및 서드파티 소스를 비롯한 여러 채널의 데이터를 결합하여 각 개별 고객에 대한 거시적인 보기를 유지합니다.

초보자를 위한 주요 개념은 **프로필 조각** 모델입니다. 고객이 특정 장치 또는 채널(웹 사이트, 모바일 앱, 스토어)에서 브랜드와 상호 작용할 때마다 해당 상호 작용은 프로필 조각으로 기록됩니다. 해당 특정 터치포인트를 기반으로 하는 해당 고객의 부분 보기입니다. Real-Time Customer Profile은 공유 ID 값을 기반으로 이러한 조각을 지속적으로 결합함으로써 완전한 최신 프로필을 빌드합니다. Journey Optimizer은 어셈블된 이 프로필에서 를 읽어 조건을 평가하고 오퍼를 선택하며 실시간으로 메시지를 개인화합니다.

➡️ [Journey Optimizer의 ID에 대해 자세히 알아보기](../audience/get-started-identity.md)

### 조회 데이터 세트 {#lookup-dataset}

조회 데이터 세트를 사용하면 Journey Optimizer이 실시간 고객 프로필에 데이터를 저장하지 않고 Adobe Experience Platform 데이터 세트에서 런타임에 참조 또는 트랜잭션 데이터를 검색할 수 있습니다. 이 기능은 메시지 시간에 필요하지만 프로필에 속하지 않는 참조 데이터(가격, 인벤토리, 저장 시간) 또는 트랜잭션 데이터를 자주 변경하는 데 유용합니다. Journey Optimizer은 제품 ID와 같은 키를 기반으로 여정 또는 메시지 실행 중에 조회를 수행합니다.

➡️ [조회 데이터 세트에 대해 자세히 알아보기](lookup-aep-data.md)

## 데이터 준비 체크리스트 {#checklist}

마케터가 여정 및 캠페인 빌드를 시작하기 전에 조직에서 일련의 데이터 준비 단계를 완료해야 합니다. 이렇게 하면 Journey Optimizer이 적절한 시간과 호환 방식으로 올바른 데이터를 사용할 수 있습니다.

>[!NOTE]
>아래 단계에는 데이터 엔지니어, 관리자 및 마케터의 여러 역할이 포함됩니다. 이 체크리스트를 공유 플랜으로 사용하여 환경을 준비합니다. 1~4단계는 Adobe Experience Platform에서 완료되고 5~6단계는 Journey Optimizer에서 구성됩니다.

아래 6개 단계에서는 ID 구성에서 데이터가 Journey Optimizer으로 올바르게 유입되는지 확인까지의 전체 데이터 설정 프로세스를 안내합니다.

1. ID 전략 정의
1. 프로필 및 이벤트 데이터를 위한 스키마 디자인
1. 프로필이 활성화된 데이터 세트 만들기
1. 소스에서 데이터 수집
1. Journey Optimizer에서 데이터 소스 구성
1. 추적, 피드백 및 여정 데이터 세트 확인

+++ ID 전략 정의

고객을 위한 기본 ID(예: ECID, 이메일 또는 CRMID)를 선택하고 Adobe Experience Platform ID 서비스에서 해당 네임스페이스를 구성합니다. 프로필 활성화 스키마에 ID 필드가 있는지 확인하고 프로필이 ID 그래프에 올바르게 결합되었는지 확인하십시오.

➡️ [Journey Optimizer의 ID에 대해 자세히 알아보기](../audience/get-started-identity.md)

+++

+++ 프로필 및 이벤트 데이터를 위한 스키마 디자인

**XDM 개인 프로필** 스키마를 만들어 이름 및 연락처 정보, 환경 설정 및 관심 분야, 라이프사이클 단계 또는 동의 상태와 같은 고객 특성을 캡처합니다. **XDM ExperienceEvent** 스키마를 만들어 웹 및 앱 이벤트, 구매 및 오프라인 상호 작용과 같은 동작 및 트랜잭션 데이터를 캡처합니다. 적절한 경우 올바른 필드를 ID 및 프로필 속성으로 표시합니다.

➡️ [스키마에 대해 자세히 알아보기](get-started-schemas.md)

+++

+++ 프로필이 활성화된 데이터 세트 만들기

Adobe Experience Platform에서 XDM 스키마를 기반으로 데이터 세트를 만들고 실시간 고객 프로필에 기여해야 하는 모든 데이터 세트에서 프로필을 활성화합니다. Journey Optimizer에서 만든 시스템 생성 데이터 세트가 데이터 세트 작업 공간에 표시되는지 확인합니다.

➡️ [데이터 세트에 대해 자세히 알아보기](get-started-datasets.md)

+++

+++ 소스에서 데이터 수집

Adobe Analytics, Adobe Experience Platform Web SDK 또는 CRM 및 POS 플랫폼과 같은 엔터프라이즈 시스템에 대한 소스 커넥터를 구성하고 들어오는 필드를 XDM 스키마에 매핑합니다. 데이터가 올바른 데이터 세트에 도달하고 예상되는 경우 실시간 고객 프로필에 표시되는지 확인합니다.

➡️ [소스 커넥터에 대해 자세히 알아보기](../start/get-started-sources.md)

➡️ [자습서: 데이터 집합 만들기 및 데이터 수집](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/data-management/create-datasets-and-ingest-data){target="_blank"}

+++

+++ Journey Optimizer에서 데이터 소스 구성

데이터 소스는 Journey Optimizer에 고유한 개념입니다. 데이터가 있는 위치가 아니라 여정 및 메시지 실행 중에 Journey Optimizer에서 읽을 수 있는 필드를 선언하는 위치입니다. 여정이 &quot;고객이 충성도 멤버입니까?&quot;와 같은 조건을 평가하기 전에 또는 이름을 사용하여 메시지를 개인화하려면 데이터 소스 구성을 통해 관련 프로필 필드를 노출해야 합니다.

Journey Optimizer에는 실시간 고객 프로필 특성에 직접 액세스할 수 있는 기본 제공 [Adobe Experience Platform 데이터 소스](../datasource/adobe-experience-platform-data-source.md)가 포함되어 있습니다. 여기에는 개인화를 위한 프로필 속성 읽기 또는 동의 및 환경 설정 필드 확인과 같은 대부분의 사용 사례가 포함됩니다. 여정 런타임 시 서드파티 API를 호출하도록 [외부 데이터 소스](../datasource/external-data-sources.md)를 구성할 수도 있습니다. 예를 들어, 실시간 충성도 점수, 제품 추천 또는 Adobe Experience Platform에 저장되지 않은 스토어 재고 수준을 검색할 수 있습니다.

>[!NOTE]
>기본 제공 Adobe Experience Platform 데이터 소스를 통해 경험 이벤트 데이터에 직접 액세스하는 방법은 더 이상 사용되지 않으며 점진적으로 비활성화됩니다. [자세히 알아보기](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/orchestrate-journeys/journey-use-cases/exp-event-lookup){target="_blank"}.

데이터 소스 구성은 여정 작성자 및 마케터를 위한 전체 데이터 레이어의 잠금을 해제하는 관리 작업입니다. 필드가 데이터 소스를 통해 노출되면 여정 조건 빌더, 메시지 개인화 편집기, 여정 결정 규칙에서 필드를 사용할 수 있습니다. 따라서 데이터 소스 작성 시 추가 엔지니어링 작업이 필요하지 않습니다.

➡️ [데이터 원본 구성에 대해 자세히 알아보기](../datasource/about-data-sources.md)

+++

+++ 추적, 피드백 및 여정 데이터 세트 확인

Journey Optimizer 시스템에서 생성한 데이터 세트를 데이터 세트 작업 영역에서 사용할 수 있는지 확인합니다. 테스트 여정 및 캠페인을 실행한 다음 쿼리 편집기를 사용하여 보내기, 열기, 클릭 및 바운스 이벤트가 기록되고 여정 단계 이벤트와 상태가 올바르게 캡처되는지 확인합니다. 지속적인 모니터링, 문제 해결 및 여정 최적화에 이러한 데이터 세트를 사용합니다.

➡️ [Journey Optimizer의 쿼리에 대해 자세히 알아보기](get-started-queries.md)

+++

## 보호 및 데이터 디자인 고려 사항 {#guardrails}

일부 제품 보호 기능 및 제한 사항은 데이터 모델 및 여정을 디자인하는 방식에 영향을 줄 수 있습니다. 나중에 다시 작업하지 않도록 이 내용을 일찍 검토하십시오.

>[!IMPORTANT]
>최신 정보는 항상 [Journey Optimizer 보호 및 제한 사항](../start/guardrails.md) 페이지를 참조하세요. 아래 요약은 주요 항목을 강조하지만 시간이 지남에 따라 발전할 수 있습니다.

### Journey Optimizer 시스템 데이터 세트 및 TTL {#datasets-ttl}

Journey Optimizer은 추적, 피드백 및 여정 단계 이벤트를 위한 몇 가지 시스템 생성 데이터 세트를 만듭니다. 2025년 2월부터 TTL(Time-to-Live) 가드레일이 이러한 데이터 세트 중 일부로 배포되고 있으며, 이는 분석 및 문제 해결을 위해 데이터가 유지되는 기간에 영향을 줄 수 있습니다.

➡️ [데이터 세트 TTL 가드레일에 대해 자세히 알아보기](datasets-ttl.md)

### 스트리밍 세분화 및 Journey Optimizer 이벤트 {#streaming-segmentation}

2024년 11월 1일부터 스트리밍 세그먼테이션은 더 이상 Journey Optimizer 추적 및 피드백 데이터 세트에서 전송 및 열기 이벤트를 지원하지 않습니다. 빈도 제한 및 피로도 관리와 같은 사용 사례의 경우 보내기/열기 이벤트를 기반으로 세그먼트를 스트리밍하지 않고 [비즈니스 규칙](../conflict-prioritization/rule-sets.md)을(를) 사용하십시오.

➡️ [데이터 세트에 대해 자세히 알아보기](get-started-datasets.md)

### 데이터 세트 조회 및 의사 결정 {#lookup-guardrails}

데이터 세트 조회는 자주 변경되는 속성(재고, 가격, 날씨) 또는 실시간 고객 프로필에 저장할 필요가 없는 데이터에 이상적입니다. 조회 전략을 설계하기 전에 관련 문서에서 데이터 세트 크기 제한 및 쿼리 제한 등 제품별 보호 기능을 검토하십시오.

➡️ [조회 데이터 세트에 대해 자세히 알아보기](lookup-aep-data.md)

## 예: 시작 여정을 위한 데이터 준비 {#example}

다음 예제는 간단한 시나리오에서 이 페이지의 개념이 함께 작동하는 방식을 보여 줍니다.

1. 데이터 엔지니어는 고객 특성(이름, 이메일, 충성도 계층, 동의)에 대한 [XDM 개인 프로필 스키마](get-started-schemas.md)와 웹 등록 이벤트에 대한 XDM ExperienceEvent 스키마를 만듭니다.
1. [프로필이 활성화된 데이터 세트](get-started-datasets.md)이(가) 각 스키마에 대해 만들어집니다(CRM 특성에 대해 하나, 등록 이벤트에 대해 하나).
1. 웹 및 모바일 팀은 Adobe Experience Platform Web SDK을 통해 등록 이벤트를 스트리밍합니다. CRM 데이터는 [소스 커넥터](../start/get-started-sources.md)를 통해 수집됩니다.
1. 관리자는 Journey Optimizer에서 [Adobe Experience Platform 데이터 원본](../datasource/adobe-experience-platform-data-source.md)을(를) 구성하고 `profile.person.name.firstName`, `profile.personalEmail.address` 및 `profile.loyaltyTier`과(와) 같은 필드를 표시합니다.
1. 마케터 [시작 여정을 만들고](../building-journeys/journey-gs.md) 등록 이벤트를 수신하고 해당 프로필 특성을 사용하여 [시작 전자 메일을 개인 설정](../personalization/personalize.md)합니다. Journey Optimizer은 전송 및 열기 이벤트를 추적 데이터 세트에 쓰고 여정 단계 이벤트 데이터 세트의 여정 진행률을 기록합니다.
1. 개발자는 [쿼리 편집기](get-started-queries.md)를 사용하여 이벤트가 올바르게 흐르는지 확인하고 성능(열기, 클릭 수, 보내기 시간)을 분석합니다. 팀은 이러한 통찰력을 기반으로 여정 및 콘텐츠를 조정합니다.

이 플로우는 초보자 친화적인 전체 사용 사례에서 스키마, 데이터 세트, 소스, 데이터 소스 및 쿼리가 함께 작동하는 방식을 보여 줍니다.

## 관련 리소스 {#related-resources}

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg)

**스키마 시작**

Adobe Experience Platform에서 XDM 스키마를 만들고 올바른 클래스 및 필드 그룹을 선택하고 프로필 속성 및 동작 이벤트를 모델링하는 방법에 대해 알아봅니다.

[자세히 알아보기](get-started-schemas.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg)

**데이터 세트 작업**

프로필 사용 및 이벤트 데이터 세트를 만들고, 데이터 수집을 모니터링하고, Journey Optimizer이 추적, 피드백 및 여정 단계 이벤트를 위해 자동으로 만드는 시스템 생성 데이터 세트를 탐색하는 방법을 이해합니다.

[자세히 알아보기](get-started-datasets.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg)

**데이터 소스 구성**

여정 내에 프로필 필드 및 외부 API 응답을 노출하기 위한 내장 Adobe Experience Platform 데이터 소스 및 선택적 외부 데이터 소스 설정에 대한 단계별 지침입니다.

[자세히 알아보기](../datasource/about-data-sources.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg)

**Adobe Experience Platform 데이터 사용(조회)**

실시간 고객 프로필에 저장하지 않고 AEP 데이터 세트의 참조 또는 트랜잭션 데이터를 사용하여 런타임 시 메시지를 보강하는 방법에 대해 알아봅니다.

[자세히 알아보기](lookup-aep-data.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg)

**쿼리 시작**

쿼리 서비스를 사용하여 Journey Optimizer 데이터 세트를 분석하고, 이벤트가 올바르게 흐르는지 확인하고, 데이터 보내기, 열기, 클릭 및 바운스에 대한 보고 쿼리를 빌드합니다.

[자세히 알아보기](get-started-queries.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg)

**프로필 시작**

Journey Optimizer에서 실시간 고객 프로필이 작동하는 방식과 Platform UI에서 개별 고객 프로필을 탐색, 검사 및 확인하는 방법을 살펴봅니다.

[자세히 알아보기](../audience/get-started-profiles.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

**데이터 개요 설정 자습서**

Journey Optimizer의 데이터 설정에 대한 초보자용 비디오 연습으로서 스키마, 데이터 세트 및 소스를 포괄합니다.

[자습서 보기](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/data-management/set-up-data-overview){target="_blank"}
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

**데이터 집합 만들기 및 데이터 수집 자습서**

Adobe Experience Platform에서 데이터 세트를 만들고 소스 커넥터를 사용하여 데이터를 수집하는 방법을 보여 주는 실습 튜토리얼로서, 샌드박스에서 참조할 수 있는 단계별 지침을 제공합니다.

[자습서 보기](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/data-management/create-datasets-and-ingest-data){target="_blank"}
:::

::::
