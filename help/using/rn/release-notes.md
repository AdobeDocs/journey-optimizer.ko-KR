---
solution: Journey Optimizer
product: journey optimizer
title: 릴리스 정보
feature: Release Notes
topic: Content Management
description: Adobe Journey Optimizer 릴리스 정보
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 6480bb7e35d92ba1771b3e5c01310ee93a8c77b1
workflow-type: tm+mt
source-wordcount: '746'
ht-degree: 27%

---

# 릴리스 정보 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="새로운 기능"
>abstract="**Adobe Journey Optimizer**&#x200B;는 지속적으로 새로운 기능, 기존 기능 개선, 버그 수정을 제공합니다. 모든 변경 사항은 매달 마지막 주에 여기 있는 릴리스 정보에 통합됩니다."

[!DNL Adobe Journey Optimizer]은(는) 지속적으로 새로운 기능, 기존 기능 개선, 버그 해결을 제공합니다. 모든 변경 사항은 매달 마지막 주 여기 있는 릴리스 정보에 통합됩니다. [!DNL Adobe Journey Optimizer]은 기본적으로 [!DNL Adobe Experience Platform] 기반으로 빌드되었으며 최신 혁신 및 향상된 기능을 활용할 수 있습니다. 변경 사항에 대한 자세한 내용은 [Adobe Experience Platform 릴리스 정보](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html){target="_blank"}를 참조하십시오.


## 2025년 2월 릴리스 정보 {#25-02-rn}

<!--
**Early release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published at the release date.-->

**릴리스 날짜**: 2025년 2월 18~19일


### 새로운 기능 {#25-02-features}

이번 릴리스의 새로운 기능은 아래에 자세히 설명되어 있습니다.

<table>
<thead>
<tr>
<th><strong>비즈니스 규칙 생성 및 관리</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 규칙 세트를 사용하여 비즈니스 규칙을 만들 수 있습니다. 규칙 세트는 캠페인 내의 보낸 메시지 및 채널 간 여정 작업을 제한하고 여정에 대한 프로필 항목을 제어하는 데 도움이 되는 규칙 그룹입니다.<p>
<p><ul><li>채널 규칙 세트를 만들어 하나 또는 여러 채널에서 전송되는 메시지 수를 제한합니다. 캠페인 또는 여정 작업에 적용하여 규칙 세트에 정의된 규칙을 적용합니다. 채널 규칙 세트를 사용하면 통신 유형에 따라 최대 가용량 규칙을 적용할 수 있습니다. 예를 들어 "프로모션 메시지"와 "뉴스레터"에 대한 다른 메시지를 제한하도록 규칙 세트를 설정합니다. 보내는 커뮤니케이션 유형에 따라 캠페인 또는 여정 작업에 적절한 규칙 세트를 적용합니다.</li>
<li> 프로필 항목을 여정으로 제어하려면 여정 규칙 세트를 만듭니다. 프로필이 지정된 기간 내에 여정을 입력할 수 있는 빈도 또는 프로필을 동시에 등록할 수 있는 여정 수를 제한합니다. 여정 수준에서 이를 적용하여 적절한 항목 관리를 보장합니다.</li></p>
<p>이전에는 조직 집합(LA)에서 사용할 수 있었으나, 이제 모든 사용자(GA)가 비즈니스 규칙을 사용할 수 있습니다.</p>
<p>자세한 내용은 <a href="../configuration/rule-sets.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>AI Assistant를 사용하여 랜딩 페이지 생성</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 AI 어시스턴트의 도움을 받아 전체 페이지 디자인, 개인화된 텍스트, 맞춤화된 시각 자료 등 랜딩 페이지에 사용할 매력적인 콘텐츠를 제작할 수 있습니다.</p>
<img src="assets/do-not-localize/ai-lp.gif">
<p>자세한 내용은 <a href="../content-management/generative-lp.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>AI Assistant를 사용하는 브랜드(Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 고유한 브랜드 를 설정하여 브랜드의 시각적 및 언어적 정체성을 정의할 수 있습니다. </p>
<p>이 기능은 제한된 고객 집합에 대한 비공개 베타로 출시됩니다. 향후 릴리스에서 모든 고객에게 점진적으로 제공될 예정입니다.</p>
<p>자세한 내용은 <a href="../content-management/brands.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>사용자 지정 작업 문제 해결</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Adobe Journey Optimizer에서 직접 실제 API를 호출하여 사용자 지정 작업 구성의 유효성을 검사할 수 있습니다. </p>
<p>자세한 내용은 <a href="../action/troubleshoot-custom-action.md">세부 설명서</a>를 참조하십시오.</p>
<!--p> This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>유연한 대상 평가(제한된 가용성)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>유연한 대상자 평가를 사용하면 선택한 대상자에 대해 온디맨드로 세분화 작업을 실행할 수 있어 대상자를 Journey Optimizer 여정 및 캠페인으로 타기팅하기 전에 항상 최신 대상자 데이터를 보유할 수 있습니다.</p>
<img src="assets/do-not-localize/flexible-audience.gif">
<p>자세한 내용은 <a href="../audience/creating-a-segment-definition.md#flexible">세부 설명서</a>를 참조하십시오.</p>
<p>이 기능은 조직 집합(제한된 가용성)에만 사용할 수 있습니다. 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.</p>
<p>사용 가능한 날짜: 2025년 1월 28일</p>
</tr>
</tbody>
</table>
</table>


