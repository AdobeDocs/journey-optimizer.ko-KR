---
title: Journey Optimizer에서 인앱 알림 만들기
description: Journey Optimizer에서 인앱 메시지를 만드는 방법을 알아봅니다
feature: In App
topic: Content Management
role: User
level: Beginner
keywords: 인앱, 메시지, 만들기, 시작
exl-id: b3b79fe2-7db3-490d-9c3d-87267aa55eea
source-git-commit: 59ecb9a5376e697061ddac4cc68f09dee68570c0
workflow-type: tm+mt
source-wordcount: '1961'
ht-degree: 13%

---

# 인앱 메시지 만들기  {#create-in-app}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_triggers"
>title="인앱 트리거 관리"
>abstract="메시지를 활성화할 특정 이벤트 및 기준을 선택하여 트리거를 효율적으로 제어합니다. 사용자는 규칙 빌더를 사용하여 정확한 조건 및 값을 정의할 수 있습니다. 이러한 조건이 충족되면 인앱 메시지 게재를 포함한 일련의 작업이 시작됩니다."

캠페인 또는 여정에서 인앱 메시지를 추가할 수 있습니다. 아래 설명된 단계에 따라 두 컨텍스트에서 인앱 메시지를 만드십시오.

인앱 메시지는 운영 체제에서 푸시 알림의 옵트인 또는 옵트아웃에 대한 사용자의 선택에 의해 영향을 받지 않습니다.

>[!BEGINTABS]

>[!TAB 여정에 인앱 메시지 추가]

여정에 인앱 메시지를 추가하려면 다음 단계를 수행합니다.

1. 여정을 열고 팔레트의 **[!UICONTROL 작업]** 섹션에서 **[!UICONTROL 인앱]** 활동을 끌어서 놓습니다.

   프로필이 여정 끝에 도달하면 표시되는 모든 인앱 메시지가 자동으로 만료됩니다. 이러한 이유로, 적절한 타이밍을 보장하기 위해 인앱 활동 후에 대기 활동이 자동으로 추가됩니다.

   ![](assets/in_app_journey_1.png)

1. 메시지에 대해 **[!UICONTROL 레이블]** 및 **[!UICONTROL 설명]**&#x200B;을 입력하십시오.

1. 사용할 [인앱 표면](inapp-configuration.md)을(를) 선택하십시오.

   ![](assets/in_app_journey_2.png)

1. 이제 **[!UICONTROL 콘텐츠 편집]** 버튼을 사용하여 콘텐츠 디자인을 시작할 수 있습니다. [자세히 알아보기](design-in-app.md)

