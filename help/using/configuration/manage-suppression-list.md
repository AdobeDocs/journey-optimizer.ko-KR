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
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
source-git-commit: 50c3dfe4f756e7c6e8f210dc9d3f615965c3a053
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 2%

---


# 제외 목록 관리 {#manage-suppression-list}

[!DNL Journey Optimizer] 을 사용하면 다음과 같이 여정에서 전송에서 자동으로 제외된 모든 이메일 주소를 모니터링할 수 있습니다.

* 잘못된 주소(하드 바운스).
* 게재를 계속 포함하는 경우 일관되게 소프트 바운스, 그리고 이메일 평판에 부정적인 영향을 줄 수 있는 주소를 제공합니다.
* 이메일 메시지 중 하나에 대해 일종의 스팸 불만 사항을 발행한 수신자입니다.

이러한 이메일 주소는 Journey Optimizer **제외 목록**&#x200B;에 자동으로 수집됩니다. 자세한 내용은 [이 섹션](../suppression-list.md)을 참조하십시오.

## 제외 목록에 액세스합니다 {#access-suppression-list}

제외된 이메일 주소의 세부 목록에 액세스하려면 **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL General]** 메뉴를 연 다음 **[!UICONTROL View suppression lists]** 링크를 클릭합니다.

![](../assets/suppression-list-link.png)

<!--To access the detailed list of excluded email addresses, go to **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]**, and select **[!UICONTROL Suppression list]**.
You can also display the suppression list content using the **[!UICONTROL View suppression list]** link through the **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL General]** menu, but this view does not allow you to edit the list.

![](../assets/suppression-list-access-temp.png)-->

필터를 사용하여 목록을 탐색할 수 있습니다.

![](../assets/suppression-list-filters-temp.png)

<!--![](../assets/suppression-list-filters.png)

You can filter on the **[!UICONTROL Suppression category]**, **[!UICONTROL Address type]**, or **[!UICONTROL Reason]**. Select the option(s) of your choice for each criterion.

![](../assets/suppression-list-filtering-example.png)

Once selected, you can clear each filter or all filters displayed on top of the list.-->

## 제외 카테고리 및 이유 {#suppression-categories-and-reasons}

메시지가 이메일 주소로 배달되지 않으면 [!DNL Journey Optimizer] 은 게재가 실패한 이유를 결정하고 **[!UICONTROL Suppression category]**&#x200B;에 연결합니다.

억제 카테고리는 다음과 같습니다.

* **하드**: 이메일 주소가 즉시 제외 목록으로 전송됩니다.

   >[!NOTE]
   >
   >스팸 메일의 결과로 오류가 발생하면 **Hard** 카테고리도 해당됩니다. 불만을 발행한 수신자의 이메일 주소가 즉시 억제 목록으로 전송됩니다.

* **소프트**: 소프트 오류의 경우 오류 카운터가 제한 임계값에 도달하면 제외 목록에 주소를 보냅니다. [다시 시도하는 방법에 대해 자세히 알아보기](retries.md)

   <!--
    **Ignored**:
    * When the error occurred for a valid email address but is known to be temporary, such as a failed connection attempt or a temporary technical issue, the email address is added to the suppression list once the error counter reaches the limit threshold. [Learn more on retries](retries.md).
    * When the error is the result of a spam complaint, the email address of the recipient who issued the complaint is immediately sent to the suppression list.
    -->

