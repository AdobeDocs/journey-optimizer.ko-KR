---
solution: Journey Optimizer
product: journey optimizer
title: AEM 컨텐츠 조각
description: AEM 콘텐츠 조각 액세스 및 관리 방법 알아보기
topic: Content Management
role: User
level: Beginner
source-git-commit: b06229e7a2fc64fbe28154c798b152cca8203a86
workflow-type: tm+mt
source-wordcount: '866'
ht-degree: 6%

---

# Adobe Experience Manager 콘텐츠 조각 시작 {#aem-fragments}

이제 Adobe Experience Manager as a Cloud Service를 Adobe Journey Optimizer와 통합하여 AEM 콘텐츠 조각을 Journey Optimizer 콘텐츠에 원활하게 통합할 수 있습니다. 이렇게 간소화된 연결을 통해 AEM 콘텐츠에 액세스하고 활용하는 프로세스가 간단해져 개인화되고 동적인 캠페인 및 여정을 만들 수 있게 됩니다.

AEM 콘텐츠 조각에 대한 자세한 내용은 Experience Manager 설명서에서 [콘텐츠 조각을 사용하여 작업](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments-with-journey-optimizer){target="_blank"}을 참조하세요.

## 시작하기 전 {#start}

>[!AVAILABILITY]
>
>의료 고객의 경우 Journey Optimizer Healthcare Shield 및 Adobe Experience Manager Enhanced Security 추가 기능 서비스의 라이선스가 있을 때만 통합이 활성화됩니다.

### 제한 사항 {#limitations}

Journey Optimizer에서 Adobe Experience Manager 콘텐츠 조각을 사용하여 작업할 때 다음 제한 사항을 참고하십시오.

* **콘텐츠 조각 유형**: 간단한 콘텐츠 조각 및 중첩된 콘텐츠 조각이 지원됩니다. 콘텐츠 조각 변형은 현재 지원되지 않습니다.

* **다국어 콘텐츠**: 수동 흐름만 지원됩니다. 각 언어 변형은 Adobe Experience Manager에서 독립적으로 작성, 태그 지정, 게시 및 Journey Optimizer에서 수동으로 선택해야 합니다. 자동 언어 확인 또는 대체 메커니즘이 없습니다.

* **저장소 액세스**: Journey Optimizer은 인증되지 않은 공개 끝점을 통해 콘텐츠 조각을 사용할 수 있는 Adobe Experience Manager 게시 계층과 배타적으로 통합됩니다. 작성자 저장소는 저장소 선택기에 표시될 수 있지만, 게시 계층에 게시된 콘텐츠 조각만 Journey Optimizer에서 사용할 수 있습니다.

* **콘텐츠 조각 상태**: Journey Optimizer은 **게시됨** 및 **수정됨** 상태의 콘텐츠 조각을 표시합니다. 모든 경우에 게시된 최신 버전만 사용됩니다. 게시 후 조각이 수정되면 해당 변경 사항은 콘텐츠 조각이 Journey Optimizer에서 다시 게시될 때까지 Adobe Experience Manager에 반영되지 않습니다. Adobe Experience Manager과 Journey Optimizer 간에는 자동 버전 조정이 없습니다.

* **Personalization**: 프로필 특성, 컨텍스트 특성, 정적 문자열 및 사전 선언된 변수만 지원됩니다. 파생 또는 계산된 속성은 지원되지 않습니다.

* **업데이트 및 버전 관리**: 콘텐츠 조각 업데이트는 Adobe Experience Manager에서 수동으로 다시 게시해야 합니다. Adobe Experience Manager과 Journey Optimizer 간에는 자동 버전 조정이 없습니다. 컨텐츠 조각이 Adobe Experience Manager에 게시되면 Journey Optimizer은 이벤트를 수신하고 Journey Optimizer 측에서 업데이트합니다. 성공하면 단일 여정의 경우 5분 후, 배치 사용 사례의 경우 다음 배치에서 업데이트를 사용할 수 있습니다.

* **캐싱 및 증명**: 콘텐츠 조각은 Adobe Experience Manager 게시 계층에서 실시간으로 검색됩니다. 사전 렌더링 또는 스냅샷 캐싱이 없습니다. 캠페인 및 여정에 대한 증명은 항상 가장 최근에 게시된 콘텐츠 조각 버전을 반영하며 기록 버전은 증명을 위해 잠글 수 없습니다.

