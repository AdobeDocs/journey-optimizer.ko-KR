---
solution: Journey Optimizer
product: journey optimizer
title: 데이터 엔지니어용 Journey Optimizer 시작하기
description: 데이터 엔지니어로서 Journey Optimizer로 작업하는 방법에 대해 자세히 알아보세요.
feature: Get Started
role: Developer
level: Intermediate
exl-id: 8beaafc2-e68d-46a1-be5c-e70892575bfb
source-git-commit: 5ff7987c00afda3263cb97654967c5b698f726c2
workflow-type: tm+mt
source-wordcount: '806'
ht-degree: 52%

---

# 데이터 엔지니어용 시작하기 {#data-engineer}

**Adobe Journey Optimizer 데이터 엔지니어**&#x200B;로서 고객 프로필 데이터를 준비 및 유지 관리하여 [!DNL Journey Optimizer]에서 오케스트레이션한 경험을 강화하고, 고객 및 비즈니스 데이터를 스키마로 모델링하고, 데이터 수집을 위한 소스 커넥터를 구성합니다. [시스템 관리자](administrator.md)가 액세스 권한을 부여하고 환경을 준비하면 [!DNL Adobe Journey Optimizer] 작업을 시작할 수 있습니다.

>[!NOTE]
>
>**데이터 수집**&#x200B;에 대한 자세한 내용은 [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html?lang=ko){target="_blank"}를 참조하십시오.

## 필수 데이터 구성 단계

Journey Optimizer에 대한 데이터 기반을 설정하려면 다음 단계를 따르십시오.

1. **ID 네임스페이스를 만듭니다**. Adobe [!DNL Journey Optimizer]에서 **ID**&#x200B;는 장치와 채널 전반에 걸쳐 소비자를 연결하며 결과는 ID 그래프입니다. 연결된 ID 그래프는 모든 비즈니스 접점에서 상호 작용을 기반으로 경험을 개인화하는 데 사용됩니다. [이 페이지에서](../../audience/get-started-identity.md) ID 및 ID 네임스페이스에 대해 자세히 알아보십시오.

   또한 주문 ID 또는 예약 ID와 같은 보조 식별자를 기반으로 동일한 프로필에서 여러 여정 인스턴스를 입력할 수 있도록 **보조 식별자**&#x200B;를 구성하십시오. [보조 식별자](../../building-journeys/supplemental-identifier.md)에 대해 알아봅니다.

1. **스키마를 만들고** 프로필에 대해 활성화합니다. 스키마는 데이터의 구조와 형식을 나타내고 유효성을 검사하는 규칙 세트입니다. 스키마는 높은 수준에서 실제 개체(예: 사람)에 대한 추상적인 정의를 제공하고, 해당 개체의 각 인스턴스에 포함되어야 하는 데이터(예: 이름, 성, 생일 등)에 대한 개요를 제공합니다.

   * 표준 여정 및 캠페인의 경우: [XDM 스키마](../../data/get-started-schemas.md) 사용
   * 오케스트레이션된 캠페인의 경우: [관계형 스키마](../../orchestrated/gs-schemas.md)를 만들어 다중 엔티티 세그먼테이션을 사용하도록 설정합니다.

1. **데이터 세트를 만들고** 프로필에 사용하도록 설정합니다. 데이터 세트는 스키마(열) 및 필드(행)를 포함하는 데이터 수집을 위한 저장소 및 관리 구조입니다. 데이터 세트에는 저장하는 데이터의 다양한 측면을 설명하는 메타데이터도 포함됩니다. 데이터 세트가 만들어지면 기존 스키마에 매핑하고 데이터를 추가할 수 있습니다. [이 페이지에서](../../data/get-started-datasets.md) 데이터세트에 대해 자세히 알아보십시오.

   고급 시나리오의 경우 레코드 데이터 세트의 실시간 데이터를 사용하여 여정 실행을 강화하려면 **런타임 조회를 위한 데이터 세트**&#x200B;를 준비하십시오. [데이터 집합 조회](../../building-journeys/dataset-lookup.md)에 대해 알아봅니다.

1. **소스 커넥터를 구성합니다**. Adobe Journey Optimzer를 사용하면 외부 소스에서 데이터를 수집하는 동시에 Platform 서비스를 사용하여 들어오는 데이터를 구조화하고 레이블을 지정하고 개선할 수 있습니다. Adobe 애플리케이션, 클라우드 기반 저장소, 데이터베이스 및 기타 여러 소스와 같은 다양한 소스에서 데이터를 수집할 수 있습니다. [이 페이지에서](../get-started-sources.md) 소스 커넥터에 대해 자세히 알아보십시오.

