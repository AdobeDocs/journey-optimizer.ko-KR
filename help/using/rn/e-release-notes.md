---
solution: Journey Optimizer
product: journey optimizer
title: 릴리스 정보
description: Journey Optimizer 초기 릴리스 정보
feature: Release Notes
topic: Content Management
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 5714e0aab20bce91ecf588c6b170a975be1f7d89
workflow-type: tm+mt
source-wordcount: '1671'
ht-degree: 47%

---

# 초기 릴리스 정보 {#e-release-notes}

[!DNL Adobe Journey Optimizer]는 지속적으로 새로운 기능, 기존 기능 개선, 버그 해결을 제공합니다. 모든 변경 사항은 매월 말 [릴리스 정보](release-notes.md)에 통합됩니다.

**아래 초기 릴리스 정보는 릴리스 공개 당일까지 사전 통지 없이 변경될 수 있습니다**. 링크, 화면, 업데이트된 설명서는 릴리스 날짜의 [릴리스 정보](release-notes.md)에 게시됩니다.

## 2024년 10월 초기 릴리스 정보 {#e-2024}

**릴리스 날짜**: 2024년 10월 29~30일

### 새로운 기능 {#e-features}

이번 릴리스에는 아래에 있는 새로운 기능이 제공됩니다.

<table>
<thead>
<tr>
<th><strong>이메일 콘텐츠 잠그기</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer에서 이메일 템플릿의 콘텐츠를 잠글 수 있습니다. 템플릿 전체를 잠그거나 특정 구조 및 구성 요소를 잠그는 것이 가능합니다. 이를 통해 의도하지 않은 편집 또는 삭제를 방지할 수 있으므로 템플릿의 사용자 정의 기능을 더욱 강력하게 제어하고 이메일 캠페인의 효율성과 안정성을 향상시킬 수 있습니다.</p>
<!--p>For more information, refer to the <a href="../content-management/gs-generative.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/ai-content.gif"/-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>여정 및 캠페인에서의 승인(일반 가용성)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 승인 정책을 사용하여 Journey Optimizer 내 승인 프로세스를 설정할 수 있습니다. 이를 통해 마케팅 팀에서 캠페인 및 여정을 라이브로 전환하기 전에 적절한 이해 관계자의 검토 및 승인을 놓치지 않을 수 있습니다.</p>
<p>이전에는 조직 집합(LA)에서 사용할 수 있었으나, 이제 모든 사용자(GA)가 승인 정책을 사용할 수 있습니다.</p>
<p>자세한 내용은 <a href="../test-approve/gs-approval.md">세부 설명서</a>를 참조하십시오.</p>
<img src="assets/do-not-localize/approval.gif"/>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>이메일 구성 개인화(일반 가용성)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 이메일 채널 구성을 만들 때 동적 하위 도메인과 개인화된 헤더 매개 변수를 정의하여 이메일 설정을 더욱 유연하게 제어할 수 있습니다.</p>
<p>이전에는 조직 집합(LA)에서 사용할 수 있었으나, 이제 모든 사용자(GA)가 이메일 구성 개인화를 사용할 수 있습니다.</p>
<p>자세한 내용은 <a href="../email/surface-personalization.md">세부 설명서</a>를 참조하십시오.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>웹 디자이너의 비시각적 편집 모드</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer 웹 디자이너의 대체 요소로서 시각적이지 않은 편집기를 사용하여 웹 사이트에 수정 사항을 추가할 수 있습니다. 이 옵션을 사용하면 시각적 편집기에서 페이지를 열지 않고도 변경 사항을 수동으로 입력할 수 있습니다.
이 비시각적 편집 모드는 웹 디자이너에서 페이지를 로드하는 데 필요한 Adobe Experience Cloud Visual Helper와 같은 브라우저 확장 기능을 설치할 수 없는 경우에 유용합니다.</p>
<!--p>For more information, refer to the <a href="../email/surface-personalization.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>



