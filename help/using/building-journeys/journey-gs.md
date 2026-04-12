---
solution: Journey Optimizer
product: journey optimizer
title: 첫 여정 만들기
description: ' [!DNL Adobe Journey Optimizer]을(를) 사용하여 첫 번째 여정을 빌드하는 주요 단계'
feature: Journeys, Get Started
topic: Content Management
role: User
level: Intermediate
keywords: 여정, 첫 번째, 시작, 빠른 시작, 대상, 이벤트, 작업
exl-id: d940191e-8f37-4956-8482-d2df0c4274aa
version: Journey Orchestration
source-git-commit: e7586f50e9f806b7dccb6d88998c43a89feb392b
workflow-type: tm+mt
source-wordcount: '1215'
ht-degree: 10%

---

# 첫 여정 만들기 {#jo-quick-start}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card2"
>title="여정 만들기"
>abstract="**[!DNL Adobe Journey Optimizer]**&#x200B;를 통해 이벤트 또는 데이터 소스에 저장된 상황별 데이터를 활용하여 실시간 오케스트레이션 사용 사례를 빌드할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_journey_create"
>title="여정"
>abstract="고객 여정 설계를 통해 개인화된 상황별 경험을 제공할 수 있습니다. Journey Optimizer를 사용하면 이벤트 또는 데이터 소스에 저장된 상황별 데이터를 활용하여 실시간 오케스트레이션 사용 사례를 빌드할 수 있습니다. **개요** 탭에는 여정과 관련된 주요 지표가 포함된 대시보드가 &#x200B;&#x200B;표시됩니다. **찾아보기** 탭에는 기존 여정의 목록이 표시됩니다."

[!DNL Adobe Journey Optimizer]에는 마케터가 마케팅 활동과 일대일 고객 참여를 조화롭게 조정할 수 있는 옴니채널 오케스트레이션 캔버스가 포함되어 있습니다. 사용자 인터페이스를 사용하면 팔레트에서 캔버스로 활동을 쉽게 끌어다 놓아 여정을 빌드할 수 있습니다. 여정 사용자 인터페이스는 [이 페이지](journey-ui.md)에 자세히 설명되어 있습니다.

![여정 캔버스 샘플](assets/journey38.png)

여정을 만드는 주요 단계는 이 페이지에 자세히 설명되어 있습니다. 다음과 같이 간소화됩니다.

![여정 만들기 단계: 만들기, 디자인, 테스트 및 게시](assets/journey-creation-process.png)

이 안내서에서는 다음 작업을 수행합니다.

* 여정 진입점 정의 — 대상 세그먼트 또는 실시간 이벤트
* 채널 간에 이메일, 푸시, SMS, 인앱, 웹, 코드 기반 경험, 콘텐츠 카드 등의 메시지 작업을 추가합니다. [지원되는 채널 보기](journey-action.md)
* 활성화하기 전에 테스트 프로필로 여정 테스트
* 여정 게시 및 성능 모니터링

여러 단계로 구성된 고객 여정을 구축하여 채널 간에 실시간으로 상호 작용, 오퍼 및 메시지를 전송할 수 있습니다. 이 접근 방식은 고객이 자신의 행동과 관련 비즈니스 신호를 기반으로 최적의 순간에 참여할 수 있도록 합니다.

<!--
>[!TIP]
>
>Not sure whether to use a journey or a campaign? [Learn how to choose the right approach](../start/journeys-vs-campaigns.md).
-->

## 시작하기 전에 {#prerequisites}

빌드하기 전에 구성해야 할 사항은 여정이 트리거되는 방식에 따라 다릅니다. 대부분의 여정은 다음 두 진입점 중 하나에서 시작됩니다.

* **대상 기반 항목** — 예약된 시간에 정의된 프로필 집합에 대해 여정이 실행됩니다. 여정을 빌드하기 전에 Adobe Experience Platform에서 [대상자를 만듭니다](../audience/about-audiences.md). Journey Optimizer을 처음 사용하는 경우 권장되는 시작 지점입니다.

* **이벤트 기반 항목** — 여정은 개인이 구매 또는 등록과 같은 작업을 수행할 때 실시간으로 트리거됩니다. [이벤트를 구성](../event/about-events.md)하여 트리거와 전달하는 데이터를 정의합니다.

다음 요소는 선택 사항이지만 사용 사례에 따라 필요할 수 있습니다.

* **데이터 원본** — 외부 시스템의 데이터로 여정 조건 또는 개인화를 보강하려면 [데이터 원본](../datasource/about-data-sources.md)을 설정하십시오.

* **사용자 지정 작업** — 기본 제공 채널이 아닌 서드파티 시스템을 통해 메시지를 전달하는 경우 [사용자 지정 작업](../action/action.md)을 구성하십시오.

