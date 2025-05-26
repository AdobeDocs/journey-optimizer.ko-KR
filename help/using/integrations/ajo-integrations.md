---
solution: Journey Optimizer
product: journey optimizer
title: 다른 솔루션과 통합
description: Journey Optimizer를 다른 솔루션과 통합시키는 방법을 자세히 알아보세요.
feature: Integrations
role: User
level: Intermediate
exl-id: 700dc66e-ae2d-418f-b75e-ece15af57ab3
source-git-commit: 11c6dd43d6b20864f9823130c5aed790a3091938
workflow-type: tm+mt
source-wordcount: '1021'
ht-degree: 59%

---

# 다른 솔루션과 통합 {#integration}

Adobe Journey Optimizer를 사용하면 이 데이터를 쉽게 관리하고 유지할 수 있으며, 기술 스택에 포함된 플랫폼 또는 시스템으로 내보낼 수 있습니다. 이러한 통합을 통해 특정 사용 사례를 해결하고, Adobe Journey Optimizer의 기능 범위를 확장할 수 있습니다.

>[!NOTE]
>
> Adobe Experience Platform을 기반으로 구축된 Adobe Journey Optimizer은 기본적으로 [Adobe 실시간 고객 프로필](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=ko){target="_blank"}에 연결됩니다. 기본 제공 데이터 소스는 사전 구성되어 있으며 실시간 고객 프로필에서 데이터를 검색하고 사용하도록 설계되었습니다(예: 여정에 참여한 사람이 클라이언트인지 여부 확인). 프로필 데이터 및 경험 이벤트 데이터를 사용할 수 있습니다. [자세히 알아보기](../datasource/adobe-experience-platform-data-source.md).
>

## Adobe Customer Journey Analytics {#integration-cja}

Customer Journey Analytics를 사용하여 Journey Optimizer에서 생성한 데이터에 대한 고급 분석을 수행할 수 있습니다.

Journey Optimizer은 Adobe Experience Platform에 데이터를 저장하며, Customer Journey Analytics을 사용하면 자동화된 보고서 배포와 사용자 지정 데이터 시각화를 통해 모든 여정, 캠페인 및 오퍼를 전체적으로 볼 수 있습니다.

Journey Optimizer에서 여정을 만든 후 Customer Journey Analytics는 플랫폼에서 데이터를 수집하여 보고를 시작하고 고객이 여정과 갖는 모든 상호 작용의 영향을 이해할 수 있습니다.

[Journey Optimizer + Customer Journey Analytics](../reports/cja-ajo.md)에 대해 자세히 알아보세요.

## Adobe Analytics {#integration-aa}

이미 플랫폼에 캡처 및 스트리밍 되고 있는 모든 Adobe Analytics 행동 이벤트 데이터를 활용하여 고객을 위해 고객의 실시간 여정을 유도하고 경험을 자동화할 수 있습니다. 이 데이터는 Journey Optimizer를 통해 활용할 수 있는 대상자를 만드는 데도 사용할 수 있습니다.

[Journey Optimizer + Analytics](../event/about-analytics.md)에 대해 자세히 알아보세요.

## Adobe Experience Manager {#integration-aem}

Adobe Experience Manager 사용자는 워크플로를 Adobe Journey Optimizer과 결합할 수 있습니다. 사용 가능한 사용 사례는 다음과 같습니다.


>[!BEGINTABS]

>[!TAB AEM Assets]

**[!DNL Adobe Experience Manager Assets]** 통합은 마케팅 워크플로와 크리에이티브 워크플로를 결합해 줍니다. 기본적으로 **[!DNL Adobe Journey Optimizer]**&#x200B;과(와) 통합되어 디지털 자산을 저장, 관리, 검색 및 배포하려면 **[!DNL Assets Essentials]** 또는 **[!DNL Assets as a Cloud Service]**&#x200B;에 액세스하십시오. 이 통합은 메시지의 내용을 채우는 데 사용할 수 있는 단일 중앙 집중식 자산 저장소 역할을 합니다.

