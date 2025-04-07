---
solution: Journey Optimizer
product: journey optimizer
title: PTR 기록
description: PTR 레코드 관리 방법 알아보기
feature: Subdomains, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: 하위 도메인, PTR, 레코드, DNS, 도메인, 메일
exl-id: 4c930792-0677-4ad5-a46c-8d40fc3c4d3a
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 9%

---

# PTR 기록 만들기 및 편집 {#ptr-records}

>[!CONTEXTUALHELP]
>id="ajo_admin_ptr_record"
>title="하위 도메인의 PTR 기록"
>abstract="포인터 레코드(PTR)는 IP 주소에 연결된 도메인 이름을 제공하는 DNS 레코드 유형으로 수신 메일 서버가 발신자의 IP 주소를 확인하는 데 도움을 줍니다. 전달성 전문가의 심사와 충분한 논의를 거친 후에만 PTR 기록을 편집합니다."

>[!CONTEXTUALHELP]
>id="ajo_admin_ptr_record_header"
>title="하위 도메인의 PTR 기록"
>abstract="Journey Optimizer에서 첫 번째 하위 도메인이 Adobe에 위임되면 PTR 기록이 자동으로 생성됩니다."

## PTR 레코드 기본 정보 {#about-ptr-records}

PTR(포인터 레코드)은 IP 주소에 연결된 도메인 이름을 제공하는 DNS(Domain Name System) 레코드 유형입니다.

PTR 기록을 사용하여 수신 메일 서버는 해당 IP 주소가 서버가 연결하는 이름과 일치하는지 식별하여 전송 메일 서버의 신뢰성을 확인할 수 있습니다.

## 하위 도메인의 PTR 레코드 액세스 {#access-ptr-records}

[!DNL Journey Optimizer]에서 첫 번째 하위 도메인을 Adobe에 [위임](delegate-subdomain.md)하면 IP에 대한 PTR 레코드가 자동으로 만들어집니다. **[!UICONTROL 관리]** > **[!UICONTROL 채널]** > **[!UICONTROL 전자 메일 설정]** > **[!UICONTROL PTR 레코드]** 메뉴에서 액세스할 수 있습니다.

![](assets/ptr-records.png)

이 목록에는 아래 구문을 사용하여 생성된 PTR 기록이 표시됩니다.

* &quot;r&quot; for record,
* IP 주소의 마지막 두 숫자에 대해 &quot;xx&quot;
* 하위 도메인 이름.

목록에서 PTR 레코드를 열어 연결된 하위 도메인 이름 및 IP 주소를 표시할 수 있습니다.

## PTR 기록 편집 {#edit-ptr-record}

[!DNL Journey Optimizer]에서 PTR 레코드를 수동으로 만들 수 없습니다. 대신 첫 번째 하위 도메인을 Adobe에 [위임](delegate-subdomain.md)하면 IP에 대한 PTR 레코드가 자동으로 만들어집니다.

각 IP는 단일 PTR 레코드를 수신합니다. 모든 PTR 레코드의 형식은 &#39;rxx.subdomain&#39;입니다. 여기서 &#39;subdomain&#39;은 [!DNL Journey Optimizer]에서 위임한 첫 번째 하위 도메인입니다.

추가 하위 도메인을 만들 때 하나 이상의 PTR 레코드를 수정하고 새 하위 도메인을 할당해야 합니다. 그 방법은 다음과 같습니다.

>[!CAUTION]
>
>PTR 레코드는 모든 환경에 대해 공통입니다. 따라서 PTR 레코드를 수정하면 프로덕션 샌드박스에도 영향을 미칩니다.
>
>PTR 레코드를 편집할 때 각별히 주의하십시오. 의심이 가는 경우 게재 가능성 전문가에게 문의하십시오.

### 완전히 위임된 하위 도메인 {#fully-delegated-subdomains}

