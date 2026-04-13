---
solution: Journey Optimizer
product: journey optimizer
title: MCP를 통해 AI 지원 팀과 작업
description: MCP(Model Context Protocol) 서버를 사용하여 Adobe Journey Optimizer을 AI 지원에 연결하는 방법에 대해 알아봅니다
feature: Integrations
topic: Content Management, Artificial Intelligence
badge: label="제한된 가용성" type="Informative"
role: User, Developer
level: Beginner, Intermediate
source-git-commit: b92ef33b03e0bdcd6e615846cd7654aaab1b4a1a
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 1%

---

# MCP를 통해 AI 지원 팀과 작업 {#ajo-mcp}

>[!AVAILABILITY]
>
>[!DNL Adobe Journey Optimizer] MCP 서버는 현재 **클라우드 웹** 및 **클라우드 데스크톱**&#x200B;에서만 사용할 수 있습니다.

## 모델 컨텍스트 프로토콜이란 무엇입니까? {#mcp-overview}

마케팅 및 고객 경험 팀은 일상적인 업무를 간소화하기 위해 Anthropic Claude, OpenAI ChatGPT, Cursor, Microsoft Copilot Studio와 같은 채팅 기반 애플리케이션과 개발자 도구에 점점 더 의존하고 있습니다. 이러한 응용 프로그램은 응용 프로그램이 백엔드 도구를 대형 언어 모델(LLM)에 균일한 방식으로 노출할 수 있도록 해주는 개방형 표준인 **MCP(Model Context Protocol)**&#x200B;을 지원합니다.

[!DNL Adobe Journey Optimizer]은(는) 이제 MCP 호환 응용 프로그램 내에서 직접 캠페인, 여정, 충성도 및 샌드박스 작업을 나타내는 MCP 서버를 제공합니다. [!DNL Adobe Journey Optimizer] MCP 통합을 통해 서로 다른 가상 사용자가 [!DNL Adobe Journey Optimizer] REST API에 대한 쿼리를 작성하거나 여러 UI 화면을 탐색하지 않고도 동일한 오케스트레이션 데이터를 공동 작업할 수 있습니다. 고객은 대화식으로 자신의 의도를 설명하고 LLM이 적절한 MCP 도구를 호출하도록 할 수 있다.

## 주요 기능 {#mcp-capabilities}

[!DNL Adobe Journey Optimizer] MCP 서버를 사용하면 AI 도우미에서 직접 [!DNL Adobe Journey Optimizer]개의 여정, 캠페인 및 오퍼를 검사, 요약 및 해결할 수 있습니다. [!DNL Adobe Journey Optimizer]의 검색 API는 일반 언어 답변으로 변경되므로 다음을 수행할 수 있습니다.

* **여정 논리 이해** - 사람이 인식할 수 있는 여정 분기, 조건 및 작업에 대한 요약을 가져옵니다.
* **캠페인 준비 확인** - 캠페인이 게시되지 않도록 하는 차단기를 식별합니다.
* **범위 간격 확인** — 라이브 여정 및 캠페인에 적용되는 채널과 간격이 있는 위치를 확인합니다.
* **오케스트레이션 포트폴리오 감사** - JSON을 구문 분석하거나 제품 화면 사이를 이동하지 않고 캠페인 및 여정의 전체 상태를 검토합니다.

## 사용 사례 {#mcp-use-cases}

다음 예제는 자연어를 사용하여 [!DNL Adobe Journey Optimizer] MCP 서버와 상호 작용하는 방법을 보여 줍니다.

| 목표 | 예제 프롬프트 |
|---|---|
| **캠페인 세부 정보 요약** | &quot;캠페인 cmp456을 가져오고 대상, 일정, 상태 및 패키지를 요약합니다.&quot; |
| **인벤토리 및 상태 감사** | &quot;우리는 무엇을 가지고 있으며, 어떤 상태에 있습니까? 캠페인에 대한 실시간 및 초안, 완료/중지/보관된 수를 보여줍니다.&quot; |
| **게시 준비 확인** | &quot;campaign cmp456을 게시할 준비가 되지 않은 이유는 무엇입니까? 차단기를 보여 주세요.&quot; |
| **개체 비교** | &quot;캠페인 abc123과 xyz789 비교 — 상태 및 일정에서 변경된 사항?&quot; |
| **포트폴리오 감사** | &quot;모든 라이브 여정 및 캠페인에서 어떤 채널이 적용되며 그 차이는 어디에 있습니까?&quot; |
| **채널 범위 및 혼합** | &quot;여정, 캠페인 및 오퍼 배치(이메일 전용 및 다중 채널, 푸시/SMS/인앱 사용, 여정 채널 간 불일치)에서 채널 풋프린트를 표시합니다.&quot; |

## 전제 조건 {#mcp-prerequisites}

[!DNL Adobe Journey Optimizer] MCP 서버를 AI 도우미에 연결하기 전에 다음 사항을 확인하십시오.

* 활성 [!DNL Adobe Journey Optimizer] 라이선스가 있습니다.
* 지원되는 MCP 호환 애플리케이션(현재 클라우드 웹 또는 클라우드 데스크탑)에 액세스할 수 있습니다.
* [!DNL Adobe Journey Optimizer]에서 캠페인, 여정 및 오퍼를 볼 수 있는 권한이 있습니다.

## [!DNL Adobe Journey Optimizer] MCP 서버 연결 {#mcp-connect}

>[!NOTE]
>
>통합을 일반적으로 사용할 수 있게 되면 자세한 설정 단계가 추가됩니다. 조기 액세스는 Adobe 담당자에게 문의하십시오.

<!--
Step-by-step connection instructions to be added here, including:
- How to obtain MCP server credentials from [!DNL Adobe Journey Optimizer]
- How to configure the MCP server in Claude Desktop / Claude Web
- How to authenticate
-->

## 자주 묻는 질문 {#mcp-faq}

+++지원되는 AI 도우미는 무엇입니까?

[!DNL Adobe Journey Optimizer] MCP 서버는 현재 **클라우드 웹** 및 **클라우드 데스크톱**&#x200B;에서 사용할 수 있습니다. 추가 MCP 호환 애플리케이션에 대한 지원은 향후 릴리스에 추가될 수 있습니다.
+++

+++MCP를 통해 액세스할 수 있는 [!DNL Adobe Journey Optimizer] 개체는 무엇입니까?

캠페인, 여정, 오퍼, 충성도 데이터 및 샌드박스 정보에 액세스할 수 있습니다. 작업은 읽기 전용(API 검색)이며 쓰기 작업은 현재 릴리스에서 지원되지 않습니다.
+++

+++[!DNL Adobe Journey Optimizer] MCP 서버를 사용하려면 개발자 액세스 권한이 필요합니까?

아니요. MCP 서버는 마케팅 및 기술 담당자 모두를 위해 설계되었습니다. 마케터는 Claude의 자연어 프롬프트를 사용하여 상호 작용할 수 있으며, 개발자는 MCP를 지원하는 개발자 도구에서도 사용할 수 있습니다.
+++

+++AI 비서 공급자에게 데이터가 전송됩니까?

프롬프트를 제출하면 AI 도우미는 처리를 위해 해당 컨텍스트(MCP 서버에서 반환된 [!DNL Adobe Journey Optimizer] 데이터 포함)를 해당 모델에 보낼 수 있습니다. 프로덕션 데이터에 연결하기 전에 AI 지원 공급자의 개인정보 보호 및 데이터 처리 정책을 검토하십시오.
+++

