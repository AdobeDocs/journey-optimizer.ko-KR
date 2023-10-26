---
solution: Journey Optimizer
product: journey optimizer
title: IP 준비 계획 만들기
description: Journey Optimizer에서 IP 준비 계획을 만드는 방법을 알아봅니다.
feature: IP Warmup Plans
topic: Administration
role: Admin
level: Experienced
keywords: IP, 그룹, 하위 도메인, 전달성
hide: true
hidefromtoc: true
exl-id: c2434086-2ed4-4cd0-aecd-2eea8f0a55f6
source-git-commit: eb4a4929de17f0b57216f69e00da6314f7b59b07
workflow-type: tm+mt
source-wordcount: '1111'
ht-degree: 11%

---

# IP 준비 계획 만들기 {#ip-warmup}

>[!BEGINSHADEBOX]

이 설명서의 내용:

* [IP 준비 시작](ip-warmup-gs.md)
* [IP 워밍업 캠페인 만들기](ip-warmup-campaign.md)
* **[IP 준비 계획 만들기](ip-warmup-plan.md)**
* [IP 준비 계획 실행](ip-warmup-execution.md)

>[!ENDSHADEBOX]

한 개 이상 만든 경우 [IP 준비 캠페인](ip-warmup-campaign.md) 전용 서피스와 해당 옵션이 활성화되면 IP 준비 계획 작성을 시작할 수 있습니다.

>[!CAUTION]
>
>IP 준비 계획에 액세스하고, 만들고, 편집하고, 삭제하려면 다음을 수행해야 합니다. **[!UICONTROL 전달성 컨설턴트]** 권한. <!--Learn more on managing [!DNL Journey Optimizer] users' access rights in [this section](../administration/permissions-overview.md).-->

## IP 준비 계획 파일 준비 {#prepare-file}

IP 웜업은 합법적인 발신자로서의 평판을 확립하기 위해 IP 및 도메인에서 주요 인터넷 서비스 공급자(ISP)로 나가는 이메일 양을 점차적으로 늘리는 작업입니다.

이 활동은 업계 도메인, 사용 사례, 지역, ISP 및 다양한 기타 요소를 기반으로 잘 설계된 계획을 준비하는 데 도움을 주는 전달성 전문가의 도움을 받아 정기적으로 수행됩니다.

<!--When working with the [!DNL Journey Optimizer] IP warmup feature, this plan takes the form of an Excel file that must contain a number of predefined columns.-->

에서 IP 준비 계획을 만들기 전에 [!DNL Journey Optimizer] 인터페이스에서는 계획을 제공할 모든 데이터를 Excel 템플릿에 입력해야 합니다.

>[!CAUTION]
>
>게재 컨설턴트와 협력하여 IP 준비 계획 파일이 올바르게 설정되었는지 확인합니다.
>
>템플릿에 제공된 형식을 사용해야 합니다.

다음은 IP 웜업 플랜이 포함된 파일의 예입니다.

![](assets/ip-warmup-sample-file.png)

>[!NOTE]
>
>지금은 을(를) 떠나십시오. **속성** 및 **값** 만지지 않은 세포.

### IP 준비 계획 탭 {#ip-warmup-plan-tab}

* 이 예에서 계획은 17일 이상에 걸쳐 준비되었습니다(&quot;라고 함)**실행**&quot;) 백만 개 이상의 프로필이 타겟인 볼륨에 도달하기 위해

* 이 계획은 6시까지 실행됩니다. **단계**, 각 행에 하나 이상의 실행이 포함됩니다.

