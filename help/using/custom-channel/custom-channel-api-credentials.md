---
title: 사용자 지정 채널에 대한 API 자격 증명 관리
description: Adobe Journey Optimizer에서 사용자 지정 채널에 대한 API 자격 증명을 관리하는 방법을 알아봅니다.
feature: Channel Configuration
topic: Content Management
role: Admin
level: Experienced
badge: label="제한 공개" type="Informative"
source-git-commit: 9dfa2792db981f5f1a4e9fc3868ffd200c855a5b
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 3%

---


# API 자격 증명 관리 {#api-credentials}

>[!BEGINSHADEBOX]

**이 페이지에서:** 채널을 복제하지 않고 다양한 브랜드 또는 환경에서 엔드포인트에 대한 요청을 인증할 수 있도록 Adobe Journey Optimizer에서 사용자 지정 채널에 대한 API 자격 증명 세트를 보고, 관리하고, 만드는 방법을 알아봅니다.

>[!ENDSHADEBOX]

사용자 지정 채널이 **없음** 이외의 인증 유형으로 만들어진 경우 채널이 활성화될 때 초기 API 자격 증명 집합이 자동으로 생성됩니다.

**[!UICONTROL 관리]** > **[!UICONTROL 채널]** > **[!UICONTROL 채널 빌더]** > **[!UICONTROL API 자격 증명]**&#x200B;에서 자격 증명을 보고 관리하고 편집할 수 있습니다.

![API 자격 증명](assets/custom_channel_api_credentials.png){width="100%"}

동일한 채널에 대해 여러 자격 증명을 사용하면 채널 정의를 복제하지 않고도 다른 브랜드 또는 사용 사례와 같이 다른 채널 구성에 다른 인증 값을 첨부할 수 있습니다.

기존 자격 증명 집합을 편집하려면 인벤토리 목록에서 항목을 클릭합니다. 모든 필드를 편집할 수 있습니다.

동일한 채널에 대한 추가 자격 증명을 만들려면 아래 단계를 따르십시오.

1. **[!UICONTROL API 자격 증명]** 목록에서 **[!UICONTROL API 자격 증명 만들기]**&#x200B;를 클릭합니다.

1. 이름과 설명을 입력합니다.

   ![API 자격 증명 만들기](assets/custom_channel_create_api_credentials.png){width="100%"}

1. 자격 증명을 만들 **[!UICONTROL 채널]**&#x200B;을(를) 선택하십시오.

   >[!NOTE]
   >
   >인증 유형이 **없음**&#x200B;이 아닌 활성화된 사용자 지정 채널만 드롭다운 목록에 표시됩니다.

1. 목록에서 **[!UICONTROL 인증 유형]**&#x200B;을(를) 선택하십시오.
1. 인증별 필드를 채웁니다.
   * **[!UICONTROL API 키]** - 키 이름, 값 및 위치(쿼리 매개 변수 또는 헤더)를 제공합니다.
   * **[!UICONTROL 기본 인증]** - 사용자 이름과 암호를 제공하십시오.
   * **[!UICONTROL OAuth 2.0]** - OAuth 2.0 인증을 위해 페이로드를 구성합니다.
1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

## 다음 단계 {#next-steps}

* [하위 도메인 위임](custom-channel-subdomains.md)(선택 사항 - 링크 추적에 필요)
* [채널 구성 만들기](custom-channel-configuration.md)