* **사용자 액세스**: 실수로 인한 오류 위험을 줄이기 위해 콘텐츠 조각을 게시할 수 있는 액세스 권한을 가진 사용자 수를 제한하는 것이 좋습니다.


### 콘텐츠 조각 라이프사이클

![](assets/do-not-localize/AEM_CF.png)

콘텐츠 조각은 존재하는 Adobe Experience Manager 계층에 따라 다른 라이프사이클 단계를 따릅니다. [Adobe Experience Manager 설명서에서 자세히 알아보기](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/sites/authoring/author-publish)

콘텐츠는 **작성자 계층**&#x200B;에서 만들어지고 관리되며, 조각에는 새로 만들기, 초안, 게시됨, 수정됨 또는 게시 취소됨 등의 상태가 있을 수 있습니다. 이러한 상태는 **작성자 계층**&#x200B;에만 적용되며 콘텐츠 만들기 및 검토를 지원합니다.

콘텐츠 조각이 게시되면 복사본이 **게시 계층**&#x200B;에 만들어지고 인증되지 않은 공개 끝점을 통해 노출됩니다. Journey Optimizer은 이 **게시 계층**&#x200B;과(와) 독점적으로 통합됩니다.

따라서 Journey Optimizer은 게시된 콘텐츠 조각 또는 수정된 콘텐츠 조각만 표시하고 항상 게시된 최신 버전을 사용합니다. 게시 후 수행된 모든 변경 사항은 컨텐츠 조각이 다시 게시될 때까지 Journey Optimizer에 반영되지 않습니다.


## 문제 해결 {#troubleshooting}

Journey Optimizer에서 Adobe Experience Manager 콘텐츠 조각을 사용하여 작업할 때 문제가 발생하는 경우 다음의 일반적인 문제 및 해결 방법을 참조하십시오.

| 문제 | 원인 | 해결 방법 |
|-|-|-|
| **태그를 찾을 수 없음** 또는 **콘텐츠 조각이 선택기에 표시되지 않음** | Adobe Experience Manager 태그 구문이 필수 형식 `ajo-enabled:{OrgId}/{SandboxName}`과(와) 일치하지 않습니다. | 태그 ID가 올바른 **조직 ID** 및 **샌드박스 이름**&#x200B;을 사용하는지 확인하십시오. 공백이나 잘못된 구분 기호가 없는지 확인합니다. 태그를 수정한 후 콘텐츠 조각을 다시 게시합니다. |
| **콘텐츠 조각이 목록에 표시되지 않음** | 콘텐츠 조각이 초안 상태이거나 승인되지 않음 | 승인되고 게시된 콘텐츠 조각만 Journey Optimizer 선택기에 표시됩니다. Adobe Experience Manager에서 콘텐츠 조각을 게시하고 이 조각이 승인됨 상태인지 확인합니다. |
| **정의되지 않은 변수 오류** | Personalization 자리 표시자가 조각 도우미 태그에 선언되지 않음 | 조각 도우미 태그에 모든 필수 매개 변수를 추가합니다. 콘텐츠 조각에 사용된 각 자리 표시자는 해당 매핑으로 명시적으로 선언해야 합니다. |
| **증명이 예기치 않은 콘텐츠를 표시함** | 증명은 Adobe Experience Manager의 최신 게시 버전을 사용합니다. | 증명은 항상 Adobe Experience Manager에서 콘텐츠 조각의 가장 최근 게시를 반영합니다. Adobe Experience Manager에서 최근 변경 작업을 수행한 경우 조각을 다시 게시하고 증명을 새로 고칩니다. |
| **CPES(액세스 거부) 오류** | 사용자 역할이 특정 속성에 액세스할 수 있는 권한이 없음 | 시스템 관리자에게 문의하여 개인화에 사용된 프로필 또는 컨텍스트 속성에 대해 역할에 적절한 권한이 있는지 확인하십시오. |
| **조각이 비어 있거나 누락된 콘텐츠를 표시합니다** | 필수 개인화 매개 변수 또는 대체 값 누락 | 모든 필수 매개 변수가 제공되었는지 확인하고 선택적 속성에 대한 대체 값을 추가하는 것이 좋습니다. |

문제가 지속되면 컨텐츠 조각 ID, 캠페인 또는 여정 ID에 대한 세부 정보와 표시되는 오류 메시지를 Adobe 담당자에게 문의하십시오.
