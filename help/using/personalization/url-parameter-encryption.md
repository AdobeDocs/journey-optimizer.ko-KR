---
solution: Journey Optimizer
product: journey optimizer
title: URL 매개 변수 암호화
description: PII가 Journey Optimizer 추적 링크 및 랜딩 페이지의 일반 텍스트로 노출되지 않도록 중요한 URL 쿼리 매개 변수를 암호화하는 방법에 대해 알아봅니다.
feature: Personalization
topic: Personalization
role: Admin
level: Intermediate
badge: label="제한된 가용성" type="Informative"
keywords: 암호화, URL, 추적, 랜딩 페이지, 키 레지스트리, 개인화, 보안, 개인 정보, 샌드박스
exl-id: 82e2b6e4-769f-4bdc-b2e2-19352fbaec8e
source-git-commit: 300f57042131b64c1f51e890a3f14199f33c1419
workflow-type: tm+mt
source-wordcount: '656'
ht-degree: 3%

---

# URL 매개 변수 암호화 {#url-parameter-encryption}

>[!AVAILABILITY]
>
>이 기능은 제한된 가용성으로 사용할 수 있습니다. 액세스 권한을 얻으려면 Adobe 담당자에게 문의하십시오.
>
>이 기능은 현재 이메일 채널에만 사용할 수 있습니다.

## URL 매개 변수 암호화를 사용하는 이유는 무엇입니까? {#why-url-parameter-encryption}

개인화된 추적 링크 및 랜딩 페이지 URL은 종종 쿼리 문자열에 프로필 속성, 식별자, 토큰 또는 기타 값을 포함합니다. 이러한 매개 변수는 일반적으로 이메일이나 SMS에 일반 텍스트로 표시되며, 누군가 링크를 복사, 공유 또는 책갈피를 지정하면 읽을 수 있습니다. 값에 PII(개인 식별 정보) 또는 보호해야 하는 기타 민감한 데이터가 포함될 수 있는 경우 이는 보안 및 개인정보 위험이 될 수 있습니다.

[!DNL Journey Optimizer]은(는) 개인화 편집기에서 암호화 도우미를 제공하므로 렌더링 시 모든 표현식 값(예: 프로필 속성, 토큰 또는 여러 필드에서 작성한 문자열)을 암호화할 수 있습니다. 암호화는 항상 조직의 레지스트리에서 키가 필요합니다.

관리자가 샌드박스 수준 레지스트리에서 관리하는 키를 사용하여 선택한 쿼리 매개 변수만 암호화하므로 링크를 공유하거나 검사할 때 기밀 값이 일반 텍스트로 노출되지 않습니다.

### 작동 방식 {#how-it-works}

* **관리자**&#x200B;는 키 레지스트리를 사용하여 조직의 보안 정책에 따라 [키를 만들고](#create-keys) [키를 관리합니다](#manage-keys).
* **마케터** 개인화 편집기에서 `Encrypt` 도우미를 삽입하고 레지스트리에서 보호할 값과 활성 키 식별자를 전달합니다. 구문 및 옵션에 대해서는 [이 섹션](functions/helpers.md#url-parameter-encryption-helper)을 참조하십시오.

>[!IMPORTANT]
>
>암호 해독은 조직의 책임입니다. [!DNL Journey Optimizer]은(는) 메시지가 렌더링될 때 값을 암호화합니다. 웹 사이트, 앱 또는 API는 사용자가 정의한 것과 동일한 암호화 자료 및 프로세스를 사용하여 보안 모델과 일관되게 매개 변수를 해독해야 합니다.

### 예

랜딩 페이지 URL은 값이 문자열 토큰인 쿼리 매개 변수(예: 오퍼 또는 프로필 식별자가 있는 JSON 페이로드)를 사용할 수 있습니다. `token` 암호화를 사용하지 않으면 해당 문자열 토큰이 링크에 일반 텍스트로 표시됩니다. 해당 값을 암호화 도우미로 줄바꿈하면 나머지 링크는 변경되지 않은 상태로 중요한 페이로드가 URL의 암호문으로 대체됩니다.

## 키 만들기 {#create-keys}

URL 매개 변수 암호화 도우미를 사용하려면 먼저 키를 만들어야 합니다. 그 방법은 다음과 같습니다.

<!--
>[!IMPORTANT]
>
>To access and manage keys, you you must have the **View Key Registry** and **Manage Key Registry** permissions granted. [Learn more](../administration/high-low-permissions.md)-->

1. **[!UICONTROL 관리]** > **[!UICONTROL 구성]**(으)로 이동합니다.

1. **[!UICONTROL 관리]** 단추를 클릭하여 **[!UICONTROL 키 레지스트리]**&#x200B;를 엽니다.

   ![관리 메뉴의 키 레지스트리 섹션](assets/encryption-key-registry.png){width="80%"}

1. 전용 버튼을 사용하여 조직에 필요한 키를 만듭니다.

   ![키 레지스트리 섹션에 키 단추 만들기](assets/encryption-create-key.png){width="80%"}

1. 팀이 개인화 편집기에서 참조할 수 있는 명확한 레이블 또는 식별자를 지정합니다.

   ![키 레지스트리 섹션의 키 세부 정보](assets/encryption-key-details.png){width="80%"}

1. 변경 내용을 확인하려면 **[!UICONTROL 제출]**&#x200B;을 클릭하세요.

키가 생성되면 마케터는 개인화 편집기의 [URL 매개 변수 암호화](functions/helpers.md#url-parameter-encryption-helper) 도우미를 사용하여 URL 쿼리 매개 변수에 배치되는 특정 값을 암호화할 수 있습니다.

## 키 관리 {#manage-keys}

키를 관리하려면 아래 단계를 따르십시오.

1. **[!UICONTROL 키 레지스트리]**&#x200B;에 액세스합니다. 목록 보기에서 현재 샌드박스에 대해 만들어진 모든 키를 볼 수 있습니다.

   ![키 레지스트리 목록 보기](assets/encryption-key-registry-list.png){width="100%"}

1. 키 세부 정보를 열려면 **[!UICONTROL 활성]** 상태의 키를 클릭하십시오.

   ![활성 키 세부 정보](assets/encryption-key-active-details.png){width="80%"}

1. 새 암호화에 대해 키를 영구적으로 사용하지 않도록 설정하려면 **[!UICONTROL 취소]** 단추를 클릭하십시오.

   키가 취소되면 렌더링 시 도우미에서 해당 키를 사용하려고 시도해도 실패합니다. 취소된 항목은 감사를 위해 계속 표시됩니다. 팀은 자체 시스템에서 이전 페이로드를 해독하기 위해 해당 자료가 필요할 수 있습니다.

1. 여정 및 캠페인이 이미 참조하는 안정적인 키 식별자를 유지하면서 새 키 자료를 제공하려면 **[!UICONTROL 회전]** 단추를 클릭하십시오.

   이전 자료는 취소된 상태와 적절한 이유(예: 회전 타임스탬프)로 레지스트리에 유지되며, 새 행이나 버전은 활성 키를 반영합니다.

   >[!NOTE]
   >
   >개인화 편집기에서 새 값을 암호화하려면 활성 키만 선택해야 합니다. 새 콘텐츠에 대해 해지된 키를 사용하지 마십시오.
