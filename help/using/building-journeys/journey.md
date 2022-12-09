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
source-wordcount: '572'
ht-degree: 0%

---


# 여정 시작{#jo-general-principle}

사용 [!DNL Journey Optimizer] 이벤트나 데이터 소스에 저장된 상황별 데이터를 사용하여 실시간 오케스트레이션 사용 사례를 빌드하려면 다음을 수행하십시오.

다음 기능을 통해 제공되는 여러 단계로 구성된 고급 시나리오 설계:

* 실시간 보내기 **단일 제공** 이벤트가 수신될 때 트리거되거나 **일괄적으로** adobe Experience Platform 세그먼트 사용.

* 활용 **컨텍스트 기반 데이터** 이벤트, Adobe Experience Platform의 정보 또는 서드파티 API 서비스의 데이터를 포함합니다.

* 를 사용하십시오 **기본 작업** 에 디자인된 메시지를 보냅니다. [!DNL Journey Optimizer] 또는 만들기 **사용자 지정 작업** 서드파티 시스템을 사용하여 메시지를 전송하는 경우

* 사용 **여정 디자이너**, 여러 단계 사용 사례를 빌드합니다. 시작 이벤트 또는 세그먼트 읽기 활동을 쉽게 끌어다 놓고 조건을 추가하고 개인화된 메시지를 보냅니다.

## 여정을 만드는 단계{#steps-journey}

Adobe Journey Optimizer를 사용하여 단일 캔버스에서 개인화된 여정을 디자인 및 오케스트레이션할 수 있습니다.

Adobe Journey Optimizer에는 마케터가 일대일 고객 참여와 마케팅 범위를 조화롭게 처리할 수 있는 옴니채널 오케스트레이션 캔버스가 포함되어 있습니다. 사용자 인터페이스를 사용하면 팔레트의 활동을 캔버스로 끌어다 놓아 여정을 구축할 수 있습니다.

![](assets/interface-journeys.png)

에서 첫 번째 여정을 시작하고 만드는 방법을 알아봅니다 [이 페이지](journey-gs.md).

옴니채널 여정 디자이너는 타겟팅된 대상과 실시간 고객 또는 비즈니스 상호 작용에 따른 업데이트, 직관적인 드래그하여 놓기 인터페이스를 사용하여 옴니채널 메시지를 포함하는 여러 단계 여정을 구축할 수 있습니다.

![](assets/journey38.png)

자세한 내용 [이 섹션](using-the-journey-designer.md).

데이터 엔지니어는 데이터 소스, 이벤트 및 작업을 포함하여 여정 구성 단계를 자세히 설명합니다. [이 섹션](../configuration/about-data-sources-events-actions.md).


## 사용 사례{#uc-journey}

다음의 종단 간 사용 사례에서 여정을 구축하는 방법을 알아봅니다.

비즈니스 사용 사례:

* [다중 채널 메시지 보내기](journeys-uc.md)
* [Campaign v7/v8을 사용하여 메시지 보내기](ajo-ac.md)
* [구독자에게 메시지 보내기](message-to-subscribers-uc.md)

기술 사용 사례:

* [사용자 지정 작업을 사용하여 동적으로 컬렉션 전달](collections.md)
* [게재 램프 업](ramp-up-deliveries-uc.md)
* [외부 데이터 소스 및 사용자 지정 작업으로 처리량 제한](limit-throughput.md)

## 여정 버전{#journey-versions}

여정 목록에는 모든 여정 버전이 버전 번호와 함께 표시됩니다. 자세한 내용은 [이 페이지](../building-journeys/using-the-journey-designer.md).

여정을 검색하면 애플리케이션이 처음 열리면 최신 버전이 목록 맨 위에 표시됩니다. 그런 다음 원하는 정렬을 정의할 수 있으며 응용 프로그램에서 해당 정렬을 사용자 기본 설정으로 유지합니다. 여정의 버전은 캔버스 위에 있는 journey edition 인터페이스 상단에도 표시됩니다.

![](assets/journeyversions1.png)

>[!NOTE]
>
>일반적으로 프로필은 동일한 여정에 동시에 여러 번 있을 수 없습니다. 다시 입장할 수 있는 경우 프로필이 다시 입장할 수 있지만, 여정의 이전 인스턴스를 완전히 종료한 후에는 해당 여정을 수행할 수 없습니다. [자세한 내용](end-journey.md).

라이브 여정으로 수정해야 하는 경우, 여정의 새 버전을 만드십시오.

1. 라이브 여정의 최신 버전을 열고 를 클릭합니다. **[!UICONTROL Create a new version]** 확인

   ![](assets/journeyversions2.png)

   >[!NOTE]
   >
   >최신 버전의 여정에서 새 버전만 만들 수 있습니다.

1. 수정한 후 **[!UICONTROL Publish]** 확인

   ![](assets/journeyversions3.png)

여정을 게시하면 개인들이 최신 버전의 여정으로 이동되기 시작합니다. 이미 이전 버전을 입력한 사람은 여정을 완료할 때까지 계속 유지됩니다. 나중에 동일한 여정을 다시 시작하면 최신 버전으로 이동하게 됩니다.

여정 버전은 개별적으로 중지할 수 있습니다. 여정의 모든 버전은 동일한 이름을 갖습니다.

새 여정 버전을 게시하면 이전 버전이 자동으로 종료되고 로 전환됩니다 **닫힘** 상태. 그 여정에 들어오는 것은 있을 수 없다. 최신 버전을 중지해도 이전 버전은 닫혀 있습니다.

>[!NOTE]
>
>여정 버전 가드레일 및 제한에 대해 자세히 알아보려면 [이 페이지](../start/guardrails.md#journey-versions-limitations)