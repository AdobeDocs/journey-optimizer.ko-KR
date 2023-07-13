---
solution: Journey Optimizer
product: journey optimizer
title: 표현식 편집기 정보
description: 표현식 편집기로 작업하는 방법을 알아봅니다.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: 표현식, 편집기, 정보, 시작
exl-id: 1ac2a376-a3a8-41ae-9b04-37886697f0fc
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '420'
ht-degree: 12%

---

# 표현식 편집기 시작 {#build-personalization-expressions}

>[!CONTEXTUALHELP]
>id="ajo_perso_editor"
>title="표현식 편집기 정보"
>abstract="표현식 편집기를 통해 모든 데이터를 선택하고, 배열하고, 사용자 정의하고 검증하여 개인 맞춤화 콘텐츠를 만들 수 있습니다."

표현식 편집기는 의 개인화의 중심입니다 [!DNL Journey Optimizer]. 이메일, 푸시 및 오퍼와 같은 개인화를 정의해야 하는 모든 컨텍스트에서 사용할 수 있습니다.

표현식 편집기 인터페이스에서 모든 데이터를 선택하고, 정렬하고, 사용자 정의하고, 유효성을 검사하여 콘텐츠에 대한 사용자 지정된 개인화를 만듭니다.

![](assets/perso_ee1.png)

## 사용 가능한 개인화 소스 {#sources}

화면의 왼쪽 부분에는 개인화할 소스를 선택할 수 있는 도메인 선택기가 표시됩니다. 사용 가능한 소스는 다음과 같습니다.

* **[!UICONTROL 프로필 속성]** : 다음에 설명된 프로필 스키마와 관련된 모든 참조를 나열합니다. [Adobe Experience Platform 데이터 모델(XDM) 설명서](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko-KR){target="_blank"}.
* **[!UICONTROL 대상]** : Adobe Experience Platform 세그멘테이션 서비스에서 만든 모든 대상을 나열합니다. 세그멘테이션에 대한 추가 정보 사용 가능 [여기](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html){target="_blank"}.
* **[!UICONTROL 오퍼 결정]** : 특정 배치와 관련된 모든 오퍼를 나열합니다. 배치를 선택한 다음 콘텐츠에 오퍼를 삽입합니다. 오퍼 관리 방법에 대한 전체 설명서는 를 참조하십시오. [이 섹션](../offers/get-started/starting-offer-decisioning.md).
* **[!UICONTROL 컨텍스트 속성]** : 여정에서 채널 작업 활동(이메일, 푸시, SMS)을 사용하면 이 메뉴를 통해 상황별 여정 필드를 사용할 수 있습니다. 자세한 내용은 [이 섹션](personalization-use-case.md)을 참조하십시오.
* **[!UICONTROL 도우미 함수]** : 계산, 데이터 형식 지정 또는 전환, 조건 및 개인화의 컨텍스트에서 조작 등 데이터에 대한 작업을 수행하는 데 사용할 수 있는 모든 도우미 함수를 나열합니다. 자세한 내용은 [이 섹션](functions/functions.md)을 참조하십시오.

## 개인화 속성 추가 {#add}

+ 단추를 클릭하여 개인화 표현식에 속성을 추가합니다.

&quot;+&quot; 아이콘 옆에 있는 줄임표 메뉴를 사용하면 각 변수에 대한 자세한 내용을 확인하고 가장 자주 사용하는 속성을 즐겨찾기에 추가할 수 있습니다. [즐겨찾기에 속성을 추가하는 방법 알아보기](personalization-favorites.md)

또한 문자열 유형 프로필 속성이 비어 있는 경우 표시될 기본 대체 텍스트를 정의할 수 있습니다. 이렇게 하려면 속성 옆에 있는 줄임표 버튼을 클릭하고 을 선택합니다 **[!UICONTROL 대체 텍스트가 있는 삽입]**. 프로필에 대한 속성 값이 비어 있는 경우 기본적으로 표시되는 텍스트를 작성한 다음 을 클릭합니다 **[!UICONTROL 추가]**.

![](assets/attribute-details.png)

다음 예에서는 표현식 편집기를 사용하여 오늘 생일이 있는 프로필을 선택한 다음 해당 날짜에 해당하는 특정 오퍼를 삽입하여 맞춤화를 완료할 수 있습니다.

![](assets/perso_ee2.png)

개인화 표현식이 준비되면 표현식 편집기에서 유효성을 검사해야 합니다. 자세한 내용은 [이 섹션](personalization-validation.md)을 참조하십시오.
