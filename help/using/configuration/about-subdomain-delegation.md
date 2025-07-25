---
solution: Journey Optimizer
product: journey optimizer
title: ' [!DNL Journey Optimizer]의 하위 도메인 위임'
description: 하위 도메인을 위임하는 방법 알아보기
feature: Subdomains
topic: Administration
role: Admin
level: Experienced
keywords: 하위 도메인, 최적화 도구, 위임
exl-id: 1b5ca4db-44d9-49e2-ab39-a1abba223ec7
source-git-commit: 7854de133ebcd3b29ca59b747aa89fae242f2ea5
workflow-type: tm+mt
source-wordcount: '859'
ht-degree: 32%

---

# [!DNL Journey Optimizer]에서 하위 도메인 위임 {#subdomain-delegation}

>[!CONTEXTUALHELP]
>id="ajo_admin_delegated_subdomains"
>title="위임된 하위 도메인이 여기에 표시됩니다."
>abstract="첫 번째 하위 도메인을 위임합니다. 위임이 완료되면 PTR 기록이 생성되고 이메일 채널이 활성화됩니다."

이메일 캠페인용 하위 도메인을 생성하면 브랜드가 다양한 유형의 트래픽(예: 마케팅과 기업)을 특정 IP 풀과 특정 도메인으로 분리할 수 있으므로 IP 준비 프로세스가 빨라지고 전체적으로 전달성이 향상됩니다.

도메인을 공유하면 차단되거나 차단 목록에 추가되면 회사 메일 게재에 영향을 줄 수 있습니다. 그러나 이메일 마케팅 커뮤니케이션과 관련된 도메인의 신뢰도 문제 또는 차단은 그러한 이메일 흐름에 영향을 줍니다. 메인 도메인을 발신자로 사용하거나 여러 메일 스트림의 &#39;보낸 사람&#39; 주소로 사용하면 이메일 인증이 손상되어 메시지가 차단되거나 스팸 폴더에 보관될 수 있습니다.

>[!CAUTION]
>
>동일한 발신 도메인을 사용하여 [!DNL Adobe Journey Optimizer] 및 다른 제품(예: [!DNL Adobe Campaign] 또는 [!DNL Adobe Marketo Engage])에서 메시지를 보낼 수 없습니다.

## 하위 도메인을 설정하는 이유  {#why-set-up-subdomains}

하위 도메인은 브랜드나 다양한 트래픽 유형(예: 트랜잭션 메시지 및 마케팅 커뮤니케이션)을 분리하는 데 사용할 수 있는 도메인의 하위 도메인입니다.

트랜잭션 및 마케팅 메시지를 모두 전송하는 데 사용되는 &quot;mybrand.com&quot; 도메인을 예로 들어 보겠습니다. 이 도메인에서는 다음의 두 하위 도메인을 설정할 수 있습니다.

* 구매 확인, 암호 재설정 등의 트랜잭션 메시지용 &quot;info.mybrand.com&quot; 하위 도메인
* 잠재 고객 대상 이메일 전송용 &quot;marketing.mybrand.com&quot; 하위 도메인

이러한 하위 도메인을 설정하면 사용 중인 도메인과 다른 하위 도메인의 평판을 유지할 수 있습니다. 예를 들어 인터넷 서비스 공급자가 게재 가능성 불량을 이유로 &quot;marketing.mybrand.com&quot; 하위 도메인을 차단 목록에 추가하더라도 전체 &quot;mybrand.com&quot; 도메인과 &quot;info.mybrand.com&quot; 하위 도메인은 차단 목록에 추가되지 않습니다.

솔루션을 구현할 때 외부 구성 요소에 대한 요구 사항이 있습니다. 여기에는 추적할 링크 및 웹 페이지 설정, 미러 페이지 표시 등이 포함됩니다.

이러한 요구 사항은 Adobe과 고객 모두가 호스팅하는 구성 요소를 통해 관리되지만 이메일 수신자가 볼 수 있는 URL이 포함됩니다. 기본 기술 솔루션 또는 호스팅 공급자를 나타내는 URL이 없는 경우 이메일 수신자에게 투명하도록 하위 도메인을 설정할 수 있습니다.

**자세히 알아보기**

* 인터페이스에서 직접 [하위 도메인을 위임](delegate-subdomain.md)하는 방법을 알아봅니다.
* Gmail 주소로 이메일이 성공적으로 배달되도록 하기 위해 하위 도메인에 [Google TXT 레코드를 추가](google-txt.md)하는 방법을 알아봅니다
* 메일 서버를 전송하여 하위 도메인을 확인할 수 있도록 [생성된 PTR 레코드에 액세스](ptr-records.md)하는 방법을 알아봅니다

## 하위 도메인 구성 메서드 {#subdomain-delegation-methods}

하위 도메인 구성을 사용하면 Adobe Campaign에서 사용할 도메인의 하위 섹션(기술적 명칭은 &quot;DNS 영역&quot;)을 구성할 수 있습니다.

