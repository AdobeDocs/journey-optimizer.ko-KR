---
solution: Journey Optimizer
product: journey optimizer
title: 이메일 구성 시작
description: ' [!DNL Journey Optimizer]의 이메일 구성 자세히 알아보기'
role: Admin
level: Experienced
feature: Channel Configuration, Email
topic: Administration
keywords: 이메일, 구성, 표면, 하위 도메인
exl-id: 1fc9a4f6-6c34-4414-b400-aac6bda9ee25
source-git-commit: ea8f77c2821bfae7b853b3ac39ea22f0d19ae43d
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 62%

---

# 이메일 구성 시작 {#get-starte-email-config}

[!DNL Journey Optimizer]에서 여정 및 캠페인을 통해 이메일을 보내려면 몇 가지 구성 단계를 완료해야 합니다.

1. 최적의 전달성을 보장하고 평판을 보호하려면 **과(와) 함께 전자 메일을 보내는 데 사용할**&#x200B;하위 도메인을 Adobe에 위임[!DNL Journey Optimizer]하는 것으로 시작하십시오. 하위 도메인은 추적할 웹 페이지와 미러 페이지 URL 등 요소를 결정합니다. [자세히 알아보기](../configuration/about-subdomain-delegation.md)

   ![](../configuration/assets/subdomain-list.png)

1. 인스턴스와 함께 제공된 **IP 주소를 함께 그룹화**&#x200B;할 IP 풀을 만듭니다. [자세히 알아보기](../configuration/ip-pools.md)

   ![](../configuration/assets/ip-pool-create.png)

1. **채널 구성**&#x200B;을 만들고 **[!UICONTROL 이메일]** 채널을 선택하십시오. [자세히 알아보기](../configuration/channel-surfaces.md)


   ![](../configuration/assets/preset-general.png)

1. 각 전자 메일 채널 구성에서 전자 메일을 전달하는 데 필요한 모든 **기술 매개 변수**&#x200B;를 구성하십시오. [자세히 알아보기](email-settings.md)

   * 이때 이메일을 보내는 데 사용할 하위 도메인과, 구성에 연결할 IP 풀을 선택합니다. [자세히 알아보기](email-settings.md#subdomains-and-ip-pools)

   ![](assets/surface-subdomain-ip-pool.png)

   * **[!UICONTROL 보내는 사람 이메일]**&#x200B;과 **[!UICONTROL 오류 이메일]** 주소는 현재 선택한 위임된 하위 도메인을 사용해야 합니다. [자세히 알아보기](email-settings.md#email-header)

   ![](assets/preset-header.png)

1. Adobe Experience Platform에서 여러 주소를 사용할 수 있는 경우 받는 사람의 우선 순위에서 사용할 **실행 필드**&#x200B;를 결정하십시오. [자세히 알아보기](../configuration/primary-email-addresses.md)

   ![](../configuration/assets/primary-address-execution-fields.png)

1. 금지 목록에 이메일 주소를 보내기 전에 **재시도**&#x200B;를 하는 기간(일)을 관리합니다. [자세히 알아보기](../configuration/manage-suppression-list.md)

   ![](../configuration/assets/suppression-list-edit-retries.png)
