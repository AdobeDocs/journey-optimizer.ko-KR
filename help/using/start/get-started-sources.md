---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer의 소스 커넥터 사용 시작하기
description: Adobe Journey Optimizer에서 외부 소스의 데이터를 수집하는 방법을 알아봅니다.
feature: Integrations, Data Ingestion
role: User
level: Beginner
exl-id: 359ea3c6-7746-469e-8a24-624f9726f2d8
source-git-commit: 52b58d18cdbbff79f4dcb7af2817b178a4a0b429
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 11%

---

# 소스 커넥터 시작하기 {#sources-gs}

## 소스란 무엇입니까? {#what-is-source}

**source**&#x200B;은(는) 외부 데이터를 Adobe Journey Optimizer으로 가져오는 커넥터입니다. 소스를 사용하면 CRM 플랫폼, 클라우드 스토리지 또는 데이터베이스와 같이 이미 사용하는 시스템에서 고객 정보를 가져와 해당 데이터를 개인화된 고객 여정 생성에 사용할 수 있습니다.

소스를 Journey Optimizer과 외부 데이터 시스템 간의 브리지로 간주합니다. 이들은 자동으로 데이터를 동기화하므로 마케팅 캠페인을 지원하기 위한 최신 고객 정보가 항상 제공됩니다.

## 소스가 중요한 이유 {#why-sources-matter}

소스는 Journey Optimizer에서 개인화된 데이터 기반 고객 경험을 만드는 데 필수적입니다. 이유는 다음과 같습니다.

* **통합 고객 보기** - 여러 시스템의 데이터를 결합하여 각 고객의 전체 그림을 봅니다.
* **실시간 개인화** - 새로운 데이터를 사용하여 여정에서 적절한 메시지를 적시에 전달합니다.
* **자동화된 데이터 동기화** - 수동으로 데이터를 가져오지 않고 고객 정보를 최신 상태로 유지합니다.
* **효율적인 워크플로** - 한 번 연결하면 데이터가 자동으로 여정으로 이동합니다.

예를 들어 소스를 사용하여 전자 상거래 플랫폼에서 구매 내역을 가져온 다음, 고객이 구매한 항목을 기반으로 개인화된 제품 추천을 전송하는 여정을 만들 수 있습니다.

## 소스를 사용하여 수행할 수 있는 작업 {#sources-use-cases}

Journey Optimizer의 소스에 대한 일반적인 사용 사례는 다음과 같습니다.

* **CRM 시스템에서 고객 데이터 가져오기** - Salesforce 또는 Microsoft Dynamics 같은 플랫폼에서 연락처 정보, 환경 설정 및 참여 기록을 동기화합니다.
* **구매 데이터 연결** - 전자 상거래 플랫폼의 주문 내역과 제품 환경 설정을 가져와 오퍼를 개인화합니다
* **충성도 프로그램 데이터 통합** - 액세스 포인트 잔액과 계층 정보를 통해 가장 많이 참여하는 고객에게 보상 제공
* **동작 데이터 동기화** - 웹 사이트 상호 작용 및 앱 사용 패턴을 가져와서 관련 여정을 트리거합니다.
* **프로필 특성 업데이트** - 클라우드 저장소 또는 데이터베이스의 데이터로 고객 프로필을 최신 상태로 유지

## 일반 소스 유형 {#source-types}

Journey Optimizer은 기존 시스템과 연결할 수 있는 다양한 유형의 소스를 지원합니다.

**Adobe 응용 프로그램:**
* Adobe Analytics
* Adobe Audience Manager
* Adobe Campaign
* Adobe Commerce

**클라우드 저장소:**
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

➡️ [Experience Platform 소스 카탈로그](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html#sources-catalog){target="_blank"}의 전체 목록 보기

## 시작하기에 앞서 {#prerequisites}

소스를 구성하기 전에 다음을 확인하십시오.

* **적절한 권한** - Adobe Experience Platform에서 소스를 관리하기 위한 액세스 권한
* **Source 시스템 자격 증명** - 연결할 외부 시스템에 대한 인증 세부 정보
* **데이터 이해** - 필요한 데이터 필드와 Journey Optimizer 프로필에 매핑되는 방법 알아보기

➡️ [액세스 제어 및 사용 권한에 대해 알아보기](../../administration/permissions.md)

## 소스 작동 방식 {#how-sources-work}

Adobe Journey Optimizer은 Adobe Experience Platform의 소스 프레임워크를 사용합니다. 기본 워크플로우는 다음과 같습니다.

1. **연결** - 외부 데이터 시스템에 대한 인증 설정
2. **데이터 선택** - 가져올 데이터와 동기화 빈도를 선택합니다.
3. **필드 매핑** - 외부 데이터 필드가 Journey Optimizer 프로필 특성에 대응하는 방법을 정의합니다.
4. **일정** - 자동 데이터 새로 고침 간격 설정
5. **모니터링** - 데이터 흐름을 추적하고 모든 동기화 문제를 해결합니다.

소스가 구성되면 백그라운드에서 자동으로 실행되어 고객 데이터를 최신 상태로 유지하고 여정에서 사용할 수 있도록 준비됩니다.

## 자세히 알아보기 {#learn-more}

![](assets/sources-home.png)

이 비디오를 통해 Journey Optimizer에서 소스 커넥터와 소스 커넥터를 구성하는 방법을 이해하십시오.

>[!VIDEO](https://video.tv.adobe.com/v/335919?quality=12)

소스 구성 및 관리에 대한 자세한 내용은 [Adobe Experience Platform 소스 설명서](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html?lang=ko){target="_blank"}를 참조하세요.

## 다음 단계 {#next-steps}

이제 소스가 무엇인지, 왜 중요한 것인지 이해하게 되었습니다.

* [소스 카탈로그](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html#sources-catalog){target="_blank"}를 탐색하여 시스템에 대한 커넥터를 찾으십시오.
* [소스 연결을 만드는 방법](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/overview.html){target="_blank"} 알아보기
* [데이터 매핑 및 변환 이해](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/dataflow/overview.html){target="_blank"}
* [여정에서 가져온 데이터를 사용하는 방법](../building-journeys/journey-gs.md)을 참조하세요.
