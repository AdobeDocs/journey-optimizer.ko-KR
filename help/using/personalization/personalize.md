---
title: Journey Optimizer에서 콘텐츠 개인화
description: 개인화 시작
feature: 개인화
topic: 개인화
role: Data Engineer
level: Beginner
source-git-commit: adb915a2013d1d1bf17ed5efb7ac4eb9c655c501
workflow-type: tm+mt
source-wordcount: '663'
ht-degree: 11%

---

# 개인화 시작{#add-personalization}

[!DNL Adobe Journey Optimizer] 개인화 기능을 살펴보고 그에 대한 데이터 및 정보를 활용하여 각 특정 수신자에게 메시지를 반영합니다. 그것은 그의 이름, 그의 관심, 그가 사는 곳, 그가 산 것 등이 될 수 있습니다.

[!DNL :arrow_forward:] [이 비디오에서 메시지를 개인화하는 방법을 알아봅니다](#video-perso)

[!DNL Journey Optimizer] 는  **** 중괄호로 묶은 내용을 포함하는 표현식을 만들 수 있도록 해주는 Handlebars 기반의 간단한 개인화 구문&#x200B;**{}**&#x200B;을 사용합니다. 동일한 콘텐츠 또는 필드에 제한 없이 여러 식을 추가할 수 있습니다. 자세한 내용은 [개인화 구문](personalization-syntax.md)을 참조하십시오.

개인화는 Adobe Experience Platform에 정의된 **XDM 개인 프로필** 스키마에서 관리하는 프로필 데이터를 기반으로 합니다. 자세한 내용은 [Adobe XDM(Experience Platform Data Model) 설명서](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko)를 참조하십시오.

>[!CAUTION]
>**XDM 개별 프로필** 스키마는 [!DNL Journey Optimizer]에서 컨텐츠를 개인화하는 데 사용할 수 있는 유일한 스키마입니다.

**예:**

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`

* `Hello {{profile.person.name.fullName}}`

메시지(전자 메일 및 푸시)를 처리할 때 Journey Optimizer은 표현식을 Experience Cloud 플랫폼 데이터베이스에 포함된 데이터로 대체합니다. `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`은 &quot;Hello John Doe&quot;가 됩니다.


## 개인화 컨텍스트{#personalization-areas}

[!DNL Journey Optimizer]에서 전달하는 메시지의 콘텐츠와 표시에 대해서는 여러 가지 방법으로 개인화할 수 있습니다.

편집기 아이콘이 있는 모든 필드에서 개인화 편집기(표현식 편집기라고도 함)를 열고 개인화를 정의할 수 있습니다.

![](assets/perso_icon.png)

### 이메일 개인화

이메일을 만들 때 메시지의 **이메일 제목** 필드에 개인화를 추가할 수 있습니다.

![](assets/perso_subject.png)

이메일 디자이너에서 콘텐츠를 개인화할 수 있습니다.

* **메시지**&#x200B;에서:텍스트 블록 내부를 클릭하고 상황별 도구 모음에서 **개인화** 아이콘을 클릭한 다음 **개인화 삽입** 필드를 선택합니다. 전자 메일 디자이너 인터페이스에 대한 자세한 내용은 이 [섹션](../design-emails.md)을 참조하십시오.

   ![](assets/perso_insert.png)

* **링크**&#x200B;의 경우:텍스트 블록 내의 텍스트나 이미지를 선택하고 상황별 도구 모음에서 **링크 삽입** 아이콘을 클릭합니다. 창에서 **개인화 추가** 아이콘을 클릭하여 개인화 블록을 추가할 수 있습니다.

   ![](assets/perso_link.png)

두 경우 모두 개인화 편집기에 액세스합니다.

![](assets/perso_ee.png)


### 푸시 알림 개인화

다음 필드에서 **푸시 알림**&#x200B;을 개인화할 수도 있습니다.

* **Title**
* **본문**
* **사용자 정의 사운드**
* **배지**
* **사용자 지정 데이터**

![](assets/perso_push.png)

[이 섹션](../push-gs.md)의 푸시 알림 구성에 대해 자세히 알아보십시오.

## 표현식 편집기 사용

표현식 편집기는 [!DNL Journey Optimizer]에 있는 개인화의 중심입니다.

이메일, 푸시 및 오퍼와 같은 개인화를 정의해야 하는 모든 컨텍스트에서 이 아이콘이 제공됩니다.

표현식 편집기 인터페이스에서 모든 데이터를 선택, 정렬, 사용자 지정 및 확인하여 컨텐츠에 대한 사용자 지정 개인화를 만듭니다.

![](assets/perso_ee1.png)

화면의 왼쪽 부분에는 개인화할 소스를 선택할 수 있는 도메인 선택기가 표시됩니다. 사용 가능한 소스는 다음과 같습니다.

* **프로필** :xdm( [Adobe Experience Platform 데이터 모델) 설명서](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html)에 설명된 프로필 스키마와 연결된 모든 참조를 나열합니다.
* **세그먼트 멤버십** :Adobe Experience Platform 세그멘테이션 서비스에서 만든 모든 세그먼트를 나열합니다. 세그먼테이션에 대한 자세한 내용은 [여기](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=en)를 참조하십시오.
* **오퍼** :특정 배치에 연결된 모든 오퍼를 나열합니다. 배치를 선택한 다음 컨텐츠에 오퍼를 삽입합니다. 오퍼를 관리하는 방법에 대한 전체 설명서는 [이 섹션](../deliver-personalized-offers.md)을 참조하십시오.
* **컨텍스트** :여정 **** 에서 메시지 활동을 사용하면 이 메뉴에서 컨텍스트 여정 필드를 사용할 수 있습니다. 자세한 내용은 [이 섹션](personalization-use-case.md)을 참조하십시오.
* **도우미 함수** :계산, 데이터 형식 지정 또는 전환, 조건 등과 같이 데이터에 대한 작업을 수행하고 개인화 컨텍스트에서 조작하는 데 사용할 수 있는 모든 도우미 함수를 나열합니다. 자세한 내용은 [이 섹션](functions/functions.md)을 참조하십시오.

선택 시 참조가 편집기에 추가됩니다.

>[!NOTE]
>
>&quot;+&quot; 아이콘 옆에 있는 정보 아이콘을 사용하면 각 변수에 대한 자세한 정보를 제공하는 도구 설명이 열립니다.

다음 예에서는 표현식 편집기를 사용하여 오늘이 생일인 프로필을 선택한 다음 이 날에 해당하는 특정 오퍼를 삽입하여 사용자 지정을 완료할 수 있습니다.

![](assets/perso_ee2.png)

## 방법 비디오{#video-perso}

여정에서 컨텍스트 기반 이벤트 정보를 사용하여 메시지를 개인화하는 방법을 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

여정에서 컨텍스트 기반 이벤트 정보를 사용하여 메시지를 개인화하는 방법을 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)
