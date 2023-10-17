---
solution: Journey Optimizer
product: journey optimizer
title: IP 풀 만들기
description: IP 풀을 관리하는 방법 알아보기
feature: Subdomains, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: IP, 풀, 그룹, 하위 도메인, 전달성
exl-id: 606334c3-e3e6-41c1-a10e-63508a3ed747
source-git-commit: 8579acfa881f29ef3947f6597dc11d4c740c3d68
workflow-type: tm+mt
source-wordcount: '717'
ht-degree: 10%

---

# IP 풀 만들기 {#create-ip-pools}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_pool_header"
>title="IP 풀 설정"
>abstract="IP 풀은 이메일 전달성을 개선할 수 있도록 하위 도메인의 IP 주소를 수집합니다."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_pool"
>title="IP 풀 설정"
>abstract="Journey Optimizer를 통해 IP 풀을 만들어 하위 도메인의 IP 주소를 함께 그룹화할 수 있습니다. 이렇게 하면 하위 도메인의 신뢰도가 다른 하위 도메인에 영향을 미칠 수 없으므로 이메일 전달성이 크게 개선될 수 있습니다."

## IP 풀 기본 정보 {#about-ip-pools}

포함 [!DNL Journey Optimizer]를 사용하여 하위 도메인의 IP 주소를 함께 그룹화하는 IP 풀을 만들 수 있습니다.

이메일 전달성을 위해 IP 풀을 만드는 것이 좋습니다. 이렇게 하면 하위 도메인의 평판이 다른 하위 도메인에 영향을 주지 않도록 할 수 있습니다.

예를 들어 마케팅 메시지용 IP 풀 하나와 트랜잭션 메시지용 IP 풀 하나를 갖는 것이 좋습니다. 이렇게 하면 마케팅 메시지 중 하나가 나쁜 성과를 보이고 고객이 스팸으로 선언한 경우, 이는 여전히 트랜잭션 메시지(구매 확인, 암호 복구 메시지 등)를 받을 동일한 고객에게 전송된 트랜잭션 메시지에는 영향을 주지 않습니다.

>[!CAUTION]
>
>IP 풀 구성은 모든 환경에 공통됩니다. 따라서 모든 IP 풀 생성 또는 편집 작업은 프로덕션 샌드박스에도 영향을 줍니다.

## IP 풀 만들기 {#create-ip-pool}

IP 풀을 만들려면 다음 단계를 수행합니다.

1. 액세스 **[!UICONTROL 관리]** > **[!UICONTROL 채널]** > **[!UICONTROL IP 풀]** 메뉴를 선택한 다음 **[!UICONTROL IP 풀 만들기]**.

   ![](assets/ip-pool-create.png)

1. IP 풀의 이름과 설명을 입력합니다(선택 사항).

   >[!NOTE]
   >
   >이름은 문자(A-Z)로 시작하고, 이름에는 영숫자나 특수문자( _, ., - )만 포함되어야 합니다.

1. 드롭다운 목록에서 풀에 포함할 IP 주소를 선택한 다음 를 클릭합니다. **[!UICONTROL 제출]**.

   ![](assets/ip-pool-config.png)

   >[!NOTE]
   >
   >인스턴스와 함께 프로비저닝된 모든 IP 주소를 목록에서 사용할 수 있습니다.

IP를 선택하면 목록에서 IP와 연결된 PTR 레코드를 볼 수 있습니다. 이렇게 하면 IP 풀을 만들 때 각 IP에 대한 브랜딩 정보를 확인하고 예를 들어 동일한 브랜딩 정보가 있는 IP를 선택할 수 있습니다. [PTR 레코드에 대한 자세한 정보](ptr-records.md)

![](assets/ip-pool-ptr-record.png)

>[!NOTE]
>
>IP에 대해 구성된 PTR 레코드가 없는 경우 해당 IP를 선택할 수 없습니다. 해당 IP의 PTR 기록을 구성하려면 Adobe 담당자에게 문의하십시오.

IP 풀이 만들어지면 IP 풀 드롭다운 목록 아래에 표시된 IP 주소 위로 마우스를 가져가면 PTR 정보가 표시됩니다.

![](assets/ip-pool-ptr-record-tooltip.png)

이제 IP 풀이 만들어지고 목록에 표시됩니다. 해당 속성에 액세스하고 관련 채널 표면(즉, 메시지 사전 설정)을 표시하도록 선택할 수 있습니다. 채널 표면을 IP 풀과 연결하는 방법에 대한 자세한 내용은 [이 섹션](channel-surfaces.md).

![](assets/ip-pool-created.png)

## IP 풀 편집 {#edit-ip-pool}

IP 풀을 편집하려면 아래 단계를 따르십시오.

1. 목록에서 IP 풀 이름을 클릭하여 엽니다.

   ![](assets/ip-pool-list.png)

1. 원하는 대로 속성을 편집합니다. 설명을 수정하고 IP 주소를 추가하거나 제거할 수 있습니다.

   >[!NOTE]
   >
   >IP 풀 이름을 편집할 수 없습니다. 이를 수정하려면 IP 풀을 삭제하고 선택한 이름으로 다른 IP 풀을 만들어야 합니다.

   ![](assets/ip-pool-edit.png)

   >[!CAUTION]
   >
   >IP를 삭제하면 다른 IP에 추가 로드가 발생하고 전달성에 심각한 영향을 미칠 수 있으므로 삭제할 때 각별한 주의를 기울여 진행하십시오. 의심이 가는 경우 게재 가능성 전문가에게 문의하십시오.

1. 변경 내용을 저장합니다.

업데이트는 연결된 IP 풀에 따라 즉시 또는 비동기적으로 적용됩니다. [채널 표면](channel-surfaces.md) 또는 아님:

* IP 풀이 인 경우 **아님** 모든 채널 표면과 연결된 업데이트는 즉시 수행됩니다(**[!UICONTROL 성공]** 상태).
* IP 풀인 경우 **은(는)** 채널 표면과 연결된 업데이트는 최대 3시간 정도 소요될 수 있습니다(**[!UICONTROL 처리 중]** 상태).

>[!NOTE]
>
>날짜 [채널 표면 만들기](channel-surfaces.md#create-channel-surface), 편집 중인 IP 풀을 선택하는 경우(**[!UICONTROL 처리 중]** status) 및 은(는) 해당 표면에 대해 선택된 하위 도메인과 연결된 적이 없으므로 표면 생성을 계속할 수 없습니다. [자세히 알아보기](channel-surfaces.md#subdomains-and-ip-pools)

IP 풀 업데이트 상태를 확인하려면 **[!UICONTROL 추가 작업]** 단추 및 선택 **[!UICONTROL 최근 업데이트]**.

![](assets/ip-pool-recent-update.png)

>[!NOTE]
>
>IP 풀이 성공적으로 업데이트되면 다음을 기다려야 할 수 있습니다.
>* 단일 메시지에 소비되기 몇 분 전에
>* 다음 배치(IP 풀 배치 시)가 배치 메시지에 유효할 때까지.

다음을 사용할 수도 있습니다 **[!UICONTROL 삭제]** IP 풀 삭제 단추 채널 표면과 연결된 IP 풀은 삭제할 수 없습니다.

