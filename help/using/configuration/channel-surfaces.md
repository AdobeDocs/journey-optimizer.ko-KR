---
solution: Journey Optimizer
product: journey optimizer
title: 채널 구성 설정
description: 채널 구성 구성 및 모니터링 방법 알아보기
feature: Surface, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: 채널, 표면, 기술, 매개변수, 최적기
exl-id: 9038528f-3da0-4e0e-9b82-b72c67b42391
source-git-commit: 8fb87d2e2085d98dd8b014df6aa4d734bab4e997
workflow-type: tm+mt
source-wordcount: '1721'
ht-degree: 2%

---

# 채널 구성 설정 {#set-up-channel-surfaces}

>[!CONTEXTUALHELP]
>id="ajo_admin_channel_surfaces"
>title="채널 구성"
>abstract="채널 구성은 시스템 관리자가 정의한 구성입니다. 여기에는 헤더 매개변수, 하위 도메인, 모바일 앱 등과 같이 메시지를 전송하기 위한 모든 기술 매개변수가 포함되어 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_admin_marketing_action"
>title="마케팅 액션"
>abstract="이 설정을 사용하여 메시지에 동의 정책을 연결하려면 마케팅 작업을 선택하십시오. 마케팅 액션에 연결된 모든 동의 정책은 고객의 선호도를 존중하는 데 사용됩니다."

[!DNL Journey Optimizer]을(를) 사용하면 메시지에 필요한 모든 기술 매개 변수(이메일 유형, 보낸 사람 전자 메일 및 이름, 모바일 앱, SMS 구성 등)를 정의하는 채널 구성(즉, 메시지 사전 설정)을 설정할 수 있습니다.

