---
title: 의사 결정에 컨텍스트 데이터 활용
description: 의사 결정에서 컨텍스트 데이터를 활용하는 방법 알아보기
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
badge: label="제한 공개"
exl-id: ddc4b681-020b-4433-b4b3-3791c41907c9
source-git-commit: ac8ccb52bd16a26c14dea148f989256e28170765
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 0%

---

# 의사 결정에 컨텍스트 데이터 활용 {#context}

Decisioning을 사용하면 Adobe Experience Platform에서 사용할 수 있는 정보를 활용하여 [의사 결정 규칙](rules.md) 또는 [등급 수식](ranking.md)을 만드는 등 다양한 작업을 수행할 수 있습니다. 예를 들어 결정 요청이 수행된 시점에 현재 날씨가 ≥80도여야 하는 결정 규칙을 디자인할 수 있습니다.

>[!NOTE]
>
>컨텍스트 데이터는 Adobe Experience Platform에서 정의되며 의사 결정 요청 시 전송됩니다. 여기에는 이전 데이터가 포함되지 않습니다.

컨텍스트 데이터를 사용하려면 먼저 Decisioning에서 사용할 데이터를 정의해야 합니다. 완료되면 이 데이터는 의사 결정 규칙을 만들 때 사용할 수 있는 **[!UICONTROL 컨텍스트 데이터]** 탭에서 의사 결정에 원활하게 통합됩니다. 등급 수식을 편집할 때 데이터를 활용할 수도 있습니다.

![](assets/decision-rules-context.png)

Adobe Experience Platform 데이터를 사용하여 Decisioning에 데이터를 제공하는 단계는 다음과 같습니다.

1. Adobe Experience Platform 및 관련 **데이터 세트**&#x200B;에서 **경험 이벤트 스키마**&#x200B;를 만듭니다. [스키마를 만드는 방법 알아보기](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/resources/schemas){target="_blank"}

1. 새 Adobe Experience Platform 데이터스트림 만들기:

   1. **[!UICONTROL 데이터스트림]** 메뉴로 이동한 다음 **[!UICONTROL 새 데이터스트림]**&#x200B;을 선택합니다.

   1. **[!UICONTROL 이벤트 스키마]** 드롭다운 목록에서 이전에 만든 경험 이벤트 스키마를 선택한 다음 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

      ![](assets/decision-rule-context-datastream.png)

   1. **[!UICONTROL 서비스 추가]**&#x200B;를 클릭하고 &quot;Adobe Experience Platform&quot;를 서비스로 선택합니다. **[!UICONTROL 이벤트 데이터 세트]** 드롭다운 목록에서 이전에 만든 이벤트 데이터 세트를 선택하고 **[!UICONTROL Adobe Journey Optimizer]** 옵션을 활성화합니다.

      ![](assets/decision-rules-context-datastream-service.png)

데이터 스트림이 저장되면 선택한 데이터 세트의 정보를 자동으로 가져와 Decisioning에 통합합니다. 일반적으로 약 24시간 내에 사용할 수 있습니다.

Adobe Experience Platform을 사용하여 작업하는 방법에 대한 추가 지침을 보려면 다음 리소스를 살펴보십시오.

* [XDM(경험 데이터 모델) 스키마](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/composition){target="_blank"}
* [데이터 세트](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/overview){target="_blank"}
* [데이터스트림](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/overview){target="_blank"}
