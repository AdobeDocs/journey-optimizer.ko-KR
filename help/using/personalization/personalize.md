---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer에서 콘텐츠 개인화
description: 개인화를 시작합니다.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Beginner
keywords: 표현식, 편집기, 시작, 개인화
exl-id: f448780b-91bc-455e-bf10-9a9aee0a0b24
source-git-commit: 78c1464ccddec75e4827cbb1877d8fab5ac08b90
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 30%

---

# 개인화 시작{#add-personalization}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card5"
>title="개인화 경험"
>abstract="**Adobe Journey Optimizer**&#x200B;를 사용하면 수신자에 대한 데이터와 정보를 활용하여 각 수신자에 맞게 메시지를 적응할 수 있습니다. 이는 이름, 관심사, 거주지, 구입한 제품 등이 될 수 있습니다."

[!DNL Adobe Journey Optimizer] 개인화 기능을 사용하면 보유한 데이터 및 정보를 활용하여 메시지를 각 특정 받는 사람에게 적용할 수 있습니다. 이는 이름, 관심사, 거주지, 구입한 제품 등이 될 수 있습니다.

## 개인화 작동 방식

**개인화 편집기**&#x200B;를 사용하면 모든 데이터를 선택하고, 정렬하고, 사용자 지정하고, 유효성을 검사하여 콘텐츠에 맞는 사용자 지정 개인화를 만들 수 있으며, 도우미 함수나 미리 정의된 표현식 등 다양한 도구를 활용하여 메시지를 효과적으로 사용자 지정할 수 있습니다.

Journey Optimizer에서는 중괄호 **{{}}**&#x200B;로 묶은 내용을 포함하는 식을 만들 수 있는 Handlebars를 기반으로 한 인라인 개인화 구문을 사용합니다.

메시지를 처리할 때 Journey Optimizer은 표현식을 Experience Platform 데이터 세트에 포함된 데이터로 대체합니다. 예를 들어 `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`은(는) 동적으로 `Hello John Doe`이(가) 됩니다.

이 구문을 사용하면 이메일 제목 줄, 메시지 본문, 푸시 알림 또는 URL을 포함하여 여러 필드에 메시지를 개인화할 수 있습니다.

## 개인화에 사용되는 데이터

Personalization은 Adobe Experience Platform에 정의된 **XDM 개인 프로필** 스키마에서 관리하는 프로필 데이터를 기반으로 합니다. **XDM 개인 프로필** 스키마는 [!DNL Journey Optimizer]에서 콘텐츠를 개인화하는 데 사용할 수 있는 유일한 스키마입니다. 자세한 내용은 [XDM(Adobe Experience Platform 데이터 모델) 설명서](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko){target="_blank"}를 참조하세요.

**계산된 특성**&#x200B;을 활용하여 콘텐츠를 개인화할 수도 있습니다. 계산된 속성을 사용하면 개별 행동 이벤트를 Adobe Experience Platform에서 사용할 수 있는 계산된 프로필 속성으로 요약할 수 있습니다. [계산된 특성으로 작업하는 방법을 알아봅니다](../audience/computed-attributes.md)

또한 [!DNL Journey Optimizer]을(를) 사용하면 개인화 편집기에서 Adobe Experience Platform의 데이터를 활용하여 콘텐츠를 개인화할 수 있습니다. 이렇게 하려면 조회 개인화에 필요한 데이터 세트를 먼저 API 호출을 통해 활성화해야 합니다. 완료되면 해당 데이터를 사용하여 콘텐츠를 Journey Optimizer에 개인화할 수 있습니다. 이 기능은 현재 Beta에서 사용할 수 있습니다. [자세히 알아보기](../personalization/lookup-aep-data.md)

## 더 자세히 알아보기

이제 **[!DNL Journey Optimizer]**&#x200B;의 개인화에 대해 이해했으므로 이 설명서 섹션을 자세히 살펴보고 기능 작업을 시작할 차례입니다.

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="personalization-build-expressions.md">
<img alt="개인화 추가" src="assets/do-not-localize/add.png">
</a>
<div>
<a href="personalization-build-expressions.md"><strong>개인화 추가</strong></a>
</div>
<p>
</td>
<td>
<a href="../personalization/personalization-syntax.md">
<img alt="리드" src="assets/do-not-localize/syntax.png">
</a>
<div><a href="../personalization/personalization-syntax.md"><strong>Personalization 구문</strong>
</div>
<p>
</td>
<td>
<a href="../personalization/functions/functions.md">
<img alt="드물게" src="assets/do-not-localize/functions.png">
</a>
<div>
<a href="../personalization/functions/functions.md"><strong>도우미 함수 목록</strong></a>
</div>
<p></td>
<td>
<a href="../personalization/personalization-use-case.md">
<img alt="드물게" src="assets/do-not-localize/uc.png">
</a>
<div>
<a href="../personalization/personalization-use-case.md"><strong>Personalization 사용 사례</strong></a>
</div>
<p></td>
</tr></table>

## 방법 비디오{#video-perso}

여정에서 얻은 컨텍스트 기반 이벤트 정보를 사용하여 메시지를 개인화하는 방법을 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

메시지에 프로필 기반 개인 맞춤화를 추가하는 방법과 개인 맞춤화 블록의 전제 조건으로 대상자 멤버십을 사용하는 방법에 대해 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)

