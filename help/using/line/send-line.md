---
solution: Journey Optimizer
product: journey optimizer
title: LINE 메시지 미리 보기, 유효성 검사 및 보내기
description: LINE 메시지를 미리 보고 유효성을 검사하고, 경고 및 오류를 해결하고, 필요한 경우 승인을 요청하고, 여정 또는 캠페인에서 활성화하거나 게시하는 방법에 대해 알아봅니다
feature: Line
topic: Content Management
role: User
level: Beginner
exl-id: fd8437c6-0052-4116-af60-5624569bda65
TQID: https://experienceleague.adobe.com/Bfu4AL1axI4XUq0PKXuN0PnnxNvq4MB-O7Bzz66mtbU
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037id: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dffid: f8d2e9f0-69c9-40cd-890f-71336c8dfff7id: e09fc1e6-407c-418f-adc5-e2ffe8b8986e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: 94a7cd6e4e89b2c8a4a09cfb4fbfc173ca76c391
workflow-type: tm+mt
source-wordcount: 400
ht-degree: 2%

---


# LINE 메시지 미리 보기, 유효성 검사 및 보내기 {#send-line}

>[!BEGINSHADEBOX]

**이 페이지에서:** LINE 메시지를 미리 보고 유효성을 검사하고, 경고와 오류를 해결하고, 필요한 경우 승인을 요청하고, 여정 또는 캠페인 구성을 완료하여 메시지를 보냅니다.

>[!ENDSHADEBOX]

## 시작하기 전에 {#before-you-start}

시작하기 전에 다음을 확인하십시오.

* 조직에 대해 LINE을 사용할 수 있습니다. LINE을 사용할 수 없는 경우 Adobe 담당자에게 문의하여 활성화를 요청하십시오.
* Journey Optimizer에서 LINE 채널 구성을 사용할 수 있습니다. [LINE 채널 구성](./line-configuration.md)을 참조하세요.
* 여정 또는 캠페인에 LINE 작업을 추가하고 메시지 콘텐츠를 정의했습니다. [LINE 메시지 만들기](./create-line.md)를 참조하세요.

## LINE 메시지 미리 보기 {#preview-line}

메시지 콘텐츠를 정의한 후 **[!UICONTROL 콘텐츠 시뮬레이션]**&#x200B;을 사용하여 메시지를 보내기 전에 미리 봅니다.

다음 옵션 중 하나를 사용할 수 있습니다.

| 시뮬레이션 옵션 | 사용 대상 |
| --- | --- |
| **[!UICONTROL 콘텐츠 시뮬레이션]** | 샘플 입력 데이터 또는 AI 자동 생성을 사용하여 콘텐츠 변형을 테스트합니다. |
| **[!UICONTROL 콘텐츠 시뮬레이션]** > **[!UICONTROL 콘텐츠 시뮬레이션(AEP 프로필)]** | 테스트 프로필로 메시지를 미리 봅니다. |

각 변형을 검토하고 메시지 콘텐츠와 개인화된 값이 예상대로 표시되는지 확인합니다.

콘텐츠 미리 보기 및 테스트에 대한 자세한 내용은 [콘텐츠 미리 보기 및 테스트](../content-management/preview-test.md)를 참조하십시오.

## 콘텐츠 유효성 검사 {#line-validate}

계속하기 전에 메시지 편집기 상단에 표시된 경고를 검토하십시오.

Journey Optimizer에는 두 가지 유형의 경고가 표시됩니다.

* **경고**&#x200B;는 권장 사항 또는 모범 사례 제안입니다. 테스트하거나 메시지를 보내는 것을 금지하지 않습니다.
* **오류**&#x200B;은(는) 여정을 테스트하거나 활성화하거나 캠페인을 게시하기 전에 해결해야 하는 문제를 식별합니다.

계속하기 전에 모든 오류를 해결하십시오. 메시지가 의도한 고객 경험을 제공하지 않을 수 있음을 나타낼 때 경고를 해결합니다.

## 필요한 경우 승인 요청 {#line-approval}

캠페인이 승인 정책의 적용을 받는 경우 메시지를 보내기 전에 승인을 요청하십시오.

[승인 요청 방법 알아보기](../test-approve/gs-approval.md)를 참조하세요.

## LINE 메시지 보내기 {#line-send}

메시지가 준비되면 LINE 작업이 포함된 여정 또는 캠페인으로 돌아가서 해당 구성을 완료합니다.

* **여정:** 여정 구성을 완료한 다음 여정을 활성화합니다.
* **캠페인:** 캠페인 구성을 완료한 다음 캠페인을 게시합니다.

여정을 활성화하거나 캠페인을 게시할 수 없는 경우 메시지 편집기로 돌아가서 나머지 오류를 해결하십시오.

## 관련 작업 {#related-tasks}

* [LINE 시작](./get-started-line.md)
* [LINE 메시지 만들기](./create-line.md)
* [LINE 채널 구성](./line-configuration.md)

{{$include /help/_includes/do-not-localize/line/ai-augmented-send-line.md}}
