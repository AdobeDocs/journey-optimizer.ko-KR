---
solution: Journey Optimizer
product: journey optimizer
title: 충성도 문제 시작
description: Adobe Journey Optimizer에서 충성도 문제를 만들고 관리하여 매력적이고 보람 있는 충성도 프로그램을 구축하는 방법을 알아봅니다.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 1c84d9d0-cef7-4764-9f72-5428597a7203
feature_v2: []
subfeature_v2: id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
source-git-commit: b45a83f480603ecd38cfcbdf31ccc639f617f592
workflow-type: tm+mt
source-wordcount: 917
ht-degree: 13%

---

# 충성도 문제 시작 {#get-started-loyalty-challenges}

## 개요 {#overview}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_inventory"
>title="충성도 챌린지"
>abstract="충성도 챌린지를 사용하면 고객 행동을 유도하고 브랜드 관계를 심화하는 매력적이고 게임화된 충성도 프로그램을 만들 수 있습니다. 구매 및 리뷰 작성부터 소셜 미디어 참여 및 친구 추천에 이르기까지 특정 액션에 대해 고객에게 보상해 주는 챌린지를 작성하십시오."

>[!AVAILABILITY]
>
>* Journey Optimizer 로열티는 현재 Healthcare Shield 및 Privacy and Security Shield 고객은 사용할 수 없습니다. Healthcare Shield 및 Privacy and Security Shield 고객의 가용성은 향후 기능 준비 시 업데이트됩니다.

충성도 챌린지를 사용하면 고객 행동을 유도하고 브랜드 관계를 심화하는 매력적이고 게임화된 충성도 프로그램을 만들 수 있습니다. 구매 및 리뷰 작성부터 소셜 미디어 참여 및 친구 추천에 이르기까지 특정 액션에 대해 고객에게 보상해 주는 챌린지를 작성하십시오.

충성도 문제를 통해 다음과 같은 작업을 수행할 수 있습니다.

* **유연한 과제 유형 디자인**: 비즈니스 목표에 맞게 표준, 연속 또는 순차적 과제 만들기
* **전략적으로 보상 구성**: 작업 마일스톤 또는 전체 완료 시 포인트를 전달하여 참여 유지
* **경험 개인화**: 콘텐츠 카드 및 다중 채널 메시지를 사용하여 몰입형 브랜드 경험을 만듭니다
* **원활하게 통합**: 기존 충성도 공급자와 연결하고 Experience Platform 데이터 활용
* **자동으로 추적**: 사용자 지정 개발 없이 자동 생성된 여정을 통해 고객 진행 상황을 모니터링합니다.
* **성과 측정**: 기본 제공 보고 대시보드를 사용하여 프로그램 KPI, 과제 결과 및 작업 수준 지표를 추적합니다.

![](assets/challenges-gs.png)

다음과 같은 유형의 과제 경험을 만들 수 있습니다.

* **표준 과제**: 고객은 순서에 관계없이 지정된 수의 작업을 완료합니다. 유연성과 여러 경로를 완성하려면 이 유형을 사용하십시오.\
  *예: &quot;Summer Wellness Challenge&quot; - 5가지 작업 중 3가지 완료: 건강 제품 구입, 소셜 미디어 공유, 친구 추천, 리뷰 작성 또는 가상 이벤트 참석*

* **연속 문제**: 고객은 동일한 작업을 여러 번 연속적으로 완료합니다. 이 유형을 사용하여 시간이 지남에 따라 일관되고 반복되는 동작을 장려합니다.\
  *예: &quot;커피 애호가 주간&quot; - 7일 연속으로 커피 제품을 구입하여 무료 음료 보상을 받으세요*

* **순차적인 문제**: 고객은 정의된 순서로 작업을 완료합니다. 이 유형을 사용하여 특정 여정 또는 온보딩 프로세스를 안내합니다.\
  *예: &quot;새 구성원 여정&quot; - 전자 메일→ 등록하여 첫 번째 구매 → 제품 리뷰 작성 → 친구 참조(이 순서로 완료)*

* **고유한 데이터 문제 해결**(제한된 가용성): 충성도 문제 데이터 통합에서 문제 프레임워크(작업 및 보상)를 취합합니다. 다른 모든 과제 유형에 대해 하듯이 설정, 콘텐츠 및 메시징을 구성합니다.

## 작동 방식 {#how-it-works}

충성도 과제 사용에는 일반적으로 관리자 및 실무자 역할 간에 공유되는 세 가지 광범위한 단계(설정, 실행 및 측정)가 포함됩니다.

**1. 프로그램 설정** *(관리자)*

문제를 작성하기 전에 관리자는 보상 제공업체, 고객 작업을 작업 완료, 제품 인벤토리 및 제외 목록에 매핑하는 이벤트 정의 등 프로그램 기반을 구성합니다. [충성도 문제를 구성하는 방법을 알아보세요](loyalty-admin.md).

**2. 작성 및 실행 문제** *(실무자)*

마케터는 유형(표준, 연속, 순차적 또는 고유한 데이터 가져오기)을 선택하고, 설정(대상, 일정, 규칙)을 구성하고, 작업 및 보상을 정의하여 문제를 만듭니다. 선택적으로 **콘텐츠 카드** 또는 **코드 기반 경험**&#x200B;을 사용하여 구성원 대면 인터페이스에 문제를 표시하고 문제 라이프사이클에서 중요한 순간에 대한 채널 알림을 설정할 수 있습니다. 구성이 완료되면 과제를 게시하고, 자동으로 빌드된 여정을 생성한 다음 게시하여 과제를 라이브로 만듭니다. [문제를 만드는 방법을 알아보세요](create-challenges.md).

