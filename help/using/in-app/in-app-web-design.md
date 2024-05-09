---
title: 웹 인앱 콘텐츠 디자인
description: 웹 인앱 콘텐츠를 디자인하는 방법에 대해 알아봅니다
feature: In App
topic: Content Management
role: User
level: Beginner
keywords: 인앱, 메시지, 만들기, 시작
hide: true
hidefromtoc: true
source-git-commit: b62f8954e09f50896ad5e70784c5a93943617e85
workflow-type: tm+mt
source-wordcount: '780'
ht-degree: 7%

---

# 웹 인앱 콘텐츠 디자인 {#in-app-web-design}

>[!BEGINSHADEBOX]

**목차**

* [웹 인앱 채널 구성](configure-in-app-web.md)
* [웹 인앱 메시지 캠페인 만들기](create-in-app-web.md)
* 웹 인앱 콘텐츠 디자인

>[!ENDSHADEBOX]

인앱 메시지 콘텐츠를 편집하려면 다음을 클릭하십시오. **[!UICONTROL 콘텐츠 편집]** 단추 **[!UICONTROL 작업]** Campaign의 메뉴.

![](assets/in_app_web_surface_7.png)

다음 **[!UICONTROL 고급 서식]** 전환 은 경험을 사용자 지정하는 추가 옵션을 활성화합니다.

인앱 메시지가 만들어지고 콘텐츠가 정의되고 개인화되면 이를 검토하고 활성화할 수 있습니다. 그러면 캠페인 일정에 따라 알림이 전송됩니다. [이 페이지](send-in-app.md)에서 자세히 알아보십시오.

## 메시지 레이아웃 {#message-layout}

다음에서 **[!UICONTROL 메시지 레이아웃]** 섹션에서, 메시징 요구 사항에 따라 선택할 네 가지 레이아웃 옵션 중 하나를 선택합니다.

![](assets/in_app_web_design_1.png)

* **[!UICONTROL 전체 화면]**: 이 유형의 레이아웃은 대상 디바이스의 전체 화면을 포함합니다.

  미디어(이미지, 비디오), 텍스트 및 버튼 구성 요소를 지원합니다.

* **[!UICONTROL 모달]**: 이 레이아웃은 큰 경고 스타일 창에 나타나며 백그라운드에서 애플리케이션이 계속 표시됩니다.

  미디어(이미지, 비디오), 텍스트 및 버튼 구성 요소를 지원합니다.

* **[!UICONTROL 배너]**: 이 유형의 레이아웃은 기본 OS 경고 메시지로 표시됩니다.

  다음만 추가할 수 있습니다. **[!UICONTROL 머리글]** 및 a **[!UICONTROL 본문]** 메시지를 표시합니다.

* **[!UICONTROL 사용자 정의]**: 사용자 지정 메시지 모드를 사용하면 사전 구성된 HTML 메시지 중 하나를 직접 가져오고 편집할 수 있습니다.

   * 선택 **[!UICONTROL 작성]** 원시 HTML 코드를 입력하거나 붙여넣습니다.

     왼쪽 창을 사용하여 Journey Optimizer 개인화 기능을 활용합니다. 이 작업에 대한 자세한 정보는 [이 섹션](../personalization/personalize.md)을 참조하십시오.

   * 선택 **[!UICONTROL 가져오기]** HTML 내용이 포함된 HTML 또는 .zip 파일을 가져옵니다.

## 컨텐츠 탭 {#content-tab}

다음에서 **콘텐츠** 탭에서 알림의 콘텐츠와 스타일을 정의하고 개인화할 수 있습니다. **닫기** 단추를 클릭합니다. 인앱 알림에 미디어를 추가하고 이 탭에서 작업 버튼을 추가할 수도 있습니다.

### 닫기 버튼 {#close-button}

![](assets/in_app_web_design_2.png)

다음을 선택합니다. **[!UICONTROL 스타일]** / **[!UICONTROL 닫기 단추]**.

사용 가능한 스타일은 다음과 같습니다.

* **[!UICONTROL 단순]**
* **[!UICONTROL 원]**
* **[!UICONTROL 사용자 정의 이미지]** 미디어 URL 또는 에셋에서 참조할 수 있습니다.

+++고급 서식이 있는 추가 옵션

다음과 같은 경우 **[!UICONTROL 고급 서식 모드]** 이(가) 켜져 있으면 **[!UICONTROL 색상]** 단추의 색상과 불투명도를 선택하는 옵션입니다.

+++

### 미디어 {#add-media}

다음 **[!UICONTROL 미디어]** 필드를 사용하면 인앱 메시지에 미디어를 추가하여 최종 사용자를 위한 매력적인 경험을 만들 수 있습니다.

![](assets/in_app_web_design_3.png)

