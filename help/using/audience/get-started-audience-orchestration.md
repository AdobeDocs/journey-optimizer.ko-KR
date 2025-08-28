---
solution: Journey Optimizer
product: journey optimizer
title: 대상자 컴포지션 시작
description: 대상자 구성에 대해 자세히 알아보기
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: af71d24d-77eb-44df-8216-b0aeaf4c4fa4
source-git-commit: 060d65e8d3fb1442b04626170a35d463d1faa514
workflow-type: tm+mt
source-wordcount: '1030'
ht-degree: 51%

---

# 대상자 컴포지션 시작 {#get-start-audience-composition}

>[!CONTEXTUALHELP]
>id="ajo_ao_create_composition"
>title="컴포지션 만들기"
>abstract="컴포지션 워크플로를 만들어 기존 Adobe Experience Platform 대상자를 시각적 캔버스로 결합하고 다양한 활동(분할, 제외...)을 활용하여 새 대상자를 생성합니다."

>[!CONTEXTUALHELP]
>id="ajo_ao_publish"
>title="대상자 게시"
>abstract="컴포지션을 게시하여 최종 대상자를 Adobe Experience Platform에 저장합니다."

>[!CONTEXTUALHELP]
>id="ajo_ao_audience"
>title="대상자 활동"
>abstract="대상자 활동을 통해 기존 대상에 속하는 추가 프로필이 컴포지션에 포함되도록 할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_ao_merge_types"
>title="병합 유형"
>abstract="선택한 대상자 프로필을 어떻게 병합해야 하는지 지정합니다."

>[!CONTEXTUALHELP]
>id="ajo_ao_exclude_type"
>title="제외 유형"
>abstract="대상 제외 유형을 사용하여 기존 대상자에 속하는 프로필을 제외합니다. 속성 유형을 사용하는 제외를 통해 특정 속성을 기반으로 프로필을 제외할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_ao_exclude"
>title="제외 활동"
>abstract="제외 활동을 통해 기존 대상자를 선택하거나 규칙을 사용하여 컴포지션에서 프로필을 제외할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_ao_enrich"
>title="보강 활동"
>abstract="보강 활동을 사용하여 Adobe Experience Platform 데이터 세트에서 제공되는 추가 속성으로 대상자를 보강합니다. 예를 들어 이름, 가격 또는 제조업체 ID와 같이 구매한 제품과 관련된 정보를 추가하고 이러한 정보를 활용하여 대상자에게 전송하는 게재를 개인화할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_ao_enrich_dataset"
>title="보강 데이터 세트"
>abstract="대상자에 연결하려는 데이터가 포함된 보강 데이터 세트를 선택합니다."

>[!CONTEXTUALHELP]
>id="ajo_ao_enrich_criteria"
>title="보강 기준"
>abstract="소스 데이터 세트(즉, 대상자 및 보강 데이터 세트) 사이의 조정 키로 사용할 필드를 선택합니다."

>[!CONTEXTUALHELP]
>id="ajo_ao_enrich_attributes"
>title="보강 속성"
>abstract="보강 데이터 세트에서 하나 또는 여러 속성을 선택하여 대상자와 연결합니다. 컴포지션이 게시되면 해당 속성을 대상자에 연결하고 Journey Optimizer 캠페인에서 활용하여 게재 정보를 개인화할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_ao_ranking"
>title="순위 활동"
>abstract="순위 활동을 통해 특정 속성을 기반으로 프로필의 순위를 지정하고 컴포지션에 포함할 수 있습니다. 예를 들어 로열티 포인트가 가장 많은 50개의 프로필이 구성에 포함됩니다."

>[!CONTEXTUALHELP]
>id="ajo_ao_rank_profilelimit_text"
>title="프로필 제한 추가"
>abstract="이 옵션을 토글하여 이 컴포지션에 포함할 최대 프로필 수를 지정합니다."

<!-- [!CONTEXTUALHELP]
>id="ajo_ao_control_group_text"
>title="Control Group"
>abstract="Use control groups to isolate a portion of the profiles. This allows you to measure the impact of a marketing activity and make a comparison with the behavior of the rest of the population."-->

>[!CONTEXTUALHELP]
>id="ajo_ao_split"
>title="분할 활동"
>abstract="분할 활동을 통해 컴포지션을 여러 경로로 나눌 수 있습니다. 컴포지션을 게시할 때 하나의 대상자가 각 경로의 Adobe Experience Platform에 저장됩니다."

>[!CONTEXTUALHELP]
>id="ajo_ao_split_type"
>title="분할 유형"
>abstract="% 분할 유형을 사용하여 프로필을 여러 경로로 임의 분할합니다. 속성 분할 유형을 사용하여 특정 속성을 기반으로 프로필을 분할할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_ao_split_otherprofiles_text"
>title="기타 프로필"
>abstract="이 옵션을 토글하여 다른 경로에 지정된 조건과 일치하지 않는 나머지 프로필로 추가 경로를 만듭니다."

>[!BEGINSHADEBOX]

이 설명서에서는 Adobe Journey Optimizer 내에서 대상자 컴포지션을 사용하는 방법에 대해 자세한 정보를 제공합니다. 실시간 고객 프로필 전용 고객이고 Adobe Journey Optimizer를 사용하지 않는 경우 [여기를 클릭하세요](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/audience-composition.html?lang=ko){target="_blank"}.

>[!ENDSHADEBOX]

대상 구성을 사용하면 **구성 워크플로**&#x200B;를 만들 수 있습니다. 이 워크플로우에서는 기존 Adobe Experience Platform 대상을 시각적 캔버스로 결합하고 다양한 활동(분할, 제외...)을 활용하여 새 대상을 만들 수 있습니다.

