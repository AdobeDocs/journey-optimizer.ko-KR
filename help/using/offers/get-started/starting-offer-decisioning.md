---
title: 의사 결정 관리 시작
description: Adobe Journey Optimizer를 통해 고객에게 최적의 오퍼를 적시에 전송하는 방법을 살펴볼 수 있습니다
feature: Offers
topic: Integrations
role: User
level: Beginner
exl-id: 659984cb-b232-47ba-9f5a-604bf97a5e92
source-git-commit: c530905eacbdf6161f6449d7a0b39c8afaf3a321
workflow-type: tm+mt
source-wordcount: '929'
ht-degree: 0%

---

# 의사 결정 관리 정보 {#about-decision-management}

사용 [!DNL Journey Optimizer] 모든 터치 포인트에서 고객에게 최적의 오퍼 및 경험을 제공하기 위한 것입니다. 일단 디자인되면 개인화된 오퍼로 대상을 타깃팅합니다.

의사 결정 관리를 사용하면 마케팅 오퍼의 중앙 라이브러리와 Adobe Experience Platform에서 만든 풍부한 실시간 프로필에 규칙과 제한을 적용하여 고객에게 적합한 오퍼를 적시에 보낼 수 있도록 하는 의사 결정 엔진을 통해 개인화를 손쉽게 수행할 수 있습니다.

결정 관리 기능은 다음 두 가지 주요 구성 요소로 구성됩니다.

* 다음 **중앙 집중식 오퍼 라이브러리** 오퍼를 구성하고, 규칙과 제한을 정의하는 다양한 요소를 만들고 관리하는 인터페이스입니다.
* 다음 **오퍼 결정 엔진** 오퍼가 전달될 고객 및 채널을 선택하기 위해 오퍼 라이브러리와 함께 Adobe Experience Platform 데이터 및 실시간 고객 프로필을 활용합니다.

![](../assets/architecture.png)

다음과 같은 이점이 있습니다.

* 여러 채널에서 개인화된 오퍼를 전달하여 캠페인 성과 개선
* 향상된 워크플로우: 마케팅 팀은 게재 또는 캠페인을 여러 개 만드는 대신 단일 게재를 만들어 워크플로우를 개선하고 템플릿의 여러 부분에서 오퍼에 변화를 줄 수 있습니다.
* 캠페인 및 고객 간에 오퍼가 표시되는 횟수를 제어합니다.

➡️ [이 비디오에서 의사 결정 관리에 대해 자세히 알아보십시오](#video)


>[!NOTE]
>
>만약 [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html){target=&quot;_blank&quot;} 사용자가 **Offer Decisioning** 응용 프로그램 서비스에서는 이 섹션에 설명된 모든 의사 결정 관리 기능이 적용됩니다.

## 오퍼 및 결정 정보 {#about-offers-and-decisions}

An **오퍼** 는 고객에게 표시되는 조건을 정의하는 컨텐츠, 자격 규칙 및 제한 사항으로 구성됩니다.

이 템플릿은 **오퍼 라이브러리**- 오퍼를 만들고 게시하기 위해 자격 규칙 및 제한을 여러 컨텐츠와 연결할 수 있는 중앙 오퍼 카탈로그를 제공합니다( 참조). [오퍼 라이브러리 사용자 인터페이스](../get-started/user-interface.md)).

![](../assets/offer_structure.png)

오퍼 라이브러리가 오퍼와 함께 보강되면 오퍼를 **결정**.

결정 사항은 게재 대상에 따라 게재할 최상의 오퍼를 선택하기 위해 오퍼 결정 엔진을 활용할 오퍼의 컨테이너입니다.

## 일반적인 사용 사례 {#common-use-cases}

의사 결정 관리 기능과 Adobe Experience Platform과의 통합을 통해 고객의 참여와 전환을 높이는 데 도움이 되는 다양한 사용 사례를 처리할 수 있습니다.

* Adobe Experience Platform의 데이터를 기반으로 방문한 고객의 관심 영역에 일치하는 웹 사이트 홈 페이지에 표시합니다.

   ![](../assets/website.png)

* 고객이 상점 중 한 곳에 근접하면 자신의 특성(충성도 수준, 성별, 이전 구매..)에 따라 사용 가능한 오퍼를 상기시키는 푸시 알림을 보냅니다.

   ![](../assets/push_sample.png)

* 또한 의사 결정 관리를 통해 지원 팀에 문의할 때 고객의 경험을 향상시킬 수 있습니다. 의사 결정 관리 API를 사용하면 고객이 상환한 정보와 다음 최상의 오퍼에 대한 콜 센터 에이전트의 포털 정보를 표시할 수 있습니다.

   ![](../../assets/do-not-localize/call-center.png)

