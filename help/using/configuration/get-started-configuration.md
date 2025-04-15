---
solution: Journey Optimizer
product: journey optimizer
title: ' [!DNL Journey Optimizer] 채널 구성 시작'
description: ' [!DNL Journey Optimizer] 채널 구성에 대해 자세히 알아보기'
role: Admin, Developer
level: Intermediate, Experienced
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
feature: Application Settings
topic: Administration
keywords: 구성, 구성하기, 메시지, 채널, 샌드박스, optimizer
source-git-commit: e052cf9bcd42cecbaaeb9047990ed603dd0730a0
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 48%

---


# 채널 구성 시작 {#start-optimizer-configuration}

[!DNL Journey Optimizer]에 처음 액세스하면 프로덕션 샌드박스가 프로비저닝되고 계약에 따라 특정 수의 IP가 할당됩니다.


메시지를 보내려면 아래 나열된 구성 단계를 수행해야 합니다.

1. [Adobe Journey Optimizer 시스템 관리자](../start/path/administrator.md)로서 채널 구성을 정의합니다. 다음 페이지에서 이러한 구성을 설정하는 방법을 알아보십시오.

<table style="table-layout:fixed"><tr style="border: 0;">
<td><a href="../email/get-started-email-config.md"><img alt="이메일" src="../channels/assets/do-not-localize/email.png"></a>
<div align="center"><a href="../email/get-started-email-config.md"><strong>이메일</strong></a></div></td>
<td><a href="../sms/sms-configuration.md"><img alt="sms" src="../channels/assets/do-not-localize/sms.png"></a>
<div align="center"><a href="../sms/sms-configuration.md"><strong>SMS</strong></a></div></td>
<td><a href="../push/push-configuration.md"><img alt="푸시" src="../channels/assets/do-not-localize/push.png"></a>
<div align="center"><a href="../push/push-configuration.md"><strong>푸시 알림</strong></a></div></td>
<td><a href="../direct-mail/direct-mail-configuration.md"><img alt="다이렉트 메일" src="../channels/assets/do-not-localize/direct-mail.jpg"></a>
<div align="center"><a href="../direct-mail/direct-mail-configuration.md"><strong>다이렉트 메일</strong></a></div></td>
</tr></table>

<table style="table-layout:fixed"><tr style="border: 0;">
<td><a href="../in-app/inapp-configuration.md"><img alt="인앱" src="../channels/assets/do-not-localize/inapp.jpg"></a>
<div align="center"><a href="../in-app/inapp-configuration.md"><strong>인앱</strong></a></div></td>
<td><a href="../web/web-configuration.md"><img alt="웹" src="../channels/assets/do-not-localize/web.jpg"></a>
<div align="center"><a href="../web/web-configuration.md"><strong>웹</strong></a></div></td>
<td><a href="../code-based/code-based-configuration.md"><img alt="코드 기반 경험" src="../channels/assets/do-not-localize/code.png"></a>
<div align="center"><a href="../code-based/code-based-configuration.md"><strong>코드 기반 경험</strong></a></div></td>
<td><a href="../content-card/content-card-configuration-prereq.md"><img alt="콘텐츠 카드" src="../channels/assets/do-not-localize/cards.png"></a>
<div align="center"><a href="../content-card/content-card-configuration-prereq.md"><strong>콘텐츠 카드</strong></a></div></td>
</tr></table>

>[!NOTE]
>
>모바일 채널의 경우 [안내 채널 설정](set-mobile-config.md)을 통해 마케팅 채널을 신속하게 구성하여 필요한 모든 리소스를 Experience Platform, Journey Optimizer 및 데이터 수집 내에서 쉽게 사용할 수 있습니다. 이렇게 하면 마케팅 팀이 캠페인 및 여정을 만들기 시작할 수 있습니다.

1. 완료되면 메시지를 전달하는 데 필요한 모든 기술 매개 변수를 구성하려면 **채널 구성**&#x200B;을 만들어야 합니다. [채널 구성에 대해 자세히 알아보기](channel-surfaces.md)

1. 다음 작업도 수행할 수 있습니다.

   * 금지 목록에 이메일 주소를 보내기 전에 재시도를 하는 기간(일)을 관리합니다. [자세히 알아보기](manage-suppression-list.md)

   * 개인 사용자에게 보내는 메시지의 사본을 보관하려면 **BBC 이메일 옵션**&#x200B;을 활성화합니다. [자세히 알아보기](archiving-support.md#enable-bcc)

   * 받는 사람을 너무 많이 사용하지 않도록 **비즈니스 규칙**&#x200B;을 구성하세요. [자세히 알아보기](../configuration/rule-sets.md)

   * Adobe Experience Platform에서 수신자의 주소/전화번호를 여러 개 사용할 수 있는 경우 어느 주소/전화번호를 우선으로 사용할지 정합니다. [자세히 알아보기](primary-email-addresses.md)
