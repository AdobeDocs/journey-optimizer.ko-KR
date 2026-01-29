---
title: 다이렉트 메일 메시지 만들기
description: Journey Optimizer에서 다이렉트 메일 메시지를 만드는 방법 알아보기
feature: Direct Mail
topic: Content Management
role: User
level: Beginner
keywords: 다이렉트 메일, 메시지, 캠페인
exl-id: 6b438268-d983-4ab8-9276-c4b7de74e6bd
source-git-commit: 916239c98c982acf9c6f999316e46036d36b2098
workflow-type: tm+mt
source-wordcount: '972'
ht-degree: 15%

---

# 다이렉트 메일 메시지 만들기 {#create-direct}

>[!CONTEXTUALHELP]
>id="ajo_direct_mail"
>title="다이렉트 메일 만들기"
>abstract="예약된 캠페인 및 여정에서 DM 메시지를 만들고 DM 공급자가 고객에게 메일을 보내는 데 필요한 추출 파일을 디자인합니다."

>[!CONTEXTUALHELP]
>id="ajo_journey_direct_mail"
>title="종료 활동"
>abstract="다이렉트 메일은 서드파티 다이렉트 메일 공급자가 고객에게 메일을 보내는 데 필요한 추출 파일을 개인화하고 생성할 수 있는 오프라인 채널입니다."

DM 메시지를 만들려면 예약된 캠페인이나 여정을 만들고 추출 파일을 구성합니다. DM 공급자가 고객에게 메일을 보낼 때 이 파일이 필요합니다.

