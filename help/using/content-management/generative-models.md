---
solution: Journey Optimizer
product: journey optimizer
title: 브랜드 관리
description: 생성 모델을 만들고 관리하는 방법에 대해 알아봅니다
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 9ef6b02c-0a17-4b46-bcd3-8e922eef059a
source-git-commit: d2110b995bc26df861825cdd49ca2fd39f904442
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 0%

---

# 생성 모델 생성 및 관리 {#generative-models}

내장된 모델, 맞춤형 Firefly 모델 및 서드파티 이미지 생성 공급자를 통해 AI 이미지 생성 기능을 확장하여 특정 요구 사항을 충족하고 브랜드 정렬을 개선합니다.

요구 사항에 맞는 모델을 선택하십시오.

- Firefly Image Model 4에서 제공하는 **[!UICONTROL Adobe 모델]**&#x200B;은(는) 즉시 제공되며 추가 설정 없이 즉각적인 이미지 생성에 사용할 수 있습니다.
- Gemini 2.5 Flash에서 제공하는 **[!UICONTROL 파트너 모델]**&#x200B;은(는) 특정 사용 사례에 특화된 기능을 제공합니다. AI Assistant의 이미지에 대해 **텍스트 오버레이**&#x200B;와 함께 **Gemini**&#x200B;를 사용하는 단계별 워크플로에 대해서는 [텍스트 오버레이 이미지에 대한 생성 모델로 Gemini 사용](generative-uc.md#generative-gemini)을 참조하십시오.
- **[!UICONTROL 사용자 지정 모델]**&#x200B;은(는) 자신의 자산에 대해 교육되고 조직에서 추가한 브랜드별 모델입니다.

  **[!UICONTROL Adobe Firefly 설명서]**&#x200B;의 [사용자 지정 모델](https://helpx.adobe.com/kr/firefly/web/work-with-enterprise-features/train-custom-models/custom-models-overview.html)에 대해 자세히 알아보기

구성하고 나면 콘텐츠에서 이미지를 만들 때 생성 모델을 선택할 수 있습니다. [이미지 생성에 대해 자세히 알아보세요](generative-image.md).

## 생성 모델 관리

중앙 위치에서 생성 모델을 관리합니다. 사용 가능한 모든 모델을 보고, 특정 모델을 찾기 위해 필터링 및 검색하고, 브랜드에 대한 설정을 구성합니다.

1. **[!UICONTROL 브랜드]** 메뉴에서 **[!UICONTROL 생성 모델]** 탭을 선택합니다.

   ![](assets/gen-model-manage-1.png){zoomable="yes"}

1. ![](assets/do-not-localize/Smock_Filter_18_N.svg) 아이콘을 클릭하여 필터 메뉴에 액세스합니다. **[!UICONTROL 유형]** 또는 **[!UICONTROL 상태]**&#x200B;별로 모델을 필터링합니다.

   ![](assets/gen-model-manage-2.png){zoomable="yes"}

1. 검색 막대를 사용하여 이름별로 특정 생성 모델을 찾습니다.

1. 모델을 활성화 또는 비활성화하거나 삭제할 수 있는 고급 메뉴에 액세스하려면 ![](assets/do-not-localize/Smock_More_18_N.svg) 아이콘을 클릭하십시오.

   **[!UICONTROL 사용자 지정 모델]**&#x200B;만 삭제할 수 있습니다.

   ![](assets/gen-model-manage-6.png){zoomable="yes"}

1. 새 생성 모델을 처음부터 만들려면 **[!UICONTROL 모델 추가]**&#x200B;를 클릭하세요.

이제 콘텐츠에서 이미지를 만들 때 생성 모델을 선택할 수 있습니다. [이미지 생성에 대해 자세히 알아보세요](generative-image.md).

## 생성 모델 추가

>[!IMPORTANT]
>
>사용자 지정 Firefly 모델을 만들려면 Firefly ETLA 계약이 필요합니다.

사용자 지정 Firefly 모델은 고유한 자산에 대해 교육된 브랜드별 AI 모델로서, 브랜드 정체성, 스타일 및 시각적 지침에 정확하게 부합하는 이미지를 생성할 수 있도록 합니다.

맞춤형 Firefly 모델 공급자를 생성하면 기본 모델 이상으로 AI 기능을 확장하고 생성된 콘텐츠가 브랜드 고유의 미적 및 요구 사항을 일관되게 반영하도록 할 수 있습니다.

➡️ [사용자 지정 모델을 교육하는 방법 알아보기](https://helpx.adobe.com/kr/firefly/web/work-with-enterprise-features/train-custom-models/train-firefly-custom-models.html)

1. **[!UICONTROL 브랜드]** 메뉴에서 **[!UICONTROL 생성 모델]** 탭에 액세스하여 **[!UICONTROL 모델 추가]**&#x200B;를 클릭합니다.

   ![](assets/gen-model-manage-4.png){zoomable="yes"}

1. 모델의 **[!UICONTROL 이름]**&#x200B;을(를) 입력하십시오.

1. **[!UICONTROL 모델 ID]**&#x200B;를 입력하십시오.

   +++ Firefly 모델 ID 찾기

   1. Firefly 웹 사이트에 액세스하여 훈련된 모델로 이동합니다.
   1. [미리 보기 및 테스트](https://helpx.adobe.com/kr/firefly/web/work-with-enterprise-features/train-custom-models/train-firefly-custom-models.html#preview-and-test) 메뉴에 액세스합니다.
   1. URL에서 `customModelId=` 뒤에 있는 값을 찾습니다. 모델 ID로 사용하려면 이 값을 복사하십시오.

   자세한 내용은 [Firefly 사용자 지정 모델 설명서](https://helpx.adobe.com/kr/firefly/web/work-with-enterprise-features/train-custom-models/manage-custom-models.html)를 참조하세요.

   ![](assets/gen-model-manage-10.png){zoomable="yes"}

   +++

   </br>

   ![](assets/gen-model-manage-5.png){zoomable="yes"}

1. 필요한 경우 모델을 식별하는 데 도움이 되도록 **[!UICONTROL 설명]**&#x200B;을 입력하십시오.

1. 모델 구성을 확인하려면 **[!UICONTROL 연결 테스트]**&#x200B;를 클릭하십시오.

1. 연결 테스트가 성공하면 **[!UICONTROL 저장]**&#x200B;을 클릭하여 모델 구성을 저장합니다.

   ![](assets/gen-model-manage-7.png){zoomable="yes"}

1. 저장한 후 사용자 지정 모델이 모델 목록에 추가됩니다. 언제든지 비활성화하거나 삭제할 수 있습니다.

   ![](assets/gen-model-manage-8.png){zoomable="yes"}

<!--
1. Once the connection test is successful, choose whether to enable the model for selected brands.

1. Enable or disable the option to connect the model to all brands.

    If disabled, select which brands this model should be applied to.
-->

구성하고 나면 콘텐츠에서 이미지를 만들 때 사용자 지정 생성 모델을 선택할 수 있습니다. [이미지 생성에 대해 자세히 알아보세요](generative-image.md).

![](assets/gen-model-manage-9.png){zoomable="yes"}
