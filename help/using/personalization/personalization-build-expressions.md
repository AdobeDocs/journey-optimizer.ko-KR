---
solution: Journey Optimizer
product: journey optimizer
title: 개인화 편집기 정보
description: 개인화 편집기로 작업하는 방법을 알아봅니다.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: 표현식, 편집기, 정보, 시작
exl-id: 1ac2a376-a3a8-41ae-9b04-37886697f0fc
source-git-commit: 155ae8ef14e5482d94e54b15962afa09aa6826fc
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 10%

---

# 개인화 편집기 시작하기 {#build-personalization-expressions}

>[!CONTEXTUALHELP]
>id="ajo_perso_editor"
>title="개인화 편집기 정보"
>abstract="개인화 편집기를 통해 모든 데이터를 선택하고, 배열하고, 사용자 정의하고 검증하여 개인 맞춤화 콘텐츠를 만들 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_perso_editor_autocomplete"
>title="자동 완성"
>abstract="이 옵션을 전환하면 표현식을 입력하는 동안 시스템에서 코드를 자동으로 완료하고 제안을 할 수 있습니다. 이 옵션은 HTML 및 텍스트 형식에만 사용할 수 있습니다."

개인화 편집기는 [!DNL Journey Optimizer]에서 개인화의 중심입니다. 이메일, 푸시 및 오퍼와 같은 개인화를 정의해야 하는 모든 컨텍스트에서 사용할 수 있습니다.

개인화 편집기 인터페이스에서 모든 데이터를 선택하고, 정렬하고, 맞춤화하고, 유효성을 검사하여 콘텐츠에 대한 맞춤화된 개인화를 만듭니다.

![](assets/perso_ee1.png)

## 사용 가능한 개인화 소스 {#sources}

화면의 왼쪽 부분에는 개인화할 소스를 선택할 수 있는 도메인 선택기가 표시됩니다. 사용 가능한 소스는 다음과 같습니다.

* **[!UICONTROL 프로필 특성]** : [XDM(Adobe Experience Platform 데이터 모델) 설명서](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko-KR){target="_blank"}에 설명된 프로필 스키마와 관련된 모든 참조를 나열합니다.
* **[!UICONTROL 대상]** : Adobe Experience Platform 세분화 서비스에서 만든 모든 대상을 나열합니다. 사용 가능한 세분화에 대한 자세한 정보는 [여기](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=ko){target="_blank"}를 참조하세요.
* **[!UICONTROL 오퍼 결정]** : 특정 배치와 관련된 모든 오퍼를 나열합니다. 배치를 선택한 다음 콘텐츠에 오퍼를 삽입합니다. 오퍼 관리 방법에 대한 전체 문서를 보려면 [이 섹션](../offers/get-started/starting-offer-decisioning.md)을 참조하세요.
* **[!UICONTROL 컨텍스트 특성]** : 여정 또는 캠페인에서 채널 작업 활동(이메일, 푸시, SMS)을 사용하면 이벤트 및 속성과 관련된 컨텍스트 특성을 개인화할 수 있습니다. 컨텍스트 특성을 활용하는 개인화의 예가 [이 섹션](personalization-use-case.md)에 나와 있습니다.
* **[!UICONTROL 도우미 함수]** : 계산, 데이터 서식 지정 또는 전환, 조건, 개인화 컨텍스트에서 조작 등 데이터에 대한 작업을 수행하는 데 사용할 수 있는 모든 도우미 함수를 나열합니다. 자세한 내용은 [이 섹션](functions/functions.md)을 참조하십시오.

## 개인화 속성 추가 {#add}

+ 단추를 클릭하여 개인화 표현식에 속성을 추가합니다.

&quot;+&quot; 아이콘 옆에 있는 줄임표 메뉴를 사용하면 각 변수에 대한 자세한 내용을 확인하고 가장 자주 사용하는 속성을 즐겨찾기에 추가할 수 있습니다. [즐겨찾기에 특성을 추가하는 방법 알아보기](personalization-favorites.md)

>[!NOTE]
>
>작성 워크플로우를 사용하여 생성된 보강 속성을 사용하여 대상자를 타겟팅하는 경우 이러한 보강 속성을 활용하여 메시지를 개인화할 수 있습니다. [대상 데이터 보강 특성을 사용하는 방법을 알아보세요](../audience/about-audiences.md#enrichment)

또한 문자열 유형 프로필 속성이 비어 있는 경우 표시될 기본 대체 텍스트를 정의할 수 있습니다. 이렇게 하려면 특성 옆에 있는 줄임표 버튼을 클릭하고 **[!UICONTROL 대체 텍스트로 삽입]**&#x200B;을 선택합니다. 프로필에 대한 특성 값이 비어 있는 경우 기본적으로 표시되는 텍스트를 작성한 다음 **[!UICONTROL 추가]**&#x200B;를 클릭합니다.

![](assets/attribute-details.png)

다음 예에서는 개인화 편집기를 사용하여 생일이 오늘 인 프로필을 선택한 다음 해당 요일에 해당하는 특정 오퍼를 삽입하여 맞춤화를 완료할 수 있습니다.

![](assets/perso_ee2.png)

개인화 표현식이 준비되면 개인화 편집기에서 유효성을 검사해야 합니다. 자세한 내용은 [이 섹션](personalization-validation.md)을 참조하십시오.
