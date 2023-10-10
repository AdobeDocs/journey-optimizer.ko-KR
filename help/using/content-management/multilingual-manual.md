---
solution: Journey Optimizer
product: journey optimizer
title: 다국어 콘텐츠 시작
description: Journey Optimizer의 다국어 콘텐츠에 대해 자세히 알아보기
feature: Multilingual
topic: Content Management
role: User
level: Beginner
keywords: 시작하기, 시작, 콘텐츠, 실험
hide: true
hidefromtoc: true
source-git-commit: 3b1acd7ada0637ce22e360e6e1bb35921dde2315
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 1%

---

# 다국어 콘텐츠 만들기 {#multilingual}

다국어 기능을 사용하면 단일 캠페인 내에서 손쉽게 여러 언어로 콘텐츠를 만들 수 있습니다. 이 기능을 사용하면 캠페인을 편집할 때 언어 간에 전환할 수 있으므로 전체 편집 프로세스를 간소화하고 다국어 콘텐츠를 효율적으로 관리할 수 있습니다.

## 로케일 만들기 {#create-locale}

다음에 설명된 대로 언어 설정을 구성할 때 [언어 설정 만들기](#language-settings) 섹션, 특정 로케일을 다국어 콘텐츠에 사용할 수 없는 경우 **[!UICONTROL 번역]** 메뉴 아래의 제품에서 사용할 수 있습니다.

1. 다음에서 **[!UICONTROL 관리]** 메뉴, 액세스 **[!UICONTROL 채널]**.

   번역 메뉴를 통해 활성화된 로케일 목록에 액세스할 수 있습니다.

1. 다음에서 **[!UICONTROL 로케일 사전]** 탭을 클릭하고 **[!UICONTROL 로케일 추가]**.

   ![](assets/locale_1.png)

1. 에서 로케일 코드를 선택합니다. **[!UICONTROL 언어]** 목록 및 관련 항목 **[!UICONTROL 지역]**.

1. 클릭 **[!UICONTROL 저장]** 로케일을 만들 수 있습니다.

   ![](assets/locale_2.png)

## 언어 설정 만들기 {#language-settings}

이 섹션에서는 다국어 콘텐츠 관리를 위한 기본 언어 및 관련 로케일을 설정할 수 있습니다. 프로필 언어와 관련된 정보를 조회하는 데 사용할 속성을 선택할 수도 있습니다

1. 다음에서 **[!UICONTROL 관리]** 메뉴, 액세스 **[!UICONTROL 채널]**.

1. 다음에서 **[!UICONTROL 언어 설정]** 메뉴, 클릭 **[!UICONTROL 언어 설정 만들기]**.

   ![](assets/multilingual-settings-1.png)

1. 의 이름을 입력합니다. **[!UICONTROL 언어 설정]**.

1. 다음 항목 선택 **[!UICONTROL 로케일]** 이 설정에 연결되었습니다. 최대 50개의 로케일을 추가할 수 있습니다.

   다음과 같은 경우 **[!UICONTROL 로케일]** 이(가) 누락되었습니다. 다음에서 미리 수동으로 생성할 수 있습니다. **[!UICONTROL 번역]** 메뉴 또는 API별 을(를) 참조하십시오 [새 로케일 만들기](#create-locale).

   ![](assets/multilingual-settings-2.png)

1. 다음에서 **[!UICONTROL 전송 환경 설정]** 메뉴에서 찾을 속성을 선택하여 프로필 언어에 대한 정보를 찾습니다.

   ![](assets/multilingual-settings-3.png)

1. 클릭 **[!UICONTROL 편집]** 옆에 있는 **[!UICONTROL 로케일]** 추가 개인화 및 추가 **[!UICONTROL 프로필 환경 설정]**.

   ![](assets/multilingual-settings-4.png)

1. 기타 선택 **[!UICONTROL 로케일]** 프로필 기본 설정 드롭다운에서 **[!UICONTROL 프로필 추가]**.

1. 의 고급 메뉴에 액세스 **[!UICONTROL 로케일]** 을(를) 정의하려면 **[!UICONTROL 기본 로케일]**, 즉 프로필 속성이 지정되지 않은 경우 기본 언어입니다.

   이 고급 메뉴에서 로케일을 삭제할 수도 있습니다.

   ![](assets/multilingual-settings-5.png)

1. 클릭 **[!UICONTROL 제출]** 다음을 만들려면: **[!UICONTROL 언어 설정]**.

<!--
1. Access the **[!UICONTROL Channel surfaces]** menu and create a new channel surface or select an existing one.

1. In the **[!UICONTROL Header parameters]** section, select the **[!UICONTROL Enable multilingual]** option.

1. Select your **[!UICONTROL Locales dictionary]** and add as many as needed.
-->

## 다국어 캠페인 만들기 {#create-multilingual-campaign}

1. 먼저 요구 사항에 따라 캠페인을 만들고 구성합니다. [자세히 알아보기](../campaigns/create-campaign.md)

1. 다음 위치로 이동 **[!UICONTROL 작업]** 메뉴 및 선택 **[!UICONTROL 콘텐츠 편집]**.

   ![](assets/multilingual-campaign-1.png)

1. 원래 콘텐츠를 만들거나 가져온 후 필요에 따라 개인화합니다.

1. 기본 컨텐츠가 만들어지면 **[!UICONTROL 저장]** campaign 구성 화면으로 돌아갑니다.

   ![](assets/multilingual-campaign-2.png)

1. 클릭 **[!UICONTROL 언어 추가]** 이전에 만든 을(를) 선택합니다 **[!UICONTROL 언어 설정]**. [자세히 알아보기](#create-language-settings)

   ![](assets/multilingual-campaign-3.png)

1. 의 고급 설정에 액세스 **[!UICONTROL 로케일]** 메뉴 및 선택 **[!UICONTROL 모든 로케일에 기본 복사]**.

   ![](assets/multilingual-campaign-4.png)

1. 이제 주요 콘텐츠가 선택한 전체 영역에서 복제됩니다.  **[!UICONTROL 로케일]**, 각 로케일에 액세스하고 **[!UICONTROL 이메일 본문 편집]** 콘텐츠 번역

   ![](assets/multilingual-campaign-5.png)

1. 다음을 사용하여 로케일을 비활성화하거나 활성화할 수 있습니다. **[!UICONTROL 추가 작업]** 선택한 로케일의 메뉴.

   ![](assets/multilingual-campaign-6.png)

1. 다국어 구성을 비활성화하려면 **[!UICONTROL 언어 추가]** 로컬 언어로 유지할 언어를 선택합니다.

   ![](assets/multilingual-campaign-7.png)

1. 클릭 **[!UICONTROL 활성화하려면 검토]** 캠페인 요약을 표시합니다.

   요약을 사용하면 필요한 경우 캠페인을 수정하고 매개 변수가 틀리거나 누락되었는지 확인할 수 있습니다.

1. 다국어 콘텐츠를 탐색하여 각 언어로 렌더링을 확인합니다.

   ![](assets/multilingual-campaign-8.png)

1. 캠페인이 올바르게 구성되었는지 확인한 다음, **[!UICONTROL 활성화]**.

이제 캠페인이 활성화되었습니다. 캠페인에 구성된 메시지는 즉시 전송되거나 지정된 날짜에 전송됩니다. Campaign이 라이브되는 즉시 수정할 수 없습니다. 콘텐츠를 재사용하기 위해 캠페인을 복제할 수 있습니다.

전송되면 캠페인 보고서 내에서 캠페인의 영향을 측정할 수 있습니다.

## 다국어 캠페인 보고서 {#multilingual-campaign-report}

전역 보고서, 다음에서 액세스 가능: **모든 시간** 탭에는 최소 2시간 전에 발생한 이벤트가 표시되며, 선택한 기간 동안의 이벤트도 표시됩니다. Campaign 글로벌 보고서는 Campaign에서 **[!UICONTROL 보고서 보기]** 단추를 클릭합니다.

Campaign 보고서에서 사용할 수 있는 데이터에 대한 자세한 내용은 다음을 참조하십시오. [이 페이지](../reports/campaign-global-report.md).

+++다국어 콘텐츠에 사용할 수 있는 다양한 지표 및 위젯에 대해 자세히 알아보십시오.

![](assets/report_multilingual.png)

다음 **[!UICONTROL 언어별 이메일 전송 통계]** 위젯은 다음에 따라 게재의 성공을 자세히 설명합니다. **[!UICONTROL 로케일]**:

* **[!UICONTROL 전달됨]**: 성공적으로 전송된 메시지 수와 총 전송된 메시지 수

* **[!UICONTROL 바운스]**: 총 보낸 메시지 수와 관련하여 게재 및 자동 반환 처리 중에 누적된 총 오류.

* **[!UICONTROL 오류]**: 게재 중에 발생하여 프로필로 전송되지 않은 총 오류 수입니다.

다음 **[!UICONTROL 언어별 이메일 추적 통계]** 위젯에는 다음에 따라 게재에 대한 수신자 활동에 사용할 수 있는 데이터가 포함되어 있습니다. **[!UICONTROL 로케일]**:

* **[!UICONTROL 구독 취소]**: 구독 취소 링크의 클릭 수입니다.

* **[!UICONTROL 열림]**: 메시지가 열린 횟수입니다.

* **[!UICONTROL 클릭수]**: 콘텐츠를 클릭한 횟수입니다.
+++


<!--
# Create a multilingual journey {#create-multilingual-journey}

1. Create your journey with a Delivery and personalize your content as needed.
1. From your delivery action, click Edit content.
1. Click Add languages.

# Translation project/ Create translation project:

1. From the Translation projects menu, click Create project.
1. Type-in a Name and Description.
1. Select the Source locale.
1. Click Add language to access the menu and define the languages for your translation project.
1. Select from the list your Target locale(s) and choose which Translation provider you want to use.
1. Click Add language when you finished linking your Target locale with the correct Translation provider.
1. Click Save.
1. From the Advanced menu of your Translation project, you can choose to Edit, deactive or delete it.
-->
