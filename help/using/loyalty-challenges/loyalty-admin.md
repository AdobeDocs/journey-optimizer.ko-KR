---
solution: Journey Optimizer
product: journey optimizer
title: 충성도 프로그램 구성
description: Adobe [!DNL Journey Optimizer]에서 충성도 프로그램에 대한 보상 공급자, 이벤트 정의 및 조직 수준 설정을 구성하는 방법에 대해 알아봅니다.
feature: Journeys
topic: Content Management
role: Admin
level: Intermediate
hide: true
badge: label="비공개 베타" type="Informative"
mini-toc-levels: 1
exl-id: f8a3b2c1-4d5e-6f7a-8b9c-0d1e2f3a4b5c
source-git-commit: e4ee70a9c918bffb372ab7cee567ae7422c3720c
workflow-type: tm+mt
source-wordcount: '1456'
ht-degree: 0%

---

# 충성도 프로그램 구성 {#loyalty-admin}

>[!BEGINSHADEBOX]

**충성도 과제 설명서:**

* [충성도 문제 시작](get-started.md)
* [과제 및 작업 액세스 및 관리](access-loyalty-challenges.md)
* [과제 만들기](create-challenges.md)
* [작업 만들기](create-tasks.md)
* [충성도 과제 성능 모니터링](loyalty-reporting.md)
* **충성도 프로그램 구성** ◀︎**현재 상태**
* [충성도 과제 API 참조](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>이 기능은 현재 **개인 베타**&#x200B;에 있습니다. [!DNL Journey Optimizer]의 릴리스 주기 및 가용성 단계에 대한 자세한 내용은 [릴리스 주기](../rn/releases.md)를 참조하십시오.

[!DNL Journey Optimizer]의 충성도 프로그램 구성을 사용하여 외부 충성도 시스템에 연결합니다. 마케터는 **[!UICONTROL 충성도 과제(Beta)]**&#x200B;를 사용하여 과제, 작업, 콘텐츠 및 메시지를 디자인합니다. 충성도 프로그램 구성은 보상 이행, 이벤트 매핑, 제품 인벤토리 및 제외를 위한 별도의 관리자 전용 영역입니다.

## 사전 요구 사항 {#prerequisites}

충성도 프로그램 구성은 관리자를 위한 것입니다. 충성도 문제에 필요한 권한 외에 [!DNL Journey Optimizer] 인스턴스에 대한 관리자 수준의 액세스 권한이 필요합니다. 액세스 권한을 요청하려면 Adobe 관리자에게 문의하십시오.

## 액세스 충성도 프로그램 구성 {#access-loyalty-admin}

충성도 프로그램 구성 인터페이스에 액세스하려면 **[!UICONTROL 충성도]**(으)로 이동하고 **[!UICONTROL 충성도 관리자]**&#x200B;를 선택합니다.

인터페이스는 탭으로 구성됩니다.

* **전역 설정** — Experience Platform ID 네임스페이스를 설정합니다. [전역 설정을 구성하는 방법을 알아봅니다](#global-settings)
* **보상 제공자** — 보상 유형, 프록시 및 인증을 포함하여 보상을 이행하는 외부 API를 연결합니다. [보상 공급자를 구성하는 방법을 알아보세요](#reward-providers)
* **이벤트 정의** — 들어오는 경험 이벤트를 **[!UICONTROL 사용자 지정 이벤트]** 작업에서 사용할 수 있는 활동에 매핑합니다. [이벤트 정의를 구성하는 방법을 알아봅니다](#event-definitions)
* **제품 인벤토리** - 항목-그룹 간 매핑을 업로드하여 작업 자격 규칙에서 제품 그룹을 사용할 수 있습니다. [제품 인벤토리를 구성하는 방법을 알아봅니다](#product-inventory)
* **제외** — 마케터가 작업을 구성할 때 적용되는 조직 전체 항목 및 그룹 제외를 업로드합니다. [제외 구성 방법 알아보기](#exclusions)

## 전역 설정 {#global-settings}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_global_settings"
>title="전역 설정"
>abstract="충성도 프로그램을 위한 Adobe Experience Platform ID 네임스페이스를 선택합니다."

**[!UICONTROL 전역 설정]** 탭을 엽니다. 현재 이 탭에서 사용할 수 있는 기본 구성은 **[!UICONTROL 네임스페이스]** 드롭다운에서 충성도 프로그램에서 사용하는 Adobe Experience Platform ID 네임스페이스를 선택하는 것입니다.

![](assets/admin-global-settings.png)

➡️ [ID 네임스페이스로 작업하는 방법을 알아봅니다](https://experienceleague.adobe.com/ko/docs/experience-platform/identity/features/namespaces){target="_blank"}

## 보상 제공자 {#reward-providers}

**보상 공급자**&#x200B;는 도전 진행률이 기록되거나 도전이 완료되면 이행 호출을 보낼 위치를 [!DNL Journey Optimizer]에 알려줍니다(예: 회원 계정에 충성도 포인트 또는 스타트를 크레딧하는 API).

보상 제공자 구성은 다음과 같습니다.

![](assets/admin-reward.png)

* 기본 연결 세부 정보(이름, 설명, URL, 헤더).
* **[!UICONTROL 보상 정의]** — 공급자가 발급할 수 있는 보상 유형(예: stars 또는 miles).
* **[!UICONTROL 보상 프록시]** - 호출이 끝점 대신 직접 라우팅되는 중간 프록시입니다.
* **[!UICONTROL 인증 토큰 생성기]** - [!DNL Journey Optimizer] 메커니즘이 API를 호출하기 전에 액세스 토큰을 가져오는 데 사용합니다.

보상 제공자를 생성하려면 다음 단계를 수행합니다.

1. **[!UICONTROL 보상 공급자]** 탭을 열고 **[!UICONTROL 보상 공급자 만들기]**&#x200B;를 선택합니다.

1. **[!UICONTROL 이름]** 및 **[!UICONTROL 설명]**&#x200B;을 입력하십시오.

1. **[!UICONTROL URL]** 필드에 이행 요청을 받는 API URL을 입력합니다.

1. 필요에 따라 API(예: API 키 또는 콘텐츠 유형)에 **[!UICONTROL 헤더]**&#x200B;를 추가합니다.

1. 보상 공급자와 관련된 아래 리소스를 구성합니다. 자세한 내용을 보려면 각 섹션을 확장하십시오.

   +++보상 정의 - 제공업체가 지원하는 보상 당 하나의 항목(예: 프로그램 포인트 또는 별, 금전 크레딧)

   각 정의에 대해 다음 작업을 수행합니다.

   * 이름과 설명을 입력합니다.
   * 정의가 **[!UICONTROL 활성화됨]**&#x200B;인지 여부를 지정하십시오.
   * **![!UICONTROL Default]** 옵션을 전환하여 한 정의를 이 공급자에 대한 기본값으로 표시합니다.
   * 이행 호출과 함께 전송된 **페이로드**&#x200B;를 지정하십시오.

   ![](assets/admin-reward-definition.png)

   +++

   +++보상 프록시 - 엔드포인트로 직접 이동하는 대신 중간 서버를 통해 이행 호출을 라우팅합니다.

   * 이름과 설명을 입력합니다.
   * **[!UICONTROL 호스트]**, **[!UICONTROL 포트]** 정보를 입력하십시오.
   * 프록시가 **[!UICONTROL 사용]**&#x200B;인지 여부를 지정하십시오.
   * 프록시 **[!UICONTROL 자격 증명]**&#x200B;을(를) 추가합니다.

   ![](assets/admin-reward-proxies.png)

   +++

   +++인증 토큰 생성기 - API에 인증을 위한 전달자 토큰이 필요한 경우

   * 이름과 설명을 입력합니다.
   * 인증 유형 필드에 인증 유형(예: 전달자)을 입력합니다.
   * 사용할 HTTP 메서드(예: POST)를 선택합니다.
   * 토큰 끝점 URL을 입력합니다. **[!UICONTROL 토큰 키]**&#x200B;를 응답에 추가합니다(예: `access_token`).
   * 인증 토큰 생성기가 **[!UICONTROL 활성화됨]**&#x200B;인지 여부를 지정하십시오.
   * 필요한 경우 토큰 엔드포인트에 필요한 헤더를 추가합니다.

   [!DNL Journey Optimizer]은(는) 보상 API를 호출하기 전에 이 구성을 사용하여 새 토큰을 가져옵니다.

   ![](assets/admin-reward-auth.png)

   +++

1. **[!UICONTROL 보상 공급자 만들기]**&#x200B;를 선택하십시오. 공급자와 구성된 모든 리소스가 함께 저장됩니다.

저장하면 보상 제공자 목록에 제공자가 나타납니다. 마케터는 과제 보상을 구성할 때 이 제공자를 선택할 수 있습니다. [도전 보상을 구성하는 방법 알아보기](create-challenges.md#rewards)

기존 보상 공급자를 편집하려면 **[!UICONTROL 보상 공급자]** 탭을 열고 공급자를 선택한 다음 필드를 업데이트하십시오. 하위 리소스(보상 정의, 프록시, 인증 토큰 생성기)를 업데이트하면 변경 사항이 저장됩니다.

>[!NOTE]
>
>**[!UICONTROL 자신의 데이터를 가져오세요]** 도전은 자신의 데이터 통합을 통해 보상을 충족합니다. 여기에 구성된 보상 제공자는 이러한 문제에 적용되지 않습니다. [데이터 가져오기 문제를 만드는 방법을 알아봅니다](create-challenges.md#create-the-challenge)

## 이벤트 정의(선택 사항) {#event-definitions}

**[!UICONTROL 이벤트 정의]** 시스템(예: 구매, 호텔 체크인)의 경험 이벤트를 충성도 문제가 발생할 수 있는 활동(특히 **[!UICONTROL 사용자 지정 이벤트]** 작업)에 매핑합니다. 이벤트가 도착하면 [!DNL Journey Optimizer]이(가) 이러한 정의를 사용하여 이벤트를 처리할지 여부를 결정합니다. 정의와 일치하지 않는 이벤트는 무시됩니다.

### 이벤트 정의 만들기 {#create-event-definition}

1. **[!UICONTROL 이벤트 정의]** 탭을 열고 새 정의를 만듭니다.

   ![](assets/admin-event-definition.png)

1. 이벤트의 **[!UICONTROL 이름]**(예: `Coffee purchase`)을 입력하십시오. 이는 마케터가 **[!UICONTROL 사용자 지정 이벤트]** 작업을 구성할 때 표시되는 이름입니다.

1. [!DNL Journey Optimizer]이(가) 수신 페이로드에서 이벤트를 인식하는 방법을 지정합니다. **[!UICONTROL 식별자 경로]**, **[!UICONTROL XDM 스키마 ID]** 또는 둘 다 제공:

   * **[!UICONTROL 식별자 경로]** — 이벤트 또는 멤버를 식별하는 필드의 경로(예: `data.memberId`). 페이로드의 값으로 이벤트를 일치시킬 때 사용합니다.
   * **[!UICONTROL 식별자 값]** — 이 정의를 일치시키기 위해 존재해야 하는 식별자 경로의 값입니다.
   * **[!UICONTROL XDM 스키마 ID]** — 이 이벤트 유형에 대한 Experience Platform XDM 스키마의 ID입니다. 알려진 스키마에 대해 이벤트가 캡처될 때 사용합니다.

1. 브랜드가 자체 JSON 형식으로 이벤트를 보낼 때 [!DNL Journey Optimizer]이(가) 데이터를 식별하고, 구문 분석하고, 추적 여부를 결정할 수 있도록 **[!UICONTROL 스키마]** 및 **[!UICONTROL 변환기]**&#x200B;에 문자열을 붙여 넣으십시오.

   * **[!UICONTROL 스키마]** — 들어오는 페이로드의 유효성 검사 문자열입니다.
   * **[!UICONTROL 변환기]** — 페이로드를 충성도 문제가 예상하는 형식에 매핑하는 변환 표현식(예: JSONata).

1. 이벤트 정의를 저장합니다. **[!UICONTROL 이벤트 정의]** 목록에 나타납니다. 이제 이를 문제 해결에 사용할 수 있습니다. [문제를 만드는 방법을 알아보세요](create-challenges.md)

## 제품 재고 {#product-inventory}

**[!UICONTROL 제품 인벤토리]** 탭에서는 카탈로그 항목을 그룹화할 수 있으므로 모든 항목 ID를 나열하지 않고 작업에서 이를 타깃팅할 수 있습니다. 각 항목 식별자를 하나 이상의 **제품 그룹**&#x200B;에 매핑하는 **CSV 파일**&#x200B;을 업로드합니다(동일한 항목이 여러 그룹에 표시될 수 있음). 가져온 후 작업 자격 조건을 구성할 때 해당 그룹을 사용할 수 있습니다. [작업을 만드는 방법 알아보기](create-tasks.md)

1. 각 항목 식별자를 하나 이상의 제품 그룹에 매핑하는 CSV 파일을 준비합니다. 아래 섹션을 확장하여 예제를 확인합니다.

   +++제품 재고 CSV 예

   ![](assets/admin-inventory-csv.png)

   +++

1. **[!UICONTROL 제품 인벤토리]** 탭을 엽니다.

1. **[!UICONTROL 업로드]** 단추를 클릭하고 CSV 파일을 선택합니다.

   ![](assets/admin-inventory-upload.png)

1. 인벤토리 목록에서 가져온 파일을 검토합니다. 목록에는 항목당 하나의 행이 표시됩니다. ]**에 포함된**[!UICONTROL &#x200B;그룹 열에는 해당 항목이 속한 모든 제품 그룹이 표시됩니다. 각 그룹은 알약으로 나타납니다(품목이 여러 그룹에 있는 경우 여러 알약).

   ![](assets/admin-inventory-imported.png)

1. 제품 그룹의 모든 항목을 보려면 행의 **[!UICONTROL 포함된 그룹]** 열에서 해당 그룹의 알약을 선택하십시오. 그룹 세부 사항 보기에는 선택한 행의 항목뿐만 아니라 그룹의 모든 항목이 나열됩니다.

   ![](assets/admin-inventory-group.png)

1. **[!UICONTROL 업로드 기록]**&#x200B;을 사용하여 CSV 파일의 이전 업로드를 확인합니다.

## 제외 {#exclusions}

**[!UICONTROL 제외]** 탭을 사용하면 각 작업의 모든 항목 ID를 나열하지 않고 충성도 프로그램에서 제외되는 카탈로그 항목 및 그룹을 정의할 수 있습니다. 각 항목 식별자를 하나 이상의 **제외 그룹**&#x200B;에 매핑하는 **CSV 파일**&#x200B;을 업로드합니다(동일한 항목이 여러 그룹에 표시될 수 있음). 가져온 항목 및 그룹은 작업 빌더에서 사용할 수 있습니다. 제외된 항목은 자동으로 표시되며 작업에 포함할 수 없습니다. 제외 그룹은 포함 목록이 아니라 작업의 제외 목록에만 추가할 수 있습니다. [작업에 대한 적격 항목 및 제외를 정의하는 방법 알아보기](create-tasks.md#eligible-items-exclusions)

1. 각 항목 식별자를 하나 이상의 제외 그룹에 매핑하는 CSV 파일을 준비합니다. 아래 섹션을 확장하여 예제를 확인합니다.

   +++제외 CSV 예

   ![](assets/admin-exclusions-csv.png)

   +++

1. **[!UICONTROL 제외]** 탭을 엽니다.

1. **[!UICONTROL 업로드]** 단추를 클릭하고 CSV 파일을 선택합니다.

   ![](assets/admin-exclusions-upload.png)

1. 제외 목록에서 가져온 파일을 검토합니다. 목록에는 항목당 하나의 행이 표시됩니다. ]**에 포함된**[!UICONTROL &#x200B;그룹 열에는 해당 항목이 속한 모든 제외 그룹이 표시됩니다. 각 그룹은 알약으로 나타납니다(품목이 여러 그룹에 있는 경우 여러 알약).

1. 제외 그룹의 모든 항목을 보려면 행의 **[!UICONTROL 포함된 그룹]** 열에서 해당 그룹의 알약을 선택하십시오. 그룹 세부 사항 보기에는 선택한 행의 항목뿐만 아니라 그룹의 모든 항목이 나열됩니다.

1. **[!UICONTROL 업로드 기록]**&#x200B;을 사용하여 CSV 파일의 이전 업로드를 확인합니다.
