---
solution: Journey Optimizer
product: journey optimizer
title: 컨텐츠 및 여정 마이그레이션
description: 이메일 콘텐츠 템플릿을 마이그레이션하고 외부 플랫폼에서 여정을 가져오는 방법을 알아봅니다.
feature: Get Started
topic: Content Management
role: User
level: Intermediate
hide: true
source-git-commit: 8731e10c9a6278c34cd0db8ccdec112f2d5c90d8
workflow-type: tm+mt
source-wordcount: '1298'
ht-degree: 10%

---

# 컨텐츠 및 여정 마이그레이션 {#migrate-content-and-journeys}

다른 마케팅 플랫폼에서 [!DNL Journey Optimizer]&#x200B;(으)로 이동하는 경우 빈 슬레이트에서 시작할 필요가 없습니다. Journey Optimizer에는 기존 이메일 콘텐츠와 여정을 가져오는 전용 작업 영역이 포함되어 있습니다. [!DNL Journey Optimizer]개의 콘텐츠 템플릿 및 여정으로 변환되므로 처음부터 모든 것을 다시 빌드하지 않고 중단한 위치를 선택할 수 있습니다.

콘텐츠와 여정을 Journey Optimizer으로 마이그레이션하려면 캠페인 관리, 여정 관리, 메시지 관리, 세그먼트 관리, 라이브러리 항목 관리, 샌드박스 보기 및 관리, AJO 통합 구성 관리 권한이 필요합니다. [역할 및 권한에 대해 자세히 알아보기](../administration/permissions.md)

[!DNL Journey Optimizer] 홈 페이지에서 바로 이 작업 영역에 액세스할 수 있습니다.

![마이그레이션 작업 영역에 액세스](assets/onboarding-hub-15.png)

## 연결 설정 {#set-up-a-connection}

>[!CONTEXTUALHELP]
>id="ajo_migration_connection_name"
>title="연결 이름"
>abstract="소스 시스템을 식별하는 설명적인 이름(예: &#39;Marketing-Automation-Prod&#39;). 문자로 시작해야 하며 영숫자, 밑줄 또는 하이픈만 포함할 수 있습니다(4~50자)."


>[!CONTEXTUALHELP]
>id="ajo_migration_base_api_url"
>title="기본 API URL"
>abstract="리소스 경로나 쿼리 문자열 없는 API의 루트 URL입니다(예: https://api.example.com)."

>[!CONTEXTUALHELP]
>id="ajo_migration_authentication_method"
>title="인증 방법 선택"
>abstract="API 키는 각 요청에 대해 단일 자격 증명을 보내는 반면, OAuth 2.0은 엔터프라이즈 및 타사 API에 더 적합한 토큰 기반 프로토콜을 사용합니다."

>[!CONTEXTUALHELP]
>id="ajo_migration_client_id"
>title="클라이언트 ID"
>abstract="인증 서버에 등록할 때 발급되는 애플리케이션의 공개 식별자입니다."

>[!CONTEXTUALHELP]
>id="ajo_migration_client_secret"
>title="클라이언트 암호"
>abstract="앱과 인증 서버에만 알려진 비밀 자격 증명입니다. 클라이언트측 코드에서는 절대 노출하지 마십시오."


>[!CONTEXTUALHELP]
>id="ajo_migration_token_url"
>title="토큰 URL"
>abstract="클라이언트 자격 증명 흐름에 대한 액세스 토큰을 발급하는 인증 서버 엔드포인트로, 일반적으로 /oauth/token 또는 /token으로 끝납니다."


>[!NOTE]
>
>API를 통해 가져오는 대신 HTML 파일 또는 스크린샷을 업로드하는 경우에는 연결이 필요하지 않습니다.

API를 통해 콘텐츠 또는 여정을 가져오려면 먼저 [!DNL Journey Optimizer]을(를) 원본 플랫폼에 연결합니다.

1. 작업 영역에서 **[!UICONTROL 연결 관리]**&#x200B;를 선택합니다.

   ![연결 관리 단추](assets/onboarding-hub-14.png)

1. **[!UICONTROL 새 연결]**&#x200B;을 클릭합니다.

   ![새 연결 단추가 강조 표시된 연결 관리 창](assets/onboarding-hub-1.png)

