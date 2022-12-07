---
solution: Journey Optimizer
product: journey optimizer
title: 푸시 알림 보내기
description: Journey Optimizer에서 푸시 알림을 미리 보고 테스트하는 방법을 알아봅니다
feature: Overview
topic: Content Management
role: User
level: Beginner
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 0%

---

# 푸시 알림 보내기 {#send-push}

## 푸시 알림 미리 보기 {#preview-push}

메시지 콘텐츠가 정의되면 테스트 프로필을 사용하여 미리 보고 테스트할 수 있습니다. 개인화된 콘텐츠를 삽입한 경우 테스트 프로필 데이터를 활용하여 이 콘텐츠가 메시지에 표시되는 방식을 확인할 수 있습니다.

1. 클릭 **[!UICONTROL 컨텐츠 시뮬레이션]**.

1. 클릭 **[!UICONTROL 테스트 프로필 관리]** 테스트 프로필을 추가하려면

1. 를 사용하여 테스트 프로필 찾기 **[!UICONTROL ID 네임스페이스]** 및 **[!UICONTROL ID 값]** 필드. 그런 다음 **[!UICONTROL 프로필 추가]**.

   ![](assets/push_preview_1.png)

1. 위에 설명된 것과 동일한 단계를 적용하여 테스트 프로필을 선택하고

   ![](assets/push_preview_2.png)

1. 푸시 미리 보기에서 테스트 프로필 데이터는 메시지 콘텐츠에서 활용됩니다.

   컨텐츠를 미리 볼 장치 유형을 선택합니다. **[!UICONTROL iOS]** 또는 **[!UICONTROL Android]**.

   ![](assets/push_preview_3.png)

## 푸시 알림 유효성 검사 {#push-validate}

>[!NOTE]
>
> 보다 나은 게재 능력을 위해 항상 공급자가 지원하는 형식으로 전화 번호를 사용해야 합니다. 예를 들어, Twilio 및 Sinch는 E.164 형식의 전화 번호만 지원합니다.

편집기의 상단 섹션에서도 경고를 확인해야 합니다.  일부 경고는 간단한 경고이지만 일부 사용자는 메시지를 사용하지 못하도록 할 수 있습니다. 다음 두 가지 유형의 경고가 발생할 수 있습니다.

* **경고** 권장 사항 및 우수 사례를 참조하십시오.

* **오류** 다음과 같이 여정이 해결되지 않는 한 테스트하거나 활성화할 수 없습니다.

   * **[!UICONTROL 메시지의 푸시 버전이 비어 있습니다]**: 이 오류는 푸시 알림 본문 또는 제목이 누락된 경우 표시됩니다. 에서 푸시 알림 콘텐츠를 정의하는 방법을 알아봅니다. [이 섹션](create-push.md).

   * **[!UICONTROL 서피스가 없습니다.]**: 메시지 생성 후 선택한 서피스가 삭제되면 메시지를 사용할 수 없습니다. 이 오류가 발생하면 메시지에서 다른 서피스를 선택합니다 **[!UICONTROL 속성]**. 의 채널 표면에 대해 자세히 알아보기 [이 섹션](../configuration/channel-surfaces.md).

   * **[!UICONTROL 푸시 iOS/Android 페이로드가 4KB의 제한을 초과했습니다]**: 푸시 알림 크기는 4KB를 초과할 수 없습니다. 이 제한을 준수하려면 이미지나 이모지의 사용을 줄이십시오. 에서 푸시 알림 콘텐츠를 관리하는 방법을 알아봅니다 [이 섹션](../push/create-push.md).

![](assets/push_alert.png)

푸시 알림이 준비되면 구성을 완료하십시오 [여정](../building-journeys/journey-gs.md) 또는 [campaign](../campaigns/create-campaign.md) 전송하기 위해

