---
solution: Journey Optimizer
product: journey optimizer
title: 구독자에게 메시지 보내기
description: 목록 구독자에게 메시지를 보내는 여정을 만드는 방법을 알아봅니다
feature: Journeys, Use Cases, Subscriptions
topic: Content Management
role: User, Data Engineer
level: Intermediate, Experienced
keywords: 여정, 사용 사례, 메시지, 구독자, 목록, 읽기
exl-id: 2540938f-8ac7-43fa-83ff-fed59f6bc417
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 17%

---

# 사용 사례: 목록의 구독자에게 메시지 보내기{#send-a-message-to-the-subscribers-of-a-list}

이 사용 사례의 목적은 목록 구독자에게 메시지를 보내는 여정을 만드는 것입니다.

이 예제에서는 [!DNL Adobe Experience Platform]의 **[!UICONTROL 동의 및 환경 설정 세부 정보]** 필드 그룹이 사용됩니다. 이 필드 그룹을 찾으려면 **[!UICONTROL 데이터 관리]** 메뉴에서 **[!UICONTROL 스키마]**&#x200B;를 선택하십시오. **[!UICONTROL 필드 그룹]** 탭에서 검색 필드에 필드 그룹의 이름을 입력합니다.

![이 필드 그룹에 구독 요소가 포함되어 있습니다](assets/consent-and-preference-details-field-group.png)

이 여정을 구성하려면 다음 단계를 수행합니다.

1. **[!UICONTROL 읽기]** 활동으로 시작하는 여정을 만듭니다. [자세히 보기](journey-gs.md).
1. **[!UICONTROL 전자 메일]** 작업 활동을 여정에 추가합니다. [자세히 보기](journeys-message.md).
1. **[!UICONTROL 이메일]** 활동 설정의 **[!UICONTROL 이메일 매개 변수]** 섹션에서 기본 이메일 주소(`PersonalEmail.adress`)를 목록 구독자의 이메일 주소로 바꾸십시오.

   1. **[!UICONTROL 주소]** 필드 오른쪽에 있는 **[!UICONTROL 매개 변수 재정의 사용]** 아이콘을 클릭한 다음 **[!UICONTROL 편집]** 아이콘을 클릭합니다.

      ![](assets/message-to-subscribers-uc-1.png)

   1. 표현식 편집기에서 구독자의 이메일 주소를 검색하는 표현식을 입력합니다. [자세히 보기](expression/expressionadvanced.md).

      다음 예에서는 매핑 필드에 대한 참조를 포함하는 표현식을 보여 줍니다.

      ```json
      #{ExperiencePlatform.Subscriptions.profile.consents.marketing.email.subscriptions.entry('daily-email').subscribers.firstEntryKey()}
      ```

      이 예에서는 다음 함수가 사용됩니다.

      | 함수 | 설명 | 예 |
      | --- | --- | --- |
      | `entry` | 선택한 네임스페이스에 따라 맵 요소를 참조하십시오. | 특정 구독 목록 참조 |
      | `firstEntryKey` | 맵의 첫 번째 시작 키 검색 | 구독자의 첫 번째 이메일 주소 검색 |

      이 예제에서 구독 목록의 이름은 `daily-email`입니다. 이메일 주소는 `subscribers` 맵에서 구독 목록 맵에 연결된 키로 정의됩니다.

      식의 [필드 참조](expression/field-references.md)에 대해 자세히 알아보세요.

      ![](assets/message-to-subscribers-uc-2.png)

   1. **[!UICONTROL 식 추가]** 대화 상자에서 **[!UICONTROL 확인]**&#x200B;을 클릭합니다.

>[!CAUTION]
>
>이메일 주소 재정의는 특정 사용 사례에만 사용해야 합니다. 대부분의 경우 **[!UICONTROL 실행 필드]**&#x200B;에 기본 주소로 정의된 값을 사용해야 하므로 이메일 주소를 변경할 필요가 없습니다. [자세히 알아보기](../configuration/primary-email-addresses.md)
