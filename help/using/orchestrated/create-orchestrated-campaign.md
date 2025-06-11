---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer을 사용하여 오케스트레이션된 캠페인 만들기 및 예약
description: Adobe Journey Optimizer으로 오케스트레이션된 캠페인을 만드는 방법을 알아봅니다
badge: label="Alpha"
hide: true
exl-id: 13da680d-fef8-4749-9190-8ca3d77b060a
source-git-commit: 38d4cc896414fce2e8453940fb4674ce7e60fd2b
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 17%

---


# 오케스트레이션된 캠페인 만들기 및 예약 {#create-first-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_creation_workflow"
>title="오케스트레이션된 캠페인 목록"
>abstract="**오케스트레이션** 탭에 오케스트레이션된 모든 캠페인이 나열됩니다. 오케스트레이션된 캠페인의 이름을 클릭하여 편집할 수 있습니다. 오케스트레이션된 새 캠페인을 추가하려면 **오케스트레이션된 캠페인 만들기** 버튼을 사용합니다."

## 캠페인 만들기 {#create}

오케스트레이션된 캠페인을 만들려면 다음 단계를 수행합니다.

1. **[!UICONTROL 캠페인]** 메뉴로 이동하여 **[!UICONTROL 오케스트레이션]** 탭을 선택하고 **[!UICONTROL 캠페인 만들기]**&#x200B;를 선택합니다.

   ![](assets/inventory-create.png)

1. 오케스트레이션된 캠페인의 이름을 입력합니다. 또한 전용 필드에 설명을 추가하는 것이 좋습니다.

1. (선택 사항) **태그** 필드를 사용하여 오케스트레이션된 캠페인에 Adobe Experience Platform 통합 태그를 할당합니다. 태그를 할당하면 캠페인을 간단히 분류하고 캠페인 목록에서 편하게 검색할 수 있습니다. [태그를 사용하여 작업하는 방법을 알아봅니다](../start/search-filter-categorize.md#tags).

1. 확인하려면 **[!UICONTROL 만들기]** 단추를 클릭하세요.


이제 오케스트레이션된 캠페인을 캠페인 목록에서 만들고 사용할 수 있습니다. 언제든지 캠페인 캔버스에서 ![캠페인 설정 아이콘](assets/do-not-localize/campaign-settings.svg) 아이콘을 클릭하여 이러한 속성을 변경할 수 있습니다.


## 캠페인 예약 {#schedule}

기본적으로 오케스트레이션된 캠페인은 수동으로 활성화되면 시작되고 활동이 실행되는 즉시 종료됩니다.

활성화 직후 오케스트레이션된 캠페인을 실행하지 않으려면 실행해야 하는 날짜와 시간을 지정할 수 있습니다. 다양한 기준에 따라 정기적인 빈도로 캠페인을 실행할 수도 있습니다.

캠페인의 일정을 구성하려면 오케스트레이션된 캠페인을 열고 **[!UICONTROL 가능한 한 빨리]** 단추를 클릭하십시오.

![](assets/create-schedule.png)

<!--In the Execution frequency field, select 

time zone

daily, weekly, monthly
several times a day based on specific hours or periodically

recurring frequencies (all except as soon and once)
preview launch times
validity period

>[!NOTE]
>
>When scheduling campaigns in [!DNL Adobe Journey Optimizer], ensure your start date/time aligns with the desired first delivery. For recurring campaigns, if the initial scheduled time has already passed, the campaigns will roll over to the next available time slot according to their recurrence rules.

## Work with orchestrated campaign templates {#campaign-templates}

>[!CONTEXTUALHELP]
>id="ajo_workflow_template_for_campaign"
>title="Orchestrated campaign templates"
>abstract="Orchestrated campaign templates contain pre-configured settings and activities which can be reused for creating new orchestrated campaign."

>[!CONTEXTUALHELP]
>id="ajo_workflow_template_creation_properties"
>title="Orchestrated campaign properties"
>abstract="Orchestrated campaign templates contain pre-configured settings and activities which can be reused for creating new orchestrated campaigns. In this screen, enter the label of the orchestrated campaign template and configure its settings such as its internal name, folder and execution folders, timezone, and supervisor group."

Orchestrated campaign templates contain pre-configured settings and activities which can be reused for creating new orchestrated campaigns. You can select the template of your orchestrated campaign from the orchestrated campaign properties, when creating an orchestrated campaign. An empty template is provided by default.

You can create a template from an existing orchestrated campaign, or create a new template from scratch. Both methods are detailed below.

>[!BEGINTABS]

>[!TAB Create a template from an existing orchestrated campaign]

To create an orchestrated campaign template from an existing orchestrated campaign, follow these steps:

1. Open to the **Campaign** menu and browse to the orchestrated campaign to save as a template.
1. Click the three dots on the right of the name of the orchestrated campaign, and choose **Copy as template**.
1. In the popup window, confirm the template creation.
1. In the orchestrated campaign template canvas, check, add, and configure the activities as needed.
1. Browse to the settings, from the **Settings** button, to change the name of the orchestrated campaign template, and enter a description.
1. Select the **folder** and **execution folder** of the template. The folder is the location where the orchestrated campaign template is saved. The execution folder is the folder where orchestrated campaigns created based on this template are saved.
1. Save your changes. 

The orchestrated campaign template is now available in the template list. You can create an orchestrated campaign based on this template. This orchestrated campaign will be pre-configured with the settings and activities defined in the template.


>[!TAB Create a template from scratch]


To create an orchestrated campaign template from scratch, follow these steps:

1. Open to the **Campaign** menu and browse to the **Templates** tab. You can see the list of available orchestrated campaign templates.
1. Click the **[!UICONTROL Create template]** button in the upper-right corner of the screen.
1. Enter the label and open the additional options to enter a description of your orchestrated campaign template.
1. Select the folder and execution folder of the template. The folder is the location where the orchestrated campaign template is saved. The execution folder is the folder where orchestrated campaigns created based on this template are saved.
1. Click the **Create** button to confirm your settings.
1. In the orchestrated campaign template canvas, add and configure the activities as needed.

     ![](assets/wf-template-activities.png){zoomable="yes"}

1. Save your changes. 

The orchestrated campaign template is now available in the template list. You can create an orchestrated campaign based on this template. This orchestrated campaign will be pre-configured with the settings and activities defined in the template.

>[!ENDTABS]






## Next steps {#next}

Once your campaign configuration and content are ready, you can review and activate it. [Learn more](review-activate-campaign.md)

-->