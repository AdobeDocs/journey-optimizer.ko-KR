---
solution: Journey Optimizer
product: journey optimizer
title: 콘텐츠 실험 만들기
description: 캠페인에서 콘텐츠 실험을 만드는 방법을 알아봅니다
feature: A/B Testing
topic: Content Management
role: User
level: Beginner
keywords: 내용, 실험, 복수, 대상자, 처리
hide: true
hidefromtoc: true
exl-id: bd35ae19-8713-4571-80bc-5f40e642d121
badge: label="Beta" type="정보"
source-git-commit: 160e4ce03d3be975157c30fbe511875a85b00551
workflow-type: tm+mt
source-wordcount: '1145'
ht-degree: 5%

---

# 콘텐츠 실험 만들기 {#content-experiment}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment"
>title="콘텐츠 실험"
>abstract="여러 게재 처리를 정의하고 대상에 가장 적합한 조합을 결정하기 위해 게재 콘텐츠, 제목 또는 발신자를 변경하도록 선택할 수 있습니다."

>[!BEGINSHADEBOX]

이 설명서에서 찾을 수 있는 내용:

* [콘텐츠 실험 시작](get-started-experiment.md)
* **[콘텐츠 실험 만들기](content-experiment.md)**
* [통계 계산 이해](experiment-calculations.md)
* [실험 보고서 구성](reporting-configuration.md)
* [실험 보고서의 통계 계산](experiment-report-calculations.md)

>[!ENDSHADEBOX]

Journey Optimizer 컨텐츠 실험 을 사용하면 타겟 대상자에게 가장 적합한 성과를 측정하기 위해 여러 게재 처리를 정의할 수 있습니다. 게재 콘텐츠, 제목 또는 발신자를 변경하도록 선택할 수 있습니다. 관심 대상은 각 처리에 임의로 할당되어 지정된 지표 측면에서 가장 적합한 대상을 결정합니다.

>[!NOTE]
>
>콘텐츠 실험으로 시작하기 전에 보고 구성이 사용자 지정 데이터 세트에 대해 설정되어 있는지 확인하십시오. 자세한 내용은 [이 섹션](reporting-configuration.md)을 참조하십시오.

아래 예에서 게재 대상은 두 그룹으로 분할되었으며, 각 그룹은 대상 모집단의 45%를 나타내고 홀드아웃 그룹은 10%로 게재를 받지 않습니다.

타겟팅된 대상의 각 사용자는 한 버전의 이메일을 받게 되며, 제목 줄은 다음 두 가지 중 하나입니다.

* 새 컬렉션과 이미지에 대한 10% 오퍼를 직접 홍보합니다.
* 나머지 한 곳은 이미지 없이 10% 할인을 명시하지 않고 스페셜 오퍼만 광고하고 있습니다.

여기의 목표는 받은 실험에 따라 수신자가 이메일과 상호 작용하는지 확인하는 것입니다. 따라서 우리는 선택할 것입니다 **[!UICONTROL 이메일 열람수]** 를 이 콘텐츠 실험의 기본 목표 지표로 사용합니다.

![](assets/content_experiment.png)

## 캠페인 만들기 {#campaign-experiment}

1. 다음에서 **[!UICONTROL 캠페인]** 페이지, 클릭 **[!UICONTROL 캠페인 만들기]**.

   ![](assets/content_experiment_1.png)

1. 채널을 선택한 다음 **[!UICONTROL 표면]** 이 게재에 을(를) 사용하고 **[!UICONTROL 만들기]**. 자세한 내용은 [채널 표면](../configuration/channel-surfaces.md) 페이지를 가리키도록 업데이트하는 중입니다.

   ![](assets/content_experiment_2.png)

1. 다음을 설정합니다. **[!UICONTROL 속성]** 게재 기간:
   * **[!UICONTROL 이름]**
   * **[!UICONTROL 설명]**

