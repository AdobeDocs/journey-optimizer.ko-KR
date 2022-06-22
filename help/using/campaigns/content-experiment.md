---
title: 컨텐츠 실험 만들기
description: 캠페인에서 컨텐츠 실험을 만드는 방법을 알아봅니다
feature: Overview
topic: Content Management
role: User
level: Beginner
source-git-commit: e6d0b4ab3d66d65f7575e63f85ab5c125107615b
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 0%

---

# 컨텐츠 실험 만들기 {#content-experiment}

컨텐츠 실험 기능을 사용하면 여러 전달 처리를 정의할 수 있습니다. 관심 대상은 관심 지표에 대해 가장 잘 수행하는 대상을 결정하기 위해 각 처리에 무작위로 할당됩니다. 이메일의 콘텐츠, 제목 또는 발신자를 변경하도록 선택할 수 있습니다.

아래 예에서는 게재 대상이 두 그룹으로 분할되어, 각각 타겟팅된 모집단의 45%를 나타내고, 10%의 상위 그룹은 게재를 받지 않습니다.

타겟팅된 대상의 각 사용자는 다음 두 가지 중 하나에 해당하는 제목란과 함께 한 버전의 이메일을 받게 됩니다.

* 한 오퍼가 새 컬렉션과 이미지에 대해 10% 오퍼를 직접 홍보합니다.
* 다른 오퍼는 이미지 없이 10% 할인을 지정하지 않고 특별 오퍼만 광고합니다.

여기서 목표는 수신자가 수신된 실험에 따라 이메일과 상호 작용하는지 확인하는 것입니다. 그러므로 우리는 **[!UICONTROL Email Opens]** 을 이 컨텐츠 실험에서의 기본 목표 지표로 사용하십시오.

![](assets/content_experiment.png)

## 캠페인 만들기 {#campaign-experiment}

1. 에서 **[!UICONTROL Campaigns]** 페이지를 클릭한 다음 **[!UICONTROL Create Campaign]**.

   ![](assets/content_experiment_1.png)

1. 선택 **[!UICONTROL Email]** 그러면 **[!UICONTROL Preset]** 이 게재에 을 사용하려고 합니다. 자세한 내용은 사전 설정 페이지를 참조하십시오.

   ![](assets/content_experiment_2.png)

1. **[!UICONTROL Create]**&#x200B;을(를) 클릭합니다.

1. 설정 **[!UICONTROL Properties]** 게재 시:
   * **[!UICONTROL Title]**
   * **[!UICONTROL Description]**
   * **[!UICONTROL Category]**: **[!UICONTROL Marketing]** / **[!UICONTROL Transactional]**

1. 컨텐츠 실험을 시작하려면 **[!UICONTROL Content experiment]** 선택 사항입니다. 다음 **[!UICONTROL Content experiment]** 메뉴가 나타납니다.

   ![](assets/content_experiment_3.png)

1. 설정 **[!UICONTROL Audience]** 및 **[!UICONTROL Schedule]** 게재에 대한 매개 변수입니다. [자세히 보기](create-campaign.md)

1. 클릭 **[!UICONTROL Edit content]** 다양한 **[!UICONTROL Treatments]**.

   ![](assets/content_experiment_4.png)

## 치료 만들기 {#treatment-experiment}

1. 에서 **[!UICONTROL Edit content]** 창에서 **[!UICONTROL Subject line]** 치료 A의 경우 e-메일을 확인하고 **[!UICONTROL Save]**.

   이 처리를 위해 오퍼를 제목 줄에 직접 지정합니다.

   ![](assets/content_experiment_5.png)

1. 클릭 **[!UICONTROL Email designer]** 게재 개인화를 시작하려면 다음을 수행하십시오.

   ![](assets/content_experiment_6.png)

1. 이메일을 디자인한 후 **[!UICONTROL Save]** 그리고 다시 **[!UICONTROL Edit content]** 치료 B를 생성할 창.

1. 에서 **[!UICONTROL More actions]** 버튼, 클릭 **[!UICONTROL Duplicate]**.

   을(를) 클릭하여 새 처리를 처음부터 시작하도록 선택할 수도 있습니다. **[!UICONTROL Content experiment]** 단추를 클릭하여 고급 옵션에 액세스한 다음 **[!UICONTROL Add treatment]**.

   ![](assets/content_experiment_7.png)

1. 변경 **[!UICONTROL Title]** 그들을 더 잘 차별화하기 위해 당신의 치료들을

   ![](assets/content_experiment_8.png)

1. 새로 만든 전자 메일 게재에 연결된 전자 메일 게재를 선택합니다 **[!UICONTROL Treatment]**.

1. 추가 **[!UICONTROL Subject line]** 전달을 위한 것입니다.

   이 치료를 위해 **[!UICONTROL Subject line]**.

   ![](assets/content_experiment_9.png)

1. 클릭 **[!UICONTROL Email designer]** 필요한 경우 처리 B 전달을 추가로 개인화합니다.

치료법이 개인화되면 컨텐츠 실험 구성을 시작할 수 있습니다.

## 콘텐츠 실험 구성 {#configure-experiment}

1. 두 게재가 모두 개인화된 경우, **[!UICONTROL Edit content]** 창, 선택 **[!UICONTROL Configure content experiment]**.

   ![](assets/content_experiment_10.png)

1. 실험에 설정할 목표를 선택합니다.

   테스트를 위해 **[!UICONTROL Email open]** 프로모션 코드가 제목 줄에 있는 경우 수신자가 이메일을 열는지 테스트하기 위해.

   ![](assets/content_experiment_11.png)

1. 추가 선택 **[!UICONTROL Holdout]** 그룹화하여 게재할 수 있습니다. 이 그룹은 이 캠페인에서 콘텐츠를 받지 않습니다.

   전환 표시줄을 켜면 모집단의 10%가 자동으로 전환되며, 필요한 경우 이 백분율을 조정할 수 있습니다.

   ![](assets/content_experiment_12.png)

1. 그런 다음 각 항목에 정확한 백분율을 할당하도록 선택할 수 있습니다 **[!UICONTROL Treatment]** 또는 **[!UICONTROL Distribute evenly]** 막대 전환

   ![](assets/content_experiment_13.png)

1. 클릭 **[!UICONTROL Save]** 구성을 설정할 때.

1. 컨텐츠 실험이 준비되면 **[!UICONTROL Review to activate]** 캠페인 요약을 표시합니다. 매개 변수가 잘못되었거나 누락된 경우 경고가 표시됩니다.

   ![](assets/content_experiment_15.png)

1. 캠페인이 올바르게 구성되었는지 확인하고 를 클릭합니다. **[!UICONTROL Activate]** 실행

   ![](assets/content_experiment_14.png)

