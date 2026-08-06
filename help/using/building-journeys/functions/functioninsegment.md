---
product: journey optimizer
title: inSegment
description: inSegment 함수에 대해 알아보기
feature: Journeys
role: Developer
level: Experienced
keywords: inSegment, 함수, 표현식, 여정
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
version: Journey Orchestration
feature_v2: []
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 521
ht-degree: 2%

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

대상자 참여 상태가 **실현됨**&#x200B;인 개인만 대상자의 구성원으로 간주됩니다. 대상자를 평가하는 방법에 대한 자세한 내용은 [세그먼테이션 서비스 설명서](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results)를 참조하세요.

`inSegment('segmentName') == true`은(는) 입력한/기존 상태의 segmentMembership이 있음을 의미합니다.

`inSegment('segmentName') == false`은(는) 종료한 상태의 segmentMembership이 있음을 의미합니다.

## 카테고리

Adobe Experience Platform

## 함수 구문

`inSegment(<parameter>)`

## 매개변수

| 매개 변수 | 설명 | 유형 |
|--- |--- |--- |
| 세그먼트 | 대상자 이름 | `<string>` |

## 서명 및 반환된 유형

`inSegment(<string>)`

부울 반환.

## 예

`inSegment("men over 50")`

설명:

이 함수는 여정 인스턴스 내의 개인이 &quot;50세 이상의 남성&quot;이라는 Adobe Experience Platform 대상의 일부인 경우 **[!UICONTROL true]**&#x200B;을 반환하고, 그렇지 않은 경우 **[!UICONTROL false]**&#x200B;을 반환합니다.

+++ AI 기술 자료 참조

이 단원에는 이 주제와 관련된 해석, 검색 및 질문 답변을 지원하기 위한 구조화된 지식이 포함되어 있습니다.

이해를 돕기 위해 이 정보를 이 페이지의 설명서와 통합해야 합니다. 두 소스 모두 독립적으로 사용하기 위한 것은 아닙니다. 이 페이지에서는 기능에 대해 설명하지만, 용어, 의도, 적용 가능성 및 제약 조건을 명확히 하는 데 도움이 되는 추가 컨텍스트를 제공합니다.

* **TL;DR:** 이 페이지에서는 여정 프로필이 명명된 Adobe Experience Platform 대상에 속하는지 확인하고 부울을 반환하는 기존 `inSegment` 함수를 문서화합니다.

**의도:**
* `inSegment`을(를) 사용하여 프로필이 명명된 대상의 활성 구성원인지 확인
* `inSegment('name') == true`을(를) 사용하여 여정 조건에서 실현된(활성) 대상 멤버십을 확인하십시오
* `inSegment('name') == false`을(를) 사용하여 종료한(비활성) 대상 멤버십을 확인합니다.

**용어집:**
* **실현됨**: 개체가 현재 세그먼트 정의 *(제품별)에 적격함을 의미하는 대상 기여도 상태*
* **종료됨**: 엔터티가 종료되거나 세그먼트 정의 *(제품별)을(를) 남겼음을 의미하는 대상자 참여 상태*

**보호 기능:**
* 단일 여정에서 최대 100개의 대상자를 검색할 수 있습니다
* 대상 이름은 문자열 상수여야 합니다. 필드 참조 및 표현식은 매개 변수로 지원되지 않습니다.

**용어:**
* 정식 이름: inSegment — 약어: none — 변형: inAudience(현재 기본 함수)
* 동의어: &quot;inSegment&quot; = &quot;audience membership check&quot; (기존)
* 혼동하지 마십시오. &quot;inSegment&quot;(기존/더 이상 사용되지 않는 함수)≠ &quot;inAudience&quot;(현재 권장되는 함수)
* 혼동하지 않음: &quot;인식됨&quot;(활성 멤버) ≠ &quot;종료됨&quot;(더 이상 멤버 아님)

**FAQ:**
* **Q: `inSegment`과(와) `inAudience`의 차이점은 무엇입니까?** — `inSegment`은(는) 레거시 함수 이름이고 `inAudience`은(는) 현재 권장되는 함수입니다. 둘 다 대상자 멤버십을 확인하지만 `inAudience`에는 보호 기능 및 전파 시간 세부 정보를 포함한 더 완벽한 설명서가 있습니다.
* **Q: `inSegment('name') == true`은(는) 무엇을 의미합니까?** — 프로필에 &quot;실현된&quot; 세그먼트 멤버십 상태가 있음을 의미합니다. 즉, 개인은 대상의 활성 멤버입니다.
* **Q: 동적 식을 대상 이름으로 전달할 수 있습니까?** — 아니요. 대상 이름은 문자열 상수여야 합니다. 필드 참조 및 표현식은 지원되지 않습니다.
* **Q: 한 여정에 몇 명의 대상을 평가할 수 있습니까?** — 단일 여정 내에서 최대 100개의 대상을 검색할 수 있습니다.

+++