>[!IMPORTANT]
>
>DM 메시지를 만들기 전에 다음을 구성했는지 확인하십시오.
>
>1. 추출 파일을 업로드하고 저장할 서버를 지정하는 [파일 라우팅 구성](../direct-mail/direct-mail-configuration.md#file-routing-configuration),
>1. 파일 라우팅 구성을 참조하는 [DM 메시지 구성](../direct-mail/direct-mail-configuration.md#direct-mail-surface).

## DM 메시지 추가 {#create-dm-campaign}

캠페인이나 여정에 DM 메시지를 추가하는 방법을 알아보려면 아래 탭을 살펴보십시오.

>[!BEGINTABS]

>[!TAB 여정에 DM 메시지 추가]

1. 여정을 열고 팔레트의 **[!UICONTROL 작업]** 섹션에서 **DM** 활동을 끌어서 놓습니다.

1. 메시지에 대한 기본 정보(레이블, 설명, 카테고리)를 입력한 다음 사용할 메시지 구성을 선택합니다. **[!UICONTROL 구성]** 필드는 기본적으로 미리 채워져 있으며 사용자가 해당 채널에 대해 마지막으로 사용한 구성입니다. 여정 구성 방법에 대한 자세한 내용은 [이 페이지](../building-journeys/journey-gs.md)를 참조하세요.

1. DM 공급자에게 보낼 추출 파일을 구성합니다. 이렇게 하려면 **[!UICONTROL 콘텐츠 편집]** 단추를 클릭하십시오.

   ![](assets/direct-mail-add-journey.png)

1. 표시할 파일 이름 또는 열과 같은 추출 파일 속성을 조정합니다. 추출 파일 속성을 구성하는 방법에 대한 자세한 내용은 [DM 메시지 만들기](../direct-mail/create-direct-mail.md#extraction-file) 섹션을 참조하십시오.

   ![](assets/direct-mail-journey-content.png)

1. 추출 파일의 콘텐츠가 정의되면 테스트 프로필을 사용하여 미리 볼 수 있습니다. 개인화된 콘텐츠를 삽입한 경우 테스트 프로필 데이터를 활용하여 이 콘텐츠가 메시지에 어떻게 표시되는지 확인할 수 있습니다.

   이렇게 하려면 **[!UICONTROL 콘텐츠 시뮬레이션]**&#x200B;을 클릭한 다음 테스트 프로필을 추가하여 테스트 프로필 데이터를 사용하여 추출 파일 렌더링 방법을 확인하십시오. 테스트 프로필을 선택하고 콘텐츠를 미리 보는 방법에 대한 자세한 내용은 [콘텐츠 관리](../content-management/preview-test.md) 섹션에서 확인할 수 있습니다.

   ![](assets/direct-mail-simulate.png){width="800" align="center"}

추출 파일이 준비되면 [여정](../building-journeys/journey-gs.md)의 구성을 완료하여 전송하십시오.

>[!TAB Campaign에 DM 메시지 추가]

1. **[!UICONTROL 캠페인]** 메뉴에 액세스한 다음 **[!UICONTROL 캠페인 만들기]**&#x200B;를 클릭합니다.

1. **예약됨 - 마케팅** 캠페인 유형을 선택합니다.

1. **[!UICONTROL 속성]** 섹션에서 Campaign의 **[!UICONTROL 제목]** 및 **[!UICONTROL 설명]**&#x200B;을(를) 편집합니다.

1. 타겟 대상을 정의하려면 **[!UICONTROL 대상 선택]** 단추를 클릭하고 사용 가능한 Adobe Experience Platform 대상 중에서 선택합니다. [자세히 알아보기](../audience/about-audiences.md).

   >[!IMPORTANT]
   >
   >현재 대상자 선택은 300만 프로필로 제한됩니다. 이 제한은 Adobe 담당자에게 요청하면 해제할 수 있습니다.

1. **[!UICONTROL ID 네임스페이스]** 필드에서 선택한 대상 내의 개인을 식별할 적절한 네임스페이스를 선택합니다. [자세히 알아보기](../event/about-creating.md#select-the-namespace).

1. **[!UICONTROL 작업]** 섹션에서 **[!UICONTROL DM]**&#x200B;을(를) 선택하세요.

1. 사용할 **[!UICONTROL DM 구성]**&#x200B;을(를) 선택하거나 만드십시오. [DM 구성을 만드는 방법을 알아보세요](direct-mail-configuration.md#direct-mail-surface).

   ![](assets/direct-mail-campaign.png){width="800" align="center"}

   >[!AVAILABILITY]
   >
   >DM은 **홀드아웃** 기능을 지원하지만 현재 **처리**&#x200B;를 지원하지 않습니다. [실험 작업 방법 알아보기](../content-management/get-started-experiment.md)

1. 특정 날짜에 대해 캠페인을 예약하거나 정기적으로 반복하도록 설정할 수 있습니다. **[!UICONTROL 이 섹션]**&#x200B;에서 캠페인의 [일정](../campaigns/campaign-schedule.md)을 구성하는 방법을 알아보세요.

이제 DM 공급자에게 보낼 추출 파일 구성을 시작할 수 있습니다.

## 추출 파일 구성 {#extraction-file}

>[!CONTEXTUALHELP]
>id="ajo_direct_mail_data_fields"
>title="데이터 필드"
>abstract="다이렉트 메일 공급자가 고객에게 메일을 보내는 데 필요한 추출 파일에 표시할 열과 정보를 추가하고 구성합니다. 최대 50개의 열을 추가할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_direct_mail_formatting"
>title="추출 파일 서식"
>abstract="각 필드에 대해 개인화 편집기를 사용하여 표시할 레이블과 정보를 지정합니다. <br/><br/><b>정렬 기준</b> 옵션을 사용하면 선택한 필드를 통해 추출 파일의 열을 정렬할 수 있습니다."

DM 공급자가 고객에게 메일을 보낼 때 추출 파일이 필요합니다. 추출 파일 구성을 정의하려면 다음 단계를 수행합니다.

1. 캠페인 구성 화면에서 **[!UICONTROL 콘텐츠 편집]** 단추를 클릭하여 추출 파일 콘텐츠를 구성합니다.

1. 추출 파일 속성을 조정합니다.

   1. **[!UICONTROL 파일 이름]** 필드에 추출 파일의 이름을 지정하십시오.

      >[!NOTE]
      >
      >기본적으로 파일은 서버의 루트 디렉터리에 기록됩니다. **[!UICONTROL 파일 이름]** 필드에도 &quot;/your/path/here/Filename.csv&quot; 형식을 사용할 수 있습니다. 여기서 지정된 경로는 선택한 서버의 대상 디렉터리입니다. <!--TBC if for SFTP and Azure only, or for all servers including S3-->

   1. 필요한 경우 지정된 파일 이름에 자동 타임스탬프를 추가하려면 **[!UICONTROL 타임스탬프를 파일 이름에 추가]** 옵션을 활성화합니다.

   1. 추출 파일의 시작 또는 끝 부분에 정보를 추가해야 하는 경우가 있습니다. 이렇게 하려면 **[!UICONTROL 메모]** 필드를 사용한 다음 메모를 머리글이나 바닥글로 포함할지 여부를 지정합니다.

      ![](assets/direct-mail-properties.png){width="800" align="center"}

1. 추출 파일에 표시할 열과 정보를 구성합니다.

   1. 새 열을 만들려면 **[!UICONTROL 추가]** 단추를 클릭하십시오.

   1. 선택한 열을 설정할 수 있는 **[!UICONTROL 서식]** 창이 오른쪽에 표시됩니다. 열에 대해 **[!UICONTROL Label]**&#x200B;을(를) 지정하십시오.

   1. **[!UICONTROL 데이터]** 필드에서 [개인화 편집기](../personalization/personalization-build-expressions.md)를 사용하여 표시할 프로필 특성을 선택합니다.

   1. 열을 사용하여 추출 파일을 정렬하려면 열을 선택하고 **[!UICONTROL 정렬 기준]** 옵션을 켜십시오. **[!UICONTROL 데이터 필드]** 섹션에서 열 레이블 옆에 **[!UICONTROL 정렬 기준]** 아이콘이 표시됩니다.

      ![](assets/direct-mail-content.png){width="800" align="center"}

   1. 추출 파일에 필요한 수만큼 열을 추가하려면 이 단계를 반복합니다. 최대 50개의 열을 추가할 수 있습니다.

      열의 위치를 변경하려면 열을 **[!UICONTROL 데이터 필드]** 섹션의 원하는 위치로 끌어서 놓습니다. 열을 삭제하려면 열을 선택하고 **[!UICONTROL 서식]** 창에서 **[!UICONTROL 제거]** 단추를 클릭합니다.

이제 DM 메시지를 테스트하여 대상자에게 보낼 수 있습니다. [DM 메시지를 테스트하고 보내는 방법 알아보기](test-send-direct-mail.md)
