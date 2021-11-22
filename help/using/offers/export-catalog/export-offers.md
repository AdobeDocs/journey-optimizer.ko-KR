---
title: 개인화된 오퍼 데이터 세트
description: 이 섹션에는 오퍼용으로 내보낸 데이터 세트에 사용되는 모든 필드가 나열됩니다.
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: c7f691aa-8f89-4f23-b897-53211863eb6d
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '2003'
ht-degree: 3%

---

# 개인화된 오퍼 데이터 세트 {#offers-dataset}

오퍼가 수정될 때마다 개인화된 컨텐츠 오퍼에 대해 자동 생성된 데이터 세트가 업데이트됩니다.

![](../../assets/dataset-offers.png)

데이터 집합에 있는 가장 최근 성공한 일괄 처리가 오른쪽에 표시됩니다. 데이터 집합에 대한 스키마의 계층 구조 보기가 왼쪽 창에 표시됩니다.

>[!NOTE]
>
>에서 오퍼 라이브러리의 각 개체에 대해 내보낸 데이터 세트에 액세스하는 방법을 알아봅니다 [이 섹션](../export-catalog/access-dataset.md).

다음은 에서 사용할 수 있는 모든 필드 목록입니다 **[!UICONTROL Decision Object Repository - Personalized Offers]** 데이터 세트.

<!--Personalized offers form the set of choices for a decision. The objective for decisioning is to take a large inventory of items and apply numerous constraint rules to that inventory to narrow it down and then to rank the qualifying options according to a criteria. The resulting propositions assemble and personalize the experience for specific individuals.-->

## 식별자

**필드:** _id
**제목:** 식별자
**설명:** 레코드의 고유 식별자입니다.
**유형:** 문자열

## _경험

**필드:** _experience
**유형:** 개체

### _experience > decisioning

**필드:** 의사 결정
**유형:** 개체

#### _experience > decisioning > calendarConstraints

**필드:** calendarConstraints
**제목:** 달력 제한 세부 정보
**설명:** 달력 제한은 날짜 범위가 지정된 결정 옵션이 유효한지 여부를 결정합니다. 해당 날짜 범위를 벗어나면 옵션을 제안할 수 없습니다.
**유형:** 개체

* **종료 날짜 및 시간**

   **필드:** endDate
   **제목:** 종료 날짜 및 시간
   **설명:** 결정 옵션 유효성의 종료 일자. 종료 날짜가 지난 옵션은 더 이상 의사 결정 프로세스에서 제안할 수 없습니다.
   **유형:** 문자열

* **시작 날짜 및 시간**

   **필드:** startDate
   **제목:** 시작 날짜 및 시간
   **설명:** 결정 옵션 유효성의 시작 날짜입니다. 시작 날짜에 도달하지 않은 옵션은 의사 결정 프로세스에서 아직 제안할 수 없습니다.
   **유형:** 문자열

#### _experience > decisioning > 특성

**필드:** 특성
**제목:** 결정 옵션 특성
**설명:** 이 특정 결정 옵션에 속하는 추가 속성 또는 속성입니다. 인스턴스마다 특성(맵에 있는 키)이 다를 수 있습니다. 특징은 하나의 결정 옵션을 다른 결정 옵션과 구분하는 데 사용되는 이름 값 쌍입니다. 특징은 이 결정 옵션을 나타내는 컨텐츠와 옵션 성능을 분석 및 최적화하는 기능으로 사용됩니다. 모든 인스턴스에 동일한 속성 또는 속성이 있는 경우 해당 측면을 결정 옵션 세부 정보에서 파생되는 확장 스키마로 모델링해야 합니다.
**유형:** 개체

#### _experience > decisioning > 콘텐츠

**필드:** 내용
**제목:** 컨텐츠 세부 사항
**설명:** 다른 컨텍스트에서 의사 결정 항목을 렌더링할 콘텐츠 항목입니다. 단일 결정 옵션에는 여러 콘텐츠 변형이 있을 수 있습니다. 콘텐츠는 (디지털) 경험에서 사용할 대상을 향해 오는 정보입니다. 컨텐츠는 채널을 통해 특정 배치로 전달됩니다.
**유형:** 배열

