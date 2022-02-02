---
title: 표현식 편집기
description: 표현식 편집기 사용 방법을 알아봅니다.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
exl-id: fe39570b-cbd2-4b24-af10-e12990a9a885
source-git-commit: 01573675c28972f863e3516577d8a06b403de312
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 1%

---

# 표현식 편집기 {#build-personalization-expressions}

표현식 편집기는 의 개인화의 핵심입니다 [!DNL Journey Optimizer]. 이메일, 푸시 및 오퍼와 같은 개인화를 정의해야 하는 모든 컨텍스트에서 이 아이콘이 제공됩니다.

표현식 편집기 인터페이스에서 모든 데이터를 선택, 정렬, 사용자 지정 및 확인하여 컨텐츠에 대한 사용자 지정 개인화를 만듭니다.

![](assets/perso_ee1.png)

화면의 왼쪽 부분에는 개인화할 소스를 선택할 수 있는 도메인 선택기가 표시됩니다.

![](assets/perso_ee3.png)

사용 가능한 소스는 다음과 같습니다.

* **[!UICONTROL Profile attributes]** : 에 설명된 프로필 스키마와 연결된 모든 참조를 나열합니다. [Adobe Experience Platform 데이터 모델(XDM) 설명서](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko){target=&quot;_blank&quot;}.
* **[!UICONTROL Segment memberships]** : Adobe Experience Platform 세그멘테이션 서비스에서 만든 모든 세그먼트를 나열합니다. 세그먼테이션에 대한 자세한 내용을 사용할 수 있습니다 [여기](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html){target=&quot;_blank&quot;}.
* **[!UICONTROL Offer decisions]** : 특정 배치에 연결된 모든 오퍼를 나열합니다. 배치를 선택한 다음 컨텐츠에 오퍼를 삽입합니다. 오퍼를 관리하는 방법에 대한 전체 설명서는 [이 섹션](../deliver-personalized-offers.md).
* **[!UICONTROL Contextual attributes]** : http 화이트보드 **메시지** 여정에서 을 사용하는 경우 이 메뉴를 통해 컨텍스트 여정 필드를 사용할 수 있습니다. 추가 정보 [이 섹션](personalization-use-case.md).
* **[!UICONTROL Helper functions]** : 계산, 데이터 형식 지정 또는 전환, 조건 등과 같이 데이터에 대한 작업을 수행하고 개인화 컨텍스트에서 조작하는 데 사용할 수 있는 모든 도우미 함수를 나열합니다. 추가 정보 [이 섹션](functions/functions.md).

선택 시 참조가 편집기에 추가됩니다.

>[!NOTE]
>
>&quot;+&quot; 아이콘 옆에 있는 정보 아이콘을 사용하면 각 변수에 대한 자세한 정보를 제공하는 도구 설명이 열립니다.
>
>즐겨찾기에 가장 자주 사용하는 특성을 추가할 수 있습니다. 추가 정보 [이 섹션](personalization-favorites.md).

다음 예에서는 표현식 편집기를 사용하여 오늘이 생일인 프로필을 선택한 다음 이 날에 해당하는 특정 오퍼를 삽입하여 사용자 지정을 완료할 수 있습니다.

![](assets/perso_ee2.png)

개인화 표현식이 준비되면 표현식 편집기로 유효성 검사를 받아야 합니다. 추가 정보 [이 섹션](personalization-validation.md).