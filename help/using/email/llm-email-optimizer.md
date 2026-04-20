---
title: AI 받은 편지함에 대한 이메일 최적화
description: AI 지원 받은 편지함 클라이언트가 AI로 최적화 Designer에서 메일을 요약하거나 의도를 추출할 때 오퍼와 CTA를 사용할 수 있도록 메시지의 전용 버전을 생성하고 세분화합니다.
feature: Email Design
topic: Content Management, Artificial Intelligence
role: User
level: Beginner, Intermediate
exl-id: 0c2f95ce-28a0-480c-9829-b7e4975b6340
source-git-commit: 0d0999b831d01442c46015361018d6e646abc33c
workflow-type: tm+mt
source-wordcount: '1069'
ht-degree: 1%

---

# AI 받은 편지함에 대한 이메일 최적화 {#email-text-optimizer}

[!DNL Adobe Journey Optimizer]에는 개선된 AI 지원 받은 편지함 환경(예: [!DNL Apple Intelligence]의 [!DNL Google Gemini] 및 [!DNL Gmail])을 위해 특정 버전의 메시지를 구성하는 데 도움이 되는 이메일 채널 기능이 포함되어 있으므로 질문에 답변하고 콘텐츠를 기반으로 메일을 보다 정확하게 요약하여 더 나은 결과를 얻을 수 있습니다.

이 기능을 사용하면 얇은 자동 생성 텍스트나 관련 없는 컨텍스트가 아닌 AI 지원 받은 편지함 경험에서 오퍼, 작업 호출 및 의도한 세부 정보를 표시할 수 있도록 전용 메시지 버전을 생성하고 개선할 수 있습니다.

<!--
>[!NOTE]
>
>This optimized for AI inboxes text version is not the same as the default or custom plain text version of your messages. [Learn more](text-version-email.md)
-->

## 작동 방식 {#how-it-works}

받는 사람이 AI 지원 받은 편지함 경험에서 물어볼 수 있는 일반적인 질문은 *입니다. 이 이메일은 무엇에 관한 것입니까?* 또는 *이러한 오퍼는 무엇입니까?*.

* 이러한 AI 도우미가 제공하는 답변은 간단한 요약일 수 있습니다(예: 메시지가 홍보용이며, VIP 조기 액세스 및 판매라고 언급되며, 제품 카테고리에 대한 링크가 포함됨). 그러나 보조자들이 효과적으로 볼 수 있는 텍스트(의도한 전체 스토리가 아닌)에서 추론하고 있기 때문에 마케터가 신경 쓴 목표를 여전히 생략합니다.

* 또한, 도우미들이 적극적으로 브랜드와 관련된 할인이나 쿠폰을 검색한 후 이를 답안에 접어 넣으면 사용자는 더 이상 사용자의 메시지가 실제로 약속한 내용만 보지 않게 된다. 이 동작은 최종 사용자에게 유용하지만, 전송에서 실제 용어를 추적하기 위해 답변이 필요한 마케터에는 제어를 희석합니다.

이러한 문제를 방지하기 위해 [!DNL Journey Optimizer]은(는) 쿠폰, 할인 범위, 콜 투 액션 및 기타 우선 순위가 명확한 선형 복사본에 맨 앞에 표시되도록 메시지의 추가 특정 버전을 만듭니다. <!--This version is different from the HTML view and default or custom plain text version of your messages.-->

목표는 받은 편지함 AI가 얇은 기본 텍스트 부분이나 관련 없는 웹 결과에 기대지 않고 정의된 오퍼와 작업에서 요약과 Q&amp;A를 접지하는 것입니다.

