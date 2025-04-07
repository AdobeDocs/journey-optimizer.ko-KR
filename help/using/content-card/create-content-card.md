---
title: 콘텐츠 카드 만들기
description: Journey Optimizer에서 컨텐츠 카드를 작성하고 컨텐츠를 편집하는 방법에 대해 알아봅니다
topic: Content Management
feature: Content Cards
role: User
level: Beginner
exl-id: a26bb3bd-d593-466b-9852-94e194d6d2b7
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '919'
ht-degree: 10%

---

# 콘텐츠 카드 만들기 {#create-content-card}

>[!BEGINTABS]

>[!TAB 여정에 콘텐츠 카드 추가]

여정에 컨텐츠 카드를 추가하려면 다음 단계를 따르십시오.

1. 여정을 열고 팔레트의 **[!UICONTROL 작업]** 섹션에서 **[!UICONTROL 카드]** 활동을 끌어서 놓습니다.

   ![](assets/content-card-jo-1.png)

1. 메시지에 대해 **[!UICONTROL 레이블]** 및 **[!UICONTROL 설명]**&#x200B;을 입력하십시오.

1. 사용할 [콘텐츠 카드 구성](content-card-configuration.md)을 선택하세요.

   ![](assets/content-card-jo-2.png)

1. 이제 **[!UICONTROL 콘텐츠 편집]** 버튼을 사용하여 콘텐츠 디자인을 시작할 수 있습니다. [자세히 알아보기](design-content-card.md)

