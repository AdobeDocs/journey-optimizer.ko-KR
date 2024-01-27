---
solution: Journey Optimizer
product: journey optimizer
title: 릴리스 정보
description: Journey Optimizer 초기 릴리스 정보
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: fae367cbbacffbbecde4cdbf7b39b1baeec452d1
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 20%

---

# 초기 릴리스 정보 {#e-release-notes}

[!DNL Adobe Journey Optimizer]는 지속적으로 새로운 기능, 기존 기능 개선, 버그 해결을 제공합니다. 모든 변경 사항은 매달 마지막 주 [릴리스 정보](release-notes.md)에 통합됩니다.

아래 초기 릴리스 정보는 릴리스를 사용할 수 있는 당일까지 사전 통지 없이 변경될 수 있습니다. 링크, 화면, 업데이트된 설명서는 릴리스 날짜의 [릴리스 정보](release-notes.md)에 게시됩니다.

## 2024년 1월 초기 릴리스 정보 {#oct-jan-2024}

**릴리스 날짜**: 2024년 1월 30~31일

### 새로운 기능{#jan-2024-features}

이번 릴리스에는 아래 목록에 있는 새로운 기능이 제공됩니다.


<table>
<thead>
<tr>
<th><strong>게재 기능 업데이트</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer에서 DMARC 인증 기술을 지원합니다.</p>
<p>2024년 2월 1일부터 Google 및 Yahoo! 은(는) 이메일을 보내는 데 사용하는 모든 도메인에 대한 DMARC 레코드가 있어야 합니다. Journey Optimizer에서 Adobe에게 위임했거나 위임하고 있는 모든 하위 도메인에 대해 DMARC 레코드가 설정되어 있는지 확인하십시오.</p>
<!--img src="assets/channel-reports.png"/-->
<p>자세한 내용은 <a href="../configuration/dmarc-record-update.md">자세한 설명서</a>를 참조하세요.</p>
</tr>
</tbody>
</table>



### 개선 사항 {#jan-2024-improvements}

이 릴리스는 아래 목록에 있는 개선 사항과 함께 제공됩니다.

**보고**

* **도메인별 채널 보고서** - Campaign 및 여정 보고서를 개선하기 위해 새 위젯이 추가되었습니다. 다음 **도메인별 바운스 이유**, **도메인에서 전송 및 전달**, **도메인별 열기 및 클릭 수** 및 **도메인별 바운스 및 오류** 위젯은 도메인 수준에서 주요 이메일 게재 및 추적 지표에 대한 세부 분류를 제공합니다.

**SMS 채널**

* **이중 옵트인** - SMS에 대한 이중 옵트인 워크플로우를 사용하면 장치에서 요청을 시작할 때 사용자가 메시지를 수신하도록 명시적으로 옵트인할 수 있습니다. 사용자는 인바운드 SMS 메시지를 전송하여 동의 프로세스를 시작합니다. 동의를 확인하면 최종 확인을 요청하는 후속 메시지가 발송된다. 사용자 프로필이 존재하지 않으면 확인 후 생성됩니다.

  이는 Sinch 및 Infobip SMS 공급자에만 적용됩니다.

**여정**

* **반응 이벤트 기간** - 다음에서 정의할 수 있는 최대 기간 **반응 이벤트** 는 현재 30일이 아니라 29일입니다.

* **날짜 필터** - 이제 미리 정의된 기존 날짜 필터 외에 사용자 지정 날짜를 사용하여 여정 인벤토리를 필터링할 수 있습니다. 이렇게 하면 특정 날짜, 특정 달 내, 전체 연도 또는 지정된 시간 범위에 게시된 여정을 표시하여 목록을 세분화할 수 있습니다.

* **대상자 읽기**  - 이제 대상자 읽기 활동은 예약된 일별 일괄 처리 작업이 실행된 후 하루에 한 번만 생성되는 일괄 처리 세그먼트에 대한 프로필 스냅샷 데이터 세트를 사용합니다.

**빈도 규칙**

* **주별 및 일별 빈도 상한** - 이제 월별 외에 일주일 또는 하루 단위로 고객 프로필에 전송되는 최대 메시지 수를 지정할 수 있습니다. 주파수 캡은 선택된 캘린더 기간에 기초하고 대응하는 시간 프레임의 시작에서 리셋된다.


**의사 결정 관리**

* **에지에서 주파수 캡처** - 이제 빈도 제한 카운터가 업데이트되어 Edge Decisioning API 의사 결정에서 3초 이내에 사용할 수 있습니다.