>[!NOTE]
>
>* 기술 설정(이벤트, 데이터 소스 및 작업)을 담당하는 데이터 엔지니어인 경우 [이 섹션](../configuration/about-data-sources-events-actions.md)을 참조하세요.
>
>* 여정 보호 기능 및 제한 사항에 대해서는 [이 페이지](../start/guardrails.md)에 자세히 설명되어 있습니다.

## 여정 만들기 {#jo-build}

여러 단계 여정을 만들려면 다음 단계를 수행합니다.

1. 여정 관리 메뉴 섹션에서 **[!UICONTROL 여정]**&#x200B;을(를) 클릭합니다.

1. 새 여정을 만들려면 **[!UICONTROL 여정 만들기]** 단추를 클릭하십시오.

1. 여정의 구성 창을 편집하여 여정 이름을 정의하고 속성을 설정합니다. [이 여정](journey-properties.md)에서 페이지의 속성을 설정하는 방법을 알아보세요.

   >[!TIP]
   >
   >**어떤 여정 유형을 선택해야 합니까?** Journey Optimizer을 처음 사용하는 경우 **[!UICONTROL 대상 읽기]** 활동을 사용하여 대상 기반 여정으로 시작하십시오. 이전 이벤트 구성이 필요하지 않으며 캔버스에 익숙해지는 가장 쉬운 방법입니다. 구매 또는 양식 제출에 반응하는 등 이벤트가 트리거되는 실시간 경험의 경우, 먼저 이벤트를 구성하고 이벤트 기반 항목을 사용합니다. 더 깊이 갈 준비가 되셨습니까? [모든 여정 유형과 해당 시작 규칙을 살펴봅니다](entry-management.md#types-of-journeys).

   설정 및 구성 옵션이 있는 ![여정 속성 패널](assets/jo-properties.png)

그런 다음 여정 디자인을 시작할 수 있습니다.

## 여정 디자인 {#jo-design}

여정 디자이너를 사용하면 직관적인 드래그 앤 드롭 인터페이스를 사용하여 여러 단계의 여정을 작성할 수 있습니다. 왼쪽 팔레트의 활동은 **이벤트**, **오케스트레이션** 및 **작업**&#x200B;의 세 가지 범주로 구성됩니다. 캔버스 및 해당 컨트롤에 대한 전체 개요는 [이 페이지](using-the-journey-designer.md)를 참조하세요.

![활동 팔레트 및 캔버스가 있는 여정 디자이너 인터페이스](assets/journey38.png)

다음 단계에 따라 여정을 디자인합니다.

1. **진입점 추가** — 이벤트 또는 **[!UICONTROL 대상자 읽기]** 활동을 팔레트에서 캔버스로 드래그합니다. 이렇게 하면 프로필이 실시간으로(이벤트 기반) 개별적으로 또는 정의된 대상(대상 기반)에서 한 번에 하나씩 여정에 들어가는 방식이 정의됩니다.

   ![대상 대상을 선택하기 위한 대상 활동 구성 읽기](assets/read-segment.png)

1. **메시지 작업 추가** — 팔레트의 **[!UICONTROL 작업]** 섹션에서 채널 작업을 캔버스로 드래그하여 여정을 통해 흐르는 프로필에 메시지를 보냅니다. 작업은 이메일, 푸시 알림, SMS 등에 사용할 수 있습니다.

1. **오케스트레이션 활동 추가** — **[!UICONTROL 조건]** 활동을 사용하여 여정 특성 또는 동작을 기준으로 프로필을 여러 경로로 분기합니다. **[!UICONTROL 대기]** 활동을 사용하여 단계 사이에 시간 지연을 도입할 수 있습니다.

>[!TIP]
>
>여러 단계 또는 터치포인트가 많은 여정의 경우 엔드투엔드 흐름을 **[!UICONTROL Jump]** 활동과 연결된 더 작은 하위 여정으로 나누는 것이 좋습니다. 이렇게 하면 복잡성이 줄어들고 각 하위 여정을 독립적으로 테스트하기 쉬워집니다. [디자인 전략: 바이트 크기 하위 여정](jump.md#jump-strategy)에서 자세히 알아보세요.

## 여정 테스트 {#jo-test}

여정을 빌드했으면 게시하기 전에 테스트합니다. Journey Optimizer은 여정을 따라 이동하면서 테스트 프로필을 볼 수 있는 방법으로 **테스트 모드**&#x200B;를 제공하여 활성화 전에 잠재적인 오류를 감지합니다. 빠른 테스트를 실행하면 여정이 올바르게 작동하여 안심하고 게시할 수 있습니다. 이 섹션[에서 여정 &#x200B;](testing-the-journey.md)을(를) 테스트하는 방법을 알아보세요.

**시험 실행**&#x200B;에서도 여정을 실행할 수 있습니다. 여정 시험 실행은 Adobe Journey Optimizer의 특별한 여정 게시 모드로, 이를 통해 여정 실무자가 실제 고객과 연락하거나 프로필 정보를 업데이트하지 않고도 실제 프로덕션 데이터를 사용하여 여정을 테스트할 수 있습니다. 이 기능은 여정 제공자가 라이브로 게시하기 전에 여정 디자인 및 대상 타깃팅에 대한 자신감을 갖도록 도와줍니다. 이 섹션[에서 여정을 시험 실행 모드 &#x200B;](journey-dry-run.md)에 게시하는 방법을 알아봅니다.

## 여정 게시 {#jo-pub}

여정을 활성화하려면 게시를 하고 새 프로필에서 입력할 수 있도록 해야 합니다. 여정을 게시하기 전에 유효하고 오류가 없는지 확인하십시오. 오류가 있는 여정은 게시할 수 없습니다. 이 [섹션](publish-journey.md)에서 여정 게시에 대해 자세히 알아보세요.

![대상, 조건 및 동작이 포함된 여정 흐름 완료](assets/jo-journeyuc2_32bis.png)

게시되면 전용 보고 도구를 사용하여 여정을 모니터링하여 여정의 효과를 측정할 수 있습니다.

![성능 지표 및 통계를 보여 주는 여정 분석 보고서](assets/jo-dynamic_report_journey_12.png)

이 [섹션](../reports/live-report.md)에서 여정 보고서에 대해 자세히 알아보세요.

## 일반적인 사용 사례 {#use-cases}

어디서부터 시작할지 모르겠습니까? 다음은 여정이 가장 많은 가치를 제공하는 세 가지 일반적인 시나리오입니다.

<table style="table-layout:fixed">
  <tr style="border: 0;">
    <td>
      <a href="https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/tutorials/use-cases/customer-onboarding" target="_blank">
        <img src="../assets/do-not-localize/icon-quick-start.svg" width="35px">
      </a>
      <div><strong>환영 시리즈</strong><br/>신규 사용자를 등록하고 제품 또는 서비스를 안내하는 일련의 메시지를 자동으로 온보딩합니다.</div>
    </td>
    <td>
      <a href="https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart" target="_blank">
        <img src="../assets/do-not-localize/icon-campaign.svg" width="35px">
      </a>
      <div><strong>장바구니 포기</strong><br/>구매가 완료되지 않은 상태에서 나간 고객에게 적절한 시기에 개인화된 콘텐츠로 미리 알림을 보내 다시 참여시키십시오.</div>
    </td>
    <td>
      <a href="jo-use-cases.md">
        <img src="../assets/do-not-localize/icon-content.svg" width="35px">
      </a>
      <div><strong>다시 참여</strong><br/>마지막으로 알려진 동작을 기준으로 타깃팅된 오퍼 또는 업데이트를 사용하여 비활성 사용자를 다시 이기십시오.</div>
    </td>
  </tr>
  <tr style="border: 0;">
    <td align="center"><a href="https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/tutorials/use-cases/customer-onboarding" target="_blank"><img src="../assets/do-not-localize/learn-more-button.svg"></a></td>
    <td align="center"><a href="https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart" target="_blank"><img src="../assets/do-not-localize/learn-more-button.svg"></a></td>
    <td align="center"><a href="jo-use-cases.md"><img src="../assets/do-not-localize/learn-more-button.svg"></a></td>
  </tr>
</table>

## 추가 리소스

* **[여정 유형 및 프로필 항목](entry-management.md)** - 모든 여정 유형(단일 이벤트, 비즈니스 이벤트, 대상자 읽기, 대상자 자격)과 프로필이 여정을 입력, 재입력 및 통과하는 방식을 이해합니다.
* **[여정 디자이너 개요](using-the-journey-designer.md)** - 고객 여정을 디자인하고 오케스트레이션하기 위한 여정 캔버스 인터페이스를 기본으로 제공합니다.
* **[여정 활동](about-journey-activities.md)** - 이벤트, 작업 및 오케스트레이션 구성 요소를 포함하여 사용 가능한 모든 활동을 살펴봅니다.
* **[여정 테스트](testing-the-journey.md)** - 프로덕션에 게시하기 전에 테스트 모드를 사용하여 여정을 테스트하는 방법에 대해 알아봅니다.
* **[여정 게시](publish-journey.md)** - 여정 게시 프로세스 및 실시간 여정 관리 방법을 이해합니다.
* **[여정 보고](report-journey.md)** - 자세한 지표와 통찰력을 통해 여정 성과를 추적하고 분석합니다.
* **[여정 문제 해결](troubleshooting.md)** - 일반적인 여정 문제와 디버깅에 대한 모범 사례에 대한 해결 방법을 찾아봅니다.
* **[여정 자습서](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/tutorials/journeys/introduction-to-building-a-journey){target="_blank"}** - 여정 작성 및 모범 사례에 대한 단계별 비디오 자습서를 살펴보십시오.

