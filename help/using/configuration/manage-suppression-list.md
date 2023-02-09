---
solution: Journey Optimizer
product: journey optimizer
title: 제외 목록 관리
description: Journey Optimizer 제외 목록에 액세스하고 관리하는 방법을 알아봅니다
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: 억제, 목록, 바운스, 이메일, 최적기, 격리
exl-id: 430a2cd4-781d-4d37-a75d-405f5ed82377
source-git-commit: 2a3bb638ff3485b6c74d92d64126b3b5fd2925e6
workflow-type: tm+mt
source-wordcount: '1488'
ht-degree: 0%

---

# 제외 목록 관리 {#manage-suppression-list}

사용 [!DNL Journey Optimizer]를 사용하면 하드 바운스, 소프트 바운스 수 및 스팸 불만 등과 같이 여정 또는 캠페인에서 자동으로 전송되지 않는 모든 이메일 주소를 모니터링할 수 있습니다.

이러한 이메일 주소는 Journey Optimizer에 자동으로 수집됩니다 **제외 목록**. 제외 목록은 대상에서 제외할 주소 및 도메인으로 구성됩니다. 여기에는 샌드박스 ID와 연결된 조직 ID를 의미하는 단일 클라이언트 환경의 모든 메일링 간에 표시되지 않는 이메일 주소와 도메인이 수집됩니다.

에서 억제 목록 개념 및 사용에 대해 자세히 알아보십시오 [이 섹션](../reports/suppression-list.md).



## 제외 목록에 액세스합니다 {#access-suppression-list}

제외된 이메일 주소 및 도메인의 세부 목록에 액세스하려면 다음 위치로 이동하십시오 **[!UICONTROL 관리]** > **[!UICONTROL 채널]** > **[!UICONTROL 이메일 구성]**, 을(를) 선택하고 을(를) 선택합니다. **[!UICONTROL 제외 목록]**.


![](assets/suppression-list-access.png)

