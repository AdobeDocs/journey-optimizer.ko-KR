---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer에 대한 사전 릴리스 정보
description: Adobe Journey Optimizer 사전 릴리스 정보
hide: true
feature: Release Notes
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
subfeature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
source-git-commit: d1dbd15068b0af7af0acc3e8ebd68cd1d3db3bbb
workflow-type: tm+mt
source-wordcount: 1928
ht-degree: 19%

---


# 사전 릴리스 정보 {#e-release-notes}

Adobe Journey Optimizer는 지속적으로 새로운 기능, 기존 기능 개선 및 버그 수정 사항을 제공합니다. 모든 변경 사항은 매월 말 [릴리스 정보](release-notes.md)에 통합됩니다.

## 2026년 9월 프리릴리스 정보 {#sep-26-rn}

**아래 사전 릴리스 정보는 릴리스 공개 당일까지 사전 통지 없이 변경될 수 있습니다**. 링크, 스크린샷 및 업데이트된 설명서는 변경 사항이 프로덕션 환경에 적용된 후 게시됩니다. 대부분의 변경 사항은 릴리스 날짜에 제공되지만, 일부는 나중에 배포될 수 있습니다. 자세한 내용은 각 항목에 명시된 제공 예정일을 참조하세요.

[Adobe Experience Platform 사전 릴리스 정보](https://experienceleague.adobe.com/ko/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}도 참조하십시오.

**릴리스 날짜**: 2026년 9월 22~23일

### 콘텐츠 관리 {#sep-26-content-management}

이 릴리스에서는 다음 기능이 콘텐츠 관리에 적용됩니다.

<table>
<thead>
<tr>
<th><strong>CX Coworker의 메시지 복사 및 이메일 디자인 플러그인</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 CX Coworker에서 전략에서 배포에 이르기까지 <strong>메시징 및 이메일 워크플로</strong>를 간소화하는 두 가지 새로운 플러그인을 사용할 수 있습니다.</p>
<p><strong>메시지 복사 플러그 인</strong>:</p>
<ul>
<li>캠페인 브리핑을 캡처하고 메시지 맵, 내러티브 아크 및 채널 역할을 정의합니다.</li>
<li>채널, 터치포인트, 로케일, 대상자 및 변형에 맞게 구성된 다차원 콘텐츠 매트릭스를 구축합니다.</li>
<li>완전히 새로운 사본을 만들고 Adobe Firefly을 활용하여 캠페인 비주얼을 생성, 자르기 및 조정합니다.</li>
<li>즉석 콘텐츠 평가를 허용하고 승인된 에셋을 다시 Journey Optimizer, Adobe Campaign V8 및 Marketo으로 직접 동기화할 수 있습니다.</li>
</ul>
<p><strong>전자 메일 디자인 플러그 인</strong>:</p>
<ul>
<li>마케팅 목표, 참조 스크린샷 또는 Figma 디자인 링크를 사용자 지정 레이아웃 계획 및 프로덕션 준비 이메일 HTML으로 변환합니다.</li>
<li>재사용 가능한 브랜드 자산, 디자인 토큰 및 구조적 이메일 템플릿을 관리합니다.</li>
<li>기업 규정 준수, 시각적 디자인 품질 및 WCAG 2.1 AA 접근성 표준에 대해 조립된 이메일 코드를 감사합니다.</li>
<li>승인된 HTML을 Adobe Journey Optimizer 및 Adobe Campaign으로 직접 내보냅니다.</li>
</ul>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

### 충성도 {#sep-26-loyalty}

이 릴리스에서는 다음과 같은 기능 및 개선 사항이 충성도에 적용됩니다.

<table>
<thead>
<tr>
<th><strong>과제 기회</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>충성도 성능 메뉴에는 이제 계층 진행 마찰 또는 과제 작업 드롭오프와 같이 AI가 감지한 트렌드와 차이를 예상되는 영향과 한 번의 클릭으로 "AI로 만들기" 작업을 통해 해결하는 문제를 생성하는 <strong>기회 탭</strong>이 포함됩니다.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>충성도 이벤트 매핑 업데이트</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 이벤트 매핑 생성 또는 편집에서는 새로운 **시각적 매핑 빌더**&#x200B;를 사용합니다. 스키마를 선택하고, 검색 가능한 필드 선택기에서 필드를 선택하고, 각 필드를 행별 연결 상태가 있는 충성도 이벤트 필드에 매핑하고, 언제든지 수동 JSONata 편집으로 전환하는 옵션과 함께 자동 생성된 JSONata 표현식을 미리 봅니다.</p><p>또한 충성도 관리자의 "이벤트 정의"가 사람이 읽을 수 있는 Experience 이벤트 스키마 이름을 보여 주는 목록 보기가 새로 고쳐진 상태로 "이벤트 매핑"으로 이름이 변경되었습니다.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **CX 동료의 충성도 추천 기술** - 마케터는 이제 CX 동료의 대화 인터페이스에서 직접 **도전 기회**&#x200B;를 요청할 수 있으며, 실제 충성도 프로그램 트렌드를 기반으로 기본적인 도전 아이디어를 얻고 채팅 중단 없이 실시간 도전으로 전환할 수 있습니다. <!-- Documentation link: TBD -->

### 온보딩 {#sep-26-onboarding}

이 릴리스에서는 다음 기능이 온보딩됩니다.

<table>
<thead>
<tr>
<th><strong>이메일 및 여정 온보딩을 위한 안내 기능(일반 공급)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>기존 이메일 콘텐츠와 여정을 Journey Optimizer로 마이그레이션하는 데 도움이 되는 안내형 기능을 통해 다른 마케팅 플랫폼에서 Adobe Journey Optimizer로의 전환이 더욱 쉬워졌습니다. <strong>전용 작업 영역</strong>을 사용하면 처음부터 다시 빌드하는 대신 기존 작업 영역을 다시 사용할 수 있습니다.</p>
<p>이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성).</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

