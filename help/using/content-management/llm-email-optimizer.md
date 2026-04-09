---
title: AI 받은 편지함에 대한 이메일 텍스트 최적화
description: Journey Optimizer에서 이메일의 일반 텍스트 계층을 세분화하여 AI 지원 받은 편지함 클라이언트가 AI를 사용하여 이메일 Designer에서 메일을 요약하거나 의도를 추출할 때 오퍼와 CTA를 사용할 수 있습니다.
feature: Email Design
topic: Content Management, Artificial Intelligence
role: User
level: Beginner, Intermediate
exl-id: 0c2f95ce-28a0-480c-9829-b7e4975b6340
source-git-commit: d7d9c371f4b0d8b4ea51e1f23eb9a2f665711fce
workflow-type: tm+mt
source-wordcount: '1084'
ht-degree: 1%

---

# AI 받은 편지함에 대한 이메일 텍스트 최적화 {#email-text-optimizer}

[!DNL Adobe Journey Optimizer]에는 개선된 AI 지원 받은 편지함 환경(예: [의 ](../email/text-version-email.md) 및 [!DNL Apple Intelligence])을 위해 메시지의 [!DNL Google Gemini]텍스트 버전[!DNL Gmail]을 구성하는 데 도움이 되는 전자 메일 채널 기능이 포함되어 있으므로 질문에 답변하고 콘텐츠를 기반으로 메일을 보다 정확하게 요약하여 더 나은 결과를 얻을 수 있습니다.

>[!NOTE]
>
>이 기능은 이메일 콘텐츠의 HTML 버전이 아니라 일반 텍스트만 변경합니다.

이 이메일 텍스트 최적화 프로그램을 사용하면 AI가 지원하는 받은 편지함 경험을 위해 이메일 콘텐츠의 일반 텍스트 버전을 향상시켜 이러한 이메일 받은 편지함 공급자의 AI 기능에 제공하는 정보가 정확히 제공하려는 정보인지 확인할 수 있습니다.

## 작동 방식 {#how-it-works}

받는 사람이 AI 지원 받은 편지함 경험에서 물어볼 수 있는 일반적인 질문은 *입니다. 이 이메일은 무엇에 관한 것입니까?* 또는 *이러한 오퍼는 무엇입니까?*.

* 이러한 AI 도우미가 제공하는 답변은 짧은 요약일 수 있지만(예를 들어, 메시지는 홍보용이며, VIP 조기 액세스 및 판매에 대해 언급하고, 제품 범주에 대한 링크를 포함하는 경우), 도우미가 효과적으로 볼 수 있는 모든 텍스트에서 추론하고 있기 때문에 마케터가 신경 쓴 목표를 여전히 생략할 수 있습니다(의도한 전체 스토리가 아닐 수도 있습니다).

* 또한, 도우미들이 적극적으로 브랜드와 관련된 할인이나 쿠폰을 검색한 후 이를 답안에 접어 넣으면 사용자는 더 이상 사용자의 메시지가 실제로 약속한 내용만 보지 않게 된다. 이 동작은 최종 사용자에게 유용하지만, 전송에서 실제 용어를 추적하기 위해 답변이 필요한 마케터에는 제어를 희석합니다.

이러한 문제를 방지하기 위해 [!DNL Journey Optimizer]은(는) 쿠폰, 할인 범위, 콜 투 액션 및 기타 우선 순위가 명확한 선형 복사본에 앞에 나타나도록 일반 텍스트를 다시 작성합니다. 목표는 받은 편지함 AI가 얇은 기본 텍스트 부분이나 관련 없는 웹 결과에 기대지 않고 정의된 오퍼와 작업에서 요약과 Q&amp;A를 접지하는 것입니다.

