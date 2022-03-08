---
title: 표현식 편집기 정보
description: 표현식 편집기 사용 방법을 알아봅니다.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
exl-id: 1ac2a376-a3a8-41ae-9b04-37886697f0fc
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 5%

---

# 표현식 편집기 정보 {#build-personalization-expressions}

>[!CONTEXTUALHELP]
>id="ajo_perso_editor"
>title="표현식 편집기 정보"
>abstract="표현식 편집기를 사용하면 모든 데이터를 선택, 정렬, 사용자 지정 및 확인하여 컨텐츠에 대한 사용자 지정 개인화를 만들 수 있습니다."

표현식 편집기는 의 개인화의 핵심입니다 [!DNL Journey Optimizer]. 이메일, 푸시 및 오퍼와 같은 개인화를 정의해야 하는 모든 컨텍스트에서 이 아이콘이 제공됩니다.

표현식 편집기 인터페이스에서 모든 데이터를 선택, 정렬, 사용자 지정 및 확인하여 컨텐츠에 대한 사용자 지정 개인화를 만듭니다.

![](assets/perso_ee1.png)

화면의 왼쪽 부분에는 개인화할 소스를 선택할 수 있는 도메인 선택기가 표시됩니다.

![](assets/perso_ee3.png)

사용 가능한 소스는 다음과 같습니다.

* **[!UICONTROL Profile attributes]** : 에 설명된 프로필 스키마와 연결된 모든 참조를 나열합니다. [Adobe Experience Platform 데이터 모델(XDM) 설명서](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko){target=&quot;_blank&quot;}.
* **[!UICONTROL Segment memberships]** : Adobe Experience Platform 세그멘테이션 서비스에서 만든 모든 세그먼트를 나열합니다. 세그먼테이션에 대한 자세한 내용을 사용할 수 있습니다 [여기](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html){target=&quot;_blank&quot;}.
* **[!UICONTROL Offer decisions]** : 특정 배치에 연결된 모든 오퍼를 나열합니다. 배치를 선택한 다음 컨텐츠에 오퍼를 삽입합니다. 오퍼를 관리하는 방법에 대한 전체 설명서는 [이 섹션](../messages/deliver-personalized-offers.md).
* **[!UICONTROL Contextual attributes]** : http 화이트보드 **메시지** 여정에서 을 사용하는 경우 이 메뉴를 통해 컨텍스트 여정 필드를 사용할 수 있습니다. 추가 정보 [이 섹션](personalization-use-case.md).
* **[!UICONTROL Helper functions]** : 계산, 데이터 형식 지정 또는 전환, 조건 등과 같이 데이터에 대한 작업을 수행하고 개인화 컨텍스트에서 조작하는 데 사용할 수 있는 모든 도우미 함수를 나열합니다. 추가 정보 [이 섹션](functions/functions.md).

+ 단추를 클릭하여 속성에 편집기를 추가합니다.

>[!NOTE]
>
>&quot;+&quot; 아이콘 옆에 있는 타원 메뉴를 사용하면 각 변수에 대해 더 자세한 정보를 얻을 수 있고 가장 자주 사용하는 속성을 [즐겨찾기](personalization-favorites.md).

![](assets/attribute-details.png)

다음 예에서는 표현식 편집기를 사용하여 오늘이 생일인 프로필을 선택한 다음 이 날에 해당하는 특정 오퍼를 삽입하여 사용자 지정을 완료할 수 있습니다.

![](assets/perso_ee2.png)

개인화 표현식이 준비되면 표현식 편집기로 유효성 검사를 받아야 합니다. 추가 정보 [이 섹션](personalization-validation.md).
