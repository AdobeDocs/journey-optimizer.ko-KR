---
title: 비즈니스 이벤트 구성
description: 비즈니스 이벤트를 만드는 방법을 알아봅니다
feature: Events
topic: Administration
role: Admin
level: Intermediate
exl-id: 39eb40e1-d7f5-4a8e-9b64-c620940d5ff2
source-git-commit: 51254efaab08a572def118d475dc18f74c9d29b7
workflow-type: tm+mt
source-wordcount: '1041'
ht-degree: 12%

---

# 비즈니스 이벤트 구성 {#configure-a-business-event}

단일 이벤트와 달리 비즈니스 이벤트는 특정 프로필에 연결되어 있지 않습니다. 이벤트 ID 유형은 항상 규칙을 기반으로 합니다. 비즈니스 이벤트에 대한 자세한 내용 [이 섹션](../event/about-events.md).

세그먼트 기반 읽기 여정은 이벤트가 발생할 때 한 번에 하나씩, 정기적으로 스케줄러에 의해 또는 비즈니스 이벤트에 의해 트리거될 수 있습니다.

비즈니스 이벤트는 &quot;제품이 다시 재고&quot;, &quot;회사의 주가가 특정 값에 도달함&quot; 등이 될 수 있습니다.

>[!NOTE]
>
>비즈니스 이벤트 사용 사례를 볼 수도 있습니다 [튜토리얼](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/use-case-business-event.html).

## 중요 정보 {#important-notes}

