---
title: DM에서의 일괄 의사 결정
description: Experience Decisioning을 사용하여 DM 추출 파일을 개인화하거나 다운스트림 시스템에서 사용할 의사 결정 데이터를 내보냅니다
feature: Decisioning, Direct Mail
topic: Integrations
role: User
level: Intermediate
keywords: 일괄 의사 결정, dm, 의사 결정
source-git-commit: 1b4e12b9433a819a3be34c4f01c489af1d6091ed
workflow-type: tm+mt
source-wordcount: '853'
ht-degree: 0%

---


# DM에서의 일괄 의사 결정 {#batch-decisioning-direct-mail}

일괄 처리 의사 결정을 통해 Decisioning은 각 프로필에 가장 적합한 의사 결정 항목을 선택하고 DM 추출 파일에 해당 결과를 포함합니다. 결정 정책을 구성할 때 **[!UICONTROL 항목 수]**&#x200B;를 설정하여 프로필당 여러 항목을 반환할 수 있습니다. 내보낸 파일은 DM 개인화에 사용하거나 프로필 및 의사 결정 속성을 다른 시스템으로 내보내는 배치 사용 사례에 사용할 수 있습니다.

DM에서의 일괄 의사 결정은 두 가지 주요 사용 사례를 지원합니다.

* **의사 결정 포함 DM** - 받는 사람별로 실제 메일을 개인화합니다. 예를 들어 자격 규칙 및 순위(우선 순위 또는 수식)를 사용하여 각 프로필에 가장 적합한 이미지나 오퍼를 선택합니다. 추출 파일에는 프로필 데이터와 DM 공급자에 대해 선택한 결정 항목의 속성(예: 오퍼 이미지 URL)이 포함되어 있습니다.
* **다운스트림 시스템에 대한 일괄 내보내기** - 다른 시스템에서 사용할 프로필 및 의사 결정 결과(예: 오퍼 ID, 특성)를 내보냅니다. 일괄 의사 결정을 실행하고 파일을 서버로 내보냅니다. 다운스트림 도구(예: 서드파티 이메일 서비스 공급자)는 자체 캠페인 또는 프로세스에 해당 데이터를 사용합니다.

>[!NOTE]
>
>이 페이지에서는 DM을 통한 일괄 의사 결정 사용의 의사 결정 관련 측면에 중점을 둡니다. 파일 라우팅, 채널 구성 및 추출 파일 설정을 포함하여 DM 채널 설정 및 사용에 대한 자세한 내용은 [DM 시작](../direct-mail/get-started-direct-mail.md) 및 [DM 메시지 만들기](../direct-mail/create-direct-mail.md)를 참조하세요.

## 워크플로우 개요 {#workflow}

1. **DM 캠페인 또는 여정 만들기**: 여정 또는 캠페인을 만들고, **[!UICONTROL DM]** 작업을 선택하고, DM 구성을 선택하고, 대상을 정의합니다.

   ➡️ [DM 메시지를 만드는 방법 알아보기](../direct-mail/create-direct-mail.md)

