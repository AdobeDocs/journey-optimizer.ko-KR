---
solution: Journey Optimizer
product: journey optimizer
title: 'Journey Optimizer 가드레일 및 제한 사항 '
description: Journey Optimizer 가드레일에 대해 자세히 알아보기
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: a7468879b36dfe9184471824b387f1638fae3d50
workflow-type: ht
source-wordcount: '2504'
ht-degree: 100%

---

# 가드레일 및 제한 사항 {#limitations}

[!DNL Adobe Journey Optimizer] 사용 시 다음과 같은 추가 가드레일 및 제한 사항이 있습니다.

자격, 제품 제한 사항, 성능 가드레일 목록은 [Adobe Journey Optimizer 제품 설명 페이지](https://helpx.adobe.com/kr/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}에서 확인하실 수 있습니다.

시작 전 [실시간 고객 프로필 데이터 가드레일](https://experienceleague.adobe.com/docs/experience-platform/profile/guardrails.html?lang=ko){target="_blank"}에 대해 알고 있어야 합니다.

## 지원되는 브라우저 {#browsers}

Adobe [!DNL Journey Optimizer] 인터페이스는 최신 버전의 Google Chrome에서 최적으로 작동되도록 디자인되었습니다. 이전 버전 또는 기타 브라우저에서 특정 기능을 사용하는 데 문제가 있을 수 있습니다.

## 데이터 세트 가드레일 {#datasets-guardrails}

2025년 2월부터 **새로운 샌드박스와 새로운 조직**&#x200B;에서 Journey Optimizer 시스템 생성 데이터 세트에 다음과 같은 TTL(Time-to-Live) 가드레일이 롤아웃됩니다.

* 프로필 스토어의 데이터에 대해 90일
* 데이터 레이크의 데이터에 대해 13개월

이 변경 사항은 차후 **기존 고객 샌드박스**&#x200B;에 대해서도 롤아웃됩니다. [데이터 세트 TTL(Time-To-Leave) 가드레일에 대해 자세히 알아보기](../data/datasets-ttl.md)

## 채널 가드레일 {#channel-guardrails}

>[!NOTE]
>
>드문 경우지만 특정 지역에서 일시적으로 서비스가 중단되면 유효한 프로필이 여정에서 제외되거나 메일이 바운스로 잘못 표시될 수 있습니다. 서비스가 복원되면 여정 로그를 재점검하고 동의 프로필 필드를 확인한 다음 필요한 경우 여정을 다시 게시합니다. ISP 중단 시 금지 목록에서 프로필을 제거하는 방법은 [이 섹션](../configuration/manage-suppression-list.md#remove-from-suppression-list)에서 확인할 수 있습니다.
>

### 이메일 가드레일 {#message-guardrails}

[이메일 채널](../email/get-started-email.md)에 다음 가드레일이 적용됩니다.

* [!DNL Journey Optimizer]에서는 이메일에 첨부 파일을 추가할 수 없습니다.
* 동일한 발신 도메인을 사용하여 [!DNL Adobe Journey Optimizer] 및 다른 제품(예: [!DNL Adobe Campaign] 또는 [!DNL Adobe Marketo Engage])에서 메시지를 보낼 수 없습니다.

### SMS 가드레일 {#sms-guardrails}

[SMS 채널](../sms/get-started-sms.md) 활동에 다음 가드레일이 적용됩니다.

* 지원 URL을 통해 MMS에 넣을 미디어 파일을 포함할 수 있습니다. 미디어 파일이 별도로 업로드되는지 확인해야 합니다.
* 현재 MMS에는 메시지 피드백 동기화를 사용할 수 없습니다.
* MMS에 대한 동의 관리는 SMS 채널 수준에서 작동합니다.

### 웹 채널 가드레일 {#web-guardrails}

[!DNL Journey Optimizer] [웹 캠페인](../web/get-started-web.md)은 다른 채널에서 이전에 참여하지 않은 새 프로필을 타기팅합니다. 이렇게 하면 총 참여 가능 프로필 수가 증가하므로, 사용자가 계약 시 구입한 참여 가능 프로필 수를 초과하는 경우 비용이 발생할 수 있습니다. 

각 패키지별 라이선스 지표 목록은 [Journey Optimizer 제품 설명](https://helpx.adobe.com/kr/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"} 페이지에서 확인할 수 있습니다.

### 코드 기반 채널 가드레일 {#code-based-guardrails}

[!DNL Journey Optimizer]에서 코드 기반 경험 작업을 사용하고 애플리케이션에서 사용할 수 있는 코드 콘텐츠 페이로드를 전달하려면 [이 페이지](../code-based/code-based-prerequisites.md)에 설명된 전제 조건을 따르십시오.

## 랜딩 페이지 보호 {#lp-guardrails}

[랜딩 페이지](../landing-pages/get-started-lp.md)에 다음 가드레일이 적용됩니다.

* 하나의 기본 페이지에서 하나의 **양식** 구성 요소만 사용할 수 있습니다.
* **양식** 구성 요소는 하위 페이지에서 사용할 수 없습니다.
* 랜딩 페이지에 사전 헤더를 추가할 수 없습니다. 
* 방문 기본 페이지를 디자인할 때 **자신만의 코드 작성** 옵션을 선택할 수 없습니다.

## 하위 도메인 가드레일 {#subdomain-guardrails}

기본적으로,[!DNL Journey Optimizer] 총 10개까지 하위 도메인을 위임할 수 있습니다(이메일 및 웹 채널 모두 포함).

그러나 라이선스 계약에 따라 최대 100개의 하위 도메인을 위임할 수 있습니다. 부여된 하위 도메인 수에 대해 자세히 알아보려면 Adobe 담당자에게 문의하십시오.

[이 페이지](../configuration/delegate-subdomain.md)에서 도메인 위임에 대해 자세히 알아보십시오.

## 조각 가드레일 {#fragments-guardrails}

[조각](../content-management/fragments.md)에 다음 가드레일이 적용됩니다.

* 시각적 조각은 이메일 채널에만 사용할 수 있습니다.
* 인앱 채널에는 표현식 조각을 사용할 수 없습니다.

## 대상자 가드레일 {#audience}

주어진 샌드박스 하나에 최대 10개의 대상자 컴포지션을 게시할 수 있습니다. 이 임계값에 도달한 경우 컴포지션을 삭제하여 공간을 확보하고 새 컴포지션을 게시해야 합니다.

[이 페이지](../audience/get-started-audience-orchestration.md)에서 대상자 컴포지션에 대해 자세히 알아보십시오.

## 의사 결정 및 의사 결정 관리 가드레일 {#decisioning-guardrails}

의사 결정 및 의사 결정 관리 작업 시 기억해야 할 가드레일과 제한 사항은 의사 결정 및 의사 결정 관리 섹션에 자세히 설명되어 있습니다.

* [의사 결정 가드레일 및 제한 사항](../experience-decisioning/decisioning-guardrails.md)
* [의사 결정 관리 가드레일 및 제한 사항](../offers/decision-management-guardrails.md)


## 여정 보호  {#journeys-guardrails}

### 일반 여정 가드레일 {#journeys-guardrails-journeys}

* 한 여정에 넣을 수 있는 활동 수는 50개로 제한됩니다. 활동 수는 여정 캔버스의 왼쪽 위 섹션에 표시됩니다. 이는 가독성과 QA, 문제 해결에 도움이 됩니다.
* 여정을 게시하면 처리량과 안정성을 최대화하기 위해 자동으로 규모를 조절합니다. 한 번에 100개의 실시간 여정을 실행하는 마일스톤에 가까워지면 100개를 달성할 예정이라는 알림이 UI에 표시됩니다. 이 알림을 받았는데 실시간 여정을 100개 넘게 실행하도록 현재 여정의 수를 확장해야 하는 경우, 고객 지원 센터에 보내는 티켓을 개설해 주시면 Adobe가 목표 달성을 도와 드리겠습니다.
  <!-- DOCAC-10977 * As you publish journeys, we automatically scale and adjust to ensure maximum throughput and stability. As you near the milestone of 500 live journeys at one time, you will see a notification appear in the UI on this achievement. If you see this notification and have a need to extend your journeys beyond 500 live journeys at a time, please create a ticket for customer care and we will help you reach your goals.-->
* 여정에서 대상자 선별을 사용할 때 해당 대상자 선별 활동이 활성화되고 대상자에 들어오거나 나가는 프로필을 확인하는 데 최대 10분이 걸릴 수 있습니다.
* 한 프로필의 여정 인스턴스 최대 크기는 1MB입니다. 여정 실행의 일환으로 수집한 모든 데이터는 해당 여정 인스턴스에 저장됩니다. 따라서 수신 이벤트의 데이터, Adobe Experience Platform에서 검색한 프로필 정보, 사용자 정의 작업 응답 등은 해당 여정 인스턴스에 저장되어 여정 크기에 영향을 줍니다. 여정이 이벤트로 시작하는 경우 여정 실행 시 몇 가지 활동 후에 위의 제한에 도달하지 않도록 해당 이벤트 페이로드의 최대 크기를 제한(예: 800KB 미만)하는 것이 좋습니다. 제한에 도달하면 프로필이 오류 상태가 되어 여정에서 제외됩니다.
* 여정 활동에 사용되는 시간 초과 외에 인터페이스에 표시되지 않고 변경할 수 없는 전체 여정 시간 초과도 있습니다. 이 전역 시간 제한은 개인 사용자가 여정에 들어간 후 91일이 지나면 진행을 중지합니다. [자세히 보기](../building-journeys/journey-properties.md#global_timeout)

### 일반 작업  {#general-actions-g}

여정의 [작업](../building-journeys/about-journey-activities.md)에 다음 가드레일이 적용됩니다.

* 오류가 발생하면 시스템에서 세 번 다시 시도합니다. 수신된 오류 메시지에 따라 재시도 횟수를 조정할 수 없습니다. HTTP 401, 403, 404를 제외한 모든 HTTP 오류에 대해 다시 시도됩니다.
* 기본으로 제공되는 **반응** 이벤트를 사용하면 즉시 사용 가능한 작업에 반응할 수 있습니다. [이 페이지](../building-journeys/reaction-events.md)에서 자세히 알아보십시오. 사용자 정의 액션을 통해 보낸 메시지에 반응하려면 전용 이벤트를 구성해야 합니다.
* 두 가지 작업을 병렬로 배치할 수 없으며 하나씩 추가해야 합니다.
* 프로필은 모든 활성 [버전의 여정](../building-journeys/publishing-the-journey.md#create-a-new-version-of-a-journey-journey-create-new-version)에 대해 동일한 여정에서 동시에 여러 번 나타날 수 없습니다. 재진입이 활성화된 경우 프로필은 여정에 다시 입장할 수 있지만 여정의 이전 인스턴스를 완전히 종료할 때까지는 다시 입장할 수 없습니다. [자세히 보기](../building-journeys/end-journey.md)

### 여정 버전 {#journey-versions-g}

[여정 버전](../start/user-interface.md)에 다음 가드레일이 적용됩니다.

* v1에서 이벤트 활동으로 시작하는 여정은 이후 버전에서 이벤트 이외의 다른 것으로 시작할 수 없습니다. **대상자 선별** 이벤트로 여정을 시작할 수 없습니다.
* v1에서 **대상자 선별** 활동으로 시작하는 여정은 이후 버전에서도 항상 **대상자 선별**&#x200B;로 시작해야 합니다.
* **대상자 선별**(첫 번째 노드)에서 선택한 대상자 및 네임스페이스는 새 버전에서 변경할 수 없습니다.
* 재진입 규칙은 모든 여정 버전에서 동일해야 합니다.
* **대상자 읽기**&#x200B;로 시작하는 여정은 다음 버전에서 다른 이벤트로 시작할 수 없습니다.
* 증분 읽기가 있는 대상자 읽기 여정에 대해서는 새 버전을 만들 수 없습니다. 여정을 복제해야 합니다.

### 사용자 정의 액션 {#custom-actions-g}

여정의 [사용자 정의 작업](../action/action.md)에 다음 가드레일이 적용됩니다.

* 모든 사용자 정의 작업의 호스트 및 샌드박스당 1분간 300,000개의 호출 상한 설정이 정의됩니다. [이 페이지](../action/about-custom-action-configuration.md)를 참조하십시오. 이 제한은 사용자 정의 작업으로 타깃팅된 외부 끝점을 보호하기 위해 고객 사용량을 기준으로 설정되었습니다. 이는 적절한 읽기 속도(사용자 정의 작업 사용 시 프로필 5,000개/초)를 정의함으로써 대상자 기반 여정에서 고려되어야 합니다. 필요한 경우 Capping/Throttling API를 통해 상한 설정 또는 스로틀링 제한을 보다 크게 정의하는 방법으로 이 설정을 재정의할 수 있습니다. [이 페이지](../configuration/external-systems.md)를 참조하십시오.
* 사용자 정의 작업 URL은 동적 매개 변수를 지원하지 않습니다. 
* POST, PUT 및 GET 호출 메서드가 지원됩니다.
* 쿼리 매개 변수 또는 헤더의 이름은 “.” 또는 &quot;$&quot;로 시작해서는 안 됩니다.
* IP 주소를 사용할 수 없습니다. 
* 내부 Adobe 주소(`.adobe.*`)는 URL 및 API에 사용할 수 없습니다.
* 기본 제공 사용자 정의 작업은 제거할 수 없습니다.
* 사용자 정의 작업은 요청 또는 응답 페이로드를 사용하는 경우에만 JSON 형식을 지원합니다. [이 페이지](../action/about-custom-action-configuration.md#custom-actions-limitations)를 참조하십시오.
* 사용자 정의 작업을 사용하여 타깃팅할 엔드포인트를 선택할 때 다음을 확인하십시오.

   * 이 엔트포인트는 제한하는 [Throttling API](../configuration/throttling.md) 또는 [Capping API](../configuration/capping.md)의 구성을 사용하여 여정의 처리량을 지원할 수 있습니다. 스로틀링 구성은 200TPS 미만일 수 없습니다. 타기팅한 모든 엔드포인트는 최소 200TPS를 지원해야 합니다.
   * 이 엔드포인트는 가능한 한 낮은 응답 시간을 가져야 합니다. 예상 처리량에 따라 응답 시간이 길면 실제 처리량에 영향을 줄 수 있습니다.

### 이벤트 {#events-g}

여정의 [이벤트](../event/about-events.md)에 다음 가드레일이 적용됩니다.

* Journey Optimizer가 지원하는 인바운드 여정 이벤트의 최대 볼륨은 초당 5,000개입니다.
* 이벤트 트리거 여정의 첫 번째 액션을 처리하는 데에는 최대 5분이 걸릴 수 있습니다.
* 시스템 생성 이벤트의 경우 고유한 오케스트레이션 ID를 얻으려면 먼저 고객 여정을 시작하는 데 사용되는 스트리밍 데이터를 Journey Optimizer 내에서 구성해야 합니다.. 이 오케스트레이션 ID는 Adobe Experience Platform으로 들어오는 스트리밍 페이로드에 추가되어야 합니다. 이 제한은 규칙 기반 이벤트에는 적용되지 않습니다. 
* 비즈니스 이벤트는 단일 이벤트 또는 대상자 선별 활동과 함께 사용할 수 없습니다. 
* 단일 여정(이벤트 또는 대상자 선별로 시작)에는 동일한 이벤트에 대해 여정이 여러 번 잘못 트리거되는 것을 방지하는 가드레일이 포함됩니다. 프로필 재진입은 기본적으로 5분 동안 일시적으로 차단됩니다. 예를 들어 이벤트가 특정 프로필에 대해 12:01에 여정을 트리거하고 다른 이벤트가 12:03에 도착하는 경우(동일한 이벤트이든 동일한 여정을 트리거하는 다른 이벤트이든) 해당 여정은 이 프로필에 대해 다시 시작되지 않습니다.
* Journey Optimizer에서 여정을 트리거하기 위해서는 이벤트를 Data Collection Core Service(DCCS)로 스트리밍해야 합니다. 배치로 수집된 이벤트 또는 내부 Journey Optimizer 데이터 세트의 이벤트(메시지 피드백, 이메일 추적 등)는 여정을 트리거하는 데 사용할 수 없습니다. 스트리밍 이벤트를 가져올 수 없는 사용 사례의 경우에는 대신 이 이벤트를 기반으로 대상자를 작성하고 **대상자 읽기** 활동을 사용해야 합니다. 대상자 선별의 경우 기술적으로는 사용할 수 있지만, 사용하는 액션에 따라 다운스트림 문제가 발생할 수 있어 권장하지 않습니다.

### 데이터 소스  {#data-sources-g}

여정의 [데이터 원본](../datasource/about-data-sources.md)에 다음 가드레일이 적용됩니다.

* 고객 여정 내에서 외부 데이터 소스를 활용하여 실시간으로 외부 데이터를 조회할 수 있습니다. 이러한 소스는 REST API를 통해 사용할 수 있어야 하고 JSON을 지원하고 요청 볼륨을 처리할 수 있어야 합니다.
* 내부 Adobe 주소(`.adobe.*`)는 URL 및 API에 사용할 수 없습니다.

>[!NOTE]
>
>이제 응답이 지원되므로 외부 데이터 소스 사용 사례에서 데이터 소스 대신 사용자 정의 작업을 사용해야 합니다.

### 여정 및 프로필 만들기  {#journeys-limitation-profile-creation}

Adobe Experience Platform에서 API 기반 프로필 만들기/업데이트와 관련된 지연이 발생합니다. 지연 시간 측면에서 SLT(서비스 수준 목표)는 20,000RPS(초당 요청) 볼륨에서 95번째 백분위수 요청에 대해 수집에서 통합 프로필까지 1분 미만입니다.

프로필 만들기와 동시에 여정이 트리거되고 Profile Service에서 정보를 즉시 확인/검색하면 제대로 작동하지 않을 수 있습니다.

다음 두 가지 솔루션 중 하나를 선택할 수 있습니다.

* 첫 번째 이벤트 후에 대기 활동을 추가하여 Adobe Experience Platform에 Profile Service에 대한 수집을 수행하는 데 필요한 시간을 제공합니다.

* 프로필을 즉시 활용하지 않는 여정을 설정합니다. 예를 들어 여정이 계정 생성을 확인하도록 설계된 경우 경험 이벤트에는 첫 번째 확인 메시지(이름, 성, 이메일 주소 등)를 보내는 데 필요한 정보가 포함될 수 있습니다.

### 프로필 업데이트 {#update-profile-g}

**[!UICONTROL 프로필 업데이트]** 활동에 특정 가드레일이 적용됩니다. [이 페이지](../building-journeys/update-profiles.md)에 나열되어 있습니다.

### 대상자 읽기 {#read-segment-g}

[대상자 읽기](../building-journeys/read-audience.md) 여정 활동에 다음 가드레일이 적용됩니다.

* 스트리밍 대상자는 항상 최신 상태이지만 일괄 처리 대상자는 검색하는 순간에 계산되지 않습니다. 일일 배치 평가 시간에만 매일 평가됩니다.
* **대상자 읽기** 활동을 사용하는 여정의 경우 정확히 동시에 시작할 수 있는 여정의 최대 개수가 정해져 있습니다. 시스템에서 재시도를 수행하기는 하지만, 정확히 같은 시간에 다섯 개가 넘는 여정(**대상자 읽기** 활동이 있거나 예약했거나 “최대한 빨리” 시작하는 여정)을 실행하는 것을 피하기 위해 5~10분 간격을 두는 등 시간을 분산하는 것이 좋습니다.
* **대상자 읽기** 활동은 Adobe Campaign 활동과 함께 사용할 수 없습니다.
* **대상자 읽기** 활동은 비즈니스 이벤트 활동 이후의 여정의 첫 번째 활동으로만 사용할 수 있습니다.
* 여정은 하나의 **대상자 읽기** 활동만 가질 수 있습니다.
* [이 페이지](../building-journeys/read-audience.md)의 **대상자 읽기** 활동을 사용하는 방법에 대한 권장 사항도 참조하십시오.
* 내보내기 작업을 검색하는 동안 대상이 트리거된 여정(**대상자 읽기** 또는 **비즈니스 이벤트**&#x200B;로 시작)에서 기본적으로 다시 시도가 적용됩니다. 내보내기 작업 생성 중 오류가 발생하면 최대 1시간 동안 10분마다 다시 시도됩니다. 그 후에는 실패로 간주합니다. 따라서 이러한 유형의 여정은 예정된 시간보다 최대 1시간 후에 실행될 수 있습니다.

### 대상자 선별 {#audience-qualif-g}

[대상자 선별](../building-journeys/audience-qualification-events.md) 여정 활동에 다음 가드레일이 적용됩니다.

* 대상자 선별 활동은 Adobe Campaign 활동과 함께 사용할 수 없습니다.

### 표현식 편집기  {#expression-editor}

[여정 표현식 편집기](../building-journeys/expression/expressionadvanced.md)에는 다음 가드레일이 적용됩니다.

* 경험 이벤트 필드 그룹은 대상자 읽기, 대상자 선별 또는 비즈니스 이벤트 활동으로 시작하는 여정에서 사용할 수 없습니다. 새 대상자를 만들고 여정에서 대상자 내 조건을 사용해야 합니다.
* `timeSeriesEvents` 속성은 표현식 편집기에서 사용할 수 없습니다. 프로필 수준에서 [경험 이벤트]에 액세스하려면 `XDM ExperienceEvent` 스키마를 기반으로 새 필드 그룹을 만드십시오.


### 인앱 활동 {#in-app-activity-limitations}

**[!UICONTROL 인앱 메시지]** 작업에 다음 가드레일이 적용됩니다. [이 페이지](../in-app/create-in-app.md)에서 인앱 메시지에 대해 자세히 알아보십시오.

* 현재 Healthcare 고객에게는 이 기능이 제공되지 않습니다.

* 개인화에는 프로필 속성만 포함할 수 있습니다.

* 인앱 활동은 Adobe Campaign 활동과 함께 사용할 수 없습니다.

* 인앱 표시는 여정 지속 시간에 연결되어 있습니다. 즉, 특정 프로필에 대한 여정이 종료되면 해당 여정 내의 모든 인앱 메시지는 해당 프로필에 표시되지 않습니다.  따라서 여정 활동에서 바로 인앱 메시지를 중지할 수는 없습니다. 인앱 메시지가 프로필에 표시되지 않도록 하려면 전체 여정을 종료해야 합니다.

* 테스트 모드에서 인앱 표시는 여정의 지속 시간에 따라 달라집니다. 테스트 중에 여정이 너무 일찍 종료되지 않도록 하려면 **[!UICONTROL 대기]** 활동의 **[!UICONTROL 대기 시간]** 값을 조정합니다.

* **[!UICONTROL 반응]** 활동은 인앱 열기 또는 클릭에 반응하는 데 사용할 수 없습니다.

* 사용자 프로필이 캔버스의 인앱 활동에 도달하는 순간과 해당 사용자에게 인앱 메시지가 표시되는 시간 사이에 활성화 지연이 발생할 수 있습니다.

* 인앱 메시지 콘텐츠 크기는 2MB로 제한됩니다. 큰 이미지를 포함하면 게시 프로세스에 지장이 있을 수 있습니다.

### 이동 활동 {#jump-g}

**[!UICONTROL 이동]** 활동에는 특정 가드레일이 적용됩니다. [이 페이지](../building-journeys/jump.md#jump-limitations)에 나열되어 있습니다.

### Campaign 활동 {#ac-g}

**[!UICONTROL Campaign v7/v8]** 및 **[!UICONTROL Campaign Standard]** 활동에는 다음 가드레일이 적용됩니다.

* Adobe Campaign 활동은 [대상자 읽기] 또는 [대상자 선별] 활동과 함께 사용할 수 없습니다.
* 캠페인 활동은 다른 채널 활동(카드, 코드 기반 경험, 이메일, 푸시, SMS, 인앱 메시지, 웹)과 함께 사용할 수 없습니다.
