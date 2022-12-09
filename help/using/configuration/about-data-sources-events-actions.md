---
solution: Journey Optimizer
product: journey optimizer
title: 여정 구성
description: 데이터 소스, 이벤트 및 작업을 구성하는 방법을 알아봅니다
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: c144d44f-031f-4ca2-800e-d3878af400a5
source-git-commit: f04454860ebe597d3306e62b58de5f32e08342ee
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 0%

---

# 여정 구성 {#configure-journeys}

>[!CONTEXTUALHELP]
>id="ajo_journey_configuration_dashboard"
>title="여정 구성"
>abstract="여정으로 메시지를 보내려면 데이터 소스, 이벤트 및 작업을 구성해야 합니다. 데이터 소스를 사용하면 여정에서 사용할 조건 등의 추가 정보를 검색할 시스템에 대한 연결을 정의할 수 있습니다. 이벤트를 사용하면 이벤트가 수신될 때 여정을 트리거할 수 있습니다. 사용자 지정 작업을 사용하면 서드파티 시스템에 연결하여 메시지를 보낼 수 있습니다. Journey Optimizer 기본 제공 메시지 기능을 사용하는 경우 작업을 구성할 필요가 없습니다."

여정으로 메시지를 보내려면 구성해야 합니다 **[!UICONTROL Data Sources]**, **[!UICONTROL Events]** 및 **[!UICONTROL Actions]**.

![](assets/admin-menu.png)

## 데이터 소스 {#data-sources}

데이터 소스 구성을 사용하면 여정에서 사용할 추가 정보를 검색할 시스템에 대한 연결을 정의할 수 있습니다. [추가 정보](../../using/datasource/about-data-sources.md)

## 이벤트 {#events}

이벤트를 사용하면 여정으로 유입되는 개인에게 실시간으로 메시지를 보낼 수 있도록 여정 경로를 트리거할 수 있습니다.

이벤트 구성에서는 여정에서 예상되는 이벤트를 구성합니다. 수신되는 이벤트 데이터는 Adobe Experience 데이터 모델(XDM)에 따라 표준화됩니다. 이벤트는 인증된 이벤트 및 인증되지 않은 이벤트(예: Adobe Mobile SDK 이벤트)에 대한 스트리밍 수집 API에서 가져옵니다. [추가 정보](../../using/event/about-events.md)

## 작업 {#actions}

Journey Optimizer 메시지 기능이 내장되어 있습니다. 여정에 채널 작업 활동만 추가해야 합니다. 서드파티 시스템을 사용하여 메시지를 전송하는 경우 사용자 지정 작업을 만들 수 있습니다. [추가 정보](../../using/action/action.md)

## Adobe Experience Platform 필드 탐색 {#friendly-names-display}

정의할 때 [이벤트 페이로드](../event/about-creating.md#define-the-payload-fields), [필드 그룹 페이로드](../datasource/configure-data-sources.md#define-field-groups) 및 [표현식 편집기](../building-journeys/expression/expressionadvanced.md)를 입력하면 필드 이름과 함께 표시 이름이 표시됩니다. 이 정보는 Experience Data Model의 스키마 정의에서 검색됩니다.

스키마를 설정할 때 &quot;xdm:alternateDisplayInfo&quot;와 같은 설명자를 입력하면 사용자에게 친숙한 이름이 표시 이름 대신 표시됩니다. 이 기능은 &quot;eVar&quot; 및 일반 필드 사용 시 특히 유용합니다. API 호출을 통해 친숙한 이름 설명자를 구성할 수 있습니다. 자세한 내용은 [스키마 레지스트리 개발자 안내서](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html){target=&quot;_blank&quot;}.

![](assets/xdm-from-descriptors.png)

친숙한 이름을 사용할 수 있으면 필드가 `<friendly-name>(<name>)`. 친숙한 이름을 사용할 수 없으면 예를 들어 표시 이름이 표시됩니다 `<display-name>(<name>)`. 어떤 이름도 정의되어 있지 않으면 필드의 기술 이름만 표시됩니다 `<name>`.

>[!NOTE]
>
>스키마 조합에서 필드를 선택하면 친숙한 이름이 검색되지 않습니다.
