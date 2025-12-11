---
solution: Journey Optimizer
product: journey optimizer
title: 여정 시작 및 종료 기준
description: 실제 사례 및 모범 사례를 통해 프로필이 여정에 들어오고 나가는 시기를 효과적으로 관리하는 방법을 알아봅니다
feature: Journeys, Profiles
role: User
level: Intermediate
keywords: 시작, 종료, 기준, 여정, 프로필, 재입력, 우수 사례
version: Journey Orchestration
source-git-commit: a60ea57ffed3fa9e11dc202f26889d05862604d9
workflow-type: tm+mt
source-wordcount: '1494'
ht-degree: 0%

---


# 여정 시작 및 종료 기준을 사용한 작업 {#entry-exit-criteria-guide}

Customer Experience Orchestration에서 적절한 시간에 적절한 메시지를 전달하려면 고객이 여정을 출입할 때를 정확하게 제어해야 합니다. 시작 및 종료 기준을 이해하고 적절히 구성하면 성공적인 캠페인과 놓친 기회 또는 메시지 피로도 간에 차이를 만들 수 있습니다.

이 안내서에서는 Adobe Journey Optimizer에서 여정 시작 및 종료 기준을 관리하기 위한 실용적인 지침, 실제 사례 및 모범 사례를 제공합니다.

## 시작 및 종료 기준이란 무엇입니까? {#what-are-criteria}

**시작 기준**&#x200B;은(는) [고객 프로필](../audience/get-started-profiles.md)이(가) 특정 여정을 입력할 수 있는 조건을 결정합니다. 프로필은 다음을 기준으로 입력할 수 있습니다.

* **[고객 동작](../event/about-events.md)** - 고객이 수행한 작업은 구매, 장바구니 포기 또는 모바일 앱 열기와 같은 여정 항목을 실시간으로 트리거합니다.

* **[프로필 특성](../audience/get-started-profiles.md)** - 고객 특성은 충성도 계층, 위치, 연령 또는 커뮤니케이션 환경 설정과 같이 프로필에 저장된 데이터를 기반으로 자격을 결정합니다.

* **[외부 이벤트](../event/about-creating-business.md)** - 낮은 재고 알림, 날씨 상태 또는 가격 변경과 같이 여러 고객에게 동시에 영향을 미치는 비즈니스 또는 환경 트리거입니다.

* **[대상 멤버십](../audience/about-audiences.md)** - 특정 대상 세그먼트에 속하면 고가치 고객, 비활성 사용자 또는 새 구독자와 같은 그룹에 대해 타깃팅된 여정을 사용할 수 있습니다.

**종료 기준**&#x200B;은(는) 프로필이 여정을 떠나거나 프로필에서 제거되는 시기와 방법을 정의합니다.

* **여정 완료** - 프로필이 모든 여정 경로의 [끝](end-journey.md)에 도달하면 자동으로 종료되어 디자인된 경험이 완료됩니다.

* **성공 지표 달성** - 프로필이 구매 또는 앱 다운로드와 같은 [여정 목표](success-metrics.md)를 완료하면 종료되며 불필요한 후속 커뮤니케이션이 필요하지 않습니다.

* **조건 기반** - 일정 기간 동안 활동이 없거나 프로필 특성이 변경되는 등 [특정 조건](condition-activity.md)이 충족되면 프로필이 종료됩니다.

* **이벤트 기반** - [구독 취소 또는 제품 반환과 같은 특정 이벤트가 발생하면](../event/about-events.md)프로필이 종료됩니다.

* **대상 자격 상실** - 프로필이 더 이상 [대상 기준](../audience/about-audiences.md)을 충족하지 않으면 종료되어 메시지의 관련성이 유지됩니다.

## 시작 및 종료 기준이 중요한 이유 {#why-they-matter}

진입 및 종료 기준을 올바르게 정의하면 다음과 같은 중요한 비즈니스 가치를 얻을 수 있습니다.

* **관련성**: 적절한 고객만 여정에 참여하여 최적의 시간에 가장 적절한 대상을 타기팅하여 참여도와 전환율을 높입니다.

* **효율성**: 고객이 관련 없는 여정에 머무르지 않도록 하여 불필요한 통신, 운영 비용 및 고객 불편을 줄입니다.

* **Personalization**: 실시간 데이터 및 동작을 기반으로 경험에 대한 동적 맞춤화를 활성화하여 보다 의미 있는 고객 상호 작용을 만듭니다.

