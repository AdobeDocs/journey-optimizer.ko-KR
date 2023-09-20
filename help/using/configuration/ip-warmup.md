---
solution: Journey Optimizer
product: journey optimizer
title: IP 준비 계획 구현
description: IP 웜업 계획을 구현하는 방법 알아보기
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP, 풀, 그룹, 하위 도메인, 전달성
hide: true
hidefromtoc: true
source-git-commit: 1ac68f1b3a9657ce71a653011ab92fb817ca80b0
workflow-type: tm+mt
source-wordcount: '1529'
ht-degree: 2%

---

# IP 준비 계획 구현 {#ip-warmup}

<!--
>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_plan"
>title="Define your IP warmup plan"
>abstract="You can perform IP warmup workflows directly from the Journey Optimizer interface in a standardized and efficient way that follows the best practices for optimal deliverability."
-->

>[!AVAILABILITY]
>
>IP 웜업 기능은 현재 사용자를 선택하는 베타 버전으로만 사용할 수 있습니다. Beta 프로그램에 참여하려면 Adobe 고객 지원 센터에 문의해 주십시오.

포함 [!DNL Journey Optimizer]를 사용하면 최적의 전달성을 위한 모범 사례를 따르는 표준화되고 효율적인 방식으로 사용자 인터페이스에서 직접 IP 웜업 워크플로우를 쉽게 수행할 수 있습니다.

>[!CAUTION]
>
>이 기능은 이메일 채널에만 적용됩니다.

새로운 플랫폼을 사용해 이메일을 보낼 때 인터넷 서비스 제공자(ISP)는 인지되지 않은 IP 주소를 의심하게 된다. 대량의 이메일이 갑자기 전송되면 ISP는 해당 이메일을 스팸으로 표시하는 경우가 많습니다.

스팸으로 표시되지 않도록 하기 위해 IP 준비 계획 기능을 사용하여 전송되는 볼륨을 점진적으로 늘릴 수 있습니다. 관리 메뉴의 새 옵션을 사용하면 복잡한 여정을 만드는 대신 보다 원활하게 작업을 수행할 수 있습니다. 이를 통해 시작 단계를 원활하게 발전시키고 잘못된 주소의 전체 비율을 줄일 수 있습니다.

>[!NOTE]
>
>에서 IP warming을 사용하여 이메일 평판을 높이는 방법에 대해 자세히 알아보십시오. [전달성 모범 사례 안내서](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html).

<!--
Here are the main steps:

1. You get a deliverability plan from the deliverability consulting team.

