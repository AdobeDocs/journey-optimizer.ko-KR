---
solution: Journey Optimizer
product: journey optimizer
title: API에서 트리거된 캠페인 콘텐츠 편집
description: API에서 트리거된 캠페인 콘텐츠를 편집하는 방법을 알아봅니다.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: 캠페인, API 트리거, REST, 최적화 도구, 메시지
exl-id: b7f12c65-c1af-4c49-b126-c13a51940a43
source-git-commit: 93698c93f3750b4d7feff18509f8144a7c79f156
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 2%

---

# API에서 트리거된 캠페인 콘텐츠 편집 {#api-content}

메시지 콘텐츠를 구성하려면 **[!UICONTROL 콘텐츠]** 탭으로 이동하거나 **[!UICONTROL 콘텐츠 편집]** 단추를 클릭합니다.

![](assets/campaign-content.png)

## 콘텐츠 디자인 {#design}

콘텐츠 만들기 프로세스는 선택한 채널에 따라 다릅니다. 다음 페이지에서 메시지 콘텐츠를 만드는 자세한 단계를 배웁니다.

<table style="table-layout:fixed"><tr style="border: 0;">
<td><a href="../email/create-email.md"><img alt="이메일" src="../channels/assets/do-not-localize/email.png"></a>
<div align="center"><a href="../email/create-email.md"><strong>이메일</strong></a></div></td>
<td><a href="../sms/create-sms.md"><img alt="sms" src="../channels/assets/do-not-localize/sms.png"></a>
<div align="center"><a href="../sms/create-sms.md"><strong>SMS</strong></a></div></td>
<td><a href="../push/create-push.md"><img alt="푸시" src="../channels/assets/do-not-localize/push.png"></a>
<div align="center"><a href="../push/create-push.md"><strong>푸시 알림</strong></a></div></td>
</tr></table>

## 컨텍스트 기반 데이터를 사용하여 콘텐츠 개인화 {#contextual}

메시지를 개인화하는 데 활용할 수 있는 API 페이로드에 추가 데이터를 전달할 수 있습니다.

고객이 암호를 재설정하고자 하고 서드파티 도구에서 생성된 암호 재설정 URL을 전송하고자 하는 이 예를 살펴보겠습니다. API 트리거된 캠페인을 사용하면 이렇게 생성된 URL을 API 페이로드에 전달하고 이를 캠페인에 활용하여 메시지에 추가할 수 있습니다.

이렇게 하려면 API 페이로드에 전달하고 개인화 편집기를 사용하여 메시지에 추가해야 합니다. `{{context.<contextualAttribute>}}` 구문을 사용하십시오. 여기서 `<contextualAttribute>`은(는) 전달할 데이터를 포함하는 API 페이로드의 변수 이름과 일치해야 합니다.

지금은 왼쪽 레일 메뉴에서 사용할 수 있는 컨텍스트 속성이 없습니다. [!DNL Journey Optimizer]에서 검사를 수행하지 않고 개인화 식에서 직접 특성을 입력해야 합니다.

![](assets/api-triggered-context.png)

**읽어야 함**

* 요청에 전달된 컨텍스트 속성은 200kb를 초과할 수 없으며 항상 유형 문자열로 간주됩니다.
* `context.system` 구문은 Adobe 내부 사용으로만 제한되며 컨텍스트 특성을 전달하는 데 사용해서는 안 됩니다.
* 프로필 활성화 이벤트와 달리 REST API에서 전달된 컨텍스트 데이터는 일회성 통신에 사용되며 프로필에 대해 저장되지 않습니다. 네임스페이스가 누락된 경우 최대 네임스페이스 세부 정보로 프로필이 만들어집니다.
* 콘텐츠에 수많은 상황별 데이터 또는 방대한 컨텍스트 데이터를 사용하면 성능에 영향을 줄 수 있습니다.

## 콘텐츠 테스트 및 확인

콘텐츠가 정의되면 **[!UICONTROL 콘텐츠 시뮬레이션]** 버튼을 사용하여 CSV/JSON 파일에서 업로드하거나 수동으로 추가한 테스트 프로필 또는 샘플 입력 데이터로 콘텐츠를 미리 보고 테스트합니다. [콘텐츠를 미리 보고 테스트하는 방법에 대해 알아보세요](../content-management/preview-test.md). 캠페인 생성 화면으로 돌아가려면 왼쪽 화살표를 클릭합니다.

![](assets/create-campaign-design.png)

## 다음 단계 {#next}

캠페인 구성 및 콘텐츠가 준비되면 캠페인 대상자를 정의할 수 있습니다. [자세히 알아보기](api-triggered-campaign-audience.md)
