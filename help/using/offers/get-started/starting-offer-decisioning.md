---
title: 의사 결정 관리 시작하기
description: 의사 결정 관리를 시작합니다. 아키텍처, 제안, 의사 결정, 일반적인 활용 사례에 대해 자세히 알아보십시오.
translation-type: tm+mt
source-git-commit: b527186d0722492f5f509f1ae0a5315b9a9f771e
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 38%

---


# 의사 결정 관리 정보 {#about-offer-decision}

[!DNL Journey Optimizer] 를 사용하여 적절한 시기에 모든 접점에서 고객에게 최상의 혜택과 경험을 제공하십시오. 일단 디자인한 후에는 개인화된 제안을 통해 고객을 타깃팅하십시오.

의사 결정 관리 기능은 다음 두 가지 주요 구성 요소로 이루어집니다.

* 오퍼를 구성하는 다른 요소를 만들고 관리하고 해당 규칙과 제약 조건을 정의하는 인터페이스인 **중앙 오퍼 라이브러리**&#x200B;입니다.
* 오퍼 라이브러리와 함께 Adobe Experience Platform 데이터 및 실시간 고객 프로파일을 활용하는 **오퍼 결정 엔진**&#x200B;에서 오퍼가 제공될 올바른 시간, 고객 및 채널을 선택합니다.

![](../../assets/architecture.png)

이점은 다음과 같습니다.

* 다중 채널에 개인화된 오퍼를 전달하여 캠페인 성과를 향상시킬 수 있습니다.
* 워크플로우 개선: 마케팅 팀은 게재 또는 캠페인을 여러 개 만드는 대신 하나의 게재를 만들어 워크플로우를 개선하고 템플릿의 여러 부분에서 오퍼에 변화를 줄 수 있습니다,
* 캠페인 및 고객 측면에 표시될 오퍼 횟수를 제어합니다.

![](../../assets/do-not-localize/how-to-video.png) [의사 결정 관리에 ](#tutorial-videos) 대한 자세한 내용은 이 자습서를 참조하십시오.

## 오퍼 및 결정 정보 {#offers-offer-activities}

**오퍼**&#x200B;는 고객에게 제공되는 조건을 정의하는 콘텐츠, 자격 조건 규칙 및 제약 조건으로 구성됩니다.

오퍼를 만들고 게시할 여러 콘텐츠에 자격 조건 규칙 및 제약 조건을 연결할 수 있는 중앙 오퍼 카탈로그를 제공하는 **오퍼 라이브러리**&#x200B;를 사용하여 만듭니다([오퍼 라이브러리 사용자 인터페이스 참조](../get-started/user-interface.md)).

![](../../assets/offer_structure.png)

오퍼 라이브러리가 오퍼와 함께 증가하면 오퍼를 **결정**(이전에는 &#39;오퍼 활동&#39;이라고 함)에 통합할 수 있습니다.

의사 결정 엔진을 활용하면 배송 대상에 따라 최적의 오퍼를 선택할 수 있는 오퍼 컨테이너입니다.

## 일반적인 사용 사례

의사 결정 관리 기능과 Adobe Experience Platform와의 통합을 통해 고객의 참여도와 전환율을 높일 수 있는 다양한 활용 사례를 소개합니다.

* Adobe Experience Platform의 데이터를 기반으로 방문자의 관심 사항과 일치하는 오퍼를 웹 사이트에 표시합니다.

   ![](../../assets/website.png)

* 고객이 매장 근처에 있는 경우, 고객의 특성(충성도 수준, 성별, 이전 구매...)에 따라 사용 가능한 오퍼를 알려 주는 푸시 알림을 보냅니다.

   ![](../../assets/push_sample.png)

* 또한 의사 결정 관리를 사용하면 고객 지원 팀에 문의할 때 고객 경험을 향상시킬 수 있습니다. 의사 결정 관리 API를 사용하여 고객의 상환 및 다음 우수 오퍼에 대한 콜 센터 에이전트의 포털 정보를 표시할 수 있습니다.

   ![](../../assets/call-center.png)

## 튜토리얼 비디오 {#tutorial-videos}

>[!NOTE]
>
>이러한 비디오는 Adobe Experience Platform을 기반으로 구축된 Offer decisioning 응용 프로그램 서비스에 적용되며 [!DNL Adobe Journey Optimizer]에만 국한되지 않습니다. 하지만, 이 지침에서는 [!DNL Journey Optimizer] 컨텍스트에서 의사 결정 관리를 사용하기 위한 일반적인 지침을 제공합니다.

### 의사 결정 관리란 무엇입니까?{#what-is-offer-decisioning}

아래 비디오에서는 의사 결정 관리 주요 기능, 아키텍처 및 활용 사례를 소개합니다.

>[!VIDEO](https://video.tv.adobe.com/v/326961?quality=12&learn=on)

### 오퍼 정의 및 관리 {#use-offer-decisioning}

아래 비디오에서는 의사 결정 관리를 사용하여 오퍼를 정의 및 관리하고 실시간 고객 데이터를 활용하는 방법을 보여줍니다.

>[!VIDEO](https://video.tv.adobe.com/v/326841?quality=12&learn=on)
