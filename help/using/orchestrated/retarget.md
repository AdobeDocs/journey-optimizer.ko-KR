---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Journey Optimizer을 사용하여 오케스트레이션된 캠페인 시작 및 모니터링
description: Adobe Journey Optimizer을 사용하여 오케스트레이션된 캠페인을 시작 및 모니터링하는 방법을 알아봅니다.
hide: true
hidefromtoc: true
exl-id: 3c1cad30-3ed7-4df1-a46a-60394a834e79
source-git-commit: 25120dd71159d0233783ac4c189f528ff2c93ae3
workflow-type: tm+mt
source-wordcount: '766'
ht-degree: 1%

---

# 리타겟팅 쿼리 빌드 {#retarget}

+++ 목차

| 오케스트레이션된 캠페인 시작 | 첫 오케스트레이션된 캠페인 시작 | 데이터베이스 쿼리 | 오케스트레이션된 캠페인 활동 |
|---|---|---|---|
| [오케스트레이션된 캠페인 시작](gs-orchestrated-campaigns.md)<br/><br/>관계형 스키마 및 데이터 세트 만들기 및 관리:</br> <ul><li>[수동 스키마](manual-schema.md)</li><li>[파일 업로드 스키마](file-upload-schema.md)</li><li>[데이터 수집](ingest-data.md)</li></ul>[오케스트레이션된 캠페인 액세스 및 관리](access-manage-orchestrated-campaigns.md)<br/><br/>[오케스트레이션된 캠페인을 만드는 주요 단계](gs-campaign-creation.md) | [캠페인 만들기 및 예약](create-orchestrated-campaign.md)<br/><br/>[활동 오케스트레이션](orchestrate-activities.md)<br/><br/>[캠페인 시작 및 모니터링](start-monitor-campaigns.md)<br/><br/>[보고](reporting-campaigns.md) | [규칙 빌더로 작업](orchestrated-rule-builder.md)<br/><br/>[첫 번째 쿼리 빌드](build-query.md)<br/><br/>[표현식 편집](edit-expressions.md)<br/><br/><b>[재타겟팅](retarget.md)</b> | [활동 시작](activities/about-activities.md)<br/><br/>활동:<br/>[및 가입](activities/and-join.md) - [대상 작성](activities/build-audience.md) - [차원 변경](activities/change-dimension.md) - [채널 활동](activities/channels.md) - [결합](activities/combine.md) - [중복 제거](activities/deduplication.md) - [데이터 보강](activities/enrichment.md) - [포크](activities/fork.md) - [조정](activities/reconciliation.md) - [대상 저장](activities/save-audience.md) - [분할](activities/split.md) - [대기](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

이 페이지의 컨텐츠는 최종본이 아니며, 변경될 수 있습니다.

>[!ENDSHADEBOX]

리타겟팅을 사용하면 이전에 오케스트레이션된 캠페인에 응답한 방식을 기반으로 수신자를 후속 처리할 수 있습니다. 예를 들어 수신했지만 첫 번째 이메일을 클릭하지 않은 수신자에게 두 번째 이메일을 보낼 수 있습니다.

**[!UICONTROL 오케스트레이션된 Campaign]**&#x200B;은(는) 다음 두 가지 기본 특성을 제공합니다.

* **[!UICONTROL 메시지 피드백]**: 게재 관련 이벤트(예: 보낸 메시지, 연 메시지, 반송된 메시지 등)를 캡처합니다.
* **[!UICONTROL 전자 메일 추적]**: 사용자 작업(예: 클릭 및 열기)을 캡처합니다.

![](assets/do-not-localize/retarget-schema.png){zoomable="yes"}


## 피드백 기반 리타겟팅 규칙 만들기 {#feedback-retarget}

피드백 기반 리타겟팅 규칙을 사용하면 **[!UICONTROL 메시지 피드백]** 특성에 캡처된 메시지 게재 이벤트에 따라 수신자를 리타겟팅할 수 있습니다. 이러한 이벤트에는 전송, 열기, 반송 또는 스팸으로 표시된 메시지와 같은 결과가 포함됩니다.

이 데이터를 사용하여 특정 게재 상태에 따라 후속 커뮤니케이션을 가능하게 하는 이전 메시지를 받은 수신자를 식별하는 규칙을 정의할 수 있습니다.

1. 새 **[!UICONTROL 오케스트레이션된 캠페인 만들기]**.

1. **[!UICONTROL 대상자 빌드]** 활동을 추가하고 타겟팅 차원을 **[!UICONTROL 수신자(caas)]**(으)로 설정합니다.

1. **[!UICONTROL 규칙 빌더]**&#x200B;에서 **[!UICONTROL 조건 추가]**&#x200B;를 클릭하고 **[!UICONTROL 특성 선택기]**&#x200B;에서 **[!UICONTROL 메시지 피드백]**&#x200B;을 선택합니다. **[!UICONTROL 확인]**&#x200B;을 클릭하여 **조건과 같은**&#x200B;메시지 피드백을 만듭니다.

   ![](assets/retarget_1.png){zoomable="yes"}

1. 메시지 게재 이벤트를 대상으로 **[!UICONTROL 피드백 상태]** 특성을 선택하십시오.

+++ 세부 단계별

   1. **[!UICONTROL 메시지 피드백]** 특성에 연결된 다른 조건을 추가합니다.

   1. **[!UICONTROL 피드백 상태]** 특성을 검색하고 **[!UICONTROL 확인]**&#x200B;을 클릭합니다.

      ![](assets/retarget_3.png){zoomable="yes"}

   1. **[!UICONTROL 사용자 지정 조건]** 메뉴에서 **[!UICONTROL 값]** 드롭다운에서 추적할 게재 상태를 선택합니다.

      ![](assets/retarget_4.png){zoomable="yes"}

+++

1. 오케스트레이션된 특정 캠페인을 대상으로 지정하려면 **[!UICONTROL 오케스트레이션된 캠페인 이름]** 특성을 선택하십시오.

+++ 세부 단계별

   1. **[!UICONTROL 메시지 피드백]** 특성에 연결된 다른 조건을 추가하고 **[!UICONTROL 엔터티]**&#x200B;을(를) 검색한 후 다음으로 이동:

      `_experience > CustomerJourneyManagement > Entities > AJO Orchestrated Campaign entity`.

   1. **[!UICONTROL 오케스트레이션된 캠페인 이름]**&#x200B;을 선택하세요.

      ![](assets/retarget_5.png){zoomable="yes"}

   1. **[!UICONTROL 사용자 지정 조건]** 메뉴에서 **[!UICONTROL 값]** 필드에 캠페인 이름을 지정하십시오.

+++

1. 오케스트레이션된 캠페인 내의 특정 메시지 또는 활동을 타깃팅하려면 **[!UICONTROL 오케스트레이션된 캠페인 작업 이름]** 특성을 선택하십시오.

+++ 세부 단계별

   1. **[!UICONTROL 메시지 피드백]** 특성에 연결된 다른 조건을 추가하고 **[!UICONTROL 엔터티]**&#x200B;을(를) 검색한 후 다음으로 이동:

      `_experience > CustomerJourneyManagement > Entities > AJO Orchestrated Campaign entity`.

   1. **[!UICONTROL 오케스트레이션된 캠페인 작업 이름]**&#x200B;을 선택하십시오.

      ![](assets/retarget_6.png){zoomable="yes"}

   1. **[!UICONTROL 사용자 지정 조건]** 메뉴에서 **[!UICONTROL 값]** 필드에 캠페인 동작 이름을 지정하십시오.

      활동의 레이블 필드 옆에 있는 ![정보 아이콘](assets/do-not-localize/info-icon.svg)을 클릭하여 작업 이름을 찾을 수 있습니다.

+++

1. 또는 Campaign 속성에서 찾을 수 있는 **[!UICONTROL Campaign ID]**(UUID)별로 필터링할 수도 있습니다.

이제 피드백 기반 리타겟팅 규칙을 구성하여 전송, 열기, 반송 또는 스팸으로 표시된 것과 같은 이전 메시지의 게재 상태를 기반으로 수신자를 식별합니다. 이 대상자를 정의하면 [추적 기반 리타겟팅 규칙을 구성](#tracking-based)하여 사용자 상호 작용 데이터를 사용하여 후속 이메일을 추가하거나 타겟팅을 세분화할 수 있습니다.

![](assets/retarget_9.png){zoomable="yes"}


## 추적 기반 리타겟팅 규칙 만들기 {#tracking-based}

추적 기반 리타겟팅 규칙은 **[!UICONTROL 전자 메일 추적]** 특성의 데이터를 사용하여 메시지와의 상호 작용에 따라 수신자를 타깃팅합니다. 이메일 열기 및 링크 클릭과 같은 사용자 작업을 캡처합니다.

메시지 상호 작용(예: 열기 또는 클릭)에 따라 수신자를 다시 타겟팅하려면 다음과 같이 **[!UICONTROL 전자 메일 추적]** 엔터티를 사용합니다.

1. 새 **[!UICONTROL 오케스트레이션된 캠페인 만들기]**.

1. **[!UICONTROL 대상자 빌드]** 활동을 추가하고 타겟팅 차원을 **[!UICONTROL 수신자(caas)]**(으)로 설정하여 오케스트레이션된 이전 캠페인 수신자에 집중하십시오.

1. **[!UICONTROL 규칙 빌더]**&#x200B;에서 **[!UICONTROL 조건 추가]**&#x200B;를 클릭하고 **[!UICONTROL 특성 선택기]**&#x200B;에서 **[!UICONTROL 전자 메일 추적]**&#x200B;을(를) 선택합니다.

   **[!UICONTROL 확인]**&#x200B;을 클릭하여 **조건과 같은**&#x200B;전자 메일 추적을 만듭니다.

   ![](assets/retarget_2.png){zoomable="yes"}

1. 수신자의 메시지 상호 작용을 타겟팅하려면 **[!UICONTROL 전자 메일 추적]** 특성에 연결된 다른 조건을 추가하고 **[!UICONTROL 상호 작용 유형]** 특성을 검색하십시오.

   ![](assets/retarget_7.png){zoomable="yes"}

1. 사용자 지정 조건 옵션에서 연산자로 **[!UICONTROL 포함]**&#x200B;을 사용하고 사용 사례에 따라 하나 이상의 값을 선택합니다(예: **[!UICONTROL 열린 메시지]** 또는 **[!UICONTROL 클릭한 메시지 링크]**).

   ![](assets/retarget_8.png){zoomable="yes"}

이제 **[!UICONTROL 전자 메일 추적]** 특성의 데이터를 사용하여 전자 메일 열기 또는 링크 클릭과 같은 이전 메시지와의 상호 작용을 기반으로 수신자를 타깃팅하는 추적 기반 재타깃팅 규칙을 구성했습니다. 이 대상자를 정의하면 [피드백 기반 리타겟팅 규칙](#feedback-retarget)과(와) 결합하여 전송, 반송 또는 스팸으로 표시된 메시지 결과를 포함하도록 후속 작업을 추가하거나 타겟팅을 세분화할 수 있습니다.


![](assets/retarget_10.png){zoomable="yes"}
