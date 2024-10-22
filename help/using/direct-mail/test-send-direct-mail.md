---
title: DM 메시지 확인 및 보내기
description: Journey Optimizer에서 DM 메시지를 확인하고 보내는 방법 알아보기
feature: Direct Mail, Test Profiles, Preview
topic: Content Management
role: User
level: Beginner
keyword: direct, mail, configuration, direct-mail, provider
exl-id: 69a19190-d2e2-4858-a1df-ffd008226e2b
source-git-commit: 8fecd0d4812ba875dba1d47bc32ab08178a13f2c
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 3%

---

# DM 메시지 확인 및 보내기 {#direct-mail-test-send}

## 추출 파일 미리 보기 {#preview-dm}

추출 파일의 콘텐츠가 정의되면 테스트 프로필을 사용하여 미리 볼 수 있습니다. 개인화된 콘텐츠를 삽입한 경우 테스트 프로필 데이터를 활용하여 이 콘텐츠가 메시지에 어떻게 표시되는지 확인할 수 있습니다.

이렇게 하려면 **[!UICONTROL 콘텐츠 시뮬레이션]**&#x200B;을 클릭한 다음 테스트 프로필을 추가하여 테스트 프로필 데이터를 사용하여 추출 파일 렌더링 방법을 확인하십시오.

![](assets/direct-mail-simulate.png){width="800" align="center"}

테스트 프로필을 선택하고 콘텐츠를 미리 보는 방법에 대한 자세한 내용은 [콘텐츠 관리](../content-management/preview-test.md) 섹션에서 확인할 수 있습니다.

파일 콘텐츠를 전송할 준비가 되면 시뮬레이트 화면을 닫은 다음 **[!UICONTROL 활성화하려면 검토]** 단추를 클릭하십시오.

## DM 캠페인 유효성 검사 및 활성화 {#dm-validate}

>[!IMPORTANT]
>
> 캠페인이 승인 정책의 적용을 받는 경우 DM 캠페인을 보내려면 승인을 요청해야 합니다. [자세히 알아보기](../test-approve/gs-approval.md)

DM 캠페인을 활성화하기 전에 캠페인과 추출 파일이 제대로 구성되어 있는지 확인하십시오. 이렇게 하려면 편집기의 위쪽 섹션에서 경고를 확인하십시오. 일부는 간단한 경고이지만 일부는 메시지를 보내지 못하게 할 수 있습니다. 경고와 오류의 두 가지 경고 유형이 발생할 수 있습니다.

* **경고**&#x200B;는 권장 사항과 모범 사례를 참조합니다. 예를 들어 SMS 메시지가 비어 있는 경우 경고 메시지가 표시됩니다.

* **오류**&#x200B;로 인해 캠페인이 해결되지 않으면 게시할 수 없습니다. 예를 들어 제목 줄이 누락된 경우 경고 메시지가 표시됩니다.

![](assets/direct-mail-review.png){width="800" align="center"}

DM 캠페인이 준비되면 **[!UICONTROL 활성화]** 단추를 클릭하세요. 캠페인이 시작되면 추출 파일이 자동으로 생성되고 [파일 라우팅 구성](../direct-mail/direct-mail-configuration.md)에 지정된 서버로 내보내집니다.

DM을 전송하면 캠페인 보고서 내에서 DM 캠페인의 영향을 측정할 수 있습니다. 보고에 대한 자세한 정보는 이 섹션 을 참조하십시오.

## DM에 대한 동의 관리 {#dm-consent-management}

[!DNL Journey Optimizer]에서 동의는 Experience Platform [동의 스키마](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html?lang=ko){target="_blank"}가 처리합니다. 기본적으로 동의 필드의 값은 비어 있으며 커뮤니케이션을 수신하기 위한 동의로 처리됩니다.

프로필이 DM 수신을 옵트아웃한 경우 해당 Experience Platform 프로필 특성에서 `consents.marketing.postalMail.val`의 값은 `n`이(가) 되며 해당 프로필은 후속 게재에서 제외됩니다.

다시 활성화하려면 프로필 특성을 `consents.marketing.postalMail.val`: `y`(으)로 다시 변경해야 합니다.

프로필의 속성을 관리하려면 Experience Platform 로 이동하여 ID 네임스페이스 및 해당 ID 값을 선택하여 프로필에 액세스합니다. 자세한 내용은 [Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=ko#getting-started){target="_blank"}를 참조하세요.

[이 섹션](../privacy/opt-out.md)에서 Journey Optimizer의 옵트아웃 관리에 대해 자세히 알아보세요.
