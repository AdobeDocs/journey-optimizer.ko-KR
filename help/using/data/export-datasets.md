---
solution: Journey Optimizer
product: journey optimizer
title: 클라우드 스토리지 위치로 데이터 세트 내보내기
description: Adobe Experience Platform 클라우드 스토리지 대상을 사용하여 데이터 세트를 내보내는 방법을 알아봅니다.
role: User
level: Beginner
badge: label="Beta" type="Advertising"
keywords: 플랫폼, 데이터 레이크, 만들기, 레이크, 데이터 세트, 프로필
source-git-commit: c3ad875b50999da833d75e97a787cab9e24e38d4
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 1%

---


# 클라우드 스토리지 위치로 데이터 세트 내보내기 {#export-datasets}

>[!AVAILABILITY]
>
>데이터 세트 내보내기 기능은 현재 베타에 있으며 모든 Adobe Journey Optimizer 사용자가 사용할 수 있습니다. 아직 액세스 권한이 없는 경우 Adobe 담당자에게 대상 액세스 권한을 요청하십시오.

Journey Optimizer을 사용하면 데이터 세트의 컨텐츠를 내보내기 위해 클라우드 스토리지 위치와 라이브 연결을 설정할 수 있습니다.

데이터를 주기적으로 내보내면 고객 상호 작용에 대한 완전하고 최신 기록을 확보하고, 보고 또는 분석 목적으로 이 정보를 사용하고, 법적 요구 사항을 준수할 수 있습니다.

## 사용 가능한 클라우드 스토리지 대상 {#destinations}

에서 액세스할 수 있는 6개의 클라우드 스토리지 대상으로 데이터 세트를 내보낼 수 있습니다 **[!UICONTROL 대상]** 메뉴, **[!UICONTROL 카탈로그]** 탭.

![](assets/dataset-export-setup.png)

>[!AVAILABILITY]
>
>이러한 대상은 모두 베타로 제공되며 변경될 수 있습니다.

각 대상에 대한 자세한 내용은 Adobe Experience Platform 설명서에서 확인할 수 있습니다.

* [Amazon S3](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/amazon-s3.html)
* [Azure Blob](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/azure-blob.html)
* [Azure Data Lake Gen 2](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/adls-gen2.html)
* [데이터 랜딩 영역](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/data-landing-zone.html)
* [Google 클라우드 스토리지](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/google-cloud-storage.html)
* [SFTP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/sftp.html)

## 전제 조건 {#prerequisites}

데이터 세트 내보내기를 시작하기 전에 다음 사전 요구 사항을 확인하십시오.

* 데이터 세트를 내보내려면 **대상 관리**, **대상 보기**, **대상 활성화**, 및 **데이터 집합 대상 관리 및 활성화** [액세스 제어 권한](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html#permissions). 다음 문서를 참조하십시오. [액세스 제어 개요](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/overview.html) 또는 제품 관리자에게 문의하여 필요한 권한을 얻으십시오.

* 이 기능은 1세대 데이터, 즉 [Real-time Customer Data Platform 제품 설명](https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-b2c-edition-prime-and-ultimate-packages.html). 내보내려는 데이터 세트에 2세대 데이터가 포함되어 있지 않은지 확인하십시오.

## 데이터 세트를 내보내는 주요 단계 {#main-steps}

데이터 세트를 클라우드 스토리지 위치로 내보내는 주요 단계는 다음과 같습니다.

![](assets/dataset-export-process.png)

각 단계에 대한 자세한 내용은 Adobe Experience Platform 설명서에서 확인할 수 있습니다. [클라우드 스토리지 대상으로 데이터 세트 내보내기](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html?lang=en).

1. **클라우드 스토리지 대상 설정**. 아직 수행하지 않았다면 대상 카탈로그의 클라우드 스토리지 대상에 연결합니다. [새 대상 연결을 만드는 방법을 알아봅니다](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html?lang=en#setup)

   <!--![](assets/dataset-export-setup.png)-->

1. **클라우드 스토리지 대상 선택** 데이터 세트를 내보낼 위치. 대상 카탈로그에서 **[!UICONTROL 데이터 세트 내보내기]** 원하는 카드에서 버튼을 클릭하고 사용할 연결을 선택합니다.

   <!--![](assets/dataset-export-destination.png)-->

   >[!NOTE]
   >
   >실시간 고객 프로필과 함께 Adobe Journey Optimizer을 사용하는 경우 대상 카드에 &quot;활성화&quot; 단추가 표시되므로 활성화한 권한에 따라 데이터 세트를 내보내고 이 대상에 대한 세그먼트를 활성화할 수 있습니다.

1. **데이터 세트를 선택합니다** 선택한 대상으로 내보낼 대상.

   <!--![](assets/dataset-export-dataset-selection.png)-->

1. **내보내기 예약** 데이터 세트에 포함되어 있습니다. 내보내기를 시작할 시점과 내보내기가 발생할 빈도를 지정합니다.

   <!--![](assets/dataset-export-schedule.png)-->

1. **내보내기 검토 및 확인** 구성 끝에 표시되는 요약을 확인합니다.

   <!--![](assets/dataset-export-review.png)-->

내보내기가 완료되면 데이터 세트의 컨텐츠가 구성된 일정에 따라 클라우드 스토리지 위치에 보관됩니다. [성공적인 데이터 세트 내보내기를 확인하는 방법을 알아봅니다](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html#verify)
