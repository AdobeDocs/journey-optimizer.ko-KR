---
solution: Journey Optimizer
product: journey optimizer
title: 여정 테스트 또는 게시 전 오류 문제 해결
description: 여정을 테스트하거나 게시하기 전에 오류를 해결하는 방법 알아보기
feature: Journeys, Monitoring
topic: Content Management
role: User
level: Intermediate
keywords: 문제 해결, 문제 해결, 여정, 확인, 오류
exl-id: 03fbc4f4-b0a8-46d5-91f9-620685b11493
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/DorhpVm3trSxHG-l77-DpwbLTNQQxET1SIMYX-8ClQc
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 995
ht-degree: 18%

---

# 여정 테스트 전 오류 해결 {#troubleshooting}

>[!BEGINSHADEBOX]

**이 페이지에서:** 테스트하거나 게시하기 전에 여정을 문제 없이 실행할 수 있도록 활동 및 여정 구성 오류를 찾아 수정하는 방법에 대해 알아봅니다.

>[!ENDSHADEBOX]

이 섹션에서는 테스트 또는 게시 전에 여정 문제를 해결하는 방법에 대해 알아봅니다. 아래 나열된 모든 검사는 여정이 테스트 모드에 있거나 여정이 라이브 상태일 때 수행할 수 있습니다. 테스트 모드에서 아래의 모든 검사를 수행한 후에 게시를 진행하는 것이 좋습니다. [이 페이지](../building-journeys/testing-the-journey.md)의 테스트 모드에 대해 자세히 알아보세요.

