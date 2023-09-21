---
solution: Journey Optimizer
product: journey optimizer
title: IP 준비 캠페인 만들기
description: IP 준비 캠페인을 만드는 방법을 알아봅니다.
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP, 풀, 그룹, 하위 도메인, 전달성
hide: true
hidefromtoc: true
source-git-commit: ea86d44f7c9309ff69877e01cea6a13e7907a039
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 3%

---

# IP 준비 캠페인 만들기 {#create-ip-warmup-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_ip_warmup"
>title="IP 준비 계획 옵션 활성화"
>abstract="IP 웜업 플랜 활성화 옵션을 선택합니다. 캠페인이 라이브되면 IP 준비 플랜과 연결할 수 있습니다."

>[!BEGINSHADEBOX]

이 설명서의 내용:

* [IP 준비 시작](ip-warmup-gs.md)
* **[IP 준비 캠페인 만들기](ip-warmup-campaign.md)**
* [IP 준비 계획 만들기](ip-warmup-plan.md)
* [IP 준비 계획 실행](ip-warmup-running.md)

>[!ENDSHADEBOX]

IP 준비 계획에 사용할 수 있도록 특정 옵션이 활성화된 캠페인을 하나 이상 만들어야 합니다.

IP 준비 캠페인을 만들려면 아래 단계를 수행합니다.

1. 이메일 만들기 [표면](channel-surfaces.md) 준비 계획에 대해 식별한 도메인 및 IP에 대해 해당됩니다.<!--how do you identify these or who does it at the customer level?-->

   >[!NOTE]
   >
   >의 이메일 표면에서 사용할 도메인 및 IP를 선택하는 방법을 알아봅니다. [이 섹션](../email/email-settings.md#subdomains-and-ip-pools).

1. 만들기 [campaign](../campaigns/create-campaign.md) 및 선택 [이메일](../email/create-email.md#create-email-journey-campaign) 작업.

1. IP 웜업을 위해 생성한 서피스를 선택합니다.

   ![](assets/ip-warmup-campaign-surface.png)

   <!--You must use the same surface as the one that will be used for the asociated IP warmup plan. [Learn how to create an IP warmup plan](#create-ip-warmup-plan)-->

1. **[!UICONTROL 만들기]**&#x200B;를 클릭합니다.

1. 다음에서 **[!UICONTROL 예약]** 섹션, 선택 **[!UICONTROL IP 준비 계획 활성화]**.

   ![](assets/ip-warmup-campaign-plan-activation.png)

   캠페인 [예약](../campaigns/create-campaign.md#schedule) 이(가) 다음에 의해 구동됩니다. [IP 준비 계획](ip-warmup-plan.md) 와 연결됩니다. 즉, 캠페인 자체에서 일정이 더 이상 정의되지 않습니다.

1. [활성화](../campaigns/review-activate-campaign.md) 캠페인. 라이브 상태가 되면 IP 준비 계획에 사용할 수 있습니다.

>[!NOTE]
>
>IP 준비 계획이 활성화된 라이브 캠페인의 경우 **[!UICONTROL 삭제]** 단추는 IP 준비 계획과 연결될 때까지 사용할 수 있습니다.

캠페인 구성 방법에 대한 자세한 내용은 다음을 참조하십시오. [이 페이지](../campaigns/get-started-with-campaigns.md).

<!--Any recommendations when defining an audience? i.e do you have to include all your database or a limited number or according to your Excel file?-->

