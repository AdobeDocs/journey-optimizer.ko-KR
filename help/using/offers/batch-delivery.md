---
title: 일괄 의사 결정
description: 주어진 Adobe Experience Platform 세그먼트의 모든 프로필에 오퍼 결정을 제공하는 방법을 알아봅니다.
exl-id: 810c05b3-2bae-4368-bf12-3ea8c2f31c01
source-git-commit: f3f38e7db95bd1a6dc41b1626177c800280fb71c
workflow-type: tm+mt
source-wordcount: '793'
ht-degree: 1%

---

# 일괄 의사 결정 {#deliver}

## 배치 의사 결정 시작 {#start}

Journey Optimizer에서는 주어진 Adobe Experience Platform 세그먼트의 모든 프로필에 오퍼 결정을 제공할 수 있습니다.

이렇게 하려면 타깃팅할 세그먼트 및 사용할 오퍼 결정 정보가 포함된 작업 요청을 Journey Optimizer에서 만들어야 합니다. 그런 다음 세그먼트의 각 프로필에 대한 오퍼 컨텐츠를 사용자 지정 일괄 처리 워크플로우에 사용할 수 있는 Adobe Experience Platform 데이터 세트에 배치합니다.

API를 사용하여 일괄 전달을 수행할 수도 있습니다. 자세한 내용은 [Batch Decisioning API 설명서](api-reference/offer-delivery-api/batch-decisioning-api.md).

## 전제 조건 {#prerequisites}

작업 요청을 구성하기 전에 다음을 생성했는지 확인하십시오.

* **데이터 세트** Adobe Experience Platform. 이 데이터 집합은 &quot;ODE DecisionEvents&quot; 스키마를 사용하여 결정 결과를 저장하는 데 사용됩니다. 자세한 내용은 [데이터 세트 설명서](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html).

