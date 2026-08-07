---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer에 대한 사전 릴리스 정보
description: Adobe Journey Optimizer 사전 릴리스 정보
feature: Release Notes
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
hide: true
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2: id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
source-git-commit: fcf7ea6d5d6ceaa02490e8cbaf807b9f670c63cc
workflow-type: tm+mt
source-wordcount: 2157
ht-degree: 20%

---


# 사전 릴리스 정보 {#e-release-notes}

Adobe Journey Optimizer는 지속적으로 새로운 기능, 기존 기능 개선 및 버그 수정 사항을 제공합니다. 모든 변경 사항은 매월 말 [릴리스 정보](release-notes.md)에 통합됩니다.

## 2026년 8월 프리릴리스 정보 {#august-26-rn}

**아래 사전 릴리스 정보는 릴리스 공개 당일까지 사전 통지 없이 변경될 수 있습니다**. 링크, 스크린샷 및 업데이트된 설명서는 변경 사항이 프로덕션 환경에 적용된 후 게시됩니다. 대부분의 변경 사항은 릴리스 날짜에 전달되지만 일부는 나중에 롤아웃될 수 있습니다.

[Adobe Experience Platform 사전 릴리스 정보](https://experienceleague.adobe.com/ko/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}도 참조하십시오.

**릴리스 날짜**: 2026년 8월 18~19일

### 온보딩 {#august-26-onboarding}

이 릴리스의 온보딩에 다음 기능이 추가되었습니다.

<table>
<thead>
<tr>
<th><strong>이메일 및 여정 온보딩을 위한 안내 기능(일반 공급)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>다른 마케팅 플랫폼에서 Adobe Journey Optimizer으로 전환하면 기존 이메일 콘텐츠와 여정을 Journey Optimizer으로 이동하는 데 도움이 되는 안내 기능을 통해 더 쉽게 이동할 수 있습니다. 전용 작업 영역을 사용하면 처음부터 다시 빌드하는 대신 기존 작업 영역을 다시 사용할 수 있습니다.</p>
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15330">DOCAC-15330</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

### 여정 {#august-26-journeys}

이번 릴리스에서는 다음과 같은 기능 및 개선 사항이 여정에 추가되었습니다.

<table>
<thead>
<tr>
<th><strong>여정 수준 유지</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 여정 속성에서 직접 여정에 대한 홀드아웃 그룹을 구성할 수 있습니다. 홀드아웃은 여정 입력에서 제외되고 커뮤니케이션을 수신하지 않는 타겟 대상의 구성 가능한 백분율입니다. 홀드아웃 프로필을 Customer Journey Analytics 보고의 활성 프로필과 비교하여 여정이 제공하는 증분 상승도 - 실제 영향을 측정할 수 있습니다.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15162">DOCAC-15162</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **여정 표현식 편집기에 새 dateDiff 함수 추가** - 이제 여정 표현식 편집기에 두 날짜의 일 수 차이를 계산하는 `dateDiff` 함수가 포함됩니다. 이 기능은 기한 만들기, 고객 라이프사이클 기간 계산 또는 여정 조건에서 카운트다운 타이머 작성과 같은 시간 기반 논리에 유용합니다. <a href="https://jira.corp.adobe.com/browse/DOCAC-15293">DOCAC-15293</a> <!-- Documentation link: TBD -->

* **여정 헤더의 시작 및 종료 날짜** - 여정에 시작 및/또는 종료 날짜가 구성되면 상태 배지 옆의 여정 헤더에 표시됩니다. 표시되는 레이블은 각 날짜가 다가오는지 또는 이미 지났는지에 따라 달라집니다. <a href="https://jira.corp.adobe.com/browse/DOCAC-14702">DOCAC-14702</a> <!-- Documentation link: TBD -->

### 캠페인 {#august-26-camp}

이 릴리스의 캠페인에 다음과 같은 기능 및 개선 사항이 추가되었습니다.

<table>
<thead>
<tr>
<th><strong>액션 캠페인의 인바운드 경험 시뮬레이션</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 시작하기 전에 작업 캠페인에서 인바운드 채널 작업을 시뮬레이션할 수 있습니다. 시뮬레이션 모드를 사용하여 시뮬레이트된 사용자로 구성을 테스트하고 생성된 URL 및 QR 코드를 포함한 렌더링된 경험을 미리 보면 규칙, 의사 결정 및 컨텐츠 렌더링의 엔드 투 엔드를 확인할 수 있습니다.</p>
<p>이 기능은 현재 개인 베타 버전으로 제한된 조직 세트에서 사용할 수 있습니다. 더 많은 내용은 Adobe 담당자에게 문의하십시오.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15166">DOCAC-15166</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **캠페인용 폴더** - 이제 캠페인을 폴더로 구성하여 인터페이스에서 탐색 및 관리를 개선할 수 있습니다. <a href="https://jira.corp.adobe.com/browse/DOCAC-15098">DOCAC-15098</a> <!-- Documentation link: TBD -->

* **캠페인 대시보드의 브랜드 일관성 점수** - 이제 캠페인 대시보드에서 직접 브랜드 일관성 점수를 평가하여 콘텐츠가 브랜드에 부합하는지 확인할 수 있습니다. 이렇게 하면 콘텐츠 디자이너를 열지 않고도 가이드라인을 한눈에 검증할 수 있습니다. <a href="https://jira.corp.adobe.com/browse/DOCAC-14516">DOCAC-14516</a> <!-- Documentation link: TBD -->

* **캠페인의 기본 실행 필드 재정의** - 이전에는 여정 수준에서 사용할 수 있었던 기능이지만, 이제 캠페인 매개변수에서 이메일, SMS, WhatsApp 게재에 대해 전역으로 설정된 기본 실행 필드를 재정의할 수 있습니다. <a href="https://jira.corp.adobe.com/browse/DOCAC-14718">DOCAC-14718</a> <!-- Documentation link: TBD -->

### 오케스트레이션된 캠페인 {#august-26-oc}

이번 릴리스에서는 오케스트레이션된 캠페인에 다음과 같은 기능 및 개선 사항이 추가되었습니다.

<table>
<thead>
<tr>
<th><strong>오케스트레이션된 캠페인에 대한 Quiet Hours 지원</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 오케스트레이션된 캠페인에 조용한 시간을 적용할 수 있습니다. 자동 시간에는 특정 기간 동안 메시지가 전송되지 않도록 시간 기반 제외 항목을 정의할 수 있으므로, 캠페인 오케스트레이션 사용 사례 전반에서 고객 선호도 및 규정 준수 요구 사항을 준수할 수 있습니다.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14054">DOCAC-14054</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **프로필 대상 차원을 관리하는 기능** - 이제 프로필 대상 Dimension을 삭제하거나 구성된 ID 네임스페이스를 편집 및 교환하여 데이터 설정을 보다 유연하게 제어할 수 있습니다. <a href="https://jira.corp.adobe.com/browse/DOCAC-15018">DOCAC-15018</a> <!-- Documentation link: TBD -->

* **Line 지원(제한된 가용성)** - 이제 오케스트레이션된 캠페인에 직접 LINE 작업을 추가할 수 있습니다. 이 새로운 활동을 통해 텍스트, 스티커, 이미지, 비디오, 위치 데이터 및 풍부한 Flex 메시지를 비롯한 고도로 개인화된 콘텐츠를 구축 및 전달하여 LINE 플랫폼에서 고객을 원활하게 참여시킬 수 있습니다. 이 기능은 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오. <a href="https://jira.corp.adobe.com/browse/DOCAC-14905">DOCAC-14905</a> <!-- Documentation link: TBD -->

* **오케스트레이션된 새 캠페인 공개 API** - 이제 오케스트레이션된 캠페인에 새 API 사양을 사용할 수 있습니다. 이러한 API를 사용하면 오케스트레이션된 캠페인을 프로그래밍 방식으로 만들고, 관리하고, 트리거할 수 있으므로 외부 시스템 및 자동화 파이프라인과의 긴밀한 통합을 가능하게 합니다. <a href="https://jira.corp.adobe.com/browse/DOCAC-14308">DOCAC-14308</a> <!-- Documentation link: TBD -->

* **받는 사람 및 캠페인별로 전자 메일 보낸 사람 세부 정보 개인화** - 이제 오케스트레이션된 캠페인에서 프로필 특성 또는 관계 데이터를 사용하여 보낸 사람 이름, 보낸 사람 주소 및 회신 주소를 포함한 전자 메일 헤더 필드를 개인화할 수 있습니다. 이 작업을 통해 모든 발송물을 단일 회사 주소를 통해 보내는 대신, 발신자 세부 정보에 각 수신자에게 적합한 담당자, 위치 또는 지점을 반영할 수 있습니다. 헤더 값은 채널 수준에서 설정할 수 있으며, 세밀한 제어를 위해 컨텍스트 데이터를 사용하여 캠페인별로 재정의할 수 있습니다. <a href="https://jira.corp.adobe.com/browse/DOCAC-13761">DOCAC-13761</a> <!-- Documentation link: TBD -->

* **오케스트레이션된 캠페인의 대상 차원 단순화** - 이제 활성 타깃팅 차원이 워크플로우 캔버스에 표시되므로 채널 활동에서 사용하는 차원을 확인할 수 있습니다. 다중 엔티티 세분화 흐름은 더 이상 별도의 &quot;차원 변경&quot; 활동이 필요하지 않으므로 더 간단합니다. 또한 이제 메시지가 프로필 수준에서 전송되는지 또는 보조 차원 수준에서 전송되는지를 명시적으로 선택할 수 있습니다. <a href="https://jira.corp.adobe.com/browse/DOCAC-13554">DOCAC-13554</a> <!-- Documentation link: TBD -->

* **오케스트레이션된 캠페인에서 웨이브를 사용하여 보내기** - 이제 오케스트레이션된 캠페인의 아웃바운드 메시지를 시간에 따라 제어된 배치로 전달하도록 예약할 수 있습니다. 대량 또는 시간에 민감한 캠페인에 적합한 웨이브 전송은 더 나은 전달성을 지원하며, 스팸으로 플래그가 지정될 위험을 줄여 강력한 발신자 평판을 유지하는 데도 도움이 됩니다. <a href="https://jira.corp.adobe.com/browse/DOCAC-13990">DOCAC-13990</a> <!-- Documentation link: TBD -->

### 채널 {#august-26-channels}

이 릴리스의 채널에 다음과 같은 기능 및 개선 사항이 추가되었습니다.

<table>
<thead>
<tr>
<th><strong>웹 채널에서 의사 결정 지원</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 웹 채널에 의사 결정을 사용할 수 있습니다. 웹 시각적 편집기에서 직접 의사 결정 정책을 사용하여 각 방문자에게 가장 관련성이 높은 오퍼를 전달할 수 있습니다.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-11548">DOCAC-11548</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>API가 트리거된 이메일의 개인화된 PDF 첨부 파일</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer에서는 API 트리거 캠페인에서 이메일당 최대 5개의 수신자 특정 PDF를 첨부할 수 있습니다. PDF 파일은 데이터 랜딩 구역에서 안전하게 가져오고 전송 시 첨부되며 각 파일의 위치는 API 페이로드로 직접 전달됩니다. 이렇게 하면 Journey Optimizer에서 게재를 처리하면서 기존 업스트림 문서 생성 시스템이 제자리에 유지될 수 있습니다.</p>
<p>지원되는 사용 사례에는 송장, 명세서, 티켓, 계약서, 배송 라벨 및 수신자마다 다른 유사한 문서가 포함됩니다. 개인화된 PDF 첨부 파일은 API 트리거 캠페인에서만 사용할 수 있으며, 여정 또는 오케스트레이션된 캠페인에서는 지원되지 않습니다.</p>
<p>PDF 첨부 파일 추가 기능을 통해 더 큰 첨부 파일 볼륨 및 크기가 지원됩니다. 자세한 내용은 Adobe 담당자에게 문의하십시오.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15186">DOCAC-15186</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **LINE 채널 - 작성 기능 변경** - LINE 채널 UI가 고급 메시지 작성 기능으로 업그레이드되었습니다. 이 릴리스에서는 실시간 장치 미리 보기와 함께 텍스트, 이미지, 이미지 맵, 회전 메뉴 및 Flex(JSON 편집기)를 비롯한 여러 메시지 형식을 지원합니다. 이제 사용자는 최대 5개의 메시지로 구성된 그룹 메시지를 관리하고(추가, 제거 및 순서 변경 기능 포함) 통합된 개인화 편집기를 활용하여 검증된 동적 메시지를 보낼 수 있습니다. <a href="https://jira.corp.adobe.com/browse/DOCAC-14869">DOCAC-14869</a> <!-- Documentation link: TBD -->

* **처리량을 위한 성능 추가 기능 - 푸시** - API 트리거 캠페인에서 새로운 처리량 트랜잭션 메시지 모드를 사용할 수 있습니다. 이 모드는 대규모 실시간 트랜잭션 메시지 전송을 위해 설계되었으며 더 높은 가용성으로 초당 최대 5,000개의 트랜잭션을 지원합니다. 이전에는 이메일 채널에서만 사용할 수 있었지만, 이제 이 기능은 Adobe 고처리량 트랜잭션 메시지 추가 기능 서비스를 구입한 조직의 푸시 채널에서도 사용할 수 있습니다. 자세한 내용은 Adobe 담당자에게 문의하십시오. <a href="https://jira.corp.adobe.com/browse/DOCAC-14717">DOCAC-14717</a> <!-- Documentation link: TBD -->

### 결정 {#august-26-decisioning}

이 릴리스의 Decisioning에 다음과 같은 개선 사항이 추가되었습니다.

* **의사 결정의 배치 수준 빈도 제한** - 이제 의사 결정의 빈도 제한 규칙을 개별 배치로 지정할 수 있으므로 오퍼가 지정된 표면에 표시되는 빈도를 보다 세밀하게 제어할 수 있습니다. 두 가지 모드를 사용할 수 있습니다. 배치별 캡핑은 오퍼가 선택한 배치에 표시될 때만 적용되는 캡을 정의하고, 배치별 캡핑은 오퍼가 나타나는 모든 배치에 독립적으로 캡을 적용하므로 각 배치는 자체 캡핑 카운터를 유지합니다. 배치 관련 한도 설정은 Adobe Experience Platform 데이터 기반의 규칙을 사용하여 설정된 오퍼에는 적용되지 않습니다. <a href="https://jira.corp.adobe.com/browse/DOCAC-14980">DOCAC-14980</a> <!-- Documentation link: TBD -->

### 이메일 디자이너 {#august-26-email}

이 릴리스의 이메일 Designer에 다음과 같은 개선 사항이 추가되었습니다.

* **전자 메일 Designer의 새 테이블 구성 요소** - 이제 전자 메일 Designer에 기본 제공 테이블 구성 요소가 포함되어 있으므로 전자 메일 내에서 직접 행 및 열의 콘텐츠를 구성할 수 있습니다. 구성 요소를 캔버스에 드래그하여 놓고, 행과 열의 수를 사용자 정의하고, 각 셀의 스타일을 독립적으로 지정하여 사용자 지정 HTML에 의존하지 않고 명확하고 체계적인 레이아웃을 만듭니다. <a href="https://jira.corp.adobe.com/browse/DOCAC-15093">DOCAC-15093</a> <!-- Documentation link: TBD -->

### 관리 {#august-26-administration}

이 릴리스의 관리에 다음과 같은 개선 사항이 추가되었습니다.

* **사용자 지정 하위 도메인에 대한 피드백 루프 OTP 프로세스** - 제품 UI 내에서 Yahoo sender 허브 OTP(일회성 암호)를 직접 표시하여 피드백 루프(FBL) 사용자 지정 하위 도메인 구성 프로세스가 개선되었습니다. 이제 사용자는 Yahoo 발신자 허브 도메인 소유권 확인 중에 생성된 OTP를 자동으로 검색하고 표시할 수 있습니다. <a href="https://jira.corp.adobe.com/browse/DOCAC-14815">DOCAC-14815</a> <!-- Documentation link: TBD -->

### 사용성 개선 사항 {#august-26-usability}

이 릴리스의 사용성에 다음과 같은 개선 사항이 추가되었습니다.

* **콘텐츠 변형에 대한 새로운 콘텐츠 시뮬레이션 경험** - **콘텐츠 시뮬레이션** 워크플로에서는 새롭게 디자인된 경험을 도입했습니다. 이제 모든 변형을 한 번에 하나의 변형 보기를 대체하여 스크롤 가능한 그리드(나란히, 스택 또는 래핑된 레이아웃)에서 함께 렌더링합니다. 단일 하단 작업 표시줄은 테스트 변형 간 탐색, 확대/축소, 뷰포트 전환(데스크탑/모바일), 로케일 전환, 샘플 입력 추가, AI를 통한 변형 생성, 시뮬레이션된 사용자 선택 및 저장, 변형 가져오기 또는 내보내기를 통합합니다. 왼쪽 레일을 제거하고 추가 헤더 레이어를 축소하면 미리보기에 훨씬 더 많은 공간이 제공됩니다. 하단 작업 표시줄의 **클래식 경험으로 전환** 옵션을 사용하면 언제든지 이전 경험으로 되돌릴 수 있습니다. <a href="https://jira.corp.adobe.com/browse/DOCAC-15285">DOCAC-15285</a> <!-- Documentation link: TBD -->

* **여정 인벤토리의 대량 작업** - 이제 여정 인벤토리 목록에서 직접 새로운 대량 작업을 수행할 수 있으므로 여러 여정을 한 번에 더 빠르게 관리할 수 있습니다. 여러 여정을 선택하고 패키지에 추가, 삭제, 폴더로 이동, 태그 편집 또는 액세스 관리 등의 새 작업을 한 단계로 적용합니다. 이렇게 하면 한 번에 한 여정에 동일한 작업을 반복할 필요가 줄어들어 많은 여정으로 작업하는 팀의 여정 관리가 간소화됩니다. <a href="https://jira.corp.adobe.com/browse/DOCAC-15358">DOCAC-15358</a> <!-- Documentation link: TBD -->

<!--
## June '26 pre-release notes {#june-26-rn}

**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published once changes are live in production. While most changes are delivered on the release date, a few may roll out later — refer to the Availability Date listed for each entry for details.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Release date**: June 16-17, 2026

### Journeys {#june-26-journeys}

The following capabilities and improvements are coming to journeys in this release.

* **Increased live journey limit and new guardrails** - You can now have up to **200 active journeys**, increased from the previous limit of 100.



### Orchestrated campaigns {#june-26-oc}

The following capabilities and improvements are coming to orchestrated campaigns in this release.

-->

## 2026년 7월 프리릴리스 정보 {#july-26-rn}

**아래 사전 릴리스 정보는 릴리스 공개 당일까지 사전 통지 없이 변경될 수 있습니다**. 링크, 스크린샷 및 업데이트된 설명서는 변경 사항이 프로덕션 환경에 적용된 후 게시됩니다. 대부분의 변경 사항은 릴리스 날짜에 전달되지만 일부는 나중에 롤아웃될 수 있습니다.

[Adobe Experience Platform 사전 릴리스 정보](https://experienceleague.adobe.com/ko/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}도 참조하십시오.

**릴리스 날짜**: 2026년 7월 28~29일

<!--

### Onboarding {#july-26-onboarding}

Journey Optimizer introduces the Onboarding Assistant, a new capability in this release.

<table>
<thead>
<tr>
<th><strong>Onboarding Assistant</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Transitioning to Adobe Journey Optimizer from another marketing platform is easier with guided capabilities that help you move existing email content and journeys into Journey Optimizer. A dedicated workspace lets you reuse what you have instead of rebuilding from scratch.</p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<GIF placeholder: to be added>
<Documentation link: TBD>
</td>
</tr>
</tbody>
</table>

-->

### 여정 {#july-26-journeys}

이 릴리스의 여정에 다음과 같은 개선 사항이 추가되었습니다.


### 캠페인 {#july-26-campaigns}

이 릴리스의 캠페인에 다음과 같은 기능 및 개선 사항이 추가되었습니다.

<!--
<table>
<thead>
<tr>
<th><strong>Inbound experience simulation in Action campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now simulate inbound channel actions in Action campaigns before going live. Use simulation mode to test your configuration with simulated users and preview the rendered experience, including a generated URL and QR code, so you can validate rules, decisioning, and content rendering end-to-end.</p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
</td>
</tr>
</tbody>
</table>
-->

### 오케스트레이션된 캠페인 {#july-26-oc}

이 릴리스의 오케스트레이션된 캠페인에 다음과 같은 개선 사항이 추가되었습니다.

<!--

<table>
<thead>
<tr>
<th><strong>Quiet Hours support for orchestrated campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now apply quiet hours to Orchestrated campaigns. Quiet hours let you define time-based exclusions to prevent messages from being sent during specific periods, helping you respect customer preferences and compliance requirements across campaign orchestration use cases.</p>
<Documentation link: TBD>
</td>
</tr>
</tbody>
</table>

* **Ability to Manage Profile Target Dimensions** - You can now delete a Profile Target Dimension or edit and swap its configured identity namespace, providing greater control and flexibility over your data setups.

* **Support for Line** - You can now add LINE actions directly into your Orchestrated campaigns. This new activity allows you to build and deliver highly personalized content, including text, stickers, images, videos, location data, and rich Flex Messages, to engage your customers seamlessly on the LINE platform. This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.

* **New Orchestrated campaigns public APIs** - New API specifications are now available for Orchestrated campaigns. These APIs allow you to programmatically create, manage, and trigger orchestrated campaigns, enabling deeper integration with external systems and automation pipelines.

* **Personalize email sender details per recipient and campaign** - Orchestrated campaigns now support personalization of email header fields, including From name, From address, and Reply-To, using profile attributes or relational data. This allows sender details to reflect the relevant advisor, location, or branch for each recipient, rather than routing all sends through a single corporate address. Header values can be set at the channel level and overridden per campaign using contextual data for more precise control. Documentation link: TBD

* **Target dimension simplification in Orchestrated campaigns** - The active targeting dimension is now shown on the workflow canvas, so you can see which dimension is used by a channel activity. The multi-entity segmentation flow is simpler as you no longer need a separate "Change dimension" activity. Moreover, you can now choose explicitly whether messages are sent at the profile level or at a secondary dimension level.

* **Send messages in waves** - You can now schedule outbound messages from orchestrated campaigns to be delivered in controlled batches over time. Ideal for high-volume or time-sensitive campaigns, wave sending also supports better deliverability and helps maintain a strong sender reputation by reducing the risk of being flagged as spam.

-->

### 채널 {#july-26-channels}

이 릴리스의 채널에 다음과 같은 기능 및 개선 사항이 추가되었습니다.

### 결정 {#july-26-decisioning}

이 릴리스의 Decisioning에 다음과 같은 개선 사항이 추가되었습니다.

<!--
* **Placement-level frequency capping in Decisioning** - Frequency capping rules in Decisioning can now be scoped to individual placements, giving you finer control over how often an offer is shown in a given surface. Two modes are available: placement-specific capping (define a cap that applies only when the offer is displayed in a selected placement) and per-placement capping (apply a cap independently across every placement where the offer appears, so each placement maintains its own capping counter). Documentation link: TBD
-->

### 콘텐츠 관리 {#july-26-content}

이 릴리스의 콘텐츠 관리에 다음과 같은 개선 사항이 추가되었습니다.

<!--
### Integrations {#july-26-integrations}

The following improvements have been added to integrations in this release.

* **Real-time countdown timers for Adobe Experience Manager Dynamic Media integration** - Marketers can now build countdown timers as Dynamic Media templates in Adobe Experience Manager and pull them directly into Journey Optimizer. Timers render live at the moment of open, so every recipient sees an accurate countdown, not a static image. Configure dates, styling, and fallback values right within the Journey Optimizer editor to power flash sales and limited-time offers. [Documentation link: TBD]
-->

### 개인화 {#july-26-personalization}

이 릴리스의 개인화에 다음과 같은 개선 사항이 추가되었습니다.


### 이메일 디자이너 {#july-26-email}

이 릴리스의 이메일 채널에 다음 기능이 추가되었습니다.


### 관리 {#july-26-administration}

이 릴리스의 관리에 다음 기능이 추가되었습니다.


### 사용성 개선 사항 {#july-26-usability}

이번 릴리스에는 다음과 같은 사용 편의성 개선 사항이 적용되었습니다.

* **콘텐츠 템플릿의 SMS, 푸시, 인앱 및 Codebase 채널에 대한 빠른 실행 바로 가기** - 이제 콘텐츠 템플릿 목록의 **추가 작업** 단추에서 채널별 바로 가기를 추가로 사용할 수 있습니다. SMS 템플릿의 경우 메시지를 빠르게 편집하거나 문자 수/세그먼트를 확인합니다. 푸시 템플릿의 경우 제목, 본문 또는 미디어를 편집합니다. 인앱 템플릿의 경우 메시지 헤더, 메시지 본문 또는 미디어 URL을 편집합니다. 코드베이스 채널 템플릿의 경우 코드를 직접 편집합니다. 이러한 단축키는 이미 사용 가능한 이메일 채널 빠른 실행 단축키를 확장합니다. <!-- Documentation link: TBD -->
