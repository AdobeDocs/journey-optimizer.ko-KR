---
solution: Journey Optimizer
product: journey optimizer
title: CX Coworker의 Journey Optimizer 기술
description: 자세한 지침과 샘플 프롬프트를 통해 CX Coworker에서 사용할 수 있는 Adobe Journey Optimizer 기술을 살펴보십시오.
feature: Overview
topic: Artificial Intelligence
role: User
level: Beginner
source-git-commit: 8400f5603934b6f9dfe9fe9df00aa5eb0736f847
workflow-type: tm+mt
source-wordcount: '2860'
ht-degree: 8%

---


# CX Coworker의 Journey Optimizer 기술 {#ajo-coworker-skills}

>[!BEGINSHADEBOX]

**이 페이지에서:** 각 스킬에 대한 자세한 지침, 예제 프롬프트 및 모범 사례를 통해 여정 생성 및 분석에서 채널 콘텐츠 생성에 이르기까지 CX Coworker에서 사용할 수 있는 Adobe Journey Optimizer 스킬을 살펴보십시오.

>[!ENDSHADEBOX]

## 개요 {#overview}

CX Coworker 는 Adobe Journey Optimizer에 AI 기반 기능을 제공합니다. [CX Coworker](https://experienceleague.adobe.com/ko/docs/cx-enterprise-coworker/content/home){target="_blank"}은(는) 비즈니스 애플리케이션과 통합하여 보다 효율적으로 작업할 수 있는 Adobe의 대화 환경입니다.

AI 기반의 기술을 갖춘 CX Coworker를 사용하면 Journey Optimizer 사용자가 자연어 인터페이스를 사용하여 마케팅 여정을 생성, 분석 및 최적화할 수 있습니다. 여정 기술을 통해 실무자는 신속하게 여정을 구축하고, 일정 또는 대상 충돌을 감지 및 해결하고, 성과 및 중단점을 분석하고, 향후 캠페인을 위해 복제할 최고 성과의 여정을 식별할 수 있습니다. 이를 통해 실무자는 데이터 중심의 의사 결정을 내리고, 고객 참여를 개선하며, 여정 오케스트레이션을 간소화할 수 있습니다.

CX Coworker 는 여정 및 충성도 문제를 관리하는 다양한 기술을 제공합니다.

**여정 중심 스킬:**

* **여정 만들기**: 자연어 프롬프트를 통해 마케팅 여정을 빌드하고 구성합니다.
* **채널 콘텐츠 만들기**: AI 기반 콘텐츠 생성을 사용하여 여정에 대한 채널별 콘텐츠(이메일, 푸시, SMS)를 생성하고 편집하고 관리합니다.
* **여정 분석**: 여정 분석, 문제 감지, 인사이트 발견 및 여정 성능 최적화

**충성도 중심 스킬:**

* **충성도 문제 관리**: 자연어 프롬프트를 사용하여 충성도 문제를 만들고 관리합니다.

<!--
feedback from Ivan: Need to remove Simulate skill from docs until Nico confirms the release timeline.

In addition, **Journey Simulation** is a Journey Optimizer feature that includes [Journey Simulate](https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/orchestrate-journeys/create-journey/simulate-journey/simulate-journey-gs), an in-product agentic skill, non conversational, with three capabilities: 

* Generating simulated users
* Generating event values
* Quick simulation
-->

## 여정 만들기

여정 만들기 를 사용하면 Journey Optimizer 사용자가 자연어 인터페이스를 사용하여 마케팅 여정을 구축하고 구성할 수 있습니다. 여정 만들기를 사용하면 전문가가 대화 프롬프트에서 요구 사항을 설명하여 여정을 빠르게 만들 수 있습니다. 이 기술은 사용자가 여정을 만들기 위한 다양한 옵션을 안내하므로 마케터가 기술 구성이 아닌 전략에 집중할 수 있습니다.

>[!AVAILABILITY]
>
>여정 만들기 기능을 완전히 사용하려면 다음 권한이 필요합니다.
>
>**여정 관리**: 이 권한을 사용하면 CX Coworker에서 직접 새 여정을 만들 수 있습니다.
>
>**여정 이벤트, 데이터 소스 및 작업 보기**: 이 권한을 사용하면 CX 동료가 여정 이벤트 및 사용자 지정 작업을 검색할 수 있습니다.
>
>**세그먼트 보기**: 이 권한은 CX Coworker가 여정을 만들 때 대상 세그먼트를 검색할 수 있도록 합니다.
>
>**세그먼트 관리**: 이 권한을 사용하면 CX Coworker에서 직접 새 대상을 만들 수 있습니다.

### 주요 사용 사례

여정 만들기 마케팅 실행을 가속화하는 데 활용할 수 있는 오퍼 기능:

1. **이벤트가 트리거된 여정 만들기**

   * 특정 고객 이벤트를 기반으로 활성화되는 여정을 만듭니다.
   * 고객 행동에 대한 자동화된 반응을 실시간으로 디자인할 수 있습니다.
   * 고객 행동을 기반으로 개인화된 커뮤니케이션 흐름을 구축하세요.

   **스토어 방문 여정:**
   &quot;사용자가 내 스토어 위치를 입력할 때 시작되는 여정을 만듭니다. 스토어에 오신 사용자를 환영하기 위해 푸시 알림을 보냅니다. 2일 동안 기다렸다가 사용자에게 유효한 이메일 주소가 있는지 확인합니다. 사용자에게 유효한 이메일 주소가 있는 경우 스토어 경험을 묻는 이메일 설문 조사를 보냅니다. 사용자에게 유효한 이메일 주소가 없는 경우 푸시 알림을 보내 등록 여부를 묻습니다.&quot;

   **구매 후 여정:**
   &quot;고객이 온라인으로 구매할 때 시작되는 여정을 만듭니다. 구매에 대한 감사를 표하기 위해 푸시 알림을 보냅니다. 다음으로 충성도 멤버인지 확인합니다. 사용자가 충성도 보상 멤버인 경우 10% 할인 코드가 있는 두 번째 푸시 알림을 보냅니다. 사용자가 충성도 보상 멤버가 아닌 경우 충성도 프로그램에 등록할 수 있도록 초대하는 푸시를 보냅니다. 2일 동안 기다린 후 구매 경험에 대한 설문 조사를 통해 후속 푸시를 보내십시오.&quot;

   **이벤트 기반 승격:**
   &quot;게임 점수가 50점이 될 때 트리거되는 여정을 만듭니다. 충성도 보상 회원에게 파트너 스폰서로부터 무료 피자 한 조각을 받을 수 있다는 SMS 메시지를 보냅니다.&quot;

1. **대상 타깃팅된 여정 만들기**

   * 특정 대상 세그먼트를 타겟팅하는 여정을 빌드합니다.
   * 전략적 타이밍으로 다단계 커뮤니케이션 시퀀스를 설계합니다.

   **시즌 캠페인:**
   &quot;일일 등산객의 대상을 타겟팅하는 여정을 만들고 싶습니다. 다양한 하이킹 필수품을 포함한 다가오는 휴일 세일에 대해 이 대상자에게 경고하는 이메일을 보내려고 합니다. 첫 번째 이메일을 보낸 후 3일 후에 기다렸다가 무료 배송이 포함된 15% 쿠폰이 포함된 두 번째 이메일을 보냅니다. 1주 정도 기다린 후 새로운 침낭과 텐트 컬렉션을 보여주는 세 번째 이메일 메시지를 보내세요. 여정이 2020년 12월 20일에 시작되도록 예약합니다.&quot;

   **충성도 평가:**
   무료 세차 오퍼가 포함된 감사 푸시 알림과 첫 번째 알림이 1일 이내에 상호 작용하지 않을 경우 후속 푸시 알림 미리 알림을 포함하여 SUV 소유자를 위한 로열티 감사 여정을 구축합니다.

1. **비즈니스 이벤트 트리거 여정 만들기**

   * 특정 비즈니스 이벤트를 기반으로 활성화되는 여정을 만들고 지정된 대상(예: 제품 재입고 또는 게임 점수 변경)을 타겟팅합니다
   * 비즈니스 상태가 변경될 때 상황에 맞는 메시지를 적시에 트리거합니다.

1. **대상 자격 여정 만들기**

   * 프로필이 대상 세그먼트 정의를 입력하거나 종료할 때 활성화되는 여정을 만듭니다.
   * 시작 및 종료 메시지를 자동화하여 온보딩, 유지 및 윈백 목표를 지원합니다.

1. **조건부 여정 흐름**

   * 고객 속성을 기반으로 의사 결정 분기를 만듭니다.
   * 고객 환경 설정에 맞게 분할된 경로 디자인

1. **이미지에서 여정 만들기**

   * 참조 이미지를 동료에 업로드하고 이미지를 참조로 사용하여 여정을 생성하도록 요청합니다
   * 여정 작성 스킬은 참조 이미지에서 편집 가능한 프롬프트를 추출합니다.

이 기술을 사용하면 자연어 요구 사항이 구조화된 여정 구성으로 변환됩니다.

### 범위 스킬 내

여정 만들기에서 지원하는 기능은 다음과 같습니다.

* **자연어 여정 만들기**: 사용자가 대화 언어로 여정 흐름을 설명할 수 있도록 허용합니다.
* **이벤트 기반 및 대상 기반 여정**: 트리거 기반 및 예약된 여정 유형과 비즈니스 이벤트 및 대상 자격을 모두 지원합니다.
* **조건부 논리**: 고객 특성에 따라 의사 결정 분할과 분기를 처리합니다.
* **다중 채널 메시징**: 푸시 알림, 전자 메일 및 SMS 채널을 지원합니다.
* **여정 예약**: 예약된 여정의 시작 날짜 및 시간을 구성합니다.

### 범위 외 스킬

현재 다음 기능은 지원되지 않습니다.

* 고급 여정 분석
* 크로스 여정 오케스트레이션
* A/B 테스팅 구성
* InAudience 표현식 생성
* 데이터 세트 조회 노드
* 웨이브 전송 설정
* 자동연장 옵션 예약
* 대상을 위한 네임스페이스 선택
* 사용자 지정 작업 필드 매핑
* 복잡한 데이터 변환

### 프롬프트 우수 사례

여정 만들기의 효과를 극대화하려면 다음 모범 사례를 따르십시오.

1. **구체적으로**: 여정 목표, 대상 및 원하는 작업에 대한 자세한 정보를 제공합니다. 채널, 시간 및 조건에 대한 정보를 포함합니다.
1. **시간 지정**: 동작 사이의 대기 기간과 여정을 시작해야 하는 시기를 명확히 나타냅니다.
1. **조건 정의**: 조건부 논리를 사용할 때는 각 분기 경로의 기준을 설명하십시오.
1. **채널 포함**: 사용할 통신 채널(푸시, 이메일, SMS)을 지정합니다.
1. **예약 언급**: 예약된 여정의 경우 원하는 시작 날짜 및 시간을 제공하십시오.
1. **사용자 지정 작업**: 워크플로우에서 사용자 지정 작업을 사용하는 경우 사용자 지정 작업의 정확한 이름과 함께 사용자 지정 작업을 사용하고 있음을 지정해야 합니다. 예:
사용자가 내 스토어 위치를 입력하면 사용자 지정 작업 ExternalPush를 사용하여 환영 메시지를 보냅니다. 2일 동안 기다린 다음 사용자 지정 작업 ExternalEmail을 사용하여 방문에 대한 설문 조사와 함께 후속 메시지를 보냅니다.
1. **식 유효성 검사**: 올바른 필드와 값이 사용되었는지 확인하려면 여정 기술에서 만든 식을 확인하고 검사해야 합니다.

### 모범 사례 설정

* **명확한 목표 정의**: 여정을 만들기 전에 명확한 목표(유지 개선, 전환 촉진, 참여 증가)를 설정하십시오.
* **대상 준비**: 대상 대상이 이미 만들어져 있고 올바르게 세그먼트화되었는지 확인하십시오.
* **메시지 콘텐츠 계획**: 여정을 만들기 전에 메시징 전략을 정의하십시오.
* **고객 경험 고려**: 고객 환경 설정을 준수하고 과도한 커뮤니케이션을 방지하는 여정 흐름을 디자인합니다.

## 채널 컨텐츠 만들기

<!--Ivan : Need to speak with Amar on new options for content generation as this skill has changed. -->

>[!AVAILABILITY]
>
>이 기능은 제한된 가용성의 모든 고객이 사용할 수 있습니다. 액세스 권한을 얻으려면 Adobe 담당자에게 문의하십시오.

채널 컨텐츠 만들기 를 사용하면 Journey Optimizer 사용자가 AI 기반 컨텐츠 생성을 사용하여 여정에 대한 채널별 컨텐츠를 생성, 편집 및 관리할 수 있습니다.

### 주요 사용 사례

1. **채널별 콘텐츠 생성**: 자연어 프롬프트를 사용하여 이메일, 푸시 알림, SMS 및 기타 채널에 대한 콘텐츠를 생성합니다.

   &quot;내 환영 여정에 대한 이메일 콘텐츠를 생성합니다. 친근한 어조로 새로운 고객을 위한 환영 이메일을 만들고 10% 할인 오퍼를 포함하십시오.&quot;

   &quot;내 스토어 방문 여정에 대한 푸시 알림을 생성합니다. 고객이 체크인하고 특별 오퍼를 받을 수 있도록 격려하는 환영 메시지를 만드십시오.&quot;

   &quot;이벤트가 트리거된 여정에 대한 SMS 콘텐츠를 생성합니다. call-to-action을 사용한 플래시 판매에 대해 고객에게 알리는 짧은 메시지를 만듭니다.&quot;

1. **템플릿 기반 콘텐츠 만들기**: 미리 보기 기능이 있는 사용 가능한 템플릿에서 찾아 선택합니다.

   &quot;시즌 캠페인 여정에 사용할 수 있는 이메일 템플릿을 표시합니다.&quot;

   &quot;현대적이고 깔끔한 디자인의 내 이메일에 대한 템플릿을 선택하십시오.&quot;

1. **다중 채널 콘텐츠 관리**: 동일한 여정 워크플로 내에서 여러 채널에 대한 콘텐츠를 생성하고 관리합니다.

1. **컨텍스트 내 콘텐츠 편집**: 편집 및 개선을 위해 Content Designer에서 생성된 콘텐츠를 엽니다.

   &quot;디자인을 사용자 지정할 수 있도록 컨텐츠 Designer에서 이메일 컨텐츠를 엽니다.&quot;

1. **콘텐츠 개선 및 반복**: 다시 생성 작업을 사용하여 색조 또는 스타일이 다른 콘텐츠를 다시 생성합니다.

   &quot;보다 캐주얼한 톤으로 푸시 알림 콘텐츠를 다시 생성합니다.&quot;

   &quot;프로모션 코드를 포함하도록 이메일 콘텐츠를 업데이트합니다.&quot;

1. **여정 캔버스 통합**: 인벤토리에서 여정을 선택하고 관련 채널을 봅니다.

### 범위 스킬 내

채널 콘텐츠 작성은 다음 기능을 지원합니다.

* **AI 기반 콘텐츠 생성**: 자연어 프롬프트를 사용하여 이메일, 푸시, SMS 및 기타 채널에 대한 콘텐츠를 생성합니다.
* **템플릿 관리**: 미리 보기 기능이 있는 사용 가능한 템플릿 중에서 찾아 선택합니다.
* **직접 편집**: 편집 및 개선을 위해 Content Designer에서 생성된 콘텐츠를 엽니다.
* **콘텐츠 다시 생성**: 다시 생성 작업을 사용하여 색조, 스타일 또는 메시징이 다른 콘텐츠를 다시 생성합니다.
* **다중 채널 지원**: 동일한 여정 워크플로 내에서 여러 채널에 대한 콘텐츠를 생성하고 관리합니다.
* **여정 인벤토리 액세스**: 인벤토리에서 여정을 선택하고 관련 채널을 봅니다.

### 범위 외 스킬

현재 다음 기능은 지원되지 않습니다.

* **브랜드 정렬 및 콘텐츠 품질 검사**
* **콘텐츠 노드를 여정 캔버스에 직접 삽입**
* **템플릿 가져오기**

### 프롬프트 우수 사례

1. **고유해야 함**: 콘텐츠 형식, 색조, 대상 및 키 메시지에 대한 자세한 내용을 제공합니다.
1. **채널 지정**: 콘텐츠를 만드는 채널(전자 메일, 푸시, SMS)을 명확하게 표시합니다.
1. **톤 정의**: 원하는 톤(친숙한 톤, 정형적인 톤, 캐주얼한 톤, 긴급 톤)을 지정합니다.
1. **반복 및 세분화**: 요구 사항을 충족할 때까지 재생성 작업을 사용하여 콘텐츠를 세분화합니다.

## 충성도 과제 관리

>[!AVAILABILITY]
>
>충성도 기술은 CX Coworker 를 통해 지원 대상이 되는 조직에서 사용할 수 있습니다. 고객 충성도 라이센스를 보유한 고객은 추가 CX Coworker 라이센스가 없는 경우에도 이러한 충성도 기술에 액세스할 수 있습니다.

Loyalty Challenge Management를 사용하면 Journey Optimizer 사용자가 자연어 프롬프트를 사용하여 CX Coworker에서 충성도 문제를 만들고 관리할 수 있습니다. 자세한 설정 지침을 포함하여 충성도 문제를 만들고, 구성하고, 관리하는 방법에 대한 포괄적인 설명서는 [충성도 문제 안내서](../loyalty-challenges/get-started.md)를 참조하십시오.

### 주요 사용 사례

1. **여러 단계 온보딩 과제**

   &quot;새로 등록한 고객을 위해 당좌 예금을 개설하고 최소 500달러의 자금을 조달하며 모바일 앱을 다운로드하는 등의 단계를 순서대로 완료해야 하는 &quot;새 계정 킥스타트&quot;라는 과제를 작성하십시오. 모든 단계가 완료되면 5,000점의 보너스 포인트로 보상하십시오. 동부 시간대인 9월 1일부터 10월 31일까지 실행하십시오.&quot;

1. **누적 활동 임계값 챌린지**

   &quot;3분기 동안 카드 회원이 신용 카드로 1,500달러를 쓰면 50달러 명세서 크레딧을 받는 카드 회원을 위한 &quot;Spend &amp; Earn Summer&quot;라는 과제를 만드십시오. 동부 표준 시간대인 7월 1일부터 시작합니다.&quot;

1. **연속 빈도 시도**

   &quot;2개월 연속 매달 3회 비행이 필요한 엘리트 계층 회원들을 위한 &quot;Frequent Flyer Sprint&quot;라는 도전을 만들어라. 계층 상태 확장 및 10,000 보너스 마일로 완료 보상. 다음 달 1일, 태평양 시간대를 시작합니다.&quot;

1. **단일 자격 액션 과제**

   &quot;자동결제에 등록한 후 30일 이내에 페이퍼리스 청구로 전환하면 후불 가입자에게 500개의 보너스 포인트를 지급하는 &quot;Go 페이퍼리스&quot;라는 과제를 설정하세요. 다음 달 1일, 중부 시간대에서 시작합니다.&quot;

1. **참여/소비 목표 과제**

   8월 한 달 동안 최소 3개의 다른 카테고리에서 5개의 활동을 완료해야 하는 멤버에 대해 &quot;탐색기 배지&quot;라는 문제를 만듭니다. 완료 시 1,000포인트와 &quot;Explorer&quot; 배지로 보상합니다. 산악 시간대인 8월 1일부터 시작합니다.&quot;

1. **일일 작업 과제**

   &quot;말차 애호가들을 위한 도전을 만드는데 도움을 주세요. 말차 애호가들은 매주 매장에 와서 말차 음료를 사야만 합니다. 도전을 완수하면 200점을 더 줘야 한다. &quot;Mad about Matcha&quot;로 부르고, SKU matcha-001을 사용하고, 동부 표준 시간대인 다음 주 월요일에 시작하십시오.&quot;

### 범위 스킬 내

충성도 과제 관리에서 지원하는 기능은 다음과 같습니다.

* **도전 만들기**: 자연어(대상, 작업 기준, 시간, 보상, 이름 지정)에서 도전 구성을 만듭니다.
* **과제 업데이트**: 반복적인 프롬프트를 통해 과제 세부 정보를 수정합니다.
* **챌린지 게시**: 지원되는 챌린지 구성을 대화에서 직접 게시합니다.
* **문제 컨텍스트 가시성**: 반복하는 동안 문제 정보를 검색하고 검토합니다.

### 범위 외 스킬

현재 다음 기능은 지원되지 않습니다.

* 과제 삭제
* 충성도 통찰력 및 추천 기술
* 모든 경우의 과제 메시지를 위한 완벽한 콘텐츠 작성 자동화

### 프롬프트 우수 사례

1. **이름 지정**: 명확하고 기억에 남는 제목을 따옴표로 묶습니다.
1. **대상 지정**: 자격 조건을 갖춘 사람(예: 모든 구성원, 계층, 세그먼트, 새 등록자, 카드 소유자, 구독자).
1. **작업과 양을 정의합니다**: 구성원이 수행해야 하는 작업과 완료로 계산되는 빈도, 임계값 또는 순서.
1. **기간을 설정하십시오**: 시작 날짜(기간이 고정된 경우 종료 날짜)와 표준 시간대를 더한 값입니다.
1. **보상 설명**: 포인트, 마일, 문 크레딧, 상태 확장, 바우처 또는 완료 시 부여된 권한.
1. **자격 부여 이벤트 참조**: 문제가 추적하는 특정 SKU, 제품, 계정 작업 또는 참여 이벤트를 가리킵니다.

## 여정 분석

여정 기술을 통해 Journey Optimizer 사용자는 자연어 인터페이스를 사용하여 여정을 분석하고 최적화할 수 있습니다. 실무자는 여정 기술을 통해 스케줄 및/또는 대상 충돌을 신속하게 식별 및 해결하고, 여정에서 사용자 포기 지점을 감지하고 통찰력 또는 권장 사항을 제공할 수 있습니다. 이를 통해 실무자는 데이터 중심의 의사 결정을 내리고, 고객 참여를 개선하며, 여정 오케스트레이션을 간소화할 수 있습니다.

>[!AVAILABILITY]
>
>여정 기술은 CX Coworker를 액세스할 수 있는 모든 고객이 사용할 수 있습니다. 하지만 여정 스킬 기능을 완전히 사용하려면 다음 권한이 필요합니다.
>
>**여정 보기**: 이 권한을 사용하면 CX Coworker에서 직접 여정에 대한 인사이트를 볼 수 있습니다.
>
>**여정 관리**: 이 권한을 사용하면 CX Coworker에서 직접 새 여정을 만들 수 있습니다.
>
>**세그먼트 보기**: 이 권한을 사용하면 CX Coworker에서 직접 대상자에 대한 통찰력을 볼 수 있습니다.
>
>**세그먼트 관리**: 이 권한을 사용하면 CX Coworker에서 직접 새 대상을 만들 수 있습니다.

### 주요 사용 사례

여정 분석은 마케팅 노력을 최적화하기 위해 활용할 수 있는 다양한 기능을 제공합니다.

1. **여정 폴아웃 분석**

   * 고객이 여정 중에 어디서, 왜 이탈하는지 파악합니다.
   * 고객 이탈로 이어지는 고객 행동 패턴을 감지합니다.
   * 인사이트를 활용하여 여정 설계를 개선하고 유지력을 향상시킵니다.

   샘플 프롬프트:
   * &quot;7월 4일 여정 캠페인에 대한 노드별 폴아웃을 분석하려고 합니다.&quot;
   * &quot;7월 4일 여정 캠페인에 대한 폴아웃 분석을 수행합니다.&quot;
   * &quot;7월 4일 여정 과정에서 프로필이 손실된 이유는 무엇입니까?&quot;
   * &quot;7월 4일 여정에서 사용자가 드롭오프하는 위치를 표시합니다.&quot;

1. **여정 대상자 오버랩 분석**

   * 여러 여정에서 대상자 오버랩이 되는 부분을 분석합니다.
   * 과도한 타기팅으로 인한 대상자 피로를 예방합니다.
   * 균형 잡힌 참여를 보장하기 위해 세분화를 최적화합니다.

   샘플 프롬프트:
   * &quot;X개 이상의 여정에서 사용되는 대상자는 무엇입니까?&quot;
   * &quot;[대상 이름] 대상을 사용하는 모든 여정을 나열합니다.&quot;
   * &quot;여정 [여정 이름]에 대한 대상 겹침 충돌 표시&quot;
   * &quot;여정 [여정 이름] 및 다른 여정에 대해 겹치는 대상을 표시합니다.&quot;

1. **여정 일정 오버랩 분석**

   * 동일한 대상자를 타기팅하여 예약된 여정 간의 시간 충돌을 감지합니다.
   * 과도한 의사소통을 피하고 예약 효율성을 향상시킵니다.
   * 여정이 최적의 시간에 진행되도록 하여 대상자에게 미치는 영향력을 극대화합니다.

   샘플 프롬프트:
   * &quot;여정 [여정 이름]에 대해 일정 충돌이 있습니까?&quot;
   * &quot;여정 [여정 이름]과(와) 관련된 일정 충돌을 확인하십시오.&quot;
   * &quot;여정 [여정 이름]과(와) 실시간 여정 간 일정이 겹칩니다.&quot;
   * &quot;[여정 이름] 여정이 다른 여정과 충돌하여 실행되고 있습니까?&quot;

1. **운영 인사이트**

   * 프롬프트 기반 여정 인사이트 - 여정에 대한 운영적인 인사이트 표시 , 즉 &quot;모든 라이브 여정 표시&quot;

   샘플 프롬프트:
   * &quot;[여정 이름]이(가) 게시된 시기는 언제입니까?&quot;
   * &quot;[여정 이름]이(가) 중지된 시기는 언제입니까?&quot;
   * &quot;현재 테스트 모드에 있는 모든 여정 나열&quot;
   * &quot;보유한 라이브 여정은 몇 개입니까?&quot;
   * &quot;모든 예약된 반복 여정 및 예상 실행 시간 목록을 제공합니다.&quot;

## 범위 스킬 내

여정 분석에서는 다음 기능이 지원됩니다.

* **반응형 쿼리**: 사용자가 여정 성과, 대상자 사용, 일정 충돌에 대해 구체적인 질문을 할 수 있습니다.
* **다른 스킬과 통합**: 심층 분석을 위해 Audience 및 Data Insights 기능과 공동 작업합니다.
* **응답 구조**: 추론(논리 설명), 분석 요약(주요 사항 강조 표시), 문제 세부 정보(문제 설명) 및 권장 사항(다음 단계 제안).

### 범위 외 기술

현재 다음 기능은 지원되지 않습니다.

* **여정 생성 자동화**
* **실시간 예외 항목 탐지**
* **채널 겹치기**
* **여정 입력 분석**
* **기술 문제 분석**
* **피로도 분석**

### 프롬프트 모범 사례

여정 분석의 효과를 극대화하려면 다음 모범 사례를 따르십시오.

1. **구체적으로 말하기**: 명확하고 간결한 프롬프트를 사용하여 타기팅된 인사이트를 얻습니다. 예를 들어 &quot;내 여정은 무엇입니까?&quot;를 묻는 대신 &quot;지난 달에 만든 모든 여정 나열&quot;을 지정합니다.
1. **인사이트 결합**: Audience 및 Data Insights 기능의 인사이트를 통합하여 여정 성능을 전체적으로 볼 수 있습니다.
1. **반복적인 개선**: 폴아웃 및 중복 분석을 사용하여 여정 설계와 일정을 반복적으로 개선합니다.

### 모범 사례 설정

* **명확한 목표 정의**: 여정을 분석하기 전에 명확한 목표(예: 유지율 향상, 전환율 증가)를 설정합니다.
* **정기적 모니터링**: 여정 성과를 정기적으로 검토하여 트렌드 및 예외 항목을 파악합니다.
* **세분화 최적화**: 피로를 막고 참여도를 극대화할 수 있도록 대상자 세분화를 균형 있게 조정합니다.

<!--
Journey analysis new skills to document:

Journey Custom Action Error Analysis
- Identify when custom actions are failing or error rates spike within a journey.
- Diagnose root causes before failures cascade into broader journey disruption.
- Use specific remediation steps to restore custom action reliability quickly.

Journey Anomaly Detection
- Detect unexpected spikes or drops in journey sends and exits against historical baselines.
- Catch send or exit volume issues early, before they affect a large share of your audience.
- Use the insights to pinpoint the root cause and keep the journey performing as expected.
-->

<!--
Feedback from Ivan: Journey simulate is not ready as a skill

## Journey Simulate: Use Cases, Agentic Skills and User Guide

## Overview

>[!BEGINSHADEBOX]

Journey Simulation is available to all Journey Optimizer customers. Journey Simulate, the in-product agentic skill within Journey Simulation, is available to customers that are a part of the Agent Orchestrator Explorer program and requires at least one of the following permissions:

* **Simulate journeys**: Run simulation workflows from the journey canvas.

* **Publish journeys**: Publish journeys, including flows that use simulation before go-live.

* **Approve and Publish journeys**: Approve and publish journeys when your organization uses approval workflows.

To use AI in **[!UICONTROL Simulation]** (**[!UICONTROL Quick simulation]**, generating simulated users with AI, **[!UICONTROL Generate event values]**), users require **[!UICONTROL Generate Content]** permission from the **[!UICONTROL AI Assistant]** capability. 

[Learn more about permissions](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/administration/permissions).

>[!ENDSHADEBOX]

Journey Simulation is a Journey Optimizer feature that enables Journey Optimizer users to safely test and validate marketing journeys before activation. Within Journey Simulation, Journey Simulate is an in-product agentic skill, not a conversational one, that automates and assists the testing process directly from the journey canvas.

Journey Simulate includes three capabilities:

* Generating simulated users
* Generating event values
* Quick simulation. 

Together, they bridge the gap between journey creation and activation, building confidence in journey logic and reducing the risk of post-launch errors.

## Use cases

### Key use cases for Journey Simulate

Journey Simulate offers three capabilities that can be leveraged to reduce testing time and improve journey quality before go-live:

**Generating simulated users**

* Generate simulated users automatically based on journey paths and required attributes.
* Create simulated users that cover all branches and conditions in a journey, including execution addresses (email, push, SMS).
* Update simulated user attributes on demand to refine test scenarios.
* Ensure all journey branches are covered by assigning the right simulated user to each path.

**Generating event values**

* Generate values for events used in a journey to drive test execution through specific paths.
* Define event attribute values that trigger the desired conditions and branches during simulation.

**Quick simulation**

* Start journey simulation and trigger test executions for all simulated users needed to test all paths of a journey, in a single interaction.
* Visualize how simulated users flow through a journey, step by step, including branching paths and conditional logic.
* Identify which simulated user flows through which path, and why, with detailed node-by-node traversal.
* Review simulation reporting at the end of a run in the Journey Optimizer UI to validate outcomes before activation.

## In scope skills and limitations

### **In scope**

The following capabilities are supported by the Journey Simulation feature:

* **Simulated user management**: View, edit, and update simulated user attributes, including execution addresses and personalization data.
* **Simulation control**: Start and stop journey simulation directly through the Journey Simulation in-product experience.
* **Test execution**: Trigger test executions for one or multiple simulated users.
* **Journey flow visualization**: View step-by-step traversal of simulated users through journey nodes, including branching, splits, and user status.
* **Simulation reporting**: View reporting at the end of a simulation run in the Journey Optimizer UI.
* **Multi-user testing**: Run and visualize tests for multiple simulated users simultaneously, covering all journey branches.

In addition to this, the following capabilities are supported by the Journey Simulate skill:

* **Simulated user generation**: Create simulated users based on journey paths, existing test profiles, or specified attributes.
* **Event value generation**: Generate and assign event attribute values to drive test execution through specific journey paths.
* **Quick simulation**: Run a full end-to-end simulation with minimal intervention. The skill automatically generates simulated users, event values, and pre-filled test settings, then executes the journey and surfaces results for review.

### **Limitations**

Simulation may not support every activity, channel, or integration that Test mode or a live journey supports, and behavior may change as the capability matures.

➡️ Learn more about [Simulation limitations](https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/orchestrate-journeys/create-journey/simulate-journey/simulate-journey-gs#limitations) in the Journey Optimizer documentation.

-->
