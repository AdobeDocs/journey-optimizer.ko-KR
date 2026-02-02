---
title: 의사 결정 정책 시작
description: 의사 결정 정책으로 작업하여 오퍼를 제공하는 방법을 알아봅니다.
feature: Decisioning
topic: Integrations
role: User
level: Experienced
exl-id: 63aa1763-2220-4726-a45d-3a3a8b8a55ec
version: Journey Orchestration
source-git-commit: c2388c84346ed9a0409270fd96f3a1458bf8ad88
workflow-type: tm+mt
source-wordcount: '625'
ht-degree: 29%

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

>[!AVAILABILITY]
>
>현재 모든 고객은 코드 기반 경험 채널의 의사 결정 정책을 사용할 수 있습니다. 제한된 가용성으로 이메일 채널에 사용할 수 있습니다. 액세스 권한을 얻으려면 Adobe 담당자에게 문의하십시오.

## 주요 단계 {#key}

메시지에서 의사 결정 정책을 활용하는 주요 단계는 다음과 같습니다.

1. [의사 결정 정책 만들기](../experience-decisioning/create-decision-policy.md)

   반환할 항목 수를 선택하고, 선택 전략, 대체 옵션 및 평가 순서를 구성하여 메시지에 결정 정책을 설정합니다.

1. [콘텐츠의 의사 결정 정책 사용](../experience-decisioning/use-decision-policy.md)

   메시지에 표시할 결정 항목의 결정 정책 출력 및 속성으로 콘텐츠를 개인화합니다.

1. [보고 대시보드 만들기](cja-reporting.md)

   사용자 지정 Customer Journey Analytics 대시보드를 작성하여 성과를 측정하고 의사 결정 정책 및 오퍼가 전달되고 참여하는 방식에 대한 통찰력을 얻으십시오.

## 가드레일 및 제한 사항

* **전자 메일 미러 페이지** - 지금은 결정 항목이 전자 메일 미러 페이지에 렌더링되지 않습니다.
* **추적 및 링크 유형** - 의사 결정에 의해 생성된 링크를 추적하려면 스키마에서 &quot;Decisioning Assets&quot;로 정의하십시오. 속성 기반 링크는 추적할 수 없습니다.
* **전자 메일에 의사 결정 정책 중첩** - 이미 연결된 의사 결정 정책이 있는 상위 전자 메일 구성 요소에 여러 의사 결정 정책을 중첩할 수 없습니다.
* **의사 결정 기능이 있는 중복된 여정/캠페인** - 의사 결정 정책이 포함된 여정 또는 캠페인을 복제하는 경우 복제된 버전이 원본 전자 메일 또는 코드 기반 경험을 참조하므로 오류가 발생합니다. 항상 복제 후 결정 정책을 재구성합니다.
* **동의 정책** - 동의 정책 업데이트는 적용되는 데 최대 48시간이 걸립니다. 의사 결정 정책이 최근에 업데이트된 동의 정책에 연결된 속성을 참조하는 경우 변경 사항이 즉시 적용되지 않습니다.

  마찬가지로 동의 정책의 대상인 새 프로필 속성이 의사 결정 정책에 추가되면 사용할 수 있지만 지연이 경과할 때까지 연결된 동의 정책이 적용되지 않습니다.

  동의 정책은 Adobe Healthcare Shield 또는 Privacy and Security Shield 추가 기능이 있는 조직만 사용할 수 있습니다.

* **AI 등급** - 현재 AI 등급은 Decisioning이 있는 여정의 이메일 채널에 대해 지원되지 않습니다.

## 다음 단계 {#next-steps}

의사 결정 정책의 작동 방식과 맞춤형 오퍼를 제공하는 데 도움이 되는 방법을 이해했으므로 이제 첫 번째 의사 결정 정책을 만들 준비가 되었습니다.

➡️ [의사 결정 정책을 만드는 방법 알아보기](../experience-decisioning/create-decision-policy.md)

## 사용 방법 비디오 {#video}

Decisioning을 사용하여 대상자를 위한 이메일을 개인화하는 방법을 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/3479199?quality=12)
