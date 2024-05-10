---
solution: Journey Optimizer
product: journey optimizer
title: IP 준비 계획 실행
description: IP 준비 계획을 실행하고 모니터링하는 방법에 대해 알아봅니다.
feature: IP Warmup Plans
topic: Administration
role: Admin
level: Experienced
keywords: IP, 그룹, 하위 도메인, 전달성
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 752ffd7f-09c2-4aa3-a067-2dbe0634709c
source-git-commit: 737b7f59819d235b1f637d4a6b996e97cfddb9fe
workflow-type: tm+mt
source-wordcount: '2153'
ht-degree: 14%

---

# IP 준비 계획 실행 {#ip-warmup-running}

>[!BEGINSHADEBOX]

이 설명서의 내용:

* [IP 준비 계획 시작](ip-warmup-gs.md)
* [IP 워밍업 캠페인 만들기](ip-warmup-campaign.md)
* [IP 준비 계획 만들기](ip-warmup-plan.md)
* **[IP 준비 계획 실행](ip-warmup-execution.md)**

>[!ENDSHADEBOX]

다음 작업을 완료하면 [ip 준비 계획을 만들었습니다.](ip-warmup-plan.md) 게재 컨설턴트와 함께 준비한 파일을 업로드하면 플랜에서 단계 및 실행을 정의할 수 있습니다.

각 단계는 단일 캠페인으로 할당되는 여러 실행으로 구성됩니다.

## 단계 정의 {#define-phases}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_campaigns_excluded"
>title="캠페인 대상자 제외"
>abstract="현재 단계에서 대상자를 제외할 캠페인을 선택합니다. 이는 이전에 다른 단계에서 연락을 보낸 프로필이나 다른 IP 워밍업 플랜이 다시 대상으로 지정되는 것을 방지하기 위한 것입니다."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_domains_excluded"
>title="도메인 그룹 제외"
>abstract="현재 단계에서 제외하려는 도메인을 선택합니다. 도메인 제외에는 미실행 단계가 필요하므로 제외를 추가하려면 실행 단계를 분할해야 할 수 있습니다."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/implement-ip-warmup-plan/ip-warmup-execution.html?lang=ko-KR#split-phase" text="단계 분할"

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_phases"
>title="플랜의 단계 정의"
>abstract="각 단계는 단일 캠페인으로 할당되는 여러 실행으로 구성됩니다."

<!--You need to associate the campaign and audience at phase level and turns on some settings as needed for all runs associated with a single creative/campaign

At phase level, system ensures that previously targeted + new profiles are picked up AND at iteration level, system ensures that each run is having unique profiles and the count matches what is stated in plan-->

<!--![](assets/ip-warmup-plan-phase-1.png)-->

