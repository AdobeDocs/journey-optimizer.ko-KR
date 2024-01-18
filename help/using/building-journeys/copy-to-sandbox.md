---
solution: Journey Optimizer
product: journey optimizer
title: 다른 샌드박스로 여정 복사
description: 여정을 다른 샌드박스로 복사하는 방법 알아보기
feature: Journeys, Sandboxes
topic: Content Management
role: User, Developer, Data Engineer
level: Experienced
keywords: 샌드박스, 여정, 복사, 환경
exl-id: 8c63f2f2-5cec-4cb2-b3bf-2387eefb5002
source-git-commit: b7c31db7a126eb134c353e26c9e263a9bd1674a6
workflow-type: tm+mt
source-wordcount: '743'
ht-degree: 9%

---

# 다른 샌드박스로 여정 복사 {#copy-to-sandbox}

<!--
>[!CONTEXTUALHELP]
>id="ajo_journey_copy_main"
>title="Copy a journey to another sandbox"
>abstract="Journey Optimizer allows you to copy an entire journey from one sandbox to another. For example, you can copy a journey from the Stage sandbox environment to your Production sandbox. In addition to the Journey itself, Journey Optimizer also copies most of the objects the journey depends on."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_sandbox_details"
>title="Sandbox details"
>abstract="Select the destination sandbox you want to copy the journey to. Only sandboxes within your organization are available."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_object_details"
>title="Object details"
>abstract="This is the journey you are going to copy."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_dependent_objects"
>title="Dependent objects"
>abstract="This is the list of associated objects used in the journey. This list displays the name, the object type, as well as the internal Journey Optimizer ID."
-->

샌드박스 도구 를 사용하면 패키지 내보내기 및 가져오기를 활용하여 여러 샌드박스 간에 개체를 복사할 수 있습니다. 패키지는 단일 개체 또는 여러 개체로 구성될 수 있습니다. 패키지에 포함되는 모든 개체는 동일한 샌드박스에서 가져온 개체여야 합니다.

이 페이지에서는 Journey Optimizer 컨텍스트에서 샌드박스 도구 사용 사례를 설명합니다. 기능 자체에 대한 자세한 내용은 [Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/sandbox-tooling.html).

>[!NOTE]
>
>이 기능을 사용하려면 의 다음 권한이 필요합니다. **샌드박스 관리** 기능: 샌드박스 관리(또는 샌드박스 보기) 및 패키지 관리. [자세히 알아보기](../administration/ootb-permissions.md)

## 샌드박스 도구 시작{#sandbox-gs}

