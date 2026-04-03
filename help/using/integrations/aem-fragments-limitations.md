---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Experience Manager 콘텐츠 조각 고려 사항 및 문제 해결
description: Journey Optimizer의 AEM 컨텐츠 조각에 대한 고려 사항 및 일반적인 문제입니다.
topic: Content Management
role: User
level: Beginner
source-git-commit: 4f7e36a6cc19e4138e867950e34c5a5e6452b364
workflow-type: tm+mt
source-wordcount: '733'
ht-degree: 0%

---

# 고려 사항 및 문제 해결 {#aem-fragments-limitations}

## 주요 고려 사항 {#considerations}

[!DNL Adobe Experience Manager]의 [!DNL Journey Optimizer]에서 콘텐츠 조각을 사용할 때는 다음 사항에 유의하십시오.

* **콘텐츠 조각 유형**
   * 단순 콘텐츠 조각, 중첩된 콘텐츠 조각 및 **콘텐츠 조각 변형**&#x200B;이 지원됩니다. [!DNL Journey Optimizer]에 조각을 삽입할 때 변형을 선택합니다. 변형을 선택하지 않으면 **Main** 변형([!DNL Adobe Experience Manager]에 있는 조각의 기본 콘텐츠)이 사용됩니다.

* **다국어 콘텐츠**
   * 각 변형은 작성, 태그 지정 및 [!DNL Adobe Experience Manager]에 게시되어야 합니다. [!DNL Journey Optimizer]에서 각 메시지 언어 또는 로케일과 일치하는 조각 변형을 선택합니다.
   * 변형 간에 자동 언어 확인 또는 대체 기능이 없습니다.

* **저장소 액세스**
   * [!DNL Journey Optimizer]은(는) [!DNL Adobe Experience Manager] **Publish** 계층만 통합됩니다(사이트, 콘텐츠 조각). 콘텐츠 조각은 인증되지 않은 공개 끝점을 통해 사용할 수 있습니다.
   * 작성자 저장소는 저장소 선택기에 표시될 수 있지만 **게시**&#x200B;에 게시된 조각만 [!DNL Journey Optimizer]에서 사용할 수 있습니다.

* **콘텐츠 조각 상태**
   * 조각은 **[!UICONTROL 게시됨]** 또는 **[!UICONTROL 수정됨]** 상태를 표시할 수 있습니다. [!DNL Journey Optimizer]은(는) 항상 **최신 게시 버전**&#x200B;을 사용합니다.
   * 게시 후 변경한 내용은 조각을 [!DNL Journey Optimizer]에 다시 게시할 때까지 [!DNL Adobe Experience Manager]에 반영되지 않습니다. 두 제품 간에는 자동 버전 조정이 없습니다.

* **개인화**
   * 지원됨: 프로필 속성, 컨텍스트 속성, 정적 문자열 및 사전 선언된 변수.
   * 지원되지 않음: 파생 또는 계산된 속성.

* **업데이트 및 버전 관리**
   * 업데이트는 [!DNL Adobe Experience Manager]에서 수동으로 다시 게시해야 합니다. 자동 버전 조정은 없습니다.
   * 콘텐츠 조각이 [!DNL Adobe Experience Manager]에 게시되거나 다시 게시되면 [!DNL Journey Optimizer]에서 해당 조각을 업데이트하고 활성 캠페인 또는 여정에서 **참조된 해당 조각의 모든 변형**&#x200B;을 새로 고칩니다.
   * [!DNL Adobe Experience Manager] [게시 작업](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/manage-publication)이(가) 지연될 수 있습니다. 완료되면 [!DNL Journey Optimizer]이(가) 이벤트를 받고 콘텐츠를 새로 고칩니다.
   * 업데이트가 성공하면 일반적으로 단일 여정의 경우 약 **5분** 내에, 일괄 사용 사례의 경우 **다음 배치**&#x200B;에서 변경 사항을 사용할 수 있습니다.

