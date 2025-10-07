---
solution: Journey Optimizer
product: journey optimizer
title: 캠페인 액션 구성
description: Campaign 작업을 구성하는 방법을 알아봅니다.
feature: Campaigns
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
keywords: 만들기, 최적화 도구, 캠페인, 표면, 메시지
exl-id: fed96e48-2e54-4bd4-ae17-77434d1b90eb
source-git-commit: 801b90201c3ffcbfb7b038abac2bf99209a14c7a
workflow-type: tm+mt
source-wordcount: '815'
ht-degree: 35%

---

# 캠페인 액션 구성 {#action-campaign-action}

**[!UICONTROL 액션]** 탭을 사용하여 메시지의 채널 구성을 선택하고 추적, 콘텐츠 실험 또는 다국어 콘텐츠와 같은 추가 설정을 구성합니다.

1. **채널 선택**

   **[!UICONTROL 작업]** 탭으로 이동하여 **[!UICONTROL 작업 추가]** 단추를 클릭하고 통신 채널을 선택합니다.

   ![](assets/create-campaign-add-action.png)

   >[!NOTE]
   >
   >지원되는 채널은 [이메일](../email/get-started-email.md), [SMS/MMS/RCS](../sms/get-started-sms.md), [푸시 알림](../push/get-started-push.md), [WhatsApp](../whatsapp/get-started-whatsapp.md), [LINE](../line/get-started-line.md), [다이렉트 메일](../direct-mail/get-started-direct-mail.md), [앱 내](../in-app/get-started-in-app.md), [웹](../web/get-started-web.md), [코드 기반 경험](../code-based/get-started-code-based.md)입니다.
   >
   >사용 가능한 채널은 사용하는 라이선스 모델 및 추가 기능에 따라 다릅니다.

   인바운드 채널(코드 기반 경험, 인앱 메시지, 콘텐츠 카드 또는 웹 작업)을 선택하는 경우 단일 캠페인에서 최대 10개의 작업에 대해 더 많은 인바운드 작업을 추가할 수 있습니다. [방법 알아보기](#multi-action)

1. **채널 구성 선택**

   구성은 [시스템 관리자](../start/path/administrator.md)가 정의합니다. 여기에는 헤더 매개변수, 하위 도메인, 모바일 앱 등 메시지 전송을 위한 모든 기술적 매개변수가 포함되어 있습니다. [채널 구성을 설정하는 방법 알아보기](../configuration/channel-surfaces.md)

   ![](assets/create-campaign-action.png)

1. **최적화 활용**

   **[!UICONTROL 최적화]** 섹션을 사용하여 콘텐츠 실험을 실행하거나, 타깃팅 규칙을 활용하거나, 실험과 타깃팅을 모두 사용하는 고급 조합을 사용할 수 있습니다. 이러한 다양한 옵션과 따라야 할 단계는 [이 섹션](campaigns-message-optimization.md)에 자세히 설명되어 있습니다.
<!--
1. **Create a content experiment**

    Use the **[!UICONTROL Content experiment]** section to define multiple delivery treatments in order to measure which one performs best for your target audience. Click the **[!UICONTROL Create experiment]** button then follow the steps detailed in this section: [Create a content experiment](../content-management/content-experiment.md).-->

1. **다국어 콘텐츠 추가**

   **[!UICONTROL 언어]** 섹션을 사용하여 캠페인 내에서 여러 언어로 콘텐츠를 만듭니다. 이렇게 하려면 **[!UICONTROL 언어 추가]** 버튼을 클릭하고 원하는 **[!UICONTROL 언어 설정]**&#x200B;을 선택합니다. 다국어 기능을 설정하고 사용하는 방법에 대한 자세한 내용은 [이 섹션](../content-management/multilingual-gs.md)을 참조하세요.

선택한 통신 채널에 따라 추가 설정을 사용할 수 있습니다. 자세한 내용을 보려면 아래 섹션을 확장하십시오.

+++**최대 가용량 규칙 적용**(전자 메일, DM, 푸시, SMS)

**[!UICONTROL 비즈니스 규칙]** 드롭다운 목록에서 최대 가용량 규칙을 캠페인에 적용할 규칙 집합을 선택하십시오. 채널 규칙 세트를 활용하면 통신 유형별로 빈도 상한을 설정하여 유사한 메시지가 있는 고객을 오버로드할 수 있습니다. [규칙 세트 작업 방법 알아보기](../conflict-prioritization/rule-sets.md)

+++

+++**참여 추적**(전자 메일, SMS).

**[!UICONTROL 액션 추적]** 섹션을 사용하여 수신자가 이메일 또는 SMS 게재에 어떻게 반응하는지 추적할 수 있습니다. 캠페인이 실행되면 캠페인 보고서에서 추적 결과에 액세스할 수 있습니다. [캠페인 보고서에 대해 자세히 알아보기](../reports/campaign-global-report-cja.md)

+++

+++**빠른 전송 모드를 사용**(푸시)합니다.

빠른 전송 모드는 캠페인을 통해 대량으로 매우 빠르게 푸시 메시지를 전송할 수 있는 [!DNL Journey Optimizer] 추가 기능입니다. 빠른 게재는 메시지 게재 지연이 비즈니스에 중요한 경우, 휴대폰에 긴급 푸시 알림을 전송하려는 경우(예: 뉴스 채널 앱을 설치한 사용자에게 속보 전달) 사용됩니다. 빠른 전송 모드를 사용할 때의 성능에 대한 자세한 내용은 [Adobe Journey Optimizer 제품 설명](https://helpx.adobe.com/kr/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}을 참조하십시오.

+++

+++**우선 순위 점수 할당**(웹, 인앱, 코드 기반)

캠페인에 우선 순위 점수를 할당하면 빈도 상한과 같은 부과된 제한 사항이 있을 때 인바운드 캠페인의 우선 순위를 지정할 수 있습니다. 숫자 값(0~100)을 입력하십시오. 숫자가 높을수록 우선순위가 높다는 점에 유의하십시오. [여정 및 캠페인에 우선 순위 점수를 할당하는 방법 알아보기](../conflict-prioritization/priority-scores.md)

+++

+++**추가 게재 규칙 설정**(콘텐츠 카드)

콘텐츠 카드 캠페인의 경우 추가 게재 규칙을 활성화하여 메시지를 트리거하는 이벤트 및 기준을 선택할 수 있습니다. [콘텐츠 카드를 만드는 방법을 알아봅니다](../content-card/create-content-card.md)

+++

+++**트리거 정의**(인앱)

인앱 메시지의 경우 **[!UICONTROL 트리거 편집]** 단추를 사용하여 메시지를 트리거하는 이벤트 및 기준을 선택할 수 있습니다. [인앱 메시지를 만드는 방법을 알아봅니다](../in-app/create-in-app.md)

+++

## 여러 인바운드 액션 추가 {#multi-action}

>[!CONTEXTUALHELP]
>id="ajo_multi_action"
>title="여러 인바운드 액션 추가"
>abstract="단일 캠페인 내에서 여러 인바운드 액션을 선택할 수 있습니다. 이 기능을 사용하면 여러 코드 기반 경험, 인앱 메시지, 콘텐츠 카드 또는 웹 액션을 동시에 여러 위치에 게재할 수 있으며, 각 액션에는 특정 콘텐츠가 포함됩니다."

캠페인 오케스트레이션을 단순화하기 위해 단일 캠페인 내에서 여러 인바운드 작업을 정의할 수 있습니다. 각 작업에는 특정 콘텐츠가 포함됩니다.

>[!NOTE]
>
>이 용량은 인바운드 채널에만 사용할 수 있습니다. 현재 이메일 등의 아웃바운드 채널은 지원되지 않습니다.

이 용량을 사용하면 여러 캠페인을 만들 필요 없이 다양한 코드 기반 경험, 인앱 메시지, 콘텐츠 카드 또는 웹 작업을 동시에 다른 위치에 전달할 수 있습니다. 이렇게 하면 모든 데이터를 하나의 캠페인으로 통합하여 캠페인을 보다 쉽게 배포할 수 있고 보고를 보다 원활하게 수행할 수 있습니다.

예를 들어 콘텐츠가 약간 다른 여러 끝점에 코드 기반 경험을 보낼 수 있습니다. 이렇게 하려면 동일한 캠페인 내에서 각각 다른 끝점 구성을 갖는 여러 코드 기반 작업을 만듭니다.

캠페인에서 여러 인바운드 작업을 정의하려면 아래 단계를 따르십시오.

1. **작업** 섹션에서 인바운드 작업(**코드 기반 경험**, **인앱 메시지**, **콘텐츠 카드** 또는 **[!UICONTROL 웹]**)을 선택하십시오.

1. 채널 구성을 선택하고 해당 작업에 대한 특정 콘텐츠를 정의합니다.

1. **[!UICONTROL 작업 추가]** 단추를 사용하여 드롭다운 목록에서 다른 인바운드 작업을 선택합니다.

   ![](assets/create-campaign-multi-action.png){width="80%"}

1. 작업을 추가하려면 유사하게 진행합니다. 캠페인에 최대 10개의 인바운드 작업을 추가할 수 있습니다.

캠페인이 [live](review-activate-campaign.md)이면 모든 작업이 동시에 활성화됩니다.

## 다음 단계 {#next}

캠페인 작업이 준비되면 콘텐츠를 디자인할 수 있습니다. [자세히 알아보기](campaign-content.md)
