---
solution: Journey Optimizer
product: journey optimizer
title: 다른 솔루션과 통합
description: Journey Optimizer을 다른 솔루션과 통합하는 방법을 자세히 알아보십시오
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 700dc66e-ae2d-418f-b75e-ece15af57ab3
source-git-commit: 12ae84646e69870564406066e102c540ac920df7
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 6%

---

# 다른 솔루션과 통합 {#integration}

Adobe Journey Optimizer을 사용하면 이 데이터를 쉽게 관리, 유지 및 기술 스택에 포함된 플랫폼 또는 시스템으로 내보낼 수 있습니다. 이러한 통합은 특정 사용 사례를 해결하고 Adobe Journey Optimizer 기능 범위를 확장하는 데 도움이 됩니다.

>[!NOTE]
>
> Adobe Experience Platform을 기반으로 구축된 Adobe Journey Optimizer은 기본적으로 [Adobe 실시간 고객 프로필](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=ko){target=&quot;_blank&quot;}. 이 기본 제공 데이터 소스는 사전 구성되어 있으며 실시간 고객 프로필에서 데이터를 검색하고 사용하도록 설계되었습니다(예: 여정을 입력한 사람이 클라이언트인지 확인). 프로필 데이터 및 경험 이벤트 데이터를 사용할 수 있습니다. [자세히 알아보기](../datasource/adobe-experience-platform-data-source.md).

## 보고{#integration-reporting}

### Adobe Customer Journey Analytics{#integration-cja}

Journey Optimizer에서 생성된 데이터를 내보내 Customer Journey Analytics에서 고급 분석을 수행할 수 있습니다.

Journey Optimizer과 Customer Journey Analytics 통합은 자동화된 보고서 분배 및 데이터에 대한 사용자 지정 시각화를 통해 모든 여정을 전체적으로 볼 수 있도록 합니다.

Journey Optimizer에서 여정을 만든 후 고객 데이터를 Customer Journey Analytics으로 가져와서 보고서를 시작하고 고객이 여정과 상호 작용한 모든 결과의 영향을 이해할 수 있습니다.

추가 정보 [Journey Optimizer + Customer Journey Analytics](../reports/cja-ajo.md).

### Adobe Analytics{#integration-aa}

이미 Adobe Experience Platform으로 캡처 및 스트리밍하고 있는 모든 Adobe Analytics 행동 이벤트 데이터를 활용하여 여정을 트리거하고 고객을 위한 경험을 자동화할 수 있습니다.

추가 정보 [Journey Optimizer + Analytics](../event/about-analytics.md).

## 기계 학습{#integration-intelligent-service}

Adobe Intelligent Services와의 통합을 통해 고객 경험 사용 사례에서 인공 지능과 머신 러닝을 활용할 수 있습니다. 이를 통해 마케팅 분석가는 데이터 과학 전문 지식 없이도 비즈니스 수준 구성을 사용하여 기업의 요구 사항에 맞는 예측을 설정할 수 있습니다. [자세히 알아보기](../building-journeys/ai-services-overview.md).

## 메시지 보내기 {#integration-messages}

서드파티 시스템을 사용하여 메시지를 보낼 수 있습니다.

### Adobe Campaign{#integration-ac}

Adobe Campaign v7 또는 v8이 있는 경우 통합을 사용할 수 있습니다. 이 통합을 사용하여 Adobe Campaign 트랜잭션 메시지 기능을 사용하여 이메일, 푸시 알림 및 SMS를 전송할 수 있습니다.

추가 정보 [Journey Optimizer + 캠페인](../building-journeys/ajo-ac.md).

Adobe Campaign Standard과 통합하여 여정에서 메시지를 보내도록 설정할 수도 있습니다.

추가 정보 [Journey Optimizer + Campaign Standard](../building-journeys/ajo-ac.md).

### 사용자 지정 채널{#integration-custom}

서드파티 시스템을 사용하여 메시지를 보내거나 여정이 서드파티 시스템에 API 호출을 전송하도록 하려면 사용자 지정 작업을 사용하여 여정에 대한 연결을 구성하십시오. 예를 들어 사용자 지정 작업으로 다음 시스템에 연결할 수 있습니다. Epsilon, Slack, [Adobe Developer](https://developer.adobe.com){target=&quot;_blank&quot;}, Firebase 등

사용자 지정 작업은 기술 사용자가 정의하며 마케터가 사용할 수 있는 추가 작업입니다. 구성되면 여정 왼쪽 팔레트의 **[!UICONTROL 작업]** 카테고리. [이 페이지](../building-journeys/about-journey-activities.md#action-activities)에서 자세히 알아보십시오.

추가 정보 [사용자 지정 작업](../action/about-custom-action-configuration.md).

## 외부 시스템{#integration-external-systems}

Journey Optimizer에서는 사용자 지정 데이터 소스 및 사용자 지정 작업을 통해 외부 시스템에 대한 연결을 구성할 수 있습니다. 예를 들어 외부 예약 시스템에서 가져온 데이터로 여정을 보강할 수 있습니다.

에서 외부 데이터 소스를 사용하여 타사 시스템에 대한 연결을 정의하는 방법을 알아봅니다. [이 섹션](../datasource/external-data-sources.md).