>[!CAUTION]
>
> * 채널 구성을 만들고 편집하고 삭제하려면 [메시지 사전 설정 관리](../administration/high-low-permissions.md#administration-permissions) 권한이 있어야 합니다.
>
> * 채널 구성을 만들기 전에 [이메일 구성](../email/get-started-email-config.md), [푸시 구성](../push/push-configuration.md), [SMS 구성](../sms/sms-configuration.md), [인앱 구성](../in-app/inapp-configuration.md), [코드 기반 구성](../code-based/code-based-configuration.md), [웹 구성](../web/web-configuration.md) 및 [DM 구성](../direct-mail/direct-mail-configuration.md) 단계를 수행해야 합니다.

채널 구성이 구성되면 여정 또는 캠페인에서 메시지를 만들 때 선택할 수 있습니다.

가이드 채널 설정을 사용하여 통합 환경에서 채널 설정을 자동화하고 유효성을 검사하여 Journey Optimizer 시작 프로세스 속도를 높일 수도 있습니다. [자세히 알아보기](set-mobile-config.md)

<!--
➡️ [Learn how to create and use email configurations in this video](#video-presets)
-->

## 채널 구성 만들기 {#create-channel-surface}

>[!CONTEXTUALHELP]
>id="ajo_admin_message_presets_header"
>title="채널 구성 설정"
>abstract="채널 구성을 설정할 때 적용되는 채널을 선택하고 이메일 유형, 발신자 이름, 모바일 앱, SMS 구성 등과 같이 전송에 필요한 모든 기술 매개 변수를 정의합니다."

>[!CONTEXTUALHELP]
>id="ajo_admin_message_presets"
>title="채널 구성 설정"
>abstract="여정 또는 캠페인의 이메일과 같은 작업을 만들려면 먼저 메시지에 필요한 모든 기술 설정을 정의하는 채널 구성을 만들어야 합니다. 채널 구성을 생성, 편집 및 삭제하려면 메시지 사전 설정 관리 권한이 있어야 합니다."

>[!CONTEXTUALHELP]
>id="ajo_surface_marketing_action"
>title="마케팅 액션 선택"
>abstract="동의 정책을 메시지에 연결하려면 구성에서 마케팅 작업을 선택하십시오."

채널 구성을 만들려면 다음 단계를 수행하십시오.

1. **[!UICONTROL 채널]** > **[!UICONTROL 일반 설정]** > **[!UICONTROL 채널 구성]** 메뉴에 액세스한 다음 **[!UICONTROL 채널 구성 만들기]**&#x200B;를 클릭하십시오.

   ![](assets/preset-create.png)

1. 구성의 이름 및 설명(선택 사항)을 입력한 다음 구성할 채널을 선택합니다.

   ![](assets/preset-general.png)

   >[!NOTE]
   >
   > 이름은 문자(A-Z)로 시작해야 합니다. 영숫자만 포함할 수 있습니다. 밑줄 `_`, 점`.` 및 하이픈 `-`자를 사용할 수도 있습니다.

1. 구성에 사용자 지정 또는 핵심 데이터 사용 레이블을 할당하려면 **[!UICONTROL 액세스 관리]**&#x200B;를 선택할 수 있습니다. [OLAC(개체 수준 액세스 제어)에 대해 자세히 알아보세요](../administration/object-based-access.md).

1. 채널을 선택합니다.

1. 이 구성을 사용하여 동의 정책을 메시지에 연결하려면 **[!UICONTROL 마케팅 액션]**&#x200B;을 선택하십시오. 마케팅 액션과 관련된 모든 동의 정책은 고객의 선호도를 존중하기 위해 활용됩니다. [자세히 알아보기](../action/consent.md#surface-marketing-actions)

   >[!NOTE]
   >
   >동의 정책은 현재 **Healthcare Shield** 및 **Privacy and Security Shield** 추가 기능 서비스를 구입한 조직에서만 사용할 수 있습니다.

   ![](assets/surface-marketing-action.png)

1. 모든 매개 변수가 구성되면 **[!UICONTROL 제출]**&#x200B;을 클릭하여 확인합니다. 채널 구성을 초안으로 저장하고 나중에 구성을 다시 시작할 수도 있습니다.

   ![](assets/preset-submit.png)

   >[!NOTE]
   >
   >선택한 IP 풀이 [편집](ip-pools.md#edit-ip-pool)(**[!UICONTROL 처리]** 상태) 아래에 있고 선택한 하위 도메인과 연결된 적이 없는 동안에는 전자 메일 구성 만들기를 진행할 수 없습니다. [자세히 알아보기](#subdomains-and-ip-pools)
   >
   >구성을 초안으로 저장하고 IP 풀이 **[!UICONTROL 성공]** 상태가 될 때까지 기다렸다가 구성 만들기를 다시 시작합니다.

1. 채널 구성이 만들어지면 목록에 **[!UICONTROL 처리 중]** 상태로 표시됩니다.

   이 단계에서는 제대로 구성되었는지 확인하기 위해 몇 가지 검사를 수행합니다. <!--The processing time is around **48h-72h**, and can take up to **7-10 business days**.-->

   >[!NOTE]
   > 하위 도메인에 대한 이메일 구성을 만들 때 처리 시간은 아래에 자세히 설명되어 있으므로 달라집니다.
   >
   > * **새 하위 도메인**&#x200B;의 경우 첫 번째 채널 구성을 만드는 데 **10분에서 10일**&#x200B;이 걸릴 수 있습니다.
   > * **비프로덕션 샌드박스**&#x200B;의 경우 또는 선택한 하위 도메인이 다른 승인된 채널 구성에서 **이미 사용**&#x200B;된 경우 프로세스는 최대 **3시간**&#x200B;만 소요됩니다.


   이러한 검사에는 Adobe 팀에서 수행되는 구성 및 기술 테스트가 포함됩니다.

   * SPF 유효성 검사
   * DKIM 유효성 검사
   * MX 레코드 유효성 검사
   * IP 확인 차단 목록에 추가
   * 호스트 확인 도움말
   * IP 풀 확인
   * A/PTR 기록, t/m/res 하위 도메인 확인
   * FBL 등록(이 검사는 지정된 하위 도메인에 대한 이메일 구성이 처음 생성될 때만 수행됩니다.)

   >[!NOTE]
   >
   >검사에 실패한 경우 [이 섹션](#monitor-channel-surfaces)에서 가능한 실패 이유에 대해 자세히 알아보세요.

1. 검사가 성공하면 채널 구성이 **[!UICONTROL 활성]** 상태가 됩니다. 메시지를 전달하는 데 사용할 준비가 되었습니다.

   ![](assets/preset-active.png)

## 채널 구성 모니터링 {#monitor-channel-surfaces}

모든 채널 구성이 **[!UICONTROL 채널]** > **[!UICONTROL 채널 구성]** 메뉴에 표시됩니다. 목록(채널, 사용자, 상태)을 검색하는 데 도움이 되는 필터를 사용할 수 있습니다.

![](assets/preset-filters.png)

채널 구성이 생성되면 다음과 같은 상태를 가질 수 있습니다.

* **[!UICONTROL 초안]**: 채널 구성이 초안으로 저장되었으며 아직 제출되지 않았습니다. 구성을 다시 시작하려면 여십시오.
* **[!UICONTROL 처리 중]**: 채널 구성이 제출되었으며 몇 가지 확인 단계를 거치고 있습니다.
* **[!UICONTROL 활성]**: 채널 구성이 확인되었으며 메시지를 만들도록 선택할 수 있습니다.
* **[!UICONTROL 실패]**: 채널 구성을 확인하는 동안 하나 이상의 검사를 수행하지 못했습니다.
* **[!UICONTROL 비활성화됨]**: 채널 구성이 비활성화되었습니다. 새 메시지를 만드는 데 사용할 수 없습니다.

채널 구성 만들기에 실패한 경우 각 가능한 실패 이유에 대한 자세한 내용은 아래에 설명되어 있습니다.

이러한 오류 중 하나가 발생하면 [고객 지원 Adobe](https://helpx.adobe.com/kr/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target="_blank"}에 연락하여 지원을 받으십시오.

* **SPF 유효성 검사 실패**: SPF(Sender Policy Framework)는 지정된 하위 도메인에서 전자 메일을 보낼 수 있는 승인된 IP를 지정할 수 있는 전자 메일 인증 프로토콜입니다. SPF 유효성 검사 실패는 SPF 레코드의 IP 주소가 사서함 공급자에게 전자 메일을 보내는 데 사용되는 IP 주소와 일치하지 않음을 의미합니다.

* **DKIM 유효성 검사 실패**: DKIM(DomainKeys Identified Mail)을 사용하면 받는 사람 서버에서 받은 메시지를 연결된 도메인의 실제 보낸 사람이 보냈는지 확인할 수 있으며 원본 메시지의 내용이 변경되지 않았는지 확인할 수 있습니다. DKIM 유효성 검사 실패는 수신 메일 서버에서 메시지 콘텐츠의 신뢰성 및 전송 도메인과의 연결을 확인할 수 없음을 의미합니다.

* **MX 레코드 유효성 검사 실패**: MX(Mail eXchange) 레코드 유효성 검사 실패는 지정된 하위 도메인을 대신하여 인바운드 전자 메일을 수락하는 메일 서버가 올바르게 구성되지 않았음을 의미합니다.

* **게재 구성 실패**: 다음 이유로 인해 게재 구성 실패가 발생할 수 있습니다.
   * 할당된 IP의 차단 목록에 추가
   * 잘못된 `helo` 이름
   * 해당 구성의 IP 풀에 지정된 IP 이외의 IP에서 전송 중인 이메일
   * 주요 ISP의 받은 편지함에 이메일을 게재할 수 없음

## 채널 구성 편집 {#edit-channel-surface}

채널 구성을 편집하려면 아래 단계를 따르십시오.

>[!NOTE]
>
>**[!UICONTROL 푸시 알림 설정]**&#x200B;을 편집할 수 없습니다. 푸시 알림 채널에 대해서만 채널 구성이 구성된 경우 편집할 수 없습니다.

1. 목록에서 채널 구성 이름을 클릭하여 엽니다.

   ![](assets/preset-name.png)

1. 원하는 대로 속성을 편집합니다.

   >[!NOTE]
   >
   >채널 구성의 상태가 **[!UICONTROL 활성]**&#x200B;인 경우 **[!UICONTROL 이름]**, **[!UICONTROL 채널 선택]** 및 **[!UICONTROL 하위 도메인]** 필드가 회색으로 표시되어 편집할 수 없습니다.

1. 변경 내용을 확인하려면 **[!UICONTROL 제출]**&#x200B;을 클릭하세요.

   >[!NOTE]
   >
   >채널 구성을 초안으로 저장하고 나중에 업데이트를 다시 시작할 수도 있습니다.

변경 사항이 제출되면 채널 구성은 [채널 구성을 만들 때](#create-channel-surface)에 적용된 것과 유사한 유효성 검사 주기를 거칩니다. 편집 처리 시간은 최대 **3시간**&#x200B;이 소요될 수 있습니다.

>[!NOTE]
>
>**[!UICONTROL 설명]**, **[!UICONTROL 전자 메일 형식]** 및/또는 **[!UICONTROL 전자 메일 다시 시도 매개 변수]** 필드만 편집하면 즉시 업데이트됩니다.

### 업데이트 세부 정보 {#update-details}

**[!UICONTROL 활성]** 상태인 채널 구성의 경우 업데이트 세부 정보를 확인할 수 있습니다. 방법은 다음과 같습니다.

활성 구성 이름 옆에 표시되는 **[!UICONTROL 최근 업데이트]** 아이콘을 클릭합니다.

![](assets/preset-recent-update-icon.png)

<!--You can also access the update details from an active channel configuration while update is in progress.-->

**[!UICONTROL 최근 업데이트]** 화면에서 업데이트 상태 및 요청된 변경 내용 목록과 같은 정보를 볼 수 있습니다.

<!--![](assets/preset-recent-update-screen.png)-->

### 업데이트 상태 {#update-statuses}

채널 구성 업데이트는 다음 상태를 가질 수 있습니다.

* **[!UICONTROL 처리 중]**: 채널 구성 업데이트가 제출되었으며 몇 가지 확인 단계를 거치고 있습니다.
* **[!UICONTROL 성공]**: 업데이트된 채널 구성이 확인되었으며 메시지를 만들도록 선택할 수 있습니다.
* **[!UICONTROL 실패]**: 채널 구성 업데이트를 확인하는 동안 하나 이상의 검사가 실패했습니다.

각 상태는 아래에 자세히 설명되어 있습니다.

#### 처리 중 {#surface-processing}

구성이 제대로 업데이트되었는지 확인하기 위해 몇 가지 게재 가능성 검사를 수행합니다.

>[!NOTE]
>
>**[!UICONTROL 설명]**, **[!UICONTROL 전자 메일 형식]** 및/또는 **[!UICONTROL 전자 메일 다시 시도 매개 변수]** 필드만 편집하면 즉시 업데이트됩니다.

처리 시간은 최대 **3시간**&#x200B;이 소요될 수 있습니다. [이 섹션](#create-channel-surface)에서 유효성 검사 주기 동안 수행되는 검사에 대해 자세히 알아보세요.

이미 활성화된 구성을 편집하는 경우:

* 유효성 검사 프로세스가 진행되는 동안 해당 상태는 **[!UICONTROL 활성]** 상태로 유지됩니다.

* 채널 구성 목록의 구성 이름 옆에 **[!UICONTROL 최근 업데이트]** 아이콘이 표시됩니다.

* 유효성 검사 프로세스 중에 이 구성을 사용하여 구성된 메시지는 여전히 이전 버전의 구성을 사용합니다.

>[!NOTE]
>
>업데이트가 진행되는 동안에는 채널 구성을 수정할 수 없습니다. 여전히 이름을 클릭할 수 있지만 모든 필드가 회색으로 표시됩니다. 업데이트에 성공할 때까지 변경 사항이 반영되지 않습니다.

#### 성공 {#success}

유효성 검사 프로세스가 성공하면 이 구성을 사용하는 모든 메시지에 구성의 새 버전이 자동으로 사용됩니다. 그러나 다음을 기다려야 할 수 있습니다.
* 단일 메시지에 소비되기 몇 분 전에
* 구성을 배치 메시지에 적용하기 위한 다음 배치까지.

#### 실패 {#failed}

유효성 검사 프로세스가 실패하면 이전 버전의 구성이 계속 사용됩니다.

[이 섹션](#monitor-channel-surfaces)에서 가능한 실패 이유에 대해 자세히 알아보세요.

업데이트 실패 시 구성을 다시 편집할 수 있게 됩니다. 이름을 클릭하고 수정해야 하는 설정을 업데이트할 수 있습니다.

## 채널 구성 비활성화 {#deactivate-a-surface}

새 메시지를 만드는 데 **[!UICONTROL 활성]** 채널 구성을 사용할 수 없게 하려면 비활성화하면 됩니다. 그러나 현재 이 구성을 사용하는 여정 메시지는 영향을 받지 않으며 계속 작동합니다.

>[!NOTE]
>
>업데이트를 처리하는 동안에는 채널 구성을 비활성화할 수 없습니다. 업데이트가 성공하거나 실패할 때까지 기다려야 합니다. [채널 구성 편집](#edit-channel-surface) 및 [업데이트 상태](#update-statuses)에 대해 자세히 알아보세요.

1. 채널 구성 목록에 액세스합니다.

1. 선택한 활성 구성을 보려면 **[!UICONTROL 추가 작업]** 단추를 클릭하십시오.

1. **[!UICONTROL 비활성화]**&#x200B;를 선택합니다.

   ![](assets/preset-deactivate.png)

>[!NOTE]
>
>이러한 구성을 사용하여 메시지를 보내는 여정에서 문제를 방지하기 위해 비활성화된 채널 구성을 삭제할 수 없습니다.

비활성화된 채널 구성은 직접 편집할 수 없습니다. 그러나 이를 복제하고 사본을 편집하여 새 메시지를 만드는 데 사용할 새 버전을 만들 수 있습니다. 다시 활성화할 수도 있으며 업데이트가 성공적으로 완료될 때까지 기다린 후 편집할 수도 있습니다.

![](assets/preset-activate.png)

<!--
## How-to video{#video-presets}

Learn how to create channel configurations, how to use them and how to delegate a subdomain and create an IP pool.

>[!VIDEO](https://video.tv.adobe.com/v/334343?quality=12)
-->
