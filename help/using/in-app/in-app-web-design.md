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
source-git-commit: 8a1ec5acef067e3e1d971deaa4b10cffa6294d75
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

인앱 메시지 콘텐츠를 편집하려면 Campaign의 **[!UICONTROL 작업]** 메뉴에서 **[!UICONTROL 콘텐츠 편집]** 단추를 클릭하십시오.

![](assets/in_app_web_surface_7.png)

**[!UICONTROL 고급 서식 설정]** 전환은 환경을 사용자 지정하는 추가 옵션을 활성화합니다.

인앱 메시지가 만들어지고 콘텐츠가 정의되고 개인화되면 이를 검토하고 활성화할 수 있습니다. 그러면 캠페인 일정에 따라 알림이 전송됩니다. [이 페이지](send-in-app.md)에서 자세히 알아보십시오.

## 메시지 레이아웃 {#message-layout}

**[!UICONTROL 메시지 레이아웃]** 섹션에서 메시지 요구 사항에 따라 선택할 4가지 레이아웃 옵션 중 하나를 선택합니다.

![](assets/in_app_web_design_1.png)

* **[!UICONTROL 전체 화면]**: 이 형식의 레이아웃은 대상 장치의 전체 화면을 포함합니다.

  미디어(이미지, 비디오), 텍스트 및 버튼 구성 요소를 지원합니다.

* **[!UICONTROL 모달]**: 이 레이아웃은 큰 경고 스타일 창에 나타나며 백그라운드에서 응용 프로그램이 계속 표시됩니다.

  미디어(이미지, 비디오), 텍스트 및 버튼 구성 요소를 지원합니다.

* **[!UICONTROL 배너]**: 이 유형의 레이아웃은 기본 OS 경고 메시지로 표시됩니다.

  메시지에 **[!UICONTROL 헤더]** 및 **[!UICONTROL 본문]**&#x200B;만 추가할 수 있습니다.

* **[!UICONTROL 사용자 지정]**: 사용자 지정 메시지 모드를 사용하면 미리 구성된 HTML 메시지 중 하나를 직접 가져오고 편집할 수 있습니다.

   * 원시 HTML 코드를 입력하거나 붙여 넣으려면 **[!UICONTROL 작성]**&#x200B;을 선택하세요.

     왼쪽 창을 사용하여 Journey Optimizer 개인화 기능을 활용합니다. 이 작업에 대한 자세한 정보는 [이 섹션](../personalization/personalize.md)을 참조하십시오.

   * HTML 내용이 포함된 HTML 또는 .zip 파일을 가져오려면 **[!UICONTROL 가져오기]**&#x200B;를 선택하십시오.

## 컨텐츠 탭 {#content-tab}

**콘텐츠** 탭에서 알림의 콘텐츠와 **닫기** 단추의 스타일을 정의하고 개인화할 수 있습니다. 인앱 알림에 미디어를 추가하고 이 탭에서 작업 버튼을 추가할 수도 있습니다.

### 닫기 버튼 {#close-button}

![](assets/in_app_web_design_2.png)

**[!UICONTROL 닫기 단추]**&#x200B;의 **[!UICONTROL 스타일]**&#x200B;을(를) 선택하십시오.

사용 가능한 스타일은 다음과 같습니다.

* **[!UICONTROL 단순]**
* **[!UICONTROL 원]**
* 미디어 URL 또는 Assets의 **[!UICONTROL 사용자 지정 이미지]**.

+++고급 서식이 있는 추가 옵션

**[!UICONTROL 고급 서식 모드]**&#x200B;가 켜져 있으면 **[!UICONTROL 색상]** 옵션을 선택하여 단추의 색상과 불투명도를 선택할 수 있습니다.

+++

### 미디어 {#add-media}

**[!UICONTROL 미디어]** 필드를 사용하면 인앱 메시지에 미디어를 추가하여 최종 사용자를 위한 매력적인 환경을 만들 수 있습니다.

![](assets/in_app_web_design_3.png)

미디어 URL을 입력하거나 **[!UICONTROL Assets 선택]** 아이콘을 클릭하여 Assets 라이브러리에 저장된 자산을 인앱 메시지에 직접 추가합니다. [자산 관리에 대해 자세히 알아보세요](../content-management/assets-essentials.md).
화면 읽기 응용 프로그램에 **[!UICONTROL 대체 텍스트]**&#x200B;를 추가할 수도 있습니다.

+++고급 서식이 있는 추가 옵션

