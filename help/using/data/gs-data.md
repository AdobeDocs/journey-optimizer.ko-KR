---
solution: Journey Optimizer
product: journey optimizer
title: 에서 데이터 시작 [!DNL Journey Optimizer]
description: 에서 데이터를 사용하여 작업하는 방법 알아보기 [!DNL Journey Optimizer]
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 25519acb-a017-446a-992b-653d3a8a3d96
source-git-commit: 2dcfcc8d7006c92e046152db5ac1288bdde8b063
workflow-type: tm+mt
source-wordcount: '891'
ht-degree: 0%

---

# 에서 데이터 관리 시작 [!DNL Journey Optimizer] {#about-data}

최종 고객 데이터의 풍부성과 범위는 모든 고객 경험 솔루션의 강점과 성공을 정의하는 것입니다. 또한 이 데이터는 신성하며 해당 고객에게 가장 높은 가치를 갖습니다. 기술 선택은 기본적으로 데이터 관리 기능에 대한 엄격한 평가를 통해 이루어집니다.

Adobe Journey Optimizer을 사용하면 이 데이터를 쉽게 관리, 유지 및 기술 스택에 포함된 플랫폼 또는 시스템으로 내보낼 수 있습니다.

**내 데이터, 내 규칙** - Journey Optimizer은 모든 여정 데이터 및 해당 작업에 고유한 오퍼 데이터 외에 지속적으로 다양한 고객 프로필 데이터 세트를 만듭니다(또한 실시간으로). 데이터베이스에서 수집된 사용자 데이터의 Strawman-version이 보강되어 적용 범위뿐만 아니라 깊이가 높은 고부가가치 데이터로 변환됩니다. 이 데이터를 안전하게 보호하고 동시에 유비쿼터스(유비쿼터스형)로 활용하여 전체 IT 에코시스템에서 해당 가치를 활용할 수 있습니다.

데이터 유연성은 크게 세 가지 방식입니다.


<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <div><img alt="대상" src="assets/do-not-localize/dest.png" /> 
    <br>다른 대상에서 사용 가능 - Journey Optimizer은 고도로 개인화된 고객 경험을 위해 데이터를 시너지 효과를 내고 통합하지만 이 데이터를 활용하는 다른 방법을 모색하고 있지만, 전반적인 기술 환경에서 이 데이터를 다른 시스템으로 활용하려는 경우.
    <div>
     <a href="../start/ajo-integrations.md">자세히 알아보기</a></div>
    </div>
    <br>
  </td>
</tr>
  <td>
    <div><img alt="유지" src="assets/do-not-localize/retention.png" />  
    <br>지정된 기간 동안 보존됨 - 업계 또는 지역 규정(GDPR 또는 CCPA 등) 또는 내부 데이터 거버넌스 정책은 지속 시간이 얼마나 오래 또는 짧아야 Adobe Experience Platform Data Lake에서 데이터를 유지 또는 보관해야 하는지 설명합니다. <a href="../privacy/get-started-privacy.md">자세히 알아보기</a></div>
  </td>
</tr>
<tr style="border: 0;">
  <td>
    <div><img alt="정책" src="assets/do-not-localize/policy.png" /> 
    <br>합의된 타임라인 또는 정책을 기반으로 삭제 - 데이터 삭제는 데이터 보호의 중요한 측면이며 모든 데이터 거버넌스 프로세스의 주요 단계입니다. Journey Optimizer은 필요 이상으로 더 많은 데이터를 생성할 수 있습니다. 또한 유틸리티 또는 규정 때문에 데이터 세트에 필요한 기간 이후에 발생하는 사항을 최대한 고려하려고 합니다. 필요한 컨트롤은 지정된 시간에 데이터를 삭제하는 것입니다. <a href="https://experienceleague.adobe.com/docs/experience-platform/hygiene/ui/overview.html">Adobe Experience Platform 설명서에서 데이터 위생에 대해 자세히 알아보십시오</a></div>
  </td>
</tr>
</table>

Journey Optimizer이 구축된 Adobe Experience Platform은 참여 동안과 서비스 종료 시 가장 높은 수준의 데이터 제어 기능을 제공합니다. Journey Optimizer 내에서, Journey Optimizer으로 가져와지거나에 의해 생성된 데이터, 해당 데이터 및 해당 데이터가 전송되는 대상에 대한 거버넌스가 오버레이됩니다.

