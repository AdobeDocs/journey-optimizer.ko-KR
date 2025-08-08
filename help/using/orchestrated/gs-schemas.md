---
solution: Journey Optimizer
product: journey optimizer
title: 구성 단계
description: DDL을 업로드하여 Adobe Experience Platform 내에서 관계형 스키마를 만드는 방법을 알아봅니다
exl-id: 327597f6-8a53-42dc-966a-baae49b58bb3
source-git-commit: 7fc03d15c63789a2c35e3d517ca0c63f93545d4c
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 3%

---


# 관계형 스키마 및 데이터 세트 시작{#gs-schemas}

이 안내서에서는 관계형 스키마를 만들고, 오케스트레이션된 캠페인에 대한 데이터 세트를 구성하고, 데이터를 수집하는 프로세스를 안내합니다.

![](assets/do-not-localize/schema_admin.png)

1. [관계형 스키마를 수동으로 만들기](manual-schema.md) 또는 [DDL 파일 사용](file-upload-schema.md)

   테이블, 속성 및 관계를 포함한 데이터 모델의 구조를 정의합니다. 빠른 설정을 위해 사용자 인터페이스에서 스키마를 수동으로 작성하거나 DDL 파일을 업로드하도록 선택하십시오.

   스키마를 수동으로 생성할 때 데이터 세트도 수동으로 생성하고 활성화해야 합니다. DDL 파일을 사용하는 경우 데이터 세트 생성 및 활성화가 자동으로 수행됩니다.

1. [스키마 연결](file-upload-schema.md)

   스키마 간의 관계를 설정하여 데이터 일관성을 보장하고 엔티티 간 쿼리를 활성화합니다. 예를 들어 충성도 거래를 수신자에게 연결하거나 브랜드를 대상으로 보상을 연결할 수 있습니다.

1. [데이터 수집](ingest-data.md)

   SFTP, 클라우드 스토리지 또는 데이터베이스와 같이 지원되는 소스에서 Adobe Experience Platform으로 데이터를 가져옵니다.

