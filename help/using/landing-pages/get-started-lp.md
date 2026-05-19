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
TQID: https://experienceleague.adobe.com/wr4XGNostKoN8jZ50VRAQPoGg9tsNhMOyJGEt1mASso
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: b19d9237-76be-466d-a869-aacf2d72205f
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 1e0a06dddba6c5ca4c53e4b143eb7fa7763ded6b
workflow-type: tm+mt
source-wordcount: 735
ht-degree: 96%

---

# 랜딩 페이지 시작 {#get-started-lp}

랜딩 페이지는 사용자가 이메일이나 웹 사이트, 광고 또는 기타 디지털 위치를 클릭하면 이동하게 되는 독립형 웹 페이지입니다.

[!DNL Journey Optimizer]를 사용하면 사용자가 온라인 양식으로 이동하여 뉴스레터와 같은 특정 서비스 또는 기타 정보 수신을 옵트인하거나 옵트아웃할 수 있도록 하는 랜딩 페이지를 만들고 디자인할 수 있습니다.

➡️ [이 비디오에서 구독을 구성하고 랜딩 페이지를 만드는 자세한 방법을 알아보십시오.](#video)

## 랜딩 페이지 사용 시기 {#when-to-use}

다음과 같은 경우 랜딩 페이지 사용

* 이메일이나 캠페인의 링크를 통해 고객이 마케팅 커뮤니케이션이나 특정 서비스 또는 뉴스레터 수신을 **옵트인하거나 옵트아웃**&#x200B;할 수 있도록 합니다. 여기에는 타겟 서비스 구독 목록도 포함됩니다. [자세히 보기](lp-use-cases.md#subscription-to-a-service)
* 커뮤니케이션 자료를 보내기 전에 **동의를 받고** 옵트인 또는 옵트아웃 시 **확인 이메일**&#x200B;을 보냅니다. [자세히 보기](lp-use-cases.md#send-confirmation-email)
* **[!UICONTROL 데이터 캡처]** 랜딩 페이지의 양식을 사용하여 **프로필 데이터를 캡처하거나 업데이트**&#x200B;합니다. 점진적 프로파일링, 환경 설정, 등록 및 유사한 시나리오에 사용됩니다. [자세히 보기](#data-capture-lp)
* [!DNL Journey Optimizer] 외부에 별도의 페이지를 구축하지 않고 사용자를 **전용 웹 양식**&#x200B;으로 리디렉션합니다.
* [!DNL Journey Optimizer]의 콘텐츠 디자인 기능을 사용하여 **반응형 랜딩 페이지**&#x200B;를 구축합니다.

### 랜딩 페이지를 사용한 데이터 캡처 {#data-capture-lp}

**[!UICONTROL 데이터 캡처]** 랜딩 페이지를 사용하면 게시된 양식을 임베드하여 방문자가 속성을 제출할 수 있으며, 제출된 속성은 양식 사전 설정에 구성된 스트리밍 연결을 통해 [!DNL Adobe Experience Platform] 데이터 세트에 기록됩니다. [랜딩 페이지에서 양식을 만들고 임베드하는 방법 알아보기](lp-forms.md)

>[!NOTE]
>
>랜딩 페이지 양식을 통한 데이터 캡처는 **알려진 프로필**([!DNL Adobe Experience Platform]에서 식별된 기존 프로필)에 대해 지원됩니다. 랜딩 페이지는 **개인화된 링크**(예: 이메일 캠페인)를 통해 열려야 페이지 로드 시 프로필 ID를 확인할 수 있습니다.

다음은 사용 사례의 예입니다.

1. **점진적 프로필 강화** — 개인화된 랜딩 페이지를 통해 기존 고객으로부터 전화번호, 생년월일, 위치와 같은 추가 속성을 수집하여 세분화 및 개인화를 위해 기존 [!DNL Experience Platform] 프로필을 강화합니다.

2. **환경설정 센터 업데이트** — 기존 구독자가 랜딩 페이지를 통해 커뮤니케이션 환경설정(채널, 관심 주제)을 관리할 수 있도록 하며, 변경 사항은 일반적으로 약 15분 이내에 [!DNL Experience Platform] 프로필에 반영됩니다.

3. **이벤트 또는 웨비나 등록** — 등록 페이지에서 기존 프로필의 이벤트별 데이터를 수집하고, 등록 속성으로 프로필을 업데이트하며, 확인 여정을 시작합니다.

4. **충성도 또는 프로그램 등록** — 기존 고객이 랜딩 페이지를 통해 추가 정보를 제출하여 충성도 프로그램이나 멤버십 등급에 등록할 수 있도록 하여 다운스트림 타겟팅을 위한 프로필을 강화합니다.

5. **경품 행사 또는 이벤트 참여** — 기존 고객이 랜딩 페이지 양식을 통해 경품 행사 또는 이벤트에 참여할 수 있도록 합니다. 참여 관련 세부 정보(답변, 선호 사항 또는 선언)를 수집하여 자격 심사, 당첨자 선정 및 후속 여정을 지원하기 위해 프로필에 기록합니다.

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
<img alt="저빈도" src="../assets/do-not-localize/lp-list.jpg">
</a>
<div>
<a href="subscription-list.md"><strong>구독 목록 만들기</strong></a>
</div>
<p></td>
<td>
<a href="lp-forms.md">
<img alt="Journey Optimizer의 랜딩 페이지용 양식 목록" src="../assets/do-not-localize/lp-design.jpg">
</a>
<div>
<a href="lp-forms.md"><strong>랜딩 페이지의 양식 사용</strong></a>
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

랜딩 페이지를 만들기 전에 다음 설정 단계를 완료하세요.

1. **하위 도메인 구성** — 랜딩 페이지 호스팅 전용 하위 도메인을 설정합니다. [자세히 알아보기](lp-subdomains.md)
1. **랜딩 페이지 사전 설정 생성** — 사전 설정은 랜딩 페이지에 적용되는 하위 도메인과 기타 설정을 정의합니다. [자세히 알아보기](lp-presets.md#lp-create-preset)
1. **구독 목록 생성**(구독 사용 사례용) — 고객이 특정 서비스를 구독하거나 구독을 취소할 수 있도록 하려면 필수입니다. [자세히 알아보기](subscription-list.md)
1. **양식 생성**(데이터 캡처 사용 사례용) — **[!UICONTROL 데이터 캡처]** 랜딩 페이지에 양식을 삽입하고 제출된 내용을 [!DNL Experience Platform]에 보내려는 경우 필수입니다. [자세히 알아보기](lp-forms.md)

## 작동 방식 {#how-it-works}

랜딩 페이지 생성 및 배포는 다음 순서로 진행됩니다.

1. **랜딩 페이지 생성 및 구성** — 사전 설정을 선택하고 기본 페이지를 설정하며 필요한 하위 페이지를 추가합니다. [자세히 알아보기](create-lp.md#create-landing-page)
1. **페이지 디자인** — [!DNL Journey Optimizer]의 드래그 앤 드롭 편집기를 사용하여 페이지 콘텐츠와 양식을 만듭니다. [자세히 알아보기](design-lp.md)
1. **랜딩 페이지 테스트 및 게시** — 페이지를 미리 보고, 양식 동작을 테스트한 다음, 게시하여 라이브로 보냅니다. [자세히 알아보기](create-lp.md#test-landing-page)
1. **메시지 또는 여정의 링크** - 고객이 랜딩 페이지에 도달할 수 있도록 이메일, 캠페인 또는 여정 액션에 URL을 추가합니다. [자세히 알아보기](../email/message-tracking.md#insert-links)

## 사용 방법 비디오{#video}

아래 비디오에서는 구독 목록을 만들고, 서비스 옵트인/옵트아웃을 위한 랜딩 페이지를 설정하고, 메시지에 옵트인/옵트아웃 옵션을 통합하고, 관련 여정을 구성하는 방법을 확인할 수 있습니다.

>[!VIDEO](https://video.tv.adobe.com/v/344401?captions=kor&quality=12&learn=on)

➡️ **실제로 보기:** 구독 관리, 확인 전자 메일 및 데이터 캡처 시나리오에 대한 단계별 예제를 보려면 [랜딩 페이지 사용 사례](lp-use-cases.md)를 살펴보십시오.
