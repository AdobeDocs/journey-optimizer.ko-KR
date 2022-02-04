---
title: 의사 결정 규칙 만들기
description: 오퍼를 표시할 수 있는 오퍼를 정의하는 의사 결정 규칙을 만드는 방법을 알아봅니다
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 401ce05b-412b-4fa0-a516-bf75727f6387
source-git-commit: 0545cda9f91ff18791310a4ee2463b2287ac7557
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 12%

---

# 의사 결정 규칙 만들기 {#create-decision-rules}

Adobe Experience Platform에서 사용할 수 있는 데이터를 기반으로 오퍼 의사 결정 규칙을 만들 수 있습니다. 의사 결정 규칙은 오퍼를 표시할 수 있는 대상을 결정합니다.

예를 들어 (Gender = &#39;Female&#39;) 및 (Region = &#39;Northeast&#39;)일 때만 &#39;여성용 겨울 의류 상품&#39;을 표시하도록 지정할 수 있습니다. 

➡️ [비디오에서 이 기능 살펴보기](#video)

만든 의사 결정 규칙 목록은 **[!UICONTROL Components]** 메뉴 아래의 제품에서 사용할 수 있습니다.

![](../../assets/decision_rules_list.png)

의사 결정 규칙을 만들려면 다음 단계를 수행합니다.

1. 로 이동합니다. **[!UICONTROL Rules]** 탭을 클릭한 다음 **[!UICONTROL Create rule]**.

   ![](../../assets/offers_decision_rule_creation.png)

1. 규칙에 이름을 지정하고 설명을 제공한 다음 필요에 따라 규칙을 구성합니다.

   이렇게 하려면 **세그먼트 빌더** 는 규칙 조건을 작성하는 데 도움이 될 수 있습니다. [자세히 알아보기](../../segment/about-segments.md)

   이 예에서는 규칙이 &quot;Gold&quot; 충성도 수준이 있는 고객을 타깃팅합니다.

   ![](../../assets/offers_decision_rule_creation_segment.png)

   >[!NOTE]
   >
   >의사 결정 규칙을 만들기 위해 제공된 세그먼트 빌더에서는 와 함께 사용되는 세그먼트 빌더와 비교하여 몇 가지 특성을 제공합니다 **[!UICONTROL Audience Destinations]** 서비스. 예: **[!UICONTROL Segments]** 탭을 사용할 수 없습니다. 하지만 세그먼트 빌더 설명서에 설명된 전역 프로세스는 오퍼 결정 규칙을 작성하는 데 여전히 유효합니다.

1. 클릭 **[!UICONTROL Save]** 확인합니다.

1. 규칙이 만들어지면 규칙 목록에 표시됩니다. 속성을 선택하여 등록 정보를 표시하고 편집하거나 삭제할 수 있습니다.

   ![](../../assets/rule_created.png)

>[!CAUTION]
>
>이벤트 기반 오퍼는에서 현재 지원되지 않습니다 [!DNL Journey Optimizer]. 을 기반으로 의사 결정 규칙을 생성하는 경우 [이벤트](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=en#events){target=&quot;_blank&quot;} 오퍼에서는 활용할 수 없습니다.

## 튜토리얼 비디오 {#video}

>[!NOTE]
>
>이 비디오는 Adobe Experience Platform을 기반으로 하는 Offer decisioning 애플리케이션 서비스에 적용됩니다. 그러나 Journey Optimizer 컨텍스트에서 오퍼를 사용하는 일반적인 지침을 제공합니다.

>[!VIDEO](https://video.tv.adobe.com/v/329373?quality=12)
