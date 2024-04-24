---
solution: Journey Optimizer
product: journey optimizer
title: 비즈니스 규칙
description: 비즈니스 규칙을 만들고 적용하는 방법 알아보기
feature: Rules
topic: Content Management
role: User
level: Intermediate
keywords: 메시지, 빈도, 규칙, 압력
hide: true
hidefromtoc: true
badge: label="Beta"
source-git-commit: c1eef06b0edc4e1bcd1b145f8f822295924b205c
workflow-type: tm+mt
source-wordcount: '1426'
ht-degree: 10%

---

# 비즈니스 규칙 {#business-rules}

>[!AVAILABILITY]
>
>비즈니스 규칙은 현재 사용자를 선택하는 베타 버전으로 사용할 수 있습니다.

[!DNL Journey Optimizer] 을 사용하면 메시지 및 작업에서 과도하게 요청된 프로필을 자동으로 제외하는 채널 간 규칙을 설정하여 사용자가 메시지를 받는 빈도를 제어할 수 있습니다.

예를 들어 브랜드의 경우, 한 달에 4개 이하의 마케팅 메시지를 고객에게 보내는 규칙이 있을 수 있습니다. 이렇게 하려면 월별 캘린더 기간 동안 하나 이상의 채널을 기반으로 전송된 메시지 수를 제한하는 빈도 규칙을 사용할 수 있습니다.

세부 기간을 개선하기 위해 서로 다른 규칙 세트를 만들어 다음과 같은 작업을 수행합니다. [!DNL Journey Optimizer] 에서는 다른 유형의 마케팅 커뮤니케이션에 빈도 제한을 적용할 수 있습니다. 예를 들어 의 수를 제한하는 규칙 세트를 만들 수 있습니다. **프로모션 커뮤니케이션** (으)로 보낸 다음 수를 제한하는 다른 규칙 세트를 만듭니다. **뉴스레터** 보내졌습니다.