### 여정 {#sep-26-journeys}

이번 릴리스에서는 다음과 같은 기능 및 개선 사항이 여정에 추가됩니다.

<table>
<thead>
<tr>
<th><strong>CX Coworker의 여정 시뮬레이션(MCP &amp; Chat)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>CX Coworker의 <strong>여정 시뮬레이션 기술</strong>은(는) 엔드 투 엔드 여정 유효성 검사를 자동화하고 결과를 쉽게 해석할 수 있도록 해줍니다. 이 기능은 현재 빠른 시뮬레이션 흐름만 지원하며 Journey Optimizer 수동 시뮬레이션 경험을 완전히 대체하지는 않습니다.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>CX Coworker 레일에서 여정 생성</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 CX Coworker 오른쪽 레일에서 AI를 사용하여 <strong>여정을 만들 수 있습니다. </strong>은(는) 이전 AI Assistant 경험을 여정 생성을 위한 브랜드 변경 및 통합 진입점으로 대체합니다.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* Decisioning의 Optimize 활동의 일부인 **여정 시뮬레이션의 Decisioning 경로 실험** - **경로 실험**&#x200B;이(가) 이제 여정 시뮬레이션에서 지원됩니다. <!-- Documentation link: TBD -->

* **여정 시뮬레이션에서 보조 ID 지원** - **보조 ID**&#x200B;이(가) 이제 여정 시뮬레이션에서 지원되므로 읽기 대상 및 이벤트가 트리거된 여정 모두에 대해 복잡한 사용자 시나리오를 테스트할 수 있습니다. <!-- Documentation link: TBD -->

* **세분화된 일괄 처리 대상 평가 대기 논리** - **대상 읽기 활동**&#x200B;에서 여정의 &quot;일괄 처리 대상 평가 후 트리거&quot; 옵션은 이제 일괄 처리 세그먼테이션이 이미 진행 중이고 활성화된 일괄 처리가 이전 실행에서 사용된 것과 다른 경우에만 새 대상 평가를 대기하므로 기다릴 필요가 없는 여정에 대한 불필요한 지연을 방지할 수 있습니다. <!-- Documentation link: TBD -->

