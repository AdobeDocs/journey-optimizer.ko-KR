---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 가드레일 및 제한 사항
description: Journey Optimizer 가드레일에 대해 자세히 알아보기
feature: Guardrails
role: User
level: Intermediate
mini-toc-levels: 2
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
TQID: https://experienceleague.adobe.com/k4DqGogrTZ9QrnqyFGwdgDeUI9ivpOd1iSI0c5comuU
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4ebid: ad78185d-8f79-40ad-9bad-cbde74af74ee
subfeature_v2: id: a6c67b0d-bd3e-4d5d-95a8-882e3709d632
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11id: d3cdead0-685a-4489-9250-4bb709942f66id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 26e1073e2fef79ecdfd72ff1c2e5247ec2d62f8a
workflow-type: tm+mt
source-wordcount: 4622
ht-degree: 64%

---


# 가드레일 및 제한 사항 {#limitations}

[!DNL Adobe Journey Optimizer] 사용 시 다음과 같은 가드레일 및 제한 사항이 있습니다.

자격, 제품 제한 사항, 성능 가드레일 목록은 [Adobe Journey Optimizer 제품 설명 페이지](https://helpx.adobe.com/kr/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}에서 확인하실 수 있습니다.

>[!CAUTION]
>
>* [실시간 고객 프로필 데이터 및 세분화에 대한 가드레일](https://experienceleague.adobe.com/ko/docs/experience-platform/profile/guardrails){target="_blank"}이 Adobe Journey Optimizer에도 적용됩니다.
>
>* [실시간 고객 프로필에서 데이터 수집 가드레일](https://experienceleague.adobe.com/ko/docs/experience-platform/ingestion/guardrails){target="_blank"}도 참조하십시오.

## 주요 제한 사항 개요 {#quick-reference}

이 테이블을 사용하여 작성하거나 게시하기 전에 가장 중요한 숫자 제한을 조회합니다. 전체 세부 정보 및 컨텍스트는 아래 섹션에 있습니다.

| 영역 | 제한 | 값 |
|---|---|---|
| **여정** | [여정 당 최대 활동](#journeys-guardrails-journeys) | **50** |
| **여정** | [최대 라이브/일시 중지/시험 실행 여정](#journeys-guardrails-journeys) | **100** |
| **여정** | [여정 인스턴스 크기](#journeys-guardrails-journeys) | **1MB** |
| **여정** | [여정 페이로드 크기(게시)](#journey-payload-size) | **2MB**(90% 경고) |
| **여정** | [전역 여정 시간 초과](#journeys-guardrails-journeys) | **91일** |
| **여정** | [프로필당 보류 중인 이벤트 큐](#journeys-guardrails-journeys) | **10개 이벤트** |
| **여정** | [동시 읽기 대상 인스턴스](#read-segment-g) | 모든 샌드박스에서 **5** |
| **여정** | [대상 샌드박스 읽기 처리량](#read-segment-g) | **20,000개 프로필/초**(공유) |
| **여정** | [대상자 읽기 작업 시간 초과](#read-segment-g) | **12시간** |
| **채널** | [초당 인바운드 요청](#inbound-guardrails) | **5,000RPS** |
| **채널** | [최대 활성 인바운드 동작](#inbound-guardrails) | **500** |
| **채널** | [트랜잭션 메시지/초(캠페인)](#transactional-message-guardrails) | **500** |
| **채널** | [초당 인바운드 여정 이벤트](#events-g) | **5,000** |
| **사용자 지정 작업** | [분당 호출 수(응답 &lt; 0.75초)](#custom-actions-g) | 호스트/샌드박스당 **300,000 / 분** |
| **사용자 지정 작업** | [30초당 호출 수(응답 > 0.75초)](#custom-actions-g) | 호스트/샌드박스당 **150,000 / 30초** |
| **콘텐츠** | [게시의 전자 메일 메시지 콘텐츠](#message-content-size) | **2MB**(1MB 미만 작성자) |
| **콘텐츠** | [인앱 메시지 콘텐츠](#in-app-activity-limitations) | **2MB** |
| **콘텐츠** | [시각적 조각 크기](#fragments-guardrails) | **100KB** |
| **콘텐츠** | [식 조각 크기](#fragments-guardrails) | **200KB** |
| **콘텐츠** | [여정 조각 노드](#fragments-journey-g) | **20개 노드/조각**, 200개 활성/샌드박스 |
| **대상자** | [샌드박스당 대상 구성](#audience) | **10** |
| **데이터 세트** | [프로필 저장소 TTL(새 조직/샌드박스)](#datasets-guardrails) | **90일** |
| **데이터 세트** | [데이터 레이크 TTL(새 조직/샌드박스)](#datasets-guardrails) | **13개월** |


## 시스템 및 플랫폼 {#system-platform}

### 지원되는 브라우저 {#browsers}

Adobe [!DNL Journey Optimizer] 인터페이스는 최신 버전의 Google Chrome에서 최적으로 작동되도록 디자인되었습니다. 이전 버전 또는 기타 브라우저에서 특정 기능을 사용하는 데 문제가 있을 수 있습니다.

### 데이터 세트 가드레일 {#datasets-guardrails}

2025년 2월부터 **새로운 샌드박스와 새로운 조직**&#x200B;에서 Journey Optimizer 시스템 생성 데이터 세트에 다음과 같은 TTL(Time-to-Live) 가드레일이 롤아웃됩니다.

* 프로필 저장소의 데이터에 대한 **90일**
* 데이터 레이크의 데이터에 대한 **13개월**

이 변경 사항은 차후 **기존 고객 샌드박스**&#x200B;에 대해서도 롤아웃됩니다. [데이터 세트 TTL(Time-To-Leave) 가드레일에 대해 자세히 알아보기](../data/datasets-ttl.md)

## 채널 및 메시지 {#channel-guardrails}

이 섹션에서는 이메일, SMS, 인바운드 채널(웹, 인앱, 코드 기반, 콘텐츠 카드) 및 트랜잭션 메시지를 포함한 모든 커뮤니케이션 채널에 대한 가드레일을 다룹니다.

>[!NOTE]
>
>드문 경우지만 특정 지역에서 일시적으로 서비스가 중단되면 유효한 프로필이 여정에서 제외되거나 메일이 바운스로 잘못 표시될 수 있습니다. 서비스가 복원되면 여정 로그를 재점검하고 동의 프로필 필드를 확인한 다음 필요한 경우 여정을 다시 게시합니다. ISP 중단 시 금지 목록에서 프로필을 제거하는 방법은 [이 섹션](../configuration/manage-suppression-list.md#remove-from-suppression-list)에서 확인할 수 있습니다.

### 이메일 가드레일 {#message-guardrails}

[이메일 채널](../email/get-started-email.md)에 다음 가드레일이 적용됩니다.

* 동일한 발신 도메인을 사용하여 [!DNL Adobe Journey Optimizer] 및 다른 제품(예: [!DNL Adobe Campaign] 또는 [!DNL Adobe Marketo Engage])에서 이메일 메시지를 보낼 수 없습니다.

이메일 메시지를 디자인할 때 시스템은 주요 설정을 확인하고 경고(권장 사항 및 모범 사례)와 오류(테스트 또는 활성화를 방해하는 차단 문제)에 대한 알림을 표시합니다. [이 섹션](../email/create-email.md#check-email-alerts)에서 이메일 경고 및 유효성 검사 요구 사항에 대해 자세히 알아보십시오.

#### 여정 게시용 메시지 콘텐츠 크기 {#message-content-size}

전자 메일 메시지가 포함된 여정을 게시할 때 백 엔드를 처리한 후 총 메시지 콘텐츠 크기는 **2MB**&#x200B;를 초과할 수 없습니다. 게시 중에 시스템은 링크, 이미지를 패치하고 변형을 적용하여 메시지 콘텐츠를 자동으로 처리하므로 페이로드 크기가 작성된 콘텐츠 크기 이상으로 증가합니다.

>[!CAUTION]
>
>최종 처리된 메시지 콘텐츠가 **2MB**&#x200B;를 초과하면 여정 게시가 실패합니다. 백엔드 처리 오버헤드에 대해 300-400KB의 버퍼를 허용하도록 작성된 메시지 콘텐츠를 2MB 미만(이상적으로는 **1MB** 미만)으로 유지하십시오.

**게시 실패를 방지하는 모범 사례:**

* 작성된 전자 메일 콘텐츠를 **1MB** 미만으로 유지
* 콘텐츠 변형 수 최소화
* 메시지에 추가하기 전에 이미지를 최적화하고 압축하기
* 사용하지 않는 에셋 및 불필요한 HTML 요소 제거
* 프로덕션에 여정을 게시하기 전에 메시지 크기 테스트

컨텐츠 크기로 인해 여정 게시가 실패하면 메시지 컨텐츠를 줄이고 여정을 다시 게시하십시오.

### SMS 가드레일 {#sms-guardrails}

[SMS 채널](../mobile/get-started-mobile.md) 활동에 다음 가드레일이 적용됩니다.

* 지원 URL을 통해 MMS에 넣을 미디어 파일을 포함할 수 있습니다. 미디어 파일이 별도로 업로드되는지 확인해야 합니다.
* 현재 MMS에는 메시지 피드백 동기화를 사용할 수 없습니다.
* MMS에 대한 동의 관리는 SMS 채널 수준에서 작동합니다.

### 인바운드 채널 가드레일 {#inbound-guardrails}

* [!DNL Journey Optimizer]에서 [코드 기반 경험](../code-based/get-started-code-based.md) 액션을 사용하고 애플리케이션에서 사용할 수 있는 코드 콘텐츠 페이로드를 전달하려면 [이 페이지](../code-based/code-based-prerequisites.md)에서 설명하는 전제 조건을 따라야 합니다.

* [!DNL Journey Optimizer] 사용자 인터페이스에서 [웹 페이지](../web/get-started-web.md)에 액세스하고 작성하려면 [이 페이지](../web/web-prerequisites.md)에 나열된 필수 구성 요소를 따르세요.

* [!DNL Journey Optimizer]를 사용하여 여정 및 캠페인에서 인앱 메시지를 보내려면 [이 페이지](../in-app/inapp-configuration.md)에 나열된 게재 필수 조건을 따르세요.

* Adobe Journey Optimizer에서 콘텐츠 카드를 올바르게 표시하려면 [이 페이지](../content-card/content-card-configuration-prereq.md)에 나열된 Adobe Experience Platform 설정을 구성해야 합니다.

* Journey Optimizer은 **초당 5,000개의 인바운드 요청**&#x200B;의 최대 볼륨을 지원합니다. 이 가드레일은 Journey Optimizer에서 지원하는 인바운드 채널([웹](../web/get-started-web.md), [인앱](../in-app/get-started-in-app.md), [코드 기반 경험](../code-based/get-started-code-based.md), [콘텐츠 카드](../../rp_landing_pages/content-card-landing-page.md))에서 발생할 수 있는 모든 인바운드 요청에 적용됩니다.

* Journey Optimizer은 언제든지 최대 **500개의 활성 인바운드 작업**&#x200B;을 지원합니다. 이 인바운드 액션은 라이브 캠페인의 일부이거나 라이브 여정에 사용되는 노드인 경우 계산됩니다. 이 수에 도달하면 새 캠페인을 시작하기 전에 인바운드 액션을 사용하는 이전 캠페인이나 여정을 비활성화해야 합니다.

#### 인바운드 채널을 통한 프로필 관리 {#profile-management-inbound}

[!DNL Journey Optimizer] 인바운드 채널은 익명 프로필을 타기팅할 수 있습니다. 즉, 다른 채널에서 이전에 참여하지 않았으므로 인증되지 않았거나 아직 알 수 없는 프로필을 의미합니다. 이 경우는 예를 들어 ECID와 같은 임시 ID를 기반으로 모든 방문자 또는 대상을 타기팅할 때 해당됩니다.

이렇게 하면 총 참여 가능 프로필 수가 증가하므로, 사용자가 계약 시 구입한 참여 가능 프로필 수를 초과하는 경우 비용이 발생할 수 있습니다. 각 패키지별 라이선스 지표 목록은 [Journey Optimizer 제품 설명](https://helpx.adobe.com/kr/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"} 페이지에서 확인할 수 있습니다. [라이선스 사용 대시보드](../audience/license-usage.md)에서 참여 가능한 프로필 수를 확인할 수 있습니다.

참여 가능한 프로필을 합리적인 제한 이내로 유지하려면 Adobe에서는 TTL(Time-To-Live)을 설정하여 특정 기간 내에 방문하거나 참여한 적이 없는 경우 실시간 고객 프로필에서 익명 프로필을 자동으로 삭제할 것을 권장합니다. Adobe에서는 현재 Edge 프로필 TTL과 일치하도록 TTL 값을 **14일**(으)로 설정하는 것이 좋습니다.

>[!NOTE]
>
>[Experience Platform 설명서](https://experienceleague.adobe.com/ko/docs/experience-platform/profile/pseudonymous-profiles){target="_blank"}에서 익명 프로필에 대한 데이터 만료를 구성하는 방법에 대해 알아봅니다.

### 트랜잭션 메시지 가드레일 {#transactional-message-guardrails}

Journey Optimizer은 캠페인에서 최대 볼륨 **초당 500개의 트랜잭션 메시지**&#x200B;를 지원합니다.

## 콘텐츠 및 자산 {#content-assets}

이 섹션에서는 랜딩 페이지, 하위 도메인, 조각을 포함한 콘텐츠 제작 및 관리에 대한 가드레일을 다룹니다.

### AI Assistant 보호 {#ai-assistant-g}

지원되는 채널(이메일, 푸시, 웹, SMS) 및 개인화 편집기 제한을 포함하여 **AI Assistant 콘텐츠 생성**&#x200B;에 대한 보호 기능 및 제한 사항이 [이 페이지](../content-management/gs-generative.md#generative-guardrails)에 나열되어 있습니다.

### 랜딩 페이지 보호 {#lp-guardrails}

[랜딩 페이지](../landing-pages/get-started-lp.md)에 다음 가드레일이 적용됩니다.

* 하나의 기본 페이지에서 하나의 **양식** 구성 요소만 사용할 수 있습니다.
* **양식** 구성 요소는 하위 페이지에서 사용할 수 없습니다.
* 랜딩 페이지에 사전 헤더를 추가할 수 없습니다.
* 방문 기본 페이지를 디자인할 때 **자신만의 코드 작성** 옵션을 선택할 수 없습니다.

### 하위 도메인 가드레일 {#subdomain-guardrails}

Journey Optimizer의 하위 도메인 위임에 적용되는 가드레일 및 제한 사항에 대해서는 [이 페이지](../configuration/delegate-subdomain.md#guardrails)에 자세히 설명되어 있습니다.

### 조각 가드레일 {#fragments-guardrails}

[조각](../content-management/fragments.md)에 다음 가드레일이 적용됩니다.

* 조각을 만들고, 편집하고, 보관하고, 게시하려면 **[!DNL Content Library Manager]** 제품 프로필에 포함된 **[!DNL Manage library items]** 및 **[조각 게시]** 권한이 필요합니다. [자세히 알아보기](../administration/ootb-product-profiles.md#content-library-manager)
* 시각적 조각은 이메일 채널에만 사용할 수 있습니다.
* 인앱 채널에는 표현식 조각을 사용할 수 없습니다.
* 시각적 조각은 **100KB**&#x200B;을(를) 초과할 수 없습니다. 식 조각은 **200KB**&#x200B;을(를) 초과할 수 없습니다.
* 이제 여정 또는 캠페인에서 조각을 사용하려면 해당 조각이 **라이브** 상태여야 합니다.
* [컨텍스트 속성](../personalization/personalization-build-expressions.md)은 조각 내에서 지원되지 않습니다.
* 테마 사용 모드와 수동 스타일 모드 간에는 시각적 조각이 상호 호환되지 않습니다. 테마를 적용할 콘텐츠에서 조각을 사용할 수 있으려면 테마 사용 모드에서 이 조각을 만들어야 합니다. [테마에 대해 자세히 알아보기](../email/apply-email-themes.md)
* 여정 또는 캠페인에서 추적이 활성화되면 조각에 링크를 추가하고 이 조각을 메시지에 사용하는 경우 메시지에 포함된 다른 모든 링크와 같이 이러한 링크가 추적됩니다. [링크 및 추적에 대해 자세히 알아보기](../email/message-tracking.md)

## 대상자 및 프로필 {#audiences-profiles}

이 섹션에서는 대상자 관리, 프로필 처리, 활용 가능한 프로필 고려 사항에 대한 가드레일을 다룹니다.

### 대상자 및 프로필 가드레일 {#audience}

* 지정된 샌드박스에서 최대 **10개의 대상 구성**&#x200B;을 게시할 수 있습니다. 이 임계값에 도달한 경우 컴포지션을 삭제하여 공간을 확보하고 새 컴포지션을 게시해야 합니다.

  [이 페이지](../audience/get-started-audience-orchestration.md)에서 대상자 컴포지션에 대해 자세히 알아보십시오.

* 데이터를 수집할 때 이메일은 대소문자를 구분합니다. 즉, 중복 프로필을 만들어(예: John.Greene@luma.com 프로필 하나, john.greene@luma.com 프로필 하나) [!DNL Journey Optimizer] 여정 및 캠페인에서 해당 수신자를 타기팅할 때 사용할 수 있습니다.

* 인바운드 채널을 통해 익명 프로필(인증되지 않은 방문자)을 타기팅할 때 자동 프로필 삭제에 대한 TTL(Time-To-Live)을 설정하여 참여 가능한 프로필 수 및 관련 비용을 관리하는 것이 좋습니다. [자세히 알아보기](#profile-management-inbound)

## 의사 결정 관리 {#decision-management}

### 의사 결정 및 의사 결정 관리 가드레일 {#decisioning-guardrails}

의사 결정이나 의사 결정 관리 기능으로 작업할 때 기억해야 할 가드레일과 제한 사항은 의사 결정 및 의사 결정 관리 섹션에서 자세히 설명합니다.

* [의사 결정 가드레일 및 제한 사항](../experience-decisioning/decisioning-guardrails.md)
* [의사 결정 관리 가드레일 및 제한 사항](../offers/decision-management-guardrails.md)

## 여정 {#journeys-guardrails}

이 섹션에서는 일반적인 여정 제한 사항, 여정 구성 요소(액션, 이벤트, 데이터 소스), 여정 활동, 사용자 정의 액션과 표현식 편집기 등 특정 기능을 포함하여 여정에 대한 가드레일과 제한 사항을 설명합니다.

### 일반 여정 가드레일 {#journeys-guardrails-journeys}

* 여정의 활동 수는 **50**(으)로 제한됩니다. 활동 수는 여정 캔버스의 왼쪽 위 섹션에 표시됩니다.

  이 제한에 근접한 여정은 편집 및 게시 성능이 저하되고 저장 또는 유효성 검사 오류가 발생할 수 있습니다. 이 경우 [이동 활동](../building-journeys/jump.md)을 사용하여 여정을 더 작은 하위 여정으로 분할하거나 새 버전으로 다시 만드십시오. 활동 제한을 늘릴 수 없습니다.

* 기본적으로 한 번에 라이브/일시 중지/드라이 실행 여정 수는 **100**(으)로 제한됩니다. 현재 여정 수는 여정 캔버스 위에 표시됩니다.

  여정을 게시하면 처리량과 안정성을 최대화하기 위해 자동으로 규모를 조절합니다. 한 번에 100개의 실시간 여정을 실행하는 마일스톤에 가까워지면 100개를 달성할 예정이라는 알림이 UI에 표시됩니다. 이 알림을 받았는데 실시간 여정을 100개 넘게 실행하도록 현재 여정의 수를 확장해야 하는 경우, 고객 지원 센터에 보내는 티켓을 개설해 주시면 Adobe가 목표 달성을 도와 드리겠습니다.

* 여정에서 대상 자격을 사용할 때 해당 대상 자격 활동이 활성 상태가 되고 대상을 입력하거나 나가는 프로필을 수신하는 데 최대 **10분**&#x200B;이 걸릴 수 있습니다.

* 프로필의 여정 인스턴스의 최대 크기는 **1MB**&#x200B;입니다. 여정 실행의 일환으로 수집한 모든 데이터는 해당 여정 인스턴스에 저장됩니다. 따라서 수신 이벤트 데이터, Adobe Experience Platform에서 가져온 프로필 정보, 사용자 정의 액션 응답 등이 해당 여정 인스턴스에 저장되어 여정 크기에 영향을 미칩니다. 여정이 이벤트로 시작할 때 여정 실행에서 몇 가지 활동 후에 해당 제한에 도달하지 않도록 해당 이벤트 페이로드의 최대 크기(예: **800KB** 미만)를 제한하는 것이 좋습니다. 제한에 도달하면 프로필이 오류 상태가 되어 여정에서 제외됩니다.

* 각 프로필 및 여정 버전에 대해 여정 런타임에서는 하나가 처리되는 동안 최대 **10개의 보류 중인 이벤트**&#x200B;의 내부 큐를 유지합니다. 이 한도에 도달하면 스택이 비워질 때까지 추가 이벤트는 `maxInstanceStackEventsReached` 이유와 함께 삭제됩니다. [차단된 여정 인스턴스로 인해 폐기된 이벤트](../building-journeys/troubleshooting-execution.md#max-instance-stack-events-reached)를 참조하세요.

* 여정 활동에 사용되는 시간 초과 외에 인터페이스에 표시되지 않고 변경할 수 없는 전체 여정 시간 초과도 있습니다. 이 전역 시간 제한은 입력한 후 **91일** 여정에서 개인 사용자의 진행률을 중지합니다. [자세히 보기](../building-journeys/journey-properties.md#global_timeout)

>[!TIP]
>
>**다음 중 무엇을 의미합니까:** **50-활동 제한** 및 **100-live-여정 제한**&#x200B;은(는) 크기를 조정할 때 대부분의 팀이 먼저 경험하는 두 개의 가드레일입니다. 샌드박스 처리량 경합을 방지하기 위해 여정 분할 작업을 조기에 계획하고 대상 읽기 시작 시간을 최소 5~10분 간격으로 분산합니다.

#### 여정 페이로드 크기 유효성 검사 {#journey-payload-size}

여정을 저장하거나 게시할 때 Journey Optimizer가 안정성과 성능을 유지하기 위해 총 여정 페이로드 크기를 확인합니다.

| 시나리오 | 임계값 | 비헤이비어 |
|---|---|---|
| 페이로드 제한의 90% 미만 | 경고 이하 | 여정이 저장하고 성공적으로 게시했습니다. 경고 또는 오류가 표시되지 않습니다. |
| 제한의 90-99% 페이로드 | 경고(소프트) | 여정이 저장되며 경고가 게시됩니다. **경고**: 여정 페이로드 크기가 한도에 가깝습니다. 가장 큰 노드: &#39;[NodeName]&#39;(형식: &#39;[NodeType]&#39;, 크기: [N]바이트). |
| 페이로드≥ 100% 제한 | **오류(하드)** | 저장 또는 게시가 차단되었습니다. **HTTP 413 요청 엔터티가 너무 큼**&#x200B;을 반환합니다. 오류: 여정 페이로드 크기가 한도를 초과했습니다. 가장 큰 노드: &#39;[NodeName]&#39;(형식: &#39;[NodeType]&#39;, 크기: [N]바이트). |

**기본 구성**

* **기본 최대 요청 크기**: **2MB**(2,000,000바이트). 일부 조직에는 Adobe에서 구성한 사용자 정의 제한이 있을 수 있습니다.
* **경고 임계값**: 최대 제한의 90%.
* **오류 임계값**: 최대 제한의 100%.

**문제 해결 및 권장 사항**

* 경고 또는 오류에 표시된 가장 큰 노드를 검토합니다.
* 조건을 단순화하고, 데이터 매핑을 줄이고, 불필요한 단계 또는 매개 변수를 제거합니다.
* 필요한 경우 여정을 더 작은 여러 여정으로 분할할 수도 있습니다.
* 조직에 더 높은 제한이 필요하다고 판단되는 경우 Adobe 담당자에게 문의하십시오.

게시하기 전에 여정의 현재 페이로드 크기를 모니터링하려면 여정 속성 패널에서 **[!UICONTROL 현재 여정 페이로드 크기]** 표시기를 사용하십시오. [여정 페이로드 크기를 확인하는 방법을 알아봅니다](../building-journeys/journey-properties.md#journey-payload-size)

### 라이선스 패키지 비교 {#select-package-limitations}

>[!NOTE]
>
>아래 패키지 선택 제한 사항은 대상자 읽기 또는 비즈니스 이벤트 여정에 적용되지 않습니다. 여러 액션, 조건 또는 대기 활동이 포함된 더욱 복잡한 여정 로직이 필요한 경우, 라이선스 패키지를 업그레이드하거나 적용 가능한 경우 읽기 대상자 여정을 사용하는 것을 고려해 보세요.

**Select** 라이선스 패키지를 사용하는 고객의 경우 다음의 추가 제한이 단일 여정(이벤트 또는 대상 자격으로 시작하는 여정)에 특별히 적용됩니다.

| 제한 사항 | 오류 코드 | 설명 |
|---|---|---|
| 하나의 작업만 허용됨 | `ERR_PKG_SELECT_8` | 단일 여정은 **one** 동작 활동만 포함할 수 있습니다. 동일한 여정 내에서 여러 개의 이메일, 푸시, SMS 또는 기타 작업 활동을 사용할 수 없습니다. |
| 허용된 조건 없음 | `ERR_PKG_SELECT_7` | 조건 활동은 단일 여정에서 사용할 수 없습니다. 여정은 분기 로직 없이 단일 선형 경로를 따라야 합니다. |
| 대기 활동 없음 | `ERR_PKG_SELECT_6` | 대기 활동을 단일 여정에 추가할 수 없습니다. 액션은 지연 없이 즉시 실행해야 합니다. |
| 시간 초과/오류 전환은 종료 노드로 이동해야 함 | `ERR_PKG_SELECT_2` | 작업(예: 이메일 작업)에 대한 시간 초과 또는 오류 전환을 구성하는 경우 이러한 경로는 직접 최종 노드를 가리켜야 합니다. 여정의 다른 활동이나 액션과 연결될 수 없습니다. |

>[!TIP]
>
>**Select 패키지에 있고 분기 논리, 대기 활동 또는 여러 작업이 필요한 경우 대신 대상자 읽기 여정을 사용하거나 Adobe 담당자에게 패키지 업그레이드에 대해 문의해야 합니다.**

### 일반 작업 {#general-actions-g}

여정의 [작업](../building-journeys/about-journey-activities.md)에 다음 가드레일이 적용됩니다.

* 오류가 발생하면 시스템에서 세 번 다시 시도합니다. 수신된 오류 메시지에 따라 재시도 횟수를 조정할 수 없습니다. HTTP 401, 403, 404를 제외한 모든 HTTP 오류에 대해 다시 시도됩니다.
* 기본으로 제공되는 **반응** 이벤트를 사용하면 즉시 사용 가능한 작업에 반응할 수 있습니다. [이 페이지](../building-journeys/reaction-events.md)에서 자세히 알아보십시오. 사용자 정의 액션을 통해 보낸 메시지에 반응하려면 전용 이벤트를 구성해야 합니다.
* 두 가지 작업을 병렬로 배치할 수 없으며 하나씩 추가해야 합니다.
* 프로필은 모든 활성 [버전의 여정](../building-journeys/publish-journey.md#journey-create-new-version)에 대해 동일한 여정에서 동시에 여러 번 나타날 수 없습니다. 재진입이 활성화된 경우 프로필은 여정에 다시 입장할 수 있지만 여정의 이전 인스턴스를 완전히 종료할 때까지는 다시 입장할 수 없습니다. [자세히 보기](../building-journeys/end-journey.md)

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

| 가드레일 | 값 | 참고 |
|---|---|---|
| 최대 한도 — 응답 &lt; 0.75 s | 호스트 및 샌드박스당 **300,000회 호출/분** | 슬라이딩 윈도우. 샌드박스 및 엔드포인트별로 강제 적용됩니다. |
| 한도 설정 — 응답 > 0.75초 | 호스트 및 샌드박스당 **150,000회 호출/30초** | 슬라이딩 윈도우. 끝점 지연 시간이 0.75초를 초과할 때 별도의 제한이 적용됩니다. |
| URL 유형 | 정적 전용 | 사용자 지정 작업 URL의 동적 매개 변수는 지원되지 않습니다. |
| 지원되는 HTTP 메서드 | POST, PUT, GET | 다른 메서드는 지원되지 않습니다. |
| 쿼리 매개 변수/헤더 이름 형식 | `.` 또는 `$`(으)로 시작할 수 없습니다. | 이 문자로 시작하는 이름은 거부됩니다. |
| URL의 IP 주소 | 허용되지 않음 | IP 주소 대신 호스트 이름을 사용하십시오. |
| 내부 Adobe 주소 | 허용되지 않음 | URL 및 API에는 `.adobe.*` 주소를 사용할 수 없습니다. |
| 기본 제공 사용자 지정 작업 | 제거할 수 없음 | 기본 제공 사용자 지정 작업은 영구적입니다. |
| 페이로드 형식 | JSON만 | JSON 형식은 요청 및 응답 페이로드 모두에 필요합니다. [이 페이지](../action/about-custom-action-configuration.md#custom-actions-limitations)를 참조하십시오. |
| 최소 엔드포인트 처리량 | 200TPS | 사용자 지정 작업으로 타깃팅된 모든 끝점은 최소 200개의 TPS를 지원해야 합니다. |

>[!TIP]
>
>**이 방법은 다음을 의미합니다.** 기본 호출 수/분 제한은 외부 끝점이 여정 처리량에 의해 압도되지 않도록 보호합니다. 끝점에서 더 많은 로드를 처리할 수 있는 경우 [API 최대 가용량](../configuration/capping.md) 또는 [API 제한](../configuration/throttling.md)을 사용하여 이 제한을 늘릴 수 있습니다. 더 높은 조직 제한이 필요한 경우 Adobe 담당자에게 문의하십시오.

이 제한은 사용자 정의 작업으로 타깃팅된 외부 끝점을 보호하기 위해 고객 사용량을 기준으로 설정되었습니다. 필요한 경우 Capping/Throttling API를 통해 상한 설정 또는 스로틀링 제한을 보다 크게 정의하는 방법으로 이 설정을 재정의할 수 있습니다. [이 페이지](../configuration/external-systems.md)를 참조하십시오.

### 이벤트 {#events-g}

여정의 [이벤트](../event/about-events.md)에 다음 가드레일이 적용됩니다.

* Journey Optimizer은 모든 샌드박스에서 최대 볼륨인 **초당 5,000개의 인바운드 여정 이벤트**&#x200B;를 지원합니다. [이 페이지](../event/about-events.md#event-thoughput)에서 이 제한에 대해 자세히 알아보십시오.
* 여정에서 첫 번째 작업을 처리하는 데 최대 **5분**&#x200B;이 걸릴 수 있습니다.
* 시스템 생성 이벤트의 경우 고유한 오케스트레이션 ID를 얻으려면 먼저 고객 여정을 시작하는 데 사용되는 스트리밍 데이터를 Journey Optimizer 내에서 구성해야 합니다.. 이 오케스트레이션 ID는 Adobe Experience Platform으로 들어오는 스트리밍 페이로드에 추가되어야 합니다. 이 제한은 규칙 기반 이벤트에는 적용되지 않습니다.
* 비즈니스 이벤트는 단일 이벤트 또는 대상자 선별 활동과 함께 사용할 수 없습니다.
* 단일 여정(이벤트 또는 대상자 선별로 시작)에는 동일한 이벤트에 대해 여정이 여러 번 잘못 트리거되는 것을 방지하는 가드레일이 포함됩니다. 프로필 재입력은 기본적으로 **5분** 동안 일시적으로 차단됩니다. 예를 들어 이벤트가 특정 프로필에 대해 12:01에 여정을 트리거하고 다른 이벤트가 12:03에 도착하는 경우(동일한 이벤트이든 동일한 여정을 트리거하는 다른 이벤트이든) 해당 여정은 이 프로필에 대해 다시 시작되지 않습니다.
* Journey Optimizer에서 여정을 트리거하기 위해서는 이벤트를 Data Collection Core Service(DCCS)로 스트리밍해야 합니다. 배치로 수집된 이벤트, **쿼리 서비스**&#x200B;를 통해 삽입된 이벤트 또는 내부 Journey Optimizer 데이터 세트의 이벤트(메시지 피드백, 이메일 추적 등)는 여정을 트리거하는 데 사용할 수 없습니다. 스트리밍 이벤트를 가져올 수 없는 사용 사례의 경우에는, 이 이벤트를 기반으로 대상자를 구축하고 **대상자 읽기** 활동을 대신 사용해야 합니다. 대상자 선별의 경우 기술적으로는 사용할 수 있지만, 사용하는 액션에 따라 다운스트림 문제가 발생할 수 있어 권장하지 않습니다.

### 데이터 소스 {#data-sources-g}

여정의 [데이터 원본](../datasource/about-data-sources.md)에 다음 가드레일이 적용됩니다.

* 고객 여정 내에서 외부 데이터 소스를 활용하여 실시간으로 외부 데이터를 조회할 수 있습니다. 이러한 소스는 REST API를 통해 사용할 수 있어야 하고 JSON을 지원하고 요청 볼륨을 처리할 수 있어야 합니다.
* 내부 Adobe 주소(`.adobe.*`)는 URL 및 API에 사용할 수 없습니다.

>[!NOTE]
>
>이제 응답이 지원되므로 외부 데이터 소스 사용 사례에서 데이터 소스 대신 사용자 정의 작업을 사용해야 합니다.

### 여정 및 프로필 만들기 {#journeys-limitation-profile-creation}

Adobe Experience Platform에서 API 기반 프로필 만들기/업데이트와 관련된 지연이 발생합니다. 지연 시간 측면에서 SLT(서비스 수준 목표)는 **20K RPS(초당 요청 수)**&#x200B;의 볼륨에서 95번째 백분위수 요청에 대해 수집에서 통합 프로필까지 1분 미만입니다.

프로필 만들기와 동시에 여정이 트리거되고 Profile Service에서 정보를 즉시 확인/검색하면 제대로 작동하지 않을 수 있습니다.

다음 두 가지 솔루션 중 하나를 선택할 수 있습니다.

* 첫 번째 이벤트 후에 대기 활동을 추가하여 Adobe Experience Platform에 Profile Service에 대한 수집을 수행하는 데 필요한 시간을 제공합니다.

* 프로필을 즉시 활용하지 않는 여정을 설정합니다. 예를 들어 여정이 계정 생성을 확인하도록 설계된 경우 경험 이벤트에는 첫 번째 확인 메시지(이름, 성, 이메일 주소 등)를 보내는 데 필요한 정보가 포함될 수 있습니다.

### 보조 식별자 {#supplemental}

여정에서 보조 식별자를 사용할 때는 특정 가드레일이 적용됩니다. [이 페이지](../building-journeys/supplemental-identifier.md#guardrails)에 나열되어 있습니다.

### 표현식 편집기 {#expression-editor}

[여정 표현식 편집기](../building-journeys/expression/expressionadvanced.md)에는 다음 가드레일이 적용됩니다.

* 경험 이벤트 필드 그룹은 대상자 읽기, 대상자 선별 또는 비즈니스 이벤트 활동으로 시작하는 여정에서 사용할 수 없습니다. 새 대상자를 만들고 여정에서 대상자 내 `inaudience` 조건을 사용해야 합니다.
* `timeSeriesEvents` 속성은 표현식 편집기에서 사용할 수 없습니다. 프로필 수준에서 [경험 이벤트]에 액세스하려면 `XDM ExperienceEvent` 스키마를 기반으로 새 필드 그룹을 만드십시오.

### 여정 활동 {#activities}

#### 대상자 선별 활동 {#audience-qualif-g}

[대상자 선별](../building-journeys/audience-qualification-events.md) 여정 활동에 다음 가드레일이 적용됩니다.

* 대상자 선별 활동은 Adobe Campaign 활동과 함께 사용할 수 없습니다.
* 보조 식별자는 대상자 자격 여정에서 지원되지 않습니다.

[이 섹션](../building-journeys/entry-management.md#journey-processing-rate)에서 여정 처리 속도 및 처리량 제한에 대해 자세히 알아보십시오.

스트리밍 및 배치 대상에 대한 권장 사항과 구성 대상 제한 사항을 포함하는 추가 보호 기능은 [이 페이지](../building-journeys/audience-qualification-events.md#audience-qualification-guardrails)에 나열되어 있습니다.

#### Campaign 활동 {#ac-g}

**[!UICONTROL Campaign v7/v8]** 및 **[!UICONTROL Campaign Standard]** 활동에는 다음 가드레일이 적용됩니다.

* Adobe Campaign 활동은 [대상자 읽기] 또는 [대상자 선별] 활동과 함께 사용할 수 없습니다.
* **[!UICONTROL Campaign Standard]** 활동은 다른 채널 활동(카드, 코드 기반 경험, 이메일, 푸시, SMS, 인앱 메시지, 웹)과 함께 사용할 수 없습니다.
* **[!UICONTROL Campaign v7/v8]** 활동은 기본 채널 활동과 동일한 여정에 함께 사용할 수 있습니다.

#### 반응 이벤트 {#reaction-events-g}

채널 작업 후 즉시 활동을 배치해야 하는 요구 사항과 다른 여정에서 보낸 메시지를 추적할 수 없는 사항 등 특정 보호 기능이 **[!UICONTROL 반응]** 이벤트에 적용됩니다. [이 페이지](../building-journeys/reaction-events.md#guardrails-limitations)에 나열되어 있습니다.

#### 인앱 활동 {#in-app-activity-limitations}

**[!UICONTROL 인앱 메시지]** 작업에 다음 가드레일이 적용됩니다. [이 페이지](../in-app/create-in-app.md)에서 인앱 메시지에 대해 자세히 알아보십시오.

* 현재 Healthcare 고객에게는 이 기능이 제공되지 않습니다.

* 개인화에는 프로필 속성만 포함할 수 있습니다.

* 인앱 활동은 **[!UICONTROL Campaign Standard]** 활동과 함께 사용할 수 없습니다.

* 인앱 표시는 여정 지속 시간에 연결되어 있습니다. 즉, 특정 프로필에 대한 여정이 종료되면 해당 여정 내의 모든 인앱 메시지는 해당 프로필에 표시되지 않습니다. 따라서 여정 활동에서 바로 인앱 메시지를 중지할 수는 없습니다. 인앱 메시지가 프로필에 표시되지 않도록 하려면 전체 여정을 종료해야 합니다.

* 테스트 모드에서 인앱 표시는 여정의 지속 시간에 따라 달라집니다. 테스트 중에 여정이 너무 일찍 종료되지 않도록 하려면 **[!UICONTROL 대기]** 활동의 **[!UICONTROL 대기 시간]** 값을 조정합니다.

* **[!UICONTROL 반응]** 활동은 인앱 열기 또는 클릭에 반응하는 데 사용할 수 없습니다.

* 사용자 프로필이 캔버스의 인앱 활동에 도달하는 순간과 해당 사용자에게 인앱 메시지가 표시되는 시간 사이에 활성화 지연이 발생할 수 있습니다.

* 인앱 메시지 콘텐츠 크기는 **2MB**(으)로 제한됩니다. 큰 이미지를 포함하면 게시 프로세스에 지장이 있을 수 있습니다.

#### 콘텐츠 결정 활동 {#content-decision-g}

업데이트된 동의 정책이 결정 정책에 적용되기 전 48시간 지연을 포함하여 **[!UICONTROL 콘텐츠 결정]** 활동에 특정 보호 기능이 적용됩니다. [이 페이지](../building-journeys/content-decision.md#guardrails)에 나열되어 있습니다.

#### 이동 활동 {#jump-g}

**[!UICONTROL 이동]** 활동에는 특정 가드레일이 적용됩니다. [이 페이지](../building-journeys/jump.md#jump-limitations)에 나열되어 있습니다.

#### 대상자 읽기 활동 {#read-segment-g}

[대상자 읽기](../building-journeys/read-audience.md) 여정 활동에 다음 가드레일이 적용됩니다.

| 가드레일 | 값 | 참고 |
|---|---|---|
| 동시 인스턴스(모든 샌드박스 + 여정) | **5** | 대상자 읽기가 동시에 시작되는 5개 이상의 여정을 예약하지 마십시오. 5~10분 간격으로 분산하십시오. |
| 샌드박스 처리량 | **20,000개 프로필/초**(공유) | 샌드박스의 모든 대상자 읽기 활동에서 공유됩니다. 제한에 도달하면 작업이 큐에 대기할 수 있습니다. |
| 활동당 구성 가능한 처리량 | **500-20,000개 프로필/초** | 샌드박스 공유 제한 내에서 활동당 을 구성합니다. |
| 작업 처리 시간 초과 | **12시간** | 12시간 이내에 처리할 수 없는 작업은 자동으로 정리되며 실행되지 않습니다. |
| 재시도 기간 | 최대 **1시간**(10분 간격) | 내보내기 작업을 검색하는 동안 다시 시도가 적용됩니다. 여정은 예약된 시간보다 최대 1시간 후에 실행할 수 있습니다. |
| 보조 ID 읽기 비율 | 여정 인스턴스당 **500개 프로필/초** | 보조 ID를 사용 중인 경우 적용됩니다. |
| 여정 당 대상 인스턴스 읽기 | **1** | 여정은 대상자 읽기 활동을 하나만 가질 수 있습니다. |
| 대상자 유형 | 스트리밍된 대상자는 항상 최신 상태입니다 | 배치 대상은 일일 배치 평가 시간에 하루에 한 번만 평가됩니다. |
| 프로필 속성 새로 고침 | **대기** 활동에서 새로 고침 | 여정 항목에서 프로필은 배치 스냅샷 값을 사용합니다. 프로필이 대기 활동에 도달하면 속성이 새로 고쳐집니다. |
| 여정 내 포지셔닝 | 첫 번째 활동 또는 비즈니스 이벤트 후 | 대상 읽기 활동은 여정의 첫 번째 활동으로 또는 비즈니스 이벤트 활동 후에만 사용할 수 있습니다. |
| Adobe Campaign에 사용 | 지원되지 않음 | 대상자 읽기 활동은 Adobe Campaign 활동과 함께 사용할 수 없습니다. |
| 여러 대상 | 직접 지원되지 않음 | 대상 읽기 활동은 한 여정 당 한 명의 대상자만 타깃팅할 수 있습니다. 여러 대상을 사용하려면 먼저 대상을 병합하십시오. [방법 알아보기](../audience/get-started-audience-orchestration.md) |

>[!TIP]
>
>**이를 통해 얻을 수 있는 이점:** 5개의 동시 인스턴스 제한은 전체 조직에 적용되는 엄격한 제한입니다. 여러 팀이 대상자 읽기 여정을 예약한 경우 시작 시간을 신중하게 조정합니다. 12시간 처리 기간이 누락된 작업은 자동으로 삭제됩니다. 즉, 항상 여정 로그에서 성공적인 실행을 확인합니다.

대상자 읽기 활동에 대한 [권장 사항 및 구성](../building-journeys/read-audience.md#must-read)도 참조하십시오.

#### 프로필 활동 업데이트 {#update-profile-g}

**[!UICONTROL 프로필 업데이트]** 활동에 특정 가드레일이 적용됩니다. [이 페이지](../building-journeys/update-profiles.md)에 나열되어 있습니다.

#### 여정 일시 중지 {#pause-g}

조직의 모든 일시 중지된 여정에 대해 최대 일시 중지 기간인 **14일**&#x200B;과(와) **1억 프로필 상한**&#x200B;을(를) 포함하여 **일시 중지 여정**&#x200B;에 특정 보호 기능이 적용됩니다. [이 페이지](../building-journeys/journey-pause.md#journey-pause-guardrails)에 나열되어 있습니다.

#### 여정 시험 실행 {#dry-run-g}

참여 가능한 프로필 및 실시간 여정 할당량에 대한 계산을 포함하여 **여정 시험 실행**&#x200B;에 특정 보호 기능이 적용됩니다. [이 페이지](../building-journeys/journey-dry-run.md#journey-dry-run-limitations)에 나열되어 있습니다.

#### 여정 조각 {#fragments-journey-g}

조각당 최대 **20개 노드** 및 샌드박스당 **200개 활성 조각**&#x200B;을 포함하여 **여정 조각**&#x200B;에 특정 보호 기능이 적용됩니다. [이 페이지](../building-journeys/journey-fragments.md#guardrails)에 나열되어 있습니다.

#### 예약된 일괄 처리를 사용하여 보내기 {#waves-g}

여정에서 **웨이브 보내기**&#x200B;에는 2~10개의 웨이브 범위와 웨이브 사이의 **30분 최소 간격**&#x200B;을 포함하여 특정 가드레일이 적용됩니다. [이 페이지](../building-journeys/send-using-waves.md#limitations-guardrails)에 나열되어 있습니다.

#### 여정 시뮬레이션 {#simulation-g}

**여정 시뮬레이션**&#x200B;에 특정 보호 기능이 적용됩니다. [이 페이지](../building-journeys/simulate-journey.md#limitations)에 나열되어 있습니다.

## 캠페인 오케스트레이션 {#campaign-orchestration}

### 캠페인 오케스트레이션 가드레일 {#orchestration-guardrails}

캠페인 오케스트레이션을 사용할 때 염두에 두어야 할 가드레일과 제한 사항은 [가드레일 및 제한 사항](../orchestrated/guardrails.md) 섹션에 자세히 설명되어 있습니다.
