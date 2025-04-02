---
solution: Journey Optimizer
product: journey optimizer
title: 여정 보고서
description: 여정 보고서에서 푸시 알림 데이터를 사용하는 방법을 알아봅니다
feature: Reporting, Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 6d4b7669-7852-42f0-9347-399a3994011f
source-git-commit: 7d1b89ca851442d2a67dda1e5c08d50d74d44028
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 3%

---

# 푸시 알림 여정 보고서 {#journey-global-report}

>[!BEGINSHADEBOX]

여정 내의 **[!UICONTROL 보고서 보기]** 단추를 클릭하여 푸시 알림 여정 보고서에 액세스할 수 있습니다. [자세히 알아보기](report-gs-cja.md)

![](assets/report-access-jo.png)

>[!ENDSHADEBOX]

## 전송 통계 {#sending-statistics-push}

![](assets/cja-campaign-push-sending-stat.png)

**[!UICONTROL 전송 통계]** 표를 사용하면 푸시 알림의 수행 방식을 이해할 수 있습니다. 게재율 및 대상 크기와 같은 주요 지표가 포함되어 있어 여정의 효율성과 도달 범위에 대한 중요한 통찰력을 제공합니다.

+++ 전송 통계 지표에 대해 자세히 알아보기

* **[!UICONTROL 사용자]**: SMS 메시지의 대상 프로필로 적합한 사용자 프로필 수입니다.

* **[!UICONTROL 타깃팅]**: 분석 중에 처리된 총 푸시 알림 수입니다.

* **[!UICONTROL 전송]**: 푸시 알림에 대한 총 전송 수입니다.

* **[!UICONTROL 배달됨]**: 보낸 총 푸시 알림 수와 관련하여 푸시 알림 수를 보냈습니다.

* **[!UICONTROL 아웃바운드 채널에 대한 바운스 수]**: 총 푸시 알림 수와 관련하여 전송 프로세스 및 자동 반환 처리 중에 누적된 총 오류 수입니다.

* **[!UICONTROL 아웃바운드 오류]**: 프로필로 보낼 수 없는 발생한 총 오류 수입니다.

* **[!UICONTROL 아웃바운드 제외]**: Adobe Journey Optimizer에서 제외된 프로필 수입니다.

+++

## 추적 통계 {#tracking-statistics-push}

![](assets/cja-campaign-push-track-stat.png)

**[!UICONTROL 추적 통계]** 테이블은 푸시 알림과 연결된 프로필 활동에 대한 자세한 스냅숏을 제공하여 참여 및 푸시 알림 효과에 대한 중요한 통찰력을 제공합니다.

+++ 추적 통계 지표에 대해 자세히 알아보기

* **[!UICONTROL 클릭스루 비율(CTR)]**: 푸시 알림과 상호 작용한 사용자의 비율입니다.

* **[!UICONTROL CTOR(Clickthrough open rate)]**: 푸시 알림을 연 횟수입니다.

* **[!UICONTROL 클릭 수]**: 푸시 알림에서 콘텐츠를 클릭한 횟수입니다.

* **[!UICONTROL 고유 클릭 수]**: 푸시 알림에서 콘텐츠를 클릭한 프로필 수입니다.

* **[!UICONTROL 푸시 사용자 지정 작업]**: 푸시 알림에 대한 응답으로 프로필에서 수행한 사용자 지정 작업 수입니다.
+++

## 추적된 링크 레이블 {#track-link-label-push}

![](assets/cja-campaign-push-link-labels.png)

**[!UICONTROL 추적된 링크 레이블]** 테이블은 푸시 알림 내의 링크 레이블에 대한 포괄적인 개요를 제공하여 가장 높은 방문자 트래픽을 생성하는 레이블을 강조 표시합니다. 이 기능을 사용하면 가장 인기 있는 링크를 식별하고 우선 순위를 지정할 수 있습니다.

+++ 추적된 링크 레이블 지표에 대해 자세히 알아보기

* **[!UICONTROL 고유 클릭 수]**: 푸시 알림에서 콘텐츠를 클릭한 프로필 수입니다.

* **[!UICONTROL 클릭 수]**: 푸시 알림에서 콘텐츠를 클릭한 횟수입니다.

+++

## 추적된 링크 URL {#track-link-url-push}

![](assets/cja-campaign-push-link-urls.png)

**[!UICONTROL 추적된 링크 URL]** 테이블은 가장 높은 방문자 트래픽을 유도하는 푸시 알림 내의 URL에 대한 포괄적인 개요를 제공합니다. 이를 통해 가장 인기 있는 링크를 식별하고 우선 순위를 지정할 수 있으므로 푸시 알림의 특정 콘텐츠와 함께 프로필 참여에 대한 이해를 높일 수 있습니다.

+++ 추적된 링크 URL 지표에 대해 자세히 알아보기

* **[!UICONTROL 고유 클릭 수]**: 푸시 알림에서 콘텐츠를 클릭한 프로필 수입니다.

* **[!UICONTROL 클릭 수]**: 푸시 알림에서 콘텐츠를 클릭한 횟수입니다.

+++

## 바운스 이유 {#bounce-reasons-push}

**[!UICONTROL 반송 원인]** 테이블은 반송된 푸시 알림과 관련된 데이터에 대한 포괄적인 개요를 제공하여 푸시 알림 반송 인스턴스의 특정 이유에 대한 중요한 통찰력을 제공합니다.

## 오류 원인 {#error-reasons-push}

**[!UICONTROL 오류 원인]** 테이블을 사용하면 푸시 알림을 보내는 동안 발생한 특정 오류를 식별할 수 있으므로 발생한 문제를 철저히 분석할 수 있습니다.

## 제외된 이유 {#exclude-reasons-push}

![](assets/cja-campaign-push-excluded.png)

**[!UICONTROL 제외 이유]** 표는 타깃팅된 대상에서 사용자 프로필을 제외하여 푸시 알림을 받지 못하게 한 다양한 요인을 시각적으로 보여 줍니다.

포괄적인 제외 이유 목록은 [이 페이지](exclusion-list.md)를 참조하세요.
