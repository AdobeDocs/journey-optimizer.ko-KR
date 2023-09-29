---
title: DM 구성
description: Journey Optimizer에서 DM 채널을 구성하는 방법 알아보기
feature: Overview
topic: Content Management
role: User
level: Beginner
keyword: direct, mail, configuration, direct-mail, provider
exl-id: ae5cc885-ade1-4683-b97e-eda1f2142041
source-git-commit: 280e311ca4515d2147f451af0fffbe6d5fc8029c
workflow-type: tm+mt
source-wordcount: '914'
ht-degree: 31%

---

# DM 구성 {#direct-mail-configuration}

[!DNL Journey Optimizer] dm 공급자가 고객에게 메일을 보내는 데 필요한 파일을 개인화하고 생성할 수 있습니다.

날짜 [dm 메시지 만들기](../direct-mail/create-direct-mail.md), 선택한 연락처 정보(예: 우편 주소)를 포함하는 타겟팅된 대상 데이터를 정의합니다. 그러면 이 데이터가 포함된 파일이 자동으로 생성되고 서버에 내보내져 DM 공급자가 해당 데이터를 검색하고 실제 전송을 처리할 수 있습니다.

이 파일을 생성하려면 먼저 다음을 생성해야 합니다.

1. A [파일 라우팅 구성](#file-routing-configuration) 파일을 내보낼 서버를 지정하고 필요한 경우 파일을 암호화합니다.

1. A [DM 표면](#direct-mail-surface) 그러면 파일 라우팅 구성을 참조합니다.

>[!CAUTION]
>
>파일 라우팅 옵션을 구성하지 않은 경우 DM 표면을 만들 수 없습니다.

## 파일 라우팅 구성 {#file-routing-configuration}

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_details"
>title="파일 라우팅 구성 정의"
>abstract="DM 메시지를 만든 후에는 타겟팅된 대상자 데이터가 포함된 파일을 생성하여 서버로 내보냅니다. DM 공급자가 DM 게재를 위해 해당 파일에 액세스하여 사용할 수 있도록 서버 세부 사항을 지정해야 합니다."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/direct-mail/create-direct-mail.html" text="DM 메시지 만들기"

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_details_header"
>title="파일 라우팅 구성 정의"
>abstract="DM 공급자가 사용하려는 파일을 내보낼 위치를 정의해야 합니다."

>[!CONTEXTUALHELP]
>id="ajo_dm_select_file_routing"
>title="파일 라우팅 구성"
>abstract="원하는 파일 라우팅 구성을 선택하여 DM 공급자가 사용하려는 파일을 내보낼 위치를 정의합니다."

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_type"
>title="파일의 서버 유형을 선택합니다."
>abstract="DM 파일 내보내기에 사용할 서버 유형을 선택합니다. 현재 Journey Optimizer는 Amazon S3 및 SFTP만 지원합니다."

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_aws_region"
>title="AWS 지역 선택"
>abstract="DM 파일을 내보내려는 AWS 서버가 있는 지역을 선택합니다. 일반적으로 DM 공급자 위치와 가장 가까운 지역을 선택하는 것이 좋습니다."

DM 메시지를 게재하려면, [!DNL Journey Optimizer] 에서는 타깃팅된 대상 데이터가 포함된 파일을 생성하여 서버로 내보냅니다.

DM 공급자가 메일을 전달하기 위해 해당 파일에 액세스하고 사용할 수 있도록 서버 세부 정보를 지정해야 합니다.

파일 라우팅을 구성하려면 아래 단계를 따르십시오.

1. 액세스 **[!UICONTROL 관리]** > **[!UICONTROL 채널]** > **[!UICONTROL 파일 라우팅 구성]** > **[!UICONTROL 파일 라우팅]** 메뉴를 선택한 다음 **[!UICONTROL 라우팅 구성 만들기]**.

   ![](assets/file-routing-config-button.png){width="800" align="center"}

1. 구성의 이름을 설정합니다.

1. 다음 항목 선택 **[!UICONTROL 서버 유형]** dm 파일을 내보내는 데 사용할 수 있습니다.

   ![](assets/file-routing-config-type.png){width="800" align="center"}

   >[!NOTE]
   >
   >현재 Amazon S3, SFTP 및 Azure는에서 지원됩니다. [!DNL Journey Optimizer].

1. 서버 주소, 액세스 키 등과 같은 서버의 세부 정보 및 자격 증명을 입력합니다.

   ![](assets/file-routing-config-sftp-details.png)

1. 선택한 경우 **[!UICONTROL Amazon]**, 을(를) 선택합니다. **[!UICONTROL AWS 지역]** 서버 인프라가 배치될 위치입니다.

   ![](assets/file-routing-config-aws-region.png){width="800" align="center"}

   >[!NOTE]
   >
   >AWS 지역은 AWS이 클라우드 인프라를 호스팅하는 데 사용하는 지리적 영역입니다. 일반적으로 DM 공급자 위치와 가장 가까운 지역을 선택하는 것이 좋습니다.

1. 파일을 암호화하려면 암호화 키를 **[!UICONTROL PGP/GPG 암호화 키]** 필드.

1. **[!UICONTROL 제출]**&#x200B;을 선택합니다. 파일 라우팅 구성은 **[!UICONTROL 활성]** 상태. 이제 사용할 준비가 되었습니다. [DM 표면](#direct-mail-surface).

   >[!NOTE]
   >
   >다음을 선택할 수도 있습니다. **[!UICONTROL 초안으로 저장]** 파일 경로설정 구성을 생성하려면 해당 구성을 생성할 때까지 서피스에서 선택할 수 없습니다 **[!UICONTROL 활성]**.

## DM 표면 만들기 {#direct-mail-surface}

>[!CONTEXTUALHELP]
>id="ajo_dm_surface_settings"
>title="DM 설정 정의"
>abstract="DM 표면에는 타겟팅된 대상자 데이터가 있고 메일 공급자가 사용할 수 있는 파일 형식에 대한 설정이 포함됩니다. 파일 라우팅 구성을 선택하여 파일을 내보낼 위치도 정의해야 합니다."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/direct-mail/direct-mail-configuration.html?lang=ko-KR#file-routing-configuration" text="파일 라우팅 구성"

<!--
>[!CONTEXTUALHELP]
>id="ajo_dm_surface_sort"
>title="Define the sort order"
>abstract="If you select this option, the sort will be by profile ID, ascending or descending. If you unselect it, the sorting configuration defined when creating the direct mail message within a journey or a campaign."-->

>[!CONTEXTUALHELP]
>id="ajo_dm_surface_split"
>title="파일 분할 임계값 정의"
>abstract="대상자 데이터가 포함된 각 파일의 최대 레코드 수를 설정해야 합니다. 1과 200,000 사이에서 레코드 수를 선택할 수 있습니다. 지정된 임계값에 도달하면 나머지 레코드에 대해 다른 파일이 만들어집니다."

DM을 게재하려면 [!DNL Journey Optimizer], 메일 공급자가 사용할 파일 형식 설정을 정의할 채널 표면을 만들어야 합니다.

DM 표면에는 DM 파일을 내보낼 서버를 정의하는 파일 라우팅 구성도 포함되어야 합니다.

1. 채널 표면을 만듭니다. [자세히 알아보기](../configuration/channel-surfaces.md)

1. 다음 항목 선택 **[!UICONTROL 다이렉트 메일]** 채널.

   ![](assets/surface-direct-mail-channel.png){width="800" align="center"}

1. 채널 표면 구성의 전용 섹션에서 DM 설정을 정의합니다.

   ![](assets/surface-direct-mail-settings.png){width="800" align="center"}

   <!--![](assets/surface-direct-mail-settings-with-insertion.png)-->

1. 파일 형식 선택: **[!UICONTROL CSV]** 또는 **[!UICONTROL 텍스트로 구분됨]**.

1. 다음을 선택하는 경우 **[!UICONTROL 텍스트로 구분됨]**&#x200B;을(를) 통해 원하는 열 구분 기호(표, 세미콜론, 파이프 또는 앰퍼샌드)를 정의합니다.

   ![](assets/surface-direct-mail-column-separator.png)

1. 다음 항목 선택 **[!UICONTROL 파일 라우팅 구성]** 만든 항목 중에서 선택합니다. DM 공급자가 사용할 파일을 내보내는 위치를 정의합니다.

   >[!CAUTION]
   >
   >파일 라우팅 옵션을 구성하지 않은 경우 DM 표면을 만들 수 없습니다. [자세히 알아보기](#file-routing-configuration)

   ![](assets/surface-direct-mail-file-routing.png){width="800" align="center"}

   <!--![](assets/surface-direct-mail-file-routing-with-insertion.png)-->

1. DM 표면을 제출합니다.

이제 다음을 수행할 수 있습니다. [dm 메시지 만들기](../direct-mail/create-direct-mail.md) 캠페인 내부. 캠페인이 시작되면 타겟팅된 대상자 데이터가 포함된 파일은 정의한 서버로 자동으로 내보내집니다. 그러면 DM 공급자는 해당 파일을 검색하고 DM 게재를 진행할 수 있습니다.

>[!NOTE]
>
>중복 행은 자동으로 제거됩니다.
>
>프로필 데이터가 포함된 각 파일의 최대 레코드 수(즉, 행)가 너무 많으면 나머지 레코드에 대해 다른 파일이 자동으로 만들어집니다.

<!--
    In the **[!UICONTROL Insertion]** section, you can choose to automatically remove duplicate rows.

    Define the maximum number of records (i.e. rows) for each file containing profile data. After the specified threshold is reached, another file will be created for the remaining records.

    ![](assets/surface-direct-mail-split.png)

    For example, if there are 100,000 records in the file and the threshold limit is set to 60,000, the records will be split into two files. The first file will contain 60,000 rows, and the second file will contain the remaining 40,000 rows.

    >[!NOTE]
    >
    >NOTE You can set any number between 1 and 200,000 records, meaning each file must contain at least 1 row and no more than 200,000 rows.

-->