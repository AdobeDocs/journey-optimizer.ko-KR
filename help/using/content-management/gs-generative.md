---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer Content Accelerator에서 AI Assistant 시작
description: Journey Optimizer Content Accelerator에서 AI Assistant에 액세스하고 사용하는 방법을 알아봅니다
feature: Content Assistant
topic: Content Management
role: User
level: Beginner
exl-id: 6e291ce3-f324-4e5d-975b-5229dea4d581
source-git-commit: a531f4b0a9f3fbc3185a0e84d9c2634e3b589011
workflow-type: tm+mt
source-wordcount: '883'
ht-degree: 42%

---

# AI Assistant Content Accelerator 시작 {#gs-content-assistant}

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_settings"
>title="Journey Optimizer for Content Acceleration의 AI Assistant"
>abstract="게재를 제작하고 개인화하면 Journey Optimizer for Content Acceleration의 AI Assistant를 사용하여 콘텐츠를 향상시킬 수 있습니다. 이 기능을 사용하면 생성하려는 내용을 설명하여 콘텐츠를 더욱 세부적으로 조정할 수 있어 개인화 및 콘텐츠 개선 프로세스가 간소화됩니다."

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_context"
>title="브랜드 자산 업로드"
>abstract="브랜드 에셋 업로드 메뉴를 사용하면 Journey Optimizer for Content Acceleration에서 AI Assistant에 대한 추가 컨텍스트를 제공할 수 있는 콘텐츠가 포함된 브랜드 에셋을 추가하거나 이전에 업로드한 에셋을 선택할 수 있습니다. 이 옵션을 사용하면 AI 어시스턴트가 필요한 모든 자료에 액세스하여 기능을 개선하고 보다 연관성 있는 답변을 제공할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_start"
>title="Adobe 생성형 AI 약관"
>abstract="이 기능에 대한 액세스 가능 여부는 Adobe Experience Cloud 생성형 AI 사용자 가이드라인에 대한 사용자의 동의 여부에 따라 달라집니다. 이 기능을 통한 모든 출력 내용이 정확한지 검토하고 사용 사례에 적합한지 확인해 보시기 바랍니다."
>additional-url="https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html" text="Adobe 생성형 AI 사용자 가이드라인"

