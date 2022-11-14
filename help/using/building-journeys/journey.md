---
solution: Journey Optimizer
product: journey optimizer
title: 여정 시작
description: 여정 시작
feature: Journeys
role: User
level: Beginner
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
source-git-commit: f6db4f7cbb1951c009fa7915f340da96eea74120
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 25%

---


# 여정 시작{#jo-general-principle}

사용 [!DNL Journey Optimizer] 이벤트나 데이터 소스에 저장된 상황별 데이터를 사용하여 실시간 오케스트레이션 사용 사례를 빌드하려면 다음을 수행하십시오.

다음 기능을 통해 제공되는 여러 단계로 구성된 고급 시나리오 설계:

* 이벤트가 수신될 때 트리거되는 실시간 **단일 게재**&#x200B;로 보내거나 Adobe Experience Platform 세그먼트를 사용하여 **일괄적으로** 보냅니다.

* 이벤트의 **컨텍스트 기반 데이터**, Adobe Experience Platform의 정보 또는 서드파티 API 서비스의 데이터를 활용합니다.

* 를 사용하십시오 **기본 작업** 에 디자인된 메시지를 보냅니다. [!DNL Journey Optimizer] 또는 만들기 **사용자 지정 작업** 서드파티 시스템을 사용하여 메시지를 전송하는 경우

* **여정 디자이너**&#x200B;를 사용하여 여러 단계 사용 사례를 빌드합니다. 시작 이벤트 또는 세그먼트 읽기 활동을 쉽게 끌어다 놓고 조건을 추가하고 개인화된 메시지를 보냅니다.

## 여정 만들기 단계{#steps-journey}

Adobe Journey Optimizer을 사용하여 단일 캔버스에서 개인화된 여정을 디자인하고 오케스트레이션할 수 있습니다.

Adobe Journey Optimizer에는 마케터가 일대일 고객 참여와 마케팅 활동을 조화롭게 처리할 수 있는 옴니채널 오케스트레이션 캔버스가 포함되어 있습니다. 사용자 인터페이스를 사용하면 팔레트의 활동을 캔버스로 끌어다 놓아 여정을 작성할 수 있습니다.

![](assets/interface-journeys.png)

에서 첫 번째 여정을 시작하고 만드는 방법을 알아봅니다 [이 페이지](journey-gs.md).

옴니채널 여정 디자이너는 타겟팅된 대상들로 여러 단계 여정을 구축하고, 실시간 고객 또는 비즈니스 상호 작용을 기반으로 업데이트를 수행하고, 직관적인 드래그하여 놓기 인터페이스를 사용하여 옴니채널 메시지를 만들 수 있습니다.

![](assets/journey38.png)

자세한 내용 [이 섹션](using-the-journey-designer.md).

데이터 엔지니어는 데이터 소스, 이벤트 및 작업을 비롯한 여정 구성 단계를 자세히 설명합니다. [이 섹션](../configuration/about-data-sources-events-actions.md).


## 사용 사례{#uc-journey}

다음의 종단 간 사용 사례에서 여정을 빌드하는 방법을 알아봅니다.

비즈니스 사용 사례:

* [다중 채널 메시지 보내기](journeys-uc.md)
* [Campaign v7/v8을 사용하여 메시지 보내기](ajo-ac.md)
* [구독자에게 메시지 보내기](message-to-subscribers-uc.md)

기술 사용 사례:

* [사용자 지정 작업으로 컬렉션을 동적으로 보내기](collections.md)
* [게재 램프 업](ramp-up-deliveries-uc.md)
* [외부 데이터 원본 및 사용자 지정 작업으로 처리량 제한](limit-throughput.md)

## 여정 버전{#journey-versions}

여정 목록에 모든 여정 버전이 버전 번호와 함께 표시됩니다. [이 페이지](../building-journeys/using-the-journey-designer.md)를 참조하십시오.

여정을 검색하면 애플리케이션이 처음 열리는 목록 맨 위에 최신 버전이 나타납니다. 그런 다음 원하는 정렬을 정의할 수 있으며 응용 프로그램에서 해당 정렬을 사용자 기본 설정으로 유지합니다. 여정 버전이 캔버스 위의 여정 편집 인터페이스 맨 위에 표시됩니다.

![](assets/journeyversions1.png)

>[!NOTE]
>
>일반적으로 프로필은 동일한 여정에 동시에 여러 번 있을 수 없습니다. 재입력이 활성화된 경우 프로필은 여정에 다시 입력할 수 있지만 여정의 이전 인스턴스를 완전히 종료할 때까지는 다시 입력할 수 없습니다. [자세히 보기](end-journey.md).

라이브 여정으로 수정해야 하는 경우, 여정의 새 버전을 만드십시오.

1. 라이브 여정의 최신 버전을 열고 **[!UICONTROL 새 버전 만들기]** 확인

   ![](assets/journeyversions2.png)

   >[!NOTE]
   >
   >최신 버전의 여정에서는 새 버전만 만들 수 있습니다.

1. 수정한 후 **[!UICONTROL 게시]** 확인

   ![](assets/journeyversions3.png)

여정이 게시되는 순간부터 개인은 최신 버전의 여정으로 이동하기 시작합니다. 이미 이전 버전을 입력한 사람은 여정을 완료할 때까지 안에 있습니다. 나중에 동일한 여정을 다시 입력하면 최신 버전으로 전환됩니다.

여정 버전을 개별적으로 중지할 수 있습니다. 모든 버전의 여정의 이름은 동일합니다.

새 버전의 여정을 게시하면 이전 버전이 자동으로 종료되고 **닫힘** 상태. 여정 출입은 불가능합니다. 최신 버전을 중지해도 이전 버전은 닫혀 있습니다.

>[!NOTE]
>
>여정 버전 보호 및 제한에 대한 자세한 내용은 [이 페이지](../start/guardrails.md#journey-versions-limitations)