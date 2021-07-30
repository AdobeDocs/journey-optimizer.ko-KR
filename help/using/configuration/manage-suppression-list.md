---
title: 제외 목록 관리
description: 'Journey Optimizer 제외 목록에 액세스하고 관리하는 방법을 알아봅니다 '
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
feature: 애플리케이션 설정
topic: 관리
role: Admin
level: Intermediate
source-git-commit: 83d0cbdb7524f0317bd576ed7c689f9933bb658f
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 2%

---


# 제외 목록 관리 {#manage-suppression-list}

[!DNL Journey Optimizer] 을 사용하면 다음과 같이 여정에서 전송에서 자동으로 제외된 모든 이메일 주소를 모니터링할 수 있습니다.

* 잘못된 주소(하드 바운스) 또는 일관된 소프트 바운스(소프트 바운스)이며, 게재 시 계속 해당 주소를 포함하는 경우 이메일 평판에 부정적인 영향을 줄 수 있는 주소입니다.
* 이메일 메시지 중 하나에 대해 일종의 스팸 불만 사항을 발행한 수신자입니다.

<!--Profiles who unsubscribe from your sendings. Learn more on [opting-out](../consent.md). NOT TRUE as confirmed by eng.: "Subscribe and Unsubscribe are handled by the Consent/Subscription service. A user that opts out will not make it to the suppression list – we won’t send them emails."-->

이러한 이메일 주소는 Journey Optimizer **제외 목록**&#x200B;에 자동으로 수집됩니다. 자세한 내용은 [이 섹션](../suppression-list.md)을 참조하십시오.

## 제외 목록에 액세스합니다 {#access-suppression-list}

제외된 이메일 주소의 세부 목록에 액세스하려면 **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL General]** 메뉴를 연 다음 **[!UICONTROL View suppression lists]** 링크를 클릭합니다.

![](../assets/suppression-list-link.png)

필터를 사용하여 목록을 탐색할 수 있습니다.

![](../assets/suppression-list-filters.png)

<!--suppression date,  category and reason, but on staging, only creation date filter is available-->

<!--You can also download the list as a CSV file for analysis and reporting purpose. Won't be available.-->

## 제외 카테고리 및 이유 {#suppression-categories-and-reasons}

메시지가 이메일 주소로 배달되지 않으면 Journey Optimizer은 게재가 실패한 이유를 파악하고 제외 카테고리와 연결합니다.

억제 카테고리는 다음과 같습니다.

* **하드**: 이메일 주소가 즉시 제외 목록으로 전송됩니다.

* **소프트**: 소프트 오류의 경우 오류 카운터가 제한 임계값에 도달하면 제외 목록에 주소를 보냅니다. [다시 시도하는 방법에 대해 자세히 알아보기](retries.md)

* **무시됨**:
   * 유효한 전자 메일 주소에 대해 오류가 발생했지만 실패한 연결 시도 또는 임시 기술 문제 등 일시적인 것으로 알려진 경우 오류 카운터가 제한 임계값에 도달하면 전자 메일 주소가 제외 목록에 추가됩니다. [다시 시도하는 방법에 대해 자세히 알아보십시오](retries.md).
   * 스팸 메일의 결과로 오류가 발생하면 불만 사항을 발행한 수신자의 이메일 주소가 즉시 억제 목록에 전송됩니다.

<!--**Manual**: You can also manually add an email address to the suppression list. => Manual category will be available when manually adding an address to the suppression list (via API)-->

