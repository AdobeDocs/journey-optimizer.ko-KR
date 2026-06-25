---
solution: Journey Optimizer
product: journey optimizer
title: 푸시 알림 시작
description: Journey Optimizer에서 푸시 알림을 만드는 방법 알아보기
feature: Overview, Push
topic: Content Management
role: User
level: Beginner
exl-id: c1f16edd-efdf-41c2-a0ad-5f55009008f5
TQID: https://experienceleague.adobe.com/S-3ZtTNfgZGEFChfjaXPihxGWpdkWacrWF9AWc-AyZY
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: c96d2aa5-76a2-443d-8d23-5de95577c909
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: cbcb1cb0abbb8d4c6ea173c4deff071d0081da4e
workflow-type: tm+mt
source-wordcount: 389
ht-degree: 95%

---

# 푸시 알림 시작 {#gs-push-notification}

>[!BEGINSHADEBOX]

**이 페이지의 내용:** Adobe Journey Optimizer에서 푸시 알림을 시작하여 여정과 캠페인을 통해 모바일 앱 사용자 및 웹 방문자에게 도달합니다.

>[!ENDSHADEBOX]

>[!IMPORTANT]
>
>[푸시 알림]을 처음 만드는 경우 [푸시] 채널 구성을 완료했는지 확인해야 합니다. [자세히 알아보기](push-gs.md)

푸시 알림을 통해 모바일 앱 사용자와 웹 방문자에게 언제든지 연락할 수 있습니다. 특히 해당 사용자가 활발하게 사용자의 앱을 사용하거나 웹사이트를 탐색하고 있지 않을 때 유용합니다. 푸시 알림은 서비스 업데이트 제공, 사용자 행동 요청, 새로운 프로모션 알림 등 다양한 사용 사례를 달성하는 데 도움이 될 수 있습니다. 장치 플랫폼에 따라 최종 사용자가 알림을 수신하거나 확인하려면 옵트인을 해야 합니다. 사용자 옵트인은 앱을 설치한 후 처음 시작할 때 바로 받거나, 필요에 따라 후속 세션이나 워크플로를 통해 받을 수 있습니다.

[!DNL Journey Optimizer]는 푸시 알림을 지원하며 업계 최고 수준의 처리 속도로 적절한 알림을 보내는 데 도움이 됩니다. 푸시 알림에는 브랜드의 [!DNL Adobe CX Enterprise]에 대한 데이터 인사이트를 활용하기 위한 개인화 및 여정 기반 컨텍스트가 포함될 수 있습니다.

푸시 알림은 다음 방법으로 만들 수 있습니다.

* **여정**&#x200B;에서 만들기: 여정에 [푸시] 활동을 추가하고 기본 설정을 정의한 다음 오른쪽의 **[!UICONTROL 작업: 푸시]** 창에서 [푸시 알림]의 내용을 작성합니다. [여정 만드는 방법 알아보기](../building-journeys/journey-gs.md)

* **캠페인**&#x200B;에서: 캠페인을 만든 후 [푸시 알림]을 작업으로 선택하고 기본 설정을 정의합니다. [액션 캠페인](../campaigns/campaign-action.md#action-campaign-action) | [API 트리거 캠페인](../campaigns/api-triggered-campaigns.md) | [오케스트레이션된 캠페인](../orchestrated/create-orchestrated-campaign.md#create) 만드는 방법 알아보기

전용 탭을 사용하여 **iOS**, **Android**, **웹** 플랫폼의 푸시 알림 설정을 정의합니다.

>[!NOTE]
>
>**[!DNL Journey Optimizer]**&#x200B;는 이메일 및 SMS 메시지에서 옵트아웃을 관리하는 방법을 제공하지만, 푸시 알림은 수신자가 디바이스를 통해 직접 구독을 취소할 수 있으므로 별도의 작업이 필요하지 않습니다. 예를 들어, 앱을 다운로드하거나 사용하는 경우 알림을 중지하도록 선택할 수 있습니다. 마찬가지로 수신자는 모바일 운영 체제나 웹 브라우저 설정을 통해 알림 설정을 변경할 수 있습니다. AEP 프로필 뷰어에서 프로필의 푸시 동의 상태를 확인하려면 [푸시 옵트아웃 상태 확인](../privacy/opt-out.md#push-opt-out-status)을 참조하세요.

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="create-push.md">
<img alt="리드" src="../assets/do-not-localize/push-create.jpg">
</a>
<div><a href="create-push.md"><strong>푸시 알림 만들기</strong>
</div>
<p>
</td>
<td>
<a href="design-push.md">
<img alt="저빈도" src="../assets/do-not-localize/push-design.jpg">
</a>
<div>
<a href="design-push.md"><strong>푸시 알림 디자인</strong></a>
</div>
<p></td>
<td>
<a href="send-push.md">
<img alt="유효성 검사" src="../assets/do-not-localize/push-sending.jpg">
</a>
<div>
<a href="send-push.md"><strong>푸시 알림 보내기</strong></a>
</div>
<p>
</td>
<td>
<a href="push-gs.md">
<img alt="유효성 검사" src="../assets/do-not-localize/push-config.jpg">
</a>
<div>
<a href="push-gs.md"><strong>푸시 알림 구성</strong></a>
</div>
<p>
</td>
</tr></table>
