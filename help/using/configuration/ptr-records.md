---
solution: Journey Optimizer
product: journey optimizer
title: PTR 레코드
description: PTR 레코드를 관리하는 방법 알아보기
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: 하위 도메인, PTR, 레코드, DNS, 도메인, 메일
exl-id: 4c930792-0677-4ad5-a46c-8d40fc3c4d3a
source-git-commit: b8065a68ed73102cb2c9da2c2d2675ce8e5fbaad
workflow-type: tm+mt
source-wordcount: '785'
ht-degree: 9%

---

# PTR 레코드 {#ptr-records}

>[!CONTEXTUALHELP]
>id="ajo_admin_ptr_record"
>title="하위 도메인의 PTR 기록"
>abstract="포인터 레코드(PTR)는 IP 주소에 연결된 도메인 이름을 제공하는 DNS 레코드 유형으로 수신 메일 서버가 발신자의 IP 주소를 확인하는 데 도움을 줍니다. 이메일 게재 전문가의 심사와 충분한 논의를 거친 후에만 PTR 기록을 편집합니다."

>[!CONTEXTUALHELP]
>id="ajo_admin_ptr_record_header"
>title="하위 도메인의 PTR 기록"
>abstract="Journey Optimizer에서 하위 도메인이 Adobe에 위임되면 PTR 기록이 자동으로 만들어지고 이 하위 도메인에 연결됩니다."

## PTR 레코드 정보 {#about-ptr-records}

PTR(포인터 레코드)는 IP 주소에 연결된 도메인 이름을 제공하는 DNS(Domain Name System) 레코드의 유형입니다.

PTR 레코드를 통해 수신 메일 서버는 해당 IP 주소가 서버가 연결하는 이름에 해당하는지 여부를 확인하여 전송 메일 서버의 진위를 확인할 수 있습니다.

## 하위 도메인의 PTR 레코드에 액세스 {#access-ptr-records}

한 번 [하위 도메인이 위임됨](delegate-subdomain.md) Adobe Journey Optimizer에서 이 하위 도메인과 PTR 레코드가 자동으로 만들어지고 연결됩니다. 에서 액세스할 수 있습니다. **[!UICONTROL 관리]** > **[!UICONTROL 채널]** > **[!UICONTROL 이메일 구성]** > **[!UICONTROL PTR 레코드]** 메뉴 아래의 제품에서 사용할 수 있습니다.

![](assets/ptr-records.png)

이 목록에는 아래 구문을 사용하여 위임된 각 하위 도메인에 대해 생성된 PTR 레코드가 표시됩니다.

* &quot;r&quot;은 레코드,
* IP 주소의 마지막 두 수치에 대해 &quot;xx&quot;
* 하위 도메인 이름.

목록에서 PTR 레코드를 열어 연결된 하위 도메인 이름과 IP 주소를 표시할 수 있습니다.

## PTR 레코드 편집 {#edit-ptr-record}

PTR 레코드를 수정하여 IP 주소와 연결된 하위 도메인을 편집할 수 있습니다.

>[!CAUTION]
>
>PTR 레코드는 모든 환경에서 일반적입니다. 따라서 PTR 레코드를 수정하면 프로덕션 샌드박스도 영향을 받습니다.
>
>PTR 레코드를 편집할 때 추가 주의가 필요합니다. 확실하지 않은 경우 게재 가능성 전문가에게 문의하십시오.

### 완전히 위임된 하위 도메인 {#fully-delegated-subdomains}

