---
title: 인앱 메시지 시작
description: Journey Optimizer로 인앱 알림을 보내는 방법 알아보기
feature: In App
topic: Content Management
role: User
level: Beginner
keywords: 인앱, 메시지, 만들기, 시작
exl-id: 51562843-7b50-4eb5-bf79-5ce03f7549cb
TQID: https://experienceleague.adobe.com/b139LQsPe3HwKe1O5cyBx4Nj4jpW3GXCFIVIWTAIlbg
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dffid: cc5c44e2-54a1-4927-b794-442cd87d8f74id: c96d2aa5-76a2-443d-8d23-5de95577c909id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 75ebd043971ce40e2da0f627622441a46a8e667c
workflow-type: ht
source-wordcount: 601
ht-degree: 100%

---

# 인앱 채널 시작하기 {#gs-in-app}

>[!BEGINSHADEBOX]

**이 페이지의 내용:** Adobe Journey Optimizer의 인앱 메시징 채널을 사용하여 앱 사용자에게 기능, 혜택, 온보딩을 홍보하는 알림을 보내 참여를 유도합니다.

>[!ENDSHADEBOX]

인앱 메시지는 앱 안에 있는 사용자에게 보내어 특정 관심 영역으로 안내할 수 있는 알림입니다. 이 알림은 새로운 기능을 홍보하거나, 특별 오퍼를 제공하거나, 사용자의 앱 적응을 돕는 등 다양한 용도로 사용할 수 있습니다. 인앱 메시지를 활용하면 대상자와 효과적으로 소통하고 애플리케이션의 중요한 부분을 안내할 수 있습니다.

Journey Optimizer를 사용하여 인앱 알림을 만들고 경험 옵션(메시지의 레이아웃과 표시, 텍스트, 버튼 옵션 등)을 구성합니다.

</br>

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="inapp-configuration.md">
<img alt="유효성 검사" src="../assets/do-not-localize/inapp-config.jpg">
</a>
<div>
<a href="inapp-configuration.md"><strong>인앱 채널 구성</strong></a>
</div>
<p>
</td>
<td>
<a href="create-in-app.md">
<img alt="리드" src="../assets/do-not-localize/inapp-create.jpeg">
</a>
<div><a href="create-in-app.md"><strong>인앱 메시지 만들기</strong>
</div>
<p>
</td>
<td>
<a href="design-in-app.md">
<img alt="드물게" src="../assets/do-not-localize/inapp-design.jpg">
</a>
<div>
<a href="design-in-app.md"><strong>인앱 콘텐츠 디자인</strong></a>
</div>
<p></td>
<td>
<a href="../reports/campaign-global-report-cja-inapp.md">
<img alt="유효성 검사" src="../assets/do-not-localize/inapp-report.jpg">
</a>
<div>
<a href="../reports/campaign-global-report-cja-inapp.md"><strong>인앱 보고서 액세스</strong></a>
</div>
<p>
</td>
</tr></table>

## 사용 사례

인앱 메시지는 사용자가 이미 앱을 사용하는 동안 해당 순간을 적극 활용하여 사용자를 안내하거나 영향을 미치고자 할 때 가장 적합합니다.

| 이점 | 이유 | 사용 사례 예시 |
| --- | --- | --- |
| 높은 사용자 참여 | 사용자가 앱 세션에서 활동 중일 때 사용자에게 도달합니다 | 기능 공지, 온보딩 팁 |
| 상황에 맞는 트리거 | 인앱 동작 또는 위치를 기반으로 트리거될 수 있습니다 | 사용자가 관련 화면을 방문한 직후 기능 강조 표시 |
| 실시간 전달 | 푸시 토큰 또는 외부 게재 서비스에 대한 종속성 없음 | 현재 세션 중에 적절한 시점에 표시되는 프롬프트 |
| 외부 채널에 대한 종속성 없음 | 다른 채널의 옵트인 상태에 관계없이 앱 내에서 완전히 작동합니다 | 푸시 알림을 옵트아웃한 사용자에게 도달 |
| 더 나은 전환 잠재력 | 집중하고 있는 순간에 전달되어 응답률을 높입니다 | 업셀 또는 크로스셀 오퍼, 설문 조사 프롬프트 |
| 사용자 지정 및 세분화 | 레이아웃, 텍스트 및 버튼은 특정 대상에 맞게 조정할 수 있습니다 | 다양한 사용자 세그먼트에 대한 개인화된 온보딩 흐름 |
| 방해되지 않는 디자인 | 사용자 경험을 방해하지 않고 보완하도록 디자인 가능 | 앱의 UI에 맞는 배너 또는 모달 |

## 사용하지 말아야 할 경우

인앱 메시지는 활성 세션에 따라 다르므로 모든 시나리오에 적합하지 않습니다. 다음과 같은 상황에서는 다른 채널을 고려하세요.

* 사용자가 앱을 적극적으로 사용하지 않아 메시지가 표시되지 않는 경우
* 앱 외부에서도 사용자에게 전달해야 하는 중요하거나 긴급한 메시지인 경우(예: 중단 또는 보안 경고)
* 커뮤니케이션이 규제 또는 법적 사안과 관련되어 있어 인앱 메시지가 제공할 수 없는 읽음 확인이 필요한 경우
* 앱을 열 가능성이 낮은 비활성 사용자를 위한 계정 재활성화 또는 재참여 캠페인이 목표인 경우
* 주문 확인과 같은 대량 트랜잭션 업데이트 메시지로 이메일 또는 SMS가 더 적합한 경우
* 과다 사용이 배너 맹목으로 이어지고, 사용자가 너무 자주 나타나는 메시지를 무시하기 시작하는 경우
* 메시지가 전달되어야 하는 시점에 사용자가 오프라인 상태이거나 앱 연결이 없는 경우



## 추가 리소스

* **[인앱 메시지 만들기](create-in-app.md)** - 모바일 애플리케이션용 인앱 메시지를 만들고 구성하는 방법에 대해 알아봅니다.
* **[인앱 채널 구성](inapp-configuration.md)** - 적절한 모바일 앱 구성을 사용하여 인앱 메시지 채널을 설정합니다.
* **[인앱 콘텐츠 디자인](design-in-app.md)** - 인앱 메시지 레이아웃, 스타일, 버튼, 인터랙티브한 요소를 사용자 정의합니다.
* **[웹용 인앱](create-in-app-web.md)** - 웹 애플리케이션용 인앱 메시지를 만들고 게재하는 방법을 알아봅니다.
* **[인앱 채널 튜토리얼](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/tutorials/channels/in-app-channel/in-app-messages-overview){target="_blank"}** - 인앱 메시지 기능과 모범 사례에 대한 단계별 비디오 튜토리얼을 살펴봅니다.

