---
solution: Journey Optimizer
product: journey optimizer
title: 금지 목록
description: 제외 목록 사용 방법 알아보기
feature: Deliverability
topic: Content Management
role: Admin
level: Intermediate, Experienced
exl-id: a4653378-b70f-454c-a446-ab4a14d2580a
source-git-commit: f8d62a702824bcfca4221c857acf1d1294427543
workflow-type: tm+mt
source-wordcount: '828'
ht-degree: 11%

---

# 금지 목록 {#suppression-list}

제외 목록은 게재에서 제외하려는 주소 및 도메인으로 구성됩니다. 이러한 연락처로 보내면 전송 평판과 게재 속도가 떨어질 수 있기 때문입니다.

[!DNL Journey Optimizer] 비표시 목록은 고유한 환경 수준(예: 지정된 샌드박스에 대해 관리됨)에서 관리됩니다.

샌드박스 ID와 연관된 조직 ID와 관련된 것을 의미하는 단일 클라이언트 환경의 모든 메일링에서 억제되는 이메일 주소 및 도메인을 수집합니다.

>[!NOTE]
>
>Adobe은 참여 및 메일링 평판에 유해한 것으로 입증된 알려진 잘못된 주소의 업데이트된 목록을 보관하고 이메일이 게재되지 않도록 합니다. 이 목록은 모든 Adobe 고객에게 공통으로 적용되는 글로벌 금지 목록에서 관리됩니다. 글로벌 금지 목록에 포함된 주소와 도메인 이름은 숨겨집니다. 게재 보고서에는 제외된 수신자 수만 표시됩니다.

또한 Journey Optimizer **Suppression REST API**&#x200B;를 활용하면 제외 및 허용 목록을 통해 보내는 메시지를 제어할 수 있습니다. [Suppression REST API 사용 방법 알아보기](https://developer.adobe.com/journey-optimizer-apis/references/suppression/){target="_blank"}

## 제외 목록이 필요한 이유 {#why-suppression-list}

받은 편지함 소유자가 받는 이메일 메시지를 제어하고 원하는 메시지만 받도록 보장하기 위해 인터넷 서비스 공급자(ISP) 및 상업용 스팸 필터는 사용 중인 IP 주소 및 전송 도메인을 기반으로 이메일 보낸 사람의 전체 평판을 추적하는 자체 독점 알고리즘을 갖습니다.

피드백(스팸 불만, 바운스 등)을 받지 않는 경우 고려해보면, 그들은 당신의 평판을 떨어뜨릴 것이다. 제외 목록은 ISP의 피드백을 반영하는 데 도움이 됩니다.

이메일 주소가 억제된 수신자는 메시지 게재에서 자동으로 제외됩니다. 이를 통해 게재 속도를 높일 수 있습니다. 오류율은 게재 속도에 상당한 영향을 미치기 때문입니다.

## 금지 목록에 뭐가 있어? {#what-s-on-suppression-list}

주소는 다음과 같이 제외 목록에 추가됩니다.

* 모든 **하드 바운스** 및 **스팸 불만**&#x200B;은(는) 한 번 발생한 후에 해당 주소를 제외 목록에 자동으로 보냅니다. [이 섹션](#spam-complaints)에서 스팸 불만 사항에 대해 자세히 알아보세요.

* **소프트 바운스**&#x200B;는 주소를 제외 목록에 즉시 보내지 않지만 오류 카운터를 증가시킵니다. 그런 다음 여러 [다시 시도](../configuration/retries.md)를 수행하고 오류 카운터가 임계값에 도달하면 주소가 제외 목록에 추가됩니다.

