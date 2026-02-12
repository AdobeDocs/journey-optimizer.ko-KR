---
title: 의사 결정 정책의 구성요소 활용
description: 의사 결정 정책에서 조각을 활용하는 방법 알아보기
feature: Decisioning
topic: Integrations
role: User
level: Experienced
exl-id: 70f64348-092b-4350-91dc-72c3c07300f9
source-git-commit: b414d330a25a98c11b7417beda4536c54c41fd83
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 0%

---

# 의사 결정 정책의 구성요소 활용 {#fragments}

의사 결정 정책에 조각이 포함된 의사 결정 항목이 포함되어 있는 경우 의사 결정 정책 코드에서 이러한 조각을 활용할 수 있습니다. [조각에 대해 자세히 알아보기](../content-management/fragments.md)

>[!AVAILABILITY]
>
>이 기능은 현재 **코드 기반 경험** 채널에서만 사용할 수 있습니다.

예를 들어 여러 모바일 디바이스 모델에 대해 서로 다른 콘텐츠를 표시하려고 한다고 가정해 보겠습니다. 해당 디바이스에 해당하는 조각을 결정 정책에서 사용 중인 결정 항목에 추가했는지 확인하십시오. [방법을 알아보세요](items.md#attributes).

![](assets/item-fragments.png){width=70%}

완료되면 다음 방법 중 하나를 사용할 수 있습니다.

>[!BEGINTABS]

>[!TAB 직접 코드 삽입]

아래의 코드 블록을 의사 결정 정책 코드에 복사하여 붙여넣기만 하면 됩니다. `variable`을(를) 조각 ID로 바꾸고 `placement`을(를) 조각 참조 키로 바꿉니다.

```
{% let variable =  get(item._experience.decisioning.offeritem.contentReferencesMap, "placement").id %}
{{fragment id = variable}}
```

>[!TAB 자세한 단계 따르기]

1. **[!UICONTROL 도우미 함수]**(으)로 이동하고 조각에 대한 변수를 선언할 수 있는 코드 창에 **Let** 함수 `{% let variable = expression %} {{variable}}`을(를) 추가합니다.

   ![](assets/decision-let-function.png)

1. **맵** > **Get** 함수 `{%= get(map, string) %}`을(를) 사용하여 식을 빌드합니다. 맵은 결정 항목에서 참조된 조각이며 문자열은 **[!UICONTROL 조각 참조 키]**(으)로 결정 항목에 입력한 장치 모델일 수 있습니다.

   ![](assets/decision-map-function.png)

1. 이 디바이스 모델 ID가 포함된 상황별 속성을 사용할 수도 있습니다.

   ![](assets/decision-contextual-attribute.png)

1. 조각에 대해 선택한 변수를 조각 ID로 추가합니다.

   ![](assets/decision-fragment-id.png)

>[!ENDTABS]

결정 항목의 **[!UICONTROL 조각]** 섹션에서 조각 ID와 참조 키가 선택됩니다.

>[!WARNING]
>
>조각 키가 올바르지 않거나 조각 컨텐츠가 유효하지 않은 경우 렌더링이 실패하여 Edge 호출에 오류가 발생합니다.

## 조각을 사용할 때의 보호 기능 {#fragments-guardrails}

**결정 항목 및 컨텍스트 특성**

[!DNL Journey Optimizer] 조각에서는 기본적으로 결정 항목 특성 및 contextal 특성이 지원되지 않습니다. 그러나 아래 설명된 것처럼 전역 변수를 대신 사용할 수 있습니다.

조각에서 *sport* 변수를 사용한다고 가정해 보겠습니다.

1. 조각에서 이 변수를 참조합니다. 예를 들면 다음과 같습니다.

   ```
   Elevate your practice with new {{sport}} gear!
   ```

1. 결정 정책 블록 내에서 **Let** 함수를 사용하여 변수를 정의합니다. 아래 예에서 *sport*&#x200B;은(는) 결정 항목 특성으로 정의됩니다.

   ```
   {#each decisionPolicy.13e1d23d-b8a7-4f71-a32e-d833c51361e0.items as |item|}}
   {% let sport = item._cjmstage.value %}
   {{fragment id = get(item._experience.decisioning.offeritem.contentReferencesMap, "placement1").id }}
   {{/each}}
   ```

**결정 항목 조각 콘텐츠 유효성 검사**

* 이러한 조각의 동적 특성으로 인해 캠페인에서 사용할 경우, 의사 결정 항목에서 참조되는 조각에 대해 캠페인 콘텐츠 생성 중 메시지 유효성 검사를 건너뜁니다.

* 조각 콘텐츠의 유효성 검사는 조각 생성 및 게시 중에만 수행됩니다.

* JSON 유형 표현식 조각의 경우 조각이 저장될 때 콘텐츠가 구문적으로 확인됩니다. 유효성 검사 오류는 경고로 표시됩니다.

런타임 시 캠페인 콘텐츠(의사 결정 항목의 조각 콘텐츠 포함)의 유효성이 검사됩니다. 유효성 검사 실패 시 캠페인이 렌더링되지 않습니다.
