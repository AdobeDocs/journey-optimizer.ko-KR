---
solution: Journey Optimizer
product: journey optimizer
title: 여정 단계 공유 개요
description: 여정 단계 공유 개요
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 07d25f8e-0065-4410-9895-ffa15d6447bb
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 5%

---

# 여정 보고서 만들기 {#design-jo-reports}

추가 [실시간 보고서](live-report.md) 및 내장 [글로벌 보고 기능](global-report.md), [!DNL Journey Optimizer] 은 여정 성능 데이터를 Adobe Experience Platform에 자동으로 전송할 수 있으므로 분석 목적으로 다른 데이터와 결합할 수 있습니다.

>[!NOTE]
>
>이 기능은 여정 단계 이벤트를 위한 모든 인스턴스에서 기본적으로 활성화됩니다. 단계 이벤트를 프로비전하는 동안 생성된 스키마 및 데이터 세트는 수정하거나 업데이트할 수 없습니다. 기본적으로 이러한 스키마와 데이터 세트는 읽기 전용 모드입니다.

예를 들어, 여러 개의 이메일을 보내는 여정을 설정했습니다. 이 기능을 사용하면 [!DNL Journey Optimizer] 전환 발생 횟수, 웹 사이트에서 발생한 참여 수 또는 저장소에서 발생한 트랜잭션 수와 같은 다운스트림 이벤트 데이터가 있는 데이터입니다. 여정 정보를 다른 디지털 속성에서 또는 오프라인 속성에서 Adobe Experience Platform의 데이터와 결합하여 보다 포괄적인 성능 보기를 제공할 수 있습니다.

[!DNL Journey Optimizer] 은(는) 개별 여정에서 수행하는 각 단계에 대해 필요한 스키마와 스트림을 Adobe Experience Platform에 자동으로 만듭니다. 단계 이벤트는 여정에서 한 노드에서 다른 노드로 이동하는 개별 이벤트에 해당합니다. 예를 들어 이벤트, 조건 및 작업이 있는 여정에서 3단계 이벤트가 Adobe Experience Platform으로 전송됩니다.

전달되는 XDM 필드 목록은 포괄적입니다. 일부는 시스템 생성 코드를 포함하고 나머지는 읽을 수 있는 친숙한 이름을 가지고 있습니다. 예를 들면 여정 활동의 레이블이나 단계 상태가 있습니다. 오류가 발생하여 작업 시간이 초과되거나 종료된 횟수입니다.

>[!CAUTION]
>
>실시간 프로필 서비스에 대해 데이터 세트를 설정할 수 없습니다. 다음 사항을 확인하십시오 **[!UICONTROL 프로필]** 토글이 꺼져 있습니다.

[!DNL Journey Optimizer] 스트리밍 방식으로 데이터가 발생하는 대로 데이터를 전송합니다. 쿼리 서비스를 사용하여 이 데이터를 쿼리할 수 있습니다. Customer Journey Analytics 또는 기타 BI 도구에 연결하여 이러한 단계와 관련된 데이터를 볼 수 있습니다.

다음 스키마가 만들어집니다.

* 에 대한 여정 단계 이벤트 스키마 [!DNL Journey Orchestration] - 여정 메타데이터에 연결된 여정 단계 이벤트입니다.
* 여정 필드가 있는 여정 스키마 [!DNL Journey Orchestration] - 여정을 설명하는 여정 메타데이터.

![](assets/sharing1.png)

![](assets/sharing2.png)

다음 데이터 세트가 전달됩니다.

* 여정 단계 이벤트
* 여정

![](assets/sharing3.png)

Adobe Experience Platform에 전달된 XDM 필드 목록은 다음 항목에 자세히 설명되어 있습니다.

* [단계 이벤트 필드 목록](../reports/sharing-field-list.md)
* [레거시 단계 이벤트 필드](../reports/sharing-legacy-fields.md)

## Customer Journey Analytics과 통합 {#integration-cja}

[!DNL Journey Optimizer] 단계 이벤트는 의 다른 데이터 세트에 연결할 수 있습니다 [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=ko){target=&quot;_blank&quot;}.

일반 워크플로우는 다음과 같습니다.

* [!DNL Customer Journey Analytics] 는 &quot;여정 단계 이벤트&quot; 데이터 세트를 설정합니다.
* 다음 **profileID** 연결된 &quot;Journey Orchestration에 대한 여정 단계 이벤트 스키마&quot;의 필드는 ID 필드로 정의됩니다. in [!DNL Customer Journey Analytics]그런 다음 이 데이터 세트를 개인 기반 식별자와 동일한 값을 갖는 다른 데이터 세트에 연결할 수 있습니다.
* 에서 이 데이터 세트를 사용하려면 [!DNL Customer Journey Analytics]- 크로스 채널 여정 분석의 경우 [Customer Journey Analytics 설명서](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-usecases/cross-channel.html){target=&quot;_blank&quot;}.

