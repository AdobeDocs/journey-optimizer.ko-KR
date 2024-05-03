---
solution: Journey Optimizer
product: journey optimizer
title: AI 어시스턴트와 함께하는 SMS 세대
description: AI Assistant를 사용하여 SMS 콘텐츠 생성 시작
feature: Content Assistant
topic: Content Management
role: User
level: Beginner
badge: label="Beta" type="Informative"
hide: true
hidefromtoc: true
source-git-commit: 5c4b7cde5514f60f61050837fc9ae325f7bef2e8
workflow-type: tm+mt
source-wordcount: '889'
ht-degree: 8%

---

# AI 어시스턴트와 함께하는 SMS 세대 {#generative-sms}

>[!BEGINSHADEBOX]

**목차**

* [AI 어시스턴트 시작하기](gs-generative.md)
* [AI 어시스턴트로 이메일 생성](generative-email.md)
* [AI 어시스턴트와 함께하는 SMS 세대](generative-sms.md)
* **[AI Assistant를 사용하여 푸시 생성](generative-push.md)**
* [AI Assistant를 사용한 콘텐츠 실험](generative-experimentation.md)

>[!ENDSHADEBOX]

대상의 환경 설정에 맞게 SMS 메시지를 만들고 맞춤화한 후 Journey Optimizer의 AI Assistant와의 커뮤니케이션을 향상시키십시오.

이 리소스는 콘텐츠를 세밀하게 조정할 수 있는 통찰력 있는 권장 사항을 제공하여 메시지가 공감하고 참여를 극대화할 수 있도록 지원합니다.

Journey Optimizer에서 AI Assistant를 사용하는 방법을 알려면 아래 탭을 살펴보십시오.

