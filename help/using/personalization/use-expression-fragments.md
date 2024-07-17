---
solution: Journey Optimizer
product: journey optimizer
title: 표현식 조각 사용
description: ' [!DNL Journey Optimizer] 개인화 편집기에서 식 조각을 사용하는 방법을 알아봅니다.'
feature: Personalization, Fragments
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: 표현식, 편집기, 라이브러리, 개인화
exl-id: 74b1be18-4829-4c67-ae45-cf13278cda65
source-git-commit: e6924928e03d494817a2368b33997029ca2eca1c
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 0%

---

# 표현식 조각 활용 {#use-expression-fragments}

**개인화 편집기**&#x200B;를 사용하는 경우 현재 샌드박스에 만들거나 저장한 모든 표현식 조각을 활용할 수 있습니다.

조각은 [!DNL Journey Optimizer] 캠페인 및 여정에서 참조할 수 있는 재사용 가능한 구성 요소입니다. 이 기능을 사용하면 마케팅 사용자가 개선된 디자인 프로세스에서 콘텐츠를 빠르게 조합하는 데 사용할 수 있는 여러 사용자 지정 콘텐츠 블록을 미리 빌드할 수 있습니다. [조각을 만들고 관리하는 방법을 알아보세요](../content-management/fragments.md).

➡️[이 비디오에서 조각을 관리, 작성 및 사용하는 방법을 알아봅니다](../content-management/fragments.md#video-fragments)

## 표현식 조각 사용 {#use-expression-fragment}

콘텐츠에 표현식 조각을 추가하려면 아래 단계를 수행합니다.

>[!NOTE]
>
>주어진 게재에서 최대 30개의 조각을 추가할 수 있습니다. 조각은 최대 1개 수준까지만 중첩할 수 있습니다.

1. [개인화 편집기](personalization-build-expressions.md)를 열고 왼쪽 창에서 **[!UICONTROL 조각]** 단추를 선택합니다.

   목록에는 현재 샌드박스에서 조각으로 생성되거나 저장된 모든 표현식 조각이 표시됩니다. 만든 날짜별로 정렬됩니다. 최근에 추가된 표현식 조각이 목록에 먼저 표시됩니다. [자세히 알아보기](../content-management/fragments.md#create-expression-fragment)

   ![](assets/expression-fragments-pane.png)

   이 목록을 새로 고칠 수도 있습니다.

   >[!NOTE]
   >
   >콘텐츠를 편집하는 동안 일부 조각이 수정되거나 추가된 경우 목록이 최신 변경 내용으로 업데이트됩니다.

1. 표현식 조각 옆에 있는 + 아이콘을 클릭하여 해당 조각 ID를 편집기에 삽입합니다.

   ![](assets/expression-fragment-add.png)

   >[!CAUTION]
   >
   >콘텐츠에 **초안** 또는 **라이브** 조각을 추가할 수 있습니다. 하지만 초안 상태의 조각을 사용 중인 경우에는 여정 또는 캠페인을 활성화할 수 없습니다. 여정 또는 캠페인 게시 시 초안 조각에 오류가 표시되며 이를 승인해야 게시할 수 있습니다.

1. 조각 ID가 추가되면 해당 식 조각을 열고 인터페이스에서 [편집](../content-management/fragments.md#edit-fragments)하면 변경 내용이 동기화됩니다. 해당 조각 ID를 포함하는 모든 초안 또는 라이브 여정/캠페인에 자동으로 전파됩니다.

1. 조각 옆에 있는 **[!UICONTROL 추가 작업]** 단추를 클릭합니다. 화면에 표시되는 메뉴에서 **[!UICONTROL 조각 보기]**&#x200B;를 선택하여 해당 조각에 대한 자세한 정보를 확인합니다. **[!UICONTROL 조각 ID]**&#x200B;도 표시되며 여기에서 복사할 수 있습니다.

   ![](assets/expression-fragment-view.png)

1. 상황별 메뉴에서 **[!UICONTROL 조각 열기]** 옵션을 사용하거나 **[!UICONTROL 조각 정보]** 창에서 해당 콘텐츠 및 속성을 편집할 수 있습니다. [조각을 편집하는 방법을 알아보세요](../content-management/fragments.md#edit-fragments)

   ![](assets/expression-fragment-open.png)

1. 그런 다음 [개인화 편집기](personalization-build-expressions.md)의 모든 개인화 및 작성 기능을 사용하여 평소와 같이 콘텐츠를 사용자 지정하고 유효성을 검사할 수 있습니다.

>[!NOTE]
>
>여러 줄 바꿈이 포함된 식 조각을 만들어 [SMS](../sms/create-sms.md#sms-content) 또는 [푸시](../push/design-push.md) 콘텐츠에서 사용하면 줄 바꿈이 유지됩니다. 따라서 메시지를 보내기 전에 [SMS](../sms/send-sms.md) 또는 [푸시](../push/send-push.md) 메시지를 테스트하십시오.

## 편집 가능한 필드 사용자 지정 {#customize-fields}

변수를 사용하여 표현식 조각의 특정 부분을 편집할 수 있게 만든 경우 특정 구문을 사용하여 해당 기본값을 무시할 수 있습니다. [조각을 사용자 지정할 수 있게 만드는 방법을 알아보세요](../content-management/customizable-fragments.md)

필드를 사용자 정의하려면 다음 단계를 수행합니다.

1. **조각** 메뉴에서 코드에 조각을 삽입합니다.

1. 변수의 기본값을 재정의하려면 구문 끝에 있는 `<fieldId>="<value>"` 코드를 사용하십시오.

   아래 예에서는 ID가 &quot;sports&quot;인 변수의 값을 &quot;yoga&quot; 값으로 재정의합니다. 스포츠 변수가 참조되는 모든 곳에서 조각 콘텐츠에 &quot;요가&quot;가 표시됩니다.

   ![](../content-management/assets/fragment-expression-use.png)

전자 메일을 만들 때 편집 가능한 필드를 표현식 조각에 추가하고 해당 값을 재정의하는 방법을 보여 주는 예는 [이 섹션](../content-management/customizable-fragments.md#example)에서 확인할 수 있습니다.

## 상속 중단 {#break-inheritance}

개인화 편집기에 조각 ID를 추가하면 원본 표현식 조각에 대한 변경 사항이 동기화됩니다.

그러나 표현식 조각의 콘텐츠를 편집기에 붙여넣을 수도 있습니다. 상황별 메뉴에서 **[!UICONTROL 조각 붙여넣기]**&#x200B;를 선택하여 해당 콘텐츠를 삽입합니다.

![](assets/expression-fragment-paste.png)

이 경우 원본 조각의 상속이 끊어집니다. 조각의 콘텐츠가 편집기에 복사되며, 변경 사항은 더 이상 동기화되지 않습니다.

이 요소는 더 이상 원본 조각에 연결되지 않는 독립 실행형 요소가 됩니다. 코드의 다른 요소로 편집할 수 있습니다.

