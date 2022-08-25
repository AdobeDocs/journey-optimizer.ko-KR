---
title: 캠페인 라이브 보고서
description: Campaign 라이브 보고서에서 데이터를 사용하는 방법을 알아봅니다
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 925494b6-e08a-4bd3-8a2f-96a5d9cbc387
source-git-commit: 711fdf1dce0688d2e21d405a4e3e8777612b2f3b
workflow-type: tm+mt
source-wordcount: '570'
ht-degree: 1%

---

# 캠페인 라이브 보고서 {#campaign-live-report}

캠페인 라이브 보고서는 **[!UICONTROL Reports]** 버튼을 클릭합니다.

![](assets/campaign_report_1.png)

을(를) 선택한 후 **[!UICONTROL Last 24hrs]** 탭, 캠페인 **[!UICONTROL Live report]** 페이지는 다음 탭에 표시됩니다.

* [Campaign](#campaign-live)
* [이메일](#email-live)
* [푸시](#push-live)

캠페인 **[!UICONTROL Live report]** 은 캠페인의 성공 및 오류를 자세히 설명하는 서로 다른 위젯으로 구분됩니다. 필요한 경우 각 위젯의 크기를 조정하고 삭제할 수 있습니다. 자세한 내용은 다음을 참조하십시오 [섹션](../reports/live-report.md#modify-dashboard).

## 캠페인 탭 {#campaign-global}

### 제공 {#delivery-global}

다음 **[!UICONTROL Campaign Statistics]** 위젯은 캠페인과 관련된 주요 정보를 자세히 설명합니다.

* **[!UICONTROL Entered profiles]**: 여정을 시작한 프로필 수입니다.

<!--
### Experimentation tab (#experimentation-live)

From your Campaign **[!UICONTROL Live report]**, the **[!UICONTROL Experimentation]** tab details the main information relative to how each variant is performing and if there is was winner during the test.
-->
## 이메일 탭 {#email-live}

캠페인에서 **[!UICONTROL Live report]**, **[!UICONTROL Email]** 탭 은 campaign에서 전송된 이메일 게재와 관련된 주요 정보를 자세히 설명합니다.

다음 **[!UICONTROL Email Sending Statistics]** 위젯은 메시지에 대한 주요 정보를 자세히 설명합니다.

* **[!UICONTROL Delivered]**: 보낸 총 메시지 수와 관련하여 성공적으로 보낸 메시지 수입니다.

* **[!UICONTROL Bounces]**: 총 보낸 메시지 수와 관련하여 게재 및 자동 반환 처리 중에 누적된 총 오류 수입니다.

* **[!UICONTROL Errors]**: 게재 중에 발생한 총 오류로 인해 프로필이 전송되지 않았습니다.

다음 **[!UICONTROL Sending metrics by Email]** 테이블 및 **[!UICONTROL Email Summary]** 그래프는 게재 성공에 대해 자세히 설명합니다.

* **[!UICONTROL Sent]**: 게재에 대한 총 전송 수입니다.

* **[!UICONTROL Delivered]**: 보낸 총 메시지 수와 관련하여 성공적으로 보낸 메시지 수입니다.

* **[!UICONTROL Bounces]**: 총 보낸 메시지 수와 관련하여 게재 및 자동 반환 처리 중에 누적된 총 오류 수입니다.

* **[!UICONTROL Errors]**: 게재 중에 발생한 총 오류로 인해 프로필이 전송되지 않았습니다.

* **[!UICONTROL Opens]**: 게재에서 메시지를 연 횟수입니다.

* **[!UICONTROL Clicks]**: 게재에서 콘텐츠를 클릭한 횟수입니다.

* **[!UICONTROL Unsubscribe]**: 구독 취소 링크에 대한 클릭 수입니다.

* **[!UICONTROL Spam complaints]**: 메시지가 스팸 또는 정크 메일로 선언된 횟수입니다.

다음 **[!UICONTROL Bounce Reasons]**, **[!UICONTROL Bounce categories]** 및 **[!UICONTROL Hard and bounce - by Email]** 위젯에는 다음과 같이 바운스된 메시지와 관련하여 사용할 수 있는 데이터가 포함되어 있습니다.

* **[!UICONTROL Hard bounce]**: 잘못된 이메일 주소와 같은 총 영구 오류 수입니다. 여기에는 알 수 없는 사용자와 같이 주소가 유효하지 않다는 오류 메시지가 명시적으로 표시됩니다.

* **[!UICONTROL Soft bounce]**: 전체 받은 편지함과 같은 총 임시 오류 수입니다.

* **[!UICONTROL Ignored]**: 부재 중 또는 기술 오류(예: 발신자 유형이 postmaster인 경우)와 같은 총 임시 수입니다.

다음 **[!UICONTROL Error Reasons]** 및 **[!UICONTROL Exclude Reasons]** 그래프 및 표를 사용하면 게재 중에 발생한 오류와 제외를 확인할 수 있습니다.

다음 **[!UICONTROL Email - Top recipient domain]** 전자 메일을 여는 데 받는 사람이 가장 많이 사용하는 도메인을 그래프 및 표 세부 사항입니다.

## 푸시 탭 {#push-live}

캠페인에서 **[!UICONTROL Live report]**, **[!UICONTROL Push]** 탭 은 campaign에서 전송된 푸시 게재와 관련된 기본 정보를 자세히 설명합니다.

**[!UICONTROL Push notification sending performance]**, **[!UICONTROL Push notification summary]** 및 **[!UICONTROL Sending metrics - by Push]** 위젯은 메시지에 대한 기본 정보를 자세히 설명합니다.

* **[!UICONTROL Sent]**: 게재에 대한 총 전송 수입니다.

* **[!UICONTROL Delivered]**: 보낸 총 메시지 수와 관련하여 성공적으로 보낸 메시지 수입니다.

* **[!UICONTROL Bounces]**: 총 보낸 메시지 수와 관련하여 게재 및 자동 반환 처리 중에 누적된 총 오류 수입니다.

* **[!UICONTROL Errors]**: 게재 중에 발생한 총 오류로 인해 프로필이 전송되지 않았습니다.

* **[!UICONTROL Opens]**: 게재에서 메시지를 연 횟수입니다.

* **[!UICONTROL Actions]**: 전달된 푸시 알림에 대한 총 작업 수(예: 단추 클릭 또는 취소)

* **[!UICONTROL Engagements]**: 이 푸시 알림에 대한 총 열기 및 작업 수(즉, 프로필이 푸시를 열었는지 또는 단추를 클릭했는지 여부)입니다.

다음 **[!UICONTROL Error Reasons]** 및 **[!UICONTROL Exclude Reasons]** 그래프 및 표를 사용하면 게재 중에 발생한 오류와 제외를 확인할 수 있습니다.

다음 **[!UICONTROL Sending statistics - Failed]** 위젯을 사용하면 발생한 오류 및 반송 수를 확인할 수 있습니다.

다음 **[!UICONTROL Tracking by platform]**, **[!UICONTROL Sending by platform]** 및 **[!UICONTROL Breakdown by platform]** 그래프 및 표는 운영 시스템에 따라 푸시 알림의 성공을 자세히 설명합니다.
