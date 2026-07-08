---
solution: Journey Optimizer
product: journey optimizer
title: 이메일 추적 픽셀에 대한 CNIL 지침
description: 이메일 추적 픽셀 및 규정 준수 노력을 지원할 수 있는 Adobe Journey Optimizer 컨트롤에 대한 CNIL의 업데이트된 지침에 대해 알아봅니다.
feature: Privacy, Consent Management
topic: Content Management
role: User
level: Intermediate
keywords: CNIL, 추적, 픽셀, 이메일, 동의, 옵트아웃, 개인 정보
source-git-commit: dc428295d1916580c1b15eacce987696f178668b
workflow-type: tm+mt
source-wordcount: '1464'
ht-degree: 1%

---


# 이메일 추적 픽셀에 대한 CNIL의 업데이트된 지침 이해 {#cnil-pixel-tracking}

>[!BEGINSHADEBOX]

**이 페이지에서:** 전자 메일 추적 픽셀에 대한 CNIL의 2026년 4월 권장 사항에 대해 알아보고, 공개 추적 토글, 링크 수준 추적, 동의 관리, 옵트아웃 메커니즘 및 비표시 등 규정 준수를 지원할 수 있는 Adobe Journey Optimizer 컨트롤을 알아봅니다.

>[!ENDSHADEBOX]

이 페이지는 정보 제공용으로만 제공됩니다. 이는 법률적인 조언이 아니며, 해당 법률의 준수를 보증하지 않습니다. 아래에 설명된 Adobe Journey Optimizer 제품 기능은 적절하게 구성되고 작동되어 규정 준수 구현을 지원할 수 있는 기본 구성단위입니다. 각 고객은 해당 법률에 따라 자신의 의무를 결정하고 준수할 책임이 있습니다.

## 개요 {#overview}

2026년 4월 14일, 프랑스의 데이터 보호 당국인 *Commission Nationale de l&#39;Informatique et des Libertés*(CNIL)은 [이메일 내의 픽셀 추적 사용에 대한 권장 사항](https://www.cnil.fr/sites/default/files/2026-04/recommandation-pixels_de_suivi.pdf)을 게시했습니다. 안내서에서는 동의가 필요한 시기를 명확히 설명하고 이메일 픽셀 추적에 대한 적절한 동의 사례의 중요성을 강조합니다. 이 정책은 프랑스에 기반을 둔 구독자에게 이메일을 게재하는 모든 엔터티의 전송 사례에 영향을 줄 수 있습니다.

