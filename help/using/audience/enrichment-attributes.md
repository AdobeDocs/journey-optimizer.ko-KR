---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Experience Platform 대상자 정보
description: Adobe Experience Platform 대상자 사용 방법 알아보기
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 3ec496ba-7555-49e2-992c-403c33302a90
source-git-commit: f99ba639b5d47fa334741b7e55e7bce83697626d
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 3%

---

# 대상자 강화 속성 사용 {#enrichment}

작성 워크플로우, 사용자 지정(CSV 파일) 대상 또는 통합 대상 작성을 사용하여 생성된 대상을 타깃팅할 때 이러한 대상의 보강 속성을 활용하여 여정을 작성하고 메시지를 개인화할 수 있습니다.

>[!NOTE]
>
>2024년 10월 1일 이전에 CSV 파일 사용자 지정 업로드를 통해 생성된 대상은 개인화할 수 없습니다. 이러한 대상의 속성을 사용하고 이 기능을 최대한 활용하려면 이 날짜 이전에 가져온 외부 CSV 대상을 다시 만들고 다시 업로드하십시오.
>
>동의 정책은 데이터 보강 속성을 지원하지 않습니다. 따라서 동의 정책 규칙은 프로필에 있는 속성만 기반으로 해야 합니다.

다음은 대상의 데이터 보강 속성을 사용하여 수행할 수 있는 작업입니다.

* 대상 대상의 강화 특성을 활용하는 규칙을 기반으로 **여정에 여러 경로를 만듭니다**. 이렇게 하려면 [대상 읽기](../building-journeys/read-audience.md) 활동을 사용하여 대상을 타깃팅한 다음 대상의 데이터 보강 특성을 기반으로 [조건](../building-journeys/condition-activity.md) 활동에서 규칙을 만듭니다.

  ![](assets/audience-enrichment-attribute-condition.png){width="70%" zoomable="yes"}

* 개인화 편집기에서 타겟팅된 대상의 데이터 보강 특성을 추가하여 여정 또는 캠페인에서 **메시지를 개인화합니다**. [개인화 편집기로 작업하는 방법을 알아보세요](../personalization/personalization-build-expressions.md)

  ![](assets/audience-enrichment-attribute-perso.png){width="70%" zoomable="yes"}

>[!IMPORTANT]
>
>작성 워크플로우를 사용하여 만든 대상의 보강 속성을 사용하려면 &quot;ExperiencePlatform&quot; 데이터 Source 내의 필드 그룹에 추가되었는지 확인하십시오.
>
>+++ 필드 그룹에 데이터 보강 속성을 추가하는 방법 알아보기>
>
>1. &quot;관리&quot; > &quot;구성&quot; > &quot;데이터 소스&quot;로 이동합니다.
>1. &quot;Experience Platform&quot;를 선택하고 필드 그룹을 만들거나 편집합니다.
>1. 스키마 선택기에서 적절한 스키마를 선택합니다. 스키마 이름은 &#39;Schema for audienceId:&#39; + 대상 ID 형식으로 이루어집니다. 대상자 인벤토리의 대상자 세부 사항 화면에서 대상자 ID를 찾을 수 있습니다.
>1. 필드 선택기를 열고 추가할 데이터 보강 속성을 찾은 다음 해당 속성 옆의 확인란을 선택합니다.
>1. 변경 내용을 저장합니다.
>1. 데이터 보강 속성이 필드 그룹에 추가되면 위에 나열된 위치의 Journey Optimizer에서 이를 활용할 수 있습니다.
>
>데이터 소스에 대한 자세한 내용은 다음 섹션에서 확인할 수 있습니다.
>
>* [Adobe Experience Platform 데이터 원본으로 작업](../datasource/adobe-experience-platform-data-source.md)
>* [데이터 원본 구성](../datasource/configure-data-sources.md)
>
>+++







+++ 데이터 보강 속성이란 무엇입니까?

데이터 보강 속성은 상황에 맞는 추가 속성이며 대상에만 국한됩니다. 프로필과 연결되어 있지 않으며 일반적으로 개인화 목적으로 사용됩니다.

데이터 보강 속성은 대상자 구성의 데이터 보강 활동이나 사용자 지정 업로드 프로세스를 통해 대상자에 연결됩니다.

+++

+++ Journey Optimizer 내에서 데이터 보강 속성을 사용할 수 있는 곳은 어디입니까?

대상자 구성의 데이터 보강 속성은 다음 영역에서 활용할 수 있습니다. [대상 데이터 보강 특성을 사용하는 방법을 알아보세요](#enrichment)

* 조건 활동(여정)
* 사용자 지정 작업 특성(여정)
* 메시지 개인화(여정 및 캠페인)

+++

+++ 여정에서 데이터 보강 속성을 활성화하려면 어떻게 해야 합니까?

작성 워크플로를 사용하여 만든 대상의 데이터 보강 속성을 사용하려면 해당 속성이 &quot;ExperiencePlatform&quot; 데이터 Source 내의 필드 그룹에 추가되어 있는지 확인하십시오. 필드 그룹에 데이터 보강 특성을 추가하는 방법에 대한 정보는 [이 섹션](#enrichment)에서 확인할 수 있습니다.

+++

+++ 여정이 시작된 후 데이터 보강 속성 값이 업데이트됩니까?

현재는 없습니다. 대기 노드나 이벤트 여정 후에도 데이터 보강 속성 값은 이벤트가 시작될 때와 동일하게 유지됩니다.

+++
