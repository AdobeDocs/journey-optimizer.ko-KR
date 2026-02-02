---
title: 의사 결정 정책 만들기
description: 의사 결정 정책을 만드는 방법 알아보기
feature: Decisioning
topic: Integrations
role: User
level: Experienced
version: Journey Orchestration
source-git-commit: 2dfc9c2db5af1b9b74f7405a68e85563f633a54f
workflow-type: tm+mt
source-wordcount: '2108'
ht-degree: 6%

---


# 결정 정책 만들기 {#create-decision}

>[!CONTEXTUALHELP]
>id="ajo_code_based_item_number"
>title="반환할 항목 수 정의"
>abstract="반환하려는 결정 항목의 수를 선택합니다. 예를 들어 항목 2개를 선택하면 현재 구성에 대한 적격 제안 2개가 표시됩니다."

>[!CONTEXTUALHELP]
>id="ajo_code_based_fallback"
>title="대체 항목 선택"
>abstract="해당 결정 정책에 정의된 선택 전략 중 어느 것도 적합하지 않은 경우 사용자에게 대체 항목이 표시됩니다."

>[!CONTEXTUALHELP]
>id="ajo_code_based_strategy"
>title="전략이란?"
>abstract="선택 전략의 순서에 따라 먼저 평가할 전략을 결정합니다. 적어도 한 개의 전략이 필요합니다. 결합된 전략의 결정 항목을 동시에 평가합니다."
>additional-url="https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="전략 만들기"

고객에게 최상의 다이내믹 오퍼 및 경험을 제공하려면 캠페인 또는 여정에서 콘텐츠에 의사 결정 정책을 추가한 다음, 반환할 항목과 사용할 선택 전략을 구성하십시오. 이렇게 하려면 아래 절차를 따르십시오.

