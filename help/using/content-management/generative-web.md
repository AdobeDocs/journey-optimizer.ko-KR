---
solution: Journey Optimizer
product: journey optimizer
title: AI Assistant를 사용하여 웹 페이지 생성
description: AI Assistant를 사용하여 웹 페이지 컨텐츠 및 자산 생성 시작
feature: Content Assistant
topic: Content Management
role: User
level: Beginner
badge: label="Beta" type="Informative"
hide: true
hidefromtoc: true
source-git-commit: b62f8954e09f50896ad5e70784c5a93943617e85
workflow-type: tm+mt
source-wordcount: '1320'
ht-degree: 5%

---

# AI Assistant를 사용하여 웹 페이지 생성 {#generative-web}

>[!BEGINSHADEBOX]

**목차**

* [AI 어시스턴트 시작하기](gs-generative.md)
* [AI 어시스턴트로 이메일 생성](generative-email.md)
* [AI 어시스턴트와 함께하는 SMS 세대](generative-SMS.md)
* [AI Assistant를 사용하여 푸시 생성](generative-push.md)
* AI Assistant를 사용하여 웹 페이지 생성
* [AI Assistant를 사용한 콘텐츠 실험](generative-experimentation.md)

>[!ENDSHADEBOX]

이메일을 만들고 개인화한 후에는 생성 AI에서 제공하는 Adobe Journey Optimizer의 AI Assistant를 사용하여 콘텐츠를 한 차원 높입니다.

AI 도우미는 대상자에게 반향을 일으킬 가능성이 높은 다양한 콘텐츠를 제안하여 게재의 영향을 최적화하는 데 도움이 됩니다.

