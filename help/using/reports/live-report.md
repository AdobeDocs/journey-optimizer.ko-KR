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
TQID: https://experienceleague.adobe.com/RmJeQGDGLOM5LbdRS4HQbWE7sttyT4jGsuyXF-BdB-Q
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a9f73820-6899-47c2-a597-3fec28ab756aid: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04
subfeature_v2: id: d145add9-d5b9-481b-aa8a-e15e6bb7f813id: a7289281-9ae4-47b1-b8cf-4028b98af776id: b5afe8bf-bda6-41b5-ba06-922638872d63
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: b36ce7a039c976d80f49292e73be23c9b011b568
workflow-type: tm+mt
source-wordcount: 603
ht-degree: 2%

---

# 라이브 보고서 시작 {#live-report}

>[!BEGINSHADEBOX]

**이 페이지에서:** Adobe Journey Optimizer 실시간 보고서를 시작하여 여정 및 캠페인 성능을 실시간으로 시각화하고, 대시보드 위젯을 사용자 지정하고, 보고서를 내보냅니다.

>[!ENDSHADEBOX]

**[!UICONTROL 라이브 보고서]**&#x200B;를 사용하여 기본 제공 대시보드에서 여정 및 메시지의 영향과 성능을 실시간으로 측정하고 시각화할 수 있습니다. 게재를 보내거나 **[!UICONTROL 최근 24시간]** 탭에서 여정을 실행하는 즉시 **[!UICONTROL 실시간 보고서]**&#x200B;에서 데이터를 사용할 수 있습니다.

* 여정의 컨텍스트에서 여정을 타깃팅하려면 **[!UICONTROL 여정]** 메뉴에서 여정의 **[!UICONTROL 추가 작업]** 메뉴에 액세스하고 **[!UICONTROL 최근 24시간 보고서 보기]** 단추를 클릭하십시오.

  ![](assets/report_journey.png)

* 캠페인을 타깃팅하려면 **[!UICONTROL 캠페인]** 메뉴에서 캠페인에 액세스하고 **[!UICONTROL 보고서]** 버튼을 클릭한 다음 **[!UICONTROL 최근 24시간 보고서 보기]**&#x200B;를 클릭합니다.

  ![](assets/report_campaign.png)

Adobe Journey Optimizer에서 사용할 수 있는 모든 지표의 자세한 목록은 [이 페이지](#list-of-components-live)를 참조하세요.

>[!NOTE]
>
>라이브 보고서와 전체 보고서 간의 단기 불일치가 예상됩니다. 라이브 보고서는 실시간에 가까운 데이터 피드를 사용하지만, 실시간 보고서는 집계된 데이터를 사용합니다. 불일치가 발생하면 데이터가 일반적으로 해당 기간 내에 집계된 보기로 전파되므로 두 보고서를 조정하기 전에 최소 2시간을 허용하십시오.

## 대시보드 맞춤화 {#modify-dashboard}

위젯 크기를 조정하거나 위젯을 제거하여 각 보고 대시보드를 수정할 수 있습니다. 위젯을 변경하는 것은 현재 사용자의 대시보드에만 영향을 줍니다. 다른 사용자는 자신의 대시보드 또는 기본적으로 설정된 대시보드를 볼 수 있습니다.

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

다양한 보고서를 PDF 또는 CSV 형식으로 쉽게 내보내 공유하거나 인쇄할 수 있습니다.

>[!BEGINTABS]

>[!TAB 보고서를 PDF 파일로 내보내기]

1. 보고서에서 **[!UICONTROL 내보내기]**&#x200B;를 클릭하고 **[!UICONTROL PDF 파일]**&#x200B;을 선택합니다.

   ![](assets/export_6.png)

1. 인쇄 창에서 필요에 따라 문서를 구성합니다. 선택 사항은 브라우저에 따라 다를 수 있습니다.

1. 보고서를 PDF으로 인쇄하거나 저장하도록 선택합니다.

1. 파일을 저장할 폴더를 찾아 필요한 경우 이름을 변경한 다음 [저장]을 클릭합니다.

이제 PDF 파일에서 보고서를 보거나 공유할 수 있습니다.

>[!TAB 보고서를 CSV 파일로 내보내기]

1. 보고서에서 **[!UICONTROL 내보내기]**&#x200B;를 클릭하고 **[!UICONTROL CSV 파일]**&#x200B;을 선택하여 전체 보고서 수준에서 CSV 파일을 생성합니다.

   ![](assets/export_4.png)

1. 특정 위젯에서 데이터를 내보내도록 선택할 수도 있습니다. 선택한 위젯 옆에 있는 **[!UICONTROL CSV 파일 다운로드]**&#x200B;를 클릭합니다.

   ![](assets/export_5.png)

1. 파일은 자동으로 다운로드되며 로컬 파일에서 찾을 수 있습니다.

   보고서 수준에서 파일을 생성한 경우, 여기에는 제목 및 데이터를 포함하여 각 위젯에 대한 자세한 정보가 포함됩니다.

   위젯 수준에서 파일을 생성한 경우 선택한 위젯에 대한 데이터가 특별히 제공됩니다.

>[!ENDTABS]