### 채널 {#sep-26-channels}

이 릴리스의 채널에는 다음과 같은 기능 및 개선 사항이 적용됩니다.

<table>
<thead>
<tr>
<th><strong>Android 라이브 업데이트를 위한 라이브 활동</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer은 <strong>라이브 활동 지원을 Android</strong>(으)로 확장하여 실시간 모바일 개인화 기능을 확장합니다. 주문 추적, 비행 상태, 라이브 이벤트 업데이트 및 실시간 스포츠 점수와 같은 실시간 진행 상황 업데이트를 사용자에게 직접 제공할 수 있습니다.</p>
<p>이제 iOS 라이브 활동을 지원하는 것 외에도 Journey Optimizer은 플랫폼 구성에서 Android 라이브 업데이트에 대한 임시 푸시 토큰을 관리합니다. API 트리거 캠페인 및 Headless API를 사용하여 브로드캐스트 및 트랜잭션 업데이트 흐름을 모두 지원합니다.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>사용자 지정 아웃바운드 채널(일반 가용성)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>사용자 지정 아웃바운드 채널</strong>을 통해 관리자는 WeChat, Kakao Talk, Messenger 또는 독점 공급자와 같은 아웃바운드 HTTP 기반 메시징 채널을 코드 없는 채널 빌더를 통해 직접 Journey Optimizer으로 가져올 수 있습니다. 구성이 완료되면 사용자 정의 채널은 캠페인, 여정 및 오케스트레이션된 캠페인 전체에서 사용할 수 있으며, 표현식 편집기를 사용한 개인화, 콘텐츠 실험, 미리보기 및 교정쇄, 기본 제공 보고서, 동의 및 거버넌스 시행 등 기본 채널과 동일한 모든 기능을 제공합니다.</p>
<p>이번 릴리스를 통해 사용자 지정 아웃바운드 채널에는 다음과 같은 몇 가지 새로운 기능도 있습니다.</p>
<ul>
<li>코드 기반 경험과 동일한 방식으로 Personalization 편집기를 통해 사용자 지정 채널 페이로드에서 Journey Optimizer Decisioning을 사용합니다.</li>
<li>기본 채널에서 이미 수행할 수 있는 것과 동일한 방식으로 비즈니스 규칙을 사용자 지정 채널에 적용합니다.</li>
<li>API 트리거 캠페인에 대한 채널 목록에서 이전에 가능하지 않았던 사용자 지정 채널을 선택합니다.</li>
<li>사용자 지정 채널에 대한 보고 웹후크를 정의하고 채널 구성에 연결하므로 상호 작용 이벤트로 Journey Optimizer 보고서를 보강할 수 있습니다.</li>
</ul>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>여정의 대상 채널</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Adobe Journey Optimizer에는 여정 캔버스에 새 <strong>대상 노드</strong>가 포함되어 있어 Adobe Experience Platform Real-Time CDP 및 Journey Optimizer 공동 고객이 여정 내에서 직접 Facebook 및 Google과 같은 외부 유료 미디어 대상에 프로필을 추가하거나 제거할 수 있습니다.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **사용자 지정 SMS BYOP 인증 유연성** - 이제 SMS 공급자의 OAuth 설정에 연결할 때 보내는 메시지에 토큰을 배치하는 위치와 토큰 요청 자체의 형식을 포함하여 **사용자 지정 인증 헤더**&#x200B;를 구성할 수 있습니다. <!-- Documentation link: TBD -->

### 오케스트레이션된 캠페인 {#sep-26-oc}

이번 릴리스에서는 오케스트레이션된 캠페인에 다음과 같은 기능 및 개선 사항이 추가됩니다.

