---
title: 데이터 세트 가져오기
description: 이 섹션에는 폴백 오퍼에 대해 내보낸 데이터 세트에 사용된 모든 필드가 나열됩니다.
translation-type: tm+mt
source-git-commit: 70c172e19d5900c898d4850801468a2e186e682d
workflow-type: tm+mt
source-wordcount: '1003'
ht-degree: 3%

---

# 대체 오퍼가 데이터 세트 {#fallback-dataset}

오퍼가 수정될 때마다 대체 오퍼에 대해 자동으로 생성된 데이터 세트가 업데이트됩니다.

![](../../assets/dataset-fallback.png)

데이터 세트에서 가장 최근에 성공한 일괄 처리가 오른쪽에 표시됩니다. 데이터 세트에 대한 스키마의 계층 구조 보기가 왼쪽 창에 표시됩니다.

>[!NOTE]
>
>[이 섹션](../export-catalog/access-dataset.md)에서 오퍼 라이브러리의 각 개체에 대해 내보낸 데이터 집합에 액세스하는 방법을 알아봅니다.

다음은 **[!UICONTROL Decision Object Repository - Fallback Offers]** 데이터 세트에 사용할 수 있는 모든 필드의 목록입니다.

## 식별자

**필드:** _id 
**제목:** 식별자 
**설명:** 레코드에 대한 고유한 식별자입니다.
**유형:** 문자열

## _경험

**필드:** _경험 
**유형:** 객체

### 의사 결정

**필드:** 의사 결정 
**유형:** 객체

#### 특성

**필드:** 특성 
**제목:** 결정 옵션 
**특성 설명:** 이 특정 결정 옵션에 속하는 추가 속성 또는 특성입니다. 각 인스턴스는 맵에 있는 키 등 서로 다른 특성을 가질 수 있습니다. 특징은 하나의 결정 옵션을 다른 결정 옵션과 구분하는 데 사용되는 이름 값 쌍입니다. 특성은 이 결정 옵션을 나타내는 컨텐츠와 옵션의 성능을 분석 및 최적화하는 기능으로 사용됩니다. 모든 인스턴스에 동일한 속성이나 속성이 있으면 해당 종횡비를 결정 옵션 세부 사항에서 파생되는 확장 스키마로 모델링해야 합니다.
**유형:** 객체

<!--Field under Characteristics without title = additionalProperties? Desc = Value of the property. Type: string-->

#### 목차

**필드:** 컨텐츠 
**제목:** 컨텐츠 
**세부 사항 설명:** 다른 컨텍스트에서 의사 결정 항목을 렌더링할 컨텐츠 항목입니다. 단일 결정 옵션에는 여러 컨텐츠 변형이 있을 수 있습니다. 컨텐츠는 (디지털) 경험에서 소비하기 위해 고객을 대상으로 하는 정보입니다. 컨텐츠는 채널을 통해 특정 배치로 전달됩니다.
**유형:** 배열

