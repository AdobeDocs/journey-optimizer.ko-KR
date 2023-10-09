---
title: 컬렉션
description: 컬렉션 작업 방법 알아보기
feature: Offers
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 099d1439-34f7-47fe-9181-0e9ce2032a01
source-git-commit: c4ab97999d000d969f6f09f4d84be017d1288f94
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 17%

---

# 컬렉션 {#collections}

>[!BEGINSHADEBOX]

이 설명서의 내용:

* [Experience Decisioning 시작](gs-experience-decisioning.md)
* 결정 항목 관리
   * [항목 카탈로그 구성](catalogs.md)
   * [결정 항목 만들기](items.md)
   * **[항목 컬렉션 관리](collections.md)**
* 항목 선택 구성
   * [의사 결정 규칙 만들기](rules.md)
   * [등급 메서드 만들기](ranking.md)
* [선택 전략 만들기](selection-strategies.md)
* [결정 정책 만들기](create-decision.md)

>[!ENDSHADEBOX]

컬렉션을 사용하면 환경 설정에 따라 결정 항목을 범주화하고 그룹화할 수 있습니다. 이러한 범주는 의사 결정 항목의 속성을 활용하는 규칙을 만들어 만듭니다.

예를 들어 결정 항목의 카탈로그 스키마에 &quot;Category&quot; 사용자 지정 특성을 추가했다고 가정해 보겠습니다. 이렇게 하면 &quot;Category&quot; 특성에 &quot;Yoga&quot; 값이 있는 모든 결정 항목을 포함하는 컬렉션을 만들 수 있습니다.

컬렉션 목록은 다음 위치에서 액세스할 수 있습니다. **[!UICONTROL 항목]** 메뉴 아래의 제품에서 사용할 수 있습니다.

컬렉션을 만들려면 다음 단계를 수행하십시오.

1. 다음으로 이동 **[!UICONTROL 항목]** > **[!UICONTROL 컬렉션]** 및 클릭 **[!UICONTROL 컬렉션 만들기]**.
1. 컬렉션에 사용할 이름과 설명을 입력합니다.
1. 하나 이상의 규칙을 추가하여 컬렉션에 포함할 항목을 결정합니다. 다음 작업을 수행하십시오.

   1. 기준으로 사용할 항목 속성을 선택합니다. 속성 목록에는 카탈로그 스키마에 정의된 모든 표준 및 사용자 지정 속성이 포함됩니다. [항목 카탈로그에 대한 자세한 정보](catalogs.md)
   1. 원하는 연산자를 선택하고 필터링할 값을 입력합니다.
   1. 필요한 만큼 규칙을 추가하려면 이 단계를 반복하십시오. 여러 규칙이 추가되면 다음 중 하나를 선택할 수 있습니다. **및** 및 **또는** 연산자를 사용하여 결합할 수 있습니다. 이렇게 하려면 운영자 배지를 클릭하여 두 선택 항목 간을 전환합니다.

   ![](assets/collection-create.png)

1. 컬렉션 규칙이 정의되면 **[!UICONTROL 만들기]**. 이제 컬렉션이 목록에 표시됩니다.
