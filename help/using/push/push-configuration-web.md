---
solution: Journey Optimizer
product: journey optimizer
title: 푸시 알림 구성
description: Journey Optimizer을 사용하여 푸시 알림을 전송하도록 환경을 구성하는 방법 알아보기
feature: Push, Channel Configuration
role: Admin
level: Intermediate
hidefromtoc: true
hide: true
source-git-commit: 0706cb23bb41aff56984d7723df22c5a07bbe51d
workflow-type: tm+mt
source-wordcount: '1076'
ht-degree: 6%

---

# 웹 푸시 알림 채널 구성 {#push-notification-configuration}

[!DNL Journey Optimizer]에서는 여정을 만들고 타겟팅한 대상자에게 메시지를 보낼 수 있습니다. [!DNL Journey Optimizer]을(를) 사용하여 웹 푸시 알림을 전송하기 전에 Adobe Experience Platform에 구성 및 통합이 제대로 되어 있는지 확인해야 합니다. [!DNL Adobe Journey Optimizer]의 푸시 알림 데이터 흐름을 파악하려면 [이 페이지](push-gs.md)를 참조하십시오.

>[!AVAILABILITY]
>
>이제 새 **모바일 온보딩 빠른 시작 워크플로우**&#x200B;를 사용할 수 있습니다. 이 새로운 제품 기능을 사용하여 모바일 이벤트 데이터 수집 및 유효성 검사를 시작하고 모바일 푸시 알림을 전송할 모바일 SDK을 신속하게 구성할 수 있습니다. 이 기능은 데이터 수집 홈 페이지를 통해 공개 베타로 액세스할 수 있습니다. [자세히 알아보기](mobile-onboarding-wf.md)
>

## 시작하기 전 {#start-push}

### 권한 설정 {#setup-permissions}

모바일 애플리케이션을 만들기 전에 먼저 Adobe Experience Platform의 태그에 대한 올바른 사용자 권한이 있는지 확인하거나 사용자에게 할당해야 합니다. 자세한 내용은 [태그 설명서](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/user-permissions.html){target="_blank"}를 참조하세요.

>[!CAUTION]
>
>푸시 구성은 전문가 사용자가 수행해야 합니다. 구현 모델 및 이 구현에 관련된 담당자에 따라 단일 제품 프로필에 전체 권한 집합을 할당하거나 앱 개발자와 **Adobe Journey Optimizer** 관리자 간에 권한을 공유해야 할 수 있습니다. **이 설명서**&#x200B;에서 [태그](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/user-permissions.html){target="_blank"} 권한에 대해 자세히 알아보세요.

<!--ou need to your have access to perform following roles :

* Manage Datastreams
* Manage Client-side Properties
* Manage App Configurations
-->

**속성** 및 **회사** 권한을 할당하려면 아래 단계를 따르십시오.

1. **[!DNL Admin Console]**&#x200B;에 액세스합니다.

1. **[!UICONTROL 제품]** 탭에서 **[!UICONTROL Adobe Experience Platform 데이터 수집]** 카드를 선택합니다.

   ![](assets/push_product_1.png)

1. 기존 **[!UICONTROL 제품 프로필]**&#x200B;을 선택하거나 **[!UICONTROL 새 프로필]** 버튼을 사용하여 새 프로필을 만드십시오. **[!UICONTROL Admin Console 설명서]**&#x200B;에서 새 [새 프로필](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/create-profile.html#ui){target="_blank"}을 만드는 방법을 알아보세요.

1. **[!UICONTROL 권한]** 탭에서 **[!UICONTROL 속성 권한]**&#x200B;을 선택합니다.

   ![](assets/push_product_2.png)

1. **[!UICONTROL 모두 추가]**&#x200B;를 클릭합니다. 이렇게 하면 제품 프로필에 다음 권한이 추가됩니다.
   * **[!UICONTROL 승인]**
   * **[!UICONTROL 개발]**
   * **[!UICONTROL 환경 관리]**
   * **[!UICONTROL 확장 관리]**
   * **[!UICONTROL 게시]**

   Adobe Experience Platform Mobile SDK에서 Adobe Journey Optimizer 확장을 설치 및 게시하고 앱 속성을 게시하려면 이러한 권한이 필요합니다.

1. 그런 다음 왼쪽 메뉴에서 **[!UICONTROL 회사 권한]**&#x200B;을 선택합니다.

   ![](assets/push_product_4.png)

