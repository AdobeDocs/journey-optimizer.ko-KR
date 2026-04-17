---
solution: Journey Optimizer
product: journey optimizer
title: MCP 클라이언트(Beta) 작업
description: MCP 서버를 사용하여 Adobe Journey Optimizer을 MCP 클라이언트에 연결하는 방법에 대해 알아봅니다
feature: Integrations
topic: Content Management, Artificial Intelligence
badge: label="Beta" type="Informative"
role: User, Developer
level: Beginner, Intermediate
hide: true
source-git-commit: aebdc15b5ca46a2aa623c8c245f00c74a43c9bb2
workflow-type: tm+mt
source-wordcount: '1300'
ht-degree: 1%

---

# MCP 클라이언트(Beta) 작업 {#ajo-mcp}

>[!CAUTION]
>
>**Beta 설명서 알림:** 이 설명서는 Beta 기능을 다루고 있으며 최종 설명서를 구성하지 않습니다. 여기에 설명된 콘텐츠는 Beta 릴리스와 관련되며, 일반 공급 이전에 변경될 수 있습니다. Adobe은 이 설명서의 완벽성이나 정확성에 대해 어떠한 표현도 하지 않습니다.
>
>Adobe Journey Optimizer MCP 서버(Beta)(&quot;Beta&quot;)를 사용하면 Beta이 어떠한 종류의 보증도 없이 **&quot;있는 그대로&quot; 제공된다는 것을 인정합니다**. Adobe은 Beta을 유지, 수정, 업데이트, 변경, 수정 또는 지원할 의무가 없습니다. 이러한 Beta 및/또는 동봉된 자료의 올바른 기능이나 성능에 어떤 식으로든 의존하지 말고 주의하는 것이 좋습니다. Beta은 Adobe의 기밀 정보로 간주됩니다. 귀하가 Adobe에 제공한 &quot;피드백&quot;(Beta 사용 중 발생하는 문제 또는 결함, 제안, 개선 사항 및 권장 사항을 포함하되 이에 제한되지 않는 Beta 관련 정보)은 해당 피드백에 대한 모든 권한, 제목 및 관심을 포함하여 Adobe에 할당됩니다.

[!DNL Adobe Journey Optimizer] MCP 통합을 사용하면 API 호출을 작성하거나 제품 화면을 탐색하지 않고도 일반 언어 프롬프트를 사용하여 캠페인 및 오퍼를 쿼리할 수 있습니다. 이 페이지에서는 통합 작동 방식, 통합 기능으로 수행할 수 있는 작업 및 시작 방법을 설명합니다.

>[!AVAILABILITY]
>
>[!DNL Adobe Journey Optimizer] MCP 서버는 현재 **클라우드 웹** 및 **클라우드 데스크톱**&#x200B;에서만 사용할 수 있습니다. 추가 MCP 호환 애플리케이션에 대한 지원은 향후 릴리스에 추가될 예정입니다.

## 모델 컨텍스트 프로토콜이란 무엇입니까? {#mcp-overview}

마케팅 및 고객 경험 팀은 일상적인 업무를 간소화하기 위해 Anthropic Claude, OpenAI ChatGPT, Cursor, Microsoft Copilot Studio와 같은 채팅 기반 애플리케이션과 개발자 도구에 점점 더 의존하고 있습니다. 이러한 응용 프로그램은 응용 프로그램이 백엔드 도구를 대형 언어 모델(LLM)에 균일한 방식으로 노출할 수 있도록 해주는 개방형 표준인 **MCP(Model Context Protocol)**&#x200B;을 지원합니다.

[!DNL Adobe Journey Optimizer]은(는) 이제 MCP 호환 응용 프로그램 내에서 직접 캠페인, 충성도 및 샌드박스 작업을 나타내는 MCP 서버를 제공합니다. [!DNL Adobe Journey Optimizer] MCP 통합을 통해 서로 다른 가상 사용자가 [!DNL Adobe Journey Optimizer] REST API에 대한 쿼리를 작성하거나 여러 UI 화면을 탐색하지 않고도 동일한 오케스트레이션 데이터를 공동 작업할 수 있습니다. 고객은 대화식으로 자신의 의도를 설명하고 LLM이 적절한 MCP 도구를 호출하도록 할 수 있다.

## 주요 기능 {#mcp-capabilities}

[!DNL Adobe Journey Optimizer] MCP 서버를 사용하면 AI 도우미에서 직접 캠페인 및 오퍼를 검사, 요약 및 해결할 수 있습니다. 모든 작업은 **읽기 전용**&#x200B;입니다. MCP 서버 표면이 API를 일반 언어 답변으로 검색하므로 다음을 수행할 수 있습니다.

