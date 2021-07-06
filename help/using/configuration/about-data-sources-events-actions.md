---
title: 관리 및 설정
description: 관리 및 설정 지침 학습
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
feature: 애플리케이션 설정
topic: 관리
role: Administrator
level: Intermediate
source-git-commit: b07970ff11f1ba7c4e6db30dc2eca1252a579ca4
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 50%

---

# 여정 구성

여정과 함께 메시지를 보내려면 **[!UICONTROL Data Sources]**, **[!UICONTROL Events]** 및 **[!UICONTROL Actions]**&#x200B;를 구성해야 합니다.

![](../assets/admin-menu.png)

## 데이터 소스

데이터 소스 구성을 사용하면 시스템에 대한 연결을 정의하여 여정에 사용할 추가 정보를 검색할 수 있습니다. [자세히 알아보기](../../using/datasource/about-data-sources.md)

## 이벤트

이벤트를 사용하면 여정으로 유입되는 개인에게 실시간으로 메시지를 보낼 때까지 여정을 트리거할 수 있습니다.

이벤트 구성에서는 여정에 필요한 이벤트를 구성합니다. 수신되는 이벤트 데이터는 Adobe Experience 데이터 모델(XDM)에 따라 표준화됩니다. 이벤트는 인증된 이벤트와 인증되지 않은 이벤트(예: Adobe Mobile SDK 이벤트)를 위한 수집 API 스트리밍에서 옵니다. [자세히 알아보기](../../using/event/about-events.md)

## 작업

Journey Optimizer 메시지 기능 기본 제공:콘텐츠를 디자인하고 메시지를 게시하기만 하면 됩니다. 서드파티 시스템을 사용하여 메시지를 전송하는 경우 사용자 지정 작업을 만들 수 있습니다. [자세히 알아보기](../../using/action/action.md)

## Adobe Experience Platform 필드를 통한 검색 {#friendly-names-display}

[이벤트 페이로드](../event/about-creating.md#define-the-payload-fields), [필드 그룹 페이로드](../datasource/configure-data-sources.md#define-field-groups)를 정의하고 [표현식 편집기](https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/expressionadvanced.html?lang=ko){target=&quot;_blank&quot;}에서 필드를 선택할 때 필드 이름과 함께 표시 이름이 표시됩니다. 이 정보는 Experience Data Model의 스키마 정의에서 검색됩니다.

스키마를 설정할 때 &quot;xdm:alternateDisplayInfo&quot;와 같은 설명자를 입력하면 사용자에게 친숙한 이름이 표시 이름 대신 표시됩니다. &quot;eVars&quot; 및 일반 필드로 작업할 때 특히 유용합니다. API 호출을 통해 친숙한 이름 설명자를 구성할 수 있습니다. 자세한 내용은 [스키마 레지스트리 개발자 안내서](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html?lang=ko){target=&quot;_blank&quot;}를 참조하십시오.

![](../assets/xdm-from-descriptors.png)

친숙한 이름을 사용할 수 있으면 필드가 `<friendly-name>(<name>)`으로 표시됩니다. 친숙한 이름을 사용할 수 없으면 `<display-name>(<name>)`과 같이 표시 이름이 표시됩니다. 어떤 이름도 정의되어 있지 않으면 필드의 기술적 이름(`<name>`)만 표시됩니다.

>[!NOTE]
>
>스키마 조합에서 필드를 선택하면 친숙한 이름이 검색되지 않습니다.