1. 아래에 세부 정보를 입력하십시오.

   * **[!UICONTROL 연결 이름]**: `Marketing-Automation-Prod`과(와) 같이 소스 시스템을 식별하는 이름입니다. 이름은 문자로 시작해야 하며 4자에서 50자 사이의 문자, 숫자, 밑줄 또는 하이픈만 포함할 수 있습니다.
   * **[!UICONTROL 기본 API URL]**: `https://api.example.com`과(와) 같은 리소스 경로나 쿼리 문자열이 없는 소스 시스템 API의 루트 URL입니다.
   * **[!UICONTROL 설명]**: 사용자 및 다른 사용자가 이 연결의 목적을 식별하는 데 도움이 되는 선택적 컨텍스트입니다.
   * **[!UICONTROL 인증 방법]**: [!DNL Journey Optimizer]이(가) 원본 시스템에 대해 인증하는 방법입니다. 각 요청과 함께 하나의 자격 증명을 보내려면 **API 키**&#x200B;를 선택하세요. 엔터프라이즈 및 타사 API에 더 적합한 토큰 기반 프로토콜을 사용하려면 **OAuth 2.0**&#x200B;을(를) 선택하십시오.
   * **[!UICONTROL 클라이언트 ID]**: 인증 서버에 응용 프로그램을 등록할 때 응용 프로그램에 할당된 공용 식별자입니다. OAuth 2.0 연결에 필요합니다.
   * **[!UICONTROL 클라이언트 암호]**: 클라이언트 ID와 연결된 기밀 자격 증명입니다. 애플리케이션과 인증 서버에만 알려져 있으므로 비공개로 유지합니다. OAuth 2.0 연결에 필요합니다.
   * **[!UICONTROL 토큰 URL]**: 클라이언트 자격 증명 흐름에 대한 액세스 토큰을 발급하는 인증 서버 끝점으로, 일반적으로 `/oauth/token` 또는 `/token`에서 끝납니다. OAuth 2.0 연결에 필요합니다.

     ![연결 이름, 기본 API URL 및 인증 세부 정보에 대한 필드가 있는 새 연결 양식](assets/onboarding-hub-2.png)

1. Select **[!UICONTROL Create]**.

1. 연결이 설정되면 고급 메뉴를 사용하여 연결을 삭제하거나, 다음에 콘텐츠나 여정을 가져올 때 미리 선택되도록 기본값으로 표시합니다.

   ![연결을 삭제하거나 기본값으로 표시하는 옵션이 있는 고급 메뉴](assets/onboarding-hub-3.png)

## 이메일 콘텐츠 가져오기 {#import-email-content}

HTML 파일 또는 소스 플랫폼에 대한 연결인 콘텐츠에 대한 소스가 있으면 작업 영역으로 가져와 [!DNL Journey Optimizer] 콘텐츠 템플릿으로 변환합니다.

1. **[!UICONTROL 전자 메일 콘텐츠]** 탭에서 전자 메일 콘텐츠를 가져오는 방법을 선택합니다.

   * **[!UICONTROL HTML 업로드]**: 컴퓨터에서 하나 이상의 HTML 이메일 파일을 선택하십시오.

   * **[!UICONTROL 연결에서 찾아보기]**: 파일을 수동으로 내보내고 업로드할 필요 없이 연결된 마케팅 플랫폼에서 직접 이메일을 검색하고 선택합니다.

   ![HTML을 업로드하거나 연결을 검색하는 옵션이 있는 전자 메일 콘텐츠 탭](assets/onboarding-hub-6.png)

1. HTML 업로드의 경우 파일을 찾아보거나 업로드 영역으로 드래그 앤 드롭합니다. 완료되면 **[!UICONTROL 업로드]**&#x200B;를 클릭합니다.

   파일은 `.html` 또는 `.htm` 형식이어야 하며 10MB 이하여야 합니다.

   ![전자 메일 콘텐츠에 대한 HTML 파일 업로드 영역](assets/onboarding-hub-7.png)

1. 연결에서 가져오려면 전자 메일 목록에서 선택하고 **[!UICONTROL 가져오기]**&#x200B;를 클릭합니다.

1. 가져온 이메일에 액세스하고 가져온 HTML을 검토합니다.

1. **[!UICONTROL 제목 줄]**&#x200B;을 추가하고 각 개인화 자리 표시자를 해당 프로필 특성에 매핑합니다.

   작업공간은 소스 스크립팅 구문을 자동으로 Handlebars 구문으로 변환합니다. 지원되는 연산자 목록을 보려면 [연산자](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/personalization/functions/operators)를 참조하십시오.

   ![제목 줄 필드 및 개인화 자리 표시자 매핑이 있는 전자 메일 편집기를 가져왔습니다](assets/onboarding-hub-8.png)

1. [!DNL Experience Manager Assets]에 전자 메일의 이미지를 업로드할 폴더를 선택하고 **[!UICONTROL 자산 업로드]**&#x200B;를 클릭합니다.

   ![Experience Manager Assets에 전자 메일 이미지를 업로드하기 위한 폴더 선택 창](assets/onboarding-hub-9.png)

1. 이메일이 준비되면 **[!UICONTROL 마이그레이션]**&#x200B;을 선택한 다음 **다음 항목 보기[!DNL Journey Optimizer]**&#x200B;를 선택하여 새 콘텐츠 템플릿을 엽니다.

   ![완료된 전자 메일에 대한 마이그레이션 단추 및 Journey Optimizer 보기 옵션](assets/onboarding-hub-10.png)

