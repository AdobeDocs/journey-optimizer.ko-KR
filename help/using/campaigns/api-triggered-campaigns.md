---
title: API를 사용하여 캠페인 트리거
description: 을 사용하여 캠페인을 트리거하는 방법 알아보기 [!DNL Journey Optimizer] API
hide: true
hidefromtoc: true
exl-id: 0ef03d33-da11-43fa-8e10-8e4b80c90acb
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '642'
ht-degree: 3%

---

# API를 사용하여 캠페인 트리거 {#trigger-campaigns}

## API로 트리거된 캠페인 기본 정보 {#about}

사용 [!DNL Journey Optimizer]를 사용하여 사용자 트리거를 기반으로 캠페인을 만든 다음 외부 시스템에서 캠페인을 호출할 수 있습니다. [대화형 메시지 실행 REST API](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution). 이를 통해 암호 재설정, OTP 토큰 등과 같은 다양한 운영 및 트랜잭션 메시지 요구 사항을 처리할 수 있습니다.

이렇게 하려면 먼저 Journey Optimizer에서 API 트리거 캠페인을 만든 다음 API 호출을 통해 해당 실행을 실행해야 합니다.

API로 트리거되는 캠페인에 사용할 수 있는 채널은 이메일, SMS 및 푸시 메시지 입니다.

>[!NOTE]
>
>대화형 메시지 실행 API는 현재 베타 버전이며 예고 없이 자주 업데이트될 수 있습니다.

## API로 트리거된 캠페인 만들기 {#create}

API 트리거된 캠페인을 만드는 프로세스는 API 페이로드에서 수행되는 대상 선택을 제외하고 예약된 캠페인과 동일하게 유지됩니다. 캠페인을 만드는 방법에 대한 자세한 내용은 [이 섹션](create-campaign.md).

API로 트리거된 캠페인을 만들려면 다음 단계를 수행합니다.

1. 를 사용하여 새 캠페인 만들기 **[!UICONTROL API-triggered]** 유형.

1. 메시지를 보내는 데 사용할 채널과 채널 표면을 선택한 다음 를 클릭합니다 **[!UICONTROL Create]**.

   ![](assets/api-triggered-type.png)

1. 캠페인의 제목과 설명을 지정한 다음 전송할 메시지를 구성합니다.

   ![](assets/api-triggered-properties.png)

   >[!NOTE]
   >
   >메시지를 개인화하는 데 활용할 수 있는 API 페이로드에 추가 데이터를 전달할 수 있습니다. [자세히 보기](#contextual)

1. 세그먼트에서 개인을 식별하는 데 사용할 네임스페이스를 지정합니다.

1. 캠페인의 시작 및 종료 날짜를 구성합니다.

   캠페인에 대한 특정 시작 및/또는 종료 날짜를 구성하는 경우 이러한 날짜 외부에서 실행되지 않으며, API에 의해 캠페인이 트리거되면 API 호출이 실패합니다.

1. 에서 **[!UICONTROL cURL request]** 섹션, 검색 **[!UICONTROL Campaign ID]** 를 사용 중입니다.

   ![](assets/api-triggered-curl.png)

1. 클릭 **[!UICONTROL Review to activate]** 캠페인이 올바르게 구성되어 있는지 확인한 다음 활성화합니다.

## API로 트리거된 캠페인에서 컨텍스트 특성 사용 {#contextual}

API로 트리거되는 캠페인을 사용하여 API 페이로드에서 추가 데이터를 전달하고 캠페인 내에서 사용하여 메시지를 개인화할 수 있습니다.

고객이 암호를 재설정하고 타사 도구에서 생성된 암호 재설정 URL을 이 고객에게 전송하려는 경우를 예로 들어 보겠습니다. API로 트리거되는 캠페인을 사용하여 생성된 이 URL을 API 페이로드에 전달하고 캠페인에 활용하여 메시지에 추가할 수 있습니다.

>[!NOTE]
>
>프로필 사용 이벤트와 달리 REST API에서 전달된 컨텍스트 데이터는 일회성 통신에 사용되며 프로필에 대해 저장되지는 않습니다. 프로파일이 누락된 경우 네임스페이스에 대한 세부 정보를 사용하여 생성됩니다.

캠페인에서 이러한 데이터를 사용하려면 API 페이로드에 전달하고 표현식 편집기를 사용하여 메시지에 추가해야 합니다. 이렇게 하려면 `{{context.<contextualAttribute>}}` 구문, 위치 `<contextualAttribute>` 전달하려는 데이터가 포함된 API 페이로드의 변수 이름과 일치해야 합니다.

다음 `{{context.<contextualAttribute>}}` 구문은 문자열 데이터 유형에만 매핑됩니다.

![](assets/api-triggered-context.png)

>[!IMPORTANT]
>
>다음 `context.system` 구문은 Adobe 내부 사용으로만 제한되며 컨텍스트 속성을 전달하는 데 사용해서는 안 됩니다.
현재는 왼쪽 레일 메뉴에서 사용할 수 있는 상황별 속성이 없습니다. 에서는 확인이 수행되지 않고 속성을 개인화 표현식에 직접 입력해야 합니다. [!DNL Journey Optimizer].

## 캠페인 실행 {#execute}

API로 트리거된 캠페인을 실행하려면 먼저 해당 ID를 검색하고 API 페이로드에 전달해야 합니다. 이렇게 하려면 캠페인을 열고 ID를 **[!UICONTROL cURL request]** 섹션을 참조하십시오.

![](assets/api-triggered-id.png)

그런 다음 이 ID를 API 페이로드에 사용하여 캠페인을 트리거할 수 있습니다. 자세한 내용은 [대화형 메시지 실행 API 설명서](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution) 추가 정보.

>[!NOTE]
>
>캠페인을 만들 때 특정 시작 및/또는 종료 날짜를 구성한 경우 이러한 날짜 외부에서 실행되지 않고 API 호출이 실패합니다.

## 추가 리소스

* [캠페인 시작](get-started-with-campaigns.md)
* [캠페인 만들기](create-campaign.md)
* [캠페인 수정 또는 중지](modify-stop-campaign.md)
* [캠페인 라이브 보고서](campaign-live-report.md)
* [캠페인 글로벌 보고서](campaign-global-report.md)
