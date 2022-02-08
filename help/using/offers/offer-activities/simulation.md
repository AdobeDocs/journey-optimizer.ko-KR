---
title: 시뮬레이션 만들기
description: 의사결정 로직의 유효성을 확인하기 위해 주어진 배치에 대해 전달되는 오퍼를 시뮬레이션하는 방법을 알아봅니다
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: da9e898b-8e5d-43da-9226-5c9ccb78e174
source-git-commit: 60ccb9b918284b3fcb62101bc94bf64d2272e8e2
workflow-type: tm+mt
source-wordcount: '739'
ht-degree: 1%

---

# 시뮬레이션 만들기 {#create-simulations}

## 시뮬레이션 기본 정보 {#about-simulation}

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

## 테스트 프로필 선택 {#select-test-profiles}

먼저 시뮬레이션에 사용할 테스트 프로필을 선택해야 합니다.

1. **[!UICONTROL Manage profile]**&#x200B;을(를) 클릭합니다.

   ![](../../assets/offers_simulation-manage-profile.png)

1. 테스트 프로필을 식별하는 데 사용할 ID 네임스페이스를 선택합니다. 이 예제에서는 **이메일** 네임스페이스.

   >[!NOTE]
   >
   >ID 네임스페이스는 이메일 주소 또는 CRM ID와 같은 식별자의 컨텍스트를 정의합니다. Adobe Experience Platform ID 네임스페이스에 대해 자세히 알아보십시오 [이 섹션](../../start/get-started-identity.md){target=&quot;_blank&quot;}.

1. ID 값을 입력하고 를 클릭합니다. **[!UICONTROL View]** 사용 가능한 프로필을 나열하려면 다음을 수행하십시오.

   ![](../../assets/offers_simulation-add-profile.png)

1. 다른 프로필 데이터를 테스트하려는 경우 다른 프로필을 추가하고 선택 항목을 저장합니다.

   ![](../../assets/offers_simulation-save-profiles.png)

1. 추가한 모든 프로필은 아래의 드롭다운 목록에 나열됩니다 **[!UICONTROL Test profile]**. 저장된 테스트 프로필 간을 전환하여 선택한 각 프로필에 대한 결과를 표시할 수 있습니다.

   ![](../../assets/offers_simulation-saved-profiles.png)

   >[!NOTE]
   >
   >선택한 프로필은 **[!UICONTROL Simulation]** 탭에서 를 사용하여 제거할 때까지 세션에서 세션으로 이동합니다. **[!UICONTROL Manage profile]**.

1. 을(를) 클릭합니다. **[!UICONTROL Profile details]** 링크를 클릭하여 선택한 프로필 데이터를 표시합니다.