1. 각 단계에 대해 이 IP 준비 계획 단계와 연결할 캠페인을 선택합니다.

   >[!NOTE]
   >
   >다른 IP 준비 계획에서 이미 사용 중인 캠페인은 선택할 수 없습니다. 그러나 동일한 IP 웜업 계획의 하나 이상의 단계에서 동일한 캠페인을 사용할 수 있습니다.

   ![](assets/ip-warmup-plan-select-campaign.png)

   >[!IMPORTANT]
   >
   >* 이 포함된 캠페인만 **[!UICONTROL IP 준비 계획 활성화]** 활성화된 옵션은 선택할 수 있습니다. [자세히 알아보기](#create-ip-warmup-campaign)
   >
   >* 현재 IP 준비 계획에 대해 선택한 것과 동일한 표면을 사용하는 캠페인을 선택해야 합니다.

1. 현재 단계에 대해 캠페인을 선택하면 프로필, 캠페인 대상자 및 도메인 그룹을 제외하는 섹션이 표시됩니다.

   >[!NOTE]
   >
   >실행이 활성화되면 사용자가 아닌 이상 제외를 수정할 수 없습니다. [실행 분할](#split-phase) 새로운 단계로 넘어갑니다.

   1. 다음에서 **[!UICONTROL 프로필 제외]** 섹션에서 해당 단계의 이전 실행의 프로필이 항상 제외되어 있음을 확인할 수 있습니다. 예를 들어 실행 시 타겟팅되#1 처음 4800명에서 프로필이 포함된 경우 시스템은 동일한 프로필이 실행 시 이메일을 수신하지 않도록 자동으로 #2.

      >[!NOTE]
      >
      >이 섹션은 편집할 수 없습니다.

   1. 다음에서 **[!UICONTROL 캠페인 대상자 제외됨]** 섹션에서 현재 단계에서 제외할 대상자에 해당하는 캠페인을 선택합니다.

      ![](assets/ip-warmup-plan-exclude-campaigns.png)

      예를 들어 1단계를 실행하는 동안 [분할하기](#split-phase) 어떤 이유에서든. 따라서 1단계에서 사용된 캠페인을 제외하여 1단계에서 이전에 연락한 프로필이 2단계에 포함되지 않도록 할 수 있습니다. 다른 IP 준비 계획에서 캠페인을 제외할 수도 있습니다.

   1. 다음에서 **[!UICONTROL 도메인 그룹 제외됨]** 섹션에서 해당 단계에서 제외할 도메인을 선택합니다.

      >[!NOTE]
      >
      >도메인 제외에는 실행되지 않는 단계가 필요하므로 다음을 수행해야 할 수 있습니다. [실행 단계 분할](#split-phase) 제외를 추가합니다.

      ![](assets/ip-warmup-plan-exclude-domains.png)

      예를 들어 며칠 동안 IP 웜업을 실행한 후에는 도메인(예: Adobe)에 대한 ISP 평판이 좋지 않음을 깨닫고 IP 웜업 계획을 중지하지 않고 이를 해결하려고 합니다. 이러한 경우 Adobe 도메인 그룹을 제외할 수 있습니다.

      >[!NOTE]
      >
      >에 추가된 사용자 정의 도메인 그룹만 제외할 수 있습니다. [IP 준비 계획 템플릿](ip-warmup-plan.md#prepare-file). 그렇지 않은 경우 제외할 사용자 정의 도메인 그룹으로 템플릿을 업데이트하고 [플랜 다시 업로드](#re-upload-plan).

1. 필요한 경우 **[!UICONTROL 캠페인 바꾸기]** 단추를 클릭합니다.

   ![](assets/ip-warmup-plan-replace-campaign.png)

   >[!NOTE]
   >
   >이 작업은 단계의 첫 번째 실행을 활성화하기 전에만 가능합니다. 실행이 활성화되면 다음을 수행하지 않는 한 캠페인을 교체할 수 없습니다. [실행 분할](#split-phase) 새로운 단계로 넘어갑니다.

1. 필요한 경우 단계를 추가할 수 있습니다. 마지막 현재 단계 이후에 추가됩니다.

   ![](assets/ip-warmup-plan-add-phase.png)

1. 사용 **[!UICONTROL 단계 삭제]** 단추를 클릭하여 원하지 않는 단계를 제거합니다. 이 작업은 한 단계에서 실행이 실행되지 않는 경우에만 사용할 수 있습니다. <!--Once a run is executed, deletion is not allowed.-->

   >[!CAUTION]
   >
   >실행을 취소할 수 없습니다. **[!UICONTROL 삭제]** 작업.

   ![](assets/ip-warmup-plan-delete-phase.png)

   >[!NOTE]
   >
   >IP 준비 계획에서 모든 단계를 삭제하는 경우 계획을 다시 업로드하는 것이 좋습니다. [자세히 알아보기](#re-upload-plan)

## 실행 정의 {#define-runs}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_run"
>title="각 실행 정의"
>abstract="모든 단계에 대해 각각의 실행을 정의하고 활성화합니다."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_last_engagement"
>title="참여 필터링"
>abstract="이 열은 예를 들어 지난 20일 동안 해당 브랜드에 참여한 사용자만 대상으로 하는 필터입니다. **실행 편집** 옵션을 통해 이 설정을 변경할 수도 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_retry"
>title="기간 설정"
>abstract="세분화 작업에서 지연이 발생하는 경우 IP 워밍업 캠페인을 실행할 수 있는 기간을 정의할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_pause"
>title="대상자 오류가 있는 실행 취소"
>abstract="해당 실행에 대해 대상자가 평가된 후 적격 프로필이 대상이 되는 프로필보다 적은 경우에 실행을 취소하려면 이 옵션을 선택합니다."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_qualified"
>title="적격 프로필 보기"
>abstract="이 열에 적격 프로필 수가 표시됩니다. 대상자가 실행에 대해 평가된 후 적격 프로필보다 대상이 되는 프로필이 더 많은 경우 **Pause for errors(오류로 인해 일시 중지)** 옵션이 활성화된 경우가 아니라면 실행은 계속 실행됩니다. 해당 경우 실행은 취소됩니다."

1. 지정된 시간에 실행되도록 각 실행에 대한 일정을 선택합니다.

   ![](assets/ip-warmup-plan-send-time.png)

1. 선택적으로, 다음에 지연이 있을 경우 IP 워밍업 캠페인을 실행할 수 있는 기간 을 정의할 수 있습니다. [대상자 평가](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html#how-segmentation-works){target="_blank"}. 이렇게 하려면 계획 이름 옆에 있는 왼쪽 상단의 등록 정보 아이콘을 누르고 **[!UICONTROL 재시도 실행 시간]** 드롭다운 목록에서 지속 시간을 선택합니다(최대 240분(4시간)).

   >[!NOTE]
   >
   >정의된 기간이 끝날 때까지 30분마다 다시 시도합니다.

   ![](assets/ip-warmup-plan-retry-run-time.png)

   예를 들어, 지정된 일에 전송 시간을 오전 9시로 설정하고 120분을 다시 시도 실행 시간으로 선택하면 대상 평가에서 예상치 못한 지연에 대해 2시간(오전 9시 - 오전 11시)의 기회 창을 실행할 수 있습니다.

   >[!NOTE]
   >
   >기간을 지정하지 않으면 전송 시간에 실행이 시도되며 대상 평가가 완료되지 않으면 실패합니다.

1. 필요한 경우 다음을 선택합니다 **[!UICONTROL 실행 편집]** 추가 작업 아이콘에서 참조할 수 있습니다. 여기에서 각 열의 주소 수를 업데이트할 수 있습니다. 다음을 업데이트할 수도 있습니다. **[!UICONTROL 마지막 참여]** 지난 20일 동안의 브랜드와 관련된 사용자만 타겟팅하는 필드.

   >[!NOTE]
   >
   >게재 가능성 전문가와 상의하여 이 숫자들을 수정하는 것이 좋습니다.

   ![](assets/ip-warmup-plan-edit-run.png)

   >[!NOTE]
   >
   >실행에 참여 기간을 적용하지 않으려면 **[!UICONTROL 마지막 참여]** 필드.

1. 다음 항목 선택 **[!UICONTROL 오류 발생 시 일시 중지]** 대상이 해당 실행에 대해 평가된 후 자격이 있는 프로필이 타겟팅된 프로필보다 적은 경우 실행을 취소하는 옵션입니다. 이 경우 실행은 **[!UICONTROL 실패]** 상태.

   ![](assets/ip-warmup-plan-pause.png)

1. **[!UICONTROL 활성화]** 달리기. [자세히 알아보기](#activate-run)

1. 이 실행의 상태가 (으)로 변경됩니다. **[!UICONTROL 라이브]**: 시스템이 실행 예약 요청을 수락했음을 의미합니다.

   >[!NOTE]
   >
   >다양한 실행 상태가 다음에 나열됩니다. [이 섹션](#monitor-plan).

1. 캠페인 실행이 시작되지 않은 경우 라이브 실행을 중단할 수 있습니다. 이 작업 액션은 실행 일정을 취소하며 전송을 중지하지 않습니다.

   ![](assets/ip-warmup-plan-stop-run.png)

   >[!NOTE]
   >
   >캠페인 실행이 시작되면 **[!UICONTROL 중지]** 버튼을 사용할 수 없게 됩니다.

1. 실행을 추가하려면 다음을 선택합니다. **[!UICONTROL 아래에 실행 추가]** 추가 작업 아이콘에서 참조할 수 있습니다.

   ![](assets/ip-warmup-plan-run-more-actions.png)

## 실행 활성화 {#activate-run}

실행을 활성화하려면 **[!UICONTROL 활성화]** 단추를 클릭합니다. 그런 다음 매일 다음 실행을 활성화할 수 있습니다.

을(를) 허용할 충분한 시간을 예약했는지 확인하십시오. [대상자 평가](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html#how-segmentation-works){target="_blank"} 실행할 수 있습니다.

![](assets/ip-warmup-plan-activate.png)

>[!CAUTION]
>
>각 실행은 실제 전송 시간보다 최소 12시간 전에 활성화되어야 합니다. 그렇지 않으면 대상 평가가 완료되지 않을 수 있습니다.

실행을 활성화하면 여러 대상이 자동으로 만들어집니다.

* 단계의 첫 번째 실행을 활성화하는 경우:

   * An [대상자](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html){target="_blank"} 제외된 캠페인 대상자(있는 경우)에 대해 다음 명명 규칙을 사용하여 만들어집니다. `<warmupName>_Phase<phaseNo>-Audience Exclusion`.

   * 제외된 도메인 그룹(있는 경우)에 대해 다음 명명 규칙을 사용하여 다른 대상이 만들어집니다. `<warmupName>_Phase<phaseNo>-Domain Exclusion`.

  >[!NOTE]
  >
  >대상자는 준비 계획이 완료된 것으로 표시된 후에 정리됩니다.
  >
  >후속 단계에 대해 제외된 캠페인 대상이나 도메인 그룹에 변경 사항이 없는 경우 새 대상자가 만들어지지 않습니다.

* 모든 실행을 활성화할 때:

   * 다음 명명 규칙을 사용하여 마지막 참여 필터에 대해 다른 대상자가 만들어집니다. `<warmupName>_Phase<phaseNo>_Run<runNo>-Engagement Filter`.

     >[!NOTE]
     >
     >대상자는 준비 계획이 완료된 것으로 표시된 후 정리됩니다.
     >
     >후속 단계에 대한 마지막 참여 필터가 변경되지 않은 경우 시스템에서 새 대상을 만들지 않습니다.

   * An [대상자 구성](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/audience-composition.html?lang=ko){target="_blank"} 은 다음 명명 규칙을 사용하여 캠페인이 전송될 대상자에 따라 만들어집니다. `<warmupName>-Phase<phaseNo>-Run<runNo>`.

     >[!NOTE]
     >
     >실행 시마다 새 대상자 작성이 생성됩니다.
     >
     >다음 반복이 활성화될 때 대상 구성(및 출력 대상)이 정리됩니다.

<!--How do you know when segmentation is complete? Is there a way to prevent user from scheduling less than 12 hours before the segmentation job?-->

<!--Sart to execute on every day basis by simply clicking the play button > for each run? do you have to come back every day to activate each run? or can you schedule them one after the other?)-->

<!--Upon activation, when the segment evaluation happens, more segments will be created by the IP warmup service and will be leveraged in an audience composition and a new audience will be created for each run splitted into the different selected domains.-->

## 플랜 모니터링 {#monitor-plan}

IP 준비 계획을 성공적으로 실행하려면 보고서를 모니터링하고 실행을 활성화하고 매일 상태를 확인해야 합니다.

### 강조 표시 섹션 사용 {#highlights}

단계에 대해 첫 번째 실행이 활성화되면 **[!UICONTROL 강조 표시]** 섹션이 표시됩니다.

현재 실행과 향후 실행에 대한 빠른 개요를 제공합니다. 이 섹션에서 다음 실행을 편집하고 활성화할 수도 있습니다.

![](assets/ip-warmup-plan-highlights.png)

### 실행 상태 확인 {#run-statuses}

IP 워밍업 계획 자체가 한 곳에서 통합 보고서 역할을 한다. 의 수와 같은 요소를 확인할 수 있습니다. **[!UICONTROL 라이브]** 또는 **[!UICONTROL 완료됨]** 는 각 단계에 대해 실행되며 IP 웜업 계획이 어떻게 진행되고 있는지 확인합니다.

>[!NOTE]
>
>가장 좋은 방법은 IP 준비 계획을 매일 모니터링하는 것입니다.

실행은 다음과 같은 상태를 가질 수 있습니다.

* **[!UICONTROL 초안]** : 실행이 생성될 때마다 [새 계획 생성](ip-warmup-plan.md) 또는 [실행 추가](#define-runs) 사용자 인터페이스에서 **[!UICONTROL 초안]** 상태.
* **[!UICONTROL 라이브]**: 실행을 활성화할 때마다 **[!UICONTROL 라이브]** 상태. 즉, 전송이 시작된 것이 아니라 시스템이 실행 예약 요청을 수락했습니다.
* **[!UICONTROL 완료됨]**: 이 실행에 대한 캠페인 실행이 완료되었습니다. <!--i.e. campaign execution has started, no error happened and emails have reached users? to check with Sid-->
* **[!UICONTROL 취소됨]**: a **[!UICONTROL 라이브]** 을(를) 사용하여 실행이 취소되었습니다. **[!UICONTROL 중지]** 단추 또는 를 활성화한 경우 **[!UICONTROL 오류 발생 시 일시 중지]** 옵션과 오류가 발생했습니다. [자세히 알아보기](#define-runs)
* **[!UICONTROL 실패]**: 시스템에서 오류가 발생하거나 현재 단계에 사용되는 캠페인이 중지되었습니다. 실행이 실패할 경우 다음 날 다른 실행을 예약할 수 있습니다.

### 보고서 사용 {#reports}

보다 일반적으로 플랜의 영향을 측정하기 위해 다음을 사용하여 IP 준비 캠페인의 성과를 확인할 수 있습니다. [!DNL Journey Optimizer] 캠페인 보고서. 이렇게 하려면 완료된 각 실행에 대해 **[!UICONTROL 보고서 보기]** 단추를 클릭합니다. Campaign 이메일에 대해 자세히 알아보기 [라이브 보고서](../reports/campaign-live-report.md#email-live) 및 [글로벌 보고서](../reports/campaign-global-report.md#email-global).

![](assets/ip-warmup-plan-reports.png)

다음에서 보고서에 액세스할 수도 있습니다 [캠페인 메뉴](../campaigns/modify-stop-campaign.md#access) 다른 캠페인을 사용할 수 있습니다.

## 플랜 관리 {#manage-plan}

어느 시점에서 IP 준비 계획이 예상대로 수행되지 않으면 아래 작업을 수행할 수 있습니다.

### 단계 분할 {#split-phase}

특정 실행에서 시작하는 새 단계를 추가하려면 다음을 선택합니다. **[!UICONTROL 새 단계로 분할 옵션]** 추가 작업 아이콘에서 참조할 수 있습니다.

![](assets/ip-warmup-plan-run-split-run.png)

현재 단계의 나머지 실행에 대해 새 단계가 생성됩니다.

예를 들어, 실행 #4에 대해 이 옵션을 선택하면 #8에 #4 실행 이 현재 단계 바로 뒤에 새 단계로 이동됩니다.

다음 단계 [위](#define-phases) 새 단계를 정의합니다.

* 다음을 사용할 수 있습니다. **[!UICONTROL 캠페인 바꾸기]** 새로운 단계에 대한 옵션입니다.

* 이전 캠페인이나 성과가 좋지 않은 도메인을 제외할 수도 있습니다. 에서 방법 알아보기 [이 섹션](#define-phases).

<!--
You don't have to decide the campaign upfront. You can do a split later. It's a work in progress plan: you activate one run at a time with a campaign and you always have the flexibility to modify it while working on it.

But need to explain in which case you want to modify campaigns, provide examples
-->

### IP 준비 계획 다시 업로드 {#re-upload-plan}

IP 준비 계획이 예상대로 수행되지 않는 경우(예: 일부 ISP에서 메시지를 스팸으로 표시하는 경우) 전달성 전문가에게 다른 IP 준비 계획 파일을 설정하고 해당 버튼을 사용하여 다시 업로드하도록 요청할 수 있습니다.

![](assets/ip-warmup-re-upload-plan.png)

이전에 실행된 모든 실행은 읽기 전용입니다. 새 계획은 첫 번째 계획 아래에 표시됩니다.

다음 단계 [위](#define-phases) 을 눌러 새 계획에서 단계를 정의합니다.

>[!NOTE]
>
>IP 준비 계획 세부 사항은 새로 업로드한 파일에 따라 변경됩니다. 이전에 실행된 실행(실행 수에 상관없이) [상태](#monitor-plan))은 영향을 받지 않습니다.

예를 들어 보겠습니다.

* 초기 IP 웜업 계획으로 2단계는 9번의 실행을 수행했습니다.

* 4개의 실행이 실행되었습니다(실패, 완료 또는 취소의 경우 상관 없음).<!--as long as a run has been attempted, it is an executed run-->).

* 새 계획을 다시 업로드하면 처음 실행된 4번의 실행이 있는 단계 2가 읽기 전용 모드로 전환됩니다.

* 나머지 5개 실행(초안 상태)은 새로 업로드한 계획에 따라 표시되는 새 단계(3단계)로 이동합니다.

### 계획을 완료됨으로 표시 {#mark-as-completed}

플랜이 제대로 수행되지 않거나 다른 플랜을 만들기 위해 드롭하려는 경우 완료된 플랜으로 표시할 수 있습니다.

이렇게 하려면 **[!UICONTROL 자세히]** IP 웜업 계획의 오른쪽 상단에 있는 단추이며 **[!UICONTROL 완료로 표시]**.

![](assets/ip-warmup-plan-mark-completed.png)

이 옵션은 플랜의 모든 실행이 포함된 경우에만 사용할 수 있습니다. **[!UICONTROL 완료됨]** 또는 **[!UICONTROL 초안]** 상태. 실행 시 **[!UICONTROL 라이브]**&#x200B;을 지정하면 옵션이 회색으로 표시됩니다.

다양한 실행 상태가 다음에 나열됩니다. [이 섹션](#monitor-plan).

