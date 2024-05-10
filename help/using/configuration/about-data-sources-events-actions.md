---
solution: Journey Optimizer
product: journey optimizer
title: 여정 구성
description: 데이터 소스, 이벤트 및 작업 구성 방법 알아보기
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: 구성, 여정, 대시보드, 데이터 소스, 이벤트, 작업
exl-id: c144d44f-031f-4ca2-800e-d3878af400a5
source-git-commit: b8065a68ed73102cb2c9da2c2d2675ce8e5fbaad
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 65%

---

# 여정 구성 {#configure-journeys}

>[!CONTEXTUALHELP]
>id="ajo_journey_configuration_dashboard"
>title="여정 구성 정보"
>abstract="여정과 함께 메시지를 전송하려면 데이터 원본, 이벤트 및 작업을 구성해야 합니다. 데이터 원본을 사용하여 여정에 사용할 조건 등의 추가 정보를 검색하려면 시스템에 대한 연결을 정의해야 합니다. 이벤트를 수신하면 이벤트를 사용하여 여정을 트리거할 수 있습니다. 사용자 정의 액션을 통해 서드파티 시스템에 연결하여 메시지를 전송할 수 있습니다. Journey Optimizer 내장 메시지 기능을 사용하는 경우 작업을 구성할 필요가 없습니다."

여정과 함께 메시지를 보내려면 다음을 구성해야 합니다. **[!UICONTROL 데이터 소스]**, **[!UICONTROL 이벤트]** 및 **[!UICONTROL 작업]**.

![](assets/admin-menu.png)

## 데이터 소스 {#data-sources}

데이터 소스 구성을 사용하면 여정에서 사용할 추가 정보를 검색하기 위해 시스템에 대한 연결을 정의할 수 있습니다. [자세히 알아보기](../../using/datasource/about-data-sources.md)

## 이벤트 {#events}

이벤트를 사용하면 여정을 통합적으로 트리거하여 여정에 참여하는 개인에게 실시간으로 메시지를 보낼 수 있습니다.

이벤트 구성에서 여정에서 예상되는 이벤트를 구성합니다. 수신되는 이벤트 데이터는 Adobe 경험 데이터 모델(XDM)에 따라 표준화됩니다. 이벤트는 인증된 이벤트와 인증되지 않은 이벤트(예: Adobe Mobile SDK 이벤트)를 위한 수집 API 스트리밍에서 옵니다. [자세히 알아보기](../../using/event/about-events.md)

## 작업 {#actions}

Journey Optimizer 메시지 기능 기본 제공: 여정에 채널 작업 활동을 추가하기만 하면 됩니다. 서드파티 시스템을 사용하여 메시지를 전송하는 경우 사용자 지정 작업을 만들 수 있습니다. [자세히 알아보기](../../using/action/action.md)

## Adobe Experience Platform 필드 검색 {#friendly-names-display}

[이벤트 페이로드](../event/about-creating.md#define-the-payload-fields)와 [필드 그룹 페이로드](../datasource/configure-data-sources.md#define-field-groups)를 정의하고 [표현식 편집기](../building-journeys/expression/expressionadvanced.md)에서 필드를 선택할 때는 필드 이름과 함께 표시 이름도 표시됩니다. 이 정보는 Experience Data Model의 스키마 정의에서 검색됩니다.

스키마를 설정할 때 &quot;xdm:alternateDisplayInfo&quot;와 같은 설명자를 입력하면 사용자에게 친숙한 이름이 표시 이름 대신 표시됩니다. &quot;eVars&quot; 및 일반 필드로 작업할 때 특히 유용합니다. API 호출을 통해 친숙한 이름 설명자를 구성할 수 있습니다. 자세한 내용은 [스키마 레지스트리 개발자 안내서](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html?lang=ko){target="_blank"}.

![](assets/xdm-from-descriptors.png)

친숙한 이름을 사용할 수 있으면 필드가 `<friendly-name>(<name>)`으로 표시됩니다. 친숙한 이름을 사용할 수 없으면 `<display-name>(<name>)`과 같이 표시 이름이 표시됩니다. 어떤 이름도 정의되어 있지 않으면 필드의 기술적 이름(`<name>`)만 표시됩니다.

>[!NOTE]
>
>스키마 조합에서 필드를 선택하면 친숙한 이름이 검색되지 않습니다.
