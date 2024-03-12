---
solution: Journey Optimizer
product: journey optimizer
title: 의 하위 도메인 위임 [!DNL Journey Optimizer]
description: 하위 도메인을 위임하는 방법 알아보기
feature: Subdomains
topic: Administration
role: Admin
level: Experienced
keywords: 하위 도메인, 최적화 도구, 위임
exl-id: 1b5ca4db-44d9-49e2-ab39-a1abba223ec7
source-git-commit: c80fecf1373528c8b46f76ee6a6eaafbcda58892
workflow-type: tm+mt
source-wordcount: '915'
ht-degree: 30%

---

# [!DNL Journey Optimizer]에서 하위 도메인 위임 {#subdomain-delegation}

>[!CONTEXTUALHELP]
>id="ajo_admin_delegated_subdomains"
>title="위임된 하위 도메인이 여기에 표시됩니다."
>abstract="첫 번째 하위 도메인을 위임하십시오. 위임이 완료되면 PTR 기록이 생성되고 이메일 채널이 활성화됩니다."

이메일 캠페인용 하위 도메인을 생성하면 브랜드가 다양한 유형의 트래픽(예: 마케팅과 기업)을 특정 IP 풀과 특정 도메인으로 분리할 수 있으므로 IP 준비 프로세스가 빨라지고 전달성이 전반적으로 향상됩니다.

도메인을 공유하면 차단되거나 차단 목록에 추가되면 회사 메일 게재에 영향을 줄 수 있습니다. 그러나 이메일 마케팅 커뮤니케이션과 관련된 도메인의 신뢰도 문제 또는 차단은 그러한 이메일 흐름에 영향을 줍니다. 메인 도메인을 발신자로 사용하거나 여러 메일 스트림의 &#39;보낸 사람&#39; 주소로 사용하면 이메일 인증이 손상되어 메시지가 차단되거나 스팸 폴더에 보관될 수 있습니다.

>[!NOTE]
>
>동일한 발신 도메인을 사용하여 메시지를 보낼 수 없습니다. [!DNL Adobe Journey Optimizer] 및 다른 제품에서 가져온 다음과 같은 [!DNL Adobe Campaign] 또는 [!DNL Adobe Marketo Engage].

## 하위 도메인을 설정하는 이유  {#why-set-up-subdomains}

하위 도메인은 브랜드나 다양한 트래픽 유형(예: 트랜잭션 메시지 및 마케팅 커뮤니케이션)을 분리하는 데 사용할 수 있는 도메인의 하위 도메인입니다.

트랜잭션 및 마케팅 메시지를 모두 전송하는 데 사용되는 &quot;mybrand.com&quot; 도메인을 예로 들어 보겠습니다. 이 도메인에서는 다음의 두 하위 도메인을 설정할 수 있습니다.

* 구매 확인, 암호 재설정 등의 트랜잭션 메시지용 &quot;info.mybrand.com&quot; 하위 도메인
* 잠재 고객 대상 이메일 전송용 &quot;marketing.mybrand.com&quot; 하위 도메인

이러한 하위 도메인을 설정하면 사용 중인 도메인과 다른 하위 도메인의 평판을 유지할 수 있습니다. 예를 들어 인터넷 서비스 공급자가 게재 가능성 불량을 이유로 &quot;marketing.mybrand.com&quot; 하위 도메인을 차단 목록에 추가하더라도 전체 &quot;mybrand.com&quot; 도메인과 &quot;info.mybrand.com&quot; 하위 도메인은 차단 목록에 추가되지 않습니다.

솔루션을 구현할 때 외부 구성 요소에 대한 요구 사항이 있습니다. 여기에는 추적할 링크 및 웹 페이지 설정, 미러 페이지 표시 등이 포함됩니다.

이러한 요구 사항은 Adobe과 고객 모두가 호스팅하는 구성 요소를 통해 관리되지만, 이메일 수신자가 볼 수 있는 URL이 포함됩니다. 기본 기술 솔루션 또는 호스팅 공급자를 나타내는 URL이 없는 경우 이메일 수신자에게 투명하도록 하위 도메인을 설정할 수 있습니다.

**자세히 알아보기**

* 방법 알아보기 [하위 도메인 위임](delegate-subdomain.md) 인터페이스에서 직접
* 방법 알아보기 [Google TXT 레코드 추가](google-txt.md) 이메일이 Gmail 주소로 성공적으로 전달되도록 하위 도메인
* 방법 알아보기 [PTR 레코드 액세스](ptr-records.md) 메일 서버를 보내 하위 도메인을 확인할 수 있도록 하위 도메인용으로 생성됨

## 하위 도메인 구성 메서드 {#subdomain-delegation-methods}

하위 도메인 구성을 사용하면 Adobe Campaign에서 사용할 도메인의 하위 섹션(기술적 명칭은 &quot;DNS 영역&quot;)을 구성할 수 있습니다. 사용 가능한 설정 방법은 다음과 같습니다.

