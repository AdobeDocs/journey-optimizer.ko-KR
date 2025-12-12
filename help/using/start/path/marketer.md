---
solution: Journey Optimizer
product: journey optimizer
title: 마케터를 위한 Journey Optimizer 시작
description: 여정 실무자로서 Journey Optimizer를 사용하여 작업하는 방법에 대해 자세히 알아보십시오
level: Beginner
feature: Get Started
Role: User
exl-id: 34304142-3ee8-4081-94b9-e914968c75ba
source-git-commit: 6fbb9f3d47f4299b35214be4966aafb8151183a2
workflow-type: tm+mt
source-wordcount: '1122'
ht-degree: 6%

---

# 마케터를 위한 시작 {#get-started-marketers}

**마케터** 또는 **여정 실무자**&#x200B;는 오퍼 및 여정을 만들고 콘텐츠를 디자인할 책임이 있습니다. [시스템 관리자](administrator.md) 및 [데이터 엔지니어](data-engineer.md)에 액세스 권한을 부여하고 환경을 준비하면 [!DNL Adobe Journey Optimizer] (으)로 작업을 시작할 수 있습니다.

## 기본 사항 시작

Journey Optimizer을 사용하면 이메일, SMS, 푸시, 인앱, 웹, 콘텐츠 카드 등에서 개인화되고 연결된 고객 경험을 만들 수 있습니다. [관리자](administrator.md)와(과) 협력하여 액세스 권한을 얻고 [데이터 엔지니어](data-engineer.md)와(과) 협력하여 대상 및 데이터를 설정합니다.

다음 핵심 단계에 따라 경험 빌드를 시작하십시오.

1. **대상자 만들기**. 세그먼트 정의를 통해 대상자를 만들거나, CSV 파일을 업로드하거나, 대상자 구성을 사용하십시오. Journey Optimizer은 적합한 고객을 타깃팅하는 다양한 방법을 제공합니다. [대상](../../audience/about-audiences.md) 및 [세그먼트 정의 만들기](../../audience/creating-a-segment-definition.md)에 대해 자세히 알아보세요.

1. **콘텐츠 디자인**. 이메일, SMS, 푸시, 인앱, 웹 및 콘텐츠 카드를 포함하여 모든 채널에서 매력적인 메시지 만들기:
   * **AI Assistant**&#x200B;을(를) 사용하여 브랜드 지침을 기반으로 이메일 콘텐츠, 제목 줄 및 이미지를 생성합니다. [AI 콘텐츠 생성에 대해 알아보기](../../content-management/gs-generative.md)
   * 고객 데이터, 다이내믹 콘텐츠 및 조건부 논리를 사용하여 **메시지를 개인 설정**&#x200B;합니다. [개인화에 대해 알아보기](../../personalization/personalize.md)
   * 이벤트, 사용자 지정 작업 및 데이터 집합 조회의 동적 목록을 표시하려면 **컨텍스트 데이터를 반복합니다**. [컨텍스트 데이터 반복에 대해 알아보기](../../personalization/iterate-contextual-data.md)
   * 브랜드 일관성을 유지하기 위해 재사용 가능한 **콘텐츠 템플릿** 및 **조각**&#x200B;을 만듭니다. [템플릿 작업](../../content-management/content-templates.md)
   * 모바일 앱 및 웹 사이트에서 지속적이고 비간섭적인 **콘텐츠 카드**&#x200B;를 제공합니다. 푸시 알림과 달리 콘텐츠 카드는 해제될 때까지 계속 표시됩니다. [콘텐츠 카드에 대해 알아보기](../../content-card/create-content-card.md)
   * **Adobe Experience Manager Assets** 통합으로 자산을 관리합니다. [에셋에 대해 알아보기](../../integrations/assets.md)

   ![](../assets/perso_ee2.png)

1. **오퍼 및 의사 결정 추가**. AI 기반 의사 결정을 사용하여 각 고객에게 적시에 최상의 오퍼를 제공합니다. [의사 결정 관리](../../offers/get-started/starting-offer-decisioning.md) 및 [경험 의사 결정](../../experience-decisioning/gs-experience-decisioning.md)에 대해 알아봅니다.

   ![](../assets/offers-e2e-offers-displayed.png)

1. **테스트 및 유효성 검사**. 보내기 전에 콘텐츠 미리 보기 및 테스트:
   * **테스트 프로필**&#x200B;을 사용하여 개인 맞춤화를 미리 보고 장치 간 렌더링을 확인하십시오.
   * CSV/JSON 파일의 **샘플 데이터**(으)로 테스트
   * 인기 있는 전자 메일 클라이언트에서 **전자 메일 렌더링** 미리 보기
   * 콘텐츠 변형을 최적화하려면 **A/B 테스트 및 실험**&#x200B;을 실행하십시오. multi-armed bandit 실험을 사용하여 실시간으로 더 많은 트래픽을 승리 변형에 자동으로 할당합니다. [실험에 대해 알아보기](../../content-management/content-experiment.md)
   * 캠페인 및 여정에 대해 **승인 워크플로**&#x200B;를 설정합니다(추가 라이선스 필요). [승인에 대해 알아보기](../../test-approve/gs-approval.md)

   [메시지 테스트 및 유효성 검사](../../content-management/preview-test.md)하는 방법을 알아보세요.

