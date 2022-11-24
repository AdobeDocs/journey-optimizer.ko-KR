---
title: 인앱 보고서
description: 인앱 보고서에서 데이터를 사용하는 방법을 알아봅니다
feature: Reporting
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 3d496efc-1bf9-4895-906c-3757f92c6fe3
source-git-commit: 6b3207f8da2f022d6094e6a2f321ac1b4f137e83
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 3%

---

# 인앱 보고서  {#inapp-report}

인앱 보고서는 캠페인 보고서에서 사용할 수 있습니다.

캠페인 보고서 페이지가 다음 탭과 함께 표시됩니다.

* [Campaign](../reports/campaign-global-report.md#campaign-live)
* [이메일](../reports/campaign-global-report.md#email-live)
* [푸시](../reports/campaign-global-report.md#push-live)
* [SMS](../reports/campaign-global-report.md#sms-live)
* [인앱](#in-app-global)

캠페인 **[!UICONTROL 글로벌 보고서]** 은 캠페인의 성공 및 오류를 자세히 설명하는 서로 다른 위젯으로 구분됩니다. 필요한 경우 각 위젯의 크기를 조정하고 삭제할 수 있습니다. 자세한 내용은 다음을 참조하십시오 [섹션](../reports/global-report.md#modify-dashboard).

Adobe Journey Optimizer에서 사용할 수 있는 모든 지표에 대한 자세한 목록은 다음을 참조하십시오 [이 페이지](../reports/global-report.md#list-of-components-global.md)

## 인앱 탭 {#inapp-global}

캠페인에서 **[!UICONTROL 글로벌 보고서]**, **[!UICONTROL 인앱]** 탭에서 캠페인에 전송된 인앱 게재와 관련된 기본 정보를 자세히 설명합니다.

![](assets/campaign_report_global_6.png)

+++인앱 보고서에 사용할 수 있는 다양한 지표 및 위젯에 대해 자세히 알아보십시오.

다음 **[!UICONTROL 인앱 성능]** KPI는 방문자와 인앱 메시지가 상호 작용하는 상대적인 기본 정보(예: )를 자세히 설명합니다.

* **[!UICONTROL 고유 노출 횟수]**: 인앱 메시지가 전달된 고유 사용자 수입니다.

* **[!UICONTROL 노출 횟수]**: 모든 사용자에게 전달된 총 인앱 메시지 수

* **[!UICONTROL 클릭률]**: 인앱 메시지에 포함된 버튼과 상호 작용한 사용자의 비율을 메시지를 본 사용자와 비교했습니다.

* **[!UICONTROL 할인]**: 수신자가 해지한 인앱 메시지의 비율입니다.

다음 **[!UICONTROL 인앱 요약]** 그래프는 관련 기간에 대한 인앱 노출의 변화를 보여줍니다.

다음 **[!UICONTROL 클릭기준 단추]** 그래프 및 표에는 버튼당 수신자 동작에 사용할 수 있는 데이터가 포함되어 있습니다.

* **[!UICONTROL 클릭 수]**: 인앱 메시지에 포함된 버튼과 상호 작용한 총 수신자 수.

* **[!UICONTROL 클릭률]**: 인앱 메시지에 포함된 버튼과 상호 작용한 사용자의 비율을 메시지를 본 사용자와 비교했습니다.
+++

**관련 항목:**

* [인앱 메시지 만들기](../in-app/create-in-app.md)
* [인앱 메시지 디자인](../in-app/design-in-app.md)
* [인앱 구성](../in-app/inapp-configuration.md)


>[!BEGINTABS]

>[!TAB 여정에 푸시 추가]

1. 여정을 열고 팔레트의 작업 섹션에서 푸시 활동을 끌어다 놓습니다.

1. 메시지(레이블, 설명, 카테고리)에 대한 기본 정보를 제공한 다음 사용할 메시지 면을 선택합니다.

>[!TAB 캠페인에 푸시 추가]

1. 예약되었거나 API가 트리거된 새 캠페인을 만들어 다음을 선택합니다. **[!UICONTROL 푸시 알림]** 를 원하는 대로 선택하고 **[!UICONTROL 앱 표면]** 를 사용하십시오.

1. **[!UICONTROL 만들기]**&#x200B;를 클릭합니다.

1. 에서 **[!UICONTROL 속성]** 섹션에서 캠페인 편집 **[!UICONTROL 제목]** 및 **[!UICONTROL 설명]**.

1. 을(를) 클릭합니다. **[!UICONTROL 대상 선택]** 사용 가능한 Adobe Experience Platform 세그먼트 목록에서 타깃팅할 대상을 정의하는 단추입니다.

1. 에서 **[!UICONTROL ID 네임스페이스]** 필드에서 선택한 세그먼트에서 개인을 식별하는 데 사용할 네임스페이스를 선택합니다.

1. 캠페인은 특정 날짜 또는 반복 빈도에 실행되도록 디자인됩니다. 구성 방법 알아보기 **[!UICONTROL 예약]** 캠페인 사용.

1. 에서 **[!UICONTROL 작업 트리거]** 메뉴에서 **[!UICONTROL 빈도]** 푸시 알림:

   * 한 번
   * 일별
   * 주별
   * 월별

>[!ENDTABS]

테스트 3:

1. 이건 시험입니다

>[!BEGINTABS]

>[!TAB 여정에 푸시 추가]

1. 여정을 열고 팔레트의 작업 섹션에서 푸시 활동을 끌어다 놓습니다.

1. 메시지(레이블, 설명, 카테고리)에 대한 기본 정보를 제공한 다음 사용할 메시지 면을 선택합니다.

>[!TAB 캠페인에 푸시 추가]

1. 예약되었거나 API가 트리거된 새 캠페인을 만들어 다음을 선택합니다. **[!UICONTROL 푸시 알림]** 를 원하는 대로 선택하고 **[!UICONTROL 앱 표면]** 를 사용하십시오.

1. **[!UICONTROL 만들기]**&#x200B;를 클릭합니다.

1. 에서 **[!UICONTROL 속성]** 섹션에서 캠페인 편집 **[!UICONTROL 제목]** 및 **[!UICONTROL 설명]**.

1. 을(를) 클릭합니다. **[!UICONTROL 대상 선택]** 사용 가능한 Adobe Experience Platform 세그먼트 목록에서 타깃팅할 대상을 정의하는 단추입니다.

1. 에서 **[!UICONTROL ID 네임스페이스]** 필드에서 선택한 세그먼트에서 개인을 식별하는 데 사용할 네임스페이스를 선택합니다.

1. 캠페인은 특정 날짜 또는 반복 빈도에 실행되도록 디자인됩니다. 구성 방법 알아보기 **[!UICONTROL 예약]** 캠페인 사용.

1. 에서 **[!UICONTROL 작업 트리거]** 메뉴에서 **[!UICONTROL 빈도]** 푸시 알림:

   * 한 번
   * 일별
   * 주별
   * 월별

>[!ENDTABS]

1. 이것은 테스트의 일부입니다
