---
solution: Journey Optimizer
product: journey optimizer
title: 조정 활동 사용
description: 오케스트레이션된 캠페인에서 조정 활동을 사용하는 방법을 알아봅니다
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 0d5cfffe-bc6c-40bc-b3e1-5b44368ac76f
source-git-commit: a19fe429d34a88c6159ab3b2b4dfa3768bcd24ad
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 32%

---

# 조정 {#reconciliation}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation"
>title="조정 활동"
>abstract="**조정** 활동은 Adobe Journey Optimizer와 작업 테이블의 데이터 간 링크를 정의할 수 있는 **타기팅** 활동입니다."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_field"
>title="조정 필드 선택"
>abstract="조정 필드 선택"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_condition"
>title="조정 생성 조건"
>abstract="조정 생성 조건"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_complement"
>title="조정 생성 여집합"
>abstract="조정 생성 여집합"


+++ 목차

| 오케스트레이션된 캠페인 시작 | 첫 오케스트레이션된 캠페인 시작 | 데이터베이스 쿼리 | 오케스트레이션된 캠페인 활동 |
|---|---|---|---|
| [오케스트레이션된 캠페인 시작](../gs-orchestrated-campaigns.md)<br/><br/>[구성 단계](../configuration-steps.md)<br/><br/>[오케스트레이션된 캠페인 액세스 및 관리](../access-manage-orchestrated-campaigns.md) | [오케스트레이션된 캠페인을 만드는 주요 단계](../gs-campaign-creation.md)<br/><br/>[캠페인 만들기 및 예약](../create-orchestrated-campaign.md)<br/><br/>[활동 오케스트레이션](../orchestrate-activities.md)<br/><br/>[캠페인 시작 및 모니터링](../start-monitor-campaigns.md)<br/><br/>[보고](../reporting-campaigns.md) | [규칙 빌더로 작업](../orchestrated-rule-builder.md)<br/><br/>[첫 번째 쿼리 빌드](../build-query.md)<br/><br/>[표현식 편집](../edit-expressions.md)<br/><br/>[재타겟팅](../retarget.md) | [활동 시작](about-activities.md)<br/><br/>활동:<br/>[및 가입](and-join.md) - [대상 작성](build-audience.md) - [차원 변경](change-dimension.md) - [채널 활동](channels.md) - [결합](combine.md) - [중복 제거](deduplication.md) - [데이터 보강](enrichment.md) - [포크](fork.md) - <b>[조정](reconciliation.md)</b> - [대상 저장](save-audience.md) - [분할](split.md) - [대기](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

**[!UICONTROL 조정]** 활동은 **[!UICONTROL 타깃팅]** 활동으로, Adobe Journey Optimizer의 데이터와 작업 테이블의 데이터(예: 외부 파일에서 로드된 데이터) 간의 링크를 정의할 수 있습니다.

**[!UICONTROL 데이터 보강]** 활동을 사용하면 오케스트레이션된 캠페인에 데이터를 추가할 수 있습니다. 예를 들어 여러 소스의 데이터를 결합하거나 임시 리소스에 연결할 수 있습니다. 반대로 **[!UICONTROL 조정]** 활동은 미확인 또는 외부 데이터와 데이터베이스의 기존 리소스를 일치시키는 데 사용됩니다.

**[!UICONTROL 조정]**&#x200B;을 사용하려면 관련 레코드가 시스템에 이미 있어야 합니다. 예를 들어 제품, 타임스탬프 및 고객 정보가 나열된 구매 파일을 가져오는 경우 링크를 설정하려면 제품과 고객 모두 데이터베이스에 이미 있어야 합니다.

## 조정 활동 구성 {#reconciliation-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_targeting"
>title="타기팅 차원"
>abstract="새로운 타기팅 차원을 선택합니다. 차원을 사용하여 대상 모집단(수신자, 앱 구독자, 운영자, 구독자 등)을 정의할 수 있습니다. 기본적으로 현재 타기팅 차원이 선택됩니다."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_rules"
>title="조정 규칙"
>abstract="중복 제거에 사용할 조정 규칙을 선택합니다. 속성을 사용하려면 **단순 속성** 옵션을 선택하고 소스 및 대상 필드를 선택합니다. 쿼리 모델러를 사용하여 자체 조정 조건을 만들려면 **고급 조정 조건** 옵션을 선택합니다."
>additional-url="https://experienceleague.adobe.com/ko/docs/campaign-web/v8/query-database/query-modeler-overview" text="쿼리 모델러로 작업"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_targeting_selection"
>title="타기팅 차원 선택"
>abstract="조정할 인바운드 데이터의 타기팅 차원을 선택합니다."
>additional-url="https://experienceleague.adobe.com/docs/campaign-web/v8/audiences/gs-audiences-recipients.html#targeting-dimensions" text="타기팅 차원"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_keep_unreconciled_data"
>title="조정되지 않은 데이터 유지"
>abstract="기본적으로 조정되지 않은 데이터는 아웃바운드 전환에 보관되며 나중에 작업 테이블에서 사용할 수 있습니다. 조정되지 않은 데이터를 제거하려면 **조정되지 않은 데이터 유지** 옵션을 비활성화합니다."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_attribute"
>title="조정 속성"
>abstract="데이터 조정에 사용할 속성을 선택하고 확인을 클릭합니다."

**[!UICONTROL 조정]** 활동을 구성하려면 다음 단계를 따르십시오.

1. 워크플로우에 **[!UICONTROL 조정]** 활동을 추가합니다.

1. 수신자나 구독자와 같이 타겟팅하는 사용자를 정의하려면 새 타겟팅 차원을 선택합니다.

1. 들어오는 데이터를 기존 프로필과 일치시키는 데 사용할 필드를 설정합니다.

1. 기본 필드를 사용하여 데이터를 일치시키려면 **[!UICONTROL 단순 특성]**&#x200B;을 선택하세요.

1. 일치하는 필드 설정:

   * **[!UICONTROL Source]**: 들어오는 데이터 필드를 나열합니다.

   * **[!UICONTROL 대상]**: 선택한 타겟팅 차원의 필드를 참조합니다.

   두 값이 같은 경우 일치(예: 프로필을 식별하기 위해 **[!UICONTROL 이메일]**&#x200B;로 일치)가 발생합니다.

   ![](../assets/workflow-reconciliation-criteria.png)

1. 일치하는 규칙을 더 추가하려면 **[!UICONTROL 규칙 추가]**&#x200B;를 클릭하세요. 일치가 발생하려면 모든 조건이 충족되어야 합니다.

1. 더 복잡한 조건을 보려면 **[!UICONTROL 고급 조정 조건]**&#x200B;을 선택하세요. [쿼리 모델러](../orchestrated-rule-builder.md)를 사용하여 사용자 지정 논리를 정의합니다.

1. 조정할 데이터를 필터링하려면 **[!UICONTROL 필터 만들기]**&#x200B;를 클릭하고 쿼리 모델러에서 조건을 정의합니다.

1. 기본적으로 일치하지 않는 레코드는 아웃바운드 전환에 유지되고 작업 테이블에 저장됩니다. 이를 제거하려면 **[!UICONTROL 조정되지 않은 데이터 유지]** 옵션을 사용하도록 설정하십시오.

## 예 {#example-reconciliation}

이 예제에서는 Adobe Journey Optimizer의 **[!UICONTROL 조정]** 활동을 사용하여 인식된 고객에게만 이메일을 보내도록 합니다. 데이터는 이전 주문이 있는 사용자를 타겟팅하는 **[!UICONTROL 대상자 읽기]** 활동을 통해 전송됩니다. 그런 다음 **[!UICONTROL 조정]** 활동은 전자 메일 필드를 사용하여 이 들어오는 데이터를 데이터베이스의 기존 프로필과 일치시킵니다.

![](../assets/workflow-reconciliation-sample-1.0.png)