Adobe에 [완전히 위임](delegate-subdomain.md#full-subdomain-delegation)된 하위 도메인으로 PTR 레코드를 편집하려면 아래 단계를 따르십시오.

1. 목록에서 PTR 레코드 이름을 클릭하여 엽니다.

   ![](assets/ptr-record-select.png)

1. 목록에서 Adobe에 [완전히 위임됨](delegate-subdomain.md#full-subdomain-delegation) 하위 도메인을 선택하십시오.

   ![](assets/ptr-record-subdomain.png)

1. 변경 내용을 확인하려면 **[!UICONTROL 저장]**&#x200B;을 클릭하세요.

>[!NOTE]
>
>**[!UICONTROL IP]** 및 **[!UICONTROL PTR 레코드]** 필드를 수정할 수 없습니다.

### CNAME 메서드를 사용하는 위임된 하위 도메인 {#edit-ptr-subdomains-cname}

[CNAME 메서드](delegate-subdomain.md#cname-subdomain-delegation)를 사용하여 Adobe에 위임된 하위 도메인으로 PTR 레코드를 편집하려면 아래 단계를 따르십시오.

1. 목록에서 PTR 레코드 이름을 클릭하여 엽니다.

   ![](assets/ptr-record-select.png)

1. 목록에서 [CNAME 메서드](delegate-subdomain.md#cname-subdomain-delegation)를 사용하여 Adobe으로 위임된 하위 도메인을 선택하십시오.

   ![](assets/ptr-record-subdomain-cname.png)

1. 호스팅 플랫폼에서 새로운 순방향 DNS 레코드를 생성해야 합니다. 이렇게 하려면 Adobe에서 생성한 레코드를 복사합니다. 완료되면 &quot;확인...&quot; 상자를 선택합니다.

   ![](assets/ptr-record-subdomain-confirm.png)

   >[!NOTE]
   >
   >&quot;먼저 순방향 DNS를 만든 다음 다시 시도하십시오&quot;라는 메시지가 표시되면 아래 단계를 따르십시오.
   >   * 순방향 DNS 레코드가 성공적으로 생성되었는지 DNS 공급자를 확인합니다.
   >   * DNS의 레코드는 즉시 동기화되지 않을 수 있습니다. 몇 분 정도 기다린 후 다시 시도하십시오.

1. 변경 내용을 확인하려면 **[!UICONTROL 저장]**&#x200B;을 클릭하세요.

>[!NOTE]
>
>**[!UICONTROL IP]** 및 **[!UICONTROL PTR 레코드]** 필드를 수정할 수 없습니다.

## PTR 기록 업데이트 세부 정보 확인 {#check-ptr-record-update}

PTR 레코드 편집을 확인하면 목록의 PTR 레코드 이름 옆에 **[!UICONTROL 처리 중]** 아이콘이 표시됩니다.

![](assets/ptr-record-updating.png)

>[!NOTE]
>
>[업데이트 처리](#processing)에는 최대 3시간이 걸릴 수 있습니다.

PTR 기록 업데이트 세부 정보를 확인하려면 옆에 있는 아이콘을 클릭합니다. [이 섹션](#ptr-record-update-statuses)의 다른 아이콘과 관련된 상태에 대해 자세히 알아보세요.

![](assets/ptr-record-recent-update.png)

업데이트 상태 및 요청된 변경 사항과 같은 정보를 볼 수 있습니다.

![](assets/ptr-record-updates.png)

## PTR 기록 업데이트 상태 {#ptr-record-update-statuses}

PTR 레코드 업데이트는 다음 상태를 가질 수 있습니다.

* ![](assets/do-not-localize/ptr-record-processing.png) **[!UICONTROL 처리 중]**: PTR 레코드 업데이트가 제출되었으며 확인 프로세스를 진행 중입니다.
* ![](assets/do-not-localize/ptr-record-success.png) **[!UICONTROL 성공]**: 업데이트된 PTR 레코드가 확인되었으며 새 하위 도메인이 이제 IP 주소와 연결됩니다.
* ![](assets/do-not-localize/ptr-record-failed.png) **[!UICONTROL 실패]**: PTR 레코드 업데이트 확인 중 하나 이상의 검사에 실패했습니다.

### 처리 중 {#processing}

IP 주소와 연결할 새 하위 도메인이 유효한지 확인하기 위해 몇 가지 게재 가능성 검사를 수행합니다. 최대 3시간 정도 소요될 수 있습니다.

>[!NOTE]
>
>업데이트가 진행되는 동안에는 PTR 레코드를 수정할 수 없습니다. 해당 이름을 계속 클릭할 수 있지만 **[!UICONTROL 하위 도메인]** 필드가 회색으로 표시됩니다. 업데이트에 성공할 때까지 변경 사항이 반영되지 않습니다.

유효성 검사 프로세스 중에 이전 하위 도메인은 여전히 IP 주소와 연결되어 있습니다.

### 성공 {#success}

유효성 검사 프로세스가 성공하면 새 하위 도메인이 자동으로 IP 주소와 연결됩니다.

### 실패 {#failes}

유효성 검사 프로세스가 실패하면 이전 PTR 레코드가 표시됩니다. 이전에 IP 주소와 연결된 유효한 하위 도메인은 변경되지 않습니다.

가능한 업데이트 오류 유형은 다음과 같습니다.
* PTR 레코드에 대한 새 순방향 DNS를 만들지 못했습니다.
* 레코드 업데이트 실패
* 관심도를 다시 온보딩하지 못함

업데이트 실패 시 PTR 기록을 다시 편집할 수 있게 됩니다. 이름을 클릭하고 하위 도메인을 다시 업데이트할 수 있습니다.
