---
solution: Journey Optimizer
product: journey optimizer
title: 세그먼트 정의 작성
description: 세그먼트 정의를 통해 대상자를 만드는 방법을 알아봅니다
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 289aac5d-6cdb-411f-985e-3acef58050a8
source-git-commit: 9fcf0e07edad27ab1eac3c29b26888fd99e26751
workflow-type: tm+mt
source-wordcount: '1017'
ht-degree: 17%

---

# 세그먼트 정의 작성 {#build-segments}

>[!CONTEXTUALHELP]
>id="ajo_ao_create_rule"
>title="규칙 만들기"
>abstract="규칙 빌드 만들기 메서드를 통해 Adobe Experience Platform 세분화 서비스를 사용하여 새 대상자 정의를 만들 수 있습니다."

## 세그먼트 정의 만들기 {#create}

이 예에서는 Atlanta, San Francisco 또는 Seattle에 거주하며 1980년 이후 출생한 모든 고객을 타깃팅하는 대상을 구성합니다. 이 모든 고객은 지난 7일 이내에 구매해야 합니다.

➡️0&rbrace;이 비디오에서 대상자를 만드는 방법을 알아보세요[&#128279;](#video-segment)

1. **[!UICONTROL 대상]** 메뉴에서 **[!UICONTROL 대상 만들기]** 단추를 클릭하고 **[!UICONTROL 규칙 빌드]**&#x200B;를 선택합니다.

   ![](assets/create-segment.png)

   세그먼트 정의 화면에서는 대상자를 정의하는 데 필요한 모든 필드를 구성할 수 있습니다. [세그먼테이션 서비스 설명서](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=ko){target="_blank"}에서 대상을 구성하는 방법을 알아보세요.

   ![](assets/segment-builder.png)

1. **[!UICONTROL 대상 속성]** 창에서 대상의 이름과 설명을 입력합니다(선택 사항).

   ![](assets/segment-properties.png)

1. 왼쪽 창에서 중앙 작업 영역으로 원하는 필드를 드래그하여 놓은 다음 필요에 따라 구성합니다.

   세그먼트 정의의 기본 구성 요소는 **특성** 및 **이벤트**&#x200B;입니다. 또한 기존 대상자에 포함된 속성 및 이벤트를 새 정의의 구성 요소로 사용할 수 있습니다. [세분화 서비스 설명서에서 자세히 알아보기](https://experienceleague.adobe.com/ko/docs/experience-platform/segmentation/ui/segment-builder#building-blocks){target="_blank"}

   >[!NOTE]
   >
   >왼쪽 창에서 사용할 수 있는 필드는 조직에 대해 **XDM 개인 프로필** 및 **XDM ExperienceEvent** 스키마를 구성한 방식에 따라 다릅니다.  자세한 내용은 [XDM(경험 데이터 모델) 설명서](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko-KR){target="_blank"}를 참조하세요.

   ![](assets/drag-fields.png)

   이 예제에서는 대상을 만들려면 **특성** 및 **이벤트** 필드를 사용해야 합니다.

   * **특성**: 1980년 이후에 태어난 애틀랜타, 샌프란시스코 또는 시애틀에 거주하는 프로필입니다.

     ![](assets/add-attributes.png)

   * **이벤트**: 지난 7일 내에 구매한 프로필입니다.

     ![](assets/add-events.png)

1. 작업 영역에서 새 필드를 추가하고 구성할 때 **[!UICONTROL 대상 속성]** 창이 대상에 속하는 예상 프로필에 대한 정보로 자동으로 업데이트됩니다.

   ![](assets/segment-estimate.png)

1. 대상자가 준비되면 **[!UICONTROL 저장]**&#x200B;을 클릭하세요. Adobe Experience Platform 대상자 목록에 표시됩니다. 목록의 특정 대상자를 검색하는 데 도움이 되는 검색 창을 사용할 수 있습니다.

이제 여정에서 대상을 사용할 수 있습니다. 이 작업에 대한 자세한 정보는 [이 섹션](../audience/about-audiences.md)을 참조하십시오.

## 대상자 평가 방법 {#evaluation-method-in-journey-optimizer}

Adobe Journey Optimizer에서 대상자는 아래 세 가지 평가 방법 중 하나를 사용하여 세그먼트 정의에서 생성됩니다.

+++ 스트리밍 세분화

대상에 대한 프로필 목록은 새 데이터가 시스템으로 유입될 때 실시간으로 최신 상태로 유지됩니다.

스트리밍 세분화는 사용자 활동에 대응하여 대상자를 업데이트하는 진행형 데이터 선택 프로세스입니다. 세그먼트 정의를 작성하고 결과 대상자를 저장한 다음부터는 Journey Optimizer로 들어오는 데이터에 세그먼트 정의가 적용됩니다. 즉, 프로필 데이터가 변경될 때 개인이 대상에서 추가되거나 제거되어 대상 대상이 항상 관련성이 있게 됩니다. [Adobe Expe에서 자세히 알아보기](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/streaming-segmentation.html?lang=ko){target="_blank"}

>[!IMPORTANT]
>
>2024년 11월 1일부터 스트리밍 세분화는 더 이상 Journey Optimizer 추적 및 피드백 데이터 세트에서 **send** 및 **open** 이벤트를 사용할 수 없습니다.
>
>* 이 변경 사항은 모든 고객 샌드박스 및 조직에 적용됩니다.
>* 전송 및 열기 이벤트만 영향을 받습니다. 클릭 수 및 기타 추적 이벤트는 스트리밍 세분화에 계속 사용할 수 있습니다.
>* 이 변경 사항은 스트리밍 세분화에만 적용됩니다. 보내기 및 열기 이벤트는 여전히 배치 세그먼트에서 사용할 수 있지만 스트리밍 세그먼트에 포함된 경우 배치 방식으로 평가됩니다. 또한 전송 이벤트로 인한 제외 이벤트 및 바운스/지연 이벤트도 이 변경의 영향을 받습니다.
>* 추적 데이터 수집은 영향을 받지 않습니다. 보내기 및 열기 이벤트는 평소와 같이 계속 수집됩니다.
>* 여정의 반응 이벤트는 이 변경의 영향을 받지 않습니다.

+++

+++ 배치 세분화

대상자에 대한 프로필 목록은 24시간마다 평가됩니다.

일괄 처리 세분화는 스트리밍 세분화 대신 사용할 수 있는 방법으로, 세그먼트 정의를 통해 모든 프로필 데이터를 한꺼번에 처리합니다. 이를 통해 대상자의 스냅샷을 만드는데, 이를 저장하거나 내보내서 사용할 수 있습니다. 하지만 스트리밍 세분화와 달리 배치 세분화는 실시간으로 대상 목록을 지속적으로 업데이트하지 않으며, 배치 프로세스 후에 들어오는 새 데이터는 다음 배치 프로세스가 진행될 때까지 대상에 반영되지 않습니다. 즉각적인 업데이트를 시도해도 일일 사이클이 재정의되지 않습니다. 즉각적인 증분 업데이트의 경우 스트리밍 또는 온디맨드 세분화 옵션을 사용하는 것이 좋습니다.

자세한 내용은 [Adobe Experience Platform 세그먼테이션 서비스 설명서](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=ko#batch){target="_blank"}를 참조하세요.

+++

+++ 에지 세분화

Edge 세그멘테이션은 Adobe Experience Platform의 세그먼트를 즉시 [edge](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=ko){target="_blank"}에서 평가하는 기능으로, 동일한 페이지 및 다음 페이지 개인화 사용 사례를 가능하게 합니다. 현재 선택한 쿼리 유형만 가장자리 세분화를 통해 평가할 수 있습니다. 자세한 내용은 [Adobe Experience Platform 세그먼테이션 서비스 설명서](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/edge-segmentation.html?lang=ko#query-types){target="_blank"}를 참조하세요.

+++

사용할 평가 방법을 알고 있는 경우 드롭다운 목록을 사용하여 선택합니다. 돋보기로 찾아보기 아이콘 폴더 아이콘을 클릭하여 사용 가능한 세그먼트 정의 평가 방법 목록을 볼 수도 있습니다. 자세한 내용은 [Adobe Experience Platform 세그먼테이션 서비스 설명서](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=ko#segment-properties){target="_blank"}를 참조하세요.

![](assets/evaluation-methods.png)

<!--The determination between batch segmentation and streaming segmentation is made by the system for each audience, based on the complexity and the cost of evaluating the segment definition rule. You can view the evaluation method for each audience in the **[!UICONTROL Evaluation method]** column of the audience list.
    
![](assets/evaluation-method.png)

>[!NOTE]
>
>If the **[!UICONTROL Evaluation method]** column does not display, you  need to add it using configuration button on the top right of the list.-->

대상을 처음 정의한 후 자격이 주어지면 프로필이 대상에 추가됩니다. 이전 데이터를 사용하여 대상자를 다시 채우는 데 최대 24시간이 걸릴 수 있습니다. 대상자를 다시 채운 후 대상자는 계속 최신 상태로 유지되며 언제든 타겟팅할 수 있습니다.

## 유연한 대상 평가 {#flexible}

Adobe Experience Platform 대상 포털을 사용하면 선택한 대상에 대해 온디맨드로 세분화 작업을 실행할 수 있으므로 Journey Optimizer 여정 및 캠페인에 타겟팅하기 전에 항상 최신 대상 데이터를 보유하게 됩니다.

유연한 대상 평가를 통해 다음과 같은 작업을 수행할 수 있습니다.

1. 최신 데이터를 기반으로 새 세그먼트를 만듭니다.
1. 실시간으로 대상자를 평가하여 정확성을 보장합니다. 특정 기준(예: 사람 기반, 세그먼테이션 서비스 원본)을 충족하는 경우, 평가하려는 대상을 선택하고 &quot;대상 평가&quot;를 선택합니다.
1. 정확한 타겟팅을 위해 Adobe Journey Optimizer 캠페인 또는 여정에서 평가된 대상자를 사용합니다.

한 번에 최대 20개의 대상을 평가할 수 있으며 부적격 대상은 자동으로 제외됩니다. 자세한 내용은 [Adobe Experience Platform 세그먼테이션 서비스 설명서](https://experienceleague.adobe.com/ko/docs/experience-platform/segmentation/ui/audience-portal#flexible-audience-evaluation)를 참조하세요.

## 사용 방법 비디오{#video-segment}

Journey Optimizer에서 규칙을 사용하여 대상자를 생성하는 원리를 이해하고 속성, 이벤트, 기존 대상자를 사용하여 대상자를 만드는 방법을 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/3425020?quality=12)
