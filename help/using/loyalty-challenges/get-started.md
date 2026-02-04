---
solution: Journey Optimizer
product: journey optimizer
title: 충성도 문제 시작
description: 매력적인 충성도 프로그램을 제작하기 위해 Adobe Journey Optimizer에서 충성도 문제를 만들고 관리하는 방법을 알아봅니다.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="비공개 베타" type="Informative"
source-git-commit: e98fe328b5a72a7091d48b5e2939a24e4ad6954c
workflow-type: tm+mt
source-wordcount: '759'
ht-degree: 2%

---


# 충성도 문제 시작 {#get-started-loyalty-challenges}

>[!BEGINSHADEBOX]

**충성도 과제 설명서:**

* **충성도 문제 시작** ◀︎**현재 상태** - 개요, 워크플로, 사전 요구 사항
* [충성도 문제 액세스](access-loyalty-challenges.md) - 인벤토리 및 필터링
* [과제 만들기](create-challenges.md) - 과제 빌드 및 구성
* [문제 관리](manage-challenges.md) - 편집, 모니터링, 최적화

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenges_overview"
>title="충성도 문제 정보"
>abstract="충성도 문제를 사용하면 고객이 특정 작업을 완료하고 보상을 획득하도록 유도하는 개인화된 참여 오퍼를 만들 수 있습니다."

>[!AVAILABILITY]
>
>이 기능은 현재 **개인 베타**&#x200B;에 있으며 사용자의 환경에서는 사용할 수 없습니다. 액세스 권한을 얻으려면 Adobe 담당자에게 문의하십시오.

## 개요 {#overview}

충성도 과제는 작업과 이정표 정의에서 채널 전반에 걸쳐 콘텐츠 전달 및 성능 추적에 이르기까지 충성도 프로그램을 규모에 맞게 제작할 수 있는 완벽한 솔루션을 제공합니다. 외부 충성도 관리 시스템과의 통합을 유지하면서 세 가지 유형의 과제 여정을 만들고, 보상을 구성하고, 주요 라이프사이클 단계에서 다중 채널 알림을 보내고, 자동으로 생성된 경험을 통해 성능을 모니터링할 수 있습니다.

## 주요 기능 {#key-capabilities}

충성도 문제를 사용하여 다음을 수행할 수 있습니다.

* **세 가지 유형의 문제 만들기**:
   * **표준**: 고객은 보상을 얻기 위해 임의 순서로 임의 개수의 작업을 완료합니다
   * **연속**: 고객은 동일한 작업을 여러 번 연속적으로 완료합니다
   * **순차적**: 고객은 특정 순서로 작업을 완료합니다

* **과제 콘텐츠 디자인**: Journey Optimizer 콘텐츠 카드를 사용하여 고객 장치에서 과제를 시각적으로 표현합니다. 콘텐츠 카드에는 과제 정보, 진행 상황 및 보상이 표시됩니다.

* **작업 요구 사항 설정**: 다음과 같은 보상을 얻기 위해 고객이 수행해야 하는 작업을 정의합니다.
   * 작업 유형(구매, 지출 금액, 방문, 참여, 사용자 정의 이벤트)
   * 수량 요구 사항
   * SKU, 카테고리 또는 속성을 사용한 제품 포함/제외
   * 사용자 지정 속성 및 조건

* **보상 구성**: 고객이 작업 완료 시(점진적 보상) 또는 전체 도전 완료 후(최종 보상) 적립하는 보상을 정의합니다.

* **다중 채널 알림 보내기**: 주요 단계에서 여러 채널(인앱, 이메일, 푸시)에 메시지를 전달합니다.
   * **시작**: 도전이 시작될 때
   * **진행 중**: 고객이 잠시 지나간 시간
   * **완료**: 고객이 과제를 마치면

* **성과 추적**: 자동으로 생성된 여정을 모니터링하고 기본 제공 보고서를 통해 과제 성과를 검토합니다.

## 작동 방식 {#how-it-works}

충성도 문제를 만들고 실행하는 것은 다음 워크플로를 따릅니다.

1. **데이터 수집 설정** - 고객 작업 및 진행 상황을 추적하는 고객 충성도 이벤트 데이터를 수집하도록 Experience Platform 소스 커넥터(예: Capillary)를 구성합니다.

2. **챌린지 만들기** - 이름, 유형(표준, 연속 또는 순차적), 대상 및 날짜 범위를 포함한 기본 챌린지 속성을 정의합니다.

3. **작업 추가** - 작업 유형(구매, 지출, 방문 등), 수량, 제품 필터 및 보상을 포함하여 고객이 완료해야 하는 특정 작업을 정의합니다.