여정 이벤트의 문제를 해결하는 방법, 프로필이 여정을 입력했는지 여부, 프로필을 통해 이동하는 방법, 메시지가 이 페이지에서 [전송되는지 여부](troubleshooting-execution.md)를 알아봅니다. 이벤트가 수집되고 있지만 이벤트 기반 여정에 프로필이 들어오지 않는 경우 [이벤트 조건 데이터 형식이 이벤트 스키마와 일치하는지 확인](troubleshooting-execution.md#verify-event-identity-and-rule-data-types)하십시오.

인바운드 액션을 사용 중인 경우 이 페이지에서 [문제를 해결하는 방법](troubleshooting-inbound.md)을 알아보세요.

## 활동 오류 {#activity-errors}

여정을 테스트하고 게시하기 전에 모든 활동이 올바르게 구성되었는지 확인하십시오. 시스템에서 오류가 계속 감지되면 테스트나 게시를 수행할 수 없습니다.

캔버스에서 활동 자체에 경고 기호가 표시되면서 오류가 나타납니다. 커서를 느낌표 위에 놓으면 오류 메시지가 표시됩니다. 활동을 선택하면 오류가 발생한 줄이 경고와 함께 표시됩니다. 예:

* 필수 필드가 비어 있으면 오류가 표시됩니다

  ![여정 유효성 검사 오류가 오류 표시기와 함께 캔버스에 표시됨](assets/journey63.png)

* 캔버스에서 두 활동의 연결이 끊기면 경고가 표시됩니다

  ![여정 캔버스에서 연결이 끊어진 활동을 표시하는 경고 아이콘](assets/canvas-disconnected.png)

## 여정 오류 {#canvas-errors}

캔버스 위의 **[!UICONTROL 경고]** 단추에서도 오류가 표시됩니다. 이 단추를 사용하면 시스템에서 감지된 오류와 테스트 모드 활성화 또는 여정 게시를 방지할 수 있습니다.

시스템에서 두 종류의 문제를 감지합니다. **오류** 및 **경고**. 오류는 게시 및 테스트 활성화를 차단합니다. 경고는 테스트 활성화 또는 게시를 차단하지 않는 잠재적인 문제를 나타냅니다. 문제에 대한 설명 그리고 ERR_XXX_XXX 유형의 문제 로그 ID가 표시됩니다. 이렇게 하면 문제를 식별하는 데 도움이 될 수 있습니다.

![설명 도구 설명이 있는 여정의 오류 및 경고 표시기](assets/journey-error-and-warning.png)

<!--Most of the time, errors detected by the system are linked to errors visible on the activities but they can also relate to other issues. In all cases, check alerts and resolve the issue using to the error description. If you cannot identify the issue, use the **[!UICONTROL Copy details]** button to store the alerts, and send them to your administrator.-->

여정에서 전체적으로 발생하는 오류와 경고가 목록에 먼저 나타납니다. 특정 활동과 관련된 오류와 경고는 그 뒤에 활동 순서별로 또는 여정 내 등장 순서별로 왼쪽에서 오른쪽으로 나열됩니다. 경고 목록의 맨 아래에 있는 **[!UICONTROL 세부 정보 복사]** 단추를 사용하여 문제를 해결하는 데 유용한 여정에 대한 기술 정보를 복사할 수 있습니다. 복사된 필드 목록(일시 중지 및 다시 시작 정보 포함)은 여정 속성에서 [기술 세부 정보 복사](journey-properties.md#access-properties)를 참조하십시오.

## 대체 경로 추가 {#canvas-add-path}

다음 여정 활동에 대해 오류가 발생하는 경우 대체 동작을 정의할 수 있습니다. **[!UICONTROL 최적화]** 및 **[!UICONTROL 동작]**.

작업 또는 조건에 오류가 발생하면 개별 여정이 중지됩니다. 이를 지속할 수 있는 유일한 방법은 문제를 해결하는 것이다. 여정이 중단되지 않도록 하기 위해 **[!UICONTROL 활동 속성에서 시간 초과 또는 오류 발생 시 대체 경로를 추가]** 옵션을 선택할 수도 있습니다. [이 섹션](../building-journeys/using-the-journey-designer.md#paths)에서 자세히 알아보십시오.

+++ AI 기술 자료 참조

이 단원에는 이 주제와 관련된 해석, 검색 및 질문 답변을 지원하기 위한 구조화된 지식이 포함되어 있습니다.

이해를 돕기 위해 이 정보를 이 페이지의 설명서와 통합해야 합니다. 두 소스 모두 독립적으로 사용하기 위한 것은 아닙니다. 이 페이지에서는 기능에 대해 설명하지만, 용어, 의도, 적용 가능성 및 제약 조건을 명확히 하는 데 도움이 되는 추가 컨텍스트를 제공합니다.

* **TL;DR:** 이 페이지에서는 테스트 모드에 들어가거나 게시하기 전에 여정에서 구성 오류 및 경고를 식별하고 해결하는 방법에 대해 설명합니다.

**의도:**

* 여정을 테스트하거나 게시하기 전에 활동 수준 구성 오류 식별
* 경고 패널에서 차단 오류와 비차단 경고를 구분합니다
* 오류 로그 ID(ERR_XXX_XXX 형식)를 사용하여 여정 문제를 진단합니다.
* 문제 해결을 위해 관리자와 공유할 기술 여정 세부 정보 복사
* 오류 또는 시간 초과 시 개별 여정이 중지되지 않도록 하는 대체 경로 추가

**용어집:**

* **경고 단추**: 게시 또는 테스트 활성화를 차단하는 모든 시스템 감지 오류 및 경고를 표시하는 캔버스 컨트롤 *(제품별)*
* **ERR_XXX_XXX**: 감지된 각 문제에 할당된 문제 로그 ID 형식이며, 오류를 식별하고 전달하는 데 사용됩니다. *(제품별)*
* **대체 경로**: 오류나 시간 제한이 발생할 때 여정을 계속하는 동작 또는 조건 활동에 대체 분기가 추가되었습니다. *(제품별)*

**보호 기능:**

* 차단 오류가 해결되지 않은 상태로 남아 있으면 테스트 모드를 활성화하거나 여정을 게시할 수 없습니다.
* 경고는 게시나 테스트 활성화를 차단하지 않지만 잠재적인 문제를 나타냅니다.
* 대체 경로는 최적화 및 작업 활동에만 사용할 수 있습니다.

**용어:**

* 정식 이름: 경고 — 약어: 없음 — 변형: 경고 패널, 경고 버튼
* 동의어: &quot;errors&quot; = &quot;차단 문제&quot;; &quot;warnings&quot; = &quot;비차단 문제&quot;
* 혼동하지 마십시오. &quot;오류&quot;(게시 차단) ≠ &quot;경고&quot;(게시 차단 안 함)

**FAQ:**

* **Q: Journey Optimizer에서 오류와 경고의 차이점은 무엇입니까?** — 오류는 테스트 모드 활성화와 여정 게시를 모두 차단합니다. 경고는 잠재적인 문제를 나타내지만 테스트나 게시를 금지하지 않습니다.
* **Q: 내 여정에 영향을 주는 모든 오류는 어디에서 볼 수 있습니까?** — 시스템에서 감지된 모든 오류 및 경고에 대한 통합 목록을 보려면 캔버스 위의 경고 버튼을 클릭합니다.
* **Q: 오류 설명에서 문제를 식별할 수 없으면 어떻게 해야 합니까?** — 경고 목록 하단의 세부 정보 복사 버튼을 사용하여 기술 정보를 캡처하여 관리자에게 보냅니다.
* **Q: 작업에 오류가 있어도 개인 사용자에 대해 여정을 계속 실행할 수 있습니까?** — 예, 활동 속성에서 &quot;시간 초과 또는 오류 발생 시 대체 경로 추가&quot; 옵션을 활성화하여 대체 경로를 정의합니다.
* **Q: 언제 이러한 문제 해결 검사를 수행해야 합니까?** — 모든 검사는 테스트 모드에서 또는 여정이 라이브 상태일 때 수행할 수 있습니다. 게시하기 전에 테스트 모드에서 모든 문제를 해결하는 것이 좋습니다.

+++
