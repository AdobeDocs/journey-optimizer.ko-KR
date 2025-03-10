---
solution: Journey Optimizer
product: journey optimizer
title: 여러 단계 캠페인 생성의 주요 원칙
description: Adobe Journey Optimizer을 사용한 다단계 캠페인의 주요 원칙 알아보기
hide: true
hidefromtoc: true
source-git-commit: 00f843300a9cfe798ea4d3a92fbe89ba80e70bc5
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 36%

---


# 여러 단계 캠페인 생성의 주요 원칙 {#ms-campaign-creation}

Adobe Journey Optimizer을 사용하면 여러 단계 캠페인을 시각적 캔버스로 빌드하여 세그멘테이션, 캠페인 실행 및 파일 처리와 같은 크로스 채널 프로세스를 디자인할 수 있습니다.

## 여러 단계로 진행되는 캠페인의 내부는 무엇입니까? {#gs-ms-campaign-inside}

여러 단계 캠페인 다이어그램은 발생할 내용을 보여 줍니다. 앞으로 수행할 다양한 작업과 이러한 작업이 어떻게 서로 연결되어 있는지 설명합니다.

![](assets/workflow-example.png){zoomable="yes"} {zoomable="yes"}

각 다중 단계 캠페인에는 다음이 포함됩니다.

* **활동**: 활동은 수행할 작업입니다. 다양한 활동이 다이어그램에 아이콘으로 표시됩니다. 각 활동에는 특정 속성과 모든 활동에 공통되는 다른 속성이 있습니다.

  여러 단계 캠페인 다이어그램에서 주어진 활동은 여러 작업, 특히 반복이나 반복 작업이 있는 작업을 생성할 수 있습니다.

* **전환**: 전환은 원본 활동을 대상 활동에 연결하고 해당 시퀀스를 정의합니다.

* **작업 테이블**: 작업 테이블에는 전환에 의해 전달되는 모든 정보가 포함됩니다. 각 여러 단계 캠페인에서는 여러 작업 테이블을 사용합니다. 이러한 표에 전달된 데이터는 여러 단계 캠페인의 수명 주기 동안 사용할 수 있습니다.

## 여러 단계 캠페인을 만드는 주요 단계 {#gs-ms-campaign-steps}

여러 단계 캠페인을 만드는 주요 단계는 다음과 같습니다.

![](assets/workflow-creation-process.png){zoomable="yes"}

