---
title: 시작하기
description: 오퍼 라이브러리 API를 사용하여 의사 결정 엔진을 사용해 주요 작업을 수행하는 방법을 알아봅니다.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 773bee50-849f-4b07-9423-67de5279ad28
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 96%

---

# 의사 결정 관리 API 개발자 안내서 {#decision-management-api-developer-guide}

>[!CONTEXTUALHELP]
>id="od_api_support"
>title="새로운 의사 결정 관리 API"
>abstract="이제 의사 결정 관리 개체를 생성하고 관리하기 위한 새로운 API를 사용할 수 있습니다. 레거시 API는 2024년 3월 27일까지 지원됩니다."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_api_support"
>title="새로운 의사 결정 관리 API"
>abstract="이제 의사 결정 관리 개체를 생성하고 관리하기 위한 새로운 API를 사용할 수 있습니다. 레거시 API는 2024년 3월 27일까지 지원됩니다."

이 개발자 안내서에서는 [!DNL Offer Library] API 사용을 시작하는 데 도움이 되는 단계를 제공합니다. 그런 다음 이 안내서에서는 의사 결정 엔진을 사용하여 주요 작업을 수행하기 위한 샘플 API 호출을 제공합니다.

➡️[이 비디오에서 의사 결정 관리의 구성 요소에 대해 자세히 알아보세요](#video)

## 전제 조건 {#prerequisites}

이 안내서를 사용하려면 Adobe Experience Platform의 다음 구성 요소에 대해 이해하고 있어야 합니다.

* [[!DNL Experience Data Model (XDM) System]](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko-KR){target="_blank"}: [!DNL Experience Platform]이 고객 경험 데이터를 구성하는 표준화된 프레임워크입니다.
   * [스키마 컴포지션 기본 사항](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=ko-KR){target="_blank"}: XDM 스키마의 기본 구성 요소에 대해 알아봅니다.
* [의사 결정 관리](../../../using/offers/get-started/starting-offer-decisioning.md): 일반적인 Decisioning, 특히 의사 결정 관리에 사용되는 개념과 구성 요소를 설명합니다. 고객 경험 중에 제공할 최상의 옵션을 선택하는 데 사용되는 전략을 보여 줍니다.
* [[!DNL Profile Query Language (PQL)]](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html?lang=ko){target="_blank"}: PQL은 XDM 인스턴스를 통해 표현식을 작성할 수 있는 강력한 언어입니다. PQL은 의사 결정 규칙을 정의하는 데 사용됩니다.

## 샘플 API 호출 읽기 {#reading-sample-api-calls}

이 안내서에서는 요청 형식을 지정하는 방법을 보여 주는 예제 API 호출을 제공합니다. 여기에는 경로, 필수 헤더 및 적절한 형식의 요청 페이로드가 포함됩니다. API 응답에서 반환되는 샘플 JSON도 제공됩니다. 샘플 API 호출에 대한 문서에 사용된 규칙에 대한 자세한 내용은 [!DNL Experience Platform] 문제 해결 안내서의 [예제 API 호출을 읽는 방법](https://experienceleague.adobe.com/docs/experience-platform/landing/troubleshooting.html?lang=ko#how-do-i-format-an-api-request){target="_blank"} 섹션을 참조하세요.

## 필수 헤더에 대한 값 수집 {#gather-values-for-required-headers}

[!DNL Adobe Experience Platform] API를 호출하려면 먼저 [인증 튜토리얼](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html?lang=ko){target="_blank"}을 완료해야 합니다. 인증 튜토리얼을 완료하면 아래와 같이 모든 [!DNL Experience Platform] API 호출의 필수 헤더 각각에 대한 값이 제공됩니다.

* `Authorization: Bearer {ACCESS_TOKEN}`
* `x-api-key: {API_KEY}`
* `x-gw-ims-org-id: {IMS_ORG}`
* `x-sandbox-name: {SANDBOX_NAME}`

페이로드(POST, PUT, PATCH)가 포함된 모든 요청에는 추가 헤더가 필요합니다.

* `Content-Type: application/json`

## 다음 단계 {#next-steps}

이 문서에서는 [!DNL Offer Library] API를 호출하는 데 필요한 사전 지식을 다뤘습니다. 이제 이 개발자 안내서에 제공된 샘플 호출로 진행하여 지침을 따를 수 있습니다.
<!--
>[!NOTE]
>
> The In-app messaging channel in Adobe Journey Optimizer uses decision management objects. If your organization uses the in-app messaging channel, then API list requests for objects will include objects created by the in-app messaging service and can be ignored for decision management use cases. Objects created for in-app messages will have `createdBy = "Mobile_Sheliak"`.
-->

<!-- ## How-to video {#video}

The following video is intended to support your understanding of the components of Decision Management.

>[!VIDEO](https://video.tv.adobe.com/v/329919?quality=12) -->