>[!IMPORTANT]
>
>정확한 AI 지원 동작은 받은 편지함 공급자 및 모델 버전에 따라 다릅니다. 이메일이 게재되면 외부 AI 클라이언트가 제공하는 답변 및 요약이 잘못되거나 불완전하거나 웹 결과와 혼용될 수 있습니다.
>
>AI 받은 편지함에 대한 이메일 최적화 기능은 Journey Optimizer의 전용 버전만 생성합니다. 서드파티 도우미가 메시지를 해석하거나 표시하는 방식을 보장하지는 않습니다. 타사 받은 편지함 AI의 [제한 사항 및 위험](#inbox-ai-risks)에 대해 자세히 알아보세요.

## 권장 사용 사례 {#use-cases}

<!--
* **Critical details only in images** — Offers, promo codes, or deadlines shown in banners or graphics are invisible in plain text. Use the optimizer (and manual edits) so the same facts appear as text, improving extraction by AI summaries and text-only clients.
-->

* **조밀하거나 조각난 콘텐츠** — 전자 메일의 콘텐츠를 스캔하기 어려운 경우 최적화는 명확한 오퍼 및 링크를 통해 명확한 선형 설명을 생성할 수 있습니다.

* **받은 편지함 Q&amp;A 제어** — 받는 사람이 도우미에게 *이메일이 무엇인지* 또는 *오퍼가 무엇인지*&#x200B;를 물을 것으로 예상할 때 AI 버전에 맞게 최적화된 강력한 기능을 통해 부분 요약을 줄이고 승인된 복사본에 연결되지 않은 웹 보충 답변을 사용하지 않습니다.

## AI 받은 편지함 경험에 최적화 {#optimize-with-ai}

>[!IMPORTANT]
>
>이 기능을 사용하기 전에 관련 [위험 및 제한 사항](#inbox-ai-risks)을 읽어 보십시오.
>
>이 기능에 액세스하려면 [!DNL Journey Optimizer]에서 생성 AI를 처음 사용할 때 표시되는 사용자 계약에 동의해야 합니다. 자세한 내용은 [Adobe Experience Cloud Generative AI 사용 지침](https://www.adobe.com/kr/legal/licenses-terms/adobe-gen-ai-user-guidelines.html){target="_blank"}을 참조하세요.

[!DNL Journey Optimizer]을(를) 사용하여 AI 받은 편지함 경험에 대한 전자 메일 콘텐츠를 최적화하려면 아래 단계를 따르십시오.

1. [전자 메일 Designer](content-from-scratch.md)에서 전자 메일을 엽니다(워크플로우에 따라 캠페인, 여정 또는 템플릿에서).

1. **[!UICONTROL AI 받은 편지함에 최적화]** 단추를 클릭하여 AI 지원 읽기 및 요약에 대한 주요 정보를 강조 표시하는 향상된 버전을 생성합니다.

   ![전자 메일 Designer의 AI 받은 편지함에 최적화](assets/optimize-for-ai-button.png){zoomable="yes" width="80%"}

1. [!DNL Journey Optimizer]에서 생성 AI를 처음 사용하는 경우 사용자 계약에 동의하라는 메시지가 표시됩니다. 자세한 내용은 [Adobe Generative AI 사용 지침](https://www.adobe.com/kr/legal/licenses-terms/adobe-gen-ai-user-guidelines.html){target="_blank"}을 참조하세요.

   Journey Optimizer의 ![생성 AI 사용자 동의 대화 상자](assets/optimize-ai-inbox-agreement.png){width=50%}

   계속하려면 **[!UICONTROL 동의]**&#x200B;를 클릭하세요.

1. 생성된 버전이 **[!UICONTROL AI 받은 편지함 최적화 도구]** 창에 표시됩니다.

   ![생성된 버전이 AI 받은 편지함에 최적화됨](assets/optimize-ai-inbox-output.png){zoomable="yes" width="80%"}

   >[!NOTE]
   >
   >최적화된 버전은 이메일의 HTML 및 텍스트 보기와 다릅니다. 디자인, 레이아웃 또는 이미지는 변경되지 않습니다.

1. 자동으로 생성된 콘텐츠를 편집하려면 **[!UICONTROL 편집 사용]** 토글을 선택하고 필요에 따라 수동으로 변경합니다.

1. 버전이 마음에 들면 **[!UICONTROL 전자 메일 최적화]** 단추를 클릭하여 확인합니다. **[!UICONTROL 다시 최적화]** 단추를 사용하여 새 버전을 생성할 수도 있습니다.

1. **[!UICONTROL HTML]** 보기로 리디렉션되며 이제 이메일이 AI 받은 편지함에 최적화되었습니다. 최적화된 버전에 다시 액세스하거나 편집하려면 **[!UICONTROL AI 받은 편지함에 최적화됨]** 단추를 클릭하세요.

   ![이메일 Designer의 다시 최적화 단추](assets/optimize-ai-inbox-optimized-button.png){zoomable="yes" width="80%"}

1. 최적화된 버전이 표시됩니다. **[!UICONTROL 최적화를 제거]**&#x200B;하거나 **[!UICONTROL 다시 최적화]**&#x200B;을 클릭하여 새 버전을 생성할 수 있습니다.

   ![이전에 전자 메일 Designer에서 최적화된 버전](assets/optimize-ai-inbox-optimized-version.png){zoomable="yes" width="80%"}

   >[!NOTE]
   >
   >원래 HTML 콘텐츠를 변경하는 경우 새 콘텐츠와 일치하도록 생성된 AI 받은 편지함 버전을 다시 최적화해야 합니다.

## 타사 받은 편지함 AI의 위험 및 제한 사항 {#inbox-ai-risks}

AI 받은 편지함에 대한 전자 메일 최적화 기능을 사용하면 사서함 공급자가 [!DNL Journey Optimizer] 전송을 처리할 수 있는 방법에 대한 전자 메일 버전을 준비하는 데 도움이 됩니다. 이러한 공급자의 제품은 제어하지 않습니다. 메시지가 전달되면 [!DNL Gmail], [!DNL Apple] 메일, [!DNL Outlook] 또는 다른 클라이언트의 모든 AI 기능은 Adobe이 아닌 해당 용어, 모델 및 정책에 따라 작동합니다.

* **예측할 수 없는 프레젠테이션** — 요약, 알림 흐림 및 대화 답변을 생략하거나, 가격 또는 날짜를 잘못 기재하거나, 관련 없는 웹 결과와 콘텐츠를 병합하거나, 더 이상 승인된 복사본과 일치하지 않는 방식으로 대체됩니다. 이 동작은 공급업체가 예고 없이 모델이나 UI를 업데이트할 때 변경될 수 있습니다.

* **HTML과의 동등한 기능을 보장할 수 없음** — 미리 보기나 길잡이 답변을 사용하는 수신자는 사용자의 전체 HTML 디자인, 이미지 또는 법적 절차를 볼 수 없습니다. 그들이 &quot;말하는&quot; 메시지가 AI가 생성한 짧은 요약에서만 나올 수 있다고 믿는 것.

* **개인 정보, 규정 준수 및 데이터 사용** — 받은 편지함 AI가 해당 공급자의 개인 정보 보호 정책, 보존 및 지역 규칙에 따라 공급자 인프라에서 메시지 콘텐츠를 처리할 수 있습니다. 규제 대상 업종의 조직은 [!DNL Journey Optimizer]에서 전자 메일이 작성된 방식과 관계없이 이러한 기능의 수신자 사용이 의무에 영향을 미치는지 여부를 평가해야 합니다.

* **브랜드 및 법적 노출** — 잘못되거나 불완전한 AI 요약으로 인해 여전히 고객 혼란 또는 프로모션, 약관 또는 옵트아웃 언어에 대한 분쟁이 발생할 수 있습니다. [!DNL Journey Optimizer]은(는) 서드파티 모델이 최적화된 버전의 전자 메일을 충실하게 재현할 수 있는지 확인하지 않습니다.

* **[!UICONTROL 의]** AI 받은 편지함에 최적화[!DNL Journey Optimizer] — 전자 메일 Designer의 작성 시간 컨트롤은 최종 사용자 받은 편지함 도우미와 별개입니다. 보내기 전에 항상 생성된 콘텐츠를 검토하십시오.

## 관련 항목 {#related-topics}

* [이메일 디자인 시작](get-started-email-design.md)
* Adobe 생성 기능에 대한 자세한 내용은 [AI Assistant 시작](../content-management/gs-generative.md)을 참조하십시오.
