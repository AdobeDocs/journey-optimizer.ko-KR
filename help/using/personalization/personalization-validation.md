---
solution: Journey Optimizer
product: journey optimizer
title: 개인화 유효성 검사
description: 개인화 유효성 검사 및 문제 해결 방법에 대해 자세히 알아보십시오.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: 표현식, 편집기, 유효성 검사, 오류, 개인화
exl-id: 7abeec5e-743f-48fb-a4a6-056665e8bfda
source-git-commit: c0afa3e2bc6dbcb0f2f2357eebc04285de8c5773
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 1%

---

# 개인화 유효성 검사 {#personalization-validation}

## 유효성 검사 메커니즘 {#validation-mechanisms}

에서 **표현식 편집기** 화면, **유효성 검사** 버튼을 클릭하여 개인화 구문을 확인합니다.

>[!NOTE]
> 유효성 검사는 **추가** 단추를 클릭하여 편집기 창을 닫습니다.

![](assets/perso_validation1.png)

>[!IMPORTANT]
> 개인화 구문이 올바르지 않으면 표현식 편집기 창을 닫을 수 없습니다.

## 일반적인 오류 {#common-errors}

* **경로 &quot;XYZ&quot;를 찾을 수 없습니다.**

스키마에 정의되지 않은 필드를 참조하려고 할 때.

이 경우 **firstName1** 은 프로필 스키마에 속성으로 정의되지 않았습니다.

```
{{profile.person.name.firstName1}}
```

* **변수 &quot;XYZ&quot;에 대한 유형이 일치하지 않습니다. 배열이 필요합니다. 문자열을 찾았습니다.**

배열 대신 문자열을 반복하려고 할 때:

이 경우 **product** 배열이 아닙니다.

```
{{each profile.person.name.firstName as |product|}}
 {{product.productName}}
{{/each}}
```

* **handlebars 구문이 잘못되었습니다. 발견됨`‘[XYZ}}’`**

잘못된 handlebars 구문을 사용하는 경우.

Handlebars 식은 로 둘러싸여 있습니다. **{{expression}}**

```
   {{[profile.person.name.firstName}}
```

* **잘못된 세그먼트 정의**

```
No segment definition found for 988afe9f0-d4ae-42c8-a0be-8d90e66e151
```

## 오퍼와 관련된 특정 오류 {#specific-errors}

이메일 또는 푸시 메시지의 오퍼 통합과 관련된 오류는 다음 패턴을 갖습니다.

```
Offer.<offerType>.[PlacementID].[ActivityID].<offer-attribute>
```

유효성 검사는 표현식 편집기에서 개인화 컨텐츠 유효성 검사 중에 수행됩니다.

<table> 
 <thead> 
  <tr> 
   <th> 오류 제목<br /> </th> 
   <th> 유효성 검사 / 해결 <br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>ID placementID와 유형이 OfferPlacement인 리소스를 찾을 수 없음 <br/>
id activityID 및 유형이 OfferActivity인 리소스를 찾을 수 없음<br/></td> 
   <td>ActivityID 및/또는 PlacementID를 사용할 수 있는지 확인합니다</td> 
  </tr> 
   <tr> 
   <td>리소스의 유효성을 검사할 수 없습니다.</td> 
   <td>배치의 componentType은 offerType 오퍼와 일치해야 합니다</td> 
  </tr> 
   <tr> 
   <td>공개 URL이 offerId에 없습니다.</td> 
   <td>이미지 오퍼(결정 및 배치 쌍과 연결된 모든 개인화된 및 폴백)에는 공개 URL이 채워져야 합니다(deliveryURL은 비워 둘 수 없음).</td> 
  </tr> 
  <tr> 
   <td>이 결정에는 비프로필 속성이 포함됩니다.</td> 
   <td>오퍼 모델 사용에는 프로필 속성만 포함되어야 합니다.</td> 
  </tr> 
  <tr> 
   <td>의사 결정 사용을 가져오는 동안 오류가 발생했습니다.</td> 
   <td>이 오류는 API가 오퍼 모델을 가져오려고 할 때 발생할 수 있습니다.</td> 
  </tr>
  <tr> 
   <td>오퍼 속성 오퍼 특성이 잘못되었습니다.</td> 
   <td>오퍼 드롭에서 참조되는 오퍼 속성이 유효한지 확인합니다. 다음은 유효한 속성입니다. <br/>
이미지: deliveryURL, linkURL<br/>
텍스트: 콘텐츠<br/>
HTML: 콘텐츠<br/></td> 
  </tr> 
 </tbody> 
</table>