* 주소 또는 도메인을 [**수동으로**](../configuration/manage-suppression-list.md#add-addresses-and-domains)할 수도 있습니다.

[이 섹션](#delivery-failures)에서 하드 바운스 및 소프트 바운스에 대해 자세히 알아보세요.

>[!NOTE]
>
>[!DNL Journey Optimizer]에서 전자 메일을 받지 않으므로 구독 취소된 사용자의 주소를 제외 목록으로 보낼 수 없습니다. 이러한 선택은 Experience Platform 수준에서 처리됩니다. [옵트아웃](../privacy/opt-out.md)에 대해 자세히 알아보세요.

각 주소에 대해 제외되는 기본 이유와 제외 범주(소프트, 하드 등) 제외 목록에 표시됩니다. [이 섹션](../configuration/manage-suppression-list.md)에서 제외 목록에 액세스하고 관리하는 방법에 대해 자세히 알아보세요.

>[!NOTE]
>
>메시지 전송 프로세스 중에 **[!UICONTROL 제외됨]** 상태의 프로필은 제외됩니다. 따라서 **여정 보고서**&#x200B;에는 이러한 프로필이 여정([대상자 읽기](../building-journeys/read-audience.md) 및 [메시지 활동](../building-journeys/journeys-message.md))을 통해 이동한 것으로 표시되지만, 전자 메일을 보내기 전에 필터링되므로 **전자 메일 보고서**&#x200B;에는 이러한 프로필이 **[!UICONTROL 전송됨]** 지표에 포함되지 않습니다.
>
>[실시간 보고서](../reports/live-report.md) 및 [글로벌 보고서](../reports/global-report.md)에 대해 자세히 알아보세요. 모든 제외 사례에 대한 이유를 알아보려면 [Adobe Experience Platform 쿼리 서비스](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target="_blank"}를 사용할 수 있습니다.

### 게재 실패 {#delivery-failures}

게재가 실패할 경우 두 가지 유형의 오류가 있습니다.

* **하드 바운스**. 하드 바운스는 잘못된 이메일 주소(즉, 존재하지 않는 이메일 주소)를 나타냅니다. 여기에는 주소가 유효하지 않다는 것을 명시적으로 설명하는 수신 이메일 서버의 바운스 메시지가 포함됩니다.
* **소프트 바운스**. 유효한 이메일 주소에 대해 발생한 임시 이메일 바운스입니다.

**하드 바운스**&#x200B;는 메일 주소를 제외 목록에 자동으로 추가합니다.

너무 많이 발생하는 **소프트 바운스** <!--or an **ignored** error-->도 여러 번 다시 시도한 후 비표시 목록으로 전자 메일 주소를 보냅니다. [다시 시도에 대해 자세히 알아보기](../configuration/retries.md)

이러한 주소로 계속 전송하는 경우 이메일 주소 목록 유지 관리 모범 사례를 따르지 않을 수 있으므로 신뢰할 수 없는 발신자일 수 있음을 ISP에 알려 주기 때문에 전송 속도에 영향을 줄 수 있습니다.

### 스팸 고객 불만 {#spam-complaints}

제외 목록은 메시지를 스팸으로 표시하는 이메일 주소를 수집합니다. 예를 들어, 누군가가 고객 서비스에 귀하로부터 메일을 다시 받지 않도록 요청하는 메시지를 보내는 경우, 해당 사용자의 이메일 주소는 인스턴스 전체에 표시되지 않으며, 해당 주소로 더 이상 배달할 수 없습니다.

스팸 불만을 제출한 후 수신자에게 보내는 것은 ISP에 원치 않는 이메일을 보내고 수신자의 의견을 듣지 않을 수 있음을 알려 주기 때문에 전송 평판에 큰 영향을 미칠 수 있습니다.

이로 인해 IP 주소 또는 전송 도메인이 차단될 수 있으며, 이러한 주소는 제외 목록에 있으므로 방지할 수 있습니다.

일부 ISP에서는 이메일을 받은 사용자가 이메일을 스팸으로 표시하기로 선택하면 이메일 발신자에게 자동으로 알림을 보낼 수 있는 피드백 루프(FBL)를 제공합니다. [자세히 알아보기](deliverability.md#feedback-loops)
