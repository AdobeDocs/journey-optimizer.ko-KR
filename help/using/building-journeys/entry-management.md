---
solution: Journey Optimizer
product: journey optimizer
title: 프로필 항목 관리
description: 프로필 항목 관리 방법 알아보기
feature: Journeys, Profiles
role: User
level: Intermediate
keywords: 재입력, 여정, 프로필, 반복
exl-id: 8874377c-6594-4a5a-9197-ba5b28258c02
source-git-commit: 135dd7528e87a6fde7e148745ef2f49104809bc1
workflow-type: tm+mt
source-wordcount: '701'
ht-degree: 5%

---


# 프로필 시작 관리 {#entry-management}

여정 등록 관리는 프로필 유형에 따라 다릅니다. Adobe Journey Optimizer에서는 다음 유형의 여정을 사용할 수 있습니다.

* **단일 이벤트** 여정: 이러한 여정은 단일 이벤트로 시작합니다. 이벤트가 수신되면 관련 프로필이 여정에 들어갑니다. [자세히 보기](#entry-unitary)

* **비즈니스 이벤트** 여정: 이 여정은 비즈니스 이벤트로 바로 시작한 다음 **대상자 읽기** 활동으로 시작합니다. 이벤트가 수신되면 타겟팅된 대상에 속하는 프로필이 여정에 들어갑니다. 각 프로필에 대해 이 여정의 인스턴스가 하나씩 생성됩니다. [자세히 보기](#entry-business)

* **대상자 읽기** 여정: 이 여정은 **대상자 읽기** 활동으로 시작합니다. 여정이 실행되면 타겟팅된 대상에 속하는 프로필이 여정에 들어갑니다. 각 프로필에 대해 이 여정의 인스턴스가 하나씩 생성됩니다. 이러한 여정은 반복 또는 &quot;일회성&quot;일 수 있습니다. [자세히 보기](#entry-read-audience)

* **대상 자격** 여정: 이 여정은 대상 자격 이벤트로 시작합니다. 이러한 여정은 대상자의 프로필 출입구를 수신합니다. 이런 경우 관련 프로필이 여정에 들어갑니다. [자세히 보기](#entry-unitary)

모든 여정 유형에서 프로필은 동일한 여정에 동시에 여러 번 나타날 수 없습니다. 개인이 여정에 있는지 확인하기 위해 프로필 ID가 키로 사용됩니다. 시스템에서는 동일한 키(예: 키 CRMID=3224)가 동일한 여정의 다른 위치에 있는 것을 허용하지 않습니다.

## 단일 이벤트 및 대상 자격 여정{#entry-unitary}

**단일 이벤트** 및 **대상 자격** 여정에서 재등록을 활성화하거나 비활성화할 수 있습니다.

* 재입력이 활성화된 경우 프로필은 여정을 여러 번 입력할 수 있지만 여정의 이전 인스턴스를 완전히 종료할 때까지는 다시 입력할 수 없습니다.

* 재입력이 비활성화된 경우 프로필은 글로벌 여정 시간 제한 기간 내에 동일한 여정을 여러 번 입력할 수 없습니다. 이 [섹션](../building-journeys/journey-properties.md#global_timeout)을 참조하세요.

기본적으로 여정은 다시 입력할 수 있습니다. **다시 입력 허용** 옵션이 활성화되면 **다시 입력 대기 기간** 필드가 표시됩니다. 프로필에서 여정을 다시 입력할 수 있도록 허용하기 전에 대기할 시간을 정의할 수 있습니다. 이를 통해 동일한 이벤트에 대해 여정을 여러 번 트리거하는 오류를 방지할 수 있습니다. 이 필드는 기본적으로 5분으로 설정되어 있습니다. 최대 기간은 91일([전역 시간 초과](journey-properties.md#global_timeout))입니다.

<!--
When a journey ends, its status is **[!UICONTROL Closed]**. New individuals can no longer enter the journey. Persons already in the journey automatically exit the journey. 
-->

![](assets/journey-re-entrance.png)

재입장 기간이 지나면 프로필이 여정에 재입장할 수 있다. 이를 방지하고 이러한 프로필에 대한 재입력을 완전히 비활성화하려면 프로필 또는 대상 데이터를 사용하여 프로필이 이미 입력되었는지 여부를 테스트하는 조건을 추가할 수 있습니다.

<!--
Due to the 30-day journey timeout, when journey re-entrance is not allowed, we cannot make sure the re-entrance blocking will work more than 91 days. Indeed, as we remove all information about persons who entered the journey 91 days after they enter, we cannot know the person entered previously, more than 91 days ago. -->

## 비즈니스 여정 {#entry-business}

<!--
Business events follow re-entrance rules in the same way as for unitary events. If a journey allows re-entrance, the next business event will be processed.
-->

**비즈니스 여정**&#x200B;에서 여러 비즈니스 이벤트 실행을 허용하려면 여정 속성의 **[!UICONTROL 실행]** 섹션에서 해당 옵션을 활성화합니다.

![](assets/business-entry.png)

비즈니스 이벤트의 경우, 주어진 여정의 경우 첫 번째 실행 시 검색된 대상 데이터가 1시간 기간 동안 재사용됩니다.

프로필은 동일한 여정에 동시에 여러 번 표시될 수 있지만, 서로 다른 비즈니스 이벤트의 컨텍스트에 있을 수 있습니다.

자세한 정보는 이 [섹션](../event/about-creating-business.md)을 참조하세요.

## 대상자 여정 읽기 {#entry-read-audience}

**대상자 읽기** 여정은 반복 또는 &quot;일회성&quot;일 수 있습니다.

* 반복되지 않는/&quot;단발성&quot; 여정의 경우: 프로필은 여정에 한 번만 입력합니다.

* 반복 여정의 경우: 기본적으로 대상에 속하는 모든 프로필은 각 반복에 여정을 입력합니다. 다른 경우에 다시 입력하기 전에 여정을 완료해야 합니다.

반복 대상자 읽기 여정에 두 가지 옵션을 사용할 수 있습니다.

* **증분 읽기** 옵션: 반복 **대상자 읽기**&#x200B;를 사용하는 여정이 처음 실행되면 대상자의 모든 프로필이 여정에 들어갑니다. 이 옵션을 사용하면 여정의 마지막 실행 이후 대상에 들어온 개인만 첫 번째 발생 이후에 타깃팅할 수 있습니다.

  >[!NOTE]
  >
  >여정에서 [사용자 지정 업로드 대상](../audience/about-audiences.md#segments-in-journey-optimizer)을(를) 대상으로 하는 경우, 이러한 대상이 수정되므로 반복 여정에서 이 옵션이 활성화된 경우 프로필은 첫 번째 반복에서만 검색됩니다.

* **반복 시 다시 시작 강제**: 이 옵션을 사용하면 여정에 여전히 있는 모든 프로필이 다음 실행 시 자동으로 종료되도록 할 수 있습니다. 이 여정에서 프로필의 수명이 반복 빈도보다 길 수 있는 경우(예: 대기 활동을 사용하는 경우) 프로필이 여정을 완료할 수 있도록 이 옵션을 활성화하지 마십시오.

![](assets/read-audience-options.png)

자세한 정보는 이 [섹션](../building-journeys/read-audience.md#configuring-segment-trigger-activity)을 참조하세요.

<!--
After 91 days, a Read audience journey switches to the **Finished** status. This behavior is set for 91 days only (i.e. journey timeout default value) as all information about profiles who entered the journey is removed 91 days after they entered. Persons still in the journey automatically are impacted. They exit the journey after the 30 day timeout. 
-->
