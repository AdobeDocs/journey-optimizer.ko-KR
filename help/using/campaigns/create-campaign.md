---
solution: Journey Optimizer
product: journey optimizer
title: 캠페인 만들기
description: Journey Optimizer에서 캠페인을 만드는 방법을 알아봅니다
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: 만들기, 최적기, 캠페인, 표면, 메시지
exl-id: 617d623c-e038-4b5b-a367-5254116b7815
source-git-commit: bf058b13508c7ad644a3b1f63e9208740abf8602
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 22%

---

# 캠페인 만들기 {#create-campaign}

>[!NOTE]
>
>새 캠페인을 만들기 전에 표면 채널(즉, 메시지 사전 설정)과 Adobe Experience Platform 세그먼트를 사용할 준비가 되었는지 확인하십시오. 자세한 내용은 다음 섹션을 참조하십시오.
>
>* [채널 표면 생성](../configuration/channel-surfaces.md)
>* [세그먼트 시작](../segment/about-segments.md)


새 캠페인을 만들려면 **[!UICONTROL 캠페인]** 메뉴를 클릭한 다음 **[!UICONTROL 캠페인 만들기]**. 기존 라이브 캠페인을 복제하여 새 라이브 캠페인을 만들 수도 있습니다. [자세히 알아보기](modify-stop-campaign.md#duplicate)

## 캠페인 유형 및 채널을 선택합니다 {#campaigntype}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="캠페인 유형"
>abstract="보내는 날짜를 지정하여 마케팅 메시지를 보내는 경우 **예약됨** 유형이 가장 적합한 유형입니다. 단, 암호 재설정 또는 장바구니 비우기와 같은 트랜잭션 메시지를 보내려는 경우 **API 트리거** 유형이 가장 적합한 유형입니다."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_category"
>title="캠페인 범주"
>abstract="범주 값은 캠페인 유형 값에 직접 연결됩니다. **마케팅** 범주에 대한 예약 캠페인 유형과 **트랜잭션** 범주에 대한 API 트리거 유형"

1. 에서 **[!UICONTROL 속성]** 섹션에서 캠페인을 실행할 방법을 지정합니다. 사용할 수 있는 캠페인에는 두 가지 유형이 있습니다.

   * **[!UICONTROL 예약됨]**: 캠페인을 즉시 또는 지정된 날짜에 실행합니다. 예약된 캠페인은 **마케팅** 메시지 입력.

   * **[!UICONTROL API 트리거]**: api 호출을 사용하여 캠페인을 실행합니다. API로 트리거된 캠페인은 **트랜잭션** 메시지, 즉 개인이 수행한 작업에 따라 전송된 메시지: 암호 재설정, 장바구니 포기 등 [API를 사용하여 캠페인을 트리거하는 방법을 알아봅니다](api-triggered-campaigns.md)

1. 에서 **[!UICONTROL 작업]** 섹션에서 메시지를 보내는 데 사용할 채널과 채널 표면을 선택합니다.

   표면은 [시스템 관리자](../start/path/administrator.md)에 의해 정의된 구성입니다. 여기에는 헤더 매개 변수, 하위 도메인, 모바일 앱 등과 같이 메시지를 전송하기 위한 모든 기술 매개 변수가 포함되어 있습니다. [자세히 알아보기](../configuration/channel-surfaces.md).

   마케팅 캠페인 유형과 호환되는 채널 표면만 드롭다운 목록에 나열됩니다.

   ![](assets/create-campaign-action.png)

   >[!NOTE]
   >
   >푸시 알림 캠페인을 만드는 경우 **[!UICONTROL 신속한 전달 모드]**: 대용량 볼륨에서 매우 빠른 푸시 메시지를 전송할 수 있는 Journey Optimizer 추가 기능입니다. [자세히 알아보기](../push/create-push.md#rapid-delivery)

1. 클릭 **[!UICONTROL 만들기]** 캠페인을 만들려면

## 캠페인 속성을 정의합니다 {#create}

1. 에서 **[!UICONTROL 속성]** 섹션에서 캠페인의 이름과 설명을 지정합니다.

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../campaigns/content-experiment.md).-->

1. 사용자 지정 또는 핵심 데이터 사용 레이블을 캠페인에 지정하려면 **[!UICONTROL 액세스 관리]** 버튼을 클릭합니다. [개체 수준 액세스 제어(OLA)에 대한 자세한 정보](../administration/object-based-access.md)

## 메시지 만들기 및 추적 구성 {#content}

에서 **[!UICONTROL 작업]** 섹션에서 캠페인과 함께 전송할 메시지를 만듭니다.

1. 을(를) 클릭합니다. **[!UICONTROL 컨텐츠 편집]** 버튼을 클릭한 다음 메시지 콘텐츠를 만들고 디자인합니다.

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

1. 컨텐츠가 정의되면 **[!UICONTROL 컨텐츠 시뮬레이션]** 테스트 프로필로 컨텐츠를 미리 보고 테스트할 수 있습니다. [자세히 알아보기](../email/preview.md).

1. 화살표를 클릭하여 캠페인 만들기 화면으로 돌아갑니다.

   ![](assets/create-campaign-design.png)

1. 에서 **[!UICONTROL 작업 추적]** 섹션에서 수신자가 게재에 어떻게 반응하는지를 추적할지 지정합니다. 클릭 및/또는 열기를 추적할 수 있습니다.

   캠페인이 실행되면 캠페인 보고서에서 추적 결과에 액세스할 수 있습니다. [캠페인 보고서에 대해 자세히 알아보기](../reports/campaign-global-report.md)

## 대상자 정의 {#audience}

을(를) 클릭합니다. **[!UICONTROL 대상 선택]** 사용 가능한 Adobe Experience Platform 세그먼트 목록을 표시하는 단추. [세그먼트에 대해 자세히 알아보기](../segment/about-segments.md)

>[!NOTE]
>
>API로 트리거되는 캠페인의 경우 API 호출을 통해 대상을 설정해야 합니다. [자세히 알아보기](api-triggered-campaigns.md)

에서 **[!UICONTROL ID 네임스페이스]** 필드에서 선택한 세그먼트에서 개인을 식별하는 데 사용할 네임스페이스를 선택합니다. [네임스페이스에 대해 자세히 알아보기](../event/about-creating.md#select-the-namespace)

![](assets/create-campaign-namespace.png)

>[!NOTE]
>
>다른 ID 중 선택한 ID(네임스페이스)가 없는 세그먼트에 속하는 개인은 캠페인에서 타겟팅되지 않습니다.

<!--If you are are creating an API-triggered campaign, the **[!UICONTROL cURL request]** section allows you to retrieve the **[!UICONTROL Campaign ID]** to use in the API call. [Learn more](api-triggered-campaigns.md)-->

## 캠페인 예약 {#schedule}

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
>title="캠페인 직업 트리거"
>abstract="캠페인 메시지를 전송해야 하는 빈도를 정의합니다."

기본적으로 캠페인은 수동으로 활성화되면 시작되고 메시지가 한 번 전송되면 종료됩니다.

캠페인의 메시지를 보낼 빈도를 정의할 수 있습니다. 이렇게 하려면 **[!UICONTROL 작업 트리거]** 캠페인 만들기 화면의 옵션 을 사용하여 캠페인을 매일, 주별 또는 월별 중 어떤 것으로 실행해야 하는지를 지정합니다.

활성화 직후 캠페인을 실행하지 않으려면 를 사용하여 메시지를 보낼 날짜와 시간을 지정할 수 있습니다 **[!UICONTROL 캠페인 시작]** 선택 사항입니다. 다음 **[!UICONTROL 캠페인 종료]** 옵션을 사용하면 반복 캠페인의 실행을 중지할 시기를 지정할 수 있습니다.

![](assets/create-campaign-schedule.png)

캠페인이 준비되면 검토하고 게시할 수 있습니다. [자세히 알아보기](review-activate-campaign.md)
