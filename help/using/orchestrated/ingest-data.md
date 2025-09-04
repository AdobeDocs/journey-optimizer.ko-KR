---
solution: Journey Optimizer
product: journey optimizer
title: 구성 단계
description: SFTP, 클라우드 스토리지 또는 데이터베이스와 같이 지원되는 소스에서 Adobe Experience Platform으로 데이터를 가져오는 방법을 알아봅니다.
exl-id: 7f1e7985-b68e-43d6-9c8f-fea2469f8af9
version: Campaign Orchestration
source-git-commit: 07ec28f7d64296bdc2020a77f50c49fa92074a83
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 21%

---


# 데이터 수집 {#ingest-data}

>[!IMPORTANT]
>
>데이터 세트의 데이터 소스를 변경하려면 동일한 데이터 세트 및 새 소스를 참조하는 새 데이터 플로우를 생성하기 전에 먼저 기존 데이터 흐름을 삭제해야 합니다.
>
>Adobe Experience Platform에서는 데이터 흐름과 데이터 세트 간에 엄격한 일대일 관계를 적용합니다. 따라서 정확한 증분 수집을 위해 소스와 데이터 세트 간의 동기화를 유지할 수 있습니다.

Adobe Experience Platform을 사용하면 외부 소스에서 데이터를 수집하는 동시에 Experience Platform 서비스를 사용하여 수신 데이터를 구조화하고 레이블을 지정하며 개선할 수 있습니다. Adobe 애플리케이션, 클라우드 기반 저장소, 데이터베이스 및 기타 여러 소스와 같은 다양한 소스에서 데이터를 수집할 수 있습니다.

데이터 세트는 스키마(열) 및 필드(행)를 포함하는 데이터 수집을 위한 저장소 및 관리 구조입니다. Experience Platform에 성공적으로 수집된 데이터는 데이터 세트로 데이터 레이크 내에 저장됩니다.

## 오케스트레이션된 캠페인에 대해 지원되는 소스 {#supported}

오케스트레이션된 캠페인에 사용할 수 있도록 지원되는 소스는 다음과 같습니다.

<table>
  <thead>
    <tr>
      <th>유형</th>
      <th>소스</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="3">클라우드 스토리지</td>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/s3">Amazon S3</a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/google-cloud-storage">Google 클라우드 스토리지</a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/sftp">SFTP</a></td>
    </tr>
      <td rowspan="4">클라우드 데이터 웨어하우스</td>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/databases/snowflake">Snowflake</a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/databases/bigquery">Google BigQuery</a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/data-landing-zone">데이터 랜딩 구역<a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/databases/databricks">Azure Databricks</a></td>
    </tr>
    <tr>
      <td rowspan="3">파일 기반 업로드</td>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/local-system/local-file-upload">로컬 파일 업로드<a></td>
    </tr>

</tbody>
</table>

## 관계형 스키마 데이터 위생 지침 {#cdc}

**[!UICONTROL 데이터 캡처 변경]**&#x200B;을 통해 활성화된 데이터 세트의 경우 삭제를 포함한 모든 데이터 변경 내용이 소스 시스템에서 Adobe Experience Platform으로 자동으로 미러링됩니다.

Adobe Journey Optimizer Campaign에서 **[!UICONTROL 데이터 캡처 변경]**&#x200B;을 통해 온보딩된 모든 데이터 세트를 활성화해야 하므로 소스에서 삭제를 관리하는 것은 고객의 책임입니다. 소스 시스템에서 삭제된 모든 레코드는 Adobe Experience Platform의 해당 데이터 세트에서 자동으로 제거됩니다.

파일 기반 수집을 통해 레코드를 삭제하려면 고객의 데이터 파일에서 `D` 필드의 `Change Request Type` 값을 사용하여 레코드를 표시해야 합니다. 이는 소스 시스템을 미러링하여 Adobe Experience Platform에서 레코드를 삭제해야 함을 나타냅니다.

고객이 원래 소스 데이터에 영향을 주지 않고 Adobe Experience Platform에서만 레코드를 삭제하려는 경우 다음 옵션을 사용할 수 있습니다.

