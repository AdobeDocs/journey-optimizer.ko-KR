---
solution: Journey Optimizer
product: journey optimizer
title: 이메일 설정 구성
description: 채널 구성 수준에서 이메일 설정을 구성하는 방법 알아보기
feature: Email, Surface
topic: Administration
role: Admin
level: Experienced
keywords: 설정, 이메일, 구성
exl-id: 13536962-7541-4eb6-9ccb-4f97e167734a
source-git-commit: d782c668b412cebeacd1289c79bbf86ec710786b
workflow-type: tm+mt
source-wordcount: '2484'
ht-degree: 98%

---

# 이메일 설정 구성 {#email-settings}

이메일 만들기를 시작하려면 메시지에 필요한 모든 기술 매개 변수를 정의하는 이메일 채널 구성을 설정해야 합니다. [구성을 만드는 방법 알아보기](../configuration/channel-surfaces.md)

>[!NOTE]
>
>전달률을 유지하고 전달성을 향상시키기 위해, 이메일 구성을 만들기에 앞서 이메일 전송에 사용할 하위 도메인을 설정합니다. [자세히 알아보기](../configuration/about-subdomain-delegation.md)

이메일 설정은 아래에서 자세히 설명하는 바와 같이 채널 구성의 전용 섹션에서 정의합니다.

![](assets/surface-email-settings.png){width="50%" align="left"}

이메일 구성이 적용되어 아래 논리에 따라 커뮤니케이션을 보내게 됩니다.

* 배치 여정의 경우 이메일 표면 구성이 만들어지기 전에 이미 시작된 배치 실행에는 적용되지 않습니다. 다음 반복 또는 새로운 실행 시 변경 사항이 적용됩니다.

* 트랜잭션 메시지의 경우 다음 커뮤니케이션에 변경 사항이 즉시 적용됩니다(최대 5분 지연).

>[!NOTE]
>
>업데이트된 이메일 구성 설정은 구성이 사용되는 여정 또는 캠페인에 자동으로 적용됩니다.

## 이메일 유형 {#email-type}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_emailtype"
>title="이메일 유형 정의"
>abstract="이 구성을 사용할 때 전송할 이메일 유형 선택: 사용자 동의가 필요한 프로모션 이메일을 위한 마케팅 또는 특정 컨텍스트에서 구독 해지 프로필로 전송할 수도 있는 비상업적 이메일을 위한 트랜잭션."

**이메일 유형** 섹션에서 구성에 사용할 메시지 유형을 **[!UICONTROL 마케팅]** 또는 **[!UICONTROL 트랜잭션]** 중에서 선택합니다.

* 소매점의 주간 프로모션 등 프로모션 이메일의 경우 **마케팅**&#x200B;을 선택합니다. 이 메시지에는 사용자의 동의가 필요합니다.

* 주문 확인, 암호 재설정 알림 또는 배송 정보 등 비상업적 이메일에 대해서는 **트랜잭션**&#x200B;을 선택합니다. 이 이메일은 마케팅 커뮤니케이션에서 **구독 취소**&#x200B;한 프로필에도 보낼 수 있습니다. 이 메시지는 특정 컨텍스트에서만 보낼 수 있습니다.

메시지를 만들 때는 이메일에 대해 선택한 카테고리에 맞는 유효한 채널 구성을 선택해야 합니다.

## 하위 도메인 {#subdomains}

이메일을 보내는 데 사용할 하위 도메인을 선택합니다.

