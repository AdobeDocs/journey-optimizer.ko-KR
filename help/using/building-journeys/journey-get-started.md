---
solution: Journey Optimizer
product: journey optimizer
title: Journey Orchestration - 전체 안내서
description: Adobe Journey Optimizer에서 여정 오케스트레이션 시작을 위한 포괄적인 안내서
feature: Journeys, Get Started, Overview
role: User
level: Beginner, Intermediate
hide: true
hidefromtoc: true
keywords: 여정, 오케스트레이션, 시작, 온보딩, 기능
source-git-commit: 856f35ebd70f38065e9b116bb648de1f2c2d439a
workflow-type: tm+mt
source-wordcount: '896'
ht-degree: 47%

---


# Journey Orchestration - 전체 안내서{#journey-orchestration-guide}

Adobe Journey Optimizer의 여정을 사용하면 대상자의 행동 및 요구에 실시간으로 적응하는 여러 단계의 개인화된 고객 여정을 만들 수 있습니다. 직관적인 드래그 앤 드롭 캔버스를 사용하여 컨텍스트 기반 데이터와 대상 타겟팅을 활용하여 여러 채널에서 메시지와 작업을 오케스트레이션할 수 있으므로 최대의 효과를 얻을 수 있습니다.

실시간 트리거를 탐색하거나, 여정 속성을 관리하거나, 사용자 지정 작업 및 표현식과 같은 고급 도구를 사용하는 경우 이 안내서에서는 의미 있고 시기적절한 고객 경험을 제공하는 여정을 자신 있게 디자인하고 구체화할 수 있는 명확한 로드맵을 제공합니다.

## 여정 소개

[!DNL Journey Optimizer]를 통해 이벤트 또는 데이터 소스에 저장된 상황별 데이터를 활용하여 실시간 오케스트레이션 사용 사례를 빌드할 수 있습니다. 고객 행동 및 비즈니스 이벤트에 실시간으로 응답하는 여러 단계로 구성된 고급 시나리오를 디자인합니다.

Journey Optimizer 여정 디자이너는 마케터와 여정 실무자가 전체 채널에서 여러 단계로 구성된 1:1 여정을 조정하는 데 필요한 모든 것을 제공합니다. 여기에는 여정의 각 단계를 조정하고, 타깃 대상자를 정의하며, 행동과 상황별 데이터 및 비즈니스 이벤트를 기반으로 타깃 대상자 구성원이 보게 될 채널 전반의 메시지, 오퍼 및 콘텐츠를 포함하는 직관적인 드래그 앤 드롭 캔버스가 포함됩니다.

![팔레트, 캔버스 및 속성 창이 있는 여정 디자이너 인터페이스](assets/journey38.png)

**빌드를 시작할 준비가 되셨습니까?** [이 여정](journey-gs.md)에서 첫 번째 페이지를 만들고 디자인하는 방법을 알아봅니다.

## 여정 시작 {#section-getting-started}

Adobe Journey Optimizer에서 여정 오케스트레이션을 마스터할 주요 영역을 살펴봅니다.

>[!BEGINTABS]

>[!TAB 첫 번째 여정 구축]

여정 설정, 활동 추가, 게시 전 테스트 등 첫 번째 이벤트를 처음부터 만들고 디자인하는 방법에 대해 알아봅니다.

[![자세히 알아보기](../assets/do-not-localize/learn-more-button.svg)](journey-gs.md)

>[!TAB 주요 기능]

실시간 게재, 컨텍스트 데이터, 기본 제공 및 사용자 지정 작업, 비주얼 디자이너, 테스트 기능 등 여정으로 수행할 수 있는 작업을 알아봅니다.

