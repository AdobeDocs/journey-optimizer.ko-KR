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
subfeature_v2: []
feature_v2:
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
source-git-commit: 7ced44f92f816d83d9a9ad667b4322dcb5930741
workflow-type: tm+mt
source-wordcount: 1369
ht-degree: 1%

---

# MCP 클라이언트 작업 {#ajo-mcp}

>[!BEGINSHADEBOX]

**이 페이지에서:** Model Context Protocol 기본 사항 및 지원되는 클라이언트에서 사용 가능한 도구, 샘플 프롬프트, 설치 사전 요구 사항, 연결 단계 및 일반적인 질문에 대한 답변에 이르기까지 [!DNL Adobe Journey Optimizer] MCP 서버에 대한 단계별 개요를 살펴보십시오.

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer] MCP 통합을 사용하면 API 호출을 작성하거나 제품 화면을 탐색하지 않고도 일반 언어 프롬프트를 사용하여 캠페인, 여정 및 오퍼를 쿼리할 수 있습니다. 이 페이지에서는 통합 작동 방식, 통합 기능으로 수행할 수 있는 작업 및 시작 방법을 설명합니다.

>[!AVAILABILITY]
>
>[!DNL Adobe Journey Optimizer] MCP 서버는 현재 **클라우드 웹**, **클라우드 데스크톱** 및 **커서**&#x200B;에서 사용할 수 있습니다. 추가 MCP 호환 애플리케이션에 대한 지원은 향후 릴리스에 추가될 예정입니다.

## Beta, 보안 및 법적 고지 사항 {#mcp-notices}

**Beta 설명서 알림:** 이 설명서는 Beta 기능을 다루고 있으며 최종 설명서를 구성하지 않습니다. 여기에 설명된 콘텐츠는 Beta 릴리스와 관련되며, 일반 공급 이전에 변경될 수 있습니다. Adobe은 이 설명서의 완벽성이나 정확성에 대해 어떠한 표현도 하지 않습니다.

Adobe Journey Optimizer MCP 서버(Beta)(&quot;Beta&quot;)를 사용하면 Beta이 어떠한 종류의 보증도 없이 **&quot;있는 그대로&quot; 제공된다는 것을 인정합니다**. Adobe은 Beta을 유지, 수정, 업데이트, 변경, 수정 또는 지원할 의무가 없습니다. 이러한 Beta 및/또는 동봉된 자료의 올바른 기능이나 성능에 어떤 식으로든 의존하지 말고 주의하는 것이 좋습니다. Beta은 Adobe의 기밀 정보로 간주됩니다. 귀하가 Adobe에 제공한 &quot;피드백&quot;(Beta 사용 중 발생하는 문제 또는 결함, 제안, 개선 사항 및 권장 사항을 포함하되 이에 제한되지 않는 Beta 관련 정보)은 해당 피드백에 대한 모든 권한, 제목 및 관심을 포함하여 Adobe에 할당됩니다.

>[!WARNING]
>
>MCP(Model Context Protocol)는 새로운 오픈 소스 표준이며 보안 또는 신뢰성 위험을 제시할 수 있습니다. Adobe MCP 서버 통합 및 관련 설명서는 어떠한 종류의 보증도 없이 &quot;있는 그대로&quot; 제공됩니다.
>
>MCP 클라이언트 또는 서버를 Adobe 제품에 연결하는 것은 고객이 선택한 구성입니다. 고객은 MCP 통합의 보안 및 적합성을 평가할 책임이 있습니다. Adobe은 잘못된 구성, MCP 오용, 서드파티 구현의 취약점 또는 MCP 지원 워크플로우를 통해 수행된 의도하지 않은 작업으로 인해 발생하는 문제에 대해 책임을 지지 않습니다.
>
>위험을 줄이기 위해 Adobe에서는 생산적 사용을 시작하기 전에 샌드박스 환경에서 통합을 테스트하고, 이를 확인하거나 의존하기 전에 모든 MCP에서 시작한 작업과 응답을 주의 깊게 검토하고 유효성을 검사하는 것을 권장합니다.

## 모델 컨텍스트 프로토콜이란 무엇입니까? {#mcp-overview}

마케팅 및 고객 경험 팀은 일상적인 업무를 간소화하기 위해 Anthropic Claude, OpenAI ChatGPT, Cursor, Microsoft Copilot Studio와 같은 채팅 기반 애플리케이션과 개발자 도구에 점점 더 의존하고 있습니다. 이러한 응용 프로그램은 응용 프로그램이 백엔드 도구를 대형 언어 모델(LLM)에 균일한 방식으로 노출할 수 있도록 해주는 개방형 표준인 **MCP(Model Context Protocol)**&#x200B;을 지원합니다.

