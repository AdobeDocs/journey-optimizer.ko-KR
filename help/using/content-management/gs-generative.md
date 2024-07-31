---
solution: Journey Optimizer
product: journey optimizer
title: AI 어시스턴트 시작하기
description: Journey Optimizer의 AI 어시스턴트에 액세스하고 작업하는 방법 알아보기
feature: Content Assistant
topic: Content Management
role: User
level: Beginner
badge: label="Beta" type="Informative"
hide: true
hidefromtoc: true
exl-id: 6e291ce3-f324-4e5d-975b-5229dea4d581
source-git-commit: 930070843c2c1ce022beb5dc6e8a61c8d4f70365
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 91%

---

# AI 어시스턴트 시작하기 {#gs-content-assistant}

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_settings"
>title="AI 어시스턴트"
>abstract="게재를 만들고 개인화한 다음에는 AI 어시스턴트를 사용하여 콘텐츠를 개선할 수 있습니다. 이 기능을 사용하면 생성하려는 내용을 설명하여 콘텐츠를 더욱 세부적으로 조정할 수 있어 개인화 및 콘텐츠 개선 프로세스가 간소화됩니다."


>[!CONTEXTUALHELP]
>id="ajo_ai_generation_context"
>title="브랜드 자산 업로드"
>abstract="브랜드 자산 업로드 메뉴를 사용하면 AI Assistant에 추가 컨텍스트를 제공할 수 있는 콘텐츠가 포함된 브랜드 자산을 추가하거나 이전에 업로드한 자산을 선택할 수 있습니다. 이 옵션을 사용하면 AI Assistant가 필요한 모든 자료에 액세스하여 기능과 연관성을 향상시킬 수 있습니다."


>[!CONTEXTUALHELP]
>id="ajo_ai_generation_start"
>title="Adobe 생성형 AI 약관"
>abstract="이 기능에 대한 액세스 가능 여부는 Adobe Experience Cloud 생성형 AI 사용자 가이드라인에 대한 사용자의 동의 여부에 따라 달라집니다. 이 기능을 통한 모든 출력 내용이 정확한지 검토하고 사용 사례에 적합한지 확인해 보시기 바랍니다."
>additional-url="https://www.adobe.com/kr/legal/licenses-terms/adobe-gen-ai-user-guidelines.html" text="Adobe 생성형 AI 사용자 가이드라인"

>[!BEGINSHADEBOX]

**목차**

* AI 어시스턴트 시작하기
* [AI 어시스턴트를 통한 이메일 생성](generative-email.md)
* [AI 어시스턴트를 통한 SMS 생성](generative-sms.md)
* [AI 어시스턴트와 함께하는 푸시 세대](generative-push.md)
* [AI 어시스턴트로 콘텐츠 실험](generative-experimentation.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Adobe Journey Optimizer의 AI 어시스턴트는 현재 일부 사용자에게만 Beta 버전으로 제공됩니다.

Adobe Journey Optimizer의 Azure OpenAI 기반 AI 어시스턴트는 텍스트 및 이미지에 대해 적극적으로 콘텐츠 변형을 제안합니다. 이메일, 푸시, SMS 채널에 사용 가능합니다. 이 새로운 기능은 프롬프트 기반의 텍스트 및 이미지 생성을 제공합니다. 이미지 생성은 Adobe Firefly로 관리됩니다.

AI 어시스턴트를 사용하여 다양한 중심 제목과 이미지를 실험해 보며 메시지의 영향을 최적화할 수 있습니다. 여러 변형을 생성하고 비교할 실험을 빌드합니다. Journey Optimizer 컨텐츠 실험을 활용하면 여러 메시지 처리를 정의하여 어느 메시지가 타깃 대상자에게 가장 적합한지 측정할 수 있습니다. 게재 콘텐츠 또는 제목을 변경하도록 선택할 수 있습니다. 메시지 대상자는 지정된 지표 측면에서 가장 적합한 처리를 결정하기 위해 각 처리에 임의로 할당됩니다. [이 섹션](../content-management/content-experiment.md)에서 콘텐츠 실험에 대해 자세히 알아보십시오.

## 보호 및 제한 사항 {#generative-guardrails}

이메일 생성을 위해 Journey Optimizer에서 AI 어시스턴트를 사용하기 위한 일반 지침은 다음과 같습니다.

* 생성된 콘텐츠의 품질은 사용자가 정의한 마케팅 목표/프롬프트의 영향을 상당히 많이 받습니다. GenAI 모델에 대해 잘 정의된 프롬프트를 사용하여 정확하게 해석하십시오. 
* 브랜드 콘텐츠에 대한 정확한 정보를 얻으려면 브랜드 자산을 업로드하십시오. 그렇지 않은 경우 콘텐츠는 공개적으로 이용 가능한 정보를 기반으로 합니다. 업로드된 콘텐츠는 PDF, JPEG, PNG 또는 ZIP 파일(지원되는 파일 형식 포함) 형식일 수 있습니다.
* 업로드되는 브랜드 자산의 최대 크기는 50MB입니다. 더 큰 파일이나 많은 이미지를 사용할 수 있지만 처리 시간이 늘어납니다.
* Adobe Campaign으로 작성된 이메일 템플릿을 사용하는 것이 좋습니다. [기본 제공 이메일 템플릿](../email/use-email-templates.md), 브랜드별 템플릿 또는 사용자 정의 템플릿을 사용하여 이메일 콘텐츠를 생성하세요. 최대 8~10개의 이미지가 포함된 이메일 템플릿을 권장합니다.
* 변형을 선택할 때 엄지손가락 위로, 엄지손가락 아래로 또는 플래그 아이콘을 사용하여 문제가 있는 출력을 보고하십시오.
* AI 어시스턴트 사용 시 Adobe Experience Cloud 생성형 AI 사용자 지침이 적용됩니다. [자세히 알아보기](https://www.adobe.com/kr/legal/licenses-terms/adobe-gen-ai-user-guidelines.html)

Journey Optimizer의 AI 어시스턴트에는 다음 제한 사항이 적용됩니다.

* 영어로만 지원됩니다.
* 이메일, 푸시 및 SMS 채널에서만 사용할 수 있습니다.
* GenAI 콘텐츠가 항상 정확하지는 않을 수 있습니다. 엔지니어가 모델을 개선할 수 있도록 피드백을 공유해 주십시오.
* 여러 브랜드 자산을 업로드할 수 있지만 특정 세대에 대해서는 하나의 활용할 수 있습니다.

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
</tr></table>
