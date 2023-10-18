---
title: 컬렉션 만들기
description: 컬렉션을 사용하여 오퍼를 구성하는 방법 알아보기
feature: Decision Management, Collections
topic: Integrations
role: User
level: Intermediate
exl-id: 0c8808e3-9148-4a33-9fd5-9218e02c2dfd
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '364'
ht-degree: 8%

---

# 컬렉션 만들기 {#create-collections}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_decision_collection"
>title="오퍼 컬렉션 정보"
>abstract="오퍼 컬렉션을 사용하면 선택한 범주로 다시 그룹화하여 오퍼를 구성할 수 있습니다."

컬렉션을 사용하면 오퍼를 선택한 카테고리로 다시 그룹화하여 오퍼를 구성할 수 있습니다. 예를 들어 스포츠 관련 오퍼만 포함하는 &quot;sport&quot; 컬렉션을 만들 수 있습니다.

➡️ [비디오에서 이 기능 살펴보기](#video)

오퍼 컬렉션 목록은 다음에서 액세스할 수 있습니다. **[!UICONTROL 오퍼]** 메뉴 아래의 제품에서 사용할 수 있습니다.

![](../assets/collections_list.png)

다음 두 가지 유형의 컬렉션을 만들 수 있습니다.

* **동적 컬렉션** 는 컬렉션 한정자(이전의 &quot;태그&quot;라고 함)를 기반으로 하는 오퍼의 컬렉션입니다. 이러한 컬렉션은 자동으로 업데이트됩니다. 예를 들어 선택한 컬렉션 한정자를 사용하여 새 오퍼를 만든 경우 해당 오퍼는 자동으로 컬렉션에 추가됩니다.

* **정적 컬렉션** 은 컬렉션에 포함할 개별 오퍼를 수동으로 선택하여 빌드된 컬렉션입니다. 수동으로 오퍼를 더 추가하여 컬렉션을 업데이트할 수 없습니다.

컬렉션을 만들려면 다음 단계를 수행하십시오.

1. 로 이동 **[!UICONTROL 컬렉션]** 탭을 클릭한 다음 를 클릭합니다 **[!UICONTROL 컬렉션 만들기]**.

1. 만들 컬렉션의 이름과 유형을 지정합니다.

   ![](../assets/collection_create.png)

1. 동적 컬렉션을 만들려면 왼쪽 창에서 컬렉션에 추가할 오퍼의 컬렉션 한정자를 선택한 다음 을 클릭합니다 **[!UICONTROL 저장]**. 선택한 컬렉션 한정자를 사용하는 모든 오퍼가 컬렉션에 저장됩니다.

   컬렉션 한정자 만들기에 대한 자세한 내용은 [컬렉션 한정자 만들기](../offer-library/creating-tags.md).

   ![](../assets/dynamic_collection.png)

1. 정적 컬렉션을 만들려면 왼쪽 창에서 오퍼 목록(상태, 컬렉션 한정자, 날짜, 채널, 콘텐츠 유형)을 필터링한 다음 컬렉션에 추가할 오퍼를 선택합니다.

   ![](../assets/static_collection.png)

   >[!NOTE]
   >
   >정적 컬렉션은 자동으로 업데이트되지 않습니다. 정적 컬렉션에 오퍼를 추가하려면 오퍼를 편집하고 수동으로 추가해야 합니다.

1. 정적 컬렉션에 사용자 지정 또는 핵심 데이터 사용 레이블을 할당하려면 다음을 선택합니다. **[!UICONTROL 액세스 관리]**. [OLAC(Object Level Access Control)에 대해 자세히 알아보기](../../administration/object-based-access.md)

   >[!NOTE]
   >
   >동적 컬렉션에는 OLAC를 사용할 수 없습니다. 오퍼 수준에서 관리되어야 합니다. 따라서 이러한 오퍼에 액세스할 수 없는 경우 동적 컬렉션에 오퍼가 표시되지 않을 수 있습니다.

1. 컬렉션이 만들어지면 목록에 표시됩니다. 선택하여 편집하거나 삭제할 수 있습니다.

   ![](../assets/collection_created.png)

## 방법 비디오 {#video}

>[!VIDEO](https://video.tv.adobe.com/v/329376?quality=12)


