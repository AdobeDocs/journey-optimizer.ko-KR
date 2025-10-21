---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer에 대한 사전 릴리스 정보
description: Adobe Journey Optimizer 사전 릴리스 정보
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: d09fc3ed670a50b6a99bcf660353ee37d31c7501
workflow-type: tm+mt
source-wordcount: '1089'
ht-degree: 52%

---

# 사전 릴리스 정보 {#e-release-notes}

[!DNL Adobe Journey Optimizer]은 지속적으로 새로운 기능, 기존 기능 개선, 버그 해결을 제공합니다. 모든 변경 사항은 매월 말 [릴리스 정보](release-notes.md)에 통합됩니다.


## 2025년 10월 프리릴리스 정보 {#oct-25-10-rn}

**아래 사전 릴리스 정보는 릴리스 공개 당일까지 사전 통지 없이 변경될 수 있습니다**. 링크, 화면, 업데이트된 설명서는 릴리스 일자에 릴리스 정보에 게시됩니다.

[Adobe Experience Platform 사전 릴리스 정보](https://experienceleague.adobe.com/ko/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}도 참조하십시오.

**릴리스 일자**: 2025년 10월 22일 목요일

### 새로운 기능 {#oct-25-10-features}



<table>
<thead>
<tr>
<th><strong>방해 금지 모드 시간/시간 기반 제외</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>자동 시간에서는 이메일, SMS, 푸시 및 WhatsApp 채널에 대한 시간 기반 제외를 정의할 수 있습니다. 특정 기간 동안 메시지가 전송되지 않도록 하여 고객 선호도 및 규정 준수 요구 사항을 준수할 수 있습니다.</p>
<p>규칙 세트를 통해 방해 금지 시간을 적용할 수 있으며, 이를 정확한 제어를 위해 캠페인이나 여정의 개별 작업에 할당할 수 있습니다. 이러한 프로세스를 간소화함으로써</p>
<p>이 기능은 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>사용자 정의 액션 모니터링 및 보고</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이 기능은 라이프사이클 상태 및 성과 경고를 포함하여 여정 상태와 실행에 대한 가시성을 향상시킵니다. 이제 사용자 정의 액션에서 예외적인 상황이 발생한 시점, 위치, 이유를 빠르게 이해할 수 있습니다.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>RCS Basic Messaging</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>With the new RCS Basic add-on offering, you can now deliver basic Rich Communication Services (RCS) messaging in Journey Optimizer, enabling the following enhanced messaging capabilities subject to provider and geographical support:</p>
<ul>
<li><strong>Branded and verified sender support:</strong> Send messages using verified business profiles with branding elements (logo, sender name, etc.).</li>
<li><strong>Message delivery insights:</strong> Receive detailed delivery reports including message status updates (e.g., sent, delivered, read).</li>
<li><strong>Link tracking:</strong> Embed and track URLs within RCS messages for engagement analytics.</li>
<li><strong>Fallback to SMS:</strong> Automatic fallback to SMS when the recipient's device does not support RCS or is temporarily unreachable via RCS.</li>
<li><strong>Basic message composition:</strong> Send basic text-based RCS messages.</li>
</ul>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<!--/td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Direct mail channel in Orchestrated campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Direct mail channel is now available in orchestrated campaigns. The Direct mail activity facilitates direct mail sending within your Orchestrated campaign, for both one-time and recurring messages. It serves to automate the process of generating the extraction file required by direct mail providers. You can combine channel activities into the Orchestrated campaign canvas to create cross-channel campaigns that can trigger actions based on customer behavior and data.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<!--/td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Direct Mail channel in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Previously limited to Campaigns, Direct Mail channel is now available on the journey canvas, enabling you to incorporate Direct Mail into your journeys. Direct Mail can now be used in both batch and 1:1 journey scenarios, with support for file extraction configuration and time-based frequency settings.</p>
<p> Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<!--/td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>작업 캠페인을 검색하는 새 API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 새로운 Journey Optimizer API를 사용할 수 있으므로 세부 정보, 버전 및 구성과 같은 캠페인 관련 데이터를 프로그래밍 방식으로 검색하고 검사할 수 있습니다.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>충성도 앱을 위한 새로운 소스 커넥터</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Adobe Experience Platform에서 Talon.One, Capillary 및 Kobie 충성도 앱에 대한 새로운 소스 커넥터를 사용할 수 있습니다. 이러한 커넥터를 사용하면 충성도 데이터를 Adobe Experience Platform으로 원활하게 스트리밍하고 Journey Optimizer에서 이러한 데이터를 활용할 수 있습니다.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Decisioning support in email channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add Decision policies into email journeys and campaigns. Decision policies are containers for your offers that leverage the Decisioning engine to dynamically return the best content to deliver for each audience member.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<img src="assets/do-not-localize/FILE.gif">
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>API 트리거 이메일 캠페인에 대한 높은 처리량 모드</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 API 트리거 캠페인에서 새로운 높은 처리량 모드를 사용할 수 있습니다. 이 모드는 대규모 실시간 메시지(초당 최대 5,000개의 트랜잭션)를 위해 설계되었으며 짧은 대기 시간으로 높은 가용성을 제공합니다.</p>
<p>이 기능은 Adobe 높은 처리량 트랜잭션 메시지 추가 기능 서비스를 구입한 조직의 이메일 채널에서만 사용할 수 있습니다. 자세한 내용은 Adobe 담당자에게 문의하십시오.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>재사용 가능한 타겟팅 규칙</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer을 사용하여 전용 UI 메뉴에서 규칙을 만들고 여정 최적화 활동에서 여정 또는 캠페인의 콘텐츠 최적화의 일부로 타깃팅을 작성할 때 활용할 수 있습니다.</p>
<p>타깃팅 규칙은 현재 제한된 가용성입니다. 액세스 권한을 얻으려면 Adobe 담당자에게 문의하세요.</p>
<p>이 기능은 Decisioning 추가 기능 서비스를 구입한 조직에서만 사용할 수 있습니다. 모든 고객에게 점진적으로 제공될 예정입니다.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>이메일 디자이너 테마</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 사전 승인된 테마를 빠르게 적용하여 모든 이메일에 대한 브랜드 일관성을 보장하고, 캠페인을 만드는 프로세스의 속도를 높이고, 디자인 팀에 대한 의존도를 줄이면서 고품질 이메일을 독립적으로 만들 수 있습니다.</p>
<p>이전에 Beta 버전으로 릴리스된 이 기능은 이제 조직 집합(제한된 가용성)에서 사용할 수 있습니다. 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.</p>
<img src="assets/do-not-localize/themes.gif">
<p>자세한 내용은 <a href="../email/apply-email-themes.md">세부 설명서</a>를 참조하십시오.</p>
<!--p>Availability date: October 22, 2025</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>새 여정 경고</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>여정 실행을 모니터링하는 데 사전 구성된 새 경고를 사용할 수 있습니다.</p>
<ul><li><a href="../reports/alerts.md#alert-discard-rate">프로필 삭제 비율 초과</a>: 지난 5분 동안 입력한 프로필에 대한 프로필 삭제 비율 임계값 초과</li>
<li><a href="../reports/alerts.md#alert-custom-action-error-rate">사용자 지정 작업 오류율 초과</a>: 지난 5분 동안 임계값에 대한 성공한 HTTP 호출에 대한 사용자 지정 작업 오류의 비율</li>
<li><a href="../reports/alerts.md#alert-profile-error-rate">프로필 오류율 초과</a>: 지난 5분 동안 입력한 프로필에 대한 오류가 있는 프로필의 비율이 임계값을 초과했습니다.</li></ul> <p>임계값을 수정하고 개별 여정 수준에서 경고를 받거나 전체적으로 구독할 수 있습니다.</p>
<p>자세한 내용은 <a href="../reports/alerts.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2025년 10월 14일 수요일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>실행 메타데이터 도우미</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>개인화 편집기에서 새로운 'executionMetadata' 도우미 기능을 사용할 수 있습니다. 이를 통해 컨텍스트 정보를 모든 기본 작업에 추가하고 데이터 세트에 캡처하여 외부 시스템으로 내보낼 수 있습니다.</p>
<p>이 기능은 제한적으로 이용할 수 있습니다. 액세스 권한을 얻으려면 Adobe 담당자에게 문의하세요.</p>
<p>자세한 내용은 <a href="../personalization/functions/helpers.md#execution-metadata">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2025년 10월 13일 화요일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>실험 요원이 여기 있습니다!</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><a href="https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-orchestrator.html" target="_blank">Adobe Experience Platform Agent Orchestrator</a>에서 제공하는 실험 에이전트는 Journey Optimizer에서 사용할 수 있습니다. </p>
<p>실험 에이전트는 웹 사이트, 이메일, 푸시 메시지 및 애플리케이션에서 디지털 실험을 실행하고 관리할 수 있는 방법을 현대화한 AI 기반 도구입니다. 실험을 보다 효율적으로 실행하고, 비즈니스 목표를 구성하고, 실행 가능한 통찰력을 생성하여, 무엇이 작동하고, 무엇이 작동하지 않았으며, 다음 실험할 위치를 강조 표시하는 데 도움이 됩니다.</p>
<p>자세한 내용은 <a href="https://experienceleague.adobe.com/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-experiment.html" target="_blank">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2025년 10월 10일 토요일</p>
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
<li>용량이나 수량이 더 필요하다면 PDF 첨부 파일 추가 기능을 구매할 수 있습니다. 자세한 내용은 Adobe 담당자에게 문의하십시오.</li>
</ul>
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).</p>
<p><img src="assets/do-not-localize/pdf-attachments.gif"/></p>
<p>자세한 내용은 <a href="../email/pdf-attachments.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2025년 9월 30일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>여정 검색을 위한 공개 API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 새로운 Journey Optimizer API를 사용하여 캠페인과 표면 등 여정 및 관련 개체를 검색할 수 있습니다.</p>
<p>자세한 내용은 <a href="https://developer.adobe.com/journey-optimizer-apis/references/journeys-retrieve/">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2025년 9월 25일</p>
</td>
</tr>
</tbody>
</table>


