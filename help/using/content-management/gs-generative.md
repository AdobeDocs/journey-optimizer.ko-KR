---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer에서 AI Assistant 시작
description: Journey Optimizer에서 AI Assistant에 액세스하고 작업하는 방법을 알아봅니다
feature: Content Assistant
topic: Content Management, Artificial Intelligence
role: User
level: Beginner
mini-toc-levels: 1
exl-id: 6e291ce3-f324-4e5d-975b-5229dea4d581
TQID: https://experienceleague.adobe.com/lACM3Joa-M9aAfD0YOX4jOndjrcoiLMDAEBdFxgjt8o
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 999
ht-degree: 0%

---

# AI Assistant 시작 {#gs-content-assistant}

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_settings"
>title="Journey Optimizer의 AI 지원"
>abstract="게재를 제작하고 개인화하면 Journey Optimizer의 AI Assistant를 사용하여 콘텐츠를 개선할 수 있습니다. 이 기능은 생성하려는 내용을 설명하여 콘텐츠를 미세 조정할 수 있도록 함으로써 개인화 및 콘텐츠 개선 프로세스를 간소화합니다."

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_context"
>title="브랜드 자산 업로드"
>abstract="브랜드 에셋 업로드 메뉴를 사용하면 Journey Optimizer의 AI Assistant에 추가 컨텍스트를 제공할 수 있는 콘텐츠가 포함된 모든 브랜드 에셋을 추가하거나 이전에 업로드한 에셋을 선택할 수 있습니다. 이 옵션을 사용하면 AI Assistant가 필요한 모든 자료에 액세스하여 기능과 연관성을 높일 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_start"
>title="Adobe Generative AI 용어"
>abstract="이 기능에 대한 액세스는 Adobe Experience Cloud 생성 AI 사용자 지침에 대한 귀하의 동의에 따라 달라집니다. 이 기능의 출력을 정확하게 검토하고 사용 사례에 적합한지 확인하십시오."
>additional-url="https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html" text="Adobe Generative AI 사용 지침"

