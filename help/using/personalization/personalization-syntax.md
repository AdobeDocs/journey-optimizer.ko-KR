---
solution: Journey Optimizer
product: journey optimizer
title: 개인화 구문
description: 개인화 구문을 사용하는 방법을 알아봅니다.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: 표현식, 편집기, 구문, 개인화
exl-id: 5a562066-ece0-4a78-92a7-52bf3c3b2eea
source-git-commit: 78c1464ccddec75e4827cbb1877d8fab5ac08b90
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 3%

---

# 개인화 구문 {#personalization-syntax}

[!DNL Journey Optimizer]의 Personalization은 Handlebars라는 템플릿 구문을 기반으로 합니다. Handlebars 구문에 대한 자세한 설명은 [HandlebarsJS 설명서](https://handlebarsjs.com/)를 참조하십시오.

템플릿과 입력 개체를 사용하여 HTML 또는 기타 텍스트 형식을 생성합니다. Handlebars 템플릿은 포함된 Handlebars 표현식이 있는 일반 텍스트처럼 보입니다.

단순 표현식 샘플:

`{{profile.person.name}}`

여기서:

* `profile`은(는) 네임스페이스입니다.
* `person.name`은(는) 특성으로 구성된 토큰입니다. 속성 구조는 Adobe Experience Platform XDM 스키마에서 정의됩니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko-KR){target="_blank"}.

## 구문 일반 규칙 {#general-rules}

* 식별자는 다음을 제외한 모든 유니코드 문자일 수 있습니다.

  ```
  Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
  ```

* 구문은 대/소문자를 구분합니다.

* **true**, **false**, **null** 및 **정의되지 않음**&#x200B;은(는) 경로 식의 첫 부분에서만 사용할 수 있습니다.

* Handlebars에서 {{expression}}이(가) 반환한 값은 **HTML 이스케이프**&#x200B;입니다. 식에 `&`이(가) 포함된 경우 반환된 HTML 이스케이프 출력은 `&amp;`(으)로 생성됩니다. Handlebars가 값을 이스케이프 처리하지 않게 하려면 &quot;triple-stash&quot;를 사용합니다.

* 리터럴 함수 인수와 관련하여 템플릿 언어 파서는 이스케이프 처리되지 않은 단일 백슬래시(`\`) 기호를 지원하지 않습니다. 이 문자는 추가 백슬래시(`\`) 기호로 이스케이프해야 합니다. 예 :

  `{%= regexGroup("abc@xyz.com","@(\\w+)", 1)%}`

## 사용 가능한 네임스페이스 {#namespaces}

* **프로필**

  이 네임스페이스를 사용하면 [XDM(Adobe Experience Platform 데이터 모델) 설명서](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=ko-KR){target="_blank"}에 설명된 프로필 스키마에 정의된 모든 특성을 참조할 수 있습니다.

  [!DNL Journey Optimizer] 개인화 블록에서 참조하기 전에 스키마에 특성을 정의해야 합니다.

  조건에서 프로필 특성을 활용하는 방법에 대한 자세한 내용은 [이 섹션](functions/helpers.md#if-function)을 참조하세요.

  +++샘플 참조

   * `{{profile.person.name.fullName}}`
   * `{{profile.person.name.firstName}}`
   * `{{profile.person.gender}}`
   * `{{profile.personalEmail.address}}`
   * ` {{profile.mobilePhone.number}}`
   * `{{profile.homeAddress.city}}`
   * `{{profile.faxPhone.number}}`

+++

* **대상자**

  세분화 서비스에 대한 자세한 내용은 [이 설명서](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=ko){target="_blank"}를 참조하세요.

* **오퍼**

  이 네임스페이스를 사용하면 기존 오퍼 결정을 참조할 수 있습니다.

  오퍼를 참조하려면 오퍼를 정의하는 다양한 정보가 있는 경로를 선언해야 합니다. 이 경로의 구조는 다음과 같습니다.

  `offers.Type.[Placement Id].[Activity Id].Attribute`

  여기서:

   * `offers`은(는) 오퍼 네임스페이스에 속하는 경로 식을 식별합니다
   * `Type`이(가) 오퍼 표시 형식을 결정합니다. 가능한 값은 `image`, `html` 및 `text`입니다.
   * `Placement Id` 및 `Activity Id`은(는) 배치 및 활동 식별자입니다.
   * `Attributes`은(는) 오퍼 유형에 따라 다른 오퍼 특정 특성입니다. 예제: `deliveryUrl`(이미지)

  Decisions API 및 오퍼 표시에 대한 자세한 내용은 [이 페이지](../offers/api-reference/offer-delivery-api/decisioning-api.md)를 참조하세요.

  [이 페이지](../personalization/personalization-build-expressions.md)에 설명된 유효성 검사 메커니즘을 사용하여 오퍼 스키마에 대해 모든 참조의 유효성을 검사합니다.

  +++샘플 참조

   * 이미지가 호스팅되는 위치:

     `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].deliveryUrl`

   * 이미지를 클릭할 때 대상 URL:

     `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].linkUrl`

   * 의사 결정 엔진에서 제공되는 오퍼의 텍스트 콘텐츠:

     `offers.text.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`

   * decisioning 엔진에서 제공하는 오퍼의 HTML 콘텐츠:

     `offers.html.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`

+++

## 도우미{#helpers-all}

Handlebars 도우미는 매개 변수 뒤에 올 수 있는 간단한 식별자입니다. 각 매개 변수는 Handlebars 표현식입니다. 이러한 도우미는 템플릿의 모든 컨텍스트에서 액세스할 수 있습니다.

이러한 블록 도우미는 도우미 이름 앞에 `#`이(가) 있어 같은 이름의 일치하는 닫는 `/`이(가) 필요합니다.

블록은 블록 열기(`{{# }}`)와 닫기(`{{/}}`)가 있는 식입니다.

도우미 함수에 대한 자세한 내용은 [이 섹션](functions/helpers.md)을 참조하세요.

## 리터럴 유형 {#literal-types}

[!DNL Adobe Journey Optimizer]은(는) 다음 리터럴 형식을 지원합니다.

| 리터럴 | 정의 |
| ------- | ---------- |
| 문자열 | 큰따옴표로 묶인 문자로 구성된 데이터 유형입니다. <br>예: `"prospect"`, `"jobs"`, `"articles"` |
| 부울 | true 또는 false인 데이터 유형입니다. |
| 정수 | 정수를 나타내는 데이터 형식입니다. 양수, 음수 또는 0일 수 있습니다. <br>예: `-201`, `0`, `412` |
| 배열 | 다른 리터럴 값의 그룹으로 구성된 데이터 유형입니다. 대괄호를 사용하여 그룹화하고 쉼표를 사용하여 서로 다른 값 사이를 구분합니다. <br> **참고:** 배열 내의 항목 속성에 직접 액세스할 수 없습니다. <br> 예: `[1, 4, 7]`, `["US", "FR"]` |

>[!CAUTION]
>
>개인화 식에는 **xEvent** 변수를 사용할 수 없습니다. xEvent에 대한 모든 참조는 유효성 검사 실패를 초래합니다.
