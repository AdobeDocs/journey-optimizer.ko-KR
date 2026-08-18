---
title: 이메일 렌더링 테스트
description: 이메일 렌더링을 테스트하고 이메일 클라이언트 및 환경 전반의 알려진 렌더링 제한 사항을 이해하는 방법에 대해 알아봅니다.
feature: Preview
role: User
level: Beginner
exl-id: fe077a8b-9788-4723-a1e7-32816a879af9
feature_v2: []
subfeature_v2:
  - id: f8d2e9f0-69c9-40cd-890f-71336c8dfff7
source-git-commit: ca053767a216de5f43415c94eb7dd24cffe9dff7
workflow-type: tm+mt
source-wordcount: 405
ht-degree: 1%

---

# 이메일 렌더링 테스트 {#email-rendering}

>[!BEGINSHADEBOX]

**이 페이지에서:** Litmus 계정을 Adobe Journey Optimizer에 연결하여 인기 있는 이메일 클라이언트에서 이메일 렌더링을 테스트하고 모바일 웹 브라우저 환경을 포함한 알려진 렌더링 제한 사항을 이해하는 방법에 대해 알아봅니다.

>[!ENDSHADEBOX]

**Litmus** 계정을 [!DNL Journey Optimizer]에 활용하면 인기 있는 이메일 클라이언트에서 **이메일 렌더링**&#x200B;을(를) 즉시 미리 볼 수 있습니다. 그런 다음 모든 받은 편지함에서 이메일 콘텐츠가 제대로 표시되고 제대로 작동하는지 확인할 수 있습니다.

전자 메일 렌더링을 확인하려면 다음 단계를 수행합니다.

1. 메시지의 콘텐츠 편집 화면 또는 이메일 Designer에서 **[!UICONTROL 콘텐츠 시뮬레이션]**&#x200B;을 클릭한 다음 드롭다운에서 **[!UICONTROL 콘텐츠 시뮬레이션(AEP 프로필)]**&#x200B;을 선택합니다.

1. **[!UICONTROL 전자 메일 렌더링]** 단추를 선택합니다.

   ![](../email/assets/email-rendering-button.png)

1. 오른쪽 상단의 **Litmus 계정 연결**&#x200B;을 클릭합니다.

   ![](../email/assets/email-rendering-litmus.png)

1. 자격 증명을 입력하고 로그인하십시오.

   ![](../email/assets/email-rendering-credentials.png)

1. 전자 메일 미리 보기를 생성하려면 **테스트 실행** 단추를 클릭하십시오.

1. 인기 있는 데스크탑, 모바일 및 웹 기반 클라이언트에서 이메일 콘텐츠를 확인합니다.

   ![](../email/assets/email-rendering-previews.png)

>[!CAUTION]
>
>[!DNL Journey Optimizer]과(와) **Litmus** 계정에 연결할 때 테스트 메시지가 Litmus로 전송되는 것에 동의합니다. 전송되면 이러한 이메일은 더 이상 Adobe에서 관리되지 않습니다. 따라서 이러한 테스트 메시지에 포함될 수 있는 개인화 데이터를 포함하여 이러한 이메일에 Litmus 데이터 보존 이메일 정책이 적용됩니다.

## 모바일 웹 브라우저 제한 사항 {#rendering-limitations}

전자 메일 렌더링은 기본 모바일 앱이나 데스크톱 클라이언트를 사용하는 대신 받는 사람이 모바일 웹 브라우저&#x200B;**(예: 전화의 Chrome)를 통해 Gmail 또는 Outlook**&#x200B;을 열 때 다를 수 있습니다. 이는 모바일 웹 메일 환경의 알려진 제한이며 Journey Optimizer에만 국한되지 않습니다.

이러한 렌더링 차이는 웹 메일 클라이언트가 모바일 브라우저 내에서 작동하는 방식에서 비롯됩니다. 브라우저는 먼저 전체 데스크탑 웹 메일 UI를 렌더링하여 2개의 레이어를 깊이 있게 만듭니다. 이는 응답하는 CSS나 미디어 쿼리의 범위를 벗어납니다. Gmail 웹은 CSS `<style>` 블록을 제거하고 이메일 콘텐츠를 자체 `<div>`(으)로 래핑하므로 스타일을 재정의하고 정렬 충돌을 만들 수 있습니다.

일반적인 증상으로는 텍스트 정렬 이동(가운데 표시된 왼쪽 정렬 텍스트), 컨텐츠 섹션 사이의 추가 흰색 구분선 및 템플릿 디자인과 다른 전체 레이아웃이 있습니다.

이러한 문제는 모바일 브라우저를 통해 액세스할 때 Gmail Web 및 Outlook Web에서만 발생합니다. 모든 데스크탑 클라이언트뿐만 아니라 Outlook 및 Gmail 기본 모바일 앱도 영향을 받지 않습니다.

>[!TIP]
>
>영향을 최소화하려면 다음 작업을 수행하십시오.
>
>* 완전히 인라인된 CSS를 사용하여 간단한 표 기반 레이아웃을 사용합니다.
>
>* 텍스트 정렬과 같은 중요한 레이아웃 속성에 미디어 쿼리 또는 `<style>` 블록을 사용하지 마십시오.