1. 다음 권한을 추가합니다.

   * **[!UICONTROL 앱 구성 관리]**
   * **[!UICONTROL 속성 관리]**

   이러한 권한은 모바일 앱 개발자가 **Adobe Experience Platform 데이터 수집**&#x200B;에서 푸시 자격 증명을 설정하고 **Adobe Journey Optimizer**&#x200B;에서 푸시 알림 채널 구성(즉, 메시지 사전 설정)을 정의하는 데 필요합니다.

   ![](assets/push_product_5.png)

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

이 **[!UICONTROL 제품 프로필]**&#x200B;을 사용자에게 할당하려면 아래 단계를 따르십시오.

1. **[!DNL Admin Console]**&#x200B;에 액세스합니다.

1. **[!UICONTROL 제품]** 탭에서 **[!UICONTROL Adobe Experience Platform 데이터 수집]** 카드를 선택합니다.

1. 이전에 구성한 **[!UICONTROL 제품 프로필]**&#x200B;을 선택하세요.

1.  **[!UICONTROL 사용자]** 탭에서 **[!UICONTROL 사용자 추가]**&#x200B;를 클릭합니다.

   ![](assets/push_product_6.png)

1. 사용자의 이름 또는 이메일 주소를 입력하고 사용자를 선택합니다. 그런 다음 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

   >[!NOTE]
   >
   >사용자가 이전에 Admin Console에서 만들어진 것이 아니라면 [사용자 추가 설명서](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html#add-users)를 참조하세요.

   ![](assets/push_product_7.png)


### 데이터 세트 확인 {#push-datasets}

푸시 알림 채널에서는 다음 스키마 및 데이터 세트를 사용할 수 있습니다.

| 스키마 <br>데이터 집합 | 필드 그룹 | 작업 |
| -------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------- |
| CJM 푸시 프로필 스키마 <br>CJM 푸시 프로필 데이터 세트 | 푸시 알림 세부 정보<br>Adobe CJM ExperienceEvent - 메시지 프로필 세부 정보<br>Adobe CJM ExperienceEvent - 메시지 실행 세부 정보<br>애플리케이션 세부 정보<br>환경 세부 정보 | 푸시 토큰 등록 |
| CJM 푸시 추적 경험 이벤트 스키마<br>CJM 푸시 추적 경험 이벤트 데이터 세트 | 푸시 알림 추적 | 상호 작용 추적 및 보고 UI에 대한 데이터 제공 |


>[!NOTE]
>
>푸시 추적 이벤트가 CJM 푸시 추적 경험 이벤트 데이터 세트에 수집되면 데이터가 부분적으로 성공적으로 수집되더라도 일부 오류가 발생할 수 있습니다. 이 문제는 매핑의 일부 필드가 수신 이벤트에 없는 경우 발생할 수 있습니다. 시스템에서 경고를 기록하지만 데이터의 유효한 부분에 대한 수집은 금지하지 않습니다. 이러한 경고는 일괄 처리 상태에서 &#39;실패&#39;로 표시되지만 부분 수집 성공을 반영합니다.
>
>각 스키마의 전체 필드와 속성 목록을 보려면 [Journey Optimizer 스키마 사전](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=ko){target="_blank"}을 찾아봅니다.

### pushNotification 속성 구성 {#push-property}

**웹 푸시 알림**&#x200B;을 사용하려면 먼저 [pushNotifications 속성](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/pushnotifications)이 웹 SDK 내에서 올바르게 구성되어 있는지 확인해야 합니다. 이 속성은 웹 애플리케이션에서 푸시 알림을 처리하는 방법을 제어합니다.

또한 Journey Optimizer에서 [앱 푸시 자격 증명](#push-credentials-launch)을 구성하는 데 필요한 VAPID 키를 생성해야 합니다.

## 1단계: Journey Optimizer에서 앱 푸시 자격 증명 추가 {#push-credentials-launch}

올바른 사용자 권한을 부여한 후 이제 Journey Optimizer에서 모바일 애플리케이션 푸시 자격 증명을 추가해야 합니다.

Adobe이 사용자를 대신하여 푸시 알림을 전송하도록 승인하려면 모바일 앱 푸시 자격 증명 등록이 필요합니다. 아래에 자세히 설명된 단계를 참조하십시오.

1. **[!UICONTROL 채널]** > **[!UICONTROL 푸시 설정]** > **[!UICONTROL 푸시 자격 증명]** 메뉴에 액세스합니다.

1. **[!UICONTROL 푸시 자격 증명 만들기]**&#x200B;를 클릭합니다.

1. **[!UICONTROL 플랫폼]** 드롭다운에서 **[!UICONTROL 웹]**&#x200B;을 선택합니다.

   ![](assets/add-app-config-web.png)

1. **[!UICONTROL 앱 ID]**&#x200B;를 제공하십시오.

1. **[!UICONTROL VAPID 공개 키]** 및 **[!UICONTROL 개인 키]**&#x200B;를 입력하십시오.

1. 앱 구성을 만들려면 **[!UICONTROL 제출]**&#x200B;을 클릭합니다.

## 2단계: 푸시할 채널 구성 만들기{#message-preset}

푸시 자격 증명을 만든 후에는 **[!DNL Journey Optimizer]**&#x200B;에서 푸시 알림을 전송할 수 있는 구성을 만들어야 합니다.

1. **[!UICONTROL 채널]** > **[!UICONTROL 일반 설정]** > **[!UICONTROL 채널 구성]** 메뉴에 액세스한 다음 **[!UICONTROL 채널 구성 만들기]**&#x200B;를 클릭하십시오.

   ![](assets/push-config-9.png)

1. 구성의 이름 및 설명(선택 사항)을 입력합니다.

   >[!NOTE]
   >
   > 이름은 문자(A-Z)로 시작해야 합니다. 영숫자만 포함할 수 있습니다. 밑줄 `_`, 점 `.`, 하이픈 `-`도 사용할 수 있습니다.


1. 구성에 사용자 지정 또는 핵심 데이터 사용 레이블을 할당하려면 **[!UICONTROL 액세스 관리]**&#x200B;를 선택할 수 있습니다. [OLAC(개체 수준 액세스 제어)에 대해 자세히 알아보세요](../administration/object-based-access.md).

1. **푸시** 채널을 선택하십시오.

   ![](assets/push-config-10.png)

1. 이 구성을 사용하여 동의 정책을 메시지에 연결하려면 **[!UICONTROL 마케팅 액션]**&#x200B;을 선택하십시오. 마케팅 액션과 관련된 모든 동의 정책은 고객의 선호도를 존중하기 위해 활용됩니다. [자세히 알아보기](../action/consent.md#surface-marketing-actions)

1. **[!UICONTROL 플랫폼]**: Android, iOS 및/또는 웹을 선택하세요.

1. 위에 구성된 **[!UICONTROL 푸시 자격 증명]**&#x200B;과 동일한 [앱 ID](#push-credentials-launch)을(를) 선택하십시오.

1. 변경 내용을 저장합니다.

이제 푸시 알림을 만들 때 구성을 선택할 수 있습니다.

## 3단계: sendPushSubscription 속성 구성 {#sendPushSubscription-property}

푸시 자격 증명과 채널 구성이 설정되면 웹 애플리케이션에서 [sendPushSubscription 명령](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/sendpushsubscription)을 구현해야 합니다. 이 명령은 사용자 푸시 구독을 Adobe Experience Platform에 등록하여 시스템에서 푸시 알림을 받도록 선택한 사용자를 추적하고 구독 상태를 유지할 수 있습니다. 이 등록은 Journey Optimizer이 타깃팅된 푸시 알림을 사용자에게 전송하는 데 필수적입니다.

## 4단계: 이벤트로 모바일 앱 테스트 {#mobile-app-test}

Adobe Experience Platform 및 [!DNL Adobe Experience Platform Data Collection]에서 웹 푸시 구성을 완료한 후 웹 푸시 알림을 프로필로 전송하기 전에 구현을 테스트할 수 있습니다. 테스트를 통해 구독이 제대로 등록되고 알림이 사용자의 브라우저에 올바르게 전달되는지 확인할 수 있습니다.

웹 푸시 설정의 유효성을 확인하기 위해 이벤트를 사용하여 테스트 여정을 만드는 방법에 대한 자세한 지침은 모바일 및 웹 푸시 채널 모두에 적용할 수 있는 포괄적인 테스트 워크플로를 제공하는 [모바일 앱 푸시 알림 구성 설명서](push-configuration.md)를 참조하십시오.
