---
solution: Journey Optimizer
product: journey optimizer
title: API를 사용하여 캠페인 트리거
description: Journey Optimizer API를 사용하여 캠페인을 트리거하는 방법 알아보기
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: 캠페인, API 트리거, REST, 최적화 도구, 메시지
exl-id: 0ef03d33-da11-43fa-8e10-8e4b80c90acb
source-git-commit: 47185cdcfb243d7cb3becd861fec87abcef1f929
workflow-type: tm+mt
source-wordcount: '1005'
ht-degree: 2%

---

# API를 사용하여 캠페인 트리거 {#trigger-campaigns}

## API 트리거 캠페인 기본 정보 {#about}

[!DNL Journey Optimizer]을(를) 사용하면 캠페인을 만든 다음 [대화형 메시지 실행 REST API](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution)를 사용하는 사용자 트리거를 기반으로 외부 시스템에서 실행할 수 있습니다. 이를 통해 암호 재설정, OTP 토큰 등과 같은 다양한 마케팅 및 트랜잭션 메시지 요구 사항을 처리할 수 있습니다.

이렇게 하려면 먼저 Journey Optimizer에서 API 트리거 캠페인을 만든 다음 API 호출을 통해 실행을 시작해야 합니다.

![](../rn/assets/do-not-localize/api-triggered.gif)

API 트리거 캠페인에 사용할 수 있는 채널은 이메일, SMS 및 푸시 메시지입니다.

>[!NOTE]
>
>현재 빠른 전송 모드는 푸시 알림 API 트리거 캠페인에 대해 지원되지 않습니다.

