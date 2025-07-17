---
solution: Journey Optimizer
product: journey optimizer
title: 구성 단계
description: SFTP, 클라우드 스토리지 또는 데이터베이스와 같이 지원되는 소스에서 Adobe Experience Platform으로 데이터를 가져오는 방법을 알아봅니다.
badge: label="Alpha"
hide: true
hidefromtoc: true
source-git-commit: 3f92dc721648f822687b8efc302c40989b72b145
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 17%

---

# 데이터 수집 {#ingest-data}

+++ 목차

| 오케스트레이션된 캠페인 시작 | 첫 오케스트레이션된 캠페인 시작 | 데이터베이스 쿼리 | 오케스트레이션된 캠페인 활동 |
|---|---|---|---|
| [오케스트레이션된 캠페인 시작](gs-orchestrated-campaigns.md)<br/><br/>관계형 스키마 및 데이터 세트 만들기 및 관리</br> <ul><li>[스키마 및 데이터 세트 시작](gs-schemas.md)</li><li>[수동 스키마](manual-schema.md)</li><li>[파일 업로드 스키마](file-upload-schema.md)</li><li>[데이터 수집](ingest-data.md)</li></ul>[오케스트레이션된 캠페인 액세스 및 관리](access-manage-orchestrated-campaigns.md)<br/><br/>[오케스트레이션된 캠페인을 만드는 주요 단계](gs-campaign-creation.md) | [캠페인 만들기 및 예약](create-orchestrated-campaign.md)<br/><br/>[활동 오케스트레이션](orchestrate-activities.md)<br/><br/>[캠페인 시작 및 모니터링](start-monitor-campaigns.md)<br/><br/>[보고](reporting-campaigns.md) | [규칙 빌더로 작업](orchestrated-rule-builder.md)<br/><br/>[첫 번째 쿼리 빌드](build-query.md)<br/><br/>[표현식 편집](edit-expressions.md)<br/><br/>[재타겟팅](retarget.md) | [활동 시작](activities/about-activities.md)<br/><br/>활동:<br/>[및 가입](activities/and-join.md) - [대상 작성](activities/build-audience.md) - [차원 변경](activities/change-dimension.md) - [채널 활동](activities/channels.md) - [결합](activities/combine.md) - [중복 제거](activities/deduplication.md) - [데이터 보강](activities/enrichment.md) - [포크](activities/fork.md) - [조정](activities/reconciliation.md) - [대상 저장](activities/save-audience.md) - [분할](activities/split.md) - [대기](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

</br>

이 페이지의 컨텐츠는 최종본이 아니며, 변경될 수 있습니다.

>[!ENDSHADEBOX]

Adobe Experience Platform을 사용하면 외부 소스에서 데이터를 수집할 수 있으며 Experience Platform 서비스를 사용하여 들어오는 데이터를 구조화하고, 레이블을 지정하고, 향상시킬 수 있습니다. Adobe 애플리케이션, 클라우드 기반 저장소, 데이터베이스 및 기타 여러 소스와 같은 다양한 소스에서 데이터를 수집할 수 있습니다.

<!--
## With Cloud storage {#ingest}


>[!IMPORTANT]
>
>Each dataset in Adobe Experience Platform supports only one active dataflow at a time. For detailed setup guidance on how to switch data sources, refer to this [section](#cdc-ingestion).


You can configure a data flow to ingest data from an Amazon S3 source into Adobe Experience Platform. Once configured, the data flow enables automated, scheduled ingestion of structured data and supports real-time updates.

1. From the **[!UICONTROL Connections]** menu, access the **[!UICONTROL Sources]** menu.

1. Select the **[!UICONTROL Cloud storage]** category then Amazon S3 and click **[!UICONTROL Add Data]**.

    ![](assets/admin_sources_1.png)

1. Connect your S3 Account:

    * With an existing account

    * With a new account

    [Learn more in Adobe Experience Platform documentation](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/amazon-s3#connect)

    ![](assets/admin_sources_2.png)

1. Choose your folder **[!UICONTROL Data format]**, **[!UICONTROL Delimiter]** and **[!UICONTROL Compression type]**.

1. Navigate through the connected S3 source until you locate the two folders created earlier i.e. **loyalty rewards** and **loyalty transactions**.

1. Select the folder that contains your data.
    
    Selecting a folder ensures that all current and future files with the same structure are automatically processed. Selecting a single file, however, requires manually uploading each new data increment.

    ![](assets/S3_config_2.png)

1. Choose your folder **[!UICONTROL Data format]**, **[!UICONTROL Delimiter]** and **[!UICONTROL Compression type]**. Review your sample data for accuracy, then click **[!UICONTROL Next]**.

    ![](assets/S3_config_1.png)

1. Check **[!UICONTROL Enable Change data capture]** to select from datasets that are mapped to relational schemas and have both a primary key and a version descriptor defined.

1. Select your [previously created Dataset](#entities) and click **[!UICONTROL Next]**.

    ![](assets/S3_config_3.png)

1. In the **[!UICONTROL Mapping]** window, verify that each source file attribute is correctly mapped with the corresponding fields in the target schema.

    Click **[!UICONTROL Next]** once done.

    ![](assets/S3_config_4.png)

1. Configure the data flow **[!UICONTROL Schedule]** based on your desired frequency.

1. Click **[!UICONTROL Finish]** to create the data flow. It will execute automatically according to the defined schedule.

1. From the **[!UICONTROL Connections]** menu, select **[!UICONTROL Sources]** and access the **[!UICONTROL Data Flows]** tab to track flow execution, review ingested records, and troubleshoot any errors.

    ![](assets/S3_config_5.png)

-->

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