---
solution: Journey Optimizer
product: journey optimizer
title: AI Assistant를 사용하여 이미지 생성
description: Journey Optimizer에서 AI Assistant를 사용하여 이미지를 생성하는 방법을 알아봅니다.
feature: Content Assistant
topic: Content Management
role: User
level: Beginner
source-git-commit: b70911f1f1fa00154729b5b88517233b67a377cb
workflow-type: tm+mt
source-wordcount: '1414'
ht-degree: 2%

---

# AI Assistant를 사용하여 이미지 생성 {#generative-image}

>[!IMPORTANT]
>
>이 기능을 사용하기 전에 관련 [보호 및 제한 사항](gs-generative.md#generative-guardrails)을 읽어보십시오.
></br>
>
>Journey Optimizer에서 AI Assistant를 사용하려면 [사용자 계약](https://www.adobe.com/kr/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html)에 동의해야 합니다. 자세한 내용은 Adobe 담당자에게 문의하십시오.

Journey Optimizer의 AI Assistant를 사용하여 이메일, 웹, 랜딩 페이지 및 푸시 알림에서 메시지를 향상시키는 매력적인 시각적 콘텐츠를 생성할 수 있습니다. AI Assistant를 사용하면 에셋을 최적화하고 개선할 수 있으므로 대상자에게 보다 사용자 친화적이고 매력적인 경험을 제공할 수 있습니다.

## 이메일 및 웹 채널용 {#email-web-channels}

AI Assistant는 이메일 캠페인, 웹 경험 및 랜딩 페이지에 대한 완전한 시각적 경험을 생성할 수 있습니다. 이 기능을 사용하면 디지털 터치포인트에서 대상자와 공감하는 온브랜드, 주목을 끄는 이미지를 만들 수 있습니다.

### 액세스 및 구성 {#access-configure}

AI Assistant를 사용하여 이미지 생성을 시작하려면 먼저 캠페인이나 여정을 설정하고 콘텐츠 편집기를 엽니다. 아래 단계에 따라 작업 영역을 준비하고 AI Assistant 패널에 액세스합니다.

1. 캠페인 또는 여정 만들기 및 구성:
   * **전자 메일**: 전자 메일 캠페인을 만들고 구성한 후 **[!UICONTROL 콘텐츠 편집]**&#x200B;을 클릭하세요. [자세히 알아보기](../email/create-email.md)
   * **웹**: 웹 페이지를 만들고 구성한 후 **[!UICONTROL 웹 페이지 편집]**&#x200B;을 클릭하세요. [자세히 알아보기](../web/create-web.md)
   * **랜딩 페이지**: 랜딩 페이지를 만들고 구성한 후 **[!UICONTROL 디자이너 열기]**&#x200B;를 클릭합니다. [자세히 알아보기](../landing-pages/create-lp.md)

1. AI Assistant를 사용하여 변경할 에셋을 선택합니다.

1. 오른쪽 메뉴에서 **[!UICONTROL AI 길잡이]**(또는 **[!UICONTROL 웹용 콘텐츠 길잡이 표시]**)를 선택합니다.

   ![이미지 자산을 선택하고 AI 도우미 패널을 열었습니다](assets/image-genai-1.png){zoomable="yes"}

### 콘텐츠 생성 {#generate-content}

AI Assistant를 사용하여 효과적인 프롬프트를 작성하고 이미지 설정을 구성하여 시각적으로 매력적인 이미지를 생성하는 방법에 대해 알아봅니다. 종횡비, 시각적 강도 및 조명과 같은 매개 변수를 사용자 지정하여 브랜드 및 캠페인 목표에 맞는 이미지를 만들 수 있습니다.

1. AI 관리자가 참조 콘텐츠를 기반으로 새 콘텐츠를 개인화하려면 **[!UICONTROL 참조 스타일]** 옵션을 활성화하십시오. 이미지를 업로드하여 변형에 컨텍스트를 추가할 수도 있습니다.

1. AI 생성 콘텐츠가 브랜드 사양에 맞게 조정되도록 하려면 **[!UICONTROL 브랜드]**&#x200B;를 선택하십시오. 브랜드에 대해 [자세히 알아보기](brands.md).

1. **[!UICONTROL 프롬프트]** 필드에 생성할 내용을 설명하여 내용을 미세 조정하십시오.

   프롬프트 작성에 도움이 필요한 경우 캠페인을 개선하기 위한 다양한 프롬프트 아이디어를 제공하는 **[!UICONTROL 프롬프트 라이브러리]**&#x200B;에 액세스하십시오.

   ![옵션이 있는 AI Assistant 이미지 생성 패널](assets/image-genai-2.png){zoomable="yes"}

1. **[!UICONTROL 이미지 설정]** 옵션을 사용하여 메시지를 사용자 지정합니다.

   * **[!UICONTROL 종횡비]**: 에셋의 너비와 높이를 결정합니다. 16:9, 4:3, 3:2 또는 1:1과 같은 일반적인 비율 중에서 선택할 수 있는 옵션이 있거나 사용자 지정 크기를 입력할 수 있습니다.
   * **[!UICONTROL 콘텐츠 형식]**: 이 옵션은 시각적 요소의 특성을 분류하여 사진, 그래픽 또는 미술과 같은 시각적 표현의 다른 형식을 구분합니다.
   * **[!UICONTROL 시각적 강도]**: 이미지의 강도를 조정하여 이미지의 영향을 제어할 수 있습니다. 낮은 설정 (2)는 부드럽고 절제된 모양을 만들고, 높은 설정 (10)은 이미지를 더 생동감 있고 시각적으로 강력하게 만듭니다.
   * **[!UICONTROL 색상 및 색조]**: 이미지 내의 전체 색상 모양과 이미지 내의 분위기 또는 분위기를 전달합니다.
   * **[!UICONTROL 조명]**: 이미지에 있는 번개(대기의 모양과 특정 요소의 강조 표시)를 나타냅니다.
   * **[!UICONTROL 컴포지션]**: 이미지 프레임 내의 요소 배열을 참조합니다

     컨트롤이 있는 ![이미지 설정 패널](assets/image-genai-4.png){zoomable="yes"}

1. **[!UICONTROL 참조 콘텐츠]** 메뉴에서 **[!UICONTROL 파일 업로드]**&#x200B;를 클릭하여 추가 컨텍스트 AI 도우미를 제공할 수 있는 콘텐츠가 포함된 브랜드 자산을 추가하거나 이전에 업로드한 콘텐츠를 선택합니다.

   이전에 업로드한 파일은 **[!UICONTROL 업로드된 참조 콘텐츠]** 드롭다운에서 사용할 수 있습니다. 세대에 포함할 자산을 전환하기만 하면 됩니다.

1. 프롬프트 구성에 만족하면 **[!UICONTROL 생성]**&#x200B;을 클릭합니다.

### 세분화 및 완료 {#refine-finalize}

이미지 변형을 생성한 후 결과를 검토하고, 브랜드 정렬을 확인하고, Adobe Express에서 편집하고, 콘텐츠에 가장 적합한 옵션을 선택할 수 있습니다.

1. **[!UICONTROL 변형 제안]**&#x200B;을 검색하여 원하는 자산을 찾습니다.

1. 백분율 아이콘을 클릭하여 **[!UICONTROL 브랜드 맞춤 점수]**&#x200B;를 보고 브랜드에 대한 모든 오정렬을 식별합니다.

   [브랜드 정렬 점수](brands-score.md)에 대해 자세히 알아보세요.

   ![변형에 대한 브랜드 정렬 점수](assets/image-genai-6.png){zoomable="yes"}

1. 선택한 변형의 전체 화면 버전을 보려면 **[!UICONTROL 미리 보기]**&#x200B;를 클릭하고 현재 콘텐츠를 바꾸려면 **[!UICONTROL 적용]**&#x200B;을 클릭하십시오.

1. 추가 사용자 지정 기능에 액세스하려면 **[!UICONTROL 미리 보기]** 창 내에서 **[!UICONTROL 다시 정의]** 옵션으로 이동하십시오.

   * 이 변형과 관련된 이미지를 보려면 **[!UICONTROL 유사한 이미지를 생성]**&#x200B;하십시오.
   * 에셋을 추가로 사용자 지정하려면 **[!UICONTROL Adobe Express에서 편집]**&#x200B;하십시오.

[Adobe Express 통합에 대해 자세히 알아보기](../integrations/express.md)

   * 나중에 액세스할 수 있도록 자산을 저장하려면 **[!UICONTROL 저장]**&#x200B;하세요.

     ![사용 가능한 작업을 표시하는 옵션 세분화](assets/image-genai-5.png){zoomable="yes"}

1. 적절한 콘텐츠를 찾으면 **[!UICONTROL 선택]**&#x200B;을 클릭합니다.

   콘텐츠에 대한 실험을 활성화할 수도 있습니다. [자세히 알아보기](generative-experimentation.md)

1. 메시지 콘텐츠를 정의한 후 **[!UICONTROL 콘텐츠 시뮬레이션]** 단추를 클릭하여 렌더링을 제어하고 테스트 프로필로 개인화 설정을 확인합니다. [자세히 알아보기](../personalization/personalize.md)

1. 콘텐츠를 검토하고 활성화합니다.
   * **이메일**: 콘텐츠, 대상자 및 일정을 정의했으면 이메일 캠페인을 준비할 준비가 되었습니다. [자세히 알아보기](../campaigns/review-activate-campaign.md)
   * **웹**: 웹 캠페인 설정을 정의하고 원하는 대로 콘텐츠를 편집한 후에는 웹 캠페인을 검토하고 활성화할 수 있습니다. [자세히 알아보기](../web/create-web.md#activate-web-campaign)
   * **랜딩 페이지**: 랜딩 페이지가 준비되면 이를 게시하여 메시지에 사용할 수 있도록 할 수 있습니다. [자세히 알아보기](../landing-pages/create-lp.md#publish-landing-page)

## 모바일 채널용 {#mobile-channels}

AI Assistant를 사용하면 푸시 알림에 대한 매력적인 이미지를 생성할 수 있으므로 대상을 포착하고 공감하는 시각적으로 매력적인 모바일 커뮤니케이션을 만들 수 있습니다.

### 액세스 및 구성 {#mobile-access-configure}

푸시 알림에 AI 비서를 사용하려면 푸시 게재를 설정하고 콘텐츠 편집기로 이동해야 합니다. 다음 단계는 게재를 만들고 AI Assistant 기능에 액세스하는 과정을 안내합니다.

1. 푸시 알림 게재를 만들고 구성한 후 **[!UICONTROL 콘텐츠 편집]**&#x200B;을 클릭합니다.

   푸시 게재 구성에 대한 자세한 내용은 [이 페이지](../push/create-push.md)를 참조하세요.

1. 필요에 따라 푸시 알림을 개인화합니다. [자세히 알아보기](../push/design-push.md)

1. **[!UICONTROL AI Assistant 표시]** 메뉴에 액세스합니다.

   ![AI Assistant 메뉴 표시를 보여주는 스크린샷](assets/push-genai-1.png){zoomable="yes"}

### 콘텐츠 생성 {#mobile-generate-content}

AI Assistant에 액세스한 후 생성 설정을 조정하여 내 브랜드에 맞는 이미지를 만들고 푸시 알림 목표를 지원할 수 있습니다. 모바일 디스플레이에 최적화된 시각적 개체를 생성하도록 프롬프트 및 이미지 매개 변수를 구성합니다.

1. AI 생성 콘텐츠가 브랜드 사양에 맞게 조정되도록 하려면 **[!UICONTROL 브랜드]**&#x200B;를 선택하십시오. 브랜드에 대해 [자세히 알아보기](brands.md).

   브랜드 기능은 비공개 베타로 출시되며 모든 고객은 향후 릴리스에서 점진적으로 사용할 수 있습니다.

1. **[!UICONTROL 프롬프트]** 필드에 생성할 내용을 설명하여 내용을 미세 조정하십시오.

   프롬프트 작성에 도움이 필요한 경우 캠페인을 개선하기 위한 다양한 프롬프트 아이디어를 제공하는 **[!UICONTROL 프롬프트 라이브러리]**&#x200B;에 액세스하십시오.

   ![푸시용 AI 길잡이 이미지 생성](assets/push-gen-img.png){zoomable="yes"}

1. 생성할 필드로 **[!UICONTROL 이미지]**&#x200B;을(를) 선택하십시오.

1. **[!UICONTROL 이미지 설정]** 선택:

   * **[!UICONTROL 콘텐츠 형식]**: 이 옵션은 시각적 요소의 특성을 분류하여 사진, 그래픽 또는 미술과 같은 시각적 표현의 다른 형식을 구분합니다.
   * **[!UICONTROL 시각적 강도]**: 이미지의 강도를 조정하여 이미지의 영향을 제어할 수 있습니다. 낮은 설정 (2)는 부드럽고 절제된 모양을 만들고, 높은 설정 (10)은 이미지를 더 생동감 있고 시각적으로 강력하게 만듭니다.
   * **[!UICONTROL 색상 및 색조]**: 이미지 내의 전체 색상 모양과 이미지 내의 분위기 또는 분위기를 전달합니다.
   * **[!UICONTROL 조명]**: 이미지에 있는 번개(대기의 모양과 특정 요소의 강조 표시)를 나타냅니다.
   * **[!UICONTROL 컴포지션]**: 이미지 프레임 내의 요소 배열을 참조합니다

     ![푸시용 AI 길잡이 이미지 생성](assets/push-gen-img-3.png){zoomable="yes"}

1. **[!UICONTROL 참조 콘텐츠]** 메뉴에서 **[!UICONTROL 파일 업로드]**&#x200B;를 클릭하여 추가 컨텍스트 AI 도우미를 제공할 수 있는 콘텐츠가 포함된 브랜드 자산을 추가하거나 이전에 업로드한 콘텐츠를 선택합니다.

   이전에 업로드한 파일은 **[!UICONTROL 업로드된 참조 콘텐츠]** 드롭다운에서 사용할 수 있습니다. 세대에 포함할 자산을 전환하기만 하면 됩니다.

1. 메시지가 준비되면 **[!UICONTROL 생성]**&#x200B;을 클릭합니다.

### 세분화 및 완료 {#mobile-refine-finalize}

푸시 알림에 대한 이미지 변형을 생성한 후 결과를 미세 조정하여 정확한 요구 사항을 충족할 수 있습니다. 브랜드 정렬을 검토하고 필요한 경우 Adobe Express에서 편집한 다음 모바일 캠페인에 가장 적합한 이미지를 선택합니다.

1. 생성된 **[!UICONTROL 변형]**&#x200B;을 검색합니다.

1. 백분율 아이콘을 클릭하여 **[!UICONTROL 브랜드 맞춤 점수]**&#x200B;를 보고 브랜드에 대한 모든 오정렬을 식별합니다.

   [브랜드 정렬 점수](brands-score.md)에 대해 자세히 알아보세요.

   ![변형에 대한 브랜드 정렬 점수](assets/q.png){zoomable="yes"}

1. 선택한 변형의 전체 화면 버전을 보려면 **[!UICONTROL 미리 보기]**&#x200B;를 클릭하고 현재 콘텐츠를 바꾸려면 **[!UICONTROL 적용]**&#x200B;을 클릭하십시오.

1. **[!UICONTROL 브랜드 정렬]** 탭을 열어 콘텐츠가 [브랜드 지침](brands.md)에 어떻게 적합한지 확인합니다.

1. 적절한 콘텐츠를 찾으면 **[!UICONTROL 선택]**&#x200B;을 클릭합니다.

   콘텐츠에 대한 실험을 활성화할 수도 있습니다. [자세히 알아보기](generative-experimentation.md)

콘텐츠, 대상자 및 일정을 정의했으면 푸시 캠페인을 준비할 준비가 되었습니다. [자세히 알아보기](../campaigns/review-activate-campaign.md)

