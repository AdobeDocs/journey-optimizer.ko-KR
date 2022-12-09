---
solution: Journey Optimizer
product: journey optimizer
title: 옵트아웃 관리
description: 옵트아웃 및 개인 정보를 관리하는 방법 알아보기
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: c5bae757-a109-45f8-bf8d-182044a73cca
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 0%

---

# 옵트아웃 관리 {#consent}

## 옵트아웃 관리 기본 정보 {#about}

수신자가 브랜드로부터 커뮤니케이션 수신을 취소할 수 있는 기능을 제공하는 것은 법적 요구 사항입니다. 에서 해당 법률에 대해 자세히 알아보십시오 [Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html#regulations){target=&quot;_blank&quot;}.

**중요한 이유는 무엇입니까?**

* 이러한 규정을 준수하지 않으면 브랜드에 대한 규정 법적 위험이 발생합니다.
* 요청하지 않은 커뮤니케이션을 수신자에게 보내지 않도록 하는 데 도움이 되며, 수신자는 메시지를 스팸으로 표시하고 자신의 명성을 손상시킬 수 있습니다.

## Journey Optimizer의 옵트아웃 관리 {#opt-out-ajo}

여정 또는 캠페인에서 메시지를 보낼 때 고객이 미래 커뮤니케이션에서 구독을 취소할 수 있도록 항상 확인해야 합니다. 가입 해지되면 향후 마케팅 메시지 대상자에서 프로필이 자동으로 제거됩니다.

While **[!DNL Journey Optimizer]** 은 이메일 및 SMS 메시지에서 옵트아웃을 관리하는 방법을 제공하며, 수신자는 자체 장치를 통해 옵트아웃을 취소할 수 있으므로 푸시 알림은 사용자 측에서 어떤 작업도 필요하지 않습니다. 예를 들어 앱을 다운로드하거나 사용할 때 알림을 중지하도록 선택할 수 있습니다. 마찬가지로 모바일 운영 체제를 통해 알림 설정을 변경할 수 있습니다.

다음 섹션에서 Journey Optimizer 이메일 및 SMS 메시지에서 옵트아웃을 관리하는 방법을 알아봅니다.

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="../email/email-opt-out.md">
<img alt="리드" src="../assets/do-not-localize/privacy-email-optout.jpeg" width="50%&gt;
&lt;/a&gt;
&lt;div&gt;&lt;a href=" ../email/email-opt-out.md"><strong>이메일 옵트아웃 관리</strong>
</div>
<p>
</td>
<td>
<a href="../sms/sms-opt-out.md">
<img alt="자주" src="../assets/do-not-localize/privacy-sms-opt-out.jpeg" width="50%&gt;
&lt;/a&gt;
&lt;div&gt;
&lt;a href=" ../sms/sms-opt-out.md"><strong>SMS 옵트아웃 관리</strong></a>
</div>
<p></td>
</tr></table>

>[!NOTE]
>
>in [!DNL Journey Optimizer], 동의는 Experience Platform에 의해 처리됩니다 [동의 스키마](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html){target=&quot;_blank&quot;}. 기본적으로 동의 필드의 값은 비어 있으며 커뮤니케이션을 수신하기 위한 동의로 처리됩니다. 나열된 가능한 값 중 하나로 온보딩하는 동안 이 기본값을 수정할 수 있습니다 [여기](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html#choice-values){target=&quot;_blank&quot;}.