1. **결정 정책 추가**:

   1. 추출 파일을 구성하려면 **[!UICONTROL 콘텐츠 편집]**&#x200B;을 클릭하십시오.
   1. 추출 파일에 열을 추가하고 ![](assets/do-no-localize/editor-icon.svg) 아이콘을 사용하여 개인화 편집기를 엽니다.

      ![](assets/decision-policy-dm-add.png)

   1. 결정 정책을 만들려면 **[!UICONTROL Decisioning]** 메뉴로 이동합니다. 프로필당 결정 항목이 두 개 이상 필요한 경우 정책 구성에서 **[!UICONTROL 항목 수]**&#x200B;를 설정한 다음 선택 전략과 선택적 대체를 구성합니다.

      ![](assets/decision-policy-dm-create.png)

   ➡️ [DM에서 의사 결정 정책을 추가하고 구성하는 방법에 대해 알아보세요](create-decision-policy.md#add)

1. **의사 결정 특성을 사용하여 DM 파일 개인화**: 의사 결정 결과를 포함해야 하는 열의 경우 Personalization 편집기를 열고 **[!UICONTROL 의사 결정 정책]**(으)로 이동한 다음 **[!UICONTROL 정책 삽입]**&#x200B;을 선택하여 의사 결정 정책에 대한 코드를 추가하십시오.

   선택한 오퍼 정보가 각 프로필의 추출 파일에 포함되도록 반환된 의사 결정 항목 속성을 사용합니다. 여러 항목이 반환되면 정책 `#each` 루프를 사용하여 열에 있는 각 항목의 특성을 매핑합니다.

   ➡️ [메시지에서 의사 결정 정책을 사용하는 방법 알아보기 - 다이렉트 메일 탭](use-decision-policy.md)

1. 테스트 프로필로 **[!UICONTROL 콘텐츠 시뮬레이션]**&#x200B;을(를) 사용하여 내보낸 행(결정 값 포함)을 미리 봅니다.

   ![](assets/batch-decisioning-simulate.png)

   ➡️ [콘텐츠를 미리 보고 테스트하는 방법에 대해 알아보세요](../content-management/preview-test.md)

1. 캠페인을 활성화하거나 여정을 게시하여 파일을 생성하고(CSV 또는 텍스트로 구분) 구성된 서버에 내보냅니다.

   ➡️ [캠페인을 검토하고 활성화하는 방법을 알아보세요](../campaigns/review-activate-campaign.md) | [여정 게시 방법 알아보기](../building-journeys/publish-journey.md)

## DM + 의사 결정 예 {#example-direct-mail}

예: 피트니스 retailer은 10개의 가능한 이미지 중 하나를 사용하여 각 고객에게 개인화된 엽서를 보냅니다. Decisioning을 사용하여 프로필별로 최상의 이미지를 선택합니다.

1. 자격 규칙(예: 연령, 성별)이 있는 10개의 결정 항목(이미지당 한 개)을 만듭니다.
2. 컬렉션에 추가하고 등급 방법(예: 수동 우선 순위 또는 공식)으로 선택 전략을 만듭니다.
3. DM 캠페인 또는 여정에서 의사 결정을 활성화하고 이 선택 전략을 사용하는 의사 결정 정책을 추가합니다.
4. 추출 파일에서, 데이터가 선택한 이미지(예: 오퍼 이미지 URL)를 포함하는 의사 결정 항목 속성인 열을 추가합니다. 다른 열에는 전체 이름, 주소, 상태, zip 등이 있을 수 있습니다.
5. 캠페인이 실행되면 각 프로필은 내보내기에서 해당 프로필에 대해 선택한 이미지와 함께 하나의 행을 가져옵니다. DM 공급자는 이 파일을 사용하여 실제 메일을 생성합니다.

테스트 프로필과 함께 **[!UICONTROL 콘텐츠 시뮬레이션]**&#x200B;을 사용하여 해당 프로필에 대해 내보낼 의사 결정 결과(예: 이미지)를 볼 수 있습니다.

## 일괄 내보내기(미들웨어) 사용 사례 {#example-batch-export}

일부 고객은 일괄 의사 결정을 사용하여 프로필과 다른 시스템(예: CRM 또는 이메일 서비스 공급자)에서 사용할 의사 결정 결과를 내보냅니다. 흐름은 다음과 같습니다.

1. 위와 같이 DM(파일 라우팅 + 채널 구성)을 구성합니다.
2. DM 캠페인 또는 여정을 만들고 결정 정책을 추가합니다.
3. 내보내기에 필요한 프로필 필드 및 결정 항목 속성에 대해 열을 추가합니다.
4. 캠페인을 활성화합니다. 파일을 서버(예: Amazon S3 또는 SFTP)로 내보냅니다.
5. 다운스트림 시스템은 파일을 검색하고 자체 캠페인 또는 프로세스에 프로필 및 의사 결정 데이터를 사용합니다.

Experience Decisioning이 포함된 DM 채널을 통해 일괄 의사 결정 사용 사례를 지원합니다.

## 관련 설명서 {#related}

* [DM 메시지 만들기](../direct-mail/create-direct-mail.md) - 추출 파일을 구성하고 의사 결정 사용
* [결정 정책 만들기](create-decision-policy.md#add) - DM 탭에서 결정 정책을 추가합니다.
* [DM 구성](../direct-mail/direct-mail-configuration.md) - 파일 라우팅 및 채널 구성
* [의사 결정 시작](gs-experience-decisioning.md) - 개념 및 보호
