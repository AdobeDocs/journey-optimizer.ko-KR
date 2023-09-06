---
title: 시작하기
description: Offer Library API를 사용하여 의사 결정 엔진을 사용하여 주요 작업을 수행하는 방법을 알아봅니다.
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 773bee50-849f-4b07-9423-67de5279ad28
source-git-commit: 4f2bbef98b2e529c2f6a663a3cf7e1ad5493c41a
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 7%

---

# 의사 결정 관리 API 개발자 안내서 {#decision-management-api-developer-guide}

이 개발자 안내서에서는 다음을 사용하는 데 도움이 되는 단계를 제공합니다. [!DNL Offer Library] API. 그런 다음 이 안내서에서는 의사 결정 엔진을 사용하여 주요 작업을 수행하기 위한 샘플 API 호출을 제공합니다.

➡️ [이 비디오에서 의사 결정 관리의 구성 요소에 대해 자세히 알아보십시오.](#video)

## 전제 조건 {#prerequisites}

이 안내서를 사용하려면 Adobe Experience Platform의 다음 구성 요소에 대해 이해하고 있어야 합니다.

* [[!DNL Experience Data Model (XDM) System]](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko-KR){target="_blank"}: 표준화된 프레임워크 [!DNL Experience Platform] 고객 경험 데이터를 구성합니다.
   * [스키마 컴포지션 기본 사항](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=ko-KR){target="_blank"}: XDM 스키마의 기본 구성 요소에 대해 알아봅니다.
* [의사 결정 관리](../../../using/offers/get-started/starting-offer-decisioning.md): Experience Decisioning에 사용되는 개념과 구성 요소에 대해 설명합니다. 고객 경험 중에 제공할 최상의 옵션을 선택하는 데 사용되는 전략을 보여 줍니다.
* [[!DNL Profile Query Language (PQL)]](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html){target="_blank"}: PQL은 XDM 인스턴스를 통해 표현식을 작성할 수 있는 강력한 언어입니다. PQL은 의사 결정 규칙을 정의하는 데 사용됩니다.

## 샘플 API 호출 읽기 {#reading-sample-api-calls}

이 안내서에서는 요청 형식을 지정하는 방법을 보여 주는 예제 API 호출을 제공합니다. 여기에는 경로, 필수 헤더 및 적절한 포맷의 요청 페이로드가 포함됩니다. API 응답에서 반환되는 샘플 JSON도 제공됩니다. 샘플 API 호출에 대한 설명서에 사용되는 규칙에 대한 자세한 내용은 의 섹션을 참조하십시오. [예제 API 호출을 읽는 방법](https://experienceleague.adobe.com/docs/experience-platform/landing/troubleshooting.html#how-do-i-format-an-api-request){target="_blank"} 다음에서 [!DNL Experience Platform] 문제 해결 가이드.

## 필수 헤더에 대한 값 수집 {#gather-values-for-required-headers}

을 호출하기 위해 [!DNL Adobe Experience Platform] API, 먼저 다음을 완료해야 합니다. [인증 자습서](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html){target="_blank"}. 인증 자습서를 완료하면 모든 항목에서 필요한 각 헤더에 대한 값이 제공됩니다 [!DNL Experience Platform] 아래와 같이 API 호출:

* `Authorization: Bearer {ACCESS_TOKEN}`
* `x-api-key: {API_KEY}`
* `x-gw-ims-org-id: {IMS_ORG}`
* `x-sandbox-name: {SANDBOX_NAME}`

페이로드(POST, PUT, PATCH)가 포함된 모든 요청에는 추가 헤더가 필요합니다.

* `Content-Type: application/json`

## 다음 단계 {#next-steps}

이 문서에서는 [!DNL Offer Library] API. 이제 이 개발자 안내서에 제공된 샘플 호출로 진행하여 지침을 따를 수 있습니다.

## 방법 비디오 {#video}

다음 비디오는 의사 결정 관리의 구성 요소에 대한 이해를 돕기 위한 것입니다.

>[!VIDEO](https://video.tv.adobe.com/v/329919?quality=12)

