---
solution: Journey Optimizer
product: journey optimizer
title: 기본 제공 역할
description: 기본 제공 권한에 대해 알아보기
feature: Access Management
topic: Administration
role: Admin, User
level: Intermediate
keywords: 권한, 작성, 메시지
exl-id: fd7a7564-bf67-4796-8182-0b9b04516f21
source-git-commit: 417eea2a52d4fb38ae96cf74f90658f87694be5a
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 6%

---

# 기본 권한 {#ootb-permissions}

| 기능 | 권한 |
|-|-|
| 캠페인 | **[!DNL Manage campaigns]**: 캠페인 읽기, 만들기, 편집 및 삭제 </br>**[!DNL Publish campaigns]**: 캠페인을 게시할 권한.</br>**[!DNL View campaigns]**: 캠페인에 대한 읽기 전용 액세스 권한. </br>**[!DNL View campaigns report]**: 캠페인 보고서를 읽고 편집합니다. |
| 대시보드 | **[!DNL View license usage dashboards]**: 라이선스 사용 대시보드에 대한 읽기 전용 액세스 권한입니다. </br>**[!DNL Manage custom dashboards]**: 새 대시보드를 만들거나 기존 대시보드를 편집할 수 있습니다.</br>**[!DNL View custom dashboards]**: 사용자 정의 대시보드에 대한 읽기 전용 액세스 권한. </br>**[!DNL View standard dashboards]**: 프로필, 대상 및 세그먼트 대시보드에 대한 읽기 전용 액세스 권한.</br>**[!DNL Manage standard dashboards]**: 위젯 라이브러리를 통해 사용자 정의 위젯을 만들고 위젯 스키마를 편집할 수 있습니다. |
| 데이터 수집 | **[!DNL Manage datastream]**: 데이터스트림 읽기, 생성 및 편집&#x200B;</br>**[!DNL View datastream]**: 데이터스트림에 대한 읽기 전용 액세스. |
| 데이터 거버넌스 | **[!DNL Manage usage labels]**: 레이블 읽기, 만들기, 편집 및 삭제&#x200B;</br>**[!DNL Manage data usage policies]**: 데이터 사용 정책을 읽고, 만들고, 편집하고, 삭제합니다.</br>**[!DNL View data usage policies]**: 조직에 속한 데이터 사용 정책에 대한 읽기 전용 액세스 권한.</br>**[!DNL View user activity log]**: Platform 활동의 기록된 감사 로그를 보기 위한 읽기 전용 액세스입니다. |
| 데이터 위생 | **[!DNL View data hygiene]**: 데이터 위생을 위한 읽기 전용 액세스입니다.</br>**[!DNL Manage data hygiene]**: 데이터 위생 읽기, 만들기, 편집 및 삭제 |
| 데이터 수집 | **[!DNL Manage sources]**: 소스를 읽고, 만들고, 편집하고, 비활성화합니다.</br>**[!DNL View sources]**: 카탈로그 탭의 사용 가능한 소스와 찾아보기 탭의 인증된 소스에 대한 읽기 전용 액세스 권한. |
| 데이터 관리 | **[!DNL Manage datasets]**: 데이터 세트 읽기, 만들기, 편집 및 삭제 스키마에 대한 읽기 전용 액세스 권한.</br>**[!DNL View datasets]**: 데이터 세트 및 스키마에 대한 읽기 전용 액세스 권한.</br>**[!DNL Data monitoring]**: 모니터링 데이터 세트 및 스트림에 대한 읽기 전용 액세스. |
| 데이터 모델링 | **[!DNL Manage schemas]**: XDM(경험 데이터 모델) 스키마를 읽고 만들고 편집합니다.</br>**[!DNL View schemas]**: 스키마에 대한 읽기 전용 액세스 권한.</br>**[!DNL Manage relationships]**: 스키마 관계를 읽기, 만들기, 편집 및 삭제합니다.</br>**[!DNL Manage identity metadata]**: 스키마에 대한 id 메타데이터를 읽고, 만들고, 편집하고, 삭제합니다. |
| 의사 결정 관리 | **[!DNL Manage decisions]**: 의사 결정 엔티티를 읽고, 만들고, 편집하고, 삭제합니다.</br>**[!DNL View decisions]**: 오퍼 엔티티에 대한 읽기 전용 액세스 권한.</br>**[!DNL Manage offers]**: 모든 오퍼, 구성 요소, 의사 결정 및 컬렉션을 읽고, 만들고, 편집하고, 삭제합니다.</br>**[!DNL Manage ranking strategies]**: 사용자 지정 보고서를 읽고, 만들고, 편집하고, 삭제하고, 작업 기능을 사용합니다.</br> |
| 대상 | **[!DNL Manage destinations]**: 대상 활성화 플로우 및 대상 계정을 읽고 만들고 삭제합니다.</br>**[!DNL View destinations]**: 카탈로그 탭의 사용 가능한 대상 및 찾아보기 탭의 인증된 대상에 대한 읽기 전용 액세스 권한.</br>**[!DNL Activate destinations]**: 사용자에게 기존 대상에 대한 세그먼트를 활성화할 수 있는 기능을 제공합니다.</br>**[!DNL Activate segment without mapping]**: 사용자에게 매핑 단계를 표시하지 않고 기존 대상에 대한 세그먼트를 활성화할 수 있는 기능을 제공합니다. 사용자는 활성화 워크플로에서 세그먼트를 추가 및 제거할 수 있지만, 매핑된 속성 또는 ID를 추가하거나 제거할 수는 없습니다.</br>**[!DNL Manage and activate dataset destination]**: 데이터 세트 내보내기 흐름을 읽고, 만들고, 편집하고, 비활성화합니다. 생성된 활성 데이터 세트에 대한 데이터도 활성화할 수 있습니다.</br>**[!DNL Destination authoring]**: Adobe Experience Platform Destination SDK을 사용하는 작성자 대상. |
| ID 관리 | **[!DNL Manage identity namespaces]**: id 네임스페이스를 읽고, 만들고, 편집합니다.</br>**[!DNL View identity namespaces]**: id 네임스페이스에 대한 읽기 전용 액세스 권한.</br>**[!DNL Manage identity settings]**: id 설정을 읽고, 만들고, 편집합니다.</br>**[!DNL View identity settings]**: id 설정에 대한 읽기 전용 액세스 권한.</br>**[!DNL View identity graph]**: id 그래프에 대한 읽기 전용 액세스 권한. |
| Journey Optimizer 라이브러리 | **[!DNL Manage Library Items]**: 저장된 표현식을 추가하고 삭제합니다. [!DNL Journey Optimizer] 라이브러리.</br>**[!DNL Simulate content]**: 미리 보기 및 증명을 위한 콘텐츠 시뮬레이션 옵션에 액세스 |
| Journey Optimizer 규칙 | **[!DNL View frequency rules]**: 규칙에 대한 읽기 전용 액세스 권한&#x200B;</br>**[!DNL Manage frequency rules]**: 메시지 빈도 규칙에 액세스, 만들기, 편집 또는 삭제 |
| 여정 | **[!DNL Manage journeys]**: 여정 읽기, 만들기, 편집 및 삭제&#x200B;</br>**[!DNL View journeys]**: 여정에 대한 읽기 전용 액세스 권한</br>**[!DNL Publish journeys]**: 여정 게시.</br>**[!DNL Manage journeys events, data sources and actions]**: 이벤트, 소스 또는 작업을 읽고, 만들고, 편집하고, 삭제합니다.</br>**[!DNL View journeys events, data sources and actions]**: 여정 이벤트, 사용자 지정 작업 여정 및 여정 데이터 소스에 대한 읽기 전용 액세스 권한.</br>**[!DNL View journeys report]**: 여정 보고서를 읽고 편집합니다.</br> |
| 프로필 관리 | **[!DNL Manage profiles]**: 고객 프로필에 사용되는 데이터 세트를 읽기, 만들기, 편집 및 삭제합니다. 사용 가능한 프로필에 대한 읽기 전용 액세스 권한.</br>**[!DNL View profiles]**: 사용 가능한 프로필에 대한 읽기 전용 액세스 권한.</br>**[!DNL Export audience segments]**: 평가된 대상 세그먼트를 데이터 세트로 내보냅니다.</br>**[!DNL View segments]**: 사용 가능한 세그먼트에 대한 읽기 전용 액세스 권한.</br>**[!DNL Evaluate a segment to an audience]**: 세그먼트 정의를 평가하여 대상에 대한 프로필을 생성합니다.</br>**[!DNL Manage merge policies]**: 병합 정책을 읽기, 만들기, 편집 및 삭제합니다.</br>**[!DNL View merge policies]**: 사용 가능한 병합 정책에 대한 읽기 전용 액세스 권한. |
| 쿼리 서비스 | **[!DNL Manage queries]**: Platform 데이터에 대한 구조화된 SQL 쿼리를 읽고, 만들고, 편집하고, 삭제합니다.</br>**[!DNL Manage query service integration]**: 쿼리 서비스 액세스에 대한 만료되지 않는 자격 증명을 만들고, 업데이트하고, 삭제합니다. |
| 샌드박스 관리 | **[!DNL Manage sandboxes]**: 샌드박스 읽기, 만들기, 편집 및 삭제&#x200B;</br>**[!DNL View sandboxes]**: 조직에 속한 샌드박스에 대한 읽기 전용 액세스 권한.</br>**[!DNL Reset sandboxes]**: 샌드박스를 재설정하는 기능.</br>**[!DNL Export sandboxes]**: 샌드박스를 내보내는 기능. |

{style="table-layout:fixed"}