<!--Learn more on [selecting test profiles](messages/preview.md#select-test-profiles)-->

## 결정 범위 추가 {#add-decision-scopes}

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

## 시뮬레이션 설정 정의 {#define-simulation-settings}

시뮬레이션에 대한 기본 설정을 편집하려면 아래 단계를 따르십시오.

1. **[!UICONTROL Settings]**&#x200B;을(를) 클릭합니다.

   ![](../../assets/offers_simulation-settings.png)

1. 에서 **[!UICONTROL Deduplication]** 섹션에서 결정 및/또는 배치 간에 중복 오퍼를 허용하도록 선택할 수 있습니다. 즉, 여러 결정/배치에서 동일한 오퍼를 할당할 수 있습니다.

   ![](../../assets/offers_simulation-settings-deduplication.png)

   >[!NOTE]
   >
   >기본적으로 모든 중복 제거 플래그가 시뮬레이션에 사용됩니다. 이는 의사 결정 엔진이 중복을 허용하므로 여러 의사 결정/배치 간에 동일한 제안을 만들 수 있음을 의미합니다. 추가 정보 [!DNL Decisions] 의 API 요청 속성 [이 섹션](../api-reference/decisions-api/deliver-offers.md).

1. 에서 **[!UICONTROL Response format]** 섹션에서 코드 보기에 메타데이터를 포함하도록 선택할 수 있습니다. 해당 옵션을 선택하고 선택한 메타데이터를 선택합니다. 선택 시 요청 및 응답 페이로드에 표시됩니다 **[!UICONTROL View code]**. 자세한 내용은 [시뮬레이션 결과 보기](#simulation-results) 섹션을 참조하십시오.

   ![](../../assets/offers_simulation-settings-response-format.png)

   >[!NOTE]
   >
   >옵션을 켜면 기본적으로 모든 항목이 선택됩니다.

1. **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

>[!NOTE]
>
>현재 시뮬레이션 데이터의 경우 **[!UICONTROL Hub]** API.

<!--
In the **[!UICONTROL API for simulation]** section, select the API you want to use: **[!UICONTROL Hub]** or **[!UICONTROL Edge]**.
Hub and Edge are two different end points for simulation data.

In the **[!UICONTROL Context data]** section, you can add as many elements as needed.

    >[!NOTE]
    >
    >This section is hidden if you select Edge API in the section above. Hub allows the use of Context data, Edge does not.

Context data allows the user to add contextual data that could affect the simulation score.
For instance, let's say the customer has an offer for a discount on ice cream. In the rules for that offer, it can have logic that would rank it higher when the temperature is above 80 degrees. In simulation, the user could add context data: temperature=65 and that offer would rank lower, of they could add temperature=95 and that would rank higher.
-->

## 시뮬레이션 결과 보기 {#simulation-results}

결정 범위를 추가하고 테스트 프로필을 선택하면 결과를 볼 수 있습니다.

1. **[!UICONTROL View results]**&#x200B;을(를) 클릭합니다.

   ![](../../assets/offers_simulation-view-results.png)

1. 사용 가능한 최상의 오퍼는 각 결정에 대해 선택한 프로필에 따라 표시됩니다.

   세부 사항을 표시할 오퍼를 선택합니다.

   ![](../../assets/offers_simulation-offer-details.png)

1. 클릭 **[!UICONTROL View code]** 요청 및 응답 페이로드를 표시합니다. [자세히 알아보기](#view-code)

1. 목록에서 다른 프로필을 선택하여 다른 테스트 프로필에 대한 오퍼 결정 결과를 표시합니다.

1. 필요한 만큼 결정 범위를 추가, 제거 또는 업데이트할 수 있습니다.

>[!NOTE]
>
>프로필을 변경하거나 결정 범위를 업데이트할 때마다 **[!UICONTROL View results]** 버튼을 클릭합니다.

## 코드 보기 {#view-code}

1. 를 사용하십시오 **[!UICONTROL View code]** 버튼을 클릭하여 요청 및 응답 페이로드를 표시합니다.

   ![](../../assets/offers_simulation-view-code.png)

   코드 보기에는 현재 사용자에 대한 개발자 정보가 표시됩니다. 기본적으로 **[!UICONTROL Response payload]** 이 표시됩니다.

   ![](../../assets/offers_simulation-request-payload.png)

1. 클릭 **[!UICONTROL Response payload]** 또는 **[!UICONTROL Request payload]** 두 탭 간을 탐색하려면

   ![](../../assets/offers_simulation-response-payload.png)

1. 요청 페이로드를 [!DNL Journey Optimizer] - 예를 들어 문제 해결 목적으로 다음을 사용하여 복사합니다. **[!UICONTROL Copy to clipboard]** 코드 보기의 맨 위에 있는 단추입니다.

   ![](../../assets/offers_simulation-copy-payload.png)

   <!--You cannot copy the response payload. ACTUALLY YES YOU CAN > to confirm with PM/dev? -->

   >[!NOTE]
   >
   >요청이나 응답 페이로드를 자신의 코드에 복사할 때는 {USER_TOKEN} 및 {API_KEY}을 올바른 값으로 바꾸십시오. 에서 이러한 값을 검색하는 방법을 알아봅니다 [Adobe Experience Platform API](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html){target=&quot;_blank&quot;} 설명서입니다.

