---
title: 메시지 사전 설정 만들기
description: 메시지 사전 설정을 구성하고 모니터링하는 방법을 알아봅니다
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 9038528f-3da0-4e0e-9b82-b72c67b42391
source-git-commit: a5c104539cae37197e0caa43cefcfed2bee23737
workflow-type: tm+mt
source-wordcount: '1684'
ht-degree: 1%

---

# 메시지 사전 설정 만들기 {#message-presets-creation}

사용 [!DNL Journey Optimizer], 전자 메일 및 푸시 알림 메시지에 필요한 모든 기술 매개 변수를 정의하는 메시지 사전 설정을 설정할 수 있습니다. 이메일 유형, 보낸 사람 이메일 및 이름, 모바일 앱 등.

>[!CAUTION]
>
> * 메시지 사전 설정 구성은 여정 관리자로 제한됩니다. [자세히 알아보기](../administration/ootb-product-profiles.md#journey-administrator)
>
> * 전자 메일 구성을 수행하고 [푸시 구성](../messages/push-configuration.md) 메시지 사전 설정을 만들기 전 단계.


메시지 사전 설정이 구성되면, **[!UICONTROL Presets]** 목록.

➡️ [이 비디오에서 이메일 사전 설정을 만들고 사용하는 방법을 알아봅니다](#video-presets)

## 메시지 사전 설정 만들기 {#create-message-preset}

메시지 사전 설정을 만들려면 다음 단계를 수행합니다.

1. 액세스 권한 **[!UICONTROL Channels]** > **[!UICONTROL Branding]** > **[!UICONTROL Message presets]** 메뉴를 클릭한 다음 **[!UICONTROL Create Message preset]**.

   ![](../assets/preset-create.png)

1. 사전 설정에 대한 이름과 설명(선택 사항)을 입력한 다음 구성할 채널을 선택합니다.

   ![](../assets/preset-general.png)

   >[!NOTE]
   >
   > 이름은 문자(A-Z)로 시작해야 합니다. 영숫자만 포함할 수 있습니다. 밑줄을 사용할 수도 있습니다 `_`, 점`.` 및 하이픈 `-` 자.

1. 구성 **이메일** 설정.

   ![](../assets/preset-email.png)

   * 사전 설정으로 전송할 메시지 유형을 선택합니다. **트랜잭션** 또는 **마케팅**

      >[!CAUTION]
      >
      > **트랜잭션** 마케팅 커뮤니케이션의 구독을 취소한 프로필로 메시지를 보낼 수 있습니다. 이러한 메시지는 암호 재설정, 주문 상태, 게재 알림 등과 같은 특정 컨텍스트에서만 보낼 수 있습니다.

   * 이메일을 보내는 데 사용할 하위 도메인을 선택합니다. [자세히 알아보기](about-subdomain-delegation.md)
   * 사전 설정과 연결할 IP 풀을 선택합니다. [자세히 알아보기](ip-pools.md)
   * 해당 사전 설정을 사용하여 보낸 전자 메일의 헤더 매개 변수를 입력합니다.

      >[!CAUTION]
      >
      >이메일 주소는 현재 선택한 주소를 사용해야 합니다 [위임된 하위 도메인](about-subdomain-delegation.md).

      * **[!UICONTROL Sender name]**: 브랜드 이름과 같은 발신자의 이름입니다.

      * **[!UICONTROL Sender email]**: 통신에 사용할 이메일 주소입니다. 예를 들어 위임된 하위 도메인이 *marketing.luma.com*, 다음 사용 가능 *contact@marketing.luma.com*.

      * **[!UICONTROL Reply to (name)]**: 수신자가 **회신** 버튼을 클릭합니다.

      * **[!UICONTROL Reply to (email)]**: 수신자가 **회신** 버튼을 클릭합니다. 위임된 하위 도메인에 정의된 주소를 사용해야 합니다(예: *reply@marketing.luma.com*). 그렇지 않으면 이메일이 삭제됩니다.

      * **[!UICONTROL Error email]**: 이 주소에는 배달되는 며칠 후 ISP에서 생성한 모든 오류(비동기 바운스)가 수신됩니다.
      >[!NOTE]
      >
      >2021년 10월 릴리스부터 의 정방향 이메일 주소를 더 이상 정의할 수 없습니다 [!DNL Journey Optimizer] 사용자 인터페이스. 모든 전자 메일을 받는 데 필요한 경우 [!DNL Journey Optimizer] 특정 이메일 주소로 전달될 위임된 하위 도메인은 [Adobe 고객 지원 지원 팀](https://helpx.adobe.com/kr/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target=&quot;_blank&quot;}.

      ![](../assets/preset-header.png)

      >[!NOTE]
      >
      >이름은 문자(A-Z)로 시작해야 합니다. 영숫자만 포함할 수 있습니다. 밑줄을 사용할 수도 있습니다 `_`, 점`.` 및 하이픈 `-` 자.

   * 구성 **전자 메일 다시 시도 매개 변수**. 기본적으로 [재시도 기간](retries.md#retry-duration) 은 84시간으로 설정되어 있지만 이 설정을 필요에 더 잘 맞게 조정할 수 있습니다.

      ![](../assets/preset-retry-paramaters.png)

      다음 범위 내에 정수 값(시간 또는 분 단위)을 입력해야 합니다.
      * 마케팅 이메일 유형의 경우 최소 재시도 기간은 6시간입니다.
      * 트랜잭션 이메일 유형의 경우 최소 다시 시도 기간은 10분입니다.
      * 두 이메일 유형의 경우 최대 다시 시도 기간은 84시간(또는 5040분)입니다.


1. 구성 **푸시 알림** 설정.

   ![](../assets/preset-push.png)

   * 하나 이상의 플랫폼을 선택하십시오. **iOS** 및/또는 **Android**

   * 각 플랫폼에 사용할 모바일 애플리케이션을 선택합니다.

      푸시 알림을 전송하도록 환경을 구성하는 방법에 대한 자세한 내용은 [이 섹션](../messages/push-gs.md).

<!--
1. Configure the **SMS** settings.

     ![](../assets/preset-sms.png)

    * Select the **[!UICONTROL SMS Type]** that will be sent with the preset: **[!UICONTROL Transactional]** or **[!UICONTROL Marketing]**
    
    * Select the **[!UICONTROL SMS configuration]** to associate with the preset.
        
      For more on how to configure your environment to send SMS messages, refer to [this section](sms-configuration.md).

    * Enter the **[!UICONTROL Sender number]** ​you want to use for your communications.
-->

1. 모든 매개 변수가 구성되면 **[!UICONTROL Submit]** 확인합니다. 메시지 사전 설정을 초안으로 저장하고 나중에 구성을 다시 시작할 수도 있습니다.

   ![](../assets/preset-submit.png)

1. 메시지 사전 설정이 만들어지면 와 함께 목록에 표시됩니다 **[!UICONTROL Processing]** 상태.

   이 단계에서는 구성이 올바른지 확인하기 위해 몇 가지 확인이 수행됩니다. 처리 시간이 거의 다 되었습니다 **48h-72h**&#x200B;과 같은 작업을 수행할 수 있습니다. **7-10 영업일**.

   이러한 검사에는 Adobe 팀이 수행하는 구성 및 기술 테스트가 포함됩니다.

   * SPF 유효성 검사
   * DKIM 유효성 검사
   * MX 레코드 유효성 검사
   * IP 차단 목록에 추가 확인
   * 헬로 호스트 확인
   * IP 풀 확인
   * A/PTR 레코드, t/m/res 하위 도메인 확인

   >[!NOTE]
   >
   >검사가 실패하면 의 가능한 실패 이유에 대해 자세히 알아보십시오 [이 섹션](#monitor-message-presets).

1. 확인이 성공하면 메시지 사전 설정이 **[!UICONTROL Active]** 상태. 메시지를 전달하는 데 사용할 준비가 되었습니다.

   ![](../assets/preset-active.png)

## 메시지 사전 설정 모니터링 {#monitor-message-presets}

모든 메시지 사전 설정이 **[!UICONTROL Channels]** > **[!UICONTROL Message presets]** 메뉴 아래의 제품에서 사용할 수 있습니다. 필터를 사용하여 목록(채널 유형, 사용자, 상태)을 검색할 수 있습니다.

![](../assets/preset-filters.png)

메시지 사전 설정에는 다음 상태가 있을 수 있습니다.

* **[!UICONTROL Draft]**: 메시지 사전 설정이 초안으로 저장되었으며 아직 제출되지 않았습니다. 구성을 다시 시작하려면 엽니다.
* **[!UICONTROL Processing]**: 메시지 사전 설정이 제출되었으며 몇 가지 확인 단계를 수행하고 있습니다.
* **[!UICONTROL Active]**: 메시지 사전 설정이 확인되었으며 메시지를 만들기 위해 선택할 수 있습니다.
* **[!UICONTROL Failed]**: 메시지 사전 설정 확인 중에 하나 또는 여러 개의 검사가 실패했습니다.
* **[!UICONTROL Deactivated]**: 메시지 사전 설정이 비활성화됩니다. 새 메시지를 만드는 데 사용할 수 없습니다.

메시지 사전 설정을 만들지 못한 경우 가능한 각 실패 이유에 대한 세부 사항이 아래에 설명되어 있습니다.

이러한 오류 중 하나가 발생하면 [Adobe 고객 지원 지원 팀](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html)지원을 받으려면 {target=&quot;_blank&quot;}.

* **SPF 유효성 검사 실패**: SPF(Sender Policy Framework)는 지정된 하위 도메인에서 전자 메일을 보낼 수 있는 인증된 IP를 지정할 수 있는 전자 메일 인증 프로토콜입니다. SPF 유효성 검사 실패가 SPF 레코드의 IP 주소가 사서함 공급자에게 전자 메일을 보내는 데 사용되는 IP 주소와 일치하지 않음을 의미합니다.

* **DKIM 유효성 검사 실패**: DKIM(DomainKeys Identified Mail)을 사용하면 수신자 서버가 수신한 메시지가 연관된 도메인의 실제 발신자에 의해 전송되었고 원래 메시지의 컨텐츠가 도중에 변경되지 않았는지 확인할 수 있습니다. DKIM 유효성 검사 오류는 수신 메일 서버가 메시지 컨텐츠의 진위 여부 및 전송 도메인과의 연결을 확인할 수 없음을 의미합니다.

* **MX 레코드 유효성 검사 실패**: MX(Mail eXchange) 레코드 유효성 검사 실패 는 주어진 하위 도메인을 대신하여 인바운드 전자 메일을 수락하는 메일 서버가 올바르게 구성되지 않음을 의미합니다.

* **게재 기능 구성이 실패했습니다.**: 다음 이유 중 하나로 인해 게재 기능 구성 오류가 발생할 수 있습니다.
   * 할당된 IP의 차단 목록에 추가
   * 유효하지 않습니다 `helo` 이름
   * 해당 사전 설정의 IP 풀에 지정된 이메일이 아닌 IP에서 전송 중인 이메일
   * Gmail 및 Yahoo와 같은 주요 ISP의 받은 편지함으로 이메일을 전달할 수 없습니다

## 메시지 사전 설정 편집 {#edit-message-preset}

메시지 사전 설정을 편집하려면 아래 단계를 따르십시오.

>[!NOTE]
>
>는 편집할 수 없습니다 **[!UICONTROL Push notification settings]**. 메시지 사전 설정이 푸시 알림 채널에 대해서만 구성된 경우 편집할 수 없습니다.

1. 목록에서 메시지 사전 설정 이름을 클릭하여 엽니다.

   ![](../assets/preset-name.png)

1. 원하는 대로 속성을 편집합니다.

   >[!NOTE]
   >
   >메시지 사전 설정에 **[!UICONTROL Active]** 상태, **[!UICONTROL Name]**, **[!UICONTROL Select channel]** 및 **[!UICONTROL Subdomain]** 필드가 회색으로 표시되어 편집할 수 없습니다.

1. 클릭 **[!UICONTROL Submit]** 를 클릭하여 변경 사항을 확인합니다.

   ![](../assets/preset-confirm-update.png)

   >[!NOTE]
   >
   >메시지 사전 설정을 초안으로 저장하고 나중에 업데이트를 다시 시작할 수도 있습니다.

변경 사항이 제출되면 메시지 사전 설정은 [사전 설정 만들기](#create-message-preset).

>[!NOTE]
>
>를 편집할 때만 **[!UICONTROL Description]**, **[!UICONTROL Email type]** 및/또는 **[!UICONTROL Email retry parameters]** 필드, 업데이트는 즉시 수행됩니다.

다음을 포함하는 메시지 사전 설정 **[!UICONTROL Active]** 상태, 업데이트 세부 사항을 확인할 수 있습니다. 방법은 다음과 같습니다.

* 을(를) 클릭합니다. **[!UICONTROL Recent update]** 활성 사전 설정 이름 옆에 표시되는 아이콘입니다.

   ![](../assets/preset-recent-update-icon.png)

* 업데이트가 진행되는 동안 활성 메시지 사전 설정에서 업데이트 세부 정보에 액세스할 수도 있습니다.

   ![](../assets/preset-view-update-details.png)

설정 **[!UICONTROL Recent update]** 화면에서 업데이트 상태 및 요청한 변경 사항 목록 등의 정보를 볼 수 있습니다.

![](../assets/preset-recent-update-screen.png)

### 상태 업데이트 {#update-statuses}

메시지 사전 설정 업데이트에는 다음 상태가 있을 수 있습니다.

* **[!UICONTROL Processing]**: 메시지 사전 설정 업데이트가 제출되었으며 몇 가지 확인 단계를 수행하고 있습니다.
* **[!UICONTROL Success]**: 업데이트된 메시지 사전 설정이 확인되었으며 메시지를 만들기 위해 선택할 수 있습니다.
* **[!UICONTROL Failed]**: 메시지 사전 설정 업데이트 확인 중에 하나 또는 여러 개의 검사가 실패했습니다.

각 상태는 아래에 자세히 설명되어 있습니다.

### 처리 중

사전 설정이 제대로 업데이트되었는지 확인하기 위해 몇 가지 게재 기능 검사가 수행됩니다.

>[!NOTE]
>
>를 편집할 때만 **[!UICONTROL Description]**, **[!UICONTROL Email type]** 및/또는 **[!UICONTROL Email retry parameters]** 필드, 업데이트는 즉시 수행됩니다.

처리 시간이 거의 다 되었습니다 **48h-72h**&#x200B;과 같은 작업을 수행할 수 있습니다. **7-10 영업일**. 에서 유효성 검사 주기 동안 수행한 검사에 대해 자세히 알아보십시오 [이 섹션](#create-message-preset).

이미 활성 상태인 사전 설정을 편집하는 경우:

* 상태 유지 **[!UICONTROL Active]** 유효성 검사 프로세스가 진행되는 동안

* 다음 **[!UICONTROL Recent update]** 메시지 사전 설정 목록에 있는 사전 설정 이름 옆에 아이콘이 표시됩니다.

* 유효성 검사 프로세스 중에 이 사전 설정을 사용하여 구성된 메시지는 이전 버전의 사전 설정을 계속 사용합니다.

>[!NOTE]
>
>업데이트가 진행되는 동안에는 메시지 사전 설정을 수정할 수 없습니다. 여전히 해당 이름을 클릭할 수 있지만, 모든 필드가 회색으로 표시됩니다. 업데이트가 완료될 때까지 변경 사항이 반영되지 않습니다.

### 성공 {#success}

유효성 검사 프로세스가 성공하면 이 사전 설정을 사용하는 모든 메시지에 새 버전의 사전 설정이 자동으로 사용됩니다. 그러나 다음을 기다려야 할 수 있습니다.
* 몇 분 전에 한 가지 메세지에 의해
* 사전 설정에 대한 다음 일괄 처리가 배치 메시지에서 유효할 때까지.

### 실패 {#failed}

유효성 검사 프로세스가 실패하면 이전 버전의 사전 설정이 계속 사용됩니다.

에서 가능한 실패 이유에 대해 자세히 알아보십시오 [이 섹션](#monitor-message-presets).

업데이트가 실패하면 사전 설정을 다시 편집할 수 있게 됩니다. 해당 이름을 클릭하고 수정해야 하는 설정을 업데이트할 수 있습니다.

## 메시지 사전 설정 비활성화 {#deactivate-preset}

을(를) 만들려면 **[!UICONTROL Active]** 새 메시지를 만들 때 메시지 사전 설정을 사용할 수 없으므로 비활성화할 수 있습니다. 그러나 이 사전 설정을 사용하여 게시된 메시지는 영향을 받지 않으며 계속 작동합니다.

>[!NOTE]
>
>업데이트가 처리되는 동안에는 메시지 사전 설정을 비활성화할 수 없습니다. 업데이트가 성공하거나 실패할 때까지 기다려야 합니다. 추가 정보 [메시지 사전 설정 편집](#edit-message-preset) 그리고 [상태 업데이트](#update-statuses).

1. 메시지 사전 설정 목록에 액세스합니다.

1. 선택한 활성 사전 설정에 대해 **[!UICONTROL More actions]** 버튼을 클릭합니다.

1. **[!UICONTROL Deactivate]**&#x200B;를 선택합니다.

   ![](../assets/preset-deactivate.png)

>[!NOTE]
>
>비활성화된 메시지 사전 설정은 이러한 사전 설정을 사용하여 메시지를 보내는 여정에서 문제를 방지하기 위해 삭제할 수 없습니다.

비활성화된 메시지 사전 설정은 직접 편집할 수 없습니다. 그러나 복제하고 복사본을 편집하여 새 메시지를 만드는 데 사용할 새 버전을 만들 수 있습니다. 다시 활성화할 수도 있으며, 업데이트가 성공적으로 편집될 때까지 기다립니다.

![](../assets/preset-activate.png)

## 방법 비디오{#video-presets}

메시지 사전 설정을 만드는 방법, 메시지 사전 설정을 사용하는 방법, 하위 도메인을 위임하고 IP 풀을 만드는 방법을 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/334343?quality=12)
