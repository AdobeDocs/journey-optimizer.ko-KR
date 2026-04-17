---
solution: Journey Optimizer
product: journey optimizer
title: Personalization 표현식을 위한 AI 지원
description: Journey Optimizer에서 AI Assistant를 사용하여 Personalization 편집기의 자연어에서 개인화 표현식을 생성하는 방법과 이메일 Designer에서 표현식 추가 컨트롤이 작동하는 방법에 대해 알아봅니다.
feature: Content Assistant
topic: Content Management, Artificial Intelligence
role: User
level: Intermediate
mini-toc-levels: 1
source-git-commit: a71456af0d414ba435e307f29dd6dd70ba2737a8
workflow-type: tm+mt
source-wordcount: '1064'
ht-degree: 2%

---

# 개인화 표현식을 위한 AI 지원{#generative-personalization-expressions}

>[!IMPORTANT]
>
>이 기능을 사용하기 전에 관련 [보호 및 제한 사항](gs-generative.md#generative-guardrails)을 읽어보십시오.
></br>
>
>Journey Optimizer에서 AI Assistant를 사용하려면 [사용자 계약](https://www.adobe.com/kr/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html)에 동의해야 합니다. 자세한 내용은 Adobe 담당자에게 문의하십시오.

## 개요 {#where-available}

[!UICONTROL AI Assistant]를 사용하면 일반 언어로 새로운 개인화를 생성하고, 기존 표현식이 수행하는 작업을 설명하고, 선택한 코드의 문제를 수정하여 구문 및 수동 필드 검색에 드는 시간을 줄일 수 있습니다. 선택 내용을 반복하거나 대화의 다른 변경 사항을 요청할 수도 있습니다. 다음 두 가지 방법으로 사용할 수 있습니다.

* **[!UICONTROL Personalization 편집기]** — 여러 채널(제목 줄, 본문 및 이를 여는 기타 필드)에서 편집기를 사용할 수 있는 모든 위치. 다음은 AI 지원 개인화의 일반적인 경로입니다. 편집기를 여는 위치 및 방법은 [개인화 추가](../personalization/personalization-build-expressions.md#where)를 참조하십시오.
* **전자 메일 Designer 도구 모음** — 전자 메일 Designer에서 전자 메일을 작성할 때 구성 요소를 선택하고 상황별 도구 모음에서 **[!UICONTROL 식 추가]**&#x200B;를 사용하여 전체 편집기를 먼저 열지 않고 도구 상자에서 도우미를 엽니다. 이 진입점은 이메일 작성 외부에서는 사용할 수 없습니다. [전자 메일 Designer에서 생성](#generate-email-designer)을 참조하세요.

더 광범위한 AI Assistant 설정 및 언어에 대해서는 [AI Assistant 시작](gs-generative.md)을 참조하십시오. 개인화 개념에 대해서는 [개인화 시작](../personalization/personalize.md)을 참조하십시오. 프롬프트 아이디어는 [AI 프롬프트 모범 사례](ai-assistant-prompting-guide.md)를 참조하십시오.

캠페인 또는 여정 컨텍스트에 따라 도우미는 데이터를 사용하여 작업하고 이미 노출된 [!UICONTROL Personalization 편집기]를 구성할 수 있습니다(예: 프로필 특성, 세그먼트 멤버십, 도우미 기능 및 관련 개인화 소스).

>[!NOTE]
>
>해당 세션에서 [!UICONTROL AI Assistant]가 열려 있는 동안에만 도우미가 프롬프트에서 컨텍스트를 유지합니다. 도우미나 편집기를 닫으면 대화가 지워집니다. 다음에 도우미를 열면 새 대화가 시작됩니다.

## 개인화 표현식 생성 {#generate}

이 단계들은 처음부터 개인화 표현식을 생성하는 것을 다룹니다. 편집기에 이미 있는 코드를 사용하여 작업하려면 [기존 코드 편집, 수정 또는 설명](#edit-existing)을 참조하세요.

1. 메시지 또는 콘텐츠에서 **[!UICONTROL Personalization 편집기]**&#x200B;를 엽니다.

1. 생성된 개인화 코드를 삽입할 편집기에 커서를 놓은 다음 **[!UICONTROL AI 길잡이]** 단추를 클릭합니다.

   ![](assets/ai-perso-access.png)

1. 텍스트 필드에서 필요한 프로필 특성, 세그먼트 또는 논리와 같은 일반 언어로 원하는 개인화 표현식을 설명한 다음 **[!UICONTROL 생성]**&#x200B;을 클릭합니다.

   또한 개인화된 인사말, 프로모션 코드 생성 등과 같이 **[!UICONTROL 빠른 프롬프트]** 섹션에서 바로 사용할 수 있는 프롬프트를 사용할 수도 있습니다.

   ![](assets/ai-perso-generate.png)

   >[!NOTE]
   >
   >관련 없는 프롬프트 또는 질문이 있으면 범위를 벗어나는 오류가 반환됩니다. 프롬프트를 조정하고 필요한 개인화에 대한 관련 질문을 하십시오.

1. 다중 전환 대화에서 도우미와 계속 토론할 수 있습니다. 이는 프롬프트에서 컨텍스트를 유지하므로 동일한 표현식을 단계별로 구체화할 수 있습니다. 다시 시작하려면 **[!UICONTROL 새 세션]** 단추를 클릭하세요.

   ![](assets/ai-perso-question.png)

1. 표현식을 생성한 후 **[!UICONTROL 샘플 프로필에 대한 미리 보기 표시]**&#x200B;를 클릭하여 **one** 합성 샘플 프로필에 대해 표현식이 평가되는 방식을 확인하고 관련 페이로드를 JSON으로 확인합니다. 미리 보기는 **단일** 별색 검사이므로 코드가 예상대로 확인될 수 있습니다. 여러 수신자, 다양한 데이터 또는 전체 범위를 **시뮬레이트하지 않습니다**. 샘플 데이터는 조직에 저장되거나 저장되지 않습니다.

   샘플을 조정해야 하는 경우(예: 강조된 다른 특성), 도우미를 사용한 토론에서 필요한 사항을 설명하고 프롬프트에 **미리 보기** 키워드를 포함하십시오.

   ![](assets/ai-perso-preview-button.png)

   +++미리 보기 예

   ![](assets/ai-perso-preview.png)

   >[!NOTE]
   >
   >여기에서는 여러 개의 미리 보기 행 또는 완벽한 시나리오를 예상하지 마십시오. 컨트롤은 많은 프로필에서 부분 범위가 아니라 빠른 코드 검사를 위해 **one** 샘플 평가로 의도적으로 제한됩니다. 비현실적으로 큰 미리보기 세트를 요청하면 요청이 실패할 수 있습니다.

   +++

   >[!NOTE]
   >
   >이 컨트롤은 편집기에서 개인화 코드를 빠르게 검사하기 위한 것이며 콘텐츠의 전체 메시지 미리 보기가 아닙니다. 경험에 대한 완전한 유효성 검사는 일반적인 시뮬레이션 흐름을 사용하십시오. [콘텐츠를 미리 보고 테스트하는 방법에 대해 알아보세요](../content-management/preview-test.md)

1. 개인화 식에서 출력을 구현하려면 **[!UICONTROL 적용]**&#x200B;을 클릭합니다. 도우미 출력은 개인화 편집기의 커서 위치에 삽입됩니다. 이미 있는 코드를 대신 바꾸려면 먼저 편집기에서 해당 코드를 선택한 다음 **[!UICONTROL AI 도우미로 편집]**&#x200B;을 사용합니다([기존 코드 편집, 수정 또는 설명](#edit-existing) 참조).

   출력을 복사한 후 ![복사 아이콘](../orchestrated/assets/do-not-localize/activity-copy.svg) 아이콘을 사용하여 필요한 위치에 붙여넣을 수도 있습니다.

## 기존 코드 편집, 수정 또는 설명 {#edit-existing}

기존 개인화 표현식을 선택하고 AI Assistant를 사용하여 개인화 문제를 해결하거나, 코드의 기능을 설명하거나, 기타 변경 사항을 요청할 수 있습니다.

1. 편집기에서 기존 개인화 코드를 선택합니다.

1. 선택 항목을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL AI 도우미로 편집]**&#x200B;을 선택하면 도우미가 선택 항목을 컨텍스트로 사용합니다.

   ![](assets/ai-perso-right-click.png)

1. **[!UICONTROL AI 길잡이]**&#x200B;가 열립니다. **[!UICONTROL 빠른 명령]**&#x200B;에서 **[!UICONTROL 설명]** 또는 **[!UICONTROL 수정]**&#x200B;을 클릭하거나 텍스트 필드를 사용하여 다른 변경 사항을 요청하고 대화를 시작하십시오.

   ![](assets/ai-perso-edit.png)

1. **[!UICONTROL 수정]**&#x200B;을(를) 사용하는 경우 토론 내용에 있는 **[!UICONTROL 수정 세부 정보 표시]**&#x200B;를 클릭하여 수정 사항에 대한 설명과 미리 보기 전후의 줄바꿈을 표시합니다.

   ![](assets/ai-perso-fix.png)

1. 개인화 식을 생성할 때와 마찬가지로 **[!UICONTROL 적용]**&#x200B;을 클릭하여 도우미 출력을 구현합니다. 개인화 편집기에서 선택한 코드를 대체합니다. 예를 들어 코드에 대한 설명을 요청한 경우 을 적용하면 표현식에 수행하는 작업을 설명하는 주석이 추가됩니다.

## 이메일 Designer 도구 모음에서 생성 {#generate-email-designer}

>[!NOTE]
>
>이 섹션은 전자 메일 Designer에서 **전자 메일** 콘텐츠를 편집하는 경우에만 적용됩니다. 다른 채널의 경우 **[!UICONTROL Personalization 편집기]**&#x200B;를 사용하십시오.

이메일 Designer에서 먼저 전체 [!UICONTROL Personalization 편집기]를 열지 않고도 상황별 도구 모음에서 개인화 표현식에 [!UICONTROL AI Assistant]를 사용할 수 있습니다.

1. 이메일 Designer에서 개인화할 구성 요소를 선택하고 표현식을 삽입할 위치를 클릭합니다.

1. 상황별 도구 모음에서 **[!UICONTROL 식 추가]**&#x200B;를 클릭합니다.

   ![](assets/ai-perso-add-expression.png)

1. AI Assistant에 개인화를 묻는 메시지를 표시할 수 있는 도구 상자가 열립니다. 필요한 내용을 일반 언어로 입력하면 빠른 표현식 빌드를 위해 도우미가 프로필 필드 및 프롬프트와 일치하는 기타 속성을 제안합니다.

1. 도우미가 표현식을 생성합니다.

   ![](assets/ai-perso-add-expression-insert.png)

   다음과 같은 작업을 수행할 수 있습니다.

   * 샘플 값 하나로 식 출력의 유효성을 검사합니다. **[!UICONTROL 미리 보기]** 탭을 사용하십시오.
   * 같은 프롬프트에서 다른 제안을 생성합니다. **[!UICONTROL 다시 생성]**&#x200B;을 사용하십시오.
   * 토론을 지우고 다시 시작하십시오. **[!UICONTROL 다시 설정]**&#x200B;을 사용하십시오.
   * 전체 편집기에서 식을 다듬어 ![편집 아이콘](assets/do-not-localize/Smock_Edit_18_N.svg "편집") 아이콘을 클릭하여 **[!UICONTROL Personalization 편집기]**&#x200B;를 엽니다.

1. 결과에 만족하면 **[!UICONTROL 삽입]**&#x200B;을 클릭하여 콘텐츠에 식을 추가합니다.
