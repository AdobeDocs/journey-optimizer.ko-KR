---
title: 오퍼 카탈로그 내보내기 시작
description: 이 섹션에는 결정을 위해 내보낸 데이터 세트에 사용되는 모든 필드가 나열됩니다
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 064762b7-9774-42eb-bcef-1d92bc94a988
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '1550'
ht-degree: 3%

---

# 의사 결정 데이터 세트 {#decisions-dataset}

오퍼가 수정될 때마다 결정을 위해 자동 생성된 데이터 세트(이전의 활동)가 업데이트됩니다.

![](../assets/dataset-activities.png)

데이터 집합에 있는 가장 최근 성공한 일괄 처리가 오른쪽에 표시됩니다. 데이터 집합에 대한 스키마의 계층 구조 보기가 왼쪽 창에 표시됩니다.

>[!NOTE]
>
>에서 오퍼 라이브러리의 각 개체에 대해 내보낸 데이터 세트에 액세스하는 방법을 알아봅니다 [이 섹션](../export-catalog/access-dataset.md).

다음은 에서 사용할 수 있는 모든 필드 목록입니다 **[!UICONTROL Decision Object Repository - Decisions]** 데이터 세트(이전에는 결정 객체 저장소 - 활동이라고 함)

<!--A decision (formerly known as offer decision) is used to control the decisioning process. It specifies the filter applied to the total inventory to narrow down offers by topic/category, the placement to narrow down the inventory to those offers that technically fit into the reserved space for the offer and specifies a fallback option should the combined constraints disqualify all available personalization offers.-->

## 식별자 {#identifier}

**필드:** _id
**제목:** 식별자
**설명:** 레코드의 고유 식별자입니다.
**유형:** 문자열

## _경험 {#experience}

**필드:** _experience
**유형:** 개체

### _experience > decisioning

**필드:** 의사 결정
**유형:** 개체

#### _experience > decisioning > 기준

**필드:** 기준
**제목:** 기준
**설명:** 각각에 제약 조건 세트가 포함된 결정 기준 세트를 정의합니다.
**유형:** 배열

**_experience > decisioning > 기준 > 설명**

**필드:** 설명
**제목:** 설명
**설명:** 기준 설명. 이 기준은 어떻게, 왜 이 기준이 만들어졌는지, 그리고 이것이 결정에 어떤 영향을 미치는지에 대한 사람이 읽을 수 있는 의도를 전달하는 데 사용됩니다.
**유형:** 문자열

**_experience > decisioning > 기준 > optionSelection**

**필드:** optionSelection
**제목:** 옵션 선택
**설명:** 옵션 선택 은 이 컨텍스트에서 옵션의 유효성/적용을 정의합니다.
**유형:** 개체

* **설명**

   **필드:** 설명
   **제목:** 설명
   **설명:** 옵션 선택 설명입니다. 이 옵션은 이 옵션 선택이 구성되는 방법 또는 이유 및/또는 어떤 옵션이 일치하는지에 대한 사람이 읽을 수 있는 의도를 전달하는 데 사용됩니다.
   **유형:** 문자열

* **옵션 필터**

   **필드:** 필터
   **제목:** 옵션 필터
   **설명:** 첨부된 태그를 사용하여 인벤토리의 옵션과 일치하는 태그 기반 필터에 대한 참조입니다. 값은 참조되는 의사 결정 규칙의 URI(@id)입니다. 스키마 https://ns.adobe.com/experience/decisioning/filter 를 참조하십시오.
   **유형:** 문자열

* **프로필 제한 유형**

   **필드:** optionSelectionType
   **제목:** 프로필 제한 유형
   **설명:** 현재 제약 조건이 설정되어 있는지 여부 및 제약 조건이 표현되는 방식을 결정합니다. 필터 쿼리 또는 하나 이상의 세그먼트 멤버십을 통해 수행될 수 있습니다.
   **유형:** 문자열
   **가능한 값:** &quot;none&quot;(기본값), &quot;directList&quot;, &quot;filter&quot;

* **옵션 목록**

   **필드:** 옵션
   **제목:** 옵션 목록
   **설명:** 필터 쿼리를 평가하지 않고 옵션을 직접 지정하는 목록입니다. 옵션 목록이나 옵션 필터 규칙을 지정할 수 있습니다.
   **유형:** 배열

   <!--Missing title under Option List? Desc = An identifier of an decision option entity. The value value refers to an `@id` property of a decision option. Type: string-->

**_experience > decisioning > 기준 > 배치**

**필드:** 배치
**제목:** 배치 제한
**설명:** 배치 제약조건에서는 이 기준이 나열된 배치에만 적용할 수 있다고 설명합니다. 타깃팅된 배치가 `xdm:placements` list는 고려되는 선택 사항입니다. 그렇지 않으면 전체 결정 기준을 건너뜁니다. xdm:placement&#39; 목록이 생략되거나 비어 있으면 타깃팅된 배치에 대해 기준이 고려됩니다. 여기에 나열된 배치는 옵션 선택에 대해 암시적 기준을 적용합니다. 고려할 옵션에는 타깃팅된 배치를 위한 표현이 있어야 합니다.
**유형:** 배열

