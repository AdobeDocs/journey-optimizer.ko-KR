---
solution: Journey Optimizer
product: journey optimizer
title: 캠페인 작업 구성
description: Campaign 작업을 구성하는 방법을 알아봅니다.
feature: Campaigns
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
keywords: 만들기, 최적화 도구, 캠페인, 표면, 메시지
source-git-commit: 1bdba8c5c1a9238d351b159551f6d3924935b339
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 10%

---


# 캠페인 작업 구성 {#action-campaign-action}

**[!UICONTROL 작업]** 탭을 사용하여 메시지에 대한 채널 구성을 선택하고 추적, 콘텐츠 실험 또는 다국어 콘텐츠와 같은 추가 설정을 구성합니다.

1. **채널 선택**

   **[!UICONTROL 작업]** 탭으로 이동하여 **[!UICONTROL 작업 추가]** 단추를 클릭하고 통신 채널을 선택합니다.

   ![](assets/create-campaign-add-action.png)

   >[!NOTE]
   >
   >사용 가능한 채널은 라이선스 모델 및 추가 기능에 따라 다릅니다.

1. **채널 구성 선택**

   [시스템 관리자](../start/path/administrator.md)에 의해 구성이 정의되었습니다. 여기에는 헤더 매개변수, 하위 도메인, 모바일 앱 등 메시지 전송을 위한 모든 기술적 매개변수가 포함되어 있습니다. [채널 구성을 설정하는 방법 알아보기](../configuration/channel-surfaces.md)

   ![](assets/create-campaign-action.png)

1. **콘텐츠 실험 만들기**

   대상 대상자에게 가장 적합한 성과를 측정하기 위해 **[!UICONTROL 콘텐츠 실험]** 섹션을 사용하여 여러 게재 처리를 정의합니다. **[!UICONTROL 실험 만들기]** 단추를 클릭한 다음 이 섹션에 설명된 단계를 따릅니다. [콘텐츠 실험 만들기](../content-management/content-experiment.md).

1. **다국어 콘텐츠 추가**

   **[!UICONTROL 언어]** 섹션을 사용하여 캠페인 내에서 여러 언어로 콘텐츠를 만드십시오. 이렇게 하려면 **[!UICONTROL 언어 추가]** 단추를 클릭하고 원하는 **[!UICONTROL 언어 설정]**&#x200B;을 선택합니다. 다국어 기능 설정 및 사용 방법에 대한 자세한 정보는 이 섹션에서 확인할 수 있습니다. [다국어 콘텐츠 시작](../content-management/multilingual-gs.md)

선택한 통신 채널에 따라 추가 설정을 사용할 수 있습니다. 자세한 내용을 보려면 아래 섹션을 확장하십시오.

+++**최대 가용량 규칙 적용**(전자 메일, DM, 푸시, SMS)

**[!UICONTROL 비즈니스 규칙]** 드롭다운 목록에서 최대 가용량 규칙을 캠페인에 적용할 규칙 집합을 선택하십시오. 채널 규칙 세트를 활용하면 통신 유형별로 빈도 상한을 설정하여 유사한 메시지가 있는 고객을 오버로드할 수 있습니다. [규칙 세트 작업 방법 알아보기](../conflict-prioritization/rule-sets.md)

+++

+++**참여 추적**(전자 메일, SMS).

**[!UICONTROL 작업 추적]** 섹션을 사용하여 수신자가 이메일 또는 SMS 게재에 어떻게 반응하는지를 추적하세요. 캠페인이 실행되면 캠페인 보고서에서 추적 결과에 액세스할 수 있습니다. [캠페인 보고서에 대해 자세히 알아보기](../reports/campaign-global-report-cja.md)

+++

+++**빠른 전송 모드를 사용**(푸시)합니다.

빠른 전송 모드는 캠페인을 통해 대량으로 매우 빠른 푸시 메시지를 전송할 수 있는 [!DNL Journey Optimizer] 추가 기능입니다. 빠른 게재는 메시지 게재 지연이 비즈니스에 중요한 경우, 휴대폰에 긴급 푸시 알림(예: 뉴스 채널 앱을 설치한 사용자에게 속보)을 전송하려는 경우 사용됩니다. 빠른 전송 모드를 사용할 때의 성능에 대한 자세한 내용은 [Adobe Journey Optimizer 제품 설명](https://helpx.adobe.com/kr/legal/product-descriptions/adobe-journey-optimizer.html)을 참조하세요.

+++

+++**우선 순위 점수 할당**(웹, 인앱, 코드 기반)

캠페인에 우선 순위 점수를 할당하면 빈도 상한과 같은 부과된 제한 사항이 있을 때 인바운드 및 캠페인의 우선 순위를 지정할 수 있습니다. 숫자 값(0~100)을 입력하십시오. 숫자가 높을수록 우선순위가 높다는 점에 유의하십시오. [여정 및 캠페인에 우선 순위 점수를 할당하는 방법 알아보기](../conflict-prioritization/priority-scores.md)

+++

+++**추가 게재 규칙 설정**(콘텐츠 카드)

콘텐츠 카드 캠페인의 경우 추가 게재 규칙을 활성화하여 메시지를 트리거하는 이벤트 및 기준을 선택할 수 있습니다. [콘텐츠 카드를 만드는 방법을 알아봅니다](../content-card/create-content-card.md)

+++

+++**트리거 정의**(인앱)

인앱 메시지의 경우 **[!UICONTROL 트리거 편집]** 단추를 사용하여 메시지를 트리거하는 이벤트 및 기준을 선택할 수 있습니다. [인앱 메시지를 만드는 방법을 알아봅니다](../in-app/create-in-app.md)

+++

## 다음 단계 {#next}

캠페인 작업이 준비되면 콘텐츠를 디자인할 수 있습니다. [자세히 알아보기](campaign-content.md)