<table>
<thead>
<tr>
<th><strong>OR 조인 활동</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>AND-Join 활동이 일반 <strong>Join 활동</strong>(으)로 업그레이드되어 AND와 OR 조인 조건 중에서 선택할 수 있습니다.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>오케스트레이션된 캠페인 경고</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 오케스트레이션된 캠페인이 캠페인에 실패하거나, 정의된 임계값보다 오래 실행되거나, 활동 수준 오류가 발생할 때 중요 알림을 포함한 <strong>실시간 경고</strong>를 지원하므로 마케터는 캠페인이 완료될 때까지 기다리지 않고 문제를 포착하고 해결할 수 있습니다.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **LINE 지원** - 이제 오케스트레이션된 캠페인에 **LINE 작업**&#x200B;을 바로 추가할 수 있습니다. 이 새로운 활동을 통해 텍스트, 스티커, 이미지, 비디오, 위치 데이터 및 풍부한 Flex 메시지를 포함한 고도로 개인화된 콘텐츠를 제작하고 전달하여 LINE 플랫폼에서 고객과 원활하게 소통할 수 있습니다. 이전에 제한된 가용성으로 릴리스된 이 기능은 이제 모든 환경에서 사용할 수 있습니다(일반 가용성). <!-- Documentation link: TBD -->

* **오케스트레이션된 새 캠페인 모니터링 API** - 이제 오케스트레이션된 캠페인에 새 **API 사양**&#x200B;을 사용할 수 있습니다. 이를 통해 오케스트레이션된 캠페인을 프로그래밍 방식으로 만들고, 관리하고, 트리거할 수 있으므로 외부 시스템 및 자동화 파이프라인과의 긴밀한 통합을 지원합니다. <!-- Documentation link: TBD -->

### 캠페인 {#sep-26-campaigns}

이 릴리스의 캠페인에는 다음과 같은 기능 및 개선 사항이 적용되었습니다.