* **세그먼트** Adobe Experience Platform. 세그먼트를 평가한 다음 업데이트해야 합니다. 에서 세그먼트 멤버십 평가를 업데이트하는 방법 알아보기 [Segmentation Service 설명서](http://www.adobe.com/go/segmentation-overview-en)

   >[!NOTE]
   >
   >하루에 한 번 발생하는 프로필 스냅샷에서 일괄 처리 작업이 실행됩니다. 배치 의사 결정은 빈도를 제한하며 항상 최신 스냅샷의 프로필을 로드합니다.

* **결정** Adobe Journey Optimizer. [결정을 만드는 방법 알아보기](offer-activities/create-offer-activities.md)

<!-- in API doc, remove these info and add ref here-->

## 작업 요청 만들기

새 작업 요청을 만들려면 아래 단계를 수행하십시오.

1. 에서 **[!UICONTROL Offers]** 메뉴를 열고 **[!UICONTROL Batch decisioning]** 탭을 클릭한 다음 **[!UICONTROL Create request]**.

   ![](assets/batch-create.png)

1. 작업 요청의 이름을 지정한 다음 작업 데이터를 보낼 데이터 세트를 선택합니다.

1. 타깃팅할 Adobe Experience Platform 세그먼트를 선택합니다.

1. 세그먼트에 오퍼를 전달하는 데 사용할 하나 이상의 오퍼 결정 범위를 선택하십시오.
   1. 목록에서 배치를 선택합니다.
   1. 선택한 배치에 사용할 수 있는 결정들이 표시됩니다. 원하는 결정을 선택하고 을(를) 클릭합니다 **[!UICONTROL Add]**.
   1. 작업을 반복하여 원하는 만큼 결정 범위를 추가합니다.

   ![](assets/batch-decision.png)

1. 기본적으로 각 프로필에 대해 결정 범위의 한 오퍼가 반환됩니다. 를 사용하여 반환된 오퍼 수를 조정할 수 있습니다 **[!UICONTROL Request offer per profile]** 선택 사항입니다. 예를 들어 2를 선택하면 선택한 결정 범위에 대해 가장 적합한 2개의 오퍼가 표시됩니다.

   >[!NOTE]
   >
   >결정 범위당 최대 30개의 오퍼를 요청할 수 있습니다.

1. 데이터 세트에 오퍼 컨텐츠를 포함하려면, 을 전환하십시오 **[!UICONTROL Include content]** 옵션 켜짐. 이 옵션은 기본적으로 비활성화됩니다.

1. 클릭 **[!UICONTROL Create]** 작업 요청을 실행하려면

## 배치 작업 모니터링

요청된 모든 배치 작업은 **[!UICONTROL Batch decisioning]** 탭. 또한 검색 및 필터링 도구를 사용하여 목록을 세분화할 수 있습니다.

![](assets/batch-list.png)

### 작업 요청 상태

작업 요청이 만들어지면 배치 작업은 여러 상태를 거칩니다.

>[!NOTE]
>
>작업 요청의 상태에 대한 최신 정보를 얻으려면 작업 옆에 있는 타원 버튼을 사용하여 새로 고칩니다.

1. **[!UICONTROL Queued]**: 작업 요청이 생성되어 처리 큐에 들어갔습니다. 데이터 세트당 한 번에 최대 5개의 배치 작업을 실행할 수 있습니다. 출력 데이터 세트가 동일한 다른 일괄 처리 요청이 큐에 추가됩니다. 이전 작업 실행이 완료되면 처리할 대기 중인 작업이 선택됩니다.
1. **[!UICONTROL Processing]**: 작업 요청을 처리 중입니다.
1. **[!UICONTROL Ingesting]**: 작업 요청이 실행되어 선택한 데이터 집합에 결과 데이터가 수집되고 있습니다.
1. **[!UICONTROL Completed]**: 작업 요청이 실행되었으며 결과 데이터가 이제 선택한 데이터 세트에 저장됩니다.

   >[!NOTE]
   >
   >작업 목록에서 해당 이름을 클릭하여 작업 결과가 저장되는 데이터 세트에 액세스할 수 있습니다.

작업 요청을 실행하는 동안 오류가 발생하면 **[!UICONTROL Error]** 상태. 새 요청을 만들려면 배치 작업을 복제해 보십시오. [배치 작업을 복제하는 방법을 알아봅니다](#duplicate)

### 일괄 처리 작업 처리 시간

모든 배치 작업에 대한 종료 시간은 작업 로드를 생성하는 시점부터 출력 데이터 세트에 결정 결과를 사용할 수 있는 시간까지 지속 시간입니다.

세그먼트 크기는 종단 간 배치 결정 시간에 영향을 주는 주요 요소입니다. 자격이 있는 오퍼에 전역 빈도 제한이 활성화된 경우 배치 결정을 내리는 데 추가 시간이 소요됩니다. 다음은 적절한 오퍼에 대한 빈도 캡처가 있는 경우와 없는 경우 각각의 세그먼트 크기에 대한 종단 간 처리 시간의 근사치입니다.

적합한 오퍼에 대해 빈도 제한이 활성화된 경우:

| 세그먼트 크기 | 종단 간 처리 시간 |
|--------------|----------------------------|
| 10,000개 이하 | 7분 |
| 백만 프로필 이하 | 30분 |
| 1,500만 개 이하 | 50분 |

적합한 오퍼에 대한 빈도 제한 없음:

| 세그먼트 크기 | 종단 간 처리 시간 |
|--------------|----------------------------|
| 10,000개 이하 | 6분 |
| 백만 프로필 이하 | 8분 |
| 1,500만 개 이하 | 16분 |

## 작업 요청 복제 {#duplicate}

기존 작업의 정보를 다시 사용하여 새 요청을 만들 수 있습니다.

이렇게 하려면 복제 아이콘을 클릭하고 필요한 경우 작업 정보를 편집한 다음 **[!UICONTROL Create]** 새 요청을 만들려면

![](assets/batch-duplicate.png)
