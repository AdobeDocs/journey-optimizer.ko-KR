---
title: 의사 결정 정책의 구성요소 활용
description: 의사 결정 정책에서 조각을 활용하는 방법 알아보기
feature: Decisioning
topic: Integrations
role: User
level: Experienced
exl-id: 70f64348-092b-4350-91dc-72c3c07300f9
source-git-commit: e33a18cdb330f9d5d1a88b771a648031176c20a8
workflow-type: tm+mt
source-wordcount: '752'
ht-degree: 0%

---

# 의사 결정 정책의 구성요소 활용 {#fragments}

의사 결정 정책에 조각이 포함된 의사 결정 항목이 포함되어 있는 경우 의사 결정 정책 내에서 메시지를 작성할 때 이러한 조각을 활용할 수 있습니다. [조각에 대해 자세히 알아보기](../content-management/fragments.md)

>[!AVAILABILITY]
>
>이 기능은 **코드 기반 경험** 및 **이메일** 채널에서 사용할 수 있습니다.

예를 들어 여러 모바일 디바이스 모델에 대해 서로 다른 콘텐츠를 표시하려고 한다고 가정해 보겠습니다. 다른 전화 모델에 속하는 지정된 조각을 결정 정책에서 사용 중인 결정 항목에 추가합니다. [방법을 알아보세요](items.md#attributes).

![조각 참조 및 배치 키를 표시하는 결정 항목의 조각 섹션.](assets/item-fragments.png){width=70%}

완료되면 다음 방법 중 하나를 사용할 수 있습니다.

>[!BEGINTABS]

>[!TAB 직접 코드 삽입]

아래의 코드 블록을 의사 결정 정책 코드에 복사하여 붙여넣기만 하면 됩니다. `variable`을(를) 조각 ID로 바꾸고 `placement`을(를) 조각 참조 키로 바꿉니다.

```handlebars
{% let variable =  get(item._experience.decisioning.offeritem.contentReferencesMap, "placement").id %}
{{fragment id = variable required=false}}
```

>[!TAB 자세한 단계 따르기]

1. **[!UICONTROL 도우미 함수]**(으)로 이동하고 조각에 대한 변수를 선언할 수 있는 코드 창에 **Let** 함수 `{% let variable = expression %} {{variable}}`을(를) 추가합니다.

   ![도우미 함수를 코드 창에 추가하도록 설정하는 방법을 보여 주는 의사 결정 정책 코드 편집기.](assets/decision-let-function.png)

1. **맵** > **Get** 함수 `{%= get(map, string) %}`을(를) 사용하여 식을 빌드합니다. 맵은 의사 결정 항목에서 참조되는 조각입니다. 문자열은 **[!UICONTROL 조각 참조 키]**(으)로 결정 항목에 입력한 장치 모델일 수 있습니다.

   ![조각 맵과 조각 참조 키를 참조하는 데 사용되는 매핑 및 가져오기 함수입니다.](assets/decision-map-function.png)

1. 이 디바이스 모델 ID가 포함된 상황별 속성을 사용할 수도 있습니다.

   ![장치 모델 식별자에 대해 컨텍스트 특성이 선택되었습니다.](assets/decision-contextual-attribute.png)

1. 조각에 대해 선택한 변수를 조각 ID로 추가합니다.

   ![결정 정책 코드의 결정 항목에서 설정된 조각 ID 변수입니다.](assets/decision-fragment-id.png)

>[!ENDTABS]

결정 항목의 **[!UICONTROL 조각]** 섹션에서 조각 ID와 참조 키가 선택됩니다.

>[!WARNING]
>
>조각 키가 올바르지 않거나 조각 컨텐츠가 유효하지 않은 경우 렌더링이 실패하고 Edge 호출에 오류가 발생할 수 있습니다.
>
>조각을 일시적으로 사용할 수 없을 때 오류를 방지하기 위해 `required=false` 플래그가 사용되므로 대신 해당 조각을 건너뜁니다. [자세히 알아보기](#temporary-unavailable-fragments)

## 사용 및 보호 {#fragments-guardrails}

### 이메일의 콘텐츠 및 표현식 조각 시뮬레이션 {#simulate-content-expression-fragments}

**이메일** 채널의 경우 **[!UICONTROL 증명 보내기]** 또는 캠페인이 활성화될 때 결정 항목과 연결된 표현식 조각이 올바르게 표시됩니다. 그러나 **[!UICONTROL 콘텐츠 시뮬레이션]**&#x200B;은(는) 결정 항목의 표현식 조각을 표시하지 않습니다.

### 이메일의 시각적 조각 및 의사 결정 항목 {#visual-fragments-decision-items}

**[!UICONTROL 시각적 조각]**&#x200B;을(를) 결정 항목에 할당할 수 없습니다. 이 컨텍스트에서는 **식 조각**&#x200B;만 지원됩니다.

### 의사 결정 항목 및 컨텍스트 속성 {#decision-item-context-attributes}

[!DNL Journey Optimizer] 조각에서는 기본적으로 의사 결정 항목 특성 및 컨텍스트 특성이 지원되지 않습니다. 그러나 아래 설명된 것처럼 전역 변수를 대신 사용할 수 있습니다.

조각에서 *sport* 변수를 사용한다고 가정해 보겠습니다.

1. 조각에서 이 변수를 참조합니다. 예를 들면 다음과 같습니다.

   ```text
   Elevate your practice with new {{sport}} gear!
   ```

1. 결정 정책 블록 내에서 **Let** 함수를 사용하여 변수를 정의합니다. 아래 예에서 *sport*&#x200B;은(는) 결정 항목 특성으로 정의됩니다.

   ```handlebars
   {#each decisionPolicy.13e1d23d-b8a7-4f71-a32e-d833c51361e0.items as |item|}}
   {% let sport = item._cjmstage.value %}
   {{fragment id = get(item._experience.decisioning.offeritem.contentReferencesMap, "placement1").id }}
   {{/each}}
   ```

### 의사 결정 항목 조각 콘텐츠 유효성 검사 {#fragment-content-validation}

* 이러한 조각의 동적 특성으로 인해 캠페인에서 사용할 경우, 의사 결정 항목에서 참조되는 조각에 대해 캠페인 콘텐츠 생성 중 메시지 유효성 검사를 건너뜁니다.

* 조각 콘텐츠의 유효성 검사는 조각 생성 및 게시 중에만 수행됩니다.

* JSON 유형 표현식 조각의 경우 조각이 저장될 때 콘텐츠가 구문적으로 확인됩니다. 유효성 검사 오류는 경고로 표시됩니다.

런타임 시 캠페인 콘텐츠(의사 결정 항목의 조각 콘텐츠 포함)의 유효성이 검사됩니다. 유효성 검사 실패 시 캠페인이 렌더링되지 않습니다.

### 일시적으로 사용할 수 없는 조각은 건너뜁니다. {#temporary-unavailable-fragments}

여정 또는 캠페인이 의사 결정 항목에 첨부된 조각을 참조하는 경우 업데이트된 조각을 Edge에서 사용하기 전에 잠시 동기화가 지연될 수 있습니다.

조각을 일시적으로 사용할 수 없을 때 오류를 방지하기 위해 이제 조각에 `required` 플래그가 기본적으로 `false`(으)로 설정되어 여정 또는 캠페인이 실패하는 대신 건너뜁니다.

즉, Edge에서 조각을 일시적으로 사용할 수 없는 경우 이를 무시합니다. 조각을 사용할 수 있는 경우 정상적으로 렌더링됩니다.

**예**

결정 정책이 두 개의 오퍼에 적합하고 각 오퍼에 조각(예: &quot;20% 할인&quot; 및 &quot;30% 할인&quot;)이 있고 두 번째 조각을 일시적으로 사용할 수 없는 경우 `required=false`을(를) 사용하면 시스템에서 여정 또는 캠페인에 실패하는 대신 사용 가능한 오퍼를 렌더링하고(20% 할인) 다른 조각을 건너뜁니다(30% 할인). 이렇게 하면 콘텐츠가 여전히 동기화 중일 때 안정성이 향상됩니다.

>[!NOTE]
>
>`required` 플래그를 `true`(으)로 설정하여 조각을 필수 항목으로 표시할 수 있습니다. 그러나 조각이 일시적으로 누락된 경우 여정 또는 캠페인 렌더링이 실패할 수 있습니다.

