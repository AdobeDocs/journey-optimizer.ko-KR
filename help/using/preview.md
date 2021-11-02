---
title: 메시지 미리 보기 및 증명 보내기
description: 메시지를 미리 보고 테스트하는 방법을 알아봅니다
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: f2c2a360-a4b2-4416-bbd0-e27dd014e4ac
source-git-commit: a9e65986c3ccd0dc54a54bc5f349f5c9c87c5039
workflow-type: tm+mt
source-wordcount: '1023'
ht-degree: 3%

---

# 메시지 미리 보기 및 테스트{#preview-and-proof}

메시지 콘텐츠가 정의되면 테스트 프로필을 사용하여 미리 보고 테스트할 수 있습니다. 삽입한 경우 [개인화된 콘텐츠](personalization/personalize.md)를 입력하면 테스트 프로필 데이터를 활용하여 이 콘텐츠가 메시지에 어떻게 표시되는지 확인할 수 있습니다.

이메일 콘텐츠 또는 개인화 설정에서 가능한 오류를 탐지하려면 테스트 프로필에 증명을 보냅니다. 최신 콘텐츠를 확인하려면 변경 사항이 있을 때마다 증명을 보내야 합니다.

>[!CAUTION]
>
>메시지를 미리 보고 증명을 보내려면 테스트 프로필을 사용할 수 있어야 합니다.
>
>에서 테스트 프로필을 만드는 방법을 알아봅니다. [이 페이지](building-journeys/creating-test-profiles.md).

메시지 콘텐츠를 테스트하려면 다음을 수행해야 합니다.

