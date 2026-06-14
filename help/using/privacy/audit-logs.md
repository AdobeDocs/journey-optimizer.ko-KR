---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 리소스에 대한 작업 감사
description: Journey Optimizer 리소스에서 수행된 작업을 추적하는 방법을 알아봅니다.
feature: Monitoring
role: User
level: Intermediate
exl-id: 759b014a-c834-4331-bffd-5bc159ec555d
TQID: https://experienceleague.adobe.com/Usk3qin9P4IZlKw-gEI4zaKO-aRtaKq9-0GMVlOecjA
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: aeebb91a-f216-4d5f-8da1-3a7e6f696ed0
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
subfeature_v2:
  - id: a9cf78bf-e9e4-4836-85a5-b6b3cf93bf56
  - id: f365ec33-2b99-4b7f-b4ee-c743dd7f615f
  - id: c8d5f2ce-ba44-43e9-a2bf-94a3d7d85ec3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 4e89993a998268ae2810c949d0669bf6dc458dd6
workflow-type: tm+mt
source-wordcount: 380
ht-degree: 90%

---

# Journey Optimizer 리소스에 대한 작업 감사 {#track-changes}

>[!BEGINSHADEBOX]

**이 페이지에서:** 가시성을 높이고 문제를 해결하며 규정 및 데이터 관리 정책을 준수하는지 확인할 수 있도록 Journey Optimizer 리소스에 대한 사용자 작업을 기록하는 감사 로그를 검토하십시오.

>[!ENDSHADEBOX]

## 감사 로그 정보 {#audit-logs}

>[!IMPORTANT]
>
>감사 로그를 보고 내보내려면 **[!DNL View User Activity Log]** 권한이 있어야 합니다. [자세히 알아보기](../administration/ootb-product-profiles.md)

Journey Optimizer를 사용하면 시스템에서 여정, 메시지, 랜딩 페이지 등과 같은 다양한 서비스 및 기능에서 사용자가 수행한 작업을 식별할 수 있습니다.

이를 통해 시스템에서 수행되는 작업의 가시성을 높이고, 문제를 해결하며, 규정 및 기업 데이터 관리 정책을 준수할 수 있습니다.

각 작업은 Adobe Experience Platform에서 액세스할 수 있는 &quot;감사 로그&quot;에 메타데이터로 기록됩니다. UI 또는 API에서 감사 로그를 보고 관리하는 방법 등 감사 로그에 대한 자세한 내용은 [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview.html?lang=ko)를 참조하세요.

![](assets/audit-logs.png)

## 감사 로그로 캡처된 이벤트 유형 {#events}

다음 테이블에서는 감사 로그에서 Journey Optimizer 리소스를 기록하는 작업을 간략하게 설명합니다. 감사 로그에 캡처된 전체 작업 목록은 [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview.html?lang=ko#category)를 참조하십시오.

>[!NOTE]
>
>**의사 결정 관리**&#x200B;와 관련된 감사 로그는 **[!UICONTROL 로그 다운로드]** 버튼을 사용하여 다운로드할 수 있는 CSV 파일에서만 볼 수 있습니다.

| 리소스 | 작업 |
|-----------|------------------|
| AJO 캠페인 | 만들기 / 삭제 / 업데이트 / 활성화 / 중지 |
| AJO 채널 일반 설정 | 만들기 / 삭제 / 업데이트 |
| AJO IP 풀 | 만들기 / 삭제 / 업데이트 |
| AJO 랜딩 페이지 | 만들기 / 삭제 / 업데이트 / 게시 / 게시 취소 |
| AJO 랜딩 페이지 HTML 템플릿 | 만들기 / 삭제 / 업데이트 |
| AJO 랜딩 페이지 사전 설정 | 만들기 / 삭제 / 업데이트 |
| AJO 랜딩 페이지 하위 도메인 | 만들기 / 삭제 / 업데이트 |
| AJO 메시지 사전 설정 | 만들기 / 삭제 / 업데이트 |
| AJO PTR 레코드 | 만들기 / 삭제 / 업데이트 |
| AJO 저장된 표현식 템플릿 | 만들기 / 삭제 / 업데이트 |
| AJO SMS API 자격 증명 | 만들기 / 삭제 / 업데이트 |
| AJO 하위 도메인 | 만들기 / 삭제 / 업데이트 |
| AJO 금지 목록 | CSV 만들기 / 삭제 / 다운로드 |
| 필드 그룹 | 만들기 / 삭제 / 업데이트 |
| 여정 | 만들기 / 삭제 / 업데이트 / 중지 / 게시 |
| 여정 사용자 지정 작업 | 만들기 / 삭제 / 업데이트 |
| 여정 데이터 소스 | 만들기 / 삭제 / 업데이트 |
| 여정 이벤트 | 만들기 / 삭제 / 업데이트 |
| 여정 조각 | 만들기 / 삭제 / 업데이트 / 활성화 / 아카이브 |
| 메시지 빈도 규칙 | 만들기 / 삭제 / 업데이트 |
| 등급 전략 | 만들기 / 삭제 / 업데이트 |
