---
solution: Journey Optimizer
product: journey optimizer
title: 릴리스 정보
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Adobe Journey Optimizer 릴리스 정보
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
TQID: https://experienceleague.adobe.com/YJKQFYUi8Kw7yZZKm8blcM-1G9uYsqcsEsopH0hOMhA
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2:
  - id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794
  - id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0
  - id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 0ccd65f3e2f37c7893e81ab0a94ee4842cd4565d
workflow-type: tm+mt
source-wordcount: 1045
ht-degree: 38%

---

# 릴리스 정보 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="새로운 기능"
>abstract="**Adobe Journey Optimizer**&#x200B;는 지속적으로 새로운 기능, 기존 기능 개선 및 버그 해결을 지원합니다. 모든 변경 사항은 매달 마지막 주에 여기 있는 릴리스 정보에 통합됩니다."

[!DNL Adobe Journey Optimizer]은(는) 지속적 제공 모델을 따르므로 Adobe에서 새로운 기능, 개선 사항, 버그 해결 업데이트를 지속적으로 제공할 수 있습니다. 이 접근 방식을 사용하면 확장 가능한 단계별 기능 롤아웃을 통해 모든 환경에서 성능과 안정성을 보장할 수 있습니다. 이 모델로 인해 월별 릴리스 사이에 릴리스 정보가 업데이트됩니다. 릴리스 주기 및 가용성 단계에 대한 자세한 내용은 [Journey Optimizer 릴리스 주기](releases.md)를 참조하십시오.

[!DNL Adobe Journey Optimizer]은 기본적으로 [!DNL Adobe Experience Platform] 기반으로 빌드되었으며 최신 혁신 및 향상된 기능을 활용할 수 있습니다. 변경 사항에 대한 자세한 내용은 [Adobe Experience Platform 릴리스 정보](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=ko){target="_blank"}를 참조하십시오.

>[!NOTE]
>
>이 릴리스 정보에 나열된 기능에는 각 변경 사항이 사용자 환경에서 사용 가능해지는 시점을 나타내는 **사용 가능한 날짜**&#x200B;가 포함되어 있습니다. **곧 출시 예정** 아코디언 항목은 향후 며칠 또는 몇 주 내에 제공될 예정입니다. 이 섹션의 정보는 변경될 수 있습니다.

## 2026년 7월 릴리스 정보 {#july-26-updates}

### 여정 {#july-26-journeys}

이번 릴리스에서는 다음과 같은 기능 및 개선 사항이 여정에 추가되었습니다.
<table>
<thead>
<tr>
<th><strong>새로운 사용자 인터페이스</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>여정 캔버스에 <b>새로운 여정 인터페이스</b>가 도입되어 대규모 사용자에 대한 향상된 성능, 향상된 가독성을 위한 자동 레이아웃 및 안내식 작성 환경을 제공합니다.</p>
<p><img src="../building-journeys/assets/journey-new-canvas.png"></p>
<p>새 UI로 전환하려면 <b>새 경험</b> 단추를 클릭하세요. 이 설정은 여정 수준에서 저장되므로 기본적으로 여정은 새 경험에서 다시 열립니다. 되돌리려면 <b>이전 경험</b>을 클릭하세요. <a href="../building-journeys/using-the-journey-designer.md#canvas-capabilities">자세히 알아보기</a></p>
<p><img src="../building-journeys/assets/journey-new-experience-switch.png"></p>
<p> 사용 가능한 날짜: 2026년 7월 16일</p>
</td>
</tr>
</tbody>
</table>

* [!BADGE 사용 중단]{type=Negative} 일괄 처리 대상은 대상 자격 노드에서 더 이상 지원되지 않습니다. 2026년 8월 3일부터 Journey Optimizer에서는 대상 자격 노드에서 일괄 처리 대상을 사용하는 여정에 대한 게시를 차단합니다. 이 시행은 6월 릴리스에 도입된 캔버스 경고를 대체합니다. 기존 라이브 여정은 영향을 받지 않습니다. 대상 자격 노드에서 스트리밍 대상을 사용하거나 대상 읽기 활동으로 전환합니다. [여정 마이그레이션 방법 알아보기](../building-journeys/aq-batch-audiences-migration.md)