1. 메시지를 트리거할 이벤트 및 조건을 선택하려면 **[!UICONTROL 트리거 편집]**&#x200B;을 클릭하세요. 규칙 빌더를 사용하면 충족될 경우 인앱 메시지 전송과 같은 작업 세트를 트리거하는 기준과 값을 지정할 수 있습니다.

   ![](assets/in_app_journey_4.png)

   1. 필요한 경우 이벤트 드롭다운을 클릭하여 트리거 를 변경합니다.

      +++사용 가능한 트리거 를 참조하십시오.

      | 패키지 | 트리거 | 정의 |
      |---|---|---|
      | 플랫폼으로 데이터 보내기 | 플랫폼으로 데이터 전송됨 | 모바일 앱이 Adobe Experience Platform에 데이터를 보내기 위해 Edge Experience 이벤트를 발행할 때 트리거됩니다. 일반적으로 API는 AEP Edge 확장에서 [sendEvent](https://developer.adobe.com/client-sdks/documentation/edge-network/api-reference/#sendevent)를 호출합니다. |
      | 코어 추적 | 작업 추적 | 모바일 코드 API [trackAction](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#trackaction)에서 제공되는 레거시 기능이 호출될 때 트리거됩니다. |
      | 코어 추적 | 상태 추적 | 모바일 코드 API [trackState](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#trackstate)에서 제공되는 레거시 기능이 호출될 때 트리거됩니다. |
      | 코어 추적 | PII 수집 | 모바일 코드 API [collectPII](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#collectpii)에서 제공되는 레거시 기능이 호출될 때 트리거됩니다. |
      | 응용 프로그램 수명 주기 | 애플리케이션 실행 | 충돌 및 설치를 포함하여 실행 시마다 트리거됩니다. 라이프사이클 세션 시간이 초과되면 배경에서 다시 시작할 때도 트리거됩니다. |
      | 응용 프로그램 수명 주기 | 애플리케이션 설치 | 설치 또는 재설치 후 처음 실행할 때 트리거됩니다. |
      | 응용 프로그램 수명 주기 | 애플리케이션 업데이트 | 업그레이드 후 또는 버전 번호가 변경되고 처음 실행할 때 트리거됩니다. |
      | 응용 프로그램 수명 주기 | 애플리케이션 닫기 | 애플리케이션이 닫히면 트리거됩니다. |
      | 응용 프로그램 수명 주기 | 애플리케이션 충돌 | 애플리케이션이 닫기 전에 배경에 있지 않을 경우 트리거됩니다. 이 이벤트는 충돌 후 애플리케이션이 시작될 때 전송됩니다. Adobe Mobile 충돌 보고는 발견되지 않은 전역 예외 핸들러를 구현하지 않습니다. |
      | 장소 | POI 입력 | 고객이 사용자가 구성한 관심 영역(POI)에 들어갈 때 위치 SDK에 의해 트리거됩니다. |
      | 장소 | POI 종료 | 고객이 사용자가 구성한 관심 영역(POI)을 종료할 때 위치 SDK에 의해 트리거됩니다. |

+++

   1. 트리거에서 여러 이벤트 또는 조건을 고려하려면 **[!UICONTROL 조건 추가]**&#x200B;를 클릭하십시오.

   1. **[!UICONTROL 트리거]**&#x200B;를 더 추가하여 규칙을 확장하려면 **[!UICONTROL Or]** 조건을 선택하십시오.

      ![](assets/in_app_create_3.png)

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
      | 장소 | 현재 POI | 고객이 지정된 관심 영역(POI)에 들어갈 때 위치 SDK에 의해 트리거됩니다. |
      | 장소 | 마지막으로 입력한 POI | 마지막으로 입력한 POI(관심 영역)에 따라 위치 SDK에 의해 트리거됩니다. |
      | 장소 | 마지막으로 종료한 POI | 고객이 마지막으로 종료한 관심 영역(POI)에 따라 위치 SDK에 의해 트리거됩니다. |

+++

      ![](assets/in_app_create_8.png)

   1. 트리거를 함께 그룹화하려면 **[!UICONTROL 그룹 만들기]**&#x200B;를 클릭하세요.

      ![](assets/in_app_journey_3.png)

   1. 인앱 메시지가 활성 상태일 때 트리거 빈도를 선택합니다.

      * **[!UICONTROL 항상 표시]**: **[!UICONTROL 모바일 앱 트리거]** 드롭다운에서 선택한 이벤트가 발생하면 항상 메시지를 표시합니다.
      * **[!UICONTROL 한 번 표시]**: **[!UICONTROL 모바일 앱 트리거]** 드롭다운에서 선택한 이벤트가 처음 발생할 때만 이 메시지를 표시합니다.
      * **[!UICONTROL 클릭할 때까지 표시]**: **[!UICONTROL 모바일 앱 트리거]** 드롭다운에서 선택한 이벤트가 &quot;클릭함&quot; 동작을 사용하여 SDK에서 상호 작용 이벤트를 보낼 때까지 발생할 때 이 메시지를 표시합니다.

1. 필요한 경우 추가 작업 또는 이벤트를 끌어다 놓아 여정 흐름을 완료합니다. [자세히 알아보기](../building-journeys/about-journey-activities.md)

1. 인앱 메시지가 준비되면 구성을 완료하고 여정을 게시하여 활성화합니다.

여정 구성 방법에 대한 자세한 내용은 [이 페이지](../building-journeys/journey-gs.md)를 참조하세요.

>[!TAB 인앱 메시지를 캠페인에 추가]

캠페인에 인앱 메시지를 추가하려면 다음 단계를 수행합니다.

1. **[!UICONTROL 캠페인]** 메뉴에 액세스한 다음 **[!UICONTROL 캠페인 만들기]**&#x200B;를 클릭합니다.

1. **[!UICONTROL 속성]** 섹션에서 캠페인 실행 유형(예약됨 또는 API 트리거됨)을 선택합니다. [이 페이지](../campaigns/create-campaign.md#campaigntype)에서 캠페인 유형에 대해 자세히 알아보세요.

1. **[!UICONTROL 작업]** 섹션에서 인앱 메시지에 대해 이전에 구성된 **[!UICONTROL 인앱 메시지]** 및 **[!UICONTROL 앱 표면]**&#x200B;을 선택합니다. 그런 다음 **[!UICONTROL 만들기]**&#x200B;를 클릭합니다.

   [이 페이지](inapp-configuration.md)에서 인앱 구성에 대해 자세히 알아보세요.

   ![](assets/in_app_create_1.png)

1. **[!UICONTROL 속성]** 섹션에서 **[!UICONTROL 제목]** 및 **[!UICONTROL 설명]** 설명을 입력하십시오.

1. 인앱 메시지에 사용자 지정 또는 핵심 데이터 사용 레이블을 할당하려면 **[!UICONTROL 액세스 관리]**&#x200B;를 선택하세요. [자세히 알아보기](../administration/object-based-access.md).

1. 사용 가능한 Adobe Experience Platform 대상 목록에서 타깃팅할 대상을 정의하려면 **[!UICONTROL 대상 선택]** 단추를 클릭하십시오. [자세히 알아보기](../audience/about-audiences.md).

   ![](assets/in_app_create_2.png)

1. **[!UICONTROL ID 네임스페이스]** 필드에서 선택한 대상에서 개인을 식별하기 위해 사용할 네임스페이스를 선택합니다. [자세히 알아보기](../event/about-creating.md#select-the-namespace).

1. 콘텐츠 실험 구성을 시작하고 처리를 만들어 성능을 측정하고 대상 대상에 가장 적합한 옵션을 식별하려면 **[!UICONTROL 실험 만들기]**&#x200B;를 클릭하십시오. [자세히 알아보기](../content-management/content-experiment.md)

1. 메시지를 트리거할 이벤트 및 조건을 선택하려면 **[!UICONTROL 트리거 편집]**&#x200B;을 클릭하세요. 규칙 빌더를 사용하면 충족될 경우 인앱 메시지 전송과 같은 작업 세트를 트리거하는 기준과 값을 지정할 수 있습니다.

   1. 필요한 경우 이벤트 드롭다운을 클릭하여 트리거 를 변경합니다.

      +++사용 가능한 트리거 를 참조하십시오.

      | 패키지 | 트리거 | 정의 |
      |---|---|---|
      | 플랫폼으로 데이터 보내기 | 플랫폼으로 데이터 전송됨 | 모바일 앱이 Adobe Experience Platform에 데이터를 보내기 위해 Edge Experience 이벤트를 발행할 때 트리거됩니다. 일반적으로 API는 AEP Edge 확장에서 [sendEvent](https://developer.adobe.com/client-sdks/documentation/edge-network/api-reference/#sendevent)를 호출합니다. |
      | 코어 추적 | 작업 추적 | 모바일 코드 API [trackAction](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#trackaction)에서 제공되는 레거시 기능이 호출될 때 트리거됩니다. |
      | 코어 추적 | 상태 추적 | 모바일 코드 API [trackState](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#trackstate)에서 제공되는 레거시 기능이 호출될 때 트리거됩니다. |
      | 코어 추적 | PII 수집 | 모바일 코드 API [collectPII](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#collectpii)에서 제공되는 레거시 기능이 호출될 때 트리거됩니다. |
      | 응용 프로그램 수명 주기 | 애플리케이션 실행 | 충돌 및 설치를 포함하여 실행 시마다 트리거됩니다. 라이프사이클 세션 시간이 초과되면 배경에서 다시 시작할 때도 트리거됩니다. |
      | 응용 프로그램 수명 주기 | 애플리케이션 설치 | 설치 또는 재설치 후 처음 실행할 때 트리거됩니다. |
      | 응용 프로그램 수명 주기 | 애플리케이션 업데이트 | 업그레이드 후 또는 버전 번호가 변경되고 처음 실행할 때 트리거됩니다. |
      | 응용 프로그램 수명 주기 | 애플리케이션 닫기 | 애플리케이션이 닫히면 트리거됩니다. |
      | 응용 프로그램 수명 주기 | 애플리케이션 충돌 | 애플리케이션이 닫기 전에 배경에 있지 않을 경우 트리거됩니다. 이 이벤트는 충돌 후 애플리케이션이 시작될 때 전송됩니다. Adobe Mobile 충돌 보고는 발견되지 않은 전역 예외 핸들러를 구현하지 않습니다. |
      | 장소 | POI 입력 | 고객이 사용자가 구성한 관심 영역(POI)에 들어갈 때 위치 SDK에 의해 트리거됩니다. |
      | 장소 | POI 종료 | 고객이 사용자가 구성한 관심 영역(POI)을 종료할 때 위치 SDK에 의해 트리거됩니다. |

+++

   1. 트리거에서 여러 이벤트 또는 조건을 고려하려면 **[!UICONTROL 조건 추가]**&#x200B;를 클릭하십시오.

   1. **[!UICONTROL 트리거]**&#x200B;를 더 추가하여 규칙을 확장하려면 **[!UICONTROL Or]** 조건을 선택하십시오.

      ![](assets/in_app_create_3.png)

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
      | 장소 | 현재 POI | 고객이 지정된 관심 영역(POI)에 들어갈 때 위치 SDK에 의해 트리거됩니다. |
      | 장소 | 마지막으로 입력한 POI | 마지막으로 입력한 POI(관심 영역)에 따라 위치 SDK에 의해 트리거됩니다. |
      | 장소 | 마지막으로 종료한 POI | 고객이 마지막으로 종료한 관심 영역(POI)에 따라 위치 SDK에 의해 트리거됩니다. |

+++

      ![](assets/in_app_create_8.png)

   1. 트리거를 함께 그룹화하려면 **[!UICONTROL 그룹 만들기]**&#x200B;를 클릭하세요.

1. 인앱 메시지가 활성 상태일 때 트리거 빈도를 선택합니다. 다음 옵션을 사용할 수 있습니다.

   * **[!UICONTROL 항상]**: **[!UICONTROL 모바일 앱 트리거]** 드롭다운에서 선택한 이벤트가 발생하면 항상 메시지를 표시합니다.
   * **[!UICONTROL 한 번]**: **[!UICONTROL 모바일 앱 트리거]** 드롭다운에서 선택한 이벤트가 처음 발생할 때만 이 메시지를 표시합니다.
   * **[!UICONTROL 클릭할 때까지]**: **[!UICONTROL 모바일 앱 트리거]** 드롭다운에서 선택한 이벤트가 SDK에서 &quot;클릭함&quot; 동작을 사용하여 상호 작용 이벤트를 보낼 때까지 발생할 때 이 메시지를 표시합니다.
   * **[!UICONTROL X회]**: 이 메시지를 X회 표시합니다.

1. 필요한 경우 인앱 메시지를 표시할 **[!UICONTROL 요일]** 또는 **[!UICONTROL 시간]**&#x200B;을(를) 선택하십시오.

1. 캠페인은 특정 날짜 또는 되풀이되는 빈도로 실행되도록 디자인됩니다. [이 섹션](../campaigns/create-campaign.md#schedule)에서 캠페인의 **[!UICONTROL 일정]**&#x200B;을 구성하는 방법을 알아보세요.

   ![](assets/in-app-schedule.png)

1. 이제 **[!UICONTROL 콘텐츠 편집]** 버튼을 사용하여 콘텐츠 디자인을 시작할 수 있습니다. [자세히 알아보기](design-in-app.md)

   ![](assets/in_app_create_4.png)

>[!ENDTABS]

## 방법 비디오{#video}

* 아래 비디오에서는 캠페인에서 인앱 메시지를 만들고, 구성하고, 게시하는 방법을 보여 줍니다.

  +++비디오 참조

  >[!VIDEO](https://video.tv.adobe.com/v/3410430?quality=12&learn=on)

+++

* 아래 비디오에서는 A/B 테스트 인앱 메시지에 대한 콘텐츠 실험을 구성하고 분석하는 방법을 보여 줍니다.

  +++비디오 참조

  >[!VIDEO](https://video.tv.adobe.com/v/3419898)

+++

* 아래 비디오에서는 여정에서 인앱 메시지를 만드는 방법과 여정을 테스트하고 게시하는 방법을 보여 줍니다.

  +++비디오 참조

  >[!VIDEO](https://video.tv.adobe.com/v/3423077)

+++

**관련 항목:**

* [인앱 메시지 디자인](design-in-app.md)
* [인앱 메시지 테스트 및 보내기](send-in-app.md)
* [인앱 보고서 ](../reports/campaign-global-report.md#inapp-report)
* [인앱 구성](inapp-configuration.md)