* **규정 준수**: 브랜드 평판을 유지하면서 고객 선호도 및 규제 요구 사항을 준수하면서 빈도 제한을 관리하고 과도한 커뮤니케이션을 방지하는 데 도움이 됩니다.

## 여정 시작 및 종료의 실제 예 {#real-world-examples}

다음은 실제로 시작 및 종료 기준이 작동하는 방식을 보여 주는 일반적인 시나리오입니다.

**새 구독자를 위한 시작 캠페인**

브랜드, 제품 및 서비스에 대한 소개를 통해 신규 가입자에게 자동으로 안내하여 개인화된 첫인상을 만듭니다.

* **시작**: 프로필이 뉴스레터를 구독할 때 여정을 입력합니다.
* **종료**: 환영 전자 메일 시리즈를 완료한 프로필이 종료되거나 참가하지 않는 경우 설정된 시간 후에 프로필이 종료됩니다
* **혜택**: 신규 가입자가 반복 메시지를 피하면서 적시에 온보딩을 받도록 합니다.

**장바구니 복구를 중단함**

고객에게 놓고 간 항목을 상기시키고 구매를 완료하기 위한 인센티브를 제공하여 매출을 회수합니다.

* **시작**: 고객이 장바구니에 항목을 추가했지만 24시간 이내에 체크아웃을 완료하지 않으면 여정을 입력합니다
* **종료**: 구매가 완료될 때 또는 구매가 이루어지지 않은 경우 7일 후에 프로필이 종료됩니다
* **이점**: 관심이 없는 고객에게 스팸 메일을 보내지 않고 적시에 미리 알림으로 전환을 유도합니다.

**충성도 프로그램 참여**

브랜드 충성도를 강화하고 라이프타임 가치를 높이는 독점 혜택 및 개인화된 커뮤니케이션으로 가장 가치 있는 고객에게 보답하십시오.

* **시작**: 고객이 특정 충성도 포인트에 도달한 후 여정에 참여합니다.
* **종료**: 보상을 받은 후 또는 60일 동안 비활성 상태인 경우 프로필이 종료됩니다
* **이익**: 가치가 높은 고객의 개인화된 오퍼 참여를 유지하고 통신 피로를 방지합니다.

**제품 피드백 컬렉션**

게재 후 최적의 순간에 피드백을 요청하여 고객 만족도 및 제품 성능에 대한 인사이트를 수집합니다.

* **시작**: 고객이 제품 배달 확인 이벤트를 받은 후 여정을 입력합니다
* **종료**: 피드백이 제출되면 프로필이 종료되거나 응답이 없는 경우 10일 후에 프로필이 종료됩니다
* **혜택**: 지속적인 요청으로 성가신 고객 없이 중요한 피드백을 즉시 캡처합니다.

## 여정 입력 기준을 구성하는 방법 {#configure-entry}

>[!BEGINSHADEBOX]

**여기에서 항목 기준에 대해 알아야 할 모든 것을 알아보세요.**

* **[여정 기반 트리거](../event/about-events.md)**: &quot;프로필 만들기&quot;, &quot;트랜잭션 완료&quot; 또는 사용자 지정 이벤트와 같은 이벤트를 사용하여 이벤트를 시작합니다. [이벤트 구성](../event/about-creating.md)(**[!UICONTROL 관리]** > **[!UICONTROL 이벤트]**), [이벤트 스키마 및 필드](../event/experience-event-schema.md) 정의 후 **[!UICONTROL 여정 디자이너]**&#x200B;의 [이벤트](using-the-journey-designer.md) 팔레트에서 이벤트를 추가합니다.

