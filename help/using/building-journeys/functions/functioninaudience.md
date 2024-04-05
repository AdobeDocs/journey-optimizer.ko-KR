---
product: journey optimizer
title: inAudience
description: inAudience 함수에 대해 알아봅니다.
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inAudience, 함수, 표현식, 여정
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 6%

---

# inAudience {#inAudience}

개인이 주어진 대상자에 속하는지 확인합니다.

>[!NOTE]
>
>최대 100개의 대상을 검색할 수 있습니다.

대상 이름은 문자열 상수여야 합니다. 필드 참조나 식이 될 수 없습니다.

대상자는에 정의되어 있습니다. [Adobe Experience Platform](https://platform.adobe.com/audience/overview). 표현식 편집기는 자동으로 완성된 대상자 목록을 제공합니다.

대상자는 다음 세 가지 상태를 가질 수 있습니다.

* 기존: 엔티티가 대상에 계속 포함됩니다.
* 인식됨: 엔티티가 대상자로 들어가고 있습니다.
* 종료됨: 엔티티가 대상을 종료하는 중입니다.

다음을 보유한 개인만 **실현됨** 및 **기존 항목** 대상자 참여 상태는 대상자의 구성원으로 간주됩니다. 대상을 평가하는 방법에 대한 자세한 내용은 [세그먼테이션 서비스 설명서](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results).

`inAudience('audienceName') == true` 은(는) 입력한/기존 상태의 segmentMembership이 있음을 의미합니다.

`inAudience('audienceName') == false` 은(는) 종료한 상태의 segmentMembership이 있음을 의미합니다.

## 카테고리

Adobe Experience Platform

## 함수 구문

`inAudience(<parameter>)`

## 매개 변수

| 매개변수 | 설명 | 유형 |
|--- |--- |--- |
| Audience | 대상자 이름 | `<string>` |

## 서명 및 반환된 유형

`inAudience(<string>)`

부울 반환.

## 예

`inAudience("men over 50")`

설명:

함수는 를 반환합니다 **[!UICONTROL true]** 여정 인스턴스 내의 개인이 &quot;50세 이상의 남성&quot;이라는 Adobe Experience Platform 대상의 일부인 경우 **[!UICONTROL false]** 그렇지 않으면.
