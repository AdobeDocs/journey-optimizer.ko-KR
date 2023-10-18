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

이 예에서는 **[!UICONTROL 동의 및 환경 설정 세부 정보]** 다음에서 필드 그룹: [!DNL Adobe Experience Platform] 를 사용합니다. 이 필드 그룹을 찾으려면 **[!UICONTROL 데이터 관리]** 메뉴, 선택 **[!UICONTROL 스키마]**. 다음에서 **[!UICONTROL 필드 그룹]** 탭에서 검색 필드에 필드 그룹의 이름을 입력합니다.

![이 필드 그룹에는 subscriptions 요소가 포함되어 있습니다.](assets/consent-and-preference-details-field-group.png)

이 여정을 구성하려면 다음 단계를 수행합니다.

1. 다음으로 시작하는 여정 만들기 **[!UICONTROL 읽기]** 활동. [자세히 보기](journey-gs.md).
1. 추가 **[!UICONTROL 이메일]** 여정에 대한 작업 활동. [자세히 보기](journeys-message.md).
1. 다음에서 **[!UICONTROL 이메일 매개 변수]** 의 섹션 **[!UICONTROL 이메일]** 활동 설정에서 기본 이메일 주소()를 바꿉니다.`PersonalEmail.adress`) 아래에 나열된 목록의 구독자를 위한 이메일 주소를 추가합니다.

   1. 다음을 클릭합니다. **[!UICONTROL 매개 변수 재정의 활성화]** 아이콘(오른쪽) **[!UICONTROL 주소]** 필드를 클릭한 다음 **[!UICONTROL 편집]** 아이콘.

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

      이 예제에서 가입 목록의 이름은 입니다 `daily-email`. 이메일 주소는 의 키로 정의됨 `subscribers` 구독 목록 맵에 연결된 맵.

      자세한 내용 [필드에 대한 참조](expression/field-references.md) 표현식.

      ![](assets/message-to-subscribers-uc-2.png)

   1. 다음에서 **[!UICONTROL 표현식 추가]** 대화 상자에서 **[!UICONTROL 확인]**.

>[!CAUTION]
>
>이메일 주소 재정의는 특정 사용 사례에만 사용해야 합니다. 대부분의 경우 **[!UICONTROL 실행 필드]**&#x200B;에 기본 주소로 정의된 값을 사용해야 하므로 이메일 주소를 변경할 필요가 없습니다. [자세히 알아보기](../configuration/primary-email-addresses.md)
