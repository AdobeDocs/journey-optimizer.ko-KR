---
solution: Journey Optimizer
product: journey optimizer
title: 이메일 채널 구성의 CC(Carbon Copy)
description: Journey Optimizer 이메일 채널에 보이는 CC 수신자를 구성합니다. CC 필드 설정 방법, BCC와 차이점 및 제한 사항에 대해 알아봅니다.
feature: Channel Configuration
topic: Administration
role: Admin
level: Experienced
hide: true
hidefromtoc: true
keywords: CC, Carbon Copy, 이메일, 채널 구성, 이메일 헤더, BCC
badge: label="제한된 가용성" type="Informative"
exl-id: 9649cc07-3183-4510-b5d9-b1e33eff43e9
source-git-commit: 780a9259ee081336d1efb3e38c2a8eee4e97b7e3
workflow-type: tm+mt
source-wordcount: '879'
ht-degree: 1%

---

# 이메일에 참조 필드 추가 {#cc-email-field}

>[!CONTEXTUALHELP]
>id="ajo_admin_config_cc"
>title="CC 이메일 주소 정의"
>abstract="이 채널 구성으로 보낸 이메일에 보이는 CC(Carbon Copy) 필드를 추가할 수 있습니다. 고정 이메일 주소를 입력하거나 개인화(프로필 속성 또는 컨텍스트 변수)를 사용하십시오. CC 사용량은 권한이 부여된 메시지 볼륨에 계산됩니다."

>[!AVAILABILITY]
>
>이 기능은 제한된 가용성의 모든 고객이 사용할 수 있습니다. 액세스 권한을 얻으려면 Adobe 담당자에게 문의하십시오.

여정 및 캠페인을 통해 [!DNL Journey Optimizer]이(가) 보낸 전자 메일에 보이는 CC(참조) 필드를 추가할 수 있습니다. 이 선택적 기능은 이메일 헤더 매개 변수 및 BCC 이메일 옵션과 함께 [채널 구성](channel-surfaces.md) 수준에서 구성됩니다.

>[!CAUTION]
>
>CC 기능 사용량은 라이선스가 부여된 메시지 수에 따라 계산됩니다. 표시되는 CC 수신자가 필요한 경우에만 활성화하십시오. 사용 허가된 볼륨에 대한 계약을 확인하십시오.

