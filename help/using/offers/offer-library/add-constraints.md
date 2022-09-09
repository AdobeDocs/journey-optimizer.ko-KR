---
title: 오퍼에 제한 추가
description: 오퍼를 표시할 조건을 정의하는 방법을 알아봅니다
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 7234a8e8-4ab0-4f17-a833-5e452fadac35
source-git-commit: e9aab8f3e686a6858e401101f751a35933a21c0a
workflow-type: tm+mt
source-wordcount: '1772'
ht-degree: 2%

---

# 오퍼에 제한 추가 {#add-constraints}

>[!CONTEXTUALHELP]
>id="od_offer_constraints"
>title="오퍼 제한 기본 정보"
>abstract="제한 조건을 사용하여 오퍼의 우선 순위가 지정되고 다른 오퍼와 비교하여 사용자에게 표시되는 방법을 지정할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_constraints"
>title="오퍼 제한 기본 정보"
>abstract="제한 조건을 사용하여 오퍼의 우선 순위가 지정되고 다른 오퍼와 비교하여 사용자에게 표시되는 방법을 지정할 수 있습니다."

>[!CONTEXTUALHELP]
>id="od_offer_priority"
>title="오퍼 우선 순위 정보"
>abstract="이 필드에서 오퍼에 대한 우선순위 설정을 지정할 수 있습니다. 우선 순위는 자격, 날짜 및 최대 가용량과 같은 모든 제한 사항을 충족하는 오퍼의 등급을 매기는 데 사용되는 숫자입니다."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_priority"
>title="우선 순위 설정"
>abstract="우선 순위는 사용자가 두 개 이상의 오퍼를 자격이 있는 경우 다른 오퍼와 비교하여 오퍼의 우선순위를 정의하는 데 도움이 됩니다. 오퍼의 우선 순위가 높을수록 오퍼의 우선 순위가 더 높습니다."

제한 조건을 사용하면 오퍼가 표시될 조건을 정의할 수 있습니다.

