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
source-git-commit: 7eaca4faf61431fa438afc7550ff4b89f95fa192
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 2%

---

# 문자 메시지 확인 및 보내기(SMS/MMS){#send-sms}

## 문자 메시지 미리 보기 {#preview-sms}

메시지 콘텐츠가 정의되면 테스트 프로필 또는 샘플 입력 데이터(CSV/JSON 파일에서 업로드하거나 수동으로 추가)를 사용하여 콘텐츠를 미리 볼 수 있습니다. 개인화된 콘텐츠를 삽입하면 이 콘텐츠가 메시지에 어떻게 표시되는지 확인할 수 있습니다.

이렇게 하려면 **[!UICONTROL 콘텐츠 시뮬레이션]**&#x200B;을 클릭한 다음 테스트 프로필 데이터를 사용하여 메시지를 확인하세요.

![](assets/sms_preview_2.png)

콘텐츠를 미리 보고 테스트하는 방법에 대한 자세한 내용은 [콘텐츠 관리](../content-management/preview-test.md) 섹션에서 확인할 수 있습니다.

### 문자 인코딩 및 제한 {#sms-character-limits}

문자 수는 SMS 메시지 계획 및 관리를 지원하기 위해 **[!UICONTROL 콘텐츠 시뮬레이션]** 메뉴에 액세스할 때 표시됩니다.

![](assets/sms_preview_3.png)

Journey Optimizer은 SMS 편집기에서 UTF-8 인코딩을 사용하므로 더블바이트 또는 유니코드 문자를 입력하거나 붙여넣을 수 있습니다. 그런 다음 이러한 문자가 전달을 위해 서비스 공급자에게 전송됩니다. 대부분의 SMS 공급자는 160자 제한이 있는 표준 메시지에 GSM 7비트 인코딩을 사용하고, GSM이 아닌 문자가 70자 제한으로 감지되면 UTF-16(UCS-2)으로 전환합니다.

문자 수는 동적 개인화에 의해 도입된 변형 또는 GSM이 아닌 7비트 특수 문자를 반영하지 않습니다.

>[!IMPORTANT]
>
>Journey Optimizer SMS 게재 보고는 연결된 메시지 및 동적 개인화를 고려하지 않으므로 공급자로부터 전송된 실제 메시지 수를 반영하지 않을 수 있습니다. 자세한 사용 및 청구 정보는 Adobe 담당자에게 문의하십시오.
>
>SMS 청구 초과를 최소화하기 위한 모범 사례를 알아보려면 [문자 최적화를 위한 SMS 모범 사례](sms-cost-optimization.md)를 참조하세요.

## 콘텐츠 유효성 검사 {#sms-validate}

편집기의 위쪽 섹션에서 경고를 확인해야 합니다. 일부는 간단한 경고이지만 일부는 메시지를 보내지 못하게 할 수 있습니다. 경고와 오류의 두 가지 경고 유형이 발생할 수 있습니다.

![](assets/sms-alert-button.png)

* **경고**&#x200B;는 권장 사항과 모범 사례를 참조합니다. 예를 들어 텍스트 메시지가 비어 있는 경우 경고 메시지가 표시됩니다.

* **오류**&#x200B;로 인해 여정을 테스트 또는 활성화하거나 캠페인을 게시하지 못할 수 있습니다. 단, 해결되지 않는 한 가능합니다. 예를 들어 제목 줄이 누락된 경우 경고 메시지가 표시됩니다.


>[!NOTE]
>
> 전달성을 향상시키려면 공급자가 지원하는 형식의 전화 번호를 사용하십시오. 예를 들어 Twilio와 Sinch는 E.164 형식의 전화 번호만 지원합니다.

## 문자 메시지 보내기 {#sms-send}

>[!IMPORTANT]
>
> 캠페인이 승인 정책의 적용을 받는 경우 문자 메시지를 보내려면 승인을 요청해야 합니다. [자세히 알아보기](../test-approve/gs-approval.md)

문자 메시지가 준비되면 [여정](../building-journeys/journey-gs.md) 또는 [캠페인](../campaigns/create-campaign.md)의 구성을 완료하여 보내십시오.

**관련 항목**

* [SMS 채널 구성](sms-configuration.md)
* [SMS/MMS 보고서](../reports/journey-global-report-cja-sms.md)
* [텍스트 메시지 만들기](create-sms.md)
* [여정에 메시지 추가](../building-journeys/journeys-message.md)
