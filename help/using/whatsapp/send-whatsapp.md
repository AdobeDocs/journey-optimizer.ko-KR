---
solution: Journey Optimizer
product: journey optimizer
title: WhatsApp 메시지 확인 및 테스트
description: Journey Optimizer에서 WhatsApp 메시지를 확인하고 보내는 방법을 알아봅니다
feature: Whatsapp
topic: Content Management
role: User
level: Beginner
exl-id: 31acb095-de90-495f-8e8c-43a78dedfa06
TQID: https://experienceleague.adobe.com/u2OevVu38fPdytpuTmHeSdEx3Wvpih7ifk-j88rhDFI
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: f8d2e9f0-69c9-40cd-890f-71336c8dfff7
  - id: b8df23d2-98a2-4406-86cc-2babe8728d36
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: a4e4f5ca5c3eb9dbfb5691cb5de420009ed7e5a5
workflow-type: tm+mt
source-wordcount: 414
ht-degree: 2%

---

# WhatsApp 메시지 확인 및 보내기 {#send-whatsapp}

## WhatsApp 메시지 미리 보기 {#preview-whatsapp}

메시지 콘텐츠가 정의되면 다음 시뮬레이션 방법 중 하나를 사용하여 콘텐츠를 미리 볼 수 있습니다.

* 샘플 입력 데이터 또는 AI 자동 생성을 사용하여 콘텐츠 변형을 테스트하려면 **[!UICONTROL 콘텐츠 시뮬레이션]**&#x200B;을 클릭하십시오. [콘텐츠 변형을 시뮬레이션하는 방법을 알아봅니다](../test-approve/simulate-sample-input.md)
* **[!UICONTROL 콘텐츠 시뮬레이션]**&#x200B;을 클릭한 다음 드롭다운에서 **[!UICONTROL 콘텐츠 시뮬레이션(AEP 프로필)]**&#x200B;을 선택하여 테스트 프로필로 미리 봅니다.

콘텐츠를 미리 보고 테스트하는 방법에 대한 자세한 내용은 [콘텐츠 관리](../content-management/preview-test.md) 섹션에서 확인할 수 있습니다.

## 콘텐츠 유효성 검사 {#whatsapp-validate}

편집기의 위쪽 섹션에서 경고를 확인해야 합니다. 일부는 간단한 경고이지만 일부는 메시지를 보내지 못하게 할 수 있습니다. 경고와 오류의 두 가지 경고 유형이 발생할 수 있습니다.

* **경고**&#x200B;는 권장 사항과 모범 사례를 참조합니다. 예를 들어 텍스트 메시지가 비어 있는 경우 경고 메시지가 표시됩니다.

* **오류**&#x200B;로 인해 여정을 테스트 또는 활성화하거나 캠페인을 게시하지 못할 수 있습니다. 단, 해결되지 않는 한 가능합니다. 예를 들어 제목 줄이 누락된 경우 경고 메시지가 표시됩니다.

## WhatsApp 메시지 보내기 {#whatsapp-send}

>[!IMPORTANT]
>
> 캠페인이 승인 정책의 적용을 받는 경우 문자 메시지를 보내려면 승인을 요청해야 합니다. [자세히 알아보기](../test-approve/gs-approval.md)

WhatsApp 메시지가 준비되면 [여정](../building-journeys/publish-journey.md) 또는 [캠페인](../campaigns/review-activate-campaign.md)의 구성을 완료하여 보내십시오.

## WhatsApp 상호 작용 분석 {#whatsapp-channel-context}

Journey Optimizer은 WhatsApp 채널에서 반환된 추가 상호 작용 데이터를 캡처하여 `whatsAppChannelContext` 필드 그룹의 **AJO - 전자 메일 추적 경험 이벤트 데이터 세트**&#x200B;에 저장합니다. 이 필드를 사용하여 [대상](../audience/about-audiences.md)을(를) 빌드하고, [쿼리](../data/get-started-queries.md)를 실행하고, WhatsApp 참여를 분석하십시오. [시스템 데이터 세트에 대해 자세히 알아보세요](../data/get-started-datasets.md#system-datasets).

다음 필드가 캡처됩니다.

| 필드 | 설명 |
|-|-|
| `messageType` | WhatsApp 메시지 유형(예: `templateBased`, `response`). |
| `inboundMessage` | 인바운드 회신 콘텐츠(예: `stop`, `start`, `subscribe`). |
| `inboundNumber` | 인바운드 메시지가 수신된 발신자 ID. |
| `channelType` | 채널 범주(`Utility`, `Marketing` 또는 `Promotional`). |
| `profileNumber` | 인바운드 메시지가 수신된 전화 번호. |
| `origTimestamp` | Meta / WhatsApp의 원래 타임스탬프. |
| `status` | 표준화된 공급자 피드백(`sent`, `delivered`, `bounce`, `error`, `delay`, `duplicate`, `denylist`, `exclude` 또는 `unknown`)과 원시 공급자 상태 메시지를 포함하는 게재 상태입니다. |
| `reactionEvent` | 사용자 응답 콘텐츠: 반응을 위한 이모지 또는 특정 메시지에 대한 답글을 위한 메시지 텍스트. |
| `reactionMessageID` | 응답 중인 원래 메시지의 ID입니다. |
| `reactionActionName` | 응답 작업 유형(`react`, `unreact` 또는 `reply`). |
| `interactiveSelectedTitle` | WhatsApp 대화형 메시지에서 사용자가 선택한 제목입니다. |
| `interactiveType` | 대화형 메시지 유형(`list reply`, `button reply` 또는 `button`). |
| `interactiveSelectedDescription` | 선택한 WhatsApp 대화형 옵션에 대한 설명입니다. |
| `interactiveSelectedID` | WhatsApp에서 선택한 옵션의 ID입니다. |

이 데이터 집합을 쿼리하려면 쿼리 서비스의 `ajo_email_tracking_experience_event_dataset` 테이블을 사용합니다. 쿼리 패턴 및 관련 사용 사례는 [데이터 집합 쿼리 예제](../data/datasets-query-examples.md)를 참조하십시오.