* 시계열 스키마만 사용할 수 있습니다. 경험 이벤트, 의사 결정 이벤트 및 여정 단계 이벤트 스키마를 사용할 수 없습니다. 이벤트 스키마에는 기본 ID가 포함되어야 합니다. 다음 필드를 필요에 따라 설정해야 합니다. `_id` 및 `timestamp`
* 비즈니스 이벤트는 여정의 첫 번째 단계로만 삭제할 수 있습니다.
* 비즈니스 이벤트를 여정의 첫 번째 단계로 놓을 때 여정의 스케줄러 유형은 &quot;비즈니스 이벤트&quot;가 됩니다.
* 비즈니스 이벤트 후에 세그먼트 읽기 활동만 삭제할 수 있습니다. 다음 단계로 자동으로 추가됩니다.
* 여러 비즈니스 이벤트 실행을 허용하려면 **[!UICONTROL Execution]** 섹션에 나열된 상태로 남아 있습니다.
* 비즈니스 이벤트가 트리거되면 세그먼트를 15분에서 최대 1시간까지 내보내는 시간이 지연됩니다.
* 비즈니스 이벤트를 테스트할 때 테스트 여정에 입력할 이벤트 매개 변수와 테스트 프로필의 식별자를 전달해야 합니다. 또한 비즈니스 이벤트 기반 여정을 테스트할 때 단일 프로필 시작만 트리거할 수 있습니다. [이 섹션](../building-journeys/testing-the-journey.md#test-business)을 참조하십시오. 테스트 모드에서는 사용할 수 있는 &quot;코드 보기&quot; 모드가 없습니다.
* 새로운 비즈니스 이벤트가 도착하면 현재 여정에 있는 개인에게는 어떻게 됩니까? 이는 새 반복이 발생할 때 개인이 여전히 되풀이되는 여정에 있을 때와 같은 방식으로 동작합니다. 그들의 길은 끝났다. 따라서 마케터는 빈번한 비즈니스 이벤트를 예상하는 경우 너무 긴 여정을 만들지 않도록 주의해야 합니다.

## 여러 비즈니스 이벤트 {#multiple-business-events}

다음은 여러 비즈니스 이벤트가 연속적으로 수신될 때 적용되는 몇 가지 중요한 정보입니다.

**여정이 처리되는 동안 비즈니스 이벤트를 받을 때의 동작은 무엇입니까?**

비즈니스 이벤트는 단일 이벤트에 대한 것과 같은 방식으로 재가입 규칙을 따릅니다. 여정이 다시 입장할 수 있으면 다음 비즈니스 이벤트가 처리됩니다.

**구체화된 세그먼트를 오버로드할 수 없도록 하는 보호 기능이란 무엇입니까?**

촬영 중인 비즈니스 이벤트의 경우, 지정된 여정에 대해 첫 번째 이벤트 작업에서 푸시한 데이터는 1시간 기간 동안 재사용됩니다. 예약된 여정의 경우 가드레일이 없습니다. 의 세그먼트에 대해 자세히 알아보십시오 [Adobe Experience Platform 세그멘테이션 서비스 설명서](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

## 비즈니스 이벤트 시작 {#gs-business-events}

비즈니스 이벤트를 구성하는 첫 번째 단계는 다음과 같습니다.

1. 관리 메뉴 섹션에서 **[!UICONTROL Configurations]**. 에서  **[!UICONTROL Events]** 섹션을 클릭합니다. **[!UICONTROL Manage]**. 그러면 이벤트 목록이 표시됩니다.

   ![](../assets/jo-event1.png)

1. 새 이벤트를 만들려면 **[!UICONTROL Create Event]**&#x200B;를 클릭합니다. 그러면 화면 오른쪽에 이벤트 구성 창이 열립니다.

   ![](../assets/jo-event2.png)

1. 이벤트의 이름을 입력합니다. 설명을 추가할 수도 있습니다.

   ![](../assets/jo-event3-business.png)

   >[!NOTE]
   >
   >공백이나 특수 문자는 사용하지 말고 이름은 30자까지만 입력하십시오.

1. 에서 **[!UICONTROL Type]** 필드, 선택 **비즈니스**.

   ![](../assets/jo-event3bis-business.png)

1. 이 이벤트를 사용하는 경로 수가 **[!UICONTROL Used in]** 필드에 표시됩니다. **[!UICONTROL View journeys]** 아이콘을 클릭하여 이 이벤트를 사용하는 경로 목록을 표시할 수 있습니다.

1. 스키마 및 페이로드 필드를 정의합니다. 여기서 여정이 수신하도록 하는 이벤트 정보(대개 페이로드)를 선택합니다. 그러면 이 정보를 경로에 사용할 수 있습니다. [이 섹션](../event/about-creating-business.md#define-the-payload-fields)을 참조하십시오.

   ![](../assets/jo-event5-business.png)

   시계열 스키마만 사용할 수 있습니다. 경험 이벤트, 의사 결정 이벤트 및 여정 단계 이벤트 스키마를 사용할 수 없습니다. 이벤트 스키마에는 기본 ID가 포함되어야 합니다. 다음 필드를 필요에 따라 설정해야 합니다. `_id` 및 `timestamp`

   ![](../assets/test-profiles-4.png)

1. 의 내부를 클릭합니다. **[!UICONTROL Event ID condition]** 필드. 단순 표현식 편집기를 사용하여 시스템에서 여정을 트리거할 이벤트를 식별하는 데 사용할 조건을 정의합니다.
   ![](../assets/jo-event6-business.png)

   이 예제에서는 제품 ID를 기반으로 조건을 작성했습니다. 즉, 시스템에서 이 조건과 일치하는 이벤트를 수신할 때마다 여정에게 전달됩니다.

   >[!NOTE]
   >
   >단순 표현식 편집기에서 모든 연산자를 사용할 수 있는 것은 아니며, 데이터 유형에 따라 달라집니다. 예를 들어 문자열 유형 필드의 경우 &quot;contains&quot; 또는 &quot;equal to&quot;를 사용할 수 있습니다.

1. **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

   ![](../assets/journey7-business.png)

   이제 이벤트가 구성되었으며 경로에 추가할 수 있는 상태가 되었습니다. 이벤트를 수신하려면 추가 구성 단계를 수행해야 합니다. [이 페이지](../event/additional-steps-to-send-events-to-journey-orchestration.md)를 참조하십시오.

## 페이로드 필드를 정의합니다 {#define-the-payload-fields}

페이로드 정의를 사용하면 시스템에서 여정의 이벤트에서 받게 될 정보를 선택하고 키와 어떤 사람이 이벤트에 연결되어 있는지 식별할 수 있습니다. 페이로드는 Experience Cloud XDM 필드 정의를 기반으로 합니다. XDM에 대한 자세한 내용은 [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko){target=&quot;_blank&quot;}.

1. 목록에서 XDM 스키마를 선택하고 를 클릭합니다. **[!UICONTROL Fields]** 필드 또는 **[!UICONTROL Edit]** 아이콘.

   ![](../assets/journey8-business.png)

   스키마에 정의된 모든 필드가 표시됩니다. 필드 목록은 스키마마다 다릅니다. 특정 필드를 검색하거나 필터를 사용하여 모든 노드와 필드를 표시하거나 선택한 필드만 표시할 수 있습니다. 스키마 정의에 따라 일부 필드는 필수 필드이며 미리 선택되어 있을 수 있습니다. 선택 취소할 수 없습니다. 여정이 이벤트를 제대로 수신하기 위해 필수 필드인 모든 필드는 기본적으로 선택됩니다.

   ![](../assets/journey9-business.png)

   >[!NOTE]
   >
   > 다음 필드가 선택되어 있는지 확인합니다. `_id` 및 `timestamp`

1. 이벤트에서 받을 필드를 선택합니다. 비즈니스 사용자가 여정에서 활용할 수 있는 필드입니다.

1. 필요한 필드 선택을 완료했으면 을 클릭합니다 **[!UICONTROL Save]** 또는 **[!UICONTROL Enter]**.

   선택한 필드 수가 **[!UICONTROL Fields]** 필드.

   ![](../assets/journey12-business.png)

## 페이로드 미리 보기 {#preview-the-payload}

페이로드 미리 보기를 사용하면 페이로드 정의의 유효성을 검사할 수 있습니다.

1. 을(를) 클릭합니다. **[!UICONTROL View Payload]** 아이콘을 클릭하여 시스템에 필요한 페이로드를 미리 봅니다.

   ![](../assets/journey13-business.png)

   선택한 필드가 표시되었음을 알 수 있습니다.

   ![](../assets/journey14-business.png)

1. 미리 보기를 선택하여 페이로드 정의의 유효성을 확인합니다.

1. 그런 다음 이벤트 전송을 담당하는 사람과 페이로드 미리 보기를 공유할 수 있습니다. 이 페이로드는 푸시 이벤트 설정을 디자인하는 데 도움이 될 수 있습니다 [!DNL Journey Optimizer]. [이 페이지](../event/additional-steps-to-send-events-to-journey-orchestration.md)를 참조하십시오.
