---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer에 대한 사전 릴리스 정보
description: Adobe Journey Optimizer 사전 릴리스 정보
feature: Release Notes
hide: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2: id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
source-git-commit: ea1a283aacceafad32bd26560941a1bf613f3fea
workflow-type: tm+mt
source-wordcount: 2002
ht-degree: 10%

---


# 사전 릴리스 정보 {#e-release-notes}

Adobe Journey Optimizer은 새로운 기능, 기존 기능 개선 사항 및 버그 수정 사항을 지속적으로 제공합니다. 모든 변경 사항은 매월 말 [릴리스 정보](release-notes.md)에 통합됩니다.

## 2026년 6월 프리릴리스 정보 {#june-26-rn}

**아래 사전 릴리스 정보는 릴리스 공개 당일까지 사전 통지 없이 변경될 수 있습니다**. 변경 사항이 프로덕션에 배포되면 링크, 화면 및 업데이트된 설명서가 게시됩니다. 대부분의 변경 사항은 릴리스 날짜에 전달되지만 일부는 나중에 롤아웃될 수 있습니다. 자세한 내용은 각 항목에 대해 나열된 가용성 날짜를 참조하십시오.

[Adobe Experience Platform 사전 릴리스 정보](https://experienceleague.adobe.com/ko/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}도 참조하십시오.

**릴리스 날짜**: 2026년 6월 16~17일


### 여정 {#june-26-journeys}

이 릴리스의 여정은 다음과 같은 기능 및 개선 사항을 제공합니다.

<table>
<thead>
<tr>
<th><strong>여정 경로 최적화 - 타깃팅</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 <strong>활동 최적화</strong>에서 <strong>타깃팅 규칙</strong>을 지원합니다. 타깃팅 규칙을 사용하면 대상 세그먼트 또는 프로필 속성에 따라 고객이 특정 여정 경로에 대해 자격을 부여하기 위해 충족해야 하는 특정 기준을 정의할 수 있습니다.</p>
<p>고객을 경로에 무작위로 할당하는 실험과 달리 타깃팅에서는 결정론적 논리를 사용하여 적절한 대상 또는 고객 프로필이 의도한 경로로 라우팅되도록 합니다.</p>
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14720">DOCAC JIRA 작업 링크</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>여정 중재 - 공식</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 <strong>수식</strong>을 사용하여 고객 프로필 특성 및 컨텍스트 요인에 따라 자동으로 <strong>우선 순위 지정 및 중재</strong>할 수 있으므로 고객이 가장 관련성이 높은 여정을 입력하도록 할 수 있습니다.</p>
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14719">DOCAC JIRA 작업 링크</a></p>
</td>
</tr>
</tbody>
</table>

* **실시간 여정 제한 및 새 보호 기능 증가** - 이제 최대 **200개의 활성 여정을 사용할 수 있습니다**. 이전 제한인 100개에서 증가했습니다.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14826">DOCAC JIRA 작업에 연결</a>

* **여정 헤더의 시작 및 종료 날짜** - 시작 및/또는 종료 날짜가 라이브 여정에 구성되면 이제 라이브 상태 배지 옆의 **여정 헤더**에 표시됩니다. 표시된 레이블은 각 날짜가 예정된 날짜인지 또는 이미 지난 날짜인지에 따라 조정됩니다.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14702">DOCAC JIRA 작업에 연결</a>

* **일시 중지된 여정을 직접 중지하거나 닫을 수 있습니다** - 이제 **일시 중지됨** 상태에서 **여정을 중지하거나 새 출구로 닫을 수 있습니다**. 이전에는 일시 중지된 여정을 중단하거나 닫으려면 먼저 라이브로 다시 시작해야 했습니다.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14229">DOCAC JIRA 작업에 연결</a>

* **외부 대상에 대한 보조 식별자 지원** - 이제 CSV 파일에서 가져온 대상과 Federated Audience Composition으로 만든 대상을 포함하여 외부 대상에 대해 여정의 보조 식별자가 지원됩니다. 대상자의 모든 비ID 속성 또는 비개인 ID 속성을 보조 ID로 지정할 수 있으며, 스키마 레이블 지정은 필요하지 않습니다.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14541">DOCAC JIRA 작업에 연결</a>

### 오케스트레이션된 캠페인 {#june-26-oc}

이 릴리스의 오케스트레이션된 캠페인에는 다음과 같은 기능 및 개선 사항이 적용됩니다.

<table>
<thead>
<tr>
<th><strong>오케스트레이션된 캠페인에서 파일 활동 로드</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 오케스트레이션된 캠페인은 파일을 Adobe Experience Platform으로 먼저 수집하지 않고도 <strong>CSV 또는 TXT 파일</strong>을 타깃팅 대상자로 캠페인 캔버스에 직접 로드할 수 있습니다. 파일 데이터는 실행 시 사용되며 Adobe Experience Platform 데이터 세트로 지속되지 않습니다. 파일 설정 중에 열 매핑, 데이터 유형, NULL 처리 및 열별 오류 정책을 정의할 수 있습니다. 전체 수집 파이프라인 구축이 실용적이지 않은 임시 전송 또는 파트너 목록 캠페인을 지원합니다.</p>
<p>이 기능은 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14704">DOCAC JIRA 작업 링크</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>오케스트레이션된 캠페인에 대한 Quiet Hours 지원</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 오케스트레이션된 캠페인에 <strong>조용한 시간</strong>을 적용할 수 있습니다. 방해 금지 모드를 사용하면 특정 기간 동안 메시지가 전송되지 않도록 <strong>시간 기반 제외</strong>를 정의할 수 있으므로, 캠페인 오케스트레이션 사용 사례에서 고객 환경 설정 및 준수 요구 사항을 준수하는 데 도움이 됩니다.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14054">DOCAC JIRA 작업 링크</a></p>
</td>
</tr>
</tbody>
</table>

* **오케스트레이션된 캠페인의 관계형 데이터에 대한 루프 기반 개인화** - 이제 개인화 편집기는 주문, 계정 또는 예약과 같은 관계형 컬렉션을 반복하고 단일 전자 메일 또는 SMS 내에서 레코드당 하나의 콘텐츠 블록을 렌더링하는 **루프 블록**을 지원합니다. 컬렉션은 표현식 쓰기가 필요하지 않고 개인화 토큰을 사용하여 데이터 선택기를 통해 구성됩니다.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14703">DOCAC JIRA 작업에 연결</a>

* **받는 사람 및 캠페인별 전자 메일 보낸 사람 세부 정보 개인화** - 이제 오케스트레이션된 캠페인이 프로필 특성 또는 관계 데이터를 사용하여 보낸 사람 이름, 보낸 사람 주소 및 회신 주소를 포함한 **전자 메일 머리글 필드**의 개인화를 지원합니다. 이를 통해 보낸 사람의 세부 정보가 하나의 회사 주소를 통해 모든 전송을 라우팅하는 대신 각 받는 사람에 대한 관련 조언자, 위치 또는 분기를 반영할 수 있습니다. 헤더 값은 채널 수준에서 설정할 수 있으며 보다 정밀한 제어를 위해 컨텍스트 데이터를 사용하여 캠페인별로 재정의할 수 있습니다.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13761">DOCAC JIRA 작업에 연결</a>

* **오케스트레이션된 캠페인의 차원 단순화** - 이제 활성 **타깃팅 차원**이 워크플로 캔버스에 표시되므로 채널 활동에서 사용하는 차원을 확인할 수 있습니다. 다중 엔티티 세분화 흐름은 더 이상 별도의 &quot;차원 변경&quot; 활동이 필요하지 않으므로 더 간단합니다. 또한 이제 메시지가 프로필 수준에서 전송되는지 또는 보조 차원 수준에서 전송되는지를 명시적으로 선택할 수 있습니다.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13554">DOCAC JIRA 작업에 연결</a>

* **캠페인의 기본 실행 필드 재정의** - 이전에는 여정 수준에서 사용할 수 있었지만, 이제 캠페인 매개 변수에서 이메일, SMS 및 WhatsApp 게재에 대해 전역적으로 설정된 기본 **실행 필드**을(를) 재정의할 수 있습니다.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14718">DOCAC JIRA 작업에 연결</a>

### 결정 {#june-26-decisioning}

이 릴리스에서는 다음 기능이 의사 결정 기능으로 제공됩니다.

<table>
<thead>
<tr>
<th><strong>Decisioning에서 Adobe Experience Manager 콘텐츠 조각 활용</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Decisioning의 <strong>결정 항목</strong>에 <strong>Adobe Experience Manager 콘텐츠 조각</strong>을(를) 매핑하고 결정 정책 내에서 활용하여 적절한 시기에 적절한 고객에게 적절한 조각을 전달할 수 있습니다.</p>
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14885">DOCAC JIRA 작업 링크</a></p>
</td>
</tr>
</tbody>
</table>

### 이메일 채널 {#june-26-email}

이 릴리스의 이메일 채널에는 다음과 같은 기능 및 개선 사항이 적용됩니다.

<table>
<thead>
<tr>
<th><strong>고급 구성 요소 - 레이아웃 (수퍼 구성 요소)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 전자 메일 Designer에 머리글, 제품 카드(1, 2 또는 3열), 정보 블록 및 바닥글과 같은 <strong>바로 사용할 수 있는 레이아웃 구성 요소 라이브러리</strong>가 포함되어 있으므로 전자 메일 캔버스로 바로 끌어서 놓을 수 있습니다. 각 구성 요소는 편집 가능한 속성(이미지, 제목, 텍스트, 버튼, 링크)으로 사전 구성되어 있으며 WYSIWYG 인터페이스를 통해 완전히 맞춤화할 수 있으므로 처음부터 구조를 빌드하지 않고도 이메일 작성 시간을 단축할 수 있습니다.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14877">DOCAC JIRA 작업 링크</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>이메일 Designer에서 컨텐츠 확인</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer을 통해 사용자는 이메일 Designer 인터페이스 내에서 직접 <strong>가독성, 효율성 및 콘텐츠 응집성을 포함한 이메일 콘텐츠 품질</strong>을 확인할 수 있습니다.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14870">DOCAC JIRA 작업 링크</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>이메일 크기 감소 활성화</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이 새 옵션을 사용하면 전자 메일의 모양을 변경하지 않고도 불필요한 공백, 주석 및 중복 코드를 제거하여 전자 메일의 <strong>HTML 크기를 줄일 수 있습니다</strong>. 이렇게 하면 게재 능력을 향상시키고(일부 이메일 공급자는 크기 초과된 이메일을 거부하거나 플래그를 지정) 수신자의 로드 시간을 단축할 수 있습니다.</p>
<p>사용 가능한 날짜: 2026년 6월 10일</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14777">DOCAC JIRA 작업 링크</a></p>
</td>
</tr>
</tbody>
</table>

* **조각의 텍스트 모드 지원** - 이제 텍스트 기반 이메일 워크플로를 지원하기 위해 해당 조각을 포함하는 일반 텍스트 버전의 이메일에 최적의 사용을 위해 시각적 조각의 **텍스트 버전**을 만들고 관리할 수 있습니다. 현재 릴리스 전에 생성된 조각을 사용하는 경우 조각 텍스트 버전이 이메일 Designer 및 수신자에게 전달된 최종 이메일 모두에서 잘못 렌더링될 수 있습니다. 이전 조각을 사용하여 최상의 결과를 얻으려면 각 조각을 편집, 저장 및 다시 게시하십시오.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14204">DOCAC JIRA 작업에 연결</a>

* **고객 응대 시나리오를 사용한 일괄 전송 처리량 벤치마크 업데이트됨** - Adobe Journey Optimizer의 **일괄 전송 처리량 벤치마크**는 조건부 논리를 사용하는 기본 전송부터 복잡한 동적 콘텐츠까지 여러 개인화 시나리오에서 프로덕션 수준의 성능을 반영하도록 업데이트되었습니다. 이제 고객이 메시지 볼륨을 정확하게 계획하는 데 도움이 되도록 제품 설명서에서 새로 고친 지표를 사용할 수 있습니다.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14816">DOCAC JIRA 작업에 연결</a>

* **사용자 지정 하위 도메인에 대한 피드백 루프 OTP 프로세스** - 제품 UI 내에서 Yahoo 보낸 사람 허브 **OTP(일회용 암호)**를 직접 표시하여 FBL(피드백 루프) 사용자 지정 하위 도메인 구성 프로세스가 개선되었습니다. 이제 사용자는 Yahoo 발신자 허브 도메인 소유권 확인 중에 생성된 OTP를 자동으로 검색하고 표시할 수 있습니다.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14815">DOCAC JIRA 작업에 연결</a>

### 모바일 메시징(SMS, MMS, RCS 및 LINE) {#june-26-mobile}

이 릴리스의 모바일 메시징에는 다음과 같은 개선 사항이 적용되었습니다.

* **SMS 보고서에 대한 고유 클릭 수** - 새로운 **고유 클릭 수** 모듈이 SMS 보고서에 도입되어 현재 이메일 보고서에 사용할 수 있는 SMS에 동일한 수준의 세분화된 성능 추적을 제공합니다.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14895">DOCAC JIRA 작업에 연결</a>

* **LINE 채널 - 변경 내용 작성** - LINE 채널 UI가 고급 메시지 작성 기능으로 업그레이드되었습니다. 이 릴리스에서는 실시간 장치 미리 보기와 함께 텍스트, 이미지, 이미지 맵, 회전판 및 Flex(JSON 편집기)를 비롯한 **여러 메시지 형식**에 대한 지원이 도입되었습니다. 이제 사용자는 최대 5개의 순서가 지정된 메시지로 구성된 그룹화된 메시지를 관리하고(추가, 제거 및 순서 조정 컨트롤 포함), 검증된 다이내믹 메시징을 위해 통합 개인화 편집기를 활용할 수 있습니다.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14869">DOCAC JIRA 작업에 연결</a>

* **SMS - 사용 지표 표시** - Adobe Journey Optimizer을 통해 SMS를 직접 구매하는 고객의 경우 새 **SMS 사용 대시보드**가 도입되었습니다. 이제 MO(Mobile Originated) 및 MT(Mobile Terminated) 메시지로 분류된 최근 90일 간의 메시지 전송 지표를 보고 추적할 수 있습니다. 이 데이터는 CSV를 통해서도 다운로드할 수 있으므로 SMS 소비에 대한 가시성과 제어 능력이 향상됩니다.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14345">DOCAC JIRA 작업에 연결</a>

### 컨텐츠 및 통합 {#june-26-content}

이 릴리스의 콘텐츠 관리 및 통합에 대해 다음과 같은 기능 및 개선 사항이 적용되었습니다.

<table>
<thead>
<tr>
<th><strong>Adobe Experience Manager을 사용한 컨텐츠 조각</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이번 릴리스에서는 Adobe Experience Manager 작성 워크플로 내에서 <strong>Journey Optimizer 콘텐츠 조각</strong>을(를) 더 사용 가능하고, 더 관리 가능하며, 더 프로덕션 환경에서 사용할 수 있도록 하는 몇 가지 개선 사항이 제공됩니다.</p>
<ul>
<li>Journey Optimizer은 이제 작성자, 게시 및 인증된 게시 계층을 포함하여 여러 Adobe Experience Manager 구성에서 콘텐츠 조각 가져오기를 지원합니다.</li>
<li>조각을 선택하면 해당 컨텍스트가 메시지 전체에 유지되므로 작성자가 다시 선택하지 않고도 콘텐츠 블록 간 조각 필드를 재사용할 수 있습니다.</li>
<li>라이프사이클 관리를 개선하기 위해 새로운 전용 콘텐츠 조각 목록 페이지가 Journey Optimizer에 도입되었습니다. 사용자는 동기화 중단 조각을 식별하고 수동 동기화를 트리거하여 최신 상태를 유지할 수 있습니다.</li>
<li>이제 로케일 및 변형 지원을 통해 마케터는 보다 의도적으로 동일한 콘텐츠 조각의 대체 버전을 사용하여 작업할 수 있습니다.</li>
</ul>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14686">DOCAC JIRA 작업 링크</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Adobe Experience Manager 저장소 구성</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Adobe Journey Optimizer에서 Adobe Experience Manager 콘텐츠에 액세스하는 방법을 유연하게 사용할 수 있습니다. 이 릴리스에서는 여정 및 캠페인에 사용된 콘텐츠 조각에 대해 <strong>소스 리포지토리를 전환</strong>하는 기능을 도입했습니다.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14684">DOCAC JIRA 작업 링크</a></p>
</td>
</tr>
</tbody>
</table>

* **기본 Adobe Experience Manager 콘텐츠 조각(Managed Services) 통합** - 이제 **Managed Services**과(와) 호환되며, 개인화를 위해 Journey Optimizer에서 직접 Adobe Experience Manager 콘텐츠 조각을 보고, 액세스하고, 사용할 수 있습니다. 구성 설정에 Adobe Experience Manager Managed Services 저장소 URL을 1회 설정으로 추가하기만 하면 됩니다.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14821">DOCAC JIRA 작업에 연결</a>

* **Adobe Experience Manager Asset Essentials와 AI Assistant 통합** - 이제 이메일, 웹 페이지 및 푸시 알림을 생성할 때 AI Assistant가 Adobe Experience Manager Assets에서 직접 **브랜드 승인 이미지**를 자동으로 가져옵니다. 이렇게 하면 Assets을 수동으로 검색하거나 일반 AI 폴백에 의존할 필요가 없어 모든 시각적 요소가 완벽하게 정확하고 브랜드 규정을 준수하도록 할 수 있습니다.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14761">DOCAC JIRA 작업에 연결</a>

### 사용자 지정 채널 {#june-26-channels}

이 릴리스의 채널에는 다음과 같은 기능이 제공됩니다.

<table>
<thead>
<tr>
<th><strong>사용자 지정 아웃바운드 채널</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer은 이제 관리자가 <strong>코드 없는 채널 빌더</strong>를 통해 직접 AJO으로 WeChat, Kakao Talk, Messenger 또는 독점 공급자와 같은 아웃바운드 HTTP 기반 메시징 채널을 가져올 수 있는 새로운 기능인 <strong>사용자 지정 채널</strong>을 도입했습니다. 구성하고 나면 캠페인, 여정 및 오케스트레이션된 캠페인에서 기본 채널과 동일한 전체 기능 세트를 사용하여 사용자 정의 채널을 사용할 수 있습니다. 표현식 편집기를 사용한 개인화, 콘텐츠 실험, 미리보기 및 증명, 즉시 사용 가능한 보고, 동의 및 거버넌스 적용. 이렇게 하면 이전에 여정으로 제한되고 전용 콘텐츠 작성이 부족했던 사용자 지정 작업에서 다루었던 간격이 채워집니다.</p>
<p>이 기능은 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-11381">DOCAC JIRA 작업 링크</a></p>
</td>
</tr>
</tbody>
</table>

### 보고 {#june-26-reporting}

이번 릴리스에서는 다음과 같은 개선 사항이 보고되었습니다.

* **이메일 및 SMS 보고에 대한 새로운 예상 클릭 메트릭** - 실제 고객 참여를 보다 정확하게 파악할 수 있도록 여정, 캠페인 및 채널 보고서에서 새로운 예상 메트릭을 사용할 수 있습니다. 이러한 지표는 보고 데이터에서 비인적 상호 작용(NHI) 및 보트 클릭을 필터링하는 데 도움이 됩니다.
   * 예상 클릭 수: 식별된 봇 및 비사람 트래픽을 제거한 후 카운트된 총 클릭 수입니다.
   * 예상 CTR: 총 게재와 관련된 예상 클릭 수입니다.
   * 이메일에 대한 예상 CTOR 전용: 예상 열람에 대한 예상 클릭수.

  <a href="https://jira.corp.adobe.com/browse/DOCAC-14354">DOCAC JIRA 작업에 연결</a>

### 구성 {#june-26-configuration}

이 릴리스의 구성 및 관리에는 다음과 같은 개선 사항이 적용됩니다.

* **AJO 랜딩 페이지의 웹 응용 프로그램 방화벽(WAF) IP 허용 목록** - Adobe Journey Optimizer은 이제 랜딩 페이지의 **웹 응용 프로그램 방화벽(WAF) IP 허용 목록**을 지원하므로 조직에서 구성된 WAF 인프라를 통해서만 모든 수신 요청이 라우팅되도록 할 수 있습니다. 이 향상된 기능을 통해 고객은 WAF 계층을 무시하는 직접 요청을 거부하도록 AJO을 구성할 수 있으므로 Imperva와 같은 도구에 정의된 보안 정책이 일관되게 적용됩니다. 이 기능은 엄격한 네트워크 액세스 요구 사항을 가진 기업의 보안 태세를 강화하여 AJO이 호스팅하는 랜딩 페이지로의 트래픽 흐름을 완벽하게 제어합니다.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14814">DOCAC JIRA 작업에 연결</a>

* **스트리밍에서 일괄 처리 모드로 데이터 세트 이동** - AJO 메시지 피드백 이벤트 데이터 세트가 스트리밍에서 **일괄 처리 수집 모드**(으)로 전환됩니다. 이 변경 사항은 데이터 수집이 스트리밍 수집 제한을 초과하지 않도록 합니다. Customer Journey Analytics 보고서에서 이 데이터 세트를 사용하거나 이에 대한 쿼리를 실행하는 경우 향후 최대 2시간의 데이터 지연 증가가 예상됩니다.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14771">DOCAC JIRA 작업에 연결</a>

### 유용성 개선 {#june-26-usability}

이번 릴리스에서는 다음과 같은 사용 편의성 개선 사항이 적용되었습니다.

* **여정 및 캠페인용 폴더** - 이제 인터페이스 탐색 및 관리를 개선하기 위해 여정 및 캠페인을 **폴더**로 구성할 수 있습니다.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14038">DOCAC JIRA 작업에 연결</a>