>[!NOTE]
>
>[게재 실패 유형](../suppression-list.md#delivery-failures) 섹션의 소프트 바운스 및 하드 바운스에 대해 자세히 알아보십시오.

나열된 각 이메일 주소에 대해 **[!UICONTROL Reason]** 을 제외하는지, 제외 목록에 추가된 날짜/시간을 확인할 수도 있습니다.

![](../assets/suppression-list-temp.png)
<!--to replace with suppression-list.png when Manual category is available (through API)-->

게재 실패 이유는 다음과 같습니다.

| 이유 | 설명 | 제외 카테고리 |
---------|----------|--------- |
| **[!UICONTROL Undetermined]** | 받는 사람 도메인 MTA(메시지 전송 에이전트)로부터 받은 바운스 이유를 식별할 수 없습니다. | 무시됨 |
| **[!UICONTROL Invalid Recipient]** | 수신자가 잘못되었거나 없습니다. | 하드 |
| **[!UICONTROL Soft Bounce]** | 메시지가 소프트 바운스되어, ISP에서 권장하는 허용 비율을 전송할 때와 같이 이 표에 나열된 소프트 오류 이외의 다른 이유로 바운스됩니다. | 소프트 |
| **[!UICONTROL DNS Failure]** | DNS 오류로 인해 메시지가 반송되었습니다. | 소프트 |
| **[!UICONTROL Mailbox Full]** | 받는 사람의 사서함이 가득 차서 더 이상의 메시지를 받을 수 없어서 메시지가 반송되었습니다. | 소프트 |
| **[!UICONTROL Too Large]** | 수신자에게 너무 커서 메시지가 반송 되었습니다. [](retries.md) 검색이 수행됩니다. 메시지 크기를 편집하고 게재하기 위해 다시 삽입할 수 있습니다. | 무시됨 |
| **[!UICONTROL Timeout]** | 메시지 시간이 초과되었습니다. 즉, 소프트 바운스되어 메시지 다시 시도 제한(3.5일)에 도달했습니다. | 무시됨 |
| **[!UICONTROL Admin Failure]** | 전송 시스템 관리자가 구성한 정책에 따라 메시지가 실패했습니다. <!--For example, if emails are blackholed at the global, domain or binding level using the "blackhole" directive, this bounce code is used.--> | 무시됨 |
| **[!UICONTROL Generic Bounce: No RCPT]** | 메시지에 대한 수신자를 확인할 수 없습니다. | 무시됨 |
| **[!UICONTROL Generic Bounce]** | 메시지가 지정되지 않은 이유로 실패했습니다. | 무시됨 |
| **[!UICONTROL Mail Block]** | 받는 사람(즉, 받는 사람 MTA)이 메시지를 차단했습니다. | 무시됨 |
| **[!UICONTROL Spam Block]** | 스팸 메일로부터 온 것으로 수신자가 메시지를 차단했습니다. 예를 들어 전송 IP 블록일 수 있습니다. | 무시됨 |
| **[!UICONTROL Spam Content]** | 메시지 콘텐츠가 받는 사람(수신자 MTA)에 의해 스팸으로 차단되었습니다. | 무시됨 |
| **[!UICONTROL Prohibited Attachment]** | 메시지가 첨부 파일이 포함되어 있어서 수신기에 의해 차단되었습니다. | 무시됨 |
| **[!UICONTROL Relaying Denied]** | 릴레이가 허용되지 않아 수신자가 메시지를 차단했습니다. | 소프트 |
| **[!UICONTROL Auto-Reply]** | 이 메시지는 자동 회신/휴가 우편입니다. | 무시됨 |
| **[!UICONTROL Transient Failure]** | 메시지 전송이 일시적으로 지연되었습니다. | 무시됨 |
| **[!UICONTROL Challenge-Response]** | 이 메시지는 Challenge-Response Probe입니다. | 소프트 |

>[!NOTE]
>
>구독하지 않은 사용자가 [!DNL Journey Optimizer]에서 이메일을 받지 않으므로 해당 이메일 주소를 제외 목록으로 보낼 수 없습니다. 선택 사항은 Experience Platform 수준에서 처리됩니다. [옵트아웃](../consent.md)에 대해 자세히 알아보십시오.

<!--
Removed from the table provided by SparkPost/Momentum:
| **[!UICONTROL Subscribe]** | The message is a subscribe request. | Ignored |
| **[!UICONTROL Unsubscribe]** | The message is an unsubscribe request. | Hard |
-->

<!--Note to add eventually: If a user is subscribed and [!DNL Journey Optimizer] fails to send emails to their subscribed email address, they will get added to the suppression list. (not sure it's possible to subscribe through AJO or need to find reference to Experience Platform doc?)-->


