---
title: 콘텐츠 미리 보기 및 테스트
description: 콘텐츠를 미리 보고 테스트하는 방법을 알아봅니다.
feature: Preview, Proofs
role: User
level: Beginner
exl-id: 736fc861-17f2-47b7-8635-9afd261ea3a8
source-git-commit: 4847415fa33ebf1c21622ebf4faecafd4decc8d3
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 98%

---

# 콘텐츠 미리 보기 및 테스트 {#preview-test}

>[!CONTEXTUALHELP]
>id="ac_preview_testprofiles"
>title="콘텐츠 렌더링 방식 확인"
>abstract="콘텐츠가 정의되면 테스트 프로필을 사용하여 콘텐츠를 미리 보고 사용 중인 채널에 따라 렌더링이 올바른지 확인할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_preview_simulate"
>title="콘텐츠 렌더링 방식 확인"
>abstract="콘텐츠가 정의되면 미리 보고 사용 중인 채널에 따라 렌더링이 올바른지 확인할 수 있습니다."

## 미리 보기 및 테스트 정보 {#about}

콘텐츠가 정의되면 메시지를 보내기 전에 콘텐츠를 미리 볼 수 있습니다. 이는 콘텐츠 및 개인화 설정 모두 정확하면서도 오류가 없는지 확인하는 중요한 단계입니다.

또한 테스트 및 유효성 검사를 위해 특정 수신자 또는 구독자에게 이메일 메시지 테스트 게재를 보내고, 널리 쓰이는 데스크탑, 모바일, 웹 기반 클라이언트에서 해당 렌더링을 확인할 수 있습니다.

>[!CAUTION]
>
>메시지를 미리 보거나 증명을 보낼 때에는 프로필 개인화 데이터만 표시됩니다. 이벤트 정보와 같이 컨텍스트 데이터를 기반으로 하는 개인화는 여정 컨텍스트에서만 테스트할 수 있습니다. [이 사용 사례](../personalization/personalization-use-case.md)에서 개인화를 테스트하는 방법을 알아보십시오.

이 모든 작업은 메시지의 콘텐츠 편집 화면이나, 이메일 및 웹 채널의 경우 이메일 및 웹 디자이너에서 액세스할 수 있는 **[!UICONTROL 콘텐츠 시뮬레이션]** 버튼을 사용하여 수행할 수 있습니다.

![](../email/assets/email-preview-button.png)

단, **[!DNL Content Library Manager]** 제품 프로필에 **[!DNL Manage Simulate Content]** 권한이 포함되어 있어야 합니다. [자세히 알아보기](../administration/ootb-product-profiles.md#content-library-manager).

## 테스트 프로필 또는 샘플 입력 데이터를 사용한 테스트 {#methods}

다음을 사용하여 콘텐츠를 미리 보고 테스트할 수 있습니다.

* **테스트 프로필**

  테스트 프로필을 사용하여 콘텐츠를 미리 보고, 이메일 증명을 보내고, 이메일 렌더링을 확인할 수 있습니다. 개인화된 필드를 추가한 경우 테스트 프로필 데이터를 사용하여 해당 필드가 표시되는 방식을 확인할 수 있습니다. 자세한 내용은 다음 섹션을 참조하십시오.

  ➡️ [테스트 프로필 선택](test-profiles.md)

  ➡️ [테스트 프로필을 사용한 콘텐츠 미리 보기](preview.md)

  ➡️ [이메일 증명 보내기](proofs.md)

  ➡️ [이메일 렌더링 확인](rendering.md)

  ➡️0}이메일 미리 보기 및 증명(비디오)](#video-preview)[

* **샘플 입력 데이터**

  [!DNL Journey optimizer]에서는 콘텐츠의 다양한 변형을 테스트하기 위해 CSV/JSON 파일에서 업로드하거나 수동으로 추가한 샘플 입력 데이터를 사용하여 변형을 미리 보고 증명을 전송할 수 있습니다. 

  콘텐츠에서 개인화를 위해 사용되는 모든 프로필 속성은 시스템에서 자동 감지되며, 이를 테스트에 사용하여 여러 변형을 만들 수 있습니다.

  ➡️ [샘플 입력 데이터를 사용하여 콘텐츠를 테스트하는 방법 알아보기](../test-approve/simulate-sample-input.md)

  >[!NOTE]
  >
  >이 기능은 현재 모든 고객이 이메일, SMS, 푸시 알림 채널에서만 공개 Beta 버전으로 사용할 수 있습니다.

## 사용 방법 비디오 {#video-preview}

테스트 프로필을 사용하여 받은 편지함 간에 이메일 렌더링을 테스트하고, 테스트 프로필로 개인화된 이메일을 미리 보고, 증명을 보내는 방법을 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/3425026?quality=12)