**3. 성능 모니터링** *(실무자/분석가)*

문제가 실행되면 기본 제공 보고 대시보드가 대상 funnel 성과, 작업 완료율, 보상 발행 및 매출에 미치는 영향과 같은 문제 수준 지표를 제공합니다. AI 기반의 인사이트 엔진은 프로그램 성능을 최적화하는 데 도움이 되는 상황별 권장 사항도 제공합니다. [충성도 보고에 대해 알아봅니다](loyalty-reporting.md).

## 사전 요구 사항 {#prerequisites}

충성도 문제를 사용하기 전에 다음을 확인하십시오.

+++필요한 권한

충성도 문제를 사용하려면 충성도 역할에 할당되어야 합니다. 기본 역할은 Prod 샌드박스에서 관리자, 실무자 및 분석가가 사용할 수 있습니다. 비프로덕션 샌드박스의 경우 관리자는 필요한 충성도 권한이 있는 사용자 정의 역할을 만들어야 합니다.

기능에 액세스할 수 없거나 추가 권한이 필요한 경우 관리자에게 문의하십시오. [충성도 문제 권한을 구성하는 방법을 알아보세요](loyalty-permissions.md).

+++

+++고객 충성도 프로그램 구성(관리자)

관리자는 **[!UICONTROL 충성도 관리자]** 메뉴에서 보상 공급자, 이벤트 정의, 제품 인벤토리, 제외 및 전역 설정을 구성합니다. 도전만 생성하는 마케터는 이 메뉴에 액세스할 필요가 없습니다. [충성도 문제를 구성하는 방법에 대해 알아보세요](loyalty-admin.md)

왼쪽 탐색에 **[!UICONTROL 충성도 관리자]** 메뉴가 표시되지 않는 경우 관리자에게 문의하십시오.

+++

+++타깃 대상자

과제를 만들기 전에 필요한 타겟 대상이 Adobe Experience Platform에 있는지 확인하십시오. 과제 구성 중에 참여할 수 있는 고객을 정의하는 대상을 선택합니다. [대상자를 사용하여 작업하는 방법을 알아봅니다](../audience/about-audiences.md).

+++

## 더 자세히 알아보기 {#lets-dive-deeper}

이제 충성도 문제가 무엇인지, 어떻게 작동하는지 알고 있으므로 세부 사항을 자세히 살펴볼 차례입니다. 다음 항목을 탐색하여 인터페이스에 액세스하고, 첫 번째 과제를 만들고, 고객이 완료할 작업을 정의합니다.

<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <a href="access-loyalty-challenges.md">
      <img alt="액세스" src="assets/do-not-localize/icon-access.png" width="200"/>
    </a>
    <div>
    <a href="access-loyalty-challenges.md"><strong>챌린지 및 작업 액세스 및 관리</strong></a>
    </div>
    <p>
    <em>인벤토리에 액세스하고 문제 및 작업을 관리하는 방법을 알아봅니다.</em>
    </p>
  </td>
  <td>
    <a href="create-challenges.md">
      <img alt="만들기" src="assets/do-not-localize/icon-challenge.png" width="200"/>
    </a>
    <div>
    <a href="create-challenges.md"><strong>챌린지 만들기</strong></a>
    </div>
    <p>
    <em>첫 번째 충성도 과제를 만들고 구성하는 방법에 대해 알아봅니다.</em>
    </p>
  </td>
  <td>
    <a href="create-tasks.md">
      <img alt="작업" src="assets/do-not-localize/icon-task.png" width="200"/>
    </a>
    <div>
    <a href="create-tasks.md"><strong>작업 만들기</strong></a>
    </div>
    <p>
    <em>고객이 어려움에 대해 완료하는 작업을 정의하는 방법을 알아보세요</em>
    </p>
  </td>
  <td>
    <a href="loyalty-reporting.md">
      <img alt="보고서" src="assets/do-not-localize/icon-reporting.png" width="200"/>
    </a>
    <div>
    <a href="loyalty-reporting.md"><strong>성능 모니터링</strong></a>
    </div>
    <p>
    <em>기본 제공 대시보드를 사용하여 프로그램 KPI, 과제 결과 및 작업 지표 추적</em>
    </p>
  </td>
  <!--
    <a href="loyalty-admin.md"><strong>Configure the loyalty program</strong></a>
  <td>
    <a href="loyalty-admin.md">
    <em>Set up reward providers, event definitions, and org settings for fulfillment</em>
    </a>
    <div>
-->
    <a href="loyalty-admin.md"><strong>충성도 챌린지 구성</strong></a>
    </div>
    <p>
    <em>보상 공급자, 이벤트 정의 및 조직 설정을 설정합니다</em>
    </p>
  </td>
</tr>
</table>

## API 참조 {#api-reference}

충성도 문제를 프로그래밍 방식으로 관리하려면 [충성도 문제 API](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}를 사용하십시오. API를 사용하면 REST 끝점을 통해 과제 및 작업을 만들고, 업데이트하고, 관리할 수 있습니다.