<!--* **Understand journey logic** — Get a human-readable summary of any journey's branching, conditions, and actions.-->
* **즉각적인 캠페인 가시성 확보** - 메뉴를 탐색하거나 보고서를 수동으로 가져오지 않고 일반 언어로 캠페인 상태 및 채널 구성에 대해 질문하고 즉시 답변을 얻을 수 있습니다.
* **문제를 조기에 발견** — 요청 시 표면 중단 캠페인, 분리된 초안 및 채널 구성 문제가 발생하여 팀이 신속하게 조치를 취할 수 있습니다.
* **라이브 데이터를 중심으로 공동 작업** - 마케터, 캠페인 관리자 및 관련자는 모두 AI 도우미를 통해 동일한 라이브 [!DNL Adobe Journey Optimizer] 데이터를 쿼리할 수 있으므로 더 쉽게 정렬, 결정 및 이동할 수 있습니다.
* **오케스트레이션 포트폴리오 감사** - JSON을 구문 분석하거나 제품 화면 간에 이동하지 않고 캠페인의 전체 상태를 검토합니다.

## 사용 가능한 도구 {#mcp-tools}

[!DNL Adobe Journey Optimizer] MCP 서버에서 다음 도구를 노출합니다.

| 도구 | 설명 |
|---|---|
| **캠페인 나열** | [!DNL Adobe Journey Optimizer] 마케팅 캠페인을 찾아봅니다. 상태(초안, 라이브, 중단됨, 완료됨)별로 필터링을 지원합니다. |
| **캠페인 가져오기** | 대상 타기팅, 일정, 채널 및 콘텐츠 설정을 포함하여 ID별로 특정 캠페인에 대한 전체 세부 정보 및 구성을 가져옵니다. |
| **채널 구성 나열** | 이메일, SMS, 푸시 또는 WhatsApp 채널에 대한 표면 사전 설정 및 브랜딩 설정을 봅니다. |

>[!NOTE]
>
>모든 도구는 읽기 전용입니다. 현재 Beta 릴리스에서는 쓰기 작업(개체 만들기, 업데이트 또는 삭제)이 지원되지 않습니다.

## 사용 사례 {#mcp-use-cases}

다음 예제는 자연어를 사용하여 [!DNL Adobe Journey Optimizer] MCP 서버와 상호 작용하는 방법을 보여 줍니다.

| 목표 | 예제 프롬프트 |
|---|---|
| **캠페인 개요** | &quot;모든 AJO 캠페인 표시&quot; / &quot;AJO에 설정된 캠페인은 몇 개입니까?&quot; |
| **상태 감사** | &quot;현재 어떤 캠페인이 라이브됩니까?&quot; / &quot;일시 중지되거나 중지된 캠페인을 나열합니다.&quot; |
| **캠페인 세부 정보** | &quot;캠페인 [ID]&quot;에 대한 전체 세부 정보 가져오기 / &quot;캠페인 [ID]에 설정된 모든 항목을 소개합니다.&quot; |
| **대상 및 타깃팅** | &quot;캠페인 [ID]에서 타깃팅된 대상은 무엇입니까?&quot; / &quot;캠페인 [ID]에 설정된 자격 규칙은 무엇입니까?&quot; |
| **일정 및 시간** | &quot;[ID] 캠페인은 언제 실행되도록 예약됩니까?&quot; / &quot;[ID] 캠페인이 일회성 전송입니까, 반복 전송입니까?&quot; |
| **문제 해결** | &quot;캠페인 [ID]을(를) 보내지 않는 이유는 무엇입니까?&quot; / &quot;문제에 대한 [ID] 캠페인 설정을 검토하십시오.&quot; |
| **채널 구성** | &quot;내 샌드박스에서 사용할 수 있는 채널 사전 설정은 무엇입니까?&quot; / &quot;내 이메일 채널 구성을 모두 표시합니다.&quot; |
| **채널 감사** | &quot;누락되었거나 불완전한 채널 구성은 무엇입니까?&quot; / &quot;모든 채널에서 몇 개의 채널 구성을 사용할 수 있습니까?&quot; |

## 전제 조건 {#mcp-prerequisites}

[!DNL Adobe Journey Optimizer] MCP 서버를 MCP 클라이언트에 연결하기 전에 다음 사항을 확인하십시오.

* 활성 [!DNL Adobe Journey Optimizer] 라이선스가 있습니다.
* 지원되는 MCP 호환 애플리케이션(현재 클라우드 웹 또는 클라우드 데스크탑)에 액세스할 수 있습니다.
* [!DNL Adobe Journey Optimizer]에서 캠페인과 오퍼를 볼 수 있는 권한이 있습니다.

## [!DNL Adobe Journey Optimizer] MCP 서버 연결 {#mcp-connect}

>[!NOTE]
>
>이 통합은 Beta에 있습니다. 자세한 설정 단계는 일반 가용성에 도달하면 게시됩니다. 조기 액세스를 요청하고 구성 지침을 받으려면 Adobe 담당자에게 문의하십시오.

Beta 단계에서 Adobe 담당자는 다음을 제공합니다.

* 조직에 관련된 MCP 서버 엔드포인트 URL.
* AI 도우미를 [!DNL Adobe Journey Optimizer]에 연결하기 위한 인증 자격 증명입니다.
* Cloud Desktop 또는 Cloud Web에서 MCP 서버 구성에 대한 지침