1. 타깃팅할 대상을 정의합니다. 이렇게 하려면 **[!UICONTROL 대상자 선택]** 단추를 클릭하여 사용 가능한 Adobe Experience Platform 세그먼트 목록을 표시합니다. [세그먼트에 대해 자세히 알아보기](../segment/about-segments.md)

   다음에서 **[!UICONTROL ID 네임스페이스]** 필드에서 선택한 세그먼트에서 개인을 식별하기 위해 사용할 네임스페이스를 선택합니다. [자세히 알아보기](get-started-experiment.md#content-experiment-work)

   ![](assets/content_experiment_16.png)

1. 다음에서 **[!UICONTROL 작업 추적]** 섹션, 수신자가 게재에 반응하는 방식을 추적할지 여부를 지정합니다. 클릭 및/또는 열기를 추적할 수 있습니다.

   캠페인이 실행되면 캠페인 보고서에서 추적 결과에 액세스할 수 있습니다.

1. 특정 날짜 또는 반복 주기에 캠페인을 실행하려면 **[!UICONTROL 예약]** 섹션. [자세히 알아보기](create-campaign.md)

1. 클릭 **[!UICONTROL 콘텐츠 편집]** 게재 개인화를 시작합니다. [자세히 알아보기](../email/content-from-scratch.md)

   ![](assets/content_experiment_17.png)

1. 다음에서 **[!UICONTROL 콘텐츠 편집]** 창자, 치료 A를 개인화하기 시작하세요.

   이 처리를 위해 제목 줄에 직접 특별 오퍼를 지정하고 개인화를 추가합니다.

   ![](assets/content_experiment_5.png)

## 콘텐츠 실험 구성 {#configure-experiment}

1. 게재를 개인화하면 캠페인 요약 페이지에서 을(를) 클릭합니다. **[!UICONTROL 실험 만들기]** 콘텐츠 실험 구성을 시작합니다.

   ![](assets/content_experiment_3.png)

1. 다음 항목 선택 **[!UICONTROL 성공 지표]** 실험을 위해 을(를) 설정합니다.

   실험을 위해 다음을 선택합니다. **[!UICONTROL 이메일 열기]** 프로모션 코드가 제목 줄에 있는 경우 수신자가 이메일을 여는지 테스트합니다.

   ![](assets/content_experiment_11.png)

1. 클릭 **[!UICONTROL 처리 추가]** 필요한 만큼 새로운 치료법을 만들다.

   ![](assets/content_experiment_8.png)

1. 변경 **[!UICONTROL 제목]** 그들을 더 잘 구별하기 위해 당신의 치료의.

1. 을(를) 추가하도록 선택 **[!UICONTROL 유지]** 게재를 그룹화합니다. 이 그룹은 이 캠페인으로부터 어떤 콘텐트도 받지 않습니다.

   토글 막대를 켜면 인구의 10%가 자동으로 사용됩니다. 필요한 경우 이 비율을 조정할 수 있습니다.

   ![](assets/content_experiment_12.png)

1. 그런 다음 각 항목에 정확한 백분율을 할당하도록 선택할 수 있습니다 **[!UICONTROL 처리]** 또는 간단히 **[!UICONTROL 균등 분배]** 토글 막대.

   ![](assets/content_experiment_13.png)

1. 클릭 **[!UICONTROL 만들기]** 구성을 설정할 때입니다.

## 트리트먼트 디자인 {#treatment-experiment}

1. 다음에서 **[!UICONTROL 콘텐츠 편집]** 창에서 치료 B를 선택하여 내용을 변경합니다.

   여기에서는 오퍼를 **[!UICONTROL 제목 줄]**.

   ![](assets/content_experiment_18.png)

1. 클릭 **[!UICONTROL 이메일 본문 편집]** 을 추가하여 치료 B를 개인화합니다.

   ![](assets/content_experiment_9.png)

1. 치료를 디자인한 후 다음을 클릭하십시오. **[!UICONTROL 추가 작업]** 처리와 관련된 옵션에 액세스하려면: **[!UICONTROL 이름 바꾸기]**, **[!UICONTROL 복제]** 및 **[!UICONTROL 삭제]**.

   ![](assets/content_experiment_7.png)

1. 필요한 경우 **[!UICONTROL 실험 설정]** 메뉴: 처리 구성을 변경합니다.

   ![](assets/content_experiment_19.png)

1. 메시지 콘텐츠가 정의되면 **[!UICONTROL 콘텐츠 시뮬레이션]** 게재 렌더링을 제어하고 테스트 프로필로 개인화 설정을 확인하는 버튼입니다. [자세히 알아보기](../email/preview.md)

1. 콘텐츠 실험이 준비되면 캠페인 요약 페이지에서 다음을 클릭할 수 있습니다. **[!UICONTROL 활성화하려면 검토]** 캠페인 요약을 표시합니다. 매개 변수가 잘못되거나 누락된 경우 경고가 표시됩니다.

   ![](assets/content_experiment_15.png)

1. 캠페인이 올바르게 구성되었는지 확인한 다음, **[!UICONTROL 활성화]** 시작합니다.

   ![](assets/content_experiment_14.png)

실험 및 캠페인을 구성한 후 캠페인 보고서를 통해 게재의 성공 여부를 확인할 수 있습니다.

## 목표 보고서 {#objectives-global}

>[!AVAILABILITY]
>
>콘텐츠 실험 기능은 현재 조직 집합(제한된 가용성)에만 사용할 수 있습니다. 자세한 내용은 Adobe 직원에게 문의하십시오.

![](assets/performance_report.gif)

다음 **[!UICONTROL 목표]** 캠페인 보고서의 탭에서는 한 개의 특정 지표를 타깃팅하여 게재 보고서를 더 세밀하게 조정할 수 있습니다.

다음 **[!UICONTROL 목표]** 나열된 항목이 다음에 링크됨 **[!UICONTROL 데이터 세트]** 추가 정보를 검색할 수 있도록 시스템에 대한 연결을 정의합니다. 기본 제공 목록 **[!UICONTROL 목표]** 은(는) 사용할 수 있지만, 새 을(를) 추가하여 자신의 을(를) 추가할 수 있습니다. **[!UICONTROL 데이터 세트]**. 자세한 절차는 다음을 참조하십시오. [섹션](reporting-configuration.md).

타깃팅할 목표를 선택한 후 다음 두 가지 **[!UICONTROL 성능 개요]** 및 **[!UICONTROL 캠페인 목표]** 위젯은 게재 성능에 대한 자세한 요약을 제공합니다.

포함 **[!UICONTROL 캠페인 목표]** 위젯을 사용하여 기본 목표를 다른 지표와 비교하도록 선택할 수도 있습니다.

필요한 경우 각 위젯의 크기를 조정하고 삭제할 수 있습니다. 자세한 내용은 다음을 참조하십시오. [섹션](../reports/global-report.md#modify-dashboard).

## 실험 보고서 {#experimentation-global}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_click"
>title="성공 지표"
>abstract="실험을 만들 때 이전에 선택한 성공 지표의 총 값을 프로필 수로 나눈 값입니다."

>[!AVAILABILITY]
>
>콘텐츠 실험 기능은 현재 조직 집합(제한된 가용성)에만 사용할 수 있습니다. 자세한 내용은 Adobe 직원에게 문의하십시오.

![](assets/experimentation_report_3.png)

캠페인에서 **[!UICONTROL 글로벌 보고서]**, **[!UICONTROL 실험]** 탭에서는 각 변형의 수행 방식 및 최상의 수행자가 있는지 여부에 대한 기본 정보를 자세히 설명합니다.

최상의 수행자를 정의하는 데 시간이 걸릴 수 있습니다. 이 아이콘으로 표시됩니다. ![](assets/experimentation_report_1.png).

다음 **[!UICONTROL 실험 결과]** 위젯은 각 변형의 성능을 자세히 설명합니다. 에서 처리 중 하나를 선택하여 기준선을 변경할 수 있습니다. **[!UICONTROL 기준선]** 드롭다운. 최고의 치료법은 별 모양 아이콘으로 표시됩니다.

이 표에는 다음 지표가 나와 있습니다.

* **[!UICONTROL 프로필]**: 이 처리의 대상으로 삼은 프로필 수입니다.

* **[!UICONTROL 고유 아웃바운드 클릭수]**: 아웃바운드 채널 간 총 클릭 수.

* **[!UICONTROL 프로필별 개수]**: 실험 목표 지표를 프로필 수로 나눈 총 값입니다.

* **[!UICONTROL 신뢰 구간]**: 기준 처리와 최상의 성능 처리 사이의 성능 차이율 [자세히 알아보기](../campaigns/experiment-calculations.md#confidence-intervals).

* **[!UICONTROL 평균 리프트]**: 기준선에 대한 해당 처리의 전환율 개선 백분율입니다. [자세히 알아보기](../campaigns/experiment-calculations.md#understand-lift)

* **[!UICONTROL 신뢰도]**: 주어진 치료가 기준 치료와 동일하다는 증거. [자세히 알아보기](../campaigns/experiment-calculations.md#understand-confidence)

이러한 결과에 대한 자세한 내용과 해석 방법은 다음을 참조하십시오. [이 페이지](../campaigns/get-started-experiment.md#interpret-results).
