---
solution: Journey Optimizer
product: journey optimizer
title: 모바일 메시지 확인 및 테스트
description: Journey Optimizer에서 모바일 메시지를 확인하고 보내는 방법 알아보기
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: 31c9b080-e334-4a11-af33-4c6f115c70a4
TQID: https://experienceleague.adobe.com/JPjBxyZzo13tgSLo0dqd5bFOwn9C6MHkA-DjLzlAdEI
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: c41e8697-e629-4c38-96b3-564faaa17acf
  - id: f8d2e9f0-69c9-40cd-890f-71336c8dfff7
  - id: b3b09fe1-10f1-4793-9f6b-1ca0269eebe7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 4c82775044b5a0a3a48920f59b0afb8a3c6a6d80
workflow-type: tm+mt
source-wordcount: 562
ht-degree: 1%

---

# 모바일 메시지 확인 및 보내기 {#send-sms}

>[!BEGINSHADEBOX]

**이 페이지에서:** 문자 인코딩 및 제한을 확인하고 배달하기 전에 알림을 확인하는 등 Adobe Journey Optimizer에서 모바일 메시지를 미리 보고, 유효성을 확인하고, 보내는 방법을 알아봅니다.

>[!ENDSHADEBOX]

## 모바일 메시지 미리 보기 {#preview-sms}

메시지 콘텐츠가 정의되면 다음 시뮬레이션 방법 중 하나를 사용하여 콘텐츠를 미리 볼 수 있습니다.

* 샘플 입력 데이터 또는 AI 자동 생성을 사용하여 콘텐츠 변형을 테스트하려면 **[!UICONTROL 콘텐츠 시뮬레이션]**&#x200B;을 클릭하십시오. [콘텐츠 변형을 시뮬레이션하는 방법을 알아봅니다](../test-approve/simulate-sample-input.md)
* **[!UICONTROL 콘텐츠 시뮬레이션]**&#x200B;을 클릭한 다음 드롭다운에서 **[!UICONTROL 콘텐츠 시뮬레이션(AEP 프로필)]**&#x200B;을 선택하여 테스트 프로필로 미리 봅니다.

![](assets/sms_preview_2.png)

콘텐츠를 미리 보고 테스트하는 방법에 대한 자세한 내용은 [콘텐츠 관리](../content-management/preview-test.md) 섹션에서 확인할 수 있습니다.

### 문자 인코딩 및 제한 {#sms-character-limits}

**[!UICONTROL 콘텐츠 시뮬레이션]**&#x200B;에서 시뮬레이션 방법에 액세스할 때 문자 수가 표시되어 모바일 메시지를 계획하고 관리하는 데 도움이 됩니다.

![](assets/sms_preview_3.png)

Journey Optimizer은 SMS 편집기에서 UTF-8 인코딩을 사용하므로 더블바이트 또는 유니코드 문자를 입력하거나 붙여넣을 수 있습니다. 그런 다음 이러한 문자가 전달을 위해 서비스 공급자에게 전송됩니다. 대부분의 SMS 공급자는 160자 제한이 있는 표준 메시지에 GSM 7비트 인코딩을 사용하고, GSM이 아닌 문자가 70자 제한으로 감지되면 UTF-16(UCS-2)으로 전환합니다.

문자 수는 동적 개인화에 의해 도입된 변형 또는 GSM이 아닌 7비트 특수 문자를 반영하지 않습니다.

>[!IMPORTANT]
>
>Journey Optimizer SMS 게재 보고는 연결된 메시지 및 동적 개인화를 고려하지 않으므로 공급자로부터 전송된 실제 메시지 수를 반영하지 않을 수 있습니다. 자세한 사용 및 청구 정보는 Adobe 담당자에게 문의하십시오.
>
>SMS 청구 초과를 최소화하기 위한 모범 사례를 알아보려면 [문자 최적화를 위한 SMS 모범 사례](mobile-cost-optimization.md)를 참조하세요.

## 콘텐츠 유효성 검사 {#sms-validate}

>[!NOTE]
>
> 전달성을 향상시키려면 공급자가 지원하는 형식의 전화 번호를 사용하십시오. 예를 들어 Twilio와 Sinch는 E.164 형식의 전화 번호만 지원합니다.

편집기의 위쪽 섹션에서 경고를 확인해야 합니다. 일부는 간단한 경고이지만 일부는 메시지를 보내지 못하게 할 수 있습니다. 경고와 오류의 두 가지 경고 유형이 발생할 수 있습니다.

![](assets/sms-alert-button.png)

* **경고**&#x200B;는 권장 사항과 모범 사례를 참조합니다. 예를 들어 모바일 메시지가 비어 있거나 동적 콘텐츠에서 문자 제한을 초과할 수 있는 경우 경고 메시지가 표시됩니다.

  **문자 제한:** 세그먼트당 160자(GSM 7비트), 유니코드/이모지의 경우 70자, 총 1500자.

* **오류**&#x200B;로 인해 여정을 테스트 또는 활성화하거나 캠페인을 게시하지 못할 수 있습니다. 단, 해결되지 않는 한 가능합니다. 예를 들어 제목 줄이 누락된 경우 경고 메시지가 표시됩니다.

경고 **&quot;SMS 텍스트 문자 제한을 초과했습니다.&quot;** 유효성 검사가 모든 조건부 분기, 개인화 필드 및 동적 콘텐츠를 최장 시간에 평가하여 **최대 가능한 길이**&#x200B;를 계산하기 때문에 시뮬레이션된 메시지가 더 짧은 경우에도 나타날 수 있습니다.

검증은 가능한 모든 프로파일 데이터에 대한 최대 길이를 계산하는 반면 시뮬레이션은 하나의 테스트 프로파일에 대한 실제 출력을 보여 줍니다.

## 모바일 메시지 보내기 {#sms-send}

>[!IMPORTANT]
>
> 캠페인이 승인 정책의 적용을 받는 경우 모바일 메시지를 보내려면 승인을 요청해야 합니다. [자세히 알아보기](../test-approve/gs-approval.md)

모바일 메시지가 준비되면 [여정](../building-journeys/journey-gs.md) 또는 [캠페인](../campaigns/create-campaign.md)의 구성을 완료하여 보내십시오.

**관련 항목**

* [SMS 채널 구성](mobile-configuration.md)
* [SMS/RCS/MMS 보고서](../reports/journey-global-report-cja-sms.md)
* [모바일 메시지 만들기](create-mobile-message.md)
* [여정에 메시지 추가](../building-journeys/journey-action.md)
