---
solution: Journey Optimizer
product: journey optimizer
title: 콘텐츠 변형 자동 생성(Beta)
description: AI 기반 시뮬레이션을 사용하여 콘텐츠 변형을 자동으로 생성하는 방법을 알아봅니다.
feature: Email, Email Rendering, Personalization, Preview, Proofs
topic: Content Management
role: User
level: Intermediate
badge: label="비공개 베타" type="Informative"
hidefromtoc: true
hide: true
exl-id: 9b7fbd43-3d90-458b-8a2f-0bf0ac5437c3
source-git-commit: 45ebae048a748429a1918326526f3756a3e93c4c
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 2%

---

# 콘텐츠 변형 자동 생성(Beta){#auto-generate-variants}

>[!AVAILABILITY]
>
>이 기능은 현재 **개인 베타**&#x200B;에 있으며 사용자의 환경에서는 사용할 수 없습니다. 액세스 권한을 얻으려면 Adobe 담당자에게 문의하십시오.

[!DNL Journey Optimizer]에서는 콘텐츠를 테스트하기 위해 여러 변형을 자동으로 생성할 수 있는 AI 기반 시뮬레이션을 소개합니다. 이 기능을 사용하면 변형을 수동으로 만들 필요가 줄어들어 복잡한 템플릿 간의 개인화 논리를 더 쉽게 확인할 수 있습니다.

시뮬레이션 또는 교정을 위해 콘텐츠를 렌더링할 때 시스템은 콘텐츠를 분석하고 모든 개인화 토큰 및 분기 규칙을 식별합니다. 이는 개인화 토큰을 최종 콘텐츠의 거의-사실적인 미리보기를 제공하는 의미 있는 값으로 대체합니다.

**투자자 유형**, **연령 그룹**, **결혼 상태**, **세금 ID 확인** 및 **위치**&#x200B;를 기반으로 하는 분기 논리를 사용하는 금융 서비스 전자 메일 템플릿을 고려하십시오. 변형을 생성하지 않으면 수십 개의 변형을 수동으로 만들어 모든 경로의 유효성을 확인해야 합니다. 자동 생성된 변형을 사용하면 시스템에서 이러한 조건을 자동으로 다루는 대표 변형을 생성합니다.  생성된 각 변형은 미리 보기 창에서 렌더링되어 적용된 블록 및 조건을 정확하게 보여 줍니다.

## 콘텐츠 변형 생성

콘텐츠의 변형을 생성하고 미리 보려면 다음 단계를 수행하십시오.

1. 콘텐츠를 열고 **[!UICONTROL 콘텐츠 시뮬레이션]** / **[!UICONTROL 콘텐츠 변형 시뮬레이션]**&#x200B;을 선택합니다.

   ![](assets/simulate-sample.png)

2. **[!UICONTROL 생성]** 단추를 클릭합니다.

   ![](assets/simulate-generate-variant.png)

3. [!DNL Journey Optimizer]은(는) 검색된 특성을 기반으로 변형을 자동으로 생성합니다.

4. 왼쪽 창에서 생성된 변형 목록을 검토하고 변형을 선택하여 미리 보기 창에서 개인화된 렌더링을 확인합니다.

>[!NOTE]
>
>이 기능은 표준 콘텐츠 변형 시뮬레이트 기능과 동일한 방식으로 작동합니다. 콘텐츠 변형 시뮬레이션, 관련 보호 기능 및 제한 사항에 대한 자세한 내용은 [콘텐츠 변형 시뮬레이션](../test-approve/simulate-sample-input.md) 섹션을 참조하십시오.
