---
title: 시뮬레이션 만들기
description: 시뮬레이션을 만드는 방법 알아보기
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: null
source-git-commit: bad206b6c9b48241dbbd7758a331d602fac466b4
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 0%

---


# 시뮬레이션 만들기

## 시뮬레이션 기본 정보

의사 결정 로직의 유효성을 검사하기 위해 주어진 배치에 대한 테스트 프로필에 전달되는 오퍼를 시뮬레이션할 수 있습니다.

<!--Simulation allows you to view the results of offer decisions as a selected profile.-->

이렇게 하면 타깃팅된 수신자에게 영향을 주지 않고 다양한 버전의 오퍼를 테스트하고 세분화할 수 있습니다.

>[!NOTE]
>
>이 기능은 [!DNL Decisions] API. 추가 정보 [결정 API를 사용하여 오퍼 제공](../api-reference/decisions-api/deliver-offers.md).

이 기능에 액세스하려면 **[!UICONTROL Simulation]** 탭에서 **[!UICONTROL Decision management]** > **[!UICONTROL Offers]** 메뉴 아래의 제품에서 사용할 수 있습니다.

![](../../assets/offers_simulation-tab.png)

<!--
➡️ [Discover this feature in video](#video)
-->

## 테스트 프로필 선택

먼저 시뮬레이션에 사용할 테스트 프로필을 선택해야 합니다.

1. **[!UICONTROL Manage profile]**&#x200B;을(를) 클릭합니다.

   ![](../../assets/offers_simulation-manage-profile.png)

1. 테스트 프로필을 식별하는 데 사용할 ID 네임스페이스를 선택합니다. 이 예제에서는 **이메일** 네임스페이스.

   >[!NOTE]
   >
   >ID 네임스페이스는 이메일 주소 또는 CRM ID와 같은 식별자의 컨텍스트를 정의합니다. Adobe Experience Platform ID 네임스페이스에 대해 자세히 알아보십시오 [이 섹션](../../get-started-identity.md){target=&quot;_blank&quot;}.

1. ID 값을 입력하고 를 클릭합니다. **[!UICONTROL View]** 사용 가능한 프로필을 나열하려면 다음을 수행하십시오.

   ![](../../assets/offers_simulation-add-profile.png)

1. 다른 프로필 데이터를 테스트하려는 경우 다른 프로필을 추가하고 선택 항목을 저장합니다.

   ![](../../assets/offers_simulation-save-profiles.png)

1. 추가한 모든 프로필은 아래의 드롭다운 목록에 나열됩니다 **[!UICONTROL Test profile]**. 저장된 테스트 프로필 간을 전환하여 선택한 각 프로필에 대한 결과를 표시할 수 있습니다.

   ![](../../assets/offers_simulation-saved-profiles.png)

1. 을(를) 클릭합니다. **[!UICONTROL Profile details]** 링크를 클릭하여 선택한 프로필 데이터를 표시합니다.

<!--Learn more on [selecting test profiles](preview.md#select-test-profiles)-->

## 결정 범위 추가

이제 테스트 프로필에서 시뮬레이션할 오퍼 결정을 선택합니다.

1. **[!UICONTROL Add decision scope]**&#x200B;를 선택합니다.

   ![](../../assets/offers_simulation-add-decision.png)

1. 목록에서 배치를 선택합니다.

   ![](../../assets/offers_simulation-add-decision-scope.png)

1. 사용 가능한 결정이 표시됩니다.

   * 검색 필드를 사용하여 선택 사항을 구체화할 수 있습니다.
   * 을(를) 클릭합니다. **[!UICONTROL Open offer decisions]** 링크를 클릭하여 작성한 모든 결정 목록을 엽니다. 추가 정보 [결정](create-offer-activities.md).

   원하는 결정을 선택하고 을(를) 클릭합니다 **[!UICONTROL Add]**.

   ![](../../assets/offers_simulation-add-decision-scope-add.png)

1. 방금 정의한 결정 범위가 기본 작업 공간에 표시됩니다.

   요청하려는 오퍼 수를 조정할 수 있습니다. 예를 들어 2를 선택하면 이 결정 범위에 대해 가장 적합한 2개의 오퍼가 표시됩니다.

   ![](../../assets/offers_simulation-request-offer.png)

   >[!NOTE]
   >
   >최대 30개의 오퍼를 요청할 수 있습니다.

1. 위의 단계를 반복하여 필요한 만큼 결정을 추가합니다.

   ![](../../assets/offers_simulation-add-more-decisions.png)

   >[!NOTE]
   >
   >여러 결정 범위를 정의하더라도 하나의 API 요청만 시뮬레이션됩니다.
   >
   >모든 중복 제거 플래그는 시뮬레이션에 기본적으로 활성화되어 있습니다. 즉, 의사 결정 엔진이 중복을 허용하므로 여러 의사 결정 시 동일한 제안을 할 수 있습니다. 추가 정보 [!DNL Decisions] 의 API 요청 속성 [이 섹션](../api-reference/decisions-api/deliver-offers.md).

## 시뮬레이션 결과 보기

결정 범위를 추가하고 테스트 프로필을 선택하면 결과를 볼 수 있습니다.

1. **[!UICONTROL View results]**&#x200B;을(를) 클릭합니다.

   ![](../../assets/offers_simulation-view-results.png)

1. 사용 가능한 최상의 오퍼는 각 결정에 대해 선택한 프로필에 따라 표시됩니다.

   세부 사항을 표시할 오퍼를 선택합니다.

   ![](../../assets/offers_simulation-offer-details.png)

1. 목록에서 다른 프로필을 선택하여 다른 테스트 프로필에 대한 오퍼 결정 결과를 표시합니다.

1. 필요한 만큼 결정 범위를 추가, 제거 또는 업데이트할 수 있습니다.

>[!NOTE]
>
>프로필을 변경하거나 결정 범위를 업데이트할 때마다 **[!UICONTROL View results]** 버튼을 클릭합니다.

<!--Questions

* Is it recommended to first select profiles or first add decision scopes?
* What does Request offer changes?
* Nothing displays when I click View results? Can't see any score...
* What's the typical example? i.e. how many decisions do you select, and how do you compare scores?
* What do you learn from simulation? i.e. if I selected 2 decisions and I compare the scores, which one is better or should I use for my customers?
* Is there a way to create relevant test profiles?
* Error on Profile details link.
* Is there a tutorial planned to be released?
* Why still a big red frame when no profile is found?

## Tutorial video {#video}

>[!NOTE]
>
>This video applies to the Offer Decisioning application service built on Adobe Experience Platform. However, it provides generic guidance to use Offer in the context of Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329606?quality=12)
-->