### 오케스트레이션된 캠페인 {#july-26-oc}

이번 릴리스에서는 오케스트레이션된 캠페인에 다음과 같은 기능 및 개선 사항이 추가됩니다.

<table>
<thead>
<tr>
<th><strong>오케스트레이션된 캠페인의 파일 기반 타겟팅</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 오케스트레이션된 캠페인은 파일을 Adobe Experience Platform으로 먼저 수집하지 않고도 <strong>CSV 또는 TXT 파일</strong>을 타깃팅 대상자로 캠페인 캔버스에 직접 로드할 수 있습니다. 파일 데이터는 실행 시 사용되며 Adobe Experience Platform 데이터 세트로 지속되지 않습니다. 파일 설정 중에 열 매핑, 데이터 유형, NULL 처리 및 열별 오류 정책을 정의할 수 있습니다. 유효성 검사에 실패한 행은 캠페인이 실행되기 전에 거부되고 기록되므로, 수동 사전 처리 없이 대상자를 깔끔하게 유지합니다. 이는 전체 수집 파이프라인을 구축하는 것이 실용적이지 않은 애드혹 전송 또는 파트너 목록 캠페인에 특히 적합합니다.</p>
<p>자세한 내용은 <a href="../orchestrated/activities/load-file.md">세부 설명서</a>를 참조하십시오.</p>
<p> 사용 가능한 날짜: 2026년 7월 6일</p>
</td>
</tr>
</tbody>
</table>

### 콘텐츠 관리 {#july-26-content}

이 릴리스의 콘텐츠 관리에 다음과 같은 기능 및 개선 사항이 추가되었습니다.

