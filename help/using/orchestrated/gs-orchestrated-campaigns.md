---
solution: Journey Optimizer
product: journey optimizer
title: 오케스트레이션된 캠페인 시작
description: 오케스트레이션된 캠페인을 시작하는 방법 알아보기
short-description: 오케스트레이션된 캠페인 주요 기능 및 사용 사례 살펴보기
exl-id: 611dd06d-aa18-4fa3-a477-8a910cec21d8
version: Campaign Orchestration
source-git-commit: 97f9c32435667fecb950892ed6f6531085055e59
workflow-type: ht
source-wordcount: '652'
ht-degree: 100%

---


# 오케스트레이션된 캠페인 시작 {#orchestrated-camp}

>[!CONTEXTUALHELP]
>id="campaigns_overview_orchestrated"
>title="오케스트레이션된 캠페인 개요"
>abstract="<b>Campaign 오케스트레이션</b><br/>관계형 데이터 세트를 분할, 결합, 강화, 조작하여 대상자를 정의합니다<br/><br/> <b>다중 엔티티 데이터 활용</b><br/>오케스트레이션된 캠페인이 관계형 데이터 세트를 활용하여 세분화 및 개인화를 위한 데이터를 보강하는 방법 알아보기<br/><br/><b>애드혹 세분화 및 정확한 카운트</b><br/>정확한 카운트를 기반으로 단계별로 세그먼트 빌드<br/><br/><b>사용 가능한 채널</b><br/>이메일, SMS, 푸시 알림"

[!DNL Adobe Journey Optimizer]의 캠페인 오케스트레이션은 채널 전반에서 정교한 브랜드 주도 마케팅 캠페인의 기반이 됩니다. 이를 통해 대규모로 참여도, 매출, 고객 충성도를 높일 수 있습니다.

>[!IMPORTANT]
>
>캠페인 오케스트레이션에 액세스하려면 라이선스에 **Journey Optimizer - 캠페인 및 여정** 또는 **Journey Optimizer - 캠페인** 패키지가 포함되어야 합니다. 필요한 경우 Adobe 담당자에게 문의하여 라이선스를 확인하고 업데이트하십시오.

크로스 채널 마케팅은 필수적이지만 오케스트레이션된 캠페인을 통해 원활하게 이루어집니다. 드래그하여 놓는 시각적 인터페이스를 통해 세그먼테이션에서 메시지 게재에 이르기까지 여러 채널에 걸쳐 복잡한 마케팅 워크플로를 디자인하고 자동화할 수 있습니다. 속도, 제어 및 효율성을 위해 구축된 하나의 직관적인 환경에서 모든 작업이 수행됩니다.

![](assets/canvas-example-diagram.png){zoomable="yes"}

