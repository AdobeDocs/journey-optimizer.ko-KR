---
solution: Journey Optimizer
product: journey optimizer
title: AJO 메시지 내보내기 스키마
description: AJO 메시지 내보내기 데이터 세트에서 사용할 수 있는 필드에 대해 알아봅니다
feature: Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: 내보내기, 메시지, 데이터 세트, 스키마, 이메일, SMS
feature_v2: []
subfeature_v2: id: cf64c7f6-7428-4ae5-b158-8df9771f38f4
source-git-commit: 0d9c480cc48c4352e82d1f4624c65fc16a60b959
workflow-type: tm+mt
source-wordcount: 447
ht-degree: 3%

---

# AJO 메시지 내보내기 스키마 {#ajo-message-export-schema}

>[!BEGINSHADEBOX]

**이 페이지에서:** 보낸 전자 메일 및 SMS 메시지 콘텐츠를 Adobe Experience Platform에 저장하는 AJO 메시지 내보내기 데이터 세트의 구조 및 개별 필드를 살펴봅니다.

>[!ENDSHADEBOX]

이메일 또는 SMS 채널 구성에서 **메시지 내보내기**&#x200B;를 사용하도록 설정하면 보낸 메시지 콘텐츠가 [!DNL Adobe Experience Platform]의 **AJO 메시지 내보내기 데이터 세트**&#x200B;에 기록됩니다.

이 섹션에는 내보낸 데이터 세트에서 사용할 수 있는 필드가 나열됩니다.

## 데이터 세트 필드

+++ 경험(_E)

**필드:** `_experience`\
**유형:** 개체

+++

+++ _experience > customerJourneyManagement

**필드:** `customerJourneyManagement`\
**유형:** 개체

+++

+++ _experience > customerJourneyManagement > messageDeliveryMetadata

**필드:** `messageDeliveryMetadata`\
**유형:** 개체

+++

+++ _experience > customerJourneyManagement > messageDeliveryMetadata > emailMetadata

**필드:** `emailMetadata`\
**유형:** 개체

* 수신자

  **필드:** `recipient`\
  **유형:** 개체

   * bcc

     **필드:** `bcc`\
     문자열의 **유형:** 배열

   * 참조

     **필드:** `cc`\
     문자열의 **유형:** 배열

   * 이메일

     **필드:** `email`\
     **유형:** 문자열

   * 이름

     **필드:** `name`\
     **유형:** 문자열

* 보낸 사람

  **필드:** `sender`\
  **유형:** 개체

   * 이메일

     **필드:** `email`\
     **유형:** 문자열

   * 오류 이메일

     **필드:** `errorEmail`\
     **유형:** 문자열

   * 이름

     **필드:** `name`\
     **유형:** 문자열

   * replyToEmail

     **필드:** `replyToEmail`\
     **유형:** 문자열

   * replyToname

     **필드:** `replyToName`\
     **유형:** 문자열

+++

+++ _experience > customerJourneyManagement > messageDeliveryMetadata > smsMetadata

**필드:** `smsMetadata`\
**유형:** 개체

* 수신자

  **필드:** `recipient`\
  **유형:** 개체

   * 번호

     **필드:** `number`\
     **유형:** 문자열

* 보낸 사람

  **필드:** `sender`\
  **유형:** 개체

   * 숫자

     **필드:** `numbers`\
     문자열의 **유형:** 배열

+++

+++ _experience > customerJourneyManagement > messageExecution

**필드:** `messageExecution`\
**유형:** 개체

* 대상자

  **필드:** `audience`\
  **유형:** 개체

   * ID

     **필드:** `id`\
     **유형:** 문자열

   * 유형

     **필드:** `type`\
     **유형:** 문자열

* fragmentPublicationIDs

  **필드:** `fragmentPublicationIDs`\
  문자열의 **유형:** 배열

* 메타데이터

  **필드:** `metadata`\
  **유형:** 맵

   * [맵 키]

     **유형:** 문자열

* parentSourceMeta

  **필드:** `parentSourceMeta`\
  **유형:** 개체

   * sourceActionId

     **필드:** `sourceActionID`\
     **유형:** 문자열

   * sourceID

     **필드:** `sourceID`\
     **유형:** 문자열

   * sourceType

     **필드:** `sourceType`\
     **유형:** 문자열

   * 소스 버전 ID

     **필드:** `sourceVersionID`\
     **유형:** 문자열