* **캐싱 및 증명**
   * 조각이 캠페인 또는 여정에 처음 추가되면 [!DNL Journey Optimizer]에서 이를 캐시합니다. **[!UICONTROL AEM CF 선택기 열기]**&#x200B;를 통해 다른 곳에서 이미 사용된 조각을 선택하면 [!DNL Journey Optimizer] 캐시에서 로드됩니다.
   * [!DNL Adobe Experience Manager]에서 수정된 조각을 다시 게시하면 [!DNL Journey Optimizer]이(가) 이벤트를 수신하고 캐시를 업데이트합니다.
   * 증명은 항상 **가장 최근에 게시된** 버전을 반영하며, 증명을 위해 기록 버전을 잠글 수 없습니다.

## 문제 해결 {#troubleshooting}

Journey Optimizer에서 Adobe Experience Manager 콘텐츠 조각을 사용하여 작업할 때 문제가 발생하는 경우 다음의 일반적인 문제 및 해결 방법을 참조하십시오.

| 문제 | 원인 | 해결 방법 |
|-|-|-|
| **태그를 찾을 수 없음** 또는 **콘텐츠 조각이 선택기에 표시되지 않음** | Adobe Experience Manager 태그 구문이 필수 형식 `ajo-enabled:{OrgId}/{SandboxName}`과(와) 일치하지 않습니다. | 태그 ID가 올바른 **조직 ID** 및 **샌드박스 이름**&#x200B;을 사용하는지 확인하십시오. 공백이나 잘못된 구분 기호가 없는지 확인합니다. 태그를 수정한 후 콘텐츠 조각을 다시 게시합니다. |
| **콘텐츠 조각이 목록에 표시되지 않음** | 콘텐츠 조각이 초안 상태이거나 게시되지 않음 | 승인되고 게시된 콘텐츠 조각만 Journey Optimizer 선택기에 표시됩니다. Adobe Experience Manager에서 콘텐츠 조각을 게시하고 게시된 상태인지 확인합니다. |
| **정의되지 않은 변수 오류** | Personalization 자리 표시자가 조각 도우미 태그에 선언되지 않음 | 조각 도우미 태그에 모든 필수 매개 변수를 추가합니다. 콘텐츠 조각에 사용된 각 자리 표시자는 해당 매핑으로 명시적으로 선언해야 합니다. |
| **증명이 예기치 않은 콘텐츠를 표시함** | 증명은 Adobe Experience Manager의 최신 게시 버전을 사용합니다. | 증명은 항상 Adobe Experience Manager에서 콘텐츠 조각의 가장 최근 게시를 반영합니다. Adobe Experience Manager에서 최근 변경 작업을 수행한 경우 조각을 다시 게시하고 증명을 새로 고칩니다. |
| **CPES(액세스 거부) 오류** | 사용자 역할이 특정 속성에 액세스할 수 있는 권한이 없음 | 시스템 관리자에게 문의하여 개인화에 사용된 프로필 또는 컨텍스트 속성에 대해 역할에 적절한 권한이 있는지 확인하십시오. |
| **조각이 비어 있거나 누락된 콘텐츠를 표시합니다** | 필수 개인화 매개 변수 또는 대체 값 누락 | 모든 필수 매개 변수가 제공되었는지 확인하고 선택적 속성에 대한 대체 값을 추가하는 것이 좋습니다. |
| **이미지가 렌더링되지 않거나 손상된 것 같습니다** | 콘텐츠 조각의 이미지 URL이 상대 경로이거나 채널에서 연결할 수 없습니다. | 이미지 필드에 **절대** URL(`https://...`)을 사용합니다. Adobe Experience Manager의 상대 경로는 지원되지 않습니다. 브라우저 또는 메시지 미리 보기에서 URL을 확인합니다. |
| **Experience League AEM 링크가 404를 반환함** | 부실 책갈피, 미리보기 빌드 또는 게시되지 않은 AEM 도움말 페이지 | 라이브 Experience Manager 설명서에서 [Adobe Journey Optimizer을 사용하여 콘텐츠 조각](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments-with-journey-optimizer){target="_blank"} 항목을 열고 페이지 내 목차에서 이동하거나 섹션 이름(예: **Dispatcher 구성**)을 검색합니다. |

문제가 지속되면 컨텐츠 조각 ID, 캠페인 또는 여정 ID에 대한 세부 정보와 표시되는 오류 메시지를 Adobe 담당자에게 문의하십시오.