<table>
<thead>
<tr>
<th><strong>Movable Ink 및 Adobe Journey Optimizer 통합</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Movable Ink Da Vinci와 Adobe Journey Optimizer을 통합할 수 있습니다. 이 새로운 통합을 통해 다음과 같은 작업을 수행할 수 있습니다. </p>
<p><ul><li>Movable Ink의 Da Vinci 제품에 포함된 강력한 기능을 활용하여 일괄 캠페인을 위한 이메일 변형을 취합하고 개인화합니다</li>
<li>작성을 위해 Da Vinci를 사용하고 최적화 및 전달을 위해 AJO을 사용하는 Journey Optimizer 고객을 위한 실용적인 워크플로 가속화</li>
<li>Adobe 데이터로 다빈치 모델 최적화.</li></ul></p>
<!--p>For more information, refer to the <a href="../code-based/get-started-code-based.md">detailed documentation</a>.</p-->
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>여정에서의 실험(일반 가용성)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer가 이제 여정에서도 실험을 지원합니다. 캠페인에서는 이미 실험을 사용할 수 있습니다. 실험은 무작위화한 시험 회기 여러 개를 모아 놓은 것입니다. 온라인 테스팅 맥락에서는 무작위로 선택한 사용자 일부를 특정한 버전의 메시지에 노출하고, 무작위로 선택한 다른 사용자들을 다른 처리 버전에 노출하는 것을 말합니다. 노출 후에는 이메일 열람, 구독 또는 구매 등 궁금한 결과 지표를 측정할 수 있습니다.</p>
<p>이전에는 조직 집합(LA)에서 사용할 수 있었지만, 이제 모든 사용자(GA)가 여정에서 실험을 사용할 수 있습니다.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>비즈니스 규칙(일반 가용성)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 세분화된 빈도 제한 규칙을 만들어 규칙 세트를 통해 다양한 유형의 마케팅 커뮤니케이션에 적용할 수 있습니다. 이 새로운 기능을 사용하면 메시지 및 작업에서 과도하게 요청된 프로필을 자동으로 제외하는 크로스 채널 규칙을 설정하여 대상자가 메시지를 받는 빈도를 제어할 수 있습니다.</p>
<p>이전에는 조직 집합(LA)에서 사용할 수 있었지만, 이제 모든 사용자(GA)가 규칙 집합을 사용할 수 있게 되었습니다.</p>
<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>여정 및 캠페인의 다국어 메시지(일반 가용성)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 단일 캠페인 또는 여정 내에서 간편하게 여러 언어로 콘텐츠를 만들 수 있습니다. 이 기능을 사용하면 캠페인이나 여정을 편집할 때 언어를 전환할 수 있으므로 전체 편집 프로세스를 간소화하고 다국어 콘텐츠를 더욱 효율적으로 관리할 수 있습니다.</p>
<p>이전에는 조직 집합(LA)에서 사용할 수 있었지만, 이제 모든 사용자(GA)가 다국어 메시지를 사용할 수 있습니다.</p>
<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>업데이트된 보고 환경(일반 가용성)</strong><br/>2024년 10월 16일 이후 사용 가능<br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 Journey Optimizer 보고가 GA(General Availability)되었으며 Customer Journey Analytics 기능과의 상호 운용성이 개선되어 두 플랫폼 간에 보고를 표준화하고 데이터 일관성과 안정성을 향상시킵니다. 이렇게 Journey Optimizer와 Customer Journey Analytics가 원활하게 통합됨으로써 사용자가 성과 지표를 보다 명확하게 확인하여 확실한 정보에 근거한 결정을 내릴 수 있습니다.</p>
<p>일반 공급 기능에는 간단한 지표 만들기, 대상자 만들기 및 게시, Insight Builder를 사용하여 임시 질문하기, 주요 수신자에게 자동으로 이메일로 전송할 보고서 예약 등의 네 가지 새로운 기능이 도입되었습니다.</p>
<p>자세한 내용은 <a href="../reports/report-cja-manage.md">세부 설명서</a>를 참조하십시오.</p>
<img src="assets/do-not-localize/ajo-cja.gif">
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>여정의 코드 기반 경험</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>코드 기반 경험 채널에서는 Adobe Journey Optimizer에서 원하는 인바운드 속성에 대해 고급 개인화 및 테스트를 수행할 수 있으므로 웹 앱, 모바일 앱, 데스크탑 앱, 비디오 콘솔, TV에 연결된 디바이스, 스마트 TV, 키오스크, ATM, IoT 디바이스 등과 같은 다양한 접점에서 맞춤형 경험을 원활하게 전달할 수 있습니다. 이제 여정 캔버스에서 코드 기반 경험 채널을 사용할 수 있습니다.</p>
<p>자세한 내용은 <a href="../code-based/create-code-based.md">세부 설명서</a>를 참조하십시오.</p>
<img src="../assets/do-not-localize/code-based-journey.gif"/>
<p>사용 가능한 날짜: 2024년 10월 1일</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>여정의 웹 경험</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>웹 채널을 사용하면 Adobe Journey Optimizer에서 인바운드 웹 채널을 통해 고객에게 제공하는 웹 경험을 개인화할 수 있습니다. 이제 여정 캔버스에서 웹 채널을 사용할 수 있습니다.</p>
<p>자세한 내용은 <a href="../web/create-web.md">세부 설명서</a>를 참조하십시오.</p>
<img src="../assets/do-not-localize/web-journey.gif"/>
<p>사용 가능한 날짜: 2024년 10월 1일</p>
</tr>
</tbody>
</table>

