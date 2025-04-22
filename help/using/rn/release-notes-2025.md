---
solution: Journey Optimizer
product: journey optimizer
title: 2025년 릴리스 정보
description: Journey Optimizer 2025 릴리스 노트
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: aa8c74de-748b-4947-a972-14703f6ab4a7
source-git-commit: 9d87d133bb580ebed94a265beded5895f7fd0301
workflow-type: tm+mt
source-wordcount: '674'
ht-degree: 91%

---

# 2025년 릴리스 정보 {#release-notes-2025}

이 페이지에는 2025년에 릴리스된 [!DNL Journey Optimizer]의 모든 기능과 개선 사항이 나와 있습니다.

## 2025년 2월 릴리스 정보 {#25-02-rn}

**릴리스 날짜**: 2026년 2월 18~19일


### 새로운 기능 {#25-02-features}

이번 릴리스의 새로운 기능을 아래에서 자세히 설명합니다.

<table>
<thead>
<tr>
<th><strong>비즈니스 규칙 만들기 및 관리</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 규칙 세트를 사용하여 비즈니스 규칙을 만들 수 있습니다. 규칙 세트는 캠페인 내에서 보내는 메시지와 채널 간 여정 작업을 제한하고 프로필의 여정 진입을 제어하는 데 도움이 되는 규칙 그룹입니다.<p>
<p><ul><li>채널 규칙 세트를 만들어 한 채널 또는 여러 채널에서 전송되는 메시지 수를 제한합니다. 캠페인 또는 여정 작업에 적용하여 규칙 세트에 정의된 규칙을 시행합니다. 채널 규칙 세트를 사용하면 커뮤니케이션 유형에 따른 캡핑 규칙을 적용할 수 있습니다. 예를 들어 "프로모션 메시지"를 제한하는 규칙 세트를 설정하고 "뉴스레터"에 대해 또 다른 규칙 세트를 설정할 수 있습니다. 보내는 커뮤니케이션 유형에 따라 캠페인 또는 여정 작업에 적절한 규칙 세트를 적용합니다.</li>
<li> 프로필의 여정 진입을 제어하려면 여정 규칙 세트를 만듭니다. 프로필이 지정된 기간 내에 여정에 진입할 수 있는 빈도 또는 프로필을 동시에 등록할 수 있는 여정 수를 제한합니다. 여정 수준에서 이를 적용하여 적절한 진입 관리를 보장합니다.</li></ul></p>
<p>이전에는 일부 조직에서만 사용할 수 있던(LA) 비즈니스 규칙을 이제 모든 사용자가 사용할 수 있습니다(GA). 여정 도메인 비즈니스 규칙은 여전히 제한된 일부 조직에서만 사용할 수 있습니다(LA).</p>
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
<p>이제 AI Assistant를 사용하여 전체 페이지 디자인, 개인화된 텍스트 및 맞춤화된 시각 자료 등 랜딩 페이지에 대한 매력적인 콘텐츠를 제작할 수 있습니다.</p>
<img src="assets/do-not-localize/ai-lp.gif">
<p>자세한 내용은 <a href="../content-management/generative-lp.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>AI Assistant가 있는 브랜드(Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 고유한 브랜드를 설정하여 브랜드의 시각적 및 언어적 정체성을 정의할 수 있습니다. </p>
<p>이 기능은 제한된 수의 고객을 위한 Private Beta로 출시됩니다. 향후 릴리스에서 점진적으로 사용 범위를 확대하여 모든 고객에게 제공할 예정입니다.</p>
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
<p>이제 Adobe Journey Optimizer에서 직접 실제 API 호출을 수행하여 사용자 정의 액션 구성의 유효성을 검사할 수 있습니다. 이 새로운 기능은 여정에서 사용자 정의 작업을 사용하기 전이나 후에 문제를 해결하는 데 도움이 됩니다. </p>
<p>자세한 내용은 <a href="../action/troubleshoot-custom-action.md">세부 설명서</a>를 참조하십시오.</p>
<!--p> This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>유연한 대상자 평가(제한된 가용성)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>유연한 대상자 평가를 사용하면 선택한 대상자에 대해 온디맨드로 세분화 작업을 실행할 수 있어 대상자를 Journey Optimizer 여정 및 캠페인으로 타기팅하기 전에 항상 최신 대상자 데이터를 보유할 수 있습니다.</p>
<img src="assets/do-not-localize/flexible-audience.gif">
<p>자세한 내용은 <a href="../audience/creating-a-segment-definition.md#flexible">세부 설명서</a>를 참조하십시오.</p>
<p>이 기능은 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.</p>
<p>사용 가능한 날짜: 2025년 1월 28일</p>
</tr>
</tbody>
</table>
</table>


### 개선 사항 {#25-02-improvements}

2월 업데이트에서는 아래의 개선 사항이 제공됩니다.

* **데이터 세트 TTL(Time-to-Live)** - 이번 달부터 새로운 샌드박스와 새로운 조직에서 Journey Optimizer 시스템 생성 데이터 세트에 TTL(Time-to-Live) 가드레일이 다음과 같이 롤아웃됩니다.

   * 프로필 스토어의 데이터에 대해 90일
   * 데이터 레이크의 데이터에 대해 13개월

  이 변경 사항은 차후 기존 고객 샌드박스에 대해서도 롤아웃됩니다. 

  [해당 FAQ](../data/datasets-ttl.md#frequently-asked-questions)에서 이 업데이트에 대해 자세히 알아보세요.

<!--* **Playbooks** - You can now create and publish your own Use Case Playbooks in Journey Optimizer.-->

* **다이렉트 메일** - 이제 다이렉트 메일 채널 구성에서 파일 라우팅에 대해 새로운 서버 유형인 데이터 랜딩 구역이 지원됩니다. [자세히 보기](../direct-mail/direct-mail-configuration.md#file-routing-configuration)

* **SMS** - 이제 게재, 피드백, 인바운드 및 콜백 URL을 재정의하여 다중 지역 엔드포인트의 SMS 메시지 게재를 관리할 수 있습니다. 이를 지원하기 위해 새 필드인 재정의 URL이 API 자격 증명 구성에 추가되었습니다. 이 변경 사항은 Sinch 공급자에서만 사용할 수 있습니다. [자세히 보기](../sms/sms-configuration-sinch.md)

* **개인화**(사용 가능한 날짜: 2025년 1월 29일) - 새로운 날짜/시간 도우미 함수를 개인화 편집기에서 사용할 수 있습니다. [자세히 보기](../personalization/functions/dates.md)


<!--
* The personalization editor has been enhanced with new capabilities such as Auto-complete, Search, and filtering options. You can also show or hide deprecated attributes.-->


* **이메일 구성** - Adobe 외부에서 동의를 관리하는 경우 이제 이메일 채널 구성 설정의 일부로 사용자 정의 구독 취소 이메일 주소와 사용자 정의 원클릭 구독 취소 URL을 설정할 수 있습니다. [자세히 보기](../email/list-unsubscribe.md#custom-managed)

  ![](../email/assets/surface-list-unsubscribe-custom.png){width="80%"}

* **의사 결정**(사용 가능한 날짜: 2025년 1월 28일) - 이제 의사 결정에서 항목 카탈로그의 스키마를 편집할 때 오브젝트 데이터 형식을 지원합니다. [자세히 보기](../experience-decisioning/catalogs.md)
