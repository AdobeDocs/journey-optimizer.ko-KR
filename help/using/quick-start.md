---
title: 빠른 시작
description: Journey Optimizer 빠른 시작
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 71ab7369-fd84-46eb-95d2-941bd887d565
source-git-commit: c6592d16dc8bd9ea2bada4fc351c844985a1042f
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 35%

---

# 빠른 시작 {#cjm-quick-start}

## 시작하는 주요 단계 {#cjm-key-steps}

[!DNL Adobe Journey Optimizer]를 사용하면 기존 콘텐츠를 가져와 새로운 콘텐츠를 디자인할 수 있고 고객 프로필 데이터를 통해 메시지를 개인화할 수 있습니다. 또한 메시지를 트리거할 이벤트 만들기, 세그먼트를 정의, 대상 세분화 및 다중 채널 메시지를 전송할 수 있으며 메시지 및 여정의 영향을 측정하는 모든 보고 및 모니터링 도구를 이용할 수 있습니다.

조직에 따라 여러 유형의 사용자를 정의하고 권한에 따라 특정 기능에 대한 액세스 권한을 부여할 수 있습니다.

## 환경 준비 및 구성

[!DNL Adobe Journey Optimizer] 사용을 시작하기 전에 환경을 준비하기 위해 몇 가지 단계가 필요합니다.

시스템 관리자는 **제품 프로필을 이해하고 샌드박스 관리 및 채널 구성에 대한 권한**을 할당해야 합니다. 또한 샌드박스를 설정하고 사용 가능한 제품 프로필에 대해 관리해야 합니다.
그런 다음 팀 구성원을 제품 프로필에 할당하고 메시지를 위해 **채널 구성**&#x200B;을 설정할 수 있습니다.

자세한 내용은 다음 페이지에서 확인하십시오.

* **제품 프로필 및 권한 시작**

* **사용자** 권한을 설정하고 팀 구성원에게 액세스 권한을 제공합니다. [자세히 보기](../using/administration/permissions.md)

* **배포[!DNL Adobe Experience Manager Assets Essentials]** 를 통해 메시지의 자산 및 이미지를 관리합니다. 액세스 권한이 필요한 사용자는  [!DNL Assets Essentials] Assets Essentials 소비자  **사용자 또는/및** Assets Essentials 사용자 제품 프로필에  **** 포함되어야 합니다. [자세한](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html) 내용{target=&quot;_blank&quot;}

* **채널을** 구성하고 이메일 및 푸시 알림 설정을 정의합니다. [자세히 보기](../using/configuration/get-started-configuration.md)

* **프레젠테이션을** 정의하고 브랜딩 매개 변수를 구성합니다. [자세히 보기](../using/configuration/message-presets.md)

* **인스턴스** 를 분리된 가상 환경으로 분할하려면 sandboxestet을 관리합니다. [자세히 보기](../using/administration/sandboxes.md)


## 데이터 준비 및 여정 구성

데이터 관리자는 **데이터를 식별하고 스키마 및 데이터 세트**&#x200B;를 만들어야 데이터를 Adobe Experience Platform에 가져올 수 있습니다.

ID 네임스페이스 및 프로필에 대해 활성화된 데이터 세트를 만들고 세그먼트 및 테스트 프로필을 만드는 단계는 아래 섹션에 자세히 설명되어 있습니다.

* [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=ko){target=&quot;_blank&quot;}에서 **데이터 세트**&#x200B;을 미리 보고 만드는 방법을 알아봅니다

* [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html#manage-namespaces){target=&quot;_blank&quot;}에서 **ID 네임스페이스**&#x200B;를 만드는 방법을 알아봅니다

* [이 페이지에서 **테스트 프로필**&#x200B;을 만드는 방법을 알아봅니다.](../using/building-journeys/creating-test-profiles.md)

* [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html?lang=ko){target=&quot;_blank&quot;}의 **데이터 수집**&#x200B;에 대해 자세히 알아보십시오

* **대상 정의**, 세그먼트 만들기, 동의 및 개인 정보 관리 방법을 [이 페이지](../using/segment/about-segments.md)에서 알아봅니다.

또한 여정에서 메시지를 보낼 수 있으려면 **[!UICONTROL Data Sources]**, **[!UICONTROL Events]** 및 **[!UICONTROL Actions]**&#x200B;를 구성해야 합니다. [이 섹션](../using/configuration/about-data-sources-events-actions.md)에서 자세히 알아보기

## 메시지, 오퍼 및 여정 만들기

여정 연습자는 다음 섹션을 참조하여 첫 번째 여정을 설정하고, 오퍼, 자산을 추가하고, 메시지를 보냅니다.

* **메시지 만들기**: 메시지에 액세스, 이메일 및 푸시 콘텐츠 디자인 또는 로드, 개인화 추가 및 메시지를 미리 봅니다. [자세히 보기](create-message.md)

* **자산 업로드**: Adobe Experience Manager Assets Essentials을 사용하여 자산 및 이미지를 관리합니다. [자세히 보기](assets-essentials.md)

* **오퍼 추가**: Journey Optimizer 의사 결정 관리를 사용하여 메시지에 개인화된 오퍼를 추가하십시오. [자세히 보기](../using/offers/get-started/starting-offer-decisioning.md)

* **여정 만들기**: 메시지를 전송하고 컨텍스트 기반의 데이터를 활용하며 고객을 세분화하고 여러 단계로 구성된 사용 사례를 디자인 및 실행합니다. [자세히 보기](building-journeys/journey.md)

* **메시지 및 여정 모니터링**: 메시지 실행 제어, 확인 메시지 및 여정 보고서, 후속 게재 기능 지표. [자세히 보기](message-monitoring.md)
