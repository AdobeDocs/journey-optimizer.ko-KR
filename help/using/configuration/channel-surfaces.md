---
solution: Journey Optimizer
product: journey optimizer
title: 채널 표면 설정
description: 채널 표면 구성 및 모니터링 방법 알아보기
feature: Application Settings, Surface
topic: Administration
role: Admin
level: Intermediate
keywords: 채널, 표면, 기술, 매개변수, 최적기
exl-id: 9038528f-3da0-4e0e-9b82-b72c67b42391
source-git-commit: 9555c37f8bac295a668f64990e229c6e0e5ceb8d
workflow-type: tm+mt
source-wordcount: '1607'
ht-degree: 8%

---

# 채널 표면 설정 {#set-up-channel-surfaces}

>[!CONTEXTUALHELP]
>id="ajo_admin_channel_surfaces"
>title="표면"
>abstract="표면은 시스템 관리자에 의해 정의된 구성입니다. 여기에는 헤더 매개 변수, 하위 도메인, 모바일 앱 등과 같이 메시지를 전송하기 위한 모든 기술 매개 변수가 포함되어 있습니다."

포함 [!DNL Journey Optimizer], 메시지에 필요한 모든 기술 매개 변수(이메일 유형, 보낸 사람 이메일 및 이름, 모바일 앱, SMS 구성 등)를 정의하는 채널 표면(즉, 메시지 사전 설정)을 설정할 수 있습니다.

