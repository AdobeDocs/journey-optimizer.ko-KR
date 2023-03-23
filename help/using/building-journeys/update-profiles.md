---
solution: Journey Optimizer
product: journey optimizer
title: 프로필 업데이트
description: 여정에서 프로필 업데이트 활동을 사용하는 방법을 알아봅니다
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 프로필, 업데이트, 여정, 활동
exl-id: 8b2b2d1e-9bd1-439d-a15e-acdbab387c4b
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 9%

---

# 프로필 업데이트 {#update-profile}

>[!CONTEXTUALHELP]
>id="ajo_journey_update_profiles"
>title="프로필 활동 업데이트"
>abstract="프로필 업데이트 작업 활동을 사용하여 이벤트, 데이터 소스 또는 특정 값을 사용하여 도출하는 데이터로 기존 Adobe Experience Platform 프로필을 업데이트할 수 있습니다."

를 사용하십시오 **[!UICONTROL 프로필 업데이트]** 작업 활동을 통해 이벤트, 데이터 소스 또는 특정 값으로 기존 Adobe Experience Platform 프로필을 업데이트할 수 있습니다.

## 권장 사항

* 다음 **프로필 업데이트** 작업은 네임스페이스가 있는 이벤트로 시작하는 여정에서만 사용할 수 있습니다.
* 작업은 기존 필드만 업데이트하며 새 프로필 필드를 만들지 않습니다.
* 를 사용할 수 없습니다 **프로필 업데이트** 구매 등의 경험 이벤트를 생성하는 작업입니다.
* 다른 작업과 마찬가지로 오류 또는 시간 제한 시 대체 경로를 정의할 수 있으며 두 작업을 동시에 배치할 수 없습니다.
* Adobe Experience Platform에 전송된 업데이트 요청은 즉시/1초 내에 있습니다. 보통 몇 초 정도 걸리지만 가끔은 장담할 수 없는 경우도 있다. 따라서, 예를 들어 작업에서 **프로필 업데이트** 바로 전에 배치된 작업은 작업에서 &quot;필드 1&quot;이 업데이트되기를 기대하면 안 됩니다.
* 다음 **프로필 업데이트** 활동은 열거형으로 정의된 XDM 필드를 지원하지 않습니다.

## 프로필 업데이트 사용

1. 이벤트를 시작하여 여정을 디자인합니다. 이 [섹션](../building-journeys/journey.md)을 참조하세요.

1. 에서 **작업** 팔레트의 섹션에서 **프로필 업데이트** 활동을 캔버스로 이동합니다.

   ![](assets/profileupdate0.png)

1. 목록에서 스키마를 선택합니다.

1. 클릭 **필드** 을(를) 클릭하여 업데이트할 필드를 선택합니다. 필드를 하나만 선택할 수 있습니다.

   ![](assets/profileupdate2.png)

1. 목록에서 데이터 세트를 선택합니다.

   >[!NOTE]
   >
   >다음 **프로필 업데이트** 작업은 프로필 데이터를 실시간으로 업데이트하지만 데이터 세트는 업데이트하지 않습니다. 프로필이 데이터 세트와 관련된 레코드이므로 데이터 세트 선택이 필요합니다.

1. 을(를) 클릭합니다. **값** 필드를 사용하여 사용할 값을 정의합니다.

   * 단순 표현식 편집기를 사용하여 데이터 소스 또는 수신 이벤트에서 필드를 선택할 수 있습니다.

      ![](assets/profileupdate4.png)

   * 특정 값을 정의하거나 고급 함수를 활용하려면 **고급 모드**.

      ![](assets/profileupdate3.png)

다음 **프로필 업데이트** 이제 가 구성되었습니다.

![](assets/profileupdate1.png)


## 테스트 모드 사용 {#using-the-test-mode}

테스트 모드에서는 프로필 업데이트가 시뮬레이션되지 않습니다. 업데이트는 테스트 프로필에서 수행됩니다.

테스트 프로필만 테스트 모드에서 여정에 들어갈 수 있습니다. 새 테스트 프로필을 만들거나 기존 프로필을 테스트 프로필로 전환할 수 있습니다. Adobe Experience Platform에서 csv 파일 가져오기 또는 API 호출을 통해 프로필 속성을 업데이트할 수 있습니다. 간단한 방법은 **프로필 업데이트** 작업 활동을 수행하고 테스트 프로필 부울 필드를 false에서 true로 변경합니다.

기존 프로필을 테스트 프로필로 변환하는 방법에 대한 자세한 내용은 다음 문서를 참조하십시오 [섹션](../segment/creating-test-profiles.md#create-test-profiles-csv).
