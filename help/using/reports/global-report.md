---
solution: Journey Optimizer
product: journey optimizer
title: 글로벌 보고서
description: 글로벌 보고서의 데이터를 사용하는 방법을 알아봅니다
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: ec15e700-7659-4dbf-8446-6534ea48c5c8
source-git-commit: 47482adb84e05fe41eb1c50479a8b50e00469ec4
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 28%

---

# 글로벌 보고서 시작 {#global-report}

>[!AVAILABILITY]
>
>현재 보고 경험은 2025년 1월부터 종료됩니다. 이 날짜 이후에는 새로운 보고 경험이 표준이 됩니다. 원활한 전환을 위해 새로운 기능을 숙지하는 것이 좋습니다. [Journey Optimizer 새 보고 인터페이스를 시작합니다.](report-gs-cja.md)

>[!NOTE]
>
> 쿼리 서비스를 사용할 때 API를 통해 사용자 지정 쿼리가 만들어지는 경우 보고서에 약간의 지연이 있을 것으로 예상하십시오.

**[!UICONTROL 전역 보고서]**&#x200B;를 사용하여 선택한 기간 동안 여정 및 게재의 영향을 측정합니다.

* 여정의 컨텍스트에서 여정 또는 게재를 타겟팅하려면 **[!UICONTROL 여정]** 메뉴에서 여정에 액세스하고 **[!UICONTROL 보고서 보기]** 단추를 클릭합니다. 그런 다음 여정, 이메일, SMS 및 푸시 글로벌 보고서를 찾을 수 있습니다.

  ![](assets/report_journey.png)

* 캠페인을 타깃팅하려면 **[!UICONTROL 캠페인]** 메뉴에서 캠페인에 액세스하고 **[!UICONTROL 보고서]** 단추를 클릭하십시오.

  ![](assets/report_campaign.png)

* 게재할 **[!UICONTROL 실시간 보고서]**&#x200B;에서 **[!UICONTROL 전역 보고서]**(으)로 전환하려면 탭 전환기에서 **[!UICONTROL 항상]**&#x200B;을(를) 클릭하십시오.

  ![](assets/report_5.png)

