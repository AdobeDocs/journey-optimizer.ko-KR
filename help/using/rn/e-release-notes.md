---
solution: Journey Optimizer
product: journey optimizer
title: 릴리스 정보
description: Journey Optimizer 초기 릴리스 정보
feature: Release Notes
topic: Content Management
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: f24f4526d4b324df8da56013f0e41c11e1268ca8
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 77%

---

# 초기 릴리스 정보 {#e-release-notes}

[!DNL Adobe Journey Optimizer]는 지속적으로 새로운 기능, 기존 기능 개선, 버그 해결을 제공합니다. 모든 변경 사항은 매월 말 [릴리스 정보](release-notes.md)에 통합됩니다.

**아래 초기 릴리스 정보는 릴리스 공개 당일까지 사전 통지 없이 변경될 수 있습니다**. 링크, 화면, 업데이트된 설명서는 릴리스 날짜의 [릴리스 정보](release-notes.md)에 게시됩니다.

## 2024년 7월 초기 릴리스 정보 {#e-2024}

**릴리스 일자**: 2024년 7월 30~31일

### 새로운 기능 {#e-features}

이번 릴리스에는 아래에 있는 새로운 기능이 제공됩니다.

<table>
<thead>
<tr>
<th><strong>IP 준비 워크플로</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>완전히 새로운 IP 주소로 이메일을 보내는 경우 이제 사용자 인터페이스에서 직접 IP 준비 워크플로를 쉽게 수행할 수 있습니다. Adobe Journey Optimizer는 최적의 전달성을 위한 모범 사례에 따라 IP 주소를 준비하는 표준화되고 효율적인 방법을 제공합니다.</p>
<!--p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>모든 공급자의 SMS 채널(Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer 내에서 기본 공급자인 Sinch, Infobip, Twilio 외 추가 SMS 공급자를 구성할 수 있습니다.</p>
<!--p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Federated Audience 구성(제한된 가용성)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Adobe Journey Optimizer에서 Federated Audience Composition을 사용할 수 있습니다. 이를 통해 기업은 다양한 사용 사례에서 더 나은 활용도를 위해 데이터를 구성할 수 있습니다. Adobe Real-time Customer Data Platform 및/또는 Adobe Journey Optimizer 사용자는 이 새로운 접근 방식을 통해 기존 데이터 웨어하우스에서 직접 데이터 세트를 페더레이션하여 하나의 시스템에 Adobe Experience Platform 대상 및 속성을 모두 구축하고 보강할 수 있습니다.</p>
<!--p>For more information, refer to the <a href="https://experienceleague.adobe.com/en/docs/federated-audience-composition/using/home"  target="_blank">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Marketo Engage custom action</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now integrate Adobe Journey Optimizer with Adobe Marketo Engage to build your B2B use cases. From a journey, a new custom action allows you to ingest data into Marketo.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Improved channel configurations</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The current channel surface capabilities have been enhanced for a consistent approach across all channels. You can now define, manage, and reuse these configurations for any of your channels.</p>
<p><ul>
<li>Channel surfaces are now renamed to <strong>Channel configurations</strong></li>
<li>From the Channel configurations inventory you can now create reusable channel configurations for all channels, including now Web, In-app messaging, or Code-based experience</li>
<li>Object level access control (OLAC) is now available for each channel configuration, allowing you to decide which of your users are allowed to create or use specific configurations</li>
<li>For some channels, you can create channel configurations that target multiple platforms. An example here would be an In-app messaging channel configuration that can target a web page, an iOS app and an Android app.</li>
</ul></p>
<p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p>
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

**여정**

* (사용 가능: 7월 8일)이제 이벤트를 구성할 때 고급 표현식 편집기를 활용하여 이벤트 ID 조건에 보다 복잡한 표현식을 정의하거나 함수를 사용할 수 있습니다. [자세히 알아보기](../event/about-creating.md#adv-exp-editor)

<!--* The `event-id` condition is now automatically filled during test mode. -->

<!--**SMS channel**

* You can now modify existing SMS configurations.-->

**인앱 채널**

* 이제 인앱 채널에 표현식 조각을 사용할 수 있습니다.

**대상자**

* 이제 사용자 정의 업로드(CSV 파일)에서 가져온 대상자를 Privacy 및 Security Shield에도 사용할 수 있습니다.
<!--
**Push channel**

* You can now add your mobile application push credentials inside Adobe Journey Optimizer channel configuration settings. Creating an App surface in Adobe Experience Platform Data Collection is no longer required.-->
