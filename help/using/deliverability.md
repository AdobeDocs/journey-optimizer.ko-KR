---
title: 메시지 실행 모니터링
description: 모니터링 및 전달 가능성 지침 학습
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '552'
ht-degree: 0%

---

# 배달 가능 관리 {#manage-deliverability}

![](assets/do-not-localize/badge.png)

배달은 수신자에게 배달되는 배달이 받은 편지함으로 배달되는 데 성공한 척도입니다.

**이메일** 배달은 짧은 시간 내에, 컨텐츠 및 형식 측면에서 예상되는 품질과 함께, 메시지가 대상에 도달할 수 있는 능력을 결정하는 일련의 특성을 의미합니다. 이러한 특성은 4가지 주요 카테고리로 분류됩니다.데이터 품질, 메시지 및 컨텐츠, 전송 인프라 및 명성을 높일 수 있습니다. 성공적인 이메일 제공 프로그램의 기반이 됩니다.

**배달율**&#x200B;은 배달된 메시지 수와 비교하여 받는 사람의 받은 편지함을 히트한 메시지 수입니다. 이것은 많은 요인들에 따라, 특히 다음과 같습니다.

* 제한적인 스팸 불만 사항
* 낮은 하드 바운스 비율
* 타깃팅된 주소의 품질
* 메시지 내용
* 보낸 사람 평판

[!DNL Journey Optimizer] 경험의 제공 능력을 최적화하기 위해 이 섹션에 나열된 우수 사례를 사용하는 것이 좋습니다. 제공 가능성 문제는 일반적으로 인터넷 서비스 공급자(ISP) 및 메일 서버 관리자가 구현한 스팸으로부터 보호하는 것과 관련이 있습니다.

## 불만 비율 {#reduce-complaint-rate} 감소

ISP는 일반적으로 수신한 메시지를 스팸으로 보고하는 뛰어난 방법을 가지고 있습니다. 따라서 신뢰할 수 없는 출처를 식별할 수 있습니다. 수신 거부 요청을 신속하게 준수하고 신뢰할 수 있는 발신자임을 보여주면 불만 요율을 줄일 수 있습니다. [옵트아웃 관리에 대해 자세히 알아보십시오](consent.md#opt-out-management).

일반적으로 이메일 주소 또는 이름과 같은 필드를 채우도록 요구함으로써 수신을 거부하려는 수신자의 방해가 되지 않도록 합니다. 구독 취소 랜딩 페이지에는 하나의 유효성 확인 단추만 있어야 합니다.

추가 확인을 요청할 때 추가 관리:사용자는 동일한 상자로 리디렉션된 두 개의 이메일 주소를 가질 수 있습니다(예:firstname.lastname@club.com 및 firstname.lastname@internet-club.com)을 참조하십시오. 프로필이 첫 번째 주소만 기억할 수 있고 다른 주소로 보낸 메시지를 통해 구독을 취소하려는 경우, 암호화된 식별자와 입력한 이메일 주소가 일치하지 않기 때문에 양식이 거부됩니다.

## 제외 목록 사용 {#suppression-lists}

[!DNL Journey Optimizer] 일관되게 발생하는 스팸 불만, 하드 바운스 및 소프트 바운스를 수집하는 억제 목록을 관리합니다.

배달 능력을 보호하기 위해, 수신 거부 목록에 있는 주소가 있는 수신자는 이러한 연락처로 보내는 것이 사용자의 전송 명성을 손상시킬 수 있으므로 모든 향후 배달에서 기본적으로 제외됩니다.

[제외 목록에 대해 자세히 알아보십시오](suppression-lists.md).

## 모니터링 도구 사용 {#monitoring-tools}

[!DNL Journey Optimizer]에서 제공하는 기능을 사용하여 배달 능력을 모니터링합니다.

메시지 목록의 **[!UICONTROL Executions]** 탭에서는 일련의 실시간 표시기를 통해 배달이 어떻게 수행되는지 확인할 수 있습니다. 다른 것들 중에서 이 탭은 다음과 같이 표시됩니다.
* 성공적으로 실행, 전송 및 배달된 메시지 수입니다.
* 연 메시지 수와 클릭한 메시지/링크 수입니다.

[메시지 실행 모니터링에 대해 자세히 알아보십시오](message-monitoring.md).

## 메시지 내용 적용 {#adapt-message-content}

어느 정도, 특정 메시지의 컨텐츠가 스팸으로 감지될 수 있습니다.

<!--The use of certain words or of exclamation points in the subject line and within the messages can be read as signs of spam.

Spammers are also known to replace text with images to stop offending text from being analyzed automatically by anti-spam filters. In response to this, a message (in HTML format) with a high proportion of images, or images as attachments, may end up being blocked.-->

배달율을 향상시키고 이메일을 수신자에게 확실히 전달하려면 메시지 컨텐츠를 디자인할 때 아래 원칙을 따르십시오.

* **보낸 사람 이름 및 주소**:주소는 발신자를 명시적으로 식별해야 합니다. 도메인을 소유해야 하며 발신자에게 등록되어 있어야 합니다. 도메인 레지스트리를 민영화하지 않아야 합니다.

<!--* **Subject**: Avoid excessive capitalization and punctuation, and words that are frequently used by spammers ("Win", "Free", etc.).
* **Personalize your email**: Personalizing the email increases the chances of your message being opened.
* **Images and text**: Respect a decent text/image ratio (for example 60% text and 40% images).-->
* **링크 및 랜딩 페이지 구독 취소**:가입 해지 링크는 필수입니다. 표시 및 유효해야 하며 양식이 제대로 작동하는지 확인해야 합니다.

<!--**Use tools** offered by Journey Optimizer to optimize the content of your email (delivery analysis, anti-spam analysis).-->

[이메일 컨텐츠 디자인에 대한 자세한 내용을 살펴보십시오](design-emails.md).
