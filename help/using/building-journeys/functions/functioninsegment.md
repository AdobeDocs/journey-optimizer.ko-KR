---
product: journey optimizer
title: inSegment
description: inSegment 함수에 대해 알아보기
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inSegment, 함수, 표현식, 여정
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
source-git-commit: 85a8d0713f87a8b3505a2294402156ba6598c8bb
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 6%

---

# inSegment {#inSegment}

개인이 주어진 대상자에 속하는지 확인합니다.

>[!NOTE]
>
>최대 100개의 대상을 검색할 수 있습니다.

대상 이름은 문자열 상수여야 합니다. 필드 참조나 식이 될 수 없습니다.

대상은 [Adobe Experience Platform](https://platform.adobe.com/audience/overview)에 정의되어 있습니다. 표현식 편집기는 자동으로 완성된 대상자 목록을 제공합니다.

대상자는 다음 두 가지 상태를 가질 수 있습니다.

* 실현됨: 엔티티가 세그먼트 정의에 적합합니다.
* 종료됨: 엔티티가 세그먼트 정의를 종료하는 중입니다.

대상자 참여 상태가 **실현됨**&#x200B;인 개인만 대상자의 구성원으로 간주됩니다. 대상자를 평가하는 방법에 대한 자세한 내용은 [세그먼테이션 서비스 설명서](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=ko#interpret-segment-results)를 참조하세요.

`IF inSegment('segmentName') == true`은(는) 입력한/기존 상태의 segmentMembership이 있음을 의미합니다.

`ELSE inSegment('segmentName') == false`은(는) 종료한 상태의 segmentMembership이 있음을 의미합니다.

## 카테고리

Adobe Experience Platform

## 함수 구문

`inSegment(<parameter>)`

## 매개 변수

| 매개변수 | 설명 | 유형 |
|--- |--- |--- |
| 세그먼트 | 대상자 이름 | `<string>` |

## 서명 및 반환된 유형

`inSegment(<string>)`

부울 반환.

## 예

`inSegment("men over 50")`

설명:

함수는 여정 인스턴스 내의 개인이 &quot;50세 이상의 남성&quot;이라는 Adobe Experience Platform 대상의 일부인 경우 **[!UICONTROL true]**&#x200B;을 반환하고, 그렇지 않은 경우 **[!UICONTROL false]**&#x200B;을 반환합니다.
