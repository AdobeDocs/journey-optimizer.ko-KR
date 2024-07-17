---
title: Journey Optimizer에서 웹 인앱 메시지 만들기
description: Journey Optimizer에서 웹 인앱 메시지를 만드는 방법을 알아봅니다
feature: In App
topic: Content Management
role: User
level: Beginner
keywords: 인앱, 메시지, 만들기, 시작
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 2%

---


# 웹 인앱 채널 구성 {#configure-in-app-web}

## 전제 조건 {#prerequisites}

* **Adobe Experience Platform Web SDK** 확장에 최신 버전을 사용하고 있는지 확인하십시오.

* **태그 속성**&#x200B;에 **Adobe Experience Platform Web SDK** 확장을 설치하고 **Personalization 저장소** 옵션을 활성화하십시오.

  이 구성은 클라이언트에서 이벤트 기록을 저장하는 데 필수적이며, 규칙 빌더에서 빈도 규칙을 구현하기 위한 전제 조건입니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration.html?lang=en)

  ![](assets/configure_web_inapp_1.png)

## 플랫폼 규칙에 전송된 데이터 구성 {#configure-sent-data-trigger}

1. **Adobe Experience Platform 데이터 수집** 인스턴스에 액세스하여 **Adobe Experience Platform Web SDK** 확장으로 구성된 **태그 속성**&#x200B;으로 이동합니다.

1. **작성** 메뉴에서 **규칙**&#x200B;을 선택한 다음 **새 규칙 만들기** 또는 **규칙 추가**&#x200B;를 선택합니다.

   ![](assets/configure_web_inapp_2.png)

1. **이벤트** 섹션에서 **추가**&#x200B;를 클릭하고 다음과 같이 구성하십시오.

   * **확장**: 코어

   * **이벤트 유형**: 라이브러리가 로드되었습니다(페이지 상단).

   ![](assets/configure_web_inapp_3.png)

1. 이벤트 구성을 저장하려면 **변경 내용 유지**&#x200B;를 클릭합니다.

1. **작업** 섹션에서 **추가**&#x200B;를 클릭하고 다음과 같이 구성하십시오.

   * **확장**: Adobe Experience Platform 웹 SDK

   * **작업 유형**: 이벤트 보내기

   ![](assets/configure_web_inapp_4.png)

1. **Action** 형식의 **Personalization** 섹션에서 **시각적 개인화 결정 렌더링** 옵션을 사용하도록 설정하십시오.

   ![](assets/configure_web_inapp_5.png)

1. **결정 컨텍스트** 섹션에서 전달할 경험을 결정하는 **키** 및 **값** 쌍을 정의합니다.

   ![](assets/configure_web_inapp_6.png)

1. **변경 내용 유지**&#x200B;를 클릭하여 **작업** 구성을 저장합니다.

1. **게시 흐름** 메뉴로 이동합니다. 새 **라이브러리**&#x200B;를 만들거나 기존 **라이브러리**&#x200B;를 선택하고 새로 만든 **규칙**&#x200B;을(를) 추가하십시오. [자세히 알아보기](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/libraries.html?lang=en#create-a-library)

1. **라이브러리**&#x200B;에서 **개발에 저장 및 빌드**&#x200B;를 선택합니다.

   ![](assets/configure_web_inapp_7.png)

## 수동 규칙 구성 {#configure-manual-trigger}

1. **Adobe Experience Platform 데이터 수집** 인스턴스에 액세스하여 **Adobe Experience Platform Web SDK** 확장으로 구성된 **태그 속성**&#x200B;으로 이동합니다.

1. **작성** 메뉴에서 **규칙**&#x200B;을 선택한 다음 **새 규칙 만들기** 또는 **규칙 추가**&#x200B;를 선택합니다.

   ![](assets/configure_web_inapp_8.png)

1. **이벤트** 섹션에서 **추가**&#x200B;를 클릭하고 다음과 같이 구성하십시오.

   * **확장**: 코어

   * **이벤트 유형**: 클릭

   ![](assets/configure_web_inapp_9.png)

1. **구성 클릭**&#x200B;에서 평가할 **선택기**&#x200B;을(를) 정의합니다.

   ![](assets/configure_web_inapp_10.png)

1. **변경 내용 유지**&#x200B;를 클릭하여 **이벤트** 구성을 저장합니다.

1. **작업** 섹션에서 **추가**&#x200B;를 클릭하고 다음과 같이 구성하십시오.

   * **확장**: Adobe Experience Platform 웹 SDK

   * **작업 유형**: 규칙 집합 평가

   ![](assets/configure_web_inapp_11.png)

1. **작업** 형식의 **규칙 집합 평가 작업** 섹션에서 **시각적 개인화 결정 렌더링** 옵션을 사용하도록 설정하십시오.

   ![](assets/configure_web_inapp_13.png)

1. **결정 컨텍스트** 섹션에서 전달할 경험을 결정하는 **키** 및 **값** 쌍을 정의합니다.

1. **게시 흐름** 메뉴에 액세스하거나 새 **라이브러리**&#x200B;를 만들거나 기존 **라이브러리**&#x200B;를 선택하고 새로 만든 **규칙**&#x200B;을(를) 추가하십시오. [자세히 알아보기](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/libraries.html?lang=en#create-a-library)

1. **라이브러리**&#x200B;에서 **개발에 저장 및 빌드**&#x200B;를 선택합니다.

   ![](assets/configure_web_inapp_14.png)