* **[대상 기반 항목](read-audience.md)**: 특정 대상에 속하는 프로필에 대한 여정을 일회성 배치로 또는 되풀이하는 일정으로 타깃팅합니다. [대상자 만들기](../audience/creating-a-segment-definition.md)(**[!UICONTROL 대상자]**) 메뉴에서 **[!UICONTROL 대상자 읽기]** 활동을 추가한 다음 [일정을 구성](journey-properties.md#schedule).

* **[대상 자격 항목](audience-qualification-events.md)**: 프로필이 특정 대상에 대해 자격이 있거나 실시간으로 종료되는 경우 여정을 트리거합니다. [스트리밍 대상](../audience/about-audiences.md)을 정의하고 **[!UICONTROL 이벤트]** 팔레트에서 **[!UICONTROL 대상 자격]** 이벤트를 추가한 다음 트리거 유형을 선택하십시오.

* **[특성 필터](condition-activity.md)**: AND/OR 논리를 사용하여 이벤트 또는 대상을 프로필 특성 및 컨텍스트와 결합하여 항목 기준을 구체화합니다. [조건](conditions.md)을(를) 사용하여 [프로필 특성](../audience/get-started-profiles.md), 이벤트 또는 [외부 데이터](../datasource/about-data-sources.md)를 참조합니다.

* **[시간 창 및 예약](journey-properties.md#schedule)**: 여정을 적시에 적절한 상태로 유지하도록 임시 제한을 설정합니다. 대상자 읽기 활동에 대한 [일정을 구성](read-audience.md)하고, [대기 활동](wait-activity.md)을 사용하고, [시간 기반 조건](conditions.md)을 추가하여 타이밍을 제어하십시오.

>[!ENDSHADEBOX]

## 여정 종료 기준을 설정하는 방법 {#configure-exit}

>[!BEGINSHADEBOX]

**여기서 종료 기준에 대해 알아야 할 모든 것을 알아보세요.**

* **[여정 완료](end-journey.md)**: 프로필이 최종 여정 단계에 도달하면 자동으로 종료됩니다. **[!UICONTROL 종료]** 활동에 끝낼 여정 경로를 디자인합니다.

* **[성공 지표 달성](journey-properties.md#exit-criteria)**: 완료 시 성공 지표(예: 구매 또는 구독) 및 종료 프로필을 정의합니다. **[!UICONTROL 종료 기준 표시]** 아이콘을 클릭하고 **[!UICONTROL 종료 기준 추가]**&#x200B;를 선택한 다음 [이벤트](../event/about-events.md) 또는 [대상](../audience/about-audiences.md)을 종료 트리거로 선택합니다.

* **[비활성 시간 초과](wait-activity.md)**: 설정된 일정 내에 참여가 발생하지 않으면 프로필을 종료합니다. 마지막 참여 날짜를 확인하는 대상자와 함께 [종료 기준](journey-properties.md#exit-criteria)을 사용하고 정의된 기간이 있는 [대기 활동](wait-activity.md)을 설정하고 [조건](condition-activity.md)을 사용하여 활동을 확인하세요.

* **[여정 다시 입력](entry-management.md)**: 캠페인 전략에 따라 프로필이 규칙을 여러 번 다시 입력할 수 있는지 한 번만 입력할 수 있는지 결정합니다. **[!UICONTROL 속성]** 여정에서 **[!UICONTROL 다시 입력]** 설정을 구성하여 대기 기간을 설정하거나 강제 다시 입력을 사용하도록 설정하거나 컨텍스트별 다시 입력을 위해 [보조 식별자](supplemental-identifier.md)를 사용하십시오.

>[!ENDSHADEBOX]

## 자세한 여정 예 {#journey-examples}

전체 기술 세부 사항을 포함한 단계별 구현 지침을 보려면 다음 문서화된 사용 사례를 살펴보십시오.

* **[고객 온보딩 여정](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/tutorials/use-cases/customer-onboarding)** - 대상 자격, 이벤트 시간 제한 및 목표 기반 종료로 개인화된 환영 경험을 빌드합니다.

* **[포기한 장바구니 복구](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart)** - 이벤트 트리거 여정, 플레이북 및 채널 라우팅을 사용하여 손실된 판매 복구

* **[다시 참여 캠페인](https://experienceleague.adobe.com/ko/docs/experience-platform/rtcdp/use-cases/personalization-insights-engagement/use-cases-luma)** - 행동 타깃팅 및 유료 미디어 활성화를 통해 비활성 고객을 다시 확보

* **[구독자에게 메시지 보내기](message-to-subscribers-uc.md)** - 대상자 읽기 및 개인화된 콘텐츠로 구독 목록을 타깃팅합니다.

* **[다중 채널 메시지 보내기](journeys-uc.md)** - 이메일과 푸시를 반응 이벤트 및 다중 경로 논리와 결합합니다.

* **[평일에만 전자 메일 보내기](weekday-email-uc.md)** - 시간 기반 조건 및 대기 수식을 사용하여 통신 예약

>[!TIP]
>
>[여정 사용 사례 라이브러리](jo-use-cases.md)에서 [게재 램프 업](ramp-up-deliveries-uc.md), [경험 이벤트 패턴](exp-event-lookup.md), [라이브 여정에서 프로필 제거](journey-pause.md#apply-an-exit-criteria-in-a-paused-journey)를 포함하여 더 많은 패턴 및 구현을 찾아봅니다.

## 시작 및 종료 관리 우수 사례 {#best-practices}

**정의 지우기**

* 마케팅 및 분석 팀을 조정하기 위해 여정을 작성하기 전에 시작 및 종료 로직을 문서화합니다
* 진입점, 여정 경로 및 종료 조건을 보여 주는 순서도 만들기
* 비즈니스 규칙을 명확히 정의: &quot;X가 발생하거나 Y일 후 프로필이 종료됨&quot;
* 설명 레이블 사용: &quot;종료 1&quot;이 아닌 &quot;종료 - 구매 완료&quot;
* 보고 및 필터링을 위해 [여정에 지속적으로 태그 지정](../start/search-filter-categorize.md#tags)

**여정 중복 방지**

* 충돌을 방지하기 위해 유사한 여정을 시작하기 전에 [활성 계정을 감사](journey-ui.md)
* [충돌 관리](../conflict-prioritization/conflicts.md) 및 [우선 순위 점수](../conflict-prioritization/priority-scores.md)를 활용하여 중복을 해결하고 여정 우선 순위를 지정하십시오
* 서로 경쟁하지 않고 보완하는 여정 디자인

>[!NOTE]
>
>우선순위가 더 높은 여정에 대한 자격이 있을 때 프로필을 자동으로 제거하는 것과 같은 고급 시나리오의 경우 종료 기준 대신 [여정 제한 및 중재](../conflict-prioritization/journey-capping.md)를 사용하십시오.

**모니터링 및 최적화**

* [여정 보고서](../reports/journey-global-report-cja.md)를 사용하여 각 여정에 대한 시작 비율, 종료 비율 및 완료율을 추적합니다.
* [성공 지표](success-metrics.md) 모니터링: 성공 지표 완료를 통해 종료되는 비율과 시간 초과
* 시작하기 전에 다양한 프로필 시나리오를 사용하여 [시작 및 종료 기준 테스트](testing-the-journey.md)
* 데이터를 기반으로 조정: 조기 종료가 높은 경우 시작 기준 관련성을 검토하고 성공 지표 완료가 낮은 경우 콘텐츠 및 타이밍을 분석합니다.
* 분기별 모든 활성 여정 검토

**빈도 상한 준수**

* 적절한 [재등록 대기 기간](entry-management.md)을 설정하거나 일회성 여정에 대한 재등록을 비활성화합니다.
* [빈도 제한 규칙](../conflict-prioritization/rule-sets.md)을(를) 사용하여 과도한 통신을 방지합니다.
* 보고의 빈도 지표를 모니터링하여 규정 준수 보장

>[!NOTE]
>
>여러 여정에서 빈도 제한 및 여정 입력 제한을 관리하려면 [채널별 여정 제한 및 중재](../conflict-prioritization/journey-capping.md) 및 [채널별 빈도 제한](../conflict-prioritization/channel-capping.md)을(를) 사용합니다.

## 결론 {#conclusion}

여정 시작 및 종료 기준은 Adobe Journey Optimizer을 통해 개인화되고, 시기적절하며, 효과적인 고객 경험을 제공하기 위한 기초입니다. 마케터는 이러한 조건을 신중하게 만들어 참여를 촉진하고, 마찰을 줄이고, 더 강한 고객 관계를 형성할 수 있습니다.

먼저 고객 트리거 및 종료 지점을 명확히 매핑하고, 철저하게 테스트하고, 결과를 모니터링하여 여정 오케스트레이션을 지속적으로 구체화합니다.

## 관련 리소스 {#related-resources}

**기술 설명서**

[프로필 시작 관리](entry-management.md) | [여정 속성 및 종료 기준](journey-properties.md) | [여정 종료 방법](end-journey.md) | [보조 식별자](supplemental-identifier.md) | [여정 디자이너](using-the-journey-designer.md)

**튜토리얼 및 예제**

[여정 사용 사례](jo-use-cases.md) | [고객 온보딩 비디오](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/tutorials/use-cases/customer-onboarding) | [포기한 장바구니 비디오](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart) | [커뮤니티 블로그: 시작 및 종료 기준](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/mastering-journey-entry-and-exit-criteria-in-adobe-journey/ba-p/760958)

**관련 기능**

[대상 자격 이벤트](audience-qualification-events.md) | [성공 지표 및 목표](success-metrics.md) | [충돌 관리](../conflict-prioritization/conflicts.md) | [빈도 제한](../conflict-prioritization/rule-sets.md) | [여정 테스트](testing-the-journey.md) | [조건 활동](condition-activity.md) | [반응 이벤트](reaction-events.md) | [대기 활동](wait-activity.md)
