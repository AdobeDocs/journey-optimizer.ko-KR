---
title: 개인화 구문
description: 개인화 구문을 사용하는 방법 알아보기
feature: 개인화
topic: 개인화
role: Data Engineer
level: Intermediate
source-git-commit: b07970ff11f1ba7c4e6db30dc2eca1252a579ca4
workflow-type: tm+mt
source-wordcount: '563'
ht-degree: 4%

---


# 개인화 구문 {#personalization-syntax}

[!DNL Journey Optimizer]의 개인화는 Handlebars라는 템플릿 구문을 기반으로 합니다.
Handlebars 구문에 대한 전체 설명은 [HandlebarsJS 설명서](https://handlebarsjs.com/)를 참조하십시오.

템플릿과 입력 개체를 사용하여 HTML 또는 기타 텍스트 형식을 생성합니다. Handlebars 템플릿은 포함된 Handlebars 표현식이 있는 일반 텍스트와 같습니다.

단순 표현식 샘플:

`{{profile.person.name}}`

위치:

* `profile` 는 네임스페이스입니다.
* `person.name` 는 속성으로 구성된 토큰입니다. 특성 구조는 Adobe Experience Platform XDM 스키마에 정의되어 있습니다. [자세한](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko) 내용{target=&quot;_blank&quot;}.

## 구문 일반 규칙

식별자는 다음을 제외하고 유니코드 문자일 수 있습니다.

```
Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
```

구문은 대/소문자를 구분합니다.

**true**, **false**, **null** 및 **undefined**&#x200B;라는 단어는 경로 식의 첫 부분에서만 사용할 수 있습니다.

Handlebars에서 {{expression}}에서 반환되는 값은 **HTML-escape**&#x200B;입니다. 표현식에 `&`이 포함되어 있으면 반환된 HTML 이스케이프 처리된 출력이 `&amp;`로 생성됩니다. Handlebars가 값을 이스케이프 처리하지 않도록 하려면 &quot;트리플 스태시&quot;를 사용합니다.

## 프로필

이 네임스페이스를 사용하면 [Adobe Experience Platform 데이터 모델(XDM) 설명서](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html){target=&quot;_blank&quot;}에 설명된 프로필 스키마에 정의된 모든 속성을 참조할 수 있습니다.

[!DNL Journey Optimizer] 개인화 블록에서 참조되기 전에 스키마에서 속성을 정의해야 합니다.

>[!NOTE]
>
>[이 섹션](functions/helpers.md#if-function)에 있는 조건에서 프로필 속성을 활용하는 방법을 알아봅니다.

**샘플 참조:**

`{{profile.person.name.fullName}}`

`{{profile.person.name.firstName}}`

`{{profile.person.gender}}`

`{{profile.personalEmail.address}}`

`{{profile.mobilePhone.number}}`

`{{profile.homeAddress.city}}`

`{{profile.faxPhone.number}}`

## 세그먼트{#perso-segments}

[이 섹션](functions/helpers.md#if-function)에 있는 조건에서 프로필 속성을 활용하는 방법을 알아봅니다.

>[!NOTE]
>세그먼테이션 및 세그멘테이션 서비스에 대한 자세한 내용은 [이 섹션](../segment/about-segments.md)을 참조하십시오.


## 오퍼

이 네임스페이스를 사용하면 기존 오퍼 결정을 참조할 수 있습니다.
오퍼를 참조하려면 오퍼를 정의하는 다른 정보로 경로를 선언해야 합니다.

이 경로는 다음 구조를 갖습니다.

`offers.Type.[Placement Id].[Activity Id].Attribute`

위치:

* `offers` 오퍼 네임스페이스에 속하는 경로 표현식을 식별합니다
* `Type`  오퍼 표현 유형을 결정합니다. 가능한 값은 다음과 같습니다.`image`, `html` 및 `text`
* `Placement Id` 및 `Activity Id` 는 배치 및 활동 식별자입니다
* `Attributes` 은 오퍼 유형에 따라 달라지는 오퍼 특정 속성입니다. 예:이미지의 경우 `deliveryUrl`

결정 API 및 오퍼 표현에 대한 자세한 내용은 [이 페이지](../../using/offers/api-reference/decisions-api/deliver-offers.md)를 참조하십시오

모든 참조는 [이 페이지](personalization-validation.md)에 설명된 유효성 검사 메커니즘을 사용하여 오퍼 스키마에 대해 검증됩니다

**샘플 참조:**

* 이미지가 호스팅되는 위치:

   `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].deliveryUrl`

* 이미지를 클릭하면 Target URL:

   `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].linkUrl`

* 의사 결정 엔진에서 나오는 오퍼의 텍스트 컨텐츠:

   `offers.text.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`

* 의사 결정 엔진에서 나오는 오퍼의 HTML 콘텐츠:

   `offers.html.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`


## 도우미{#helpers-all}

Handlebars 도우미는 매개 변수 뒤에 올 수 있는 간단한 식별자입니다.
각 매개 변수는 Handlebars 표현식입니다. 이러한 도우미는 템플릿의 모든 컨텍스트에서 액세스할 수 있습니다.

이러한 블록 도우미는 도우미 이름 앞에 있는 # 로 식별되며 같은 이름의 닫는 / 와 일치해야 합니다.
블록은 블록 열기({{# }})와 닫기({/}})가 있는 표현식입니다.


>[!NOTE]
>
>도우미 함수는 [이 섹션](functions/helpers.md)에 자세히 설명되어 있습니다.


## 리터럴 형식

[!DNL Adobe Journey Optimizer] 에서는 다음 리터럴 유형을 지원합니다.

| 리터럴 | 정의 |
| ------- | ---------- |
| 문자열 | 큰따옴표로 묶인 문자로 구성된 데이터 유형입니다. <br>예: `"prospect"`, `"jobs"`, `"articles"` |
| 부울 | true 또는 false인 데이터 유형입니다. |
| 정수 | 전체 수를 나타내는 데이터 유형입니다. 양수, 음수 또는 0일 수 있습니다. <br>예: `-201`, `0`, `412` |
| 어레이 | 다른 리터럴 값의 그룹으로 구성된 데이터 유형입니다. 대괄호는 대괄호를 사용하여 그룹화하고 쉼표를 사용하여 서로 다른 값 간에 구분합니다.<br> **참고:**  배열 내의 항목의 속성에 직접 액세스할 수는 없습니다. <br> 예: `[1, 4, 7]`, `["US", "FR"]` |

>[!CAUTION]
>
>개인화 식에는 **xEvent** 변수를 사용할 수 없습니다. xEvent를 참조하면 유효성 검사가 실패합니다.