>[!NOTE]
>
>이 기능의 사용을 시작하기 전에 관련 항목을 읽어 보십시오. [보호 및 제한 사항](generative-gs.md#guardrails-and-limitations).

>[!BEGINTABS]

>[!TAB 웹 페이지 전체 생성]

다음 예에서는 AI 도우미를 활용하여 기존 이메일을 구체화하고, 특별한 이벤트를 위해 사용자 지정합니다.

1. 이메일 게재를 만들고 구성한 후 **[!UICONTROL 콘텐츠 편집]**.

   이메일 게재를 구성하는 방법에 대한 자세한 내용은 을(를) 참조하십시오. [이 페이지](../email/create-email-content.md).

1. 필요에 따라 이메일을 개인화하고 **[!UICONTROL AI Assistant]** 메뉴 아래의 제품에서 사용할 수 있습니다.

   ![](assets/full-email-1.png){zoomable=&quot;yes&quot;}

1. 활성화 **[!UICONTROL 원본 컨텐츠 사용]** ai 비서가 게재, 게재명 및 선택한 대상자를 기반으로 새 콘텐츠를 개인화할 수 있는 옵션.

   프롬프트는 항상 특정 컨텍스트에 연결되어 있어야 합니다.

1. 에서 생성하려는 내용을 설명하여 콘텐츠를 미세 조정합니다. **[!UICONTROL 프롬프트]** 필드.

   메시지를 작성하는 데 도움이 필요한 경우 **[!UICONTROL 프롬프트 라이브러리]** 게재를 개선하기 위한 다양한 신속한 아이디어를 제공합니다.

   ![](assets/full-email-2.png){zoomable=&quot;yes&quot;}

1. 다음을 전환할 수 있습니다. **[!UICONTROL 제목 줄]** 또는 **[!UICONTROL 사전 머리글]** 변형 생성에 포함할 수 있습니다.

1. 클릭 **[!UICONTROL 브랜드 자산 업로드]** 추가 컨텍스트를 제공할 수 있는 콘텐츠가 포함된 브랜드 자산을 AI Assistant에 추가하거나 이전에 업로드한 자산을 선택합니다.

   ![](assets/full-email-3.png){zoomable=&quot;yes&quot;}

1. 프롬프트를 다음과 같은 다양한 옵션으로 사용자 지정합니다.

   * **[!UICONTROL 커뮤니케이션 전략]**: 생성된 텍스트에 가장 적합한 커뮤니케이션 스타일을 선택합니다.
   * **[!UICONTROL 언어]**: 콘텐츠를 생성할 언어를 선택합니다.
   * **[!UICONTROL 톤]**: 이메일의 톤은 대상자에게 울려 퍼져야 합니다. AI 어시스턴트는 여러분이 유익하거나, 장난스럽거나, 설득력 있게 들리기를 원하든 상관없이 메시지를 그에 따라 조정할 수 있습니다.
   * **[!UICONTROL Length]**: 범위 슬라이더를 사용하여 원하는 콘텐츠 길이를 선택합니다.

   ![](assets/full-email-4.png){zoomable=&quot;yes&quot;}

1. 프롬프트가 준비되면 다음을 클릭합니다. **[!UICONTROL 생성]**.

1. 생성된 를 통해 찾아보기 **[!UICONTROL 변형]** 및 클릭 **[!UICONTROL 미리 보기]** 선택한 변형의 전체 화면 버전을 보려면 다음과 같이 하십시오.

1. 다음 위치로 이동 **[!UICONTROL 세부 조정]** 내의 옵션 **[!UICONTROL 미리 보기]** 추가 사용자 지정 기능에 액세스하기 위한 창:

   * **[!UICONTROL 구문 변경]**: AI Assistant는 다양한 방식으로 메시지를 고쳐 써서 다양한 대상자를 유혹할 수 있습니다.

   * **[!UICONTROL 간단한 언어 사용]**: AI Assistant를 사용하여 언어를 단순화함으로써, 보다 많은 대상자가 명확하고 쉽게 사용할 수 있습니다.

   ![](assets/full-email-5.png){zoomable=&quot;yes&quot;}

1. 클릭 **[!UICONTROL 선택]** 적절한 콘텐츠를 찾았으면

1. 개인화 필드를 삽입하여 프로필 데이터를 기반으로 이메일 콘텐츠를 사용자 정의합니다. 그런 다음 **[!UICONTROL 콘텐츠 시뮬레이션]** 단추를 클릭하여 렌더링을 제어하고 테스트 프로필로 개인화 설정을 확인합니다. [자세히 알아보기](../preview-test/preview-content.md)

   ![](assets/full-email-6.png){zoomable=&quot;yes&quot;}

콘텐츠, 대상자 및 일정을 정의했으면 이메일 게재를 준비할 준비가 되었습니다. [자세히 알아보기](../monitor/prepare-send.md)

>[!TAB 웹 페이지 텍스트 생성]

다음 예에서는 AI 도우미를 활용하여 예정된 이벤트에 대한 이메일 초대 콘텐츠를 개선합니다.

1. 이메일 게재를 만들고 구성한 후 **[!UICONTROL 콘텐츠 편집]**.

   이메일 게재를 구성하는 방법에 대한 자세한 내용은 을(를) 참조하십시오. [이 페이지](../email/create-email-content.md).

1. 선택 **[!UICONTROL 텍스트 구성 요소]** 특정 콘텐츠만 타겟팅할 수 있습니다. 및 액세스 **[!UICONTROL AI Assistant]** 메뉴 아래의 제품에서 사용할 수 있습니다.

   ![](assets/text-genai-1.png){zoomable=&quot;yes&quot;}

1. 활성화 **[!UICONTROL 원본 컨텐츠 사용]** ai 비서가 게재, 게재명 및 선택한 대상자를 기반으로 새 콘텐츠를 개인화할 수 있는 옵션.

   프롬프트는 항상 특정 컨텍스트에 연결되어 있어야 합니다.

1. 에서 생성하려는 내용을 설명하여 콘텐츠를 미세 조정합니다. **[!UICONTROL 프롬프트]** 필드.

   메시지를 작성하는 데 도움이 필요한 경우 **[!UICONTROL 프롬프트 라이브러리]** 게재를 개선하기 위한 다양한 신속한 아이디어를 제공합니다.

   ![](assets/text-genai-2.png){zoomable=&quot;yes&quot;}

1. 클릭 **[!UICONTROL 브랜드 자산 업로드]** 추가 컨텍스트를 제공할 수 있는 콘텐츠가 포함된 브랜드 자산을 AI Assistant에 추가합니다.

   ![](assets/text-genai-3.png){zoomable=&quot;yes&quot;}

1. 프롬프트를 다음과 같은 다양한 옵션으로 사용자 지정합니다.

   * **[!UICONTROL 커뮤니케이션 전략]**: 생성된 텍스트에 대해 원하는 통신 접근 방식을 선택합니다.
   * **[!UICONTROL 언어]**: 변형 콘텐츠의 언어를 선택합니다.
   * **[!UICONTROL 톤]**: 텍스트가 대상자 및 목적에 적합한지 확인합니다.
   * **[!UICONTROL Length]**: 범위 슬라이더를 사용하여 콘텐츠의 길이를 선택합니다.

   ![](assets/text-genai-4.png){zoomable=&quot;yes&quot;}

1. 프롬프트가 준비되면 다음을 클릭합니다. **[!UICONTROL 생성]**.

1. 생성된 를 통해 찾아보기 **[!UICONTROL 변형]** 및 클릭 **[!UICONTROL 미리 보기]** 선택한 변형의 전체 화면 버전을 보려면 다음과 같이 하십시오.

1. 다음 위치로 이동 **[!UICONTROL 세부 조정]** 내의 옵션 **[!UICONTROL 미리 보기]** 추가 사용자 지정 기능에 액세스하기 위한 창:

   * **참조 콘텐츠로 사용**: 선택한 변형은 다른 결과를 생성하기 위한 참조 콘텐츠 역할을 합니다.

   * **정교하**: AI Assistant를 사용하면 특정 주제를 확장하고 더 나은 이해와 참여를 위해 추가 세부 정보를 제공할 수 있습니다.

   * **요약**: 정보가 길면 이메일 수신자에게 과부하가 걸릴 수 있습니다. AI Assistant를 사용하여 주요 사항을 명확하고 간결한 요약으로 요약하여 주목 받고 더 자세히 읽을 수 있도록 장려합니다.

   * **구문 변경**:AI Assistant는 다양한 방식으로 메시지를 고쳐 써서 다양한 대상자를 유혹할 수 있습니다.

   * **간단한 언어 사용**: AI Assistant를 사용하여 언어를 단순화함으로써, 보다 많은 대상자가 명확하고 쉽게 사용할 수 있습니다.

   ![](assets/text-genai-5.png){zoomable=&quot;yes&quot;}

1. 클릭 **[!UICONTROL 선택]** 적절한 콘텐츠를 찾았으면

1. 개인화 필드를 삽입하여 프로필 데이터를 기반으로 이메일 콘텐츠를 사용자 정의합니다. 그런 다음 **[!UICONTROL 콘텐츠 시뮬레이션]** 단추를 클릭하여 렌더링을 제어하고 테스트 프로필로 개인화 설정을 확인합니다. [자세히 알아보기](../preview-test/preview-content.md)

   ![](assets/text-genai-7.png){zoomable=&quot;yes&quot;}

콘텐츠, 대상자 및 일정을 정의했으면 이메일 게재를 준비할 준비가 되었습니다. [자세히 알아보기](../monitor/prepare-send.md)

>[!TAB 웹 페이지 이미지 생성]

아래 예에서는 AI Assistant를 활용하여 에셋을 최적화하고 개선하여 보다 사용자 친화적인 경험을 제공하는 방법에 대해 알아봅니다.

1. 이메일 게재를 만들고 구성한 후 **[!UICONTROL 콘텐츠 편집]**.

   이메일 게재를 구성하는 방법에 대한 자세한 내용은 을(를) 참조하십시오. [이 페이지](../email/create-email-content.md).

1. 다음을 입력합니다. **[!UICONTROL 기본 세부 정보]** 게재를 위해. 완료되면 다음을 클릭합니다. **[!UICONTROL 이메일 콘텐츠 편집]**.

1. AI Assistant를 사용하여 변경할 에셋을 선택합니다.

1. 오른쪽 메뉴에서 **[!UICONTROL AI Assistant]**.

   ![](assets/image-genai-1.png){zoomable=&quot;yes&quot;}

1. 에서 생성하려는 내용을 설명하여 콘텐츠를 미세 조정합니다. **[!UICONTROL 프롬프트]** 필드.

   메시지를 작성하는 데 도움이 필요한 경우 **[!UICONTROL 프롬프트 라이브러리]** 게재를 개선하기 위한 다양한 신속한 아이디어를 제공합니다.

   ![](assets/image-genai-2.png){zoomable=&quot;yes&quot;}

1. 클릭 **[!UICONTROL 브랜드 자산 업로드]** 추가 컨텍스트를 제공할 수 있는 콘텐츠가 포함된 브랜드 자산을 AI Assistant에 추가합니다.

   프롬프트는 항상 특정 컨텍스트에 연결되어 있어야 합니다.

1. 프롬프트를 다음과 같은 다양한 옵션으로 사용자 지정합니다.

   * **[!UICONTROL 종횡비]**: 에셋의 너비와 높이를 결정합니다. 16:9, 4:3, 3:2 또는 1:1과 같은 일반적인 비율 중에서 선택할 수 있는 옵션이 있거나 사용자 지정 크기를 입력할 수 있습니다.
   * **[!UICONTROL 색상 및 톤]**: 이미지 내의 전체 색상 모양과 전달하는 분위기 또는 분위기.
   * **[!UICONTROL 컨텐츠 유형]**: 사진, 그래픽 또는 예술과 같은 다양한 형식의 시각적 표현을 구별하여 시각적 요소의 특성을 분류합니다.
   * **[!UICONTROL 조명]**: 이미지에 있는 번개를 말하며, 분위기를 형성하고 특정 요소를 강조 표시합니다.
   * **[!UICONTROL 컴포지션]**: 이미지 프레임 내의 요소 배열을 말합니다

   ![](assets/image-genai-3.png){zoomable=&quot;yes&quot;}

1. 프롬프트 구성이 만족스러우면 **[!UICONTROL 생성]**.

1. 찾아보기 **[!UICONTROL 변형 제안]** 원하는 자산을 찾습니다.

   클릭 **[!UICONTROL 미리 보기]** 선택한 변형의 전체 화면 버전을 보려면 다음과 같이 하십시오.

   ![](assets/image-genai-5.png){zoomable=&quot;yes&quot;}

1. 선택 **[!UICONTROL 유사 항목 표시]** 이 변형과 관련된 이미지를 보려는 경우.

1. 클릭 **[!UICONTROL 선택]** 적절한 콘텐츠를 찾았으면

   ![](assets/image-genai-6.png){zoomable=&quot;yes&quot;}

1. 메시지 콘텐츠를 정의한 후 **[!UICONTROL 콘텐츠 시뮬레이션]** 단추를 클릭하여 렌더링을 제어하고 테스트 프로필로 개인화 설정을 확인합니다.  [자세히 알아보기](../preview-test/preview-content.md)

   ![](assets/image-genai-7.png){zoomable=&quot;yes&quot;}

1. 콘텐츠, 대상자 및 일정을 정의했으면 이메일 게재를 준비할 준비가 되었습니다. [자세히 알아보기](../monitor/prepare-send.md)

>[!ENDTABS]

