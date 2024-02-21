---
solution: Journey Optimizer
product: journey optimizer
title: 문자 메시지 확인 및 테스트
description: Journey Optimizer에서 문자 메시지를 확인하고 보내는 방법 알아보기
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: 31c9b080-e334-4a11-af33-4c6f115c70a4
source-git-commit: f275820c3f79bb4c9aca8593c2c761ccd4283795
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 3%

---

# 문자 메시지 확인 및 보내기 {#send-sms}

## 문자 메시지 미리 보기 {#preview-sms}

메시지 콘텐츠가 정의되면 테스트 프로필을 사용하여 콘텐츠를 미리 볼 수 있습니다. 개인화된 콘텐츠를 삽입한 경우 테스트 프로필 데이터를 활용하여 이 콘텐츠가 메시지에 어떻게 표시되는지 확인할 수 있습니다.

이렇게 하려면 다음을 클릭하십시오. **[!UICONTROL 콘텐츠 시뮬레이션]** 그런 다음 테스트 프로필을 추가하여 테스트 프로필 데이터를 사용하여 메시지를 확인합니다.

![](assets/sms_preview_2.png)

테스트 프로필을 선택하고 콘텐츠를 미리 보는 방법에 대한 자세한 내용은 [콘텐츠 관리](../content-management/preview-test.md) 섹션.

## 콘텐츠 유효성 검사 {#sms-validate}

편집기의 위쪽 섹션에서 경고를 확인해야 합니다. 일부는 간단한 경고이지만 일부는 메시지를 보내지 못하게 할 수 있습니다. 경고와 오류의 두 가지 경고 유형이 발생할 수 있습니다.

![](assets/sms-alert-button.png)

* **경고** 권장 사항 및 모범 사례를 참조하십시오. 예를 들어 텍스트 메시지가 비어 있는 경우 경고 메시지가 표시됩니다.

* **오류** 해결되지 않는 한 여정을 테스트 또는 활성화하거나 캠페인을 게시하지 못하도록 합니다. 예를 들어 제목 줄이 누락된 경우 경고 메시지가 표시됩니다.


>[!NOTE]
>
> 전달성을 향상시키려면 공급자가 지원하는 형식의 전화 번호를 사용하십시오. 예를 들어 Twilio와 Sinch는 E.164 형식의 전화 번호만 지원합니다.

## 문자 메시지 보내기 {#sms-send}

문자 메시지가 준비되면 구성을 완료합니다. [여정](../building-journeys/journey-gs.md) 또는 [campaign](../campaigns/create-campaign.md) 보낼 수 있습니다.

**관련 항목**

* [SMS 채널 구성](sms-configuration.md)
* [SMSS 보고서](../reports/journey-global-report.md#sms-global)
* [텍스트 메시지 만들기](create-sms.md)
* [여정에 메시지 추가](../building-journeys/journeys-message.md)
