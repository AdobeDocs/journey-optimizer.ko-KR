---
solution: Journey Optimizer
product: journey optimizer
title: 인텔리전트 서비스와 통합
description: Journey Optimizer에서 Adobe Intelligent Services 및 Customer AI 예측을 활용하는 방법에 대해 알아봅니다
feature: Journeys, Integrations
topic: Artificial Intelligence
role: User
level: Intermediate
keywords: 인공, AI, 지능형, 여정, 서비스
exl-id: 20da09e1-0611-4d27-a589-30552011e06c
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/rTKcWHwfwleQtD68fcdeqYK2AMQHVaknKtsNDFsOldI
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 669
ht-degree: 0%

---

# 인텔리전트 서비스와 통합 {#ai-overview}

>[!BEGINSHADEBOX]

**이 페이지에서:** Adobe Intelligent Services 및 Customer AI 예측을 Journey Optimizer과 통합하여 결정, 작업 및 세그먼트 작성을 위한 프로필 특성으로 이탈 및 전환 점수를 사용하는 방법에 대해 알아봅니다.

>[!ENDSHADEBOX]

**[!DNL Adobe Intelligent Services]**&#x200B;과의 통합을 통해 고객 경험 사용 사례에 인공 지능과 머신 러닝을 활용할 수 있습니다. 이를 통해 마케팅 분석가는 데이터 과학 전문 지식 없이도 비즈니스 수준의 구성을 사용하여 기업의 요구 사항에 맞게 예측을 설정할 수 있습니다.

[!DNL Adobe Experience Platform]에 빌드된 [!DNL Intelligent Services]은(는) 고객 경험 팀에 AI-as-a-service를 제공합니다. 이는 고객 행동을 예측하고, 캠페인 영향을 측정하고, 투자 수익을 개선하는 데 도움이 됩니다. 자세한 내용은 [[!DNL Adobe Experience Platform] 설명서](https://experienceleague.adobe.com/docs/experience-platform/intelligent-services/home.html){target="_blank"}를 참조하세요.

[!DNL Journey Optimizer]과(와) [!DNL Intelligent Services] 간의 통합을 통해 고객 예측을 활용할 수 있습니다.

[!DNL Adobe Intelligent Services]의 구성 요소인 Customer AI는 고객의 행동을 예측합니다. [[!DNL Adobe Experience Platform] 설명서](https://experienceleague.adobe.com/docs/experience-platform/intelligent-services/customer-ai/overview.html){target="_blank"}를 참조하세요.

고객 AI를 통해 브랜드는 이탈 또는 전환 머신 러닝 기반 점수를 만들 수 있습니다. 이러한 점수는 [!DNL Adobe Experience Platform]개 프로필(실시간 고객 프로필)에서 프로필 특성으로 사용할 수 있습니다.

따라서 이러한 속성은 Journey Optimizer의 다른 프로필 속성과 마찬가지로 사용할 수 있습니다. 의사 결정, 작업 또는 세그먼트 작성 조건에 사용할 수 있습니다.

![성향 점수 및 예측을 표시하는 고객 AI 통합](assets/customer-ai.png)

+++ AI 기술 자료 참조

이 단원에는 이 주제와 관련된 해석, 검색 및 질문 답변을 지원하기 위한 구조화된 지식이 포함되어 있습니다.

이해를 돕기 위해 이 정보를 이 페이지의 설명서와 통합해야 합니다. 두 소스 모두 독립적으로 사용하기 위한 것은 아닙니다. 이 페이지에서는 기능에 대해 설명하지만, 용어, 의도, 적용 가능성 및 제약 조건을 명확히 하는 데 도움이 되는 추가 컨텍스트를 제공합니다.

- **TL;DR:** 이 페이지에서는 Journey Optimizer을 Adobe Intelligent Services(특히 고객 AI)와 통합하여 머신 러닝 기반 성향 점수를 여정의 프로필 속성으로 활용하는 방법을 설명합니다.

**의도:**
- Adobe Intelligent Services를 Journey Optimizer과 통합하는 방법 이해
- 여정 조건 또는 작업에서 고객 AI 성향 점수를 프로필 속성으로 사용
- 데이터 과학 전문 지식 없이도 이탈 또는 전환을 위한 AI 기반 예측 활성화
- Journey Optimizer 내의 세그먼트 빌드에 머신 러닝 점수 적용

**용어집:**
- **Adobe Intelligent Services**: 데이터 과학 전문 지식 *(제품별)* 없이도 고객 경험 예측을 가능하게 하는 Adobe Experience Platform에 구축된 AI/ML 서비스 세트입니다.
- **고객 AI**: 고객 프로필 *(제품별)에 대한 머신 러닝 기반 이탈 또는 전환 성향 점수를 생성하는 Adobe Intelligent Services의 구성 요소*
- **성향 점수**: 고객이 프로필 특성 *(제품별)로 저장된 특정 작업(예: 이탈 또는 전환)을 수행할 가능성을 나타내는 기계 학습 기반 점수*

**보호 기능:**
- 데이터 과학 전문 지식이 필요하지 않지만 마케팅 분석가가 비즈니스 수준 구성을 완료해야 합니다
- Customer AI 점수를 Adobe Experience Platform에서 프로필 속성으로 사용하려면 먼저 Journey Optimizer에서 구성해야 합니다

**용어:**
- 정식 이름: Adobe Intelligent Services — 약어: none — 변형: Intelligent Services, AI 서비스
- 정식 이름: Customer AI — 약어: none — 변형: Customer AI 점수, 성향 점수
- 동의어: &quot;이탈 점수&quot; = &quot;이탈 성향&quot; ; &quot;전환 점수&quot; = &quot;전환 성향&quot;
- 혼동하지 마십시오: &quot;Adobe Intelligent Services&quot; ≠ &quot;AI Assistant&quot;(Intelligent Services는 예측 ML 플랫폼이며 AI Assistant는 대화 인터페이스임)

**FAQ:**
- **Q: Journey Optimizer의 컨텍스트에서 고객 AI란 무엇입니까?** — Customer AI는 머신 러닝 기반 이탈 또는 전환 점수를 생성하는 Adobe Intelligent Services 구성 요소로, Journey Optimizer 조건, 작업 및 세그먼트 작성에서 사용할 수 있는 프로필 속성으로 사용할 수 있습니다.
- **Q: Adobe Intelligent Services를 사용하려면 데이터 과학 기술이 필요합니까?** — 아니요. 마케팅 분석가는 데이터 과학에 대한 전문 지식 없이도 비즈니스 수준의 설정을 사용하여 예측을 구성할 수 있습니다.
- **Q: 고객 AI 점수는 어디에 저장되어 있습니까?** — Adobe Experience Platform의 실시간 고객 프로필에 프로필 속성으로 저장되므로 Journey Optimizer의 다른 프로필 속성처럼 액세스할 수 있습니다.
- **Q: 여정에서 Customer AI 점수를 사용하려면 어떻게 해야 합니까?** — 프로필 속성으로 사용할 수 있게 되면 의사 결정, 작업 구성 또는 대상 세그먼트 작성 조건에 점수를 사용할 수 있습니다.

+++