* 일괄 처리 인스턴스 ID

  **필드:** `batchInstanceID`\
  **유형:** 문자열

* campaignActionId

  **필드:** `campaignActionID`\
  **유형:** 문자열

* 캠페인 ID

  **필드:** `campaignID`\
  **유형:** 문자열

* 캠페인 버전 ID

  **필드:** `campaignVersionID`\
  **유형:** 문자열

* 여정 작업 ID

  **필드:** `journeyActionID`\
  **유형:** 문자열

* 여정 버전 ID

  **필드:** `journeyVersionID`\
  **유형:** 문자열

* 여정 버전 인스턴스 ID

  **필드:** `journeyVersionInstanceID`\
  **유형:** 문자열

* 여정 버전 노드 ID

  **필드:** `journeyVersionNodeID`\
  **유형:** 문자열

* messageExecutionID

  **필드:** `messageExecutionID`\
  **유형:** 문자열

* messageID

  **필드:** `messageID`\
  **유형:** 문자열

* messagePublicationID

  **필드:** `messagePublicationID`\
  **유형:** 문자열

* messageType

  **필드:** `messageType`\
  **유형:** 문자열

* waveID

  **필드:** `waveID`\
  **유형:** 문자열

+++

+++ 경험 > customerJourneyManagement > messageProfile(_e)

**필드:** `messageProfile`\
**유형:** 개체

* 채널

  **필드:** `channel`\
  **유형:** 개체

   * contentType

     **필드:** `contentTypes`\
     문자열의 **유형:** 배열

   * 위치 유형

     **필드:** `locationTypes`\
     문자열의 **유형:** 배열

   * 지표 유형

     **필드:** `metricTypes`\
     문자열의 **유형:** 배열

   * _ID

     **필드:** `_id`\
     **유형:** 문자열

   * 유형(_t)

     **필드:** `_type`\
     **유형:** 문자열

   * mediaAction

     **필드:** `mediaAction`\
     **유형:** 문자열

   * mediaType

     **필드:** `mediaType`\
     **유형:** 문자열

   * 모드

     **필드:** `mode`\
     **유형:** 문자열

   * referringSource

     **필드:** `referringSource`\
     **유형:** 문자열

   * typeAtSource

     **필드:** `typeAtSource`\
     **유형:** 문자열

* isSendTimeOptimized

  **필드:** `isSendTimeOptimized`\
  **유형:** 부울

* isTestExecution

  **필드:** `isTestExecution`\
  **유형:** 부울

* 메시지 프로필 ID

  **필드:** `messageProfileID`\
  **유형:** 문자열

* messageProfileTrackingId

  **필드:** `messageProfileTrackingID`\
  **유형:** 문자열

* requestID

  **필드:** `requestID`\
  **유형:** 문자열

* secondaryDimensionID

  **필드:** `secondaryDimensionID`\
  **유형:** 문자열

* secondaryDimensionName

  **필드:** `secondaryDimensionName`\
  **유형:** 문자열

* 변형

  **필드:** `variant`\
  **유형:** 문자열

+++

+++ _experience > customerJourneyManagement > messageRenderedContent

**필드:** `messageRenderedContent`\
**유형:** 개체

* emailContent

  **필드:** `emailContent`\
  **유형:** 개체

   * html

     **필드:** `html`\
     **유형:** 문자열

   * 제목

     **필드:** `subject`\
     **유형:** 문자열

   * 텍스트

     **필드:** `text`\
     **유형:** 문자열

* smsContent

  **필드:** `smsContent`\
  **유형:** 개체

   * 미디어

     **필드:** `media`\
     **유형:** 문자열

   * message

     **필드:** `message`\
     **유형:** 문자열

   * 제목

     **필드:** `title`\
     **유형:** 문자열

+++

+++ identityMap

**필드:** `identityMap`\
**유형:** 맵

* [맵 키]

  개체의 **유형:** 배열

   * authenticatedState

     **필드:** `authenticatedState`\
     **유형:** 문자열

   * ID

     **필드:** `id`\
     **유형:** 문자열

   * 기본

     **필드:** `primary`\
     **유형:** 부울

+++

+++ eventType

**필드:** `eventType`\
**유형:** 문자열

+++

+++ 제작자

**필드:** `producedBy`\
**유형:** 문자열

+++

+++ 타임스탬프

**필드:** `timestamp`\
**유형:** dateTime

+++

