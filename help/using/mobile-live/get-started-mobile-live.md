---
solution: Journey Optimizer
product: journey optimizer
title: 라이브 활동 시작
description: Journey Optimizer에서 라이브 활동을 보내는 방법 알아보기
topic: Content Management
role: User
level: Beginner
exl-id: c9766603-df19-4efd-8319-27e9764254b4
TQID: https://experienceleague.adobe.com/IB00r0QSfCthvgvyqubGwsaUoiJKBL-E96duLn4R5i0
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: c96d2aa5-76a2-443d-8d23-5de95577c909
  - id: ed2fba79-65cb-4680-96d2-2ad5d851714d
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 0977b7c36d8556d4aaed43f4b94abb4ccacd2305
workflow-type: tm+mt
source-wordcount: 449
ht-degree: 84%

---

# 라이브 활동 시작 {#get-started-mobile-live}

>[!BEGINSHADEBOX]

**이 페이지에서:** 라이브 활동이 iPhone 잠금 화면 및 Dynamic Island에서 지속적인 실시간 업데이트를 제공하므로 진행 중인 이벤트 동안 사용자의 참여를 유지하고 Adobe Journey Optimizer으로 보내는 데 필요한 구성 및 API 트리거 캠페인을 계획할 수 있습니다.

>[!ENDSHADEBOX]

라이브 활동은 디바이스 잠금 화면에 표시되는 지속적이고 매력적인 UI 요소입니다. 이 활동을 사용하면 앱이 최신 정보를 실시간으로 제공할 수 있습니다. 즉, 사용자가 앱을 열거나 반복적인 푸시 알림을 받지 않고도 이벤트가 지속되는 동안 정보를 확인할 수 있습니다.

>[!AVAILABILITY]
>
>Adobe Journey Optimizer의 라이브 활동은 Apple iOS에만 호환됩니다.

기존의 푸시 알림과 달리 라이브 활동은 **상태 기반 참여**&#x200B;를 나타냅니다. 즉, 일회성 알림을 제공하는 대신 이벤트가 발전함에 따라 동적으로 업데이트되는 연속적이고 상황에 맞는 존재감을 유지합니다.


<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<img alt="iOS 잠금 화면 및 Dynamic Island의 라이브 활동" src="assets/do-not-localize/live-activity.jpeg">
</td>
<td>
<p><strong>주요 이점</strong></p>
<p>라이브 활동은 모바일 참여를 알림 기반에서 상태 기반으로 전환하여 브랜드가 다음 목표를 달성하도록 지원합니다.</p>
<ul>
<li>가치가 높은 이벤트 기간 내내 잠금 화면에서 <strong>지속적인 존재감</strong> 유지</li>
<li>반복된 알림으로 사용자에게 부담을 주지 않으면서 <strong>정보를 동적으로 업데이트</strong></li>
<li>실제 이벤트에 연결된 <strong>보다 풍부하고 상황에 맞는</strong> 모바일 순간 제공</li>
<li>활성 트랜잭션 또는 라이브 경험 중 <strong>참여도 및 유지율 증가</strong></li>
</ul>
</td>
</tr>
</table>

Adobe Journey Optimizer를 사용하면 API 트리거 캠페인을 통해 프로그래밍 방식으로 **시작**, **업데이트**, **종료** 라이브 활동을 원격 수행할 수 있습니다. 이는 개인별 및 대상자 기반 사용 사례를 모두 대규모로 지원합니다.

**API 트리거** 캠페인을 통해 라이브 활동을 **only**&#x200B;할 수 있으므로 사용자 지정 페이로드를 제공하고 자체 페이로드를 통해 모든 개인화를 수행할 수 있습니다.
의도한 라이브 활동 사용 사례를 기반으로 적절한 **API-triggered** 캠페인 유형을 선택해야 합니다.

* 브로드캐스트 사용 사례의 경우 **API 트리거된 마케팅**&#x200B;을 선택합니다. 대상자 기반 업데이트가 대규모로 전송됩니다.

   * 스포츠 점수 및 라이브 이벤트 카운트
   * 경로의 모든 승객에게 비행 상태 업데이트
   * 사용자 세그먼트 전체에 걸쳐 공유 경험

* 개인별 사용 사례의 경우 **API 트리거 트랜잭션**&#x200B;을 선택합니다. 사용자별로 1:1 실시간 업데이트가 전송됩니다.

   * 주문 추적 및 배송 진행 상황
   * 승차 또는 서비스 상태 업데이트
   * 실시간 예약 및 약속 확인

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

Adobe Journey Optimizer로 iOS 라이브 활동을 구성하여 iPhone 잠금 화면 및 Dynamic Island에서 다양한 실시간 업데이트를 제공하는 방법에 대해 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/3479864/?learn=on)
