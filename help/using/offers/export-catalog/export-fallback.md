---
title: 대체 오퍼 데이터 세트
description: 이 섹션에는 대체 오퍼에 대해 내보낸 데이터 세트에 사용된 모든 필드가 나열됩니다
feature: Offers, Datasets
topic: Integrations
role: User
level: Intermediate
exl-id: 73bfdc24-28cf-4cfd-bac9-a4ff1ea543e3
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: tm+mt
source-wordcount: '1056'
ht-degree: 3%

---

# 대체 오퍼 데이터 세트 {#fallback-dataset}

오퍼가 수정될 때마다 대체 오퍼에 대해 자동 생성된 데이터 세트가 업데이트됩니다.

![](../assets/dataset-fallback.png)

데이터 세트에서 가장 최근에 성공한 일괄 처리가 오른쪽에 표시됩니다. 데이터 세트에 대한 스키마의 계층 구조 보기가 왼쪽 창에 표시됩니다.

>[!NOTE]
>
>에서 오퍼 라이브러리의 각 개체에 대해 내보낸 데이터 세트에 액세스하는 방법에 대해 알아봅니다 [이 섹션](../export-catalog/access-dataset.md).

다음은에서 사용할 수 있는 모든 필드 목록입니다. **[!UICONTROL 의사 결정 개체 저장소 - 대체 오퍼]** 데이터 세트.

+++ 식별자

**필드:** _id
**제목:** 식별자
**설명:** 레코드에 대한 고유 식별자.
**유형:** 문자열

+++

+++ _경험

**필드:** 경험(_E)
**유형:** 오브젝트

+++

+++ 경험 > 의사 결정(_e)

**필드:** 의사 결정
**유형:** 오브젝트

+++

+++ _experience > 의사 결정 > 특성

**필드:** 특성
**제목:** 의사 결정 옵션 특성
**설명:** 이 특정 결정 옵션에 속하는 추가 속성 또는 속성입니다. 인스턴스마다 특성(맵의 키)이 다를 수 있습니다. 특징은 하나의 결정 옵션을 다른 결정 옵션과 구별하기 위해 사용되는 이름 값 쌍이다. 특성은 이 결정 옵션을 나타내는 콘텐츠의 값 및 옵션의 성능을 분석하고 최적화하는 기능으로 사용됩니다. 모든 인스턴스에 동일한 속성 또는 속성이 있는 경우 해당 측면을 의사 결정 옵션 세부 사항에서 파생되는 확장 스키마로 모델링해야 합니다.
**유형:** 오브젝트

+++

<!--Field under Characteristics without title = additionalProperties? Desc = Value of the property. Type: string-->

+++ _experience > 의사 결정 > 컨텐츠

**필드:** 목차
**제목:** 콘텐츠 세부 사항
**설명:** 다른 컨텍스트에서 결정 항목을 렌더링할 콘텐츠 항목입니다. 단일 결정 옵션에는 여러 콘텐츠 변형이 있을 수 있습니다. 콘텐츠는 (디지털) 경험의 소비를 위해 대상자에게 안내되는 정보입니다. 콘텐츠는 채널을 통해 특정 배치로 전달됩니다.
**유형:** 배열

+++

+++_경험 > 의사 결정 > 콘텐츠 > 구성 요소

**필드:** 구성 요소
**설명:** 모든 언어 변형을 포함하여 의사 결정 옵션을 나타내는 콘텐츠의 구성 요소입니다. 특정 구성 요소는 &quot;dx:format&quot;, &quot;dc:subject&quot; 및 &quot;dc:language&quot; 또는 이들의 조합으로 제공됩니다. 이 메타데이터는 오퍼와 연결된 콘텐츠를 찾거나 나타내고 배치 계약에 따라 통합하는 데 사용됩니다.
**유형:** 배열
**필수 여부:** &quot;_type&quot;, &quot;_dc&quot; <!--TBC?-->

