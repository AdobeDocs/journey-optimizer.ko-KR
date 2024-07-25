---
solution: Journey Optimizer
product: journey optimizer
title: 릴리스 정보
description: Journey Optimizer 초기 릴리스 정보
hide: true
hidefromtoc: true
exl-id: 841122b9-04f6-4250-b0a5-e61f470787f7
source-git-commit: 5ccf9e08a24f840de7adbf04dc545904eaa32b8c
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 100%

---

# 초기 릴리스 정보 {#early-release-notes}

[!DNL Adobe Journey Optimizer]는 지속적으로 새로운 기능, 기존 기능 개선, 버그 해결을 제공합니다. 모든 변경 사항은 매월 말 [릴리스 정보](release-notes.md)에 통합됩니다.

아래 초기 릴리스 정보는 릴리스를 사용할 수 있는 당일까지 사전 통지 없이 변경될 수 있습니다. 링크, 화면, 업데이트된 설명서는 릴리스 날짜의 [릴리스 정보](release-notes.md)에 게시됩니다.

## 2024년 4월 초기 릴리스 정보 {#early-2024}

**릴리스 일자**: 2024년 5월 2일

### 새로운 기능 {#early-features}

이번 릴리스에는 아래에 있는 새로운 기능이 제공됩니다.

<!--table>
<thead>
<tr>
<th><strong>Business rules - Private Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>It is now possible to create and apply rule sets to your marketing communications.  </p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Experience Decisioning - Limited Availability</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Experience Decisioning simplifies personalization by offering a centralized catalog of marketing offers known as 'decision items' and a sophisticated decision engine. This engine leverages rules and ranking criteria to select and present the most relevant decision items to each individual.</p>
<p>These decision items are seamlessly integrated into a wide range of inbound surfaces through the new code-based experience channel, now accessible within Journey Optimizer campaigns. Experience Decisioning decision policies are available for use in code-based experience campaigns only.</p>
<p>Experience Decisioning is currently only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Personalization - Local Lookups - Multi-Entity Support - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>TBD</p>
</td>
</tr>
</tbody>
</table-->

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
<th><strong>IP Warmup Workflow - LA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now easily perform IP warmup workflows directly from the Journey Optimizer interface in a standardized and efficient way that follows the best practices for optimal deliverability.</p>
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

### 개선 사항 {#early-improvements}

이 릴리스는 아래 목록에 있는 개선 사항과 함께 제공됩니다.

<!--
* **Experience Decisioning + Code-based experiences (LA)**: You can now leverage the Experience decisioning feature to use decision items in your code-based campaigns. Note: The Code-based experience channel and Experience decisioning are not available for organizations that have purchased the Adobe Healthcare Shield and Privacy and Security Shield add-on offerings.
-->
<!--
* **Expression Fragments supported for Web and In-App**: Expression fragments are now available for the Web and In-app channels. 
-->


<!--
* **DULE for AJO Channel Surface**: It is now possible to apply a label on certain profile attributes to restrict their usage inside a channel surface through marketing actions.
-->


<!--
* **List-Unsubscribe updates**: Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. 
-->

<!--


**Experience decisionning**

From beta to LA, the following improvements that have been added:

* You can now leverage context data from Adobe Experience Platform in your decision rules using the **Context data** tab.  
* A new "Manage Experience decisions" permission is now available for the Decision Management resource. It allows you to manage rights related to Experience Decisioning.   
* You can now add multiple capping rules for a given decision item in Experience Decisioning. This allows you to increase the level of control over the way offers are sent.
* You can now create custom reporting dashboards of Experience Decisioning campaigns using [!DNL Customer Journey Analytics].
-->

**의사 결정 관리**

* 오퍼 또는 의사 결정에 적용된 모든 변경 사항을 확인할 수 있는 **변경 로그** 탭이 제거되었습니다. 이제 오퍼 및 의사 결정과 관련된 변경 사항을 **감사** 메뉴 아래 제품에서 사용할 수 있습니다.


**구성**

* 이제 채널 표면 수준에서 마케팅 작업을 선택할 수 있습니다. 표면에서 사용할 경우 고객의 동의 여부를 존중하기 위해 해당 마케팅 작업과 연결된 모든 동의 정책을 활용합니다.
* 이제 채널 표면에 대해 객체 수준 액세스 제어를 사용할 수 있습니다.

