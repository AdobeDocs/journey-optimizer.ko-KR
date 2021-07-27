---
title: 데이터 소스 정보
description: 데이터 소스 구성 방법 알아보기
feature: 데이터 소스
topic: 관리
role: Admin
level: Intermediate
source-git-commit: d69779418d50fdc4b75cc777b27a62392d1634a0
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 72%

---

# 데이터 소스 정보 {#concept_s1s_dqt_52b}

>[!CONTEXTUALHELP]
>id="jo_datasources"
>title="데이터 소스 정보"
>abstract="데이터 소스는 항상 기술 사용자가 구성해야 합니다. 데이터 소스를 구성하면 여정에서 사용할 추가 정보 검색을 위해 시스템에 대한 연결을 정의할 수 있습니다. 이러한 추가 정보에는 조건 정의, 작업의 매개 변수 및 개인화 데이터, 사용자 지정 대기 정의, 시간대 정의 등이 있습니다."

데이터 소스를 구성하면 여정에서 사용할 추가 정보 검색을 위해 시스템에 대한 연결을 정의할 수 있습니다. 이러한 추가 정보에는 다음과 같은 항목이 포함됩니다.

* [조건 정의](../building-journeys/condition-activity.md)
* [작업](../action/action.md)의 매개 변수 및 개인화 데이터
* [사용자 지정 대기 정의](../building-journeys/wait-activity.md#custom)
* [시간대 정의](../building-journeys/timezone-management.md)

여정이 이벤트 페이로드에서 전송되는 로컬 데이터만 활용하는 경우에는 이 구성을 수행하지 않아도 됩니다. 예를 들어 여정에 이벤트, 그리고 해당 이벤트의 데이터만 사용하는 메시지 활동이 차례로 포함되어 있으면 데이터 소스를 구성할 필요가 없습니다.

데이터 소스에는 다음의 두 가지 유형이 있습니다.

* 실시간 고객 프로필 서비스에 대한 연결을 정의하는 사전 구성된 Adobe Experience Platform 데이터 소스(기본 데이터 소스). [이 페이지](../datasource/adobe-experience-platform-data-source.md)를 참조하십시오.
* 외부 시스템에 대한 연결을 정의할 수 있는 외부 데이터 소스. 이러한 소스는 직접 만들 수 있습니다. [이 페이지](../datasource/external-data-sources.md)를 참조하십시오.

각 데이터 소스에서는 필드 그룹을 사용하여 검색할 정보를 정의합니다. 필드 그룹은 데이터 소스에서 검색할 수 있는 필드 세트입니다. [이 페이지](../datasource/configure-data-sources.md#define-field-groups)를 참조하십시오.

>[!NOTE]
>
>이제 데이터 소스에 대해 스키마 관계가 지원됩니다.

Adobe Experience Platform 데이터 소스 및 외부 데이터 소스를 구성하는 방법, 그리고 여정에서 데이터를 찾아서 사용하는 방법과 관련된 자세한 내용을 확인하려면 이 [튜토리얼 비디오](https://experienceleague.adobe.com/docs/journey-orchestration-learn/tutorials/configure-data-sources.html){target=&quot;_blank&quot;}를 시청하십시오.
