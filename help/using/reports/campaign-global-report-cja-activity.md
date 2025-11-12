---
solution: Journey Optimizer
product: journey optimizer
title: 캠페인 보고서
description: 캠페인 보고서에서 라이브 활동 데이터를 사용하는 방법을 알아봅니다
feature: Reporting
topic: Content Management
role: User
level: Intermediate
source-git-commit: ce6bfca78d097588b5958c10c721b29b7013b3e2
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 2%

---

# 라이브 활동 캠페인 보고서 {#campaign-global-report-cja-activity}

>[!BEGINSHADEBOX]

캠페인에서 **[!UICONTROL 보고서]** 버튼을 클릭한 다음 **[!UICONTROL 모든 시간 보고서 보기]**&#x200B;를 선택하여 라이브 활동 캠페인 보고서에 액세스할 수 있습니다. [자세히 알아보기](report-gs-cja.md)

![](assets/report-access.png)

>[!ENDSHADEBOX]

## 전송 통계 {#sending-statistics-mobile}

![](assets/sending-statistics-mobile-live.png)

**[!UICONTROL 전송 통계]** 테이블은 라이브 활동 캠페인과 관련된 주요 지표에 대한 자세한 개요를 제공합니다. 대상 대상의 크기, 푸시 알림이 성공적으로 제공된 수와 같은 필수 정보를 표시하므로 라이브 푸시 알림의 전체 도달 범위와 성능을 평가하는 데 도움이 됩니다.

+++ 전송 통계 지표에 대해 자세히 알아보기

* **[!UICONTROL 타깃팅]**: 라이브 활동 중에 타깃팅된 총 프로필 수입니다.

* **[!UICONTROL 전송]**: 대상 프로필로 전송하려고 시도한 총 푸시 알림 수입니다.

* **[!UICONTROL 전달됨]**: 총 전송 시도 횟수와 관련된 푸시 알림 수가 장치에 전달되었습니다.

* **[!UICONTROL 오류 보내기]**: 오류(예: 잘못된 토큰 또는 연결 문제)로 인해 보낼 수 없는 총 푸시 알림 수입니다.

* **[!UICONTROL 제외 보내기]**: Adobe Journey Optimizer에서 보내는 데 제외된 프로필 수입니다(예: 옵트아웃 상태 또는 자격 규칙으로 인해).

+++

## 라이브 활동 라이프사이클 {#lifecycle}

![](assets/activity-lifecycle.png)

**[!UICONTROL 라이브 활동 라이프사이클]** 표는 라이브 활동이 시간이 지남에 따라 어떻게 진행되는지 종합적으로 볼 수 있습니다. 활동이 시작, 업데이트 또는 종료되는 시기와 같은 주요 이벤트에 대한 가시성을 제공하여 사용자 참여 및 라이브 활동 캠페인의 전체 라이프사이클을 더 잘 이해할 수 있습니다.

+++ 라이브 활동 라이프사이클 지표에 대해 자세히 알아보기

* **[!UICONTROL 원격 시작]**: 원격으로 시작된 Live 활동 수입니다. 일반적으로 서버나 백 엔드 시스템에 의해 트리거됩니다.

* **[!UICONTROL 로컬 시작]**: 사용자 장치에서 로컬로 시작된 라이브 활동 수로, 사용자 상호 작용이나 클라이언트측 트리거로 인해 발생하는 경우가 많습니다.

**[!UICONTROL 업데이트]**: 장치로 보낸 총 라이브 활동 업데이트 수입니다. 업데이트에는 상태 변경, 새 콘텐츠 또는 진행 상황 알림이 포함될 수 있습니다.

**[!UICONTROL 종료]**: 완료 시 자동으로 종료되거나 정의된 트리거나 시간 제한을 통해 수동으로 종료된 Live 활동 수입니다.

**[!UICONTROL 총계 수]**: 시작, 업데이트 및 종료를 포함한 모든 라이브 활동 라이프사이클 이벤트의 전체 합계로서, 라이브 활동 볼륨의 완전한 측정을 제공합니다.

+++

## 오류 원인 {#error-reasons}

![](assets/error-reasons-activity.png)

**[!UICONTROL 오류 원인]** 테이블을 사용하면 라이브 활동 전송 프로세스 중에 발생한 특정 오류를 식별하여 발생한 문제를 철저히 분석할 수 있습니다.

## 제외된 이유 {#excluded-reasons}

![](assets/excluded-activity.png)

**[!UICONTROL 제외된 이유]** 표는 타깃팅된 대상에서 사용자 프로필을 제외하여 실시간 활동을 받지 못하게 한 다양한 요인을 시각적으로 보여 줍니다.