>[!IMPORTANT]
>
>현재 보고 경험은 2025년 1월부터 종료됩니다. 이 날짜 이후에는 새로운 보고 경험이 표준이 됩니다. 원활한 전환을 위해 새로운 기능을 숙지하는 것이 좋습니다.
>
> [Journey Optimizer의 새로운 보고 인터페이스를 시작하는 방법 알아보기](../reports/report-gs-cja.md)


### 개선 사항 {#e-improvements}

이 릴리스는 아래 목록에 있는 개선 사항과 함께 제공됩니다.

**SMS 채널**

메시징 기능을 개선하기 위해 SMS 개선 사항이 도입되었습니다.

* SMS 캠페인 및 여정에 대한 고유 키워드를 정의하고 관리하여 보다 개인화되고 효율적인 커뮤니케이션을 가능하게 할 수 있습니다.
* 키워드가 인식되지 않을 때 기본 SMS 메시지를 만들고 전달할 수 있습니다.

**빈도 및 우선 순위 관리**

* **캠페인이나 여정에 따른 빈도 제한** - 이제 여정에 적용할 빈도 규칙을 만들 수 있으므로 일별, 주별 또는 월별 여정 수를 제한하고 동시에 실행되는 동시 여정 수를 제어할 수 있습니다.

* **우선 순위 점수** - 이제 0에서 100 범위의 우선 순위 점수를 캠페인이나 여정에 할당할 수 있습니다. 숫자가 높을수록 우선 순위가 높다는 뜻입니다. 두 개의 캠페인 또는 여정이 동일한 표면을 사용하는 경우 Journey Optimizer에서 우선순위 점수가 가장 높은 것을 선택합니다. 캠페인의 점수가 동일한 경우, 가장 최근에 수정된 캠페인이 선택됩니다. 우선 순위 점수는 캠페인의 모든 인바운드 채널에 사용할 수 있으며 여정의 인앱 채널에 사용할 수 있습니다.

* **충돌 보기** - 이제 여정 및 캠페인의 새 **충돌 보기** 단추를 사용하여 시작 날짜, 타깃팅된 대상 또는 선택한 여정 구성과 같은 다른 채널 또는 캠페인과 겹칠 가능성이 있을 때마다 확인할 수 있습니다.

**의사 결정 관리**

* **감사** - 오퍼 또는 의사 결정에 대한 모든 변경 내용을 볼 수 있는 **변경 로그** 탭입니다. 이제 오퍼 및 의사 결정과 관련된 변경 사항을 **감사** 메뉴 아래 제품에서 사용할 수 있습니다.


**구성**

* **표면 개인화** - 이제 캠페인이나 여정에서 개인화된 구성을 사용할 때 이메일 콘텐츠를 미리 보고 정의한 동적 설정으로 잠재적인 오류가 있는지 확인할 수 있습니다.

