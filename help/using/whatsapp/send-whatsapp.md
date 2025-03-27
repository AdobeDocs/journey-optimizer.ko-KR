---
solution: Journey Optimizer
product: journey optimizer
title: WhatsApp 메시지 확인 및 테스트
description: Journey Optimizer에서 WhatsApp 메시지를 확인하고 보내는 방법을 알아봅니다
feature: WhatsApp
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
badge: label="Beta" type="Informative"
source-git-commit: 7ca149d420f802a6230e699cffefddc4117cb85e
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 2%

---

# WhatsApp 메시지 확인 및 보내기 {#send-whatsapp}

>[!BEGINSHADEBOX]

**목차**

* [WhatsApp 메시지 시작](get-started-whatsapp.md)
* [WhatsApp 구성 시작](whatsapp-configuration.md)
* [WhatsApp 메시지 만들기](create-whatsapp.md)
* **[WhatsApp 메시지 확인 및 보내기](send-whatsapp.md)**

>[!ENDSHADEBOX]

## WhatsApp 메시지 미리 보기 {#preview-whatsapp}

메시지 콘텐츠가 정의되면 테스트 프로필 또는 CSV/JSON 파일에서 업로드한 샘플 입력 데이터 또는 수동으로 추가한 샘플 입력 데이터를 사용하여 콘텐츠를 미리 볼 수 있습니다. 개인화된 콘텐츠를 삽입하면 이 콘텐츠가 메시지에 어떻게 표시되는지 확인할 수 있습니다. [샘플 입력 데이터를 사용하여 콘텐츠를 테스트하는 방법을 알아보세요](../test-approve/simulate-sample-input.md)

이렇게 하려면 **[!UICONTROL 콘텐츠 시뮬레이션]**&#x200B;을 클릭한 다음 테스트 프로필 데이터를 사용하여 메시지를 확인하세요.

콘텐츠를 미리 보고 테스트하는 방법에 대한 자세한 내용은 [콘텐츠 관리](../content-management/preview-test.md) 섹션에서 확인할 수 있습니다.

## 콘텐츠 유효성 검사 {#whatsapp-validate}

편집기의 위쪽 섹션에서 경고를 확인해야 합니다. 일부는 간단한 경고이지만 일부는 메시지를 보내지 못하게 할 수 있습니다. 경고와 오류의 두 가지 경고 유형이 발생할 수 있습니다.

* **경고**&#x200B;는 권장 사항과 모범 사례를 참조합니다. 예를 들어 텍스트 메시지가 비어 있는 경우 경고 메시지가 표시됩니다.

* **오류**&#x200B;로 인해 여정을 테스트 또는 활성화하거나 캠페인을 게시하지 못할 수 있습니다. 단, 해결되지 않는 한 가능합니다. 예를 들어 제목 줄이 누락된 경우 경고 메시지가 표시됩니다.

## WhatsApp 메시지 보내기 {#whatsapp-send}

>[!IMPORTANT]
>
> 캠페인이 승인 정책의 적용을 받는 경우 문자 메시지를 보내려면 승인을 요청해야 합니다. [자세히 알아보기](../test-approve/gs-approval.md)

WhatsApp 메시지가 준비되면 [여정](../building-journeys/publishing-the-journey.md) 또는 [캠페인](../campaigns/review-activate-campaign.md)의 구성을 완료하여 보내십시오.