* 전달하려는 도메인에 대해 원하는 만큼 열을 가질 수 있습니다. 이 예에서 플랜은 6개의 열로 나뉩니다.

   * 이 중 4개는 **기본 도메인 그룹** 플랜에 사용할 수 있습니다(Gmail, Microsoft, Yahoo 및 Orange).
   * 하나는 사용자 정의 도메인 그룹에 해당합니다(다음을 사용하여 추가해야 함). [사용자 정의 도메인 그룹](#custom-domain-group-tab) 탭).
   * 여섯 번째 열, **기타**&#x200B;에는 플랜에서 명시적으로 다루지 않는 다른 도메인의 나머지 주소가 모두 포함되어 있습니다. 이 열은 선택 사항입니다. 생략하면 이메일이 지정된 도메인으로만 이동합니다.
* 다음 **참여 기간(일)** 열에는 입력한 지난 기간 동안 브랜드와 관련된 프로필만 타겟팅됨을 보여 줍니다.

이 아이디어는 각 실행에서 타깃팅된 주소의 수를 점진적으로 늘리면서 각 단계에 대한 실행 수를 줄이는 것입니다.

플랜에 추가할 수 있는 기본 도메인 그룹은 다음과 같습니다.

* Gmail
* Adobe
* WP
* 컴캐스트
* Yahoo
* 빅폰드
* 주황
* 소프트뱅크
* 도코모
* 유나이티드 인터넷
* Microsoft
* KDDI
* 이탈리아 온라인
* 라 포스트
* Apple

<!--
+++ Gmail
gmail.com;gmail.fr;gmail.de;gmail.co.uk;gmail.it
+++

+++ Adobe
adobe.com;adobe.fr;adobe.es
+++

+++WP
+++

+++Comcast
+++

+++Yahoo
+++

+++Bigpond
+++

+++Orange
+++

+++Softbank
+++

+++Docomo
+++

+++United Internet
+++

+++Microsoft
+++

+++KDDI
+++

+++Italia Online
+++

+++La Poste
+++
-->

### 사용자 정의 도메인 그룹 탭 {#custom-domain-group-tab}

사용자 정의 도메인 그룹을 포함하여 플랜에 열을 더 추가할 수도 있습니다.

사용 **[!UICONTROL 사용자 정의 도메인 그룹]** 탭으로 이동하여 새 도메인 그룹을 정의합니다. 각 도메인에 대해 포함되는 모든 하위 도메인을 추가할 수 있습니다.<!--TBC-->

예를 들어 사용자 정의 도메인 Luma를 추가하는 경우 luma.com, luma.co.uk, luma.it, luma.fr, luma.de 등의 하위 도메인을 포함하려고 합니다.

![](assets/ip-warmup-sample-file-custom.png)

### 예 {#example}

두 개의 사용자 정의 도메인 그룹을 원한다고 가정해 보겠습니다.

* Hotmail 도메인에만 사용할 수 있습니다.
* 도메인 그룹 Microsoft의 다른 모든 도메인에 대한 것입니다(따라서 모든 Hotmail 도메인 제외).

다른 모든 도메인은 **[!UICONTROL 기타]** 열.

1. 다음에서 **[!UICONTROL 사용자 정의 도메인 그룹]** 탭, 만들기 **핫메일** 도메인 그룹.

1. 동일한 행에 모든 Hotmail 도메인을 추가합니다.

   다음을 수행할 수 있습니다. [복사하여 붙여넣기](#copy-paste) 에 나열된 모든 Hotmail 도메인 [IP 준비 계획 탭](#ip-warmup-plan-tab) 섹션.

1. 다른 행을 추가합니다.

1. 만들기 **MICROSOFT X** 도메인 그룹.

1. Hotmail이 아닌 모든 Microsoft 도메인을 같은 행에 추가합니다. 마찬가지로 위의 목록에서 복사하여 붙여넣을 수 있습니다. [자세히 알아보기](#copy-paste)

1. 로 돌아가기 **[!UICONTROL IP 준비 계획]** 탭.

1. 세 개의 열 만들기: **핫메일**, 1개 **MICROSOFT X** 다음에 대한 1개 **기타**.

1. 필요에 따라 열을 입력합니다.

>[!NOTE]
>
>IP 준비 계획이 (으)로 업로드되면 [!DNL Journey Optimizer], Microsoft 도메인 그룹을 제외할 필요가 없습니다.

<!--Only the domain groups listed in the **[!UICONTROL IP Warmup Plan]** tab will be taken into account.-->

### 기본 도메인 복사-붙여넣기 {#copy-paste}

예를 들어 모든 Hotmail 도메인을 포함하는 사용자 정의 도메인 그룹을 만들려면 제공된 기본 목록에서 도메인을 복사하여 붙여 넣을 수 있습니다 [위](#ip-warmup-plan-tab).

그런 다음 Excel 변환 도구를 사용하여 텍스트를 열로 변환합니다.

1. 선택 **[!UICONTROL 데이터]** > **[!UICONTROL 텍스트를 열로 변환...]**, 선택 **[!UICONTROL 구분됨]** 및 선택 **[!UICONTROL 다음]**.

1. 선택 **[!UICONTROL 세미콜론]**, 클릭 **[!UICONTROL 다음]** 및 **[!UICONTROL 완료]**.

이제 각 도메인이 동일한 행의 다른 열에 표시됩니다.

## IP 준비 계획 액세스 및 관리 {#manage-ip-warmup-plans}

1. 액세스 **[!UICONTROL 관리]** > **[!UICONTROL 채널]** > **[!UICONTROL IP 준비 계획]** 메뉴 아래의 제품에서 사용할 수 있습니다. 지금까지 만든 모든 IP 준비 계획이 표시됩니다.

   ![](assets/ip-warmup-filter-list.png)

1. 상태를 필터링할 수 있습니다. 다양한 상태는 다음과 같습니다.

   * **시작되지 않음**: 아직 활성화된 실행이 없습니다. [자세히 알아보기](ip-warmup-execution.md#define-runs)
   * **라이브**: 플랜은 첫 번째 단계의 첫 번째 실행이 성공적으로 활성화되는 즉시 이 상태로 변경됩니다. [자세히 알아보기](ip-warmup-execution.md#define-runs)
   * **완료됨**: 플랜이 완료된 것으로 표시되었습니다. <!--This option is only available if all the runs in the plan are in **[!UICONTROL Completed]** or **[!UICONTROL Draft]** status (no run can be **[!UICONTROL Live]**).--> [자세히 알아보기](ip-warmup-execution.md#mark-as-completed)
     <!--* **Paused**: to check (user action)-->

1. IP 준비 계획을 삭제하려면 **[!UICONTROL 삭제]** 아이콘은 플랜의 이름 옆에 있으며 삭제를 확인합니다.

   >[!NOTE]
   >
   >이 포함된 플랜만 **시작되지 않음** 상태를 삭제할 수 있습니다.

   ![](assets/ip-warmup-delete-plan.png)

   >[!CAUTION]
   >
   >선택한 IP 준비 계획이 영구적으로 삭제됩니다.

## IP 준비 계획 만들기 {#create-ip-warmup-plan}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_upload"
>title="IP 워밍업 플랜 지정"
>abstract="CSV 템플릿을 다운로드하고 IP 워밍업 단계와 타겟 프로필 수에 대한 데이터로 채우세요."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_surface"
>title="마케팅 표면 선택"
>abstract="IP 워밍업 플랜과 연결하려는 캠페인에서 선택한 것과 동일한 표면을 선택해야 합니다."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html" text="채널 표면 설정"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html" text="IP 워밍업 캠페인 만들기"

IP 준비 계획을 만들려면 아래 단계를 수행합니다.

1. 액세스 **[!UICONTROL 관리]** > **[!UICONTROL 채널]** > **[!UICONTROL IP 준비 계획]** 메뉴를 선택한 다음 **[!UICONTROL IP 준비 계획 만들기]**.

   ![](assets/ip-warmup-create-plan.png)

1. IP 준비 계획 세부 사항을 입력합니다. 이름과 설명을 입력합니다.

   ![](assets/ip-warmup-plan-details.png)

1. 다음 항목 선택 [표면](channel-surfaces.md) 몸을 따뜻하게 하고 싶으시군요. 마케팅 표면만 선택할 수 있습니다. [이메일 유형에 대해 자세히 알아보기](../email/email-settings.md#email-type)

   >[!NOTE]
   >
   >IP 준비 계획과 연결할 캠페인은 동일한 표면을 사용해야 합니다. [IP 준비 캠페인을 만드는 방법을 알아봅니다.](ip-warmup-campaign.md)

1. IP 준비 계획이 포함된 Excel 파일을 업로드합니다. [자세히 알아보기](#prepare-file)

   <!--
    You can also download the Excel template from the [!DNL Journey Optimizer] user interface and upload it after filling it with the IP warmup details.-->

   ![](assets/ip-warmup-upload-success.png)

   >[!NOTE]
   >
   >업로드가 실패할 경우 올바른 형식 및 파일 형식(.xls 또는 .xlsx)을 사용하고 있는지 확인하십시오. 제공된 샘플을 Adobe으로 사용하십시오.

1. **[!UICONTROL 만들기]**&#x200B;를 클릭합니다. 업로드한 파일에 정의된 모든 단계, 실행, 열 및 해당 콘텐츠가 [!DNL Journey Optimizer] 인터페이스.

   ![](assets/ip-warmup-plan-uploaded.png)

이제 IP 준비 계획을 실행할 준비가 되었습니다. [자세히 알아보기](ip-warmup-execution.md)