* **Adobe에 전체 하위 도메인 위임** (권장): 하위 도메인이 Adobe에 완전히 위임됩니다. Adobe은 메시지 전달, 렌더링 및 추적에 필요한 DNS의 모든 측면을 제어하고 유지 관리할 수 있습니다. [전체 하위 도메인 위임에 대해 자세히 알아보기](delegate-subdomain.md#full-subdomain-delegation)

* **CNAME 사용**: 하위 도메인을 만들고 CNAME을 사용하여 Adobe 관련 레코드를 가리킵니다. 이 설정을 사용하면 사용자와 Adobe이 DNS 유지 관리를 공동으로 수행합니다. [CNAME 하위 도메인 위임에 대해 자세히 알아보기](delegate-subdomain.md#cname-subdomain-delegation)

>[!CAUTION]
>
>* 전체 하위 도메인 위임이 기본 방법입니다.
>
>* 조직의 정책이 전체 하위 도메인 위임 방법을 제한하는 경우 CNAME 방법을 사용하는 것이 좋습니다. 이 접근 방식을 사용하려면 DNS 레코드를 직접 유지 및 관리해야 합니다. Adobe은 CNAME 메서드를 통해 구성된 하위 도메인의 DNS 변경, 유지 관리 또는 관리를 지원할 수 없습니다.

아래 표에는 이러한 두 가지 방법의 작동 방식과 각 방법을 사용하는 경우의 작업량이 간략하게 요약되어 있습니다.

| 구성 방법 | 작동 방식 | 작업량 |
|---|---|---|
| **전체 위임** | 고객이 하위 도메인과 네임스페이스 레코드를 만들면 Adobe에서 Adobe Campaign에 필요한 모든 DNS 레코드를 구성합니다.<br/><br/>이 설정에서는 Adobe가 하위 도메인 및 모든 DNS 레코드를 관리를 전적으로 책임집니다. | 낮음 |
| **CNAME, 사용자 지정 방법** | 고객이 하위 도메인과 네임스페이스 레코드를 만들면 Adobe에서 DNS 서버에 배치할 레코드를 제공하고 Adobe Campaign DNS 서버에서 해당 값을 구성합니다.<br/><br/>이 설정에서는 사용자와 Adobe가 DNS 유지 관리를 공동으로 수행합니다. | 높음 |

도메인 구성에 대한 추가 정보는 [이 설명서](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/product-specific-resources/campaign/ac-domain-name-setup.html?lang=ko)에서 확인할 수 있습니다.

하위 Adobe 구성 방법에 대한 질문이 있는 경우 도메인에 문의하거나 고객 지원 센터에 연락하여 게재 가능성 컨설팅을 요청하십시오.

## 위임된 하위 도메인 액세스 {#access-delegated-subdomains}

위임된 모든 하위 도메인은 **[!UICONTROL 관리]** > **[!UICONTROL 채널]** > **[!UICONTROL 하위 도메인]** 메뉴 아래의 제품에서 사용할 수 있습니다. 필터를 사용하여 목록(위임 날짜, 사용자 또는 상태)을 구체화할 수 있습니다.

![](assets/subdomain-list.png)

다음 **[!UICONTROL 상태]** 열은 하위 도메인 위임 프로세스에 대한 정보를 제공합니다.

* **[!UICONTROL 초안]**: 하위 도메인 위임이 초안으로 저장되었습니다. 위임 프로세스를 재개하려면 하위 도메인 이름을 클릭하십시오.
* **[!UICONTROL 처리 중]**: 하위 도메인을 사용하기 전에 몇 가지 구성 검사를 수행하고 있습니다.
* **[!UICONTROL 성공]**: 하위 도메인이 정상적으로 검사를 통과했으며 메시지를 전달하는 데 사용할 수 있습니다.
* **[!UICONTROL 실패]**: 하위 도메인 위임을 제출한 후 하나 이상의 검사가 실패했습니다.

을(를) 사용하여 하위 도메인에 대한 세부 정보에 액세스하려면 **[!UICONTROL 성공]** 상태, 목록에서 엽니다.

![](assets/subdomain-delegated.png)

다음과 같은 작업을 수행할 수 있습니다.

* 위임 프로세스 중에 구성된 하위 도메인 이름(읽기 전용)과 생성된 URL(리소스, 미러 페이지, 추적 URL) 검색

* 하위 도메인에 Google 사이트 확인 TXT 레코드를 추가하여 확인합니다(참조) [하위 도메인에 Google TXT 레코드 추가](google-txt.md)).


>[!CAUTION]
>
>하위 도메인 구성은 모든 환경에 공통됩니다. 따라서 하위 도메인을 수정하면 프로덕션 샌드박스에도 영향을 줍니다.