>[!NOTE]
>
>비즈니스 규칙은 사용자가 브랜드로부터 커뮤니케이션 수신을 취소할 수 있는 옵트아웃 관리와는 다릅니다. [자세히 알아보기](../privacy/opt-out.md#opt-out-management)

## 규칙 세트 액세스 {#access-rule-sets}

규칙 세트는 다음에서 사용할 수 있습니다. **[!UICONTROL 관리]** > **[!UICONTROL 비즈니스 규칙(Beta)]** 메뉴 아래의 제품에서 사용할 수 있습니다. 모든 규칙이 표시되며, 만든 날짜별로 정렬됩니다.

![](assets/rule-sets-list.png)

규칙 세트 이름을 클릭하여 해당 콘텐츠를 보고 편집합니다. 해당 규칙 세트에 포함된 모든 규칙이 나열됩니다.

오른쪽 상단의 상황별 메뉴를 사용하면 다음 작업을 수행할 수 있습니다.

* 규칙 세트의 이름 및 설명 편집
* 규칙 세트 활성화 - [자세히 알아보기](#activate-rule)
* 규칙 세트 삭제

![](assets/rule-set-example.png)

규칙 세트의 각 규칙에 대해 **[!UICONTROL 추가 작업]** 버튼을 사용하면 다음 작업을 수행할 수 있습니다.

* 규칙 편집
* 규칙 활성화 [자세히 알아보기](#activate-rule)
* 규칙 삭제

![](assets/rule-set-example-rules.png)

<!--### Permissions{#permissions-frequency-rules}

To access, create, edit or delete message frequency rules, you must have the **[!UICONTROL Manage frequency rules]** permission. 

Users with the **[!UICONTROL View frequency rules]** permission are able to view rules, but not to modify or delete them.

![](assets/message-rules-access.png)

Learn more about permissions in [this section](../administration/high-low-permissions.md).-->

## 규칙 세트 만들기 {#create-rule-set}

규칙 세트를 만들려면 아래 단계를 수행합니다.

1. 액세스 **[!UICONTROL 규칙 세트]** 목록을 작성한 다음 **[!UICONTROL 규칙 집합 만들기]**.

   ![](assets/rule-sets-create-button.png)

1. 규칙 세트 이름을 정의하고 필요한 경우 설명을 추가한 다음 을 클릭합니다. **[!UICONTROL 저장]**.

   ![](assets/rule-sets-create.png)

   >[!NOTE]
   >
   >규칙 세트 이름은 고유해야 합니다.

1. 이제 다음을 수행할 수 있습니다 [규칙 정의](#create-new-rule) 이 규칙 세트에 추가하고 [활성화](#activate-rule) 그래.

   >[!NOTE]
   >
   >메시지에 적용할 모든 규칙이 규칙 집합에서도 활성화되어 있는지 확인합니다.

## 규칙 만들기 {#create-new-rule}

>[!CONTEXTUALHELP]
>id="ajo_rule_sets_category"
>title="메시지 규칙 범주 선택"
>abstract="활성화되어 메시지에 적용되면 선택한 범주와 일치하는 모든 빈도 규칙은 이 메시지에 자동으로 적용됩니다. 현재 마케팅 범주만 사용할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_rule_sets_capping"
>title="규칙의 상한 설정"
>abstract="선택한 시간대 내에 고객 프로필로 전송되는 최대 메시지 수를 지정합니다. 빈도 캡은 선택된 캘린더 기간에 기반하고 대응하는 시간대가 시작될 때 재설정됩니다."

>[!CONTEXTUALHELP]
>id="ajo_rule_sets_channel"
>title="규칙이 적용되는 채널 정의"
>abstract="하나 이상의 채널을 선택합니다. 상한 설정은 채널에서 총 횟수로 적용됩니다."

규칙 세트에 규칙을 추가하려면 아래 단계를 수행합니다.

1. 방금 만든 규칙 세트에서 **[!UICONTROL 규칙 추가]**.

   ![](assets/rule-sets-create-rule-button.png)

1. 규칙 이름을 정의합니다.

   >[!NOTE]
   >
   >규칙 세트 이름은 고유해야 합니다.

1. 메시지 규칙 범주를 선택합니다.

   >[!NOTE]
   >
   >현재는 **[!UICONTROL 마케팅]** 카테고리를 사용할 수 있습니다.

1. 다음에서 **[!UICONTROL 기간]** 드롭다운 목록에서 적용할 캡핑에 대한 시간대를 선택합니다. [자세히 알아보기](#frequency-cap)

1. 규칙의 상한을 설정합니다. 즉, 위의 선택에 따라 매월, 주 또는 일별로 개별 사용자 프로필에 보낼 수 있는 최대 메시지 수를 의미합니다.

1. 이 규칙에 사용할 채널 선택: **[!UICONTROL 이메일]**, **[!UICONTROL SMS]**, **[!UICONTROL 푸시 알림]** 또는 **[!UICONTROL 다이렉트 메일]**.

   ![](assets/rule-set-channels.png)

   >[!NOTE]
   >
   >규칙을 만들려면 채널을 하나 이상 선택해야 합니다.

1. 선택한 모든 채널에 캡핑을 총 카운트로 적용하려면 여러 채널을 선택하십시오.

   예를 들어 최대 가용량 을 5로 설정하고 이메일 채널과 sms 채널을 모두 선택합니다. 프로필이 선택한 기간 동안 이미 3개의 마케팅 이메일과 2개의 마케팅 SMS를 받은 경우, 이 프로필은 다음 마케팅 이메일 또는 SMS 게재에서 제외됩니다.

1. 클릭 **[!UICONTROL 저장]** 규칙 만들기를 확인합니다. 메시지가 규칙 세트에 추가되고 **[!UICONTROL 초안]** 상태.

   ![](assets/rule-set-rule-created.png)

1. 위의 단계를 반복하여 규칙 세트에 필요한 만큼 규칙을 추가합니다.

이제 모든 메시지에 적용하려면 먼저 각 규칙을 활성화해야 합니다. [자세히 알아보기](#activate-rule)

>[!NOTE]
>
>메시지에서 규칙 세트를 선택할 수 있도록 규칙 세트도 활성화되었는지 확인합니다.

### 빈도 상한 {#frequency-cap}

>[!CONTEXTUALHELP]
>id="ajo_rule_sets_duration"
>title="메시지 규칙 범주 선택"
>abstract="활성화되어 메시지에 적용되면 선택한 범주와 일치하는 모든 빈도 규칙은 이 메시지에 자동으로 적용됩니다. 현재 마케팅 범주만 사용할 수 있습니다."

다음에서 **[!UICONTROL 기간]** 월별, 주별 또는 일별로 상한을 적용하려면 드롭다운 목록을 선택합니다.

빈도 상한은 선택한 달력 기간을 기반으로 합니다. 해당 시간대의 시작 부분에서 재설정됩니다.

![](assets/rule-set-capping-duration.png)

기간별 사용기간 종료일은 다음 각 호와 같다.

* **[!UICONTROL 월별]**: 빈도 상한은 월 마지막 날인 23일까지 유효합니다.:59:59 UTC입니다. 예를 들어 1월의 월별 만료일은 01-31 23입니다:59:59 UTC입니다.

* **[!UICONTROL 매주]**: 빈도 상한은 토요일 23일까지 유효합니다:59:캘린더 주가 일요일에 시작됨에 따라 해당 주의 59 UTC입니다. 만료는 규칙 생성과 무관합니다. 예를 들어, 규칙이 목요일에 만들어지면 이 규칙은 토요일 23까지 유효합니다:59:59.

* **[!UICONTROL 매일]**: 일별 빈도 상한은 23일까지 일에 대해 유효합니다.:59:59 UTC이고 다음 날 시작 시 0으로 재설정됩니다.

### 일일 빈도 상한 {#daily-frequency-cap}

>[!CAUTION]
>
>일별 빈도 제한 규칙의 정확도를 보장하기 위해 [스트리밍 세분화](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/streaming-segmentation.html){target="_blank"} 은(는) 필수입니다. 에서 대상 평가 방법에 대해 자세히 알아보기 [이 섹션](../audience/about-audiences.md#evaluation-method-in-journey-optimizer).

최대 시간당 6천만 개의 메시지 제한까지 모든 세그먼트 크기<!--not clear-->, 캠페인과 최소 2시간 차이가 있는지 확인하십시오.


<!-- Journey example:

* If customer sets a Daily rule under the Global Ruleset for email <= 2/day:
   * Journey 123 (scheduled for noon)
   * Journey 456 (scheduled for noon)
   * Journey 789 (scheduled for 1 pm)

   In this example, the Daily Frequency cap will not guarantee <= 2/day. The rule will only be guaranteed when Journeys are at least 2 hours apart:
   * Journey 123 (scheduled for noon)
   * Journey 456 (scheduled for 2 pm)
   * Journey 789 (scheduled for 4 pm)-->

예를 들어 이메일 채널에 대해 2일 이하의 규칙 세트 아래에 일별 규칙을 설정하고 다음 캠페인을 만드는 경우,
* 캠페인 A(정오에 예약됨)
* 캠페인 A(오후 3시로 예약됨)
* 캠페인 B(오후 1시로 예약됨)

이 설정은 다음 두 가지 이유로 작동하지 않습니다.
* 캠페인이 2시간 간격이 아니므로 일일 빈도 상한은 보장되지 않습니다.
* 일일 상한제를 활용하기 위해 동일한 캠페인을 하루에 여러 번 예약하는 것은 좋은 방법이 아닙니다.

아래 예제는 일일 빈도 상한에 따라 적용되어야 합니다.
* 캠페인 A(정오에 예약됨)
* 캠페인 B(오후 2시로 예약됨)

<!--* To use the Daily Cap with a Journey, customers can use either an Event Triggered Journey or an Audience Qualified Journey. If customers wish to use the Daily Cap with a Read Audience Journey, they should use a Campaign instead and associate a Local Ruleset with the campaign, following the example given above.-->

## 규칙 및 규칙 세트 활성화 {#activate-rule}

규칙이 만들어지면 **[!UICONTROL 초안]** 은(는) 상태이며 아직 메시지에 영향을 주지 않습니다. 활성화하려면 **[!UICONTROL 추가 작업]** 규칙 옆에 있는 버튼을 클릭하고 다음을 선택합니다. **[!UICONTROL 활성화]**.

![](assets/rule-set-activate-rule.png)

캠페인/여정에서 규칙 세트에 액세스하고 메시지에 적용하려면 규칙 세트를 활성화해야 합니다.

![](assets/rule-set-activate-set.png)

규칙 세트를 활성화하면 규칙 세트가 다음 실행에 적용되는 모든 메시지에 영향을 줍니다. 방법 알아보기 [메시지에 규칙 세트 적용](#apply-rule-set).

>[!NOTE]
>
>규칙 또는 규칙 세트가 완전히 활성화되려면 최대 10분이 걸릴 수 있습니다. 규칙을 적용하려면 메시지를 수정하거나 여정을 다시 게시할 필요가 없습니다.

<!--Currently, once a rule set is activated, no more rules can be added to that rule set.-->

## 규칙 및 규칙 세트 비활성화 {#deactivate-rule}

규칙 또는 규칙 세트를 비활성화하려면 **[!UICONTROL 추가 작업]** 원하는 항목 옆에 있는 버튼을 선택하고 **[!UICONTROL 비활성화]**.

![](assets/rule-set-inactive-rule.png)

상태가 (으)로 변경됩니다. **[!UICONTROL 비활성]** 및 규칙은 향후 메시지 실행에 적용되지 않습니다. 현재 실행 중인 모든 메시지는 영향을 받지 않습니다.

>[!NOTE]
>
>규칙 또는 규칙 세트를 비활성화하는 것은 개별 프로필의 카운트에 영향을 주거나 재설정되지 않습니다.

## 메시지에 빈도 규칙 적용 {#apply-frequency-rule}

메시지에 빈도 규칙을 적용하려면 아래 단계를 수행합니다.

1. 를 만들 때 [campaign](../campaigns/create-campaign.md)규칙 세트에 대해 정의한 채널 중 하나를 선택하고 메시지 콘텐츠를 편집합니다.

1. 콘텐츠 편집 화면에서 다음을 클릭합니다. **[!UICONTROL 비즈니스 규칙 추가]** 단추를 클릭합니다.

1. 다음 항목 선택 [생성한 규칙 세트](#create-rule-set).

   ![](assets/rule-set-campaign-add-rule-button.png)

   >[!NOTE]
   >
   >전용 [활성화됨](#activate-rule) 규칙 세트가 목록에 표시됩니다.

   <!--Messages where the category selected is **[!UICONTROL Transactional]** will not be evaluated against business rules.-->

1. 게재에서 제외된 프로필 수를 볼 수 있습니다. [글로벌 보고서](../reports/global-report.md), 및 [라이브 보고서](../reports/live-report.md): 사용자가 게재에서 제외되는 가능한 이유로 빈도 규칙이 나열됩니다.

>[!NOTE]
>
>동일한 채널에 여러 규칙을 적용할 수 있지만 하위 상한에 도달하면 프로필이 다음 게재에서 제외됩니다.

<!--
## Example: combine several rules {#frequency-rule-example}

You can combine several message frequency rules, such as described in the example below.

1. [Create a rule](#create-new-rule) called *Overall Marketing Capping*:

   * Select all channels.
   * Set capping to 12 monthly.

   ![](assets/message-rules-ex-overall-cap.png)

1. To further restrict the number of marketing-based push notifications that a user is sent, create a second rule called *Push Marketing Cap*:

   * Select Push channel.
   * Set capping to 4 monthly.

   ![](assets/message-rules-ex-push-cap.png)

1. Save and [activate](#activate-rule) the rule.

1. [Create a message](../building-journeys/journeys-message.md) for every channel you want to communicate through and select the **[!UICONTROL Marketing]** category for each message. [Learn how to apply a frequency rule](#apply-frequency-rule)

   ![](assets/journey-message-category.png)

In this scenario, an individual profile:
* can receive up to 12 marketing messages per month;
* but will be excluded from marketing push notifications after they have received 4 push notifications.-->

빈도 규칙을 테스트할 때에는 새로 만든 를 사용하는 것이 좋습니다 [테스트 프로필](../audience/creating-test-profiles.md), 프로필의 빈도 상한에 도달하면 다음 기간까지 카운터를 재설정할 방법이 없기 때문입니다. 규칙을 비활성화하면 캡핑된 프로필에서 메시지를 받을 수 있지만 카운터 증분은 제거되거나 삭제되지 않습니다.

