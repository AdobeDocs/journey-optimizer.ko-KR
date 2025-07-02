---
solution: Journey Optimizer
product: journey optimizer
title: 여정 속성 정의
description: Adobe Journey Optimizer을 사용하여 여정 속성을 설정하는 방법 알아보기
feature: Journeys, Get Started
topic: Content Management
role: User
level: Intermediate
keywords: 여정, 구성, 속성
exl-id: 6c21371c-6cbc-4d39-8fe6-39f1b8b13280
source-git-commit: 7d5d27d9509dd80fece2e360d58437d26df7c4de
workflow-type: tm+mt
source-wordcount: '2392'
ht-degree: 17%

---

# 여정 속성 정의 {#jo-properties}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties"
>title="여정 속성"
>abstract="이 섹션은 여정 속성을 보여 줍니다. 기본적으로 읽기 전용 매개변수는 숨겨져 있습니다. 사용 가능한 설정은 여정 상태, 권한 및 제품 구성에 따라 다릅니다."

## 여정 속성 액세스 {#access-properties}

여정 속성은 오른쪽 레일에서 중앙 집중화됩니다. 이 섹션은 새 여정을 만들 때 기본적으로 표시됩니다. 기존 여정의 경우 여정 이름 옆에 있는 연필 아이콘을 클릭하여 엽니다.

이 섹션에서 여정 이름을 정의하고 설명을 추가한 다음 여정 전역 속성을 설정합니다.

다음과 같은 작업을 수행할 수 있습니다.

