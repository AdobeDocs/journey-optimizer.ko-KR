---
title: 의사 결정 관리 이벤트 시작
description: Adobe Experience Platform에서 의사 결정 관리 보고서를 만드는 방법을 알아봅니다.
feature: Offers
topic: Integrations
role: User
level: Beginner
exl-id: 51830c63-fa88-47e7-8605-192297fcf6b8
source-git-commit: b06b545d377fcd1ffe6ed218badeb94c1bb85ef2
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 56%

---

# 의사 결정 관리 이벤트 시작 {#monitor-offer-events}

의사 결정 관리 가 주어진 프로필에 대해 결정을 내릴 때마다 이러한 이벤트와 관련된 정보가 Adobe Experience Platform에 자동으로 전송됩니다.

이렇게 하면 이러한 데이터를 내보내 자체 보고 시스템으로 분석할 수 있습니다. 분석 및 보고 기능을 향상하기 위해 다른 도구와 함께 Adobe Experience Platform [쿼리 서비스](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=ko)를 활용할 수도 있습니다.

의사 결정 관리 이벤트가 포함된 데이터 세트는 Adobe Experience Platform에서 액세스할 수 있습니다 **[!UICONTROL 데이터 세트]** 메뉴 아래의 제품에서 사용할 수 있습니다. 각 인스턴스에 대해 프로비저닝할 때 데이터 세트 하나가 자동으로 만들어집니다.

![](../assets/events-datasets-list.png)

이러한 데이터 세트는 **[!UICONTROL 코드 결정 이벤트]** 스키마. 여기에는 의사 결정 관리에서 Adobe Experience Platform으로 정보를 전송하는 데 필요한 모든 XDM 필드가 포함되어 있습니다.

>[!NOTE]
>
>ODE DecisionEvents 데이터 세트는 **비프로필 데이터 세트**&#x200B;이므로 실시간 고객 프로필에서 사용하기 위해 Experience Platform으로 수집할 수 없습니다.

**관련 항목:**

* [의사 결정 관리 이벤트 주요 정보](../reports/key-information.md)
* [이벤트 XDM 필드 액세스](../reports/xdm-fields.md)
