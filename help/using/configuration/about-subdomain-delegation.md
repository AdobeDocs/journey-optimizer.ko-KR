---
title: 하위 도메인 위임
description: 하위 도메인을 위임하는 방법 알아보기
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
source-git-commit: da995c56b59fb191934788c7aea9048123a2fe6d
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 43%

---


# 하위 도메인 위임 시작

## 브랜드를 분리하여 평판 보호

하위 도메인은 브랜드나 다양한 트래픽 유형(트랜잭션 메시지, 마케팅 정보 등)을 분리하는 데 사용할 수 있는 도메인의 개별 부분입니다.
트랜잭션 및 마케팅 메시지를 모두 전송하는 데 사용되는 &quot;mybrand.com&quot; 도메인을 예로 들어 보겠습니다. 이 도메인에서는 다음의 두 하위 도메인을 설정할 수 있습니다.

* 구매 확인, 암호 재설정 등의 트랜잭션 메시지용 &quot;info.mybrand.com&quot; 하위 도메인
* 잠재 고객 대상 이메일 전송용 &quot;marketing.mybrand.com&quot; 하위 도메인

이러한 하위 도메인을 설정하면 사용 중인 도메인과 다른 하위 도메인의 평판을 유지할 수 있습니다. 예를 들어 인터넷 서비스 공급자가 게재 가능성 불량을 이유로 &quot;marketing.mybrand.com&quot; 하위 도메인을 차단 목록에 추가하더라도 전체 &quot;mybrand.com&quot; 도메인과 &quot;info.mybrand.com&quot; 하위 도메인은 차단 목록에 추가되지 않습니다.

## 리소스 URL을 투명하게 고객에게 유지

솔루션을 구현할 때 외부에서 향하는 구성 요소에 대한 요구 사항이 있습니다.여기에는 추적할 링크 및 웹 페이지 설정, 미러 페이지 표시 등이 포함됩니다.

이러한 요구 사항은 Adobe과 고객이 모두 호스팅하는 구성 요소를 통해 관리되지만 전자 메일의 수신자가 볼 수 있는 URL이 포함됩니다. 기본 기술 솔루션 또는 호스팅 공급자를 나타내는 URL이 없는 것을 방지하기 위해 하위 도메인을 설정하여 전자 메일 수신자에게 이를 투명하게 할 수 있습니다. [도메인 위임에 대해 자세히 알아보십시오](https://helpx.adobe.com/kr/campaign/kb/domain-name-delegation.html).

## Journey Optimizer의 하위 도메인 위임

Journey Optimizer은 하위 도메인을 관리하는 데 도움이 되는 몇 가지 기능을 제공합니다.

* [인터페이스에서 ](delegate-subdomain.md) 직접 하위 도메인을 위임합니다.
* [Google TXT 레코드](google-txt.md) 를 하위 도메인에 추가하여 Gmail 주소로 이메일을 성공적으로 게재할 수 있습니다.
* [하위 도메인에 대해 ](ptr-records.md) 생성된 PTR 레코드에 액세스하여 메일 서버를 보내 확인할 수 있습니다.