* [테스트 프로필 선택](#select-test-profiles)
* [메시지 미리 보기 확인](#preview-your-messages)

그러면 다음을 수행할 수 있습니다 [증명 보내기](#send-proofs) 테스트 프로필로 이동합니다.

또한 **리트머스** 계정 [!DNL Journey Optimizer] 즉시 미리 보려면 **전자 메일 렌더링** 인기 있는 이메일 클라이언트에서 그런 다음 모든 받은 편지함에서 전자 메일 콘텐츠가 제대로 표시되고 제대로 작동하는지 확인할 수 있습니다. 에서 리트머스 전자 메일 미리 보기의 잠금을 해제하는 방법을 알아봅니다. [이 섹션](#email-rendering)

>[!CAUTION]
>
>메시지를 미리 보거나 증명을 보낼 때 프로필 개인화 데이터만 표시됩니다. 이벤트 정보와 같은 컨텍스트 데이터를 기반으로 한 개인화는 여정 컨텍스트에서만 테스트할 수 있습니다. 에서 개인화를 테스트하는 방법을 알아봅니다. [이 사용 사례](personalization/personalization-use-case.md).

➡️ [이 비디오에서 이메일을 미리 보고, 증명을 하고, 게시하는 방법을 알아봅니다](#video-preview)

## 테스트 프로필 선택{#select-test-profiles}

>[!CONTEXTUALHELP]
>id="ac_preview_testprofiles"
>title="메시지 미리 보기 및 테스트"
>abstract="메시지 콘텐츠가 정의되면 테스트 프로필을 사용하여 미리 보고 테스트할 수 있습니다."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/create-messages/create-message/preview.html?lang=en#email-rendering" text="이메일 렌더링"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/create-messages/create-message/preview.html?lang=en#preview-your-messages" text="미리 보기"



사용 [테스트 프로필](building-journeys/creating-test-profiles.md) 정의한 타겟팅 기준과 일치하지 않는 추가 수신자를 타겟팅합니다.

테스트 프로필을 선택하려면 아래 단계를 수행하십시오.

1. 메시지 인터페이스 또는 이메일 디자이너에서 **[!UICONTROL Show preview]** 테스트 프로필 선택에 액세스하는 단추입니다.

   ![](assets/email-preview-button.png)

1. 을(를) 클릭하여 테스트 프로필을 식별하는 데 사용할 네임스페이스를 선택합니다 **[!UICONTROL Identity namespace]** 선택 아이콘.

   ![](assets/previewselect-namespace.png)

   Adobe Experience Platform ID 네임스페이스에 대해 자세히 알아보십시오 [이 섹션](get-started-identity.md){target=&quot;_blank&quot;}.

   아래 예에서는 **이메일** 네임스페이스.

1. 검색 필드를 사용하여 네임스페이스를 찾아 선택하고 을(를) 클릭합니다 **[!UICONTROL Select]**

   ![](assets/preview-email-namespace.png)

1. 테스트 프로필을 식별할 값을 입력하고 **[!UICONTROL Find test profile]**.

   ![](assets/preview-identity-value.png)

1. 메시지에 개인화를 추가한 경우 프로필 데이터에 따라 메시지의 다른 변형을 테스트할 수 있도록 다른 프로필을 추가하십시오. 추가한 프로필은 선택 필드 아래에 나열됩니다.

   ![](assets/preview-profile-list.png)

   메시지 개인화 요소를 기반으로 이 목록에는 관련 열의 각 테스트 프로필에 대한 데이터가 표시됩니다.

## 메시지 미리 보기{#preview-your-messages}

한 번 [테스트 프로필](#select-test-profiles) 이 옵션을 선택하면 메시지를 미리 보고 콘텐츠를 확인할 수 있습니다.

1. 을(를) 클릭합니다. **[!UICONTROL Preview]** 탭을 클릭하여 메시지를 테스트합니다.

1. 테스트 프로필을 선택합니다. 열에서 사용할 수 있는 값을 확인할 수 있습니다. 데이터를 검색하려면 오른쪽/왼쪽 화살표를 사용합니다.

   ![](assets/preview-tab-select-profile.png)

1. 을(를) 클릭합니다. **[!UICONTROL Select data]** 아이콘 위로 클릭하여 열을 추가하거나 제거합니다.

   ![](assets/preview-select-data.png)

   목록 맨 뒤에는 현재 메시지에 해당하는 개인화 필드가 표시됩니다. 이 예에서는 프로필 도시, 이름 및 성이 있습니다. 이러한 필드를 선택하고 이러한 값이 테스트 프로필에 채워졌는지 확인합니다.

1. 메시지 미리 보기에서 개인화된 요소는 선택한 테스트 프로필 데이터로 대체됩니다.

   예를 들어 이 메시지의 경우 이메일 콘텐츠와 이메일 제목이 모두 개인화됩니다.

   ![](assets/preview-test-profile.png)

1. 다른 테스트 프로필을 선택하여 메시지의 각 변형에 대한 이메일 렌더링을 미리 봅니다.

푸시 알림 미리 보기의 경우:

1. 로 전환 **[!UICONTROL Push]** 채널에서 **[!UICONTROL Channels]** 오른쪽 상단의 드롭다운 목록 **[!UICONTROL Preview]** 화면.

   ![](assets/preview-select-channel.png)

1. 위에 설명된 것과 동일한 단계를 적용하여 테스트 프로필을 선택하고 컨텐츠를 미리 볼 장치 유형을 선택합니다. **[!UICONTROL iOS]** 또는 **[!UICONTROL Android]**

   ![](assets/preview-iOS.png)

1. 푸시 미리 보기에서 테스트 프로필 데이터는 메시지 콘텐츠에서 활용됩니다.

   예를 들어 이 푸시 알림의 경우 제목과 본문은 모두 개인화됩니다.

   ![](assets/preview-android.png)

## 증명 보내기{#send-proofs}

증명은 메시지를 주요 대상자에게 보내기 전에 테스트하기 위한 특정 메시지입니다. 증명의 수신자는 메시지를 승인해야 합니다. 렌더링, 컨텐츠, 개인화 설정, 구성

한 번 [테스트 프로필](#select-test-profiles) 을(를) 선택하면 증명을 보낼 수 있습니다.

1. 에서 **[!UICONTROL Preview]** 화면에서 **[!UICONTROL Send proof]** 버튼을 클릭합니다.

   ![](assets/send-proof-button.png)

1. 에서 **[!UICONTROL Send proof]** 창을 열고 수신자 전자 메일을 입력하고 **[!UICONTROL Add]** 본인 또는 조직의 구성원에게 증명을 전송하기 위해

   증명 전달을 위해 최대 10명의 수신자를 추가할 수 있습니다.

   ![](assets/send-proof-button_2.png)

1. 그런 다음 **테스트 프로필** 메시지 콘텐츠를 개인화하는 데 사용됩니다.

   증명의 각 수신자는 선택한 테스트 프로필 수만큼 메시지를 수신합니다. 예를 들어 5개의 수신자 이메일을 추가하고 10개의 테스트 프로필을 선택한 경우 50개의 증명 메시지를 받게 되며 각 수신자에게는 10개의 메시지를 받게 됩니다.

1. 필요한 경우 증명의 제목란에 접두사를 추가할 수 있습니다. 영숫자 문자 및 특수 문자(예: . - _ ( ) 만 사용할 수 있습니다. [ ]는 제목란에 접두사로 사용할 수 있습니다.

1. **[!UICONTROL Send proof]**&#x200B;을(를) 클릭합니다.

   ![](assets/send-proof-select.png)

1. 다시  **[!UICONTROL Preview]** 화면에서  **[!UICONTROL View proofs]** 상태를 확인하는 단추입니다.

   ![](assets/send-proof-view.png)

메시지 콘텐츠를 매번 수정한 후 증명을 보내는 것이 좋습니다.

>[!NOTE]
>
>테스트 프로필로 전송된 증명의 경우 미러 페이지에 대한 링크가 활성화되지 않습니다. 최종 메시지에서만 활성화됩니다.

## 이메일 렌더링{#email-rendering}

을(를) 활용할 수 있습니다 **리트머스** 계정 [!DNL Journey Optimizer] 즉시 미리 보려면 **전자 메일 렌더링** 인기 있는 이메일 클라이언트에서

전자 메일 렌더링 기능에 액세스하려면 다음을 수행해야 합니다.

* 리트머스 계정을 보유합니다.
* [테스트 프로필 선택](#select-test-profiles)

그런 다음 아래 단계를 수행합니다.

1. 이메일 디자이너에서 **[!UICONTROL Preview]** 버튼을 클릭하고 **[!UICONTROL Email rendering]** 탭.

1. 클릭 **리트머스 계정 연결** 오른쪽 상단입니다.

   ![](assets/email-rendering-litmus.png)

1. 자격 증명을 입력하고 로그인합니다.

   ![](assets/email-rendering-credentials.png)

1. 을(를) 클릭합니다. **테스트 실행** 전자 메일 미리 보기를 생성하는 단추입니다.

1. 인기 있는 데스크탑, 모바일 및 웹 기반 클라이언트에서 이메일 콘텐츠를 확인합니다.

   ![](assets/email-rendering-previews.png)

>[!CAUTION]
>
>연결 시 **리트머스** 계정 [!DNL Journey Optimizer]: 테스트 메시지를 Litmus로 전송하는 것에 동의합니다. 전송되면 이러한 이메일은 더 이상 Adobe에서 관리하지 않습니다. 따라서 Litmus 데이터 보존 이메일 정책은 이러한 테스트 메시지에 포함될 수 있는 개인화 데이터를 포함하여 이러한 이메일에 적용됩니다.

## 방법 비디오{#video-preview}

여러 받은 편지함에 걸쳐 이메일 렌더링을 테스트하고, 테스트 프로필에 따라 개인화 이메일을 미리 보고, 교정쇄를 보내고, 이메일을 게시하는 방법을 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/334239?quality=12)
