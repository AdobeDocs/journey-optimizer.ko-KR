---
solution: Journey Optimizer
product: journey optimizer
title: 단일 이벤트 구성
description: 단일 이벤트를 구성하는 방법 알아보기
feature: Journeys, Events
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate, Experienced
keywords: event, unitary, create, 여정
exl-id: e22e2bc7-0c15-457a-8980-97bea5da7784
source-git-commit: f9f2cd339680d0dbff1812e64c5082ca97a34771
workflow-type: tm+mt
source-wordcount: '1638'
ht-degree: 10%

---

# 단일 이벤트 구성 {#configure-an-event}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_unitary"
>title="단일 이벤트"
>abstract="이벤트 구성에서는 Journey Optimizer가 이벤트로 수신할 정보를 정의할 수 있습니다. 여정의 각 단계에서 여러 이벤트를 사용할 수 있으며 여러 여정에서 같은 이벤트를 사용할 수도 있습니다. 단일 이벤트는 특정 프로필에 연결됩니다. 단일 이벤트는 규칙 기반이거나 시스템 생성일 수 있습니다."

단일 이벤트는 특정 프로필에 연결됩니다. 규칙 기반 또는 시스템 생성 방식일 수 있습니다.  단일 이벤트 [이 섹션](../event/about-events.md)에 대해 자세히 알아보세요.

다음은 새 이벤트를 구성하는 첫 번째 단계입니다.

1. 관리 메뉴 섹션에서 **[!UICONTROL 구성]**(으)로 이동하고 **[!UICONTROL 이벤트]** 섹션에서 **[!UICONTROL 관리]**&#x200B;를 클릭합니다. 이벤트 목록이 표시됩니다.

   ![](assets/jo-event1.png)

1. 새 이벤트를 만들려면 **[!UICONTROL 이벤트 만들기]**&#x200B;를 클릭합니다. 그러면 화면 오른쪽에 이벤트 구성 창이 열립니다.

   ![](assets/jo-event2.png)

1. 이벤트의 이름을 입력합니다. 설명을 추가할 수도 있습니다.

   ![](assets/jo-event3.png)

   >[!NOTE]
   >
   >영숫자와 밑줄만 허용됩니다. 최대 길이는 30자입니다.

1. **[!UICONTROL Type]** 필드에서 **Unitary**&#x200B;를 선택합니다.

   ![](assets/jo-event3bis.png)

