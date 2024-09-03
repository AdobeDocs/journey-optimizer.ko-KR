---
solution: Journey Optimizer
product: journey optimizer
title: 채널 설정 만들기
description: 채널 설정을 만드는 방법을 알아봅니다
feature: Surface, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: 채널, 표면, 기술, 매개변수, 최적기
source-git-commit: 77e2892dc188ebdd79031792434b4f55913ee811
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 39%

---

# 채널 설정 만들기 {#set-mobile-ios}

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_javascript_code"
>title="Javascript 코드"
>abstract="헤드 태그에는 웹 페이지의 기본 콘텐츠 전에 로드되는 필수 메타데이터와 리소스가 포함되어 있습니다. 이 섹션에 코드를 배치하면 코드가 적절하게 초기화되고 조기에 실행되어 웹 페이지가 효율적으로 로드되고 기능할 수 있습니다. head 섹션에 코드를 추가하면 사이트의 구조, 성능 및 전반적인 사용자 경험을 향상시킬 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_push_token"
>title="디바이스 토큰 가져오기"
>abstract="디바이스의 푸시 토큰이 Adobe Experience Platform 프로필과 제대로 동기화되도록 하려면 다음 코드를 애플리케이션에 통합해야 합니다. 이러한 통합은 최신 커뮤니케이션 기능을 유지하고 원활한 사용자 경험을 보장하는 데 필수적입니다."

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_push_xcode"
>title="Xcode에서 애플리케이션 실행"
>abstract="푸시 토큰을 얻으려면 먼저 Xcode를 사용하여 애플리케이션을 실행합니다. 애플리케이션이 시작된 후 다시 시작하여 유효성 검사 프로세스가 완료되었는지 확인합니다. 그러면 Adobe에서 유효성 검사 결과의 일부로 푸시 토큰을 제공합니다. 이 토큰은 푸시 알림을 활성화하는 데 필수적이며 설정이 성공적으로 검증되면 표시됩니다."

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_push_certificate_fcm"
>title="푸시 인증서 입력"
>abstract=".json 비공개 키 파일을 끌어다 놓습니다. 이 파일에는 애플리케이션과 서버 간의 안전한 통합 및 통신에 필요한 인증 정보가 포함되어 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_push_certificate"
>title="푸시 인증서 입력"
>abstract=".p8 키 파일에는 안전한 푸시 알림을 위해 Apple 서버에서 앱을 인증하는 데 사용되는 비공개 키가 포함되어 있습니다. 개발자 계정의 인증서, 식별자 및 프로필 페이지에서 이 키를 얻을 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_push_key_id"
>title="키 ID"
>abstract="p8 인증 키를 만드는 동안 할당된 10자리 문자열인 키 ID는 개발자 계정의 인증서, 식별자 및 프로필 페이지의 **키** 탭 아래에서 찾을 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_push_team_id"
>title="팀 ID"
>abstract="팀을 식별하는 데 사용되는 문자열 값인 팀 ID는 개발자 계정의 **멤버십** 탭에서 찾을 수 있습니다."


이 설정을 사용하면 마케팅 채널의 빠른 구성이 간소화되어 Experience Platform, Journey Optimizer 및 데이터 수집 앱에서 모든 필수 리소스를 쉽게 사용할 수 있습니다. 이렇게 하면 마케팅 팀이 캠페인 및 여정 만들기를 빠르게 시작할 수 있습니다.

1. Journey Optimizer 홈페이지에서 **[!UICONTROL 모바일 및 웹 채널 설정]** 카드에서 **[!UICONTROL 시작]**&#x200B;을 클릭합니다.

   ![](assets/guided-setup-config-1.png)

1. **[!UICONTROL 새]** 구성을 만듭니다.

   기존 구성이 있는 경우 하나를 선택하거나 새 구성을 만들 수 있습니다.

   ![](assets/guided-setup-config-2.png)

1. 새 구성에 대한 **[!UICONTROL 이름]**&#x200B;을(를) 입력하고 **[!UICONTROL 데이터 스트림]**&#x200B;을(를) 선택하거나 만드세요. 이 **[!UICONTROL 이름]**&#x200B;은(는) 자동으로 만든 모든 리소스에 사용됩니다.

1. 조직에 여러 데이터 스트림이 있는 경우 기존 옵션 중에서 하나를 선택하십시오. 데이터 스트림이 없는 경우 자동으로 만들어집니다.

1. 플랫폼을 선택하고 **[!UICONTROL 리소스 자동 만들기]**&#x200B;를 클릭합니다.

1. 설치 프로세스를 간소화하기 위해 시작하는 데 도움이 되는 필수 리소스가 자동으로 생성됩니다. 여기에는 새 **[!UICONTROL Mobile 태그 속성]**&#x200B;을 만들고 확장을 설치하는 작업이 포함됩니다.

[자동 생성된 리소스에 대한 자세한 정보](set-mobile-config.md#auto-create-resources)

1. 리소스 생성이 완료되면 사용자 인터페이스의 지침에 따라 SDK 및 채널을 설정하고 확인합니다.

1. 구성을 완료한 후 자동 생성된 **[!UICONTROL 채널 구성]**&#x200B;을(를) 여정 및 캠페인 생성을 담당하는 팀원과 공유합니다.

   ![](assets/guided-setup-config-ios-8.png){zoomable="yes"}

1. 이제 캠페인 또는 여정 인터페이스에서 **[!UICONTROL 채널 구성]**&#x200B;을(를) 참조할 수 있으므로 설정과 타깃팅된 여정 및 캠페인의 실행 간에 원활한 연결이 가능합니다.

## 모바일 기존 구성 수정 {#reconnect}

구성을 만든 후 언제든지 쉽게 다시 방문하여 채널을 추가하거나 필요에 따라 추가 조정할 수 있습니다

1. Journey Optimizer 홈페이지에서 **[!UICONTROL 모바일 및 웹 채널 설정]** 카드에서 **[!UICONTROL 시작]**&#x200B;을 클릭합니다.

   ![](assets/guided-setup-config-1.png)

1. **[!UICONTROL 기존]**&#x200B;을(를) 선택하고 드롭다운에서 기존 **[!UICONTROL Tag 속성]**&#x200B;을(를) 선택합니다.

   ![](assets/guided-setup-config-ios-9.png)

1. 기존 구성에 액세스할 때는 Adobe 보증을 사용하여 다시 연결해야 합니다. SDK 설정 메뉴에서 **[!UICONTROL 다시 연결]**&#x200B;을 클릭합니다.

   ![](assets/guided-setup-config-ios-10.png)

1. **[!UICONTROL 사용 가능한 장치]** 드롭다운에서 장치를 선택하고 **[!UICONTROL 연결]**&#x200B;을 클릭합니다.

   ![](assets/guided-setup-config-ios-11.png){zoomable="yes"}

1. 이제 필요에 따라 구성을 업데이트할 수 있습니다.

