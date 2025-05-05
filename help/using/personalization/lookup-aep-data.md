---
solution: Journey Optimizer
product: journey optimizer
title: 개인화(Beta)에 Adobe Experience Platform 데이터 사용
description: 개인화에 Adobe Experience Platform 데이터를 사용하는 방법을 알아봅니다.
badge: label="Beta" type="Informative"
feature: Personalization, Rules
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: 표현식, 편집기
exl-id: 2fc10fdd-ca9e-46f0-94ed-2d7ea4de5baf
source-git-commit: 47ff62f7dee5974afbffdd38dfe4a3f967781e93
workflow-type: tm+mt
source-wordcount: '1044'
ht-degree: 2%

---

# 개인화에 Adobe Experience Platform 데이터 사용{#aep-data}

>[!AVAILABILITY]
>
>이 기능은 현재 모든 고객이 공개 베타로 사용할 수 있습니다.
>
>이 기능을 사용하려면 먼저 개인화 편집기에서 새 &quot;datasetLookup&quot; 도우미 함수를 추가할 때 표시되는 조직의 Beta 용어를 수락해야 합니다.

Journey Optimizer을 사용하면 개인화 편집기에서 Adobe Experience Platform의 데이터를 활용하여 [콘텐츠를 개인 맞춤화](../personalization/personalize.md)할 수 있습니다. 이렇게 하려면 조회 개인화에 필요한 데이터 세트를 먼저 아래 설명된 대로 API 호출을 통해 활성화해야 합니다. 완료되면 해당 데이터를 사용하여 콘텐츠를 [!DNL Journey Optimizer]&#x200B;(으)로 개인화할 수 있습니다.

## Beta 제한 사항 및 지침 {#guidelines}

시작하기 전에 다음 제한 사항 및 지침을 검토하십시오.

### 데이터 세트 지원 {#enablement}

* **데이터 세트 크기**&#x200B;은(는) 프로덕션 데이터 세트의 경우 5GB, 개발 샌드박스 데이터 세트의 경우 1GB로 제한됩니다
* **조직 당 조회에 대해 최대 50개의 데이터 세트를 사용할 수 있습니다**.
* **레코드 수**&#x200B;은(는) 프로덕션 데이터 세트에서는 5백만 개, 개발 샌드박스 데이터 세트에서는 1백만 개로 제한됩니다.
* **데이터 사용 레이블 지정 및 적용**&#x200B;은 현재 조회를 위해 활성화된 데이터 세트에 대해 적용되지 않습니다.
* **조회를 사용하도록 설정되어 있고 개인화에 사용되는 데이터 세트는 삭제로부터 보호되지 않습니다**. 삭제되거나 제거되지 않도록 개인화에 사용되는 데이터 세트를 추적하는 것은 귀하의 책임입니다.

### [!DNL Adobe Experience Platform] 데이터를 사용하는 Personalization {#perso}

* **지원되는 채널**: 현재 이 기능은 전자 메일, SMS 및 DM 채널 내에서만 사용할 수 있습니다.
* **데이터 사용 레이블 지정 및 적용**&#x200B;은 현재 조회를 위해 활성화된 데이터 세트에 대해 적용되지 않습니다.
* **조각**: 지금은 식 또는 시각적 조각 내에 데이터 집합 조회 개인 설정을 배치할 수 없습니다.

## 데이터 조회를 위해 데이터 세트 활성화 {#enable}

개인화를 위해 데이터 세트의 데이터를 활용하려면 API 호출을 사용하여 상태를 검색하고 조회 서비스를 활성화해야 합니다.

### 전제 조건 {#prerequisites-enable}