➡️ [비디오에서 오케스트레이션된 캠페인 살펴보기](#video-oc)

## 핵심 기능

캠페인 오케스트레이션은 다음 네 가지 주요 요소를 기반으로 구축됩니다.

<table style="table-layout:auto">
<tr style="border: 0;">
<td><img alt="온디맨드 대상자" src="assets/do-not-localize/icon-audience.svg" width="150px"></a></td><td><b>온디맨드 대상자</b><br/>데이터 세트 간 즉각적 쿼리를 통해 모든 데이터 형식과 차원의 조합을 자유롭게 사용하여 대상자 세그먼트를 만듭니다.</td></tr>
<tr style="border: 0;">
<td><img alt="다중 엔터티 세분화 및 전송" src="assets/do-not-localize/icon-entity.svg" width="150px"></a></td><td><b>다중 엔터티 세분화 및 전송</b><br/>개인 기반 캠페인을 넘어 제품 카탈로그, 스토어 위치 또는 서비스 데이터와 같은 엔터티를 사용하여 정밀하게 타기팅합니다.<br/><br/>
프로필 및 연결된 보조 엔터티별로 메시지가 하나씩 전송되는 다중 레벨 전송을 지원합니다. 이 보조 엔터티에는 연락처, 예약, 구독, 계약 또는 기타 연결된 데이터를 포함할 수 있습니다. 예를 들어 이 기능으로 프로필의 알려진 모든 주소 또는 해당 프로필과 연결된 각 예약에 대해 캠페인을 전송할 수 있습니다.</td></tr>
<tr style="border: 0;">
<td><img alt="사전 전송 가시성 및 정밀도" src="assets/do-not-localize/icon-visibility.svg" width="150px"></a></td><td><b>사전 전송 가시성 및 정밀도</b><br/>실행 전에 정확한 세분화 수와 전체 캠페인 범위를 가져와 정확성과 신뢰도를 보장합니다.</td></tr>
<tr style="border: 0;">
<td><img alt="여러 단계 캠페인 워크플로" src="assets/do-not-localize/icon-multistep.svg" width="150px"></a></td><td><b>여러 단계 캠페인 워크플로</b><br/>일별 메시지부터 시즌 프로모션 또는 주요 제품 출시와 같은 복잡한 캠페인에 이르기까지 여러 단계의 캠페인을 디자인합니다.</td></tr>
</table>


>[!NOTE]
>
>지원 채널: [이메일](../email/get-started-email.md), [SMS/MMS/RCS](../sms/get-started-sms.md), [푸시 알림](../push/get-started-push.md).
>
>사용 가능한 채널은 사용하는 라이선스 모델 및 추가 기능에 따라 다릅니다.

## 오케스트레이션된 캠페인 여정

오케스트레이션된 캠페인 시각화는 여정과 유사하지만 다양한 목적과 사용 사례를 해결합니다.

* **여정** - 각 프로필이 각자의 속도로 다른 단계를 진행하는 1:1 캔버스입니다. 각 고객의 상태는 해당 컨텍스트 내에서 유지되어 실시간 액션을 트리거합니다.

* **오케스트레이션된 캠페인** - 여정과 달리 오케스트레이션된 캠페인은 세그먼트를 계산하는 배치 캔버스를 사용하여 작동합니다. 모든 프로필이 동시에 한꺼번에 처리됩니다.

두 캔버스 모두 각각의 사용 사례에 최적화되어 있습니다. 여정 캔버스는 보다 긴 기간 동안 작동하는 경향이 있는 여정을 게시하는 반면, 캠페인 캔버스는 배치 캠페인의 반복적이고 점차 증가하는 실행을 위해 설계되었습니다.

## 오케스트레이션된 캠페인 속에는 무엇이 있을까요? {#gs-ms-campaign-inside}

오케스트레이션된 캠페인 캔버스는 어떤 일이 일어나야 하는지를 나타냅니다. 앞으로 수행할 다양한 작업과 이러한 작업이 어떻게 서로 연결되어 있는지 설명합니다.

![오케스트레이션된 캠페인 캔버스를 보여 주는 이미지](assets/canvas-example.png)

오케스트레이션된 캠페인마다 다음 항목이 포함됩니다.

* **활동**: 활동은 수행할 작업입니다. [다양한 활동](activities/about-activities.md)이 캔버스에 아이콘으로 표시됩니다. 각 활동에는 특정 속성과 모든 활동에 공통되는 다른 속성이 있습니다.

  오케스트레이션된 캠페인 캔버스에서는 특정 활동 하나가 여러 작업을 생성할 수 있습니다. 특히 루프 또는 반복 액션이 있는 경우에 그렇습니다.

* **전환**: 전환은 원본 활동을 대상 활동에 연결하고 해당 시퀀스를 정의합니다.

* **작업 테이블**: 작업 테이블에는 전환에 의해 전달되는 모든 정보가 포함됩니다. 오케스트레이션된 캠페인마다 여러 작업 테이블을 사용합니다. 이 테이블로 전달된 데이터는 오케스트레이션된 캠페인의 수명 주기 전체에서 사용할 수 있습니다.


## 소개 비디오 {#video-oc}

오케스트레이션된 캠페인의 주요 개념과 사용할 수 있는 기능에 대해 알아봅니다.


>[!VIDEO](https://video.tv.adobe.com/v/3471538/?learn=on&enablevpops)


## 더 자세히 알아보기

오케스트레이션된 캠페인이 무엇인지 이해했다면 이제 아래 설명서 섹션을 자세히 살펴보고 이 기능을 활용하여 작업을 시작할 차례입니다.

<table><tr style="border: 0; text-align: center;">
<td>
<a href="gs-campaign-creation.md">
<img alt="캠페인 액세스 및 관리" src="assets/do-not-localize/workflow-access.jpeg">
</a>
<div>
<a href="gs-campaign-creation.md"><strong>구성 단계</strong></a>
</div>
<p>
</td>
<td>
<a href="create-orchestrated-campaign.md">
<img alt="리드" src="assets/do-not-localize/workflow-create.jpeg">
</a>
<div><a href="create-orchestrated-campaign.md"><strong>오케스트레이션된 캠페인 만들기</strong>
</div>
<p>
</td>
<td>
<a href="activities/about-activities.md">
<img alt="드물게" src="assets/do-not-localize/workflow-activities.jpeg">
</a>
<div>
<a href="activities/about-activities.md"><strong>활동을 사용하여 작업</strong></a>
</div>
<p></td>
</tr></table>
