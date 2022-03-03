---
title: 구독자에게 메시지 보내기
description: 목록 구독자에게 메시지를 보내는 여정을 만드는 방법을 알아봅니다
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 2540938f-8ac7-43fa-83ff-fed59f6bc417
source-git-commit: dee8dbac067dac851af02d87a3dece1ba2b29376
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 5%

---

# 사용 사례: 목록의 구독자에게 메시지 보내기{#send-a-message-to-the-subscribers-of-a-list}

이 사용 사례의 목적은 목록의 구독자에게 메시지를 보낼 여정을 만드는 것입니다.

이 예에서 **[!UICONTROL Consent and Preference Details]** 필드 그룹 [!DNL Adobe Experience Platform] 이 사용됩니다. 이 필드 그룹을 찾으려면 **[!UICONTROL Data Management]** 메뉴, 선택 **[!UICONTROL Schemas]**. 설정 **[!UICONTROL Field groups]** 탭에서 검색 필드에 필드 그룹의 이름을 입력합니다.

![이 필드 그룹에는 구독 요소가 포함됩니다](assets/consent-and-preference-details-field-group.png)

이 여정을 구성하려면 다음 단계를 수행합니다.

1. 다음으로 시작하는 여정 만들기 **[!UICONTROL Read]** 활동. [자세히 보기](journey-gs.md).
1. 추가 **[!UICONTROL Message]** 활동을 여정에 이메일과 함께 보냅니다. [자세히 보기](journeys-message.md).
1. 에서 **[!UICONTROL Email parameters]** 섹션 **[!UICONTROL Message]** 활동 설정에서 기본 이메일 주소(`PersonalEmail.adress`) 목록 구독자의 이메일 주소가 있는 경우:

   1. 을(를) 클릭합니다. **[!UICONTROL Enable parameter override]** 아이콘 을 클릭하여 제품에서 사용할 수 있습니다. **[!UICONTROL Address]** 필드를 클릭한 다음 **[!UICONTROL Edit]** 아이콘.

      ![](assets/message-to-subscribers-uc-1.png)

      이메일 주소를 수정하려면 이전에 메시지를 게시했는지 확인해야 합니다.

   1. 표현식 편집기에서 구독자의 이메일 주소를 검색할 표현식을 입력합니다. [자세히 보기](expression/expressionadvanced.md).

      이 예는 맵 필드에 대한 참조를 포함하는 표현식을 보여줍니다.

      ```json
      #{ExperiencePlatform.Subscriptions.profile.consents.marketing.email.subscriptions.entry('daily-email').subscribers.firstEntryKey()}
      ```

      이 예에서는 다음 함수가 사용됩니다.

      | 함수 | 설명 | 예 |
      | --- | --- | --- |
      | `entry` | 선택한 네임스페이스에 따라 맵 요소를 참조하십시오 | 특정 구독 목록을 참조하십시오 |
      | `firstEntryKey` | 맵의 첫 번째 시작 키 검색 | 구독자의 첫 번째 이메일 주소 검색 |

      이 예제에서 구독 목록은 `daily-email`. 이메일 주소는 `subscribers` 맵: 가입 목록 맵에 연결됩니다.

      자세한 내용 [필드 참조](expression/field-references.md) 참조하십시오.

      ![](assets/message-to-subscribers-uc-2.png)

   1. 에서 **[!UICONTROL Add an expression]** 대화 상자 **[!UICONTROL Ok]**.

   ![](assets/message-to-subscribers-uc-3.png)

1. 로 여정 종료 **[!UICONTROL End]** 활동.
