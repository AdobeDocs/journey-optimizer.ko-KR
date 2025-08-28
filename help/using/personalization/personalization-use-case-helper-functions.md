---
solution: Journey Optimizer
product: journey optimizer
title: Personalization 사용 사례&콜론; 장바구니 포기 이메일
description: 사용 사례를 통해 이메일 메시지의 본문을 개인화하는 방법을 알아봅니다.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: 표현식, 편집기, 도우미, 사용 사례, 개인화
exl-id: 9c9598c0-6fb1-4e2f-b610-ccd1a80e516e
source-git-commit: c9627cfd1d717d56744f0287738b1303194c23e1
workflow-type: tm+mt
source-wordcount: '1037'
ht-degree: 2%

---

# Personalization 사용 사례: 장바구니 포기 이메일 {#personalization-use-case-helper-functions}

이 예제에서는 이메일 메시지의 본문을 개인화합니다. 이 메시지는 장바구니에 품목을 남겨두었지만 구매를 완료하지 않은 고객을 타겟팅합니다.

다음 유형의 도우미 함수를 사용합니다.

* 고객의 이름을 대문자로 삽입하는 `upperCase` 문자열 함수입니다. [자세히 알아보기](functions/string.md#upper).
* `each` 도우미가 장바구니에 있는 항목을 나열합니다. [자세히 알아보기](functions/helpers.md#each).
* 관련 제품이 장바구니에 있는 경우 제품별 메모를 삽입하려면 `if` 도우미를 사용하십시오. [자세히 알아보기](functions/helpers.md#if-function).
<!-- **Context**: personalization based on contextual data from the journey -->

➡️ [이 비디오에서 도우미 함수를 사용하는 방법에 대해 알아보세요](#video)

시작하기 전에 다음 요소를 구성하는 방법을 알고 있어야 합니다.

* 단일 이벤트입니다. [자세히 알아보기](../event/about-events.md).
* 이벤트로 시작하는 여정. [자세히 알아보기](../building-journeys/using-the-journey-designer.md).
* 여정 내 이메일 메시지. [자세히 알아보기](../email/create-email.md)
* 이메일의 본문. [자세히 알아보기](../email/content-from-scratch.md).

다음 단계를 수행하십시오.

1. [초기 이벤트와 여정을 만듭니다](#create-context).
1. [전자 메일 메시지 만들기](#configure-email).
1. [고객의 이름을 대문자로 삽입](#uppercase-function).
1. [전자 메일에 장바구니 콘텐츠를 추가](#each-helper).
1. [제품별 메모를 삽입합니다](#if-helper).
1. [여정 테스트 및 게시](#test-and-publish).

## 1단계: 초기 이벤트 및 관련 여정 만들기 {#create-context}

장바구니 콘텐츠는 여정의 컨텍스트 정보입니다. 따라서 여정 관련 정보를 이메일에 추가하려면 먼저 초기 이벤트와 이메일을 장바구니에 추가해야 합니다.

1. 스키마에 `productListItems` 배열이 포함된 이벤트를 만듭니다.
1. 이 배열의 모든 필드를 이 이벤트의 페이로드 필드로 정의합니다.

   [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/product-list-item.html){target="_blank"}에서 제품 목록 항목 데이터 형식에 대해 자세히 알아보세요.

1. 이 이벤트로 시작하는 여정을 만듭니다.
1. **전자 메일** 활동을 여정에 추가합니다.

   ![](assets/personalization-uc-helpers-8.png)

## 2단계: 이메일 만들기{#configure-email}

1. **전자 메일** 활동에서 **[!UICONTROL 콘텐츠 편집]**&#x200B;을 클릭한 다음 **[!UICONTROL 전자 메일 Designer]**&#x200B;을 클릭합니다.

   ![](assets/personalization-uc-helpers-1.png)

1. 이메일 Designer 홈 페이지의 왼쪽 팔레트에서 3개의 구조 구성 요소를 메시지 본문으로 끌어서 놓습니다.

1. HTML 콘텐츠 구성 요소를 각 새 구조 구성 요소로 끌어다 놓습니다.

   ![](assets/personalization-uc-helpers-2.png)

## 3단계: 고객의 이름을 대문자로 삽입 {#uppercase-function}

1. 이메일 Designer 홈 페이지에서 고객의 이름을 추가하려는 HTML 구성 요소를 클릭합니다.
1. 상황별 도구 모음에서 **[!UICONTROL 소스 코드 표시]**&#x200B;를 클릭합니다.

   ![](assets/personalization-uc-helpers-3.png)

1. **[!UICONTROL HTML 편집]** 창에서 `upperCase` 문자열 함수를 추가합니다.
   1. 왼쪽 메뉴에서 **[!UICONTROL 도우미 함수]**&#x200B;를 선택합니다.
   1. 검색 필드를 사용하여 &quot;대문자&quot;를 찾습니다.
   1. 검색 결과에서 `upperCase` 함수를 추가합니다. 이렇게 하려면 `{%= upperCase(string) %}: string` 옆에 있는 더하기(+) 기호를 클릭합니다.

      표현식 편집기에는 다음 표현식이 표시됩니다.

      ```handlebars
      {%= upperCase(string) %}
      ```

      ![](assets/personalization-uc-helpers-4.png)

1. 표현식에서 &quot;문자열&quot; 자리 표시자를 제거합니다.
1. 이름 토큰 추가:
   1. 왼쪽 메뉴에서 **[!UICONTROL 프로필 특성]**&#x200B;을 선택합니다.
   1. **[!UICONTROL 사용자]** > **[!UICONTROL 전체 이름]**&#x200B;을 선택합니다.
   1. **[!UICONTROL 이름]** 토큰을 식에 추가하십시오.

      표현식 편집기에는 다음 표현식이 표시됩니다.

      ```handlebars
      {%= upperCase(profile.person.name.firstName) %}
      ```

      ![](assets/personalization-uc-helpers-5.png)

      [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/person-name.html){target="_blank"}에서 개인 이름 데이터 유형에 대해 자세히 알아보세요.

1. **[!UICONTROL 유효성 검사]**&#x200B;를 클릭한 다음 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

   ![](assets/personalization-uc-helpers-6.png)

1. 메시지를 저장합니다.

## 4단계: 장바구니에서 항목 목록 삽입 {#each-helper}

1. 메시지 콘텐츠를 다시 엽니다.

1. 이메일 Designer 홈 페이지에서 장바구니 콘텐츠를 나열할 HTML 구성 요소를 클릭합니다.
1. 상황별 도구 모음에서 **[!UICONTROL 소스 코드 표시]**&#x200B;를 클릭합니다.

   ![](assets/personalization-uc-helpers-3.png)

1. **[!UICONTROL HTML 편집]** 창에서 `each` 도우미를 추가합니다.
   1. 왼쪽 메뉴에서 **[!UICONTROL 도우미 함수]**&#x200B;를 선택합니다.
   1. 검색 필드를 사용하여 &quot;각각&quot;을 찾습니다.
   1. 검색 결과에서 `each` 도우미를 추가합니다.

      표현식 편집기에는 다음 표현식이 표시됩니다.

      ```handlebars
      {{#each someArray as |variable|}} {{/each}}
      ```

      ![](assets/personalization-uc-helpers-9.png)

1. 식에 `productListItems` 배열을 추가합니다.

   1. 표현식에서 &quot;someArray&quot; 자리 표시자를 제거합니다.
   1. 왼쪽 메뉴에서 **[!UICONTROL 컨텍스트 특성]**&#x200B;을 선택합니다.

      **[!UICONTROL 컨텍스트 특성]**&#x200B;은(는) 여정 컨텍스트가 메시지에 전달된 후에만 사용할 수 있습니다.

   1. **[!UICONTROL Journey Optimizer]** > **[!UICONTROL 이벤트]** > ***[!UICONTROL event_name]***&#x200B;을 선택한 다음 **[!UICONTROL productListItems]** 노드를 확장합니다.

      이 예제에서 *event_name*&#x200B;은 이벤트의 이름을 나타냅니다.

   1. **[!UICONTROL Product]** 토큰을 식에 추가하십시오.

      표현식 편집기에는 다음 표현식이 표시됩니다.

      ```handlebars
      {{#each context.journey.events.event_ID.productListItems.product as |variable|}} {{/each}}
      ```

      이 예제에서 *event_ID*&#x200B;은 이벤트의 ID를 나타냅니다.

      ![](assets/personalization-uc-helpers-10.png)

   1. 표현식을 수정합니다.
      1. &quot;.product&quot; 문자열을 제거합니다.
      1. &quot;variable&quot; 자리 표시자를 &quot;product&quot;로 바꿉니다.

      다음 예에서는 수정된 표현식을 보여 줍니다.

      ```handlebars
      {{#each context.journey.events.event_ID.productListItems as |product|}}
      ```

1. 여는 `{{#each}}` 태그와 닫는 `{/each}}` 태그 사이에 이 코드를 붙여 넣습니다.

   ```html
   <table>
      <tbody>
         <tr>
            <td><b>#name</b></td>
            <td><b>#quantity</b></td>
            <td><b>$#priceTotal</b></td>
         </tr>
      </tbody>
   </table>
   ```

1. 품목명, 수량 및 가격에 대한 개인화 토큰을 추가합니다.

   1. HTML 표에서 자리 표시자 &quot;#name&quot;를 제거합니다.
   1. 이전 검색 결과에서 **[!UICONTROL Name]** 토큰을 식에 추가하십시오.

   다음 단계를 두 번 반복합니다.

   * 자리 표시자 &quot;#quantity&quot;을 **[!UICONTROL 수량]** 토큰으로 바꾸십시오.
   * 자리 표시자 &quot;#priceTotal&quot;을 **[!UICONTROL 총 가격]** 토큰으로 바꾸십시오.

   다음 예에서는 수정된 표현식을 보여 줍니다.

   ```handlebars
   {{#each context.journey.events.event_ID.productListItems as |product|}}
      <table>
         <tbody>
            <tr>
            <td><b>{{product.name}}</b></td>
            <td><b>{{product.quantity}}</b></td>
            <td><b>${{product.priceTotal}}</b></td>
            </tr>
         </tbody>
      </table>
   {{/each}}
   ```

1. **[!UICONTROL 유효성 검사]**&#x200B;를 클릭한 다음 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

   ![](assets/personalization-uc-helpers-11.png)

## 5단계: 제품별 참고 사항 삽입 {#if-helper}

1. 이메일 Designer 홈 페이지에서 메모를 삽입하려는 HTML 구성 요소를 클릭합니다.
1. 상황별 도구 모음에서 **[!UICONTROL 소스 코드 표시]**&#x200B;를 클릭합니다.

   ![](assets/personalization-uc-helpers-3.png)

1. **[!UICONTROL HTML 편집]** 창에서 `if` 도우미를 추가합니다.
   1. 왼쪽 메뉴에서 **[!UICONTROL 도우미 함수]**&#x200B;를 선택합니다.
   1. 검색 필드를 사용하여 &quot;if&quot;를 찾습니다.
   1. 검색 결과에서 `if` 도우미를 추가합니다.

      표현식 편집기에는 다음 표현식이 표시됩니다.

      ```handlebars
      {%#if condition1%} render_1
         {%else if condition2%} render_2
         {%else%} default_render
      {%/if%}
      ```

      ![](assets/personalization-uc-helpers-12.png)

1. 표현식에서 이 조건 제거:

   ```handlebars
   {%else if condition2%} render_2
   ```

   다음 예에서는 수정된 표현식을 보여 줍니다.

   ```handlebars
   {%#if condition1%} render_1
      {%else%} default_render
   {%/if%}
   ```

1. 조건에 제품 이름 토큰을 추가합니다.
   1. 표현식에서 &quot;condition1&quot; 자리 표시자를 제거합니다.
   1. 왼쪽 메뉴에서 **[!UICONTROL 컨텍스트 특성]**&#x200B;을 선택합니다.
   1. **[!UICONTROL Journey Orchestration]** > **[!UICONTROL 이벤트]** > ***[!UICONTROL event_name]***&#x200B;을 선택한 다음 **[!UICONTROL productListItems]** 노드를 확장합니다.

      이 예제에서 *event_name*&#x200B;은 이벤트의 이름을 나타냅니다.

   1. **[!UICONTROL Name]** 토큰을 식에 추가합니다.

      표현식 편집기에는 다음 표현식이 표시됩니다.

      ```handlebars
      {%#if context.journey.events.`event_ID`.productListItems.name%}
         render_1
         {%else%} default_render
      {%/if%}
      ```

      ![](assets/personalization-uc-helpers-13.png)

1. 표현식을 수정합니다.
   1. 표현식 편집기에서 `name` 토큰 뒤에 제품 이름을 지정합니다.

      이 구문을 사용하십시오. 여기서 *product_name*&#x200B;은(는) 제품 이름을 나타냅니다.

      ```javascript
      = "product_name"
      ```

      이 예에서 제품 이름은 &quot;Juno Jacket&quot;입니다.

      ```handlebars
      {%#if context.journey.events.`event_ID`.productListItems.name = "Juno Jacket" %}
         render_1
         {%else%} default_render
      {%/if%}
      ```

   1. &quot;render_1&quot; 자리 표시자를 메모의 텍스트로 바꿉니다.

      예:

      ```handlebars
      {%#if context.journey.events.`event_ID`.productListItems.name = "Juno Jacket" %}
         Due to longer than usual lead times on the Juno Jacket, please expect item to ship two weeks after purchase.
         {%else%} default_render
      {%/if%}
      ```

   1. 표현식에서 &quot;default_render&quot; 자리 표시자를 제거합니다.
1. **[!UICONTROL 유효성 검사]**&#x200B;를 클릭한 다음 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

   ![](assets/personalization-uc-helpers-14.png)

1. 메시지를 저장합니다.

## 6단계: 여정 테스트 및 게시 {#test-and-publish}

1. **[!UICONTROL 테스트]** 토글을 켜고 **[!UICONTROL 이벤트 트리거]**&#x200B;를 클릭합니다.

   ![](assets/personalization-uc-helpers-15.png)

1. **[!UICONTROL 이벤트 구성]** 창에서 입력 값을 입력한 다음 **[!UICONTROL 보내기]**&#x200B;를 클릭합니다.

   테스트 모드는 테스트 프로필에서만 작동합니다.

   ![](assets/personalization-uc-helpers-16.png)

   이메일은 테스트 프로필의 주소로 전송됩니다.

   이 제품은 장바구니에 들어 있으므로 이 이메일에는 Juno Jacket에 대한 메모가 포함되어 있습니다.

   ![](assets/personalization-uc-helpers-17.png)

1. 오류가 없는지 확인한 다음 여정을 게시합니다.


## 관련 항목 {#related-topics}

### Handlebars 함수 {#handlebars}

* [도우미](functions/helpers.md)

* [문자열 함수](functions/string.md)

### 사용 사례 {#use-case}

* [프로필 정보, 컨텍스트 및 오퍼가 있는 Personalization](personalization-use-case.md)

* [의사 결정 기반 오퍼가 있는 Personalization](../offers/offers-e2e.md)

## 사용 방법 비디오{#video}

도우미 함수를 사용하는 방법에 대해 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/334244?quality=12)
