---
title: 시뮬레이션 만들기
description: 시뮬레이션을 만드는 방법 알아보기
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: da9e898b-8e5d-43da-9226-5c9ccb78e174
source-git-commit: 39b52f39ec19c185d2cd95634a60e37f62a66f83
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 1%

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
   >기본적으로 모든 중복 제거 플래그가 시뮬레이션에 사용됩니다. 이는 의사 결정 엔진이 중복을 허용하므로 여러 의사 결정/배치 간에 동일한 제안을 만들 수 있음을 의미합니다. 추가 정보 [!DNL Decisions] 의 API 요청 속성 [이 섹션](../api-reference/decisions-api/deliver-offers.md).<!--Deduplication note TO REMOVE WHEN SIMULATIONS V2 is on PROD-->

<!--SIMULATIONS V2

## Define simulation settings {#define-simulation-settings}

To edit the default settings for your simulations, follow the steps below.

1. Click **[!UICONTROL Settings]**.

    ![](../../assets/offers_simulation-settings.png)

1. In the **[!UICONTROL Deduplication]** section, you can choose to allow duplicate offers accross decisions and/or placements. It means that multiple decisions/placements may get assigned the same offer.

    ![](../../assets/offers_simulation-settings-deduplication.png)

    >[!NOTE]
    >
    >By default, all Deduplication flags are enabled for simulation, which means that the decision engine allows duplicates and thus can make the same proposition accross multiple decisions/placements. Learn more on the [!DNL Decisions] API request properties in [this section](../api-reference/decisions-api/deliver-offers.md).

