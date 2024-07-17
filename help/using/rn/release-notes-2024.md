---
solution: Journey Optimizer
product: journey optimizer
title: 2024년 릴리스 정보
description: Journey Optimizer 2024 릴리스 노트
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: bae533c5-1bfc-48bf-9f8d-1145383c040c
source-git-commit: fec6b15db9f8e6b2a07b55bc9e8fc4d9cb0d73d7
workflow-type: tm+mt
source-wordcount: '2229'
ht-degree: 98%

---

# 2024년 릴리스 정보 {#release-notes-2024}

이 페이지에는 2024년에 릴리스된 [!DNL Journey Optimizer]의 모든 기능과 개선 사항이 나와 있습니다.



## 2024년 5월 릴리스 정보 {#may-2024}

**릴리스 날짜**: 2024년 5월 21~22일

### 새로운 기능 {#e-features}

이번 릴리스에는 아래에 있는 새로운 기능이 제공됩니다.

<table>
<thead>
<tr>
<th><strong>Experience Decisioning - 제한된 가용성</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Experience Decisioning은 '의사 결정 항목'으로 알려진 마케팅 의 중앙 집중식 카탈로그와 정교한 의사 결정 엔진을 제공하여 개인화를 간소화합니다. 이 엔진은 규칙과 순위 기준을 활용하여 각 개인에게 가장 관련성 높은 의사 결정 항목을 선택하고 제공합니다.</p>
<p>이러한 의사 결정 항목은 이제 Journey Optimizer 캠페인에서 액세스할 수 있는 새로운 코드 기반 경험 채널을 통해 광범위한 인바운드 표면에 원활하게 통합됩니다. 경험 결정 의사 결정 정책은 코드 기반 경험 캠페인에서만 사용할 수 있습니다.</p>
<p>SMS 채널은 현재 조직 집합(제한된 가용성)에만 사용할 수 있습니다. 권한을 얻으려면 Adobe 담당자에게 문의하십시오.</p>
<img src="assets/do-not-localize/gif-exd.gif"/>
<p>자세한 내용은 <a href="../experience-decisioning/gs-experience-decisioning.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>이메일 표면 개인화 - 제한된 가용성</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 이메일 채널 표면을 만들 때 동적 하위 도메인과 개인화된 헤더 매개 변수를 정의하여 이메일 설정을 더욱 유연하게 제어하고 있습니다.</p>
<p>이메일 표면 개인화는 현재 조직 집합에만 사용할 수 있습니다(제한된 가용성). 권한을 얻으려면 Adobe 담당자에게 문의하십시오.</p>
<p>자세한 내용은 <a href="../email/surface-personalization.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>IP Warmup Workflow</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>If you are sending email on a brand new IP address, you can now easily perform IP warmup workflows directly from the user interface. Adobe Journey Optimizer offers a standardized and efficient way to warm up your IP adresses that follows the best practices for optimal deliverability.</p>
<p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Business rules - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create granular frequency capping rules, and apply them to different types of marketing communications through rule sets. This new capability lets you control how often your audiences receive a message by setting cross-channel rules, that automatically exclude over-solicited profiles from messages and actions.</p>
<p>Business rules capability is currently available as a beta. To join the beta program, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Extended personalization data - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now lookup and fetch data values within Adobe Experience Platform datasets, and use these values to build conditions in Adobe Journey Optimizer. You can leverage data from a lookup dataset when a relationship has been defined using an attribute inside of an array of objects. You can specify non-profile enabled datasets for lookup. Once enabled, you can use a profile attribute as a join key to the specified dataset to retrive further data for personalization.</p>
<p>This capability is currently available as a public beta.</p>
</td>
</tr>
</tbody>
</table-->

### 개선 사항 {#e-improvements}

이 릴리스는 아래 목록에 있는 개선 사항과 함께 제공됩니다.

**경험 결정**(제한된 가용성)

Beta부터 이 릴리스까지 다음과 같은 개선 사항이 추가되었습니다.

