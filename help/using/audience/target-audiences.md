---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Experience Platform 대상자 정보
description: Adobe Experience Platform 대상자 사용 방법 알아보기
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 78b95ccd-bc28-46cd-937a-f68e3f34cc1e
source-git-commit: d7ebba4144eeb5b29e9e6fa21afde06a7e520e07
workflow-type: tm+mt
source-wordcount: '567'
ht-degree: 25%

---

# [!DNL Journey Optimizer]의 대상자 활성화 {#segments-in-journey-optimizer}

캠페인 및 여정에서 세그먼트 정의, 사용자 지정 업로드, 작성 워크플로우 또는 페더레이션 대상 작성을 사용하여 생성된 대상을 선택할 수 있습니다.

>[!AVAILABILITY]
>
>대상자 작성의 대상자 및 속성은 현재 Healthcare Shield 또는 Privacy and Security Shield에서 사용할 수 없습니다. [Journey Optimizer에서 대상 데이터 보강 특성을 사용하는 방법을 알아보세요](../audience/about-audiences.md#enrichment)

## 대상자 활성화 지연 {#activation}

대상자는 수집이 완료된 후 바로 Journey Optimizer에서 사용할 준비가 되었습니다. 일반적으로 1시간 이내이지만 약간의 변동성이 있습니다. 컴포지션으로 인한 대상자는 게시 후 24시간 후에 사용할 수 있어야 합니다.

## 사용자 지정 업로드 및 페더레이션 대상 구성

사용자 지정 업로드 및 Federated Audience Composition 대상자의 경우, 다음 보호 기능을 참조하십시오.

* **미리 보기 및 증명 지원:** 현재 미리 보기 및 증명은 CSV 업로드 또는 Federated Audience Composition을 사용하여 만든 대상에 대해 지원되지 않습니다. 캠페인을 계획할 때는 이 점을 염두에 두십시오.

* **새 프로필 타깃팅:** 레코드와 UPS 프로필 간에 일치하는 항목을 찾을 수 없으면 새 빈 프로필이 만들어집니다. 이 프로필은 데이터 레이크에 저장된 데이터 보강 속성에 연결됩니다. 이 새 프로필은 비어 있으므로 Journey Optimizer에서 일반적으로 사용되는 타겟팅 필드(예: personalEmail.address, mobilePhone.number)는 비어 있으므로 타겟팅에 사용할 수 없습니다.

  이를 해결하려면 채널 구성에서 &quot;실행 필드&quot;(또는 채널에 따른 &quot;실행 주소&quot;)를 &quot;identityMap&quot;으로 지정할 수 있습니다. 이렇게 하면 대상을 만들 때 ID로 선택한 속성이 Journey Optimizer에서 타깃팅에 사용되는 속성이 됩니다.

* **활성화된 레코드 및 ID 결합:** 대상자의 모든 레코드는 모든 중복을 포함하여 활성화됩니다. 다음 UPS 프로필 내보내기 동안 이러한 레코드는 ID 결합을 거칩니다. 그 결과 활성화된 레코드 수는 ID 결합 후 프로필 수와 다를 수 있습니다.

## [!DNL Journey Optimizer]의 대상

**[!DNL Journey Optimizer]**&#x200B;에서 다양한 방법으로 대상자를 활용할 수 있습니다.

* **캠페인** 대상자를 선택하면 선택한 대상자에 속하는 모든 개인에게 메시지를 보냅니다. [캠페인의 대상자를 정의하는 방법을 알아봅니다](../campaigns/create-campaign.md#define-the-audience-audience).

* 여정에서 **대상자 읽기** 오케스트레이션 활동을 사용하여 대상자의 모든 개인이 여정을 입력하고 여정에 포함된 메시지를 받도록 합니다. “실버 고객”이라는 대상자가 있다고 가정해 보겠습니다. 이 활동으로 모든 실버 고객이 여정에 입장하도록 하여 이들에게 연속으로 이어지는 개인화된 메시지를 보낼 수 있습니다. [대상자 읽기 활동을 구성하는 방법을 알아봅니다](../building-journeys/read-audience.md#configuring-segment-trigger-activity).

  >[!NOTE]
  >
  >대상 읽기 활동의 대상 구성 또는 사용자 지정 업로드에서 대상을 활용하는 모든 여정은 마지막 일괄 처리 평가만큼 새로운 프로필 속성을 갖게 됩니다. 여기에는 여정의 동의/억제도 포함됩니다.

* 여정에 **조건** 활동을 사용하면 대상자 멤버십을 기반으로 조건을 작성할 수 있습니다. [조건에서 대상자를 사용하는 방법을 알아봅니다](../building-journeys/condition-activity.md#using-a-segment).

* 여정에서 **대상 자격** 이벤트 활동을 사용하여 개인이 Adobe Experience Platform 대상 출입구를 기준으로 여정에 들어오거나 앞으로 이동하도록 할 수 있습니다. 예를 들면 모든 신규 실버 고객이 여정에 입장하도록 하여 이들에게 메시지를 보낼 수 있습니다. 이 활동을 사용하는 자세한 방법은 [대상자 선별 활동을 구성하는 방법 알아보기](../building-journeys/audience-qualification-events.md)를 참조하세요.

  >[!NOTE]
  >
  >작성 워크플로우, 사용자 지정 업로드 또는 연합 대상 작성을 사용하여 만든 대상의 일괄 처리 특성으로 인해, &quot;대상 자격&quot; 활동에서 이러한 대상을 타깃팅할 수 없습니다. 세그먼트 정의를 사용하여 생성된 대상만 이 활동에서 활용할 수 있습니다.
