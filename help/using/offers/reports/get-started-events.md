---
title: 의사 결정 관리 이벤트 작업
description: Adobe Experience Platform에서 의사 결정 관리 보고서를 만드는 방법을 알아봅니다.
feature: Offers
topic: Integrations
role: User
level: Beginner
exl-id: 51830c63-fa88-47e7-8605-192297fcf6b8
source-git-commit: a6a892ec20dfeb6879bef2f4c2eb4a0f8f54885f
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 100%

---

# 의사 결정 관리 이벤트 시작 {#monitor-offer-events}

[의사 결정 관리]에서 특정 프로필에 대해 의사 결정을 내릴 때마다 해당 이벤트와 관련된 정보가 자동으로 Adobe Experience Platform으로 보내집니다.

이를 통해 의사 결정에 대한 인사이트를 얻을 수 있습니다. 예를 들면 주어진 프로필에 제시한 오퍼를 파악할 수 있습니다. 이 데이터를 내보내 자체 보고 시스템에서 분석하거나, Adobe Experience Platform [쿼리 서비스](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=ko)를 다른 도구와 함께 활용하여 분석과 보고를 개선할 수 있습니다.

## 데이터 세트에서 사용할 수 있는 주요 정보 {#key-information}

결정이 내려질 때 전송되는 각 이벤트에는 분석 및 보고 용도로 활용할 수 있는 4개의 키 데이터 포인트가 포함되어 있습니다:

![](../assets/events-dataset-preview.png)

* **[!UICONTROL 대체]**: 맞춤형 오퍼를 선택하지 않은 경우 대체 제안의 이름과 ID,
* **[!UICONTROL 배치]**: 오퍼를 게재하는 데 사용되는 배치의 이름, ID, 채널,
* **[!UICONTROL 선택]**: 프로필에 대해 선택한 오퍼의 이름 및 ID,
* **[!UICONTROL 활동]**: 의사 결정의 이름 및 ID입니다.

또한 **[!UICONTROL identityMap]** 및 **[!UICONTROL Timestamp]** 필드를 활용하여 프로필의 정보와 오퍼가 게재된 시간을 검색할 수도 있습니다.

각 결정과 함께 전송되는 모든 XDM 필드에 대한 자세한 내용은 [이 섹션](xdm-fields.md)을 참조하십시오.

## 데이터 세트 액세스 {#access-datasets}

[의사 결정 관리] 이벤트가 있는 데이터 세트는 Adobe Experience Platform **[!UICONTROL 데이터 세트]** 메뉴에서 액세스할 수 있습니다. 각 인스턴스에 대해 프로비저닝할 때 데이터 세트 하나가 자동으로 만들어집니다.

![](../assets/events-datasets-list.png)

이 데이터 세트는 [의사 결정 관리]에서 Adobe Experience Platform으로 정보를 보내는 데 필요한 모든 XDM 필드가 있는 **[!UICONTROL ODE DecisionEvents]** 스키마를 기반으로 합니다.

>[!NOTE]
>
>ODE DecisionEvents 데이터 세트는 **비프로필 데이터 세트**&#x200B;이므로 실시간 고객 프로필에서 사용하기 위해 Experience Platform으로 수집할 수 없습니다.
