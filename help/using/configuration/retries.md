---
title: 다시 시도
description: 주소를 제외 목록으로 보내기 전에 다시 시도하는 방법을 알아봅니다
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
source-git-commit: 79c3c47eb6978f377bf4dc49f787e9a509aa3f61
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---


# 다시 시도 {#retries}

일시적인 **소프트 바운스** 또는 **무시됨** 오류로 인해 이메일 메시지가 실패하면 여러 번 다시 시도됩니다. 각 오류로 인해 오류 카운터가 증가합니다. 이 카운터가 제한 임계값에 도달하면 주소가 제외 목록에 추가됩니다.

>[!NOTE]
>
>[게재 실패 유형](../suppression-list.md#delivery-failures) 섹션의 오류 유형에 대해 자세히 알아봅니다.

기본 구성에서 임계값은 다음 세 가지 오류로 설정됩니다.

* 동일한 게재의 경우, 세 번째 발생한 오류에서 주소가 무시됩니다.

* 다른 게재가 있고 최소 24시간 간격으로 두 개의 오류가 발생하는 경우 오류 카운터가 오류마다 증가하며 세 번째 시도에서는 주소도 억제됩니다.

다시 시도하여 게재가 성공하면 주소의 오류 카운터는 다시 초기화됩니다.

**[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL General]** 메뉴에서 **[!UICONTROL Edit]** 버튼을 사용하여 제한 임계값을 수정할 수 있습니다.

![](../assets/retries-edition.png)

<!--The minimum delay between retries and the maximum number of retries to be performed are based on how well an IP is performing, both historically and currently, at a given domain.-->

## 다시 시도 기간 {#retry-duration}

**다시 시도 기간**&#x200B;은 일시적인 오류나 소프트 바운스가 발생한 게재 전자 메일 메시지가 다시 시도하는 시간입니다.

기본적으로 메시지는 전자 메일 큐에 추가된 시간부터 **3.5일**(또는 **84시간**)에 대해 다시 시도됩니다.

그러나 더 이상 필요하지 않은 경우 다시 시도하지 않도록 전자 메일 채널에 적용되는 [메시지 사전 설정](message-presets.md)을 만들거나 편집할 때 필요에 따라 이 설정을 변경할 수 있습니다.

예를 들어, 암호 재설정과 관련된 트랜잭션 전자 메일에 대해 다시 시도 기간을 24시간으로 설정하고 하루 동안만 유효한 링크를 포함할 수 있습니다. 마찬가지로, 자정 판매에 대해 다시 시도 기간을 6시간으로 정의할 수 있습니다.

>[!NOTE]
>
>다시 시도 기간은 84시간을 초과할 수 없습니다. 최소 다시 시도 기간은 마케팅 이메일의 경우 6시간, 트랜잭션 이메일의 경우 10분입니다.

[이 섹션](message-presets.md#create-message-preset)에서 메시지 사전 설정을 만들 때 전자 메일 다시 시도 매개 변수를 조정하는 방법을 알아봅니다.

<!--After 3.5 days, any message in the retry queue will be removed from the queue and sent back as a bounce.-->