>[!INFO]
>
>기능을 직접 탐색하고 기능을 완전히 이해할 수 있도록 설계된 [라이브 기능 미리 보기](https://experienceleague.adobe.com/ko/apps/journey-optimizer/ai-assistant-content-accelerator){target="_blank"}를 통해 실습 경험에 몰입하세요.


Microsoft Azure OpenAI 및 Adobe Firefly에서 제공하는 Adobe Journey Optimizer의 AI 도우미는 텍스트 및 이미지에 대한 사전 예방적 콘텐츠 변형 제안을 제공합니다. 이 새 기능은 **프롬프트 기반 텍스트 및 이미지 생성**&#x200B;을 제공합니다. 이미지 생성은 Adobe Firefly을 통해 관리됩니다.

AI Assistant는 여러 언어로 **세대를 지원합니다**. 이를 통해 다양한 글로벌 대상자에게 도달하여 참여할 수 있습니다. AI Assistant는 다음 언어로 제공됩니다.

<table style="table-layout:fixed; margin-top: 0px; margin-bottom: 0px;">
  <tbody>
    <tr style="border: 0;background-color: #FFFFFF;">
      <td>
        <ul>
          <li>중국어(홍콩)</li>
          <li>중국어(간체)</li>
          <li>중국어(대만)</li>
          <li>네덜란드어</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>프랑스어</li>
          <li>독일어</li>
          <li>이탈리아어</li>
          <li>일본어</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>노르웨이어</li>
          <li>포르투갈어</li>
          <li>스페인어</li>
          <li>스웨덴어</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

Adobe Journey Optimizer의 AI Assistant를 사용하여 다양한 주요 제목 및 이미지를 실험하여 메시지의 효과를 최적화할 수 있습니다. 여러 변형을 생성하고 비교할 실험을 빌드합니다. **Journey Optimizer 콘텐츠 실험**&#x200B;을 활용하여 대상 대상에 가장 적합한 성과를 측정하기 위해 여러 메시지 처리를 정의할 수 있습니다. 게재 콘텐츠 또는 주제를 변경하도록 선택할 수 있습니다. 메시지 대상자는 지정된 지표 측면에서 가장 적합한 처리를 결정하기 위해 각 처리에 임의로 할당됩니다. [이 섹션](../content-management/content-experiment.md)에서 콘텐츠 실험에 대해 자세히 알아보세요.

>[!IMPORTANT]
>
>* 이 기능을 사용하기 전에 관련 [보호 기능 및 제한 사항](#generative-guardrails)을 읽어 보십시오.
>
>
>* Adobe Journey Optimizer에서 AI Assistant를 사용하려면 [사용자 계약](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"}에 동의해야 합니다. 자세한 내용은 Adobe 담당자에게 문의하십시오.

## AI Assistant 액세스 {#generative-access}

Adobe Journey Optimizer의 AI Assistant 기능에 액세스하려면 사용자에게 **콘텐츠 생성** 권한이 부여되어야 합니다. [자세히 알아보기](../administration/permissions.md)

+++  콘텐츠 생성 관련 권한을 할당하는 방법을 알아봅니다

1. **권한** 제품에서 **역할** 탭으로 이동하여 원하는 **역할**&#x200B;을(를) 선택하십시오.

1. 권한을 수정하려면 **편집**&#x200B;을 클릭하십시오.

1. **AI Assistant** 리소스를 추가한 다음 드롭다운 메뉴에서 **콘텐츠 생성**&#x200B;을 선택합니다.

   ![](assets/gen-ai-role.png){zoomable="yes"}

1. 변경 내용을 적용하려면 **저장**&#x200B;을 클릭하세요.

   이 역할에 이미 할당된 모든 사용자의 권한은 자동으로 업데이트됩니다.

1. 새 사용자에게 이 역할을 할당하려면 **역할** 대시보드의 **사용자** 탭으로 이동하여 **사용자 추가**&#x200B;를 클릭하세요.

1. 사용자 이름, 전자 메일 주소를 입력하거나 목록에서 선택한 다음 **저장**&#x200B;을 클릭합니다.

1. 사용자를 이전에 만들지 않은 경우 [이 설명서](https://experienceleague.adobe.com/ko/docs/experience-platform/access-control/abac/permissions-ui/users)를 참조하세요.

사용자는 인스턴스에 액세스하기 위한 지침이 포함된 이메일을 받게 됩니다.

+++

## 보호 기능 및 제한 사항 {#generative-guardrails}

이메일 생성을 위해 Adobe Journey Optimizer에서 AI Assistant를 사용하는 방법에 대한 일반 지침은 다음과 같습니다.

### 지원되는 채널

* 이메일, 푸시, 웹 및 SMS 채널에만 사용할 수 있습니다.

### 컨텐츠 품질, 프롬프트 및 피드백

* 생성된 콘텐츠의 품질은 사용자가 정의하는 마케팅 목표/프롬프트의 영향을 많이 받습니다. GenAI 모델이 정확하게 해석할 수 있도록 잘 정의된 프롬프트를 사용하십시오. 
* GenAI 콘텐츠가 항상 정확하지는 않을 수 있습니다. 엔지니어가 모델을 세분화할 수 있도록 피드백을 공유하십시오.
* 변형을 선택할 때 썸네일 업, 썸네일 다운 또는 플래그 아이콘을 사용하여 문제가 있는 출력을 보고해야 합니다.

### 브랜드 자산

* 브랜드 에셋을 업로드하여 브랜드 콘텐츠에 정확하게 맞춥니다. 그 외의 경우 콘텐츠는 공개적으로 사용 가능한 정보를 기반으로 합니다. 업로드된 콘텐츠는 PDF, JPEG, PNG 또는 ZIP 파일(지원되는 파일 형식 포함) 형식일 수 있습니다.
* 업로드된 브랜드 자산의 최대 크기는 50MB입니다. 파일이 크거나 이미지가 많으면 작동할 수 있지만 처리 시간은 늘어납니다.
* 여러 브랜드 자산을 업로드할 수 있지만 특정 세대에 대해 하나만 활용할 수 있습니다.

### 이메일 템플릿 및 이미지

* 브랜드별 또는 맞춤형 템플릿을 사용하여 Adobe Journey Optimizer에서 AI Assistant를 사용하여 이메일 콘텐츠를 생성합니다. 최대 8~10개의 이미지가 포함된 이메일 템플릿이 권장됩니다.

### 법적 사용 및 투명성

* AI Assistant 사용 시 Adobe Experience Cloud 생성 AI 사용자 지침이 적용됩니다. [자세히 알아보기](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html)
* 미디어 제작에서 생성 AI 도구 사용의 투명성을 증진하기 위한 Adobe의 약속의 일환으로 Adobe은 Firefly 생성 에셋이 포함된 콘텐츠 또는 프로젝트를 다운로드하거나 내보낼 때 Content Credentials을 적용합니다. [자세히 알아보기](https://helpx.adobe.com/kr/firefly/using/content-credentials.html)

### 개인화 표현식을 위한 AI 지원 {#ai-assistant-personalization-editor-guardrails}

다음 가드레일은 [!UICONTROL Personalization 편집기] 및 이메일 Designer의 [개인화 표현식에 대한 AI Assistant](generative-personalization-expressions.md)에 적용됩니다.

* **Offer 및 Experience Decisioning** — 지원되지 않습니다.
* **즐겨찾기** — 지원되지 않습니다.
* **저장된 조건** — 지원되지 않습니다.
* **Adobe Experience Manager 콘텐츠 조각** — 지원되지 않습니다.

## AI Assistant 콘텐츠 생성 기능 {#generative-features}

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="generative-full-content.md">
<img alt="전체 콘텐츠 생성" src="assets/do-not-localize/email-genai.jpeg">
</a>
<div>
<a href="generative-full-content.md"><strong>전체 콘텐츠 생성</strong></a>
</div>
<p>
</td>
<td>
<a href="generative-text.md">
<img alt="텍스트 생성" src="assets/do-not-localize/text-genai.jpeg">
</a>
<div><a href="generative-text.md"><strong>텍스트 생성</strong>
</div>
<p>
</td>
<td>
<a href="generative-image.md">
<img alt="이미지 생성" src="assets/do-not-localize/image-genai.jpeg">
</a>
<div>
<a href="generative-image.md"><strong>이미지 생성</strong></a>
</div>
<p></td>
</tr></table>

## 추가 리소스

* **[생성 실험](generative-experimentation.md)** - AI 생성 콘텐츠를 실험과 결합하는 방법을 이해합니다.
* **[AI Assistant 사용 사례](generative-uc.md)** - 사용 사례를 통해 AI Assistant 사용 방법 알아보기
* **[AI Assistant 튜토리얼](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/tutorials/introduction-to-journey-optimizer/ai-assistant){target="_blank"}** - AI Assistant 기능 및 모범 사례에 대한 단계별 비디오 튜토리얼을 살펴보십시오.