모든 데이터는 고객의 속성으로 간주되며 요청 시에만 유지, 암호화, 배포 또는 삭제할 수 있습니다. Adobe은 데이터에 대한 전혀 권한이 없는 필수적인 역할을 합니다.

Journey Optimizer의 데이터 유연성을 사용하여 데이터 보존, 보관 또는 삭제와 관련된 특정 요구 사항을 해결할 수 있습니다.

* **데이터 추출/내보내기**: 데이터 액세스 API를 통해 언제든지 벌칙이나 시간 지연 없이 소스 데이터 추출을 시작할 수 있습니다. 다음 [데이터 액세스 API](https://experienceleague.adobe.com/docs/experience-platform/data-access/api.html){target=&quot;_blank&quot;}에서는 Experience Platform 내에서 수집된 데이터 세트의 검색 기능 및 액세스 가능성에 중점을 둔 RESTful 인터페이스를 사용자에게 제공합니다. <!--In the future (on roadmap), you can use file-based destinations to export and migrate log data from Adobe Journey Optimizer. -->

   여정 또는 캠페인에 사용된 컨텐츠는 위에 언급된 API 또는 대상 방법을 통해 추출할 수 없습니다.

* **프로필 서비스 데이터 유지**: 프로필에 추가된 동작 및 시간 시리즈 데이터의 경우, 프로필 추가일부터 최대 30일 동안 또는 사용자가 선택한 대체 기간이 될 때까지 이 데이터를 유지하는 Journey Optimizer의 기본 설정을 사용하도록 선택할 수 있습니다. Adobe이 이 데이터를 보관하는 시간은 계약에 따라 다르며 조직의 데이터 보존 정책에 요약되어 있습니다.

   에서 경험 이벤트 만료에 대해 자세히 알아보십시오 [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/profile/event-expirations.html){target=&quot;_blank&quot;}.

* **제거 및 아카이빙 메커니즘**: Journey Optimizer에서 데이터 및 아카이브 제거를 자유롭게 정의하고 자동화하여 데이터 보존 정책을 자동화할 수 있습니다. 서로 다른 데이터 엔티티에 대해 서로 다른 에이징 전략을 정의할 수 있습니다. 오래된 데이터를 삭제하거나 보관하기 전에 자동으로 내보내도록 내보내기 메커니즘을 정의할 수도 있습니다.

   Adobe Experience Platform UI의 데이터 위생 작업 공간을 사용하면 소비자 ID 삭제 및 데이터 세트 만료 예약 등 다양한 데이터 위생 작업을 만들고 모니터링할 수 있습니다. 이 작업 공간은 보안 및 개인 정보 보호(Security &amp; Privacy Shield)와 Healthcare Shield로 제공됩니다. 추가 정보 [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/hygiene/ui/overview.html){target=&quot;_blank&quot;}.

* **데이터 레이크 및 삭제**: Data Lake에 저장된 고객 데이터는 Journey Optimizer에서 유지할 수 있습니다.

   * 7일 동안 고객 데이터를 프로필 서비스로 쉽게 온보딩할 수 있도록 했으며, 그 이후에는 영구적으로 삭제되거나,
   * 사용자가 삭제할 때까지


* **참여 종료/종료 시 데이터 추출**: 계약이 종료되면 데이터가 Adobe의 스토리지 공간에서 완전히 제거됩니다. 또한 계약을 종료하기 전에 전체 프로파일 추출을 가져올 수도 있습니다. 이 기능에 대한 추가 비용은 없습니다. 이 작업은 종료 시에만 수행되는 것이 아니라 언제든지 수행할 수 있습니다.

위의 방법은 계약 시작 시 Adobe이 사용자와 상호 동의하는 데이터 처리 계약(DPA)에 계약상으로 정의되고 자세히 설명되어 있습니다. Journey Optimizer을 포함한 Adobe 애플리케이션은 각 클라이언트의 데이터를 해당 클라이언트의 개인 데이터 자산으로 처리하는 원칙을 기반으로 설계되었습니다.
