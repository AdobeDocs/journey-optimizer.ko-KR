---
solution: Journey Optimizer
product: journey optimizer
title: API에서 트리거된 캠페인 대상 정의
description: API로 트리거된 캠페인 대상자를 정의하는 방법을 알아봅니다.
topic: Content Management
role: Developer
level: Experienced
keywords: 캠페인, API 트리거, REST, 최적화 도구, 메시지
exl-id: 6dda5687-3742-4e88-be7c-c4969b183161
source-git-commit: 93698c93f3750b4d7feff18509f8144a7c79f156
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 2%

---

# API에서 트리거된 캠페인 대상 정의 {#api-audience}

**[!UICONTROL 대상자]** 탭을 사용하여 캠페인 대상자를 정의합니다.

![](assets/campaign-audience.png)

## 대상자 선택

**마케팅 API 트리거 캠페인**&#x200B;의 경우 **[!UICONTROL 대상 선택]** 단추를 클릭하여 사용 가능한 Adobe Experience Platform 대상 목록을 표시합니다. [대상자에 대해 자세히 알아보기](../audience/about-audiences.md).

>[!IMPORTANT]
>
>[대상 구성](../audience/get-started-audience-orchestration.md)의 대상 및 특성을 현재 Healthcare Shield 또는 Privacy and Security Shield에서 사용할 수 없습니다.

**트랜잭션 API 트리거 캠페인**&#x200B;의 경우 API 호출에 타겟팅된 프로필을 정의해야 합니다. 단일 API 호출은 최대 20개의 고유 수신자를 지원합니다. 각 수신자는 고유한 사용자 ID를 가져야 하며, 중복된 사용자 ID는 허용되지 않습니다. 자세한 내용은 [대화형 메시지 실행 API 설명서](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution/operation/postIMUnitaryMessageExecution){target="_blank"}를 참조하세요

## ID 유형 선택

**[!UICONTROL ID 유형]** 필드에서 선택한 대상에서 개인을 식별하는 데 사용할 키 유형을 선택합니다. 기존 ID 유형을 사용하거나 Adobe Experience Platform ID 서비스를 사용하여 새 ID 유형을 만들 수 있습니다. 표준 ID 네임스페이스는 [이 페이지](https://experienceleague.adobe.com/ko/docs/experience-platform/identity/features/namespaces#standard){target="_blank"}에 나열됩니다.

캠페인당 하나의 ID 유형만 허용됩니다. 다른 ID 중에서 선택한 ID 유형이 없는 세그먼트에 속하는 개인은 캠페인에서 타깃팅할 수 없습니다. [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=ko-KR){target="_blank"}에서 ID 유형 및 네임스페이스에 대해 자세히 알아보세요.

## 캠페인 실행 시 프로필 만들기 활성화

경우에 따라 시스템에 없는 프로필로 트랜잭션 메시지를 보내야 할 수도 있습니다. 예를 들어 알 수 없는 사용자가 웹 사이트에서 암호를 재설정하려고 하는 경우입니다. 데이터베이스에 프로필이 없는 경우, Journey Optimizer에서 캠페인을 실행할 때 프로필을 자동으로 만들어 이 프로필로 메시지를 보낼 수 있습니다.

캠페인 실행 시 프로필 만들기를 활성화하려면 **[!UICONTROL 새 프로필 만들기]** 옵션을 켜십시오. 이 옵션이 비활성화되면 모든 전송에 대해 알 수 없는 프로필이 거부되고 API 호출이 실패합니다.

![](assets/api-triggered-create-profile.png)

>[!IMPORTANT]
>
>이 옵션은 플랫폼에 이미 존재하는 많은 프로필이 있는 대용량 트랜잭션 전송 사용 사례에서 **매우 작은 볼륨 프로필 만들기**&#x200B;에 제공됩니다.
>
>**AJO 대화형 메시징 프로필 데이터 집합** 데이터 집합에서 각 아웃바운드 채널(이메일, SMS 및 푸시)에 대해 각각 세 개의 기본 네임스페이스(이메일, 전화 및 ECID)에 알 수 없는 프로필이 만들어집니다. 그러나 사용자 지정 네임스페이스를 사용하는 경우 동일한 사용자 지정 네임스페이스로 ID가 만들어집니다.

## Webhook 활성화 {#webhook}

트랜잭션 API 트리거 캠페인의 경우, 웹후크를 활성화하여 메시지 실행 상태에 대한 실시간 피드백을 받을 수 있습니다. 이렇게 하려면 **[!UICONTROL Enable Webhooks]** 옵션을 전환하여 구성된 Webhook에 게재 상태 이벤트를 보냅니다.

![](assets/api-triggered-webhook.png)

Webhook 구성은 **[!UICONTROL 관리]** / **[!UICONTROL 채널]** / **[!UICONTROL 피드백 Webhook]** 메뉴에서 중앙에서 관리됩니다. 여기에서 관리자는 웹후크 끝점을 만들고 편집할 수 있습니다. [피드백 웹후크를 만드는 방법을 알아보세요](../configuration/feedback-webhooks.md)

## 다음 단계 {#next}

캠페인 구성 및 콘텐츠가 준비되면 실행을 예약할 수 있습니다. [자세히 알아보기](api-triggered-campaign-schedule.md)
