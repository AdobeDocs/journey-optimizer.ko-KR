---
solution: Journey Optimizer
product: journey optimizer
title: 여정 시작
description: 여정 시작
feature: Journeys, Get Started, Overview
role: User
level: Beginner, Intermediate
keywords: 여정, 검색, 시작
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
source-git-commit: 0571a11eabffeb5e318bebe341a8df18da7db598
workflow-type: ht
source-wordcount: '613'
ht-degree: 100%

---


# 여정 시작{#jo-general-principle}

[!DNL Journey Optimizer]를 통해 이벤트 또는 데이터 소스에 저장된 상황별 데이터를 활용하여 실시간 오케스트레이션 사용 사례를 빌드할 수 있습니다.

다음 기능을 통해 여러 단계로 구성된 고급 시나리오를 설계할 수 있습니다.

* 이벤트 수신 시 트리거되는 실시간 **단일 게재**&#x200B;를 보내거나 Adobe Experience Platform 대상자를 사용하여 **일괄적으로** 게재를 보냅니다.

* 이벤트의 **컨텍스트 기반 데이터**, Adobe Experience Platform의 정보 또는 서드파티 API 서비스의 데이터를 활용합니다.

* **기본 제공 채널 작업**&#x200B;을 사용하여 [!DNL Journey Optimizer]에서 작성된 메시지를 보내거나, 서드파티 시스템을 사용하여 메시지를 전송하는 경우 **사용자 정의 작업**&#x200B;을 만듭니다.

* **여정 디자이너**&#x200B;를 사용하면 여러 단계로 이루어진 사용 사례를 구축할 수 있습니다. 간단하게 시작 이벤트나 대상자 읽기 활동을 끌어다 놓고 조건을 추가하며 개인화된 메시지를 보내세요.

>[!NOTE]
>
>[이 페이지](../start/guardrails.md)에서 여정 가드레일 및 제한 사항을 자세히 확인할 수 있습니다.

## 여정 만들기 단계{#steps-journey}

Adobe Journey Optimizer를 사용하여 단일 캔버스에서 개인화된 여정을 디자인하고 오케스트레이션할 수 있습니다. 캠페인을 만드는 주요 단계는 다음과 같습니다.

![](assets/journey-creation-process.png)

➡️ [비디오에서 이 기능 살펴보기](#video)

Adobe Journey Optimizer에는 마케팅 활동과 일대일 고객 참여를 조화롭게 조정할 수 있는 옴니채널 오케스트레이션 캔버스가 포함되어 있습니다. 사용자 인터페이스를 사용하면 팔레트에서 캔버스로 활동을 쉽게 드래그 앤 드롭하여 여정을 작성할 수 있습니다.

![](assets/interface-journeys.png)

[이 페이지](journey-gs.md)에서 첫 번째 여정을 시작하고 만드는 방법을 알아봅니다.

옴니채널 여정 디자이너를 통해 타겟팅된 대상, 실시간 고객 또는 비즈니스 상호 작용을 기반으로 하는 업데이트 및 직관적인 드래그 앤 드롭 인터페이스를 사용한 옴니채널 메시지를 통해 여러 단계로 구성된 여정을 작성할 수 있습니다.

![](assets/journey38.png)

자세한 내용은 [이 섹션](using-the-journey-designer.md)을 참조하십시오.

데이터 엔지니어로서 데이터 소스, 이벤트 및 작업을 포함하여 여정을 구성하는 단계는 [이 섹션](../configuration/about-data-sources-events-actions.md)에 자세히 설명되어 있습니다.


## 사용 사례{#uc-journey}

다음의 엔드 투 엔드 사용 사례에서 여정을 작성하는 방법을 알아봅니다.

비즈니스 사용 사례:

* [다중 채널 메시지 보내기](journeys-uc.md)
* [Campaign v7/v8을 사용하여 메시지 보내기](ajo-ac.md)
* [구독자에게 메시지 보내기](message-to-subscribers-uc.md)

기술 사용 사례:

* [사용자 지정 작업으로 컬렉션을 동적으로 보내기](collections.md)
* [게재 램프 업](ramp-up-deliveries-uc.md)
* [외부 데이터 원본 및 사용자 지정 작업으로 처리량 제한](limit-throughput.md)

## 여정 버전{#journey-versions}

여정 목록에는 모든 여정 버전이 버전 번호와 함께 표시됩니다. [이 페이지](../building-journeys/using-the-journey-designer.md)를 참조하십시오.

여정을 검색하면 애플리케이션이 처음 열릴 때 최신 버전이 목록 맨 위에 나타납니다. 그런 다음 원하는 정렬을 정의하면 애플리케이션이 이를 사용자 기본 설정으로 유지합니다. 여정 버전은 여정 편집 인터페이스의 맨 위에 캔버스 위에 표시됩니다.

![](assets/journeyversions1.png)

>[!NOTE]
>
>대부분의 경우 프로필은 동일한 여정에서 동시에 여러 번 나타날 수 없습니다. 재진입이 활성화된 경우 프로필은 여정에 다시 진입할 수 있지만 여정의 이전 인스턴스를 완전히 종료할 때까지는 다시 진입할 수 없습니다. [자세히 보기](end-journey.md).

라이브 여정으로 수정해야 하는 경우 여정의 새 버전을 만듭니다.

1. 최신 버전의 라이브 여정을 열고 **[!UICONTROL 새 버전 만들기]**&#x200B;를 클릭한 후 확인합니다.

   ![](assets/journeyversions2.png)

   >[!NOTE]
   >
   >최신 버전의 여정에서만 새 버전을 만들 수 있습니다.

1. 수정하고 **[!UICONTROL 게시]**&#x200B;를 클릭한 후 확인합니다.

여정이 게시되는 순간부터 개인 사용자는 최신 버전의 여정으로 유입되기 시작합니다. 이미 이전 버전으로 진입한 사람은 여정이 완료될 때까지 해당 버전을 유지합니다. 나중에 동일한 여정으로 다시 진입하면 최신 버전으로 이동합니다.

여정 버전은 개별적으로 중지할 수 있습니다. 여정의 모든 버전은 이름이 같습니다.

새 여정 버전을 게시하면 이전 버전이 자동으로 종료되고 **닫힌** 상태로 전환됩니다. 여정 출입이 있을 수 없습니다. 최신 버전을 중지해도 이전 버전은 닫힌 상태로 유지됩니다.

## 방법 비디오 {#video}

여정의 구성 요소를 살펴보고 캔버스에서 여정을 작성할 때의 기본을 이해합니다.

>[!VIDEO](https://video.tv.adobe.com/v/3424996?quality=12)
