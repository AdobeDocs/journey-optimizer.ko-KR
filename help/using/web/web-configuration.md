---
title: 웹 채널 구성
description: 웹 채널 구성 만들기
feature: Web Channel, Channel Configuration
topic: Content Management
role: Admin
level: Experienced
source-git-commit: b9208544b08b474db386cce3d4fab0a4429a5f54
workflow-type: tm+mt
source-wordcount: '855'
ht-degree: 10%

---

# 웹 채널 구성 만들기 {#web-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_page_rule"
>title="페이지 일치 규칙"
>abstract="동일한 기준을 공유하는 URL 그룹을 효율적으로 관리하고 타겟팅하려면 페이지 일치 규칙을 만드십시오. 이 규칙을 사용하면 여러 URL을 하나의 가이드라인으로 통합하여 이러한 페이지 전체에서 쉽게 일관된 설정과 액션을 적용할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_admin_default_url"
>title="기본 작성 및 미리보기 URL"
>abstract="이 필드는 규칙에 의해 생성되거나 규칙과 일치하는 페이지에 지정된 URL이 있는지 확인하는 데 필요한데, 이는 콘텐츠를 효과적으로 만들고 미리 보는 데 필수적입니다."

웹 구성은 콘텐츠가 전달될 URL로 식별되는 웹 속성입니다. 단일 페이지 URL 또는 여러 페이지를 일치시킬 수 있으므로 하나 또는 여러 웹 페이지에서 수정 사항을 전달할 수 있습니다.

1. **[!UICONTROL 채널]** > **[!UICONTROL 일반 설정]** > **[!UICONTROL 채널 구성]** 메뉴에 액세스한 다음 **[!UICONTROL 채널 구성 만들기]**&#x200B;를 클릭하십시오.

   ![](assets/web_config_1.png)

1. 구성의 이름 및 설명(선택 사항)을 입력합니다.

   >[!NOTE]
   >
   > 이름은 문자(A-Z)로 시작해야 합니다. 영숫자만 포함할 수 있습니다. 밑줄 `_`, 점`.` 및 하이픈 `-`자를 사용할 수도 있습니다.

1. 구성에 사용자 지정 또는 핵심 데이터 사용 레이블을 할당하려면 **[!UICONTROL 액세스 관리]**&#x200B;를 선택할 수 있습니다. [OLAC(개체 수준 액세스 제어)에 대해 자세히 알아보세요](../administration/object-based-access.md).

1. **웹** 채널을 선택하십시오.

   ![](assets/web_config_2.png)

1. 이 구성을 사용하여 동의 정책을 메시지에 연결하려면 **[!UICONTROL 마케팅 액션]**&#x200B;을 선택하십시오. 마케팅 액션과 관련된 모든 동의 정책은 고객의 선호도를 존중하기 위해 활용됩니다. [자세히 알아보기](../action/consent.md#surface-marketing-actions)

1. 변경 내용을 단일 페이지에만 적용하려면 **[!UICONTROL 페이지 URL]**&#x200B;을(를) 입력할 수 있습니다.

1. 또는 **[!UICONTROL 페이지 일치 규칙]**&#x200B;을(를) 만들어 동일한 규칙과 일치하는 여러 URL을 대상으로 할 수 있습니다. 예를 들어, 전체 웹 사이트에서 히어로 배너에 변경 사항을 적용하거나 웹 사이트의 모든 제품 페이지에 표시되는 상위 이미지를 추가하려는 경우입니다.

   이렇게 하려면 **[!UICONTROL 페이지 일치 규칙]**&#x200B;을 선택합니다.

1. **[!UICONTROL 도메인]** 및 **[!UICONTROL 페이지]** 필드에 대한 조건을 정의합니다.

   예를 들어 Luma 웹 사이트의 모든 여성 제품 페이지에 표시되는 요소를 편집하려면 **[!UICONTROL 도메인]** > **[!UICONTROL 다음으로 시작]** > `luma` 및 **[!UICONTROL 페이지]** > **[!UICONTROL 포함]** > `women`을(를) 선택합니다.

   ![](assets/web_config_3.png)

1. **[!UICONTROL 페이지 일치 규칙]**&#x200B;을 만든 경우 **기본** 작성 및 미리 보기 URL을 입력해야 합니다. 이 단계에서는 규칙을 통해 생성되거나 일치된 페이지에 콘텐츠 작성 및 미리보기 목적으로 지정된 URL이 있는지 확인합니다. 아래 [섹션](#web-page-matching-rule)에서 페이지 일치 규칙에 대해 자세히 알아보세요.

1. 변경 내용을 저장합니다.

이제 캠페인이나 여정에서 웹 채널을 사용할 때 구성을 선택할 수 있습니다.

