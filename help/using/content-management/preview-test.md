---
title: 콘텐츠 미리 보기 및 테스트
description: 콘텐츠를 미리 보고 테스트하는 방법을 알아봅니다.
feature: Preview, Proofs
role: User
level: Beginner
exl-id: 736fc861-17f2-47b7-8635-9afd261ea3a8
source-git-commit: aa28d13b2ad874e4dc61510bfdc250415e8e8be1
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 100%

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

콘텐츠가 정의되면 메시지를 보내기 전에 콘텐츠를 미리 볼 수 있습니다. 이는 콘텐츠 및 개인화 설정 모두 정확하면서도 오류가 없는지 확인하는 중요한 단계입니다.

또한 테스트 및 유효성 검사를 위해 특정 수신자 또는 구독자에게 이메일 메시지 테스트 게재를 보내고, 널리 쓰이는 데스크탑, 모바일, 웹 기반 클라이언트에서 해당 렌더링을 확인할 수 있습니다.

이 모든 작업은 메시지의 콘텐츠 편집 화면이나, 이메일 및 웹 채널의 경우 이메일 및 웹 디자이너에서 액세스할 수 있는 **[!UICONTROL 콘텐츠 시뮬레이션]** 버튼을 사용하여 수행할 수 있습니다.

![](../email/assets/email-preview-button.png)

## 테스트 프로필 데이터 또는 샘플 입력 데이터를 사용한 테스트 {#methods}

Journey Optimizer는 콘텐츠를 테스트할 수 있는 두 가지 경험을 제공합니다.

* **테스트 프로필 데이터를 사용하여 콘텐츠 테스트**

  테스트 프로필을 사용하여 콘텐츠를 미리 보고, 이메일 증명을 보내고, 이메일 렌더링을 확인할 수 있습니다. 개인화된 필드를 추가한 경우, 테스트 프로필 데이터를 사용하여 해당 필드가 표시되는 방식을 확인할 수 있습니다. 자세한 내용은 다음 섹션을 참조하십시오.

  ➡️ [테스트 프로필 선택](test-profiles.md)
➡️ [테스트 프로필을 사용하여 미리 보기](preview.md)
➡️ [이메일 증명 보내기](proofs.md)
➡️ [이메일 렌더링 확인](rendering.md)
➡️ [이메일 미리 보기 및 증명(비디오)](#video-preview)

* **샘플 입력 데이터를 사용하여 콘텐츠 베리에이션 테스트**

  [!DNL Journey optimizer]에서는 CSV/JSON 파일에서 업로드하거나 수동으로 추가한 샘플 입력 데이터를 사용하여 콘텐츠의 다양한 베리에이션을 미리 보고 증명을 전송할 수 있습니다. 

  콘텐츠에서 개인화를 위해 사용되는 모든 프로필 속성은 시스템에서 자동 감지되며, 이를 테스트에 사용하여 여러 변형을 만들 수 있습니다.

  ➡️ [콘텐츠 베리에이션 시뮬레이션](../test-approve/simulate-sample-input.md)

## 반드시 알아야 할 사항

* **필요한 권한** - **[!DNL Content Library Manager]** 제품 프로필에 **[!DNL Manage Simulate Content]** 권한이 포함되어 있어야 합니다. [자세히 알아보기](../administration/ootb-product-profiles.md#content-library-manager).

  증명을 보내려면 이메일과 연결된 특정 리소스(캠페인 또는 여정)에 대해 **승인 및 게시** 권한이 있어야 합니다. 또한 여정에서 증명을 보내려면 **여정 게시** 권한도 필요합니다. [권한에 대해 자세히 알아보십시오](../administration/ootb-permissions.md).

* **컨텍스트 데이터를 사용한 개인화** - 메시지를 미리 보거나 증명을 보낼 때에는 프로필 개인화 데이터만 표시됩니다. 이벤트 정보와 같이 컨텍스트 데이터를 기반으로 하는 개인화는 여정 컨텍스트에서만 테스트할 수 있습니다. [이 사용 사례](../personalization/personalization-use-case.md)에서 방법을 알아보십시오.

* **여러 조건부 베리에이션이 있는 콘텐츠 미리 보기** - 여러 조건부 베리에이션이 포함된 이메일에 대한 증명을 시뮬레이션 또는 렌더링할 때는 Journey Optimizer에 처리 시간이 더 필요할 수 있습니다. 시간이 초과되거나 오류 메시지가 표시되면 총 베리에이션 수를 줄이거나 조건부 규칙을 단순화하는 것이 좋습니다. [이 페이지](../personalization/dynamic-content.md)에서 조건부 콘텐츠에 대해 자세히 알아보십시오.

## 사용 방법 비디오 {#video-preview}

테스트 프로필을 사용하여 받은 편지함 간에 이메일 렌더링을 테스트하고, 테스트 프로필로 개인화된 이메일을 미리 보고, 증명을 보내는 방법을 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/3430340?captions=kor&quality=12)
