---
solution: Journey Optimizer
product: journey optimizer
title: 다단계 캠페인 설정 구성
description: Adobe Journey Optimizer을 사용하여 여러 단계의 캠페인 설정을 구성하는 방법에 대해 알아봅니다.
hide: true
hidefromtoc: true
exl-id: a9bb3782-a4d1-43fe-ae2a-aef3f17ba588
source-git-commit: 323472ef9d6203cbbadc44ceb17ddcc7f6207323
workflow-type: tm+mt
source-wordcount: '1082'
ht-degree: 27%

---

# 다단계 캠페인 설정 구성 {#workflow-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_creation_properties"
>title="다단계 캠페인 속성"
>abstract="이 화면에서 다단계 캠페인을 만들고 레이블을 지정하는 데 사용할 템플릿을 선택합니다. **추가 옵션** 섹션을 확장하여 다단계 캠페인 내부 이름, 해당 폴더, 시간대, 감독자 그룹 등의 추가적인 설정을 구성합니다. 오류가 발생하는 경우 운영자에게 경고할 수 있도록 감독자 그룹을 선택할 것이 권장됩니다."

캔버스에서 여러 단계 캠페인을 만들거나 여러 단계 캠페인 활동을 오케스트레이션할 때 여러 단계 캠페인과 관련된 고급 설정에 액세스할 수 있습니다. 예를 들어, 다중 단계 캠페인에 대한 특정 시간대를 설정하거나, 오류 발생 시 다중 단계 캠페인이 작동하는 방식을 관리하거나, 다중 단계 캠페인 내역을 삭제해야 하는 지연 시간을 관리할 수 있습니다.

이러한 설정은 다중 단계 캠페인을 만들 때 선택한 템플릿에 사전 구성되어 있지만, 필요에 따라 이 특정 다중 단계 캠페인에 대해 편집할 수 있습니다.

![](assets/workflow-settings-button.png){zoomable="yes"}{width="70%" align="left"}

## 다단계 캠페인 속성 {#properties}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_properties"
>title="다단계 캠페인 속성"
>abstract="이 섹션에서는 다단계 캠페인을 만들 때에도 액세스할 수 있는 일반 다단계 캠페인 속성을 제공합니다. 다단계 캠페인을 만들고 레이블을 지정하는 데 사용할 템플릿을 선택할 수 있습니다. 폴더 또는 시간대를 저장하는 다단계 캠페인과 같은 특정 설정을 구성하려면 추가 옵션 섹션을 확장합니다."

**[!UICONTROL 속성]** 섹션은 여러 단계 캠페인을 만들 때 구성할 수 있는 일반 설정을 제공합니다. 기존 여러 단계 캠페인의 속성에 액세스하려면 여러 단계 캠페인 캔버스 위의 작업 표시줄에서 사용할 수 있는 **[!UICONTROL 설정]** 단추를 클릭하십시오.


![](assets/workflow-settings.png){zoomable="yes"}{width="70%" align="left"}


이러한 속성은 다음과 같습니다.

* 목록에 표시되는 다중 단계 캠페인의 **[!UICONTROL 레이블]**.
* 여러 단계 캠페인의 **[!UICONTROL 내부 이름]**.
* 여러 단계 캠페인을 저장할 **[!UICONTROL 폴더]**&#x200B;입니다.
* 모든 여러 단계 캠페인의 활동에서 사용할 기본 **[!UICONTROL 표준 시간대]**입니다. 기본적으로 여러 단계 캠페인의 시간대는 현재 캠페인 연산자에 대해 정의된 시간대입니다.
가능한 값:
   * Adobe Experience Platform 조직의 시간대를 사용할 **서버 시간대**
   * **여러 단계 캠페인을 실행하는 연산자의 시간대를 사용하는 연산자 시간대**
   * 데이터베이스 서버의 시간대를 사용하려면 **데이터베이스의 시간대**
   * 특정 시간대
* 여러 단계 캠페인이 실패하면 **[!UICONTROL 감독자]** 필드에서 선택한 연산자 그룹에 속하는 연산자에게 전자 메일로 알림이 전송됩니다.
* 여러 단계 캠페인의 **[!UICONTROL 설명]**&#x200B;을 입력할 수도 있습니다.

## 세분화 설정  {#segmentation-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_segmentation"
>title="세분화 설정"
>abstract="이 섹션에서는 다단계 캠페인에서 프로필을 타기팅할 타기팅 차원을 선택하고 두 실행 간에 워크플로 결과를 유지하도록 선택할 수 있습니다. 이 옵션은 테스트 목적으로만 사용해야 하며 프로덕션 다단계 캠페인에서 활성화해서는 안 됩니다."

* **[!UICONTROL 타겟팅 차원]**: 프로필 타겟팅에 사용할 타겟팅 차원(수신자, 계약 수혜자, 운영자, 구독자 등)을 선택하십시오.

* **[!UICONTROL 두 실행 사이의 중간 모집단 결과를 유지합니다]**: 기본적으로 여러 단계 캠페인의 마지막 실행에 대한 작업 테이블만 유지됩니다. 이전 실행의 작업 테이블은 매일 실행되는 기술 다단계 캠페인에 의해 삭제됩니다.

  이 옵션을 활성화하면 여러 단계 캠페인이 실행된 후에도 작업 테이블이 유지됩니다. 테스트 목적으로 사용할 수 있으므로 개발 또는 스테이징 환경에서 **전용**&#x200B;을 사용해야 합니다. 프로덕션 다중 단계 캠페인에서는 체크해서는 안 됩니다.

