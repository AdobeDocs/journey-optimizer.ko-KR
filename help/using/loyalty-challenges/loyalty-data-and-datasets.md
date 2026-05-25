---
solution: Journey Optimizer
product: journey optimizer
title: 충성도 데이터 및 데이터 세트
description: Adobe Experience Platform 프로필 데이터 및 데이터 세트 충성도 문제를 파악하고 데이터 세트 TTL(Time-to-Live)이 유지에 미치는 영향을 알아봅니다.
feature: Journeys
topic: Content Management
role: Admin, Developer
level: Intermediate
hide: true
badge: label="비공개 베타" type="Informative"
mini-toc-levels: 1
exl-id: a7c4e1b2-8f3d-4a6c-9e0b-1d2e3f4a5b6c
source-git-commit: dfeaa32ed3b216fdf63806356e1e5750db0c80cb
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 5%

---

# 충성도 데이터 및 데이터 세트 {#loyalty-data-and-datasets}

>[!BEGINSHADEBOX]

**충성도 과제 설명서**

[충성도 문제 시작](get-started.md)

+++과제 생성 및 관리

* [과제 및 작업 액세스 및 관리](access-loyalty-challenges.md)
* [과제 만들기](create-challenges.md)
* [작업 만들기](create-tasks.md)
* [충성도 과제 성능 모니터링](loyalty-reporting.md)

+++

+++구성 및 통합

<!-- * [Configure loyalty challenges](loyalty-admin.md) -->
* **충성도 데이터 및 데이터 세트** ◀︎ **현재 상태**
* [충성도 과제 API 참조](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

+++

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>이 기능은 현재 **개인 베타**&#x200B;에 있습니다. 릴리스 주기 및 가용성 단계에 대한 자세한 내용은 [Journey Optimizer 릴리스 주기](../rn/releases.md)를 참조하십시오.

## 개요 {#overview}

충성도 문제는 ID, 프로필 속성, 경험 이벤트 및 대상에 대해 Adobe Experience Platform에 의존합니다. 이 페이지를 사용하여 문제를 작성하거나 충성도 문제 API를 사용하기 전에 준비할 데이터, 관련된 데이터 세트 및 **TTL(time-to-live)**&#x200B;이(가) 유지에 미치는 영향을 알아봅니다.

Journey Optimizer 프로그램 설정(보상 이행 및 이벤트 매핑)에 대해 Adobe 관리자에게 문의하십시오. REST 끝점 및 인증의 경우 [충성도 도전 API 참조](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}를 참조하십시오.

## Adobe Experience Platform 데이터 {#aep-data}

### 프로필 속성 {#profile-attributes}

Challenge 대상자, 개인화 및 보고는 **[!DNL XDM Individual Profile]** 클래스의 프로필을 사용합니다. 충성도 문제에 사용하는 ID [namespace](https://experienceleague.adobe.com/ko/docs/experience-platform/identity/features/namespaces){target="_blank"}을(를) 프로필 데이터에서 구성원이 식별되는 방식과 맞춥니다.

프로필의 표준 충성도 특성(포인트, 계층, 프로그램, 상태 및 관련 필드)에 대해서는 Experience Platform **[충성도 세부 정보](https://experienceleague.adobe.com/ko/docs/experience-platform/xdm/field-groups/profile/loyalty-details){target="_blank"}** 스키마 필드 그룹을 사용하십시오. 해당 필드 그룹은 `loyalty` 개체와 해당 속성을 정의합니다(예: `points`, `tier`, `program` 및 `status`).

➡️ [충성도 세부 정보 스키마 필드 그룹](https://experienceleague.adobe.com/ko/docs/experience-platform/xdm/field-groups/profile/loyalty-details){target="_blank"}

### 경험 이벤트 {#experience-events}

**[!UICONTROL 구매]**, **[!UICONTROL 지출]** 및 **[!UICONTROL 사용자 지정 이벤트]** 작업은 Adobe Experience Platform에 수집된 경험 이벤트에 따라 다릅니다. **[!UICONTROL 사용자 지정 이벤트]** 작업의 경우 작업 빌더에서 선택하기 전에 관리자가 일치하는 이벤트 정의(식별자 경로, 선택적 XDM 스키마 ID, 스키마 및 변환기)를 구성해야 합니다.

이벤트 페이로드가 충성도 과제 구성과 동일한 ID 네임스페이스를 사용하므로 진행 상황이 올바른 프로필에 귀속될 수 있습니다.

### 대상 및 보고 {#audiences-reporting}

마케팅 담당자는 과제 자격 조건을 구성할 때 플랫폼 [대상](../audience/about-audiences.md)을(를) 선택합니다. 충성도 보고 대시보드는 Adobe Customer Journey Analytics을 사용합니다. [충성도 챌린지 성능을 모니터링하는 방법 알아보기](loyalty-reporting.md)

## 데이터 세트 TTL(Time-to-Live) {#dataset-ttl}

로열티 과제는 Adobe Experience Platform 데이터 세트(프로그램을 위해 만들어진 이벤트 및 개인화 관련 데이터 세트 포함)에 운영 및 보고 데이터를 저장합니다. 데이터 집합 **TTL(time-to-live)**&#x200B;은(는) 데이터가 데이터 레이크에 유지되는 기간과 해당되는 경우 프로필 스토어에서 유지되는 기간을 제어합니다.

Journey Optimizer은 시스템에서 생성한 여러 데이터 세트에 TTL 가드레일을 적용합니다. 로열티 관련 데이터 세트는 샌드박스에 대해 동일한 플랫폼 유지 모델을 따릅니다.

➡️ [Journey Optimizer의 TTL(데이터 세트 Time-to-Live) 보호](../data/datasets-ttl.md)

>[!NOTE]
>
>조직 수준의 충성도 구성에는 충성도 메타데이터 서비스를 통해 관리되는 아카이브 및 보존 설정(예: 아카이브 기간)이 포함될 수 있습니다. 비공개 베타 환경에 대한 보존 조정이 필요한 경우 Adobe 관리자와 협력합니다.

<!-- For UI-based setup (reward providers, event definitions, product inventory, and exclusions), see [Configure loyalty challenges](loyalty-admin.md). -->
