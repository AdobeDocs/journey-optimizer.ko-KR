---
title: 데이터 수집
description: 의사 결정 관리 피드백 데이터 수집에 대해 자세히 알아보기
feature: Decision Management, Datasets
topic: Integrations
role: User, Data Engineer, Developer
level: Experienced
exl-id: 278cb255-439c-4ce8-ab59-07df79774b98
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 3%

---

# 의사 결정 관리 데이터 수집 {#data-collection}

## 데이터 수집 이해

표시되는 오퍼와 사용자의 상호 작용 방법 등 Adobe Experience Platform에서 offer decisioning 피드백을 수집할 수 있습니다. 이 데이터는 다음 용도로 사용할 수 있습니다.
* 작성 중 [의사 결정 관리 보고서](../reports/get-started-events.md);
* 사용 [빈도 설정](../offer-library/add-constraints.md#capping) 규칙;
* 빌드 중 [AI 모델](../ranking/create-ranking-strategies.md) 등급 메서드로 사용할 수 있습니다.

## 이벤트 유형

데이터 수집 방법은 캡처하려는 이벤트 유형에 따라 다릅니다.

### 의사 결정 이벤트

의사 결정 관리자가 의사 결정을 내릴 때마다 해당 의사 결정 이벤트와 관련된 정보가 **자동으로** 모든 채널을 위해 Adobe Experience Platform으로 전송됩니다. [자세히 알아보기](../reports/get-started-events.md)

### 노출 및 클릭 이벤트

의사 결정 관리 노출 횟수 및 클릭 수는 다음과 같이 정의됩니다.

* An **노출 횟수** 이벤트는 오퍼가 사용자에게 표시되는 때입니다.

* A **클릭** 이벤트는 사용자가 오퍼를 클릭하거나 오퍼와 상호 작용하는 경우입니다.

노출 횟수 및 클릭 수에 대한 피드백은 다음에 따라 캡처됩니다. [!DNL Journey Optimizer] 사용되는 채널입니다.

**이메일** 작성자: [!DNL Journey Optimizer] **자동으로** 노출 횟수 및 클릭 수를 추적합니다.

그러나 **대부분의 채널** 노출 횟수 및 클릭 수를 다음으로 Adobe Experience Platform에 전송해야 함 **경험 이벤트**. 여기에는 다음 항목이 포함되어 있습니다.

* 를 사용하는 웹 페이지 [Adobe Experience Platform 웹 SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=ko-KR){target="_blank"} 오퍼를 렌더링하려면

* 를 사용하는 모바일 앱 [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html){target="_blank"} to render offers - [Learn more](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer-decisioning/#ab-sj-tracking-servers){target="_blank"}
* 키오스크
* 서드파티 애플리케이션을 통해 전송된 메시지
  <!--Mobile push notifications authored by [!DNL Journey Optimizer] - [Learn more](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer/api-reference/#handlenotificationresponse){target="_blank"}-->

>[!NOTE]
>
>의사 결정 API 요청을 사용하여 오퍼를 받는 채널에는 경험 이벤트로 전송된 피드백이 필요합니다. 즉, 오퍼에 렌더링 방법에 대한 지침이 필요한 경우 경험 이벤트로 피드백을 보내야 한다고 가정할 수 있습니다.

### 사용자 정의 이벤트

오퍼에 연결된 사용자 지정 이벤트에 대한 피드백은 사용자 고유의 환경 설정에 따라 Adobe Experience Platform으로 전송될 수 있습니다. 예를 들어 오퍼에 와 같은 여러 버튼이 있는 경우 *관심 있음*, *관심 없음*&#x200B;등 이러한 이벤트를 별도로 보내려고 할 수도 있지만, 이러한 이벤트를 경험 이벤트로 보낼 수도 있습니다.

## 피드백 데이터 보내기

피드백 데이터를 전송하려면 이벤트를 수집할 데이터 세트를 만들고 각 이벤트 유형에 대해 Adobe Experience Platform으로 전송할 경험 이벤트를 정의해야 합니다.

* 경험 이벤트가 수집될 데이터 세트를 만드는 방법을 알아봅니다 [이 섹션](create-dataset.md).

* 에서 피드백 데이터를 전송할 경험 이벤트를 정의하는 방법을 알아봅니다 [이 섹션](schema-requirement.md).
