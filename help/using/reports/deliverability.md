---
solution: Journey Optimizer
product: journey optimizer
title: 전달성 시작
description: 전달성 지침 알아보기
feature: Deliverability
topic: Content Management
role: Admin
level: Intermediate, Experienced
exl-id: 8f33dda7-9bd5-4293-8d0d-222205cbc7d5
source-git-commit: 0eeb9f6aa6276b99a4d38efc2d371ebdb58c141d
workflow-type: tm+mt
source-wordcount: '1045'
ht-degree: 8%

---

# 전달성 시작 {#manage-deliverability}

전달성은 수신자에게 도달된 게재의 성공을 측정하는 것입니다.

>[!NOTE]
>
>Healthcare Shield를 허가한 고객의 경우 Adobe이 TLS(Transport Layer Security) 1.2를 사용하여 사용자 시스템(수신자)과 Journey Optimizer(발신자) 간의 데이터 교환을 보호합니다. 수신 메일 서버가 TLS 1.2를 지원하지 않는 경우 고객은 보낸 사람에게 이메일 반송 등 전달성 문제를 겪게 됩니다.

**전자 메일 전달성**&#x200B;은(는) 개인 전자 메일 주소를 통해, 짧은 시간 내에, 그리고 콘텐츠와 형식 측면에서 예상되는 품질로 메시지를 대상에 도달시킬 수 있는 기능을 결정하는 일련의 특성을 나타냅니다. 이러한 특성은 데이터 품질, 메시지 및 콘텐츠, 전송 인프라, 평판의 네 가지 주요 범주로 나뉩니다. 이 두 솔루션은 성공적인 이메일 전달성 프로그램의 기반을 형성합니다.

**전달률**&#x200B;은(는) 배달된 메시지 수와 비교하여 받는 사람의 받은 편지함에 도달한 메시지 수입니다. 이는 수많은 요인에 따라 다르며, 특히 다음과 같습니다.

* 제한적인 스팸 고객 불만
* 낮은 하드 바운스 비율
* 타겟팅된 주소 품질
* 메시지 콘텐츠
* 보낸 사람의 신뢰도

[!DNL Journey Optimizer] 경험의 전달성을 최적화하려면 이 섹션에 나열된 모범 사례를 사용하는 것이 좋습니다. 전달성 문제는 일반적으로 인터넷 서비스 공급자(ISP) 및 메일 서버 관리자가 구현하는 스팸을 방지하는 것과 관련이 있습니다.

전달성의 의미에 대해 자세히 알아보고 주요 전달성 용어, 개념 및 접근 방식에 대한 자세한 내용은 [Adobe 전달성 모범 사례 안내서](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html?lang=ko){target="_blank"}를 참조하세요.

## 고객 불만 신고율 감소 {#reduce-complaint-rate}

