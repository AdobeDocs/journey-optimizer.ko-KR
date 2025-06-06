---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer을 사용하여 오케스트레이션된 캠페인 만들기
description: Adobe Journey Optimizer으로 오케스트레이션된 캠페인을 만드는 방법을 알아봅니다
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 13da680d-fef8-4749-9190-8ca3d77b060a
source-git-commit: 450f83eb53068df10a63d39d1a43483ad3c7e803
workflow-type: tm+mt
source-wordcount: '788'
ht-degree: 17%

---


# 오케스트레이션된 캠페인 만들기 {#create-first-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_creation_workflow"
>title="오케스트레이션된 캠페인 목록"
>abstract="**다단계** 탭에는 모든 오케스트레이션된 캠페인이 나열됩니다. 오케스트레이션된 캠페인의 이름을 클릭하여 편집할 수 있습니다. 오케스트레이션된 새 캠페인을 추가하려면 **오케스트레이션된 캠페인 만들기** 버튼을 사용합니다."

+++ 목차

| 오케스트레이션된 캠페인 시작 | 오케스트레이션된 첫 번째 캠페인 시작 | 데이터베이스 쿼리 | 오케스트레이션된 캠페인 활동 |
|---|---|---|---|
| [오케스트레이션된 캠페인 시작](gs-orchestrated-campaigns.md)<br/><br/>[구성 단계](configuration-steps.md)<br/><br/>[오케스트레이션된 캠페인 만들기에 대한 주요 단계](gs-campaign-creation.md) | <b>[오케스트레이션된 캠페인 만들기](create-orchestrated-campaign.md)</b><br/><br/>[오케스트레이션된 캠페인 설정 오케스트레이션](orchestrated-campaign-settings.md)<br/><br/>[활동 오케스트레이션](orchestrate-activities.md)<br/><br/>[오케스트레이션된 캠페인으로 메시지 보내기](send-messages.md)<br/><br/>[캠페인 시작 및 모니터링](start-monitor-campaigns.md)<br/><br/>[보고](reporting-campaigns.md) | [규칙 빌더로 작업](orchestrated-rule-builder.md)<br/><br/>[첫 번째 쿼리 작성](build-query.md)<br/><br/>[표현식 편집](edit-expressions.md) | [활동 시작](activities/about-activities.md)<br/><br/>활동:<br/>[및 가입](activities/and-join.md) - [대상 작성](activities/build-audience.md) - [차원 변경](activities/change-dimension.md) - [결합](activities/combine.md) - [중복 제거](activities/deduplication.md) - [데이터 보강](activities/enrichment.md) - [포크](activities/fork.md) - [조정](activities/reconciliation.md) - [분할](activities/split.md) - [대기](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

## 캠페인 만들기

오케스트레이션된 캠페인을 만들려면 다음 단계를 수행합니다.

1. **오케스트레이션된 캠페인**&#x200B;을 만들려면 **캠페인** 메뉴로 이동하세요.

1. 화면 오른쪽 상단의 **[!UICONTROL 오케스트레이션된 캠페인 만들기]** 단추를 클릭합니다.

1. 오케스트레이션된 캠페인 **속성** 대화 상자에서 오케스트레이션된 캠페인을 만드는 데 사용할 템플릿을 선택합니다(기본 제공 템플릿을 사용할 수도 있음). [오케스트레이션된 캠페인 템플릿에 대해 자세히 알아보세요](#campaign-templates).

1. 오케스트레이션된 캠페인의 레이블을 입력합니다. 또한 오케스트레이션된 캠페인에 화면 **[!UICONTROL 추가 옵션]** 섹션의 전용 필드에 설명을 추가하는 것이 좋습니다.

1. 오케스트레이션된 캠페인에 대한 추가 설정을 구성하려면 **[!UICONTROL 추가 옵션]** 섹션을 확장합니다.

1. **[!UICONTROL 오케스트레이션된 캠페인 만들기]** 단추를 클릭하여 오케스트레이션된 캠페인 만들기를 확인합니다.

이제 오케스트레이션된 캠페인이 생성되어 워크플로 목록에서 사용할 수 있습니다. 이제 해당 시각적 캔버스에 액세스하여 수행할 작업을 추가, 구성 및 오케스트레이션할 수 있습니다. [오케스트레이션된 캠페인 활동을 오케스트레이션하는 방법을 알아보세요](orchestrate-activities.md).

## 캠페인 설정 구성

새 관리 설정 개요> 스키마, 실행 필드, 병합 정책. [자세히 알아보기](configuration-steps.md)

## 오케스트레이션된 캠페인 템플릿 작업 {#campaign-templates}

>[!CONTEXTUALHELP]
>id="ajo_workflow_template_for_campaign"
>title="오케스트레이션된 캠페인 템플릿"
>abstract="오케스트레이션된 캠페인 템플릿에는 오케스트레이션된 새 캠페인을 만드는 데 재사용할 수 있는 사전 구성된 설정과 활동이 포함되어 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_workflow_template_creation_properties"
>title="오케스트레이션된 캠페인 속성"
>abstract="오케스트레이션된 캠페인 템플릿에는 오케스트레이션된 새 캠페인을 만드는 데 재사용할 수 있는 사전 구성된 설정과 활동이 포함되어 있습니다. 이 화면에서는 오케스트레이션된 캠페인 템플릿의 레이블을 입력하고 내부 이름, 폴더 및 실행 폴더, 시간대, 감독자 그룹 등의 설정을 구성합니다."

오케스트레이션된 캠페인 템플릿에는 오케스트레이션된 새 캠페인을 만드는 데 재사용할 수 있는 사전 구성된 설정과 활동이 포함되어 있습니다. 오케스트레이션된 캠페인을 생성할 때 오케스트레이션된 캠페인 속성에서 오케스트레이션된 캠페인의 템플릿을 선택할 수 있습니다. 기본적으로 빈 템플릿이 제공됩니다.

오케스트레이션된 기존 캠페인으로 템플릿을 만들거나 처음부터 새 템플릿을 만들 수 있습니다. 두 방법 모두 아래에 자세히 설명되어 있습니다.

>[!BEGINTABS]

>[!TAB 오케스트레이션된 기존 캠페인에서 템플릿을 만듭니다]

기존의 오케스트레이션된 캠페인으로 오케스트레이션된 캠페인 템플릿을 만들려면 다음 단계를 수행합니다.

1. **Campaign** 메뉴를 열고 조정된 캠페인으로 이동하여 템플릿으로 저장합니다.
1. 오케스트레이션된 캠페인의 이름 오른쪽에 있는 세 점을 클릭하고 **템플릿으로 복사**&#x200B;를 선택합니다.
1. 팝업 창에서 템플릿 만들기를 확인합니다.
1. 오케스트레이션된 캠페인 템플릿 캔버스에서 필요에 따라 활동을 확인, 추가 및 구성합니다.
1. **설정** 단추에서 설정으로 이동하여 오케스트레이션된 캠페인 템플릿의 이름을 변경하고 설명을 입력하십시오.
1. 템플릿의 **폴더** 및 **실행 폴더**&#x200B;를 선택하십시오. 폴더는 오케스트레이션된 캠페인 템플릿이 저장된 위치입니다. 실행 폴더는 이 템플릿을 기반으로 생성된 오케스트레이션된 캠페인이 저장되는 폴더입니다.
1. 변경 내용을 저장합니다.

이제 오케스트레이션된 캠페인 템플릿을 템플릿 목록에서 사용할 수 있습니다. 이 템플릿을 기반으로 오케스트레이션된 캠페인을 만들 수 있습니다. 이 오케스트레이션된 캠페인은 템플릿에 정의된 설정 및 활동으로 사전 구성됩니다.


>[!TAB 처음부터 템플릿을 만듭니다]


오케스트레이션된 캠페인 템플릿을 처음부터 만들려면 다음 단계를 수행하십시오.

1. **캠페인** 메뉴를 열고 **템플릿** 탭으로 이동합니다. 사용 가능한 오케스트레이션된 캠페인 템플릿 목록을 볼 수 있습니다.
1. 화면 오른쪽 상단의 **[!UICONTROL 템플릿 만들기]** 단추를 클릭합니다.
1. 레이블을 입력하고 추가 옵션을 열어 오케스트레이션된 캠페인 템플릿에 대한 설명을 입력합니다.
1. 템플릿의 폴더 및 실행 폴더를 선택합니다. 폴더는 오케스트레이션된 캠페인 템플릿이 저장된 위치입니다. 실행 폴더는 이 템플릿을 기반으로 생성된 오케스트레이션된 캠페인이 저장되는 폴더입니다.
1. **만들기** 단추를 클릭하여 설정을 확인합니다.
1. 오케스트레이션된 캠페인 템플릿 캔버스에서 필요에 따라 활동을 추가하고 구성합니다.

   ![](assets/wf-template-activities.png){zoomable="yes"}

1. 변경 내용을 저장합니다.

이제 오케스트레이션된 캠페인 템플릿을 템플릿 목록에서 사용할 수 있습니다. 이 템플릿을 기반으로 오케스트레이션된 캠페인을 만들 수 있습니다. 이 오케스트레이션된 캠페인은 템플릿에 정의된 설정 및 활동으로 사전 구성됩니다.

>[!ENDTABS]