4. **콘텐츠 카드 디자인** - 고객 장치에 표시되는 Journey Optimizer 콘텐츠 카드를 사용하여 도전의 시각적 표현을 만듭니다.

5. **메시지 구성**(선택 사항) - 시작, 진행 중 및 완료와 같은 주요 단계에 대해 멀티채널 메시지(인앱, 이메일, 푸시)를 설정합니다.

6. **검토 및 게시** - 테스트 프로필로 문제를 테스트한 다음 게시하여 대상 대상자가 사용할 수 있도록 합니다.

7. **자동 생성된 여정** - 게시하면 Journey Optimizer에서 자동으로 콘텐츠 카드 게재 및 메시지를 조정하는 여정을 만듭니다.

8. **여정 활성화** - 자동 생성된 여정은 챌린지 시작 날짜에 활성화되고 모든 고객 상호 작용을 관리합니다.

9. **성능 모니터링** - 기본 제공 보고서 및 여정 캔버스를 통해 기여도, 완료율, 보상 배포 및 메시지 참여를 추적합니다.

>[!NOTE]
>
>자동 생성된 여정은 여정 인벤토리에 표시되며 필요한 경우 사용자 정의할 수 있습니다. 그러나 여정에 직접 적용한 변경 사항은 과제 구성에 다시 동기화되지 않습니다.

## 전제 조건 {#prerequisites}

충성도 문제를 사용하기 전에 다음을 확인하십시오.

### 데이터 수집 설정 {#data-ingestion}

충성도 문제는 Experience Platform 소스 커넥터를 통해 수집된 데이터를 사용하여 고객 진행 상황과 작업 완료를 추적합니다.

1. **지원되는 소스 커넥터를 구성하십시오**: 현재 Capillary 커넥터는 일반적으로 사용할 수 있습니다. 추가 커넥터가 예정되어 있습니다.

2. **데이터 수집 유효성 검사**: 충성도 이벤트 및 고객 데이터가 Experience Platform으로 유입되어 Journey Optimizer에서 사용할 수 있는지 확인하십시오.

자세한 지침은 다음을 참조하십시오.

* [Experience Platform 소스 설명서](https://experienceleague.adobe.com/en/docs/experience-platform/sources/home)
* [Journey Optimizer에서 소스 커넥터 구성](../start/get-started-sources.md)

### 필요한 권한 {#required-permissions}

충성도 문제를 사용하려면 Journey Optimizer에서 적절한 권한이 필요합니다. 기능에 액세스할 수 없는 경우 관리자에게 문의하십시오.

### 타깃 대상자 {#target-audiences}

문제를 제기하기 전에 Experience Platform에서 타겟 대상을 만드십시오. 기존 대상을 선택할 수 있지만 충성도 문제 UI에서 새 대상을 만들 수는 없습니다.

## 중요한 제한 사항 {#limitations}

* **원장 시스템 없음**: 충성도 문제에서 통화 가치 또는 포인트 잔액을 추적하지 않습니다. 고객이 도전을 완료하고 보상을 획득하면 Journey Optimizer은 외부 충성도 관리 시스템을 호출하여 포인트 할당을 처리합니다.

* **대상 선택만**: 기존 대상을 선택할 수 있지만 충성도 문제 UI에서 새 대상을 만들 수는 없습니다.

## 다음 단계 {#next-steps}

<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <a href="access-loyalty-challenges.md">
    <!--<img alt="Access" src="../assets/do-not-localize/learn-more-button.svg">-->
    </a>
    <div>
    <a href="access-loyalty-challenges.md"><strong>충성도 문제 액세스</strong></a>
    </div>
    <p>
    <em>인벤토리 및 필터링 문제 액세스 방법 알아보기</em>
    <p>
  </td>
  <td>
    <a href="create-challenges.md">
      <!--<img alt="Create" src="../assets/do-not-localize/start-button.svg">-->
    </a>
    <div>
    <a href="create-challenges.md"><strong>문제 만들기</strong></a>
    </div>
    <p>
    <em>첫 번째 충성도 과제 구축 및 구성</em>
    <p>
  </td>
  <td>
    <a href="manage-challenges.md">
    <!--<img alt="Manage" src="../assets/do-not-localize/monitor-button.svg">-->
    </a>
    <div>
    <a href="manage-challenges.md"><strong>문제 관리</strong></a>
    </div>
    <p>
    <em>문제 편집, 모니터링 및 최적화</em>
    <p>
  </td>
</tr>
</table>
