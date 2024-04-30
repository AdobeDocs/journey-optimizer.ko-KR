---
title: 항목 카탈로그
description: 항목 카탈로그 작업 방법 알아보기
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 2d118f5a-32ee-407c-9513-fe0ebe3ce8f0
source-git-commit: 2b9261ff0f225a429b9be04db214452736163766
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 5%

---

# 항목 카탈로그 {#catalog}

>[!BEGINSHADEBOX &quot;이 설명서 안내서에서 확인할 수 있는 사항&quot;]

* [Experience Decisioning 시작](gs-experience-decisioning.md)
* 의사 결정 항목 관리: **[항목 카탈로그 구성](catalogs.md)** - [의사 결정 항목 만들기](items.md) - [항목 컬렉션 관리](collections.md)
* 항목의 선택 사항 구성: [의사 결정 규칙 만들기](rules.md) - [등급 메서드 만들기](ranking.md)
* [선택 전략 만들기](selection-strategies.md)
* [결정 정책 만들기](create-decision.md)

>[!ENDSHADEBOX]

Experience Decisioning에서 카탈로그는 의사 결정 항목을 구성하는 중앙 컨테이너 역할을 합니다. 각 카탈로그는 의사 결정 항목에 할당할 수 있는 모든 속성을 포함하는 Adobe Experience Platform 스키마에 연결됩니다.

지금은 생성된 모든 의사 결정 항목이 단일 &quot;오퍼&quot; 카탈로그 내에 통합되어 를 통해 액세스할 수 있습니다. **[!UICONTROL 카탈로그]** 메뉴 아래의 제품에서 사용할 수 있습니다.

![](assets/catalogs-list.png)

결정 항목 속성이 저장된 카탈로그의 스키마에 액세스하려면 다음 단계를 따르십시오.

1. 항목 목록에서 **[!UICONTROL 스키마 편집]** 다음 옆에 있는 단추 **[!UICONTROL 항목 만들기]** 단추를 클릭합니다.

1. 카탈로그의 스키마가 아래 구조에 따라 새 탭에서 열립니다.

   * 다음 **`_experience`** 노드에는 이름, 시작 및 종료 날짜, 설명 등 표준 결정 항목 속성이 포함됩니다.
   * 다음 **`_<imsOrg>`** 노드에는 사용자 지정 의사 결정 항목 속성이 있습니다. 기본적으로 사용자 지정 속성은 구성되지 않지만 요구 사항에 맞게 필요한 만큼 추가할 수 있습니다. 완료되면 사용자 지정 속성이 표준 속성과 함께 의사 결정 항목 만들기 화면에 표시됩니다.

   ![](assets/catalogs-schema.png)

1. 사용자 지정 속성을 스키마에 추가하려면 **`_<imsOrg>`** 노드를 클릭하고 구조에서 원하는 위치에 있는 &quot;+&quot; 단추를 클릭합니다.

   ![](assets/catalogs-add.png)

1. 추가된 속성에 필요한 필드를 입력하고 를 클릭합니다 **[!UICONTROL 적용]**.

   >[!CAUTION]
   >
   >현재 Experience Decisioning은 아래에 나열된 데이터 유형만 지원합니다. 이러한 데이터 형식을 벗어나는 필드는 의사 결정 항목을 만들 때 사용할 수 없습니다.
   >* 문자열
   >* 부울
   >* 숫자

   Adobe Experience Platform 스키마로 작업하는 방법에 대한 자세한 내용은 [XDM 시스템 설명서](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=ko).

1. 원하는 사용자 지정 속성이 추가되면 스키마를 저장합니다. 이제 새 필드를 항목 의사 결정 만들기 화면의 **[!UICONTROL 사용자 지정 속성]** 섹션.