완료되면 **결과 대상**이 기존 대상과 함께 Adobe Experience Platform에 저장되며 Journey Optimizer 캠페인 및 여정에서 타겟 고객에게 활용될 수 있습니다. Journey Optimizer에서 대상을 타기팅하는 방법 알아보기
![](assets/audiences-process.png)

>[!IMPORTANT]
>
>* 대상자 작성의 대상자 및 속성은 현재 Healthcare Shield 또는 Privacy and Security Shield에서 사용할 수 없습니다.
>
>* 데이터 보강 속성은 아직 정책 시행 서비스와 통합되지 않았습니다. 따라서 데이터 보강 속성에 적용하는 데이터 사용 레이블은 Journey Optimizer 캠페인 또는 여정에 적용되지 않습니다.

대상자 컴포지션 기능은 Adobe Journey Optimizer의 **[!UICONTROL 대상자]** 메뉴에서 액세스할 수 있습니다.

![](assets/audiences-browse.png)

* **[!UICONTROL 개요]** 탭에는 조직의 대상자 데이터 관련 주요 지표를 볼 수 있는 전용 대시보드가 있습니다. 자세한 내용은 [Adobe Experience Platform 대시보드 안내서](https://experienceleague.adobe.com/docs/experience-platform/dashboards/guides/segments.html?lang=ko)를 참조하십시오.

* **[!UICONTROL 찾아보기]** 탭에는 Adobe Experience Platform에 저장된 기존 대상자의 전체 목록이 있습니다.

* **[!UICONTROL 컴포지션]** 탭에서는 구성 워크플로를 만들 수 있습니다. 만든 워크플로로 대상자를 결합하고 배열하여 새로운 대상자를 만들 수 있습니다.

## 컴포지션 워크플로우 만들기 {#create}

작성 워크플로우를 만들려면 다음 단계를 수행합니다.

1. **[!UICONTROL 대상자]** 메뉴에 액세스하고 **[!UICONTROL 대상자 만들기]**&#x200B;를 선택하십시오.

1. **[!UICONTROL 대상자 작성]**&#x200B;을 선택합니다.

   ![](assets/audiences-create.png)

1. 컴포지션 캔버스에는 다음과 같은 두 가지 기본 활동이 표시됩니다.

   * **[!UICONTROL 대상]**: 컴포지션의 시작점입니다. 이 활동을 사용하면 워크플로우의 기반으로 하나 이상의 대상을 선택할 수 있습니다.

   * **[!UICONTROL 저장]**: 컴포지션의 마지막 단계입니다. 이 활동을 사용하면 워크플로우의 결과를 새 대상자에 저장할 수 있습니다.

1. 컴포지션 속성을 열어 제목과 설명을 지정합니다.

   속성에 제목이 정의되지 않은 경우 컴포지션의 레이블이 &quot;Composition&quot;, 작성 날짜 및 시간으로 설정됩니다.

   ![](assets/audiences-properties.png)

1. **[!UICONTROL 대상]** 및 **[!UICONTROL 저장]** 활동 사이에 필요한 만큼 활동을 추가하여 구성을 구성합니다. 컴포지션을 만드는 방법에 대한 자세한 내용은 [대상 컴포지션 설명서](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-composition)를 참조하세요.

   ![](assets/audiences-publish.png)

1. 컴포지션이 준비되면 **[!UICONTROL 게시]** 단추를 클릭하여 컴포지션을 게시하고 결과 대상자를 Adobe Experience Platform에 저장합니다.

   >[!IMPORTANT]
   >
   >주어진 샌드박스에서 최대 10개의 컴포지션을 게시할 수 있습니다. 이 임계값에 도달한 경우 컴포지션을 삭제하여 공간을 확보하고 새 컴포지션을 게시해야 합니다.

   게시 중에 오류가 발생하면 문제 해결 방법에 대한 정보가 경고에 표시됩니다.

   ![](assets/audiences-alerts.png)

1. 컴포지션이 게시됩니다. 결과 대상자는 Adobe Experience Platform에 저장되며 Journey Optimizer에서 타깃팅할 준비가 되었습니다. [Journey Optimizer에서 대상을 타깃팅하는 방법 알아보기](../audience/about-audiences.md#segments-in-journey-optimizer)

>[!NOTE]
>
>**대상 구성**&#x200B;의 대상은 매일 실행되므로 Journey Optimizer에서 사용하려면 최대 24시간을 기다려야 할 수 있습니다. 대상 구성 대상의 풍부한 속성은 마지막 구성 실행만큼 신선하며 과거에는 최대 24시간까지 소요될 수 있습니다.

## 컴포지션 액세스 {#access}

**[!UICONTROL 구성]** 탭에서 만든 모든 구성에 액세스할 수 있습니다. 목록의 줄임표 버튼을 사용하여 언제든지 기존 컴포지션을 복제하거나 삭제할 수 있습니다.

컴포지션에는 여러 가지 상태가 있을 수 있습니다.

* **[!UICONTROL 초안]**: 작성이 진행 중이고 게시되지 않았습니다.
* **[!UICONTROL 게시됨]**: 컴포지션이 게시되어 결과 대상이 저장되었으며 사용할 수 있습니다.

![](assets/audiences-compositions.png)

>[!NOTE]
>
>대상 구성은 현재 샌드박스 재설정 기능과 통합되지 않았습니다. 샌드박스 재설정을 시작하기 전에 관련 대상 데이터가 제대로 정리되도록 컴포지션을 수동으로 삭제해야 합니다. 자세한 내용은 Adobe Experience Platform [샌드박스 설명서](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html#delete-audience-compositions)를 참조하세요.
