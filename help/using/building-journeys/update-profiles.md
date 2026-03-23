---
solution: Journey Optimizer
product: journey optimizer
title: 프로필 업데이트
description: 여정에서 프로필 업데이트 활동을 사용하는 방법 알아보기
feature: Journeys, Profiles, Activities
topic: Content Management
role: User
level: Intermediate
keywords: 프로필, 업데이트, 여정, 활동
exl-id: 8b2b2d1e-9bd1-439d-a15e-acdbab387c4b
version: Journey Orchestration
source-git-commit: 5383e0af430188dadd3e9ee259253115f7f1992d
workflow-type: tm+mt
source-wordcount: '862'
ht-degree: 4%

---

# 프로필 업데이트 {#update-profile}

>[!CONTEXTUALHELP]
>id="ajo_journey_update_profiles"
>title="프로필 활동 업데이트"
>abstract="프로필 업데이트 액션 활동을 사용하여 이벤트, 데이터 소스 또는 특정 값을 사용하여 도출하는 데이터로 기존 [!DNL Adobe Experience Platform] 프로필을 업데이트할 수 있습니다."

고객이 여정 과정을 진행할 때 **[!UICONTROL 프로필 업데이트]** 작업 활동을 사용하여 기존 [!DNL Adobe Experience Platform] 프로필을 보강하거나 수정하십시오. 여정 이벤트, 구성된 데이터 소스 또는 정적 값에서 가져온 필드 값을 설정할 수 있으므로 여정 캔버스를 벗어나지 않고도 프로필 데이터를 정확하고 실행 가능하게 유지할 수 있습니다. 이 활동을 구성하기 전에 적용되는 [보호 기능 및 제한 사항](#guardrails)을 검토하십시오.

## 데이터 세트 선택 {#dataset-selection}

**[!UICONTROL 프로필 업데이트]** 활동에는 업데이트를 저장할 전용 데이터 세트가 필요합니다. 이 활동은 [프로필 저장소](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html#profile-data-store){target="_blank"}만 업데이트하므로(Datalake는 아님), 모든 업데이트는 [프로필 업데이트](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/user-guide#enable-profile){target="_blank"} 작업에 대해 특별히 지정된 **[!UICONTROL 프로필 사용 데이터 세트]**&#x200B;에 저장되어야 합니다.

>[!CAUTION]
>
>일괄 처리 또는 스트리밍 수집에도 사용되는 데이터 세트를 사용하지 마십시오. 다른 수집 실행은 **[!UICONTROL 프로필 업데이트]** 작업의 변경 내용을 덮어쓰게 되어 프로필 특성이 사라지거나 이전 값으로 되돌아갑니다. 이 비헤이비어를 관찰하는 경우 Adobe Experience Platform에서 다른 수집이 동일한 데이터 세트에 기록되지 않는지 확인하십시오. 문제 해결 단계는 [Adobe Journey Optimizer에서 프로필 업데이트 오류 해결](https://experienceleague.adobe.com/ko/docs/experience-cloud-kcs/kbarticles/ka-26352){target="_blank"}을 참조하십시오.

또한 **[!UICONTROL 프로필 업데이트]** 활동 구성에는 [ID 네임스페이스](https://experienceleague.adobe.com/ko/docs/experience-platform/identity/features/namespaces){target="_blank"}가 필요하지 않습니다. 따라서 선택한 데이터 집합이 여정을 시작한 작업에서 사용한 것과 동일한 **[!UICONTROL ID 네임스페이스]**&#x200B;을(를) 이 네임스페이스와 동일하게 사용하도록 하십시오. 선택한 데이터 세트에서 ID 맵을 사용할 수도 있습니다. 올바른 ID 네임스페이스가 있는 데이터 집합 또는 ID 맵을 사용하는 데이터 집합을 선택하지 않으면 **[!UICONTROL 프로필 업데이트]** 활동이 실패합니다.

## 프로필 업데이트 활동 구성 {#use-profile-update}

여정에서 **[!UICONTROL 프로필 업데이트]** 활동을 구성하려면 아래 단계를 따르십시오.

1. 여정 디자인을 시작합니다. [첫 번째 여정 만들기](../building-journeys/journey-gs.md)에서 자세히 알아보세요.

1. 팔레트의 **[!UICONTROL 작업]** 섹션에서 **[!UICONTROL 프로필 업데이트]** 활동을 캔버스에 놓습니다.

   ![작업 아래의 여정 팔레트에서 프로필 활동 업데이트](assets/profileupdate0.png)

1. 목록에서 스키마를 선택합니다.

   >[!NOTE]
   >
   >선택한 XDM 프로필 스키마에 이미 있는 필드만 선택할 수 있습니다. 필요한 필드가 나열되지 않으면 먼저 Adobe Experience Platform의 스키마에 추가합니다.

1. 업데이트할 필드를 선택하려면 **[!UICONTROL 필드]**&#x200B;를 클릭하십시오.

   ![업데이트할 필드 선택](assets/profileupdate2.png)

1. 목록에서 데이터 세트를 선택합니다.

   >[!NOTE]
   >
   >**[!UICONTROL 프로필 업데이트]** 작업은 프로필 데이터를 실시간으로 업데이트하지만 데이터 세트는 업데이트되지 않습니다. 프로필이 데이터 세트와 관련된 레코드이므로 데이터 세트를 선택해야 합니다.

1. 사용할 값을 정의하려면 **[!UICONTROL 값]** 필드를 클릭합니다.

   * 단순 표현식 편집기를 사용하여 데이터 소스 또는 수신 이벤트에서 필드를 선택할 수 있습니다.

     ![프로필 특성 업데이트에 대한 단순 모드 필드 선택기](assets/profileupdate4.png)

   * 특정 값을 정의하거나 고급 함수를 사용하려면 [**[!UICONTROL 고급 모드]**](expression/expressionadvanced.md)를 선택하십시오.

     ![복잡한 프로필 업데이트를 위한 고급 모드 식 편집기](assets/profileupdate3.png)

1. 같은 작업에서 추가 프로필 특성을 업데이트하려면 **[!UICONTROL 다른 필드 업데이트]**&#x200B;를 클릭하고 필드 및 값 선택을 반복합니다. 단일 **[!UICONTROL 프로필 업데이트]** 작업에서 최대 5개의 필드/값 쌍을 추가할 수 있습니다. [보호 기능 및 제한 사항](#guardrails)을 참조하세요.

이제 **[!UICONTROL 프로필 업데이트]** 활동이 구성되었습니다.

![여러 필드 구성이 있는 여정의 프로필 업데이트 활동](assets/profileupdate1.png)


## 프로필 업데이트 테스트 {#using-the-test-mode}

[테스트 모드](testing-the-journey.md)에서 프로필 업데이트는 테스트 프로필에 즉시 적용되며 시뮬레이션되지 않습니다.

테스트 프로필만 테스트 모드에서 여정에 들어갈 수 있습니다. 새 테스트 프로필을 만들거나 기존 프로필을 테스트 프로필로 변환할 수 있습니다. [!DNL Adobe Experience Platform]에서 프로필 특성은 CSV 파일 가져오기 또는 API 호출을 통해 업데이트할 수 있습니다. 보다 빠른 대안은 여정 자체 내에서 **[!UICONTROL 프로필 업데이트]** 활동을 사용하여 테스트 프로필 부울 필드를 true로 설정하는 것입니다.

기존 프로필을 테스트 프로필로 변환하는 방법에 대한 자세한 내용은 이 [섹션](../audience/creating-test-profiles.md#create-test-profiles-csv)을 참조하세요.

## 가드레일 및 제한 사항 {#guardrails}

* **[!UICONTROL 프로필 업데이트]** 작업은 [네임스페이스](../event/about-creating.md#select-the-namespace)가 있는 프로필에서만 사용할 수 있습니다.
* 이 작업은 기존 필드만 업데이트합니다. 새 프로필 필드는 만들어지지 않습니다.
* 이 작업은 간단한 필드 유형(문자열, 숫자, 부울)만 지원합니다. 열거형, 제안 값, 개체 배열 또는 복잡한 컬렉션(예: 제품 목록)으로 정의된 XDM 필드는 지원되지 않습니다.
* **[!UICONTROL 프로필 업데이트]** 작업을 사용하여 구매와 같은 [경험 이벤트](../event/about-events.md)를 생성할 수 없습니다.
* 다른 작업과 마찬가지로 오류 또는 시간 초과 시 [대체 경로를 정의할 수 있습니다](using-the-journey-designer.md#paths). 두 가지 작업을 동시에 수행할 수 없습니다.
* 프로필 업데이트는 동일한 여정에서 다운스트림으로 즉시 사용할 수 없습니다. 업데이트된 값이 아직 반영되지 않았을 수 있으므로 필드를 작성하는 **[!UICONTROL 프로필 업데이트]** 작업 바로 뒤에 필드를 읽는 작업을 삽입하지 마십시오.
* **[!UICONTROL 프로필 업데이트]** 활동은 데이터 레이크가 아닌 [프로필 저장소](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html#profile-data-store){target="_blank"}만 업데이트합니다.
* 하나의 **[!UICONTROL 프로필 업데이트]** 작업에서 최대 5개의 필드/값 쌍을 업데이트할 수 있습니다. **[!UICONTROL 다른 필드 업데이트]** 단추를 사용하여 쌍을 더 추가합니다.
* 성능을 향상시키기 위해 여러 특성 업데이트를 특성당 하나의 동작을 사용하지 않고 단일 **[!UICONTROL 프로필 업데이트]** 동작으로 그룹화합니다.