하위 도메인으로 PTR 레코드를 편집하려면 [완전히 위임됨](delegate-subdomain.md#full-subdomain-delegation) Adobe을 수행하려면 아래 단계를 따르십시오.

1. 목록에서 PTR 레코드 이름을 클릭하여 엽니다.

   ![](assets/ptr-record-select.png)

1. 하위 도메인 선택 [완전히 위임됨](delegate-subdomain.md#full-subdomain-delegation) Adobe을 클릭합니다.

   ![](assets/ptr-record-subdomain.png)

1. 클릭 **[!UICONTROL 저장]** 를 클릭하여 변경 사항을 확인합니다.

>[!NOTE]
>
>는 수정할 수 없습니다 **[!UICONTROL IP]** 및 **[!UICONTROL PTR 레코드]** 필드.

### CNAME 방법을 사용하여 위임된 하위 도메인 {#edit-ptr-subdomains-cname}

을 사용하여 Adobe에 위임되는 하위 도메인으로 PTR 레코드를 편집하려면 [CNAME 메서드](delegate-subdomain.md#cname-subdomain-delegation)를 채우기 위해 아래의 단계를 수행하십시오.

1. 목록에서 PTR 레코드 이름을 클릭하여 엽니다.

   ![](assets/ptr-record-select-cname.png)

1. 을 사용하여 Adobe에 위임한 하위 도메인을 선택합니다. [CNAME 메서드](delegate-subdomain.md#cname-subdomain-delegation) 참조하십시오.

   ![](assets/ptr-record-subdomain-cname.png)

1. 호스팅 플랫폼에서 새 정방향 DNS 레코드를 만들어야 합니다. 이렇게 하려면 Adobe에서 생성한 레코드를 복사합니다. 완료되면 &quot;확인...&quot; 상자를 선택합니다.

   ![](assets/ptr-record-subdomain-confirm.png)

   >[!NOTE]
   >
   >이 메시지가 나타나면: &quot;먼저 앞으로 DNS를 만든 후 다시 시도하세요.&quot;는 아래 단계를 따르십시오.
   >   * 전달 DNS 레코드가 성공적으로 만들어졌는지 DNS 공급자를 확인합니다.
   >   * DNS의 레코드는 즉시 동기화되지 않을 수 있습니다. 잠시 기다렸다가 다시 시도하십시오.


1. 클릭 **[!UICONTROL 저장]** 를 클릭하여 변경 사항을 확인합니다.

>[!NOTE]
>
>는 수정할 수 없습니다 **[!UICONTROL IP]** 및 **[!UICONTROL PTR 레코드]** 필드.

## PTR 레코드 업데이트 세부 정보 확인 {#check-ptr-record-update}

PTR 레코드 편집을 확인한 후에는 **[!UICONTROL 처리 중]** 목록의 PTR 레코드 이름 옆에 아이콘이 표시됩니다.

![](assets/ptr-record-updating.png)

>[!NOTE]
>
>다음 [업데이트 처리](#processing) 최대 3시간이 소요될 수 있습니다.

PTR 레코드 업데이트 세부 정보를 확인하려면 옆에 있는 아이콘을 클릭합니다. 의 다른 아이콘과 연결된 상태에 대해 자세히 알아보십시오 [이 섹션](#ptr-record-update-statuses).

![](assets/ptr-record-recent-update.png)

업데이트 상태 및 요청된 변경 사항과 같은 정보를 볼 수 있습니다.

![](assets/ptr-record-updates.png)

## PTR 레코드 업데이트 상태 {#ptr-record-update-statuses}

PTR 레코드 업데이트에는 다음 상태가 있을 수 있습니다.

* ![](assets/do-not-localize/ptr-record-processing.png) **[!UICONTROL 처리 중]**: PTR 레코드 업데이트가 제출되었으며 확인 프로세스를 진행 중입니다.
* ![](assets/do-not-localize/ptr-record-success.png) **[!UICONTROL 성공]**: 업데이트된 PTR 레코드가 확인되었으며 새 하위 도메인이 IP 주소와 연결됩니다.
* ![](assets/do-not-localize/ptr-record-failed.png) **[!UICONTROL 실패]**: PTR 레코드 업데이트 확인 중에 하나 또는 여러 개의 검사가 실패했습니다.

### 처리 중 {#processing}

IP 주소와 연결할 새 하위 도메인이 유효한지 확인하기 위해 몇 가지 게재 기능 검사가 수행됩니다. 최대 3시간이 소요될 수 있습니다.

>[!NOTE]
>
>업데이트가 진행 중인 동안에는 PTR 레코드를 수정할 수 없습니다. 여전히 해당 이름을 클릭할 수 있지만, **[!UICONTROL 하위 도메인]** 필드가 회색으로 표시됩니다. 업데이트가 완료될 때까지 변경 사항이 반영되지 않습니다.

유효성 검사 프로세스 중에 이전 하위 도메인이 IP 주소와 계속 연결됩니다.

### 성공 {#success}

유효성 검사 프로세스가 성공하면 새 하위 도메인이 IP 주소와 자동으로 연결됩니다.

### 실패 {#failes}

유효성 검사 프로세스가 실패하면 이전 PTR 레코드가 표시됩니다. 이전에 IP 주소와 연결된 유효한 하위 도메인은 변경되지 않고 그대로 유지됩니다.

가능한 업데이트 오류 유형은 다음과 같습니다.
* PTR 레코드에 대한 새 전달 DNS를 만들지 못했습니다.
* 레코드를 업데이트하지 못했습니다.
* 관심 영역 재게재 실패

업데이트가 실패하면 PTR 레코드를 다시 편집할 수 있게 됩니다. 해당 이름을 클릭하고 하위 도메인을 다시 업데이트할 수 있습니다.
