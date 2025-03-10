---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer에서 데이터 관리 시작
description: Journey Optimizer의 데이터 작업 방법 알아보기
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 데이터, 관리, 플랫폼
exl-id: 25519acb-a017-446a-992b-653d3a8a3d96
source-git-commit: da46230b9a086743fea1052b57b48bf18b920abd
workflow-type: ht
source-wordcount: '655'
ht-degree: 100%

---

# 데이터 관리 시작 {#about-data}

최종 고객 데이터의 풍부성과 적용 범위야말로 모든 고객 경험 솔루션의 강력함과 성공을 결정하는 요소입니다. 이 데이터는 불가침의 영역이며, 어떤 고객에게든 최고의 가치를 가지고 있습니다. 이제 기술 선택에 처음부터 데이터 관리 기능에 대한 엄격한 평가가 기본적으로 제공됩니다.

[!DNL Adobe Journey Optimizer]에서는 이 데이터를 쉽게 관리하고 유지하며 기술 스택에 포함된 플랫폼 또는 시스템으로 내보낼 수 있습니다. 

**내 데이터, 내 규칙** - [!DNL Adobe Journey Optimizer] 작업에 기본적으로 포함되는 여정 데이터 및 오퍼 데이터 전체에 더해 풍부한 고객 프로필 데이터 세트를 지속적(이며 실시간)으로 만듭니다. 데이터베이스에서 수집한 Strawman 버전의 사용자 데이터를 보강하고 변환하여 심도 깊고 적용 범위가 넓은 고부가가치 데이터로 만듭니다. 이 데이터를 안전하게 보호하는 동시에 유비쿼터스화하면 전체 IT 생태계에서 그 가치를 최대한 활용할 수 있습니다.

크게 보면 데이터에 기대할 수 있는 유연성은 다음과 같습니다.


<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <div><img alt="대상" src="assets/do-not-localize/dest.png" /> 
    <br>다른 대상에서 사용 가능 - [!DNL Adobe Journey Optimizer]에서는 데이터를 시너지화하고 통합하여 초개인화된 고객 경험을 도모하는데, 사용자는 이 데이터를 사용자의 전체 기술 환경에 있는 다른 시스템에 통합하는 한편 이 데이터를 활용할 다른 방법을 모색하려 할 수 있습니다.
    <div>
     <a href="../integrations/ajo-integrations.md">자세히 알아보기</a></div>
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
    <br>합의된 타임라인 또는 정책을 기반으로 삭제 - 데이터 삭제는 데이터 보호의 중요한 측면이며 모든 데이터 거버넌스 프로세스의 핵심 단계입니다. [!DNL Adobe Journey Optimizer]에서는 필요 이상의 데이터를 만들 수도 있습니다. 또한 활용성 때문이든 규제 때문이든, 데이터 세트에 필요한 기간 이후에 발생하는 일을 중요하게 고려하는 것이 좋습니다. 이 경우 필요한 제어 권한은 언제든 특정 시점에 데이터를 삭제하는 것입니다. 
    </div>
      <div>
     <a href="../privacy/data-hygiene.md">자세히 알아보기</a></div>
    </div>
  </td>
</tr>
</table>

[!DNL Adobe Journey Optimizer]의 구축 기반인 [!DNL Adobe Experience Platform]에서는 사용자에게 최고 수준의 데이터 제어 권한을 제공하며, 이는 참여 기간뿐 아니라 참여가 끝난 이후에도 적용됩니다. [!DNL Journey Optimizer] 내에서는 [!DNL Journey Optimizer]에서 가져오거나 생성한 데이터와, 해당 데이터에 적용되는 거버넌스, 해당 데이터가 전송되는 대상에 대한 모든 권한이 사용자에게 있습니다.

모든 데이터는 고객의 소유물로 간주되며 사용자의 요청에 의해서만 유지, 암호화, 배포 또는 파기될 수 있습니다. Adobe는 데이터에 대한 권한이 전혀 없는 수탁자 역할을 합니다.

[!DNL Journey Optimizer]의 데이터 유연성을 활용하여 데이터 보존, 보관 또는 삭제와 관련된 특정 요구 사항을 충족할 수 있습니다.

* **데이터 추출/내보내기**: 언제든지 데이터 액세스 API를 통해 페널티나 시간 지연 없이 소스 데이터 추출을 시작할 수 있습니다. [데이터 액세스 API](https://experienceleague.adobe.com/docs/experience-platform/data-access/api.html?lang=ko){target="_blank"}는 사용자에게 [!DNL Adobe Experience Platform] 내에서 수집된 데이터 세트의 검색 및 액세스 용이성에 중점을 둔 RESTful 인터페이스를 제공합니다. <!--In the future (on roadmap), you can use file-based destinations to export and migrate log data from Adobe Journey Optimizer. -->

  단, 여정 또는 캠페인에 사용된 콘텐츠는 위에서 언급한 API 또는 대상 메서드를 통해 추출할 수 없습니다.

<!--
* **Profile Service Data Retention**: For Behavioral and Time series data appended to any Profile, you may choose to use Journey Optimizer's default setting of retaining this data for up to 91 days from the date of its addition to a Profile, or until an alternative time-period selected by the you. The time that Adobe keeps this data varies from contract to contract, and is outlined in an organization's data retention policy.

  Learn more about Experience Event expirations in [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/profile/event-expirations.html){target="_blank"}.
-->

* **제거 및 보관 메커니즘**: [!DNL Adobe Journey Optimizer]에서 데이터 삭제 및 보관 작업을 자유롭게 정의하고 자동화하여 데이터 보존 정책을 자동화할 수 있습니다. 다양한 데이터 엔터티에 대해 서로 다른 에이징 전략을 정의할 수 있습니다. 내보내기 메커니즘을 정의하여 오래된 데이터를 삭제하거나 보관 처리하기 전에 자동으로 내보낼 수도 있습니다.

  데이터 수명주기 작업 영역에서는 소비자 ID 삭제와 데이터 세트 만료 일정 예약 등 다양한 데이터 수명주기 작업을 만들고 모니터링할 수 있습니다. 이 작업 영역은 Security &amp; Privacy Shield 및 Healthcare Shield를 통해 사용할 수 있습니다. [이 페이지](../privacy/data-hygiene.md)에서 자세히 알아보십시오.

<!--
* **Data Lake and Deletions**: Customer Data stored in the Data Lake can be retained by Journey Optimizer:
    
    * for 7 days to facilitate the onboarding of Customer Data into the Profile Services, after which it may be permanently deleted, or
    * until chosen to be deleted by you

-->

* **참여 종료/중도 파기 시 데이터 추출**: 계약이 종료되면 Adobe의 스토리지 공간에서 사용자의 데이터가 완전히 제거됩니다. 또한 계약을 종료하기 전에 전체 프로필을 추출하여 가져올 수도 있습니다. 이 기능에는 추가 비용이 들지 않습니다. 또한 이 작업은 계약이 종료될 때뿐 아니라 언제든지 수행할 수 있습니다.

위의 방법은 계약상으로 정의되며 DPA(데이터 처리 계약)에서 계약 시작 시 Adobe가 사용자와 상호 동의하는 것으로 자세히 설명되어 있습니다. [!DNL Journey Optimizer]를 포함한 Adobe 애플리케이션은 각 고객의 데이터가 해당 고객이 소유한 데이터 자산으로 처리된다는 원칙을 기반으로 설계됩니다.