ISP에는 일반적으로 수신된 메시지를 스팸으로 보고하는 눈에 띄는 수단이 있습니다. 이로 인해 신뢰할 수 없는 출처를 식별할 수 있다. 옵트아웃 요청을 신속하게 준수하여 신뢰할 수 있는 발신자임을 보임으로써 고객 불만 비율을 줄일 수 있습니다. [옵트아웃 관리에 대해 자세히 알아보기](../privacy/opt-out.md#opt-out-management)

일반적으로 옵트아웃을 원하는 수신자에게 이메일 주소 또는 이름 등의 필드를 작성하도록 요구하여 방해를 받지 마십시오. 구독 취소 랜딩 페이지에는 유효성 검사 버튼이 하나만 있어야 합니다.

추가 확인을 요청할 때 추가 주의를 기울입니다. 사용자는 두 개의 이메일 주소를 동일한 상자로 리디렉션할 수 있습니다(예: firstname.lastname@club.com 및 firstname.lastname@internet-club.com). 프로필에서 첫 번째 주소만 기억할 수 있고 다른 주소로 보낸 메시지를 통해 구독을 취소하려는 경우 암호화된 식별자와 입력한 이메일 주소가 일치하지 않기 때문에 양식에서 이를 거부합니다.

## 제외 목록 활용 {#suppression-lists}

[!DNL Journey Optimizer]은(는) 지속적으로 발생하는 스팸 불만, 하드 바운스 및 소프트 바운스를 수집하는 비표시 목록을 관리합니다.

게재 가능성을 보호하기 위해 주소가 제외 목록에 있는 수신자는 이후 모든 게재에서 기본적으로 제외됩니다. 이러한 연락처로 보내면 전송 평판이 손상될 수 있기 때문입니다.

[제외 목록에 대해 자세히 알아보기](suppression-list.md)

## 모니터링 도구 사용 {#monitoring-tools}

[!DNL Journey Optimizer]이(가) 제공하는 보고 기능을 사용하여 게재 가능성을 모니터링합니다.

캠페인 및 여정 보고서를 사용하면 일련의 실시간 지표를 통해 게재의 성과를 확인할 수 있습니다. 여러 가지 항목 중에서 다음을 표시합니다.

* 실행, 전송 및 게재된 메시지 수입니다.
* 열린 메시지 수와 클릭한 메시지/링크 수.

[실시간 보고서](../reports/live-report.md) 및 [모든 시간 보고서](../reports/report-gs-cja.md)에 대해 자세히 알아보기

## 메시지 콘텐츠 조정 {#adapt-message-content}

그보다 낮은 수준으로 특정 메시지의 콘텐츠가 스팸으로 감지될 수 있습니다.

게재 가능성을 향상시키고 이메일이 수신자에게 도달하는지 확인하려면 메시지 콘텐츠를 디자인할 때 아래 원칙을 따르십시오.

* **보낸 사람 이름 및 주소**: 주소가 보낸 사람을 명시적으로 식별해야 합니다. 도메인은 발신자가 소유하고 등록해야 합니다. 도메인 레지스트리를 개인화하면 안 됩니다.

* **구독 취소 링크 및 랜딩 페이지**: 구독 취소 링크는 필수입니다. 표시 및 유효해야 하며 양식이 제대로 작동해야 합니다.

[이메일 콘텐츠 디자인에 대해 자세히 알아보기](../email/get-started-email-design.md)

## 보낸 사람으로서의 평판 확립 {#reputation}

최근 다른 이메일 서비스 공급자, IP 주소, 이메일 도메인 또는 하위 도메인으로 이동한 경우 발신자로서의 신뢰도를 설정해야 합니다. 그렇지 않으면 게재가 차단되거나 수신자 사서함의 스팸 폴더로 이동될 수 있습니다.

완전히 새로운 IP 주소로 이메일을 보낼 때 이제 사용자 인터페이스에서 직접 IP 준비 워크플로우를 쉽게 수행할 수 있습니다.

Adobe Journey Optimizer는 최적의 전달성을 위한 모범 사례에 따라 IP 주소를 준비하는 표준화되고 효율적인 방법을 제공합니다.

[IP 준비 계획에 대해 자세히 알아보기](../configuration/ip-warmup-gs.md)

<!--To warm up your IP, you can gradually ramp up the number of your deliveries. Learn more in this [use case](../building-journeys/ramp-up-deliveries-uc.md).-->

## DMARC 구현 {#dmarc}

[!DNL Journey Optimizer]을(를) 사용하면 합법적인 이메일이 스팸 또는 거부로 표시될 위험을 완화하고 게재 가능성 문제를 방지할 수 있습니다. 이를 통해 Adobe에 위임하는 모든 하위 도메인에 대해 DMARC 레코드를 설정할 수 있습니다.

도메인 기반 메시지 인증, 보고 및 적합성(DMARC)은 도메인 소유자가 도메인을 악의적인 행위자의 무단 사용으로부터 보호할 수 있는 이메일 인증 방법입니다.

[DMARC 레코드에 대한 자세한 내용](../configuration/dmarc-record.md)

## 피드백 루프에 대한 정보 {#feedback-loops}

>[!CONTEXTUALHELP]
>id="ajo_surface_dynamic_subdomain_list"
>title="일부 하위 도메인은 사용하지 못할 수 있습니다."
>abstract="현재 피드백 루프 등록이 보류되어 특정 하위 도메인을 선택할 수 없습니다. 이 과정은 영업일 기준 최대 10일 정도 소요될 수 있습니다. 완료되면 사용 가능한 모든 하위 도메인 중에서 선택할 수 있습니다."
>additional-url="https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/configuration/delegate-subdomains/about-subdomain-delegation" text="하위 도메인 위임 시작"

FBL(피드백 루프)은 일부 ISP에서 제공하는 서비스로, 이메일을 받은 사용자가 이메일을 스팸으로 표시하도록 선택하면 이메일 발신자에게 자동으로 알림을 보낼 수 있습니다(&quot;컴플레인&quot;이라고도 함).

최종 사용자가 ISP에서 Adobe에게 다시 보내는 컴플레인을 생성하면 전자 메일 주소가 자동으로 [제외 목록](../reports/suppression-list.md)에 추가되고 이후 게재에서 제외됩니다. 실제로 스팸으로 표시된 사용자에게 이메일을 보내면 보낸 사람의 신뢰도에 부정적인 영향을 미쳐 게재 가능성 문제가 발생할 수 있습니다. [스팸 불만 사항에 대해 자세히 알아보기](../reports/suppression-list.md#spam-complaints)

>[!IMPORTANT]
>
>모든 ISP가 Gmail과 같은 기존 FBL을 제공하는 것은 아닙니다. Gmail은 개별 수준 피드백을 제공하지 않으며, Google Postmaster 도구 내의 집계 수준 보고에 중점을 두고 개별 수신자에게 스팸 불만을 추적하는 데 사용할 수 없습니다. [자세히 알아보기](https://support.google.com/a/answer/6254652?hl=en){target="_blank"}

모든 Adobe 고객은 자동으로 다음 ISP의 기존 FBL에 등록됩니다.

* 1&amp;1

* AOL

* 블루타이

* 컴캐스트

* Fastmail

* 간디

* 이탈리아 온라인

* 라 포스트

* 리버티 글로벌 (첼로, UPC, 유니티 미디어)

* Locaweb

* Mail.RU

* Microsoft

* OpenSRS

* 랙 공간

* SEZNM

* SFR

* 실버스카이

* 스위스컴

* 시나코

* 텔레콤 이탈리아

* 텔레넷

* 텔레노르

* 텔스트라

* 테라

* UOL

* 버진 미디어

* Yahoo

* 직고

Adobe은 이러한 FBL을 정기적으로 감사하여 사용 가능한 최신 FBL이 추가되었는지 확인합니다.
