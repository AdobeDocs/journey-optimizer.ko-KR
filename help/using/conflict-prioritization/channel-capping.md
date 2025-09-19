---
solution: Journey Optimizer
product: journey optimizer
title: 규칙 세트 작업
description: 규칙 세트를 만들고 적용하는 방법 알아보기
feature: Rules
topic: Content Management
role: User
level: Intermediate
keywords: 메시지, 빈도, 규칙, 압력
exl-id: 80bd5a61-1368-435c-9a9a-dd84b9e4c208
source-git-commit: 8c3ff6c60f846af2cddc8c84507cd64fd457cbbb
workflow-type: tm+mt
source-wordcount: '1225'
ht-degree: 5%

---

# 채널 및 커뮤니케이션 유형별 빈도 캡핑 {#rule-sets}

**채널** 규칙 집합은 최대 가용량 규칙을 통신 채널에 적용합니다. 예를 들어 하루에 1개 이상의 이메일 또는 SMS 커뮤니케이션을 보내지 마십시오.

채널 규칙 세트를 활용하면 통신 유형별로 빈도 상한을 설정하여 유사한 메시지가 있는 고객을 오버로드할 수 있습니다. 예를 들어 고객에게 전송되는 **프로모션 커뮤니케이션**&#x200B;의 수를 제한하는 규칙 세트와 고객에게 전송되는 **뉴스레터**&#x200B;의 수를 제한하는 규칙 세트를 만들 수 있습니다. 생성 중인 캠페인 유형에 따라 프로모션 커뮤니케이션 또는 뉴스레터 규칙 세트를 적용하도록 선택할 수 있습니다.