1. **고객 여정 작성**. 여정 캔버스를 사용하여 개인화된 실시간 경험을 만듭니다.

   * **여정**(고객 작업) 또는 **대상**(일괄 전송)으로 이벤트 트리거
   * 고객 데이터를 기반으로 개인화된 경로를 만들려면 **조건**&#x200B;을 추가하십시오.
   * **대기 활동**&#x200B;을 사용하여 메시지 사이에 완벽한 타이밍을 만드십시오.
   * 한 여정 내에서 **여러 채널**&#x200B;을 통해 메시지 보내기
   * **A/B 테스트**&#x200B;를 적용하고 전송 시간을 최적화하여 참여를 극대화합니다.
   * **데이터 집합 조회**&#x200B;를 사용하여 Adobe Experience Platform의 실시간 데이터로 여정을 보강합니다. [데이터 세트 조회에 대해 알아보기](../../building-journeys/dataset-lookup.md)
   * **보조 식별자**&#x200B;을(를) 활용하여 동일한 프로필에서 여러 여정 인스턴스(예: 다른 주문 또는 예약)를 입력할 수 있도록 합니다. [보조 식별자에 대해 알아보기](../../building-journeys/supplemental-identifier.md)

   ![](../assets/journey-design.png)

   [여정을 디자인 및 실행](../../building-journeys/journey-gs.md)하고 [여정 사용 사례](../../building-journeys/jo-use-cases.md)를 살펴보는 방법에 대해 알아봅니다. 프로필 흐름을 제어하려면 [시작/종료 기준](../../building-journeys/entry-exit-criteria-guide.md)을 이해하십시오.

1. **모니터링 및 최적화**. 시간 경과에 따른 성능 추적 및 결과 개선:
   * **실시간 여정** 성능 모니터링 및 병목 현상 식별
   * **메시지 게재** 비율 및 참여 지표 분석
   * Customer Journey Analytics 통합으로 **보고 대시보드** 사용
   * **전환** 및 비즈니스 영향 추적
   * 과도한 통신을 방지하기 위해 충돌 관리 규칙을 사용하여 **메시지 빈도 및 우선 순위 지정**&#x200B;을(를) 관리합니다. [충돌 관리에 대해 알아보기](../../conflict-prioritization/gs-conflict-prioritization.md)

   [성능을 모니터링](../../reports/report-gs-cja.md)하는 방법에 대해 알아봅니다.

## 성공을 위한 우수 사례

### 콘텐츠 만들기

* **템플릿으로 시작**: 미리 만들어진 템플릿과 콘텐츠 조각을 사용하여 만들기 속도를 높이고 일관성을 유지합니다.
* **일찍 테스트하고 자주 테스트하십시오**: 항상 장치 간에 콘텐츠를 미리 보고 테스트 프로필을 사용하여 개인화의 유효성을 검사하십시오
* **AI를 현명하게 활용**: 초기 초안 및 변형에는 AI Assistant를 사용하지만 브랜드 목소리에 맞게 항상 검토하고 다듬을 수 있습니다
* **단순하게 유지**: 강력한 클릭 유도 문안 메시지를 통해 명확하고 간결한 메시지를 사용하면 복잡한 레이아웃보다 더 나은 성과를 얻을 수 있습니다.

### 여정 디자인

* **명확한 목표 정의**: 여정 구축 전에 성공 지표를 설정하십시오.
* **고객 경험 매핑**: 구현하기 전에 전체 여정 시각화
* **대기 활동을 전략적으로 사용**: 후속 작업을 보내기 전에 고객에게 참여할 시간을 제공합니다.
* **종료 전략 계획**: 고객이 여정을 종료해야 하는 시기와 이유를 정의합니다.
* **초안 모드에서 테스트**: 활성화하기 전에 시험 실행으로 여정 논리의 유효성을 검사합니다.