* **변경 데이터 캡처 복제를 위한 프록시 또는 정리된 테이블**

  고객은 프록시 또는 정리된 소스 테이블을 만들어 Adobe Experience Platform에 복제되는 레코드를 제어할 수 있습니다. 그런 다음 이 중간 테이블에서 삭제를 선택적으로 관리할 수 있습니다.

* **Data Distiller을 통한 삭제**

  라이선스가 부여된 경우 **Data Distiller**&#x200B;을(를) 사용하여 소스 시스템과 관계없이 Adobe Experience Platform 내에서 직접 삭제 작업을 지원할 수 있습니다.

  [데이터 Distiller에 대해 자세히 알아보기](https://experienceleague.adobe.com/en/docs/experience-platform/query/data-distiller/overview)

## 데이터 흐름 구성

이 예에서는 구조화된 데이터를 Adobe Experience Platform에 수집하는 데이터 흐름을 구성하는 방법을 보여 줍니다. 구성된 데이터 흐름은 자동화된 예약 수집을 지원하고 실시간 업데이트를 가능하게 합니다.

1. **[!UICONTROL 연결]** 메뉴에서 **[!UICONTROL 소스]** 메뉴에 액세스합니다.

1. [오케스트레이션된 캠페인에 대해 지원되는 소스](#supported)에 따라 소스를 선택하십시오.

   ![](assets/admin_sources_1.png)

1. 클라우드 기반 소스를 선택한 경우 클라우드 스토리지 또는 Google 클라우드 스토리지 계정을 연결합니다.

   ![](assets/admin_sources_2.png)

1. Adobe Experience Platform에 수집할 데이터를 선택합니다.

   ![](assets/S3_config_1.png)

1. **[!UICONTROL 데이터 세트 세부 정보]** 페이지에서 **[!UICONTROL 데이터 캡처 변경 사용]**&#x200B;을 선택하여 관계형 스키마에 매핑되고 기본 키와 버전 설명자가 모두 포함된 데이터 세트만 표시합니다.

[관계형 스키마 데이터 위생 지침에 대해 자세히 알아보십시오](#cdc)

   >[!IMPORTANT]
   >
   > **파일 기반 원본 전용**&#x200B;의 경우 데이터 파일의 각 행에는 값이 `_change_request_type`(업데이트) 또는 `U`(삭제)인 `D` 열이 있어야 합니다. 이 열이 없으면 시스템에서 변경 사항 추적을 지원하는 것으로 데이터를 인식하지 않으며, 오케스트레이션된 캠페인 토글이 표시되지 않아서 타깃팅용으로 데이터 세트를 선택할 수 없습니다.

   ![](assets/S3_config_6.png)

1. 이전에 만든 데이터 집합을 선택하고 **[!UICONTROL 다음]**&#x200B;을(를) 클릭합니다.

   ![](assets/S3_config_3.png)

1. 파일 기반 소스만 사용하는 경우 **[!UICONTROL 데이터 선택]** 창에서 로컬 파일을 업로드하고 해당 구조와 내용을 미리 봅니다.

   지원되는 최대 크기는 100MB입니다.

1. **[!UICONTROL 매핑]** 창에서 각 원본 파일 특성이 대상 스키마의 해당 필드와 올바르게 매핑되었는지 확인하십시오. [타겟팅 차원에 대해 자세히 알아보세요](target-dimension.md).

   완료되면 **[!UICONTROL 다음]**&#x200B;을 클릭합니다.

   ![](assets/S3_config_4.png)

1. 원하는 빈도에 따라 **[!UICONTROL 일정]** 데이터 흐름을 구성합니다.

1. 데이터 흐름을 만들려면 **[!UICONTROL 완료]**&#x200B;을 클릭합니다. 정의된 일정에 따라 자동으로 실행됩니다.

1. **[!UICONTROL 연결]** 메뉴에서 **[!UICONTROL 소스]**&#x200B;를 선택하고 **[!UICONTROL 데이터 흐름]** 탭에 액세스하여 흐름 실행을 추적하고 수집된 레코드를 검토하며 오류 문제를 해결합니다.

   ![](assets/S3_config_5.png)