* **배치 식별자**

   **제목:** 배치 식별자
   **설명:** 배치 엔티티에 대한 참조. 값은 참조되는 배치의 URI(@id)입니다. 스키마 https://ns.adobe.com/experience/decisioning/placement 를 참조하십시오.
   **유형:** 문자열

**_experience > decisioning > 기준 > profileConstraints**

**필드:** profileConstraints
**제목:** 프로필 제한
**설명:** 프로필 제약 조건은 이 컨텍스트에서 현재 이 프로필 ID에 대해 옵션 선택을 사용할 수 있는지 여부를 결정합니다. 프로필 제약 조건이 각 옵션의 값을 고려할 필요가 없는 경우(예: 옵션 선택에서 옵션 중 불변인 경우 &#39;false&#39;로 평가되는 프로필 제약 조건은 전체 옵션 선택을 취소합니다.) 반면, 옵션을 매개 변수로 사용하는 프로필 제한 규칙은 옵션 선택의 각 자격 옵션에 대해 평가됩니다.
**유형:** 개체

* **_experience > decisioning > 기준 > profileConstraints > 설명**

   **필드:** 설명
   **제목:** 설명
   **설명:** 프로필 제한 설명입니다. 이 프로필 제한을 구성하는 방법 또는 이유 및/또는 이 프로필에 의해 포함 또는 제외할 옵션에 대한 사람이 읽을 수 있는 의도를 전달하는 데 사용됩니다.
   **유형:** 문자열

* **_experience > decisioning > 기준 > profileConstraints > 자격 규칙**

   **필드:** requalificationRule
   **제목:** 자격 규칙
   **설명:** 주어진 프로필 및/또는 지정된 컨텍스트 XDM 개체에 대해 true 또는 false로 평가되는 의사 결정 규칙에 대한 참조입니다. 이 규칙은 이 옵션이 지정된 프로필에 적합한지를 결정하는 데 사용됩니다. 값은 참조되는 의사 결정 규칙의 URI(@id)입니다. 스키마 https://ns.adobe.com/experience/decisioning/rule 를 참조하십시오.
   **유형:** 문자열

* **_experience > decisioning > 기준 > profileConstraints > 프로필 제한 유형**

   **필드:** profileConstraintType
   **제목:** 프로필 제한 유형
   **설명:** 현재 제약 조건이 설정되어 있는지 여부 및 제약 조건이 표현되는 방식을 결정합니다. 규칙 또는 하나 이상의 세그먼트 멤버십을 통해 수행될 수 있습니다.
   **유형:** 문자열
   **가능한 값:**
   * &quot;none&quot;(기본값)
   * &quot;qualificationRule&quot;: &quot;프로필 제약 조건은 제약 조건이 허용되기 전에 true로 평가해야 하는 단일 규칙으로 표시됩니다.&quot;
   * &quot;anySegments&quot;: &quot;프로필 제한은 하나 이상의 세그먼트로 표시되며, 제한 작업이 허용되기 전에 프로필은 하나 이상의 세그먼트의 구성원이어야 합니다.&quot;
   * &quot;allSegments&quot;: &quot;프로필 제한은 하나 이상의 세그먼트로 표시되며, 제한 작업이 허용되기 전에 프로필은 모든 세그먼트의 구성원이어야 합니다.&quot;
   * &quot;rules&quot;: &quot;프로파일 제약은 자격, 적용 가능성, 적합성 등의 다양한 규칙으로 표시되며 제한적 조치를 허용하기 전에 모두 true로 평가해야 합니다.&quot;

* **_experience > decisioning > 기준 > profileConstraints > segmentIdentities**

   **필드:** segmentIdentities
   **제목:** 세그먼트 식별자
   **설명:** 세그먼트의 식별자입니다.
   **유형:** 배열

   * **식별자**

      **필드:** _id
      **제목:** 식별자
      **설명:** 관련 네임스페이스에서 세그먼트의 ID입니다.
      **유형:** 문자열

   * **namespace**

      **필드:** namespace
      **제목:** 네임스페이스
      **설명:** 와 연결된 네임스페이스 `xid` 속성을 사용합니다.
      **유형:** 개체
      **필수 여부:** &quot;code&quot;

      * **코드**

         **필드:** 코드
         **제목:** 코드
         **설명:** 이 코드는 네임스페이스에 대해 사람이 읽을 수 있는 식별자이며, ID 그래프 처리에 사용되는 기술 네임스페이스 ID를 요청하는 데 사용할 수 있습니다.
         **유형:** 문자열
   * **경험 식별자**

      **필드:** xid
      **제목:** 경험 식별자
      **설명:** 이 값은 모든 네임스페이스에서 모든 네임스페이스 범위 식별자에서 고유한 네임스페이스 간 식별자를 나타냅니다.
      **유형:** 문자열


**_experience > decisioning > 기준 > 등급**

**필드:** 등급
**제목:** 등급 세부 정보
**설명:** 등급(우선 순위). 결정 기준의 컨텍스트를 통해 \&quot;최상의 선택 사항\&quot;이 결정되는 방법을 정의합니다. 프로파일 제약 조건을 충족하는 선택한 모든 옵션 중에서, 등급에서 제안할 상위(또는 상위 N) 옵션을 결정합니다.
**유형:** 개체

* **_experience > decisioning > 기준 > 등급 > 순서**

   **필드:** 주문
   **제목:** 주문 평가
   **설명:** 하나 이상의 결정 옵션의 상대적 순서 평가. 서수 값이 낮은 옵션에는 더 높은 서수 값이 있는 옵션이 선택됩니다. 이 방법으로 결정된 값은 순서를 지정할 수 있지만 그 사이의 거리를 측정할 수 없으며 합계나 제품을 계산할 수도 없습니다. 중앙값 및 모드는 서수 데이터에 사용할 수 있는 유일한 중앙값 측정값입니다.
   **유형:** 개체

   * **점수 함수**

      **필드:** 함수
      **제목:** 점수 함수
      **설명:** 이 결정 옵션에 대한 숫자 점수를 계산하는 함수에 대한 참조입니다. 그런 다음 결정 옵션을 해당 점수로 순서 지정(등급)합니다. 이 속성의 값은 한 번에 옵션과 함께 호출할 함수의 URI(@id)입니다. 스키마 https://ns.adobe.com/experience/decisioning/function 를 참조하십시오.
      **유형:** 문자열

   * **주문 평가 유형**

      **필드:** orderEvaluationType
      **제목:** 주문 평가 유형
      **설명:** 사용할 주문 평가 메커니즘, 결정 옵션의 정적 우선순위, 모든 옵션에 대한 숫자 값을 계산하는 점수 함수 또는 목록을 수신하여 순서를 지정하는 등급 전략을 지정합니다.
      **유형:** 문자열
      **가능한 값:** &quot;static&quot;, &quot;scoringFunction&quot;, &quot;rankingStrategy&quot;

   * **등급 전략**

      **필드:** rankingStrategy
      **제목:** 등급 전략
      **설명:** 결정 옵션 목록의 등급을 매기는 전략에 대한 참조. 결정 옵션이 순서가 지정된 목록으로 반환됩니다. 이 속성의 값은 한 번에 옵션과 함께 호출할 함수의 URI(@id)입니다. 스키마 https://ns.adobe.com/experience/decisioning/rankingStrategy 를 참조하십시오.
      **유형:** 문자열

* **_experience > decisioning > 기준 > 등급 > 우선순위**

   **필드:** 우선순위
   **제목:** 우선순위
   **설명:** 다른 모든 옵션에 상대적인 단일 결정 옵션의 우선 순위입니다. 순서 함수가 제공되지 않는 옵션은 이 속성을 사용하여 우선 순위가 지정됩니다. 우선 순위 값이 높은 옵션은 낮은 우선 순위 옵션보다 먼저 선택됩니다. 두 개 이상의 자격 옵션이 가장 높은 우선 순위 값을 공유하는 경우 하나의 옵션은 균일한 임의 상태로 선택되며 결정 제안에 사용됩니다.
   **유형:** 정수
   **최소값:** 0
   **기본값:** 0

#### _experience > decisioning > 활동 종료 날짜 및 시간

**필드:** endTime
**제목:** 활동 종료 날짜 및 시간
**설명:** 결정(이전의 활동)의 종료 날짜 및 종료 시간입니다. 이 속성은 http://schema.org/Action에 정의된 schema.org의 &#39;endTime&#39; 속성의 의미 체계를 갖습니다.
**유형:** 문자열

#### _experience > decisioning > 대체 옵션

**필드:** 대체
**제목:** 대체 옵션
**설명:** 이 결정의 컨텍스트에서 의사 결정을 내릴 때 사용되는 폴백 옵션에 대한 참조는 일반 옵션 중 어느 것도 사용할 수 없습니다(일반적으로 하드 제한이 적용될 때 발생함). 값은 참조되는 대체 옵션의 URI(@id)입니다.
**유형:** 문자열

#### _experience > decisioning > 활동 이름

**필드:** 이름
**제목:** 활동 이름
**설명:** 다양한 사용자 인터페이스에 표시되는 의사 결정(이전의 활동)입니다.
**유형:** 문자열

#### _experience > decisioning > 활동 시작 날짜 및 시간

**필드:** startTime
**제목:** 활동 시작 날짜 및 시간
**설명:** 결정(이전의 활동)의 시작 날짜 및 종료 시간입니다. 이 속성은 http://schema.org/Action에 정의된 schema.org의 &#39;startTime&#39; 속성의 의미 체계를 갖습니다.
**유형:** 문자열

## _repo {#repo}

**필드:** _repo
**유형:** 개체

### _repo > 활동 ETag

**필드:** 태그
**제목:** 활동 태그
**설명:** 스냅샷을 가져올 때 결정(이전의 활동) 객체가 있었던 수정 버전입니다.
**유형:** 문자열
