---
title: 테스트 프로필 선택
description: 테스트 프로필을 선택하여 콘텐츠를 미리 보고 테스트하는 방법을 알아봅니다.
feature: Preview, Proofs
role: User
level: Beginner
exl-id: c51e4089-7f51-437d-a5ed-de10bab46cf8
source-git-commit: 03cb3298c905766bc059e82c58969a2111379345
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 13%

---

# 테스트 프로필 선택 {#select-test-profiles}

>[!CONTEXTUALHELP]
>id="ajo_preview_test_profiles"
>title="테스트 프로필을 사용하여 콘텐츠 확인"
>abstract="테스트 프로필을 사용하여 콘텐츠를 미리 보고 테스트합니다. 개인화된 필드를 추가한 경우 테스트 프로필 데이터를 사용하여 해당 필드가 표시되는 방식을 확인할 수 있습니다."

콘텐츠를 미리 보거나 테스트하기 전에 먼저 정의된 타겟팅 기준과 일치하지 않는 추가 수신자인 테스트 프로필을 선택해야 합니다. [테스트 프로필을 만드는 방법을 알아봅니다](../audience/creating-test-profiles.md)

>[!NOTE]
>
>테스트 프로필 외에도 [!DNL Journey optimizer]을(를) 사용하면 CSV/JSON 파일에서 업로드하거나 수동으로 추가한 샘플 입력 데이터를 사용하여 콘텐츠를 미리 보고 증명을 전송하여 다양한 변형의 콘텐츠를 테스트할 수도 있습니다. [샘플 입력 데이터를 사용하여 콘텐츠를 테스트하는 방법을 알아보세요](../test-approve/simulate-sample-input.md)

테스트 프로필을 선택하려면 다음 단계를 수행합니다.

1. 메시지의 콘텐츠 편집 화면 또는 이메일 Designer에서 **[!UICONTROL 콘텐츠 시뮬레이션]** 단추를 클릭합니다.

1. **[!UICONTROL 테스트 프로필 관리]** 단추를 클릭한 다음 **[!UICONTROL ID 네임스페이스]** 선택 아이콘을 클릭하여 테스트 프로필을 식별하는 데 사용할 네임스페이스를 선택하십시오. [Adobe Experience Platform ID 네임스페이스에 대해 자세히 알아보기](../audience/get-started-identity.md).

   아래 예제에서는 **이메일** 네임스페이스를 사용합니다.

   ![](../email/assets/previewselect-namespace.png)

1. 검색 필드를 사용하여 네임스페이스를 찾은 다음 **[!UICONTROL 선택]**&#x200B;을(를) 클릭합니다.

   ![](../email/assets/preview-email-namespace.png)

1. **[!UICONTROL ID 값]** 필드에 테스트 프로필을 식별할 값(여기서는 전자 메일 주소)을 입력하고 **[!UICONTROL 프로필 추가]**&#x200B;를 클릭합니다.

   <!--![](assets/preview-identity-value.png)-->

1. 메시지에 개인화를 추가한 경우 프로필 데이터에 따라 메시지의 다양한 변형을 테스트할 수 있도록 다른 프로필을 추가합니다. 추가한 프로필은 선택한 필드 아래에 나열됩니다.

   ![](../email/assets/preview-profile-list.png)

   이 목록은 메시지 개인화 요소를 기반으로 관련 열의 각 테스트 프로필에 대한 데이터를 표시합니다.