1. Create a campaign - marketer [Learn more](#create-ip-warmup-campaign)

1. Your associated practitioner (customer's practitioner/ACS consultant/partner consultant) creates a IP warmup object in project and uploads a plan.

    The CSV manifests itself like below with numbers showing up with/without domain bifurcation. Below screen shows one phase (creative) with associated runs (The plan obviously has more such phases)

1. Practitioner associates the campaign and audience at phase level and turns on some settings as needed for all runs associated with a single creative/campaign

1. Then start to execute on every day basis by simply clicking the play button

1. Reports will continue to show up at campaign level with similar capabilities as today. NO enhancements in BETA. But the IP warmup plan also serves as a consolidated report at one single place of how many executions were done and so on

Benefits are as follows:

* No more creation of daily journeys and associated testing

* Standardization on Campaign which will be easy for practitioners too

* No more pain of creating queries, audiences and testing those as system will create the audiences. At phase level, system ensures that previously targeted + new profiles are picked up AND at iteration level, system ensures that each run is having unique profiles and the count matches what is stated in plan

* Ease of excluding domains and changing the plan with help of simple toggles to exclude OR by editing numbers inline or create new phases or reupload plan if drastic change. No more pain of editing audience definitions, journey conditions

* Single place to manage and view how IP warm is progressing.

* Consolidated report at creative/campaign level as all runs for a phase 

* There is an expectation that with this, it will ease around 30% of effort and will be much better experience for consultant/partner/practitioner - right from planning to execution to reporting
-->

IP 준비 계획을 구현하는 주요 단계는 다음과 같습니다.

* [IP 준비 캠페인 만들기](#create-ip-warmup-campaign)
* [IP 준비 계획 정의](#define-ip-warmup-plan)

## IP 준비 캠페인 만들기 {#create-ip-warmup-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_ip_warmup"
>title="IP 준비 계획 옵션 활성화"
>abstract="IP 웜업 플랜 활성화 옵션을 선택합니다. 캠페인이 라이브되면 IP 준비 플랜과 연결할 수 있습니다."

IP 준비 계획에 사용할 수 있도록 특정 옵션이 활성화된 캠페인을 하나 이상 만들어야 합니다. 아래 단계를 수행합니다.

1. 만들기 [표면](channel-surfaces.md) 준비 계획에 대해 식별한 도메인 및 IP에 대해 해당됩니다.

1. 만들기 [campaign](../campaigns/create-campaign.md) 및 선택 [이메일](../email/create-email.md#create-email-journey-campaign) 작업.

1. IP 웜업을 위해 생성한 서피스를 선택합니다.

   <!--You must use the same surface as the one that will be used for the asociated IP warmup plan. [Learn how to create an IP warmup plan](#create-ip-warmup-plan)-->

1. **[!UICONTROL 만들기]**&#x200B;를 클릭합니다.

1. 다음에서 **[!UICONTROL 예약]** 섹션, 선택 **[!UICONTROL IP 준비 계획 활성화]**.

   ![](assets/ip-warmup-campaign-plan-activation.png)

   캠페인 [예약](../campaigns/create-campaign.md#schedule) 는 와 연결될 IP 준비 계획에 따라 구동되며, 이는 일정이 캠페인 자체에 더 이상 정의되어 있지 않음을 의미합니다.

1. [활성화](../campaigns/review-activate-campaign.md) 캠페인. 라이브 상태가 되면 IP 준비 계획에 사용할 수 있습니다.

>[!NOTE]
>
>IP 준비 계획이 활성화된 라이브 캠페인의 경우 **[!UICONTROL 삭제]** 단추는 IP 준비 계획과 연결될 때까지 사용할 수 있습니다.

캠페인 구성 방법에 대한 자세한 내용은 다음을 참조하십시오. [이 페이지](../campaigns/get-started-with-campaigns.md).

## IP 준비 계획 정의 {#define-ip-warmup-plan}

### IP 준비 계획 관리 {#manage-ip-warmup-plans}

1. 액세스 **[!UICONTROL 관리]** > **[!UICONTROL 채널]** > **[!UICONTROL IP 준비 계획]** 메뉴 아래의 제품에서 사용할 수 있습니다. 지금까지 만든 모든 IP 준비 계획이 표시됩니다.

   ![](assets/ip-warmup-filter-list.png)

1. 상태를 필터링할 수 있습니다. 다양한 상태는 다음과 같습니다.

   * **시작되지 않음**: 실행이 발생하지 않았습니다
   * **진행 중**: 한 번의 실행이 시작되자마자 <!--or is done?-->
   * **일시 중지됨**
   * **완료됨**: 플랜의 모든 실행이 완료되었습니다

1. IP 준비 계획을 삭제하려면 **[!UICONTROL 삭제]** 아이콘을 클릭하여 목록 항목 옆에 있는 삭제를 확인합니다.

   ![](assets/ip-warmup-delete-plan.png)

   >[!CAUTION]
   >
   >선택한 IP 준비 계획이 영구적으로 삭제됩니다.

### IP 준비 계획 만들기 {#create-ip-warmup-plan}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_upload"
>title="IP 준비 계획 지정"
>abstract="CSV 템플릿을 다운로드하고 IP 웜업 단계 및 대상 프로필 수에 대한 데이터로 채웁니다."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_surface"
>title="마케팅 표면 선택"
>abstract="IP 준비 계획과 연결할 캠페인에서 선택한 서피스와 동일한 서피스를 선택해야 합니다."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html" text="채널 표면 설정"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html" text="IP 준비 캠페인 만들기"

>[!CAUTION]
>
>IP 준비 계획을 만들고, 편집하고, 삭제하려면 **[!UICONTROL 전달성 컨설턴트]** 권한.
<!--Learn more on managing [!DNL Journey Optimizer] users' access rights in [this section](../administration/permissions-overview.md).-->

하나 이상의 라이브 캠페인이 **[!UICONTROL IP 준비 계획 활성화]** 활성화된 옵션이 활성화되면 IP 준비 계획과 연결할 수 있습니다.

>[!CAUTION]
>
>게재 컨설턴트와 협력하여 IP 준비 계획 템플릿이 올바르게 설정되었는지 확인합니다. <!--TBC-->

1. 액세스 **[!UICONTROL 관리]** > **[!UICONTROL 채널]** > **[!UICONTROL IP 준비 계획]** 메뉴를 선택한 다음 **[!UICONTROL IP 준비 계획 만들기]**.

   ![](assets/ip-warmup-create-plan.png)

1. IP 준비 계획 세부 사항을 입력합니다. 이름과 설명을 입력합니다.

   ![](assets/ip-warmup-plan-details.png)

1. 선택 [표면](channel-surfaces.md). 마케팅 표면만 선택할 수 있습니다. [이메일 유형에 대해 자세히 알아보기](../email/email-settings.md#email-type)

   >[!CAUTION]
   >
   >IP 준비 계획과 연결할 캠페인에서 선택한 서피스와 동일한 서피스를 선택해야 합니다. [IP 준비 캠페인을 만드는 방법을 알아봅니다.](#create-ip-warmup-campaign)

1. IP 준비 계획이 포함된 Excel 파일 업로드<!--which formats are allowed?-->. 게재 가능성 팀이 제공한 템플릿을 사용할 수 있습니다.<!--TBC?--> [자세히 알아보기](#upload-plan)
   <!--
    You can also download the Excel template from the [!DNL Journey Optimizer] user interface and upload it after filling it with the IP warmup details.-->

   ![](assets/ip-warmup-upload-success.png)

1. **[!UICONTROL 만들기]**&#x200B;를 클릭합니다. 업로드한 파일에 정의된 단계 수가 자동으로 표시되면 각 단계에 대한 모든 실행이 실행됩니다. [자세히 알아보기](#upload-plan)

   ![](assets/ip-warmup-plan-phases.png)

### IP 준비 계획 다시 업로드 {#re-upload-plan}

해당 버튼을 사용하여 다른 IP 웜업 계획을 다시 업로드할 수 있습니다.

![](assets/ip-warmup-re-upload-plan.png)

>[!NOTE]
>
>IP 준비 계획 세부 사항은 새로 업로드한 파일에 따라 변경됩니다. 전체 실행 및 활성화된 실행은 영향을 받지 않습니다.

### 플랜이 포함된 파일 업로드 {#upload-plan}

다음은 IP 웜업 플랜이 포함된 파일의 예입니다.

![](assets/ip-warmup-sample-file.png)

각 단계는 단일 캠페인을 할당할 여러 실행으로 구성된 기간에 해당합니다.

각 실행에 대해 특정 수의 수신자가 있으며 이 실행이 실행될 날짜를 정의합니다.

전달하려는 도메인에 대해 원하는 만큼 열을 가질 수 있습니다. 이 예에는 세 개의 열, 즉 Gmail, Adobe 및 기타 열이 있습니다. 즉,

첫 번째 단계에서 더 많은 실행을 수행하고, 실행 수를 줄이면서 타겟팅된 주소의 수를 점진적으로 늘리는 것이 좋습니다.

### 단계 정의 {#define-phases}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_campaigns_excluded"
>title="제외할 캠페인 대상 선택"
>abstract="현재 단계에서 제외하려는 다른 캠페인에서 대상을 선택합니다."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_domains_excluded"
>title="제외할 도메인 그룹 선택"
>abstract="현재 단계에서 제외할 도메인을 선택합니다."

1. 각 단계에 대해 이 IP 준비 계획 단계와 연결할 캠페인을 선택합니다.

   ![](assets/ip-warmup-plan-select-campaign.png)

   다음 사항을 참고하십시오.

   * 이 포함된 캠페인만 **[!UICONTROL IP 준비 계획 활성화]** 옵션 활성화됨 <!--and live?--> 선택할 수 있습니다. [자세히 알아보기](#create-ip-warmup-campaign)

   * 현재 IP 준비 계획에 대해 선택한 것과 동일한 표면을 사용하는 캠페인을 선택해야 합니다.

   * 다른 IP 준비 캠페인에서 이미 사용 중인 캠페인은 선택할 수 없습니다.

1. 각 단계에 대해 다음 사항이 적용됩니다.

   * **[!UICONTROL 프로필 제외]** - 해당 단계의 이전 실행 프로필은 항상 제외됩니다. 예를 들어, Leo가 처음 6300명의 대상#1 선정되면 시스템이 자동으로 Leo가 메일을 #2 받지 못하도록 합니다.

   * **[!UICONTROL 캠페인 대상자 제외됨]** - 다른 대상에서 대상 선택 <!--executed/live?-->현재 단계에서 제외하려는 캠페인.

     예를 들어, 단계를 실행하고 있고 어떤 이유에서든 단계를 분할해야 할 수 있습니다. 이런 경우 2단계에서는 1단계에서 사용한 캠페인을 이 섹션에 포함시켜 2단계에서는 1단계에서 이전에 연락한 사람이 포함되지 않도록 할 것입니다. 이는 동일한 IP 준비 계획에 사용된 캠페인뿐만 아니라 다른 IP 준비 계획에서도 수행할 수 있습니다.

   * **[!UICONTROL 도메인 그룹 제외됨]** - 해당 단계에서 제외할 도메인(예: Gmail)을 선택합니다. <!--??-->

     며칠 동안 IP 워밍업을 실행한 후에는 도메인을 사용한 ISP 평판이 hotmail이 좋지 않음을 알고 ISP로 해결하려고 하지만 IP 워밍업 계획을 중지하지 않으려고 합니다. 이 경우 도메인 그룹 hotmail을 제외된 범주에 넣을 수 있습니다.

     >[!NOTE]
     >
     >도메인 제외에는 실행되지 않는 단계가 필요하므로 제외를 추가하려면 실행 단계를 분할해야 할 수 있습니다. 마찬가지로 도메인 그룹이 OOTB 도메인 그룹이 아닌 경우 Excel에서 도메인 그룹을 만들고 업로드한 다음 동일한 그룹을 제외해야 할 수 있습니다.

   ![](assets/ip-warmup-plan-phase-1.png)

1. 필요한 경우 단계를 추가할 수 있습니다. 마지막 현재 단계 이후에 추가됩니다. 사용 **[!UICONTROL 단계 삭제]** 단추를 클릭하여 원하지 않는 단계를 제거합니다.

   ![](assets/ip-warmup-plan-add-delete-phases.png)

   >[!CAUTION]
   >
   >실행을 취소할 수 없습니다. **[!UICONTROL 삭제]** 작업.
   >
   >IP 준비 계획에서 모든 단계를 삭제하는 경우 계획을 다시 업로드하는 것이 좋습니다.

### 실행 정의 {#define-runs}

1. 각 실행에 대한 일정을 선택합니다. <!--which is actually a window of opportunity. meaning? how many hours? shall we specify that to clarify?-->

   ![](assets/ip-warmup-plan-send-time.png)

1. 종료 시간을 선택합니다. 이는 기본적으로 대상자 작업이 지연되는 경우 준비 캠페인을 실행할 수 있는 창을 의미합니다. 지정하지 않으면 시작 시간에 시도하고 실패합니다. 종료 시간이 제공되면 해당 창 사이의 실행이 실행됩니다.

1. 각 실행을 활성화합니다. 세분화 작업을 실행할 수 있도록 시간을 충분히 일찍 예약하십시오. <!--explain how you can evaluate a proper time-->

   >[!CAUTION]
   >
   >각 실행은 실제 전송 시간보다 최소 12시간 전에 활성화되어야 합니다. 그렇지 않으면 세그먼테이션이 완료되지 않을 수 있습니다. <!--How do you know when segmentation is complete? Is there a way to prevent user from scheduling less than 12 hours before the segmentation job?-->

1. 캠페인 실행이 시작되지 않은 경우 실행을 중단할 수 있습니다.

   캠페인 실행이 시작되면 **[!UICONTROL 중지]** 버튼을 사용할 수 없게 됩니다. <!--TBC in UI-->

   ![](assets/ip-warmup-plan-stop-run.png)

1. 실행을 추가하려면 다음을 선택합니다. **[!UICONTROL 아래에 실행 추가]** 점 세 개 아이콘에서

   ![](assets/ip-warmup-plan-run-more-actions.png)

1. 언제든지 특정 실행에서 시작하는 다른 캠페인을 사용하려면 다음을 선택합니다. **[!UICONTROL 새 단계로 분할 옵션]** 점 세 개 아이콘에서 현재 단계의 나머지 실행에 대해 새 단계가 생성됩니다. 다음 단계 [위](#define-phases) 새 단계를 정의합니다.

   예를 들어 실행 #4에 대해 이 옵션을 선택하면 #8에 #4 실행이 새 단계로 이동됩니다.

<!--
You don't have to decide the campaign upfront. You can do a split later. It's a work in progress plan: you activate one run at a time with a campaign and you always have the flexibility to modify it while working on it.

But need to explain in which case you want to modify campaigns, provide examples
-->

실행은 다음과 같은 상태를 가질 수 있습니다<!--TBC with Medha-->:

* **[!UICONTROL 완료됨]**:
* **[!UICONTROL 실패]**:
* **[!UICONTROL 취소됨]**: 캠페인 실행이 시작되기 전에 실행을 중지했습니다.

