---
product: journey optimizer
title: inSegment
description: inSegment 함수에 대해 알아보기
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inSegment, 함수, 표현식, 여정
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
source-git-commit: 59499dec7d15dd4565c7910d7b454d82243ff011
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 6%

---

# inSegment {#inSegment}

개인이 주어진 세그먼트에 속하는지 확인합니다.

>[!NOTE]
>
>최대 100개의 세그먼트를 검색할 수 있습니다.

세그먼트 이름은 문자열 상수여야 합니다. 필드 참조나 식이 될 수 없습니다.

세그먼트는에 정의됩니다. [Adobe Experience Platform](https://platform.adobe.com/segment/overview). 표현식 편집기는 자동으로 완성된 세그먼트 목록을 제공합니다.

세그먼트는 세 가지 상태를 가질 수 있습니다.

* 기존: 엔티티가 계속 세그먼트에 있습니다.
* 인식됨: 엔티티가 세그먼트를 입력 중입니다.
* 종료됨: 엔티티가 세그먼트를 종료 중입니다.

다음을 보유한 개인만 **실현됨** 및 **기존 항목** 세그먼트 기여도 상태는 세그먼트의 멤버로 간주됩니다. 세그먼트를 평가하는 방법에 대한 자세한 내용은 [세그먼테이션 서비스 설명서](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results).

`IF inSegment('segmentName') == true` 은(는) 입력한/기존 상태의 segmentMembership이 있음을 의미합니다.

`ELSE inSegment('segmentName') == false` 은(는) 종료한 상태의 segmentMembership이 있음을 의미합니다.

## 카테고리

Adobe Experience Platform

## 함수 구문

`inSegment(<parameter>)`

## 매개 변수

| 매개변수 | 설명 | 유형 |
|--- |--- |--- |
| 세그먼트 | 세그먼트 이름 | `<string>` |

## 서명 및 반환된 유형

`inSegment(<string>)`

부울 반환.

## 예

`inSegment("men over 50")`

설명:

함수는 를 반환합니다 **[!UICONTROL true]** 여정 인스턴스 내의 개인이 &quot;50세 이상 남성&quot;이라는 Adobe Experience Platform 세그먼트에 속하는 경우 **[!UICONTROL false]** 그렇지 않으면.
