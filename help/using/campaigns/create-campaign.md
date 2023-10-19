---
solution: Journey Optimizer
product: journey optimizer
title: 캠페인 만들기
description: Journey Optimizer에서 캠페인을 만드는 방법 알아보기
feature: Campaigns
topic: Content Management
role: User
level: Beginner
keywords: 만들기, 최적화 도구, 캠페인, 표면, 메시지
exl-id: 617d623c-e038-4b5b-a367-5254116b7815
source-git-commit: 27447578dad6bd2612989d79cd0dc8ddbe78d629
workflow-type: tm+mt
source-wordcount: '933'
ht-degree: 34%

---

# 캠페인 만들기 {#create-campaign}

>[!NOTE]
>
>새 캠페인을 만들기 전에 표면 채널(즉, 메시지 사전 설정)과 Adobe Experience Platform 대상을 사용할 준비가 되어 있는지 확인하십시오. 다음 섹션에서 자세히 알아보기:
>
>* [채널 표면 생성](../configuration/channel-surfaces.md)
>* [대상자 시작](../audience/about-audiences.md)

새 캠페인을 만들려면 **[!UICONTROL 캠페인]** 메뉴를 선택한 다음 **[!UICONTROL 캠페인 만들기]**. 기존 라이브 캠페인을 복제하여 새 캠페인을 만들 수도 있습니다. [자세히 알아보기](modify-stop-campaign.md#duplicate)

## 캠페인 유형 및 채널 선택 {#campaigntype}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="캠페인 유형"
>abstract="**예약된 캠페인**&#x200B;은 즉시 또는 지정된 날짜에 실행되며 마케팅 유형 메시지 전송을 의미합니다. **API 트리거** 캠페인은 API 호출을 사용하여 실행됩니다. 이는 마케팅 메시지(사용자 동의가 필요한 프로모션 메시지) 또는 트랜잭션 메시지(특정 상황에서 구독하지 않은 프로필에도 보낼 수 있는 비상업적 메시지)를 전송하는 것을 목표로 합니다."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_category"
>title="캠페인 범주"
>abstract="예약된 캠페인을 생성하면 **마케팅** 유형이 자동으로 선택됩니다. API로 트리거되는 캠페인의 경우 **마케팅** 메시지(사용자 동의가 필요한 프로모션 메시지)를 보낼 것인지 또는 **트랜잭션** 메시지(특정 상황에서 구독하지 않은 프로필에도 보낼 수 있는 비상업적 메시지)를 보낼 것인지 선택하십시오."

1. 다음에서 **[!UICONTROL 속성]** 섹션에서 캠페인을 실행할 방법을 지정합니다. 두 가지 유형의 캠페인을 사용할 수 있습니다.

   * **[!UICONTROL 예약됨]**: 캠페인을 즉시 또는 지정된 날짜에 실행합니다. 예약된 캠페인은 전송을 목표로 합니다. **마케팅** 메시지. 사용자 인터페이스에서 구성 및 실행됩니다.

   * **[!UICONTROL API 트리거됨]**: API 호출을 사용하여 캠페인을 실행합니다. API 트리거 캠페인은 다음 중 하나를 전송하는 것을 목표로 합니다. **마케팅**, 또는 **트랜잭션** 메시지 (예: 암호 재설정, 장바구니 구매 등 개인이 수행한 작업에 따라 전송된 메시지) [API를 사용하여 캠페인을 트리거하는 방법 알아보기](api-triggered-campaigns.md)

1. 예약된 캠페인을 생성하면 **마케팅** 유형이 자동으로 선택됩니다. API 트리거 캠페인의 경우 다음을 전송할지 여부를 선택합니다. **마케팅** 또는 **트랜잭션** 메시지.&quot;

1. 다음에서 **[!UICONTROL 작업]** 섹션에서 메시지를 보내는 데 사용할 채널과 채널 표면을 선택합니다.

   표면은 [시스템 관리자](../start/path/administrator.md)에 의해 정의된 구성입니다. 여기에는 헤더 매개 변수, 하위 도메인, 모바일 앱 등과 같이 메시지를 전송하기 위한 모든 기술 매개 변수가 포함되어 있습니다. [자세히 알아보기](../configuration/channel-surfaces.md).

   마케팅 캠페인 유형과 호환되는 채널 표면만 드롭다운 목록에 나열됩니다.

   ![](assets/create-campaign-action.png)

   >[!NOTE]
   >
   >푸시 알림 캠페인을 만드는 경우 **[!UICONTROL 빠른 전송 모드]**: 대량으로 매우 빠른 푸시 메시지 전송을 허용하는 Journey Optimizer 추가 기능입니다. [자세히 알아보기](../push/create-push.md#rapid-delivery)

1. 클릭 **[!UICONTROL 만들기]** 캠페인을 만들기 위해 사용됩니다.

## 캠페인 속성 정의 {#create}

1. 다음에서 **[!UICONTROL 속성]** 섹션에서 캠페인의 이름과 설명을 지정합니다.

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../campaigns/content-experiment.md).-->

1. 다음 **태그** 필드를 사용하면 Adobe Experience Platform 통합 태그를 캠페인에 할당할 수 있습니다. 태그를 할당하면 캠페인을 간단히 분류하고 캠페인 목록에서 편하게 검색할 수 있습니다. [태그 작업 방법 알아보기](../start/search-filter-categorize.md#tags)

1. 사용자 지정 또는 핵심 데이터 사용 레이블을 캠페인에 할당하려면 **[!UICONTROL 액세스 관리]** 단추를 클릭합니다. [OLA(Object Level Access Control)에 대해 자세히 알아보기](../administration/object-based-access.md)

## 메시지 만들기 및 추적 구성 {#content}

다음에서 **[!UICONTROL 작업]** 섹션, 캠페인과 함께 보낼 메시지를 만듭니다.

1. 다음을 클릭합니다. **[!UICONTROL 콘텐츠 편집]** 단추를 클릭한 다음 메시지 콘텐츠를 만들고 디자인합니다.

   다음 페이지에서 메시지 콘텐츠를 만드는 자세한 단계를 배웁니다.

   <table style="table-layout:fixed">
    <tr style="border: 0;">
    <td>
    <a href="../email/create-email.md">
    <img alt="리드" src="../assets/do-not-localize/email.jpg">
    </a>
    <div><a href="../email/create-email.md"><strong>이메일 만들기</strong>
    </div>
    <p>
    </td>
    <td>
    <a href="../push/create-push.md">
      <img alt="드물게" src="../assets/do-not-localize/push.jpg">
    </a>
    <div>
    <a href="../push/create-push.md"><strong>푸시 알림 만들기</strong></a>
    </div>
    <p>
    </td>
    <td>
    <a href="../sms/create-sms.md">
      <img alt="유효성 검사" src="../assets/do-not-localize/sms.jpg">
    </a>
    <div>
    <a href="../sms/create-sms.md"><strong>SMS 메시지 만들기</strong></a>
    </div>
    <p>
    </td>
    </tr>
    </table>

1. 콘텐츠가 정의되면 **[!UICONTROL 콘텐츠 시뮬레이션]** 테스트 프로필로 콘텐츠를 미리 보고 테스트하는 버튼입니다. [자세히 알아보기](../content-management/preview-test.md).

1. 화살표를 클릭하여 캠페인 만들기 화면으로 돌아갑니다.

   ![](assets/create-campaign-design.png)

1. 다음에서 **[!UICONTROL 작업 추적]** 섹션, 수신자가 게재에 반응하는 방식을 추적할지 여부를 지정합니다. 클릭 및/또는 열기를 추적할 수 있습니다.

   캠페인이 실행되면 캠페인 보고서에서 추적 결과에 액세스할 수 있습니다. [캠페인 보고서에 대해 자세히 알아보기](../reports/campaign-global-report.md)

## 대상자 정의 {#audience}

다음을 클릭합니다. **[!UICONTROL 대상자 선택]** 단추를 클릭하여 사용 가능한 Adobe Experience Platform 대상 목록을 표시합니다. [대상자에 대해 자세히 알아보기](../audience/about-audiences.md)

>[!NOTE]
>
>API 트리거 캠페인의 경우, API 호출을 통해 대상자를 설정해야 합니다. [자세히 알아보기](api-triggered-campaigns.md)

다음에서 **[!UICONTROL ID 네임스페이스]** 필드에서 선택한 세그먼트에서 개인을 식별하기 위해 사용할 네임스페이스를 선택합니다. [네임스페이스에 대해 자세히 알아보기](../event/about-creating.md#select-the-namespace)

![](assets/create-campaign-namespace.png)

>[!NOTE]
>
>다른 ID 중 선택한 ID(네임스페이스)가 없는 세그먼트에 속하는 개인은 캠페인에서 타깃팅되지 않습니다.

<!--If you are are creating an API-triggered campaign, the **[!UICONTROL cURL request]** section allows you to retrieve the **[!UICONTROL Campaign ID]** to use in the API call. [Learn more](api-triggered-campaigns.md)-->

## 캠페인 예약 {#schedule}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule"
>title="캠페인 일정"
>abstract="기본적으로 캠페인은 수동 활성화 시 시작되고 메시지가 전송된 후에 즉시 종료됩니다. 그러나 메시지를 보낼 특정 날짜와 시간을 유연하게 설정할 수 있습니다. 또한 반복 캠페인이나 API 트리거 캠페인의 종료 날짜를 지정할 수 있습니다. 액션 트리거에서 환경 설정에 맞게 메시지 전송 빈도를 구성할 수도 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_start"
>title="캠페인 시작"
>abstract="메시지를 전송해야 하는 날짜와 시간을 지정합니다."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_end"
>title="캠페인 종료"
>abstract="반복 캠페인 실행을 중지해야 하는 시점을 지정합니다."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_triggers"
>title="캠페인 액션 트리거"
>abstract="캠페인 메시지를 전송해야 하는 빈도를 정의합니다."

기본적으로 캠페인은 수동으로 활성화되면 시작되고 메시지가 한 번 전송되는 즉시 종료됩니다.

캠페인 메시지를 전송해야 하는 빈도를 정의할 수 있습니다. 이렇게 하려면 **[!UICONTROL 작업 트리거]** 캠페인 만들기 화면의 옵션을 사용하여 캠페인을 일별, 주별 또는 월별 단위로 실행할지 지정할 수 있습니다.

활성화 직후 캠페인을 실행하지 않으려면 다음을 사용하여 메시지를 전송해야 하는 날짜 및 시간을 지정할 수 있습니다. **[!UICONTROL 캠페인 시작]** 옵션을 선택합니다. 다음 **[!UICONTROL 캠페인 종료]** 옵션을 사용하면 반복 캠페인의 실행을 중지해야 하는 시기를 지정할 수 있습니다.

![](assets/create-campaign-schedule.png)

캠페인이 준비되면 검토하고 게시할 수 있습니다. [자세히 알아보기](review-activate-campaign.md)
