---
solution: Journey Optimizer
product: journey optimizer
title: 캠페인 시작
description: Journey Optimizer의 캠페인에 대해 자세히 알아보기
feature: Campaigns
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
keywords: 캠페인, 방법 , 시작, Optimizer
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: 27de3d2171e6f6575eb66ada20f951f6cb3abc98
workflow-type: tm+mt
source-wordcount: '1513'
ht-degree: 98%

---

# 캠페인 시작 {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule"
>title="캠페인 예약"
>abstract="기본적으로 캠페인은 수동 활성화를 통해 시작되고 메시지가 한 번 발송되는 즉시 종료됩니다. 메시지를 전송할 특정 날짜와 시간을 유연하게 설정할 수 있습니다. 또한 반복적인 액션 캠페인의 종료 날짜를 지정할 수 있습니다. 액션 트리거에서는 환경 설정에 따라 메시지 전송 빈도를 구성할 수도 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_start"
>title="캠페인 시작"
>abstract="메시지를 전송해야 하는 날짜와 시간을 지정하십시오."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_end"
>title="캠페인 종료"
>abstract="반복 캠페인 실행을 중지해야 하는 시점을 지정하십시오."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_triggers"
>title="캠페인 액션 트리거"
>abstract="캠페인 메시지를 전송해야 하는 빈도를 정의하십시오."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_throttling"
>title="속도 제어"
>abstract="원하는 속도 제한을 지정하여 캠페인에 대한 속도 제어를 설정합니다. 이 기능은 랜딩 페이지나 고객 지원 센터 플랫폼과 같은 다운스트림 시스템의 오버로드를 방지하는 데 특히 유용합니다."

>[!CONTEXTUALHELP]
>id="ajo_homepage_card3"
>title="캠페인 만들기"
>abstract="**Adobe Journey Optimizer**&#x200B;로 다양한 채널을 사용하는 특정 대상자에 일회성 콘텐츠를 게재할 수 있습니다. 여정을 사용할 때 작업은 순서대로 실행됩니다. 캠페인을 사용하면 작업을 동시에 즉시 또는 지정한 일정에 따라 수행합니다."

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="캠페인"
>abstract="캠페인을 만들어 다양한 채널을 통해 특정 대상자에게 일회성 콘텐츠를 게재할 수 있습니다. 캠페인을 만들기 전에 채널 구성과 Adobe Experience Platform 대상자를 사용할 준비가 되었는지 확인하십시오."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="캠페인 유형"
>abstract="캠페인 유형을 선택합니다. 사용 가능한 채널은 선택한 유형에 따라 다릅니다. <br>**예약된 캠페인**(액션 캠페인) – 특정 시간에 실행되도록 예약할 수 있는 간단한 일회성 일괄 커뮤니케이션에 적합합니다.<br>**API 트리거 캠페인** – API 호출을 통해 활성화되어 외부 시스템에서 직접 자동화된 이벤트 기반 메시지를 활성화합니다.<br>**오케스트레이션된 캠페인** – 시각적으로 명확한 드래그 앤 드롭 캔버스를 제공하여 대상자 세분화부터 채널 전반의 개인화된 메시지 게재에 이르기까지 복잡하고 다단계적인 마케팅 워크플로를 설계하고 자동화합니다."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_orchestration"
>title="캠페인"
>abstract="세분화 플로우를 만들고 크로스 채널 메시지를 작성하고 캠페인을 기획합니다. 지원되는 채널: 이메일, SMS, 푸시 알림."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_scheduled_marketing"
>title="캠페인"
>abstract="단일 또는 반복 아웃바운드 게재 또는 지속적인 인바운드 액션을 게재합니다."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_scheduled_transactional"
>title="캠페인"
>abstract="단일 또는 반복 아웃바운드 트랜잭션 액션을 게재합니다."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_api_marketing"
>title="캠페인"
>abstract="타깃 대상자에게 개인화된 마케팅 커뮤니케이션을 게재합니다. 지원 채널: 이메일, SMS, 푸시 알림."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_api_transactional"
>title="캠페인"
>abstract="개별 프로필이나 프로필 그룹에 트랜잭션 커뮤니케이션을 보내 보세요. 지원 채널: 이메일, SMS, 푸시 알림."

Adobe Journey Optimizer를 사용하면 여러 채널에서 특정 대상자에게 타겟팅된 일회성 콘텐츠를 제공할 수 있습니다. 캠페인을 활용하면 여러 마케팅 활동을 동시에 조정하여 적절한 시기에 적절한 메시지를 대상자에게 전달할 수 있습니다.

이 안내서에서는 캠페인의 기본 사항을 이해하고, 사용 사례에 맞는 캠페인 유형을 선택하며, 효과적인 고객 경험을 제공하는 캠페인을 자신 있게 디자인하는 데 도움이 되는 명확한 로드맵을 제공합니다.