>[!NOTE]
>
>이 기능의 사용을 시작하기 전에 관련 항목을 읽어 보십시오. [보호 및 제한 사항](gs-generative.md#generative-guardrails).

>[!BEGINTABS]

>[!TAB 전체 SMS 생성]

1. SMS 캠페인을 만들고 구성한 후 **[!UICONTROL 콘텐츠 편집]**.

   SMS 캠페인을 구성하는 방법에 대한 자세한 내용은 다음을 참조하십시오. [이 페이지](../sms/create-sms.md).

1. 다음을 입력합니다. **[!UICONTROL 기본 세부 정보]** 캠페인을 위해 사용됩니다. 완료되면 다음을 클릭합니다. **[!UICONTROL 콘텐츠 편집]**.

1. 필요에 따라 SMS 메시지를 개인화합니다. [자세히 알아보기](../sms/create-sms.md)

1. 액세스 **[!UICONTROL AI Assistant 표시]** 메뉴 아래의 제품에서 사용할 수 있습니다.

   ![](assets/sms-genai-1.png){zoomable=&quot;yes&quot;}

1. 활성화 **[!UICONTROL 원본 컨텐츠 사용]** campaign 콘텐츠, 이름 및 선택한 대상을 기반으로 새 콘텐츠를 개인화할 수 있는 AI 길잡이 옵션입니다.

   프롬프트는 항상 특정 컨텍스트에 연결되어 있어야 합니다.

1. 에서 생성하려는 내용을 설명하여 콘텐츠를 미세 조정합니다. **[!UICONTROL 프롬프트]** 필드.

   메시지를 작성하는 데 도움이 필요한 경우 **[!UICONTROL 프롬프트 라이브러리]** 는 캠페인을 개선하기 위한 다양한 신속한 아이디어를 제공합니다.

   ![](assets/sms-genai-2.png){zoomable=&quot;yes&quot;}

1. 선택 **[!UICONTROL 브랜드 자산 업로드]** 추가 컨텍스트를 제공할 수 있는 콘텐츠가 포함된 브랜드 자산을 AI Assistant에 추가합니다.

1. 프롬프트를 다음과 같은 다양한 옵션으로 사용자 지정합니다.

   * **[!UICONTROL 커뮤니케이션 전략]**: 생성된 텍스트에 대해 원하는 통신 접근 방식을 선택합니다.
   * **[!UICONTROL 언어]**: 변형 콘텐츠의 언어를 선택합니다.
   * **[!UICONTROL 톤]**: 텍스트가 대상자 및 목적에 적합한지 확인합니다.
   * **[!UICONTROL Length]**: 범위 슬라이더를 사용하여 콘텐츠의 길이를 선택합니다.

   ![](assets/sms-genai-3.png){zoomable=&quot;yes&quot;}

1. 프롬프트가 준비되면 다음을 클릭합니다. **[!UICONTROL 생성]**.

1. 생성된 를 통해 찾아보기 **[!UICONTROL 변형]** 및 클릭 **[!UICONTROL 미리 보기]** 선택한 변형의 전체 화면 버전을 보려면 다음과 같이 하십시오.

1. 다음 위치로 이동 **[!UICONTROL 세부 조정]** 내의 옵션 **[!UICONTROL 미리 보기]** 추가 사용자 정의 기능에 액세스하고 변형을 환경 설정에 맞게 세부 조정할 수 있는 창:

   * **[!UICONTROL 참조 콘텐츠로 사용]**: 선택한 변형은 다른 결과를 생성하기 위한 참조 콘텐츠 역할을 합니다.

   * **[!UICONTROL 구문 변경]**:AI Assistant는 다양한 방식으로 메시지를 고쳐 써서 다양한 대상자를 유혹할 수 있습니다.

   * **[!UICONTROL 더 간결한 언어 사용]**: AI Assistant를 사용하여 언어를 단순화함으로써, 보다 많은 대상자가 명확하고 쉽게 사용할 수 있습니다.

   ![](assets/sms-genai-4.png){zoomable=&quot;yes&quot;}

1. 클릭 **[!UICONTROL 선택]** 적절한 콘텐츠를 찾았으면

   콘텐츠에 대한 실험을 활성화할 수도 있습니다. [자세히 알아보기](generative-experimentation.md)

1. 개인화 필드를 삽입하여 프로필 데이터를 기반으로 SMS 콘텐츠를 사용자 지정합니다. [콘텐츠 개인화에 대해 자세히 알아보기](../personalization/personalize.md)

1. 메시지 콘텐츠를 정의한 후 **[!UICONTROL 콘텐츠 시뮬레이션]** 단추를 클릭하여 렌더링을 제어하고 테스트 프로필로 개인화 설정을 확인합니다. [자세히 알아보기](../personalization/personalize.md)

콘텐츠, 대상자 및 일정을 정의했으면 SMS 캠페인을 준비할 준비가 되었습니다. [자세히 알아보기](../campaigns/review-activate-campaign.md)

>[!TAB 텍스트 생성]

1. SMS 캠페인을 만들고 구성한 후 **[!UICONTROL 콘텐츠 편집]**.

   SMS 캠페인을 구성하는 방법에 대한 자세한 내용은 다음을 참조하십시오. [이 페이지](../sms/create-sms.md).

1. 다음을 입력합니다. **[!UICONTROL 기본 세부 정보]** 캠페인을 위해 사용됩니다. 완료되면 다음을 클릭합니다. **[!UICONTROL 콘텐츠 편집]**.

1. 필요에 따라 SMS 메시지를 개인화합니다. [자세히 알아보기](../sms/create-sms.md)

1. 액세스 **[!UICONTROL AI Assistant를 사용하여 텍스트 편집]** 메뉴 옆에 있는 **[!UICONTROL 메시지]** 필드.

   ![](assets/sms-text-genai-1.png){zoomable=&quot;yes&quot;}

1. 활성화 **[!UICONTROL 참조 콘텐츠 사용]** campaign 콘텐츠, 이름 및 선택한 대상을 기반으로 새 콘텐츠를 개인화할 수 있는 AI 길잡이 옵션입니다.

   프롬프트는 항상 특정 컨텍스트에 연결되어 있어야 합니다.

1. 에서 생성하려는 내용을 설명하여 콘텐츠를 미세 조정합니다. **[!UICONTROL 프롬프트]** 필드.

   메시지를 작성하는 데 도움이 필요한 경우 **[!UICONTROL 프롬프트 라이브러리]** 는 캠페인을 개선하기 위한 다양한 신속한 아이디어를 제공합니다.

   ![](assets/sms-text-genai-1.png){zoomable=&quot;yes&quot;}

1. 선택 **[!UICONTROL 브랜드 자산 업로드]** 추가 컨텍스트를 제공할 수 있는 콘텐츠가 포함된 브랜드 자산을 AI Assistant에 추가합니다.

1. 프롬프트를 다음과 같은 다양한 옵션으로 사용자 지정합니다.

   * **[!UICONTROL 커뮤니케이션 전략]**: 생성된 텍스트에 대해 원하는 통신 접근 방식을 선택합니다.
   * **[!UICONTROL 언어]**: 변형 콘텐츠의 언어를 선택합니다.
   * **[!UICONTROL 톤]**: 텍스트가 대상자 및 목적에 적합한지 확인합니다.
   * **[!UICONTROL Length]**: 범위 슬라이더를 사용하여 콘텐츠의 길이를 선택합니다.

   ![](assets/sms-text-genai-3.png){zoomable=&quot;yes&quot;}

1. 프롬프트가 준비되면 다음을 클릭합니다. **[!UICONTROL 생성]**.

1. 생성된 를 통해 찾아보기 **[!UICONTROL 변형]** 및 클릭 **[!UICONTROL 미리 보기]** 선택한 변형의 전체 화면 버전을 보려면 다음과 같이 하십시오.

1. 다음 위치로 이동 **[!UICONTROL 세부 조정]** 내의 옵션 **[!UICONTROL 미리 보기]** 추가 사용자 정의 기능에 액세스하고 변형을 환경 설정에 맞게 세부 조정할 수 있는 창:

   * **[!UICONTROL 참조 콘텐츠로 사용]**: 선택한 변형은 다른 결과를 생성하기 위한 참조 콘텐츠 역할을 합니다.

   * **[!UICONTROL 구문 변경]**:AI Assistant는 다양한 방식으로 메시지를 고쳐 써서 다양한 대상자를 유혹할 수 있습니다.

   * **[!UICONTROL 더 간결한 언어 사용]**: AI Assistant를 사용하여 언어를 단순화함으로써, 보다 많은 대상자가 명확하고 쉽게 사용할 수 있습니다.

   ![](assets/sms-text-genai-4.png){zoomable=&quot;yes&quot;}

1. 클릭 **[!UICONTROL 선택]** 적절한 콘텐츠를 찾았으면

   콘텐츠에 대한 실험을 활성화할 수도 있습니다. [자세히 알아보기](generative-experimentation.md)

1. 개인화 필드를 삽입하여 프로필 데이터를 기반으로 SMS 콘텐츠를 사용자 지정합니다. [콘텐츠 개인화에 대해 자세히 알아보기](../personalization/personalize.md)

1. 메시지 콘텐츠를 정의한 후 **[!UICONTROL 콘텐츠 시뮬레이션]** 단추를 클릭하여 렌더링을 제어하고 테스트 프로필로 개인화 설정을 확인합니다.

콘텐츠, 대상자 및 일정을 정의했으면 SMS 캠페인을 준비할 준비가 되었습니다. [자세히 알아보기](../campaigns/review-activate-campaign.md)

>[!ENDTABS]