1. 구성 **[!UICONTROL Offer eligibility]**. [자세히 보기](#eligibility)

   ![](../assets/offer-eligibility.png)

1. 을(를) 정의합니다 **[!UICONTROL Priority]** 두 개 이상의 오퍼에 대해 사용자가 자격이 있는 경우 다른 오퍼와 비교한 것입니다. 오퍼의 우선 순위가 높을수록 오퍼의 우선 순위가 더 높습니다.

   ![](../assets/offer-priority.png)

1. 오퍼를 지정합니다 **[!UICONTROL Capping]**: 오퍼가 표시되는 횟수를 의미합니다. [자세히 보기](#capping)

   ![](../assets/offer-capping.png)

1. 클릭 **[!UICONTROL Next]** 정의한 모든 구속을 확인하려면

예를 들어 다음 구속을 설정하는 경우

![](../assets/offer-constraints-example.png)

* 오퍼는 &quot;골드 충성도 고객&quot; 의사 결정 규칙에만 해당하는 사용자에 대해서만 고려됩니다.
* 오퍼의 우선순위는 &quot;50&quot;으로 설정됩니다. 즉, 오퍼는 1과 49 사이의 우선 순위를 가진 오퍼 앞에, 그리고 51 이상의 우선 순위가 있는 오퍼 후에 표시됩니다.
* 오퍼는 모든 배치를 통과하는 사용자당 한 번만 표시됩니다.

## 자격 {#eligibility}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_eligibility"
>title="자격 정의"
>abstract="기본적으로 모든 프로필에는 오퍼를 표시할 수 있지만 세그먼트나 결정 규칙을 사용하여 오퍼를 특정 프로필로 제한할 수 있습니다."

>[!CONTEXTUALHELP]
>id="od_offer_eligibility"
>title="오퍼 자격 기본 정보"
>abstract="이 섹션에서는 결정 규칙을 사용하여 오퍼에 적합한 사용자를 결정할 수 있습니다."
>additional-url="https://video.tv.adobe.com/v/329373" text="데모 비디오 시청"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_total_profile_estimate"
>title="총 프로필 예상"
>abstract="세그먼트나 결정 규칙을 선택하면 예상 자격을 갖춘 프로필에 대한 정보를 볼 수 있습니다."

다음 **[!UICONTROL Offer eligibility]** 섹션에서 세그먼트나 결정 규칙을 사용하여 정의하는 특정 프로필로 오퍼를 제한할 수 있습니다.

>[!NOTE]
>
>사용에 대해 자세히 알아보기 **세그먼트** 비교 **의사 결정 규칙** in [이 섹션](#segments-vs-decision-rules).

* 기본적으로 **[!UICONTROL All visitors]** 옵션이 선택되어 있다면 모든 프로필이 오퍼를 제공할 수 있습니다.

   ![](../assets/offer-eligibility-default.png)

* 오퍼의 프레젠테이션을 하나 또는 여러 명의 구성원으로 제한할 수도 있습니다 [Adobe Experience Platform 세그먼트](../../segment/about-segments.md).

   이렇게 하려면 를 활성화합니다 **[!UICONTROL Visitors who fall into one or multiple segments]** 옵션을 선택한 다음 왼쪽 창에서 한 개 또는 여러 개의 세그먼트를 추가하고 을(를) 사용하여 결합합니다 **[!UICONTROL And]** / **[!UICONTROL Or]** 논리 연산자입니다.

   ![](../assets/offer-eligibility-segment.png)

* 특정 [의사 결정 규칙](../offer-library/creating-decision-rules.md) 오퍼에 대해 **[!UICONTROL By defined decision rule]**&#x200B;을 클릭한 다음 왼쪽 창에서 원하는 규칙을 **[!UICONTROL Decision rule]** 영역.

   ![](../assets/offer_rule.png)

   >[!CAUTION]
   >
   >이벤트 기반 오퍼는에서 현재 지원되지 않습니다 [!DNL Journey Optimizer]. 을 기반으로 의사 결정 규칙을 생성하는 경우 [이벤트](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=en#events){target=&quot;_blank&quot;} 오퍼에서는 활용할 수 없습니다.

세그먼트나 결정 규칙을 선택하면 예상 자격을 갖춘 프로필에 대한 정보를 볼 수 있습니다. 클릭 **[!UICONTROL Refresh]** 를 눌러 데이터를 업데이트합니다.

![](../assets/offer-eligibility-segment-estimate.png)

>[!NOTE]
>
>규칙 매개 변수에 컨텍스트 데이터 등의 프로필에 없는 데이터가 포함된 경우 프로필 예측을 사용할 수 없습니다. 예를 들어 현재 날씨가 ≥80도여야 하는 자격 규칙입니다.

### 세그먼트와 의사 결정 규칙 사용 {#segments-vs-decision-rules}

제한을 적용하려면 하나 또는 여러 오퍼의 구성원으로 오퍼 선택을 제한할 수 있습니다 **Adobe Experience Platform 세그먼트**&#x200B;또는 **의사 결정 규칙**, 두 솔루션은 서로 다른 용도에 해당합니다.

기본적으로 세그먼트의 출력은 프로필 목록이지만, 의사 결정 규칙은 의사 결정 프로세스 동안 단일 프로필에 대해 주문형 실행되는 함수입니다. 그 두 사용법의 차이는 아래에 자세히 나와 있다.

* **세그먼트**

   반면 세그먼트는 프로필 속성 및 경험 이벤트를 기반으로 특정 논리를 일치하는 Adobe Experience Platform 프로필 그룹입니다. 그러나 오퍼 관리 는 세그먼트를 다시 계산하지 않으므로 오퍼를 표시할 때 최신 상태가 아닐 수 있습니다.

   의 세그먼트에 대해 자세히 알아보기 [이 섹션](../../segment/about-segments.md).

* **의사 결정 규칙**

   반면, 의사 결정 규칙은 Adobe Experience Platform에서 사용할 수 있는 데이터를 기반으로 하며 오퍼를 표시할 수 있는 사용자를 결정합니다. 오퍼나 지정된 배치에 대한 결정에서 선택하면, 규칙이 결정될 때마다 실행되어 각 프로필은 최신 오퍼와 최상의 오퍼를 얻을 수 있습니다.

   의 의사 결정 규칙에 대해 자세히 알아보십시오 [이 섹션](creating-decision-rules.md).

## 최대 가용량 {#capping}

>[!CONTEXTUALHELP]
>id="od_offer_globalcap"
>title="오퍼 최대 가용량 기본 정보"
>abstract="이 필드에서 오퍼를 표시할 수 있는 횟수를 지정할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_capping"
>title="최대 가용량 사용"
>abstract="과도한 요청을 방지하려면 최대 제안 횟수를 정의하는 캡핑 을 사용하십시오."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_frequency_capping"
>title="최대 가용량 빈도 설정"
>abstract="오퍼 최대 가용량 카운터를 일별, 주별 또는 월별 기준으로 재설정하도록 선택할 수 있습니다."

최대 가용량은 오퍼를 표시할 수 있는 최대 횟수를 정의하는 제한으로 사용됩니다.

사용자가 특정 오퍼를 얻는 횟수를 제한하면 과도한 요청을 방지하여 최상의 오퍼로 각 터치포인트를 최적화할 수 있습니다.

최대 가용량을 설정하려면 아래 단계를 따르십시오.

1. 오퍼를 표시할 수 있는 횟수를 정의합니다.

   ![](../assets/offer-capping-times.png)

   >[!NOTE]
   >
   >숫자는 0보다 큰 정수여야 합니다.

1. 캡핑을 모든 사용자 간에 적용할지 또는 특정 프로필에 적용할지를 지정합니다.

   ![](../assets/offer-capping-total.png)

   * 선택 **[!UICONTROL In total]** 을(를) 통해 모든 사용자에게 의미하는 결합된 target 대상에서 오퍼를 몇 번 제안할 수 있는지 정의합니다.

      예를 들어 &#39;TV 초버스터 딜&#39;을 보유한 전자 소매업체인 경우 모든 프로필에서 오퍼를 200번만 반환해야 합니다.

   * 선택 **[!UICONTROL Per profile]** 동일한 사용자에게 오퍼를 몇 번 제안할 수 있는지 정의합니다.

      예를 들어 &#39;Platinum Credit&#39; 오퍼가 있는 은행인 경우 이 오퍼가 프로필당 5번 이상 표시되는 것을 원치 않습니다. 실제로, 사용자는 사용자가 오퍼를 5번 보았고 오퍼에 대해 행동하지 않았다면 다음 최상의 오퍼에 대해 행동할 가능성이 더 높다고 믿고 있습니다.

1. 설정 **[!UICONTROL Frequency]** 최대 가용량 카운트가 재설정되는 빈도를 정의합니다. 이렇게 하려면 계산 기간(일별, 주별 또는 월별)을 정의하고 선택한 일/주/개월 수를 입력합니다.

   ![](../assets/offer-capping-frequency.png)

   >[!NOTE]
   >
   >재설정은 정의한 날 또는 해당되는 경우 주/월의 첫 날에 오전 12시 UTC에 수행됩니다. 주 시작일은 일요일입니다.

   예를 들어, 최대 가용량 카운트를 2주마다 재설정하려면 다음을 선택합니다 **[!UICONTROL Weekly]** 에서 **[!UICONTROL Repeat]** 드롭다운 목록 및 유형 **2개** 두 번째 필드에서 참조할 수 있습니다. 재설정은 2주 일요일 오후 12시 UTC에 수행됩니다.

1. 여러 항목을 정의한 경우 [표현](#representations) 오퍼에 대해 최대 가용량 적용 여부를 지정합니다 **[!UICONTROL Across all placements]** 또는 **[!UICONTROL For each placement]**.

   ![](../assets/offer-capping-placement.png)

   * **[!UICONTROL Across all placements]**: 최대 가용량 카운트는 오퍼와 연관된 배치의 모든 결정을 합합니다.

      예를 들어 오퍼에 가 **이메일** 배치 및 **웹** 배치, 캐핑 위치 설정 **모든 배치에서 프로필당 2개**&#x200B;그러면 각 프로필은 배치 혼합에 관계없이 총 2회까지 오퍼를 받을 수 있습니다.

   * **[!UICONTROL For each placement]**: 최대 가용량 카운트는 각 배치에 대해 결정 카운트를 개별적으로 적용합니다.

      예를 들어 오퍼에 가 **이메일** 배치 및 **웹** 배치, 캐핑 위치 설정 **각 배치마다 프로필당 2개**&#x200B;를 지정하는 경우 각 프로필은 이메일 배치에 대해 최대 2회, 웹 배치에 대해서는 2회까지 오퍼를 수신할 수 있습니다.

1. 저장 및 승인되면, 정의한 기준 및 기간에 따라 오퍼가 이 필드에서 지정한 횟수를 제시하면 해당 게재가 중지됩니다.

오퍼를 제안하는 횟수는 이메일 준비 시 계산됩니다. 예를 들어, 많은 수의 오퍼가 포함된 이메일을 준비하는 경우 해당 숫자는 이메일 전송 여부와 관계없이 최대 상한에 포함됩니다.

<!--If an email delivery is deleted or if the preparation is done again before being sent, the capping value for the offer is automatically updated.-->

>[!NOTE]
>
>최대 가용량 카운터는 오퍼가 만료될 때 또는 오퍼 시작 날짜 후 2년(둘 중 먼저 오는 날짜)이 재설정됩니다. 에서 오퍼의 날짜를 정의하는 방법을 알아봅니다. [이 섹션](creating-personalized-offers.md#create-offer).

### 날짜 변경이 최대 가용성에 미치는 영향 {#capping-change-date}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_offer_change_date"
>title="날짜 변경은 최대 가용성에 영향을 줄 수 있습니다"
>abstract="최대 가용량이 이 오퍼에 적용되는 경우, 시작 또는 종료 날짜를 변경할 때 영향을 받을 수 있습니다."

오퍼의 날짜를 변경할 때 다음 조건이 충족되는 경우 캡핑에 영향을 줄 수 있으므로 주의깊게 진행해야 합니다.

* 오퍼는 [승인됨](#review).
* [최대 가용량](#capping) 은 이미 오퍼에 적용됩니다.
* 최대 가용성은 프로필별로 정의됩니다.

>[!NOTE]
>
>에서 오퍼의 날짜를 정의하는 방법을 알아봅니다. [이 섹션](creating-personalized-offers.md#create-offer).

프로필당 최대 가용량 은 각 프로필의 최대 가용량 카운트를 저장합니다. 승인된 오퍼의 시작 및 종료 날짜를 변경할 때 일부 프로필에 대한 최대 가용량 카운트는 아래에 설명된 다른 시나리오에 따라 영향을 받을 수 있습니다.

![](../assets/offer-capping-change-date.png)

다음은 **오퍼 시작 날짜 변경**:

| 시나리오:<br>만약.. | 다음이 발생합니다.<br>그럼.. | 최대 가용성에 미치는 영향 |
|--- |--- |--- |
| ...오퍼의 시작 날짜는 원래 오퍼 시작 날짜가 시작되기 전에 업데이트됩니다. | ... 최대 가용량 카운트는 새 시작 날짜에 시작됩니다. | 아니요 |
| ... 새 시작 날짜가 현재 종료 날짜보다 이전입니다. | ...최대 가용량은 새 시작 날짜로 계속 유지되며 각 프로필에 대한 이전 최대 가용량은 계속 전달됩니다. | 아니요 |
| ... 새 시작 날짜가 현재 종료 날짜 이후입니다. | ...현재 최대 가용량이 만료되고 새 시작 날짜의 모든 프로필에 대해 새 최대 가용량 수가 0부터 다시 시작됩니다. | 예 |

다음은 **오퍼 종료 날짜 확장**:

| 시나리오:<br>만약.. | 다음이 발생합니다.<br>그럼.. | 최대 가용성에 미치는 영향 |
|--- |--- |--- |
| ...최초 오퍼 종료 날짜 이전에 의사 결정 요청이 발생합니다. | ...최대 가용량 카운트가 업데이트되고 각 프로필에 대한 이전 최대 가용량 카운트가 전달됩니다. | 아니요 |
| ... 원래 종료 날짜 이전에 의사 결정 요청이 발생하지 않습니다. | ...각 프로필에 대한 원래 종료 날짜에 최대 가용량 카운트가 재설정됩니다. 그런 다음 원래 종료 날짜 이후에 발생하는 모든 새 의사 결정 요청에 대해 새 최대 가용량 카운트가 0에서 다시 시작됩니다. | 예 |

**예**

원래 시작 날짜가 로 설정된 오퍼가 있다고 가정합니다 **1월 1일**, 만료 **31년 1월**.

1. 프로필 X, Y 및 Z 가 오퍼를 제공합니다.
1. 설정 **10년 1월**&#x200B;로 설정되면 오퍼의 종료 날짜가 **2월 15일**.
1. **1월 11일부터 1월 31일까지**&#x200B;에는 프로필 Z만 오퍼가 표시됩니다.

   * 원래 종료 날짜 이전에 의사 결정 요청이 발생했으므로 **프로필 Z용**&#x200B;로 설정하면 오퍼의 종료 날짜를 **2월 15일**.
   * 하지만 원래 종료 날짜 이전에 활동이 발생하지 않았으므로 **프로필 X 및 Y**&#x200B;로 설정되면 카운터가 만료되고 최대 가용량 카운트가 0으로 재설정됩니다. **31년 1월**.

![](../assets/offer-capping-change-date-ex.png)
