---
title: IP 풀 만들기
description: '"ip 풀을 관리하는 방법 알아보기"'
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
source-git-commit: 63de381ea3a87b9a77bc6f1643272597b50ed575
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 3%

---


# IP 풀 만들기

## IP 풀 기본 정보

Journey Optimizer을 사용하여 하위 도메인의 IP 주소를 함께 그룹화하는 IP 풀을 만들 수 있습니다.

이메일 게재 기능을 위해서는 IP 풀을 만드는 것이 좋습니다. 이렇게 하면 하위 도메인의 평판을 다른 하위 도메인에 영향을 주지 않을 수 있습니다.

예를 들어, 마케팅 메시지를 위한 IP 풀과 트랜잭션 메시지를 위한 IP 풀이 있는 것이 좋습니다. 그렇게 하면 마케팅 메시지 중 하나가 제대로 수행되지 않고 고객이 스팸으로 선언할 경우 이는 트랜잭션 메시지(구매 확인, 암호 복구 메시지 등)를 계속 수신할 이 고객에게 보내는 트랜잭션 메시지에 영향을 주지 않습니다.

## IP 풀 만들기

IP 풀을 생성하려면 다음 단계를 수행합니다.

1. **[!UICONTROL Channels]** / **[!UICONTROL IP pools]** 메뉴에 액세스한 다음 **[!UICONTROL Create IP Pool]** 를 클릭합니다.

   ![](../assets/ip-pool-create.png)

1. IP 풀의 이름과 설명(선택 사항)을 제공합니다.

   >[!NOTE]
   >
   >하위 도메인의 이름은 문자(A-Z)로 시작하고 영숫자 또는 특수 문자( _, ., - )만 포함해야 합니다.

1. 드롭다운 목록에서 풀에 포함할 IP 주소를 선택한 다음 **[!UICONTROL Submit]** 을 클릭합니다.

   ![](../assets/ip-pool-config.png)

   >[!NOTE]
   >
   >인스턴스와 함께 제공된 모든 IP 주소를 목록에서 사용할 수 있습니다.

이제 IP 풀이 생성되고 목록에 표시됩니다. 속성을 선택하여 해당 속성에 액세스하고 관련 메시지 사전 설정을 표시할 수 있습니다. 메시지 사전 설정을 IP 풀과 연결하는 방법에 대한 자세한 내용은 [이 섹션](message-presets.md))을 참조하십시오.

![](../assets/ip-pool-created.png)

IP 풀을 편집하려면 해당 풀을 연 다음 원하는 대로 속성을 편집합니다.

>[!NOTE]
>
>메시지 사전 설정이 IP 풀에 연결되어 있는 경우 IP 풀을 편집하기 전에 먼저 메시지를 제거해야 합니다. 수정을 완료하면 메시지 사전 설정을 다시 연결할 수 있습니다.