### 개선 사항

AI 모델을 통한 이메일 **의사 결정**

이제 Decisioning을 사용하여 AI 모델을 사용하여 이메일의 최상의 콘텐츠를 최적화할 수 있습니다. 예를 들어 이 기능을 사용하면 구매, 버튼 클릭 수, 장바구니에 추가 등과 같은 사용자 지정 이벤트에 따라 최상의 콘텐츠를 최적화할 수 있습니다.

**WhatsApp 채널의 실행 필드**

이메일 및 SMS 외에도 샌드박스 수준에서 WhatsApp 게재에 대한 기본 실행 필드 업데이트를 알 수 있습니다. 또한 WhatsApp 여정 활동 고급 매개 변수 또는 WhatsApp 채널 구성에서 변경하여 전역적으로 설정된 실행 필드를 재정의할 수 있습니다. <!-- [Read more](../FILE.md) -->

**Mailto(구독 취소) 주소에 대한 사용자 정의 속성 지원**

Journey Optimizer를 사용하면 Adobe 외부에서 동의를 관리하는 경우 이메일 구성에서 원클릭 구독 취소 링크와 사용자 정의 구독 취소 이메일 주소를 정의하여 외부 사용자 정의 엔드포인트를 설정할 수 있습니다. 수신자가 구독 취소 링크를 클릭하면 Journey Optimizer는 기본 프로필별 매개 변수 몇 가지를 동의 업데이트 이벤트에 추가합니다.

사용자 정의 엔드포인트를 더욱 개인화하기 위해 이제 동의 이벤트에 추가될 사용자 정의 속성을 정의할 수 있습니다. [자세히 보기](../email/list-unsubscribe.md#custom-attributes)

>[!AVAILABILITY]
>
>이 기능은 이미 2025년 8월부터 사용자 정의 **[!UICONTROL 원클릭 구독 취소 URL]**&#x200B;에 사용할 수 있었으며, 이제 제한된 가용성으로 **[!UICONTROL Mailto(구독 취소)]** 옵션이 릴리스되었습니다. 액세스 권한을 얻으려면 Adobe 담당자에게 문의하세요.

사용 가능한 날짜: 2025년 10월 6일