---
solution: Journey Optimizer
product: journey optimizer
title: 이메일의 URL 개인화
description: 추적을 안정적으로 유지하면서 동적으로 URL을 생성하기 위한 모범 사례와 제한 사항에 대해 알아봅니다
feature: Email Design, Monitoring
topic: Content Management
role: User
level: Intermediate, Experienced
keywords: url, 링크, 개인화, 추적, 인코딩, 중괄호
source-git-commit: 36fad8d6c200118210794249fa12263ae70e5422
workflow-type: tm+mt
source-wordcount: '760'
ht-degree: 1%

---

# 이메일의 URL 개인화 {#url-personalization}

개인화된 URL을 사용하면 받는 사람별 링크를 생성하거나 동적 매개 변수를 추가하는 등, [!DNL Journey Optimizer] 전자 메일 메시지를 통해 상황별 경험을 제공할 수 있습니다.

프로필 속성에 따라 수신자를 웹 사이트의 특정 페이지 또는 개인화된 마이크로사이트로 안내합니다.

## URL 개인화 {#personalize-url}

URL을 개인화하려면 아래 단계를 수행합니다.

1. 이메일 Designer에서 콘텐츠에서 요소를 선택하고 상황별 도구 모음을 사용하여 [링크 삽입](message-tracking.md#insert-links)을 합니다.

   >[!IMPORTANT]
   >
   >Personalization은 **[!UICONTROL 외부 링크]**, **[!UICONTROL 구독 취소 링크]** 및 **[!DNL Opt-Out]**&#x200B;에만 사용할 수 있습니다. 적절한 링크 유형을 선택해야 합니다.

1. 개인화 아이콘을 선택합니다.

   ![](assets/message-tracking-insert-link-perso.png)

1. 개인화 편집기를 사용하여 URL을 개인화할 프로필 속성을 추가합니다.

1. 변경 내용을 저장합니다.

다음은 개인화된 URL의 몇 가지 예입니다.

* `https://www.adobe.com/users/{{profile.person.name.lastName}}`
* `https://www.adobe.com/users?uid={{profile.person.name.firstName}}`
* `https://www.adobe.com/usera?uid={{context.journey.technicalProperties.journeyUID}}`
* `https://www.adobe.com/users?uid={{profile.person.crmid}}&token={{context.token}}`

>[!NOTE]
>
>개인화 편집기에서 개인화된 URL을 편집할 때 보안상의 이유로 도우미 함수와 대상자 멤버십이 비활성화됩니다.
>
>URL 내에서 사용되는 개인화 토큰에는 공백이 지원되지 않습니다.

안정적인 렌더링 및 추적을 위해 아래의 [모범 사례 및 보호 기능](#best-practices)을 따르십시오.

## 전체/기본 URL 개인화 {#personalize-complete-base-url}

Journey Optimizer은 다음과 같은 URL의 **전체** URL 또는 **기본 도메인** 개인화도 지원합니다.

```html
<a href="{{profile.social.link}}" />
<a href="{{profile.social.baseUrl}}/profile" />
<a href="https://{{profile.social.baseUrl}}/profile" />
```

>[!IMPORTANT]
>
>전체 또는 기본 URL 개인화를 활성화하려면 Adobe에 연락하여 허용된 도메인 목록을 제공하십시오. 안전하지 않은 리디렉션을 방지하기 위해 필요합니다.

## URL 추적 매개 변수 개인화 {#personalize-url-tracking-parameters}

[URL 추적](url-tracking.md)은(는) 채널 구성 수준에서 관리되며 메시지 콘텐츠에 포함된 모든 URL에 적용됩니다. 이메일 Designer에서 개별 링크에 대한 URL 추적 매개 변수를 개인화할 수도 있습니다. 이렇게 하면 수신자별 매개 변수를 단일 링크에 추가할 수 있습니다(예: 웹 분석 도구에 식별자를 전달).

이렇게 하려면 [링크를 삽입](message-tracking.md#insert-links)하고 개인화 아이콘을 선택하고 URL 추적 매개 변수를 추가한 다음 [개인화 편집기](../personalization/personalization-build-expressions.md)에서 선택한 프로필 특성을 선택하십시오.

![](assets/message-tracking-perso-parameter.png)

이 추적 매개 변수를 추가할 각 링크에 대해 위의 단계를 반복합니다.

이제 이메일이 발송되면 이 매개 변수가 URL의 끝에 자동으로 추가됩니다. 그런 다음 웹 분석 도구 또는 성능 보고서에서 이 매개 변수를 캡처할 수 있습니다.

>[!NOTE]
>
>최종 URL을 확인하려면 증명을 [보내고](../content-management/proofs.md) 증명을 받은 후 전자 메일의 콘텐츠에서 링크를 클릭할 수 있습니다. URL에 추적 매개 변수가 표시되어야 합니다. 예: <https://luma.enablementadobe.com/content/luma/us/en.html?utm_contact=profile.userAccount.contactDetails.homePhone.number>

## 우수 사례 및 보호 기능 {#best-practices}

링크를 유효하고 클릭 가능하며 추적 가능하게 유지하려면 아래 모범 사례 및 보호 기능을 따르십시오.

### 동적 URL 중괄호 {#use-braces}

개인화가 포함된 URL을 삽입할 때 URL의 동적 부분에 세 개의 중괄호(`{{{ ... }}}`)를 사용합니다. 이렇게 하면 이스케이프가 특수 문자(예: `/` 및 `+`)를 변경하지 못하도록 하고 끊어진 URL, 잘못된 리디렉션 또는 추적 문제를 방지하는 데 도움이 됩니다.

다음은 한 예입니다.

```html
<a href="https://example.com/path/{{{profile.person.customSlug}}}?ref={{{context.system.source.id}}}">View details</a>
```

>[!IMPORTANT]
>
>원시 출력(`{{{ ... }}}`)을 사용하면 값이 그대로 삽입됩니다. 신뢰할 수 있고 URL에 안전한 값(예: 업스트림을 생성하거나 유효성을 검사하는 값)에만 사용하십시오.

### URL 추적 수정 {#enable-url-tracking}

* 개인화를 사용하여 URL을 생성할 때 확인된 값이 모든 수신자에 대해 `http`/`https`(으)로 시작하는지 확인하십시오. 그렇지 않으면 추적이 적용되지 않고 링크가 예상대로 작동하지 않을 수 있습니다.

* 개인화 편집기의 URL 필드에 직접 `let`, `each` 또는 `if` 문과 같은 동적 논리를 사용하지 마십시오. 보안상의 이유로 비활성화됩니다.

* 시나리오에 개인화된 URL을 생성하는 복잡한 논리가 포함된 경우 해당 논리를 개인화 편집기의 URL 필드에 직접 배치하지 마십시오. 대신:
   * URL 필드 위 또는 근처의 HTML 컨텐츠에 필요한 논리 및 문을 추가합니다.
   * 개인화된 속성을 별도로 생성 및 저장한 다음 이메일 콘텐츠에서 참조합니다.

### URL 인코딩 및 길이 {#encoding}

* URI 구문 규칙([RFC 3986 standard](https://datatracker.ietf.org/doc/html/rfc3986){target="_blank"})은 전자 메일 콘텐츠의 모든 URL에 적용됩니다. 그러나 수신자별 값으로 인해 예약된 문자(예: 쿼리 매개 변수)가 발생할 수 있으므로 개인화된 URL은 인코딩 문제를 초래할 가능성이 높습니다. 따라서 동적 값이 URL로 인코딩되어 있는지(특히 공백, `&`, `#`, `%` 및 `+`) 확인하고 쿼리 값에 `+`을(를) 사용하지 마십시오.

* 매우 긴 URL은 브라우저, 메일 클라이언트 또는 다운스트림 시스템에서 잘리거나 거부할 수 있습니다. 예를 들어 런타임 개인화가 많을 때 미러 페이지 URL이 크게 증가할 수 있습니다. 개인화된 페이로드를 작게 유지하고 큰 오브젝트를 URL에 임베드하지 마십시오.

### 권장 유효성 검사 단계 {#validation}

여정 또는 캠페인을 활성화하기 전에 아래 권장 사항을 따르십시오.

* [증명](../content-management/proofs.md)을(를) 보내고 링크를 클릭하여 확인된 URL이 `http`/`https`(으)로 시작되고 예상 구조를 유지하는지 확인하십시오.
* 추적 매개 변수가 추가되면 최종 URL에 해당 매개 변수가 포함되어 있는지 확인합니다(구성 수준 URL 추적 또는 링크당 추적 매개 변수를 통해).

