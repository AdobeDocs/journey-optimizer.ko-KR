---
solution: Journey Optimizer
product: journey optimizer
title: 릴리스 정보
description: Journey Optimizer 초기 릴리스 정보
hide: true
hidefromtoc: true
source-git-commit: 1bf010b247b3683c6171bc387c9b94ab1b5dcefc
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 23%

---

# 초기 릴리스 정보 {#e-release-notes}

[!DNL Adobe Journey Optimizer]는 지속적으로 새로운 기능, 기존 기능 개선, 버그 해결을 제공합니다. 모든 변경 사항은 매달 마지막 주 [릴리스 정보](release-notes.md)에 통합됩니다.

아래 초기 릴리스 정보는 릴리스를 사용할 수 있는 당일까지 사전 통지 없이 변경될 수 있습니다. 링크, 화면, 업데이트된 설명서는 릴리스 날짜의 [릴리스 정보](release-notes.md)에 게시됩니다.

## 2023년 9월 초기 릴리스 정보 {#sept-rn-2023}

**릴리스 날짜**: 2023년 9월 26~27일

### 새로운 기능{#sept-2023-features}

이번 릴리스에는 아래 목록에 있는 새로운 기능이 제공됩니다.


<table>
<thead>
<tr>
<th><strong>통합 채널 보고서</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>채널 보고서 기능은 분석가와 마케터에게 채널 수준의 트래픽 및 참여 지표에 대한 포괄적인 개요를 제공합니다. '보고서' 메뉴에 액세스하려면 '채널 보고서 보기' 권한이 있어야 합니다.</p>
<img src="assets/channel-reports.png"/>
<!--p>For more information, refer to the <a href="../in-app/get-started-in-app.md">detailed documentation</a>.</p-->
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>데이터 세트 내보내기 대상(GA)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 클라우드 스토리지 대상으로 Journey Optimizer 데이터 세트 내보내기를 일반적으로 사용할 수 있습니다. 이제 클라우드 스토리지 위치와 실시간 연결을 설정하여 데이터 세트의 콘텐츠를 내보낼 수 있습니다.</p>
<img src="../data/assets/dataset-export-setup.png">
<!--p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>샌드박스당 모바일 애플리케이션 자격 증명 저장소</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이 새로운 기능을 사용하면 푸시 자격 증명을 앱 표면의 전용 샌드박스와 쉽게 관리하고 연결할 수 있습니다.</p>
<p>자세한 내용은 <a href="../in-app/inapp-configuration.md">자세한 설명서</a>를 참조하세요.</p>
</tr>
</tbody>
</table>

### 개선 사항 {#sept-2023-improvements}

이 릴리스는 아래 목록에 있는 개선 사항과 함께 제공됩니다.

<!--**Audiences**

* You can now target audiences uploaded from a CSV file into journeys and campaigns.
* You can now target audiences resulting from composition workflows into journeys. -->

**개인화**

* 이제 시각적 조각 외에도 표현식 편집기를 통해 Journey Optimizer 인터페이스에서 표현식 조각을 만들고, 저장하고, 다시 사용할 수 있습니다. 표현식 조각은 이전에 저장된 표현식을 대체합니다.
* 이제 Journey Optimizer의 개인화에 Adobe Experience Platform 계산된 속성을 사용할 수 있습니다. 계산된 속성은 Adobe Experience Platform에 수집된 프로필 사용 경험 이벤트 데이터 세트를 기반으로 계산되는 집계된 값입니다.

**경고**

* 새로운 유형의 시스템 경고가 도입되었습니다. 이제 대상자 읽기가 실패하면 알림을 받을 수 있습니다.

**웹 채널**

* 이제 웹 디자이너 비주얼 편집기에서 SPA(단일 페이지 애플리케이션)을 작성할 수 있습니다. 이제 웹 페이지 수정 사항을 적용할 특정 보기를 선택할 수 있습니다. 보기는 전체 사이트 또는 홈 페이지, 전체 제품 사이트 또는 모든 체크아웃 페이지의 게재 환경 설정 프레임과 같은 사이트의 시각적 요소 그룹으로 정의할 수 있습니다. Adobe Experience Platform Web SDK 구현에서 보기를 정의하려면 일회용 개발자 설정이 필요합니다. 이렇게 하면 마케터는 SPA에서 Adobe Journey Optimizer 웹 캠페인을 만들고 실행할 수 있습니다.

* 이제 웹 디자이너를 사용하여 페이지를 편집할 때 **수정 사항** 창 - 디자이너 인터페이스에서 구성 요소를 선택하고 편집할 필요 없이
* 이제 웹 하위 도메인을 설정할 때 Adobe으로 이미 위임된 하위 도메인을 사용할 수 있을 뿐만 아니라 고유한 하위 도메인을 추가할 수 있는 옵션이 제공됩니다.

**여정**

* 이제 사용자 지정 작업 응답에 대한 지원이 GA됩니다. 이렇게 하면 사용자 지정 작업에서 API 호출 응답을 활용하고, 이러한 응답을 기반으로 여정을 오케스트레이션할 수 있습니다. 또한 모든 통관 조치를 엔드포인트당 호출 수 5000회로 제한하는 가드레일이 새로 추가되었습니다.
* 이제 여정을 복제할 때 여정 사본의 이름을 정의할 수 있습니다.

<!--
* The maximum duration that you can define in the Wait activity is now 29 days instead of 30.
-->

**이메일 채널**

이메일 표면 구성의 새 옵션을 사용하면 이메일 주소가 Adobe Journey Optimizer 제외 목록에 있는 경우에도 프로필에 트랜잭션 메시지를 보내도록 선택할 수 있습니다.

**SMS 채널**

두 개의 새 필드, **옵트인 메시지** 및 **도움말 메시지**&#x200B;가 API 구성 화면에 추가되어 사용자가 인바운드 키워드에 대한 응답을 사용자 지정할 수 있습니다. Sinch SMS 공급자만 사용할 수 있습니다.

**보고**

이제 Journey Optimizer 보고서를 CSV 파일로 내보낼 수 있습니다. [자세히 알아보기](../reports/global-report.md#export-reports)

<!--**Decision management**

Enhancements have been made to the audience picker in journeys or campaigns, with the addition of new columns displaying the origin and update frequency of audiences.    -->