## 캠페인이란 무엇인가요?

**캠페인**&#x200B;은 하나 이상의 채널을 통해 특정 대상자에게 콘텐츠를 전달하는 조정된 마케팅 액션입니다. 여정에서는 액션이 순차적으로 실행되는 반면, 캠페인에서는 액션이 즉시 또는 정해진 일정에 따라 동시에 실행됩니다.

[!DNL Journey Optimizer] 캠페인을 사용하여 다음을 수행할 수 있습니다.

* 타겟팅된 대상자 세그먼트에 **일회성 또는 반복 콘텐츠** 게재
* 이메일, 푸시, SMS, 인앱, 웹 등을 통해 **조정된 멀티채널 커뮤니케이션** 실행
* 실시간 이벤트 기반 메시지를 위해 API 호출을 통해 **자동화된 응답** 트리거
* 시각적 오케스트레이션 도구를 사용하여 **복잡한 마케팅 워크플로** 디자인

![](assets/gs-campaigns.png)

➡️ **구축을 시작할 준비가 되셨나요?** [몇 분 만에 첫 번째 캠페인을 만듭니다](create-campaign.md).

## 캠페인 유형 선택 {#campaign-types}

**캠페인 구축을 시작하기 전에** 사용 사례에 적합한 캠페인 유형을 이해하는 것이 중요합니다. Adobe Journey Optimizer는 서로 다른 시나리오와 활성화 메커니즘에 맞춰 설계된 세 가지 캠페인 유형을 지원합니다.

![](assets/campaign-modal.png)

>[!BEGINTABS]

>[!TAB 오케스트레이션된 캠페인]

**사용 시점:** 복잡한 다단계 마케팅 워크플로

**오케스트레이션된 캠페인**&#x200B;은 정교한 마케팅 워크플로를 디자인하고 자동화할 수 있는 시각적인 드래그 앤 드롭 캔버스를 제공합니다. 대상자 세분화부터 다양한 채널을 통한 개인화된 메시지 전달까지, 모든 것이 빠른 속도와 손쉬운 관리를 위해 설계된 직관적인 단일 환경에서 이루어집니다.

**적합한 용도:** 여러 단계로 구성된 고객 참여 프로그램, 복잡한 세분화 및 타겟팅 전략, 크로스 채널 캠페인 오케스트레이션, 브랜드 주도형 대규모 마케팅, 의사 결정 지점이 여러 개인 고급 워크플로 자동화.

➡️ [오케스트레이션된 캠페인에 대해 알아보기](../orchestrated/gs-orchestrated-campaigns.md)

>[!TAB 액션 캠페인(예약됨)]

**사용 시점:** 간단하고 예약된 일괄 커뮤니케이션

**액션 캠페인**(예약 캠페인이라고도 함)은 특정 시간에 실행되는 간단한 일회성 또는 반복적인 일괄 커뮤니케이션에 적합합니다.

**두 가지 범주:**

* **마케팅** - 프로모션 오퍼, 참여 캠페인, 공지, 법적 고지 또는 정책 업데이트. 수신자가 옵트인해야 합니다.
* **트랜잭션** - 중단, 긴급 상황, 취소. 옵트인이 필요하지 않습니다.

**적합한 용도:** 고객 세그먼트별 월간 뉴스레터, 시기적절한 프로모션 공지, 시즌별 마케팅 캠페인, 제품 출시 안내, 서비스 중단 알림.

➡️ [액션 캠페인에 대해 알아보기](create-campaign.md)

>[!TAB API 트리거 캠페인]

**사용 시점:** 외부 시스템과의 실시간 이벤트 기반 메시지

**API 트리거 캠페인**&#x200B;은 API 호출을 통해 활성화되어 외부 시스템에서 직접 자동화된 메시지를 보낼 수 있습니다. 이러한 캠페인은 프로필 속성과 API 페이로드의 실시간 컨텍스트 데이터를 모두 사용하여 개인화를 지원합니다.

**두 가지 범주:**

* **마케팅** - 타겟팅된 고객을 위한 맞춤형 마케팅 커뮤니케이션
* **트랜잭션** - 개별 액션(암호 재설정, 장바구니 구매 등) 후 표시되는 메시지

**적합한 용도:** 암호 재설정 확인, 장바구니 포기 복구, 주문 확인 및 배송 업데이트, 계정 활동 알림, 실시간 맞춤 추천.

➡️ [API 트리거 캠페인에 대해 알아보기](api-triggered-campaigns.md)

>[!ENDTABS]

>[!NOTE]
>
>어떤 유형을 선택해야 할지 모르시겠나요? 예약된 일괄 커뮤니케이션을 위한 **액션 캠페인** 또는 실시간 메시지를 위한 **API 트리거 캠페인**&#x200B;으로 시작하세요. 이러한 캠페인은 가장 일반적인 사용 사례를 다룹니다.