미디어 URL을 입력하거나 **[!UICONTROL 에셋 선택]** 아이콘 : 자산 라이브러리에 저장된 자산을 인앱 메시지에 직접 추가합니다. [에셋 관리에 대해 자세히 알아보기](../content-management/assets-essentials.md).
다음을 추가할 수도 있습니다. **[!UICONTROL 대체 텍스트]** 화면 읽기 애플리케이션용.

+++고급 서식이 있는 추가 옵션

다음과 같은 경우 **[!UICONTROL 고급 서식 모드]** 이(가) 켜져 있으므로 **[!UICONTROL 최대 높이]** 및 **[!UICONTROL 최대 폭]** 미디어.

+++

### 콘텐츠 {#title-body}

메시지를 작성하려면 **[!UICONTROL 머리글]** 및 **[!UICONTROL 본문]** 필드.

![](assets/in_app_web_design_4.png)

사용 **[!UICONTROL 개인화]** 아이콘을 클릭하여 개인화를 추가합니다. Adobe Journey Optimizer 표현식 편집기의 개인화에 대해 자세히 알아보기 [이 섹션에서](../personalization/personalize.md).

+++고급 서식이 있는 추가 옵션

다음과 같은 경우 **[!UICONTROL 고급 서식 모드]** 이(가) 켜져 있으므로 다음을 선택할 수 있습니다. **[!UICONTROL 머리글]** 및 **[!UICONTROL 본문]**:

* 다음 **[!UICONTROL 글꼴]**
* 다음 **[!UICONTROL Pt 크기]**
* 다음 **[!UICONTROL 글꼴 색상]**
* 다음 **[!UICONTROL 정렬]**
+++

### 버튼 {#add-buttons}

사용자가 인앱 메시지와 상호 작용할 수 있는 버튼을 추가합니다.

![](assets/in_app_web_design_5.png)

버튼을 개인화하려면

1. 단추 #1 텍스트(기본) 필드를 편집합니다. 다음을 사용할 수도 있습니다 **[!UICONTROL 개인화]** 아이콘 을 클릭하여 콘텐츠 및 개인화 데이터를 정의합니다.

1. 다음 항목 선택 **[!UICONTROL 이벤트 상호 작용]** - 사용자가 버튼과 상호 작용한 후의 버튼 작업을 정의합니다.

1. 웹 URL 또는 딥 링크를 **[!UICONTROL Target]** 필드.

1. 여러 버튼을 추가하려면 **[!UICONTROL 추가 단추]**.

+++고급 서식이 있는 추가 옵션

다음과 같은 경우 **[!UICONTROL 고급 서식 모드]** 이(가) 켜져 있으므로 다음을 선택할 수 있습니다. **[!UICONTROL 단추]**:

* 다음 **[!UICONTROL 글꼴]**
* 다음 **[!UICONTROL Pt 크기]**
* 다음 **[!UICONTROL 글꼴 색상]**
* 다음 **[!UICONTROL 정렬]**
* 다음 **[!UICONTROL 단추 스타일]**
* 다음 **[!UICONTROL 반경]**
* 다음 **[!UICONTROL 단추 색상]**

+++

## 설정 탭 {#settings-tab}

다음에서 **설정** 탭에서는 메시지 레이아웃을 정의하고 인앱 메시지를 미리 볼 수 있습니다. 고급 서식 옵션에 액세스할 수도 있습니다.

### 레이아웃 {#layout-options}

![](assets/in_app_web_design_6.png)

다음 **[!UICONTROL 배경 이미지]** 필드를 사용하면 인앱 메시지에 배경을 추가할 수 있습니다.

* URL 링크의 미디어.

* 배경색입니다.

### 메시지 {#message-tab}

![](assets/in_app_web_design_7.png)

기본적으로 활성화되어 있는 UI 인계 옵션을 사용하면 인앱 메시지 뒤의 배경을 어둡게 하여 콘텐츠에 초점을 강조할 수 있습니다.

+++고급 서식이 있는 추가 옵션

다음과 같은 경우 **[!UICONTROL 고급 서식 모드]** 이(가) 켜져 있으면 다음 옵션을 사용하여 메시지를 추가로 개인화할 수 있습니다.

* **[!UICONTROL UI 인계 사용자 지정]**: 배경에 표시할 색상과 해당 불투명도를 선택할 수 있습니다.

* **[!UICONTROL 크기 사용자 지정]**: 인앱 알림의 폭과 높이를 조정할 수 있습니다.

* **[!UICONTROL 위치 사용자 지정]**: 사용자 화면에서 인앱 메시지의 위치를 사용자 지정할 수 있습니다. 세로 및 가로 정렬을 변경할 수 있습니다.

* **[!UICONTROL 메시지 라운드 모서리]**: 를 변경하여 인앱 알림에 라운드 코너를 추가할 수 있습니다. **[!UICONTROL 모퉁이 반경]**.

+++

**관련 항목:**

* [인앱 메시지 테스트 및 보내기](send-in-app.md)
* [인앱 보고서 ](../reports/campaign-global-report.md#inapp-report)
* [인앱 구성](inapp-configuration.md)