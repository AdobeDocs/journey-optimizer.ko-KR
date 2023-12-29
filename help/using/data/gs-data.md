---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer에서 데이터 시작
description: Journey Optimizer에서 데이터를 사용하여 작업하는 방법을 알아봅니다.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 데이터, 관리, 플랫폼
exl-id: 25519acb-a017-446a-992b-653d3a8a3d96
source-git-commit: ef34cb0207d3011eca6d76ad6568f3edc00e13a3
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 1%

---

# 에서 데이터 관리 시작 [!DNL Journey Optimizer] {#about-data}

최종 고객 데이터의 풍부성과 적용 범위는 고객 경험 솔루션의 강점과 성공을 정의하는 것입니다. 이 데이터는 신성하며 주어진 고객에게 가장 높은 가치를 제공합니다. 기술 선택은 이제 기본적으로 데이터 관리 기능에 대한 엄격한 평가와 함께 내장되어 있습니다.

포함 [!DNL Adobe Journey Optimizer]를 사용하면 이 데이터를 쉽게 관리하고 유지할 수 있으며 기술 스택에 포함된 플랫폼 또는 시스템으로 내보낼 수 있습니다.

**내 데이터, 내 규칙** - [!DNL Adobe Journey Optimizer] 모든 여정 데이터와 해당 작업에 고유한 오퍼 데이터 외에도 다양한 고객 프로필 데이터 세트를 지속적으로(및 실시간으로) 만듭니다. 데이터베이스에서 수집된 스트로만 버전의 사용자 데이터는 보강되고 깊이 뿐만 아니라 적용 범위를 가진 고부가가치 데이터로 변환됩니다. 이러한 데이터를 안전하게 보호하면서 동시에 유비쿼터스하게 관리하여 전체 IT 생태계에서 그 가치를 최대한 활용할 수 있습니다.

데이터의 유연성은 광범위하게 다음과 같습니다.


<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <div><img alt="대상" src="assets/do-not-localize/dest.png" /> 
    <br>다른 대상에서 사용 - While [!DNL Adobe Journey Optimizer] 초개인화된 고객 경험을 위해 데이터를 시너지화하고 통합하므로 전체 기술 환경의 다른 시스템에 이 데이터를 사용하고, 이 데이터를 활용하는 다른 방법을 모색할 수 있습니다.
    <div>
     <a href="../start/ajo-integrations.md">자세히 알아보기</a></div>
    </div>
    <br>
  </td>
</tr>
</table>

<!--td>
    <div><img alt="retention" src="assets/do-not-localize/retention.png" />  
    <br>Retained for a stipulated duration – Industry or regional regulations (such as GDPR or CCPA) or internal data governance policies stipulate how long or how short a duration, data needs to be maintained or archived in Adobe Experience Platform Data Lake. <a href="../privacy/get-started-privacy.md">Learn more</a></div>
  </td>
</tr>
<tr style="border: 0;"-->
<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <div><img alt="정책" src="assets/do-not-localize/policy.png" /> 
    <br>합의된 타임라인 또는 정책을 기반으로 삭제 - 데이터 삭제는 데이터 보호의 중요한 측면이며 모든 데이터 거버넌스 프로세스의 핵심 단계입니다. [!DNL Adobe Journey Optimizer] 필요 이상의 데이터를 생성할 수 있습니다. 또한 유틸리티 또는 규제 때문에 데이터 세트에 필요한 기간 후에 발생하는 일을 최대한 주의해야 합니다. 필요한 컨트롤은 특정 시점에 데이터를 삭제하는 것입니다. 
    </div>
      <div>
     <a href="../privacy/data-hygiene.md">자세히 알아보기</a></div>
    </div>
  </td>
</tr>
</table>

[!DNL Adobe Experience Platform], [!DNL Adobe Journey Optimizer] 은 구축되어 있으며, 참여 도중과 참여 종료 시 사용자에게 최고 수준의 데이터 제어를 제공합니다. 다음 범위 내 [!DNL Journey Optimizer], 로 가져오거나 생성된 데이터에 대한 모든 권한이 있습니다. [!DNL Journey Optimizer]) 해당 데이터와 데이터가 전송되는 대상에 오버레이되는 거버넌스입니다.