[![자세히 알아보기](../assets/do-not-localize/learn-more-button.svg)](#capabilities)

>[!TAB 사용 사례]

환영 이메일, 전송 시간 최적화, 램프 업 게재 및 평일 타겟팅을 포함한 실제 여정 예를 살펴봅니다.

[![자세히 알아보기](../assets/do-not-localize/learn-more-button.svg)](#use-cases)

>[!TAB 학습 리소스]

비디오 튜토리얼, 단계별 안내서 및 설명서에 액세스하여 마스터 여정 구축 및 문제 해결

[![자세히 알아보기](../assets/do-not-localize/learn-more-button.svg)](#learning-resources)

>[!ENDTABS]

## 주요 기능 {#capabilities}

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

**실시간 및 일괄 게재**

이벤트 수신 시 트리거되는 실시간 **단일 게재**&#x200B;를 보내거나 Adobe Experience Platform 대상자를 사용하여 **일괄** 게재를 보냅니다.

[여정 항목에 대해 알아보기](entry-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg)

**컨텍스트 데이터**

이벤트의 **컨텍스트 기반 데이터**, Adobe Experience Platform의 정보 또는 서드파티 API 서비스의 데이터를 활용합니다.

[데이터 소스 작업](../datasource/about-data-sources.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg)

**기본 제공 작업**

**기본 제공 채널 작업**&#x200B;을(를) 사용하여 [!DNL Journey Optimizer]에서 디자인된 메시지를 전자 메일, 푸시, SMS/MMS 등으로 보냅니다.

[여정으로 메시지 보내기](journeys-message.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg)

**사용자 지정 작업**

서드파티 시스템을 사용하여 메시지를 보내거나 외부 API에 연결하는 경우 **사용자 지정 작업**&#x200B;을(를) 만듭니다.

[사용자 정의 액션 구성](../action/about-custom-action-configuration.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/layout.svg)

**시각적 여정 디자이너**

**여정 디자이너**&#x200B;를 사용하면 여러 단계로 이루어진 사용 사례를 구축할 수 있습니다. 간단하게 시작 이벤트나 대상자 읽기 활동을 끌어다 놓고 조건을 추가하며 개인화된 메시지를 보내세요.

[여정 디자이너 탐색](using-the-journey-designer.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg)

**테스트 및 최적화**

게시 전에 여정을 테스트하고, 성능을 모니터링하고, 전송 시간 최적화와 같은 고급 기능을 사용하여 게재를 최적화합니다.

[여정 테스트 및 게시](testing-the-journey.md)
:::

::::

## 사용 사례 및 예 {#use-cases}

마케터는 여정 디자이너 내에서 이벤트가 발생할 때 모든 채널을 통해 실시간으로 트리거된 1:1 메시지를 보낼 수 있습니다. 예를 들어 고객이 서비스에 가입하면 [환영 이메일을 트리거](message-to-subscribers-uc.md)하여 앱에 처음 로그인하고 기본 설정을 지정하게 유도할 수 있습니다. 구매 완료, 이메일 열기, 앱 로그인과 같은 작업으로 여정을 통해 새로운 고객을 확보할 수 있습니다.

### 많이 사용하는 여정 사용 사례

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg)

**새 구독자 시작**

고객이 서비스를 구독하면 개인화된 환영 여정을 보내 온보딩 단계를 안내합니다.

[자세히 알아보기](message-to-subscribers-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/calendar-alt.svg)

**전자 메일 전송 시간 최적화**

AI 기반의 전송 시간 최적화를 사용하여 각 고객이 참여할 가능성이 가장 높을 때 이메일을 전송합니다.

[자세히 알아보기](send-time-optimization.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg)

**게재 램프 업**

메시지 볼륨을 점차 늘려 전송 평판을 개선하고 게재 가능성 문제를 방지합니다.

[자세히 알아보기](ramp-up-deliveries-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg)

평일별 **타겟**

고객이 여정을 입력하는 요일을 기준으로 다른 콘텐츠를 보냅니다.

[자세히 알아보기](weekday-email-uc.md)
:::

::::

### 추가 사용 사례

[여정 디자이너](using-the-journey-designer.md)는 이메일, 푸시 알림 및 SMS/MMS와 같은 아웃바운드 메시지와 모바일 앱, 웹 사이트 및 Journey Optimizer 내에서 직접 빌드된 코드 기반 경험을 비롯한 인바운드 채널을 지원하는 [기본 제공 채널 작업](journeys-message.md)을 제공합니다. 서드파티 시스템을 사용하여 메시지를 보낼 수도 있습니다. Journey Optimizer에는 이러한 시스템을 여정 디자이너에서 직접 여정에 통합할 수 있도록 하는 [사용자 지정 작업](using-custom-actions.md)이 포함되어 있습니다.

**구현 가능한 전체 시나리오를 검색하려면**&#x200B;이 페이지[에서 모든 여정 사용 사례를 살펴봅니다](jo-use-cases.md).

>[!NOTE]
>
>여정 가드레일 및 제한 사항은 [이 페이지](../start/guardrails.md)에서 자세히 확인할 수 있습니다.

## 학습 리소스 {#learning-resources}

### 비디오 튜토리얼 {#video}

여정의 구성 요소를 살펴보고 캔버스에서 여정을 작성할 때의 기본을 이해합니다.

>[!VIDEO](https://video.tv.adobe.com/v/3424996?quality=12)

### 주제별 탐색

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg)

**여정 만들기 및 관리**

개인화된 옴니채널 캠페인을 작성할 수 있는 고객 여정의 디자인, 테스트, 게시 및 추적에 대한 단계별 지침입니다.

[여정 만들기 살펴보기](/help/rp_landing_pages/create-journey-landing-page.md) | [여정 관리 학습](/help/rp_landing_pages/manage-journey-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg)

**여정 활동**

트리거, 의사 결정 단계, 대상자 관리 및 여정의 개인화된 메시지와 같은 활동을 구성하고 사용하는 방법을 알아봅니다.

[활동 살펴보기](/help/rp_landing_pages/about-journey-building-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg)

**표현식 및 조건**

강력한 도구와 구문을 사용한 동적 워크플로, 데이터 조작 및 고급 여정 오케스트레이션을 위한 표현식 작성을 완벽히 숙지해 보세요.

[표현식에 대해 알아보기](/help/rp_landing_pages/building-advanced-conditions-journeys-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bell.svg)

**문제 해결 및 모니터링**

디버깅 및 최적화를 위한 도구, 오류 코드 및 모범 사례를 통해 여정 실행 문제를 진단하고 해결합니다.

[문제 해결 안내서](/help/rp_landing_pages/troubleshoot-journey-landing-page.md)
:::

::::

### 추가 리소스

* **[여정 FAQ](journey-faq.md)** - 여정 관련 자주 하는 질문
* **[오류 코드 참조](error-codes-reference.md)** - 여정 오류 코드 및 문제 해결 단계
* **[경고](../reports/alerts.md)** - 여정 모니터링을 위한 경고 설정
* **[문제 해결](troubleshooting.md)** - 일반적인 여정 문제 및 해결 방법
* **[여정 자습서](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/tutorials/journeys/journey-designer-overview){target="_blank"}** - 실습형 비디오 자습서를 통해 여정 빌드에 대해 알아봅니다.