[![자세히 알아보기](../assets/do-not-localize/learn-more-button.svg)](../integrations/assets.md)

>[!TAB AEM 템플릿]

Adobe Journey Optimizer을 사용하면 Adobe Experience Manager 사이트를 통해 사용자 지정 메시지를 만들 수 있습니다. Adobe Experience Manager의 콘텐츠 소스를 사용하여 템플릿을 디자인한 다음 Adobe Journey Optimizer으로 전송합니다. 이렇게 공유된 템플릿은 Adobe Journey Optimizer의 이메일 디자이너에서 액세스할 수 있으므로, 원하는 대상자에게 메시지를 만들고 보내는 프로세스를 단순화할 수 있습니다.

[![자세히 알아보기](../assets/do-not-localize/learn-more-button.svg)](../integrations/aem-templates.md)

>[!TAB AEM 조각]

이제 Adobe Experience Manager을 Adobe Journey Optimizer과 통합하여 AEM 콘텐츠 조각을 Journey Optimizer 이메일 콘텐츠에 원활하게 통합할 수 있습니다. 이렇게 간소화된 연결을 통해 AEM 콘텐츠에 액세스하고 활용하는 프로세스를 간소화하여 개인화되고 동적인 캠페인 및 여정을 만들 수 있습니다.

[![자세히 알아보기](../assets/do-not-localize/try-it-button.svg)](../integrations/aem-fragments.md)

>[!TAB Dynamic Media]

Journey Optimizer Asset 선택기를 사용하여 Journey Optimizer 내에서 승인된 Dynamic Media 렌디션을 선택하고 사용합니다. Adobe Experience Manager의 자산에 대한 변경 사항은 즉시 Journey Optimizer 콘텐츠에 반영되므로 수동으로 업데이트하지 않아도 최신 버전을 항상 사용할 수 있습니다.

[![자세히 알아보기](../assets/do-not-localize/learn-more-button.svg)](../integrations/aem-dynamic.md)


>[!ENDTABS]



## Adobe Stock {#integration-stock}

[!DNL Adobe Stock] 및 [!DNL Adobe Journey Optimizer] 이메일 디자이너 통합 플러그인을 사용하면 메시지를 작성하는 데 사용할 이미지를 쉽게 탐색, 라이선싱, 저장할 수 있습니다.

[Journey Optimizer + Stock](../integrations/stock.md)에 대해 자세히 알아보십시오.

## Adobe Express {#express}

Adobe Journey Optimizer의 Adobe Express 통합을 통해 콘텐츠를 만드는 동안 Adobe Express의 강력한 편집 도구에 쉽게 액세스할 수 있습니다. 이 통합을 통해 솔루션 간에 전환할 필요 없이 이미지 크기를 조정하고, 배경을 제거하고, 시각적 개체를 자르고, 자산을 JPEG 또는 PNG로 변환할 수 있습니다.

[Journey Optimizer + Adobe Express](../integrations/express.md)에 대해 자세히 알아보세요.

## GenStudio for Performance Marketing

Adobe GenStudio for Performance Marketing은 마케팅 팀이 자체 광고 및 이메일을 만들어 브랜드 표준을 준수하고 엔터프라이즈 정책을 준수하는 영향력이 큰 개인화된 마케팅 캠페인을 유도할 수 있는 생성 AI 우선 애플리케이션입니다. Adobe AI 기술을 활용함으로써 크리에이티브가 혁신에 집중할 수 있도록 콘텐츠 생성 및 관리의 복잡성을 간소화하는 포괄적인 도구 모음을 제공합니다.

[Journey Optimizer + GenStudio for Performance Marketing](../integrations/genstudio.md)에 대해 자세히 알아보세요.


## Adobe Intelligent Services {#integration-intelligent-service}