* **조각 인벤토리의 빠른 실행 바로 가기** - 이제 **[!UICONTROL 추가 작업]** 단추를 사용하여 조각 목록에서 일반적인 작업에 빠르게 액세스할 수 있습니다. 사용 가능한 단축키에는 조각 편집, 세부 정보 열기, 초안 버전 삭제 등이 있습니다. [자세히 알아보기](../content-management/manage-fragments.md#quick-launch-fragments)

  ![](../content-management/assets/fragment-quick-launch.png)

* **템플릿 인벤토리의 빠른 실행 바로 가기** - 이제 콘텐츠 템플릿 목록의 **[!UICONTROL 추가 작업]** 단추를 사용하여 템플릿 세부 정보 편집, 콘텐츠 시뮬레이션 및 템플릿 삭제와 같은 일반적인 작업에 빠르게 액세스할 수 있습니다. 이메일 템플릿의 경우 추가 단축키를 사용하여 제목란 및 이메일 본문을 편집하고, 증명을 보거나 보내고, 스팸 보고서를 실행하고, 이메일을 렌더링할 수 있습니다. [자세히 알아보기](../content-management/access-content-templates.md#quick-launch-templates)

  ![](../content-management/assets/content-template-quick-launch.png)

### 이메일 채널 {#july-26-email}

이 릴리스의 이메일 채널에 다음과 같은 개선 사항이 추가되었습니다.

<table>
<thead>
<tr>
<th><strong>채널 최적화</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 여러 아웃바운드 채널(이메일, 푸시, SMS)을 포함하도록 여정 또는 캠페인 작업을 구성하고 Journey Optimizer에서 각 고객을 위한 최상의 채널을 자동으로 전달하도록 할 수 있습니다. 세 가지 최적화 모드를 사용할 수 있습니다.</p>
<ul>
<li>수동 순위: 선호하는 채널 순서를 지정합니다.</li>
<li>고객 환경 설정: 프로필에서 고객이 선호하는 채널을 사용합니다(Experience Data Model 동의 및 환경 설정 속성).</li>
<li>AI 모델 기반 순위: 머신 러닝 성향 점수를 사용하여 고객당 가장 효과적인 채널을 추론합니다.</li>
</ul>
<p>최상위 채널을 사용할 수 없는 경우(옵트인, 주파수 제한 또는 구성되지 않은 경우) 시스템이 사용 가능한 다음 채널로 폴백합니다.</p>
<p>이 기능은 일부 조직에서만 사용할 수 있습니다(제한된 가용성). 액세스 권한을 받으려면 Adobe 담당자에게 문의하십시오.</p>
<p><img src="assets/do-not-localize/channel-optimization.gif"></p>
<p>자세한 내용은 <a href="../building-journeys/channel-optimization.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 7월 22일</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>이메일 Designer에서 컨텐츠 확인(일반 가용성)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer는 이제 이메일 디자이너에 직접 자동화된 기술 유효성 검사 기능을 포함하여 전송 전에 HTML 및 CSS 문제를 감지할 수 있도록 지원합니다.</p>
<p>검사에는 <code>&lt;script&gt;</code> 및 <code>&lt;base&gt;</code> 태그와 같은 지원되지 않는 요소, Microsoft Outlook에서 레이아웃을 깨뜨릴 수 있는 빈 div, HTML Meta 새로 고침 태그, Gmail에서 렌더링 오류를 유발하는 CSS 또는 HTML 크기 임계값 등이 포함됩니다.</p>
<p>검사 결과는 작성 패널에 오류, 경고 또는 정보 알림으로 표시되며, 상황별 세부 정보와 가능한 경우 원클릭 수정 기능이 제공되므로 편집기를 종료하지 않고도 문제를 해결할 수 있습니다.</p>
<p>이전에는 제한 공급으로만 사용 가능했던 이 기능이 이제 모든 고객에게 정식으로 제공됩니다.</p>
<p><img src="assets/do-not-localize/content-check.gif"></p>
<p>자세한 내용은 <a href="../email/content-check.md">세부 설명서</a>를 참조하십시오.</p>
<p>사용 가능한 날짜: 2026년 7월 16일</p>
</td>
</tr>
</tbody>
</table>

### 콘텐츠 및 통합 {#july-26-integration}

이번 릴리스에서는 콘텐츠 관리 및 통합 기능에 다음과 같은 기능과 개선 사항이 추가될 예정입니다.

* **의사 결정 항목의 동적 사용자 지정 특성** - 이제 프로필, 컨텍스트 및 대상 데이터를 사용하여 전달 시 의사 결정 항목 사용자 지정 특성을 개인화할 수 있습니다. 이렇게 하면 사소한 콘텐츠 변형에 대한 중복 오퍼를 관리할 필요가 없어지므로 마케터는 더 적고 유연한 결정 항목을 관리할 수 있습니다. [자세히 보기](../experience-decisioning/items.md#attributes)

  사용 가능한 날짜: 2026년 7월 27일

* **AJO MCP 서버 새 도구** - 이제 [!DNL Adobe Journey Optimizer] MCP 서버는 5개의 추가 읽기 전용 **채널 구성 도구**&#x200B;를 노출하므로 AI 도우미에서 직접 채널 구성, 지원 리소스 및 마케팅 작업을 쿼리할 수 있습니다. 이제 **목록 채널 구성**(모든 AJO 채널에서), **채널 구성 가져오기**, **목록 구성 리소스**, **구성 리소스 가져오기** 및 **목록 마케팅 작업**&#x200B;을 사용할 수 있습니다. [자세히 보기](../integrations/ajo-mcp.md#mcp-tools)

  사용 가능한 날짜: 2026년 7월 9일

### 관리 {#july-26-administration}

이 릴리스의 관리 및 데이터 관리에 다음과 같은 개선 사항이 추가되었습니다.

* **TTL(Time-to-Live) 보호 — 기존 샌드박스** - Journey Optimizer 시스템 생성 데이터 세트에 대한 TTL(Time-to-Live) 보호(프로필 스토어에서 90일, 데이터 레이크에서 13개월)가 **기존 고객 샌드박스 및 조직에 적용됩니다** **2026년 10월 1일**. [자세히 알아보기](../data/datasets-ttl.md#ttl-guardrail)


