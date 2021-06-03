---
title: 메시지 사전 설정 만들기
description: 이메일 및 푸시 알림 메시지 사전 설정을 만드는 방법을 알아봅니다
source-git-commit: 4353b8f01bb4e47f6f2384e464341c0ee80ecaf2
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 0%

---


# 메시지 사전 설정 만들기

[!DNL Journey Optimizer]을(를) 사용하여 이메일 및 푸시 알림 메시지에 필요한 모든 기술 매개 변수(이메일 유형, 보낸 사람 이메일 및 이름, 모바일 앱 등)를 정의하는 메시지 사전 설정을 설정할 수 있습니다.

통신해야 하는 다양한 브랜드에 따라 원하는 만큼 메시지 사전 설정을 설정할 수 있습니다.

메시지 사전 설정이 구성되면 **[!UICONTROL Presets]** 목록에서 메시지를 만들 때 메시지 사전 설정을 선택할 수 있습니다.

## 메시지 사전 설정 {#create-message-preset} 만들기

메시지 사전 설정을 만들려면 다음 단계를 수행합니다.

1. **[!UICONTROL Channels]** / **[!UICONTROL Message presets]** 메뉴에 액세스한 다음 **[!UICONTROL Create Message preset]** 를 클릭합니다.

   ![](../assets/preset-create.png)

1. 사전 설정에 대한 이름과 설명(선택 사항)을 제공한 다음, 구성할 채널을 지정합니다.

   ![](../assets/preset-general.png)

1. 전자 메일 및 푸시 알림 설정을 구성합니다.

   전자 메일 채널의 경우 다음을 지정합니다.

   * 사전 설정된(트랜잭션 또는 마케팅 메시지)와 함께 보낼 커뮤니케이션 유형입니다.
   * 전자 메일을 보내는 데 사용할 [하위 도메인](about-subdomain-delegation.md)
   * 사전 설정과 연결할 [IP 풀](ip-pools.md)
   * 사전 설정을 사용하여 보낸 이메일에 사용할 헤더 매개 변수입니다.

   ![](../assets/preset-email.png)

   푸시 알림 채널의 경우 메시지에 사용할 IOS 및/또는 Android 모바일 애플리케이션을 지정합니다. 푸시 알림을 전송하도록 환경을 구성하는 방법에 대한 자세한 내용은 [이 섹션](../push-configuration.md)을 참조하십시오.

   ![](../assets/preset-push.png)

1. 모든 매개 변수가 구성되면 **[!UICONTROL Submit]** 을 클릭하여 확인합니다. 메시지 사전 설정을 초안으로 저장하고 나중에 구성을 다시 시작할 수도 있습니다.

   ![](../assets/preset-submit.png)

1. 메시지 사전 설정이 만들어지면 목록에 **[!UICONTROL Processing]** 상태가 표시됩니다.

   이 단계에서는 구성이 올바른지 확인하기 위해 몇 가지 확인이 수행됩니다. 처리 시간은 48시간~72시간 이며 최대 7~10일이 소요될 수 있습니다.

   이러한 검사에는 Adobe 게재 가능성 팀이 수행하는 게재 가능성 테스트가 포함됩니다.

   * SPF 유효성 검사,
   * DKIM 검증,
   * MX 레코드 유효성 검사,
   * IP 블랙리스트 확인,
   * 헬로 호스트 검사,
   * IP 풀 확인,
   * A/PTR 레코드, t/m/res 하위 도메인 확인.

1. 확인이 성공하면 메시지 사전 설정이 **[!UICONTROL Active]** 상태를 가져옵니다. 메시지를 전달하는 데 사용할 준비가 되었습니다.

   <!-- later on, users will be notified in Pulse -->

   ![](../assets/preset-active.png)

## 메시지 사전 설정 모니터링

모든 메시지 사전 설정이 **[!UICONTROL Channels]** / **[!UICONTROL Message presets]** 메뉴에 표시됩니다. 필터를 사용하여 목록(채널 유형, 사용자, 상태)을 검색할 수 있습니다.

![](../assets/preset-filters.png)

메시지 사전 설정에는 다음 상태가 있을 수 있습니다.

* **[!UICONTROL Draft]**:메시지 사전 설정이 초안으로 저장되었으며 아직 제출되지 않았습니다. 구성을 다시 시작하려면 엽니다.
* **[!UICONTROL Processing]**:메시지 사전 설정이 제출되었으며 몇 가지 확인 단계를 수행하고 있습니다.
* **[!UICONTROL Active]**:메시지 사전 설정이 확인되었으며 메시지를 만들기 위해 선택할 수 있습니다.
* **[!UICONTROL Failed]**:메시지 사전 설정 확인 중에 하나 또는 여러 개의 검사가 실패했습니다.
* **[!UICONTROL De-activated]**:메시지 사전 설정이 비활성화 되었습니다. 새 메시지를 만드는 데 사용할 수 없습니다.

## 메시지 사전 설정 편집

메시지 사전 설정을 편집하려면 먼저 메시지 사전 설정을 비활성화하여 새 메시지를 만들 수 없도록 해야 합니다(이 사전 설정을 사용하여 게시된 메시지는 영향을 받지 않으며 계속 작동합니다). 그런 다음 메시지 사전 설정을 복제하여 새 메시지를 만드는 데 사용할 새 버전을 만들어야 합니다.

1. 메시지 사전 설정 목록에 액세스한 다음 편집할 메시지 사전 설정을 비활성화합니다.

   ![](../assets/preset-deactivate.png)

1. 비활성화된 메시지 사전 설정을 복제합니다. **[!UICONTROL Draft]** 상태의 복사본이 목록에 자동으로 추가됩니다.

   ![](../assets/preset-duplicated.png)

1. 복제한 메시지 사전 설정을 열고 필요에 따라 수정한 다음 변경 사항을 제출합니다. 메시지 사전 설정은 [작성 단계](#create-message-preset)와 동일한 유효성 검사 주기를 따릅니다.

1. 유효성이 확인되면 **[!UICONTROL Active]** 상태가 되고 새 메시지를 만드는 데 사용할 준비가 되었습니다.

   >[!NOTE]
   >
   >메시지를 보내기 위해 이러한 사전 설정을 사용하는 여정에서 문제를 방지하기 위해 비활성화 메시지 사전 설정을 삭제할 수 없습니다.