>[!CAUTION]
>
> * 채널 서피스를 생성, 편집 및 삭제하려면 [채널 표면 관리](../administration/high-low-permissions.md#manage-channel-surface) 권한.
>
> * 다음을 수행해야 합니다. [이메일 구성](../email/get-started-email-config.md), [푸시 구성](../push/push-configuration.md) 및 [SMS 구성](../sms/sms-configuration.md) 채널 서피스를 생성하기 전 단계입니다.


채널 표면이 구성되면 여정 또는 캠페인에서 메시지를 만들 때 채널 표면을 선택할 수 있습니다.

<!--
➡️ [Learn how to create and use email surfaces in this video](#video-presets)
-->

## 채널 표면 만들기 {#create-channel-surface}

>[!CONTEXTUALHELP]
>id="ajo_admin_message_presets_header"
>title="채널 표면 설정"
>abstract="채널 표면을 설정할 때 적용할 채널을 선택하고, 이메일 유형, 보낸 사람 이름, 모바일 앱, SMS 구성 등과 같이 전송에 필요한 모든 기술 매개변수를 정의합니다."

>[!CONTEXTUALHELP]
>id="ajo_admin_message_presets"
>title="채널 표면 설정"
>abstract="여정 또는 캠페인에서 이메일과 같은 작업을 만들 수 있도록 먼저 메시지에 필요한 모든 기술 설정을 정의하는 채널 표면을 만들어야 합니다. 채널 표면을 만들고, 편집하고 삭제하려면 채널 표면 관리 권한이 있어야 합니다."

채널 표면을 만들려면 다음 단계를 수행합니다.

1. 액세스 **[!UICONTROL 채널]** > **[!UICONTROL 브랜딩]** > **[!UICONTROL 채널 표면]** 메뉴를 선택한 다음 **[!UICONTROL 채널 표면 만들기]**.

   ![](assets/preset-create.png)

1. 표면에 대한 이름과 설명(선택 사항)을 입력한 다음 구성할 채널을 선택합니다.

   ![](assets/preset-general.png)

   >[!NOTE]
   >
   > 이름은 문자(A-Z)로 시작해야 합니다. 영숫자만 포함할 수 있습니다. 밑줄을 사용할 수도 있습니다 `_`, 점`.` 및 하이픈 `-` 자.

1. 다음을 선택한 경우 **[!UICONTROL 이메일]** 채널,에 설명된 대로 설정 구성 [이 섹션](../email/email-settings.md).

   ![](assets/preset-email.png)

1. 의 경우 **[!UICONTROL 푸시 알림]** 채널, 하나 이상의 플랫폼 선택 -  **iOS** 및/또는 **Android** - 및 각 플랫폼에 사용할 모바일 애플리케이션

   ![](assets/preset-push.png)

   >[!NOTE]
   >
   >푸시 알림을 전송하도록 환경을 구성하는 방법에 대한 자세한 내용은 [이 섹션](../push/push-gs.md).

1. 의 경우 **[!UICONTROL SMS]** 채널,에 자세히 설명된 대로 설정 정의 [이 섹션](../sms/sms-configuration.md#message-preset-sms).

   ![](assets/preset-sms.png)

   >[!NOTE]
   >
   >SMS 메시지를 보내도록 환경을 구성하는 방법에 대한 자세한 내용은 [이 섹션](../sms/sms-configuration.md).

1. 모든 매개 변수가 구성되면 **[!UICONTROL 제출]** 확인할 수 있습니다. 채널 서피스를 구배로 저장하고 나중에 구성을 재개할 수도 있습니다.

   ![](assets/preset-submit.png)

   >[!NOTE]
   >
   >선택한 IP 풀이 아래에 있는 동안에는 표면 생성을 계속할 수 없습니다. [에디션](ip-pools.md#edit-ip-pool) (**[!UICONTROL 처리 중]** 상태) 및 은(는) 선택한 하위 도메인과 연결된 적이 없습니다. [자세히 알아보기](#subdomains-and-ip-pools)
   >
   >표면을 초안으로 저장하고 IP 풀이 다음을 가질 때까지 기다립니다. **[!UICONTROL 성공]** 서피스 생성을 재개하는 상태입니다.

1. 채널 표면이 만들어지면 목록에 다음과 같이 표시됩니다. **[!UICONTROL 처리 중]** 상태.

   이 단계에서는 제대로 구성되었는지 확인하기 위해 몇 가지 검사를 수행합니다. <!--The processing time is around **48h-72h**, and can take up to **7-10 business days**.-->

   >[!NOTE]
   >주어진 하위 도메인에 대한 첫 번째 이메일 표면을 만들 때 처리 시간이 걸릴 수 있습니다 **10분~10일**. 선택한 하위 도메인을 다른 이메일 표면에 이미 사용하고 있는 경우 최대 3시간만 소요됩니다.

   이러한 검사에는 Adobe 팀에서 수행되는 구성 및 기술 테스트가 포함됩니다.

   * SPF 유효성 검사
   * DKIM 유효성 검사
   * MX 레코드 유효성 검사
   * IP 확인 차단 목록에 추가
   * 호스트 확인 도움말
   * IP 풀 확인
   * A/PTR 기록, t/m/res 하위 도메인 확인
   * FBL 등록(이 검사는 지정된 하위 도메인에 대한 이메일 표면이 처음 생성될 때만 수행됩니다.)

   >[!NOTE]
   >
   >검사가 실패한 경우 다음에서 가능한 실패 이유에 대해 자세히 알아보십시오. [이 섹션](#monitor-channel-surfaces).

1. 검사가 성공하면 채널 표면이 **[!UICONTROL 활성]** 상태. 메시지를 전달하는 데 사용할 준비가 되었습니다.

   ![](assets/preset-active.png)

## 채널 표면 모니터링 {#monitor-channel-surfaces}

모든 채널 표면이 **[!UICONTROL 채널]** > **[!UICONTROL 채널 표면]** 메뉴 아래의 제품에서 사용할 수 있습니다. 목록(채널, 사용자, 상태)을 검색하는 데 도움이 되는 필터를 사용할 수 있습니다.

![](assets/preset-filters.png)

생성된 채널 표면은 다음과 같은 상태를 가질 수 있습니다.

* **[!UICONTROL 초안]**: 채널 표면이 초안으로 저장되었으며 아직 제출되지 않았습니다. 구성을 다시 시작하려면 여십시오.
* **[!UICONTROL 처리 중]**: 채널 표면이 제출되었으며 몇 가지 확인 단계를 거치고 있습니다.
* **[!UICONTROL 활성]**: 채널 표면이 확인되었으며 메시지를 생성하도록 선택할 수 있습니다.
* **[!UICONTROL 실패]**: 채널 표면을 확인하는 동안 하나 이상의 검사가 실패했습니다.
* **[!UICONTROL 비활성화됨]**: 채널 표면이 비활성화되었습니다. 새 메시지를 만드는 데 사용할 수 없습니다.

채널 표면 만들기에 실패한 경우 가능한 각 실패 이유에 대한 자세한 내용은 아래에 설명되어 있습니다.

이러한 오류 중 하나가 발생하면 [Adobe 고객 지원 센터](https://helpx.adobe.com/kr/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target="_blank"} 도움을 받으려고.

* **SPF 유효성 검사 실패**: SPF(Sender Policy Framework)는 주어진 하위 도메인에서 이메일을 보낼 수 있는 승인된 IP를 지정할 수 있는 이메일 인증 프로토콜입니다. SPF 유효성 검사 실패는 SPF 레코드의 IP 주소가 사서함 공급자에게 전자 메일을 보내는 데 사용되는 IP 주소와 일치하지 않음을 의미합니다.

* **DKIM 유효성 검사 실패**: DKIM(DomainKeys Identified Mail)을 사용하면 받는 사람 서버에서 받은 메시지를 관련 도메인의 실제 보낸 사람이 보냈으며 원본 메시지의 콘텐츠가 그 도중에 변경되지 않았는지 확인할 수 있습니다. DKIM 유효성 검사 실패는 수신 메일 서버에서 메시지 콘텐츠의 신뢰성 및 전송 도메인과의 연결을 확인할 수 없음을 의미합니다.

* **MX 레코드 유효성 검사 실패**: MX(Mail eXchange) 레코드 유효성 검사 실패는 지정된 하위 도메인을 대신하여 인바운드 전자 메일을 받는 책임이 있는 메일 서버가 올바르게 구성되지 않았음을 의미합니다.

* **게재 기능 구성 실패**: 게재 기능 구성 실패는 다음 이유로 인해 발생할 수 있습니다.
   * 할당된 IP의 차단 목록에 추가
   * 잘못됨 `helo` 이름
   * 해당 표면의 IP 풀에 지정된 IP 이외의 IP에서 전송 중인 이메일
   * 주요 ISP의 받은 편지함에 이메일을 게재할 수 없음

## 채널 표면 편집 {#edit-channel-surface}

채널 표면을 편집하려면 아래 단계를 따르십시오.

>[!NOTE]
>
>다음을 편집할 수 없습니다. **[!UICONTROL 푸시 알림 설정]**. 채널 표면이 푸시 알림 채널에만 구성된 경우 편집할 수 없습니다.

1. 목록에서 채널 표면 이름을 클릭하여 엽니다.

   ![](assets/preset-name.png)

1. 원하는 대로 속성을 편집합니다.

   >[!NOTE]
   >
   >채널 표면에 **[!UICONTROL 활성]** 상태, **[!UICONTROL 이름]**, **[!UICONTROL 채널 선택]** 및 **[!UICONTROL 하위 도메인]** 필드는 회색으로 표시되며 편집할 수 없습니다.

1. 클릭 **[!UICONTROL 제출]** 을 클릭하여 변경 내용을 확인합니다.

   >[!NOTE]
   >
   >채널 서피스를 구배로 저장하고 나중에 업데이트를 재개할 수도 있습니다.

변경 사항이 제출되면 채널 표면은 다음과 유사한 유효성 검사 주기를 거치게 됩니다 [채널 표면 만들기](#create-channel-surface). 편집 처리 시간은 최대 **3시간**.

>[!NOTE]
>
>를 편집하는 경우에만 **[!UICONTROL 설명]**, **[!UICONTROL 이메일 유형]** 및/또는 **[!UICONTROL 이메일 재시도 매개 변수]** 필드를 입력하면 즉시 업데이트됩니다.

### 업데이트 세부 정보 {#update-details}

가 있는 채널 서피스의 경우 **[!UICONTROL 활성]** 상태 업데이트 세부 사항을 확인할 수 있습니다. 방법은 다음과 같습니다.

다음을 클릭합니다. **[!UICONTROL 최근 업데이트]** 활성 서피스 이름 옆에 표시되는 아이콘입니다.

![](assets/preset-recent-update-icon.png)

<!--You can also access the update details from an active channel surface while update is in progress.-->

다음에서 **[!UICONTROL 최근 업데이트]** 화면에 업데이트 상태 및 요청된 변경 사항 목록과 같은 정보가 표시됩니다.

<!--![](assets/preset-recent-update-screen.png)-->

### 업데이트 상태 {#update-statuses}

채널 표면 업데이트는 다음 상태를 가질 수 있습니다.

* **[!UICONTROL 처리 중]**: 채널 표면 업데이트가 제출되었으며 몇 가지 확인 단계를 거치고 있습니다.
* **[!UICONTROL 성공]**: 업데이트된 채널 표면이 확인되었으며 메시지를 만들도록 선택할 수 있습니다.
* **[!UICONTROL 실패]**: 채널 표면 업데이트를 확인하는 동안 하나 이상의 확인이 실패했습니다.

각 상태는 아래에 자세히 설명되어 있습니다.

#### 처리 중 {#surface-processing}

서피스가 제대로 업데이트되었는지 확인하기 위해 몇 가지 게재 가능성 확인이 수행됩니다.

>[!NOTE]
>
>를 편집하는 경우에만 **[!UICONTROL 설명]**, **[!UICONTROL 이메일 유형]** 및/또는 **[!UICONTROL 이메일 재시도 매개 변수]** 필드를 입력하면 즉시 업데이트됩니다.

처리 시간은 최대 까지 소요될 수 있습니다. **3시간**. 의 유효성 검사 주기 동안 수행되는 검사에 대해 자세히 알아보십시오. [이 섹션](#create-channel-surface).

이미 활성화된 서피스를 편집하는 경우

* 상태가 유지됩니다. **[!UICONTROL 활성]** 유효성 검사 프로세스가 진행되는 동안.

* 다음 **[!UICONTROL 최근 업데이트]** 채널 표면 목록의 표면 이름 옆에 아이콘이 표시됩니다.

* 유효성 검사 프로세스 중에 이 서피스를 사용하여 구성된 메시지는 이전 버전의 서피스를 계속 사용합니다.

>[!NOTE]
>
>업데이트가 진행되는 동안에는 채널 표면을 수정할 수 없습니다. 여전히 이름을 클릭할 수 있지만 모든 필드가 회색으로 표시됩니다. 업데이트에 성공할 때까지 변경 사항이 반영되지 않습니다.

#### 성공 {#success}

유효성 검사 프로세스가 성공하면 이 서피스를 사용하는 모든 메시지에 서피스의 새 버전이 자동으로 사용됩니다. 그러나 다음을 기다려야 할 수 있습니다.
* 단일 메시지에 소비되기 몇 분 전에
* 일괄 처리 메시지에 사용할 표면을 위한 다음 일괄 처리까지.

#### 실패 {#failed}

검증 프로세스가 실패하면 이전 버전의 서피스가 계속 사용됩니다.

에서 발생할 수 있는 실패 이유에 대해 자세히 알아보기 [이 섹션](#monitor-channel-surfaces).

업데이트 실패 시 서피스를 다시 편집할 수 있게 됩니다. 이름을 클릭하고 수정해야 하는 설정을 업데이트할 수 있습니다.

## 채널 표면 비활성화 {#deactivate-a-surface}

다음을 수행하십시오. **[!UICONTROL 활성]** 채널 표면을 새 메시지를 만들 수 없으며 비활성화할 수 있습니다. 그러나 현재 이 표면을 사용 중인 여정 메시지는 영향을 받지 않으며 계속 작동합니다.

>[!NOTE]
>
>업데이트가 처리되는 동안에는 채널 표면을 비활성화할 수 없습니다. 업데이트가 성공하거나 실패할 때까지 기다려야 합니다. 자세히 알아보기 [채널 표면 편집](#edit-channel-surface) 및 [상태 업데이트](#update-statuses).

1. 채널 표면 목록에 액세스합니다.

1. 선택한 활성 서피스에 대해 **[!UICONTROL 추가 작업]** 단추를 클릭합니다.

1. 선택 **[!UICONTROL 비활성화]**.

   ![](assets/preset-deactivate.png)

>[!NOTE]
>
>비활성화된 채널 표면은 이러한 표면을 사용하여 메시지를 보내는 여정에 문제가 발생하지 않도록 삭제할 수 없습니다.

비활성화된 채널 표면은 직접 편집할 수 없습니다. 그러나 이를 복제하고 사본을 편집하여 새 메시지를 만드는 데 사용할 새 버전을 만들 수 있습니다. 다시 활성화할 수도 있으며 업데이트가 성공적으로 완료될 때까지 기다린 후 편집할 수도 있습니다.

![](assets/preset-activate.png)

<!--
## How-to video{#video-presets}

Learn how to create channel surfaces, how to use them and how to delegate a subdomain and create an IP pool.

>[!VIDEO](https://video.tv.adobe.com/v/334343?quality=12)
-->
