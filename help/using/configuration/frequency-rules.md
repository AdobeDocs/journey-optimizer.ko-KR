---
title: 빈도 규칙
description: 빈도 규칙 정의 방법을 알아봅니다
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 49248fb6-5a91-45b2-9de8-2f078d59c0fc
source-git-commit: f1ac47a0cb405eaadc5428e7e5479eaf776d7abe
workflow-type: tm+mt
source-wordcount: '762'
ht-degree: 1%

---

# 메시지 빈도 규칙 {#frequency-rules}

[!DNL Journey Optimizer] 에서는 메시지 및 작업에서 과도하게 요청된 프로필을 자동으로 제외하는 크로스 채널 규칙을 설정하여 사용자가 메시지를 수신하거나 여정에 입력하는 빈도를 제어할 수 있습니다.

예를 들어 브랜드에서 고객에게 매월 3개 이상의 마케팅 메시지를 보내지 않도록 할 수 있습니다.

이를 위해 월별 달력 기간 동안 하나 이상의 채널을 기반으로 하여 전송되는 메시지 수를 제한하는 빈도 규칙을 사용할 수 있습니다.

>[!NOTE]
>
>메시지 빈도 규칙은 옵트아웃 관리와는 다릅니다. 옵트아웃 관리에서는 사용자가 브랜드로부터 커뮤니케이션 수신을 취소할 수 있습니다. [자세히 알아보기](../messages/consent.md#opt-out-management)

## 액세스 규칙 {#access-rules}

규칙은 **[!UICONTROL Administration]** > **[!UICONTROL Rules]** 메뉴 아래의 제품에서 사용할 수 있습니다. 모든 규칙이 수정 날짜별로 정렬되어 나열됩니다.

>[!NOTE]
>
>메시지 빈도 규칙에 액세스, 만들기, 편집 또는 삭제하려면 [빈도 규칙 관리](../administration/high-low-permissions.md#manage-frequency-rules) 권한.

![](assets/message-rules-access.png)

필터 아이콘을 사용하여 카테고리, 상태 및/또는 채널을 필터링합니다. 메시지 레이블에서도 검색할 수 있습니다.

![](assets/message-rules-filter.png)

## 규칙 만들기 {#create-new-rule}

새 규칙을 만들려면 아래 단계를 수행하십시오.

1. 액세스 권한 **[!UICONTROL Message frequency rules]** list 를 클릭한 다음 **[!UICONTROL Create rule]**.

   ![](assets/message-rules-create.png)

1. 규칙 이름을 정의합니다.

   ![](assets/message-rules-details.png)

1. 메시지 규칙 카테고리를 선택합니다.

   >[!NOTE]
   >
   >현재 **[!UICONTROL Marketing]** 카테고리를 사용할 수 있습니다.

1. 규칙에 대한 최대 최대 가용량(매월 개별 사용자 프로필에 보낼 수 있는 최대 메시지 수)을 설정합니다.

   ![](assets/message-rules-capping.png)

   >[!NOTE]
   >
   >빈도 제한은 월별 달력 기간을 기반으로 합니다. 매월 초에 재설정됩니다.

1. 이 규칙에 사용할 채널을 선택합니다. **[!UICONTROL Email]** 또는 **[!UICONTROL Push notification]**.

   ![](assets/message-rules-channels.png)

   >[!NOTE]
   >
   >규칙을 만들려면 적어도 하나의 채널을 선택해야 합니다.

1. 선택한 모든 채널에 대해 최대 가용량을 총 횟수로 적용하려면 여러 채널을 선택합니다.

   예를 들어 최대 가용량을 15로 설정하고, 이메일과 푸시 채널을 모두 선택합니다. 프로필에서 이미 10개의 마케팅 이메일 및 5개의 마케팅 푸시 알림을 받은 경우 이 프로필은 모든 마케팅 이메일 또는 푸시 알림의 바로 다음 게재에서 제외됩니다.

1. 클릭 **[!UICONTROL Save as draft]** 규칙 만들기를 확인하려면 메시지가 을 사용하여 규칙 목록에 추가됩니다. **[!UICONTROL Draft]** 상태.

   ![](assets/message-rules-created.png)

## 규칙 활성화 {#activate-rule}

메시지 빈도 규칙을 만들면 **[!UICONTROL Draft]** 상태 및 메시지가 아직 영향을 받지 않습니다. 사용하려면 규칙 옆의 생략 부호를 클릭하고 를 선택합니다 **[!UICONTROL Activate]**.

![](assets/message-rules-activate.png)

규칙을 활성화하면 다음 실행 시 적용되는 메시지에 영향을 줍니다. 방법 알아보기 [메시지에 빈도 규칙 적용](#apply-frequency-rule).

>[!NOTE]
>
>규칙을 적용하려면 메시지 또는 여정을 수정하거나 다시 게시할 필요가 없습니다.

메시지 빈도 규칙을 비활성화하려면 규칙 옆에 있는 줄임표를 클릭하고 을 선택합니다 **[!UICONTROL Deactivate]**.

![](assets/message-rules-deactivate.png)

규칙의 상태는 로 변경됩니다 **[!UICONTROL Inactive]** 그리고 이 규칙은 향후 메시지 실행에 적용되지 않습니다. 현재 실행 중인 모든 메시지는 영향을 받지 않습니다.

>[!NOTE]
>
>규칙을 비활성화하는 것은 개별 프로필의 카운트에 영향을 주지 않거나 재설정되지는 않습니다.

## 메시지에 빈도 규칙 적용 {#apply-frequency-rule}

메시지에 빈도 규칙을 적용하려면 아래 단계를 따르십시오.

1. 메시지 만들기. [자세히 알아보기](../messages/get-started-content.md#create-new-message)

1. 에 대해 정의한 카테고리를 선택합니다 [만든 규칙](#create-new-rule).

   ![](assets/message-rules-msg-properties.png)

   >[!NOTE]
   >
   >현재 **[!UICONTROL Marketing]** 카테고리는 메시지 빈도 규칙에 사용할 수 있습니다.

1. 메시지에 대해 선택한 채널을 선택합니다.

   ![](assets/message-rules-msg-channels.png)

1. 을(를) 클릭합니다. **[!UICONTROL Frequency rule]** 링크를 클릭하여 선택한 카테고리 및 채널에 적용할 빈도 규칙을 봅니다.

   ![](assets/message-rules-msg-link.png)

   일치하는 메시지 빈도 규칙을 표시하는 새 탭이 열립니다.

1. [디자인](../design/design-emails.md) 및 [게시](../messages/publish-manage-message.md) 메시지를 표시합니다.

선택한 카테고리 및 채널과 일치하는 모든 빈도 규칙이 이 메시지에 자동으로 적용됩니다.

<!--Clicking the link out button next to the category selector will jump you over to the rules inventory screen to see which rules will be applied to the message.-->

에서 게재에서 제외된 프로필 수를 볼 수 있습니다 [라이브 및 전역 보기](../reports/message-monitoring.md), 및에서 [이메일 라이브 보고서](../reports/email-live-report.md): 게재에서 제외된 사용자에 대한 가능한 이유로 빈도 규칙이 나열됩니다.

>[!NOTE]
>
>여러 규칙이 동일한 채널에 적용할 수 있지만 하위 캡에 도달하면 프로필이 다음 게재에서 제외됩니다.

## 예: 여러 규칙 결합 {#frequency-rule-example}

아래 예와 같이 여러 메시지 빈도 규칙을 결합할 수 있습니다.

1. [규칙 만들기](#create-new-rule) called *전체 마케팅 최대 가용량*:

   * 모든 채널(이메일, 푸시)을 선택합니다.
   * 최대 가용량을 12로 설정합니다.

   ![](assets/message-rules-ex-overall-cap.png)

1. 사용자가 전송되는 마케팅 기반 푸시 알림 수를 추가로 제한하려면 *푸시 마케팅 상한*:

   * 푸시 채널 을 선택합니다.
   * 최대 가용량을 4로 설정합니다.

   ![](assets/message-rules-ex-push-cap.png)

1. 저장 및 [활성화](#activate-rule) 규칙.

1. 메시지 만들기. [자세히 알아보기](../messages/get-started-content.md#create-new-message)

1. 을(를) 선택합니다 **[!UICONTROL Marketing]** 카테고리.

   ![](assets/message-rules-ex-category-maktg.png)

1. 을(를) 선택합니다 **[!UICONTROL Email]** 및 **[!UICONTROL Push Notification]** 채널입니다.

   ![](assets/message-rules-ex-channels.png)

1. 을(를) 클릭합니다. **[!UICONTROL Frequency rule]** 링크를 클릭하여 선택한 카테고리 및 채널에 적용할 빈도 규칙을 봅니다.

1. [디자인](../design/design-emails.md) 및 [게시](../messages/publish-manage-message.md) 메시지를 표시합니다.

이 시나리오에서는 개별 프로필이 다음과 같습니다.
* 은 매월 최대 12개의 마케팅 메시지를 받을 수 있습니다.
* 그러나 4개의 푸시 알림을 수신하면 마케팅 푸시 알림에서 제외됩니다.
