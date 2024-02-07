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
source-git-commit: 97967e8043df9b75d3120e4a7bfccff700f5d57f
workflow-type: ht
source-wordcount: '558'
ht-degree: 100%

---

# 초기 릴리스 정보 {#e-release-notes}

[!DNL Adobe Journey Optimizer]는 지속적으로 새로운 기능, 기존 기능 개선, 버그 해결을 제공합니다. 모든 변경 사항은 매달 마지막 주 [릴리스 정보](release-notes.md)에 통합됩니다.

아래 초기 릴리스 정보는 릴리스를 사용할 수 있는 당일까지 사전 통지 없이 변경될 수 있습니다. 링크, 화면, 업데이트된 설명서는 릴리스 날짜의 [릴리스 정보](release-notes.md)에 게시됩니다.

## 2024년 1월 초기 릴리스 정보 {#e-2024}

**릴리스 날짜**: 2024년 1월 20~31일

### 새로운 기능{#e-features}

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
<!--img src="assets/channel-reports.png"/-->
<p>자세한 내용은 <a href="../configuration/dmarc-record.md">세부 설명서</a>를 참고하십시오.</p>
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
<p>Real-Time CDP 및 Journey Optimizer의 산업별 사용 사례 플레이북 카탈로그를 활용하여 Adobe Experience Platform 및 Adobe Journey Optimiser를 사용하여 수행할 수 있는 일반적인 사용 사례를 해결합니다.</p><p>요구 사항에 가장 적합한 플레이북을 선택하면 여정, 메시지, 스키마 또는 세그먼트와 같은 사용 사례를 지원하는 데 필요한 자산을 생성하고, 가치 창출 시간을 단축하기 위해 스키마에 맞게 사용자 지정할 수 있습니다.</p>
<br/><img src="assets/do-not-localize/playbooks.gif"/>
<!--<p>For more information, refer to the <a href="../start/playbooks.md">detailed documentation</a>.</p>-->
</tr>
</tbody>
</table>

### 개선 사항 {#e-improvements}

이 릴리스는 아래 목록에 있는 개선 사항과 함께 제공됩니다.

**보고**

* **새 도메인 기반 분류 위젯** - 캠페인 및 여정 보고서를 개선하기 위해 새 위젯이 추가되었습니다. **도메인별 바운스 이유**, **도메인에서 전송 및 전달**, **도메인별 열기 및 클릭 수** 및 **도메인별 바운스 및 오류** 위젯은 도메인 수준에서 주요 이메일 게재 및 추적 지표에 대한 세부 분류를 제공합니다. [자세히 알아보기](../reports/channel-report.md)

**SMS 채널**

* **이중 옵트인** - SMS에 대한 이중 옵트인 워크플로우를 사용하면 장치에서 요청을 시작할 때 사용자가 메시지를 수신하도록 명시적으로 옵트인할 수 있습니다. 사용자는 인바운드 SMS 메시지를 전송하여 동의 프로세스를 시작합니다. 동의를 확인하면 최종 확인을 요청하는 후속 메시지가 발송됩니다. 사용자 프로필이 존재하지 않으면 확인 후 생성됩니다. [자세히 알아보기](../sms/sms-configuration.md#create-api)

  이는 Sinch 및 Infobip SMS 공급자에만 적용됩니다.

**여정**

* **반응 이벤트 기간** - **반응 이벤트**&#x200B;에서 정의할 수 있는 최대 기간은 이제 30일이 아니라 29일입니다. [자세히 알아보기](../building-journeys/reaction-events.md)

<!--* **Date filters** - You can now use custom dates to filter the journeys inventory, in addition to the existing predefined date filters. This allows you to refine the list by displaying journeys published on a specific date, within a particular month, throughout an entire year, or within specified time ranges. [Learn more](../building-journeys/journey-gs.md#filter)-->

* **대상자 읽기**  - 이제 대상자 읽기 활동은 예약된 일별 배치 작업이 실행된 후 하루에 한 번만 생성되는 배치 세그먼트에 대한 프로필 스냅샷 데이터 세트를 사용하므로 데이터는 마지막 일별 배치 작업까지 새로 고쳐집니다.

* **필드 그룹** - 특정 경우에 저장할 필드 그룹을 차단하는 문제를 수정했습니다.

* **표현식 편집기** - 이제 모든 표현식과 추가 함수에서 listObject 데이터 유형을 지원합니다. [추가 정보](../building-journeys/expression/functions.md)

**빈도 규칙**

* **주별 및 일별 빈도 상한** - 이제 월별 외에 일주일 또는 하루 단위로 고객 프로필에 전송되는 최대 메시지 수를 지정할 수 있습니다. 빈도 캡은 선택된 캘린더 기간에 기반하고 대응하는 시간대가 시작될 때 재설정됩니다. [자세히 알아보기](../configuration/frequency-rules.md#create-new-rule)

**의사 결정 관리**

* **Edge 빈도 설정** - 이제 빈도 설정 카운터가 업데이트되었으므로 Edge Decisioning API 결정에서 3초 이내에 사용할 수 있습니다.