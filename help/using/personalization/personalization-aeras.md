---
title: Journey Optimizer의 개인화 컨텍스트
description: 개인화를 추가할 수 있는 컨텍스트 파악
translation-type: tm+mt
source-git-commit: e73b47ab6243b13f82aa1503bd8c751f976f29ee
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 2%

---

# 개인화 영역 {#personalization-areas}

![](../assets/do-not-localize/badge.png)

Journey Optimizer에서 제공하는 메시지 내용 및 표시는 여러 가지 방법으로 개인화할 수 있습니다.

편집기 아이콘과 연관된 모든 필드는 개인화 편집기를 열고 개인화 콘텐츠를 수신할 수 있습니다.

![](assets/perso_icon.png)

## 이메일 개인화

이메일 채널 메시지를 만드는 동안 **이메일 제목** 필드는 개인화할 수 있습니다.

![](assets/perso_subject.png)

이메일 디자이너는 컨텐츠를 개인화할 수 있습니다.

* **메시지**&#x200B;에서:텍스트 블록 내부를 클릭하고 컨텍스트 도구 모음에서 **개인화** 아이콘을 클릭한 다음 **개인화 삽입** 필드를 선택합니다. 이메일 디자이너 인터페이스에 대한 자세한 내용은 이 [섹션](../design-emails.md)을 참조하십시오.

   ![](assets/perso_insert.png)

* **링크**&#x200B;의 경우:텍스트 블록 내의 텍스트 또는 이미지를 선택하고 컨텍스트 도구 모음에서 **링크 삽입** 아이콘을 클릭합니다. 창에서 **개인화 추가** 아이콘을 클릭하여 개인화 블록을 추가할 수 있습니다.

   ![](assets/perso_link.png)

## 푸시 알림 개인화

**푸시 채널**&#x200B;에서 개인화를 통해 푸시 알림을 세밀하게 조정할 수 있습니다.

다음 필드에 개인화를 추가할 수 있습니다.

* **Title**
* **본문**
* **사용자 정의 사운드**
* **배지**
* **사용자 지정 데이터**

![](assets/perso_push.png)

푸시 알림 구성에 대한 전체 문서는 [이 섹션](../configure-push.md)을 참조하십시오.


## 표현식 편집기 사용

표현식 편집기가 Journey Optimizer에서 개인화의 핵심입니다.

이메일, 푸시 및 오퍼와 같은 개인화를 정의해야 하는 모든 컨텍스트에서 제공됩니다.

표현식 편집기 인터페이스에서 모든 데이터를 선택, 정렬, 사용자 정의 및 확인하여 컨텐츠에 대한 사용자 정의 개인화를 만듭니다.

![](assets/perso_ee1.png)

화면의 왼쪽 부분에는 개인화할 소스를 선택할 수 있는 도메인 선택기가 표시됩니다.

* **프로필** :XDM( [Adobe Experience Platform Data Model) 설명서에 설명된 프로필 스키마에 연결된 모든 참조를 나열합니다](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko).
* **세그먼트 멤버십** :Adobe Experience Platform 세그멘테이션 서비스에서 만든 모든 세그먼트를 나열합니다. 사용 가능한 세그먼테이션에 대한 자세한 내용은 [여기](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=en)를 참조하십시오.
* **오퍼** :특정 배치와 연관된 모든 오퍼를 나열합니다. 배치를 선택한 다음 오퍼를 컨텐츠에 삽입합니다. 오퍼를 관리하는 방법에 대한 전체 문서는 [이 섹션](../../using/offers/get-started/starting-offer-decisioning.md)을 참조하십시오.

선택 시 참조가 편집기에 추가됩니다.

>[!NOTE]
>
>&quot;+&quot; 아이콘 옆의 정보 아이콘은 각 변수에 대한 자세한 내용을 제공하는 도구 설명을 엽니다.

다음 예에서 표현식 편집기를 사용하면 오늘 생일을 맞는 프로필을 선택한 다음 이 날짜에 해당하는 특정 오퍼를 삽입하여 사용자 지정을 완료할 수 있습니다.

![](assets/perso_ee2.png)




