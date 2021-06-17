---
title: 메시지 게시 및 수정
description: 메시지 게시 및 업데이트 방법 알아보기
snippet: y
feature: 여정
topic: 콘텐츠 관리
role: User
level: Intermediate
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 4%

---

# 메시지 {#publish-manage-messages} 게시

## 메시지 {#publish-message} 게시

메시지가 만들어지면 이를 게시하여 실행할 수 있도록 할 수 있습니다.

>[!CAUTION]
>
>경고를 게시하기 전에 경고를 확인하고 확인합니다. [자세히 알아보기](alerts.md).

![](assets/publish-message.png)

메시지가 게시되면 **[!UICONTROL Published]** 상태가 있는 메시지 목록에 추가됩니다.

이제 하나 이상의 [여정](building-journeys/journey.md)에 의해 트리거될 준비가 되었습니다.

## 읽기 전용 메시지 {#modify-message} 업데이트

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

<!--For batch messages, the audience/segment being processed in the previous execution will not be affected by the new version. Only the next incoming API call with an audience/segment will generate a new message execution with the new version.-->