>[!IMPORTANT]
>
>정확한 AI 지원 동작은 받은 편지함 공급자 및 모델 버전에 따라 다릅니다. 이메일이 게재되면 외부 AI 클라이언트가 제공하는 답변 및 요약이 잘못되거나 불완전하거나 웹 결과와 혼용될 수 있습니다.
>
>AI 받은 편지함에 대한 이메일 텍스트 최적화 기능은 Journey Optimizer에서 작성하는 일반 텍스트만 향상시킵니다. 타사 도우미가 메시지를 해석하거나 표시하는 방식을 보장하지는 않습니다. 타사 받은 편지함 AI의 [제한 사항 및 위험](#inbox-ai-risks)에 대해 자세히 알아보세요.

## 권장 사용 사례 {#use-cases}

<!--
* **Critical details only in images** — Offers, promo codes, or deadlines shown in banners or graphics are invisible in plain text. Use the optimizer (and manual edits) so the same facts appear as text, improving extraction by AI summaries and text-only clients.
-->

* **자동 생성된 조밀 또는 조각화된 텍스트** — 기본 일반 텍스트를 스캔하기 어려운 경우 최적화를 통해 명확한 오퍼 및 링크를 통해 선명한 선형을 생성할 수 있습니다.

* **받은 편지함 Q&amp;A 제어** — 받는 사람이 도우미에게 *이메일이 무엇인지* 또는 *오퍼가 무엇인지*&#x200B;를 물어볼 것으로 예상되면 강력한 일반 텍스트 버전이 부분 요약을 줄이고 승인된 복사본에 연결되지 않은 웹 보충 응답에 대한 의존도를 낮춥니다.

## AI 받은 편지함 경험에 최적화 {#optimize-with-ai}

>[!IMPORTANT]
>
>이 기능의 사용을 시작하기 전에 관련 [위험 및 제한 사항](#inbox-ai-risks)을 읽어 보십시오.
>
>이 기능에 액세스하려면 [!DNL Journey Optimizer]에서 생성 AI를 처음 사용할 때 표시되는 사용자 계약에 동의해야 합니다. 자세한 내용은 [Adobe Experience Cloud Generative AI 사용 지침](https://www.adobe.com/kr/legal/licenses-terms/adobe-gen-ai-user-guidelines.html){target="_blank"}을 참조하세요.

[!DNL Journey Optimizer]을(를) 사용하여 AI 받은 편지함에 대한 전자 메일의 일반 텍스트 버전을 최적화하려면 아래 단계를 따르십시오.

1. [전자 메일 Designer](../email/content-from-scratch.md)에서 전자 메일을 엽니다(워크플로우에 따라 캠페인, 여정 또는 템플릿에서).

1. **[!UICONTROL 일반 텍스트]** 아이콘을 선택하여 전자 메일의 텍스트 버전을 엽니다. [자세히 알아보기](../email/text-version-email.md)

   ![일반 텍스트 아이콘을 선택하여 전자 메일의 텍스트 버전을 엽니다](assets/text-optimizer-text-icon.png){zoomable="yes"}

1. 이메일의 텍스트 버전이 표시됩니다. **[!UICONTROL AI 받은 편지함에 최적화]** 단추를 클릭하여 AI 지원 읽기 및 요약에 대한 주요 정보를 강조 표시하는 개선된 일반 텍스트 버전을 생성합니다.

   ![텍스트 버전 보기의 AI 받은 편지함에 최적화](assets/text-optimizer-for-ai-button.png){zoomable="yes" width="80%"}

   >[!NOTE]
   >
   >**[!UICONTROL AI 받은 편지함에 최적화]** 단추를 클릭하면 **[!UICONTROL HTML과 동기화]** 옵션이 자동으로 비활성화됩니다. [자세히 알아보기](../email/text-version-email.md#plain-text-custom)

1. [!DNL Journey Optimizer]에서 생성 AI를 처음 사용하는 경우 사용자 계약에 동의하라는 메시지가 표시됩니다. 자세한 내용은 [Adobe Generative AI 사용 지침](https://www.adobe.com/kr/legal/licenses-terms/adobe-gen-ai-user-guidelines.html){target="_blank"}을 참조하세요.

   Journey Optimizer의 ![생성 AI 사용자 동의 대화 상자](assets/text-optimizer-agreement.png){width=50%}

   계속하려면 **[!UICONTROL 동의]**&#x200B;를 클릭하세요.

1. 생성된 텍스트가 표시됩니다. 변경 사항을 검토하고 필요한 경우 편집한 다음 평소와 같이 이메일을 저장합니다.

   ![텍스트 버전 보기에서 생성된 텍스트](assets/text-optimizer-output.png){zoomable="yes" width="80%"}

   >[!NOTE]
   >
   >이메일 텍스트 최적기는 일반 텍스트 본문만 업데이트합니다. HTML 디자인, 레이아웃 또는 이미지는 변경되지 않습니다.

1. **[!UICONTROL 데스크톱 보기로 전환]** 아이콘을 클릭하여 언제든지 HTML 버전의 전자 메일로 다시 전환할 수 있습니다. 텍스트 버전의 변경 사항은 그대로 유지됩니다.

   >[!CAUTION]
   >
   >**[!UICONTROL HTML과 동기화]** 옵션을 다시 사용하면 변경 내용이 손실되어 HTML 버전에서 생성된 텍스트 콘텐츠로 바뀝니다.

## 타사 받은 편지함 AI의 위험 및 제한 사항 {#inbox-ai-risks}

AI 받은 편지함에 대한 전자 메일 텍스트 최적화 기능을 사용하면 사서함 공급자가 [!DNL Journey Optimizer] 전송을 처리할 수 있는 방법에 대한 일반 텍스트를 준비하는 데 도움이 됩니다. 이러한 공급자의 제품은 제어하지 않습니다. 메시지가 전달되면 [!DNL Gmail], [!DNL Apple] 메일, [!DNL Outlook] 또는 다른 클라이언트의 모든 AI 기능은 Adobe이 아닌 해당 용어, 모델 및 정책에 따라 작동합니다.

* **예측할 수 없는 프레젠테이션** — 요약, 알림 흐림 및 대화 답변을 생략하거나, 가격 또는 날짜를 잘못 기재하거나, 관련 없는 웹 결과와 콘텐츠를 병합하거나, 더 이상 승인된 복사본과 일치하지 않는 방식으로 대체됩니다. 공급업체가 예고 없이 모델 또는 UI를 업데이트할 때 동작이 변경됩니다.

* **HTML과의 동등한 기능을 보장할 수 없음** — 미리 보기나 길잡이 답변을 사용하는 수신자는 사용자의 전체 HTML 디자인, 이미지 또는 법적 절차를 볼 수 없습니다. 그들이 &quot;말하는&quot; 메시지가 AI가 생성한 짧은 요약에서만 나올 수 있다고 믿는 것.

* **개인 정보, 규정 준수 및 데이터 사용** — 받은 편지함 AI가 해당 공급자의 개인 정보 보호 정책, 보존 및 지역 규칙에 따라 공급자 인프라에서 메시지 콘텐츠를 처리할 수 있습니다. 규제 대상 업종의 조직은 [!DNL Journey Optimizer]에서 전자 메일이 작성된 방식과 관계없이 이러한 기능의 수신자 사용이 의무에 영향을 미치는지 여부를 평가해야 합니다.

* **브랜드 및 법적 노출** — 잘못되거나 불완전한 AI 요약으로 인해 여전히 고객 혼란 또는 프로모션, 약관 또는 옵트아웃 언어에 대한 분쟁이 발생할 수 있습니다. 최적기는 사용자가 제공하는 텍스트 레이어를 개선합니다. 타사 모델이 이를 성실하게 재현할 수 있는 것은 아닙니다.

* **[!UICONTROL 의]** AI 받은 편지함에 최적화[!DNL Journey Optimizer] — 전자 메일 Designer의 작성 시간 작업은 최종 사용자 받은 편지함 도우미와 별도의 시스템입니다. 보내기 전에 항상 생성된 일반 텍스트를 검토하십시오.

## 관련 항목 {#related-topics}

* [이메일의 텍스트 버전 관리](../email/text-version-email.md)
* [이메일 디자인 시작](../email/get-started-email-design.md)
* Adobe 생성 기능에 대한 자세한 내용은 [AI Assistant 시작](gs-generative.md)을 참조하십시오.
