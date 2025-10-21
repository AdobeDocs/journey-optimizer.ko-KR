---
solution: Journey Optimizer
product: journey optimizer
title: 작업 시작
description: 작업 방법 알아보기
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Engineer, Admin
level: Experienced
keywords: 작업, 여정, 메시지, 보내기, 연결
exl-id: 7f0cda1d-daf0-4d4c-9978-ddef81473813
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 40%

---

# 사용자 정의 액션 시작 {#about_actions}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_list"
>title="사용자 정의 액션"
>abstract="액션은 푸시 알림, 이메일, SMS 또는 회사에서 사용하는 기타 디지털 참여 방법 등의 개인화된 실시간 경험을 고객에게 제공하는 데 사용되는 연결입니다."

액션은 푸시 알림, 이메일, SMS 또는 회사에서 사용하는 기타 디지털 참여 방법 등의 개인화된 실시간 경험을 고객에게 제공하는 데 사용되는 연결입니다.

➡️ [비디오에서 이 기능 살펴보기](#video)

[!DNL Journey Optimizer]에는 기본 메시지 기능이 포함되어 있습니다. 사용자 정의 액션에서는 메시지나 API 호출을 전송할 서드파티 시스템의 연결을 구성할 수 있습니다. JSON 형식 페이로드를 사용하여 REST API를 통해 호출할 수 있는 모든 공급자의 어떤 서비스로든 작업을 구성할 수 있습니다.

* Adobe Campaign v7 또는 v8을 사용하는 경우 요청 시 통합을 사용할 수 있습니다. [이 페이지](../action/acc-action.md)를 참조하십시오.

* Epsilon, Facebook, Adobe Developer, Firebase 등의 서드파티 시스템을 사용하여 메시지를 보내는 경우, 사용자 지정 작업을 만들고 구성해야 합니다. [이 페이지](../action/about-custom-action-configuration.md)를 참조하십시오.

>[!CAUTION]
>
>사용자 지정 작업은 **기술 사용자**&#x200B;가 구성해야 합니다.

사용자 지정 작업은 기술 사용자가 정의하고 마케터가 사용할 수 있는 추가 작업입니다. 구성되면 여정의 왼쪽 팔레트의 **[!UICONTROL 작업]** 카테고리에 표시됩니다. [이 페이지](../building-journeys/about-journey-activities.md#action-activities)에서 자세히 알아보십시오.

작업 목록을 보거나 새 작업을 구성하려면 관리 메뉴 섹션에서 **[!UICONTROL 구성]**&#x200B;을 선택합니다. **[!UICONTROL 작업]** 섹션에서 **[!UICONTROL 관리]**&#x200B;를 클릭합니다. 그러면 작업 목록이 표시됩니다. 인터페이스에 대한 자세한 내용은 [이 페이지](../start/user-interface.md)를 참조하십시오.

![](assets/custom1.png)

이 전용 페이지[에서 사용자 지정 작업 &#x200B;](../action/troubleshoot-custom-action.md)의 문제를 해결하는 방법을 알아보세요.

## 사용 방법 비디오 {#video}

사용자 지정 작업을 구성하는 방법을 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/3428396?quality=12)

## 추가 리소스

사용자 지정 작업 구성 및 사용에 대한 자세한 내용은 아래 섹션을 참조하십시오.

* [사용자 지정 작업 구성](../action/about-custom-action-configuration.md) - 사용자 지정 작업을 만들고 구성하는 방법에 대해 알아봅니다.
* [사용자 지정 작업 사용](../building-journeys/using-custom-actions.md) - 여정에서 사용자 지정 작업을 사용하는 방법에 대해 알아봅니다.
* [사용자 지정 작업 매개 변수에 컬렉션 전달](../building-journeys/collections.md) - 런타임에 동적으로 채워진 사용자 지정 작업 매개 변수에서 컬렉션을 전달하는 방법을 알아봅니다.
* [사용자 지정 작업 문제 해결](../action/troubleshoot-custom-action.md) - 사용자 지정 작업 문제를 해결하는 방법 알아보기