1. **[!UICONTROL 이벤트 ID 유형]** 필드에서 사용할 이벤트 ID 유형을 선택합니다. **규칙 기반** 또는 **시스템 생성**. [이 섹션](../event/about-events.md#event-id-type)의 이벤트 ID 유형에 대해 자세히 알아보세요.

   ![](assets/jo-event4.png)

1. 이 이벤트를 사용하는 여정 수는 **[!UICONTROL 다음 항목에서 사용됨]** 필드에 표시됩니다. **[!UICONTROL 여정 보기]** 아이콘을 클릭하여 이 이벤트를 사용하는 여정 목록을 표시할 수 있습니다.

1. 스키마 및 페이로드 필드를 정의합니다. 이 단계에서 여정이 수신하도록 할 이벤트 정보(대개 페이로드)를 선택합니다. 그러면 이 정보를 경로에 사용할 수 있습니다. [이 섹션](../event/about-creating.md#define-the-payload-fields)을 참조하십시오.

   ![](assets/jo-event5.png)

   >[!NOTE]
   >
   >**[!UICONTROL 시스템 생성]** 유형을 선택하면 eventID 유형 필드가 있는 스키마만 사용할 수 있습니다. **[!UICONTROL 규칙 기반]** 유형을 선택하면 모든 경험 이벤트 스키마를 사용할 수 있습니다.

1. 규칙 기반 이벤트의 경우 **[!UICONTROL 이벤트 ID 조건]** 필드 내부를 클릭합니다. 단순 또는 고급 표현식 편집기를 사용하여 여정을 트리거할 이벤트를 식별하는 데 시스템에서 사용할 조건을 정의합니다.

   ![](assets/jo-event6.png)

   이 예제에서는 프로필의 도시를 기반으로 조건을 작성했습니다. 즉, 시스템에서 이 조건(**[!UICONTROL City]** 필드 및 **[!UICONTROL Paris]** 값)과 일치하는 이벤트를 받을 때마다 여정에게 전달합니다.

   >[!NOTE]
   >
   >단순 표현식 편집기에서 모든 연산자를 사용할 수 있는 것은 아니며, 데이터 유형에 따라 다릅니다. 예를 들어 필드의 문자열 유형의 경우 &quot;포함&quot; 또는 &quot;같음&quot;을 사용할 수 있습니다.
   >
   >이벤트를 만든 후 새 열거형 값으로 스키마를 수정하는 경우, 다음 단계에 따라 변경 사항을 기존 이벤트에 적용해야 합니다. 이벤트 필드에서 열거형 필드를 선택 취소하고, 선택을 확인한 다음 열거형 필드를 다시 선택합니다. 이제 새 열거형 값이 표시됩니다.

1. ID 유형을 추가합니다. 이 단계는 선택 사항이지만 ID 유형을 추가하면 실시간 고객 프로필 서비스에 저장된 정보를 활용할 수 있으므로 권장됩니다. 이 정보에 따라 이벤트의 키 유형이 정의됩니다. 자세한 내용은 [이 섹션](../event/about-creating.md#select-the-namespace)을 참조하십시오.

1. 프로필 식별자 정의: 페이로드 필드에서 필드를 선택하거나 공식을 정의하여 이벤트와 연관된 사용자를 식별합니다. ID 유형을 선택하면 이 키가 자동으로 설정되지만 편집할 수 있습니다. 실제로 여정은 ID 유형에 해당해야 하는 키를 선택합니다(예를 들어 이메일 ID 유형을 선택하면 이메일 키가 선택됨). 자세한 내용은 [이 섹션](../event/about-creating.md#define-the-event-key)을 참조하십시오.

   ![](assets/jo-event7.png)

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

   이제 이벤트가 구성되었으며 경로에 추가할 수 있는 상태가 되었습니다. 이벤트를 수신하려면 추가 구성 단계를 수행해야 합니다. [이 페이지](../event/additional-steps-to-send-events-to-journey.md)를 참조하십시오.

## 페이로드 필드 정의 {#define-the-payload-fields}

페이로드 정의를 사용하면 여정의 이벤트에서 시스템이 받을 것으로 예상되는 정보와 해당 이벤트와 연관된 사용자를 식별하는 키를 선택할 수 있습니다. 페이로드는 Experience Cloud XDM 필드 정의를 기반으로 합니다. XDM에 대한 자세한 내용은 [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko-KR){target="_blank"}를 참조하세요.

1. 목록에서 XDM 스키마를 선택하고 **[!UICONTROL 필드]** 필드 또는 **[!UICONTROL 편집]** 아이콘을 클릭합니다.

   ![](assets/journey8.png)

   스키마에 정의된 모든 필드가 표시됩니다. 필드 목록은 스키마마다 다릅니다. 특정 필드를 검색하거나 필터를 사용하여 모든 노드 및 필드를 표시하거나 선택한 필드만 표시할 수 있습니다. 스키마 정의에 따라 일부 필드는 필수이고 미리 선택될 수 있습니다. 선택을 취소할 수 없습니다. 여정이 이벤트를 제대로 수신하기 위해 반드시 필요한 모든 필드가 기본적으로 선택됩니다.

   >[!NOTE]
   >
   >시스템 생성 이벤트의 경우 XDM 스키마에 &quot;orchestration&quot; 필드 그룹을 추가했는지 확인하십시오. 이렇게 하면 스키마에 [!DNL Journey Optimizer] 작업에 필요한 모든 정보가 포함됩니다.

   ![](assets/journey9.png)

1. 이벤트에서 수신할 필드를 선택합니다. 비즈니스 사용자가 여정 시 활용할 필드입니다. 이벤트에 연결된 사용자를 식별하는 데 사용할 키도 포함해야 합니다([이 섹션](../event/about-creating.md#define-the-event-key) 참조).

   >[!NOTE]
   >
   >시스템 생성 이벤트의 경우 [!DNL Journey Optimizer]에서 이벤트를 식별할 수 있도록 선택한 필드 목록에 **[!UICONTROL eventID]** 필드가 자동으로 추가됩니다. 이벤트를 푸시하는 시스템은 ID를 생성하지 않아야 하며 페이로드 미리 보기에서 사용할 수 있는 ID를 사용해야 합니다. [이 섹션](../event/about-creating.md#preview-the-payload)을 참조하십시오.

1. 필요한 필드 선택을 마쳤으면 **[!UICONTROL 확인]**&#x200B;을 클릭하거나 **[!UICONTROL Enter]**&#x200B;을 누릅니다.

   선택한 필드 수가 **[!UICONTROL 필드]** 필드에 나타납니다.

   ![](assets/journey12.png)

## ID 유형 선택 {#select-the-namespace}

>[!CONTEXTUALHELP]
>id="ajo_journey_namespace"
>title="ID 유형"
>abstract="이벤트와 연결된 고객 프로필을 식별하는 키를 선택합니다."

ID 유형(이전의 &#39;네임스페이스&#39;)을 사용하면 이벤트와 관련된 사용자를 식별하는 데 사용되는 키 유형을 정의할 수 있습니다. 구성은 선택 사항입니다. [실시간 고객 프로필](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=ko){target="_blank"}에서 가져온 추가 정보를 여정에서 검색하려면 필요합니다. 사용자 지정 데이터 소스를 통해 서드파티 시스템에서 오는 데이터만 사용하는 경우에는 ID 유형 정의가 필요하지 않습니다.

기존 ID 유형을 사용하거나 Adobe Experience Platform ID 서비스를 사용하여 새 ID 유형을 만들 수 있습니다. 자세한 내용은 [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=ko-KR){target="_blank"}를 참조하세요.

기본 ID가 있는 스키마를 선택하면 **[!UICONTROL 프로파일러 식별자]** 및 **[!UICONTROL ID 유형]** 필드가 미리 채워집니다. ID가 정의되지 않은 경우 _identityMap > id_&#x200B;을(를) 기본 키로 선택합니다. 그런 다음 ID 유형을 선택해야 하며, _identityMap > id_&#x200B;을(를) 사용하여 키가 **[!UICONTROL ID 유형]** 필드 아래에 미리 채워집니다.

필드를 선택하면 기본 ID 필드에 태그가 지정됩니다.

![](assets/primary-identity.png)

드롭다운 목록에서 ID 유형을 선택합니다.

![](assets/journey17.png)

여정 당 하나의 ID 유형만 허용됩니다. 동일한 여정에서 여러 이벤트를 사용하는 경우 동일한 ID 유형을 사용해야 합니다. [이 페이지](../building-journeys/journey.md)를 참조하십시오.

>[!NOTE]
>
>사용자 기반 ID 유형만 선택할 수 있습니다. 조회 테이블에 대한 ID 유형을 정의한 경우(예: 제품 조회에 대한 ProductID ID 유형) **ID 유형** 드롭다운 목록에서 사용할 수 없습니다.

## 프로필 식별자 정의 {#define-the-event-key}

키는 필드 또는 필드 조합이며, 이는 이벤트 페이로드 데이터의 일부이며 시스템에서 이벤트와 연관된 사용자를 식별할 수 있도록 합니다. 키는 예를 들어 Experience Cloud ID, CRM ID 또는 이메일 주소일 수 있습니다.

Adobe 실시간 고객 프로필 데이터베이스에 저장된 데이터를 사용하려면 이벤트 키가 [실시간 고객 프로필 서비스](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=ko){target="_blank"}에서 프로필 ID로 정의한 정보여야 합니다.

프로필 식별자를 통해 시스템은 이벤트와 개인의 프로필 간의 조정을 수행할 수 있습니다. 기본 ID가 있는 스키마를 선택하면 **[!UICONTROL 프로필 식별자]** 및 **[!UICONTROL ID 유형]** 필드가 미리 채워집니다. ID가 정의되지 않은 경우 _identityMap > id_&#x200B;이(가) 기본 키입니다. 그런 다음 ID 유형을 선택해야 하며, _identityMap > id_&#x200B;을 사용하여 키가 자동으로 미리 채워집니다.

필드를 선택하면 기본 ID 필드에 태그가 지정됩니다.

![](assets/primary-identity.png)

CRM ID 또는 이메일 주소와 같은 다른 키를 사용해야 하는 경우, 아래에 설명된 대로 수동으로 추가해야 합니다.

1. **[!UICONTROL 프로필 식별자]** 필드 안이나 연필 아이콘을 클릭합니다.

   ![](assets/journey16.png)

1. 페이로드 필드 목록에서 키로 선택한 필드를 선택합니다.

이벤트가 수신될 때, 키의 값은 시스템이 이벤트와 연관된 사람을 식별할 수 있게 한다. [ID 형식](../event/about-creating.md#select-the-namespace)과(와) 연결된 키를 사용하여 Adobe Experience Platform에서 쿼리를 수행할 수 있습니다. [이 페이지](../building-journeys/about-journey-activities.md#orchestration-activities)를 참조하세요.
또한 이 키는 개인이 여정 내에 있는지 확인하는 데도 사용됩니다. 실제로, 한 사람은 같은 여정에서 두 개의 다른 장소에 있을 수 없다. 따라서 시스템은 동일한 키(예: 키 CRMID=3224)가 동일한 여정의 다른 위치에 있는 것을 허용하지 않습니다.

## 고급 표현식 편집기 {#adv-exp-editor}

이벤트 ID 조건 또는 프로필 식별자를 정의할 때 고급 표현식 편집기로 전환하여 보다 복잡한 키(예: 두 필드의 이벤트 연결)를 만들 수 있습니다.

![](assets/journey20.png)

추가 조작을 수행하려면 **[!UICONTROL 고급 모드]** 단추에서 고급 식 함수에 액세스할 수 있습니다. 이러한 함수를 사용하면 필드의 일부(예: 첫 번째 문자 10개)만 고려하여 필드 연결을 수행하는 등 형식 변경과 같은 특정 쿼리를 수행하는 데 사용되는 값을 조작할 수 있습니다. 이 [페이지](../building-journeys/expression/expressionadvanced.md)를 참조하십시오.


## 페이로드 미리 보기 {#preview-the-payload}

페이로드 미리 보기를 사용하면 페이로드 정의의 유효성을 확인할 수 있습니다.

>[!NOTE]
>
>시스템 생성 이벤트의 경우 이벤트를 만들 때 페이로드 미리 보기를 보려면 이벤트를 저장한 다음 다시 엽니다. 이 단계는 페이로드에서 이벤트 ID를 생성하는 데 필요합니다.

1. 시스템에서 예상한 페이로드를 미리 보려면 **[!UICONTROL 페이로드 보기]** 아이콘을 클릭하십시오.

   ![](assets/journey13.png)

   선택한 필드가 표시됩니다.

   ![](assets/journey14.png)

1. 미리 보기를 확인하여 페이로드 정의의 유효성을 검사합니다.

1. 그런 다음 이벤트 전송을 담당하는 사람과 페이로드 미리 보기를 공유할 수 있습니다. 이 페이로드는 [!DNL Journey Optimizer]에 푸시하는 이벤트의 설정을 디자인하는 데 도움이 될 수 있습니다. [이 페이지](../event/additional-steps-to-send-events-to-journey.md)를 참조하십시오.