* Adobe Experience Platform 통합 태그를 여정에 할당하여 캠페인 목록에서 쉽게 분류하고 검색을 개선합니다. [태그 작업 방법 알아보기](../start/search-filter-categorize.md#tags)
* 여정 지표를 선택합니다. [여정 지표를 구성하고 추적하는 방법에 대해 알아보기](success-metrics.md)
* [입장 및 재입장](#entrance)을 관리합니다. 여정 등록 관리는 프로필 유형에 따라 다릅니다. 자세한 정보는 [이 페이지](entry-management.md)를 참조하세요.
* [데이터에 대한 액세스 관리](#manage-access)
* 여정 및 프로필 [시간대](#timezone) 선택
* 사용자 지정 [시작 및 종료 날짜 선택](#dates)
* 여정 활동에서 [시간 제한 기간](#timeout)을(를) 정의합니다(관리자 전용).
* [충돌 관리 도구](#conflict)를 사용하여 충돌을 모니터링하고 여정 우선 순위 지정

![](assets/new-journey-properties.png){width="80%"}{zoomable="yes"}

>[!NOTE]
>
>라이브 여정의 경우 이 화면에는 게시 날짜와 여정을 게시한 사용자의 이름만 표시됩니다.

**기술 세부 정보 복사** 옵션을 사용하면 지원 팀이 문제를 해결하는 데 사용할 수 있는 여정에 대한 기술 정보를 복사할 수 있습니다. `JourneyVersion UID`, `OrgID`, `orgName`, `sandboxName`, `lastDeployedBy`, `lastDeployedAt` 정보가 복사되었습니다.

특정 프로필의 여정과 관련된 기술 필드 및 [이 페이지에서](expression/journey-properties.md)을(를) 사용하는 방법에 대해 자세히 알아보세요.

## 입장 및 재입장 {#entrance}

프로필 시작 모드는 오른쪽 구성 창의 여정 수준에서 정의됩니다. 설정은 아래에 설명되어 있습니다.

여정 등록 관리는 프로필 유형에 따라 다릅니다. [이 페이지](entry-management.md)에서 프로필 시작 및 재시작 관리에 대해 자세히 알아보세요.

### 재진입 허용  {#allow-reentrance}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_entrance"
>title="재진입 허용"
>abstract="기본적으로 새 여정은 재진입을 허용합니다. 예를 들어 사용자가 상점에 입장할 때 일회성 선물을 제공하려 한다면 **재진입 허용** 옵션을 선택 해제하면 됩니다."
>additional-url="https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/orchestrate-journeys/manage-journey/entry-management" text="프로필 시작 관리"

기본적으로 새 여정은 재진입을 허용합니다. 예를 들어, 한 사람이 상점에 들어갈 때 일회성 선물을 제공하려는 경우 &quot;한 번&quot; 여정에 대해 **재입장 허용** 옵션의 선택을 취소할 수 있습니다.

### 재진입 대기 기간  {#reentrance-wait}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_re-entrance_wait"
>title="재진입 대기 기간"
>abstract="프로필이 단일 여정에서 다시 여정에 진입할 수 있도록 허용하기 전에 대기할 시간을 설정하십시오. 이렇게 하면 선택한 기간 동안 사용자가 여정에 재진입하는 것을 방지할 수 있습니다. 최대 기간은 90일입니다."
>additional-url="https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/orchestrate-journeys/manage-journey/entry-management" text="프로필 시작 관리"

**재입력 허용** 옵션이 활성화되면 **재입력 대기 기간** 필드가 표시됩니다. 이 필드에서는 단일 여정(이벤트 또는 대상자 선별로 시작)에서 프로필이 다시 여정에 들어오려면 기다려야 하는 시간을 정의할 수 있습니다. 이를 통해 동일한 이벤트에 대해 여정을 여러 번 트리거하는 오류를 방지할 수 있습니다. 이 필드는 기본적으로 5분으로 설정되어 있습니다. 최대 기간은 90일입니다.

## 액세스 관리 {#manage-access}

액세스 레이블에 따라 여정에 대한 액세스를 제한할 수 있습니다.

여정 지정 데이터 사용 레이블을 사용자에게 할당하려면 **[!UICONTROL 액세스 레이블 관리]** 아이콘을 클릭하고 하나 또는 여러 레이블을 선택합니다.

[OLAC(Object Level Access Control)에 대해 자세히 알아보기](../administration/object-based-access.md)

## 여정 및 프로필 시간대 {#timezone}

시간대는 여정 수준에서 정의됩니다. 고정 시간대를 입력하거나 Adobe Experience Platform 프로필을 사용하여 여정 시간대를 정의할 수 있습니다. Adobe Experience Platform 프로필에 시간대가 정의된 경우 여정에서 검색할 수 있습니다.

[시간대 관리에 대해 자세히 알아보기](../building-journeys/timezone-management.md)

## 시작 및 종료 일자 {#dates}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_start_date"
>title="시작 날짜"
>abstract="프로필이 여정 진입을 시작할 수 있는 날짜를 선택하십시오. 시작 일자를 설정하지 않으면 여정의 게시 일자가 기본으로 설정됩니다."

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_end_date"
>title="종료 날짜"
>abstract="여정이 종료되는 날짜를 설정하십시오. 활성화된 프로필은 이 날짜에 자동으로 여정에서 종료되며 새로 진입할 수 없습니다."

기본적으로 프로필은 게시되는 즉시 여정을 입력할 수 있으며 [전역 여정 시간 제한](#global_timeout)에 도달할 때까지 유지될 수 있습니다. 유일한 예외는 **되풀이 시 강제 재입력**&#x200B;이 활성화된 되풀이 대상 여정 읽기이며, 다음 발생의 시작 날짜에 끝납니다.

필요한 경우 사용자 지정 **시작 날짜** 및 **종료 날짜**&#x200B;를 정의할 수 있습니다. 이렇게 하면 프로필에서 특정 날짜에 여정을 입력하고 종료 날짜에 도달하면 자동으로 종료할 수 있습니다.

## 시간 초과 {#timeout}

### 여정 활동의 시간 초과 {#timeout_and_error}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_timeout"
>title="시간 초과 또는 오류"
>abstract="여정이 시간 초과로 간주되기 전에 액션을 수행하거나 조건을 평가하는 데 소요되는 시간을 지정합니다. 권장되는 값은 1~30초입니다."

작업 또는 조건 활동을 편집할 때 오류 또는 시간 초과가 발생하는 경우 대체 경로를 정의할 수 있습니다. 서드파티 시스템에 문의하는 활동 처리가 여정 속성의 **[!UICONTROL 시간 초과 또는 오류]** 필드에 정의된 시간 초과 기간을 초과하는 경우 잠재적인 대체 작업을 수행하도록 두 번째 경로가 선택됩니다.

권장되는 값은 1~30초입니다.

여정이 시간에 민감한 경우(예: 사람의 실시간 위치에 반응) 몇 초 이상 작업을 지연할 수 없으므로 매우 짧은 **[!UICONTROL 시간 초과 또는 오류]** 값을 정의하는 것이 좋습니다. 여정에서 시간에 덜 민감한 경우, 더 긴 값을 사용하여 유효한 응답을 보내기 위해 호출된 시스템에 더 많은 시간을 제공할 수 있습니다.

여정은 또한 아래에 설명된 대로 글로벌 시간 제한을 사용합니다.

### 전역 여정 시간 제한 {#global_timeout}

여정 활동에 사용된 [timeout](#timeout_and_error) 외에 글로벌 여정 시간 제한이 적용됩니다. 인터페이스에 표시되지 않으므로 변경할 수 없습니다.

이 전역 시간 제한은 입력한 후 **91일** 여정에서 개인 사용자의 진행률을 중지합니다. 이는 개인의 여정이 91일을 초과할 수 없음을 의미합니다. 이 시간 제한 기간이 지나면 개인의 데이터가 삭제됩니다. 시간 제한 기간이 끝날 때 여전히 여정에 유입되는 개인은 중지되며, 보고에서 고려되지 않습니다. 따라서 종료하는 것보다 더 많은 사람들이 여정에 들어가는 것을 볼 수 있습니다.

91일 여정 시간 제한으로 인해 여정 재입력이 허용되지 않으면 재입력 차단이 91일 이상 작동하도록 할 수 없습니다. 실제로 해당 여정에 입장한 후 91일이 지난 사람에 대한 정보를 모두 삭제하기 때문에 91일 이상 전에 입력한 사람을 알 수 없습니다.

개인은 91일 여정 시간 제한 전에 대기 기간을 완료할 수 있는 충분한 시간이 여정에 남아 있는 경우에만 대기 활동을 입력할 수 있습니다. [이 페이지](../building-journeys/wait-activity.md)를 참조하십시오.

#### TTL(Time-to-Live) 및 데이터 유지 FAQ {#timeout-faq}

2024년 6월 Adobe Journey Optimizer 릴리스부터 여정 전역 시간 제한이 30일에서 91일로 이동되었습니다. 영향은 아래 FAQ에 나열되어 있습니다.

단일 여정 **의 경우**
<table style="table-layout:auto">
  <tr style="border: 1;">
    <td>
      <p>TTL 확장이 롤아웃된 후 게시된 여정은 어떻게 됩니까?</p>
    </td>
    <td>
      <p>새 여정에 들어가는 프로필의 TTL은 91일로 자동 설정됩니다.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>TTL 확장 프로그램 시작 전에 게시된 여정을 입력하는 프로필은 어떻게 됩니까?</p>
    </td>
    <td>
      <p>프로필의 TTL은 여정이 처음 게시된 시간과 일치하는 30일(HIPAA의 경우 7일)입니다.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>TTL 확장을 시작할 때 이미 여정에 들어간 프로필은 어떻게 됩니까?</p>
    </td>
    <td>
      <p>프로필은 여정의 원래 게시 시간에 따라 30일(HIPAA의 경우 7일)의 TTL을 유지합니다.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>TTL 확장 프로그램 실행 후 다시 게시된 이전 여정 버전의 프로필은 어떻게 됩니까?</p>
    </td>
    <td>
      <p>프로필은 원래 여정 버전의 게시 시간에 맞추어 30일(HIPAA의 경우 7일)의 TTL을 유지 관리합니다.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>TTL 확장 기능 시작 후 다시 게시된 여정 버전을 입력하는 새 프로필은 어떻게 됩니까?</p>
    </td>
    <td>
      <p>프로필의 TTL은 91일로, 새로 다시 게시된 여정 버전의 TTL과 일치합니다.</p>
    </td>
  </tr>
</table>

**세그먼트 트리거 여정의 경우**

<table style="table-layout:auto">
  <tr style="border: 1;">
    <td>
      <p>TTL 확장 후 게시된 새 일회성 여정은 어떻게 됩니까?</p>
    </td>
    <td>
      <p>새 여정에 들어가는 프로필의 TTL은 91일로 자동 설정됩니다.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>TTL 확장 후 게시된 강제 재입력이 없는 새 반복 여정은 어떻게 됩니까?</p>
    </td>
    <td>
      <p>새 여정에 들어가는 프로필의 TTL은 91일로 자동 설정됩니다.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>TTL 확장 후 강제 재입력이 게시된 새 반복 여정은 어떻게 됩니까?</p>
    </td>
    <td>
      <p>새 여정에 들어가는 프로필의 TTL은 반복 기간과 동일합니다. 예를 들어 여정이 매일 실행되는 경우 TTL은 1일이 됩니다.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>TTL 확장 프로그램 시작 전에 게시된 여정을 입력하는 프로필은 어떻게 됩니까?</p>
    </td>
    <td>
      <p>프로필의 TTL은 원래 게시 시간과 일치하는 30일(HIPAA의 경우 7일)입니다. 강제 재입력이 있는 반복 여정의 경우 TTL은 반복 기간과 일치합니다.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>TTL 확장을 시작할 때 여정에서 실행되는 프로필은 어떻게 됩니까?</p>
    </td>
    <td>
      <p>프로필은 여정의 원래 게시 시간에 따라 30일(HIPAA의 경우 7일)의 TTL을 유지합니다. 강제 재입력이 있는 반복 여정의 경우 TTL은 반복 기간과 일치합니다.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>TTL 확장 프로그램 실행 후 다시 게시된 이전 여정 버전에서 실행 중인 프로필은 어떻게 됩니까?</p>
    </td>
    <td>
      <p>이 프로필은 원래 여정 버전의 게시 시간에 맞추어 30일(HIPPA의 경우 7일)의 TTL을 유지합니다. 강제 재입력이 있는 반복 여정의 경우 TTL은 반복 기간과 일치합니다.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>TTL 확장 기능 시작 후 다시 게시된 여정 버전을 입력하는 새 프로필은 어떻게 됩니까?</p>
    </td>
    <td>
      <p>프로필의 TTL은 91일로, 새로 다시 게시된 여정 버전의 TTL과 일치합니다. 강제 재입력이 있는 반복 여정의 경우 TTL은 반복 기간과 일치합니다.</p>
    </td>
  </tr>
</table>

## 병합 정책 {#merge-policies}

Adobe Journey Optimizer은 Adobe Experience Platform에서 프로필 데이터를 검색하는 동안 병합 정책을 사용합니다. 여정 유형에 따라 서로 다른 병합 정책이 사용됩니다.

* 대상자 읽기 또는 대상자 자격 여정: 대상자의 병합 정책이 사용됩니다
* 단일 이벤트 여정에서: 기본 병합 정책이 사용됩니다
* 비즈니스 이벤트 여정: 다음 대상 읽기 활동에서 타깃팅된 대상의 병합 정책이 사용됩니다

Adobe Journey Optimizer은 전체 여정에 사용된 병합 정책을 적용합니다. 따라서 한 여정에서 여러 대상을 사용하는 경우(예: [`inAudience`개의 함수](functions/functioninaudience.md)에서 사용) 여정에서 사용하는 병합 정책과 일치하지 않으면 오류가 발생하고 게시가 차단됩니다. 하지만 메시지 개인화에 일관되지 않은 대상이 사용되면 불일치에도 불구하고 경고가 발생하지 않습니다. 이러한 이유로, 메시지 개인화에 이 대상자를 사용할 때에는 대상자와 연결된 병합 정책을 확인하는 것이 좋습니다.

병합 정책에 대한 자세한 내용은 [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/ko/docs/experience-platform/profile/merge-policies/overview){target="_blank"}를 참조하세요.

>[!NOTE]
>
>대상 병합 정책이 업데이트되면 해당 대상을 참조하는 모든 활성 여정을 다시 게시(또는 복제)해야 합니다. 병합 정책을 변경하면 진행 중인 여정이 액세스할 수 없는 &#39;새로운&#39; 대상자가 효과적으로 생성되어 데이터 일관성이 보장됩니다.

## 종료 기준 {#exit-criteria}

>[!CONTEXTUALHELP]
>id="ajo_journey_exit_criterias"
>title="여정 종료 기준"
>abstract="이 섹션에는 종료 기준 옵션이 표시됩니다. 여정에 대해 하나 이상의 종료 기준 규칙을 만들 수 있습니다."

### 설명 {#exit-criteria-desc}

종료 기준을 추가하면 이벤트가 발생(예: 구매)하거나 프로필이 대상자 자격에 해당하는 즉시 해당 프로필의 여정을 종료합니다. 그러면 해당 사용자가 더 이상 해당 여정의 커뮤니케이션을 받지 않게 됩니다.

프로필이 더 이상 여정의 목적에 부합하지 않는 경우 여정에서 프로필을 제거할 수 있습니다. 목표 관리와 밀접하게 연관된 **전역 종료 기준**&#x200B;을 통해 이를 달성할 수 있습니다.

**샘플 사용 사례**

마케터에는 일련의 커뮤니케이션이 있는 프로모션 여정이 있습니다. 이러한 각 커뮤니케이션은 고객이 구매를 하도록 유도하는 데 목적이 있습니다. 구매가 이루어지는 즉시 고객은 일련의 메시지 중 나머지 메시지를 받지 않아야 합니다. 종료 기준을 정의하면 구매한 모든 프로필이 여정에서 제거됩니다.

### 구성 및 사용 {#exit-criteria-config}

종료 기준은 여정 수준에서 설정됩니다. 한 여정에 여러 종료 기준이 있을 수 있습니다. 여러 종료 기준을 설정한 경우 `OR` 논리를 사용하여 위에서 아래로 평가됩니다. 따라서 종료 기준 A와 종료 기준 B가 있으면 **OR** B로 평가됩니다. 기준은 여정의 모든 단계에서 평가됩니다.

종료 기준을 **만들기**&#x200B;하려면 다음 단계를 수행합니다.

1. 여정을 엽니다.

1. 여정 캔버스의 오른쪽 위 섹션에 있는 ![](assets/do-not-localize/Smock_UserCheckedOut_18_N.svg) **[!UICONTROL 종료 기준 표시]** 아이콘을 클릭합니다.

1. **[!UICONTROL 종료 기준 추가]**&#x200B;를 선택합니다.

1. **레이블**&#x200B;을(를) 입력하고 종료 기준이 **이벤트** 또는 **대상자**&#x200B;를 기반으로 하는지 선택합니다.

   * 예를 들어 앱 다운로드 또는 장바구니에 제품 추가와 같은 이벤트를 기반으로 한 종료 기준의 경우 단일 이벤트만 선택합니다.
   * 예를 들어 고객이 지난 24시간 동안 구매했는지 확인하는 대상과 같은 대상을 기반으로 한 종료 기준의 경우 대상을 선택합니다. 참고: 대상을 사용하여 종료 기준을 적용하려면 최대 10분이 걸릴 수 있습니다.

여러 종료 기준을 추가할 수 있습니다.

![](assets/exitcriteria-sample.png){width="40%" align="left"}

### 가드레일 및 제한 사항 {#exit-criteria-guardrails}

여정 종료 기준 기능에는 다음 보호 기능 및 제한 사항이 적용됩니다.

* 종료 기준은 초안 상태에서만 정의됩니다
* 이벤트와 이벤트 기반 종료 기준 간의 네임스페이스 일관성 여정

## 여정 일정 {#schedule}

**[!UICONTROL 일정]** 섹션은 **[!UICONTROL 대상자 읽기]** 활동이 캔버스에서 삭제된 경우에만 사용할 수 있습니다. 이를 통해 여정을 실행해야 하는 특정 날짜/시간 및 빈도를 정의할 수 있습니다. [대상자 읽기 여정을 예약하는 방법 알아보기](../building-journeys/read-audience.md)

## 충돌 관리 {#conflict}

여정 속성의 **[!UICONTROL 충돌 관리]** 섹션에서 충돌을 모니터링하고 여정의 우선 순위를 지정할 수 있습니다. 다음과 같은 작업을 수행할 수 있습니다.

* 최대 가용량 규칙에 따라 이 여정을 대상의 일부에 제외하려면 **규칙 집합**&#x200B;을 적용하세요. [규칙 세트 작업 방법 알아보기](../conflict-prioritization/rule-sets.md)

* 여정에 0에서 100 사이의 **우선 순위 점수**&#x200B;를 지정하십시오. 숫자가 높을수록 우선 순위가 높다는 뜻입니다. 여기에 삽입된 우선 순위 값은 이 여정에 포함된 모든 인바운드 액션(예: 인앱)에 상속됩니다. [우선 순위 점수를 사용하여 작업하는 방법을 알아봅니다](../conflict-prioritization/priority-scores.md)

  동일한 인바운드 채널 구성이 다른 캠페인이나 여정에 사용되는 경우, 우선 순위 점수가 가장 높은 인바운드 액션이 수신자에게 표시됩니다. 여러 여정이나 캠페인의 점수가 동일한 경우, 가장 최근에 수정된 요소가 선택됩니다.

* 다른 여정, 캠페인 또는 채널 구성과의 **충돌 보기**. 대상, 시작 및 종료 날짜, 채널 구성, 채널 또는 규칙 세트에 대한 겹침을 식별하려면 여기에서 잠재적인 충돌을 볼 수 있습니다. [여정에서 잠재적인 충돌을 식별하는 방법에 대해 알아봅니다](../conflict-prioritization/conflicts.md)