>[!CAUTION]
>
>제외 목록을 보고, 내보내고 관리할 수 있는 권한은 다음으로 제한됩니다 [여정 관리자](../administration/ootb-product-profiles.md#journey-administrator). 관리에 대해 자세히 알아보기 [!DNL Journey Optimizer] 사용자 액세스 권한 [이 섹션](../administration/permissions-overview.md).


필터를 사용하여 목록을 탐색할 수 있습니다.

![](assets/suppression-list-filters.png)

을(를) **[!UICONTROL 제외 카테고리]**, **[!UICONTROL 주소 유형]**, 또는 **[!UICONTROL 이유]**. 각 기준에 대해 하나 이상의 옵션을 선택합니다. 선택하면 각 필터 또는 목록 맨 위에 표시된 모든 필터를 지울 수 있습니다.

![](assets/suppression-list-filtering-example.png)


## 실패 이유 이해 {#suppression-categories-and-reasons}

메시지가 이메일 주소로 배달되지 않으면 [!DNL Journey Optimizer] 게재가 실패한 이유를 확인하고 **[!UICONTROL 제외 카테고리]**.

억제 카테고리는 다음과 같습니다.

* **하드**: 하드 바운스는 잘못된 이메일 주소(즉, 존재하지 않는 이메일 주소)를 나타냅니다. 여기에는 주소가 유효하지 않다고 명시적으로 설명하는 수신 이메일 서버의 바운스 메시지가 포함됩니다. 이메일 주소가 즉시 제외 목록으로 전송됩니다.

   스팸메일 신고로 인한 오류일 경우 스팸메일 신고도 해당된다 **하드** 카테고리. 불만을 발행한 수신자의 이메일 주소가 즉시 억제 목록으로 전송됩니다.

* **소프트**: 소프트 바운스는 유효한 이메일 주소에 대해 발생한 임시 이메일 바운스입니다. 여러 번 다시 시도한 후 이메일 주소가 제외 목록에 추가됩니다. 소프트 오류의 경우 오류 카운터가 제한 임계값에 도달하면 제외 목록에 주소를 보냅니다. [다시 시도하는 방법에 대해 자세히 알아보기](retries.md)

* **수동**: 수동 오류가 제외 목록에 수동으로 추가되었습니다. [자세히 알아보기](#add-addresses-and-domains)

나열된 각 이메일 주소에 대해 다음을 확인할 수도 있습니다 **[!UICONTROL 유형]** (이메일 또는 도메인), **[!UICONTROL 이유]** 제외하기 위해 추가한 사람과 제외 목록에 추가한 날짜/시간입니다.

![](assets/suppression-list.png)

게재 실패 이유는 다음과 같습니다.

| 이유 | 설명 | 카테고리 |
| --- | --- | --- |
| **[!UICONTROL 잘못된 받는 사람]** | 수신자가 잘못되었거나 없습니다. | 하드 |
| **[!UICONTROL 소프트 바운스]** | 메시지가 소프트 바운스되어, ISP에서 권장하는 허용 비율을 전송할 때와 같이 이 표에 나열된 소프트 오류 이외의 다른 이유로 바운스됩니다. | 소프트 |
| **[!UICONTROL DNS 실패]** | DNS 오류로 인해 메시지가 반송되었습니다. | 소프트 |
| **[!UICONTROL 사서함 가득 참]** | 받는 사람의 사서함이 가득 차서 더 이상의 메시지를 받을 수 없어서 메시지가 반송되었습니다. | 소프트 |
| **[!UICONTROL 연결 거부]** | 릴레이가 허용되지 않아 수신자가 메시지를 차단했습니다. | 소프트 |
| **[!UICONTROL Challenge-Response]** | 이 메시지는 Challenge-Response Probe입니다. | 소프트 |
| **[!UICONTROL 스팸 불만]** | 받는 사람이 스팸으로 표시했기 때문에 메시지가 차단되었습니다. | 하드 |

>[!NOTE]
>
>구독하지 않은 사용자가 보낸 이메일을 받지 않습니다. [!DNL Journey Optimizer]따라서 해당 이메일 주소를 제외 목록으로 보낼 수 없습니다. 선택 사항은 Experience Platform 수준에서 처리됩니다. [옵트아웃에 대해 자세히 알아보기](../privacy/opt-out.md)


### 제외 규칙  {#suppression-rules}

에서 **[!UICONTROL 제외 목록]** 보기에서 제외 규칙과 연결된 다시 시도 매개 변수를 편집할 수도 있습니다 **[!UICONTROL 제외 규칙 편집]** 버튼을 클릭합니다. 이 옵션을 사용하여 현재 샌드박스의 재시도 임계값을 업데이트합니다. [다시 시도하는 방법에 대해 자세히 알아보기](retries.md).


## 제외 목록에 주소 및 도메인 추가{#add-addresses-and-domains}

>[!CONTEXTUALHELP]
>id="ajo_admin_suppression_list_header"
>title="제외 목록에 전자 메일 또는 도메인 추가"
>abstract="전송에서 특정 이메일 주소 및/또는 도메인을 제외하려면 Journey Optimizer 제외 목록을 수동으로 채울 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_admin_suppression_list"
>title="제외 목록에 전자 메일 또는 도메인 추가"
>abstract="제외 목록을 채우려면 이메일 주소 또는 도메인을 수동으로 추가할 수 있습니다. 한 번에 하나씩 또는 CSV 파일 업로드를 통해 벌크 모드에서 수행할 수 있습니다. 이러한 특정 이메일 주소 및/또는 도메인은 전송에서 제외됩니다."

메시지를 전자 메일 주소에 배달하지 못하면 이 주소가 정의된 제외 규칙 또는 바운스 수를 기반으로 하여 제외 목록에 자동으로 추가됩니다.

그러나 수동으로 [!DNL Journey Optimizer] 전송에서 특정 이메일 주소 및/또는 도메인을 제외하는 제외 목록입니다.

>[!NOTE]
>
>최대 60분 정도 걸릴 수 있습니다 [!DNL Journey Optimizer] 보내는 이메일의 숨겨진 주소를 고려합니다.

이메일 주소 또는 도메인을 추가할 수 있습니다 [한 번에 하나씩](#add-one-address-or-domain), 또는 [일괄 모드에서](#upload-csv-file) 를 사용하십시오.

### 주소 또는 도메인 하나 추가 {#add-one-address-or-domain}

>[!CONTEXTUALHELP]
>id="ajo_admin_suppression_list_address"
>title="한 항목을 제외 목록에 추가합니다"
>abstract="이메일 주소 및/또는 도메인을 하나씩 추가하여 제외 목록을 채울 수 있습니다."

전자 메일 주소 또는 도메인을 제외 목록에 추가하려면 아래 단계를 따르십시오.

1. 을(를) 선택합니다 **[!UICONTROL 이메일 또는 도메인 추가]** 버튼을 클릭합니다.

   ![](assets/suppression-list-add-email.png)

1. 을(를) 선택합니다 **[!UICONTROL 하나씩]** 선택 사항입니다.

   ![](assets/suppression-list-add-email-address.png)

1. 주소 유형을 선택합니다. **[!UICONTROL 이메일]** 또는 **[!UICONTROL 도메인]**.

1. 전송에서 제외할 이메일 주소 또는 도메인을 입력합니다.

   >[!NOTE]
   >
   >올바른 이메일 주소(예: abc@company.com) 또는 도메인(예: abc.company.com)을 입력해야 합니다.

1. (선택 사항) 사유를 입력합니다. 이 필드에는 32~126 사이의 ASCII 인쇄 가능 문자가 모두 포함될 수 있습니다.

1. 를 사용하십시오 **[!UICONTROL 제출]** 확인할 단추입니다.

### CSV 파일 업로드 {#upload-csv-file}

>[!CONTEXTUALHELP]
>id="ajo_admin_suppression_list_csv"
>title="CSV를 업로드하여 제외 목록에 항목 추가"
>abstract="제외할 이메일 주소/도메인으로 채워진 CSV 파일을 업로드하여 제외 목록을 채울 수 있습니다."

전자 메일 주소 그룹 또는 도메인을 제외 목록에 추가하려면 아래 단계를 따르십시오.

1. 을(를) 선택합니다 **[!UICONTROL 이메일 또는 도메인 추가]** 버튼을 클릭합니다.
1. 을(를) 선택합니다 **[!UICONTROL CSV 업로드]** 선택 사항입니다.

   ![](assets/suppression-list-upload-csv.png)

1. 아래 열과 형식을 포함하는 사용할 CSV 템플릿을 다운로드합니다.

   ```
   TYPE,VALUE,COMMENT
   EMAIL,abc@somedomain.com,Comment
   DOMAIN,somedomain.com,Comment
   ```

1. CSV 템플릿을 이메일 주소 및/또는 도메인으로 채워 제외 목록에 추가합니다. 32~126 사이의 ASCII 인쇄 가능 문자는 **댓글** 열.

   >[!CAUTION]
   >
   >CSV 템플릿의 열 이름을 변경하지 마십시오.
   >
   >파일 크기는 1MB를 초과할 수 없습니다.

1. 완료되면 CSV 파일을 끌어다 놓고 을(를) 사용합니다 **[!UICONTROL 제출]** 확인할 단추입니다.

   ![](assets/suppression-list-upload-csv-submit.png)

업로드가 완료되면, [최근 업로드](#recent-uploads) 버튼을 클릭합니다.

### 업로드 상태 확인 {#recent-uploads}

를 사용하십시오 **[!UICONTROL 최근 업로드]** 단추를 클릭하여 업로드된 최신 CSV 파일의 상태를 확인합니다.

![](assets/suppression-list-recent-uploads-button.png)

가능한 상태는 다음과 같습니다.

* **[!UICONTROL 보류 중]**: 파일 업로드가 처리 중입니다.
* **[!UICONTROL 오류]**: 기술 문제 또는 파일 형식 오류로 인해 파일 업로드 프로세스가 실패했습니다.
* **[!UICONTROL 완료]**: 파일 업로드 프로세스가 완료되었습니다.

업로드 중에 일부 주소가 올바른 형식이 아닌 경우, 이 주소가 [!DNL Journey Optimizer] 제외 목록.

이 경우 업로드가 완료되면 보고서와 연결됩니다. 다운로드하여 발생한 오류를 확인할 수 있습니다<!-- and understand why they were not added to the suppression list-->.

![](assets/suppression-list-recent-uploads-report.png)

다음은 오류 보고서에서 찾을 수 있는 항목 유형의 예입니다.

```
type,value,comments,failureReason
Email,examplemail.com,MANUAL,Invalid format for value: examplemail.com
Email,examplemail,MANUAL,Invalid format for value: examplemail
Email,example@mail,MANUAL,Invalid format for value: example@mail
Domain,example,MANUAL,Invalid format for value: example
Domain,example.!com,MANUAL,Invalid format for value: example.!com
Domain,!examplecom,MANUAL,Invalid format for value: !examplecom
```

## 제외 목록에서 주소 제거{#remove-from-suppression-list}

억제 목록을 수동으로 업데이트할 수 있습니다. 격리 시 이메일 주소를 제거하는 것은 중요한 작업이며 IP 신뢰도 및 게재 능력에 영향을 줄 수 있습니다. 주의 깊게 진행하십시오.

제외 목록에서 이메일 주소 또는 도메인을 삭제하면 Adobe Journey Optimizer에서 이 주소 또는 도메인에 다시 배달할 수 있습니다.  에서 게재 기능에 대해 자세히 알아보십시오 [이 섹션](../reports/deliverability.md).

제외 목록에서 주소를 제거하려면 **[!UICONTROL 삭제]** 버튼을 클릭합니다.

![](assets/suppression-list-delete.png)


>[!NOTE]
>
>이메일 주소 또는 도메인 삭제를 고려할 때 추가 주의가 필요합니다. 확실하지 않은 경우 게재 가능성 전문가에게 문의하십시오.

예를 들어, ISP(인터넷 서비스 공급자) 서비스 중단이 발생하면, 이메일은 수신자에게 성공적으로 전달할 수 없기 때문에 하드 바운스로 잘못 표시됩니다. 이러한 이메일 주소는 제외 목록에서 제거해야 합니다.

이러한 주소를 검색하려면 중단 컨텍스트에 따라 사용자 지정 매개 변수로 특정 쿼리를 실행합니다. [이 샘플에서 자세히 알아보기](../data/datasets-query-examples.md#isp-outage-query).

영향을 받는 이메일 주소가 식별되면 제외 목록을 필터링하여 표시합니다. 예를 들어, ISP 중단이 2022년 11월 11일부터 2022년 11월 13일까지 **test.com** 도메인, 아래와 같이 해당 기간의 제외 목록에 추가된 주소를 필터링하십시오.

![](assets/remove-from-supp-list.png)

그런 다음 다음을 사용하여 제외 목록에서 격리된 이메일 주소를 제거할 수 있습니다 **[!UICONTROL 삭제]** 버튼을 클릭합니다.

## 제외 목록 다운로드 {#download-suppression-list}

<!--
>[!CONTEXTUALHELP]
>id="ajo_admin_suppression_list_download"
>title="Export the list as a CSV file"
>abstract="To download the suppression list, Qou can either export the current list by generating a new file, or download the file that was previously generated."
-->

제외 목록을 CSV 파일로 내보내려면 아래 단계를 수행하십시오.

1. 을(를) 선택합니다 **[!UICONTROL CSV 다운로드]** 버튼을 클릭합니다.

   ![](assets/suppression-list-download-csv.png)

1. 파일이 생성될 때까지 기다립니다.

   ![](assets/suppression-list-download-generate.png)

   >[!NOTE]
   >
   >다운로드 시간은 파일 크기에 따라 다릅니다. 즉, 제외 목록에 있는 주소 수입니다.
   >
   >지정된 샌드박스에 대해 한 번에 하나의 다운로드 요청을 처리할 수 있습니다.

1. 파일이 생성되면 알림을 받게 됩니다. 화면 오른쪽 위의 벨 아이콘을 클릭하여 표시합니다.

1. 알림 자체를 클릭하여 파일을 다운로드합니다.

   ![](assets/suppression-list-download-notification.png)

   >[!NOTE]
   >
   >링크는 24시간 동안 유효합니다.

<!--When downloading the CSV file, you can choose to either:

* Download the file that was previously generated by another user or yourself.

* Generate a new file in order to export the current suppression list.-->