[!DNL Adobe Journey Optimizer]은(는) 이제 MCP 호환 응용 프로그램 내에서 직접 캠페인 및 샌드박스 작업을 표시하는 MCP 서버를 제공합니다. [!DNL Adobe Journey Optimizer] MCP 통합을 통해 서로 다른 가상 사용자가 [!DNL Adobe Journey Optimizer] REST API에 대한 쿼리를 작성하거나 여러 UI 화면을 탐색하지 않고도 동일한 오케스트레이션 데이터를 공동 작업할 수 있습니다. 고객은 대화식으로 자신의 의도를 설명하고 LLM이 적절한 MCP 도구를 호출하도록 할 수 있다.

## 주요 기능 {#mcp-capabilities}

[!DNL Adobe Journey Optimizer] MCP 서버를 사용하면 AI 도우미에서 직접 캠페인, 여정 및 오퍼를 검사, 요약 및 해결할 수 있습니다. 모든 작업은 **읽기 전용**&#x200B;입니다. MCP 서버 표면이 API를 일반 언어 답변으로 검색하므로 다음을 수행할 수 있습니다.

* **여정 논리 이해** - 사람이 인식할 수 있는 여정 분기, 조건 및 작업에 대한 요약을 가져옵니다.
* **즉각적인 캠페인 가시성 확보** - 메뉴를 탐색하거나 보고서를 수동으로 가져오지 않고 일반 언어로 캠페인 상태 및 채널 구성에 대해 질문하고 즉시 답변을 얻을 수 있습니다.
* **문제를 조기에 발견** — 요청 시 표면 중단 캠페인, 분리된 초안 및 채널 구성 문제가 발생하여 팀이 신속하게 조치를 취할 수 있습니다.
* **라이브 데이터를 중심으로 공동 작업** - 마케터, 캠페인 관리자 및 관련자는 모두 AI 도우미를 통해 동일한 라이브 [!DNL Adobe Journey Optimizer] 데이터를 쿼리할 수 있으므로 더 쉽게 정렬, 결정 및 이동할 수 있습니다.
* **오케스트레이션 포트폴리오 감사** - JSON을 구문 분석하거나 제품 화면 간에 이동하지 않고 캠페인의 전체 상태를 검토합니다.

## 사용 가능한 도구 {#mcp-tools}

[!DNL Adobe Journey Optimizer] MCP 서버에서 다음 도구를 노출합니다.

**캠페인 도구**

| 도구 | 설명 |
|---|---|
| **캠페인 나열** | [!DNL Adobe Journey Optimizer] 마케팅 캠페인을 찾아봅니다. 상태(초안, 라이브, 중단됨, 완료됨)별로 필터링을 지원합니다. |
| **캠페인 가져오기** | 대상 타기팅, 일정, 채널 및 콘텐츠 설정을 포함하여 ID별로 특정 캠페인에 대한 전체 세부 정보 및 구성을 가져옵니다. |
| **채널 구성 나열** | 이메일, SMS, 푸시 또는 WhatsApp 채널에 대한 표면 사전 설정 및 브랜딩 설정을 봅니다. |

**여정 도구**

| 도구 | 설명 |
|---|---|
| **모든 여정 가져오기** | [!DNL Adobe Journey Optimizer] 샌드박스의 모든 여정을 찾아봅니다. |
| **여정 가져오기** | 분기, 조건 및 작업을 포함하여 ID별로 특정 여정에 대한 전체 세부 정보를 가져옵니다. |
| **여정 시각화** | 대화형 도구로 여정을 렌더링하여 구조를 시각적으로 탐색할 수 있습니다. |

>[!NOTE]
>
>모든 도구는 읽기 전용입니다. 현재 Beta 릴리스에서는 쓰기 작업(개체 만들기, 업데이트 또는 삭제)이 지원되지 않습니다.

## 사용 사례 {#mcp-use-cases}

다음 예제는 자연어를 사용하여 [!DNL Adobe Journey Optimizer] MCP 서버와 상호 작용하는 방법을 보여 줍니다.

| 목표 | 예제 프롬프트 |
|---|---|
| **캠페인 및 여정 개요** | 모든 Journey Optimizer 캠페인/여정 보기 / Journey Optimizer에 설정된 캠페인/여정 수는 얼마입니까? |
| **상태 감사** | 현재 어떤 캠페인/여정이 라이브됩니까? / 일시 중지되거나 중지된 캠페인/여정을 나열합니다. |
| **캠페인 및 여정 세부 정보** | [ID] 캠페인에 대한 전체 세부 정보를 확인하고 [ID] 캠페인에 설정된 모든 내용을 소개합니다. / [ID] 여정에 대한 전체 세부 정보를 확인하고 [ID] 여정에 설정된 모든 내용을 소개합니다. |
| **대상 및 타깃팅** | 캠페인/여정 [ID]에서 타깃팅된 대상은 무엇입니까? / 캠페인/여정 [ID]에 설정된 자격 규칙은 무엇입니까? |
| **일정 및 시간** | 캠페인 [ID]이(가) 언제 실행되도록 예약됩니까? / 캠페인 [ID]이(가) 일회성 전송입니까? 아니면 반복입니까? |
| **문제 해결** | 캠페인 [ID]을(를) 보내지 않는 이유는 무엇입니까? / 문제에 대한 [ID] 캠페인 설정을 검토하십시오. |
| **채널 구성** | 내 샌드박스에서 사용할 수 있는 채널 사전 설정은 무엇입니까? / 내 이메일 채널 구성을 모두 표시합니다. |
| **채널 감사** | 누락되거나 불완전한 채널 구성은 무엇입니까? / 모든 채널에서 몇 개의 채널 구성을 사용할 수 있습니까? |

