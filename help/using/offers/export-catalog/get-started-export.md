---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: 오퍼 카탈로그 내보내기 시작
description: 오퍼 카탈로그를 데이터 세트로 내보내는 방법 알아보기
badge: label="레거시" type="Informative"
feature: Decision Management, Datasets
topic: Integrations
role: User, Developer
level: Intermediate
exl-id: f30abea1-b204-4470-9836-75fae916bbb1
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/71W86v7R-wgsa7JDTE3d6Lddc71MOcTxrY5l0Ts600o
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
  - id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
feature_v2:
  - id: ed0d8d0e-04b9-4326-be72-a0fbca265377
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 133
ht-degree: 100%

---

# 오퍼 카탈로그 내보내기 시작 {#export-catalog}

>[!TIP]
>
>[!DNL Adobe Journey Optimizer]의 새로운 의사 결정 기능인 [결정]을 이제 코드 기반 경험 및 이메일 채널을 통해 사용할 수 있습니다. [자세히 알아보기](../../experience-decisioning/gs-experience-decisioning.md)

Journey Optimizer의 오퍼 카탈로그를 자동으로 Adobe Experience Platform으로 내보낼 수 있습니다.

내보내면 [오퍼 라이브러리]의 개체마다 데이터 세트가 하나씩 생깁니다([내보낸 데이터 세트에 액세스](../export-catalog/access-dataset.md) 참조). 이러한 서비스에는 다음이 포함됩니다.

* 개인화된 오퍼
* 대체 오퍼
* 배치
* 결정

[오퍼 라이브러리]에서 이 개체 중 하나를 수정할 때마다 새 내보내기 작업이 자동으로 실행되어 데이터 세트를 업데이트합니다.

>[!NOTE]
>
>이 기능은 기본적으로 활성화되어 있습니다. 추가 활성화 단계 없이 사용할 수 있습니다. 활성화하면 별도 조치 없이도 내보내기 작업이 자동화됩니다.

<!--
>[!NOTE]
>
>This feature is not enabled by default. If you want to use it, reach out to your Adobe contact to have it activated for your catalog. Once it is enabled, export jobs will be automated and will require no action from your side.
-->
