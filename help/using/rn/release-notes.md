---
title: 릴리스 정보
description: Journey Optimizer 릴리스 정보
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 16bda5dcdfdc65f236d814ec02c6222b98a5652f
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 릴리스 정보 {#release-notes}

이 페이지에는 [!DNL Journey Optimizer]의 새로운 기능과 개선 사항이 모두 포함되어 있습니다. 또한 자세한 변경 사항은 [최신 설명서 업데이트](documentation-updates.md) 페이지를 참조하십시오.

[!DNL Adobe Journey Optimizer]은(는) 기본적으로 [!DNL Adobe Experience Platform] 기반으로 구축되었으며 최신 혁신 및 향상된 기능을 활용할 수 있습니다. [Adobe Experience Platform 릴리스 노트](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=ko-KR){target=&quot;_blank&quot;}에서 이러한 변경 사항에 대해 자세히 알아보십시오.

![뉴스레터](../assets/do-not-localize/nl-icon.png) 오늘 [Adobe Journey Optimizer 분기 뉴스레터](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;}에 등록하시면 분기마다 최신 제품 업데이트, 흥미로운 사례, 사용 사례, 팁 등을 받은 편지함에 바로 받을 수 있습니다.

## 2022년 7월 릴리스 {#july-2022-release}

### 새로운 기능

<table>
<thead>
<tr>
<th><strong>새로운 인라인 메시징 흐름</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer은 여정에서 메시지를 작성할 수 있는 새로운 흐름을 제공합니다. 인라인 메시징을 사용하면 사용자에게 상당한 시간을 절약하고 Journey Optimizer에서 이메일, 푸시 알림 또는 SMS를 만들고 전달하는 워크플로우 프로세스를 간소화할 수 있습니다. 메시지를 별도의 단계로 제거하고 대신 여정 캔버스에서 작업의 일부로 인라인 편집할 수 있도록 함으로써, 사용자는 더 적은 수의 단추를 클릭하고 더 적은 화면으로 이동하여 컨텐츠를 디자인하고 편집해야 합니다.</p>
<img src="assets/do-not-localize/inline.gif"/>
<p>자세한 내용은 <a href="../messages/get-started-content.md">세부 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>속성 기반 액세스 제어(제한된 가용성)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 조직 또는 데이터 사용 범위를 정의하는 레이블을 사용하여 스키마 필드를 식별할 수 있습니다. 관리자는 권한 인터페이스를 사용하여 XDM 스키마 필드에 적용되는 액세스 정책을 정의하고 사용자 또는 사용자 그룹(내부, 외부 또는 타사 사용자)에 부여된 액세스를 더 잘 관리하며 특정 데이터 유형(즉, 중요한 개인 데이터/SPD)에 대한 액세스를 관리할 수 있습니다.</p>
<p>속성 기반 액세스 제어 사용은 현재 선택한 사용자로만 제한되며 향후 릴리스의 모든 환경에 배포됩니다.</p>
<p>자세한 내용은 <a href="../administration/attribute-based-access.md">세부 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>일괄 결정 작업</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 사용자 인터페이스에서 배치 의사 결정 작업을 실행할 수 있으므로 배치 api 작업을 실행하는 개발자가 필요하지 않으며 마케팅 관련 시간을 줄일 수 있습니다. 이 새 인터페이스를 사용하면 작업을 만들고 현재/과거 작업을 관리할 수 있습니다.</p>
<img src="assets/do-not-localize/batch.gif"/>
<p>자세한 내용은 <a href="../offers/batch-delivery.md">세부 설명서를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>의사 결정 시 가장 성과가 좋은 오퍼를 자동으로 사용(제한된 가용성)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 의사 결정 관리에서 개인화된 최적화 모델 시스템을 사용할 수 있습니다. 이 새로운 유형의 모델을 사용하면 세그먼트와 오퍼 성과를 기반으로 오퍼를 최적화하고 개인화할 수 있습니다.</p>
<p>개인화된 최적화 AI 모델의 사용은 현재 선택한 사용자로만 제한되며 향후 릴리스의 모든 환경에 배포됩니다.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>자세한 내용은 <a href="../offers/ranking/personalized-optimization-model.md">자세한 설명서</a>를 참조하세요.</p>
</td>
</tr>
</tbody>
</table>

### 개선 사항

**여정**

* **여정 종료** - 여정 캔버스에서 **종료** 활동이 팔레트에서 제거되었습니다. 이제 끝 태그가 각 경로 끝에 기본적으로 추가되므로 제거할 수 없습니다. 이 개선 사항을 통해 고객이 여정에서 드롭된 위치를 여정 전문가의 작업 없이 더 잘 보고할 수 있습니다. 자세한 내용은 [설명서](../building-journeys/journey-end.md) 및 [기능 비디오](https://video.tv.adobe.com/v/345376){target=&quot;_blank&quot;}.

**메시지**

* 이제 메시지 사전 설정이 **채널 서피스**. [자세히 알아보기](../configuration/channel-surfaces.md)

**관리**

* **PTR 레코드 편집** - 이제 PTR 레코드를 업데이트할 때 처리 시간은 최대 3시간만 소요됩니다. [자세히 보기](../configuration/ptr-records.md#processing)

* **허용 목록 UI** - 이제 Journey Optimizer 사용자 인터페이스를 사용하여 허용 목록에 새 이메일 주소 또는 도메인을 추가할 수 있습니다. [자세히 보기](../configuration/allow-list.md)

* **허용 목록 논리 업데이트** - 이제 목록이 비어 있더라도 기능이 활성화되는 즉시 허용 목록 논리가 적용됩니다. [자세히 보기](../configuration/allow-list.md#logic)

* **URL 추적 매개 변수** - 이제 표현식 편집기를 사용하여 전자 메일 표면(즉, 메시지 사전 설정)에서 URL 추적 매개 변수를 구성할 수 있습니다. [자세히 알아보기](../configuration/email-settings.md#url-tracking)

**Offer Decisioning**

* **대상 크기** - 이제 의사 결정 규칙을 만들거나, 세그먼트 또는 규칙을 선택하여 오퍼 자격 설정을 하거나, 세그먼트 또는 규칙을 의사 결정 범위에 추가할 때 사용자 인터페이스에 새 대상 크기 예상 구성 요소가 표시됩니다.