## 의사 결정 관리에 대한 액세스 권한 부여 {#granting-acess-to-decision-management}

의사 결정 기능에 액세스하고 사용할 권한은 [Adobe Admin Console](https://helpx.adobe.com/enterprise/managing/user-guide.html){target=&quot;_blank&quot;}.

의사 결정 관리 기능에 대한 액세스 권한을 부여하려면 **[!UICONTROL Product profile]** 사용자에게 해당 권한을 할당합니다. 관리에 대해 자세히 알아보기 [!DNL Journey Optimizer] 사용자 및 권한 [이 섹션](../../administration/permissions.md).

결정 관리에 대한 권한은 다음과 같습니다. [이 섹션](../../administration/high-low-permissions.md#decisions-permissions).

## 용어 설명 {#glossary}

의사 결정 관리 사용 시 사용할 주요 개념 목록을 아래에서 확인할 수 있습니다.

* **최대 가용량** 또는 **빈도 제한**: 최대 가용성은 오퍼가 표시되는 횟수를 정의하는 제한으로 사용됩니다. 두 가지 유형의 대문자로, &quot;총 대문자&quot;라고도 하는 결합된 타겟 대상 전체에서 오퍼를 제안할 수 있는 횟수와 &quot;프로필 상한&quot;이라고도 하는 동일한 최종 사용자에게 오퍼를 제안할 수 있는 횟수를 설명합니다.

* **컬렉션**: 컬렉션은 오퍼의 카테고리와 같이 마케터가 정의한 사전 정의된 조건을 기반으로 오퍼의 하위 집합입니다.

* **결정**: 결정에는 오퍼의 선택을 알리는 논리가 포함되어 있습니다.

* **의사 결정 규칙**: 의사 결정 규칙은 개인화된 오퍼에 추가되고 자격을 결정하기 위해 프로필에 적용되는 제한입니다.

* **적합한 오퍼**: 적합한 오퍼는 프로필에 일관되게 제공할 수 있는 업스트림으로 정의된 제한 사항을 충족합니다.

* **의사 결정 관리**: 비즈니스 로직 및 의사 결정 규칙을 사용하여 채널 및 애플리케이션 간에 개인화된 오퍼 경험을 만들고 전달할 수 있습니다.

* **대체 오퍼**: 대체 오퍼는 최종 사용자가 컬렉션에서 개인화된 오퍼에 적합하지 않을 때 표시되는 기본 오퍼입니다.

* **오퍼**: 오퍼는 오퍼를 볼 수 있는 사용자를 지정하는 규칙과 연관된 규칙이 있을 수 있는 마케팅 메시지입니다.

* **오퍼 라이브러리**: 오퍼 라이브러리는 개인화된 및 대체 오퍼, 의사 결정 규칙 및 결정을 관리하는 데 사용되는 중앙 라이브러리입니다.

* **개인화된 오퍼**: 개인화된 오퍼는 자격 규칙 및 제한을 기반으로 사용자 정의 가능한 마케팅 메시지입니다.

* **배치**: 배치는 최종 사용자에 대해 오퍼가 표시되는 위치 및 컨텍스트입니다.

* **우선순위**: 우선 순위는 자격, 달력 및 캡핑과 같은 모든 제한 사항을 충족하는 오퍼의 등급을 지정하는 데 사용됩니다.

* **표현**: 표현은 오퍼를 표시하기 위해 위치나 언어 등의 채널이 사용하는 정보입니다.

## 방법 비디오{#video}

>[!NOTE]
>
>이 비디오들은 Adobe Experience Platform을 기반으로 구축된 Offer Decisioning 애플리케이션 서비스에 적용되며, 이에 국한되지 않습니다 [!DNL Adobe Journey Optimizer]. 그러나 다음과 같은 맥락에서 의사 결정 관리를 사용하기 위한 일반적인 지침을 제공합니다 [!DNL Journey Optimizer].

### 의사 결정 관리란 무엇입니까? {#what-is-offer-decisioning}

아래 비디오에서는 의사 결정 관리 주요 기능, 아키텍처 및 활용 사례를 소개합니다.

>[!VIDEO](https://video.tv.adobe.com/v/326961?quality=12&learn=on)

### 오퍼 정의 및 관리 {#use-offer-decisioning}

아래 비디오에서는 의사 결정 관리를 사용하여 오퍼를 정의 및 관리하고 실시간 고객 데이터를 활용하는 방법을 보여줍니다.

>[!VIDEO](https://video.tv.adobe.com/v/326841?quality=12&learn=on)


