---
title: 결정 보고서
description: 의사 결정에 대해 보고하는 방법을 알아봅니다.
feature: Decisioning
topic: Integrations
role: User
level: Experienced
exl-id: 7c45cd8a-8e86-4646-ba0a-db393e92d9da
source-git-commit: 4c0605d6ccff5cd62ef7aeb04e0610342d7cc3d5
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 5%

---


# 결정 보고서 {#decisioning-report}

## 코드 기반 캠페인 보고 {#campaigns}

코드 기반 경험이 실행되면 전용 보고서에 액세스하여 주요 성과 지표(KPI)를 모든 것을 아우르는 대시보드로 모니터링하여 캠페인과 관련된 필수 지표에 대한 분석을 제공할 수 있습니다.

이는 의사 결정 항목 성과와 관련된 세부사항 및 사용자가 이들 성과와 어떻게 상호 작용했는지를 포괄한다. [코드 기반 경험 보고서로 작업하는 방법을 알아봅니다](../reports/campaign-global-report-cja-code.md)

![](../reports/assets/cja-decisioning-item-performance.png)

## Customer Journey Analytics에서 보고 {#cja}

Customer Journey Analytics을 사용하는 경우 Decisioning을 활용하는 코드 기반 캠페인에 대한 사용자 지정 보고 대시보드를 만들 수 있습니다.

주요 단계는 아래에 나와 있습니다. Customer Journey Analytics 작업 방법에 대한 자세한 내용은 [Customer Journey Analytics 설명서](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-landing){target="_blank"}를 참조하세요.

1. Customer Journey Analytics에서 **연결**&#x200B;을 만들고 구성합니다. 이렇게 하면 보고서를 보낼 데이터 세트에 연결할 수 있습니다. [연결을 만드는 방법을 알아보세요](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-connections/create-connection){target="_blank"}

1. **데이터 보기**&#x200B;를 만들어 이전에 만든 연결에 연결합니다. **[!UICONTROL 구성 요소]** 탭에서 보고에 표시할 관련 스키마 필드를 선택합니다. Decisioning의 경우 **propositioninteract** 및 **propositiondisplay** 필드를 포함해야 합니다. [데이터 보기를 만들고 구성하는 방법을 알아봅니다](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/create-dataview){target="_blank"}

1. **작업 영역 프로젝트**&#x200B;에서 데이터 구성 요소, 테이블 및 시각화를 결합하여 코드 기반 캠페인에 대한 보고서를 만들고 공유할 수 있습니다. [작업 영역 프로젝트를 만드는 방법을 알아봅니다](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects){target="_blank"}