* **수동**: 이메일 주소 또는 도메인을 수동으로 제외 목록에 추가할 수도 있습니다. [자세히 알아보기](#add-addresses-and-domains)

>[!NOTE]
>
>[게재 실패 유형](../suppression-list.md#delivery-failures) 섹션의 소프트 바운스 및 하드 바운스에 대해 자세히 알아보십시오.

나열된 각 이메일 주소에 대해 **[!UICONTROL Type]**(전자 메일 또는 도메인), **[!UICONTROL Reason]** 을 제외하고 추가한 사람 및 제외 목록에 추가한 날짜/시간을 확인할 수도 있습니다.

<!--![](../assets/suppression-list.png)-->

게재 실패 이유는 다음과 같습니다.

| 이유 | 설명 | 제외 카테고리 |
| --- | --- | --- |
| **[!UICONTROL Invalid Recipient]** | 수신자가 잘못되었거나 없습니다. | 하드 |
| **[!UICONTROL Soft Bounce]** | 메시지가 소프트 바운스되어, ISP에서 권장하는 허용 비율을 전송할 때와 같이 이 표에 나열된 소프트 오류 이외의 다른 이유로 바운스됩니다. | 소프트 |
| **[!UICONTROL DNS Failure]** | DNS 오류로 인해 메시지가 반송되었습니다. | 소프트 |
| **[!UICONTROL Mailbox Full]** | 받는 사람의 사서함이 가득 차서 더 이상의 메시지를 받을 수 없어서 메시지가 반송되었습니다. | 소프트 |
| **[!UICONTROL Relaying Denied]** | 릴레이가 허용되지 않아 수신자가 메시지를 차단했습니다. | 소프트 |
| **[!UICONTROL Challenge-Response]** | 이 메시지는 Challenge-Response Probe입니다. | 소프트 |

>[!NOTE]
>
>구독하지 않은 사용자가 [!DNL Journey Optimizer]에서 이메일을 받지 않으므로 해당 이메일 주소를 제외 목록으로 보낼 수 없습니다. 선택 사항은 Experience Platform 수준에서 처리됩니다. [옵트아웃](../consent.md)에 대해 자세히 알아보십시오.

<!--
Removed from the table provided by SparkPost/Momentum:
| **[!UICONTROL Undetermined]** | The bounce reason received from the recipient domain Message Transfer Agent (MTA) could not be identified. | Ignored |
| **[!UICONTROL Too Large]** | The message bounced because it was too large for the recipient. [Retries](retries.md) will be performed: you can edit the message size and re-inject it for delivery. | Ignored |
| **[!UICONTROL Timeout]** | The message timed out, meaning it soft bounced and reached the message retry limit (3.5 days). | Ignored |
| **[!UICONTROL Admin Failure]** | The message was failed according to the policies configured by the sending system administrator. ///For example, if emails are blackholed at the global, domain or binding level using the "blackhole" directive, this bounce code is used. | Ignored |
| **[!UICONTROL Generic Bounce: No RCPT]** | No recipient could be determined for the message. | Ignored |
| **[!UICONTROL Generic Bounce]** | The message failed for unspecified reasons. | Ignored |
| **[!UICONTROL Mail Block]** | The message was blocked by the receiver (i.e. recipient MTA). | Ignored |
| **[!UICONTROL Spam Block]** | The message was blocked by the receiver as coming from a known spam source. It could be a sending IP block for example. | Ignored |
| **[!UICONTROL Spam Content]** | The message content was blocked by the receiver (recipient MTA) as spam. | Ignored |
| **[!UICONTROL Prohibited Attachment]** | The message was blocked by the receiver because it contained an attachment. | Ignored |
| **[!UICONTROL Auto-Reply]** | The message is an auto-reply/vacation mail. | Ignored |
| **[!UICONTROL Transient Failure]** | Message transmission has been temporarily delayed. | Ignored |
| **[!UICONTROL Subscribe]** | The message is a subscribe request. | Ignored |
| **[!UICONTROL Unsubscribe]** | The message is an unsubscribe request. | Hard |
-->

<!--Note to add eventually: If a user is subscribed and [!DNL Journey Optimizer] fails to send emails to their subscribed email address, they will get added to the suppression list. (not sure it's possible to subscribe through AJO or need to find reference to Experience Platform doc?)-->

<!--## Manually add addresses and domains {#add-addresses-and-domains}

When a message fails to be delivered to an email address, this address is automatically added to the suppression list based on the defined suppression rule or bounce count.

However, you can also manually populate the [!DNL Journey Optimizer] suppression list to exclude specific email addresses and/or domains from your sending.

You may add email addresses or domains [one at a time](#add-one-address-or-domain), or [in bulk mode](#upload-csv-file) through a CSV file upload.

To do this, select the **[!UICONTROL Add email or domain]** button, then follow one of the methods below.

![](../assets/suppression-list-add-email.png)

### Add one address or domain {#add-one-address-or-domain}

1. Select the **[!UICONTROL One by one]** option.

    ![](../assets/suppression-list-add-email-address.png)

1. Choose the address type: **[!UICONTROL Email address]** or **[!UICONTROL Domain address]**.

1. Enter the email address or domain you want to exclude from your sending.

    >[!NOTE]
    >
    >Make sure you enter a valid email address (such as abc@company) or domain (such as abc.company.com).

1. Specify a reason if needed.

1. Click **[!UICONTROL Submit]**.

### Upload a CSV file {#upload-csv-file}

1. Select the **[!UICONTROL Upload CSV]** option.

    ![](../assets/suppression-list-upload-csv.png)

1. Download the CSV template to use, which includes the columns and format below:

    ```
    TYPE,VALUE,COMMENT
    EMAIL,abc@somedomain.com,Comment
    DOMAIN,somedomain.com,Comment
    ```
    You can also download this template from the **[!UICONTROL Suppression list]** main view.

    >[!CAUTION]
    >
    >Do not change the names of the columns in the CSV template.
    >
    >The file size should not exceed 50 MB.

1. Fill in the CSV template with the email addresses and/or domains you want to add to the suppression list.

1. Once completed, drag and drop your CSV file, then click **[!UICONTROL Upload file]**.

    ![](../assets/suppression-list-upload-file-button.png)

1. Click **[!UICONTROL Submit]**.

### Check recent uploads status {#recent-uploads}

You can check the list of the latest CSV files you uploaded.

To do this, from the **[!UICONTROL Suppression list]** view, click the **[!UICONTROL Recent uploads]** button.

![](../assets/suppression-list-recent-uploads-button.png)

The latest uploads you submitted and their corresponding statuses are displayed.

If an error report is associated with a file, you can download it to check the errors encountered.

![](../assets/suppression-list-recent-uploads-error.png)

Below is an example of the type of entries you can find in the error report:

```
type,value,comments,failureReason
Email,examplemail.com,MANUAL,Invalid format for value: examplemail.com
Email,examplemail,MANUAL,Invalid format for value: examplemail
Email,example@mail,MANUAL,Invalid format for value: example@mail
Domain,example,MANUAL,Invalid format for value: example
Domain,example.!com,MANUAL,Invalid format for value: example.!com
Domain,!examplecom,MANUAL,Invalid format for value: !examplecom
```

-->


