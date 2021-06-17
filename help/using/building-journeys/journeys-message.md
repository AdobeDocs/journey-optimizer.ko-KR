---
title: 여정에 메시지 추가
description: 여정에 메시지 추가
feature: 여정
topic: 콘텐츠 관리
role: User
level: Intermediate
source-git-commit: d76eee0efa6735d6d81d7d7c752ed253b4cbebb5
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 3%

---

# 여정에 메시지 추가

[!DNL Journey Optimizer] 메시지 기능이 내장되어 있으므로 컨텐츠를 디자인하고 메시지를 게시하기만 하면 됩니다. [이 섹션](../get-started-content.md)을 참조하십시오. 그런 다음 Journey Optimizer을 사용하여 디자인된 푸시 또는 이메일 메시지를 여정에 추가하면 됩니다.

서드파티 시스템을 사용하여 메시지를 전송하는 경우 사용자 지정 작업을 만들 수 있습니다. 자세한 내용은 이 [섹션](../action/action.md)을 참조하십시오.

## 메시지 활동 추가

1. 항상 그렇듯이 이벤트 또는 **여정 읽기** 활동으로 세그먼트를 시작합니다.

   ![](../assets/jo-message0.png)

1. 팔레트의 **작업** 섹션에서 **메시지** 활동을 캔버스로 끌어다 놓습니다.

   ![](../assets/jo-message1.png)

1. 레이블 및 설명을 추가합니다.

   ![](../assets/jo-message2.png)

1. **메시지** 필드 내부를 클릭합니다. Journey Optimizer에서 디자인된 사용 가능한 메시지 목록이 표시됩니다. 상태별로 목록을 필터링할 수 있습니다.

   ![](../assets/jo-message3.png)

1. 메시지를 선택하고 **선택**&#x200B;을 클릭합니다. **메시지 만들기**&#x200B;를 클릭하여 이 화면에서 직접 새 메시지를 만들 수도 있습니다.

   ![](../assets/jo-message4-ter.png)

   메시지를 확인하려면 **메시지** 필드에서 **메시지** 아이콘을 클릭할 수 있습니다. 메시지가 새 탭에서 열립니다.

   ![](../assets/jo-message4-bis.png)

1. 여정에 다음 단계를 추가합니다.

## 전자 메일 매개 변수 및 푸시 매개 변수

**[!UICONTROL Email parameters]** 및 **[!UICONTROL Push parameters]** 섹션에는 읽기 전용 필드가 표시됩니다. 일반적으로 메시지를 만들 때 이 구성을 수행합니다. [이 섹션](../get-started-content.md)을 참조하십시오.

![](../assets/jo-message4.png)

특정 값을 강제 수행하려면 필드 오른쪽의 **매개 변수 재정의 사용** 아이콘을 사용할 수 있습니다. 이 옵션은 테스트 목적으로 유용할 수 있습니다. 예를 들어 이메일의 경우 이메일 주소를 추가할 수 있습니다. 여정을 게시하면 이메일이 사용자에게 전송됩니다.
