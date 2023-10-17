---
title: DM 메시지 만들기
description: Journey Optimizer에서 DM 메시지를 만드는 방법을 알아봅니다
feature: Direct Mail
topic: Content Management
role: User
level: Beginner
keywords: DM, 메시지, 캠페인
exl-id: 6b438268-d983-4ab8-9276-c4b7de74e6bd
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: tm+mt
source-wordcount: '720'
ht-degree: 17%

---

# DM 메시지 만들기 {#create-direct}

>[!CONTEXTUALHELP]
>id="ajo_direct_mail"
>title="DM(Direct Mail) 만들기"
>abstract="예약된 캠페인에서 DM 메시지를 만들고, DM 공급자가 고객에게 메일을 전송하는 데 필요한 추출 파일을 디자인합니다."

DM 메시지를 만들려면 예약된 캠페인을 만들고 추출 파일을 구성합니다. DM 공급자가 고객에게 메일을 보낼 때 이 파일이 필요합니다.

>[!IMPORTANT]
>
>DM 메시지를 만들기 전에 다음을 구성했는지 확인하십시오.
>
>1. A [파일 라우팅 구성](../direct-mail/direct-mail-configuration.md#file-routing-configuration) 추출 파일을 업로드하고 저장할 서버를 지정합니다.
>1. A [다이렉트 메일 메시지 표면](../direct-mail/direct-mail-configuration.md#direct-mail-surface) 파일 라우팅 구성을 참조합니다.


## DM 캠페인 만들기{#create-dm-campaign}

DM 캠페인을 만들려면 다음 단계를 수행합니다.

1. 새 예약된 캠페인을 만들고 선택 **[!UICONTROL 다이렉트 메일]** as the action.

1. 다음 항목 선택 **[!UICONTROL 다이렉트 메일 표면]** 을(를) 사용하고 **[!UICONTROL 만들기]**. [DM 표면을 만드는 방법 알아보기](direct-mail-configuration.md#direct-mail-surface).

   ![](assets/direct-mail-campaign.png){width="800" align="center"}

1. 다음에서 **[!UICONTROL 속성]** 섹션, 캠페인의 편집 **[!UICONTROL 제목]** 및 **[!UICONTROL 설명]**.

1. 타겟 대상을 정의하려면 다음을 클릭하십시오. **[!UICONTROL 대상자 선택]** 버튼을 클릭하고 사용 가능한 Adobe Experience Platform 대상 중에서 선택합니다. [자세히 알아보기](../audience/about-audiences.md).

   >[!IMPORTANT]
   >
   >현재 대상자 선택은 300만 프로필로 제한됩니다. 이 제한은 Adobe 담당자에게 요청하면 완화될 수 있습니다.

1. 다음에서 **[!UICONTROL ID 네임스페이스]** 필드에서 선택한 대상 내의 개인을 식별할 적절한 네임스페이스를 선택합니다. [자세히 알아보기](../event/about-creating.md#select-the-namespace).

   ![](assets/direct-mail-campaign-properties.png){width="800" align="center"}

1. 특정 날짜에 대해 캠페인을 예약하거나 정기적으로 반복하도록 설정할 수 있습니다. 구성 방법 알아보기 **[!UICONTROL 예약]** 의 내 캠페인 [이 섹션](../campaigns/create-campaign.md#schedule).

이제 DM 공급자에게 보낼 추출 파일 구성을 시작할 수 있습니다.

## 추출 파일 구성 {#extraction-file}

>[!CONTEXTUALHELP]
>id="ajo_direct_mail_data_fields"
>title="데이터 필드"
>abstract="다이렉트 메일 공급자가 고객에게 메일을 보내는 데 필요한 추출 파일에 표시할 열과 정보를 추가하고 구성합니다. 최대 50개의 열을 추가할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_direct_mail_formatting"
>title="추출 파일 서식"
>abstract="각 필드에 대해 표현식 편집기를 사용하여 표시할 레이블과 정보를 지정합니다. <br/><br/><b>정렬 기준</b> 옵션을 사용하면 선택한 필드를 통해 추출 파일의 열을 정렬할 수 있습니다."

1. 추출 파일에 표시할 열과 정보를 구성합니다.

   1. 다음을 클릭합니다. **[!UICONTROL 추가]** 단추를 클릭하여 새 열을 만듭니다.

   1. 다음 **[!UICONTROL 서식]** 선택한 열을 설정할 수 있는 창이 오른쪽에 표시됩니다. 지정 **[!UICONTROL 레이블]** 열.

   1. 다음에서 **[!UICONTROL 데이터]** 필드에서 다음을 사용하여 표시할 프로필 속성을 선택합니다. [표현식 편집기](../personalization/personalization-build-expressions.md).

   1. 열을 사용하여 추출 파일을 정렬하려면 열을 선택하고 **[!UICONTROL 정렬 기준:]** 옵션을 선택합니다. 다음 **[!UICONTROL 정렬 기준:]** 아이콘은 열의 레이블 옆에 표시됩니다. **[!UICONTROL 데이터 필드]** 섹션.







DM 공급자가 고객에게 메일을 보낼 때 추출 파일이 필요합니다. 추출 파일 구성을 정의하려면 다음 단계를 수행합니다.

1. 캠페인 구성 화면에서 다음을 클릭합니다. **[!UICONTROL 콘텐츠 편집]** 단추를 클릭하여 추출 파일 콘텐츠를 구성합니다.

1. 추출 파일 속성을 조정합니다.

   1. 원하는 을 지정합니다 **[!UICONTROL 파일 이름]** 추출 파일용입니다.

   1. 필요한 경우 **[!UICONTROL 파일 이름 내보내기에 타임스탬프 추가]** 지정된 파일 이름에 자동 타임스탬프를 추가하려면 옵션을 선택합니다.

   1. 추출 파일의 시작 또는 끝 부분에 정보를 추가해야 하는 경우가 있습니다. 이렇게 하려면 **[!UICONTROL 메모]** 필드를 지정하고 메모를 머리글이나 바닥글로 포함할지 지정합니다.

      ![](assets/direct-mail-properties.png){width="800" align="center"}

1. 추출 파일에 표시할 열과 정보를 구성합니다.

   1. 다음을 클릭합니다. **[!UICONTROL 추가]** 단추를 클릭하여 새 열을 만듭니다.

   1. 다음 **[!UICONTROL 서식]** 선택한 열을 설정할 수 있는 창이 오른쪽에 표시됩니다. 지정 **[!UICONTROL 레이블]** 열.

   1. 다음에서 **[!UICONTROL 데이터]** 필드에서 다음을 사용하여 표시할 프로필 속성을 선택합니다. [표현식 편집기](../personalization/personalization-build-expressions.md).

   1. 열을 사용하여 추출 파일을 정렬하려면 열을 선택하고 **[!UICONTROL 정렬 기준:]** 옵션을 선택합니다. 다음 **[!UICONTROL 정렬 기준:]** 아이콘은 열의 레이블 옆에 표시됩니다. **[!UICONTROL 데이터 필드]** 섹션.

      ![](assets/direct-mail-content.png){width="800" align="center"}

   1. 추출 파일에 필요한 수만큼 열을 추가하려면 이 단계를 반복합니다. 최대 50개의 열을 추가할 수 있습니다.

      열의 위치를 변경하려면 열의 원하는 위치로 끌어서 놓습니다. **[!UICONTROL 데이터 필드]** 섹션. 열을 삭제하려면 열을 선택하고 **[!UICONTROL 제거]** 의 단추 **[!UICONTROL 서식]** 창.

이제 DM 메시지를 테스트하여 대상자에게 보낼 수 있습니다. [DM 메시지 테스트 및 보내기 방법 알아보기](test-send-direct-mail.md)
