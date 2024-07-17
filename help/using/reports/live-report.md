---
solution: Journey Optimizer
product: journey optimizer
title: 라이브 보고서
description: 라이브 보고서의 데이터를 사용하는 방법을 알아봅니다
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 8dd48bb2-a805-4c46-a16c-c68173a9ac08
source-git-commit: 9a1eea69c47ace2ad9bbd1d4668007b8ea1796fc
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 1%

---

# 라이브 보고서 시작 {#live-report}

**[!UICONTROL 라이브 보고서]**를 사용하여 기본 제공 대시보드에서 여정 및 메시지의 영향과 성능을 실시간으로 측정하고 시각화할 수 있습니다.
게재를 보내거나 **[!UICONTROL 최근 24시간]** 탭에서 여정을 실행하는 즉시 **[!UICONTROL 실시간 보고서]**&#x200B;에서 데이터를 사용할 수 있습니다.

* 여정의 컨텍스트에서 여정을 타깃팅하려면 **[!UICONTROL 여정]** 메뉴에서 여정에 액세스하고 **[!UICONTROL 보고서 보기]** 단추를 클릭합니다.

  ![](assets/report_journey.png)

* 캠페인을 타깃팅하려면 **[!UICONTROL 캠페인]** 메뉴에서 캠페인에 액세스하고 **[!UICONTROL 보고서]** 단추를 클릭하십시오.

  ![](assets/report_campaign.png)

* 게재를 위해 **[!UICONTROL 글로벌 보고서]**&#x200B;에서 **[!UICONTROL 라이브 보고서]**(으)로 전환하려면 탭 전환기에서 **[!UICONTROL 최근 24시간]**&#x200B;을 클릭하세요.

  ![](assets/report_3.png)

Adobe Journey Optimizer에서 사용할 수 있는 모든 지표의 자세한 목록은 [이 페이지](#list-of-components-live)를 참조하세요.

## 대시보드 맞춤화 {#modify-dashboard}

위젯의 크기를 조정하거나 제거하여 각 보고 대시보드를 수정할 수 있습니다. 위젯을 변경하는 것은 현재 사용자의 대시보드에만 영향을 줍니다. 다른 사용자는 자신의 대시보드 또는 기본적으로 설정된 대시보드를 볼 수 있습니다.

1. **[!UICONTROL 작업]** 드롭다운에서 여정의 특정 작업 중 하나를 보고하려면 선택합니다.

1. 토글 막대를 사용하여 보고서에서 테스트 이벤트를 제외하려면 선택합니다. 테스트 이벤트에 대한 자세한 내용은 [이 페이지](../building-journeys/testing-the-journey.md)를 참조하세요.

   **[!UICONTROL 테스트 이벤트 제외]** 옵션은 여정 보고서에만 사용할 수 있습니다.

   ![](assets/report_modify_6.png)

1. 위젯의 크기를 조정하거나 제거하려면 **[!UICONTROL 수정]**&#x200B;을 클릭하세요.

   ![](assets/report_modify_7.png)

1. 오른쪽 아래 모서리를 끌어 위젯 크기를 조정합니다.

   ![](assets/report_modify_8.png)

1. 필요하지 않은 위젯을 제거하려면 **[!UICONTROL 제거]**&#x200B;를 클릭하십시오.

   ![](assets/report_modify_9.png)

1. 표시 순서 및 위젯 크기에 만족하면 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

1. 데이터 표시 방식을 사용자 정의하기 위해 그래프, 표, 도넛 차트 등 다양한 시각화 옵션에서 전환할 수 있습니다.

   ![](assets/report_modify_11.png)

이제 대시보드가 저장되었습니다. 다른 변경 사항은 나중에 라이브 보고서를 사용할 수 있도록 다시 적용됩니다. 필요한 경우 **[!UICONTROL 재설정]** 옵션을 사용하여 기본 위젯 및 위젯의 순서를 복원합니다.

## 보고서 내보내기 {#export-reports}

서로 다른 보고서를 PDF 또는 CSV 형식으로 쉽게 내보내 공유하거나 인쇄할 수 있습니다.

>[!BEGINTABS]

>[!TAB 보고서를 PDF 파일로 내보내기]

1. 보고서에서 **[!UICONTROL 내보내기]**&#x200B;를 클릭하고 **[!UICONTROL 파일 PDF]**&#x200B;을 선택합니다.

   ![](assets/export_6.png)

1. 인쇄 창에서 필요에 따라 문서를 구성합니다. 선택 사항은 브라우저에 따라 다를 수 있습니다.

1. 보고서를 PDF으로 인쇄 또는 저장하도록 선택합니다.

1. 파일을 저장할 폴더를 찾아 필요한 경우 이름을 변경한 다음 [저장]을 클릭합니다.

이제 PDF 파일에서 보고서를 보거나 공유할 수 있습니다.

>[!TAB 보고서를 CSV 파일로 내보내기]

1. 보고서에서 **[!UICONTROL 내보내기]**&#x200B;를 클릭하고 **[!UICONTROL CSV 파일]**&#x200B;을 선택하여 전체 보고서 수준에서 CSV 파일을 생성합니다.

   ![](assets/export_4.png)

1. 특정 위젯에서 데이터를 내보내도록 선택할 수도 있습니다. 선택한 위젯 옆에 있는 **[!UICONTROL 위젯 데이터를 CSV로 내보내기]**&#x200B;를 클릭합니다.

   ![](assets/export_5.png)

1. 파일은 자동으로 다운로드되며 로컬 파일에서 찾을 수 있습니다.

   보고서 수준에서 파일을 생성한 경우, 여기에는 제목 및 데이터를 포함하여 각 위젯에 대한 자세한 정보가 포함됩니다.

   위젯 수준에서 파일을 생성한 경우 선택한 위젯에 대한 데이터가 특별히 제공됩니다.

>[!ENDTABS]