* **_experience > 의사 결정 > 컨텐츠 > 구성 요소 > 컨텐츠 구성 요소 유형**

  **필드:** 유형(_t)
  **제목:** 콘텐츠 구성 요소 유형
  **설명:** 각 값이 콘텐츠 구성 요소에 지정된 유형에 매핑되는 열거형 URI 세트입니다. 콘텐츠 표현의 일부 소비자는 @type 값이 콘텐츠 구성 요소의 추가 속성을 설명하는 스키마에 대한 참조가 될 것으로 예상합니다.
  **유형:** 문자열

* **_experience > 의사 결정 > 콘텐츠 > 구성 요소 > _dc**

  **필드:** _dc
  **유형:** 오브젝트
  **필수 여부:** &quot;format&quot;

   * **형식**

     **필드:** 형식
     **제목:** 형식
     **설명:** 리소스의 물리적 또는 디지털 표현입니다. 일반적으로 형식에는 리소스의 미디어 유형이 포함되어야 합니다. 포맷을 사용하여 리소스를 표시하거나 운영하는 데 필요한 소프트웨어, 하드웨어 또는 기타 장비를 결정할 수 있습니다. 권장 모범 사례는 통제 어휘(예: 목록)에서 값을 선택하는 것입니다. [인터넷 미디어 유형](컴퓨터 미디어 형식을 정의하는 https://www.iana.org/ assignments/media-types/).
     **유형:** 문자열
     **예:** &quot;application/vnd.adobe.photoshop&quot;

   * **언어**

     **필드:** 언어
     **제목:** 언어
     **설명:** 리소스의 언어입니다. \n언어는 다음에 정의된 대로 언어 코드에 지정됩니다. [IETF RFC 3066](https://www.ietf.org/rfc/rfc3066.txt): XDM의 다른 곳에서 사용되는 BCP 47의 일부입니다.
     **유형:** 배열
     **예:** &quot;\n&quot;, &quot;pt-BR&quot;, &quot;es-ES&quot;

* **_experience > 의사 결정 > 콘텐츠 > 구성 요소 > _repo**

  **필드:** _repo
  **유형:** 오브젝트

   * **ID**

     **필드:** id
     **설명:** 콘텐츠 저장소의 에셋을 참조하는 선택적 고유 식별자입니다. Platform API를 사용하여 표현을 검색하는 경우 클라이언트는 추가 속성 \&quot;repo:resolveUrl\&quot;을 사용하여 에셋을 검색할 수 있습니다.
     **유형:** 문자열
     **예:** &quot;urn:aaid:sc:US:6dc33479-13ca-4b19-b25d-c805eff8a69e&quot;

   * **이름**

     **필드:** 이름
     **설명:** \&quot;repo:id\&quot;로 외부 에셋을 저장하는 저장소를 찾을 위치에 대한 힌트입니다.
     **유형:** 문자열

   * **저장소 ID**

     **필드:** 저장소 ID
     **설명:** 콘텐츠 저장소의 에셋을 참조하는 선택적 고유 식별자입니다. Platform API를 사용하여 표현을 검색하는 경우 클라이언트는 추가 속성 \&quot;repo:resolveUrl\&quot;을 사용하여 에셋을 검색할 수 있습니다.
     **유형:** 문자열
     **예:** &quot;C87932A55B06F7070A49412D@AdobeOrg&quot;

   * **resolveURL**

     **필드:** resolveURL
     **설명:** 콘텐츠 저장소의 에셋을 읽을 수 있는 선택적 고유 리소스 로케이터입니다. 이렇게 하면 클라이언트가 에셋의 관리 위치와 호출할 API를 이해하지 않고도 에셋을 보다 쉽게 가져올 수 있습니다. 이는 HAL 링크와 유사하지만 의미는 더 간단하고 목적성이 강하다.
     **유형:** 문자열
     **예:** &quot;https://plaftform.adobe.io/resolveByPath?path=&quot;/mycorp/content/projectx/fragment/prod/herobanners/banner14.html3&quot;&quot;

* **_experience > 의사 결정 > 컨텐츠 > 구성 요소 > 컨텐츠**

  **필드:** 콘텐츠
  **설명:** 컨텐츠를 직접 보관할 선택적 필드입니다. 에셋 저장소의 콘텐츠를 참조하는 대신 구성 요소에 간단한 콘텐츠를 직접 저장할 수 있습니다. 이 필드는 복합, 복합 및 바이너리 콘텐츠 자산에는 사용되지 않습니다.
  **유형:** 문자열

* **_experience > 의사 결정 > 컨텐츠 > 구성 요소 > deliveryURL**

  **필드:** deliveryURL
  **설명:** 컨텐츠 전달 네트워크 또는 서비스 끝점에서 자산을 가져오는 선택적 고유 리소스 로케이터입니다. 이 URL은 사용자 에이전트가 공개적으로 에셋에 액세스하는 데 사용됩니다.
  **유형:** 문자열
  **예:** &quot;https://cdn.adobe.io/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

* **_experience > 의사 결정 > 컨텐츠 > 구성 요소 > linkURL**

  **필드:** linkURL
  **설명:** 사용자 상호 작용을 위한 선택적 고유 리소스 로케이터입니다. 이 URL은 사용자 에이전트에서 최종 사용자를에 연결하는 데 사용되며 추적할 수 있습니다.
  **유형:** 문자열
  **예:** &quot;https://cdn.adobe.io/tracker?code=23432&amp;redirect=/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

+++

+++ _experience > 의사 결정 > 컨텐츠 > 배치

**필드:** 배치
**제목:** 배치
**설명:** 준수할 배치. 값은 참조되는 오퍼 배치의 URI(@id)입니다. 스키마 https://ns.adobe.com/experience/decisioning/placement 를 참조하십시오.
**유형:** 문자열

+++

+++ 경험 > 의사 결정 > 라이프사이클 상태(_E)

**필드:** lifecycleStatus
**제목:** 라이프사이클 상태
**설명:** 라이프사이클 상태를 사용하면 객체를 사용하여 워크플로우를 수행할 수 있습니다. 상태는 객체가 보이거나 관련성이 있는 것으로 간주되는 위치에 영향을 줄 수 있습니다. 상태 변경은 개체를 사용하는 클라이언트나 서비스에 의해 결정됩니다.
**유형:** 문자열
**가능한 값:** &quot;초안&quot;(기본값), &quot;승인됨&quot;, &quot;라이브&quot;, &quot;완료됨&quot;, &quot;보관됨&quot;

+++

+++ _experience > 의사 결정 > 의사 결정 옵션 이름

**필드:** 이름
**제목:** 결정 옵션 이름
**설명:** 다양한 사용자 인터페이스에 표시되는 옵션 이름입니다.
**유형:** 문자열

+++

+++ _experience > 의사 결정 > 태그

**필드:** 태그
**제목:** 태그
**설명:** 이 엔터티와 연결된 컬렉션 한정자 집합(이전에는 &quot;태그&quot;라고 함)입니다. 컬렉션 한정자는 전체 인벤토리를 하위 집합(범주)으로 제한하는 필터 표현식에 사용됩니다.
**유형:** 배열

+++

<!--Field without name under collection qualifiers: Description: An identifier of a collection qualifier object. The value is the @id of the collection qualifier that is referenced. See tag schema: https://ns.adobe.com/experience/decisioning/tag. Type: string-->

+++ _repo

**필드:** _repo
**유형:** 오브젝트

+++

+++ _repo > 의사 결정 옵션 ETag

**필드:** etag
**제목:** 의사 결정 옵션 ETag
**설명:** 스냅샷 생성 시 결정 옵션 객체의 개정 버전.
**유형:** 문자열

+++
