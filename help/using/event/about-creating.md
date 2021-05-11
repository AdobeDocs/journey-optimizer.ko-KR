---
title: 단일 이벤트 구성
description: 단일 이벤트 구성 방법 알아보기
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '1637'
ht-degree: 14%

---

# 단일 이벤트 {#configure-an-event} 구성

![](../assets/do-not-localize/badge.png)

단일 이벤트는 특정 프로필에 연결됩니다. 규칙을 기반으로 하거나 시스템에서 생성할 수 있습니다.  단일 이벤트 [이 섹션](../event/about-events.md)에 대해 자세히 알아보십시오.

다음은 새 이벤트를 구성하는 첫 번째 단계입니다.

1. 왼쪽 메뉴에서 **[!UICONTROL Admin]** 아이콘을 클릭한 다음 **[!UICONTROL Events]**&#x200B;을 클릭합니다. 그러면 이벤트 목록이 표시됩니다.

   ![](../assets/jo-event1.png)

1. 새 이벤트를 만들려면 **[!UICONTROL Add]**&#x200B;를 클릭합니다. 그러면 화면 오른쪽에 이벤트 구성 창이 열립니다.

   ![](../assets/jo-event2.png)

1. 이벤트 이름을 입력합니다. 설명을 추가할 수도 있습니다.

   ![](../assets/jo-event3.png)

   >[!NOTE]
   >
   >공백이나 특수 문자는 사용하지 말고 이름은 30자까지만 입력하십시오.

1. **[!UICONTROL Type]** 필드에서 **단일 이벤트**&#x200B;를 선택합니다.

   ![](../assets/jo-event3bis.png)