사용 가능한 설정 방법은 다음과 같습니다.

### 하위 도메인을 Adobe에 완전히 위임(권장) {#full-subdomain-delegation}

[!DNL Journey Optimizer]을(를) 사용하면 제품 인터페이스에서 직접 하위 도메인을 Adobe에 완전히 위임할 수 있습니다. 이렇게 하면 Adobe은 이메일 캠페인 게재, 렌더링 및 추적에 필요한 DNS의 모든 측면을 제어하고 유지 관리함으로써 메시지를 관리 서비스로 전달할 수 있습니다.

<!--The subdomain is fully delegated to Adobe. Adobe is able to control and maintain all aspects of DNS that are required for delivering, rendering and tracking messages.-->

Adobe을 사용하여 이메일 마케팅 전송 도메인에 대한 업계 표준 전달성 요구 사항을 충족하는 데 필요한 DNS 인프라를 유지 관리하는 동시에 내부 이메일 도메인에 대한 DNS를 계속 유지 및 제어할 수 있습니다.

>[!IMPORTANT]
>
>전체 하위 도메인 위임이 기본 방법입니다.

[이 섹션](delegate-subdomain.md#set-up-subdomain)에서 하위 도메인을 Adobe에 완전히 위임하는 방법을 알아봅니다.

### 하위 도메인을 CNAME으로 설정 {#cname-subdomain-setup}

도메인별 제한 정책이 있고 Adobe에서 DNS에 대한 부분적인 제어만 허용하려면 사용자 측에서 모든 DNS 관련 활동을 수행하도록 선택할 수 있습니다.

CNAME 하위 도메인 설정을 사용하면 하위 도메인을 만들고 CNAME을 사용하여 Adobe 관련 레코드를 지정할 수 있습니다. 이 구성을 사용하면 사용자와 Adobe가 이메일을 보내고 렌더링 및 추적하기 위한 환경을 설정하기 위한 DNS 유지 관리를 공동으로 수행합니다.

>[!CAUTION]
>
>조직의 정책이 전체 하위 도메인 위임 방법을 제한하는 경우 CNAME 방법을 사용하는 것이 좋습니다. 이 접근 방식을 사용하려면 DNS 레코드를 직접 유지 및 관리해야 합니다.
>
>Adobe은 CNAME 메서드를 통해 구성된 하위 도메인의 DNS를 변경, 유지 관리 또는 관리하는 것을 지원할 수 없습니다.

CNAME을 사용하여 [이 섹션](delegate-subdomain.md#cname-subdomain-setup)의 Adobe 관련 레코드를 가리키도록 하위 도메인을 만드는 방법을 알아봅니다.

## 구성 메서드 비교

아래 테이블에는 이러한 두 가지 방법의 작동 방식과 각 방법을 사용하는 경우의 작업량이 간략하게 요약되어 있습니다.

| 구성 방법 | 작동 방식 | 작업량 |
|---|---|---|
| **전체 위임** | 고객이 하위 도메인과 네임스페이스 레코드를 만들면 Adobe에서 Adobe Campaign에 필요한 모든 DNS 레코드를 구성합니다.<br/><br/>이 설정에서는 Adobe가 하위 도메인 및 모든 DNS 레코드를 관리를 전적으로 책임집니다. | 낮음 |
| **CNAME 메서드** | 고객이 하위 도메인과 네임스페이스 레코드를 만들면 Adobe에서 DNS 서버에 배치할 레코드를 제공하고 Adobe Campaign DNS 서버에서 해당 값을 구성합니다.<br/><br/>이 설정에서는 사용자와 Adobe가 DNS 유지 관리를 공동으로 수행합니다. | 높음 |

<!--
| Configuration method | How it works | Level of effort |
|---|---|---|
| **Full delegation** | Create the subdomain and namespace record. Adobe will then configure all DNS records required for Adobe Campaign.<br/><br/>In this setup, Adobe is fully responsible for managing the subdomain and all the DNS records. | Low |
| **CNAME method** |  Create the subdomain and namespace record. Adobe will then provide the records to be placed in your DNS servers and will configure the corresponding values in Adobe Campaign DNS servers.<br/><br/>In this setup, both you and Adobe share responsibility for maintaining DNS. | High |
| **Custom delegation method** |  Create the subdomain and namespace record - Adobe will then provide the records to be placed in your DNS servers. Upload the SSL Certificate obtained from the Certificate Authority and complete the Feedback Loop steps by verifying domain ownership and reporting email address.<br/><br/>In this setup, you have full responsibility for maintaining DNS. | Very high |-->

도메인 구성에 대한 추가 정보는 [이 설명서](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/product-specific-resources/campaign/ac-domain-name-setup.html?lang=ko){target="_blank"}에서 확인할 수 있습니다.

하위 도메인 구성 방법에 대한 질문이 있는 경우 Adobe에 문의하거나 고객 지원 센터에 연락하여 게재 가능성 컨설팅을 요청하십시오.


