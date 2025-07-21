---
solution: Journey Optimizer
product: journey optimizer
title: API에서 트리거된 캠페인 속성 정의
description: API에서 트리거된 캠페인 속성을 정의하는 방법을 알아봅니다.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: 캠페인, API 트리거, REST, 최적화 도구, 메시지
source-git-commit: 1bdba8c5c1a9238d351b159551f6d3924935b339
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 22%

---


# API에서 트리거된 캠페인 속성 정의 {#api-properties}

새 API 트리거 캠페인을 만들려면 다음 단계를 수행하십시오.

1. **[!UICONTROL 캠페인]** 메뉴로 이동한 다음 **[!UICONTROL API 트리거]** 탭을 선택합니다.

1. **[!UICONTROL 캠페인 만들기]** 단추를 클릭하고 캠페인 유형을 선택합니다.

   * **[!UICONTROL API 트리거됨 - 마케팅]** - 이 유형의 API 트리거된 캠페인을 선택하여 타깃팅된 대상자에게 개인화된 마케팅 커뮤니케이션을 보냅니다.

   * **[!UICONTROL API 트리거됨 - 트랜잭션]** - 트랜잭션 캠페인은 트랜잭션 메시지(예: 암호 재설정 요청, 장바구니 구매 등 개인이 수행한 작업에 따라 발송된 메시지)를 보내는 것을 목표로 합니다.

   ![](assets/api-triggered-modal.png)

1. **[!UICONTROL 속성]** 탭에서 캠페인의 이름과 설명을 입력합니다.

   ![](assets/create-campaign-properties.png)

1. **태그** 필드를 사용하여 Adobe Experience Platform 통합 태그를 캠페인에 지정하십시오. 태그를 할당하면 캠페인을 간단히 분류하고 캠페인 목록에서 편하게 검색할 수 있습니다. [태그를 사용하여 작업하는 방법을 알아봅니다](../start/search-filter-categorize.md#tags).

1. 액세스 레이블에 따라 이 캠페인에 대한 액세스를 제한할 수 있습니다. 액세스 제한을 추가하려면 이 페이지 상단의 **[!UICONTROL 액세스 관리]** 버튼을 찾아보십시오. 사용 권한이 있는 레이블만 선택해야 합니다. [개체 수준 액세스 제어에 대해 자세히 알아보세요](../administration/object-based-access.md).

## 다음 단계 {#next}

캠페인 구성 및 콘텐츠가 준비되면 해당 작업을 구성할 수 있습니다. [자세히 알아보기](api-triggered-campaign-action.md)