Adobe Journey Optimizer에서 사용할 수 있는 모든 지표의 자세한 목록은 [이 페이지](#list-of-components-global)를 참조하세요.

## 대시보드 맞춤화 {#modify-dashboard}

기간을 변경하고 위젯의 크기를 조정하거나 제거하여 각 보고 대시보드를 수정할 수 있습니다. 위젯을 변경하는 것은 현재 사용자의 대시보드에만 영향을 줍니다. 다른 사용자는 자신의 대시보드 또는 기본적으로 설정된 대시보드를 볼 수 있습니다.

1. 글로벌 보고서에서 특정 데이터를 타겟팅할 시작 및 종료 시간을 선택합니다.

   ![](assets/report_modify_1.png)

1. 구성된 여러 **[!UICONTROL 작업]**&#x200B;이 포함된 여정 보고서의 경우 드롭다운 메뉴에서 특정 **[!UICONTROL 작업]**&#x200B;을(를) 선택하십시오.

1. 하나 또는 여러 개의 반복 메시지만 대상으로 지정하려면 **[!UICONTROL 실행 시간]** 드롭다운에서 선택합니다.

   ![](assets/report_modify_12.png)

1. 토글 막대를 사용하여 보고서에서 테스트 이벤트를 제외하려면 선택합니다. 테스트 이벤트에 대한 자세한 내용은 [이 페이지](../building-journeys/testing-the-journey.md)를 참조하세요.

   **[!UICONTROL 테스트 이벤트 제외]** 옵션은 여정 보고서에만 사용할 수 있습니다.

   ![](assets/report_modify_2.png)

1. 대시보드 사용자 지정을 시작하려면 **[!UICONTROL 수정]**&#x200B;을 클릭하세요.

   ![](assets/report_modify_3.png)

1. 오른쪽 아래 모서리를 끌어 위젯 크기를 조정합니다.

   ![](assets/report_modify_4.png)

1. 필요하지 않은 위젯을 제거하려면 **[!UICONTROL 제거]**&#x200B;를 클릭하십시오.

   ![](assets/report_modify_5.png)

1. 표시 순서 및 위젯 크기에 만족하면 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

1. 데이터 표시 방식을 사용자 정의하기 위해 그래프, 표, 도넛 차트 등 다양한 시각화 옵션에서 전환할 수 있습니다.

   ![](assets/report_modify_10.png)

이제 대시보드가 저장되었습니다. 다른 변경 사항은 나중에 라이브 보고서를 사용할 수 있도록 다시 적용됩니다. 필요한 경우 **[!UICONTROL 재설정]** 옵션을 사용하여 기본 위젯 및 위젯의 순서를 복원합니다.

## 보고서 내보내기 {#export-reports}

서로 다른 보고서를 PDF 또는 CSV 형식으로 쉽게 내보내 공유하거나 인쇄할 수 있습니다. 보고서를 내보내는 단계는 아래 탭에 자세히 설명되어 있습니다.

➡️ [비디오에서 이 기능 살펴보기](#video-csv)


>[!BEGINTABS]

>[!TAB 보고서를 CSV 파일로 내보내기]

1. 보고서에서 **[!UICONTROL 내보내기]**&#x200B;를 클릭하고 **[!UICONTROL CSV 파일]**&#x200B;을 선택하여 전체 보고서 수준에서 CSV 파일을 생성합니다.

   ![](assets/export_1.png)

1. 특정 위젯에서 데이터를 내보내도록 선택할 수도 있습니다. 선택한 위젯 옆에 있는 **[!UICONTROL 위젯 데이터를 CSV로 내보내기]**&#x200B;를 클릭합니다.

   ![](assets/export_3.png)

1. 파일은 자동으로 다운로드되며 로컬 파일에서 찾을 수 있습니다.

   보고서 수준에서 파일을 생성한 경우, 여기에는 제목 및 데이터를 포함하여 각 위젯에 대한 자세한 정보가 포함됩니다.

   위젯 수준에서 파일을 생성한 경우 선택한 위젯에 대한 데이터가 특별히 제공됩니다.

>[!TAB 보고서를 PDF 파일로 내보내기]

1. 보고서에서 **[!UICONTROL 내보내기]**&#x200B;를 클릭하고 **[!UICONTROL 파일 PDF]**&#x200B;을 선택합니다.

   ![](assets/export_2.png)

1. 인쇄 창에서 필요에 따라 문서를 구성합니다. 선택 사항은 브라우저에 따라 다를 수 있습니다.

1. 보고서를 PDF으로 인쇄 또는 저장하도록 선택합니다.

1. 파일을 저장할 폴더를 찾아 필요한 경우 이름을 변경한 다음 [저장]을 클릭합니다.

이제 PDF 파일에서 보고서를 보거나 공유할 수 있습니다.



>[!ENDTABS]


### 보고서 내보내기 (비디오) {#video-csv}

다음 방법 비디오에서 보고서 및 단일 위젯에 대한 CSV 보고서를 다운로드하는 방법을 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/3424603?quality=12)



>[!CONTEXTUALHELP]
>id="ajo_report_campaign_ctr"
>title="CTR"
>abstract="CTR 위젯"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_clicks"
>title="클릭수"
>abstract="클릭수 위젯"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_delivered"
>title="게재됨"
>abstract="게재된 위젯"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_overview"
>title="캠페인 개요"
>abstract="캠페인 개요 위젯"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_funnel"
>title="캠페인 단계 결과"
>abstract="캠페인 단계 결과 위젯"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_tracking_link"
>title="추적된 링크 레이블"
>abstract="추적된 링크 레이블 위젯"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_displays"
>title="디스플레이"
>abstract="디스플레이 위젯"

<!--campaign email-->

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_delivered_click"
>title="게재 및 클릭 트렌드"
>abstract="게재됨 및 클릭 트렌드 위젯"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_delivery_status"
>title="게재 상태"
>abstract="게재 상태 위젯"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_sending_statistics"
>title="전송 통계"
>abstract="전송 통계 위젯"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_tracking_statistics"
>title="추적 통계"
>abstract="추적 통계 위젯"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_domains"
>title="이메일 도메인"
>abstract="이메일 도메인 위젯"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_tracked_link"
>title="추적된 링크 레이블"
>abstract="추적된 링크 레이블 위젯"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_tracked_link_urls"
>title="추적된 링크 URL"
>abstract="추적된 링크 URL 위젯"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_subjects"
>title="이메일 제목"
>abstract="이메일 제목 위젯"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_bounce_reasons"
>title="바운스 이유"
>abstract="바운스 이유 위젯"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_exclude"
>title="제외 이유"
>abstract="제외 이유 위젯"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_error"
>title="오류 원인"
>abstract="오류 이유 위젯"


<!--campaign push-->

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_push_sending_statistics"
>title="전송 통계"
>abstract="전송 통계 위젯"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_push_tracking_statistics"
>title="추적 통계"
>abstract="추적 통계 위젯"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_push_tracked_link"
>title="추적된 링크 레이블"
>abstract="추적된 링크 레이블 위젯"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_push_tracked_link_urls"
>title="추적된 링크 URL"
>abstract="추적된 링크 URL 위젯"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_push_bounce_reasons"
>title="바운스 이유"
>abstract="바운스 이유 위젯"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_push_exclude"
>title="제외된 이유"
>abstract="제외됨 이유 위젯"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_push_email_error"
>title="오류 원인"
>abstract="오류 이유 위젯"

<!--campaign inapp-->


>[!CONTEXTUALHELP]
>id="ajo_report_campaign_inapp_impression"
>title="노출 횟수 및 클릭 트렌드"
>abstract="노출 횟수 및 클릭 트렌드 위젯"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_inapp_clicks"
>title="클릭수"
>abstract="클릭수 위젯"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_inapp_displays"
>title="디스플레이"
>abstract="디스플레이 위젯"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_inapp_tracking_data"
>title="추적 데이터"
>abstract="추적 데이터 위젯"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_inapp_tracked_link"
>title="추적된 링크 레이블"
>abstract="추적된 링크 레이블 위젯"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_inapp_tracked_link_urls"
>title="추적된 링크 URL"
>abstract="추적된 링크 URL 위젯"

<!--campaign sms-->


>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_delivered_click"
>title="게재 및 클릭 트렌드"
>abstract="게재됨 및 클릭 트렌드 위젯"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_delivery_status"
>title="게재 상태"
>abstract="게재 상태 위젯"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_tracked_link"
>title="추적된 링크 레이블"
>abstract="추적된 링크 레이블 위젯"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_tracked_link_urls"
>title="추적된 링크 URL"
>abstract="추적된 링크 URL 위젯"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_inbound"
>title="SMS 인바운드 메시지"
>abstract="SMS 인바운드 메시지 위젯"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_message_type"
>title="SMS 메시지 유형"
>abstract="SMS 메시지 유형 위젯"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_providers"
>title="SMS 공급자"
>abstract="SMS 공급자 위젯"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_bounce"
>title="바운스 이유"
>abstract="바운스 이유 위젯"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_exclude"
>title="제외 이유"
>abstract="제외 이유 위젯"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_error"
>title="오류 원인"
>abstract="오류 이유 위젯"
