---
solution: Journey Optimizer
product: journey optimizer
title: 조정 활동 사용
description: 오케스트레이션된 캠페인에서 조정 활동을 사용하는 방법을 알아봅니다
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 0d5cfffe-bc6c-40bc-b3e1-5b44368ac76f
source-git-commit: a6b293a5eb1358f692d53c9611b794cf8f7fc753
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 44%

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

**조정** 활동은 **타깃팅** 활동으로, Adobe Journey Optimizer의 데이터와 작업 테이블의 데이터(예: 외부 파일에서 로드된 데이터) 간의 링크를 정의할 수 있습니다.

## 모범 사례 {#reconciliation-best-practices}

**데이터 보강** 활동을 통해 오케스트레이션된 캠페인에서 처리할 추가 데이터를 정의할 수 있지만(**데이터 보강** 활동을 사용하여 여러 세트에서 가져온 데이터를 결합하거나 임시 리소스에 대한 링크를 만들 수 있음), **조정** 활동을 통해 미식별 데이터를 기존 리소스에 연결할 수 있습니다.

>[!NOTE]
>조정 작업은 연결된 차원의 데이터가 이미 데이터베이스에 있음을 의미합니다.  예를 들어 어떤 제품을, 어떤 시간에, 어떤 고객이 구매했는지 등을 표시하는 구매 파일을 가져올 경우, 데이터베이스에는 이미 고객과 제품이 존재할 것입니다.

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
>additional-url="https://experienceleague.adobe.com/docs/campaign-web/v8/audiences/gs-audiences-recipients.html?lang=ko&#targeting-dimensions" text="타기팅 차원"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_keep_unreconciled_data"
>title="조정되지 않은 데이터 유지"
>abstract="기본적으로 조정되지 않은 데이터는 아웃바운드 전환에 보관되며 나중에 작업 테이블에서 사용할 수 있습니다. 조정되지 않은 데이터를 제거하려면 **조정되지 않은 데이터 유지** 옵션을 비활성화합니다."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_attribute"
>title="조정 속성"
>abstract="데이터 조정에 사용할 속성을 선택하고 확인을 클릭합니다."

**조정** 활동을 구성하려면 다음 단계를 따르십시오.

1. 오케스트레이션된 캠페인에 **조정** 활동을 추가합니다.

1. 새로운 타기팅 차원을 선택합니다. 차원을 사용하면 타겟팅된 모집단(수신자, 앱 구독자, 연산자, 구독자 등)을 정의할 수 있습니다.

1. 조정에 사용할 필드를 선택합니다. 조정 기준을 하나 이상 사용할 수 있습니다.

   1. 특성을 사용하여 데이터를 조정하려면 **단순 특성** 옵션을 선택하십시오. **Source** 필드에는 조정할 입력 전환에서 사용할 수 있는 필드가 나열됩니다. **대상** 필드는 선택한 타겟팅 차원의 필드에 해당합니다. 소스와 대상이 같을 때 데이터가 조정됩니다. 예를 들어 **이메일** 필드를 선택하여 이메일 주소를 기반으로 프로필을 중복 제거합니다.

      다른 조정 기준을 추가하려면 **규칙 추가** 단추를 클릭하십시오. 여러 조인 조건이 지정된 경우 데이터를 함께 연결할 수 있도록 모두 를 확인해야 합니다.

      ![](../assets/workflow-reconciliation-criteria.png)

   1. 다른 특성을 사용하여 데이터를 조정하려면 **고급 조정 조건** 옵션을 선택하십시오. 그런 다음 쿼리 모델러를 사용하여 자신의 조정 조건을 만들 수 있습니다.

1. **필터 만들기** 단추를 사용하여 조정할 데이터를 필터링할 수 있습니다. 이렇게 하면 쿼리 모델러를 사용하여 사용자 지정 조건을 만들 수 있습니다.

기본적으로, 조정되지 않은 데이터는 아웃바운드 전환에 유지되고 나중에 사용할 수 있도록 작업 테이블에서 사용할 수 있습니다. 조정되지 않은 데이터를 제거하려면 **조정되지 않은 데이터 유지** 옵션을 비활성화합니다.
