---
title: 의사 결정 정책 시작
description: 의사 결정 정책으로 작업하여 오퍼를 제공하는 방법을 알아봅니다.
feature: Decisioning
topic: Integrations
role: User
level: Experienced
exl-id: 63aa1763-2220-4726-a45d-3a3a8b8a55ec
version: Journey Orchestration
source-git-commit: fb35bc5a51421818297586b5e386aa75deb1c669
workflow-type: tm+mt
source-wordcount: '674'
ht-degree: 26%

---

# 결정 정책 시작 {#create-decision}

>[!CONTEXTUALHELP]
>id="ajo_code_based_decision"
>title="의사 결정은 무엇입니까?"
>abstract="결정 정책에는 결정 엔진이 최상의 콘텐츠를 선택하기 위한 모든 선택 논리가 포함되어 있습니다. 결정 정책은 캠페인별로 다릅니다. 목표는 각 프로필에 가장 적합한 제안을 선택하는 것이며, 캠페인 작성을 통해서는 메시지에 포함될 항목 속성을 포함하여 선택한 결정 항목이 표시될 방법을 지정할 수 있습니다."
>additional-url="https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="결정 정보"

>[!CONTEXTUALHELP]
>id="ajo_journey_decision_policy"
>title="결정 정책 정의"
>abstract="결정 정책을 사용하면 결정 엔진에서 최상의 항목을 선택하여 올바른 대상자에게 전달할 수 있습니다."
>additional-url="https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="결정 정보"

>[!CONTEXTUALHELP]
>id="ajo_exd_decision_policy"
>title="결정 정책"
>abstract="결정 정책을 사용하면 결정 엔진에서 최상의 항목을 선택하여 각 대상자에게 전달할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_exd_placements"
>title="배치"
>abstract="배치는 결정 엔진에서 반환된 항목이 메시지에 나타나는 위치를 결정합니다. 보고에서 다양한 배치에 대한 성과를 추적할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_exd_decision_attribute"
>title="카탈로그에서 결정 속성 선택"
>abstract="결정 속성은 카탈로그의 스키마에 저장됩니다. 선택한 카탈로그에서 여기에서 사용할 속성을 선택합니다."

의사 결정 정책은 의사 결정 엔진을 활용하여 각 대상 구성원에 대해 제공할 최상의 콘텐츠를 동적으로 반환하는 오퍼에 대한 컨테이너입니다. 이 프로필의 목표는 각 프로필에 가장 적합한 오퍼를 선택하는 것이며, 캠페인/여정 작성에서는 메시지에 포함할 항목 속성을 포함하여 선택한 결정 항목을 표시하는 방법을 나타낼 수 있습니다.

➡️ [비디오에서 이 기능 살펴보기](#video)

## 가드레일 및 제한 사항

* **지원되는 채널** - 의사 결정 정책은 코드 기반 경험, 이메일, SMS 및 푸시 알림과 같은 채널에 사용할 수 있습니다.
* **푸시 알림 SDK 요구 사항** - 푸시 알림을 사용하는 Experience Decisioning에는 Mobile SDK의 특정 버전이 필요합니다. 이 기능을 구현하기 전에 [릴리스 정보](https://developer.adobe.com/client-sdks/home/release-notes/){target="_blank"}를 확인하여 필요한 버전을 식별하고 그에 따라 업그레이드했는지 확인하십시오. [이 섹션](https://developer.adobe.com/client-sdks/home/current-sdk-versions/){target="_blank"}에서 사용 가능한 플랫폼에 대한 모든 SDK 버전을 볼 수도 있습니다.
* **전자 메일 미러 페이지** - 지금은 결정 항목이 전자 메일 미러 페이지에 렌더링되지 않습니다.
* **추적 및 링크 유형** - 의사 결정에 의해 생성된 링크를 추적하려면 스키마에서 &quot;Decisioning Assets&quot;로 정의하십시오. 속성 기반 링크는 추적할 수 없습니다.
* **전자 메일에 의사 결정 정책 중첩** - 이미 연결된 의사 결정 정책이 있는 상위 전자 메일 구성 요소에 여러 의사 결정 정책을 중첩할 수 없습니다.
* **의사 결정 기능이 있는 중복된 여정/캠페인** - 의사 결정 정책이 포함된 여정 또는 캠페인을 복제하는 경우 복제된 버전이 원본 전자 메일 또는 코드 기반 경험을 참조하므로 오류가 발생합니다. 항상 복제 후 결정 정책을 재구성합니다.
* **동의 정책** - 동의 정책 업데이트는 적용되는 데 최대 48시간이 걸립니다. 의사 결정 정책이 최근에 업데이트된 동의 정책에 연결된 속성을 참조하는 경우 변경 사항이 즉시 적용되지 않습니다.

  마찬가지로 동의 정책의 대상인 새 프로필 속성이 의사 결정 정책에 추가되면 사용할 수 있지만 지연이 경과할 때까지 연결된 동의 정책이 적용되지 않습니다.

  동의 정책은 Adobe Healthcare Shield 또는 Privacy and Security Shield 추가 기능이 있는 조직만 사용할 수 있습니다.

* **AI 등급** - 현재 AI 등급은 Decisioning이 있는 여정의 이메일 채널에 대해 지원되지 않습니다.

* **콘텐츠 템플릿** - 콘텐츠 내에 구성된 결정 정책은 템플릿에 저장되지 않습니다. 템플릿을 다른 작업에 적용하는 경우 정책을 다시 구성해야 합니다.

## 주요 단계 {#key}

메시지에서 의사 결정 정책을 활용하는 주요 단계는 다음과 같습니다.

1. **의사 결정 정책 만들기**

   메시지에 결정 정책을 추가하고 반환할 항목 수, 선택 전략 및 대체 옵션을 구성합니다.

   ➡️ [의사 결정 정책을 만드는 방법 알아보기](../experience-decisioning/create-decision-policy.md)

1. **콘텐츠의 결정 정책 사용**

   메시지에 표시할 결정 항목의 속성을 삽입하여 결정 정책 출력으로 콘텐츠를 개인화합니다

   ➡️ [메시지에서 의사 결정 정책을 사용하는 방법 알아보기](../experience-decisioning/create-decision-policy.md)

## 방법 비디오 {#video}

Decisioning을 사용하여 대상자를 위한 이메일을 개인화하는 방법을 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/3476171?captions=kor&quality=12)

Decisioning을 사용하여 대상을 위한 푸시 알림을 개인화하는 방법을 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/3479217?captions=kor&quality=12)

Decisioning을 사용하여 대상자를 위한 SMS 메시지를 개인화하는 방법을 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/3479536?captions=kor&quality=12)