## 사전 요구 사항 {#mcp-prerequisites}

[!DNL Adobe Journey Optimizer] MCP 서버를 MCP 클라이언트에 연결하기 전에 다음 사항을 확인하십시오.

* 활성 [!DNL Adobe Journey Optimizer] 라이선스가 있습니다.
* 지원되는 MCP 호환 애플리케이션(현재 Cloud Web, Cloud Desktop 또는 Cursor)에 액세스할 수 있습니다.
* [!DNL Adobe Journey Optimizer]에서 캠페인, 여정 및 오퍼를 볼 수 있는 권한이 있습니다.

## [!DNL Adobe Journey Optimizer] MCP 서버 연결 {#mcp-connect}

>[!NOTE]
>
>이 통합은 Beta에 있습니다.

**클라우드 웹**, **클라우드 데스크톱**, **커서**&#x200B;를 포함하여 선호하는 MCP 클라이언트를 통해 [!DNL Adobe Journey Optimizer] MCP 서버를 연결할 수 있습니다.

**MCP 클라이언트를 통해 연결**

MCP 클라이언트에서 MCP 서버를 설정할 때 다음 서버 끝점 URL을 사용합니다.

`https://ajo-mcp.adobe.io/mcp`

**클라우드 웹 또는 클라우드 데스크톱을 통해 연결**

클라우드 웹 또는 클라우드 데스크톱에서 MCP 서버를 설정하려면 **커넥터**(으)로 이동하여 **Adobe Journey Optimizer**&#x200B;을(를) 선택하십시오.

## 자주 묻는 질문 {#mcp-faq}

+++지원되는 MCP 클라이언트는 무엇입니까?

[!DNL Adobe Journey Optimizer] MCP 서버는 현재 **클라우드 웹**, **클라우드 데스크톱** 및 **커서**&#x200B;에서 사용할 수 있습니다. 추가 MCP 호환 애플리케이션에 대한 지원은 향후 릴리스에 추가될 수 있습니다.
+++

+++MCP를 통해 액세스할 수 있는 [!DNL Adobe Journey Optimizer] 개체는 무엇입니까?

캠페인, 여정, 오퍼 및 샌드박스 정보에 액세스할 수 있습니다. 작업은 읽기 전용(API 검색)이며 쓰기 작업은 현재 릴리스에서 지원되지 않습니다.
+++

+++[!DNL Adobe Journey Optimizer] MCP 서버를 사용하려면 개발자 액세스 권한이 필요합니까?

아니요. MCP 서버는 마케팅 및 기술 담당자 모두를 위해 설계되었습니다. 마케터는 지원되는 모든 MCP 클라이언트에서 자연어 프롬프트를 사용하여 상호 작용할 수 있으며, 개발자는 MCP를 지원하는 개발자 도구에서 사용할 수도 있습니다.
+++

+++내 데이터가 MCP 클라이언트 공급자에게 전송됩니까?

프롬프트를 제출하면 MCP 클라이언트는 관련 컨텍스트(MCP 서버에서 반환된 [!DNL Adobe Journey Optimizer] 데이터 포함)를 처리를 위해 해당 모델로 보낼 수 있습니다. 프로덕션 데이터에 연결하기 전에 MCP 클라이언트 공급자의 개인정보 보호 및 데이터 처리 정책을 검토하십시오.
+++

+++[!DNL Adobe Journey Optimizer]에서 어떤 권한이 필요합니까?

쿼리할 개체(캠페인, 여정 또는 오퍼)에 대해 최소 **보기** 권한이 필요합니다. MCP 서버는 읽기 작업만 수행하므로 쓰기 권한이 필요하지 않습니다. 현재 액세스 수준을 잘 모를 경우 [!DNL Adobe Journey Optimizer] 관리자에게 문의하십시오.
+++

+++샌드박스 환경에서 MCP 서버를 사용할 수 있습니까?

예. MCP 서버는 [!DNL Adobe Journey Optimizer] 샌드박스 구성을 준수합니다. 프롬프트에서 샌드박스를 지정하거나 특정 샌드박스에 지정된 자격 증명으로 연결하여 샌드박스 특정 데이터를 쿼리할 수 있습니다.
+++

