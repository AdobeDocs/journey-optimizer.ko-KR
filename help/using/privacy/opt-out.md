---
solution: Journey Optimizer
product: journey optimizer
title: 옵트아웃 관리
description: 옵트아웃 및 개인 정보 관리 방법 알아보기
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: c5bae757-a109-45f8-bf8d-182044a73cca
source-git-commit: 8b459f71852d031dc650b77725bdc693325cdb1d
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 43%

---

# 옵트아웃 관리 {#consent}

수신자가 브랜드로부터 커뮤니케이션 수신을 거부할 수 있는 기능을 제공하는 것은 법적 요구 사항이며 이러한 선택이 허용되도록 합니다. 적용되는 법률에 대한 자세한 내용은[Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html?lang=ko#regulations){target="_blank"}를 참조하세요.

**중요한 이유**

* 이러한 규정을 준수하지 않으면 브랜드에 대한 규제 법률 리스크가 발생합니다.
* 이메일은 원하지 않는 커뮤니케이션을 수신자에게 보내지 않도록 함으로써 메시지를 스팸으로 표시하고 명성을 손상시킬 수 있습니다.

## 여정 및 캠페인에서의 구독 취소 관리 {#opt-out-ajo}

여정 또는 캠페인에서 메시지를 보낼 때 고객이 향후 커뮤니케이션에서 구독을 취소할 수 있도록 항상 확인해야 합니다. 구독이 취소되면 향후 마케팅 메시지 대상자에서 프로필이 자동으로 제거됩니다.

**[!DNL Journey Optimizer]**&#x200B;는 이메일 및 SMS 메시지에서 옵트아웃을 관리하는 방법을 제공하지만, 푸시 알림은 수신자가 디바이스를 통해 직접 구독을 취소할 수 있으므로 별도의 작업이 필요하지 않습니다. 예를 들어, 앱을 다운로드하거나 사용하는 경우 알림을 중지하도록 선택할 수 있습니다. 마찬가지로 모바일 운영 체제를 통해 알림 설정을 변경할 수 있습니다.

다음 섹션에서 Journey Optimizer 이메일 및 SMS 메시지에서 옵트아웃을 관리하는 방법을 알아봅니다.

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="../email/email-opt-out.md">
<img alt="리드" src="../assets/do-not-localize/privacy-email-optout.jpeg" width="50%">
</a>
<div><a href="../email/email-opt-out.md"><strong>이메일 옵트아웃 관리</strong>
</div>
<p>
</td>
<td>
<a href="../sms/sms-opt-out.md">
<img alt="드물게" src="../assets/do-not-localize/privacy-sms-opt-out.jpeg" width="50%">
</a>
<div>
<a href="../sms/sms-opt-out.md"><strong>SMS 옵트아웃 관리</strong></a>
</div>
<p></td>
</tr></table>

>[!NOTE]
>
>[!DNL Journey Optimizer]에서 동의는 Experience Platform [동의 스키마](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html?lang=ko){target="_blank"}. By default, the value for the consent field is empty and treated as consent to receive your communications. You can modify this default value while onboarding to one of the possible values listed [here](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html?lang=ko#choice-values){target="_blank"}가 처리합니다.

## 개인화 동의 구현 {#opt-out-personalization}

고객은 개인화된 콘텐츠를 표시하지 않도록 선택할 수도 있습니다. 프로필이 개인화를 옵트아웃한 경우 해당 데이터가 개인화에 사용되지 않도록 해야 하며 개인화된 모든 콘텐츠를 대체 변형으로 교체해야 합니다.

### 의사 결정 관리

오퍼를 활용하는 경우 개인화 환경 설정은에서 자동으로 구현되지 않습니다. [결정 범위](../offers/offer-activities/create-offer-activities.md#add-decision-scopes) 다음에서 사용됨: [의사 결정](../offers/api-reference/offer-delivery-api/decisioning-api.md) API 요청 또는 [edge decisioning](../offers/api-reference/offer-delivery-api/edge-decisioning-api.md) API 요청. 이 경우 개인화 동의를 수동으로 적용해야 합니다. 이렇게 하려면 아래 단계를 수행합니다.

>[!NOTE]
>
>에 사용되는 결정 범위 [!DNL Journey Optimizer] 작성된 채널은 속한 여정 또는 캠페인에서 이 요구 사항을 충족합니다.



1. 만들기 [Adobe Experience Platform 세그먼트](../segment/about-segments.md) 프로필 속성 사용: *&quot;개인화에 대한 동의 = True&quot;* 개인화에 동의한 사용자를 타겟팅할 수 있습니다.

1. 를 만들 때 [결정](../offers/offer-activities/create-offer-activities.md), 의사 결정 범위를 추가하고 개인화된 오퍼를 포함하는 각 평가 기준 컬렉션에 대해 이 세그먼트를 기반으로 자격 제한 사항을 정의합니다.

1. 만들기 [대체 오퍼](../offers/offer-library/creating-fallback-offers.md) 여기에는 개인화된 콘텐츠가 포함되지 않습니다.

1. [할당](../offers/offer-activities/create-offer-activities.md#add-fallback) 결정에 대한 개인화되지 않은 대체 오퍼입니다.

1. [검토 및 저장](../offers/offer-activities/create-offer-activities.md#review) 결정.

사용자에게 다음이 있는 경우:

* 개인화에 동의하면 결정 범위가 해당 프로필에 대한 최상의 오퍼를 결정합니다.

* 개인화에 동의하지 않으면 해당 프로필은 평가 기준에 있는 오퍼에 적격하지 않으므로 개인화되지 않은 대체 오퍼를 수신하게 됩니다.

>[!NOTE]
>
>에서 프로필 데이터를 사용하는 데 대한 동의 [데이터 모델링](../offers/ranking/ai-models.md) 은(는)에서 아직 지원되지 않습니다. [!DNL Journey Optimizer].

