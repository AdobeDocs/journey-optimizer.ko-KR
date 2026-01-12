---
solution: Journey Optimizer
product: journey optimizer
title: 시스템 경고 액세스 및 구독
description: 시스템 경고에 액세스하고 구독하는 방법을 알아봅니다
feature: Journeys, Alerts, Monitoring
topic: Administration
role: User
level: Intermediate
exl-id: 0855ca5b-c7af-41c4-ad51-bed820ae5ecf
source-git-commit: 03e9d4205f59a32347cd1702b24bfbad2bf540b9
workflow-type: tm+mt
source-wordcount: '2385'
ht-degree: 1%

---

# 시스템 경고 액세스 및 구독 {#alerts}

## 개요

Adobe Journey Optimizer은 작업을 모니터링하고 문제를 해결하는 데 도움이 되는 두 가지 유형의 경고를 제공합니다.

* **캔버스 내 유효성 검사 경고**: 여정 및 캠페인을 빌드할 때 캔버스에서 **경고** 단추를 사용하여 게시 전에 구성 오류를 식별하고 해결하십시오. [여정 문제 해결](../building-journeys/troubleshooting.md)을 통해 캠페인을 검토하는 방법을 알아봅니다. [액션 캠페인](../campaigns/review-activate-campaign.md) | [API 트리거 캠페인](../campaigns/review-activate-api-triggered-campaign.md) | [오케스트레이션된 캠페인](../orchestrated/start-monitor-campaigns.md).

* **시스템 모니터링 경고**(이 페이지에 자세히 설명됨): 운영 임계값이 초과되거나 실시간 여정 및 채널 구성에서 문제가 감지되면 사전 알림을 받습니다. 이러한 경고를 통해 잠재적인 문제가 고객 경험에 영향을 미치기 전에 신속하게 대응할 수 있습니다.

시스템 경고는 **[!UICONTROL 관리]**&#x200B;의 **[!UICONTROL 경고]** 메뉴에서 사용할 수 있습니다. Adobe Experience Platform은 여정 및 채널 구성에 대한 [!DNL Adobe Journey Optimizer]별 경고를 포함하여 활성화할 수 있는 사전 정의된 경고 규칙을 제공합니다.

## 전제 조건

경고 작업 전:

* **권한**: 경고를 보고 관리하려면 특정 권한이 필요합니다. [Adobe Experience Platform에서 필요한 권한](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html#permissions){target="_blank"}을 참조하세요.

* **샌드박스 인식**: 경고 구독은 샌드박스별로 다릅니다. 경고에 가입하면 현재 샌드박스에만 적용됩니다. 샌드박스가 재설정되면 모든 경고 구독도 재설정됩니다.

* **알림 환경 설정**: [Adobe Experience Cloud 환경 설정](../start/user-interface.md#in-product-uc)에서 알림(전자 메일 및/또는 인앱)을 받는 방법을 구성합니다.

>[!NOTE]
>
>Journey Optimizer 관련 경고는 **live** 여정에 대해서만 적용됩니다. 테스트 모드의 여정에 대해서는 경고가 트리거되지 않습니다. 경고 프레임워크에 대한 자세한 내용은 [Adobe Experience Platform 경고 설명서](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=ko){target="_blank"}를 참조하십시오.

## 사용 가능한 경고

경고에 액세스하려면 왼쪽 메뉴에서 **[!UICONTROL 관리]** > **[!UICONTROL 경고]**&#x200B;로 이동하십시오. **찾아보기** 탭에는 Journey Optimizer에 사용할 수 있는 사전 구성된 모든 경고가 표시됩니다.

![](assets/updated-alerts-list.png){width=50%}

Journey Optimizer은 두 가지 범주의 시스템 경고를 제공합니다.

**여정 경고** - 여정 실행 및 성능 모니터링:

* [대상자 읽기 트리거 실패](#alert-read-audiences) - 대상자 읽기 활동이 프로필을 처리하지 못할 때 경고합니다.
* [사용자 지정 작업 오류율 초과](#alert-custom-action-error-rate) - 사용자 지정 작업 API 호출에서 높은 오류율을 검색합니다(이전 여정 사용자 지정 작업 실패 경고를 대체).
* [프로필 삭제 비율 초과](#alert-discard-rate) - 프로필이 비정상적인 비율로 삭제되는 시기를 식별합니다.
* [프로필 오류율 초과](#alert-profile-error-rate) - 여정 실행 중 프로필에 오류가 발생하면 플래그로 표시합니다.
* [여정 게시됨](#alert-journey-published) - 여정 게시 시 정보 알림
* [여정 완료됨](#alert-journey-finished) - 여정 완료 시 정보 알림
* [사용자 지정 작업 한도 트리거됨](#alert-custom-action-capping) - API 호출 한도에 도달하면 알립니다.

**채널 구성 경고** - 전자 메일 게재 기능 설정 관련 문제 감지:

* [AJO 도메인 DNS 레코드 누락](#alert-dns-record-missing) - 누락 또는 잘못 구성된 DNS 레코드를 식별합니다.
* [AJO 채널 구성 실패](#alert-channel-config-failure) - 전자 메일 구성 문제(SPF, DKIM, MX 레코드)를 검색합니다.
  <!--* the [AJO domain certificates renewal unsuccessful](#alert-certificates-renewal) alert-->

>[!NOTE]
>
>다른 Adobe Experience Platform 서비스의 경고(데이터 수집, ID 확인, 세그먼테이션 등)에 대해서는 [표준 경고 규칙 문서](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/rules.html){target="_blank"}를 참조하십시오.

## 경고 구독 {#subscribe-alerts}

경고 알림은 특정 조건이 충족될 때(예: 임계값 초과 또는 구성 문제 감지) 경고 알림을 구독한 사용자에게 전달됩니다.

다음 두 가지 방법으로 경고에 가입할 수 있습니다.

* **[전역 구독](#global-subscription)**: 현재 샌드박스의 모든 여정 및 캠페인에 적용
* **[여정 특정 구독](#unitary-subscription)**: 개별 여정에 대해서만 적용

**경고 알림 작동 방식:**

* **게재 채널**: 경고는 Journey Optimizer 알림 센터(오른쪽 상단 모서리의 벨 아이콘)의 이메일 및/또는 인앱 알림을 통해 전송됩니다. [Adobe Experience Cloud 환경 설정](../start/user-interface.md#in-product-uc)에서 선호하는 게재 채널을 구성하십시오.

* **경고 유형**: Journey Optimizer은 일회성 경고(게시된 여정과 같은 정보 이벤트)와 반복 경고(임계값 모니터링)를 모두 제공합니다. 조건이 해결될 때까지 반복 경고가 계속됩니다.

* **해결 방법**: 경고 조건이 해결되면 구독자에게 &quot;해결됨&quot; 알림이 전송됩니다. 알림 피로가 값 변동을 방지하기 위해 상태가 지속되더라도 1시간 후에 경고가 자동으로 해결됩니다.

I/O 이벤트를 통해 구독하는 방법에 대한 자세한 내용은 [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html){target="_blank"}를 참조하세요.


### 전역 구독 {#global-subscription}

전역 구독을 통해 현재 샌드박스의 모든 여정 및 캠페인에 대한 알림을 받을 수 있습니다.

**경고를 구독하려면:**

1. 왼쪽 메뉴에서 **[!UICONTROL 관리]** > **[!UICONTROL 경고]**(으)로 이동합니다.

1. **[!UICONTROL 찾아보기]** 탭에서 모니터링할 경고를 찾습니다.

1. 원하는 경고를 보려면 **[!UICONTROL 구독]**&#x200B;을 클릭하세요.

   ![경고 구독 중](assets/alert-subscribe.png){width=80%}

**구독을 취소하려면:**

경고 옆에 있는 **[!UICONTROL 구독 취소]**&#x200B;를 클릭합니다.

>[!IMPORTANT]
>
>경고 구독은 샌드박스별로 다릅니다. 알림을 수신하려는 각 샌드박스에서 별도로 경고에 가입해야 합니다.

**대체 구독 메서드:**

외부 시스템과의 통합을 허용하는 [I/O 이벤트 알림](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html){target="_blank"}을 통해 구독할 수도 있습니다. Journey Optimizer 경고에 대한 이벤트 구독 이름이 아래 [경고 설명](#journey-alerts)에 각각 나열됩니다.

### 여정 특정 구독 {#unitary-subscription}

여정 특정 구독을 사용하면 조직의 모든 여정에 대해 경고를 받지 않고 우선순위가 높은 개별 여정을 모니터링할 수 있습니다.

**특정 여정에 대한 경고를 구독하려면:**

1. 여정 인벤토리로 이동합니다.

1. 모니터링할 여정의 **⋯**(추가 작업) 메뉴를 클릭합니다.

1. **[!UICONTROL 경고 구독]**&#x200B;을 선택하세요.

   ![특정 여정에 대한 경고를 구독하는 중](assets/subscribe-journey-alert.png){width=75%}

1. 사용 가능한 옵션에서 활성화할 경고를 선택합니다.
   * [프로필 삭제율 초과](#alert-discard-rate)
   * [사용자 정의 액션 오류율 초과](#alert-custom-action-error-rate)
   * [프로필 오류율 초과](#alert-profile-error-rate)
   * [여정 게시됨](#alert-journey-published)
   * [여정 완료됨](#alert-journey-finished)
   * [사용자 지정 작업 한도 트리거됨](#alert-custom-action-capping)

1. 구독을 확인하려면 **[!UICONTROL 저장]**&#x200B;을 클릭하세요.

**구독을 취소하려면:**

같은 대화 상자를 열고 경고를 선택 취소한 다음 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

>[!NOTE]
>
>[대상자 트리거 읽기 실패](#alert-read-audiences) 경고는 여정 구독이 아닌 전역 구독을 통해서만 사용할 수 있습니다.

<!--To enable email alerting, refer to [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html#enable-email-alerts){target="_blank"}.-->

## 여정 경고 {#journey-alerts}


사용자 인터페이스에서 사용할 수 있는 모든 여정 알림이 아래에 나열되어 있습니다.

>[!CAUTION]
>
>Adobe Journey Optimizer 관련 경고는 **live** 여정에 대해서만 적용됩니다. 테스트 모드의 여정에 대해서는 경고가 트리거되지 않습니다.

### 대상자 읽기 트리거 실패 {#alert-read-audiences}

이 경고는 **대상자 읽기** 활동이 예약된 실행 시간 10분 후에 어떤 프로필도 처리하지 않은 경우 경고합니다. 이 실패는 기술 문제 또는 대상이 비어 있기 때문에 발생할 수 있습니다. 이 실패가 기술적인 문제로 인해 발생한 경우 문제 유형에 따라 다시 시도가 계속 발생할 수 있습니다(예: 내보내기 작업 만들기가 실패한 경우 최대 1시간 동안 10밀리초마다 다시 시도).

**대상자 읽기** 활동에 대한 경고는 반복 여정에 적용됩니다. **한 번** 또는 **가능한 한 빨리** 실행 일정이 있는 Live 여정의 **대상자 읽기** 활동은 무시됩니다.

**대상자 읽기**&#x200B;에 대한 경고는 프로필이 **대상자 읽기** 노드에 들어갈 때 또는 1시간 후에 해결됩니다.

**대상자 읽기 트리거 실패** 경고에 해당하는 I/O 이벤트 구독 이름은 **대상자 읽기 지연, 실패 및 오류 여정**&#x200B;입니다.

**대상 읽기** 경고 문제를 해결하려면 Experience Platform 인터페이스에서 대상 수를 확인하십시오.

### 프로필 삭제율 초과 {#alert-discard-rate}

이 경고는 지난 5분 동안 입력한 프로필에 대한 프로필 폐기 비율이 임계값을 초과하는 경우 경고합니다. 기본 임계값이 20%로 설정되어 있지만 [사용자 지정 임계값을 정의](#custom-threshold)할 수 있습니다.

경고 세부 정보 및 구성을 확인하려면 경고 이름을 클릭합니다.

![](assets/profile-discard-alert.png)

프로필을 삭제할 수 있는 몇 가지 이유가 있으며, 이는 문제 해결 방법을 알려줍니다. 몇 가지 일반적인 이유는 다음과 같습니다.

* 해당 단일 여정에서 이미 라이브되므로 시작 시 프로필이 삭제되었습니다. 이 문제를 해결하려면 프로필에 다음 이벤트가 도달하기 전에 여정을 종료할 시간이 충분한지 확인합니다.
* 프로필에 대해 ID가 설정되지 않았거나 대상자 읽기 여정에서 사용하는 네임스페이스가 해당 프로필에서 사용되지 않습니다. 이를 해결하려면 여정의 네임스페이스가 프로필에서 사용하는 ID 네임스페이스와 일치하는지 확인합니다.
* 이벤트 처리량이 초과되었습니다. 이를 해결하려면 시스템으로 들어오는 이벤트가 이러한 제한을 초과하지 않도록 하십시오.


### 사용자 정의 액션 오류율 초과 {#alert-custom-action-error-rate}

이 경고는 최근 5분 동안 성공한 HTTP 호출에 대한 사용자 지정 작업 오류의 비율이 임계값을 초과하는 경우 경고합니다. 기본 임계값이 20%로 설정되어 있지만 [사용자 지정 임계값을 정의](#custom-threshold)할 수 있습니다.

>[!NOTE]
>
>이 경고는 이전 **여정 사용자 지정 작업 실패** 경고를 대체합니다.

경고 세부 정보 및 구성을 확인하려면 경고 이름을 클릭합니다.

사용자 지정 작업 오류는 다양한 이유로 발생할 수 있습니다. 이러한 오류를 해결하려면 다음을 수행할 수 있습니다.

* 다른 여정에서 [테스트 모드](../building-journeys/testing-the-journey.md)를 사용하여 사용자 지정 작업을 확인하세요.
* 작업에 대한 오류 이유를 보려면 [여정 보고서](../reports/journey-live-report.md)를 확인하십시오.
* 여정 stepEvents를 확인하여 &quot;failureReason&quot;에 대한 자세한 정보를 찾으십시오.
* 사용자 지정 작업이 올바르게 구성되었는지 확인하고 인증이 여전히 유효한지 확인하십시오. 예를 들어 Postman을 사용하여 수동 검사를 수행합니다.
* 끝점에 연결할 수 있고 사용자 지정 작업이 사용자 지정 작업 연결 검사기를 통해 끝점에 도달할 수 있는지 확인하십시오.
* 인증 자격 증명을 확인하고 인터넷 연결을 확인합니다.

### 프로필 오류율 초과 {#alert-profile-error-rate}

이 경고는 지난 5분 동안 입력한 프로필에 대한 오류가 있는 프로필의 비율이 임계값을 초과한 경우 경고합니다. 기본 임계값이 20%로 설정되어 있지만 [사용자 지정 임계값을 정의](#custom-threshold)할 수 있습니다.

경고 세부 정보 및 구성을 확인하려면 경고 이름을 클릭합니다.

프로필 오류를 해결하려면 여정에서 프로필이 실패한 위치와 이유를 파악하기 위해 단계 이벤트의 데이터를 쿼리할 수 있습니다.

### 여정 게시됨 {#alert-journey-published}

이 경고는 전문가가 여정 캔버스에서 여정을 게시하면 알려줍니다.

조직의 여정 라이프사이클 이벤트를 추적하는 데 도움이 되는 정보 알림입니다. 일회성 알림이므로 해결 기준이 없습니다.

### 여정 완료됨 {#alert-journey-finished}

이 경고는 여정이 완료되면 알려 줍니다. 완료됨의 정의는 여정 유형에 따라 다릅니다. [여정이 완료된 것으로 간주되는 시기에 대해 자세히 알아보세요](../building-journeys/end-journey.md#journey-finished-definition).

여정 완료를 추적하는 데 도움이 되는 정보 경고입니다. 일회성 알림이므로 해결 기준이 없습니다.

### 사용자 지정 작업 한도 트리거됨 {#alert-custom-action-capping}

이 경고는 사용자 지정 작업에서 상한이 트리거되면 경고합니다. 최대 가용량(capping)은 끝점을 초과하지 않도록 외부 끝점으로 전송되는 호출 수를 제한하는 데 사용됩니다.

경고 세부 정보 및 구성을 확인하려면 경고 이름을 클릭합니다.

캡핑이 트리거되면 정의된 기간 내에 최대 API 호출 수에 도달하고 추가 호출이 조절되거나 큐에 있음을 의미합니다. [이 페이지](../action/about-custom-action-configuration.md#custom-action-enhancements-best-practices)에서 사용자 지정 작업의 최대 한도에 대해 자세히 알아보세요.

이 경고는 캡핑이 더 이상 활성화되지 않거나 평가 기간 동안 프로필이 사용자 지정 작업에 도달하지 않을 때 해결됩니다.

최대 가용량 문제를 해결하려면 다음을 수행하십시오.

* 사용자 지정 작업에 대한 최대 가용량 구성을 검토하여 제한이 사용 사례에 적합한지 확인하십시오.
* API 호출 볼륨이 예상보다 높은지 확인하고 여정 디자인 또는 최대 가용량 설정을 조정하는 것이 좋습니다.
* 외부 끝점을 모니터링하여 예상 로드를 처리할 수 있는지 확인합니다.

## 구성 경고 {#configuration-alerts}

사용자 인터페이스에서 사용할 수 있는 채널 구성 모니터링 경고 목록은 다음과 같습니다.

### AJO 도메인 DNS 레코드 누락 {#alert-dns-record-missing}

이 경고는 적절한 전달성 구성에 필요한 중요 DNS 레코드(NS 또는 CNAME)가 누락되거나 잘못 구성된 경우 알려줍니다. 이러한 레코드가 없으면 이메일 전달성이 손상될 수 있습니다.

>[!NOTE]
>
>* NS 레코드는 Adobe에 전체 하위 도메인을 위임하는 데 필수적입니다. [자세히 알아보기](../configuration/about-subdomain-delegation.md#full-subdomain-delegation)
>
>* CNAME 레코드는 CNAME 하위 도메인 설정을 지원합니다. [자세히 알아보기](../configuration/about-subdomain-delegation.md#cname-subdomain-setup)

필요한 NS 또는 CNAME 레코드가 없거나 구성 표준과 일치하지 않음을 시스템에서 감지하면 **AJO 도메인 DNS 레코드 누락** 경고가 트리거됩니다.

1. [&#x200B; 인터페이스에서 영향을 받는 &#x200B;](../configuration/delegate-subdomain.md)하위 도메인[!DNL Journey Optimizer]&#x200B;(으)로 보낼 경고를 클릭합니다.

   <!--For guidance on editing delegated subdomains, see [this section](../configuration/delegate-subdomain.md).-->

1. 레코드를 올바르게 설정하고 [하위 도메인을 제출](../configuration/delegate-subdomain.md#submit-subdomain) 위임하여 DNS 구성을 다시 수정하십시오.

   >[!NOTE]
   >
   >계속하기 전에 도메인 호스팅 솔루션에 모든 레코드가 올바르게 생성되었는지 확인하십시오.

1. 올바른 값을 모를 경우 영향을 받는 하위 도메인과 같은 이름으로 [!DNL Journey Optimizer]에 새 하위 도메인을 만들 수 있습니다. [새 하위 도메인을 설정하는 방법 알아보기](../configuration/delegate-subdomain.md#set-up-subdomain)

변경 사항으로 문제가 해결되지 않으면 다음 날 동일한 경고가 다시 트리거됩니다.

<!--The I/O event subscription name corresponding to this alert is xx. > Do we need to mention this?-->

### AJO 채널 구성 실패 {#alert-channel-config-failure}

>[!IMPORTANT]
>
>이 경고는 **사용자 지정 하위 도메인** 위임 유형을 사용하는 [전자 메일](../configuration/delegate-custom-subdomain.md) 채널 구성에만 적용됩니다. <!--Other channel types (such as SMS, push, or in-app) are not covered by this alert.-->

이 경고는 시스템 감사가 이메일 채널 구성 문제를 감지하는 경우 트리거됩니다. 이러한 문제에는 잘못 구성된 채널 설정, 잘못된 DNS 구성, 제외 목록 문제, IP 불일치 또는 이메일 게재에 영향을 줄 수 있는 기타 모든 오류가 포함될 수 있습니다.

이러한 경고를 받으면 해결 단계 가 아래에 나열됩니다.

1. [&#x200B; 인터페이스에서 영향을 받는 &#x200B;](../email/get-started-email-config.md)전자 메일 채널 구성[!DNL Journey Optimizer]&#x200B;(으)로 보낼 경고를 클릭합니다.

   채널 구성 편집에 대한 지침은 [이 섹션](../configuration/channel-surfaces.md#edit-channel-surface)을 참조하세요.

1. 제공된 구성 세부 정보 및 오류 메시지를 검토하십시오. 일반적인 실패 원인은 다음과 같습니다.

   * SPF 유효성 검사 실패
   * DKIM 유효성 검사 실패
   * MX 레코드 유효성 검사 실패
   * 잘못된 DNS 레코드

   >[!NOTE]
   >
   >가능한 구성 실패 이유는 [이 섹션](../configuration/channel-surfaces.md)에 나열되어 있습니다.

1. 문제 해결:

   * 필요에 따라 채널 구성을 업데이트합니다.
   * 경고에 언급된 특정 DNS 문제를 수정해야 할 수 있습니다.

   >[!NOTE]
   >
   >단일 도메인을 여러 채널 구성과 연결할 수 있으므로 한 채널 구성에 대한 DNS 문제를 해결하면 여러 구성에서 관련된 문제를 자동으로 해결할 수 있습니다.

변경 사항으로 문제가 해결되지 않으면 다음 날에 동일한 경고가 다시 트리거됩니다.

이메일 구성 문제를 해결할 때에는 아래 나열된 모범 사례를 염두에 두십시오.

* 즉시 조치 - 이메일 게재 중단을 방지하기 위해 구성 실패가 감지되면 즉시 해결합니다.
* 모든 구성 확인 - 경고에 영향을 받는 여러 이메일 구성이 표시되면 각각의 구성을 검토하고 수정합니다.

<!--### AJO domain certificates renewal unsuccessful {#alert-certificates-renewal}

This alert warns you if a domain certificate (CDN, tracking URL) renewal failed for a specific Journey Optimizer subdomain.-->

## 경고 관리 {#manage-alerts}

### 경고 편집

해당 줄을 클릭하여 경고의 세부 정보를 확인할 수 있습니다. 이름, 상태 및 알림 채널이 왼쪽 패널에 표시됩니다.
여정 경고의 경우 **[!UICONTROL 추가 작업]** 단추를 사용하여 편집하십시오. 그런 다음 이러한 경고에 대해 [사용자 지정 임계값](#custom-threshold)을(를) 정의할 수 있습니다.

![](assets/alert-more-actions.png){width=60%}

### 사용자 지정 임계값 정의 {#custom-threshold}

[여정 경고](#journey-alerts)에 대한 임계값을 설정할 수 있습니다. 위의 임계값 경고는 기본적으로 20%입니다.

임계값을 변경하려면 다음과 같이 하십시오.

1. **경고** 화면으로 이동
1. 업데이트할 경고의 **[!UICONTROL 추가 작업]** 단추를 클릭하십시오.
1. 새 임계값을 입력하고 확인합니다. 새 임계값은 **모두** 여정에 적용됩니다.


![](assets/alert-threshold.png){width=60%}

>[!CAUTION]
>
>임계값 수준은 모든 여정에 걸쳐 전역적이며 각 여정에 대해 개별적으로 수정할 수 없습니다.

### 경고 비활성화

기본적으로 모든 경고가 활성화됩니다. 경고를 사용하지 않으려면 **[!UICONTROL 경고 사용 안 함]** 옵션을 선택하십시오. 이 경고에 대한 모든 구독자는 더 이상 관련 알림을 받지 않습니다.


### 경고 상태

가능한 경고 상태는 다음과 같습니다.

* **[!UICONTROL 활성화됨]** - 경고가 활성화되었으며 현재 트리거 조건을 모니터링하고 있습니다.
* **[!UICONTROL 사용 안 함]** - 경고가 사용하지 않도록 설정되어 있으며 현재 트리거 조건을 모니터링하고 있지 않습니다. 이 경고에 대한 알림이 수신되지 않습니다.
* **[!UICONTROL 트리거됨]** - 경고의 트리거 조건이 현재 충족되고 있습니다.


### 구독자 보기 및 업데이트 {#manage-subscribers}

경고를 구독한 사용자 목록을 보려면 **[!UICONTROL 경고 구독자 관리]**&#x200B;를 선택하십시오.

![](assets/alert-subscribers.png){width=80%}

구독자를 추가하려면 쉼표로 구분된 전자 메일을 입력하고 **[!UICONTROL 업데이트]**&#x200B;를 선택하세요.

구독자를 제거하려면 현재 구독자에서 해당 전자 메일 주소를 삭제하고 **[!UICONTROL 업데이트]**&#x200B;를 선택하세요.

## 추가 리소스 {#additional-resources-alerts}

* [이 페이지](../building-journeys/troubleshooting.md)에서 여정 문제를 해결하는 방법을 알아보세요.
* [이 페이지](../campaigns/review-activate-campaign.md)에서 캠페인을 검토하는 방법을 알아보세요.