이제 콘텐츠 템플릿을 [!DNL Journey Optimizer]에서 사용할 수 있으며 여정에서 사용할 준비가 되었습니다.

➡️ [콘텐츠 템플릿에 대해 자세히 알아보기](../content-management/use-content-templates.md)

## 여정 가져오기 {#import-journeys}

여정 흐름의 스크린샷을 가져오거나 소스 플랫폼에 연결하여 여정을 다시 만듭니다.

1. **[!UICONTROL 여정]** 탭에서 여정 가져오기 방법을 선택합니다.

   * **[!UICONTROL 스크린샷 업로드]**: 컴퓨터에서 여정 스크린샷을 하나 이상 선택하십시오.

   * **[!UICONTROL 연결에서 찾아보기]**: 스크린샷을 수동으로 내보내고 업로드할 필요 없이 연결된 마케팅 플랫폼에서 직접 여정을 검색하고 선택합니다.

   스크린샷을 업로드하거나 연결에서 검색하는 옵션이 있는 ![여정 탭](assets/onboarding-hub-11.png)

1. HTML 업로드의 경우 파일을 찾아보거나 업로드 영역으로 드래그 앤 드롭합니다. 완료되면 **[!UICONTROL 업로드]**&#x200B;를 클릭합니다.

   파일은 .png, .jpg, .gif, .webp 형식이어야 하며 5MB 이하여야 합니다.

   ![여정 이미지의 스크린샷 업로드 영역](assets/onboarding-hub-13.png)

1. 연결에서 가져오려면 여정 목록에서 선택한 다음 **[!UICONTROL 가져오기]**&#x200B;를 클릭합니다.

1. 소스에서 작업 영역이 생성하는 여정을 미리 봅니다.

1. **[!UICONTROL 작업 항목]** 창에서 해당 항목이 속한 활동 유형에 따라 각 항목을 해결합니다.

   * 각 메시지 단계에 대해 채널 구성 및 콘텐츠 템플릿을 선택합니다.
   * 각 **[!UICONTROL 대상]** 활동에 대해 대상을 선택합니다.

1. **[!UICONTROL 변경 내용 적용]**&#x200B;을 선택한 다음 **다음[!DNL Journey Optimizer]**&#x200B;에서 보기 를 선택하여 여정 캔버스를 엽니다.

   해결된 활동 및 변경 내용 적용 단추가 있는 ![작업 항목 창](assets/onboarding-hub-12.png)

이제 [!DNL Journey Optimizer]에서 여정을 사용할 수 있습니다. 이 곳에서 캔버스를 검토하고 최종 조정을 수행한 다음 라이브로 전환할 준비가 되면 활성화할 수 있습니다.

➡️ [여정 만들기에 대해 자세히 알아보기](../building-journeys/journey-gs.md)

## 마이그레이션 추적 {#track-migration-progress}

작업 영역 개요를 사용하면 가져온 모든 이메일을 추적하고 아직 작업 대기 중인 이메일을 빠르게 찾을 수 있습니다. 가져온 각 이메일에는 검토, 마이그레이션 또는 실패 상태가 표시되므로 상태를 한눈에 볼 수 있습니다. 화면 상단의 KPI 세트는 각 상태에 있는 항목의 요약 개수를 제공합니다.

* **총 전자 메일**(또는 **총 여정**): 작업 영역으로 가져온 전체 항목 수입니다.
* **진행 중**: 마이그레이션하기 전에 아직 검토하거나 매핑하고 있는 항목입니다.
* **마이그레이션됨**: [!DNL Journey Optimizer]에서 사용할 수 있는 전환된 항목입니다.
* **실패**: 마이그레이션할 수 없어 주의가 필요한 항목입니다.

![총, 진행 중, 마이그레이션된 항목 및 실패한 항목에 대한 KPI가 포함된 Workspace 개요](assets/onboarding-hub-4.png)

필터 세트를 사용하면 가져온 이메일 콘텐츠 목록의 범위를 좁힐 수 있으므로 모든 항목을 스크롤하는 대신 특정 하위 집합에 집중할 수 있습니다. 다음 필터 중 하나 이상을 결합하여 원하는 항목을 찾습니다.

* **[!UICONTROL 상태]**: **[!UICONTROL 검토 필요]**, **[!UICONTROL 마이그레이션됨]** 또는 **[!UICONTROL 실패]**&#x200B;와 같은 특정 상태의 전자 메일만 표시합니다.
* **[!UICONTROL 생성됨]**: 특정 날짜 범위 내에 가져온 전자 메일을 표시합니다.
* **[!UICONTROL 업데이트됨]**: 특정 날짜 범위 내에서 마지막으로 수정한 전자 메일을 표시합니다.

![작업 영역의 상태, 만든 날짜 및 업데이트된 날짜에 대한 필터 옵션](assets/onboarding-hub-5.png)


