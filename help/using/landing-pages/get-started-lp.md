---
solution: Journey Optimizer
product: journey optimizer
title: 랜딩 페이지 시작
description: Journey Optimizer의 랜딩 페이지에 대해 알아보기
feature: Landing Pages, Subscriptions
topic: Content Management
role: User
level: Beginner
keywords: 랜딩, 랜딩 페이지, 시작, 시작하기
exl-id: 0da96e32-52ad-4cc3-bac4-844b1f39ed16
source-git-commit: d0dd382521aeb2c7e18dc547c2ec55fa1472ab8d
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 14%

---

# 랜딩 페이지 시작 {#get-started-lp}

랜딩 페이지는 사용자가 이메일이나 웹 사이트, 광고 또는 기타 디지털 위치를 클릭하면 이동하게 되는 독립형 웹 페이지입니다.

[!DNL Journey Optimizer]을(를) 사용하면 랜딩 페이지를 만들고 디자인하여 사용자가 커뮤니케이션 또는 뉴스레터와 같은 특정 서비스 수신을 옵트인하거나 옵트아웃할 수 있는 온라인 양식으로 사용자를 보낼 수 있습니다.

➡️ [이 비디오에서 구독을 구성하고 랜딩 페이지를 만드는 자세한 방법을 알아보십시오.](#video)

## 랜딩 페이지 사용 시기 {#when-to-use}

다음과 같은 작업을 수행할 때 랜딩 페이지를 사용합니다.

* 타겟팅된 서비스에 대한 구독 목록을 포함하여 이메일 또는 캠페인의 링크에서 고객이 마케팅 커뮤니케이션 또는 특정 서비스나 뉴스레터를 **옵트인 또는 옵트 아웃**&#x200B;하도록 합니다. [자세히 보기](lp-use-cases.md#subscription-to-a-service)
* 메시지를 보내기 전에 **동의를 수집**&#x200B;하고 옵트인 또는 옵트아웃 시 **확인 전자 메일**&#x200B;을 보냅니다. [자세히 보기](lp-use-cases.md#send-confirmation-email)
* **데이터 캡처** 랜딩 페이지에서 양식을 사용하여 프로필 데이터를 **[!UICONTROL 캡처 또는 업데이트]**(점진적 프로파일링, 환경 설정, 등록 및 유사한 시나리오). [자세히 보기](#data-capture-lp)
* **외부에서 외부 페이지를 만들지 않고**&#x200B;전용 웹 폼[!DNL Journey Optimizer]&#x200B;(으)로 사용자 리디렉션
* **의 콘텐츠 디자인 기능을 사용하여**&#x200B;응답형 랜딩 페이지[!DNL Journey Optimizer]를 빌드합니다.

### 랜딩 페이지를 사용한 데이터 캡처 {#data-capture-lp}

**[!UICONTROL 데이터 캡처]** 랜딩 페이지를 사용하면 게시된 양식을 포함할 수 있으므로 방문자가 양식 사전 설정에 구성된 스트리밍 연결을 통해 [!DNL Adobe Experience Platform] 데이터 집합에 작성된 특성을 제출할 수 있습니다. [랜딩 페이지에서 양식을 만들고 임베드하는 방법을 알아보세요](lp-forms.md)

>[!NOTE]
>
>랜딩 페이지 양식을 통한 데이터 캡처는 **알려진 프로필**([!DNL Adobe Experience Platform]에서 식별된 기존 프로필)에 대해 지원됩니다. 페이지가 로드될 때 프로필 ID를 확인할 수 있도록 **개인화된 링크**(예: 이메일 캠페인)에서 랜딩 페이지를 열어야 합니다.

다음은 사용 사례의 예입니다.

1. **점진적 프로필 강화** — 개인 맞춤화된 랜딩 페이지를 통해 전화 번호, 생년월일 또는 위치와 같은 알려진 고객의 추가 특성을 수집하여 세분화 및 개인화를 위해 기존 [!DNL Experience Platform] 프로필을 보강합니다.

2. **기본 설정 센터 업데이트** — 알려진 구독자가 랜딩 페이지를 통해 커뮤니케이션 기본 설정(채널, 주제 관심 분야)을 관리할 수 있도록 허용합니다. 변경 내용은 일반적으로 [!DNL Experience Platform] 프로필에 약 15분 내에 반영됩니다.

3. **이벤트 또는 웨비나 등록** — 등록 페이지의 알려진 프로필에서 이벤트 관련 데이터를 캡처하고, 등록 특성으로 프로필을 업데이트하고, 확인 여정을 트리거합니다.

4. **충성도 또는 프로그램 등록** — 기존 고객이 랜딩 페이지를 통해 추가 세부 정보를 제출하여 충성도 프로그램 또는 멤버십 계층에 등록할 수 있도록 하여 다운스트림 타겟팅을 위한 프로필을 보강합니다.

5. **경쟁 또는 경연 참가** - 알려진 고객이 랜딩 페이지 양식을 통해 경쟁이나 경품 행사에 참가할 수 있도록 하고, 참가자별 세부 정보(답변, 환경 설정 또는 선언)를 캡처하여 프로필에 작성함으로써 자격요건, 우승자 선택 및 후속 여정을 지원합니다.

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="create-lp.md">
<img alt="리드" src="../assets/do-not-localize/lp-subscription.jpeg">
</a>
<div><a href="create-lp.md"><strong>랜딩 페이지 만들기</strong>
</div>
<p>
</td>
<td>
<a href="subscription-list.md">
<img alt="드물게" src="../assets/do-not-localize/lp-list.jpg">
</a>
<div>
<a href="subscription-list.md"><strong>구독 목록 만들기</strong></a>
</div>
<p></td>
<td>
<a href="lp-forms.md">
<img alt="Journey Optimizer의 랜딩 페이지 Forms 목록" src="../assets/do-not-localize/lp-design.jpg">
</a>
<div>
<a href="lp-forms.md"><strong>랜딩 페이지에서 양식 사용</strong></a>
</div>
<p>
</td>
<td>
<a href="../reports/lp-report-live.md">
<img alt="유효성 검사" src="../assets/do-not-localize/lp-reporting.jpg">
</a>
<div>
<a href="../reports/lp-report-live.md"><strong>보고</strong></a>
</div>
<p>
</td>
</tr></table>

## 시작하기 전에 {#prerequisites}

랜딩 페이지를 만들기 전에 다음 설정 단계를 완료하십시오.

1. **하위 도메인 구성** — 랜딩 페이지 호스팅 전용 하위 도메인을 설정합니다. [자세히 알아보기](lp-subdomains.md)
1. **랜딩 페이지 사전 설정 만들기** — 사전 설정은 랜딩 페이지에 적용되는 하위 도메인 및 기타 설정을 정의합니다. [자세히 알아보기](lp-presets.md#lp-create-preset)
1. **구독 목록 만들기**(구독 사용 사례의 경우) - 고객이 특정 서비스를 구독하거나 구독 취소하도록 하려는 경우 필요합니다. [자세히 알아보기](subscription-list.md)
1. **양식 만들기**(데이터 캡처 사용 사례의 경우) — **[!UICONTROL 데이터 캡처]** 랜딩 페이지에 양식을 포함하고 [!DNL Experience Platform]&#x200B;(으)로 제출을 전송하려는 경우 필요합니다. [자세히 알아보기](lp-forms.md)

## 작동 방식 {#how-it-works}

랜딩 페이지를 만들고 배포하는 절차는 다음과 같습니다.

1. **랜딩 페이지 만들기 및 구성** — 사전 설정을 선택하고 기본 페이지를 설정하고 필요한 하위 페이지를 추가합니다. [자세히 알아보기](create-lp.md#create-landing-page)
1. **페이지 디자인** — [!DNL Journey Optimizer]의 드래그 앤 드롭 편집기를 사용하여 페이지 콘텐츠와 양식을 작성합니다. [자세히 알아보기](design-lp.md)
1. **랜딩 페이지 테스트 및 게시** - 페이지를 미리 보고, 양식 동작을 테스트한 다음 게시하여 라이브로 만드십시오. [자세히 알아보기](create-lp.md#test-landing-page)
1. **메시지 또는 여정에 연결** - 고객이 연결할 수 있도록 랜딩 페이지 URL을 전자 메일, 캠페인 또는 여정 작업에 추가합니다. [자세히 알아보기](../email/message-tracking.md#insert-links)

## 사용 방법 비디오{#video}

아래 비디오에서는 구독 목록을 만들고, 서비스를 옵트인 또는 옵트아웃하도록 랜딩 페이지를 설정하고, 옵트인/옵트아웃 옵션을 메시지에 통합하고, 관련 여정을 구성하는 방법을 보여 줍니다.

>[!VIDEO](https://video.tv.adobe.com/v/341280?quality=12&learn=on)
