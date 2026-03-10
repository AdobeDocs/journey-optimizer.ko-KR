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
source-git-commit: 2240a4bf85d3f5f41a12d128afdc15431dbab75b
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 22%

---

# 랜딩 페이지 시작 {#get-started-lp}

랜딩 페이지는 사용자가 이메일이나 웹 사이트, 광고 또는 기타 디지털 위치를 클릭하면 이동하게 되는 독립형 웹 페이지입니다.

[!DNL Journey Optimizer]을(를) 사용하면 랜딩 페이지를 만들고 디자인하여 사용자가 커뮤니케이션 또는 뉴스레터와 같은 특정 서비스 수신을 옵트인하거나 옵트아웃할 수 있는 온라인 양식으로 사용자를 보낼 수 있습니다.

➡️ [이 비디오에서 구독을 구성하고 랜딩 페이지를 만드는 자세한 방법을 알아보십시오.](#video)

## 랜딩 페이지 사용 시기 {#when-to-use}

다음과 같은 작업을 수행할 때 랜딩 페이지를 사용합니다.

* 타겟팅된 서비스에 대한 구독 목록을 포함하여 이메일 또는 캠페인의 링크에서 고객이 마케팅 커뮤니케이션 또는 특정 서비스나 뉴스레터를 **옵트인 또는 옵트 아웃**&#x200B;하도록 합니다. [자세히 보기](lp-use-cases.md#subscription-to-a-service)
* 메시지를 보내기 전에 **동의를 수집**&#x200B;하고 옵트인 또는 옵트아웃 시 **확인 전자 메일**&#x200B;을 보냅니다. [자세히 보기](lp-use-cases.md#send-confirmation-email)
* **외부에서 외부 페이지를 만들지 않고**&#x200B;전용 웹 폼[!DNL Journey Optimizer]&#x200B;(으)로 사용자 리디렉션
* **의 콘텐츠 디자인 기능을 사용하여**&#x200B;응답형 랜딩 페이지[!DNL Journey Optimizer]를 빌드합니다.

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
<a href="design-lp.md">
<img alt="유효성 검사" src="../assets/do-not-localize/lp-design.jpg">
</a>
<div>
<a href="design-lp.md"><strong>랜딩 페이지 디자인</strong></a>
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

1. [**하위 도메인 구성**](lp-subdomains.md) — 랜딩 페이지 호스팅 전용 하위 도메인을 설정합니다.
1. [**랜딩 페이지 사전 설정 만들기**](lp-presets.md#lp-create-preset) — 사전 설정은 랜딩 페이지에 적용되는 하위 도메인 및 기타 설정을 정의합니다.
1. [**구독 목록 만들기**](subscription-list.md)(구독 사용 사례의 경우) - 고객이 특정 서비스를 구독하거나 구독 취소하도록 하려는 경우 필요합니다.

## 작동 방식 {#how-it-works}

랜딩 페이지를 만들고 배포하는 절차는 다음과 같습니다.

1. [**랜딩 페이지 만들기 및 구성**](create-lp.md) — 사전 설정을 선택하고 기본 페이지를 설정하고 필요한 하위 페이지를 추가합니다.
1. [**페이지 디자인**](design-lp.md) — [!DNL Journey Optimizer]의 드래그 앤 드롭 편집기를 사용하여 페이지 콘텐츠와 양식을 작성합니다.
1. 랜딩 페이지 [**테스트**](create-lp.md#test-landing-page) 및 [**게시**](create-lp.md#publish-landing-page) — 페이지를 미리 보고, 양식 동작을 테스트한 다음 게시하여 라이브로 만드십시오.
1. [**메시지 또는 여정에 연결**](../email/message-tracking.md#insert-links) - 고객이 연결할 수 있도록 랜딩 페이지 URL을 전자 메일, 캠페인 또는 여정 작업에 추가합니다.

## 사용 방법 비디오{#video}

아래 비디오에서는 구독 목록을 만들고, 서비스를 옵트인 또는 옵트아웃하도록 랜딩 페이지를 설정하고, 옵트인/옵트아웃 옵션을 메시지에 통합하고, 관련 여정을 구성하는 방법을 보여 줍니다.

>[!VIDEO](https://video.tv.adobe.com/v/344401?captions=kor&quality=12&learn=on)
