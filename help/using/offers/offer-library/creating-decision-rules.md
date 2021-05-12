---
title: 의사 결정 규칙 만들기
description: Adobe Experience Platform에서 의사 결정 규칙을 만드는 방법을 알아봅니다.
translation-type: tm+mt
source-git-commit: db7fd318b14d01a0369c934a3e01c6e368d7658d
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 12%

---

# 의사 결정 규칙 만들기 {#creating-decision-rules}

Adobe Experience Platform에서 사용할 수 있는 데이터를 기반으로 오퍼 결정 규칙을 만들 수 있습니다. 의사 결정 규칙은 오퍼를 표시할 사람을 결정합니다.

예를 들어 (Gender = &#39;Female&#39;) 및 (Region = &#39;Northeast&#39;)일 때만 &#39;여성용 겨울 의류 상품&#39;을 표시하도록 지정할 수 있습니다. 

![](../../assets/do-not-localize/how-to-video.png) [비디오에서 이 기능 살펴보기](#video)

만든 결정 규칙 목록은 **[!UICONTROL Components]** 메뉴에서 액세스할 수 있습니다.

![](../../assets/decision_rules_list.png)

결정 규칙을 만들려면 다음 단계를 수행합니다.

1. **[!UICONTROL Rules]** 탭으로 이동한 다음 **[!UICONTROL Create rule]**&#x200B;를 클릭합니다.

   ![](../../assets/offers_decision_rule_creation.png)

1. 규칙의 이름을 지정하고 설명을 제공한 다음 필요에 따라 규칙을 구성합니다.

   이렇게 하려면 규칙 조건을 작성하는 데 도움이 되는 Adobe Experience Platform의 **세그먼트 빌더**&#x200B;를 사용할 수 있습니다. 사용 방법에 대한 자세한 내용은 [전용 설명서](https://docs.adobe.com/content/help/en/experience-platform/segmentation/ui/segment-builder.html)를 참조하십시오.

   이 예에서는 &quot;Gold&quot; 충성도 수준이 있는 고객을 대상으로 합니다.

   ![](../../assets/offers_decision_rule_creation_segment.png)

   >[!NOTE]
   >
   >의사 결정 규칙을 만들기 위해 제공된 세그먼트 빌더는 **[!UICONTROL Audience Destinations]** 서비스에 사용된 세그먼트 빌더와 비교하여 몇 가지 특정 특성을 제공합니다. 예를 들어 **[!UICONTROL Segments]** 탭을 사용할 수 없습니다. 하지만 세그먼트 빌더 설명서에 설명된 글로벌 프로세스는 오퍼 결정 규칙을 만드는 데 여전히 유효합니다.

1. **[!UICONTROL Save]**&#x200B;을 클릭하여 확인합니다.

1. 규칙이 만들어지면 규칙 목록에 표시됩니다. 속성을 표시하고 이를 편집하거나 삭제할 수 있도록 선택할 수 있습니다.

   ![](../../assets/rule_created.png)

## 자습서 비디오 {#video}

>[!NOTE]
>
>이 비디오는 Adobe Experience Platform 기반으로 구축된 Offer decisioning 응용 프로그램 서비스에 적용됩니다. 그러나 Journey Optimizer 컨텍스트에서 오퍼를 사용하기 위한 일반적인 지침을 제공합니다.

>[!VIDEO](https://video.tv.adobe.com/v/329373?quality=12)
