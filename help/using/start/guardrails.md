---
title: Journey Optimizer 보호 및 제한 사항
description: Journey Optimizer 보호 기능에 대해 자세히 알아보십시오
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: 80a5edec92377753e6bfd96699591b1a87e25248
workflow-type: tm+mt
source-wordcount: '743'
ht-degree: 2%

---

# 보호 및 제한 사항 {#limitations}

자격, 제품 제한 및 성능 보호 기능은 [Adobe Journey Optimizer 제품 설명 페이지](https://helpx.adobe.com/kr/legal/product-descriptions/adobe-journey-optimizer.html){target=&quot;_blank&quot;}.

사용 시 다음과 같은 추가 보호 및 제한 사항이 있습니다 [!DNL Adobe Journey Optimizer].

## 메시지 보호 기능 {#message-guardrails}

* 전자 메일에 첨부 파일을 추가할 수 없습니다 [!DNL Journey Optimizer].
* 같은 전송 도메인을 사용하여 메시지를 보낼 수 없습니다 [!DNL Adobe Journey Optimizer] 및 [!DNL Adobe Campaign] 또는 [!DNL Adobe Marketo Engage] 예.


## 의사 결정 관리 보호 기능 {#offer-guardrails}

의사 결정 관리에 대한 성능 보호 및 정적 제한은 [Adobe Offer decisioning 앱 서비스 제품 설명 페이지](https://helpx.adobe.com/legal/product-descriptions/offer-decisioning-app-service.html){target=&quot;_blank&quot;}.


## 랜딩 페이지는 가드레일을 보장합니다 {#lp-guardrails}

* 하나만 **양식** 구성 요소는 단일 기본 페이지에서 사용할 수 있습니다.
* 다음 **양식** 구성 요소는 하위 페이지에서 사용할 수 없습니다.
* 랜딩 페이지에 사전 헤더를 추가할 수 없습니다.
* 을(를) 선택할 수 없습니다 **직접 코드 작성** 랜딩 기본 페이지를 디자인할 때 선택합니다.

## 여정 가드 레일 {#journeys-guardrails}

### 일반 작업 {#general-actions-g}

* 전송 제한이 없습니다.
* 오류가 발생한 경우 세 번 다시 시도가 체계적으로 수행됩니다. 받은 오류 메시지에 따라 다시 시도 횟수를 조정할 수 없습니다.
* 기본 제공 **반응** 이벤트를 사용하면 기본 작업에 대응할 수 있습니다. 자세한 내용은[ 이 페이지](../building-journeys/reaction-events.md)를 참조하세요. 사용자 지정 작업을 통해 전송된 메시지에 응답하려면 전용 이벤트를 구성해야 합니다.
* 두 작업을 동시에 배치할 수 없으므로 두 작업을 하나씩 추가해야 합니다.
* 오늘날 여정에는 한 프로필이 동시에 여러 번 표시되지 않는 기술적인 제한이 있습니다. 프로필은 여정(설정에 따라)를 다시 입력할 수 있지만 해당 여정의 이전 인스턴스를 완전히 종료한 후에는 해당 프로필을 수행할 수 없습니다.
* 대부분의 경우 프로필이 동일한 여정에 동시에 여러 번 있을 수 없습니다. 다시 여정을 사용하도록 설정하면 프로필이 여정을 다시 입력할 수 있지만, 해당의 이전 인스턴스를 완전히 종료할 때까지 이를 수행할 수 없습니다. [자세히 보기](../building-journeys/journey-end.md)

### 메시지 작업 {#message-action-g}

* 다중 채널 메시지를 추가하면 두 개의 메시지가 전송됩니다.

### 여정 버전 {#journey-versions-g}

* v1에서 이벤트 활동으로 시작하는 여정은 이후 버전의 이벤트 이외의 항목으로 시작할 수 없습니다. 여정은 **세그먼트 자격** 이벤트.
* 다음으로 시작하는 여정 **세그먼트 자격** v1의 활동은 항상 **세그먼트 자격** 추가 버전.
* 에서 선택한 세그먼트 및 네임스페이스 **세그먼트 자격** (첫 번째 노드)는 새 버전에서 변경할 수 없습니다.
* 재시작 규칙은 모든 여정 버전에서 동일해야 합니다.
* 다음으로 시작하는 여정 **세그먼트 읽기** 다음 버전에서 다른 이벤트로 시작할 수 없습니다.

### 사용자 정의 작업 {#custom-actions-g}

* 사용자 지정 작업 URL은 동적 매개 변수를 지원하지 않습니다.
* POST 및 PUT 호출 메서드만 지원됩니다
* 쿼리 매개 변수 또는 헤더의 이름은 &quot;.&quot;로 시작하면 안 됩니다. 또는 &quot;$&quot;
* IP 주소를 사용할 수 없습니다.
* 내부 Adobe 주소(.adobe.) 허용되지 않습니다.

### 이벤트 {#events-g}

* 시스템에서 생성한 이벤트의 경우, 고유한 오케스트레이션 ID를 얻으려면 먼저 Journey Optimizer 내에서 고객 여정을 시작하는 데 사용되는 스트리밍 데이터를 구성해야 합니다. 이 오케스트레이션 ID는 Adobe Experience Platform으로 들어오는 스트리밍 페이로드에 추가해야 합니다. 이 제한은 규칙 기반 이벤트에는 적용되지 않습니다.

### 데이터 소스 {#data-sources-g}

* 고객 여정 내에서 외부 데이터 소스를 활용하여 외부 데이터를 실시간으로 조회할 수 있습니다. 이러한 소스는 REST API를 통해 사용할 수 있어야 하며, JSON을 지원하고, 요청 볼륨을 처리할 수 있어야 합니다.

### 여정 및 프로필 만들기 {#journeys-limitation-profile-creation}

Adobe Experience Platform의 API 기반 프로필 만들기/업데이트와 연관된 지연이 있습니다. 지연에 대한 SLT(서비스 수준 Target)은 RPS(초당 20K 요청 수)로 요청의 95번째 백분위수에 대한 통합 프로필에 대해 수집에서 1분 미만입니다.

여정이 프로필 만들기로 동시에 트리거되고 프로필 서비스에서 정보를 즉시 확인/검색하는 경우 제대로 작동하지 않을 수 있습니다.

다음 두 솔루션 중 하나를 선택할 수 있습니다.

* 첫 번째 이벤트 다음에 대기 활동을 추가하여 Adobe Experience Platform에 프로필 서비스에 수집을 수행해야 하는 시간을 지정합니다.

* 프로필을 즉시 활용하지 않는 여정을 설정합니다. 예를 들어 여정이 계정 만들기를 확인하도록 디자인된 경우 경험 이벤트에는 첫 번째 확인 메시지(이름, 성, 이메일 주소 등)를 전송하는 데 필요한 정보가 포함될 수 있습니다.

### 세그먼트 읽기 {#read-segment-g}

* 스트리밍된 세그먼트는 항상 최신 상태이지만 배치 세그먼트는 검색 시 계산되지 않습니다. 일일 배치 평가 시간에서만 매일 평가됩니다.
