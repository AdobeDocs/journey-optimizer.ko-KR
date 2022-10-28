---
title: DM 구성
description: Journey Optimizer에서 DM 채널을 구성하는 방법 알아보기
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: bca233ab888e2ca33b866bc3def31653f2d55ea9
workflow-type: tm+mt
source-wordcount: '946'
ht-degree: 0%

---

# DM 구성 {#direct-mail-configuration}

[!DNL Journey Optimizer] 을(를) 통해 다이렉트 메일 공급자가 고객에게 메일을 보내는 데 필요한 파일을 개인화하고 생성할 수 있습니다.

When [dm 메시지 만들기](../messages/create-direct-mail.md)을(를) 선택한 연락처 정보(예를 들어 우편 주소)를 포함하여 타겟팅된 대상 데이터를 정의합니다. 그러면 이 데이터가 포함된 파일이 자동으로 생성되어 서버로 내보내집니다. 여기서 DM 공급자가 데이터를 검색하고 실제 전송을 처리할 수 있습니다.

이 파일을 생성하려면 먼저 다음을 만들어야 합니다.

1. A [파일 라우팅 구성](#file-routing-configuration) 파일을 내보낼 서버를 지정합니다.

1. A [DM 표면](#direct-mail-surface) 파일 라우팅 구성을 참조합니다.

>[!CAUTION]
>
>파일 라우팅 옵션을 구성하지 않은 경우 DM 서피스를 생성할 수 없습니다.

## 파일 라우팅 구성 {#file-routing-configuration}

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_details"
>title="파일 라우팅 구성 정의"
>abstract="DM 메시지를 만들면 타깃팅된 대상 데이터가 포함된 파일이 생성되고 서버로 내보내집니다. DM 공급자가 해당 파일에 액세스하여 DM 전달에 사용할 수 있도록 서버 세부 사항을 지정해야 합니다."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/messages/create-direct-mail.html" text="DM 메시지 만들기"

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_details_header"
>title="파일 라우팅 구성 정의"
>abstract="DM 공급자가 사용할 파일을 내보낼 위치를 정의해야 합니다."

>[!CONTEXTUALHELP]
>id="ajo_dm_select_file_routing"
>title="파일 라우팅 구성"
>abstract="DM 공급자가 사용할 파일을 내보낼 위치를 정의하는 원하는 파일 라우팅 구성을 선택합니다."

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_type"
>title="파일의 서버 유형을 선택합니다"
>abstract="DM 파일을 내보내는 데 사용할 서버 유형을 선택합니다. 현재 Journey Optimizer에서는 Amazon S3 및 SFTP만 지원됩니다."

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_aws_region"
>title="AWS 지역 선택"
>abstract="DM 파일을 내보낼 AWS 서버의 지역 영역을 선택합니다. 일반적으로 DM 공급자 위치에 가장 가까운 지역을 선택하는 것이 좋습니다."

DM 메시지를 배달하려면 [!DNL Journey Optimizer] 타겟팅된 대상 데이터가 포함된 파일을 생성하여 서버로 내보냅니다.

DM 공급자가 해당 파일에 액세스하여 메일 배달에 사용할 수 있도록 서버 세부 정보를 지정해야 합니다.

파일 라우팅을 구성하려면 아래 단계를 따르십시오.

1. 액세스 권한 **[!UICONTROL 관리]** > **[!UICONTROL 채널]** > **[!UICONTROL 파일 라우팅 구성]** > **[!UICONTROL 파일 라우팅]** 메뉴를 클릭한 다음 **[!UICONTROL 라우팅 구성 만들기]**.

   ![](assets/file-routing-config-button.png)

1. 구성 이름을 설정합니다.

1. 을(를) 선택합니다 **[!UICONTROL 서버 유형]** DM 파일을 내보내는 데 사용할 DM입니다.

   ![](assets/file-routing-config-type.png)

   >[!NOTE]
   >
   >현재 Amazon S3 및 SFTP만 [!DNL Journey Optimizer].

1. 서버 주소, 액세스 키 등과 같은 서버의 세부 정보 및 자격 증명을 입력합니다.

   ![](assets/file-routing-config-sftp-details.png)

1. 선택한 경우 **[!UICONTROL Amazon S3]**&#x200B;을(를) 선택하고 을(를) 선택합니다. **[!UICONTROL AWS 지역]** 서버 인프라가 위치할 위치입니다.

   ![](assets/file-routing-config-aws-region.png)

   >[!NOTE]
   >
   >AWS 지역은 AWS이 클라우드 인프라를 호스팅하기 위해 사용하는 지리적 영역입니다. 일반적으로 DM 공급자의 위치에 가장 가까운 지역을 선택하는 것이 좋습니다.

1. 선택 **[!UICONTROL 제출]**. 파일 라우팅 구성은 **[!UICONTROL 활성]** 상태. 이제 다음 위치에서 사용할 준비가 되었습니다. [DM 표면](#direct-mail-surface).

   >[!NOTE]
   >
   >선택할 수도 있습니다 **[!UICONTROL 초안으로 저장]** 파일 경로설정 구성을 생성하기 위해 파일 경로설정 구성이 생성되기 전까지 서피스에서 선택할 수 없습니다 **[!UICONTROL 활성]**.

## DM 표면 만들기 {#direct-mail-surface}

>[!CONTEXTUALHELP]
>id="ajo_dm_surface_settings"
>title="DM 설정 정의"
>abstract="DM 표면에는 타겟팅된 대상 데이터가 포함되어 있으며 메일 공급자가 사용할 파일의 형식에 대한 설정이 포함되어 있습니다. 파일 라우팅 구성을 선택하여 파일을 내보낼 위치도 정의해야 합니다."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/configuration-message/direct-mail-configuration.html#file-routing-configuration" text="파일 라우팅 구성"

<!--
>[!CONTEXTUALHELP]
>id="ajo_dm_surface_sort"
>title="Define the sort order"
>abstract="If you select this option, the sort will be by profile ID, ascending or descending. If you unselect it, the sorting configuration defined when creating the direct mail message within a journey or a campaign."-->

>[!CONTEXTUALHELP]
>id="ajo_dm_surface_split"
>title="파일 분할 임계값 정의"
>abstract="대상 데이터가 포함된 각 파일에 대한 최대 레코드 수를 설정해야 합니다. 레코드 1에서 200,000개 사이의 숫자를 선택할 수 있습니다. 지정한 임계값에 도달하면 나머지 레코드에 대한 다른 파일이 만들어집니다."

DM을 [!DNL Journey Optimizer]을(를) 만들려면 메일 공급자가 사용할 파일의 형식에 대한 설정을 정의해야 합니다.

DM 서피스에는 DM 파일을 내보낼 서버를 정의하는 파일 라우팅 구성도 포함되어야 합니다.

1. 채널 서피스를 생성합니다. [자세히 보기](channel-surfaces.md)

1. 을(를) 선택합니다 **[!UICONTROL DM]** 채널.

   ![](assets/surface-direct-mail-channel.png)

1. 채널 서피스 구성의 전용 섹션에서 DM 설정을 정의합니다.

   ![](assets/surface-direct-mail-settings.png)

1. 파일 형식을 선택합니다. **[!UICONTROL CSV]** 또는 **[!UICONTROL 텍스트 구분]**.

1. 에서 **[!UICONTROL 삽입]** 섹션에서 중복 행을 자동으로 제거하도록 선택할 수 있습니다.

1. 프로필 데이터가 포함된 각 파일에 대한 최대 레코드 수(예: 행)를 정의합니다. 지정한 임계값에 도달하면 나머지 레코드에 대한 다른 파일이 만들어집니다.

   ![](assets/surface-direct-mail-split.png)

   예를 들어 파일에 100,000개의 레코드가 있고 임계값 제한이 60,000으로 설정되어 있으면 레코드가 두 개의 파일로 분할됩니다. 첫 번째 파일에는 60,000개의 행이 포함되며 두 번째 파일에는 나머지 40,000개의 행이 포함됩니다.

   >[!NOTE]
   >
   >1과 20만 레코드 사이의 숫자를 설정할 수 있습니다. 즉, 각 파일에는 1개 이상의 행과 20만 개의 행을 포함할 수 없습니다.

1. 마지막으로 **[!UICONTROL 파일 라우팅 구성]** 만든 것들 중에서. DM 공급자가 사용할 파일을 내보낼 위치를 정의합니다.

   >[!CAUTION]
   >
   >파일 라우팅 옵션을 구성하지 않은 경우 DM 서피스를 생성할 수 없습니다. [자세히 보기](#file-routing-configuration)

   ![](assets/surface-direct-mail-file-routing.png)

1. DM 표면을 제출합니다.

이제 다음을 수행할 수 있습니다 [dm 메시지 만들기](../messages/create-direct-mail.md) 캠페인 내부. 캠페인이 시작되면 타겟팅된 대상 데이터가 포함된 파일을 정의한 서버로 자동으로 내보냅니다. 그러면 DM 공급자가 해당 파일을 검색하고 DM 게재를 계속 진행할 수 있습니다.