1. **테스트 프로필 만들기**. 테스트 프로필은 여정에서 [테스트 모드](../../building-journeys/testing-the-journey.md)를 사용할 때 필요하며 전송하기 전에 [메시지를 미리 보고 테스트하는 데](../../content-management/preview-test.md) 필요합니다. 테스트 프로필을 만드는 단계는 [이 페이지에서](../../audience/creating-test-profiles.md) 자세히 설명합니다.

1. **계산된 특성을 구성합니다**(선택 사항). 프로필 데이터에서 파생된 속성을 생성하여 세분화 및 개인화를 간소화합니다. 계산된 속성은 &quot;최근 90일 동안의 총 구매&quot; 또는 &quot;평균 주문 값&quot;과 같은 복잡한 지표를 자동으로 계산합니다. [계산된 특성](../../audience/computed-attributes.md)에 대해 알아봅니다.

또한 여정에서 메시지를 보내려면 **[!UICONTROL 데이터 원본]**, **[!UICONTROL 이벤트]** 및 **[!UICONTROL 작업]**&#x200B;을 구성해야 합니다. 자세한 내용은 [이 섹션](../../configuration/about-data-sources-events-actions.md)을 참조하세요.

![](../assets/admin-menu.png)

* **데이터 소스** 구성을 사용하면 여정에 사용될 추가 정보를 검색하기 위해 시스템에 대한 연결을 정의할 수 있습니다. [이 섹션에서](../../datasource/about-data-sources.md) 데이터 소스에 대해 자세히 알아보세요.

* **이벤트**&#x200B;를 사용하면 여정을 통합적으로 트리거하여 여정에 참여하는 개인에게 실시간으로 메시지를 보낼 수 있습니다. 이벤트 구성에서 여정에서 예상되는 이벤트를 구성합니다. 수신되는 이벤트 데이터는 Adobe Experience 데이터 모델(XDM)에 따라 표준화됩니다. 이벤트는 인증된 이벤트와 인증되지 않은 이벤트(예: Adobe Mobile SDK 이벤트)를 위한 수집 API 스트리밍에서 옵니다. [이 섹션에서](../../event/about-events.md) 이벤트에 대해 자세히 알아보세요.

* [!DNL Journey Optimizer]에는 메시지 기능이 기본 제공됩니다. 여정 내에서 메시지를 만들고 콘텐츠를 디자인할 수 있습니다. Adobe Campaign과 같은 타사 시스템을 사용하여 메시지를 보내는 경우 **사용자 정의 작업**&#x200B;을 만듭니다. 이 섹션[에서 ](../../action/action.md) 작업에 대해 자세히 알아보세요.

## 여정 데이터 모니터링 및 분석

여정이 실행되면 데이터 레이크에서 여정 단계 이벤트를 쿼리하여 성능을 모니터링하고, 문제를 해결하고, 고객 행동을 분석할 수 있습니다. SQL 쿼리를 사용하여 분석:

* 프로필 시작 및 종료 패턴
* 오류율 및 이유 삭제
* 대상자 내보내기 작업 성능 읽기
* 사용자 지정 작업 성능 지표
* 여정 인스턴스 상태 및 병목 현상

데이터 분석 및 문제 해결을 시작하려면 즉시 사용할 수 있는 [여정 분석에 대한 쿼리 예제](../../reports/query-examples.md)를 살펴보십시오.

## 업데이트 상태 유지

최신 Journey Optimizer 기능 및 개선 사항을 따라가십시오.

* **[릴리스 정보](../../rn/release-notes.md)**: 매월 릴리스되는 새로운 기능, 개선 사항 및 수정 사항을 검토합니다.
* **[설명서 업데이트](../../rn/documentation-updates.md)**: 새 페이지 및 업데이트된 콘텐츠를 포함하여 설명서의 최근 변경 내용을 추적합니다.
* **제품 알림**: [Adobe Experience Cloud 프로필](https://experience.adobe.com/preferences){target="_blank"}에서 알림을 활성화하여 다음에 대한 알림을 받을 수 있습니다.
   * 새로운 제품 릴리스 및 기능
   * 유지 관리 기간 및 시스템 업데이트
   * 중요 공지 및 변경 사항

  알림을 활성화하려면 Adobe Experience Cloud 오른쪽 상단의 프로필 아이콘을 클릭하고 **환경 설정 > 알림**(으)로 이동한 다음 Journey Optimizer 알림 환경 설정을 구성하십시오.
