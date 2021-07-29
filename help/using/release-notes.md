---
title: 릴리스 정보
description: Journey Optimizer 릴리스 정보
source-git-commit: cd38b6ec9be0417f5c65e37805c0e7b072d1cb96
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 16%

---


# 릴리스 정보 {#release-notes}

이 페이지에는 [!DNL Journey Optimizer]의 새로운 기능과 개선 사항이 모두 포함되어 있습니다. 최신 [설명서 업데이트](documentation-updates.md)도 확인할 수 있습니다.

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
<p>Adobe Experience Platform을 사용하면 한 데이터 세트를 다른 데이터 세트에 대한 조회 테이블로 사용하기 위해 스키마 간의 관계를 정의할 수 있습니다. 이제 [!DNL Journey Optimizer]은 연결된 스키마에서 가져온 데이터를 활용할 수 있습니다.</p>
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
<p>이제 테스트 목적으로 안전한 환경을 갖도록 샌드박스 수준에서 특정 전송 안전 목록을 정의할 수 있습니다. 허용 목록이 실수가 발생할 수 있는 비프로덕션 인스턴스에서 고객에게 원치 않는 메시지를 보낼 위험이 없습니다. 이 기능은 억제 API를 활용하여 활성화됩니다.</p>
<p>자세한 내용은 <a href="allow-list.md">자세한 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>

### 개선 사항

* **여정**
   * 동일한 샌드박스에서 동시에 실행되는 모든 읽기 세그먼트의 전체 전송률은 초당 17,000개의 메시지로 제한됩니다. [자세히 보기](building-journeys/read-segment.md#configuring-segment-trigger-activity)
   * **캐시 기간** 필드가 데이터 소스 구성 창에서 제거되었습니다. [자세히 보기](datasource/about-data-sources.md)
   * 이제 외부 데이터 소스의 경우 초당 15개의 호출의 최대 가용량 규칙이 자동으로 정의됩니다. [자세히 보기](configuration/external-systems.md#capping)
   * 이제 라이브 여정의 경우 여정 속성 화면에 게시 날짜와 여정을 게시한 사용자의 이름이 표시됩니다. [자세히 보기](building-journeys/journey-gs.md#change-properties)
   * 여정 목록 화면에서 여정 유형 필터가 추가되었습니다. [자세히 보기](user-interface.md#section_lgm_hpz_pgb)
   * **[!UICONTROL Throttling rate]** 매개 변수가 세그먼트 읽기 활동에 추가되었습니다. [자세히 보기](building-journeys/read-segment.md#configuring-segment-trigger-activity)

* **미리 보기 및 테스트**
   * 이제 ID 및 네임스페이스가 **[!UICONTROL Preview]** 화면에 표시됩니다. [자세히 보기](preview.md#preview-your-messages)
   * 이제 증명을 위한 테스트 전자 메일 수가 10개로 제한됩니다.
   * 이제 증명에서 **제목 줄 접두사**&#x200B;에 사용할 수 있는 문자가 제한됩니다. [자세히 보기](preview.md#send-proofs)

* **개인화 표현식 편집기**
   * 도우미 드롭다운 목록의 이름이 변경되고 순서가 변경되었습니다.

### 수정 사항

* 배치 이메일 게재에 대해 중복 메시지가 전달되는 문제를 해결했습니다.
* 이제 다시 시도 기간이 끝나면 이메일 전송이 수행되지 않을 때 그에 따라 이벤트가 생성됩니다.
* PTR Records 화면에서 IP 정보가 누락되는 문제를 해결했습니다.
* 이제 표현식 편집기 내의 오퍼 레일의 현지화가 구현되었습니다.
* 정보 팝업에서 잘못된 간격이 수정되었습니다.