1. In the **[!UICONTROL Response format]** section, you can choose to include metadata in the code view. Check the corresponding option, and select the metadata of your choice. They will be displayed in the request and response payloads when selecting **[!UICONTROL View code]**. Learn more in the [View simulation results](#simulation-results) section.

    ![](../../assets/offers_simulation-settings-response-format.png)

    >[!NOTE]
    >
    >When turning on the option, all items are selected by default.

1. Click **[!UICONTROL Save]**.-->

<!--NOT FOR SIMULATIONS V2

In the **[!UICONTROL API for simulation]** section, select the API you want to use: **[!UICONTROL Hub]** or **[!UICONTROL Edge]**.
Hub and Edge are two different end points for simulation data.

In the **[!UICONTROL Context data]** section, you can add as many elements as needed.

    >[!NOTE]
    >
    >This section is hidden if you select Edge API in the section above. Hub allows the use of Context Data, Edge does not.

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

   <!--
    SIMULATIONS V2
    1. Click **[!UICONTROL View code]** to display the request and response payloads. [Learn more](#view-code)-->

1. 목록에서 다른 프로필을 선택하여 다른 테스트 프로필에 대한 오퍼 결정 결과를 표시합니다.

1. 필요한 만큼 결정 범위를 추가, 제거 또는 업데이트할 수 있습니다.

>[!NOTE]
>
>프로필을 변경하거나 결정 범위를 업데이트할 때마다 **[!UICONTROL View results]** 버튼을 클릭합니다.

<!--
SIMULATIONS V2

## View code {#view-code}

To use the request payload outside of [!DNL Journey Optimizer] - for troubleshooting purpose for example, you can copy it by clicking the corresponding button on top of the code view.
    
>[!NOTE]
>
>You cannot copy the response payload.

Below is an example of code view:

    ```
    curl -X POST \
    'https://platform.adobe.io/data/core/ode/{CONTAINER_ID}/decisions' \
    -H 'Accept: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"' \
    -H 'Content-Type: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0"' \
    -H 'Authorization: Bearer eyJhbGciOiJSUzI1NiIsIng1dSI6Imltc19uYTEtc3RnMS1rZXktMS5jZXIifQ.eyJpZCI6IjE2NDMxMzg3NDMxODlfOTIzY2ZjZjgtOWVkYy00MjE1LWJjODgtYmEyYTY2ZGIyYmMyX3VlMSIsInR5cGUiOiJhY2Nlc3NfdG9rZW4iLCJjbGllbnRfaWQiOiJhY3BfdWlfcGxhdGZvcm0iLCJ1c2VyX2lkIjoiNDhENTc0N0E2MDc3NkRERTBBNDk0MDFEQEFkb2JlSUQiLCJzdGF0ZSI6IntcInNlc3Npb25cIjpcImh0dHBzOi8vaW1zLW5hMS1zdGcxLmFkb2JlbG9naW4uY29tL2ltcy9zZXNzaW9uL3YxL1l6azNNakE0TXpNdFpXVTVaUzAwTVdOaExUZ3pNamd0TmpFM1pqZ3lOak5qTmpSakxTMDBPRVExTnpRM1FUWXdOemMyUkVSRk1FRTBPVFF3TVVSQVFXUnZZbVZKUkFcIn0iLCJhcyI6Imltcy1uYTEtc3RnMSIsImFhX2lkIjoiNDhENTc0N0E2MDc3NkRERTBBNDk0MDFEQEFkb2JlSUQiLCJjdHAiOjAsImZnIjoiV0VQQTNUSUY0UjRaQTZEWlBDUk1BMklBQ1U9PT09PT0iLCJzaWQiOiIxNjQzMDYwMDg0NzI2XzYzNGJkNDEzLWMwYTktNDA0NS1iNTM3LWRmMzgzYzU5ZGIxY191ZTEiLCJydGlkIjoiMTY0MzEzODc0MzE4OV9lYWMxOWY5Yi00ZjhhLTQ1NWMtOWVmMi1mNjYwNmQ0ODY4N2ZfdWUxIiwibW9pIjoiYmVjOTQzYzIiLCJwYmEiOiIiLCJvYyI6InJlbmdhKm5hMXItc3RnMSoxN2U5MmIzNzYzNCo2MEJEVjBGUlhOMFlRMkdHSkRON0E5Tk1HOCIsInJ0ZWEiOiIxNjQ0MzQ4MzQzMTg5IiwiZXhwaXJlc19pbiI6Ijg2NDAwMDAwIiwic2NvcGUiOiJvcGVuaWQsc2Vzc2lvbixyZWFkX29yZ2FuaXphdGlvbnMsYWRkaXRpb25hbF9pbmZvLnByb2plY3RlZFByb2R1Y3RDb250ZXh0LGFkZGl0aW9uYWxfaW5mby5yb2xlcyxhdWRpZW5jZW1hbmFnZXJfYXBpLEFkb2JlSUQiLCJjcmVhdGVkX2F0IjoiMTY0MzEzODc0MzE4OSJ9.TgZ998KHA4Zeoyq7b_NbPv8aPHb2cs9GgP3uJKrTbzosylKKRYqLpj_8HkloI-bFVQFCBCOWbCwtJtkcRIvFlQFruTr5bpMatPV8izEUVutO6smkYBFoGFYyEGuN5Xe97uOJZEHzFSWguGZtgttSrNhXr-j0hFloofjXDJXPB_911dzXALp5s15sd3HLH9XWTwwlqF_a5SMNDXaSj1800RxsB9bJ8_YL0x4pqQwjYJxRGMhiy7Y9IOpwogSBEiqCQitlKYgaO7yaJzFwhfyisnqM7_MWX2ETn-kGFEOoBHxXDTx9P2OPojzb8ChWQgmGf7Expyvtc1ke3nJkppzrxg' \
    -H 'x-api-key: {API_KEY}' \
    -H 'x-gw-ims-org-id: 5D1328435BF324E90A49402A@AdobeOrg' \
    -H 'x-sandbox-name: prod' \
    -D '{
      "xdm:propositionRequests": [
            {
                  "xdm:placementId": "xcore:offer-placement:1416f4109d9d292c",
                  "xdm:activityId": "xcore:offer-activity:1416f4aad9fd99d7",
                  "xdm:itemCount": 2
            }
      ],
      "xdm:profiles": [
            {
                  "xdm:identityMap": {
                        "email": [
                              {
                                    "xdm:id": "poyfair@adobe.com"
                              }
                        ]
                  }
            }
      ],
      "xdm:allowDuplicatePropositions": {
            "xdm:acrossActivities": true,
            "xdm:acrossPlacements": true
      },
      "xdm:responseFormat": {
            "xdm:includeMetadata": {
                  "xdm:activity": [],
                  "xdm:option": [],
                  "xdm:placement": []
            }
      }
    }'
    ```

>[!NOTE]
>
>When copying the request payload into your own code, make sure you replace CONTAINER_ID and API_KEY with your own values.-->

