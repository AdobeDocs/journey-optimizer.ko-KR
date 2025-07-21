---
solution: Journey Optimizer
product: journey optimizer
title: API 트리거 캠페인 검토 및 활성화
description: API 트리거 캠페인을 검토하고 활성화하는 방법에 대해 알아봅니다.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: 캠페인, API 트리거, REST, 최적화 도구, 메시지
source-git-commit: 1bdba8c5c1a9238d351b159551f6d3924935b339
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 4%

---


# API 트리거 캠페인 검토 및 활성화 {#api-review}

작업 캠페인이 구성되면 활성화하기 전에 해당 매개 변수와 콘텐츠를 검토해야 합니다. 이렇게 하려면 다음 단계를 수행합니다.

>[!IMPORTANT]
>
> 캠페인이 승인 정책의 적용을 받는 경우 캠페인을 보내려면 승인을 요청해야 합니다. [자세히 알아보기](../test-approve/gs-approval.md)

1. 캠페인 구성 화면에서 **[!UICONTROL 활성화 검토]**&#x200B;를 클릭하여 캠페인 요약을 표시합니다.

   ![](assets/campaign-review.png)

1. 캠페인 구성 요약이 표시되어 매개 변수가 잘못되거나 누락되었는지 확인하고 필요한 경우 캠페인을 수정할 수 있습니다.

   오류가 발생한 경우 캠페인을 활성화할 수 없습니다. 계속하기 전에 오류를 해결하십시오.

   ![](assets/create-campaign-alerts.png)

1. 캠페인이 올바르게 구성되었는지 확인한 다음 **[!UICONTROL 활성화]**&#x200B;를 클릭합니다.

1. 캠페인이 활성화되었습니다. 해당 상태는 **[!UICONTROL Live]**&#x200B;이거나 시작 날짜를 입력한 경우 **[!UICONTROL 예약됨]**&#x200B;입니다.

   **[!UICONTROL 완료됨]** 상태는 캠페인이 활성화된 후 3일 또는 캠페인 종료 날짜(반복 실행)에 자동으로 할당됩니다. [캠페인 상태에 대해 자세히 알아보기](get-started-with-campaigns.md#statuses).

   종료 날짜가 지정되지 않은 경우 캠페인은 **[!UICONTROL Live]** 상태를 유지합니다. 변경하려면 캠페인을 수동으로 중지해야 합니다. [캠페인을 중지하는 방법 알아보기](modify-stop-campaign.md)


1. 캠페인이 활성화되면 언제든지 해당 정보를 열어 확인할 수 있습니다. 이 요약을 사용하면 타겟팅된 프로필 수와 게재됨 및 실패한 작업 수에 대한 통계를 가져올 수 있습니다.

   **[!UICONTROL 보고서]** 단추를 클릭하여 전용 보고서에서 추가 통계를 얻을 수도 있습니다. [자세히 알아보기](../reports/campaign-global-report-cja.md)

   ![](assets/create-campaign-summary.png)

## 다음 단계 {#next}

API가 트리거된 캠페인이 준비되면 API를 사용하여 실행을 트리거할 수 있습니다. [자세히 알아보기](trigger-campaigns.md)
