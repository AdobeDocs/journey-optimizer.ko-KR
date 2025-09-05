---
solution: Journey Optimizer
product: journey optimizer
title: 릴리스 정보
feature: Release Notes
topic: Content Management
description: Adobe Journey Optimizer 릴리스 정보
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 831db9b83f1b7011cdd26f957195592b06160837
workflow-type: tm+mt
source-wordcount: '2063'
ht-degree: 67%

---

# 릴리스 정보 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="새로운 기능"
>abstract="**Adobe Journey Optimizer**&#x200B;는 지속적으로 새로운 기능, 기존 기능 개선, 버그 수정을 제공합니다. 모든 변경 사항은 매달 마지막 주에 여기 있는 릴리스 정보에 통합됩니다."

[!DNL Adobe Journey Optimizer]은(는) 지속적으로 새로운 기능, 기존 기능 개선, 버그 해결을 제공합니다. 모든 변경 사항은 매달 마지막 주 여기 있는 릴리스 정보에 통합됩니다. [!DNL Adobe Journey Optimizer]은 기본적으로 [!DNL Adobe Experience Platform] 기반으로 빌드되었으며 최신 혁신 및 향상된 기능을 활용할 수 있습니다. 변경 사항에 대한 자세한 내용은 [Adobe Experience Platform 릴리스 정보](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=ko){target="_blank"}를 참조하십시오.

## 9월 25일 업데이트 {#sep-updates}

### 새로운 기능 {#Sep-25-features}

<table>
<thead>
<tr>
<th><strong>여정 경로 최적화</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>새로운 최적화 노드를 사용하여 특정 대상자를 타기팅하거나 A/B 테스트를 실행하여 비즈니스 중심 KPI를 충족하는 최상의 경로를 결정합니다.</p>
<p>이 도구를 사용하여 테스트 및 변경을 수행하고 커뮤니케이션, 시퀀스, 타이밍을 사용자 정의하여 고객에게 가장 효과적으로 다가갈 수 있습니다.</p>
<p>이 기능은 제한적으로 이용할 수 있습니다. 액세스 권한을 얻으려면 Adobe 담당자에게 문의하십시오.</p>
<p><img src="assets/do-not-localize/optimize.gif"/></p>
<p>자세한 내용은 <a href="../building-journeys/optimize.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2025년 9월 4일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>하위 도메인에 대한 사용자 정의 위임 방법</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 전체 위임과 CNAME 방법 외에 새로운 하위 도메인 구성 방법인 사용자 정의 위임 방법을 사용할 수 있습니다. 이 방법을 사용하면 메시지 게재, 렌더링, 추적에 필요한 DNS의 모든 측면을 사용자가 완전히 제어하고 유지 관리할 수 있습니다.</p>
<p>이 기능은 제한적으로 이용할 수 있습니다. 액세스 권한을 얻으려면 Adobe 담당자에게 문의하십시오.</p>
<p>자세한 내용은 <a href="../configuration/delegate-custom-subdomain.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2025년 9월 4일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>개인화 및 의사 결정에 Adobe Experience Platform 데이터 사용 - 제한된 가용성</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이전에 공개 베타로 출시된 이 기능은 이제 제한된 가용성의 모든 환경에서 사용할 수 있습니다. 이번 릴리스에서는 다음과 같은 개선 사항이 도입되었습니다.</p>
<ul><li>인바운드 채널에서 데이터 세트 조회 개인화를 지원합니다.</li>
<li>이제 "datasetLookup" 도우미 함수를 표현식 조각 내에서 사용할 수 있습니다.</li>
<li>이제 데이터 세트 관리 인터페이스의 옵션을 통해 API 호출을 수행하지 않고도 조회 개인화에 대해 레코드 기반 데이터 세트를 활성화할 수 있습니다.</li>
<li>데이터 수집 상태를 추적하고 데이터 세트를 조회할 준비가 되었는지 알 수 있도록 모니터링을 개선했습니다.</li>
<li>최적의 성능과 안정성을 보장하기 위해 사용 지침 및 보호 기능을 업데이트했습니다.</li>
<li>이제 의사 결정 최대 가용량 규칙에서 Adobe Experience Platform 데이터 세트를 활용할 수 있습니다.</li></ul></p>
<p>자세한 내용은 <a href="../data/lookup-aep-data.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2025년 9월 1일</p>
</td>
</tr>
</tbody>
</table>