[여정 모범 사례 학습](../../building-journeys/entry-exit-criteria-guide.md#best-practices)

### 대상 타기팅

* **신중하게 세그먼트**: 명확한 기준에 따라 실행 가능한 특정 대상 세그먼트를 만듭니다.
* **정기적으로 새로 고침**: 적절한 평가 일정을 설정하여 대상자가 최신 상태를 유지하는지 확인하십시오.
* **균형 크기 및 정밀도**: 통계적 중요도는 충분히 크지만 관련성은 충분히 구체적인 대상
* **데이터 보강 특성 사용**: 더 자세한 개인화를 위해 계산된 특성 및 데이터 보강 데이터를 활용합니다.

### 빈도 관리

* **고객 환경 설정 준수**: 옵트아웃 및 커뮤니케이션 환경 설정 준수
* **빈도 상한선 설정**: 채널 간 메시지 피로를 방지하기 위해 규칙 집합을 사용합니다.
* **캠페인 조정**: 충돌 관리를 사용하여 고객이 적시에 올바른 메시지를 받도록 합니다.
* **참여 모니터링**: 피로의 징후를 확인하십시오(열람율 감소, 구독 취소 증가).

[빈도 설정에 대해 알아보기](../../conflict-prioritization/channel-capping.md)

## 사용 사례 살펴보기

Journey Optimizer 기능을 보여 주는 실제 사례를 통해 알아보십시오.

**자주 사용하는 사용 사례:**

* **시작 시리즈**: 개인화된 여러 단계 여정으로 새 고객을 온보딩합니다. [사용 사례 보기](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/tutorials/use-cases/customer-onboarding)
* **장바구니 복구를 중단함**: 장바구니에 항목을 남긴 고객을 다시 참여시키십시오. [사용 사례 보기](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart)
* **재참여 캠페인**: 타깃팅된 오퍼를 사용하여 비활성 고객을 다시 확보하십시오. [사용 사례 보기](https://experienceleague.adobe.com/ko/docs/experience-platform/rtcdp/use-cases/personalization-insights-engagement/use-cases-luma)
* **생일 캠페인**: 특별 오퍼와 함께 개인화된 생일 메시지를 보냅니다.
* **제품 추천**: 탐색 및 구매 기록을 기반으로 관련 제품 제안
* **이벤트 기반 메시징**: 고객 작업에 실시간으로 응답

**여정 패턴:**

* [구독자에게 메시지 보내기](../../building-journeys/message-to-subscribers-uc.md): 개인화된 콘텐츠가 있는 구독 목록을 대상으로 합니다.
* [다중 채널 메시징](../../building-journeys/journeys-uc.md): 이메일과 푸시를 반응 이벤트와 결합
* [평일 전용 이메일](../../building-journeys/weekday-email-uc.md): 시간 기반 조건을 사용하여 통신 예약

더 많은 패턴 및 구현을 보려면 전체 [여정 사용 사례 라이브러리](../../building-journeys/jo-use-cases.md)를 찾아보십시오.

## 다른 역할과 공동 작업

마케팅 작업은 다른 팀과 연결됩니다.

* **[데이터 엔지니어와 작업](data-engineer.md)**: 새로운 계산된 특성을 요청하고, 대상 품질에 대한 피드백을 제공하고, 데이터 요구 사항을 조정합니다
* **[개발자와 작업](developer.md)**: 이벤트 트리거를 조정하고, 모바일 구현을 테스트하고, 추적 유효성 검사를 수행합니다.
* **[관리자](administrator.md)**&#x200B;와(과) 작업: 채널 구성을 요청하고, 사용 권한에 대한 문제를 보고하고, 새 기능 사용을 조정합니다.

## 업데이트 상태 유지

최신 Journey Optimizer 기능 및 마케팅 기능을 최신 상태로 유지하십시오.

* **[릴리스 정보](../../rn/release-notes.md)**: 매달 릴리스되는 새로운 기능, 채널 업데이트 및 개선 사항을 검토합니다.
* **[설명서 업데이트](../../rn/documentation-updates.md)**: 새로운 사용 사례, 모범 사례 및 기능 설명서를 포함하여 최근 변경 내용을 추적합니다.
* **제품 알림**: [Adobe Experience Cloud 프로필](https://experience.adobe.com/preferences){target="_blank"}에서 알림을 활성화하여 다음에 대한 알림을 받을 수 있습니다.
   * 새로운 채널 및 기능
   * 예정된 기능 실행 및 베타 프로그램
   * 모범 사례 및 교육 기회
   * 캠페인에 영향을 주는 중요한 공지

  알림을 활성화하려면 Adobe Experience Cloud 오른쪽 상단의 프로필 아이콘을 클릭하고 **환경 설정 > 알림**(으)로 이동한 다음 Journey Optimizer 알림 환경 설정을 구성하십시오.

## 다음 단계

1. **작게 시작**: 플랫폼을 학습하려면 간단한 시작 여정 또는 단일 메시지 캠페인을 만드십시오.
2. **AI 활용**: AI Assistant를 사용하여 질문하고 콘텐츠 생성 속도를 높입니다.
3. **커뮤니티에 참여**: [Experience League 커뮤니티에서 다른 Journey Optimizer 사용자와 연결](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer){target="_blank"}
4. **튜토리얼 살펴보기**: [Experience League](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=ko){target="_blank"}에서 단계별 비디오 보기
