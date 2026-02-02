---
title: 메시지에 결정 정책 사용
description: 메시지에서 의사 결정 정책을 사용하는 방법을 알아봅니다.
feature: Decisioning
topic: Integrations
role: User
level: Experienced
mini-toc-levels: 1
version: Journey Orchestration
source-git-commit: 083545ff7b2dc5ce45ef3766321fdf12e1b96c5c
workflow-type: tm+mt
source-wordcount: '694'
ht-degree: 3%

---

# 메시지에 결정 정책 사용 {#create-decision}

콘텐츠에 의사 결정 정책을 추가한 후에는 개인화를 위해 반환된 의사 결정 항목의 속성을 사용할 수 있습니다. 이렇게 하려면 먼저 의사 결정 정책 코드를 콘텐츠에 삽입합니다.

>[!CAUTION]
>
>결정 정책은 **코드 기반 경험** 및 **푸시 알림** 채널에 대해 모든 고객이 사용할 수 있습니다.
>
>이메일 채널에 대한 의사 결정은 제한된 가용성으로 사용할 수 있습니다. 액세스 권한을 요청하려면 Adobe 담당자에게 문의하십시오. [가용성 레이블](../rn/releases.md#availability-labels)에 대해 자세히 알아보세요.

## 의사 결정 정책 코드 삽입 {#insert}

>[!BEGINTABS]

>[!TAB 코드 기반 경험]

1. 코드 기반 환경을 편집하고 **[!UICONTROL 결정 정책]**(으)로 이동합니다.

2. 결정 정책 코드를 추가하려면 **[!UICONTROL 정책 삽입]**&#x200B;을 선택하십시오.

   ![](assets/decision-code-based-add-decision.png)

>[!NOTE]
>
>코드 기반 경험의 경우 의사 결정 정책에 조각이 포함된 의사 결정 항목이 포함되어 있으면 의사 결정 정책 코드에서 이러한 조각을 활용할 수 있습니다. [조각을 활용하는 방법 알아보기](../experience-decisioning/fragments-decision-policies.md)

>[!TAB 이메일]

1. **Personalization 편집기**&#x200B;를 열고 **[!UICONTROL 의사 결정 정책]**(으)로 이동합니다.

2. **[!UICONTROL 구문 삽입]**&#x200B;을 선택하여 의사 결정 정책에 대한 코드를 추가합니다.

   ![](assets/decision-policy-add.png)

   >[!NOTE]
   >
   >삽입 옵션이 나타나지 않으면 상위 구성 요소에 대해 의사 결정 정책이 이미 구성되어 있을 수 있습니다.

3. 아직 구성 요소에 할당된 배치가 없으면 목록에서 배치를 선택하고 **[!UICONTROL 할당]**&#x200B;을 클릭합니다.

   ![](assets/decision-policy-placement.png)

>[!TAB 푸시]

1. **Personalization 편집기**&#x200B;를 열고 **[!UICONTROL 의사 결정 정책]**(으)로 이동합니다.

2. **[!UICONTROL 구문 삽입]**&#x200B;을 선택하여 의사 결정 정책에 대한 코드를 추가합니다.

   ![](assets/decision-policy-add-push-insert-syntax.png)

>[!IMPORTANT]
>
>푸시 알림을 사용하는 Experience Decisioning에는 모바일 SDK의 특정 버전이 필요합니다. 이 기능을 구현하기 전에 [릴리스 정보](https://developer.adobe.com/client-sdks/home/release-notes/){target="_blank"}를 확인하여 필요한 버전을 식별하고 그에 따라 업그레이드했는지 확인하십시오. [이 섹션](https://developer.adobe.com/client-sdks/home/current-sdk-versions/){target="_blank"}에서 사용 가능한 플랫폼에 대한 모든 SDK 버전을 볼 수도 있습니다.

>[!ENDTABS]

결정 정책 코드가 추가됩니다. 이제 반환된 의사 결정 항목의 속성을 사용하여 콘텐츠를 개인화할 수 있습니다.

>[!NOTE]
>
>코드 기반 경험 및 이메일 채널의 경우 반환할 의사 결정 항목마다 이 시퀀스를 한 번씩 반복합니다. 예를 들어 [결정을 만들 때](create-decision-policy.md) 2개 항목을 반환하도록 선택한 경우 시퀀스를 두 번 반복합니다. 푸시 채널의 경우 하나의 결정 항목만 반환할 수 있습니다.

## 의사 결정 항목 속성을 사용하여 개인화 {#attributes}

콘텐츠에 의사 결정 정책에 대한 코드를 추가하면 반환된 의사 결정 항목의 모든 속성을 개인화할 수 있습니다. [개인 맞춤화를 사용하여 작업하는 방법을 알아보세요](../personalization/personalize.md).

특성은 &quot;오퍼&quot; [카탈로그 스키마](catalogs.md)에 저장됩니다. 개인화 편집기에서 다음 폴더에 표시됩니다.
* **사용자 지정 특성**: `_\<imsOrg\>` 폴더
* **표준 특성**: `_experience` 폴더

[!DNL Journey Optimizer] 조각에서는 기본적으로 의사 결정 항목 특성 및 컨텍스트 특성이 지원되지 않습니다. 그러나 아래 설명된 것처럼 전역 변수를 대신 사용할 수 있습니다.

![](assets/decision-code-based-decision-attributes.png)

특성을 추가하려면 특성 옆에 있는 **`+`** 아이콘을 클릭합니다. 필요한 만큼 속성을 추가할 수 있습니다. 프로필 데이터와 같은 다른 개인화 속성도 포함할 수 있습니다.

* **Email** 및 **코드 기반** 채널의 경우 `#each` 루프 내에서 대괄호 `[ ]`을(를) 사용하여 특성을 래핑한 다음 닫는 `/each` 태그 앞에 쉼표를 추가하십시오.

  +++예제 참조

  ![](assets/decision-code-based-wrap-code.png)

  +++

* **Push** 채널의 경우, 결정 정책의 구문 코드 뒤에 특성을 삽입해야 합니다. 이 구문은 항상 1행을 유지해야 합니다.

  >[!NOTE]
  >이미지 자산 속성을 푸시 콘텐츠(예: 제목 또는 본문)에 삽입하면 속성 값이 URL로 표시됩니다. 이미지 자체는 해당 필드에서 렌더링되지 않습니다.

* 결정 항목 추적을 사용하려면 `trackingToken` 특성을 추가하십시오. `trackingToken: {{item._experience.decisioning.decisionitem.trackingToken}}`

## 콘텐츠 미리 보기 및 테스트

콘텐츠를 빌드한 후 여정 또는 캠페인을 활성화하기 전에 미리보기 및 테스트하십시오. 시뮬레이션 인터페이스에서 선택한 프로필을 기반으로 의사 결정 항목을 렌더링합니다. [콘텐츠를 미리 보고 테스트하는 방법에 대해 알아보세요](../content-management/preview-test.md).

## 다음 단계 {#final-steps}

콘텐츠가 준비되면 캠페인 또는 여정을 검토하고 게시합니다.

* [여정 게시](../building-journeys/publish-journey.md)
* [캠페인 검토 및 활성화](../campaigns/review-activate-campaign.md)

코드 기반 경험의 경우 개발자가 채널 구성에 정의된 표면에 대한 콘텐츠를 가져오기 위해 API 또는 SDK 호출을 수행하면 바로 웹 페이지 또는 앱에 변경 사항이 적용됩니다.

>[!NOTE]
>
>현재 [코드 기반 경험](../code-based/create-code-based.md) 캠페인 또는 여정에 대한 의사 결정 기반 콘텐츠를 시뮬레이션할 수 없습니다. 해결 방법은 [여기](../code-based/code-based-decisioning-implementations.md)에서 확인할 수 있습니다.

## 보고 대시보드 사용

의사 결정의 성과를 파악하기 위해 캠페인 또는 여정 보고서에서 즉시 사용 가능한 의사 결정 지표를 보거나, 사용자 지정 Customer Journey Analytics 대시보드를 작성하여 성과를 측정하고 의사 결정 정책 및 오퍼가 전달되고 참여하는 방식에 대한 통찰력을 얻을 수 있습니다. [의사 결정 보고에 대해 자세히 알아보세요](cja-reporting.md).

![](../reports/assets/cja-decisioning-item-performance.png)
