---
solution: Journey Optimizer
product: journey optimizer
title: 릴리스 정보
description: Journey Optimizer 초기 릴리스 정보
hide: true
hidefromtoc: true
source-git-commit: 36634fc3993261756c081e71c47e7408c77c65ae
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 41%

---

# 초기 릴리스 정보 {#e-release-notes}

[!DNL Adobe Journey Optimizer]는 지속적으로 새로운 기능, 기존 기능 개선, 버그 해결을 제공합니다. 모든 변경 사항은 매달 마지막 주 [릴리스 정보](release-notes.md)에 통합됩니다.

아래 초기 릴리스 정보는 릴리스를 사용할 수 있는 당일까지 사전 통지 없이 변경될 수 있습니다. 링크, 화면, 업데이트된 설명서는 릴리스 날짜의 [릴리스 정보](release-notes.md)에 게시됩니다.

## 2023년 8월 초기 릴리스 정보 {#aug-rn-2023}

**릴리스 날짜**: 2023년 8월 23~24일

### 새로운 기능{#aug-2023-features}

이번 릴리스에는 아래 목록에 있는 새로운 기능이 제공됩니다.

<table>
<thead>
<tr>
<th><strong>여정의 인앱 채널</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 여정 내에서 앱 사용자에게 개인화된 인앱 메시지를 보낼 수 있습니다. Journey Optimizer를 사용하여 알림을 디자인하고 메시지 레이아웃, 디스플레이, 텍스트, 버튼을 사용자 정의하여 원활한 경험을 만들 수 있습니다.</p>
<img src="assets/in_app_journey_1.png"/>
<p>자세한 내용은 <a href="../in-app/get-started-in-app.md">세부 설명서</a>를 참조하십시오.</p>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>시드 목록을 사용하여 이메일 유효성 검사</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer에서 시드 목록을 만들고 관리할 수 있습니다. 시드 목록은 실제 대상자에게 보내기 전에 전자 메일을 보내는 테스트 전자 메일 주소로 구성됩니다. 이 기능을 사용하여 전송된 이메일 복사본을 모니터링하고 모든 표시 형식, URL, 이미지 및 링크가 올바른지 확인하십시오.</p>
<img src="../configuration/assets/seed-list-details.png">
<!--p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>텍스트 및 이미지용 콘텐츠 지원</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>메시지를 만들고 개인화했으면 콘텐츠 도우미를 통해 콘텐츠를 한 단계 더 발전시킵니다. 이제 콘텐츠 도우미를 사용하여 다양한 주요 제목과 이미지를 실험하여 메시지의 영향을 최적화할 수 있습니다. 각 변형은 더 많은 클릭을 효과적으로 생성하는 제목을 측정하고 비교하기 위해 고유한 처리로 관리됩니다.</p>
<img src="assets/gen-ai-image-2.png"/>
<!--p>For more information, refer to the <a href="../start/search-filter-categorize.md#tags">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>



### 개선 사항 {#aug-2023-improvements}

이 릴리스는 아래 목록에 있는 개선 사항과 함께 제공됩니다.

**API**

이제 콘텐츠 조각을 만들고 관리하기 위한 새 API를 사용할 수 있습니다. [자세히 알아보기](https://developer.adobe.com/journey-optimizer-apis/references/content-templates/#tag/Content-fragment-API){target="_blank"}.

**이메일 채널**

* 트랜잭션 메시지 대상자에 스팸 불만으로 인해 억제된 이메일 주소를 포함하는 새로운 옵션을 이메일 표면 설정에서 사용할 수 있습니다. 마케팅 메시지를 스팸으로 표시했더라도 이러한 프로필은 암호 재설정 또는 계정 구문과 같은 트랜잭션 메시지를 받을 수 있습니다. 이 옵션은 기본적으로 비활성화되어 있습니다.

**여정**

* 이제 사용자 정의 작업에 API 호출 응답을 활용하고, 이 응답을 기반으로 여정을 오케스트레이션할 수 있습니다.
* 새로운 유형의 시스템 경고가 도입되었습니다. 이제 사용자 정의 작업이 실패하면 알림을 받을 수 있습니다.
