---
title: PTR 레코드
description: xxxx 방법 알아보기
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
source-git-commit: 6988a6ab9412e5d27f1ba9d1145cc11c7c06e7b7
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 0%

---


# PTR 레코드

## PTR 레코드 정보

PTR(포인터 레코드)는 IP 주소에 연결된 도메인 이름을 제공하는 DNS(Domain Name System) 레코드의 유형입니다.

PTR 레코드를 사용하면 수신 메일 서버가 해당 IP 주소가 서버가 연결하는 이름과 일치하는지 확인하여 전송 메일 서버의 진위를 확인할 수 있습니다.

## 하위 도메인의 PTR 레코드에 액세스

Customer Journey Management에서 하위 도메인이 위임되면 PTR 레코드가 자동으로 만들어지고 이 하위 도메인과 연결됩니다. **[!UICONTROL Channels]** / **[!UICONTROL PTR records]** 메뉴에서 액세스할 수 있습니다.

![](../assets/ptr-records.png)

이 목록에는 아래 구문을 사용하여 위임된 각 하위 도메인에 대해 생성된 PTR 레코드가 표시됩니다.

* &quot;r&quot;은 레코드,
* IP 주소의 마지막 두 수치에 대해 &quot;xx&quot;
* 하위 도메인 이름.

목록에서 PTR 레코드를 열어 연결된 하위 도메인 이름과 IP 주소를 표시할 수 있습니다.

>[!NOTE]
>
>PTR 레코드는 읽기 전용이며 IP 주소에 연결된 하위 도메인은 수정할 수 없습니다.