[BCC](archiving-support.md#bcc-email)와 같이 CC 필드는 전자 메일의 복사본을 추가 주소로 보냅니다. 그러나 BCC와는 다음과 같은 점에서 다릅니다.

* CC 이메일 주소는 기본 수신자에게 표시되므로 기본 수신자가 복사한 사용자를 확인하고 후속 작업을 위해 연락할 사용자를 알 수 있습니다.
* BCC와 달리 CC 이메일 필드는 개인화를 지원하므로 여러 시나리오에 대해 하나의 채널 구성을 사용하고 사본을 수신자(예: 관계 관리자)별로 적절한 사람에게 보낼 수 있습니다. API 트리거 캠페인의 경우, 특정 이벤트나 트랜잭션과 관련된 주소를 CC할 수 있습니다.

>[!NOTE]
>
>보관 또는 규정 준수를 위해 주소가 받는 사람에게 표시되지 않아야 하는 복사본을 보관해야 하는 경우 CC 대신 [BCC](archiving-support.md#bcc-email)을(를) 사용하십시오.

## CC 이메일 활성화 {#enable-cc}

**[!UICONTROL CC 전자 메일]** 옵션을 활성화하려면 [전자 메일 채널 구성](../email/email-settings.md)에서 CC 필드를 구성하십시오.

![](assets/email-config-cc.png)

Adobe으로 위임된 하위 도메인에 정의된 이메일 주소를 제외한 모든 외부 주소를 올바른 형식으로 지정할 수 있습니다. 예를 들어 *marketing.luma.com* 하위 도메인을 Adobe에 위임한 경우 *abc@marketing.luma.com*&#x200B;과(와) 같은 주소는 사용할 수 없습니다.

>[!CAUTION]
>
>이메일 주소는 하나만 정의할 수 있습니다. CC 주소가 현재 채널 구성을 사용하여 보낸 모든 이메일을 저장할 수 있는 충분한 수신 용량을 가지고 있는지 확인합니다.
>
>더 많은 권장 사항이 [이 섹션](#cc-recommendations-limitations)에 나열됩니다.

**[!UICONTROL CC 전자 메일]** 필드에는 다음 세 가지 유형의 값을 사용할 수 있습니다.

* 고정 이메일 주소일 수 있는 **하드코딩된 값**.

* 프로필에서 사용할 수 있는 관계 관리자 전자 메일 주소와 같은 **프로필 특성**&#x200B;입니다.

* **컨텍스트 특성** - 이 값은 **API 트리거 캠페인에서만 사용할 수 있음**. CC 주소 값이 있는 컨텍스트 변수 `context.channel.email.ccvalues`을(를) 포함해야 하는 API 페이로드에서 검색됩니다.

  >[!WARNING]
  >
  >CC가 **컨텍스트 변수**&#x200B;을(를) 사용하여 설정된 경우 **API 트리거 캠페인**&#x200B;에서만 지원됩니다. 여정 또는 작업 캠페인에서 해당 채널 구성을 사용하는 경우 기본 수신자에게만 이메일이 전송되며 CC 주소에는 사본이 전송되지 않습니다.

메시지에 포함된 모든 [첨부 파일](../email/pdf-attachments.md)은(는) 기본 받는 사람과 참조 주소로 모두 전송됩니다.

CC 값이 잘못되거나 전송 시 누락된 경우(예: 빈 컨텍스트 변수) CC 복사는 건너뜁니다. 기본 수신자는 여전히 이메일을 수신합니다.

CC 필드에 대한 값이 여러 개인 경우(예: 프로필 속성이나 표현식을 사용하여 여러 주소로 확인되는 경우) 이메일 전송에 첫 번째 값만 사용됩니다.

## 기존 채널 구성에서 CC 이메일 편집 {#cc-edit}

[전자 메일 구성을 편집](channel-surfaces.md#edit-channel-surface)하고 참조 필드를 추가하거나 변경하는 경우 다음만 사용할 수 있습니다.

* **하드코딩된** CC 전자 메일 주소 또는
* **컨텍스트 변수**(API 트리거 사용용).

>[!CAUTION]
>
>기존 전자 메일 채널 구성을 편집할 때 [CC 전자 메일](../personalization/personalization-build-expressions.md#sources) 필드에 새 **[!UICONTROL 프로필 특성]**&#x200B;을 추가할 수 없습니다. [새 채널 구성을 만들어야](channel-surfaces.md#create-channel-surface).

## 권장 사항 및 제한 사항 {#cc-recommendations-limitations}

* **권한:** CC 사용량이 권한 있는 메시지 볼륨에 계산됩니다. 표시된 CC 수신자가 필요한 경우에만 CC를 사용하십시오. 사용 허가된 볼륨에 대한 계약을 확인하십시오.

* **개인 정보 및 규정 준수:** 개인 정보 규정을 준수하려면 해당되는 경우 PII(개인 식별 정보)를 안전하게 저장할 수 있는 시스템에서 CC 이메일을 처리해야 합니다. 메시지에는 PII와 같은 중요한 데이터나 개인 데이터가 포함될 수 있으므로 CC 주소가 올바른지 확인하고 메시지에 대한 액세스 권한을 보호하십시오.

* **받은 편지함 관리:** CC에 사용되는 받은 편지함은 공간 및 배달을 위해 적절하게 관리해야 합니다. 받은 편지함이 반송되면 일부 전자 메일이 수신되지 않을 수 있습니다.

* **배달 시간:** 메시지가 대상 받는 사람 앞에 CC 전자 메일 주소로 배달될 수 있습니다. 원본 메시지에 [반송](../reports/suppression-list.md#delivery-failures)이 있을 수 있어도 CC 메시지를 보낼 수 있습니다.

* **보고:** 열기, 클릭 수 및 CC 수신자의 기타 참여가 전자 메일 보고 지표에 포함됩니다. 따라서 CC 수신자의 열람 또는 클릭으로 인해 [보고서](../reports/report-gs-cja.md)에서 계산 착오가 발생합니다.

* **스팸:** CC 받은 편지함에서 메시지를 스팸으로 표시하지 마십시오. 이 메시지는 이 주소로 전송되는 다른 모든 전자 메일에 영향을 미칩니다.

* **전달성:** 전송 사례 및 받는 사람 기대에 따라 CC를 사용하십시오. CC를 과도하게 사용하면 전달성에 영향을 줄 수 있습니다. [전달성 모범 사례](../reports/deliverability.md) 및 계약 조건을 따르세요.

>[!CAUTION]
>
>**받는 사람** 전자 메일의 구독을 즉시 취소하므로 CC 주소로 전송된 전자 메일의 구독 취소 링크를 클릭하지 마십시오.