>[!NOTE]
>
>이메일 설정에 대한 제어를 강화하기 위해 동적 하위 도메인을 정의할 수 있습니다. [자세히 알아보기](../email/surface-personalization.md#dynamic-subdomains)

도메인 기본값을 유지하고 IP 준비 프로세스의 속도를 높이며 전달성을 개선하기 위해 발신 하위 도메인을 Adobe에 위임할 수 있습니다. [자세히 알아보기](../configuration/about-subdomain-delegation.md)

## IP 풀 세부 정보 {#ip-pools}

구성과 연결할 IP 풀을 선택합니다. [자세히 알아보기](../configuration/ip-pools.md)

![](assets/surface-subdomain-ip-pool.png){width="50%" align="left"}

선택한 IP 풀이 [편집](../configuration/ip-pools.md#edit-ip-pool) 중이고(**[!UICONTROL 처리 중]** 상태) 선택한 하위 도메인과 연결된 적이 없는 경우 구성 만들기를 진행할 수 없습니다. 그렇지 않으면 가장 오래된 버전의 IP 풀/하위 도메인 연결이 계속 사용됩니다. 이 경우 구성을 초안으로 저장하고 IP 풀이 **[!UICONTROL 성공]** 상태가 되면 다시 시도하십시오.

>[!NOTE]
>
>비프로덕션 환경의 경우, Adobe는 기본 제공 테스트 하위 도메인을 만들거나 공유 전송 IP 풀에 대한 액세스 권한을 부여하지 않습니다. [자신의 하위 도메인을 위임](../configuration/delegate-subdomain.md)하고 조직에 할당된 풀의 IP를 사용해야 합니다.

IP 풀을 선택한 후 IP 풀 드롭다운 목록 아래에 표시된 IP 주소 위로 마우스를 가져가면 PTR 정보가 표시됩니다. [PTR 기록에 대해 자세히 알아보기](../configuration/ptr-records.md)

>[!NOTE]
>
>PTR 기록이 구성되지 않은 경우 Adobe 담당자에게 문의하십시오.

## 목록 구독 취소 {#list-unsubscribe}

목록에서 하위 도메인을 선택하면 **[!UICONTROL 목록 구독 취소 사용]** 옵션이 표시됩니다. 기본적으로 활성화되어 있습니다.

원클릭 구독 취소 URL을 이메일 헤더에 포함할 수 있습니다. [자세히 알아보기](list-unsubscribe.md)

## 헤더 매개변수 {#email-header}

**[!UICONTROL 헤더 매개변수]** 섹션에서 해당 구성을 사용하여 보내는 이메일 유형과 연결된 발신자 이름 및 이메일 주소를 입력합니다.

>[!NOTE]
>
>이메일 설정에 대한 제어를 강화하려면 헤더 매개변수를 개인화할 수 있습니다. [자세히 알아보기](../email/surface-personalization.md#personalize-header)

* **[!UICONTROL 발신자 이름]**: 보내는 사람의 이름입니다. 브랜드 이름 등을 사용할 수 있습니다.
* **[!UICONTROL 발신자 이메일 접두사]**: 커뮤니케이션에 사용할 이메일 주소입니다.
* **[!UICONTROL 회신 대상 이름]**: 수신자가 이메일 클라이언트 소프트웨어에서 **회신** 버튼을 클릭했을 때 사용할 이름입니다.
* **[!UICONTROL 회신 대상 이메일]**: 수신자가 이메일 클라이언트 소프트웨어에서 **회신** 버튼을 클릭했을 때 사용할 이메일 주소입니다. [자세히 알아보기](#reply-to-email)
* **[!UICONTROL 오류 이메일 접두사]**: 메일 전달 후 며칠 간 ISP에서 생성한 오류(비동기 바운스)는 모두 이 주소로 수신됩니다. 부재 중 알림 및 문제 응답도 이 주소로 수신됩니다.

  Adobe에 위임되지 않은 특정 이메일 주소에 대한 부재 중 알림 및 문제 응답을 받으려면 [전달 프로세스](#forward-email)를 설정해야 합니다. 이 경우 해당 받은 편지함에 도착하는 이메일을 처리할 수동 또는 자동화된 솔루션이 있는지 확인합니다.

>[!NOTE]
>
>**[!UICONTROL 발신자 이메일 접두사]** 및 **[!UICONTROL 오류 이메일 접두사]** 주소는 현재 선택한 [위임된 하위 도메인](../configuration/about-subdomain-delegation.md)을 사용하여 이메일을 보냅니다. 예를 들어 위임된 하위 도메인이 *marketing.luma.com*&#x200B;인 경우를 가정해 보겠습니다.
>* *contact*&#x200B;를 **[!UICONTROL 발신자 이메일 접두사]**&#x200B;로 입력하면 발신자 이메일은 *contact@marketing.luma.com*&#x200B;입니다.
>* *error*&#x200B;를 **[!UICONTROL 오류 이메일 접두사]**&#x200B;로 입력하면 오류 주소는 *error@marketing.luma.com*&#x200B;입니다.


![](assets/preset-header.png){width="80%"}

>[!NOTE]
>
>주소는 문자(A-Z)로 시작해야 하며 영문자와 숫자만 포함할 수 있습니다. 밑줄 `_`, 점 `.`, 하이픈 `-`도 사용할 수 있습니다.

### 회신 대상 이메일 {#reply-to-email}

**[!UICONTROL 회신 대상 이메일]** 주소를 정의할 때는 어떤 이메일 주소든 유효한 주소이고 올바른 형식이며 오타가 없기만 하면 지정할 수 있습니다.

부재 중 알림 및 문제 응답을 제외한 모든 회신 이메일은 회신에 사용되는 받은 편지함에서 받게 되며, 부재 중 알림과 문제 응답은 **오류 이메일** 주소로 수신됩니다.

올바른 회신 관리를 위해서는 아래 추천 사항을 따라야 합니다.

* 전용 받은 편지함의 수신 용량이 이메일 구성을 사용하여 보내는 모든 회신 이메일을 받기에 충분한지 확인합니다. 받은 편지함에서 바운스를 반환하면 고객 회신이 수신되지 않을 수 있습니다.

* 답장에는 PII(개인 식별 정보)가 포함될 수 있으므로 개인 정보 및 준수 의무를 고려하여 처리해야 합니다.

* 회신 받은 편지함에서는 메시지를 스팸으로 표시하지 마십시오. 이 주소로 전송된 다른 모든 답장에 영향을 줍니다.

또한 **[!UICONTROL 회신 대상 이메일]** 주소를 정의할 때 유효한 MX 레코드 구성이 있는 하위 도메인을 사용해야 합니다. 그렇지 않으면 이메일 구성 처리가 실패합니다.

이메일 구성 제출 시 오류가 발생하면 입력한 주소의 하위 도메인에 대해 MX 레코드가 구성되지 않은 것입니다. 관리자에게 문의하여 해당 MX 레코드를 구성하거나, 유효한 MX 레코드 구성이 있는 다른 주소를 사용하십시오.

>[!NOTE]
>
>입력한 주소의 하위 도메인이 Adobe에 [완전히 위임된](../configuration/delegate-subdomain.md#full-subdomain-delegation) 도메인인 경우 Adobe 계정 담당자에게 문의하십시오.

### 이메일 전달 {#forward-email}

위임된 하위 도메인에 대해 [!DNL Journey Optimizer]에서 수신한 모든 이메일을 특정 이메일 주소로 전달하려면 Adobe 고객 지원 센터에 문의하십시오.

>[!NOTE]
>
>**[!UICONTROL 회신 대상 이메일]** 주소에 사용되는 하위 도메인이 Adobe에 위임되지 않은 경우 이 주소에 대해 전달이 작동하지 않습니다.

다음 사항을 입력해야 합니다.

* 원하는 전달 이메일 주소. 전달 이메일 주소 도메인은 Adobe에 위임된 하위 도메인과 일치할 수 없습니다.
* 사용자의 샌드박스 이름.
* 전달 이메일 주소를 사용할 구성 이름 또는 하위 도메인.
  <!--* The current **[!UICONTROL Reply to (email)]** address or **[!UICONTROL Error email]** address set at the channel configuration level.-->

>[!NOTE]
>
>하위 도메인당 하나의 전달 이메일 주소만 설정할 수 있습니다. 따라서 여러 구성에서 동일한 하위 도메인을 사용하는 경우 모든 구성에 대해 동일한 전달 이메일 주소를 사용해야 합니다.

전달 이메일 주소는 Adobe에 의해 설정됩니다. 3~4일 정도 소요될 수 있습니다.

완료되면 **[!UICONTROL 회신 대상 이메일]** 및 **오류 이메일** 주소에서 받은 모든 메시지와 **발신자 이메일** 주소로 보낸 모든 이메일이 사용자가 입력한 특정 이메일 주소로 전달됩니다.

>[!NOTE]
>
>기본적으로 전달을 활성화하지 않은 경우 **발신자 이메일** 주소로 직접 보낸 이메일은 삭제됩니다.

## BCC 이메일 {#bcc-email}

[!DNL Journey Optimizer]에서 보낸 이메일의 동일한 복사본(또는 숨은 참조)을 BCC 받은 편지함으로 보내어 규정 준수 또는 보관 목적으로 저장할 수 있습니다.

이렇게 하려면 채널 구성 수준에서 **[!UICONTROL BCC 이메일]** 선택 기능을 활성화합니다. [자세히 알아보기](../configuration/archiving-support.md#bcc-email)

![](assets/preset-bcc.png)

또한 **[!UICONTROL Bcc 이메일]** 주소를 정의할 때 유효한 MX 레코드 구성이 있는 하위 도메인을 사용해야 합니다. 그렇지 않으면 이메일 구성 처리가 실패합니다.

이메일 구성 제출 시 오류가 발생하면 입력한 주소의 하위 도메인에 대해 MX 레코드가 구성되지 않은 것입니다. 관리자에게 문의하여 해당 MX 레코드를 구성하거나, 유효한 MX 레코드 구성이 있는 다른 주소를 사용하십시오.

## 표시되지 않는 이메일 주소로 보내기 {#send-to-suppressed-email-addresses}

>[!CONTEXTUALHELP]
>id="ajo_surface_suppressed_addresses"
>title="금지 목록 우선순위 무시"
>abstract="스팸 불만 사항으로 인해 이메일 주소가 Adobe Journey Optimizer 금지 목록에 포함된 경우에도 해당 프로필에 트랜잭션 메시지를 보내도록 결정할 수 있습니다. 이 옵션은 기본적으로 비활성화되어 있습니다."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/monitor-reputation/manage-suppression-list.html?lang=ko" text="금지 목록 관리"

>[!IMPORTANT]
>
>이 옵션은 **[!UICONTROL 트랜잭션]** 이메일 유형을 선택한 경우에만 사용할 수 있습니다. [자세히 알아보기](#email-type)

[!DNL Journey Optimizer]에서 하드 바운스, 소프트 바운스, 스팸 불만으로 표시된 모든 이메일 주소는 [제외 목록](../configuration/manage-suppression-list.md)에 자동으로 수집되어 여정 또는 캠페인의 전송 대상에서 제외됩니다.

그러나 사용자의 스팸 불만 때문에 이메일 주소가 금지 목록에 있는 경우에도 프로필에 **트랜잭션** 유형의 메시지는 계속 보내도록 설정할 수 있습니다.

실제로 트랜잭션 메시지에는 일반적으로 주문 확인 또는 암호 재설정 알림 등 유용하고 필요한 정보가 포함됩니다. 따라서 대부분은 고객이 마케팅 메시지 하나를 스팸으로 신고했더라도 이 유형의 비상업적 이메일은 받기를 원합니다.

스팸 불만으로 인해 금지된 이메일 주소를 트랜잭션 메시지 대상자에 포함하려면 **[!UICONTROL 표시되지 않은 이메일 주소로 보내기]** 섹션에서 해당 옵션을 선택합니다.

![](assets/preset-suppressed-email-addresses.png)

>[!NOTE]
>
>이 옵션은 기본적으로 비활성화되어 있습니다.

전달성 모범 사례로서, 이 옵션은 기본적으로 비활성화되어 있습니다. 옵트아웃한 고객에게 연락하지 않도록 보장하기 위해서입니다. 그러나 이 기본 옵션을 변경하여 고객에게 트랜잭션 메시지를 보낼 수 있습니다.

이 옵션이 활성화되면 고객이 마케팅 이메일을 스팸으로 표시한 경우에도 해당 고객이 현재 구성을 사용한 트랜잭션 메시지를 받을 수 있습니다. 항상 전달성 모범 사례에 따라 옵트아웃 환경 설정을 관리해야 합니다.

## 시드 목록 {#seed-list}

>[!CONTEXTUALHELP]
>id="ajo_surface_seed_list"
>title="시드 목록 추가"
>abstract="특정 내부 주소를 대상자에게 자동으로 추가하려면 원하는 시드 목록을 선택합니다. 이러한 시드 주소는 게재 실행 시간에 포함되며 확인 목적으로 메시지와 동일한 사본을 수신합니다."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/seed-lists.html#use-seed-list" text="시드 목록이란 무엇입니까?"

[!DNL Journey Optimizer]의 시드 목록을 사용하면 특정 이메일 시드 주소를 게재에 자동으로 포함할 수 있습니다. [자세히 알아보기](../configuration/seed-lists.md)

>[!CAUTION]
>
>현재 이 기능은 이메일 채널에만 적용됩니다.

**[!UICONTROL 시드 목록]** 섹션에서 사용자와 관련된 목록을 선택합니다. [이 섹션](../configuration/seed-lists.md#create-seed-list)에서는 시드 목록을 만드는 방법을 알아봅니다.

![](../configuration/assets/seed-list-surface.png){width="80%"}

>[!NOTE]
>
>시드 목록은 한 번에 하나만 선택할 수 있습니다.

현재 구성을 캠페인이나 여정에서 사용하면 게재 실행 시 선택한 시드 목록의 이메일 주소가 포함됩니다. 즉, 보증 목적으로 게재 사본을 받게 됩니다.

[이 섹션](../configuration/seed-lists.md#use-seed-list)에서는 캠페인 또는 여정에서 시드 목록을 사용하는 방법을 알아봅니다.

## 이메일 재시도 매개변수 {#email-retry}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_retryperiod"
>title="재시도 기간 조정"
>abstract="일시적인 소프트 바운스 오류로 인해 이메일을 게재하지 못하면 3.5일(84시간)간 재시도를 수행합니다. 필요에 맞게 이 기본 재시도 기간을 조정할 수 있습니다."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/monitor-reputation/retries.html?lang=ko" text="재시도 정보"

**이메일 재시도 매개변수**&#x200B;를 구성할 수 있습니다.

![](assets/preset-retry-parameters.png)

기본적으로 [재시도 시간](../configuration/retries.md#retry-duration)은 84시간으로 설정되어 있지만 필요에 맞게 이 설정을 조정할 수 있습니다.

다음 범위 내의 정수 값(시간 또는 분)을 입력해야 합니다.

* 마케팅 이메일의 경우 최소 재시도 시간은 6시간입니다.
* 트랜잭션 이메일의 경우 최소 재시도 시간은 10분입니다.
* 두 이메일 유형 모두 최대 재시도 시간은 84시간(또는 5040분)입니다.

[이 섹션](../configuration/retries.md)에서는 재시도에 대해 자세히 알아봅니다.

## URL 추적 {#url-tracking}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_utm"
>title="URL 추적 매개변수 정의"
>abstract="이 섹션을 사용하여 추적 매개변수를 이메일 콘텐츠에 있는 URL에 자동으로 추가합니다. 이 기능은 선택 사항입니다."

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_url_preview"
>title="URL 추적 매개변수 미리보기"
>abstract="추적 매개변수를 이메일 콘텐츠에 있는 URL에 추가하는 방법을 확인합니다."

**[!UICONTROL URL 추적 매개변수]**&#x200B;를 사용하여 채널 전반의 마케팅 활동의 효과를 측정할 수 있습니다. 이 기능은 선택 사항입니다.

이 섹션에서 정의하는 매개변수는 이메일 메시지 콘텐츠에 포함되는 URL의 끝에 추가됩니다. 그런 다음 Adobe Analytics나 Google Analytics 등 웹 분석 도구에서 이 매개변수를 캡처하여 다양한 성과 보고서를 만들 수 있습니다.

**[!UICONTROL 새 매개변수 추가]** 버튼을 사용하여 최대 10개의 추적 매개변수를 추가할 수 있습니다.

![](assets/preset-url-tracking.png){width="80%"}

URL 추적 매개변수를 구성하기 위해 **[!UICONTROL 이름]** 및 **[!UICONTROL 값]** 필드에 원하는 값을 직접 입력할 수 있습니다.

[개인화 편집기](../personalization/personalization-build-expressions.md)를 사용하여 각 **[!UICONTROL 값]** 필드를 편집할 수도 있습니다. 편집 아이콘을 클릭하여 편집기를 엽니다. 여기에서는 사용 가능한 상황별 속성을 선택하거나 텍스트를 직접 편집할 수 있습니다.

![](assets/preset-url-tracking-editor.png)

개인화 편집기를 통해 다음과 같은 사전 정의된 값을 사용할 수 있습니다.

* **소스 액션 ID**: 여정 또는 캠페인에 추가된 이메일 액션의 ID입니다.

* **소스 액션 이름**: 여정 또는 캠페인에 추가된 이메일 액션의 이름입니다.

* **소스 ID**: 이메일을 보낸 여정 또는 캠페인의 ID입니다.

* **소스 이름**: 이메일을 보낸 여정 또는 캠페인의 이름입니다.

* **소스 버전 ID**: 이메일을 보낸 여정 또는 캠페인 버전의 ID입니다.

* **오퍼 ID**: 이메일에 사용된 오퍼의 ID입니다.

>[!NOTE]
>
>개인화 편집기의 상황별 속성 사용과 텍스트 값 입력을 결합하여 사용할 수 있습니다. 각 **[!UICONTROL 값]** 필드에는 최대 5KB까지 여러 문자를 사용할 수 있습니다.

<!--You can drag and drop the parameters to reorder them.-->

다음은 Adobe Analytics 및 Google Analytics 호환 URL의 예입니다.

* Adobe Analytics 호환 URL: `www.YourLandingURL.com?cid=email_AJO_{{context.system.source.id}}_image_{{context.system.source.name}}`

* Google Analytics 호환 URL: `www.YourLandingURL.com?utm_medium=email&utm_source=AJO&utm_campaign={{context.system.source.id}}&utm_content=image`

결과 추적 URL을 동적으로 미리 볼 수 있습니다. 매개변수를 추가, 편집 또는 제거할 때마다 미리보기가 자동으로 업데이트됩니다.

![](assets/preset-url-tracking-preview.png)

>[!NOTE]
>
>이메일 콘텐츠에 있는 링크에 동적 개인화 추적 매개변수를 추가할 수도 있지만, 구성 수준에서는 가능하지 않습니다. 이 작업은 이메일 디자이너를 사용하여 메시지를 작성할 때 수행해야 합니다. [자세히 알아보기](message-tracking.md#url-tracking)

## 실행 주소 {#execution-address}

>[!CONTEXTUALHELP]
>id="ajo_email_config_execution_address"
>title="사용할 기본 실행 주소 재정의"
>abstract="데이터베이스에서 여러 이메일 주소를 사용하는 경우(개인용, 업무용 등) 전송의 우선순위를 지정할 수 있는 항목을 선택할 수 있습니다. 기본 주소는 샌드박스 수준에서 정의되지만 여기서 이 특정 이메일 구성에 대한 기본 설정을 재정의할 수 있습니다."

프로필을 타기팅하면 데이터베이스에서 여러 이메일 주소(업무 이메일 주소, 개인 이메일 주소 등)를 사용 가능할 수도 있습니다.

이 경우 [!DNL Journey Optimizer]에서는 샌드박스 수준에서 **[!UICONTROL 실행 필드]**&#x200B;에 지정된 주소를 사용하여 프로필 서비스에서 우선 사용할 이메일 주소를 결정합니다. [자세히 알아보기](../configuration/primary-email-addresses.md)

>[!NOTE]
>
>현재 기본적으로 사용되는 필드를 확인하려면 **[!UICONTROL 관리]** > **[!UICONTROL 채널]** > **[!UICONTROL 일반 설정]** > **[!UICONTROL 실행 필드]** 메뉴에 액세스합니다.

하지만 이메일 채널 구성 수준에서 이 기본 실행 필드를 변경할 수 있습니다. 그런 다음에는 특정 캠페인이나 여정에 이 설정을 적용할 수 있습니다.

이렇게 하려면 **[!UICONTROL 게재 주소]** 필드를 편집하고 사용 가능한 이메일 유형 XDM 필드 목록에서 항목을 선택합니다.

![](assets/email-config-delivery-address.png)

실행 필드가 업데이트되고 기본 주소로 사용됩니다. 샌드박스 수준의 일반 설정보다 우선 적용됩니다.
