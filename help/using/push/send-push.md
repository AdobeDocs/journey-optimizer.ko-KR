---
solution: Journey Optimizer
product: journey optimizer
title: 푸시 알림 미리 보기 및 테스트
description: Journey Optimizer에서 푸시 알림을 미리 보고 테스트하는 방법을 알아봅니다
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: aad4e08a-3369-454d-9e32-974347a3b393
source-git-commit: 81ab92022329788c1feea24c7a621ef154d33422
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 9%

---

# 푸시 알림 미리 보기 및 테스트 {#send-push}

## 푸시 알림 미리 보기 {#preview-push}

메시지가 정의되면 테스트 프로필을 사용하여 미리 보고 테스트할 수 있습니다. 개인화된 콘텐츠를 삽입한 경우 테스트 프로필 데이터를 활용하여 이 콘텐츠가 메시지에 어떻게 표시되는지 확인할 수 있습니다.

1. 클릭 **[!UICONTROL 콘텐츠 시뮬레이션]**.

1. 클릭 **[!UICONTROL 테스트 프로필 관리]** 테스트 프로필을 추가합니다.

1. 을(를) 사용하여 테스트 프로필 찾기 **[!UICONTROL ID 네임스페이스]** 및 **[!UICONTROL ID 값]** 필드. 그런 다음 을 클릭합니다. **[!UICONTROL 프로필 추가]**.

   ![](assets/push_preview_1.png)

1. 테스트 프로필을 선택하면 **[!UICONTROL 테스트 프로필 추가]** 창.

1. 다음에서 **미리 보기 및 테스트** 창, 테스트 프로필 데이터가 메시지 콘텐츠에 추가됩니다.

   콘텐츠를 미리 볼 장치 유형 선택: **[!UICONTROL iOS]** 또는 **[!UICONTROL Android]**.

   ![](assets/push_preview_3.png)

## 푸시 알림 유효성 확인 {#push-validate}


편집기의 위쪽 섹션에서 경고를 확인해야 합니다. 일부는 간단한 경고이지만 일부는 메시지를 보내지 못하게 할 수 있습니다. 경고와 오류의 두 가지 경고 유형이 발생할 수 있습니다.

* **경고** 권장 사항 및 모범 사례를 참조하십시오.

* **오류** 여정이 해결되지 않으면 다음과 같이 테스트를 수행하거나 활성화할 수 없습니다.

   * **[!UICONTROL 메시지의 푸시 버전이 비어 있음]**: 이 오류는 푸시 알림 본문 또는 제목이 누락된 경우 표시됩니다. 에서 푸시 알림 콘텐츠를 정의하는 방법 알아보기 [이 섹션](create-push.md).

   * **[!UICONTROL 표면이 존재하지 않음]**: 메시지를 만든 후 선택한 표면이 삭제되면 메시지를 사용할 수 없습니다. 이 오류가 발생하면 메시지에서 다른 서피스를 선택합니다 **[!UICONTROL 속성]**. 의 채널 표면에 대해 자세히 알아보기 [이 섹션](../configuration/channel-surfaces.md).

   * **[!UICONTROL 푸시 iOS/Android 페이로드가 4KB 제한을 초과했습니다.]**: 푸시 알림 크기는 4KB를 초과할 수 없습니다. 이 제한을 준수하려면 이미지 또는 이모지의 사용을 줄이십시오. 에서 푸시 알림 콘텐츠를 관리하는 방법 알아보기 [이 섹션](../push/create-push.md).

   ![](assets/push_alert.png)


>[!NOTE]
>
> 더 나은 전달성을 위해 공급자가 지원하는 형식의 전화 번호를 항상 사용해야 합니다. 예를 들어 Twilio와 Sinch는 E.164 형식의 전화 번호만 지원합니다.

## 푸시 알림 보내기{#push-send}

푸시 메시지가 준비되면 의 구성을 완료합니다. [여정](../building-journeys/journey-gs.md) 또는 [campaign](../campaigns/create-campaign.md) 보낼 수 있습니다.

**관련 항목**

* [푸시 채널 구성](push-configuration.md)
* [푸시 알림 보고서](../reports/journey-global-report.md#push-global)
* [푸시 알림 만들기](create-push.md)
* [여정에 메시지 추가](../building-journeys/journeys-message.md)
* [캠페인에 메시지 추가](../campaigns/create-campaign.md)

