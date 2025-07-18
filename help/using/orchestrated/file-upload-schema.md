---
solution: Journey Optimizer
product: journey optimizer
title: 구성 단계
description: DDL을 업로드하여 Adobe Experience Platform 내에서 관계형 스키마를 만드는 방법을 알아봅니다
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 88eb1438-0fe5-4a19-bfb6-2968a427e9e8
source-git-commit: 3dc0bf4acc4976ca1c46de46cf6ce4f2097f3721
workflow-type: tm+mt
source-wordcount: '872'
ht-degree: 1%

---

# DDL 파일을 사용하여 관계형 스키마 생성 {#file-upload-schema}

+++ 목차

| 오케스트레이션된 캠페인 시작 | 첫 오케스트레이션된 캠페인 시작 | 데이터베이스 쿼리 | 오케스트레이션된 캠페인 활동 |
|---|---|---|---|
| [오케스트레이션된 캠페인 시작](gs-orchestrated-campaigns.md)<br/><br/>관계형 스키마 및 데이터 세트 만들기 및 관리:</br> <ul><li>[스키마 및 데이터 세트 시작](gs-schemas.md)</li><li>[수동 스키마](manual-schema.md)</li><li>[파일 업로드 스키마](file-upload-schema.md)</li><li>[데이터 수집](ingest-data.md)</li></ul>[오케스트레이션된 캠페인 액세스 및 관리](access-manage-orchestrated-campaigns.md)<br/><br/>[오케스트레이션된 캠페인을 만드는 주요 단계](gs-campaign-creation.md) | [캠페인 만들기 및 예약](create-orchestrated-campaign.md)<br/><br/>[활동 오케스트레이션](orchestrate-activities.md)<br/><br/>[캠페인 시작 및 모니터링](start-monitor-campaigns.md)<br/><br/>[보고](reporting-campaigns.md) | [규칙 빌더로 작업](orchestrated-rule-builder.md)<br/><br/>[첫 번째 쿼리 빌드](build-query.md)<br/><br/>[표현식 편집](edit-expressions.md)<br/><br/>[재타겟팅](retarget.md) | [활동 시작](activities/about-activities.md)<br/><br/>활동:<br/>[및 가입](activities/and-join.md) - [대상 작성](activities/build-audience.md) - [차원 변경](activities/change-dimension.md) - [채널 활동](activities/channels.md) - [결합](activities/combine.md) - [중복 제거](activities/deduplication.md) - [데이터 보강](activities/enrichment.md) - [포크](activities/fork.md) - [조정](activities/reconciliation.md) - [대상 저장](activities/save-audience.md) - [분할](activities/split.md) - [대기](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

</br>

이 페이지의 컨텐츠는 최종본이 아니며, 변경될 수 있습니다.

>[!ENDSHADEBOX]

**충성도 멤버십**, **충성도 트랜잭션** 및 **충성도 보상**&#x200B;과 같은 스키마를 만들어 오케스트레이션된 캠페인에 필요한 관계형 데이터 모델을 정의합니다. 각 스키마에는 기본 키, 버전 관리 특성 및 **수신자** 또는 **브랜드**&#x200B;와 같은 참조 엔터티에 대한 적절한 관계가 포함되어야 합니다.

스키마를 인터페이스를 통해 수동으로 생성하거나 DDL 파일을 사용하여 일괄로 가져올 수 있습니다.

이 섹션에서는 DDL(데이터 정의 언어) 파일을 업로드하여 Adobe Experience Platform 내에서 관계형 스키마를 생성하는 방법에 대한 단계별 지침을 제공합니다. DDL 파일을 사용하면 테이블, 속성, 키 및 관계를 포함하여 데이터 모델의 구조를 미리 정의할 수 있습니다.

1. [DDL 파일을 업로드](#ddl-upload)하여 관계형 스키마를 만들고 구조를 정의합니다.

1. 데이터 모델의 테이블 간 [관계를 정의](#relationships)합니다.

1. [스키마를 연결](#link-schema)하여 받는 사람 또는 브랜드와 같은 기존 프로필 엔터티와 관계형 데이터를 연결합니다.

1. [지원되는 소스에서 데이터 집합에 데이터 수집](ingest-data.md).

## DDL 파일 업로드{#ddl-upload}

DDL 파일을 업로드하여 테이블, 속성, 키, 관계 등 데이터 모델의 구조를 미리 정의할 수 있습니다.

1. Adobe Experience Platform에 로그인.

1. **데이터 관리** > **스키마** 메뉴로 이동합니다.

1. **스키마 만들기**&#x200B;를 클릭합니다.

1. **[!UICONTROL 관계형]**&#x200B;을(를) **스키마 형식**(으)로 선택합니다.

   ![](assets/admin_schema_1.png)

1. 엔터티 관계 다이어그램을 정의하고 스키마를 만들려면 **[!UICONTROL DDL 파일 업로드]**&#x200B;를 선택하십시오.

   테이블 구조에는 다음이 포함되어야 합니다.
   * 하나 이상의 기본 키
   * `lastmodified` 또는 `datetime` 형식의 `number` 필드와 같은 버전 식별자입니다.

1. DDL 파일을 끌어다 놓고 **[!UICONTROL 다음]**&#x200B;을(를) 클릭합니다.

1. **[!UICONTROL 스키마 이름]**&#x200B;을(를) 입력하십시오.

1. 기본 키가 지정되도록 각 스키마와 해당 열을 설정합니다.

   `lastmodified`과(와) 같은 특성 하나를 버전 설명자로 지정해야 합니다. 일반적으로 `datetime`, `long` 또는 `int` 유형의 이 특성은 데이터 집합이 최신 데이터 버전으로 업데이트되도록 수집 프로세스에 필수적입니다.

   ![](assets/admin_schema_2.png)

1. 완료되면 **[!UICONTROL 완료]**&#x200B;를 클릭하세요.

이제 캔버스 내에서 테이블 및 필드 정의를 확인할 수 있습니다. [아래 섹션에서 자세히 알아보기](#entities)

## 관계 정의 {#relationships}

스키마 내의 테이블 간에 논리적 연결을 정의하려면 아래 단계를 따르십시오.

1. 데이터 모델의 캔버스 보기에 액세스하고 연결할 두 테이블을 선택합니다

1. Source 조인 옆에 있는 ![](assets/do-not-localize/Smock_AddCircle_18_N.svg) 단추를 클릭한 다음 화살표를 드래그하여 Target 조인 방향으로 안내하여 연결을 설정합니다.

   ![](assets/admin_schema_5.png)

1. 지정된 양식을 입력하여 링크를 정의하고 구성된 후 **적용**&#x200B;을 클릭합니다.

   ![](assets/admin_schema_3.png)

   **카디널리티**:

   * **1-N**: 원본 테이블의 발생 항목 하나는 대상 테이블의 여러 발생 항목을 가질 수 있지만, 대상 테이블의 발생 항목 하나는 원본 테이블의 해당 발생 항목을 최대 한 개까지 가질 수 있습니다.

   * **N-1**: 대상 테이블의 발생 항목 하나는 원본 테이블의 여러 발생 항목을 가질 수 있지만, 원본 테이블의 발생 항목 하나는 대상 테이블의 해당 발생 항목을 최대 한 개까지 가질 수 있습니다.

   * **1-1**: 원본 테이블의 발생 항목 하나는 대상 테이블의 해당 발생 항목을 최대 한 개까지 가질 수 있습니다.

1. 데이터 모델에 정의된 모든 링크는 캔버스 보기에서 화살표로 표시됩니다. 세부 정보를 보거나, 편집하거나, 필요에 따라 링크를 제거하려면 두 테이블 사이의 화살표를 클릭합니다.

   ![](assets/admin_schema_6.png)

1. 도구 모음을 사용하여 캔버스를 사용자 정의하고 조정합니다.

   ![](assets/toolbar.png)

   * **확대**: 데이터 모델의 세부 정보를 더 명확하게 보려면 캔버스를 확대하십시오.

   * **축소**: 데이터 모델을 더 넓게 보려면 캔버스 크기를 줄이십시오.

   * **보기 맞춤**: 표시 영역 내의 모든 스키마에 맞게 확대/축소를 조정합니다.

   * **필터**: 캔버스 내에 표시할 스키마를 선택합니다.

   * **자동 레이아웃 강제 적용**: 더 나은 조직을 위해 스키마를 자동으로 정렬합니다.

   * **맵 표시**: 미니맵 오버레이를 전환하여 크거나 복잡한 스키마 레이아웃을 보다 쉽게 탐색할 수 있도록 합니다.

1. 완료되면 **저장**&#x200B;을 클릭하세요. 이 작업은 스키마 및 관련 데이터 세트를 만들고 오케스트레이션된 캠페인에서 사용할 데이터 세트를 활성화합니다.

1. **[!UICONTROL 작업 열기]**&#x200B;를 클릭하여 만들기 작업의 진행 상황을 모니터링합니다. 이 프로세스는 DDL 파일에 정의된 테이블 수에 따라 몇 분 정도 걸릴 수 있습니다.

   ![](assets/admin_schema_4.png)

## 스키마 연결 {#link-schema}

**충성도 트랜잭션** 스키마와 **수신자** 스키마 간의 관계를 설정하여 각 트랜잭션을 올바른 고객 레코드와 연결합니다.

1. **[!UICONTROL 스키마]**(으)로 이동하여 이전에 만든 **충성도 트랜잭션**&#x200B;을(를) 엽니다.

1. 고객 **[!UICONTROL 필드 속성]**&#x200B;에서 **[!UICONTROL 관계 추가]**&#x200B;를 클릭합니다.

   ![](assets/schema_1.png)

1. **[!UICONTROL 다대일]**&#x200B;을(를) 관계 **[!UICONTROL 유형]**(으)로 선택합니다.

1. 기존 **수신자** 스키마에 대한 링크입니다.

   ![](assets/schema_2.png)

1. **[!UICONTROL 현재 스키마의 관계 이름]** 및 **[!UICONTROL 참조 스키마의 관계 이름]**&#x200B;을 입력하십시오.

1. 변경 내용을 저장하려면 **[!UICONTROL 적용]**&#x200B;을 클릭하세요.

계속해서 **충성도 보상** 스키마와 **브랜드** 스키마 간의 관계를 만들어 각 보상 항목을 적절한 브랜드와 연결합니다.

![](assets/schema_3.png)


<!--### Setting Up Change data capture ingestion {#cdc-ingestion}

If you need to change the data source, you must delete the existing dataflow and create a new one pointing to the same dataset with the new source.

When using Change Data Capture (CDC), it is essential that the source and dataset remain in sync to ensure accurate incremental updates. Follow the steps below:

1. **Schema Requirements**
   - Your schema must include:
     - A **primary key** (e.g., `transaction_id`)
     - A **versioning field** (e.g., `lastmodified` or an incrementing `version_id`)
   - Enable the dataset for **Orchestrated Campaigns** if needed.

2. **CDC Dataflow Setup**
   - During dataflow creation, after choosing your source and files:
     - **Enable the CDC option**
     - Select your CDC-ready dataset
     - Confirm field mappings (especially version field)

3. **Keep Source and Target in Sync**
   - The source system must consistently update the version field so the platform can detect changes accurately.

Once set up, the platform will automatically ingest **only changed or new records** each time the flow runs.
-->