**여정**

* **여정의 경로 실험** - 이제 여정 경로 실험을 통해 여정 경로에 대한 주요 지표를 정의하고 추적할 수 있으므로 활동의 영향을 측정하고 성능에 대한 보다 명확한 통찰력을 제공할 수 있습니다.

* **최대 라이브 여정 수** - 이제 Journey Optimizer의 프로덕션 샌드박스에 100개가 아닌 500개 라이브 여정의 가드레일이 있습니다. 라이브 여정 수는 여정 캔버스에 표시됩니다. <!-- DOCAC-10977-->

* **TTL(Time-to-Live) 보호** - 2024년 11월 1일부터 다음과 같이 Journey Optimizer 시스템 생성 데이터 세트에 TTL(Time-to-Live) 보호가 적용됩니다.

   * 프로필 스토어의 데이터에 대해 90일
   * 13개월 데이터 레이크

또한 이 시점에서는 스트리밍 세분화가 더 이상 추적 및 피드백 데이터 세트의 전송 및 피드백 이벤트 사용을 지원하지 않습니다. 한동안 스트리밍 세분화에 이러한 이벤트를 사용하지 않도록 권장했었는데, 이제 이러한 이벤트를 모두 비활성화합니다.

* 이 변경 사항은 스트리밍 세분화에서 전송/열기 이벤트 사용만 제한합니다. 클릭 이벤트는 여전히 스트리밍 세그먼트에서 사용할 수 있습니다. 또한 보내기/열기 이벤트는 일괄 처리 세그먼트에서 계속 사용할 수 있습니다.
* 추적 데이터는 계속 수집됩니다. 이 변경 사항은 추적에 영향을 주지 않습니다. 이메일을 보낸 사람과 이메일을 클릭한 사람을 계속 추적할 수 있습니다.
* 여정의 반응 이벤트는 이 변경의 영향을 받지 않습니다.

* **사용자 지정 작업의 매개 변수**(사용 가능한 날짜: 2024년 10월 3일) - 이제 사용자 지정 작업에서 NULL 및 선택적 매개 변수가 지원됩니다. [자세히 알아보기](../action/about-custom-action-configuration.md#define-the-message-parameters)

**데이터 거버넌스 및 동의 정책** - 사용 가능한 날짜: 2024년 10월 7일

* **데이터 거버넌스 정책** 시행이 이제 Journey Optimizer의 모든 채널에 적용됩니다. Adobe Experience Platform에서 정책을 만든 고객의 경우 이 정책은 채널 구성 설정의 일부로 마케팅 액션에 적용됩니다. 구성을 사용하여 콘텐츠를 만들 때 시스템은 모든 개인화 필드를 확인하여 데이터 거버넌스 위반 여부를 찾습니다. 위반이 발견되면 여정 또는 캠페인을 게시할 수 없습니다. [자세히 알아보기](../action/action-privacy.md)

* 이제 **사용자 정의 동의 정책**&#x200B;이 모든 Journey Optimizer 채널에 적용됩니다. 메시지가 전송되거나 인바운드 경험이 게재되기 전에 적용 시 시스템은 사용자가 수신할 콘텐츠의 개인화 필드 사용에 동의했는지 확인합니다. 동의를 하지 않은 경우 해당 경험이 표시되지 않습니다. [자세히 알아보기](../action/consent.md)

  >[!NOTE]
  >
  >동의 정책 기능은 현재 Adobe **Healthcare Shield** 또는 **Privacy and Security Shield** 추가 기능 서비스를 구매한 조직에만 제공됩니다.

**대상자** - 사용 가능한 날짜: 2024년 10월 8일

* 이제 CSV 파일 대상자를 타기팅할 때 개인화 편집기와 여정 및 캠페인 규칙 빌더에서 파일의 속성을 사용할 수 있습니다. [자세히 알아보기](../audience/about-audiences.md)

* 이제 사용자 정의 업로드(CSV 파일)의 대상자 및 속성을 Healthcare Shield 또는 Privacy and Security Shield에서도 사용할 수 있습니다.



