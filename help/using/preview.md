---
title: 메시지 미리 보기 및 교정본 보내기
description: 메시지를 미리 보고 테스트하는 방법 학습
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 2%

---

# 메시지 미리 보기 및 테스트{#preview-and-proof}

![](assets/do-not-localize/badge.png)

메시지 내용이 정의된 후 테스트 프로필을 사용하여 미리 보고 테스트할 수 있습니다. [개인화된 컨텐츠](personalization/personalize.md)를 삽입한 경우 테스트 프로필 데이터를 활용하여 이 컨텐츠가 메시지에 어떻게 표시되는지 확인할 수 있습니다.

이메일 컨텐츠 또는 개인화 설정에서 가능한 오류를 탐지하려면 테스트 프로파일에 교정본을 보냅니다. 최신 컨텐츠를 확인하기 위해 변경 사항이 있을 때마다 증명 자료를 보내야 합니다.

>[!CAUTION]
>
>메시지를 미리 보고 교정을 전송할 수 있도록 테스트 프로파일을 사용할 수 있어야 합니다. [자세히 알아보기](building-journeys/testing-the-journey.md#create-test-profile).

메시지 내용을 테스트하려면 다음을 수행해야 합니다.

* [테스트 프로필 선택](#select-test-profiles)
* [메시지 미리 보기 확인](#preview-your-messages)

그러면 [교정본을 테스트 프로파일에 보내기](#send-proofs)할 수 있습니다.

또한 **리트머스** 계정을 [!DNL Journey Optimizer]에 활용하여 인기 있는 이메일 클라이언트에서 **이메일 렌더링**&#x200B;을 즉시 미리 봅니다. 이메일 컨텐츠가 모든 받은 편지함에서 올바로 표시되고 작동하는지 확인할 수 있습니다. [이 섹션](#email-rendering)에서 리트머스 이메일 미리 보기의 잠금을 해제하는 방법을 알아봅니다.

## 테스트 프로필 선택{#select-test-profiles}

테스트 프로필을 사용하면 정의한 타겟팅 기준과 일치하지 않는 추가 수신자를 타겟팅할 수 있습니다.

테스트 프로필을 선택하려면 아래 단계를 수행합니다.

1. 메시지 인터페이스 또는 이메일 디자이너에서 **[!UICONTROL Preview]** 단추를 클릭하여 테스트 프로필 선택에 액세스합니다.

   ![](assets/email-preview-button.png)

1. **[!UICONTROL Identity namespace]** 선택 아이콘을 클릭하여 테스트 프로필을 식별하는 데 사용할 네임스페이스를 선택합니다.

   ![](assets/previewselect-namespace.png)

   이 섹션](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html?lang=en#getting-started)에서 Adobe Experience Platform ID 네임스페이스 [에 대해 자세히 알아보십시오.

   아래 예에서는 **이메일** 네임스페이스를 사용합니다.

1. 검색 필드를 사용하여 네임스페이스를 찾아 선택하고 **[!UICONTROL Select]**

   ![](assets/preview-email-namespace.png)

1. 테스트 프로필을 식별할 값을 입력하고 **[!UICONTROL Find test profile]**&#x200B;을 클릭합니다.

   ![](assets/preview-identity-value.png)

1. 메시지에 개인화를 추가한 경우 프로필 데이터에 따라 메시지의 다른 변형을 테스트할 수 있도록 다른 프로필을 추가하십시오. 프로필이 추가되면 선택 필드 아래에 나열됩니다.

   ![](assets/preview-profile-list.png)

   메시지 개인화 요소를 기반으로 이 목록은 관련 열에 있는 각 테스트 프로필에 대한 데이터를 표시합니다.

## 메시지 미리 보기{#preview-your-messages}

[테스트 프로필](#select-test-profiles)이 선택되면 메시지를 미리 보고 내용을 확인할 수 있습니다.

1. 메시지를 테스트하려면 **[!UICONTROL Preview]** 탭을 클릭합니다.

1. 테스트 프로필을 선택합니다. 열에서 사용할 수 있는 값을 확인할 수 있습니다. 오른쪽/왼쪽 화살표를 사용하여 데이터를 검색합니다.

   ![](assets/preview-tab-select-profile.png)

1. 열을 추가하거나 제거하려면 목록 위의 **[!UICONTROL Select data]** 아이콘을 클릭합니다.

   ![](assets/preview-select-data.png)

   목록 끝에 현재 메시지에 해당하는 개인화 필드가 표시됩니다. 이 예에서는 프로필 도시, 이름 및 성을 나타냅니다. 이러한 필드를 선택하고 이 값이 테스트 프로필에 채워졌는지 확인합니다.

1. 메시지 미리 보기에서 개인화된 요소는 선택한 테스트 프로필 데이터로 바뀝니다.

   예를 들어, 이 메시지의 경우 이메일 컨텐츠와 이메일 제목이 모두 개인화됩니다.

   ![](assets/preview-test-profile.png)

1. 메시지의 각 변형에 대한 이메일 렌더링을 미리 보려면 다른 테스트 프로필을 선택합니다.

푸시 알림 미리 보기의 경우:

1. **[!UICONTROL Preview]** 화면의 왼쪽 상단에 있는 **[!UICONTROL Channels]** 드롭다운 목록에서 **[!UICONTROL Push]** 채널로 전환합니다.

   ![](assets/preview-select-channel.png)

1. 위에서 설명한 것과 동일한 단계를 적용하여 테스트 프로필을 선택하고 컨텐츠를 미리 볼 장치 유형을 선택합니다.**[!UICONTROL iOS]** 또는 **[!UICONTROL Android]**

   ![](assets/preview-iOS.png)

1. 푸시 미리 보기에서 테스트 프로필 데이터는 메시지 컨텐츠에서 활용됩니다.

   예를 들어 이 푸시 알림의 경우 제목과 본문은 모두 개인화됩니다.

   ![](assets/preview-android.png)

## 증거 자료 보내기{#send-proofs}

증명은 메시지를 기본 대상자에게 보내기 전에 테스트할 수 있도록 하는 특정 메시지입니다. 문서 받는 사람은 다음 메시지를 승인합니다.렌더링, 컨텐츠, 개인화 설정, 구성.

[테스트 프로필](#select-test-profiles)이 선택되면 교정본을 보낼 수 있습니다.

1. **[!UICONTROL Preview]** 화면에서 **[!UICONTROL Send proof]** 단추를 클릭합니다.

   ![](assets/send-proof-button.png)

1. 증명을 받을 테스트 프로필을 선택하고 **[!UICONTROL Send proof]**&#x200B;을 클릭합니다. 필요한 경우 교정기의 제목 줄에 접두사를 추가할 수 있습니다.

   ![](assets/send-proof-select.png)

1. **[!UICONTROL Preview]** 화면으로 돌아가 **[!UICONTROL View proofs]** 단추를 클릭하여 상태를 확인합니다.

   ![](assets/send-proof-view.png)

메시지 내용을 수정한 후 교정본을 보내야 합니다.

## 전자 메일 렌더링{#email-rendering}

**리트머스** 계정을 [!DNL Journey Optimizer]에 활용하여 인기 있는 이메일 클라이언트에서 **이메일 렌더링**&#x200B;을 즉시 미리 볼 수 있습니다.

이메일 렌더링 기능에 액세스하려면 다음을 수행해야 합니다.

* 리트머스 계정 만들기
* [테스트 프로필 선택](#select-test-profiles)

그런 다음 아래 단계를 수행하십시오.

1. 이메일 디자이너에서 **[!UICONTROL Preview]** 단추를 클릭하고 **[!UICONTROL Email rendering]** 탭을 선택합니다.

1. 오른쪽 위 섹션에서 **리트머스 계정 연결**&#x200B;을 클릭합니다.

   ![](assets/email-rendering-litmus.png)

1. 자격 증명을 입력하고 로그인합니다.

   ![](assets/email-rendering-credentials.png)

1. 이메일 미리 보기를 생성하려면 **테스트 실행** 단추를 클릭합니다.

1. 널리 사용되는 데스크탑, 모바일 및 웹 기반 클라이언트에서 이메일 컨텐츠를 확인할 수 있습니다.

   ![](assets/email-rendering-previews.png)

>[!CAUTION]
>
>**리트머스** 계정을 [!DNL Journey Optimizer]에 연결할 때 테스트 메시지가 리트머스:한 번 전송되면 이러한 이메일은 더 이상 Adobe에서 관리하지 않습니다. 그 결과, 리트머스 데이터 유지 이메일 정책은 이러한 테스트 메시지에 포함될 수 있는 개인화 데이터를 포함하여 이러한 이메일에 적용됩니다.

