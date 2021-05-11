---
title: 개인화 유효성 검사
description: 개인화 유효성 검사와 문제 해결 방법에 대한 자세한 내용
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%

---

# 개인화 유효성 검사 {#personalization-validation}

![](../assets/do-not-localize/badge.png)

## 유효성 검사 메커니즘

표현식 편집기 화면에서 **유효성 검사** 단추를 사용하여 개인화 구문의 유효성을 검사할 수 있습니다.

>[!NOTE]
> 유효성 검사는 **추가**&#x200B;를 클릭하여 편집기 창을 닫을 때 자동으로 수행됩니다.


![](assets/perso_validation1.png)

>[!IMPORTANT]
> 개인화 구문이 올바르지 않으면 표현식 편집기 창을 닫을 수 없습니다.


## 일반적인 오류

* **경로 &quot;XYZ&quot;를 찾을 수 없습니다.**

스키마에 정의되지 않은 필드를 참조하려고 할 때.

이 경우 **firstName1**&#x200B;이(가) 프로필 스키마에 속성으로 정의되지 않았습니다.

```
{{profile.person.name.firstName1}}
```

* **변수 &quot;XYZ&quot;의 유형이 일치하지 않습니다. 배열이 필요합니다. 문자열을 찾았습니다.**

배열 대신 문자열을 반복하려고 할 때:

이 경우 **product**&#x200B;은(는) 배열이 아닙니다.

```
{{each profile.person.name.firstName as |product|}}
 {{product.productName}}
{{/each}}
```

* **잘못된 handlebars 구문입니다.`‘[XYZ}}’`**&#x200B;을(를) 찾았습니다.

잘못된 handlebars 구문을 사용하는 경우

handlebars 식은 **{{expression}}**&#x200B;로 둘러싸여 있습니다.

```
   {{[profile.person.name.firstName}}
```

* **잘못된 세그먼트 정의**

```
No segment definition found for 988afe9f0-d4ae-42c8-a0be-8d90e66e151
```

### 오퍼와 관련된 특정 오류

이메일 또는 푸시 메시지의 오퍼 통합과 관련된 오류는 다음 패턴을 가집니다.

```
Offer.<offerType>.[PlacementID].[ActivityID].<offer-attribute>
```

메시지 게시 도중 또는 표현식 편집기에서 개인화 컨텐츠 유효성 검사 중에 유효성 검사가 수행됩니다.

<table> 
 <thead> 
  <tr> 
   <th> 오류 제목<br /> </th> 
   <th> 유효성 검사 / 해상도 <br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>id placementID가 있고 OfferPlacement 유형이 <br/>인 리소스를 찾을 수 없습니다.
id activityID 및 유형의 OfferActivity가 있는 리소스를 찾을 수 없습니다.<br/></td> 
   <td>ActivityID 및/또는 PlacementID를 사용할 수 있는지 확인</td> 
  </tr> 
   <tr> 
   <td>리소스를 확인할 수 없습니다.</td> 
   <td>배치의 componentType은 offerType 오퍼와 일치해야 합니다</td> 
  </tr> 
   <tr> 
   <td>공개 URL이 offerId에 없습니다.</td> 
   <td>이미지 오퍼(의사 결정 및 배치 쌍과 연관된 모든 개인화된 및 폴백)에는 공개 URL이 채워져야 합니다(deliveryURL은 비워 둘 수 없습니다).</td> 
  </tr> 
  <tr> 
   <td>의사 결정(이전의 오퍼 활동이라고 함)에는 비프로필 속성이 포함되어 있습니다.</td> 
   <td>오퍼 모델 사용에는 프로필 속성만 포함되어야 합니다.</td> 
  </tr> 
  <tr> 
   <td>의사 결정 사용을 가져오는 동안 오류가 발생했습니다.</td> 
   <td>이 오류는 API가 오퍼 모델을 가져오려고 할 때 발생할 수 있습니다.</td> 
  </tr>
  <tr> 
   <td>오퍼 속성 오퍼 속성이 잘못되었습니다.</td> 
   <td>오퍼 드롭에서 참조된 오퍼 속성이 유효한지 확인합니다. 다음은 유효한 속성입니다.<br/>
이미지:deliveryURL, linkURL<br/>
텍스트:콘텐트<br/>
HTML:콘텐트<br/></td> 
  </tr> 
 </tbody> 
</table>

