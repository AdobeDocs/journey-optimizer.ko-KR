---
title: 제외 목록
description: 억제 목록이 무엇이고, 그 목적과 그 목록에 포함된 것을 알아봅니다.
feature: 전달성
topic: 콘텐츠 관리
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '643'
ht-degree: 4%

---

# 제외 목록 {#suppression-list}

![](assets/do-not-localize/badge.png)

이러한 연락처로 보내면 전송 신뢰도와 전송 속도가 저하될 수 있으므로 게재에서 제외하려는 이메일 주소로 제외 목록이 구성됩니다.

[!DNL Journey Optimizer] 제외 목록은 사용자의 환경 수준에서 관리됩니다.

여기에는 샌드박스 ID와 연결된 IMS 조직 ID와 관련된 것으로, 단일 클라이언트 환경의 모든 메일링 간에 표시되지 않는 이메일 주소와 도메인이 수집됩니다.

<!--It gathers spam complaints, hard bounces, and soft bounces that occur consistently.-->

## 제외 목록이 왜 있습니까?{#why-suppression-list}

받은 편지함 소유자가 수신한 이메일 메시지를 제어하고 원하는 메시지만 수신하도록 하기 위해, 인터넷 서비스 공급자(ISP) 및 상용 스팸 필터는 IP 주소와 사용 도메인에 따라 전자 메일 발송자의 전체 평판을 추적하는 자체 알고리즘을 제공합니다.

피드백에 동의하지 않는 경우(예: 스팸 불만, 바운스 수 등) 그들이 당신의 명성을 떨어뜨릴 것이라는 것을 고려해보겠습니다. 억제 목록은 ISP의 피드백을 확인하는 데 도움이 됩니다.

이메일 주소가 표시되지 않는 수신자는 메시지 배달에서 자동으로 제외됩니다. 이를 통해 게재 속도를 높일 수 있습니다. 오류율은 게재 속도에 상당한 영향을 미치기 때문입니다.

## 억제 목록에 뭐가 있어요?{#what-s-on-suppression-list}

전자 메일 주소는 다음과 같이 제외 목록에 추가됩니다.

* 모든 **하드 바운스** 및 **스팸 불만**&#x200B;은(는) 한 번 발생한 후 해당 이메일 주소를 제외 목록에 자동으로 보냅니다.

* **소프트** 바운스 및  **** 임시 ignorerrors는 이메일 주소를 제외 목록에 즉시 전송하지 않지만, 오류 카운터를 증가시킵니다. 그런 다음 여러 번 다시 시도되고 오류 카운터가 임계값에 도달하면 주소가 제외 목록에 추가됩니다. [다시 시도](configuration/retries.md)에 대해 자세히 알아보십시오.

<!--You can also manually add an address to the suppression list. Manual category will be available when ability to manually add an address to the suppression list (via API) is released.-->

>[!NOTE]
>
>[!DNL Journey Optimizer]에서 전자 메일을 받지 않으므로 가입 해지된 사용자의 주소를 제외 목록으로 보낼 수 없습니다. 선택 사항은 Experience Platform 수준에서 처리됩니다. [옵트아웃](../using/consent.md)에 대해 자세히 알아보십시오.
<!--Email addresses of recipients who **unsubscribe** from your sendings are NOT sent to the suppression list. Confirmed by eng.: "Subscribe and Unsubscribe are handled by the Consent/Subscription service. A user that opts out will not make it to the suppression list – we won’t send them emails."-->

각 주소에 대해 억제되는 기본 이유와 억제 범주(소프트, 하드 등)는 제외 목록에 표시됩니다. [이 섹션](configuration/manage-suppression-list.md)에서 제외 목록에 액세스 및 관리하는 방법에 대해 자세히 알아보십시오.

<!--Once a message is sent, the message logs allow you to view the delivery status for each recipient and the associated failure type and reason. [Learn more about monitoring message execution](monitoring.md). NO ACCESS TO LOGS YET-->

### 게재 실패 {#delivery-failures}

게재가 실패할 경우 세 가지 유형의 오류가 있습니다.

* **하드 바운스**. 하드 바운스는 잘못된 이메일 주소(즉, 존재하지 않는 이메일 주소)를 나타냅니다. 여기에는 &#39;알 수 없는 사용자&#39;와 같이 주소가 유효하지 않다고 명시적으로 설명하는 수신 이메일 서버의 바운스 메시지가 포함됩니다.
* **소프트 바운스**. 유효한 이메일 주소에 대해 발생한 임시 이메일 바운스입니다.
* **무시됨**. 유효한 전자 메일 주소에 대해 발생했지만 실패한 연결 시도, 임시 스팸 관련 문제(전자 메일 신뢰도) 또는 일시적인 기술 문제와 같이 일시적인 것으로 알려진 전자 메일 바운스입니다.<!--does it exist in CJM?-->

**하드 바운스**&#x200B;는 전자 메일 주소를 제외 목록에 자동으로 추가합니다.

너무 여러 번 발생하는 **소프트 바운스** 또는 **무시된** 오류도 여러 번 다시 시도한 후 이메일 주소를 제외 목록에 보냅니다. [다시 시도하는 방법에 대해 자세히 알아보기](configuration/retries.md)

이러한 주소로 계속 보내는 경우, ISP에 사용자가 메일 주소 목록 유지 관리 우수 사례를 따르지 않을 수 있음을 알려 주므로, 배달율에 영향을 줄 수 있습니다.

### 스팸 불만 {#spam-complaints}

제외 목록은 메시지를 스팸으로 표시하는 이메일 주소를 수집합니다. 예를 들어 고객이 귀하로부터 메일을 다시 받지 않도록 요청하는 고객 서비스에 편지를 쓰는 경우, 해당 사용자의 이메일 주소가 사용자 인스턴스에서 억제되고 귀하는 더 이상 해당 주소로 게재할 수 없습니다.

스팸 메일을 제출한 후 수신자에게 보내는 것은 원치 않는 이메일을 보낼 수 있으며 수신자의 의견을 듣지 않을 수도 있다는 정보를 ISP에 알리므로 보내는 데 큰 영향을 줄 수 있습니다.

이로 인해 IP 주소 또는 전송 도메인이 차단될 수 있으며, 이는 이러한 주소가 제외 목록에 있으므로 방지할 수 있습니다.

<!--### Unsubscriptions {#unsubscriptions}

Every email sent to recipients must include an unsubscribe link. Upon clicking this link, if a recipient confirms [opting out](consent.md), the corresponding email address is immediately sent to the suppression list. This user must not receive communication from your brand until subscribed again.
NOT TRUE > "Subscribe and Unsubscribe are handled by the Consent/Subscription service. A user that opts out will not make it to the suppression list – we won’t send them emails."-->

<!--MOVED to Configuration/Retries section

The threshold is set at three errors:
* For the same delivery, at the third attempt, the address is suppressed.
* If there are different deliveries and two errors occur at least 24 hours apart, the error counter is incremented upon each error and the address is also suppressed at the third attempt.
When a delivery is successful after a retry, the error counter of the address is reinitialized.

### Retries {#retries}

If a message fails due to a temporary bounce of the **Ignored** type, retries will be performed for **3.5 days** from the time the message was added to the email queue.

The minimum delay between retries and the maximum number of retries to be performed are ///managed by the Enhanced MTA/// based on how well an IP is performing, both historically and currently at a given domain.

After 3.5 days, any message in the retry queue will be removed from the queue and sent back as a bounce.-->
