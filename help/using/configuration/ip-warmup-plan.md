---
solution: Journey Optimizer
product: journey optimizer
title: IP 준비 계획 만들기
description: IP 준비 계획을 만드는 방법을 알아봅니다.
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP, 풀, 그룹, 하위 도메인, 전달성
hide: true
hidefromtoc: true
source-git-commit: 1ec2c406e777e08de97c3ad53cee5986afeb3c44
workflow-type: tm+mt
source-wordcount: '798'
ht-degree: 5%

---

# IP 준비 계획 만들기 {#ip-warmup}

>[!BEGINSHADEBOX]

이 설명서의 내용:

* [IP 준비 시작](ip-warmup-gs.md)
* [IP 준비 캠페인 만들기](ip-warmup-campaign.md)
* **[IP 준비 계획 만들기](ip-warmup-plan.md)**
* [IP 준비 계획 실행](ip-warmup-running.md)

>[!ENDSHADEBOX]

한 개 이상 만든 경우 [IP 준비 캠페인](ip-warmup-campaign.md) 전용 서피스와 해당 옵션이 활성화되면 IP 준비 계획 작성을 시작할 수 있습니다.

## IP 웜업 템플릿 입력 {#upload-plan}

Journey Optimizer 인터페이스에서 IP 준비 계획을 만들려면 먼저 계획을 채울 모든 데이터로 Excel 형식의 템플릿을 채워야 합니다.

>[!CAUTION]
>
>게재 컨설턴트와 협력하여 IP 준비 계획 파일이 올바르게 설정되었는지 확인합니다.

다음은 IP 웜업 플랜이 포함된 파일의 예입니다.

![](assets/ip-warmup-sample-file.png)

### IP 준비 계획 탭

IP 웜업은 합법적인 발신자로서의 평판을 확립하기 위해 IP 및 도메인에서 주요 인터넷 서비스 공급자(ISP)로 나가는 이메일 양을 점차적으로 늘리는 작업입니다.

이 활동은 산업 도메인, 사용 사례, 지역, ISP 및 다양한 기타 요소를 기반으로 잘 계획된 계획을 준비하는 전달성 컨설턴트나 전문가의 도움을 받아 주기적으로 수행됩니다.

* 이 예에서는 17일 이상에 걸쳐 계획을 작성하여 대상 볼륨 xxx 프로필에 도달합니다.

* 이 계획은 6단계를 거쳐 실행됩니다.

* 전달하려는 도메인에 대해 원하는 만큼 열을 가질 수 있습니다. 이 예제에서는 플랜을 Gmail, Adobe, Yahoo 및 Others와 같은 플랜에 사용할 도메인 그룹에 해당하는 4개의 열로 나눕니다.

첫 번째 단계에서 더 많은 실행을 수행하고, 실행 수를 줄이면서 타겟팅된 주소의 수를 점진적으로 늘리는 것이 좋습니다.

기본 제공 도메인 목록은 다음과 같습니다.

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

### 사용자 정의 도메인 그룹 탭

사용자 정의 도메인 그룹으로 열을 더 추가할 수도 있습니다.

사용 **[!UICONTROL 사용자 정의 도메인 그룹]** 새 도메인을 정의할 수 있는 탭입니다. 각 도메인에 대해 포함되는 모든 하위 도메인을 추가할 수 있습니다.<!--TBC-->

## IP 준비 계획 액세스 및 관리 {#manage-ip-warmup-plans}

1. 액세스 **[!UICONTROL 관리]** > **[!UICONTROL 채널]** > **[!UICONTROL IP 준비 계획]** 메뉴 아래의 제품에서 사용할 수 있습니다. 지금까지 만든 모든 IP 준비 계획이 표시됩니다.

   ![](assets/ip-warmup-filter-list.png)

1. 상태를 필터링할 수 있습니다. 다양한 상태는 다음과 같습니다.

   * **시작되지 않음**: 아직 활성화된 실행이 없습니다. [자세히 알아보기](ip-warmup-running.md#define-runs)
   * **진행 중 / 라이브**: 플랜은 첫 번째 단계의 첫 번째 실행이 성공적으로 활성화되는 즉시 이 상태를 사용합니다. [자세히 알아보기](ip-warmup-running.md#define-runs)
   * **완료됨**: 플랜이 완료된 것으로 표시되었습니다. 이 옵션은 플랜의 모든 실행이 포함된 경우에만 사용할 수 있습니다. **[!UICONTROL 성공]** 또는 **[!UICONTROL 초안]** 상태(실행할 수 없음) **[!UICONTROL 라이브]**). [자세히 알아보기](ip-warmup-running.md#define-runs#mark-as-completed)
   * **일시 중지됨**<!--: to check (user action)-->

1. IP 준비 계획을 삭제하려면 **[!UICONTROL 삭제]** 아이콘을 클릭하여 목록 항목 옆에 있는 삭제를 확인합니다.

   ![](assets/ip-warmup-delete-plan.png)

   >[!CAUTION]
   >
   >선택한 IP 준비 계획이 영구적으로 삭제됩니다.

## IP 준비 계획 만들기 {#create-ip-warmup-plan}

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

하나 이상의 라이브 캠페인이 **[!UICONTROL IP 준비 계획 활성화]** 활성화된 옵션이 활성화되면 IP 준비 계획과 연결할 수 있습니다.

>[!CAUTION]
>
>IP 준비 계획을 만들고, 편집하고, 삭제하려면 **[!UICONTROL 전달성 컨설턴트]** 권한. <!--Learn more on managing [!DNL Journey Optimizer] users' access rights in [this section](../administration/permissions-overview.md).-->
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

## IP 준비 계획 다시 업로드 {#re-upload-plan}

해당 버튼을 사용하여 다른 IP 웜업 계획을 다시 업로드할 수 있습니다.

![](assets/ip-warmup-re-upload-plan.png)

>[!NOTE]
>
>IP 준비 계획 세부 사항은 새로 업로드한 파일에 따라 변경됩니다. 전체 실행 및 활성화된 실행은 영향을 받지 않습니다.