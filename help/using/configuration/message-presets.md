---
title: 메시지 사전 설정 만들기
description: 메시지 사전 설정을 구성하고 모니터링하는 방법을 알아봅니다
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
source-git-commit: f52f73b1d7f2ad5a7ebd2e8b23b7c68c4dc99212
workflow-type: tm+mt
source-wordcount: '1206'
ht-degree: 1%

---


# 메시지 사전 설정 만들기

[!DNL Journey Optimizer]을(를) 사용하여 전자 메일 및 푸시 알림 메시지에 필요한 모든 기술 매개 변수를 정의하는 메시지 사전 설정을 설정할 수 있습니다. 이메일 유형, 보낸 사람 이메일 및 이름, 모바일 앱 등.

>[!CAUTION]
>
> * 메시지 사전 설정 구성은 여정 관리자로 제한됩니다. [자세히 알아보기](../administration/ootb-product-profiles.md#journey-administrator)
>
> * 메시지 사전 설정을 만들기 전에 전자 메일 및 푸시 구성 단계를 수행해야 합니다.


메시지 사전 설정이 구성되면 **[!UICONTROL Presets]** 목록에서 메시지를 만들 때 메시지 사전 설정을 선택할 수 있습니다.

[➡️ 이 비디오에서 이메일 사전 설정을 만들고 사용하는 방법을 알아봅니다](#video-presets)

## 메시지 사전 설정 만들기 {#create-message-preset}

메시지 사전 설정을 만들려면 다음 단계를 수행합니다.

1. **[!UICONTROL Channels]** / **[!UICONTROL Message presets]** 메뉴에 액세스한 다음 **[!UICONTROL Create Message preset]** 를 클릭합니다.

   ![](../assets/preset-create.png)

1. 사전 설정에 대한 이름과 설명(선택 사항)을 입력한 다음 구성할 채널을 선택합니다.

   ![](../assets/preset-general.png)

   >[!NOTE]
   >
   > 이름은 문자(A-Z)로 시작해야 합니다. 영숫자만 포함할 수 있습니다. 밑줄 `_`, 점`.` 및 하이픈 `-` 문자를 사용할 수도 있습니다.

1. **전자 메일** 설정을 구성합니다.

   ![](../assets/preset-email.png)

   * 사전 설정으로 전송할 메시지 유형을 선택합니다. **Transactional** 또는 **Marketing**

      >[!CAUTION]
      >
      > **** 트랜잭션 메시지는 마케팅 커뮤니케이션의 구독을 취소한 프로필로 보낼 수 있습니다. 이러한 메시지는 암호 재설정, 주문 상태, 게재 알림 등과 같은 특정 컨텍스트에서만 보낼 수 있습니다.

   * 이메일을 보내는 데 사용할 하위 도메인을 선택합니다. [자세히 알아보기](about-subdomain-delegation.md)
   * 사전 설정과 연결할 IP 풀을 선택합니다. [자세히 알아보기](ip-pools.md)
   * 해당 사전 설정을 사용하여 보낸 전자 메일의 헤더 매개 변수를 입력합니다.

      >[!CAUTION]
      >
      >**회신(전자 메일 전달)** 필드를 제외하고 전자 메일 주소 도메인은 현재 선택한 [위임된 하위 도메인](about-subdomain-delegation.md)을 사용해야 합니다.

      * **[!UICONTROL Sender name]**: 브랜드 이름과 같이 발신자의 이름입니다.

      * **[!UICONTROL Sender email]**: 통신에 사용할 이메일 주소입니다. 예를 들어 위임된 하위 도메인이 *marketing.luma.com*&#x200B;인 경우 *contact@marketing.luma.com*&#x200B;을 사용할 수 있습니다.

      * **[!UICONTROL Reply to (name)]**: 수신자가 전자 메일 클라이언트 소프트웨어 **** 에서 재생 단추를 클릭할 때 사용할 이름입니다.

      * **[!UICONTROL Reply to (email)]**: 수신자가 전자 메일 클라이언트 소프트웨어에서 재생  **** 단추를 클릭할 때 사용되는 전자 메일 주소입니다. 이 주소로 전송된 이메일은 아래에 제공된 **[!UICONTROL Reply to (forward email)]** 주소로 전달됩니다. 위임된 하위 도메인에 정의된 주소(예: *reply@marketing.luma.com*)를 사용해야 합니다. 그렇지 않으면 이메일이 삭제됩니다.

      * **[!UICONTROL Reply to (forward email)]**: 위임된 하위 도메인 [!DNL Journey Optimizer] 에 대해 에서 받은 모든 이메일은 이 전자 메일 주소로 전달됩니다. 위임된 하위 도메인에 정의된 이메일 주소를 제외한 모든 주소를 지정할 수 있습니다. 예를 들어 위임된 하위 도메인이 *marketing.luma.com*&#x200B;인 경우 *abc@marketing.luma.com*&#x200B;과 같은 주소는 사용할 수 없습니다.

      * **[!UICONTROL Error email]**: 이 주소에는 배달되는 며칠 후 ISP에서 생성한 모든 오류(비동기 바운스)가 수신됩니다.

      ![](../assets/preset-header.png)

      >[!NOTE]
      >
      >이름은 문자(A-Z)로 시작해야 합니다. 영숫자만 포함할 수 있습니다. 밑줄 `_`, 점`.` 및 하이픈 `-` 문자를 사용할 수도 있습니다.

   * **전자 메일 다시 시도 매개 변수**&#x200B;를 구성합니다. 기본적으로 [다시 시도 기간](retries.md#retry-duration)은 84시간으로 설정되어 있지만 사용자의 요구 사항에 맞게 이 설정을 조정할 수 있습니다.

      ![](../assets/preset-retry-paramaters.png)

      다음 범위 내에 정수 값(시간 또는 분 단위)을 입력해야 합니다.
      * 마케팅 이메일 유형의 경우 최소 재시도 기간은 6시간입니다.
      * 트랜잭션 이메일 유형의 경우 최소 다시 시도 기간은 10분입니다.
      * 두 이메일 유형의 경우 최대 다시 시도 기간은 84시간(또는 5040분)입니다.


1. **푸시 알림** 설정을 구성합니다.

   ![](../assets/preset-push.png)

   * 하나 이상의 플랫폼을 선택하십시오. **iOS** 및/또는 **Android**

   * 각 플랫폼에 사용할 모바일 애플리케이션을 선택합니다.

      푸시 알림을 전송하도록 환경을 구성하는 방법에 대한 자세한 내용은 [이 섹션](../push-gs.md)을 참조하십시오.

1. 모든 매개 변수가 구성되면 **[!UICONTROL Submit]** 을 클릭하여 확인합니다. 메시지 사전 설정을 초안으로 저장하고 나중에 구성을 다시 시작할 수도 있습니다.

   ![](../assets/preset-submit.png)

1. 메시지 사전 설정이 만들어지면 목록에 **[!UICONTROL Processing]** 상태가 표시됩니다.

   이 단계에서는 구성이 올바른지 확인하기 위해 몇 가지 확인이 수행됩니다. 처리 시간은 **48h-72h** 주위이며, 최대 **7-10일**&#x200B;이 소요될 수 있습니다.

   이러한 검사에는 Adobe 게재 가능성 팀이 수행하는 게재 가능성 테스트가 포함됩니다.

   * SPF 유효성 검사
   * DKIM 유효성 검사
   * MX 레코드 유효성 검사
   * IP 차단 목록에 추가 확인
   * 헬로 호스트 확인
   * IP 풀 확인
   * A/PTR 레코드, t/m/res 하위 도메인 확인

   >[!NOTE]
   >
   >검사가 실패하면 [이 섹션](#monitor-message-presets)에서 가능한 실패 이유에 대해 자세히 알아보십시오.

1. 확인이 성공하면 메시지 사전 설정이 **[!UICONTROL Active]** 상태를 가져옵니다. 메시지를 전달하는 데 사용할 준비가 되었습니다.

   <!-- later on, users will be notified in Pulse -->

   ![](../assets/preset-active.png)

## 메시지 사전 설정 모니터링 {#monitor-message-presets}

모든 메시지 사전 설정이 **[!UICONTROL Channels]** / **[!UICONTROL Message presets]** 메뉴에 표시됩니다. 필터를 사용하여 목록(채널 유형, 사용자, 상태)을 검색할 수 있습니다.

![](../assets/preset-filters.png)

메시지 사전 설정에는 다음 상태가 있을 수 있습니다.

* **[!UICONTROL Draft]**: 메시지 사전 설정이 초안으로 저장되었으며 아직 제출되지 않았습니다. 구성을 다시 시작하려면 엽니다.
* **[!UICONTROL Processing]**: 메시지 사전 설정이 제출되었으며 몇 가지 확인 단계를 수행하고 있습니다.
* **[!UICONTROL Active]**: 메시지 사전 설정이 확인되었으며 메시지를 만들기 위해 선택할 수 있습니다.
* **[!UICONTROL Failed]**: 메시지 사전 설정 확인 중에 하나 또는 여러 개의 검사가 실패했습니다.
* **[!UICONTROL De-activated]**: 메시지 사전 설정이 비활성화 되었습니다. 새 메시지를 만드는 데 사용할 수 없습니다.

메시지 사전 설정을 만들지 못한 경우 가능한 각 실패 이유에 대한 세부 사항이 아래에 설명되어 있습니다.

이러한 오류 중 하나가 발생하면 [고객 지원 센터 지원 팀 Adobe](https://helpx.adobe.com/kr/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target=&quot;_blank&quot;}에 문의하여 지원을 받으십시오.

* **SPF 유효성 검사 실패**: SPF(Sender Policy Framework)는 지정된 하위 도메인에서 전자 메일을 보낼 수 있는 인증된 IP를 지정할 수 있는 전자 메일 인증 프로토콜입니다.
SPF 유효성 검사 실패가 SPF 레코드의 IP 주소가 사서함 공급자에게 전자 메일을 보내는 데 사용되는 IP 주소와 일치하지 않음을 의미합니다.

* **DKIM 유효성 검사 실패**: DKIM을 사용하면 수신한 메시지가 연관된 도메인의 실제 발신자에 의해 전송되었고 원래 메시지의 컨텐츠가 도중에 변경되지 않았는지 확인할 수 있습니다.
DKIM 유효성 검사 오류는 수신 메일 서버가 메시지 컨텐츠의 진위 여부 및 전송 도메인과의 연결을 확인할 수 없음을 의미합니다.

* **MX 레코드 유효성 검사 실패**: MX 레코드 유효성 검사 실패 는 주어진 하위 도메인을 대신하여 인바운드 전자 메일을 수락하는 메일 서버가 올바르게 구성되지 않음을 의미합니다.

* **게재 기능 구성이 실패했습니다**. 다음 이유 중 하나로 인해 게재 기능 구성 오류가 발생할 수 있습니다.
   * 할당된 IP의 차단 목록에 추가
   * 잘못된 `helo` 이름
   * 해당 사전 설정의 IP 풀에 지정된 이메일이 아닌 IP에서 전송 중인 이메일
   * Gmail 및 Yahoo와 같은 주요 ISP의 받은 편지함으로 이메일을 전달할 수 없습니다

## 메시지 사전 설정 편집

메시지 사전 설정을 편집하려면 먼저 메시지 사전 설정을 비활성화하여 새 메시지를 만들 수 없도록 해야 합니다(이 사전 설정을 사용하여 게시된 메시지는 영향을 받지 않으며 계속 작동합니다). 그런 다음 메시지 사전 설정을 복제하여 새 메시지를 만드는 데 사용할 새 버전을 만들어야 합니다.

1. 메시지 사전 설정 목록에 액세스한 다음 편집할 메시지 사전 설정을 비활성화 합니다.

   ![](../assets/preset-deactivate.png)

1. 비활성화된 메시지 사전 설정을 복제합니다. **[!UICONTROL Draft]** 상태의 복사본이 목록에 자동으로 추가됩니다.

   ![](../assets/preset-duplicated.png)

1. 복제한 메시지 사전 설정을 열고 필요에 따라 수정한 다음 변경 사항을 제출합니다. 메시지 사전 설정은 [작성 단계](#create-message-preset)와 동일한 유효성 검사 주기를 따릅니다.

1. 유효성이 확인되면 **[!UICONTROL Active]** 상태가 되고 새 메시지를 만드는 데 사용할 준비가 되었습니다.

   >[!NOTE]
   >
   >메시지를 보내기 위해 이러한 사전 설정을 사용하는 여정에서 문제를 방지하기 위해 비활성화 메시지 사전 설정을 삭제할 수 없습니다.

## 방법 비디오{#video-presets}

메시지 사전 설정을 만드는 방법, 메시지 사전 설정을 사용하는 방법, 하위 도메인을 위임하고 IP 풀을 만드는 방법을 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/334343?quality=12)
