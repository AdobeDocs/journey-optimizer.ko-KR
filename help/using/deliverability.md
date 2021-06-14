---
title: 메시지 실행 모니터링
description: 모니터링 및 게재 기능 지침 학습
feature: 전달성
topic: 콘텐츠 관리
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 0%

---

# 게재 기능 관리 {#manage-deliverability}

![](assets/do-not-localize/badge.png)

게재 기능은 수신자의 받은 편지함에 도달하는 게재의 성공을 측정하는 것입니다.

**이메일** 게재 기능은 짧은 시간 내에 개인 이메일 주소를 통해 메시지 대상에 도달하고 콘텐츠 및 형식 측면에서 예상되는 품질을 결정하는 일련의 특성을 나타냅니다. 이러한 특징은 네 가지 주요 범주로 분류됩니다.데이터 품질, 메시지 및 컨텐츠, 전송 인프라, 평판. 이들은 함께 성공적인 이메일 게재 가능성 프로그램의 기반을 형성합니다.

**게재능력률**&#x200B;은 배달된 메시지 수와 비교하여 수신자의 받은 편지함에 도달하는 메시지 수입니다. 그것은 많은 요인들에 따라, 특히 다음과 같이 달라집니다.

* 제한된 스팸 불만
* 낮은 하드 바운스 비율
* 타겟팅된 주소의 품질
* 메시지 콘텐츠
* 보낸 사람 평판

[!DNL Journey Optimizer] 경험의 게재 능력을 최적화하려면 이 섹션에 나열된 우수 사례를 사용하는 것이 좋습니다. 게재 기능 문제는 일반적으로 인터넷 서비스 공급자(ISP) 및 메일 서버 관리자가 구현하는 스팸으로부터 보호하는 것과 연결되어 있습니다.

## 불만 비율 {#reduce-complaint-rate} 감소

ISP에는 보통 받은 메시지를 스팸으로 보고하는 잘 알려진 방법이 있습니다. 이렇게 하면 신뢰할 수 없는 출처를 식별할 수 있습니다. 옵트아웃 요청을 빠르게 준수하고 따라서 신뢰할 수 있는 발신자임을 나타냄에 따라 불만율을 줄일 수 있습니다. [옵트아웃 관리에 대해 자세히 알아보십시오](consent.md#opt-out-management).

일반적으로, 예를 들어 이메일 주소나 이름과 같은 필드를 작성할 것을 요구하여 옵트아웃하려는 수신자의 방해가 되지 않도록 하십시오. 구독 취소 랜딩 페이지에는 하나의 유효성 검사 단추만 있어야 합니다.

추가 확인을 요청할 때 추가 서비스 제공:사용자는 두 개의 이메일 주소를 동일한 상자로 리디렉션할 수 있습니다(예:firstname.lastname@club.com 및 firstname.lastname@internet-club.com). 프로필에서 첫 번째 주소만 기억할 수 있고 다른 주소로 전송된 메시지를 통해 구독을 취소하려는 경우 암호화된 식별자와 입력한 이메일 주소가 일치하지 않으므로 양식이 이 요청을 거부합니다.

## 제외 목록 사용 {#suppression-lists}

[!DNL Journey Optimizer] 일관되게 발생하는 스팸 불만, 하드 바운스 및 소프트 바운스를 수집하는 억제 목록을 관리합니다.

게재 능력을 보호하기 위해 이 연락처에 보내는 것은 보내는 명성을 손상시킬 수 있으므로 주소가 제외 목록에 있는 수신자는 기본적으로 모든 향후 게재에서 제외됩니다.

[제외 목록에 대해 자세히 알아보십시오](suppression-list.md).

## 모니터링 도구 사용 {#monitoring-tools}

[!DNL Journey Optimizer]에서 제공하는 기능을 사용하여 게재 능력을 모니터링합니다.

메시지 목록의 **[!UICONTROL Executions]** 탭에서는 일련의 실시간 표시기를 통해 게재가 어떻게 작동하는지 확인할 수 있습니다. 다른 항목 중에서 이 탭에 다음이 표시됩니다.
* 실행, 전송 및 전달된 메시지 수입니다.
* 열린 메시지 수와 클릭한 메시지/링크 수입니다.

[메시지 실행 모니터링에 대해 자세히 알아보십시오](message-monitoring.md).

## 메시지 내용 조정 {#adapt-message-content}

어느 정도, 특정 메시지의 내용은 스팸으로 탐지될 수 있습니다.

<!--The use of certain words or of exclamation points in the subject line and within the messages can be read as signs of spam.

Spammers are also known to replace text with images to stop offending text from being analyzed automatically by anti-spam filters. In response to this, a message (in HTML format) with a high proportion of images, or images as attachments, may end up being blocked.-->

게재 능력을 향상시키고 이메일이 수신자에게 도달하는지 확인하려면 메시지 콘텐츠를 디자인할 때 아래 원칙을 따르십시오.

* **발신자 이름 및 주소**:주소는 발신자를 명시적으로 식별해야 합니다. 도메인은 의 소유가 되어야 하며 발신자에게 등록해야 합니다. 도메인 레지스트리를 민영화해서는 안 됩니다.

<!--* **Subject**: Avoid excessive capitalization and punctuation, and words that are frequently used by spammers ("Win", "Free", etc.).
* **Personalize your email**: Personalizing the email increases the chances of your message being opened.
* **Images and text**: Respect a decent text/image ratio (for example 60% text and 40% images).-->
* **링크 및 랜딩 페이지 구독 취소**:가입 해지 링크는 필수입니다. 이 변수는 표시적이고 유효해야 하며 양식이 작동해야 합니다.

<!--**Use tools** offered by Journey Optimizer to optimize the content of your email (delivery analysis, anti-spam analysis).-->

[이메일 콘텐츠 디자인에 대한 자세한 내용을 살펴보십시오](design-emails.md).