모든 데이터는 Customers의 속성으로 간주되며 사용자의 요청에 의해서만 유지, 암호화, 배포 또는 파기될 수 있습니다. Adobe은 데이터에 대한 권한이 전혀 없는 수탁자 역할을 합니다.

다음을 사용할 수 있습니다. [!DNL Journey Optimizer]의 데이터 유연성으로 데이터 보존, 보관 또는 삭제와 관련된 특정 요구 사항을 충족할 수 있습니다.

* **데이터 추출/내보내기**: 데이터 액세스 API를 통해 언제든지 위약금이나 시간 지연 없이 소스 데이터 추출을 시작할 수 있습니다. 다음 [데이터 액세스 API](https://experienceleague.adobe.com/docs/experience-platform/data-access/api.html){target="_blank"} 는 내에서 수집된 데이터 세트의 검색 가능성과 액세스 가능성에 중점을 둔 RESTful 인터페이스를 사용자에게 제공합니다 [!DNL Adobe Experience Platform]. <!--In the future (on roadmap), you can use file-based destinations to export and migrate log data from Adobe Journey Optimizer. -->

  여정 또는 캠페인에 사용된 콘텐츠는 위에 언급된 API 또는 대상 메서드를 통해 추출할 수 없습니다.

<!--
* **Profile Service Data Retention**: For Behavioral and Time series data appended to any Profile, you may choose to use Journey Optimizer’s default setting of retaining this data for up to 30 days from the date of its addition to a Profile, or until an alternative time-period selected by the you. The time that Adobe keeps this data varies from contract to contract, and is outlined in an organization’s data retention policy.

  Learn more about Experience Event expirations in [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/profile/event-expirations.html){target="_blank"}.
-->

* **제거 및 아카이빙 메커니즘**: 데이터 삭제 및 아카이브 작업을 자유롭게 정의하고 자동화할 수 있습니다. [!DNL Adobe Journey Optimizer] 데이터 보존 정책을 자동화합니다. 서로 다른 데이터 엔티티에 대해 서로 다른 에이징 전략을 정의할 수 있습니다. 오래된 데이터를 삭제하거나 보관하기 전에 자동으로 내보내도록 내보내기 메커니즘을 정의할 수도 있습니다.

  데이터 위생 작업 영역을 사용하면 소비자 ID 삭제 및 데이터 세트 만료 일정 예약 등 다양한 데이터 위생 작업을 만들고 모니터링할 수 있습니다. 이 작업 영역은 Security &amp; Privacy Shield 및 Healthcare Shield에서 사용 가능합니다. [이 페이지](../privacy/data-hygiene.md)에서 자세히 알아보십시오.

<!--
* **Data Lake and Deletions**: Customer Data stored in the Data Lake can be retained by Journey Optimizer:
    
    * for 7 days to facilitate the onboarding of Customer Data into the Profile Services, after which it may be permanently deleted, or
    * until chosen to be deleted by you

-->

* **참여 종료/종료 시 데이터 추출**: 계약이 종료되면 Adobe의 저장 공간에서 데이터가 완전히 제거됩니다. 또한 계약을 종료하기 전에 전체 프로필 추출을 가져올 수 있습니다. 이 기능에 대한 추가 비용은 없습니다. 이는 종료 시에만 수행할 수 있는 것이 아니라 언제든지 수행할 수 있습니다.

위의 방법은 계약상으로 정의되며 DPA(데이터 처리 계약)에서 계약 시작 시 Adobe이 사용자와 상호 동의하는 것으로 자세히 설명되어 있습니다. Adobe 애플리케이션, [!DNL Journey Optimizer]는 각 클라이언트의 데이터가 클라이언트의 고유 데이터 자산으로 처리된다는 원칙을 기반으로 설계되었습니다.
