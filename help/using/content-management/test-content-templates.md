---
solution: Journey Optimizer
product: journey optimizer
title: 콘텐츠 템플릿 테스트
description: 일부 이메일 콘텐츠 템플릿의 렌더링을 테스트하는 방법을 알아봅니다
feature: Templates
topic: Content Management
role: User
level: Beginner
exl-id: 01726ab6-f581-4d19-aedd-2541bc0f27c6
TQID: https://experienceleague.adobe.com/CC56E9rV4TImjLBbm-fsq2a4JKLnEA4wJB2DVLgOAfM
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: dc22c819-3f29-4e91-8b7d-5c6719831141id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: a5683ded-e5d5-4ec6-b9fd-e1b56a94ab96id: d595a60b-bcf5-4a63-a189-66a0be755cc7id: f8d2e9f0-69c9-40cd-890f-71336c8dfff7id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 252
ht-degree: 4%

---

# 이메일 콘텐츠 템플릿 테스트 {#test-template}

처음부터 만들거나 기존 콘텐츠에서 만든 일부 이메일 템플릿의 렌더링을 테스트할 수 있습니다. 그 방법은 다음과 같습니다.

1. **[!UICONTROL 콘텐츠 관리]** > **[!UICONTROL 콘텐츠 템플릿]** 메뉴를 통해 콘텐츠 템플릿 목록에 액세스하고 전자 메일 템플릿을 선택합니다.

1. **[!UICONTROL 템플릿 속성]**&#x200B;에서 **[!UICONTROL 콘텐츠 편집]**&#x200B;을 클릭합니다.

1. **[!UICONTROL 콘텐츠 시뮬레이션]**&#x200B;을 클릭하고 테스트 프로필을 선택하여 렌더링을 확인합니다. [자세히 알아보기](../content-management/preview-test.md)

   ![](assets/content-template-stimulate.png)

   >[!NOTE]
   >
   >[!DNL Journey optimizer]을(를) 사용하면 콘텐츠 템플릿을 미리 보고 CSV/JSON 파일에서 업로드하거나 수동으로 추가한 샘플 입력 데이터를 사용하여 증명을 전송하여 다양한 변형을 테스트할 수도 있습니다. [콘텐츠 변형을 시뮬레이션하는 방법을 알아봅니다](../test-approve/simulate-sample-input.md)

1. 여정 또는 캠페인에서 사용하기 전에 증명을 전송하여 콘텐츠를 테스트하고 일부 내부 사용자에 의해 승인받을 수 있습니다.

   * 이렇게 하려면 **[!UICONTROL 증명 보내기]** 단추를 클릭하고 [이 섹션](../content-management/proofs.md)에 설명된 단계를 수행합니다.

   * 증명을 보내기 전에 콘텐츠를 테스트하는 데 사용할 [전자 메일 구성](../configuration/channel-surfaces.md)을(를) 선택해야 합니다.

     ![](assets/content-template-stimulate-proof-surface.png)

>[!CAUTION]
>
>현재 추적은 이메일 콘텐츠 템플릿을 테스트할 때 지원되지 않습니다. 즉, 이벤트, UTM 매개 변수 및 랜딩 페이지 링크를 추적하는 것은 템플릿에서 전송되는 증명에서 효과적이지 않습니다. 추적을 테스트하려면 전자 메일에서 [콘텐츠 템플릿을 사용](../email/use-email-templates.md)하고 테스트 프로필 또는 CSV/JSON 파일에서 업로드하거나 수동으로 추가한 샘플 입력 데이터를 사용하여 증명을 보냅니다. [콘텐츠를 미리 보고 테스트하는 방법에 대해 알아보세요](../content-management/preview-test.md)