1. **[!UICONTROL Event ID type]** 필드에서 사용할 이벤트 ID 유형을 선택합니다.**규칙 기반** 또는 **시스템 생성**. [이 섹션](../event/about-events.md#event-id-type)의 이벤트 ID 유형에 대한 자세한 내용을 참조하십시오.

   ![](../assets/jo-event4.png)

1. 이 이벤트를 사용하는 경로 수가 **[!UICONTROL Used in]** 필드에 표시됩니다. **[!UICONTROL View journeys]** 아이콘을 클릭하여 이 이벤트를 사용하는 경로 목록을 표시할 수 있습니다.

1. 스키마 및 페이로드 필드를 정의합니다.여기에서 수신할 이벤트 정보(일반적으로 페이로드라고 함) 여정을 선택합니다. 그러면 이 정보를 경로에 사용할 수 있습니다. [이 섹션](../event/about-creating.md#define-the-payload-fields)을 참조하십시오.

   ![](../assets/jo-event5.png)

   >[!NOTE]
   >
   >**[!UICONTROL System Generated]** 유형을 선택하면 eventID 유형 믹싱이 있는 스키마만 사용할 수 있습니다. **[!UICONTROL Rule Based]** 유형을 선택하면 모든 경험 이벤트 스키마를 사용할 수 있습니다.

1. 규칙 기반 이벤트의 경우 **[!UICONTROL Event ID condition]** 필드 내부를 클릭합니다. 간단한 표현식 편집기를 사용하여 여정을 트리거할 이벤트를 식별하는 데 시스템에서 사용할 조건을 정의합니다.
   ![](../assets/jo-event6.png)

   예를 들면, 우리는 프로필의 도시에 따라 조건을 작성했습니다. 즉, 시스템에서 이 조건(**[!UICONTROL City]** 필드 및 **[!UICONTROL Paris]** 값)과 일치하는 이벤트를 받을 때마다 여정에 전달됩니다.

1. 네임스페이스를 추가합니다. 이 단계는 원하는 경우에만 수행하면 되지만, 네임스페이스를 추가하면 실시간 고객 프로필 서비스에 저장된 정보를 활용할 수 있습니다. 이 정보에 따라 이벤트의 키 유형이 정의됩니다. [이 섹션](../event/about-creating.md#select-the-namespace)을 참조하십시오.
1. 키를 정의합니다. 페이로드 필드에서 필드를 선택하거나 공식을 정의하여 이벤트와 연관된 사용자를 지정합니다. 이 키는 네임스페이스를 선택하면 자동으로 설정되지만 편집할 수 있습니다. 실제로 여정은 네임스페이스에 해당하는 키를 선택합니다(예: 이메일 네임스페이스를 선택하는 경우 이메일 키가 선택됩니다). [이 섹션](../event/about-creating.md#define-the-event-key)을 참조하십시오.

   ![](../assets/jo-event7.png)

1. 시스템에서 생성된 이벤트의 경우 조건을 추가할 수 있습니다. 조건을 추가합니다. 조건을 추가하면 시스템은 조건을 충족하는 이벤트만 처리합니다. 조건은 이벤트에 포함된 정보를 기준으로만 추가할 수 있습니다. [이 섹션](../event/about-creating.md#add-a-condition)을 참조하십시오.
1. **[!UICONTROL Save]**&#x200B;을 클릭합니다.

   ![](../assets/journey7.png)

   이제 이벤트가 구성되었으며 경로에 추가할 수 있는 상태가 되었습니다. 이벤트를 수신하려면 추가 구성 단계를 수행해야 합니다. [이 페이지](../event/additional-steps-to-send-events-to-journey-orchestration.md)를 참조하십시오.

## 페이로드 필드 정의 {#define-the-payload-fields}

페이로드 정의를 사용하면 시스템에서 여정의 이벤트에서 수신할 정보와 이벤트에 연결된 사람을 식별할 키를 선택할 수 있습니다. 페이로드가 Experience Cloud XDM 필드 정의를 기반으로 합니다. XDM에 대한 자세한 내용은 [이 페이지](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko)를 참조하십시오.

1. 목록에서 XDM 스키마를 선택하고 **[!UICONTROL Payload]** 필드 또는 **[!UICONTROL Edit]** 아이콘을 클릭합니다.

   ![](../assets/journey8.png)

   스키마에 정의된 모든 필드가 표시됩니다. 필드 목록은 스키마마다 다릅니다. 특정 필드를 검색하거나 필터를 사용하여 모든 노드 및 필드를 표시하거나 선택한 필드만 표시할 수 있습니다. 스키마 정의에 따라 일부 필드는 필수일 수도 있고 미리 선택할 수도 있습니다. 선택 취소할 수 없습니다. 여정에서 이벤트를 제대로 수신해야 하는 모든 필드는 기본적으로 선택됩니다.

   >[!NOTE]
   >
   >XDM 스키마에 &quot;오케스트레이션&quot; 믹싱을 추가해야 합니다. 이렇게 하면 스키마에 [!DNL Journey Optimizer]에서 작업하는 데 필요한 모든 정보가 포함되어 있습니다.

   ![](../assets/journey9.png)

1. 이벤트에서 받을 필드를 선택합니다. 비즈니스 사용자가 여정에서 활용할 필드입니다. 또한 이벤트에 연결된 사람을 식별하는 데 사용할 키를 포함해야 합니다([이 섹션](../event/about-creating.md#define-the-event-key) 참조).

   ![](../assets/journey10.png)

   >[!NOTE]
   >
   >시스템에서 생성된 이벤트의 경우 **[!UICONTROL eventID]** 필드가 선택된 필드 목록에 자동으로 추가되므로 [!DNL Journey Optimizer] 는 이벤트를 식별할 수 있습니다. 이벤트를 실행하는 시스템은 ID를 생성하지 않아야 합니다. 페이로드 미리 보기에서 사용할 수 있는 ID를 사용해야 합니다. [이 섹션](../event/about-creating.md#preview-the-payload)을 참조하십시오.

1. 필요한 필드 선택이 끝나면 **[!UICONTROL Save]**&#x200B;을 클릭하거나 **[!UICONTROL Enter]**&#x200B;을(를) 누릅니다.

   ![](../assets/journey11.png)

   선택한 필드의 수가 **[!UICONTROL Payload]** 필드에 표시됩니다.

   ![](../assets/journey12.png)

## 네임스페이스 {#select-the-namespace} 선택

네임스페이스를 통해 이벤트에 연결된 사람을 식별하는 데 사용되는 키 유형을 정의할 수 있습니다. 구성은 선택 사항입니다. 여정에서 [실시간 고객 프로필](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html)에서 오는 추가 정보를 검색하려면 이 값이 필요합니다. 사용자 지정 데이터 소스를 통해 타사 시스템에서 오는 데이터만 사용하는 경우에는 네임스페이스 정의가 필요하지 않습니다.

사전 정의된 항목 중 하나를 사용하거나 ID 네임스페이스 서비스를 사용하여 새 ID 네임스페이스 서비스를 만들 수 있습니다. 이 [페이지](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html)를 참조하십시오.

기본 ID가 있는 스키마를 선택하면 **[!UICONTROL Key]** 및 **[!UICONTROL Namespace]** 필드가 미리 채워집니다. ID가 정의되지 않은 경우 _identityMap > id_&#x200B;를 기본 키로 선택합니다. 그런 다음 네임스페이스를 선택해야 합니다. 그러면 _identityMap > id_&#x200B;를 사용하여 **[!UICONTROL Namespace]** 필드 아래에 키가 미리 채워집니다.

필드를 선택하면 기본 ID 필드에 태그가 지정됩니다.

![](../assets/primary-identity.png)


드롭다운 목록에서 네임스페이스를 선택합니다.

![](../assets/journey17.png)

여정당 하나의 네임스페이스만 허용됩니다. 동일한 여정에서 여러 이벤트를 사용하는 경우 동일한 네임스페이스를 사용해야 합니다. [이 페이지](../building-journeys/journey.md)를 참조하십시오.

## 이벤트 키 {#define-the-event-key} 정의

키는 이벤트 페이로드 데이터의 필드나 필드 조합이 되어 시스템에서 이벤트에 연결된 사람을 식별할 수 있도록 합니다. 키는 Experience Cloud ID, CRM ID 또는 이메일 주소와 같은 것일 수 있습니다.

실시간 고객 프로필 데이터베이스에 저장된 데이터를 활용하려면 [실시간 고객 프로필 서비스](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html)에서 프로필 ID로 정의한 정보를 이벤트 키로 선택해야 합니다.

그러면 시스템에서 이벤트와 개인 프로필 간의 조정을 수행할 수 있습니다. 기본 ID가 있는 스키마를 선택하면 **[!UICONTROL Key]** 및 **[!UICONTROL Namespace]** 필드가 미리 채워집니다. ID가 정의되지 않은 경우 _identityMap > id_&#x200B;를 기본 키로 선택합니다. 그런 다음 네임스페이스를 선택해야 합니다. 그러면 _identityMap > id_&#x200B;를 사용하여 **[!UICONTROL Namespace]** 필드 아래에 키가 미리 채워집니다.

필드를 선택하면 기본 ID 필드에 태그가 지정됩니다.

![](../assets/primary-identity.png)

CRM ID 또는 이메일 주소와 같은 다른 키를 사용해야 하는 경우 수동으로 추가해야 합니다.

1. **[!UICONTROL Key]** 필드 안이나 연필 아이콘을 클릭합니다.

   ![](../assets/journey16.png)

1. 페이로드 필드 목록에서 키로 선택한 필드를 선택합니다. 고급 표현식 편집기로 전환하여 보다 복잡한 키를 만들 수도 있습니다(예: 이벤트의 두 필드 연결). 아래 섹션을 참조하십시오.

   ![](../assets/journey20.png)

이벤트가 수신되면 시스템에서 해당 이벤트와 관련된 사람을 식별할 수 있도록 키 값을 허용합니다. 네임스페이스에 연결된 경우([이 섹션](../event/about-creating.md#select-the-namespace) 참조), 키를 사용하여 Adobe Experience Platform에서 쿼리를 수행할 수 있습니다. [이 페이지](../building-journeys/about-journey-activities.md#orchestration-activities)를 참조하십시오.
키는 또한 여정에 있는지 확인하는 데 사용됩니다. 사실, 한 사람은 같은 여정에서 두 곳에 있을 수 없다. 따라서 동일한 여정의 다른 위치에 있는 키(예: 키 CRMID=3224)를 허용하지 않습니다.

추가 조작을 수행하려면 고급 표현식 함수(**[!UICONTROL Advanced mode]**)에 액세스할 수도 있습니다. 이러한 함수를 사용하면 필드의 일부(예: 첫 번째 문자 10개)만 고려하여 형식 변경, 필드 연결 수행 등 특정 쿼리를 수행하는 데 사용되는 값을 조작할 수 있습니다. [이 페이지](https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/expressionadvanced.html)를 참조하십시오.

## 조건 {#add-a-condition} 추가

조건은 시스템에서 생성된 이벤트에만 사용할 수 있습니다. 시스템에서 이벤트 처리를 필터링할 수 있는 이벤트 조건을 정의할 수 있습니다. 조건이 true이면 이벤트가 처리됩니다. 조건이 true가 아니면 이벤트가 무시됩니다.

이벤트에 대한 조건은 이벤트 페이로드에서 전달된 데이터만 기반으로 할 수 있습니다. 이벤트 수준에서 정의된 조건은 마케터가 캔버스에서 변경할 수 없습니다. 이 이벤트를 사용할 때 이 조건을 강화합니다. 예를 들어 장바구니 값이 너무 작은 경우 마케터가 장바구니 포기 이벤트를 사용하지 않도록 하려는 경우 &quot;장바구니 값&quot; 이벤트 필드에 조건을 만들고 100달러 이상의 값을 부과할 수 있습니다.

간단한 표현식 편집기 또는 고급 표현식 편집기를 사용하여 이벤트에 대한 조건을 설정할 수 있습니다. [이 페이지](https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/expressionadvanced.html)를 참조하십시오.

예를 들어 특정 이벤트 유형의 이벤트만 처리하고 다른 유형을 무시하는 조건을 정의할 수 있습니다. 또는 이벤트가 장바구니 포기이고 페이로드에 장바구니 값 필드가 포함된 경우 장바구니 값이 100달러보다 큰 경우에만 이벤트 조건을 정의하여 이벤트를 처리할 수 있습니다.

![](../assets/journey78.png)

## 페이로드 미리 보기 {#preview-the-payload}

페이로드 미리 보기를 사용하면 페이로드 정의의 유효성을 확인할 수 있습니다.

>[!NOTE]
>
>시스템 생성 이벤트의 경우 이벤트를 만들 때 페이로드 미리 보기를 보기 전에 이벤트를 저장하고 다시 엽니다. 페이로드에서 이벤트 ID를 생성하려면 이 단계가 필요합니다.

1. 시스템에서 필요한 페이로드를 미리 보려면 **[!UICONTROL View Payload]** 아이콘을 클릭합니다.

   ![](../assets/journey13.png)

   선택한 필드가 표시됩니다.

   ![](../assets/journey14.png)

1. 미리 보기를 선택하여 페이로드 정의를 확인합니다.

1. 그런 다음 페이로드 미리 보기를 이벤트 전송을 담당하는 사람과 공유할 수 있습니다. 이 페이로드는 [!DNL Journey Optimizer]에 푸시되는 이벤트의 설정을 설계하는 데 도움이 될 수 있습니다. [이 페이지](../event/additional-steps-to-send-events-to-journey-orchestration.md)를 참조하십시오.