* **경험 결정+코드 기반 경험(LA)**: 이제 경험 결정 기능을 활용하여 코드 기반 캠페인에서 의사 결정 항목을 사용할 수 있습니다. 참고: Adobe Healthcare Shield 및 Privacy and Security Shield 추가 기능을 구매한 조직에서는 코드 기반 경험 채널 및 경험 결정을 사용할 수 없습니다. [자세히 보기](../code-based/get-started-code-based.md)
* **컨텍스트 데이터** - 이제 의사 결정 규칙 및 등급 수식에서 Adobe Experience Platform의 컨텍스트 데이터를 활용할 수 있습니다. [자세히 보기](../experience-decisioning/context-data.md)
* **새로운 권한** - 이제 의사 결정 관리 리소스에 대해 새로운 ‘경험 결정 관리’ 권한을 사용할 수 있습니다. 이를 통해 경험 결정과 관련된 권한을 관리할 수 있습니다. [자세히 보기](../experience-decisioning/gs-experience-decisioning.md)
* **캡핑 규칙** - 이제 경험 결정에서 지정된 의사 결정 항목에 대해 여러 개의 캡핑 규칙을 추가할 수 있습니다. 이를 통해 오퍼를 전송하는 방식에 대한 제어 수준을 향상시킬 수 있습니다. [자세히 보기](../experience-decisioning/items.md#capping)
* **보고** - 이제 [!DNL Customer Journey Analytics]를 사용하여 경험 결정 캠페인의 사용자 정의 보고 대시보드를 만들 수 있습니다. [자세히 보기](../experience-decisioning/cja-reporting.md)


<!--**Decision Management**

* **Multi-rule support** - You can now add up to 10 capping rules for a given offer in Decision Management. This allows you to increase the level of control over the way offers are sent.
* **Audits** - The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu. -->


**이메일 채널**

<!--
* **List-unsubscribe** - Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. Refer to the following pages: [Email opt-out management](../email/email-opt-out.md#unsubscribe-header) and [Configure email settings](../email/email-settings.md#list-unsubscribe)
-->

* **스팸 점수**(Beta) - 이제 전용 스팸 보고서에서 콘텐츠 스팸 점수를 확인할 수 있습니다. 이제 Adobe Journey Optimizer에서 SpamAssassin을 사용하여 이메일 콘텐츠를 테스트하고 ISP 또는 사서함 공급자가 이를 스팸으로 간주할지 여부를 나타내는 점수를 매길 수 있습니다. [자세히 보기](../content-management/spam-report.md)

  >[!AVAILABILITY]
  >
  >이 기능은 현재 beta 버전으로 beta 고객에게만 제공됩니다. Beta 프로그램에 참여하려면 Adobe 담당자에게 문의하십시오.

<!--
**Audiences**

* The use of audiences and attributes from audience composition and custom upload (CSV file) is now available for use with Healthcare Shield or Privacy and Security Shield.-->

<!--**Personalization**

* **Expression fragment** - Expression fragments are now available for the **In-app channel**. [Read more](../personalization/use-expression-fragments.md)-->

**여정**

<!--* **Merge policies** (Limited Availability)- Merge policies used by a journey are now visible and consistent throughout the journey.-->
* **mTLS 지원** - 이제 사용자 정의 작업에 mTLS 인증이 지원됩니다. mTLS를 활성화하기 위해 사용자 정의 작업 또는 여정에 구성을 추가할 필요는 없습니다. mTLS 활성화 엔드포인트가 감지되면 자동으로 활성화됩니다. [자세히 보기](../action/about-custom-action-configuration.md#mtls-protocol-support)
* **이벤트의 조회 테이블** - 이제 개체 배열 내의 속성을 사용하여 관계를 정의한 경우 조회 데이터 세트의 데이터를 활용할 수 있습니다. 조회 값을 여정(조건, 사용자 정의 작업 등) 및 메시지 개인화에 사용할 수 있습니다. [자세히 보기](../event/experience-event-schema.md#relationships_limitations)
* **이벤트 구성의 고급 표현식 편집기**(LA) - 이제 이벤트를 구성할 때 고급 표현식 편집기를 활용하여 이벤트 ID 조건에 보다 복잡한 표현식을 정의하거나 함수를 사용할 수 있습니다. 이 기능은 일부 고객 대상 제한된 가용성으로 릴리스됩니다. [자세히 보기](../event/about-creating.md#adv-exp-editor)
* **병합 정책**(LA) - 여정에서 사용하는 병합 정책이 이제 여정 전체에서 일관적이며 직접 볼 수 있습니다. 이 기능은 일부 고객 대상 제한된 가용성으로 릴리스됩니다. [자세히 보기](../building-journeys/journey-properties.md#merge-policies)

**세계화**

통일성 있는 사용자 경험을 제공하기 위한 지속적인 노력의 일환으로 Adobe Experience Cloud 제품 및 앱에서 사용되는 용어를 서로 맞추는 작업을 합니다. 이에 따라 독일어 서비스에서 “Titel”이라는 용어가 개체와 관련된 상황의 경우 “Label”로 변경됩니다. 이 변경 사항은 UI 및 설명서에 점진적으로 적용됩니다.




## 2024년 4월 릴리스 정보 {#apr-2024}

**릴리스 일자**: 2024년 5월 2일

### 새로운 기능 {#apr-features}

이번 릴리스에는 아래에 있는 새로운 기능이 제공됩니다.

<table>
<thead>
<tr>
<th><strong>MMS(멀티미디어 메시지 서비스) - 모든 공급자</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 [SMS 채널]을 통해 MMS(멀티미디어 메시지 서비스) 메시지를 보내 고객과 이미지, GIF 또는 비디오를 공유하는 기능이 추가되어 커뮤니케이션을 더욱 원활하게 진행할 수 있습니다. 이전에는 Sinch에서만 사용할 수 있었지만, 이제 MMS는 Infobip 및 Twilio에서도 사용할 수 있습니다.</p>
<img src="assets/do-not-localize/mms.gif"/>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>향상된 여정 디자이너 및 라이브 보고</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이번 릴리스는 여정을 위한 캔버스 사용자 인터페이스가 개선되어 보다 직관적이고 효율적인 사용자 경험을 제공합니다. 활동은 더 적은 클릭 수로 여정 캔버스에 더 명확하고 많은 정보를 제공합니다.</p>
<img src="assets/new-canvas3.gif"/>
<p>향상된 여정 캔버스 디자인과 함께 지난 24시간 보고 지표를 여정 캔버스에서 직접 볼 수 있는 기능을 도입했습니다. </p>
<img src="assets/new-canvas6bis.png"/>
<p><strong>참고</strong>: 이러한 변경 사항은 4월 릴리스부터 모든 환경으로 점진적으로 롤아웃됩니다.</p>
<p>자세한 내용은 <a href="new-canvas.md">자세한 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>

<!-- table>
<thead>
<tr>
<th><strong>AI Assistant - Experience Variant Generation - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Once you have created and personalized your message, take your content to the next level with the AI assistant. You can now use the AI assistant to optimize your message's impact by experimenting with different main titles, and images. Each variant is managed as a unique Treatment, to measure and compare which title effectively generates more clicks.</p>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Email Surface Personalization - Private beta </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now define dynamic subdomains and personalized header parameters when creating email channel surfaces, for increased flexibility and control over your email settings.</p>
</td>
</tr>
</tbody>
</table-->

### 개선 사항 {#apr-improvements}

이 릴리스는 아래 목록에 있는 개선 사항과 함께 제공됩니다.

<!--
* **Expression Fragments supported for Web and In-App**: Expression fragments are now available for the Web and In-app channels. 
-->


<!--
* **DULE for AJO Channel Surface**: It is now possible to apply a label on certain profile attributes to restrict their usage inside a channel surface through marketing actions.
-->


<!--
* **List-Unsubscribe updates**: Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. 
-->

**구성**

* 이제 채널 표면 수준에서 마케팅 작업을 선택할 수 있습니다. 표면에서 사용할 경우 고객의 환경 설정을 존중하기 위해 해당 마케팅 액션과 관련된 모든 동의 정책을 활용합니다. [자세히 보기](../action/consent.md#surface-marketing-actions)
* 이제 채널 표면에 대해 객체 수준 액세스 제어를 사용할 수 있습니다. [자세히 보기](../configuration/channel-surfaces.md#create-channel-surface)
* 이제 채널 표면에서 목록 구독 취소를 활성화하면서 다른 모든 소스의 동의를 관리하는 방식에 맞게 동의 수준을 정의할 수 있습니다. [자세히 보기](../email/email-settings.md#list-unsubscribe)

**콘텐츠 관리**

* 이제 모든 채널에 대한 콘텐츠 템플릿을 시뮬레이션할 수 있습니다. [자세히 보기](../content-management/content-templates.md#test-templates)

**개인화**

* 새로운 **toInt** 헬퍼 함수는 표현식 편집기에서 사용할 수 있습니다. 이 옵션을 사용하면 이러한 유형(number, double, int, long, float, short, byte, boolean, string) 중 하나를 정수로 전환할 수 있습니다. [자세히 보기](../personalization/functions/math.md#to-int)



## 2024년 3월 릴리스 정보 {#mar-2024}

**릴리스 날짜**: 2024년 3월 19~20일

### 새로운 기능 {#mar-features}

이번 릴리스에서 제공하는 새로운 기능을 아래에서 자세히 설명합니다.

<table>
<thead>
<tr>
<th><strong>코드 기반 경험</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>새로운 [코드 기반 경험] 채널로 Adobe Journey Optimizer에서 원하는 인바운드 속성에 대해 고급 개인화 및 테스트를 수행할 수 있으므로 웹 앱, 모바일 앱, 데스크탑 앱, 비디오 콘솔, TV에 연결된 디바이스, 스마트 TV, 키오스크, ATM, IoT 디바이스 등과 같은 다양한 접점에서 맞춤형 경험을 원활하게 전달할 수 있습니다.</p>
<P>주요 기능은 다음을 포함합니다.</p>
<ul><li> 범용 개인화: 개인화된 경험을 모든 접점으로 확장하여 통합적이고 맞춤화된 사용자 여정을 보장합니다.</li>
<li>세분화된 편집 정밀도: 앱 또는 웹 페이지 내의 개별 위치에서 있는 특정 콘텐츠를 편집할 수 있습니다.</li>
<li>다목적 구현: 개발 환경과 원활하게 통합할 수 있도록 서버측, API 기반 또는 SDK 기반 구현 방법을 지원합니다.</li></ul></p>
<p>자세한 내용은 <a href="../code-based/get-started-code-based.md">자세한 설명서</a>를 참조하세요.</p>
<img src="assets/do-not-localize/code-based.gif"> 
</tr>
</tbody>
</table>

### 개선 사항 {#mar-improvements}

이 릴리스는 아래 목록에 있는 개선 사항과 함께 제공됩니다.

**콘텐츠 템플릿**

* **썸네일** - 이제 콘텐츠 템플릿을 시각적 접근성을 개선하기 위해 썸네일을 표시하는 **그리드 보기** 모드로 볼 수 있습니다. 현재는 이메일 HTML 템플릿만 지원됩니다. [자세히 알아보기](../content-management/content-templates.md#template-thumbnails)

  >[!AVAILABILITY]
  >
  >이 기능은 소규모 고객을 위해 LA(Limited Availability)에서 출시됩니다.

**여정**

여정 작성 라이프사이클에 새로운 중간 상태가 추가되었습니다.

* **초안** 상태와 **라이브** 상태 사이의 **게시 중** 상태
* **라이브** 상태와 **정지됨** 상태 사이의 **멈추는 중** 상태
* **초안** 상태와 **초안(테스트)** 상태 사이의 **테스트 모드 활성화 중** 또는 **테스트 모드 비활성화 중** 

여정이 중간 상태일 때는 읽기 전용입니다. [자세히 알아보기](../building-journeys/journey-gs.md#filter)

## 2024년 2월 릴리스 정보 {#feb-2024}

**릴리스 날짜**: 2024년 2월 21~22일

### 새로운 기능{#feb-features}

이번 릴리스에는 아래 목록에 있는 새로운 기능이 제공됩니다.


<table>
<thead>
<tr>
<th><strong>웹 인앱 메시지</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 새로운 웹 인앱 메시지 기능을 사용하면 모달 오버레이 메시지를 통해 웹 사이트에 직접 개인화된 콘텐츠를 표시할 수 있습니다. 이 기능을 사용하면 웹 방문자와 효과적으로 상호 작용하여 사용자 상호 작용, 보존 및 전환율을 향상할 수 있습니다.<br/><br/></p>
<p>자세한 내용은 <a href="../in-app/create-in-app-web.md">세부 설명서</a>를 참조하십시오.<br></br></p>
<img src="assets/do-not-localize/web_inapp.gif">
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>다중 채널 콘텐츠 템플릿</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 이메일 외에도 푸시, 인앱, SMS 및 DM 채널에 콘텐츠 템플릿을 사용할 수 있습니다. 각 채널에는 전용 템플릿 유형이 있습니다. 이메일의 경우 이제 제목 줄을 이메일 템플릿의 일부로 저장할 수 있는 콘텐츠 유형을 선택할 수 있습니다. <br/><br/></p>
<p>자세한 내용은 <a href="../content-management/content-templates.md">자세한 설명서</a>를 참조하세요.<br></br></p>
<img src="assets/do-not-localize/multi-chan-templates.gif"> 
</tr>
</tbody>
</table>


### 개선 사항 {#feb-improvements}

이 릴리스는 아래 목록에 있는 개선 사항과 함께 제공됩니다.

**대상자**

* **시드 목록** - 이제 **시드 목록**&#x200B;을 사용할 때 변형이 지원됩니다. 시드 주소는 동일한 메시지의 모든 변형(예: 콘텐츠 실험의 다양한 처리) 사본을 받습니다. [자세히 보기](../configuration/seed-lists.md)

이전에 Beta로 제공되었던 향상된 기능은 이제 모든 사용자가 사용할 수 있습니다.

* 이제 **대상자 구성을 통해 생성된** 대상자를 타겟팅하고 여정에서 데이터 보강 속성을 활용할 수 있습니다. [자세히 알아보기](../building-journeys/read-audience.md)

* 이제 여정과 캠페인에 **CSV 파일에서 업로드된 대상자**&#x200B;를 타겟팅할 수 있습니다. [자세히 알아보기](../audience/about-audiences.md#segments-in-journey-optimizer)

  >[!AVAILABILITY]
  >
  >* 대상자 구성 및 사용자 정의 업로드(CSV 파일)의 대상자 및 속성은 현재 Healthcare Shield 또는 Privacy and Security Shield에서 사용할 수 없습니다.
  >* **CSV 파일의 대상자 업로드** 개선 사항은 초기 릴리스 이후 며칠 동안 점진적으로 롤아웃됩니다. 일부 사용자는 즉시 액세스할 수 있지만 다른 사용자는 자신의 환경에서 사용할 수 있게 되기까지 지연이 발생할 수 있습니다.

**여정**

* **여정 필터링** - 이제 기존의 사전 정의된 날짜 필터 외에도 **사용자 정의 날짜를 사용하여 여정** 인벤토리를 필터링할 수 있습니다. 이렇게 하면 특정 날짜, 특정 달 내, 전체 연도 또는 지정된 시간 범위에 작성되었거나 게시된 여정을 표시하여 목록을 세분화할 수 있습니다. [자세히 보기](../building-journeys/journey-gs.md#filter)
* **사용자 정의 작업** - 이제 **content-type** 헤더를 업데이트할 수 있습니다. 이 새로운 **content-type**&#x200B;은 JSON 콘텐츠를 참조해야 합니다. [자세히 보기](../action/about-custom-action-configuration.md#url-configuration)
* **구성** - stepEvents의 identityMap 속성이 이제 미리 채워져 있습니다. 기본 신원은 “primary = true”로 정의됩니다. [자세히 보기](../reports/sharing-field-list.md)
* **사용자 인터페이스** - 여정 화면의 상단 표시줄이 향상된 경험을 위해 재구성되었습니다. 여러 업데이트 중 여정 속성에 액세스할 수 있는 &#39;연필&#39; 아이콘이 이제 여정 이름 옆의 상단 표시줄 왼쪽에 표시됩니다. [자세히 보기](../building-journeys/journey-properties.md)

**SMS 채널**

* **옵트인/옵트아웃 키워드** - 이제 SMS 채널을 구성할 때 원하는 대로 **옵트인 및 옵트아웃 키워드**&#x200B;를 사용자 정의할 수 있습니다. Journey Optimizer는 지정된 이러한 키워드를 기반으로 응답을 트리거합니다. [자세히 알아보기](../sms/sms-configuration.md)

**캠페인**

* **API 트리거 캠페인** - API 트리거 캠페인을 활성화한 후 생성된 cURL 코드가 향상되었습니다. 이제 메시지에 사용된 모든 개인화(프로필 및 컨텍스트) 변수가 포함됩니다. [자세히 보기](../campaigns/api-triggered-campaigns.md#execute)

**빈도 규칙**

* 이제 이메일 및 푸시 외에도 SMS 및 DM 채널에 대한 빈도 규칙을 만들 수 있습니다. 빈도 규칙은 빈도 상한에 도달하면 메시지 및 작업에서 과도하게 요청된 프로필을 자동으로 제외합니다. [자세히 보기](../configuration/frequency-rules.md)

<!--**Decision management**

* **Capping rules** - You can now add **multiple capping rules** for one offer. This allows you to increase the level of control over the way offers are sent.-->


## 2024년 1월 릴리스 정보 {#jan-2024}

**릴리스 날짜**: 2024년 1월 30~31일

### 새로운 기능{#jan24-features}

이번 릴리스에는 아래 목록에 있는 새로운 기능이 제공됩니다.

<table>
<thead>
<tr>
<th><strong>전달성 업데이트</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer에서 DMARC 인증 기술을 지원합니다.</p>
<p>2024년 2월 1일부터 Google 및 Yahoo!에서 이메일을 보내는 데 사용하는 모든 도메인에 DMARC 레코드를 요구합니다. Journey Optimizer에서 Adobe에 위임한 모든 하위 도메인에 DMARC 레코드가 설정되어 있는지 확인해 주세요.</p>
<p>자세한 내용은 <a href="../configuration/dmarc-record-update.md">세부 설명서</a>를 참고하십시오.</p>
<br/><img src="assets/do-not-localize/dmarc.gif"/>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>사용 사례 플레이북</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Real-Time CDP 및 Journey Optimizer의 산업별 사용 사례 플레이북 카탈로그를 활용하여 Adobe Experience Platform 및 Adobe Journey Optimizer를 사용하여 수행할 수 있는 일반적인 사용 사례를 해결합니다.</p><p>요구 사항에 가장 적합한 플레이북을 선택하면 여정, 메시지, 스키마 또는 세그먼트와 같은 사용 사례를 지원하는 데 필요한 자산을 생성하고, 가치 창출 시간을 단축하기 위해 스키마에 맞게 사용자 지정할 수 있습니다.</p>
<p>자세한 내용은 <a href="../start/playbooks.md">자세한 설명서</a>를 참조하세요.</p>
<br/><img src="assets/do-not-localize/playbooks.gif"/>
</tr>
</tbody>
</table>

### 개선 사항 {#jan24-improvements}

이 릴리스는 아래 목록에 있는 개선 사항과 함께 제공됩니다.

**보고**

* **새 도메인 기반 분류 위젯** - 캠페인 및 여정 보고서를 개선하기 위해 새 위젯이 추가되었습니다. **도메인별 바운스 이유**, **도메인에서 전송 및 전달**, **도메인별 열기 및 클릭 수** 및 **도메인별 바운스 및 오류** 위젯은 도메인 수준에서 주요 이메일 게재 및 추적 지표에 대한 세부 분류를 제공합니다. [자세히 알아보기](../reports/channel-report.md)

**SMS 채널**

* **이중 옵트인** - SMS에 대한 이중 옵트인 워크플로우를 사용하면 장치에서 요청을 시작할 때 사용자가 메시지를 수신하도록 명시적으로 옵트인할 수 있습니다. 사용자는 인바운드 SMS 메시지를 전송하여 동의 프로세스를 시작합니다. 동의를 확인하면 최종 확인을 요청하는 후속 메시지가 발송됩니다. 사용자 프로필이 존재하지 않으면 확인 후 생성됩니다. [자세히 알아보기](../sms/sms-configuration.md)

  이 기능은 Sinch 및 Infobip SMS 공급자만 사용할 수 있습니다.

**여정**

* **반응 이벤트 기간** - **반응 이벤트**&#x200B;에서 정의할 수 있는 최대 기간은 이제 30일이 아니라 29일입니다. [자세히 알아보기](../building-journeys/reaction-events.md)

<!--* **Date filters** - You can now use custom dates to filter the journeys inventory, in addition to the existing predefined date filters. This allows you to refine the list by displaying journeys published on a specific date, within a particular month, throughout an entire year, or within specified time ranges. [Learn more](../building-journeys/journey-gs.md#filter)-->

* **대상자 읽기**  - **대상자 읽기** 활동은 이제 예약된 일별 배치 작업이 실행된 후 하루에 한 번만 생성되는 배치 세그먼트에 대한 프로필 스냅샷 데이터 세트를 사용하므로 데이터는 마지막 일별 배치 작업까지 새로 고쳐집니다. [자세히 알아보기](../building-journeys/read-audience.md)

* **필드 그룹** - 이 릴리스에서는 특정 경우에 필드 그룹이 저장되지 않는 문제를 해결했습니다.

* 여러 함수에서 `<listObject>` 지원이 수정되었습니다.

**빈도 규칙**

* **주별 빈도 상한** - 이제 월별 외에 일주일 단위로 고객 프로필에 전송되는 최대 메시지 수를 지정할 수 있습니다. 빈도 캡은 선택된 캘린더 기간에 기반하고 대응하는 시간대가 시작될 때 재설정됩니다. [자세히 알아보기](../configuration/frequency-rules.md#create-new-rule)

  >[!NOTE]
  >
  >필요에 따라 일일 빈도 상한도 이용하실 수 있습니다. Adobe 담당자에게 문의하십시오.

**의사 결정 관리**

* **Edge 빈도 설정** - 이제 빈도 제한 카운터가 업데이트되어 Edge Decisioning API 결정에서 3초 이내에 사용할 수 있습니다. [자세히 알아보기](../offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)
