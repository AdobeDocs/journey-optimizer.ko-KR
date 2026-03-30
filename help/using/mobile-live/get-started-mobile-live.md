---
solution: Journey Optimizer
product: journey optimizer
title: 라이브 활동 시작하기
description: Journey Optimizer에서 라이브 활동을 보내는 방법 알아보기
topic: Content Management
role: User
level: Beginner
exl-id: c9766603-df19-4efd-8319-27e9764254b4
source-git-commit: c6b36f31af29d21053cc455fd5dbba68ed5af63b
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 20%

---

# 라이브 활동 시작하기 {#get-started-mobile-live}


라이브 활동은 장치 잠금 화면에 표시되는 영구적이고 매력적인 UI 요소입니다. 이를 통해 앱에서 최신 정보를 실시간으로 제공할 수 있습니다. 즉, 앱을 열거나 반복적인 푸시 알림을 받지 않고도 사용자가 지속적인 이벤트 동안 알림을 받을 수 있습니다.

>[!AVAILABILITY]
>
>Adobe Journey Optimizer의 라이브 활동은 Apple iOS과만 호환됩니다.

기존의 푸시 알림과 달리 라이브 활동은 **상태 기반 참여**&#x200B;를 나타냅니다. 일회성 알림을 제공하는 대신 이벤트가 발전함에 따라 동적으로 업데이트되는 지속적이고 상황별 상태를 유지합니다.


<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<img alt="잠금 화면 및 Dynamic Island의 iOS 라이브 활동" src="assets/do-not-localize/live-activity.jpeg">
</td>
<td>
<p><strong>주요 이점</strong></p>
<p>라이브 활동은 모바일 참여를 알림 기반에서 상태 기반으로 전환하여 브랜드가 다음을 수행할 수 있도록 합니다.</p>
<ul>
<li>가치가 높은 이벤트 전체에서 잠금 화면에서 <strong>지속적인 현재 상태</strong>를 유지합니다.</li>
<li>반복된 알림으로 압도적인 사용자 없이 <strong>정보를 동적으로 업데이트</strong></li>
<li>실제 이벤트에 연결된 <strong>풍부하고 상황에 맞는</strong>개의 모바일 순간 제공</li>
<li>활성 트랜잭션 또는 라이브 경험 중에 <strong>참여 및 유지 증가</strong></li>
</ul>
</td>
</tr>
</table>

Adobe Journey Optimizer을 사용하면 API 트리거 캠페인을 통해 원격으로 **시작**, **업데이트** 및 **종료** 라이브 활동을 프로그래밍 방식으로 수행할 수 있습니다. 이는 규모에 따라 개별 및 대상 기반 사용 사례를 모두 지원합니다.

**API 트리거** 캠페인을 통해 라이브 활동을 **only**&#x200B;할 수 있으므로 사용자 지정 페이로드를 제공하고 자체 페이로드를 통해 모든 개인화를 수행할 수 있습니다.
의도한 라이브 활동 사용 사례를 기반으로 적절한 **API-triggered** 캠페인 유형을 선택해야 합니다.

* 브로드캐스트 사용 사례에 대해 **API 트리거된 마케팅**&#x200B;을(를) 선택합니다. 대상 기반 업데이트는 대규모로 전송됩니다.

   * 스포츠 점수 및 라이브 이벤트 카운트
   * 경로의 모든 승객에 대한 비행 상태 업데이트
   * 사용자 세그먼트 전체에 걸쳐 공유된 경험

* 개별 사용 사례에 대해 **API 트리거 트랜잭션**&#x200B;을(를) 선택합니다. 사용자당 실시간 업데이트 1:1개:

   * 주문 추적 및 게재 진행률
   * 승차 또는 서비스 상태 업데이트
   * 실시간 예약 및 예약 확인

## 빠른 시작 안내서

아래 단계를 완료하여 애플리케이션에서 라이브 활동을 구성하고 구현하세요.

1. **[Adobe Journey Optimizer 구성하기](mobile-live-configuration.md)**

   모바일 구성을 만들어 환경을 설정합니다.

1. **[Adobe Experience Platform Mobile SDK 통합](mobile-live-configuration-sdk.md)**

   Adobe Experience Platform Mobile SDK와 통합하여 잠금 화면 및 Dynamic Island에서 실시간 동적 업데이트를 가능하게 합니다.

1. **[Journey Optimizer에서 라이브 활동 만들기](create-mobile-live.md)**

   Journey Optimizer에서 API 트리거 캠페인을 사용하여 라이브 활동을 시작합니다.

1. **[캠페인 추적](../reports/campaign-global-report-cja-activity.md)**

   기본 제공 보고서를 통해 라이브 활동의 영향을 측정하기 시작합니다.

## 사용 방법 비디오

Adobe Journey Optimizer을 사용하여 iOS 라이브 활동을 구성하여 iPhone 잠금 화면 및 Dynamic Island에서 다양한 실시간 업데이트를 제공하는 방법에 대해 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/3479864/?learn=on)
