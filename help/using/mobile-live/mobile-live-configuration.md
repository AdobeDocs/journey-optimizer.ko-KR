---
solution: Journey Optimizer
product: journey optimizer
title: 라이브 활동 채널 구성
description: Journey Optimizer을 사용하여 라이브 활동을 전송하도록 환경을 구성하는 방법에 대해 알아봅니다.
feature: Channel Configuration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: ce6bfca78d097588b5958c10c721b29b7013b3e2
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 2%

---

# 라이브 활동 구성 시작 {#mobile-live-config}

>[!BEGINSHADEBOX]

* [라이브 활동 시작](get-started-mobile-live.md)
* **[라이브 활동 구성](mobile-live-configuration.md)**
* [Adobe Experience Platform Mobile SDK과 라이브 활동 통합](mobile-live-configuration-sdk.md)
* [라이브 활동 만들기](create-mobile-live.md)
* [자주 묻는 질문](mobile-live-faq.md)
* [라이브 활동 캠페인 보고서](../reports/campaign-global-report-cja-activity.md)

>[!ENDSHADEBOX]

라이브 활동을 보내기 전에 Adobe Journey Optimizer 환경을 구성해야 합니다. 다음을 수행하십시오.

## 1단계: Journey Optimizer에서 앱 푸시 자격 증명 추가(선택 사항){#push-credentials-launch}

Adobe이 사용자를 대신하여 푸시 알림을 전송하도록 승인하려면 모바일 앱 푸시 자격 증명 등록이 필요합니다.

푸시 자격 증명이 이미 구성된 경우 1단계는 선택 사항이며, 이는 라이브 활동 채널 구성에 다시 사용할 수 있기 때문입니다. 자격 증명이 정의되지 않은 경우 앱에 대한 새 푸시 자격 증명을 만들어야 합니다. 아래에 자세히 설명된 단계를 참조하십시오.

1. **[!UICONTROL 채널]** > **[!UICONTROL 푸시 설정]** > **[!UICONTROL 푸시 자격 증명]** 메뉴에 액세스합니다.

1. **[!UICONTROL 푸시 자격 증명 만들기]**&#x200B;를 클릭합니다.

   ![](assets/credential-1.png)

1. **[!UICONTROL 플랫폼]** 드롭다운에서 운영 체제를 선택합니다.

1. 모바일 앱 **[!UICONTROL 앱 ID]**&#x200B;를 입력하세요.

   ![](assets/credential-2.png)

1. **[!UICONTROL 모든 샌드박스에 적용]** 옵션을 활성화하여 모든 샌드박스에서 푸시 자격 증명을 사용할 수 있도록 합니다. 특정 샌드박스에 동일한 플랫폼 및 앱 ID 쌍에 대한 자체 자격 증명이 있는 경우 해당 샌드박스별 자격 증명이 우선합니다.

1. 자격 증명을 추가하려면 **[!UICONTROL 푸시 자격 증명 수동 입력]** 단추를 켭니다.

1. .p8 Apple 푸시 알림 인증 키 파일을 끌어서 놓습니다. 이 키는 **인증서**, **식별자** 및 **프로필** 페이지에서 가져올 수 있습니다.

1. **키 ID**&#x200B;을(를) 제공합니다. p8 인증 키를 만드는 동안 할당된 10개의 문자열입니다. **인증서**, **식별자** 및 **프로필** 페이지의 **키** 탭에서 찾을 수 있습니다.

1. **팀 ID**&#x200B;를 제공하십시오. 멤버십 탭에서 찾을 수 있는 문자열 값입니다.

1. 앱 구성을 만들려면 **[!UICONTROL 제출]**&#x200B;을 클릭합니다.

## 2단계: 라이브 활동 구성 만들기 {#config-live-activity}

1. 왼쪽 레일에서 **[!UICONTROL 관리]** > **[!UICONTROL 채널]**(으)로 이동한 다음 **[!UICONTROL 일반 설정]** > **[!UICONTROL 채널 구성]**&#x200B;을 선택합니다. **[!UICONTROL 채널 구성 만들기]** 단추를 클릭합니다.

   ![](assets/config-1.png)

1. 구성의 이름 및 설명(선택 사항)을 입력한 다음 WhatsApp 채널을 선택합니다.

   >[!NOTE]
   >
   > 이름은 문자(A-Z)로 시작해야 합니다. 영숫자만 포함할 수 있습니다. 밑줄 `_`, 점 `.`, 하이픈 `-`도 사용할 수 있습니다.

1. **[!DNL Live activity]**&#x200B;을(를) 채널로 선택합니다.

   ![](assets/config-2.png)

1. 이 구성을 사용하여 동의 정책을 메시지에 연결하려면 **[!UICONTROL 마케팅 액션]**&#x200B;을 선택하세요. 마케팅 액션과 관련된 모든 동의 정책은 고객의 선호도를 존중하기 위해 활용됩니다. 자세히 알아보기

1. iOS을 **[!UICONTROL 플랫폼]**(으)로 선택합니다.

1. 드롭다운에서 위에 구성된 **[!UICONTROL 푸시 자격 증명]**&#x200B;과 동일한 [앱 ID](#push-credentials-launch)을 선택하거나 기존 ID를 선택합니다.

   ![](assets/config-3.png)

1. 모든 매개 변수가 구성되면 **[!UICONTROL 제출]**&#x200B;을 클릭하여 확인합니다. 채널 구성을 초안으로 저장하고 나중에 구성을 다시 시작할 수도 있습니다.

1. 채널 구성이 만들어지면 목록에 **[!UICONTROL 처리 중]** 상태로 표시됩니다.

   >[!NOTE]
   >
   >검사에 실패한 경우 [이 섹션](../configuration/channel-surfaces.md)에서 가능한 실패 이유에 대해 자세히 알아보세요.

1. 검사가 성공하면 채널 구성이 **[!UICONTROL 활성]** 상태가 됩니다. 메시지를 전달하는 데 사용할 준비가 되었습니다.

이제 Adobe Experience Platform Mobile SDK과의 통합을 시작하여 잠금 화면 및 Dynamic Island에서 실시간 동적 업데이트를 활성화할 수 있습니다.

➡️ [Adobe Experience Platform Mobile SDK 통합에 대해 자세히 알아보기](mobile-live-configuration-sdk.md)
