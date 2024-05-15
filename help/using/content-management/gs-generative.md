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
source-git-commit: 644e0959ee0d0ec8ee0c4ec54c3bcd1cc3c4dda9
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 54%

---

# AI 어시스턴트 시작하기 {#gs-content-assistant}

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_settings"
>title="AI 어시스턴트"
>abstract="게재 내용을 작성하고 개인화한 후 AI 어시스턴트를 사용하여 콘텐츠를 개선할 수 있습니다. 이 기능은 생성하려는 내용을 설명하여 콘텐츠를 미세 조정할 수 있도록 함으로써 개인화 및 콘텐츠 개선 프로세스를 간소화합니다."


>[!CONTEXTUALHELP]
>id="ajo_ai_generation_context"
>title="AI Assistant를 사용하여 컨텍스트 정의"
>abstract="선택한 컨텐츠를 컨텐츠 생성에 대한 입력으로 사용하려면 **원본 컨텐츠 사용** 토글. 또한 브랜드 자산을 업로드하여 소스로 사용할 수도 있습니다. 선택한 콘텐츠를 사용하지 않는 경우 브랜드 자산 업로드와 브랜드 자산 선택이 필수입니다."


>[!CONTEXTUALHELP]
>id="ajo_ai_generation_start"
>title="Adobe 생성형 AI 약관"
>abstract="이 기능의 이용에는 Adobe Experience Cloud 생성형 AI 사용자 가이드라인에 대한 계약이 적용됩니다. 이 기능에 제공하는 모든 프롬프트, 컨텍스트, 추가 정보 또는 기타 입력 내용은 특정 컨텍스트와 연결되어야 하며, 여기에는 브랜딩 자료, 웹 사이트 콘텐츠, 데이터, 해당 데이터에 대한 스키마, 템플릿 또는 기타 신뢰할 수 있는 문서가 포함될 수 있으나 개인 정보는 포함되지 않아야 합니다(개인 정보에는 특정 개인 사용자와 다시 연결될 수 있는 모든 항목이 포함됨). 이 기능을 통한 모든 출력 내용이 정확한지 검토하고 사용 사례에 적합한지 확인해 보시기 바랍니다."
>additional-url="https://www.adobe.com/kr/legal/licenses-terms/adobe-gen-ai-user-guidelines.html" text="Adobe 생성형 AI 사용자 가이드라인"

>[!BEGINSHADEBOX]

**목차**

* AI 어시스턴트 시작하기
* [AI 어시스턴트로 이메일 생성](generative-email.md)
* [AI 어시스턴트와 함께하는 SMS 세대](generative-sms.md)
* [AI Assistant를 사용하여 푸시 생성](generative-push.md)
* [AI Assistant를 사용한 콘텐츠 실험](generative-experimentation.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Adobe Journey Optimizer의 AI Assistant는 현재 사용자를 선택하는 베타 버전으로 사용할 수 있습니다.

Adobe Journey Optimizer의 AI 어시스턴트는 텍스트 및 이미지에 대한 사전 예방적 콘텐츠 변형 제안을 제공합니다. 이메일, 푸시 및 SMS 채널에 사용 가능합니다. 이 새로운 기능은 프롬프트 기반의 텍스트 및 이미지 생성을 제공합니다. 이미지 생성은 Adobe Firefly로 관리됩니다.

AI 어시스턴트를 사용하여 다양한 중심 제목과 이미지를 실험해 보며 메시지의 영향을 최적화할 수 있습니다. 여러 변형을 생성하고 비교할 실험을 빌드합니다. Journey Optimizer 컨텐츠 실험을 활용하면 여러 메시지 처리를 정의하여 어느 메시지가 타깃 대상자에게 가장 적합한지 측정할 수 있습니다. 게재 콘텐츠 또는 제목을 변경하도록 선택할 수 있습니다. 메시지 대상자는 지정된 지표 측면에서 가장 적합한 처리를 결정하기 위해 각 처리에 임의로 할당됩니다. [이 섹션](../campaigns/content-experiment.md)에서 콘텐츠 실험에 대해 자세히 알아보십시오.

## 보호 및 제한 사항 {#generative-guardrails}

이메일 생성을 위해 Journey Optimizer에서 AI Assistant를 사용하는 방법에 대한 일반 지침은 다음과 같습니다.

* 생성된 콘텐츠의 품질은 사용자가 정의하는 마케팅 목표/프롬프트의 영향을 많이 받습니다. GenAI 모델이 정확하게 해석할 수 있도록 잘 정의된 프롬프트를 사용하십시오. 
* 브랜드 에셋을 업로드하여 브랜드 콘텐츠에 정확하게 맞춥니다. 그 외의 경우 콘텐츠는 공개적으로 사용 가능한 정보를 기반으로 합니다. 업로드된 콘텐츠는 PDF, JPEG, PNG 또는 ZIP 파일(지원되는 파일 형식 포함) 형식일 수 있습니다.
* 업로드된 브랜드 자산의 최대 크기는 50MB입니다. 파일이 크거나 이미지가 많으면 작동할 수 있지만 처리 시간은 늘어납니다.
* Adobe Campaign 작성 이메일 템플릿 사용(권장) [기본 제공 전자 메일 템플릿](../email/use-email-templates.md)이메일 콘텐츠를 만들기 위한 브랜드별 템플릿 또는 맞춤형 템플릿입니다. 이메일 템플릿에는 최대 8~10개의 이미지가 권장됩니다.
* 변형을 선택할 때 썸네일 업, 썸네일 다운 또는 플래그 아이콘을 사용하여 문제가 있는 출력을 보고해야 합니다.
* AI 비서 사용은 Adobe Experience Cloud 생성 AI 사용자 지침의 적용을 받습니다. [자세히 알아보기](https://www.adobe.com/kr/legal/licenses-terms/adobe-gen-ai-user-guidelines.html)

Journey Optimizer의 AI Assistant에는 다음과 같은 제한이 적용됩니다.

* 지원되는 언어는 영어입니다.
* 이메일, 푸시 및 SMS 채널에만 사용할 수 있습니다.
* GenAI 콘텐츠가 항상 정확하지는 않을 수 있습니다. 엔지니어가 모델을 세분화할 수 있도록 피드백을 공유하십시오.
* 여러 브랜드 자산을 업로드할 수 있지만 특정 세대에 대해 하나만 활용할 수 있습니다.

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
<img alt="푸시 생성" src="assets/do-not-localize/email-genai.jpeg">
</a>
<div>
<a href="generative-push.md"><strong>푸시 알림 생성</strong></a>
</div>
<p></td>
</tr></table>
