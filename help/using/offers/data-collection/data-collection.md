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
source-wordcount: '386'
ht-degree: 1%

---

# 의사 결정 관리 데이터 수집 {#data-collection}

## 데이터 수집 이해

표시되는 오퍼와 사용자의 상호 작용 방법 등 Adobe Experience Platform에서 offer decisioning 피드백을 수집할 수 있습니다. 이 데이터는 다음 용도로 사용할 수 있습니다.
* [의사 결정 관리 보고서 작성](../reports/get-started-events.md);
* [빈도 제한](../offer-library/add-constraints.md#capping) 규칙 사용;
* 순위 지정 메서드로 사용할 수 있는 [AI 모델](../ranking/create-ranking-strategies.md)을(를) 빌드하고 있습니다.

## 이벤트 유형

데이터 수집 방법은 캡처하려는 이벤트 유형에 따라 다릅니다.

### 의사 결정 이벤트

의사 결정 관리에서 결정을 내릴 때마다 해당 결정 이벤트와 관련된 정보는 모든 채널에 대해 Adobe Experience Platform으로 전송되는 **자동**&#x200B;입니다. [자세히 알아보기](../reports/get-started-events.md)

### 노출 및 클릭 이벤트

의사 결정 관리 노출 횟수 및 클릭 수는 다음과 같이 정의됩니다.

* **노출** 이벤트는 오퍼가 사용자에게 표시되는 경우입니다.

* **click** 이벤트는 사용자가 오퍼를 클릭하거나 오퍼와 상호 작용할 때입니다.

사용된 [!DNL Journey Optimizer] 채널에 따라 노출 횟수 및 클릭 수에 대한 피드백이 캡처됩니다.

[!DNL Journey Optimizer] **자동으로**&#x200B;하여 작성한 **전자 메일** 노출 횟수 및 클릭 수를 추적합니다.

그러나 **대부분의 채널**&#x200B;에서는 노출 횟수 및 클릭 수를 **경험 이벤트**(으)로 Adobe Experience Platform에 전송해야 합니다. 여기에는 다음 항목이 포함되어 있습니다.

* 오퍼를 렌더링하기 위해 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html){target="_blank"}를 사용하는 웹 페이지

* 오퍼를 렌더링하기 위해 [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html){target="_blank"}를 사용하는 모바일 앱 - [자세히 알아보기](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer-decisioning/#ab-sj-tracking-servers){target="_blank"}
* 키오스크
* 서드파티 애플리케이션을 통해 전송된 메시지
  <!--Mobile push notifications authored by [!DNL Journey Optimizer] - [Learn more](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer/api-reference/#handlenotificationresponse){target="_blank"}-->

>[!NOTE]
>
>의사 결정 API 요청을 사용하여 오퍼를 받는 채널에는 경험 이벤트로 전송된 피드백이 필요합니다. 즉, 오퍼에 렌더링 방법에 대한 지침이 필요한 경우 경험 이벤트로 피드백을 보내야 한다고 가정할 수 있습니다.

### 사용자 지정 이벤트

오퍼에 연결된 사용자 지정 이벤트에 대한 피드백은 사용자 고유의 환경 설정에 따라 Adobe Experience Platform으로 전송될 수 있습니다. 예를 들어 오퍼에 *관심 있음*, *관심 없음* 등의 여러 단추가 있는 경우 이러한 이벤트를 별도로 보낼 수 있지만, 이러한 이벤트를 경험 이벤트로 보낼 수도 있습니다.

## 피드백 데이터 보내기

피드백 데이터를 전송하려면 이벤트를 수집할 데이터 세트를 만들고 각 이벤트 유형에 대해 Adobe Experience Platform으로 전송할 경험 이벤트를 정의해야 합니다.

* [이 섹션](create-dataset.md)에서 경험 이벤트를 수집할 데이터 집합을 만드는 방법을 알아봅니다.

* [이 섹션](schema-requirement.md)에서 피드백 데이터를 보낼 경험 이벤트를 정의하는 방법을 알아보세요.
