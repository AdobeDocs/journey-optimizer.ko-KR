---
title: Experience Decisioning 시작
description: Experience Decisioning에 대한 자세한 내용
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
badge: label="제한 공개"
exl-id: 4c57dbf9-b2a4-42da-8aa3-5a1b3a475a32
source-git-commit: 5ce388e5d86950e5cc6b173aab48225825f1c648
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 19%

---

# Experience Decisioning 시작 {#get-started-experience-decisioning}

>[!AVAILABILITY]
>
>SMS 채널은 현재 조직 집합(제한된 가용성)에만 사용할 수 있습니다. 자세한 내용은 Adobe 담당자에게 문의하십시오.
>
>현재 이 기능은 Adobe을 구입한 고객에게 제공되지 않습니다 **헬스케어 실드** 및 **개인 정보 보호 및 보안 보호** 추가 기능 제공.

## Experience Decisioning 소개 {#about}

Experience Decisioning은 &#39;의사 결정 항목&#39;으로 알려진 마케팅 의 중앙 집중식 카탈로그와 정교한 의사 결정 엔진을 제공하여 개인화를 간소화합니다. 이 엔진은 규칙과 순위 기준을 활용하여 각 개인에게 가장 관련성 높은 의사 결정 항목을 선택하고 제공합니다.

이러한 의사 결정 항목은 이제 Journey Optimizer 캠페인 내에서 액세스할 수 있는 새로운 코드 기반 경험 채널을 통해 광범위한 인바운드 표면에 원활하게 통합됩니다. Experience Decisioning 의사 결정 정책은 코드 기반 경험 캠페인에서만 사용할 수 있습니다.

## Experience Decisioning 주요 단계 {#steps}

Experience Decisioning을 사용하는 주요 단계는 다음과 같습니다.

1. **적절한 권한 할당**. Experience Decisioning은 Experience Decisioning 관련 기능에 대한 액세스 권한이 있는 사용자만 사용할 수 있습니다. **[!UICONTROL 역할]** 의사 결정 관리자 등. Experience Decisioning에 액세스할 수 없는 경우 권한을 확장해야 합니다.

   +++의사 결정 관리자 역할을 할당하는 방법 알아보기

   1. 에서 사용자에게 역할을 할당하려면 다음을 수행하십시오. [!DNL Permissions] product에서 **[!UICONTROL 역할]** 을 탭하고 [의사 결정 관리자]를 선택합니다.

      ![](assets/decision_permission_1.png)

   1. 다음에서 **[!UICONTROL 사용자]** 탭을 클릭하고 **[!UICONTROL 사용자 추가]**.

      ![](assets/decision_permission_2.png)

   1. 사용자 이름 또는 이메일 주소를 입력하거나 목록에서 사용자를 선택하고 **[!UICONTROL 저장]**.

      사용자가 이전에 만들어지지 않은 경우 [사용자 설명서 추가](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/ui/users).

      ![](assets/decision_permission_3.png)

   그러면 인스턴스로 리디렉션되는 이메일을 사용자가 받게 됩니다.

+++

1. **사용자 지정 속성 구성**: 사용자 지정 특성을 카탈로그의 스키마로 설정하여 항목 카탈로그를 특정 요구 사항에 맞게 맞춤화합니다.

1. **의사 결정 항목 만들기** 을 입력하여 타깃팅된 대상자에게 표시할 수 있습니다.

1. **컬렉션으로 구성**: 컬렉션을 사용하여 속성 기반 규칙에 따라 결정 항목을 분류합니다. 컬렉션을 선택 전략에 통합하여 고려해야 하는 결정 항목의 컬렉션을 결정합니다.

1. **의사 결정 규칙 만들기**: 의사 결정 규칙은 의사 결정 항목 및/또는 선택 전략에서 의사 결정 항목을 표시할 수 있는 대상을 결정하는 데 사용됩니다.

1. **등급 메서드 구현**: 등급 메서드를 만들고 의사 결정 전략 내에 적용하여 의사 결정 항목 선택의 우선 순위를 결정합니다.

1. **선택 전략 만들기**: 컬렉션, 의사 결정 규칙 및 등급 방법을 활용하여 프로필에 표시하는 데 적합한 의사 결정 항목을 식별하는 선택 전략을 수립합니다.

1. **코드 기반 캠페인에 의사 결정 정책 포함**: 의사 결정 정책은 여러 선택 전략을 결합하여 의도한 대상자에게 표시할 적합한 의사 결정 항목을 결정합니다.
