---
solution: Journey Optimizer
product: journey optimizer
title: 여정 게시
description: 여정에 대해 보고하는 방법 알아보기
feature: Journeys, Monitoring
topic: Content Management
role: User
level: Intermediate
keywords: 게시, 여정, 라이브, 유효성, 확인
exl-id: 186b061d-0941-48be-8917-bbdfff6dae90
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/pclOxVDnQikU-2nLYMJ8mqEog9QL4WZBC7-NbvhuzIg
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d556b755-390a-43f0-be32-a08cf6236126id: d998adac-2f81-400b-a669-d07bb196e4ebid: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2: id: fa683eda-48de-4558-af32-2673edcd44feid: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 566
ht-degree: 1%

---

# 여정 캔버스의 라이브 보고서 {#report-journey}

여정이 게시된 후 [시험 실행 모드](journey-dry-run.md)가 활성화되면 **실시간 보고**&#x200B;에서는 지난 24시간 동안의 지표를 여정 캔버스 내에서 직접 제공합니다.


>[!AVAILABILITY]
>
>여정 실시간 보고서에서 데이터를 볼 수 없는 경우 **[!UICONTROL 여정 보고서 보기]** 권한을 포함하도록 액세스 권한을 확장해야 합니다. [자세히 알아보기](../administration/permissions.md)


표시된 이벤트는 지난 24시간 내에 발생했으며, 이벤트와 해당 표시 간 최소 간격은 2분이며, 일반적으로 5분 이내입니다.

실시간 성능 지표를 표시하는 ![여정 실시간 보고서 대시보드](assets/journey_live_report.png)

라이브 또는 [시험 실행 모드](journey-dry-run.md)의 여정에 대해 다음을 확인할 수 있습니다.

* **[!UICONTROL 입력한 프로필]**: 여정에 입력한 총 개인 수.
* **[!UICONTROL 종료된 프로필]**: 여정을 종료한 총 개인 수(오류 포함).
* **[!UICONTROL 오류가 있는 프로필]**: 여정 중에 오류가 발생한 개인의 총 수입니다.
* **[!UICONTROL 삭제된 프로필]**: 다음 이유 중 하나로 여정에서 삭제된 총 개인 수:

   * **대상 자격** 활동의 경우 대상 자격에 대한 예상 동사가 여정이 받은 내용과 일치하지 않으면(예: &quot;실현됨&quot; 대신 &quot;종료됨&quot;) 취소가 발생할 수 있습니다.
   * **event-triggered** 여정의 경우, 개인이 너무 빨리 여정을 다시 입력하려고 시도하거나 다시 입력이 허용되지 않는 경우 취소가 발생할 수 있습니다.
   * **반복** 여정에서 개인이 이미 여정에 있고 재입력 정책이 &quot;강제 재입력&quot;으로 설정되어 있지 않은 경우 각 반복에서 취소가 계산됩니다.
   * **대상자 읽기** 활동에서 내보낸 개인에 대해 ID가 설정되지 않았거나 수신된 ID 네임스페이스가 여정의 예상 ID와 일치하지 않으면 무시됩니다.

Live 또는 [시험 실행 모드](journey-dry-run.md)의 모든 여정 내의 각 활동에 대해 다음에 액세스할 수 있습니다.

* **[!UICONTROL 입력됨]**: 이 활동에 입력한 총 개인 수입니다. **Action** 활동의 경우, 시험 실행 모드에서 실행되지 않으므로 이 지표는 프로필이 통과함을 나타냅니다.
* **[!UICONTROL 종료됨(종료 기준을 충족함)]**: 종료 기준(오류 포함)으로 인해 해당 활동에서 여정을 종료한 총 개인 수.
* **[!UICONTROL 종료됨(강제 종료)]**: 여정 실무자 구성으로 인해 일시 중지된 동안 여정을 종료한 총 개인 수 이 지표는 시험 실행 모드의 여정에 대해 항상 0입니다.
* **[!UICONTROL 오류]**: 해당 활동에 오류가 있는 개인의 총 수입니다.

## 누락된 보고 데이터 문제 해결 {#troubleshooting-missing-data}

여정 보고서에 예상 데이터가 표시되지 않으면 다음 사항을 고려하십시오.

* **여정 이름 동기화**: [!DNL Adobe Journey Optimizer]의 여정 이름이 보고 데이터 집합에 저장된 이름과 일치하는지 확인하십시오. 이 이름이 일치하지 않으면 보고 데이터가 올바르게 표시되지 않을 수 있습니다.

* **데이터 새로 고침 시간**: 여정 이름 또는 구성을 업데이트한 후 데이터를 새로 고칠 수 있는 충분한 시간을 허용하십시오. 보고 데이터는 일반적으로 몇 분 이내에 표시되지만, 경우에 따라 더 오래 걸릴 수 있습니다.

* **액세스 권한**: 여정 보고서를 보는 데 필요한 권한이 있는지 확인하십시오. 데이터가 표시되지 않으면 관리자에게 **[!UICONTROL 여정 보고서 보기]** 권한이 활성화되었는지 확인하십시오. [권한에 대해 자세히 알아보기](../administration/permissions.md)

* **여정 상태**: 보고 데이터는 게시된 여정 또는 [시험 실행 모드](journey-dry-run.md)에서 실행 중인 여정에 대해서만 사용할 수 있습니다. 초안 여정은 보고 데이터를 생성하지 않습니다.

이러한 항목을 확인한 후에도 문제가 지속되면 Adobe 관리자 또는 [Adobe 지원](../start/user-interface.md#support-ticket-guidelines)에 지원을 요청하세요.

>[!MORELIKETHIS]
>
>* [보고 시작하기](../reports/gs-reports.md)
>* [여정 게시](publish-journey.md)
>* [여정 시험 실행](journey-dry-run.md)
>* [여정 지표 구성 및 추적](success-metrics.md)
>* [사용자 지정 여정 보고서](../reports/sharing-overview.md)
