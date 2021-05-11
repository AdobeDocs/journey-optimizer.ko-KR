---
title: 메시지 만들기
description: 메시지를 만드는 방법 학습
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 1%

---

# 메시지 {#create-message} 만들기

![](assets/do-not-localize/badge.png)

메시지는 왼쪽 레일의 **[!UICONTROL Messages]** 바로 가기에서 사용할 수 있습니다. 모든 메시지가 나열되며 게시 날짜(게시된 메시지의 경우) 또는 작성 날짜(초안 메시지의 경우)별로 정렬됩니다.

>[!NOTE]
>
>모든 사용자는 메시지를 액세스, 만들기, 편집 및 게시할 수 있습니다. 이 섹션](permissions.md)에서 사용자 권한 [에 대해 자세히 알아보십시오.

![](assets/messages-list.png)

지난 5일 동안 액세스한 메시지에 직접 링크를 추가하려면 **[!UICONTROL Show recents]** 토글을 사용합니다.

![](assets/show-recent-messages.png)

필터 아이콘을 사용하여 게시되는 초안, 게시됨 또는 메시지만 표시합니다. 아래와 같이 메시지 레이블에서 검색할 수도 있습니다.

![](assets/filter-messages.png)

## 새 메시지 만들기

새 메시지를 만들려면 아래 단계를 수행하십시오.

1. 메시지 목록에 액세스한 다음 **[!UICONTROL Create Message]**&#x200B;을 클릭합니다.

1. 메시지 속성을 정의합니다.

   ![](assets/create-message-properties.png)

   * **[!UICONTROL Title]**(필수) 및 **[!UICONTROL Description]**&#x200B;을 입력합니다.

   * 메시지에 사용할 **[!UICONTROL Preset]**&#x200B;을 선택합니다.

      사전 설정에는 브랜드에 따라 전송되는 이메일 및/또는 푸시 알림에 필요한 모든 매개 변수가 포함되어 있습니다. [브랜딩에 대한 자세한 내용을 살펴보십시오](administration.md#cjm-branding).

   * 해당 메시지에 사용할 채널을 선택합니다.이메일 및/또는 푸시 알림. 메시지를 만들 수 있으려면 채널을 하나 이상 선택해야 합니다.
   메시지 인터페이스의 **[!UICONTROL Properties]** 단추를 사용하여 언제든지 메시지의 제목, 설명 및 사전 설정에 액세스하고 수정할 수 있습니다.

   ![](assets/message-properties.png)


1. **[!UICONTROL Create]**&#x200B;을 클릭하여 메시지 작성을 확인합니다. 메시지가 메시지 목록의 **[!UICONTROL Draft]** 상태에 추가됩니다.

   선택한 각 채널에 대해 하나의 탭을 사용할 수 있습니다. 이 탭을 사용하여 각 채널에 대한 컨텐츠를 구성합니다. 탭을 선택하고 오른쪽의 **[!UICONTROL Delete channel]** 단추를 클릭하여 탭을 제거할 수 있습니다.

   ![](assets/create-messages-content.png)

   이제 메시지의 내용을 만들고 설정을 조정할 수 있습니다. 이메일 및 푸시 알림 구성에 대한 자세한 내용은 다음 섹션을 참조하십시오.

   * [이메일 구성](configure-email.md)
   * [푸시 알림 구성](configure-push.md)

   >[!NOTE]
   >   
   >표현식 편집기를 사용하여 프로필의 데이터를 사용하여 메시지를 개인화할 수 있습니다. 개인화에 대한 자세한 내용은 [이 섹션](personalization/personalize.md)을 참조하십시오.


1. 왼쪽의 미리 보기 섹션을 사용하여 메시지 렌더링을 제어하고 테스트 프로필로 개인화 설정을 확인합니다. 이 작업에 대한 자세한 정보는 [이 섹션](preview.md)을 참조하십시오.

   ![](assets/messages-simple-preview.png)

1. 편집기의 상단 섹션에서 경고를 확인합니다.  일부 메시지는 간단한 경고이지만 다른 사용자는 메시지를 게시하지 못하도록 할 수 있습니다. [이 섹션](alerts.md)에서 자세히 알아보십시오.

1. 이제 **[!UICONTROL Publish]** 단추를 클릭하여 메시지를 게시하거나 나중에 초안으로 유지하고 게시할 수 있습니다. 메시지를 게시하는 방법에 대한 자세한 내용은 [이 섹션](publish-manage-message.md)을 참조하십시오.

## 메시지 복제

기존 메시지로부터 메시지를 만들려면 메시지 인터페이스에서 **[!UICONTROL Duplicate]** 단추를 사용합니다. 모든 설정 및 구성이 새 메시지에 복사됩니다.

![](assets/message-duplicate.png)

중복을 확인하기 전에 메시지의 이름을 변경할 수 있습니다.

![](assets/message-duplicate-confirm.png)

새 메시지가 만들어지면 창 하단에 확인 메시지가 표시됩니다.

전용 아이콘을 사용하여 메시지 목록에서 메시지를 복제할 수도 있습니다.

![](assets/message-duplicate-from-list.png)

동일한 확인 프로세스가 적용됩니다.