<!--
Step-by-step connection instructions to be added here, including:
- How to obtain MCP server credentials from [!DNL Adobe Journey Optimizer]
- How to configure the MCP server in Claude Desktop / Claude Web
- How to authenticate
-->

## 알려진 제한 사항(Beta) {#mcp-limitations}

다음 제한 사항은 [!DNL Adobe Journey Optimizer] MCP 서버의 현재 Beta 릴리스에 적용됩니다.

| 제한 사항 | 설명 | 해결 방법 |
|---|---|---|
| **참여 또는 성능 지표 없음** | MCP 서버는 보고 데이터를 노출하지 않습니다. 도구는 노출 횟수, 클릭스루 비율, 전환 또는 게재 통계를 반환하지 않습니다. | 지표에 AJO Reporting UI, CJA MCP 또는 Adobe Analytics MCP를 사용합니다. AEP 쿼리 서비스는 캠페인 실행 ID를 사용하여 원시 이벤트 데이터를 쿼리할 수 있습니다. |
| **캠페인 목록 페이지 매김이 제한됨** | `List Campaigns`은(는) 항상 결과의 첫 페이지를 반환합니다(최대 50개의 캠페인을 사전순으로 정렬). 오프셋 및 제한 값이 적용되지 않으므로 대형 샌드박스에서 전체 열거를 사용할 수 없습니다. | 캠페인 ID 또는 이름이 알려진 경우 `Get Campaign`을(를) 직접 사용하십시오. 전체 목록을 탐색 및 필터링하려면 AJO UI를 사용하십시오. |
| **날짜, 채널 또는 일정별 서버측 필터링 없음** | `List Campaigns`은(는) 상태별 필터링만 지원합니다. 게시 날짜, 예약 날짜, 채널 또는 캠페인 유형별 필터링은 서버측에서 사용할 수 없습니다. | 기본 날짜 및 채널 필터링을 지원하는 AJO UI 캠페인 목록을 사용합니다. |
| **메시지 콘텐츠 검색을 사용할 수 없음** | 메시지 콘텐츠 도구는 모든 채널 유형(이메일, 코드 기반 등)에 대해 HTTP 502를 반환합니다. 메시지 HTML, 제목 줄, 개인화 토큰 및 오퍼 콘텐츠는 MCP를 통해 검색할 수 없습니다. | **캠페인 > [캠페인] > 컨텐츠** 아래의 AJO UI에서 직접 메시지 컨텐츠 및 개인화 토큰을 봅니다. |

## 자주 묻는 질문 {#mcp-faq}

+++지원되는 MCP 클라이언트는 무엇입니까?

[!DNL Adobe Journey Optimizer] MCP 서버는 현재 **클라우드 웹** 및 **클라우드 데스크톱**&#x200B;에서 사용할 수 있습니다. 추가 MCP 호환 애플리케이션에 대한 지원은 향후 릴리스에 추가될 수 있습니다.
+++

+++MCP를 통해 액세스할 수 있는 [!DNL Adobe Journey Optimizer] 개체는 무엇입니까?

캠페인, 오퍼, 충성도 데이터 및 샌드박스 정보에 액세스할 수 있습니다. 작업은 읽기 전용(API 검색)이며 쓰기 작업은 현재 릴리스에서 지원되지 않습니다.
+++

+++[!DNL Adobe Journey Optimizer] MCP 서버를 사용하려면 개발자 액세스 권한이 필요합니까?

아니요. MCP 서버는 마케팅 및 기술 담당자 모두를 위해 설계되었습니다. 마케터는 지원되는 모든 MCP 클라이언트에서 자연어 프롬프트를 사용하여 상호 작용할 수 있으며, 개발자는 MCP를 지원하는 개발자 도구에서 사용할 수도 있습니다.
+++

+++내 데이터가 MCP 클라이언트 공급자에게 전송됩니까?

프롬프트를 제출하면 MCP 클라이언트는 관련 컨텍스트(MCP 서버에서 반환된 [!DNL Adobe Journey Optimizer] 데이터 포함)를 처리를 위해 해당 모델로 보낼 수 있습니다. 프로덕션 데이터에 연결하기 전에 MCP 클라이언트 공급자의 개인정보 보호 및 데이터 처리 정책을 검토하십시오.
+++

+++[!DNL Adobe Journey Optimizer]에서 어떤 권한이 필요합니까?

쿼리할 개체(캠페인 또는 오퍼)에 대해 최소 **보기** 권한이 필요합니다. MCP 서버는 읽기 작업만 수행하므로 쓰기 권한이 필요하지 않습니다. 현재 액세스 수준을 잘 모를 경우 [!DNL Adobe Journey Optimizer] 관리자에게 문의하십시오.
+++

+++샌드박스 환경에서 MCP 서버를 사용할 수 있습니까?

예. MCP 서버는 [!DNL Adobe Journey Optimizer] 샌드박스 구성을 준수합니다. 프롬프트에서 샌드박스를 지정하거나 특정 샌드박스에 지정된 자격 증명으로 연결하여 샌드박스 특정 데이터를 쿼리할 수 있습니다.
+++