## 페이지 일치 규칙 {#web-page-matching-rule}

여러 페이지에 걸쳐 동일한 콘텐츠 변경 내용을 한 번에 적용할 수 있도록 여러 페이지와 일치하는 규칙을 만들 때 **도메인** 및 **경로** 섹션에서 다른 연산자를 사용하여 원하는 규칙을 만들 수 있습니다. 아래에서 사용 가능한 연산자를 확인하십시오.

페이지 일치 규칙 작성에 사용할 수 있는 연산자:

* **도메인**

  | 연산자  | 설명  | 예  |
  |---|---|---|
  | 다음과 같음  | 도메인의 정확한 일치  |
  | 다음으로 시작  | 입력한 문자열로 시작하는 모든 도메인(하위 도메인 포함)과 일치합니다.  | 예: &quot;다음으로 시작: dev&quot; -> dev.example.com, dev.products.example.com, developer.example.com과 같이 &quot;dev&quot;로 시작하는 모든 도메인 및 하위 도메인과 일치  |
  | 다음으로 끝남  | 입력한 문자열로 끝나는 모든 도메인(하위 도메인 포함)과 일치합니다.  | 예: &quot;example.com으로 끝남&quot; -> stage.example.com, prod.example.com, myexample.com 등 &quot;example.com&quot;으로 끝나는 모든 도메인 및 하위 도메인과 일치  |
  | 와일드카드 일치  | &quot;와일드카드 일치&quot; 연산자를 사용하면 사용자가 &quot;dev&quot;와 같이 문자열 중간에 와일드카드 일치를 정의할 수 있습니다.*.example.com&quot;. 유효성 검사 규칙은 연산자가 &quot;와일드카드 일치&quot;인 경우 값에 와일드카드(별표)를 하나만 포함해야 합니다.  | 예: &quot;와일드카드 일치: dev.*.example.com&quot; -> dev.products.example.com, dev.mytest.products.example.com, dev.blog.example.com 등의 도메인과 일치합니다.  |
  | 임의  | 모든 도메인에 일치 - 도메인 간 특정 경로를 테스트할 때 유용함  |


* **경로**

  | | | |
  |-|-|-|
  | 연산자  | 설명  | 예  |
  | 다음과 같음  | 경로의 정확한 일치.  |    |
  | 다음으로 시작  | 입력한 문자열로 시작하는 모든 경로(하위 경로 포함)와 일치합니다.  |    |
  | 다음으로 끝남  | 입력한 문자열로 끝나는 모든 경로(하위 경로 포함)와 일치합니다.  |    |
  | 임의  | 모든 경로와 일치합니다. 하나 또는 여러 도메인에서 모든 경로를 타깃팅할 때 유용합니다.  |    |
  | 와일드카드 일치  | &quot;와일드카드 일치&quot; 연산자를 사용하면 사용자가 &quot;/products/*/detail&quot;과 같은 내부 와일드카드를 경로 내에 정의할 수 있습니다.  경로 ** 구성 요소의 와일드카드 문자 *는 첫 번째 / 문자가 발견될 때까지 문자 시퀀스를 일치시킵니다.  /*/ 모든 문자 시퀀스(하위 경로 포함)와 일치  | 예: &quot;와일드카드 일치: /products/*/detail&quot;, 다음과 같은 모든 경로와 일치:  example.com/products/yoga/detail  example.com/products/surf/detail  example.com/products/tennis/detail  example.com/products/yoga/pants/detail   예: &quot;일치함: /prod*/detail, 다음과 같은 모든 경로와 일치함:  example.com/products/detail  example.com/production/detail   다음과 같은 경로와 일치하지 않음:  example.com/products/yoga/detail  |
  | 다음 포함  | &quot;포함&quot;은 &quot;mystring&quot;과 같은 와일드카드로 변환되고 이 문자 시퀀스를 포함하는 모든 경로와 일치합니다.  | 예: &quot;Contains: product&quot;, example.com/products, example.com/yoga/perfproduct, example.com/surf/productdescription, example.com/home/product/page 등과 같이 문자열 product가 포함된 모든 경로와 일치  |


하나의 규칙을 사용하여 사용 사례를 모델링할 수 없는 경우 여러 페이지 규칙을 추가할 수 있는 옵션이 있으며 이들 사이에 &#39;Or&#39; 또는 &#39;Exclude&#39; 연산자를 사용할 수 있습니다. &#39;제외&#39;는 정의된 규칙과 일치하는 페이지 중 하나를 타깃팅해서는 안 되는 경우에 유용합니다. 예를 들어 `https://example.com/blogs/productinfo` 페이지를 제외하고 &quot;product&quot;가 포함된 모든 &quot;example.com&quot; 페이지입니다.