1. **[!UICONTROL 추가 게재 규칙 사용]** 옵션을 사용하도록 설정합니다. 그런 다음 **[!UICONTROL 규칙을 편집]**&#x200B;하여 메시지를 트리거할 이벤트 및 기준을 선택합니다. 규칙 빌더를 사용하면 충족될 때 작업 세트를 트리거하는 기준과 값을 지정할 수 있습니다.

   ![](assets/content-card-jo-3.png)

   1. 이벤트를 선택하려면 **[!UICONTROL 조건 추가]**&#x200B;를 클릭하세요.

      +++사용 가능한 이벤트 를 참조하십시오.

      | 패키지 | 트리거 | 정의 |
      |---|---|---|
      | 플랫폼으로 데이터 보내기 | 플랫폼으로 데이터 전송됨 | 모바일 앱이 Adobe Experience Platform에 데이터를 보내기 위해 Edge Experience 이벤트를 발행할 때 트리거됩니다. 일반적으로 AEP Edge 확장에서 API 호출 [sendEvent](https://developer.adobe.com/client-sdks/documentation/edge-network/api-reference/#sendevent)을(를) 사용합니다. |
      | 코어 추적 | 작업 추적 | 모바일 코드 API [trackAction](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#trackaction)에서 제공되는 레거시 기능이 호출될 때 트리거됩니다. |
      | 코어 추적 | 상태 추적 | 모바일 코드 API [trackState](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#trackstate)에서 제공되는 레거시 기능이 호출될 때 트리거됩니다. |
      | 코어 추적 | PII 수집 | 모바일 코드 API [collectPII](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#collectpii)에서 제공되는 레거시 기능이 호출될 때 트리거됩니다. |
      | 응용 프로그램 수명 주기 | 애플리케이션 실행 | 충돌 및 설치를 포함하여 실행 시마다 트리거됩니다. 라이프사이클 세션 시간이 초과되면 배경에서 다시 시작할 때도 트리거됩니다. |
      | 응용 프로그램 수명 주기 | 애플리케이션 설치 | 설치 또는 재설치 후 처음 실행할 때 트리거됩니다. |
      | 응용 프로그램 수명 주기 | 애플리케이션 업데이트 | 업그레이드 후 또는 버전 번호가 변경되고 처음 실행할 때 트리거됩니다. |
      | 응용 프로그램 수명 주기 | 애플리케이션 닫기 | 애플리케이션이 닫히면 트리거됩니다. |
      | 응용 프로그램 수명 주기 | 애플리케이션 충돌 | 애플리케이션이 닫기 전에 배경에 있지 않을 경우 트리거됩니다. 이 이벤트는 충돌 후 애플리케이션이 시작될 때 전송됩니다. Adobe Mobile 충돌 보고는 발견되지 않은 전역 예외 핸들러를 구현하지 않습니다. |

+++

   1. **[!UICONTROL 트리거]**&#x200B;를 더 추가하여 규칙을 확장하려면 **[!UICONTROL Or]** 조건을 선택하십시오.

   1. **[!UICONTROL 트레이트]**&#x200B;를 추가하고 규칙을 보다 세밀하게 조정하려면 **[!UICONTROL And]** 조건을 선택하십시오.

      +++사용 가능한 트레이트 를 참조하십시오.

      | 패키지 | 특성 | 정의 |
      |---|---|---|
      | 장치 정보 | 통신사 이름 | 목록의 통신사 이름 중 하나가 충족되면 트리거됩니다. |
      | 장치 정보 | 장치 이름 | 장치 이름 중 하나가 충족되면 트리거됩니다. |
      | 장치 정보 | 로케일 | 목록의 언어 중 하나가 충족되면 트리거됩니다. |
      | 장치 정보 | OS 버전 | 지정된 OS 버전 중 하나가 충족되면 트리거됩니다. |
      | 장치 정보 | 이전 OS 버전 | 지정된 이전 OS 버전 중 하나가 충족되면 트리거됩니다. |
      | 장치 정보 | 실행 모드 | 실행 모드가 애플리케이션 또는 확장인 경우 트리거됩니다. |
      | 응용 프로그램 수명 주기 | 앱 ID | 지정된 앱 ID가 충족되면 트리거됩니다. |
      | 응용 프로그램 수명 주기 | 요일 | 지정된 요일이 충족될 때 트리거됩니다. |
      | 응용 프로그램 수명 주기 | 최초 사용 이후 일 | 처음 사용한 이후 지정된 일 수가 충족되면 트리거됩니다. |
      | 응용 프로그램 수명 주기 | 마지막 사용 이후 일 | 마지막 사용 이후 지정된 일 수가 충족되면 트리거됩니다. |
      | 응용 프로그램 수명 주기 | 업그레이드 이후 일 | 마지막 업그레이드 이후 지정된 일 수가 충족되면 트리거됩니다. |
      | 응용 프로그램 수명 주기 | 설치 날짜 | 지정된 설치 날짜가 충족되면 트리거됩니다. |
      | 응용 프로그램 수명 주기 | 론치 | 지정된 실행 수가 충족되면 트리거됩니다. |
      | 응용 프로그램 수명 주기 | 하루 중 시간 | 지정된 시간이 충족될 때 트리거됩니다. |

+++

   1. 트리거를 함께 그룹화하려면 **[!UICONTROL 그룹 만들기]**&#x200B;를 클릭하세요.

1. 필요한 경우 추가 작업 또는 이벤트를 끌어다 놓아 여정 흐름을 완료합니다. [자세히 알아보기](../building-journeys/about-journey-activities.md)

1. Content 카드가 준비되면 구성을 완료하고 여정을 게시하여 활성화합니다.

여정 구성 방법에 대한 자세한 내용은 [이 페이지](../building-journeys/journey-gs.md)를 참조하세요.

>[!TAB 캠페인에 콘텐츠 카드 추가]

캠페인을 통해 콘텐츠 카드 빌드를 시작하려면 아래 단계를 따르십시오.

1. 캠페인을 만듭니다. [자세히 알아보기](../campaigns/create-campaign.md)

1. 실행할 캠페인 유형 선택

   * **[!UICONTROL 예약됨 - 마케팅]**: 캠페인을 즉시 또는 지정한 날짜에 실행합니다. 예약된 캠페인은 **마케팅** 메시지를 보내는 것을 목표로 합니다. 사용자 인터페이스에서 구성 및 실행됩니다.

   * **[!UICONTROL API 트리거됨 - 마케팅/트랜잭션]**: API 호출을 사용하여 캠페인을 실행하십시오. API 트리거 캠페인은 **마케팅** 또는 **트랜잭션** 메시지(예: 암호 재설정, 장바구니 구매 등 개인이 수행한 작업 후 발송된 메시지)를 보내는 것을 목표로 합니다. [API를 사용하여 캠페인을 트리거하는 방법을 알아봅니다](../campaigns/api-triggered-campaigns.md)

   ![](assets/content-card-create-1.png)

1. **[!UICONTROL 속성]** 섹션에서 캠페인의 이름과 설명을 지정하십시오.

1. **대상** 섹션에서 **[!UICONTROL 대상 선택]** 단추를 클릭하여 사용 가능한 Adobe Experience Platform 대상 목록을 표시합니다. [대상자에 대해 자세히 알아보기](../audience/about-audiences.md)

1. **[!UICONTROL ID 네임스페이스]** 필드에서 선택한 세그먼트에서 개인을 식별하기 위해 사용할 네임스페이스를 선택합니다. [네임스페이스에 대해 자세히 알아보기](../event/about-creating.md#select-the-namespace)

1. **[!UICONTROL 콘텐츠 카드]** 작업을 선택하십시오.

   ![](assets/content-card-create-2.png)

1. [콘텐츠 카드 구성](content-card-configuration.md)을 선택하거나 새로 만듭니다.

1. 메시지의 내용을 테스트하려면 **[!UICONTROL 실험 만들기]**&#x200B;를 클릭하세요. 이를 통해 샘플 모집단에서 여러 게재 변수를 테스트하여 타겟팅된 대상자에게 가장 큰 영향을 미치는 처리를 결정할 수 있습니다. [콘텐츠 실험에 대해 자세히 알아보세요](../content-management/content-experiment.md).

1. 추가 트리거가 필요한 경우 **[!UICONTROL 추가 게재 규칙 사용]** 전환을 사용합니다. 추가 게재 규칙은 필요하지 않습니다.

   **[!UICONTROL 트리거 편집]**&#x200B;을 클릭하여 이벤트 및 메시지 게재 조건을 선택합니다. 규칙 빌더를 사용하면 충족될 때 작업을 트리거하는 조건 및 값을 지정할 수 있습니다.

   ![](assets/content-card-create-3.png)

1. 캠페인을 특정 날짜로 예약하거나 정기적으로 반복되도록 설정할 수 있습니다. [자세히 알아보기](../campaigns/create-campaign.md#schedule)

1. 이제 **[!UICONTROL 콘텐츠 편집]**&#x200B;을 통해 콘텐츠 디자인을 시작할 수 있습니다. [자세히 알아보기](design-content-card.md)

   ![](assets/content-card-create-4.png)

>[!ENDTABS]
