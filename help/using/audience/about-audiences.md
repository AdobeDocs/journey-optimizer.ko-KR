---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Experience Platform 대상자 정보
description: Adobe Experience Platform 대상자 사용 방법 알아보기
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 19%

---


# 대상자 시작 {#about-segments}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_segment"
>title="Audience"
>abstract="Adobe Experience Platform에서는 실시간 고객 프로필 데이터를 활용하여 간단히 세그먼트 정의를 작성함으로써 고객의 고유 행동과 선호를 포착한 타겟팅 대상자를 만들 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_audience"
>title="캠페인 대상자 선택"
>abstract="이 목록에는 사용 가능한 모든 Adobe Experience Platform 대상자가 표시됩니다. 캠페인으로 타기팅할 대상자를 선택합니다. 캠페인에 구성된 메시지는 선택한 대상자에 속한 모든 개인 사용자에게 전송됩니다. [대상자에 대해 자세히 알아보기](../audience/about-audiences.md)"

대상자는 유사한 행동 및/또는 특성을 공유하는 사람들의 컬렉션입니다. Adobe Experience Platform 세분화 서비스를 사용하여 Adobe Experience Platform에서 중앙 집중식으로 구성 및 유지 관리되며 Journey Optimizer 내에서 쉽게 액세스하여 여정 및 캠페인에서 활성화할 수 있습니다.

Adobe Journey Optimizer은 대상을 만들고, 관리하고, 보강하여 마케팅 활동을 강화할 수 있는 강력한 도구를 제공합니다. Adobe Real-Time Customer Data Platform과 결합하면 Journey Optimizer을 사용하여 보다 복잡한 세분화를 위해 대상에 레이어를 배치하고 다른 Adobe Experience Cloud 솔루션과 대상을 양방향으로 공유할 수 있습니다.

실시간 데이터 스트림 또는 일괄 업로드되면 데이터 세트가 업데이트되고 Journey Optimizer이 실시간으로 개인 사용자를 대상 및 여정으로 동적으로 이동합니다.

>[!BEGINSHADEBOX]

이 설명서는 [!DNL Adobe Journey Optimizer] 내의 대상자를 사용하여 작업하는 방법에 대한 정보를 제공합니다. 대상자 포털 및 대상자에 대한 자세한 내용은 Adobe Experience Platform 세그멘테이션 서비스 설명서에서 확인할 수 있습니다. 자세한 내용은 다음 섹션을 참조하십시오.

* [세그먼테이션 서비스 UI 안내서](https://experienceleague.adobe.com/ko/docs/experience-platform/segmentation/ui/overview){target="_blank"}

* [세분화 서비스 - 자주 묻는 질문](https://experienceleague.adobe.com/ko/docs/experience-platform/segmentation/faq){target="_blank"}

>[!ENDSHADEBOX]

## 대상자 찾아보기 {#browse}

대상은 **[!UICONTROL 고객]** > **[!UICONTROL 대상]** 메뉴에서 사용할 수 있습니다.

대시보드는 중요한 대상 간의 겹침을 시각적으로 보여 주며, 지정된 기간 동안의 대상 크기 변경 또는 대상의 갑작스러운 급증과 같은 중요한 대상 트렌드를 탐색하도록 지원하므로 대상을 축소하게 한 이벤트 또는 작업뿐만 아니라 성공적인 오퍼와 같은 대상 증가를 초래한 이벤트나 작업도 강조할 수 있습니다.

![](assets/audiences-overview.png)

대상 포털에서 표준화된 레이블 지정, 거버넌스 제어, 검색 가능한 폴더 및 태그를 사용하여 대상을 쉽게 관리하고, 찾고, 탐색할 수 있습니다.

대상자 포털에서 대상자를 사용하여 작업하는 방법에 대한 자세한 내용은 [Adobe Experience Platform 세그먼테이션 서비스 설명서](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=ko){target="_blank"}를 참조하세요.

## 대상자 유형 {#types}

다음과 같은 다양한 방법을 사용하여 대상을 생성할 수 있습니다.

* **세그먼트 정의**: Adobe Experience Platform 세분화 서비스를 사용하여 새 대상 정의를 만듭니다. 대상은 세그먼트 정의에서 생성되며 평가 유형에 따라 다른 시간에 새로 고쳐집니다.

   * 스트리밍 세분화: 새로운 데이터가 유입되면 대상이 실시간으로 업데이트되므로 사용자 활동을 기반으로 지속적인 관련성이 보장됩니다.
   * 배치 세그멘테이션: 대상자가 24시간마다 새로 고쳐지며, 고정된 간격으로 프로필 스냅샷을 캡처합니다.
   * Edge 세그멘테이션: 대상자가 에지에서 즉시 평가되어 실시간 개인화가 가능합니다.

[세그먼트 정의를 만드는 방법을 알아봅니다](creating-a-segment-definition.md)

* **사용자 지정 업로드**: CSV 파일을 사용하여 대상을 가져옵니다. [사용자 지정 업로드 대상자를 만드는 방법을 알아봅니다](custom-upload.md)

* **대상 컴포지션**: 컴포지션 워크플로를 만들어 기존 대상을 시각적 캔버스로 결합하고 등급, 분할, 조인 등의 작업을 적용하여 새 대상을 만듭니다. [대상 구성을 사용하여 작업하는 방법을 알아봅니다](get-started-audience-orchestration.md)

* **페더레이션 대상 구성**: 기존 데이터 웨어하우스에서 직접 데이터 세트를 페더레이션하여 하나의 시스템에 Adobe Experience Platform 대상 및 특성을 모두 빌드하고 보강합니다. [Federated Audience Composition을 사용하여 작업하는 방법을 알아봅니다](federated-audience-composition.md).

## 사용 방법 비디오 {#video}

Journey Optimizer의 통합 고객 프로필 및 대상자에 대해 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/3432671?quality=12)