1. [의사 결정 정책 추가](#add)
1. [결정 정책을 구성합니다](#configure) - 이름을 추가하고 전자 메일 채널에 대해 반환할 항목 수를 지정합니다.
1. [전략 시퀀스를 설정합니다](#strategy) - 결정 정책으로 반환할 항목을 선택합니다.
1. [대체 오퍼 선택](#fallback)(선택 사항) - 적합한 항목이나 선택 전략이 없는 경우 표시할 항목을 선택합니다.
1. 선택 전략을 [검토 및 저장](#review)
1. [배치 할당](#placement)(전자 메일 채널)

>[!AVAILABILITY]
>
>결정 정책은 **코드 기반 경험**, **푸시 알림** 및 SMS 채널에 대해 모든 고객이 사용할 수 있습니다.
>
>이메일 채널에 대한 의사 결정은 제한된 가용성으로 사용할 수 있습니다. 액세스 권한을 요청하려면 Adobe 담당자에게 문의하십시오. [가용성 레이블](../rn/releases.md#availability-labels)에 대해 자세히 알아보세요.

## 의사 결정 정책 추가 {#add}

메시지에 결정 정책을 추가하려면 여정 또는 캠페인을 열고 [채널 작업](../building-journeys/journeys-message.md)을 선택하세요.

메시지 콘텐츠를 편집하고 아래 탭에서 선택한 채널을 기반으로 결정 정책을 추가하는 방법에 대한 자세한 내용을 확인하십시오.

>[!BEGINTABS]

>[!TAB 코드 기반 경험]

코드 기반 경험의 경우 속성 창에서 사용할 수 있는 **코드 편집기** 또는 **의사 결정** 메뉴를 사용하여 새 의사 결정 정책을 추가할 수 있습니다.

+++코드 편집기에서 의사 결정 정책 추가

1. **[!UICONTROL 코드 편집]** 단추를 사용하여 코드 편집기 편집기를 엽니다.

1. **[!UICONTROL 결정 정책]** 메뉴로 이동한 다음 **[!UICONTROL 결정 정책 추가]** 단추를 클릭합니다.

   ![](assets/decision-policy-add-code-editor.png)

+++

+++Decisioning 메뉴에서 의사 결정 정책 추가

1. 속성 창에서 ![](assets/do-no-localize/decisioning-icon.png) 아이콘을 클릭하여 **[!UICONTROL Decisioning]** 메뉴에 액세스합니다.

1. **[!UICONTROL 결정 정책 추가]** 단추를 클릭합니다.

   ![](assets/decision-policy-add-code.png)

+++

>[!TAB 이메일]

1. **[!UICONTROL 의사 결정 사용]** 옵션을 전환합니다.

   ![](assets/decision-policy-enable.png)

   >[!IMPORTANT]
   >
   >의사 결정을 활성화하면 기존 이메일 콘텐츠가 지워집니다. 이미 이메일을 디자인한 경우 콘텐츠를 템플릿으로 미리 저장해야 합니다.

1. 전자 메일 디자이너에서 사용할 수 있는 **개인화 편집기** 또는 **의사 결정** 메뉴를 사용하여 새 의사 결정 정책을 추가하십시오.

   +++Personalization 편집기에서 의사 결정 정책 추가

   1. 제목 줄 필드 또는 개인화를 추가할 수 있는 이메일 본문의 모든 필드에서 사용할 수 있는 ![](assets/do-no-localize/editor-icon.svg) 아이콘을 사용하여 개인화 편집기를 엽니다.

   1. **[!UICONTROL 의사 결정 정책]** 메뉴로 이동한 다음 **[!UICONTROL 의사 결정 정책 추가]** 단추를 클릭합니다.

      ![](assets/decision-policy-add-email-editor.png)

   +++

   +++Decisioning 메뉴에서 의사 결정 정책 추가

   1. 이메일 Designer을 열고 이메일 구조에서 구성 요소를 선택합니다.

   1. 속성 창에서 ![](assets/do-no-localize/decisioning-icon.png) 아이콘을 클릭하여 **[!UICONTROL Decisioning]** 메뉴에 액세스합니다.

   1. **[!UICONTROL 새 정책 추가]** 단추를 클릭합니다.

      ![](assets/decision-policy-add-email-add.png)

   >[!NOTE]
   >
   >**[!UICONTROL 결정 출력 재사용]**&#x200B;을 통해 이 전자 메일 내에 이미 만들어진 결정 정책을 재사용할 수 있습니다.

>[!TAB SMS]

SMS의 경우 속성 창에서 사용할 수 있는 **개인화 편집기** 또는 **의사 결정** 메뉴를 사용하여 새 의사 결정 정책을 추가할 수 있습니다.

+++개인화 편집기에서 의사 결정 정책 추가

1. ![](assets/do-no-localize/editor-icon.svg) 아이콘을 사용하여 개인화 편집기를 엽니다.
1. **[!UICONTROL 의사 결정 정책]** 메뉴로 이동한 다음 **[!UICONTROL 의사 결정 정책 추가]** 단추를 클릭합니다.

   ![](assets/decision-policy-add-sms-editor.png)

+++

+++Decisioning 메뉴에서 의사 결정 정책 추가

1. 속성 창에서 ![](assets/do-no-localize/decisioning-icon.png) 아이콘을 클릭하여 **[!UICONTROL Decisioning]** 메뉴에 액세스합니다.

1. **[!UICONTROL 결정 정책 추가]** 단추를 클릭합니다.

   ![](assets/decision-policy-add-sms.png)

>[!TAB 푸시 알림]

푸시 알림의 경우 속성 창에서 사용할 수 있는 **개인화 편집기** 또는 **의사 결정** 메뉴를 사용하여 새 의사 결정 정책을 추가할 수 있습니다.

+++개인화 편집기에서 의사 결정 정책 추가

1. ![](assets/do-no-localize/editor-icon.svg) 아이콘을 사용하여 개인화 편집기를 엽니다.
1. **[!UICONTROL 의사 결정 정책]** 메뉴로 이동한 다음 **[!UICONTROL 의사 결정 정책 추가]** 단추를 클릭합니다.

   ![](assets/decision-policy-add-push.png)

+++

+++Decisioning 메뉴에서 의사 결정 정책 추가

1. 속성 창에서 ![](assets/do-no-localize/decisioning-icon.png) 아이콘을 클릭하여 **[!UICONTROL Decisioning]** 메뉴에 액세스합니다.

1. **[!UICONTROL 결정 정책 추가]** 단추를 클릭합니다.

   ![](assets/decision-policy-add-push-menu.png)

>[!IMPORTANT]
>
>푸시 알림을 사용하는 Experience Decisioning에는 모바일 SDK의 특정 버전이 필요합니다. 이 기능을 구현하기 전에 [릴리스 정보](https://developer.adobe.com/client-sdks/home/release-notes/){target="_blank"}를 확인하여 필요한 버전을 식별하고 그에 따라 업그레이드했는지 확인하십시오. [이 섹션](https://developer.adobe.com/client-sdks/home/current-sdk-versions/){target="_blank"}에서 사용 가능한 플랫폼에 대한 모든 SDK 버전을 볼 수도 있습니다.

>[!ENDTABS]

## 의사 결정 정책 구성 {#configure}

콘텐츠에 새 결정 정책을 추가한 후 결정 정책 구성 화면이 열립니다. 다음 단계에 따라 의사 결정 정책을 구성합니다.

1. 결정 정책의 이름을 입력하고 카탈로그(현재 기본 **[!UICONTROL 오퍼]** 카탈로그로 제한됨)를 선택하십시오.

   ![](assets/decision-code-based-details.png)

1. **[!UICONTROL 항목 수]** 필드를 사용하면 결정 정책으로 반환할 결정 항목의 수를 정의할 수 있습니다. 예를 들어 항목 2개를 선택하면 현재 구성에 대한 적격 제안 2개가 표시됩니다.

   >[!NOTE]
   >
   >이 옵션은 이메일 및 코드 기반 경험 채널에만 사용할 수 있습니다. 다른 모든 채널의 경우, 작업 당 하나의 결정 항목만 반환될 수 있습니다.

   이메일 채널에 대해 여러 항목을 반환하려면 **[!UICONTROL 반복 그리드]** 구성 요소 내에 결정 정책을 추가해야 합니다. 자세한 내용을 보려면 아래 섹션을 확장하십시오.

   +++이메일에 여러 결정 항목 반환

   1. 이메일의 **[!UICONTROL 반복 그리드]** 구성 요소를 드래그하고 **[!UICONTROL 설정]** 창을 사용하여 원하는 대로 구성하십시오.

      ![](assets/decision-policy-repeat.png)

   1. 캔버스 도구 모음에서 **[!UICONTROL Decisioning]** 아이콘을 클릭하거나 **[!UICONTROL Decisioning]** 창을 열고 **[!UICONTROL 의사 결정 정책 추가]**&#x200B;를 선택합니다.

   1. **[!UICONTROL 항목 수]** 필드에 반환할 항목 수를 지정한 다음 아래 문서화된 대로 결정 정책을 구성하십시오. 선택할 수 있는 최대 항목 수는 **[!UICONTROL 반복 그리드]** 구성 요소에 정의된 타일 수로 제한됩니다.

   ![](assets/decision-policy-repeat-number.png)

   +++

1. **[!UICONTROL 다음]**&#x200B;을 클릭합니다.

## 전략 시퀀스 설정 {#strategy}

**[!UICONTROL 전략 시퀀스]** 섹션에서 결정 항목을 선택하고 결정 정책에 사용할 선택 전략을 설정할 수 있습니다.

1. **[!UICONTROL 추가]**&#x200B;를 클릭하고 정책에 포함할 개체 유형을 선택하십시오.

   ![](assets/decision-code-based-strategy-sequence.png)

   * **[!UICONTROL 선택 전략]** - 의사 결정 전략은 자격 조건 및 순위 방법과 관련된 컬렉션을 활용하여 표시할 항목을 결정합니다. 하나 이상의 기존 선택 전략을 선택하거나 **[!UICONTROL 선택 전략 만들기]** 단추를 사용하여 새 선택 전략을 만들 수 있습니다. [선택 전략을 만드는 방법을 알아봅니다](selection-strategies.md)

   * **[!UICONTROL 결정 항목]** - 선택 전략을 실행하지 않고도 단일 결정 항목을 선택합니다. 한 번에 하나의 결정 항목만 선택할 수 있습니다. 품목에 대해 설정된 모든 자격 제한이 적용됩니다.

   >[!NOTE]
   >
   >의사 결정 정책은 선택 전략과 의사 결정 항목을 합하여 최대 10개까지 지원한다. [보호 기능 및 제한 결정에 대해 자세히 알아보기](gs-experience-decisioning.md#guardrails)

1. 여러 개의 의사 결정 항목 및/또는 전략을 추가할 때 특정 순서로 평가된다. 시퀀스에 추가된 첫 번째 객체가 먼저 평가됩니다. 기본 시퀀스를 변경하려면 개체 및/또는 그룹을 드래그 앤 드롭하여 원하는 대로 순서를 변경합니다. 자세한 내용을 보려면 아래 섹션을 확장하십시오.

   +++의사 결정 정책에서 평가 순서 관리

   정책에 결정 항목 및 선택 전략을 추가한 후에는 해당 순서를 정렬하여 평가 순서를 결정하고 선택 전략을 결합하여 함께 평가할 수 있습니다.

   항목 및 전략을 평가할 **순차적 순서**&#x200B;은 각 개체 또는 개체 그룹의 왼쪽에 숫자로 표시됩니다. 시퀀스 내에서 선택 전략(또는 전략 그룹)의 위치를 이동하려면 해당 위치를 다른 위치로 끌어다 놓습니다.

   ![](assets/decision-code-based-strategy-groups.png)

   >[!NOTE]
   >
   >선택 전략만 시퀀스 내에서 드래그하여 놓을 수 있습니다. 결정 항목의 위치를 변경하려면 먼저 평가하려는 다른 항목을 추가한 후 **[!UICONTROL 추가]** 단추를 사용하여 결정 항목을 제거하고 다시 추가해야 합니다.

   여러 선택 전략을 그룹으로 **결합**&#x200B;하여 개별적으로 평가되지 않고 함께 평가할 수도 있습니다. 이렇게 하려면 선택 전략 아래의 **`+`** 단추를 클릭하여 다른 단추와 결합하십시오. 선택 전략을 다른 전략에 끌어다 놓아 두 전략을 그룹으로 그룹화할 수도 있습니다.

   >[!NOTE]
   >
   >결정 항목을 다른 항목이나 선택 전략과 함께 그룹화할 수 없습니다.

   여러 전략과 해당 그룹화에 따라 전략의 우선 순위와 적격 오퍼의 순위가 결정됩니다. 첫 번째 전략은 우선순위가 가장 높고 동일 그룹 내에서 결합된 전략은 우선순위가 같다.

   예를 들어 전략 A와 전략 B에 각각 하나씩, 이렇게 두 개의 컬렉션이 있습니다. 요청은 두 개의 결정 항목이 다시 전송될 수 있도록 하는 것입니다. 전략 A의 2개의 적격 오퍼와 전략 B의 3개의 적격 오퍼가 있다고 가정해 보겠습니다.

   * 두 전략이 **결합되지 않음** 또는 순차적 순서(1과 2)인 경우 첫 번째 전략의 상위 2개의 적격 오퍼가 첫 번째 행에 반환됩니다. 첫 번째 전략에 적합한 오퍼가 두 개 없는 경우, 의사 결정 엔진은 계속해서 필요한 만큼 많은 오퍼를 찾기 위해 다음 전략으로 이동하고, 필요한 경우 최종적으로 대체 오퍼를 반환합니다.

     ![](assets/decision-code-based-consecutive-strategies.png)

   * 두 컬렉션이 **동시에 평가되는 경우**, 전략 A의 2개 적격 오퍼와 전략 B의 3개 적격 오퍼가 있으므로 5개 오퍼는 모두 각 순위 방법으로 결정된 값을 기준으로 스택됩니다. 2개의 오퍼가 요청되므로 이 5개의 오퍼 중 상위 2개의 적격 오퍼가 반환됩니다.

     ![](assets/decision-code-based-combined-strategies.png)

   **여러 전략을 사용하는 예제**

   이제 여러 전략을 서로 다른 그룹으로 나눈 예를 살펴보겠습니다. 세 가지 전략을 정의했습니다. 전략 1과 전략 2는 그룹 1에서 함께 결합되고 전략 3은 독립적이다(그룹 2). 각 전략에 대한 적격 오퍼와 해당 우선순위(순위 함수 평가에 사용됨)는 다음과 같습니다.

   * 그룹 1:
      * 전략 1 - (오퍼 1, 오퍼 2, 오퍼 3) - 우선순위 1
      * 전략 2 - (오퍼 3, 오퍼 4, 오퍼 5) - 우선순위 1

   * 그룹 2:
      * 전략 3 - (오퍼 5, 오퍼 6) - 우선순위 0

   우선 순위가 가장 높은 전략 오퍼를 먼저 평가하고 등급 오퍼 목록에 추가합니다.

   * **반복 1:**

     전략 1 및 전략 2 오퍼는 함께 평가됩니다(오퍼 1, 오퍼 2, 오퍼 3, 오퍼 4, 오퍼 5). 그 결과는 다음과 같습니다.

     오퍼 1 - 10
오퍼 2 - 20
전략 1에서 오퍼 3 - 30, 전략 2에서 오퍼 45. 둘 중 가장 높은 것을 고려할 것이므로 45를 고려한다.
오퍼 4 - 40
오퍼 5 - 50

     이제 등급 오퍼는 다음과 같습니다. 오퍼 5, 오퍼 3, 오퍼 4, 오퍼 2, 오퍼 1.

   * **반복 2:**

     전략 3 오퍼가 평가됩니다(오퍼 5, 오퍼 6). 그 결과는 다음과 같습니다.

      * 오퍼 5 - 위의 결과에 이미 있으므로 평가되지 않습니다.
      * 오퍼 6 - 60

     이제 등급 오퍼는 다음과 같습니다. 오퍼 5 , 오퍼 3, 오퍼 4, 오퍼 2, 오퍼 1, 오퍼 6.

   +++

1. 선택 전략이 준비되면 **[!UICONTROL 다음]**&#x200B;을 클릭합니다.

## 대체 오퍼 추가 {#fallback}

결정 항목 및/또는 선택 전략을 선택하면 위의 항목 또는 선택 전략이 모두 충족되지 않는 경우 표시할 대체 오퍼를 추가할 수 있습니다.

현재 샌드박스에서 만든 모든 결정 항목을 표시하는 목록에서 항목을 선택할 수 있습니다. 적합한 선택 전략이 없으면 선택한 항목<!--nor frequency capping when available - TO CLARIFY-->에 적용된 날짜 및 자격 제한에 관계없이 대체 항목이 사용자에게 표시됩니다.

![](assets/decision-code-based-strategy-fallback.png)

>[!NOTE]
> 폴백은 선택 사항입니다. 요청된 항목 수까지 선택할 수 있습니다. 적합한 항목이 없고 대체 항목이 설정되지 않은 경우 아무것도 표시되지 않습니다.

## 결정 정책 검토 및 저장 {#review}

선택 전략을 구성하고 대체 오퍼를 추가한 후 **[!UICONTROL 다음]**&#x200B;을 클릭하여 의사 결정 정책을 검토하고 저장한 다음 **[!UICONTROL 만들기]**&#x200B;를 클릭하여 정책 만들기를 확인합니다.

>[!IMPORTANT]
>
>의사 결정 정책이 만들어지면 모든 데이터 영역에 전파되는 데 최대 15분, 캐나다의 경우 최대 30분이 걸릴 수 있습니다. 여기에는 새 결정 항목을 컬렉션에 추가, 항목에서 규칙 변경, 항목 콘텐츠 변경 또는 수식 업데이트와 같은 변경 내용이 포함됩니다.

개인화 편집기의 줄임표 단추나 구성 요소 속성 창의 **[!UICONTROL 결정]** 메뉴에서 언제든지 결정 정책을 편집하거나 삭제할 수 있습니다.

>[!BEGINTABS]

>[!TAB 개인화 편집기에서 정책을 편집하거나 삭제]

![](assets/decision-policy-edit.png)

>[!TAB 의사 결정 메뉴에서 정책을 편집하거나 삭제]

![](assets/decision-policy-edit-properties.png)

>[!ENDTABS]

## 배치 할당(이메일) {#placement}

이메일의 경우 의사 결정 정책과 연관된 구성 요소에 대한 배치를 정의해야 합니다. 이렇게 하려면 구성 요소 속성 창에서 **[!UICONTROL 의사 결정]** 단추를 클릭하고 **[!UICONTROL 배치 할당]**&#x200B;을 선택합니다. [배치 작업 방법 알아보기](../experience-decisioning/placements.md)

![](assets/decision-policy-rail.png)

## 다음 단계 {#next-steps}

의사 결정 정책을 만드는 방법을 이해했으므로 [!DNL Journey Optimizer] 채널에서 오퍼를 제공할 준비가 되었습니다.

➡️ [메시지에서 의사 결정 정책을 사용하는 방법 알아보기](../experience-decisioning/use-decision-policy.md)