<table>
<thead>
<tr>
<th><strong>액션 캠페인의 인바운드 경험 시뮬레이션(Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 액션 캠페인을 실제 운영하기 전에 인바운드 채널 액션을 시뮬레이션할 수 있습니다. 시뮬레이션 모드를 사용하여 시뮬레이션 사용자로 구성을 테스트하고 생성된 URL 및 QR 코드를 포함한 렌더링된 환경을 미리 볼 수 있으므로 규칙, 의사 결정, 콘텐츠 렌더링을 처음부터 끝까지 검증할 수 있습니다.</p>
<p>이 기능은 현재 Private Beta 버전으로 일부 조직에서만 사용할 수 있습니다. 더 많은 내용은 Adobe 담당자에게 문의하세요.</p>
</td>
</tr>
</tbody>
</table>

* **캠페인용 폴더** - 이제 캠페인을 **폴더**(으)로 구성하여 인터페이스에서 탐색 및 관리를 개선할 수 있습니다. <!-- Documentation link: TBD -->

### 결정 {#sep-26-decisioning}

이번 릴리스에서는 다음과 같은 기능 및 개선 사항이 결정에 추가됩니다.

<table>
<thead>
<tr>
<th><strong>웹 채널에서 의사 결정 지원</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 웹 채널에서도 결정 기능을 사용할 수 있습니다. 웹 시각화 편집기에서 직접 결정 정책을 사용하여 각 방문자에게 가장 관련성이 높은 오퍼를 제공할 수 있습니다.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **CX Coworker의 의사 결정 규칙 생성** - 이전에는 오른쪽 레일을 통해 사용할 수 있었던 **AI 지원 의사 결정 규칙 생성** 환경에 이제 CX Coworker를 통해 액세스할 수 있습니다. 이 환경은 AI로 규칙을 작성하는 방법으로 오른쪽 레일을 대체합니다. <!-- Documentation link: TBD -->

### 이메일 디자이너 {#sep-26-email-designer}

이 릴리스의 이메일 Designer에는 다음과 같은 기능 및 개선 사항이 적용되었습니다.

<table>
<thead>
<tr>
<th><strong>이메일 테마 변형을 위한 독립적인 다크 모드 스타일</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 이메일 테마가 어두운 모드를 위한 독립적인 스타일을 지원합니다. 테마 빌더에서 특정 변형에 대해 어두운 모드를 켜서 밝은 모드 스타일과 별도로 편집하는 전용 어두운 모드 스타일시트를 생성할 수 있습니다. 한 모드에서 변경한 사항이 다른 모드를 더 이상 덮어쓰지 않습니다. 이메일 및 템플릿 편집기에서 데스크탑 및 모바일 보기 옵션 옆에 새로운 미리보기 토글을 사용하면 어두운 모드로 콘텐츠를 미리 볼 수 있습니다.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>이메일 Designer의 PSD 파일에서 직접 Dynamic Media 템플릿 가져오기</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이메일 Designer의 Dynamic Media 구성 요소를 사용하면 기존 Dynamic Media 템플릿을 검색할 뿐만 아니라 Photoshop(PSD) 파일을 새 템플릿으로 바로 가져올 수 있습니다. PSD 파일을 구성 요소로 끌어다 놓으면 Adobe Journey Optimizer이 자동으로 Dynamic Media에 저장된 Dynamic Media 템플릿으로 전환합니다. 수동 전환이나 Adobe Experience Manager을 통한 왕복 작업은 필요하지 않습니다. 가져온 후에는 내장된 Dynamic Media 편집기를 사용하여 템플릿을 편집할 수 있습니다. 이는 이메일 Designer의 Adobe Express 콘텐츠에 사용된 것과 동일한 경험입니다.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>이메일 Designer의 새 테이블 구성 요소</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Email Designer에 기본 제공 <strong>테이블 구성 요소</strong>가 포함되어 있으므로 전자 메일 내에서 직접 행과 열로 콘텐츠를 구성할 수 있습니다. 구성 요소를 캔버스에 드래그하여 놓고, 행과 열의 수를 사용자 정의하고, 각 셀의 스타일을 독립적으로 지정하여 사용자 지정 HTML에 의존하지 않고 명확하고 체계적인 레이아웃을 만듭니다.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **전자 메일 테마의 사용자 지정 글꼴에 대한 대체 글꼴** - 이제 전자 메일 테마를 통해 적용된 모든 사용자 지정(웹) 글꼴에 대한 대체 글꼴을 정의할 수 있습니다. 가입자의 이메일 클라이언트가 사용자 정의 글꼴을 지원하지 않는 경우 Adobe Journey Optimizer은 이메일 클라이언트의 기본값으로 선택을 유지하는 대신 지정된 대체 글꼴을 자동으로 표시합니다. 이렇게 하면 이메일 타이포그래피를 브랜드 지침에 더 가깝게 유지할 수 있으며 이메일 클라이언트 간의 글꼴 렌더링 불일치를 줄일 수 있습니다. <!-- Documentation link: TBD -->

### 관리 {#sep-26-administration}

이 릴리스에서는 다음과 같은 개선 사항이 적용되었습니다.

* **사용자 지정 하위 도메인에 대한 피드백 루프 OTP 프로세스** - 제품 UI 내에서 Yahoo 보낸 사람 허브 **OTP(일회용 암호)**&#x200B;를 직접 표시하여 FBL(피드백 루프) 사용자 지정 하위 도메인 구성 프로세스가 개선되었습니다. 이제 사용자는 Yahoo 발신자 허브 도메인 소유권 확인 중에 생성된 OTP를 자동으로 검색하고 표시할 수 있습니다. <!-- Documentation link: TBD -->

### 사용성 개선 사항 {#sep-26-usability}

* **콘텐츠 시뮬레이션 경험의 유용성 개선** - 이제 새로운 콘텐츠 시뮬레이션 경험을 통해 손쉽게 비교할 수 있도록 변형의 이름을 지정하고 구성하며, 각 카드에서 직접 변형 세부 정보를 복사하거나 삭제할 수 있으며, 전체 속성 경로 및 카드별 채널 구성을 요청 시 볼 수 있으며, 더 눈에 띄는 업로드 버튼에서 고유한 CSV, JSON 또는 JSONL 프로필을 업로드할 수 있습니다.


