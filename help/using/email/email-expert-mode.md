---
solution: Journey Optimizer
product: journey optimizer
title: 고급 HTML 편집기를 사용하여 이메일 콘텐츠 편집
description: 전문가 모드를 사용하여 기능 플래그 제어, 보호 및 저장 유효성 검사와 함께 이메일 Designer에서 이메일 콘텐츠의 HTML 소스를 보고 편집할 수 있습니다.
feature: Email Design
topic: Content Management
role: User
level: Experienced
exl-id: 0c586565-0c65-435f-986d-cd08b59de159
source-git-commit: 110c4c9b12b085f3febb83f799f5fd0ba8a8b1fb
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 7%

---

# 고급 HTML 편집기를 사용하여 이메일 콘텐츠 편집 {#email-expert-mode}

>[!AVAILABILITY]
>
>이 기능은 제한적으로 이용할 수 있습니다. 액세스 권한을 얻으려면 Adobe 담당자에게 문의하십시오.

**고급 HTML 편집기**&#x200B;는 여정, 캠페인에 대한 **이메일 디자인** 또는 [!DNL Journey Optimizer]이메일 콘텐츠 템플릿[을(를) 편집하든 간에 ](get-started-email-design.md) [이메일 Designer](content-from-scratch.md)에서 직접 [이메일 콘텐츠](../content-management/create-content-templates.md)의 원시 HTML 소스를 보고 편집할 수 있는 전문가 모드입니다.

이 기능을 사용하면 조건과 같은 고급 표현식을 소스에 직접 삽입할 수 있습니다. 시각적(데스크톱) 보기로 다시 전환하면 컨텐츠가 다시 렌더링되므로 어떻게 표시되는지 확인하고 두 보기 중 하나에서 편집을 계속할 수 있습니다.

## 가드레일 {#guardrails}

고급 HTML 편집기를 사용하는 경우 다음 가드레일은 콘텐츠 호환성을 보호하고 기대를 설정합니다.

* 고급 HTML 편집기 **이(가) 코드를 확인**&#x200B;하지 않습니다. 구문 오류나 끊어진 레이아웃은 확인하지 않습니다. 저장하기 전에 콘텐츠를 주의 깊게 검토하십시오.

* 향후 시스템 업데이트로 기본 마크업에 대한 변경 사항을 덮어쓸 수 있습니다. **변경 내용이 유지되지 않을 수 있습니다**.

* [!DNL Adobe] 지원 팀 **이(가) 사용자 지정 코드 및 수동 변경으로 인해 발생한** 문제를 해결하거나 해결할 수 없습니다. 되돌리기가 필요할 경우를 대비하여 콘텐츠를 백업하십시오.

* 고급 HTML 보기에서는 콘텐츠를 시뮬레이션할 수 없습니다. 콘텐츠를 미리 보려면 데스크톱 보기로 전환하십시오.

* 콘텐츠 호환성을 위해 고급 HTML 보기에서 **저장할 수 없습니다**. 변경 내용을 저장할 준비가 되면 다시 데스크톱 보기로 전환합니다.

>[!WARNING]
>
>고급 HTML 편집기는 이메일 Designer의 **[!UICONTROL 직접 코드 작성]** 모드와 다릅니다. [!UICONTROL 나만의 코드 작성] 모드에서는 비주얼 편집기로 다시 전환할 수 없습니다. 해당 경로를 선택하면 코드 전용 편집이 유지됩니다. 반대로 고급 HTML 편집기를 사용하면 언제든지 HTML 보기와 데스크탑(시각적) 보기 간을 전환할 수 있습니다. [코드 편집기에 대해 자세히 알아보기](code-content.md)

## 고급 HTML 보기로 전환 {#switch-to-html-view}

고급 HTML 편집기를 열고 HTML 소스를 편집하려면 다음 단계를 따르십시오.

1. 여정 또는 캠페인에서 [이메일 만들기 또는 편집](create-email.md)과 같이 이메일 Designer에서 편집할 이메일 또는 템플릿을 열거나 [이메일 콘텐츠 템플릿](../content-management/create-content-templates.md)을 열고 [이메일 Designer](get-started-email-design.md)에서 본문을 편집합니다.

1. 화면 오른쪽 상단의 **[!UICONTROL HTML]** 단추를 클릭합니다.

   ![전자 메일 Designer 도구 모음의 HTML 단추 위치](assets/email-template-expert-mode-button.png)

1. 고급 HTML 편집기를 처음 열면 경고 메시지가 표시됩니다. 자세히 검토하고 **[!UICONTROL 확인]**&#x200B;을 클릭하여 계속하십시오. [자세히 알아보기](#guardrails)

   ![고급 HTML 편집기를 처음 열 때 경고 대화 상자](assets/email-template-expert-mode-warning.png){zoomable="yes"}

   >[!NOTE]
   >
   >이 경고는 고급 HTML 편집기를 처음 열 때만 나타나며 매월 재설정됩니다.

1. 고급 HTML 편집기가 표시됩니다.

   ![전자 메일 소스 코드를 표시하는 고급 HTML 편집기 인터페이스](assets/email-template-expert-mode.png)

1. 이메일 콘텐츠에 원하는 변경 사항을 추가합니다.

   >[!WARNING]
   >
   >구문 유효성 검사 프로세스가 없으며 [!DNL Adobe]에서 지원을 제공하지 않으므로 올바른 HTML 및 CSS 코드를 입력해야 합니다. [자세히 알아보기](#guardrails)

1. 호환성의 이유로 고급 HTML 보기에서는 콘텐츠 시뮬레이션 및 저장을 사용할 수 없습니다. 데스크탑 보기로 다시 전환하여 콘텐츠를 미리 보고 변경 사항을 저장합니다.

   ![변경 내용을 저장하려면 데스크톱 보기로 다시 전환](assets/email-template-expert-mode-save.png){zoomable="yes"}

   >[!NOTE]
   >
   >보기를 전환하면 편집 내용이 유지됩니다.

<!--
    ![](assets/email-template-expert-mode-simulate.png){zoomable="yes"}
-->

## 관련 항목

* [자체 이메일 콘텐츠 코딩](code-content.md)
* [콘텐츠 템플릿 만들기](../content-management/create-content-templates.md)
* [이메일 디자이너 시작](get-started-email-design.md)
