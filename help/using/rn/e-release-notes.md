---
solution: Journey Optimizer
product: journey optimizer
title: 릴리스 정보
description: Journey Optimizer 초기 릴리스 정보
feature: Release Notes
topic: Content Management
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
hide: true
hidefromtoc: true
source-git-commit: f957737aa741cc8b854912414d15154489d1b0b0
workflow-type: ht
source-wordcount: '311'
ht-degree: 100%

---

# 초기 릴리스 정보 {#e-release-notes}

[!DNL Adobe Journey Optimizer]는 지속적으로 새로운 기능, 기존 기능 개선, 버그 해결을 제공합니다. 모든 변경 사항은 매월 말 [릴리스 정보](release-notes.md)에 통합됩니다.

아래 초기 릴리스 정보는 릴리스를 사용할 수 있는 당일까지 사전 통지 없이 변경될 수 있습니다. 링크, 화면, 업데이트된 설명서는 릴리스 날짜의 [릴리스 정보](release-notes.md)에 게시됩니다.

## 2024년 3월 초기 릴리스 정보 {#e-2024}

**릴리스 날짜**: 2024년 3월 19~20일

### 새로운 기능 {#e-features}

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

### 개선 사항 {#e-improvements}

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

여정이 중간 상태일 때는 읽기 전용입니다.