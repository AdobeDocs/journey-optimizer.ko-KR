---
solution: Journey Optimizer
product: journey optimizer
title: AEM 컨텐츠 조각
description: AEM 콘텐츠 조각 액세스 및 관리 방법 알아보기
topic: Content Management
role: User
level: Beginner
exl-id: c36a53a4-c324-4082-838e-ed27bd3b2e90
TQID: https://experienceleague.adobe.com/GRQ3Wz7Y4YJ3545mTtju0R8en9BYiejyo8UoMx558nM
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
subfeature_v2:
  - id: c7dc31c0-c4f7-42a7-8cf5-a8c5aeb0de74
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 6dbdae6edd95d97e039565ed5c6e3cab9f4a19d8
workflow-type: tm+mt
source-wordcount: 296
ht-degree: 16%

---

# Adobe Experience Manager 콘텐츠 조각 시작 {#aem-fragments}

>[!BEGINSHADEBOX]

**이 페이지에서:** Adobe Experience Manager 콘텐츠 조각을 시작하고 작성자 및 게시 주기에 따라 Journey Optimizer에서 사용할 수 있는 조각이 결정되는 방법을 이해합니다.

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>의료 고객의 경우 Journey Optimizer Healthcare Shield 및 Adobe Experience Manager Enhanced Security 추가 기능 서비스의 라이선스가 있을 때만 통합이 활성화됩니다.

이제 Adobe Experience Manager as a Cloud Service를 Adobe Journey Optimizer와 통합하여 AEM 콘텐츠 조각을 Journey Optimizer 콘텐츠에 원활하게 통합할 수 있습니다. 이렇게 간소화된 연결을 통해 AEM 콘텐츠에 액세스하고 활용하는 프로세스가 간단해져 개인화되고 동적인 캠페인 및 여정을 만들 수 있게 됩니다.

AEM 콘텐츠 조각에 대한 자세한 내용은 Experience Manager 설명서에서 [콘텐츠 조각을 사용하여 작업](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments-with-journey-optimizer){target="_blank"}을 참조하세요.

## 콘텐츠 조각 라이프사이클

![](assets/do-not-localize/AEM_CF.png)

콘텐츠 조각은 존재하는 Adobe Experience Manager 계층에 따라 다른 라이프사이클 단계를 따릅니다. [Adobe Experience Manager 설명서에서 자세히 알아보기](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/author-publish)

콘텐츠는 **작성자 계층**&#x200B;에서 만들어지고 관리되며, 조각에는 새로 만들기, 초안, 게시됨, 수정됨 또는 게시 취소됨 등의 상태가 있을 수 있습니다. 이러한 상태는 **작성자 계층**&#x200B;에만 적용되며 콘텐츠 만들기 및 검토를 지원합니다.

콘텐츠 조각이 게시되면 복사본이 **게시 계층**&#x200B;에 만들어지고 인증되지 않은 공개 끝점을 통해 노출됩니다. Journey Optimizer은 이 **게시 계층**&#x200B;과(와) 독점적으로 통합됩니다.

따라서 Journey Optimizer은 게시된 콘텐츠 조각 또는 수정된 콘텐츠 조각만 표시하고 항상 게시된 최신 버전을 사용합니다. 게시 후 수행된 모든 변경 사항은 컨텐츠 조각이 다시 게시될 때까지 Journey Optimizer에 반영되지 않습니다.
