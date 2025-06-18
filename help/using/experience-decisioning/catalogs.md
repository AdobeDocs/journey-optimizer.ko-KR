---
title: 항목 카탈로그
description: 항목 카탈로그로 작업하는 방법을 알아봅니다.
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 2d118f5a-32ee-407c-9513-fe0ebe3ce8f0
source-git-commit: 25b1e6050e0cec3ae166532f47626d99ed68fe80
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 0%

---

# 항목 카탈로그 {#catalog}

Decisioning에서 카탈로그는 의사 결정 항목을 구성하는 중앙 컨테이너 역할을 합니다. 각 카탈로그는 의사 결정 항목에 할당할 수 있는 모든 속성을 포함하는 Adobe Experience Platform 스키마에 연결됩니다.

지금은 생성된 모든 결정 항목이 단일 &quot;오퍼&quot; 카탈로그 내에 통합되어 **[!UICONTROL 카탈로그]** 메뉴를 통해 액세스할 수 있습니다.

![](assets/catalogs-list.png)

## 가드레일 및 제한 사항

최적의 성능과 일관성을 보장하기 위해 Decisioning에서는 다음과 같은 보호 기능 및 제한 사항을 적용합니다.

* **지원되는 데이터 형식**

  현재 Decisioning은 String, Integer, Boolean, Date, DateTime, Decisioning 에셋 및 Object 데이터 형식을 독점적으로 지원합니다. 이러한 데이터 형식을 벗어나는 필드는 의사 결정 항목이나 카탈로그를 작성할 때 사용할 수 없습니다.


* **사용자 지정 특성 제한**

  각 결정 항목에는 최대 100개의 사용자 지정 속성이 포함될 수 있습니다.

* **중첩 제한**

  최대 네 가지 수준의 중첩이 지원됩니다. 이미지가 마지막 수준에서 지원되지 않습니다.

## 카탈로그의 스키마 액세스 및 편집 {#access-catalog-schema}

결정 항목 속성이 저장된 카탈로그의 스키마에 액세스하려면 다음 단계를 따르십시오.

1. 항목 목록에서 **[!UICONTROL 항목 만들기]** 단추 옆에 있는 **[!UICONTROL 스키마 편집]** 단추를 클릭합니다.

1. 카탈로그의 스키마가 아래 구조에 따라 새 탭에서 열립니다.

   * **`_experience`** 노드에는 이름, 시작 및 종료 날짜, 설명 등 표준 결정 항목 특성이 포함되어 있습니다.
   * **`_<imsOrg>`** 노드에는 사용자 지정 결정 항목 특성이 있습니다. 기본적으로 사용자 지정 속성은 구성되지 않지만 요구 사항에 맞게 필요한 만큼 추가할 수 있습니다. 완료되면 사용자 지정 속성이 표준 속성과 함께 의사 결정 항목 만들기 화면에 표시됩니다.

   ![](assets/catalogs-schema.png)

1. 스키마에 사용자 지정 특성을 추가하려면 **`_<imsOrg>`** 노드를 확장하고 구조의 원하는 위치에서 &quot;+&quot; 단추를 클릭하십시오.

   ![](assets/catalogs-add.png)

1. 추가된 특성에 필요한 필드를 입력하고 **[!UICONTROL 적용]**&#x200B;을 클릭합니다.

   자산 속성을 결정하는 속성에 입력되는 값은 공개 URL입니다. 대부분의 경우 이미지를 가리킵니다.

   Adobe Experience Platform 스키마를 사용하는 방법에 대한 자세한 내용은 [XDM 시스템 설명서](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=ko)를 참조하세요.

1. 원하는 사용자 지정 속성이 추가되면 스키마를 저장합니다. 이제 **[!UICONTROL 사용자 지정 특성]** 섹션 내의 결정 항목 만들기 화면에서 새 필드를 사용할 수 있습니다.


   아래 예제는 스키마에 정의된 개체와 같은 사용자 지정 속성이 있는 항목 만들기 화면을 보여 줍니다.

   ![](assets/custom-attributes.png)

