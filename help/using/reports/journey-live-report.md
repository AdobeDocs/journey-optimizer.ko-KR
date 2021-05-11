---
title: 여정 라이브 보고서
description: 여정 라이브 보고서의 데이터를 사용하는 방법 학습
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '676'
ht-degree: 0%

---

# 여정 라이브 보고서 {#journey-live-report}

![](../assets/do-not-localize/badge.png)

여정 라이브 보고서는 **[!UICONTROL Live report]** 단추를 사용하여 여정에서 직접 액세스할 수 있습니다.

![](../assets/report_1.png)

여정 **[!UICONTROL Live report]** 페이지는 다음 탭으로 표시됩니다.

* [여정](#journey-live)
* [이메일](#email-live)
* [푸시](#push-live)

여정 **[!UICONTROL Live report]**&#x200B;은(는) 여정의 성공 및 오류를 자세히 설명하는 다른 위젯으로 나누어집니다. 필요한 경우 각 위젯의 크기를 조정하고 삭제할 수 있습니다. 이에 대한 자세한 내용은 이 [섹션](live-report.md#modify-dashboard)을 참조하십시오.

## 여정 탭 {#journey-live}

여정 **[!UICONTROL Live report]**&#x200B;에서 **[!UICONTROL Journey]** 탭에서는 여정에 대한 가장 중요한 추적 데이터를 명확하게 볼 수 있습니다.

![](../assets/report_journey_2.png)

**[!UICONTROL Journey`s performance]** 여정을 단계별로 대상 프로필의 경로를 볼 수 있습니다.

**[!UICONTROL Journey`s statistics]** 위젯에는 다음 KPI가 표시됩니다.

* **[!UICONTROL Entered profiles]**:여정 시작 이벤트에 도달한 총 개인 수입니다.

* **[!UICONTROL Exited profiles]**:여정을 종료한 총 개인 수입니다.

* **[!UICONTROL Failed individual journey]**:성공적으로 실행되지 않은 총 개별 여정 수입니다.

![](../assets/report_journey_3.png)

**[!UICONTROL Event executed over the last 24 hours]**, **[!UICONTROL Events executed]** 및 **[!UICONTROL Events]** 위젯을 사용하면 요약 번호, 그래프 및 표를 통해 어떤 이벤트가 성공적으로 실행되었는지 확인할 수 있습니다.

![](../assets/report_journey_4.png)

**[!UICONTROL Action executed over the last 24 hours]** 위젯 **[!UICONTROL Actions executed and errors]** 은 작업이 트리거될 때 발생한 가장 성공적인 작업 및 오류를 나타냅니다. 작업 그래프, 테이블 및 요약 번호에는 다음과 같은 작업에 사용할 수 있는 데이터가 포함됩니다.

* **[!UICONTROL Actions successfully executed]**:여정에 대해 성공적으로 실행된 총 작업 수입니다.

* **[!UICONTROL Error in action]**:작업에 대해 발생한 총 오류 수입니다.

## 이메일 탭 {#email-live}

여정 **[!UICONTROL Live report]**&#x200B;에서 **[!UICONTROL Email]** 탭은 여정에서 보낸 이메일 게재와 관련된 기본 정보를 자세히 설명합니다.

특정 이메일 배달에 대한 자세한 보고서는 [실시간 보고서 이메일](email-live-report.md) 섹션을 참조하십시오.

![](../assets/report_email_1.png)

**[!UICONTROL Sending Statistics]** 및 **[!UICONTROL Sending metrics by Email]** 위젯은 배달의 성공 여부를 자세히 설명합니다.

* **[!UICONTROL Delivered]**:보낸 총 메시지 수와 관련하여 성공적으로 보낸 메시지 수입니다.

* **[!UICONTROL Bounces]**:총 보낸 메시지 수와 관련하여 배달 중 및 자동 반환 처리 중에 누적된 총 오류 수입니다.

* **[!UICONTROL Errors]**:배달 중에 발생한 총 오류 수 때문에 프로필로 전송되지 않습니다.

<!--Hard and bounce - by Email-->

**[!UICONTROL Email summary]** 그래프는 메시지와 관련된 기본 정보를 자세히 설명합니다.

* **[!UICONTROL Sent]**:배달에 대한 총 전송 수입니다.

* **[!UICONTROL Delivered]**:보낸 총 메시지 수와 관련하여 성공적으로 보낸 메시지 수입니다.

* **[!UICONTROL Bounces]**:총 보낸 메시지 수와 관련하여 배달 중 및 자동 반환 처리 중에 누적된 총 오류 수입니다.

* **[!UICONTROL Errors]**:배달 중에 발생한 총 오류 수 때문에 프로필로 전송되지 않습니다.

* **[!UICONTROL Opens]**:배달에서 메시지를 연 횟수입니다.

* **[!UICONTROL Clicks]**:게재에서 컨텐츠를 클릭한 횟수입니다.

![](../assets/report_email_2.png)

**[!UICONTROL Bounce Reasons]** 및 **[!UICONTROL Bounce categories]** 위젯에는 바운스된 메시지와 관련하여 사용할 수 있는 다음과 같은 데이터가 포함됩니다.

* **[!UICONTROL Hard bounce]**:잘못된 이메일 주소와 같은 총 영구 오류 수입니다. 이 작업에는 주소를 알 수 없는 사용자 등의 유효하지 않다고 명시적으로 표시하는 오류 메시지가 포함됩니다.

* **[!UICONTROL Soft bounce]**:전체 받은 편지함과 같은 총 임시 오류 수입니다.

* **[!UICONTROL Ignored]**:보낸 사람 유형이 postmaster인 경우와 같이, 부재 중 또는 기술 오류와 같은 총 임시 수입니다.

**[!UICONTROL Error Reasons]** 그래프 및 표를 사용하면 배달 중 발생한 오류를 확인할 수 있습니다.

## 푸시 탭 {#push-live}

여정 **[!UICONTROL Live report]**&#x200B;에서 **[!UICONTROL Push]** 탭은 여정에서 전송된 푸시 배달과 관련된 기본 정보를 자세히 설명합니다.

특정 푸시 전달에 대한 자세한 보고서는 [라이브 보고서 푸시](push-live-report.md) 섹션을 참조하십시오.

![](../assets/report_push_1.png)

**[!UICONTROL Push notification sending performance]**,  **[!UICONTROL Push notification summary]** 및  **[!UICONTROL Sending metrics - by Push]** 위젯은 메시지와 관련된 기본 정보를 자세히 설명합니다.

* **[!UICONTROL Sent]**:배달에 대한 총 전송 수입니다.

* **[!UICONTROL Delivered]**:보낸 총 메시지 수와 관련하여 성공적으로 보낸 메시지 수입니다.

* **[!UICONTROL Bounces]**:총 보낸 메시지 수와 관련하여 배달 중 및 자동 반환 처리 중에 누적된 총 오류 수입니다.

* **[!UICONTROL Errors]**:배달 중에 발생한 총 오류 수 때문에 프로필로 전송되지 않습니다.

* **[!UICONTROL Opens]**:배달에서 메시지를 연 횟수입니다.

* **[!UICONTROL Actions]**:배달된 푸시 알림에 대한 총 작업 수(예: 단추 클릭 또는 종료).

* **[!UICONTROL Engagements]**:이 푸시 알림에 대한 총 열기 및 작업 수입니다(예: 프로필이 푸시를 열었거나 단추를 클릭했을 때).

**[!UICONTROL Error Reasons]** 그래프 및 표를 사용하면 배달 중 발생한 오류를 확인할 수 있습니다.

![](../assets/report_push_2.png)

**[!UICONTROL Tracking by platform]**, **[!UICONTROL Sending by platform]** 및 **[!UICONTROL Breakdown by platform]** 그래프 및 표는 운영 체제에 따라 푸시 알림의 성공 여부를 자세히 설명합니다.

**[!UICONTROL Sending statistics - Failed]** 위젯을 사용하면 발생한 오류와 바운스 수를 확인할 수 있습니다.
