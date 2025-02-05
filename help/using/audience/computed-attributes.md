---
solution: Journey Optimizer
product: journey optimizer
title: 계산된 속성 관련 작업
description: 계산된 속성으로 작업하는 방법을 알아봅니다.
feature: Audiences, Profiles
role: User
level: Intermediate
exl-id: 5402a179-263f-46a7-bddf-5b7017cf0f82
source-git-commit: 12449430f48153ebe3fbb30b782f51de4b11d4ef
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 4%

---

# 계산된 속성 관련 작업 {#computed-attributes}

계산된 속성을 사용하면 개별 행동 이벤트를 Adobe Experience Platform에서 사용할 수 있는 계산된 프로필 속성으로 요약할 수 있습니다. 이러한 계산된 속성은 Adobe Experience Platform에 수집된 프로필 사용 경험 이벤트 데이터 세트를 기반으로 하며 고객 프로필 내에 저장된 집계된 데이터 포인트로 사용됩니다.

각 계산된 속성은 여정 및 캠페인에서 세그멘테이션, 개인화 및 활성화를 위해 활용할 수 있는 프로필 속성입니다. 이러한 간소화는 고객에게 시기적절하고 의미 있는 개인화된 경험을 제공하는 기능을 향상시킵니다.


![](../rn/assets/do-not-localize/computed-attributes.gif)


>[!NOTE]
>
>계산된 속성에 액세스하려면 적절한 권한(**계산된 속성 보기** 및 **계산된 속성 관리**)이 있어야 합니다.

## 계산된 속성 만들기 {#manage}

계산된 특성을 만들려면 왼쪽에 있는 **[!UICONTROL 프로필]** 메뉴의 **[!UICONTROL 계산된 특성]** 탭으로 이동합니다.

이 화면에서 이벤트 속성, 집계 함수를 지정된 전환 확인 기간과 함께 결합하는 규칙을 작성하여 계산된 속성을 구성할 수 있습니다. 예를 들어, 지난 3개월 동안의 구매 합계를 계산하거나, 지난 주에 구매하지 않은 프로필에서 본 가장 최근 항목을 식별하거나, 각 프로필별로 누적된 총 보상 포인트를 계산할 수 있습니다.

![](assets/computed-attributes.png)

규칙이 준비되면 계산된 속성을 게시하여 Journey Optimizer을 포함한 다른 다운스트림 서비스에서 사용할 수 있도록 합니다.

계산된 특성을 만들고 관리하는 방법에 대한 자세한 내용은 [계산된 특성 설명서](https://experienceleague.adobe.com/docs/experience-platform/profile/computed-attributes/overview.html?lang=ko)를 참조하세요.

## Adobe Experience Platform 데이터 소스에 계산된 속성 추가 {#source}

Journey Optimizer에서 계산된 특성을 활용하려면 먼저 계산된 특성을 Journey Optimizer **Experience Platform** 데이터 소스에 추가해야 합니다.

Adobe Experience Platform 데이터 소스는 Adobe 실시간 고객 프로필에 대한 연결을 정의합니다. 이 데이터 소스는 실시간 고객 프로필 서비스에서 프로필 데이터 및 경험 이벤트 데이터를 검색하도록 설계되었습니다.

계산된 속성을 데이터 소스에 추가하려면 다음 단계를 수행합니다.

1. **[!UICONTROL 구성]** 왼쪽 메뉴로 이동한 다음 **[!UICONTROL 데이터 원본]** 카드를 클릭합니다.

1. **[!UICONTROL Experience Platform]** 데이터 원본을 선택하십시오.

   ![](assets/computed-attributes-add.png)

1. 만든 모든 계산 특성을 포함하는 **[!UICONTROL SystemComputedAttributes]** 필드 그룹을 추가합니다.

   ![](assets/computed-attributes-fieldgroup.png)

이제 계산된 속성을 Journey Optimizer에서 사용할 수 있습니다. [Journey Optimizer에서 계산된 특성을 사용하는 방법을 알아봅니다](#use)

Adobe Experience Platform 데이터 원본에 필드 그룹을 추가하는 방법에 대한 자세한 내용은 [이 섹션](../datasource/adobe-experience-platform-data-source.md)에서 확인할 수 있습니다.

## Journey Optimizer에서 계산된 속성 사용 {#use}

>[!NOTE]
>
>시작하기 전에 계산된 속성을 Adobe Experience Platform 데이터 소스에 추가했는지 확인하십시오. [이 섹션에서 방법을 알아보세요](#source).

계산된 속성은 여정 최적화 도구에서 다양한 기능 세트를 제공합니다. 메시지 콘텐츠를 개인화하거나, 새 대상을 만들거나, 특정 계산된 속성을 기반으로 여정을 분할하는 등 다양한 용도로 사용할 수 있습니다. 예를 들어, 조건 활동에 계산된 단일 속성을 추가하여 지난 3주 동안의 여정 총 구매를 기반으로 프로필의 경로를 분할할 수 있습니다. 각 프로필에 대해 가장 최근에 본 항목을 표시하여 이메일을 개인화할 수도 있습니다.

계산된 특성은 프로필 공용 구조체 스키마에서 만든 프로필 특성 필드이므로 **SystemComputedAttributes** 필드 그룹 내의 개인화 편집기에서 액세스할 수 있습니다. 여기에서 계산된 속성을 다른 프로필 속성과 마찬가지로 취급하여 표현식에 추가하여 원하는 작업을 수행할 수 있습니다.

![](assets/computed-attributes-ajo.png)