**_experience > decisioning > content > components**

**필드:** 구성 요소
**설명:** 모든 언어 변형을 포함하여 결정 옵션을 나타내는 컨텐츠의 구성 요소입니다. 특정 구성 요소는 &#39;dx:format&#39;, &#39;dc:subject&#39; 및 &#39;dc:language&#39; 또는 이들의 조합으로 찾을 수 있습니다. 이 메타데이터는 오퍼와 연관된 컨텐츠를 찾거나 나타내고 배치 계약에 따라 통합하는 데 사용됩니다.
**유형:** 배열
**필수 여부:** &quot;_type&quot;, &quot;_dc&quot; <!--TBC?-->

* **_experience > decisioning > contents > components > Content Component Type**

   **필드:** _type
   **제목:** 컨텐츠 구성 요소 유형
   **설명:** 각 값이 컨텐츠 구성 요소에 지정된 유형에 매핑되는 열거된 URI 세트입니다. 컨텐츠 표현의 일부 소비자는 @type 값이 컨텐츠 구성 요소의 추가 속성을 설명하는 스키마를 참조할 것으로 기대하고 있습니다.
   **유형:** 문자열

* **_experience > decisioning > contents > components > _dc**

   **필드:** _dc
   **유형:** 개체
   **필수 여부:** &quot;format&quot;

   * **포맷**

      **필드:** 포맷
      **제목:** 형식
      **설명:** 리소스의 실제 또는 디지털 표시. 일반적으로 형식에는 리소스의 미디어 유형이 포함되어야 합니다. 리소스를 표시하거나 운영하는 데 필요한 소프트웨어, 하드웨어 또는 기타 장비를 결정하는 데 형식을 사용할 수 있습니다. 권장되는 우수 사례는 통제 어휘에서 값을 선택하는 것입니다(예: [인터넷 미디어 유형](http://www.iana.org/assignments/media-types/) 컴퓨터 미디어 형식 정의).
      **유형:** 문자열
      **예:** &quot;application/vnd.adobe.photoshop&quot;

   * **언어**
      **필드:** 언어
      **제목:** 언어
      **설명:** 리소스의 언어 또는 언어입니다. \n언어는 [IETF RFC 3066](https://www.ietf.org/rfc/rfc3066.txt)는 XDM의 다른 곳에서 사용되는 BCP 47의 일부입니다.
      **유형:** 배열
      **예:** &quot;\n&quot;, &quot;pt-BR&quot;, &quot;es-ES&quot;

* **_experience > decisioning > content > components > _repo**

   **필드:** _repo
   **유형:** 개체

   * **ID**

      **필드:** id
      **설명:** 컨텐츠 저장소에서 자산을 참조하는 선택적 고유 식별자입니다. Platform API를 사용하여 표현을 검색할 때 클라이언트는 추가 속성 \&quot;repo:resolveUrl\&quot;이 자산을 검색할 수 있습니다.
      **유형:** 문자열
      **예:** &quot;urn&quot;:aaid:sc:US:6dc33479-13ca-4b19-b25d-c805eff8a69e&quot;

   * **이름**

      **필드:** 이름
      **설명:** 일부 힌트는 외부 자산을 \&quot;repo:id\&quot;로 저장하는 저장소를 찾을 위치에 대한 힌트입니다.
      **유형:** 문자열

   * **repositoryID**

      **필드:** repositoryID
      **설명:** 컨텐츠 저장소에서 자산을 참조하는 선택적 고유 식별자입니다. Platform API를 사용하여 표현을 검색할 때 클라이언트는 추가 속성 \&quot;repo:resolveUrl\&quot;이 자산을 검색할 수 있습니다.
      **유형:** 문자열
      **예:** &quot;C87932A55B06F7070A49412D@AdobeOrg&quot;

   * **resolveURL**

      **필드:** resolveURL
      **설명:** 컨텐츠 저장소에서 자산을 읽을 수 있는 선택적 고유 리소스 로케이터입니다. 이렇게 하면 클라이언트가 자산이 관리되는 위치와 호출할 API를 이해하지 않고 자산을 쉽게 가져올 수 있습니다. 이것은 HAL 링크와 유사하지만, 의미론적 의미가 더 간단하고 더 목적적이다.
      **유형:** 문자열
      **예:** &quot;https://plaftform.adobe.io/resolveByPath?path=&quot;/mycorp/content/projectx/fragment/prod/herobanners/banner14.html3&quot;

* **_experience > decisioning > content > components > content**

   **필드:** 콘텐츠
   **설명:** 컨텐츠를 직접 저장할 선택 필드입니다. 구성 요소는 자산 저장소에서 컨텐츠를 참조하는 대신 간단한 콘텐츠를 직접 보유할 수 있습니다. 이 필드는 복합, 복합 및 이진 컨텐츠 자산에 사용되지 않습니다.
   **유형:** 문자열

* **_experience > decisioning > contents > components > deliveryURL**

   **필드:** deliveryURL
   **설명:** 콘텐츠 게재 네트워크 또는 서비스 끝점에서 자산을 가져오는 선택적 고유 리소스 로케이터입니다. 이 URL은 사용자 에이전트가 공개적으로 자산에 액세스하는 데 사용됩니다.
   **유형:** 문자열
   **예:** &quot;https://cdn.adobe.io/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

* **_experience > decisioning > contents > components > linkURL**

   **필드:** linkURL
   **설명:** 사용자 상호 작용을 위한 선택적 고유 리소스 로케이터입니다. 이 URL은 사용자 에이전트에서 최종 사용자를 참조하는 데 사용되며 추적할 수 있습니다.
   **유형:** 문자열
   **예:** &quot;https://cdn.adobe.io/tracker?code=23432&amp;redirect=/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

**_experience > decisioning > 콘텐츠 > 배치**

**필드:** 배치
**제목:** 배치
**설명:** 준수하기 위한 배치. 값은 참조되는 오퍼 배치의 URI(@id)입니다. 스키마 https://ns.adobe.com/experience/decisioning/placement 를 참조하십시오.
**유형:** 문자열

#### _experience > decisioning > 라이프사이클 상태

**필드:** lifecycleStatus
**제목:** 라이프사이클 상태
**설명:** 라이프사이클 상태를 사용하면 개체를 사용하여 워크플로우를 수행할 수 있습니다. 상태는 객체가 표시되거나 관련 있는 것으로 간주되는 위치에 영향을 줄 수 있습니다. 상태 변경은 개체를 사용하는 클라이언트나 서비스에 의해 결정됩니다.
**유형:** string
**가능한 값:** &quot;초안&quot;(기본값), &quot;승인됨&quot;, &quot;라이브&quot;, &quot;완료됨&quot;, &quot;보관됨&quot;

#### _experience > decisioning > 결정 옵션 이름

**필드:** 이름
**제목:** 결정 옵션 이름
**설명:** 다양한 사용자 인터페이스에 표시되는 옵션 이름입니다.
**유형:** 문자열

#### _experience > decisioning > profileConstraints

**필드:** profileConstraints
**제목:** 프로필 제한 세부 정보
**설명:** 프로필 제약 조건은 현재 이 컨텍스트에서 이 프로필 ID에 대한 옵션을 사용할 수 있는지 여부를 결정합니다. 프로필 제약 조건이 각 옵션의 값을 고려할 필요가 없는 경우(예: 옵션 선택에서 옵션 중 불변인 경우 &#39;false&#39;로 평가되는 프로필 제약 조건은 전체 옵션 선택을 취소합니다.) 반면, 옵션을 매개 변수로 사용하는 프로필 제한 규칙은 옵션 선택의 각 자격 옵션에 대해 평가됩니다.
**유형:** 개체

**_experience > decisioning > profileConstraints > 설명**

**필드:** 설명
**제목:** 설명
**설명:** 프로필 제한 설명입니다. 이 프로필 제한을 구성하는 방법 또는 이유 및/또는 이 프로필에 의해 포함 또는 제외할 옵션에 대한 사람이 읽을 수 있는 의도를 전달하는 데 사용됩니다.
**유형:** 문자열

**_experience > decisioning > profileConstraints > 자격 규칙**

**필드:** requalificationRule
**제목:** 자격 규칙
**설명:** 주어진 프로필 및/또는 지정된 컨텍스트 XDM 개체에 대해 true 또는 false로 평가되는 의사 결정 규칙에 대한 참조입니다. 이 규칙은 이 옵션이 지정된 프로필에 적합한지를 결정하는 데 사용됩니다. 값은 참조되는 의사 결정 규칙의 URI(@id)입니다. 스키마 https://ns.adobe.com/experience/decisioning/rule 를 참조하십시오.
**유형:** 문자열

**_experience > decisioning > profileConstraints > 프로필 제한 유형**

**필드:** profileConstraintType
**제목:** 프로필 제한 유형
**설명:** 현재 제약 조건이 설정되어 있는지 여부 및 제약 조건이 표현되는 방식을 결정합니다. 규칙 또는 하나 이상의 세그먼트 멤버십을 통해 수행될 수 있습니다.
**유형:** string
**가능한 값:**
* &quot;none&quot;(기본값)
* &quot;qualificationRule&quot;: &quot;프로필 제약 조건은 제약 조건이 허용되기 전에 true로 평가해야 하는 단일 규칙으로 표시됩니다.&quot;
* &quot;anySegments&quot;: &quot;프로필 제한은 하나 이상의 세그먼트로 표시되며, 제한 작업이 허용되기 전에 프로필은 하나 이상의 세그먼트의 구성원이어야 합니다.&quot;
* &quot;allSegments&quot;: &quot;프로필 제한은 하나 이상의 세그먼트로 표시되며, 제한 작업이 허용되기 전에 프로필은 모든 세그먼트의 구성원이어야 합니다.&quot;
* &quot;rules&quot;: &quot;프로파일 제약은 자격, 적용 가능성, 적합성 등의 다양한 규칙으로 표시되며 제한적 조치를 허용하기 전에 모두 true로 평가해야 합니다.&quot;

**_experience > decisioning > profileConstraints > 세그먼트 식별자**

**필드:** segmentIdentities
**제목:** 세그먼트 식별자
**설명:** 세그먼트의 식별자
**유형:** 배열

* **식별자**

   **필드:** _id
   **제목:** 식별자
   **설명:** 관련 네임스페이스에서 세그먼트의 ID입니다.
   **유형:** 문자열

* **네임스페이스**

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

#### _experience > decisioning > 등급

**필드:** 등급
**제목:** 등급 세부 정보
**설명:** 등급(우선 순위). 결정 기준의 컨텍스트 시 \&quot;최상의 작업\&quot;로 간주되는 항목을 정의합니다. 자격 제약 조건을 충족하는 선택한 모든 옵션 중에서 순위 순서가 제안할 상위(또는 상위 N) 옵션을 결정합니다.
**유형:** 개체

**_experience > decisioning > 등급 > 주문 평가**

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

**_experience > decisioning > 등급 > 우선순위**

**필드:** 우선순위
**제목:** 우선순위
**설명:** 다른 모든 옵션에 상대적인 단일 결정 옵션의 우선 순위입니다. 순서 함수가 제공되지 않는 옵션은 이 속성을 사용하여 우선 순위가 지정됩니다. 우선 순위 값이 높은 옵션은 낮은 우선 순위 옵션보다 먼저 선택됩니다. 두 개 이상의 자격 옵션이 가장 높은 우선 순위 값을 공유하는 경우 하나의 옵션은 균일한 임의 상태로 선택되며 결정 제안에 사용됩니다.
**유형:** 정수
**최소값:** 0
**기본값:** 0

#### _experience > decisioning > 태그

**필드:** 태그
**제목:** 태그
**설명:** 이 엔터티에 연결된 태그 집합입니다. 태그는 전체 인벤토리를 하위 집합(카테고리)으로 제한하기 위해 필터 표현식에 사용됩니다.
**유형:** 배열

<!--Field without name under tags: Description: An identifier of a tag object. The value is the @id of the tag that is referenced. See tag schema: https://ns.adobe.com/experience/decisioning/tag. Type: string-->

## _repo

**필드:** _repo
**유형:** 개체

### _repo > 결정 옵션 태그

**필드:** 태그
**제목:** 결정 옵션 태그
**설명:** 스냅샷을 가져올 때 결정 옵션 객체가 있던 수정 버전입니다.
**유형:** 문자열
