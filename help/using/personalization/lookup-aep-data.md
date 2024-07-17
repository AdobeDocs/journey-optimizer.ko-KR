---
solution: Journey Optimizer
product: journey optimizer
title: 개인화에 Adobe Experience Platform 데이터 사용(베타)
description: 개인화에 Adobe Experience Platform 데이터를 사용하는 방법을 알아봅니다.
feature: Personalization, Rules
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: 표현식, 편집기
hidefromtoc: true
hide: true
exl-id: 2fc10fdd-ca9e-46f0-94ed-2d7ea4de5baf
source-git-commit: a03541b5f1d9c799c30bf1d38b6f187d94c21dff
workflow-type: tm+mt
source-wordcount: '537'
ht-degree: 0%

---

# 개인화에 Adobe Experience Platform 데이터 사용(베타) {#aep-data}

>[!AVAILABILITY]
>
>이 기능은 현재 비공개 베타로만 사용할 수 있습니다.
>
>지금은 **이메일 채널**&#x200B;에 대해서만 사용할 수 있으며 Adobe에 제공한 비프로덕션 샌드박스와 Beta에 대해 요청된 데이터 세트에 대해서만 테스트용입니다.

Journey Optimizer을 사용하면 개인화 편집기에서 Adobe Experience Platform의 데이터를 활용하여 [콘텐츠를 개인 맞춤화](../personalization/personalize.md)할 수 있습니다. 단계는 다음과 같습니다.

1. 메시지와 같은 개인화를 정의할 수 있는 모든 컨텍스트에서 사용할 수 있는 개인화 편집기를 엽니다. [개인화 편집기로 작업하는 방법을 알아보세요](../personalization/personalization-build-expressions.md)

1. 도우미 함수 목록으로 이동하여 **datasetLookup** 도우미 함수를 코드 창에 추가합니다.

   ![](assets/aep-data-helper.png)

1. 이 함수는 Adobe Experience Platform 데이터 세트에서 필드를 호출할 수 있는 사전 정의된 구문을 제공합니다. 구문은 다음과 같습니다.

   ```
   {{entity.datasetId="datasetId" id="key" result="store"}}
   ```

   * **entity.datasetId**&#x200B;은(는) 작업 중인 데이터 세트의 ID입니다.
   * **id**&#x200B;은(는) 조회 데이터 세트의 기본 ID와 연결해야 하는 원본 열의 ID입니다.

     >[!NOTE]
     >
     >이 필드에 입력한 값은 필드 ID(*profile.couponValue*), 여정 여정 이벤트에서 전달된 필드(*context.profile.events.event_ID.couponValue*) 또는 정적 값(*couponAbcd*)일 수 있습니다. 어떤 경우든 시스템은 값을 사용하고 데이터 세트를 조회하여 키가 일치하는지 확인합니다.

   * **result**&#x200B;은(는) 데이터 집합에서 검색할 모든 필드 값을 참조하기 위해 제공해야 하는 임의의 이름입니다. 이 값은 코드에서 각 필드를 호출하는 데 사용됩니다.

   +++데이터 세트 ID를 검색할 위치

   데이터 세트 ID는 Adobe Experience Platform 사용자 인터페이스에서 검색할 수 있습니다. [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/user-guide#view-datasets){target="_blank"}에서 데이터 세트로 작업하는 방법을 알아보세요.

   ![](assets/aep-data-dataset.png)

+++

1. 필요에 맞게 구문을 조정하십시오. 이 예제에서는 승객의 비행과 관련된 데이터를 검색하려고 합니다. 구문은 다음과 같습니다.

   ```
   {{entity.datasetId="1234567890abcdtId" id=profile.upcomingFlightId result="flight"}}
   ```

   * ID가 &quot;abcdtId&quot;인 데이터 세트에서 작업 1234567890,
   * 조회 데이터 세트에 가입하는 데 사용할 필드는 *profile.uncomingFlightId*&#x200B;입니다.
   * &quot;플라이트&quot; 참조 아래에 모든 필드 값을 포함하려고 합니다.

1. Adobe Experience Platform 데이터 세트에서 호출할 구문이 구성되면 검색할 필드를 지정할 수 있습니다. 구문은 다음과 같습니다.

   ```
   {{result.fieldId}}
   ```

   * **result**&#x200B;은(는) **MultiEntity** 도우미 함수에서 **result** 매개 변수에 할당한 값입니다. 이 예에서는 &quot;플라이트&quot;입니다.
   * **fieldID**&#x200B;은(는) 검색할 필드의 ID입니다. 이 ID는 데이터 세트를 검색할 때 Adobe Experience Platform 사용자 인터페이스에 표시됩니다. 아래 섹션을 확장하여 예를 표시합니다.

     +++필드 ID를 검색하는 위치

     Adobe Experience Platform 사용자 인터페이스에서 데이터 세트를 미리 볼 때 필드 ID를 검색할 수 있습니다. [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/user-guide#preview){target="_blank"}에서 데이터 세트를 미리 보는 방법에 대해 알아보세요.

     ![](assets/aep-data-field.png)

+++

   이 예제에서는 승객의 탑승 시간 및 탑승구와 관련된 정보를 사용하려고 합니다. 따라서 다음 두 행을 추가합니다.

   * `{{flight._myorg.booking.boardingTime}}`
   * `{{flight._myorg.booking.gate}}`

1. 이제 코드가 준비되었으므로 평소와 같이 콘텐츠를 완료하고 **콘텐츠 시뮬레이션** 단추를 사용하여 테스트하여 개인화를 확인할 수 있습니다. [콘텐츠를 미리 보고 테스트하는 방법에 대해 알아보세요](../content-management/preview-test.md)


   ![](assets/aep-data-sample.png)