CNIL은 기업이 이메일 수신자(&#39;사용자&#39;)에게 추적 픽셀의 존재 여부, 목적, 사용자의 옵트아웃 권리 등을 알리도록 권고일로부터 3개월의 기간을 제공했다. 이 전환 기간 동안 고객은 픽셀 추적에 대해 사용자에게 알리고 필요한 경우 옵트아웃을 제공할 것으로 예상됩니다. **CNIL은 2026년 7월 14일 이후에 적용 활동을 시작할 예정입니다.**

CNIL과 기타 규제 기관이 픽셀 추적 및 관련 문제에 대한 지침을 명확히 함에 따라 Adobe은 업데이트를 계속 모니터링하고 Adobe Journey Optimizer을 포함하여 이메일 마케팅을 지원하는 Adobe 제품의 기술 기능을 고객에게 알릴 예정입니다.

Adobe Journey Optimizer은 고객이 게재 수준에서 열린 추적을 관리하는 데 도움이 되는 컨트롤을 제공합니다. 고객은 해당 CNIL 지침 및 기타 법률에 따라 자신의 규정 준수 의무를 결정할 책임이 있지만 이러한 기능은 고객 규정 준수 노력을 지원할 수 있습니다.

### 이메일 추적 픽셀이란 무엇입니까? {#tracking-pixel}

이메일 추적 픽셀은 이메일의 HTML에 임베드된 1x1 투명 이미지입니다. 수신자의 이메일 클라이언트가 해당 이미지를 로드할 때 픽셀은 타임스탬프, 디바이스 유형, 이메일 클라이언트 및 경우에 따라 대략적인 위치에 대한 IP 주소와 같은 데이터를 기록하는 서버를 ping합니다. 그러면 해당 로그가 수신자의 레코드에 연결되어 마케터는 이메일이 열렸는지 여부를 확인할 수 있습니다.

### 고객 지원 {#support}

위에서 설명한 변경 사항을 구현하는 데 도움을 원하는 고객은 기존 Adobe 에코시스템과 연계될 수 있습니다. 참조된 Adobe 기능에 대한 기술적인 질문이 있는 경우 고객 성공 관리자 또는 기술 계정 관리자에게 문의하십시오.

## 이메일 추적과 관련된 Adobe Journey Optimizer 기능 {#ajo-functionality}

Adobe Journey Optimizer은 고객이 CNIL 지침 요소를 처리할 수 있도록 지원하는 몇 가지 기본 제어 기능을 제공합니다. 아래 섹션에서는 관련 제품 기능에 대해 설명합니다.

### 이메일 유형 분류 {#email-type}

Adobe Journey Optimizer에서 모든 이메일 채널 구성은 마케팅 또는 거래로 분류됩니다. 이 분류는 보내기 전에 구독자의 동의가 필요한지 여부를 결정합니다.

* **마케팅 이메일**: 옵트인 구독자에게 전송된 홍보 통신입니다. 사용자 동의가 필요합니다. 이러한 이메일은 제외 및 옵트아웃 환경 설정을 자동으로 준수합니다.
* **트랜잭션 전자 메일**: 비상업적인 통신(예: 주문 확인, 암호 재설정). 해당 법률에 따라 마케팅 커뮤니케이션의 구독을 취소한 프로필로 보낼 수 있습니다.

전자 메일 유형은 [채널 구성](../email/email-settings.md#email-type) 수준에서 설정됩니다. 여정 또는 캠페인에서 이메일을 작성할 때 작성자는 이메일 유형이 통신의 특성과 일치하는 채널 구성을 선택해야 합니다. 이 분류는 게재 전에 적용되는 동의 검사를 알려줍니다.

### 추적 컨트롤 열기 {#open-tracking}

Adobe Journey Optimizer을 사용하면 마케터가 개별 메시지 수준에서 열린 추적(즉, 1x1 픽셀)을 제어할 수 있습니다. 여정 또는 캠페인에서 이메일을 만들 때 메시지 속성 패널에서 두 가지 추적 옵션을 사용할 수 있습니다.

* **[!UICONTROL 전자 메일 열기]**: 전자 메일에 열린 추적 픽셀이 포함되어 있는지 여부를 제어합니다. 이 옵션은 기본적으로 활성화되어 있습니다.
* **[!UICONTROL 전자 메일 클릭]**: 링크 클릭 추적 여부를 제어합니다. 이 옵션은 또한 기본적으로 활성화되어 있습니다.

특정 전자 메일에 대한 열기 추적을 비활성화하려면 메시지를 만들 때 **[!UICONTROL 전자 메일 열기]** 옵션을 선택 취소하세요. 비활성화되면 옵션은 해당 게재에 대해 열린 추적 데이터가 수집되지 않도록 합니다. 범위 내 조직의 경우 시행일 전에 모든 활성 여정 및 캠페인에 대한 진행 중 추적 설정을 검토하십시오.

<!--
Unclear whether unchecking "Email opens" fully removes the 1x1 tracking pixel from the delivered HTML, or whether the pixel is still present in the HTML but open data is suppressed at the data processing layer only. The current wording ("prevents open tracking data from being collected") is intentionally neutral as engineering wasn't able to clarify.
-->

[메시지 추적 방법 알아보기](../email/message-tracking.md)

### 링크 수준 추적 관리 {#link-tracking}

메시지당 열기 추적 토글 외에도 Adobe Journey Optimizer의 이메일 Designer은 추적되는 URL에 대한 세분화된 제어를 제공합니다. 작성자가 이메일 Designer의 **[!UICONTROL 링크]** 패널을 사용하면 메시지에서 추적된 모든 URL을 보고 각 링크에 대한 추적 모드를 개별적으로 설정할 수 있습니다.

각 링크에 사용할 수 있는 추적 모드는 다음과 같습니다.

* **추적됨**: 이 URL에 대한 추적을 활성화합니다.
* **옵트아웃**: 이 URL을 옵트아웃 또는 구독 취소 URL로 지정합니다.
* **미러 페이지**: 이 URL을 미러 페이지 링크로 지정합니다.
* **사용 안 함**: 메시지 수준 설정에 관계없이 이 URL에 대해 추적이 활성화되지 않습니다.

특정 링크를 **Never**(으)로 설정하면 메시지 수준 추적이 활성화된 경우에도 특정 URL이 추적되지 않습니다.

[이메일 Designer에서 추적을 관리하는 방법 알아보기](../email/message-tracking.md#manage-tracking)

### 동의 캡처 및 관리 {#consent-management}

Adobe Journey Optimizer은 Adobe Experience Platform(AEP) [동의 및 환경 설정 스키마](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html?lang=ko){target="_blank"}를 통해 동의를 처리합니다. 동의 환경 설정은 프로필 수준에서 저장되며 여정 및 캠페인 실행 중에 자동으로 적용됩니다.

이메일 추적과 관련된 주요 동의 속성은 다음과 같습니다.

* **`consents.marketing.email.val`**: 기본 이메일 마케팅 동의 필드. `y` 값은 옵트인을 나타내며, `n`은(는) 옵트아웃을 나타냅니다. 빈 값은 기본적으로 동의로 처리됩니다(이 기본값은 온보딩 시 변경할 수 있음).

### 옵트아웃 및 철회 메커니즘 {#opt-out}

Adobe Journey Optimizer은 구독자가 커뮤니케이션을 옵트아웃하고 환경 설정을 관리할 수 있는 여러 메커니즘을 제공하며, 이러한 모든 메커니즘은 Adobe Experience Platform에서 프로필의 동의 속성을 업데이트합니다.

**한 번의 클릭으로 구독 취소(이메일 헤더)**

이메일 채널 구성에서 **[!UICONTROL 목록 구독 취소 사용]** 옵션이 켜지면 한 번의 클릭으로 구독 취소 URL 및 mailto 주소가 이메일 헤더에 자동으로 추가됩니다. 수신자는 이메일 본문을 클릭하지 않고 이메일 클라이언트에서 직접 옵트아웃할 수 있습니다. 이 옵션은 새 채널 구성에 대해 기본적으로 활성화되어 있습니다.

[목록 구독 취소를 구성하는 방법 알아보기](../email/list-unsubscribe.md)

**한 번의 클릭으로 옵트아웃(메일 본문)**

작성자는 이메일 Designer을 사용하여 이메일 콘텐츠에 직접 원클릭 옵트아웃 링크를 삽입할 수 있습니다. 수신자가 이 링크를 클릭하면 기본 설정이 즉시 업데이트됩니다. 옵트아웃의 범위는 다음 중 하나에서 지정할 수 있습니다.

* **채널 수준**: 향후 채널 전체에서 전자 메일 통신에서 프로필을 옵트아웃합니다.
* **ID 수준**: 현재 메시지에만 사용되는 특정 전자 메일 주소를 옵트아웃합니다.

[원클릭 옵트아웃 링크를 추가하는 방법 알아보기](../email/email-opt-out.md#one-click-opt-out)

**랜딩 페이지를 통한 기본 설정 센터**

Adobe Journey Optimizer의 기본 랜딩 페이지 기능을 통해 조직은 구독자가 커뮤니케이션 및 추적 환경 설정을 관리할 수 있는 환경 설정 센터를 구축할 수 있습니다. 구독자가 환경 설정 센터 양식을 제출하면 해당 선택 사항이 동의 및 환경 설정 필드 그룹의 AEP 프로필 속성에 다시 기록됩니다.

CNIL 규정 준수 시나리오의 경우 수신자가 구독 상태와 독립적으로 추적 환경 설정을 관리할 수 있도록 환경 설정 센터 랜딩 페이지를 이메일 바닥글(구독 취소 링크와 구별됨)에서 연결할 수 있습니다.

[고객의 환경 설정을 관리하는 방법 알아보기](../action/preference-center.md)

### 동의 처리 및 적용 {#consent-enforcement}

수신자가 위의 메커니즘 중 하나를 통해 옵트아웃하면 다음 오류가 발생합니다.

* 프로필의 동의 특성(`consents.marketing.email.val`)이 Adobe Experience Platform에서 `n`(으)로 업데이트되었습니다.
* 프로필은 여정 및 캠페인에서 향후 마케팅 이메일 전송에서 즉시 제외됩니다.
* 옵트아웃 정보는 AEP 동의 서비스 데이터 세트에 저장됩니다.
* Journey Optimizer은 각 전송을 수행하기 전에 채널 수준에서 동의 검사를 수행하여 옵트아웃된 프로필이 마케팅 커뮤니케이션을 받지 않도록 합니다.

[옵트아웃 관리에 대해 자세히 알아보기](opt-out.md)

### 동의 정책 {#consent-policies}

조직은 Adobe Journey Optimizer에서 동의 정책을 만들고 적용하여 특정 동의 기준을 충족하는 프로필만 커뮤니케이션을 받도록 할 수 있습니다. 동의 정책은 마케팅 작업을 통해 채널 구성과 연결할 수 있습니다.

[동의 정책으로 작업하는 방법을 알아봅니다.](../action/consent.md)

### 비표시 목록 및 재요청 {#suppression}

Adobe Journey Optimizer은 하드 바운스, 소프트 바운스 또는 스팸 컴플레인을 유발하는 이메일 주소를 포함하는 제외 목록을 자동으로 관리합니다. 제외 목록의 프로필은 향후 마케팅 전송에서 제외됩니다.

Journey Optimizer Suppression REST API는 보내는 메시지에 대한 추가적인 프로그래밍 방식 제어를 제공하여 조직에서 API를 통해 억제 및 허용 목록 동작을 관리할 수 있도록 합니다.

[제외 목록 관리 방법 알아보기](../configuration/manage-suppression-list.md)

<!--
AJO has no native equivalent of Campaign v8's "lastPixelRefusalDate" field or re-solicitation typology rule. If re-solicitation governance for pixel consent refusal is required, customers would likely need to: (a) create a custom XDM date field to capture the pixel refusal date, and (b) build an AEP audience that filters out profiles where that date falls within the last six months, then use that audience as a suppression filter in campaigns/journeys.
-->

### 보고 {#reporting}

Adobe Journey Optimizer의 이메일 보고는 [라이브 보고서](../reports/live-report.md) 및 [Customer Journey Analytics 보고서](../reports/report-gs-cja.md)를 통해 열기 및 클릭 지표를 제공합니다. 메시지에 대해 **[!UICONTROL 이메일 열기]** 추적을 사용하지 않도록 설정하면 해당 게재에 대해 열린 데이터가 수집되지 않습니다. 보고는 클릭 수 및 기타 참여 신호만 반영합니다.
