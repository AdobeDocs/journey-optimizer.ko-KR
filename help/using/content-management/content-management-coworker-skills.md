---
solution: Journey Optimizer
product: journey optimizer
title: 컨텐츠 관리를 위한 동료
description: 자세한 지침과 샘플 프롬프트를 통해 Journey Optimizer 콘텐츠 에셋을 검색, 생성 및 관리하는 데 사용할 수 있는 CX Enterprise Coworker 콘텐츠 관리 도구를 살펴보십시오.
feature: Overview
topic: Artificial Intelligence
role: User
level: Beginner
mini-toc-levels: 1
exl-id: 9f23a6f5-7221-4f87-95cd-047955ca33d5
feature_v2:
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
    internal-label: Content management
subfeature_v2:
  - id: d595a60b-bcf5-4a63-a189-66a0be755cc7
    internal-label: Templates
source-git-commit: 2e8b79e40abe397222b76c2a7b1ff4dcfcc90292
workflow-type: tm+mt
source-wordcount: '759'
ht-degree: 2%
---

# 컨텐츠 관리를 위한 동료 {#content-management-coworker-skills}

>[!BEGINSHADEBOX]

**이 페이지에서:** 자세한 지침, 예제 프롬프트 및 모범 사례를 사용하여 콘텐츠 템플릿, 조각, 랜딩 페이지 및 여정/캠페인 인라인 콘텐츠를 탐색, 만들기, 업데이트, 복제 및 게시할 수 있는 Adobe Journey Optimizer에서 사용할 수 있는 CX Enterprise Coworker 콘텐츠 관리 도구를 살펴보십시오.

자세히 알아보기:

* [Journey Optimizer의 동료 기술](../start/ai-features.md#cx-coworker-skills) - Journey Optimizer의 여정, 충성도 및 컨텐츠 관리에 대한 동료 기술 개요.
* [Coworker 설명서](https://experienceleague.adobe.com/ko/docs/cx-enterprise-ai/experience-cloud-ai/coworker/overview){target="_blank"} - Coworker의 캠페인, 채팅 및 프로젝트 기능에 대한 개요입니다.
* [동료 채팅 UI 안내서](https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/ui-guide){target="_blank"} - 동료 채팅에 액세스하고 탐색하는 방법.

>[!ENDSHADEBOX]

## 콘텐츠 관리 도구 {#content-management}

>[!AVAILABILITY]
>
>콘텐츠 관리는 Coworker에 액세스할 수 있는 모든 고객이 사용할 수 있습니다.

Journey Optimizer 사용자는 자연어 프롬프트를 사용하여 Coworker에서 직접 콘텐츠 템플릿, 조각, 랜딩 페이지 및 여정/캠페인 인라인 메시지 콘텐츠와 같은 콘텐츠 에셋을 검색하고 관리할 수 있습니다. 이 옵션을 사용하면 대화에서 나가지 않고 &quot;내 콘텐츠 설명&quot;에서 &quot;작성, 업데이트 및 게시&quot;로 이동할 수 있습니다. 이 기능은 Journey Optimizer 콘텐츠용 읽기 및 쓰기 가능 MCP 도구 15개를 통해 제공됩니다.

### 주요 사용 사례

1. **콘텐츠 검색 및 검사**

   * 사용 가능한 콘텐츠 템플릿, 조각 또는 랜딩 페이지를 나열하고 구조, 메타데이터 및 상태를 검색합니다.
   * 여정 또는 캠페인 작업 노드에 구성된 인라인 메시지 콘텐츠를 검색합니다.

   샘플 프롬프트:
   * &quot;내 이메일 콘텐츠 템플릿을 나열합니다.&quot;
   * &quot;여름 캠페인에 사용할 수 있는 조각을 표시합니다.&quot;
   * &quot;랜딩 페이지-123의 세부 정보를 가져옵니다.&quot;
   * &quot;Campaign camp-789에서 작업 노드의 이메일 변형에 대해 구성된 콘텐츠는 무엇입니까?&quot;

1. **콘텐츠 템플릿 만들기**

   * 모든 채널에 대해 새 콘텐츠 템플릿을 만듭니다.

   샘플 프롬프트:
   * &quot;이 HTML 콘텐츠로 Summer Sale이라는 이메일 템플릿을 만듭니다.&quot;
   * &quot;Flash Alert라는 새 SMS 템플릿을 만듭니다.&quot;

1. **콘텐츠 템플릿 업데이트**

   * 기존 템플릿의 콘텐츠를 완전히 바꿉니다.

   샘플 프롬프트:
   * &quot;이 새로운 HTML 본문으로 템플릿 abc-123을 업데이트합니다.&quot;

1. **조각 만들기, 업데이트, 복제 및 게시**

   * 새 HTML 또는 표현식 조각을 만듭니다.
   * 기존 조각의 콘텐츠 또는 메타데이터를 업데이트합니다.
   * 새 이름으로 기존 조각을 복제합니다.
   * 발행할 초안 조각을 제출합니다.

   샘플 프롬프트:
   * &quot;이 마크업을 사용하여 프로모션 배너라는 HTML 조각을 만듭니다.&quot;
   * &quot;조각 frag-456을 업데이트하여 이름을 프로모션 배너 V2로 변경합니다.&quot;
   * &quot;복제 조각 abc-123을 프로모션 배너로 - 여름 (변형 B).&quot;
   * &quot;조각 frag-456을 게시합니다.&quot;

1. **인라인 메시지 콘텐츠 업데이트**

   * 캠페인 또는 여정 작업 노드의 인라인 메시지에서 하나의 채널 변형을 대체합니다.
   * 여정 또는 캠페인 작업 노드에 정의된 채널 변형을 나열합니다.

   샘플 프롬프트:
   * &quot;이 새로운 콘텐츠로 campaign camp-789의 작업 노드의 이메일 변형을 업데이트하십시오.&quot;
   * &quot;이 작업 노드에 정의된 채널 변형은 무엇입니까?&quot;

### 범위 내

컨텐츠 관리에서 지원하는 기능은 다음과 같습니다.

* **콘텐츠 템플릿 나열 및 가져오기**: 콘텐츠 템플릿을 검색하고 구조와 메타데이터를 검색합니다.
* **조각 나열 및 가져오기**: 콘텐츠 및 표현식 조각을 찾아 세부 정보를 검색합니다.
* **랜딩 페이지 나열 및 가져오기**: 랜딩 페이지를 검색하고 메타데이터와 페이지 콘텐츠를 검색합니다.
* **캠페인/여정 인라인 콘텐츠 가져오기**: 다국어 변형을 포함하여 캠페인 또는 여정 작업 노드에 구성된 인라인 메시지 콘텐츠를 검색합니다.
* **콘텐츠 템플릿 만들기**: 모든 채널에 대해 새 템플릿을 만듭니다.
* **콘텐츠 템플릿 업데이트**: 기존 템플릿의 콘텐츠를 완전히 바꿉니다.
* **조각 만들기, 업데이트, 복제 및 게시**: 새 조각을 만들고 기존 조각을 업데이트하며 새 이름으로 조각을 복제하고 게시하기 위해 초안 조각을 제출합니다.
* **인라인 메시지 콘텐츠 업데이트**: 캠페인/여정 동작 노드의 인라인 메시지에 있는 채널 변형(다국어 변형 포함)을 바꾸고 동작 노드에 정의된 채널 변형을 나열합니다.

### 범위를 벗어남

현재 다음 기능은 지원되지 않습니다.

* **템플릿 또는 조각에 대한 전체 텍스트 검색**
* **템플릿 또는 조각 유효성 검사**(분리된 참조, 끊어진 링크, 더 이상 사용되지 않는 구성 요소)
* **랜딩 페이지 만들기 또는 게시**
* **콘텐츠 템플릿, 조각 또는 랜딩 페이지 삭제**

### 프롬프트 우수 사례

1. **알려진 경우 참조 ID**: 특정 에셋을 가져오거나 업데이트하거나 복제하거나 게시하도록 요청할 때 템플릿, 조각, 랜딩 페이지 또는 캠페인/여정 ID를 제공합니다.
1. **채널에 대해 자세히 표시**: 템플릿 또는 조각을 만들 때 채널 또는 콘텐츠 형식(전자 메일, HTML 조각, 표현식 조각)을 지정하십시오.
1. **게시 전에 확인**: 조각의 콘텐츠를 만들거나 업데이트한 후 Coworker에게 게시하도록 요청하기 전에 해당 조각의 콘텐츠를 검토합니다.
1. **전체 대체 콘텐츠 제공**: 업데이트 작업은 전체 콘텐츠를 대체하므로 전체 HTML 본문 또는 변형 콘텐츠를 프롬프트에 포함하십시오.

{{$include /help/_includes/do-not-localize/start/ai-augmented-content-management-coworker-skills.md}}
