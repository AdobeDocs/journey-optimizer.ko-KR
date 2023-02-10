---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 보호 및 제한 사항
description: Journey Optimizer 보호 기능에 대해 자세히 알아보기
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: 78675ca22d8ee9a93d9af128d5708c305523da78
workflow-type: ht
source-wordcount: '956'
ht-degree: 100%

---

# 보호 및 제한 사항 {#limitations}

자격, 제품 제한 사항, 성능 가드레일 목록은 [Adobe Journey Optimizer 제품 설명 페이지](https://helpx.adobe.com/kr/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}에서 확인하실 수 있습니다.

[시작하기 전에 실시간 고객 프로필 데이터 가드레일](https://experienceleague.adobe.com/docs/experience-platform/profile/guardrails.html?lang=ko){target="_blank"}에 대해서도 알고 있어야 합니다.

[!DNL Adobe Journey Optimizer] 사용 시 다음과 같은 추가 보호 기능 및 제한 사항이 있습니다.

## 메시지 보호 {#message-guardrails}

* [!DNL Journey Optimizer]에서는 이메일에 첨부 파일을 추가할 수 없습니다.
* 동일한 발신 도메인을 사용하여 [!DNL Adobe Journey Optimizer] 및 다른 제품(예: [!DNL Adobe Campaign] 또는 [!DNL Adobe Marketo Engage])에서 메시지를 보낼 수 없습니다.


## 의사 결정 관리 보호 {#offer-guardrails}

의사 결정 관련 성능 가드레일 및 정적 제한 사항 목록은 [Adobe Offer Decisioning App Service 제품 설명 페이지](https://helpx.adobe.com/kr/legal/product-descriptions/offer-decisioning-app-service.html){target="_blank"}에서 확인하실 수 있습니다.


## 랜딩 페이지 보호 {#lp-guardrails}

* 하나의 기본 페이지에서 하나의 **양식** 구성 요소만 사용할 수 있습니다.
* **양식** 구성 요소는 하위 페이지에서 사용할 수 없습니다.
* 랜딩 페이지에 사전 헤더를 추가할 수 없습니다. 
* 방문 기본 페이지를 디자인할 때 **자신만의 코드 작성** 옵션을 선택할 수 없습니다.

## 여정 보호  {#journeys-guardrails}

### 일반 작업  {#general-actions-g}

* 전송 제한이 없습니다. 
* 오류가 발생하면 시스템에서 세 번 다시 시도합니다. 수신된 오류 메시지에 따라 재시도 횟수를 조정할 수 없습니다.
* 기본으로 제공되는 **반응** 이벤트를 사용하면 즉시 사용 가능한 작업에 반응할 수 있습니다. [이 페이지](../building-journeys/reaction-events.md)에서 자세히 알아보십시오. 사용자 지정 작업을 통해 보낸 메시지에 반응하려면 전용 이벤트를 구성해야 합니다.
* 두 가지 작업을 병렬로 배치할 수 없으며 하나씩 추가해야 합니다.
* 대부분의 경우 프로필은 동일한 여정에서 동시에 여러 번 나타날 수 없습니다. 재입력이 활성화된 경우 프로필은 여정에 다시 입력할 수 있지만 여정의 이전 인스턴스를 완전히 종료할 때까지는 다시 입력할 수 없습니다. [자세히 보기](../building-journeys/end-journey.md)

### 여정 버전 {#journey-versions-g}

* v1의 이벤트 활동으로 시작하는 여정은 이후 버전의 이벤트 이외의 다른 것으로 시작할 수 없습니다. **세그먼트 자격** 이벤트로 여정을 시작할 수 없습니다.
* v1에서 **세그먼트 자격** 활동으로 시작하는 여정은 이후 버전에서 항상 **세그먼트 자격**&#x200B;으로 시작해야 합니다.
* **세그먼트 자격**(첫 번째 노드)에서 선택한 세그먼트 및 네임스페이스는 새 버전에서 변경할 수 없습니다.
* 재입력 규칙은 모든 여정 버전에서 동일해야 합니다.
* **세그먼트 읽기**&#x200B;로 시작하는 여정은 다음 버전의 다른 이벤트로 시작할 수 없습니다.

### 사용자 정의 작업 {#custom-actions-g}

* 사용자 정의 작업 URL은 동적 매개 변수를 지원하지 않습니다. 
* POST 및 PUT 호출 메서드만 지원됩니다.
* 쿼리 매개 변수 또는 헤더의 이름은 “.” 또는 &quot;$&quot;로 시작해서는 안 됩니다.
* IP 주소를 사용할 수 없습니다. 
* 내부 Adobe 주소(.adobe.)를 사용할 수 없습니다.

### 이벤트 {#events-g}

* 시스템 생성 이벤트의 경우 고유한 오케스트레이션 ID를 얻으려면 먼저 고객 여정을 시작하는 데 사용되는 스트리밍 데이터를 Journey Optimizer 내에서 구성해야 합니다.. 이 오케스트레이션 ID는 Adobe Experience Platform으로 들어오는 스트리밍 페이로드에 추가되어야 합니다. 이 제한은 규칙 기반 이벤트에는 적용되지 않습니다. 
* 비즈니스 이벤트는 단일 이벤트 또는 세그먼트 자격 활동과 함께 사용할 수 없습니다. 
* 단일 여정(이벤트 또는 세그먼트 자격으로 시작)에는 동일한 이벤트에 대해 여정이 여러 번 잘못 트리거되는 것을 방지하는 보호가 포함됩니다. 프로필 재입력은 기본적으로 5분 동안 일시적으로 차단됩니다. 예를 들어 이벤트가 특정 프로필에 대해 12:01에 여정을 트리거하고 다른 이벤트가 12:03에 도착하는 경우(동일한 이벤트이든 동일한 여정을 트리거하는 다른 이벤트이든) 해당 여정은 이 프로필에 대해 다시 시작되지 않습니다.
* Journey Optimizer에서 여정을 트리거하기 위해서는 이벤트를 Data Collection Core Service(DCCS)로 스트리밍해야 합니다. 배치로 수집된 이벤트 또는 내부 Journey Optimizer 데이터 세트(메시지 피드백, 이메일 추적 등) 이벤트는 여정을 트리거하는 데 사용할 수 없습니다. 스트리밍된 이벤트를 가져올 수 없는 사용 사례의 경우, 이러한 이벤트를 기반으로 세그먼트를 작성하고 **세그먼트 읽기** 활동을 대신 사용하십시오. 세그먼트 자격을 기본적으로 사용할 수 있지만 사용되는 작업에 따라 다운스트림 문제가 발생할 수 있습니다.

### 데이터 소스  {#data-sources-g}

* 고객 여정 내에서 외부 데이터 소스를 활용하여 실시간으로 외부 데이터를 조회할 수 있습니다. 이러한 소스는 REST API를 통해 사용할 수 있어야 하고 JSON을 지원하고 요청 볼륨을 처리할 수 있어야 합니다.

### 여정 및 프로필 만들기  {#journeys-limitation-profile-creation}

Adobe Experience Platform에서 API 기반 프로필 만들기/업데이트와 관련된 지연이 발생합니다. 지연 시간 측면에서 SLT(서비스 수준 목표)는 20,000RPS(초당 요청) 볼륨에서 95번째 백분위수 요청에 대해 수집에서 통합 프로필까지 1분 미만입니다.

프로필 만들기와 동시에 여정이 트리거되고 Profile Service에서 정보를 즉시 확인/검색하면 제대로 작동하지 않을 수 있습니다.

다음 두 가지 솔루션 중 하나를 선택할 수 있습니다.

* 첫 번째 이벤트 후에 대기 활동을 추가하여 Adobe Experience Platform에 Profile Service에 대한 수집을 수행하는 데 필요한 시간을 제공합니다.

* 프로필을 즉시 활용하지 않는 여정을 설정합니다. 예를 들어 여정이 계정 생성을 확인하도록 설계된 경우 경험 이벤트에는 첫 번째 확인 메시지(이름, 성, 이메일 주소 등)를 보내는 데 필요한 정보가 포함될 수 있습니다.

### 세그먼트 읽기 {#read-segment-g}

* 스트리밍된 세그먼트는 항상 최신 상태이지만 일괄 세그먼트는 검색 시 계산되지 않습니다. 일일 배치 평가 시간에만 매일 평가됩니다.
* 세그먼트 읽기 활동을 사용하는 여정의 경우 정확히 동시에 시작할 수 있는 최대 여정 수가 있습니다. 재시도는 시스템에서 수행되지만 5분에서 10분 간격과 같이 시간에 따라 분산하여 정확히 같은 시간에 시작하는 5개 이상의 여정(세그먼트 읽기, 예약 또는 &quot;가능한 한 빨리&quot; 시작)을 초과하는 것은 피하십시오.

### 표현식 편집기  {#expression-editor}

* 경험 이벤트 필드 그룹은 읽기 세그먼트, 세그먼트 자격 또는 비즈니스 이벤트 활동으로 시작하는 여정에서 사용할 수 없습니다.

