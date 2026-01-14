---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer의 소스 커넥터 사용 시작하기
description: Adobe Journey Optimizer에서 외부 소스의 데이터를 수집하는 방법을 알아봅니다.
feature: Integrations, Data Ingestion
role: User
level: Beginner
exl-id: 359ea3c6-7746-469e-8a24-624f9726f2d8
source-git-commit: 7864012ad148c2e52bc38598016e7bd7fac9644e
workflow-type: ht
source-wordcount: '584'
ht-degree: 100%

---

# 소스 커넥터 시작하기 {#sources-gs}

## 소스란 무엇인가요? {#what-is-source}

**소스**&#x200B;는 외부 데이터를 Adobe Journey Optimizer로 가져오는 커넥터입니다. 소스 기능을 사용하면 CRM 플랫폼, 클라우드 스토리지 또는 데이터베이스와 같이 이미 사용 중인 시스템에서 고객 정보를 가져와 개인화된 고객 여정을 생성하는 데 사용할 수 있습니다.

소스는 Journey Optimizer와 외부 데이터 시스템을 연결하는 다리라고 생각하면 됩니다. 소스는 데이터를 자동으로 동기화하여 마케팅 캠페인에 필요한 최신 고객 정보를 항상 확보할 수 있도록 도와줍니다.

## 소스가 중요한 이유 {#why-sources-matter}

Journey Optimizer에서 데이터 기반의 개인화된 고객 경험을 구축하려면 소스가 필수적입니다. 그 이유는 다음과 같습니다.

* **통합 고객 뷰** - 여러 시스템의 데이터를 결합하여 각 고객에 대한 완전한 정보를 확인합니다.
* **실시간 개인화** - 최신 데이터를 활용하여 여정 전반에서 시의적절하고 관련성 있는 메시지를 전달합니다.
* **자동화된 데이터 동기화** - 수동으로 데이터를 가져오지 않고 고객 정보를 최신 상태로 유지합니다.
* **효율적인 워크플로** - 한 번만 연결하면 데이터가 여정에 자동으로 입력됩니다.

예를 들어, 소스를 사용하여 전자 상거래 플랫폼에서 구매 내역을 가져온 다음, 고객이 구매한 상품을 기반으로 개인화된 제품 추천을 보내는 여정을 만들 수 있습니다.

## 소스를 사용하여 수행할 수 있는 작업 {#sources-use-cases}

Journey Optimizer에서 소스를 사용하는 일반적인 사례는 다음과 같습니다.

* **CRM 시스템에서 고객 데이터 가져오기** - Salesforce 또는 Microsoft Dynamics와 같은 플랫폼에서 연락처 정보, 선호도 및 참여 기록을 동기화합니다.
* **구매 데이터 연결** - 전자 상거래 플랫폼에서 주문 내역과 제품 선호도를 가져와 맞춤형 오퍼를 제공합니다.
* **충성도 프로그램 데이터 통합** - 포인트 잔액과 등급 정보를 활용하여 가장 적극적인 고객에게 보상을 제공합니다.
* **행동 데이터 동기화** - 웹 사이트 상호 작용과 앱 사용 패턴을 가져와 관련 여정을 트리거합니다.
* **프로필 속성 업데이트** - 클라우드 스토리지 또는 데이터베이스의 데이터를 사용하여 고객 프로필을 최신 상태로 유지합니다.

## 일반 소스 유형 {#source-types}

Journey Optimizer는 기존 시스템과 연결하기 위해 다양한 유형의 소스를 지원합니다.

**Adobe 애플리케이션:**
* Adobe Analytics
* Adobe Audience Manager
* Adobe Campaign
* Adobe Commerce

**클라우드 스토리지:**
* Amazon S3
* Azure Blob 스토리지
* Google 클라우드 스토리지
* SFTP

**데이터베이스:**
* Amazon Redshift
* Google BigQuery
* Microsoft SQL Server
* MySQL
* PostgreSQL

**CRM 및 마케팅 자동화:**
* Microsoft Dynamics
* Salesforce
* Salesforce Marketing Cloud

➡️ 전체 목록은 [Experience Platform 소스 카탈로그](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html?lang=ko#sources-catalog){target="_blank"}에서 확인하세요.

## 시작하기에 앞서 {#prerequisites}

소스를 구성하기 전에 다음을 확인해야 합니다.

* **적절한 권한** - Adobe Experience Platform에서 소스를 관리할 수 있는 액세스 권한
* **소스 시스템 자격 증명** - 연결할 외부 시스템에 대한 인증 세부 정보
* **데이터 이해** - 필요한 데이터 필드와 해당 필드가 Journey Optimizer 프로필에 매핑되는 방식 알아보기

➡️ [액세스 제어 및 권한에 대해 알아보기](../administration/permissions.md)

## 소스 작동 방식 {#how-sources-work}

Adobe Journey Optimizer는 Adobe Experience Platform의 소스 프레임워크를 사용합니다. 기본 워크플로는 다음과 같습니다.

1. **연결** - 외부 데이터 시스템에 대한 인증을 설정합니다.
2. **데이터 선택** - 가져올 데이터와 동기화 빈도를 선택합니다.
3. **필드 매핑** - 외부 데이터 필드가 Journey Optimizer 프로필 속성에 어떻게 대응하는지 정의합니다.
4. **예약** - 자동 데이터 새로 고침 간격을 설정합니다.
5. **모니터링** - 데이터 흐름을 추적하고 모든 동기화 문제를 해결합니다.

구성이 완료되면 소스는 백그라운드에서 자동으로 실행되어 고객 데이터를 최신 상태로 유지하고 여정에서 바로 사용할 수 있도록 준비합니다.

## 자세히 알아보기 {#learn-more}

![](assets/sources-home.png)

이 비디오를 시청하여 소스 커넥터와 Journey Optimizer에서 소스 커넥터를 구성하는 방법을 알아보세요.

>[!VIDEO](https://video.tv.adobe.com/v/3422585?captions=kor&quality=12)

소스 구성 및 관리에 대한 자세한 내용은 [Adobe Experience Platform 소스 설명서](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html?lang=ko){target="_blank"}를 참조하세요.

## 다음 단계 {#next-steps}

이제 소스가 무엇이며 왜 중요한지 이해하셨으니 다음 작업을 수행해 보세요.

* 시스템에 적합한 커넥터를 찾으려면 [소스 카탈로그](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html?lang=ko#sources-catalog){target="_blank"} 확인
* [소스 연결을 생성](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/overview.html?lang=ko){target="_blank"}하는 방법 알아보기
* [데이터 매핑 및 변환](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/dataflow/overview.html?lang=ko){target="_blank"} 이해
* [가져온 데이터를 여정에 사용하는 방법](../building-journeys/journey-gs.md) 참조