실시간 고객 데이터 플랫폼을 기반으로 하는 Adobe Intelligent Services를 사용하면 고객 경험 사용 사례에서 인공 지능과 머신 러닝을 활용할 수 있습니다. 이를 통해 마케팅 분석가가 데이터 과학에 대한 전문 지식 없이도 비즈니스 수준의 구성을 사용하여 기업의 요구 사항에 맞는 예측을 설정할 수 있습니다.

고객 AI는 브랜드가 Adobe Experience Platform에서 프로필 속성으로 사용할 수 있고 여정을 개인화하는 데 사용할 수 있는 회전 또는 변환 머신 러닝 기반 점수를 만들 수 있도록 합니다.

[Journey Optimizer + Adobe Intelligent Services](../building-journeys/ai-services-overview.md)에 대해 자세히 알아보세요.


## Adobe Campaign {#integration-ac}

Adobe Campaign v7 또는 v8이 있는 경우 통합을 사용할 수 있습니다. 이 통합을 사용하면 Adobe Campaign 트랜잭션 메시지 기능을 사용하여 이메일, 푸시 알림 및 SMS를 전송할 수 있습니다.

[Journey Optimizer + Campaign](../building-journeys/ajo-ac.md)에 대해 자세히 알아보세요.

Adobe Campaign Standard과 통합하여 여정에서 메시지를 보내도록 설정할 수도 있습니다.

[Journey Optimizer + Campaign Standard](../building-journeys/using-adobe-campaign-standard.md)에 대해 자세히 알아보세요.


## Adobe Workfront {#integration-workfront}

Adobe Workfront의 Adobe Journey Optimizer 모듈을 사용하여 레코드를 생성하고 읽거나 업데이트 또는 삭제하거나 Adobe Journey Optimizer API에 대한 사용자 정의 API 호출을 수행할 수 있습니다.

이 통합의 주요 단계에 대한 개요를 이 블로그 게시물에서 [사용할 수 있습니다](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/accelerating-go-to-market-how-workfront-workfront-fusion-aep-and/ba-p/653685?profile.language=ko){target="_blank"}.

Journey Optimizer + Adobe Workfront에 대해 자세히 알아보기 [Adobe Workfront 설명서](https://experienceleague.adobe.com/docs/workfront/using/adobe-workfront-fusion/fusion-apps-and-modules/adobe-journey-optimizer-modules.html?lang=ko){target="_blank"}.

## 사용자 지정 채널 {#integration-custom}

서드파티 시스템을 사용하여 메시지를 보내거나 서드파티 시스템으로 API 호출을 보내려는 경우, 사용자 지정 작업을 사용하여 여정에 연결합니다. 예를 들어 사용자 지정 작업으로 Epsilon, Slack, [Adobe Developer](https://developer.adobe.com){target="_blank"}, Firebase 등의 시스템에 연결할 수 있습니다.

사용자 지정 작업은 기술 사용자가 정의하고 마케터가 사용할 수 있는 추가 작업입니다. 구성하고 나면 여정의 왼쪽 팔레트에서 **[!UICONTROL 작업]** 카테고리가 표시됩니다. [이 페이지](../building-journeys/about-journey-activities.md#action-activities)에서 자세히 알아보십시오.

[사용자 지정 작업](../action/about-custom-action-configuration.md)에 대해 자세히 알아보세요.

## 외부 데이터 소스 {#integration-external-systems}

Journey Optimizer에서는 사용자 지정 데이터 소스 및 사용자 지정 작업을 통해 외부 시스템에 대한 연결을 구성할 수 있습니다. 예를 들어, 외부 예약 시스템에서 오는 데이터로 여정을 보강할 수 있습니다.

[이 섹션](../datasource/external-data-sources.md)에서 외부 데이터 소스를 사용하여 서드파티 시스템에 대한 연결을 정의하는 방법을 알아봅니다.
