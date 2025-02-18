---
solution: Journey Optimizer
product: journey optimizer
title: IP 워밍업 캠페인 만들기
description: IP 준비 캠페인을 만드는 방법을 알아봅니다.
feature: Campaigns, IP Warmup Plans
topic: Administration
role: Admin
level: Intermediate
keywords: IP, 풀, 전달성
exl-id: a9995ca1-d7eb-4f8d-a9d9-fe56198ac325
source-git-commit: 84cbaebc9c274f620ee707cb0d9320673ae24b71
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 11%

---

# IP 워밍업 캠페인 만들기 {#create-ip-warmup-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_ip_warmup"
>title="IP 워밍업 플랜 활성화 옵션"
>abstract="이 옵션을 선택하면 IP 워밍업 플랜에서 캠페인을 사용할 수 있습니다. 그런 다음 캠페인 일정은 관련 IP 워밍업 플랜에 따라 결정됩니다."

[!DNL Journey Optimizer]에서 IP 준비 계획 자체를 만들기 전에 먼저 IP 준비 계획<!--through a dedicated option-->에서 사용하도록 특별히 디자인된 캠페인을 하나 이상 만들어야 합니다.

IP 준비 캠페인을 만들려면 아래 단계를 수행합니다.

1. 준비 계획에 대해 식별한 도메인 및 IP에 대한 전자 메일 채널 [구성](channel-surfaces.md)을(를) 만듭니다.

   전달성 컨설턴트와 함께 사용할 도메인 및 IP를 식별합니다. [이 섹션](../email/email-settings.md#subdomains-and-ip-pools)에서 전자 메일 구성에서 선택하는 방법을 알아보세요.

   >[!CAUTION]
   >
   >IP 준비 계획이 [시작](ip-warmup-execution.md)된 후에는 전자 메일 채널 구성을 편집하지 마십시오.

1. 예약된 마케팅 [캠페인](../campaigns/create-campaign.md)을(를) 만들고 [이메일](../email/create-email.md#create-email-journey-campaign) 작업을 선택합니다.

   <!--Select the Marketing category. The IP warmup plan activation option is only available for  marketing-type campaigns.-->

1. IP 웜업을 위해 만든 구성을 선택합니다.

   ![](assets/ip-warmup-campaign-surface.png)

   <!--You must use the same configuration as the one that will be used for the asociated IP warmup plan. [Learn how to create an IP warmup plan](#create-ip-warmup-plan)-->

1. **[!UICONTROL 만들기]**&#x200B;를 클릭합니다.

1. **[!UICONTROL 일정]** 섹션에서 **[!UICONTROL IP 준비 계획 활성화]**&#x200B;를 선택합니다.

   ![](assets/ip-warmup-campaign-plan-activation.png)

   [일정](../campaigns/create-campaign.md#schedule) 캠페인은 연결된 IP 준비 계획에 따라 진행됩니다. 즉, 캠페인 자체에 더 이상 일정이 정의되지 않습니다.

1. 캠페인 속성, [대상자](../audience/about-audiences.md)<!--best practices for IP warmup in terms of audience?--> 및 [콘텐츠](../email/get-started-email-design.md#key-steps)를 정의하는 등 이메일 캠페인을 만드는 단계를 완료하십시오.

   >[!IMPORTANT]
   >
   >IP 준비 캠페인에 허용된 대상은 [세그먼트 기반](../audience/creating-a-segment-definition.md)이어야 하며 [기본 병합 정책](https://experienceleague.adobe.com/en/docs/experience-platform/profile/merge-policies/overview#default-merge-policy){target="_blank"}을(를) 사용하여 만들어야 합니다.

   캠페인을 구성하는 방법에 대한 자세한 내용은 [이 페이지](../campaigns/get-started-with-campaigns.md)를 참조하세요.

1. 캠페인을 [활성화](../campaigns/review-activate-campaign.md)합니다. 상태가 **[!UICONTROL Live]**(으)로 변경됩니다.

   >[!NOTE]
   >
   >[비즈니스 규칙](rule-sets.md#apply-frequency-rule)은(는) IP 준비 계획에 사용할 수 없습니다. 이러한 규칙을 적용하면 캠페인에 대해 원하는 수의 타겟팅된 프로필에 도달하지 못할 수 있습니다.

   IP 준비 계획이 활성화된 라이브 캠페인의 경우 **[!UICONTROL 삭제]** 단추를 IP 준비 계획과 연결할 때까지 사용할 수 있습니다. 플랜에 사용된 후에는 캠페인을 더 이상 삭제할 수 없습니다.

1. 캠페인이 **[!UICONTROL 캠페인]** 목록에 표시됩니다. 현재 샌드박스에서 만든 모든 IP 준비 캠페인을 쉽게 검색하려면 **[!UICONTROL IP 준비]** 캠페인 옵션을 필터링하면 됩니다.

   ![](assets/ip-warmup-campaign-filter.png)

라이브가 되면 캠페인이 IP 준비 계획에 사용할 준비가 되었습니다. [자세히 알아보기](ip-warmup-plan.md)

IP 준비 캠페인은 하나의 IP 준비 계획에서만 사용할 수 있습니다. 그러나 동일한 IP 웜업 계획의 하나 이상의 단계에서 동일한 캠페인을 사용할 수 있습니다. [자세히 알아보기](ip-warmup-plan.md#define-phases)

>[!NOTE]
>
>IP 준비 계획에 라이브 캠페인을 사용할 때 플랜이 [완료된 것으로 표시](ip-warmup-execution.md#mark-as-completed)된 후 해당 캠페인의 상태가 **[!UICONTROL 중지됨]**(으)로 변경됩니다.

