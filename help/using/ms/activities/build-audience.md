---
solution: Journey Optimizer
product: journey optimizer
title: 대상자 작성 활동 사용
description: 오케스트레이션된 캠페인에서 대상자 빌드 활동을 사용하는 방법을 알아봅니다
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 3959b5fa-0c47-42a5-828f-4d7ca9b7e72d
source-git-commit: 94de60c33c7cf1d8956294aebb91d7533534088f
workflow-type: tm+mt
source-wordcount: '369'
ht-degree: 52%

---

# 대상자 빌드 {#build-audience}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_build_audience"
>title="대상자 빌드 활동"
>abstract="**대상자 빌드** 활동을 통해 오케스트레이션된 캠페인에 참여할 대상자를 정의할 수 있습니다. 오케스트레이션된 캠페인 컨텍스트에서 메시지를 전송할 때 메시지 대상자는 채널 활동에서 정의되지 않고 **대상자 빌드** 활동에서 정의됩니다."

마케터는 사용자 친화적인 인터페이스를 사용하여 복잡한 쿼리를 쉽게 만들 수 있으므로 광범위한 기준과 동작을 기반으로 대상을 세그먼트화하여 캠페인을 보다 효과적으로 조정할 수 있습니다.

이렇게 하려면 **대상자 빌드** 타깃팅 활동을 사용하십시오. 이 활동을 통해 오케스트레이션된 캠페인을 입력할 대상자를 정의할 수 있습니다. 오케스트레이션된 캠페인 컨텍스트에서 메시지를 전송할 때 메시지 대상자는 채널 활동에서 정의되지 않고 **대상자 빌드** 활동에서 정의됩니다.

대상자 모집단을 정의하기 위해 수행할 수 있는 작업은 다음과 같습니다.

* 기존 대상자를 선택합니다.
* 미리 정의된 필터를 선택합니다.
* 필터링 기준을 정의하고 결합하여 쿼리 모델러로 새 대상을 작성합니다.

>[!NOTE]
>
>파일에서 로드한 대상은 대상 작성 활동을 사용하여 타깃팅할 수 없습니다. 이렇게 하려면 **파일 로드** 활동 다음에 **조정** 활동을 사용해야 합니다.


## 대상자 빌드 활동 구성 {#build-audience-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_build_audience_audienceselector"
>title="Audience"
>abstract="새 게재를 디자인할 때 대상자를 사용하는 것과 같은 방식으로 대상자를 선택합니다."

**대상자 빌드** 활동을 구성하려면 다음 단계를 따르십시오.

![](../assets/build-audience.png)

1. **대상자 빌드** 활동을 추가합니다.
1. 레이블을 정의합니다.
1. **직접 만들기** 또는 **대상자 읽기 만들기**&#x200B;로 대상자 유형을 정의합니다.
1. 아래 탭에 자세히 나와 있는 단계에 따라 대상자를 구성합니다.


자체 쿼리를 만들려면 다음 단계를 수행합니다.

1. **직접 만들기(쿼리)**&#x200B;를 선택합니다.
1. **차원 타겟팅**&#x200B;을 선택합니다. 타겟팅 차원을 사용하면 수신자, 약정 수혜자, 운영자, 구독자 등 작업에서 타겟팅하는 모집단을 정의할 수 있습니다. 기본적으로 대상은 수신자 중에서 선택됩니다.
1. **계속을 클릭합니다**.
1. 쿼리 모델러를 사용하여 쿼리를 정의합니다. [이 섹션에서 쿼리 모델러에 대해 자세히 알아보세요](../ms-query-modeler.md)

## 예시{#build-audience-examples}

다음은 두 개의 **대상자 작성** 활동으로 오케스트레이션된 캠페인의 예입니다. 첫 번째는 포커 플레이어 대상자를 대상으로 하며 이메일 게재로 이어집니다. 두 번째는 VIP 클라이언트 대상자를 대상으로 하며 SMS 게재로 이어집니다.

![](../assets/workflow-audience-example.png)
