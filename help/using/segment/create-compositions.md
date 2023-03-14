---
solution: Journey Optimizer
product: journey optimizer
title: 첫 번째 컴포지션 워크플로우 만들기
description: 기존 대상자를 결합하고 정렬하는 작성 워크플로우를 만드는 방법을 알아봅니다.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 8b978900-fcef-46f2-bc19-70776e4f3d43
badge: label="Beta" type="정보"
source-git-commit: 160e4ce03d3be975157c30fbe511875a85b00551
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 3%

---

# 첫 번째 컴포지션 워크플로우 만들기 {#create-compositions}

>[!BEGINSHADEBOX]

이 설명서에서 찾을 수 있는 내용:

* [대상자 구성 시작](get-started-audience-orchestration.md)
* **[첫 번째 컴포지션 워크플로우 만들기](create-compositions.md)**
* [컴포지션 캔버스 작업](composition-canvas.md)
* [대상자 액세스 및 관리](access-audiences.md)

>[!ENDSHADEBOX]

## 컴포지션 워크플로우 만들기 {#create}

작성 워크플로우를 만들려면 다음 단계를 수행합니다.

1. 액세스 **[!UICONTROL 세그먼트]** 메뉴 및 선택 **[!UICONTROL 대상자 만들기]**.

1. 선택 **[!UICONTROL 대상자 작성]**.

   >[!NOTE]
   >
   >다음 **[!UICONTROL 규칙 작성]** 생성 방법을 사용하면 다음을 사용하여 새 세그먼트 정의를 생성할 수 있습니다. [세분화 서비스](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html).

   ![](assets/audiences-create.png)

1. 컴포지션 캔버스에는 다음과 같은 두 가지 기본 활동이 표시됩니다.

   * **[!UICONTROL 대상자]**: 컴포지션의 시작점입니다. 이 활동을 사용하면 워크플로우의 기반으로 하나 이상의 대상을 선택할 수 있습니다.

   * **[!UICONTROL 저장]**: 컴포지션의 마지막 단계입니다. 이 활동을 사용하면 워크플로우의 결과를 새 대상자에 저장할 수 있습니다.
   작성 워크플로 캔버스에서 활동을 구성하는 방법에 대한 자세한 내용은 다음을 참조하십시오. [컴포지션 캔버스 작업](composition-canvas.md).

1. 컴포지션 속성을 열어 제목과 설명을 지정합니다.

   속성에 제목이 정의되지 않은 경우 컴포지션의 레이블이 &quot;Composition&quot;, 작성 날짜 및 시간으로 설정됩니다.

   ![](assets/audiences-properties.png)

1. 사이에 필요한 만큼 활동을 추가하여 컴포지션을 구성합니다. **[!UICONTROL 대상자]** 및 **[!UICONTROL 저장]** 활동. [컴포지션 캔버스 작업 방법 알아보기](composition-canvas.md)

   ![](assets/audiences-publish.png)

1. 컴포지션이 준비되면 **[!UICONTROL 게시]** 단추를 클릭하여 컴포지션을 게시하고 결과 대상자를 Adobe Experience Platform에 저장합니다.

   게시 중에 오류가 발생하면 문제 해결 방법에 대한 정보가 경고에 표시됩니다.

   ![](assets/audiences-alerts.png)

1. 컴포지션이 게시됩니다. 결과 대상자는 Adobe Experience Platform에 저장되고 Journey Optimizer 캠페인에서 타겟팅할 준비가 되었습니다. [캠페인 작업 방법 알아보기](../campaigns/get-started-with-campaigns.md)

## 컴포지션 액세스 {#access}

>[!CONTEXTUALHELP]
>id="ajo_ao_publish"
>title="대상자 게시"
>abstract="컴포지션을 게시하여 결과 대상자를 Adobe Experience Platform에 저장합니다."

생성된 모든 컴포지션은 **[!UICONTROL 컴포지션]** 탭. 다음과 같은 여러 상태를 가질 수 있습니다.

* **[!UICONTROL 초안]**: 컴포지션이 진행 중이며 게시되지 않았습니다.
* **[!UICONTROL 게시됨]**: 컴포지션이 게시되어 결과 대상이 저장되고 사용할 수 있습니다.
* **[!UICONTROL 보관됨]**: 컴포지션이 보관되었습니다.

![](assets/audiences-compositions.png)

>[!NOTE]
>
>목록의 줄임표 버튼을 사용하여 언제든지 기존 컴포지션을 복제하거나 삭제할 수 있습니다.
