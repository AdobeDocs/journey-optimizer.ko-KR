---
solution: Journey Optimizer
product: journey optimizer
title: 콘텐츠 템플릿 테스트
description: 일부 이메일 콘텐츠 템플릿의 렌더링을 테스트하는 방법을 알아봅니다
feature: Templates
topic: Content Management
role: User
level: Beginner
source-git-commit: 59c675dd2ac94b6967cfb3a93f74b2016a090190
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 4%

---

# 이메일 콘텐츠 템플릿 테스트 {#test-template}

처음부터 만들거나 기존 콘텐츠에서 만든 일부 이메일 템플릿의 렌더링을 테스트할 수 있습니다. 그 방법은 다음과 같습니다.

1. 다음을 통해 콘텐츠 템플릿 목록에 액세스 **[!UICONTROL 콘텐츠 관리]** > **[!UICONTROL 콘텐츠 템플릿]** 을(를) 메뉴에서 선택하고 이메일 템플릿을 선택합니다.

1. 클릭 **[!UICONTROL 콘텐츠 편집]** 다음에서 **[!UICONTROL 템플릿 속성]**.

1. 클릭 **[!UICONTROL 콘텐츠 시뮬레이션]** 그리고 테스트 프로필을 선택하여 렌더링을 확인합니다. [자세히 알아보기](../content-management/preview-test.md)

   ![](assets/content-template-stimulate.png)

1. 여정 또는 캠페인에서 사용하기 전에 증명을 전송하여 콘텐츠를 테스트하고 일부 내부 사용자에 의해 승인받을 수 있습니다.

   * 이렇게 하려면 **[!UICONTROL 증명 보내기]** 버튼을 누르고 다음에 설명된 단계를 따릅니다. [이 섹션](../content-management/proofs.md).

   * 증명을 보내기 전에 [이메일 표면](../configuration/channel-surfaces.md) 콘텐츠를 테스트하는 데 사용됩니다.

     ![](assets/content-template-stimulate-proof-surface.png)

>[!CAUTION]
>
>현재 추적은 이메일 콘텐츠 템플릿을 테스트할 때 지원되지 않습니다. 즉, 이벤트, UTM 매개 변수 및 랜딩 페이지 링크를 추적하는 것은 템플릿에서 전송되는 증명에서 효과적이지 않습니다. 추적을 테스트하려면 [콘텐츠 템플릿 사용](../email/use-email-templates.md) 이메일 및 [증명 보내기](../content-management/preview-test.md#send-proofs).
