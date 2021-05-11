---
title: 기술 설정
description: 관리 및 설정 지침 학습
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 7%

---

# 기술 설정

![](assets/do-not-localize/badge.png)

## 브랜딩 매개 변수 설정{#cjm-branding}

모든 회사에는 브랜드 시각적 및 기술적 지침이 있습니다. 로고, 이메일 보낸 사람, 미러 페이지의 URL 도메인 또는 메시지 추적 설정 등 기술적 측면까지 고객에게 일관된 브랜드를 제공하기 위해 일련의 사양을 정의할 수 있습니다.
브랜드를 최종 사용자가 만들거나 수정할 수 없습니다.이 구성은 Adobe에 의해 관리됩니다.

[!DNL Journey Optimizer] 인스턴스에 대한 브랜딩 매개 변수를 설정하려면 Adobe에 문의하고 다음 세부 정보를 공유해야 합니다.

* 회사 이름

* 보낸 사람(보낸 사람) 이메일 주소

* 보낸 사람(보낸 사람) 이름

* 회신 주소

브랜딩 매개 변수가 구성되면 메시지를 만들 때 이를 선택할 수 있습니다.

브랜딩 매개 변수가 구성되면 **[!UICONTROL Presets]** 목록에서 메시지를 만들 때 해당 매개 변수를 선택할 수 있습니다. [콘텐츠 제작에 대한 자세한 내용을 살펴보십시오](create-message.md).

## 푸시 알림 채널 구성

이 [섹션](configure-push.md)에서 푸시 채널을 구성하는 방법을 알아봅니다.

## 하위 도메인 위임

[!DNL Journey Optimizer]에서 사용할 새 하위 도메인의 경우 첫 번째 단계는 이 하위 도메인을 위임하는 것입니다. Adobe 기술 담당자에게 연락해야 합니다.

솔루션을 구현할 때 외부에서 만나는 구성 요소에 대한 요구 사항이 있습니다.추적될 링크 및 웹 페이지 설정, 미러 페이지 표시 등이 포함됩니다.

이러한 요구 사항은 Adobe과 고객이 모두 호스팅하는 구성 요소를 통해 관리되지만, 해당 요구 사항에는 이메일 수신자가 볼 수 있는 URL이 포함됩니다.  기본 기술 솔루션 또는 호스팅 제공업체를 나타내는 URL이 없는 것을 방지하기 위해 하위 도메인을 설정하여 이메일 수신자에게 이 항목을 투명하게 만들 수 있습니다.

이러한 위임 후, Adobe에 의해 지정된 인프라에서는 위임 또는 CNAME 기반 전송 도메인에 대해 다음 서비스가 수행되도록 합니다.

* postmaster@ 및 inbox 남용@ 만들기

* 위임된 도메인에 대한 피드백 루프 설정

* 기본 DMARC 레코드 구성

Adobe에 의해 설정된 매개 변수는 위임을 완료하고 Adobe에 의해 확인되는 시점에서만 유효하며 기능성이 유지됩니다.

[도메인 위임에 대해 자세히 알아보십시오](https://helpx.adobe.com/kr/campaign/kb/domain-name-delegation.html).


## 데이터 소스, 이벤트 및 작업 만들기

**[!UICONTROL Admin]** 섹션을 사용하여 **[!UICONTROL Data Sources]**, **[!UICONTROL Events]** 및 **[!UICONTROL Actions]**&#x200B;을(를) 관리합니다.

![](assets/admin-menu.png)

### 데이터 소스

데이터 소스 구성을 사용하면 시스템에 대한 연결을 정의하여 여정에 사용할 추가 정보를 검색할 수 있습니다.

이 [섹션](../using/datasource/about-data-sources.md)에서 데이터 소스에 대해 자세히 알아보십시오.

### 이벤트

이벤트를 사용하면 여정에 유입되는 개별 사용자에게 실시간으로 메시지를 보낼 수 없도록 여정을 트리거할 수 있습니다.

이벤트 구성에서는 여정에 필요한 이벤트를 구성합니다. 들어오는 이벤트의 데이터는 XDM(Adobe Experience Data Model)에 따라 표준화됩니다. 이벤트는 인증된 이벤트와 인증되지 않은 이벤트(예: Adobe Mobile SDK 이벤트)를 위한 수집 API 스트리밍에서 옵니다.

이 [섹션](../using/event/about-events.md)의 이벤트에 대한 자세한 내용

### 작업

[!DNL Journey Optimizer] 메시지 기능 내장:콘텐츠를 디자인하고 메시지를 게시하기만 하면 됩니다. 제3자 시스템을 사용하여 메시지를 전송하는 경우 사용자 지정 작업을 만들 수 있습니다.

이 [섹션](../using/action/action.md)의 작업에 대해 자세히 알아보기