Journey Optimizer를 사용하여 한 샌드박스에서 다른 샌드박스로 전체 여정을 복사할 수 있습니다. 예를 들어 Stage 샌드박스 환경에서 프로덕션 샌드박스로 여정을 복사할 수 있습니다. Journey Optimizer은 여정 자체 외에도 여정이 의존하는 대부분의 개체(대상, 스키마, 이벤트 및 작업)도 복사합니다. 복사된 객체에 대한 자세한 내용은 다음을 참조하십시오. [섹션](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/sandbox-tooling.html#abobe-journey-optimizer-objects).

>[!CAUTION]
>
>연결된 모든 요소가 대상 샌드박스에 복사된다고 보장하지는 않습니다. 여정을 게시하기 전에 철저한 검사를 수행하는 것이 좋습니다. 이를 통해 잠재적인 누락된 오브젝트를 식별할 수 있습니다.

Target 샌드박스에서 복사되는 객체는 고유하며, 기존 요소를 덮어쓸 위험이 없습니다. 여정과 여정 내의 모든 메시지는 초안 모드에서 가져옵니다. 이렇게 하면 Target 샌드박스에서 게시하기 전에 전체 유효성 검사를 수행할 수 있습니다. 복사 프로세스는 여정 및 해당 여정의 객체에 대한 메타데이터에만 복사합니다. 이 프로세스의 일부로 프로필 또는 데이터 세트 데이터가 복사되지 않습니다.

복사 프로세스는 소스 샌드박스와 대상 샌드박스 간에 패키지 내보내기 및 가져오기를 통해 수행됩니다. 다음은 한 샌드박스에서 다른 샌드박스로 여정을 복사하는 일반적인 단계입니다.

1. 소스 샌드박스에서 여정을 패키지로 추가합니다.
1. 패키지를 대상 샌드박스로 내보냅니다.

또한 Journey Optimizer을 활용할 수 있습니다 **개체 복사 서비스 REST API** 를 클릭하여 샌드박스 개체를 관리합니다. [Object Copy Service REST API를 사용하여 작업하는 방법을 알아봅니다.](https://developer.adobe.com/journey-optimizer-apis/references/sandbox/)

## 여정을 패키지로 추가{#export}

여정을 다른 샌드박스로 복사하려면 먼저 소스 샌드박스에서 여정을 패키지로 추가해야 합니다. 다음 단계를 수행하십시오.

1. 여정 관리 메뉴 섹션에서 **[!UICONTROL 여정]**. 여정 목록이 표시됩니다.

1. 복사할 여정을 검색하고 **추가 작업** 아이콘(여정 이름 옆에 있는 세 점)을 클릭하고 **패키지에 추가**.

   ![](assets/journey-sandbox1.png)

   다음 **패키지에 추가** 창이 표시됩니다.

   ![](assets/journey-sandbox2.png)

1. 기존 패키지에 여정을 추가하거나 새 패키지를 만들 것인지 선택합니다.

   * **기존 패키지**: 드롭다운 메뉴에서 패키지를 선택합니다.
   * **새 패키지 만들기**: 패키지 이름을 입력합니다. 설명을 추가할 수도 있습니다.

1. 관리 메뉴 섹션에서 **[!UICONTROL 샌드박스]**&#x200B;를 선택하고 **패키지** 를 탭하고 내보낼 패키지를 클릭합니다.

   ![](assets/journey-sandbox3.png)

1. 내보낼 객체를 선택하고 **게시**

   ![](assets/journey-sandbox4.png)

   게시에 실패한 경우 로그를 확인하여 실패 이유를 파악할 수 있습니다. 패키지를 열고 **실패한 작업 확인**, 가져오기 작업을 선택하고 **가져오기 세부 정보 보기**.

   ![](assets/journey-sandbox9.png)

## 대상 샌드박스로 패키지 내보내기 {#import}

패키지가 게시되면 대상 샌드박스로 내보내야 합니다.

1. 소스 샌드박스에서 **[!UICONTROL 샌드박스]** 메뉴에서 **패키지** 를 탭하고 내보낼 패키지 옆에 있는 + 아이콘을 클릭합니다.

   ![](assets/journey-sandbox5.png)

1. 다음 항목 선택 **Target 샌드박스** 드롭다운 필드에서 을(를) 클릭하고 **다음**. 조직 내 샌드박스만 사용할 수 있습니다.

   ![](assets/journey-sandbox6.png)

1. 패키지 개체 및 종속성을 검토합니다. 다음은 여정에 사용되는 연결된 오브젝트 목록입니다. 이 목록에는 이름과 객체 유형이 표시됩니다. 각 개체에 대해 새 개체를 만들거나 대상 샌드박스에서 기존 개체를 사용하도록 선택할 수 있습니다.

   ![](assets/journey-sandbox7.png)

1. 다음을 클릭합니다. **완료** 오른쪽 상단 모서리에서 버튼을 눌러 대상 샌드박스에 패키지 복사를 시작합니다. 복사 프로세스는 여정의 복잡성과 복사해야 하는 개체 수에 따라 다릅니다.

1. 가져오기 작업을 클릭하여 복사 결과를 검토합니다.

   * 클릭 **가져온 개체 보기** 을 눌러 복사된 각 개별 객체를 표시합니다.
   * 클릭 **가져오기 세부 정보 보기** 을 눌러 각 객체의 가져오기 결과를 확인합니다.

   ![](assets/journey-sandbox8.png)

1. 대상 샌드박스에 액세스하여 복사된 모든 객체를 철저히 검사합니다.
