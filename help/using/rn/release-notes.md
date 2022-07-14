---
title: 릴리스 정보
description: Journey Optimizer 릴리스 정보
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: ac3c49c16a2496b3d5bc9b803589644b69c6565c
workflow-type: ht
source-wordcount: '487'
ht-degree: 100%

---

# 릴리스 정보 {#release-notes}

이 페이지에는 [!DNL Journey Optimizer]의 새로운 기능과 개선 사항이 모두 포함되어 있습니다. 또한 자세한 변경 사항은 [최신 설명서 업데이트](documentation-updates.md) 페이지를 참조하십시오.

[!DNL Adobe Journey Optimizer]은(는) 기본적으로 [!DNL Adobe Experience Platform] 기반으로 구축되었으며 최신 혁신 및 향상된 기능을 활용할 수 있습니다. [Adobe Experience Platform 릴리스 노트](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=ko-KR){target=&quot;_blank&quot;}에서 이러한 변경 사항에 대해 자세히 알아보십시오.

![뉴스레터](../assets/do-not-localize/nl-icon.png) 오늘 [Adobe Journey Optimizer 분기 뉴스레터](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;}에 등록하시면 분기마다 최신 제품 업데이트, 흥미로운 사례, 사용 사례, 팁 등을 받은 편지함에 바로 받을 수 있습니다.

## 2022년 6월 릴리스 {#june-2022-release}

### 새로운 기능

<table>
<thead>
<tr>
<th><strong>사용자에게 SMS 보내기(제한된 가용성)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 <b>Sinch</b> 또는 <b>Twilio</b>와의 통합을 통해 Journey Optimizer에서 SMS를 만들고, 개인화하고, 보낼 수 있습니다.</p>
<img src="assets/do-not-localize/SMS.gif"/>
<p>SMS 채널은 현재 조직 집합(제한된 가용성)에만 사용할 수 있습니다. 자세한 내용은 Adobe 직원에게 문의하십시오.</p>
<p>이 <a href="../messages/create-sms.md">세부 설명서</a>에서 SMS를 만들고 보내는 방법을 알아보십시오.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Adobe Stock 통합을 통해 더 효과적인 이미지 찾기</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Stock 및 Adobe Journey Optimizer 이메일 디자이너 통합 플러그인을 사용하면 메시지를 작성하는 데 사용할 이미지를 쉽게 탐색, 라이선싱 및 저장할 수 있습니다. </br> 새로운 <b>유사한 스톡 사진 찾기</b> 옵션으로도 이미지의 내용, 색상 및 컴포지션과 일치하는 스톡 사진을 찾을 수 있습니다. </p>
<img src="assets/do-not-localize/stock-rn.gif"/>
<p>자세한 내용은 <a href="../design/stock.md">세부 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>모든 이메일에서 이메일 BCC 사용</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 이메일 BCC(숨은 참조) 기능을 사용하여 Adobe Journey Optimizer에서 보낸 이메일을 저장할 수 있습니다. 이메일 사전 설정에서 이 옵션을 활성화하여 전송된 모든 이메일이 BCC 주소로 블라인드(bcc)로 복사됩니다.</p>
<img src="assets/do-not-localize/bcc-rn.gif"/>
<p>자세한 내용은 <a href="../configuration/bcc-email.md">세부 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>

<!--<table>
<thead>
<tr>
<th><strong>Automatically use the best performing offer in your decisions</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use personalized optimization model systems in Decision Management. This new type of model allows you to optimize and personalize offers based on segments and offer performance.</p>
<p>The use of personalized optimization AI models is currently restricted to selected users, and will be deployed to all environments in a future release.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>For more information, refer to the <a href="../offers/ranking/personalized-optimization-model.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>샌드박스 간 개체 복사</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer 샌드박스에서 다른 샌드박스(예: 비프로덕션 샌드박스에서 프로덕션 샌드박스로)로 경험을 다시 만들 수 있습니다. 이 새 기능은 여정이 올바르게 실행하기 위해 사용하는 개체 등 전체 여정을 특정 환경에서 다른 환경으로 복사합니다. 여정 외에도 오퍼, 메시지, 스키마, 데이터 세트, 데이터 소스, 이벤트, 작업과 같은 다른 구성 요소를 복사할 수 있습니다.</p>
<p>자세한 내용은 <a href="../building-journeys/copy-to-sandbox.md">자세한 설명서</a>를 참조하세요.
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Dynamic Expression Builder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create conditional content blocks across different authoring services to personalize your content. In addition to the Personalization Expression Library, the Expression Editor provides a new Conditional Rule Builder to help you design and save your content blocks.</p>
<p>For more information, refer to the <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->


### 개선 사항

**의사 결정 관리**

* **HTML 및 JSON 파일 지원** - 이제 Adobe Experience Cloud 자산 라이브러리의 외부 HTML 및 JSON 파일을 오퍼 표시 컨텐츠로 끌어다 놓을 수 있습니다. [자세히 보기](../offers/offer-library/add-representations.md#html-json)


**이메일**

* **템플릿으로 저장** - 이제 이메일 콘텐츠를 템플릿으로 저장하고 다른 메시지를 만들 때 다시 사용할 수 있습니다. [자세히 알아보기](../design/email-templates.md)

<!--
**Journeys**

* **Ending a journey** - In the journey canvas, the **End** activity has been removed from the palette. End tags are now added by default at the end of each path and cannot be removed. This improvement allows better reporting of where a customer dropped out of the journey, without any action from the user.

-->

**관리**

<!--* **Allowed list in the UI** - You can now use the Journey Optimizer user interface to add new email addresses or domains to the allowed list.-->

* **미리 보기 추적 URL 매개 변수** - 메시지 사전 설정을 구성할 때 URL 추적 매개 변수를 정의하는 경우 결과 추적 URL의 동적 미리 보기가 표시됩니다. [자세히 보기](../configuration/email-settings.md#url-tracking)

* **메시지 사전 설정 에디션** - 메시지 사전 설정을 업데이트할 때 드는 최대 처리 시간이 3시간으로 단축되었습니다. [자세히 보기](../configuration/message-presets.md#edit-message-preset)

* **IP 풀 에디션** - IP 풀을 업데이트할 때 드는 최대 처리 시간이 최대 3시간으로 단축되었습니다. [자세히 보기](../configuration/ip-pools.md#edit-ip-pool)

<!--* **Personalize tracking URL parameters** - You can now use the Expression Editor to configure URL tracking parameters in your message presets. [Learn more](../configuration/email-settings.md#url-tracking)-->

<!--
**Reporting**

* **Performance measurement** - A new **Reporting** tab is now available in the Administration > Configurations menu to set up reporting data sources.
-->