**[!UICONTROL 고급 서식 모드]**&#x200B;가 켜져 있으면 미디어의 **[!UICONTROL 최대 높이]** 및 **[!UICONTROL 최대 너비]**&#x200B;를 사용자 지정할 수 있습니다.

+++

### 콘텐츠 {#title-body}

메시지를 작성하려면 **[!UICONTROL 헤더]** 및 **[!UICONTROL 본문]** 필드에 내용을 입력하십시오.

![](assets/in_app_web_design_4.png)

**[!UICONTROL Personalization]** 아이콘을 사용하여 개인화를 추가하십시오. Adobe Journey Optimizer 개인화 편집기 [의 개인화에 대한 자세한 내용은 이 섹션](../personalization/personalize.md)을 참조하세요.

+++고급 서식이 있는 추가 옵션

**[!UICONTROL 고급 서식 모드]**&#x200B;가 켜져 있으면 **[!UICONTROL 머리글]** 및 **[!UICONTROL 본문]**&#x200B;을 선택할 수 있습니다.

* **[!UICONTROL 글꼴]**
* **[!UICONTROL Pt 크기]**
* **[!UICONTROL 글꼴 색상]**
* **[!UICONTROL 정렬]**
+++

### 버튼 {#add-buttons}

사용자가 인앱 메시지와 상호 작용할 수 있는 버튼을 추가합니다.

![](assets/in_app_web_design_5.png)

버튼을 개인화하려면

1. 단추 #1 텍스트(기본) 필드를 편집합니다. **[!UICONTROL Personalization]** 아이콘을 사용하여 콘텐츠 및 개인화 데이터를 정의할 수도 있습니다.

1. 사용자가 상호 작용한 후 단추의 동작을 정의하는 **[!UICONTROL 상호 작용 이벤트]**&#x200B;를 선택하세요.

1. **[!UICONTROL Target]** 필드에 웹 URL이나 딥 링크를 입력합니다.

1. 여러 단추를 추가하려면 **[!UICONTROL 단추 추가]**&#x200B;를 클릭하세요.

+++고급 서식이 있는 추가 옵션

**[!UICONTROL 고급 서식 모드]**&#x200B;가 켜져 있으면 **[!UICONTROL 단추]**&#x200B;를 선택할 수 있습니다.

* **[!UICONTROL 글꼴]**
* **[!UICONTROL Pt 크기]**
* **[!UICONTROL 글꼴 색상]**
* **[!UICONTROL 정렬]**
* **[!UICONTROL 단추 스타일]**
* **[!UICONTROL 반경]**
* **[!UICONTROL 단추 색상]**

+++

## 설정 탭 {#settings-tab}

**설정** 탭에서 메시지 레이아웃을 정의하고 인앱 메시지를 미리 볼 수 있습니다. 고급 서식 옵션에 액세스할 수도 있습니다.

### 레이아웃 {#layout-options}

![](assets/in_app_web_design_6.png)

**[!UICONTROL 배경 이미지]** 필드를 사용하면 인앱 메시지에 배경을 추가할 수 있습니다.

* URL 링크의 미디어.

* 배경색입니다.

### 메시지 {#message-tab}

![](assets/in_app_web_design_7.png)

기본적으로 활성화되어 있는 UI 인계 옵션을 사용하면 인앱 메시지 뒤의 배경을 어둡게 하여 콘텐츠에 초점을 강조할 수 있습니다.

+++고급 서식이 있는 추가 옵션

**[!UICONTROL 고급 서식 모드]**&#x200B;가 켜져 있으면 다음 옵션을 사용하여 메시지를 개인화할 수 있습니다.

* **[!UICONTROL UI 인계 사용자 지정]**: 배경색과 불투명도에 표시할 색상을 선택할 수 있습니다.

* **[!UICONTROL 크기 사용자 지정]**: 인앱 알림의 너비와 높이를 조정할 수 있습니다.

* **[!UICONTROL 위치 사용자 지정]**: 사용자의 화면에서 인앱 메시지의 위치를 사용자 지정할 수 있습니다. 세로 및 가로 정렬을 변경할 수 있습니다.

* **[!UICONTROL 메시지 모퉁이]**: **[!UICONTROL 모퉁이 반경]**&#x200B;을 변경하여 인앱 알림에 모퉁이를 추가할 수 있습니다.

+++

**관련 항목:**

* [인앱 메시지 테스트 및 보내기](send-in-app.md)
* [인앱 보고서 ](../reports/campaign-global-report.md#inapp-report)
* [인앱 구성](inapp-configuration.md)