## 전제 조건 {#prerequisites}

캠페인을 시작하기 전에 다음 사항들이 준비되어 있는지 확인하세요.

* **대상자** - 캠페인을 만들기 전에 Adobe Experience Platform에서 대상자를 사용할 수 있어야 합니다. [대상자 시작하기 →](../audience/about-audiences.md)

* **채널 구성** - 사용할 채널에 대한 채널 구성(사전 설정)을 만들어야 합니다. [채널 구성 설정 →](../configuration/channel-surfaces.md)

* **권한** - 캠페인 유형에 따라 적절한 권한이 필요합니다. 캠페인 기능에 액세스할 수 없는 경우 관리자에게 문의하세요. [기본 제공 역할에 대해 알아보기→](../administration/ootb-product-profiles.md)

  +++캠페인 권한 목록

  | 캠페인 유형 | 권한 |
  |-------------|---------------|
  | **작업 캠페인** 및 **API 트리거 캠페인** | 캠페인 전체 관리자<br>캠페인 승인자<br>캠페인 관리자<br>캠페인 확인자 |
  | **오케스트레이션된 캠페인** | 오케스트레이션된 캠페인 전체 관리자<br>오케스트레이션된 캠페인 승인자<br>오케스트레이션된 캠페인 관리자<br>오케스트레이션된 캠페인 확인자 |

  +++

  +++캠페인 권한을 할당하는 방법

   1. [!DNL Permissions] 제품의 **[!UICONTROL 역할]** 탭으로 이동하여 기본 제공 캠페인 관련 **[!UICONTROL 역할]** 중 하나를 선택합니다.

   1. **[!UICONTROL 사용자]** 탭에서 **[!UICONTROL 사용자 추가]**&#x200B;를 클릭합니다.

   1. 사용자 이름 또는 이메일 주소를 입력하거나 목록에서 사용자를 선택하고 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

  이전에 사용자를 생성하지 않은 경우 [사용자 설명서 추가](https://experienceleague.adobe.com/ko/docs/experience-platform/access-control/ui/users){target="_blank"}를 참조하십시오.

  그러면 사용자가 인스턴스로 리디렉션되는 이메일을 받게 됩니다.

  +++

## 캠페인 생성 워크플로 {#workflow}

성공적인 캠페인을 구축하려면 명확하고 반복 가능한 프로세스가 필요합니다. 다음은 단계별 워크플로입니다.

+++&#x200B;1. 캠페인을 계획합니다

시작하기 전에 목표를 명확히 하세요.

* **목표가 무엇인가요?**(예: 전환율 개선, 참여도 향상, 고객에게 알림 전송)
* **대상자는 누구인가요?**(예: Adobe Experience Platform에서 빌드 또는 선택)
* **적합한 캠페인 유형은 무엇인가요?**(위의 [캠페인 유형](#campaign-types) 참조)
* **어떤 채널을 사용하나요?**(이메일, 푸시, SMS, 인앱, 웹 등) → [캠페인 유형별로 지원되는 채널 보기](../channels/gs-channels.md#channels)
* **언제 실행해야 하나요?**(즉시, 예약됨 또는 API 트리거)

+++

+++&#x200B;2. 캠페인 속성 구성

캠페인 기반을 설정합니다.

1. 캠페인을 쉽게 식별할 수 있도록 **이름과 설명 입력**
2. **캠페인 유형 선택**(액션, API 트리거 또는 오케스트레이션)
3. **대상자 선택**
4. 충돌 관리를 사용하는 경우 **우선순위 설정**
5. **일정 구성**(액션 캠페인의 경우) 또는 API 세부 정보(API 트리거의 경우)

**유형별 안내서:** [액션 캠페인 속성](campaign-properties.md) | [API 트리거 캠페인 속성](api-triggered-campaign-properties.md) | [오케스트레이션된 캠페인 설정](../orchestrated/create-orchestrated-campaign.md)

+++

+++&#x200B;3. 콘텐츠 디자인

대상자를 위한 매력적인 메시지를 만듭니다.

* 다양한 이메일 경험을 위해 **이메일 디자이너** 사용
* 이미지와 딥링크로 **푸시 알림** 구성
* 개인화를 사용하여 **SMS/MMS 메시지** 디자인
* **인앱** 및 **웹** 경험 만들기
* 프로필 속성과 컨텍스트 데이터를 사용하여 **개인화** 추가

**유형별 안내서:** [액션 캠페인 콘텐츠](campaign-content.md) | [API 트리거 캠페인 콘텐츠](api-triggered-campaign-content.md) | [오케스트레이션된 캠페인 콘텐츠](../orchestrated/create-orchestrated-campaign.md)

+++

+++&#x200B;4. 검토 및 테스트

활성화하기 전에 항상 캠페인을 검토합니다.

* 테스트 프로필을 사용하여 **콘텐츠 미리 보기**
* 올바른 대상자를 보장하기 위해 **타겟팅 확인**
* **일정 확인** 및 활성화 설정
* 승인 워크플로를 사용하는 경우 **승인 요청**
* 시드 목록을 사용하여 **전달성 테스트**

**유형별 안내서:** [액션 캠페인 검토](review-activate-campaign.md) | [API 트리거 캠페인 검토](review-activate-api-triggered-campaign.md) | [오케스트레이션된 캠페인 검토](../orchestrated/create-orchestrated-campaign.md)

+++

+++&#x200B;5. 캠페인 활성화

검토가 완료되면 캠페인을 활성화합니다.

* **수동 활성화** - 즉시 또는 예약된 시간에 활성화
* **API 활성화** - API 트리거 캠페인의 경우 활성화 엔드포인트 사용
* **승인 프로세스** - 필요한 경우 이해 당사자 승인 대기

참고: 활성 캠페인은 편집할 수 없습니다(변경하려면 복제해야 함).

**유형별 안내서:** [액션 캠페인 활성화](review-activate-campaign.md) | [API 트리거 캠페인 활성화](review-activate-api-triggered-campaign.md) | [오케스트레이션된 캠페인 활성화](../orchestrated/create-orchestrated-campaign.md)

+++

+++&#x200B;6. 모니터링 및 분석

캠페인의 성과를 추적합니다.

* 캠페인 보고서 및 분석 보기
* 게재 비율 및 참여 지표 모니터링
* 오류 및 바운스 추적
* 전환 및 ROI 분석
* 최적화에 인사이트 사용

**유형별 안내서:** [액션 캠페인 보고서](../reports/campaign-global-report-cja.md) | [API 트리거 캠페인 모니터링](api-triggered-campaigns.md#monitor) | [오케스트레이션된 캠페인 분석](../orchestrated/create-orchestrated-campaign.md)

+++

## 더 자세히 알아보기 {#get-started-types}

이제 [!DNL Journey Optimizer]에서 캠페인에 대해 이해하셨으니 캠페인 유형을 선택하여 시작해 보세요.

<table style="table-layout:fixed"><tr style="border: 0; text-align: center;">
<td><a href="create-campaign.md"><img width="70%" alt="액션 캠페인" src="assets/do-not-localize/gs-action-campaign.png"></a><br/><a href="create-campaign.md">액션 캠페인</a></td>
<td><a href="api-triggered-campaigns.md"><img width="70%" alt="sms" src="assets/do-not-localize/gs-api-triggered-campaign.png"></a><br/><a href="api-triggered-campaigns.md">API 트리거 캠페인</a></td>
<td><a href="../orchestrated/gs-orchestrated-campaigns.md"><img width="70%" alt="푸시" src="assets/do-not-localize/gs-orchestrated-campaign.png"></a><a href="../orchestrated/gs-orchestrated-campaigns.md">오케스트레이션된 캠페인</a></td>
</tr></table>

캠페인에 익숙해지면 다음과 같은 강력한 기능을 활용해 보세요.

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/calendar-alt.svg)

**예약 및 시간**

특정 날짜/시간에 맞춰 캠페인을 예약하고, 반복 게재를 설정하며, 전송 시간을 최적화하여 최대 효과를 얻습니다. (액션 및 API 트리거 캠페인)

[예약에 대해 알아보기](campaign-schedule.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg)

**속도 제어**

랜딩 페이지나 고객 지원 센터 플랫폼과 같은 하위 시스템에 과부하가 걸리는 것을 방지하기 위해 메시지 처리량을 제한합니다. (액션 및 API 트리거 캠페인)

[제어 속도 제한](create-campaign.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg)

**대상자 타겟팅**

Adobe Experience Platform의 특정 대상자를 정확하게 타겟팅하고 대상자 선별을 동적으로 관리합니다.

[캠페인 대상자 선택](campaign-audience.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg)

**승인 워크플로**

캠페인을 시작하기 전에 검토 및 승인 프로세스를 구현하여 품질과 규정 준수를 보장합니다. (액션 및 API 트리거 캠페인)

[검토 및 활성화](review-activate-campaign.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/clock.svg)

**방해 금지 시간**

고객이 지정한 시간대에는 메시지 전달을 피함으로써 고객의 선호도를 존중합니다. (액션 및 API 트리거 캠페인)

[방해 금지 시간 구성](quiet-hours.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg)

**최적화**

타겟팅 규칙과 콘텐츠 실험을 활용하여 개인화된 콘텐츠를 제공하고 참여도를 극대화합니다.

[캠페인 최적화](../content-management/gs-message-optimization.md)
:::

::::
