---
solution: Journey Optimizer
product: journey optimizer
title: 릴리스 정보
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
description: Journey Optimizer 릴리스 정보
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 0c428b18469eb98392fe6c49d5892a4699477457
workflow-type: tm+mt
source-wordcount: '601'
ht-degree: 27%

---

# 릴리스 정보 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="새로운 기능"
>abstract="**Adobe Journey Optimizer**&#x200B;는 지속적으로 새로운 기능, 기존 기능 개선, 버그 해결을 제공합니다. 모든 변경 사항은 매달 마지막 주에 여기 있는 릴리스 정보에 통합됩니다."

[!DNL Adobe Journey Optimizer]는 지속적으로 새로운 기능, 기존 기능 개선, 버그 해결을 제공합니다. 모든 변경 사항은 매달 마지막 주에 여기 있는 릴리스 노트에 통합됩니다.

[!DNL Adobe Journey Optimizer]은(는) 기본적으로 [!DNL Adobe Experience Platform] 기반으로 구축되었으며 최신 혁신 및 향상된 기능을 활용할 수 있습니다. 변경 사항에 대한 자세한 내용은 [Adobe Experience Platform 릴리스 노트](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=ko-KR){target="_blank"}를 참조하세요.

![뉴스레터](../assets/do-not-localize/nl-icon.png) 오늘 [Adobe Journey Optimizer 분기별 뉴스레터](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"}에 등록하여 분기마다 최신 제품 업데이트, 재미있는 이야기, 사용 사례, 팁 등을 메일로 직접 받아 보세요.

## 2024년 1월 초기 릴리스 정보 {#jan-2024}

**릴리스 날짜**: 2024년 1월 30~31일

### 새로운 기능{#jan24-features}

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
<p>자세한 내용은 <a href="../configuration/dmarc-record-update.md">세부 설명서</a>를 참고하십시오.</p>
<br/><img src="assets/do-not-localize/dmarc.gif"/>
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
<p>Real-Time CDP 및 Journey Optimizer의 산업별 사용 사례 플레이북 카탈로그를 활용하여 Adobe Experience Platform 및 Adobe 여정 최적기를 사용하여 수행할 수 있는 일반적인 사용 사례를 해결합니다.</p><p>요구 사항에 가장 적합한 플레이북을 선택하면 여정, 메시지, 스키마 또는 세그먼트와 같은 사용 사례를 지원하는 데 필요한 자산을 생성하고, 가치 창출 시간을 단축하기 위해 스키마에 맞게 사용자 지정할 수 있습니다.</p>
<p>자세한 내용은 <a href="../start/playbooks.md">자세한 설명서</a>를 참조하세요.</p>
<br/><img src="assets/do-not-localize/playbooks.gif"/>
</tr>
</tbody>
</table>

### 개선 사항 {#jan24-improvements}

이 릴리스는 아래 목록에 있는 개선 사항과 함께 제공됩니다.

**보고**

* **새 도메인 기반 분류 위젯** - Campaign 및 여정 보고서를 개선하기 위해 새 위젯이 추가되었습니다. 다음 **도메인별 바운스 이유**, **도메인에서 전송 및 전달**, **도메인별 열기 및 클릭 수** 및 **도메인별 바운스 및 오류** 위젯은 도메인 수준에서 주요 이메일 게재 및 추적 지표에 대한 세부 분류를 제공합니다. [자세히 알아보기](../reports/channel-report.md)

**SMS 채널**

* **이중 옵트인** - SMS에 대한 이중 옵트인 워크플로우를 사용하면 장치에서 요청을 시작할 때 사용자가 메시지를 수신하도록 명시적으로 옵트인할 수 있습니다. 사용자는 인바운드 SMS 메시지를 전송하여 동의 프로세스를 시작합니다. 동의를 확인하면 최종 확인을 요청하는 후속 메시지가 발송된다. 사용자 프로필이 존재하지 않으면 확인 후 생성됩니다. [자세히 알아보기](../sms/sms-configuration.md#create-api)

  이 기능은 Sinch 및 Infobip SMS 공급자에서 사용할 수 있습니다.

**여정**

* **반응 이벤트 기간** - 다음에서 정의할 수 있는 최대 기간 **반응 이벤트** 는 현재 30일이 아니라 29일입니다. [자세히 알아보기](../building-journeys/reaction-events.md)

<!--* **Date filters** - You can now use custom dates to filter the journeys inventory, in addition to the existing predefined date filters. This allows you to refine the list by displaying journeys published on a specific date, within a particular month, throughout an entire year, or within specified time ranges. [Learn more](../building-journeys/journey-gs.md#filter)-->

* **대상자 읽기**  - **대상자 읽기** 이제 활동은 예약된 일별 배치 작업이 실행된 후 하루에 한 번만 생성되는 배치 세그먼트에 대한 프로필 스냅샷 데이터 세트를 사용하므로 데이터는 마지막 일별 배치 작업까지 새로 고쳐집니다.

* **필드 그룹** - 이 릴리스에서는 특정 경우에 필드 그룹이 저장되지 않는 문제를 해결했습니다.

**빈도 규칙**

* **주별 및 일별 빈도 상한** - 이제 월별 외에 일주일 또는 하루 단위로 고객 프로필에 전송되는 최대 메시지 수를 지정할 수 있습니다. 주파수 캡은 선택된 캘린더 기간에 기초하고 대응하는 시간 프레임의 시작에서 리셋된다. [자세히 알아보기](../configuration/frequency-rules.md#create-new-rule)

**의사 결정 관리**

* **가장자리 빈도 설정** - 이제 빈도 제한 카운터가 업데이트되어 Edge Decisioning API 의사 결정에서 3초 이내에 사용할 수 있습니다.