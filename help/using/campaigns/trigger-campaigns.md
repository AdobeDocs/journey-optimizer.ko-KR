---
solution: Journey Optimizer
product: journey optimizer
title: 캠페인 검토 및 활성화
description: Journey Optimizer에서 캠페인을 검토하고 활성화하는 방법에 대해 알아봅니다
feature: Campaigns
topic: Content Management
role: User
level: Intermediate
keywords: 캠페인, 검토, 유효성 검사, 활성화, 활성화, 최적화
source-git-commit: 1bdba8c5c1a9238d351b159551f6d3924935b339
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 3%

---


# API에서 트리거된 캠페인 실행 {#execute}

캠페인이 활성화되면 생성된 샘플 cURL 요청을 검색하고 API에 사용하여 페이로드를 빌드하고 캠페인을 트리거해야 합니다.

1. 캠페인을 연 다음 **[!UICONTROL cURL 요청]** 섹션에서 페이로드 요청을 복사하여 붙여 넣으십시오. 이 페이로드에는 메시지에 사용된 모든 개인화(프로필 및 컨텍스트) 변수가 포함됩니다. 캠페인이 라이브되면 사용할 수 있습니다.

   ![](assets/api-triggered-curl.png)

1. 이 cURL 요청을 API에 사용하여 페이로드를 빌드하고 캠페인을 트리거합니다. 자세한 내용은 [대화형 메시지 실행 API 설명서](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution)를 참조하세요.


   API 호출 예는 [이 페이지](https://developer.adobe.com/journey-optimizer-apis/references/messaging-samples/)에서도 사용할 수 있습니다.

   >[!NOTE]
   >
   >캠페인을 생성할 때 특정 시작 날짜 및/또는 종료 날짜를 구성했다면 이 날짜 이후에 실행되지 않고 API 호출이 실패합니다.
