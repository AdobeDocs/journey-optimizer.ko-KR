---
solution: Journey Optimizer
product: journey optimizer
title: 컴포지션 워크플로우 처음 만들기
description: 기존 대상자를 결합하고 정렬하는 작성 워크플로우를 만드는 방법을 알아봅니다.
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 8b978900-fcef-46f2-bc19-70776e4f3d43
source-git-commit: 01c14590fe55d8f11c1ff2b18141933b0b3dd5ca
workflow-type: tm+mt
source-wordcount: '444'
ht-degree: 15%

---

# 컴포지션 워크플로우 처음 만들기 {#create-compositions}

>[!BEGINSHADEBOX]

이 설명서에서는 Adobe Journey Optimizer 내에서 대상자 구성을 사용하는 방법에 대해 자세한 정보를 제공합니다. Adobe Journey Optimizer을 사용하지 않는 경우 [여기를 클릭](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/audience-composition.html?lang=ko){target="_blank"}하십시오.

>[!ENDSHADEBOX]

## 컴포지션 워크플로우 만들기 {#create}

작성 워크플로우를 만들려면 다음 단계를 수행합니다.

1. **[!UICONTROL 대상자]** 메뉴에 액세스하고 **[!UICONTROL 대상자 만들기]**&#x200B;를 선택하십시오.

1. **[!UICONTROL 대상자 작성]**&#x200B;을 선택합니다.

   ![](assets/audiences-create.png)

   >[!NOTE]
   >
   >**[!UICONTROL 빌드 규칙]** 만들기 메서드를 사용하면 [세그먼테이션 서비스](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=ko)를 사용하여 새 세그먼트 정의를 만들 수 있습니다.

1. 컴포지션 캔버스에는 다음과 같은 두 가지 기본 활동이 표시됩니다.

   * **[!UICONTROL 대상]**: 컴포지션의 시작점입니다. 이 활동을 사용하면 워크플로우의 기반으로 하나 이상의 대상을 선택할 수 있습니다.

   * **[!UICONTROL 저장]**: 컴포지션의 마지막 단계입니다. 이 활동을 사용하면 워크플로우의 결과를 새 대상자에 저장할 수 있습니다.

   컴포지션 워크플로 캔버스에서 활동을 구성하는 방법에 대한 자세한 내용은 [컴포지션 캔버스에서 작업](composition-canvas.md)을 참조하세요.

1. 컴포지션 속성을 열어 제목과 설명을 지정합니다.

   속성에 제목이 정의되지 않은 경우 컴포지션의 레이블이 &quot;Composition&quot;, 작성 날짜 및 시간으로 설정됩니다.

   ![](assets/audiences-properties.png)

1. **[!UICONTROL 대상]** 및 **[!UICONTROL 저장]** 활동 사이에 필요한 만큼 활동을 추가하여 구성을 구성합니다. [컴포지션 캔버스로 작업하는 방법을 알아봅니다](composition-canvas.md)

   ![](assets/audiences-publish.png)

1. 컴포지션이 준비되면 **[!UICONTROL Publish]** 단추를 클릭하여 컴포지션을 게시하고 결과 대상자를 Adobe Experience Platform에 저장합니다.

   >[!IMPORTANT]
   >
   >주어진 샌드박스에서 최대 10개의 컴포지션을 게시할 수 있습니다. 이 임계값에 도달한 경우 구성을 삭제하여 공간을 확보하고 새 구성을 게시해야 합니다.

   게시 중에 오류가 발생하면 문제 해결 방법에 대한 정보가 경고에 표시됩니다.

   ![](assets/audiences-alerts.png)

1. 컴포지션이 게시됩니다. 결과 대상자는 Adobe Experience Platform에 저장되며 Journey Optimizer에서 타깃팅할 준비가 되었습니다. [Journey Optimizer에서 대상을 타깃팅하는 방법 알아보기](../audience/about-audiences.md#segments-in-journey-optimizer)

## 컴포지션 액세스 {#access}

>[!CONTEXTUALHELP]
>id="ajo_ao_publish"
>title="대상자 게시"
>abstract="구성을 게시하여 최종 대상자를 Adobe Experience Platform에 저장합니다."

**[!UICONTROL 구성]** 탭에서 만든 모든 구성에 액세스할 수 있습니다. 목록의 줄임표 버튼을 사용하여 언제든지 기존 컴포지션을 복제하거나 삭제할 수 있습니다.

구성은 다음과 같은 여러 상태를 가질 수 있습니다.

* **[!UICONTROL 초안]**: 작성이 진행 중이고 게시되지 않았습니다.
* **[!UICONTROL 게시됨]**: 컴포지션이 게시되어 결과 대상이 저장되었으며 사용할 수 있습니다.

![](assets/audiences-compositions.png)

>[!NOTE]
>
>대상 구성은 현재 샌드박스 재설정 기능과 통합되지 않았습니다. 샌드박스 재설정을 시작하기 전에 관련 대상 데이터가 제대로 정리되도록 컴포지션을 수동으로 삭제해야 합니다. 자세한 내용은 Adobe Experience Platform [샌드박스 설명서](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html#delete-audience-compositions)를 참조하세요.
