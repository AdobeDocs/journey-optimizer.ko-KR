---
solution: Journey Optimizer
product: journey optimizer
title: 이메일 구성 시작
description: 의 이메일 구성에 대해 자세히 알아보십시오 [!DNL Journey Optimizer]
role: Admin
level: Intermediate
feature: Application Settings
topic: Administration
exl-id: 1fc9a4f6-6c34-4414-b400-aac6bda9ee25
source-git-commit: d1c11881654580247e8d7c92237cad130f11f749
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 21%

---

# 이메일 구성 시작 {#get-starte-email-config}

에서 여정 및 캠페인을 통해 이메일을 보낼 수 있음 [!DNL Journey Optimizer]를 채우기 위해 여러 가지 구성 단계를 수행해야 합니다.

1. 최적의 게재 능력을 확보하고 평판을 보호하려면 전자 메일을 전송하는 데 사용할 하위 도메인을 Adobe 하도록 위임해야 합니다 [!DNL Journey Optimizer]. 이러한 하위 도메인은 추적할 웹 페이지 및 미러 페이지 URL과 같은 요소를 결정합니다. [자세히 알아보기](../configuration/about-subdomain-delegation.md)

   ![](../configuration/assets/subdomain-list.png)

1. 인스턴스로 제공된 IP 주소를 함께 그룹화하여 이메일 게재 능력과 평판을 향상시킵니다. [자세히 알아보기](../configuration/ip-pools.md)

   ![](../configuration/assets/ip-pool-create.png)

1. 채널 서피스를 생성하고 **[!UICONTROL 이메일]** 채널. [자세히 알아보기](../configuration/channel-surfaces.md)


   ![](../configuration/assets/preset-general.png)

1. 각 이메일 채널 화면에서 이메일을 전달하는 데 필요한 모든 기술 매개 변수를 구성합니다. [자세히 알아보기](email-settings.md)

   * 이 단계에서 전자 메일을 보내는 데 사용할 하위 도메인을 선택하고 지표와 연결할 IP 풀을 선택합니다. [자세히 알아보기](email-settings.md#subdomains-and-ip-pools)

   ![](assets/preset-subdomain-ip-pool.png)

   * 다음 **[!UICONTROL 보낸 사람 이메일]** 및 **[!UICONTROL 오류 이메일]** 주소는 현재 선택한 위임된 하위 도메인을 사용해야 합니다. [자세히 알아보기](email-settings.md#email-header)

   ![](assets/preset-header.png)

1. Adobe Experience Platform에서 여러 주소를 사용할 수 있는 경우 수신자의 우선 순위에 사용할 이메일 주소를 결정합니다. [자세히 알아보기](../configuration/primary-email-addresses.md)

   ![](../configuration/assets/primary-address-execution-fields.png)

1. 금지 목록에 이메일 주소를 보내기 전에 재시도를 하는 기간(일)을 관리합니다. [자세히 알아보기](../configuration/manage-suppression-list.md)

   ![](../configuration/assets/suppression-list-edit-retries.png)
