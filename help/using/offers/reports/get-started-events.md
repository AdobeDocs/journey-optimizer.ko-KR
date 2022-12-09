---
title: 의사 결정 관리 이벤트 시작
description: Adobe Experience Platform에서 의사 결정 관리 보고서를 만드는 방법을 알아봅니다.
feature: Offers
topic: Integrations
role: User
level: Beginner
exl-id: 51830c63-fa88-47e7-8605-192297fcf6b8
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 0%

---

# 의사 결정 관리 이벤트 시작 {#monitor-offer-events}

의사 결정 관리 가 주어진 프로필에 대해 결정을 내릴 때마다 이러한 이벤트와 관련된 정보가 Adobe Experience Platform으로 자동 전송됩니다.

이를 통해 이러한 데이터를 내보내 자체 보고 시스템으로 분석할 수 있습니다. Adobe Experience Platform을 활용할 수도 있습니다 [쿼리 서비스](https://experienceleague.adobe.com/docs/experience-platform/query/home.html) 를 다른 도구와 결합하여 분석 및 보고를 향상시킵니다.

의사 결정 관리 이벤트가 포함된 데이터 세트는 Adobe Experience Platform에서 액세스할 수 있습니다 **[!UICONTROL Datasets]** 메뉴 아래의 제품에서 사용할 수 있습니다. 각 인스턴스에 대한 프로비저닝 시 하나의 데이터 세트가 자동으로 생성됩니다.

![](../assets/events-datasets-list.png)

이러한 데이터 세트는 **[!UICONTROL ODE DecisionEvents]** 스키마. 결정 관리에서 Adobe Experience Platform으로 정보를 전송하는 데 필요한 모든 XDM 필드를 포함합니다.

>[!NOTE]
>
>ODE DecisionEvents 데이터 세트는 **비프로필 데이터 세트**: 실시간 고객 프로필에서 사용하기 위해 Experience Platform에 수집할 수 없음을 의미합니다.

**관련 항목:**

* [의사 결정 관리 이벤트 주요 정보](../reports/key-information.md)
* [이벤트 XDM 필드 액세스](../reports/xdm-fields.md)
