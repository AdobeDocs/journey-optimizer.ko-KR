---
solution: Journey Optimizer
product: journey optimizer
title: 비용 최적화를 위한 SMS 모범 사례
description: Journey Optimizer에서 문자 제한, 인코딩 및 개인화를 관리하여 SMS 메시지 비용을 최적화하는 방법을 알아봅니다
feature: SMS
topic: Content Management
role: User
level: Intermediate
source-git-commit: 7eaca4faf61431fa438afc7550ff4b89f95fa192
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---

# SMS 비용 최적화 우수 사례 {#sms-cost-optimization}

SMS 메시지는 일반적으로 제공업체에서 메시지당 160자 제한을 기준으로 청구합니다. SMS 메시지를 여러 부분으로 분할하면 추가 비용이 발생할 수 있습니다.

메시징 전략을 최적화하고 비용을 줄이려면 다음 지침을 따르십시오.

## 짧은 메시지 유지 {#keep-messages-short}

Journey Optimizer에서는 SMS 메시지 본문에 최대 1,500자를 사용할 수 있습니다. 이 제한을 초과하면 경고가 표시되며, 이 임계값을 초과하는 메시지는 오류를 트리거합니다.

대부분의 SMS 공급자는 GSM 7비트 인코딩을 지원하며, 여기서 단일 SMS에는 최대 160자가 포함될 수 있습니다. 이 길이를 초과하는 메시지는 자동으로 여러 SMS 부분으로 분할됩니다(연결).

* **160자 미만**: SMS 파트 1개
* **161-306자**: SMS 파트 2개
* **307-459자**: SMS 파트 3개

**비용을 최소화하려면** 메시지를 160자 미만으로 유지해야 하므로 단일 SMS 부분으로 청구됩니다.

예를 들어 Journey Optimizer에서 1,600자로 된 메시지는 단일 메시지로 표시되지만 10개의 SMS 크레딧을 사용할 수 있습니다.

## 길이가 늘어나는 특수 문자는 사용하지 마십시오 {#avoid-special-characters}

특정 문자(예: `| ^ € { } [ ] ~ \`)는 GSM 인코딩에서 두 문자로 계산됩니다. 이 문자를 포함하면 메시지가 **160자 제한**&#x200B;을(를) 더 빨리 초과할 수 있습니다.

## UCS-2 인코딩 방지 {#prevent-ucs2-encoding}

메시지에 중국어 또는 아랍어 텍스트, 상표 기호 또는 서식 있는 도구의 하드 리턴과 같은 GSM이 아닌 문자가 포함된 경우 공급자는 SMS당 70자만 지원하는 UCS-2를 사용하여 메시지를 인코딩합니다.

UCS-2 인코딩을 사용하면 문자 수가 증가하여 서비스 공급자와의 메시지 청구에 영향을 줄 수 있습니다.

예를 들어 200자의 유니코드 메시지는 3개의 SMS 파트로 전달됩니다.

## 작성 모범 사례 {#authoring-best-practices}

최종 SMS 메시지를 Journey Optimizer 내에서 직접 작성하거나 일반 텍스트 애플리케이션에서 붙여넣습니다.

리치 텍스트 애플리케이션은 UCS-2 인코딩을 트리거하는 숨겨진 문자 또는 줄 바꿈을 도입할 수 있으므로 SMS 부분 수와 관련 비용이 모두 증가할 수 있으므로 사용하지 마십시오.

## 보내기 전 문자 수 확인 {#check-character-count}

일반 텍스트 응용 프로그램 또는 Journey Optimizer **[!UICONTROL 콘텐츠 시뮬레이션]** 메뉴를 사용하여 문자 수를 확인합니다.

Journey Optimizer은 컨텐츠 시뮬레이션 중에 공백을 포함한 문자 수를 표시하지만, 다음 사항에 유의하십시오.

* 동적 개인화를 통해 생성된 문자 또는 특정 특수 문자를 포함하지 **않습니다**.

* **x/1500 count**&#x200B;은 메시지당 제한(예: 160자 GSM 7비트 제한)이 아닌 기술 페이로드 제한의 시각적 표시기 역할을 합니다.

* Adobe은 편집기에서 GSM-7비트 인코딩과 다른 UTF-8 인코딩을 지원합니다.

## 보고 이해 {#understanding-reporting}

**Journey Optimizer 보고**&#x200B;에서는 SMS 부분에 관계없이 전체 메시지를 한 번의 전송으로 계산합니다. 이렇게 하면 참여 가능한 프로필 양을 줄이는 데 도움이 됩니다.

**공급자 보고**&#x200B;는 배달할 실제 SMS 부분을 표시하므로 청구 및 초과를 확인하는 데 사용해야 합니다.

## Personalization 고려 사항 {#personalization-considerations}

동적 개인화는 메시지의 길이를 늘릴 수 있습니다. 예를 들어, 변수를 긴 이름으로 대체하면 문자를 추가할 수 있습니다.

## 추가 리소스 {#additional-resources}

[Sinch 문자 지원 안내서](https://developers.sinch.com/docs/sms/resources/message-info/character-support/)에서 지원되는 문자 및 인코딩 규칙을 검토합니다.

