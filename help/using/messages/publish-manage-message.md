---
title: 메시지 게시 및 수정
description: 메시지 게시 및 업데이트 방법 알아보기
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 116e2223-a806-4f68-9a8c-c0bde6008010
source-git-commit: b43e3432ede1d4985e0a6b57b57c5efc3cf60c50
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 2%

---

# 메시지 게시 {#publish-manage-messages}

## 메시지 게시 {#publish-message}

메시지가 만들어지면 이를 게시하여 실행할 수 있도록 할 수 있습니다.

>[!CAUTION]
>
>경고를 게시하기 전에 경고를 확인하고 확인합니다. [자세히 알아보기](alerts.md)

![](assets/publish-message.png)

메시지가 게시되면 메시지가 와 함께 메시지 목록에 추가됩니다. **[!UICONTROL Published]** 상태.

이제 하나 이상 트리거할 준비가 되었습니다 [여정](../building-journeys/journey.md).

>[!NOTE]
>
>게시된 메시지에서 직접 또는 간접적으로 참조되는 오퍼, 대체 오퍼, 오퍼 컬렉션 또는 오퍼 결정을 업데이트하면 이제 다시 게시할 필요 없이 업데이트가 해당 메시지에 자동으로 반영됩니다. [오퍼에 대해 자세히 알아보기](../offers/get-started/starting-offer-decisioning.md)

## 읽기 전용 메시지 업데이트 {#modify-message}

게시 후 메시지는 읽기 전용 모드로 전환됩니다. 해당 메시지의 새 초안을 만들어 업데이트할 수도 있습니다.

이렇게 하면 메시지가 사용되는 전체 여정을 다시 게시하지 않고 컨텐츠를 업데이트하거나 문제를 해결할 수 있습니다.

>[!NOTE]
>
>게시된 버전이 여전히 게시되고 활성 상태인 동안에는 초안 버전을 편집할 수 있습니다.

게시된 메시지를 업데이트하려면:

1. 메시지 목록에서 메시지를 선택하여 엽니다.

1. **[!UICONTROL Modify]**&#x200B;을(를) 클릭합니다.

   ![](assets/message-modify.png)

1. 선택을 확인합니다. 메시지의 초안 버전이 만들어집니다.

   ![](assets/message-modify-v2.png)

1. 컨텐츠를 편집하거나 원하는 대로 설정을 변경합니다.
1. **[!UICONTROL Publish]**&#x200B;을(를) 클릭합니다. 이 작업은 다음 실행에 사용될 메시지의 새 버전을 게시합니다.

새 버전이 게시되는 즉시 다음 API 호출 시 새 메시지 실행이 생성됩니다. 다음 수신 프로필은 새 버전을 받습니다.

<!--For batch messages, the audience/segment being processed in the previous execution will not be affected by the new version. Only the next incoming API call with an audience/segment will generate a new message execution with the new version. -->