* **구성 요소**

   **필드:** 구성 요소
   **설명:** 모든 언어 변형을 포함하여 결정 옵션을 나타내는 컨텐츠의 구성 요소입니다. &#39;dx:format&#39;, &#39;dc:subject&#39; 및 &#39;dc:language&#39; 또는 그 조합으로 특정 구성 요소를 찾을 수 있습니다. 이 메타데이터는 오퍼와 연관된 컨텐츠를 찾거나 표시하고 배치 계약에 따라 통합하는 데 사용됩니다.
   **유형:** 배열
   **필수:** &quot;_type&quot;, &quot;_dc&quot;  <!--TBC?-->

   * **컨텐츠 구성 요소 유형**

      **필드:** _type
      **제목:** 컨텐츠 구성 요소 유형
      **설명:** 각 값이 컨텐츠 구성 요소에 지정된 유형에 매핑되는 열거된 URI 세트입니다. 컨텐츠 표현의 일부 소비자는 @type 값이 컨텐츠 구성 요소의 추가 속성을 설명하는 스키마에 대한 참조일 것으로 예상하고 있습니다.
      **유형:** 문자열

   * **_dc**

      **필드:** _dc
      **유형:** 객체
      **필수:** &quot;형식&quot;

      * **형식**

         **필드:** 형식
         **제목:** 형식
         **설명:** 리소스의 실제 또는 디지털 표현입니다. 일반적으로 형식은 리소스의 미디어 유형을 포함해야 합니다. 이 포맷은 리소스를 표시 또는 운영하는 데 필요한 소프트웨어, 하드웨어 또는 기타 장비를 결정하는 데 사용할 수 있습니다. 제어된 단어(예: 컴퓨터 미디어 형식을 정의하는 [인터넷 미디어 유형](http://www.iana.org/ assignments/media-types/) 목록)에서 값을 선택하는 것이 좋습니다.
         **유형:** 문자열
         **예:** &quot;application/vnd.adobe.photoshop&quot;

      * **언어**

         **필드:** 언어
         **제목:** 언어
         **설명:** 리소스의 언어 또는 언어입니다. \n언어는 XDM의 다른 곳에서 사용되는 BCP 47의 일부인 [IETF RFC 3066](https://www.ietf.org/rfc/rfc3066.txt)에 정의된 언어 코드에 지정됩니다.
         **유형:** 배열
         **예:** &quot;\n&quot;, &quot;pt-BR&quot;, &quot;es-ES&quot;
   * **_repo**

      **필드:** _repo
      **유형:** 객체

      * **ID**

         **필드:** id
         **설명:** 컨텐츠 저장소의 자산을 참조하는 선택적 고유 식별자입니다. 플랫폼 API를 사용하여 표현을 검색할 때 클라이언트는 추가 속성 \&quot;repo:resolveUrl\&quot;을 사용하여 자산을 검색할 수 있습니다.
         **유형:** 문자열
         **예:** &quot;urn:aid:sc:US:6dc33479-13ca-4b19-b25d-c805eff8a69e&quot;

      * **이름**

         **필드:** 이름
         **설명:** 외부 자산을 \&quot;repo:id\&quot;로 저장하는 저장소를 찾을 위치에 대한 힌트입니다.
         **유형:** 문자열

      * **repositoryID**

         **필드:** repositoryID
         **설명:** 컨텐츠 저장소의 자산을 참조하는 선택적 고유 식별자입니다. 플랫폼 API를 사용하여 표현을 검색할 때 클라이언트는 추가 속성 \&quot;repo:resolveUrl\&quot;을 사용하여 자산을 검색할 수 있습니다.
         **유형:** 문자열
         **예:** &quot;C87932A55B06F7070A49412D@AdobeOrg&quot;

      * **resolveURL**

         **필드:** resolveURL
         **설명:** 컨텐츠 저장소에서 자산을 읽을 수 있는 선택적 고유 리소스 로케이터입니다. 이렇게 하면 클라이언트가 에셋이 관리되는 위치와 호출할 API를 이해하지 않아도 에셋을 보다 쉽게 얻을 수 있습니다. 이것은 HAL 링크와 비슷하지만 의미론적 의미는 더 간단하고 더 의도적이다.
         **유형:** 문자열
         **예:** &quot;https://plaftform.adobe.io/resolveByPath?path=&quot;/mycorp/content/projectx/fragment/prod/herobanners/banner14.html3&quot;&quot;
   * **콘텐츠**

      **필드:** 콘텐트
      **설명:** 컨텐트를 직접 포함할 선택적 필드입니다. 자산 저장소의 컨텐츠를 참조하는 대신 구성 요소는 간단한 컨텐츠를 직접 저장할 수 있습니다. 이 필드는 복합, 복합 및 이진 컨텐츠 자산에 사용되지 않습니다.
      **유형:** 문자열

   * **deliveryURL**

      **필드:** deliveryURL
      **설명:** 컨텐트 배달 네트워크 또는 서비스 끝점에서 자산을 가져오는 선택적 고유 자원 보관처. 이 URL은 사용자 에이전트가 공개적으로 자산을 액세스하는 데 사용됩니다.
      **유형:** 문자열
      **예:** &quot;https://cdn.adobe.io/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

   * **linkURL**

      **필드:** linkURL
      **설명:** 사용자 상호 작용에 대한 선택적 고유 자원 보관처. 이 URL은 최종 사용자가 사용자 에이전트에서 방문하도록 참조하는 데 사용되며 추적할 수 있습니다.
      **유형:** 문자열
      **예:** &quot;https://cdn.adobe.io/tracker?code=23432&amp;redirect=/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;



* **배치**

   **필드:** 배치
   **제목:** 배치
   **설명:** 준수하기 위한 배치. 값은 참조되는 오퍼 위치의 URI(@id)입니다. 스키마 https://ns.adobe.com/experience/decisioning/placement을 참조하십시오.
   **유형:** 문자열

#### 라이프사이클 상태

**필드:** lifecycleStatus 
**Title:** 라이프사이클 상태 
**설명:** 라이프사이클 상태를 사용하여 개체를 사용하여 워크플로우를 수행할 수 있습니다. 상태는 개체가 표시되거나 관련이 있다고 간주되는 경우에 영향을 줄 수 있습니다. 상태 변경은 개체를 사용하는 클라이언트 또는 서비스에 의해 결정됩니다.
**유형:** 문자열 
**가능한 값:** &quot;초안&quot;, &quot;승인됨&quot;, &quot;라이브&quot;, &quot;완료됨&quot;, &quot;보관됨&quot;, &quot;보관됨&quot; 
**기본값:** &quot;초안&quot;

#### 결정 옵션 이름

**필드:** 이름 
**제목:** 결정 옵션 이름 
**설명:** 다양한 사용자 인터페이스에 표시되는 옵션 이름입니다.
**유형:** 문자열

#### 태그

**필드:** 태그 
**제목:** 태그 
**설명:** 이 엔티티와 연관된 태그 집합입니다. 이 태그는 전체 인벤토리를 하위 세트(카테고리)로 제한하기 위해 필터 표현식에 사용됩니다.
**유형:** 배열

<!--Field without name under tags: Description: An identifier of a tag object. The value is the @id of the tag that is referenced. See tag schema: https://ns.adobe.com/experience/decisioning/tag. Type: string-->

## _repo

### 결정 옵션 설정

**필드:** 태그 
**제목:** 결정 
**옵션 ETag** 설명:스냅샷을 가져올 때 결정 옵션 객체가 있었던 개정입니다.
**유형:** 문자열