➡️ [비디오에서 이 기능 살펴보기](#video)

## API 트리거 캠페인 만들기 {#create}

### 캠페인 구성 및 활성화 {#create-activate}

API 트리거 캠페인을 만들려면 아래 단계를 따르십시오. 캠페인을 만드는 방법에 대한 자세한 정보는 [이 섹션](create-campaign.md)에서 확인할 수 있습니다.

1. **[!UICONTROL API 트리거]** 유형으로 새 캠페인을 만드십시오.

1. 보내려는 통신 유형에 따라 **[!UICONTROL 마케팅]** 또는 **[!UICONTROL 트랜잭션]** 범주를 선택하십시오.

1. 메시지를 보내는 데 사용할 지원되는 채널 및 관련 채널 구성 중 하나를 선택한 다음 **[!UICONTROL 만들기]**&#x200B;를 클릭합니다.

   ![](assets/api-triggered-type.png)

1. 캠페인에 대한 제목과 설명을 지정한 다음 **[!UICONTROL 콘텐츠 편집]**&#x200B;을 클릭하여 전송할 메시지를 구성하세요.

   >[!NOTE]
   >
   >메시지를 개인화하는 데 활용할 수 있는 API 페이로드에 추가 데이터를 전달할 수 있습니다. [자세히 알아보기](#contextual)
   >
   >콘텐츠에 수많은 상황별 데이터 또는 방대한 컨텍스트 데이터를 사용하면 성능에 영향을 줄 수 있습니다.

1. **[!UICONTROL 대상]** 섹션에서 개인을 식별하는 데 사용할 네임스페이스를 지정하십시오.

   * **트랜잭션** 유형 캠페인을 만드는 경우 API 호출에서 대상 프로필을 정의해야 합니다. **[!UICONTROL 새 프로필 만들기]** 옵션을 사용하면 데이터베이스에 없는 프로필을 자동으로 만들 수 있습니다. [캠페인 실행 시 프로필 만들기에 대해 자세히 알아보기](#profile-creation)

     >[!NOTE]
     >
     >단일 API 호출은 최대 20개의 고유 수신자를 지원합니다. 각 수신자는 고유한 사용자 ID를 가져야 하며, 중복된 사용자 ID는 허용되지 않습니다. 자세한 내용은 [대화형 메시지 실행 API 설명서](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution/operation/postIMUnitaryMessageExecution){target="_blank"}를 참조하세요.

   * **마케팅** 유형 캠페인의 경우 **[!UICONTROL 대상]** 단추를 클릭하여 타깃팅할 대상을 선택하십시오.

1. 캠페인의 시작 및 종료 날짜를 구성합니다.

   캠페인에 대한 특정 시작 날짜 및/또는 종료 날짜를 구성하는 경우 이 날짜 외에는 실행되지 않으며, API에 의해 캠페인이 트리거되면 API 호출이 실패합니다.

1. **[!UICONTROL 활성화하려면 검토]**&#x200B;를 클릭하여 캠페인이 올바르게 구성되었는지 확인한 다음 활성화하십시오.

이제 API에서 캠페인을 실행할 준비가 되었습니다. [자세히 알아보기](#execute)

### 캠페인 실행 {#execute}

캠페인이 활성화되면 생성된 샘플 cURL 요청을 검색하고 API에 사용하여 페이로드를 빌드하고 캠페인을 트리거해야 합니다.

1. 캠페인을 연 다음 **[!UICONTROL cURL 요청]** 섹션에서 페이로드 요청을 복사하여 붙여 넣으십시오. 이 페이로드에는 메시지에 사용된 모든 개인화(프로필 및 컨텍스트) 변수가 포함됩니다. 캠페인이 라이브되면 사용할 수 있습니다.

   ![](assets/api-triggered-curl.png)

1. 이 cURL 요청을 API에 사용하여 페이로드를 빌드하고 캠페인을 트리거합니다. 자세한 내용은 [대화형 메시지 실행 API 설명서](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution)를 참조하세요.


   API 호출 예는 [이 페이지](https://developer.adobe.com/journey-optimizer-apis/references/messaging-samples/)에서도 사용할 수 있습니다.

   >[!NOTE]
   >
   >캠페인을 생성할 때 특정 시작 날짜 및/또는 종료 날짜를 구성했다면 이 날짜 이후에 실행되지 않고 API 호출이 실패합니다.

## API가 트리거된 캠페인에서 컨텍스트 속성 사용 {#contextual}

API 트리거 캠페인을 사용하면 API 페이로드에서 추가 데이터를 전달하고 캠페인 내에서 이를 사용하여 메시지를 개인화할 수 있습니다.

고객이 암호를 재설정하고자 하고 서드파티 도구에서 생성된 암호 재설정 URL을 전송하고자 하는 이 예를 살펴보겠습니다. API 트리거된 캠페인을 사용하면 이렇게 생성된 URL을 API 페이로드에 전달하고 이를 캠페인에 활용하여 메시지에 추가할 수 있습니다.

>[!NOTE]
>
>프로필 활성화 이벤트와 달리 REST API에서 전달된 컨텍스트 데이터는 일회성 통신에 사용되며 프로필에 대해 저장되지 않습니다. 네임스페이스가 누락된 경우 최대 네임스페이스 세부 정보로 프로필이 만들어집니다.

캠페인에서 이러한 데이터를 사용하려면 해당 데이터를 API 페이로드에 전달하고 개인화 편집기를 사용하여 메시지에 추가해야 합니다. 이렇게 하려면 `{{context.<contextualAttribute>}}` 구문을 사용합니다. 여기서 `<contextualAttribute>`은(는) 전달할 데이터가 포함된 API 페이로드의 변수 이름과 일치해야 합니다.

`{{context.<contextualAttribute>}}` 구문은 String 데이터 형식에만 매핑됩니다.

![](assets/api-triggered-context.png)


>[!IMPORTANT]
>
>요청에 전달된 컨텍스트 속성은 200kb를 초과할 수 없으며 항상 유형 문자열을 고려합니다.
>
>`context.system` 구문은 Adobe 내부 사용으로만 제한되며 컨텍스트 특성을 전달하는 데 사용해서는 안 됩니다.

지금은 왼쪽 레일 메뉴에서 사용할 수 있는 컨텍스트 속성이 없습니다. [!DNL Journey Optimizer]에서 검사를 수행하지 않고 개인화 식에서 직접 특성을 입력해야 합니다.

## 캠페인 실행 시 프로필 만들기 {#profile-creation}

경우에 따라 시스템에 없는 프로필로 트랜잭션 메시지를 보내야 할 수도 있습니다. 예를 들어 알 수 없는 사용자가 웹 사이트에서 암호를 재설정하려고 하는 경우입니다.

데이터베이스에 프로필이 없는 경우, Journey Optimizer에서 캠페인을 실행할 때 프로필을 자동으로 만들어 이 프로필로 메시지를 보낼 수 있습니다.

>[!IMPORTANT]
>
>트랜잭션 메시지의 경우 이 기능은 플랫폼에 이미 존재하는 많은 프로필이 있는 대용량 트랜잭션 전송 사용 사례에서 **매우 작은 볼륨 프로필 만들기**&#x200B;에 제공됩니다.

캠페인 실행 시 프로필 만들기를 활성화하려면 **[!UICONTROL 대상자]** 섹션에서 **[!UICONTROL 새 프로필 만들기]** 옵션을 켜십시오. 이 옵션이 비활성화되면 모든 전송에 대해 알 수 없는 프로필이 거부되고 API 호출이 실패합니다.

![](assets/api-triggered-create-profile.png)

>[!NOTE]
>
>**AJO 대화형 메시징 프로필 데이터 집합** 데이터 집합에서 각 아웃바운드 채널(이메일, SMS 및 푸시)에 대해 각각 세 개의 기본 네임스페이스(이메일, 전화 및 ECID)에 알 수 없는 프로필이 만들어집니다. 그러나 사용자 지정 네임스페이스를 사용하는 경우 동일한 사용자 지정 네임스페이스로 ID가 만들어집니다.

## 사용 방법 비디오 {#video}

대화형 메시지 실행 REST API를 사용하여 사용자 상호 작용을 기반으로 외부 시스템에서 캠페인을 만들고 트리거하는 방법에 대해 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/3452732?quality=12&captions=kor)