>[!INFO]
>
>기능을 직접 탐색하고 기능을 완전히 이해할 수 있도록 설계된 [대화형 데모](https://experienceleague.adobe.com/en/apps/journey-optimizer/ai-assistant-content-accelerator){target="_blank"}를 통해 실습 경험에 몰입하십시오.


Microsoft Azure OpenAI 및 Adobe Firefly에서 제공하는 Adobe Journey Optimizer for Content Acceleration의 AI Assistant는 텍스트 및 이미지에 대한 사전 예방적 콘텐츠 변형 제안을 제공합니다. 이메일, 푸시, SMS 채널에 사용 가능합니다. 이 새로운 기능은 프롬프트 기반의 텍스트 및 이미지 생성을 제공합니다. 이미지 생성은 Adobe Firefly로 관리됩니다.

Adobe Journey Optimizer for Content Acceleration의 AI Assistant를 사용하여 다양한 주요 제목 및 이미지를 실험하여 메시지의 효과를 최적화합니다. 여러 변형을 생성하고 비교할 실험을 빌드합니다. Journey Optimizer 컨텐츠 실험을 활용하면 여러 메시지 처리를 정의하여 어느 메시지가 타깃 대상자에게 가장 적합한지 측정할 수 있습니다. 게재 콘텐츠 또는 제목을 변경하도록 선택할 수 있습니다. 메시지 대상자는 지정된 지표 측면에서 가장 적합한 처리를 결정하기 위해 각 처리에 임의로 할당됩니다. [이 섹션](../content-management/content-experiment.md)에서 콘텐츠 실험에 대해 자세히 알아보십시오.

>[!IMPORTANT]
>
>* 이 기능의 사용을 시작하기 전에 관련 [보호 기능 및 제한 사항](#generative-guardrails)을 읽어 보십시오.
>
>
>* 콘텐츠 가속화를 위해 Adobe Journey Optimizer에서 AI 도우미를 사용하려면 먼저 [사용자 계약](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"}에 동의해야 합니다. 자세한 내용은 Adobe 직원에게 문의하십시오.

## AI Assistant Content Accelerator 액세스 {#generative-access}

Adobe Journey Optimizer for Content Acceleration 기능에 액세스하려면 사용자에게 **콘텐츠 생성** 권한이 부여되어야 합니다. [자세히 알아보기](../administration/permissions.md)

+++  콘텐츠 생성 관련 권한을 할당하는 방법을 알아봅니다

1. **권한** 제품에서 **역할** 탭으로 이동하여 원하는 **역할**&#x200B;을(를) 선택하십시오.

1. 권한을 수정하려면 **편집**&#x200B;을 클릭하십시오.

1. **AI 도우미** 리소스를 추가한 다음 드롭다운 메뉴에서 **콘텐츠 생성**&#x200B;을 선택합니다.

   ![](assets/gen-ai-role.png){zoomable="yes"}

1. 변경 내용을 적용하려면 **저장**&#x200B;을 클릭하세요.

   이 역할에 이미 할당된 모든 사용자의 권한은 자동으로 업데이트됩니다.

1. 새 사용자에게 이 역할을 할당하려면 **역할** 대시보드의 **사용자** 탭으로 이동하여 **사용자 추가**&#x200B;를 클릭하세요.

1. 사용자 이름, 전자 메일 주소를 입력하거나 목록에서 선택한 다음 **저장**&#x200B;을 클릭합니다.

1. 사용자를 이전에 만들지 않은 경우 [이 설명서](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/users)를 참조하세요.

사용자는 인스턴스에 액세스하기 위한 지침이 포함된 이메일을 받게 됩니다.

+++

## 보호 및 제한 사항 {#generative-guardrails}

Adobe Journey Optimizer for Content Acceleration에서 이메일 생성을 위해 AI Assistant를 사용하는 방법에 대한 일반 지침은 다음과 같습니다.

* 생성된 콘텐츠의 품질은 사용자가 정의한 마케팅 목표/프롬프트의 영향을 상당히 많이 받습니다. GenAI 모델에 대해 잘 정의된 프롬프트를 사용하여 정확하게 해석하십시오. 
* 브랜드 콘텐츠에 대한 정확한 정보를 얻으려면 브랜드 자산을 업로드하십시오. 그렇지 않은 경우 콘텐츠는 공개적으로 이용 가능한 정보를 기반으로 합니다. 업로드된 콘텐츠는 PDF, JPEG, PNG 또는 ZIP 파일(지원되는 파일 형식 포함) 형식일 수 있습니다.
* 업로드되는 브랜드 자산의 최대 크기는 50MB입니다. 더 큰 파일이나 많은 이미지를 사용할 수 있지만 처리 시간이 늘어납니다.
* Adobe Journey Optimizer for Content Acceleration에서 AI Assistant를 사용하여 이메일 콘텐츠를 만들려면 브랜드별 또는 맞춤형 템플릿을 사용하십시오. 최대 8~10개의 이미지가 포함된 이메일 템플릿이 권장됩니다.
* 변형을 선택할 때 엄지손가락 위로, 엄지손가락 아래로 또는 플래그 아이콘을 사용하여 문제가 있는 출력을 보고하십시오.
* AI 어시스턴트 사용 시 Adobe Experience Cloud 생성형 AI 사용자 지침이 적용됩니다. [자세히 알아보기](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html)
* 미디어 제작에서 생성 AI 도구 사용의 투명성을 증진하기 위한 Adobe의 약속의 일부로, Adobe은 Firefly 생성 에셋이 포함된 콘텐츠 또는 프로젝트를 다운로드하거나 내보낼 때 Content credentials을 적용합니다. [자세히 알아보기](https://helpx.adobe.com/firefly/using/content-credentials.html)

Adobe Journey Optimizer for Content Acceleration의 AI Assistant에는 다음 제한 사항이 적용됩니다.

* 지원되는 언어는 영어입니다. 영어가 아닌 입력은 일관되지 않거나 잘못된 결과를 생성할 수 있습니다. 비영어 응답에서 발생하는 문제는 현재 해결되거나 개선되지 않을 것입니다.
* 이메일, 푸시, 웹 및 SMS 채널에만 사용할 수 있습니다.
* GenAI 콘텐츠가 항상 정확하지는 않을 수 있습니다. 엔지니어가 모델을 개선할 수 있도록 피드백을 공유해 주십시오.
* 여러 브랜드 자산을 업로드할 수 있지만 특정 세대에 대해서는 하나의 활용할 수 있습니다.


## AI Assistant 콘텐츠 생성 기능 {#generative-features}


<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="generative-email.md">
<img alt="이메일 생성" src="assets/do-not-localize/text-genai.jpeg">
</a>
<div>
<a href="generative-email.md"><strong>이메일 생성</strong></a>
</div>
<p>
</td>
<td>
<a href="generative-sms.md">
<img alt="SMS 생성" src="assets/do-not-localize/image-genai.jpeg">
</a>
<div><a href="generative-sms.md"><strong>SMS 생성</strong>
</div>
<p>
</td>
<td>
<a href="generative-push.md">
<img alt="CSR 생성" src="assets/do-not-localize/email-genai.jpeg">
</a>
<div>
<a href="generative-push.md"><strong>푸시 알림 </strong></a>
</div>
<p></td>
<td>
<a href="generative-web.md">
<img alt="웹 생성" src="assets/do-not-localize/web-genai.jpeg">
</a>
<div><a href="generative-web.md"><strong>웹 페이지 생성</strong>
</div>
<p>
</td>
</tr></table>
