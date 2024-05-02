---
solution: Journey Optimizer
product: journey optimizer
title: 프로필 업데이트
description: 여정에서 프로필 업데이트 활동을 사용하는 방법 알아보기
feature: Journeys, Profiles, Activities
topic: Content Management
role: User
level: Intermediate
keywords: 프로필, 업데이트, 여정, 활동
exl-id: 8b2b2d1e-9bd1-439d-a15e-acdbab387c4b
source-git-commit: 0571a11eabffeb5e318bebe341a8df18da7db598
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 6%

---

# 프로필 업데이트 {#update-profile}

>[!CONTEXTUALHELP]
>id="ajo_journey_update_profiles"
>title="프로필 활동 업데이트"
>abstract="프로필 업데이트 작업 활동을 사용하여 이벤트, 데이터 소스 또는 특정 값을 사용하여 도출하는 데이터로 기존 Adobe Experience Platform 프로필을 업데이트할 수 있습니다."

사용 **[!UICONTROL 프로필 업데이트]** 작업 활동을 통해 이벤트, 데이터 소스 또는 특정 값에서 가져오는 정보로 기존 Adobe Experience Platform 프로필을 업데이트합니다.

## 추천 항목

* 다음 **프로필 업데이트** 작업은 네임스페이스가 있는 여정에서만 사용할 수 있습니다.
* 작업은 기존 필드만 업데이트하며 새 프로필 필드는 만들지 않습니다.
* 를 사용할 수 없습니다. **프로필 업데이트** 경험 이벤트를 생성하는 액션(예: 구매).
* 다른 작업과 마찬가지로 오류나 시간 초과 시 대체 경로를 정의할 수 있으며 두 작업을 동시에 배치할 수는 없습니다.
* Adobe Experience Platform에 전송된 업데이트 요청은 즉시/1초 이내에 수행됩니다. 보통 몇 초는 걸리지만, 어떤 때는 보장이 없이 더 걸릴 수도 있습니다. 그 결과, 예를 들어 작업에서 로 업데이트된 &quot;필드 1&quot;을 사용하는 경우 **프로필 업데이트** 바로 앞에 배치된 작업입니다. 작업에서 &quot;필드 1&quot;이 업데이트될 것으로 예상해서는 안 됩니다.
* 다음 **프로필 업데이트** 활동이 열거형으로 정의된 XDM 필드를 지원하지 않습니다.
* 다음 **[!UICONTROL 프로필 업데이트]** 활동은 다음만 업데이트합니다. [프로필 저장소](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html#profile-data-store){target="_blank"}, 데이터 레이크가 아님.
* 에서 데이터 세트를 선택할 때 **[!UICONTROL 프로필 업데이트]** 활동으로, 데이터 수집 흐름에서 타깃팅되지 않은 것을 사용하는 것이 좋습니다. 이유 **프로필 업데이트** 업데이트는 [프로필 저장소](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html#profile-data-store){target="_blank"}, 이러한 변경 사항을 데이터 수집 플로우로 덮어쓸 위험이 있습니다.

  또한 **프로필 업데이트** 활동 구성에는 id 네임스페이스가 필요하지 않습니다. 따라서 선택한 데이터 세트가 이 업데이트에서 사용할 ID 네임스페이스와 동일한 ID 네임스페이스를 여정을 시작한 작업에서 사용하도록 합니다. 선택한 데이터 세트에서 ID 맵을 사용할 수도 있습니다. 올바른 네임스페이스가 있는 데이터 집합 또는 ID 맵을 사용하는 데이터 집합을 선택하지 않으면 **프로필 업데이트** 활동이 실패합니다.



## 프로필 업데이트 사용

1. 이벤트로 시작하여 여정을 디자인합니다. 이 [섹션](../building-journeys/journey.md)을 참조하세요.

1. 다음에서 **작업** 팔레트의 섹션에서 **프로필 업데이트** 활동을 캔버스에 추가합니다.

   ![](assets/profileupdate0.png)

1. 목록에서 스키마를 선택합니다.

1. 클릭 **필드** 업데이트하려는 필드를 선택합니다. 필드는 하나만 선택할 수 있습니다.

   ![](assets/profileupdate2.png)

1. 목록에서 데이터 세트를 선택합니다.

   >[!NOTE]
   >
   >다음 **프로필 업데이트** 작업은 프로필 데이터를 실시간으로 업데이트하지만 데이터 세트는 업데이트하지 않습니다. 프로필이 데이터 세트와 관련된 레코드이므로 데이터 세트를 선택해야 합니다.

1. 을(를) 클릭합니다 **값** 사용할 값을 정의하는 필드:

   * 단순 표현식 편집기를 사용하여 데이터 소스 또는 수신 이벤트에서 필드를 선택할 수 있습니다.

     ![](assets/profileupdate4.png)

   * 특정 값을 정의하거나 고급 함수를 활용하려면 다음을 클릭하십시오. **고급 모드**.

     ![](assets/profileupdate3.png)

다음 **프로필 업데이트** 이제 가 구성되었습니다.

![](assets/profileupdate1.png)


## 테스트 모드 사용 {#using-the-test-mode}

테스트 모드에서는 프로필 업데이트가 시뮬레이트되지 않습니다. 업데이트가 테스트 프로필에서 수행됩니다.

테스트 프로필만 테스트 모드에서 여정에 들어갈 수 있습니다. 새 테스트 프로필을 만들거나 기존 프로필을 테스트 프로필로 만들 수 있습니다. Adobe Experience Platform에서 csv 파일 가져오기 또는 API 호출을 통해 프로필 속성을 업데이트할 수 있습니다. 간단한 방법은 **프로필 업데이트** 작업 활동 및 테스트 프로필 부울 필드를 false에서 true로 변경합니다.

기존 프로필을 테스트 프로필로 변환하는 방법에 대한 자세한 내용은 다음을 참조하십시오. [섹션](../audience/creating-test-profiles.md#create-test-profiles-csv).
