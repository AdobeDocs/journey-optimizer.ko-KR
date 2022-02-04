---
title: 시스템 관리자용 Journey Optimizer 시작하기
description: 시스템 관리자는 Journey Optimizer을 사용하여 작업하는 방법에 대해 자세히 알아봅니다
level: Intermediate
exl-id: 24f85ced-aa45-493f-b2c4-7c7b58351b38
source-git-commit: 7a07f2348f08b4582a1310fb65d431c55451d9b6
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 2%

---

# 시스템 관리자용 시작하기 {#get-started-sys-admins}

![administrator](assets/do-not-localize/user-2.png)

사용을 시작하기 전 [!DNL Adobe Journey Optimizer]를 채울 때는 몇 가지 단계를 수행해야 합니다.  다음 단계를 수행하여 [데이터 엔지니어](data-engineer.md) 및 [여정 연습](marketer.md) 작업 시작 [!DNL Adobe Journey Optimizer].


로서의 **시스템 관리자**: **제품 프로필 이해 및 권한 할당** 샌드박스 관리 및 채널 구성용. 또한 샌드박스를 설정하고 사용 가능한 제품 프로필에 대해 관리해야 합니다. 그런 다음 팀 구성원을 제품 프로필에 할당할 수 있습니다.

이러한 기능은 **[!UICONTROL Product administrators]** admin console에 액세스할 수 있습니다. [Adobe Admin Console에 대해 자세히 알아보기](https://helpx.adobe.com/kr/enterprise/admin-guide.html){target=&quot;_blank&quot;}.

다음 페이지에서 액세스 관리에 대해 알아봅니다.

1. **샌드박스 만들기** 인스턴스를 격리된 별도의 가상 환경으로 분할합니다. **샌드박스** 에서 작성됨 [!DNL Journey Optimizer]. 자세한 내용은 [샌드박스](../../administration/sandboxes.md) 섹션을 참조하십시오.

   >[!NOTE]
   >로서의 **시스템 관리자**&#x200B;가 표시되지 않으면 **[!UICONTROL Sandboxes]** 메뉴 [!DNL Journey Optimizer]에서 권한을 업데이트합니다. [Admin Console](https://adminconsole.adobe.com/){_blank}. 에서 제품 프로필을 업데이트하는 방법을 알아봅니다 [이 페이지](../../administration/permissions.md#edit-product-profile).

1. **제품 프로필 이해**. 제품 프로필은 사용자가 인터페이스의 특정 기능 또는 개체에 액세스할 수 있도록 하는 통합된 권리 집합입니다. 자세한 내용은 [기본 제품 프로필](../../administration/ootb-product-profiles.md) 섹션을 참조하십시오.

1. **권한 설정** 제품 프로필의 경우 **샌드박스**&#x200B;를 채울 수 있고 다른 제품 프로필에 할당할 수 있으므로 팀 구성원에게 액세스 권한을 제공합니다. 이 단계는 [Admin Console](https://adminconsole.adobe.com/){_blank}. 권한은 사용자에게 할당된 승인을 정의할 수 있는 통합된 권리입니다 **[!UICONTROL Product profile]**. 각 권한은 여정, 메시지 또는 오퍼와 같은 기능에 수집되며, 이 기능은 의 다양한 기능 또는 개체를 나타냅니다 [!DNL Journey Optimizer]. 자세한 내용은 [권한 수준](../../administration/high-low-permissions.md) 섹션을 참조하십시오.

또한 Assets Essentials 액세스 권한이 필요한 사용자를 **Assets Essentials 소비자 사용자** 또는/and **Assets Essentials 사용자** 제품 프로필. [Assets Essentials 설명서에서 자세한 내용](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html){target=&quot;_blank&quot;}.

>[!NOTE]
>2022년 1월 6일 이전에 획득한 Journey Optimizer 제품의 경우 를 배포해야 합니다 [!DNL Adobe Experience Manager Assets Essentials] 사용할 수 있습니다. 자세한 내용은 [Assets Essentials 배포](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html){target=&quot;_blank&quot;} 섹션.

액세스 시 [!DNL Journey Optimizer] 처음으로 프로덕션 샌드박스를 프로비저닝하고 계약에 따라 특정 수의 IP를 할당하게 됩니다.

여정을 만들고 메시지를 보내려면 **관리** 메뉴 아래의 제품에서 사용할 수 있습니다. 찾아보기 **[!UICONTROL Channels]** 메뉴를 사용하여 이메일 메시지 및 사전 설정을 구성할 수 있습니다.

>[!NOTE]
>로서의 **시스템 관리자**&#x200B;가 표시되지 않으면 **[!UICONTROL Channels]** 메뉴 [!DNL Journey Optimizer]에서 권한을 업데이트합니다. [Admin Console](https://adminconsole.adobe.com/){_blank}. 에서 제품 프로필을 업데이트하는 방법을 알아봅니다 [이 페이지](../../administration/permissions.md#edit-product-profile).

아래 나열된 단계를 수행합니다.

1. **메시지 및 채널 구성**: 사전 설정 정의, 이메일 및 푸시 메시지 설정 조정 및 사용자 정의

   * 정의 **푸시 알림 설정** 둘 다 [!DNL Adobe Experience Platform] 및 [!DNL Adobe Experience Platform Launch]. [자세히 알아보기](../../messages/push-gs.md)

   * 만들기 **메시지 사전 설정** 전자 메일 및 푸시 알림 메시지에 필요한 모든 기술 매개 변수를 구성하려면 다음을 수행하십시오. [자세히 알아보기](../../configuration/message-presets.md)

   * 해당 기간(일 수)을 관리합니다 **다시 시도** 전자 메일 주소를 제외 목록으로 보내기 전에 수행됩니다. [자세히 알아보기](../../configuration/manage-suppression-list.md)

1. **하위 도메인 위임**: Journey Optimizer에서 사용할 새 하위 도메인의 경우 첫 번째 단계는 하위 도메인을 위임하는 것입니다. [자세히 알아보기](../../configuration/about-subdomain-delegation.md)

   ![](../../assets/subdomain.png)

1. **IP 풀 만들기**: 인스턴스로 제공된 IP 주소를 그룹화하여 이메일 게재 능력과 평판을 향상시킵니다. [자세히 알아보기](../../configuration/ip-pools.md)

   ![](../../assets/ip-pool.png)

1. **억제 및 허용 목록 관리**: 억제 및 허용 목록을 통해 게재 능력 개선

   * A [제외 목록](../../messages/suppression-list.md) 은(는) 이러한 연락처로 보내면 전송 신뢰도와 전송 속도가 저하될 수 있으므로 게재에서 제외할 이메일 주소로 구성됩니다. 잘못된 주소, 일관된 소프트 바운스(소프트 바운스)를 갖는 주소, 이메일 평판에 부정적인 영향을 줄 수 있는 수신자 등 여정에서 전송하지 않고 자동으로 제외된 모든 이메일 주소를 모니터링할 수 있으며, 이메일 메시지 중 하나에 대해 어떤 종류의 스팸 불만 사항을 제기하는 수신자도 모니터링할 수 있습니다. 관리 방법 알아보기 [제외 목록](../../configuration/manage-suppression-list.md) 및 [다시 시도](../../configuration/retries.md).
   ![](../../assets/suppression-list-filtering-example.png)

   * 다음 [허용 목록](../../messages/allow-list.md) 특정 샌드박스에서 보내는 이메일을 받을 수 있는 권한이 있는 유일한 수신자 또는 도메인이 되는 개별 이메일 주소 또는 도메인을 지정할 수 있도록 해줍니다. 따라서 테스트 환경에 있을 때 실수로 실제 고객 주소로 이메일을 보내지 않을 수 있습니다. 방법 알아보기 [허용 목록 활성화](../../messages/allow-list.md).
   의 게재 기능 관리에 대해 자세히 알아보십시오 [!DNL Adobe Journey Optimizer] [이 페이지에서](../../messages/deliverability.md).