## 실행 설정  {#exec-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_execution"
>title="실행 설정"
>abstract="이 섹션에서는 다단계 캠페인 기록이 유지되는 일 수와 같이 워크플로 실행과 관련된 설정을 구성할 수 있습니다."

* **[!UICONTROL 일 단위 기록]**: 기록을 제거해야 하는 일 수를 지정합니다. 내역에는 여러 단계 캠페인과 관련된 요소인 로그, 작업, 이벤트(여러 단계 캠페인 작업에 연결된 기술 개체)가 포함되어 있습니다. 기본 설정 여러 단계 캠페인 템플릿의 경우 기본값은 30일입니다. 기록 제거는 기본적으로 매일 실행되는 데이터베이스 정리 기술 여러 단계 캠페인에 의해 수행됩니다

  >[!IMPORTANT]
  >
  >**[!UICONTROL 일별 기록]** 필드를 비워두면 해당 값이 “1”로 간주되어 1일 후에 기록이 제거됩니다.

* **[!UICONTROL 기본 선호도]**: 설치에 여러 단계 캠페인 서버가 포함된 경우 이 필드를 사용하여 여러 단계 캠페인이 실행될 서버를 지정하십시오. 이렇게 하면 특정 서버에서 해당 여러 단계 캠페인을 강제로 실행할 수 있습니다. 기존 선호도 이름을 선택할 수 있지만 공백이나 구두점을 사용하지 않아야 합니다. 다른 서버를 사용하는 경우 쉼표로 구분하여 다른 이름을 지정합니다.

  >[!IMPORTANT]
  >
  >이 필드에 정의된 값이 서버에 없는 경우 여러 단계 캠페인이 보류 상태로 유지됩니다.


* **[!UICONTROL 로그에 SQL 쿼리 저장]**: workflmulti-step campaignow의 SQL 쿼리를 로그에 저장하려면 이 옵션을 선택하십시오. 이 기능은 고급 사용자용으로 예약되어 있습니다. **[!UICONTROL 대상자 작성]**&#x200B;과 같은 타깃팅 활동이 포함된 여러 단계 캠페인에 적용됩니다. 이 옵션을 활성화하면 여러 단계 캠페인 실행 중에 데이터베이스로 전송된 SQL 쿼리가 여러 단계 캠페인의 로그에 표시되므로 이를 분석하여 쿼리를 최적화하거나 문제를 진단할 수 있습니다.

## 오류 관리 설정  {#error-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_error"
>title="오류 관리 설정"
>abstract="이 섹션에서는 다단계 캠페인을 통해 실행 중 오류를 관리하는 방법을 정의할 수 있습니다. 프로세스를 일시 중지하거나, 특정 수의 오류를 무시하거나, 다단계 캠페인 실행을 중지하도록 선택할 수 있습니다."

* **[!UICONTROL 오류 관리]**: 이 필드를 사용하면 여러 단계 캠페인 작업에 오류가 있는 경우 수행할 작업을 정의할 수 있습니다. 다음과 같은 세 가지 옵션이 있습니다.

   * **[!UICONTROL 프로세스 일시 중단]**: 여러 단계 캠페인이 자동으로 일시 중지되고 상태가 **[!UICONTROL 실패]**(으)로 변경됩니다. 문제가 해결되면 **[!UICONTROL 다시 시작]** 단추를 사용하여 여러 단계 캠페인을 다시 시작합니다.
   * **[!UICONTROL 무시]**: 오류를 트리거한 작업의 상태가 **[!UICONTROL 실패]**(으)로 변경되지만 여러 단계 캠페인은 **[!UICONTROL 시작됨]** 상태를 유지합니다. <!-- TO ADD ONCE SCHEUDLER IS AVAILABLE This configuration is relevant for recurring tasks: if the branch includes a scheduler, it will start normally next time the workflow is executed.-->
   * **[!UICONTROL 프로세스 중단]**: 다중 단계 캠페인이 자동으로 중지되고 상태가 **[!UICONTROL 실패]**(으)로 변경됩니다. 문제가 해결되면 **[!UICONTROL 시작]** 단추를 사용하여 여러 단계 캠페인을 다시 시작하십시오.

* **[!UICONTROL 연속 오류]**: **[!UICONTROL 오류의 경우]** 필드에서 **[!UICONTROL 무시]** 값을 선택하면 이 필드를 사용할 수 있습니다. 프로세스가 중지되기 전에 무시할 수 있는 오류 수를 지정할 수 있습니다. 이 수에 도달하면 여러 단계의 캠페인 상태가 **[!UICONTROL 실패]**(으)로 변경됩니다. 이 필드의 값이 0이면 오류 수에 관계없이 여러 단계 캠페인을 중지하지 않습니다.

## 초기화 스크립트 {#initialization-script}

**초기화 스크립트**&#x200B;를 사용하여 변수를 초기화하거나 활동 속성을 수정할 수 있습니다. **코드 편집** 단추를 클릭하고 실행할 코드 조각을 입력하십시오. 여러 단계 캠페인이 실행되면 스크립트가 호출됩니다. [이벤트 변수](event-variables.md)와 관련된 섹션을 참조하세요.