* [이 설명서](https://developer.adobe.com/journey-optimizer-apis/references/authentication/)에 설명된 지침에 따라 API 명령을 보내도록 환경을 구성하십시오.
* 개발자 프로젝트에는 Adobe Journey Optimizer 및 Adobe Experience Platform API가 프로젝트에 추가되어 있어야 합니다.

  ![](assets/aep-data-api.png)

* 역할의 일부로 데이터 세트 관리 권한이 있어야 합니다.
* 데이터 집합의 기반이 되는 스키마에는 조회 키로 사용할 수 있는 **기본 ID**&#x200B;이(가) 있어야 합니다.

### API 호출 구조 {#call}

```
curl -s -XPATCH "https://platform.adobe.io/data/core/entity/lookup/dataSets/${DATASET_ID}/${ACTION}" \ -H "Authorization: Bearer ${ACCESS_TOKEN}" \ -H "x-api-key: ${API_KEY}" \ -H "x-gw-ims-org-id: ${IMS_ORG}" \ -H "x-sandbox-name: ${SANDBOX_NAME}"
```

위치:

* **URL**&#x200B;은(는) `https://platform.adobe.io/data/core/entity/lookup/dataSets/${DATASET_ID}/${ACTION}`입니다.
* **데이터 세트 ID**&#x200B;은(는) 활성화하려는 데이터 세트입니다.
* **Action**&#x200B;을(를) 사용하거나 사용하지 않도록 설정합니다.
* 개발자 콘솔에서 **액세스 토큰**&#x200B;을(를) 검색할 수 있습니다.
* **API 키**&#x200B;는 개발자 콘솔에서 검색할 수 있습니다.
* **IMS 조직 ID**&#x200B;은(는) Adobe 조직입니다.
* **샌드박스 이름**&#x200B;은(는) 데이터 세트가 있는 샌드박스 이름입니다(예: prod, dev 등).

>[!NOTE]
>
>데이터 세트를 활성화하기 위해 API 호출을 시도할 때 아래 오류가 발생하는 경우 개발자 콘솔 프로젝트에서 Adobe Journey Optimizer API를 제거한 다음 다시 추가해 보십시오.
>
>```
>
>"error_code": "403003", 
>"message": "Api Key is invalid"
>
>```

## 개인화를 위한 데이터 세트 활용 {#leverage}

API 호출을 사용하여 조회 개인화에 대한 데이터 집합을 활성화하면 해당 데이터를 사용하여 콘텐츠를 [!DNL Journey Optimizer]&#x200B;(으)로 개인화할 수 있습니다.

1. 메시지와 같은 개인화를 정의할 수 있는 모든 컨텍스트에서 사용할 수 있는 개인화 편집기를 엽니다. [개인화 편집기로 작업하는 방법을 알아보세요](../personalization/personalization-build-expressions.md)

1. 도우미 함수 목록으로 이동하여 **datasetLookup** 도우미 함수를 코드 창에 추가합니다.

   ![](assets/aep-data-helper.png)

1. 이 함수는 Adobe Experience Platform 데이터 세트에서 필드를 호출할 수 있는 사전 정의된 구문을 제공합니다. 구문은 다음과 같습니다.

   ```
   {{datasetLookup datasetId="datasetId" id="key" result="store" required=false}}
   ```

   * **datasetId**&#x200B;은(는) 작업 중인 데이터 세트의 ID입니다.
   * **id**&#x200B;은(는) 조회 데이터 세트의 기본 ID와 연결해야 하는 원본 열의 ID입니다.

     >[!NOTE]
     >
     >이 필드에 입력한 값은 필드 ID(*profile.packages.packageSKU*), 여정 여정 이벤트에서 전달된 필드(*context.profile.events.event_ID.productSKU*) 또는 정적 값(*sku007653*)일 수 있습니다. 어떤 경우든 시스템은 값을 사용하고 데이터 세트를 조회하여 키가 일치하는지 확인합니다.
     >
     >키에 리터럴 문자열 값을 사용하는 경우 텍스트를 따옴표로 묶습니다. 예: `{{datasetLookup datasetId="datasetId" id="SKU1234" result="store" required=false}}`. 속성 값을 동적 키로 사용하는 경우 따옴표를 제거합니다. 예: `{{datasetLookup datasetId="datasetId" id=category.product.SKU result="SKU" required=false}}`

   * **result**&#x200B;은(는) 데이터 집합에서 검색할 모든 필드 값을 참조하기 위해 제공해야 하는 임의의 이름입니다. 이 값은 코드에서 각 필드를 호출하는 데 사용됩니다.

   * **required=false**: 필요한 경우 TRUE로 설정되어 있으면 일치하는 키가 있는 경우에만 메시지가 배달됩니다. false로 설정하면 일치하는 키가 필요하지 않고 메시지를 계속 전달할 수 있습니다. false로 설정된 경우 메시지 콘텐츠에 대체 항목 또는 기본값을 고려하는 것이 좋습니다.

   +++데이터 세트 ID를 검색할 위치

   데이터 세트 ID는 Adobe Experience Platform 사용자 인터페이스에서 검색할 수 있습니다. [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/user-guide#view-datasets){target="_blank"}에서 데이터 세트로 작업하는 방법을 알아보세요.

   ![](assets/aep-data-dataset.png)

   +++

1. 필요에 맞게 구문을 조정하십시오. 이 예제에서는 승객의 비행과 관련된 데이터를 검색하려고 합니다. 구문은 다음과 같습니다.

   ```
   {{datasetLookup datasetId="1234567890abcdtId" id=profile.upcomingFlightId result="flight"}}
   ```

   * ID가 &quot;abcdtId&quot;인 데이터 세트에서 작업 1234567890,
   * 조회 데이터 세트에 가입하는 데 사용할 필드는 *profile.uncomingFlightId*&#x200B;입니다.
   * &quot;플라이트&quot; 참조 아래에 모든 필드 값을 포함하려고 합니다.

1. Adobe Experience Platform 데이터 세트에서 호출할 구문이 구성되면 검색할 필드를 지정할 수 있습니다. 구문은 다음과 같습니다.

   ```
   {{result.fieldId}}
   ```

   >[!NOTE]
   >
   >데이터 세트 필드를 참조할 때 스키마 내에 정의된 전체 필드 경로와 일치하는지 확인하십시오.

   * **result**&#x200B;은(는) **MultiEntity** 도우미 함수에서 **result** 매개 변수에 할당한 값입니다. 이 예에서는 &quot;플라이트&quot;입니다.
   * **fieldID**&#x200B;은(는) 검색할 필드의 ID입니다. 이 ID는 데이터 집합과 관련된 레코드 스키마를 검색할 때 [!DNL Adobe Experience Platform] 사용자 인터페이스에 표시됩니다.

     +++필드 ID를 검색하는 위치

     Adobe Experience Platform 사용자 인터페이스에서 데이터 세트를 미리 볼 때 필드 ID를 검색할 수 있습니다. [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/user-guide#preview){target="_blank"}에서 데이터 세트를 미리 보는 방법에 대해 알아보세요.

     ![](assets/aep-data-field.png)

     +++

   이 예제에서는 승객의 탑승 시간 및 탑승구와 관련된 정보를 사용하려고 합니다. 따라서 다음 두 행을 추가합니다.

   * `{{flight._myorg.booking.boardingTime}}`
   * `{{flight._myorg.booking.gate}}`

1. 이제 코드가 준비되었으므로 평소와 같이 콘텐츠를 완료하고 **콘텐츠 시뮬레이션** 단추를 사용하여 테스트하여 개인화를 확인할 수 있습니다. [콘텐츠를 미리 보고 테스트하는 방법에 대해 알아보세요](../content-management/preview-test.md)


   ![](assets/aep-data-sample.png)