### 개선 사항 {#Sep-25-improv}

* **의사 결정 최대 가용량 규칙에 대한 식** - 이제 의사 결정 항목에 대한 최대 가용량 규칙의 임계값을 정의하기 위해 자체 식을 만들 수 있습니다. [자세히 보기](../experience-decisioning/items.md#capping)

  >[!NOTE]
  >
  >이 기능은 현재 모든 사용자에게 제한된 가용성으로 제공됩니다.

* **관리**

  **채널 구성 모니터링 경고** - 이제 사용자 지정 하위 도메인 위임 유형을 사용하는 이메일 채널 구성 오류가 발생하는 경우 이메일 또는 Journey Optimizer 알림 센터에서 시스템 경고를 수신하도록 구독할 수 있습니다. [자세히 보기](../reports/alerts.md#alert-dns-record-missing)

## 2025년 8월 릴리스 정보 {#25-8-rn}

**릴리스 일자**: 2025년 8월 19일

### 새로운 기능 {#Aug-25-8-features}

이번 릴리스의 새로운 기능을 아래에서 자세히 설명합니다.

<table>
<thead>
<tr>
<th><strong>여정 일시 중단 및 다시 시작</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 여정을 일시 중단했다가 다시 시작할 수 있습니다. 이 기능을 사용하면 고객 경험을 중단하지 않고 라이브 여정을 일시적으로 중단할 수 있으므로 여정 실무자가 여정을 보다 자유롭게 제어하고 유연하게 조정할 수 있습니다. 일시 중단하면 커뮤니케이션이 전송되지 않으며 프로필은 여정이 다시 시작될 때까지 보류 상태로 유지됩니다.</p>
<p>하나의 여정만 일시 중단했다가 다시 시작하거나, 여정 그룹에 일괄 일시 중단 및 다시 시작 작업을 수행할 수 있습니다.</p>
<p>또한 일시 중단된 프로필에 전역 필터를 적용하여 속성에 따라 프로필을 제외할 수 있습니다.</p>
<p><img src="assets/do-not-localize/PauseResume.gif"/></p>
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).</p>
<p>자세한 내용은 <a href="../building-journeys/journey-pause.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>캘린더 보기</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 여정 및 캠페인 목록에서 캘린더 보기를 사용할 수 있습니다. 이를 통해 각 목록에 있는 모든 여정 및 캠페인의 활성화를 시각화할 수 있습니다.</p>
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다. 이번 GA 릴리스에서는 다음과 같은 기능이 제공됩니다.</p>
<ul>
<li>날짜 내 탐색에 대한 디자인 개선 사항</li>
<li>시작 및 종료 날짜를 설정한 경우 초안 캠페인을 볼 수 있는 기능</li>
<li>오래 실행되는 일정 항목을 숨기거나 표시하는 새로운 설정</li>
</ul>
<p><img src="assets/do-not-localize/calendar.gif"/></p>
<p>자세한 내용은 <a href="../building-journeys/journey-ui.md#calendar">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Dark mode in the Email Designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The Journey Optimizer Email Designer now offers the ability to switch to dark mode view, where you can additionally define specific custom settings that will display only for recipients reading their emails in dark mode.</p>
<p>Note the following:</p>
<ul>
<li>The dark mode final rendering may vary and depends on the recipient's email client.</li>
<li>Not all email clients support custom dark mode. Moreover, some email clients only apply their own default dark mode for all emails that are received. In both cases, the custom settings that you defined in the Email Designer cannot be rendered.</li>
</ul>
<P>This capability is currently in beta version and only available to beta customers. To join the beta program, contact your Adobe representative.</p>
<p><img src="assets/do-not-localize/dark-mode.gif"/></p>
<p>For more information, refer to the <a href="../email/dark-mode.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Use Adobe Experience Platform data for personalization</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Leverage data from [!DNL Adobe Experience Platform] in the personalization editor to personalize your content and decision attributes. In particular, this allows you to extend the definition of your attributes to additional data in datasets for bulk updates that change periodically without having to manually update the attributes one at a time.</p>
<p>With this release, the following enhancements have been introduced:</p>
<ul>
<li>Support of inbound channels,</li>
<li>The "datasetLookup" helper function can now be used within expression and visual fragments to personalize content using data from Adobe Experience Platform datasets,</li>
<li>An option in the dataset now allows you to enable datasets for lookup personalization, without having to perform an API call.</li>
</ul>
<p>This capability is available in Limited Availability. Contact your Adobe representative to gain access.</p>
<p>For more information, refer to the <a href="../personalization/aep-data-perso.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Use Decisioning in email channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add Decision policies into email journeys and campaigns. Decision policies are containers for your offers that leverage the Decisioning engine to dynamically return the best content to deliver for each audience member.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p><img src="assets/do-not-localize/FILE.gif"/></p>
<p><For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>여정의 액션 활동</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer가 단일 액션과 여러 액션이 있는 인바운드 액션 그룹을 모두 구성할 수 있는 포괄적 액션 활동을 새롭게 지원하여 여정 캔버스 내 액션 구성을 간소화할 수 있습니다. 특히 이 새로운 기능에는 다음과 같은 이점이 있습니다.</p>
<ul>
<li>여정 캔버스 내 기본 액션 구성 간소화.</li>
<li>여러 작업 인바운드 작업 그룹을 만들 수 있는 용량입니다.</li>
<li>모든 기본 제공 채널 액션에 최적화를 더하는 기능.</li>
<li>모든 액션에 실험과 다국어 옵션을 모두 추가하는 기능.</li>
</ul>
<p>이 기능은 제한적으로 이용할 수 있습니다. 액세스 권한을 얻으려면 Adobe 담당자에게 문의하십시오.</p>
<p><img src="assets/do-not-localize/action-activity.gif"/></p>
<p>자세한 내용은 <a href="../building-journeys/journey-action.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>이메일에 PDF 파일 첨부</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer로 보내는 이메일 메시지에 정적 PDF 파일을 첨부할 수 있습니다.</p>
<ul>
<li>매년 프로필별로 최대 6개의 PDF 첨부 파일을 사용하여 메시지를 보낼 수 있습니다.</li>
<li>각 첨부 파일의 최대 크기는 5MB입니다.</li>
<li>크기나 볼륨이 더 필요하다면 첨부 파일 팩 추가 기능을 구매할 수 있습니다. 자세한 내용은 Adobe 담당자에게 문의하십시오.</li>
</ul>
<p>이 기능은 제한적으로 이용할 수 있습니다. 액세스 권한을 얻으려면 Adobe 담당자에게 문의하십시오.</p>
<p><img src="assets/do-not-localize/pdf-attachments.gif"/></p>
<p>자세한 내용은 <a href="../email/pdf-attachments.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Landing page custom forms</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>With [!DNL Journey Optimizer], you can now capture profile attributes though your landing pages.</p>
<p>Create, design and manage custom forms tailored to your needs based on a specific dataset. You can then leverage these forms in landing pages to add the profile attributes of your choice into the dataset defined for each form.</p>
<p>This capability is currently in beta version and only available to beta customers. To join the beta program, contact your Adobe representative.</p>
<p><img src="assets/do-not-localize/forms.gif"/></p>
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>캠페인의 최적화</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer은 대상자에게 개인화되고 최적화된 콘텐츠를 전달하는 도구를 제공하므로 콘텐츠 실험을 실행하고, 규칙 기반 타기팅을 만들고, 두 방법의 고급 조합을 사용하여 캠페인과 여정의 효과를 극대화할 수 있습니다.</p>
<p>최적화를 사용하면 다음을 할 수 있습니다.</p>
<ul>
<li>여러 콘텐츠 변형을 테스트하여 가장 효과적인 메시징을 식별합니다.</li>
<li>사용자 특성 및 컨텍스트 데이터를 기반으로 개인화된 콘텐츠를 제공합니다.</li>
<li>고급 전략에 대한 타깃팅과 실험을 결합합니다.</li>
<li>변형 기준과 일치하지 않는 사용자를 필터링합니다.</li>
<li>사용자 참여를 유지하기 위한 대체 메커니즘을 확인하십시오.</li>
</ul>
<P>여정 또는 캠페인이 라이브되면 정의된 기준에 따라 프로필이 평가되고, 일치하는 기준을 기반으로 적절한 경험 또는 콘텐츠와 함께 전달됩니다.</p>
<p><img src="assets/do-not-localize/campaign-optimization.gif"/></p>
<p>이전에 캠페인에서만 8월 8일에 릴리스된 이 용량은 이제 8월 22일부터 여정에서도 사용할 수 있습니다.</p>
<p>자세한 내용은 <a href="../campaigns/campaigns-message-optimization.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>

### 개선 사항 {#Aug-25-8-improv}

다음은 이번 릴리스의 개선 사항 목록입니다.

* **관리**

   * **채널 구성 모니터링 경고** - 이제 <!--a channel configuration failure happens or if -->DNS 레코드가 누락된 경우 시스템 경고를 전자 메일 또는 Journey Optimizer 알림 센터에서 수신하도록 구독할 수 있습니다. [자세히 보기](../reports/alerts.md#alert-dns-record-missing)

* **AI 어시스턴트**

   * **여러 언어로 콘텐츠 생성** - 이제 프랑스어, 스페인어, 독일어, 이탈리아어, 일본어, 스웨덴어, 네덜란드어 및 노르웨이어로 콘텐츠를 생성할 수 있습니다. [자세히 보기](../content-management/generative-uc.md#languages)

     사용 가능한 날짜: 8월 25일


* **캠페인**

   * **아웃바운드 캠페인의 비율 제어** - 이제 아웃바운드 캠페인(이메일, SMS, 푸시 알림)에 대한 비율 제어를 사용하도록 설정하여 랜딩 페이지나 고객 지원 플랫폼과 같은 다운스트림 시스템에서 오버로드를 방지할 수 있습니다. [자세히 보기](../campaigns/campaign-schedule.md#rate-control)

   * **액션 캠페인 예약** - 되풀이 일정을 보다 세부적으로 제어하는 기능을 제공하기 위해 캠페인 일별, 주별, 월별 스케줄러를 업데이트했습니다. 

      * **주별 반복**: 이제 캠페인 반복 주기를 매주 또는 격주 중 선택하고 실행할 요일도 선택할 수 있습니다.

      * **월별 반복**: 이제 캠페인 반복 주기를 매월 또는 격월 중 선택하고 실행할 날짜도 선택할 수 있습니다.

      * **일별, 주별 또는 월별 일정**: 되풀이 일정을 특정 날짜에 중지할지 또는 특정 실행 횟수 이후에 중지할지 지정할 수 있습니다.

   * **예약된 트랜잭션 액션 캠페인** - 이제 예약된 트랜잭션 액션 캠페인으로 이메일, SMS, 푸시 채널을 통해 대상자 기반 배치 트랜잭션 커뮤니케이션을 보낼 수 있습니다.

* **채널 - 콘텐츠 카드**

   * **콘텐츠 카드 레이아웃 템플릿** - 이제 콘텐츠 카드 채널은 작성 환경을 간소화하는 OOTB 메시지 레이아웃을 제공합니다. 이 릴리스에는 작은 이미지, 큰 이미지 및 이미지 전용 레이아웃 템플릿이 포함됩니다. [자세히 보기](../content-card/design-content-card.md)

* **채널 - 푸시**

   * **푸시 알림 만료일** - 이제 각 푸시 알림에 대해 만료일을 지정할 수 있습니다. 이 기능으로 시간에 민감한 메시지(예: 블랙 프라이데이 세일)가 특정 날짜 이후에 전송되지 않도록 설정해 고객에게 좋지 않은 경험을 전하는 것을 방지할 수 있습니다.

* **채널 - SMS**

   * **퍼지 옵트아웃** - **퍼지 옵트아웃** 옵션을 활성화하면 정의된 옵트아웃 키워드(예: &#39;CANCIL&#39;)와 유사한 인바운드 메시지를 감지하고 자동으로 확인 응답을 보내 사용자의 구독 취소 의도를 확인합니다. 사용자가 정의된 프롬프트를 통해 확인하는 경우 가입을 취소합니다. [자세히 보기](../sms/sms-configuration-sinch.md)

     >[!NOTE]
     >
     >**퍼지 옵트아웃**&#x200B;은(는) Sinch 및 Infobip에서만 사용할 수 있습니다.

   * **SMS 연결 확인** - 이제 샘플 메시지를 지정된 장치로 전송하여 Adobe Journey Optimizer 내에서 SMS API 자격 증명을 쉽게 테스트하고 확인할 수 있습니다. [자세히 보기](../sms/sms-configuration-sinch.md)

* **구성**

  &lt;!—* **동적 도메인 지원** - 이제 Journey Optimizer에서 Adobe에서 허용하는 사전 정의된 도메인에 대한 전체/기본 URL 개인화를 지원합니다. 이 기능은 일부 고객에게는 제한된 가용성으로 제공됩니다. [자세히 읽기](../personalization/personalization-build-expressions.md#where)—8월 21일 업데이트: eng 대기 중 프로덕션에 배포 시기를 확인하려면 다음을 수행하십시오.—>

   * **원클릭 구독 취소 URL에 사용자 정의 특성 지원** - Journey Optimizer를 사용할 때 Adobe 외부에서 동의를 관리하는 경우 이메일 구성에서 원클릭 구독 취소 링크를 정의하여 외부 사용자 정의 엔드포인트를 설정할 수 있습니다. 수신자가 구독 취소 링크를 클릭하면 Journey Optimizer는 기본 프로필별 매개 변수 몇 가지를 동의 업데이트 이벤트에 추가합니다.

     이제 원클릭 구독 취소 링크를 개인화하기 위해 동의 이벤트에도 추가될 사용자 지정 속성을 정의할 수 있습니다. [자세히 보기](../email/list-unsubscribe.md#custom-attributes)

* **데이터 세트**

   * **Experience Decisioning 개체 저장소 - 개인화된 오퍼 항목** - 이제 기본 제공 내보내기 데이터 세트가 모든 오퍼 특성 및 라이프사이클 상태를 캡처하여 완벽한 개인화 및 보고를 가능하게 합니다. [자세히 보기](../data/export-datasets.md)

   * 일관성을 개선하고 변경 내용을 추적하여 오퍼 항목을 보다 안정적으로 제공하기 위해 `etag` 필드를 통해 버전 검사를 도입했습니다.

* **의사 결정**

   * **의사 결정 항목에 조각 첨부** - 이제 Journey Optimizer에서 의사 결정 정책을 통해 코드 기반 경험 캠페인에서 활용할 수 있는 의사 결정 항목에 조각을 첨부할 수 있는 기능을 제공합니다. 이 기능은 일부 고객에게는 제한된 가용성으로 제공됩니다. [자세히 보기](../experience-decisioning/create-decision.md#fragments)

* **여정**

   * **여정 일괄 작업** - 이제 여정 목록에서 여러 항목을 선택할 수 있습니다. 선택하면 한 번에 최대 10개의 여정을 일시 중지하거나 다시 시작할 수 있습니다.

   * **사용자 정의 액션 리디렉션(302) 지원** - 이제 사용자 정의 액션에서 요청별로 HTTP 302 리디렉션을 처리할 수 있습니다. 이를 통해 요청을 현지화된 URL 또는 지역별 URL로 리디렉션하는 API를 여정에 통합할 수 있습니다. 리디렉션은 자동으로 수행되므로 추가 구성 없이도 정확한 콘텐츠가 전달됩니다.

   * **여정의 여러 인바운드 작업** - 이제 여정 오케스트레이션을 단순화하기 위해 단일 여정에서 여러 인바운드 작업을 정의할 수 있습니다. 이전에 캠페인에서 사용할 수 있었던 이 기능을 사용하면 여러 코드 기반 경험, 인앱 메시지, 콘텐츠 카드 또는 웹 작업을 동시에 다른 위치에 전달할 수 있으며 각 작업에는 특정 콘텐츠가 포함되어 있습니다. [자세히 보기](../building-journeys/journey-action.md#multi-action)

## 캠페인 오케스트레이션

**사용 가능한 날짜**: 2025년 8월 4일

이제 Journey Optimizer에 브랜드 주도 일괄 캠페인을 위해 특별히 설계된 새로운 기능인 **캠페인 오케스트레이션**&#x200B;이 포함됩니다. 이 릴리스에서는 캠페인 오케스트레이션 캔버스 및 향상된 데이터 모델링을 도입하여 마케터가 개인화된 크로스 채널 캠페인을 계획하고, 타깃팅하고, 제공할 수 있도록 함께 작업합니다.

>[!IMPORTANT]
>
>캠페인 오케스트레이션에 액세스하려면 라이선스에 **Journey Optimizer - 캠페인 및 여정** 또는 **Journey Optimizer - 캠페인** 패키지가 포함되어야 합니다. 필요한 경우 Adobe 담당자에게 문의하여 라이선스를 확인하고 업데이트하십시오.

![캠페인 오케스트레이션 GIF](assets/do-not-localize/release.gif)

여기에는 [관계형 스키마 및 데이터 세트](#oc-relational) 및 [Campaign 캔버스](#oc-canvas)가 포함됩니다. 이러한 두 가지 혁신적인 기능을 통해 Journey Optimizer에서 일괄 캠페인을 오케스트레이션하기 위한 새로운 기준을 마련할 수 있습니다. 주요 기능은 아래에 나와 있습니다.

### 주요 기능 {#oc-capabilities}

* **여러 단계 워크플로**

  특별히 제작된 새로운 캠페인 오케스트레이션 캔버스를 통해 정교한 멀티채널 일괄 캠페인을 수행할 수 있습니다.

* **온디맨드 대상자**

  즉각적인 활성화를 위해 온디맨드로 대상자를 세그먼트화합니다.

* **다중 엔터티 세분화**

  제품, 스토어, 갱신, 예약 등과 같은 비즈니스 컨텍스트(비사용자 차원)를 사용하여 대상자를 작성합니다.

* **사전 전송 가시성**

  캠페인 실행 전과 실행 중에 대상자 및 캠페인을 검토, 세분화 및 최적화합니다.

### 캠페인 캔버스 {#oc-canvas}

일괄 캠페인을 위해 특별히 빌드된 새로운 시각적 오케스트레이션 인터페이스입니다. 이 캔버스를 통해 다음을 할 수 있습니다.

* 여러 단계, 다중 채널 캠페인 흐름의 시각적 계획

* 관계형 쿼리를 기반으로 구축된 온디맨드 대상 지원

* 고급 대상 분할, 대기 및 조건부 논리

* 비즈니스 규칙 및 필터 적용 후 정확한 사전 전송 카운트

### 관계형 스키마 및 데이터 세트 {#oc-relational}

이제 Adobe Journey Optimizer가 사용자 기반 프로필에 연결된 관계형 엔티티(예: 제품, 스토어, 예약, 계약)를 지원합니다. 이를 통해 다차원 데이터 구조 간에 세분화 및 개인화를 수행할 수 있으므로 다음과 같은 사용 사례가 가능합니다.

* 예약, 구독 또는 계약당 하나의 메시지

* 관련 엔티티 속성(예: 제품 카테고리 또는 스토어 위치)을 기반으로 한 세분화

* 향상된 주소 지정(예: 엔티티에 연결된 알려진 모든 연락처로 전송)

### 이것이 중요한 이유

이 릴리스를 통해 마케터는 유연한 데이터 모델링과 특별히 빌드된 오케스트레이션 경험을 결합하여 브랜드 주도, 대상 기반 일괄 마케팅을 완벽하게 제어할 수 있습니다. 이는 고급 개인화 및 확장성을 제공하면서도 실시간 여정의 일괄 캠페인 오케스트레이션을 위해 특별히 설계되었습니다.

### 자세히 알아보기

[캠페인 오케스트레이션](../orchestrated/gs-orchestrated-campaigns.md)에서 자세히 알아보십시오.


