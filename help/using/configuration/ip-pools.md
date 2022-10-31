---
solution: Journey Optimizer
product: journey optimizer
title: IP 풀 만들기
description: IP 풀을 관리하는 방법 알아보기
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 606334c3-e3e6-41c1-a10e-63508a3ed747
source-git-commit: 3a932747de33ced59d68835a96386b7ac560e4fe
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 1%

---

# IP 풀 만들기 {#create-ip-pools}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_pool_header"
>title="IP 풀 설정"
>abstract="IP 풀은 하위 도메인의 IP 주소를 수집하여 전자 메일 게재 기능을 개선합니다."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_pool"
>title="IP 풀 설정"
>abstract="Journey Optimizer을 사용하여 하위 도메인의 IP 주소를 함께 그룹화하는 IP 풀을 만들 수 있습니다. 이렇게 하면 하위 도메인의 평판을 다른 하위 도메인에 영향을 주지 않으므로 이메일 게재 기능이 크게 향상될 수 있습니다."

## IP 풀 기본 정보 {#about-ip-pools}

사용 [!DNL Journey Optimizer]를 설정하는 경우 하위 도메인의 IP 주소를 함께 그룹화하는 IP 풀을 만들 수 있습니다.

이메일 게재 기능을 위해서는 IP 풀을 만드는 것이 좋습니다. 이렇게 하면 하위 도메인의 평판을 다른 하위 도메인에 영향을 주지 않을 수 있습니다.

예를 들어, 마케팅 메시지를 위한 IP 풀과 트랜잭션 메시지를 위한 IP 풀이 있는 것이 좋습니다. 이 방법으로 마케팅 메시지 중 하나가 제대로 수행되지 않고 고객이 스팸으로 선언할 경우 이는 트랜잭션 메시지(구매 확인, 암호 복구 메시지 등)를 계속 수신할 이 고객에게 보내는 트랜잭션 메시지에 영향을 주지 않습니다.

>[!CAUTION]
>
>IP 풀 구성은 모든 환경에 공통입니다. 따라서 모든 IP 풀 생성 또는 에디션은 프로덕션 샌드박스에도 영향을 줍니다.

## IP 풀 만들기 {#create-ip-pool}

IP 풀을 생성하려면 다음 단계를 수행합니다.

1. 액세스 권한 **[!UICONTROL 관리]** > **[!UICONTROL 채널]** > **[!UICONTROL IP 풀]** 메뉴를 클릭한 다음 **[!UICONTROL IP 풀 만들기]**.

   ![](assets/ip-pool-create.png)

1. IP 풀의 이름과 설명(선택 사항)을 제공합니다.

   >[!NOTE]
   >
   >이름은 문자(A-Z)로 시작하고 영숫자 또는 특수 문자( _, ., - )만 포함해야 합니다.

1. 드롭다운 목록에서 풀에 포함할 IP 주소를 선택한 다음 를 클릭합니다 **[!UICONTROL 제출]**.

   ![](assets/ip-pool-config.png)

   >[!NOTE]
   >
   >인스턴스와 함께 제공된 모든 IP 주소를 목록에서 사용할 수 있습니다.

이제 IP 풀이 생성되고 목록에 표시됩니다. 속성을 선택하여 해당 속성에 액세스하고 관련 채널 서피스(즉, 메시지 사전 설정)를 표시할 수 있습니다. 채널 서피스를 IP 풀과 연결하는 방법에 대한 자세한 내용은 [이 섹션](channel-surfaces.md).

![](assets/ip-pool-created.png)

## IP 풀 편집 {#edit-ip-pool}

IP 풀을 편집하려면 아래 단계를 따르십시오.

1. 목록에서 IP 풀 이름을 클릭하여 엽니다.

   ![](assets/ip-pool-list.png)

1. 원하는 대로 속성을 편집합니다. 설명을 수정하고 IP 주소를 추가하거나 제거할 수 있습니다.

   >[!NOTE]
   >
   >IP 풀 이름을 편집할 수 없습니다. 수정하려면 IP 풀을 삭제하고 선택한 이름을 가진 다른 풀을 만들어야 합니다.

   ![](assets/ip-pool-edit.png)

   >[!CAUTION]
   >
   >IP 삭제를 고려할 때 추가 로드를 다른 IP에 할당하고 게재 능력에 심각한 영향을 줄 수 있으므로 추가 주의가 필요합니다. 확실하지 않은 경우 게재 가능성 전문가에게 문의하십시오.

1. 변경 내용을 저장합니다.

업데이트는 다음에 연결되는 IP 풀에 따라 즉시 또는 비동기식으로 적용됩니다 [채널 표면](channel-surfaces.md) 또는 다음 아님:

* IP 풀이 **not** 모든 채널 서피스와 연결된 업데이트는 즉시 수행됩니다(**[!UICONTROL 성공]** 상태).
* IP 풀이 **is** 채널 서피스와 연결된 업데이트에는 최대 3시간이 소요될 수 있습니다(**[!UICONTROL 처리 중]** 상태).

>[!NOTE]
>
>When [채널 서피스 생성](channel-surfaces.md#create-channel-surface)( 버전( )에 있는 IP 풀을 선택하는 경우&#x200B;**[!UICONTROL 처리 중]** 상태) 및 를 해당 서피스에 대해 선택한 하위 도메인과 연관되지 않은 경우 서피스 생성을 진행할 수 없습니다. [자세히 보기](channel-surfaces.md#subdomains-and-ip-pools)

IP 풀 업데이트 상태를 확인하려면 **[!UICONTROL 추가 작업]** 단추를 누르고 선택합니다. **[!UICONTROL 최근 업데이트]**.

![](assets/ip-pool-recent-update.png)

>[!NOTE]
>
>IP 풀이 성공적으로 업데이트되면 다음을 기다려야 할 수 있습니다.
>* 몇 분 전에 한 가지 메세지에 의해
>* 배치 메시지에서 IP 풀이 유효할 때까지.


를 사용할 수도 있습니다 **[!UICONTROL 삭제]** IP 풀을 삭제하는 단추 채널 서피스에 연결된 IP 풀은 삭제할 수 없습니다.

