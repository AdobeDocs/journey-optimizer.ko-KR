---
title: 제외 목록
description: 억제 목록이 무엇이고, 그 목적과 그 목록에 포함된 것을 알아봅니다.
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
exl-id: a4653378-b70f-454c-a446-ab4a14d2580a
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 2%

---

# 제외 목록 {#suppression-list}

이러한 연락처로 보내면 전송 신뢰도와 전송 속도가 저하될 수 있으므로 게재에서 제외하려는 이메일 주소로 제외 목록이 구성됩니다.

다음 [!DNL Journey Optimizer] 제외 목록은 자체 환경 수준에서 관리됩니다.

여기에는 샌드박스 ID와 연결된 IMS 조직 ID와 관련된 것으로, 단일 클라이언트 환경의 모든 메일링 간에 표시되지 않는 이메일 주소와 도메인이 수집됩니다.

## 제외 목록이 왜 있습니까? {#why-suppression-list}

받은 편지함 소유자가 수신한 이메일 메시지를 제어하고 원하는 메시지만 수신하도록 하기 위해, 인터넷 서비스 공급자(ISP) 및 상용 스팸 필터는 IP 주소와 사용 도메인에 따라 전자 메일 발송자의 전체 평판을 추적하는 자체 알고리즘을 제공합니다.

피드백에 동의하지 않는 경우(예: 스팸 불만, 바운스 수 등) 그들이 당신의 명성을 떨어뜨릴 것이라는 것을 고려해보겠습니다. 억제 목록은 ISP의 피드백을 확인하는 데 도움이 됩니다.

이메일 주소가 표시되지 않는 수신자는 메시지 배달에서 자동으로 제외됩니다. 이를 통해 게재 속도를 높일 수 있습니다. 오류율은 게재 속도에 상당한 영향을 미치기 때문입니다.

## 억제 목록에 뭐가 있어요? {#what-s-on-suppression-list}

전자 메일 주소는 다음과 같이 제외 목록에 추가됩니다.

* 모두 **하드 바운스** 및 **스팸 불만** 한 번 발생하면 해당 이메일 주소를 제외 목록에 자동으로 보냅니다.

* **소프트 바운스** 전자 메일 주소를 제외 목록에 즉시 보내지 않지만 오류 카운터가 증가합니다. 몇 개 [다시 시도](../configuration/retries.md) 그런 다음 오류 카운터가 임계값에 도달하면 주소가 제외 목록에 추가됩니다.

* 다음을 수행할 수도 있습니다 [**수동** 주소 또는 도메인 추가](../configuration/manage-suppression-list.md#add-addresses-and-domains) 제외 목록에 추가합니다.

의 하드 바운스 및 소프트 바운스에 대해 자세히 알아보십시오 [이 섹션](#delivery-failures).

>[!NOTE]
>
>구독하지 않은 사용자의 주소는 보낸 이메일을 받지 않으므로 제외 목록으로 보낼 수 없습니다 [!DNL Journey Optimizer]. 선택 사항은 Experience Platform 수준에서 처리됩니다. 추가 정보 [옵트아웃](consent.md).

각 주소에 대해 억제되는 기본 이유와 억제 범주(소프트, 하드 등)는 제외 목록에 표시됩니다. 의 제외 목록 액세스 및 관리에 대해 자세히 알아보십시오 [이 섹션](../configuration/manage-suppression-list.md).

>[!NOTE]
>
>다음 포함 **[!UICONTROL Suppressed]** 상태는 메시지 전송 프로세스 중에 제외됩니다. 따라서 **여정 보고서** 은(는) 이러한 프로필을 여정을 통해 이동했음을 나타냅니다([세그먼트 읽기](../building-journeys/read-segment.md) 및 [메시지](../building-journeys/journeys-message.md) 활동), **이메일 보고서** 에는 이러한 매개 변수가 포함되지 않습니다. **[!UICONTROL Sent]** 지표는 이메일 전송 전에 필터링됩니다.
>
>추가 정보 [라이브 보고서](../reports/live-report.md) 및 [글로벌 보고서](../reports/global-report.md). 모든 제외 사례에 대한 이유를 알아보려면 [Adobe Experience Platform 쿼리 서비스](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;}.

### 게재 실패 {#delivery-failures}

게재가 실패할 경우 두 가지 유형의 오류가 있습니다.

* **하드 바운스**. 하드 바운스는 잘못된 이메일 주소(즉, 존재하지 않는 이메일 주소)를 나타냅니다. 여기에는 주소가 유효하지 않다고 명시적으로 설명하는 수신 이메일 서버의 바운스 메시지가 포함됩니다.
* **소프트 바운스**. 유효한 이메일 주소에 대해 발생한 임시 이메일 바운스입니다.

A **하드 바운스** 자동으로 이메일 주소를 제외 목록에 추가합니다.

A **소프트 바운스** <!--or an **ignored** error--> 너무 여러 번 발생하는 경우 여러 번 다시 시도한 후 이메일 주소를 제외 목록으로 보냅니다. [다시 시도하는 방법에 대해 자세히 알아보기](../configuration/retries.md)

이러한 주소로 계속 보내는 경우, ISP에 사용자가 메일 주소 목록 유지 관리 우수 사례를 따르지 않을 수 있음을 알려 주므로, 배달율에 영향을 줄 수 있습니다.

### 스팸 불만 {#spam-complaints}

제외 목록은 메시지를 스팸으로 표시하는 이메일 주소를 수집합니다. 예를 들어 고객이 귀하로부터 메일을 다시 받지 않도록 요청하는 고객 서비스에 편지를 쓰는 경우, 해당 사용자의 이메일 주소가 사용자 인스턴스에서 억제되고 귀하는 더 이상 해당 주소로 게재할 수 없습니다.

스팸 메일을 제출한 후 수신자에게 보내는 것은 원치 않는 이메일을 보낼 수 있으며 수신자의 의견을 듣지 않을 수도 있다는 정보를 ISP에 알리므로 보내는 데 큰 영향을 줄 수 있습니다.

이로 인해 IP 주소 또는 전송 도메인이 차단될 수 있으며, 이는 이러한 주소가 제외 목록에 있으므로 방지할 수 있습니다.