>[!IMPORTANT]
>
>여정 수준 제한이 올바로 작동하도록 하려면 캠페인이나 채널을 작성하는 동안 우선 순위가 가장 높은 네임스페이스를 선택해야 합니다. [플랫폼 ID 서비스 안내서](https://experienceleague.adobe.com/ko/docs/experience-platform/identity/features/identity-graph-linking-rules/namespace-priority){target="_blank"}에서 네임스페이스 우선 순위에 대해 자세히 알아보십시오.

## 채널 캡핑 규칙 만들기

>[!CONTEXTUALHELP]
>id="ajo_rule_sets_channel"
>title="규칙이 적용되는 채널 정의"
>abstract="하나 이상의 채널을 선택합니다. 상한 설정은 채널에서 총 횟수로 적용됩니다."

채널 규칙 세트를 만들려면 다음 단계를 수행하십시오.

>[!NOTE]
>
>각 채널 도메인 및 여정 도메인에 대해 최대 10개의 활성 로컬 규칙 세트를 만들 수 있습니다.

1. **[!UICONTROL 규칙 집합]** 목록에 액세스한 다음 **[!UICONTROL 규칙 집합 만들기]**&#x200B;를 클릭합니다.

   ![](assets/rule-sets-create-button.png)

1. 최대 가용량 규칙을 추가할 규칙 세트를 선택하거나 새 규칙 세트를 만듭니다.

   * 기존 규칙 세트를 사용하려면 목록에서 선택합니다. 채널 제한 규칙은 &quot;채널&quot; 도메인이 있는 규칙 세트에만 추가할 수 있습니다. **[!UICONTROL 도메인]** 열의 규칙 집합 목록에서 이 정보를 확인할 수 있습니다.

     ![](assets/journey-capping-list.png)

   * 새 규칙 집합 내에 최대 가용량 규칙을 만들려면 **[!UICONTROL 규칙 집합 만들기]**&#x200B;를 클릭하고 규칙 집합에 고유한 이름을 지정한 다음 **[!UICONTROL 규칙 집합 도메인]** 드롭다운에서 &quot;채널&quot;을 선택한 다음 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

     ![](assets/rule-sets-create.png)

1. 규칙 집합 화면에서 **[!UICONTROL 규칙 추가]** 단추를 클릭하고 규칙의 고유한 이름을 정의합니다.

1. **범주** 필드는 규칙이 적용되는 메시지의 범주를 지정합니다. 지금은 **[!UICONTROL 마케팅]** 범주만 사용할 수 있으므로 이 필드는 읽기 전용입니다.

   ![](assets/rule-set-channels.png)

1. **[!UICONTROL 최대 가용량]** 필드에서 다음 필드에서 선택한 내용에 따라 매월, 주, 일 또는 시간에 개별 사용자 프로필로 보낼 수 있는 최대 메시지 수를 의미하는 규칙의 최대 가용량(captivate)을 설정합니다.

1. **[!UICONTROL 캡핑 빈도 재설정]** 드롭다운 목록에서 캡핑을 시간별, 일별, 주별 또는 월별 단위로 적용하려는 경우 선택합니다. 빈도 상한은 선택한 달력 기간을 기반으로 합니다. 해당 시간대의 시작 부분에서 재설정됩니다.

   기간별 사용기간 종료일은 다음 각 호와 같다.

   * **[!UICONTROL 시간별]** - 빈도 상한은 선택한 시간 수에 유효합니다. 카운터는 각 시간 범위의 시작 부분에서 자동으로 재설정됩니다. 1시간 빈도 상한의 경우 UTC 시간이 종료되면 한 시간마다 재설정됩니다.
   * **[!UICONTROL 일별]** - 일별 빈도 상한은 23:59:59 UTC까지 해당 일에 대해 유효하며 다음 날 시작 시 0으로 재설정됩니다.
   * **[!UICONTROL 주별]** - 달력 주가 일요일에 시작되기 때문에 빈도 상한은 해당 주의 토요일 23:59:59 UTC까지 유효합니다. 만료 날짜는 규칙이 만들어진 시기에 관계없이 적용됩니다. 예를 들어, 규칙이 목요일에 만들어지면 이 규칙은 토요일 23:59:59까지 유효합니다.
   * **[!UICONTROL 월별]** - 빈도 상한은 23:59:59 UTC로 해당 월의 마지막 날까지 유효합니다. 예를 들어 1월의 월별 만료일은 01~31 23:59:59 UTC입니다.

   >[!IMPORTANT]
   >
   >* 정확성을 보장하려면 캠페인이나 여정을 작성하는 동안 우선 순위가 가장 높은 네임스페이스를 선택해야 합니다. [플랫폼 ID 서비스 안내서](https://experienceleague.adobe.com/ko/docs/experience-platform/identity/features/identity-graph-linking-rules/namespace-priority){target="_blank"}<br/>에서 네임스페이스 우선 순위에 대해 자세히 알아보십시오.
   >
   >* 프로필 카운터 값은 통신이 전달되면 업데이트됩니다. 대량의 통신을 전송하는 경우 처리량으로 인해 수신자는 통신을 시작한 후 몇 분 또는 몇 시간 만에 이메일을 받을 수 있으므로(수백만 개의 통신을 동시에 전송하는 경우) 이 사실을 알고 있어야 합니다. 이는 수신자가 두 개의 커뮤니케이션을 밀접하게 함께 받는 경우에 중요합니다. 수신자가 통신을 수신할 충분한 시간을 주고 그에 따라 카운터 값을 업데이트할 수 있는 경우, 최소 2시간 간격으로 통신을 구분하는 것이 좋습니다.

1. **[!UICONTROL Every]** 필드를 사용하면 지정된 기간에 따라 여러 시간, 일, 주 또는 개월 동안 빈도 제한 규칙을 반복할 수 있습니다. 예: 빈도 제한 규칙을 2주 동안 적용합니다.

   선택한 기간 유형과 일치하는 값을 입력해야 합니다. 시간별 1-23, 일별 1-30, 주별 1-4, 월별 1-3.

   새 시간 범위가 시작되면 카운터가 자동으로 0으로 재설정됩니다. 2일 빈도 상한의 경우 이 재설정은 2일마다 자정(UTC)에 발생합니다.

1. 이 규칙에 사용할 채널을 선택하십시오. **[!UICONTROL 전자 메일]**, **[!UICONTROL SMS]**, **[!UICONTROL 푸시 알림]** 또는 **[!UICONTROL DM]**.

1. 선택한 모든 채널에 캡핑을 총 카운트로 적용하려면 여러 채널을 선택하십시오.

   예를 들어 최대 가용량 을 5로 설정하고 이메일 채널과 sms 채널을 모두 선택합니다. 프로필이 선택한 기간 동안 이미 3개의 마케팅 이메일과 2개의 마케팅 SMS를 받은 경우, 이 프로필은 다음 마케팅 이메일 또는 SMS 게재에서 제외됩니다.

1. **[!UICONTROL 저장]**&#x200B;을 클릭하여 규칙 만들기를 확인합니다. 메시지가 **[!UICONTROL 초안]** 상태로 규칙 집합에 추가됩니다.

   ![](assets/rule-set-rule-created.png)

1. 위의 단계를 반복하여 규칙 세트에 필요한 만큼 규칙을 추가합니다.

1. 최대 가용량 규칙을 메시지에 적용할 준비가 되면 규칙 세트와 해당 규칙이 추가된 규칙을 활성화합니다. [규칙 집합을 활성화하는 방법 알아보기](../conflict-prioritization/rule-sets.md#create)

## 메시지에 규칙 세트 적용 {#apply-frequency-rule}

메시지에 규칙 세트를 적용하려면 다음 단계를 수행합니다.

1. 여정 또는 캠페인 메시지를 만들 때 규칙 세트에 대해 정의한 채널 중 하나를 선택하고 메시지 콘텐츠를 편집합니다

1. 콘텐츠 편집 화면에서 **[!UICONTROL 비즈니스 규칙 추가]** 단추를 클릭합니다.

1. 생성한 규칙 세트를 선택합니다.

   ![](assets/rule-set-campaign-add-rule-button.png)

   >[!NOTE]
   >
   >[활성화됨](#activate-rule) 규칙 집합만 목록에 표시됩니다.

   <!--Messages where the category selected is **[!UICONTROL Transactional]** will not be evaluated against business rules.-->

1. 여정 또는 캠페인을 활성화하기 전에 적어도 10분 후에 실행 일정을 예약하십시오.

   이렇게 하면 선택한 비즈니스 규칙에 대한 프로필의 카운터 값을 채울 수 있습니다. 캠페인을 즉시 활성화하면 규칙 세트 카운터 값이 수신자의 프로필에 채워지지 않고 메시지가 사용자 지정 규칙 세트의 빈도 제한 규칙에 계산되지 않습니다. 또한 즉시 활성화된 여정 및 캠페인과 API 트리거 캠페인에 대해 상한이 올바르게 작동하지 않을 수 있습니다.

   ![](assets/rule-set-schedule-campaign.png)

1. [Customer Journey Analytics 보고서](../reports/report-gs-cja.md)와 [실시간 보고서](../reports/live-report.md)에서 배달에서 제외된 프로필 수를 볼 수 있습니다. 여기서 사용자가 배달에서 제외되는 가능한 이유로 빈도 규칙이 나열됩니다.

>[!NOTE]
>
>동일한 채널에 여러 규칙을 적용할 수 있지만 하위 상한에 도달하면 프로필이 다음 게재에서 제외됩니다.

빈도 규칙을 테스트할 때는 새로 만든 [테스트 프로필](../audience/creating-test-profiles.md)을 사용하는 것이 좋습니다. 프로필의 빈도 상한에 도달하면 다음 기간까지 카운터를 재설정할 방법이 없기 때문입니다. 규칙을 비활성화하면 캡핑된 프로필에서 메시지를 받을 수 있지만 카운터 증분은 제거되거나 삭제되지 않습니다.

<!--add a new section for default priority namespace.-->

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

## 사용 방법 비디오 {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3444733?quality=12&captions=kor)
