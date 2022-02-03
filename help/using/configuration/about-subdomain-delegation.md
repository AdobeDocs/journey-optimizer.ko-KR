---
title: 하위 도메인 위임
description: 하위 도메인을 위임하는 방법 알아보기
internal: n
snippet: y
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 1b5ca4db-44d9-49e2-ab39-a1abba223ec7
source-git-commit: bbc2adabac63ffb813ea2630f29aec552fc3f4df
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 34%

---

# 의 하위 도메인 위임 [!DNL Journey Optimizer] {#subdomain-delegation}

이메일 캠페인용 하위 도메인을 만들면 브랜드의 다양한 트래픽 유형(예: 마케팅과 기업)을 특정 IP 풀과 특정 도메인으로 분리하여 IP 준비 프로세스를 가속화하고 전반적인 게재 능력을 향상시킬 수 있습니다. 도메인을 공유하는데 도메인을 차단하거나 차단 목록에 추가하면 회사 메일 게재에 영향을 줄 수 있습니다. 그러나 이메일 마케팅 커뮤니케이션과 관련된 도메인의 평판 문제 또는 블록은 해당 이메일 흐름에 영향을 줍니다. 기본 도메인을 발신자로 사용하거나 여러 메일 스트림에 대한 &#39;보낸 사람&#39; 주소로 사용하면 이메일 인증이 중단되어 메시지가 스팸 폴더에 저장되거나 차단될 수 있습니다.

## 하위 도메인을 설정하는 이유  {#why-setting-up-subdomains}

하위 도메인은 브랜드나 다양한 트래픽 유형(예: 트랜잭션 메시지 및 마케팅 커뮤니케이션)을 분리하는 데 사용할 수 있는 도메인의 개별 부분입니다.

트랜잭션 및 마케팅 메시지를 모두 전송하는 데 사용되는 &quot;mybrand.com&quot; 도메인을 예로 들어 보겠습니다. 이 도메인에서는 다음의 두 하위 도메인을 설정할 수 있습니다.

* 구매 확인, 암호 재설정 등의 트랜잭션 메시지용 &quot;info.mybrand.com&quot; 하위 도메인
* 잠재 고객 대상 이메일 전송용 &quot;marketing.mybrand.com&quot; 하위 도메인

이러한 하위 도메인을 설정하면 사용 중인 도메인과 다른 하위 도메인의 평판을 유지할 수 있습니다. 예를 들어 인터넷 서비스 공급자가 게재 가능성 불량을 이유로 &quot;marketing.mybrand.com&quot; 하위 도메인을 차단 목록에 추가하더라도 전체 &quot;mybrand.com&quot; 도메인과 &quot;info.mybrand.com&quot; 하위 도메인은 차단 목록에 추가되지 않습니다.

솔루션을 구현할 때 외부에서 향하는 구성 요소에 대한 요구 사항이 있습니다. 여기에는 추적할 링크 및 웹 페이지 설정, 미러 페이지 표시 등이 포함됩니다.

이러한 요구 사항은 Adobe과 고객이 모두 호스팅하는 구성 요소를 통해 관리되지만 전자 메일의 수신자가 볼 수 있는 URL이 포함됩니다. 기본 기술 솔루션 또는 호스팅 공급자를 나타내는 URL이 없는 것을 방지하기 위해 하위 도메인을 설정하여 전자 메일 수신자에게 이를 투명하게 할 수 있습니다.

**자세히 알아보기**

* 방법 알아보기 [하위 도메인 위임](delegate-subdomain.md) 인터페이스에서 직접 액세스
* 방법 알아보기 [Google TXT 레코드 추가](google-txt.md) Gmail 주소로 이메일을 성공적으로 게재하기 위해 하위 도메인에 추가
* 방법 알아보기 [PTR 레코드 액세스](ptr-records.md) 하위 도메인용 생성되어 메일 서버를 보내 확인할 수 있음

## 하위 도메인 구성 메서드 {#subdomain-delegation-methods}

하위 도메인 구성을 사용하면 Adobe Campaign에서 사용할 도메인의 하위 섹션(기술적 명칭은 &quot;DNS 영역&quot;)을 구성할 수 있습니다. 사용 가능한 설정 방법은 다음과 같습니다.

* **Adobe에 전체 하위 도메인 위임** (권장): 하위 도메인이 Adobe에 완전히 위임됩니다. Adobe은 메시지 전달, 렌더링 및 추적에 필요한 DNS의 모든 측면을 제어하고 유지 관리할 수 있습니다. [전체 하위 도메인 위임에 대해 자세히 알아보기](delegate-subdomain.md#full-subdomain-delegation)

* **CNAME 사용**: 하위 도메인을 만들고 CNAME을 사용하여 Adobe 관련 레코드를 가리키도록 설정합니다. 이 설정을 사용하면 사용자와 Adobe 모두 DNS 유지 관리를 수행해야 합니다. [CNAME 하위 도메인 위임에 대해 자세히 알아보기](delegate-subdomain.md#cname-subdomain-delegation)

아래 표에는 이러한 두 가지 방법의 작동 방식과 각 방법을 사용하는 경우의 작업량이 간략하게 요약되어 있습니다.

| 구성 메서드 | 작동 방법 | 작업량 |
|---|---|---|
| **전체 위임** | 고객이 하위 도메인과 네임스페이스 레코드를 만들면 Adobe에서 Adobe Campaign에 필요한 모든 DNS 레코드를 구성합니다.<br/><br/>이 설정에서는 Adobe가 하위 도메인 및 모든 DNS 레코드를 관리를 전적으로 책임집니다. | 낮음 |
| **CNAME, 사용자 지정 방법** | 고객이 하위 도메인과 네임스페이스 레코드를 만들면 Adobe에서 DNS 서버에 배치할 레코드를 제공하고 Adobe Campaign DNS 서버에서 해당 값을 구성합니다.<br/><br/>이 설정에서는 사용자와 Adobe가 DNS 유지 관리를 공동으로 수행합니다. | 높음 |

도메인 구성에 대한 추가 정보는 [이 설명서](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/product-specific-resources/campaign/ac-domain-name-setup.html).

하위 도메인 구성 메서드에 대한 질문이 있으면 Adobe에 문의하거나 고객 지원 센터에 문의하여 Deliverability 컨설팅을 요청하십시오.
