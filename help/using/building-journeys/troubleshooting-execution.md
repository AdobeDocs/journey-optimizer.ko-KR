---
solution: Journey Optimizer
product: journey optimizer
title: 라이브 여정 실행 문제 해결
description: 라이브 여정 실행 시 오류를 해결하는 방법 알아보기
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 문제 해결, 문제 해결, 여정, 확인, 오류
exl-id: fd670b00-4ebb-4a3b-892f-d4e6f158d29e
source-git-commit: e3b0bf6594e15f2d80d1e6782ec513c93f18c649
workflow-type: tm+mt
source-wordcount: '702'
ht-degree: 36%

---

# 라이브 여정 실행 문제 해결 {#troubleshooting-execution}

이 섹션에서는 여정 이벤트 문제 해결, 프로필이 여정에 입력되었는지 여부, 프로필이 이벤트를 탐색하는 방법 및 메시지가 전송되었는지 확인하는 방법을 알아봅니다.

여정을 테스트하거나 게시하기 전에 오류를 해결할 수도 있습니다. 이 페이지에서 [하는 방법](troubleshooting.md)을 알아보세요.

인바운드 액션을 사용 중인 경우 이 페이지에서 [문제를 해결하는 방법](troubleshooting-inbound.md)을 알아보세요.

## 이벤트가 제대로 전송되었는지 확인 {#checking-that-events-are-properly-sent}

여정의 시작점은 항상 이벤트입니다. Postman과 같은 도구를 사용하여 테스트를 수행할 수 있습니다.

이러한 도구를 통해 보내는 API 호출이 올바르게 전송되었는지 여부를 확인할 수 있습니다. 오류가 반환되면 호출에 문제가 있는 것입니다. 페이로드, 헤더(특히 조직 ID) 및 대상 URL을 다시 확인하십시오. 올바른 URL이 무엇인지를 관리자에게 물어볼 수 있습니다.

이벤트는 소스에서 여정으로 직접 푸시되지 않습니다. 실제로 여정은 Adobe Experience Platform의 수집 API 스트리밍에 의존합니다. 따라서 이벤트 관련 문제가 발생하면 [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html?lang=ko){target="_blank"}에서 수집 API 스트리밍 문제 해결을 참조할 수 있습니다.

`ERR_MODEL_RULES_16` 오류로 인해 여정에서 테스트 모드를 사용하도록 설정하지 못하는 경우 채널 작업을 사용할 때 사용된 이벤트에 [ID 네임스페이스](../audience/get-started-identity.md)가 포함되어 있는지 확인하십시오.

ID 네임스페이스는 테스트 프로필을 고유하게 식별하는 데 사용됩니다. 예를 들어 테스트 프로필을 식별하는 데 이메일을 사용하는 경우 ID 네임스페이스 **이메일**&#x200B;을(를) 선택해야 합니다. 고유 식별자가 전화번호인 경우 ID 네임스페이스 **Phone**&#x200B;을(를) 선택해야 합니다.

## 사람들이 여정을 입력하는지 확인 {#checking-if-people-enter-the-journey}

여정 보고는 여정에 들어오는 사람들을 실시간으로 측정합니다.

이벤트를 성공적으로 보냈는데 여정에 들어오는 사람이 없다면 여정에서 이벤트 보내기 및 이벤트 받기 사이에 무언가 잘못된 것입니다.

아래 질문과 함께 문제 해결을 시작할 수 있습니다.

* 수신 이벤트를 기다리는 여정이 테스트 모드이거나 라이브 상태인 것이 확실합니까?
* 페이로드 미리 보기에서 페이로드를 복사하기 전에 이벤트를 저장했습니까?
* 이벤트 페이로드에 이벤트 ID가 포함되어 있습니까?
* 정확한 URL을 입력했습니까?
* 이벤트 구성 창에서 페이로드 구조 미리 보기를 사용하여 수집 API 스트리밍 페이로드 구조를 따랐습니까? [이 페이지](../event/about-creating.md#preview-the-payload)를 참조하십시오.
* 이벤트 헤더에 올바른 키-값 쌍을 사용했습니까?

  ```
  X-gw-ims-org-id - your organization's ID
  Content-type - application/json
  ```

## 사람들이 여정을 탐색하는 방법 확인 {#checking-how-people-navigate-through-the-journey}

여정 보고는 여정 내에서 개인 사용자의 진행 상황을 측정합니다. 사람들이 어디에서 왜 멈췄는지를 쉽게 파악할 수 있습니다.

확인할 몇 가지 사항은 다음과 같습니다.

* 그 사람을 배제하는 조건 때문입니까? 예를 들어 조건이 &quot;gender = male&quot;인데 당사자가 여성입니다. 이 검사는 조건이 너무 복잡하지 않은 경우 비즈니스 사용자가 수행할 수 있습니다.
* 데이터 소스에 대한 호출이 응답하지 않기 때문입니까? 여정이 테스트 모드일 때는 이 정보를 테스트 모드 로그에서 볼 수 있습니다. 여정이 라이브 상태일 때는 관리자가 데이터 소스에 대한 직접 호출을 테스트하고 수신된 답변을 확인할 수 있습니다. 관리자가 여정을 복제하여 테스트할 수도 있습니다.

## 메시지를 성공적으로 보냈는지 확인 {#checking-that-messages-are-sent-successfully}

개인 사용자가 여정에서 플로우를 제대로 따랐는데 받아야 할 메시지를 받지 못하는 경우에는 다음을 확인하면 됩니다.

* [!DNL Journey Optimizer]이(가) 메시지를 보낼 요청을 올바르게 고려했습니다. 비즈니스 사용자는 전송되어야 하는 메시지에 액세스하여 최신 실행 시간이 여정 실행 시간과 일치하는지 확인할 수 있습니다. 최신 API 호출/이벤트를 수신했는지 확인할 수도 있습니다.
* [!DNL Journey Optimizer]이(가) 메시지를 보냈습니다. 여정 보고를 확인하여 오류가 없는지 확인합니다.

사용자 지정 작업을 통해 전송된 메시지의 경우, 여정 테스트 중에 확인할 수 있는 유일한 사실은 사용자 지정 작업 시스템의 호출이 오류로 이어졌는지 여부입니다. 사용자 지정 작업과 연결된 외부 시스템에 대한 호출이 오류로 이어지지 않았는데 메시지가 전송되지 않은 경우에는 외부 시스템 쪽에서 몇 가지 조사를 수행해야 합니다.
