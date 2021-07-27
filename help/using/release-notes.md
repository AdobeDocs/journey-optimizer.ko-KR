---
title: 릴리스 정보
description: Journey Optimizer 릴리스 정보
source-git-commit: 4d3352184aac7fe19096c21650982e29506f2bff
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 24%

---


# 릴리스 정보 {#release-notes}

이 페이지에는 Journey Orchestration의 새로운 기능과 개선 사항을 모두 나열합니다.
최신 [설명서 업데이트](documentation-updates.md)도 확인할 수 있습니다.

## 2021년 7월 릴리스 {#july-2021-release}

<table>
<thead>
<tr>
<th><strong>스키마 관계 활용</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform을 사용하면 한 데이터 세트를 다른 데이터 세트에 대한 조회 테이블로 사용하기 위해 스키마 간의 관계를 정의할 수 있습니다. 이제 Journey Optimizer은 연결된 스키마에서 가져온 데이터를 활용할 수 있습니다.</p>
<p>이러한 필드는 단일 이벤트 구성, 여정 조건, 메시지 개인화 및 사용자 지정 작업 개인화에서 사용할 수 있습니다.</p>
<p>자세한 내용은 <a href="event/experience-event-schema.md#leverage_schema_relationships">자세한 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>허용 목록</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 테스트 환경에서 수신자에게 원치 않는 이메일을 보내지 않도록 샌드박스 수준에서 특정 전송 안전 목록을 정의할 수 있습니다.
</p>
<p>자세한 내용은 <a href="allow-list.md">자세한 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>

### 개선 사항

* 동일한 샌드박스에서 동시에 실행되는 모든 읽기 세그먼트의 전체 전송률은 초당 17,000개의 메시지로 제한됩니다. [자세히 보기](building-journeys/read-segment.md#configuring-segment-trigger-activity)
* **캐시 기간** 필드가 데이터 소스 구성 창에서 제거되었습니다. [자세히 보기](datasource/about-data-sources.md)
* 이제 외부 데이터 소스의 경우 초당 15개의 호출의 최대 가용량 규칙이 자동으로 정의됩니다. [자세히 보기](configuration/external-systems.md#capping)
* 이제 라이브 여정의 경우 여정 속성 화면에 게시 날짜와 여정을 게시한 사용자의 이름이 표시됩니다. [자세히 보기](building-journeys/journey-gs.md#change-properties)
* 여정 목록 화면에서 여정 유형 필터가 추가되었습니다. [자세히 보기](user-interface.md#section_lgm_hpz_pgb)
* [!UICONTROL Throttling rate] 매개 변수가 세그먼트 읽기 활동에 추가되었습니다. [자세히 보기](building-journeys/read-segment.md#configuring-segment-trigger-activity)