### 개선 사항 {#25-02-improvements}

아래의 개선 사항은 2월 업데이트와 함께 제공됩니다.

* **여정** - 이제 관리 섹션에서 API 호출을 전송하여 사용자 지정 작업을 테스트할 수 있습니다. 이 새로운 기능은 여정에서 사용자 지정 작업을 사용하기 전이나 후에 문제를 해결하는 데 도움이 됩니다. [자세히 보기](../action/troubleshoot-custom-action.md)

* **TTL(Time-to-Live)** - 이번 달부터 TTL(Time-to-Live) 가드레일이 다음과 같이 새 샌드박스 및 새 조직의 Journey Optimizer 시스템 생성 데이터 세트로 롤아웃됩니다.

   * 프로필 스토어의 데이터에 대해 90일
   * 데이터 레이크의 데이터에 대해 13개월

  이 변경 사항은 후속 단계에서 기존 고객 샌드박스로 롤아웃됩니다.

  [전용 FAQ](../data/datasets-ttl.md#frequently-asked-questions)에서 이 업데이트에 대해 자세히 알아보세요.

<!--* **Playbooks** - You can now create and publish your own Use Case Playbooks in Journey Optimizer.-->

* **DM** - 이제 DM 채널 구성에서 파일 라우팅에 대해 새로운 서버 유형인 데이터 랜딩 영역이 지원됩니다. [자세히 보기](../direct-mail/direct-mail-configuration.md#file-routing-configuration)

* **SMS** - 이제 게재, 피드백, 인바운드 및 콜백 URL을 재정의하여 다중 지역 끝점의 SMS 메시지 게재를 관리할 수 있습니다. 이를 지원하기 위해 새 필드 Override URL이 API Credentials 구성에 추가되었습니다. 이 변경 사항은 Sinch 공급자에서만 사용할 수 있습니다. [자세히 보기](../sms/sms-configuration-sinch.md)

* **Personalization**(사용 가능한 날짜: 2025년 1월 29일) - 새 날짜/시간 도우미 함수를 개인화 편집기에서 사용할 수 있습니다. [자세히 보기](../personalization/functions/dates.md)


<!--
* The personalization editor has been enhanced with new capabilities such as Auto-complete, Search, and filtering options. You can also show or hide deprecated attributes.-->


* **이메일 구성** - Adobe 외부에서 동의를 관리하는 경우 이제 사용자 지정 구독 취소 이메일 주소와 사용자 지정 원클릭 구독 취소 URL을 이메일 채널 구성 설정의 일부로 설정할 수 있습니다. [자세히 읽기](../email/list-unsubscribe.md#custom-managed)

  ![](../email/assets/surface-list-unsubscribe-custom.png){width="80%"}

* **Decisioning**(사용 가능한 날짜: 2025년 1월 28일) - 이제 Decisioning에서 항목 카탈로그의 스키마를 편집할 때 개체 데이터 형식을 지원합니다. [자세히 보기](../experience-decisioning/catalogs.md)

